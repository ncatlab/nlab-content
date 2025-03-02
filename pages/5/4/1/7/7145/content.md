
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

\linebreak

Various concepts in [[philosophy]] and [[mathematics]] go by the name *monad*. There is a surprising (if partly accidental) coherence in these notions from [[Euclid]] all the way to the modern mathematical usage -- if one disregards the long dark medieval use of the term.


## Historical origins
 {#HistoricalOrigins}


### Euclid: Monads as conceptual/arithmetic units
 {#Euclid}

On the historical origin of the notion in a mathematical sense, cf. eg. [Gordon, Kusraev & Kutateladze 2002, §2.2.7](#GordonKusraevKutateladze02); [Kutateladze 2006](#Kutateladze06):

[[Euclid]] used "monad" (*μονάς*, stem: *μοναδ*-) in [Book VII](http://aleph0.clarku.edu/~djoyce/elements/bookVII/defVII1.html) of the *[[Elements]]* ($\sim$300 BC) in the following way:

> {#ElementsVIIDef1} **Book VII, Definition 1**: 

> mονάς ἐστιν, καθ' ἣν ἕκαστον τῶν ὄντων ἓν λέγεται. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Euc.+7.Def.1&fromdoc=Perseus%3Atext%3A1999.01.0085))

> A monad is that by virtue of which each of the things that exist is called one. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0086%3Abook%3D7%3Atype%3Ddef%3Anumber%3D1))

> {#ElementsVIIDef2} **Book VII, Definition 2**: 

> ἀριθμὸς δὲ τὸ ἐκ μονάδων συγκείμενον πλῆθος. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Euc.+7.def.2&fromdoc=Perseus%3Atext%3A1999.01.0085))

> A number is a multitude composed of monads. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0086%3Abook%3D7%3Atype%3Ddef%3Anumber%3D2))

[[Sextus Empiricus]] (2nd century AD) expands on this as follows: 

> A whole as such is indivisible and a monad, since it is a monad, is not divisible. Or, if it splits into many pieces it becomes a union of many monads rather than a &lbrack;simple&rbrack; monad.


The term "monad" (*μονάς*) here is traditionally translated as "unit" without mentioning of the original terminology.

More explicitly, [Kutateladze 2006](#Kutateladze06) ([p. 2](https://arxiv.org/pdf/math/0608298.pdf#page=2)) suggests to understand this as *conceptual units for the purpose of counting*  -- and thus to read the phrase "is called one" in [Def. 1](#ElementsVIIDef1) in the sense of counting, as in: "one sheep here, another one there" -- which happens *by virtue* of an identification (what today we would call a [[bijection]] with a [[finite set]]): While sheep are not atoms, we still regard them as "indivisible units of sheep" for the purpose of counting them.

This brings out the distinction between Euclid's notion of monads and that of geometrical points from [Book I](http://aleph0.clarku.edu/~djoyce/elements/bookI/defI1.html) of the *[[Elements]]*:

> **Book I, Definition 1**

> Σημεῖόν ἐστιν, οὗ μέρος οὐθέν. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0085%3Abook%3D1%3Atype%3Ddef%3Anumber%3D1))

> A point is that which has no part. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0086%3Abook%3D1%3Atype%3Ddef%3Anumber%3D1))

While sheep are not actually without parts, we do have a "monadic" notion of their *conceptual* indivisible unit by virtue of which we call any sheep "one sheep" such as to count them *one-by-one*.

In summary: 

<center>
Where Euclid's points are atoms in the sense of [[geometry]], 
</br>
so his monads are units in the sense of [[arithmetic]].
</center>

This also becomes clear by the way in which the concept of monad is used further in Book VII of [[Euclid]]'s *[[Elements]]*:

> {#ElementsVIIDef7} **Book VII, Definition 7**: 

> περισσὸς δὲ ὁ μὴ διαιρούμενος δίχα ἢ ὁ μονάδι διαφέρων ἀρτίου ἀριθμοῦ. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0085%3Abook%3D7%3Atype%3Ddef%3Anumber%3D7))

> An odd number is that which is not divisible into two equal parts, or that which differs by a monad from an even number. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0086%3Abook%3D7%3Atype%3Ddef%3Anumber%3D7))

> {#ElementsVIIDef15} **Book VII, Definition 15**: 

> ἀριθμὸς ἀριθμὸν πολλαπλασιάζειν λέγεται, ὅταν, ὅσαι εἰσὶν ἐν αὐτῷ μονάδες, τοσαυτάκις συντεθῇ ὁ πολλαπλασιαζόμενος, καὶ γένηταί τις. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0085%3Abook%3D7%3Atype%3Ddef%3Anumber%3D15))

> A number is said to multiply a number when that which is multiplied is added to itself as many times as there are monads in the other, and thus some number is produced. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0086%3Abook%3D7%3Atype%3Ddef%3Anumber%3D15))

These definitions evidently refer by "monad" to the element "[[1]]" among the natural numbers. 


Other definitions in *[[Elements]]* VII also refer to monads as the *multiplicative [[unit]]* element of the [[ring]] of [[natural numbers]]. To see this one first has to notice that Euclid speaks of (natural) numbers being "measured" by a *lesser* number where we today say they are "divided" by a smaller number:

> {#ElementsVIIDef5} **Book VII, Definition 5**: 

> πολλαπλάσιος δὲ ὁ μείζων τοῦ ἐλάσσονος, ὅταν καταμετρῆται ὑπὸ τοῦ ἐλάσσονος. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0085%3Abook%3D7%3Atype%3Ddef%3Anumber%3D5))

> The greater number is a multiple of the less when it is measured by the less. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0086%3Abook%3D7%3Atype%3Ddef%3Anumber%3D15))

With that understood, we see Euclid's crystal clear definition of [[prime numbers]]:

> {#ElementsVIIDef11} **Book VII, Definition 11**: 

> πρῶτος ἀριθμός ἐστιν ὁ μονάδι μόνῃ μετρούμενος. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0085%3Abook%3D7%3Atype%3Ddef%3Anumber%3D11))

> A prime number is that which is measured by a monad alone. ([source](https://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0086%3Abook%3D7%3Atype%3Ddef%3Anumber%3D11))


The use of the term "monad" as in "unit" appears again in *Introduction to Arithmetics* by [[Nicomachus of Gerasa]] (c. 60 – c. 120 AD). For example, in Book 1 Chapter 7 (e.g. [Balboa and Balboa 21](#Balboa21)) he states:

> Number Is Limited/Definite/Bounded Multitude or a Composition of Monads/Units or A Flow of Quantity composed out of Monads/Units;

> Αριθµος εστι ωρισµενον πληθος η συστηµα µοναδων η χυµα ποσσοτητος συγκειµενον εκ µοναδων;

> On the one hand, The Even is, That which can be Divided into Two Equal Parts without A Monad/Unit Intervening in The Middle; whereas on the other hand, The Odd is That which cannot be Cut/Divided into Two Equal Parts by the before-mentioned Intervention of The Monad/Unit.

> µεν αρτιον εστι, ο οιον διαιρεθηναι τε εις δυο ισα µη µοναδος παρεµπιπτουσης µεσον, δε περιττον το µη δυναµενον µερισ− εις δυο ισα −θηναι δια την προειρηµενην µεσιτειαν την µοναδος.

Part I of the [D'Ooge 1926](#Dooge26) translation of *Introduction to Arithmetics* contains further discussion about the concept of the monad in other mathematical texts (e.g. Theon of Alexandria (p.37), Iamblichus (p.96, 127), and Boethius (p. 134)).



### Middle ages: Monads as metaphysical units
 {#metaphysics}

The primarily mathematical notion of "monad" by the ancients ([above](#Euclid)) later receives a religious/[[gnosticism|gnostic]] connotation, following [[Pythagorean]] and later neo-Platonic doctrines. 

{#Monoimus} Wikipedia claims that an Arab gnostic known as *[Monoimus](https://en.wikipedia.org/wiki/Monoimus)* (150-210 AD) "is known for coining the usage of the word *Monad* in a Gnostic context."

{#BookOf24Philosophers} Then there is the first line in the "*Book of 24 Philophers*" (~1200 AD) sometimes (such as by Aquinus below) attributed to [Hermes Trismegistus](https://en.wikipedia.org/wiki/Hermes_Trismegistus):

> *Deus est monas monadem gignens is se unum reflectens ardorem.*

> &lbrack;Latin original according to [Vinzent 2012](#Vinzent12)&rbrack;

\begin{imagefromfile}
    "file_name": "Litwa-BookOf24Philosophers.jpg",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    },
    "caption": "(from [Litwa 2019](#Litwa19))"
\end{imagefromfile}


This line is quoted by [Thomas Aquinas](https://en.wikipedia.org/wiki/Thomas_Aquinas) (13th century) in his *Summa Theologica* (see eg. [here](https://www.ccel.org/ccel/aquinas/summa.FP_Q32_A1.html)) as support for his claim that "the trinity of the divine persons can be known by natural reason".

A metaphysical line of thought on "monads" continues in the Early Modern period, as with

* [[Giordano Bruno]], *[De triplici minimo](https://www.digitale-sammlungen.de/de/view/bsb10205694?page=1)* (1591)

who asserts that:

> the substance of things is the minimum, of which there are three principal varieties: the general metaphysical minimum or *monad*; the corporeal minimum or *atom*; and the geometrical minimum or *point*

This according to:

* Edward P. Butler, *Transformation and Individuation
in Giordano Bruno’s Monadology*, Socrates **3** 2 (2015) 57-70 &lbrack;[philpapers](https://philpapers.org/versions/BUTTAI-2), [pdf](https://philarchive.org/archive/BUTTAI-2)&rbrack;


{#LeibnizMonads} Later [[Leibniz]]'s *[Monadology](https://en.wikipedia.org/wiki/Monadology)* (1714) continues to insist on including "souls" and "god" among monads in a way that remains mysterious if not puzzling.

Despite (or because of?) the esoteric if not irrational nature of Leibniz' monadology it has become the most widely remembered usage of "monad", while its rational origin with Euclid is nearly forgotten (for instance Wikipedia's [entries](#WikipediaMonadPhiliosophy) do not mention Euclid). 

At the same time, both Leibniz and Bruno seem to have been following a tradition of thought that originated deeper in the middle ages:

> the striking similarities between aspects of Leibniz’s monadology and Bruno’s doctrine of minims are probably attributable to the sources and philosophical interests that they shared in common

This according to

* Dilwyn Knox, *[Giordano Bruno](https://plato.stanford.edu/Archives/spr2023/entries/bruno/)*, Stanford Encyclopedia of Philosophy (2019)



## Modern mathematical notions

In the second half of the 20th century a couple of definitions in rigorous modern mathematics are introduced under the name of "monads":

### Monads of infinitesimals
 {#MonadsOfInfinitesimals}

It certainly seems (but remains implicit) that [Robinson 1966 (p. 57)](nonstandard+analysis#Robinson66) meant to follow Euclid's and/or Leibniz's terminology when introducing the notion of 

* *[[monad in nonstandard analysis]]* 

meaning [[infinitesimal neighbourhoods]] in [[nonstandard analysis]] (as such also used in [[synthetic differential geometry]], cf. [Kock 1980](infinitesimal+neighborhood#Kock80)).

([Robinson 1966](nonstandard+analysis#Robinson66) refers to Leibniz extensively, but always with respect to Leibniz's discussion of [[differential calculus|differential]] [[calculus]], not though regarding Leibniz's *Monadology*.)

While the [[infinitesimal neighbourhood]] of a point is more than that point, it does not contain any two distinct ([[global element|global]]) [[points]] and in this sense is indivisible, whence the "monad"-terminology here seems to match well with the [original notion by Euclid](#Euclid).


### Monads on categories
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

Notice that [Bénabou 1967, p. 39](monad#Bénabou67) follows the tradition of denoting a [[terminal object]] (here: the [[terminal category]]) by the symbol "$1$" for the [[unit]] [[natural number]],  exhibiting his [[monads]] as (lax) [[images]] of "1" (in a [[2-category]] such as [[Cat]]) ---
which makes for a rather strong resonance with Euclid's notion of monads ([above](#Euclid)).

At the same time, with hindsight one may notice that the construction of infinitesimal monads in the [above](MonadsOfInfinitesimals) sense of [[infinitesimal neighbourhoods]] is (see [there](infinitesimal+disk+bundle#MonadicityAdjointToJetBundles)) in fact an example of a monad in the sense of categorical algebra.

### Monads of computational effects
 {#MonadsOfComputationalEffects}

The notion of monads in [[computer science]] -- as a model for "forms of computation" with computational *effects* within otherwise [[functional programming languages]] &lbrack;[Moggi 1989](monad+in+computer+science#Moggi89)&rbrack; -- is an equivalent perspective (cf. [[Kleisli triple]]) of the [above](#MonadsOnCategories) notion of monads on categories (the category in question now being the data [[type system]]). See at *[[monad in computer science]]* for more.

Notice in this context that, for $\mathcal{E}$ an effect monad, $\mathcal{E}$-effectful programs (see [there](monad+in+computer+science#BasicIdea)) cannot sensibly interact with plain programs unless and until they are "taken out of the monad"  (namely out of its [[Kleisli category]], or "out from under the monad symbol") by an *$\mathcal{E}$-effect handler* (see [there](monad+in+computer+science#MonadModulesInIdeaSection)). In this sense, computational effect monads have some semblance of the mutual isolation that some philosophers may associate with monads.


### Other

Finally, there is the term

* *[[Beilinson monad]]*

(maybe not widely used) which may be trying to evoke the picture not of an infinitesimal but a "[[homological algebra|homological]]" neighbourhood.

## Conclusion

If we disregard the arguably (and often expressedly) non-rational (eg. gnostic) discussion of "monads" in the middle ages (understood very broadly, ranging from [Monoimus](https://en.wikipedia.org/wiki/Monoimus) in the 2nd century over hermetics in the 12th century AD to [[Leibniz]] in the 17th century), then there is --- contrary to what may be the common perception --- a fairly coherent concept (probably partly intentionally, but partly by happy coincidence) connecting [[Euclid]] (4th century BC) to the mathematics of the second half of the 20th century: [Robinson 1966 (p. 57)](nonstandard+analysis#Robinson66), [Bénabou 1967, p. 39](monad#Bénabou67) and [Moggi 1989](monad+in+computer+science#Moggi89)).


## References

The ancient mathematical notion of monads as arithmetic units:

* [[Euclid]], *[[Elements]]* Book VII (~400-300 BC)

  translated by Thomas L. Heath (1956)

  [Perseus Digital Library](https://www.perseus.tufts.edu/hopper/text?doc=Euc.+1.&fromdoc=Perseus%3Atext%3A1999.01.0085)

which appears again in 

* [[Nicomachus]] of Gerasa: *Introduction to Arithmetic* (~90-~120 AD)

* {#Balboa21} interlinear translation by Juan and Maria Balboa &lbrack;[archive](https://archive.org/details/nicomachus-arithmetic-balboa)&rbrack;

* {#Dooge26} translation by D'Ooge (1926) &lbrack;[web](https://babel.hathitrust.org/cgi/pt?id=mdp.39015005675411&seq=9)&rbrack;




The gnostic notion of monads:

* *Book of the Twenty-Four Philosophers* (~1200 AD)

  &lbrack;[Wikipedia entry](https://en.wikipedia.org/wiki/Book_of_the_24_Philosophers)&rbrack;

  reproduced (translated/commented) in:

  * {#Vinzent12} Markus Vinzent, *Liber viginti quattor philosophorum* (2012, 2015) &lbrack;original text:[web](http://markusvinzent.blogspot.com/2012/10/book-of-24-philosophers.html), English translation:[web](http://markusvinzent.blogspot.com/2015/02/liber-xxiv-philosophorum-book-of-24.html)&rbrack;

  * The Matheson Trust, *The Book of the Twenty-Four Philosophers* (2015) &lbrack;[pdf](https://www.themathesontrust.org/papers/metaphysics/XXIV-A4.pdf)&rbrack;

  * {#Litwa19} M David Litwa, *Hermetica II: The Excerpts of Stobaeus, Papyrus Fragments, and Ancient Testimonies in an English Translation with Notes and Introduction*, Cambridge University Press (2019) &lbrack;[doi:10.1017/9781316856567.057](https://doi.org/10.1017/9781316856567.057)&rbrack;

and quoted by

* Thomas Aquinas, *Summar Theologica* &lbrack;[Wikipedia entry](https://en.wikipedia.org/wiki/Summa_Theologica), [ccel.org](https://www.ccel.org/ccel/aquinas/summa.FP_Q32_A1.html)&rbrack; (~1250 AS)


The Wikipedia entries have further historical writings on monads (but do not mention their role in Euclid's *[[Elements]]*):

* {#WikipediaMonadPhiliosophy} Wikipedia, *<a href="https://en.wikipedia.org/wiki/Monad_(philosophy)">Monad (philosophy)</a>*

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Monad_(Gnosticism)">Monad (Gnosticism)</a>*


On [[monad in nonstandard analysis|monads in]] [[nonstandard analysis]] with attention to the historical origin of the term:

* {#GordonKusraevKutateladze02} E. I. Gordon, A. G. Kusraev, [[Semën S. Kutateladze]], *Infinitesimal Analysis*, Mathematics and its Applications **544**, Springer (2002) &lbrack;[doi:10.1007/978-94-017-0063-4](https://doi.org/10.1007/978-94-017-0063-4)&rbrack;

* {#Kutateladze06} [[Semën S. Kutateladze]], *Leibniz's Definition of Monad*, NeuroQuantology **4** 3 (2006) 249-241 &lbrack;[arXiv:math/0608298](https://arxiv.org/abs/math/0608298), [pdf](https://www.researchgate.net/profile/Semen-Kutateladze/publication/2130297_Leibniz%27s_Definition_of_Monad/links/0912f5058405405dbb000000/Leibnizs-Definition-of-Monad.pdf)&rbrack;

For extensive referencing of the mathematical notions of monads see there references there:

* [[monad in nonstandard analysis]]

* [[monad]] in [[categorical algebra]]

* [[monad in computer science]]


category: disambiguation

[[!redirects monad disambiguation]]
[[!redirects monad terminology]]


