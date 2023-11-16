+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}


## Definition

Let $A: H\to H$  be an [[unbounded operator]] on a [[Hilbert space]] $H$. An unbounded operator $A^*$ is its __[[adjoint operator|adjoint]]__ if

* $(A x|y) = (x|A^*y)$ for all $x\in dom(A)$ and $y\in dom(A^*)$; and

* every $B$ satisfying the above property for $A^*$ is a restriction of $A$.

On [[finite-dimensional Hilbert spaces]], adjoint operators always exists, in [[matrix]]-components with respect to any [[orthonormal linear basis]] given by passage to the [[complex conjugation|complex conjugate]] [[transpose matrix]].

On infinite-dimensional Hilbert spaces an adjoint operator does not need to exist, in general. 

## History
 {#History}

Recounted by [MacLane 1988](#MacLane88), [p. 330](http://www.ams.org/publicoutreach/math-history/hmath1-maclane25.pdf#page=8):

> Two of [[John von Neumann|von Neummann]]'s papers on this topic &lbrack;[[Hilbert spaces]]&rbrack; had been accepted in the Mathematische Annalen, a journal of Springer Verlag. [[Marshall Stone]] had seen the manuscripts, and urged von Neumann to observe that his treatment of linear operators $T$ on a Hilbert space could be much more effective if he were to use the notion of an adjoing $T^ast$ to the linear transformation $T$ --- one for which the now familiar equation

> $\;\;\;\;\; \langle T a, b \rangle \;=\; \langle a, T^\ast b \rangle$

> would hold for all suitable $a$ and $b$. Von Neumann saw the point immediately, as was his wont, and wishes to withdraw the papers before publication. They were already set up in type; Springer finally agreed to cancel them on the condition that von Neumann write for them a book on the subject --- which he soon did &lbrack;[1932](#vonNeumann1932)&rbrack;.

> This story (told to me by [[Marshall Stone]]) illustrates the important conceptual advance represented by the definition of adjoint operators. &lbrack...&rbrack; I have written elsewhere &lbrack;[1970](#MacLane70)&rbrack; that it is a step toward the subsequent description of a [[functor]] $G$ [[right adjoint]] to a functor $F$, in terms of [a natural isomorphism](adjoint+functor#InTermsOfHomIsomorphism)

> $\;\;\;\;\; hom(F a, b) \;\simeq\; hom(a, G b)$

> between [[hom-sets]] in suitable [[categories]].

(Cf. discussion at [adjoint functor -- idea](adjoint+functor#Idea).)

## Related concepts

* [[self-adjoint operator]]

## References

The notion of adjoint operators is originally due to [[Marshall Stone]], see also the history section [above](#History), as recounted in

* {#MacLane70} [[Saunders MacLane]], *The Influence of M. H. Stone on the Origins of Category Theory*, in *Functional Analysis and Related Fields*, Springer (1970) &lbrack;[doi:10.1007/978-3-642-48272-4_12](https://doi.org/10.1007/978-3-642-48272-4_12)&rbrack;

* {#MacLane88} [[Saunders Mac Lane]]: §5 in: *Concepts and Categories in Perspective*, in: P. Duren, *A century of mathematics in America* Part 1, AMS (1988) 323-365. &lbrack;[pdf](http://www.ams.org/samplings/math-history/hmath1-maclane25.pdf), [ISBN:0-8218-0124-4](https://www.ams.org/publicoutreach/math-history/hmath1-index)&rbrack; 


Original discussion in print is due to:

* {#vonNeumann1932} [[John von Neumann]]: 

  *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;


Lecture notes:

* [[Bergfinnur Durhuus]], *Operators on Hilbert Space* &lbrack;[pdf](https://web.math.ku.dk/~durhuus/MatFys/MatFys4.pdf), [[Durhuus-OperatorsOnHilbertSpace.pdf:file]]&rbrack;




[[!redirects adjoint operators]]
