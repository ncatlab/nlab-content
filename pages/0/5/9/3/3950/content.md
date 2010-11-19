<div class="rightHandSide toc">
[[!include 2-category theory - contents]]
</div>

# Contents
* automatic table of contents
{: toc}

## Idea

A [[2-category]] is a good context for doing a lot of category theory (including [[internal category]] theory, [[enriched category]] theory, and so on), but there are some things that are hard to do there, such as to talk about [[weighted limits]] and colimits.  This leads one to introduce the notion of a [[2-category equipped with proarrows]], which is a 2-category along with extra data that plays the role of [[profunctors]], allowing the definition of weighted limits and other aspects of category theory.

However, it would also be nice if the extra data in a proarrow equipment were somehow determined by the 2-category we started with.  This is especially so when talking about functors between equipments, since functors between 2-categories are often easier to construct.  It turns out that in many cases, including the most common ones, this is the case: we can construct the proarrows in terms of the underlying 2-category.  This was originally realized by Ross Street.

The idea is to identify a profunctor with its [[collage]], aka its [[cograph of a profunctor|cograph]], which is a special sort of [[cospan]] in $Cat$ (or $V Cat$, or whatever other 2-category one wants to start with).  One then simply has to characterize, in 2-categorical terms, which cospans are collages, and how to do things like compose them.  It turns out that in most cases the characterization is precisely that they are the **two-sided codiscrete cofibrations** --- i.e. the [[two-sided fibration|two-sided discrete fibrations]] in the [[opposite 2-category]].


## Definition

Suppose that $K$ is a 2-category with finite [[2-colimits]], and $A,C\in K$.  A **cofibration** from $A$ to $C$ is a [[cospan]] $A\to B \leftarrow C$ which is an [[two-sided fibration|internal two-sided fibration]] in $K^{op}$.  As remarked at [[fibration in a 2-category]], there is a [[2-monad]] on $Span_{K^{op}}(A,C)$ whose algebras are such fibrations.  In other words, there is a *2-comonad* on $Cospan_K(A,C)$ whose *coalgebras* are such fibrations.  This 2-comonad is defined by 
$$ (A\to B \leftarrow C) \quad \mapsto\quad (A \to (A\times I) +_A B +_C (C\times I) \leftarrow C) $$
where $I$ is the [[interval category]] $(0\to 1)$ and $(-\times I)$ denotes the [[copower]] with $I$.  In the pushouts, the map $A\to A\times I$ is the inclusion at $0$ and $C\to C\times I$ is the inclusion at $1$.

A cospan $A\to B \leftarrow C$ in a 2-category $K$ is **codiscrete** if it is codiscrete in the 2-category $Cospan_K(A,C)\simeq (A+C)/K$.  This means that for any $X\in Cospan(A,C)$, the hom-category $Cospan(A,C)(B,X)$ is equivalent to a [[discrete category]].  Explicitly, it means that given any two morphisms $B \;\rightrightarrows\; X$ of cospans, if there exists a 2-cell from one to the other in $Cospan(A,C)$, then it is unique and invertible.

A **codiscrete cofibration** is a two-sided cofibration which is codiscrete as a cospan.


## Examples

### Enriched categories

We sketch a characterization of cofibrations in $V Cat$, where $V$ is any B&#233;nabou [[cosmos]].  Let $A\overset{f}{\to} B \overset{g}{\leftarrow} C$ be a cospan and let $D = (A\times I) +_A B +_C (C\times I)$.  We claim that $D$ has the following description.

* Its objects are the disjoint union of those of $A$, $B$, and $C$, i.e. $ob(D) = ob(A) \sqcup ob(B) \sqcup ob(C)$.

* $A$ and $B$ and $C$ are (disjoint) full subcategories of $D$.

* There are no morphisms in $D$ from $A$ to $B$, or from $B$ to $C$, or from $A$ to $C$.  That is, for $a\in A$, $b\in B$, and $c\in C$ we have $D(a,b) = D(b,c) = D(a,c) = \emptyset$.

* If $a\in A$, $b\in B$, and $c\in C$, we have $D(b,a) = B(b,f a)$, $D(c,b) = B(g c, b)$, and $D(c,a) = B(g c, f a)$.

That $D$ is a $V$-category is immediate, and it is easy to check the universal property.  We write $A \overset{i}{\to} D \overset{j}{\leftarrow} C$ for the inclusions.

Now suppose that $B$ is a coalgebra for the 2-comonad in question.  Therefore, in particular we have a map $h\colon B\to D$ in $Cospan(A,C)$, so that $h f = i$ and $h g = j$ (or perhaps only isomorphic; it really makes no difference here).  Moreover, the counit of the comonad is the obvious map $k\colon D\to B$, so we must have $k h = 1_B$.

Since $i$ and $j$ are injective on objects and have disjoint images, so must be $f$ and $g$.  And since $i$ and $j$ are fully faithful $V$-functors, the action of $f$ and $g$ on homs must be split monic in $V$, and the action of $h$ on homs in $A$ and $B$ must be split epic.  But since $h k = 1_B$, the action of $h$ on homs must also be split monic, hence an isomorphism, and hence so must that of $f$ and $g$ be.  Therefore, $f$ and $g$ are fully faithful inclusions with disjoint images.

Clearly $h$ must take the images of $f$ and $g$ to the images of $i$ and $j$, respectively.  Because $k h = 1_B$, it must be that $h$ takes the rest of $B$ to itself, sitting in the canonical copy of $B$ inside $D$.  This uniquely defines $h$, as long as $B$ satisfies the condition that

* For $a\in A$, $c\in C$, and $b\in B \setminus (A\cup C)$, we have $B(a,b) = B(b,c) = B(a,c) = \emptyset$.

It is then easy to check that if $f$ and $g$ are fully faithful with disjoint images and this condition holds, then $B$ is in fact a coalgebra for the comonad in question, i.e. a two-sided cofibration from $A$ to $C$.

Note that such a cofibration from $A$ to $C$ can be identified with the following data: a category $B' = B\setminus (A\cup C)$, profunctors $m\colon A &#x21F8; B$, $n\colon B &#x21F8; C$, and $p\colon A &#x21F8; C$, and a morphism $n m \to p$ of profunctors.  Such a thing is sometimes called a **gamut** from $A$ to $C$.

Now a 2-cell in $Cospan(A,C)$ is simply a natural transformation between functors $B \;\rightrightarrows\; X$ whose components on the images of $A$ and $C$ are isomorphisms.  Thus, if $B$ is a cofibration as above with the property that $B \setminus (A\cup C)$ is empty, then it must be codiscrete.  The converse is easy to check, taking $X$ to be the ordinal $4 = (0\le 1 \le 2\le 3)$ as a category.  But a gamut with $B'=\emptyset$ is nothing but a profunctor $A &#x21F8;C$; hence codiscrete cofibrations in $V Cat$ can be precisely identified with the collages of profunctors.

### Toposes

A codiscrete cofibration in the 2-category $Topoi$ of [[topoi]] can be identified with a [[left exact functor]].

### Double categories

Codiscrete cofibrations in the 2-category $Dbl$ of [[double categories]], [[double functors]], and [[horizontal transformations]] can be identified with [[double profunctors]].


## Construction of a proarrow equipment

The examples of profunctors suggest that given any 2-category $K$ with finite 2-colimits, we may try to canonically equip it with proarrows by defining the proarrows $A &#x21F8;C$ to be the codiscrete cofibrations.  The sticky point is then how to define units and composition of such proarrows in order to obtain an equipment.

The unit is obvious: we should take the unit proarrow of $A$ to be the cospan $A\to A\times I \leftarrow A$, which is always a codiscrete cofibration.

Binary composition is subtler.  The obvious way to compose codiscrete cofibrations $A \to B \leftarrow C$ and $C\to D \leftarrow E$, of course, is to take a [[pushout]] $B +_C D$.  It is not hard to show (see references):

+-- {: .un_theorem}
###### Theorem
In any 2-category with finite 2-colimits, if $B$ and $D$ are cofibrations, then so is $B +_C D$.
=--

However, $B +_C D$ will not be codiscrete even if $B$ and $D$ are.  In $V Cat$, if $B$ and $D$ are collages of profunctors $m$ and $n$, then $B +_C D$ represents the gamut consisting of $m$, $n$, and the composite profunctor $n m$, with the middle category being $C$.  Thus, in order to obtain the correct composite, we need to forget about $C$ somehow.  The best way to do this seems to be using a [[factorization system in a 2-category]], akin the way in which we construct the [[bicategory of relations]] from any [[regular category]].


### Equippable 2-categories

We are looking for a [[factorization system in a 2-category|2-categorical factorization system]] $(\mathcal{E},\mathcal{M})$ in $K$ such that if we have a two-sided cofibration $A\to C\leftarrow B$ and we factor $A+B \to C$ into an $\mathcal{E}$-map and an $\mathcal{M}$-map, then the resulting cospan $A\to E \leftarrow B$ is a codiscrete cofibration.  Codiscreteness means in particular that the $\mathcal{E}$-map $A+B\to E$ should be codiscrete, i.e. representably cofaithful and co-conservative.  Moreover, if $A\to C\leftarrow B$ was already a codiscrete cofibration, then $A+B\to C$ should already be in $\mathcal{E}$.  This suggests the following definition.

+-- {: .un_defn}
###### Definition
A 2-category with finite 2-limits and 2-colimits is **pre-equippable** if it has a factorization system $(\mathcal{E},\mathcal{M})$ such that

* if $A\to C \leftarrow B$ is a codiscrete cofibration, then $A+B \to C$ is in $\mathcal{E}$, and
* every morphism in $\mathcal{E}$ is representably co-faithful and co-conservative.

It is **equippable** if in addition it satisfies:

* Morphisms in $\mathcal{M}$ are closed under pushout and tensors with $I$.
=--

Co-conservative morphisms are also called **liberal**.  Recall that by definition of codiscreteness, if $A\to C \leftarrow B$ is a codiscrete cofibration, then $A+B\to C$ is cofaithful and liberal; thus the first two conditions are compatible.

The example to keep in mind is $V Cat$, for any suitable $V$, where $\mathcal{E}$ is the class of essentially surjective $V$-functors and $\mathcal{M}$ is the class of $V$-fully-faithful functors.

+-- {: .un_prop}
###### Proposition
Any morphism which is right orthogonal to codiscrete cofibrations is [[fully faithful morphism|representably fully faithful]].  In particular, if $K$ is pre-equippable, then every morphism in $\mathcal{M}$ is representably fully faithful.
=--
+-- {: .proof}
###### Proof
For any $X$ in $K$, we have a codiscrete cofibration $X\to X \times I \leftarrow X$, and thus $X+X \to X\times I$ is in $\mathcal{E}$.  But orthogonality with respect to all such morphisms is precisely representable fully-faithfulness.
=--

+-- {: .un_prop}
###### Proposition
Any representably fully faithful morphism is right orthogonal to any [[cocomma object]].  In particular, $K$ is pre-equippable and every codiscrete cofibration is a cocomma object, then $\mathcal{M}$ is precisely the class of representably fully faithful morphisms.
=--
+-- {: .proof}
###### Proof
Maps out of a cocomma object are in canonical correspondence with 2-cells in $K$.  But representable fully-faithfulness means that 2-cells lift uniquely along such a map.  Hence so do maps out of a cocomma object, and hence any representably fully faithful map is right orthogonal to all cocomma cospans.
=--

+-- {: .un_prop}
###### Proposition
If $K$ is pre-equippable, then any [[inverter]] or [[equifier]] is in $\mathcal{M}$, and every morphism in $\mathcal{E}$ is cofaithful and liberal.
=--
+-- {: .proof}
###### Proof
Any inverter is always right orthogonal to any liberal morphism, and any equifier is always right orthogonal to any cofaithful morphism.
=--


### The construction

In an equippable 2-category, we can compose cofibrations in the desired way.

+-- {: .un_prop}
###### Proposition
If $K$ is equippable, $A\to E \leftarrow B$ is a two-sided cofibration, and $A+B \to F \to E$ is an $(\mathcal{E},\mathcal{M})$-factorization, then $A\to F \leftarrow B$ is a codiscrete cofibration.  In particular, the category $CodCofib(A,B)$ is coreflective in the 2-category $Cofib(A,B)$.
=--
+-- {: .proof}
###### Proof
Since $\mathcal{E}$-morphisms are cofaithful and liberal, $A\to F \leftarrow B$ is certainly codiscrete.  That it is a cofibration is proven as in (MB, 4.18).  Coreflectivity follows by orthogonality for the factorization system $(\mathcal{E},\mathcal{M})$, since all codiscrete cofibrations are in $\mathcal{E}$ by assumption.
=--

Therefore, in an equippable 2-category, we can define the composite of codiscrete cofibrations $A\to B\leftarrow C$ and $C\to D\leftarrow E$ to be the codiscrete coreflection of the cofibration $A \to B +_C D\leftarrow E$.

+-- {: .un_prop}
###### Proposition
If $K$ is equippable, there is a 2-category $CodCofib(K)$, with the same objects as $K$, and with codiscrete cofibrations as 1-morphisms.  Moreover, there is a locally fully faithful identity-on-objects (pseudo) 2-functor $(-)_* K\to CodCofib(K)$ such that each 1-morphism $f_*$ has a right adjoint.  Therefore, $K$ is canonically a [[2-category equipped with proarrows]] (hence the term "equippable").
=--
+-- {: .proof}
###### Proof
This is essentially (MB, 4.20).
=--

One can then impose additional axioms on $K$ to get good behavior of this equipment, and try to characterize the equipments arising in this way; see (MB, section 5) and (PC).


### Canonical factorization systems

Note that since coreflections are determined by a universal property, the composite of codiscrete cofibrations is independent of the chosen factorization system $(\mathcal{E},\mathcal{M})$.  In fact, there are two different "extreme" ways that we might try to define an equippable factorization system; we could either

1. Define $\mathcal{E}$ to be the class of liberal and cofaithful morphisms, or
1. Define $\mathcal{E}$ to be generated by the class of codiscrete cofibrations.

In the second case we mean that $\mathcal{M}$ is the class of all morphisms right orthogonal to the morphisms $A+B\to C$ such that $A\to C \leftarrow B$ is a codiscrete cofibration, and then $\mathcal{E}$ is the class of all morphisms left orthogonal to $\mathcal{M}$.  This implies, of course, that $\mathcal{E}$ contains the codiscrete cofibrations.

Neither of the above choices is guaranteed to produce a factorization system (since the factorizations may not exist), but if either one does, then that factorization system is automatically pre-equippable.  In the first case this is obvious, since all codiscrete cofibrations are cofaithful and liberal, while in the second case, it follows since inverters and equifiers are then necessarily in $\mathcal{M}$, and anything left orthogonal to inverters and equifiers must be cofaithful and liberal.  Thus, a 2-category is equippable if either of these two choices produces a factorization system for which $\mathcal{M}$ is closed under pullback and tensors with $I$.

+-- {: .un_prop}
###### Proposition
The (essentially surjective, $V$-fully faithful) factorization system is generated by the codiscrete cofibrations, and is equippable.
=--
+-- {: .proof}
###### Proof
It suffices to show that a $V$-functor $f\colon A\to B$ is right orthogonal to codiscrete cofibrations if and only if it is $V$-fully faithful, i.e. each morphism $A(a,a') \to B(f a, f a')$ is an isomorphism in $V$.  For "if", it suffices to observe that $V$-fully faithful functors are right orthogonal to all essentially surjective ones, and any codiscrete cofibration is essentially surjective.  For "only if," suppose given $a,a'\in A$, let $X=Y=I$ be the unit $V$-category, consider the object $B(f a,f a')\in V$ as a $V$-profunctor $X \to Y$, and let $E$ be its [[collage]].  Then we have a square
$$\array{X\sqcup Y & \overset{[a,a']}{\to} & A\\
  \downarrow && \downarrow\\
  E & \underset{[f a, f a']}{\to} & B}$$
where the bottom arrow is the identity on the nontrivial hom-object $B(f a,f a')$.  A lifting in this square supplies a [[section]] of $A(a,a') \to B(f a, f a')$, and uniqueness of lifting against the collage of $A(a,a')$ (also as a profunctor $I\to I$) shows that it is an inverse isomorphism; hence $f$ is $V$-fully faithful.

Finally, it is straightforward to verify that $V$-fully-faithful functors are closed under pushout and tensors with $I$.
=--

+-- {: .un_prop}
###### Proposition
In $V Cat$, every liberal is automatically cofaithful, and there is a pre-equippable factorization system in which $\mathcal{E}$ is the class of liberal morphisms.  However, it is not equippable, even when $V=Set$.
=--
+-- {: .proof}
###### Proof
This is essentially (MB, 3.4).  In this case $\mathcal{M}$ consists of the $V$-fully faithful morphisms which are additionally closed under [[absolute colimits]], while $\mathcal{E}$ consists of the functors which are surjective up to absolute colimits ("Cauchy dense" functors).  When $V=Set$,  all absolute colimits are generated by retracts, and it is easy to construct an example of a fully faithful functor closed under retracts and a pushout of it which is no longer closed under retracts.
=--

An equippable 2-category with $\mathcal{E} =$ liberal cofaithfuls = liberals is called **faithfully co-conservational** in (MB).  This is the only case considered there, but the proofs generalize directly to any equippable 2-category.  Note that $V Cat$ is *not* faithfully co-conservational, since the above factorization system is only pre-equippable: $\mathcal{M}$ is not closed under pushout.  Its sub-2-category $V Cat_{cc}$ of [[Cauchy complete category|Cauchy complete]] $V$-categories is faithfully co-conservational, but this is arguably just because when restricted to $V Cat_{cc}$, the above factorization coincides with the other, better one.  Thus, it seems that perhaps in general it is better to consider the factorization system generated by the codiscrete cofibrations.


## References

* [[Ross Street]], "Fibrations in bicategories", [MR](http://www.ams.org/mathscinet-getitem?mr=574662), and [correction](http://www.ams.org/mathscinet-getitem?mr=903151).

* [[Aurelio Carboni]] and [[Scott Johnson]] and [[Ross Street]] and [[Dominic Verity]], "Modulated bicategories" (MB) [MR](http://www.ams.org/mathscinet-getitem?mr=1285544).

* [[Bob Rosebrugh]] and [[Richard Wood]], "Proarrows and cofibrations" (PC), [MR](http://www.ams.org/mathscinet-getitem?mr=961365)

[[!redirects codiscrete cofibrations]]
[[!redirects two-sided cofibration]]
[[!redirects two-sided cofibrations]]
[[!redirects two-sided codiscrete cofibration]]
[[!redirects two-sided codiscrete cofibrations]]
[[!redirects gamut]]
[[!redirects gamuts]]
[[!redirects conservational bicategory]]
[[!redirects conservational bicategories]]
[[!redirects faithfully conservational bicategory]]
[[!redirects faithfully conservational bicategories]]
[[!redirects co-conservational bicategory]]
[[!redirects co-conservational bicategories]]
[[!redirects faithfully co-conservational bicategory]]
[[!redirects faithfully co-conservational bicategories]]
[[!redirects modulated bicategory]]
[[!redirects modulated bicategories]]
[[!redirects comodulated bicategory]]
[[!redirects comodulated bicategories]]
