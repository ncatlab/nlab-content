
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea

Given a [[site]] $\mathcal{S}$, then a _local epimorphism_ is a [[morphism]] in the [[category of presheaves]] over the site which becomes an [[epimorphism]] under [[sheafification]].

More abstractly, for $\mathcal{S}$ a [[small category]], one says axiomatically that a system of _local epimorphisms_ is a system of [[morphisms]] in the [[presheaf]] category $[S^{op}, Set]$ that has the closure properties expected of [[epimorphisms]] under [[composition]] and under [[pullback]].

There is then a unique [[Grothendieck topology]] on $\mathcal{S}$ that induces this system of local epimorphism, see _[Relation to sieves](#RelationToSieves)_ below.

Moreover the [[local isomorphisms]] among the local epimorphisms admit a [[calculus of fractions]] which equips the [[category of presheaves]] with the structure of a [[category with weak equivalences]]. The corresponding [[reflective localization]] is the [[category of sheaves]] on the site $\mathcal{S}$.

## Definition

+-- {: .num_defn #SystemOfLocalEpimorphisms}
###### Definition
**(system of local epimorphisms)**

Let $\mathcal{S}$ be a [[small category]]. A _system of local epimorphisms_ on the [[presheaf category]] $[\mathcal{S}^{op}, Set]$ is a [[class]] of [[morphisms]] satisfying the following axioms:

**LE1** every [[epimorphism]] in $[\mathcal{S}^{op}, Set]$ is a local epimorphism;

**LE2** the [[composition|composite]] of two local epimorphisms is a local epimorphism;

**LE3** if the [[composition|composite]] $A_1 \stackrel{u}{\to} A_2 \stackrel{v}{\to} A_3$ is a local epimorphism, then so is $v$;

**LE4** a morphism $u \colon A \to B$ is a local epimorphism precisely if for all $U \in \mathcal{S}$ (regarded as a [[representable presheaf]]) and morphisms $y: U \to B$, the [[pullback]] morphism $A \times_B U \to U$ is a local epimorphism.

=--

## Properties

### Relation to sieves
 {#RelationToSieves}

The specification of a system of local epimorphisms is equivalent to a system of [[Grothendieck topology|Grothendieck covering]] [[sieves]].

To see this, translate between local epimorphisms to sieves as follows.

Throughout, let $\mathcal{S}$ be a [[small category]]. Write $[\mathcal{S}^{op}, Set]$ for its [[category of presheaves]] and write

$$
  y \;\colon\; \mathcal{S} \longrightarrow [\mathcal{S}^{op}, Set]
$$ 

for the [[Yoneda embedding]].


+-- {: .num_defn #LocalEpimorphismFromGrothendieckTopology}
###### Definition
**(local epimorphisms from [[Grothendieck topology]])**

Let the [[small category]] $\mathcal{S}$ be equipped with a [[Grothendieck topology]].

For $U \in \mathcal{S}$ an object in the site, a [[morphism]] of [[presheaves]] into the corresponding [[representable presheaf|represented presheaf]]

$$ 
  A \overset{f}{\longrightarrow} y(U) 
  \;\;\;
  \in [\mathcal{S}^{op}, Set]
$$ 

is a _local epimorphism_ if the [[sieve]]

$$
  sieve_A \subset y(U) \in [S^{op}, Set]
$$ 

at $U$ which assigns to $V$ all morphisms from $V$ to $U$ that factor through $f$

$$
  sieve_f 
    \;\colon\; 
  V 
   \;\mapsto\;
  \left\{  V \overset{g}{\to} U \,\in \mathcal{S} 
      \;\Big\vert\; 
      \array{
        && A
        \\
        & {}^{\mathllap{\exists}}\nearrow & \Big\downarrow{}^{f}
        \\
        y(V) & \underset{y(g)}{\longrightarrow} & y(U)
      }
  \right\}
$$

is a [[covering sieve]].

A general morphism of presheaves

$$
  A \overset{}{\longrightarrow} B \;\;\; \in [\mathcal{S}^{op}, Set]
$$ 

is a _local epimorphism_ if for every $U \in \mathcal{S}$ and 
every $y(U) \to B$ the [[projection]] morphism  $y(U) \times_{B} A \overset{p_1}{\to} y(V)$ out of the [[pullback]]/[[fiber product]] 

$$
  \array{
    y(U)\times_{B} A
      &\overset{}{\longrightarrow}&
    A
    \\
    {}^{\mathllap{p_1}}\Big\downarrow 
    &{}^{(pb)}& \Big\downarrow{}^{\mathrlap{f}}
    \\
    y(U) &\underset{}{\longrightarrow}& B
  }
$$

is a local epimorphism as above. By the [[universal property]] of the [[fiber product]], this means equivalently that

$$
  sieve_f 
    \;\colon\; 
  V 
   \;\mapsto\;
  \left\{  V \overset{g}{\to} U \,\in \mathcal{S} 
      \;\Big\vert\; 
      \array{
        y(V) &\overset{\exists}{\longrightarrow}& A
        \\
        {}^{\mathllap{g}}\Big\downarrow & & \Big\downarrow{}^{f}
        \\
        y(U) & \underset{}{\longrightarrow} & B
      }
  \right\}
$$

is a [[covering sieve]].

=--

+-- {: .num_remark #InTermsOfCoverages}
###### Remark
**(in terms of [[coverages]])**

If instead of a [[Grothendieck topology]] we are just given a [[coverage]], then Def. \ref{LocalEpimorphismFromGrothendieckTopology} becomes:

$$
  A \overset{f}{\longrightarrow} B
  \;\;\; \in
  [\mathcal{S}^{op}, Set]
$$

is a local epimorphism, if for all $y(U) \longrightarrow B$ there is a [[covering]] $\{ V_i \overset{\iota_i}{\longrightarrow} U \}$ in the coverage, such that for each $i$ there exists a lift

$$
  \array{
    y(V_i) &\overset{\exists}{\longrightarrow}& A
    \\
    {}^{\mathllap{\iota_i}}\Big\downarrow & & \Big\downarrow{}^{f}
    \\
    y(U) & \underset{}{\longrightarrow} & B
  }
$$

=--

+-- {: .num_defn #GrothendieckTopologyFromLocalEpimorphisms}
###### Definition
**(Grothendieck topology from local epimorphisms)**

Conversely, assume a system of local epimorphisms as in Def. \ref{SystemOfLocalEpimorphisms} is given. 

Declare a [[sieve]] $F$ at $U$ to be a [[covering sieve]] precisely if the inclusion morphism $F \hookrightarrow U$ is a local epimorphism. Then this defines a [[Grothendieck topology]] encoded by the collection of local epimorphisms.

=--


### Relation to simplicial presheaves

+-- {: .num_prop #CechNerveProjectionOfLocalEpimorphismIsLocalWeakEquivalence}
###### Proposition
**([[Cech nerve]] [[projection]] of [[local epimorphism]] is [[local weak equivalence]])**

For $\mathcal{S}$ a [[site]], let 

$$
  A \overset{f}{\longrightarrow} B
  \;\colon\;
  [\mathcal{S}^{op}, Set]
$$ 

be a local epimorphism (Def. \ref{LocalEpimorphismFromGrothendieckTopology}). Then the projection 

$$
  C(f) \longrightarrow B
  \;\;\;\;
  \in [\mathcal{S}^{op}, sSet]
$$

out of the [[Cech nerve]] [[simplicial presheaf]]

$$
  C(f)_k \;\coloneqq\; 
  \underset{
     k \; \text{factors}
  }{
  \underbrace{
    A \times_B \cdots \times_B A
  }}
$$

is a [[weak equivalence]] in the projective local [[model structure on simplicial presheaves]] $[\mathcal{S}^{op}, sSet_{Qu}]_{proj,loc}$.


=--


([Dugger-Hollander-Isaksen 02, corollary A.3](#DuggerHollanderIsaksen02))

$\,$

## References

* Kashiwara-Schapira,  section 16 of _[[Categories and Sheaves]]_

* {#MacLaneMoerdijk} [[Saunders Mac Lane]], [[Ieke Moerdijk]], chapter III, section 8 of _[[Sheaves in Geometry and Logic]], Springer 1992

* {#DuggerHollanderIsaksen02} [[Daniel Dugger]], [[Sharon Hollander]], [[Daniel Isaksen]], _Hypercovers and simplicial presheaves_, Mathematical Proceedings of the Cambridge Philosophical Society. Vol. 136. No. 1. Cambridge University Press, 2004 ([arXiv:math/0205027](https://arxiv.org/abs/math/0205027))

[[!redirects local epimorphisms]]
[[!redirects local epi]]
[[!redirects local epis]]

[[!redirects generalized cover]]
[[!redirects generalized covers]]
