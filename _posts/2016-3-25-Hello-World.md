---
layout: post
title: Creating a blog using Jekyll and GitHub pages is super easy!
---

<a target="blank" href="https://www.github.com" > GitHub </a> is really sweet. Using Github Pages you can deploy a blog for free exremely quickly and easily and best of all you do not need to use the command line (unless you want to) or have any previous HTML/CSS/JS experience (having some wont hurt).

To get a blog up and running there are a few simple steps you need to follow:

<h3> 1.) Create a Github Account </h3>
Create a free account on <a href="https://www.github.com" > GitHub</a>. 

<h3> 2.) Find a Jekyll theme that you like </h3>

If you like what you see you can create a blog using this exact theme which can be found
<a href="https://github.com/barryclark/jekyll-now " > here</a>.

  Once you have found a theme you will 'fork' a starting point. Click the 'Fork' button in the top right corner.
<!-- <div style="text-align:center"> -->
<!-- <img src= ({{ site.baseurl }} "/images/SS1.png)" /> -->
<!-- ![screen-shot](/images/SS1.png) -->

![screen-shot]({{ site.url }}/images/SS1.png)
<!-- </div> -->

<h3> 3.) Host on GitHub </h3>
Click the 'settings' button on your forked repo and change the name to 
<code> yourusername.github.io </code>

<h3> 4.) Visit  <code> yourusername.github.io </code> in your favorite browser </h3>
At this point if you have followed the steps above, you should see the your blog live. To customize the settings and content of your blog you will edit and update the variables located in <code> _config.yml </code> and then commit said changes.



<h3> 5.) Create your first blog post! </h3>
To make edits and create new posts simply open the <code> _posts </code> folder
<!-- <div style="text-align:center">
<img src="/images/SS2.png" />
</div> -->
![screen-shot]({{ site.url }}/images/SS2.png)

click <code> 2016-3-25-Hello-World.md </code> to view the example post so that you can get started. Please not that you must replicate the formatting in the title of the .md file (year-month-day-post-name.md) <br><br>


*Please note for those with dev experience you can run your jekyll blog locally by running<br> 
<div style="text-align:left">
<code> gem install jekyll </code> <br>
<code> gem install github-pages </code><br> (this one will keep your local environment in sync with the gems used on GitHub Pages)
<code> jekyll serve --watch </code><br>
(which will poll for changes)<br>
and then visiting <code> http://0.0.0.0:4000 </code><br><br>
</div>