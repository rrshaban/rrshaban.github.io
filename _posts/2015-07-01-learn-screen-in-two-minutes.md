---
layout: post
title: "Screen in two minutes"
date: 2015-07-01 02:58:15
categories: tutorial
---

I wrote up a quick how-to that I wished I had found when I was first learning screen, instead of having to navigate the [vaguely terrifying documentation](http://linux.die.net/man/1/screen) ("Each virtual terminal provides the functions of a DEC VT100 terminal and, in addition, several control functions from the ISO 6429 (ECMA 48, ANSI X3.64) and ISO 2022 standards (e.g. insert/delete line and support for multiple character sets)").

You can find my tutorial below or [on my Github](https://github.com/rrshaban/screen_tutorial).

---

`screen` is a super-useful Unix utility because it allows you to run terminal commands without needing to have your terminal window open. 

Think of a screen as a session: you can open a screen, start a script, and then detach from it. The script will keep running in the background, but you can keep doing whatever you were doing without affecting the script. More significantly, if you want to be able to step away from your terminal, or close your laptop, or let a task run overnight without needing you to be connected, use a screen. 

This quick tutorial will walk you through the basic commands necessary to get a screen working without worrying about what's going on behind the scenes.


### Start a screen session

>`$ screen -S <NAME>`

### Run whatever code you want

>`$ ruby download_the_entire_internet.rb`

This will run inside the screen, so you can freely switch out of the screen if you want.

### Switch out of the screen

`Ctrl-a d` (hold Ctrl+a and click d)

This won't affect anything running in the screen. 

### See what screens you currently have open

>`$ screen -ls`

Like `ls` in a directory, but for screens! Cool!

### Switch into a screen

>`$ screen -Dr <NAME>`

This will now bring your terminal window into a specific screen. 

### Close a screen 
`$ exit` from within the screen, or if you want to do it from your regular interface, you can run 
>`$ screen -X -S <NAME> quit`

### ???

### Profit!

If you're curious about what more you can do with screen, check out a [helpful guide](http://www.pixelbeat.org/lkdb/screen.html) or (if you're brave) [the documentation](http://linux.die.net/man/1/screen). 