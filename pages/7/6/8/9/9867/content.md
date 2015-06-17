
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Where a [[homology theory]] is a [[covariant functor]] and a [[cohomology theory]] is a [[contravariant functor]] on some [[category]] of [[spaces]], a _bivariant cohomology theory_ is a [[bifunctor]], hence a functor of two variables, contravariant in the first, and covariant in the second.

Examples:

* In [[noncommutative topology]]: [[KK-theory]].

* In [[noncommutative algebraic geometry]]: [[bivariant algebraic K-theory]], [[noncommutative motives]].


## Axiomatization in homotopy theory
 {#AxiomatizazionInHomotopyTheory}

Here are some notes on a proposal for how to usefully formalize bivariant cohomology theory in [[stable homotopy theory|stable]] [[homotopy theory]]. (This is in generalization of the structure of [[KK-theory]], while the original axioms of ([Fulton-MacPherson 81](#FultonMacPherson81)) are a little different[^footnote].  Aspects of the following appear in ([Nuiten 13](#Nuiten13), [Schreiber 14](#Schreiber14)). See also at _[[dependent linear type theory]]_ the section on _[secondary integral transforms](dependent+linear+type+theory#SecondaryIntegralTransforms)_).

$\,$

Let $E$ be an [[E-∞ ring]], write $GL_1(E)$ for its [[∞-group of units]]. With $\mathbf{H}$ the ambient [[(∞,1)-topos]], write $\mathbf{H}_{/\mathbf{B}GL_1(E)}$ for the [[slice (∞,1)-topos]] over the [[delooping]] of this [[abelian ∞-group]]. This is the [[(∞,1)-category]] of [[spaces]] equipped with [[(∞,1)-module bundle|(∞,1)-line bundles]] over $E$. Consider an [[(∞,1)-functor]] 

$$
  \Gamma^\ast \;\colon \; \mathbf{H}_{/\mathbf{B}GL_1(E)} \to E Mod
$$

to the [[(∞,1)-category of (∞,1)-modules]] over $E$, which form $E$-modules of co-sections of $E$-[[(∞,1)-module bundles]] (generalized [[Thom spectra]]). 

This is well understood for $\mathbf{H} = $ [[∞Grpd]] in which case $\Gamma \simeq \underset{\to}{\lim} \circ i$ is the [[(∞,1)-functor]] [[homotopy colimits]] in $E Mod$ under the canonical embedding $\mathbf{B} GL_1(E) \simeq E Line \hookrightarrow E Mod$. But one can consider similar constructions $\Gamma$ for more general ambient [[(∞,1)-toposes]] $\mathbf{H}$.

+-- {: .num_defn #BivariantCohomologyByHomsOfCoSections}
###### Definition

For $\chi_i \colon X_i \to \mathbf{B}GL_1(E)$ two [[objects]] of $\mathbf{H}_{/\mathbf{B}GL_1(E)}$, the _$(\chi_1,\chi_2)$-[[twisted cohomology|twisted]] bivariant $E$-[[cohomology theory|cohomology]]_ on $(X_1,X_2)$ is 

$$
  E^{\bullet + \chi_2 - \chi_1}(X_1,X_2)
  \;\coloneqq\;
  Hom_{E Mod}\left(\Gamma^\ast_{X_1}\left(\chi_1\right), \Gamma^\ast_{X_2}\left(\chi_2\right)\right)
  \in 
  E Mod
  \,.
$$

=--

+-- {: .num_example}
###### Example

By the general discussion at [[twisted cohomology]], following ([ABG, def. 5.1](#ABG)) we have

* for $X_2 = \ast$ the point, the above bivariant cohomology is the $\chi_1$-twisted $E$-cohomology of $X_1$;

  $$
    E^{\bullet + \chi_1}(X_1, \ast) \simeq E^{\bullet + \chi_1}(X_1)
    \,.
  $$

* for $X_1 = \ast$ the point, the above bivariant cohomology is the $\chi_2$-twisted $E$-[[generalized homology|homology]] of $X_2$;

  $$
    E^{\bullet + \chi_2}(\ast, X_2) \simeq E_{\bullet + \chi_2}(X_2)
    \,.
  $$

=--

+-- {: .num_example}
###### Example

[[KK-theory]] is a model for bivariant twisted [[topological K-theory]] over [[differentiable stacks]] (hence 1-truncated suitably representable objects in $\mathbf{H} = $ [[Smooth∞Grpd]], see [Tu-Xu-LG 03](#TuXuLG03)). According to ([Joachim-Stolz 09, around p. 4](#JoachimStolz09)) the category $KK$ first of all is naturally an [[enriched category]] $\mathbb{KK}$ over the category $\mathcal{S}$ of [[symmetric spectra]]  and as such comes with a symmetric [[monoidal functor|monoidal]] [[enriched functor]]

$$
  \mathbb{KK} \to KU Mod
  \,.
$$


This sends an object to its [[operator K-theory]] spectrum, hence to the $E$-[[dual object|dual]] of the $E$-module of co-sections. 

=--

+-- {: .num_remark}
###### Remark

Generally, one may want to consider in def. \ref{BivariantCohomologyByHomsOfCoSections} the dualized co-section functor

$$
  \Gamma = [\Gamma^\ast(-), E] \;\colon\; \left(\mathbf{H}_{/\mathbf{B}GL_1(E)}\right)^{op} \to E Mod
  \,.
$$

=--

+-- {: .num_example}
###### Example

A [[correspondence]] in $\mathbf{H}_{/\mathbf{B}GL_1(E)}$ 

$$
  \array{
    && Q
    \\
    & {}^{\mathllap{i_1}}\swarrow && \searrow^{\mathrlap{i_2}}
    \\
    X_1 && \swArrow_{\xi} && X_2
    \\
    & {}_{\mathllap{\chi_1}}\searrow && \swarrow_{\mathrlap{\chi_2}}
    \\
    && \mathbf{B}GL_1(E)
  }
$$

is a morphism of "twisted $E$-[[pure motive|motives]]" in that it is a [[correspondence]] in $\mathbf{H}$ between the [[spaces]] $X_1$ and $X_2$ equipped with an $(i_1^\ast \chi_1, i_2^\ast \chi_2)$-twisted bivariant $E$-cohomology [[cocycle]] $\xi$ on the correspondence space $Q$. Under the co-sections / [[Thom spectrum]] functor this is sent to a [[correspondence]]

$$
  \Gamma_{X_1}(\chi_1)
  \stackrel{\xi}{\rightarrow}
  \Gamma_Q(i_2^\ast \chi_2)
  \stackrel{i_2^\ast}{\leftarrow}
  \Gamma_{X_2}(\chi_2)
$$

in $E Mod$. If the wrong-way map of this is [[orientation in generalized cohomology|orientable]] in $E$-cohomology then we may form its [[dual morphism]]/[[Umkehr map]] to obtain the corresponding "[[index]]"

$$
  \Gamma_{X_1}(\chi_1)
   \stackrel{(i_2)_! \xi}{\to}
  \Gamma_{X_2}(\chi_2)
$$

in $E Mod$. Identifying correspondences that yield the same "[[index]]" this way yields a presentation of bivariant cohomology by [[pure motive|motive]]-like structures. 
This is how (equivariant) [[bivariant K-theory]] is presented, at least over manifolds, see at _[KK-theory -- References -- In terms of correspondences](KK-theory#ReferencesInTermsOfCorrespondences)_.

=--

## Related concepts

* [[noncommutative motive]]

* [[motivic quantization]]


## References

A general introduction to bivariant cohomology theories is in 

* {#FultonMacPherson81} [[William Fulton]], [[Robert MacPherson]], _Categorical framework for the study of singular spaces_, Memoirs of the AMS, 243, 1981

A general construction of bivariant theories on [[smooth manifolds]] from [[cohomology theories]] by geometric cycles, generalizing the construction of [[K-homology]] by [[Baum-Douglas geometric cycles]], is in 

* Martin Jakob, _Bivariant theories for smooth manifolds_, Applied Categorical Structures 10 no. 3 (2002)

A similar construction for PL manifolds is in

* S. Buoncristiano, C. P. Rourke and B. J. Sanderson, _A geometric approach to homology theory_, Cambridge Univ. Press, Cambridge, Mass. (1976)

References related to the discusison in _[Axiomatization in homotopy theory](#AxiomatizazionInHomotopyTheory)_ above include the following

* {#ABG} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 

* {#TuXuLG03} [[Jean-Louis Tu]], [[Ping Xu]], [[Camille Laurent-Gengoux]], _Twisted K-theory of differentiable stacks_ ([arXiv:math/0306138](http://arxiv.org/abs/math/0306138))
 

* {#JoachimStolz09} [[Michael Joachim]], [[Stephan Stolz]], _An enrichment of $KK$-theory over the category of symmetric spectra_ M&#252;nster J. of Math. 2 (2009), 143&#8211;182 ([pdf](http://www3.nd.edu/~stolz/KKenrich.pdf))
 

* {#Nuiten13} [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis, August 2013
 
* {#Schreiber14} [[Urs Schreiber]], _[[schreiber:Quantization via Linear homotopy types]]_ ([arXiv:1402.7041](http://arxiv.org/abs/1402.7041))

[^footnote]: Thanks to [[Thomas Nikolaus]] for patiently emphasizing this.

[[!redirects bivariant cohomology theories]]

[[!redirects bivariant homology theory]]
[[!redirects bivariant homology theories]]

[[!redirects bivariant cohomology]]

[[!redirects twisted bivariant cohomology]]
[[!redirects bivariant twisted cohomology]]