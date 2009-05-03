This entry is about the work by David Ben-Zvi, John Francis and David Nadler on application of a [[(infinity,1)-category|(infinity,1)-categorical]] realization of [[geometric function theory]] to [[FQFT|extended quantum field theory]] in the context in which Jacob Lurie proved the [[generalized tangle hypothesis|cobordism hypothesis]].

So far this work is presented in the two articles

* **IntTrans** David Ben-Zvi, John Francis, David Nadler, _Integral transforms and Drinfeld Centers in Derived Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))

* **CharTheo** David Ben-Zvi, David Nadler, _The Character Theory of a Complex Group_ ([arXiv](http://arxiv.org/abs/0904.1247))

This is based in particular on

* **LoopSpace** David Ben-Zvi, David Nadler, _Loop Spaces and Langlands Parameters_ ([arXiv](http://arxiv.org/abs/0706.0322))


+-- {: .query}

This entry is supposed to be the $n$Lab-working area for a " Journal Club -- Geometric $\infty$-function theory ". The corresponding discussion page at the $n$-Caf&#233; is [Journal Club -- Geometric Infinity-Function Theory](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html)

The idea is to 

* jointly discuss at the $n$Caf&#233; section-by-section these articles; to get an idea for what's going on;

* add here, step by step, links to keywords appearing in these sections, and create the corresponding entries describing them.

* This is supposed to be a recursive and iterative process, which, if successful, will eventually create here a useful repository of entries that describe and explain the various aspects of the topic.

=--

# Timeline #

We will try to proceed as follows: we go through the sections of the two articles, step by step, possibly several steps for one section. Each week on Monday, one of us produces a "report" on the section he or she was assigned to read. 

This "report" would try to give a rough idea of what is going on in a given section. A report may be anything from a  heap of questions (likely) to a complete detailed rederivation of all the details (maybe not quite as likely, but let's not exclude it!) The more questions, the more we all get involved, which is the whole point of doing this online.

I ([[Urs Schreiber|Urs]]) am imagining that whatever the report is like, it consists of 

* a bulleted list of whatever needs to be listed, with links to whatever deserves to be linked to, here in this $n$Lab-entry, in the following list of sections;

* a comment to the [blog entry](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html) that maybe copies this entire content but at least alerts the blog readers about the new material now to be found here, accompanied by some comments as seems necessary.

The idea is that we have discussion on the blog but distill whatever we can into the $n$Lab here.


Here is the list of reports, as planned so far:

* Monday, April 27: [[Alex Hoffnung|Alex]] on section 1, [Introduction](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=2) [[tick6.png:pic]] ([n-category caf&#233; entry](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit_1.html))

* Monday, May 4: [[Urs Schreiber|Urs]] on section 2, [Preliminaries](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=10)

* Monday, May 11: [[Bruce Bartlett|Bruce]] on section 3, [Perfect Stacks](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=16)

* Monday, May 18: [[Christopher Brav|Christopher]] on section 4, [Tensor products and integral transforms](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=24)

* Monday, May 25: somebody on section 5, [Applications](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=32)

* Monday, June 1: somebody on section 6, [Epilogue: TFT](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=39)



#Idea#

The central structural theorem of [[FQFT|TQFT]], the [[generalized tangle hypothesis|cobordism theorem]] states that [[FQFT|(infinity,n)-categorical extended topological quantum field theories]] are entirely determined by their value in the [[point]], which has to be an [[object]] in an [[(infinity,n)-category]] with high dualizability properties.

Very generally, the point of _geometric $\infty$-function theory_ is to construct and study concrete realizations of the [[FQFT]]s guaranteed to exist by this theorem.

The central tool, from which this entry draws its title, is an [[(infinity,1)-category|(infinity,1)-categorical]] version of [[geometric function theory]]: 

the rough idea is that the data the [[FQFT]] assigns to a manifold $\Sigma$ is a collection $Z(\Sigma)$ of $\infty$-functions -- the physical _fields_ -- on $\Sigma$, or, more generally, sections of some $\infty$-bundle on $\Sigma$, and that the morphism $Z(\Sigma) : Z(\Sigma_{in}) \to Z(\Sigma_{out})$ assigned by the [[FQFT]] to a [[cobordism]] $\Sigma : \Sigma_{in} \to \Sigma_{out}$
is obtained from a [[groupoidification|pull-push-operation]] on the objects of $Z(\Sigma_{in})$ through a [[span]] to obtain objects in $Z(\Sigma_{out})$.

This picture arises  naturally and is maybe best understood in terms of [[FQFT]]s that arise as [[sigma-model]]s, namely which are [[representable functor|represented]] by a _target space_ object $P$:

assume that $P$ is some kind of generalized space (which will usually mean: an [[(infinity,1)-sheaf]], see [[heuristic introduction to sheaves, cohomology and higher stacks]] for motivation of this point) and regard the manifolds $\Sigma$ as special cases of generalized manifolds.

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
    & {}^{p_1}\swarrow && \searrow^{p_2}
    \\
    [\Sigma_{in}, P] &&&& [\Sigma_{out}, P]
  }
  \right)  
  \,.
$$

If now $C([\Sigma_{in},P])$ denotes some sensible collection of $\infty$-functions on the mapping space $[\Sigma_{in}, P]$, there will be an [[(infinity,1)-category|infinity-categorical]] pull-push operation

$$
  \int_{p_2} p_1^*(-) : C([\Sigma_{in}, P]) \to C([\Sigma_{out}, P])
$$

generalizing the analogous operation as described as [[groupoidification]].

As described as [[geometric function theory]], such pull-push operations can naturally be regarded as vast generalization of familiar [[matrix calculus]], including in particular operations like Fourier-Moukai transformations.


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


#### 1.1 Perfect stacks ####

* [[ind-object]]

  * [[ind-object in an (infinity,1)-category]]

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

* [[sigma-model]]


### 2. Preliminaries ###

Recall that the goal of **geometric $\infty$-function theorys** is

* to establish a good [[higher category theory|higher categorical]] version of linear algebra ("integral transform" = "higher matrix multiplication"!)

* such that interesting classes of [[sigma-model]] [[FQFT|extended TQFTs]] $Z_P$ are [[representable functor|represented]] by [[heuristic introduction to sheaves, cohomology and higher stacks|generalized spaces]] $P$ 

  * in that the "higher linear map" $Z_P(\Sigma)$ assigned by the [[FQFT|QFT]] to a [[cobordism]] [[cospan]] $\array{ && \Sigma \\ & \nearrow && \nwarrow \\ \Sigma_{in} &&&& \Sigma_{out}}$ is giveen by the [[span]] $\array{ && [\Sigma,P] \\ & \swarrow && \searrow \\ [\Sigma_{in},P] &&&& [\Sigma_{out}, P]}$.

This clearly requires that

* we fix a good ambient context of [[Higher Topos Theory|higher sheaf- and category theory]];

* and inside that a good general concept of [[higher algebra]].

One point made by the [[David Ben-Zvi|Ben-Zvi]]/Francis/Nadler work is that a good working context of [[higher category theory]] in which a good notion of _geometric $\infty$-function theory_ can be set up nicely is the context assembled and developed in the PhD thesis of [[Jacob Lurie]], consisting of

* [[Higher Topos Theory]] -- the theory of [[(infinity,1)-category|(infinity,1)-categories]] and [[(infinity,1)-sheaf|(infinity,1)-sheaves]]

  * this assembles and develops 

    * work by [[Andre Joyal]] on [[quasi-category|quasi-categories]];

    * work by Simpson, Rezk, To&#235;n, Vezzosi and others on higher categories and higher stacks;

    * work by [[BrownAHT|Brown]], [[Andre Joyal|Joyal]], Jardine and others on [[model category|models]] for [[infinity-stack]]s. 

* [[Stable Infinity-Categories|Stable Higher Category Theory]] -- essentially the theory of [[additive and abelian categories]] lifted to the $(\infty,1)$-context;

  * which puts the large body of work on [[homotopy theory|stable homotopy theory]] and [[homological algebra]] into the above [[(infinity,1)-category|(infinity,1)-categorical]] context, in essence identifying the abstract idea modeled by [[pretriangulated dg-category|pretriangulated dg-categories]] and [[A-infinity category|A-infinity categories]]

* [[higher algebra|Higher Algebra]] -- the theory of [[monoid]]- or [[algebra]]-objects [[internalization|internal to]] ([[symmetric monoidal (infinity,1)-category|symmetrix]]) [[monoidal (infinity,1)-category|monoidal]] [[(infinity,1)-category|(infinity,1)-categories]]

  * expanding on work by To&#235;n-Vezoosi;

  * wich puts the "brave new algebra" of [[commutative ring spectrum|ring spectra]] into its natural higher categorical context.

Especially for the newcomer and non-expert it must be understood that the plethora of high-powered terminology appearing here is conceptually _simplified_ and unified by their description in the higher categorical context:

* the concept of an [[(infinity,1)-sheaf]]/[[infinity-stack]] is _much simpler_ than its model in terms of the [[model structure on simplicial presheaves]];

* the concept of a [[stable (infinity,1)-category]] is _much simpler_ than its 1-categorical shadow as a [[triangulated category]];

* the concept of a [[commutative algebra in an (infinity,1)-category]] is _simpler_ than the details of its realization given by a [[commutative ring spectrum]].

* Moreover, the gain of _geometric $\infty$-function theory_ will be that it turns out to _unify_ a wealth of concepts appearing in [[FQFT]] and [[representation theory]].

This is the reason why we bother with geometric $\infty$-function theory and devote a detailed discussion to it: _geometric $\infty$-function theory_ carries the promise of getting close to the sought-for Lawvere-ification of quantum field theory -- providing its [[physics|natural language]].



#### 2.1 $\infty$-categories ####

The [[infinity-category|infinity-categories]] that we are dealing with here are 

* [[(infinity,1)-category|(infinity,1)-categories]].

There are several reasons for 

* [[why (infinity,1)-categories?]]

in the present context, the main one being that they allow to make precise the ideas summarized in the

* [[heuristic introduction to sheaves, cohomology and higher stacks]].


In principle one will want to eventually understand [[geometric function theory]] in the context of more general [[higher category theory]], in particular for [[(infinity,n)-category|(infinity,1)-categories]], but a great deal is already gained by just (hah!) looking at [[(infinity,1)-category|(infinity,1)-categories]] -- not the least because (only) for them a well-developed theory exists, developed by [[Andre Joyal]] and further developed by [[Jacob Lurie]]:

* [[Higher Topos Theory]]

This subsumes and unifies notably a wealth of more-or-less ad-hoc constructions that have been known for a bit longer. In particular the theory of [[model category|model categories]] is realized as a way to, well, model $(\infty,1)$-categories:

In particular every

* [[simplicial model category]]

is naturally a 

* [[presentable (infinity,1)-category|presentation of an (infinity,1)-category]].

##### 2.1.1 Enhancing triangulated categories ####

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

* [[stable (infinity,1)-category]].
  
It turns out that just as [[model category|model categories]] and related [[homotopical category|homotopical categories]] are best thought of as, well, _models_ for $(\infty,1)$-categories, so various constructions in [[homological algebra]] -- and in the end really all of modern homological algebra -- is best thought of as models for [[stable (infinity,1)-category|stable (infinity,1)-categories]].

This concerns notably

* [[A-infinity category|A-infinity categoires]]

and

* [[pretriangulated dg-category|pretriangulated dg-categoires]]

which, in turn, are already [[enhanced triangulated category|enhanced]] [[triangulated category|triangulated categories]]: namely [[differential graded category|dg]]-[[enriched category|enriched]] versions thereof.

At this point you are urged to really have a look at the entry on [[stable (infinity,1)-category]] and marvel about the fact that 

* **the definition of stable $(\infty,1)$-category is short, simple and transparent**.

It's the most obvious thing in the world. And yet, it turns out that the rather involved definitions of [[derived category|derived]] [[triangulated category]] follow from this simple definition when one decides to look at just the 1-categorical shadow given by the [[homotopy category of an (infinity,1)-category|homotopy category of the stable (infinity,1)-category]].

This is a general pattern here:

* $(\infty,1)$-categorical notions -- and in particular [[quasi-category|quasi-categorical]] notions are _conceptually_ simple and lend themselves to the formulation and description of higher categorical situations;

* but for concrete constructions in terms of them there is a wealth of tools with different areas of applicability, many of which have been understood and developed as theories in their own right.



#### 2.2 monoidal $\infty$-categories ####

A central aspect of geometric $\infty$-function theory is that we regard the collection $C(X)$ of $\infty$-functions assigned to a generalized space $X$ (concretely modeled as $QC(X)$, see section 3 below) not just as a higher vector space but naturally as a [[higher algebra]]. Indeed, the central two theorems/properties of [[geometric function theory]] concern the interplay between the _geometry_ of intersections or [[pullback]]s

$$
  \array{
     && Y_1 \times_X Y_2
     \\
     & \swarrow && \searrow
     \\
     Y_1 &&&& Y_2
     \\
     & \searrow && \swarrow
     \\
     && X
  }
$$

of generalized spaces and the _algebra_ of [[tensor product]]s 

$$
  C(Y_1) \otimes_{C(X)} C(Y_2)
  \,.
$$

In order to formulate this, one needs a good general theory of [[higher algebra]]. Just as ordinary [[algebra]] takes place inside a [[monoidal category]], [[higher algebra]] takes place in a [[monoidal (infinity,1)-category]]:

an &#176;$\infty$-monoid" or &#176;$\infty$-algebra" is an [[algebra in an (infinity,1)-category|algebra/monoid object in a monoidal (infinity,1)-category]].

In order to characterize the $(\infty,1)$-categories $C(X)$ as algebra objects in such a sense we profit from the ease with which [[quasi-category|quasi-categories]] naturally reflect on themselves and allow us with comparative ease to talk about the [[(infinity,1)-category of (infinity,1)-categories]] $(\infty,1)Cat_1$.

Since $(\infty,1)Cat_1$ itself is a [[symmetric monoidal (infinity,1)-category]], we will essentially identity the $\infty$-algebras $C(X)$ as [[algebra in an (infinity,1)-category|algebra objects]] in $(\infty,1)Cat_1$.

But there is actually a slight technical simplification: we don't deal with _all_ $(\infty,1)$-categories, but just with [[presentable (infinity,1)-category|presentable (infinifty,1)-categories]]. See there for the (long) list of nice properties and characterization of presentable $(\infty,1)$-categories.

So

* presentable $(\infty,1)$-categories form the [[symmetric monoidal (infinity,1)-category of presentable (infinity,1)-categories]]  $Pr(\infty,1)Cat_1$;

* the $\infty$-algebras of $\infty$-functions $C(X)$ are [[algebra in an (infinity,1)-category|algebra objects in]] $Pr(\infty,1)Cat_1$.




#### basic ideas related to $\infty$-stacks ####

We place ourselves in the context of an [[(infinity,1)-category]]
$H$ of (possibly [[derived stack|derived]]) $\infty$-stacks, i.e. of [[(infinity,1)-sheaf|(infinity,1)-sheaves]].

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

* the first datum is: $S$ a [[small (infinity,1)-category]];

* let then $PSh(S) := Funct(S^{op}, \infty\text{-}Grpd)$ be the $(\infty,1)$-category
of [[(infinity,1)-functor]]s from the [[opposite (infinity,1)-category]] $S^{op}$
to the $(\infty,1)$-category of $\infty$-groupoids.

* the second datum is: $i : H \hookrightarrow PSh(S)$ a 
[[full and faithful (infinity,1)-functor|full (infinity,1)-subcategory]] of $PSh(S)$
such that the inclusion is a [[geometric morphism]] of  
[[(infinity,1)-topos|(infinity,1)-topoi]], i.e. such that $i$ has
a [[exact (infinity,1)-functor|left exact]] [[adjoint (infinity,1)-functor|left adjoint]]
$(-)^* : PSh(S) \to H$.

The same in one sentence: $H$ is a sub-[[(infinity,1)-topos]] of the [[(infinity,1)-topos]]
of [[(infinity,1)-presheaf|(infinity,1)-presheaves]] on $S$.

Or equivalently: $H$ is an [[(infinity,1)-category of (infinity,1)-sheaves]] on $S$.


Now the fairly explicit way:

There are various different but equivalent explicit realizations, or models,
for [[(infinity,1)-category|(infinity,1)-categories]]. 
Of these consider [[quasi-category|quasi-categories]], which are  
[[simplicial set]]s that are [[Kan fibration|weak Kan complex]]es,
and [[SSet]]-[[enriched category|enriched categories]]. 
These are related by the 
[[simplicial nerve of simplicial categories]]-functor: 

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

To get back to our [[(infinity,1)-category of (infinity,1)-sheaves]] $H$,
we describe it in terms of these models as follows.

* $S$ is some small [[simplicial set]] which we can assume to be a [[weak Kan complex]];

* $\infty\text{-}Grpd := N(Kan)$ is the [[simplicial set]] which is the image under
the [[simplicial nerve of simplicial categories]]-functor of the full [[SSet]]-subcategory
of [[SSet]] on [[Kan complex]]es;

* $PSh(S) = SSet(S^{op},\infty\text{-}Grpd)$ is just the simplicial set of
simplicial maps between the simplicial sets $S^{op}$ and $\infty\text{-}Grpd)$.

For explicitly constructing $H$ as a full sub-$(\infty,1)$-category of $PSh(S)$ 
in practice one usually switches from the [[quasi-category]] picture to 
the [[SSet]]-[[enriched category]] picture. So assume $H$ explicitly 
to be an [[SSet]]-[[enriched category]] and $i : H \to F(PSh(S))$
the suitable inclusion [[SSet]]-functor. 

Notice that its left adjoint $(-)^* : PSh(S) \to N(H)$ is 
[[(infinity,1)-sheafification]]: it sends every [[(infinity,1)-presheaf]]
to the corresponding [[(infinity,1)-sheaf]]. In other words, this is
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
often thinks of such $X$ as [[orbifold]]s. If we write $X_0 \hookrightarrow X$ for the
presheaf of objects in $X$, then 

* $Vect_\infty(X_0)$ is the $\infty$-groupoid of $\infty$-vector bundles on $X_0$

* $Vect_\infty(X)$ is the $\infty$-groupoid of _equivariant_ $\infty$-vector bundles on $X_0$,

where the equivariance in question is that encoded by the inclusion $X_0 \hookrightarrow X$.

This is notably relevant for the [[fundamental infinity-groupoid]]:

assume that our [[site]] $S$ is 
[[monoidal category|monoidal]] and
equipped with a cosimplicial object, i.e. a functor 
$\Delta_S : \Delta \to S$ from the [[simplex category]], 
such that $\Delta_S[0]$ is a [[generators]] of $S$,
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

Morphisms from the [[fundamental infinity-groupoid]] are also called [[local system]]s.



#### 2.4 derived loop spaces ####

* [[homotopy limit]]

* [[loop space object]]

* [[constant infinity-stack]]


#### 2.5 $E_n$-structures ####

* [[operad]]

  * [[category over an operad]]


### 3. perfect stacks ###

* [[(infinity,1)-category of (infinity,1)-sheaves]]

* [[derived stack]]

#### definition of a perfect stack ####

* [[compact object in an (infinity,1)-category]]

#### base change and projection formula ####

#### construcons of perfect stacks ####

### tensor products and integral transforms ###

#### tensor products of $\infty$-categories ####

#### sheaves on fiber products ####

#### geometric base stacks ####


### applications ###



#### centers and traces ####

 * [[span trace]]

 * [[co-span co-trace]]


#### centers of convolution categories ####

#### higher centers ####

### epilogue:  topological field theory ###

* [[FQFT]]


#### topological field theory from perfect stacks ####

* [[sigma-model]]

#### Deligne-Kontsevich conjectures for derived centers ####




## Character Quantum Field Theory ##

* [[ringed site]]

* [[D-module]]

### and so on ###


# Background literature #

For the general [[(infinity,1)-category|(infinity,1)-categorical]] formalism

* [[Jacob Lurie]], [[Higher Topos Theory]].

For the [[stable (infinity,1)-category|stable]] aspects

* [[Jacob Lurie]], [[Stable Infinity-Categories]].
