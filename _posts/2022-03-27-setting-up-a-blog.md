---
published: true
layout: post
title: 'Setting up a blog '
date: '2022-03-27 22:06:07 +0300'
categories: blog
---
## Launching my personal blog

Hi, I'm Utku, an internet person located in Istanbul, Turkey.
And lately, I've been contemplating different places to do blogging on. Then my mind went, "why not build it yourself while you're at it, your prospective employers would love it!" and here we are. I locked down on GitHub Pages using Ruby and [Jekyll](https://jekyllrb.com/). 

### The issue with themes
It's been quite challenging to get it working on my preferred theme, [Dinky](https://github.com/pages-themes/dinky). So we're stuck with the default theme [Minima](https://github.com/jekyll/minima) for now.

Seriously, I thought it would be simple process given that Jekyll is created by one of GitHub's co-founders and former-CEO, [Tom Preston-Werner](https://github.com/mojombo).

![I couldn't get this to work, sadly]({{site.baseurl}}/_posts/theme-chooser.png)

And there's even an option in your repository settings that promises to change your theme with a few clicks, but I couldn't get it to work. I will feel immeasurably dumb if it just decides to work one day... anyway, moving on. 

## Issues I ran into with Ruby 
### Ruby does not like UTF-8
I got my current computer second-hand, it was configured by an IT guy at a publishing company in Istanbul. I immediately wanted to do a clean installation but due to tight deadlines at the time, postponed the whole ordeal indefinitely. I just changed the OS language to English kept using it after ensuring that it was not up to anything sketchy. But, there was one critical aspect aside from the funny-yet-eerie Turkilish event logs (will provide an example below):

![turkilish-event-log.jpg]({{site.baseurl}}/_posts/turkilish-event-log.jpg)
(sooo, apparently I can't get images to work as well! will figure this out later — it probably has to do with [the markdown editor I use](https://prose.io/) and how it handles file uploads)

The PC came with the the path username "MONSTER-GAMİNG". You see where this is going? Yes the big sore "İ", some programs did not like it, _the same would also apply to "ı, ş, Ş ğ, Ğ, ü, Ü, ö, Ö, ç, Ç"_.
Thankfully, nothing I did with my computer caused a functionality breaking issue, some programs would not be able to process the path to some folders they needed so they opted to create their own folders, after a while I had: 
- "MONSTER-GAMNG"
- "MONSTER-GAMING"
- "MONSTER-GAMÅNG"
and so on.

Well, turns out, Ruby hates it when you have UTF-8 in your path names and they render Ruby unusable on Windows.  There were some 

At first, I  tried setting up a Ruby environment on Windows, It was a hassle figuring out dependencies and getting it to execute my will. When I thought I had everything sorted, I realized my CLI can't even find the path to ruby.exe. After some troubleshooting I



Coming soon "A cryptography writeup 2 millenia late" (ie. a test writeup)
