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

There are different, related ways in which one could view the notion of *algebra over a [[monad]]*: 

* If one views monads as a generalization of [[algebraic theories]] (see [[algebraic theory#RelationToMonads|algebraic theory -  relation to monads]]), an algebra over a monad is the corresponding generalization of an [[algebra over a Lawvere theory|algebra over a theory]]. In particular, if one views a monad as a way of prescribing particular [[operations]], an algebra is a context where those specified formal expressions can be evaluated to an actual result.
* From the 2-dimensional point of view, an algebra over a monad is a special case of a [[module over a monad]] for the bicategory [[Cat]], where the arrow is from the [[terminal category]].
* If one views monads as a way to model computational effects (see [[monad in computer science]]), an algebra is a context in which the extra effects can be reincorporated into the main data. 

Algebras over a monad are usually objects equipped with extra [[structure]], not just [[properties]]. (They can also be seen as [[algebra over an endofunctor|algebras over the underlying endofunctor]], satisfying extra compatibility [[properties]].)

The corresponding [[formal duality|dual]] notion is that of *[[coalgebra over a comonad]]*.



## Definition
 {#Definition}

Let $(T,\eta, \mu)$ be a [[monad]] on a [[category]] $\mathcal{C}$.

### Algebras
 {#Algebras}

\begin{definition}
An **algebra over $T$** (or just **$T$-algebra** or **$T$-module**) consists of:

1. an [[object]] $A$ of $\mathcal{C}$,

1. a [[morphism]] $a \colon T (A) \longrightarrow A$ of $\mathcal{C}$, 

such that the following [[commuting diagram|diagrams commute]] in $\mathcal{C}$ (cf. the definition of *[[module object]]* [here](module+object#MonoidsInMonoidalCategory)):

\[
  \label{UnitProperty}
  \text{Unit Property:}
\]
\begin{tikzcd}
  A 
  \ar{r}{\eta} 
  \ar[swap]{dr}{\mathrm{id}} 
  & 
  T(A) 
  \ar{d}{a} 
  \\
  & 
  A 
\end{tikzcd}

\linebreak

\[
  \label{ActionProperty}
  \text{Action Property:}
\]
\begin{tikzcd}
  T\big(T(A)\big) 
  \ar{r}{T(a)} 
  \ar{d}{\mu} 
  & 
  TA 
  \ar{d}{a} 
  \\ 
  TA 
  \ar{r}{a} 
  & 
  A
\end{tikzcd} 

\end{definition}

\begin{remark}
The diagram (eq:UnitProperty) is also sometimes called the _unit triangle_, and the diagram (eq:ActionProperty) is also called the _multiplication square_ or _algebra square_. 
\end{remark}


### Homomorphisms

Let $(A,a)$ and $(B,b)$ be $T$-algebras. A **[[homomorphism]] of $T$-algebras** is a [[morphism]] $f \colon A \to B$ of $\mathcal{C}$ which makes the following [[commuting diagram|diagram commute]].

\begin{tikzcd}
  TA 
  \ar{r}{Tf} 
  \ar{d}{a} 
  & 
  TB 
  \ar{d}{b} 
  \\
  A 
  \ar{r}{f} 
  & 
  B
\end{tikzcd}

The [[category]] formed by $T$-algebras and their homomorphisms is known as the **[[Eilenberg-Moore category]]** of $T$ and often denoted by $\mathcal{C}^T$.


### Free algebras
 {#FreeAlgebras}

Given a [[monad]] $(T,\mu,\eta)$ on a [[category]] $\mathcal{C}$, then for every [[object]] $X$ of $\mathcal{C}$, the object $T X$ is canonically equipped with a $T$-algebra [[structure]], given by the multiplication map $\mu$ of the monad. The relevant diagrams commute by the monad axioms.

$T$-Algebras of this sort are called **[[free construction|free]] $T$-algebras**. 

Given any [[morphism]] $\phi \colon X \to Y$ of $\mathcal{C}$, the [[morphism]] $T \phi \colon T X \longrightarrow T Y$ is evidently a [[homomorphism]] of $T$-algebras, by [[natural transformation|naturality]] of $\mu$. But not every homomorphism of $T$-algebras between the free $T$-algebras $T X$ and $T Y$ arises this way, in general.

However, for any morphism of the form 
$$
  f \colon X \longrightarrow T Y
$$ 
in $\mathcal{C}$ (called a $T$-*[[Kleisli morphism]]*), the induced morphism
\[
  \label{AlgebraMapInducedByKleisliMorphism}
  \mu_{Y} \circ T f 
  \;\colon\; 
  T X 
    \xrightarrow{\;\; T f  \;\;}
  T T Y
    \xrightarrow{\;\; \mu_Y \;\;}
  TY
\]

*is* a [[homomorphism]] of $T$-algebras between these free $T$-algebras, as one verifies again using the [[natural transformation|naturality]] of $\mu$. Now, all homomorphisms of $T$-algebras between the free algebras $T X$ and $T Y$ *do* arise this way.

Moreover, given in addition a morphism in $\mathcal{C}$ of the form  $g \colon Y \longrightarrow T Z$,
then, under this association, the [[composition]] of the corresponding $T$-algebra morphisms (eq:AlgebraMapInducedByKleisliMorphism) of $f$ and $g$
equals the $T$-algebra homomorphism corresponding to their *[[Kleisli composition|Kleisli composite]]*, defined by
$$
  g \circ_T f
    \;\coloneqq\;
  X
    \xrightarrow{ f }
  T Y
    \xrightarrow{ T g }
  T T Z
    \xrightarrow{ \mu_Z }
  T Z
  \,.
$$

The [[category]] of [[Kleisli morphisms]] equipped with this [[Kleisli composition]] is called the *[[Kleisli category]]* and is [[equivalence of categories|equivalent]] to the [[full subcategory]] of $T$-algebras on the free $T$-algebras (see [there](Kleisli+category#InTermsOfKleisliMorphisms) for more).

### Tensor product

In the case of a [[commutative monad]] $T$ , one can define a [[tensor product of algebras over a commutative monad|tensor product of monad algebras]], see there for more. 

## Examples

Many monads are named after their (free) algebras:

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

 

### General

> See the *[References](monad#References)* at *[[monad]]*, such as:

* [[Saunders MacLane]], §VI.2 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5**  Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


An introduction to the basic ideas, which gives some intuition for newcomers, can be found in

* [[Paolo Perrone]], Chapter 5 of: _Notes on Category Theory with examples from basic mathematics_,  &lbrack;[arXiv:1912.10642](http://arxiv.org/abs/1912.10642)&rbrack;


### Kleisli/extension system-style
 {#ReferencesKleisliStyle}

For monads presented in "[[extension system]]"/"[[Kleisli triple]]"-form (the way traditionally used for [[monads in computer science]] -- i.e. in terms of a "bind"-operation taking [[Kleisli maps]] to actual [[morphisms]], not explicitly referring to the monad product) there is the corresponding "Kleisli-triple style" or "Mendler style" &lbrack;[Uustalu (2021), p. 4](#Uustalu21Lecture2)&rbrack; for presenting the algebra/module-structures for these monads:

* {#MarmolejoWood10} [[F. Marmolejo]], [[Richard J. Wood]], Def. 3.1 in: *Monads as extension systems -- no iteration is necessary* [[TAC]] **24** 4 (2010) 84-113 &lbrack;[tac:24-04](http://www.tac.mta.ca/tac/volumes/24/4/24-04abs.html)&rbrack;

* [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], Def. 2.11 in: *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;

  > (stated in the generality of [[relative monads]])

* {#Uustalu21Lecture2} [[Tarmo Uustalu]], p. 4 of: *Monads and Interaction Lecture 2*  lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021) &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs2.pdf), [[Uustalu-Monads2.pdf:file]]&rbrack;

   
See also

* [[R. F. C. Walters]], Chapter I of: *A categorical approach to universal algebra*, Ph.D. Thesis (1970) &lbrack;[anu:1885/133321](https://openresearch-repository.anu.edu.au/handle/1885/133321)&rbrack;



[[!redirects algebra for a monad]]
[[!redirects algebra over a monad]]
[[!redirects algebras of a monad]]
[[!redirects algebras for a monad]]
[[!redirects algebras over a monad]]
[[!redirects algebras for monads]]
[[!redirects algebras over monads]]

[[!redirects Eilenberg-Moore algebra]]
[[!redirects Eilenberg-Moore algebras]]