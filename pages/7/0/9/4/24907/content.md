
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Overview

Simply sorted set theory is a [[set theory]] which is a [[first order theory]] without [[dependent type|dependent]] [[sorts]]; i.e. written in [[first order logic]] and whose [[domains of discourse]] (called [[sorts]] here) do not on other domains of discourse. In addition, membership $a \in A$ is a [[relation]], rather than a [[judgment]] as in [[dependently sorted set theory]]. Simply sorted set theories come in both [[material set theories]] and [[structural set theories]]. 

Simply sorted set theory could be distinguished between how many sorts the theory has; these include

* one-sorted set theory, which include certain presentations of [[ZFC]], [[Mostowski set theory]], [[fully formal ETCS]], and [[ZFA]]
* [[two-sorted set theory]], which include certain presentations of [[ETCS]] and [[ZFA]], 
* [[three-sorted set theory]], which include [[three-sorted SEAR]], [[three-sorted structural ZFC]] as well as certain presentations of [[ETCS with elements]]. 
* four-sorted set theory, which include certain presentations of [[SEPS]]. 

## Notions of sets and elements

\begin{definition}
A notion of set and element in a simply sorted first-order theory consists of:

* A sort $S$ of probable sets. By probable set, we mean that certain terms of $S$ are to be considered as the sets in the theory. 

* A sort $E$ of probable elements. By probable element, we mean that certain terms of $E$ are to be considered as the elements in the theory. 

* A binary predicate in $S$, $(-)=_S(-)$, called *[[definitional equality]] of sets*

* A binary predicate in $E$, $(-)=_E(-)$, called *[[equality]] of elements*

* A unary predicate in $S$, $\mathrm{set}(-)$, called *being a set*

* A unary predicate in $E$, $\mathrm{element}(-)$, called *being an element*

* A binary predicate in $E$ on the left and $S$ on the right, $(-)\in(-)$, called *membership*

such that 

* $(-)=_E(-)$ is an [[equivalence relation]]

* if $a \in b$, then $a$ is an element and $b$ is a set

$$\forall a:E.\forall b:S.(a \in b) \to \mathrm{element}(a) \wedge \mathrm{set}(b)$$

* weak extensionality for sets and elements: for all $a:S$ and for all $b:S$, if a and b are sets, then $a =_S b$ if and only if, for all $c:E$, if $c$ is an element, then $c \in a$ if and only if $c \in b$

$$\forall a:S.\forall b:S.(\mathrm{set}(a) \wedge \mathrm{set}(b)) \implies ((a =_S b) \iff \forall c:E.(\mathrm{element}(c) \implies ((c \in a) \iff (c \in b))))$$
\end{definition}

In one-sorted set theory, the sorts $E$ and $S$ are the same sort. 

## See also

* [[unsorted set theory]], [[simply sorted set theory]], [[dependently sorted set theory]]
* [[material set theory]], [[structural set theory]]

[[!redirects simply sorted set theory]]
[[!redirects simply sorted set theories]]

[[!redirects simply-sorted set theory]]
[[!redirects simply-sorted set theories]]
