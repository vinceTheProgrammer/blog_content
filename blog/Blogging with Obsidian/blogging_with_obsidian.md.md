+++
date = "2026-08-30"
title = "Blogging with Obsidian"
description = "I've chained together a few different utilities to give myself a very comfy way to blog."
authors = ["vinceTheProgrammer"]
[taxonomies]
tags = ["obsidian"]
[extra]
math = true
diagram = true
image = "banner.webp"
+++

## The Problem
I tend to barf out all my ongoing shenanigans into the Stick Nodes beta testing Discord server, but I'm starting to wonder whether the others there are getting a little bit tired of it 😅.

## The Solution
I combined:
- Zola: static site generation
- Zolarwind: Zola theme
- GitHub Actions: builds the Zola site
- Obsidian: comfy markdown editor

Which gave a me very nice way to write blog posts:
{{<image
  page={page}
  src="screenshot.png"
  dark_src="screenshot.png"
  alt="Screenshot of Obsidian mobile app"
/>}}

