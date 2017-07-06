---
layout: post
title:  "The Wii U Unbanning Process + Tools and Guide"
image: ''
date:   2017-07-05 00:06:31
tags:
- mongodb
description: ''
categories:
- Learn Jekyll 
---

<p class="music-read"><a href="spotify:track:4DAZ8UYNpWVIV46aLkN2Qp">Music for reading (spotify)</a></p>

<img src="https://raw.githubusercontent.com/backd0or/backd00r/master/assets/img/sharding-gerenciamento-usuarios/image.png">

## How, why and when.

A while back during the first days of Wii U hacking me (aqua), pirlo, electro, blue and kapu were playing around with some private hacks and stuff, and sadly we ended up getting ourselves banned off of nintendo's servers. Since then we've been trying to get ourselves unbanned, finally, after months and months of attempts, wasted consoles, pure effort and on July 7th, 2015 we succeeded! 

## The process of unbanning.

The process of unbanning was very, very, difficult it involved editing the seeprom of the console and changing a couple very very important values, including the per console keys made at factory by nintendo, the only reason we achieved this is because when the wii u sdk was leaked, nintendos cryptography keys were inside the developer firmware, and since the 3DS and WII U share keys we were able to decrypt and generate new per console keys, just like at the nintendo factories, victory! But their's stil so much to do, we'd have to actually get a iosu exploit running on the console, which me and the rest of backd00r started working on right away. And to our surprise we actually got a iosu exploit working (technical writeup on that coming soon) before any were publicly available, fearing this would enable piracy me and the rest of the team decided to keep it private and wait for a public alternative. Anyways back to the unbanning process, after achieving iosu access we set to work on a debugger client for pc (much like iosuhax) and with that used an early version of that debugger to send our code through, anndddddd failure. I'd bricked my console, *sigh*, time to get the soldering iron. And hardmod attempt #1, failure, nand wouldn't be read, reason being I modded my emmc nand, not the actual firmware nand, after modding the firmware nand I restored my console and once again began testing the groups tools. Using the developer firmware (yep, we had to get a dev Wii U for this process) the team were able to generate new per console keys, finally decrypting the seeprom putting the keys in and re-encrypting. Success.

## Automation of the tool.

Since this process was so tedious, we took a little break, make sure the method worked on every system in our possesion and then proceeded to attempt automation, after some pretty annoying mishaps we managed to get an automated python script to work through our exploit and debugger automatically pulling a set of keys from our database (still private) and writing them to the seeprom, our work was done.

### The public releases.

Ah, just when we thought we were done the public IOSU exploit came out (wiiubru), so for our final task we attempted to adapt the tool to an elevated TCPGecko client for the Wii U and a pc debugger with iosu priveledges, byebyeban.exe was born (great name ikr). It worked by running iosuhax (or any cfw) and simply running the .exe and inputting your Wii U's ip.

### TL;DR

Unbanning tool that works with iosuhax has been developed, enjoy!

### GUIDE

* Run the Wii U client provided
* Run the PC tool (AS ADMIN VERY IMPORTANT) and input your Wii U's ip
* Restart your Wii U

### Downloads

PC UNBANNER : https://ufile.io/1yacp
WII U CLIENT : 

