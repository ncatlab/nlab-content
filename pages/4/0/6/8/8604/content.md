
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
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

In [[type theory]] a _type formation rule_ is a [[natural deduction]] step roughly of the form

$$
  \frac{
    \vdash\; A \colon Type \;\;\; \vdash \;B \colon Type \;\;\; \cdots 
  }{
    \vdash \; F(A,B,\cdots) \colon Type
  }
$$

which says that given [[types]] $A, B, \cdots $, there is a new type $F(A,B, \cdots)$. 

For instance for [[product types]] it says that

$$
  \frac{\vdash \; A \colon Type \;\;\; \vdash \; B \colon Type}{\vdash \; A \times B \colon Type}
  \,.
$$

In [[natural deduction]] the type formation rule for a kind of type is the first in a quadruple of rules that come with every kind of type:

1. **type formation rule**

1. [[term introduction rule]]

1. [[term elimination rule]]

1. [[computation rule]]

## Properties

### Relation to category theory

Under the [[relation between type theory and category theory]], the [[categorical semantics]] of type formation essentially corresponds to certain [[universal constructions]] in [[category theory]].

## References

Introductory textbook account:

* [[Simon Thompson]], §4.2  4.3 in: *[[Type Theory and Functional Programming]]*, Addison-Wesley (1991) &lbrack;ISBN:0-201-41667-0, [webpage](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP), [pdf](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP/ttfp.pdf)&rbrack;



[[!redirects type formation]]
[[!redirects type formations]]

[[!redirects type former]]
[[!redirects type formers]]
[[!redirects type formation rule]]
[[!redirects type formation rules]]

[[!redirects type forming]]
[[!redirects type forming operation]]
[[!redirects type forming operations]]

[[!redirects type-forming]]
[[!redirects type-forming operation]]
[[!redirects type-forming operations]]


[[!redirects formation rule]]
[[!redirects formation rules]]

