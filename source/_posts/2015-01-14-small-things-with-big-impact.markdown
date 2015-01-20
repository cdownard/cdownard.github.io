---
layout: post
title: "Small Change, Big Impact: Planning for evolving requirements"
date: 2015-01-14 09:00:00 -0700
comments: true
categories: ruby rails OOD programming code development
published: false
---

The needs of an application change overtime. As a result, it can be difficult to
perfectly design your application in the beginning. But there are certain
decisions you should make early to prevent time sinks when the inevitable
changes come. This post will discuss one such example - driving application
logic through a central location. To do so as succinctly and plainly as
possible, we will begin by demonstrating the problem in infancy and then follow
it up with a requirements change. Finally, we will show a refactoring and the
cascading changes required to make the change.
<!--more-->
##In the beginning##
In programming there's an acronym that many refer to with the best of intentions
but is misused by those who aren't sure of what they're doing: YAGNI (You Ain't
Gonna Need It). YAGNI is the response used when someone sets out to design a
solution to a problem and drills down to the 1% or 0.1% edge cases. They labor
over trying to find the most perfect solution to a problem you might not
encounter. The problem is that you sometimes run across people who have decided
the acronym is some sort of excuse to not think about most problems.

{% blockquote %}
YAGNI is not an excuse to ignore design decisions.
{% endblockquote %}

I have witnessed veteran developers shutting down younger developers
exploring the merits of a potential future need because "it just wasn't likely."
But six months later the code base had to be refactored to handle just that. In
one case, it actually became the dominant use case. The lesson here is that you
can't know the future of your application. It's your job to try to build the most
flexible structure you can without going overboard. You won't always be able to
identify and clearly delineate that distinction; but it is something that you can
learn over time.

{% blockquote %}
It's your job to try to build the most flexible structure you can without going
overboard.
{% endblockquote %}

When you begin work on a codebase with milestones and/or timelined deliverables,
you sometimes find yourself making small compromises for the benefit of
immediate results.

###The Example###
We have an Employee model which covers a few basic attributes such as name,
birth date, gender, and status. The status is going to be the focus of this
exericse. What the application supports isn't terribly relevant to our thought
exercise - perhaps it is employee onboarding, payroll, time clock, or an
application to generate an organizational chart.

```
Employee
  - first_name
  - last_name
  - birth_date
  - gender
  - status
```

The status will simply be a marker to indicate whether an employee is active or
inactive (not working for the company). This is a common use case for HR facing
applications and specifically it's common for data going from those HR platforms
and into payroll systems.
