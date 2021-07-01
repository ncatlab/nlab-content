+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

There are different, related ways in which one could view the notion of algebra over a [[monad]]. 

* If one views monads as a generalization of [[algebraic theories]] (see [[algebraic theory#RelationToMonads|algebraic theory -  relation to monads]]), an algebra over a monad is the corresponding generalization of an [[algebra over a Lawvere theory|algebra over a theory]]. In particular, if one views a monad as a way of prescribing particular [[operations]], an algebra is a context where those specified formal expressions can be evaluated to an actual result.
* From the 2-dimensional point of view, an algebra over a monad is a special case of a [[module over a monad]] for the bicategory [[Cat]], where the arrow is from the [[terminal category]].
* If one views monads as a way to model computational effects (see [[monad in computer science]]), an algebra is a context in which the extra effects can be reincorporated into the main data. 

Algebras over a monad are usually objects equipped with extra [[structure]], not just [[properties]]. (They can also be seen as [[algebra over an endofunctor|algebras over the underlying endofunctor]], satisfying extra compatibility [[properties]].)

## Definition

Let $(T,\mu,\eta)$ be a [[monad]] on a [[category]] $C$.
An **algebra over $T$**, or **$T$-algebra**, consists of an object $A$ of $C$ together with a morphism $a:TA\to A$ of $C$, such that the following diagrams commute.

\begin{tikzcd}
A\ar{r}{\eta} \ar[swap]{dr}{\mathrm{id}} & TA \ar{d}{a} & & TTA \ar{r}{Ta} \ar{d}{\mu} & TA \ar{d}{a} \\ 
& A & & TA \ar{r}{a} & A
\end{tikzcd} 

The diagram on the left is sometimes called the _unit triangle_, and the diagram on the right the _multiplication square_ or _algebra square_. 

The corresponding [[dual]] notion is that of a [[coalgebra over a comonad]].

In the case of a commutative monad, one can define a [tensor product of algebras](https://ncatlab.org/nlab/show/tensor+product+of+algebras+over+a+commutative+monad).

### Morphisms of algebras

Let $(A,a)$ and $(B,b)$ be $T$-algebra. A **morphism of $T$-algebras** is a morphism $f:A\to B$ of $C$ which makes the following diagram commute.

\begin{tikzcd}
TA \ar{r}{Tf} \ar{d}{a} & TB \ar{d}{b} \\
A \ar{r}{f} & B
\end{tikzcd}

The category of $T$-algebras and their morphisms is called the **[[Eilenberg-Moore category]]** and denoted by $C^T$.

### Free algebras

Given a monad $(T,\mu,\eta)$ on a category $C$, for every object $X$ of $C$, the object $T X$ is canonically equipped with a $T$-algebra structure, given by the multiplication map $\mu$. The relevant diagrams commute by the monad axioms.

Algebras of this sort are called **free algebras**. 

Given any morphism $f:X\to Y$ of $C$, the map $T f:T X\to T Y$ is a morphism of algebras, by naturality of $\mu$. In general, not every morphism of algebras between $T X$ and $T Y$ arises this way.

The subcategory of free algebras and their morphisms is (equivalent to) the **[[Kleisli category]]**.


## Examples

Many monads are named after their (free) algebras. 

* The algebras of the _free monoid monad_ on [[Set]] are [[monoids]], and the morphisms of algebras the monoid homomorphisms.
* The algebras of the _free commutative monoid monad_ on [[Set]] are [[commutative monoids]], and their morphisms the monoid homomorphisms between them. 
* The algebras of the _free group monad_ on [[Set]] are groups, and their morphisms are the group homomorphisms.
* ...and so on. 

In these cases, the notion of _free group_, _free monoid_, et cetera coincide with the notion of free algebra given above.


* Given a [[monoid]] or [[group]] $M$, the algebras of the $M$-[[action monad]] on [[Set]] are the $M$-sets, i.e. sets equipped with an [[action]] of $M$. The morphisms are the [[equivariant maps]]. 
* The example above generalizes to [[action monads]] given by [[monoid objects]] in a general [[monoidal category]]. Famous examples of this construction in mathematics are smooth actions of [[Lie groups]] on [[manifolds]] and actions of [[rings]] on their [[modules]].

* The algebras of the [[maybe monad]] $(-)_*\colon Set \to Set$, which adds a disjoint point, are the pointed sets.
* The algebras of the [[power set]] monad are the sup-[[semilattices]].
* The algebras of the [[distribution monad]] are [[convex spaces]], and more generally algebras of [[probability monads]] correspond to generalized [[convex spaces]] or [[conical spaces]] (see [[probability monad#algebras_expectation_values|probability monad - algebras]]).


## Generalizations

An algebra over a monad is a special case of a [[module over a monad]] in a [[bicategory]]. See there for more information.

The Eilenberg-Moore and Kleisli categories are also special cases of more general 2-dimensional [[universal constructions]], namely the [[Eilenberg-Moore object]] and the [[Kleisli object]]. See those pages for more information.


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

An introduction to the basic ideas, which gives some intuition for newcomers, can be found in

* [[Paolo Perrone]], _Notes on Category Theory with examples from basic mathematics_, Chapter 5. ([arXiv](http://arxiv.org/abs/1912.10642))

See also the [[monad#references|references of the article on monads]].


[[!redirects algebra for a monad]]
[[!redirects algebra over a monad]]
[[!redirects algebras of a monad]]
[[!redirects algebras for a monad]]
[[!redirects algebras over a monad]]
[[!redirects algebras for monads]]
[[!redirects algebras over monads]]

[[!redirects Eilenberg-Moore algebra]]
[[!redirects Eilenberg-Moore algebras]]