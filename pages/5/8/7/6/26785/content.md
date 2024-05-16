
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}



## Idea

A *Riemannian immersion* or *isometric immersion* $\Sigma \hookrightarrow X$ of [[Riemannian manifolds]] is an [[immersion]] of their [[underlying]] [[smooth manifolds]] which is also an [[isometry]] with respect to their [[Riemannian metrics]].

Simiarly, an *isometric embedding* is an isometric immersion which is also an [[embedding of smooth manifolds]], hence [[embedding of topological spaces|of the underlying topological spaces]].

The *isometric immersion/embedding problem* is to find isometric immersions/embeddings of Riemannian manifolds into (large-dimensional) [[Euclidean spaces]] (e.g. [Han & Hong 2006](#HanHong06), [Han & Lewicka 2023](#HanLewicka23)).



## Properties

### Adapted Darboux coframes
 {#AdaptedDarbouxCoframes}

Given an immersion $\phi \colon \Sigma \hookrightarrow X$ into a [[Riemannian manifold]] $X$ --- hence in particular with $dim(\Sigma) \leq dim(X)$ --- then a local orthonormal [[frame field]] $\big(e^a\big)_{a = 1}^{dim(X)}$ on $X$ (i.e. such that the [[metric tensor]] on $X$ is locally $g = e^a \otimes e_a$) is called a *Darboux frame* ([Berger, Bryant & Griffith 1983](#BergerBryantGriffith83), later  authors also say *Darboux co-frame*, e.g. [Mastrolia, Rigoli & Setti 2012, Def. 1.17](#MastroliaRigoliSetti12), [Giron 2020, §3.2.2](#Giron20), [Chen & Giron 2021, §2.4](#ChenGiron21)) if, locally, the restriction of the frame field to its first $dim(\Sigma)$-components and [[pullback of differential forms|pulled back]] along $\phi$ to $\Sigma$

\[
  \label{PullbackOfDarbouxFrame}
  \big(
    \phi^\ast e^a
  \big)
    ^{ dim(\Sigma) }
    _{ a=1 }
\]

is a [[frame field]] for $\Sigma$. 

\begin{proposition}
\label{ExistenceOfDarbouxFrames}
Given an immersion into a Riemannian manifold, local Darboux frames always exist. 
\end{proposition}
This is claimed in passing in [Mastrolia, Rigoli & Setti 2012, p. 33](#MastroliaRigoliSetti12) and in the generality of suitable [[sequences]] of immersions in [Chen & Giron 2021, Thm. 2.2](#ChenGiron21).

Hence an immersion $\Sigma \hookrightarrow X$ of Riemannian manifolds is isometric iff for any of its Darboux frame fields the pullback frame (eq:PullbackOfDarbouxFrame) corresponds to the given metric on $\Sigma$.

## References

* {#BergerBryantGriffith83} [[Eric Berger]], [[Robert Bryant]], [[Phillip Griffiths]], *The Gauss equations and rigidity of isometric embeddings*, Duke Math. J. **50** 3 (1983) 803-892 &lbrack;[doi:10.1215/S0012-7094-83-05039-1](http://dx.doi.org/10.1215/S0012-7094-83-05039-1)&rbrack;

* {#HanHong06} Qing Han, Jia-Xing Hong: *Isometric Embedding of Riemannian Manifolds in Euclidean Spaces*, Mathematical Surveys and Monographs **130**, AMS (2006) &lbrack;[ISBN:0821840711](https://maa.org/press/maa-reviews/isometric-embedding-of-riemannian-manifolds-in-euclidean-spaces)&rbrack;


* {#MastroliaRigoliSetti12} Paolo Mastrolia, Marco Rigoli, Alberto G. Setti, §1.3 *Some formulas for immersed submanifolds* in: *Yamabe-type Equations on Complete, Noncompact Manifolds*, Birkhäuser (2012) &lbrack;[doi:10.1007/978-3-0348-0376-2](https://doi.org/10.1007/978-3-0348-0376-2)&rbrack;

* {#Giron20} Tristan Pierre Giron, *On the Analysis of Isometric Immersions of Riemannian Manifolds*, PhD thesis (2020) &lbrack;[uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e](https://ora.ox.ac.uk/objects/uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e), [pdf](https://ora.ox.ac.uk/objects/uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e/download_file?safe_filename=ThesisGironTristan.pdf&type_of_work=Thesis)&rbrack;

* {#ChenGiron21} Gui-Qiang G. Chen, Tristan P. Giron, *Weak continuity of curvature for connections in $L^p$* &lbrack;[arXiv:2108.13529](https://arxiv.org/abs/2108.13529)&rbrack;


* {#Kayban21} Nicholas Kayban, *Riemannian Immersions and Submersions* (2021) &lbrack;[pdf](https://www.math.uwaterloo.ca/~karigian/training/M11-kayban-final-project.pdf), [[Kayban-RiemannianImmersions.pdf:file]]&rbrack;


* {#HanLewicka23} Qing Han, Marta Lewicka, *Isometric immersions and applications*, Notices of the AMS 2023 &lbrack;[arXiv:2310.02566](https://arxiv.org/abs/2310.02566)&rbrack;


[[!redirects Riemannian immersions]]

[[!redirects isometric immersion]]
[[!redirects isometric immersions]]

[[!redirects isometric embedding]]
[[!redirects isometric embeddings]]

