

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition


A  **separated** [[(2,1)-presheaf]]/[[prestack]] over a [[(2,1)-site]] $C$ is a [[(2,1)-presheaf]] $X : C^{op} \to Grpd$ such that [[covering]] families $\{U_i \to U\}$ in $C$ the [[descent]] morphism

$$
  X(U) \to PSh_{(2,1)}(S(\{U_i\}), X)
$$ 

is a [[full and faithful functor]] and hence exhibits a [[full subcategory]].

(Here $S(\{U_i\})$ denotes the [[sieve]] associated to the cover).

If this morphism is even an [[equivalence of categories]], then $X$ is even a [[(2,1)-sheaf]]/[[stack]].

=--

+-- {: .un_remark}
###### Remark on terminology

The term _prestack_ is used in two different ways in the literature: some authors use it synonymously with just [[(2,1)-presheaf]], others with _separated $(2,1)$-presheaf_ .

=--

## Examples

Let [[Mfd]] be the [[site]] of [[topological manifold]]s. Let $G$ be a [[topological group]] and $\bar W G$ the [[(2,1)-presheaf]] on $Mfd$ represented by the [[nerve]] of the [[delooping]]-[[groupoid]] (see [[simplicial group]] for te notation). Let $G Bund$ be the [[(2,1)-sheaf]] of all $G$-[[principal bundle]]s. This is the [[(2,1)-sheafification]] of $\bar W G$. The canonical morphism

$$
  \bar W G \to G Bund
$$

includes over each $U \in Mfd$ the single object of $(\bar W G)(U)$ as the trivial $G$-[[principal bundle]]. Its [[automorphism]]s are given by [[continuous function]]s $C(U,G)$. This is the same on both sides, hence $(\bar W G)(U) \to G Bund(U)$ is a [[full and faithful functor]] and $\bar W G$ is a separated $(2,1)$-presheaf.

## Related concepts

* [[separated presheaf]]

* **separated $(2,1)$-presheaf**

* [[separated (∞,1)-presheaf]]

[[!redirects prestack]]

[[!redirects separated prestack]]


[[!redirects separated (2,1)-presheaves]]

[[!redirects prestacks]]