 ▐▛███▜▌   Claude Code v2.1.170
▝▜█████▛▘  google/gemini-3.5-flash · API Usage Billing
  ▘▘ ▝▝    E:\workspace\github\claude-obsidian


❯ /model                                                                        
  ⎿  Set model to qnaigc/google/gemini-3.5-flash and saved as your default for
     new sessions

❯ /wiki /skill ljg-learn the theme of my presentation is code as a medium for   
storytelling i think because I don't come from a traditional background I think 
of coding from a different lens from most professional engineers or             
programmers and so today I'll talk about a few things i'll go through uh my own 
background how I started VIP coding and the projects I've built and how I       
built them and then why it matters so first where I started so I actually never 
thought of myself as a coder i studied humanities in school i never took CS     
actually in 2023 I wrote a blog post called why I'm not learning to code that   
kind of went viral so at that point I was like I'm proudly a humanities person  
working in tech and I think tech needs more humanities people with a different  
lens i was challenging the traditional belief that only like technical people   
can work in tech but a lot changed in the past year so I started vibe coding    
maybe a year or two ago i first tried a lot of the web- based tools but at that 
time the models weren't good enough so I couldn't complete projects it was      
mostly like demos or little tools for myself i couldn't really build for other  
people but I think January this year was a turning point so in January I        
started using cloud code and other coding agents and I was able to ship         
products end to end to users other than myself i've somehow got accumulated     
like almost more than 30,000 stars on GitHub with more than five projects with  
over a thousand stars which like beyond my belief because you as you can see in 
this chart like before this January I've never even used GitHub i wasn't even   
sure like how GitHub worked but since January I think January was a watershed   
moment for AI coding it really a lot of the nontechnical people could really    
get their hands on coding and start building uh real projects i'll go through a 
few of the projects I build the first one is front- end slides so the deck      
you're seeing right now is built from this skill so this is a skill that allows 
you to build presentations using HTML so leveraging the coding agents front     
end capabilities so replacing the traditional PowerPoints this was inspired by  
the fact that I think the coding agents are very very good at front-end design  
so I I was thinking how can we apply it to an area that also has to do with     
design but it's not traditionally touched by code so I realized that HTML is a  
great canvas for the model to express itself what you're seeing right now is    
like just a bunch of the templates I've built for the HTML slides and you they  
they look really beautiful i don't think they look like the traditional slides  
i actually give them a lot of references from like artworks and very unique     
color combinations so I wanted to create more different looks from the          
traditional slides this is my most popular skill so far so it has more than     
21,000 stars on GitHub i actually didn't expect it to take off but I think      
slides is such a universal thing that a lot of people need with this skill you  
can make them really really quickly without having to you know do any of the    
pixel pushing yourself so this is the from the user experience how it works so  
first the agent like cloud code will actually start with ask you a few          
questions like what is the purpose and use case for your deck roughly how long  
do you want it to be do you have the content ready or should I help you write   
them and then it will ask you like is it speakerled or more for reading like so 
because it determines the density of the slides and then it will actually       
build you three different style previews for for you to choose from so it will  
build three different designs for the covers so this is to let the user have    
more say in how the design is made and then it will go and build the full slide 
and then after that you have the option to edit it or you can publish it to a   
URL like the the deck I have right now is like deployed to Versell and then I   
had it point to my own domain so it become becomes kind of a website that you   
can easily share with people and what's nice is you can also track it because   
it's a website so you can actually know how many people have opened it etc so   
and then I realized HTML is actually a really great medium for slides because   
first of all AI models kind of speak HTML as a native language because it's all 
over their training data like a lot most of the models are trained on tons of   
web pages so they are very very good at arranging text and images on screen and 
then also websites and slides have a lot in common they're basically just text  
and images arranged in like re rectangular boxes and sections and also if you   
make it in HTML it becomes interactive and sharable so for example for this     
slide I have there are a lot of cool interactions like as you can see my cursor 
is turned into a laser uh pointer and then on the bottom you have these like    
navigation dots that allow you to easily jump to different slides and also      
hover to see the title and then you have interactions like uh you can these     
animation effects or you can click to enlarge any of the media so these are all 
the cool things you could do on the web i wanted to talk a little bit about     
aesthetics because I think that is the key to this skill i spent a lot of time  
on figuring out how to make the slides look stunning or like at least not AI    
slop and the solution I came up with was templates but not the traditional      
templates so if you think about traditional PowerPoint templates they're just   
PowerPoint files that you fill content in at first I tried making the templates 
like HTML files but then I realized the model would overfit the template so it  
would just take whatever arrangement or layout the template had and then try    
to squeeze the content in that layout which compromised the content quality so  
then I heard I read this awesome concept called design md so there there's a    
great concept called design.mmd which is basically a markdown file that         
describes the design of a kind of a set of design tokens for a web page so      
things like the color combination the the fonts the vibe and overall uh design  
guidelines etc so it's just a markdown file and so I realized actually the      
model can do a better job with just uh this markdown file rather than the HTML  
file so that's uh what I ended up using so basically if you look at the the     
templates every folder is just a markdown file um and then just from this       
markdown file the model can do a pretty good job replicating the design system  
how to prevent AI slop in design so I think the first thing is to use cloud     
code because cloud is a lot better than codeex or other models when it comes to 
front-end design so I in my day-to-day I use clot both cloud code and codeex a  
lot but if it's anything that has to do with design I always choose cloth       
because it's just a lot better and also give a lot of opinionated references so 
these are some of the examples of the kind of images I would collect um on      
like Pinterest or other places um I would just save them in the folder and then 
let Claude reference them when making designs codify design guidelines as       
design like I just showed um and also I think we need to know what AI slop is   
before we can prevent it so I think last year AI slop looked like this so you   
have a lot of like purple gradients but this year AI slop is a lot looking like 
this so it's like this look is very clawed so it's just like instrumental       
serif like itallic so I think the goalpost for as always constantly moving      
forward uh because once everyone starts using the same tools like claw design   
like you just see a lot of designs that look very similar to each other and     
then people get tired of it so um I think we just need to know what like what   
this commonly designed slob looks like and then just ban them and I I like to   
make playgrounds so what what I mean by playgrounds is basically an HTML file   
where you can see a lot of different options for for different things so for    
example this is a playground for fonts for this deck so basically just have     
Claude make a bunch of different options for you to compare um and then this is 
a playground for colors so you could just click through the different           
combinations and get a feel for which one you like and this is a playground for 
animations so you can view all the types of cool stuff it can do on the         
basically let it show all the tricks it can do so then you can kind of pick and 
choose what you want to use kind of like a menu so I think if you're not sure   
what you want uh just have claw mix make a playground with lots of different    
options and then choose from there and also I realized SVG could be pretty      
useful so this this was a website I made it's like a list of my favorite        
restaurants and shops in Tokyo cuz I visit a lot the way I made it was actually 
uh there's a thing called Google Takeout where you can actually take out all    
of your personal data from Google products so you could actually export all     
your saved locations in Google Maps um as like a Excel spreadsheet and I give   
that spreadsheet to Clock Hole to turn into a website uh but what I really love 
about it is these cool illustrations like this cat and like uh these uh like    
this little illustrations for the different types of restaurants and stuff so   
these were generated as SVGs using a product called Quiver AI um so Quiver      
specializes in like AI generated SVGs but I really like how intricate it is and 
how it kind of seamlessly blends into the overall vibes of the design so I      
think SVGs is a very underrated um form factor that we can blend into you know  
HTML designs and then for this deck itself uh the way I made it was first I I   
just had a folder of the various images and videos cuz I I did have a lot of    
media I wanted to embed so I just put them in a folder and then I give it like  
very specific instruction on what I want to include in each slide so this was   
like the the first prompt I gave it and then of course it took a lot of rounds  
of different iterations but I did have a very specific idea of what I want um   
in each slide and then I I tell Claude how to use the different media assets    
love the playground idea would love to learn more about that yeah so for        
playground is actually super simple literally I just tell Claude like I want to 
explore different fonts make me a playground that show me the different         
options um and it will do that with like actual content that you're designing   
so the next category of software I made was super uh interesting it's like      
modifying your own software interfaces to fit your own goals so what I mean by  
that is this is especially good for the web so you can make Chrome extensions   
for yourself that modify websites or apps that you frequently use to make them  
better for you so for example I built a little Chrome extension called Tab Out  
so the problem I struggle with as you can see now I have a lot of tabs in my    
browser and I never close them like the only time I close my tabs is when my    
computer crashes and they are forced closed i struggle with like finding the    
right tab when I need it and then it's just like too much to deal with so I     
want I just brainstorm with Claude like how what can we build to do this and it 
it turns out that you can actually customize your new tab tab so this is the    
new the new tab tab so when you open a new tab this landing page you can        
actually v code this landing page um so I turn this landing page into kind of a 
mission control for all your open tabs so you can see them at a glance and      
then you can also um close close any tabs at one click so for example I can see 
what are duplicate tabs and then just like close them with one tab and then     
there's also a very satisfying like swish and sound and confetti when I close   
them and then if I can close a lot of different tabs at one go for for example  
if I want to close all my Gmail I can just click that and then close all my     
homepages so it it becomes almost like a game it's very addictive um I wanted   
to make closing tabs addictive because I think the way most browsers are        
designed they only encourage you to open more tabs they never encourage you to  
close them so I was like I want to modify the the interface so that encourages  
different behavior it groups them by domains which makes it easy to see what    
you have um so this extension is open source yeah you can change the sound you  
can change whatever you like like this is the cool thing about open source is a 
lot of people have actually modified it to fit their own habits so for example  
this user just uh sent me this video the other day like they actually change    
it to like a to-do management system so you could have your tasks uh you could  
have like your your schedule like your to like reading list whatever you want   
on this page so I think the new tab tab is a very underutilized real estate on  
our computers because we just open it so frequently throughout a day but        
usually it's just like a Google search bar or some random stuff so I encourage  
everyone to make the full use of the new tab page and just customize it however 
you like like some people change it to dark mode some people add their          
frequently visited web pages so because it's open source anyone can just like   
do whatever they want with it so for most of my open source project I actually  
want people to not just use it but like remix it um and so yeah this is the     
code on GitHub so you can just uh download it and or get cloud code to install  
it for you um and the other interesting thing which I'm still building it's not 
finished is like a tool that helps me learn from long YouTube videos so right   
so they so for example I have this like super long podcast that I want to watch 
but I may not have t time to consume the full length or the the content might   
be too dense for me it's like a lot of technical stuff so I could open this     
side panel which first first it grabs the full transcript of the podcast so I   
can quickly read the text is also fully work audio and I can click right or     
trust part to like jump to that um part of the video uh if there's anything I   
don't understand I can just select it and then uh and then the AI will actually 
exp so this is very useful for like any sort of technical uh videos or podcast  
for education um and then if you're not sure if you if this is worth your time  
you uh there's an overview tab where you know you get um highlight of the       
highle overview of what the video is about and worth watching if you are you    
know one of these things and then um it also divides it into chapters and then  
you can click on any chapter data efficient right to that part of the video um  
it will also pull the top quotes from the video um using LM and then you can    
click any part to download or copy it with one click i also like this remixing  
idea cuz sometimes I prefer to read it um but I don't want to read a bland      
summary cuz the summaries are usually really bad like they don't capture the    
best parts of the video they're too brief and too generic i like a few um form  
factors for the remix the first one is a magazine article so the prompt is      
basically like transform the transcript into like a New Yorker style magazine   
that is like a long substantial read but also a lot more uh easy to consume     
than like maybe a long video so this is an example of like a magazine article   
remixed from this specific video and this is very suitable for things like a    
long video podcast like Lex Freeman type of podcast you can also do like a      
business biography if it's like a person being interviewed or you can do like a 
briefing whatever format you like notes is also really interesting so as I'm    
watching the video you can see there is a note button here so what I can do is  
even without pausing the video I can click it to take note so let's say I'm     
watching entropic and then he says something I want to take note sun micros     
system and it's just gonna pop up this little panel that just take what he just 
said into you know a note and then uh put it in my notes panel so it's going    
to rewind maybe like a few seconds to capture what I just heard and then put it 
uh turn the transcript into a little note which I can like copy the text or     
time stamp like maybe I can turn into a tweet or you know put into my notebook  
or whatever so this is kind of just like a personal learning tool to make the   
most of uh long YouTube videos how much time does it take to make a new project 
it really depends i think the making part is actually not that hard or          
timeconuming the time consuming part is actually using it and feeling it and    
iterating it based on how you're using it actually and your own behavior        
because for example for tabouts I first made a more sophisticated tool actually 
I I had an LLM categorize all my tabs into like tasks and themes and then I     
realized I just wasn't using that feature i ended up just like want to being    
able to close them so I turned closing tabs into the main feature after just    
feeling it for a while so I think even if building it only took like a day or a 
few hours it maybe took me a week to get a hang of how I'm actually             
interacting with it and how I can shape it more around my actual behavior the   
other category I I I thought was really fun which was I think you can create    
your own personal ad network to shape your own behavior so what I mean by that  
is so advertisers are constantly trying to capture our attention on the         
different platforms but what if we can kind of manipulate our own attention to  
do things we actually want to do i have this habit of hoarding X bookmarks so I 
save a lot of posts on X as bookmarks but I I just rarely open them sometimes   
I just forget about it or I don't have time so I just end up with like hundreds 
of bookmarks so I was like how can I get myself to actually read the bookmarks  
i built a little Chrome extension that modify the X homepage so I think the     
cool thing with browser extensions is they can actually like modify the web     
interface of products you use so here I inserted like a bookmark from my        
bookmarks into like the top of my X homepage so it's almost like an ad so every 
time I open the X homepage the first post I see is like something from my       
bookmark so it's a great reminder to you know okay go read your bookmarks first 
before scrolling the rest of X because the X homepage is something I'm already  
frequently opening it's like a great entry point for me to read the bookmarks   
this is what I mean by like a personal ad network so usually if you use any     
social media like this spot will be occupied by a lot of ads but you can        
actually use a chrome extension to shape it to to you know get the uh the       
behavior you want in yourself um and the same thing with like YouTube watch     
later etc i think another real estate uh very underutilized is the phone        
wallpaper because we just open our phone like hundreds of times per day when I  
was learning Japanese um I tried turning my wallpapers into shuffling Japanese  
vocabulary images so you can build these like wallpapers using uh clock code or 
any agent so the the the images are just HTML so you can just get the agent to  
make a HTML in like the phone dimension and then export as images and then you  
can put them in a album on your phone and on iPhone you can actually set shop   
um your wallpaper to be like a shuffle for a specific album so this is how you  
get this like on key effect on the wallpaper and then every time you tap it it  
shuffles to a different wallpaper so uh this is kind of like how you can this   
like almost like a personal ad system if you want to study something um and     
this is also a cool lesson which is most people think you uh you can only make  
images with image gen models but actually code is very good with designing      
images like this so if especially if it has to do with arranging text on screen 
or text and images actually code and front end is very very good for that so    
if you want to make posters or like these cards or you know decks like code is  
actually a lot better than image generation and the the the next category is    
content remixing now that we have agents we actually have the opportunity to    
remix any sort of content into whatever format you like because we all consume  
content in different ways so for example I tried turning the acquired podcast   
into a physical book um I I like the acquired podcast uh it was it's just super 
super long and I don't have time to like go through all of them so I was like   
if if it's a physical book I would love to read it so um I actually just        
downloaded their transcript from their website and then use Claude uh use a     
super long prompt to turn each uh episode into a chapter of a book u so each    
chapter will be like 20 pages it's still a very long read but I I actually      
really like reading it because the content is so dense and sometimes when I'm   
listening to the podcast I find myself drifting off or like it's just hard to   
focus and whereas when I'm reading it's a lot easier for me to focus so I and I 
actually got it printed as a physical book and I designed the cover and         
everything so this is what it looks like um and then each chapter is like an    
episode of the show um and uh this is the prompt I use it's pretty long but     
basically I get it to uh it it's it's not a generic summary cuz I don't think a 
summary works it's also not very readable so I got Claw to write it as a great  
business biography kind of like you know Shoe Dog The Everything Store that     
kind of uh vibes and also it needs to preserve the best quotes and an anecdotes 
from the original show as much as possible so that you still get the best       
parts um but then it maps it in a story that's very readable and then um also   
if there are a lot of technical or business concepts that may not be            
understandable easily I I also got it to explain it in layman language this     
kind of prompt I build it with Claude so I have an idea of the types of things  
I like and then I just uh bounce ideas um with Claude together so do I spend a  
lot of time on prompt building i think I just spend a lot of time chatting with 
Claude i think the specific words don't matter that much i think when the       
models first came out you sort of had to say like the magic words to get them   
to do certain things but now they're smart enough that um you can just brain    
dump your thoughts i think brain dumping is very important i know a lot of      
people use the voice input to do that i think that's very good so basically     
just like ramble just give it a lot of thought it doesn't even have to be super 
structured but I think just giving it your raw unfiltered thoughts and a lot    
of the context uh would be good and then clock can help you turn it into a very 
structured prompt the other type of remixing is uh turn videos into newsletter  
just like how I showed you I can remix a podcast into like a magazine article   
you can also turn that magazine article into a eub kind of like a ebook and     
then you can have it emailed to your inbox on a regular basis so you could get  
a weekly newsletter of your favorite podcasts and then read them in the ebook   
app almost like a book this is also a super interesting project because I don't 
really know how to code still but I kind of want to understand how the code     
works under the hood i also had an opinion around how we should learn computer  
science uh in this age of AI i think traditionally in school we learned bottoms 
up so you had to go through a lot of the foundational courses first before      
moving up to the more interesting stuff but I feel like now we should just like 
build first we should just turn our ideas into reality with the coding agents   
and then go and ask hey how did you build it how does it work under the hood so 
I made this project called codebase to course because I think the best CS       
course you can take is your own vibecoded project like that's the best learning 
material so uh this is a demo of that so for example I built this tool called   
long cut i just gave the codebase to cloud code and like it's like turn into a  
course so this the course is just like HTML file that's interactive so it first 
breaks down what it does the user journey and then for the if there are         
technical terms you can hover over it to see a layman explanation um a also had 
this really useful side by side of like here's the code and here's the layman   
like English version translation of that it will also give you quizzes to help  
you understand the key concepts and then uh this part is really interesting     
where so first of all you can trace a user journey through like these cool      
animations so you can see for example how data flows in the system and then you 
can also simulate how the components interact with each other as a group chat   
so it's like the different APIs or you know technologies in the codebase        
they're talking to each other just like people talking to group chat so I found 
kind of simulating them this way really helps with understanding so just a lot  
of different tricks to help you break down technical concepts into easy to      
understand components all of this is packaged into a skill that you can use on  
GitHub so basically point it to any GitHub repo or local codebase and it will   
turn into like a HTML based CS course and then also turn Excel spreadsheets     
into interactive dashboard so I think HTML is very good at visualizing data so  
for example here is a excel spreadsheet of my x analytics and then you can just 
uh give it to cloud code or any agent it will turn into like interactive chart  
uh that you can play with which tool I use for which skills i mainly just use   
cloud code and codeex the use cases I pick for them is like if has anything to  
do with design or brainstorming products I always use cloud code uh if it's     
just executing or like everyday day-to-day tasks I use Codeex i think Codeex is 
great for when you already know what you want or you just need to like fix a    
bug it's great at execution it's also a little bit cheaper but if you don't     
know what you want you just want to like brainstorm and chat or you want        
product ideas you want to be inspired you want great design then claw code is   
much better the last part was about the projects I built the next section will  
be about how I built them so first of all how to get product ideas um the way I 
think about product ideas is I think is the intersection of users and           
technology so a product brings user and technology together together so uh when 
you think about product ideas there are two directions you can take it one is   
to start with the user and the other is to start with the technology i think    
both can work really well if you start with the user I think I got a lot of     
ideas uh not just from my own pain points but also from talking to people who   
are very different from you because um I think products are all about meeting a 
lot of people's pain points and you need the pain points that's actually like   
generalizable and has a sizable audience which is why I think uh creating       
content has helped me a lot because when I put content out there I get a lot of 
feedback from people who are very different from me so uh I get to know how     
people think and then I I also meet a lot of people for coffee and and stuff so 
just hearing the pain points from a lot of different people really help uh      
inspire my ideas um the other is uh feel your own point brainstorm with clock   
code and uh this is important like use it for a week and see if you'll still    
use it because I actually killed a lot of product ideas because I thought       
theoretically I would like use this product but then my own behavior just       
showed that I wasn't using it as much so then I I just felt like it didn't work 
so I think a good idea has to be proven empirically that you or someone would   
actually stick with it so here I wanted to give an example of like tab out i    
actually went back to cloud code and was like like hey go through our chat      
history like and then build me a HTML that kind of simulate how this idea came  
about so it didn't start out with like hey build me a Chrome extension that     
does blah blah it actually started with a question the question was like my     
Chrome browsing history is stored locally right can you access it because I     
just saw someone on Twitter build something with their Chrome history and I     
thought "Oh wow the AI can access my browser history." Like it must there must  
be some room there for building cool stuff but I I didn't know exactly what I   
wanted to build yet so I literally just asked Claw like like "You have it       
right?" And then it was like "Yes I have it." I was like "Let's do something    
with it." And then I just told him my problem my problem is I hoard too many    
tabs i never close them some of them are tasks um that I haven't finished like  
what can you do to help i didn't really have a specific idea and then Claw gave 
me a few ideas but then I said like how do you make sure I'll actually use it   
because a lot of ideas sound simple in theory like there's so many to-do lists  
or like task management apps so I just end up like still not doing my to-dos    
cuz all of them require you to be very disciplined to like click certain        
buttons remember to open certain things then Claude said like maybe have you    
considered like making it your new tab page which I thought was a brilliant     
idea because on my own I didn't know the new tab page could be customized and   
like Claude told me that so I was like okay do that and then that's how that    
became the entry point for the product because I at first it it was it wanted   
to build me an extension that's you know where you have to click a button to    
pull out your tabs and I just told it I would never click the button like I     
will never remember to click a button so can you put it somewhere where I don't 
have to click anything like I'm already naturally like opening it frequently    
um and that that's how it came up with the new tab page um and then uh I got it 
to build some mockups and then uh just gave it a lot of specific feedbacks      
most of it is just from my own behavior um and for example can can you add like 
satisfying animation and sound effect i just wanted to make it a lot more fun   
and addictive so this is uh starting with a user the other way is to start with 
a technology so I'm always on X i think I've tuned my al X algorithm such that  
it's like a very high density um information hub for like new technology and    
AI stuff so I get a lot of new models new products new APIs new cool            
technologies like use cases designs so I bookmark them and actually block out   
time to actually try them hands-on so I think it's very important to try        
technology hands-on if you see a cool new product or API just like send it to   
claude and like be like hey how do I how can we build something with it so a    
lot of times it's not like you have a you start with a painoint a lot of times  
you just start with a technology like a cool API for example and then you can   
brainstorm with claw like what can we build with it um I also I actually want   
to advocate for building something small because I think most of the internet   
will teach you to build something big but I actually think in the age of AI     
there's a lot of value in building small uh so first of all every big thing     
starts as a small thing i think in order to capture people's imagination you    
need a very sharp value proposition and positioning to stand out and right now  
I'm hearing so many products that oh like allin-one AI agent that helps you     
with everything in your work and life and integrates with everything and I just 
feel like that's so generic like if that's your positioning I may as well just  
use Claude you know cuz Claude is that so like if you want me to use your       
product you have to offer something differentiated and special that has a       
opinion and soul behind it and I think you you need to start with targeting a   
very specific use case and a very specific target audience and the problem and  
opinion yes doing everything means it's doing nothing and speaking to everybody 
means you're speaking to nobody so that's why I think we should start with      
building something small and I also think we should build for fun and build to  
learn so someone asked how did you monetize these projects so I didn't actually 
build them for monetization these were mostly just like side hustles and hobby  
projects also a great way for me to learn because I think the best way to       
learn product management is just to build products from zero and this wasn't    
available as an option if you were trying to become a PM say like three years   
ago because back then you had to rely on engineers to build out your ideas but  
now you can literally go with from idea conception to building it to            
distributing it all on your own so I'm kind of my own product manager my own    
designer my own engineer my own marketer all in one so I think that's just a    
great learning experience it's also really fun like almost like you can build a 
community of people who who are using your products and think alike and I also  
think opinionated products survive so like I said if you're just building a     
generic unopinionated AI tool like people may as well just use like their       
general like codeex clock or whatever so the I think the reason people will use 
your tool is because the opinion behind the product resonates with them so      
here is the opinion behind my products for front end slides is like I don't     
like PowerPoint use HTML to replace PowerPoint like HTML is the next medium for 
storytelling and then for codebase to course uh the the tool that turns a       
codebase into like HTML based course opinion behind it is like in the past in   
traditional education we learn to build whereas now I think it should be        
reverse which is build to learn like we should build first and learn later um   
and for tab out is like we should make closing tabs addictive and then kind of  
change the default behavior around browsers and I think the reason a lot of the 
products resonated with people is because the ideas and opinions behind the     
products resonated with people so sometimes I almost think of my GitHub as like 
a substack so because uh in the past when you had an opinion you wrote an       
article or you make a video or something now when you have an opinion you can   
put it into into a skill or a product because I think every product actually is 
a expression of how you think and the your unique way of perceiving the world   
if you want to uh get started with building similar projects here are some      
practical tips to get started but first of all is I think uh especially for     
beginners like using the best model can really save you a lot of time and even  
even save you money because I think Boris who's the founder of clock code once  
said uh if you use the best and most expensive model it can sometimes turn out  
to be cheaper because if you use a cheaper model sometimes it will just get     
stuck at solving certain problems or it just it just doesn't work and then you  
end up spending more time in token to get it to work so I usually just use the  
best model by default uh but unless you have like wrote repetitive work in that 
case you can use a cheaper one and the way I talk talk to the model is I I      
don't treat it as my employee or assistant i actually treat the model uh as my  
co-founder so I do a lot of brainstorming with it i describe problems not       
solutions so for example for tab out I just said like all my browser history is 
here what can we do with it um without a specific idea in mind and Claw was     
the one who came up with the specific idea so I think uh we don't have to have  
a very uh complete spec when we talk to Claw we can just describe the mess      
we're in and see what we can do with it um and then the third one is build      
around your actual behavior and not what you think you do because human         
behavior is very messy humans are lazy we're forgetful we're like uh            
unpredictable so uh if sometime for a lot of the products I think there's a lot 
of wishful thinking it's like they expect people to like remember to open a     
website and click on a button and do one two three like most people would just  
never do that or like they'll just forget so I like to build products around    
that which is why I think after I build something it takes me like a week to    
feel it to see okay am I still using this or did I forget or you know did it    
did it actually is it actually shaped around my actual behavior and then tweak  
it from there um and then the next one is cut more than you add so I think the  
models are very good at adding stuff and then what because adding things is so  
easy and the cost is so low these days we tend to become very greedy like more  
and more and more uh whereas I think now the human's role is actually subtract  
sub subtraction more than addition so we actually need to be very disciplined   
and always get the model to cut stuff uh so for example for tab out I first uh  
built in a um AI organization feature that categorize the tabs um but then I    
realized just I just didn't end up finding it that useful it also consume a lot 
of tokens so in the end it was like just let as let's just get rid of that      
like I'll just categorize them by domain so this tool ended up having like no   
AI but it also ended up being better cuz it was shaped around what I actually   
needed so I think before I ship anything I always take the time to cut a lot of 
things um and then uh I think putting the wraps is really important so like     
anything in life the more you do it the better you get so um I think I got a    
feel for it maybe after like my eighth project or so so I just built a lot and  
then some of them fail some of them more successful but I think just building a 
lot um is uh putting the reps actually really helps and then building a public  
is really useful so uh when I posted tab out on Twitter it got almost half a    
million views and then this um uh visitor like why does it need to run a        
noode.js server so at that point it had a server and I actually didn't know why 
I needed a server so I just asked cloud code like why do we need this and then  
cloud was like oh we we don't actually need it so I just deleted it in the end  
well I I wouldn't have known if like uh he had not commented on my post to      
tell me that cuz so I think uh bu showing your product in public uh just and    
then having people giving you feedback and comment especially from like         
engineers is really helpful because um then you can actually learn from the     
internet and then uh get better at what you build um and then the last one is   
just make it fun so I think it's important to be not so utilitarian um like you 
don't have to like make a ton of money from it or you know get like 100         
million users uh even if it's just for you and your friends uh it can be really 
useful and um educational uh so I really like this quote by Peter Steinberger   
who is the creator of Open Claw he said "It's hard to compete with somebody     
who's just there to have fun." And I think Open Claw was born out of you know   
like a fun side hustle it wasn't he didn't set out to build like a billion      
dollar business so I think a lot of good ideas can come out of these like       
non-utilitarian pursuits and then if we just try to have fun with the models    
try to push uh them to their limits and see what they can do we end up with a   
lot of good product ideas um and then uh because a lot of people are trying to  
make skills I wanted to talk a little bit about skills specifically so for      
example for front end slice the way I make it is uh first you just have an idea 
and then just try to get claw to do it so for example like I want to make a     
slide HTML like just give it the content and do it without a lot of specific    
instructions and then it will inevitably make slop so the first iteration is    
probably really really bad so you just give it a lot of feedback um like oh     
don't use purple gradients don't do this don't do that and then this iteration  
will probably take like 10 or 20 or dozens of turns um but this is very         
important like you actually need to spend a lot of time on this at this stage   
but then the next part is really important it's like tell the AI turn           
everything we just did and then package it into a skill so kind of the          
workflows and iterations you went into that is the actual skill so um the way   
you make the skill is not by starting with making a skill is but by ending uh   
with a skill so you do the thing first and then you say hey turn whatever we    
just did into a skill and because you give it so much specific feedback it's    
able to incorporate your specific taste and criteria into the skill um and then 
uh at the for the last step you can kind of package it into a more user         
friendly version and then just publish it on GitHub to share with others um so  
uh to close out I think uh I feel like coding is evolving from a profession     
into a skill so what I mean by that is um it's kind of like writing so          
traditionally we think of writing more as a skill so there are professional     
writers uh like journalists and uh book writers but mo we mostly think of       
writing as a skill so no matter what you do you can benefit from being a good   
writer i think coding is the same so uh before AI coding we mostly thought of   
coding as a profession so only the engineers did it for a living but now that   
um AI coding has made it accessible to everyone I think it's evolving into a    
skill where anyone can just talk to the models and um you know turn the ideas   
into reality so and no matter what you do if you're a business owner you're a   
marketer you're a product manager designer I think uh knowing how to work with  
the coding models will help you level up in whatever you do um and so I I think 
we need to differentiate engineering from coding so engineering is a very       
serious like discipline it's a career it requires a lot of training but coding  
is just a tool it's just just like writing like a skill like if you have an     
idea you can uh you know turn it into reality and um most people never need to  
build stuff in production like because you you you're not necessarily engineer  
working on like a production level product but you can still build something    
that improves your own lives that you use with yourself your family or your     
friends so I kind of think of it as like we we should stop thinking about       
coding as something that's like super serious and like different distant from   
my life um so I think co vibe coding is a form of self-expression so actually   
for most of my career I was a storyteller so I started as a journalist i worked 
as a marketer so I I did a lot of writing so um but I think when I started v    
coding I realized um I didn't pivot from storyteller to coder i just discovered 
a new medium for storytelling and that medium is code so uh which goes back to  
my title which is code is a medium for storytelling so I I kind of encourage    
everyone to tell your own story through code because previously you probably    
told it through you know uh writing or videos or content but now if you have an 
opinion idea or specific taste you can turn into a product a skill and then     
share on GitHub with others um so I that's all I wanted to talk about so you    
can take this stack with you by going to this URL or scanning the code and all  
of the projects I mentioned are on my GitHub you can see here yeah thank you    

  Searched for 4 patterns, read 3 files (ctrl+o to expand)

● Bash(./scripts/allocate-address.sh --peek)
  ⎿  78

  Read 2 files (ctrl+o to expand)

● Write(.raw\articles\code-as-a-medium-for-storytelling-2026-07-02.md)
  ⎿  Wrote 8 lines to
     .raw\articles\code-as-a-medium-for-storytelling-2026-07-02.md
      2 source_type: transcript
      4 title: Code as a Medium for Storytelling
      5 date: 2026-07-02
      7 ---
      8 the theme of my presentation is code as a medium for storytelling
        nk of coding from a different lens from most professional enginee
        go through uh my own background how I started VIP coding and the 
        projects I've built and how I built them and then why it matters 
         a coder i studied humanities in school i never took CS actually 
        in 2023 I wrote a blog post called why I'm not learning to c
     … +631 lines (ctrl+o to expand)

  Read 3 files (ctrl+o to expand)

● Bash(for i in {1..9}; do ./scripts/allocate-address.sh; done)
  ⎿  c-000078
     c-000079
     c-000080
     … +6 lines (ctrl+o to expand)

  Read 1 file (ctrl+o to expand)

● Write(wiki\sources\Code as a Medium for Storytelling.md)
  ⎿  Wrote 57 lines to wiki\sources\Code as a Medium for Storytelling.md
       1 ---
       2 type: source
       3 title: "Code as a Medium for Storytelling"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - source
       8   - transcript
       9   - vibe-coding
      10   - storytelling
     … +93 lines (ctrl+o to expand)

● API Error: Request rejected (429) · [anthropic-compatible-6f275f22-ec2
  2-4769-a4cf-f3b9d8b4e3f3/google/gemini-3.5-flash] [429]: 
  {"error":{"message":"UID rate limit reached for TPD (oversea) for UID 
  (request_id: chatcmpl-cda4b4ea53df4689a18a9f2c58f35ab3)","type":"rate_
  limit_exceeded_error"}} (reset after 1m 4s)

✻ Sautéed for 4m 8s

❯ /model                                                                        
  ⎿  Set model to qnaigc/deepseek/deepseek-v4-pro and saved as your default for
     new sessions

❯ continue                                                                      

  Thought for 16s (ctrl+o to expand)

● I'll continue the ingest. I've created the source page and allocated
  addresses. Now I need to create the entity page for ljg-learn and 7 concept
  pages from the transcript.

● Write(wiki\entities\ljg-learn.md)
  ⎿  Wrote 51 lines to wiki\entities\ljg-learn.md
       1 ---
       2 type: entity
       3 title: "ljg-learn"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - entity
       8   - person
       9   - vibe-coding
      10   - open-source
     … +56 lines (ctrl+o to expand)

  Thought for 7s (ctrl+o to expand)

● Now creating the 7 concept pages in parallel:

● Write(wiki\concepts\Vibe Coding.md)
  ⎿  Wrote 53 lines to wiki\concepts\Vibe Coding.md
       1 ---
       2 type: concept
       3 title: "Vibe Coding"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - concept
       8   - vibe-coding
       9   - ai-coding
      10   - no-code
     … +61 lines (ctrl+o to expand)

● Write(wiki\concepts\Design MD.md)
  ⎿  Wrote 50 lines to wiki\concepts\Design MD.md
       1 ---
       2 type: concept
       3 title: "Design MD"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - concept
       8   - design
       9   - ai-coding
      10   - frontend
     … +59 lines (ctrl+o to expand)

  Thought for 13s (ctrl+o to expand)

● Write(wiki\concepts\Playgrounds (LLM Design).md)
  ⎿  Wrote 51 lines to wiki\concepts\Playgrounds (LLM Design).md
       1 ---
       2 type: concept
       3 title: "Playgrounds (LLM Design)"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - concept
       8   - design
       9   - ai-coding
      10   - frontend
     … +58 lines (ctrl+o to expand)

● Write(wiki\concepts\Personal Ad Network.md)
  ⎿  Wrote 55 lines to wiki\concepts\Personal Ad Network.md
       1 ---
       2 type: concept
       3 title: "Personal Ad Network"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - concept
       8   - habit-formation
       9   - chrome-extension
      10   - attention
     … +66 lines (ctrl+o to expand)

  Thought for 4s (ctrl+o to expand)

● Write(wiki\concepts\Content Remixing.md)
  ⎿  Wrote 56 lines to wiki\concepts\Content Remixing.md
       1 ---
       2 type: concept
       3 title: "Content Remixing"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - concept
       8   - content
       9   - ai
      10   - transformation
     … +64 lines (ctrl+o to expand)

  Thought for 18s (ctrl+o to expand)
● Write(wiki\concepts\Build to Learn.md)
  ⎿  Wrote 53 lines to wiki\concepts\Build to Learn.md
       1 ---
       2 type: concept
       3 title: "Build to Learn"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - concept
       8   - learning
       9   - ai-coding
      10   - education
     … +60 lines (ctrl+o to expand)

  Thought for 5s (ctrl+o to expand)

● Write(wiki\concepts\Opinionated Products.md)
  ⎿  Wrote 51 lines to wiki\concepts\Opinionated Products.md
       1 ---
       2 type: concept
       3 title: "Opinionated Products"
       4 created: 2026-07-02
       5 updated: 2026-07-02
       6 tags:
       7   - concept
       8   - product-management
       9   - ai-coding
      10   - positioning
     … +59 lines (ctrl+o to expand)

  Thought for 6s (ctrl+o to expand)

● Now updating the index files, log, hot cache, and manifest. Let me read the
  current index.md and .manifest.json:

  Thought for 26s, read 2 files (ctrl+o to expand)

● Now updating all the index files, log, hot cache, and manifest:

● Update(wiki\index.md)
  ⎿  Added 1 line, removed 1 line
      23  
      24  # Wiki Index
      25  
      26 -Last updated: 2026-06-09 | Total pages: 109 | Sources ingested:
         - 8                                                             
      26 +Last updated: 2026-07-02 | Total pages: 118 | Sources ingested:
         + 9                                                             
      27  
      28  Navigation: [[overview]] | [[log]] | [[hot]] | [[dashboard]] | 
          [[Wiki Map]] | [[getting-started]]
      29  

  Thought for 8s (ctrl+o to expand)

● Now I need to add the new entries throughout the index. Let me add the
  concepts, entity, and source:

● Update(wiki\index.md)
  ⎿  Added 7 lines
       98  - [[Orchestrator-Workers]] — dynamic task breakdown and delega
           tion by a central LLM (status: developing)
       99  - [[Evaluator-Optimizer]] — generation-evaluation feedback loo
           p (status: developing)
      100  - [[Agent-Computer Interface (ACI)]] — tool design principles 
           for LLM agents (status: developing)
      101 +- [[Vibe Coding]] — building software via natural language wit
          +h AI coding agents; coding evolving from profession to general
          + skill (status: developing)                                   
      102 +- [[Design MD]] — declarative markdown design tokens for guidi
          +ng LLM front-end generation; prevents template overfit (status
          +: developing)                                                 
      103 +- [[Playgrounds (LLM Design)]] — interactive HTML comparison p
          +ages for exploring fonts, colors, and animations with AI (stat
          +us: developing)                                               
      104 +- [[Personal Ad Network]] — repurposing high-frequency digital
          + touchpoints to shape personal habits instead of serving ads (
          +status: developing)                                           
      105 +- [[Content Remixing]] — transforming source content into mult
          +iple formats optimized for different consumption preferences (
          +status: developing)                                           
      106 +- [[Build to Learn]] — reversing CS education: build first wit
          +h AI agents, then understand how the code works (status: devel
          +oping)                                                        
      107 +- [[Opinionated Products]] — software succeeds through sharp, 
          +specific opinions that resonate, not by doing everything for e
          +veryone (status: developing)                                  
      108  
      109  ---
      110  

● Update(wiki\index.md)
  ⎿  Added 1 line
      120  - [[Claude SEO]] — Tier 4 Claude Code skill for SEO analysis; 
           23 skills, 17 agents, 30 scripts at v1.9.0 (status: evergreen)
      121  - [[汤质看本质]] — B站知识创作者，看本质及高手的黑箱系列作者（
           status: developing）
      122  - [[Anthropic]] — AI safety and research company, creator of C
           laude; published the Building Effective Agents guide（status: 
           developing）
      123 +- [[ljg-learn]] — humanities-to-code creator; 30,000+ GitHub s
          +tars across open-source vibe-coded projects（status: developin
          +g）                                                           
      124  
      125  ---
      126  

  Thought for 11s (ctrl+o to expand)

● Update(wiki\index.md)
  ⎿  Added 1 line
      134  - [[高手的黑箱6-评价]] — 2026-05-22 | 汤质高手的黑箱第六期：评
           价、品味、写作修改与AI辅助创作（68页）（status: current）
      135  - [[高手的黑箱7-创作]] — 2026-05-22 | 汤质高手的黑箱第七期：创
           作、人机共创工作流与个人创作者商业模式（130页）（status: curre
           nt）
      136  - [[Building Effective Agents]] — 2026-06-09 | Anthropic engin
           eering blog: six patterns for LLM agentic systems（status: cur
           rent）
      137 +- [[Code as a Medium for Storytelling]] — 2026-07-02 | ljg-lea
          +rn presentation transcript: coding as storytelling medium, vib
          +e coding projects, design MD, opinionated products（status: cu
          +rrent）                                                       
      138  
      139  ---
      140  

  Thought for 4s (ctrl+o to expand)

● Now updating the sub-indexes, log, and manifest:

● Update(wiki\concepts\_index.md)
  ⎿  Added 10 lines
      107  - [[Evaluator-Optimizer]] — generation-evaluation feedback loo
           p (developing)
      108  - [[Agent-Computer Interface (ACI)]] — tool design principles 
           for LLM agents (developing)
      109  
      110 +## Vibe Coding and Product Design                             
      111 +                                                              
      112 +- [[Vibe Coding]] — building software via natural language wit
          +h AI coding agents (developing)                               
      113 +- [[Design MD]] — declarative markdown design tokens for guidi
          +ng LLM front-end generation (developing)                      
      114 +- [[Playgrounds (LLM Design)]] — interactive HTML comparison p
          +ages for design exploration (developing)                      
      115 +- [[Personal Ad Network]] — repurposing digital touchpoints to
          + shape personal habits (developing)                           
      116 +- [[Content Remixing]] — transforming content into formats opt
          +imized for consumption preferences (developing)               
      117 +- [[Build to Learn]] — reversing CS education: build first wit
          +h AI, then learn how it works (developing)                    
      118 +- [[Opinionated Products]] — software succeeds through sharp, 
          +specific opinions, not generic functionality (developing)     
      119 +                                                              
      120  ---
      121  
      122  ## Add new concepts here as they are extracted from sources.

● Update(wiki\entities\_index.md)
  ⎿  Added 1 line
      25  ## People
      26  
      27  - [[Andrej Karpathy]] — AI researcher, educator; originated the
           LLM Wiki pattern
      28 +- [[ljg-learn]] — humanities-to-code creator; 30,000+ GitHub st
         +ars across open-source vibe-coded projects                     
      29  - [[汤质看本质]] — 知识类创作者，《看本质》和《高手的黑箱》系列
          作者
      30  
      31  ---

  Thought for 3s (ctrl+o to expand)

● Update(wiki\entities\_index.md)
  ⎿  Added 1 line, removed 1 line
      1  ---
      2  type: meta
      3  title: "Entities Index"
      4 -updated: 2026-05-21                                             
      4 +updated: 2026-07-02                                             
      5  tags:
      6    - meta
      7    - index

● Update(wiki\concepts\_index.md)
  ⎿  Added 1 line, removed 1 line
      1  ---
      2  type: meta
      3  title: "Concepts Index"
      4 -updated: 2026-06-09                                             
      4 +updated: 2026-07-02                                             
      5  tags:
      6    - meta
      7    - index

  Thought for 9s (ctrl+o to expand)

● Update(wiki\sources\_index.md)
  ⎿  Added 1 line, removed 1 line
      1  ---
      2  type: meta
      3  title: "Sources Index"
      4 -updated: 2026-05-22                                             
      4 +updated: 2026-07-02                                             
      5  tags:
      6    - meta
      7    - index

  Thought for 3s (ctrl+o to expand)

● Update(wiki\sources\_index.md)
  ⎿  Added 1 line
      37  
      38  - [[claude-obsidian-ecosystem-research]] — Claude + Obsidian ec
          osystem research across 16+ repos
      39  - [[Building Effective Agents]] — Anthropic engineering blog (J
          an 2025): six patterns for LLM agentic systems
      40 +- [[Code as a Medium for Storytelling]] — ljg-learn presentatio
         +n transcript (Jul 2026): coding as storytelling medium, vibe co
         +ding, design MD, opinionated products                          
      41  
      42  ---
      43  

  Thought for 12s (ctrl+o to expand)
● Update(wiki\log.md)
  ⎿  Added 7 lines
      25  
      26  ---
      27  
      28 +## [2026-07-02] ingest | Code as a Medium for Storytelling     
      29 +- Source: `.raw/articles/code-as-a-medium-for-storytelling-2026
         +-07-02.md`                                                     
      30 +- Summary: [[Code as a Medium for Storytelling]]               
      31 +- Pages created: [[ljg-learn]], [[Vibe Coding]], [[Design MD]],
         + [[Playgrounds (LLM Design)]], [[Personal Ad Network]], [[Conte
         +nt Remixing]], [[Build to Learn]], [[Opinionated Products]]    
      32 +- Pages updated: [[index]], [[log]], [[hot]], [[concepts/_index
         +]], [[entities/_index]], [[sources/_index]]                    
      33 +- Key insight: Coding is evolving from a profession to a genera
         +l skill (like writing); products survive through sharp, specifi
         +c opinions rather than generic all-in-one AI functionality. The
         + talk bridges humanities storytelling with vibe-coded product d
         +evelopment, introducing concepts like Design MD tokens, playgro
         +und-based design exploration, and personal ad networks for habi
         +t shaping. Complements the existing [[智能体工作流]] and [[Augm
         +ented LLM]] agent patterns with a product-design and self-expre
         +ssion lens.                                                    
      34 +                                                               
      35  ## [2026-06-09] ingest | Building Effective Agents
      36  - Source: `.raw/articles/building-effective-agents-2025-01-06.m
          d`
      37  - Summary: [[Building Effective Agents]]

● Now update the manifest:

● Update(.raw\.manifest.json)
  ⎿  Error editing file

  Thought for 5s (ctrl+o to expand)

● Update(.raw\.manifest.json)
  ⎿  Added 24 lines
      164          "wiki/sources/_index.md",
      165          "wiki/entities/汤质看本质.md"
      166        ]
      167 +    },                                                        
      168 +                                                              
      169 +    ".raw/articles/code-as-a-medium-for-storytelling-2026-07-0
          +2.md": {                                                      
      170 +      "hash": "manual-ingest",                                
      171 +      "ingested_at": "2026-07-02",                            
      172 +      "pages_created": [                                      
      173 +        "wiki/sources/Code as a Medium for Storytelling.md",  
      174 +        "wiki/entities/ljg-learn.md",                         
      175 +        "wiki/concepts/Vibe Coding.md",                       
      176 +        "wiki/concepts/Design MD.md",                         
      177 +        "wiki/concepts/Playgrounds (LLM Design).md",          
      178 +        "wiki/concepts/Personal Ad Network.md",               
      179 +        "wiki/concepts/Content Remixing.md",                  
      180 +        "wiki/concepts/Build to Learn.md",                    
      181 +        "wiki/concepts/Opinionated Products.md"               
      182 +      ],                                                      
      183 +      "pages_updated": [                                      
      184 +        "wiki/index.md",                                      
      185 +        "wiki/hot.md",                                        
      186 +        "wiki/log.md",                                        
      187 +        "wiki/concepts/_index.md",                            
      188 +        "wiki/entities/_index.md",                            
      189 +        "wiki/sources/_index.md"                              
      190 +      ]                                                       
      191      }
      192    },
      193    "address_map": {

  Thought for 11s (ctrl+o to expand)

● Update(.raw\.manifest.json)
  ⎿  Added 10 lines, removed 1 line
      254      "wiki/concepts/Orchestrator-Workers.md": "c-000074",
      255      "wiki/concepts/Evaluator-Optimizer.md": "c-000075",
      256      "wiki/sources/Building Effective Agents.md": "c-000076",
      257 -    "wiki/concepts/Agent-Computer Interface (ACI).md": "c-0000
          -77"                                                           
      257 +    "wiki/concepts/Agent-Computer Interface (ACI).md": "c-0000
          +77",                                                          
      258 +    "wiki/sources/Code as a Medium for Storytelling.md": "c-00
          +0078",                                                        
      259 +    "wiki/entities/ljg-learn.md": "c-000079",                 
      260 +    "wiki/concepts/Vibe Coding.md": "c-000080",               
      261 +    "wiki/concepts/Design MD.md": "c-000081",                 
      262 +    "wiki/concepts/Playgrounds (LLM Design).md": "c-000082",  
      263 +    "wiki/concepts/Personal Ad Network.md": "c-000083",       
      264 +    "wiki/concepts/Content Remixing.md": "c-000084",          
      265 +    "wiki/concepts/Build to Learn.md": "c-000085",            
      266 +    "wiki/concepts/Opinionated Products.md": "c-000086"       
      267    }
      268  }

  Thought for 3s (ctrl+o to expand)

● Now update hot cache:

● Write(wiki\hot.md)
  ⎿  Added 13 lines, removed 63 lines
      1  ---
      2  type: meta
      3  title: "Hot Cache"
      4 -updated: 2026-05-22T02:00:00                                    
      4 +updated: 2026-07-02T02:00:00                                    
      5  tags:
      6    - meta
      7    - hot-cache
     ...
      20  
      21  ## Last Updated
      22  
      23 -2026-06-09: Ingested Anthropic engineering blog "Building Effec
         -tive Agents" (Jan 2025). Created 1 source page ([[Building Effe
         -ctive Agents]]), 1 entity page ([[Anthropic]]), and 7 concept p
         -ages ([[Augmented LLM]], [[Prompt Chaining]], [[Routing (LLM Ag
         -ent)]], [[Parallelization (LLM)]], [[Orchestrator-Workers]], [[
         -Evaluator-Optimizer]], [[Agent-Computer Interface (ACI)]]). Cor
         -e frame: six composable patterns from simple augmented LLMs to 
         -autonomous agents; simple, transparent, well-tested tools (ACI)
         - matter more than frameworks. Anthropic's engineering taxonomy 
         -complements the creative/role-based [[智能体工作流]] concept. A
         -pplied DragonScale addresses c-000069 through c-000077.        
      23 +2026-07-02: Ingested ljg-learn presentation transcript "Code as
         + a Medium for Storytelling." Created 1 source page ([[Code as a
         + Medium for Storytelling]]), 1 entity page ([[ljg-learn]]), and
         + 7 concept pages ([[Vibe Coding]], [[Design MD]], [[Playgrounds
         + (LLM Design)]], [[Personal Ad Network]], [[Content Remixing]],
         + [[Build to Learn]], [[Opinionated Products]]). Core frame: cod
         +ing is evolving from a profession to a general skill (like writ
         +ing); products survive through sharp, specific opinions; LLMs a
         +re guided better by declarative design tokens (Design MD) than 
         +rigid HTML templates; browser extensions and phone wallpapers c
         +an be leveraged as "personal ad networks" to shape habits. Appl
         +ied DragonScale addresses c-000078 through c-000086.           
      24  
      25 -2026-05-22: Ingested the PDF "高手的黑箱7：创作" (130 pages). C
         -reated 1 source page ([[高手的黑箱7-创作]]) and 10 concept page
         -s ([[创作能力]], [[人的事物化]], [[创作模式]], [[深度创作]], [[
         -涟漪性与绵延性]], [[人机共创工作流]], [[黑箱化工作流]], [[智能 
         -体工作流]], [[认知成长微笑曲线]], [[生活-创作-商业模式]]). Upda
         -ted [[汤质看本质]] with the final course. Core frame: creation 
         -is the human becoming object through works; AI-assisted creatio
         -n works by black-boxing workflows into input/output chains whil
         -e humans retain question, difference, duration, and taste. Appl
         -ied DragonScale addresses c-000058 through c-000068.           
      25 +2026-06-09: Ingested Anthropic engineering blog "Building Effec
         +tive Agents" (Jan 2025). Created 1 source page ([[Building Effe
         +ctive Agents]]), 1 entity page ([[Anthropic]]), and 7 concept p
         +ages ([[Augmented LLM]], [[Prompt Chaining]], [[Routing (LLM Ag
         +ent)]], [[Parallelization (LLM)]], [[Orchestrator-Workers]], [[
         +Evaluator-Optimizer]], [[Agent-Computer Interface (ACI)]]). Cor
         +e frame: six composable patterns from simple augmented LLMs to 
         +autonomous agents. Applied DragonScale addresses c-000069 throu
         +gh c-000077.                                                   
      26  
      27 -2026-05-22: Ingested the PDF "高手的黑箱6：评价" (68 pages). Cr
         -eated 1 source page ([[高手的黑箱6-评价]]) and 9 concept pages 
         -([[评价能力]], [[评价即权力]], [[评价坐标系]], [[品味判断力]], 
         -[[形神二层作品模型]], [[三一一原则]], [[解释的辩证]], [[真诚金 
         -线]], [[写作优化Prompt]]). Updated [[汤质看本质]] with the sixt
         -h course. Core frame: evaluation is language-ordered judgment a
         -nd power; creation improves through taste, denial, revision, si
         -ncerity, and targeted AI feedback. Applied DragonScale addresse
         -s c-000048 through c-000057.                                   
      27 +2026-05-22: Ingested the PDF "高手的黑箱7：创作" (130 pages). C
         +reated 1 source page and 10 concept pages. Applied DragonScale 
         +addresses c-000058 through c-000068.                           
      28  
      29 -2026-05-22: Ingested the PDF "高手的黑箱5：分析" (53 pages). Cr
         -eated 1 source page ([[高手的黑箱5-分析]]) and 8 concept pages 
         -([[分析能力]], [[质性分析]], [[扎根理论]], [[现象学分析]], [[本
         -质变更法]], [[辩证逆转]], [[差异发问]], [[问题意识]]). Updated 
         -[[汤质看本质]] with the fifth course. Core frame: analysis turn
         -s understanding into knowledge creation through distinction, or
         -ganization, attribution, qualitative inquiry, phenomenological 
         -suspension, and dialectical reversal. Applied DragonScale addre
         -sses c-000039 through c-000047.                                
      30 -                                                               
      31 -2026-05-22: Ingested the PDF "高手的黑箱4：应用" (53 pages). Cr
         -eated 1 source page ([[高手的黑箱4-应用]]) and 8 concept pages 
         -([[知识应用]], [[结构化知识]], [[菜谱型知识]], [[知行显隐四象限
         -]], [[元认知知识]], [[WOOP模型]], [[GROW模型]], [[对比反馈练习]
         -]). Updated [[汤质看本质]] with the fourth course. Core frame: 
         -application means bringing understanding into reality; knowledg
         -e lands through structured models, recipe-like procedures, and 
         -metacognitive prompts that help cross the知/行 and显/隐 barrier
         -s. Applied DragonScale addresses c-000030 through c-000038.    
      32 -                                                               
      33 -2026-05-22: Ingested the PDF "高手的黑箱3：理解" (54 pages). Cr
         -eated 1 source page ([[高手的黑箱3-理解]]) and 7 concept pages 
         -([[深度理解]], [[认知负荷理论]], [[元素交互性]], [[分割策略]], 
         -[[交替实例]], [[概念地图]], [[抽象思维]]). Updated [[汤质看本质
         -]] with the third course. Key frame: understanding is not memor
         -y but depends on long-term memory and prior knowledge; the oper
         -ational path is 分解复杂，呈现复杂，穿透复杂. Applied DragonSca
         -le addresses c-000022 through c-000029.                        
      34 -                                                               
      35 -2026-05-21 (afternoon): Ingested the PDF "高手的黑箱2：记忆与知
         -识管理" (66 pages, ~20k words). Created 1 source page ([[高手的
         -黑箱2-记忆]]), 5 concept pages ([[记忆的辩证法]], [[预测处理理 
         -论]], [[最小记忆策略]], [[记忆三原则]], [[AI时代知识管理术]]), 
         -and 1 entity page ([[汤质看本质]]). Updated [[index]], [[log]],
         - and [[hot]]. Applied DragonScale Mechanism 2 (deterministic pa
         -ge addresses) assigning addresses c-000015 through c-000021. Al
         -l 3 test suites (address, tiling, boundary) pass flawlessly on 
         -Windows with msvcrt and python-compatibility improvements.     
      36 -                                                               
      37 -2026-04-24 (late night): v1.6.0 public release notes shipped. `
         -docs/releases/v1.6.0.md` (Karpathy-style, 346 lines) establishe
         -s the release-notes convention. Three original SVGs at `wiki/me
         -ta/dragonscale-{mechanism-overview,6-test-flow,frontier-graph}.
         -svg` carry the visual load; Wikipedia dragon curve referenced b
         -y text link only (no binary vendoring). R4 codex verifier ACCEP
         -T WITH FIXES, 3 wording fixes applied. User runs `gh release cr
         -eate v1.6.0 --notes-file docs/releases/v1.6.0.md` when ready. C
         -ommits `85515bb` (docs), plus wiki/meta/ auto-commits for SVGs.
      38 -                                                               
      39 -2026-04-24 (night): DragonScale end-to-end validation pass. Six
         --test menu run via Teams orchestration (codex gpt-5.4 for M1 dr
         -y-run, M1 commit, M4 autoresearch; chair for ollama pull, M2 al
         -locate, M3 full tiling). All six green. First real fold committ
         -ed (`wiki/folds/fold-k3-from-2026-04-23-to-2026-04-24-n8.md`, 1
         -15 lines, 8 children). First real tiling report at `wiki/meta/t
         -iling-report-2026-04-24.md` (0 errors, 15 review pairs). M2 cou
         -nter advanced 2 to 3, `c-000002` reserved-unassigned. M4 autore
         -search filed 3 new concept pages (`Persistent Wiki Artifact`, `
         -Source-First Synthesis`, `Query-Time Retrieval`) extending `[[H
         -ow does the LLM Wiki pattern work]]` with Karpathy gist + RAG +
         - MemGPT + Obsidian docs as sources. v1.6.0 validated.          
      40 -                                                               
      41 -2026-04-24 (evening): v1.6.0 closeout via Teams approach (chair
         --led, codex gpt-5.4 for sub-agents). 2 explorers (closeout gaps
         - + doc surface). 6 bounded writes (non-overlapping scope): `doc
         -s/dragonscale-guide.md` (new, 563 lines), `wiki/meta/2026-04-24
         --v1.6.0-release-session.md` (new, 346 lines), `wiki/meta/bounda
         -ry-frontier-2026-04-24.md` (first real M4 run artifact, new), `
         -docs/install-guide.md` (1.5.0 to 1.6.0 + M4 callout + flat-extr
         -active correction), `README.md` (parenthetical + guide link), `
         -wiki/hot.md` (drift fixes). 1 adversarial verifier returned ACC
         -EPT WITH FIXES; all 11 fixes applied in place. Docs commit `eb1
         -562f`. `make test` green (74+ assertions). Still no git tags fo
         -r v1.5.0 / v1.5.1 / v1.6.0. User requested gpt-5.5; API rejects
         - it on this codex CLI; gpt-5.4 used throughout.                
      42 -                                                               
      43 -2026-04-24 (late): Phase 4 shipped. Mechanism 4 (boundary-first
         - autoresearch) implemented as `scripts/boundary-score.py` with 
         -expanded test coverage. `/autoresearch` without a topic now off
         -ers frontier candidates (opt-in, agenda-control labeled). Cross
         --file status updated. Version bumped to 1.6.0 in `plugin.json` 
         -+ `marketplace.json`; no git tag created locally (only pre-Drag
         -onScale tags `v1.1` - `v1.4.3` exist).                         
      44 -                                                               
      45 -2026-04-24 (afternoon): Phase 3.6 hardening, five surgical fixe
         -s (tiling --report path confinement, rollout baseline, AGENTS.m
         -d consistency, wiki-ingest .raw contradiction, install-guide ve
         -rsion). v1.5.1.                                                
      46 -                                                               
      47 -2026-04-24 (morning): Phase 3.5 hardening pass. Cross-phase aud
         -it resolved 10 hold-ship items. At that point Mechanism 4 was m
         -arked NOT IMPLEMENTED (later reversed in Phase 4 the same day).
         - `bin/setup-dragonscale.sh` + tests + Makefile added, CHANGELOG
         - created, versions synced to 1.5.0.                            
      48 -                                                               
      49 -2026-04-23 (3): Phase 3 complete. Semantic tiling lint shipped 
         -as opt-in. `scripts/tiling-check.py` with flock-guarded atomic 
         -cache, localhost-locked OLLAMA_URL default, symlink rejection, 
         -model-drift invalidation, and banded thresholds (error>=0.90, r
         -eview>=0.80, conservative seeds). 4 codex review rounds, 10/10 
         -accept.                                                        
      50 -                                                               
      51 -2026-04-23 (2): Phase 2 complete. Deterministic page addresses 
         -MVP via `scripts/allocate-address.sh` (flock-guarded, recovers 
         -counter from max observed). New frontmatter `address: c-NNNNNN`
         -. `wiki-ingest` and `wiki-lint` updated with opt-in Address Ass
         -ignment and Validation sections. 3 codex rounds, 8/8 accept.   
      52 -                                                               
      53 -2026-04-23 (1): Phase 0-1 complete. DragonScale Memory spec (`w
         -iki/concepts/DragonScale Memory.md` v0.3) plus `skills/wiki-fol
         -d/` for Mechanism 1 (log rollups, dry-run verified). Survived m
         -ulti-round codex review.                                       
      54 -                                                               
      29  ## Plugin State
      30  
      57 -- **Version**: 1.6.0 (Phase 4 shipped; plugin.json + marketplac
         -e.json synced; 1.5.1 was the Phase 3.6 hardening point release)
      58 -- **Install ID**: `claude-obsidian@claude-obsidian-marketplace`
      31 +- **Version**: 1.6.0 (Phase 4 shipped)                         
      32  - **Skills**: 11 (wiki, wiki-ingest, wiki-query, wiki-lint, wik
          i-fold, save, autoresearch, canvas, defuddle, obsidian-bases, o
          bsidian-markdown)
      60 -- **Scripts**: `scripts/allocate-address.sh`, `scripts/tiling-c
         -heck.py`, `scripts/boundary-score.py` (all opt-in; feature-dete
         -cted by skills)                                                
      61 -- **Setup**: `bin/setup-vault.sh` (base vault), `bin/setup-drag
         -onscale.sh` (opt-in DragonScale), `bin/setup-multi-agent.sh` (m
         -ulti-agent bootstrap)                                          
      62 -- **Tests**: `make test` runs `tests/test_allocate_address.sh`,
         - `tests/test_tiling_check.py`, `tests/test_boundary_score.py`. 
         -Zero ollama dependency for core tests.                         
      63 -- **Hooks**: 4 (SessionStart, PostCompact, PostToolUse [stages 
         -wiki/, .raw/, .vault-meta/], Stop)                             
      33 +- **Next DragonScale address**: 87                             
      34  
      65 -## DragonScale Mechanisms                                      
      35 +## Key Recent Facts                                            
      36  
      67 -1. **Fold operator** (Mechanism 1): `skills/wiki-fold/`, dry-ru
         -n verified AND first real fold committed at `wiki/folds/fold-k3
         --from-2026-04-23-to-2026-04-24-n8.md`.                         
      68 -2. **Deterministic addresses** (Mechanism 2): shipped and exerc
         -ised; vault counter next value is 69. `c-000001` on DragonScale
         - Memory.md; `c-000015` through `c-000068` assigned during the  
         -高手的黑箱 PDF ingests. Gaps are acceptable per spec.          
      69 -3. **Semantic tiling lint** (Mechanism 3): shipped and activate
         -d. `nomic-embed-text` pulled; first tiling report at `wiki/meta
         -/tiling-report-2026-04-24.md` (0 errors, 15 review-band pairs).
      70 -4. **Boundary-first autoresearch** (Mechanism 4): shipped (Phas
         -e 4, opt-in). `scripts/boundary-score.py` + `tests/test_boundar
         -y_score.py`. `/autoresearch` without a topic surfaces top-5 fro
         -ntier pages as candidates; user picks, overrides, or declines. 
         -Explicitly labeled "agenda control" in both spec and skill.    
      37 +- The ljg-learn transcript bridges humanities storytelling with
         + vibe-coded product development, introducing concepts like Desi
         +gn MD tokens, playground-based design exploration, and personal
         + ad networks for habit shaping                                 
      38 +- Opinionated products survive: generic "all-in-one AI" tools c
         +ompete directly with general assistants like Claude; sharp, spe
         +cific opinions are the differentiator                          
      39 +- Design MD: declarative markdown design tokens outperform HTML
         + templates for LLM front-end generation because templates cause
         + overfitting                                                   
      40 +- Build to Learn: the best CS course is your own vibe-coded pro
         +ject; reverse the traditional bottom-up curriculum             
      41  
      72 -## Key Lessons from This Release Cycle                         
      73 -                                                               
      74 -1. Cross-phase audits are essential. Individual phase reviews m
         -iss drift between phases.                                      
      75 -2. Opt-in feature detection (`[ -x script ] && [ -f state ]`) p
         -reserves default plugin behavior for adopters and non-adopters 
         -alike.                                                         
      76 -3. PostToolUse hook matcher is `Write|Edit`, so Bash writes don
         -'t fire it. Scripts that mutate tracked state must be Bash-only
         - to avoid side-effect commits.                                 
      77 -4. Seed-vault self-consistency matters: if the spec says post-r
         -ollout pages need addresses, the concept page itself has to hav
         -e one.                                                         
      78 -5. Codex adversarial review rounds stop when the punch list is 
         -empty, not when the author feels done.                         
      79 -                                                               
      80 -## Style Preferences                                           
      81 -                                                               
      82 -- No em dashes (U+2014) or `--` as punctuation. Periods, commas
         -, colons, or parentheses. Hyphens in compound words are fine.  
      83 -- Short and direct responses. No trailing summaries.           
      84 -- Parallel tool calls when independent.                        
      85 -                                                               
      42  ## Active Threads
      43  
      88 -- DragonScale Mechanism 4 shipped in Phase 4 as an opt-in Topic
         - Selection mode in `skills/autoresearch/`. All four DragonScale
         - mechanisms are now shipped and feature-gated.                 
      89 -- v1.6.0 not yet pushed to GitHub (local commits only, no git t
         -ag created). User controls push and tag timing.                
      90 -- CLAUDE.md has one pre-existing uncommitted change ("Release B
         -log Post" section) that predates this session.                 
      91 -                                                               
      92 -## Repo Locations                                              
      93 -                                                               
      94 -- Working: `E:/workspace/github/claude-obsidian/`              
      95 -- Public: https://github.com/AgriciDaniel/claude-obsidian      
      44 +- DragonScale Mechanism 4 shipped in Phase 4 as opt-in. All fou
         +r mechanisms are now shipped and feature-gated.                
      45 +- v1.6.0 not yet pushed to GitHub (local commits only). User co
         +ntrols push and tag timing.                                    
      46   No newline at end of file

  Thought for 7s (ctrl+o to expand)

● Ingest complete. Here's the summary:

  Ingest: Code as a Medium for Storytelling

  Source: ljg-learn presentation transcript, saved to
  .raw/articles/code-as-a-medium-for-storytelling-2026-07-02.md

  Pages Created (9)

  ┌───────────────────────────────────────┬─────────────────┬──────────┐
  │                 Page                  │      Type       │ Address  │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[Code as a Medium for Storytelling]] │ source          │ c-000078 │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[ljg-learn]]                         │ entity (person) │ c-000079 │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[Vibe Coding]]                       │ concept         │ c-000080 │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[Design MD]]                         │ concept         │ c-000081 │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[Playgrounds (LLM Design)]]          │ concept         │ c-000082 │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[Personal Ad Network]]               │ concept         │ c-000083 │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[Content Remixing]]                  │ concept         │ c-000084 │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[Build to Learn]]                    │ concept         │ c-000085 │
  ├───────────────────────────────────────┼─────────────────┼──────────┤
  │ [[Opinionated Products]]              │ concept         │ c-000086 │
  └───────────────────────────────────────┴─────────────────┴──────────┘

  Pages Updated (6)

  [[index]], [[log]], [[hot]], [[concepts/_index]], [[entities/_index]],
  [[sources/_index]]

  Key Insight

  The transcript bridges humanities storytelling with vibe-coded product
  development. Coding is evolving from a profession to a general skill (like
  writing), and products survive through sharp, specific opinions rather than
  generic all-in-one functionality. The talk introduces several novel concepts:
  Design MD tokens (declarative over imperative templates), playground-based
  design exploration, personal ad networks for habit shaping, and the
  build-to-learn educational philosophy. Complements the existing
  [[智能体工作流]] and agent architecture patterns with a product-design and
  self-expression lens.

✻ Sautéed for 6m 37s

❯ /model                                                                        
  ⎿  Set model to qnaigc/claude-4.6-sonnet and saved as your default for new
     sessions

❯ /model                                                                        
  ⎿  Set model to qnaigc/deepseek/deepseek-v4-pro and saved as your default for
     new sessions

❯ /model                                                                        
  ⎿  Set model to qnaigc/openai/gpt-5.5 and saved as your default for new
     sessions

❯ /ljg-read                                                                     
和我一起共读这个文本，不求速度，只求深度理解。从理论学习到实践落地，逐步完成。  

● Skill(claude-api)
  ⎿  Successfully loaded skill

● claude(analyze transcript map)
  ⎿  Done (9 tool uses · 30.3k tokens · 1m 29s)
  (ctrl+o to expand)

● Phase 0: 全局地图

  我们先不急着逐段读。先把整篇文章的骨架摸出来。
  我把这篇文本当作一篇英文口语演讲稿来读，里面有很多转录误差，比如 “cloud code”
  实际多半是 “Claude Code”，“clock” 也是 “Claude”。

  一句话摘要

  这篇演讲把 AI 时代的“写代码”从一种工程职业重新解释为一种人人可用的表达媒介：像
  写作一样，代码可以承载个人品味、观点、行为设计和故事。

  全文结构地图

  Code as a Medium for Storytelling
  |
  +-- 1. 我为什么能从这个角度谈代码
  |   |
  |   +-- 我不是传统程序员
  |   +-- 我来自 humanities / writing / marketing
  |   +-- AI coding agents 让非工程背景的人也能真实发布产品
  |
  +-- 2. 我做了什么
  |   |
  |   +-- Front-End Slides
  |   |   |
  |   |   +-- HTML 替代 PowerPoint
  |   |   +-- design.md 替代传统模板
  |   |   +-- playground 用来探索字体、颜色、动画
  |   |
  |   +-- 修改自己的软件界面
  |   |   |
  |   |   +-- Tab Out: 把新标签页变成关闭 tab 的任务控制台
  |   |   +-- Chrome extension 改造日常网站
  |   |   +-- personal ad network: 用自己的注意力入口塑造自己
  |   |
  |   +-- 内容 remix 和学习工具
  |       |
  |       +-- 长视频 -> transcript / article / notes / newsletter
  |       +-- podcast -> physical book
  |       +-- codebase -> course
  |       +-- spreadsheet -> dashboard
  |
  +-- 3. 我是怎么做出来的
  |   |
  |   +-- 产品想法来自 user pain x technology capability
  |   +-- 从真实行为出发，不从理想自我出发
  |   +-- 把 AI 当 co-founder，而不是 employee
  |   +-- 描述问题，不急着描述方案
  |   +-- cut more than you add
  |   +-- build in public
  |   +-- make it fun
  |
  +-- 4. 为什么这件事重要
      |
      +-- coding 正从 profession 变成 skill
      +-- engineering 仍然是严肃职业
      +-- coding 可以像 writing 一样成为通用表达能力
      +-- vibe coding 是 self-expression
      +-- code is a medium for storytelling

  段落分类概览

  这是 Agent 判断，你可以随时覆盖。

  1. [筋] 开场定位
  她说明自己不是传统工程背景，所以会从另一个镜头谈代码。
  2. [骨] 身份转折
  从“我不是 coder / 我不学代码”的 humanities person，到借助 AI coding agent
  发布真实产品。
  这是全文可信度来源。
  3. [肌] Front-End Slides 案例
  用 HTML 做演示文稿，用 AI 的前端能力替代 PowerPoint 的像素劳动。
  4. [骨] HTML 作为 AI 原生画布
  这里不只是说 slides，而是在说：网页技术变成了新的表达空间。
  5. [肌] 审美方法
  design.md、参考图、playground、SVG，用来避免 AI slop。
  这里讲的是“品味如何被编码”。
  6. [肌] Tab Out 案例
  把新标签页变成 tab mission control，让关闭标签页变得 addictive。
  7. [骨] 个人软件界面观
  你不必接受默认软件界面。你可以改造每天使用的网站，让它服务于你的目标。
  8. [肌] 长视频学习工具
  transcript、chapter、quote、notes、magazine article、business biography。
  核心是把内容换成自己更能吸收的形态。
  9. [骨] Build to Learn
  AI 时代不必先学完整 CS 再做项目。可以先 build，再把自己的项目反向变成课程。
  10. [骨] 产品想法来源
     好产品来自 user pain 和 technology capability
  的交叉。可以从人出发，也可以从技术出发。
  11. [骨] 小而有观点的产品
     all-in-one AI agent 太泛。真正有生命力的产品要小、尖、有 opinion、有 soul。
  12. [骨] 构建方法论
     把模型当 co-founder。描述 mess，而不是
  solution。围绕真实行为迭代。多减法。公开构建。保持好玩。
  13. [骨] skill 的生成方式
     skill
  不是一开始设计出来的，而是把一次成功实践中的判断、反馈、品味封装起来。
  14. [骨] 终局论点
     coding 从 profession 变成 skill，再变成
  self-expression。代码是继文字、视频之后的新叙事媒介。

  最值得精读的 5 个骨架段

  1. 身份转折：从“不学代码”到发布产品
  这里决定了全文不是技术宣言，而是身份转化叙事。
  2. HTML 作为 AI 原生画布
  这里出现了“媒介”的核心判断。她不是在说工具效率，而是在说表达形式变了。
  3. 个人软件界面观
  这是很有力量的一段：软件不再只是别人给你的环境，而可以被个人重新布置。
  4. 小而有观点的产品
  这是她的产品哲学核心。她反对泛化，强调产品必须有具体对象、具体场景、具体态度。
  5. coding 从 profession 到 skill，再到 self-expression
  这是全文收束。她把 code 类比为 writing，同时区分 engineering 和 coding。

  这篇文章真正值得追的问题

  不是：

  普通人会不会取代工程师？

  而是：

  当代码变成表达媒介之后，什么东西会变得更重要？

  我的初步判断是：更重要的不是语法能力，而是品味、问题感、行为观察、减法能力，以
  及把观点做成可用东西的冲动。

  进入逐段伴读前，我先问你一个问题

  这篇文本里，你现在最想先读深的是哪一条线？

  1. 身份线：一个 humanities person 如何变成 vibe coder
  2. 媒介线：为什么 HTML / code 可以成为 storytelling medium
  3. 产品线：为什么小而有观点的产品比 all-in-one AI 更有生命力
  4. 实践线：普通人如何把这个方法落到自己的项目里

  如果你不选，我建议我们从 身份线
  开始。因为那是全文的入口：她为什么有资格重新定义 coding。

✻ Baked for 2m 26s

❯ 好的                                                                          

● Phase 1: 从身份线开始

  我们先读第一组语义段。
  这一组的功能是：建立说话者位置。她不是从“工程师如何看 AI
  编程”出发，而是从“一个原本拒绝学代码的人，为什么突然开始用代码表达自己”出发。

  第 1 组：我不是从传统程序员位置说话

  原文口语转录大意：

  The theme of my presentation is code as a medium for storytelling.
  I think because I don't come from a traditional background,
  I think of coding from a different lens from most professional engineers or
  programmers.
  Today I'll talk about a few things:
  my own background, how I started vibe coding,
  the projects I've built, how I built them,
  and why it matters.

  直译层（信）

  我这次演讲的主题是：代码作为一种讲故事的媒介。

  我想，因为我并不是来自传统背景，所以我看待 coding
  的镜头，和大多数专业工程师或程序员不太一样。

  今天我会讲几件事：
  我的背景，我是怎么开始 vibe coding
  的，我做过哪些项目，我是怎么做这些项目的，以及这件事为什么重要。

  意译层（达）

  她一开场就在重新摆位置：
  她不是要讲“怎么写更好的代码”，也不是要讲“AI 会不会取代程序员”。她要讲的是：当
  一个不是工程师的人开始使用代码时，代码会变成什么。

  所以她的关键词不是：

  efficiency
  productivity
  automation

  而是：

  medium
  storytelling
  lens
  background

  也就是说，她关心的是：代码如何成为一种表达方式。

  点睛层（雅）

  这里的 medium 很关键。

  英文里的 medium 不只是“媒介”这么简单。它同时有三层意思：

  medium = 承载物 + 表达材料 + 连接人与世界的形式

  比如：

  writing is a medium
  film is a medium
  photography is a medium
  HTML can be a medium
  code can be a medium

  所以她说 code as a medium for storytelling，不是说“用代码辅助做故事”，而是说：
  代码本身可以像文字、影像、摄影一样，成为讲故事的材料。

  结构标注

  这是全文的立场开场。她先声明自己不是传统程序员，因此她接下来对 coding
  的定义不会从工程职业出发，而会从表达、创作、产品和个人经验出发。

  先停一下：第一个小问题

  这里她说自己“不是传统背景”，所以能从 different lens 看 coding。

  你觉得这个 different lens 最可能带来什么？

  A. 她会更少被工程规范束缚，所以更容易把代码看成表达材料
  B. 她可能低估 engineering 的复杂度，所以有些判断会太乐观
  C. 两者都有：她的优势和盲点来自同一个地方

  你可以直接选 A/B/C，也可以用自己的话说。

✻ Cogitated for 21s

※ recap: 我们在用 ljg-read 深读《Code as a Medium for Storytelling》，已完成全局地图并进入第一段“非传统背景如何形成不同 coding 视角”。下一步请回答：这个 different lens 更像优势、盲点，还是两者都有？ (disable recaps in /config)

❯ A                                                                             

● 确认：你选 A，是抓到了这段的正面力量

  你的判断是：

  非工程背景 -> 少一些既有框架 -> 更容易把代码看成表达材料

  我觉得这个抓得准。

  因为如果一个人从传统工程训练进入 coding，他首先看到的往往是：

  correctness
  architecture
  maintainability
  scalability
  security
  performance

  这些当然重要，但它们会把 code 首先放在“系统能不能稳定运行”的问题里。

  而她从 humanities / storytelling 进入，首先看到的是另一组东西：

  voice
  taste
  form
  audience
  experience
  meaning

  所以她会自然地问：

  这个东西表达了什么？
  它让人产生什么感觉？
  它改变了我的行为吗？
  它有没有我的品味？
  它是不是一个可以被分享的故事？

  这就是她的 different lens。

  但我们做一个压力测试

  如果有人反驳她：

  你之所以能把 coding 看成 storytelling，
  只是因为你做的项目都比较轻量：slides、Chrome extension、个人工具、内容 remix。
  一旦进入真正复杂的软件系统，
  code 首先还是 engineering，不是 storytelling。

  这个反驳其实不弱。

  你会怎么回应？

  你可以从三个方向里选一个：

  A. 接受反驳：她讲的主要是 personal software / creative tools，不适用于严肃工程
  B. 反驳它：即使在复杂工程里，code 也仍然有表达和叙事维度
  C. 区分层次：engineering 和 storytelling 不是互斥，而是在不同层级同时存在
✻ Sautéed for 14s

❯ C                                                                             

● 很好，C 是最稳的回应

  你没有把她推到一个过度夸张的位置：

  code = storytelling

  而是保留了层次：

  code can be engineering
  and code can be storytelling

  这很关键。因为如果把它说成“代码只是表达”，那就会显得轻飘。
  但如果把它说成“代码只能是工程”，又会错过这篇文章真正想打开的新空间。

  我们可以这样拆：

  engineering layer:
    这个系统能不能正确、稳定、安全、可维护地运行？

  expression layer:
    这个系统为什么要存在？
    它鼓励什么行为？
    它体现了什么品味？
    它向用户讲了一个什么关于生活/工作/学习的故事？

  比如她后面讲的 Tab Out：

  engineering layer:
    Chrome extension 能否正确读取 tabs、关闭 tabs、分组 domains？

  expression layer:
    浏览器默认鼓励你不断打开标签页。
    我想讲一个反方向的故事：
    关闭标签页也可以很爽，也可以像游戏一样。

  所以 storytelling 不是替代 engineering，而是回答另一个问题：

  这个东西的存在方式，表达了什么世界观？

  这一段我们先收束成一句话

  她的入口不是“非工程师也能写代码”这么简单，而是：

  非工程背景让她把 code 首先看成一种表达材料，而不是一种职业边界。

  下面进入第二组：她为什么从“不学代码”转向 vibe
  coding。这里会出现全文第一个真正的转折。

  第 2 组：从“我不学代码”到 AI coding watershed moment

  原文口语转录大意：

  I actually never thought of myself as a coder.
  I studied humanities in school. I never took CS.
  In 2023 I wrote a blog post called "Why I'm Not Learning to Code"
  that kind of went viral.
  At that point I was proudly a humanities person working in tech.
  I was challenging the traditional belief that only technical people can work
  in tech.

  But a lot changed in the past year.
  I started vibe coding maybe a year or two ago.
  At first I tried many web-based tools, but the models weren't good enough.
  I couldn't complete projects. They were mostly demos or little tools for
  myself.
  January this year was a turning point.
  I started using Claude Code and other coding agents,
  and I was able to ship products end to end to users other than myself.

  直译层（信）

  我其实从来没有把自己想成一个 coder。
  我在学校学的是 humanities（人文学科）。我从来没有上过 CS（computer
  science，计算机科学）课。

  2023 年，我写过一篇博客，叫 Why I'm Not Learning to 
  Code（为什么我不学代码），后来有点 viral（走红）。

  那个时候，我是一个很自豪的、在科技行业工作的人文学科背景的人。
  我在挑战一种传统信念：只有技术人员才能在科技行业工作。

  但是过去一年里，很多事情变了。
  我大概一两年前开始 vibe coding。

  一开始我试了很多 web-based tools（网页上的 AI 编程工具），但当时模型还不够好。
  我没法完成项目。它们基本上只是一些 demo，或者我自己用的小工具。

  今年一月是一个 turning point（转折点）。
  我开始使用 Claude Code 和其他 coding agents。
  于是我能够 end to end（端到端）地发布产品，而且用户不只是我自己。

  术语小注

  vibe coding

  这里不要翻成“氛围编程”就完了。它更像：

  用自然语言、感觉、目标和反馈，驱动 AI agent 写出软件

  不是你逐行控制代码，而是你描述方向、体验、问题、修改意见，让 agent
  把系统搭出来。

  end to end

  也不只是“从头到尾”。在产品语境里，它意味着：

  从 idea -> design -> implementation -> deployment -> real users

  不是 demo，不是玩具，而是可以被别人使用。

  意译层（达）

  她在讲一个身份反转：

  一开始，她甚至是公开拒绝“学代码”的。她的立场是：科技行业不应该只属于技术人，hu
  manities 的人也有资格在 tech 里提出问题、做判断、影响产品。

  但 AI coding agents 改变了她和 code 的关系。
  过去她试过一些工具，但模型能力不够，只能做 demo。到了今年一月，她发现 agent
  已经可以帮她把一个想法做成完整产品，并交给真实用户使用。

  所以她不是“突然爱上写代码”，而是发现：

  code 的门槛从“你是否掌握编程技术”
  转移到了“你是否能描述一个值得被做出来的东西”

  结构标注

  这是全文的身份转折段。它解释了为什么她有资格谈这件事：她的观点不是抽象预测，而
  是从亲身转变中长出来的。

  碰撞问题

  她这里其实想说服你接受一个判断：

  AI coding agents 改变的不是编程效率，而是“谁有资格把想法变成软件”。

  你接受吗？

  A. 接受：资格门槛真的从 coding skill 转向 product judgment / taste / problem
  framing
  B. 部分接受：门槛降低了，但真正发布产品仍然需要很多工程判断
  C. 不接受：这只是少数轻量项目的幻觉，不能说明资格结构真的变了

✻ Churned for 30s

❯ 我感觉我们的讨论偏离了这个文本的主题，主题应该更偏向AI技术的理念和应用方法、  
  落地实践                                                                      

● 对，你这个校正是对的。

  我刚才把入口放在“身份转化”和“code as self-expression”上，确实容易把文本读成一
  篇创作者身份叙事。但如果按你说的目标：AI 
  技术的理念、应用方法、落地实践，这篇文本的重心应该重新摆成：

  不是：她是谁，以及她如何成为 vibe coder
  而是：AI coding agents 改变了什么方法论，以及普通人如何把它落到项目里

  我们重新校准阅读框架。

  新的全文主线

  这篇文本可以读成一套 AI 应用方法论：

  AI 技术理念
  |
  +-- 1. AI 不是工具人，而是 co-founder / collaborator
  |
  +-- 2. 不要先给 solution，要先描述 problem / mess
  |
  +-- 3. 代码不只是实现逻辑，也是表达和界面塑造材料
  |
  +-- 4. AI 的强项不是单纯写代码，而是把想法快速变成可体验原型
  |
  +-- 5. 真正的产品迭代来自使用后的行为反馈，而不是一次性 prompt
  |
  +-- 6. 人的角色从“写更多”转向“判断、减法、品味、选择”
  |
  +-- 7. skill 不是凭空写出来的，而是从真实 workflow 中沉淀出来的

  按你的方向，文本里最重要的不是身份线，而是三层落地法

  Level 1: 理念层
    AI coding agents 改变的不是“写代码更快”
    而是“想法 -> 可用软件”的路径变短了

  Level 2: 方法层
    描述问题，不描述方案
    做 playground，不凭空想象
    用 design.md，而不是死模板
    从真实行为反馈中迭代
    cut more than you add

  Level 3: 实践层
    Front-End Slides
    Tab Out
    YouTube learning tool
    Personal ad network
    Content remixing
    Codebase to Course

  我们应该优先精读的骨架段也要换

  刚才我选了“身份转折”。现在根据你的目标，应该优先读这 5 段：

  1. January as watershed moment
  AI coding agents 从 demo 工具变成能 end-to-end ship products 的技术拐点。
  2. HTML as canvas for AI expression
  为什么 HTML/前端是 AI 特别适合落地的表达界面。
  3. Design MD + playgrounds
  如何把模糊审美转成 AI 可执行的设计约束和探索空间。
  4. Describe problems, not solutions
  AI 协作的核心交互范式：不要把模型当员工，而要当共同思考者。
  5. Cut more than you add / use it for a week
  AI 应用落地的关键不是生成，而是使用、感受、删减、收敛。

  这篇文本真正可提炼的方法论

  我先压缩成一个实践框架：

  AI 应用落地六步

  1. 捕捉一个真实行为痛点
     例：我总是不关 tab，我不会主动整理书签

  2. 不急着定义产品
     先和 AI 讨论这个痛点背后的行为机制

  3. 找一个天然入口
     例：new tab page、X homepage、phone wallpaper、YouTube side panel

  4. 快速做可体验原型
     不是 PRD，不是 mockup，而是能真的放进生活里用的东西

  5. 连续使用一周
     观察自己真实用不用，而不是理论上喜不喜欢

  6. 做减法并封装成 skill / product
     把有效 workflow 固化下来，把无用功能砍掉

  我们从这里重新开始

  我建议下一段不继续身份线，而直接进入这段：

  January this year was a turning point...
  I started using Claude Code and other coding agents,
  and I was able to ship products end to end to users other than myself.

  这一段是全文的技术拐点。

  我们要问的不是“她身份如何变化”，而是：

  AI coding agent 到底改变了软件落地链路中的哪几个环节？

  第一个重新校准后的问题

  你觉得这篇文本里，“AI 技术落地”的关键变化更像哪一个？

  A. 生产力变化：写代码速度变快了
  B. 角色变化：非工程背景的人也能参与构建
  C. 流程变化：从 idea 到 prototype 到 user feedback 的循环变短了
  D. 媒介变化：代码从工程实现变成表达、设计、行为塑造的材料

  我倾向于 C + D。
  如果按“理念到实践”的读法，C 是落地机制，D 是更深的理念变化。

✻ Brewed for 37s