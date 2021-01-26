+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition
 {#DeterminantLineBundles}

Let $V$ and $W$ be two [[vector space]]s of [[dimension]] $n = dim V = dim W$ and  

$$
  T : V \to W
$$ 

a [[linear map]].

Write $\wedge^n V$ and $\wedge^n W$ for the _top exterior power_ of these vector spaces, the skew-symmetrized $n$th [[tensor algebra|tensor power]] of $V$ and $W$. These are 1-dimensional vector spaces, hence [[lines]] over the [[ground field]]. The linear map $T$ induces a linear map 

$$
  det T \colon \wedge^n V\to \wedge^n W
$$ 

between these lines. This is the **[[determinant]]** of $T$. More specifically, if $V = W$ (being of the same finite dimension, both are necessarily [[isomorphic]] but not necessarily canonically so) then $det T : \wedge^n V \to \wedge^n V$ is a linear [[endomorphism]] of a 1-dimensional vector space and, by the equivalence

$$
  End(\wedge^n V) \simeq k
$$

of such endomorphisms with the [[ground field]] $k$, is identified with an element in $k$

$$
  det T \in k
  \,.
$$

This is the standard meaning of the **determinant** of a linear endomorphism.

Notice that the determinant construction: 

$$
  det : (V \stackrel{T}{\to} W) \mapsto (\wedge^n V \stackrel{det T}{\to} \wedge^n W)
$$ 

is a [[functor]] from the [[category]] [[Vect]] to itself

$$
  det : Vect \to Vect
  \,.
$$

Any such functor $F : Vect \to Vect$ with certain continuity assumptions induces an endo-functor on the category of [[vector bundles]] $VectBund(X)$ over any [[manifold]] $X$. 

Concretely, if a vector bundle $E \to X$ is given by a [[Cech cohomology|Cech cocycle]] 

$$
  \array{
    C(U_i) &\stackrel{(g_{i j})}{\to}& \mathbf{B} GL(n) &\to& Vect
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

with respect to an [[open cover]] $\{U_i \to X\}$ (see [[principal bundle]] and [[associated bundle]] for details), hence by transition functions

$$
  (g_{i j} \in C(U_i \cap U_j, GL(n)))
$$

with values in the [[general linear group]], its image under $det : VectBund(X) \to VectBund(X)$ is the bundle with transition functions the determinants of these transition functions

$$
  (det g_{i j} \in C(U_i \cap U_j, GL(1) \simeq k^\times))
  \,.
$$

This are the transition functions for the bundle $\wedge^\bullet E \to X$ which is fiberwise the top exterior power of $E \to X$. This is the **[[determinant line]] bundle** of $E$.

## Properties

+-- {: .un_prop}
###### Proposition

Let 

$$
 E : X \stackrel{\simeq}{\leftarrow} C(U_i) \stackrel{g_{i j}}{\to} \mathbf{B} U(n)
$$ 

be a [[unitary group]]-[[principal bundle]] (to which is canonically [[associated bundle|associated]] a rank-$n$ [[complex vector bundle]]). Then the single [[characteristic class]]

$$
  [det E] \in H^2(X, \mathbb{Z})
$$

of its determinant [[circle bundle]]

$$
 det E 
  \colon 
  X \stackrel{\simeq}{\leftarrow} C(U_i) \stackrel{det g_{i j}}{\to} \mathbf{B} U(1)
$$ 

is the [[first Chern class]] of $E$

$$
  [det E] = c_1(E)
  \,.
$$

Moreover, if $X$ is a [[smooth manifold]] and $(g_{i j}, A_i)$ is the data of a [[connection on a bundle]] $(E, \nabla)$ on $E$ then $(det g_{i j}, tr A_i)$ (where we take the [[trace]] $tr : \mathfrak{u}(n) \to \mathfrak{u}(1)$ on the [[Lie algebra]] of the [[unitary group]]) is a [[circle n-bundle with connection|line bundle with connection]] that refines the first Chern-class to [[ordinary differential cohomology]]. In other words, this is the image under the refined [[Chern-Weil homomorphism]] of $(E, \nabla)$ induced by the canonical unary [[invariant polynomial]] on $\mathfrak{u}(n)$.

=--

An explicit version of this statement is for instance in ([GriffithsHarris, p. 414](#GriffithsHarris)).

One can now look at operators $T:E\to F$ where $E,F$ are vector bundles of rank $n$ and the induced operators $\Lambda^n T : \Lambda^n E\to \Lambda^n F$ which can be considered as elements $det T\in (\Lambda^n E)^*\otimes\Lambda^n F$. 

Even more important is the case of when $X$ is replaced by an appropriate [[moduli space of connections]], instantons, holomorphic structures or some other objects related to Fredholm operators for which the determinants can be defined. 

## Examples

### Quillen's determinant line bundle

There is a specific version called **Quillen's determinant line bundle** which is certain [[line bundle]] over the [[moduli space of complex structures]] on a fixed smooth vector bundle $E$ over a fixed [[Riemann surface]] $M$. A complex structure on the bundle corresponds to an operator which in local coordinates looks as $D = d\bar{z}(\partial_z+\alpha(z))$ where $\alpha(z)$ is a smooth matrix valued function. The set of such operators is an affine space $\mathcal{A}$ whose underlying vector space is the space of $(0,1)$-End-valued forms $\Omega^{0,1} (End M)$. Then again a determinant is an element of a line $\mathcal{L}_D = \lambda(Ker D)^*\otimes \lambda(Coker D)$ where $\lambda$ is taking the top exterior power. Now one has a family $\mathcal{L}_D$ depending on $D$, which determines a holomorphic line bundle over $\mathcal{A}$. This is the **determinant line bundle**. 

If we had a trivialization of the Quillen's determinant line bundle, then we could identify every section with a holomorphic function on the base space, hence a holomorphic rule giving a number to a Cauchy-Riemann operator. For this one restricts first to the component consisting of the operators with the zero Fredholm index. Next, one considers the corresponding [[Laplace operator]] $D^* D$ and its [[functional determinant]] related to the [[zeta function of an elliptic differential operator]]. (This is related to the [[analytic torsion]]).


### Determinant bundle on the Grassmannian

Let $Gr_k(V)$ be the [[Grassmannian]] of $k$-dimensional subspaces of a finite dimensional vector space $V$. Let $W\subset V$ be a point in $Gr_k(V)$ and $\Lambda^k(W)$ its top exterior power; it is a fiber of the bundle $Det$ over $Gr_k(V)$. The determinant bundle $Det$ has no non-zero holomorphic global sections. Consider its dual $Det^*$ with fiber $\Lambda^k(W)^*$ over $W$. Then the space of of global holomorphic sections $\Gamma_{hol}(Det^*) \cong \Lambda^k(V^*)$. This construction can be suitably extended for the Segal Grassmannian, where $V= V_+\oplus V_-$ is a separable Hilbert space equipped with a polarization, see chapter 7 and especially 7.7 in the Pressley-Segal book listed below.



### Comparing Quillen's and Segal's determinant line bundles

The determinant line bundle of Quillen is in fact related to a variant of Segal's determinant bundle on the "semiinfinite" Grassmannian. Namely one considers instead $Gr_{cpt}(H)$ which is the set (space eventually) of closed supspaces $W\subset H$ where the projection $W\to H_+$ is [[Fredholm operator|Fredholm]] and $W\to H_-$ is [[compact operator|compact]]; then one follows the Segal's prescription to define $Det$ on $Gr_{cpt}(H)$. Notice that $Gr_{cpt}(H)$ is not a homogeneous space. Now there is a span of maps with contractible fibers

$$
Gr_{cpt}(H)\leftarrow \mathcal{B}\to Fred(H_+).
$$
The Quillen's determinant line bundle is defined in general on the whole $Fred(H_+)$ and its pullback to $\mathcal{B}$ is isomorphic to the pullback of the determinant bundle on $Gr_{cpt}(H)$; in fact the Quillen's version can be reconstructed from this pullback by certain quotienting construction. 

### Pfaffian line bundle

In dimens&#238;on $8k+2$ for $k \in \mathbb{N}$ the determinant line bundle has a canon&#238;cal square root line bundle, the [[Pfaffian line bundle]].

### From fermionic path integrals

See at _[[fermionic path integral]]_.

### Relation to theta function

the determinant of the Dirac operator is, up to choice of isomorphism, the [[theta function]]-section of the determinant line bundle ([Freed 87, pages 30-31](#Freed87)).


### Relation to vacuum energy, partition function

See at _[[vacuum energy]]_

## Related concepts

* [[density bundle]]

* [[pseudoscalar]]

* [[theta function]]


[[!include square roots of line bundles - table]]


## References

The relation between determinant line bundles and the first Chern class is stated explicitly for instance on p. 414 of

* Griffiths and Harris, _Principles of algebraic geometry_
 {#GriffithsHarris}

Literature on determinant line bundles of infinite-dimensional bundles includes the following:

* [[Daniel Quillen|D.G. Quillen]], _Determinants of Cauchy-Riemann operators over a Riemann surface_, Funkcionalnii Analiz i ego Prilozhenija __19__ (1985), 37-41, ([pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1334&volume=19&year=1985&issue=1&fpage=37&what=fullt&option_lang=eng) of Russian version).

  reviewed e.g. in 

  Arlo Caine, _Quillen's construction of Determinants of
Cauchy&#8211;Riemann operators over Riemann Surfaces_, 2005 ([pdf](http://web.archive.org/web/20150326122017/http://www.cpp.edu/~jacaine/pdf/quillen_determinant_notes.pdf))

* [[Michael Atiyah]], [[Isadore Singer]], _Dirac operators coupled to vector potentials_, Proc. Nat. Acad. Sci. USA __81__, 2597-2600 (1984) ([pdf](http://www.pnas.org/content/81/8/2597.full.pdf) at pnas site)

* {#Freed87} [[Daniel Freed]], _On determinant line bundles_, Math. aspects of [[string theory]], ed. S. T. Yau, World Sci. Publ. 1987,  ([dg-ga/9505002](http://arxiv.org/abs/dg-ga/9505002), [revised pdf](http://www.math.utexas.edu/~dafr/Index/determinants.pdf))

* [[Jean-Michel Bismut]], [[Daniel Freed]], _The analysis of elliptic families.I. Metrics and connections on determinant bundles_, Comm. Math. Phys. __106__, 1 (1986), 159-176, [euclid](http://projecteuclid.org/euclid.cmp/1104115586), _II. Dirac operators, eta invariants, and the holonomy theorem_, Comm. Math. Phys. __107__, 1 (1986), 103-163. [euclid](http://projecteuclid.org/euclid.cmp/1104115934)

* [[Jean-Michel Bismut]], _Quillen metrics and determinant bundles_, 2 conference lectures in honour of A. N. Tyurin, video at [link](http://www.mathnet.ru/php/presentation.phtml?presentid=62&option_lang=eng)

* A. Pressley, [[Graeme Segal|G. Segal]], _Loop Groups_, Oxford Math. Monographs, 1986. 

* Kenro Furutani, _On the Quillen determinant_, J. Geom. Phys. __49__, 4, 366-375, [math.DG/0309127](http://arxiv.org/abs/math/0309127), [doi](http://dx.doi.org/10.1016/j.geomphys.2003.07.001)

* [[M. Kontsevich]], S. Vishik, _Geometry of determinants of elliptic operators_, in Functional Analysis on the Eve of the 21st Century. 
Vol. I (S. Gindikin, et al., eds.) In honor of the 80th birthday of [[Israel Gel'fand|I.M. Gelfand]]. Birkh&#228;user, Progr. Math. __131__ (1993), 173-197, [pdf](http://193.51.104.7/~maxim/TEXTS/geometry_determinants_12.pdf), [hep-th/9406140](http://arxiv.org/abs/hep-th/9406140)

* [[Robbert Dijkgraaf]], [[Edward Witten|E. Witten]], _Topological gauge theories and group cohomology_, Commun. Math.Phys. __129__, 393--429 (1990), [euclid](http://projecteuclid.org/euclid.cmp/1104180750), [MR1048699](http://www.ams.org/mathscinet-getitem?mr=1048699)

Discussion in the context of the [[modular functor]] is in 

* [[Graeme Segal]], section 6 and section 5 of _The definition of conformal field theory_ , preprint, 1988; also in [[Ulrike Tillmann]] (ed.) _Topology, geometry and quantum field theory_ , London Math. Soc. Lect. Note Ser., Vol. 308. Cambridge University Press, Cambridge (2004) 421-577. ([pdf](https://people.maths.ox.ac.uk/segalg/0521540496txt.pdf)) 

[[!redirects determinant line bundles]]