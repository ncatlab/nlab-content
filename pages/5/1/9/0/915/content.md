# Multi-valued functions
* tic
{: toc}


## Idea

A _multi-valued function_ $f: A \to B$ is like a [[function]] from $A$ to $B$ except that there may be more than one possible value $f(x)$ for a given element $x$ of $A$.  (Compare a [[partial function]], where $f(x)$ may not exist at all.)

In older literature (into the 20th century, especially in analysis), functions were often considered to be multi-valued by default, requiring one to specify a _singe-valued_ function otherwise.  As [[set theory|set-theoretic formalisation]] spread, this intuition became difficult to maintain, and the modern concept of function must be single-valued.  If you want multi-valued functions, then you can get them in terms of single-valued functions as below.


## Definitions

Given [[set]]s $A$ and $B$, a __multi-valued function__ $f$ from a $A$ to $B$ is a [[span]]
$$ \array {
  &              & D \\
  & \swarrow_\pi &   & \searrow^f \\
A &              &   &            & B \\
} $$
of single-valued functions, where $\pi: D \to A$ is a [[surjection]].  (This condition can be dropped to define a multi-valued [[partial function]], which is simply a span.)

We will call $A$ and $B$ the _[[source]]_ and _[[target]]_ of $f$ as usual; then we call $D$ the __domain__ of $f$ and $\pi: D \to A $ the __projection__ of the domain onto the source.  By abuse of notation, the multi-valued function $f$ is conflated with the (single-valued) function $f: D \to B$.

Often one can assume that the induced function $D \to A \times B$ is an [[injection]]; in that case, a multi-valued function is the same as an [[entire relation]].  On the other hand, if you\'re considering all of the multi-valued functions for a given $D$, then this restriction is not really appropriate.

We consider two multi-valued functions (with the same given source and target) to be __equal__ if there is a [[bijection]] between their domains that makes the obvious diagrams commute.


## Examples

In 19th-century analysis, one considered the square-root function, the [[logarithm]], and so forth to be multi-valued functions of complex numbers.  We now understand this in terms of [[Riemann surface]]s; the domain $D$ above is a Riemann surface.  (Notice that the logarithm is actually a multi-valued *partial* function from $\mathbf{C}$ to $\mathbf{C}$, although it is a multi-valued total function on $\mathbf{C} \setminus \{0\}$.)


[[!redirects multivalued function]]
[[!redirects multivalued functions]]
[[!redirects multi-valued functions]]