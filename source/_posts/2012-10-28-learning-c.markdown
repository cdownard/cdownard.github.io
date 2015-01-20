---
layout: post
title: "Learning C"
date: 2012-10-28 09:00:00 -0700
comments: true
categories: learning school programming C
---
I don't have years of programming experience. The time that I devote to learning languages tends to be allocated to Python or something work related (.Net). However, I'm currently enrolled in a course focused on introductory C. At times I feel as though I have stepped into a time machine.
<!--more-->
I used to play this video game and the people who were really obsessed maxed all their stats as much as they could. There were intense calculations that could be done. People could spend hours figuring out the best way to spellcraft their armor or weapons so that every possible point or stat could be claimed. More hours would be spent "farming" locations for "drops" to create the perfect armor set. It sounds like a complete waste of time, and maybe it was, but it was certainly fun. I was one of those obsessed people that did everything they could to maximize their "utility."

C reminds me of this mindset. I can completely see how people who are obsessed with performance or being in control of as many aspects of a program as possible would love C. You get to control almost everything so you get to optimize almost everything. You manage your memory. You fine tune everything. No doubt C is fast, but for once in my life I find myself enjoying the automatic management I get from lots of other, higher-level languages. Obtaining input in C presents a good example:

```C
#include <stdio.h>

void main ()
{
    int inputChoice;
    do {
        printf("Please make a selection from the choices (1-4): ");
        scanf("%d*[\n]");
        if (inputChoice < 1 || inputChoice > 4) {
            printf("Error - you have entered an invalid choice.");
        }
} (while inputChoice < 1 || inputChoice > 4);}
```


This is how we collect input in C. We have to protect ourselves, and an easy way for a beginner like myself in C to protect against bad data is to use a do loop. Oh, that section with `*[\n]`? Yeah. That prevents the system from trying to store the newline character (`\n`). Yep. You have to handle that.

The thing is, I completely understand how awesome this must have been for a long time. But now it's just not necessary to me to spend a lot of time doing all this when I can literally do it in one line of code in another language. Take python for example:

```python
inputChoice = input('Please make a selection')
```

I'm cheating because there's no error handling. But we can add that with a couple of lines admittedly. The point isn't so much the length. It's having to handle things like the newline character. You also can't test data types in C. 
