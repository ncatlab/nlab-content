
##Idea 

Formal concept analysis is about extracting the relationships and hierarchies available from the common attributes shared by objects.


A _formal context_ is, simply, a dyadic [[Chu spaces, simple examples|Chu space]]. More precisely:

+-- {: .num_defn #space}
###### Definition

A _(dyadic or two valued) Chu space_ $\mathcal{P}$ is a triple $(P_o, \models_P, P_a)$, where $P_o$ is a set of _objects_, and $P_a$ is a set of _attributes_.  The _satisfaction_ relation $\models_P$ is a subset of $P_o\times P_a$.
=--

The terminology is that used in Formal Context Analysis. Such an object gives an array representing a relation between a set of objects and a set of attibutes. If an object, $o\in P_o$, satisfies attribute $a\in P_a$, that is $o\models_P a$, one puts a 1 in the $(o,a)$- position in the array, otherwise one puts a 0. This is thus the usual classical representation of the relation as a subset of the product. 

The task of the analysis is to see if the data encoded in the array allows one to group objects or attributes together so as to glean more information about the given relationship between the two sets.

To quote from Zhang and Shen:
>The novel idea of FCA is the clustering of attributes based
on the algebraic principle of Galois connection, forming a partially ordered set called (a) concept lattice. The clustering determines which collection of attributes forms a coherent entity called a concept, by the philosophical criteria of unity between extension and
intension. The extension of a concept consists of all objects belonging to the concept,
while the intension of a concept consists of attributes common to all these objects. One
can then take this as the defining property of a concept: _a collection of attributes which
agrees with the intension of its extension._

## Related concepts

* [[Chu spaces, simple examples|Chu space]]

* [[Galois connection]]

##References

* Ganter, B., & Wille, R. _Formal concept analysis: mathematical foundations_. Springer Science & Business Media, (2012). [doi](https://doi.org/10.1007/978-3-642-59830-2)
* Radim Belohlavek, Introduction to formal concept analysis [pdf](http://phoenix.inf.upol.cz/esf/ucebni/formal.pdf)
* Caf&#233; discussion [Formal Concept Analysis](http://golem.ph.utexas.edu/category/2013/09/formal_concept_analysis.html#more)

* Guo-Qiang Zhang, Shen, G.: [Approximable Concepts, Chu spaces, and information systems](http://www.tac.mta.ca/tac/volumes/17/5/17-05.pdf), Theory and Applications of Categories 17, 2006, no.7


* [Formal Concept Analysis Homepage](https://upriss.github.io/fca/fca.html)

[[!redirects formal concept lattice]]
[[!redirects Formal Concept Analysis]]