+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Algebra
+-- {: .hide}

=--
=--
=--

# Contents
* table of contents
{:toc}


[[!redirects hypermagmas]]
[[!redirects comagma]]


## Idea

A **hypermagma** $X$ relates to a [[magma]] like a [[hypergraph]] relates to an ordinary [[graph]] i. e. the binary operation on $X$ becomes multi-valued by taking value in $2^X$ instead of $X$.

By imposing further axioms one obtains the concept of a **hypergroup** corresponding to the generalization of the [[group|group concept]] in this context.

With the commutative variant of a [[canonical hypergroup]] this "_multi-valued hyperalgebra_" has recently gained prominence in [[number theory]] and algebraic geometry over $\mathbb{F}_1$ (cf. [[hyperring]]).

## Definition

A set $X$ together with a function $X\times X\to 2^X$ is called a _hypermagma_. The function is normally denoted by $\cdot$ and called the _hyperlaw_ (, _hyperoperation_ or _hyperproduct_) of $X$. A _morphism of hypermagmas_ from $X$ to $Y$ is a function $f:X\to Y$ such that $f(x\cdot y)\subset f(x)\cdot f(y)$ for all $x,y\in X$. The morphism is called _good_ if $f(x\cdot y) = f(x)\cdot f(y)$.

A hypermagma $X$ that satisfies furthermore:

* $(x\cdot y)\cdot z = x\cdot (y\cdot z)$ for all $x,y,z\in X$ ( _associativity_ ) and

* $x\cdot X= X = X\cdot x$ for all $x\in X$ ( _reproduction_ )

is called a _hypergroup_.

## Remarks

Given a hypermagma $X$ the hyperlaw is extended to $A,B\in 2^X$ by $A \cdot B=\cup_{a\in A,b\in B} a\cdot b$. Hence, $x\cdot Y$  is understood as $\{x\}\cdot Y$ etc.

Suppose $X$ is an associative hypermagma and $x\cdot y=\emptyset$ then $x\cdot y \cdot X=\emptyset$ and, accordingly, $y\cdot X\neq\X$ or $x\cdot X\neq X$ whence $X$ can't be a hypergroup. So we see that the hyperlaws of hypergroups are in fact valued in _non-empty_ subsets - hypermagmas with this property are sometimes called _hypergroupoids_.

But note that $\emptyset$ together with the empty map is nevertheless a hypergroup, in fact, the initial hypergroup in the obvious _category of hypergroups_ $\mathbf{HypGrp}$.

By imposing commutativity one arrives at the notion of a [[canonical hypergroup]] that enters into the definition of a [[hyperring]].

Hypergroups whose hyperlaw is valued in singleton subsets correspond to groups.

## Example

Let $G$ be a compact [[Lie group]] and $\hat{G}$ the set of its irreducible representations. Given $a,b\in\hat{G}$ define $a\cdot b$ as the set of irreducible representations $\mu_1,\dots,\mu_k$ occurring in the decomposition $a\otimes b=\Sum m_i \mu_i$. This endows $\hat{G}$ with the structure of a hypergroup. (For further details and the connection to operator algebra see [Litvinov (2011)](#Lit11)).

## Related entries

* [[magma]]

* [[hypermonoid]]

* [[hypergroup]]

* [[hyperring]]

* [[hypergraph]]

* [[multivalued group]]

* [[historical notes on quasigroups]]

## Reference

See also references at [[hypergroup]].

* S. D. Comer, _Polygroups derived from cogroups_ , J. Algebra **89** no.2 (1984) 397--405 <a href="https://doi.org/10.1016/0021-8693(84)90225-4">doi</a> 

* P. Corsini, V. Leoreanu-Fotea, _Applications of yhperstructure theory_ , Kluwer Dordrecht
2003.

* {#HS90}L. Haddad, Y. Sureau, _Les cogroupes et la construction de Utumi_ , Pacific J. Math. **145** no.1 (1990) 17--58. ([abstract](http://projecteuclid.org/euclid.pjm/1102645606))

* L. Haddad, Y. Sureau, _Les groupes, les hypergroupes et l'&#233;nigme des Murngin_ , JPAA **87** (1993) pp.221-235.

* Louis H. Rowen, _Residue structures_, [arXiv:2403.09467](https://arxiv.org/pdf/2403.09467)

category: algebra