

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

Let $f : X \to Y$ be a morphism of [[schemes]]. Write $\Delta : X \to X \times_Y X$ for the [[diagonal]] morphism. 

* The morphism $f$ is called __separated__ if $\Delta(X)$ is a [[closed subspace]] of $X \times_Y X$.

* A [[scheme]] $X$ is called __separated__ if the [[terminal object|terminal]] morphism $X \to \operatorname{Spec} \mathbb{Z}$ is separated.

=--

+-- {: .num_prop}
###### Proposition

Let $X$ be a [[scheme]] (resp. a [[locally noetherian scheme]]),
 $f: X\to Y$ a morphism of schemes (resp. a morphism locally of finite type). The following conditions are equivalent.

1. $f$ is separated.

1. The [[diagonal]] morphism $X\to X\times_Y X$ is [[quasicompact morphism|quasicompact]], and for every affine scheme $Y' = Spec A$ in which $A$ is a [[valuation ring]] (resp. a discrete valuation ring), any two morphisms from $Y'\to X$ which coincide at the generic point of $Y'$ are equal.

1. The diagonal morphism $X\to X\times_Y X$ is quasicompact, and for every affine scheme of the form  $Y' = Spec A$ in which $A$ is a valuation ring (resp. a discrete valuation ring), any two sections of $X' = X(Y')$ which coincide at the generic point of $Y'$ are equal. 

=--

This is the _[[valuative criterion of separatedness]]_. See Hartshorne or [[EGA II]] for more details.

+-- {: .num_remark}
###### Warning

The definition of a separated scheme is formally similar to the definition of a [[Hausdorff space]] which says that the diagonal $\Delta(X) \subseteq X \times X$ is closed; the same pattern is followed in the definition of a [[Hausdorff locale]], [[Hausdorff topos]], etc. More generally, the definition of a separated morphism of schemes is formally similar to e.g. a [[separated geometric morphism]]. This leads to these properties having similar formal properties. Nevertheless, because finite products and pullbacks in these categories do not necessarily agree, these notions of separation also vary. For example, the underlying topological space of a separated scheme is typically not Hausdorff.


=--

## Properties

(...)

## Related concepts


* [[separated geometric morphism]]

* [[Hausdorff topos]], [[Hausdorff topological space]]

category: algebraic geometry

[[!redirects separated morphisms of schemes]]
[[!redirects separated scheme]]
[[!redirects separated schemes]]

[[!redirects locally separated]]
