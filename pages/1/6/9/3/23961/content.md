
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A version of [[cancellative monoid|cancellative]] [[magmas]] where the binary function is not required to be either valued in the same domain set as the codomain set, this allows the concept to be generalised from [[magmas]] and [[monoids]] to other binary functions such as [[actions]] and [[modules]]. 

## Definition

Given sets $A$, $B$, and $C$, a binary function $f:A \times B \to C$ is **left cancellative** if for all $c \in B$ and $d \in B$, if $a \cdot c = a \cdot d$ for all $a \in A$, then $c = d$, and it is **right cancellative** if for all $a \in A$ and $b \in A$, if $a \cdot c = b \cdot c$ for all $c \in A$, then $a = b$. It is **cancellative** if it is both left cancellative and right cancellative. 

## See also

* [[cancellative monoid]]
* [[torsion-free module]]
* [[integral domain]]

[[!redirects cancellative binary functions]]