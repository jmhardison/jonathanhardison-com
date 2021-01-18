---
author: Jonathan
categories:
  - general
comments: true
date: 2017-07-02 01:00:00
share: null
title: Alexa Skill
---


Over the past week I decided to build and publish an Alexa skill. Yup, that's right, an Alexa skill... why not?

It was one of those adventures in coding that was on my "coding bucking list"... the list that I keep filled to the brim  with things I may never do in my life but are meant to challenge me to do new things. Like my history of being a systems and network engineer, only to turn the corner towards development, and then wind up somewhere in DevOps land. (Though honestly, I'd rather be making games.)

I digress... So what did I do with this Alexa skil? Simple, I built a skill that lets you check the status of online games. At least ones that I've built support for so far. Alexa will respond informing you if the game is up or not. For example, lets say you wanted to check the staus of Secret World Legends because you are now playing that since they re-released TSW as SWL and reset everyone to zero so you must now spend forever replaying the game you already played just to be ready to eventually, maybe, possibly play new content if they ever get to release it.... sorry, vent there.

But the skill checks in one of several fashions. Depending on the game, I may have to scrape the launcher page that gets loaded to harvest the status of the game world and then have Alexa reply. In other cases, there is either an API or a simple JSON payload I can get back that will give me better access to the state of the game. That's it... scrape or hit an API, then inform the user of the state of the game. Pretty simple concept. And what do i call it? Well since I am horrible at names, I call it the most obvious thing I could think of. "Is Game Online"

Lets boil it down some.

To start, I build an API service in NodeJS using Alexa-App sdk. After a basic construct, I published the API on Heroku where I also host my website. At which point the next step was to create the skill itself inside the Alexa developer console. All that is pretty straight forward. And to understand the deliniation, the `api` is responsible for the actual logic in the skill. What you ask for gets worked on by the `api`. But the Alexa skill defines your intent, an operation or request function if you will, and your slots, variables or buckets of words. Alexa's service will key off your intent's utterances, which are simply patters or phrases with your slots in them to harvest the data, and then passes it to your backend. Once there, its your job to work it out and respond back with the actions Alexa should take.

All fine and dandy, but during my first pass for certification it was rejected for some obvious stuff. One item it failed for I swore I tested for, but missed was to prevent access from other skills trying to access your backend. So, as a result, I decided "Well, lets just move this thing over to AWS Lambda where you can lock down access at the service (lambda) and the code level using your requesting app ID. (Which I had already done.). So, a migration of code insued. NodeJS was easily refactored, as Alexa-App already supported both models just by removing the use of ExpressJS. Then a quick upload as a Lambda function and reconfigure of the skil. Followed up by recertification and .. yes, passing certification.

Of course since then I've done more work on the skill backend, which I can do without impacting the front end. Noteably, I've increased the number of supported games and altered respose wording. To effectively round out the skill as a more friendly item and less goofy in some wording choices. And I should also mention that I did all of the testing of the skill using [EchoSim.io](http://echosim.io). EchoSim allows you to run a virtual echo inside of your browser in order to test real Alexa skills in development. While not suitable for every situation, it is definitely worth checking out before you drop money on an Echo. (Unless of course you already have one... the have fun!)

Developing the skill was really fast and easy when leveraging NodeJS and Lambda. And honestly, just reinforced why I love pushing myself into code. Loads of fun, loads of challenge, and a lot of satisfaction in seeing the result. I must have moar of this backend dev work.

Check it out if you get bored. [Is Game Online](http://isgame.online) website, and the repository of code is [here](https://github.com/jmhardison/isgame-online-lambda) hosted on GitHub.

Now if you want to use the app, you can find it on [Amazon](https://www.amazon.com/Jonathan-Hardison-Is-Game-Online/dp/B0739SWX31/ref=sr_1_1?ie=UTF8&qid=1499047972&sr=8-1&keywords=jonathan+hardison) or just ask Alexa to enable `Is Game Online`.