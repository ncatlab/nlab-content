
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

When [[symplectic geometry]] is used to model [[mechanics]] in [[physics]], then a [[symplectic manifold]] $(X,\omega)$ encodes the [[phase space]] of a [[mechanical system]] and a [[symplectomorphism]] 

$$
  \phi \;\colon\; (X_1,\omega_1) \to (X_2, \omega_2)
$$ 

encodes a process undergone by this system, for instance the time evolution induced by a [[Hamiltonian vector field]]. 

Now the [[graph]] of a [[symplectomorphism]] $\phi$ is a [[Lagrangian submanifold]] of the [[Cartesian product]] space $X_1 \times X_2$ regarded as a [[symplectic manifold]] with symplectic form $p_1^\ast \omega_1 - p_2^\ast \omega_2$. In other words, a symplectomorphism $\phi$ as above constitutes a [[Lagrangian correspondence]] between $(X_1,\omega_1)$ and $(X_2, \omega_2)$. See for instance ([Cattaneo-Mnev-Reshetikhin 12](#CattaneoMnevReshetikhin12)) for a review.

This suggests that instead of the [[category]] whose [[objects]] are [[symplectic manifolds]] and whose [[morphisms]] are [[symplectomorphisms]], one might consider a kind of [[category of correspondences]] whose objects are symplectic manifolds, and whose morphisms include [[Lagrangian correspondences]], so that [[composition]] is given by forming the [[fiber product]] along adjacent legs of [[correspondences]].

[[Alan Weinstein]] called this would-be category the _symplectic category_ and suggested that it is the natural [[domain]] for [[geometric quantization]].

However, take at face value, symplectic manifolds with [[Lagrangian correspondences]] between them do not quite form a [[category]], since the usual [[composition]] is only well-defined when the intersection of $L_1 \times L_2 \cap X_1 \times \Delta(X_2) \times X_3$ is [transverse](http://ncatlab.org/nlab/show/transversal+maps).

Proposals for how to rectify this are in ([Wehrheim-Woodward](#WehrheimWoodward)) and in ([Kitchloo](#Kitchloo)) (by turning this into an [[(infinity,1)-category]]).

## Refinements

### Prequantum correspondences
 {#PrequantumCorrespondences}

A refinement of the symplectic category to [[prequantum geometry]] is the following (see [S 13](#SyntheticQFT)).

Write $\mathbf{B}U(1)_{conn}$ for the [[moduli stack]] of smooth [[circle group]]-[[principal connections]]. Write [[Smooth∞Grpd]] for the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoids]], and $Smooth\infty Grpd_{/\mathbf{B}U(1)_{conn}}$ for the corresponding [[slice (∞,1)-topos]]. Finally write

$$
  Corr_1(Smooth\infty Grpd,\mathbf{B}U(1)_{conn})
$$

for the [[(∞,1)-category of correspondences]] in $Smooth\infty Grpd_{/\mathbf{B}U(1)_{conn}}$.

An object in here is a [[prequantum geometry]] $(X,\nabla)$ given by a map

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{\nabla}}

    \\
    \mathbf{B}U(1)_{conn}
  }
  \,.
$$

Under the [[curvature]] map $F_{(-)} \colon \mathbf{B}U(1)_{conn} \to \Omega^2_{cl}$ this maps to a [[presymplectic structure]]

$$
  (X,\omega) = (X, F_{\nabla})
  \,.
$$

If here $\omega$ is non-degenerate, this is a symplectic structure as in Weinstein's symplectic category.

Moreover, a [[morphism]] $(X_1,\nabla_1) \to (X_2,\nabla_2)$ is a [[diagram]] of the form

$$
  \array{
    && Z
    \\
    & {}^{\mathllap{i_1}}\swarrow && \searrow^{\mathrlap{i_2}}
    \\
    X_1
    && \swArrow_{\eta} &&
    X_2
    \\
    & {}_{\mathllap{\nabla_1}}\searrow && \swarrow_{\mathrlap{\nabla_2}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \,,
$$

hence a [[correspondence]] space (smooth $\infty$-groupoid) $Z$ over $X$ and $Y$ together with an [[equivalence in an (∞,1)-category]]

$$
  \eta \colon i_2^\ast \nabla_2 \stackrel{\simeq}{\to} i_1^\ast \nabla_1
  \,.
$$

On the underlying [[curvatures]] this implies that

$$
  i_2^\ast \omega_2 = i_1^\ast \omega_1
  \,.
$$

Hence if $Z \to X \times Y$ is a maximal inclusion with this property, the above diagram is a prequantization of a morphism in the Weinstein symplectic category.




### Motivic stabilization 

[[Nitu Kitchloo]] defines the [[stable (infinity,1)-category|stable]] symplectic category $\mathbb{S}$, which has as [[objects]] [[symplectic manifolds]], and [[morphisms]] are certain [[Thom spectra]]
associated to [[Lagrangian correspondences]] $\overline{M} \times N$, where $\overline{M}$ denotes the conjugate with symplectic form $-\omega$.  One can view this as a category of symplectic [[motives]].

Considering an oriented version of the category $\mathbb{S}$, there is a canonical [[fiber functor]] $F : M \mapsto \mathbb{S}(pt, M)$, and one may consider the [[motivic Galois group]] $G$ of monoidal [[automorphisms]] of $F$.  ([Kitchloo 12, question 8.6, p. 19](#Kitchloo)).

It turns out to have a natural subgroup which is isomorphic to the quotient of the [[Grothendieck-Teichmüller group]].

## Related concepts

* [[Fukaya category]]

* [[Lagrangian correspondences and category-valued TFT]]

## References
 {#References}

The way that [[Lagrangian correspondences]] encode [[symplectomorphisms]] in [[symplectic geometry]] and hence evolution in [[mechanics]] is reviewed (and put in the broader context of [[BV-BRST formalism]]) in 

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], _Classical and quantum Lagrangian field theories with boundary_ ([arXiv:1207.0239](http://arxiv.org/abs/1207.0239))
 {#CattaneoMnevReshetikhin12}

In his work on Fourier integral operators, 

* [[Lars Hörmander]], _Fourier Integral Operators I._, Acta Math. 127 (1971) 79&#8211;183.
14

following

* [[Victor Maslov]], _Theory of Perturbations and Asymptotic Methods (in Russian)_, Moskov.
Gos. Univ., Moscow, (1965).

observed that, under a transversality assumption, the set-theoretic composition of two [[Lagrangian submanifolds]] is again a Lagrangian submanifold, and that this composition is a "[[classical limit]]" of the composition of certain [[linear operators]].


Shortly thereafter, 

* [[Jędrzej Śniatycki]], W.M. Tulczyjew, *Generating forms of Lagrangian submanifolds*, Indiana Univ. Math. J. **22** (1972) 267-275

defined symplectic relations as [[isotropic submanifolds]] of products and showed that this class of relations was closed under "clean" composition.  Following in part some (unpublished) ideas of [[Alan Weinstein]], 

* [[Victor Guillemin]], [[Shlomo Sternberg]], _Some problems in integral geometry and some related problems in microlocal analysis_, Amer. J. Math. 101 (1979), 915&#8211;955 ([JSTOR](http://www.jstor.org/stable/2373923))

observed that the linear canonical relations (i.e., lagrangian subspaces of products of [[symplectic vector spaces]]) could be considered as the morphisms of a category, and they constructed a
partial [[quantization]] of this category (in which lagrangian subspaces are enhanced by halfdensities.) 
The quantization of the linear symplectic category was part of a larger project of quantizing canonical relations (enhanced with extra structure, such as half-densities) in a functorial way, and this program was set out more formally 

* [[Alan Weinstein]], _Symplectic Manifolds and Their Lagrangian Submanifolds_, Advances in Math. **6** (1971) 329346 \[<a href="https://doi.org/10.1016/0001-8708(71)90020-X">doi:10.1016/0001-8708(71)90020-X</a>\]

* [[Alan Weinstein]], _Symplectic geometry_, Bulletin Amer. Math. Soc. **5** (1981) 1-13 &lbrack;[doi:10.1090/S0273-0979-1981-14911-9](http://dx.doi.org/10.1090/S0273-0979-1981-14911-9)&rbrack;

See also:

* W.M.Tulczyjew, S.Zakrzewski, _The category of Fresnel kernels_, J. Geom. Phys. 1:3, 1984, 79--120 <a href="https://doi.org/10.1016/0393-0440(84)90021-4">doi</a>

Lecture notes reviewing these developments include

* {#Weinstein09} [[Alan Weinstein]], _Symplectic Categories_, proceedings of Geometry Summer School, Lisbon, July 2009 ([arXiv:0911.4133](http://arxiv.org/abs/0911.4133))
 
from the introduction of which parts of the commented list of references above is taken. Further review includes

* {#Canez11} Santiago Canez, _Double Groupoids, Orbifolds, and the Symplectic Category_ ([arXiv:1105.2592](http://arxiv.org/abs/1105.2592))


Further refinements in [[higher category theory]] are discussed in

* [[Katrin Wehrheim]], [[Chris Woodward]], _Functoriality for Lagrangian correspondences in Floer theory_, [arXiv:0708.2851](http://arxiv.org/abs/0708.2851)
 {#WehrheimWoodward}

* [[Nitu Kitchloo]], _The Stable Symplectic Category and Geometric Quantization_ ([arXiv:1204.5720](http://arxiv.org/abs/1204.5720v1))
 {#Kitchloo}

* [[Nitu Kitchloo]], [[Jack Morava]], _The Grothendieck--Teichm&#252;ller group and the stable symplectic category_, 2012.  ([arxiv:1212.6905](http://arxiv.org/abs/1212.6905))

A closed [[symmetric monoidal category]] version of the symplectic category and the observation that this hence is a [[categorical semantics]] for [[quantum logic]] qua [[linear logic]] is in

* [[Sergey Slavnov]], _From proof-nets to bordisms: the geometric meaning of multiplicative connectives_, Mathematical Structures in Computer Science __15__:06  (2005) 1151--1178
 {#Slavnov05}
* [[Sergey Slavnov]], _Geometrical semantics for linear logic (multiplicative fragment)_, Theoretical Computer Science 357, no. 1--3 (2006) 215--229 [doi](https://doi.org/10.1016/j.tcs.2006.03.020)

Remarks about refinements to correspondences of smooth $\infty$-groupoids in the slice over prequantum moduli is in 

* [[Urs Schreiber]], _[[schreiber:Synthetic Quantum Field Theory]]_, Talk at [CMS Summer Meeting 2013](http://cms.math.ca/Events/summer13/)
 {#SyntheticQFT}

String diagrams for the linear and affine Weinstein category using graphical linear algebra

* Cole Comfort, [[Aleks Kissinger]], _A Graphical Calculus for Lagrangian Relations_, In Proceedings ACT 2021. [doi](https://doi.org/10.4204/EPTCS.372.24)


[[!redirects stable symplectic category]]

[[!redirects symplectic category]]

[[!redirects motivic symplectic category]]
