+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

(...)

## Definition

Let $(T,\mu,\eta)$ be a [[monad]] on a [[category]] $C$.
An **algebra over $T$**, or **$T$-algebra**, consists of an object $A$ of $C$ together with a morphism $a:TA\to A$ of $C$, such that the following diagrams commute.

\begin{tikzcd}
A\ar{r}{\eta} \ar[swap]{dr}{id} & TA \ar{d}{a} & & TTA \ar{r}{Ta} \ar{d}{\mu} & TA \ar{d}{a} \\ 
& A & & TA \ar{r}{a} & A
\end{tikzcd} 

The diagram on the left is sometimes called the _unit triangle_, and the diagram on the right the _multiplication square_ or _algebra square_. 

### Morphisms of algebras

Let $(A,a)$ and $(B,b)$ be $T$-algebra. A **morphism of $T$-algebras** is a morphism $f:A\to B$ of $C$ which makes the following diagram commute.

\begin{tikzcd}
TA \ar{r}{Tf} \ar{d}{a} & TB \ar{d}{b} \\
A \ar{r}{f} & B
\end{tikzcd}

The category of $T$-algebras and their morphisms is called the **Eilenberg-Moore category** and denoted by $C^T$.


## Examples

(...)

## Generalizations

An algebra over a monad is a special case of a [[module over a monad]] in a bicategory. See there for more information.

The Eilenberg-Moore category is also a special case of a more general construction, namely the [[Eilenberg-Moore object]]. See there for more information.


## Related concepts

* **algebra over a monad**, [[module over a monad]], [[algebra over an endofunctor]], [[coalgebra over an endofunctor]], [[algebra over a profunctor]]

  [[∞-algebra over an (∞,1)-monad]] 

  * [[model structure on algebras over a monad]]

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]] / [[model structure on simplicial T-algebras]]

* [[algebra over an operad]] 

   [[∞-algebra over an (∞,1)-operad]]

   * [[model structure on algebras over an operad]]

* [[Eilenberg-Moore category]], [[Kleisli category]], [[Eilenberg-Moore object]], [[Kleisli object]]

## References 

(...)

[[!redirects algebra for a monad]]
[[!redirects algebra over a monad]]
[[!redirects algebras of a monad]]
[[!redirects algebras for a monad]]
[[!redirects algebras over a monad]]
[[!redirects algebras for monads]]
[[!redirects algebras over monads]]

[[!redirects Eilenberg-Moore algebra]]
[[!redirects Eilenberg-Moore algebras]]