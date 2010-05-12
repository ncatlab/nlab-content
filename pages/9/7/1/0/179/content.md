

<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

**$\infty$-Lie algebroids** are to [[∞-Lie groupoids]] as [[Lie algebras]] are to [[Lie groups]]. 

* [[Lie group]] - [[Lie algebra]]

* [[Lie groupoid]] - [[Lie algebroid]]

* [[∞-group|∞-Lie group]] - [[L-infinity-algebra|∞-Lie algebra]]

* [[∞-Lie groupoid]] - **$\infty$-Lie algebroid** .

In terms of [[synthetic differential geometry]] an $\infty$-Lie algebroid may be thought of as an [[∞-Lie groupoid]] all whose [[k-morphism]]-spaces over a given object are [[infinitesimal space]]s.

Since in typical [[Models for Smooth Infinitesimal Analysis|convenient models for synthetic differential geometry]] these infinitesimal spaces are represented by formal [[duality]] in terms of their [[smooth algebra]]s of functions, it follows that when [[∞-groupoid]]s are incarnated as [[simplicial object|simplicial]] [[smooth space]]s, an $\infty$-Lie algebroid

$$
  \mathfrak{a} = \left(
     \cdots \mathfrak{a}_2
     \stackrel{\to}{\stackrel{\to}{\to}} \mathfrak{a}_1 \stackrel{\to}{\to} \mathfrak{a}_0
  \right)
$$ 

may be modeled by [[cosimplicial algebra|cosimplicial]] [[smooth algebra]]s  

$$
  C^\infty(\mathfrak{a}) = \left(
     \cdots C^\infty(\mathfrak{a}_2)
     \stackrel{\leftarrow}{\stackrel{\leftarrow}{\leftarrow}} 
     C^\infty(\mathfrak{a}_1)
     \stackrel{\leftarrow}{\leftarrow} 
     C^\infty(\mathfrak{a}_0)
  \right)
  \,.
$$ 

Under the [[monoidal Dold-Kan correspondence]], these map by the [[Moore complex|normalized cochain complex functor]] $N$ to cochain [[dg-algebra]]s in non-negative degree:

$$
  CE(\mathfrak{a}) := N C^\infty(\mathfrak{a})
  \,.
$$

This dg-algebra is usefully thought of as the [[Chevalley-Eilenberg algebra]] of the $\infty$-Lie algebroid. If $\mathfrak{a} = \mathfrak{g}$ is an ordinary [[Lie algebra]], then this is indeed the ordinary Chevalley-Eilenberg algebra of that Lie algebra. 

In the literature on [[Lie algebroid]]s, however, $CE(\mathfrak{a})$ often goes by different names, such as "canonical complex" or "the complex that computes Lie algebroid cohomology". In the literature on what we here identify as $\infty$-Lie algebroids, the algebras $CE(\mathfrak{a})$ are often thought of as algebras of functions on [[NQ-supermanifold]]s.

Accordingly, there is a bit of room for different approaches of how to define the [[(∞,1)-category]] of [[∞-Lie algebroid]]s. A very general abstract [[nPOV]] perspective proceeds via the notion of [[rational homotopy theory in an (∞,1)-topos]]: here the [[(∞,1)-topos]] $\mathbf{H}$ of the given notion of [[∞-Lie groupoid]]s is taken to be equipped with a specific line-object $R$, and the [[(∞,1)-category]] $\mathbf{L}$ of [[∞-Lie algebroid]]s is the [[reflective (∞,1)-subcategory]] that [[localization of an (∞,1)-category|localize]] $\mathbf{H}$ at those morphism that induce [[isomorphism]]s in the $R$-[[cohomology]] internal to $\mathbf{H}$

$$
  \mathbf{L} \stackrel{\leftarrow}{\hookrightarrow}
  \mathbf{H}
  \,.
$$

In the case that $\mathbf{H} = Sh_{(\infty,1)}(C)$ is the [[(∞,1)-category of (∞,1)-sheaves]] on a [[site]] $C$ like the [[opposite category]] $Alg_{\mathbb{R}}^{op}$ of commutative (and suitably "small") [[algebra]]s, or the site $C = \mathbb{L}$ of [[smooth loci]], the opposite $C^\infty Alg^{op}$ of (suitably small) [[smooth algebra]], the line object may be taken to be the [[real number|real line]] in the corresponding in ternal incarnation, and one finds then that 

$$
  \mathbf{L} \simeq ([\Delta, C^\infty Alg]^op)^\circ
$$

is the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by the the opposite of the [[model structure on cosimplicial rings|model structure on cosimplicial commutative (smooth) algebras]]. 

At least for the underlying plain algebras this is equivalent, by the [[monoidal Dold-Kan correspondence]], to the $(\infty,1)$-category presented by the opposite of the standard [[model structure on dg-algebras]] $(dgAlg^{op})^\circ$, for graded commutative cochain dg-algebras in non-negative degree. This is of course the category in which much of classical [[rational homotopy theory]] takes place, and indeed it has been noticed that much of classical rational homotopy theory may be understood as being about $\infty$-Lie theory. Notably the [[Sullivan construction]] of a [[topological space]] from a [[dg-algebra]] may be thought of as essentially being the [[Lie integration]] of the $\infty$-Lie algebroid corresponding to the dg-algebra to an [[∞-groupoid]]. This can straightforwardly be refined to an integration to an [[∞-Lie groupoid]].



## Special Cases

* a $\infty$-Lie algebroid over the [[point]], $\mathfrak{a} = *$ is an **[[L-∞-algebra]]**;

* an $n$-[[truncated]] $\infty$-Lie algebroid is a **Lie $n$-algebroid**;

* an $\infty$-Lie algebroid the differential of whose [[Chevalley-Eilenberg algebra]] is "co-binary", i.e. $d : \mathfrak{a}^* \to a^* \oplus a^* \wedge g^*$, is **strict**.

So in particular

* a 1-Lie algebroid is a **[[Lie algebroid]]**;

* a 1-Lie algebroid over the point is a **[[Lie algebra]]**;

* a Lie $n$-algebroid over a point is a **[[Lie n-algebra]]**.

* a _[[BRST-complex]]_ is the [[Chevalley-Eilenberg algebra]]
  of an action-$\infty$-Lie algebroid of the 
  [[action]] of an $L_\infty$-algebra, see [[Lie ∞-algebroid representation]];

  more generally, the complexes appearing in [[BV-BRST formalism]] are 
  derived $\infty$-Lie algebroids, whose Chevalley-Eilenberg algebra may have generators in negative degree.

* a [[Courant algebroid]] is a certain Lie 2-algebroid.

* more  generally an [[n-symplectic manifold]] is a Lie $n$-algebroid.

* Standard examples of [[exterior differential system]]s are [[Chevalley?Eilenberg algebras]] of $L_\infty$-algebroids.


## Examples

### Tangent Lie algebroid

The following example is in a way the archetypical example on which all others are modeled in a sense.

For $X$ any [[smooth manifold]], there is a standard notion of the [[Lie algebroid]] which is the [[tangent Lie algebroid]] of $X$. As an $\infty$-Lie algebroid, this is the [[simplicial object|simplicial]] [[smooth locus]] given by the [[infinitesimal singular simplicial complex]] 

$$
  T X = 
  \left(
      \cdots 
      X^{(\Delta^2_{inf})} 
        \stackrel{\to}{\stackrel{\to}{\to}} 
        X^{(\Delta^1_{inf})} 
       \stackrel{\to}{\to} X
  \right)
$$

of $X$. By the central observation on combinatorial [[differential forms in synthetic differential geometry]] by [[Anders Kock]], the [[Chevalley-Eilenberg algebra]] of this is indeed isomorphic to the [[de Rham complex]] of $X$:

$$
  CE(T X) := N C^\infty(T X) \simeq (\Omega^\bullet(X), d_{dR})
  \,.
$$

For more details on the computations involved see [Spaces of infinitesimal k-simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl) at [[infinitesimal object]].

In particular for $X = \mathbb{R}^n$ a [[Cartesian space]], we have

$$
  T \mathbb{R}^n
  =
  \left(
      \cdots 
      \mathbb{R}^n \times \tilde D(2,n)
        \stackrel{\to}{\stackrel{\to}{\to}} 
        \mathbb{R}^n \times \tilde D(1,n)
       \stackrel{\to}{\to} 
       \mathbb{R}^n
  \right)   
  \,,
$$

where $\tilde D(k,n)$ is the [[smooth locus]] of [infinitesimal k-simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl) based at the origin in $\mathbb{R}^n$.

### Ordinary Lie algebras


Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$. We describe how $\mathfrak{g}$ looks when regarded as a special case of an $\infty$-Lie algebroid.

Write 

$$
  \mathbf{B}G =
  \left(
     \cdots G \times G 
     \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} * 
  \right)
$$

for the [[delooping]] [[groupoid]] of $G$, regarded as an an [[∞-Lie groupoid]] modeled by a simplicial [[smooth space]].

We claim that a morphism 

$$
  \omega : T U \to \mathbf{B}G
$$

from the tangent Lie algebroid of some $U \in $ [[CartSp]] is [[groupoid of Lie-algebra valued forms|flat Lie-algebra valued form]] and how that can be used to find the [[Lie algebra]] $\mathfrak{g}$ as the infinitesimal sub-$\infty$-groupoid

$$
  \mathbf{b}\mathfrak{g} \hookrightarrow \mathbf{B}G
$$

inside $\mathbf{B}G$.

Since $\mathbf{B}G$ is [[simplicial skeleton|2-coskeletal]] (being the [[nerve]] of a [[groupoid]]) a morphism $T U \to \mathbf{B}G$ is fixed already under its 2-[[truncated|truncation]]

$$
  \array{
    U \times \tilde D(2,n) 
     &\stackrel{\omega_2}{\to}& 
    G \times G
    \\
    \downarrow \downarrow \downarrow && 
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    \\
    U \times \tilde D(1,n) &\stackrel{\omega_1}{\to}& G
    \\
    \downarrow \downarrow && \downarrow \downarrow
    \\
    U &\to& *
  }
  \,.
$$

It is clear that $\omega_1$ factors through the inclusion $\tilde D(1,dim(G)) \hookrightarrow G$ that sends the unique point of $\tilde D(1, dim(G))$ to the neutral element (by respect for the degeneracy maps).
Then from that one finds that $\omega_2$ factors through the inclusion $\tilde D(2, dim(G)) \hookrightarrow G \times G$ that sends the unique point of $\tilde D(2,dim(G))$ to $(e,e) \in G \times G$. And evidently these two factorizations are universal, in that every other factorization will uniquelyy factor through these

$$
  \array{
    U \times \tilde D(2,n) 
     &\stackrel{\omega_2}{\to}& 
    \tilde D(2,dim(G))
    &\hookrightarrow&
    G \times G
    \\
    \downarrow \downarrow \downarrow 
     && 
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    &&
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    \\
    U \times \tilde D(1,n) 
    &\stackrel{\omega_1}{\to}& 
    \tilde D(1, dim(G))
    &\hookrightarrow&
    G
    \\
    \downarrow \downarrow 
    && \downarrow \downarrow
    && \downarrow \downarrow
    \\
    U &\to& * &\to& *
  }
  \,.
$$



## References

The term "Lie $\infty$-algebroid" or "$L_\infty$-algebroid" as such is not as yet established in the literature, as most authors working with these objects think of them entirely in terms of [[dg-algebra]]s or [[NQ-supermanifolds]] and either ignore the relation to [[Lie theory]] or take it more or less for granted. 

Possibly the first explicit appearance of the idea of $\infty$-Lie algebroids recognized in their full [[Lie theory|Lie theoretic]] meaning is

* [[Pavol ?evera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080))

which uses "[[NQ-supermanifolds]]". Of course, as this article also points out, in hindsight one finds that much of this is already implicit in the much older theory of [[Sullivan model|Sullivan models]] in [[rational homotopy theory]], which is concerned with modelling _spaces_ by qDGCAs. That these spaces can be regarded as [[∞-groupoids]] and as [[Lie ∞-groupoids]] in particular is clear in hindsight, but was possibly first explicitly realized in the above reference. See also [[Lie integration]].

[[!redirects L-infinity-algebroid]]
[[!redirects L-infinity algebroid]]
[[!redirects L-infinity Lie algebroid]]

[[!redirects L-∞-algebroid]]
[[!redirects L-∞ algebroid]]
[[!redirects L-∞ Lie algebroid]]


[[!redirects Lie-∞-algebroid]]
[[!redirects Lie-∞-algebroids]]
[[!redirects Lie-∞ algebroid]]
[[!redirects Lie-∞ algebroids]]
[[!redirects Lie ∞-algebroid]]
[[!redirects Lie ∞-algebroids]]
[[!redirects L-infinity-algebroids]]
[[!redirects L-infinity algebroids]]
[[!redirects L-infinity Lie algebroids]]

[[!redirects ∞-Lie algebroid]]
[[!redirects ∞-Lie algebroids]]