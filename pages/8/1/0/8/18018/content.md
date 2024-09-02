
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

The [[lower central series]] or [[descending central series]] of a Lie algebra $\mathfrak{g}$ is a sequence of nested ideals $\mathfrak{g}^{k+1} \trianglelefteq \mathfrak{g}^{k}$ defined inductively by $\mathfrak{g}^1 \coloneqq \mathfrak{g}$,  $\mathfrak{g}^{k+1} \coloneqq [\mathfrak{g}, \mathfrak{g}^k]$. The Lie algebra is said to be **nilpotent** if $\mathfrak{g}^{k} = 0$ for some $k \in \mathbb{N}$.

In other words, a Lie algebra $\mathfrak{g}$ is nilpotent if and only the improper ideal $\mathfrak{g}$ is a [[nilpotent element]] in the ideal lattice with respect to the ideal product $[-,-]$.

## Examples

* Trivially: Every abelian Lie algebra is nilpotent. 

* The Lie algebra of even-degree elements of the [[tensor product]] of a [[super translation Lie algebra]] ([[super Minkowski Lie algebra]]) with a [[superpoint]] $\mathbb{R}^{0\vert q}$ is nilpotent.

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

* [[Victor Kac]] (notes by Marc Doss), *Nilpotent and Solvable Lie algebras* (2010) &lbrack;[pdf](https://math.mit.edu/classes/18.745/Notes/Lecture_4_Notes.pdf), [[KacDoss-NilpotentLieAlebras.pdf:file]]&rbrack;

* _Nilpotent Lie algebras_ &lbrack;[[Perrin-NilpotentLieAlgebras.pdf:file]]&rbrack;

* Wikipedia, _[Nilpotent Lie algebra](https://en.wikipedia.org/wiki/Nilpotent_Lie_algebra)_

* [GroupProps](https://groupprops.subwiki.org/wiki/Main_Page): *[Lie correspondence between nilpotent Lie algebras and unipotent algebraic groups](https://groupprops.subwiki.org/wiki/Lie_correspondence_between_nilpotent_Lie_algebras_and_unipotent_algebraic_groups)*

On the [[Sullivan models]] which are [[Chevalley-Eilenberg algebra]] of nilpotent Lie algebras:

* [[Manuel Amann]], pp. 4 of: *On quasi-isometric nilpotent Lie groups* &lbrack;[arXiv:1710.04542](https://arxiv.org/abs/1710.04542)&rbrack;


[[!redirects ad-nilpotent Lie algebra]]
[[!redirects ad-nilpotent Lie algebras]]
[[!redirects nilpotent Lie algebra]]
[[!redirects nilpotent Lie algebras]]

[[!redirects ad-nilpotent Lie algebra]]

