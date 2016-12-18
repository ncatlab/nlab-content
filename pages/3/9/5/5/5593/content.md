
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

* For $A \in Op(X)$, we write $C[A] = E_C[A]$ (see above definition).  If $A$ is overt (such as if $X$ is overt, such as if [[excluded middle]] holds), this is equivalent to $\bigcup \{ B \in C \;|\; A \cap B$ is [[positive element|positive]] $}$.

* $C^* \coloneqq \{ C[A] \;|\; A \in C\}$.

We now define a **covering uniformity** on a locale $X$ to be a collection of covers, called **[[uniform covers]]**, such that

1. There exists a uniform cover; in light of axiom (4), it follows that the cover $\{X\}$ is a uniform cover.

2. If $C$ is a uniform cover, there exists a uniform cover $C'$ such that $(C')^* \prec C$.

3. If $C_1, C_2$ are uniform covers, so is some cover that refines $C_1 \wedge C_2$. In light of axiom (4), it follows that $C_1 \wedge C_2$ is a uniform cover.

4. If $C$ is a uniform cover and $C \prec C'$, then $C'$ is a uniform cover.

5. For any open part $A\in Op(X)$, we have
   $$ A = \bigvee \{ B | \exists \;\text{ a uniform cover }\; C \;\text{ such that }\; C[B] \le A \} $$

The last condition is the one saying that "the induced topology is again the topology of $X$."; the other conditions correspond precisely to the [uniform-cover definition](uniform+space#ucov) of a uniform topological space.


### Entourage uniformities

An **entourage uniformity** on a locale $X$ consists of a collection of open parts $E\in Op(X\times X)$, called [open] *[[entourages]]*, such that:

1. There exists an entourage (in light of axiom 4 below, it follows that $X\times X$ is an entourage)

2. For any entourage $E$, there exists an entourage $F$ such that $F\circ F \subseteq E$, and an entourage $G$ such that $G\subseteq E^{-1}$.  (In light of axiom 4 below, it follows that $E^{-1}$ is itself an entourage.)  Note that $F\circ F$ is in general only a sublocale (not necessarily open), but we can still ask it to be contained in the open sublocale $E$.

3. If $E$ and $F$ are entourages, then so is some open part contained in $E\cap F$ (in light of axiom 4 below, it follows that $E\cap F$ is itself an entourage)

4. If $E$ is an entourage and $E\subseteq F$, then $F$ is also an entourage.

5. For any $U\in Op(X)$ we have $U = \bigcup \{ V\in Op(X) \mid E[V] \subseteq U \text{ for some entourage } E\}$.

It is not clear whether these definitions are equivalent.  Most references (see below) use only covering uniformities, although [Johnstone 89](#Johnstone89) promises an equivalence to entourage uniformities in a future paper.


## References

This paper developes covering uniformities constructively, and includes citations to several other papers that do it classically:

* [[Peter Johnstone]], 1989; A constructive theory of uniform locales. I. Uniform covers; General topology and applications, 179--193; Lecture Notes in Pure and Applied Mathematics 134 (1991).
 {#Johnstone89}

A constructive and predicative theory in the programme of [[formal topology]] can be found here:

* [[Giovanni Curi]]; On the collection of points of a formal space; Annals of Pure and Applied Logic 137 (2006) 1--3, 126--146.

* [[Giovanni Curi]]; Constructive metrisability in point-free topology; Theoretical Computer Science 305 (2003) 1--3, 85--109.

But we have not read these yet.


[[!redirects uniform locale]]
[[!redirects uniform locales]]

[[!redirects pointless uniformity]]
[[!redirects pointless uniformities]]
