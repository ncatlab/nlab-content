
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
* automatic table of contents
{:toc}

## Idea

A simplicial object $X$ in a [[category]] $C$ is a collection $\{X_n\}_{n \in \mathbb{N}}$ of [[objects]] in $C$ that behave as if $X_n$ were an $n$-dimensional [[simplex]] [[internalization|internal to]] $C$. 


## Definition

A **simplicial object** in a category $C$ is a [[functor]] $\Delta^{op} \to C$, where $\Delta$ is the [[simplex category|simplicial indexing category]].

A **cosimplicial object** in $C$ is similarly a functor out of the [[opposite category]], $\Delta \to C$.

Accordingly, simplicial and cosimplicial objects in $C$ themselves form a [[category]] in an obvious way, namely the [[functor category]] $[\Delta^{op},C]$ and $[\Delta,C]$, respectively.

**Remark**

A **simplicial object** $X$ in $C$ is often specified by 
the objects, $X_n$, which are the images under $X$, of the objects $[n]$ of $\Delta$, together with a description of the face and degeneracy morphisms, $d_i$ and $s_j$, which must satisfy the [[simplicial identities]].

## Examples

* A simplicial object in [[Set]] is a [[simplicial set]].

* A simplicial object in a category of [[presheaves]] is a [[simplicial presheaf]].

* A simplicial object in [[Top]] is a [[simplicial topological space]].

* A simplicial object in [[Diff]] is a [[simplicial manifold]].

* A simplicial object in the category [[Grp]] of [[groups]] is a [[simplicial group]]. See also [[Dold-Kan correspondence]].

* A simplicial object in [[Ring]] is a [[simplicial ring]].

* A cosimplicial object in the category of [[rings]] ([[algebras]]) is a [[cosimplicial ring]] ([[cosimplicial algebra]]).

* A simplicial object in a category of simplicial objects is a [[bisimplicial object]].

* A cosimplicial object in [[sSet]] is a [[cosimplicial simplicial set]] (equivalently a simplicial object in cosimplicial sets).

* The [[bar construction]] produces a simplicial object from a [[monad]] and an algebra over that monad.

## Category of simplicial objects

For $D$ a [[category]], we write $D^{\Delta^{op}}$ for the [[functor category]] from $\Delta^{op}$ to $D$: its category of simplicial objects.

+-- {: .un_defn}
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

+-- {: .un_prop}
###### Proposition

With the above definitions $D^{\Delta^{op}}$ becomes an [[nLab:sSet]]-[[nLab:enriched category]] which is both [[nLab:copower|tensored]] as well as [[nLab:power|cotensored]] over $sSet$.

=--

+-- {: .un_def}
###### Definition

We may regard the category of cosimplicial objects $D^{\Delta}$ as an $sSet$-enriched category using the above enrichment by identifying

$$
  D^{\Delta} \simeq ({D^{op}}^{\Delta^{op}})^{op}
  \,.
$$

=--




[[!redirects simplicial objects]]
[[!redirects cosimplicial object]]
[[!redirects cosimplicial objects]]

[[!redirects category of simplicial objects]]
[[!redirects category of cosimplicial objects]]

[[!redirects categories of simplicial objects]]
[[!redirects categories of cosimplicial objects]]