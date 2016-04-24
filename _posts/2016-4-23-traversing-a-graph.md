---
layout: post
title: Traversing JSON using recursion
---

In this post I will look at a simple use case of depth first search in JavaScript when performing logic on a graph.

Recently, I ran into the challenge of trying to perform simple string maniuplation on some JSON that had a repeated nested structure. For our purposes lets use the following as our working example which replicates the structure of the graph I was dealing with:

<pre> 
var data = {
   "name":"fruitData",
   "children":[
      {
         "name":"berries",
         "children":[
            {
               "name":"strawberry",
               "children":[

               ]
            }
         ]
      },
      {
         "name":"apples",
         "children":[
            {
               "name":"green",
               "children":[
                  {
                     "name":"fuji",
                     "children":[

                     ]
                  }
               ]
            },
            {
               "name":"red",
               "children":[
                  {
                     "name":"macintosh",
                     "children":[

                     ]
                  },
                  {
                     "name":"honeycrisp",
                     "children":[

                     ]
                  }
               ]
            }
         ]
      }
   ]
};

</pre>



Lets say that you were just notified by the marketing team that there are organic options available for every fruit you have in stock - the website needs to be updated immediately.

<h2> OPTIONS: </h2>

<h4> 1.) BRUTE FORCE </h4> We can use a series of nested <code> for </code> loops to iterate through each object. What this would look like is a bunch of (scary) code.

<pre>
function makeOrganic() {
  for (var i=0; i<data.children.length; i++) {
    // perform logic on data.children[i] here
    for(var j=0; j<data.children[i].children.length; j++) {
      // perform logic on data.children[i].children[j] here
      for(var x=0; x<data.children[i].children[j].children.length; x++) {
        //perform logic on data.children[i].children[j].children[x] here
      }
    }
  }
}
</pre>

 Just imagine if this JSON was actually storing the contents of a supermarket's inventory.

<ul>
  <li>
    <strong>This code is essentially impossible to read.</strong> Performing any sort of business logic on these objects is going to be extremely difficult when working with this sort of nested for loop structure.
  </li><br>
  <li>
    What happens in the above example if we were to add new options at various nodes in the graph? Our code will break.
  </li>
</ul>
<br>

<h4> 2.) DEPTH FIRST SEARCH </h4>

What if our code looked something like:

<pre>
function parse(list) {
  list = list.map(addOrganicOptions);
}

function addOrganicOptions(element){
  if (element.children.length > 0) {
    parse(element.children);
  }
  else {
    element.children = [organicOption, nonOrganicOption];
  }
  return element;
}

parse(data.children)
</pre>

Here we begin by mapping over the children array in our JSON. We navigate through our graph until the condition of <strong> not having children </strong> is met. 

For this hypothetical instance we simply then add the two options of "organic" and "non-organic" to the child property of first node found without children.

This algorithim is known as depth first search because we start at our root node and then navigate all the way to the bottom of our graph before backtracking and performing our logic. Because our JSON's repetitive strucure we can leverage recursion by calling <code>function parse()</code> on every node with a <code>"children"</code> property that has contents.

In other words we sink down and then perform our logic while bubbling back up to our root.

![]({{ site.url }}/images/node-chart.png)


** big thank you to <a target="blank" href="https://github.com/jskelcy" > Jake Skelcy </a> for helping to explain this concept to me

