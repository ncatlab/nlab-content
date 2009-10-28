#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A Kan complex is a [[geometric definition of higher category|geometric model]] of an $\infty$-[[infinity-groupoid|groupoid]] based on the [[geometric shapes for higher structures|shape]] modeled by the [[simplex category]].

#Definition#

A _Kan complex_ is a [[simplicial set]] $S$ that satisfies the _Kan condition_, 

* which says that all [[horn|horns]] of the simplicial set have _fillers_,

* which means equivalently that the unique morphism $S \to pt$ from $S$ to the [[point]] is a [[Kan fibration]], 

* which means equivalently that for all diagrams

  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && 
    \\
    \Delta[n] 
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
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& 
    \\
    \Delta[n] 
  }
  \,.
  $$

* This in turn means equivalently that the map from $n$-simplices to $(n,i)$-horns is an [[epimorphism]]
$$
  [\Delta[n], S] \to\gt [\Lambda^i[n],S]
  \,.
$$

  In this last form the Kan condition is useful 
  for defining [[internalization|internal]] Kan 
  complexes: for instance a _smooth Kan complex_ can 
  be defined as a simplicial object in [[Diff]] 
  such that the morphisms
  $
    [\Delta[n], S] \to [\Lambda^i[n],S]
  $
  are _surjective submersions_.



#Remarks#


* Kan complexes are among the most convenient and popular models for [[∞-groupoids]]. The horn filling condition from this point of view is read as guaranteeing that

  * for all collection of $(n-1)$ composable $n$-cells (a horn $\Lambda^k[n]$) there exists an $n$-cell -- their _composite_ -- and an $(n-1)$-cell connecting the original $(n-1)$ $n$-cells with their composite. Depending on $k$, this interpretation in terms of composition implies that one thinks of all cells as being reversible. Therefore this models an [[∞-groupoid]].

  For illustrations of the horn-filler conditions see [[Kan fibration]].


* Whatever other definition of [[∞-groupoid]] one considers, it is expected to map to a Kan complex under the [[nerve]].

* A slight weakening of the Kan condition, the _weak Kan condition_ leads to the definition of [[quasi-category]].

* Kan complexes are the fibrant objects in the [[model structure on simplicial sets|model structures on simplicial sets]] for which fibrations are [[Kan fibration|Kan fibrations]].

  In this context, a weak equivalence between Kan complexes is a morphism of simplicial sets that induces an [[isomorphism]] on the [[simplicial homotopy groups]] of the two Kan complexes.

#Examples#

## Kan complexes from nerves of $n$-groupoids ##

+-- {: .un_prop}
###### Proposition

The [[nerve]] $N(C)$ of a [[small category]] 
is a Kan complex if and only if $C$ is a [[groupoid]].

=--

The existence of [[nLab:inverse|inverse]] morphisms in $D$ corresponds to the fact that in the [[Kan complex]] $N(D)$ the "outer" [[horns]]

$$
  \array{
    && d_0
    \\
    & && \searrow^{f}
    \\
    d_1 &&\stackrel{Id_{d_1}}{\to} && d_1
  }
  \;\;\; 
  \;\;\; 
  and
  \;\;\; 
  \;\;\; 
  \array{
    && d_1
    \\
    & {}^f\nearrow &&     
    \\
    d_0 &&\stackrel{Id_{d_0}}{\to} && d_0
  }
$$

have fillers 

$$
  \array{
    && d_0
    \\
    & {}^{f^{-1}}\nearrow&& \searrow^{f}
    \\
    d_1 &&\stackrel{Id_{d_1}}{\to} && d_1
  }
  \;\;\; 
  \;\;\; 
  and
  \;\;\; 
  \;\;\; 
  \array{
    && d_1
    \\
    & {}^f\nearrow && \searrow^{f^{-1}}
    \\
    d_0 &&\stackrel{Id_{d_0}}{\to} && d_0
  }
$$

(even unique fillers, due to the properties of the [[nerve]] of an ordinary category).

This is one way to see and motivate that a simplicial set that is a [[Kan complex]] but which does not necessarily have unique fillers makes models an [[∞-groupoid]].

Accordingly

+-- {: .un_prop}
###### Proposition

The [[nerve]] $N(C)$ of a [[strict ∞-category]] 
is a Kan complex if and only if $C$ is a [[strict ∞-groupoid]].

=--


## singular simplicial complexes / fundamental $\infty$-groupoids ##

For $X$ a [[topological space]], its _singular simplicial complex_ is the [[simplicial set]] $\Pi(X)$ (often denoted  $S(X)$) whose set of $n$-simplices is the [[hom-set]]

$$
  \Pi(X)_n := Top(\Delta^n_{Top}, X)
$$

in [[Top]] of continuous maps from the standard topological $n$-simplex $\Delta^n_{Top}$ into $X$.

Using the fact that the $\Delta^n_{Top}$ arrange themselves into a [[simplicial object|cosimplicial space]]

$$
  \Delta_{Top} : \Delta \to Top
$$

in the obvious way, the $(\Pi(X)_n)$ become a [[simplicial set]] in the corresponding obvious way. For instance the face maps are induced by restricting maps to $X$ along the face inclusions $\delta^i : \Delta^{n-1} \hookrightarrow \Delta^n$.

That $\Pi(X)$ is indeed a Kan complex is intuitively clear. Technically it follows from the fact that the inclusions ${{\Lambda^n}_{Top}}_k \hookrightarrow \Delta^n_{Top}$ of topological horns into topological simplices are 
[[retracts]], in that there are continuous maps $\Delta^n_{Top} \to {{\Lambda^n}_{Top}}_k$ given by "squashing" a topological $n$-simplex onto parts of its boundary, such that
$$
  ({{\Lambda^n}_{Top}}_k \to \Delta^n_{Top} \to
  {{\Lambda^n}_{Top}}_k)
  =
  Id
  \,.
$$
Therefore the map
$[\Delta^n, \Pi(X)] \to [\Lambda^n_k,\Pi(X)]$ is an epimorphism, since it is equal to 
to $Top(\Delta^n, X) \to Top(\Lambda^n_k, X)$ which has a right inverse $Top(\Lambda^n_k, X) \to Top(\Delta^n, X)$.


The [[∞-groupoid]] represented by the Kan complex $\Pi(X)$ is called the [[fundamental ∞-groupoid]] of $X$.

This example is the universal one: up to [[model structure on simplicial sets|weak equivalence of Kan complexes]] every Kan complex is the fundamental $\infty$-groupoid of a (compactly generated, weakly Hausdorff) [[topological space]].


This is the statement of the [[homotopy hypothesis]] (which is a theorem for $\infty$-groupoids modeled as Kan complexes.

[[!redirects Kan complexes]]