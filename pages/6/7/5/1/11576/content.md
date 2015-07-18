
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In a [[cohesive (∞,1)-topos]] $\mathbf{H}$, the canonical [[natural transformation]]

$$
  \flat \to \Pi
$$

from the [[flat modality]] to the [[shape modality]] may be thought of as sending "points to the pieces in which they sit".

## Definition and basic properties

Notice the existence of the following canonical [[natural transformations]] induced from the structure of a cohesive topos (a special case of the construction at _[[unity of opposites]]_).

+-- {: .num_defn #TransformationFromPointsToPieces}
###### Definition

Given a [[cohesive topos]] $\mathcal{E}$ with ($&#643; \dashv \flat$) its ([[shape modality]] $\dashv$ [[flat modality]])-[[adjunction]] of def. \ref{AdjointTriple}, then the [[natural transformation]]

$$
  \flat X \longrightarrow X \longrightarrow &#643; X 
$$

(given by the [[composition]] of the $\flat$-[[counit of a comonad|counit]] followed by the $&#643;$-[[unit of a monad|unit]]) may be called the transformation **from points to their pieces** or the **points-to-pieces-transformation**, for short.

=--

+-- {: .num_remark }
###### Remark

The $(f^\ast \dashv f_\ast)$-[[adjunct]] of the transformation from pieces to points, def. \ref{TransformationFromPointsToPieces},

$$
  \flat X \longrightarrow X \longrightarrow &#643; X
$$

is (by the rule of forming right [[adjuncts]] by first applying the [[right adjoint]] functor and then precomposing with the [[unit of an adjunction|unit]] and by the fact that the [[adjunct]] of a [[unit of an adjunction|unit]] is the [[identity]]) the map

$$
  (f_\ast X \longrightarrow f_! X)
  \coloneqq
  \left(
  f_\ast X \longrightarrow f_\ast f^\ast f_! X \stackrel{\simeq}{\longrightarrow} f_!X
  \right)
  \,.
$$

Observe that going backwards by applying $f^\ast$ to this and postcomposing with the $(f^\ast \dashv f_\ast)$-[[counit of an adjunction|counit]] is equivalent to just applying $f^\ast$, since by [[idempotent monad|idempotency]] of $\flat$ the counit is an [[isomorphism]] on the [[discrete object]] $f^\ast f_! X$. Therefore the points-to-pieces transformation and its adjunct are related by

$$
  \left(
    \flat X \longrightarrow X \longrightarrow &#643; X
  \right)
  = 
  f^\ast \left(
    f_\ast X \longrightarrow f_! X
  \right).
$$

Observe then finally that since $f^\ast$ is a [[full and faithful functor|full and faithful]] [[left adjoint|left]] and [[right adjoint]], the points-to-pieces transform is an [[epimorphism]]/[[isomorphism]]/[[monomorphism]] precisely if its [[adjunct]] $f_\ast X \longrightarrow f_! X$ is, respectively.

=--

## Relation to Aufhebung of the initial opposition
 {#RelationToAufhebung}

For a cohesive 1-topos, if the pieces-to-points transform is an [[epimorphism]] then there is [[Aufhebung]] of the initial opposition $(\emptyset \dashv \ast)$ in that $\sharp \emptyset \simeq \emptyset$ ([Lawvere-Menni 15, lemma 4.1](#LawvereMenni15)). Conversely, if the [[base topos]] is a [[Boolean topos]], then this Aufhebung implies that the pieces-to-points transform is epi ([Lawvere-Menni 15, lemma 4.2](#LawvereMenni15)).

## Examples

### Bundle equivalence and concordance
 {#BundleEquivalenceAndConcordance}

Given an [[∞-group]] $G$ in a [[cohesive (∞,1)-topos]] $\mathbf{H}$, with [[delooping]] $\mathbf{B}G$, then for any other object $X$ the [[∞-groupoid]] $\mathbf{H}(X,\mathbf{B}G)$ is that of $G$-[[principal ∞-bundles]] with [[equivalences]] between them. Alternatively one may form the [[internal hom]] $[X,\mathbf{B}G]$. Applying the [[shape modality]] to this yields the $\infty$-groupoid $\mathbf{H}^\infty(X,\mathbf{B}G) \coloneqq  &#643; [X,\mathbf{B}G]$ of $G$-principal $\infty$-bundles and [[concordances]] between them. Alternatively, the [[flat modality]] applied to the internal hom is again just the external hom $\flat [X,\mathbf{B}G] \simeq \mathbf{H}(X,\mathbf{B}G)$.

In conclusion, in this situation the points-to-pieces transform is the canonical map

$$
  \mathbf{H}(X,\mathbf{B}G) \longrightarrow \mathbf{H}^\infty(X,\mathbf{B}G)
$$

from $G$-principal $\infty$-bundles with bundle equivalences between them, to $G$-principal $\infty$-bundles with concordances between them.


### In tangent cohesion: the differential cohomology diagram

In a [[tangent cohesive (∞,1)-topos]] on [[stable homotopy types]] the points-to-pieces transform is one stage in a natural hexagonal [[long exact sequence]], the _[[differential cohomology diagram]]_. See there for more.

### Comparison map between algebraic and topological K-theory

Applied to [[stable homotopy types]] in $Stab(\mathbf{H}) \hookrightarrow T\mathbf{H}$ the [[tangent cohesive (∞,1)-topos]] which arise from a [[symmetric monoidal (∞,1)-category]] $V \in CMon_\infty(Cat_\infty(\mathbf{H}))$ [[internal (∞,1)-category|internal]] to $\mathbf{H}$ under internal [[algebraic K-theory of a symmetric monoidal (∞,1)-category]], the points-to-pieces transform interprets as the [[comparison map between algebraic and topological K-theory]]. See there for more


### In infinitesimal cohesion

In [[infinitesimal cohesion]] the points-to-pieces transform in an [[equivalence]].

## Related concepts

[[!include cohesion - table]]

## References

* {#LawvereMenni15} [[William Lawvere]], [[Matías Menni]], _Internal choice holds in the discrete part of any cohesive topos satisfying stable connected codiscreteness_, Theory and Applications of Categories, Vol. 30, 2015, No. 26, pp 909-932. ([TAC](http://www.tac.mta.ca/tac/volumes/30/26/30-26abs.html))

[[!redirects points-to-pieces transforms]]

[[!redirects points-to-pieces transformation]]
[[!redirects points-to-pieces transformations]]


[[!redirects points-to-pieces-transformation]]
[[!redirects points-to-pieces-transformations]]

[[!redirects points-to-pieces-transform]]
[[!redirects points-to-pieces-transforms]]
