Title: My First Domain Name: Adventures in DNS
Author: Tara Roys
Date: Sun Mar 17 2013 10:16:51 GMT-0600 (CST)
Node: v0.1.102


I've walked through some pretty shady neighborhoods late at night, and I didn't always feel entirely safe.  Setting up my DNS felt like  wandering into a shady neighborhood, getting lost, and asking some dude who looks like a drug dealer for directions.

When I started this project, I knew precisely three things.  First, if I typed http://192.81.214.50:8080/ into the browser, I would go to my blog.  Second, there was some way to make it so that if I typed www.tararoys.com into the browser, I would go to my blog.  Third, I had to buy tararoys.com.

Armed with my invincible ignorance, I set forth into the wrong part of town.  

## Buying a Domain Name

I turned to my trusty friend Google to figure out where to buy a domain name.  Google recommended a website called GoDaddy.  When I went to GoDaddy, I felt like I was talking to a pimp- the name sounds like something from an eighties blaxploitation movie, and the website looks like a blinged-out rapper.  I felt like I was doing something wrong just by dealing with them, but I soldiered on, right up until they asked me for a credit card.  Then my brother found out what I was doing.  

"Don't use GoDaddy." he said.  "Use names.com. That's who I use." 

I navigated to [name.com](name.com) and it looked a lot less sketchy than GoDaddy.  I think I felt better about buying from name.com because their website looks a lot simpler than GoDaddy. I also think my brother's recommendation made it seem a lot safer, too.  Name.com's buying process was a lot simpler than GoDaddy's, and when I bought the domain, I didn't feel quite so much like I was handing my credit card information to a drug dealer.  Soon, I was the proud owner of tararoys.com - for the next year, at least.  

Now all I had to do was figure out how to hook it up to my blog. 

## Hooking up my website to the domain name

I tried asking my brother how to go about doing this, but he didn't really know.  At this point, I had to do something I hate doing: employ some common sense.

My common sense went as follows:  this task is something everybody who owns a website has had to deal with.  It must be a fairly common question.  The people who should know how to do this like the back of their hands are the people who run my server: digital ocean.  They had good tutorals for how to set up my server in the first place, so they probably have a tutorial about this.  I felt beter after my common sense had given me an idea of what to do, but the reason I don't like using it is because common sense actually takes some thinking, and thinking takes effort, especially logical thinking.   

Still, I felt morevcheerful now that I had a way to begin looking for help.  My brother and I went to Digital Ocean's Help and Community page and started browsing through their tutorials.   He spotted a tutorial that looked promising: "[Setting up a Host Name with Digital Ocean](https://www.digitalocean.com/community/articles/how-to-set-up-a-host-name-with-digitalocean).". 

I wasn't sure if this was what I wanted.  _What the hell is a host name?_ I thought.  But I clicked on it and started reading, and it became apparent that this was what I was looking for.  I figured host name must be another name for domain name. (note: [it's not](http://www.bleepingcomputer.com/tutorials/domain-names-and-hostnames/))


#Following the tutorial

I started reading through the tutorial, and immediately ran into a problem:  I felt stupid.  Why did I feel stupid ?  I didn't understand half of what they were talking about.  For example, let's look at the following paragraph.  

>The first thing you need to do to set up your host name is to change your domain name
 server to point to the DigitalOcean name servers. You can do this through your domain
  registrar’s website. 

Now, let's replace every concept I didn't understand with the words blah blah.

>The first thing you need to do to set up your blah blah is to change your blah blah blah
to point to the DigitalOcean blah blah blah. You can do this through your blah blah blah
website. 

Not understanding what theynwere talking about made mee feel stupid, and feeling stupid made me feel unmotivated. To motivate myself aain, I had to use out my least favorite weapon: common sense.  I asked my hurt feelings, Does it matter if I don't know these terms? The tutorial also explained exactly what to do, so I told myself that it would be like following a recipe for making cake:  if I followed the recipe exactly, I would have delicious cake at the end of it and not have to know about the chemical reactions that go into making cake.  With the prospect of cake, I felt better, and started working again.  

The trouble is that I've never been good at following recipes exactly.

I followed the tutorial as best I could.  At the end of the tutorial, it explained that due to some internet magic it would take awhile for the whole internet to figure out that tararoys.com now pointed to http://192.81.214.50:8080/, and I would need to wait up to a day to see my changes take effect. So I went to bed.  

#In which my name is used in vain

The next morning, I awoke to a horrifying sight: tararoys.com was pointed at a page of ads.  Something had gone wrong.  But what?

Annoyed, I set out to discover what was wrong.  

I don't recall how I ran across the term 'domain parking', but that phrase turned out to be the search tem that let me solve the mystery.  See, I bought the domain name tararoys.com from name.com, but, somehow, despite following the tutorial, I had not managed to tell name.com where my website was.  Since I hadn't told them where my website was, they couldn't direct anyone there.  So they decided that, instead of saying "Page not found," they would show a page of ads.  This, as they explain, is called [domain parking](http://www.name.com/blog/general/domains/2012/01/pro-tip-how-to-get-rid-of-that-pesky-parking-page/). 

Some people think this practice is [a bit scummy](http://nathanhammond.com/namedotcom-another-unscrupulous-registrar). After thinking about it for a bit, I was forced to agree.  Let's say, in real life, that you were building a store.  You hire a person, and tell them, "My store's name is Awesome Stuff.  I'm going to pay you to make sure that nobody else has a store named Awesome Stuff.  Also, when I get the store built, I'm going to send a bunch of people your way, and I want you to tell them where Awesome Stuff is." The person nods, smiles, and takes your money.  The next day, you come back and find out that he's built as store called Awesome Stuff and is selling shrunken heads and porn magazines from it. "But wait!" you say, "Why are you selling stuff using MY name?" He shrugs and says, "You weren't open yet, and I needed to make some money.  I'll stop as soon as you tell me where your store is." 

With that analogy in mind, I had to figure out how to tell name.com where my store was, so they would stop using my name in vain and do what I hired them to do- point people at my webpage.

I went back to the [tutorial](https://www.digitalocean.com/community/articles/how-to-set-up-a-host-name-with-digitalocean). and zeroed in on step two: Change Your Domain Server.   That was the only step that had involved changing settings in my name.com account, and since it was name.com that was putting up the parkng page, I figured the problem had to be there.  The tricky thing was that name.com didn't have any setting called Domain Server or Domain Name Server:  they just had a setting called nameserver, so I assumed nameserver and domain name server were the same thing.  Fortunately, this assumption was justified.  

I opened up the Edit Nameserver setting, and found  all three digital ocean nameservers, just like the directions told me to.  There were also a couple of tips for newbies written at the bottom.  One of them caught my eye.  

>If you do change your nameservers, make sure that you are using only one set
of nameservers!  If you do not delete old nameservers, your domain will resolve 
inconsistantly.  

I looked back at my nameservers.  There were four of them: three digital ocean nameservers, and one name.com nameserver. When I had added the Digital Ocean nameservers, I didn't know I was supposed to delete the old one.  Oops.  I deleted the name.com nameserver, and waited.  Three hours later, the page of ads stopped showing up.  Instead, I got a 'server does not exist' error.  Progress, of sorts.  I was both happy  I had gotten the ads to go away and annoyed that I hadn't fixed the problem.    

This whole thing got me thinking, what exactly is a nameserver?  Let's go back to an analogy: the domain registrar is the person I hired to 1.make sure nobody else in the world was using my name and 2. tell people where to find me.  This is, in fact, two different services.   Instead of being done by one person, they can be done by two people.  The person who makes sure nobody else is using my name is the registrar.  The person who tells people where to find me is the nameserver.  When I put a list of servers in the edit nameserver page, I am basically telling the registrar, "These are the people I trust to tell everyone where I am.  Please tell the internet to talk to these people if they want to find me."

By leaving the name.com server on the list, I was, in essence, trusting the wrong person.  Since I hadn't told the name.com nameserver where I was located, he cheerfully directed everyone to a page of ads - in essence, using my name to make him some money.  Booting him off the list solved that problem, but it did make me feel leary of names.com.  This, more than anything, contributed to my feeling that I was walking through a shady neighborhood.  I considered not using name.om, but a quick survey of google implied that ethical domain registrars don't exist.  Name.com is still better than most because their website is far easier to use. Maybe I'm just hanging out with the local friendly marajuana dealer rather than dealing with a pimp.  One can hope, anyway.  

# Server Side Issues

At this point, I began to feel like I was making some real progress in understanding how everything was hooked together.  Yes, I had a lot of issues, but I could feel momentum building behind me and I was more and more confident I would be able to solve them.  I also thought I knew wht might be the source of the server not found error, which was a bit better than having no idea what to do next.  

Now that I had told the registrar what nameservers to use, I actually had to tell the nameservers where I was.  In short, I had to tell the nameservers that when people come up and ask for tararoys.com, I want the nameservers to take them to my address.  The technical term for what the nameservers are doing is Domain Name Service of DNS, and giving the nameservers directions to my site is called changing the DNS settings.  

After figuring out what a nameserver was, I had to figure out why tararoys.com was coming up with a "Server Not Found" error.  This time, it had to do with the DNS settings, and I had a sneaking suspicion about what I had done wrong.  

Earlier I likened following the turorial to baking a cake- if you follow the directions exactly, you get a cake at the end.  Anyone who has ever seen me cook knows that I don't follow recipies exactly- instead, I occasionally make substitutes when I think I know better.  Unfortunately, 95% of the time, I genuinely have no idea what I'm doing, and screw the recipe up.  

So, you might ask, what unwise substitution had I made? When following Step Three—Configure your Domain, instead of entering my ip address 192.81.214.50, I entered my ip address and a port number: 192.81.214.50:8080.    

My logic was as follows:  when I typed 192.81.214.50 into the browser, nothing showed up.  When I typed 192.81.214.50:8080 into the browser, my website showed up.  So, I figured if I wanted tararoys.com to go to my website, I had better tell it to go to port 8080 as well.  

This substitution turned out to be a bad thing.  See, a domain name service's job is to point a domain name at an IP address.  That's it.  It is most certainly not it's job to know which port on my server my website is running on.  I ended up deciding that a DNS is like a taxi: you tell them the name of the place you want to go to, and  it's their job to get a you to that adress.  When you get there, they drop you off outside the building.  Asking the DNS to point tararoys.com at port :8080 was like asking a taxi driver to get out of his car and guide his passenger to the right office in the building.  It ain't gonna happen, because it's not his job.  

So I changed the ip address to 192.81.214.50, and typed tararoys.com:8080 into the browser.  It worked!  Yay!  

#Puttering around with ports

I still wanted to get rid of the :8080 at the end of the URL, though.  That meant that I had to figure out exactly what ports were.  After reading a few less-than-helpful definitions, I decided that if a server is a building, a port is a room in a building, and the port number is like a room number: it tells you which room to go to.

But I didn't want people to have to type tararoys.com:8080, or, to put it another way, I didn't want the person coming to my building to have to know what room number to go to.  I wanted someone to meet them at the front door and guide them to the right room.  

A little poking around on the internet revealed that whenever browsers go to a particular address, they automatically try to go to port 80.  Port 80 is the default port for http traffic.  Http traffic means " people who come to my server looking for a webstite,"  so I decided to think of "http traffic" as the general public.  Whenever normal people go into a building, they go through the front door.  : so port 80 is the front door.  Nobody has to specifically tell people to go in the front door, just like nobody has to specifically tell a web-browser to use port 80.  it just automatically does it.  Port 8080, on the other hand, is like a little back office hidden somewhere in the building.  

What did this mean?  When I type tararoys.com into the browser, it's the same thing as typing tararoys.com:80.  That meant that in order for people to use tararoys.com to get to my website, I would need to switch my website to port 80, so that when people came in the front door of my building, they would immediately see my magnificent blog.  

The trouble with switching my website to port 80 is that it would involve monkeying with the source code of something called the node.js server.  Here's where I ran into a clash of terms.  There's this thing called a server, and I've stated thata server is like a building.  It has ports, and ports are like rooms in the building.  Those rooms are offices where people work, and in one office, there's a person whose job it is to paint a pretty pictures and show it to you when you walk in the room.  That picture is my website, and that person is also called a server.  Specifically, he's called an http server.  So in your server, you have ports, and in those ports are more servers.  This is something that confused me mighily.  

Let's talk about the man painting pictures, aka the http server, for a second.   He is a great artist, amd makes lovely pictures of my blog, but he only speaks Hungarian.  He gets along in an english-speaking world because somebody wrote him a very detailed list of instructions in hungarian of what to do and where to do it.  I want to tell him to take his picture and stand at the front door and show it to people, but I don't speak hungarian, so I can't.  In computery terms, my http server has a list of instructions that tells it what do to and where to do it, and hidden somewhere in that list is exactly which port to be at.  However, it is written in a language called node.js, which is basically hungarian to me.  (Yes, yes, I know that node.js is not a language but a framework, and that node.js is written in a language called javascript. It's an anaolgy.  Just roll with it.). The point is, I don't know enough node.js to tell my server what port to listen at, just like I can't tell my hungarian artist to move out of the office he's in and come to the front door.  My server's instructions tll it thst it should be at port :8080.  If I tried to tll ito to move to port 80, I would probably end up with a hysterical artist who would throw down his paintings and refuse to show anyone anything, an activity in the computer world known as "fucking up your server."

Fortunately, there was another way:  I could hire someone to meet people at the front door and take them to the painter's office.  This activity is called port forwarding, and I like to think of the guy doing it as the porter.  Unfortunately, the only porter I can hire speaks mandarin, which I don't know how to speak.  Fortunately, somebody on the internet was kind enough to write out the mandarin phrase that would tell him what to do.  
 

The porter's name is iptables, and the command I gave him is 

  [iptables -A PREROUTING -t nat -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 8080](http://stackoverflow.com/a/6848861/1344732)
 
  
These magic words did the trick.  When I typed tararoys.com into the browser, my blog showed up.  I was happy and proud that I had solved a very tricky technical problem.  Finally, my epic DNS adventure was at an end.  


# A Retrospective

This whole process took three days:  two days to do it, and one day to blog it.  When I started out, the only thing I knew was that there had to be a way to point tararoys.com at my blog.  How it might be done was a complete mystery.  For all I knew, the internet ran on the blood of unicorns and I might be asked to sacrifice one to dark lord Voldemort to get things to work.  

The dirty little secret of working with computers is hat the whole thing is driven by your emotions.  I talk a lot about my feelings in this blog:  I say things like I was happy, I was sad, I felt dumb, I felt like my domain registrar was shady, and I was demotivated.   When I think of debugging, I have this image of Spock methidically and logically working his way through a problem without any emotions.  I often feel ashamed that I am not Spock.  The truth is that dealing with my emotions- the hopes, the fears, the frutrations, and the temptation to give in is my biggest challenge.  In fact, one of the hardest things for me to accept was that emotions were a part of the process, and that you could think about and deal with emotions with the same common sense you use to find a tutorial.  

Speaking of emotions, the thing I hate most is ignorance.  My personal definition of ignorance is a complete lack of mental models for how something works.  The biggest result of this process was not the fact that I got my website to work.  Instead, it is the fact that I know have somewhere between five and eleven mental models that represent how various parts of the system works. Models like DNS is like a taxi service, a nameserver is like a person who gives other people directions to your website, and a server is a building help me understand the system and think logically about how it should work.  

I really, really hate having no model for something.  If I have a model for how omething might work, I feel like I have a chance at fixing it, and that. feeling gives me the courage to try and fix it.  Without a model, I might as well be trying things at random, like hauling out my magic wand and shouting "avada kadavra" at the computer.  I've always felt that trying things at random is dangerous: when I do it, I live in constant fear that I might, in my ignorance, screw something up permenantly and get my entire family eaten by sharks.

I have never really overcome this fear, but I have learned to ignore it, mostly by coming up with models and testing them to see if they work. You might have noticed throughout this blog that most of my time is spent using a model to  figuring out what step to take next.  Whenever I describe a model, I usually stop blathering on about how I'm feeling.  There is a reason for this:  When my brain is building a mental model, I'm usually so engaged that I don't have the mental bandwidth to fear things.  The mental model also helped me decide what to do next, and having a next step is prety comforting. Also, when I used a model to figure out what step to take, that step was very small:  changing one setting, executing one command, or figuring out one unfamiliar term.  Small steps create a lot less fear than big steps.  By breaking things down into small steps, I managed to turn a huge, emotionally-charged, unknown process into a bunch of small steps that I could feel confident about.  

The opposite of having a mental model is believing in  magic.  While I made mental models for a lot of steps in the process, there were also a lot of steps where I blindly followed the tutorial without forming any model for how it worked.  This is because, since it did work, I had no need to figure out a mental model to debug it.  I came up with no mental model for A records, CNames, and how the iptable command worked, because when I followed the tutorial and said the magic words, magic happened and it magically worked.  

I'm a bit uncomfortable with magic, partly because I don't like what I don't understand, but mostly because it's so darned boring.  Following instructions blindly is deadly dull.  All magic requires is the ability to read and follow instructions exactly.  It's like typing passages from a latin book when youndon't know any latin: sure, you could do it, but it's incredibly boring and youndon't really have any idea what you are typing.  I have a thirst to know why things work, because the more youn know why things work, the more interesting they become.  

However, magic does have it's place.  At a certain point, I do have to accept that I'll never be able to take the time to create models for everything, and sometimes it's best to make models just for stuff I need and let the rest of the world run on magic.  

And if you want to see magic happen, type tararoys.com into your browser and watch as you are magically whisked to my blog: magic that is the result of my three-day adventure with DNS.  







 





















