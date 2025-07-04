
> This page is about the general concept. For open [[continuous functions]] see at _[[open map]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### For maps between topological spaces

A [[function]]  $f : X \to Y$ between [[topological space]]s  is called an __[[open map]]__ if the [[image]] of every [[open set]] in $X$ is also open in $Y$.

Recall that $f$ is a __[[continuous map]]__ if the [[preimage]] of every [[open subspace|open set]] in $Y$ is open in $X$.  For defining open maps typically one restricts attention to open [[continuous map]]s, although it also makes sense to speak of open functions that are not continuous. 

#### Examples 

* For any two topological spaces $X$, $Y$, the projection map $\pi \colon X \times Y \to Y$ out of the [[product topological space]] is open. 

* If $G$ is a [[topological group]] and $H$ is a subgroup, then the projection to the coset space $p \colon G \to G/H$, where $G/H$ is provided with the quotient topology (making $p$ a quotient map), is open. This follows easily from the observation that if $U$ is open in $G$, then so is 
$$p^{-1}(p(U)) = U H = \bigcup_{h \in H} U h$$ 

* If $p \colon A \to B$ and $q \colon C \to D$ are open maps, then their product $p \times q \colon A \times C \to B \times D$ is also an open map. 

### For morphisms between locales

A continuous map $f\colon X \to Y$ of topological spaces defines a homomorphism $f^*\colon Op(Y) \to Op(X)$ between the [[frames]] of open sets of $X$ and $Y$.  If $f$ is open, then this frame homomorphism is also a [[complete lattice|complete]] [[Heyting algebra]] homomorphism; the converse holds if $Y$ is a [[T-D space]].  Accordingly, we define a map $f\colon X \to Y$ of [[locales]] to be __open__ if it is, as a frame homomorphism $f^*\colon Op(Y) \to Op(X)$, a complete Heyting algebra homomorphism, i.e. it preserves arbitrary [[meets]] and the Heyting implication.

This is equivalent to saying that $f^*\colon Op(Y) \to Op(X)$ has a left adjoint $f_!$ (by the [[adjoint functor theorem]] for posets) which satisfies the [[Frobenius reciprocity]] condition that $f_!(U \cap f^* V) = f_!(U) \cap V$.

In the special case that $Y$ is the one-point locale, the Frobenius reciprocity condition is automatically satisfied.


### For geometric morphisms of toposes

[[categorification|Categorifying]], a [[geometric morphism]] $f\colon X \to Y$ of [[toposes]] is an [[open geometric morphism]] if its [[inverse image functor]] $f^*\colon Y \to X$ is a [[Heyting functor]].

### For morphisms in a topos

A [[class]] $R \subset Mor(\mathcal{E})$ of [[morphism]]s in a [[topos]] $\mathcal{E}$ is called a **class of open maps** if it satisfies the following axioms.

1. Every [[isomorphism]] belongs to $R$;

1. The [[pullback]] of a morphism in $R$ belongs to $R$.

1. If the pullback of a morphism $f$ along an [[epimorphism]] lands in $R$, then $f$ is also in $R$.

1. For every [[set]] $S$ the canonical morphism $(\coprod_{s \in S} *) \to *$ from the $S$-fold [[coproduct]] of the [[terminal object]] to the terminal object is in $R$.

1. For $\{X_i \stackrel{f_i}{\to} Y_i\}_{i \in I} \subset R$ then also the [[coproduct]] $\coprod_i X_i \to \coprod_i Y_i$ is in $R$.

1. If in a diagram of the form

   $$
     \array{
        Y &&\stackrel{p}{\to}&& X
        \\
        & {}_{\mathllap{g}}\searrow && \swarrow_{\mathrlap{f}}
        \\
        && B
     }
   $$

   we have that $p$ is an [[epimorphism]] and $g$ is in $R$, then $f$ is in $R$.

The class $R$ is called a class of **&#233;tale maps** if in addition to the axioms 1-5 above it satisfies

1. for $f : X \to Y$ in $R$ also the [[diagonal]] $X \to X \times_Y X$ is in $R$.

1. If in 

   $$
     \array{
        Y &&\stackrel{p}{\to}&& X
        \\
        & {}_{\mathllap{g}}\searrow && \swarrow_{\mathrlap{f}}
        \\
        && B
     }
   $$

   we have that $p$ is an epimorphism, and $p, g \in R$, then $f\in R$.


For instance ([JoyalMoerdijk, section 1](#JoyalMoerdijk)).

## Related concepts

* [[open geometric morphism]]

* [[essential sublocale]]

* [[closed morphism]], [[proper morphism]]

* [[étale map]]

* [[separated morphism]]

## References

* [[Peter Johnstone]],  _Complemented sublocales and open maps_ , Annals of Pure and Applied Logic **137** (2006) pp.240&#8211;255.

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_, volume II, Oxford University Press 2002. (Section C1.5, pp.520-522)

* {#JoyalMoerdijk} [[André Joyal]], [[Ieke Moerdijk]], _A completeness theorem for open maps_, Annals of Pure and Applied Logic __70__ no.1 (1994) pp.51-86. [MR95j:03104](http://www.ams.org/mathscinet-getitem?mr=1303663), <a href="http://dx.doi.org/10.1016/0168-0072(94)90069-8">doi</a> 


Application to [[transition systems]] and [[bisimulations]]

* {#JoyalNielsenWisnkel94} [[André Joyal]], [[Mogens Nielsen]], [[Glynn Winskel]]: *Bisimulation from open maps*, [[BRICS]] report series RS-94-7 (1994) &lbrack;[doi:10.7146/brics.v1i7.21663](https://doi.org/10.7146/brics.v1i7.21663), [pdf](http://www.brics.dk/RS/94/7/BRICS-RS-94-7.pdf)&rbrack;, Information and Computation **127** 2 (1996) 164-185 &lbrack;[doi:10.1006/inco.1996.0057](https://doi.org/10.1006/inco.1996.0057)&rbrack;

[[!redirects open morphisms]]

