---
layout: post
title: "From Blender to the CNC: cut lists out of Home Builder, and the VCarve gadgets level up"
date: 2026-10-28 15:30:00 -0400
tags: [blender, home-builder, vcarve, cnc, cabinetry, gadgets]
excerpt: "Design a kitchen in Blender, push one button, get a shop cut list — and hand the parts straight to VCarve to nest and cut. Plus a round of upgrades to Door Nest and Cabinet Nest."
---

Last post I mentioned two things on the bench: cut lists out of Blender, and a round of VCarve gadget updates. Here's where they stand. Shop-test results and photos will follow in a later post.

## The problem: great design software, no shop paperwork

I wanted a real cabinet CAD — not just the box, but the whole room: walls, kitchens, fireplace mantels, bookcases. Fusion's cabinet add-ons fell short. So instead of writing one from scratch, I went looking for something good to build on.

That turned out to be **Home Builder 5**, a Blender add-on by **Andrew Peel**. It lays out rooms and builds every cabinet part to the style you pick — sides, backs, stretchers, face frames, shelves, doors, drawer boxes, notches and rabbets included.

What it didn't give me was the paperwork a shop runs on. So I built a companion.

## Dawn Millwork: the cut list add-on

**Dawn Millwork** sits alongside Home Builder — it doesn't change Home Builder's code, it just reads what Home Builder builds. Place a sink base or a pantry, change the style or the width, and the cut list follows.

One export gives you:

- A **printable cut list** with checkboxes, parts grouped by cabinet and stock type, a materials summary, and sheet estimates
- A **cut list CSV** for Excel, in fractions and decimal inches
- A **door and drawer-front list** with finished sizes and door style — ready to feed straight into Door Nest
- A **JSON file** with everything, for Cabinet Nest

The shop rules are mine, set once: material and edge banding per stock class, doors as finished sizes or broken into stiles/rails/panels, joinery (dado, rabbet, dowel, pocket screw, biscuit, mortise-and-tenon), and drawer boxes sized from the real cabinet openings using my standards.

Before it ever touched my shop, it got checked against Home Builder itself: all **70** face-frame products placed, and every one of **831** parts matched the 3D model's dimensions.

### Export to VCarve

This is the part I'm proudest of. Dawn Millwork doesn't try to nest — **VCarve Pro does that better**. Instead it exports the parts by material, and a small VCarve gadget, **Dawn Millwork Open Job**, opens a new job at the right sheet size and my measured material thickness and pulls the parts right in.

Design in Blender → one click → parts in VCarve, ready to nest and toolpath.

### Print Jobs

And for the customer and the shop floor: a **Mozaik-style job packet** — plan and elevation drawings, per-cabinet assembly sheets, face-frame sheets, door reports, drawer-box and hardware reports, and a priced quote — all with my company name and logo on it.

## The VCarve gadgets level up

What's been going into them:

- **Cabinet Nest** got a faster wizard (trimmed down to a handful of pages), separate base and upper cabinet entry, face-frame options for how the top and bottom sit, separate shelf-pin spacing for uppers, shelf-specific thickness so 3/4" shelves nest on their own sheets, and an optional solid-wood shelf nosing that shows up on the cut list.
- **Door Nest** builds doors around real **Amana** cutter geometry pulled from the tool database, so every vector sits exactly where the bit's center needs to be.
- **Next up: drawer boxes** — dovetail, butt, or dado corners; flush, raised-dado, or rabbeted bottoms; any bottom thickness.

## What's next

- **Shop testing** — real cuts, and a full write-up with photos of what broke and what got fixed
- **Drawer box gadget**
- **Frameless and closet** cabinets
- **Hinge and shelf-pin boring**
- **Sharing the gadgets** with other VCarve users

---

*Home Builder 5 is by [Andrew Peel](https://creativedesigner3d.com/) and is GPL-3.0. Dawn Millwork is a companion add-on and doesn't modify Home Builder.*
