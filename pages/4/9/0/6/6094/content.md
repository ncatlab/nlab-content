
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _Calabi-Yau algebra_ is an algebraic incarnation of the notion of _[[Calabi-Yau manifold]]_  and [[higher algebra]]-version of the notion of [[Frobenius algebra]].

## Definition


+-- {: .num_defn }
###### Definition

For $A$ a [[dg-algebra]] and $N$ a [[dg-module|dg-bimodule]] over $A$, write

$$
  N^! 
  \coloneqq
  RHom_{A Bimod}(N, A \otimes A)
$$

for the dual $A$-[[bimodule]], where $RHom$ denotes the [[derived functor|right derived]] [[hom-functor]] with respect to the [[model structure on dg-modules]].

=--

+-- {: .num_defn }
###### Definition

A homologically smooth [[dg-algebra]] $A$ is a **Calabi-Yau algebra** of [[dimension]] $d$ if there is a [[quasi-isomorphism]] of $A$-[[bimodule]]s

$$
 f \colon  A \stackrel{\simeq}{\to} A^![d]
$$

such that

$$
  f \simeq f^![d]
  \,.
$$ 

=--

This is [Ginzburg, def. 3.2.3](#Ginzburg).

## Properties

### General

Let $X$ be a [[smooth scheme|smooth]] [[quasi-projective variety]]. Write $D^b(Coh X)$ for the [[derived category]] of bounded [[chain complex]]es of [[coherent sheaves]] over $X$.

+-- {: .num_defn #TiltingGenerator}
###### Definition

An [[object]] $\mathcal{E} \in D^b(Coh X)$ is called a **tilting generator** if the [[Ext]]-functor satisfies

1. $Ext^i(\mathcal{E}, \mathcal{E}) = 0$ for all $i \gt 0$;

1. $Ext^\bullet(\mathcal{E},\mathcal{F}) = 0$ implies $\mathcal{F} = 0$;

1. the [[endomorphism]] algebra $End(\mathcal{E}) = Hom(\mathcal{E},\mathcal{E})$ has finite [[Hochschild cohomology|Hochschild]] [[dimension]].

=--

This appears as [Ginzburg, def. 7.1.1](#Ginzburg). 

+-- {: .num_remark}
###### Remark

For $\mathcal{E}$ a tilting generator there is an [[equivalence of categories|equivalence]] of [[triangulated categories]]

$$
  D^b(Coh X) \stackrel{\simeq}{\to}  D^b(End(\mathcal{E})Mod)
$$

to the [[derived category]] of [[module]]s over $End(\mathcal{E})$.

=--

+-- {: .num_prop}
###### Proposition

For $X$ smooth connected variety which is projective over an affine variety, let $\mathcal{E} in D^b(Coh X)$ be a tilting generator, def. \ref{TiltingGenerator}. 

Then $End \mathcal{E}$ is a Calabi-Yau algebra of dimension $d$ precisely if $X$ is a [[Calabi-Yau manifold]] of dimension $d$.

=--

This appears as [Ginzburg, prop. 3.3.1](#Ginzburg).

#### $0$-Calabi-Yau algebras

A cochain dg-algebra over $k$ is $0$-Calabi-Yau iff it is Koszul and $Tor^0_A(k_A,{}_A k)$ is a symmetric coalgebra.  Proven in  

*  J.-W. He, X.-F. Mao, _Connected cochain DG algebras of Calabi-Yau dimension 0_, Proc. Amer. Math. Soc. __145__ (2017) 937--953 [doi](https://doi.org/10.1090/proc/13081) 

It follows that a Koszul dg-algebra is $0$-Calabi-Yau iff its Ext-algebra is symmetric [[Frobenius algebra|Frobenius]].

### Relation to 2d extended TQFT and the Cobordism hypothesis

+-- {: .num_example }
###### Example

Let $\mathbf{S}$ be a [[good symmetric monoidal (∞,1)-category|good]] [[symmetric monoidal (∞,1)-category]]. Write $Alg(\mathbf{S})$ for the [[symmetric monoidal (∞,n)-category|symmetric monoidal (∞,2)-category]] whose [[object]]s are [[algebra in an (∞,1)-category|algebra objects]] in $\mathbf{S}$ and whose [[morphisms]] are [[bimodule]] objects. 

Then a Calabi-Yau object in $Alg(\mathbf{S})$ is an algebra object $A$ equipped with an $SO(2)$-equivariant morphism


$$
  tr \colon \int_{S^1} A \to 1
$$ 

from the [[Hochschild homology]] $\int_{S^1} A \simeq A \otimes_{A \otimes A} A$, satisfying the condition that the composite morphism

$$
  A \otimes A \simeq \int_{S^0} A \to \int_{S^1} A \stackrel{tr}{\to} 1
$$

exhibits $A$ as its own [[dual object]] $A^\vee$.

Such an algebra object is called a _[[Calabi-Yau algebra]] object_.

=--

This is ([Lurie 09, example 4.2.8](#Lurie09)).


### Classification of 2d TQFT

[[!include 2d TQFT -- table]]


## Related concepts

* [[Calabi-Yau object]]

  * **Calabi-Yau algebra**, [[Calabi-Yau manifold]]

  * [[Calabi-Yau category]]
* [[pre-Calabi-Yau algebra]]

## References

* {#Ginzburg} [[Victor Ginzburg]], _Calabi-Yau algebras_ &lbrack;[arXiv:0612139](http://arxiv.org/abs/math/0612139)&rbrack;
 
* {#Lurie09} [[Jacob Lurie]], section 4.2 of: _[[On the Classification of Topological Field Theories]]_ &lbrack;[arXiv:0905.0465](http://arxiv.org/abs/0905.0465)&rbrack;

An adaptation of this notion to the setting of spectra in [[stable homotopy theory]]:

* Ralph L. Cohen, Inbar Klang, _Twisted Calabi–Yau ring spectra, string topology, and gauge symmetry_, Tunisian J. Math. __2__:1 (2020) [doi](https://doi.org/10.2140/tunis.2020.2.147)

[[!redirects Calabi-Yau algebras]]

[[!redirects Calabi-Yau A-∞ algebra]]
[[!redirects Calabi-Yau A-∞ algebras]]