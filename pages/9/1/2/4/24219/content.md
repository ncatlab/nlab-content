+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The loop space of a [[pointed type]] is simply the type of [[identifications]] from a term to itself i.e. loops.

## Definition ##

Given a pointed type $(A,\star_A)$ the loop space type is the type $\Omega(A,\star_A)\equiv \star_{A} =_{A} \star_{A}$ and has basepoint $refl_{\star A}$.

The $n$-fold **iterated loop space** $\Omega^n(A,\star_A)$ can be defined by induction on $n$:
 * $\Omega^0(A,\star_A)=(A,\star_A)$
 * $\Omega^{n+1}(A,\star_A)=\Omega^n(\Omega(A,\star_A))$

[[the HoTT book|The HoTT book]] defines a 'loop space' in definitions 2.1.7 and 2.1.8:

> **Definition 2.1.7** A **pointed type** $(A,a)$ is a type $A\,:\,\mathcal{U}$ together with a point $a\,:\,A$, called its **basepoint**. We write $\mathcal{U}_\bullet :\equiv \sum_{(A:\mathcal{U})}A$ for the type of pointed types in the universe $\mathcal{U}$.

> **Definition 2.1.8** Given a pointed type $(A,a)$, we define the **loop space** of $(A,a)$ to be the following pointed type:

> $\Omega(A,a) = ((a =_A a),\,refl_a)$.

> An element of it will be called a **loop** at $a$. For $n\,:\,\mathbb{N}$, the _n-fold_ **iterated loop space** $\Omega^n(A,a)$ of a pointed type $(A,a)$ is defined recursively by:

> $\Omega^0(A,a) = (A,a)$  
> $\Omega^{n+1}(A,a) = \Omega^n(\Omega(A,a))$.

> An element of it will be called an _n-loop_ or an _n-dimensional_ **loop** at $a$.

## Related entries

* [[pointed type]]

* [[identity type]]

## References

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects loop space types]]