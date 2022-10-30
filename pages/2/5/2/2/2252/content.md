
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _formal scheme_ is a [[formal neighbourhood]] of a [[scheme]], a scheme with infinitesimal thickening.

Generally this may be formalized via [[ind-objects]] of schemes.
Hence regarded as a [[sheaf]] on [[affine schemes]], a formal scheme is a [[filtered colimit]] of ordinary schemes (e.g. [Strickland 00, section 4](#Strickland00)).

Regarded as a [[locally ringed space]] a formal scheme has the underlying [[topological space]] of an ordinary [[scheme]], but its [[structure sheaf]] contains extra nilpotent elements.

## Motivation

Formal [[power series]] [[ring]]s $k[\![x_1,\ldots,x_n]\!]$ are limits of their truncations (e.g. in one variable $k[\![x]\!]/(x^n)$); they can be viewed as completions and they get equipped with a natural filtration and [[adic topology]].

They do not converge as a series (and make sense) in an open set or in any of the standard topologies (e.g. Zariski and complex topology over $\mathbb{Z}$), but they are rather "localized" in an *[[infinitesimal neighborhood|infinitesimal neighborhood]]* of the origin. One would like to be able to talk about functions supported only infinitesimally (in the transverse direction) to a [[closed subscheme]]. The formal schemes of [[Grothendieck]] are [[ringed spaces]] containing the information on all infinitesimal neighborhoods. Zariski's theorem on formal functions and establishing the theory of [[formal group]]s were some of the concrete motivations.

## Definition

There are roughly four equivalent definitions of a $k$-formal scheme for a field $k$ (check this):

Let $Mf_k$ denote the category of finite dimensional $k$-rings (=$k$-algebras which are rings).

1. A $k$-scheme is called a $k$_-formal scheme_ if it is is equivalent to a [[filtered colimit|codirected limit]] of finite (affine) $k$-schemes.

1. A $k$-scheme is a $k$-formal scheme if it is presented by a [[profinite group|profinite]] $k$-ring; i.e a $k$-ring which is the limit of topologically discrete quotients which are finite $k$-rings. If $A$ is such a topological $k$-ring $Spf_k(A)(R)$ denotes the set of continous morphisms from $A$ to the topologically discrete ring $R$. We have $Spf_k$ is a (contravariant) equivalence between the category of profinite $k$-rings and the category $fSch_k$ of formal $k$-schemes.

1. Instead of defining the category $fSch_k$ of formal $k$-schemes as the [[opposite category|opposite]] of $Mf_k$ define it instead covariantly on the category of finite dimensional $k$-[[coring|corings]].

1. A formal $k$-scheme is precisely a left exact (commuting with finite limits) functor $X:Mf_k\to Set$. 

([Demazure, p-divisible groups, chapter I](#Demp))

The inclusion $Mf_k\hookrightarrow M_k$ induces a functor

$${}^\hat\; :Sch_k\to fSch_k$$

called _completion functor_.


### Formal spectra of Noetherian rings

If $X$ is a [[scheme]], a [[closed subscheme]] $Y\subset X$ is given by an embedding of topological spaces with the [[comorphism]] $\mathcal{O}_X\to f_*\mathcal{O}_Y$ which is a surjection; but alternatively $\mathcal{O}_Y$ can be recovered from $X$ and the defining sheaf of ideals $\mathcal{I}\subset \mathcal{O}_X$. Then one defines the [[structure sheaf]] of the completion $\mathcal{O}_{\hat{X}}$ as $lim_n \mathcal{O}_X/\mathcal{I}^n$ restricted to $Y$ and the __completion__ $\hat{X} := (Y,\mathcal{O}_{\hat{X}})$. If $X = Spec\,R$ where $R$ is a noetherian $I$-adic ring, and $Y=Spec\,R/I$ then the completion is called the **[[formal spectrum]]** of $R$ denoted

$$
  Spf\,R = \hat{X}
$$ 


(where $R$ is viewed as a topological ring). The formal spectrum is an [[ind-object]] in the [[category]] of [[algebraic schemes]], viewed as a formal colimit
$colim_n Spec (R/I^n)$. 

A (locally) noetherian formal scheme is a formal completion of a (locally) noetherian scheme along a closed subscheme. Equivalently, a locally noetherian scheme is a locally ringed space which is locally isomorphic to the formal spectrum of a complete separated adic noetherian ring.


### More general ind-schemes

The formal spectrum can be extended to a somewhat bigger class of topological rings than the noetherian ones; Grothendieck developed the theory in the generality of [[pseudocompact ring|pseudocompact]] topological rings. However, some important rings, e.g. the ring of [[integers]] $\mathbb{Z}$, do not have a pseudocompact topology. Thus one could try to consider a more general subcategory of [[ind-schemes]] (with at least the requirement that the [[ind-object]] be represented by a diagram where the connecting morphisms are [[closed subscheme|closed immersions of schemes]]); one such approach is outlined in some detail in ([Beilinson-Drinfeld](#BeilinsonDrinfeld)).

## Examples

### Formal power series and their formal spectra
 {#FormalPowerSeries}

The [[completion of a ring]] of the [[polynomial ring]] $\mathbb{Z}[x]$ (the [[formal dual]] to the [[affine line]] $\mathbb{A}^1$) at the ideal $(x)$ is the [[limit]] -- formed in the [[category]] [[CRing]] --

$$
  \mathbb{Z}[x]^\wedge_{(x)} = \underset{\longleftarrow}{lim}_n (\mathbb{Z}[x])/(x^{n+1})
$$

of the [[quotient rings]] of $\mathbb{Z}[x]$ by the ideals generated by $x^{n+1}$ (the [[ring of dual numbers]] and its higher analogs). This yields the [[formal power series]] ring 

$$
  \mathbb{Z}[x]^\wedge_{(x)}
  \simeq
   \mathbb{Z}[ [x] ]
  \,.
$$

Notice that the formal power series ring contains _no_ nilpotent elements except for zero -- even though each filtering stage $(\mathbb{Z}[x])/(x^n)$ does.

In contrast, the [[filtered colimit]] of the [[sheaves]] on [[affine varieties]] $Spec(R)$ that are [[representable functor|represented]] by this system of nilpotent rings is the formal scheme

$$
  \widehat{\mathbb{A}^1}
  =
  \underset{\longrightarrow}{lim}_n Spec(\mathbb{Z}[x]/(x^{n+1}))
  \;\;\;
  \in 
  Sh(Aff) = Sh(CRing^{op})
$$

given by the sheaf which sends each ring to its [[nilradical]]

$$
  \widehat{\mathbb{A}^1} \;\colon\;  Spec(R) \mapsto Nil(R)
  \,.
$$

(see e.g. [Strickland 00, example 4.2, example 4.18](#Strickland00)).

### Formal neighbourhood of the diagonal

See at _[[formal neighbourhood of the diagonal]]_.

### Formal groups

The [[group objects]] in formal schemes are the [[formal groups]]. See there for more.

## References

Classical discussion includes

* [[Alexander Grothendieck]], _G&#233;om&#233;trie formelle et g&#233;om&#233;trie alg&#233;brique_, FGA 2 (S&#233;minaire Bourbaki, t. 11, 1958/59, no. 182)

* [[Luc Illusie]], _Grothendieck existence theorem in formal geometry_, chapter 8 in Fantechi, Gottsche, Illusie, Kleiman, Nitsure, Vistoli, _Fundamental algebraic geometry, Grothendieck's [[FGA explained]], Math. Surveys and Monographs_ __123__, AMS 2005 (draft version [pdf](http://cdsagenda5.ictp.it//askArchive.php?categ=a0255&id=a0255s3t3&ifd=15021&down=1&type=lecture_notes))

* A. Grothendieck (avec J. Dieudonne), [[EGA]] I.10

* A. Grothendieck et al. [[SGA]] III.2 (Exp. 7a, P. Gabriel, &#201;tude infinit&#233;simale des sch&#233;mas en groupe et groupes formels; Exp. 7b, P. Gabriel, Groupes formels)

* R. Hartshorne, _Algebraic geometry_, II.9

* M. Demazure, P. Gabriel, _Groupes algebriques_, tome 1 (later volumes never appeared), Mason and Cie, Paris 1970

* {#Demp}Michel Demazure, lectures on p-divisible groups [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

* [[Daniel Murfet]], notes [Section2.9-FormalSchemes.pdf](http://therisingsea.org/notes/Section2.9-FormalSchemes.pdf)

* Leovigildo Alonso, Ana Jeremias, Marta Perez, _Infinitesimal lifting and Jacobi criterion for smoothness on formal schemes_ ([arXiv:math/0604241](http://arxiv.org/abs/math/0604241))

More general discussion in terms of ind-schemes includes

* {#BeilinsonDrinfeld} A. Beilinson, V. Drinfel'd, _Quantization of Hitchin's integrable system and Hecke eigensheaves on Hitchin system_, preliminary version ([pdf](http://www.math.uchicago.edu/~mitya/langlands/hitchin/BD-hitchin.pdf))

Another approach using a certain topological extension of the [[Yoneda lemma]] on $k Alg^{op}$ has been proposed in

* B. Pareigis, R. A. Morris, _Formal groups and Hopf algebras over discrete rings_, Trans. Amer. Math. Soc.  __197__ (1974), 113--129 ([doi](http://dx.doi.org/10.2307/1996930), [[Morris-Pareigis formal scheme|nlab entry]]).

[[Nikolai Durov]] has considered a flexible bigger category (which inludes the usual schemes) of covariant functors from the category of pairs $(R,I)$ where $R$ is a commutative ring and $I$ a [[nilpotent ideal]]; the correspondence between formal groups and [[Lie algebras]] based on Hausdorff series is neatly developed and used in that language; see chapters 7--9 of

* N. Durov, S. Meljanac, A. Samsarov, Z. &#352;koda, _A universal formula for representing Lie algebra generators as formal power series with coefficients in the Weyl algebra_, Journal of Algebra 309, n. 1, 318--359 (2007)
([doi:jalgebra](http://dx.doi.org/10.1016/j.jalgebra.2006.08.025))
([math.RT/0604096](http://front.math.ucdavis.edu/math.RT/0604096)).
 
For another generalization of formal schemes see

* T. Yasuda, _Non-adic formal schemes_, Int. Math. Research Notices 2009: 2417--2475, ([doi:imrn](http://dx.doi.org/10.1093/imrn/rnp021), [arxiv](http://arxiv.org/abs/0711.0434))

In a fundamental article in [[noncommutative algebraic geometry]],

* M. Kapranov, _Noncommutative geometry based on commutator expansions_, [math.AG/9802041](http://arxiv.org/abs/math.AG/9802041),

Kapranov introduced objects which should be interpreted as the infinitesimal neighborhoods of those commutative schemes with a closed immersion into a noncommutative scheme which is locally isomorphic to the spectrum of a free associative algebra. 

And a decidedly functorial perspective is in (section 4 of)

* {#Strickland00} [[Neil Strickland]], _Formal schemes and formal groups_, [math.AT/0011121](http://arxiv.org/abs/math.AT/0011121)


For the scheme geometric picture behind the infinitesimal neighborhoods and [[D-modules]] see also

* A. Be&#301;linson, J. Bernstein, J., _A proof of Jantzen conjectures_, in I. M. Gel&#697;fand Seminar, 1--50,
Adv. Soviet Math., 16, Part 1, Amer. Math. Soc., Providence, RI, 1993 (MR1237825 (95a:22022))

Some aspects of formal completions from the point of view of the derived categories are in

* [[Dmitri Orlov|D. Orlov]], _Formal completions and idempotent completions of triangulated categories of singularities_, [arxiv/0901.1859](http://arxiv.org/abs/0901.1859)

* Alexander I. Efimov, _Formal completion of a category along a subcategory_, [arxiv/1006.4721](http://arxiv.org/abs/1006.4721)

[[!redirects formal schemes]]