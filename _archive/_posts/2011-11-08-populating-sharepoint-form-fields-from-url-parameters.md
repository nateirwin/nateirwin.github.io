--- 
layout: post
tags: 
  - Development
title: Populating SharePoint form fields from URL parameters
---

I occasionally get asked to do a bit of SharePoint hackery for my company, so it didn't come as a surprise when I was asked last week if it was possible to populate fields in a SharePoint form with parameters passed in via the form URL. My answer, as always: "Anything is possible!" And, of course, it is possible, but it isn't quite as straight-forward as just writing a snippet of JavaScript.

Main lesson learned: Use Internet Explorer when trying to do anything with SharePoint. We are running the latest version of SharePoint, MOSS 2010, and it is amazing to me that Microsoft can still get away with releasing a product that only runs properly in Internet Explorer. When are companies going to demand more?

Now that that's out of my system: After figuring out that I had to use Internet Explorer, completing this task really was as easy as writing a few lines of JavaScript.

Here are the exact steps taken:

1. Navigate to the URL of the form that you want to hook the auto population up to ("NewForm.aspx" in most cases).
2. Insert a "ContentWebEditor" web part into the page.
3. Click within the "ContentWebEditor" web part and click on "Edit HTML Source" under the "Editing Tools &gt; Format Text &gt; HTML" menu item.
4. Copy and paste the following snippet into your page. Note: I'm using jQuery here, as we use it in pretty much all of our products. You can very easily do this without the jQuery dependency.

    &lt;script type="text/javascript" src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.6.4.min.js"&gt;&lt;/script&gt;
    &lt;script type="text/javascript"&gt;
      $(document).ready(function() {
        var query = window.location.search.replace('?', '').split('&amp;');

        for (var i = 0; i &lt; query.length; i++) {
          var p = query[i].split('=');
          
          $('input[title="' + p[0] + '"]').val(p[1]);
        }
      });
    &lt;/script&gt;

This script loads jQuery (if you already have it loaded into your web page, you obviously don't need to load it again here), grabs the query parameters from the URL, iterates through them, looking for HTML inputs with the exact same title as the parameter name, and sets the value of a matched input to the value of the parameter.

So, if I had a form located at `http://mysharepointsite/Lists/DataAction/NewForm.aspx`, I could pass parameters in like this: `http://mysharepointsite/Lists/DataAction/NewForm.aspx?Parameter1=Test1&amp;Parameter2=Test2`. The JavaScript would iterate through the parameters, and set the value of inputs with a title of "Parameter1" or "Parameter2" with the appropriate values.