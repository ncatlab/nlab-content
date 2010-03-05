
#Contents#
* automatic table of contents goes here
{:toc}

## Idea of some problems

**Proper homotopy theory** is both an old and a fairly new area of [[algebraic topology].
It deals with properties of non-[[compact space|compact]] [[topological space]]s, that cannot be detected using maps from [[simplex|simplices]] in these spaces, such as used in the [[fundamental infinity-groupoid|singular complex]]. 

Historically the subject is traced back to Kerekjarto's classification of non-compact surfaces in 1923, but its emergence as an importatn tool in geometric topology came with Larry Siebenmann's work in 1965.

Suppose $M$ is a _smooth_ [[manifold9] with boundary, $\partial M$, then $M\setminus \partial M$ is an open manifold. Now suppose someone gives us an open manifold $N$, is it possible to detect if there is a compact manifold $M$, with $M\setminus \partial \cong N$.  Siebenmann showed that certain conditions on the _ends_ of $N$ were necessary and that there were obstructions if the dimension of $M$ was greater than 5.

Its potential importance of proper homotopy, 
for example for physical applications, comes from the fact that the phenomena it studies include the limiting behaviour of the system.

##Intuitions

The basic hypothesis will be that $X$ will be a [[connected space|connected and locally connected]] compact [[Hausdorff space],. It will usually be $\simga$-compact, i.e., there will be an increasing sequence, $\{K_n\}$, of compact subspaces with each $K_n$ in the interior of $K_{n+1}$ and such that 

$$X = \bigcup^\infty_{n=0}K_n,$$

These spaces will most often than not be locally finite [[simplicial complex]]es.

We will  be interested in the [[homotopy]] of such spaces 'out towards its ends' 


###Ends

To illustrate the idea of the ends of a space $X$, we note that naively $\mathbb{R}$ has two ends, $\infty$ and $-\infty$, whilst $\mathbb{R}^2$ has only one as it is $S^2\setminus \{\infty\}$, (but that is vague!).

More exactly, consider the system of spaces

$$\epsilon(X) = \{closure(X\setminus K) : K compact \sunset X\},$$

This is an inverse system or [[pro-object]] in the category of spaces. Applying the connected component functor, $\pi_0$, to this system of spaces gives $\pi_0(X)$, and, classically, one takes the limit of this to get 

$$e(X) = lim \pi_0\epsilon(X),$$
the _set of ends_ of $X$. In general, $e(X)$ would be given the [[inverse limit topology]], to preserve more of the information coming from its construction.  This space is the _space of (Freudenthal) ends of $X$_. It is a [[profinite space]].




##References##

Survey article:

* [[Tim Porter]], _Proper Homotopy Theory_,  in the _Handbook on Algebraic Topology_, Ed. I.M.James, Elsevier,1995, p. 127-167,

Book:

* [[Hans-Joachim Baues|H. J. Baues]] and A. Quintero, _Infinite homotopy theory_, Volume 6 of K-monographs in mathematics,	Springer, 2001
