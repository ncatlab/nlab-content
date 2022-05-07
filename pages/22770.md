> This entry is about scales in [[algebra]] and [[linear logic]]. For scales in [[geometry]] and [[physics]], see [[length scale]]. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The idea of a scale comes from [[Peter Freyd]]. Scales are models of multiplicative-additive [[linear logic]]. 

## Definition

A __scale__ is a [[minor scale]] $M$ satisfying the scale identities: 

* for all $a$ and $b$ in $M$, $a \otimes b = (a^\vee \otimes b^\wedge) \vert (a^\wedge \otimes b^\vee)$

* for all $a$ and $b$ in $M$, $a \oplus b = (a^\wedge \oplus b^\vee) \vert (a^\vee \oplus b^\wedge)$

## Properties

Every scale with $\bot = \top$ is [[trivial object|trivial]]. 

As a scale is a [[closed midpoint algebra]], a scale has a [[partial order]]. Let the binary operation $(-)\multimap(-):M \times M \to M$ be defined as 

$$a \multimap b \coloneqq a^\bullet \oplus b$$ 

If $a \multimap b = \top$, then $a \leq b$. 

$(M,\wedge,\vee,\bot,\top)$ forms a [[lattice]]. 

A subset $\mathcal{I}$ of a scale $M$ is an __[[ideal]]__ if $\bot \in \mathcal{I}$, and $x \vee y \in \mathcal{I}$ if and only if $x \in \mathcal{I}$ and $y \in \mathcal{I}$. An ideal is a __zoom-invariant ideal__ if it is closed under $\bot$-zooming. 

A subset $\mathcal{I}$ of a scale $M$ is a __$\bot$-face__ if $\bot \in \mathcal{I}$, and $x \vert y \in \mathcal{I}$ if and only if $x \in \mathcal{I}$ and $y \in \mathcal{I}$. 

Every $\bot$-face is a zoom-invariant ideal. 

Given an element $a$ in scale $M$, a __principal $\bot$-face__ $((a))$ is the subset of all $b$ in $M$ such that $(\bot\vert)^n b \leq a$ for all large $n$ in $\mathbb{N}$. 

A __[[Jacobson radical]]__ of a scale $M$ is the set $J(M)$ of all $a$ in $M$ such that for all $n$ in $\mathbb{N}$, $x \leq (\bot\vert)^n \top$. $M$ is __semi-simple__ if $J(M)$ is [[trivial]]. 

+-- {: .standout}
The proof of the Linear Representation Theorem in section 8 of _Algebraic Real Analysis_ by Peter Freyd requires the use of [[excluded middle]] through its implicit definition of the [[quasiorder]] $\lt$ from the algebraically defined [[partial order]] $\leq$. In particular, that every equational axiom added to the theory of minor scales is either a consequence of the scale identity for scales, or is inconsistent with the theory of minor scales, is a classical result, as certain equations can only be derived from the scale identities through the Linear Representation Theorem. The same is true of the definition of simple scales in section 10, of the algebraic construction of the standard interval $I$ from simple scales in section 11, and various results involving absolute retracts in section 25. These results hold if the scales were linearly ordered or quasiordered, but it is unknown if these results still hold for general scales in [[constructive mathematics]] without the use of excluded middle. 
=--

### As star-autonomous categories

...

## Examples

The [[unit interval]] with $a \vert b \coloneqq \frac{a + b}{2}$, $\odot = \frac{1}{2}$, $a^\bullet = 1 - a$, $\bot = 0$, $\top = 1$, $a^\wedge = max(2a-1,0)$, and $a^\vee = min(2a,1)$ is an example of a scale.

The set of truth values in Girard's [[linear logic]] is a scale. 

## Related concepts

* [[minor scale]]

* [[Heyting scale]]

* [[linear logic]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

[[!redirects scales]]
