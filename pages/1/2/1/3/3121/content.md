

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea ##

The _stabilization_ of an [[(∞,1)-category]] $C$ with [[finite (∞,1)-limits]]  is the [[free construction|free]]
[[stable (∞,1)-category]] $Stab(C)$ on $C$. This is also called the $(\infty,1)$-category of
[[spectrum objects]]  of $C$, because for the archetypical example where $C = $ [[Top]]
the stabilization is $Stab(Top) \simeq Spec$ the category of [[spectrum|spectra]].

There is a canonical [[forgetful functor|forgetful]] [[(∞,1)-functor]] $\Omega^\infty : Stab(C) \to C$ that remembers of a [[spectrum object]] the underlying object of $C$ in degree 0. Under mild conditions, notably when $C$ is a [[presentable (∞,1)-category]], this functor has a [[left adjoint]] $\Sigma^\infty : C \to Stab(C)$ that _freely stabilizes_ any given object of $C$.

$$
  (\Sigma^\infty \dashv \Omega^\infty)
  :
  Stab(C)
   \stackrel{\overset{\Sigma^\infty}{\leftarrow}}{\underset{\Omega^\infty}{\to}}
  C
  \,.
$$

Going back and forth this way, i.e. applying the corresponding [[(∞,1)-monad]] $\Omega^\infty \circ \Sigma^\infty$ yields the assignment

$$
  X \mapsto \Omega^\infty \Sigma^\infty X
$$

that may be thought of as the **stabilization of an object** $X$. 
Indeed, as the notation suggests, $\Omega^\infty \Sigma^\infty X$ may be thought of as the result as $n$ goes to infinity of the operation that forms from $X$ first the $n$-fold [[suspension object]] $\Sigma^n X$ and then from that the $n$-fold [[loop space object]].

## Definition

### Abstract definition

Let $C$ be an [[(∞,1)-category]] with [[finite (∞,1)-limit]] and write
$C_* := C^{{*}/}$ for its [[(∞,1)-category]] of [[pointed objects]], the
[[undercategory]] of $C$ under the [[terminal object]].


On $C_*$ there is the [[loop space object]] [[(infinity,1)-functor]] 
$\Omega : C_* \to C_*$, that sends each object $X$ to the [[pullback]] of the
point inclusion ${*} \to X$ along itself. Recall that if a $(\infty,1)$-category is stable, the [[loop space object]] functor is an equivalence.

The _stabilization_ $Stab(C)$ of $C$ is the
[[(∞,1)-limit]] (in the [[(∞,1)-category of (∞,1)-categories]]) of the 
tower of applications of the loop space functor

$$
  Stab(C)
  =
  \underset{\leftarrow}{\lim}
  \left(
    \cdots \to C_* \stackrel{\Omega}{\to} C_* \stackrel{\Omega}{\to} C_*
  \right)
  \,.
$$


This is ([StabCat, proposition 8.14](http://arxiv.org/abs/math/0608228)).

The canonical functor from $Stab(C)$ to $C_*$ and then further, via the functor that
forgets the basepoint, to $C$ is therefore denoted

$$
  \Omega^\infty : Stab(C) \to C
  \,.
$$

### Construction in terms of spectrum objects

Concretely, for any $C$ with finite limits, $Stab(C)$ may be constructed as the category of [[spectrum object]]s of $C_*$:

$$
  Stab(C) = Sp(C_*)
  \,.
$$ 


This is definition 8.1, 8.2 in [StabCat](http://arxiv.org/abs/math/0608228)

### Construction in terms of stable model categories
 {#ConstructionInTermsOfStableModelCategories}

Given a presentation of an [[(∞,1)-category]] by a [[model category]], there is a notion of stabilization of this model category to a [[stable model category]]. That this in turn presents the abstractly defined stabilization of the corresponding [[(∞,1)-category]] is due to ([Robalo 12, prop. 4.14](#Robalo12)).

## Properties

* If $C$ is an $(\infty,1)$-category with finite limits that is a
[[presentable (∞,1)-category]], then the functor $\Omega^\infty : Stab(C) \to C$
has a [[left adjoint]]

  $$
    \Sigma^\infty : C \to Stab(C)
    \,.
  $$

  Prop 15.4 (2) of [StabCat](http://arxiv.org/abs/math/0608228).

* stabilization is _not_ in general functorial. It's failure of being functorial, and approximations to it, are studied in [[Goodwillie calculus]].

## Examples

* For $C = $ [[Top]] the stabilization is the category [[Spec]] of [[spectra]]. The functor $\Sigma^\infty : Top_* \to Spec$  is that which forms [[suspension spectra]].

## Related concepts

[[!include k-monoidal table]]

## References
 {#References}

A general discussion in the context of [[(∞,1)-category theory]] is in  

* [[Jacob Lurie]], section 1.4 _[[Higher Algebra]]_

* [[Jacob Lurie]], section 1 of _[[Spectral Schemes]]_

Discussion of the relation between stabilization of [[(∞,1)-categories]] (to [[stable (∞,1)-categories]]) and of [[model categories]] (to [[stable model categories]]) is in section 4.2 of

* [[Marco Robalo]], _Noncommutative Motives I: A Universal Characterization of the Motivic Stable Homotopy Theory of Schemes_, June 2012 ([arxiv:1206.3645](http://arxiv.org/abs/1206.3645))
  {#Robalo12}


[[!redirects stabilizations]]