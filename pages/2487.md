
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a [[field]] $k$, the **general linear group** $GL(n,k)$ (or $GL_n(k)$) is the [[group]] of [[invertible morphism|invertible]] [[linear maps]] from the [[vector space]] $k^n$ to itself.  It may canonically be identified with the group of $n\times n$ [[matrix|matrices]] with entries in $k$ having nonzero [[determinant]].

### As a topological group
 {#AsAtopologicalGroup}

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


Let $k = \mathbb{R}$ or $= \mathbb{C}$ be the [[real numbers]] or the [[complex numbers]] equipped with their [[Euclidean topology]].

#### Definition

+-- {: .num_defn #GLnAsTopologicalGroup}
###### Definition
**(general linear group as a topological group)**

For $n \in \mathbb{N}$, as a [[topological group]] the _general linear group_ $GL(n, k)$ is defined as follows.

The underlying group is the [[group]] of [[real number|real]] or [[complex numbers|complex]] $n \times n$ [[matrices]] whose [[determinant]] is non-vanishing

$$
  GL(n,k)
  \;\coloneqq\;
  \left(
    A \in Mat_{n \times n}(k)
    \; \vert \;
    det(A) \neq 0
  \right)
$$

with group operation given by [[matrix multiplication]]. 

The [[topological space|topology]] on this set is the [[subspace topology]] as a subset of the [[Euclidean space]] of [[matrices]]
   
$$
  Mat_{n \times n}(k) \simeq k^{(n^2)}
$$

with its [[metric topology]]. 

=--

+-- {: .num_lemma #GLnTopologicalWellDefined}
###### Lemma
**(group operations are continuous)**

Definition \ref{GLnAsTopologicalGroup} is indeed well defined in that the group operations on $GL(n,k)$ are indeed [[continuous functions]] with respect to the given topology.

=--

+-- {: .proof}
###### Proof

Observe that under the identification $Mat_{n \times n}(k) \simeq k^{(n^2)}$ [[matrix multiplication]] is a [[polynomial function]] 

$$
  k^{(n^2)}
   \times
  k^{(n^2)}
   \simeq
  k^{ 2 n^2 }
    \longrightarrow
  k^{(n^2)}
    \simeq
  Mat_{n \times n}(k)
  \,.
$$

Similarly [[inverse matrix|matrix inversion]] is a [[rational function]]. Now [[rational functions are continuous]] on their [[domain]] of definition, 
and since a real matrix is invertible previsely if its determinant is non-vanishing, the domain of definition for matrix inversion is precisely 
$GL(n,k) \subset Mat_{n \times n}(k)$.

=--

+-- {: .num_defn #}
###### Definition
**(stable general linear group)**

The evident [[tower]] of embeddings

$$
  k \hookrightarrow k^2 \hookrightarrow k^3 \hookrightarrow \cdots
$$

induces a corresponding [[tower diagram]] of embedding of the general linear groups (def. \ref{GLnAsTopologicalGroup}) 

$$
  GL(1,k)
    \hookrightarrow
  GL(2,k)
    \hookrightarrow
  GL(3,k)
    \hookrightarrow
  \cdots
  \,.
$$

The [[colimit]] over this [[diagram]] in the [[category]] of [[topological group]] is called the _stable general linear group_ denoted

$$
  GL(k) \;\coloneqq\; \underset{\longrightarrow}{\lim}_n GL(n,k)
  \,.
$$

=--

#### Properties

+-- {: .num_example #AsSubspaceOfTheMappingSpace}
###### Proposition
**(as a [[subspace]] of the [[compact-open topology|mapping space]])

The [[topological space|topology]] induced on the real general linear group when regarded as a [[topological subspace]] of [[Euclidean space]] with its [[metric topology]] 

$$
  GL(n,\mathbb{R})
    \subset
  Mat_{n \times n}(\mathbb{R})
    \simeq
  \mathbb{R}^{(n^2)}
$$

(as in def. \ref{GLnAsTopologicalGroup}) coincides with the topology induced by regarding the general linear group as a [[subspace]] of the [[mapping space]] $Maps(k^n, k^n)$, 

$$
  GL(n,\mathbb{R})
    \subset
  Maps(k^n, k^n)
$$

i.e. the set of all [[continuous functions]] $k^n \to k^n$ equipped with the [[compact-open topology]].

=--

+-- {: .proof}
###### Proof

On the one had, the [[universal property]] of the [[mapping space]] ([this prop.](Introduction+to+Topology+--+1#UniversalPropertyOfMappingSpace)) gives that the inclusion 

$$
  GL(n, \mathbb{R}) \to Maps(\mathbb{R}^n, \mathbb{R}^n)
$$

is a [[continuous function]] for $GL(n,\mathbb{R})$ equipped with the [[Euclidean space|Euclidean]] [[metric topology]], because this is the [[adjunct]] of the defining continuous [[action]] map 

$$
  GL(n, \mathbb{R}) \times \mathbb{R}^n \to \mathbb{R}^n
  \,.
$$ 


This implies that the [[Euclidean space|Euclidean]] [[metric topology]] on $GL(n,\mathbb{R})$ is equal to or [[finer topology|finer]] than the subspace topology coming from $Map(\mathbb{R}^n, \mathbb{R}^n)$. 

We conclude by showing that it is also equal to or [[coarser topology|coarser]], together this then implies the claims. 

Since we are speaking about a subspace topology, we may consider the open subsets of the ambient Euclidean space $Mat_{n \times n}(\mathbb{R}) \simeq \mathbb{R}^{(n^2)}$. Observe that a [[neighborhood base]] of a linear map or matrix $A$ consists of sets of the form 

$$
  U_A^\epsilon
  \;\coloneqq\;
  \left\{B \in Mat_{n \times n}(\mathbb{R}) \,\vert\, \underset{{1 \leq i \leq n}}{\forall}\; |A e_i - B e_i| \lt \epsilon \right\}
$$

for $\epsilon \in (0,\infty)$.

But this is also a [[base for the topology|base]] element for the [[compact-open topology]], namely

$$
  U_A^\epsilon
   \;=\;
  \bigcap_{i = 1}^n V_i^{K_i}
  \,,
$$

where $K_i \coloneqq \{e_i\}$ is a [[singleton]] and $V_i \coloneqq B^\circ_{A e^i}(\epsilon)$ is the [[open ball]] of [[radius]] $\epsilon$ around $A e^i$.

=--

+-- {: .num_prop #ConnectednessOfGeneralLinearGroup}
###### Proposition
**(connectedness properties of the general linear group)**

For all $n \in \mathbb{N}$

1. the complex general linear group $GL(n,\mathbb{C})$ is [[path-connected topological space|path-connected]];

1. the real general linear group $GL(n,\mathbb{R})$ is not [[path-connected topological space|path-connected]].

=--

+-- {: .proof}
###### Proof

First observe that $GL(1,k) = k \setminus \{0\}$ has this property:

1. $\mathbb{C} \setminus \{0\}$ is path-connected,

1. $\mathbb{R} \setminus \{0\} = (-\infty,0) \sqcup (0,\infty)$ is not path connected.

Now for the general case:

1. For $k = \mathbb{C}$: every invertible complex matrix is diagonalizable by a sequence of elementary matrix operations ([this prop.](inverse+matrix#FundamentalTheoremOfLinearAlgebra)). Each of these is clearly path-connected to the identity. Finally the subspace of invertible [[diagonal matrices]] is the [[product topological space]] $\underset{ \{1, \cdots, n\} }{\prod} (\mathbb{C} \setminus \{0\})$ and hence connected (by [this prop.](ProductSpaceOfConnectedSpacesIsConnected), since each factor space is).

1. For $k = \mathbb{R}$: the [[determinant]] function is a [[continuous function]] $GL(n,k) \to \mathbb{R} \setminus \{0\}$, and since the [[codomain]] is not path connected, the domain cannot be either.

=--
   
+-- {: .num_prop #TopologicalGeneralLinearGroup}
###### Proposition
**(compactness properties of the general linear group)**

The [[topological group|topological]] general linear group $GL(n,k)$ (def. \ref{GLnAsTopologicalGroup}) is


1. not [[compact topological space|compact]];

1. [[locally compact topological space|locally compact]];

1. [[paracompact Hausdorff topological space|paracompact Hausdorff]].

=--

+-- {: .proof}
###### Proof

Observe that 

$$
  GL_n(n,k) \subset Mat_{n \times n}(k) \simeq k^{(n^2)}
$$
   
is an [[open subset|open]] [[subspace]], since it is the [[pre-image]] under the [[determinant]] function (which is a [[polynomial]] and hence continuous, as in the proof of lemma \ref{GLnTopologicalWellDefined}) of the of the open subspace $k \setminus \{0\} \subset k$.

As an open subspace of Euclidean space, $GL(n,k)$ is not compact, by the [[Heine-Borel theorem]].

As Euclidean space is Hausdorff, and since every [[subspace]] of a Hausdorff space is again Hausdorff, so $Gl(n,k)$ is Hausdorff.
   
Similarly, as Euclidean space is [[locally compact topological space|locally compact]] and since an open subspace of a locally compact space is again locally compact, it follows that $GL(n,k)$ is locally compact.

From this it follows that $GL(n,k)$ is paracompact, since locally compact topological groups are paracompact ([this prop.](topological+group#ConnectedLocallyCompactTopologicalGroupsAreSigmaCompact)).


=--


### As a Lie group
 {#AsALieGroup}


+-- {: .num_defn}
###### Definition

Since the general linear group as a [[topological group]] (def. \ref{GLnAsTopologicalGroup}) is an  [[open subspace]] of [[Euclidean space]] (proof of prop. \ref{TopologicalGeneralLinearGroup}) it inherits the structure of a [[smooth manifold]] (by [this prop.](differentiable+manifold#OpenSubsetsOfDifferentiableManifoldsAreDifferentiableManifolds)). The group operations (being [[rational functions]]) are [[smooth functions]] with respect to this smooth structure. This is the general linear group $GL(n,\mathbb{R})$ as a _[[Lie group]]_.

=--



### As an algebraic group

This group can be considered as a (quasi-affine) sub[[variety]] of the [[affine scheme|affine space]] $M_{n\times n}(k)$ of square matrices of size $n$ defined by the condition that the [[determinant]] of a matrix is nonzero. It can be also presented as an affine subvariety of the affine space $M_{n \times n}(k) \times k$ defined by the equation $\det(M)t = 1$ (where $M$ varies over the factor $M_{n \times n}(k)$ and $t$ over the factor $k$). 

This [[variety]] is an algebraic $k$-group, and if $k$ is the field of real or complex numbers it is a [[Lie group]] over $k$.

One may in fact consider the set of invertible matrices over an arbitrary unital [[ring]], not necessarily commutative. Thus $GL_n: R\mapsto GL_n(R)$ becomes a [[presheaf]] of [[group]]s on $Aff=Ring^{op}$ where one can take rings either in commutative or in noncommutative sense. In the commutative case, this functor defines a [[group scheme]]; it is in fact the affine group scheme represented by the commutative ring $R = \mathbb{Z}[x_{11}, \ldots, x_{n n}, t]/(det(X)t - 1)$. 

Coordinate rings of general linear groups and of special general linear groups have [[quantum group|quantum deformations]] called [[quantum linear groups]]. 

## Examples

Over [[finite fields]]:

* [[GL(2,3)]]

## Properties

### Representation theory

See at *[[representation theory of the general linear group]]*.

## Related concepts

* [[translation group]], [[affine group]]

* [[Gauss decomposition]], 

* [[special linear group]], [[projective linear group]]

* [[orthogonal group]], [[unitary group]], 

* [[Borel subgroup]], [[flag variety]]

* [[group of units]]

* [[jet group]]

* [[general linear supergroup]], [[quantum linear group]]

## References 

* O.T. O'Meara, _Lectures on Linear Groups_, Amer. Math. Soc., Providence, RI, 1974.

* B. Parshall, J.Wang, _Quantum linear groups_, Mem. Amer. Math. Soc. 89(1991), No. 439, vi+157 pp. 


[[!redirects general linear group]]
[[!redirects general linear groups]]
