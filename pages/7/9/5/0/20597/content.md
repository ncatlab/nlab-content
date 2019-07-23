
# Finiteness spaces

* table of contents
{: toc}

## Idea

A **finiteness space** is a [[set]] together with a collection of its subsets that behave, in certain ways, like the collection of finite subsets.

## Definition

Given a set $X$ and a subset $\mathcal{U} \subseteq P(X)$ of its [[power set]], define 

$$\mathcal{U}^\perp = \{ v \in P(X) \mid u \cap v \;\text{ is finite for all }\; u\in \mathcal{U} \}.$$

This defines a [[Galois connection]] on $P(X)$.

+--{: .un_defn}
###### Definition
A **finiteness space** is a set $X$ equipped with a $\mathcal{U} \subseteq P(X)$ such that $\mathcal{U} = \mathcal{U}^{\perp\perp}$.
=--

We refer to the elements of $\mathcal{U}$ as **finitary**, and the elements of $\mathcal{U}^\perp$ as **cofinitary**.

## Properties

* All finite subsets of $X$ belong to $\mathcal{U}^\perp$ for any $\mathcal{U}$.  Thus, in a finiteness space all finite subsets are both finitary and cofinitary.

* Any set of the form $\mathcal{U}^\perp$ is down-closed, i.e. contains all subsets of its elements.  Thus, any subset of a finitary subset is finitary, and any subset of a cofinitary subset is cofinitary.

* Any set of the form $\mathcal{U}^\perp$ is closed under finite unions.  Thus, any finite union of finitary subsets is finitary, and any finite union of cofinitary subsets is cofinitary.

## Examples

* Taking $\mathcal{U} =$ all finite subsets of $X$ gives a **minimal** finiteness structure on $X$.

* Dually, taking $\mathcal{U}=$ all subsets of $X$ gives a **maximal** finiteness structure.

* In fact, if $(X,\mathcal{U})$ is a finiteness space, so is $(X,\mathcal{U}^\perp)$, its **dual**.  The maximal and minimal finiteness structures are dual.

* We cannot obtain any other finiteness spaces purely by cardinality restriction.  For instance, if all countable subsets of $X$ are finitary, then all cofinitary subsets must be finite, hence $X$ is maximal.  Thus, to obtain finiteness spaces other than the minimal or maximal ones, we must invoke some other structure on $X$.

* Let $X$ be a [[poset]] and $\mathcal{U}$ the set of all subsets of $X$ that are *noetherian*, i.e. contain no infinite strictly increasing chains.  Then this is a finiteness space.  Its dual (at least, assuming the [[axiom of choice]]) consists of subsets that are *artinian* (contain no infinite strictly decreasing chains) and *narrow* (contain no infinite [[antichains]]).

* Let $X$ be a [[linearly ordered set]] and let $\mathcal{U}$ the set of all *left-finite* subsets, i.e. those $u$ such that $u\cap \{ x \mid x \le y\}$ is finite for all $y$.  Since this is of the form $\mathcal{V}^\perp$ for $\mathcal{V}$ the set of subsets $\{x \mid x\le y\}$, it is a finiteness structure.

## Categories of finiteness spaces

A **relation** or **morphism** of finiteness spaces is a [[relation]] $R$ from $X$ to $Y$ such that

1. If $u\subseteq X$ is finitary, then $u\circ R = \{ y\in Y \mid \exists x\in u, x R y \}$ is finitary.
2. If $v\subseteq Y$ is cofinitary, then $R\circ v = \{ x\in X \mid \exists y\in v, x R y \}$ is cofinitary.

An equivalent way to say this is that

* If $u\subseteq X$ is finitary and $v\subseteq Y$ is cofinitary, then the set $\{ (x,y) \mid x\in u \wedge y\in v \wedge x R y \} \subseteq X \times Y$ has finite images under both projections $X\times Y\to X$ and $X\times Y\to Y$.

Additionally, in the presence of condition (1), condition (2) is equivalent to its special case when $v$ is a [[singleton]].

Let $FinSp_{rel}$ denote the category of finiteness spaces and relations, and $FinSp_{par}$ and $FinSp_{fun}$ its [[wide subcategories]] in which the morphisms are restricted to be [[partial functions]] or [[functions]], respectively.

Note that a partial function lies in $FinSp_{par}$ if and only if the preimage of any cofinitary subset is cofinitary.  For this is precisely the second condition above specialized to a partial function, while conversely if this holds then for any finitary $u\subseteq X$ and cofinitary $v\subseteq Y$, we have a surjection $u\cap f^{-1}(v) \to f(u) \cap v$ so that finiteness of the former implies finiteness of the latter.

### Monoidal structures

* All three categories are [[symmetric monoidal category|symmetric monoidal]] and the inclusions $FinSp_{fun} \hookrightarrow FinSp_{par} \hookrightarrow FinSp_{rel}$ are strict symmetric monoidal.
* $FinSp_{rel}$ is [[star-autonomous]] (see [Ehrhard](#Ehrhard05)).
* $FinSp_{par}$ is [[closed monoidal category|closed]] (see [BCJS](#BCJS18)).

### Initial and terminal structures

Let $Set_{par}$ denote the category of sets and [[partial functions]].  Note that $Set_{par}$ is equivalent to the category $Set_*$ of [[pointed sets]], and hence in particular is complete and cocomplete.

The following theorem says that $FinSp_{par}$ and $FinSp_{fun}$ are *almost* [[topological concrete categories]] over $Set_{par}$ and $Set$ respectively.

+-- {: .un_theorem}
###### Theorem
The ([[faithful functor|faithful]]) forgetful functors $U_{par}:FinSp_{par} \to Set_{par}$ and $U_{fun}:FinSp_{fun} \to Set$ have [[initial lifts]] for all (possibly large) [[sink|sources]] $\{ f_i : X \rightharpoonup U(S_i) \}$ having the property that for all $x\in X$ there exists an $i$ such that $x\in dom(f_i)$.
=--
+-- {: .proof}
###### Proof
The functor $U_{fun}$ is simply the pullback $U_{par}$ along the inclusion $Set \hookrightarrow Set_{par}$, so it suffices to consider the former, which we denote simply $U$.

Let $X$ be a set and $\{ f_i : X \rightharpoonup U(S_i) \}$ a $U$-structured [[sink|source]] satisfying the given condition, where each $(S_i,\mathcal{V}_i)$ is a finiteness space.  Let $\mathcal{V} = \big(\bigcup_i f_i^{-1}(\mathcal{V}_i^\perp)\big)^\perp$, making $X$ a finiteness space for which $u\subseteq X$ is finitary if and only if $u \cap f_i^{-1}(v)$ is finite for all cofinitary $v\subseteq S_i$.  Thus each $f_i$ becomes a morphism in $FinSp_{par}$.

For universality, suppose given a finiteness space $T$ and a partial function $g:U(T)\rightharpoonup X$ such that each composite $f_i\circ g$ is a morphism in $FinSp_{par}$.  The latter means that $(f_i\circ g)^{-1}(v)$ is cofinitary for all cofinitary $v\subseteq S_i$, which is to say $u \cap g^{-1}(f_i^{-1}(v))$ is finite for all finitary $u\subseteq T$.  It follows that $g(u) \cap f_i^{-1}(v)$ is finite (being a surjective image of $u \cap g^{-1}(f_i^{-1}(v))$), hence $g(u)$ is finitary, i.e. condition (1) in the definition of morphism holds.

Thus it remains to show that for any $x\in X$ the preimage $g^{-1}(x)$ is cofinitary in $T$.  By assumption, there exists an $i$ such that $x\in dom(f_i)$, which is to say $x\in f_i^{-1}(f_i(x))$.  But then $g^{-1}(x) \subseteq g^{-1}(f_i^{-1}(f_i(x)))$, hence is cofinitary.
=--

In the case of $U_{fun}$, the extra condition reduces to the statement that if $X$ is inhabited then so is the set of indices $i$.  This condition is necessary: empty $U_{fun}$-structured sources on inhabited sets do not have initial lifts.  The only candidate is the maximal finiteness structure in which all subsets are finitary and only finite sets are cofinitary, but not all functions into a maximal finiteness space are finiteness functions (only those with finite fibers).

In particular, $FinSp_{fun}$ does not have a terminal object, though it does have all inhabited limits, and the forgetful functor $FinSp_{fun} \to Set$ is a Grothendieck fibration.

A similar argument shows that $FinSp_{par}$ has all inhabited limits.  (The above is essentially the argument given for this in [BCJS](#BCJS18), unraveled into an explicit construction of limits in $Set_{par}$ in terms of the equivalence to $Set_*$.)  But $FinSp_{par}$ also has a terminal object, namely the empty set with its unique finiteness structure, so it is a [[complete category]].

In fact, $FinSp_{par}$ is also a [[cocomplete category]], as shown in [BCJS](#BCJS18).  But its coequalizers are not preserved by $U_{par}$, and in particular not constructed as final lifts of $U_{par}$-structured sinks.


## Linearization

Let $(X,\mathcal{U})$ be a finiteness space and $A$ an [[abelian group]], and define

$$ A \langle X\rangle = \{ f : X\to A \mid supp(f) \in \mathcal{U} \}$$

where $supp(f) = \{ x\in X \mid f(x)\neq 0 \}$ is the [[support]] of $f$.  Then $A\langle X\rangle$ is an abelian group called the **linearization** of $X$.

It is shown in [BCJS](#BCJS18) that if $X$ is a partial finiteness monoid (i.e. a monoid in $FinSp_{par}$) and $R$ a [[ring]], then $R\langle X\rangle$ is also a ring with

$$ (f\cdot g)(m) = \sum_{(m_1,m_2)\in X_m(f,g)} f(m_1)\cdot g(m_2) $$

where $X_m(f,g)$ is the set of pairs $(m_1,m_2)\in supp(f) \times supp(g)$ such that $m_1 \cdot m_2 = m$.

If $X$ is merely a monoid in $FinSp_{rel}$, then the above multiplication is still defined, but may not be associative or unital.

### Examples

* If $X$ is a minimal finiteness space, then the linearization $A\langle X\rangle$ is then the [[copower]] of $A$ by the set $X$ in [[Ab]].  Any monoid (or partial monoid) $M$ is a finiteness monoid with the minimal finiteness structure, and when $R$ is a ring the resulting ring structure on $R\langle M\rangle$ is induced on the basis elements by the multiplication of $M$.  When $M$ is a group $G$, this is the [[group algebra]] $R[G]$.

* If $X$ is a poset whose finitary subsets are the artinian and narrow ones, and whose multiplication preserves the strict order on each side, then it is a finitenes monoid, and its linearization is the ring of [[Ribenboim power series]] from $X$ with coefficients in $R$ (see [BCJS](#BCJS18)).  Thus, this includes rings of [[formal power series]], [[formal Laurent series]], [[polynomials]], [[Laurent polynomials]], and [[Hahn series]].

* If $X$ is a linearly ordered abelian group and the finitary subsets are the left-finite ones, then its linearization is the corresponding [[Novikov field]].

* As shown in [BCJS](#BCJS18), other examples include [[Puiseux series]], formal power series over a free monoid, and polynomials of bounded degree.


## References

* T. Ehrhard, *Finiteness spaces*, Mathematical Structures in Computer Science 15, pp. 615--646 (2005)
 {#Ehrhard05}

* Richard Blute, Robin Cockett, Pierre-Alain Jacqmin, and Philip Scott, *Finiteness spaces and generalized power series*, Electronic Notes in Theoretical Computer Science, 341 (2018), 5-22, [doi](https://doi.org/10.1016/j.entcs.2018.11.002), [arXiv:1805.09836](https://arxiv.org/abs/1805.09836)
 {#BCJS18}

[[!redirects finiteness spaces]]
