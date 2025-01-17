
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Horizontal categorification_ or _oidification_ (to be contrasted with the more famous *[[vertical categorification]]* which is usually just called *[[categorification]]*) describes the process by which 

 1. a concept is realized to be equivalent to a certain type of [[category]] or [[magmoid]] with a _single [[object]]_;

 2. and then this concept is generalized -- or oidified -- by passing to instances of such types of categories with more than one object.


## Examples

\begin{example}\label{Groupoids}
**(groups to groupoids)**
\linebreak
The horizontal categorification of [[groups]] are [[groupoids]]: [[category|categories]] in which every morphism is invertible.
\end{example}

Similar comments as the following Remark \ref{AreGroupoidsGeneralizedGroups} apply generally to oidification:

\begin{remark}\label{AreGroupoidsGeneralizedGroups}
In Ex. \ref{Groupoids} there is an "inclusion" [[2-functor]] of (the [[1-category]] [[Grp]]) of groups into (the [[(2,1)-category]] [[Grpd]]) of groupoids, by passage to [[delooping groupoids]] $\mathbf{B}(-)$,

$$
  \begin{array}{ccc}
    Grp &\longrightarrow& Grpd
    \\
    G &\mapsto& \mathbf{B}G
    \mathrlap{\,.}
  \end{array}
$$

Beware, though, that this 2-functor is *not* [[locally fully faithful 2-functor|fully faithful]]: For $G, H \in Grpd$, the [[hom-groupoid]] between their [[delooping groupoids]] is not quite the set of [[group homomorphisms]] $G \to H$, but is the [[action groupoid]] of that by the pointwise [[adjoint action]] of $H$:
$$
  Grpd\big(
    \mathbf{B}G
    ,\,
    \mathbf{B}H
  \big)
  \;\simeq\;
  Grp\big(
    G
    ,\,
    H
  \big)
  \sslash_{ad}
  H
  \mathrlap{\,.}
$$

For instance, if $H = A$ is [[abelian group|abelian]] then
$$
  Grpd\big(
    \mathbf{B}G
    ,\,
    \mathbf{B}A
  \big)
  \;\simeq\;
  Grp\big(
    G
    ,\,
    A
  \big)
  \times
  \mathbf{B}A
  \mathrlap{\,.}
$$

This is one formal way of seeing that it is not *quite* right to say that "groupoids are generalized groups", not without further qualification:

Namely, since $\mathbf{B}G$ is canonically a [[pointed object]] in [[Grpd]] (uniquely pointed by its single [[object]]), one may instead consider the [[delooping]]-construction to land in the [[(2,1)-category]] $Grpd^\ast$ of [[pointed object|pointed]] groupoids

$$
  \begin{array}{ccc}
    Grp &\longrightarrow& Grpd^\ast
    \\
    G &\mapsto& \mathbf{B}G
  \end{array}
$$

and as such this *is* [[locally fully faithful 2-functor|fully faithful]], [[equivalence of 2-categories|equivalently]] identifying groups with [[pointed connected groupoids]]:

$$
  Grpd^\ast\big(
    \mathbf{B}G
    ,\,
    \mathbf{B}H
  \big)
  \;\simeq\;
  Hom\big(
    G
    ,\,
    H
  \big)
  \mathrlap{\,.}
$$

This is part of a general phenomenon discussed further at *[[looping and delooping]]* (cf. also at *[[May recognition theorem]]*).

In practice, for instance [[Picard groupoids]] appear as generalized [[abelian groups]]: Indeed, Picard groupoids are [[abelian 2-groups]] and as such are in particular pointed (by their [[neutral element]], the [[tensor unit]]-[[object]]).
\end{remark}

\begin{example}\label{Algebroids}
**(algebras to algebroids)**
\linebreak
A horizontal categorification of [[algebras]] are [[algebroids]]: [[enriched category|categories enriched]] in the [[category of vector spaces]], regarded as a [[symmetric monoidal category]] via the [[tensor product of vector spaces]].
\end{exmaple}

\begin{example}
**(rings to ringoids)**
\linebreak
A horizontal categorification of [[rings]] are [[ringoids]]: [[enriched category|categories enriched]] over the [[category of abelian groups]], via the [[tensor product of abelian groups]] (cf. [blog](http://golem.ph.utexas.edu/category/2006/09/ringoids.html)).
\end{example}

\begin{example}
**($C^\ast$-algebras to $C^\ast$-categories)**
\linebreak
A horizontal categorification of [[C-star algebras|$C^*$-algebras]] hence ought to be known as _$C^\ast$--algebroids_  but is usually known as *[[C-star-category|$C^\ast$-categories]]*.
\end{example}

\begin{example}
**(groups to groupoids)**
\linebreak
Since, by the [[Gelfand-Naimark theorem]], [[C-star algebra|$C^\ast$-algebras]] are [[duality|dual]] to [[topological spaces]], [[Paolo Bertozzini]] et. al proposed to define *[[spaceoids]]* to be the entities [[formal duality|formally dual]] to $C^*$-categories (cf. [blog](http://golem.ph.utexas.edu/category/2008/01/spaceoids.html)).
\end{example}

\begin{example}\label{Monoidoid}
**(monoids to categories)**
\linebreak
And an **exception to the rule**: The many-object verion of [[monoids]] are _not_ called a _[[monoidoids]]_ -- but are called... [[categories]]! 

 On the other hand, in the case of [[enriched category|enrichment]] over [[R Mod]] (for $R$ a [[commutative ring]]), monoids are known as [[associative algebras]] over $R$
and the oidificies $R Mod$-categories may reasonably be and sometimes are called *[[algebroid]]* over $R$, 
as in Ex. \ref{Algebroids}
\end{example}

\begin{example}
**(monads to bicategory-enriched categories)**
\linebreak
A horizontal categorification of the notion of *[[monads]]* is that of *[[categories enriched in a bicategory]]*.
\end{example}

\begin{example}\label{LawvereTheoriesAndOperads}
**(Lawvere theories and operads)**
\linebreak
A horizontal categorification of a single-sorted [[Lawvere theory]] are  multisorted Lawvere theory. Analogously [[operads]] categorify to a many-colored operad.
\end{example}

\begin{example}\label{InTypeTheory} 
In [[type theory]]/[[programming language theory]], horizontal categorification is analogous to *introducing a type distinction*: an untyped language is a special case of a typed language where there is exactly one [[type]]. This fits with the [[categorical semantics]]: untyped [[lambda calculus]] has models in [[Lawvere theories]], whereas (simply) [[typed lambda calculus]] has models in Cartesian [[multicategories]].
\end{example}


[[!include oidification - table]]

## General definition

Tom Leinster's book "Higher Operads, Higher Categories"
contains a general theory of horizontal categorification of a notion of algebraic structure, as long as the algebraic structure can be defined as the category of algebras for an operad. Leinster proves that if $P$ is a (non-symmetric) operad in the category of sets, then $P$ can be extended to an "fc-multicategory" $\Sigma P$, the *suspension* of $P$, which is a kind of generalized operad which acts on directed graphs. So, for example, the horizontal categorification of the algebraic theory of monoids, as an operad, is the algebraic theory of categories, as a generalized operad. Eugenia Cheng has extended this definition of suspension so that it works for non-symmetric operads in a monoidal category $\mathcal{V}$ satisfying certain co/completeness assumptions. For example, one can take $\mathcal{V}= \mathbf{Cat}$. In this case, the operad $P$ whose algebras are monoidal categories has for its suspension (i.e., its horizontal categorification) the generalized operad whose algebras are precisely bicategories.


## Further discussion


* [[John Baez]], [_What is categorification?_](http://golem.ph.utexas.edu/category/2008/10/what_is_categorification.html)

* [[John Baez]], [_Ringoids_](http://golem.ph.utexas.edu/category/2006/09/ringoids.html)

* [[John Baez]], [_Higher Operads, Higher Categories_](https://arxiv.org/abs/math/0305049)

* [[Eugenia Cheng]], [_Comparing operadic theories of $n$-category_](https://arxiv.org/pdf/0809.2070)


[[!redirects Oidification]]
[[!redirects oidification]]
[[!redirects oidifications]]
[[!redirects horizontal categorifications]]