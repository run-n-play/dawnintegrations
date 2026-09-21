---
layout: post
title: "The 4-axis gantry, and the control behind it"
date: 2026-09-21 09:00:00 -0400
tags: [linuxcnc, cnc, retrofit]
excerpt: "A look at the shop's 4-axis gantry router — the QtDragon control screen and the cabinet wiring that drives it."
---

The workhorse in the shop is a 4-axis gantry router running LinuxCNC. Here's the control side of it — the screen I drive it from and the cabinet that makes it all move.

![QtDragon HD control screen showing the tool table and DRO](/assets/images/linuxcnc/qtdragon-tool-table.jpg)

*The QtDragon HD interface. The tool table on top holds everything from a 3/8" endmill down to the PGFUN touch probe (tool 11); the DRO at the bottom shows X, Y, Z and the A rotary — the fourth axis.*

<FILL: a sentence or two on what you like about QtDragon, or what you changed to get here.>

## Under the hood

![Control cabinet — Field I/O board and terminal blocks](/assets/images/linuxcnc/control-cabinet-01.jpg)

*<FILL: what board this is and what it replaced — e.g. the original control vs. the LinuxCNC retrofit.>*

![Field I/O wiring detail](/assets/images/linuxcnc/control-cabinet-02.jpg)

*<FILL: what's landing on these terminals — limits, home switches, spindle, etc.>*

![Analog spindle interface and I/O](/assets/images/linuxcnc/control-cabinet-03.jpg)

*<FILL: the analog spindle interface / anything worth calling out here.>*

## What's next

<FILL: what you're working on with this machine right now — ATC, probing routine, tool offsets, whatever's current.>
