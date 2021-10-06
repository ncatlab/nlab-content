
#Contents#
* table of contents
{:toc}

## Idea

Diagonal arguments are typically arguments that place limitations on the extent that a set $T$ can "talk about" attributes of elements of $T$. They are related to the paradoxes of old (e.g., the [[liar paradox]], [[Russell's paradox]]) that typically involve some degree of self-reference. 

Traditional "diagonal arguments" enter the proofs of, for example, 

* [[Cantor's theorem]]

* [[Gödel]]'s [[incompleteness theorem]]

* [[halting theorem]]

but also the traditional construction of a 

* [[fixed-point combinator]] 

due to [[Haskell Curry]]. 

As explained by [Yanofsky](#Yan) (after Lawvere), each of these diagonal arguments can be viewed as instances of the

* [[Lawvere fixed point theorem]]

which places limitations on how a set $T$ can self-describe $Y$-valued attributes of $T$ (a set $Y^T$) via a function $T \to Y^T$, or via a function $T \times T \to Y$. The name comes from a construction that involves the [[diagonal map]] $T \to T \times T$. 

## Link

* Wikipedia, _[Diagonal argument](http://en.wikipedia.org/wiki/Diagonal_argument)_

## References

Cantor used a diagonal argument to show that $|X|\ncong|2^X|$ for the first time here:

* [[Georg Cantor]], _&#220;ber eine elementare Frage der Mannigfaltigskeitslehre_ , Jahresbericht DMV **1** (1891) pp.75-78. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002113910))

But he was anticipated by

* Paul Du Bois-Reymond, _&#220;ber asymptotische Werthe, infinit&#228;re Approximationen und infinit&#228;re Aufl&#246;sung von Gleichungen_ , Math. Ann. **8** (1874) pp.363-414. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002243067))

Lawvere's seminal ideas occurred in

* [[F. William Lawvere]], *Diagonal arguments and cartesian closed categories*, pp.134-145 in *Category Theory, Homology Theory and their Applications II (Battelle Institute Conference, Seattle, Wash., 1968, Vol. Two)*, Springer LNM **92** Berlin 1969. (Reprinted with an author's comment as TAC reprint **15** (2006): [link](http://www.tac.mta.ca/tac/reprints/articles/15/tr15abs.html))

For a leisurely account see the discussion in

* [[F. William Lawvere]], [[Stephen Schanuel]], *Conceptual Mathematics*, Cambridge University Press 1997.

A discussion of logic and rigor using Lawvere's ideas about the diagonal argument and Godel theorem 

* Misha Gromov. [*Ergostuctures, Ergologic and the Universal Learning Problem: Chapters 1, 2.*, p.14-18.](https://www.ihes.fr/~gromov/wp-content/uploads/2018/08/ergologic31.pdf#17)
2013.

A nice overview is

* {#Yan}  [[Noson Yanofsky]], _A Universal Approach to Self-Referential Paradoxes, Incompleteness and Fixed Points_, 2003  ([arXiv:0305282](http://arxiv.org/abs/math/0305282)) 
 

The necessary assumptions for Lawvere's account are reduced in various ways in

* [[David Michael Roberts]], _Substructural fixed-point theorems and the diagonal argument: theme and variations_ (2021) ([arXiv:2110.00239](https://arxiv.org/abs/2110.00239))




[[!redirects diagonal arguments]] 
[[!redirects diagonalization argument]]
[[!redirects diagonalization arguments]]


[[!redirects diagonal arguments]]
