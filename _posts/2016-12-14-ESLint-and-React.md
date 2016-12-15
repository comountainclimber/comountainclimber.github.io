---
layout: post
title: ESLint, React and ES6
---

In this post I will explain how to leverage <a href="http://eslint.org/" target="blank">ESlint</a> to help you write better javscript.

Linting might not be sexy but it's important. Without it our code ends up riddled with white space, missing semi-colons, and various styling inconsistencies. 

It is 100% worth taking the time to set up linting configuration so that your text editor can work for you. On my engineering team we extend the <a target="blank" href="https://github.com/airbnb/javascript" > airbnb javascript style guide</a> but have set a few custom settings.

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

By default ESLint will look locally for a config file. However you can configure global settings as well - If eslint doesn't find a <code>.eslintrc</code> anywhere in your project, it will look for one in your home directory (<code>~/.eslintrc</code> or <code>C:\Users\username\.eslintrc</code>).

Setting up your configuration is the fun part. You can specify whether your app is leveraging es6 by the following flag in your <code>.eslintrc</code> file:
<pre>
    "env": {
        "es6": true
    }
</pre>
If you are writing JSX or React you will probably want to install additional light weight plugins - npm packages like eslint-plugin-jsx-a11y and eslint-plugin-react allow you to set rules to enforce on things common to React applications.

To enforce your configuration and fix issues from the command line run <code>eslint --fix <directory or file name> </code>

The next step is to configure eslint in your IDE or text editor... I only have experience doing this in WebStorm and Sublime 3 but for both it was fairly easy. After taking the time to set up this configuration you can truly have your text editor work for you and let eslint help you become a better developer.