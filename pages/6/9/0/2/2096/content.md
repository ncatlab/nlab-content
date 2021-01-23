
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea

Two [[differentiable functions]] $f \colon X \to Z$ and $g \colon Y \to Z$ between [[differentiable manifolds]] are called _transversal_ if, roughly, the [[images]] of $X$ and $Y$ in $Z$ do not "touch tangentially".

If $f$ or $g$ are inclusions of (possibly [[immersion|immersed]]) [[submanifolds]] one speaks of these submanifolds being transversal to each other.

## Definition 

Two [[differentiable functions]] $f \colon X \to Z$ and $g \colon Y \to Z$ between  [[differentiable manifold]] (for instance [[smooth functions]] between [[smooth manifolds]]) are __transversal__ if for all point $x \in X$ and $y \in Y$ with $f(x) = z = g(y)$ the [[differentials]] of $f$ and $g$ in these points [[linear span|span]] the entire [[tangent space]] at $z$ in the sense that

$$
  im(d f) + im(d g) \simeq T_z Z
  \,.
$$

(Notice that this is not required to be a [[direct sum]].) 

## Examples

* A [[submersion]] is transversal to all differentiable functions into its [[codomain]].



## Properties

### Pullbacks along transversal maps

Various constructions involving [[pullbacks]] of [[differentiable manifolds]] work as expected only for pullbacks involving transversal maps. 

For example, two [[differentiable functions]] with a common [[codomain]] are transversal only if their [[pullback]] exists and is preserved by the [[tangent bundle]] [[functor]]; that is, $T(X \times_Z Y) = T X \times_{T Z} T Y$.  (However, the pullback may exist and be preserved without transversality; for example if $X$ and $Y$ are both abstract [[points]], $Z$ is *not* a point, and the maps $X, Y \to Z$ are equal as concrete points of $Z$.)

This is to be regarded as the dual of the possibly more familiar statement that various constructions involving [[quotient object|quotient]]s only work as expected for _free_ [[actions]].

Both of these "problems" are solved by passing from the ordinary [[1-category]] [[Diff]] of manifolds to a suitable [[higher category theory|higher category]] of [[generalized smooth spaces]].

More precisely: 

* the problem with the [[pushouts]] (quotients) is resolved by passing to [[stacks]] and [[smooth infinity-stacks]].

* the problem with the [[pullbacks]] is resolved by passing to [[derived stacks]]. Concretely for the case of manifolds this is discussed at _[[derived smooth manifold]]_.


### Thom's transversality theorem

See at _[[Thom's transversality theorem]]_.

## Related concepts

* [[regular value]]

## References

* {#Kosinski93} [[Antoni Kosinski]], chapter IV.1 of _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))


* T. Br&#246;cker, K. J&#228;nich, C. B. Thomas, M. J. Thomas, _Introduction to differentiable topology_, 1982 (translated from German 1973 edition; &#8707; also 1990 German 2nd edition)

* Morris W. Hirsch, _Differential topology_, Springer GTM 33, [gBooks](http://books.google.com/books/about/?id=iSvnvOodWl8C)


[[!redirects transversal map]]
[[!redirects transversal maps]]
[[!redirects transverse map]]
[[!redirects transverse maps]]

[[!redirects transversality]]
