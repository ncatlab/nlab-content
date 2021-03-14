
# Contents
* table of contents
{: toc}

See also the [Petri net](http://www.azimuthproject.org/azimuth/show/Petri+net) in The Azimuth Project.

## Introduction

Petri nets are a well known model of concurrent computation, generalising [[transition systems]] by using a built in notion of resource.  Their use is widespread in modelling manufacturing systems, optimising control systems and in resource critical aspects of operational research, as well as being a useful model of computation.  Because of this they exist in many variants : colored, algebraic, probabilistic, timed, ..., and hence there are many forms of the basic definition, each thought best of that particular application.

The initial use, here, is for their links with [[transition systems]], [[event structures]], [[asynchronous automata]] etc., leading on to their comparison with [[higher dimensional automaton|higher dimensional automata]] and [[higher dimensional transition system]]s, so the first definition we will use is that given by Winskel and Nielsen (see references below), but first we will attempt to give some idea of what a Petri net is and what is does.


## Idea

The idea of a simple Petri net is based on a simple manufacturing shop.  You have various 'transitions' or manufacturing 'events' that form part of the various process occurring in the 'shop'. These typically take parts (of the final object), do something to them, such as combining two or more different parts to make a more complicated one, (for instance, putting the wheels on a car).

Parts, represented by 'tokens' are stored in 'places' and the assembly process are known, as above, as 'events' or 'transitions' (depending on the source being used for the theory).  The relationships are typically represented graphically.  For instance:

<svg width="294" height="253" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="60508">
 <g>
  <title>Layer 1</title>
  <path fill="#ffffff" stroke="#000000" stroke-width="2" d="m23.007811,27c0,-14.36464 11.635359,-26 25.999998,-26c14.364643,0 26.000004,11.63536 26.000004,26c0,14.364639 -11.635361,26 -26.000004,26c-14.364639,0 -25.999998,-11.635361 -25.999998,-26z" id="svg_60508_1"/>
  <path fill="#ffffff" stroke="#000000" stroke-width="2" d="m222.007813,27c0,-14.36464 12.082886,-26 27,-26c14.917114,0 27,11.63536 27,26c0,14.364639 -12.082886,26 -27,26c-14.917114,0 -27,-11.635361 -27,-26z" id="svg_60508_2" transform="rotate(3.74069e-06, 320.272, -74)"/>
  <path fill="#ffffff" stroke="#000000" stroke-width="2" d="m120.007813,226c0,-14.364624 12.082886,-26 27,-26c14.917114,0 27,11.635376 27,26c0,14.364624 -12.082886,26 -27,26c-14.917114,0 -27,-11.635376 -27,-26z" transform="rotate(3.74069e-06, 320.272, -74)" id="svg_60508_3"/>
  <rect fill="#ffffff" stroke="#000000" stroke-width="2" x="100.007808" y="117" width="98" height="21" id="svg_60508_4"/>
  <line fill="none" stroke="#000000" stroke-width="2" x1="68.00782" y1="46.999999" x2="148.00782" y2="118.000002" id="svg_60508_5"/>
  <line fill="none" stroke="#000000" stroke-width="2" x1="230.007808" y1="47.000002" x2="149.007807" y2="116.000003" id="svg_60508_6"/>
  <line fill="none" stroke="#000000" stroke-width="2" x1="147.007813" y1="139" x2="148.007813" y2="199" id="svg_60508_7"/>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="105.008" y="65" id="svg_60508_8" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">1</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="188.008" y="67" id="svg_60508_9" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">1</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="157.008" y="170" id="svg_60508_10" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">1</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="212.008" y="128" id="svg_60508_11" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">e</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="8.00781" y="26" id="svg_60508_12" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">A</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="286.008" y="27" id="svg_60508_13" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">B</text>
  <text fill="#000000" stroke="#000000" stroke-width="0" x="187.008" y="226" id="svg_60508_14" font-size="24" font-family="serif" text-anchor="middle" xml:space="preserve">C</text>
  <ellipse fill="#000000" stroke="#000000" stroke-width="2" cx="36.007813" cy="23" id="svg_60508_15" rx="4" ry="4"/>
  <ellipse fill="#000000" stroke="#000000" stroke-width="2" cx="60.007813" cy="24" rx="4" ry="4" id="svg_60508_16"/>
  <ellipse fill="#000000" stroke="#000000" stroke-width="2" cx="247.007813" cy="23" rx="4" ry="4" id="svg_60508_17"/>
 </g>
</svg>

represents a system with three places (labelled $A$, $B$, and $C$) and one event/ transition (labelled $e$).  Shown is a situation represented by an initial 'marking' where there are two tokens in $A$, one in $B$, and none in $C$. (The convention is that places are shown as circles and events as rectangles.)

Suppose that the 'event' takes one 'part' of type $A$, one of type $B$ and produces one of type $C$.  (This is indicated on the diagram by the labels on the edges.  Clearly with the available  resources the even $e$ is able to be performed.  (The usual Petri net jargon for this is that '$e$ is enabled'.) In this case, $e$ can be 'fired' and the result will yield a marking of one token in $A$, none in $B$ and one in $C$.  This sort of structure gets abstracted as follows:

+--{: .un_defn}
###### Definition

A **Petri net** $N$ consists of

* a set $P$ of _places_;

* an _initial marking_ $M_0 \in \mathbb{N}^P$, so $M_0 : P \to \mathbb{N}$;

* a set $E$ of _events_; and

* two functions 

  *  $pre: P\times E\to \mathbb{N}$, and

  *   $post:  P\times E\to \mathbb{N}$.
=--

## Categorical Semantics of Petri Nets {#semantics}

The functions $pre$ and $post$ can be [[curried]] to write a Petri net as a pair of functions 

\begin{centre}
\begin{tikzcd} 
E \ar[r,shift left=.5ex,"\mathrm{pre}"] \ar[r,shift right=.5ex,"\mathrm{post}",swap] & \mathbb{N} [P]
\end{tikzcd}
\end{centre}

where $\mathbb{N}[P]$ denotes the [[free monoid|free commutative monoid]] on the set $P$ of places. Written this way, the analogy to [[directed graph|graphs]] is clearer. The main difference is that now the source and target functions land in a [[free monoid|free commutative monoid]] rather than just a set. Thus, Petri nets can be thought of as _symmetric monoidal graphs_ because each edge is a multi-edge between a permutable sum of vertices. Just as [[directed graph|graphs]] generate [[free categories]], Petri nets should generate free [[symmetric monoidal categories]]. As Petri nets often model processes in various sciences, the free symmetric monoidal categories that they generate model the operational semantics of these processes. For a given Petri net $P$, the free symmetric monoidal $FP$ that it generates should have objects given by possible markings of $P$ and morphisms given by ways of composing the events in sequence and in parallel.

The first to explore this idea were [Meseguer and Montanari](#monoids) who constructed an adjunction between Petri nets and a subcategory of the category $CMC$ of [[commutative monoidal categories]]. This adjunction was modified in [_Petri nets based on Lawvere theories_](#gen) to get

\begin{center}
\begin{tikzcd}
\mathsf{Petri} \ar[r,bend left,"F"] & \ar[l,bend left,"U"] \mathsf{CMC}
\end{tikzcd}
\end{center}
Although morally Petri nets generate free symmetric monoidal categories, it turns out that because they have a free _commutative_ monoid of places, they more naturally generate [[commutative monoidal categories]], symmetric monoidal categories of an unusually strict type. [[Commutative monoidal categories]] don't show up often in nature because they aren't the result of a [[coherence]] theorem for symmetric monoidal categories. [[Saunders Mac Lane|Mac Lane's]] [[coherence theorem for symmetric monoidal categories]] says that every symmetric monoidal category is symmetric monoidally equivalent to a [[symmetric monoidal category|strict symmetric monoidal category]] which may have nontrivial symmetry morphisms. However, commutative monoidal categories have symmetry morphisms which are given by the identity so they aren't the [strictifications](https://ncatlab.org/nlab/show/coherence+theorem#strictification) of symmetric monoidal categories.

Computer scientists also haven't been satisfied with commutative monoidal categories as a categorical semantics for Petri nets. Commutative monoidal categories are said to exhibit the collective token philosophy (see e.g. [Glabeek and Plotkin](#philosophy)), where tokens do not have individual idenities. On the other hand, symmetric monoidal categories are said to have the individual token philosophy where the individual identites of the tokens are retained. The easiest to see where an issue shows up is with a variation of the [[Eckmann-Hilton argument]]. Let $C$ be a commutative monoidal category and let $f,g \colon a \to a$ be morphisms from an object a to itself. Then,
$$\begin{aligned}
g \circ f + 1_a & = g \circ f + 1_a \circ 1_a \\
&= (g+ 1_a)\circ (f + 1_a) \\
&= (g + 1_a) \circ (1_a + f) \\
& = g \circ 1_a + 1_a \circ f \\
&= g + f 
\end{aligned}$$

So in a commutative monoidal category $g \circ f + 1_a = g+ f$ even though they have very different semantic interpretations: one represents sequential composition and the other represents parallel composition.

One possible fix to this is to change the definition of Petri net. In [_Functorial Models for Petri Nets_](#functorial) the authors introduced [[Pre-net|pre-nets]]. A pre-net is a pair of functions from a set of events to the free monoid on a set of places. The key difference is that now every event is equipped with an ordering on the input and output of each transition. With pre-nets, there is a natural [[adjunction]] between the category $PreNet$ of pre-nets and $SMC$ the category of strict monoidal categories
 
\begin{center}
\begin{tikzcd}
\mathsf{PreNet} \ar[r,bend left,"A"] & \ar[l,bend left,"B"] \mathsf{SMC}
\end{tikzcd}
\end{center}

which can be composed with the adjunction which freely adds symmetries to a strict monoidal category to get an adjunction


\begin{center}
\begin{tikzcd}
\mathsf{PreNet} \ar[r,bend left,"L"] & \ar[l,bend left,"R"] \mathsf{SSMC}
\end{tikzcd}
\end{center}

where $SSMC$ is the category of [[symmetric monoidal category|strict symmetric monoidal categories]]. This gives a categorical operational semantics for pre-nets which obeys the individual token philosophy and avoids the pitfall of the above computation. Pre-nets can be turned into Petri nets via [[abelianization]]. For a given Petri net $P$, it's abelianization forgets about the ordering on the input and output of each event. Therefore, to obtain a categorical semantics for a Petri net $P$ which obeys the individual token philosophy, a pre-net $Q$ can be chosen which abelianizes to $P$. Then, the categorical semantics for $P$ can defined as the free strict symmetric monoidal category $L(Q)$.

## References

* [[John Baez]], Fabrizio Genovese, [[Jade Master]], [[Michael Shulman]], _Categories of Nets_, ([arXiv:2101.04238](https://arxiv.org/abs/2101.04238))

* [[G. Winskel]], M. Nielsen, _Models for concurrency_, Handbook of Logic in Computer Science vol. 3, pp. 100 -- 200, Oxford Univ. Press 1994. (see also [online technical report](http://www.daimi.au.dk/PB/463/PB-463.pdf)).

* [[John C. Baez]] and [[Jacob Biamonte]], _Quantum techniques in stochastic mechanics_, World Scientific, 2018. [World Scientific](https://www.worldscientific.com/worldscibooks/10.1142/10623#t=suppl) [pdf](http://math.ucr.edu/home/baez/stoch_stable.pdf)

* [wikipedia](http://en.wikipedia.org/wiki/Petri_net)

For an introduction to Petri nets (en francais, which is very clear and accessible) look at

* [[Robert Valette]], [Les R&#233;seaux de Petri](http://homepages.laas.fr/robert/enseignement.d/cour01.pdf).

On the connection to linear logic:

* [[Uffe Engberg]] and [[Glynn Winskel]], _Petri nets as models of linear logic_. CAAP 1990. Lecture Notes in Computer Science, vol 431. Springer, Berlin, Heidelberg. [Springer](https://link.springer.com/chapter/10.1007/3-540-52590-4_46), [pdf on ResearchGate](https://www.researchgate.net/publication/318253097_Petri_Nets_as_Models_of_Linear_Logic)

On the categorical semantics of Petri nets:

* {#monoids} [[José Meseguer]] and [[Ugo Montanari]], _Petri nets are monoids_, Information and Computation, Volume 88, Issue 2, Pages 105-155, 1990. [journal](https://www.sciencedirect.com/science/article/pii/0890540190900138), [pdf](https://core.ac.uk/download/pdf/82342688.pdf)

* {#gen} [[Jade Master]], _Petri nets based on Lawvere theories_, Mathematical Structures in Computer Science 30, no. 7 (2020): 833-864. Available at [journal](https://www.cambridge.org/core/journals/mathematical-structures-in-computer-science/article/petri-nets-based-on-lawvere-theories/9E0F011860A1285DDC498B740774FBDC)


* {#functorial} [[Roberto Bruni]], [[José Meseguer]], [[Ugo Montanari]], and [[Vladimiro Sassone]]. _Functorial models for Petri nets_ Information and Computation 170, no. 2 (2001): 207-236. [pdf](https://eprints.soton.ac.uk/264742/1/prenetsIandCOff.pdf)

* {#philosophy} [[Rob J. van Glabbeek]], and [[Gordon Plotkin]]. _Configuration structures, event structures and Petri nets_ Theoretical Computer Science 410, no. 41 (2009): 4111-4159. Available at [pdf](https://arxiv.org/abs/0912.4023)

[[!redirects Petri net]]
[[!redirects Petri nets]]
category: computer science