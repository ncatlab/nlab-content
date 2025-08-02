[[!redirects affine schemes]]

#Contents#
* table of contents
{:toc}

## Definition

### General

An __affine scheme__ is a [[scheme]] that as a [[sheaf]] on the [[opposite category]] [[CRing]]${}^{op}$ of commutative [[ring]]s (or equivalently as a sheaf on the subcategory of finitely presented rings) is [[representable functor|representable]]. In a [[ringed space]] picture an affine scheme is a [[locally ringed space]] which is isomorphic to the [[prime spectrum]] of a commutative ring. Affine schemes form a [[full subcategory]] $Aff\hookrightarrow Scheme$ of the category of schemes.

The correspondence $Y\mapsto Spec(\Gamma_Y \mathcal{O}_Y)$ extends to a [[functor]] $Scheme\to Aff$. The __fundamental theorem on morphisms of schemes__ (see [below](#IsbellDuality)) says that there is a bijection  

$$
  CRing(R, \Gamma_Y\mathcal{O}_Y) \cong Scheme(Y, Spec R).
$$

In other words, for fixed $Y$, and for varying $R$ there is a restricted functor  

$$ Scheme(-,Y)|_{Aff^{op}} = h_Y|_{Aff^{op}} = h_Y|_{CRing} : CRing\to Set,$$ 

and the functor $Y\mapsto h_Y|_{CRing}$ from schemes to presheaves on $Aff$ is [[fully faithful functor|fully faithful]]. Thus the general schemes if defined as ringed spaces, indeed form a full subcategory of the category of presheaves on $Aff$. See at _[[functorial geometry]]_.


There is an analogue of this theorem for relative [[noncommutative scheme]]s in the sense of Rosenberg. 

+-- {: .num_remark}
###### Remark
There is no similar equation the other way round, that is "$CRing(\Gamma_Y\mathcal{O}_Y, R) \cong Scheme(Spec R, Y)$" is not true in general. As a mnemonic, note that with ordinary [[Galois connection]]s between power sets, one is always [[Galois connection#properties|homming into (not out of)]] the functorial construction. More geometrically, consider the example $Y = \mathbb{P}^n$ and $R = \mathbb{C}$. Then the left hand side $CRing(\Gamma_Y\mathcal{O}_Y, R)$ only contains the unique ring homomorphism $\mathbb{Z} \to \mathbb{C}$, since $\mathcal{O}_{\mathbb{P}^n}(\mathbb{P}^n) \cong \mathbb{Z}$. On the other hand, the right hand side $Scheme(Spec R, Y)$ consists of all the $\mathbb{C}$-valued points of $\mathbb{P}^n$ (of which there are many).

=--

### Relative affine schemes

A __relative affine scheme__ over a scheme $Y$ is a [[relative scheme]]  $f:X\to Y$ isomorphic to the spectrum of a (commutative unital) algebra $A$ in the category of quasicoherent $\mathcal{O}_Y$-modules; such a "relative" spectrum has been introduced by Grothendieck. It is characterized by the property that for every open $V\subset Y$ the inverse image $f^{-1}V\subset X$ is an open affine subscheme of $X$ isomorphic to $Spec(A(V))$ and such open affines glue in such a way that $f^{-1}V\hookrightarrow f^{-1}W$ corresponds to the restriction morphism $A(W)\to A(V)$ of algebras. 

Relative affine scheme is a concrete way to represent an [[affine morphism]] of schemes. 

## Properties

### Isbell duality
  {#IsbellDuality}

+-- {: .num_prop #AffineSchemesFullSubcategoryOfOppositeOfRings}
###### Proposition
**([[affine schemes]] form [[full subcategory]] of [[opposite category|opposite]] of [[rings]])**

The [[functor]]

$$
  \mathcal{O}
  \;\colon\;
  Schemes_{Aff}
    \longrightarrow
  Ring^{op}
$$

from affine schemes to their global [[rings of functions]] is a [[fully faithful functor]].


=--

(e.g. [Hartschorne 77, chapter II, prop. 2.3](#Hartschorne77))

+-- {: .num_remark}
###### Remark
**([[Isbell duality]] between [[geometry]] and [[algebra]])**


Prop. \ref{AffineSchemesFullSubcategoryOfOppositeOfRings} is the analog in [[algebraic geometry]] of similar statements of [[Isbell duality]] between [[geometry]] and [[algebra]], such as [[Gelfand duality]] or [[Milnor's exercise]].

=--

[[!include Isbell duality - table]]




### Affine Serre's theorem

 [[affine Serre's theorem|Affine Serre's theorem]]

Given a commutative unital ring $R$ there is an equivalence of categories
${}_R Mod\to Qcoh(Spec R)$ between the category of $R$-modules and the category of quasicoherent sheaves of $\mathcal{O}_{Spec R}$-modules given on objects by $M\mapsto \tilde{M}$ where $\tilde{M}$ is the unique sheaf such that the restriction on the principal Zariski open subsets is given by the localization $\tilde{M}(D_f) = R[f^{-1}]\otimes_R M$ where  $D_f$ is the principal Zariski open set underlying $Spec R[f^{-1}]\subset Spec R$, and the restrictions are given by the canonical maps among the localizations. The action of $\mathcal{O}_{Spec R}$ is defined using a similar description of $\mathcal{O}_{Spec R} = \tilde{R}$. Its right adjoint (quasi)inverse functor is given by the global sections functor $\mathcal{F}\mapsto\mathcal{F}(Spec R)$. 

## Related concepts

* [[spectral topological space]]

## References

* {#Hartschorne66} Robin Hartshorne, _Algebraic geometry_, Springer 1977

On an approach on schemes as locally representable sheaves on the site of affine schemes see

* Demazure, [[P. Gabriel]], _Algebraic groups_

* [[Daniel Murfet]], _Schemes via noncommutative localisation_ (2005) [pdf](http://therisingsea.org/notes/SchemesFromLocalisation.pdf)

> In this note we give an exposition of the well-known results of [[Pierre Gabriel|Gabriel]], which show how to define affine schemes in terms of the theory of noncommutative localisation.

For [[affine schemes]] in [[cubical type theory]], see:

* [[Anders Mörtberg]], [[Max Zeuner]], *A Univalent Formalization of Affine Schemes* ([arXiv:2212.02902](https://arxiv.org/abs/2212.02902))

* [[Max Zeuner]], *A univalent formalization of affine schemes*, 20 October 2022 ([slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Zeuner-2022-10-20-HoTTEST.pdf), [video](https://www.youtube.com/watch?v=nLP7GjL1Buc))

category: algebraic geometry

[[!redirects Zariski duality]]