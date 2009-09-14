#Idea#

A _formal scheme_ is a [[scheme]] that looks like a closed subscheme $Y \hookrightarrow X$ together with the [[infinitesimal space|infinitesimal]] neighbourhood of $Y$ in $X$. This infinitesimal neighbourhood is also called the _formal neighbourhood_ or the $\infty$-jet bundle normal to $Y$ (is that last one correct?).

A formal for which $Y$ is an [[affine scheme]] is a [[formal spectrum]].

#Motivation#

Formal [[power series]] [[ring]]s $k[\![x_1,\ldots,x_n]\!]$ are limits of their truncations (e.g. in one variable $k[\![x]\!]/(x^n)$); they can be viewed as completions and they get equipped with a natural filtration and [[adic topology]].

They do not converge as a series (and make sense) in an open set or in any of the standard topologies (e.g. Zariski and complex topology over $\mathbb{Z}$), but they are rather "localized" in an *[[infinitesimal neighborhood|infinitesimal neighborhood]]* of the origin. One would like to be able to talk about functions supported only infinitesimally (in the transverse direction) to a [[closed subscheme]]. The formal schemes of [[Grothendieck]] give a geometric locus a [[ringed space]] corresponding to the information on all infinitesimal neighborhoods. Zariski's theorem on formal functions and establishing the theory of [[formal group]]s were some of the concrete motivations.


#Noetherian formal schemes#

Given any [[ring]] $R$ and an [[ideal]] $I$ of $R$, there is a natural homomorphisms of rings $R/I^{n+1}\to R/I^n$ for all $n\geq 0$. The [[inverse limit]] $\hat{R}:=lim_n R/I^n$ is called the **completion of $R$ at the ideal $I$** or the **$I$-adic completion** of $R$. If $R$ is [[noetherian ring|noetherian]], the completion is noetherian as well. 

If $X$ is a [[scheme]], a [[closed subscheme]] $Y\subset X$ is given by an embedding of topological spaces with the [[comorphism]] $\mathcal{O}_X\to f_*\mathcal{O}_Y$ which is a surjection; but alternatively $\mathcal{O}_Y$ can be recovered from $X$ and the defining sheaf of ideals $\mathcal{I}\subset \mathcal{O}_X$. Then one defines the [[structure sheaf]] of the completion $\mathcal{O}_{\hat{X}}$ as $lim_n \mathcal{O}_X/\mathcal{I}^n$ restricted to $Y$ and the __completion__ $\hat{X} := (Y,\mathcal{O}_{\hat{X}})$. If $X = Spec\,R$ where $R$ is a noetherian $I$-adic ring, and $Y=Spec\,R/I$ then the completion is called the **[[formal spectrum]]** of $R$ denoted

$$
  Spf\,R = \hat{X}
$$ 

(where $R$ is viewed as a topological ring). It is an [[ind-object]] in the [[category]] of [[algebraic scheme]]s, viewed as a formal colimit
$colim_n Spec (R/I^n)$.

A (locally) noetherian formal scheme is a formal completion of a (locally) noetherian scheme along a closed subscheme. Equivalently, a locally noetherian scheme is a locally ringed space which is locally isomorphic to the formal spectrum of a complete separated adic noetherian ring.


#Other approaches# 

The formal spectrum can be extended to a somewhat bigger class of topological rings than the noetherian ones; Grothendieck developed the theory in the generality of [[pseudocompact space|pseudocompact]] topological rings. However, some important rings, e.g. the ring of integers $\mathbb{Z}$, do not have a pseudocompact topology. Thus one could try to consider a more general subcategory of ind-schemes (with at least the requirement that the [[ind-object]] be represented by a diagram where the connecting morphisms are [[closed subscheme|closed immersions of schemes]]); one such approach is outlined in some detail in 

* A. Beilinson, V. Drinfel'd, _Quantization of Hitchin's integrable system and Hecke eigensheaves on Hitchin system_, preliminary version ([pdf](http://www.math.uchicago.edu/~mitya/langlands/hitchin/BD-hitchin.pdf))

Another approach using a certain topological extension of the [[Yoneda lemma]] on $k Alg^{op}$ has been proposed in

* B. Pareigis, R. A. Morris, _Formal groups and Hopf algebras over discrete rings_, Trans. Amer. Math. Soc.  __197__ (1974), 113--129 ([doi](http://dx.doi.org/10.2307/1996930)).

[[Nikolai Durov]] has considered a flexible bigger category (which inludes the usual schemes) of covariant functors from the category of pairs $(R,I)$ where $R$ is a commutative ring and $I$ a [[nilpotent ideal]]; the correspondence between formal groups and [[Lie algebras]] based on Hausdorff series is neatly developed and used in that language; see chapters 7--9 of

* N. Durov, S. Meljanac, A. Samsarov, Z. &#352;koda, _A universal formula for representing Lie algebra generators as formal power series with coefficients in the Weyl algebra_, Journal of Algebra 309, n. 1, 318--359 (2007)
([doi:jalgebra](http://dx.doi.org/10.1016/j.jalgebra.2006.08.025))
([math.RT/0604096](http://front.math.ucdavis.edu/math.RT/0604096)).
 
For another generalization of formal schemes see

* T. Yasuda, _Non-adic formal schemes_, Int. Math. Research Notices 2009: 2417--2475, ([doi:imrn](http://dx.doi.org/10.1093/imrn/rnp021), [arxiv](http://arxiv.org/abs/0711.0434))

In a fundamental article in [[noncommutative algebraic geometry]],

* M. Kapranov, _Noncommutative geometry based on commutator expansions_, [math.AG/9802041](http://arxiv.org/abs/math.AG/9802041),

Kapranov introduced objects which should be interpreted as the infinitesimal neighborhoods of those commutative schemes with a closed immersion into a noncommutative scheme which is locally isomorphic to the spectrum of a free associative algebra. 


#Basic literature#

* A. Grothendieck, _G&#233;om&#233;trie formelle et g&#233;om&#233;trie alg&#233;brique_, FGA 2 (S&#233;minaire Bourbaki, t. 11, 1958/59, no. 182)

* Luc Illusie, _Grothendieck existence theorem in formal geometry_, chapter 8 in Fantechi, Gottsche, Illusie, Kleiman, Nitsure, Vistoli, _Fundamental algebraic geometry, Grothendieck's FGA explained, Math. Surveys and Monographs_ __123__, AMS 2005.

* A. Grothendieck (avec J. Dieudonne), EGA I.10

* A. Grothendieck et al. SGA III.2 (Exp. 7a, P. Gabriel, &#201;tude infinit&#233;simale des sch&#233;mas en groupe et groupes formels; Exp. 7b, P. Gabriel, Groupes formels)

* R. Hartshorne, _Algebraic geometry_, II.9

* M. Demazure, P. Gabriel, _Groupes algebriques_, tome 1 (later volumes never appeared), Mason and Cie, Paris 1970 

For the scheme geometric picture behind the infinitesimal neighborhoods and [[D-modules]] see also

* A. Be&#301;linson, J. Bernstein, J., _A proof of Jantzen conjectures_, in I. M. Gel&#697;fand Seminar, 1--50,
Adv. Soviet Math., 16, Part 1, Amer. Math. Soc., Providence, RI, 1993 (MR1237825 (95a:22022))


[[!redirects formal schemes]]