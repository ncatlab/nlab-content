
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There is a noticeable [[analogy]] between phenomena ([[theorems]]) in the theory of [[number fields]] and those in the theory of [[function fields]] over [[finite fields]] ([Weil 39](#Weil39), [Iwasawa 69](#Iwasaw69), [Mazur-Wiles 83](#MazurWiles83)), hence between the theories of the two kinds of _[[global fields]]_. When regarding [[number theory]] dually as [[arithmetic geometry]], then one may see that this analogy extends further to include [[complex analytic geometry]], the theory of [[complex curves]] (e.g. [Frenkel 05](#Frenkel05)). 

At a very basic level the analogy may be plausible from the fact that both the [[integers]] $\mathbb{Z}$ as well as the [[polynomial rings]] $\mathbb{F}_q[x]$ (over [[finite fields]] $\mathbb{F}_q$) are [[principal ideal domains]] with [[finite group|finite]] [[group of units]], all [[quotients]] being finite rings and with infinitely many [[prime ideals]], which already implies that a lot of [[arithmetic]] over these rings is similar. Since [[number fields]] are the [[finite number|finite]] [[dimension|dimensional]] [[field extensions]] of the [[field of fractions]] of $\mathbb{Z}$, namely the [[rational numbers]] $\mathbb{Q}$, and since [[function fields]] are just the finite-dimensional field extensions of the fields of fractions $\mathbb{F}_q(x)$ of $\mathbb{F}_q[x]$, this similarity plausibly extends to these extensions. 

The [[entire function|entire]] [[holomorphic functions]] on the [[complex plane]] are, while not quite an principal ideal domain, still a [[Bézout domain]], but in [[constructive mathematics]] the [[integers]] and the [[polynomial rings]] over [[finite fields]] are only Bézout domains as well.

But the analogy ranges much deeper than this similarity alone might suggest.
For instance ([Weil 39](#Weil39)) defined an invariant of a [[number field]] -- the _[[genus of a number field]]_-- which is analogous to the [[genus of a curve|genus]] of the [[algebraic curve]] on which a given [[function field]] is the [[rational functions]]. This is such as to make the statement of the [[Riemann-Roch theorem]] for [[algebraic curves]] extend to [[arithmetic geometry]] ([Neukirch 92, chapter II, prop.(3.6)](#Neukirch92)).

Another notable part of the analogy is the fact that there are natural analogs of the [[Riemann zeta function]] in all three columns of the analogy. This aspect has found attention notably through the lens of regarding [[number fields]] as [[rational functions]] on "[[arithmetic curves]] over the would-be [[field with one element]] $\mathbb{F}_1$".

The analogy between [[p-adic numbers]] and [[Laurent series]] over $\mathbb{F}_p$  is strengthened by ([Fontaine-Winterberger 79](#FontaineWinterberger79)), which shows that the absolute [[Galois groups]] of the [[perfect field|perfection]] of $\mathbb{F}_p((t))$ and of $\mathbb{Q}_p[p^{\frac{1}{p^\infty}}]$ are [[isomorphism|isomorphic]]. For more review of this see also ([Hartl 06](#Hartl06)). (The generalization of this to higher dimensions is the topic of [[perfectoid spaces]].) 


It is also the function field analogy which induces the conjecture of the [[geometric Langlands correspondence]] by analogy from the number-theoretic [[Langlands correspondence]]. Here one finds that the [[moduli stack of bundles]] over a [[complex curve]] is analogous in absolute [[arithmetic geometry]] to the [[coset space]] of the [[general linear group]] with coefficients in the [[ring of adeles]] of a number field, on which [[unramified]] [[automorphic representations]] are functions. Under this analogy the [[Weil conjecture on Tamagawa numbers]] may be regarded as giving the [[groupoid cardinality]] of the [[moduli stack of bundles]] in [[arithmetic geometry]].

In summary then the analogy says that the theory of [[number fields]] and of [[function fields]] both looks much like a [[global analytic geometry]]-version of the theory [[complex curves]].


## Formalizations
 {#Formalizations}

To date the function field analogy remains just that, an [[analogy]], though various research programs may be thought of as trying to provide a context in which the analogy would become a consequence of a systematic theory (see e.g. the introduction of [v.d. Geer et al 05](#vdGeer05)). This includes 

* [[Arakelov geometry]];

* [[global analytic geometry]].

* geometry "over [[F1]]".

Regarding the last point, in particular [[Borger's absolute geometry]] ([Borger 09](#Borger09)) makes precise the analogy between [[Spec(Z)]] and the [[polynomial ring]] $k[z]$/[[entire holomorphic function]]-ring $\mathcal{O}_{\mathbb{C}}$ by interpreting the analog of the canonical [[derivation]] $\frac{\partial}{\partial z}$ on the latter two as the [[Fermat quotient]] operation, and more generally by interpreting the lift of this to arithmetic spaces over ${Spec}(\mathbb{Z})$ as lifts of [[Frobenius homomorphisms]] as given by [[Lambda-ring]] structures. See at _[Borger's absolute geometry -- Motivation](Borger%27s+absolute+geometry#Motivation)_ for more on this.

  In this context the analogy between geometry over [[number fields]] and over [[function fields]] is made precise by showing ([Borger 09, section 7](#Borger09)) that for any smooth connected curve $S/\mathbb{F}_q$ over a [[finite field]] $\mathbb{F}_q$ the standard [[geometric morphism]] of ("big") [[toposes]]

  $$
    Spec(S/\mathbb{F}_q)\longrightarrow Spec(\mathbb{F}_q)
  $$

  factors through an alternative base topos $\widetilde Spec(\mathbb{F}_q)$

  $$
    Spec(S/\mathbb{F}_q)\longrightarrow \widetilde Spec(\mathbb{F}_q) \longrightarrow Spec(\mathbb{F}_q)
  $$

  which, while different from $Spec(\mathbb{F}_q)$ is "close" to $Spec(\mathbb{F}_q)$ in some precise sense, but which has the advantage that its construction does exist for $q = 1$ in that there is directly analogous

  $$
    Spec(\mathbb{Z}) \longrightarrow \widetilde Spec(\mathbb{F}_1)
    \,,
  $$

  where the notation $\widetilde Spec(\mathbb{F}_1)$ here stands for Borger's the topos over [[Lambda-rings]], see at _[[Borger's absolute geometry]]_ for the actual details.

## Overview
 {#Overview}

[[!include function field analogy -- table]]

$\,$

[[!include Langlands analogies -- table]]

## Related concepts

* [[MKR analogy]] in [[arithmetic topology]]

## References

Original articles includes

* {#Weil39} [[André Weil]], _Sur l'analogie entre les corps de nombres alg&#233;brique et les corps de fonctions alg&#233;brique_, Revue Scient. 77, 104-106, 1939

* {#Iwasaw69} [[Kenkichi Iwasawa]], _Analogies between number fields and function fields_, in _Some Recent Advances in the Basic Sciences_, Vol. 2 (Proc. Annual Sci. Conf., Belfer Grad. School Sci., Yeshiva Univ., New York, 1965-1966), Belfer Graduate School of Science, Yeshiva Univ., New York, pp. 203&#8211;208, [MR 0255510](http://www.ams.org/mathscinet-getitem?mr=0255510)

  for more on this see: Wikipedia, _[Main conjecture of Iwasawa theory](http://en.wikipedia.org/wiki/Main_conjecture_of_Iwasawa_theory)_

* {#FontaineWinterberger79} [[Jean-Marc Fontaine]], [[Jean-Pierre Wintenberger]], _Extensions alg&#233;brique et corps des normes des extensions APF des corps locaux_, C. R. Acad. Sci. Paris S&#233;r. A&#8211;B 288(8) (1979), A441&#8211;A444

* {#MazurWiles83} [[Barry Mazur]], [[Andrew Wiles]], _Analogies between function fields and number fields_, American Journal of Mathematics Vol. 105, No. 2 (Apr., 1983), pp. 507-521 ([JStor](http://www.jstor.org/stable/2374266))

Textbook accounts include

* {#Neukirch92} [[Jürgen Neukirch]], _Algebraische Zahlentheorie_ (1992), English translation _Algebraic Number Theory_,  Grundlehren der Mathematischen Wissenschaften 322, 1999 ([pdf](http://www.plouffe.fr/simon/math/Algebraic%20Number%20Theory.pdf))

* {#Rosen02} Michael Rosen, _Number theory in function fields_, Graduate texts in mathematics, 2002

Tables showing the parallels between number fields and function fields are in

* {#Goss92} [[David Goss]] _Dictionary_, in David Goss, David R. Hayes, Michael Rosen (eds.) _The Arithmetic of Function Fields_, Ohio State Univ. Math. Res. Inst. Publ., 2, de Gruyter, Berlin, 1992,  pp. 475-482, 

* {#Poonen06} [[Bjorn Poonen]], section 2.6 of _Lectures on rational points on curves_, 2006 ([pdf](http://math.mit.edu/~poonen/papers/curves.pdf))

* {#Hartl06} [[Urs Hartl]], _A Dictionary between Fontaine-Theory and its Analogue in Equal Characteristic_ ([arXiv:math/0607182](http://arxiv.org/abs/math/0607182))

See also

* M. Blickle,[[Hélène Esnault]], K. R&#252;lling, _Characteristic $0$ and $p$ analogies, and somemotivic cohomology_ ([[EsnaultAnalogy.pdf:file]])

A collection of more recent developments is in

* {#vdGeer05} van der Geer et al (eds.) _Number Fields and Function Fields &#8211; Two Parallel Worlds_, Birkh&#228;user 2005 ([publisher page](http://www.springer.com/birkhauser/mathematics/book/978-0-8176-4397-3))

Discussion including also the complex-analytic side includes

* {#Frenkel05} [[Edward Frenkel]], section 2 of _Lectures on the Langlands Program and Conformal Field Theory_ ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172)).

and a comparison of the number theory to that of [[foliations]] is in 

* {#Deninger07} [[Christopher Deninger]], _Analogies between analysis on foliated spaces and arithmetic geometry_ ([arXiv:0709.2801](http://arxiv.org/abs/0709.2801))

An actual formalization of the analogy between geometry over number fields and function fields is in 

* {#Borger09} [[James Borger]], section 7 of _Lambda-rings and the field with one element_ ([arXiv/0906.3146](http://arxiv.org/abs/0906.3146))