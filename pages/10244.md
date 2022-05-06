

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The "doubly supersymmetric geometric approach" ([BPSTV 95](#BPSTV95), [Howe-Sezgin 97](#HoweSezgin97)), also called the _super-embedding approach_ ([Sorokin 99](#Sorokin99)), is a formulation of super-$p$-[[brane]] [[sigma-models]] entirely within [[supergeometry]], where not only the [[target spacetime]] is taken to be a [[supermanifold]], as in [[Green-Schwarz sigma-models]], and not only the [[worldvolume]] is taken to be a supermanifold, as in the [[NSR string]], but where both are taken to be supermanifolds.

<center>
<img src="https://ncatlab.org/nlab/files/pBraneEmbedding.jpg" width="800">
</center>

> graphics grabbed from [FSS 19c](#FSS19c)


## Properties

### $\kappa$-Symmetry as super-general covariance
 {#KappaSymmetry}

The notorious phenomenon of [[kappa-symmetry]] in [[Green-Schwarz sigma-models]] is revealed by the superembedding approach to be nothing but the odd-graded components of the [[super-diffeomorphism]] [[invariant|invariance]] on the [[worldvolume]], hence: of super-[[general covariance]] ([Sorokin-Tkach-Volkov 89](#SorokinTkachVolkov89), review includes [Sorokin 99, section 4.3](#Sorokin99), [Howe-Sezgin 04, section 4.3](#HoweSezgin04)): 

If 

1. $X$ denotes a [[superspacetime]] locally modeled on [[super-Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert \mathbf{N}}$

1. $\Sigma$ denotes a [[supermanifold|super]]-[[worldvolume]] of a [[super p-brane]] locally modeled on [[super-Minkowski spacetime]] $\mathbb{R}^{p,1\vert \mathbf{N}/2}$

1. so that a [[sigma-model]] [[field (physics)|field]] configuration for a [[super p-brane]] of shape $\Sigma$ to propagate in $X$ is a morphism of [[supermanifolds]] of the form

   $$
     \array{
        \Sigma && \text{super-worldvolume}
        \\
        \downarrow^{\mathrlap{\phi}} &&\text{sigma-model super-field}& 
        \\
        X && \text{super-spacetime}
     }
   $$

then:

1. the postcomposition [[action]] of [[spacetime]] [[super-isometries]] $X \stackrel{\simeq}{\longrightarrow} X$ is in even degree the action of [[spacetime]] [[isometries]] and in odd degree the action of **[[spacetime]] [[supersymmetry]]** on the sigma-model fields;

1. the precomposition action of [[worldvolume]] [[super-diffeomorphism]] $\Sigma \stackrel{\simeq}{\to} \Sigma$ is in even degree the action of bosonic worldvolume [[diffeomorphism]] and in odd degree the action of **$\kappa$-symmetry**:

$$
  \array{
      \Sigma  &\underoverset{\simeq}{\kappa\text{-symmetry}}{\longrightarrow}& \Sigma
      \\
      \downarrow^{\mathrlap{\phi}} && \downarrow^{\mathrlap{\phi'}}
      \\
      X &\underoverset{\simeq}{\text{spacetime supersymmetry}}{\longrightarrow}&
    X
  }
  \,.
$$

Notice here the assumption that the number of odd directions on the [[worldvolume]] is half that of the [[target spacetime]]. This is the default assumption for fundamental [[super p-branes]], and it directly reflects the statement that the corresponding [[black brane]] solutions are $1/2$ [[supergravity]] [[BPS states]].

For example, consider the embedding 

$$
  \mathbb{R}^{2,1} \hookrightarrow \mathbb{R}^{10,1}
$$

of 2+1d [[Minkowski spacetime]], thought of as the [[worldvolume]] of a [[membrane]], into 11d Minkowski spacetime, linearly along the coordinate axis. Any such embedding breaks the [[isometry group]] of $\mathbb{R}^{10,1}$ from the 11d [[Poincaré group]] $Iso(10,1)$ to the [[product group]] 

$$
  Iso(2,1) \times SO(8)
    \hookrightarrow
  Iso(10,1)
$$ 

(meaning that this [[subgroup]] is the [[stabilizer subgroup]] of the embedding). 

Now consider instead [[super Minkowski spacetime]] $\mathbb{R}^{10,1\vert \mathbf{32}}$ (with $\mathbf{32}$ the irreducible [[Majorana spinor]] representation in 11), hence the local model [[superspace]] for [[super spacetimes]] in [[11-dimensional supergravity]]. We are to ask what subspace of the [[spin representation]] $\mathbf{32}$ preserves the embedding in that the [spinor bilinear pairing](Majorana+spinor#TheSpinorPairingToVectors) $\overline{\psi}_1 \Gamma \psi_2$ on that subspace lands in $\mathbb{R}^{2,1} \hookrightarrow Iso(2,1) \hookrightarrow Iso(10,1)$ ([Sorokin 99, section 5.1](#Sorokin99)). This is found to be the case for a half-dimensional subspace, and hence we may lift the above to a super-embedding of the form


$$
  \label{M2WordvolumeInSpacetime}
  \mathbb{R}^{2,1\vert 8 \otimes \mathbf{2}} \hookrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}
$$

(where now $\mathbf{2}$ is the [[irrep|irreducible]] [[Majorana spinor]] representation in 3d, and $8 \otimes \mathbf{2}$ denotes the [[direct sum]] of 8 copies of it)
such that the induced [[stabilizer group|stabilizer]] [[supergroup]] inside the [[super Poincaré group ]] now is 

$$
  Iso(\mathbb{R}^{2,1\vert 8 \otimes \mathbf{2}}) \times Spin(8)
    \hookrightarrow
  Iso(\mathbb{R}^{10,1\vert \mathbf{32}})
  \,.
$$

It is in this sense that the membrane "breaks exactly half the supersymmetry", namely from $\mathbf{32}$ to $8 \otimes \mathbf{2}$.

If one now thinks of this not as inclusions of global spacetimes, but of their super tangent spaces at the points where the membrane sits in spacetime, then this reflects the local structure of $\kappa$-symmetry: the $\kappa$-symmetries are locally generated by the 16 odd dimensions in $Iso(\mathbb{R}^{2,1\vert 8 \otimes \mathbf{2}} )$, being super-translations along the membrane worldvolume. 

This explains why $\kappa$-symmetry in [[Green-Schwarz sigma models]] is taken to quotient out precisely half the spinor components, hence why, in the fully super-covariant formulation, one takes the worldvolume of a super $p$-brane in a superspacetime locally modeled on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ to be $\mathbb{R}^{p,1\vert \mathbf{N}/2}$.
But notice that this is not a mathematical necessity. One may consider the worldvolume instead to have fewer odd directions. This then describes [[sigma models]] for "non-BPS super $p$-branes" (or rather "non-half-BPS" ).

## Brane Lagrangians by relative trivialization

The super-embedding formalism has mostly been used for deriving [[equations of motion]] of [[super p-brane sigma-models]].

But at least for some brane species, also their [[Lagrangian densities]] emerge naturally from the super-embedding, namely as relative trivializations of the brane cocycles as given by the [[schreiber:The brane bouquet|brane scah/brane bouquet]], relative to the superembedding:

[[BraneSuperEmbeddings.jpg:file]]

<center>
<img src="https://ncatlab.org/nlab/files/BraneSuperEmbeddings.jpg" width="600">
</center>

> graphics grabbed from [HSS 18](#HSS18)


### For strings and membranes
 {#LagrangiansForStringsAndMembranes}

For the [[superstring]] and the [[super-membrane]] the construction of their [[Green-Schwarz sigma-model]] [[Lagrangian densities]] as relative trivialization of their super-cocycles along their super-embeddings is estalished in [Howe-Sezgin 05 (4.72)](#HoweSezgin05), [HSS 18, Prop. 6.10](#HSS18):

<center>
<img src="https://ncatlab.org/nlab/files/M2BraneEmbedding.jpg" width="800">
</center>

> graphics grabbed from [FSS 19c](#FSS19c)

### For the M5-brane

In [FSS 19c](#FSS19c) is offered a proof that combining super-embedding formalism with [[exceptional generalized geometry]], the [[Perry-Schwarz action functional|Perry-Schwarz-type Lagrangian]] for the [[M5-brane]] emerges as the relative trivialization of the super-cocycle of the M5-brane relative to its super-exceptional embedding.

## Related concepts

[[!include worldvolume-target supersymmetry of brane sigma-models]]

## References

### General

Under the name "doubly supersymmetric geometrical approach" the formalism originates in

* {#BPSTV95} [[Igor Bandos]], [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], [[Dmitry Volkov]], _Superstrings and supermembranes in the doubly supersymmetric geometrical approach_, Nucl. Phys. B446:79-118, 1995 ([arXiv:hep-th/9501113](https://arxiv.org/abs/hep-th/9501113))

* {#HoweSezgin97} [[Paul Howe]], [[Ergin Sezgin]], _$D=11$, $p=5$_, Phys.Lett. B394 (1997) 62-66 ([arXiv:hep-th/9611008](https://arxiv.org/abs/hep-th/9611008))


Review is in

* {#Sorokin99} [[Dmitri Sorokin]], _Superbranes and Superembeddings_, Phys. Rept. 329:1-101, 2000 ([arXiv:hep-th/9906142](http://arxiv.org/abs/hep-th/9906142))

* {#Sorokin01} [[Dmitri Sorokin]], _Introduction to the Superembedding Description of Superbranes_, AIP Conference Proceedings 589, 98 (2001) ([arXiv:hep-th/0105102](https://arxiv.org/abs/hep-th/0105102))

where also the term "superembedding approach" is introduced.

Derivation of [[BPS state|1/2 BPS]] superembedding via [[rational equivariant homotopy theory|rational]] [[ADE-singularity|ADE-]][[equivariant cohomotopy]]:

* {#HSS18} [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], Section 4 of _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_, Comm. Math. Phys. 2019 ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

### $\kappa$-Symmetry

The [[supergeometry|super-geometric]] interpretation of [[kappa-symmetry]] as the odd-graded part of the action of [[super-diffeomorphism]] on the [[super p-brane]] [[worldvolume]], regarded itself as a [[supermanifold]] was first suggested in

* {#SorokinTkachVolkov89} [[Dmitri Sorokin]], V. Tkach and [[Dmitrij Volkov]], _Superparticles, twistors and Siegel symmetry_, Mod. Phys. Lett. A4 (1989) 901-908 ([spire:271923](http://inspirehep.net/record/271923), [doi:10.1142/S0217732389001064](https://doi.org/10.1142/S0217732389001064))

Review of this perspective includes

* {#Sorokin99} [[Dmitri Sorokin]], _Superbranes and Superembeddings_, Phys.Rept.329:1-101,2000 ([arXiv:hep-th/9906142](http://arxiv.org/abs/hep-th/9906142))

* {#HoweSezgin04} [[Paul Howe]], [[Ergin Sezgin]], section 4.3 of _The supermembrane revisited_, Class.Quant.Grav. 22 (2005) 2167-2200 ([arXiv:hep-th/0412245](http://arxiv.org/abs/hep-th/0412245))

### For the superstring

The [[equations of motion]] for the [[superstring]] have been derived via the [[superembedding approach]] in

* [BPSTV 95, Chapter 4](#BPSTV95)

See also 

* [[Igor Bandos]], [[Dmitrij Sorokin]], [[Dmitrij Volkov]], _On the generalized action principle for superstrings and supermembranes_, Phys. Lett. B352:269-275, 1995 ([arXiv:hep-th/9502141](https://arxiv.org/abs/hep-th/9502141))

### For the M2-brane

The [[equations of motion]] for the [[M2-brane]] have been derived via the [[superembedding approach]] in 

* [BPSTV 95, Chapter 3](#BPSTV95)

and the [[Lagrangian density]] in

* {#HoweSezgin05} [[Paul Howe]], [[Ergin Sezgin]], _The supermembrane revisited_, Class. Quant. Grav. 22 (2005) 2167-2200 ([arXiv:hep-th/0412245](https://arxiv.org/abs/hep-th/0412245))

### For the M5-brane

The [[equations of motion]] for the [[M5-brane]] have been derived via the [[superembedding approach]] in

* [Howe-Sezgin 97](#HoweSezgin97)

following the [[superspace]]-computations in

* {#HoweSezginWest97} [[Paul Howe]], [[Ergin Sezgin]], [[Peter West]], _Covariant Field Equations of the M Theory Five-Brane_, Phys. Lett. B399 (1997) 49-59 ([arXiv:hep-th/9702008](https://arxiv.org/abs/hep-th/9702008))

reviewed in

* [Sorokin 99, Section 5.2](#Sorokin99)

Discussion for 3+3-dimensional split:

* Sheng-Lan Ko, [[Dmitri Sorokin]], Pichet Vanichchapongjaroen, _The M5-brane action revisited_, JHEP11(2013)072 ([arXiv:1308.2231](https://arxiv.org/abs/1308.2231))

Claim that combining the super-embedding formalism with [[super-exceptional generalized geometry]], the [[Perry-Schwarz action functional|Perry-Schwarz-type Lagrangian]] for the [[M5-brane]] emerges as the relative trivialization of the super-cocycle of the M5-brane relative to its super-exceptional embedding:

* {#FSS19c} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Super-exceptional embedding construction of the M5-brane|Super-exceptional geometry: origin of heterotic M-theory and super-exceptional embedding construction of M5]]_ ([arXiv:1908.00042](https://arxiv.org/abs/1908.00042))


[[!redirects superembedding formalism]]

[[!redirects super-embedding approach]]
[[!redirects superembedding approach]]

[[!redirects super-embedding construction]]
[[!redirects superembedding construction]]



