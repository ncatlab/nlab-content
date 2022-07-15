
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Definition

\begin{definition}
A **Heyting algebra** is a [[lattice]] $L$ which as a [[poset]] admits an operation of [[implication]] 

$$\Rightarrow: L^{op} \times L \to L$$ 

satisfying the condition (really a [[universal property]])

\[ \label{UniversalProperty}
(x \wedge a) \leq b \qquad \text{if and only if} \qquad x \leq (a \Rightarrow b)
\]

\end{definition}

This is equivalent to the following definition.

\begin{definition}
A **Heyting algebra** is a [[bicartesian closed category|bicartesian closed]] [[poset]], that is a poset which (when thought of as a [[thin category]]) is

* [[finitely complete category|finitely complete]], 

* [[finitely cocomplete category|finitely cocomplete]], 

* and [[cartesian closed category|cartesian closed]].

\end{definition}


The implication $a\Rightarrow b$ is the [[exponential object]] $b^a$. 

\begin{remark}
Insofar as all these properties of a poset are described by [[universal properties]], being a Heyting algebra is a [[property-like structure]] on a poset; a poset can be a Heyting algebra in at most one way. 

\end{remark}

The definition of Heyting algebra may be recast into purely [[algebraic theory|equational form]]: add to the equational theory of lattices the inequalities $(x \Rightarrow y) \wedge x \leq y$ and $y \leq x \Rightarrow (y \wedge x)$, writing these inequalities in equational form via the equivalence $a \leq b$ iff $a = a \wedge b$. Hence we can speak of an __[[internalization|internal]] Heyting algebra__ in any [[cartesian monoidal category|category with products]]. 

\begin{definition}
A Heyting algebra [[homomorphism]] is a homomorphism of the underlying [[lattice]]s that preserve $\Rightarrow$.  Heyting algebras and their homomorphisms form a [[concrete category]] [[HeytAlg]].
\end{definition}


## Properties

\begin{prop}\label{prop:distributive}
Any Heyting algebra is a [[distributive lattice]].
That is, finite meets distribute over finite joins and vice versa.
\end{prop}

\begin{proof}
As discussed at [[distributive lattice]], it suffices to prove the nontrivial direction of either of the two (dual) binary distributivity laws.  We prove that for any $x, y, z$ in a Heyting algebra $H$:
$$ x \wedge (y \vee z) \leq (x \wedge y) \vee (x \wedge z) $$

By the universal property \eqref{UniversalProperty}, this is equivalent to:
$$ y \vee z \leq
   x \Rightarrow \big( (x \wedge y) \vee (x \wedge z) \big) $$
But then by the universal property of $\vee$, this follows from the two inequalities
$$
  \begin{aligned}
    y &\leq
      x \Rightarrow \big( (x \wedge y) \vee (x \wedge z) \big)
    \\
    z &\leq
      x \Rightarrow \big( (x \wedge y) \vee (x \wedge z) \big)
    \,.
  \end{aligned}
$$
These in turn each follow from applying \eqref{UniversalProperty} in the opposite direction.
\end{proof}

The relation of **modus ponens** is immediate from
\eqref{UniversalProperty}: for any $a, b$ in a Heyting algebra,
\[ \label{ModusPonens}
a \wedge (a \Rightarrow b) \leq b
\]

We list some further basic facts which are frequently useful,
including in the proofs below:

\begin{proposition} \label{BasicProperties}
The following hold for any $a, b, c$ in any Heyting algebra:


  1. Composition law:
     $(a \Rightarrow b) \wedge (b \Rightarrow c) \leq a \Rightarrow c$.

  1. Currying:
     $a \wedge b \Rightarrow c =
      a \Rightarrow (b \Rightarrow c)$.

  1. $a \Rightarrow {-}$ is monotone:
     $a \Rightarrow b \leq a \Rightarrow c$ if $b \leq c$.

  1. $a \Rightarrow {-}$ is increasing:
     $b \leq a \Rightarrow b$.

  1. $a \Rightarrow {-}$ is idempotent:
     $a \Rightarrow (a \Rightarrow b) = a \Rightarrow b$.

  1. ${-} \Rightarrow a$ is antimonotone:
     $c \Rightarrow a \leq b \Rightarrow a$ if $b \leq c$.

  1. ${-} \Rightarrow a$ is self-adjoint:
     ${-} \Rightarrow a: L \rightarrow L^{\mathrm{op}}$ is left adjoint
     to ${-} \Rightarrow a: L^{\mathrm{op}} \rightarrow L$.

     Explicitly, $b \leq (c \Rightarrow a)$ just if
     $(b \Rightarrow a) \leq^{\mathrm{op}} c$, i.e. just if
     $c \leq (b \Rightarrow a)$.

  1. $({-} \Rightarrow a) \Rightarrow a$ is increasing:
     $
     b \leq
     (b \Rightarrow a) \Rightarrow a
     $.

  1. $({-} \Rightarrow a) \Rightarrow a$ is idempotent:
     $
     (b \Rightarrow a) \Rightarrow a =
     (((b \Rightarrow a) \Rightarrow a) \Rightarrow a) \Rightarrow a
     $.

\end{proposition}
\begin{proof}
  Each of these is a short exercise using the universal property
  \eqref{UniversalProperty} and modus ponens \eqref{ModusPonens}.
\end{proof}

Most of these facts can be packaged up more abstractly like so:

\begin{proposition}\label{Monads}
  In any Heyting algebra $H$, for any element $a \in H$:

  * $a \Rightarrow {-}$ is a [[monad]].

  * $({-} \Rightarrow a) \Rightarrow a$ is a monad.

\end{proposition}
\begin{proof}
  A monad in a poset (or a [[preorder]], aka [[(0,1)-category]]) like
  $H$ is just a monotone, increasing, idempotent function.

  From Proposition \ref{BasicProperties} it is immediate that
  this describes both $a \Rightarrow {-}$
  and $({-} \Rightarrow a) \Rightarrow a$.
\end{proof}


### Negation

In any Heyting algebra $H$, we may define a [[negation]] operator:

\begin{definition}\label{Negation}
The **negation** operator
$\neg\colon H^{op} \to H$
is $\neg x = (x \Rightarrow 0)$, where $0$ is the bottom element of
the lattice.
\end{definition}

\begin{corollary}\label{DoubleNegationMonad}
$\neg\neg\colon H \to H$ is a [[monad]].
\end{corollary}
\begin{proof}
Immediate from \ref{Monads}.
\end{proof}

We collect some further frequently-useful facts:

\begin{proposition}\label{NegationFacts}
  In any Heyting algebra $H$, we have the following for all $x, y \in H$:

  1. Negation is antimonotone:
     $\neg y \leq \neg x$ if $x \leq y$.

  1. Currying:
     $\neg (x \wedge y) = (x \Rightarrow \neg y)$.

  1. Triple negation is just negation:
     $\neg \neg \neg x = \neg x$.

  1. Proof by contradiction:
     $x \leq \neg y$ just if $x \wedge y \leq 0$.

  1. [[De Morgan's law]] for negation over disjunction:
     $\neg (x \vee y) = \neg x \wedge \neg y$.

  1. One-way De Morgan's law for negation over conjunction:
     $\neg x \vee \neg y \leq \neg (x \wedge y)$.

  1. $x \wedge \neg x = 0$

  1. $\neg \neg (x \vee \neg x) = 1$
     (equivalently, $\neg (x \vee \neg x) = 0$)

  1. $\neg x \vee y \leq x \Rightarrow y$

  1. \[ \label{NegIfEq}
     \neg (x \Rightarrow y) = \neg\neg x \wedge \neg y
     \]

\end{proposition}
\begin{proof}
  Each of these is a short [[exercise]] using the universal property
  \eqref{UniversalProperty}, Proposition \ref{BasicProperties},
  and the preceding properties in the list.
\end{proof}


### Double negation

The double-negation map $\neg\neg \colon H \to H$ on a Heyting algebra
$H$ is often relevant, particularly in the relationship
[with Boolean algebras](#ToBooleanAlgebras).  We saw in
\ref{DoubleNegationMonad} that $\neg\neg$ is a [[monad]].
Further:

\begin{lem}\label{lem:NegnegMeets}
[[double negation|Double negation]] $\neg \neg\colon L \to L$ [[preserved limit|preserves]] [[finite limit|finite]] [[meets]].
\end{lem}

\begin{proof}
Nullary meets are trivial: $\neg \neg 1 = \neg 0 = 1$.
For binary meets, the direction
$\neg \neg (x \wedge y) \leq (\neg \neg x) \wedge (\neg \neg y)$
holds simply because $\neg \neg$ is monotone.

In the other direction, we show
$
(\neg \neg x) \wedge (\neg \neg y) \leq \neg \neg (x \wedge y)
$
by currying (per \ref{NegationFacts}) $\neg (x \wedge y)$ to calculate:
$$
\begin{aligned}
  (\neg \neg x) \wedge (\neg \neg y) \wedge \neg (x \wedge y)
  & =
  (\neg \neg x) \wedge (\neg y \Rightarrow 0) \wedge (x \Rightarrow \neg y)
  \\
  & \leq
  (\neg \neg x) \wedge (x \Rightarrow 0)
  \\
  & =
  (\neg x \Rightarrow 0) \wedge \neg x
  \\
  & \leq
  0
\end{aligned}
$$
where the two inequalities follow from composition
(Proposition \ref{BasicProperties}) and modus ponens \eqref{ModusPonens}.
\end{proof}

The following Lemma \ref{lem:NegnegImplication} is important for the [[double negation translation]].

\begin{lem}\label{lem:NegnegImplication}
[[double negation|Double negation]] $\neg \neg\colon L \to L$ preserves [[implication]]:
$ \neg\neg( a \Rightarrow b ) =
  (\neg\neg a \Rightarrow \neg\neg b) $.
\end{lem}
\begin{proof}
Applying \eqref{NegIfEq} and currying (by \ref{NegationFacts}), we have
$$
 \neg\neg (a \Rightarrow b) =
 \neg ((\neg\neg a) \wedge (\neg b)) =
 (\neg\neg a \Rightarrow (\neg b \Rightarrow 0)) =
 (\neg \neg a \Rightarrow \neg \neg b)
 \; .
$$
\end{proof}




## Relation to other concepts

### To logic

In [[logic]], Heyting algebras are precisely algebraic models for [[intuitionistic logic|intuitionistic]] [[propositional calculus]], just as [[Boolean algebra|Boolean algebras]] model [[classical logic|classical]] propositional calculus. As one might guess from this description, the "law of the [[excluded middle]]" does not generally hold in a Heyting algebra; see the discussion below.

In a [[Heyting category]], every [[subobject poset]] $Sub(A)$ is a Heyting algebra.  In particular, this holds for every [[topos]].  Furthermore, in a topos, the [[power object]] $\mathcal{P}(A)$ is an [[internalisation|internal]] Heyting algebra that corresponds to the external Heyting algebra $Sub(A)$.  In a [[boolean topos]], the internal Heyting algebras are all internal [[boolean algebras]].  In general, however, the [[internal logic]] of a topos (or other Heyting category) is intuitionistic.


### To topology

One of the chief sources of Heyting algebras is given by [[topology|topologies]]. As a poset, the topology of a topological space $X$ is a [[complete lattice]] (it has arbitrary [[joins]] and [[meets]], although the infinitary meets are not in general given by [[intersection]]), and the implication operator is given by 
$$(U \Rightarrow V) = int(U^c \vee V)$$ 
where $U, V$ are open sets, $U^c$ is the set-theoretic complement of $U$, and $int(S)$ denotes the interior of a subset $S \subseteq X$.

Somewhat more generally, a [[frame]] (a [[sup-lattice]] in which finite meets distribute over arbitrary sups) also carries a Heyting algebra structure. In a frame, we may define 
$$(u \Rightarrow v) = \bigvee_{x \wedge u \leq v} x$$ 
and the distributivity property guarantees that the universal property \eqref{UniversalProperty} holds. (The detailed proof is a "baby" application of an [[adjoint functor theorem]].)

Thus frames are extensionally the same thing as _[[complete lattice|complete]] Heyting algebras_. However, _intensionally_ they are quite different; that is, a morphism of frames is not usually a morphism of complete Heyting algebras: they do not preserve the implication operator. 

A [[locale]] is the same thing as a frame, but again the morphisms are different; they are reversed.

Topologies that are [[Boolean algebras]] are the exception rather than the rule; basic examples include topologies of [[Stone spaces]]; see [[Stone duality]]. Another example is the topology of a [[discrete space]] $X$.


### To Boolean algebras 
 {#ToBooleanAlgebras}

A Heyting algebra is [[Boolean algebra|Boolean]] if the [[double negation]]
$\neg \neg\colon L \to L$
(with negation as defined at \ref{Negation})
coincides with the identity map; this gives one of many ways of defining a Boolean algebra. 

In any Heyting algebra $L$, we have for all $a, b \in L$ the inequality 
$$ (\neg a \vee b) \leq (a \Rightarrow b) ,$$ 
and another characterization of Boolean algebra is a Heyting algebra in which this is an equality for all $a, b$. 

There are several ways of passing back and forth between Boolean algebras and Heyting algebras, having to do with the [[double negation]] operator.
By \ref{DoubleNegationMonad}, double negation $\neg \neg\colon L \to L$ is a [[monad]].
Further, by \ref{lem:NegnegMeets}, it [[preserved limit|preserves]] [[finite limit|finite]] [[meets]].

The proof of Lemma \ref{lem:NegnegMeets} can be made purely equational, and is therefore internally valid in any category with products. Applied to the internal Heyting algebra $L = \Omega$ of a [[topos]], that is the [[subobject classifier]], this lemma says exactly that the double negation operator $\neg \neg\colon \Omega \to \Omega$ defines a [[Lawvere–Tierney topology]]. Similarly, we get the [[double negation sublocale]] of any [[locale]].

Now let $L_{\neg\neg}$ denote the poset of _[[regular element]]s_ of $L$, that is, those elements $x$ such that $\neg\neg x = x$. (When $L$ is the topology of a space, an open set $U$ is [[regular open subspace|regular]] if and only if it is the interior of its closure, that is if it is a regular element of the Heyting algebra of open sets described above.) With the help of Lemma \ref{lem:NegnegMeets}, we may prove

\begin{thm}\label{thm:NegnegAdjoint}
The poset $L_{\neg\neg}$ is a Boolean algebra. Moreover, the assignment $L \mapsto L_{\neg\neg}$ is the object part of a functor 
$$F\colon Heyt \to Bool$$
called _Booleanization_, which is left adjoint to the full and faithful inclusion 
$$i\colon Bool \hookrightarrow Heyt.$$
The unit of the [[adjoint functor|adjunction]], applied to a Heyting algebra $L$, is the map $L \to L_{\neg\neg}$ which maps each element $x$ to its _[[regular element|regularization]]_ $\neg\neg x$.
\end{thm}

Thus $\neg\neg\colon L \to L_{\neg\neg}$ preserves finite joins and finite meets and implication. In the other direction, we have an inclusion $i\colon L_{\neg\neg} \to L$, and this preserves meets but not joins. It also preserves negations; more generally and perhaps surprisingly, it preserves implications as well. 

Regular elements are not to be confused with _[[complemented element]]s_, i.e., elements $x$ in a Heyting algebra such that $x \vee \neg x = 1$, although it is true that every complemented element is regular. An example of a regular element which is not complemented is given by the unit interval $(0, 1)$ as an element of the topology of $\mathbb{R}$; a complemented element in a Heyting algebra given by a topology is the same as a [[clopen subset]]. 

Complemented elements furnish another universal relation between Boolean algebras and Heyting algebras: the set of complemented elements in a Heyting algebra $H$ is a Boolean algebra $Comp(H)$, and the inclusion $Comp(H) \to H$ is a Heyting algebra map which is universal among Heyting algebra maps $B \to H$ out of Boolean algebras $B$. In other words, we have the following result.  

\begin{thm}\label{thm:CompAdjoint}
The assignment $H \mapsto Comp(H)$ is the object part of a right adjoint to the forgetful functor $Bool \to Heyt$. 
\end{thm}


#### Proofs
{#proofs}

We prove the theorems of the preceding section.

\begin{proof}
(Proof of Theorem \ref{thm:NegnegAdjoint}.)
Since $\neg \neg$ is a monad, and $L_{\neg \neg}$ is the corresponding category (poset) of $\neg \neg$-algebras, the left adjoint $\neg \neg \colon L \to L_{\neg \neg}$ preserves joins; and by Lemma \ref{lem:NegnegMeets}, it preserves finite meets. Thus $L \to L_{\neg\neg}$ is a surjective lattice map, and it follows that $L_{\neg\neg}$ is distributive because (by Proposition \ref{prop:distributive}) $L$ is.

For any $x \in L$, we have $x \leq \neg \neg x$ because $\neg \neg$ is a monad, hence $\neg \neg \neg x \leq \neg x$ because $\neg$ is antimonotone, so $\neg x$ is fixed by $\neg \neg$ and is in $L_{\neg \neg}$.

Then working in $L_{\neg \neg}$ (where the join will be written $\vee_{\neg\neg}$ and the meet $\wedge_{\neg\neg}$), we have for any $x \in L_{\neg \neg}$ the equations
$$
\begin{aligned}
x \vee_{\neg \neg} \neg x
& = \neg \neg (x \vee \neg x) = \neg (\neg x \wedge \neg \neg x) = \neg 0 = 1
\\
x \wedge_{\neg\neg} \neg x
& = x \wedge \neg x = 0
\end{aligned}
$$
so that $\neg x$ is the complement of $x \in L_{\neg \neg}$. We have thus shown that $L_{\neg\neg}$ is a complemented distributive lattice, i.e., a Boolean algebra. This calculation also shows that $\neg\neg \colon L \to L_{\neg\neg}$ preserves negation. 

To show $L \to L_{\neg\neg}$ preserves implication, we may start from the observation (in Proposition \ref{NegationFacts}) that in any Heyting algebra $L$, we have 

$$\neg(a \Rightarrow b) = (\neg \neg a) \wedge (\neg b).$$ 

Then 

$$\array{
\neg \neg(a \Rightarrow b) & = & \neg((\neg \neg a) \wedge (\neg b)) \\ 
 & = & \neg ((\neg \neg a) \wedge (\neg \neg \neg b)) \\
 & = & \neg \neg ((\neg a) \vee (\neg \neg b)) \\
 & = & \neg a \vee_{\neg \neg} (\neg \neg b) \\
 & = & \neg (\neg \neg a) \vee_{\neg \neg} (\neg \neg b)
}$$ 

where the last expression is $(\neg \neg a) \Rightarrow (\neg \neg b)$ as computed in the Boolean algebra $L_{\neg \neg}$, since in a Boolean algebra we have $(x \Rightarrow y) = (\neg x \vee y)$. 

Therefore $L \to L_{\neg\neg}$ is a Heyting algebra quotient which is the coequalizer of $1, \neg\neg \colon L \stackrel{\to}{\to} L$. It follows that a Heyting algebra map $L \to B$ to any Boolean algebra $B$ factors uniquely through this coequalizer, and the induced map $L_{\neg \neg} \to B$ is a Boolean algebra map. In other words, $L \to L_{\neg\neg}$ is the universal Heyting algebra map to a Boolean algebra, which establishes the adjunction. 
\end{proof}

\begin{proof}
(Proof of Theorem \ref{thm:CompAdjoint}.)
In a Heyting algebra $H$, the elements $0$ and $1$ are clearly complemented. If $x$ and $y$ are complemented, then so is $x \wedge y$ since 

$$1 = 1 \wedge 1 = (x \vee \neg x \vee \neg y) \wedge (y \vee \neg x \vee \neg y) = (x \wedge y) \vee (\neg x \vee \neg y)$$ 

$$\,$$ 

$$(x \wedge y) \wedge (\neg x \vee \neg y) = (x \wedge y \wedge \neg x) \vee (x \wedge y \wedge \neg y) = 0 \vee 0 = 0.$$ 

By a similar proof, $x \vee y$ is complemented. Finally, $x \Rightarrow y$ has complement $x \wedge \neg y$: writing $x \Rightarrow y = y^x$ for typographical clarity, we have 

$$1 = 1 \wedge 1 = (\neg x \vee x) \wedge (y \vee \neg y) \leq (y^x \vee x) \wedge (y^x \vee \neg y) = y^x \vee (x \wedge \neg y),$$ 

$$\,$$ 

$$y^x \wedge x \wedge \neg y \leq y \wedge \neg y = 0.$$ 

Thus the complemented elements form a Heyting subalgebra $Comp(H) \hookrightarrow H$. Clearly $Comp(H)$ is a Boolean algebra, and clearly if $B$ is Boolean, then any Heyting algebra map $B \to H$ factors uniquely through $Comp(H) \hookrightarrow H$. This proves the theorem. 
\end{proof}


### To toposes

An [[elementary topos]] is a [[vertical categorification]] of a Heyting algebra: the notion of Heyting algebra is essentially equivalent to that of [[(0,1)-topos]].  Note that a [[Grothendieck topos|Grothendieck]] $(0,1)$-topos is a [[frame]] or [[locale]].


## Examples

+-- {: .num_prop}
###### Proposition

For $\mathcal{T}$ a [[topos]] and $X \in \mathcal{T}$ any [[object]], the poset $Sub(X)$ of [[subobject]]s of $X$ is a Heyting algebra.

In other words, every topos is a [[Heyting category]].
=--

In particular for $X = \Omega$ the [[subobject classifier]], $Sub(\Omega)$ is a Heyting algebra.

In $\mathcal{T} =$ [[Set]] for every set $S$ we have that $Sub(S)$ is the [[Boolean algebra]] of subset of $S$.

More details and examples are spelled out at [[internal logic]]. 

+-- {: .num_prop} 
###### Proposition 
A [[frame]] $L$ is a Heyting algebra. 
=-- 

+-- {: .proof} 
###### Proof 
By the [[adjoint functor theorem]], a right adjoint $x \Rightarrow -$ to the map $x \wedge -: L \to L$ exists since this map preserves arbitrary joins. 
=-- 

## See also

* [[Heyting algebra object]]
* [[locally Heyting-algebraic 2-poset]]

## References

The original reference is

* [[Arend Heyting]],
_Die formalen Regeln der intuitionistischen Logik. I, II, III._
Sitzungsberichte der Preußischen Akademie der Wissenschaften, Physikalisch-Mathematische Klasse (1930), 42-56, 57-71, 158-169.
 

A quick introduction can be found in §1.2 of

* [[Francis Borceux]],
_[[Handbook of Categorical Algebra]] 3.  Categories of sheaves_,
Cambridge University Press 1994.
ISBN: 0521441803.

[[!redirects Heyting algebra]]
[[!redirects Heyting algebras]]