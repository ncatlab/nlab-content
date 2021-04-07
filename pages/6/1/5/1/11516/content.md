
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In the context of [[topology]], a _topological $G$-space_ (traditionally just _$G$-space_, for short, if the context is clear) is a [[topological space]] equipped with an [[action]] of a [[topological group]] $G$ -- the _[[equivariance group]]_ (usually taken to be the [[topological group]] underlying a [[compact Lie group]], such as a [[finite group]]).

The canonical [[homomorphisms]] of topological $G$-spaces are $G$-[[equivariant function|equivariant]] [[continuous functions]], and the canonical choice of [[homotopies]] between these are $G$-equivariant continuous homotopies (for [[trivial action|trivial]] $G$-[[action]] on the [[interval]]). 

A $G$-[[equivariant Whitehead theorem|equivariant version]] of the [[Whitehead theorem]] says that on [[G-CW complexes]] these $G$-equivariant [[homotopy equivalences]] are equivalently those maps that induce [[weak homotopy equivalences]] on all [[fixed point]] spaces for all [[subgroups]] of $G$ (compact subgroups, if $G$ is allowed to be a [[Lie group]]). 

By [[Elmendorf's theorem]], this, in turn, is equivalent to the [[(∞,1)-presheaves]] over the [[orbit category]] of $G$. See below at _[In topological spaces -- Homotopy theory](#HomotopyTheory)_.

See ([Henriques-Gepner 07](#HenriquesGepner07)) for expression in terms of [[topological groupoids]]/[[orbispaces]].

In the context of [[stable homotopy theory]] the [[stabilization]] of $G$-spaces is given by [[spectra with G-action]]; these lead to [[equivariant stable homotopy theory]]. See there for more details. (But beware that in this context one considers the richer concept of [[G-spectra]], which have a [[forgetful functor]] to [[spectra with G-action]] but better homotopy theoretic properties. ) The union of this as $G$ is allowed to vary is the [[global equivariant stable homotopy theory]].

## Properties

### Change of groups and fixed loci
 {#ChangeOfGroupsAndFixedLoci}

We discuss how any homomorphism of topological groups induces an [[adjoint triple]] of [[functors]] between the corresponding $Topological G Spaces$, and how the cross-composite of this adjoint triple with itself yields the [[fixed locus]]-[[adjunction]]. (See also at [induced representation](induced+representation#GeneralAbtractDefinition) for a formulation in [[homotopy type theory]].)


Throughout, let $G_1, G_2 \in $ [[TopologicalGroups]]
and consider a [[continuous function|continuous]] [[homomorphism]] of [[topological groups]]

\[
  \label{TopologicalGroupHomomorphism}
  \phi
  \;\colon\;
  G_1 
    \longrightarrow
  G_2
  \,.
\]


#### Pullback action

\begin{defn}\label{PullbackAction}
  **(pullback action)** \linebreak
Given a topological group homomorphism $\phi$ (eq:TopologicalGroupHomomorphism), 
write
  $$
    Topological G_1 Spaces
      \overset{
        \;\;\;
        \phi^\ast
        \;\;\;
       }{\longleftarrow}
    Topological G_2 Spaces
  $$

for the [[functor]] which takes a [[topological G-space|topological G2-space]] $(X,\rho)$ to the same underlying [[topological space]] $\rho$, equipped with the $G_1$-action $ \rho(\phi(-))$.

\end{defn}


#### Induced action

(...)

\begin{example}\label{RestrictedAction}
**(restricted action)** \linebreak

(...)

\end{example}

#### Coinduced action
 {#CoinducedActions}

\begin{defn}\label{CoinducedAction}
**(coinduced action)** \linebreak

Given a topological group homomorphism $\phi$ (eq:TopologicalGroupHomomorphism), the _coinduced action_ functor

$$
  Topological G_1 Actions
  \overset{
     Maps(G_2,-)^{G_1}
  }{\longrightarrow}
  Topological G_2 Actions
$$

sends $X \in Topological G_1 Spaces$ 
to the $G_1$-[[fixed locus]] in the [[mapping space]] between [[topological spaces]] equipped with $G_1$-[[actions]] (on $G_2$ the $\phi$-induced left multiplication action) 
and itself equipped with the $G_2$-[[group action|action]] given by

\[
  \label{ActionOnG1EquivariantMapsOutOfG2}
  \array{
    G_2 \times Maps(G_2,X)^{G_1}
    &
      \overset{}{\longrightarrow}
    &
    Maps(G_2,X)^{G_1}
    \\   
    (g_2, h)
    &\mapsto&
    h\big(
      (-) \cdot g_2
    \big)
     \,.
  }
\]
\end{defn}

\begin{example}\label{FixedLociAsCoinducedActions}
**(Fixed loci as coinduced actions)**

Let $H \subset G$ be a topological subgroup and consider the group homomorphism (eq:TopologicalGroupHomomorphism) to be the $H$-[[quotient group]] [[coprojection]] from the [[normal subgroup]] $N(H) \subset G$:

$$
  \phi \coloneqq q \;\colon\; N(H) \longrightarrow N(H)/H
  \,.
$$

Then for any $N(H)$-space $X$ (which in practice will usually be a $G$-space after restriction of its action along $N(H) \hookrightarrow G$, Example \ref{RestrictedAction}) we have that its coinduced action (Def. \ref{CoinducedAction}) is its $H$-[[fixed locus]] $X^H$ equipped with its residual $N(H)$-action:

$$
  Maps
  \big(
    N(H)/H,
    X
  \big)^{N(H)}
  \;\;
  \simeq
  \;\;
   X^H
  \,.
$$

\end{example}


\begin{prop}\label{CoinducedActionIsRightAdjointToPullbackAction}
**(coinduced action is right adjoint to pullback action)** \linebreak 

Given a topological group homomorphism $\phi$ (eq:TopologicalGroupHomomorphism), 
the pullback action functor (Def. \ref{PullbackAction}) is the [[left adjoint]] and the coinduced action functor (Def. \ref{CoinducedAction}) is the [[right adjoint]] in a pair of [[adjoint functors]]

$$
  G_1 Spaces
  \underoverset
    {
      \underset{
        Maps
        \big(
          G_2, -
        \big)^{G_1}
      }{\longrightarrow}
    }
    {
      \overset{
         \phi^\ast
      }{
         \longleftarrow
      }
    }
    {\bot}
  G_2 Spaces
$$

\end{prop}

\begin{proof}

To see the defining [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism), consider a $G_1$-[[equivariant function|equivariant]] [[continuous function]]

$$
  \phi^\ast X
  \overset{
    \;\;\;
    f
    \;\;\;
  }{
    \longrightarrow
  }
  Y
  \,.
$$

From this we obtain the following function

$$
  \array{
    X 
    &
      \overset{
        \tilde f
      }{
        \longrightarrow 
      }
    &
    Maps
    \big(
      G_2,
      Y
    \big)^{G_1}
    \\
    x
    &\mapsto&
    \big(
      g_2
      \mapsto
      f( g_2 \cdot x )
    \big)
    \,,
  }
$$

where $e \in G_2$ denotes the [[neutral element]].

This is manifestly:

* well-defined, due to the $G_1$-equivariance of $f$;

* continuous, being built from composition of continuous map;

* $G_2$-equivariant with respect to the action (eq:ActionOnG1EquivariantMapsOutOfG2).

Conversely, given a $G_2$-equivariant continuous function $X \overset{\tilde f}{\longrightarrow} Maps\big(G_2, Y\big)^{G_1}$, we obtain the following function

$$
  \array{
    \phi^\ast X 
    &\overset{}{\longrightarrow}&
    Y
    \\
    x
    &\mapsto&
     \tilde f(x)(e)
    \,.
  }
$$

This is:

* continuous, being the composition of continuous functions;

* $G_1$-equivariant due to the equivariance properties of $\tilde f$:

  $$
    \begin{aligned}
      \phi(g_1) \cdot x
      & \mapsto
      \tilde f
      \big( 
        \phi(g_1)\cdot x
      \big) 
      (e)
      \\
      & = 
      \tilde f
      ( 
        x
      ) 
      \big(
         e \cdot \phi(g_1)
      \big)
      \\
      & =
      \tilde f
      ( 
        x
      ) 
      \big(
         \phi(g_1)
         \cdot 
         e
      \big)
      \\
      & =
      g_1
        \cdot
      \big(
      \tilde f
      ( 
        x
      ) 
      (
         e
      )
      \big)
    \end{aligned} 
  $$

Finally, it is clear that these transformations $f \leftrightarrow \tilde f$ are [[natural transformation|natural]], hence it only remains to see that they are [[bijective]]:

Plugging in the above constructions we find indeed:

$$
 \widetilde 
  {\tilde f}
  \;\colon\;
  x \mapsto f(e \cdot x) = f(x)
$$

and

$$
  \widetilde {\widetilde {\tilde f}}
  \;\colon\;
  x 
  \mapsto 
  \big(
    g_2 
      \mapsto 
    \underset{
        {= \tilde f(x)(e \cdot g_2)}    
        \atop
        {= \tilde f(x)(g_2)}
    }{
      \underbrace{
        \tilde f(g_2\cdot x)(e)
      }
    }
  \big)
  \,.
$$

\end{proof}


#### Fixed loci

(...)


### Equivariant Tietze extension theorem

See at _[[equivariant Tietze extension theorem]]_

### Model structure and homotopy theory
 {#ModelStructureAndHomotopyTheory}

The standard [[homotopy theory]] on $G$-spaces used in [[equivariant homotopy theory]] considers [[weak equivalences]] which are [[weak homotopy equivalence]] on all (ordinary) [[fixed point]] spaces for all suitable [[subgroups]]. By [[Elmendorf's theorem]], this is equivalent to [[(∞,1)-presheaves]] over the [[orbit category]] of $G$.

On the other hand there is also the standard homotopy theory of [[infinity-actions]], presented by the [[Borel model structure]], in this context also called the "coarse" or "naive" equivariant model structure ([Guillou](#Guillou)).


## Examples
  {#Examples}

We discuss some classes of examples of [[G-spaces]].

### Euclidean $G$-spaces
 {#EuclideanGSpace}

Let $V \in RO(G)$ be an [[orthogonal group|orthogonal]] [[linear representation]] of a [[finite group]] $G$ on a [[real vector space]] $V$.
Then the underlying [[Euclidean space]] $\mathbb{R}^V$ inherits the [[mathematical structure|structure]] of a [[G-space]]

\begin{xymatrix}
   \mathbb{R}^V\ar@(ul,ur)^G
\end{xymatrix}

We may call this the _[[Euclidean G-space]]_ associated with the linear representation $V$.


### Representation spheres


Let $V \in RO(G)$ be an [[orthogonal group|orthogonal]] [[linear representation]] of a [[finite group]] $G$ on a [[real vector space]] $V$.
Then the [[one-point compactification]] of the underlying [[Euclidean space]] $\mathbb{R}^V$ inherits the [[mathematical structure|structure]] of a [[G-space]] with the [[one-point compactification|point at infinity]] a [[fixed point]]. This is called the _$V$-[[representation sphere]]_

\begin{xymatrix}
   S^V\ar@(ul,ur)^G
   \ar@{}[r]|-{:=}
   &
   \big( \mathbb{R}^V\ar@(ul,ur)^G\big)^{\mathrm{cpt}}
\end{xymatrix}


### Representation tori

Let $V \in RO(G)$ be an [[orthogonal group|orthogonal]] [[linear representation]] of a [[finite group]] $G$ on a [[real vector space]] $V$.

If $G$ is the [[point group]] of a [[crystallographic group]] inside the [[Euclidean group]] 

$$
  N \rtimes G
  \hookrightarrow
  Iso(\mathbb{R}^V)
$$

then the $G$-[[action]] on the Euclidean space $\mathbb{R}^V$ descends to the [[quotient]] by the [[action]] of the translational [[normal subgroup]] [[lattice in a vector space|lattice]] $N$ ([this Prop.](crystallographic+group#InducedPointGroupActionOnTorus)). The resulting $G$-space is an [[n-torus]] with $G$-action, which might be called the _[[representation torus]]_ of $V$

\begin{xymatrix}
   \mathbb{R}^V\ar@(ul,ur)^G
   \ar@{}[r]|-{:=}
   &
   \big( \mathbb{R}^V\ar@(ul,ur)^G\big)/N
\end{xymatrix}

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=13">
<img src="https://ncatlab.org/schreiber/files/ExamplesOfLinearRepsAndInducedGSpaces.jpg" width="690">
</a>
</center>

> graphics grabbed from [SS 19](equivariant+Hopf+degree+theorem#SatiSchreiber19)


### Projective $G$-space


Let $G$ be a [[finite group]] (or maybe a [[compact Lie group]]) and let $V$ be a $G$-[[linear representation]] over some [[topological field|topological]] [[ground field]] $k$.

Then the corresponding _[[projective G-space]]_ is the [[quotient space]] of the [[complement]] of the origin in (the [[Euclidean space]] underlying) $V$ by the given [[action]] of the [[group of units]] of $k$ (from the $k$-[[vector space]]-[[mathematical structure|structure]] on $V$):

$$
  k P(V)
  \;:=\;
  \big(
    V \setminus \{0\}
  \big) / k^\times
$$

and equipped with the residual $G$-[[action]] on $V$ (which passes to the [[quotient space]] since it commutes with the $k$-action, by linearity).


### G-CW complexes

See at _[[G-CW complex]]_.


## Related concepts

* [[G-set]], [[G-manifold]]

* [[fixed point space]]

* [[slice theorem]]

* [[equivariant bundle]]

* [[cyclotomic space]]

[[!include equivariant homotopy theory -- table]]

See also

* [[rational topological G-space]]

* [[equivariant rational homotopy theory]]

  [[vector G-space]]

* [[equivariant stable homotopy theory]]

* [[equivariant rational stable homotopy theory]]


## References

* {#Bredon72} [[Glen Bredon]], chapter II of: _[[Introduction to compact transformation groups]]_, Academic Press  1972


* [[Tammo tom Dieck]], Chapter 8 in: _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766, Springer 1979 ([doi:10.1007/BFb0085965](https://link.springer.com/book/10.1007/BFb0085965))

* {#Guillou} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_ ([pdf](https://faculty.math.illinois.edu/~bertg/EquivModels.pdf), [[GuillouModelsForEquivariantHomotopyTheory.pdf:file]])

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))


See also the references at _[[equivariant homotopy theory]]_.


[[!redirects topological G-spaces]]
[[!redirects topological G-spaces]]

[[!redirects G-space]]
[[!redirects G-spaces]]


[[!redirects TopologicalGActions]]

[[!redirects TopologicalGSpaces]]


