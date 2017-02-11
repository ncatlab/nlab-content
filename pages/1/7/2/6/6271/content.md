
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

__Borel\'s Theorem__ (also called _Borel\'s Lemma_) says that every [[power series]] is the [[Taylor series]] of some [[smooth function]]. In other words: for every collection of prescribed [[partial derivatives]] at some point, there is a smooth function having these as actual partial derivatives.


## Statements

+-- {: .num_theorem #basic}
###### Theorem

The canonical map from the ring of germs of $C^\infty$ function at $0 \in \mathbb{R}^n$ to the ring of formal power series obtained by taking the Taylor series at $0$ is surjective.
=--

There are many extensions and variants. 


For $\mathbb{R}^{n+m}$ a [[Cartesian space]] of [[dimension]] $n+m \in \mathbb{N}$, write $C^\infty(\mathbb{R}^{n+m})$ for the $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth function]]s with values in $\mathbb{R}$.

Write $m^\infty_{\mathbb{R}^n \times \{0\}} \subset C^\infty(\mathbb{R}^{n+m})$ for the ideal of functions all whose [[partial derivative]]s along $\mathbb{R}^m$ vanish.

+-- {: .num_theorem #general}
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


## Proof

There is a full proof in Moerdijk--Reyes, cited above.  Here we prove Theorem \ref{basic} to indicate the method; the general version is not substantially different.  (This is based on the proof in [the English Wikipedia article](https://en.wikipedia.org/wiki/Borel%27s_lemma) at the time of writing, but with more details.)

+-- {: .proof}
###### Proof (of Theorem \ref{basic})

A real [[power series]] at $0$ is given simply by an [[infinite sequence]] $c = (c_n)_{n\geq{0}}$ of [[real numbers]].  Given such a sequence, we would ideally use
$$ f(x) = \sum_{n=0}^\infty c_n x^n ,$$
but this is only correct if the sum converges on at least some [[neighbourhood]] of $0$ (in other words if the power series has a positive [[radius of convergence]]).

To ensure this, let $\psi$ be a [[smooth function|smooth]] [[bump function]] chosen so that $\psi(x) = 1$ for ${|x|} \leq 1$ and $\psi(x) = 0$ for ${|x|} \geq 2$.  (For example, $\psi(x) = \frac{\phi(x + 2)} {\phi(x + 2) + \phi(-x - 1)} \frac{\phi(-x + 2)} {\phi(-x + 2) + \phi(x - 1)}$, where $\phi(x)$ is $\exp(-1/x)$ when $x \gt 0$ and otherwise vanishes.)  Next, choose an infinite sequence $H = (H_n)_{n\geq{1}}$:
$$ H_n = \max_{0\leq{k}\lt{n}/2} \root{n-2k} {2^{2n-k} n^{\underline{k}} {\|\psi^{(k)}\|_\infty}} $$
(where $n^{\underline{k}}$ is the [[falling power]] $\prod_{0\leq{i}\lt{k}} (n - i)$, as discussed at [[binomial theorem]]).  Finally, define
$$ f(x) = c_0 + \sum_{n=1}^\infty c_n \psi(H_n x) x^n .$$
(The first term is because, morally, $H_0 = 0$.)

{I still need to explain why this series converges for all $x$ (and has the desired derivatives at $0$).  It\'s also possible that I have miscalculated $H$, in which case I should discover so as I finish this.}
=--


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
 

[[!redirects Borel's theorem]]
[[!redirects Borel\'s theorem]]
[[!redirects Borel/'s theorem]]
[[!redirects Borel's theorem]]
[[!redirects Borel theorem]]
[[!redirects Borel's theorem on power series]]

[[!redirects Borel's lemma]]
[[!redirects Borel\'s lemma]]
[[!redirects Borel/'s lemma]]
[[!redirects Borel's lemma]]
[[!redirects Borel lemma]]
