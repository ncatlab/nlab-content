
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# Companion pairs
* table of contents
{: toc}

## Idea

A **companion pair** in a [[double category]] is a way of saying that a [[horizontal  morphism]] and a [[vertical morphism]] are "[[isomorphism|isomorphic]]", even though they do not live in the same [[1-category]]/[[2-category]].

A **connection pair** in a [[double category]] is a [[strict 2-functor|strictly 2-functorial]] choice of companion pairs for every vertical morphism.

## Definition

Let $f\colon A\to B$ be a [[vertical morphism]] and $f'\colon A\to B$ a [[horizontal morphism]] in a [[double category]].  These are said to be a **companion pair** if they come equipped with [[2-morphisms]] of the form:
$$
  \array{ 
    A & \overset{f'}{\longrightarrow} & B 
    \\
    \mathllap{^f}\big\downarrow & \mathllap{^\phi}\swArrow & \big\downarrow\mathrlap{^id} 
    \\
    B & \underset{id}{\longrightarrow} & B
  } 
  \qquad
  \qquad 
  \text{and}
  \qquad
  \qquad
  \array{ 
    A & \overset{id}{\longrightarrow} & A 
   \\
   \mathllap{^id}\big\downarrow & \mathllap{^\psi}\swArrow & \big\downarrow\mathrlap{^f} 
   \\
   A & \underset{f'}{\longrightarrow} & B 
  }
$$
such that $\phi \circ_h \psi = id_{f'}$ and $\phi \circ_v \psi = id_{f}$, where $\circ_h$ and $\circ_v$ denote horizontal and vertical composition of 2-cells.

Given such a companion pair, we say that $f$ and $f'$ are **companions** of each other.


## Examples

\begin{example}
In the double category $\mathbf{Sq}(K)$ of squares ([[quintets]]) in any [[2-category]] $K$, a companion pair is simply an invertible 2-cell between two parallel 1-morphisms of $K$.
\end{example}

\begin{example}
In the [[double category of algebras | double category $T$-$\mathbf{Alg}$ of algebras, lax morphisms, and colax morphisms]] for a [[2-monad]] $T$, an arrow (of either sort) has a companion precisely when it is a *strong* (= pseudo) $T$-morphism.  This is important in the theory of [[doctrinal adjunction]].
\end{example}


## Properties

* The horizontal (or vertical) dual of a companion pair is a [[conjunction]].

* Companion pairs (and conjunctions) have a [[mate]] correspondence generalizing the calculus of mates in 2-categories.

* If every vertical arrow in some double category $D$ has a companion, then the functor $f\mapsto f'$ is a [[pseudofunctor]] $V D\to H D$ from the vertical 2-category to the horizontal one, which is the identity on objects, and [[locally fully faithful 2-functor|locally fully faithful]] by the mate correspondence.  A choice of companions that make this a strict 2-functor is called a [[connection on a double category|connection]] on $D$ (an arbitrary choice of companions may be called a "pseudo-connection").  A double category with a connection is thereby equivalent to an [[F-category]].  If every vertical arrow also has a [[conjoint]], then this makes $D$ into a [[proarrow equipment]], or equivalently a [[framed bicategory]].

* Companion pairs and mate-pairs of 2-cells between them in any double category $D$ form a 2-category $Comp(D)$.  The functor $Comp\colon DblCat \to 2Cat$ is right adjoint to the functor $Sq\colon 2Cat \to DblCat$ sending a 2-category to its double category of [[quintet construction|squares]].

## Related concepts

* [[retrocell]]

## References

* [[Marco Grandis]] and [[Robert Pare]], *Adjoints for double categories*, [NUMDAM](http://www.numdam.org/item/CTGDC_2004__45_3_193_0.pdf)

* [[Robert Dawson]] and [[Robert Pare]] and [[Dorette Pronk]], *The Span construction*, [TAC](http://www.tac.mta.ca/tac/volumes/24/13/24-13abs.html).

* [[Michael Shulman]], *Framed bicategories and monoidal fibrations*, [TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html)

This latter reference explains the relationship between companions to connection pairs and **foldings**:

* [[Ronnie Brown]] and C.B. Spencer, [Double groupoids and crossed modules](http://www.numdam.org/item/CTGDC_1976__17_4_343_0), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **17** (1976), 343--362.

* [[Ronald Brown]] and Ghafar H. Mosa, _Double categories, 2-categories, thin structures and connections_, Theory and Application of Categories 5.7 (1999): 163-1757.

* [[Thomas M. Fiore]], _Pseudo Algebras and Pseudo Double Categories_, _Journal of Homotopy and Related Structures_, Volume 2, Number 2, pages 119-170, 2007. 51 pages.


[[!redirects companion]]
[[!redirects companions]]
[[!redirects companion pair]]
[[!redirects companion pairs]]
[[!redirects companion pair in a double category]]
[[!redirects companion pairs in a double category]]
[[!redirects companion pairs in double categories]]
[[!redirects connection pair]]
[[!redirects connection pairs]]
