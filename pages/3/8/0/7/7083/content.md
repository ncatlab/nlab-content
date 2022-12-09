
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# h-Sets
* table of contents
{: toc}

## Idea
 {#Idea}

In [[homotopy type theory]] an _h-set_ is a [[type]] $X$ -- hence a [[homotopy type]] -- with the special property that any two of its [[terms]] $x,y : X$ are [[equality|equal]] ([[equivalence|equivalent]]) in an at most essentially unique way, hence that the [[identity type]] $(x = y) : Type$ is an [[h-proposition]].

The notion of h-set is an [[internalization]] of the notion of [[0-truncated]] object into homotopy type theory, essentially an internalization of the notion of _[[set]]_ (or possibly of _[[preset]]_). See below in _[Relation to internal sets](#RelationToInternalSets)_ for more on this.

h-Sets can also be regarded as a way of embedding [[extensional type theory]] into [[intensional type theory]].


## Definition

Let $A$ be a [[type]] in [[dependent type theory]] with [[dependent sums]], [[dependent products]], and [[identity types]].  We define a new type $isSet(A)$ as follows:

$$isSet(A) \coloneqq \prod_{x\colon A} \prod_{y\colon A} isProp(x=y)$$

(using any equivalent definition of the [[predicate]] [[isProp]] for [[h-propositions]]; and where "$\prod$" denotes [[dependent product]] types and "$=$" denotes [[identity types]]).


In other words, the only relationship between two elements of an h-set is whether they are equal; there is no room for more than one path between them.  By [[beta reduction|beta-reducing]] this definition, we can express it as
$$isSet(A) \coloneqq \prod_{x,y\colon A} \prod_{p,q\colon x=y} (p=q)$$
In other words, any two parallel paths in $A$ are equal.

A provably [[equivalence in homotopy type theory|equivalent]] definition is
$$isSet(A) \coloneqq \prod_{x\colon A} \prod_{p\colon x=x} (p=id_x)$$
This says that a version of Streicher's "[[axiom K]]" holds for h-sets. (See also at _[[axiom UIP]]_.)


## Examples

* Most (non-[[higher inductive type|higher]]) [[inductive types]] are h-sets (assuming that all their parameters and indices are so).  In particular, the type of [[natural numbers]] is an h-set.  This can be proven from Theorem \ref{DecidableIsSet} below.

* In a [[set-level type theory]], *all* types are h-sets.

* The [[univalence axiom]] is the only well-known property that implies that *not* all types are h-sets.  In particular, it implies that the [[universe type]] is not an h-set, and that many [[higher inductive types]] are not h-sets.


## Properties

### Equivalent characterizations

There are some equivalent characterizations of a type $A$ being an h-set:

* A type $A$ is an h-set if and only if all its identity types $x=_A y$ have [[split support]], i.e. $\prod_{(x,y:A)} \Vert x=y\Vert \to (x=y)$.  This is proven in [(KECA)](#KECA).

* More generally, $A$ is an h-set if and only if there is some $R:A\to A\to Prop$ which is reflexive (i.e. $\prod_{(x:A)} R(x,x)$) and such that $\prod_{(x,y:A)} R(x,y) \to (x=y)$.  This is Theorem 7.2.2 in the [[HoTT Book]].

### Hedberg's theorem

[[Hedberg's theorem]] states that

\begin{theorem}
Suppose that $A$ is a [[type]] with [[untruncated decidable equality]], a type such that for every element $a:A$ and $b:A$, there is an element in the sum type of the identity type $a =_A b$ and the type of functions from $a =_A b$ to the [[empty type]]. 

$$a:A, b:A \vdash \delta(a, b):(a =_A b) + (a =_A b) \to \emptyset$$

Then $A$ is a h-set.
\end{theorem}

A proof of this theorem could be found in [[Hedberg's theorem]]. 

### Relation to internal sets
 {#RelationToInternalSets}

When using [[homotopy type theory]] as the ambient [[foundations]], h-sets generally play the role of the [[sets]].  When homotopy type theory is the [[internal logic]] of some [[(∞,1)-category]], then the h-sets are the "internal sets" in this internal logic.  (Not to be confused with the other meaning of [[internal set]].)

Note, though, that this notion of "internal set" is of a different sort from the usual notions of [[internal category]] or [[internal groupoid]].  If an internal set is an h-set, then an "internal groupoid" should mean a 1-truncated type, whereas an internal groupoid usually means some kind of [[groupoid object in an (∞,1)-category]].  Conversely, the usual meaning of "internal groupoid" suggests that the meaning of "internal set" should be something more like a [[setoid]], with the h-sets being more like [[presets]].  This latter meaning is how "sets" are more often defined by constructive type theorists.

The point is that to be worthy of the name "set", a notion ought to come with "[[quotients]] of [[equivalence relations]]".  If we start with a notion which does *not* have quotients, such as the types in ordinary [[Martin-Löf dependent type theory]], then in order to get a good notion of "set" we need to "freely add quotients", which semantically means passing to the [[exact completion]] whose objects are [[setoids]].  But if we start with a notion that does have quotients, then this is unnecessary.  In homotopy type theory, h-sets do have quotients, which can be constructed using [[higher inductive types]]; thus it makes sense to call them "sets" rather than "presets".

A good way to reconcile these seemingly clashing terminologies is to talk about [[exact completions]] of [[unary sites]] or [[(∞,1)-sites]].  The presence of a [[Grothendieck topology]] allows us to "remember" to what extent our given notion has well-behaved quotients: if we have no quotients, then we use the [[trivial topology]], whereas if we have quotients, we can use the [[regular topology]].  And the exact completion builds in quotients "freely" but preserving those which the topology asserts to already exist.  In particular, if we start with quotients (an [[exact category]] or $(\infty,1)$-category), then the exact completion of the regular topology is idempotent, whereas if we start with a trivial topology, then the exact completion gives a category of setoids.  Thus, in general, the good notion of "internal set" in a unary site is "object of the exact completion".

### Pretopos of hsets
 {#PretoposOfHsets}

The h-sets in [[HoTT]] form a [[ΠW-pretopos]] ([Rijke-Spitters 13](#RijkeSpitters13)). See also at _[[structural set theory]]_.

## Related concepts

[[!include homotopy n-types - table]]

[[!include types and logic - table]]


## References

* {#Hedberg} Michael Hedberg, *A coherence theorem for Martin-L&#246;f's type theory*, J. Functional Programming, (1998)
 

* Nicolai Kraus, *A direct proof of Hedberg's theorem*, [blog post](http://homotopytypetheory.org/2012/03/30/a-direct-proof-of-hedbergs-theorem/)

* {#KECA} [[Nicolai Kraus]], [[Martin Escardo]], [[Thierry Coquand]] , [[Thorsten Altenkirch]], _Generalizations of Hedberg's theorem_, in M. Hasegawa (Ed.): TLCA 2013, LNCS 7941, pp. 173-188. Springer, Heidelberg 2013. ([pdf](http://www.cs.bham.ac.uk/~mhe/papers/hedberg.pdf))
 

Formalization of [[set theory]] via h-sets in [[homotopy type theory]] (see at [[Set in homotopy type theory]])

* {#RijkeSpitters13} [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_, Mathematical Structures in Computer Science, Volume 25, Issue 5 (From type theory and homotopy theory to Univalent Foundations of Mathematics)  ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

which became one chapter in 

* [[Univalent Foundations Project]], _[[Homotopy Type Theory – Univalent Foundations of Mathematics]]_


[[!redirects h-set]]
[[!redirects h-sets]]
[[!redirects hSet]]
[[!redirects hSets]]
[[!redirects 0-truncated type]]
[[!redirects 0-truncated types]]
[[!redirects h-level 2]]
[[!redirects h-level 2 type]]
[[!redirects h-level 2 types]]
