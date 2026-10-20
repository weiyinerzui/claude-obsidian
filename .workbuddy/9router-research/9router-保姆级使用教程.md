# 9Router 保姆级使用教程（小白到进阶）

> 本教程整合自官方 GitHub 仓库、npm 包 README、仓库 `.env.example` / `docker-compose.yml` / `start.sh` / `DOCKER.md` 原始文件，以及 4 篇微信公众号深度报道。
> **数据来源均为一级权威源**（仓库文件全文已抓取核对），不是二手转述。
>
> - 官方仓库：https://github.com/decolua/9router
> - npm 包：https://www.npmjs.com/package/9router（当前版本 0.5.20）
> - 官网：https://9router.com
> - 协议：MIT（完全免费，可商用）

---

## 目录

1. [9Router 是什么 / 解决什么问题](#一9router-是什么--解决什么问题)
2. [核心功能一览](#二核心功能一览)
3. [安装部署（保姆级，三种方式）](#三安装部署保姆级三种方式)
4. [新手入门：5 分钟跑通第一个模型](#四新手入门5-分钟跑通第一个模型)
5. [进阶用法：组合路由 / 负载均衡 / 故障转移 / 监控](#五进阶用法)
6. [常见问题排查与最佳实践](#六常见问题排查与最佳实践)
7. [附录：环境变量速查表](#七附录环境变量速查表)

---

## 一、9Router 是什么 / 解决什么问题

### 一句话定义

9Router 是一个**跑在你本地的 AI 智能路由网关**：把 40+ AI 厂商、100+ 模型聚合到一个 **OpenAI 兼容的统一入口**（`http://localhost:20128/v1`），让你所有 AI 编程工具（Claude Code、Cursor、Copilot、Codex、Cline 等）只连这一个地址，由 9Router 自动在「订阅 → 廉价 → 免费」三层之间切换，**永不中断编码**。

### 它解决的 4 个真实痛点

| 痛点 | 9Router 的解法 |
|------|---------------|
| 订阅额度月底浪费（$20-50/月常剩一大半） | 实时追踪配额，榨干每一份订阅再降级 |
| 写到关键处突然「速率限制」打断 | 三层自动降级，毫秒级切换，无感知 |
| `git diff` / `grep` / `ls` 输出冗长，烧 Token | 内置 RTK Token Saver，自动压缩 tool_result，省 20-40% |
| 多工具多账号多密钥配置混乱 | 统一面板管理，对外只暴露一个地址 + 一个 Key |

### 技术栈（了解即可）

- Node.js 18+ / Next.js 16 / React 19
- 存储：三层 SQLite 容错（`better-sqlite3` → `node:sqlite` → WASM `sql.js`），全环境兼容不丢数据
- 协议：OpenAI 兼容 REST（`POST /v1/chat/completions`、`GET /v1/models`）+ MCP 桥接
- 默认端口：**20128**

---

## 二、核心功能一览

### 1. 三层智能降级（最核心）

请求失败时，按优先级自动切换，全程零停机：

```
订阅层（优先）→ 廉价 API 层（补给）→ 免费层（兜底）
```

- **订阅层**：你已付费的 Claude Code、Codex、Gemini、Copilot 订阅额度
- **廉价层**：GLM（¥0.6/1M Token）、MiniMax（¥0.2/1M）、DeepSeek 等
- **免费层**：Kiro AI、OpenCode Free、Vertex AI（新 GCP 账号 $300 额度）等

机制：**配额耗尽 → 自动切换 → 无感知续跑 → 不打断编码流程**。

### 2. RTK Token Saver（省 20-40%）

自动识别并压缩 `tool_result` 内容——这类内容含大量冗余结构化数据（git diff、目录列表、日志），是 Token 消耗大头。默认开启，无需额外插件。

> ⚠️ **一个重要澄清**：4 篇微信文章里有篇称 RTK 是「Rust 编写的、9Router 内置核心组件」。经核对独立项目 [rtk-ai/rtk](https://github.com/rtk-ai/rtk)，那个 Rust 版 RTK 是**另一个独立 CLI 工具**，其 README **并未提及 9router**。9Router 内置的 Token Saver 是自己的实现（可选接 Headroom sidecar 做更深度压缩）。两者名字撞车但不是一回事，别混淆。

### 3. 多账号负载均衡

同一服务商配多个账号，自动轮询、处理配额/速率限制。例：3 个 Claude Code 订阅账号自动轮询，单账号限流时自动切下一个。

### 4. 全平台工具兼容

官方明确支持 18+ 工具：Claude-Code、OpenClaw、Codex、OpenCode、Cursor、Antigravity、Cline、Continue、Droid、Roo、Copilot、Kilo Code、Gemini CLI、Qwen Code、iFlow、Crush、Crusher、Aider……任何兼容 OpenAI/Claude API 的工具都能接。

### 5. 可视化 Web 仪表盘

`http://localhost:20128` 提供：提供商管理、连接测试、用量监控、配额倒计时、实时请求日志、成本统计——**全程不用手写配置文件**。

### 6. MITM 透明代理（进阶）

可拦截硬编码端点的工具流量（如 Copilot、Antigravity 的内置端点），**无需改工具源码**就能接入路由。支持 Linux NSS DB 证书注入，适配 Chrome/Firefox/Snap 浏览器。

### 7. 高级特性（进阶用户关注）

- **Smart Combos（组合）**：把多个模型链成一个对外名称，sticky 轮询 + 故障转移
- **Cloud Sync + Tunnel**：Cloudflare 边缘隧道，300+ 全球节点远程访问
- **Proxy Pools**：Vercel 中继、出站代理、IP 轮换
- **Format Translator**：OpenAI / Anthropic / Gemini 格式互转
- **9 种服务类型**：Chat/LLM、Embeddings、TTS、STT、图像生成、视觉理解、视频生成、Web Search、Web Fetch——全走同一个 `/v1` 端点

---

## 三、安装部署（保姆级，三种方式）

### 前提条件

| 必需项 | 版本 | 检查命令 | 安装方法 |
|--------|------|---------|---------|
| **Node.js** | ≥ 18.0.0（推荐 20+） | `node -v` | https://nodejs.org |
| **npm** | 随 Node 自带 | `npm -v` | — |

可选：
- **Docker**（仅 Docker 部署需要）：https://www.docker.com
- **Git**（仅源码部署需要）

> 小白首选 **方式一（npm）**，最简单。服务器/VPS 选 **方式二（Docker）**。想改源码选 **方式三**。

---

### 方式一：npm 全局安装（推荐，桌面端最简）

```bash
# 1. 全局安装
npm install -g 9router

# 2. 启动（会自动打开浏览器到 http://localhost:20128）
9router
```

**CLI 常用参数：**

```bash
9router                    # 默认启动
9router --port 8080        # 自定义端口
9router --no-browser       # 不自动开浏览器
9router --skip-update      # 跳过自动更新检查
9router --help             # 查看所有选项
```

**不想全局装？用 npx 直接跑：**

```bash
npx 9router
```

#### 数据存哪了

| 系统 | 路径 |
|------|------|
| macOS / Linux | `~/.9router/db/data.sqlite` |
| Windows | `%APPDATA%\9router\db\data.sqlite` |
| Docker | `/app/data/db/data.sqlite` |

#### ⚠️ 小白常踩的坑

1. **`npm install -g` 报权限错误（Linux/macOS）**：别用 `sudo`（会留下 root 文件后续麻烦），改用 nvm 管理 Node，或配 npm prefix 到用户目录：
   ```bash
   mkdir ~/.npm-global
   npm config set prefix '~/.npm-global'
   echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.bashrc
   source ~/.bashrc
   ```
2. **Windows PowerShell 找不到 `9router` 命令**：npm 全局 bin 目录没在 PATH。重开终端，或手动把 `%APPDATA%\npm` 加入 PATH。
3. **Node 版本过低报错**：9Router 用了 Next.js 16，Node 必须 ≥18，建议 20+。用 `nvm install 20 && nvm use 20`。
4. **v0.4.50 在 Linux 下 npm 全局装后约 10 秒就退出**（已知 bug，非 TTY/systemd 重启循环问题）。升级到最新版：`npm i -g 9router@latest --prefer-online`。

---

### 方式二：Docker 部署（推荐服务器/VPS）

#### 2a. 最简一条命令（官方镜像）

```bash
docker run -d \
  --name 9router \
  -p 20128:20128 \
  -v "$HOME/.9router:/app/data" \
  -e DATA_DIR=/app/data \
  decolua/9router:latest
```

镜像发布在 Docker Hub（`decolua/9router:latest`）和 GHCR（`ghcr.io/decolua/9router`），多平台 `linux/amd64` + `linux/arm64`。

#### 2b. 生产级部署（带密码、自动重启、强制 API Key）

```bash
sudo docker run -d \
  --name 9router \
  --restart=unless-stopped \
  -p 20128:20128 \
  -v "$HOME/.9router:/app/data" \
  -e DATA_DIR=/app/data \
  -e JWT_SECRET='换成你的超长随机字符串' \
  -e INITIAL_PASSWORD='换成你的强密码' \
  -e HOSTNAME=0.0.0.0 \
  -e REQUIRE_API_KEY=true \
  decolua/9router:latest
```

参数说明：

| 变量 | 作用 | 必填？ |
|------|------|--------|
| `DATA_DIR` | 数据目录，让挂载生效 | ✅ Docker 必填 |
| `JWT_SECRET` | 会话签名密钥，**务必改成长随机串** | ✅ 生产必填 |
| `INITIAL_PASSWORD` | 首次登录后台密码，**务必改** | ✅ 生产必填 |
| `HOSTNAME=0.0.0.0` | 允许局域网访问（默认只监听 localhost） | 局域网访问必填 |
| `REQUIRE_API_KEY=true` | 强制所有 API 调用带 Key | 公网暴露必填 |

> 🔑 **关于初始密码的权威说明**：仓库 `.env.example` 写的默认值是 `INITIAL_PASSWORD=change-me`。**不是** `123456`。无论默认是什么，生产环境**必须改掉**。

#### 2c. Docker Compose（带 Headroom 深度压缩 sidecar）

仓库 `docker-compose.yml` 原文：

```yaml
services:
  9router:
    image: decolua/9router:latest
    container_name: 9router
    restart: always
    ports:
      - "20128:20128"
    volumes:
      - 9router-data:/app/data
    env_file:
      - .env
    environment:
      DATA_DIR: /app/data
      PORT: "20128"
      HOSTNAME: "0.0.0.0"
      NODE_ENV: production
      HEADROOM_URL: http://headroom:8787
    depends_on:
      - headroom

  headroom:
    image: ghcr.io/chopratejas/headroom:latest
    container_name: headroom
    restart: always
    ports:
      - "8787:8787"

volumes:
  9router-data:
    name: 9router-data
```

启动：

```bash
# 先准备 .env 文件（参考附录的环境变量表）
docker compose up -d
```

#### Docker 管理常用命令

```bash
docker logs -f 9router        # 实时看日志
docker stop 9router           # 停
docker start 9router          # 再启动
docker rm -f 9router          # 删容器（数据在挂载卷里，不丢）
docker pull decolua/9router:latest   # 更新镜像
```

#### Headroom（深度 Token 压缩，可选）

9Router 镜像**不含** Python/Headroom。要用 Headroom 做更激进的 Token 压缩，跑成独立服务并在 9Router 里指向它：

- Docker sidecar：`HEADROOM_URL=http://headroom:8787`（见上面 compose）
- Headroom 跑在宿主机：macOS/Windows 用 `http://host.docker.internal:8787`；Linux 加 `--add-host=host.docker.internal:host-gateway`
- 启用路径：仪表盘 → `Endpoint` → `Token Saver` → `Headroom` → 确认 URL → recheck → enable

#### ⚠️ Docker 部署踩坑（来自官方 issues 真实案例）

1. **自构建启动报 `Cannot find module '/app/server.js'`**（v0.4.31 报告）：`DOCKER_BUILDKIT=1 docker build -t 9router` 自构建路径不对。**用官方预构建镜像 `decolua/9router:latest` 别自己 build**。
2. **运行中容器里跑 `npm i -g 9router@latest` 会装坏**：更新要 `docker pull` 新镜像后重建容器，别在容器内升级。
3. **镜像 tag 标错版本**（如标 0.5.12 实际报 0.5.8）：以容器内实际版本为准，pull 最新 `:latest` 绕过。
4. **`start.sh` 脚本只适合源码自构建**，且它**不启动** headroom sidecar——生产用 compose，别用 start.sh。

---

### 方式三：源码部署（开发者/想改代码）

```bash
# 1. 克隆（国内 GitHub 连不上用镜像：ghfast.top）
git clone https://github.com/decolua/9router.git
# 镜像版：git clone https://ghfast.top/https://github.com/decolua/9router.git

cd 9router

# 2. 装依赖
npm install

# 3a. 开发模式
npm run dev

# 3b. 生产模式
npm run build
npm run start
```

> 源码自构建 Docker：`cd app && docker build -t 9router .`（注意坑：见上方 issue，建议优先用官方镜像）

---

## 四、新手入门：5 分钟跑通第一个模型

### 步骤 1：启动并登录后台

```bash
9router
```

浏览器自动打开 `http://localhost:20128`（手动访问 `http://localhost:20128/dashboard`）。

- 首次用 `INITIAL_PASSWORD`（npm 默认装可看启动日志；Docker 用你设的密码）登录
- 右上角可切**中文**界面

### 步骤 2：接入第一个免费模型（无需注册）

仪表盘 → **Providers（提供商）** → Free Tier Providers：

- 选 **OpenCode Free**（无需认证，直连）→ 一键 Connect
- 或 **Kiro AI**（免费 Claude，走 AWS Builder ID / Google / GitHub OAuth 登录）

> ⚠️ **时效性提醒（2026 年实测）**：免费渠道变动频繁。微信文章作者实测反馈：**Kiro AI 免费 Claude、Qoder 免费反代已不可用**，iFlow / Qwen 免费层 2026 年已下线。**目前稳的是 `OpenCode Free` 的 `deepseek-v4-flash-free`（无需身份验证）**。具体可用模型以你仪表盘实时「连接测试」结果为准——别轻信静态教程列表。

### 步骤 3：创建对外 API Key

仪表盘 → **Endpoint（端点）** 页面 → 新建 API Key → **保存好这串 Key**（只显示一次）。

### 步骤 4：在 AI 工具里接入（以 Claude Code 为例）

编辑 `~/.claude/config.json`（或其他工具的等价配置）：

```json
{
  "anthropic_api_base": "http://localhost:20128/v1",
  "anthropic_api_key": "你在面板生成的 API Key"
}
```

**其他工具通用配置：**

| 配置项 | 值 |
|--------|-----|
| Endpoint / API Base | `http://localhost:20128/v1` |
| API Key | 面板生成的 Key |
| Model | 从提供商列表复制，如 `oc/deepseek-v4-flash-free` 或 `kr/claude-sonnet-4.5` |

重启工具即可。> 远程访问（VPS 部署）：把 `localhost` 换成服务器 IP，确保 Docker 设了 `HOSTNAME=0.0.0.0` 和 `REQUIRE_API_KEY=true`。

### 步骤 5：测试是否成功

```bash
# 用 curl 直接打 OpenAI 兼容接口
curl http://localhost:20128/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer 你的APIKey" \
  -d '{
    "model": "oc/deepseek-v4-flash-free",
    "messages": [{"role":"user","content":"说一句你好"}]
  }'
```

返回正常 JSON 回复 = 成功。也可在仪表盘「实时请求日志」看到这次调用。

> ⚠️ **测试踩坑**：仪表盘「连接测试」标绿的模型，**外部 CLI 调用时仍可能失败**（挂起 / 403 / 超时 / 406）。常见原因：请求**漏了 `stream` 参数**（如 Dify 的 OpenAI 兼容插件发 `{"model":"9router-combo","max_tokens":5,"messages":[...]}` 不带 stream）。调试时先加 `"stream": false` 试试。日志里若出现 `POST /v1/v1/messages` 这种**路径前缀重复**，说明客户端 base URL 多写了 `/v1`，去掉一层。

---

## 五、进阶用法

### 1. 组合路由（Smart Combos）—— 最实用的进阶功能

把多个模型编进一个「组合」，对外暴露一个名字，内部智能切换。某模型挂了/限额，自动用下一个，对调用方无感。

**配置步骤：**

1. 仪表盘左侧 → **Combos（组合）** → 新建
2. 起名，如 `9rtmodel`
3. 添加模型（从已添加的提供商里选，**务必先单独测好每个可用**）
4. 对外用组合名当 model 调用

调用示例：

```bash
curl http://localhost:20128/v1/chat/completions \
  -H "Authorization: Bearer 你的Key" \
  -H "Content-Type: application/json" \
  -d '{"model":"9rtmodel","messages":[{"role":"user","content":"hi"}]}'
```

**两种调度模式：**
- **顺序兜底**（默认）：按编排顺序调用，某个不可用才下一个 —— 适合「主用 A，挂了用 B」
- **轮询**（可开启）：轮流调用各模型 —— 适合负载均衡、均摊用量

### 2. 多账号负载均衡

同一提供商加多个账号 → 自动轮询 → 单账号限流自动切下一个。例：3 个 Claude Code 订阅账号，9Router 自动在它们之间分发请求，提升利用率、规避单号限流。

### 3. 故障转移（三层降级配置）

在组合或全局策略里编排优先级：

```
Claude Code 订阅（Tier1）→ GLM 廉价（Tier2）→ OpenCode Free（Tier3）
```

配额耗尽/限流/宕机时自动降级，无需人工干预。

### 4. 速率限制与配额管理

- 仪表盘实时显示各渠道 **Token 消耗 / 剩余额度 / 重置倒计时**
- 系统主动从 Gemini / GLM / MiniMax 等 API 查实时配额，**耗尽前主动切换**
- 多账号轮询天然规避单号速率限制

### 5. MITM 透明代理（拦截硬编码端点工具）

对 Copilot、Antigravity 等端点硬编码的工具，无需改源码，9Router 直接拦截其流量接入路由。支持 Linux NSS DB 证书注入（Chrome/Firefox/Snap）。

### 6. 出站代理（国内访问国际模型必备）

9Router 支持给上游 provider 调用走代理，大小写环境变量都认：

```bash
# .env 或 docker -e
HTTP_PROXY=http://127.0.0.1:7890
HTTPS_PROXY=http://127.0.0.1:7890
ALL_PROXY=socks5://127.0.0.1:7890
NO_PROXY=localhost,127.0.0.1
```

这对国内用户访问 OpenAI / Anthropic / Gemini 等国际 API 是关键配置。

### 7. Cloud Sync + Tunnel（远程访问）

Cloudflare 边缘隧道，300+ 全球节点，把你本地 9Router 暴露成公网可访问的端点（适合在外网用家里的 9Router）。

### 8. Format Translator

OpenAI / Anthropic / Gemini 三种格式互转——让只认 Anthropic 格式的工具能调 OpenAI 模型，反之亦然。

### 9. 监控统计

仪表盘提供：
- 各渠道 Token 消耗与额度
- 实时路由切换日志
- 成本统计与趋势
- 模型可用性监控
- 单次调用成本、账号负载、限流状态

### 10. 权限控制

- `REQUIRE_API_KEY=true`：强制所有 API 调用带 Key
- `JWT_SECRET`：会话签名
- `AUTH_COOKIE_SECURE`：Cookie 安全标志（HTTPS 部署时设 true）
- 每个对外 Key 可独立管理/吊销

---

## 六、常见问题排查与最佳实践

### 常见问题

| 现象 | 原因 | 解决 |
|------|------|------|
| 启动后 `localhost:20128` 打不开 | 端口被占 / 未监听 | `9router --port 8080` 换端口；Docker 确认 `-p 20128:20128` |
| npm 全局装后命令找不到 | bin 目录不在 PATH | 重开终端；Windows 加 `%APPDATA%\npm` 到 PATH |
| Node 报语法/模块错误 | Node < 18 | `nvm install 20 && nvm use 20` |
| Linux npm 装后 10 秒退出 | v0.4.50 已知 bug | 升级 `npm i -g 9router@latest` |
| Docker 自构建报 `Cannot find module '/app/server.js'` | 自构建路径问题 | **用官方镜像 `decolua/9router:latest`**，别自 build |
| 容器内升级后坏了 | 在运行容器里 `npm i -g` | `docker pull` 新镜像后**重建容器** |
| 仪表盘测试绿，外部调用失败 | 漏 `stream` 参数 / 路径重复 | 加 `"stream":false`；检查 base URL 别多 `/v1` |
| 日志出现 `POST /v1/v1/messages` | 客户端 base URL 多写了 `/v1` | base 改成 `http://localhost:20128/v1`（只一层） |
| 403 / 超时 / 挂起 | 国际模型需代理 / OAuth 过期 | 配 `HTTP_PROXY`；重新 OAuth 授权 |
| 免费模型突然不可用 | 免费渠道时效性强 | 以仪表盘实时测试为准；多备几个组合兜底 |
| 镜像 tag 与实际版本不符 | 发布标注 bug | pull `:latest`，以容器内实际版本为准 |
| 局域网其他设备访问不到 | 只监听 localhost | Docker 加 `HOSTNAME=0.0.0.0` |
| 公网部署不安全 | 默认无强制 Key | 必设 `REQUIRE_API_KEY=true` + 强密码 + 改 `JWT_SECRET` |

### 最佳实践

1. **生产环境三件套必改**：`JWT_SECRET`（长随机）、`INITIAL_PASSWORD`（强密码）、`REQUIRE_API_KEY=true`。公网暴露缺一不可。
2. **数据持久化**：Docker 必须 `-v ...:/app/data` + `-e DATA_DIR=/app/data`，否则容器删了配置全没。
3. **组合优先**：别单点依赖一个模型。建组合，主用 + 廉价兜底 + 免费保活三层。
4. **先测后用**：组合里每个模型先单独「连接测试」通过再加入，否则组合会因坏模型卡住。
5. **免费渠道别迷信**：时效性强，定期复核；核心生产用廉价付费层（GLM/MiniMax/DeepSeek）更稳。
6. **更新走镜像重建**：Docker 用 `docker pull` + 重建，别在容器内 `npm i -g`。
7. **国内访问国际模型**：务必配 `HTTP_PROXY` / `HTTPS_PROXY` 出站代理。
8. **监控用量**：定期看仪表盘成本统计，避免某个昂贵模型被组合误调产生高费。
9. **备份 SQLite**：`$DATA_DIR/db/data.sqlite` 是全部配置，定期拷一份（目录下有 `backups/` 自动备份）。

---

## 七、附录：环境变量速查表

来自仓库 `.env.example` 原文：

| 变量 | 默认值 | 说明 |
|------|--------|------|
| `JWT_SECRET` | `change-me-to-a-long-random-secret` | 会话签名，**必改** |
| `INITIAL_PASSWORD` | `change-me` | 首次登录密码，**必改** |
| `DATA_DIR` | `/var/lib/9router` | 数据目录，Docker 设 `/app/data` |
| `PORT` | `20128` | 服务端口 |
| `NODE_ENV` | `production` | 运行环境 |
| `API_KEY_SECRET` | `endpoint-proxy-api-key-secret` | 端点代理 Key 密钥 |
| `MACHINE_ID_SALT` | `endpoint-proxy-salt` | 机器 ID 盐 |
| `ENABLE_REQUEST_LOGS` | `false` | 请求日志开关 |
| `OBSERVABILITY_ENABLED` | `true` | 可观测性 |
| `AUTH_COOKIE_SECURE` | `false` | HTTPS 部署设 `true` |
| `REQUIRE_API_KEY` | `false` | 强制 API Key，公网必设 `true` |
| `BASE_URL` | `http://localhost:20128` | 本实例地址（云同步内部用） |
| `CLOUD_URL` | `https://9router.com` | 云同步地址 |
| `HEADROOM_URL` | — | Headroom 压缩 sidecar 地址 |
| `HTTP_PROXY` / `HTTPS_PROXY` / `ALL_PROXY` / `NO_PROXY` | — | 出站代理（大小写都认） |

---

## 数据来源声明

本教程关键技术细节均核对自一级源：

- **仓库文件原文**：`.env.example`、`docker-compose.yml`、`start.sh`、`DOCKER.md`（通过镜像抓取全文）
- **npm 包元数据**：registry.npmmirror.com/9router（版本 0.5.20，engines node≥18，MIT）
- **npm README**：官方 Quick Start / CLI Options / Data Location / Supported Tools
- **官方 issues**：真实踩坑案例（自构建报错、版本标错、外部调用失败、路径重复）
- **4 篇微信文章**：项目背景、功能解读、Docker 实操、组合路由实操

> ⚠️ 免费模型可用性具有强时效性（Kiro/Qoder/iFlow/Qwen 免费层 2026 年实测有变动）。**一切以你本地仪表盘的实时「连接测试」为准**，本教程不保证任何特定免费渠道长期可用。
