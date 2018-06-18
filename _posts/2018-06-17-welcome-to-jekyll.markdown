---
layout: post
title:  "D-Star-Light: Searching in Dynamic Space"
date:   2018-06-17 15:59:29 +0800
categories: algorithm
ref: d-star
lang: en
comments: true
---
**Abstract:**
Searching Algorithms are the cores of nvigation systems and motion planning. You are probably familiar with searching algorithms like Breadth-First Search, Depth-First Search, or the more advanced A* search.
If you are not familiar with A* search, here is [a great article](http://theory.stanford.edu/~amitp/GameProgramming/AStarComparison.html) to get started

But these algorithms assume the environment to be static. In reality, environment are constantly changing. To deal with it, we can simply do re-searching whenever the environment changed. But this kind of approach may suffer from inefficiency, even a small change of the world would introduce the re-computation of every single step.

Is there a way to re-compute only the necessary steps?
Here comes the D-Star-Light, the Dynamic version of A*. It works similar to A*, but computes only the necessary nodes to update the shortest path when environment is changed.

Before we get started, let's picture what are necessary and unnecessary computational steps and how the computation "propagates"

Here is the visualization of A star

![a-star](/assets/img/a_star.gif){:class="img-responsive"}

As you can see, the computation propagates from the starting node to the destination mode. More precisely, the computation propagates from nodes with smaller cost to nodes with bigger cost. This is the result of the min-queue and the DP fashioned cost updating formula: g(s) = f(s') + c(s) where s' is the predecessor with the minimal cost.
The min queue ensure that the current smaller nodes always get computed earlier then bigger nodes. The DP formula propagates the computation from nodes to nodes.

Now, lets imagine what would happen when the environment is changed.
##GIF animation of A star, changed
After the barrier is added,




**Meta:**
D-Star-Light introduces two values: g(s) and rhs(s) to capture 2,
f(n) = g(n) + h(n)
rhs(s) = c(s, s') + g(s')







Jekyll also offers powerful support for code snippets:

{% highlight python %}
INF = float("inf")
def main():
  for node in graph:
    node.rhs = node.g = INF
  start_node.rhs = 0
  open_queue = []
  while True:
    compute_shortest_path(graph)
    if is_environment_changed():
      update_graph_cost()

{% endhighlight %}



{% include disqus.html %}
