---
layout: post
title: ESLint, React and ES6
---

In this post I will explain how to leverage ESlint to help you write better javscript.

Linting might not be sexy but it's important. Without it our code ends up riddled with white space, missing semi-colons, and various styling inconsistencies. 

It is 100% worth taking the time to set up linting configuration so that your text editor can work for you. At the company I work for we adhere to the <a target="blank" href="https://github.com/airbnb/javascript" > airbnb javascript style guide</a> but have set a few custom settings.

ESlint can be installed globally or as a project's dependency.
<pre>
	npm install eslint --save-dev
</pre>

As a project's dependency ESLint will be default look for a config file at 
<code> 
.eslintrc 
</code> 

To install globally (make ESLint available across projects)
<pre>
	npm install -g eslint
</pre>

By default ESLint will look locally for a config file. The next step looks the same from the command line run:

<pre> 	eslint --init </pre>

This will walk you through some options for configuring ESLint and what kind of javascript you will be writing.

After that you will be good to go and can run ESLint from the command line or in your favorite text editor!