
#Contents#
* table of contents
{:toc}


## Motivation

Gabber and Ramero have developed a chapter in abstract algebra and [[algebraic geometry]] which should, in the style of Grothendieck's theory of [[schemes]], capture some of the ideas of 

* [[Gerd Faltings]], _Almost &#233;tale extensions_,  Cohomologies p-adiques et applications arithmétiques (II), Astérisque no. 279  (2002), p. 185-270 ([numdam:AST_2002__279__185_0](http://www.numdam.org/item/AST_2002__279__185_0))

To this aim they define a notion of almost ring/algebra, almost module, and finally, __almost scheme__. The framework is akin to many ideas in [[noncommutative algebraic geometry]] and in particular uses localization theory (compare also the generalized algebraic geometry of [[Nikolai Durov]]).


## Definitions

One starts with a "basic setup" consisting of a fixed _commutative_ unital ("[[base ring|base]]") ring $V$ containing an ideal $I$ such that $I^2 = I$. Usually one also assumes that $\tilde{I} := I \otimes_V I V$ is a flat $V$-module. A $V$-module $M$ is __almost zero__ if $IM=0$. A morphism $f:M\to N$ of $V$-modules is __almost isomorphism__ if $Ker f$ and $Coker f$ are almost zero, or equivalently if $\tilde{I}\otimes_V f : \tilde{I}\otimes_V M\to \tilde{I}\otimes_V N$ is an isomorphism. Almost isomorphisms form a category of fractions in $V-Mod$. The full subcategory $\Sigma$ of $V-Mod$ of $V$-modules which are almost isomorphic to $0$ is a Serre subcategory of $V-Mod$, hence one can construct the quotient category $V^a-Mod := V-Mod/\Sigma$ with the localization functor $Q^* : V-Mod\to V-Mod/\Sigma$; the image of $V$ in $V-Mod/\Sigma$ is denoted by $V^a$. The usual tensor product on $V-Mod$ induces a tensor product on $V^a-Mod$ making it into an abelian symmetric monoidal category. An __almost algebra__ is a commutative monoid in this tensor category; almost algebras form a category $V^a-Alg$; in the usual way one defines the (categories of) left and right (unital or not) modules over any given almost algebra. 

An __affine almost scheme__ is just an object of an opposite category to $V^a-Alg$. A number of Grothendieck topologies are available on the category of affine almost schemes $V^a-Aff$; leading to the notions of locally affine spaces in these topologies; or better in relative version $R^a-Aff = (R^a-Alg)^{op}$ where $R$ is a $V$-algebra. By convention, the default topology is an appropriate version of flat topology, leading to the site $(R^a-Aff)_{fpqc}$. An __almost $R$-scheme__ is by the definition a sheaf of sets on $(R^a-Aff)_{fpqc}$. 

More general "basic setups" in terms of topoi are also considered in the book. 

##Literature##

* [[Ofer Gabber]], Lorenzo Ramero, _Almost Ring Theory_, Lec. Notes in Math. 1800, Springer 2003. 

Abstract of the first arXiv release (51 pages [math.0002064](http://arxiv.org/abs/math/0002064))

>The categories of almost modules and almost algebras are introduced as a convenient setting for the development of Faltings' method of almost etale extensions. After some preliminaries of general "almost homological algebra" we construct the almost version of the cotangent complex and we use it to generalise some results of Faltings on the lifting of almost etale morphisms and almost etale algebras over nilpotent extensions. We also study the "almost trace" of an almost flat and almost finitely presented morphism, in particular we show that the almost trace is (almost) perfect if and only if the morphism is almost etale. Finally we study some cases of non-flat descent for almost rings, and establish the invariance of almost etale morphisms under Frobenius. 

Abstract of 6th public release at [arXiv:math/0201175] (http://arxiv.org/abs/math/0201175) (about 230 pages)

>We develop almost ring theory, which is a domain of mathematics somewhere halfway between ring theory and category theory (whence the difficulty of finding appropriate MSC-class numbers). We apply this theory to valuation theory and to p-adic analytic geometry. You should really have a look at the introductions (each chapter has one). 

In the introduction (6th public release), the authors heuristically place their work in the general field of _abstract algebraic geometry_:

>The purpose of the game is to reconstruct in this new framework as much as possible (and useful) of classical linear and commutative algebra. Essentially, this is the same as the ideology informing Deligne's paper [[Catégories Tannakiennes]], which sets out to develop algebraic geometry in the context of abstract tannakian categories. We could also claim an even earlier ancestry, in that some of the leading motifs resonating throughout our text, can be traced as far back as Gabriel's memoir [[Des catégories abéliennes]].

>In evoking Deligne's and Gabriel's works, we have unveiled another source of motivation whose influence has steadily grown throughout the long gestation of our paper. Namely, we have come to view almost ring theory as a contribution to that expanding body of research of still uncertain range and shifting boundaries, that we could call "abstract algebraic geometry". We would like to encompass under this label several heterogeneous developments: notably, it should include various versions of non-commutative geometry that have been proposed in the last twenty years, but also the relative schemes of M.HAKIM, _Topos annel&#233;s et sch&#233;mas relatifs_, Springer Ergebnisse Math. Grenz. 64 (1972), as well as Deligne's ideas for algebraic geometry over symmetric monoidal categories.

> The common thread loosely unifying these works is the realization that "geometric spaces" do not necessarily consist of set-theoretical points, and - perhaps more importantly -functions on such "spaces" do not necessarily form (sheaves of) commutative rings. Much effort has been devoted to extending the reach of geometric intuition to non-commutative algebras; alternatively, one can retain commutativity, but allow "structure sheaves" which take values in tensor categories other than the category of rings. As a case in point, to any given almost ring $A$ one can attach its spectrum $Spec A$, which is just $A$ viewed as an object of the opposite of the category $V^a-Alg$. $Spec A$ has even a natural flat topology, which allows to define more general almost schemes by gluing (i.e. taking colimits of) diagrams of affine spectra; all this is explained in section 5.7, where we also introduce quasi-projective almost schemes and investigate some basic properties of the smooth locus of a quasi-projective almost scheme. By way of illustration, these generalities are applied in section 5.8 in order to solve a deformation problem for torsors over affine almost group schemes; let us stress that the problem in question is stated purely in terms of affine objects (i.e. almost rings and "almost Hopf algebras"), but the solution requires the introduction of certain auxiliary almost schemes that are not affine.

## Related concepts

* [[almost module]]

[[!redirects almost schemes]]