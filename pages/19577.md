
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given an [[object]] in [[algebra]] $A$ (such as an [[associative algebra]], a [[group]] or a [[Lie algebra]], etc.) then an [[algebraic extension|extension]] $\widehat A \overset{p}{\longrightarrow} A$ (e.g. a [[group extension]] or [[Lie algebra extension]] etc.) is called a _central extension_ if its [[kernel]] 

\[
  \label{ExtensionShortExactSequence}
  1 \to ker(p) \overset{\phantom{A}\iota\phantom{A}}{\hookrightarrow} \widehat A \overset{\phantom{A}p\phantom{A}}{\longrightarrow} A
  \to 1
\]

is in the [[center]] $C(\widehat{A})$ of $\widehat A$

$$
  ker(p) \subset C(\widehat{A})
  \,.
$$

This means in particular that $ker(p)$ is "commutative" (e.g. a [[commutative algebra]] or [[abelian group]] or [[Lie algebra]] with vanishing [[Lie bracket]] etc.), but it means in addition that the elements of $ker(p)$ commute not just among themselves, but also with all other elements of $\widehat A$.


Typically central extensions by some commutative algebraic object $ker(p)$ are classified by the suitable degree-2 [[cohomology group]] $H^2(A,ker(p))$ of $A$ with [[coefficients]] in $ker(p)$. In fact, typically there is an embedding of the situation into [[homotopical algebra]]/[[higher algebra]] such that this [[cohomology group]] is given by the [[homotopy classes]] of morphisms to a second [[delooping]] object $B ker(p)$ (in the context of [[groups]]: the [[delooping]] [[2-group]])

$$
  H^2(A,ker(p)) 
  \;\simeq\;
  \left\{
    A \overset{\phi}{\longrightarrow} B ker(p)
  \right\}_{/homotopy}
$$

and under this identification the central extension is the [[homotopy fiber]] of the [[cocycle]] $\phi$ and the [[short exact sequence]] (eq:ExtensionShortExactSequence) is part of the [[long homotopy fiber sequence]] to the left induced by $\phi$:

$$
  \array{
    ker(p) &\overset{\iota}{\longrightarrow}& \widehat{A}
    \\
    && \Big\downarrow
    \\
    && A &\overset{ \phantom{AA}\phi\phantom{AA} }{\longrightarrow}& B ker(p)
  }
$$

## Examples

* A [[Poisson bracket]] Lie algebra is a central [[extension of Lie algebras]] of a Lie algebra of [[Hamiltonian vector fields]], 

* the corresponding [[quantomorphism group]] is a central [[extension of groups]] of the [[diffeological group]] of [[Hamiltonian symplectomorphism]].

* A [[Heisenberg group]] is a sub-central extension such a [[quantomorphism group]]-extension, over [[Hamiltonian symplectomorphisms]] on a [[Lie group]] that [[action|act]] by left multiplication. 

* A [[spin group]] is a central extension of a [[special orthogonal group]] by the [[group of order 2]] $\mathbb{Z}/2$.

* ...

## Related concepts

* [[universal central extension]], [[maximal central extension]]

* [[higher central extension]]

* [[universal higher central extension]]

* [[nilpotent group]]

## References

See also 

* Wikipedia, _[Central extension](https://en.wikipedia.org/wiki/Group_extension#Central_extension)_

Discussion of application in [[physics]]:

* G. M. Tuynman, W. A. Wiegenbrinck, _Central extensions and physics_, J. Geom. Physics 4:2(1987), 207–258.(<a href="https://doi.org/10.1016/0393-0440(87)90027-1">doi:10.1016/0393-0440(87)90027-1</a>)




[[!redirects central extensions]]