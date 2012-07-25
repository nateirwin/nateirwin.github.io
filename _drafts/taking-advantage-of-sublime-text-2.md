---
layout: post
title: Taking advantage of Sublime Text 2
---

I'm in love with [Sublime Text 2](http://www.sublimetext.com/). I'm a longtime TextMate user, but I now use Sublime Text 2 for everything I do. It has even replaced another longtime favorite, Espresso.

## Install Sublime Package Control

1. Press <code>Ctrl `</code> to open the Sublime Text 2 console
2. Paste the following into the console and hit enter

<pre>
  import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print 'Please restart Sublime Text to finish installation'
</pre>

3. Restart Sublime Text 2

## Install SublimeLinter

1. https://github.com/SublimeLinter/SublimeLinter
2. Install Node.js

## LiveReload

http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions-

or desktop app
