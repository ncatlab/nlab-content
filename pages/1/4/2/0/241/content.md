

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

Classically, we have:

+-- {: .num_defn}

A __Grothendieck topos__ $\mathcal{T}$ is a category that admits a [[geometric embedding]]

$$
  \mathcal{T} \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  PSh(C)
$$

in a [[presheaf]] category, i.e., a full and faithful functor that has a left exact left adjoint. 

This is equivalently the [[category of sheaves]] ([[Set]]-valued [[presheaves]] satisfying the sheaf condition) over a [[small category|small]] [[site]].

=--

Since smallness can be relative, we also have:

+-- {: .num_defn}

For a given fixed [[ETCS|category of sets]] $S$, a __Grothendieck topos__ over $S$ is a [[category of sheaves]] ($S$-valued [[presheaves]] satisfying the sheaf condition) over a [[site]] which is [[small category|small]] relative to $S$, that is a site [[internal category|internal]] to $S$.
=--

Note that a Grothendieck topos is a [[topos]] because (or if) $S$ is.

The [[site]] is not considered part of the structure; different sites may give rise to [[equivalence of categories|equivalent]] category of sheaves.

By the general theory of [[geometric morphisms]], every Grothendieck topos sits inside a category of [[presheaf|presheaves]] by a [[geometric embedding]] $Sh(S) \hookrightarrow PSh(S)$. 

* This may be taken as an alternative definition of [[sheaf]]: since [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] are bijectively given by [[geometric embeddings]],  instead of explicitly defining a sheaf as a presheaf satisfying [[descent]], one may define categories of sheaves as geometric embeddings into presheaf categories. 

* For details on the relation between the two perspectives see [[geometric embedding]].

* This perspective is useful for defining the [[vertical categorification]] of sheaves: [[stacks]] and [[∞-stacks]]: the higher categories of these may be defined as geometric embeddings into higher categories of presheaves. This has been worked out in detail for [[(∞,1)-categories]]. See [[(∞,1)-category of (∞,1)-sheaves]].

* Sometimes it is useful to distinguish between [[petit topos]] and [[gros topos]].


## Properties

### General

+-- {: .num_prop #LocallyPresentable}
###### Proposition

Every Grothendieck topos is a [[locally presentable category]].

=--

([Borceux 94, vol 3, prop. 3.4.16](#Borceux94))

+-- {: .num_prop #total}
###### Proposition

Every Grothendieck topos is a [[total category]] and a [[cototal category]].

=-- 

+-- {: .proof} 
###### Proof 

From the page [[total category]], totality follows from the fact that a Grothendieck topos is 

* [[cocomplete category|Cocomplete]], 
* [[well-powered category|Well-copowered]] (because [[quotient]] objects of an [[object]] $X$ are in [[bijection]] with [[equivalence relations]] on $X$, and there is a [[small set]] of these because a Grothendieck topos is well-powered), and 
* Has a [[generator]] (e.g., the [[coproduct]] of all [[representable functor|representables]] for a [[small site]] presentation). 

Dually, a Grothendieck topos is 

* [[complete category|Complete]], 
* [[well-powered category|Well-powered]] (because [[subobjects]] of an [[object]] $X$ are in [[bijection]] with elements of a [[small set|small]] [[hom-set]] $\hom(X, \Omega)$), and 
* Has a [[cogenerator]] (e.g., the [[product]] of [[power objects]] $\Omega^c$ where $c$ ranges over representables for a small site presentation). 

Therefore a Grothendieck topos is also cototal. 

=--


### Giraud\'s axiomatic characterization
{#Giraud}

Giraud characterized Grothendieck toposes as categories satisfying certain [[exactness property|exactness]] and [[small set|small]] [[complete category|completeness]] properties (where "small" is again relative to the given category of sets $S$). The exactness properties are elementary (not depending on $S$), and are satisfied in any elementary [[topos]], or even a [[pretopos]].

[[Giraud's theorem]] characterises a Grothendieck topos as follows:

1. a [[locally small]] [[category]] with a small [[generating set]],
2. with all finite [[limits]],
3. with all small [[coproducts]], which are [[disjoint coproduct|disjoint]], and [[pullback stability|pullback-stable]],
4. where all [[congruences]] have effective [[quotient objects]], which are also pullback-stable.

These conditions are equivalent to

* a [[locally small]] [[infinitary pretopos]] with a small generating set.

See the [[Elephant]], theorem C.2.2.8.  (There, the assumption of local smallness is not stated explicitly, but it is included in the definition of $\infty$-pretopos by way of [[well-powered category|well-poweredness]]; on the nLab it is not so included, so we have to state it explicitly.  To see that it is necessary, note that if $U$ and $V$ are [[Grothendieck universes]] with $U\in V$, then $Set_V$ satisfies all the other conditions relative to $Set_U$, but is not locally small and is not a Grothendieck topos.)  See also [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Topos#Giraud.27s_axioms).

Sometimes (3,4) are combined and strengthened to the statement that the category has all small [[colimits]], which are effective and pullback-stable.  However, this is a mistake for two reasons: it is a significantly stronger axiomatisation (since without the small generating set, not every infinitary pretopos has this property), and it is not valid in weak foundations (while the definition given above is).

### Street's axiomatic characterization 
{#Streetcharacterization}

Augmenting the aforementioned Proposition \ref{total} that Grothendieck toposes are total categories, [Street](#Street) more or less characterizes Grothendieck toposes as *lex total* categories having the same "size" as $Set$. 

In more detail: we take as background set theory ZFC + "there is a strongly inaccessible cardinal" $\kappa$; equivalently, the existence of a single [[Grothendieck universe]] $U$ (a set of "small sets"). Supposing given a model $V$ of $ZFC+universe$, "category" shall then refer to category theory interpreted in $V$. Let $Set$ be the category of small sets; note that the set of morphisms of $Set$ has size $\kappa$. 

Recall that locally small category $E$ is [[lex total category|lex total]] if the [[Yoneda embedding]] $y: E \to [E^{op}, Set]$ has a [[left exact functor|left exact]] [[left adjoint]]. 
 

+-- {: .num_theorem} 
###### Theorem 
**(Street)** 
A category $E$ is a Grothendieck topos iff it is lex total and the size of the set of isomorphism classes of objects is $\kappa$ or less. 
=-- 

+-- {: .num_remark} 
###### Remark 
This result is in the spirit of saying "every Grothendieck topos is the category of [[sheaves]] with respect to the [[canonical topology]] on itself". Putting aside set-theoretic issues, it suggests that Grothendieck toposes be seen as analogous to [[frames]], which may be defined as lex total objects in $\mathbf{2}$-$Cat$. In this setting, the appropriate morphisms are left exact left adjoints, so that Grothendieck toposes and [[geometric morphisms]] between them would be analogous to [[locales]] and [[continuous maps]] between them. 

One can deduce formally that lex total categories are [[locally cartesian closed category|locally cartesian closed]] [[Heyting pretoposes]]. 
=-- 

### As lex reflections of categories of presheaves

[[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes]]

### As localic groupoids
 {#AsLocalicGroupoids}

Every Grothendieck topos is equivalent to the [[classifying topos of a localic groupoid]], every Grothendieck topos [[point of a topos|with enough points]] is equivalent to the classifying topos of a [[topological groupoid]], and in fact the 2-category [[Topos]] of Grothendieck toposes is equivalent to a localization of that of [[localic groupoids]].

See at _[[classifying topos of a localic groupoid]]_ for more.

### Internal logic

Being an [[elementary topos]], a Grothendieck has an [[internal logic]] that can be taken to be [[higher-order logic]] or a form of [[dependent type theory]].  It is also useful to take its internal [[geometric logic]], in particular because that is preserved by [[geometric morphisms]] and because every geometric theory has a Grothendieck [[classifying topos]].

Although the internal logic of a Grothendieck topos is [[constructive logic]], there are a number of principles that are true in every Grothendieck topos (at least, assuming the base topos [[Set]] is [[classical mathematics|classical]]) but are not constructively provable (and in particular can fail in other toposes).  Roughly speaking, many of these axioms assert that classicality fails "in only a [[small category|small]] way".  These include:

* [[WISC]]: every set has a weakly initial set of covers.
* The (constructive) [[axiom of multiple choice]] (AMC).
* The [[axiom of stack completions]].
* (allegedly) the local [[small cardinality selection axiom]] (SCSA).
* Every [[complete small category]] is a preorder.

## In weak foundations

We have two definitions of a Grothendieck topos:

*  the category of sheaves on some small site,
*  a category that satisfies Giraud\'s axioms (as listed above).

The theorem that these are equivalent can be proved in quite weak foundations, whether [[finitist mathematics|finitist]], [[predicative mathematics|predicative]], or [[constructive mathematics|constructive]] (or all three at once), as long as we axiomatize correctly given the caveats listed in the previous section.  Some hard-nosed predicativists (and even hard-nosed ZFC fundamentalists) may object to the language (on the ground that large categories such as $Set$ and other nontrivial Grothendieck toposes don\'t really exist), but they should accept the theorems when suitably phrased.

In predicative mathematics, however, we cannot prove that every Grothendieck topos is in fact a [[topos]]!  In fact, it is immediate that [[the category of sets]] is a Grothendieck topos, but $Set$ is an elementary topos if and only if [[power sets]] are small, which is precisely what predicativists doubt.  One can use the term __Grothendieck pretopos__ to avoid implying that we have an elementary topos.  On the other hand, since Grothendeick toposes came first, perhaps it is the definition of 'elementary topos' that is too strong.

Similarly, in finitist mathematics, we cannot prove that every Grothendieck topos has a [[natural numbers object]]; while in strongly predicative mathematics, we cannot prove that every Grothendieck topos is [[cartesian closed category|cartesian closed]].  In each case, once a property is accepted of $Set$ (the [[axiom of infinity]] and small [[function sets]], in these examples), it can be proved for all Grothendieck toposes.

Constructivism as such is irrelevant; even in [[classical mathematics]], most Grothendieck toposes are not [[boolean topos|boolean]].  However, for an analogous result, try the theorem that the [[category of presheaves]] on a [[groupoid]] (and hence any category of sheaves contained within it) is boolean.  (Again, $Set$ itself is an example of this.)

The theorem that every Grothendieck topos is [[cocomplete category|cocomplete]] is a subtle point; it fails only in finitist predicative mathematics.  (The key point in the proof is to generate the [[transitive relation|transitive closure]] $\sim^*$ of a binary relation $\sim$.  One proof defines $a \sim^* b$ to mean that $a \sim x_0 \sim \cdots \sim x_{n-1} \sim b$ for some $n$, which is predicative but infinitary; another defines $a \sim^* b$ to mean that $a \sim' b$ for every transitive relation $\sim'$ that contains $\sim$, which is finitary but impredicative.)


## Related concepts

* [[topos]]

  * **Grothendieck topos**,  [[category of sheaves]]

    * [[geometric logic]], [[geometric type theory]]

  * [[2-topos]]

  * [[(∞,1)-sheaf (∞,1)-topos]]

* [[lex total category]]

[[!include locally presentable categories - table]]


## History
  {#History}

From [[Colin McLarty]] (sent to the [Categories mailing list](https://www.mta.ca/~cat-dist/) on Apr 14, 2018):

> At the start of 1958 [[Grothendieck]] believed the correct [[Weil cohomology]] of a [[scheme]] $S$ would be the [[abelian sheaf cohomology|derived functor cohomology]] of some [[category]] $Ab(S)$
of [[sheaf of abelian groups|sheaves of Abelian groups]] on $S$ ---and $Ab(S)$ was likely to be the category of all Abelian [[group objects]] in some [[category of sheaves]] of [[sets]] on $S$.  He had no name yet for such conjectural categories of sheaves of sets but for later reference I will call this category $T(S)$.  It would require some new notion of sheaves of sets more general than the existing notion using topological spaces.  He had no concrete idea what this new notion of sheaf might be.  His experience in Kansas in 1955 suggested it  was likely to come from some new notion of espace etale over a scheme. and it should have some good exactness properties.

> On April 21, 1958 Grothendieck went to the Seminaire Chevalley to hear [[Serre]] describe isotrivial fiber bundles on a variety V, which are bundles that become trivial when pulled back to some surjective family of finite, unramified maps to V.  Serre showed this gave the expected one-dimensional Weil cohomology groups of V.  Grothendieck immediately told Serre it would work in all dimensions--which Serre found "very optimistic"" at the time.

> All of this is well documented in familiar sources.

> Grothendieck's 1973 topos lectures in Buffalo show that during Serre's talk Grothendieck saw the Weil espaces etales over a scheme $S$ should be patched together from Serre's unramified maps to $S$.  That is, the sought category $T(S)$ of sheaves of sets on S should be generated by the unramified maps to S, and should have arbitrary colimits of these, and finite limits.  He first sought to axiomatize this roughly the way his Tohoku paper had axiomatized sheaves of groups.

> A few changes came soon: He realized finite unramified maps should be replaced by flat unramified maps (just as topological espaces etales are trivial locally in the fiber and not on the base).  He abandoned the axiomatic approach to $T(S)$ as too vague and shifted to construction by sites.  And for sites he began treating sheaves as a kind of functor, rather than as espaces etales.  Only after the notion ot site developed would Giraud give his topos axioms, and no one has yet really taken a precise notion of espace etale much  beyond the topological case.

> But April 21 1958 was the birth of [[topos theory]]. The term topos came
later.  (Lots of people are not named on the day they are born.)

> As of the summer of 1973 Grothendieck's stated preferred definition of topos was still: a category with arbitrary [[colimits]], [[finite limits]], and a small generating set. He says over and over this is not quite adequate for proofs.  He says proofs require the notion of [[site]], or else the [[Giraud axioms]], but he calls the vaguer idea more intuitive and says that is the way to think about a topos.

> Also in 1973 Grothendieck says the objects in any topos should be seen as [[espaces etales]] over the [[terminal object]] of the topos, in a generalized sense that includes saying any orbit of a group action lies "etale" over a [[fixed point]].  Today, it is not obvious that this can work well in general.  In [[SGA4]] Grothendieck had already given evidence that it would work for [[petit topos]] but not [[gros topos]].  But still in 1973 he did say it. And it works perfectly for petit etale toposes---as long as we generalize the notion  of espace etale to include a Galois orbit (in an extension field) lying over a single point (in the ground field).


## References

A quick introduction of the basic facts of sheaf-topos theory is chapter I, "Background in topos theory" in 

* [[Ieke Moerdijk]], _Classifying Spaces and Classifying Topoi_ Lecture Notes in Mathematics 1616, Springer (1995)


Textbook accounts include

* {#Borceux94} [[Francis Borceux]], vol 3 of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

Grothendieck topoi appear around section III,4 there.
A proof of Giraud's theorem is in appendix A.


The proof of Giraud's theorem for [[(∞,1)-topoi]] is section 6.1.5 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Street's characterization of Grothendieck toposes is given in 

* {#Street}  [[Ross Street]], _Notions of topos_, Bull. Australian Math. Soc. 23 (1981), 199-208; MR83a:18014. ([pdf link](http://journals.cambridge.org/download.php?file=%2FBAZ%2FBAZ23_02%2FS000497270000705Xa.pdf&code=c6248e4fa6a517c9bb451e4f5abcf862)) 
 


[[!redirects Grothendieck toposes]]
[[!redirects Grothendieck topoi]]

[[!redirects Giraud axiom]]
[[!redirects Giraud axioms]]
[[!redirects Giraud's axiom]]
[[!redirects Giraud's axioms]]
[[!redirects Giraud\'s axiom]]
[[!redirects Giraud\'s axioms]]
[[!redirects Giraud/'s axiom]]
[[!redirects Giraud/'s axioms]]
[[!redirects Giraud's axiom]]
[[!redirects Giraud's axioms]]

[[!redirects sheaf topos]]
[[!redirects sheaf toposes]]
[[!redirects sheaf topoi]]
