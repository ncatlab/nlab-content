
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


Loosely speaking, a _J&#243;nsson-Tarski algebra_ is a Cantorian '[[countable set|Abzählung]]' of $\mathbf{N}^2$ gone algebra.

## Definition

A **J&#243;nsson-Tarski algebra**, also called a [[Georg Cantor|Cantor]] algebra, is a [[set]] $A$ together with an [[isomorphism]] $A\cong A\times A$.

More generally, an object $A$ in a [[symmetric monoidal category]] $\mathcal{M}$ together with an isomorphism $\alpha:A\otimes A\rightarrow A$ is called a **J&#243;nsson-Tarski object**, or an _idempotent_ object (Fiore&Leinster 2010).

## Properties

* Clearly (at least in [[classical mathematics]]), any J&#243;nsson-Tarski algebra is either [[empty set|empty]], a [[singleton]], or [[infinite set|infinite]].

* The structure of a J&#243;nsson-Tarski algebra can be described by an [[algebraic theory]], with one binary operation $\mu$ and two unary operations $\lambda$ and $\rho$ such that $\mu(\lambda(x),\rho(x)) = x$, $\lambda(\mu(x,y))=x$, and $\rho(\mu(x,y))=y$.

* Any two J&#243;nsson-Tarski algebras freely generated from finite non empty sets are isomorphic. It was this property they owe their introduction to (J&#243;nsson&Tarski 1961).

* The category of J&#243;nsson-Tarski algebras is a [[topos]], the so called [[Jónsson-Tarski topos]] $\mathcal{J}_2$, and hence is an example for an [[algebraic variety]] that is also a topos (cf. Johnstone 1985).

* The [[Thompson Group]] F is the group of order-preserving automorphisms of the free J&#243;nsson-Tarski algebra on one generator.

##References

* Wikipedia, [J&#243;nsson-Tarski algebra](http://en.wikipedia.org/wiki/J&#243;nsson&#8211;Tarski_algebra)

* B. J&#243;nsson, [[A. Tarski]] , _On Two Properties of Free Algebras_ , Math. Scand. **9** (1961) pp.95-101. ([pdf](http://ojs.statsbiblioteket.dk/index.php/math/article/viewFile/10627/8648))

* [[Marcelo Fiore]], [[Tom Leinster]], _An abstract characterization of Thompson's group F_ , arXiv.math/0508617 (2010). ([pdf](http://arxiv.org/pdf/math/0508617v2.pdf))

* [[Peter Johnstone]], _When is a Variety a Topos?_ , Algebra Universalis **21** (1985) pp.198-212.

* [[Peter Johnstone]], _Collapsed Toposes and Cartesian Closed Varieties_ , JA **129** (1990) pp.446-480.

[[!redirects Jonsson-Tarski algebras]]
[[!redirects Jonsson-Tarski algebra]]
[[!redirects Jónsson-Tarski algebras]]
[[!redirects Cantor algebra]]
[[!redirects Cantor algebras]]