There are various different-looking definitions of the general notion of _cohomology_ in different contexts, some familiar, some more exotic. It turns out that all of them are subsumed in the following general definition.

A non-technical account of some concepts in cohomology from this perspective is at 

* [[motivation for sheaves, cohomology and higher stacks]].


#Definition#

## General (or "nonabelian" or "unstable") cohomology ##

Given an [[(∞,1)-topos]] $\mathbf{H}$, for any two [[objects]] $X$, $A$ of $\mathbf{H}$ the **cohomology** of $X$ with coefficients in $A$ is nothing but the [[hom-space]] $\mathbf{H}(X,A)$ (an [[∞-groupoid]]).

More precisely:

* the [[objects]] $ c \in \mathbf{H}(X,A)$ are the **cocycle**s on $X$ with values in $A$;

* the [[morphisms]] $\lambda : c \to c'$ in $\mathbf{H}(X,A)$ are the **coboundaries** between cocycles;

* the higher morphisms in $\mathbf{H}(X,A)$ are the **higher coboundaries** or **coboundaries of coboundaries**.

* the equivalence classes $[c] \in \pi_0 \mathbf{H}(X,A)$ are the **cohomology classes**.

Hence for $H = Ho_{\mathbf{H}}$ the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathbf{H}$, the _cohomology set_ with coefficients in $A$ is

$$
  H(X,A) := Ho_{\mathbf{H}}(X,A)
  \,.
$$

This is itself a group -- the [[cohomology group]] -- if $A$ happens to carry a group structure (being a [[2-group]] or [[cat-n-group]] or the like).

## relation to homotopy ##

By abstract [[duality]], cohomology is dual to [[homotopy (as an operation)]].

The cohomology _of_ $X$ with coefficients in $A$ is the [[homotopy]] of $A$ with co-coefficients in $X$.

## objects classified by cohomology classes ##

For $g : X \to A$ a cocycle, one says that its [[fibration sequence|homotopy fiber]] $P \to X$ is the
object **classified by the cohomology class*.

Such an object usually has the interpretation of a [[principal ∞-bundle]]. Special cases of this are [[principal bundles]], [[gerbes]], [[principal 2-bundles]], etc.

### Remarks ###

* Notice that this definition is in a way the very point of the notion of [[(∞,1)-topos]]: an [[(∞,1)-topos]] is supposed to be an [[(∞,1)-category]] which behaves structurally exactly like the [[(∞,1)-category]] [[Top]] of [[topological spaces]]. Since cohomology of topological spaces is nothing but homotopy classes of maps between topological spaces, the analogous statement should be true in a general [[(∞,1)-topos]]. This is what the above definition asserts.


## Abelian (stable) cohomology ##

Analogous to the above, but with $H$ now
a [[stable (∞,1)-category]]. 

+--{.query}

[[Eric]]: Could someone explain how this relates to the version of <a href="http://en.wikipedia.org/wiki/Cohomology">cohomology I am familiar with</a>? Where is the coboundary?

[[Urs Schreiber|Urs]]: I have moved the discussion of the answer to this case now to [[chain homology and cohomology]].

=--




#Remarks#

## Grading ##

Notice that the grading one usually sees on cohomology classes is in the above definition entirely encoded in the [[higher category theory|categorical degree]] of the coefficient object. The cohomology $H(X,A)$ is the usual degree $0$ cohomology with coefficients in $A$. Cohomology of other degree can be obtained by looping or delooping the coefficients $A$. For example, if $A$ is a 0-type which is $n$-times de-loopable to an $n$-[[homotopy n-type|type]] $B^n A$, then degree $n$ cohomology with coefficients in $A$ is cohomology with coefficients in $\mathbf{B}^n A$: $H^n(X,A) := H(X, \mathbf{B}^n A)$. Similarly, looping can be used to define negative cohomology.

#Examples#

* classes of special cases of cohomologies with their own entries include

  * [[chain homology and cohomology]]

  * [[group cohomology]].

  * [[generalized (Eilenberg-Steenrod) cohomology]]

  * [[abelian sheaf cohomology]]

  * [[nonabelian cohomology]]

  * [[Cech cohomology]]

  * [[differential cohomology]]

    * [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]]

  * [[twisted cohomology]]



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

* [[Cech cohomology]] is the technique of computing $H(X,A)$ by computing 1-categorical [[hom-sets]] $C(\hat X,A)$ on _resolutions_ of the domain object $X$.

* The technique of computing [[abelian sheaf cohomology]] by computing the [[derived global section functor]] is similarly a technique of computing $H(X,A)$ in terms of 1-categorical [[hom-sets]] $C(X,\hat A)$ into _resolutions_ of the coefficient object (namely [[injective resolutions]]).

* [[monadic cohomology|Monadic cohomology]], like [[Cech cohomology]], is concerned with 1-categorical resolutions of the coefficient object in terms of [[bar constructions]]...

* Differential cohomology theories are effectively the cohomology theories of [[fundamental ∞-groupoids]]. 

#History and reference#

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

* Dan Dugger, [Sheaves and homotopy theory](http://www.uoregon.edu/~ddugger/cech.html) .


Essentially by applying these general constructions in the presence of a smooth [[fundamental ∞-groupoid]] functor $\Pi : H \to H$ one obtains _differential_ cohomology. More on that is at [[schreiber:Differential Nonabelian Cohomology]].

#Related blog entries#

* David Corfield, [Cohomology and Homotopy](http://golem.ph.utexas.edu/category/2009/06/cohomology_and_homotopy.html)


# Discussion #

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

