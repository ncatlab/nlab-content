
> This entry is about induction in the sense of [[logic]]. For induction (functors) in [[representation theory]] see _[[induced module]]_, _[[induced comodule]]_, _[[cohomological induction]]_. 

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The **principle of induction** says that if a property of the 
[[natural numbers]] 

1. is [[true]] for $0 \in \mathbb{N}$;

1. if it is true for $n \in \mathbb{N}$ then it is true for $n+1$;

then it is true for every $n \in \mathbb{N}$. The intuitive notion of a property is in practical mathematics identified with (belonging to) a subset $S\subseteq\mathbb{N}$. Thus the mathematical induction says that if $0\in S$ and if $\forall n\in\mathbb{N}$ $n\in S\implies n+1\in S$ then $S = \mathbb{N}$. This is the way in
the formal Dedekind-Peano arithmetics. Usually in logic one however uses a weaker form of induction which can be stated in a first order language (or in a type theory), namely where one limits to properties given by the predicates $P(n)$ [[dependent type|depending]] on natural numbers. The corresponding conclusion is the [[proposition]] $n \in \mathbb{N} \vdash P(n)$. 
The latter version of the principle of induction is weaker because there are only
$\aleph_0$ predicates but $2^{\aleph_0}$ subsets of $\mathbb{N}$.

When formulated in one of the formalizations below, one finds that the principle of induction for propositions depending on natural numbers is the simplest special case of a very general notion of induction over _[[inductive types]]_. Other examples are induction over [[lists]], [[trees]], terms in a [[logic]], and so on.


The [[duality|dual]] notion is that of _[[coinduction]]_.


## Formalization

### By initial algebras over endofunctors

The induction principle may neatly be formalized in terms of the notion of [[initial algebras of an endofunctor]].

In the [[category]] [[Set]], the [[initial algebra]] [[algebra for an endofunctor|for the endofunctor]] $F: X \to 1 + X$ is $\langle 0, s \rangle : 1 + \mathbb{N} \to \mathbb{N}$, where $\mathbb{N}$ is the set of [[natural numbers]], $0$ is the smallest natural number, and $s$ is the [[successor]] operation. 

In terms of this the **principle of induction** is equivalent to saying that there is no proper [[subobject|subalgebra]] of $\mathbb{N}$; that is, the only subalgebra is $\mathbb{N}$ itself. This follows from the general property of [[initial objects]] that [[monomorphisms]] to them are [[isomorphisms]].



## Related concepts

* [[transfinite induction]]

* [[deduction]]

* [[inductive type]]

* [[inductive definition]]

* [[recursion]]

## References

* [[Jiří Adámek]], Stefan Milius, Lawrence Moss, _Initial algebras and terminal coalgebras: a survey_ ([pdf](https://www.tu-braunschweig.de/Medien-DB/iti/survey_full.pdf))

* [[Bart Jacobs]], Jan Rutten, _A tutorial on (co)algebras and (co)induction_, [pdf](http://www.cs.ru.nl/~bart/PAPERS/JR.pdf) EATCS Bulletin (1997); extended and updated version: _An introduction to (co)algebras and (co)induction_,  In: D. Sangiorgi and J. Rutten (eds), Advanced topics in bisimulation and coinduction, p.38-99, 2011, [pdf](http://www.cwi.nl/~janr/papers/files-of-papers/2011_Jacobs_Rutten_new.pdf) 62 pp.

* Ch. 3, Formal arithmetics, in: Elliott Mendelson, _Introduction to mathematical logic_, D. Van Nostrad 1964


[[!redirects induction]]
[[!redirects inductions]]

[[!redirects mathematical induction]]

[[!redirects induction principle]]
[[!redirects principle of induction]]

[[!redirects inductive argument]] 

[[!redirects induction scheme]]
[[!redirects induction schemes]]
[[!redirects induction schema]]
[[!redirects induction schemata]]
[[!redirects induction schemas]]
