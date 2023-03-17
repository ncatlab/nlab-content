
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Produoidal category
* table of contents
{: toc}

## Idea

A **produoidal category** is like a [[duoidal category]] in whose structure (namely, the two [[tensor product|tensor products]] and [[unit object|unit objects]]) we have replaced [[functors]] by [[profunctors]]. Alternatively, a produoidal category is a category with two [[promonoidal category|promonoidal structures]] which [[interchange law|interchange]] laxly.



## Definition 

A **produoidal category** is a pair of [[pseudomonoid|pseudomonoids]] that interchange laxly in the [[monoidal bicategory]] [[Prof]].
This means that it is a [[category]] $\mathbb{C}$ together with

* a first [[promonoidal category|promonoidal structure]] $\mathbb{C}_{\otimes} \colon \mathbb{C} \times \mathbb{C} &#8696; \mathbb{C}$ and $\mathbb{C}_{I}\colon 1 &#8696; \mathbb{C}$;
* a second [[promonoidal category|promonoidal structure]] $\mathbb{C}_{\triangleleft} \colon \mathbb{C} \times \mathbb{C} &#8696; \mathbb{C}$ and $\mathbb{C}_{N}\colon 1 &#8696; \mathbb{C}$;
* the same laxators as a [[duoidal category]], including, for instance,
$$\begin{aligned}
& \int^{U,V}\mathbb{C}_{\otimes}(X;U,V) \times \mathbb{C}_{\triangleleft}(U;A,B) \times
\mathbb{C}_{\triangleleft}(V;C,D) \to \int^{P,Q}\mathbb{C}_{\triangleleft}(X;P,Q) \times \mathbb{C}_{\otimes}(P;A,C) \times
\mathbb{C}_{\otimes}(Q;B,D);
\end{aligned}$$
* the same coherence conditions as a [[duoidal category]].



## Examples

 * [[optic (in computer science)|Optics]] over a monoidal category form a produoidal category. [EHR23](#EarnshawHeffordRoman23)


## References

The first mention of produoidal categories as a duoidale seems to be:

 * [[Thomas Booker]], [[Ross Street]]. _Tannaka duality and convolution for duoidal categories_, ([link](https://arxiv.org/pdf/1111.5659.pdf)).

An explicit unpacking of the definition, along with examples including the category of [[optic (in computer science)|optics]] appears in

 * {#EarnshawHeffordRoman23} [[Matt Earnshaw]], [[James Hefford]], [[Mario Román]]. _The Produoidal Algebra of Process Decomposition_ ([link](https://arxiv.org/abs/2301.11867)).

