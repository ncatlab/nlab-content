
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
####Algebra
####Topos Theory
+--{: .hide}
[[!include higher algebra - contents]]
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}


[[!redirects Jónsson-Tarski object]]
[[!redirects Jonsson-Tarski object]]
[[!redirects idempotent object]]
[[!redirects Cantor algebra]]

##Idea


A _J&#243;nsson-Tarski algebra_ is a set that looks like two copies of itself. Since historically the classical examples of these occured in the cardinal arithmetics of [[Georg Cantor]], they are also known as _Cantor algebras_.

## Definition

A **J&#243;nsson-Tarski algebra**, also called a [[Georg Cantor|Cantor]] algebra, is a [[set]] $A$ together with an [[isomorphism]] $A\cong A\times A$.

More generally, an object $A$ in a [[symmetric monoidal category]] $\mathcal{M}$ together with an isomorphism $\alpha:A\otimes A\rightarrow A$ is called a **J&#243;nsson-Tarski object**, or an _idempotent_ object (Fiore&Leinster 2010).

In another possible direction for generalization, one defines a **J&#243;nsson-Tarski n-algebra** as a set $X$ together with an [[isomorphism]] $X\overset{\simeq}{\to}X^n$ (cf. Smirnov 1971, Higman 1974).[^fine]

[^fine]: A profunctorial variation on this theme has been proposed by Leinster (2007). See at [[Jónsson-Tarski topos]] for some details. 

## Properties

* Clearly (at least in [[classical mathematics]]), any J&#243;nsson-Tarski algebra is either [[empty set|empty]], a [[singleton]], or [[infinite set|infinite]].

* The structure of a J&#243;nsson-Tarski algebra can be described by an [[algebraic theory]], with one binary operation $\mu$ and two unary operations $\lambda$ and $\rho$ such that $\mu(\lambda(x),\rho(x)) = x$, $\lambda(\mu(x,y))=x$, and $\rho(\mu(x,y))=y$.

* Any two J&#243;nsson-Tarski algebras freely generated from finite non empty sets are isomorphic. It was this property they owe their introduction to (J&#243;nsson&Tarski 1956,1961).

* Just like in the category $Grp$ of [[group|groups]], subalgebras of free algebras are free themselves (cf. this [Stackexchange question](#Stack)).

* The category of J&#243;nsson-Tarski algebras is a [[topos]], the so called [[Jónsson-Tarski topos]] $\mathcal{J}_2$, and hence is an example for a [[variety]] that is also a topos (cf. Johnstone 1985).

* The [[Thompson Group]] F is the group of order-preserving automorphisms of the free J&#243;nsson-Tarski algebra on one generator (cf. Fiore-Leinster 2010).

##Related concepts

* [[Jónsson-Tarski topos]]

* [[Thompson group]]

* [[idempotent]]

* [[self-similarity]]

##Links

* Wikipedia, [J&#243;nsson-Tarski algebra](https://en.wikipedia.org/wiki/J%C3%B3nsson%E2%80%93Tarski_algebra)

* {#Stack}Stackexchange: [J&#243;nsson-Tarski algebra form a Schreier variety](https://math.stackexchange.com/questions/3544667/do-j%C3%B3nsson-tarski-algebras-form-a-schreier-variety)

##References


* K. S. Brown, _Finiteness Properties of Groups_ , JPAA **44** (1987) pp.45-75.

* J. Dubeau, _J&#243;nsson J&#243;nsson-Tarski algebras_ , arXiv:2202.02460 (2022).  ([abstract](https://arxiv.org/abs/2202.02460v1))

* J. Dudek, A. W. Marczak, _On Cantor Identities_ , Algebra Universalis 
**68** (2012) pp.237–247.

* [[Marcelo Fiore]], [[Tom Leinster]], _An abstract characterization of Thompson's group F_ , arXiv.math/0508617 (2010). ([pdf](http://arxiv.org/pdf/math/0508617v2.pdf))

* R. Freese, J. B. Nation, _Free J&#243;nsson-Tarski algebras_ , ms. 2020. ([pdf](http://www.math.hawaii.edu/~jb/Jonsson-Tarski_algebras.pdf))

* G. Higman, _Finitely presented infinite simple groups_ , Notes on Pure Mathematics **8** (1974) Australian National University Canberra.

* P. Hines, _The Categorical Theory of Self-Similarity_ , TAC **6** no.3 (1999). ([abstract](http://www.tac.mta.ca/tac/volumes/6/n3/6-03abs.html))

* [[Peter Johnstone]], _When is a Variety a Topos?_ , Algebra Universalis **21** (1985) pp.198-212.

* [[Peter Johnstone]], _Collapsed Toposes and Cartesian Closed Varieties_ , JA **129** (1990) pp.446-480.

* B. J&#243;nsson, [[A. Tarski]] , _Two General Theorems Concerning Free Algebras_ , Bull. Amer. Math. Soc. **62** p.554. ([pdf](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society/volume-62/issue-6/The-summer-meeting-in-Seattle/bams/1183521094.full))

* B. J&#243;nsson, [[A. Tarski]] , _On Two Properties of Free Algebras_ , Math. Scand. **9** (1961) pp.95-101. ([pdf](http://ojs.statsbiblioteket.dk/index.php/math/article/viewFile/10627/8648))

* [[Tom Leinster]], _J&#243;nsson-Tarski toposes_, Talk Nice 2007.  ([slides](http://www.maths.ed.ac.uk/~tl/nice/jt.pdf))

* A. K. Rumjancev, _An independent basis for the quasi-identities of a free Cantor algebra_ , Algebra and Logic **16** (1977) pp.119-129.

* D. M. Smirnov, _Cantor algebras with a single generator I_ , Algebra and
Logic **10** (1971) pp.40-49.

* D. M. Smirnov, _Cantor algebras with a single generator II_ , Algebra and
Logic **12** (1973) pp.399-404.

* D. M. Smirnov, _Bases and automorphisms of free Cantor algebras of finite rank_ , Algebra and Logic **13** (1974) pp.17-33.

* S. Swierczkowski, _On isomorphic free algebras_ , Fund. Math. **50**  (1961) pp.35–44.

[[!redirects Jonsson-Tarski algebras]]
[[!redirects Jonsson-Tarski algebra]]
[[!redirects Jónsson-Tarski algebras]]
[[!redirects Cantor algebra]]
[[!redirects Cantor algebras]]