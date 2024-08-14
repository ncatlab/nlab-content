
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

A **companion pair** in a [[double category]] is a way of saying that a [[loose arrow]] and a [[tight morphism]] are "[[isomorphism|isomorphic]]", even though they do not live in the same [[1-category]]/[[2-category]].

A **connection pair** in a [[double category]] is a [[strict 2-functor|strictly 2-functorial]] choice of companion pairs for every tight morphism.

## Definition

Let $f\colon A\to B$ be a [[tight morphism]] and $g\colon A \nrightarrow B$ a [[loose arrow]] in a [[double category]].  These are said to be a **companion pair** if they come equipped with [[2-morphisms]] of the form:
\begin{tikzcd}
	A & A && A & B \\
	A & B && B & B
	\arrow[""{name=0, anchor=center, inner sep=0}, "\shortmid"{marking}, Rightarrow, no head, from=1-1, to=1-2]
	\arrow[Rightarrow, no head, from=1-1, to=2-1]
	\arrow["f", from=1-2, to=2-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{g}", "\shortmid"{marking}, from=1-4, to=1-5]
	\arrow["f"', from=1-4, to=2-4]
	\arrow[Rightarrow, no head, from=1-5, to=2-5]
	\arrow[""{name=2, anchor=center, inner sep=0}, "{g}"', "\shortmid"{marking}, from=2-1, to=2-2]
	\arrow[""{name=3, anchor=center, inner sep=0}, "\shortmid"{marking}, Rightarrow, no head, from=2-4, to=2-5]
	\arrow["\psi", shorten <=4pt, shorten >=4pt, Rightarrow, from=0, to=2]
	\arrow["\phi", shorten <=4pt, shorten >=4pt, Rightarrow, from=1, to=3]
\end{tikzcd}
such that $\phi \circ_\tau \psi = id_{g}$ and $\phi \circ_\lambda \psi = id_{f}$, where $\circ_\tau$ and $\circ_\lambda$ denote, respectively, loose and tight composition of 2-cells.

Given such a companion pair, we say that $f$ and $g$ are **companions** of each other.
A double category admitting companions to all its tight morphisms is sometimes called a **company**.

## Examples

\begin{example}
In the double category $\mathbf{Sq}(K)$ of squares ([[quintets]]) in any [[2-category]] $K$, a companion pair is simply an invertible 2-cell between two parallel 1-morphisms of $K$.
\end{example}

\begin{example}
In the [[double category of algebras | double category $T$-$\mathbf{Alg}$ of algebras, lax morphisms, and colax morphisms]] for a [[2-monad]] $T$, an arrow (of either sort) has a companion precisely when it is a *strong* (= pseudo) $T$-morphism.  This is important in the theory of [[doctrinal adjunction]].
\end{example}


## Properties

* The loose (or tight) dual of a companion pair is a [[conjunction]].

* Companion pairs (and conjunctions) have a [[mate]] correspondence generalizing the calculus of mates in 2-categories.

* If every tight arrow in some double category $D$ has a companion, then the functor $f\mapsto g$ is a [[pseudofunctor]] $T D \to L D$ from the tight 2-category to the loose one, which is the identity on objects, and [[locally fully faithful 2-functor|locally fully faithful]] by the mate correspondence.  A choice of companions that make this a strict 2-functor is called a [[connection on a double category|connection]] on $D$ (an arbitrary choice of companions may be called a "pseudo-connection").  A double category with a connection is thereby equivalent to an [[F-category]].  If every tight arrow also has a [[conjoint]], then this makes $D$ into a [[proarrow equipment]], or equivalently a [[framed bicategory]].

* Companion pairs and mate-pairs of 2-cells between them in any double category $D$ form a 2-category $Comp(D)$.  The functor $Comp\colon DblCat \to 2Cat$ is right adjoint to the functor $Sq\colon 2Cat \to DblCat$ sending a 2-category to its double category of [[quintet construction|squares]].

* A double category $\mathbb{C}$, carried by the span of categories $C_0 \xleftarrow{s} C_1 \xrightarrow{t} C_0$ has all companions iff such span is a [[two-sided fibration]] in the sense of Street. Indeed, consider a [[tight map]] $h:A \to B$ in $\mathbb{C}$, thus a morphism in $C_0$, and the unit [[loose arrow]] $U_A$ of $A$: since $s$ is an [[opfibration]], we obtain a square $\eta:=\mathrm{cocart}_h: U_A \Rightarrow h_* U_A$, with source (top boundary) $h$ and target (bottom boundary) necessarily $1_B$ since $s$-cartesian maps are $t$-vertical in a two-sided fibration. Dually, we get a cartesian square $\varepsilon:=\mathrm{cart}_h : h^*U_B \Rightarrow U_B $. We claim $\mathrm{cocart}_h$ and $\mathrm{cart}_h$ are, respectively, the unit and counit of a companionship between $h$ and $h':=h^*U_B = h_*U_A$. First, observe this latter equation holds since the identiy square of $h$ factors as $\varepsilon \eta$, using either universal property. This proves also the first companionship equation. As for the fact $\eta \odot \varepsilon = 1_{h'}$, it follows again from the aforementioned factorization: $\eta \odot \varepsilon$ is an $(s,t)$-vertical morphism which is thus isomorphic to the identity of $h'$ by uniqueness of the $s$-vertical, $(s,t)$-vertical, $t$-vertical factorization of a morphism in $C_1$.
*Vice versa*, companions can be used to construct the above co/cartesian lifts, as shown in ([Shulman '08](#Shulman08)).

## Related concepts

* [[retrocell]]
* [[conjunction]]

## References

* [[Marco Grandis]] and [[Robert Pare]], *Adjoints for double categories*, [NUMDAM](http://www.numdam.org/item/CTGDC_2004__45_3_193_0.pdf)

* [[Robert Dawson]] and [[Robert Pare]] and [[Dorette Pronk]], *The Span construction*, [TAC](http://www.tac.mta.ca/tac/volumes/24/13/24-13abs.html).

* {#Shulman08} [[Michael Shulman]], *Framed bicategories and monoidal fibrations*, [TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html)

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
