
#Contents#
* table of contents
{:toc}

Various concepts in [[philosophy]] and [[mathematics]] go by the name *monad*.


## Historical origins
 {#HistoricalOrigins}

On the historical origin of the notion, cf. eg. [Gordon, Kusraev & Kutateladze 2002, §2.2.7](#GordonKusraevKutateladze02); [Kutateladze 2006](#Kutateladze06):

[[Euclid]] used "monad" (*μονάς*, stem: *μοναδ*-) in [Book VII](http://aleph0.clarku.edu/~djoyce/elements/bookVII/defVII1.html) of the *[[Elements]]* ($\sim$300 BC) in the following way:

> **Definition 1**: 

> [mονάς ἐστιν, καθ' ἣν ἕκαστον τῶν ὄντων ἓν λέγεται](https://www.perseus.tufts.edu/hopper/text?doc=Euc.+7.Def.1&fromdoc=Perseus%3Atext%3A1999.01.0085)

> A *monad* is that by virtue of which each of the things that exist is called one.

> **Definition 2**: 

> [ἀριθμὸς δὲ τὸ ἐκ μονάδων συγκείμενον πλῆθος](https://www.perseus.tufts.edu/hopper/text?doc=Euc.+7.def.2&fromdoc=Perseus%3Atext%3A1999.01.0085)

> A *number* is a multitude composed of monads.

The term "monad" (*μονάς*) in these two "definitions" is traditionally translated as "unit" ("with no sufficient ground for that", according to [GKK02, p. 18](#GordonKusraevKutateladze02)).

[[Sextus Empiricus]] (2nd century AD) expands on this as follows: 

> A whole as such is indivisible and a monad, since it is a monad, is not divisible. Or, if it splits into many pieces it becomes a union of many monads rather than a &lbrack;simple&rbrack; monad.


Later [[Leibniz]]'s *[Monadology](https://en.wikipedia.org/wiki/Monadology)* (1714) speaks of monads as *mind-like simple substances* in a way that is now more famous than Euclid's usage, but also more mysterious, if not puzzling.


## Monads of infinitesimals
 {#MonadsOfInfinitesimals}

It certainly seems (but remains implicit) that [Robinson 1966 (p. 57)](nonstandard+analysis#Robinson66) meant to follow Euclid's (and maybe Leibniz's) terminology when introducing the notion of 

* *[[monad in nonstandard analysis]]* 

referring to [[infinitesimal neighbourhoods]] in [[nonstandard analysis]] (as such also used in [[synthetic differential geometry]], cf. [Kock 1980](infinitesimal+neighborhood#Kock80)).

While the [[infinitesimal neighbourhood]] of a point is more than that point, it does not contain any two distinct ([[global element|global]]) [[points]] and in this sense is indivisible, whence the "monad"-terminology seems well-motivated here, in view of the [above](#HistoricalOrigins).


## Monads on categories

Just a few years later, [Bénabou 1967](monad#Bénabou67) introduces the term

* *[[monad]] in [[categorical algebra]]*

\begin{imagefromfile}
    "file_name": "Benabou-MonadDefinition.jpg",
    "float": "right",
    "width": 650,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [Bénabou 1967, p. 39](monad#Bénabou67))"
\end{imagefromfile}

Bénabou's explicit reasoning on this choice of terminology has not survived, but (see the historical discussion [there](monad#Etymology)) it is striking that he proceeds to (observe that it is equivalently possible to) define category-theoretic monads as [[lax 2-functors]] of the form $\ast \to Cat$, and hence as ([[global points|global]]) [[generalized element|elements]] or "units" in a [[2-category theory|2-category theoretic sense]]. 

At the same time, with hindsight one may notice that the construction of infinitesimal monads in the [above](MonadsOfInfinitesimals) sense of [[infinitesimal neighbourhoods]] is (see [there](infinitesimal+disk+bundle#MonadicityAdjointToJetBundles)) in fact an example of a monad in the sense of categorical algebra.

## Other

Finally, there is the term

* *[[Beilinson monad]]*

(maybe not widely used) which may be trying to evoke the picture not of an infinitesimal but a "[[homological algebra|homological]]" neighbourhood.

## References

* {#Kutateladze06} [[Semën S. Kutateladze]], *Leibniz's Definition of Monad*, NeuroQuantology **4** 3 (2006) 249-241 &lbrack;[arXiv:math/0608298](https://arxiv.org/abs/math/0608298), [pdf](https://www.researchgate.net/profile/Semen-Kutateladze/publication/2130297_Leibniz%27s_Definition_of_Monad/links/0912f5058405405dbb000000/Leibnizs-Definition-of-Monad.pdf)&rbrack;

* {#GordonKusraevKutateladze02} E. I. Gordon, A. G. Kusraev, [[Semën S. Kutateladze]], *Infinitesimal Analysis*, Mathematics and its Applications **544**, Springer (2002) &lbrack;[doi:10.1007/978-94-017-0063-4](https://doi.org/10.1007/978-94-017-0063-4)&rbrack;


category: disambiguation

[[!redirects monad terminology]]


