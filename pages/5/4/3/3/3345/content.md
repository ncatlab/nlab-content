
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There is a [[model category]] structure on the [[category]] $[\Box^{op},Set]$ of [[cubical set]]s whose [[homotopy theory]] is that of the [[classical model structure on simplicial sets]].

Using this version of the [[homotopy hypothesis]]-theorem, cubical sets are a way to describe the [[homotopy type]] of [[∞-groupoid]]s using of all the [[geometric shapes for higher structures]] the [[cube]].


## Definition

There is an evident [[simplicial set]]-valued [[functor]]

$$
  \Box \to sSet
$$

from the [[cube category]] to [[sSet]], which sends the cubical $n$-cube to the simplicial $n$-cube

$$
  \mathbf{1}^n \mapsto (\Delta[1])^{\times n}
  \,.
$$

Similarly there is a canonical [[Top]]-valued functor

$$
  \Box \to Top
$$

$$
  \mathbf{1}^n \mapsto (\Delta^1_{Top})^n
  \,.
$$

The corresponding [[nerve and realization]] [[adjunction]]

$$
  (|-| \dashv Sing_\Box) : Top \stackrel{\overset{|-|}{\leftarrow}}{\underset{Sing_\Box}{\to}} Set^{\Box^{op}}
$$

is the cubical analogue of the simplicial nerve and realization discussed [above](#ForKanComplexes).

+-- {: .num_theorem}
###### Theorem


There is a [[model structure on cubical sets]] $Set^{\Box^{op}}$ whose

* weak equivalences are the morphisms that become weak equivalences under geometric realization $|-|$;

* cofibrations are the [[monomorphism]]s.

=--

This is ([Jardine, section 3](#Jardine)).

Explicitly, a set of generating cofibrations is given by the boundary inclusions $\partial \Box^n \to \Box^n$, and a set of generating acyclic cofibrations is given by the horn inclusions $\sqcap_{k,\epsilon}^n \to \Box^n$. This is ([Cisinski, Thm 8.4.38](#Cisinski)). Thus, as a consequence of Cisinski's work, the fibrations are exactly cubical Kan fibrations.

## Properties

### Homotopy theory
 {#HomotopyTheory}

The following theorem establishes a form of the [[homotopy hypothesis]] for cubical sets.

+-- {: .num_theorem}
###### Theorem

The [[unit of an adjunction|unit of the adjunction]]

$$
  A \to Sing_\Box(|A|)
$$

is a weak equivalence in $Set^{{\Box}^{op}}$ for every cubical set $A$.

The counit of the adjunction

$$
  |Sing_\Box X| \to X
$$

is a weak equivalence in $Top$ for every topological space $X$.

It follows that we have an [[equivalence of categories]] induced on the [[homotopy categories]]

$$
  Ho(Top) \simeq Ho(Set^{\Box^{op}})
  \,.
$$

=--

This is ([Jardine, theorem 29, corollary 30](#Jardine)).

In fact, by the discussion at _[[adjoint (∞,1)-functor]]_  it follow that the [[derived functors]] of the adjunction exhibit the [[simplicial localizations]] of cubical sets equivalent to that of simplicial sets, hence makes their [[(∞,1)-categories]] [[equivalence of (∞,1)-categories|equivalent]] (hence equivalent to [[∞Grpd]]). 


## Other kinds of cubical sets

In [[cubical type theory]] one uses more structured notions of cubical set (symmetric, cartesian, De Morgan, etc.)  In most cases such categories have both a test model structure, which is equivalent to spaces, and a [[cubical-type model structure]] that corresponds to the interpretation of type theory.  In many cases these are *not* equivalent, and the cubical-type model structure does not model classical homotopy types.  See [[cubical-type model structure]] for more discussion.


## Joyal-type model structures

In complete analogy to [[simplicial sets]], there is also an analogue of the [[Joyal model structure]] on [[cubical sets]], with or without connection.  See the article [[model structures for cubical quasicategories]].


## Related concepts

* [[cubical set]]

* [[cubical set with connections]]

* [[test category]], [[strict test category]]

* [[Cisinski model structure]]

* [[model structures for cubical quasicategories]]

## References

### Cubical sets without connections

Using that the [[cube category]] is a [[test category]] a model structure on cubical sets follows as a special case of the [[model structure on presheaves over a test category]], due to 

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Asterisque __308__.
  {#Cisinksi}

Cisinski also derives explicit generating cofibrations and generating acyclic cofibrations using his theory of [[generalized Reedy category]], or _categories skelettiques_. See Section 8.4.

The model structure on cubical sets as above is given in detail in

* [[J. F. Jardine]], _Cubical homotopy theory: a beginning_ (2002) ([pdf](https://web.archive.org/web/20210507014113/http://hopf.math.purdue.edu/Jardine/cubical2.pdf)) 
{#Jardine}

### Cubical sets with max-connections

The following paper proves that [[cubical sets with connections]] (more specifically, max-connections) form a [[strict test category]] and therefore admit a [[cartesian model structure]] that is Quillen equivalent to the [[Kan–Quillen model structure]] on [[simplicial sets]]:

* [[Georges Maltsiniotis]], _La catégorie cubique avec connexions est une catégorie test stricte_, Homology, Homotopy and Applications 11:2 (2009), 309-326.  [doi](http://dx.doi.org/10.4310/hha.2009.v11.n2.a15).

### Cubical sets with max-connections and min-connections

The case of cubical sets with both max-connections and min-connections largely follows the case of cubical sets with max-connections, the corresponding category of cubes again being a [[strict test category]].
The relevant results are stated explicitly as Corollary 3 and Theorem 3 of

* [[Ulrik Buchholtz]], Edward Morehouse, _Varieties of Cubical Sets_,  In: Relational and Algebraic Methods in Computer Science. RAMICS 2017. Lecture Notes in Computer Science, vol 10226. [doi](http://dx.doi.org/10.1007/978-3-319-57418-9_5) [arXiv](https://arxiv.org/abs/1701.08189).

### Cartesian cubical sets

The case of the category of presheaves over the free finite product category with a bipointed object is treated in:

* [[Steve Awodey]], _Cartesian cubical model categories_ ([arXiv:2305.00893](https://arxiv.org/abs/2305.00893))


[[!redirects model structures on cubical sets]]