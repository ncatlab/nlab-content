
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

* J. Sniatycki, W.M. Tulczyjew, _Generating forms of Lagrangian submanifolds_, Indiana Univ. Math. J. 22(1972), 267&#8211;275.

defined symplectic relations as [[isotropic submanifolds]] of products and showed that this class of relations was closed under "clean" composition.  Following in part some (unpublished) ideas of [[Alan Weinstein]], 

* [[Victor Guillemin]] [[Shlomo Sternberg]], _Some problems in integral geometry and some related problems in microlocal analysis_, Amer. J. Math. 101 (1979), 915&#8211;955.

observed that the linear canonical relations (i.e., lagrangian subspaces of products of [[symplectic vector spaces]]) could be considered as the morphisms of a category, and they constructed a
partial [[quantization]] of this category (in which lagrangian subspaces are enhanced by halfdensities.) 
The quantization of the linear symplectic category was part of a larger project of quantizing canonical relations (enhanced with extra structure, such as half-densities) in a functorial way,
and this program was set out more formally 

* [[Alan Weinstein]], _Symplectic manifolds and their lagrangian submanifolds_, Advances in Math. 6 (1971), 329&#8211;346.

* [[Alan Weinstein]], _Symplectic geometry_, Bulletin Amer. Math. Soc. (new series) 5 (1981), 1&#8211;13.

Lecture notes reviewing these developments include

* [[Alan Weinstein]], _Symplectic Categories_, proceedings of Geometry Summer School, Lisbon, July 2009 ([arXiv:0911.4133](http://arxiv.org/abs/0911.4133))
 {#Weinstein09}

from the introduction of which parts of the commented list of references above is taken.


Further refinements in [[higher category theory]] are discussed in

* [[Katrin Wehrheim]] and [[Chris Woodward]], _Functoriality for Lagrangian correspondences in Floer theory_, [arXiv:0708.2851](http://arxiv.org/abs/0708.2851)
 {#WehrheimWoodward}

* [[Nitu Kitchloo]], _The Stable Symplectic Category and Geometric Quantization_ ([arXiv:1204.5720](http://arxiv.org/abs/1204.5720v1))
 {#Kitchloo}

* [[Nitu Kitchloo]], [[Jack Morava]], _The Grothendieck--Teichm&#252;ller group and the stable symplectic category_, 2012.  ([arxiv:1212.6905](http://arxiv.org/abs/1212.6905))

Remarks about refinements to correspondences of smooth $\infty$-groupoids in the slice over prequantum moduli is in 

* [[Urs Schreiber]], _[[schreiber:Synthetic Quantum Field Theory]]_, Talk at [CMS Summer Meeting 2013](http://cms.math.ca/Events/summer13/)
 {#SyntheticQFT}

[[!redirects stable symplectic category]]

[[!redirects symplectic category]]

[[!redirects motivic symplectic category]]
