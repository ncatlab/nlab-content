
[[!redirects Craig's interpolation theorem]]
[[!redirects Craig interpolation lemma]]
[[!redirects interpolation theorem]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea
The _Craig interpolation theorem_ is a basic result in the [[model theory]] of [[first-order logic]].

First proved by W. Craig for classical predicate calculus in 1957, it has been extended to [[intuitionistic logic]] by K. Sch&#252;tte in 1962.
Andrew M. Pitts and [[Michael Makkai]] have proved variants in categorical logic e.g. for [[pretoposes]]. Diaconescu proved an abstract variant in _institution-independent model theory_ (cf. Augier-Barbier(2007), Diaconescu(2008)).

**Craig interpolation theorem.** Let $\varphi_1,\varphi_2$ be first-order sentences over the vocabularies $\mathcal{L}_1,\mathcal{L}_2$ such that $\varphi_1\models\varphi_2$. Then there is a sentence $\theta$ over the common vocabulary $\mathcal{L}_1\cap\mathcal{L}_2$, the _interpolant_, such that $\varphi_1\models\theta$ and $\theta\models\varphi_2$. 

An important corollary is the [[Beth definability theorem]].

The theorem plays an important role in [[abstract model theory]] where the question whether the Craig interpolation property can take over the role of the [[Löwenheim-Skolem theorem]] in [[Lindström's theorems]], has been called 'one of the main open problems of the field' by V&#228;&#228;n&#228;nen (2008, p.404).


## Related Concepts

* [[definability]]
* [[first-order logic]]
* [[Beth definability theorem]]
* [[Löwenheim-Skolem theorem]]
* [[Robinson consistency theorem]]
* [[conceptual completeness]]
* [[abstract model theory]]
* [[descent theory]]

##References

The original source is

* William Craig, _Linear Reasoning. A new form of the Herbrand-Gentzen theorem_ , JSL *22* (1957) pp.250-268.

* William Craig, _Three uses of the Herbrand-Gentzen Theorem in relating model theory and proof theory_, JSL **22** (1957) pp.269-285.

For an account in a standard reference see:

* C. C. Chang, H. J. Keisler, _Model Theory_ , North-Holland Amsterdam 1973.

A textbook account that covers the classical as well as the intuitionistic case is in:

* [[John Bell]], Mosh&#233; Machover, _A Course in Mathematical Logic_ , North-Holland Amsterdam 1977.

For a proof that uses Keisler's ultrapower theorem (Roughly: $\mathcal{A}\equiv\mathcal{B}$ iff $\mathcal{A}^I/F\cong\mathcal{B}^I/G$ for some ultrafilters $F,G$ on I) see:

* [[John Bell]], A. B. Slomson, _Models and Ultraproducts: An Introduction_ , North-Holland Amsterdam 1969. 

The bible on interpolation in non-classical logic is:

* Dov Gabbay, Larisa Maksimova, _Interpolation and Definability - Modal and Intuitionistic Logics_ , Oxford UP 2005.

The following provides background on proofs of Craig's theorem and categorical logic in a gentle way:

* [[Michael Makkai]], _On Gabbay's Proof of the Craig Interpolation Theorem for Intuitionistic Predicate Logic_, Notre Dame J. Form. Logic **36** no. 3 (1995) pp.364-381. ([pdf](http://projecteuclid.org/download/pdf_1/euclid.ndjfl/1040149353))

* M. Aiguier, F. Barbier, _An institution-independent Proof of the Beth Definability Theorem_ , Studia Logica **85** no. 3 (2007) pp.333-359. ([pdf](http://perso.ecp.fr/~aiguierm/publications/communications/sl07.pdf))

* Razvan Diaconescu, _Institution-indepent Model Theory_ , Birkh&#228;user Basel 2008.

* Andrew M. Pitts, _Amalgamation and Interpolation in the Category of Heyting algebras_ , JPAA **29** (1983) pp.155-165.

* Andrew M. Pitts, _An Application of Open Maps to Categorical Logic_ , JPAA **29** (1983) pp.313-326.

* [[Jouko Väänänen]], _The Craig Interpolation Theorem and abstract model  theory_ , Synthese  164:401 (2008) (freely available online)