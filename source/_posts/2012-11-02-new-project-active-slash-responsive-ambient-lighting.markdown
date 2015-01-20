---
layout: post
title: "New Project - Active/Responsive Ambient Lighting"
date: 2012-11-02 09:00:00 -0700
comments: true
categories: python project ambeint fun programming code video
---
So, while browsing the wonderful web one day recently a friend of mine,
[Clint Shuman](https://plus.google.com/109744469121910551000/posts), sent me a 
link to an RGB LED grid that acted as a 
[responsive ambient light for a TV](http://www.youtube.com/watch?v=AP2fJgS-b8g). 
Awesome right? I love stuff like this. It's simple, but it really adds an 
interesting touch to movie night. Naturally, we immediately set out to program 
our own version.
<!--more-->
The concept of active ambience is pretty interesting. The fire in that Avatar
video link really enhances the feeling of having that torch flipped around. I
definitely like that but there are a few limitations to this implementation of
ambipi.

First, it is Windows only. Although Windows is a perfectly pervasive and
acceptable OS, it is not the only one - nor is it frequently the choice of my
media enthusiasts. A home theater build using Linux is often a less expensive
and adaptable solution. Further, the limitation of using XBMC that is specially
compiled for this feature limits the playing pool to a release cycle based on
this feature. One can't simply update to the latest and greatest XBMC the
whenever they please (ambipi extensions, not boblight for those thinking of it).

Which leads to the main hurdle: what about active ambience for other uses of
the machine? VLC? Video conferencing? And the list continues. I want a solution
that works with the display output and not only one application (although it has
plenty of extensions). Adalight and others certainly have achieved this, but I
would like to solve the problem in python and make it as cross platform/device
as possible with additional configuration. Ultimately, how nifty would this type
of thing be on displays, at trade shows, etc? Pretty eye catching.

So enter python and some good fun playing with websockets to test the results. I
don't have any LEDs to plug into my [Raspberry Pi](http://raspberrypi.org), so 
Clint and I setup a cherrypy server with a websocket to communicate back to the 
server. The webpage has a configurable grid of squares. Although we started with 
a 3x2 grid, we have moved on to a 5x3 as we feel it'll produce a better ambience. 
The test with 8x8 went well but for now I just want to focus on getting a basic 
setup working flawlessly. Originally we made a full grid with all pieces of the 
screen updating (that is, all 15 boxes in a 5x3) but then decided to do a 
perimeter only since we won't have LEDs in the center behind the display. A 
perimeter of boxes on a 5x3 results in a 12-count. The grid generation algorithm 
was changed to simply build a full row if it was the first or last row and since 
the algorithm is only run once, there's no performance hit.

At first, we were at about 8 fps using screencaptures for each individual grid.
This is super slow (200-300 millisecond response time based on grid size). So we
changed the algorithm to capture the screen once and then resize it before
sending it off to be analyzed by bounding box. This significantly improved
performance and currently we're around 15-20 fps depending on how tempermental my
CPU is feeling. Oddly my computer at work runs at about 45 ms pretty consistently
while at home I'm more consistently in the 80-100 ms range. I still haven't
figured out why that is, but I did just upgrade to Windows 8 so maybe there are
some issues I haven't found yet relating to that (work is Windows XP).

Ultimately, I'd like to move to the win32api and see if I can get any improvement
over the Python Imaging Library (PIL). For linux, we currently have GTK being
used. It's possible we'll go to native C and use X to grab the window if needed,
but we'll need to run some tests. GTK is staying pretty consistent with where PIL
is (45 ms). I thought GTK would be far faster, but perhaps there's room for
improvement with the algorithm.

The current plan (for me, Clint will use an Arduino) is to have my computer
serving the image data over UDP to a Raspberry pi. Alternatively, could leave the
Pi plugged in but that does involve the limitation of putting the computer next
to the pi and therefore next to the tv. I don't currently have any spare
computers lying around so a network method is preferable.
