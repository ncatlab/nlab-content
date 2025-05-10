
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea

For $V$ a [[vector space]] and $r$ a [[cardinal number]] (generally taken to be a [[natural number]]), the **Grassmannian** $Gr(r,V)$ is the space of all  $r$-[[dimension|dimensional]] [[linear subspaces]] of $V$.

## Definition

For $n \in \mathbb{N}$, write $O(n)$ for the [[orthogonal group]] acting on $\mathbb{R}^n$. More generally, say that a [[Euclidean space|Euclidean]] [[vector space]] $V$ is an [[inner product space]] such that there exists a [[linear map|linear]] [[isometry]] $V \overset{\simeq}{\to} \mathbb{R}^n$ to $\mathbb{R}^n$ equipped with its canonical inner product. Then write $O(V)$ for the group of linear isometric [[automorphisms]] of $V$. For the following we regard these groups as [[topological groups]] in the canonical way.

+-- {: .num_defn #RealAndComplexGrassmannian}
###### Definition

For $n, k \in \mathbb{N}$ and $n \leq k$, then the $n$th **Grassmannian** of $\mathbb{R}^k$ is the [[coset]] [[topological space]].

$$
  Gr_n(\mathbb{R}^k) \coloneqq O(k)/(O(n) \times O(k-n))
  \,,
$$

where the [[action]] of the [[product group]] is via its canonical embedding $O(n)\times O(k-n) \hookrightarrow O(k)$.

Generally, for $W \subset V$ an inclusion of [[Euclidean space|Euclidean]] vector spaces, then 

$$
  Gr_W(V) \coloneqq O(V)/(O(W)\times O(V-W))
  \,,
$$

where $V-W$ denotes the [[orthogonal complement]] of $W$ in $V$. 

=--

+-- {: .num_remark}
###### Remark

The group $O(k)$ [[transitive action|acts transitively]] on the set of $n$-dimensional [[linear subspaces]], and given any such, then its [[stabilizer subgroup]] in $O(k)$ is isomorphic to $O(n)\times O(k-n)$. In this way the underlying set of $Gr_n(k)$ is in [[natural bijection]] to the set of $n$-dimensional linear subspaces in $\mathbb{R}^k$. The realization as a [[coset]] as above serves to equip this set naturally with a [[topology|topological space]].

=--


## Properties

### Relation to Stiefel manifolds and universal bundles

Similarly, the _real [[Stiefel manifold]]_ is the [[coset]]

$$
  V_n(k) \coloneqq O(k)/O(k-n)
  \,.
$$

The [[quotient]] [[projection]]

$$
  V_{n}(k)\longrightarrow Gr_n(k)
$$

is an $O(n)$-[[principal bundle]], with [[associated bundle]] $V_n(k)\times_{O(n)} \mathbb{R}^n$ a [[vector bundle]] of [[rank]] $n$. In the limit ([[colimit]]) that $k \to \infty$ is this gives a presentation of the $O(n)$-[[universal principal bundle]] and of the [[universal vector bundle]] of rank $n$, respectively.. The base space $Gr_n(\infty)\simeq_{whe} B O(n)$ is the [[classifying space]] for $O(n)$-[[principal bundles]] and rank $n$ vector bundles.

### CW-complex structure

+-- {: .num_prop #CWComplexStructure}
###### Proposition

The real Grassmannians $Gr_n(\mathbb{R}^k)$ and the complex Grassmannians $Gr_n(\mathbb{C}^k)$ admit the structure of [[CW-complexes]]. Moreover the canonical inclusions

$$
  Gr_n(\mathbb{R}^k)
  \hookrightarrow
  Gr_n(\mathbb{R}^{k+1})
$$

are subcomplex incusion (hence [[relative cell complex]] inclusions).

Accordingly there is an induced CW-complex structure on the [[classifying space]]

$$
  B O(n) \simeq \underset{\longrightarrow}{\lim}_k Gr_n(\mathbb{R}^k)
  \,.
$$

=--

A proof is spelled out in ([Hatcher, section 1.2 (pages 31-34)](#Hatcher)).

\begin{prop}\label{ComplexProjectiveSpaceIsOkaManifold}
**([[complex projective space]] is [[Oka manifold]])** \linebreak
Every [[complex projective space]] $\mathbb{C}P^n$, $n \in \mathbb{N}$, is an [[Oka manifold]]. More generally every [[Grassmannian]] over the [[complex numbers]] is an [[Oka manifold]].
\end{prop}
(review in [Forstnerič & Lárusson 11, p. 9](Oka+manifold#ForstnericLarusson11), [Forstnerič 2013, Ex. 2.7](Oka+manifold#Forstneric13))


## Examples


+-- {: .num_example}
###### Example

The [[Grassmannian]] $Gr_r(\mathbb{R}^{n+1})$ (def. \ref{RealAndComplexGrassmannian}) is

* for $r = 0$: the point;

* for $r = 1$: the [[real projective space]] $\mathbb{R}P^n$;

* for $r = n+1$: the point;

* for $r \gt n+1$: the empty space $\emptyset$.

=--

If $V$ is an [[inner product space]], then the [[orthogonal complement]] defines an [[isomorphism]] between $Gr(r,V)$ and $Gr(\dim V - r,V)$.


## Related concepts

* [[isotropic Grassmannian]]

* [[Lagrangian Grassmannian]], [[affine Grassmannian]]

* [[flag variety]], [[Schubert variety]]

* [[Stiefel manifold]]

* [[coset space]]

* [[projective space]]

* [[classifying space]], [[universal bundle]]


## References

Textbook accounts:

* {#Kochmann96} [[Stanley Kochmann]], section 1.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Hatcher} [[Allen Hatcher]], section 1.2 of _Vector bundles & K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* SL Kleiman, _Geometry on Grassmannians and applications to splitting bundles and smoothing cycles_, Publications Mathématiques de l'IHÉS, 1969, numdam/[pdf](http://www.numdam.org/article/PMIHES_1969__36__281_0.pdf)

* Karin Baur, _Grassmannians and cluster structures_,
Bull. Iranian Math. Soc. 47 (2021) (Suppl 1):S5--S33
[doi](https://doi.org/10.1007/s41980-021-00542-6)

Lecture notes:

* [[Michael Hopkins]], _Grassmannian manifolds_ ([pdf](http://isites.harvard.edu/fs/docs/icb.topic1471353.files/grassmannian.pdf))

See also:

* [[Neil Strickland]], section 5 of: *A Bestiary of Topological Objects* \[<a href="https://strickland1.org/courses/bestiary/bestiary.pdf">pdf</a>, [[Strickland-BestiaryTopological.pdf:file]]\]


category: geometry, algebra

[[!redirects Grassmannians]]


[[!redirects Grassmannian manifold]]
[[!redirects Grassmannian manifolds]]
