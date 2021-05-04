
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The symbols *ER = EPR* (pronounced: "ee arr is ee pee arr") are the name of a hypothesis about [[quantum gravity]], claiming, somewhat vaguely, that [[entangled particles]] ([[EPR paradox|Einstein-Podolsky-Rosen phenomenon]]) are connected by a [[wormhole]] ([[Einstein-Rosen bridge]]). 

This idea was proposed by [Maldacena-Susskind 13](#MaldacenaSusskind13) as a solution for the [[black hole firewall problem]].

## As a slogan for the Ryu-Takayanagi formula
 {#AsASloganForTheRyuTakayanagiFormula}

The idea may usefully be compared -- and maybe is in parts a way of turning into prose -- the *[[Ryu-Takayanagi formula]]* (which has a more well-defined content is a *[[theorem]]* in a class of discrete [[tensor network]]-models), which equates 

* **(quantum entanglement:)** the [[entanglement entropy]] of a [[boundary field theory|boundary]] [[quantum field theory]] in a subspace of an [[asymptotic boundary]] 

with 

* **(global spacetime structure:)** the minimal area of a [[coboundary|cobounding]] [[hypersurface]] in an ambient curved [[bulk]] [[spacetime]].

Concretely, in [[tensor network]]-models of [[AdS2/CFT1 duality]], the [[entanglement entropy]] $S_A$ of any [[Majorana dimer code]]-[[tensor network]] [[quantum state|state]] turns out to count the number of dimers cthat cross between the subregion $A$ and its [[complement]]:

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
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Yan 20](holographic+entanglement+entropy#Yan20)"
\end{imagefromfile}


In the case that the dimers correspond to the [[hyperbolic tesselation]] $\{5,4\}$ from the [[HaPPY code]], this entropy formula 

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

Following [Sati-Schreiber 19c](#SatiSchreiber19c) we recognize the above dimer/bit-thread networks from [JGPE 19](#JGPE19), [Yan 19](#Yan19)
as *[[chord diagram]]*-encodings of holographic bulks ([p. 38](https://arxiv.org/pdf/1912.10425v3.pdf#page=38)).

Notice that the formula for the [[entanglement entropy]] in the [[Majorana dimer code]]  holds generally, for *any* configuration and hence any underlying [[chord diagram]].

In conclusion, note how each [[chord]] here reflects at the same time:

1. (ER) one [[entanglement|entangled pair]] of [[qbits]] in the [[boundary field theory|boundary]] [[quantum system]];

1. (EPR) a [[geodesic]] through the [[hyperbolic plane]] [[bulk]] spacetime,

which is a (rigorous) state of affairs clearly reminiscent of the "ER = EPR" slogan (except that wormholes are replaced by minimal area hypersurfaces, here: geodesics).

For more on this see at *[[holographic entanglement entropy]]*.


## Related entries

* [[entanglement]]

* [[wormhole]]

* [[holographic entanglement entropy]]

* [[black hole firewall problem]]


## References

The original article:

 * {#MaldacenaSusskind13} [[Juan Maldacena]], [[Leonard Susskind]], _Cool horizons for entangled black holes_, Fortsch. Phys. 61 (2013) 781-811, 2013 ([arXiv:1306.0533](http://arxiv.org/abs/1306.0533), [doi:10.1002/prop.201300020](https://doi.org/10.1002/prop.201300020)) 

See also

* Wikipedia, *[ER=EPR](https://en.wikipedia.org/wiki/ER%3DEPR)* 
   

[[!redirects ER=EPR]]
[[!redirects er=epr]]
[[!redirects ER= EPR]]
[[!redirects ER =EPR]]
