
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **fork** is a [[diagram]] of the form

$$
A\underset{\quad e \quad}{\to}B\underoverset{\quad g \quad}{f}{\rightrightarrows}C
$$

such that $f e=g e$. An example of a special type of a fork is an [[equalizer]]. Another example is a _reflexive fork_, where $C = A$ and $f e = 1_A$. 

Note that, technically speaking, the diagram above may not commute, since $f$ and $g$ themselves are not necessarily equal. 
(But some authors, especially when talking about [[equalizers]], loosely use the term "[[commutative diagram]]" even in this case.)

A dual notion is also called a **cofork**, although some references do not distinguish forks and coforks. 

## Related concepts

* [[parallel pair]]
* [[monadicity theorem]]

[[!redirects fork]]
[[!redirects forks]]
[[!redirects cofork]]
[[!redirects coforks]] 
[[!redirects reflexive fork]] 
[[!redirects reflexive forks]] 
