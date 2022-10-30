
> This page is about [[computability]] of fundamental [[physics]] in the sense of [[computable mathematics]] and [[constructive analysis]]. It is not about _[[computational physics]]_, though of course there is a relation. For computational [[complexity theory]] in physics see at [[computational complexity and physics]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The following idea or observation or sentiment has been expressed independently by many authors. We quote from [Szudzik 10, section 2](#Szudzik10):

> The central problem is that [[model (physics)|physical models]] use [[real numbers]] to represent the values of [[observable|observable quantities]], $[...]$ Careful consideration of this problem, however, reveals that the real numbers are not actually necessary in physical models. [[natural number|Non-negative integers]] suffice for the representation of observable quantities because numbers [[measurement|measured]] in laboratory [[experiments]] necessarily have only finitely many digits of precision.

Diverse conclusions have been drawn from this. One which seems useful and well-informed by the theory of [[computability]] in [[mathematics]] is the following (further quoting from [Szudzik 10, section 2](#Szudzik10))

> So, we suffer no loss of generality by restricting the values of all observable quantities to be expressed as [[natural numbers|non-negative integers]] &#8212; the restriction only forces us to make the methods of error analysis, which were tacitly assumed when dealing with real numbers, an explicit part of each model.

In type-I [[computability]] the [[computable functions]] are [[partial recursive functions]] and in view of this some authors concluded (e.g. [Kreisel 74](#Kreisel74)) (and we still quote [Szudzik 10, section 2](#Szudzik10) for this):

> To show that a [[model (physics)|model]] $[$ of physics $]$ is [[computable function|computable]], the model must somehow be expressed using [[partial recursive function|recursive functions]].

A similar sentiment is voiced by [Geroch and Hartle](#GerochHartle):
> We propose, in parallel with the notion of a computable number in mathematics, that of a measurable number in a physical theory. The question of whether there exists an algorithm for implementing a theory may then be formulated more precisely as the question of whether the measurable numbers of the theory are computable. We argue that the measurable numbers are in fact computable in the familiar theories of physics, but there is no reason why this need be the case in order that a theory have predictive power. Indeed, in some recent formulations of quantum gravity as a sum ver histories, there are candidates for numbers that are measurable but not computable.

However, in [[computability theory]] there is also the concept of _[[computable function (analysis)|type-II computable functions]]_ used in the field of "[[constructive analysis]]", "[[computable analysis]]". This is based on the idea that for instance for specifying [[computable real numbers]] as used in [[physics]], an [[algorithm]] may work not just on single [[natural numbers]], but indefinitely on sequences of them, producing output that is in each step a finite, but in each next step a more accurate approximation. 

[[!include computable mathematics -- table]]

This concept of [[computable analysis|type-II computability]] is arguably closer to actual practice in [[physics]].

Of course there is a wide-spread (but of course controversial) vague speculation (often justified by alluding to expected implications of [[quantum gravity]] on the true microscopic nature of [[spacetime]] and sometimes formalized in terms of cellular automata, e.g. [Zuse 67](#Zuse67)) that in some sense the [[observable universe]] is fundamentally "[[finite object|finite]]", so that in the end [[computability]] is a non-issue in [[physics]] as one is really operating on a large but [[finite set]] of states.

However, since fundamental physics is [[quantum physics]] and since [[quantum mechanics]] with its [[wave functions]], [[Hilbert spaces]] and [[probability amplitudes]] invokes ([[functional analysis|functional]]) [[analysis]] and hence "non-finite mathematics" even when describing the minimum of a [[physical system]] with only two possible configurations (a "[[qbit]]") a strict [[finitism]] perspective on fundamental [[physics]] runs into problems (highlighted for instance in ([Feynman 81, slide 15](#Feynman81))). Precisely this kind of issue is the topic of _[[computable analysis]]_ ("[[constructive analysis]]", "[[exact analysis]]") with its type-II notion of [[computable functions]], which would therefore seem to be the right mathematical context discussing [[computability]] in fundamental (namely quantum) [[physics]]. This point is made in ([Weihrauch-Zhong 02](#WeihrauchZhong02)) for the [[wave equation]]. 

This matters: there are solutions to the [[wave equation]] with type-I computable initial values which are not themselves type-I computable ([Pour-El et al. 83](#PourEl83)). If type-I computability were the right concept of computabuility in physics, this result would show a violation of the [[Church-Turing thesis]]. But in ([Weihrauch-Zhong 02](#WeihrauchZhong02)) it is argued that the correct concept to use is indeed type-II computability and it is shown ([Weihrauch-Zhong 02, theorem 3.2](#WeihrauchZhong02)) that the solution operator to the wave equation is indeed type-II computable. The same is shown for the [[Schrödinger equation]] of [[quantum mechanics]] in ([Weihrauch-Zhong 01](#WeihrauchZhong01), [Weihrauch-Zhong 06](#WeihrauchZhong06)) where it is found that the Schr&#246;dinger operator is computable on the [[Lebesgue space]] $L^p$ precisely for the physically relevant value $p = 2$.

In the vein of type-II computability the issue specifically of computable [[quantum physics]]/[[quantum logic]] has only been further considered in ([Streicher 12](#Streicher12)), where it is shown that at least a fair bit of the [[Hilbert space]] technology of [[quantum mechanics]]/[[quantum logic]] sits inside the [[function realizability topos]] $RT(\mathcal{K}_2)$.

The question whether the [[observable universe]] or at least all [[experiments]] done within are computable is part of the (strong) [[physical Church-Turing thesis]]. See there for more, and see ([Waaldijk 03](#Waaldijk03)). Experiments showing non-computability in quantum processes have been claimed in ([CDDS 10](#CDDS10)).


## Related concepts

* [[interpretation of quantum mechanics]]

* [[measurement problem]]

* [[quantum logic]], [[quantum computation]]

* [[coordination]]

* [[p-adic physics]]

* [[hypercomputation]]

* [[constructive mathematics]], [[geometry of physics]]

## References

Decent discussion of computability in physics includes the following

* Robert Rosen, _Church's thesis and its relation to the concept of realizability in biology and physics_, Bulletin of Mathematical Biophysics 24 (1962), 375&#8211;393.

* {#Zuse67} [[Konrad Zuse]], _Rechnender Raum_, Elektronische Datenverarbeitung 8 (1967), 336&#8211;344.

* {#Kreisel74} [[Georg Kreisel]], _A notion of mechanistic theory_, Synthese 29 (1974), 11&#8211;26.

* {#Feynman81} [[Richard Feynman]], _Simulating physics with computers_, talk at _1st conference on Physics and Computation_ MIT (1981),  (talk notes by P. Birnbaum, E. Tromer: [pdf](http://www.wisdom.weizmann.ac.il/~naor/COURSE/feynman-simulating.pdf))

* {#PourEl83} Marian Boykan Pour-El, J. Ian Richards, _Computability and noncomputability in classical analysis', Trans. Amer. Math. Soc. 275 (1983) 539-560.

  Marian Pour-El, Ning Zhong, _The wave equation with computable initial data whose unique solution is nowhere computable_, Math. Logic Quart. 43 (1997) no. 4, 499-509.

* {#Bridges95} [[Douglas Bridges]], _Constructive mathematics and unbounded operators -- a reply to Hellman_, J. Philosophical Logic 24, 549&#8211;561 (1995)

* {#WeihrauchZhong01} [[Klaus Weihrauch]],  Ning Zhong, _Is the linear Schr&#246;dinger Propagator Turing Computable?_ , in Jens Blanck et al (eds.) _Computability and Complexity in Analysis: 4th International Workshop_ , CCA, Springer 2001

* {#WeihrauchZhong02} [[Klaus Weihrauch]],  Ning Zhong, _Is wave propagation computable or can wave computers beat the Turing machine?_, Proc. of the London Math. Soc. (3) 85 (2002) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.95.5994))

* {#Waaldijk03} [[Frank Waaldijk]], section 7 of _On the foundations of constructive mathematics -- especially in relation to the theory of continuous functions_, 2003  ([pdf](http://www.fwaaldijk.nl/foundations%20of%20constructive%20mathematics.pdf), [web discussion](http://fwaaldijk.wordpress.com/2014/01/14/experiment-to-disprove-strong-physical-church-turing-thesis/)).

* {#WeihrauchZhong06} [[Klaus Weihrauch]], _Computing Schr&#246;dinger propagators on Type-2 Turing machines_, Journal of Complexity
Volume 22, Issue 6, December 2006, Pages 918&#8211;935

* {#Szudzik10} [[Matthew Szudzik]], _The Computable Universe Hypothesis_, in  [[Hector Zenil]] (ed.) _[A Computable Universe: Understanding and Exploring Nature as Computation](http://www.worldscientific.com/worldscibooks/10.1142/8306)_ , World Scientific, 2012, pp. 479-523 ([arXiv:1003.5831](http://arxiv.org/abs/1003.5831))

* {#CDDS10} Cristian Calude, Michael Dinneen, Monica Dumitrescu, Karl Svozil, _Experimental Evidence of Quantum Randomness Incomputability_, Phys. Rev. A 82, 022102 (2010) ([arxiv:1004.1521](http://arxiv.org/abs/1004.1521), [web announcement](http://www.technologyreview.com/view/418445/first-evidence-that-quantum-processes-generate-truly-random-numbers/))

* {#Streicher12} [[Thomas Streicher]], _Computability Theory for Quantum Theory_, talk at Logic Seminar Univ. Utrecht in July 2012 ([pdf](http://www.mathematik.tu-darmstadt.de/~streicher/TALKS/qtdm.pdf))

* Stanford Encyclopedia of Philosophy, _[Computation in physics](http://plato.stanford.edu/entries/computation-physicalsystems/)_

Some general remarks on the impact of [[realizability]] ([[intuitionistic mathematics|intuitionistic]]/[[constructive mathematics]]) on computability in physics and the [[Church-Turing thesis]] are in 

* [[Andrej Bauer]],  section 4 of _Intuitionistic Mathematics and Realizability in the Physical World_, in  [[Hector Zenil]] (ed.) _[A Computable Universe: Understanding and Exploring Nature as Computation](http://www.worldscientific.com/worldscibooks/10.1142/8306)_, World Scientific 2012 ([web](http://math.andrej.com/2014/03/04/intuitionistic-mathematics-and-realizability-in-the-physical-world/), [pdf](http://math.andrej.com/wp-content/uploads/2014/03/real-world-realizability.pdf))

A useful set of lecture notes on the mathematical background of [[computability]] and [[realizability]] is in

* {#Bauer05} [[Andrej Bauer]], _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, , vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))

* {#GerochHartle} Robert Geroch, James Hartle, _Computability and physical theories_, Foundations of Physics June 1986, Volume 16, Issue 6, pp 533-550 ([doi](http://dx.doi.org/10.1007/BF01886519), [PDF](http://link.springer.com/content/pdf/10.1007/BF01886519.pdf))


[[!redirects computable quantum physics]]

[[!redirects computability in physics]]
