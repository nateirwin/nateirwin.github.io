--- 
layout: post
meta: 
  title_url: http://mapbox.github.com/wax/
tags: 
  - Development
  - Web Mapping
title: Updated documentation for MapBox's Wax
---

<a href="http://maps.nps.gov">NPMap</a> now supports TileStream layers, and when the only layers you bring into a web map are TileStream layers, NPMap automatically uses the <a href="http://maps.nps.gov/support/modestmaps-base-api.html">Modest Maps JS baseApi</a> with <a href="http://mapbox.github.com/wax/">Wax</a>.

The integration is still a work-in-progress (hence the limited documentation), but we are close to deploying a large number of web maps for a few NPS programs using this combination of technologies. The verdict so far: For datasets that don't change often, the combination of TileStream on the server-side and Modest Maps JS/Wax on the client-side is perfect. On top of this, we've been so impressed with the speed and simplicity of Modest Maps JS that we are considering putting more time into integrating it more fully into NPMap.

Stay tuned.