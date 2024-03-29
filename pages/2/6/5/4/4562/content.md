\tableofcontents

## Definition

Given any [[set]] $S$, a __[[family]] of [[subsets]]__ of $S$ consists of an index set $I$ and and a [[function]] from $I$ to the [[power set]] of $S$.  This is actually nothing special; this is the normal meaning of 'family' when taking a family of things that form a set: a family of foos is any function to the set of foos.

However, in [[predicative mathematics]], we do not accept that the subsets of $S$ form a set; that is, we believe that the power set $\mathcal{P}S$ is really a [[proper class]].  So on the face of it, a family of subsets would also be a large thing.  However, there is an alternative definition that is not only appropriate predicatively but also often provides a useful perspective in any case:  A __family of subsets__ of $S$ consists of an index set $I$ and a [[binary relation]] $\in$ between elements of $S$ and elements of $I$.

Note that we may have $x \in A \Longleftrightarrow x \in B$ for all $x$ without having $A = B$; this is because (as in any family) two different indices may index the same subset.  However, many of the operations performed on families of subsets, such as [[intersection]] and [[union]], depend only on the [[image]] of the function $I \to \mathcal{P}S$.  So it is common to assume that a family of subsets of $S$ is simply a [[subset]] of $\mathcal{P}S$.  (Besides this, not all authors agree with this page on even the *general* meaning of the word 'family'.)

## See also

* [[family of sets]]
* [[union]]

[[!redirects family of subsets]]
[[!redirects families of subsets]]

[[!redirects indexed subset]]
[[!redirects indexed subsets]]