---
layout: post
title: Markdown Lessons Learned
---
> Note that this will be my last post on Markdown.  It's time 
to move on to something else.  

Ok, so I noticed some odd layout in my previous posts.
Some of the text that i entered was not wrapping
properly on different size devices.  It was as if
it didn't auto wrap.  As I'm typing this, I'm entering
new lines to keep the text that I'm entering from 
scrolling off of the editor window.  But when it 
is rendered, i'm expexting that it will all flow 
correctly to show the text as a single formatted 
paragraph.  The problem is that it wasn't doing
that on my previous post.  

In my research, I found the following article
[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

It describes behavior of word wrapping.  It turns out
that if you put in two **trailing** spaces at the end
of a line then the markdown will force a hard line
break.  When I went back to my previous posts I saw 
that I had done just that in a couple of places!  

So I removed the extra spaces and Voila!!  Sure enough 
everything is working great again.  

Regards,  
--Dave.