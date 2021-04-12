[[!redirects (∞,1)-pretopos]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The concept of _$(\infty,1)$-pretopos_ ([Lurie, appendix A](#Lurie)) is a version of the concept of _[[pretopos]]_ as one passes from [[toposes]] to [[(∞,1)-toposes]]. The definition is a variant of the characterization of [[Grothendieck (∞,1)-toposes]], via the [Giraud-Rezk-Lurie axioms](infinity-topos#GiraudAxioms), asking only for [[finite (∞,1)-limits]] and [[finite (∞,1)-colimits]] with some exactness properties relating them.

## Definition

+-- {: .num_defn #InfinityPreTopos}
###### Definition


Let $\mathcal{C}$ be an [[(∞,1)-category]]. This is called an _$(\infty,1)$-pretopos_ if

1. $\mathcal{C}$ has a [[terminal object in an (∞,1)-category|terminal object]] and [[homotopy fiber products]];

1. $\mathcal{C}$ has [[finite (∞,1)-colimits]];

1. finite [[coproducts]] in $\mathcal{C}$ are [[universal colimits|universal]] and [[disjoint coproducts|disjoint]];

1. [[groupoid object in an (infinity,1)-category|groupoid objects]] in $\mathcal{C}$ are effective:

1. realization of groupoid objects is [[universal colimit|universal]].

If these conditions hold except possibly for the existence of a [[terminal object in an (∞,1)-category|terminal object]], then $\mathcal{C}$ is a _local $(\infty,1)$-pretopos._

=--

[Lurie, def. A:6.1.1](#Lurie)

## Examples

+-- {: .num_example}
###### Example

Every [[Grothendieck (∞,1)-topos]] is an $(\infty,1)$-pretopos (def. \ref{InfinityPreTopos}).

=--

([Lurie, example A.6.1.5](#Lurie))


+-- {: .num_example }
###### Example

Let $\mathbf{H}$ be a [[Grothendieck (∞,1)-topos]] then the [[full sub-(∞,1)-category]] 

$$
  \mathbf{H}_{coh} \hookrightarrow \mathbf{H}
$$

on the [[coherent objects]] is a local $(\infty,1)$-pretopos (def. \ref{InfinityPreTopos}).

If moreover $\mathbf{H}$ is an [[coherent (∞,1)-topos]], then $\mathbf{H}_{coh}$ is an $(\infty,1)$-pretopos.

=--

([Lurie, prop. A.6.1.6, cor. 6.1.7](#Lurie))



## Related concepts

* [[elementary (∞,1)-topos]]

## References


* {#Lurie} [[Jacob Lurie]], appendix A of _[[Spectral Algebraic Geometry]]_ ([pdf]( http://math.harvard.edu/~lurie/papers/SAG-rootfile.pdf))

