
# Contents
* table of contents
{: toc}

## Idea

A __Morita context__ or, in some authors (e.g. Bass) the __pre-equivalence data__ is a generalization of [[Morita equivalence]] between [[categories of modules]]. In the case of right [[modules]], for two [[associative algebras|associative k-algebras]] (or, in the case of $k = \mathbb{Z}$, [[rings]]) $A$ and $B$, it consists of [[bimodules]] ${}_A P_B$, ${}_B Q_A$, and bimodule [[homomorphisms]]
$f: P\otimes Q\to A$, $g: Q\otimes P\to B$ satisfying mixed [[associativity]] conditions.


## Properties

Theorem. (Bass II.3.4) If $f$ is surjective, then:

(i) $f$ is an isomorphism

(ii) $P$ and $Q$ are generators in the categories of $A$-modules

(iii) $P$ and $Q$ are finitely generated and projective

(iv) $g$ induces isomorphisms of bimodules $P\cong Hom_B(Q,B)$ and
$Q\cong Hom_B(P,B)$

(v) homomorphisms of $A$-algebras $End_B(P)\leftarrow A\rightarrow End_B(Q)$ are isomorphisms


(Bass II.4.1) A Morita context can be constructed from an $A$-algebra $B$ and a right $B$-module $P$. Then set $A = End_B(P)$ and $Q=Hom_B(P,B)$. Then $f = f_P$ and $g = g_P$ are defined by $(b q) p = b (q p)$ and $(q a) p = q(a p)$. 

(Bass II.4.4) (i) $f_P$ s surjective iff $P$ is finitely generated projective $B$-module. Then $f_P$ s iso.

(ii) $g_P$ is surjective iff $P$ s a generator of $mod_B$, then $g_P$ is iso

(iii) The Morita context $(A,B,P,Q,f,g)$ is a Morita equivalence iff $P$ is both projective and a generator. Then $\otimes_P : mod_A\to mod_B$ and its right adjoint $Hom_B(P,-)$ form the equivalence.


## Related entries

* [[Morita equivalence]], [[Eilenberg-Watts theorem]]


## Literature

* [[Hyman Bass]], _Algebraic K-theory_, chapter 2
* [[Tomasz Brzeziński]], Adrian Vazquez Marquez, Joost Vercruysse, _The Eilenberg-Moore category and a Beck-type theorem for a Morita context_, Appl. Categ. Structures __19__ (2011), no. 5, 821&#8211;858 [MR2836546](http://www.ams.org/mathscinet-getitem?mr=2836546)
[doi](http://dx.doi.org/10.1007/s10485-009-9217-0)
* Bruno J. M&#252;ller, _The quotient category of a Morita context_, J. Algebra __28__ (1974), 389&#8211;407 [MR0447336](http://www.ams.org/mathscinet-getitem?mr=0447336) <a href="http://dx.doi.org/10.1016/0021-8693(74)90048-9">doi</a> 
* A. I. Kashu, _On equivalence of some subcategories of modules in Morita contexts_, Discrete Math. 2003, no. 3, 46&#8211;53, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=adm&paperid=383&what=fullt&option_lang=rus)
* Y. Doi, _Generalized smash products and Morita contexts for arbitrary Hopf algebras_, in: J. Bergen, S. Montgomery (Eds.), Advances in Hopf algebras, in: Lecture Notes in Pure and Appl. Math. __158__, Dekker 1994 [doi](https://doi.org/10.1016/j.jalgebra.2004.02.002)
* S.Caenepeel, J.Vercruysse, Shuanhong Wang, _Morita theory for corings and cleft entwining structures_, J. Algebra __276__1 (2004) 210-235 [doi](https://doi.org/10.1016/j.jalgebra.2004.02.002)

There are generalizations in more general bicategories:

* L. El Kaoutit. Wide Morita Contexts in Bicategories. Arab. J. Sci. Eng.
__33__, (2008), 153&#8211;173
* Bertalan Pecsi, _On Morita context in bicategories_, [pdf](http://www.renyi.hu/~aladar/MrtCtx.pdf)

category: algebra


[[!redirects Morita context]]
[[!redirects Morita contexts]]
