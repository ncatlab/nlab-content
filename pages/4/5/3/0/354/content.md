#Idea#

A Kan complex is a [[geometric definition of higher category|geometric model]] of an $\infty$-[[infinity-groupoid|groupoid]] based on the [[geometric shapes for higher structures|shape]] modeled by the [[simplex category]].

#Definition#

A _Kan complex_ is a [[simplicial set]] $S$ that satisfies the _Kan condition_, which says that all [[horn|horns]] of the simplicial set have _fillers_, which means that the unique morphism $S \to pt$ is a [[Kan fibration]], which means for all diagrams

$$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& pt
  }
$$

there exists a diagonal morphism

$$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \,.
$$

This in turn means that the map from $n$-simplices to $(n,i)$-horns is an [[epimorphism]]
$$
  [\Delta[n], S] \to\gt [\Lambda^i[n],S]
  \,.
$$

In this form the Kan condition is useful for defining [[internal category|internal]] Kan complexes: for instance a _smooth Kan complex_ can be defined as a simplicial object in [[Diff]] such that the morphisms
$
  [\Delta[n], S] \to [\Lambda^i[n],S]
$
are _surjective submersions_.

#Remarks#

* Kan complexes are among the most popular models for [[infinity-groupoid|infinity-groupoids]]. The horn filling condition from this point of view is read as guaranteeing that

  * for all collection of $(n-1)$ composable $n$-cells (a horn $\Lambda^k[n]$) there exists an $n$-cell -- their _composite_ -- and an $(n-1)$-cell connecting the original $(n-1)$ $n$-cells with their composite. Depending on $k$, this interpretation in terms of composition implies that one thinks of all cells as being reversible. Therefore this models an [[infinity-groupoid]].

* Whatever other definition of [[infinity-groupoid]] one considers, it is expected to map to a Kan complex under the [[nerve]].

* A slight weakening of the Kan condition, the _weak Kan condition_ leads to the definition of [[quasi-category]].

* Kan complexes are the fibrant objects in the [[model structure on simplicial sets|model structures on simplicial sets]] for which fibrations are [[Kan fibration|Kan fibrations]].