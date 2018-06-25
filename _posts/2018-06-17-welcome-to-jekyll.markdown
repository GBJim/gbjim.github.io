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


Here are the two important properties that hold both in A* and D*-Lite:
Min Queue:
[Image]
In the min-queue, the node with minimal cost pops and gets visited earlier. This property ensures the computation on each node goes in an ascending order.

DP Update Formula:
$$
g(s) =
\begin{cases}
0 & \text{if s is start point} \\
min_{s' \in Preds(s)} (c(s, s') + g(s')) & \text{otherwise,}
\end{cases}
$$
[Image]
The computation of a node depends on it's predecessor with the minimal cost. In the other hand, if the cost of the node is the minimum to the successors, it propagates the computation to the successors. This property results the "Upstream" and the "Downstream". Upstream nodes propagates the computation to the downstream nodes.


How do we apply this two ideas in dynamic environments?
Let's see this example.

In the begining, we just search like in static space.

[Image]

When the chagne happens, we update the changes. The changed nodes propogate this information to the neighboring nodes, if the new cost ??????????? ,causing an chain reation.





#Traisition
In D-Star-Lite, this two 





**Meta:**
D-Star-Light introduces two values: g(s) and rhs(s) to capture 2,
f(n) = g(n) + h(n)
rhs(s) = c(s, s') + g(s')



$$
f(s) = g(s) + h(s)
$$

$$
rhs(s) =
\begin{cases}
0 & \text{if s is start point} \\
min_{s' \in Succ(s)} (c(s, s') + g(s')) & \text{otherwise,}
\end{cases}
$$

$$
g(s) = rhs(s)
$$

$$
key(s) = [k_1(s), k_2(s)]\\
= [\min(g(s), rhs(s)) + h(s),\\
min(g(s), rhs(s)) ]\\
$$




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
