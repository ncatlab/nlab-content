


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

* More concretely, $\mathcal{E}$ is exponentiable if there exists a functor $(_{-})^\mathcal{E}$ such that for all toposes $\mathcal{F},\mathcal{G}$ the category $Hom(\mathcal{F}\times\mathcal{E},\mathcal{G})$ is (naturally) equivalent as a category to $Hom(\mathcal{F},\mathcal{G}^\mathcal{E})$.

* By setting $\mathcal{F}=\mathcal{S}$ , the base topos, one sees from $Hom(\mathcal{S},\mathcal{G}^\mathcal{E})=Hom(\mathcal{S}\times\mathcal{E},\mathcal{G})=Hom(\mathcal{E},\mathcal{G})$ that $\mathcal{G}^\mathcal{E}$ is indeed a "mapping space" whose [[point of a topos|points]] are the [[geometric morphism|geometric morphisms]] $\mathcal{E}\to\mathcal{G}$.

* The concept generalizes to [[higher topos theory]] (cf. [Anel 2015](#A15), [Anel-Lejay 2018](#AJ18), [Lurie 2018](#Lurie18)).

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

Exponentiability is a local property:
+-- {: .num_prop}
###### Proposition
1. If a [[Grothendieck topos]] $\mathcal{E}$ is exponentiable so is $\mathcal{E}/X$ for any object $X\in\mathcal{E}$.
2. If $\mathcal{E}/X$ is exponentiable and  $X\to 1$ is an epimorphism, then $\mathcal{E}$ is exponentiable as well.

=--

This occurs as lemma 4.2 in Johnstone-Joyal ([1982](#JJ82), p.281).

Continuity also leaves a lattice-theoretic trace:

+-- {: .num_prop}
###### Proposition
If a [[Grothendieck topos]] $\mathcal{E}$ is exponentiable then the lattice of [[subobject|subobjects]] of any object $X\in\mathcal{E}$ is [[continuous lattice|continuous]].

=--

This occurs as lemma 5.1 in Johnstone-Joyal ([1982](#JJ82), p.287).

## Examples

* Since [[locally finitely presentable categories]] are [[continuous category|continuous]] and [[coherent topos|coherent toposes]] are locally finitely presentable (cf. Johnstone ([2002, p.915](#J02))) it follows that _coherent toposes are exponentiable_. This can be viewed as an avatar of the fact that (locally) compact topological spaces behave well with respect to mapping spaces.

* By the same reasoning all functor categories $Set^{\mathcal{C}}$ for  $\mathcal{C}$ a [[small category]] are exponentiable since they are [[locally finitely presentable category|locally finitely presentable]]. This includes in particular all [[presheaf toposes]] on small categories.

* An example of the latter is the [[Sierpinski topos]] $\mathcal{S}^2$. Here the exponential $\mathcal{F}^{\mathcal{S}^2}$ classifies the [[theory of model homomorphisms|theory of $\mathbb{T}$-model homorphisms]] (with $\mathbb{T}$ the [[geometric theory]] classified by $\mathcal{F}$) i.e. the theory $\mathbb{T}^2$ such that $Mod_{\mathbb{T}^2}(\mathcal{E})=Mod_\mathbb{T}(\mathcal{E})^2$.

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

Compare also the remarks of Anel ([2015](#A15)) on the $\infty$-case.

### Examples

* Let $0$ be the [[initial topos]] that classifies the _inconsistent theory_ $\mathbb{T}^\emptyset_1$ over the empty signature. Then from $\mathcal{S}[\mathbb{O}]^0=\mathcal{S}$ follows that the _dual_ of the inconsistent theory is $\mathbb{T}_1^{\emptyset\ast}=\mathbb{T}_{\emptyset}^{\emptyset}$ with $\mathbb{T}_{\emptyset}^{\emptyset}$ the [[empty theory]] (over the empty signature).

* From $\mathcal{S}[\mathbb{O}]^\mathcal{S}=\mathcal{S}[\mathbb{O}]$ follows in turn that the _double dual_ of the inconsistent theory, or, in other words, the dual of the empty theory, is $\mathbb{T}_1^{\emptyset\ast\ast}=\mathbb{T}^{\emptyset\ast}_\emptyset=\mathbb{O}$ with $\mathbb{O}$ the [[theory of objects]]. (More generally, the dual theory of any dualizable theory is itself dualizable.)

* Let $\mathcal{S}^2$ be the [[Sierpinski topos]] that classifies [[subterminal object|subterminal objects]] or the [[localic topos|theory of completely prime filters]] of the frame of opens of the [[Sierpinski space]]. Since $\mathcal{E}\times \mathcal{S}^2\cong \mathcal{E}^2$ it follows that 
  $$\mathcal{E}^2=Hom(\mathcal{E}^2,\mathcal{S}[\mathbb{O}])=Hom(\mathcal{E}\times\mathcal{S}^2,\mathcal{S}[\mathbb{O}])= Hom(\mathcal{E},\mathcal{S}[\mathbb{O}]^{\mathcal{S}^2})=Hom(\mathcal{E},\mathcal{S}[\mathbb{O}^2])\quad ,$$
  i.e. the dual theory is the [[theory of model homomorphisms|theory of morphisms]] $\mathbb{O}^2$.

### The theory of sheaves on a coherent site

Recall, that given a small site $(\mathcal{C},J)$ there is a [[geometric theory]] $\mathbb{F}_J$ called the [[theory of flat functors|theory of J-continuous flat functors]] that (albeit uneconomically) axiomaticizes the theory classified by $Sh(\mathcal{C},J)$ using the objects and morphisms in $\mathcal{C}$ for its signature. When $Sh(\mathcal{C},J)$ is exponentiable this theory is dualizable, and, in the case the site $(\mathcal{C},J_c)$ is [[coherent site|coherent]] i. e. $\mathcal{C}$ has finite limits and $J_c$ is generated by finite covering families, the following theory $\mathbb{S}$ called **the theory of sheaves** on $(\mathcal{C},J_{c})$ axiomatizes the dual theory $\mathbb{F}_{J_{c}}^\ast$ (in an equally uneconomic way):

The signature of $\mathbb{S}$ has a type symbol $A'$ for every object $A\in\mathcal{C}$ and a function symbol $f':B'\to A'$ for every morphism $f:B\to A$ in $\mathcal{C}^{op}$. The axioms are given by the following schemata

* $\top\vdash_x i'(x)=x$ for all identity morphisms $i$.

* $\top\vdash_x f'(x)=h'(g'(x))$ for all composable triples $f=g\circ h$ in $\mathcal{C}$.

* $\bigwedge_{i=1}^{n} (\alpha_i'(x)=a_i'(x'))\vdash_{x,x'} x=x'$ for each generating finite $J_{c}$-covering family $(Y_i\overset{\alpha_i}{\to} X|i=1,\dots, n)$.

* $\bigwedge_{i,j}(\beta_{ij}'(y_i)=\gamma_{ij}'(y_j))\vdash_{y_i,y_j}\exists x\big ( \bigwedge_{i=1}^{n}\alpha_i'(x)=y_i\big )$ for each generating finite $J_{c}$-covering family $(Y_i\overset{\alpha_i}{\to} X|i=1,\dots, n)$ and pullback

  $\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad
  \array{
    Z_{ij} &\overset{\beta_{ij}}{\longrightarrow}& Y_i
    \\
    {}^{\mathllap{\gamma_{ij}}}
    \downarrow 
    & & 
    \downarrow^{\mathrlap{\alpha_i}}
    \\
    Y_j 
      &\underset{\alpha_j}{\longrightarrow}& 
    X
  }
$ $\qquad \qquad.$

The models of $\mathbb{S}$ in a Grothendieck topos $\mathcal{F}$ are "sheaves of $\mathcal{F}$-objects" on $(\mathcal{C},J_{c})$ i.e. functors $\mathcal{C}^{op}\to\mathcal{F}$ satisfying the diagrammatic form of the sheaf axioms but

$$Mod_\mathbb{S}(\mathcal{F})=\mathcal{F}\times Sh(\mathcal{C},J_{c})=Hom(\mathcal{F}\times Sh(\mathcal{C},J_{c}), \mathcal{S}[\mathbb{O}])=Hom(\mathcal{F},\mathcal{S}[\mathbb{O}]^{Sh(\mathcal{C},J_{c})})$$

i.e. $\mathcal{S}[\mathbb{O}]^{Sh(\mathcal{C},J_{c})}$ is the classifying topos for $\mathbb{S}$. (For the details cf. Johnstone [1977](#J77), p.248f).
 
In particular, since $\mathbb{S}$ is a [[coherent logic|coherent theory]] this implies that $\mathcal{S}[\mathbb{O}]^{Sh(\mathcal{C},J_{c})}$ is also a [[coherent topos]]. From 

$$Hom(\mathcal{S},\mathcal{S}[\mathbb{O}]^{Sh(\mathcal{C},J_{c})})=Mod_\mathbb{S}(\mathcal{S})=\mathcal{S}\times {Sh(\mathcal{C},J_{c})}=Sh(\mathcal{C},J_c)$$

it follows then that every coherent topos $Sh(\mathcal{C},J_c)$ is the _category of points_ of a coherent topos.

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

* [[cartesian closed 2-category]]

* [[convenient category of spaces]]

* [[Verdier duality]]

## References

* [[Mathieu Anel]], _Toposes are commutative rings_ , talk at _[Topos &#224; l'IHES](https://indico.math.cnrs.fr/event/747/)_,  IHES Paris, Nov. 25-27, 2015 ([video recording](https://www.youtube.com/watch?v=wG5MZqj_JK8), at min 52:47 ff.).

* [[Mathieu Anel]], Damien Lejay, _Exponentiable Higher Toposes_ , arXiv:1802.10425 (2018). ([abstract](https://arxiv.org/abs/1802.10425))

* {#Blass84}[[Andreas Blass]], _The interaction of category theory and set theory_ , Cont. Math. **30** (1984) pp.5-29. ([draft](http://www.math.lsa.umich.edu/~ablass/interact.pdf))

* {#Hyland81}[[Martin Hyland]], _Function spaces in the category of locales_ , Springer LNM **871** (1981) pp.264-281.

* {#J77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Also available as Dover reprint Mineola 2014; pp.209-210, 248-249)

* {#J02}[[Peter Johnstone]], _Sketches of an Elephant vols. 1&2_ , CUP 2002. (sections B4.3 pp.432-438, C4.4 pp.745-754)

* {#JJ82}[[Peter Johnstone]], [[André Joyal]], _Continuous categories and exponentiable toposes_ ,  JPAA **25** (1982) pp.255-296.

* {#Lurie18}[[Jacob Lurie]], _Spectral Algebraic Geometry_ , ms. Harvard University 2018. (section 21.1.6)

* [[Susan Niefield]], _Exponentiable Morphisms: posets, spaces, locales and Grothendieck toposes_ , TAC **8** (2001) pp.16-32. ([abstract](http://www.tac.mta.ca/tac/volumes/8/n2/8-02abs.html))

* [[Myles Tierney]], _Forcing Topologies and Classifying Toposes_ , pp.211-219 in Heller, Tierney (eds.), _Algebra, Topology and Category Theory_  , Academic Press New York 1976. (p.211, 218)

[[!redirects Exponentiable topos]]
[[!redirects exponential topos]]