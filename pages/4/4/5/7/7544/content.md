
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
* table of contents
{:toc}

## Idea

The notion of an _elementary (∞,1)-topos_ is an analogue of the notion of _[[elementary topos]]_ in [[(∞,1)-category theory]].  This is in contrast to the notion of a _Grothendieck_ _[[(∞,1)-topos]] [[equivalence of (∞,1)-categories|equivalent]] to an [[(∞,1)-category of (∞,1)-sheaves]]_, the analogue of a [[sheaf topos]], which is more specific (see [[geometric homotopy type theory]]).

Note that every _Grothendieck_ [[(∞,1)-topos]] provides [[categorical semantics]] for [[homotopy type theory]] with [[univalence|univalent]] weakly-Tarskian [[types of types]] and also [[higher inductive types]] (HITs).  Elementary $(\infty,1)$-toposes ought to be roughly the larger class of *all* $(\infty,1)$-categories that provide [[categorical semantics]] for such homotopy type theory.  More precisely, we will define an elementary $(\infty,1)$-topos to have the $(\infty,1)$-categorical structure that ought to correspond to that type-theoretic structure; a [[coherence theorem]] making it *actually* model the corresponding type theory is still unknown.

In general, the problem with "elementary-izing" the notion of $(\infty,1)$-topos is that Grothendieck $(\infty,1)$-toposes have many properties that are not reflected in type theory due to the finitary nature of type theory; the question is to find appropriate "finitary shadows" of them.  For instance, one can construct [[initial algebras for endofunctors]] using a [[transfinite induction]] argument; thus in type theory we postulate the existence of [[inductive types]].  Deciding what class of "infinitary constructions" that are available in Grothendieck $(\infty,1)$-toposes can be described finitarily by something that deserves the name "[[higher inductive type]]" is overall an open question, but we can obtain reasonable definitions by restricting the class of [[HITs]] we ask for.

## Definition (impredicative case)

There are at least two ambiguities in the above sketch of a definition based on type theory: what exactly do we assume of the [[universes]] ([[object classifiers]]), and what general class of [[HITs]] do we ask for?  One reasonable answer to the universe question is that every object should be contained in a universe closed under all the relevant operations, and one reasonable answer to the HITs question is just the non-recursive ones.  This leads to the following definition.

+--{: .num_defn}
###### Definition
An **elementary $(\infty,1)$-topos** is an $(\infty,1)$-category $\mathbf{E}$ such that

* $\mathbf{E}$ has finite [[(∞,1)-limit|limits and colimits]]
* $\mathbf{E}$ is [[locally cartesian closed (∞,1)-category|locally cartesian closed]]
* There exists a [[subobject classifier]] (an [[object classifier]] that classifies the collection of all [[monomorphisms in an (∞,1)-category]])
* For any morphism $f:Y\to X$ in $\mathbf{E}$, there exists an [[object classifier]] in $\mathbf{E}$ classifying a class of morphisms that (1) includes $f$ and (2) is closed under fiberwise finite limits and colimits, composition (i.e. dependent sums), and dependent products.
=--

Note that this definition is "impredicative" just like an [[elementary topos]], in that it has a classifier for *all* subobjects.  We can't categorify this to a classifier for all objects due to size paradoxes; the existence of "enough" object classifiers closed under all the basic operations is the "next best thing".  We will refer to an object classifier satisfying (2) above as a **universe**.

## Properties

It is reasonable to hope for a coherence theorem showing that any elementary $(\infty,1)$-topos in the above sense admits a model of homotopy type theory with non-recursive [[higher inductive type|HITs]] (corresponding to the finite colimits), univalent [[type of types|universes]] (perhaps only weakly Tarski ones), and [[propositional resizing]].  See, for instance, _[[homotopytypetheory:model of type theory in an (infinity,1)-topos]]_ and _[relation between type theory and category theory -- Univalent homotopy type theory and infinity-toposes](relation+between+type+theory+and+category+theory#HomotopyWithUnivalence)_.

In an elementary 1-topos we can construct finite colimits and dependent exponentials from non-dependent exponentials and the subobject classifier (or equivalently from [[power objects]]).  In the $\infty$-case this seems less likely to be true, since subobjects tell us less about objects that are not 0-truncated.  However, there is still a good deal of extra structure that "comes for free" from the above definition.

+-- {: .num_theorem}
###### Theorem
The initial object $0$ of $\mathbf{E}$ is [[strict initial object|strict]], i.e. any morphism $A\to 0$ is an equivalence.
=--
+-- {: .proof}
###### Proof
Just as for 1-categories, this is true in any cartesian closed $(\infty,1)$-category.  For if there is a morphism $f:A\to 0$ then the projection $A\times 0 \to A$ has a section $(1_A,f)$, so that $A$ is a retract of $A\times 0$; but $A\times 0 \cong 0$ by cartesian closedness since $(A\times -)$ has a right adjoint and hence preserves colimits.
=--

+-- {: .num_theorem}
###### Theorem
Binary coproducts in $\mathbf{E}$ are [[disjoint coproducts|disjoint]], i.e. the injections $i:A\to A+B$ and $j:B\to A+B$ are monic, and their pullback is initial.
=--
+-- {: .proof}
###### Proof
This is also just like a corresponding proof for 1-toposes (see [[toposes are extensive]]).  Define $R$ and $S$ to make the following squares pullbacks:
$$\array{ R & \xrightarrow{r} & A & \xleftarrow{s} & S\\
  ^{r'}\downarrow && \downarrow^i && \downarrow\\
  A & \xrightarrow{i} & A+B & \xleftarrow{j} & B}$$
Specifically, $(r,r')$ is the [[kernel pair]] of $i$.  In particular, there is an induced diagonal $\triangle : A \to R$ such that $r \triangle = 1_A$.  On the other hand, since $\mathbf{E}$ is locally cartesian closed, pullback preserves colimits, so $(r,s)$ is a coproduct diagram.  Thus, the pair of morphisms $1_R:R\to R$ and $\triangle \circ s : S\to R$ factor (uniquely) through some $h:A\to R$, so that in particular $h r = 1_R$.  Thus, $r:R\to A$ has both a left and a right inverse, so it is an equivalence, and hence $i$ is monic.  Dually, $j$ is monic.

Now we claim that any two morphisms $f,g:S\to X$ with domain $S$ are equivalent.  For the pair of morphisms $R \xrightarrow{r} A \to A+X$ and $S \xrightarrow{f} X \to A+X$ factor uniquely through $A$ (which, recall, is the coproduct $R+S$).  But since $r$ is an equivalence, this factorization must be (equivalent to) the left coprojection $A\to A+X$.  Therefore, the composite $S \xrightarrow{f} X \to A+X$ is equivalent to the composite $S \xrightarrow{s} A \to A+X$, and similarly so is the composite $S \xrightarrow{g} X \to A+X$.  Since $X\to A+X$ is monic by the previous paragraph, $f\simeq g$.

Finally, since $0$ is a strict initial object, $0\to S$ is monic.  And of course $1_S : S\to S$ is also monic, and these two monomorphisms are classified by two maps $f,g:S\to \Omega$ into the subobject classifier.  By the previous paragraph, $f\simeq g$, hence $S\cong 0$ and is initial.
=--

+-- {: .num_theorem}
###### Theorem
For any finite family of morphisms $\{f_i : Y_i \to X_i\}_{i\in I}$, there exists a universe classifying all the $f_i$.
=--
+-- {: .proof}
###### Proof
Since $f_i$ is the pullback of $\sum_i f_i$ along the injection $X_i \to \sum_i X_i$ (this follows from extensivity), a universe classifying $\sum_i f_i$ must also classify each $f_i$.
=--

In particular, we have "universe cumulativity":

+-- {: .num_cor}
###### Corollary
For any universe $p:V\to U$, there is a universe $p':V'\to U'$ that classifies both $p$ and $U\to 1$.
=--

+-- {: .num_theorem}
###### Theorem
All finite colimits are [[van Kampen colimit|van Kampen]].
=--
+-- {: .proof}
###### Proof
Since $\mathcal{E}$ is locally cartesian closed, all colimits are pullback-stable, so it suffices to show descent.  Suppose $D$ is a finite [[simplicial set]] and $F^\rhd:G^\rhd:D^\rhd \to \mathcal{E}$ are colimiting cones under diagrams $F,G:D\to \mathcal{E}$, and let $\alpha^\rhd : F\rhd \to G^\rhd$ be a natural transformation whose restriction $\alpha:F\to G : D\to \mathcal{E}$ is [[equifibered natural transformation|equifibered]].  Let $p:V\to U$ be a universe classifying $\alpha_d : F_d \to G_d$ for each vertex $d\in D_0$.  Then $\alpha$ is the pullback of $p$ along a cocone $q:G\to U$, yielding a cocone $r : \alpha \to p$ in $\mathcal{E}^\to$ which is equifibered.

Since $\alpha^\rhd$ is colimiting under $\alpha:D\to \mathcal{E}^\to$, we have an induced map $\alpha_\star \to p$, where $\star\in D^\rhd$ is the cocone vertex.  But since colimits are pullback-stable, the pullback of $G^\rhd$ along $p$ is a colimiting cocone under $F$, and hence isomorphic to $F^\rhd$.  Thus, $\alpha^\rhd$ is equifibered.
=--

+-- {: .num_theorem}
###### Theorem
There exists a [[natural numbers object]].
=--

Intuitively, it seems as if $\Omega(S^1)$ (which can be constructed using finite limits and colimits) ought to be the [[integers]] and we should be able to construct the natural numbers from it; but it is unclear to the authors of this page how to do that.  Instead, we can (using the impredicative subobject classifier) define the smallest subobject of an object classifier $p:V\to U$ that contains the initial object and is closed under taking coproducts with the terminal object.  This is almost right, but it is not 0-truncated.  We could 0-truncate it, but to get a universal property relative to all objects rather than only 0-truncated ones, we can instead impose structure making the objects rigid, such as a partial order or a graph.  This argument is formalized in type theory [here](#ConstructingNat); to be precise either it would have to be translated manually into category-theoretic language, or the above conjecture about interpreting type theory in an elementary $(\infty,1)$-topos would have to be proven.

+-- {: .num_theorem}
###### Theorem
There is an [[(n-connected, n-truncated) factorization system]].
=--

The case $n=-1$ can be constructed impredicatively using the subobject classifier: internally, $\Vert A \Vert$ is the smallest [[truth value]] implied by $A$.  Then we can induct on *external* natural numbers, defining $\Vert A \Vert_{n+1}$ to be the $(-1)$-image of the composite $A \to U^A \to (U')^A$, where the second map is the $n$-truncation.  Note that in general it "goes up a universe level", so that the $n$-truncation "goes up $n+2$ universe levels".  However, unlike type theory, an elementary $(\infty,1)$-topos has no globally chosen tower of universes, so this doesn't literally make sense to say.  What we can say is that with this construction, it is not clear whether we can find object classifiers that are *closed* under the $n$-truncation.

However, [(Rijke17)](#Rijke17) shows (again in type theory) that using finite colimits and the natural numbers, the $(-1)$-truncation can be constructed without raising the universe level.  Assuming (as always) that this can be translated into $(\infty,1)$-category theory, it implies that we *can* find object classifiers closed under the $(-1)$-truncation, and hence (by induction) under the $n$-truncation for all $n$.  Moreover, with a natural numbers object this induction can be performed internally, obtaining in particular object classifiers closed under the $n$-truncation for all $n$ at once.

It seems likely that the construction of [[W-types]] in any elementary 1-topos can be repeated in the $(\infty,1)$-case.

There is some structure that the definition probably does not imply, namely a semantic counterpart of arbitrary *recursive* [[higher inductive types]], such as arbitrary [[localization]].  It is certain that these cannot always be constructed in an elementary 1-topos: for instance, HITs imply that all (even infinitary) [[algebraic theories]] have initial algebras, whereas this cannot be proven in [[ZF]] without the [[axiom of choice]] (under appropriate [[large cardinal]] hypotheses).  Thus, it seems very unlikely that they can be constructed in an elementary $(\infty,1)$-topos.  Moreover, it is even unclear exactly what $(\infty,1)$-categorical structure should correspond to arbitrary [[higher inductive types]], not least because we lack an accepted general definition of an "arbitrary HIT".

However, although this is an open question, it is arguably not a question about the definition of "elementary $(\infty,1)$-topos", but some stronger notion, analogous to a stronger notion of 1-topos that lacks an accepted name.  Moreover, a great deal of [[homotopy type theory]] (including synthetic homotopy theory) can be done with only non-recursive HITs, truncations, and a natural numbers type, and even in the absence of a general coherence theorem any particular result of HoTT could probably be explicitly written down in $(\infty,1)$-categorical language.


## Definition (predicative case)

Since there is no consensus even on the definition of [[predicative topos|predicative 1-topos]], it seems less likely that there is a definitive answer for a predicative $(\infty,1)$-topos.  However, it should probably include *at least* the following axioms (which as we have seen above, are all true in the impredicative case although not included in the definition):

* $E$ has finite [[(∞,1)-limit|limits and colimits]]
* $E$ is [[locally cartesian closed (∞,1)-category|locally cartesian closed]]
* For any finite family of morphisms $\{f_i:Y_i\to X_i\}_{i\in I}$, there exists a universe classifying each $f_i$.
* $E$ has a [[natural numbers object]], and perhaps also [[W-types]].

Note that the stronger universe axiom implies, as above, that finite colimits are van Kampen, and in particular therefore that finite coproducts are disjoint.  Instead of strengthening this axiom, we could assume explicitly that finite coproducts are disjoint, and then repeat the proof of descent given above.

## Examples
 {#Examples}

There is presently no known example of an elementary $(\infty,1)$-topos which is not a [[Grothendieck (∞,1)-topos]], though there are some ideas.



## Related pages

* [[elementary topos]]

* [[predicative topos]]

* [[Grothendieck (∞,1)-topos]], [[(∞,1)-pretopos]]

* [[homotopy type theory]]

* [[Awodey's conjecture]]

## References

A vague version of the above proposed definition is on the very last slide of 

* {#Shulman12} [[Mike Shulman]], _Inductive and higher inductive types_ (2012) ([pdf](https://home.sandiego.edu/~shulman/hottminicourse2012/04induction.pdf))

See also

* [[Michael Shulman]], _Towards elementary infinity-toposes_, Vladimir Voevodsky Memorial Conference, IAS, September 2018, [talk](https://www.youtube.com/watch?v=ld4YL787dAk).

* [[Michael Shulman]], [[Peter Lumsdaine]], 2016, _Semantics and syntax of higher inductive types_, ([slides](http://home.sandiego.edu/~shulman/papers/stthits.pdf))

* {#Joyal14} [[André Joyal]], _What is an elementary higher topos?_, talk at _[Reimagining The Foundations Of Algebraic Topology](https://www.msri.org/workshops/689)_ April 07, 2014 - April 11, 2014_ [web video](https://www.msri.org/workshops/689/schedules/18227) [PDF](https://www.msri.org/workshops/689/schedules/18227/documents/2046/assets/20468) (slides 57-end).  This lecture contains a proposed definition that is not an $(\infty,1)$-category but a presentation of one by a [[model category]]-like structure; this is closer to the type theory, but further from the intended examples.  In particular, there are unresolved coherence questions even as to whether every Grothendieck $(\infty,1)$-topos can be presented by a model in Joyal's sense (in particular, how strict can a universe be made, and can the [[natural numbers object]] be made fibrant).  Other than that, the main difference is that Joyal assumes only one fixed universe.

* [[Georg Hegel]], [book 2](Science+of+Logic#LehreVomWesen) of _[[Science of Logic]]_

For an alternative definition proven (in Theorem 3.16) to be equivalent to the one given above, see

* [[Nima Rasekh]], _A Theory of Elementary Higher Toposes_, ([arXiv:1805.03805](https://arxiv.org/abs/1805.03805))


The construction of $n$-truncations without recursive HITs is in

* {#Rijke17} [[Egbert Rijke]], *The join construction*, [arxiv:1701.07538](https://arxiv.org/abs/1701.07538)

The construction of natural numbers from propositional resizing and univalence is in

* {#ConstructingNat} HoTT/Coq library, <https://github.com/HoTT/HoTT/blob/master/theories/PropResizing/Nat.v>

Results holding for elementary (∞,1)-toposes:

* [[Nima Rasekh]], _Yoneda Lemma for Elementary Higher Toposes_, ([arXiv:1809.01736](https://arxiv.org/abs/1809.01736))

* [[Nima Rasekh]], _Every Elementary Higher Topos has a Natural Number Object_, ([arXiv:1809.01734](https://arxiv.org/abs/1809.01734))

* [[Nima Rasekh]], _Truncations and Blakers-Massey in an Elementary Higher Topos_, ([arXiv:1812.10527](https://arxiv.org/abs/1812.10527))

Comprehension schemes are used to characterize categorical properties of elementary ∞-toposes in

* [[Raffael Stenzel]], _(∞,1)-Categorical Comprehension Schemes_, ([arXiv:2010.09663](https://arxiv.org/abs/2010.09663))

A partial analogue of the elementary 1-topos [[FinSet]] is constructed in

* [[Mathieu Anel]], *The elementary infinity-topos of truncated coherent spaces*, [arxiv](https://arxiv.org/abs/2107.02082), 2021
 

[[!redirects elementary (∞,1)-topos]]
[[!redirects elementary (infinity,1)-topos]]
[[!redirects elementary (∞,1)-toposes]]
[[!redirects elementary (infinity,1)-toposes]]
[[!redirects elementary infinity-topos]]
[[!redirects elementary infinity-toposes]]

[[!redirects predicative elementary (∞,1)-topos]]
[[!redirects predicative elementary (infinity,1)-topos]]
[[!redirects predicative elementary (∞,1)-toposes]]
[[!redirects predicative elementary (infinity,1)-toposes]]
[[!redirects predicative elementary infinity-topos]]
[[!redirects predicative elementary infinity-toposes]]
