--- 
layout: post
meta: 
  title_url: http://developmentseed.org/blog/2011/oct/26/tilemill-060-released/
tags: 
  - Cartography
  - Design
  - Web Mapping
title: "TileMill 0.6.0 released"
---

The stuff I'm most excited about:

- Sqlite improvements - We are now using Sqlite in place of shapefiles in some of our TileMill projects. Why? Shapefiles have restrictions on field length, etc. Sqlite files don't.
- OS X desktop app - I already ran TileMill using the Google Chrome "Canary" build, but this will allow me to run it in a completely separate process.
- Better projection detection - This wasn't necessarily a major complaint before, but it will make things a bit easier.

Overall I've been really impressed with the TileMill release cycle. The last few releases, in particular, have fixed most of the major issues that prevented us from being productive in the past. In particular, we can now build out complex tilesets much faster than we could with the early 0.5.x releases. In fact, tilesets that were too complex for TileMill to handle in early 0.5.x versions are now handled quite easily.

(via [Development Seed](http://developmentseed.org/blog/2011/oct/26/tilemill-060-released/))