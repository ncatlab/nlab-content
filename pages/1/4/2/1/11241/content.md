
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

The _Church-Turing thesis_ is a (mostly informal) statement about the nature of [[computability]]. It roughly asserts that there is, up to equivalence, only one single universal concept of computability.

Slightly more in detail, the (physical) _Church-Turing thesis_ says vaguely that what is [[computation|computable]] in the mathematical sense of [[computation]] is precisely what is "effectively" computable ([[computable physics|physically computable]]).

In interpreting this one has to be careful which concept of [[computation]] is used, there are two different main types:

[[!include computable mathematics -- table]]

Indeed, there are physical processes (described by the [[wave equation]]) which are not type-I computable ([Pour-El et al. 83](#PourEl83)), but they are type-II computable ([Weihrauch-Zhong 01](WeihrauchZhong01), [Weihrauch-Zhong 02](#WeihrauchZhong02), [Weihrauch-Zhong 06](#WeihrauchZhong06)). For more on this see at _[[computable physics]]_.

One then distinguishes:

* The **physical Church-Turing thesis**: What is [[computable physics|physically computable]] is also computable in the mathematical sense of [[computability]].

* The **strong physical Church-Turing thesis**: _Every [[real number]] found by [[experiment]] in the [[observable universe]] is a [[computable real number]]_. 

  This strong version is often phrased as "the universe is a computer" or as "[digitial physics](https://en.wikipedia.org/wiki/Digital_physics)".

On the strong physical Church-Turing thesis see _[SEP -- Computation in Physical Systems -- Is every Physical system computational?](http://plato.stanford.edu/entries/computation-physicalsystems/#EvePhySysCom)_ for a general account and ([Waaldijk 03](#Waaldijk03)) for a more formal account emphasizing the role of [[intuitionistic mathematics|intuitionistic]]/[[constructive mathematics]].

More concretely, the kind of experiment proposed there to test whether non-computable sequences of events may appear in [[experiment]] has been claimed to have been carried out with [[quantum physics|quantum process]] in ([CDDS 10](#CDDS10)).


## Related concepts

* [[computability]]

* [[computable physics]]

## References

General reviews include

* Wikipedia, _[Church-Turing thesis](http://en.wikipedia.org/wiki/Church&#8211;Turing_thesis)_, _[Digital physics](https://en.wikipedia.org/wiki/Digital_physics)_

* Stanford Encyclopedia of Philosophy, _[The Church-Turing Thesis](http://plato.stanford.edu/entries/church-turing/)_, _[Computation in Physical Systems](http://plato.stanford.edu/entries/computation-physicalsystems/#EvePhySysCom)_

A discussion well-informed by theoretical [[computability]], [[realizability]] and [[intuitionistic mathematics|intuitionistic]](/[[constructive mathematics]] is in 


* {#Waaldijk03} [[Frank Waaldijk]], section 7 of _On the foundations of constructive mathematics -- especially in relation to the theory of continuous functions_, 2003  ([pdf](http://www.fwaaldijk.nl/foundations%20of%20constructive%20mathematics.pdf), [web discussion](http://fwaaldijk.wordpress.com/2014/01/14/experiment-to-disprove-strong-physical-church-turing-thesis/)).


Discussion of physical processes which are not type-I computable by [[partial recursive functions]] are found in
 
* {#PourEl83} Marian Boykan Pour-El, J. Ian Richards, _Computability and noncomputability in classical analysis, Trans. Amer. Math. Soc. 275 (1983) 539-560.

  Marian Pour-El, Ning Zhong, _The wave equation with computable initial data whose unique solution is nowhere computable_, Math. Logic Quart. 43 (1997) no. 4, 499-509.

Proof that these physics processes ([[wave equation]], [[Schrödinger equation]]) are however [[Type Two Theory of Effectivity|type-II computable]] is in 

* {#WeihrauchZhong01} [[Klaus Weihrauch]],  Ning Zhong, _Is the linear Schr&#246;dinger Propagator Turing Computable?_, in Jens Blanck et al (eds.) _Computability and Complexity in Analysis: 4th International Workshop, CCA_, Springer 2001

* {#WeihrauchZhong02} [[Klaus Weihrauch]],  Ning Zhong, _Is wave propagation computable or can wave computers beat the Turing machine?_, Proc. of the London Math. Soc. (3) 85 (2002) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.95.5994))

* {#WeihrauchZhong06} [[Klaus Weihrauch]], _Computing Schr&#246;dinger propagators on Type-2 Turing machines_, Journal of Complexity
Volume 22, Issue 6, December 2006, Pages 918&#8211;935

Discussion of (non-)computability of quantum processes is in 

* {#CDDS10} Cristian Calude, Michael Dinneen, Monica Dumitrescu, Karl Svozil, _Experimental Evidence of Quantum Randomness Incomputability_, Phys. Rev. A 82, 022102 (2010) ([arxiv:1004.1521](http://arxiv.org/abs/1004.1521), [web announcement](http://www.technologyreview.com/view/418445/first-evidence-that-quantum-processes-generate-truly-random-numbers/))

[[!redirects physical Church-Turing thesis]]
[[!redirects strong physical Church-Turing thesis]]