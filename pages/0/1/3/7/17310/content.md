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
[[!redirects comagma]]


## Idea

A **hypermagma** $X$ relates to a [[magma]] like a [[hypergraph]] relates to an ordinary [[graph]] i. e. the binary operation on $X$ takes value in $2^X$ instead of $X$. By imposing further axioms one obtains the concept of a **hypergroup** corresponding to the generalization of the [[group|group concept]] in this context.

## Definition

A set $X$ together with a function $X\times X\to 2^X$ is called a _hypermagma_. The function is normally denoted by $\dot$ and called the _hyperlaw_ or _hyperproduct_ of $X$. A _morphism of hypermagmas_ from $X$ to $Y$ is a function $f:X\to Y$ such that $f(x\dot y)\subset f(x)\dot f(y)$ for all $x,y\in X$. The morphism is called _good_ if $f(x\dot y) = f(x)\dot f(y)$.

## Related entries

* [[magma]]

* [[hypergraph]]

* [[historical notes on quasigroups]]

## Reference

* S. D. Comer, _Polygroups derived from cogroups_ , J. Algebra **89** no.2 (1984) pp.397-405. 

* L. Haddad, Y. Sureau, _Les cogroupes et la construction de Utumi_ , Pacific J. Math. **145** no.1 (1990) pp.17-58. ([abstract](http://projecteuclid.org/euclid.pjm/1102645606))

* L. Haddad, Y. Sureau, _Les groupes, les hypergroupes et l'&#233;nigme des Murngin_ , JPAA **87** (1993) pp.221-235.

