
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


##Idea##
In the mid 1970s Julian Cole proposed a topos-theoretic construction of spectra arising as right adjoints to forgetful functors that generalized [[Monique Hakim|M. Hakim's]] approach to the [[spectrum of a commutative ring]].

##Definition##
Let $T$ be [[geometric theory]]. The 2-category $T-\mathfrak{Top}$ of _T-modelled toposes_ has 

* objects pairs $(\mathcal{E},M)$ where $\mathcal{E}$ is a topos and $M$ a $T$-model in $\mathcal{E}$, 

* 1-cells $(\mathcal{F},L)\to (\mathcal{E},M)$ pairs $(p,f)$ with $p:\mathcal{F}\to\mathcal{E}$ a geometric morphism and $f:p^*M\to L$ a $T$-model homomorphism, and 

* 2-cells $(p,f)\to(q,g)$ is a [[natural transformation]] $\eta:p\to q$ such that $f=g\circ\eta_M$.

$T-\mathfrak{Top}_N$ is the full sub-2-category such that $\mathcal{E}$ has a [[natural numbers object]].


##Theorem##
Let $S$ and $T$ be finitely presented geometric theories such that $T$ is a quotient theory of $S$, and let $A$ be an admissible class of morphisms of $T$-models. Then the inclusion functor $A-\mathfrak{Top}_N\to S-\mathfrak{Top}_N$ has a right adjoint $Spec:S-\mathfrak{Top}_N\to A-\mathfrak{Top}_N$.

##Example##

The classical example is given by the [[geometric theory|geometric theories]] of [[commutative ring|commutative rings]] and [[local ring|local rings]] with the factorization given by the class of local morphisms and appropriate rings of fractions as the local factors. The right adjoint maps a commutative ring $A$ basically to the pair consisting of the sheaf topos on the Zariski spectrum of $A$ and the structure sheaf of $A$ (cf. Johnstone 1977b). 

##Remark##
In the context of his work with C. Lair on 'locally free diagrams' [[René Guitart|R. Guitart]] interprets the 'almost-freeness' of the spec construction as an 'almost-algebraicity' of topology (See Guitart 2008 and the references therein).

##Related concepts##

*[[spectrum of a commutative ring]]

*[[classifying topos]]

*[[geometric theory]]

*[[ringed topos]]

*[[Structured Spaces]]

##References##

Beside Cole's unpublished paper, Johnstone (1977b) is a good source for this material. Bunge and Reyes (1981) apply the results in a model-theoretic context. See also the short remark in Caramello (2014).

* [[Marta Bunge|M. Bunge]], [[Gonzalo E. Reyes|G. E. Reyes]] , _Boolean spectra and model completions_ , Fund.Math. **113** (1981) pp.165-173. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm113/fm113115.pdf))

* [[Olivia Caramello|O. Caramello]], _Lattices of theories_ , arXiv:0905.0299v1 (2009). ([pdf](http://arxiv.org/pdf/0905.0299v1))

* [[Olivia Caramello|O. Caramello]], _Topos-theoretic background_ , ms. 2014. ([pdf](http://www.oliviacaramello.com/Unification/ToposTheoreticPreliminariesOliviaCaramello.pdf))

* J. C. Cole, _The Bicategory of Topoi, and Spectra_ , ms. ([pdf](http://www.oliviacaramello.com/Unification/ColeBicategoryTopoiSpectra.pdf))

* M. Coste, _Localisation, spectra and sheaf representation_ , pp.212-238 in Fourman, Mulvey & Scott (eds.), _Applications of
Sheaves_ , LNM **753** (1979).

* [[René Guitart|R. Guitart]], _Toute Th&#233;orie est Alg&#233;brique et Topologique_ , Cah.Top.G&#233;om.Diff.Cat. **XLIX** no. 2 (2008) pp.83-128. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_2008__49_2/CTGDC_2008__49_2_83_0/CTGDC_2008__49_2_83_0.pdf))

* [[Peter Johnstone|P. J. Johnstone]], _Rings, fields and spectra_ , JA **49** (1977) pp.238-260.

* P. J. Johnstone, _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014). pp.205-207 
