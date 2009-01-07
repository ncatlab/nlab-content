#Idea#

A Kan complex is a [[geometric definition of higher category|geometric model]] of an $\infty$-[[infinity-groupoid|groupoid]] based on the [[geometric shapes for higher structures|shape]] modeled by the [[simplex category]].

#Definition#

A _Kan complex_ is a [[simplicial set]] $S$ that satisfies the _Kan condition_, which says that all [[horn|horns]] of the simplicial set have _fillers_, which means that for all diagrams

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


#Remarks#

* Kan complexes are among the most popular models for $\infty$-groupoids.

* Whatever other definition of [[infinity-groupoid]] one considers, it is expected to map to a Kan complex under the [[nerve]].

* A slight weakening of the Kan condition, the _weak Kan condition_ leads to the definition of [[quasi-category]].

* As the above diagrams suggest, Kan complexes are the fibrant objects in one of the [[model structure on simplicial sets|model structures on simplicial sets]].