
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

> ... under construction ...

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _automorphism $\infty$-Lie algebra_ $aut(\mathfrak{g})$ of an [[∞-Lie algebra]] $\mathfrak{g}$ -- or dually $aut(CE(\mathfrak{g}))$ of the corresponding [[Chevalley-Eilenberg algebra]] -- has in degree $k$ the [[derivation]]s on $CE(\mathfrak{g})$ of degree $-k$.

In terms of [[rational homotopy theory]] $aut(\mathfrak{g})$ is a model for the rationalization of the  group of [[automorphisms]]s of the [[rational space]] $\exp(\mathfrak{g})$ corresponding to $CE(\mathfrak{g})$ under the [[Sullivan construction]].

## Definition

Let $A := (\wedge^\bullet \mathfrak{a}^*, d_A)$ be a [[semifree dga|semifree]] [[dg-algebra]] of [[finite type]].

Notice that for $\phi : A \to A$ a [[derivation]] of degree $-k$ and $\lambda : A\to A$ another derivation of degree $-l$ the [[commutator]]

$$
  [\phi,\lambda] := \phi \circ \lambda - \lambda \circ \phi : A \to A
$$

is itself a derivation, of degree $-(k+l)$. In particular, since the [[differential]] $d_A : A \to A $ is itself a derivation of degree +1, we have that

$$
  d_A \phi := [d_A, \phi] : A \to A
$$

is a derivation of degree $-(k+1)$.

+-- {: .un_defn}
###### Definition
**(automorphism $\infty$-Lie algebra)**

The [[∞-Lie algebra]] $aut(A)$ is the [[dg-Lie algebra]] which 

* in degree $-k$ for $k \gt 0$ has the derivations $\phi : A \to A$ of degree $-k$;

* in degree $0$ the derivations that commute with the differential $d_A$

* whose differential $\delta_{aut(A)} := [d_A,-]$ is given by the commutator with the differential of $A$;

* whose Lie bracket is the commutator $[\phi,\lambda] = \phi \circ \lambda - \lambda \circ \phi$.

=--

## Properties

### Automorphism group {#AutomorphismGroup}

For stating the fundamental theorem about $aut(\mathfrak{g})$ below we need some facts about the ordinary [[automorphism group]] of a dg-algebra $A$.

(...)

(See chapter 6 of [Sullivan](#Sullivan)).


### Classifying space for $Aut(X)$-principal bundles

Let $X$ be a [[rational space]] whose [[Sullivan model]] is $\mathfrak{g}$, $X \simeq \exp(\mathfrak{g})$. Let $aut'(\mathfrak{g}) \subset aut(\mathfrak{g})$ be the sub dg-algebra of the automorphism $\infty$-Lie algebra on the maximal nilpotent ideal in degree 0. Let $G(X)$ be the maximal reductive group of genuine automorphisms of $CE(\mathfrak{g})$ (see [above](#AutomorphismGroup)). 

Then the [[rational space]]

$$
  \exp(aut'(\mathfrak{g}))/G(X)
  \simeq
  B Aut (X)
$$

is the [[classifying space]] for $Aut(X)$-[[principal bundle]]s, i.e. for [[bundle]]s with typical fiber $X$.

## Examples

* The [[inner derivation Lie 2-algebra]] $inn(\mathfrak{g})$ is the full subalgebra of the automorphism $\infty$-Lie algebra on the _inner_ derivations of the [[Chevalley-Eilenberg algebra]] of a [[Lie algebra]] $\mathfrak{g}$.

## References

The general definition of $aut(\mathfrak{g})$ is the topic of p. 313 (45 of 63) and following in 

* [[Dennis Sullivan]], _Infinitesimal computations in topology_ ([pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1977__47_/PMIHES_1977__47__269_0/PMIHES_1977__47__269_0.pdf)) {#Sullivan}

The automorphism group $Aut(A)$ of a dg-algebra is discussed in paragraph 6 there.

Concrete computations of $aut(\mathfrak{g})$ for some classes of [[rational space]]s $X = \exp(\mathfrak{g})$ can be found for instance in 

* Samual Bruce Smith, _The rational homotopy Lie algebra of classifying spaces for formal two-stage spaces_ , Journal of Pure and Applied Algebra
Volume 160, Issues 2-3, 25 June 2001, Pages 333-343 


[[!redirects automorphism ∞-Lie algebra]]
[[!redirects automorphism dg-Lie algebra]]


[[!redirects automorphism infinity-Lie algebras]]
[[!redirects automorphism ∞-Lie algebras]]
[[!redirects automorphism dg-Lie algebras]]
