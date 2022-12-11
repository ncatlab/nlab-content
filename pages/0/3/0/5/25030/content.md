
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[material set theory]], [[sets]] and [[elements]] are the same thing, so unordered pairs and pair sets are the same thing. However, in other foundations of mathematics, sets and elements are not the same thing, so an unordered pair is an element, while a **pair set** is a set. 

## Definition

### In material set theory

If $A$ is a [[set]] and $x$ and $y$ are [[elements]] of $A$, then the __pair set__ $\{x,y\}$ is a subset of $A$ such that for all elements for which $z \in \{x,y\}$ holds, $z = x$ or $z = y$. In material set theory, these are also called [[unordered pairs]]. 

In [[material set theory]], we may apply this when $x$ and $y$ are not previously given as elements of any set $A$.  In that case, the existence of the unordered pair is given by the [[axiom of pairing]].

### In structural set theory

If $A$ is a [[set]] and $x$ and $y$ are [[elements]] of $A$, then the __pair set__ $\{x,y\}$ is a subset of $A$ with injection $i:\{x,y\} \hookrightarrow A$ such that for all elements $z \in \{x,y\}$, $i(z) = x$ or $i(z) = y$, and for all other sets $B$ with injection $j:B \hookrightarrow A$ such that for all elements $w \in B$, $i(w) = x$ or $i(w) = y$, there is an injection $k:B \hookrightarrow \{x,y\}$ such that for all elements $w \in B$, $i(k(w)) = j(w)$. 

## Properties

The pair set $\{x,x\} = \{x\}$ is a [[singleton]].

## See also

* [[unordered pair]]

* [[axiom of pairing]]

[[!redirects pair set]]
[[!redirects pair sets]]
[[!redirects pair subset]]
[[!redirects pair subsets]]