---
published: true
layout: post
title: 'I''ve been busy setting up a blog '
date: '2022-03-27 22:06:07 +0300'
categories: blog
---
## Because simply infodumping on Medium ain't fun

Hi, I'm Utku, an internet person located in Istanbul, Turkey.
And lately, I've been contemplating different places to do blogging on. Then my mind went, "why not build it yourself while you're at it, your prospective employers might like it!" and here we are. 
I locked down on GitHub Pages using Ruby and [Jekyll](https://jekyllrb.com/). The idea was planted in my head after hearing about it in one of Jack Rhysider's [Darknet Diaries](https://darknetdiaries.com/) episodes explaining how and why he uses Jekyll.

### The issue with themes
Right off the bat, It's been quite challenging to get it working on my preferred theme, [Dinky](https://github.com/pages-themes/dinky). So we're stuck with the default theme [Minima](https://github.com/jekyll/minima),for now.

I seriously thought it would be a simple process given that Jekyll is created by one of GitHub's co-founders and former-CEO, [Tom Preston-Werner](https://github.com/mojombo). ¯\_(ツ)_/¯

And there's even an option in your repository settings that promises to change your theme with a few clicks, but I couldn't get it to work. I will feel immeasurably dumb if it just decides to work one day... anyway, moving on. 

## The issues I ran into with Ruby 
### Ruby does not like having spaces in its insallation path
Yup, nice and simple, my installer of choice, [RubyInstaller for Windows](https://rubyinstaller.org/) actually defaults to a space-free path "C:\Ruby31-x64" but I put a space before x64 for no reason at all during my initial installation, making it "C:\Ruby31 x64". Thankfully, [people in this post](https://github.com/jekyll/jekyll/issues/8523) knew what was going on. A clean installation of Ruby, Jekyll, and its gems solved this issue (and I later opted to do it in Linux anyway).

### Ruby does not like UTF-8
I got my current computer second-hand, it was configured by an IT guy at a publishing company in Istanbul. I immediately wanted to do a clean installation but due to the deadlines I was working with at the time, I postponed the whole ordeal indefinitely. I just changed the OS language to English kept using it after ensuring that it was not up to anything sketchy. But, there was one critical aspect aside from the weird Turkilish event logs: The %user% path.

The PC came with the the path to %user% as "MONSTER-GAMİNG". You see where this is going? Yes the big sore "İ", some programs did not like it.
Apart from "İ" the same would also apply to "ı, ş, Ş ğ, Ğ, ü, Ü, ö, Ö, ç, Ç".
Thankfully, nothing I did with my computer caused a functionality breaking issue, some programs would not be able to process the path, so they opted to create their own folders, after a while I had: 
- "MONSTER-GAMNG"
- "MONSTER-GAMING"
- "MONSTER-GAMÅNG"
and so on.

Well, turns out, Ruby hates it when you have UTF-8 in your path names. It outright renders Ruby unusable on Windows, returning the following error:
{% highlight ruby %}
invalid byte sequence in UTF-8 (ArgumentError)
{% endhighlight %}

It was simply too much trouble moving my %user% path to somewhere else and doing all the registry fixes. I tried, but it broke a couple of things and I had to fall back on a system restore. 

I finally caved in and gave my computer a good ol' factory reset. Not having to worry about any UTF-8 encoding problems in the future feels damn good!

Coming up next "A cryptography writeup 2 millenia late" (ie. a test writeup)
