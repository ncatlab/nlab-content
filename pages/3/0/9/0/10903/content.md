
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Dependent linear type theory should be a combination of _[[dependent type theory]]_ and _[[linear type theory]]_.

Following the notion of [[hyperdoctrine]] this should mean, in terms of [[categorical semantics]], that dependent linear type theory is for each [[context]] $\Gamma$ a [[linear type theory]]/possibly-non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal category|symmetric]] [[closed monoidal category]] $(\mathcal{C}_{\Gamma}, \otimes, 1)$ and for each [[homomorphism]] of [[contexts]] $f \;\colon\; \Gamma_1 \longrightarrow \Gamma_2$ functorially an [[adjoint triple]] of [[functors]]

$$
  (f_! \dashv f^\ast \dashv f_\ast) 
    \;\colon\; 
   \mathcal{C}_{\Gamma_1}
    \stackrel{\stackrel{f_!}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\longrightarrow}}{\underset{f_\ast}{\leftarrow}}}
    \mathcal{C}_{\Gamma_2}
  \,.
$$

where $f^\ast$ is [[context extension]] and where the [[left adjoint]] $f_!$ and [[right adjoint]] $f_\ast$ are to be thought of as linear analogs of [[dependent sum]] and [[dependent product]], respectively. Moreover this should satisfy [[Frobenius reciprocity]], hence $f^\ast$ should be a strong [[closed monoidal functor]]. 

Equivalently this is an [[indexed closed monoidal category]] with fiberwise [[dual object|duals]].

Typically one would in addition demand the [[Beck-Chevalley condition]] for consecutive such adjoint triples.

In [[geometry]]/[[topos theory]] such a "linear hyperdoctrine" is known as _[[six operations]] yoga in [[Wirthmüller context|Wirtmüller flavor]]_. In fact there this appears in [[geometric homotopy theory]] ("[[derived functors]] on [[quasicoherent sheaves]]") hence as _dependent linear [[homotopy type theory]]_.

## Properties

### The canonical co-modality
 {#TheCanonicalComodality}

The original axiomatics for [[linear type theory]] in ([Girard 87](#Girard87)) contain in addition to the structures corresponding to a ([[star-autonomous category|star-autonomous]]) [[symmetric monoidal category|symmetric]] [[closed monoidal category]] a certain (co-)[[modality]] traditionally denoted "$!$". 
In ([Benton 95](#Benton95), [Bierman 95](#Bierman95))
it is noticed (reviewed in ([Barber 97, p. 21 (26)](#Barber97))) that a natural [[categorical semantics]] for this modality identifies it with the [[comonad]] that is induced from a [[strong monoidal adjunction]]

$$
  (\Sigma \dashv R)
  \;\colon\;
  \mathcal{C}
  \stackrel{\overset{\Sigma}{\leftarrow}}{\underset{R}{\longrightarrow}}
  S
$$

between the [[closed monoidal category|closed]] [[symmetric monoidal category]] $\mathcal{C}$ wich interprets the given [[linear type theory]] and a [[cartesian monoidal category]] $S$.


If there is only the [[strong monoidal functor]] $\Sigma \;\colon\; S \longrightarrow \mathcal{C}$ without possibly a [[right adjoint]], then ([Barber 97, p. 21 (27)](#Barber97)) speaks of the _structural fragment_ of [[linear type theory]].


In ([Ponto-Shulman 12](#PontoShulman12)) it is observed that this in turn is canonically induced if $\mathcal{C} \simeq \mathcal{C}_\ast$ is the linear type theory over the trivial context of a dependent linear type theory/[[indexed closed monoidal category]] with category of contexts being $S$.

Namely in this case it is natural to set for $X \in S$

$$
  \Sigma(X) \coloneqq (\pi_X)_! (\pi_X)^\ast 1_{\ast}
  \,,
$$

where $\pi_X \;\colon\; X \longrightarrow \ast$ is the canonical morphism to the [[terminal object]] in $S$; and to set for $\phi \;\colon\; X \longrightarrow Y$ any [[morphism]] in $S$

$$
  \Sigma(\phi) 
    \coloneqq 
   \Sigma(X)
    =
  (\pi_X)_! (\pi_X)^\ast 1_\ast
  \stackrel{\simeq}{\to}
  (\pi_Y)_! \phi_! \phi^\ast (\pi_Y)^\ast 1_\ast
  \stackrel{(\phi_Y)_!(\epsilon_\phi)}{\longrightarrow}
  (\pi_Y)_! \phi_! (\pi_Y)^\ast 1_\ast
  =
  \Sigma(Y)
  \,.
$$

One checks that this indeed makes $\Sigma$ be a [[strong monoidal functor]] ([Ponto-Shulman 12, (4.3)](#PontoShulman12)).


## Related concepts

* [[type theory]], [[homotopy type theory]]

* [[modal type theory]]

* [[stable homotopy type]]

* [[geometric homotopy type theory]]

* [[cohesive homotopy type theory]]

## References
 {#References}

Plain [[linear type theory]] originates in

*  [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))
 {#Girard87}

The interpretation of Girard's $!$-modality as the [[comonad]] induced from a [[monoidal adjunction]] between the closed [[symmetric monoidal category]] and a [[cartesian closed category]] is due to

* G. Bierman, _On Intuitionistic Linear Logic_ PhD thesis, Computing
Laboratory, University of Cambridge, 1995
 {#Bierman95}

* N. Benton, _A mixed linear and non-linear logic; proofs, terms and
models_, In _Proceedings of Computer Science Logic_ '94, vol. 933 of
Lecture Notes in Computer Science. Verlag, June 1995. 
 {#Benton95}

A review of all this and further discussion is in 

* Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))
 {#Barber97}


A genuine account of dependent linear type theory is not in the literature at the moment. The closest is maybe this article:

* Iliano Cervesato, [[Frank Pfenning]], _A Linear Logical Framework_, 1996, ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.21.1152))

Discussion of what should be the [[categorical semantics]] of dependent linear type theory, namely [[indexed closed monoidal categories]], is in 

* [[Mike Shulman]], _Framed bicategories and monoidal fibrations_, in  Theory and Applications of Categories,  Vol. 20, 2008, No. 18, pp 650-738.  ([TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html))
 {#Shulman08}

* [[Kate Ponto]], [[Mike Shulman]], _Duality and traces for indexed monoidal categories_, Theory and Applications of Categories, Vol. 26, 2012, No. 23, pp 582-659 ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555))
 {#PontoShulman12}

* [[Mike Shulman]], _Enriched indexed categories_ ([arXiv:1212.3914](http://arxiv.org/abs/1212.3914))
 {#Shulman12}


Comments on the formalization of [[integral transforms]] and [[quantization]] in dependent linear type theory are at

* _[[schreiber:Type-semantics for quantization]]_ 

[[!redirects dependent linear type theories]]

[[!redirects linear dependent type theory]]
[[!redirects linear dependent type theories]]

[[!redirects linear dependent homotopy type theory]]
[[!redirects linear dependent homotopy type theories]]

[[!redirects dependent linear homotopy type theory]]
[[!redirects dependent linear homotopy type theories]]