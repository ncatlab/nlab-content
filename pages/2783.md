
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Regular and exact completions
* table of contents
{: toc}

## Idea

The [[forgetful functor|forgetful]] [[2-functors]] 

* from [[regular categories]] to [[lex categories]],
* from [[exact categories]] to [[lex categories]], and
* from [[exact categories]] to [[regular categories]]

have [[left adjoints]], and in fact are [[monadic adjunction|(2-)monadic]].  Their left adjoints are called ([[free construction|free]]) regular or exact completions.

In the third case the [[2-monad]] is [[idempotent monad|idempotent]], so the left adjoint can properly be called a [[completion]], while in the first two cases, the 2-monad is only [[lax-idempotent monad|lax-idempotent]], so the left adjoint should technically be called a [[free completion]].  However, the phrases *regular completion* and *exact completion* are also commonly used for the first two cases.  To disambiguate the second and third cases the phrases *ex/lex completion* and *ex/reg completion* are also used, and so by analogy the first case is called *reg/lex completion*.

In fact, the reg/lex and ex/lex completion can be applied to a category that merely has [[weak finite limits]], although in this case they are not left adjoint to the obvious forgetful functor.  A general context which includes *all* of these types of these completions is the 2-category of [[unary sites]], in which the categories of regular and exact categories form reflective sub-2-categories.
 

## Constructions

### The ex/lex completion
 {#TheExLexCompletion}

There are several constructions of the ex/lex completion.  Perhaps the quickest one to state (Hu-Tholen 1996) is that if $C$ is [[small category|small]], then $C_{ex/lex}$ is the full subcategory of its [[presheaf category]] $Set^{C^{op}}$ spanned by those presheaves $F$ such that

* $F$ admits a [[regular epimorphism]] $y(X)\twoheadrightarrow F$ from a [[representable presheaf]], 
* with the additional property that if $K\rightrightarrows y(X)$ is the [[kernel pair]] of $y(X)\twoheadrightarrow F$, then $K$ also admits a regular epi $y(Z)\to K$ from a representable presheaf.

A more explicit construction is as follows.  Let us think, informally, of the objects of $C$ as [[presets]] and the morphisms of $C$ as "proofs".  An object of $C_{ex} = C_{ex/lex}$ will then be a "set" or [[setoid]] constructed from $C$.  Precisely, we take the objects of $C_{ex}$ to be the **pseudo-equivalence relations** in $C$: a pseudo-equivalence relation consists of:

* an object $X\in C$ and
* a parallel pair $s,t\colon R\rightrightarrows X$, such that
* there exists an arrow $i\colon X\to R$ with $s i = t i = 1_X$,
* there exists an arrow $v\colon R\to R$ with $s v = t$ and $t v = s$, and
* there exists an arrow $c\colon R\times_X R \to R$ with $s c = s \pi_1$ and $t c = t \pi_2$.  (If $C$ has merely weak finite limits, we assert this for some, and hence every, weak pullback $R\times^w_X R$.)

If $(s,t)\colon R\to X\times X$ is a [[monomorphism]], then these conditions make it precisely a [[congruence]] or internal [[equivalence relation]] in $C$.  In general, we can think of the fiber of $R$ over $(x_1,x_2)$ as giving a collection of "reasons" or "proofs" that $x_1 \mathrel{R} x_2$.  Then $i$ supplies a uniform proof that $x \mathrel{R} x$ for every $x$, while $v$ supplies a uniform proof that $x \mathrel{R} y$ implies $y \mathrel{R} x$, and $c$ supplies a uniform proof that $x \mathrel{R} y$ and $y \mathrel{R} z$ imply $x \mathrel{R} z$.

If $R\rightrightarrows X$ and $S\rightrightarrows Y$ are two pseudo-equivalence relations, a morphism between them in $C_{ex}$ is defined to be a morphism $f\colon X\to Y$ in $C$, such that there exists a morphism $f_1\colon R\to S$ with $s f_1 = f s$ and $t f_1 = f t$.  That is, $f_1$ supplies a uniform proof that if $x \mathrel{R} y$ then $f(x) \mathrel{S} f(y)$.  Moreover, we declare two such morphisms $f,g\colon X\to Y$ to be *equal* if there exists a morphism $h\colon X\to S$ such that $s h = f$ and $t h = g$ (that is, a uniform proof that $f(x) \mathrel{S} g(x)$).  Because $S\rightrightarrows Y$ is a pseudo-equivalence relation, this defines an actual equivalence relation on the morphisms $f\colon X\to Y$, which is compatible with composition; thus we have a well-defined category $C_{ex}$.

We have a [[full and faithful functor]] $C\to C_{ex}$ sending an object $X$ to the pseudo-equivalence relation $X\rightrightarrows X$.  One can then verify directly that $C_{ex}$ is exact, that this embedding preserves finite limits, and that it is universal with respect to lex functors from $C$ into exact categories.

There are also other constructions.  Of course, the ex/lex completion can also be obtained by composing (any construction of) the reg/lex completion with (any construction of) the ex/reg completion.


### The reg/lex completion

The reg/lex completion $C_{reg}= C_{reg/lex}$ of a lex category $C$ is perhaps most succinctly described as the subcategory of $C_{ex}$ consisting of those objects which admit monomorphisms into objects of $C$.  That is, instead of adding *all* quotients of pseudo-equivalence relations in $C$, we only add those quotients which are necessary in order to be able to construct [[images]] of morphisms in $C$.  For many construction of $C_{ex}$, this idea can then be made more explicit and sometimes simplified.

For instance, if we regard $C_{ex}$ as a full subcategory of $Set^{C^{op}}$ as above, then we can likewise regard $C_{reg}$ as the full subcategory of $Set^{C^{op}}$ determined by those presheaves $F$ such that

* $F$ admits a regular epimorphism $y(X) \twoheadrightarrow F$ from a representable presheaf, and
* $F$ admits a monomorphism $F\rightarrowtail y(Z)$ into a representable presheaf.

If we construct $C_{ex}$ using pseudo-equivalence relations, as above, then we can characterize the pseudo-equivalence relations which we need to form $C_{reg}$ as precisely the [[kernel pairs]] of morphisms of $C$ (or finite families of such).  Therefore, we obtain an equivalent definition of $C_{reg}$ as follows.  Its objects are morphisms of $C$ (regarded as stand-ins for their formally added images).  A morphism from $p\colon X\to Y$ to $q\colon Z\to W$ should be a morphism $f\colon X\to Z$ for which there exists an $f_1$ relating the kernel of $p$ to the kernel of $q$, modulo an equivalence relation generated by maps from $X$ to the kernel of $q$.  But by definition of kernel pairs, two morphisms will be identified under this latter equivalence relation if and only if they have the same composite with $q$, so it makes sense to define the morphisms of $C_{reg}$ from $p\colon X\to Y$ to $q\colon Z\to W$ to be certain morphisms $\overline{f}\colon X\to W$ which factor through $q$ (non-uniquely).  We still have to impose the condition that $f$ should preserve the kernel pairs, but in terms of $\overline{f}$ this is simply the statement that $\overline{f} r = \overline{f} s$, where 
$(r,s)$ is the kernel pair of $p$.  This is the definition of $C_{reg}$ given in the [[Elephant]].

We can then verify that $C_{reg}$ is regular, that we have a full and faithful functor $C\to C_{reg}$, which preserves finite limits, and is universal among lex functors from $C$ to regular categories.  Again, there are also other constructions.

Also, just as for the free exact completion, the construction works essentially the same if $C$ has only weak finite limits.  In this case, instead of the objects of $C_{ex}$ admitting a monomorphism to a single object of $C$, we have to consider those admitting a jointly-monic finite family of morphisms into objects of $C$, with similar modifications for the other descriptions.


### The ex/reg completion

If $C$ is regular, a quick definition of $C_{ex/reg}$ is as the full subcategory of the category $Sh(C)$ of [[sheaves]] for the [[regular coverage]] on $C$ spanned by those sheaves which are quotients of [[congruences]] in $C$.  (Lack 1999)

A more explicit description can be obtained by first passing from $C$ to its [[allegory]] of internal relations, then [[split idempotent|splitting]] the idempotents which are equivalence relations in $C$, and finally reconstructing a regular category from the resulting allegory.  Yet more explicitly, this means that the objects of $C_{ex/reg}$ are congruences in $C$, and the morphisms are relations which are [[entire relation|entire]] and [[functional relation|functional]] relative to the given congruences.


### The higher categorical approach

A somewhat more unified approach to all these completions can be obtained as follows.  Observe that in the classical situation (that is, in the presence of choice), *sets* can be identified with all of the following:

* 0-trivial [[groupoids]], i.e. groupoids in which any two parallel morphisms are equal, i.e. [[equivalence relations]].
* 0-trivial [[2-groupoids]], i.e. 2-groupoids in which any two parallel 2-morphisms are equal and any two parallel 1-morphisms are isomorphic.
* and so on...
* 0-trivial [[n-groupoids]] for any $0\le n \le \infty$.

In the absence of choice, this is still true as long as the morphisms between 0-trivial n-groupoids are $n$-[[anafunctors]].  If instead we consider only actual functors, however, in the absence of choice what we obtain are various completions of $Set$.  Specifically:

* $Set_{reg/lex}$ can be identified with the category whose objects are 0-trivial groupoids, and whose morphisms are natural isomorphism classes of functors.
* $Set_{ex/lex}$ can be identified with the category whose objects are 0-trivial 2-groupoids, and whose morphisms are pseudonatural equivalence classes of 2-functors.  In the notion of 2-groupoid here we also demand that each 1-cell be equipped with a *specified* inverse [[equivalence]].

This idea can be generalized to provide alternate constructions of the completions for an arbitrary $C$ with finite limits.  The notions of [[internal category|internal]] $n$-category and internal $n$-functor in such a $C$ make perfect sense for any $n$.  The same is true of the notion of $n$-groupoid, as long as we interpret this to mean the *structure* of "inverse-assigning" morphisms in $C$.  The statement "any two parallel $n$-cells are equal" also makes sense in any lex category, since it demands that a certain specified morphism is monic.  Finally, we can also interpret "any two parallel $k$-cells are equivalent" algebraically by specifying a particular equivalence between any such pair.  (Note that for $k=(n-1)$, since parallel $n$-cells are equal there is a unique way to do this.)  We thereby obtain a notion of internal 0-trivial $n$-groupoid in any lex category, and we write $0 triv n Gpd(C)$ for the category of such things and internal $n$-natural equivalence classes of functors.  We then have:

* It is fairly clear from the above explicit description that $C_{reg/lex}$ is the full subcategory of $0 triv 1 Gpd(C)$ determined by the [[kernel pairs]] (which are [[congruences]], i.e. internal 0-trivial 1-groupoids).  If, like $Set$, $C$ is already exact, so that every congruence is a kernel pair, then $C_{reg/lex}\simeq 0 triv 1 Gpd(C)$.

* $C_{ex/lex}$ is always equivalent to $0 triv 2 Gpd(C)$.  To see this, note that a pseudo-equivalence relation (together with chosen maps $i$, $c$, and $v$) can be regarded as the 1-skeleton of an internal [[bicategory]] in $C$ with specified inverse equivalences for every 1-cell.  There is then a unique way to add 2-cells to make it a 0-trivial bigroupoid.

It is not clear how 0-trivial $n$-groupoids fit into this picture for $n\gt 2$, although it seems likely that the objects of *iterated* reg/lex and ex/lex completions can be identified with some type of internal [[n-fold category]].

Now if $C$ is already regular, then we can define a notion of internal [[anafunctor]] between internal $n$-categories. It is then easily seen that

* $C_{ex/reg}$ is equivalent to the category of 0-trivial 1-groupoids, and natural isomorphism classes of internal anafunctors between them.

Again, it is not entirely clear how the 0-trivial $n$-groupoids and anafunctors behave for $n\gt 1$, although it seems fairly likely (to [[Mike Shulman|me]]) that in this case the process will stabilize at $n=1$, i.e. 0-trivial $n$-groupoids with equivalence classes of ana-$n$-functors will give $C_{ex/reg}$ for all $n\ge 1$.

### Completions of unary sites

The descriptions of the ex/lex and ex/reg completions in terms of pseudo-equivalence relations and equivalence relations, respectively, have a common generalization.  Let $C$ be a [[unary site]], so that it has a notion of "covering morphism" and admits "finite local unary prelimits".  In particular, any cospan $X\to Z\leftarrow Y$ has a *local unary pre-pullback*, which is a commutative square
$$ \array{ P & \to & Y \\ \downarrow && \downarrow\\ X & \to & Z } $$
such that for any other commutative square
$$ \array{ V & \to & Y \\ \downarrow && \downarrow\\ X & \to & Z } $$
there is a cover $U\to V$ and a map $U\to P$ such that the induced composites $U\to X$ and $U\to Y$ are equal.

Now we can define a **unary congruence** in $C$ to consist of:

* An object $X\in C$

* A parallel pair $s,t:R\rightrightarrows X$, such that

* There exists a cover $p:Y\to X$ and a map $i:Y\to R$ with $s i = t i = p$,

* There exists a cover $q:S\to R$ and a map $v:S\to R$ with $s v = t q$ and $t v = s q$, and

* There exists a local unary pre-pullback $T$ of the cospan $R \xrightarrow{t} X \xleftarrow{s} R$ and an arrow $c:T\to R$ such that $s c = s \pi_1$ and $t c = t \pi_2$, where $\pi_1$ and $\pi_2$ are the projections of $T$ to $R$.

If $C$ has a trivial topology, then local unary prelimits are simply weak limits, and this reduces to the definition of pseudo-equivalence relation.  On the other hand, if $C$ is regular with its regular topology, then these conditions ensure exactly that the [[image]] of $R\to X\times X$ is an internal equivalence relation on $X$.

Now we can define morphisms between unary congruences using a suitable kind of either entire and functional relations or anafunctors, and obtain the exact completion of the unary site $C$.  This construction exhibits the 2-category of exact categories as a reflective sub-2-category of the 2-category of unary sites, and restricts to the ex/wlex and ex/reg completions on the sub-2-categories of categories with weak finite limits and trivial topologies and of regular categories with regular topologies, respectively.  It can also be modified to construct regular completions.  See ([Shulman](#Shulman)) for details.


## Generalizations to higher arity

More generally, any [[∞-ary site]] has a $\kappa$-ary exact completion, which is a [[∞-ary exact category]].  This exhibits the 2-category of $\kappa$-ary exact categories as a reflective sub-2-category of that of $\kappa$-ary sites.  See ([Shulman](#Shulman)) for details.  In particular:

* When $\kappa=\omega$, this is called the [[pretopos completion]], and applies in particular to [[coherent categories]].

* When $\kappa$ is the size of the [[universe]], this applies to any [[small category|small]] [[site]] and constructs its [[topos of sheaves]].


## Properties of regular and exact completions

Many categorical properties of interest are preserved by one or more of the regular and exact completions.  That is, if $C$ has these properties, then so does the completion, and the inclusion functor preserves them.  Note that frequently, for a completion to have some structure, it suffices for $C$ to have a "weak" version of that structure.

* Of course, [[finite limits]] are preserved by all three completions.  In fact, as we have remarked, for the ex/lex and reg/lex completions, $C$ need only have weak finite limits.

* $C$ is [[extensive category|lextensive]] if and only if $C_{ex/lex}$ is, and if and only if $C_{reg/lex}$ is, and in this case the embeddings preserve [[coproducts]] (Menni 2000).  It follows that if $C$ is a [[pretopos]], then so is $C_{ex/lex}$, although the inclusion $C\to C_{ex/lex}$ is not a "pretopos functor" as it does not preserve [[regular epis]].

* If $C$ is lextensive and has [[coequalizers]] (and hence has finite colimits), then so do $C_{ex/lex}$ and $C_{reg/lex}$ (Menni 2000).  However, the inclusion functors do not preserve coequalizers.  In fact, it suffices for $C$ to be lextensive with *quasi-coequalizers*, meaning that for every $f,g\colon Y\rightrightarrows X$ there exists $q\colon X\to Q$ with $q f = q g$, such that for any $h\colon X\to Z$ with $h f = h g$, $h$ coequalizes the [[kernel pair]] of $q$.

* The categories $C_{reg/lex}$ and $C_{ex/lex}$ always have [[projective object|enough (regular) projectives]].  In fact, the objects of $C$ are precisely the projective objects of these categories.  Moreover, an exact category $D$ is of the form $C_{ex/lex}$ for some $C$ (with weak finite limits) if and only if it has enough projectives, in which case of course $C$ can be taken to be the subcategory of projectives (Carboni--Vitale 1998).  Note that if $D$ has enough projectives, then its subcategory of projectives always has weak finite limits.  Similarly, a regular category $D$ is of the form $C_{reg/lex}$ for some $C$ (with weak finite limits) if and only if it has enough projectives and every object can be embedded in a projective one.

* If $C$ is a regular category satisfying the "regular" [[axiom of choice]] (i.e. every regular epi splits), then it is *equivalent* to $C_{reg/lex}$, and hence the latter also satisfies the axiom of choice.  Similarly, if $C$ is exact and satisfies choice, then it is equivalent to $C_{ex/lex}$.  Conversely, if the inclusion $C\to C_{reg/lex}$ or $C\to C_{ex/lex}$ is an equivalence, then since the objects of $C$ are projective in these completions, $C$ must satisfy the axiom of choice.

  In fact, if we assume merely that $C_{ex/lex} \to (C_{ex/lex})_{ex/lex}$ is a equivalence, then since the objects of $C_{ex/lex}$ are projective in $(C_{ex/lex})_{ex/lex}$, they must also all be projective in $C_{ex/lex}$, and therefore $C\to C_{ex/lex}$ is also an equivalence.  It follows by induction that if the sequence of iterations of $(-)_{ex/lex}$ stabilizes at any finite stage, it must in fact stabilize at the very beginning and $C$ must satisfy the axiom of choice.  A similar argument applies to the reg/lex completion.  (The ex/reg completion, of course, always stabilizes after one application.)

* [[cartesian closed category|Cartesian closure]] is preserved by the ex/lex completion (Carboni--Rosolini 2000).  In fact, $C_{ex/lex}$ is cartesian closed if and only if $C$ has *weak simple products*, meaning [[weak dependent product]]s along [[product]] projections.

* [[locally cartesian closed category|Local cartesian closure]] is also preserved by the ex/lex completion (Carboni--Rosolini 2000).  In fact, $C_{ex/lex}$ is locally cartesian closed if and only if $C$ is *weakly locally cartesian closed*, meaning that each [[slice category]] has weak dependent products.  It follows in particular that if $C$ is a [[Π-pretopos]], then so is $C_{ex/lex}$.  For each $\Pi$-pretopos $C$ we thus obtain a sequence $C$, $C_{ex}$, $(C_{ex})_{ex}$, ... of $\Pi$-pretopoi, which in general does not stabilize.

* (Local) cartesian closure is seemingly not always preserved by the reg/lex completion, but it is under certain hypotheses.  Recalling that $C_{reg/lex}$ is the full subcategory of $C_{ex/lex}$ consisting of the kernel pairs, suppose that $C$ has pullback-stable (epi,regular mono) factorizations and that every [[regular monomorphism|regular]] congruence is a kernel pair.  Then $C_{reg/lex}$ is [[reflective subcategory|reflective]] in $C_{ex/lex}$ (BCRS 1998, Menni 2000): the reflection of a pseudo-equivalence relation $R\rightrightarrows X$ is its (epi,regular mono) factorization.  Moreover, the reflection preserves products, and also pullbacks along maps in $C_{reg/lex}$, from which it follows that if $C_{ex/lex}$ is cartesian closed or locally cartesian closed, so is $C_{reg/lex}$.

  Thus, if $C$ is weakly cartesian closed (resp. weakly locally cartesian closed), has pullback-stable (epi,regular mono) factorizations, and every regular congruence is a kernel pair, then $C_{reg/lex}$ is cartesian closed (resp. locally cartesian closed).  In particular, the local versions of these hypotheses apply in particular to [[Top]] and to any [[quasitopos]].  Note that $Top_{reg/lex}$ is called the category of [[equilogical space]]s.

* If $C$ is lextensive with coequalizers (or "quasi-coequalizers") and a [[strong-subobject classifier]], then so is $C_{reg/lex}$ (Menni 2000).  It follows that if $C$ is a lextensive [[quasitopos]], then so is $C_{reg/lex}$.  For each lextensive quasitopos $C$ we thus obtain a sequence $C$, $C_{reg}$, $(C_{reg})_{reg}$, ... of lextensive quasitopoi, which in general does not stabilize.

* If $C$ has a [[natural numbers object]], then so do $C_{reg/lex}$ and $C_{ex/lex}$.  (Does $C_{ex/reg}$?  What about more general [[W-type]]s?)

* If $C$ is a [[ΠW-pretopos]], then so is $C_{ex/lex}$ (see [vandenBerg](#vdB), Theorem 1.1). 

* $C_{ex/lex}$ is an [[elementary topos]] iff $C$ has weak dependent products and a [[generic proof]] ([Menni2000](#Menni)).  Note that if $C$ is a topos satisfying the axiom of choice, then its subobject classifier is a generic proof.  It follows that in this case $C_{ex/lex}$ is a topos---but we already knew that, because $C_{ex/lex}$ is equivalent to $C$ for such a $C$.

* Expanding on the last point, for a [[presheaf topos]] $C = Set^{D^{op}}$, the category $C_{ex/lex}$ is a topos iff $D$ is a [[groupoid]] ([Menni2000](#Menni)). 

* If $C$ is regular, locally cartesian closed, and has a *generic mono*, i.e. a monomorphism $\tau\colon \Upsilon\to \Lambda$ such that every monomorphism is a pullback of $\tau$ (not necessarily uniquely), then $C_{ex/reg}$ is a topos ([Menni2000](#Menni)).

* If $C$ is an [[additive category]], then $C_{ex/lex}$ is an [[abelian category]].

On the other hand, some properties are *not* preserved by the completions.

* Of course, all the completions are regular categories, but the inclusions are not [[regular functor]]s, since they do not preserve regular epis.

* We have seen that the existence of a [[subobject classifier]] or [[power objects]] is not, in general, preserved by the completions (although if $C$ is a topos, then of course so is $C_{ex/reg}$, since it is equivalent to $C$).

* Similarly, if $C$ is [[well-powered category|well-powered]], it does not follow that $C_{reg/lex}$ or $C_{ex/lex}$ are.  In particular, for $X\in C$, the subobject preorders $Sub_{C_{reg/lex}}(X)$ and $Sub_{C_{ex/lex}}(X)$ are equivalent to the preorder reflection of the slice category $C/X$, and it is easy to construct examples in which this is not essentially small[^fine].

* If $C$ is a [[coherent category]], it does not follow that $C_{ex/lex}$ or $C_{reg/lex}$ is.  However, if $C$ is additionally [[extensive category|lextensive]], we have seen above that so are these completions, and hence in particular also coherent (any extensive regular category is coherent).  One can also write down the "free coherent completion" and the "free pretopos completion" of a lex category, and the "pretopos completion" of a coherent category; see [[familial regularity and exactness]] for some clues on how to proceed.

* If $C$ is a [[Heyting category]], it does not follow that $C_{ex/lex}$ or $C_{reg/lex}$ is.  However, if $C$ is additionally lextensive and locally cartesian closed, we have seen above that so are these completions, and hence Heyting (any lextensive locally cartesian closed regular category is Heyting).

* Unsurprisingly, if $C$ is a [[Boolean category]], it does not follow that $C_{ex/lex}$ or $C_{reg/lex}$ is, even if $C$ is lextensive and LCC so that its completions are Heyting.

  In fact, a stronger statement is true: if $C$ is lextensive and regular, then $C_{reg/lex}$ and $C_{ex/lex}$ are Boolean if and only if $C$ *satisfies the axiom of choice* (in which case they are of course equivalent to $C$).  More precisely, if $X\in C$ is such that every subobject of $X$ in $C_{reg/lex}$ is complemented, then $X$ is projective in $C$.  (The same argument applies to $C_{ex/lex}$.)  For suppose that $p\colon Y\to X$ is a regular epi in $C$.  Recall that $Sub_{C_{reg/lex}}(X)$ is the preorder reflection of $C/X$.  Thus $p$, considered as an object of $C/X$, defines a monomorphism in $C_{reg/lex}$.  By assumption, this monic is complemented; let its complement be represented by $q\colon Z\to X$.  Since complements are disjoint, and meets in $Sub_{C_{reg/lex}}(X)$ are given by pullbacks in $C/X$, the pullback of $p$ and $q$ admits a morphism to the initial object $0$, and hence is itself initial since $C$ is extensive.  Now $p$ is regular epi, hence so is its pullback $0\to Z$.  But in a lextensive regular category, disjointness of the coproduct $1+1$ implies that $0\to 1$ is the equalizer of of the coprojections $1\rightrightarrows 1+1$, and therefore any epimorphism with domain $0$ is an isomorphism; thus $Z$ is also initial.  Now since joins in $Sub_{C_{reg/lex}}(X)$ are given by coproducts in $C/X$, the induced map $Y+Z \to X$ must become an isomorphism in $Sub_{C_{reg/lex}}(X)$, which means that it must admit a section; but since $Z$ is initial this means that $p$ itself has a section.

* If $C$ is [[well-pointed topos|well-pointed]], it does not follow that $C_{ex/lex}$ or $C_{reg/lex}$ are (in the stronger sense appropriate for non-toposes).  It is of course always true that $1$ is projective in the completions.  And if $C$ is lextensive, so that its completions are coherent, then $1$ is indecomposable in them as soon as it is so in $C$.  However, it does not follow that $1$ is a *strong* generator in the completions even if it is so in $C$, since the completions have (in general) many more monomorphisms than $C$ does.

  If $C$ is a well-pointed topos such that $C_{ex/lex}$ is also a topos, then the latter cannot be well-pointed unless $C$ satisfies AC, because the completion would then be Boolean, and hence AC holds by the proof above.

## Examples

(to be written...)

* The category [[Set]] of [[Bishop set|Bishop sets]] is the ex/lex completion of the category of [[preset|presets]]. 

* [[Realizability toposes]] arise as ex/lex completions of categories of partitioned assemblies based on a [[partial combinatory algebra]] $A$. In fact the reg/lex completion gives, as an interesting intermediate step, the category of assemblies based on $A$ (which turns out to be the [[quasitopos]] of $\neg\neg$-separated objects inside the realizability topos). This is discussed in [Menni](#Menni). 

* The category $TF$ of [[torsion|torsion-free]] [[abelian groups]] is regular, but not exact.  For instance, the [[congruence]] $\{ (a,b) | a \equiv b \mod 2 \} \subseteq \mathbb{Z}\times\mathbb{Z}$ is not a kernel in $TF$.  Unsurprisingly, the ex/reg completion of $TF$ is equivalent to the category $Ab$ of all abelian groups.

  Note that although $TF$ is not exact, its inclusion into $Ab$ does have a left adjoint (quotient by torsion), and thus $TF$ is cocomplete.  Herein lies a subtle trap for the unwary: since the ex/reg completion monad is idempotent, it is in particular lax-idempotent, which means that any left adjoint to the unit $C \hookrightarrow C_{ex/reg}$ is in fact a (pseudo) algebra structure; but since the monad is actually idempotent, any algebra structure is an equivalence.  Of course, the reflection $Ab \to TF$ is *not* an equivalence, which doesn't contract the general facts because this left adjoint is not a regular functor, and hence not an adjunction in the 2-category on which the monad $(-)_{ex/reg}$ lives.  In fact, it is not hard to check that $C \hookrightarrow C_{ex/reg}$ has a left adjoint in $Cat$ if and only if $C$ has [[coequalizers]] of [[congruences]] (while if it has a left adjoint in $Reg$ then it must be an equivalence).

* A [[free cocompletion]] of a (possibly large) finitely complete category, i.e., the category of [[small presheaves]] on $C$, is the ex/lex completion of the [[free cartesian category|free coproduct completion]] of $C$. This appears as Lemma 3 [here](#JR). 


## References

* Carboni and Celia Magno, "The free exact category on a left exact one", J. Austral. Math. Soc. (Ser. A), 1982. 

* {#JR} Ji&#345;&#237; Rosick&#253;, _Cartesian closed exact completions_, JPAA 142 no. 3 (October 1999), 261-270. ([doi](https://doi.org/10.1016/S0022-4049(98)00146-7)) 

* Hu and Tholen, "A note on free regular and exact completions and their infinitary generalizations", [TAC](http://www.tac.mta.ca/tac/volumes/1996/n10/2-10abs.html) 1996.

* Carboni and Vitale, "Regular and exact completions", JPAA 1998.

* Birkedal and Carboni and Rosolini and Scott, "Type Theory via Exact Categories," 1998

* Stephen Lack, "A note on the exact completion of a regular
 category, and its infinitary generalizations" [TAC](http://www.tac.mta.ca/tac/volumes/1999/n3/5-03abs.html) 1999.

* The [[Elephant]], Sections A1.3 and A3.

* Carboni and Rosolini, "Locally cartesian closed exact completions", JPAA 2000

* Mat&#237;as Menni, "Exact completions and toposes," Ph.D. Thesis, University of Edinburgh, 2000. ([web](http://www.lfcs.inf.ed.ac.uk/reports/00/ECS-LFCS-00-424/))
{#Menni} 

* [[Michael Shulman]], "Exact completions and small sheaves".  *Theory and Applications of Categories*, Vol. 27, 2012, No. 7, pp 97-173.  [Free online](http://www.tac.mta.ca/tac/volumes/27/7/27-07abs.html)
{#Shulman} 

* [[Benno van den Berg]], _Inductive types and exact completion_, Ann. Pure Appl. Logic, 134 (2005), 95&#8211;121. ([online .pdf file](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.18.5456&rep=rep1&type=pdf)) 
 {#vdB} 


[^fine]: For example, let $C = Set^{\bullet \rightrightarrows \bullet}$ be the topos of [[quiver|directed graphs]]. For each ordinal $\alpha$, let $G_\alpha$ be the directed graph whose nodes are elements of $\alpha$ and with a directed edge from $\beta$ to $\gamma$ if $\beta \lt \gamma$ in $\alpha$. Then in the poset reflection $Pos(C)$, we have a class of proper monomorphisms, e.g., $[G_\alpha] \lt [G_{\alpha'}]$ whenever $\alpha \lt \alpha'$. Thus $Pos(C)$ is a large poset. This example also shows that $Pos(C)$ need not be a [[total category]] even if $C$ is. 



[[!redirects regular or exact completion]]
[[!redirects regular and exact completion]]
[[!redirects exact completion]]
[[!redirects lex completion]]
[[!redirects free exact completion]]
[[!redirects ex/lex completion]]
[[!redirects ex/reg completion]]
[[!redirects reg/lex completion]]
[[!redirects regular or exact completions]]
[[!redirects regular and exact completions]]
[[!redirects exact completions]]
[[!redirects lex completions]]
[[!redirects ex/lex completions]]
[[!redirects ex/reg completions]]
[[!redirects reg/lex completions]]

[[!redirects pseudo-equivalence relation]]
[[!redirects pseudo-equivalence relations]]
