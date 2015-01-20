---
layout: post
title: "Motivations, Projects, and Resolutions"
date: 2014-01-31 09:00:00 -0700
comments: true
categories: development planning programming project
---
The new year is a time to reflect and decide on what to focus your energy. Or,
in some instances, reflect on what projects you didn't finish. I like to look
back and evaluate what projects from the past year deserve more energy, deserve
to be let go, or need more development before they're viable.
<!--more-->
I keep a small notebook that fits comfortable in my jeans pocket for writing
down ideas. Some I'll flesh out and try to find the minimum viable product (MVP).
Some I simply like to flesh out and think about the 'cool' factor. Things that
increase cool factor:

###Real-time###

"Post and response ... is kind of boring. I think most people have become
accustomed to see the spinning wheel load your results."

This has got to be a trendy thing, but it also makes software so nifty these
days. Things like 'real-time collaboration' or sharing or feedback. They all
make software feel not only faster but engaging. Post and response, where you
post data and are then rendered a results view, is kind of boring. I think most
people have become accustomed to see the spinning wheel load your results.

I know at my day job I see that wheel all the time when I'm doing tests. We're
in the midst of launching a new version of our UI for the main part of our
product and while it's beautiful and super fast, there's one part of the
software that actually now takes longer to load - the piece that hooks into a
government integration (of course). The overhaul didn't cause this per se. It
was very well designed and load times across the board are reduced. But its new
architecture requires a certain flow and as such, all operations for this one
piece have to be re-rendered frequently. To ensure data integrity on what's
coming back from the government service, I have to query them (the government)
to get the latest results. This all occurs in real-time but the service is slow
and unfortunately doesn't provide a fast way to get the relevant data. It was
totally over-engineered. At some point I plan to change that, but for now I'm
kind of stuck. Some of the load times have doubled in the new system for this
one piece.

###Social###

"Social also means having a community. If you build a community, meaning forming
a common culture around a topic, idea, belief, etc., then you're more likely to
attract more people from that pool."

Ideas these days tend to have some social component. Sharing an achievement in a
weight loss tracker or a ride you just completed. Not to mention the calls to
action to share that you're using a given product. Moreover, it's almost more
popular now to use social authentication instead of having a database containing
usernames and passwords that you have to protect. This makes sense - now the
concern is not on you if the password store is compromised, you simply send out
an alert email to your affected customers saying "due to the recent ... at
<social network>, we'd recommend you change your password to protect your data
at our site. Please click <here> to view details about the announcement from
<social network>."

Social also means havinthem g a community. If you build a community, meaning
forming a common culture around a topic, idea, belief, etc., then you're more
likely to attract more people from that pool. Word of mouth campaigns are more
budget friendly for you than spending time and money trying to advertise your
project to form communities of one. It's always a good idea to test your idea
against the possibility of building a community with it. Not all ideas can work
that way - some are targeting very specific use cases and that's ok.

###Feedback###

"Feedback isn't just about getting criticism and praise from your users - it's
about getting data on how they use the product."
Having an excellent feedback system users want to utilize instead of avoid is
valuable. For one, your feedback loop is tight and you understand the people
using your product. Getting flooded about feature X having a bug or needing new
functionality? Awesome. No money just went out the door to get a 1 in 50 response
rate. Fix it and fix it fast and tell your users how much you appreciate their
help in making the product they use better. This reinforces the community idea
mentioned above. Empower users to be able to provide you feedback in an
unobstrusive way - don't hound them. Let them choose.

Feedback isn't just about getting criticism and praise from your users - it's
about getting data on how they use the product. Think about analytics early. When
your users creates a new item using your service and sends an invite through the
service to a friend's email, track it. And track whether that friend signed up.
Now you've got analytics on conversion rates from first-party referrals.

##Motivations and Resolutions##

This year I have some simple goals:

###1. Write more blog posts###

I need to be more consistent. I have a number of article topics I have written
down in my notebook I would like to complete. I keep listening to podcasts that
mention you have to just sit down and write to form the habit, and that's
something I need to do. I am out of practice at that. Now when I sit down at my
computer at night, once my son is asleep and the house is quieter, I tend to go
straight to projects. I need to start scheduling time to write at least once a
week, specifically in the realm of tutorials or sharing experiences about how I
solved a particular problem.

###2. Engage on Twitter###

I was one of those that used to make fun of Twitter's core concept - share in a
limited character amount. I tend to be verbose. Sometimes overly verbose. I took
almost every writing intensive course offered in the political science department
at the University of New Hampshire because writing several papers a week was easy
for me - I could always crank out more words. Twitter limits that and forces you
to focus tightly on what you want to communicate. I've been using it for a few
months more actively and I find wonderful and copious amounts of information on
topics that interest me. I'd like to build a bigger network there of like-minded
people so that I can continue to tap that resource for inspiration, help, and the
comfort of being of member of that community.

###3. Pay It Forward###

I have received help from a number of community members as I have learned what I
know. My formal CS education is extremely limited. I'm currently completing
pre-requisites to enroll in a Masters in CS program, but I earned my software
developer position as a self-taught programmer. This means I've accumulated a
lot of knowledge by the generosity of others. So I'd like to return the favor. I
plan to be making posts discussing implementation strategies, coding tutorials,
and some design information.

###4. Release a Web Application to the Public###

I have been working on an application for a few months, mostly figuring out what
I want it to do and doodling on my
[sketchpads](http://www.uistencils.com/products/responsive-sketch-pad), but I've
been coding in small bits here and there over the past month. I'd like to finish
this application and get it out to the public. Mainly, I'd like to be a user on
this site. So I believe others will want to as well.

I hope those reading this reflected on the last year and have come to decisions
about what they'd like to do in 2014. If you'd like to talk to me about code, or
hire me as a [freelancer](http://bluesuntechnologies.com/), please contact me on
[Twitter](https://twitter.com/chrisdownard),
[Google+](https://plus.google.com/+ChristopherDownard/), or at my
[website](http://bluesuntechnologies.com/contact/).
