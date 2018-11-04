

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[compactification]] of [[configuration spaces of points]] was introduced in [Fulton-MacPherson 94](#FultonMacPherson94) and an [[operad]]-[[structure]] defined on it by [Getzler-Jones 94](#GetzlerJones94) [Kontsevich 97](#Kontsevich97) spring, now called the _Fulton-MacPherson operad_. This underlies the models of configuration spaces by [[graph complexes]], see there for more.

Observe that the [[configuration space of points|configuration space]] of exactly 2 points in a [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^d$ is [[homotopy equivalence]] to the [[quotient]] by [[group of order two|Z/2]] of a [[n-sphere|(d-1)-sphere]]

$$
  Conf_2( \mathbb{R}^d )
  \;\simeq\;
  S^{d-1}/(\mathbb{Z}/2)
$$

this being the sphere of [[direction of a vector|directions]] of the [[vector]] pointing from one of the two points to the other. This means that the configuration space $Conf_n( \mathbb{R} )$ of $n$ points is [[homotopy equivalent]] to a [[quotient]] by the [[symmetric group]] $\Sigma(n)$ of the [[Cartesian product]] of one such [[n-sphere|(d-1)-sphere]] of [[direction of a vector|directions]] for each [[pair]] of points and various [[open intervals]] encoding the relative [[distance]] between the points.

The _Fulton-MacPherson compactification_ is the evident [[compactification]] of this [[quotient space|quotient]] of [[Cartesian products]] of [[n-sphere|(d-1)-spheres]] with [[open intervals]], replacing the latter by their corresponding [[closed intervals]]. 

This means that a point on the [[boundary]] of the Fulton-MacPherson compactification corresponds to a would-be [[configuration space of points|configuration]] of points where some of the points have formally vanishing [[distance]] to each other, while still remembering a relative [[direction of a vector|direction]] to each other.

In the literature these boundary configurations are often referred to in terms of "infinitesimally close points", but this is loose heuristics and unrelated to actual [[infinitesimal neighbourhoods]] in [[synthetic differential geometry]].

## Definition

For $n, d \in \mathbb{N}$, consider first the [[topological space]] of configurations of _ordered_ [[n-tuples]] of points in the [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^d$, hence the [[mapping space]] of [[injections]]/[[embeddings of topological spaces]]

$$
  Emb( \{1, \cdots, n\}, \mathbb{R}^d )
  \;\subset\;
  \left( 
    \mathbb{R}^d
  \right)^n
  \,.
$$

The [[group]] of [[translation group|translations]] and of [[scale transformations]] [[action|acts]] canonically on $\mathbb{R}^d$ and hence [[diagonal action|diagonally]] on $Emb( \{1, \cdots, n\}, \mathbb{R}^d )$. The resulting [[quotient topological space]]

$$
  Emb( \{1, \cdots, n\}, \mathbb{R}^d )
  \longrightarrow
  Emb( \{1, \cdots, n\}, \mathbb{R}^d )/ \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}
$$

is clearly [[homotopy equivalence|homotopy equivalent]] to the original space.

But now for $n \geq 2$ this quotient space canonically carries the structure of a [[topological manifold]] (in fact of a [[smooth manifold]]) of [[dimension of a manifold|dimension]]

$$
  dim
  \left(
    Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}\right)
  \right)
  \;=\;
  n \cdot d - n - 1
$$

while for $n \leq 1$ the quotient is the [[point space]] (of [[dimension of a manifold|dimension]] 0)

Now for [[pair]] $i \neq j \in \{1, \cdots, n\}$ of distinct consider the [[continuous function]]

$$
  \array{
    Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}right)
  \right)
    &\overset{\theta_{i j}}{\longrightarrow}&
    S^{d-1} \subset \mathbb{R}^d
    \\
    (x_1, \cdots, x_n)
    &\mapsto&
    \frac{
      x_j - x_i
    }{
      {\vert x_j - x_i\vert}
    }
  }
$$

which takes each configuration to the [[direction]] of the [[vector]] between the $i$th and the $j$th point in the configuration.

Moreover, for each [[triple]] $i,j,k$ of mutually distinct labels, consider the [[continuous function]]

$$
  \array{
    Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}\right)
    &\overset{\delta_{i j k}}{\longrightarrow}&
    (0,\infty) \subset [0,\infty]
    \\
    (x_1, \cdots, x_n)
    &\mapsto&
    \frac{ {\vert x_i - x_j\vert} }{ {\vert  x_j - x_k \vert} }
  }
$$

which takes each configuration to the [[ratio]] of the [[distance]] between the $i$th and the $j$th point over that of the $j$th to the $k$th point.

Together these functions induce one total [[continuous function]]

\[
  \label{EmbeddingOfTheOrderedConfigurationSpace}
  \iota
  \;\colon\;
  Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}\right)
  \overset{ (\theta_{i j}, \delta_{i j k}) }{\hookrightarrow}
  \left( S^{d-1} \right)^{ n(n-1) }
  \times [0,\infty]^{ \left(  n(n-1)(n-2) \right) }
\]

from the ordered configuration space into the [[Cartesian product]] of all these [[n-sphere|(d-1)-spheres]] and [[intervals]]. 

A moment of reflection shows that every ordered configuration modulo translation and rescaling, hence every point on the left, may be uniquely reconstructed from its direction vectors and distance ratios, hence from a point on the right, hence that this function is a [[homeomorphism]] onto its [[image]] ([Sinha 03, lemma 3.18](#Sinha03)).

+-- {: .num_defn}
###### Definition

The _Fultan-MacPherson compactification_ of the [[configuration space of points|configuration space]] of ordered [[n-tuples]] of points in the [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^d$ is the [[topological closure]] of the [[image]] of (eq:EmbeddingOfTheOrderedConfigurationSpace):

$$
  FM_n(\mathbb{R}^d)
  \;\coloneqq\;
  \overline{ \iota\left( 
      Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}\right)
  \right) }
$$

=--

(e.g. [Lambrechts-Volic 14, Def. 5.1](#LambrechtsVolic14))

The [[symmetric group]] $\Sigma(n)$ still canonically [[action|acts]] on $FM_n(\mathbb{R}^d)$ and hence the FM-compactification of the actual [[configuration space of points]] $Conf_n(\mathbb{R}^d)$ is the [[quotient space]] $FM_n(\mathbb{R}^d)/\Sigma(n)$.

## Properties

### Relation to the little $n$-disk operad

+-- {: .num_prop #WeakEquivalenceToLittleNDiskOperad}
###### Proposition

The Fulton-MacPherson operad is [[weak equivalence|weakly equivalent]] in the [[model structure on operads]] with respect to the [[classical model structure on topological spaces]], to the [[little n-disk operad]]

=--

([Salvatore 01, Prop. 4.9](#Salvatore01), summarized as [Lambrechts-Volic 14, Prop. 5.6](#LambrechtsVolic14))

### Formality

We have that [[the Fulton-MacPherson operad is formal]] in the sense that for each of its component [[topological spaces]] there is a [[zig-zag]] of [[quasi-isomorphisms]] between their [[de Rham cohomology]] and their [[de Rham complex]], and such that these morphisms are compatible with the induced [[cooperad]]-[[structure]] on both sides.

Concretely, the [[zig-zags]] may be taken to consist of one [[span]] of [[quasi-isomorphisms]] out of a suitable [[graph complex]] to the [[de Rham cohomology]]/[[de Rham complex]] of the [[Fulton-MacPherson operad]].

Here the morphism from the [[graph complex]] to the [[de Rham complex]] of the [[Fulton-MacPherson operad]] regards the latter as the [[compactification]] of a [[configuration space of points]], regards [[functions]]/[[differential forms]] on [[configuration spaces of points]] as [[n-point functions]] of a [[topological quantum field theory|topological]] [[quantum field theory]], regards suitable [[graphs]] as [[Feynman diagrams]] and proceeds by sending each such graph/Feynman diagram to a corresponding [[Feynman amplitude]].

This idea of a proof was sketched in [Kontsevich 99](#Kontsevich99), a full account is due to [Lambrechts-Volic 14](#LambrechtsVolic14).




## Related concepts

* [[little n-disk operad]]

## References

The Fulton-MacPherson [[compactification]] of [[configuration spaces of points]] was first considered in 

* {#FultonMacPherson94} William Fulton, Robert MacPherson, _A compactification of configuration spaces_, Ann. of Math. (2), 139(1):183–225, 1994.

and the [[operad]]-[[structure]] on these compactified spaces was considered in

* {#GetzlerJones94} [[Ezra Getzler]], [[John Jones]], _Operads, homotopy algebra and iterated integrals for double loop spaces_ ([arXiv:hep-th/9403055](https://arxiv.org/abs/hep-th/9403055))

and alternatively in 

* {#Kontsevich99} [[Maxim Kontsevich]], around Def. 12 of _Operads and Motives in Deformation Quantization_, Lett.Math.Phys.48:35-72,1999 ([arXiv:math/9904055](https://arxiv.org/abs/math/9904055))

* {#Kontsevich97} [[Maxim Kontsevich]], section 5.1 of _Deformation quantization of Poisson manifolds, I_, Lett.Math.Phys.66:157-216,2003 ([arXiv:q-alg/9709040](https://arxiv.org/abs/q-alg/9709040))

which was corrected in 

* Giovanni Gaiffi, _Models for real subspace arrangements and stratified manifolds_, Int. Math. Res. Not. 12:627-656, 2003 ([pdf](http://www.dm.unipi.it/~gaiffi/papers/models.pdf))

and developed in detail in 

* {#Sinha03} Dev Sinha, _Manifold theoretic compactifications of configuration spaces_, Selecta Math. (N.S.) 10(3):391-428, 2004 ([arXiv:math/0306385](https://arxiv.org/abs/math/0306385))

which also shows the equivalence to [Fulton-MacPherson 94](#FultonMacPherson94).

The equivalence to the [[little n-disk operad]] was established in 

* {#Salvatore01} Paolo Salvatore, _Configuration spaces with summable labels_, Cohomological methods in homotopy theory. Birkhäuser, Basel, 2001. 375-395.

Review includes

* {#LambrechtsVolic14} [[Pascal Lambrechts]], Ismar Volic, section 5 of _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society ; no. 1079, 2014  ([doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))



[[!redirects Fulton-MacPherson operads]]

[[!redirects Fulton-MacPherson compactification]]
[[!redirects Fulton-MacPherson compactifications]]
