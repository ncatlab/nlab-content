
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

Let $X$ by a differentiable [[manifold]]. The _tangent Lie algebroid_ $T X$ of $X$ is the [[Lie algebroid]] that corresponds -- in the sense of  [[Lie theory]] -- to 

* the [[codiscrete groupoid]] $X \times X$ of $X$. 

* the [[fundamental groupoid]] $\Pi_1(X)$ of $X$. 

When the tangent Lie algebroid is regarded as a [[Lie ∞-algebroid]] it corresponds to

* the [[path ∞-groupoid]] $\Pi_\infty(X)$.

The space of objects of $T X$ is $X$ itself and its elements in degree 1 are the vectors on $X$, i.e. the elements in the [[tangent bundle]] of $X$. These are to be thouhght of as the [[infinitesimal space|infinitesimal]] paths in $X$.

So to some extent the tangent Lie algebroid _is_ the [[tangent bundle]] $T X$ of $X$. More precisely, when using the definition of a [[Lie algebroid]] $E$ over $X$ as a diagram

$$
  \array{
    E &&\stackrel{\rho}{\to}&& T X
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

where $\rho$ is the map called the _anchor map_, the tangent Lie algebroid is that whose anchor map is the identity map

$$
  \array{
    E = T X &&\stackrel{\rho = Id}{\to}&& T X
    \\
    & \searrow && \swarrow
    \\
    && X
  }
  \,.
$$

Therefore the tangent Lie algebroid of $X$ is usually denoted $T X$, just as the [[tangent bundle]] itself.

The [[Chevalley-Eilenberg algebra]] of $T X$ is correspondingly fundamental: it is the [[deRham dg-algebra]] of [[differential form]]s on $X$:

$$
  CE(T X) = (\Omega^\bullet(X), d_{dR})
  \,.
$$

So regarded as an [[NQ-supermanifold]] the tangent Lie algebroid is the [[shifted tangent bundle]] $\Pi T X$ equipped with its canonical odd vector field.

## Relation to flat $\infty$-Lie algebroid valued differential forms ##

For $\mathfrak{a}$ any other [[Lie algebroid]] or [[Lie infinity-algebroid]], a morphism of [[Lie infinity-algebroid]]s 

$$
  \omega : T X \to \mathfrak{a}
$$

is _flat $\mathfrak{a}$-valued [[differential form]] datum_ .

For instance if $\mathfrak{a} = \mathfrak{g}$ is an ordinary [[Lie algebra]] then a morphism $T X \to \mathfrak{g}$ is a flat Lie algebra valued differential form on $X$, i.e. an element $A \in \Omega^1(X) \otimes \mathfrak{g}$ such that $d A + [-,-](A \wedge A) = 0$.

If $\mathfrak{g} = \mathfrak{u}(1) = \mathbb{R}$ is the abelian 1-dimensional Lie algebra, then a morphism $T X \to \mathfrak{g}$ is just a closed [[differential form|differential 1-form]] on $X$.

More on $\infty$-Lie algebroid-valued differential forms is (eventually) at [[schreiber:∞-Lie algebroid valued differential forms]].


## Related concepts

The higher-order version of tangent Lie algebroids are [[jet bundle]] [[D-scheme]]s.

## References ##

One of the earliest reference seems to be

* [[Ted Courant]], _Tangent Lie algebroids_.  Journal of Physics A: Mathematical and General 27:13 (1994), 4527-4536.  [doi](http://dx.doi.org/10.1088/0305-4470/27/13/026).

[[!redirects tangent Lie algebroids]]

