
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **&#268;ech model structure on simplicial sheaves** on a [[site]] $C$ is a model for the [[topological localization]] of an [[(∞,1)-category of (∞,1)-presheaves]] on $C$ to the [[(∞,1)-category of (∞,1)-sheaves]]. 

It is obtained from the the [[?ech model structure on simplicial presheaves]] on $C$ by [[transferred model structure|transfer]] along the sheafification adjunction.

Further [[Bousfield localization of model categories|left Bousfield localization]] at "internal" weak homotopy equivalences leads from the &#268;ech model structure to the [[model structure on simplicial sheaves]] that presents the [[hypercomplete (∞,1)-topos]] which is the [[hypercompletion]] of that presented by the &#268;ech model structure.


## Definition

Let $C$ be a small [[site]], let $sSh (C)$ be the category of simplicial sheaves on $C$, and write $[C^{op}, sSet]_{\check{C},proj}$ and $[C^{op}, sSet]_{\check{C},inj}$ for the projective and injective [[?ech model structure on simplicial presheaves]], respectively. 

+-- {: .un_defn}
###### Definitions

The injective **&#268;ech model structure on simplicial sheaves** on $C$ is the unique model structure on $sSh (C)$ with the following properties:

* The weak equivalences are the morphisms in $sSh (C)$ that are weak equivalences in $[C^{op}, sSet]_{\check{C},inj}$.
* The cofibrations are the monomorphisms.
* The fibrations are the morphisms in $sSh (C)$ that are fibrations in $[C^{op}, sSet]_{\check{C},inj}$.

=--


+-- {: .un_defn}
###### Definition

The projective **&#268;ech model structure on simplicial sheaves** on $C$ is the unique model structure on $sSh (C)$ with the following properties:

* The weak equivalences are the morphisms in $sSh (C)$ that are weak equivalences in $[C^{op}, sSet]_{\check{C},proj}$.
* The trivial fibrations are the morphisms in $sSh (C)$ that are trivial fibrations in the projective &#268;ech model structure on $[C^{op}, sSet]_{\check{C},proj}$, i.e. the componentwise trivial Kan fibrations.

=--

## Constructions

To construct the injective &#268;ech model structure on $sSh (C)$, we use the following facts:

* The inclusion $sSh (C) \hookrightarrow [C^{op}, sSet]$ is fully faithful.
* The left adjoint (i.e. sheafification) $[C^{op}, sSet] \to sSh (C)$ preserves monomorphisms, and the class of monomorphisms in $sSh (C)$ is closed under pushouts, transfinite composition, and retracts.
* The adjunction unit is a natural weak equivalence with respect to the (injective) &#268;ech model structure on $[C^{op}, sSet]$: see Theorem A.2 in [DHI]. 

We may then apply Kan's recognition principle for [[cofibrantly generated model category|cofibrantly generated model structures]] to transfer the injective &#268;ech model structure from $[C^{op}, sSet]$ to $sSh (C)$. By construction, the sheafification adjunction becomes a Quillen equivalence.

On the other hand, to construct the projective &#268;ech model structure on $sSh (C)$, we use Smith's recognition principle for [[combinatorial model category|combinatorial model structures]] and build it like a [[mixed model structure]].

## References

* Dugger, D., S. Hollander and D. C. Isaksen, [_Hypercovers and simplicial presheaves_](http://dx.doi.org/10.1017/S0305004103007175) ([arXiv](http://arxiv.org/abs/math/0205027)).

[[!redirects Cech model structure on simplicial sheaves]]
