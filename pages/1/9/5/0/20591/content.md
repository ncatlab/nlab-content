
#Contents#
* table of contents
{:toc}

## Idea

A _Mealy machine_ is a particular type of [[finite state automaton]].

A Mealy machine with input alphabet $A$ and output alphabet, $B$ is just a [[deterministic finite automaton]],which produces a letter of the output alphabet, $B$ at every transition step. More formally

## Definition

A finite _Mealy machine_, $\mathbf{A}$, consists of

* $Q$, a finite set of _states_;

* $A$, an _input alphabet_;

* $B$, an _output alphabet_;

* $q_0$, an _initial state_;

* $\delta: Q\times A\to Q$, a _transition function_;

and

* $\lambda:Q\times A \to B$, which associates  an output symbol with each transition.


Again as for [[Moore machines]], there is an output response function $\omega_\mathbf{A}:A^*\to B^*$ defined s follows:

if $x= x_1 \ldots x_n\in A^*$ and the states that $\mathbf{A}$ passes through when processing this string are $q_0, q_1, \ldots, q_n$, so diagrammatically

$$q_0\xrightarrow{x_1} q_1\xrightarrow{x_2}\ldots \xrightarrow{x_n} q_n,$$

define $\omega_\mathbf{A}(x)= \lambda(q_0,x_1)\ldots \lambda(q_{n-1},x_n)$.

Mealy machines and [[Moore machines]] have essentially the same descriptive power.

## Related entries

* [[Moore machine]]

* [[automata]]

* [[Mealy morphism]]

##References

* [[Mark V. Lawson]], _[Finite automata](http://www.ma.hw.ac.uk/~markl/books.html)_, CRC Press, see also [here](http://www.ma.hw.ac.uk/~markl/teaching/AUTOMATA/kleene.pdf) for a shorter version in the form of Course Notes.


* [[Dirk Pattinson]], _An Introduction to the Theory of Coalgebras_, [here](http://indiana.edu/~nasslli/2003/datas/DirkPattinson.pdf).


[[!redirects Mealy machines]]
