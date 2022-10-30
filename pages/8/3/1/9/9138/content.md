
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

> Caveat: There is an unrelated notion of "effect of a computation"; that is rather in proximity to the entry [[monad (in computer science)]].

#Contents#
* table of contents
{:toc}


## Idea

In [[quantum mechanics]] a [[self-adjoint operator]] $A$ on the given [[Hilbert space]] such that its [[spectrum of an operator|spectrum]] lies between 0 and 1 (hence a [[positive operator]] which is $\leq 1$) is sometimes called an _effect_ or _quantum effect_ (see e.g. ([Ludwig](#Ludwig), [Kraus](#Kraus))). These operators generalize [[projection operators]] and may be thought of as [[quantum observables]] with "unsharp" or "fuzzy" value. 

The notion of _effect algebra_ (due to ([Foulis-Bennet 94](#FoulisBennet))) is an abstraction of the structure exhibited by the collection of such effect operators. 

## Definition

+-- {: .num_defn}
###### Definition

A [[partial monoid|partial commutative monoid]] (PCM) consists of a set $M$ with a zero element $0 \in  M$ and a partial binary operation $\vee : M \times M \to M$ satisfying the three requirements below. They involve the notation $x \perp y$ for: $x \vee y$ is defined; in that case $x, y$ are called orthogonal.

1. Commutativity: $x\perp y$ implies $y\perp x$ and $x\vee y=y\vee x$.

1. Associativity: $y\perp z$ and $x\perp(y\vee z)$ implies $x\perp y$ and $(x\vee y)\perp z$ and $x\vee (y\vee z)=(x\vee y)\vee z$.

1. Zero: $0\perp x$ and $0\vee x=x$

([Foulis-Bennet 94](#FoulisBennet) p.22)

In a PCM, we define: $x \le y:\Leftrightarrow \exists_z. x \vee z = y$.  This is a preorder on any PCM.
=--

+-- {: .num_prop}
###### Proposition
A PCM is preordered by $\le$.
=--

+-- {: .proof}
###### Proof
Reflexivity is immediate from the Zero axiom, and transitivity follows easily from Associativity.
=--

+-- {: .num_defn}
###### Definition
A *generalized effect algebra* is a PCM $(E, 0, \vee)$ such that:

1. Cancellation Law: If $a \perp b$, $a \perp c$ and $a \vee b = a \vee c$ then $b = c$.

2. Positivity Law: If $a \perp b$ and $a \vee b = 0$ then $a = b = 0$.

In a generalized effect algebra, we define: $y\ominus x=z:\Leftrightarrow y=x\vee z$ (which exists iff $x \le y$, and is unique by the Cancellation Law).
=--

+-- {: .num_prop}
###### Proposition
A generalized effect algebra is partially ordered by $\le$.
=--

+-- {: .proof}
###### Proof
Suppose $x \le y$ and $y \le x$.  Let $x \vee a = y$ and $y \vee b = x$.  Then $x \vee (a \vee b) = x = x \vee 0$, and so $a \vee b = 0$ by the Cancellation Law.  Therefore, $a = b = 0$ and so $x = y$.
=--

+-- {: .num_defn}
###### Definition
An *effect algebra* is a PCM $(E,0,\vee)$ with an orthocomplement. The latter is a unary operation $(-)^\perp :E\to E$ satisfying:

1. Orthocomplement Law. $x^\perp\in E$ is the unique element in $E$ with $x\vee x^\perp=1$, where $1=0^\perp$.

2. Zero-One Law.  $x\perp 1\Rightarrow x=0$.

For such an effect algebra one defines: $x\wedge y:=(x^\perp\vee y^\perp)^\perp$ 
 ([Foulis-Bennet 94](#FoulisBennet) p. 23)
=--

+-- {: .num_prop}
###### Proposition
A structure $(E, 0, \vee)$ is an effect algebra iff it is a generalized effect algebra with a greatest element, in which case that greatest element is $1 = 0^\perp$.
=--

+-- {: .proof}
###### Proof

Let $(E, 0, \vee)$ be an effect algebra.  Then $E$ is a generalized effect algebra since:

1. Cancellation Law.  If $a \vee b = a \vee c$ then $a \vee b \vee (a \vee b)^\perp = a \vee c \vee (a \vee b)^\perp = 1$, and so $b = c = (a \vee (a \vee b)^\perp)^\perp$.

2. Positivity Law.  If $a \vee b = 0$ then $(a \vee b) \perp 1$, hence $a \perp 1$ and $b \perp 1$ by Associativity.  Thus, $a = b = 0$ by the Zero-One Law.

1 is the greatest elements since, for any $x$, we have $x \vee x^\perp = 1$ and so $x \leq 1$.

Conversely, let $(E, 0, \vee)$ be a generalized effect algebra with greatest element 1.  Define $x^\perp = 1 \ominus x$ for all $x$.  Then:

1. Orthocomplement Law. $x^\perp$ is the unique element such that $x \vee x^\perp = 1$ by definition.

2. Zero-One Law.  If $x \perp 1$, then $1 \leq x \vee 1$, so $x \vee 1 = 1$.  Thus, $x \vee 1 = 0 \vee 1$, and so $x = 0$ by the Cancellation Law.
=--

+-- {: .num_remark}
###### Remark
If we consider $(-)\ominus y:up(y)\to down(y^\perp)$ and $(-)\vee y:down(y^\perp)\to up$ as functors between [[posets]] we have [[adjunctions]]

$$((-\wedge y)\dashv (-\ominus y)\dashv (-\wedge y)$$

Hence these functors are a [[Frobenius functor|frobenius pair]].

 ([Foulis-Bennet 94](#FoulisBennet) p.25)
=--

## Morphisms

+-- {: .num_defn}
###### Definition
Let $E$ and $F$ be effect algebras.
A *morphism of effect algebras* $f : E \rightarrow F$ is a function such that:

1. f(1) = 1

2. If $x \perp y$ then $f(x) \perp f(y)$ and $f(x \vee y) = f(x) \vee f(y)$.

We write $\mathbf{EA}$ for the category of effect algebras and morphisms of effect algebras.
=--

## Examples


(1) [[effect algebra of predicates]]

(2) The real unit inteval $[0,1]$ with $\vee$ being addition of real numbers is an effect algebra since $[0,1]$ is a pcm with zero object $0$ and commutative, associative addition of real numbers and $x\perp y$ iff $x+y\le 1$. The orthocomplement of $x\in [0,1]$ is given by $\x^\perp=1-x$.

(3) Let $D$ denote the discrete-probability-distribution [[monad]] on $Set$ which sends a set $X$ to the collection

$$D(X):=\{r_1 x_1+\dots +r_n x_n|x_i\in X, r_i\in [0,1], \Sigma_i r_i=1\}$$

of formal convex combinations of elements of $X$ and let $Kl(D)$ denote the [[Kleisli category]] of $D$ which has as objects (just) sets and a morphism $f:X\to Y$ in $Kl(D)$ is a function $f:X\to D(Y)$ which can be interpreted as a [[Markov chain]] where the [[probability]] of the transition $x\to x_i$ is the coefficient $r_i\in [0,1]$ in the the convex sum $f(x)=r_1 x_1+\dots+r_n x_n$. $Kl(D)$ has as coproducts coproducts of $Set$. A predicate on $X\in Kl(D) $is hence a function $p:X\to D(X+X)$ and $[id_X,id_X]\circ p =id_X$ means that $p(x)\in D(X+X)$ is a convex combination of elements of the form $k_1 x, k_2 x\in X+X$ such that we have $p(x)=\varphi(x)k_1 x +\psi(x)k_2 x$ with $\varphi(x),\psi(x)\in [0,1]$ such that $\varphi{x}+\psi(x)=1$. Hence $p(x)$ can be written as $p(x)=\varphi(x)k_1 x + (1-\varphi(x))k_2 x$. In particular a predicate is (uniquely determined by) a function $\varphi:X\to [0,1]$ to the [[unit interval]]. In this view the orthocomplemet of $\varphi(x)$ is the function $x\mapsto 1-\varphi(x)$ which is point-wise the orthocomplement of the unit interval in the second example.

(4) In the category $Hilb$ of [[Hilbert space|Hilbert spaces]] the coproduct coincides with the product and hence is a [[biproduct]]. In this case a predicate $p:X\to X\otimes X$ on a Hilbert space $X$ has the form $p=\lt p_1,p_2\gt$ of a pair of maps and   $[id_X,id_X]\circ p$ is equivalent to $p_1 +p_2=id_X$ where $+$ is point-wise addition. In particular $p_1$ and $p_2$ determine each other uniquely.

And now comes the eponymous feature: The category $Hilb$ is a [[dagger category]] and the dagger morphism $(-)^\dagger:Hilb^{op}\to Hilb$ is the identity on objects and complex conjugation on morphisms. An endomorphism $f:X\to X$ is called to be a *positive endomorphism* if there is a $g$ such that $f=g^\dagger\circ g$ and a predicate on $X$ is called to be an **effect** (on $X$) if $p_1$ and $p_2$ are positive. Another name for effect is "unsharp predicate"; in this terminology a "sharp predicate" is a subset of the set of projections onto $X$.

(5) In a C$^\ast$-algebra the elements between 0 and 1 form an effect algebra with $(1-a)$ as the complement of $a$.

(6) As a special case, we obtain the effect algebra of a [[von Neumann algebra]]. In general, this is not a lattice. [De Groote](#DeGroote) defines a _spectral order_ on self-adjoint operators which makes the collection of effects a [[boundedly complete lattice]]. However, this is not the canonical order on an effect algebra, as defined above.

## Relation to D-Posets

A parallel concept in the literature is that of _D-poset_ (sometimes called _D-lattice_), originally introduced for the same purpose of studying fuzzy or quantum logics. These first appeared in [Kôpka 92](#Kopka) [Chovanec-Kôpka 95](#ChovKop).

+-- {: .num_defn}
###### Definition
A partial binary operation $\ominus$ on a poset $(P, \leq)$ is called a _difference operation_ (or simply _difference_) on $P$ iff:

(1) $a \leq b \leftrightarrow b \ominus a$ is defined,

(2) $b \ominus a \leq b$,

(3) $b \ominus (b \ominus a) = a$,

(4) if $a \leq b \leq c$ implies that $c \ominus b \leq c \ominus a$ and $(c \ominus a) \ominus (c \ominus  b) = b \ominus a$.

A _D-poset_ is a poset $(P, \leq, \ominus, 1)$ with a difference operation and greatest element $1 \in P$.
=--

Any effect algebra is automatically a D-poset under the difference $c := b \ominus a \iff a \oplus c = b$, well-defined by the cancellation property of generalized effect algebras. Ultimately this determines an isomorphism of categories between D-posets and effect algebras.


## Related concepts

* [[separation algebra]]

[[!include states and observables -- content]]


## Reference

Quantum effect operators are discussed for instance in 

* G. Ludwig, _Foundations of Quantum Mechanics I_ Springer Verlag, New York, (1983)
 {#Ludwig}

* K. Kraus, _States, Effects, and Operations_ Springer Verlag, Berlin, (1983)
 {#Kraus}

The notion of effect algebra is due to

* D. J. Foulis, M. K. Bennet, _Effect algebras and unsharp quantum logics_, Found. Phys. 24 (1994), 1 331&#8211;1 352.
 {#FoulisBennet}

Discussion of effect algebras in the context of [[categorical logic]] is in

* [[Bart Jacobs]], _New Directions in Categorical Logic, for Classical, Probabilistic and Quantum Logic_, (2012) ([arXiv:1205.3940 ](http://arxiv.org/abs/1205.3940))
 {#Jacobs}

Discussion in the context of [[quantum logic]] is in section 6 of 

* Gianpiero Cattaneo, Maria Luisa Dalla Chiara, Roberto
Giuntini and Francesco Paoli, _Quantum Logic and Nonclassical Logics_, p. 127 in  Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland
  {#CCGP09}

A survey of the use of effect algebras in [[quantum mechanics]] is in 

* Teiko Heinosaari, Mario Ziman, _Guide to Mathematical Concepts of Quantum Theory_ ([arXiv:0810.3536](http://arxiv.org/abs/0810.3536))

  also appeared as:

  _The Mathematical Language of Quantum Theory_, Cambridge University Press (2011)

* Hans de Groote, _On a canonical lattice structure on the effect algebra of a von Neumann algebra_ [arXiv:0410018](http://arxiv.org/abs/math-ph/0410018){#DeGroote}

Discussion in relation to [[presheaves]] on [[FinSet]]${}^{op}$ (hence in the [[classifying topos]] for objects) is in

* Sam Staton, Sander Uijlen, _Effect algebras, presheaves, non-locality and contextuality_ ([pdf](http://www.cs.ru.nl/S.Uijlen/ICALP-camera-ready.pdf))

D-posets were first introduced in:

* F. Kôpka,_D-posets of fuzzy sets_, Tatra Mountains Mathematical Publications, vol. 1, no. 1, pp. 83-87, 1992. {#Kopka}

* F. Chovanec and F. Kôpka, _D-lattices_, International Journal of
Theoretical Physics, vol. 34, no. 8, pp. 1297–1302, 1995. {#ChovKop}


[[!redirects effect algebras]]

[[!redirects effect]]
[[!redirects effects]]

[[!redirects quantum effect]]
[[!redirects quantum effects]]
[[!redirects effect algebra]]