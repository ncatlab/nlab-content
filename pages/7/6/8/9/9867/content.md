
#Contents#
* table of contents
{:toc}

## Idea

Where a [[homology theory]] is a [[covariant functor]] and a [[cohomology theory]] is a [[contravariant functor]] on some [[category]] of [[spaces]], a _bivariant cohomology theory_ is a [[bifunctor]], hence a functor of two variables, contravariant in the first, and covariant in the second.

## Axiomatization in homotopy theory
 {#AxiomatizazionInHomotopyTheory}

Here are some notes on a proposal for how to formalize this usefully. (Aspects of this appear in ([Nuiten 13]{#Nuiten}).

Let $E$ be an [[E-∞ ring]], write $GL_1(E)$ for its [[∞-group of units]]. Write $\mathbf{H}_{/\mathbf{B}GL_1(E)}$ for the [[slice (∞,1)-topos]] over the [[delooping]] of this [[abelian ∞-group]]. This is the [[(∞,1)-category]] of [[spaces]] equipped with [[(∞,1)-module bundle|(∞,1)-line bundles]] over $E$. Consider an [[(∞,1)-functor]] 

$$
  \Gamma \;\colon \; \mathbf{H}_{/\mathbf{B}GL_1(E)} \to E Mod
$$

to the [[(∞,1)-category of (∞,1)-modules]] over $E$, which form $E$-modules of co-sections of $E$-[[(∞,1)-module bundles]] (generalized [[Thom spectra]]). 

+-- {: .num_defn}
###### Defintiion

For $\chi_i \colon X_i \to \mathbf{B}GL_1(E)$ two [[objects]] of $\mathbf{H}_{/\mathbf{B}GL_1(E)}$, the $(\chi_1,\chi_2)$-[[twisted cohomology|twisted]] bivariant $E$-cohomology on $(X_1,X_2)$ is 

$$
  Hom_{E Mod}\left(\Gamma_{X_1}\left(\chi_1\right), \Gamma_{X_2}\left(\chi_2\right)\right)
  \in 
  E Mod
  \,.
$$

=--

+-- {: .num_example}
###### Example

By the general discussion at [[twisted cohomology]], following ([ABG, def. 5.1](#ABG)) we have

* for $X_2 = \ast$ the point, the above bivariant cohomology is the $\chi_1$-twisted $E$-cohomology of $X_1$;

* for $X_1 = \ast$ the point, the above bivariant cohomology is the $\chi_2$-twisted $E$-[[generalized homology|homology]] of $X_2$.

=--

+-- {: .num_example}
###### Example

[[KK-theory]] is meant to be a model for bivariant twisted [[topological K-theory]]. Indeed, according to ([Joachim-Stolz 09, around p. 4](#JoachimStolz09)) the category $KK$ first of all is naturally a an [[enriched category]] $\mathbb{KK}$ of the category $\mathcal{S}$ of [[symmetric spectra]]  and as such comes with a symmetric monoidal enriched functor

$$
  \mathbb{KK} \to KU Mod
  \,.
$$

=--


## Examples

* In [[noncommutative topology]]: [[KK-theory]].

* In [[noncommutative algebraic geometry]]: [[bivariant algebraic K-theory]], [[noncommutative motives]].

## References

A general introduction to bivariant cohomology theories is in 

* [[William Fulton]], [[Robert MacPherson]], _Categorical framework for the study of singular spaces_, Memoirs of the AMS, 243, 1981

A general construction of bivariant theories on [[smooth manifolds]] from [[cohomology theories]] by geometric cycles, generalizing the construction of [[K-homology]] by [[Baum-Douglas geometric cycles]], is in 

* Martin Jakob, _Bivariant theories for smooth manifolds_, Applied Categorical Structures 10 no. 3 (2002)

A similar construction for PL manifolds is in

* S. Buoncristiano, C. P. Rourke and B. J. Sanderson, _A geometric approach to homology theory_, Cambridge Univ. Press, Cambridge, Mass. (1976)

References related to the discusison in _[Axiomatization in homotopy theory](#AxiomatizazionInHomotopyTheory)_ above include the following

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 {#ABG}

* [[Michael Joachim]], [[Stephan Stolz]], _An enrichment of $KK$-theory over the category of symmetric spectra_ M&#252;nster J. of Math. 2 (2009), 143&#8211;182 ([pdf](http://www3.nd.edu/~stolz/KKenrich.pdf))
 {#JoachimStolz09}

* [[Joost Nuiten]], Master Thesis 2013
 {#Nuiten}

[[!redirects bivariant cohomology theories]]

[[!redirects bivariant homology theory]]
[[!redirects bivariant homology theories]]

[[!redirects bivariant cohomology]]

