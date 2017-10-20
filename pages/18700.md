# Linear bicategories

* table of contents
{: toc}

## Idea

The notion of *linear bicategory* (or *linearly distributive bicategory* for long) is a [[horizontal categorification]] of the notion of [[linearly distributive category]], analogous to how [[bicategories]] are a horizontal categorification of [[monoidal categories]].

## Definition

+-- {: .un_defn}
###### Definition
A **linear bicategory** consists of

1. A set of objects $x,y,z$.
1. For each $x,y$ a hom-category $B(x,y)$.
1. Two bicategory structures $(\otimes,\top)$ and $(\parr,\bot)$ on these hom-categories.  Thus we have two compositions $\otimes,\parr : B(y,z) \times B(x,y) \rightrightarrows B(x,z)$ and two units $\top_x,\bot_x \in B(x,x)$, each coherently associative and unital.
1. Linear distributivities $(X \parr Y) \otimes Z \to X \parr (Y\otimes Z)$ and $X \otimes (Y \parr Z) \to (X\otimes Y) \parr Z$, satisfying the usual coherence laws for a [[linearly distributive category]].
=--

## Examples

* Linear bicategories with one object coincide with the [[deloopings]] of (non-symmetric) [[linearly distributive categories]].
* Any [[allegory]] whose hom-sets are [[Boolean algebras]] is a linear bicategory, with $\otimes$ the usual composition and with $X \parr Z = \neg (\neg X^\circ \otimes \neg Y^\circ)^\circ$.  In particular, this includes the bicategory of [[relations]] in any [[Boolean category]], such as [[Set]] (assuming [[classical logic]]).
* Any ordinary [[bicategory]] can be regarded as a linear bicategory with $\otimes = \parr$.
* If $B$ is a linear bicategory (such as the delooping of a [[linearly distributive category]]) such that $(B,\otimes,\top)$ has [[local colimits|local coproducts]] and $(B,\parr,\bot)$ has local products, then the bicategory $Mat(B)$ (whose objects are families of objects of $B$ and whose morphisms are matrices of 1-cells in $B$) is again a linear bicategory.  For instance, if $B$ is the [[Boolean algebra]] $\mathbf{2}$ of [[truth values]], then $Mat(\mathbf{2}) \cong Rel(Set)$.

## Linear adjoints

+-- {: .un_defn}
###### Definition
A **linear adjunction** in a linear bicategory consists of 1-cells $f:X\to Y$ and $g:Y\to X$ along with a unit $\eta : \top_X \to g \parr f$ and $\epsilon : f \otimes g \to \bot_Y$ satisfying versions of the usual [[triangle identities]]  that include the linear distributivities, as for [[dual objects]] in a [[linearly distributive category]]
=--

A linear bicategory in which every 1-cell has both a linear right adjoint and a linear left adjoint is a horizontal categorification of a [[non-symmetric star-autonomous category]].  But in [Cockett-Koslowski-Seely](#CKS00) this is called a "closed linear bicategory", with the term "$\ast$-linear bicategory" reserved for something stronger analogous to a [[cyclic star-autonomous category]].

## References

* [[Robin Cockett|Cockett]] and Koslowski and [[Robert Seely|Seely]], *Introduction to linear bicategories*, Mathematical Structures in Computer Science, 10 (2), 2000 (165 - 203)
 {#CKS00}


[[!redirects linear bicategories]]
[[!redirects linearly distributive bicategory]]
[[!redirects linearly distributive bicategories]]
[[!redirects linear adjoint]]
[[!redirects linear adjoints]]
[[!redirects linear adjunction]]
[[!redirects linear adjunctions]]
