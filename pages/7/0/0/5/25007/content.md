
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### (0,1)-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A notion of [[ordered ring]] for [[strict orders]] which are not necessarily [[connected relation|connected]]. 

## Definition

A strictly ordered ring is an [[ring]] $R$ with a [[strict order]] $\lt$ such that 

* $0 \lt 1$

* for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a + b$

* for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a \cdot b$

## Properties

Every strictly ordered ring is a [[preordered ring]] given by the [[negation]] of the strict order. In the presence of [[excluded middle]], every strictly ordered ring is a [[total order|totally preordered]] ring. 

## Examples

* Every [[pseudo-ordered ring]] is a strictly ordered ring. 

* Every [[ordered local ring]] is a strictly ordered ring where every element greater than zero or less than zero is invertible.

* Every [[ordered Kock field]] is a example of a strictly ordered ring which in the presence of [[excluded middle]] is a [[linearly ordered ring]]. 

## See also

* [[ordered local ring]]

* [[ordered Kock field]]

[[!redirects strictly ordered ring]]
[[!redirects strictly ordered rings]]