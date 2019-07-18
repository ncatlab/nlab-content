
#Contents#
* table of contents
{:toc}

## Idea

A _Moore machine_ is a particular type of [[finite state automaton]].

## Definition


A finite _Moore machine_, $\mathbf{A}$, consists of

* $Q$, a finite set of _states_;

* $A$, an _input alphabet_;

* $B$, an _output alphabet_;

* $q_0$, an _initial state_;

* $\delta: Q\times A\to Q$, a _transition function_;

and

* $\lambda:Q\to B$, the _state output function_.

These determine an _output response function_, $\omega_\mathbf{A}:A^*\to B^*$ and a _characteristic function_ $\chi_\mathbf{A}:A^*\to B$ that picks out the language recognised by the machine.

Here we have, as usual, denoted by $A^*$ the [[free monoid]] (of all strings of symbols) over the 'alphabet' $A$, etc.

##Related entries

* [[Mealy machine]]

* [[automaton]]

##References

* [[Mark V. Lawson]], _[Finite automata](http://www.ma.hw.ac.uk/~markl/books.html)_, CRC Press, see also [here](http://www.ma.hw.ac.uk/~markl/teaching/AUTOMATA/kleene.pdf) for a shorter version in the form of Course Notes.

[[!redirects Moore machines]]