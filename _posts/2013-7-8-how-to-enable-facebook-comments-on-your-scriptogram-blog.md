---
layout: post
title:  "How to Enable Facebook Comments on Your Scriptogram Blog"
date:   2013-07-08 15:05:49 -0700
categories: tuts
---
I recently perused the web in search of a way to enable my readers to comment on my blog posts. Scriptogram had [this support page](http://support.scriptogr.am/discussions/suggestions/16-comments) which pointed me in the right direction, but for a n00b like myself, it wasn't the most clear and straightforward string of commenting. As a result, I decided to make this post in order to simplify the process for anyone interested.

## 1. Get the code
First, you will need to get the code from Facebook. You can do this [here](https://developers.facebook.com/docs/reference/plugins/comments/). 

<a href="http://www.flickr.com/photos/mistershmi/9243421040/" title="Screen Shot 2013-07-08 at 2.49.21 PM by MisterShmi, on Flickr"><img src="https://farm8.staticflickr.com/7318/9243421040_99f5023a14_o.png" width="237" height="296" alt="Enter the settings, the click get code"></a>

Enter your site URL, or any URL really, because we are going to replace it later. I left the width and number of posts settings at their default, but you may wish to adjust this according to your needs. Once you have done this, click "Get Code" and Facebook will generate two snippets of code that we will use.

<a href="http://www.flickr.com/photos/mistershmi/9240648477/" title="Screen Shot 2013-07-08 at 2.50.43 PM by MisterShmi, on Flickr"><img src="https://farm4.staticflickr.com/3686/9240648477_bde680b37a_z.jpg" width="640" height="406" alt="Copy and paste this code into your blog"></a>

## 2. Copy and paste the code into your blog
Go into your scriptogram dashboard and click tools, then click HTML editor.

The first code snippet is a chunk of javascript that will enable the commenting box feature on your blog. My blog already had this script right before the ending body tag under the div id "fb-root", but if it's not there you will need to add it there.

The second snippet of code is the HTML that you will need. Search your code until you have found the "{{#is_post}}" and "{{/is_post}}" tags. In between these two is where you will stick this bit of HTML. Most likely, you will see our other social sharing options as well (a "Like" button, tweet button, and a +1 button). I prefaced the code with a comment (see below) in order to recognize what it is for when I look at my code later.

<a href="http://www.flickr.com/photos/mistershmi/9240736473/" title="Screen Shot 2013-07-08 at 3.02.09 PM by MisterShmi, on Flickr"><img src="https://farm6.staticflickr.com/5443/9240736473_c0d09ea762_z.jpg" width="600" height="521" alt="This is where you stick the HTML"></a>

## 3. Enable Permalinks
Once this is done, you'll notice the HTML you just pasted will look something like this: <br />
`<div class="fb-comments" data-href="http://scriptogr.am/dhniels" data-width="470" data-num-posts="10"></div>`

What happens if you leave it like this is the comment box will remain consistent throughout the blog, meaning if someone comments on a post about cats, those comments will also show up on all your other posts about dogs or chimpanzees (or whatever it may be). What we want (well at least what I wanted) is for each post to have its own unique comments, applicable to that post only. To do this, simply replace the link under data-href to say "{{permalink}}". It will now look like this: <br />
`<div class="fb-comments" data-href="{{permalink}}" data-width="470" data-num-posts="10"></div>`

## 4. The final and most difficult step...
Click the save button!

Voila, your blog is now enabled for commenting from the 1.11 billion Facebook users out there!
