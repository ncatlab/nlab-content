+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

[[!redirects hypergroup]]
[[!redirects hypermagmas]]
[[!redirects hypergroups]]
[[!redirects comagma]]


## Idea

A **hypermagma** $X$ relates to a [[magma]] like a [[hypergraph]] relates to an ordinary [[graph]] i. e. the binary operation on $X$ becomes multi-valued by taking value in $2^X$ instead of $X$.

By imposing further axioms one obtains the concept of a **hypergroup** corresponding to the generalization of the [[group|group concept]] in this context.

With the commutative variant of a [[canonical hypergroup]] this "_multi-valued hyperalgebra_" has recently gained prominence in [[number theory]] and algebraic geometry over $\mathbb{F}_1$ (cf. [[hyperring]]).

## Definition

A set $X$ together with a function $X\times X\to 2^X$ is called a _hypermagma_. The function is normally denoted by $\dot$ and called the _hyperlaw_ (, _hyperoperation_ or _hyperproduct_) of $X$. A _morphism of hypermagmas_ from $X$ to $Y$ is a function $f:X\to Y$ such that $f(x\dot y)\subset f(x)\dot f(y)$ for all $x,y\in X$. The morphism is called _good_ if $f(x\dot y) = f(x)\dot f(y)$.

A hypermagma $X$ that satisfies furthermore:

* $(x\dot y)\dot z = x\dot (y\dot z)$ for all $x,y,z\in X$ and

* $x\dot X= X = X\dot x$ for all $x\in X$

is called a _hypergroup_.

## Remarks

By imposing commutativity and banning $\empty$ as a value for the hyperoperations one arrives at the notion of a [[canonical hypergroup]] that enters into the definition of a [[hyperring]].

Hypergroups whose hyperlaw is valued in singleton subsets correspond to groups.

Some authors demand a hypergroup to be non-empty and sometimes the hyperlaw is valued in non-empty subsets. The definition here follows the terminology in [Haddad-Sureau (1990)](#HS90).

## Related entries

* [[magma]]

* [[hypermonoid]]

* [[canonical hypergroup]]

* [[hyperring]]

* [[hypergraph]]

* [[historical notes on quasigroups]]

## Reference

* S. D. Comer, _Polygroups derived from cogroups_ , J. Algebra **89** no.2 (1984) pp.397-405. 

* P. Corsini, V. Leoreanu-Fotea, _Applications of Hyperstructure Theory_ , Kluwer Dordrecht
2003.

* {#HS90}L. Haddad, Y. Sureau, _Les cogroupes et la construction de Utumi_ , Pacific J. Math. **145** no.1 (1990) pp.17-58. ([abstract](http://projecteuclid.org/euclid.pjm/1102645606))

* L. Haddad, Y. Sureau, _Les groupes, les hypergroupes et l'&#233;nigme des Murngin_ , JPAA **87** (1993) pp.221-235.

* G. L. Litvinov, _Hypergroups and Hypergroup Algebras_ , arXiv:1109.6596 (2011). ([abtract](http://arxiv.org/abs/1109.6596))
* F. Marty,  _Sur une g&#233;n&#233;ralization de la notion de groupe_ , IV Congr&#232;s des Math&#233;maticiens Scandinaves, Stockholm 1934.
