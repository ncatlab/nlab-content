


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **bornological topos** is a [[Grothendieck topos]] based on the concept of a bounded sequence and was proposed by [[William Lawvere]] in unpublished lectures in 1983 as a convenient category to do [[functional analysis]] in.


## Definition

Let $\mathcal{C}$ be the category of [[countable set|countable sets]]. The _bornological topos_ $\mathcal{B}$ is the category of finite product preserving presheaves on $\mathcal{C}$.

## Properties

* Equivalently, $\mathcal{B}$ is the topos of sheaves on $\mathcal{C}$ for the _(finite) disjoint covering topology_ with coverings the finite families $(X_i\to Y)_{i\in I}$ , such that $\sum_{i\in I} X_i\to Y$ is an isomorphism.

* In the work of Espa&#241;ol et al., $\mathcal{B}$ is accessed as a subtopos of the topos of actions of the monoid of endomorphisms of $N$.

* $\mathcal{B}$ contains the category of (Kolmogorov) [[bornological set|bornological spaces]] as a full reflective subcategory (cf. Espa&#241;ol-Lamb&#225;n [2002](#EspanolLamban02)).

* The object $R_D$ of [[Dedekind real numbers]] of $\mathcal{B}$ is the space $l^\infty$ of bounded sequences of real numbers (cf. Espa&#241;ol-M&#237;nguez [2001](#Espanol-Minguez01)).

* " _The category of modules over the Dedekind real number object includes all the inductive limits of Banach spaces as a full subcategory, but at the same time is itself a Grothendieck AB5 Abelian category with the accompanying exactness properties._ " (Lawvere [2008](#Lawvere08), p.15).
Thus " **functional analysis becomes linear algebra** " in the bornological topos (Lawvere [1994](#Lawvere94), p.10).

## Remark: bornology and cohesiveness

The bornological topos is the [[Gaeta topos]] on $\mathcal{C}$ and as such fits Lawvere's paradigm of doing abstract "algebraic geometry" (cf. Lawvere [1986](#Lawvere86), p.17). In particular, the geometry and cohesiveness of the objects $X$ in $\mathcal{B}$ arises _covariantly_ from the basic figure shape of a 'bounded' sequence $A$ via maps $A\to X$.

That bornology provides in the context of functional analysis "_a more basic notion of cohesiveness_" than the usual topological neighborhood concept and contravariant function algebra concept based on it is argued in Lawvere ([1997](#Lawvere97), pp.3f).

Although the bornological topos can be regarded as a cohesive category of "spaces" in a broad sense, it doesn't satisfy Lawvere's _axiomatic cohesion_ since it lacks the required left adjoint components functor $\Pi:\mathcal{B}\to Set$ (cf. Lawvere [2008](#Lawvere08)).

## Related entries

* [[bornology]]

* [[Johnstone's topological topos|topological topos]]

* [[topos of recursive sets|recursive topos]]

* [[cohesion]]


## References

* L. Espa&#241;ol, _Extended real number object in the bornological topos_ , talk CT07 Carvoeiro 2007. ([pdf-slides](http://www.mat.uc.pt/~categ/ct2007/slides/espanol.pdf))

* L. Espa&#241;ol, L. Lamb&#225;n, _A tensor-hom adjunction in a topos related to vector topologies and bornologies_ , Journal of Pure and Applied Algebra **154** (2000) pp.143-158. (doi:[10.1016/S0022-4049(99)00188-7](http://dx.doi.org/10.1016/S0022-4049(99%2900188-7))

* {#Espanol-Lamban02}L. Espa&#241;ol, L. Lamb&#225;n, _On bornologies, locales and toposes of M-sets_ , Journal of Pure and Applied Algebra **176** (2002) pp.113&#8211;125. (doi:[10.1016/S0022-4049(02)00047-6](http://dx.doi.org/10.1016/S0022-4049(02%2900047-6))

* {#Espanol-Minguez01}L. Espa&#241;ol, M. C. M&#237;nguez, _Cortaduras Para $l^\infty$_ , pp.375-390 in Espa&#241;ol, Varona (eds.), _Margarita Mathematica en Memoria de Jos&#233; Javier (Chicho) Guadalupe Hern&#225;ndez_ , Universidad de La Rioja 2001. ([pdf](http://www.emis.de/proceedings/Chicho2001/Espanol-Minguez.pdf))

* {#Lawvere86}[[F. William Lawvere]], _Taking Categories Seriously_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.147-178. Reprinted as TAC Reprint no.8 (2005) pp.1-24. ([pdf](ftp://ftp.tac.mta.ca/tac/html/tac/reprints/articles/8/tr8.pdf))

* [[F. William Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Contemporary Mathematics **92** (1989) pp.261-299. ([Google Books link](https://books.google.com.au/books?id=VxAcCAAAQBAJ&pg=PA261); doi:[10.1090/conm/092/1003203](http://dx.doi.org/10.1090/conm/092/1003203)).

* {#Lawvere94}[[F. William Lawvere]], _Cohesive Toposes and Cantor's 'lauter Einsen'_ , Phil. Math. **2** no.3 (1994) pp.5-15.

* {#Lawvere97}[[F. William Lawvere]], _Volterra's functionals and covariant cohesion of space_ , in _Proceedings of the May 1997 Meeting in Perugia_ , Perugia Studies in Mathematics 1997.

* {#Lawvere08}[[F. William Lawvere]], _[[Cohesive Toposes -- Combinatorial and Infinitesimal Cases]]_, Como Ms. 2008.

* [[F. William Lawvere]], Section 2 of _Toposes generated by codiscrete objects in combinatorial topology and functional analysis_, Reprints in Theory and Applications of Categories, No. 27 (2021) pp. 1-11, [pdf](http://tac.mta.ca/tac/reprints/articles/27/tr27abs.html).


[[!redirects Bornological topos]]



