
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
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
 {#Idea}

The symbols *ER = EPR* (pronounced: "ee arr is ee pee arr") serve as a slogan for a hypothesis about [[quantum gravity]], claiming, somewhat vaguely, that [[entangled particles]] (the [[EPR paradox|Einstein-Podolsky-Rosen phenomenon]]: "EPR") "are" connected by a [[wormhole]] ([[Einstein-Rosen bridge]]: "ER"). 

This slogan is due to [Maldacena & Susskind (2013)](#MaldacenaSusskind13) (there motivated from a search for a solution for the perceived [[black hole firewall problem]]) but the idea may in this form have circulated earlier &lbrack;cf. [Verlinde & Verlinde (2022)](#VerlindeVerlinde22)&rbrack;. In fact, what is arguably a precise and provable version of the statement (in lattice models) has appeared years earlier: the [[Ryu-Takayanagi formula]], see [below](#AsASloganForTheRyuTakayanagiFormula) (which, however, applies in a [[holographic principle|holographic]] context, a qualification not necessarily brought out by [Maldacena & Susskind](#MaldacenaSusskind13)).

At face value the statement "ER = EPR", even if parsed benevolently, suffers from a [[type checking|typing error]] between [[quantum physics]] and [[classical field theory|classical]] [[gravity]]. However, [like with a Zen koan](https://twitter.com/schreiberurs/status/1134503200550203392?lang=en), one may imagine the [[paradox|paradoxical]] formulation to propel the intuitive grasp of indeed rather deep principles of [[holographic principle|holography]] and particularly of [[holographic entanglement entropy]], such as expressed with precision by the [Ryu-Takayanagi formula](#AsASloganForTheRyuTakayanagiFormula).

Another source of fun with the slogan "ER = EPR" is to thereby see the two classical and seminal papers by [[Albert Einstein]] et al. from 1935 &lbrack;[Einstein & Rosen (1935)](wormhole#EinsteinRosen35), [Einstein, Podoldsky & Rosen (1935)](EPR+paradox#EinsteinPodoldskyRosen35)&rbrack; --- which to [[Einstein]] must have seemed unrelated --- to secretly be about two sides of the same medal.



## As a slogan for the Ryu-Takayanagi formula
 {#AsASloganForTheRyuTakayanagiFormula}

The idea meant to be expressed by the slogan "ER = EPR" may usefully be compared to -- and may be a way of turning into prose -- the *[[Ryu-Takayanagi formula]]* &lbrack;[Ryu & Takayanagi (2006)](#RyuTakayanagi06a)&rbrack; (which has a more well-defined content as a *[[theorem]]* in a class of discrete [[tensor network]]-models). The RT-formula equates:

* **(quantum entanglement:)** the [[entanglement entropy]] of a [[boundary field theory|boundary]] [[quantum field theory]] in a subspace of an [[asymptotic boundary]] 

with 

* **(global spacetime structure:)** the [[minimal surface|minimal area]] of a [[coboundary|cobounding]] [[hypersurface]] in an ambient [[curvature|curved]] [[bulk]] [[spacetime]].

Concretely, in [[tensor network]]-models of [[AdS2/CFT1 duality]], the [[entanglement entropy]] $S_A$ of any [[Majorana dimer code]]-[[tensor network]] [[quantum state|state]] turns out to count the number of [[dimers]] that cross between a ([[connected topological space|connected]]) subregion $A$ and its [[complement]]:

\begin{imagefromfile}
    "file_name": "ChordDiagramEntanglementEntropy.jpg",
    "width": 460,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [JGPE 19](holographic+entanglement+entropy#JGPE19)"
\end{imagefromfile}


\begin{imagefromfile}
    "file_name": "HanUniversalHolographicCode.jpg",
    "float": "right",
    "width": 380,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Yan 20](holographic+entanglement+entropy#Yan20)"
\end{imagefromfile}


In the case that the [[dimers]] correspond to the [[hyperbolic tesselation]] $\{5,4\}$ from the [[HaPPY code]], this entropy formula 

$$
  S_A
  \;=\;
  \tfrac{1}{2}
  \ln
  \big(
    2^{ \left\vert Chords(A, \bar A) \right\vert }
  \big)
$$

recovers the [[Ryu-Takayanagi formula]] ([JGPE 19 (78)](holographic+entanglement+entropy#JGPE19)), as here the number of chords crossing any hyperbolic [[geodesic]] grows linearly with the [[length]] of this geodesic. 

A precursor to this picture is the "bit-thread"-interpretation of entanglement entropy due to [Freedman & Headrick 16](holographic+entanglement+entropy#FreedmanHeadrick16) (notice the use of "EPR pair" in their [Figure 4](https://arxiv.org/pdf/1604.00354.pdf#page=4).)

\begin{imagefromfile}
    "file_name": "ChordDiagram.jpg",
    "float": "right",
    "width": 230,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [Sati & Schreiber 19c](#SatiSchreiber19c)"
\end{imagefromfile}


Following [Sati-Schreiber 19c](#SatiSchreiber19c) we recognize the above [[Majorana dimer]]/bit-thread networks from [JGPE 19](#JGPE19), [Yan 19](#Yan19) as *[[chord diagram]]*-encodings of holographic bulks ([p. 38](https://arxiv.org/pdf/1912.10425v3.pdf#page=38)).

Notice that the formula for the [[entanglement entropy]] in the [[Majorana dimer code]]  holds generally, for *any* configuration and hence any underlying [[chord diagram]].

In conclusion, note how each [[chord]] here reflects at the same time:

1. (ER) one [[entanglement|entangled pair]] of [[qbits]] in the [[boundary field theory|boundary]] [[quantum system]];

1. (EPR) a [[geodesic]] through the [[hyperbolic plane]] [[bulk]] spacetime,

which is a (rigorous) state of affairs clearly reminiscent of the "ER = EPR" slogan (except that wormholes are replaced by minimal area hypersurfaces, here: geodesics).

For more on this see at *[[holographic entanglement entropy]]*.


## Related entries

* [[entanglement]], [[EPR paradox]]

* [[wormhole]]

* [[holographic entanglement entropy]]

* [[quantum teleportation]]

* [[black hole firewall problem]]


## References

The original result of the [[Ryu-Takayanagi formula]]:

* {#RyuTakayanagi06a} [[Shinsei Ryu]], [[Tadashi Takayanagi]], *Holographic Derivation of Entanglement Entropy from AdS/CFT*, Phys. Rev. Lett. **96** 181602 (2006) &lbrack;[arXiv:hep-th/0603001](https://arxiv.org/abs/hep-th/0603001), [doi:10.1103/PhysRevLett.96.181602](https://doi.org/10.1103/PhysRevLett.96.181602)&rbrack;

The slogan "ER = EPR" is due to:

 * {#MaldacenaSusskind13} [[Juan Maldacena]], [[Leonard Susskind]], _Cool horizons for entangled black holes_, Fortsch. Phys. 61 (2013) 781-811 &lbrack;[arXiv:1306.0533](http://arxiv.org/abs/1306.0533), [doi:10.1002/prop.201300020](https://doi.org/10.1002/prop.201300020)&rbrack;

* {#Susskind14} [[Leonard Susskind]], *ER=EPR, GHZ, and the consistency of quantum measurements*, Fortsch. Phys. **64** 1 (2016) 72-83 &lbrack;[arXiv:1412.8483](https://arxiv.org/abs/1412.8483), [doi:10.1002/prop.201500094](https://doi.org/10.1002/prop.201500094)&rbrack;

An email exchange of similar content that happened half a year earlier is recalled in:

* {#VerlindeVerlinde22} [[Erik Verlinde]], [[Herman Verlinde]], *A Conversation on ER = EPR* &lbrack;[arXiv:2212.09389](https://arxiv.org/abs/2212.09389)&rbrack;

See also

* Wikipedia, *[ER=EPR](https://en.wikipedia.org/wiki/ER%3DEPR)* 

* Xin Jiang, Peng Wang, Houwen Wu, Haitang Yang:  *Realization of "ER=EPR"* &lbrack;[arXiv:2411.18485](https://arxiv.org/abs/2411.18485)&rbrack;

   

[[!redirects ER=EPR]]
[[!redirects er=epr]]
[[!redirects ER= EPR]]
[[!redirects ER =EPR]]
