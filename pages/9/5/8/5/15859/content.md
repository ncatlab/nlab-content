
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
#### Higher Algebra
+--{: .hide}
[[!include topos theory - contents]]
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

[[!redirects Cole spectrum]]


+-- {: .rightHandSide}
> Devinette: Trouver un point commun entre la Samaritaine et [[SGA4|SGA 4]].[^CM] {#quot}
=--

##Idea##

In the mid 1970s [[Julian Cole]] proposed a [[topos theory|topos-theoretic]] construction of [[spectrum (geometry)|spectra in geometry]] arising in the sense of [[spectrum of a commutative ring]] but for more general [[algebraic theories|(algebraic) theories]], as [[right adjoints]] to [[forgetful functors]] that generalized [[Monique Hakim|M. Hakim's]] approach to [[locally ringed topos|locally ringed toposes]].

Basic ingredients are pairs of [[geometric theories]] $\mathbb{S}$ and $\mathbb{T}$ over the same [[language]] such that $\mathbb{T}$ results from $\mathbb{S}$ by addition of further [[axioms]]. Then $\mathbb{T}-Mod_\mathcal{E}$ is a [[full subcategory]] of $\mathbb{S}-Mod_\mathcal{E}$ and the spectrum construction can be viewed as a sort of generalization of a right adjoint to the inclusion. The quotient relation between the two theories gives the construction a model-theoretic flavor.

###Definition###

Let $\mathbb{T}$ be [[geometric theory]]. The 2-category $\mathbb{T}-\mathfrak{Top}$ of _[[T-modelled toposes]]_ is given as follows: 

* objects are pairs $(\mathcal{E},M)$ where $\mathcal{E}$ is a topos and $M$ a $\mathbb{T}$-model in $\mathcal{E}$, 

* 1-cells $(\mathcal{F},L)\to (\mathcal{E},M)$ are pairs $(p,f)$ with $p:\mathcal{F}\to\mathcal{E}$ a geometric morphism and $f:p^*M\to L$ a $\mathbb{T}$-model homomorphism, and 

* 2-cells $(p,f)\to(q,g)$ are [[natural transformations]] $\eta:p\to q$ such that $f=g\circ\eta_M$.

$\mathbb{T}-\mathfrak{Top}_N$ is the full sub-2-category on pairs $(\mathcal{E},M)$ such that $\mathcal{E}$ has a [[natural numbers object]].

###Definition###

Let $\mathbb{T}$ be a (geometric) quotient theory of $\mathbb{S}$. A class $\mathbb{A}$ of $\mathbb{T}$-model morphisms is called _admissible_ if

* $\mathbb{A}$ is closed under [[inverse image functor|inverse image functors]]: $p^*f\in \mathbb{A}$ for $f\in \mathbb{A}$.

* $\mathbb{A}$ contains all identity morphisms and given $g\in \mathbb{A}$ and composable $f$ : $f\in \mathbb{A}$ iff $gf\in \mathbb{A}$.

* Given an $\mathbb{S}$-model morphism $f:M\to L$ with $L$ a $\mathbb{T}$-model, there exists a factorization $M\overset{q}{\to}M_f\overset{\hat{f}}{\to}L$ with $M_f$ a $\mathbb{T}$-model and $\hat{f}\in \mathbb{A}$, such that any other such factorization $M\overset{r}{\to}P\overset{p}{\to}L$ factors with $gh=\hat{f}$ and $hq=r$ for a unique $h:M_f\to P$. Moreover, this factorization is preserved by inverse image functors.

The sub-category $\mathbb{A}-\mathfrak{Top}$ of $\mathbb{T}-\mathfrak{Top}$ for such an admissible class has 1-cells $(p,f)$ with $f\in \mathbb{A}$.

### Theorem

+-- 

*Let $\mathbb{S}$ and $\mathbb{T}$ be finitely presented geometric theories such that $\mathbb{T}$ is a quotient theory of $\mathbb{S}$, and let $\mathbb{A}$ be an admissible class of morphisms of $\mathbb{T}$-models. Then the inclusion functor $\mathbb{A}-\mathfrak{Top}_N\to \mathbb{S}-\mathfrak{Top}_N$ has a right adjoint $Spec:\mathbb{S}-\mathfrak{Top}_N\to \mathbb{A}-\mathfrak{Top}_N$.*

=--

###Example###

The classical example is given by the [[geometric theory|geometric theories]] of [[commutative ring|commutative rings]] and [[local ring|local rings]] with the factorization given by the class of local morphisms and appropriate rings of fractions as the local factors. The right adjoint maps a commutative ring $A$ basically to the pair consisting of the sheaf topos on the Zariski spectrum of $A$ and the structure sheaf of $A$ (cf. Johnstone 1977b). 

###Remark###
In the context of his work with C. Lair on 'locally free diagrams' [[René Guitart|R. Guitart]] interprets the 'almost-freeness' of the spec construction as an 'almost-algebraicity' of topology (See Guitart 2008 and the references therein).

##Related concepts##

*[[spectrum of a commutative ring]]

*[[locally algebra-ed topos]]

*[[classifying topos]]

*[[geometric theory]]

*[[ringed topos]]

*[[Structured Spaces]]

*[[formally etale morphisms]]

##References##

The original article is reprinted as

* [[Julian Cole]], _The bicategory of topoi and spectra_, Reprints in Theory and Applications of Categories, No. 25 (2016) pp. 1-16 ([TAC](http://www.tac.mta.ca/tac/reprints/articles/25/tr25abs.html))

Besides this, Johnstone's article ([1977a](#Johnstone77a)), the book of Johnstone ([1977b](#Johnstone77b)), on which the above exposition is based, is a good source for this material. Bunge (1981), Bunge and Reyes (1981) apply the results in a model-theoretic context. See also the short remark in Caramello (2014, p.55).

[[Michel Coste|M. Coste]]'s (1979) take on admissible maps flows in Coste-Michon (1981) via the 4-yoga (cf. [above](#quote)) into the more recent approach using open and &#233;tale maps pioneered by Joyal. Dubuc (2000) compares his axiomatic &#233;tale morphisms to Cole's class of admissible morphisms.

For a glimpse of [[André Joyal|A. Joyal]]'s original approach to the spectrum using distributive lattices see Joyal (1975), Espa&#241;ol (1983,1986) or Coquand-Lombardi-Schuster (2007).  For higher categorical variations on the theme _spectrum_ (of a ring) see Lurie (2009).

* [[Marta Bunge|M. Bunge]], _Sheaves and Prime Model Extensions_ , J. Algebra **68** (1981) pp.79-96.

* [[Marta Bunge|M. Bunge]], [[Gonzalo E. Reyes|G. E. Reyes]] , _Boolean spectra and model completions_ , Fund.Math. **113** (1981) pp.165-173. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm113/fm113115.pdf))

* [[Olivia Caramello|O. Caramello]], _Topos-theoretic background_ , ms. 2014. ([pdf](http://www.oliviacaramello.com/Unification/ToposTheoreticPreliminariesOliviaCaramello.pdf))

* [[Julian Cole|J. C. Cole]], _The Bicategory of Topoi, and Spectra_ , ms. ([pdf](http://www.oliviacaramello.com/Unification/ColeBicategoryTopoiSpectra.pdf))

* [[Thierry Coquand]], Henri Lombardi, Peter Schuster, _The projective spectrum as a distributive lattice_ , Cah. Top. G&#233;om. Diff. Cat. **XLIIX** no.3 (2007) pp.220-228. ([numdam](http://www.numdam.org/item?id=CTGDC_2007__48_3_220_0))

* [[Michel Coste|M. Coste]], _Localisation, spectra and sheaf representation_ , pp.212-238 in Fourman, Mulvey & Scott (eds.), _Applications of Sheaves_ , Springer LNM **753** (1979).

* M. Coste, G. Michon, _Petits et Gros Topos en G&#233;om&#233;trie Alg&#233;brique_ , Cah. Top. G&#233;om. Diff. Cat. **XXII** no.1 (1981) pp.25-30. ([pdf](http://archive.numdam.org/article/CTGDC_1981__22_1_25_0.pdf)) {#CosteMichon81}

* [[Eduardo Dubuc|E. J. Dubuc]], _Axiomatic etal maps and a theory of spectrum_ , JPAA **149** (2000) pp.15-45.
 {#Dubuc}

* L. Espa&#241;ol, _Le spectre d'un anneau dans l'alg&#232;bre constructive et applications &#224; la dimension_ , Cah. Top. G&#233;om. Diff. Cat. **XXIV** no.2 (1983) pp.133-144. ([numdam](http://www.numdam.org/numdam-bin/item?id=CTGDC_1983__24_2_133_0))

* L. Espa&#241;ol, _El Espectro y la Dimension des Anillos en el Algebra sobre un Topos_ , Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.105-128. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002541068))

* [[René Guitart|R. Guitart]], _Toute Th&#233;orie est Alg&#233;brique et Topologique_ , Cah.Top.G&#233;om.Diff.Cat. **XLIX** no. 2 (2008) pp.83-128. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_2008__49_2/CTGDC_2008__49_2_83_0/CTGDC_2008__49_2_83_0.pdf))

* [[Monique Hakim|M. Hakim]], _Topos Annel&#233;s et Sch&#233;mas Relatifs_ , Springer Heidelberg 1972.

* [[Peter Johnstone|P. T. Johnstone]], _Rings, fields and spectra_ , J. Algebra **49** (1977) pp.238-260. {#Johnstone77a}

* P. T. Johnstone, _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014). pp.205-207 {#Johnstone77b}

* [[André Joyal|A. Joyal]], _Les Th&#233;or&#232;mes de Chevalley-Tarski et Remarques sur l'Alg&#232;bre Constructive_ , Cah. Top. G&#233;om. Diff. Cat. **XVI** (1975) pp.256-258. ([Proceedings Colloque Amiens 1975](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1975__16_3/CTGDC_1975__16_3_217_0/CTGDC_1975__16_3_217_0.pdf), 6.81 MB)

* [[Jacob Lurie|J. Lurie]], _Derived Algebraic Geometry V: [[Structured Spaces]]_ , ms. 2009. ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-V.pdf))

* R. O. Robson, _Model theory and spectra_ , JPAA **63** (1990) pp.301-327.

[^CM]: Coste&Michon (1981), p.27.

[[!redirects Cole spectral theory]]
[[!redirects Cole's Theory of Spectrum]]
[[!redirects Cole spectrum]]