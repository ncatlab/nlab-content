
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Borel's theorem_ says that every [[power series]] is the [[Taylor series]] of some [[smooth function]]. In other words: for every collection of prescribed [[partial derivatives]] at some point, there is a smooth function having these as actual partial derivatives.

## Statement

+-- {: .num_theorem}
###### Theorem

The canonical map from the ring of germs of $C^\infty$ function at $0\in\mathbb{R}^n$ to the ring of formal power series obtained
by taking the Taylor series at $0$ is surjective.

=--

There are many extensions and variants. 


For $\mathbb{R}^{n+m}$ a [[Cartesian space]] of [[dimension]] $n+m \in \mathbb{N}$, write $C^\infty(\mathbb{R}^{n+m})$ for the $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth function]]s with values in $\mathbb{R}$.

Write $m^\infty_{\mathbb{R}^n \times \{0\}} \subset C^\infty(\mathbb{R}^{n+m})$ for the ideal of functions all whose [[partial derivative]]s along $\mathbb{R}^m$ vanish.

+-- {: .num_theorem}
###### Theorem

Forming the [[Taylor series]] constitutes an [[isomorphism]]

$$
  C^\infty(\mathbb{R}^{n+m})/m^\infty_{\mathbb{R}^n \times \{0\}}
  \stackrel{\simeq}{\longrightarrow}
  C^\infty(\mathbb{R}^n) [ [ Y_1, \cdots, Y_m] ]
$$

between smooth functions modulo those whose derivatives along $\mathbb{R}^m$ vanish and the ring of [[power series]] in $m$-variables over $C^\infty(\mathbb{R}^n)$.

=--

This appears for instance as ([Moerdijk-Reyes, theorem I.1.3](#MoerdijkReyes)).

## Related theorems

* the [[Hadamard lemma]]

* the [[Tietze extension theorem]]

* the [[Whitney extension theorem]]

* the [[Steenrod-Wockel approximation theorem]]

* [[embedding of smooth manifolds into formal duals of R-algebras]]

* [[smooth Serre-Swan theorem]]

* [[derivations of smooth functions are vector fields]]


## References

The original reference is

* [[Émile Borel]], _Sur quelques points de la th&#233;orie des fonctions_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 3, 12 (1895), 
p. 9-55 [numdam](http://www.numdam.org/item?id=ASENS_1895_3_12__9_0)

It has been actually proved by [[Guiseppe Peano]] before Borel

* &#193;d&#225;m Besenyei, _Peano's unnoticed proof of Borel's theorem_ ([pdf](http://www.cs.elte.hu/~badam/publications/borel.pdf))

Textbook discussion includes

* {#MoerdijkReyes} [[Ieke Moerdijk]], [[Gonzalo Reyes]], chapter I of _[[Models for Smooth Infinitesimal Analysis]]_

A generalization to [[Banach spaces]] is in 

* John C. Wells, _Differentiable functions on Banach spaces with Lipschitz derivatives_, J. Differential Geom. 8:1 (1973), 135-152 [euclid](http://projecteuclid.org/euclid.jdg/1214431488)

and is cited (along with extensive discussion and (counter)examples) also as (Ch.III) 15.4 in 

* [[Andreas Kriegl]], [[Peter Michor]], _[[The Convenient Setting of Global Analysis]]_, Mathematical Surveys and Monographs, 53 AMS (1997) [pdf](http://www.mat.univie.ac.at/~michor/apbookh-ams.pdf)

 

[[!redirects Borel theorem]]
[[!redirects Borel's theorem on power series]]