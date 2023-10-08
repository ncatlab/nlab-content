
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The *quantum IO monad* &lbrack;[Altenkirch & Green (2010)](#AltenkirchGreen10)&rbrack; is a [[monad in computer science]] (implemented in [[Haskell]]) which means to model the control of a classical computer over a [[quantum computation]]-device that it is connected to: Much like the classical [[IO monad]] (or generally a [[state monad]]) models the effects of writing to and reading from an external device, so the quantum IO monad means to model the effect of instructing a quantum device to prepare a [[qbit]]-state or to read out ([[quantum measurement|measure]]) that qbit state, etc.

## Related concepts

* [[quantum programming languages]]

* [[IO monad]]


## References

* {#AltenkirchGreen10} [[Thorsten Altenkirch]], [[Alexander Green]], *The quantum IO monad*, Ch. 5 of: Simon Gay, Ian Mackie (eds.): *Semantic Techniques in Quantum Computation* (2010) 173-205 &lbrack;[pdf](http://www.cs.nott.ac.uk/~txa/publ/qio-chapter.pdf), [doi:10.1017/CBO9781139193313.006](https://doi.org/10.1017/CBO9781139193313.006)&rbrack;

Exposition:

* [[Thorsten Altenkirch]], *The Quantum IO Monad*, Nottingham (2006) &lbrack;[pdf](http://www.cs.nott.ac.uk/~txa/talks/qnet06.pdf), [[Altenkirch-QIOMonad.pdf:file]]&rbrack;

* [[Alexander Green]], *The Quantum IO Monad*, Nottingham  (2007) &lbrack;[pdf](http://drinkupthyzider.co.uk/asg/pdfs/bctcs07.pdf), [[Green-QIOMonad.pdf:file]] &rbrack;

* [[Alexander Green]], *Towards a formally verified functional quantum programming language* (2010) &lbrack;[eprints:11457](http://eprints.nottingham.ac.uk/11457)&rbrack;


Implementation in [[Haskell]]:

* [[Alexander Green]], *[hackage.haskell.org/package/QIO](https://hackage.haskell.org/package/QIO)*


