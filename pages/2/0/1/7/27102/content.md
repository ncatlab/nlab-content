+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A *harmonic function* is a function which has zero [[Laplacian]].

It can often be interpreted as a function whose value at $x$ is equal to its [[average]] on a "neighborhood" of $x$.
A similar interpretation is as a function which is *invariant on average* under the transition given by [[diffusion]], by a [[Markov chain]], or by the [[edges]] of a [[graph]].

In [[physics]], a harmonic function represents a quantity which, in some sense, is spatially at [[equilibrium]]. For example, a body $B$ at a certain temperature $T$ surrounded by bodies of other temperatures, in such a way that the temperature $T$ is the average of the temperatures of the neighbors. This way, no net flow of heat passes into or out of $B$.


## For manifolds 

Given a [[Riemannian manifold]] $M$, a [[smooth function]] $f:M\to\mathbb{R}$ or $M\to\mathbb{C}$ is called **harmonic** if and only if its [[Laplacian]] is zero:
$$
\Delta f \;=\; 0 .
$$

(...)

### Examples

* Every [[holomorphic function]] $\mathbb{C}\to\mathbb{C}$ is harmonic.
* In [[physics]], the [[electric potential]] is [[harmonic]] when there are no [[electric charges]]. 

## For graphs

Given an [[undirected graph]] $G=(V,E)$, a function $f:V\to\mathbb{R}$ is called **harmonic** if and only if its [[discrete Laplacian]] $\Delta f$ is zero. 

For finite graphs, $f$ is equivalently harmonic if and only if 
$$
\sum_{y\sim x} f(y) \;=\; f(x) \, deg(x) .
$$
If $x$ has nonzero degree, equivalently,
$$
\frac{1}{deg(x)}\sum_{y\sim x} f(y) \;=\; f(x) .
$$
That is, $f(x)$ is equal to the [[average]] over the [[adjacent]] vertices.

If the graph is weighted, the formula becomes
$$
\sum_{y\in V} f(y) \, A(y,x) \;=\; \sum_{y\in V} f(x) \, A(y,x) ,
$$
where $A$ denotes the [[adjacency matrix]].
Again, for nonzero degree, this can be equivalently written as
$$
\frac{\sum_{y\in V} f(y) \, A(y,x)}{\sum_{y\in V} A(y,x)} \;=\; f(x)  .
$$
That is, $f(x)$ is equal to the [[weighted average]] over the [[adjacent]] vertices.


### Directed graphs

For [[directed graphs]] there is a difference between [[discrete Laplace operator#for_directed_graphs|incoming and outcoming Laplacians]]. Accordingly, a function is *incoming-harmonic* if its incoming Laplacian is zero, and *outcoming-harmonic* of its outcoming Laplacian is zero. 

For finite graphs, $f$ is equivalently incoming-harmonic if and only if for all $x\in V$, 
$$
\sum_{y\in in(x)} f(y) \;=\; f(x)\,|in(x)|
$$
where $in(x)$ denotes the set of vertices $y$ with edges $y\to x$,
and outcoming-harmonic if and only if for all $x\in V$,
$$
\sum_{y\in out(x)} f(y) \;=\; f(x)\,|out(x)|
$$
where $out(x)$ denotes the set of vertices $y$ with edges $x\to y$. 

If the graph is weighted, the formulas become 
$$
\sum_{y\in V} f(y) \, A(y,x) \;=\; \sum_{y\in V} f(x) \, A(y,x)
$$
and
$$
\sum_{y\in V} f(y) \, A(x,y) \;=\; \sum_{y\in V} f(x) \, A(x,y)
$$
respectively, where $A$ is the [[adjacency matrix]].


## For Markov chains

Given a [[finite-state Markov chain]] (or equivalently a [[stochastic matrix]]) with transitions $k(y|x)$ on a finite set $X$, a function $f:X\to\mathbb{R}$ is called **harmonic** if and only if for all $x\in X$, 
$$
\sum_{x\in X} f(y)\,k(y|x) \;=\; f(x) .
$$
Notice that this is the same as an outgoing-harmonic function on the weighted graph whose [[adjacency matrix]] is $A(x,y)=k(y|x)$. 

More generally, given a [[Markov kernel]] $k$ on a [[measurable space]] $X$, a [[measurable function]] $f:X\to\mathbb{R}$ is called **harmonic** if and only if for all $x\in X$, 
$$
\int_X f(y) \; k(d y|x) \;=\; f(x) .
$$
Given an [[invariant measure]] $p$ on $X$, we call $f$ **almost surely harmonic** if the equation above holds for $p$-almost all $x$.

\begin{proposition}
Given a [[Markov kernel]] on $X$ with an [[invariant measure]], the following conditions for a function $f:X\to\mathbb{R}$ are equivalent:

- $f$ is almost surely harmonic;

- $f$ is almost surely [[invariant]];

- $f$ is [[measurable function|measurable]] for the almost surely [[invariant set#almost_surely_invariant_sets|invariant sigma-algebra]].

\end{proposition}


## See also

* [[harmonic map]], [[harmonic form]]

* [[Laplace operator]]

* [[discrete Laplace operator]]

* [[harmonic form]]