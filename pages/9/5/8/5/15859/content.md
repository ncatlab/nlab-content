
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
* automatic table of contents goes here
{:toc}

[[!redirects Cole spectrum]]


+-- {: .rightHandSide}
> Devinette: Trouver un point commun entre la Samaritaine et [[SGA4|SGA 4]].[^CM] 
=--

##Idea##

In the mid 1970s [[Julian Cole]] proposed a [[topos theory|topos-theoretic]] construction of spectra arising in the sense of [[spectrum of a commutative ring]] but for more general [[algebraic theories|(algebraic) theories]], as [[right adjoints]] to [[forgetful functors]] that generalized [[Monique Hakim|M. Hakim's]] approach to [[locally ringed topos|locally ringed toposes]].

Basic ingredients are pairs of [[geometric theories]] $S$ and $T$ over the same [[language]] such that $T$ results from $S$ by addition of further [[axioms]]. Then $T-Mod_\mathcal{E}$ is a [[full subcategory]] of $S-Mod_\mathcal{E}$ and the spectrum construction can be viewed as a sort of generalization of a right adjoint to the inclusion. The quotient relation between the two theories gives the construction a model-theoretical flavor.

###Definition###

Let $T$ be [[geometric theory]]. The 2-category $T-\mathfrak{Top}$ of _[[T-modelled toposes]]_ is given as follows: 

* objects are pairs $(\mathcal{E},M)$ where $\mathcal{E}$ is a topos and $M$ a $T$-model in $\mathcal{E}$, 

* 1-cells $(\mathcal{F},L)\to (\mathcal{E},M)$ are pairs $(p,f)$ with $p:\mathcal{F}\to\mathcal{E}$ a geometric morphism and $f:p^*M\to L$ a $T$-model homomorphism, and 

* 2-cells $(p,f)\to(q,g)$ are [[natural transformations]] $\eta:p\to q$ such that $f=g\circ\eta_M$.

$T-\mathfrak{Top}_N$ is the full sub-2-category on pairs $(\mathcal{E},M)$ such that $\mathcal{E}$ has a [[natural numbers object]].

###Definition###

Let $T$ be a (geometric) quotient theory of $S$. A class $A$ of $T$-model morphisms is called _admissible_ if

* $A$ is closed under [[inverse image functor|inverse image functors]]: $p^*f\in A$ for $f\in A$.

* $A$ contains all identity morphisms and given $g\in A$ and composable $f$ : $f\in A$ iff $gf\in A$.

* Given an $S$-model morphism $f:M\to L$ with $L$ a $T$-model, there exists a factorization $M\overset{q}{\to}M_f\overset{\hat{f}}{\to}L$ with $M_f$ a $T$-model and $\hat{f}\in A$, such that any other such factorization $M\overset{r}{\to}P\overset{p}{\to}L$ factors with $gh=\hat{f}$ and $hq=r$ for a unique $h:M_f\to P$. Moreover, this factorization is preserved by inverse image functors.

The sub-category $A-\mathfrak{Top}$ of $T-\mathfrak{Top}$ for such an admissible class has 1-cells $(p,f)$ with $f\in A$.


##Theorem##
>Let $S$ and $T$ be finitely presented geometric theories such that $T$ is a quotient theory of $S$, and let $A$ be an admissible class of morphisms of $T$-models. Then the inclusion functor $A-\mathfrak{Top}_N\to S-\mathfrak{Top}_N$ has a right adjoint $Spec:S-\mathfrak{Top}_N\to A-\mathfrak{Top}_N$.

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

Beside Cole's unpublished paper and Johnstone's article ([1977a](#Johnstone77a)), the book of Johnstone ([1977b](#Johnstone77b)), on which the above exposition is based, is a good source for this material. Bunge and Reyes (1981) apply the results in a model-theoretical context. Dubuc (2000) compares his axiomatic &#233;tale morphisms to Cole's class of admissible morphisms. See also the short remark in Caramello (2014). For higher categorical variations on the theme _spectrum_ (of a ring) see Lurie (2009).

* [[Marta Bunge|M. Bunge]], [[Gonzalo E. Reyes|G. E. Reyes]] , _Boolean spectra and model completions_ , Fund.Math. **113** (1981) pp.165-173. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm113/fm113115.pdf))

* [[Olivia Caramello|O. Caramello]], _Topos-theoretic background_ , ms. 2014. ([pdf](http://www.oliviacaramello.com/Unification/ToposTheoreticPreliminariesOliviaCaramello.pdf))

* [[Julian Cole|J. C. Cole]], _The Bicategory of Topoi, and Spectra_ , ms. ([pdf](http://www.oliviacaramello.com/Unification/ColeBicategoryTopoiSpectra.pdf))

* [[Michel Coste|M. Coste]], _Localisation, spectra and sheaf representation_ , pp.212-238 in Fourman, Mulvey & Scott (eds.), _Applications of
Sheaves_ , Springer LNM **753** (1979).

* M. Coste, G. Michon, _Petits et Gros Topos en G&#233;om&#233;trie Alg&#233;brique_ , Cah. Top. G&#233;om. Diff. Cat. **XXII** no.1 (1981) pp.25-30. ([pdf](http://archive.numdam.org/article/CTGDC_1981__22_1_25_0.pdf)) {#CosteMichon81}

* [[Eduardo Dubuc|E. J. Dubuc]], _Axiomatic etal maps and a theory of spectrum_ , JPAA **149** (2000) pp.15-45.
 {#Dubuc}

* [[René Guitart|R. Guitart]], _Toute Th&#233;orie est Alg&#233;brique et Topologique_ , Cah.Top.G&#233;om.Diff.Cat. **XLIX** no. 2 (2008) pp.83-128. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_2008__49_2/CTGDC_2008__49_2_83_0/CTGDC_2008__49_2_83_0.pdf))

* [[Monique Hakim|M. Hakim]], _Topos Annel&#233;s et Sch&#233;mas Relatifs_ , Springer Heidelberg 1972.

* [[Peter Johnstone|P. T. Johnstone]], _Rings, fields and spectra_ , JA **49** (1977) pp.238-260. {#Johnstone77a}

* P. T. Johnstone, _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014). pp.205-207 {#Johnstone77b}

* [[Jacob Lurie|J. Lurie]], _Derived Algebraic Geometry V: Structured Spaces_ , ms. 2009. ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-V.pdf))

[^CM]: Coste&Michon (1981), p.27.