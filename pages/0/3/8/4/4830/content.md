

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _derived $\infty$-Lie algebroid_ is an [[∞-Lie algebroid]] whose underlying space is a _derived space_ , for instance a [[derived smooth manifold]].

More precisely, let $T$ be any abelian [[Lawvere theory]] and $T \hookrightarrow C \hookrightarrow T Alg^{op}$ a small full subcategory of geometric test objects formally dual to [[algebra over a Lawvere theory|T-algebras]]. Then by the theory of [[function algebras on ∞-stacks]] over $C$ one identifies $\infty LieAlgd$ with the subcategory

$$
  (T Alg^\Delta)^{op} \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\to}
  [C^{op}, sSet]
$$

of the [[(∞,1)-category of (∞,1)-sheaves]] on $C$ modeled by [[cosimplicial algebra|cosimplicial T-algebra]]s. Under the [[Dold-Kan correspondence]] applied to the underlying cosimplicial ordinary algbra, this identifies with _non-negatively graded_ [[dg-algebra]]s: the [[Chevalley-Eilenberg algebra]]s of the corresponding dual $\infty$-Lie algebroids.

But in full [[derived geometry]] this setup is further generalized: instead of considering [[∞-stack]]s on just a category of duals of $T$-algebras, one considers [[derived ∞-stack]]s over an [[(∞,1)-site]] of [[simplicial algebra]]s. Let $T \hookrightarrow C^{\Delta^{op}} \hookrightarrow T Alg^{\Delta^{op}}$ be accordingly a small subcategory of simplicial $T$-algebra,  then the above adjunction generalizes to

$$
  ((T Alg^{\Delta^{op}})^\Delta)^{op} \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\to}
  [C^{op}, sSet]
  \,,
$$

where now on the left we have _cosimplicial simplicial algebras_ . Under the Dold-Kan correspondence these now identify with _unbounded_ dg-algebras $CE(\mathfrak{a})$. We have that 

* the _categorical degree_ $k$ coming from [[k-morphism]]s of the $\infty$-sheaves contributes to positive degrees in $CE(\mathfrak{a})$;

* the _derived_ degree $l$ coming from $l$-morphisms in the $\infty$-function algebras ontribute to negative degree.

This category $(T Alg^{\Delta^{op} \times \Delta})^{op}$ we identify with that of _derived_ $\infty$-Lie algebroids.

## Examples

### BV-BRST complex

In the literature the most familiar example of a derived $\infty$-Lie algebroids -- even if not under this name -- are the [[BV-BRST complex]]es. These are [[action Lie algebroid]]s for actions of [[∞-Lie algebra]]s on [[derived smooth manifold]]s.

