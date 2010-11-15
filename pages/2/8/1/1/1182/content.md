
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
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

#Introduction#

This entry is about the work by David Ben-Zvi, John Francis and David Nadler on application of a [[(infinity,1)-category|(∞,1)-categorical]] realization of [[geometric function theory]] to [[FQFT|extended quantum field theory]] in the context in which Jacob Lurie proved the [[generalized tangle hypothesis|cobordism hypothesis]].

So far this work is presented in the two articles

* **IntTrans** [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral transforms and Drinfeld Centers in Derived Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))

* **CharTheo** [[David Ben-Zvi]], [[David Nadler]], _The Character Theory of a Complex Group_ ([arXiv](http://arxiv.org/abs/0904.1247))



+-- {: .query}

This entry is supposed to be the $n$Lab-working area for a " Journal Club -- Geometric $\infty$-function theory ". The corresponding discussion page at the $n$-Caf&#233; is [Journal Club -- Geometric ∞-Function Theory](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html)

The idea is to 

* jointly discuss at the $n$Caf&#233; section-by-section these articles; to get an idea for what's going on;

* add here, step by step, links to keywords appearing in these sections, and create the corresponding entries describing them.

* This is supposed to be a recursive and iterative process, which, if successful, will eventually create here a useful repository of entries that describe and explain the various aspects of the topic.

=--

#Basic idea in three words#

Geometric $\infty$-function theory is about the [[∞-categorification]] of the following basic fact of [[matrix calculus]]: for $X$ and $Y$ finite sets, for $k$ a field and for $C(X)$ and $C(Y)$ the $k$-vector spaces of $k$-valued functions on $X$ and $Y$, respectively, we have natural isomorphisms

$$
  C(X) \otimes C(Y)
  \simeq
  C(X \times Y)
  \simeq
  LinMap(C(X), C(Y))
  \simeq
  C(X)^* \otimes C(Y)
$$

of finite-dimensional vector spaces.

In geometric $\infty$-function theory one replaced the finite sets here with generalized spaces called [[perfect infinity-stack|perfect]] [[derived stacks]], and $k$-valued functions by something like $k$-vector bundles on these.

That's it, essentially. The point is that this simple statement then turns out to be a powerful organization and unification tool for lots of structures appearing in [[representation theory]] and [[FQFT|functorial quantum field theory]].

# Timeline #

We will try to proceed as follows: we go through the sections of the two articles, step by step, possibly several steps for one section. Each week on Monday, one of us produces a "report" on the section he or she was assigned to read. 

This "report" would try to give a rough idea of what is going on in a given section. A report may be anything from a  heap of questions (likely) to a complete detailed rederivation of all the details (maybe not quite as likely, but let's not exclude it!) The more questions, the more we all get involved, which is the whole point of doing this online.

I ([[Urs Schreiber|Urs]]) am imagining that whatever the report is like, it consists of 

* a bulleted list of whatever needs to be listed, with links to whatever deserves to be linked to, here in this $n$Lab-entry, in the following list of sections;

* a comment to the [blog entry](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html) that maybe copies this entire content but at least alerts the blog readers about the new material now to be found here, accompanied by some comments as seems necessary.

The idea is that we have discussion on the blog but distill whatever we can into the $n$Lab here.


Here is the list of reports, as planned so far:

* Monday, April 27: [[Alex Hoffnung|Alex]] on section 1, [Introduction](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=2) [[tick6.png:pic]] ([n-category caf&#233; entry](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit_1.html))

* Monday, May 4: [[Urs Schreiber|Urs]] on section 2, [Preliminaries](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=10) [[tick6.png:pic]] ([n-category caf&#233; entry](http://golem.ph.utexas.edu/category/2009/05/journal_club_geometric_infinit_2.html))

* Monday, May 11: [[Bruce Bartlett|Bruce]] on section 3, [Perfect Stacks](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=16) [[tick6.png:pic]] ([n-category caf&#233; entry](http://golem.ph.utexas.edu/category/2009/05/journal_club_geometric_infinit_3.html))

* Monday, May 18: [[Chris Brav|Christopher]] on section 4, [Tensor products and integral transforms](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=24) [[tick6.png:pic]]  ([n-category caf&#233; entry](http://golem.ph.utexas.edu/category/2009/05/journal_club_geometric_infinit_4.html))

* Monday, May 25: [[Chris Brav|Christopher]] on section 5, [Applications](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=32) [[tick6.png:pic]]

* Monday, June 1: [[Alex Hoffnung|Alex]] on section 6, [Epilogue: TFT](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=39)



#Idea#

The central structural theorem of [[FQFT|TQFT]], the [[generalized tangle hypothesis|cobordism theorem]] states that [[FQFT|(∞,n)-categorical extended topological quantum field theories]] are entirely determined by their value in the [[point]], which has to be an [[object]] in an [[(∞,n)-category]] with high dualizability properties.

Very generally, the point of _geometric $\infty$-function theory_ is to construct and study concrete realizations of the [[FQFTs]] guaranteed to exist by this theorem.

The central tool, from which this entry draws its title, is an [[(infinity,1)-category|(∞,1)-categorical]] version of [[geometric function theory]]: 

the rough idea is that the data the [[FQFT]] assigns to a [[manifold]] $\Sigma$ is a collection $Z(\Sigma)$ of $\infty$-functions -- the physical _fields_ -- on $\Sigma$, or, more generally, sections of some $\infty$-bundle on $\Sigma$, and that the morphism $Z(\Sigma) : Z(\Sigma_{in}) \to Z(\Sigma_{out})$ assigned by the [[FQFT]] to a [[cobordism]] $\Sigma : \Sigma_{in} \to \Sigma_{out}$
is obtained from a [[groupoidification|pull-push-operation]] on the objects of $Z(\Sigma_{in})$ through a [[span]] to obtain objects in $Z(\Sigma_{out})$.

This picture arises  naturally and is maybe best understood in terms of [[FQFTs]] that arise as [[∞-models]], namely which are [[representable functor|represented]] by a _target space_ object $P$:

assume that $P$ is some kind of generalized space (which will usually mean: an [[(∞,1)-sheaf]], see [[motivation for sheaves, cohomology and higher stacks]] for motivation of this point) and regard the manifolds $\Sigma$ as special cases of generalized manifolds.

Writing $[- , P]$ for the [[closed monoidal category|internal hom]] in the given context, every [[cobordism]] [[cospan]] is sent to a [[span]]

$$
  [-, P]
  : 
  \left(
  \array{
    && \Sigma
    \\
    & \nearrow && \nwarrow
    \\
    \Sigma_{in} &&&& \Sigma_{out}
  }
  \right)
  \mapsto
  \left(
  \array{
    && [\Sigma, P]
    \\
    & {}^{p_1}\swarrow && {}^{p_2}\searrow
    \\
    [\Sigma_{in}, P] &&&& [\Sigma_{out}, P]
  }
  \right)  
  \,.
$$

If now $C([\Sigma_{in},P])$ denotes some sensible collection of $\infty$-functions on the mapping space $[\Sigma_{in}, P]$, there will be an [[(infinity,1)-category|∞-categorical]] pull-push operation

$$
  \int_{p_2} p_1^*(-) : C([\Sigma_{in}, P]) \to C([\Sigma_{out}, P])
$$

generalizing the analogous operation as described as [[groupoidification]].

As described at [[geometric function theory]], such pull-push operations can naturally be regarded as vast generalization of familiar [[matrix calculus]], including in particular operations like Fourier--Mukai transformations.


## Summary ##

In __IntTrans__ the basic machinery of these $\infty$-categorical pull-push operations is established.

In _CharTheo_ the particular case of an [[FQFT]] is considered whose defining assigment to the [[point]] is the differential graded Hecke category

$$
  H_G = D( B  \backslash (G/B))
$$ 

of $B$-equivariant D-modules on the flag variety $G/B$ of a complex reductive group $G$ with Borel subgroup $B$.

(... more to say here ...)


# Keyword list #

The following is supposed to going to be a list of linked keywords corresponding section-by-section to the Ben-Zvi/Francis/Nadler articles above. 


## Integral Transforms ##

### 1. Introduction ###

+-- {: .query}
[[Alex Hoffnung|I]] am going to use this space (the introduction) as my sandbox and a place to begin a conversation on things I want to talk about it.  This way things do not muck up areas that Urs and others have made nice and they can be transported to the appropriate areas later.

* Drinfeld centers

Comment by David Ben-Zvi from [n-category cafe](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit_1.html#c023524)

>One quick comment: the Drinfeld center is not a "sub" in any reasonable sense (except in the loose sense that it's a categorical limit). This is easy to see already for the category of representations of a finite group, where the Drinfeld center (or modules for the Drinfeld double) is the category of G-equivariant vector bundles on the group G (I think they also go by the name Yetter-Drinfeld modules?) Likewise the center of a ring in the derived world (ie Hochschild cohomology) is not really a subring - even for a commutative ring, its derived center doesn't map in injectively (for a smooth commutative ring the Hochschild-Kostant-Rosenberg theorem tells us that Hochschild cohomology is the exterior algebra on derivations of the ring). I think we have to abandon the notions of sub and quotient in the homotopical world and stick to notions like (homotopy) limit and colimit.

I want to start replying to/understanding this comment.  I have some reading to do first so I will just leave this query box as is for now.
=--

#### 1.1 Perfect stacks ####

* [[ind-object]]

  * [[ind-object in an (∞,1)-category]]

  * [[compact object]]


#### 1.2 Tensors and functors ####

* [[geometric function theory]]

* [[groupoidification]]


#### 1.3 Centers and traces ####

* [[span trace]]

* [[co-span co-trace]]

* [[loop space object]]

  * [[homotopy limit]]

#### 1.4 Hecke categories ####

#### 1.5 Topological  field theory ####

* [[FQFT]]

* [[∞-model]]


### 2. Preliminaries ###

Recall that the goal of **geometric $\infty$-function theory** is

* to establish a good [[higher category theory|higher categorical]] version of linear algebra ("[[integral transform]]" = "higher matrix multiplication"!)

* such that interesting classes of [[∞-model]] [[FQFT|extended TQFTs]] $Z_P$ are [[representable functor|represented]] by [[motivation for sheaves, cohomology and higher stacks|generalized spaces]] $P$ 

  * in that the "higher linear map" $Z_P(\Sigma)$ assigned by the [[FQFT|QFT]] to a [[cobordism]] [[cospan]] $\array{ && \Sigma \\ & \nearrow && \nwarrow \\ \Sigma_{in} &&&& \Sigma_{out}}$ is given by the [[span]] $\array{ && [\Sigma,P] \\ & \swarrow && \searrow \\ [\Sigma_{in},P] &&&& [\Sigma_{out}, P]}$.

This clearly requires that

* we fix a good ambient context of [[Higher Topos Theory|higher sheaf- and category theory]];

* and inside that a good general concept of [[higher algebra]].

One point made by the [[David Ben-Zvi|Ben-Zvi]]/Francis/Nadler work is that a good working context of [[higher category theory]] in which a good notion of _geometric $\infty$-function theory_ can be set up nicely is the context assembled and developed in the PhD thesis of [[Jacob Lurie]], consisting of

* [[Higher Topos Theory]] -- the theory of [[(∞,1)-categories]] and [[(∞,1)-sheaves]]

  * this assembles and develops 

    * work by [[Andre Joyal]] on [[quasi-category|quasi-categories]];

    * work by Simpson, Rezk, To&#235;n, Vezzosi and others on [[higher category theory|higher categories]] and [[infinity-stack|higher stacks]];

    * work by [[BrownAHT|Brown]], [[Andre Joyal|Joyal]], Jardine and others on [[presentable (infinity,1)-category|models]] for [[∞-stacks]] in terms of a [[model structure on simplicial presheaves]].

* [[Stable Infinity-Categories|Stable Higher Category Theory]] -- essentially the theory of [[additive and abelian categories]] lifted to the $(\infty,1)$-context;

  * which puts the large body of work on [[homotopy theory|stable homotopy theory]] and [[homological algebra]] into the above [[(infinity,1)-category|(∞,1)-categorical]] context, in essence identifying the abstract idea modeled by [[pretriangulated dg-category|pretriangulated dg-categories]] and $A_\infty$-[[A-∞-categories|categories]]

* [[higher algebra|Higher Algebra]] -- the theory of [[monoid]]- or [[algebra]]-objects [[internalization|internal to]] ([[symmetric monoidal (infinity,1)-category|symmetric]]) [[monoidal (infinity,1)-category|monoidal]] [[(infinity,1)-category|(∞,1)-categories]]

  * expanding on work by To&#235;n-Vezzosi;

  * which puts into its natural higher categorical context

    * the "brave new algebra" of [[commutative ring spectrum|ring spectra]];

    * the notions of things like [[A∞-rings]] and [[symmetric monoidal category|E∞-category]].

Especially for the newcomer and non-expert it must be understood that the plethora of high-powered terminology appearing here is conceptually _simplified_ and unified by their description in the higher categorical context -- so you _gain_ by trying to learn this stuff here first before going into the standard literature:

* the concept of an [[(∞,1)-sheaf]]/[[∞-stack]] is _much simpler_ than its model in terms of the [[model structure on simplicial presheaves]];

* the concept of a [[stable (∞,1)-category]] is _much simpler_ than its 1-categorical shadow as a [[triangulated category]];

* the concept of a [[commutative algebra in an (∞,1)-category]] is _simpler_ than the details of its realization given by a [[commutative ring spectrum]].

* Moreover, the gain of _geometric $\infty$-function theory_ will be that it turns out to _unify_ a wealth of concepts appearing in [[FQFT]] and [[representation theory]].

This is the reason why we bother with geometric $\infty$-function theory and devote a detailed discussion to it: _geometric $\infty$-function theory_ carries the promise of getting close to the sought-for Lawvere-ification of quantum field theory -- providing its [[physics|natural language]].



#### 2.1 $\infty$-categories ####

The [[∞-categories]] that we are dealing with here are 

* [[(∞,1)-categories]].

There are several reasons for 

* [[Why (∞,1)-categories?]]

in the present context, the main one being that they allow to make precise the ideas summarized in the

* [[motivation for sheaves, cohomology and higher stacks]].


In principle one will want to eventually understand [[geometric function theory]] in the context of more general [[higher category theory]], in particular for [[(∞,n)-categories]], but a great deal is already gained by just (hah!) looking at [[(∞,1)-categories]] -- not the least because (only) for them a working well-developed full theory exists at the moment, developed by [[Andre Joyal]] and further developed by [[Jacob Lurie]]:

* [[Higher Topos Theory]]

This subsumes and unifies notably a wealth of more-or-less ad-hoc constructions that have been known for a bit longer. In particular the theory of [[model category|model categories]] is realized as a way to, well, model $(\infty,1)$-categories:

In particular every

* [[simplicial model category]]

is naturally a 

* [[presentable (infinity,1)-category|presentation of an (∞,1)-category]].

##### 2.1.1 Enhancing triangulated categories #####

The aim of _geometric $\infty$-function theory_ is to develop a good $\infty$-categorical generalization of the simple notion of 

* _sets of functions on spaces_ 

to 

* "$\infty$-categories of $\infty$-functions" on "$(\infty)$-spaces" 

essentially following the general philosophy of [[space and quantity]].

Whatever the answer is, the collection of such $\infty$-functions should be

* abelian

and

* monoidal

in a suitable sense. 

From various examples it has become clear that the right [[vertical categorification]] of a function $X \to \mathbb{C}$ is a [[functor]] $X \to Vect_{\mathbb{C}}$, which -- if sufficiently well behaved -- we may regard as a vector bundle on $X$.

Indeed, just as functions $[X,\mathbb{C}]$ form a vector space, functors $[X, Vect_{\mathbb{C}}]$ naturally form a [[2-vector space]].

Such a 2-vector space is in particular an [[abelian category]]. This is one of the ways in which we expect $\infty$-functions to form an _abelian_ collection. 

Experience shows that the right (or at least a very good) $\infty$-[[vertical categorification]] of [[abelian category]] is a

* [[stable (∞,1)-category]].
  
It turns out that just as [[model category|model categories]] and related [[homotopical category|homotopical categories]] are best thought of as, well, _models_ for $(\infty,1)$-categories, so various constructions in [[homological algebra]] -- and in the end really all of modern homological algebra -- is best thought of as models for [[stable (infinity,1)-category|stable (∞,1)-categories]].

This concerns notably

* [[A-∞ categories]]

and

* [[pretriangulated dg-category|pretriangulated dg-categoires]]

which, in turn, are already [[enhanced triangulated category|enhanced]] [[triangulated category|triangulated categories]]: namely [[dg-category|dg]]-[[enriched category|enriched]] versions thereof.

At this point you are urged to really have a look at the entry on [[stable (∞,1)-category]] and marvel about the fact that 

* **the definition of stable $(\infty,1)$-category is short, simple and transparent**.

It's the most obvious thing in the world. And yet, it turns out that the rather involved definitions of [[derived category|derived]] [[triangulated category]] follow from this simple definition when one decides to look at just the 1-categorical shadow given by the [[homotopy category of an (infinity,1)-category|homotopy category of the stable (∞,1)-category]].

This is a general pattern here:

* $(\infty,1)$-categorical notions -- and in particular [[quasi-category|quasi-categorical]] notions -- are _conceptually_ simple and lend themselves to the formulation and description of higher categorical situations;

* but for concrete constructions in terms of them there is a wealth of tools with different areas of applicability, many of which have been understood and developed as theories in their own right for a considerable time.



#### 2.2 monoidal $\infty$-categories ####

A central aspect of geometric $\infty$-function theory is that we regard the collection $C(X)$ of $\infty$-functions assigned to a generalized space $X$ (concretely modeled as $QC(X)$, see section 3 below) not just as a higher vector space but naturally as a [[higher algebra]]. Indeed, the central two theorems/properties of [[geometric function theory]] concern the interplay between the _geometry_ of intersections or [[pullbacks]]


of generalized spaces and the _algebra_ of [[tensor products]] 

$$
  C(Y_1) \otimes_{C(X)} C(Y_2)
  \,.
$$

In order to formulate this, one needs a good general theory of [[higher algebra]]. Just as ordinary [[algebra]] takes place inside a [[monoidal category]], [[higher algebra]] takes place in a [[monoidal (∞,1)-category]]:

an "$\infty$-monoid" or "$\infty$-algebra" (to distinguish from the traditional [[A? algebra]], which is supposedly a special case) is an [[algebra in an (infinity,1)-category|algebra/monoid object in a monoidal (∞,1)-category]].

In order to characterize the $(\infty,1)$-categories $C(X)$ as algebra objects in such a sense we profit from the ease with which [[quasi-category|quasi-categories]] naturally reflect on themselves and allow us with comparative ease to talk about the [[(∞,1)-category of (∞,1)-categories]] $(\infty,1)Cat_1$.

Since $(\infty,1)Cat_1$ itself is a [[symmetric monoidal (∞,1)-category]], we will essentially identify the $\infty$-algebras $C(X)$ as [[algebra in an (infinity,1)-category|algebra objects]] in $(\infty,1)Cat_1$.

But there is actually a slight technical simplification: we don't deal with _all_ $(\infty,1)$-categories, but just with [[presentable (∞,1)-categories]]. See there for the (long) list of nice properties and characterization of presentable $(\infty,1)$-categories.

So

* presentable $(\infty,1)$-categories form the [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]]  $Pr(\infty,1)Cat_1^L$;

* the $\infty$-algebras of $\infty$-functions $C(X)$ are [[algebra in an (infinity,1)-category|algebra objects in]] $Pr(\infty,1)Cat_1^L$.

Notice that this means in particular that the "additive" structure on $C(X)$ is taken to be nothing but the $(\infty,1)$-categorical colimit operation inside $C(X)$: this is the operation with respect to which [[(∞,1)-functors]] in $(\infty,1)Cat_1^L$ are linear, and with respect to which the tensor product is bilinear.

In terms of this [[higher algebra]] we will obtain the two central (defining) theorems of _geometric $\infty$-function theory_.

+-- {: .standout}
+-- {: .un_theorem}
###### Theorem
**Fundamental theorem of geometric $\infty$-function theory**

For $X \to Y \leftarrow X'$ morphisms of nice generalized spaces ([[perfect ∞-stacks]]) and for $\infty$-functions $C(-) = QC(-)$ (given by the assignment of $(\infty,1)$-categories of quasicoherent sheaves) we have

* _$\infty$-matrices ([[integral transform]]s) are $\infty$-functions on fiber products_ in that the following equivalence holds: $ C(X \times_Y X') \simeq C(X) \otimes_{C(Y)} C(X')$

* _$\infty$-linear maps are given by $\infty$-matrices in that also the following equivalence holds: $C(X \times_Y X') \simeq Fun_{C(Y)}(C(X), C(X'))$;

=--
=--

#### basic ideas related to $\infty$-stacks ####

The following discussion aims to describe the role played by [[∞-stacks]] and their morphisms in the context of geometric $\infty$-funcion theory. 

We place ourselves in the context of an [[(∞,1)-category]]
$H$ of (possibly [[derived stack|derived]]) $\infty$-stacks, i.e. of [[(∞,1)-sheaves]].

Recall what this means:

The fundamental datum that we fix once and for all and which determines
what $H$ is like is a choice of [[category]] $S$ equipped with the
structure of a [[site]]. $H$ is going to be the $(\infty,1)$-category
of generalized spaces which may be probed by objects of $S$ in a way
that is consistent with the way one glues objects in $S$ using its 
structure of a [[site]]. More generally, $S$ itself may be an 
$(\infty,1)$-category.

It is actually not hard to say this in a precise and fairly
explicit way.

First the precise way.

* the first datum is: $S$ a [[small category|small (∞,1)-category]];

* let then $PSh(S) := Funct(S^{op}, \infty\text{-}Grpd)$ be the $(\infty,1)$-category
of [[(∞,1)-functors]] from the [[opposite (infinity,1)-category|opposite (∞,1)-category]] $S^{op}$
to the $(\infty,1)$-category of $\infty$-groupoids.

* the second datum is: $i : H \hookrightarrow PSh(S)$ a 
[[full (infinity,1)-subcategory|full (∞,1)-subcategory]] of $PSh(S)$
such that the inclusion is a [[geometric morphism]] of  
[[(∞,1)-topoi]], i.e. such that $i$ has
a [[exact (infinity,1)-functor|left exact]] [[adjoint (infinity,1)-functor|left adjoint]]
$(-)^* : PSh(S) \to H$.

The same in one sentence: $H$ is a sub-[[(∞,1)-topos]] of the [[(∞,1)-topos]]
of [[(∞,1)-presheaves]] on $S$.

Or equivalently: $H$ is an [[(∞,1)-category of (∞,1)-sheaves]] on $S$.


Now the fairly explicit way:

There are various different but equivalent explicit realizations, or models,
for [[(∞,1)-categories]]. 
Of these consider [[quasi-categories]], which are  
[[simplicial sets]] that are [[Kan fibration|weak Kan complexes]],
and [[SSet]]-[[enriched categories]]. 
These are related by the 
[[homotopy coherent nerve]] functor: 

$$ 
  N : SSet\text{-}Cat \to SSet
$$

which has a [[left adjoint]]

$$ 
  F : SSet \to SSet\text{-}Cat
$$

that sends every simplicial set to the [[SSet]]-[[enriched category]] 
freely generated from it. One can think for $S$ a [[quasi-category]] of $F(S)$
as a semi-strictification of it, in which composition of morphisms along
0-cells is strictly associative.

It is convenient and usual to switch back and forth between these two
models. Quasi-categories tend to give rise to conceptually more transparent
definitions, while [[SSet]]-categories tend to be more convenient
for many explicit computations. 

To get back to our [[(∞,1)-category of (∞,1)-sheaves]] $H$,
we describe it in terms of these models as follows.

* $S$ is some small [[simplicial set]] which we can assume to be a [[weak Kan complex]];

* $\infty\text{-}Grpd := N(Kan)$ is the [[simplicial set]] which is the image under
the [[homotopy coherent nerve]] functor of the full [[SSet]]-subcategory
of [[SSet]] on [[Kan complex]]es;

* $PSh(S) = SSet(S^{op},\infty\text{-}Grpd)$ is just the simplicial set of
simplicial maps between the simplicial sets $S^{op}$ and $\infty\text{-}Grpd)$.

For explicitly constructing $H$ as a full sub-$(\infty,1)$-category of $PSh(S)$ 
in practice one usually switches from the [[quasi-category]] picture to 
the [[SSet]]-[[enriched category]] picture. So assume $H$ explicitly 
to be an [[SSet]]-[[enriched category]] and $i : H \to F(PSh(S))$
the suitable inclusion [[SSet]]-functor. 

Notice that its left adjoint $(-)^* : PSh(S) \to N(H)$ is 
[[(∞,1)-sheafification]]: it sends every [[(∞,1)-presheaf]]
to the corresponding [[(∞,1)-sheaf]]. In other words, this is
_$\infty$-stackification_. Describing the full $\infty$-stackification of
a given $(\infty,1)$-presheaf explicitly is usually hard. Moreover, it is
usually much more than one wants to actually know. 

Therefore a common approach to constructing $H$ is as an [[SSet]]-[[enriched category]]
which has precisely the same objects as $F(PSh(S))$ has, but where
every object is $(\infty,1)$-equivalent to its $(\infty,1)$-sheafification.
This is in particular what happens in the most developed explicit model
for $H$, due to K. Brown, A. Joyal, J. Jardine and others, in which (for $S$ an
ordinary 1-category) $H$ is constructed as the canonical [[SSet]]-enrichment
of the [[model structure on simplicial presheaves|model category structure on]]
$Funct(S^{op}, SSet)$. 

For such a model of $H$, let $A$ be an object, i.e. an $(\infty,1)$-presheaf
which need not be an $(\infty,1)$-sheaf/$\infty$-stack, and let $X$ be
any other object, then the simplicial set

$$
  H(X,A)
$$

(which, if it is not [[Kan complex|Kan]] already, we are to think of as representing
the $\infty$-groupoid obtained from its [[Kan fibration|Kan-fibration]] replacement)

is _equivalent_ to $H(X,\bar A)$, where $\bar A$ is the $\infty$-stackification of $A$.
 
This is most familiar in detail, if maybe not conceptually, in 
the context of [[abelian sheaf cohomology]]: an (ordinary) [[sheaf]] $A$ with
values in non-negatively graded chain complexes is, by the [[Dold-Kan correspondence]],
a special case of an $(\infty,1)$-presheaf with values in $\infty\text{-}Grpd$.
Computing the [[abelian sheaf cohomology]] of $A$ on $X$ can be understood
as being the computation of the $\infty$-stackification of $A$ evaluated on $X$.

Moreover, for a fixed $(\infty,1)$-presheaf $A$, homming into it yields a functor

$$
  H(-, A) : H^{op} \to SSet
$$

which, being $SSet$-valued, we are entitled to call an $(\infty,1)$-presheaf on $H$. 
In as far as $H$ is thought of as an $(\infty,1)$-category of $\infty$-stacks, this
is an $(\infty,1)$-presheaf or $\infty$-prestack on $\infty$-stacks.

It is natural, suggestive and common to  write $A(X) := H(X,A)$, following
the guide of the [[Yoneda lemma]], even if $X$ is far from being representable.

Let for instance $Vect_\infty \in H$ be an $(\infty,1)$-presheaf
which assigns to each test domain $U \in S$ an $\infty$-groupoid $Vect_\infty(U)$
of some kind of $\infty$-vector bundles on $U$. Then $Vect_\infty$ is,
regarded as a generalized space modeled on $X$, the 
[[classifying space]] of $\infty$-vector bundles, essentially by definition.

So for $X \in H$ any other $\infty$-stack/generalized space,

$$
  Vect_\infty(X) := H(X, Vect_\infty)
$$ 

is the (simplicial set whose Kan-fibrant replacement is) the $\infty$-groupoid of 
(some kind of) $\infty$-vector bundles of on $X$.

If the $X$ here is an $\infty$-groupoid valued presheaf which really takes
values in higher groupoids and not just in sets, then $X$ is actually 
to be regarded as a generalized $\infty$-groupoid itself, of course. One
often thinks of such $X$ as [[orbifolds]]. If we write $X_0 \hookrightarrow X$ for the
presheaf of objects in $X$, then 

* $Vect_\infty(X_0)$ is the $\infty$-groupoid of $\infty$-vector bundles on $X_0$

* $Vect_\infty(X)$ is the $\infty$-groupoid of _equivariant_ $\infty$-vector bundles on $X_0$,

where the equivariance in question is that encoded by the inclusion $X_0 \hookrightarrow X$.

This is notably relevant for the [[fundamental ∞-groupoid]]:

assume that our [[site]] $S$ is 
[[monoidal category|monoidal]] and
equipped with a cosimplicial object, i.e. a functor 
$\Delta_S : \Delta \to S$ from the [[simplex category]], 
such that $\Delta_S[0]$ is a [[generator]] of $S$,
then there is canonically the functor

$$
  \Pi : S \to H
$$

which sends each test object $X_0$ to the $(\infty,1)$-presheaf that sends
each domain $V$ to the $V$-family version of the singular simplicial complex of $U$:

$$
  \Pi(X_0) : U \mapsto S(V \otimes \Delta^\bullet, X_0)
  \,.
$$

The inclusion of the space of objects in $\Pi(X_0)$ is just $X_0 \hookrightarrow \Pi(X_0)$.
From the above we now have

* $H(X_0, Vect_\infty) =: Vect_\infty(X_0)$ is the $\infty$-groupoid of $\infty$-vector bundles on $X_0$

* $H(\Pi(X_0),Vect_\infty)$ =: $Vect_\infty(\Pi(X))$ is the $\infty$-groupoid of $\Pi$-equivariant $\infty$-vector bundles on $X_0$.

By unwrapping what "$\Pi$-equivariance" means, one finds that this may equivalently be stated as

* $H(\Pi(X_0),Vect_\infty)$ =: $Vect_\infty(\Pi(X))$ is the $\infty$-groupoid of flat
$\infty$-vector bundles with connection on $X_0$.

It should be noted here that we can combine different levels of equivariance:

we may left [[Kan extension|Kan extend]] $\Pi : S \to H$ along the inclusion $S \hookrightarrow H$
to a functor $\Pi : H \to H$, so that 
for $X$ itself n $\infty$-orbifold of sorts, $\Pi(X)$ is the fundamental $\infty$-groupoid
of that. We still have a canonical inclusion $X \hookrightarrow \Pi(X)$.
If moreover $X_0 \hookrightarrow X$ is the inclusion from above, we have

* $H(X_0, Vect_\infty) =: Vect_\infty(X_0)$ is the $\infty$-groupoid of $\infty$-vector bundles on $X_0$

* $H(X, Vect_\infty) =: Vect_\infty(X)$ is the $\infty$-groupoid of equivariant $\infty$-vector bundles on $X_0$;

* $H(\Pi(X),Vect_\infty)$ =: $Vect_\infty(\Pi(X))$ is the $\infty$-groupoid of equivariant $\infty$-vector bundles on $X_0$ with flat connection.

Morphisms from the [[fundamental ∞-groupoid]] are also called [[local systems]].



#### 2.4 derived loop spaces ####

Of particular interest in this study of 
_geometric $\infty$_-function theory is the behaviour of $\infty$-functions on [[loop space object|loop spaces]]. The $(\infty,1)$-category $C(\Lambda X)$ of $\infty$-functions on the free loop space $\Lambda X$ of a sufficiently nice generalized space (a _perfect_ [[∞-stack]]) $X$ turns out to be the  [[infinity-trace|∞-trace]] or [[infinity-center|∞-center]] of that of $X$

$$
  C(\Lambda X) \simeq Tr( C(C)) \simeq Tr (C X)
  \,.
$$

which in turn are identified with the $\infty$-version of [[infinity-Hochschild homology|∞-Hochschild homology]] 

$$
  Tr(C(X)) := HH_*(C(X)) := C(X) \otimes_{C(X)\otimes C(X)^{op}} C(X)
$$ 

and [[infinity-Hochschild cohomology|∞-Hochschild cohomology]] 

$$
  Z(C(X)) := HH^*(C(X)) := End_{C(X) \otimes C(X)^{op}}(C(X))
$$ 

of $X$.

All these statements, powerful as they are, become trivialities, due to the naturality of the language that we are using, once we realize the following:

**homotopy pullbacks and loop space objects**

one of the central crucial facts of 
[[higher category theory]] is that 

**the fiber product of a point with itself is not the point, but the [[loop space object]] based at the point**:

let $x : * \to X$ be a morphism from the [[terminal object]] $*$ to some object $X$ in some $\infty$-category, then the $\infty$-categorical pullback of $x$ along itself is the based [[loop space object]] $\Omega_x X$.

$$
  \array{
    \Omega_x X &\to& *
    \\
    \downarrow &\Downarrow& \downarrow^x
    \\
    * &\stackrel{x}{\to}& X
  }
  \,.
$$

This should be intuitively quite clear: the $\infty$-pullback commutes only up to a 2-cell, a homotopy from the constant map on $x$ to the constant map on $x$. But such a homotopy is nothing but a loop in $X$, so $\Omega_x X$ is the object that remembers all possible ways to make this diagram commute up to a 2-cell.

Notice, by the way, that this phenomenon is the source of all "long exact sequences" that you'll ever run into: if we are for instance in a [[stable (∞,1)-category]], so that the [[terminal object]] $*$ is even a [[zero object]], $* = 0$, then a sequence

$$
  A \to B \to C
$$

is _exact_ (a fibration sequence) if the first morphism is the kernel of the second, meaning that we have a pullback

$$
  \array{
     A &\to& 0
     \\
     \downarrow &\Downarrow& \downarrow
     \\
     B &\to& C
  }
  \,.
$$

But then, since $\infty$-pullback squares compose just as ordinary pullback squares do, further computing the kernel of the kernel $A \to B$ does not produce 0, as it would in an ordinary [[abelian category]], but produces loops in $C$
 
$$
  \array{
     \Omega C &\to&  A &\to& 0
     \\
     \downarrow &\Downarrow& \downarrow &\Downarrow& \downarrow
     \\
     0 &\to& B &\to& C
  }
$$

since the total (outer) diagram is of the form

$$
  \array{
     \Omega C &\to& 0
     \\
     \downarrow &\Downarrow& \downarrow
     \\
     0 &\to& C
  }
  \,.
$$

So 

* **the $\infty$-kernel of an $\infty$-kernel is not 0, but is loops.**

Continuing this way one obtains long exact sequences

$$
  \array{
     \Omega B &\to& 0
     \\
     \downarrow_{\bar \Omega f} && \downarrow
     \\
     \Omega C &\to&  A &\to& 0
     \\
     \downarrow &\Downarrow& \downarrow &\Downarrow& \downarrow
     \\
     0 &\to& B &\stackrel{f}{\to}& C
  }
$$

induced from the single map $f : B \to C$.

For the purposes of geometric $\infty$-function theory what  is more relevant than this construction of based loop spaces as kernels is the construction of _unbased_ [[loop space objects]]. By a similar reasoning, one finds that the free loop space $\Lambda X$ of a generalized space $X$ is the $\infty$-pullback of the morphism $X \stackrel{Id \times Id}{\to}X \times X$ along itself

$$
  \array{
     \Lambda X &\to& X
     \\
     \downarrow && \downarrow^{Id \times Id}
     \\
     X &\stackrel{Id \times Id}{\to}& X \times X
  }
$$

The intuitive reasoning is the same as before, only that now we don't fix a single point. For more details and in particular for descriptions and examples of how to explicitly compute these loops space objects by [[homotopy limits]] see the examples listed at

* [[loop space object]]

* [[homotopy limit]]

* [[span trace]]

* [[co-span co-trace]]

* [[generalized universal bundle]].

Notice that when we speak of "homotopy" in the above, we mean _categorical homotopies_. These loop space constructions see only homotopies which actually exist as _morphism_s. If it is isn't clear what is meant by that statement, see the discusssion at [[constant ∞-stack]] for the two different perspectives on a [[topological space]], once as a categorically discrete but topologically non-discrete object, once as a topologically discrete but categorically non-discrete object:

In order for the above homotopy pullbacks to compute the intended loop spaces of topological spaces, these topological spaces need to be regarded as the topologically discrete(!) [[∞-groupoids]] they correspond to, i.e. as [[constant ∞-stacks]].

Now, with the understanding of [[loop space objects]] as homotopy pullbacks understood, the above statement about $\infty$-Hochschild (co)homology becomes essentially a triviality:

we have

$$
  \begin{aligned}
     C(\Lambda X) \simeq 
     C(X \times_{X \times X} X)
     &
     by\;\; loop \;\;space\;\; as \;\;homotopy\;\; pullback
     \\
     \cdots \simeq C(X) \times_{C(X)\times C(X)} C(X)
     &
     by \;\;fundamental \;\;theorem \;\;of\;\; geometric \infty-function\;\; theory
     \\
     \cdots \simeq HH_*(C(X)) :=: Tr(C(X))
     &
     by \;\;definition \;\;of \;\;trace/ Hochschild homology
  \end{aligned}
$$

or equivalently

$$
  \begin{aligned}
     C(\Lambda X) \simeq 
     C(X \times_{X \times X} X)
     &
     by \;\;loop\;\; space\;\; as\;\; homotopy\;\; pullback
     \\
     \cdots \simeq Fun_{C(X)}(C(X), C(X))
     &
     by \;\;fundamental \;\;theorem \;\;of \;\;geometric \infty-function \;\;theory
     \\
     \cdots \simeq HH^*(C(X)) :=: Z(C(X))
     &
     by \;\;definition \;\;of \;\;center/Hochschild cohomology
  \end{aligned}
$$



#### 2.5 $E_n$-structures ####

While for an ordinary [[monoids]] there is just one notion of commutativity (either it is or it is not commutative), already a [[monoidal category]] distinguishes between being just [[braided monoidal category|braided monoidal]] or fully [[symmetric monoidal category|symmetric monoidal]].

This pattern continues, as expressed by the [[k-tuply monoidal n-category|periodic table of k-tuply monoidal categories]].

A [[higher category theory|higher category]] may be a [[k-tuply monoidal n-category]] or more generally [[k-tuply monoidal (n,r)-category]] for different values of $k$. The lowest value of $k= 1$ (since for $k = 0$ there is no monoidal structure at all) corresponds to monoidal product which is $\infty$-associative, i.e.  associative up to higher coherent homotopies, but need not have any degree of _commutativity_. 

One says that an $n$-category is _symmetric monoiodal_ if it is "as monoidal as possible", i.e. $\infty$-tuply monoidal. In particular, in [[higher algebra|Noncommutative algebra]] and [[higher algebra|Commutative algebra]] [[Jacob Lurie]] describes

* [[monoidal (infinity,1)-category|1-fold monoidal (∞,1)-categories]];

* [[symmetric monoidal (infinity,1)-category|∞-tuply monoidal (∞,1)-categories]].


It turns out that the monoidal $(\infty,1)$-categories that we are concerned with here in general have a tuplicity  of monoidalness (heh) in between 1 and $\infty$:

For each $1 \leq n \leq \infty$ let $E_n$ denote the [[little n-disk operad|little n-disk]] [[operad]] whose [[topological space]] of $E_n^k$ of $k$-ary operations is the space of embedding of $k$ $n$-dimensional disks (balls) in one $n$-dimensional disk without intersection, and whose composition operation is the obvious one obtained from gluing the big outer disks into given inner disks.

In [John Francis' PhD thesis](http://dspace.mit.edu/handle/1721.1/43792) (reference _EnAction_ below ) the theory of [[(∞,1)-categories]] equipped with an action of the $E_n$-[[operad]] is established, so that

* $(\infty,1)$-categories with an $E_1$-action are precisely [[monoidal (∞,1)-categories]]  -- 1-fold monoidal $(\infty,1)$-categories;

* $(\infty,1)$-categories with an $E_\infty$-action are precisely [[symmetric monoidal (∞,1)-categories]] -- $\infty$-tuply monoidal $(\infty,1)$-categories;

* $(\infty,1)$-categories with an $E_n$-action for $1 \lt n \lt \infty$ are the corresponding $n$-tuply monoidal $(\infty,1)$-categories in between.

>**Remark** The second statement is example 2.3.8 in [EnAction](http://dspace.mit.edu/handle/1721.1/43792). The first seems to be clear but is maybe not in the literature. Jacob Lurie is currently rewriting [[higher algebra|Higher Algebra]] such as to build in a discussion of $E_n$-operadic structures in the definition of $k$-tuply monoidal $(\infty,1)$-categories.


Now, since geometric $\infty$-function theory is indeed _geometric_, we obtain a simple but powerful statement about the $k$-tupliness (heh) of the monoidal structure on our $(\infty,1)$-category of $\infty$-functions $C(X)$ of a space $X$:

As described above, by the _fundamental theorem of geometric $\infty$-function theorey_ , higher traces on $C(X)$ corresponds to forming higher loop spaces of $X$. More generally, the **$E_n$-center** $Z_{E_n}(C(X))$ of $C(X)$ may be taken to be $C([S^n,X])$, where $[S^n, X]$ is my notation for the $n$-sphere space of the generalized space $X$. But there is, 

* by construction, a natural action of $E_{n+1}$ on $[S^n,X]$;

*  accordingly, a natural action of $E_{n+1}$ on $C([S^n,X])$;

*  accordingly, due to the _fundamental theorem_ a natural action of $E_{n+1}$ on $Z_{E_n}(C(X))$.

Again, due to the good formalism, this statement becomes almost a tautology. Notice that this statement is otherwise known as the _Kontsevich conjecture_, which categorifies the _Deligne conjecture_.

For more on this see also the blog entry

* Noah Snyder, [The cohomology of the periodic table on n-categories](http://sbseminar.wordpress.com/2009/03/30/the-witt-group-or-the-cohomology-of-the-periodic-table-of-n-categories/)

and in particular David Ben-Zvi's comments to that.

>Okay, this entire section here needs more details and in particular more links to nLab entries with more details.


### 3. perfect stacks ###

In this section of the paper, the notion of a  [[perfect ∞-stack]] is defined, which is the general context in which the ideas of geometric $\infty$-function theory apply thoroughly without modifications.

In general, for any derived stack $X$ one can define the $(\infty, 1)$-category $QC(X)$ of 'functions on $X$'. One writes $X$ as a colimit of affine derived schemes $X \simeq colim_{U \in Aff_{/X}} U$ and then one sets
 \[
 QC(X) = lim_{U \in Aff_{/X}} QC(U)
\]
where $QC(U)$ for an _affine_ stack $U = Spec A$ is simply defined as $Mod_A$. 

One incarnation of derived stack in differential geometry is as an _$\omega$-groupoid internal to differential graded manifolds_. Since differential graded manifolds are 'affine', in the sense that knowledge of global functions is sufficient to determine the manifold, the limit construction above is not necessary. Hence, for such a derived stack (an $\omega$ groupoid $X$ internal to differential graded manifolds) we can more simply set
 \[
 QC(X) = smooth \omega-functors from X to chain complexes
\]
since the latter plays the role of a 'derived $\mathbb{C}$-module'.

+-- {: .query}
_Bruce_: I'm shooting in the dark here with this $\omega$-groupoid sentence above. Am I right? What does that boil down to concretely?
=--

A derived stack $X$ is _perfect_ when $QC(X)$ is 'finitely generated' in an appropriate sense. One first has to decide what means by a 'finite object', and then one must decide what it means for $QC(X)$ to be 'generated' by these objects. There are various routes one could take, but happily in the context of _perfect_ stacks these all turn out to be equivalent. (In fact, it seems more or less true that perfect stacks are precisely those stacks where these various requirements coincide). 

* [[(∞,1)-category of (∞,1)-sheaves]]

* [[derived stack]]

* [[perfect ∞-stack]]

#### definition of a perfect stack ####

* [[compact object in an (∞,1)-category]]

#### base change and projection formula ####

#### constructions of perfect stacks ####

### 4. Tensor products and integral transforms ###

Classical algebra is all about constructions in the category <b>[[Ab]]</b> of [[abelian groups]]. A [[ring]] $R$ in the usual sense is a [[monoid object]] in [[Ab]], i.e. an object $R \in {\mathbf Ab}$ together with multiplication and unit morphisms $m: R \otimes R \rightarrow R$ and $\eta: \mathbb{Z} \rightarrow R$ so that we have commutativity of appropriate diagrams expressing associativity and unity. Likewise, a right [[module]] $M$ over $R$ in the usual sense is an object $M \in {\mathbf Ab}$ together with an [[action]] morphism $a: M \otimes R \rightarrow M$ such that appropriate diagrams commute, and similarly for left modules.

[[higher algebra|Brave new algebra]] is about constructions in the [[stable (∞,1)-category of spectra]] $S_{\infty}$, which, like [[Ab]], is [[symmetric monoidal (infinity,1)-category|closed symmetric monoidal]] (under [[smash product of spectra]]) and [[cocomplete category|(co)]] [[complete category|complete]]. This means that we can consider [[algebra in an (infinity,1)-category|algebra objects]] $R$ and [[commutative algebra in an (infinity,1)-category|commutative algebra objects]] $A$ in $S_{\infty}$, as well as modules over them.

Even more generally, one can develop a _fearless new algebra_ in which we consider some closed, symmetric monoidal and (co)complete $\infty$-category $C$ and algebras
and commutative algebras in it (see [[higher algebra]]). For our purposes,
we take $C$ to be $Pr^{L}$, the $\infty$-category of [[presentable (∞,1)-categories]] with morphisms given by colimit preserving functors.  (More on the closed monoidal structure
below.)

The particular algebra objects in $Pr^{L}$ of interest to BZFN are [[stable (∞,1)-categories]] $QC(X)$ of quasi-coherent sheaves on a [[perfect infinity-stack|perfect]] [[derived stack]] $X$ (the [[homotopy category]] of $QC(X)$ being the good old-fashioned [[derived category]] of quasi-coherent [[sheaf|sheaves]]). Here $QC(X)$ is symmetric monoidal under the usual [[tensor product]] of quasi-coherent sheaves. Given two perfect derived stacks $X_{1}, X_{2}$, consider the diagram 


$$
  \array{
     && X_1 \times X_2
     \\
     & {}^{p_1}\swarrow && \searrow{}^{p_2}
     \\
     X_1 &&&& X_2
    
  }
$$
Given an object $\mathcal{P} \in QC(X_1 \times X_2)$, we can define a functor $\Phi_{\mathcal{P}}: QC(X_1) \rightarrow QC(X_2)$ by pulling-back along $p_1$, tensoring
with $\mathcal{P}$, and then pushing-forward along $p_2$.
Thus given an object $\mathcal{F} \in QC(X_1)$, we have $\Phi_{\mathcal{P}}(\mathcal{F}):= {p_2}_{*}({p_1}^{*}\mathcal{F} \otimes \mathcal{P})$. We think
of this an [[integral transform]] of the sheaf $\mathcal{F}$
with respect to the kernel $\mathcal{P}$. 

In fact, because of the naturality of the above operations,
this process gives a functor

$$\Phi: QC(X_1 \times X_2) \rightarrow Fun^{L}(QC(X_1), QC(X_2)),$$
where $Fun^{L}(QC(X_1), QC(X_2))$ is the internal
Hom in $Pr^{L}$ and consists of colimit preserving functors and their natural transformations.
 
The main result of section 4 of BZFN (which has been called above the fundamental theorem of geometric $\infty$-function theory)is that this functor and its cousins are equivalences. As a slogan:

+-- {: .standout}
[[integral transform]]s = colimit preserving functors
=--

This was first proved
in the context of [[dg-category|differential graded categories]] by To&euml;n,
building on work of Bondal, Orlov, and others. Note that
one can define a functor $\Phi$ in the same way at the level of [[triangulated category|triangulated categories]], but it is known to be badly behaved, and in fact could not be well-behaved, since we do not know how to make the category of triangulated categories into a closed symmetric monoidal category.




#### 4.1 Tensor products of $\infty$-categories ####

In order to be more precise, we need to look at the closed, symmetric monoidal structure on $Pr^{L}$, as developed by
Jacob Lurie [[higher algebra|DAG II.4 and DAG III.6]]. The [[internal hom]] 
between two [[presentable (∞,1)-categories]] $C,D$
is $Fun^{L}(C,D)$, which consists of colimit preserving [[(∞,1)-functors]]. To construct it, one considers $C$ and $D$ as
[[quasi-categories]] or weak Kan complexes. Functors from $C$ to $D$ are just maps of [[simplicial sets]], so the [[(∞,1)-category of (∞,1)-functors]] from $C$ to $D$ is just
the simplicial set of maps (internal Hom in simplicial sets)
$Fun(C,D)$. This is indeed an $\infty$-category again, whenever $D$ is an $\infty$-category/weak Kan complex.
Now inside of $Fun(C,D)$, we take the $\infty$-subcategory spanned by $0$-simplices representing colimit preserving functors to get $Fun^{L}(C,D)$.

> [[Chris Brav|Chris]]: (If there is some inaccuracy noted by anyone, feel free to comment. I might have forgotten some fibrant or cofibrant replacement somewhere.)

For the [[symmetric monoidal (infinity,1)-category of presentable (infinity,1)-categories|tensor product of presentable (∞,1)-categories]] we construct the $\infty$-category $C \otimes D$ which is
'the universal recipient of a bilinear functor' from $C \times D$. Here, we think of coproducts in $C$ and $D$
as addition, so if a functor $C \times D \rightarrow E$ preserves colimits in each variable, then in particular it preserves coproducts and so is 'bilinear'. Such a bilinear
functor will factor uniquely (in a homotopic sense)
through a universal bilinear functor $C \times D \rightarrow C \otimes D$, just like for bilinear maps
and tensor products of abelian groups.

Now given the above closed [[symmetric monoidal (infinity,1)-category|symmetric monoidal structure]]
on $Pr^{L}$ and since $Pr^{L}$ also has limits and colimits,
we can have all kinds of fun. For instance, given
an algebra object $R \in Pr^{L}$, a right $R$-module $M \in Pr^{L}$, and a left $R$-module $N \in Pr^{L}$, we can form
their relative tensor product over $R$, $M \otimes_R N \in Pr^{L}$ as the coequalizer of the pair of functors

$$M \otimes R \otimes N \underoverset{\alpha}{\beta}{\rightrightarrows} M \otimes N$$
where $\alpha$ is the action of $R$ on the right of $M$
and $\beta$ is the action of $R$ on the left of $N$. (This generalizes the relative tensor product of modules over a ring in the category of abelian groups, which is defined
to have exactly this coequalizing property.)


In section of 4.1 BZFN, there are various results, which are consequences of the [[Barr-Beck theorem|(∞,1)-categorical Barr?Beck theorem]]. 

> [[Chris Brav|Chris]]: They seem interesting and useful, but I don't seem to need them just at the moment, so I'll come back to them some other time.

#### 4.2 Sheaves on fiber products ####

In our present context, we consider a morphism of [[perfect infinity-stack|perfect]] [[derived stacks]]  $q: X \rightarrow Y$.
By pulling-back along $q$ and tensoring, we make $M=QC(X)$
into a $R=QC(Y)$-module. To see this, note that the functor
$(?) \otimes q^{*}(?): QC(X) \times QC(Y) \rightarrow QC(X)$
is indeed bilinear since pullback $q^{*}$ is the left adjoint of pushforward $q_{*}$, so preserves colimits, as does $\otimes$, being the left adjoint of the internal Hom of sheaves ('sheaf' or 'local' Hom). Thus by the universal property of the tensor product of $(\infty,1)$-categories, we do indeed get an action functor $QC(X) \otimes QC(Y) \rightarrow QC(Y)$. 

Now given a pair of perfect derived stacks $X_1, X_2$ over $Y$, we get two $R=QC(Y)$-modules $M=QC(X_1)$ and $N=QC(X_2)$ (left and right don't matter here, since $R=QC(Y)$ is symmetric monoidal) and we can form their relative tensor product

$$QC(X_1) \otimes_{QC(Y)} QC(X_2).$$

Now we can define a functor 

$$\boxtimes:={p_1}^{*}? \otimes {p_2}^{*}?: QC(X_1) \otimes_{QC(Y)} QC(X_2) \rightarrow QC(X_1 \times_Y X_2).$$
(We see that the above functor is bilinear (since pullbacks and tensor products preserve colimits) and coequalizes
the action of $QC(Y)$ on $QC(X_1)$ and $QC(X_2)$ (by commutativity of the fibre product diagram), so $\boxtimes$ does indeed define a functor.)

The first step in proving that 'integral transforms=colimit preserving functors' is to show that $\boxtimes$ is an equivalence. Then one has to show that $QC(X_1)$ is self-dual as a $QC(Y)$-module, and so conclude that

$$QC(X_1) \otimes_{QC(Y)} QC(X_2) \simeq QC(X_1)^{*}\otimes_{QC(Y)} QC(X_2)\simeq Fun_{Y}^{L}(QC(X_1),QC(X_2)).$$

As an intermediate step, BZFN first establish
an equivalence $\boxtimes: QC(X_1)^{c} \otimes QC(X_2)^{c} \simeq QC(X_1 \times X_2)^{c}$, where the superscript $c$
denotes the $\infty$-subcategories of compact objects.
(Here, we use the tensor product of small, stable idempotent complete $\infty$-categories $QC(X_1)^{c} \otimes QC(X_2)^{c}$, which is just like that for presentable $\infty$-categories except that bilinear functors are only required to preserve finite colimits.) Proposition 3.22 established that the external product $\otimes$ takes compact objects to compact objects, so 
we do get a functor as above, and that the category
$QC(X_1 \times X_2)^{c}$ is generated by external products.
To prove that $\boxtimes$ is an equivalence, it is therefore
sufficient to prove that for $M_i,N_i \in QC(X_i)$, we have
a natural isomorphism

$$Hom_{X_1 \times X_2}(M_1 \boxtimes M_2, N_1 \boxtimes N_2) \simeq Hom_{X_1}(M_1, N_1) \otimes Hom_{X_2}(M_2, N_2),$$
which is a nice exercise using the dualizability of the $M_i$ and the projection formula. 

Having established the equivalence $\boxtimes: QC(X_1)^{c} \otimes QC(X_2)^{c} \simeq QC(X_1 \times X_2)^{c}$, we can now establish the equivalence without the superscript $c$.
Since (by definition of a perfect stack) $Ind(QC(X_i)^{c})\simeq QC(X_i)$ and the fact (Proposition 4.4) that $Ind: Idem \rightarrow Pr^{L}$ from small idempotent complete stable $\infty$-categories to $Pr^{L}$ is symmetric monoidal, we get that 

$$QC(X_1) \otimes QC(X_2) \simeq Ind(QC(X_1)^{c} \otimes QC(X_2)^{c}) \simeq Ind(QC(X_1 \times X_2)^{c}) \simeq QC(X_1 \times X_2).$$

This gives the absolute version of the equivalence we want. To make it relative over $Y$, one has to think about 
how to actually compute $QC(X_1) \otimes_{QC(Y)} QC(X_2)$
and $X_1 \times_{Y} X_2$ in concrete terms. For the former,
you use Barr-Beck and realize the category as modules for the monad $\pi_{*}\pi^{*}$, where $\pi: X_1 \times_{Y} X_2 \rightarrow X_1 \times X_2$. For the latter, you realize the fibre product
as the limit of a cosimplicial diagram. Then some comparision takes place. It would be hard to give a nicer, more concise explanation than in BZFN, so for further details, take a look.

Now given the equivalence $\boxtimes: QC(X_1) \otimes_{QC(Y)} QC(X_2) \rightarrow QC(X_1 \times_Y X_2)$,
it remains to see that given a morphism $p: X \rightarrow Y$
of perfect stacks, $QC(X)$ is self-dual as a $QC(Y)$-module.
For this, we use the already established equivalence
$QC(X) \otimes_{QC(Y)} QC(X) \simeq QC(X \times _Y X)$. To establish self-duality, we
need to define a trace $\tau: QC(X) \otimes_{QC(Y)} QC(X) \rightarrow QC(Y)$ and unit $u: QC(Y) \rightarrow QC(X) \otimes_{QC(Y)} QC(X)$ so that the composition
$id \otimes \tau \circ u \otimes id: QC(Y) \rightarrow QC(Y)$ is the identity. To do this, consider the relative diagonal morphism
$\Delta: X \rightarrow X \times_Y X$ and define $u=\Delta_{*}\p^{*}$ and $\tau: p_{*}\Delta^{*}$. Then a diagram chase and the base-change formula show that $u$ and $\tau$ satisfy the necessary conditions.


The final result from this section, Corollary 4.12, is useful for the applications to topological field theory:

Given a finite simplicial set $\Sigma$ a perfect stack
$X$, we may form the mapping stack $X^{\Sigma}$, which is again perfect. Then there is an equivalence $QC(X^{\Sigma}) \simeq QC(X) \otimes \Sigma$.


>[[Chris Brav|Chris]]:Haven't thought this through. Someone may comment, or I'll come back to it later.

#### 4.3 Geometric base stacks ####

The 'fundamental theorem' described above can be extended
to the case where $X_1 \rightarrow Y$ is a perfect morphism of geometric stacks ($X_1$ and $Y$ need not be absolutely perfect) and $X_2 \rightarrow Y$ is an arbitrary morphism of stacks.

+-- {: .query}

_Bruce_: What's a [[geometric stack]]? 

_Chris_: A stack is geometric if it is quasi-compact (any open cover has a finite sub-cover) and the diagonal morphism
is representable and affine, though that probably doesn't help much. I don't know much about stacks yet, but maybe someone else can explain this. I think the point is that one needs some hypotheses to actually prove stuff for stacks. 

=--

### 5. Applications ###

In this section, BZFN study the categorical center $\mathit{Z}$ and trace $\mathit{Tr}$
of presentable mononoidal $\infty$-categories, which will be defined as analogues of some classical algebraic notions.

Two geometric cases are of special interest. 

When the monoidal category is $QC(X)$, then there are equivalences

$$\mathit{Z}(QC(X))\simeq QC(LX) \simeq \mathit{Tr}(QC(X)),$$
where $LX=X \times_{X \times X} X$, the derived loop space
of $X$.

When the monoidal category is $QC(X \times_Y X)$ equipped with convolution, then there is an equivalence

$$\mathit{Z}(QC(X \times_Y X))\simeq QC(LY)$$
and once Grothendieck duality has been worked out for derived stacks, then there will be another equivalence
$$QC(LY) \simeq \mathit{Tr}(QC(X \times_Y X)).$$

The categorical center is a generalization of lots of things: the center of an algebra, the Hochschild cochain complex of an algebra, the Drinfeld double of a monoidal category... It turns out to be an $E_2$-category, the $\infty$-categorical version of a braided monoidal category. That's probably explained in section 6.

#### Some background####

Let's start with a good old-fashioned algebra $A$ (an algebra object in $Ab$ of $Vect$). We can form the center $Z(A)$ of $A$, which again is a commutative algebra. 
One can also form the endomorphisms of $A$ as a bimodule over itself: $End_{A \otimes A^{op}}(A)$. The natural homomorphism 
$$Z(A) \rightarrow End_{A \otimes A^{op}}(A)$$
that sends a central element $x$ to multiplication
by $x$ is an isomorphism of algebras (multiplication by $x$ is indeed a bimodule endomorphism since $x$ is central and 
every bimodule endomorphism $\varphi$ is of this form since it is determined by $\varphi(1)=x$).

If we consider $A$ as an algebra object in the (dg enhanced) derived category of $Ab$, then we can also 
consider the _derived_ endomorphisms of $A$ as an $A$-bimodule, which is a dg algebra (defined up to quasi-isomorphism) that we may think of as the _derived center_ of  $A$:

$$RHom_{A \otimes A^{op}}(A,A).$$  

The cohomology of this dg algebra is a graded algebra
known as the _Hochschild cohomology_ of $A$. Its zeroth graded piece is of course just the classical center $Z(A)=End_{A \otimes A^{op}}(A)$. 

To compute $RHom_{A \otimes A^{op}}(A,A)$ in practice, one has take a projective resolution of the first entry $A$ as an $A$-bimodule and then write down the complex of $Hom$s from this resolution to $A$. The standard such resolution is the 'bar resolution' of $A$, which is built using
the functor
$$L=A \otimes ?: Mod A^{op} \rightarrow  Mod A \otimes A^{op},$$
which is left adjoint to the forgetful functor $R:Mod A \otimes A^{op} \rightarrow Mod A^{op}$. Then $LR$ is a comonad on $Mod A \otimes A^{op}$ and so applying it to $A$ gives (in the usual way) an augmented simplicial object whose $k$th term is $A^{\otimes k+1}$. In particular, the $-1$st term is just $A$. By taking alternating sums of the face maps, one gets a complex $C_*(A)$ of free $A$-bimodules that can be shown to be exact and so provides a resolution of $A$. Then the $Hom$ complex 
$$Hom_{A \otimes A^{op}}(C_*(A),A)$$
is known as the Hochschild cochain complex of $A$ and provides the standard model for the derived center of $A$.

Now for the categorical trace. Given two bimodules $M,N$
we can form their relative tensor product $M \otimes_A\otimes A^{op} N$, giving a new bimodule. We think of this
operation as a 'bilinear pairing' on the category of bimodules (remember, bilinear=colimit preserving). We could also take tensor product in the derived category of bimodules, which in practice requires that we resolve one of $M$ or $N$ by flat (or a fortiori free) $A$-bimodules, and so get a derived pairing of bimodules. In particular,
we could take the derived pairing of $A$ with itself as an $A$-bimodule to get the Hochschild chain complex

$$A \otimes_{A \otimes A^{op}} C_*(A),$$
whose homology is the _Hochschild homology_ of $A$.

#### Centers and traces ####
The above constructions can be carried over to algebra objects $A$ in a closed symmetric monoidal $\infty$-category $\mathcal{C}$. In particular, we consider $C=Pr^{L}$, the $\infty$-category of presentable $\infty$-categories.

We define the _categorical center_ to be the endomorphism object 

$$End_{A \otimes A^{op}}(A) \in Pr^{L},$$
where we consider $A$ as module-category over itself on the left and on the right and we compute the internal $Hom$ in $Pr^{L}$ of $A$ with itself as bimodule.

Also we define the _categorical trace_ to the the pairing
object

$$A \otimes_{A \otimes A^{op}} A$$
of $A$ with itself as a bimodule, using the tensor product
in $Pr^{L}$ and then coequalizing the left and right actions of $A$ on itself to form the relative tensor product.
  


 * [[span trace]]

 * [[co-span co-trace]]

#### Centers of convolution categories ####

#### higher centers ####

### epilogue:  topological field theory ###

* [[FQFT]]


#### topological field theory from perfect stacks ####

* [[∞-model]]

#### Deligne-Kontsevich conjectures for derived centers ####




## Character Quantum Field Theory ##

* [[ringed site]]

* [[D-module]]

### and so on ###


# Background literature #

For the general [[(infinity,1)-category|(∞,1)-categorical]] formalism

* [[Jacob Lurie]], [[Higher Topos Theory]].

For the [[stable (infinity,1)-category|stable]] aspects

* [[Jacob Lurie]], [[Stable ∞-Categories]].

For the [[monoidal (infinity,1)-category|monoidal]] aspects 

* [[Jacob Lurie]], [[higher algebra|Noncommutative and commutative algebra]].

For the general TQFT background and in particular see

* [[Jacob Lurie]], _On the classification of TFT_ ([pdf](http://www.math.harvard.edu/~lurie/papers/cobordism.pdf))

In particular see also the beginning of section 4.1 there for more on $E_n$-monoidal $(\infty,1)$-categories.

For more details on [[loop space objects]] for [[derived stacks]]  

* **LoopSpace** [[David Ben-Zvi]], David Nadler, _Loop Spaces and Langlands Parameters_ ([arXiv](http://arxiv.org/abs/0706.0322))

[[John Francis]]' work on actions of the [[little k-cubes operad]] on $(\infty,1)$-categories is here

* **EnAction** [[John Francis]], PhD thesis ([web](http://dspace.mit.edu/handle/1721.1/43792))


For more related material see [[Northwestern TFT Conference 2009]].


[[!redirects geometric ∞-function theory]]