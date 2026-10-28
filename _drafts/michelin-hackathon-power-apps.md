---
layout: post
title: "We won the Michelin Hackathon with Power Apps and SharePoint"
date: 2026-10-28 09:00:00 -0400
tags: [power-apps, sharepoint, power-bi, low-code, michelin, hackathon]
excerpt: "A hackathon at the day job, a low-code toolkit, and a project-tracking app built on Power Apps and SharePoint. We won. Here's what we built and why it worked."
---

Most of what lands on this blog is built in my own shop — LinuxCNC, ESP32s, VCarve gadgets. This one came out of the day job.

Michelin held a hackathon, and our team **won** it. The app we built runs entirely on Microsoft's own stack: **Power Apps** for the front end, **SharePoint** for the data, and **Power BI** to put it all on one screen.

## The problem

On a capital project, the paperwork doesn't stop when the equipment shows up. Every project has to be tracked, accepted, and received — and a lot of that still lives in spreadsheets, emails, and forms that get filled out once and then lost in a folder.

The goal: one place to see every project, and one consistent way to walk each one through acceptance and reception.

## The build

### SharePoint as the database

No server, no SQL instance, nothing to ask IT for. The data lives in **SharePoint lists** — one for the projects, and lists behind each of the protocol screens. Everyone already has access to SharePoint, permissions come for free, and the lists are easy to edit by hand when you need to.

### The Power Apps canvas app

The app is a **Power Apps canvas app** with three main pages:

1. **Project list** — every project in one view. Pick one and everything else follows it.
2. **Ci Acceptance** — the acceptance protocol, filled out in the app instead of on a form that gets lost.
3. **General Information / Reception protocol** — the reception record for the project.

Each screen reads and writes straight to its SharePoint list, so whatever gets entered in the app is the record. No re-typing it into a spreadsheet later.

### Power BI on top

Off the same SharePoint lists, a **Power BI** dashboard presents all the projects at once — the view a manager actually wants, without anyone building a status report by hand.

## Why it worked

Low-code gets a bad reputation with people who write "real" code. But a hackathon is the exact place it shines: you have a short window, and the hard part isn't the code, it's understanding the process well enough to model it. Power Apps and SharePoint let us spend our time on the *workflow* instead of on hosting, authentication, and a database schema.

And because it's all inside the Microsoft 365 tenant everyone already uses, there's no new system to approve, deploy, or log into. That's a big deal when you want something to actually get used after the demo.

## The thread

It's the same move I make in the shop: find the repetitive, error-prone thing people do by hand, and build the tool that does it right every time. Different tools — a canvas app instead of a G-code macro — same idea.

Thanks to the team, and to Michelin for putting on the event.
