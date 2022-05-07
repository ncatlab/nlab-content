
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
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

A _simplicial object_ $X$ in a [[category]] $C$ is an _[[simplicial set]]_ [[internalization|internal]] to $C$: a collection $\{X_n\}_{n \in \mathbb{N}}$ of [[objects]] in $C$ that behave as if $X_n$ were an object of $n$-dimensional [[simplices]] [[internalization|internal to]] $C$ equipped with maps between these space that assign faces and degenerate simplices.

For instance, and there is a longer list further down this page, a simplicial object in $Grps$ is a collection $\{G_n\}_{n\in \mathbb{N}}$ of groups, together with face and degeneracy _homomorphisms_ between them. This is just a [[simplicial group]]. We equally well have other important instances of the same idea, when we replace $Grps$ by other categories, or higher categories.


## Definition

A **simplicial object** in a [[category]] $C$ is a [[functor]] $\Delta^{op} \to C$, where $\Delta$ is the [[simplex category|simplicial indexing category]].

More generally, a simplicial object in an [[(∞,1)-category]] is an [[(∞,1)-functor]] $\Delta^{op} \to C$.

A **[[cosimplicial object]]** in $C$ is similarly a functor out of the [[opposite category]], $\Delta \to C$.

Accordingly, simplicial and cosimplicial objects in $C$ themselves form a [[category]] in an obvious way, namely the [[functor category]] $[\Delta^{op},C]$ and $[\Delta,C]$, respectively.

**Remark**

A **simplicial object** $X$ in $C$ is often specified by 
the objects, $X_n$, which are the images under $X$, of the objects $[n]$ of $\Delta$, together with a description of the face and degeneracy morphisms, $d_i$ and $s_j$, which must satisfy the [[simplicial identities]].

## Examples
 {#Examples}

* A simplicial object in [[Set]] is a [[simplicial set]].

* A simplicial object in a category of [[presheaves]] is a [[simplicial presheaf]].

* A simplicial object in [[Top]] is a [[simplicial topological space]].

* A simplicial object in [[Diff]] is a [[simplicial manifold]].

* A simplicial object in the category [[Grp]] of [[groups]] is a [[simplicial group]]. See also [[Dold-Kan correspondence]].

* A simplicial object in the category of [[topological group]]s is a [[simplicial topological group]].

* A simplicial object in [[Lie algebra]]s is a [[simplicial Lie algebra]].

* A simplicial object in [[Ring]] is a [[simplicial ring]].

* A cosimplicial object in the category of [[rings]] ([[algebras]]) is a [[cosimplicial ring]] ([[cosimplicial algebra]]).

* A simplicial object in a category of simplicial objects is a [[bisimplicial object]].

* A cosimplicial object in [[sSet]] is a [[cosimplicial simplicial set]] (equivalently a simplicial object in cosimplicial sets).

* The [[bar construction]] produces a simplicial object from a [[monad]] and an algebra over that monad.

## Category of simplicial objects

For $D$ a [[category]], we write $D^{\Delta^{op}}$ for the [[functor category]] from $\Delta^{op}$ to $D$: its category of simplicial objects.

### Simplicial enrichment

+-- {: .num_defn #SimplicialEnrichment}
###### Definition

Let $D$ be a [[nLab:category]] with all [[nLab:limit]]s and [[nLab:colimit]]s. This implies that it is [[nLab:copower|tensored]] over [[nLab:Set]]

$$
  \cdot : D \times Set \to D
  \,.
$$

This induces a functor

$$
  \cdot^{\Delta^{op}} : D^{\Delta^{op}} \times sSet \to D^{\Delta^{op}}
$$

which we shall also write just "$\cdot$".

For $X,Y \in D^{\Delta^{op}}$ write

$$
  D^{\Delta^{op}}(X,Y) := Hom_{D^{\Delta^{op}}}(X \cdot \Delta[\bullet], Y)
  \in sSet
$$

and for $X,Y,Z \in D^{\Delta^{op}}$ let

$$
  D^{\Delta^{op}}(X,Y)
    \times  
  D^{\Delta^{op}}(Y,Z)
  \to 
  D^{\Delta^{op}}(X,Z)
$$

be given in degree $n$ by

$$
  (X \cdot \Delta[n] \to Y, Y \cdot \Delta[n] \to Z)
  \mapsto
  ( X \cdot \Delta[n] \to X \cdot \Delta[n]\times \Delta[n] \to Y \cdot \Delta[n]  \to Z)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

With the above definitions $D^{\Delta^{op}}$ becomes an [[nLab:sSet]]-[[nLab:enriched category]] which is both [[nLab:copower|tensored]] as well as [[nLab:power|cotensored]] over $sSet$.

=--

+-- {: .num_defn}
###### Definition

We may regard the category of cosimplicial objects $D^{\Delta}$ as an $sSet$-enriched category using the above enrichment by identifying

$$
  D^{\Delta} \simeq ({D^{op}}^{\Delta^{op}})^{op}
  \,.
$$

=--

### Geometric realization

If $D$ is already a [[simplicially enriched category]] in its own right, with [[powers]] and [[copowers]], we can define the [[geometric realization]] of a simplicial object $X\in D^{\Delta^{op}}$ as a [[coend]]:

$$ |X| = \int^{[n]\in\Delta} \Delta[n] \odot X_n $$

where $\odot$ denotes the [[copower]] for the simplicial enrichment of $D$.  This is [[left adjoint]] to the "total singular object" functor $D \to D^{\Delta^{op}}$ sending $Y$ to the simplicial object $n\mapsto Y^{\Delta[n]}$, the [[power]] for the simplicial enrichment.

Perhaps surprisingly, this adjunction is even a *simplicially enriched* adjunction when $D^{\Delta^{op}}$ has its simplicial structure from Definition \ref{SimplicialEnrichment}, even though the latter makes no reference to the given simplicial enrichment of $D$.  A proof can be found in [RSS01, Proposition 5.4](#RSS01).


## Related concepts

* [[simplex]], [[simplex category]]

* **simplicial object**

  * [[simplicial set]]

  * [[simplicial diagram]]

  * [[simplicial object in an (∞,1)-category]]

* [[semi-simplicial object]]

  * [[semisimplicial set]]

* [[globular set]], [[cubical set]]

* [[nerve]], [[nerve and realization]]

* [[Segal condition]]

## References

An early discussion of simplicial objects is in:

* [[Alexander Grothendieck]], p. 108 (11 of 21) in: _Techniques de construction et théorèmes d'existence en géométrie algébrique III : préschémas quotients_, Séminaire Bourbaki : années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf))


See also:

* [[Peter May]], _Simplicial objects in algebraic topology_, University of Chicago Press 1967 ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]])

* [[Dai Tamaki]], [[Akira Kono]], Appendix A.1 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))


* {#RSS01} [[Charles Rezk]], [[Stefan Schwede]], and [[Brooke Shipley]], *Simplicial structures on model categories and functors*, [arxiv](https://arxiv.org/abs/math/0101162)

[[!redirects simplicial objects]]


[[!redirects category of simplicial objects]]

[[!redirects categories of simplicial objects]]

category: simplicial object