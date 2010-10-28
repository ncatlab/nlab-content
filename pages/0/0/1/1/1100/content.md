
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Recall the following familiar 1-categorical statement:

* Working in the 1-[[category]] [[Set]] of [[0-category|0-categories]] is the same as  doing [[set theory]]. The point of [[sheaf topos|sheaf]] [[toposes]] is to pass to _parameterized_  [[0-category|0-categories]], namely  [[presheaf]] categories: these [[topos|topoi]] behave much like the category [[Set]] but their objects are generalized  [[spaces]] that may carry 
more structure, for instance they may be [[generalized smooth space]]s if one considers (pre)[[sheaf|sheaves]] on [[Diff]].

One can think of $(\infty,1)$-toposes as the generalization of the above situation from $1$ to $(\infty,1)$  (recall the notion of [[(n,r)-category]] and see the general discussion at [[∞-topos]]):

* Working in the [[(∞,1)-category]] [[∞Grpd]] of [[infinity-groupoid|(∞,0)-categories]] is the same as  doing [[homotopy theory]]. The point of 
[[(∞,1)-sheaves]] is to pass to _parameterized_ [[(∞,0)-categories]], namely  [[(∞,1)-presheaf]] categories: 
these [[(∞,1)-topoi]] behave much like the $(\infty,1)$-category 
[[∞Grpd]] but their objects are generalized  [[spaces]]  with higher [[homotopies]] that may carry  more structure, for instance they may
be [[∞-Lie groupoid]]s if one considers [[(∞,1)-sheaves]] on [[CartSp]].

## Definition {#Definition}

### As a geometric embedding into a $(\infty,1)$-presheaf category

A [[Alexander Grothendieck|Grothendieck]]--[[Charles Rezk|Rezk]]--[[Jacob Lurie|Lurie]] **$(\infty,1)$-topos** $\mathbf{H}$ is an [[accessible (∞,1)-functor|accessibly embedded]] [[reflective sub-(∞,1)-category]] of an [[(∞,1)-category of (∞,1)-presheaves]]

$$
  \mathbf{H}
  \stackrel{\overset{lex}{\leftarrow}}{\hookrightarrow}
  PSh_{(\infty,1)}(C)
  \,.
$$

If this is a [[topological localization]] then $\mathbf{H}$ is an [[(∞,1)-category of (∞,1)-sheaves]].

### By $(\infty,1)$-Giraud's axioms {#GiraudAxioms}

Equivalently: an $(\infty,1)$-topos $\mathbf{H}$ is

an [[(∞,1)-category]] that satisfies the $(\infty,1)$-categorical analogs of [[Giraud's axioms]]:

* $\mathbf{H}$ is [[presentable (infinity,1)-category|presentable]];
* [[limit in quasi-categories|(∞,1)-colimits]] in $\mathbf{H}$ [[universal colimits|are universal]];
* [[coproduct]]s in $\mathbf{H}$ are [[disjoint coproduct|disjoint]];
* every [[groupoid object in an (infinity,1)-category|groupoid object]] in $\mathbf{H}$ is [[quotient object|effective]] (i.e. has a [[delooping]]). 

The equivalence of these two characterizations is one of the main theorems of [[Higher Topos Theory|HTT]].

This is derived from the following equivalent one:

an [[(∞,1)-topos]] is

* a [[presentable (∞,1)-category]]

* with [[universal colimits]]

* and with [[object classifier]]s.

### Morphism

A [[morphism]] between $(\infty,1)$-toposes is an [[(∞,1)-geometric morphism]].

The [[(∞,1)-category]] of all $(\infty,1)$-topos is [[(∞,1)Toposes]].

## Types of $(\infty,1)$-toposes

### Topological localizations / $(\infty,1)$-sheaf toposes

for the moment see

* [[topological localization]]

### Hypercomplete $(\infty,1)$-toposes

for the moment see 

* [[hypercomplete (∞,1)-topos]]

## Models 

Another main theorem about $(\infty,1)$-toposes is that
[[models for ∞-stack (∞,1)-toposes]] are given by the [[model structure on simplicial presheaves]]. See there for details

## Properties

### Over-$(\infty,1)$-toposes

**Proposition**

For $\mathbf{H}$ an $(\infty,1)$-topos and $X \in \mathbf{H}$ an object, the [[over-(∞,1)-category]] $\mathbf{H}_{/X}$ is itself an $(\infty,1)$-topos -- an **[[over-(∞,1)-topos]]**. The projection $\pi_! : \mathbf{H}_{/X} \to \mathbf{H}$ part of an  [[essential geometric morphism]]

$$
  \pi : \mathbf{H}_{/X} 
  \stackrel{\overset{\pi_!}{\to}}{\stackrel{\overset{\pi^*}{\leftarrow}}{\underset{\pi_*}{\to}}}
  \mathbf{H}
  \,.
$$

This is [[Higher Topos Theory|HTT, prop. 6.3.5.1]].

The $(\infty,1)$-topos $\mathbf{H}_{/X}$ could be called the [[gros topos]] of $X$. A [[geometric morphism]] $\mathbf{K} \to \mathbf{H}$ that factors as $\mathbf{K} \to \mathbf{H}_{/X} \stackrel{\pi}{\to} \mathbf{H}$ is called an [[etale geometric morphism]].




## $(\infty,1)$-Topos theory {#ToposTheory}

Most of the standard constructions in [[topos theory]] have or should have  immediate generalizations to the context of $(\infty,1)$-toposes, since all notions of [[category theory]] exist for [[(∞,1)-categories]].

For instance there are evident notions of

* [[geometric morphism]]s between $(\infty,1)$-toposes, such as the [[global section]] geometric morphism to the [[terminal object|terminal]] [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf]] $(\infty,1)$-topos [[? Grpd]].

Moreover, it turns out that $(\infty,1)$-toposes come with plenty of internal structures, more than canonically present in an ordinary topos. 
Every $(\infty,1)$-topos comes with its intrinsic notion of

* [[cohomology|cohomology in an (∞,1)-topos]]

and with an intrinsic notion of

* [[homotopy groups in an (∞,1)-topos|homotopy in an (∞,1)-topos]].


In classical topos theory, cohomology and homotopy of a topos $E$ are defined in terms of [[simplicial object]]s in $C$. If $E$ is a [[sheaf topos]] with [[site]] $C$ and [[point of a topos|enough point]]s, then  this classical construction is secretly really a model for the intrinsic cohomology and homotopy in the above sense of the  [[hypercomplete (∞,1)-topos]] of [[∞-stack]]s on $C$.

The beginning of a list of all the structures that exist intrinsically in an $(\infty,1)$-topos is at

* [[schreiber:structures in an (∞,1)-topos]].

But **$(\infty,1)$-topos theory** in the style of an $\infty$-analog of the [[Elephant]] is only barely beginning to be conceived. 

There are some indications as to what the

* [[internal logic of an (∞,1)-topos]]

should be.


## Related concepts

* [[(0,1)-topos]]

* [[topos]]

* [[2-topos]]

* **$(\infty,1)$-topos**



## References

### General

In retrospect it turns out that the [[homotopy category of an (∞,1)-category|homotopy categories]] of [[(∞,1)-topos]]es have been known since

* [[Kenneth Brown]], _[[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]_ .

And the [[model category]] theory models have been known since [[Andre Joyal]] proposed the [[model structure on simplicial sheaves]] in his letter to [[Alexander  Grothendieck]].

This work used 1-categorical [[site]]s. The generalization to [[(∞,1)-category|(∞,1)categorical sites]] -- modeld by [[model site]]s -- was discussed in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry I: Topos theory_ ([arXiv](http://arxiv.org/abs/math.AG/0207028))

and "model topos"-theory was also developed in

* [[Charles Rezk]], _Toposes and homotopy toposes_ ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))

The intrinsic [[higher category theory|category-theoretic]] definition of an [[(∞,1)-topos]] was given in section 6.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

building on ideas by [[Charles Rezk]]. There is is also proven that the Brown-Joyal-Jardine-To&#235;n-Vezzosi models indeed precisely model $\infty$-stack $(\infty,1)$-toposes. Details on this relation are at [[models for ∞-stack (∞,1)-toposes]].


### $\infty$-Giraud axioms

A discussion of the $(\infty,1)$-[[universal colimits]] in terms of [[model category]] presentations is due to

* [[Charles Rezk]], _Fibrations and homotopy colimits of simplicial sheaves_ ([pdf](http://www.math.uiuc.edu/~rezk/rezk-sharp-maps.pdf))

More on this with an eye on [[associated ∞-bundle]]s is in 

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_ ([arXiv](http://arxiv.org/abs/1009.2930))

[[!redirects (infinity,1)-topoi]]
[[!redirects (infinity,1)-toposes]]
[[!redirects (∞,1)-topos]]
[[!redirects (∞,1)-topoi]]
[[!redirects (∞,1)-toposes]]