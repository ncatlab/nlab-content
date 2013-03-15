
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc} 

## Idea

A _foliation_ of a [[manifold]] $X$ is a decomposition into [[submanifolds]] in a locally well-behaved way. These submanifolds are called the _leaves_ of the foliation and one says that $X$ is _foliated by the leaves_.

For [[smooth manifolds]] smooth foliations are decomposition into [[immersion|immersed]] [[submanifolds]] such that locally this is by the [[fibers]] of a [[submersion]] (the projection to the [[space of leaves]]).

For [[smooth manifolds]] $X$, foliations arise (and this was the historical motivation for introducing them in ([Ehresmann](#Ehresmann)), ([Reeb](#Reeb))) from subbundles of the [[tangent bundle]] $E \hookrightarrow T X$ which are [[integrable distributions]] (in that the [[Lie bracket]] of [[vector fields]] that are [[sections]] of $E$ is again a section of $E$): the leaves are the submanifolds whose tangent vectors are sections of $E$. If one thinks of $E$ as encoding a [[differential equation]] then the leaves are the solution spaces to this equation.

Expressed in terms of [[higher Lie theory]] such an integrable distribution is a sub-[[Lie algebroid]] of the [[tangent Lie algebroid]] of $X$. Accordingly, under [[Lie integration]] of this structure foliations of $X$ are also equivalently encodes as [[Lie groupoids]] whose space of objects is $X$ and whose [[orbits]] are the leaves of the foliation.

Moreover, foliations are classified by [[Cech cohomology]] [[cocycles]] with coefficients in a [[topological groupoid]]/[[Lie groupoid]] called the _[[Haefliger groupoid]]_. These relations make foliation theory of sub-topic of [[Lie groupoid]]-theory. See also at _[[motivation for higher differential geometry]]_.

The Haefliger groupoids in fact classifies structures slightly more general than foliations: _[[Haefliger structures]]_.

## Definition

There are several equivalent definitions of foliations.

### Original definition

Let $M$ be an $n$-[[dimension|dimensional]] [[topological manifold]]. A decomposition of $M$ as a [[disjoint union]] of [[connected topological space|connected]] subsets $V_\alpha$, called **leaves**, 

$$ M  = \cup_\alpha V_\alpha $$

is called a **foliation** if there is a [[cover]] of $M$ by a collection of "special" [[charts]] of the form $(U, \phi)$, $\phi = (\phi_1,\ldots,\phi_n) : U \to \mathbb{R}^n$ such that for each "special" chart and each $\alpha$ there is a number $p\leq n$, called the _dimension of the foliation_, such that the intersection of any given leaf $V_\alpha$ with $U$ is one of the level sets, i.e. the solution of the system $\phi_r(x) = const = const(r,U,\alpha)$ for all $r\gt p$.

If the manifold is a [[smooth manifold]], the charts may be required to be smooth too, to obtain the notion of a _smooth foliation_ or _folitation in [[differential geometry]]_. In this case, the $p$-dimensional foliations with underlying manifold $X$ are in 1-1 correspondence with [[integrable distributions]] of hyperplanes of dimension $p$ in the [[tangent bundle]] of $X$. 

### Alternative definitions

The following equivalent definitions and their relation are discussed for instance in ([IfLg, 1.2](#MoerdijkMrcun)).

+-- {: .num_defn}
###### Definition

A **foliation atlas** of a [[manifold]] $X$ of [[dimension]] $n$ and leaf-[[codimension]] $q$ is an [[atlas]] $\{\phi_i^{-1}: R^n \to X\}_i$ such that the transition functions are globally of the form 

$$
  \phi_{i j} : (x,y) \mapsto (g_{i j}(x,y), h_{i j}(y))
$$

with respect to the canonical decomposition $\mathbb{R}^n = \mathbb{R}^{n-q} \times \mathbb{R}^q$.

$$
  \array{
    \mathbb{R}^n &\stackrel{\phi_{i j}}{\to}& \mathbb{R}^n && 
    \\
    \downarrow && \downarrow 
    \\
    \mathbb{R}^q &\stackrel{h_{i j}}{\to}& \mathbb{R}^q
  }
  \,.
$$

=--

+-- {: .num_defn #FoliationAtlasByLocalSubmersions}
###### Definition

A **foliation atlas** of a [[manifold]] $X$ of [[dimension]] $n$ and leaf-[[codimension]] $q$ is an [[open cover]] $\{U_i \to X\}_i$ of $X$ equipped with [[submersions]] $\{ s_i \colon U_i \to \mathbb{R}^q \}$
such that there exists [[diffeomorphisms]]

$$
   \gamma_{i j} \colon s_j(U_i \cap U_j) \to s_i(U_i \cap U_j)
$$

satisfying on each $U_i \cap U_j$ the condition

$$
  s_i = \gamma_{i j} \circ s_j 
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Given a foliation atlas as in def. \ref{FoliationAtlasByLocalSubmersions},
the [[diffeomorphisms]] $\{\gamma_{i j}\}_{i,j}$ satisfy the [[Cech cohomology|Cech]] [[cocycle]] condition

$$
   \gamma_{i j} \circ \gamma_{j k} = \gamma_{i k}
  \,.
$$

This is called the **[[Haefliger cocycle]]** of the foliation atlas.

=-- 

+-- {: .num_defn }
###### Definition

A smooth foliation of a [[smooth manifold]] $X$ is equivalently an [[integrable distribution]] $E \hookrightarrow T X$.

=--

## Examples

+-- {: .num_example}
###### Example

For $X \to Y$ a [[submersion]] of [[smooth manifolds]], the connected [[fibers]] of the submersion constitute a foliation of $X$ whose [[codimension]] is the [[dimension]] of $Y$. Foliations of this form are called **simple foliations**.

=--

+-- {: .num_example}
###### Example

Every [[Lie groupoid]] gives a folitation on its space of [[objects]]: the leaves are the [[orbits]]. Conversely, every regular foliation gives rise to its [[holonomy groupoid]]. This is a (not necessarily Hausdorff) Lie groupoid whose orbits are the leaves of the original foliation, and which in some sense is minimal with this condition.

=--

+-- {: .num_example}
###### Example

Every [[Poisson manifold]] has a canonical structure of a foliation whose leaves are its maximal [[symplectic manifold|symplectic]] submanifolds, called *[[symplectic leaves]]*.

=--
## Properties

### Leaf space

The set of components of a foliation is typically non-[[Hausdorff space|Hausdorff]], which is one of the motivations of the [[Alain Connes|Connes]]-style [[noncommutative geometry]]. 

### Classification

Folitation are classified by the [[Haefliger groupoid]]. See at _[[Haefliger theorem]]_.

### Characteristic classes

There is a theory of [[characteristic classes]] for foliations. A most well known example is the Godbillon-Vey characteristic class. 

## Related concepts

* [[orbifold]]

* [[higher differential geometry applied to plain differential geometry]]

## References

The notion of foliated manifolds was introduced in the 1950s, motivated from [[partial differential equation]] theory, in 


* [[Charles Ehresmann]], ...

* Reeb, ...

* [[Eli Cartan]], _Sur l'int&#233;gration des &#233;quations diff&#233;rentiels completement int&#233;grable_, Oeuvres Compl&#232;tes, Pt. II, Vol. I, 555-561.

A discussion in [[differential geometry]] is in

* Robert Hermann, _On the differential geometry of foliations_, Annals of Mathematics, Second Series, Vol. 72, No. 3 ([JSTOR](http://www.jstor.org/stable/1970226))

A textbook on the modern formulation in [[Lie groupoid]] theory is 

* [[Ieke Moerdijk]], [[Janez Mrčun]], _[[Introduction to foliations and Lie groupoids]]_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0
 {#MoerdijkMrcun}


See als

* &#1044;. &#1041;. &#1060;&#1091;&#1082;&#1089;, _&#1057;&#1083;&#1086;&#1077;&#1085;&#1080;&#1103;_, &#1048;&#1090;&#1086;&#1075;&#1080; &#1085;&#1072;&#1091;&#1082;&#1080; &#1080; &#1090;&#1077;&#1093;&#1085;. &#1057;&#1077;&#1088;. &#1040;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;. &#1058;&#1086;&#1087;&#1086;&#1083;. &#1043;&#1077;&#1086;&#1084;., 1981,  &#1090;&#1086;&#1084; __18__, &#1089;&#1090;&#1088;. 151&#8211;-213, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=inta&paperid=93&what=fullt&option_lang=rus)

* D. B. Fuks, _Cohomology of infinite-dimensional Lie algebras and characteristic classes of foliations_ (book, Rus. and Eng. versions)


* [wikipedia](http://en.wikipedia.org/wiki/Foliation), Springer Online Enc. of Math.: [foliation](http://eom.springer.de/F/f040740.htm)

* I. M. Gel&#697;fand, B. L. Fe&#301;gin, D. B. Fuks, _Cohomology of the Lie algebra of formal vector fields with coefficients in its dual space and variations of characteristic classes of foliations, Funkcional. Anal. i Prilo&#382;en.  8  (1974), no. 2, 13--29 (Russian original [pdf]())

* Claude Godbillon, _Cohomologies d'alg&#232;bres de Lie de champs de vecteurs formels_, S&#233;minaire Bourbaki, 25&#232;me ann&#233;e (1972/1973), Exp. No. 421, pp. 69--87. Lecture Notes in Math. __383__, Springer 1974. 

* &#1048;. &#1052;. &#1043;&#1077;&#1083;&#1100;&#1092;&#1072;&#1085;&#1076;, &#1044;. &#1041;. &#1060;&#1091;&#1082;&#1089;, _&#1050;&#1086;&#1075;&#1086;&#1084;&#1086;&#1083;&#1086;&#1075;&#1080;&#1080; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1099; &#1051;&#1080; &#1092;&#1086;&#1088;&#1084;&#1072;&#1083;&#1100;&#1085;&#1099;&#1093; &#1074;&#1077;&#1082;&#1090;&#1086;&#1088;&#1085;&#1099;&#1093; &#1087;&#1086;&#1083;&#1077;&#1081;_, &#1048;&#1079;&#1074;. &#1040;&#1053; &#1057;&#1057;&#1057;&#1056;. &#1057;&#1077;&#1088;. &#1084;&#1072;&#1090;&#1077;&#1084;., 1970,  __34__, &#1074;. 2, &#1089;&#1090;&#1088;. 322&#8211;-337, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=2418&what=fullt&option_lang=rus)

* A. Connes, H. Moscovici, _Modular Hecke algebras and their Hopf symmetry_, Mosc. Math. J., 4:1 (2004), 67&#8211;109; [math.QA/0301089](http://arxiv.org/abs/math/0301089), [ams](http://www.ams.org/distribution/mmj/vol4-1-2004/connes_moscovici_1.pdf); _Hopf algebras, cyclic cohomology and the transverse index theory_, [math.DG/9806109](http://arxiv.org/abs/math/9806109), Comm. Math. Phys. __198__, n.1, 1998; _Rankin-Cohen brackets and the Hopf algebra of transverse geometry_, Mosc. Math. J., 4:1 (2004), 111&#8211;130

* W. P. Thurston, _Existence of codimension-one foliations_,  Ann. of Math. (2) __104__  (1976), no. 2, 249--268 ([doi](http://dx.doi.org/10.1007/BF02566730)); _Foliations and groups of diffeomorphisms_, Bull. Amer. Math. Soc. 80  (1974), 304--307 ([pdf](http://www.ams.org/bull/1974-80-02/S0002-9904-1974-13475-0/S0002-9904-1974-13475-0.pdf)); _The theory of foliations of codimension greater than one_,  Comment. Math. Helv.  49  (1974), 214--231 ([link](http://resolver.sub.uni-goettingen.de/purl?GDZPPN00206135X))

* Yu. A. Kordyukov, _Index theory and non-commutative geometry on foliated manifolds_, Russian Math. Surveys, 64:2 (2009), 273&#8211;391 (original: &#1059;&#1052;&#1053;, 64:2(386) (2009), 73&#8211;202)


[[!redirects foliations]]

[[!redirects leaf space]]
[[!redirects leaf spaces]]

[[!redirects space of leaves]]
[[!redirects spaces of leaves]]

[[!redirects foliation theory]]
