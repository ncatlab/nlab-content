
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
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[moduli space]] of ([[pseudo-Riemannian metric|pseudo]])-[[Riemannian metric]]s $g$ on a given [[space]] ([[manifold]]) $X$.

## Definition

On the [[site]] [[CartSp]] of [[smooth manifold|smooth]] [[Cartesian space]]s consider the [[sheaf]]

$$
  Met : CartSp^{op} \to Set
$$

which sends each $U \in CartSp$ to the set of [[Riemannian metric]]s on $U$.

Then let $X$ be a [[smooth manifold]], or more generally a [[diffeological space]], or more generally a [[Lie groupoid]] or more generally a [[smooth ∞-groupoid]], all regarded in $\mathbf{H} = $ [[Smooth∞Grpd]].

Write

$$
  Met(X) := Conc [X,Met]
$$

for the [[concrete sheaf|concretification]] of the [[internal hom]]: the space of metrics on $X$.
(Various variations and extensions of this statement are of interest and can easily be written out. The above direct statement works for possibly degenerate metrics.)

A point in this space is a single (pseudo-)Riemannian metric on $X$.


The group $Aut(X)$ of [[automorphism]]s of $X$ [[action|acts]] on this by precomposition in the natural way

$$
  Aut(X) \times Met(X) \to Met(X)
$$

$$
  ((X \stackrel{\phi}{\to} X), g)
  \mapsto
  \phi^* g
  \,.
$$

If $X$ is a [[smooth manifold]] then $Aut(X) = Diff(X)$ is the group of [[diffeomorphism]]s of $X$.

The [[quotient]] ([[action groupoid]], [[moduli stack]])

$$
  Met(X)//Diff(X) \in Smooth\infty Grpd
$$

is the _moduli space of (pseudo-)Riemannian metrics_ on $X$.

Various variations of this are of interest. For instance there one consider the [[Einstein-Hilbert action]]

$$
  S : Met(X)//Diff(X) \to \mathbb{R}
  \,.
$$

The [[critical locus]] of this function is the moduli space of [[Einstein metric]]s. 

## Properties

For $X$ a smooth manifold, $Met(X)$ itself is a [[contractible space]].

## Applications

In the context of the theory of [[gravity]], the moduli space of pseudo-Riemannian metrics on $X$ is the [[configuration space]] of the [[quantum field theory|field theory]] of gravity ([[general relativity]]). The moduli space of Einstein metrics is then called the [[covariant phase space]]: this is the subspace of solutions of the [[Einstein equations]].

## Related concepts

[[!include moduli spaces -- contents]]


## References

Textbook references include 

* [[Mikhail Gromov]], _Metric structures for Riemannian and non-Riemannian spaces_ Birkh&#228;user (1999)

chapter 4 of

* A. L. Besse, _Einstein Manifolds_ , Ergeb. Math. Grenzgeb. 10, Springer-Verlag, New York,
(1987) MR 88f:53087 Zbl 0613.53001

* M. E. Shanks, _The Space of Metrics on a Compact Metrizable Space_ , American Journal of Mathematics  Vol. 66, No. 3, Jul. (1944) ([JSTOR](http://www.jstor.org/stable/2371909))

* Halldor Eliasson, _On variations of metrics_ Math. Scand. 29 (1971) 317-327 ([pdf](http://www.mscand.dk/article.php?id=2047))

* F. Farrell, Pedro Ontaneda, _The Teichm&#252;ller space of pinched negatively curved metrics on a hyperbolic manifold
is not contractible_ ([pdf](http://annals.math.princeton.edu/wp-content/uploads/annals-v170-n1-p02-p.pdf))

* Boris Botvinnik, Bernhard Hanke, [[Thomas Schick]], and Mark Walsh, _Homotopy groups of the space of metrics of positive scalar curvature_ ([pdf](http://www.math.uni-augsburg.de/de/prof/diff/arbeitsgruppe/hanke/Arbeiten/bhsw-06.pdf))

[[!redirects moduli spaces of Riemannian metrics]]