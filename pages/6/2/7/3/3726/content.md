
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea

An **$n$-connected object** is an object all whose [[homotopy group]]s _equal to or below_ degree $n$ are trivial.

More precisely, an object in an [[∞-stack]] [[(∞,1)-topos]] is $n$-connected if its [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] equal to or below degree $n$ are trivial.

The complementary notion is that of an [[n-truncated object of an (∞,1)-category]].

The [[Whitehead tower]] construction produces $n$-connected objects.


## Definition

+-- {: .un_defn}
###### Definition

An [[object]] $X$ in an [[(∞,1)-topos]] $\mathbf{H}$ is called **$n$-connected** for $n \in \mathbb{N}$ if

1. the [[terminal object|terminal]] morphism $X \to *$ is an [[effective epimorphism]];

1. all [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]]
   equal to or below degree $n$ are trivial.

   $$
     \pi_k(X) = * \;\;\; for k \leq n
     \,.
   $$
  
A [[morphism]] $f : X \to Y$ in an $(\infty,1)$-topos is $n$-connected if 

1. it is an [[effective epimorphism]]

1. regarded as an object in the 
   [[over quasi-category|over-(∞,1)-category]] 
   $\mathbf{H}_{/Y}$ all [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]]
   equal to or below degree $n$ are trivial.
=--

By convention every object is $(-2)$-connected.

This appears as [[Higher Topos Theory|HTT, def. 6.5.1.10]], but under the name "$(n+1)$-connective".  Another possible term is "$n$-simply connected"; see [[n-connected space]] for discussion.


## Properties

+-- {: .un_prop}
###### Proposition

An object $X$ is $n$-connected (for $n \geq -2$) precisely if its [[n-truncated object in an (∞,1)-category|n-truncation]] $\tau_{\leq n} X$ is [[generalized the|the]] [[terminal object]] of $\mathbf{H}$.
=--

This is [[Higher Topos Theory|HTT, prop. 6.5.1.12]].


+-- {: .un_lemma}
###### Observation

Every [[equivalence in a quasi-category|equivalence]] is $\infty$-connected.
=--

This is [[Higher Topos Theory|HTT, prop. 6.5.1.16, item 2]].

+-- {: .un_remark}
###### Remark

In a general $(\infty,1)$-topos the converse is not true: not every $\infty$-connected morphisms needs to be an equivalence. It is true in a [[hypercomplete (∞,1)-topos]].
=--


+-- {: .un_prop}
###### Proposition

The class of $n$-connected morphisms is stable under [[pullback]] and [[pushout]].

If the pullback of a morphism along an [[effective epimorphism]] is $n$-connected, then so is the original morphism.
=--

This is [[Higher Topos Theory|HTT, prop. 6.5.1.16, item 6]].


## Examples

### In $Top$

In the the [[(∞,1)-category]] [[Top]] we have that an object is $n$-connected precisely if it is an [[n-connected topological space]]:

* a $(-1)$-connected object is an [[inhabited set|inhabited space]].

* a $0$-connected object is a [[path-connected space]].

* a $1$-connected object is a [[simply connected space]].

* a $\infty$-connected object is a [[contractible space]].


[[!redirects n-connected object]]
[[!redirects n-connected objects]]
[[!redirects n-connected]]
[[!redirects n-simply connected object]]
[[!redirects n-simply connected objects]]

[[!redirects n-connective object]]
[[!redirects n-connective objects]]
[[!redirects n-connective]]

[[!redirects n-connected object in an (∞,1)-topos]]
[[!redirects n-connected object in an (infinity,1)-topos]]


[[!redirects n-connected object of an (∞,1)-topos]]
[[!redirects n-connected objects of an (∞,1)-topos]]
[[!redirects n-connected objects of (∞,1)-toposes]]
[[!redirects n-connected objects of (∞,1)-topoi]]
[[!redirects n-connected object of an (infinity,1)-topos]]
[[!redirects n-connected objects of an (infinity,1)-topos]]
[[!redirects n-connected objects of (infinity,1)-toposes]]
[[!redirects n-connected objects of (infinity,1)-topoi]]
[[!redirects n-simply connected object of an (∞,1)-topos]]
[[!redirects n-simply connected objects of an (∞,1)-topos]]
[[!redirects n-simply connected objects of (∞,1)-toposes]]
[[!redirects n-simply connected objects of (∞,1)-topoi]]
[[!redirects n-simply connected object of an (infinity,1)-topos]]
[[!redirects n-simply connected objects of an (infinity,1)-topos]]
[[!redirects n-simply connected objects of (infinity,1)-toposes]]
[[!redirects n-simply connected objects of (infinity,1)-topoi]]

[[!redirects n-connected object of an (∞,1)-category]]
[[!redirects n-connected objects of an (∞,1)-category]]
[[!redirects n-connected objects of (∞,1)-categories]]
[[!redirects n-connected object of an (infinity,1)-category]]
[[!redirects n-connected objects of an (infinity,1)-category]]
[[!redirects n-connected objects of (infinity,1)-categories]]
[[!redirects n-simply connected object of an (∞,1)-category]]
[[!redirects n-simply connected objects of an (∞,1)-category]]
[[!redirects n-simply connected objects of (∞,1)-categories]]
[[!redirects n-simply connected object of an (infinity,1)-category]]
[[!redirects n-simply connected objects of an (infinity,1)-category]]
[[!redirects n-simply connected objects of (infinity,1)-categories]]
