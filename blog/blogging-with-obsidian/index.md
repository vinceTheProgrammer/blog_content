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
image = "obsidian.webp"
+++

## The Problem
I tend to barf out all my ongoing shenanigans into the Stick Nodes beta testing Discord server, but I'm starting to wonder whether the others there are getting a little bit tired of it 😅.

## The Solution
I combined:
- Zola: static site generation
- Zolarwind: Zola theme
- GitHub Actions: builds the Zola site
- Obsidian: comfy markdown editor
- GitSync: Android app for easy syncing between a remote git repo and a local folder

Which gave a me very nice way to write blog posts:
{{<image
  page={page}
  src="screenshot.png"
  dark_src="screenshot.png"
  alt="Screenshot of Obsidian mobile app"
/>}}

Then once I'm done, I just close Obsidian and click GitSync's sync widget and wait for the site to update with my changes.

The full flow looks like:
1. Sync to GitHub [blog_content](https://github.com/vinceTheProgrammer/blog_content) repo
2. `blog_content` repo GitHub action dispatches an event to my [vincetheprogrammer.github.io](https://github.com/vinceTheProgrammer/vincetheprogrammer.github.io) repo
3. `vincetheprogrammer.github.io` repo GitHub action rebuilds and publishes using a fresh checkout of the latest `blog_content`repo
4. It's live!
