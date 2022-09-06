
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What has been called quantum "teleportation" ([BBCJPW 1993](#BBCJPW93)) is a procedure (a "protocol") in [[quantum information theory]] by which the exact transmission of a [[quantum state]] (such as that of some [[qbits]]) is equivalently established by the transmission of [[classical physics|classical]] information, *provided* that sender and receiver "share a [[Bell state]]", hence each have access to one half of a pair of [[subsystems]] which are in a maximally [[entanglement|entangled]] [[quantum state]] with each other. The protocol involves a [[quantum measurement]] and its ensuing [[wavefunction collapse]] destroys ("uses up") this entangled state in order to transmit the remaining quantum state -- which somewhat relativizes the imagery of "teleportation".

While this prose -- and certainly the imagery of "teleportation" -- may appear somewhat exotic, the actual mathematics underlying the "quantum teleportation protocol" is a short and elementary consequence of the most basic [[axioms]] of [[quantum mechanics]] (in fact it is all but a self-evident consequence when formulated in modern notation, see [below](#HistoryAndPerspective)). What makes quantum teleportation interesting is the ([[quantum information theory|quantum]]) [[information theory|information theoretic]] perspective on it.


## History and perspective
 {#HistoryAndPerspective}

Given that the basic axioms of quantum physics were established in the 1920s and widely appreciated by the 1930s, while the possibility of "quantum teleportation" was observed only [in 1993](#BBCJPW93), using neither tools nor notation not available to the founding fathers, one may naturally wonder (e.g [Coecke 2010, p. 1](#Coecke10)):

> why did it take us 60 years to discover the conceptually
intriguing and easily derivable physical phenomenon of 'quantum teleportation'?

Traditional reviews of the matter maintain that the phenomenon just happens to be intrinsically tricky to see through -- e.g. [Aaronson 2018](#Aaronson18), [p. 71](https://www.scottaaronson.com/qclec.pdf#page=71), apparently in reply to his student's puzzlement "How do people come up with this stuff?", asserts that:

> These sorts of protocols can be hard to find. 

On the other hand, it was observed around [Coecke 2004](#Coecke04), [Abramsky & Coecke 2004](#AbramskyCoecke04), and pronouncedly brought out in [Coecke 2005](#Coecke05), [2010](#Coecke10) that the logical structure of [[quantum information theory]] in general and that of quantum teleportation in particular is transparently captured by [[string diagram]]-calculus for the ambient [[compact closed category|compact closed]] [[tensor category]] of [[finite dimensional vector space|finite dimensional]] [[Hilbert spaces]] (see *[[finite quantum mechanics in terms of dagger-compact categories]]*): 

In this [[category theory|category=theoretic]] language, the quantum teleportation protocol is essentially just the [[zig-zag identity]] for [[dualizable objects]] (here: [[finite dimensional vector space|finite-dimensional]] [[Hilbert spaces]]) in any [[monoidal category]].

This suggests the following alternative answer, from [Coecke 2005, p. 1](#Coecke05):

> Why did discovering quantum teleportation take 60 year? We claim that this is due to a ‘bad quantum formalism’ (bad $\neq$ wrong) and this badness is in particular due to the fact that the formalism is ‘too low level'.
 
(Here "bad quantum formalism" refers to the traditional notation as in [BBCJPW93](#BBCJPW93), while the suggested high-level improvement is [[string diagram]]-calculus for the ambient [[tensor category]] of finite-dimensional Hilbert spaces.)

## Statement

(...)


## Related concepts

* [[quantum entanglement]]

* [[no-cloning theorem]]

* [[quantum information theory]]

## References

Original article:

* {#BBCJPW93} Charles H. Bennett, Gilles Brassard, Claude Crépeau, Richard Jozsa, Asher Peres, and William K. Wootters, *Teleporting an unknown quantum state via dual classical and Einstein-Podolsky-Rosen channels*, Phys. Rev. Lett. **70** 1895 (1993) &lbrack;[doi:10.1103/PhysRevLett.70.1895](https://doi.org/10.1103/PhysRevLett.70.1895)&rbrack;

Traditional review:

* {#Aaronson18} [[Scott Aaronson]], §10.1 in *Introduction to Quantum Information Science* (2018) &lbrack;[pdf](https://www.scottaaronson.com/qclec.pdf), [webpage](https://www.scottaaronson.com/cs378/)&rbrack;

Discussion via [[string diagram]]-calculus ([[finite quantum mechanics in terms of dagger-compact categories]]):

* {#Coecke04} [[Bob Coecke]], §4 of: *The logic of entanglement*, in: *Horizons of the Mind. A Tribute to Prakash Panangaden*, Lecture Notes in Computer Science **8464** (2014)  &lbrack;[arXiv:quant-ph/0402014](https://arxiv.org/abs/quant-ph/0402014), [doi:10.1007/978-3-319-06880-0_13](https://doi.org/10.1007/978-3-319-06880-0_13)&rbrack;

* {#AbramskyCoecke04} [[Samson Abramsky]], [[Bob Coecke]], §2 in: *A categorical semantics of quantum protocols*, Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) &lbrack;[arXiv:quant-ph/0402130](https://arxiv.org/abs/quant-ph/0402130), [doi:10.1109/LICS.2004.1319636](https://doi.org/10.1109/LICS.2004.1319636)&rbrack;

* {#Coecke05} [[Bob Coecke]], §3c in: *Kindergarten Quantum Mechanics*, in *Quantum Theory: Reconsideration of Foundations* (QTRF 3) Vaxjo, Sweden, June 6-11, 2005, AIP Conf. Proc. **810** (2006) &lbrack;[arXiv:quant-ph/0510032](https://arxiv.org/abs/quant-ph/0510032), [doi:10.1063/1.2158713](https://doi.org/10.1063/1.2158713)&rbrack;

* {#Coecke10} [[Bob Coecke]], *Quantum Picturalism*, Contemporary Physics **51** (2010) 59-83 &lbrack;[arXiv:0908.1787](https://arxiv.org/abs/0908.1787), [doi:10.1080/00107510903257624](https://doi.org/10.1080/00107510903257624)&rbrack;

See also: 

* Wikipedia, *[Quantum teleportation](https://en.wikipedia.org/wiki/Quantum_teleportation)*



