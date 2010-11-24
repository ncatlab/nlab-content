+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Gel'fand triple_ is a structure that equips a [[Hilbert space]] with a dense [[topological vector space|topological vector subspace]]  of good "test" functions, so that the dual of the subspace of test functions enhaces the Hilbert space by embedding it into a larger [[TVS]] whose elements can be considered as generalized [[eigenvector]]s for the continuous [[spectrum of an operator|spectrum]] of [[normal operator|normal]] (possibly [[unbounded operator|unbounded]]) [[linear operator]]s. 

## Definition

A __Gel'fand triple__ is datum of the form

$$
B\stackrel{J}\hookrightarrow H \stackrel{K}\hookrightarrow B^*
$$

where $H$ is a [[separable Hilbert space]], $B$ is a [[Banach space]] (or more general [[topological vector space]] (TVS)), $B^*$ is a dual TVS of $B$, $J:B\hookrightarrow H$ is an injective [[bounded operator]] with dense image, and $K$ is the composition of the canonical isomorphism $H\cong H^*$ determined by the inner product (i.e. given by Riesz theorem) and of the Banach transpose (dual) $J^*: H^*\to B^*$ of the operator $J$. The fact that $J(B)$ is dense in $H$ implies that $J^*$ (hence also $K$)  is injective as well.  

## Basic examples

A typical example is $B = \mathcal{S}(\mathbb{R}^n)$ (Schwarz space), $H = L^2(\mathbb{R}^n)$ and $B^* = \mathcal{S}'(\mathbb{R}^n)$ (the space of tempered (Schwarz) distributions). One of the basic facts on Fourier transform is that this Gel'fand triple is preserved by the Fourier transform.

Another natural example is $\mathcal{l}^1\hookrightarrow \mathcal{l}^2\hookrightarrow \mathcal{l}^\infty$. 

#### A long example

Let $H$ be the Hilbert space $L^2(\mathbb{R}, d x)$ consisting of square integrable functions $f$ with respect to [[Lebesgue measure]]. There is an unbounded self-adjoint operator 

$$m_x: H \to H: f \mapsto x \cdot f$$ 

where $(x \cdot f)(y) := y f(y)$. This operator is not defined on all of $H$, but it is defined on a dense subspace of $H$. For example, if $S$ is the Schwartz space consisting of smooth functions $f$ on $\mathbb{R}$ all of whose derivatives $f^{(n)}(x)$ decay rapidly at infinity (more rapidly than any negative power of $|x|$), then there is a dense inclusion map $i: S \to H$, and $m_x$ is defined globally on $S$. 

Meanwhile the Schwartz space $S$ carries its own topology (as described in the article [[distribution]]), stronger than the topology it inherits from $H$, and the space of tempered distributions $S^*$ is defined to be the continuous dual of the [[topological vector space|TVS]] $S$. Since the continuous inclusion $i: S \to H$ is dense, it follows that any continuous functional 

$$f: S \to \mathbb{C}$$ 

has at most one extension to a continuous functional $H \to \mathbb{C}$. In other words, the adjoint map 

$$i^*: H^* \to S^*$$ 

is injective. In addition, the topology on $S$ is such that the operator $m_x: S \to S$ is continuous. 

In this example, there is a dense inclusion $S \to S^*$ defined by the inner product pairing, and the operator $m_x$ extends uniquely to an operator $S^* \to S^*$, called $m_x$ by abuse of notation. Again, in this example, the operator $m_x: S^* \to S^*$ has an eigenvector $s_{\xi}$ for each $\xi \in \mathbb{R}$:  

$$m_x(s_{\xi}) = \xi s_{\xi}$$

(under construction)

## Isomorphisms

An isomorphism of Gelfand triples $(B_1,H_1,B^*_1)\to (B_2,H_2,B^*_2)$ is a unitary isomorphism $H_1\to H_2$ which restricts to an isomorphism of Banach spaces $B_1\to B_2$, and which extends to a weak$*$- and norm-preserving continuous isomorphism $B_1^*\to B_2^*$. 

## Terminology and references

#### Terminological variants and history

Usually, $B$ and $B^*$ are Banach spaces, when we say *Banach Gel'fand triple*, there are some other variants involving more general [[topological vector space]]s. In some cases one also uses the terminology *rigged Hilbert space*, following articles by Roberts and others since mid 1960-s. Nuclear Gel'fand triples are very common and then the notion is well behaved. In Russian literature the term *enriched* Hilbert space is used (&#1086;&#1089;&#1085;&#1072;&#1097;&#1077;&#1085;&#1085;&#1086;&#1077; &#1075;&#1080;&#1083;&#1100;&#1073;&#1077;&#1088;&#1090;&#1086;&#1074;&#1086; &#1087;&#1088;&#1086;&#1089;&#1090;&#1088;&#1072;&#1085;&#1089;&#1090;&#1074;&#1086;), sometimes translated also as *equipped* Hilbert space. The enriched word here is the same as in the phrase [[enriched category]].

#### Early references

Gel'fand triples were introduced by Gel'fand school about 1955 and quickly incorporated into the theory of generalized functions. 

* [[I. M. Gel&#697;fand, A. G. Kostyu&#269;enko, _Expansion in eigenfunctions of differential and other operators) (Russian), Dokl. Akad. Nauk SSSR (N.S.) __103__ (1955), 349&#8211;352, [MR73136](http://www.ams.org/mathscinet-getitem?mr=73136)

* [[I. M. Gel'fand]], N. Ja. Vilenkin, _Generalized functions_, vol. 4. Some applications of harmonic analysis. Equipped Hilbert spaces, Fizmatgiz, Moscow, 1961 [MR146653](http://www.ams.org/mathscinet-getitem?mr=146653), English transl. Acad. Press 1964 [MR173945](http://www.ams.org/mathscinet-getitem?mr=173945)

Related early works include 

* Ciprian Foia&#351;, _D&#233;compositions int&#233;grales des familles spectrales et semi-spectrales en op&#233;rateurs qui sortent de l'espace hilbertien_, Acta Sci. Math. Szeged __20__, 1959, 117&#8211;-155. [MR115092](http://www.ams.org/mathscinet-getitem?mr=115092)

John Roberts continued the study in the context of [[quantum mechanics]] (in his thesis work suggested by [[Paul Dirac]]), changing the name to rigged.

* [[John Roberts]], _The Dirac bra and ket formalism_, J. Mathematical Phys. 7 (1966), 1097--1104, [MR216836](http://www.ams.org/mathscinet-getitem?mr=216836), _Rigged Hilbert spaces in quantum mechanics_ , Comm. Math. Physics __3__, n. 2 (1966), 98--119, [MR228243](http://www.ams.org/mathscinet-getitem?mr=228243), [euclid](http://projecteuclid.org/euclid.cmp/1103839388)

#### Modern references and links

* [[rigged Hilbert space]]

* wikipedia [rigged Hilbert space](http://en.wikipedia.org/wiki/Rigged_Hilbert_space)

* &#1056;. &#1040;. &#1052;&#1080;&#1085;&#1083;&#1086;&#1089;, [&#1054;&#1089;&#1085;&#1072;&#1097;&#1077;&#1085;&#1085;&#1086;&#1077; &#1075;&#1080;&#1083;&#1100;&#1073;&#1077;&#1088;&#1090;&#1086;&#1074;&#1086; &#1087;&#1088;&#1086;&#1089;&#1090;&#1088;&#1072;&#1085;&#1089;&#1090;&#1074;&#1086;](http://dic.academic.ru/dic.nsf/enc_mathematics/3760/%D0%9E%D0%A1%D0%9D%D0%90%D0%A9%D0%95%D0%9D%D0%9D%D0%9E%D0%95), online article from (Soviet) Matem. enc.

* MathOverflow question: [good-references-for-rigged-hilbert-spaces](http://mathoverflow.net/questions/43313/good-references-for-rigged-hilbert-spaces)

* Feichtinger, _A Banach Gelfand triple framework for
regularization and approximation_, [slides pdf](http://www.univie.ac.at/nuhag-php/dateien/talks/1086_eucetifeislides.pdf)

A unification of various inequivalent approaches is claimed in 

* M. Gadella, F. G&#243;mez, _A unified mathematical formalism for the Dirac
formulation of quantum mechanics_  Foundations of Physics __32__, No. 6, (2002)

* S. Wickramasekara, A. Bohm, _Symmetry representations in the rigged Hilbert space formulation of quantum mechanics_, [math-ph/0302018](http://arxiv.org/abs/math-ph/0302018)

[[!redirects Gelfand triple]]
[[!redirects enriched Hilbert space]]
[[!redirects equipped Hilbert space]]