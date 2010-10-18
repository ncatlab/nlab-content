

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
* automatic table of contents goes here
{:toc}


## Idea ##

The _stabilization_ of an [[(∞,1)-category]] $C$ with finite [[limit]]s  is the [[free construction|free]]
[[stable (∞,1)-category]] $Stab(C)$ on $C$. This is also called the $(\infty,1)$-category of
[[spectrum object]]s  of $C$, because for the archetypical example where $C = $ [[Top]]
the stabilization is $Stab(Top) \simeq Spec$ the category of [[spectrum|spectra]].

There is a canonical [[forgetful functor|forgetful]] [[(∞,1)-functor]] $\Omega^\infty : Stab(C) \to C$ that remembers of a [[spectrum object]] the underlying object of $C$ in degree 0. Under mild conditions, notably when $C$ is a [[presentable (∞,1)-category]], this functor has a [[left adjoint]] $\Sigma^\infty : C \to Stab(C)$ that _freely stabilizes_ any given object of $C$.

Going back and forth this way yields the assignment

$$
  X \mapsto \Omega^\infty \Sigma^\infty X
$$

that may be thought of as the **stabilization of an object** $X$. 
Indeed, as the notation suggests, $\Omega^\infty \Sigma^\infty X$ may be thought of as the result as $n$ goes to infinity of the operation that forms from $X$ first the $n$-fold [[suspension object]] $\Sigma^n X$ and then from that the $n$-fold [[loop space object]].

## Definition

### Abstract definition

Let $C$ be an [[(∞,1)-category]] with finite [[limit]]s and write
$C_* := C^{{*}/}$ for its $(\infty,1)$-category of [[pointed object]]s, the
[[undercategory]] of $C$ under the [[terminal object]].


On $C_*$ there is the [[loop space object]] [[(infinity,1)-functor]] 
$\Omega : C_* \to C_*$, that sends each object $X$ to the [[pullback]] of the
point inclusion ${*} \to X$ along itself. Recall that if a $(\infty,1)$-category
is stable, the loop object functor is an equivalence.

The _stabilization_ $Stab(C)$ of $C$ is the
[[limit]] (in the [[(infinity,1)-category of (infinity,1)-categories]]) of the 
tower of applications of the loop space functor

$$
  Stab(C)
  =
  \lim(
    \cdots \to C_* \stackrel{\Omega}{\to} C_* \stackrel{\Omega}{\to} C_*
  )
  \,.
$$


This is proposition 8.14 in [StabCat](http://arxiv.org/abs/math/0608228).

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


