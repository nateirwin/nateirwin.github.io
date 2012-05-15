---
layout: 'post'
title: Google imposing more restrictions on Google Maps API
---

Google [continues the trend](http://googlegeodevelopers.blogspot.com/2012/04/update-to-google-maps-api-deprecation.html) of tightening down the Google Maps API terms of service. From section 10.1.1.g of the updated [Google Maps/Google Earth APIs Terms of Service](https://developers.google.com/maps/terms):

<blockquote><p>No Use of Content without a Google Map. You must not use or display the Content without a corresponding Google map, unless you are explicitly permitted to do so in the Maps APIs Documentation, or through written permission from Google. In any event, you must not use or display the Content on or in conjunction with a non-Google map. For example, you must not use geocodes obtained through the Service in conjunction with a non-Google map. As another example, you must not display Street View imagery alongside a non-Google map, but you may display Street View imagery without a corresponding Google map because the Maps APIs Documentation explicitly permits you to do so.</p></blockquote>

And from section 10.2.a:

<blockquote><p>No "Wrapping." You must not create or offer a "wrapper" for the Service, unless you obtain Google's written consent to do so. For example, you are not permitted to: (i) use or provide any part of the Service or Content (such as map imagery, geocoding, directions, places, or terrain data) in an API that you offer to others; or (ii) create a Maps API Implementation that reimplements or duplicates Google Maps/Google Earth. For clarity, you are not "re-implementing or duplicating" Google Maps/Google Earth if your Maps API Implementation provides substantial additional features or content beyond Google Maps/Google Earth, and those additional features or content constitute the primary defining characteristic of your Maps API Implementation.</p></blockquote>

I have to say I'm confused as to why Google is moving in this direction. I understand their desire to move their APIs into the enterprise space, but why do this now when OpenStreetMap is getting so much publicity and the number of viable (and much cheaper) alternatives to Google Maps is growing? It seems like Google would be working to bring in new customers, not push them away by imposing new restrictive limitations.

I also don't understand why they would ever want to impose these two specific constraints. If a company is paying Google to use their geocoding and routing services, why not let them use these services however they please? And how does "wrapping" functionality around the Google Maps API hurt Google's business model?

It seems that the days of Google Maps being the defacto web mapping platform are gone. If the terms of service don't allow me to be creative when using Google's APIs, I'm not going to use them.