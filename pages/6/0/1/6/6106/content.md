
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The [[loop space]] of a [[topological group]] $G$ inherits the structure of a [[group]] under pointwise group multiplication of [[loops]]. This is called a _loop group_ of $G$. 

(Notice that this is a group structure in addition to the [[infinity-group]]-structure of any [[loop space]] under _composition_ of loops.)

If $G$ is a [[Lie group]], then there is a smooth version of the loop group consisting of [[smooth functions]] $S^1 \to G$. By the discussion at [[manifold structure of mapping spaces]] the collection of such smooth maps is itself an [[infinite-dimensional smooth manifold]] and so the smooth loop group of a Lie group is an [[infinite-dimensional Lie group]]. 

Among all [[infinite-dimensional Lie groups]], loop groups are a most well behaved class. In particular their [[representation theory]] is similar to that of [[compact Lie groups]].

Some of these nice properties are solely due to the [[circle]] $S^1$ being a [[compact manifold]]. For $X$ any other compact manifold there is similarly an infinite-dimensional Lie group $[X,G]$ of smooth functions $X \to G$ under pointwise multiplication in $G$.

Such mapping groups appear in [[physics]] notably as groups of [[gauge transformations]] over a [[spacetime]]/[[worldvolume]] $X$. Accordingly, loop groups play a prominint role in 1- and 2-dimensional [[quantum field theory]], notably the [[WZW model]] describing the propagation of a [[string]] on $G$. The _[[current algebras]]_ ([[affine algebras]]) which arise as [[Lie algebras]] of ([[central extension|centrally extended]]) loop groups derive their name from this relation to physics. Accordingly, as for [[compact Lie groups]], the [[representation theory]] of loop groups is naturally understood in terms of their [[geometric quantization]] (by a loop variant of the [[orbit method]]).

On the other hand, for $X$ of [[dimension]] greater that 1 there are very few known results about the properties of the mapping group $[X,G]$. 
 
## Properties

### Lie algebra

Let $G$ be a [[compact Lie group]]. Write $\mathfrak{g}$
for its [[Lie algebra]].

+-- {: .num_prop }
###### Proposition

The [[Lie algebra]] of $L G$ is the [[loop Lie algebra]]

$$
  Lie(L G) \simeq L Lie(G) = L \mathfrak{g}
  \,.
$$

=--

### Complexification

Let $G$ be a [[compact Lie group]].

+-- {: .num_prop }
###### Proposition

The [[complexification of a Lie group|complexification]] of $L G$ is the loop group of the complexification of $G$


$$
  (L G)_{\mathbb{C}}
  \simeq
  L (G_\mathbb{C})
  \,.
$$

=--

### Central extensions

Loop groups of [[compact space|compact]] [[Lie groups]] have canonical [[central extensions]], often called _Kac-Moody central extensions_ . A detailed discussion is in ([Pressley & Segal](#PressleySegal)). A review is in ([BCSS](#BCSS))

### Representations
 {#Representations}

#### Positive energy

Write 

$$
  t_\theta \colon L G \to L G
$$

for the [[automorphism]] which rotates loops by an [[angle]] $\theta$. 

The corresponding [[semidirect product group]] we write $L G \rtimes S^1$

+-- {: .num_defn }
###### Definition

Let $V$ be a [[topological vector space]]. A linear representation

$$
  S^1 \to Aut(V)
$$

of the [[circle group]] is called **positive** if $\exp(i \theta)$ acts by $\exp(i A \theta)$ where $A \in End(V)$ is a [[linear operator]] with positive [[spectrum of an operator|spectrum]].

A linear [[representation]] 

$$
  \rho : L G \to Aut(V)
$$

is said to have **positive energy** or to be a **[[positive energy representation]]** if it extends to a representation of the [[semidirect product group]] $L G \rtimes S^1$ such that the restriction to $S^1$ is positive.

=--

#### By geometric quantization (looped orbit method)
 {#ByGeometricQuantization}

We discuss the [[quantization of loop groups]] in the sense of [[geometric quantization]] of their canonical [[prequantum bundle]].

Let $G$ be a [[compact Lie group]].
Let $T \hookrightarrow G$ be the inclusion of a [[maximal torus]]. There is a [[fiber sequence]]

$$
  \array{
    G/T &\to& L G / T
    \\
    && \downarrow
    \\
    && L G / G & \simeq \Omega G
  }
  \,.
$$

+-- {: .num_remark }
###### Remark

By the discussion at _[[orbit method]]_, if $G$ is a [[semisimple Lie group]], then $G/T$ is isomorphic to the [[coadjoint orbit]] of an element $\langle \lambda , -\rangle \in \mathfrak{g}^*$ for which $T \simeq G_\lambda$ is the [[stabilizer subgroup]].

If moreover $G$ is [[simply connected topological space|simply connected]], then the [[weight lattice]] $\Gamma_{wt} \subset \mathfrak{t}^* \simeq \mathfrak{t}$ of the Lie group $G$ is [[isomorphism|isomorphic]] to the group of [[group characters]]

$$
  \Gamma_{wt} \stackrel{\simeq}{\to} Hom_{LieGrp}(G,U(1))
  \,.
$$


=--

+-- {: .num_prop #RepsFromGeometricQuantization}
###### Proposition

The [[irreducible representation|irreducible]] [[projective representation|projective]] [[positive energy representations]] of $L G$ correspond precisley to the possible [[geometric quantizations]] of $L G / T$ (as in the [[orbit method]]). 

More in detail:

The degree-2 [[integral cohomology]] of $L G / T$ is

$$
  H^2(L G / T) \simeq \mathbb{Z} \oplus H^2(G / T, \mathbb{Z}) \simeq \mathbb{Z} \oplus \hat T
  \,.
$$

Writing $L_{n,\lambda}$ for the corresponding [[complex line bundle]] with level $n \in \mathbb{Z}$ and weight $\lambda \in \hat T$ we have that 

1. the space of [[holomorphic sections]] of $L_{n,\lambda}$ is either zero or is an irreducible positive energy representation;

1. every such arises this way;

1. and is non-zero precisely if $(n,\lambda)$ is positive  in the sense that for each positive [[coroot]] $h_\alpha$ of $G$

   $$
     0 \leq \lambda(h_\alpha) \leq n \langle h_\alpha, h_\alpha\rangle
    \,.
   $$

=--

This appears for instance as ([Segal, prop. 4.2](#Segal)).


### Relation to equivariant elliptic cohomology
 {#RelationToEquivariantEllipticCohomology}


Under mild conditions (but over the complex numbers) the representation ring of a loop group $L G$ is equivalent to the $G$-[[equivariant elliptic cohomology]] (see there for more) of the point ([Ando 00, theorem 10.10](#Ando00)).

This is a higher analog of how $G$-[[equivariant K-theory]] of the point gives the [[representation ring]] of $G$.

## Related concepts

* [[Kac-Moody group]]

* [[Verlinde ring]]

* [[string group]]

* [[caloron correspondence]]

* [[equivariant elliptic cohomology]]

* [[Kac character formula]]

* [[Kac-Weyl character]]

* [[double loop group]]

## References

The standard textbook on loop groups is

* {#PressleySegal} [[Andrew Pressley]], [[Graeme Segal]], _Loop groups_, Oxford University Press (1988) &lbrack;[ISBN:9780198535614](https://global.oup.com/academic/product/loop-groups-9780198535614)&rbrack;
  

A review talk is 

* {#Segal} [[Graeme Segal]], _Loop groups_ ([pdf](http://people.mpim-bonn.mpg.de/zagier/files/doi/10.1007/BFb0084581/chapter08.pdf))
 

A review of some aspects with an eye towards loop groups as part of the [[crossed module]] of groups representing a [[string 2-group]] is in

* {#BCSS05} [[John Baez]], [[Alissa Crans]], [[Urs Schreiber]], [[Danny Stevenson]], _From loop groups to 2-groups_, Homology Homotopy Appl. Volume 9, Number 2 (2007), 101-135. ([arXiv:math/0504123](https://arxiv.org/abs/math/0504123))

The relation between [[representations]] of loop groups and [[twisted K-theory]] over the group is the topic of

* [[Dan Freed]], [[Mike Hopkins]], [[Constantin Teleman]], _[[Loop Groups and Twisted K-Theory]]

The relation between representations of loop groups an [[equivariant elliptic cohomology]] of the point is discussed in

* {#Ando00} [[Matthew Ando]], _Power operations in elliptic cohomology and representations of loop groups_ Transactions of the American
Mathematical Society 352, 2000, pp. 5619-5666. ([JSTOR](http://www.jstor.org/stable/221905), [pdf](http://www.math.uiuc.edu/~mando/papers/POECLG/poeclg.pdf))

Discussion with respect to [[flag varieties]] is in 

* {#Kumar02} [[Shrawan Kumar]], _Kac-Moody Groups, their Flag Varieties and Representation Theory_, Birkh&#228;user 2002

[[!redirects loop group]]
[[!redirects loop groups]]

[[!redirects loop group representation]]
[[!redirects loop group representations]]

[[!redirects Kac-Moody central extension]]
[[!redirects Kac-Moody central extensions]]

[[!redirects Kac-Moody loop group]]
[[!redirects Kac-Moody loop groups]]
