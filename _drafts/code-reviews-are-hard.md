---
layout: default
title: Code reviews are hard.
type: post
category: iplayer
summary: Why is it hard to encourage the practice of code reviewing and how has Github helped?
author: Rich Middleditch
---

<center>![](http://www.jasonawesome.com/wp-content/uploads/2010/06/sally-code-review.png)</center>

## Problem
Last year the iPlayer web team were using SVN for version control. Code was developed and commited to trunk and if you were very lucky a code review would take place. Typically this would be a face to face meeting of the larger commits after they already made it into trunk. The team would often repeat the "more code reviews!" mantra after a breaking change made it into the codebase, yet it proved almost impossible to instil the habit. For a handful of reasons:

1.  No time set aside to review another persons code
2.  No checkpoints for code before making it to trunk
3.  Knowledge silo's increasing the time a review takes

But most importantly code reviews were hard because **we had no tools**.

## Solution
Github. We switched to git+github in August of 2013 and havent looked back. The single biggest impact on the team has been the improvement to code reviews. Our github code review flow works like this:

1.  Code is edited in a branch on the developers fork of the project
2.  At a natural break a pull request is created for the branch back to the source repository
3.  Everyone code reviews - developers, testers, product managers
4.  When the code has recieved 2 thumbs up (<img src="https://github.global.ssl.fastly.net/images/icons/emoji/%2B1.png" width="20" />) from the team a user with pull rights will merge the code

This system allows code reviews to emerge throughout the day as time allows, instead of blocking out chunks of time in which people must context switch out of what they are doing and into someone elses work.

As only the lead developers and lead testers have pull rights it also means that a checkpoint is created preventing your work from making it into the codebase until a review has taken place.

All code that makes it into the codebase is now reviewed. This means that the entire team can see changes across a large codebase. They can ask questions about areas that confuse them. They can direct others to code which already accomplishes their goals. They can get exposure to languages and tools they wouldnt normally interact with.

## Validation
From a handful of code reviews each sprint we have gone to reviewing every single change that is made to the codebase.

Last month (January 2014) the team made 734 commits across 327 pull requests. Each one reviewed and approved by at least 2 other people.

The github pulse dashboard speaks for itself:

![](/assets/code-reviews-are-hard1.png)

## Patterns
It was hard to understand why code reviews are such a hard habit for the team to pick up. Clearly code reviews are a good thing yet we couldnt get into the flow of actually performing the review.

Previous suggestions to solve this included emailing diff patches around, using online diffing tools, or just doorstepping people. However these are patches that just work around the real reason why we could never pick up the habit - there was no home in our development process for a code review to live.

By stepping back and thinking about how we could streamline our whole development process we've been able to make a code review a clear, measurable step in our workflow. Introducing another tool for code reviews would not have succeeded as it is tool without a home.

The key has been to use **the right tool in the right place.**
