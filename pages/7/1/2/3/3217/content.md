
#Contents#
* table of contents
{:toc} 


## Definition

Let $M$ be an $n$-[[dimension]]al topological [[manifold]]. The decomposition of $M$ as a disjoint union of connected subsets $V_\alpha$, called **leaves**, 

$$ M  = \cup_\alpha V_\alpha $$

is called a **foliation** if there is a cover of $M$ by a collection of "special" charts of the form $(U, \phi)$, $\phi = (\phi_1,\ldots,\phi_n) : U \to \mathbb{R}^n$ such that for each "special" chart and each $\alpha$ there is a number $p = p\leq n$, called the dimension of the foliation, such that the intersection of any given leaf $V_\alpha$ with $U$ is one of the level sets, i.e. the solution of the system $\phi_r(x) = const = const(r,U,\alpha)$ for all $r\gt p$.

If the manifold is a [[smooth manifold]], the charts are required to be smooth too. In the smooth case, the $p$-dimensional foliations with underlying manifold $M$ are in 1-1 correspondence with [[integrable distributions]] of hyperplanes of dimension $p$ in tangent bundle of $N$. 
 
## Examples

* Every [[Lie groupoid]] gives a folitation on its space of [[object]]s: the leaves are the [[orbit]]s. Conversely, every regular foliation gives rise to its [[holonomy groupoid]]. This is a (not necessarily Hausdorff) Lie groupoid whose orbits are the leaves of the original foliation, and which in some sense is minimal with this condition.

* Every [[Poisson manifold]] has a canonical structure of a foliation whose leaves are its maximal [[symplectic manifold|symplectic]] submanifolds, called *symplectic leaves*.

## Properties

The set of components of a foliation is typically non-[[Hausdorff space|Hausdorff]], which is one of the motivations of the [[Alain Connes|Connes]]-style [[noncommutative geometry]]. 

There is a theory of [[characteristic class]]es for foliations. A most well known example is the Godbillon-Vey characteristic class. 

## References

* &#1044;. &#1041;. &#1060;&#1091;&#1082;&#1089;, _&#1057;&#1083;&#1086;&#1077;&#1085;&#1080;&#1103;_, &#1048;&#1090;&#1086;&#1075;&#1080; &#1085;&#1072;&#1091;&#1082;&#1080; &#1080; &#1090;&#1077;&#1093;&#1085;. &#1057;&#1077;&#1088;. &#1040;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;. &#1058;&#1086;&#1087;&#1086;&#1083;. &#1043;&#1077;&#1086;&#1084;., 1981,  &#1090;&#1086;&#1084; __18__, &#1089;&#1090;&#1088;. 151&#8211;-213, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=inta&paperid=93&what=fullt&option_lang=rus)

* D. B. Fuks, _Cohomology of infinite-dimensional Lie algebras and characteristic classes of foliations_ (book, Rus. and Eng. versions)

* [[Ieke Moerdijk]], [[Janez Mrčun]], _Introduction to foliations and Lie groupoids_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0

* [wikipedia](http://en.wikipedia.org/wiki/Foliation), Springer Online Enc. of Math.: [foliation](http://eom.springer.de/F/f040740.htm)

* I. M. Gel&#697;fand, B. L. Fe&#301;gin, D. B. Fuks, _Cohomology of the Lie algebra of formal vector fields with coefficients in its dual space and variations of characteristic classes of foliations, Funkcional. Anal. i Prilo&#382;en.  8  (1974), no. 2, 13--29 (Russian original [pdf]())

* Claude Godbillon, _Cohomologies d'alg&#232;bres de Lie de champs de vecteurs formels_, S&#233;minaire Bourbaki, 25&#232;me ann&#233;e (1972/1973), Exp. No. 421, pp. 69--87. Lecture Notes in Math. __383__, Springer 1974. 

* &#1048;. &#1052;. &#1043;&#1077;&#1083;&#1100;&#1092;&#1072;&#1085;&#1076;, &#1044;. &#1041;. &#1060;&#1091;&#1082;&#1089;, _&#1050;&#1086;&#1075;&#1086;&#1084;&#1086;&#1083;&#1086;&#1075;&#1080;&#1080; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1099; &#1051;&#1080; &#1092;&#1086;&#1088;&#1084;&#1072;&#1083;&#1100;&#1085;&#1099;&#1093; &#1074;&#1077;&#1082;&#1090;&#1086;&#1088;&#1085;&#1099;&#1093; &#1087;&#1086;&#1083;&#1077;&#1081;_, &#1048;&#1079;&#1074;. &#1040;&#1053; &#1057;&#1057;&#1057;&#1056;. &#1057;&#1077;&#1088;. &#1084;&#1072;&#1090;&#1077;&#1084;., 1970,  __34__, &#1074;. 2, &#1089;&#1090;&#1088;. 322&#8211;-337, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=2418&what=fullt&option_lang=rus)

* A. Connes, H. Moscovici, _Modular Hecke algebras and their Hopf symmetry_, Mosc. Math. J., 4:1 (2004), 67&#8211;109; [math.QA/0301089](http://arxiv.org/abs/math/0301089), [ams](http://www.ams.org/distribution/mmj/vol4-1-2004/connes_moscovici_1.pdf); _Hopf algebras, cyclic cohomology and the transverse index theory_, [math.DG/9806109](http://arxiv.org/abs/math/9806109), Comm. Math. Phys. __198__, n.1, 1998; _Rankin-Cohen brackets and the Hopf algebra of transverse geometry_, Mosc. Math. J., 4:1 (2004), 111&#8211;130

* W. P. Thurston, _Existence of codimension-one foliations_,  Ann. of Math. (2) __104__  (1976), no. 2, 249--268 ([doi](http://dx.doi.org/10.1007/BF02566730)); _Foliations and groups of diffeomorphisms_, Bull. Amer. Math. Soc. 80  (1974), 304--307 ([pdf](http://www.ams.org/bull/1974-80-02/S0002-9904-1974-13475-0/S0002-9904-1974-13475-0.pdf)); _The theory of foliations of codimension greater than one_,  Comment. Math. Helv.  49  (1974), 214--231 ([link](http://resolver.sub.uni-goettingen.de/purl?GDZPPN00206135X))

* Yu. A. Kordyukov, _Index theory and non-commutative geometry on foliated manifolds_, Russian Math. Surveys, 64:2 (2009), 273&#8211;391 (original: &#1059;&#1052;&#1053;, 64:2(386) (2009), 73&#8211;202)

[[!redirects foliations]]