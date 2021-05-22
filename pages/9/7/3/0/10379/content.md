
# Simple examples of Chu spaces
* table of contents
{: toc}

## Idea

The simplest cases of [[Chu spaces]] can be thought of simply  as matrices over a set $\Sigma$, that is, a rectangular array whose 
entries are drawn from $\Sigma$. The case most usually considered is $\Sigma = \mathbf{2}:=\{0,1\}$, and special cases of this then correspond to many relational structures. In fact, such a 'dyadic' Chu space is just another way of representing a relation from the set of labels for the rows, to that of the labels of columns of the matrix. The role of $\mathbf{2}$ can be replaced by an arbitrary set with suitable modifications of the resulting theory.


## Definitions

The definition we will give here is just an ultra-special case of that given in [[Chu construction]].

+-- {: .num_defn #space}
###### Definition

A _(dyadic or two valued) Chu space_ $\mathcal{P}$ is a triple $(P_o, \models_P, P_a)$, where $P_o$ is a set of _objects_, and $P_a$ is a set of _attributes_.  The _satisfaction_ relation $\models_P$ is a subset of $P_o\times P_a$.
=--

The terminology used here is motivated by the link with [[formal concept analysis]].  Alternative terminologies include (from Pratt's [Coimbra notes](http://boole.stanford.edu/pub/coimbra.pdf)) $P_o$ is a set of  *points* constituting the *carrier*, whilst $P_a$ is the set of *states*, which  constitutes the *cocarrier* of the Chu space.

+-- {: .num_defn #transform}
###### Definition

A _morphism_ or _Chu transform_ from a Chu space $(P_o, \models_P, P_a)$ to a Chu space $(Q_o, \models_Q, Q_a)$ is a pair of functions $(f_a,f_o)$ with $f_o : P_o\to Q_o$ and $f_a : Q_a \to P_a$ such that, for any $x\in P_o $ and $y \in Q_a$,

$$f_o(x)\models_Q y  \iff  x \models_P f_a(y).$$
=--

This looks very much like some form of adjointness condition, and in particular cases, of course, it is.

In the above, the Chu space was thought of as 'relating' $P_o$ to $P_a$, but, equally well, such a relation relates $P_a$ to $P_o$, i.e. given any dyadic Chu space, there is a dual one:

+-- {: .num_defn #dual}
###### Definition

If $\mathcal{P} = (P_o, \models_P, P_a)$ is a dyadic Chu space, then $\mathcal{P}^\perp = (P_a, \models_P^{op}, P_o)$ is the _dual Chu space_ of $\mathcal{P}$. (It just reverses the roles of objects and attributes.)
=--


## Related concepts

* [[formal concept analysis]]

* [[topological system]] (as in the book of [[Steve Vickers]] 'Topology via Logic').


## References

* [[Vaughan Pratt]], [Chu Spaces](http://boole.stanford.edu/pub/coimbra.pdf)


The links with [[formal concept analysis]] are in:

* [[Guo-Qiang Zhang]]  _[Chu spaces, concept lattices, and domains](http://newton.eecs.cwru.edu/papers/chu-concepts-entcs.pdf)_ in Brookes, S., Panangaden, P., eds.: Electronic Notes in Theoretical Computer Science. Volume 83., (2004) 

* [[P. Hitzler]], Guo-Qiang Zhang.: _A cartesian closed category of approximating concepts_
In: Proceedings of the 12th International Conference on Conceptual Structures, 
ICCS 2004, Huntsville, Al, July 2004. Volume 3127 of Lecture Notes in Artificial 
Intelligence., Springer-Verlag (2004) 170&#8211;185.

* Guo-Qiang Zhang, Shen, G.: [Approximable Concepts, Chu spaces, and information systems](http://www.tac.mta.ca/tac/volumes/17/5/17-05.pdf), Theory and Applications of Categories 17, 2006, no.7

General applications of Chu spaces are in:

* [Special TAC Volume on Chu spaces and Applications](http://www.tac.mta.ca/tac/volumes/17/toc17.pdf)


[[!redirects Chu spaces, simple examples]]
[[!redirects simple examples of Chu spaces]]
[[!redirects simple example of Chu spaces]]
