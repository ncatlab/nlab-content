
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

What has been called quantum "teleportation" ([BBCJPW 1993](#BBCJPW93)) is a procedure (a "protocol") in [[quantum information theory]] by which the exact transmission of a [[quantum state]] (such as that of some [[qbits]]) is equivalently established by the transmission of [[classical physics|classical]] information, *provided* that sender and receiver "share a [[Bell state]]", hence that each have access to one half of a pair of [[subsystems]] which are in a maximally [[entanglement|entangled]] [[quantum state]] with each other. The protocol involves a [[quantum measurement]] and its ensuing [[wavefunction collapse]] destroys ("uses up") this entangled state in order to transmit the remaining quantum state -- which somewhat relativizes the imagery of "teleportation".

While this prose may appear somewhat exotic, the actual mathematics underlying the "quantum teleportation protocol" is an elementary and direct consequence of the most basic [[axioms]] of [[quantum mechanics]] (in fact it is all but a self-evident consequence when formulated in modern notation, see [below](#HistoryAndPerspective)). What makes quantum teleportation interesting is the ([[quantum information theory|quantum]]) [[information theory|information theoretic]] perspective on it.


## History and perspective
 {#HistoryAndPerspective}

Given that the basic axioms of quantum physics were established in the 1920s and widely appreciated by the 1930s, while the possibility of "quantum teleportation" was observed only [in 1993](#BBCJPW93), using neither tools nor notation not available to the founding fathers, one may naturally wonder (e.g [Coecke 2010, p. 1](#Coecke10)):

> why did it take us 60 years to discover the conceptually
intriguing and easily derivable physical phenomenon of 'quantum teleportation'?

Traditional reviews of the matter maintain that the phenomenon just happens to be intrinsically tricky to see through -- e.g. [Aaronson 2018](#Aaronson18), [p. 71](https://www.scottaaronson.com/qclec.pdf#page=71), apparently in reply to his student's puzzlement "How do people come up with this stuff?", asserts that:

> These sorts of protocols can be hard to find. 

On the other hand, it was observed around [Coecke 2004](#Coecke04), [Abramsky & Coecke 2004](#AbramskyCoecke04) -- and pronouncedly brought out in [Coecke 2005](#Coecke05), [2010](#Coecke10) -- that the logical structure of [[quantum information theory]] in general and that of quantum teleportation in particular is transparently captured by [[string diagram]]-calculus for the ambient [[compact closed category|compact closed]] [[tensor category]] of [[finite dimensional vector space|finite dimensional]] [[Hilbert spaces]] (see *[[finite quantum mechanics in terms of dagger-compact categories]]*): 

In this [[category theory|category-theoretic]] language, the quantum teleportation protocol is essentially just the [[zig-zag identity]] for [[dualizable objects]] (here: [[finite dimensional vector space|finite-dimensional]] [[Hilbert spaces]]) in any [[monoidal category]], see [below](#StatementInStringDiagramLanguage).

This suggests the following alternative answer, from [Coecke 2005, p. 1](#Coecke05):

> Why did discovering quantum teleportation take 60 year? 

> We claim that this is due to a ‘bad quantum formalism’ (bad $\neq$ wrong) and this badness is in particular due to the fact that the formalism is ‘too low level'.
 
Here "bad quantum formalism" refers to the traditional notation as in the original [BBCJPW93](#BBCJPW93) and in traditional reviews (e.g. [Aaronson 2018](#Aaronson18), see also [Coecke 05](#Coecke05) [ftn. 5 on p. 8](https://arxiv.org/pdf/quant-ph/0510032.pdf#page=8)), while the suggested high-level improvement is [[string diagram]]-calculus for the ambient [[tensor category]] of finite-dimensional Hilbert spaces, further discussed at *[[finite quantum mechanics in terms of dagger-compact categories]]*.


## Statement
 {#Statement}


{#StatementInStringDiagramLanguage}The quantum teleportation protocol is neatly expressed in [[string diagram]]-calculus as follows (essentially following [Coecke 2005](#Coecke05)):


<img src="https://ncatlab.org/nlab/files/QuantumTeleportationProtocol-220906b.jpg" width="850"> 

Here, by the general laws of [[string diagrams]]: a solid line pointing to the right represents a given [[finite dimensional vector space|finite dimensional]] [[Hilbert space]] $\mathscr{H} \,\simeq\, \mathbb{C}^D$ (of [[dimension of a vector space|dimension]] $D$), the same line pointing backwards denotes its [[dual vector space]], two lines running parallel reflects the [[tensor product of Hilbert spaces|tensor product]] of the corresponding Hilbert spaces, and the curve "$\supset$" denotes [[evaluation]] $\mathscr{H}^\ast \otimes \mathscr{H} \xrightarrow{ev} \mathbb{C}$.

That this [[string diagram]] (represents a [[linear map]] which) takes the [[quantum state]] $\Psi$ from "Agent A" ("Alice") to the same state $\Psi$ for "Agent B" ("Bob"), as shown is *immediate* from the [[zig-zag identity]], hence from the fact that the curved line may be "yanked straight" to an [[identity]] line, without changing the operational value of the diagram. This is the transparent [[proof]] of the quantum teleporation protocol. 

Notice that this is a [[rigorous proof]], and yet this [[string diagram]] is close to informal flow-charts traditionally used to illustrate the idea of quantum teleportation (e.g [Bouwmeester, Ekert & Zeilinger 2020, Fig. 3.1](#BouwmeesterEkertZeilinger20)).

In more detail, here the top box shows the [[projector]] onto a [[Bell state]] with one variable transformed by a [[unitary operator]] $\sigma$. This reflects the (random/unpredictable!) result of a [[quantum measurement]] in a corresponding  [[linear basis]] for $\mathscr{H} \otimes \mathscr{H}^\ast$ (according to the [[wavefunction collapse|collapse postulate]]). 

Concretely, if the [[Hilbert space]] represented by a single solid line is that of a single [[qbit]], i.e. if $\mathscr{H} = \mathbb{C}^2$ ($D = 2$), then  $\sigma$ may be taken to range over the [[unitary operator|unitary]] [[Pauli matrices]]: 
$$
  \sigma_0 
  \coloneqq 
  \left(
    \begin{array}{cc}
      1 & 0
      \\
      0 & 1
    \end{array}
  \right)
   ,\;\;\;\;
  \sigma_1 
  \coloneqq 
  \left(
    \begin{array}{cc}
      0 & 1
      \\
      1 & 0
    \end{array}
  \right)
   ,\;\;\;\;
  \sigma_2 
  \coloneqq 
  \left(
    \begin{array}{cc}
      0 & -\mathrm{i}
      \\
      \mathrm{i} & 0
    \end{array}
  \right)
   ,\;\;\;\;
  \sigma_3 
  \coloneqq 
  \left(
    \begin{array}{cc}
      1 & 0
      \\
      0 & -1
    \end{array}
  \right)
  \,.
$$

In this case, the component-evaluation of the above diagram yields the quantum teleportation protocol in its traditional form ([BBCJPW93](#BBCJPW93)).

\linebreak

The concrete implementation of the above protocol on given quantum hardware will look more complicated. 

{#AsABraidGateCircuit} For instance, the implementation of the quantum teleportation protocol as a circuit of [[braid representation|braid]] gates of [[Ising anyons]] ([[topological quantum computation]]) is given in [Xu & Zhou 2022](#XuZhou22):

<img src="https://ncatlab.org/nlab/files/BraidCircuitQuantumTeleProtocol-220915.jpg" width="450">



\linebreak

## Related concepts

* [[quantum entanglement]]

* [[no-cloning theorem]]

* [[quantum information theory]]

## References

The original article:

* {#BBCJPW93} [[Charles H. Bennett]], [[Gilles Brassard]], [[Claude Crépeau]], [[Richard Jozsa]], [[Asher Peres]], [[William K. Wootters]]: *Teleporting an unknown quantum state via dual classical and Einstein-Podolsky-Rosen channels*, Phys. Rev. Lett. **70** 1895 (1993) &lbrack;[doi:10.1103/PhysRevLett.70.1895](https://doi.org/10.1103/PhysRevLett.70.1895)&rbrack;

Traditional review:

* {#Aaronson18} [[Scott Aaronson]], §10.1 in *Introduction to Quantum Information Science* (2018) &lbrack;[pdf](https://www.scottaaronson.com/qclec.pdf), [webpage](https://www.scottaaronson.com/cs378/)&rbrack;

and phrased in the [[quantum programming language]] [[Quipper]]:


* [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], p. 5 of: 
_An Introduction to Quantum Programming in Quipper_, Lecture Notes in Computer Science 7948:110-124, Springer, 2013 ([arXiv:1304.5485](https://arxiv.org/abs/1304.5485))

and with focus on the [[experiment|experimental]] realization:

* {#BouwmeesterEkertZeilinger20} [[Dirk Bouwmeester]], [[Artur Ekert]], [[Anton Zeilinger]] (eds.), §3.3 of: *The Physics of Quantum Information -- Quantum Cryptography, Quantum Teleportation, Quantum Computation*, Springer (2020) &lbrack;[doi:10.1007/978-3-662-04209-0](https://doi.org/10.1007/978-3-662-04209-0)&rbrack;

See also: 

* Wikipedia, *[Quantum teleportation](https://en.wikipedia.org/wiki/Quantum_teleportation)*

Discussion via [[string diagram]]-calculus ([[finite quantum mechanics in terms of dagger-compact categories]]):

* {#Coecke04} [[Bob Coecke]], §4 of: *The logic of entanglement*, in: *Horizons of the Mind. A Tribute to Prakash Panangaden*, Lecture Notes in Computer Science **8464** (2014)  &lbrack;[arXiv:quant-ph/0402014](https://arxiv.org/abs/quant-ph/0402014), [doi:10.1007/978-3-319-06880-0_13](https://doi.org/10.1007/978-3-319-06880-0_13)&rbrack;

* {#AbramskyCoecke04} [[Samson Abramsky]], [[Bob Coecke]], §2 in: *A categorical semantics of quantum protocols*, Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) &lbrack;[arXiv:quant-ph/0402130](https://arxiv.org/abs/quant-ph/0402130), [doi:10.1109/LICS.2004.1319636](https://doi.org/10.1109/LICS.2004.1319636)&rbrack;

* {#Coecke05} [[Bob Coecke]], §3c in: *Kindergarten Quantum Mechanics*, in *Quantum Theory: Reconsideration of Foundations* (QTRF 3) Vaxjo, Sweden, June 6-11, 2005, AIP Conf. Proc. **810** (2006) &lbrack;[arXiv:quant-ph/0510032](https://arxiv.org/abs/quant-ph/0510032), [doi:10.1063/1.2158713](https://doi.org/10.1063/1.2158713)&rbrack;

* {#Coecke10} [[Bob Coecke]], *Quantum Picturalism*, Contemporary Physics **51** (2010) 59-83 &lbrack;[arXiv:0908.1787](https://arxiv.org/abs/0908.1787), [doi:10.1080/00107510903257624](https://doi.org/10.1080/00107510903257624)&rbrack;

Realization in [[experiment]]:

* [[Dirk Bouwmeester]], Jian-Wei Pan, Klaus Mattle, Manfred Eibl, Harald Weinfurter, [[Anton Zeilinger]], *Experimental quantum teleportation*, Nature **390** 575–579 (1997) &lbrack;[doi:10.1038/37539](https://doi.org/10.1038/37539)&rbrack;

* Dario Lago-Rivera, Jelena V. Rakonjac, Samuele Grandi, Hugues de Riedmatten, *Long-distance multiplexed quantum teleportation from a telecom photon to a solid-state qubit* &lbrack;[arXiv:2209.06249](https://arxiv.org/abs/2209.06249)&rbrack;


Implementation of the quantum teleportation protocol in [[topological quantum computation]] via [[braiding]] of [[Ising anyons]]:

* {#XuZhou22} Cheng-Qian Xu, D. L. Zhou, *Quantum teleportation using Ising anyons*, Phys. Rev. A **106** 012413 (2022) &lbrack;[arXiv:2201.11923](https://arxiv.org/abs/2201.11923), [doi:10.1103/PhysRevA.106.012413](https://doi.org/10.1103/PhysRevA.106.012413)&rbrack;



Implementation in [[quantum programming languages]]:

* *[Qiskit: Quantum Teleportation](https://qiskit.org/textbook/ch-algorithms/teleportation.html)*



