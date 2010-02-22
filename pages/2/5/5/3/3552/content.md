
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **Sullivan model** of a [[rational space]] $X$ is a particularly well-behaved [[dg-algebra]] [[quasi-isomorphism|quasi-isomorphic]] to the dg-algebra of Sullivan forms on $X$:

## Definition

A **Sullivan algebra** is a dg-algebra that is cofibrant in the standard [[model structure on dg-algebras]]: a [[semifree dga]] $(\wedge^\bullet V, d)$ with a bais $\{v_\alpha | \alpha \in J\}$ of $V$ for $J$ a [[well-order]]ed set, such that $d v_\beta \in V_{\lt  \beta}$.

A **minimal Sullivan algebra** is a Sullivan algebra such that moreover

$$
  (\alpha \lt \beta ) \Rightarrow deg v_\alpha \lt deg v_\beta
  \,.
$$


A **Sullivan (minimal) model** of a [[dg-algebra]] $A$ is a Sullivan (minimal) algebra $(\wedge^\bullet V,d)$ and a [[quasi-isomorphism]]

$$
  (\wedge^\bullet V, d) \stackrel{\simeq_{w}}{\to} A
  \,.
$$

A **Sullivan (minimal) model** of a [[connected space|connected]] [[topological space]] is a Sullivan (minimal) model of its dg-algebra $\Omega^\bullet_{Sullivan}(X)$ of Sullivan forms.

## Properties


+-- {: .un_prop }
###### Proposition

Sullivan mimimal models are unique up to [[isomorphism]]. 

=--

+-- {: .proof}
###### Proof


This appears for instance as prop 1.18 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))


=--



+-- {: .un_theorem }
###### Theorem

Rational homotopy types of simply connected spaces $X$ are in bijective corespondence with minimal [[Sullivan model]]s $(\wedge^\bullet V,d)$

$$
  (\wedge^\bullet V , d) \stackrel{\simeq}{\to}
  \Omega^\bullet_{Sullivan}(X)
  \,.
$$

And homotopy classes of morphisms on both sides are in bijection.

=--

+-- {: .proof}
###### Proof

This appears for instance as corollary 1.26 in 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))


=--


## Examples 


### The $n$-sphere

...

### Complex projective space

...

### Product spaces

...

### Formal spaces

* [[formal dg-algebra]]

## References

In

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

Sullivan algebras and minimal algebras appear in def 1.10

[[!redirects Sullivan models]]
[[!redirects Sullivan algebra]]
[[!redirects Sullivan algebras]]
[[!redirects Sullivan minimal algebra]]
[[!redirects Sullivan minimal algebras]]