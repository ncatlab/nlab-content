
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

Various concepts in [[philosophy]] and [[mathematics]] go by the name *monad*.


## Historical origins
 {#HistoricalOrigins}

On the historical origin of the notion, cf. eg. [Gordon, Kusraev & Kutateladze 2002, §2.2.7](#GordonKusraevKutateladze02); [Kutateladze 2006](#Kutateladze06):

### Euclid: Monads as conceptual units
 {#Euclid}

[[Euclid]] used "monad" (*μονάς*, stem: *μοναδ*-) in [Book VII](http://aleph0.clarku.edu/~djoyce/elements/bookVII/defVII1.html) of the *[[Elements]]* ($\sim$300 BC) in the following way:

> {#ElementsVIIDef1} **Book VII, Definition 1**: 

> [mονάς ἐστιν, καθ' ἣν ἕκαστον τῶν ὄντων ἓν λέγεται](https://www.perseus.tufts.edu/hopper/text?doc=Euc.+7.Def.1&fromdoc=Perseus%3Atext%3A1999.01.0085)

> A *monad* is that by virtue of which each of the things that exist is called one.

> {#ElementsVIIDef2} **Book VII, Definition 2**: 

> [ἀριθμὸς δὲ τὸ ἐκ μονάδων συγκείμενον πλῆθος](https://www.perseus.tufts.edu/hopper/text?doc=Euc.+7.def.2&fromdoc=Perseus%3Atext%3A1999.01.0085)

> A *number* is a multitude composed of monads.

[[Sextus Empiricus]] (2nd century AD) expands on this as follows: 

> A whole as such is indivisible and a monad, since it is a monad, is not divisible. Or, if it splits into many pieces it becomes a union of many monads rather than a &lbrack;simple&rbrack; monad.


The term "monad" (*μονάς*) here is traditionally translated as "unit" without mentioning of the original terminology.

More explicitly, [Kutateladze 2006](#Kutateladze06) ([p. 2](https://arxiv.org/pdf/math/0608298.pdf#page=2)) suggests to understand this as *conceptual units for the purpose of counting*  -- and thus to read the phrase "is called one" in [Def. 1](#ElementsVIIDef1) in the sense of counting, as in: "one sheep here, another one there" -- which happens *by virtue* of an identification (what today we would call a [[bijection]] with a [[finite set]]): While sheep are not atoms, we still regard them as "indivisible units of sheep" for the purpose of counting them.

This brings out the distinction between Euclid's notion of monads and that of geometrical points from [Book I](http://aleph0.clarku.edu/~djoyce/elements/bookI/defI1.html) of the *[[Elements]]*:

> **Book I, Definition 1**

> [Σημεῖόν ἐστιν, οὗ μέρος οὐθέν.](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0085%3Abook%3D1%3Atype%3Ddef%3Anumber%3D1)

> A point is that which has no part.

While sheep are not actually without parts, we do have a "monadic" notion of their *conceptual* indivisible unit by virtue of which we call any sheep "one sheep" such as to count them *one-by-one*.

In summary: 

<center>
Where Euclid's points are atoms in the sense of [[geometry]], 
</br>
so his monads are units in the sense of [[arithmetic]].
</center>


### Middle Ages and Early Modern Period: Monads as metaphysical units
 {#MiddleAges}

In the middle ages the primarily mathematical monad terminology of the ancients ([above](#Euclid)) receives a metaphysical and/or spiritual or even religious connotation, as in

* [[Giordano Bruno]], *[De triplici minimo](https://www.digitale-sammlungen.de/de/view/bsb10205694?page=1)* (1591)

who asserts that:

> the substance of things is the minimum, of which there are three principal varieties: the general metaphysical minimum or *monad*; the corporeal minimum or *atom*; and the geometrical minimum or *point*

This according to:

* Edward P. Butler, *Transformation and Individuation
in Giordano Bruno’s Monadology*, Socrates **3** 2 (2015) 57-70 &lbrack;[philpapers](https://philpapers.org/versions/BUTTAI-2), [pdf](https://philarchive.org/archive/BUTTAI-2)&rbrack;


{#LeibnizMonads} Later [[Leibniz]]'s *[Monadology](https://en.wikipedia.org/wiki/Monadology)* (1714) continues to insist on including "souls" and "god" among monads in a way that is more mysterious if not puzzling.

Despite (or because?) the esoteric if not irrational nature of Leibniz' monadology it has become the most widely remembered usage of the "monad" terminology, while its rational origin with Euclid is nearly forgotten (for instance  *<a href="https://en.wikipedia.org/wiki/Monad_(philosophy)">Wikipedia's entry</a>* does not know of Euclid). 

On the other hand, both Leibniz and Bruno may have been following a tradition of thought that originated deeper in the middle ages:

> the striking similarities between aspects of Leibniz’s monadology and Bruno’s doctrine of minims are probably attributable to the sources and philosophical interests that they shared in common

This according to

* Dilwyn Knox, *[Giordano Bruno](https://plato.stanford.edu/Archives/spr2023/entries/bruno/)*, Stanford Encyclopedia of Philosophy (2019)





## Monads of infinitesimals
 {#MonadsOfInfinitesimals}

It certainly seems (but remains implicit) that [Robinson 1966 (p. 57)](nonstandard+analysis#Robinson66) meant to follow Euclid's (and maybe Leibniz's) terminology when introducing the notion of 

* *[[monad in nonstandard analysis]]* 

referring to [[infinitesimal neighbourhoods]] in [[nonstandard analysis]] (as such also used in [[synthetic differential geometry]], cf. [Kock 1980](infinitesimal+neighborhood#Kock80)).

While the [[infinitesimal neighbourhood]] of a point is more than that point, it does not contain any two distinct ([[global element|global]]) [[points]] and in this sense is indivisible, whence the "monad"-terminology here seems to match well with the [original notion by Euclid](#Euclid).


## Monads on categories
 {#MonadsOnCategories}

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

## Monads of computational effects
 {#MonadsOfComputationalEffects}

The notion of monads in [[computer science]] -- as a model for computational *effects* within otherwise [[functional programming languages]] -- is directly related to the [above](#MonadsOnCategories) notion of monads on categories (the category in question now being the data [[type system]]). See at *[[monad in computer science]]* for more.

Notice in this context that, for $\mathcal{E}$ an effect monad, $\mathcal{E}$-effectful programs (see [there](monad+in+computer+science#BasicIdea)) cannot sensibly interact with plain programs unless and until they are "taken out of the monad"  (namely out of its [[Kleisli category]], or "out from under the monad symbol") by an *$\mathcal{E}$-effect handler* (see [there](monad+in+computer+science#MonadModulesInIdeaSection)). In this sense, computational effect monads have some semblance of the mutual isolation that some philosophers may associate with monads.


## Other

Finally, there is the term

* *[[Beilinson monad]]*

(maybe not widely used) which may be trying to evoke the picture not of an infinitesimal but a "[[homological algebra|homological]]" neighbourhood.

## References

The Wikipedia entry knows various further historical writings on monads (but does not mention their role in Euclid's *[[Elements]]*):

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Monad_(philosophy)">Monad (philosophy)</a>*

On [[monad in nonstandard analysis|monads in]] [[nonstandard analysis]] with attention to the historical origin of the term:

* {#GordonKusraevKutateladze02} E. I. Gordon, A. G. Kusraev, [[Semën S. Kutateladze]], *Infinitesimal Analysis*, Mathematics and its Applications **544**, Springer (2002) &lbrack;[doi:10.1007/978-94-017-0063-4](https://doi.org/10.1007/978-94-017-0063-4)&rbrack;

* {#Kutateladze06} [[Semën S. Kutateladze]], *Leibniz's Definition of Monad*, NeuroQuantology **4** 3 (2006) 249-241 &lbrack;[arXiv:math/0608298](https://arxiv.org/abs/math/0608298), [pdf](https://www.researchgate.net/profile/Semen-Kutateladze/publication/2130297_Leibniz%27s_Definition_of_Monad/links/0912f5058405405dbb000000/Leibnizs-Definition-of-Monad.pdf)&rbrack;



category: disambiguation

[[!redirects monad disambiguation]]
[[!redirects monad terminology]]


