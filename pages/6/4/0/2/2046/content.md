
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}


## Definition


+-- {: .num_defn}
###### Definition

An [[object]] $X$ in a [[category]] $C$ with a [[terminal object]] $1$ is __simple__ if there are precisely two [[quotient objects]] of $X$, namely $1$ and $X$.  

=--

+-- {: .num_remark}
###### Remark

If $C$ is [[abelian category|abelian]], then the terminal object is a [[zero object]] and we may use [[subobjects]] in place of quotient objects in the definition, and this is more common; the result is the same.

=--


+-- {: .num_remark}
###### Remark

The [[terminal object ]] itself is *not* simple, as it has only *one* quotient object.  It is [[too simple to be simple]].

=--

+-- {: .num_remark}
###### Remark

In [[constructive mathematics]], we want to phrase the definition as: a quotient object of $X$ is $X$ if and only if it is not $1$.

=--

+-- {: .num_defn}
###### Definition

An [[object]] which is a [[direct sum]] of simple objects is called a **[[semisimple object]]**.

=--

## Properties

### In an abelian category

\begin{proposition}
**([[Schur's lemma]])**

In an [[abelian category]] $C$, every [[morphism]] between simple objects is either a [[zero morphism]] or an [[isomorphism]], and the [[endomorphism]] [[algebra]] of any simple object is a [[division ring]].

If $C$ is also [[enriched category|enriched]] in [[finite-dimensional vector spaces]] over an [[algebraically closed field]] $k$, then $hom(X, Y)$ has [[dimension]] $0$ or $1$ for any pair of simple objects $X$ and $Y$.  In this case the endomorphism algebra of any simple object is $k$.
\end{proposition} 

\begin{proof} 
Suppose $X$ and $Y$ are simple objects in an abelian category $C$. If $f \colon X \to Y$ is any morphism then the kernel of $f$ must be either $0$ or $X$, while its cokernel must be $0$ or $Y$. If the kernel and cokernel are both $0$, $f$ is an isomorphism; otherwise $f = 0$. It follows that every element of the endomorphism ring $End(X)$ of a simple object $X$ is zero or invertible, so $End(X)$ is a division ring. 

Next suppose $C$ is enriched over finite-dimensional vector spaces over an algebraically closed field $k$.   In this case $End(X)$ is a finite-dimensional division algebra over $k$, but any such algebra is isomorphic to $k$.   Post-composing with an isomorphism $f: X \to Y$ gives a vector space isomorphism $End(X) \to hom(X,Y)$, so if such an isomorphism $f$ exists then $hom(X,Y)$ is one-dimensional.  If no such isomorphism exists all the morphisms from $X$ to $Y$ are zero.
\end{proof}

+-- {: .num_remark}
###### Remark

If an abelian category is enriched over finite-dimensional vector spaces over a field $k$ that is not algebraically closed, the endomorphism algebra of a simple object can be a division algebra other than $k$.  For example consider $k = \mathbb{R}$.  In the category of real representations of the [[Lie group]] [[SO(2)]], the usual action of rotations on the plane gives a simple object (that is, [[irreducible representation]]) $X$ with $End(X) \cong \mathbb{C}$. In the category of real representations of [[Sp(1))]], the action of this group by right multiplication on the [[quaternions]] gives a simple object $X$ with $End(X) \cong \mathbb{H}$.

=--

## Examples

*  In the category [[Vect]] of [[vector spaces]] over some field $k$, the simple objects are precisely the [[line]]s: the $1$-dimensional vector spaces, i.e. $k$ itself, up to [[isomorphism]].

*  A [[simple group]] is a simple object in [[Grp]].  (Here it is important to use quotient objects instead of subobjects.)

*  For $G$ a [[group]] and $Rep(G)$ its [[category of representations]], the simple objects are the [[irreducible representations]].

*  A [[simple ring]] is a simple object in [[Ring]]. Equivalently, it is a ring $R$ that is simple in its category of [[bimodules]].

*  A [[simple Lie algebra]] is a simple object in [[LieAlg]] that (by conventional fiat) is not [[abelian Lie algebra|abelian]].  As an abelian Lie algebra is simply a [[vector space]], the only simple object of $Lie Alg$ that is not accepted as a simple Lie algebra is the $1$-dimensional Lie algebra.


## Related entries

* [[length of an object]]

* [[semisimple category]]

  * [[fusion category]]

  * [[modular tensor category]]




[[!redirects simple object]]
[[!redirects simple objects]]
[[!redirects simple module]]
[[!redirects simple modules]]

[[!redirects irreducible object]]
[[!redirects irreducible objects]]
