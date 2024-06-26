
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _complex Lie group_ is a [[Lie group]] that is a [[group object]] not just [[internalization|internal]] to [[smooth manifolds]] but in fact to [[complex manifolds]]. Hence it is a [[complex manifold]] $G$ equipped with a [[group]] structure such that both the multiplication map $G \times G \to G$ as well as the [[inverse]] map $G \to G$ are [[holomorphic functions]].

## Properties

### Relation to almost complex structure

One can also consider groups in [[almost complex manifolds]]. But every _almost complex Lie group_ is automatically also a complex Lie group.

### Complexification of compact Lie groups

For $K$ a [[compact Lie group]] there is a unique [[connected topological space|connected]] complex Lie group $G$ such that 

1. the [[Lie algebra]] of $G$ is the [[complexification]] of the Lie algebra of $K$: 

   $$
     Lie(G) \simeq Lie(K) \otimes_{\mathbb{R}} \mathbb{C}
     \,,
   $$

1. $K$ is a [[maximal compact subgroup]] of $G$.

This $G$ is called the **complexification** of $K$.

### Oka property

\begin{prop}\label{CosetSpacesOfComplexLieGroupsAreOkaManifolds}
**([[coset spaces]] of [[complex Lie groups]] are [[Oka manifolds]])** \linebreak
Every [[complex Lie group]] and every [[coset space]] ([[homogeneous space]]) of complex Lie groups is an [[Oka manifold]].
\end{prop}
(review in [Forstnerič & Lárusson 11, p. 9](Oka+manifold#ForstnericLarusson11), [Forstnerič 2013, Thm. 2.6](Oka+manifold#Forstneric13))



## Related concepts

* [[complex Lie algebra]]

* [[relation between compact Lie groups and reductive algebraic groups]]


## References

* [[Dietmar Salamon]], *Notes on complex Lie groups*, 2019 ([pdf](https://people.math.ethz.ch/~salamon/PREPRINTS/cx-lie.pdf), [[Salamon_ComplexLieGroups.pdf:file]])

See also 

* Wikipedia, *[Complex Lie group](https://en.wikipedia.org/wiki/Complex_Lie_group)*

[[!redirects complex Lie groups]]
