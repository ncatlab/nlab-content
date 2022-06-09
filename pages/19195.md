+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

##Idea

**Two-level type theory** (2LTT) refers to versions of [[Martin-Lof type theory]] that combine two type theories: one level as a [[homotopy type theory]], which may include [[univalence axiom|univalent]] universes and [[higher inductive types]], and the second level as a traditional form of type theory validating [[uniqueness of identity proofs]]. The second layer may be understood as the internalised meta-theory of the first.

The rules are much inspired by the homotopical semantics in [[fibration categories]] and [[model categories]], according to which the types of the homotopy layer are sometimes called **[[fibrant object|fibrant]] types** and the others **non-fibrant types**.  An alternative terminology is simply **types** (since these are the objects of real interest) and **pretypes** (an auxiliary structure used to study the types).

In other words, where default [[homotopy type theory]] has [[categorical semantics]] (see at _[[relation between category theory and type theory]]_) in suitable [[type-theoretic model categories]] but in such a way that only the [[(infinity,1)-category]] [[presentable (infinity,1)-category|presented]] by that really matters, in two-level type theory one adds explicit control over the presenting model category (or other kind of [[fibration category]]), thus apparently breaking the $(\infty,1)$-categorical "[[principle of equivalence]]" but providing more tools for handling the presentation.  It is an open question to what extent the principle of equivalence is actually broken, i.e. whether results proven in two-level type theory can be transferred to any model categorical presentation.

## Type theories

* The first proposal for two-level type theory was [[Vladimir Voevodsky]]'s [[Homotopy Type System]].  This system had a reflection rule collapsing the non-fibrant "exact equality" to [[judgmental equality]], making some things easier but making type-checking undecidable.

* More recently the proposals of [ACK](#ACK17) simply assumes [[uniqueness of identity proofs]] for the exact equality; this seems to suffice for most if not all purposes.

* [[computational type theory|Computational]]  [[cubical type theory]] can also include  a non-fibrant layer: its syntax is interpreted as cubical sets, where "fibrancy" is a *defined* condition on pretypes (existence of Kan operations).

## Applications

### Semisimplicial types

Two-level type theories (including HTS and ACK) were motivated to a large extent by the technical difficulties encountered in formalizing [[semisimplicial types]] in default [[homotopy type theory]] (HoTT). This problem comes precisely from the fact that HoTT is really the [[internal language]] of some [[(infinity,1)-topos]] and hence defining [[simplicial objects]] or similar here means to speak of [[simplicial objects in an (infinity,1)-category]], which means that the [[simplicial identities]] hold only up to [[coherence|coherent]] higher [[homotopy]]. The problem of syntactically encoding the infinite amount of this [[coherence]] data remains unsolved to date. For [[semisimplicial types]] the difficulties greatly reduce (since the evident iterated [[dependent type]]-definition of a semisimplicial type is automatically interpreted by a [[Reedy model structure|Reedy]]-[[fibrant object]] in the given [[type-theoretic model category]], which takes care of all the homotopy coherence by the power of [[model category]] theory, see at _[[internal (infinity,1)-category]]_ for more on this) but technical problems remain even in formulating the plain 1-categorical [[simplicial identities]] to all degrees.

The "exact equality" of two-level type theories solves this problem because such equalities can be defined by induction.


## Variations

### Natural numbers

One important choice to be made in writing down a two-level type theory is whether there is one natural numbers type or two.  There must certainly be a fibrant natural numbers type; the question is whether the elimination rule for this "fibrant nat" allows elimination also into non-fibrant types.  If it does not, then there should also be a "non-fibrant nat" which is not fibrant, but whose elimination principle can eliminate into other non-fibrant types.

Semantically, this distinction corresponds to whether the natural numbers object of the model category presentation is already fibrant, or whether it needs to be fibrantly replaced to represent a (fibrant) type.  In some models, such as [[simplicial sets]], it is already fibrant; but in others, such as [[local model structure on simplicial presheaves]], it is not.  It is an open question whether any [[(infinity,1)-topos]] can be presented by a model category in which the natural numbers object is fibrant, and thus serve as semantics for a two-level type theory with only one natural numbers type.

Since the definition of semisimplicial types requires an inductive definition of a (non-fibrant) exact equality, if there are two nats then it must use the non-fibrant one.  This means that, without additional rules, a two-level type theory with two nats cannot define a *fibrant* type of *untruncated* semisimplicial types: for each non-fibrant $n$ it can define a fibrant type of $n$-truncated semisimplicial types, but the limit of these types over the *non-fibrant* nat is no longer fibrant.  Assuming only one nat is sufficient to solve this problem, but as mentioned above this may exclude desirable models.  Another weaker axiom, which *is* satisfied in all sufficiently nice model categories, is that fibrant types are closed under limits of towers of fibrations indexed by the non-fibrant nat.  (In two-level type theory terminology, this is a strengthening of the assumption that the non-fibrant nat is "cofibrant".)


##References

* [[homotopytypetheory:HomePage|Homotopy Type Theory Wiki]], _[[homotopytypetheory:Homotopy Type System]]_

* Thorsten Altenkirch, Paolo Capriotti, Nicolai Kraus, _Extending Homotopy Type Theory with Strict Equality_, ([ arXiv:1604.03799](https://arxiv.org/abs/1604.03799))

* Danil Annenkov, Paolo Capriotti, Nicolai Kraus, Christian Sattler, _Two-Level Type Theory and Applications_, ([arXiv:1705.03307](https://arxiv.org/abs/1705.03307))
{#ACK17}

[[!redirects 2-level type theory]]
[[!redirects 2-level type theories]]
[[!redirects 2LTT]]
[[!redirects fibrant type]]
[[!redirects fibrant types]]
[[!redirects non-fibrant type]]
[[!redirects non-fibrant types]]
