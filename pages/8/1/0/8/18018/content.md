
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A [[Lie algebra]] is **nilpotent** if repeatedly [[adjoint action|acting]] via the [[Lie bracket]] on any one of its elements with other elements eventually yields [[zero]].

## Definition

The *[[lower central series]]* or (descending [[central series]]) of a Lie algebra $\mathfrak{g}$ is a sequence of nested [[ideals]] $\mathfrak{g}^{k+1} \trianglelefteq \mathfrak{g}^{k}$ defined inductively by $\mathfrak{g}^1 \coloneqq \mathfrak{g}$,  $\mathfrak{g}^{k+1} \coloneqq [\mathfrak{g}, \mathfrak{g}^k]$. The Lie algebra is said to be **nilpotent** if $\mathfrak{g}^{k} = 0$ for some $k \in \mathbb{N}$.

In other words, a Lie algebra $\mathfrak{g}$ is nilpotent if and only the improper ideal $\mathfrak{g}$ is a [[nilpotent element]] in the ideal lattice with respect to the ideal product $[-,-]$.


## Examples

* Trivially: Every abelian Lie algebra is nilpotent. 

* The Lie algebra of even-degree elements of the [[tensor product]] of a [[super translation Lie algebra]] ([[super Minkowski spacetime|super Minkowski]] [[super Lie algebra]]) with a [[superpoint]] $\mathbb{R}^{0\vert q}$ is nilpotent.

## Properties

* Every nilpotent Lie algebra is [[solvable Lie algebra|solvable]].


### Relation to Sullivan models

A finite-dimensional Lie algebra $\mathfrak{g}$ is nilpotent precisely if its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ is a [[Sullivan algebra]] (necessarily minimal). See also at _[[rational homotopy theory]]_ for more on this.

## Related concepts

* [[nilpotent element]]

* [[nilpotent group]]

* [[nilpotent topological space]]

* [[nilpotent L-infinity algebra]]


## References

* {#Serre64} [[Jean-Pierre Serre]]: *Nilpotent and Solvable Lie Algebras*, Chapter V in: *Lie Algebras and Lie Groups -- 1964 Lectures given at Harvard University*, Lecture Notes in Mathematics **1500**, Springer (1992) &lbrack;[doi:10.1007/978-3-540-70634-2](https://doi.org/10.1007/978-3-540-70634-2)&rbrack;

* Arthur A. Sagle, Ralph E. Walde: *Nilpotent Lie Groups and Algebras*, Chapter 11 in: *Introduction to Lie Groups and Lie Algebras*, Pure and Applied Mathematics **51**, Elsevier (1973) 215-227 \[<a href="https://doi.org/10.1016/S0079-8169(08)61671-2">doi:10.1016/S0079-8169(08)61671-2</a>\]

* {#Milne17} [[James Milne]], pp. 260 in: *Algebraic Groups -- The theory of group schemes of finite type over a field*, Cambridge University Press (2017)  &lbrack;[doi:10.1017/9781316711736](https://doi.org/10.1017/9781316711736), [webpage](http://www.jmilne.org/math/Books/iag.html), [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf)&rbrack;


* Laurence Corwin, Frederick P. Greenleaf: Section 1.2 of: *Representations of Nilpotent Lie Groups and their Applications -- Volume 1  Part 1. Basic Theory and Examples*, Cambridge University Press (2004) &lbrack;[ISBN:9780521604956](https://www.cambridge.org/us/universitypress/subjects/mathematics/abstract-analysis/representations-nilpotent-lie-groups-and-their-applications-volume-1-part-1)&rbrack;

* [[Victor Kac]] (notes by Marc Doss), *Nilpotent and Solvable Lie algebras* (2010) &lbrack;[pdf](https://math.mit.edu/classes/18.745/Notes/Lecture_4_Notes.pdf), [[KacDoss-NilpotentLieAlebras.pdf:file]]&rbrack;

* [[Daniel Huybrechts]]: *Nilpotent Lie Algebras*, Section 1 of *Stability Structures on Lie Algebras, after Kontsevich and Soibelman* (2011) &lbrack;[pdf](https://www.math.uni-bonn.de/people/huybrech/KS.pdf), [[Huybrechts-StabilityStructures.pdf:file]]&rbrack;

* Veronique Fischer, Michael Ruzhansky, Section 1.6 in: *Quantization on Nilpotent Lie Groups*, Birkh&auml;user (2016) &lbrack;[doi:10.1007/978-3-319-29558-9](https://doi.org/10.1007/978-3-319-29558-9)&rbrack;

* _Nilpotent Lie algebras_ &lbrack;[[Perrin-NilpotentLieAlgebras.pdf:file]]&rbrack;

* Wikipedia, _[Nilpotent Lie algebra](https://en.wikipedia.org/wiki/Nilpotent_Lie_algebra)_

* [GroupProps](https://groupprops.subwiki.org/wiki/Main_Page): *[Lie correspondence between nilpotent Lie algebras and unipotent algebraic groups](https://groupprops.subwiki.org/wiki/Lie_correspondence_between_nilpotent_Lie_algebras_and_unipotent_algebraic_groups)*

On the [[Sullivan models]] which are [[Chevalley-Eilenberg algebra]] of nilpotent Lie algebras:

* [[Manuel Amann]], pp. 4 of: *On quasi-isometric nilpotent Lie groups* &lbrack;[arXiv:1710.04542](https://arxiv.org/abs/1710.04542)&rbrack;

On nilpotent [[super Lie algebras]]:

* [[Manfred Scheunert]], §III.2 in: *The theory of Lie superalgebras. An introduction*, Lect. Notes Math. **716** (1979) &lbrack;[doi:10.1007/BFb0070929](https://doi.org/10.1007/BFb0070929)&rbrack;

* Luc Frappat, Antonio Sciarrino, Paul Sorba: §26 in: _Dictionary on Lie Superalgebras_, Academic Press (2000) &lbrack;[arXiv:hep-th/9607161](http://arxiv.org/abs/hep-th/9607161), ISBN:978-0122653407&rbrack;

[[!redirects ad-nilpotent Lie algebra]]
[[!redirects ad-nilpotent Lie algebras]]
[[!redirects nilpotent Lie algebra]]
[[!redirects nilpotent Lie algebras]]

[[!redirects ad-nilpotent Lie algebra]]

