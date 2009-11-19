<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include (infinity,1)-topos - contents]]
</div>

#Contents#
* tic
{:toc}


## Idea ## 

There are various different-looking definitions of the general notion of _cohomology_ in different contexts, some familiar, some more exotic. 

The claim is all these notions of cohomology are special cases of -- and in many instances special concrete _models_ for -- the following general idea:

Cohomology is something associated to a given [[(∞,1)-topos]] $\mathbf{H}$. For $X, A$ two objects of $\mathbf{H}$, the **cohomology of $X$ with coefficients in $A$** is the set of connected components of the [[∞-groupoid]] of morphisms from $X$ to $A$ in $\mathbf{H}$:

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$

This is well familiar for the special case that $\mathbf{H} = $ [[Top]] is the [[(∞,1)-topos]] of [[topological space]]s. In this context for instance for $A := K(\mathbb{Z}, n)$ an [[Eilenberg-MacLane space]], we have that for $X$ any topological space that

$$
  \pi_0 \mathbf{H}(X,K(\mathbb{Z},n)) = H^n(X,\mathbb{Z})
$$

coincides with the "ordinary" [[integral cohomology]] of $X$.

This definition in [[Top]] alone already goes a long way. By the [[Brown representability theorem]] all cohomology theories that are called [[generalized (Eilenberg-Steenrod) cohomology]] theories are of this form, for $A$ a topological space that is part of a [[spectrum]]. This includes everything that is traditionally just called "a [[cohomology theory]]", such as [[K-theory]], [[elliptic cohomology]], [[tmf]], [[complex cobordism cohomology theory|complex cobordism]], etc.

Another big complex of notions of cohomology that on first sight maybe does not seem to fit into this pattern is [[abelian sheaf cohomology]]. Usually this is introduced and defined in the language of [[derived functor]]s. However, derived functors are nothing but a tool, or presentation, for encoding [[(∞,1)-categorical hom-space]]s such as $\mathbf{H}(X,A)$ in cases where $\mathbf{H}$ is [[presentable (∞,1)-category|presented]] by a [[homotopical category]] or [[model category]].

Indeed, it turns out that an old result from the 1960s, **Verdier's hypercovering theorem** effectively shows that what was introduced as [[abelian sheaf cohomology]] is really nothing but an instance of the above general setup. A particularly clear-sighted understanding of this fact was presented in 

* Ken Brown, [[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]].

Therein Brown considers a slightly simplified version of the [[model structure on simplicial presheaves]] -- which today is known to be one of the standard [[models for ∞-stack (∞,1)-toposes]] $\mathbf{H}$ -- rederives Verdier's hypercovering theorem and shows that ordinary [[abelian sheaf cohomology]] is indeed nothing but $\pi_0 \mathbf{H}(X,A)$ in such an [[(∞,1)-topos]], for the special case that the [[simplicial presheaf]] $A$ happens to be objectwise in the image of the [[Dold-Kan correspondence]], i.e. for the special case that $A$ is a _maximally abelian_ [[∞-stack]].

One can then understand various "cohomology theories" as nothing but tools for _computing_ $\pi_0 \mathbf{H}(X,A)$ using the known presentations of [[(∞,1)-categorical hom-space]]s: for instance [[?ech cohomology]] computes this spaces by finding cofibrant models for $X$, called [[?ech nerve]]s. Dual to that, most texts on [[abelian sheaf cohomology]] find fibrant models for $A$: called injective resolutions.

In other words, abelian sheaf cohomology is of the exact same nature as the familiar cohomology of [[topological space]]s (and hence of [[spectrum|spectra]]) if only we switch from the archetypical [[(∞,1)-topos]] [[Top]] to a more general [[(∞,1)-category of (∞,1)-sheaves|∞-stack (∞,1)-topos]]. And abelian sheaf cohomology in turn subsumes many special cases, such as [[Deligne cohomology]] or [[etale cohomology]].

But this also shows that abelian sheaf cohomology itself is just a very special case of cohomology in an $\infty$-stack $(\infty,1)$-topos: the highly abelian case. For coefficient objects $A \in \mathbf{H}$ that are not maximally abelian (not degreewise in the image of the [[Dold-Kan correspondence]]) the cohomology of an $\infty$-stack topos is a [[nonabelian cohomology]], one that classifies [[principal bundle]]s, nonabelian [[gerbe]]s, [[principal 2-bundle]]s and indeed [[principal ∞-bundle]]s.

And this in turn includes various other notions as special cases. For instance [[group cohomology]] is nothing but the cohomology in $\mathbf{H} = $ [[∞Grpd]] on objects $X = \mathbf{B}G$ that are [[delooping]]s of [[group]]s. And what is called _nonabelian group cohomology_ is nothing but the general case of this where there is no restriction on the coefficient object $A$. Here we can once again replace $\infty Grpd$ -- which is the $(\infty,1)$-topos of $\infty$-stacks on the point -- by a more general $\infty$-stack $\infty$-topos. For instance if we take the underlying [[site]] to be [[Diff]], the category of smooth [[manifold]]s, then the objects of $\mathbf{H} = Sh_{(\infty,1)}(Diff)$ are [[Lie ∞-groupoid]]s. Their cohomology is generalized group cohomology that knows about smooth structure: _smooth group cohomology_ . In this context for instance one can give cohomological interpretations of smooth realizations of the [[string 2-group]] or the [[fivebrane 6-group]].

There are some slight variations on the theme that cohomology is all about connected components of hom-spaces in [[(∞,1)-topos]]es: by looking at [[pullback]]s of such hom-spaces instead, one finds all variants of [[twisted cohomology]]. From there, one finds abelian [[differential cohomology]]. And then [[schreiber:Differential Nonabelian Cohomology|nonabelian differential cohomology]].

A non-technical account of some concepts in cohomology from this perspective is at 

* [[motivation for sheaves, cohomology and higher stacks]].


## Definition ##

### General (or "nonabelian" or "unstable") cohomology ###

Given an [[(∞,1)-topos]] $\mathbf{H}$, for any two [[objects]] $X$, $A$ of $\mathbf{H}$ the **cohomology** of $X$ with coefficients in $A$ is nothing but the [[hom-space]] $\mathbf{H}(X,A)$ (an [[∞-groupoid]]).


More precisely:

* the [[objects]] $ c \in \mathbf{H}(X,A)$ are the **cocycles** on $X$ with values in $A$;

* the [[k-morphisms]] in $\mathbf{H}(X,A)$ for $k \gt 0$ are the **coboundaries**;

* the equivalence classes $[c] \in \pi_0 \mathbf{H}(X,A)$ are the **cohomology classes**.

Hence for $H = Ho_{\mathbf{H}}$ the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathbf{H}$, the _cohomology set_ with coefficients in $A$ is

$$
  H(X,A) := Ho_{\mathbf{H}}(X,A)
  \,.
$$

This is itself a group -- the [[cohomology group]] -- if $A$ happens to carry a group structure (being a [[2-group]] or [[cat-n-group]] or the like).

### What this mean in more detail ###

Or, in the language of self-described 'old farts' such as [[Jim Stasheff]]:

> Ordinary nonabelian cohomology in degree 1 of a 'nice' topological space $X$ with values in a discrete (and possibly nonabelian) group $G$ can be defined as  the pointed set of homotopy classes of maps of topological spaces from $X$ into the classifying space $B G$. The content of *nonabelian cohomology* is the generalization of this statement to cohomology in higher degree. The content of general  nonabelian *differential* cohomology is moreover the generalization of nonabelian cohomology to generalized spaces with extra structure, in particular with smooth structure.

>Henceforth we will refer to * spaces * meaning perhaps some generalization or restriction, e.g. smooth spaces, and occasionally specify the nature of the generalization.   For spaces $X$,$A$,  we denote by $\mathcal{H}(X,A) = \mathrm{Maps}(X,A)$  the $(\infty,0)$-category of maps from $X$ to $A$. To emphasize the relation to cohomology,  we name these maps as cocycles and refer to $\mathcal{H}(X,A) = \mathrm{Maps}(X,A)$ as the cohomology of X with coefficients in A: the objects in $\mathrm{Maps} (X,A)$ are the $A$-valued cocycles on $X$, the morphisms are homotopies (or coboundaries) between these and the higher morphisms  are homotopies between homotopies, etc. The connected components in $\mathrm{Map}(X,A)$ are the cohomology classes, $H(X,A)=\pi_0 \mathrm{Map}(X,A)$. These are the sets of morphisms in the homotopy category $H$ of $\mathcal{H}$.

>For instance for $G$ an ordinary abelian group and $X$ a nice topological space, the choice $A = K(G,n)$ (an Eilenberg-Mac Lane space) yields the ordinary cohomology $H^n(X,G) = H(X,K(G,n)) = \pi_0\mathcal{H}(X,A)$.

>If $A$ is pointed in that it is equipped with a morphism ${}_* \overset{\mathrm{pt}_A}\rightarrow A $, then $\mathcal{H}(X,A)$ is naturally pointed with point $X \to {}_* \overset{\mathrm{pt}_A}\rightarrow A,$ the trivial $A$-cocycle on $X$. In particular, if $A$ is the delooping,  $A = \mathbf{B}G$, of a group-like space $G$ in $\mathcal{H}$ (an $\infty$-group or $A_\infty$-space) and if $g : X \to \mathbf{B}G$ is a cocycle, then the homotopy fiber of $g$, i.e. the   homotopy pullback $P \to X$ of the point of $A$ in 
$$
  \array{
    P          & \rightarrow            & {}_* \\
    \downarrow &                        & \downarrow \\
    X          & \overset{g}\rightarrow & \mathbf{B}G
  }
$$
>is the $G$-principal bundle classified by the cocycle $g$.

+-- {: .query}
Jim, I\'ve formatted this as if it were a quotation, since it looks like you pasted some LaTeX code from a longer article.  Remove the `>`s if you don\'t like that.  ---Toby

=--


### relation to homotopy ###

By abstract [[duality]], cohomology is dual to [[homotopy (as an operation)]].

The cohomology _of_ $X$ with coefficients in $A$ is the [[homotopy]] of $A$ with co-coefficients in $X$.

Therefore a more suitable term would be [[cohomotopy]].

## objects classified by cohomology classes ##

For $g : X \to A$ a cocycle, one says that its [[fibration sequence|homotopy fiber]] $P \to X$ is the
object **classified by the cohomology class*.

Such an object usually has the interpretation of a [[principal ∞-bundle]]. Special cases of this are [[principal bundles]], [[gerbes]], [[principal 2-bundles]], etc.

### Remarks ###

* Notice that this definition is in a way the very point of the notion of [[(∞,1)-topos]]: an [[(∞,1)-topos]] is supposed to be an [[(∞,1)-category]] which behaves structurally exactly like the [[(∞,1)-category]] [[Top]] of [[topological spaces]]. Since cohomology of topological spaces is nothing but homotopy classes of maps between topological spaces, the analogous statement should be true in a general [[(∞,1)-topos]]. This is what the above definition asserts.

## Remarks ##

### Grading ###

Notice that the grading one usually sees on cohomology classes is in the above definition entirely encoded in the [[higher category theory|categorical degree]] of the coefficient object. The cohomology $H(X,A)$ is the usual degree $0$ cohomology with coefficients in $A$. Cohomology of other degree can be obtained by looping or delooping the coefficients $A$. For example, if $A$ is a 0-type which is $n$-times de-loopable to an $n$-[[homotopy n-type|type]] $B^n A$, then degree $n$ cohomology with coefficients in $A$ is cohomology with coefficients in $\mathbf{B}^n A$: $H^n(X,A) := H(X, \mathbf{B}^n A)$. Similarly, looping can be used to define negative cohomology.

## Examples ##

* classes of special cases of cohomologies with their own entries include

  * [[chain homology and cohomology]]

  * [[group cohomology]].

  * [[generalized (Eilenberg-Steenrod) cohomology]]

    * [[integral cohomology]]

    * [[K-theory]]
  
    * [[elliptic cohomology]]
  
    * [[tmf]]

    * [[complex cobordism cohomology theory|complex cobordism]]

  * [[abelian sheaf cohomology]]

    * [[Deligne cohomology]]

    * [[etale cohomology]]

  * [[nonabelian cohomology]]

    * [[principal bundle]]

    * [[gerbe]]/[[principal 2-bundle]]

    * [[principal ∞-bundle]]
 
    * [[orientation]], [[spin structure]], [[string structure]], [[fivebrane structure]]

  * [[?ech cohomology]]

  * [[twisted cohomology]]

  * [[equivariant cohomology]]

  * [[differential cohomology]]

    * [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]]




* The archetypical example for [[nonabelian cohomology]] theory is the [[(∞,1)-topos]] $H = $ [[Top]], the [[(∞,1)-category]] of [[topological spaces]]. For $X$ and $A$ two topological spaces, the cohomology classes of $X$ with values in $A$ are the homotopy classes of continuous maps $X \to A$. For $A = K(a,n)$ an [[Eilenberg-Mac Lane space]] with $a$ an abelian group this reproduces "ordinary cohomology" of spaces. For $n \gt 1$ this special case happens to be actually abelian.
 For $A = B G$ a [[classifying space]] of a topological [[group]] $G$, this reproduces degree 1 [[nonabelian cohomology]] $H^1(X,G)$. In general, for $A$ an $n$-type, $H(X,A)$ is topological degree-$n$ [[nonabelian cohomology]].

* The archetypical example for abelian cohomology theory is the [[stable (∞,1)-topos]] $H = $ [[Spec]], the [[stable (∞,1)-category]] of [[spectrum|spectra]]. This is the case in the literature often addressed as [[generalized cohomology]], since it generalizes the entities specified by the Eilenberg--Steenrod axioms. But really, the general concept of cohomology is more general than this "generalized cohomology". 

  * "ordinary" cohomology is cohomology with coefficients in the [[Eilenberg-MacLane spectrum]]

  * K-theory is cohomology with coefficients in the [[K-theory spectrum]]

  * elliptic cohomology is somehow subsumes by cohomology with coefficients in [[tmf]].

* Objects in general nonabelian cohomology are usually called [[∞-stacks]] are 
[[(∞,1)-sheaves]], since every Grothendieck--Rezk--Lurie [[(∞,1)-topos]] arises as a [[(∞,1)-category of (∞,1)-sheaves]].

* [[abelian sheaf cohomology|Abelian sheaf cohomology]] for complexes of sheaves in non-negative degree is cohomology of the sub-[[(∞,1)-topos]] of $\infty$-stacks which take values in [[∞-groupoids]] which, under the [[Dold-Kan correspondence]] come from [[chain complexes]].

* [[abelian sheaf cohomology|Abelian sheaf cohomology]] for unbounded complexes of sheaves is stable cohomology of the [[stable (∞,1)-topos]] of [[spectrum]]-valued [[(∞,1)-sheaves]].

Several familiar "cohomology theories" are not so much genuine cohomology theories as rather computational techniques for computing certain cohomology classes in an [[(∞,1)-category]] by using 1-categorical tools of [[homotopy coherent category theory]] such as [[model categories]], [[derived categories]] and the like.

* [[?ech cohomology]] is the technique of computing $H(X,A)$ by computing 1-categorical [[hom-sets]] $C(\hat X,A)$ on _resolutions_ of the domain object $X$.

* The technique of computing [[abelian sheaf cohomology]] by computing the [[derived global section functor]] is similarly a technique of computing $H(X,A)$ in terms of 1-categorical [[hom-sets]] $C(X,\hat A)$ into _resolutions_ of the coefficient object (namely [[injective resolution]]s).

+--{.query}
Zoran: I am not happy with this assertion. First of all the notion of the derived functor is fundamental and it makes sense even in setups when the injective resolutions do not exist. Abelian sheaf cohomology IS a derived functor of the global sections functor, not a specific technique to computing it. On the other hand, the injective resolutions ARE a specific technique to compute the derived functor. It is also not clear in this entry if it is about sheaves on topological spaces or on sites or some more general setup. 
=--

* [[monadic cohomology|Monadic cohomology]], like [[?ech cohomology]], is concerned with 1-categorical resolutions of the coefficient object in terms of [[bar constructions]]...

* Differential cohomology theories are effectively the cohomology theories of [[fundamental ∞-groupoids]]. 

## History and references ##

This general perspective on cohomology was established 35 years ago in

* Kenneth Brown, [[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]] 

and apparently known in one form or other before that.

This article establishes that 

* all of [[abelian sheaf cohomology]] 

  * with all its special cases like, say, [[Deligne cohomology]], 

* all [[generalized (Eilenberg-Steenrod) cohomology]] 

  * with simple things like [[Eilenberg-MacLane spectrum|ordinary cohomology]] and more intricate things like [[K-theory spectrum|K-theory]] and [[tmf]]), 

* as well as [[nonabelian cohomology]] 

  * classifying [[gerbes]] and [[principal ∞-bundles]] 

* as well as the more mundane special cases of this like [[group cohomology]] and, yes, cohomology of cochain complexes itself

are naturally special cases of one single concept: that of hom-sets 

$$
  H(X,A) := Ho_{SSh}(X,A)
$$ 

in the [[homotopy category]] of [[∞-groupoid]]-valued [[sheaves]].

The only fundamental new addition to this insight that is available now and wasn't available 35 years ago is that 


* These categories $H = Ho_{SSh}$ are precisely the [[homotopy category of an (infinity,1)-category|hom-wise decategorification]] of [[(∞,1)-category of (∞,1)-sheaves]] otherwise known as the [[(∞,1)-topoi]] of [[∞-stacks]].


This is propositon 6.5.2.1 in [[Jacob Lurie]]'s [[Higher Topos Theory]] and builds on the fundamental work by K. Brown, Joyal and Jardine and others on the 
[[model structure on simplicial presheaves]].

For a _motivation_ of these definitions from the point of view of cohomology as a homotopy hom-set of $\infty$-stacks see for instance the introductory pages of

* Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf)) .


Essentially by applying these general constructions in the presence of a smooth [[fundamental ∞-groupoid]] functor $\Pi : H \to H$ one obtains _differential_ cohomology. More on that is at [[schreiber:Differential Nonabelian Cohomology]].

A discussion of cohomology in the general sense discussed above, using tools of [[model category]] theory for [[simplicial object]]s, is

* [[Brian Conrad]], _Cohomological descent_ ([pdf](http://math.stanford.edu/~conrad/papers/hypercover.pdf))

## Related blog entries ##

* David Corfield, [Cohomology and Homotopy](http://golem.ph.utexas.edu/category/2009/06/cohomology_and_homotopy.html)


## Discussion ##

+-- {: .query}
Is it really true/known that *all* forms of cohomology is subsumed in this definition? I would be really happy if this was true, but I am not convinced yet. Some questions:

Is it true that cohomology theories defined for algebraic varieties over a field of characteristic p, or over a p-adic field, are subsumed in the above definition? Examples: Crystalline cohomology, rigid cohomology, syntomic cohomology. If so, is this explained somewhere? Is it clear to anyone that the language of infinity-stacks is the right one if you are trying to understand cohomology of "arithmetic schemes", i.e. schemes over base rings like the integers?

For applications of many cohomology theories in arithmetic geometry, it is of crucial importance that the cohomology groups carry "extra structure", for example Galois action, Frobenius action, or Hodge structure. Is it the case that the language of infinity-stacks is the most natural language for understanding such "extra structure"? Has anyone thought about this at all?

Am grateful for any (partial) answers or references.

[[Urs Schreiber|Urs]]: Thanks for the question. What is subsumed in the definition below is

* every kind of [[abelian sheaf cohomology]];

* [[nonabelian cohomology|nonabelian sheaf cohomology]];

* generalized Eilenberg-Steenrod-type [abelian cohomology](http://en.wikipedia.org/wiki/List_of_cohomology_theories) 

The observation of the unity of these goes back to at least [[BrownAHT]], the main new bit here being that the model-theoretic constructions used there (or rather the [[category of fibrant objects|Brown category]] used there) is nicely understood as presenting $(\infty,1)$-categories, which unifies the picture still a bit more.

Please correct me if the following is wrong, but my understanding is that for instance [crystalline cohomology](http://en.wikipedia.org/wiki/Crystalline_cohomology) is a kind of sheaf cohomology, too, where the only terminological twist is that we say that the crystalline cohomology of some site is by definition the sheaf cohomology of a certain other site associated to it (its crystalline site). Similarly for syntomic cohomology and the syntomic site.

So I would tend to think that all these are subsumed under abelian sheaf cohomology. But I'd be grateful for being corrected here, if necessary.



=--

