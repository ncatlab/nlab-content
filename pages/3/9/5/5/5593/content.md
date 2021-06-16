
# Uniform Locales
* table of contents
{: toc}

## Idea

A **uniform locale** is to a [[uniform space]] as a [[locale]] is to a [[topological space]].


## Definition

While an ordinary uniform space is defined directly in terms of subsets, and the underlying topology then constructed secondarily, in the absence of an underlying set it seems more convenient to define a uniform locale as additional structure on a given locale, together with an additional axiom which essentially says "the underlying topology is the same as the one we started with."


### Basic notions

For any $E\in Op(X\times X)$ and any [[sublocale]] $A$ of $X$, with inclusion map $i:A\to X$, we write $E[A]$ for the image of $(i\times 1)^*(E)$ of $A\times X$ under the projection $A\times X \to X$.  If $A$ is [[overt space|overt]] (such as if $A$ is an open part of $X$ and $X$ is overt, or if [[excluded middle]] holds), then $E[A]$ is an open part of $X$, and can equivalently be defined as $\bigvee \{ V\in Op(X) \mid Pos(V\cap A) \}$, where $Pos(W)$ means "$W$ is [[positive element|positive]]".  Otherwise, it is merely a sublocale.

Similarly, if $E,F\in Op(X\times X)$, we write $E\circ F$ for the image of $\pi_{23}^*(E) \cap \pi_{12}^*(F)$ under the projection $\pi_{13}:X\times X\times X\to X\times X$.  If $X$ is overt, this is an open part of $X\times X$; otherwise it is merely a sublocale.  We also write $E^{-1}$ for the pullback of $E$ along the twist map $X\times X \cong X\times X$.


### Covering uniformities

An [open] **[[open cover|cover]]** of a locale $X$ is a collection $C \subseteq Op(X)$ of open parts of $X$ whose [[join]] is $X$.  For covers $C_i$, we define:

* $C_1$ **refines** $C_2$, written $C_1 \prec C_2$, if every element of $C_1$ is $\le$ in some element of $C_2$.

* $C_1 \wedge C_2 \coloneqq \{ A \wedge B \;|\; A \in C_1, B \in C_2 \}$; this is also a cover.

* $E_C = \bigcup \{ U\times U \mid U\in C \}$, and $C[A] = E_C[A]$.

* For $A \in Op(X)$, we write $C[A] = E_C[A]$ (see above definition).  If $A$ is overt (such as if $X$ is overt, such as if [[excluded middle]] holds), this is equivalent to $\bigvee \{ B \in C \;|\; A \cap B \text{ is positive } \}$, where positive is in the sense of [[positive element]].

* $C^* \coloneqq \{ C[A] \;|\; A \in C\}$.

We now define a **covering uniformity** on a locale $X$ to be a collection of covers, called **[[uniform covers]]**, such that

1. If $C$ is a uniform cover and $C \prec C'$, then $C'$ is a uniform cover.

2. The cover $\{X\}$ is a uniform cover
and if $C_1, C_2$ are uniform covers, then so is $C_1 \wedge C_2$.

3. If $C$ is a uniform cover, there exists a uniform cover $C'$ such that $(C')^* \prec C$.

4. The collection of uniform covers is __admissible__:
for any open part $A\in Op(X)$, we have
   $$ A = \bigvee \{ B | \exists \;\text{ a uniform cover }\; C \;\text{ such that }\; C[B] \le A \} $$

The last condition is the one saying that "the induced topology is again the topology of $X$."; the other conditions correspond precisely to the [uniform-cover definition](uniform+space#ucov) of a uniform topological space.


### Entourage uniformities

An __entourage__ (Picado and Pultr, Section XII.1.1)
is an open part $E\in Op(X\times X)$
such that $\{u\in Op(X)\mid u\times u\le E\}$
is an open cover of $X$.

An **entourage uniformity** (Picado and Pultr, Section XII.2.3) on a locale $X$ is a collection of [[entourages]] such that:

1. If $E$ is an entourage and $E\subseteq F$, then $F$ is also an entourage.

2. The open part $X\times X$ is an entourage
and if $E$ and $F$ are entourages, then so is $E\cap F$.

3. If $E$ is an entourage, then so is $E^{-1}$.

4. For any entourage $E$, there exists an entourage $F$ such that $F\circ F \subseteq E$.  The sublocale $F\circ F$ is not always open, but we can still ask it to be contained in the open sublocale $E$.

5. The collection of uniform entourages is __admissible__:
for any $U\in Op(X)$ we have $U = \bigvee \{ V\in Op(X) \mid E[V] \subseteq U \text{ for some uniform entourage } E\}$.

### From entourage uniformities to covering uniformities

Given an entourage $E$ on a locale $L$, we define an open cover $U_E$ by setting
$$U_E=\{x\in L\mid x\times x\subset E\}.$$

Given an entourage uniformity $\{E_i\}_i$, we construct
a covering uniformity out of it by taking all open covers $V$
that are refined by some $U_{E_i}$.

### From covering uniformities to entourage uniformities

Given an open cover $U$, we construct an entourage $E_U$
by setting $$E_U=\bigvee_{x\in U}x\times x.$$

Given a covering uniformity $\{U^i\}_i$, we construct an entourage uniformity
out of it by taking all entourages $E$ that contain some $E_{U^i}$.

### Equivalence between covering uniformities and entourage uniformities

Theorem XII.3.3.4 in Picado and Pultr shows that the above correspondence is bijective.  Furthermore, the categories of entourage uniform locales
and covering uniform locales are equivalent (Corollary XII.3.4.3 in the cited book).  However, since their book uses [[classical logic]] throughout, it is not entirely clear whether the same equivalence holds constructively.

## Properties

### Uniformizability

A [[locale]] admits a uniformity if and only if it is [[completely regular]]
(\cite[Theorem 2.8.2]{PP}).

### Fine uniformity

Uniformities are closed under unions,
so any [[completely regular]] [[locale]] admits a largest uniformity,
the __fine uniformity__.

The fine uniformity consists of all [[normal covers]] (alias [[numerable covers]]),
where a cover $U$ is __normal__
if there is a sequence of covers $\{U_n\}_{n\ge0}$
such that $U=U_0$ and $U_{n+1}U_{n+1}$ refines $U_n$.

### Compact regular locale

On a [[compact]] [[regular]] [[locale]] the system
of all covers forms a uniformity.
Maps out of [[compact regular locales]]
are automatically uniform.

### Complete uniform locales

A uniform locale $L$ is __complete__
if every dense uniform embedding $L\to X$
is an isomorphism of uniform locales.

The category of complete uniform locales
is a [[reflective subcategory]] of uniform locales.
The reflection functor is known as the __completion__ functor.

Concretely, the completion of a uniform locale $L$
with a system of uniform covers $A$
can be described as follows.
Its opens are downward-closed subsets $U$
of the underlying [[frame]] of $L$
that satisfy the following saturation conditions:

* If for some $a\in L$ we have $\{x\in L\mid x\lt_A a\}\subset U$,
then also $a\in U$.
Here $x\lt_A a$ means that there is $C\in A$
such that $C[x]\le a$.

* If for some $C\in A$ and $a\in L$ we have $a\wedge C\subset U$,
then also $a\in U$.

## Criteria for completeness

Every compact regular locale is complete.
The fine uniformity on a [[paracompact locale]] is complete.

Isbell's theorem states that a [[locale]] is [[paracompact]]
if and only if it admits a complete uniformity.

A [[completely regular]] [[locale]] is [[compact]]
if and only if it admits a complete uniformity
that has a basis in which all covers are finite.


## References


A detailed treatment of uniform locales can be fund in

* {#PP} [[Jorge Picado]], [[Aleš Pultr]], _[[Frames and Locales]]_.


The following paper developes covering uniformities constructively, and includes citations to several other papers that do it classically:

* [[Peter Johnstone]], 1989; A constructive theory of uniform locales. I. Uniform covers; General topology and applications, 179--193; Lecture Notes in Pure and Applied Mathematics 134 (1991).
 {#Johnstone89}

These ideas are developed further in

* Graham Manuell, _Uniform locales and their constructive aspects_, [arxiv:2106.00678](https://arxiv.org/abs/2106.00678)

A constructive and predicative theory in the programme of [[formal topology]] can be found here:

* [[Giovanni Curi]]; On the collection of points of a formal space; Annals of Pure and Applied Logic 137 (2006) 1--3, 126--146.

* [[Giovanni Curi]]; Constructive metrisability in point-free topology; Theoretical Computer Science 305 (2003) 1--3, 85--109.


[[!redirects uniform locale]]
[[!redirects uniform locales]]

[[!redirects pointless uniformity]]
[[!redirects pointless uniformities]]

[[!redirects complete uniformity]]
[[!redirects complete uniformities]]

[[!redirects fine uniformity]]
[[!redirects fine uniformities]]