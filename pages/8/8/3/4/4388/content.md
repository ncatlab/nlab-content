
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computing
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


# Automata
* table of contents
{: toc}

## Idea

An *automaton* is an abstract concept of machine, modelled as a collection of states and transitions between states, together with an assignment of some external behavior (typically input and/or output) to these transitions.  A quintessential example of an automaton is a vending machine, which can be in any number of different states (e.g., "READY", "INSERT 2 TOKENS", "OUT OF SERVICE", etc.), and will transition between these states in response to user input (e.g., from "READY" to "INSERT 2 TOKENS" after the user makes a selection, and from "INSERT 2 TOKENS" to "INSERT 1 TOKEN" after the user inserts a token).

Many different notions of automaton exist in the literature.  For now this article only considers one fairly basic notion taken from [[Joy of Cats]], although it is by no means the simplest nor the most general.

## Definition

A __deterministic, sequential, Moore automaton__ is formally definable (as in [[Joy of Cats]]) as a sextuple ($Q$, $\Sigma$, $Y$, $\delta$,  $q_{0}$, $y$), where $Q$ is the set of states,  $\Sigma$ and $Y$ are the sets of input symbols and output symbols, respectively,  $\delta$:  $\Sigma$ $\times$ $Q$ $\to$ $Q$ is the transition map, $q_{0}$ $\epsilon$ $Q$ is the initial state, and $y$: $Q$ $\to$ $Y$ is the output map.  [[morphism|Morphisms]] from an automaton ($Q$, $\Sigma$, $Y$, $\delta$,  $q_{0}$, $y$) to an automaton ($Q$&#8242;, $\Sigma$&#8242;, $Y$&#8242;, $\delta$&#8242;,  $q_{0}$&#8242;, $y$&#8242;) are triples ($f_{Q}$, $f_{\Sigma}$, $f_{Y}$) of [[function|functions]] $f_{Q}:  Q \to Q\prime$,  $f_{\Sigma}: \Sigma \to \Sigma\prime$,  and $f_{Y}:  Y \to Y\prime$ satisfying the following conditions:

(i) preservation of transition: 
    $\delta\prime$($f_{\Sigma}$($\sigma$), $f_{Q}$($q$)) =      $f_{Q}$($\delta$($\sigma$, $q$)),

(ii) preservation of outputs: $f_{Y}$($y$($q$)) = $y$$\prime$($f_{Q}$($q$)),

(iii) preservation of initial state: 
      $f_{Q}$($q_{0}$) = $q_{0}\prime$.    

Note that in such an automaton, the outputs are determined by the current state alone (and do not depend directly on the input).

A morphism $f$ : ($Q$, $\delta$, $q_{0}$, $F$) $\to$ ($Q\prime$, $\delta\prime$, $q_{0}\prime$, $F\prime$) (called a __simulation__) is a function $f : Q \to Q\prime$ that preserves:

(i) the transitions, i.e., $\delta\prime$($\sigma$, $f$($q$)) = $f$($\delta$($\sigma$, $q$)),

(ii) the initial state, i.e., $f$($q_{0}$) = $q_{0}\prime$, and

(iii) the final states, i.e., $f[F] \subseteq F\prime$.


## The category of automata

There is a [[category]] $Aut$ whose [[object|objects]] are deterministic sequential Moore automata and whose [[morphism|morphisms]] are simulations.

## Examples

* [[Mealy machine]]

* [[Moore machine]]

* [[Conway's game of life]]


## Variants

There are several variant forms of automaton.  The above just gives a basic one. Others are treated in the entries:

* [[asynchronous automaton]];

* [[deterministic automaton]];

* [[nondeterministic automaton]].

There are tentative definitions of 

*[[higher dimensional automaton]]

which take a more nPOV of automata theory.




## References

* [[Jiri Adamek]], [[Horst Herrlich]], [[George Strecker]], *[[Abstract and Concrete Categories]]*, John Wiley and Sons, New York (1990) reprinted as: Reprints in Theory and Applications of Categories **17** (2006) 1-507 &lbrack;[tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html), [book webpage](http://katmat.math.uni-bremen.de/acc/)&rbrack;


* [[Mark V. Lawson]], _[Finite automata](http://www.ma.hw.ac.uk/~markl/books.html)_, CRC Press, see also [here](http://www.ma.hw.ac.uk/~markl/teaching/AUTOMATA/kleene.pdf) for a shorter version in the form of Course Notes.

* [[Jiří Adámek]], *Free algebras and automata realizations in the language of categories*, Commentationes Mathematicae Universitatis Carolinae **15**.4 (1974) 589-602 &lbrack;[eudml:16649](https://eudml.org/doc/16649)&rbrack;

* [[Jiří Adámek]], Věra Trnková, *Automata and algebras in categories* **37** Springer (1990) &lbrack;[ISBN:9780792300106](https://link.springer.com/book/9780792300106)&rbrack;


* Liang-Ting Chen, Henning Urbat, _A fibrational approach to automata theory_, [arxiv/1504.02692](http://arxiv.org/abs/1504.02692)

An early discussion of automata via [[string diagrams]] in the [[Cartesian monoidal category]] of [[finite sets]]:

* {#Hotz65} [[Günter Hotz]], _Eine Algebraisierung des Syntheseproblems von Schaltkreisen_, EIK, Bd. 1, (185-205), Bd, 2, (209-231) 1965 ([part I](https://www.magentacloud.de/lnk/LiPMlYfh), [part II](https://www.magentacloud.de/lnk/YivslUWJ), [[HotzSchaltkreise.pdf:file]])

Discussion of [[non-deterministic automata]] as 1-dimensional [[defect QFT|defect]] [[TQFTs]]:

* Paul Gustafson, [[Mee Seong Im]], Remy Kaldawy, [[Mikhail Khovanov]], Zachary Lihn, *Automata and one-dimensional TQFTs with defects* &lbrack;[arXiv:2301.00700](https://arxiv.org/abs/2301.00700)&rbrack;

Review: 

* [[Mee Seong Im]], *Correspondence between automata and one-dimensional Boolean topological theories and TQFTs*, talk at *[QFT and Cobordism](https://nyuad.nyu.edu/en/events/2023/march/quantum-field-theories-and-cobordisms.html)*, [[CQTS]] (Mar 2023) &lbrack;[web](Center+for+Quantum+and+Topological+Systems#ImMar2023), video:[YT](https://www.youtube.com/watch?v=q5kynYxwTmk)&rbrack;

category:computer science

[[!redirects automata]]
[[!redirects automatons]]

[[!redirects Aut]]

[[!redirects finite state automaton]]
[[!redirects finite state automatons]]
[[!redirects finite state automata]]

[[!redirects cellular automaton]]


