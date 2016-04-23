---
layout: post
title: Creating a blog using Jekyll and GitHub pages is super easy!
---

<a target="blank" href="https://www.github.com" > GitHub </a> is really sweet. Using Github Pages you can deploy a blog for free exremely quickly and easily and best of all you do not need to use the command line (unless you want to) or have any previous HTML/CSS/JS experience (having some wont hurt).

Jekyll is a powerful <a target="blank" href="https://www.smashingmagazine.com/2015/11/modern-static-website-generators-next-big-thing/
" >static site generator</a> that can be set up very quickly. It can be leveraged for a number of content management solutions however in this guide I will walk you through setting up a basic blog such as this one.


I will outline instructions for both devs, and those with absolutely no experience, that explain how to get a blog up and running in a matter of minutes.


<h2> For those with no web development experience: </h2>
To get a blog up and running there are a few simple steps you need to follow:

<h4> 1.) Create a Github Account </h4>
Create a free account on <a href="https://www.github.com" > GitHub</a>. 

<h4> 2.) Find a Jekyll theme that you like </h4>

If you like what you see you can create a blog using this exact theme which can be found
<a target="blank" href="https://github.com/barryclark/jekyll-now " > here</a>.

Hundreds of options can be found at
<a target="blank" href="http://jekyllthemes.org/" >jekyllthemes.org/</a>.

  Once you have found a theme you will 'fork' a starting point. Click the 'Fork' button in the top right corner.
<!-- <div style="text-align:center"> -->
<!-- <img src= ({{ site.baseurl }} "/images/SS1.png)" /> -->
<!-- ![screen-shot](/images/SS1.png) -->

![screen-shot]({{ site.url }}/images/SS1.png) 

<h4> 3.) Host on GitHub </h4>
Click the 'settings' button on your forked repo and change the name to 
<code> yourusername.github.io </code>

<h4> 4.) Visit  <code> yourusername.github.io </code> in your favorite browser </h4>
At this point if you have followed the steps above, you should see the your blog live. To customize the settings and content of your blog you will edit and update the variables located in <code> _config.yml </code> and then commit said changes.



<h4> 5.) Create your first blog post! </h4>
To make edits and create new posts simply open the <code> _posts </code> folder
<br>
<br>
![screen-shot]({{ site.url }}/images/SS2.png)

click <code> 2016-3-25-Hello-World.md </code> to view the example post so that you can get started. Please not that you must replicate the formatting in the title of the .md file (year-month-day-post-name.md) <br><br>


<h2> For Developers: </h2>

You will absolutely love working with Jekyll as a CMS. Please not that it is required to have Ruby installed so that you can run the command <code> gem install </code>

<h4>
1.) Install Jekyll on your machine.
</h4>
<code>gem install jekyll</code>

<h4> 
2.) Start from scratch OR find a theme you like. </h4> Hundreds of options can be found at
<a target="blank" href="http://jekyllthemes.org/" >jekyllthemes.org/</a>. If you want to start completely fresh run <code>jekyll new myAwesomeBlog</code> then <code>cd myAwesomeBlog</code> and <code>jekyll serve</code>

This last command will start a local web server and allow you to preview all changes.

<h4>3.) Create your first post and customize  </h4>
Your blogs settings live inside <code>_config.yml</code> Edit these to get started.

Find the folder _posts within your jekyll project and create a new file. Follow the file name formatting of the default post but change it to todays date. Using markdown create new blog posts with ease!

<h4>4.) Create a github respository with the name <code>yourusername.github.io</code></h4>

Your project will now be live for the universe to see!

You will now be able to visit your blog at yourusername.github.io in any browser.