


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
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

An **exponentiable topos** is a generalization of the notion of an exponentiable [[locale]] and can be viewed as a (topological) "space" $X$ that behaves well with respect to the construction of mapping spaces $Y^X$. 

## Definition

+-- {: .num_defn}
###### Definition
A [[Grothendieck topos]] $\mathcal{E}$ is called _exponentiable_ (in the [[2-category]] of Grothendieck toposes $GrTop$) if the 2-functor ${}_{-}\times\mathcal{E}$ has a right 2-adjoint $(_{-})^\mathcal{E}$.
=--

## Remarks

* More concretely, $\mathcal{E}$ is exponentiable if there exists a functor $(_{-})^\mathcal{E}$ such that for all toposes $\mathcal{F},\mathcal{G}$ $Hom(\mathcal{F}\times\mathcal{E},\mathcal{G})$ is (naturally) equivalent as a category to $Hom(\mathcal{F},\mathcal{G}^\mathcal{E})$.

* The concept generalizes to [[higher topos theory]] (cf. [Anel-Lejay 2018](#AJ18), [Lurie 2018](#Lurie18)).

## Properties

Interestingly, in the category of locales exponentiability of a locale $X$ hinges on the existence of the single exponential $S^X$ where $S$ is the [[Sierpinski space]]: $Y^X$ exists for all $Y$ iff $S^X$ exists.

In $GrTop$ the [[classifying topos for the theory of objects|object classifier]] $\mathcal{S}[\mathbb{O}]$ takes over the role of the Sierpinski space and we have the following

+-- {: .num_prop}
###### Proposition
A [[Grothendieck topos]] $\mathcal{E}$ is exponentiable iff the [[exponential object|exponential]] $\mathcal{S}[\mathbb{O}]^\mathcal{E}$ exists.

=--

This result is due to Johnstone-Joyal ([1982](#JJ82), p.282) and occurs as theorem 4.3.1 of Johnstone ([2002, vol.1 p.433](#J02)).


The following theorem pursues this analogy and generalizes a result of [[Martin Hyland]] on locales ([1981](#Hyland81)).

+-- {: .num_prop}
###### Theorem
A [[Grothendieck topos]] $\mathcal{E}$ is an exponentiable object in the 2-category of Grothendieck toposes and [[geometric morphisms]] iff $\mathcal{E}$ is a [[continuous category]].

=--

This result is due to Johnstone-Joyal ([1982](#JJ82)) and occurs as theorem 4.4.5 of Johnstone ([2002, p.748](#J02)).

## Examples

* Since [[locally finitely presentable categories]] are [[continuous category|continuous]] and [[coherent topos|coherent toposes]] are locally finitely presentable (cf. Johnstone ([2002, p.915](#J02))) it follows that _coherent toposes are exponentiable_. This can be viewed as an avatar of the fact that (locally) compact topological spaces behave well with respect to mapping spaces.

* By the same reasoning all functor categories $Set^{\mathcal{C}}$ for  $\mathcal{C}$ a [[small category]] are exponentiable since they are [[locally finitely presentable category|locally finitely presentable]]. This includes in particular all [[presheaf toposes]] on small categories.

##Remarks on duality

It is worthwhile to muse a bit about $\mathcal{S}[\mathbb{O}]^\mathcal{E}$: 

First of at all, it is [[injective topos|injective]] since $\mathcal{S}[\mathbb{O}]$ is injective and $(_-)^\mathcal{E}$ preserves inclusions.

This and the various universal properties of the toposes involved imply that an exponentiable topos 
$$\mathcal{E}\cong Hom(\mathcal{E},\mathcal{S}[\mathbb{O}])\cong Hom(\mathcal{S}\times\mathcal{E},\mathcal{S}[\mathbb{O}])\cong Hom(\mathcal{S},\mathcal{S}[\mathbb{O}]^\mathcal{E})$$
is (up to equivalence) the _category of points of an injective topos_.

Now consider an arbitrary topos $\mathcal{E}$ classifying a geometric theory $\mathbb{T}$.

Then from the [[geometric theory#FunctorialDefinition|functorial perspective on logic]] the 2-functor $\mathbb{T}^*:GrTop^{op}\to CAT$ assigning to $\mathcal{F}$ the category of models $\mathbb{T}^*(\mathcal{F}):=\mathcal{F}\times\mathcal{E}=\mathcal{F}\times\mathcal{S}[\mathbb{T}]$ is called the **dual theory** of $\mathbb{T}$.

It need not be geometric i.e. have a [[classifying topos]] but when it is, $\mathbb{T}$ being called _dualizable_ in that case, the following

$$\mathbb{T}^*(\mathcal{F})=\mathcal{F}\times\mathcal{E}\cong Hom(\mathcal{F}\times\mathcal{E},\mathcal{S}[\mathbb{O}])\cong Hom(\mathcal{F},\mathcal{S}[\mathbb{O}]^\mathcal{E})$$

shows that $\mathcal{S}[\mathbb{O}]^\mathcal{E}$ has precisely the properties required for $\mathcal{S}[\mathbb{T}^*]$.

In other words, $\mathbb{T}^*$ is geometric (and classified by $\mathcal{S}[\mathbb{O}]^\mathcal{E}$) precisely iff $\mathcal{E}=\mathcal{S}[\mathbb{T}]$ is exponentiable! 

### Example

Let $0$ be the [[initial topos]] that classifies the _inconsistent theory_ $\mathbb{T}^\emptyset_1$ over the empty signature. Then from $\mathcal{S}[\mathbb{O}]^0=\mathcal{S}$ follows that the _dual_ of the inconsistent theory is $\mathbb{T}_1^{\emptyset\ast}=\mathbb{T}_{\emptyset}^{\emptyset}$ with $\mathbb{T}_{\emptyset}^{\emptyset}$ the [[empty theory]] (over the empty signature).

From $\mathcal{S}[\mathbb{O}]^\mathcal{S}=\mathcal{S}[\mathbb{O}]$ follows in turn that the _double dual_ of the inconsistent theory, or, in other words, the dual of the empty theory, is $\mathbb{T}_1^{\emptyset\ast\ast}=\mathbb{T}^{\emptyset\ast}_\emptyset=\mathbb{O}$ with $\mathbb{O}$ the [[theory of objects]].


## Ramifications

The notion of a [[tiny object]] in a cartesian closed category suggests the following

+-- {: .num_defn}
###### Definition
An exponentiable Grothendieck topos $\mathcal{E}$ is called _tiny_ (or _infinitesimal_) if the 2-functor $(_{-})^\mathcal{E}$ has a right 2-adjoint $(_{-})_\mathcal{E}$.
=--


## Related entries

* [[exponential object]]

* [[continuous category]]

* [[reflexive object]]

* [[injective topos]]

* [[ind-object]]

* [[classifying topos for the theory of objects]]

* [[convenient category of spaces]]

## References

* [[Mathieu Anel]], Damien Lejay, _Exponentiable Higher Toposes_ , arXiv:1802.10425 (2018). ([abstract](https://arxiv.org/abs/1802.10425))

* {#Blass84}[[Andreas Blass]], _The interaction of category theory and set theory_ , Cont. Math. **30** (1984) pp.5-29. ([draft](http://www.math.lsa.umich.edu/~ablass/interact.pdf))

* {#Hyland81}[[Martin Hyland]], _Function spaces in the category of locales_ , Springer LNM **871** (1981) pp.264-281.

* {#JJ82}[[Peter Johnstone]], [[André Joyal]], _Continuous categories and exponentiable toposes_ ,  JPAA **25** (1982) pp.255-296.

* {#J02}[[Peter Johnstone]], _Sketches of an Elephant vols. 1&2_ , CUP 2002. (sections B4.3 pp.432-438, C4.4 pp.745-754)

* {#Lurie18}[[Jacob Lurie]], _Spectral Algebraic Geometry_ , ms. Harvard University 2018. (section 21.1.6)

* [[Susan Niefield]], _Exponentiable Morphisms: posets, spaces, locales and Grothendieck toposes_ , TAC **8** (2001) pp.16-32. ([abstract](http://www.tac.mta.ca/tac/volumes/8/n2/8-02abs.html))

[[!redirects Exponentiable topos]]
[[!redirects exponential topos]]