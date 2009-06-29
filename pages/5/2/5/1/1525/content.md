
There are several concepts often called a _path category_ .

* Given a [[directed graph]], the corresponding free [[category]] or [[quiver]] on the graph is often called the graph's _path category_, as its morphisms are given by finte sequences of consecutive edges in the graph.

* Given a [[topological space]] $X$ or some other kind of space with a notion of maps from intervals into it, there are various ways to obtain a category whose collection of objects is $X$, and whose morphisms are images of intervals in $X$, i.e. paths in $X$. This is also often called a _path category_. 

  * In particular, for every toplogical space there is its [[fundamental groupoid]] whose morphisms are [[homotopy]] classes of images of intervals in $X$.

  * If $X$ is a [[directed space]] there is a notion of path category called the [[fundamental category]] of $X$.

  *  When $X$ is a smooth space, there is a notion of path category where less than homotopy of paths is divided out: just _thin_ homotopy. This yields a notion of [[path groupoid]]. 

  * If _parameterized_ paths are used, there is a way to get a category of paths without dividing out any equivalence relation: this is the [[Moore path category]].


+--{.query}

_Eric_: What is the [[functor category]] $[I,X]$ called, where $I$ is the [[interval category]]? 

Background: I was thinking that given any category $X$ and the interval category $I$, then a functor 

$$\gamma:I\to X$$

looks like a curve/path in $X$. Once I started thinking about that, the next thing to think of is a collection of such functors, which made me think of $[I,X]$. If $X$ is a "space", then $[I,X]$ would be a "path space", but if $X$ is just any category, I might be tempted to call $[I,X]$ a "path category". 

Is there another standard name for this?

_Eric_: I see. It is called the [[arrow category]].

=--