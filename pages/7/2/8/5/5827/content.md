
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Bilinear forms
* table of contents
{: toc}

## Definitions

A __bilinear form__ is simply a [[linear map]] $\langle -,-\rangle\colon V \otimes V \to k$ out of a [[tensor product]] of $k$-[[module|modules]] into the [[ring]] $k$ (typically taken to be a [[field]]).

It is called __symmetric__ if $\langle x,y\rangle = \langle y,x\rangle$ for all $x,y \in V$. For variants on this, such as the property of being _conjugate-symmetric_, see [[inner product space]].

It is called __antisymmetric__ or __skew-symmetric__ if $\langle x,y\rangle = -\langle y,x\rangle$ for all $x,y \in V$.

It is called __alternating__ if $\langle x,x\rangle = 0$ for all $x \in V$.

It is called __nondegenerate__ if the [[mate]] $V \to V^\ast = \hom(V, k)$ is injective (a [[monomorphism]]). 

Let $k = \mathbb{R}$ be the [[real numbers]]. A symmetric bilinear form is called

* [[positive definite]] if $\langle x,x\rangle \gt 0$ if $x \neq 0$.

* [[negative definite]] if $\langle x,x\rangle \lt 0$ if $x \neq 0$.

## Examples

\begin{example}\label{InnerProductOnRealVectorSpace}
An _[[inner product]]_ on a [[real vector space]] (not though generally on [[complex vector spaces]], see Rem. \ref{BewareInnerProductsOnComplexVectorSpaces}) is an example of a symmetric bilinear form. (For some authors, an inner product on a real vector space is precisely a positive definite symmetric bilinear form. Other authors relax the positive definiteness to nondegeneracy. Perhaps some authors even drop the nondegeneracy condition (citation?).)
\end{example}
\begin{remark}\label{BewareInnerProductsOnComplexVectorSpaces}
In contrast to Exp. \ref{InnerProductOnRealVectorSpace}, beware that an [[inner product]] on a [[complex vector space]] is typically *not* taken to be a bilinear form, but a *[[sesquilinear form]]* (called a *[[Hermitian form]]* if positive definite). 
\end{remark}

\begin{example}
If $f \colon \mathbb{R}^n \to \mathbb{R}$ is a [[differentiable function]] of class $C^2$, then the [[Hessian]] of $f$ at a point defines a symmetric bilinear form. It may be degenerate, but in [[Morse theory]], a [[Morse function]] is a $C^2$ function such that the Hessian at each critical point is nondegenerate. 
\end{example}

## Categorification and $n$POV
 {#CategorificationsAndnPOV}

Concepts which relate to (non-degenerate) bilinear forms from the [[nPOV]] and/or [[categorification|categorifications]] of the concept of bilinear forms  include

* [[2-Hilbert space]]

* [[Calabi-Yau object]], [[Calabi-Yau A-infinity category]]

## Generalizations

### From Ab to monoidal categories

This concept could be generalized from the [[category of abelian groups]] to any [[monoidal category]]:

Let $(C, I, \otimes)$ be a [[monoidal category]], let $(k, 1, \pi)$ be a [[monoid object]] in $C$, and let $(V, \rho)$ be a $k$-[[module object]] in $C$. $k$ itself is a $k$-module object with the [[action]] being represented by the [[monoid]] [[binary operation]] $\pi$. A bilinear form is simply an [[action]]-preserving [[morphism]] $f:V \otimes V \to k$ from the [[tensor product]] $V \otimes V$ to $k$: given morphisms $a:I \to k$, $v:I \to V$, and $w:I \to V$, 

$$f \circ ((\rho \circ (a \otimes v)) \otimes w) = \pi \circ (a \otimes (f \circ (v \otimes w))$$

and 

$$f \circ (v \otimes (\rho \circ (a \otimes w))) = \pi \circ (a \otimes (f \circ (v \otimes w))$$

However, if $C$ is not a [[Ab-enriched category]], then the morphisms of the category are not linear and it would probably be better to call these morphisms *binary forms* or something similar. 

Symmetric bilinear forms can similarly be generalized from the [[category of abelian groups]] to any [[monoidal category]], where for all morphisms $v:I \to V$ and $w:I \to V$, we have $f \circ (v \otimes w) = f \circ (w \otimes v)$. 

### From Mod to monoidal categories

This concept could be generalized from the [[category of modules]] to any [[monoidal category]], since the ground ring $k$ is the [[tensor unit]] of the category of $k$-modules:

Let $(C, I, \otimes)$ be a [[monoidal category]]. Given an object $V$, every morphism $I \otimes V \to V$ is given by the composition of an [[endomorphism]] $V \to V$ with the [[left unitor]] $\lambda_V:I \otimes V \to V$. Then given an object $V \in C$, a bilinear form is just a morphism $f:V \otimes V \to I$. However, if $C$ is not a [[Ab-enriched category]], then the morphisms of the category are not linear and it would probably be better to call these morphisms *binary forms* or something similar. In [[cartesian monoidal categories]] $(C, 1, \times)$, the binary forms $V \times V \to 1$ always exist and is unique, by the universal property of the [[terminal object]]. 

Symmetric bilinear forms can similarly be generalized from the [[category of modules]] to any [[monoidal category]], where for all morphisms $v:I \to V$ and $w:I \to V$, we have $f \circ (v \otimes w) = f \circ (w \otimes v)$. 


## Related concepts

* [[quadratic form]], [[polarization identity]]

* [[sesquilinear form]]

* [[symplectic form]], [[Kähler form]], [[Hermitian form]]

* [[Hermitian K-theory]]

* [[characteristic element of a bilinear form]]

* [[hyperbolic functor]]

* [[Riemannian metric]]

* [[Pythagorean theorem]]

* [[Cauchy–Schwarz inequality]]

* [[Bochner's theorem]]

## References

* [[John Milnor]], [[Dale Husemöller]], *Symmetric Bilinear Forms*,  Ergebnisse der Mathematik und ihrer Grenzgebiete **73**, Springer (1973) &lbrack;[doi:10.1007/978-3-642-88330-9](https://doi.org/10.1007/978-3-642-88330-9)&rbrack;

* [[Richard Elman]], [[Nikita Karpenko]], [[Alexander Merkurjev]], *Algebraic and Geometric Theory of Quadratic Forms*, Colloquium Publication **56**, AMS (2008) &lbrack;[ams:coll-56](https://bookstore.ams.org/coll-56), [pdf](https://www.math.ucla.edu/~rse/old_book/Kniga.pdf)&rbrack;

* [[Igor R. Shafarevich]], [[Alexey O. Remizov]]: §6 in: *Linear Algebra and Geometry* (2012) &lbrack;[doi:10.1007/978-3-642-30994-6](https://doi.org/10.1007/978-3-642-30994-6), [MAA-review](https://maa.org/press/maa-reviews/linear-algebra-and-geometry)&rbrack; 


Lecture notes:

* [[Keith Conrad]], *Bilinear forms* &lbrack;[pdf](https://kconrad.math.uconn.edu/blurbs/linmultialg/bilinearform.pdf), [[Conrad-BilinearForms.pdf:file]]&rbrack;

[[!redirects bilinear form]]
[[!redirects bilinear forms]]

[[!redirects positive definite bilinear form]]
[[!redirects positive definite bilinear forms]]

[[!redirects positive semi-definite bilinear form]]
[[!redirects positive semi-definite bilinear forms]]

[[!redirects indefinite bilinear form]]
[[!redirects indefinite bilinear forms]]

[[!redirects symmetric bilinear form]]
[[!redirects symmetric bilinear forms]]

[[!redirects antisymmetric bilinear form]]
[[!redirects antisymmetric bilinear forms]]

[[!redirects skew-symmetric bilinear form]]
[[!redirects skew-symmetric bilinear forms]]

[[!redirects alternating bilinear form]]
[[!redirects alternating bilinear forms]]