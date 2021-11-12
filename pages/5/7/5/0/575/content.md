
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Galois connections
* table of contents
{: toc}


## Idea
 {#Idea}

In [[order theory]] the term *Galois connection* (due to [Ore 44](#Ore44), who spelled it "connexion") can mean both: "[[adjunction]] between [[posets]]" and "[[dual adjunction]] between [[posets]]"; the former notion is sometimes called "monotone Galois connection" and the latter "antitone Galois connection". In this article the term "Galois connection" shall mean "[[dual adjunction]] between [[posets]]".

The term _Galois correspondence_ is also in use. For some authors it is synonymous to "Galois connection", others reserve it for its restriction to its [[fixed point of an adjunction|fixed points]], where it becomes an [[adjoint equivalence]].

The example that gives the concept its name is the relation between [[subgroups]] and [[subfields]] in [[Galois theory]] (see [below](#GaloisTheory)), but adjunctions between posets, hence Galois connections, appear also in many other and entirely different contexts, see further [below](#Examples).

## Definition
 {#Definition}


Given [[posets]] $A$ and $B$, a __Galois connection__ between $A$ and $B$ is a pair of order-reversing [[functions]] $f \colon A\to B$ and $g \colon B\to A$ such that $a\le g(f(a))$ and $b\le f(g(b))$ for all $a\in A$, $b\in B$.

A **Galois correspondence** is a Galois connection which is an [[adjoint equivalence]] (so $a = g(f(a))$ and $b = f(g(b))$ for all $a \in A$, $b \in B$). 

+-- {: .num_prop} 
###### Proposition 
Any Galois connection $f: A \to B$, $g: B \to A$ induces a Galois correspondence between $f(A)$ and $g(B)$, given by the composites $g(B) \hookrightarrow A \stackrel{f}{\to} f(A)$ and $f(A) \hookrightarrow B \stackrel{g}{\to} g(B)$. 
=-- 

+-- {: .proof} 
###### Proof 
For any $a \in A$ of the form $a = g(b)$, we have $a \leq (g \circ f)(a)$ and also $(g \circ f)(a) = g(f(g(b))) \leq g(b) = a$ where the inequality follows from $b \leq f(g(b))$ and antitonicity of $g$. Hence $(g \circ f)(a) = a$ for all $a \in g(B)$. Similarly $(f \circ g)(b) = b$ for all $b \in f(A)$. 
=-- 


## Examples
  {#Examples}

### Galois theory
  {#GaloisTheory}

The [[Galois theory]] normally taught in graduate-level algebra courses (and based on the work of [[Évariste Galois]]) involves a Galois connection between the intermediate [[fields]] of a [[Galois extension]] and the subgroups of the corresponding [[Galois group]].


### Galois connections induced from a relation
 {#InducedFromARelation}

Frequently Galois connections between collections of [[subsets]] ([[power sets]]) arise where $f(a)$ is "the set of all $y$ standing in some relation to every $x\in a$" and dually $g(b)$ is "the set of all $x$ standing in some relation to every $y\in b$."  

Examples of this class of Galois connections include the following

* **(Zariski topology)** The [[closed subsets]] in the [[Zariski topology]] on [[affine space]] $k^n$ or on the set of [[maximal ideals]] of a [[polynomial ring]], which may be understood as the [[fixed point of an adjunction|fixed points]]  of a Galois connection between [[polynomials]] and [[affine space]]/[[maximal ideal]]. This is discussed at _[Zariski topology -- In terms of Galois connections](Zariski+topology#InTermsOfGaloisConnections)_.

* **(orthogonality classes)** Given a [[category]] $\mathcal{C}$, then on the [[poset]] of sub-[[classes]] of [[morphisms]] the operations of forming left and right classes with [[orthogonality]] [[lifting property]] constitute a Galois connection.

In fact all Galois connections between [[power sets]] arise this way, see [below](#BetweenPowerSets).

We now spell out in detail the Galois connections induced from a relation:

+-- {: .num_defn #GaloisConnectionFromRelation}
###### Definition
**(Galois connection induced from a [[relation]])**

Consider two [[sets]] $X,Y \in Set$ and a [[relation]]

$$
  E \hookrightarrow X \times Y
  \,.
$$

Define two [[functions]] between their [[power sets]] $P(X), P(Y)$, as follows.
(In the following we write $E(x, y)$ to abbreviate the formula $(x, y) \in E$.)


1. Define

   $$
     V_E
       \;\colon\;
     P(X)
       \longrightarrow
     P(Y)
   $$

   by

   $$
     V_E(S)
       \coloneqq
     \left\{
       y \in Y \vert  \underset{x \in  X}{\forall} \left( \left(x \in S\right) \Rightarrow E(x, y)
    \right) \right\}
   $$

1. Define

   $$
     I_E
       \;\colon\;
     P(Y)
       \longrightarrow
     P(X)
   $$

   by

   $$
     I_E(T) \coloneqq \left\{x \in X \vert \underset{y \in Y}{\forall} \left( \left(y \in T \right) \Rightarrow E(x, y)  \right)\right\}
   $$

=--

+-- {: .num_prop #GaloisConnectionAsAdjunction}
###### Proposition

The construction in def. \ref{GaloisConnectionFromRelation} has the following properties:

1. $V_E$ and $I_E$ are [[contravariant functor|contravariant]] order-preserving in that

   1. if $S \subset S'$, then $V_E(S') \subset V_E(S)$;

   1. if $T \subset T'$, then $I_E(T') \subset I_E(T)$


1. The _[[adjunction]] law_ holds:
   $
     \left(
        T \subset V_E(S)
     \right)
       \,\Rightarrow\,
     \left(
       S \subset I_E(T)
     \right)
   $

   which we denote by writing

   $$
     P(X)
       \underoverset{\underset{V_E}{\longrightarrow}}{\overset{I_E}{\longleftarrow}}{\bot}
     P(Y)^{op}
   $$

1. both $V_E$ as well as $I_E$ take [[unions]] to [[intersections]].

=--

+-- {: .proof}
###### Proof

Regarding the first point: the larger $S$ is, the more conditions that are placed on $y$ in order to belong to $V_E(S)$, and so the smaller $V_E(S)$ will be.

Regarding the second point:  This is because both these conditions are equivalent to the condition $S \times T \subset E$.

Regarding the third point: Observe that in a poset such as $P(Y)$, we have that $A = B$ iff for all $C$, $C \leq A$ iff $C \leq B$ (this is the [[Yoneda lemma]] applied to posets). It follows that

$$
  \array{
    T \subset V_E(\bigcup_{i \in I} S_i) & \text{iff} & \bigcup_{i: I} S_i \subset I_E(T) \\
    & \text{iff} & \forall_{i: I} S_i \subset I_E(T) \\
    & \text{iff} & \forall_{i: I} T \subset V_E(S_i) \\
    & \text{iff} & T \subset \bigcap_{i: I} V_E(S_i)
}
$$

and we conclude $V_E(\bigcup_{i: I} S_i) = \bigcap_{i: I} V_E(S_i)$ by the [[Yoneda lemma]].


=--


+-- {: .num_prop #GaloisClosureOperator}
###### Proposition
**([[closure operators]] from Galois connection)**

Given a Galois connection as in def. \ref{GaloisConnectionFromRelation}, consider the [[composition|composites]]

$$
  I_E \circ V_E \;\colon\; P(X) \longrightarrow P(X)
$$

and

$$
  V_E \circ I_E \;\colon\; P(Y) \longrightarrow P(Y)
  \,.
$$

These satisfy:

1. For all $S \in P(X)$ then  $S \subset I_E \circ V_E(S)$.

1. For all $S \in P(X)$ then $V_E \circ I_E \circ V_E (S)  =  V_E(S)$.

1. $I_E \circ V_E$ is [[idempotent]] and [[covariant functor|covariant]].


and

1. For all $T \in P(Y)$ then $T \subset V_E \circ I_E(T)$.

1. For all $T \in P(Y)$ then $I_E \circ V_E \circ I_E (T) = I_E(T)$.

1. $V_E \circ I_E$ is [[idempotent]] and [[covariant functor|covariant]].



This is summarized by saying that
$I_E \circ V_E$ and $V_E \circ I_E$ are _[[closure operators]]_ ([[idempotent monads]]).


=--

+-- {: .proof}
###### Proof

The first statement is immediate from the adjunction law (prop. \ref{GaloisConnectionAsAdjunction}).

Regarding the second statement:
This holds  because applied to sets $S$ of the form $I_E(T)$, we see $I_E(T) \subset I_E \circ V_E \circ I_E(T)$. But applying the contravariant map $I_E$ to the inclusion $T \subset V_E \circ I_E(T)$, we also have $I_E \circ V_E \circ I_E(T) \subset I_E(T)$.

This directly implies that the function $I_E \circ V_E$. is idempotent, hence the third statement.

The argument for $V_E \circ I_E$ is directly analogous.

=--

In view of prop. \ref{GaloisClosureOperator} we say that:

+-- {: .num_defn #GaloisClosedElements}
###### Definition
**(closed elements)**

Given a Galois connection induced from a relation as in def. \ref{GaloisConnectionFromRelation}, then

1. $S \in P(X)$ is called *closed* if $I_E \circ V_E(S) = S$;

1. the _closure_ of $S \in P(X)$ is $Cl(S) \coloneqq I_E \circ V_E(S)$

and similarly

1. $T \in P(Y)$ is called *closed* if $V_E \circ I_E(T) = T$;

1. the _closure_ of $T \in P(Y)$ is $Cl(T) \coloneqq V_E \circ I_E(T)$.

=--

It follows from the properties of [[closure operators]], hence form prop. \ref{GaloisClosureOperator}:

+-- {: .num_prop #GaloisFixedPoints}
###### Proposition
**([[fixed point of an adjunction|fixed points]] of a [[Galois connection]])**

Given a Galois connection induced from a relation as in def. \ref{GaloisConnectionFromRelation}, then

1. the closed elements of $P(X)$ are precisely those in the [[image]] $im(I_E)$ of $I_E$;

1. the closed elements of $P(Y)$ are precisely those in the [[image]] $im(V_E)$ of $V_E$.

We says these are the _[[fixed point of an adjunction|fixed points]]_ of the Galois connection. Therefore the restriction of the Galois connection

$$
  P(X)
    \underoverset{\underset{V_E}{\longrightarrow}}{\overset{I_E}{\longleftarrow}}{\bot}
  P(Y)^{op}
$$

to these fixed points yields an [[equivalence of categories|equivalence]]

$$
  im(I_E)
    \underoverset{\underset{V_E}{\longrightarrow}}{\overset{I_E}{\longleftarrow}}{\simeq}
  im(V_E)^{op}
$$

now called a _[[Galois correspondence]]_.

=--


+-- {: .num_prop}
###### Proposition

Given a Galois connection induced from a relation as in def. \ref{GaloisConnectionFromRelation}, then the sets of closed elements according to def. \ref{GaloisClosedElements} are closed under forming [[intersections]].

=--


+-- {: .proof}
###### Proof


If $\{T_i \in P(Y)\}_{i: I}$ is a collection of elements closed under the operator $K = V_E \circ I_E$, then by the first item in prop. \ref{GaloisClosureOperator} it is automatic that $\bigcap_{i: I} T_i \subset K(\bigcap_{i: I} T_i)$, so it suffices to prove the reverse inclusion. But since $\bigcap_{i: I} T_i \subset T_i$ for all $i$ and $K$ is covariant and $T_i$ is closed, we have $K(\bigcap_{i: I} T_i) \subset K(T_i) \subset T_i$ for all $i$, and $K(\bigcap_{i: I} T_i) \subset \bigcap_{i: I} T_i$ follows.

=--




## Properties

### Galois connections between power sets
 {#BetweenPowerSets}

*Every* Galois connection between full [[power sets]], 

$$(f: P(X) \to P(Y)^{op}) \dashv (g: P(Y)^{op} \to P(X))$$

is of the form in def. \ref{GaloisConnectionFromRelation} [above](#InducedFromARelation): there is some [[binary relation]] $r$ from $X$ to $Y$ such that 

$$f(S) = \{y: \forall_{x \in X} x \in S \Rightarrow r(x, y)\}, \qquad g(T) = \{x: \forall_{y \in Y} y \in T \Rightarrow r(x, y)\}$$ 

Indeed, define $r: X \times Y \to \mathbf{2}$ by stipulating that $r(x, y)$ is true if and only if $y \in f(\{x\})$. Because $f$ is a left adjoint, it takes colimits in $P(X)$ (in this case, unions) to colimits in $P(Y)^{op}$, which are intersections in $P(Y)$. Since every $S$ in $P(X)$ is a union of singletons $\{x\}$, this gives 

$$f(S) = \bigcap_{x \in S} f(\{x\}) = \{y: \forall_{x \in S} r(x, y)\}$$ 

which is another way of writing the formula for $f$ given above. We observe that 

$$T \subseteq f(S) = \{y: \forall_{x \in S} r(x, y)\}$$ 

if and only if 

$$S \times T \subseteq r$$ 

(now viewing $r$ extensionally in terms of subsets). This last symmetrical expression in $S$ and $T$ means 

$$S \subseteq g(T) := \{x: \forall_{y \in T} r(x, y)\}$$ 

which means we have a Galois connection between $f$ and $g$ under this definition; since $g$ is uniquely determined by the presence of a Galois connection with $f$, we conclude that all Galois connections between power sets arise in this way, via a relation $r$ between $X$ and $Y$. 





## Related concepts

* [[modality]]
* [[adjoint modality]]
* [[adjunction]]
* Every Galois connection is an [[idempotent adjunction]].
* [[nucleus of a profunctor]]

## References

The concept is due to 

* {#Ore44} &#216;ystein Ore, _Galois connexions_ , Trans. AMS **55** (1944) pp.493-513. ([pdf](http://www.ams.org/journals/tran/1944-055-00/S0002-9947-1944-0010555-7/S0002-9947-1944-0010555-7.pdf))

Introduction is in

* M. Ern&#233;, E. Klossoswki, A. Melton, G. E. Strecker, _A primer in Galois connections_ , Annals New York Academy of Sciences **704** (1993) pp.103-125. ([draft](http://www.math.ksu.edu/~strecker/primer.ps))

See also

* Wojciech Dzik, Jouni J&#228;rvinen, Michiro Kondo, _Characterising intermediate tense logics in terms of Galois connections_ ([arXiv:1401.7646](http://arxiv.org/abs/1401.7646)).



[[!redirects Galois connection]]
[[!redirects Galois connections]]
[[!redirects Galois correspondence]]
[[!redirects Galois correspondences]]