
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

Note that such a cofibration from $A$ to $C$ can be identified with the following data: a category $B' = B\setminus (A\cup C)$, profunctors $m\colon A &#8696; B$, $n\colon B &#8696; C$, and $p\colon A &#8696; C$, and a morphism $n m \to p$ of profunctors.  Such a thing is sometimes called a **gamut** from $A$ to $C$.

Now a 2-cell in $Cospan(A,C)$ is simply a natural transformation between functors $B \;\rightrightarrows\; X$ whose components on the images of $A$ and $C$ are isomorphisms.  Thus, if $B$ is a cofibration as above with the property that $B \setminus (A\cup C)$ is empty, then it must be codiscrete.  The converse is easy to check, taking $X$ to be the ordinal $4 = (0\le 1 \le 2\le 3)$ as a category.  But a gamut with $B'=\emptyset$ is nothing but a profunctor $A &#8696;C$; hence codiscrete cofibrations in $V Cat$ can be precisely identified with the collages of profunctors.

### Toposes

A codiscrete cofibration in the 2-category $Topoi$ of [[topoi]] can be identified with a [[left exact functor]].

### Double categories

Codiscrete cofibrations in the 2-category $Dbl$ of [[double categories]], [[double functors]], and [[horizontal transformations]] can be identified with [[double profunctors]].


## Construction of a proarrow equipment

This suggests that given any 2-category $K$ with finite 2-colimits, we may try to canonically equip $K$ with proarrows by defining the proarrows $A &#8696;C$ to be the codiscrete cofibrations.  The sticky point is then how to define units and composition of such proarrows in order to obtain an equipment.

The unit is obvious: we should take the unit proarrow of $A$ to be the cospan $A\to A\times I \leftarrow A$, which is always a codiscrete cofibration.

Composition is subtler.  The obvious way to compose codiscrete cofibrations $A \to B \leftarrow C$ and $C\to D \leftarrow E$, of course, is to take a [[pushout]] $B +_C D$.  It is not hard to show (see references):

+-- {: .un_theorem}
###### Theorem
In any 2-category with finite 2-colimits, if $B$ and $D$ are cofibrations, then so is $B +_C D$.
=--

However, $B +_C D$ will not be codiscrete even if $B$ and $D$ are.  In $V Cat$, if $B$ and $D$ are collages of profunctors $m$ and $n$, then $B +_C D$ represents the gamut consisting of $m$, $n$, and the composite profunctor $n m$, with the middle category being $C$.  Thus, in order to obtain the correct composite, we need to forget about $C$ somehow.  The best way to do this seems to be using a [[factorization system]] (in the weak 2-categorical sense), akin to the construction of the [[bicategory of relations]] from any [[regular category]].

The following definition is tentative.

+-- {: .un_defn}
###### Definition
A 2-category with finite 2-colimits is **equippable** if it has a [[factorization system in a 2-category|factorization system]] $(\mathcal{E},\mathcal{M})$ such that
* Every morphism in $\mathcal{E}$ is representably co-faithful and co-conservative.
* Every morphism in $\mathcal{M}$ is representably fully faithful.
* Morphisms in $\mathcal{M}$ are closed under pushout and under copowers with $I$.
=--

Co-conservative arrows are called **liberal**.  A **faithfully co-conservational bicategory**, in the sense of the paper (MB) referenced below, is an equippable bicategory in which $\mathcal{E}$ is precisely the class of liberal arrows, and all liberal arrows are also cofaithful; in this case the arrows of $\mathcal{M}$ are called **strong conservative**.  The definition of equippable 2-category is a direct generalization of that of "faithfully co-conservational bicategory" to allow alternate factorization systems, so we will refer many proofs to their analogues in (MB).

+--{: .query}
[[Mike Shulman]]: Disclaimer: I have not carefully checked that the above definition isolates exactly the properties necessary for the proofs to go through, but I believe it does.
=--

Examples include:

* $V Cat$ is equippable for any suitable $V$, where $\mathcal{E}$ is the class of essentially surjective functors and $\mathcal{M}$ is the class of $V$-fully-faithful functors.  This is a special case of a general 2-categorical situation considered below.

* A functor between [[Cauchy completion|Cauchy complete]] $V$-categories is essentially surjective if and only if it is liberal.  Therefore, $V Cat_{cc}$ is faithfully co-conservational.  However, $V Cat$ is not co-conservational: strong-conservative functors between non-Cauchy-complete categories are not only $V$-fully faithful but closed under retracts, and these need not be preserved by pushout, even when $V=Set$.

In an equippable 2-category $K$, we can define the composite of two codiscrete cofibrations $A \to B \leftarrow C$ and $C\to D \leftarrow E$ by first taking the pushout $B +_C D$, and then factoring the morphism $A+E \to B +_C D$ as an $\mathcal{E}$-map followed by an $\mathcal{M}$-map, $A+E \to G \to B +_C D$.  By (MB, 4.18), the resulting cospan $A \to D \leftarrow E$ is a cofibration, and since $A+E \to G$ is in $\mathcal{E}$, it is cofaithful and liberal, hence $G$ is codiscrete.

One can then show (MB, section 4) that there is a 2-category $CdCofib(K)$ with the same objects as $K$ and with codiscrete cofibrations as 1-morphisms, and a locally fully faithful identity-on-objects (pseudo) 2-functor $(-)_* K\to CdCofib(K)$ such that each 1-morphism $f_*$ has a right adjoint.  Therefore, $K$ is canonically a [[2-category equipped with proarrows]] (hence the term "equippable").

One can then impose additional axioms on $K$ to get good behavior of this equipment, and try to characterize the equipments arising in this way; see (MB, section 5) and (PC).

### The strongly fully faithful factorization system

...


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
