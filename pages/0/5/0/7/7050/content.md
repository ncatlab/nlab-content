
# Simple homotopy theory
* table of contents
{: toc}

## Idea and a bit of history

The aim of much of [[homotopy theory]] in the 1930s and 1940s was to try to lay _combinatorial_ foundations for determining whether two [[topological spaces]] were of the same [[homotopy type]] and, if so, was it possible to build up the homotopy equivalences in some simple way.  The model for this idea came, it seems, from [[Tietze transformation|Tietze's theorem]] in the theory of group presentations, where any presentation of a group could be deformed into any other by a series of 'moves'.  The same process was apparent in the development of the classification theorem for surfaces.  The question thus was: could one find some simple set of 'moves' that would generate all the homotopy equivalences with a given domain, $X$?

The theory was initially developed by Reidemeister, and then [[Henry Whitehead|Whitehead]], culminating in his 1950 paper _Simple homotopy types_.  The theory received a further stimulus with [[John Milnor|Milnor]]'s classic paper in 1966 in which emphasis was put on [[elementary expansion]]s.

Further interesting approaches were developed by [[Eckmann]] and [[Siebenmann]] in 1970 (see references).

##Elementary expansions and contractions


We will work here with finite CW-complexes. These are built up by induction by gluing on $n$-cells, that is copies of $D^n=\{x\in \mathbb{R}^n\mid \sum x_i^2\leq 1\}$, at each stage.  Each $D^n$ has a boundary an $(n-1)$-sphere, $S^{n-1}=\{x\in \mathbb{R}^n\mid \sum x_i^2= 1\}$.  The construction of objects in the category of finite CW-complexes is by attaching cells by means of maps defined on part of all of the boundary of a cell.  This will usually change the homotopy type of the space, creating or filling in a 'hole'. The homotopy type will not be changed if the attaching map has domain a hemisphere.  We write $S^{n-1} = D^{n-1}_-\cup  D^{n-1}_+$, with each hemisphere homeomorphic to a $(n-1)$-cell, and their intersection being the equatorial $(n-2)$-sphere, $S^{n-2}$, of $S^{n-1}$.



Given, now, a finite CW-complex, $X$, we can build a new complex $Y$, consisting of $X$ and two new cells, $e^n$ and $e^{n-1}$ together with a continuous map, $\varphi : D^n\to Y$ satisfying 

(i) $\varphi(D^{n-1}_+)\subseteq X_{n-1}$;

(ii) $\varphi(S^{n-2}) \subseteq X_{n-2}$;

(iii) the restriction of $\varphi$ to the interior of $D^n$ is a homeomorphism onto $e^n$;

and

(iv) the restriction of $\varphi$ to the interior of $D^{n-1}_-$ is a homeomorphism onto $e^{n-1}$.


There is an obvious inclusion map, $i: X\to Y$, which is called an _elementary expansion_.  There is also a retraction map $r : Y\to X$, homotopy inverse to $i$, and which is called an _elementary contraction_.  Both are [[homotopy equivalences]]. 

* Can all homotopy equivalences between finite CW-complexes be built by composing such elementary ones? 

More precisely, if we have a homotopy equivalence $f: X\to X^\prime$, is $f$ homotopic to a composite of a finite sequence of elementary expansions and contractions?  Such a homotopy equivalence would be called _simple_.  Whitehead showed that not all homotopy equivalences are simple and constructed a group of obstructions for the problem with given space $X$, each non-identity element of the group corresponding to a distinct homotopy class of non-simple homotopy equivalence.



## References

Some original sources:

*  [[J. H. C. Whitehead]], _Simple homotopy type_, Amer. J. Math., 72,  (1950), 1 - 57.

* [[J. Milnor]], _Whitehead torsion_, Bull. Amer. math. Soc., 72 (1966), 358 - 426.

* [[B. Eckmann]], _Simple homotopy type and categories of fractions_, Symp. Math. V (1970), 285 - 299.

* [[B. Eckmann]] and S. Maumary, _Le groupe des types simples d'homotopie sur un poly&#232;dre_, Essays on Topology and related topics, M&#233;moires d&#233;di&#233;s &#224; Georges de Rham, Springer (1970).

* [[L. C. Siebenmann]], _Infinite simple homotopy types_, Indag. math. 32, (1970), 479 - 495.

A very useful textbook is:

* M. M. Cohen, _A course in Simple Homotopy Theory_, Grad. Texts in Math, 10, Springer, 1973.


A more abstract, but at the same time geometric, approach to simple homotopy theory was explored in Cohen's book as well as in the papers by Eckmann, Eckmann and Maumary, and Siebenmann, listed above. Some of this is treated in

* K. H. Kamps, [[Tim Porter]], _Abstract homotopy and simple homotopy theory_, World Scientific 1997. 
[[!redirects simple homotopy theory]]
