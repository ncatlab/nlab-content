#Contents#
* automatic table of contents goes here
{:toc}

## Idea

This page is about unbounded operators on [[Hilbert space]]s. For operators on Hilbert spaces, "bounded" and "continuous" are synonymous, so the first question to be answered is: Why consider unbounded, i.e., discontinuous operators in a category that is a [[subcategory]] of [[Top]]? The reason is simple: It is forced upon us both by applications, such as [[quantum mechanics]], and by the fact that simple and useful operators like differentiation are not bounded. Happily, in most applications the operators considered retain some sort of "limit property", namely the property of being "closed". Although that seems to be negligible compared to continuity, it allows the development of a rich and useful theory, and as a consequence there is a tremendous amount of literature devoted to this subject. 
  
### Example: differentiation is unbounded

Let $\mathcal{H}$ be the Hilbert space $L^2(\mathbb{R})$, and let $T$ be the differentiation operator defined on the dense subspace of Schwartz functions $f$ by $Tf(x) \coloneqq f'(x)$. One might hope $T$ has a continuous extension to all of $L^2$, but consider the sequence $f_k(x) := \exp(-k|x|)$ for $k \in \mathbb{N}$. Then we have $\frac{\|Tf_k\|}{\|f_k\|} = k$, so $T$ is unbounded. 

Note that the domain of definition of an unbounded operator will generally be given only on a dense subspace, as in this example. 

## Summary

After the definition we will look at some concepts that can be transferred from the bounded context [here](/nlab/show/unbounded+operator#closedness).

We will talk about the [[von Neumann algebra]] that contains all [[spectral projections]] [here](/nlab/show/unbounded+operator#affiliation).

Finally we give some counterexamples, i.e., phenomena that contradict the intuition built from bounded operators [here](/nlab/show/unbounded+operator#counterexamples).
 
## Definition

An **unbounded operator** $T$ on a Hilbert space $\mathcal{H}$ is a linear operator defined on a subspace $D$ of $\mathcal{H}$. $D$ is necessarily a linear submanifold. Usually one assumes that $D$ is dense in $\mathcal{H}$, which we will do, too, unless we indicate otherwise. 

In particular every bounded operator $A: \mathcal{H} \to \mathcal{H}$ is an unbounded operator ([[red herring principle]]). 

## Domains: a first look

Unbounded operators are not defined on the whole Hilbert space, so it is essential that, when talking about a specific unbounded operator, we are actually talking about the pair $(T, D_T)$ of an operator $T$ together with its domain $D_T$. In particular two unbounded operators $T, S$ are equal iff their domains are equal, $D_T = D_S$, and for all $x \in D_S=D_T$ we have $Tx = Sx$. 

If the domain is not specified, the default definition of the domain of a given operator $T$ is simply $D_T := \{x \in \mathcal{H} \vert Tx \in \mathcal{H} \}$.

**Warning:** if one composes two unbounded operators $T$ and $S$, it may happen that $D_T \cap D_S = \{0\}$. If we insist that all our unbounded operators are densely defined, we need as an additional assumption that $D_T \cap D_S$ is dense to make sense of the composite $T S$.

## The Hellinger-Toeplitz theorem

* Theorem: Let $A$ be an everywhere defined linear operator on a Hilbert space $\mathcal{H}$ that is symmetric. Then A is bounded.

For the definition of symmetric see below.

The Hellinger-Toeplitz theorem is a no-go theorem for [[quantum mechanics]]. Since it is known that operators essential for [[quantum mechanics]] are both symmetric and unbounded, we are led to conclude that they cannot be everywhere defined. This means that the problems that accompany only densely defined operators cannot be avoided.

### Reference

This is a corollary to the closed graph theorem III.2 in the book

* Reed, M.; Simon, B.: _Methods of modern mathematical physics_. Volume 1, Functional Analysis

## Closedness, selfadjointness, resolvent

### Closedness

Recall that the graph of an operator $T$ (or any function, in general) is the subset $\mathcal{G}_T := \{(x, y) \in \mathcal{H} \times \mathcal{H} \vert Tx = y \}$. The graph of a given operator need not be closed (in the product topology of $\mathcal{H} \times \mathcal{H}$). The notion that will be a surrogate for continuity is "closable", defined as follows:

* Definition: Given an operator T with domain $D_T$, any operator $T'$ with larger domain that is equal to $T$ on $D_T$ is called an **extension** of T, we write $T \subset T'$. 

* Definition: An operator is **closed** if its graph is closed. 

* Definition: An operator is **closable** if it has a closed extension. The smallest such extension is called the **closure** of $T$ and is denoted by $\overline{T}$.

* Proposition (closure of graph is graph of closure): If an operator $T$ is closable, then the closure of its graph $\overline{\mathcal{G}}$ is the graph of an operator, and this operator is its closure.

The last part deserves some elaboration: Given an operator $T$, we can always form the closure of its graph $\mathcal{G}$. How can the closure not be the graph of an operator? Given a sequence $(x_n)$ in $\mathcal{G}$, such that both limits $x \coloneqq \lim_{n \to \infinity} x_n$ and $y \coloneqq \lim_{n \to \infinity} T x_n$ exist, we have that $(x, y)$ is in the closure of $\mathcal{G}$. Now it may happen that there is another point $(x, y')$ in the closure with $y \neq y'$, which implies that the closure cannot be the graph of a single valued function.  

We may assume without loss of generality that $\lim_{n \to \infinity} x_n = 0$, so that we get as a characterisation of closability: if $y \coloneqq \lim_{n \to \infinity} T x_n$ exists, then $y=0$. It $T$ were continuous, we would not have to assume that $(Tx_n)$ is convergent, so this additional assumption tells us in what respect closability is weaker than continuity.

* Definition: For a closed operator $T$ a subset $D$ of $D_T$ is called a **core** of $T$ if $\overline{T \vert_{D}} = T$. In other words: if we restrict $T$ to $D$ and take the closure, we obtain again $T$.  

### Example of an operator that is not closable
...

### Selfadjointness

We let $T^*$ be the adjoint of an operator $T$. Note that for an only densly defined $T$, the domain of the adjoint may be strictly larger.

* Definition (selfadjoint et al.): An operator is **symmetric** (or **Hermitian**) if $T = T^* \vert_{D_T}$ (the adjoint is restricted to the domain of $T$). It is **selfadjoint** if it is symmetric and $D_T = D_{T^*}$. A symmetric operator is **essentially selfadjoint** if its closure is selfadjoint.

The difference of being symmetric and being selfadjoint is crucial, although there is a famous anecdote that seems to indicate otherwise:

* Anecdote of selfadjointness: Once upon a time John von Neumann thanked Werner Heisenberg for the invention of [[quantum mechanics]], because this had led to the development of so much beautiful mathematics, adding that mathematics paid back a part of the debt by clarifying for example the difference of a selfadjoint operator and one that is only symmetric. Heisenberg replied: "What is the difference?"

Nevertheless theorems that assume an operator to be selfadjoint will be not applicable to an operator that is only symmetric. One example is the [[spectral theorem]].

#### Example of a symmetric, but not selfadjoint, operator

...

## Resolvent

The definition of the resolvent does not pose any problems compared to the bounded case:

* Definition: let $T$ be a closed operator on a [[Hilbert space]] $\mathcal{H}$. A complex number $\lambda$ is in the **resolvent set** $\rho(T)$ if $\lambda \mathbb{1} - T$ is a bijection of $D_T$ and $\mathcal{H}$ with bounded inverse. The inverse operator is called
the **resolvent** $R_{\lambda}(T)$ of $T$ at $\lambda$.

* Theorem: The resolvent set is an open subset of $\mathbb{C}$ on which the resolvent is an analytic operator valued function. Resolvents at different points commute and we have
$$
      R_{\lambda}(T) - R_{\mu}(T) = (\mu - \lambda) R_{\mu}(T) R_{\lambda}(T)
$$

The proof can be done as in the bounded case.

### Commuting operators

The concept of commuting operators, which is of no problem in the bounded case, presents a conceptual difficulty in the unbounded one: for given operators $A, B$ we would like to be able to say whether they commute, although their composite may not have dense domain. For selfadjoint operators there is a solution to this problem: We know that in the bounded case, two selfadjoint operators commute iff their spectral projections commute. This suggests the

* Definition: two (possibly unbounded) selfadjoint operators commute iff all their spectral projections commute.

The [[spectral theorem]] shows that all bounded Borel functions of two commuting operators will also commute.

The following theorem states the reverse for two of the most important functions and shows that the definition of commutation above is reasonable:

* Theorem: let $A$ and $B$ be selfadjoint operators on a Hilbert space $\mathcal{H}$. Then the following three statements are equivalent:

(a) $A$ and $B$ commute

(b) if $\operatorname{Im} \lambda$ and $\operatorname{Im} \mu$ are $\neq 0$, then $R_{\lambda}(A)$ and $R_{\mu}(B)$ commute, as it is defined for bounded operators: $R_{\lambda}(A) R_{\mu}(B) = R_{\mu}(B) R_{\lambda}(A)$

(c) for all $t, s \in \mathbb{R}$ we have $\exp(itA) \exp(isB) = \exp(isB) \exp(itA)$

## Affiliation with von Neumann algebras

Let $T$ be a normal unbounded operator. Thanks to the [[spectral theorem]] for unbounded operators, $T$ has a [[spectral measure]] $P_{\lambda}$. Every single spectral projection is bounded, of course, so we may look for von Neumann algebras that contain them. Since a von Neumann algebra may be characterised as the algebra of all operators that commute with some set of unitary operators, we give the following definition:

* Definition (affiliation): A closed operator $T$ is **affiliated** with a von Neumann algebra $\mathcal{M}$, written as $T \eta \mathcal{M}$, if every unitary operator $U$ in the commutant of $\mathcal{M}$ transforms $D_T$ to itself, and we have $U^*TU = T$.

We mention some interesting theorems using this concept.

* Theorem (Kadison-Ringrose 5.6.18): An operator is normal iff it is affiliated with an abelian von Neumann algebra. If A is normal, there is a smallest von Neumann algebra that A is affiliated with, this algebra is abelian.

* Definition: Given a normal operator A, the smallest (and necessarily abelian) von Neumann algebra that A is associated with is called the **von Neumann algebra generated by A**.

  
## Strongly continuous one-parameter semigroups

A _strongly continuous one-parameter semigroup_ is an unitary representation of $\mathbb{R}$ on $\mathcal{H}$ where $\mathbb{R}$ is seen as a topological group with respect to multiplication, see [[topological group]]. An explicit definition recalling these concepts is this:

* Definition: a function $U : \mathbb{R} \to \mathcal{B}(\mathcal{H})$ is a one-parameter [[semigroup]] if the semigroup condition $U(t+s) = U(t)U(s)$ holds. If for every $x \in \mathcal{H}$ and $t \to t_0$ we have $U(t)x \to U(t_0)x$ then it is **strongly continuous**. If every $U$ is an unitary operator, it is an unitary semigroup.

In the following a semigroup will be understood to be a one-parameter unitary strongly continuous semigroup.

In physics, one-parameter semigroups of this kind often represent the time evolution of a physical system described by an [[evolution equation]].

* Theorem: a selft adjoint operator $A$ generates a semigroup via $U(t) := \exp(itA)$

* Theorem (Stone's theorem): let $U$ be a semigroup, then there is a selfadjoint operator $A$ such that $U(t) = \exp(i t A)$. This operator is often called the **infinitesimal generator** of $U$.

These two theorems are essential for the Schr&#246;dinger picture of quantum mechanics, which describes a system by the [[Schrödinger equation]], we have now a one-to-one correspondence of selfadjoint operators which can be seen as [[Hamilton operator]]s (only special operators will be seen as describing actual physical systems, of course), and semigroups which describe the time evolution generated by the [[Hamilton operator]]. 

As a trivial observation we add that Stone's theorem is a (huge) generalization of the Taylor series, let $f: \mathbb{R} \to \mathbb{R}$ that is (real) analytical in a neighborhood of $0$, then we get for $x$ small enough:
$$
f(h) = \sum_{k=0}^{\infty} \frac{f^{n}(0)}{n!} h^n = \exp(i h(-i \frac{d}{dx} ))
$$

This shows that the operator $-i \frac{d}{dx}$ generates the semigroup of translations on the real line. Now we could, for example, use Stone's theorem to prove that $-i \frac{d}{dx}$ is selfadjoint by proving that the translation group is strongly continous.

## Subtleties resulting from domain issues

(This rather generic title will have to be revised.)

### Nelson's example of noncommuting exponentials

#### Idea

Nelson's example shows that the rather involved definition of commutativity of two unbounded operators is well motivated, because a more naive one will have unwanted consequences. It is a counteraxample to the following conjecture:

* Conjecture (**false!**): Let $A$ and $B$ selfadjoint operators on a Hilbert space $\mathcal{H}$ and $D$ a dense subset such that both $A$ and $B$ restricted to $D$ are essentially selfadjoint. Suppose that for all $x \in D$ we have $ A B x - B A x = 0$. Then $A$ and $B$ commute.

We have alredy seen that on $\mathbb{R}^2$ we can define two essentially selfadjoint operators $-i \partial_x$ and $-i \partial_y$ that generate translations along the x-axis and the y-axis respectivly. Both the generated translations and the operators commute (the latter if applied to differentiable functions, of course). 

The central idea of Nelson's counterexample is to replace $\mathbb{R}^2$ by a [[Riemann surface]] with two sheets, such that walking east, then walking north takes you to one sheet, while walking north then walking east takes you to the other sheet.  

#### Definition

We use the Riemann surface $M$ of $f(z) = \sqrt(z)$. We give a brief exposition of it's construction: Take two copies of $\mathbb{C}$, two "sheets", let them call I and II. Cut both along $(0, \infty)$, label the edge of the first quadrant along the cut as $+$ and the edge of the fourth quadrant $-$. Then attach the $+$ edge of I with the $-$ of II and vice versa.

Let $\mathcal{H} = L^2(M)$ with respect to Lebesgue measure. As indicated in the idea-section we define A = $-i \partial_x$ and B = $-i \partial_y$, this is with respect to the canonical chart on each sheet that projects it onto $\mathcal{C}$ and then identifies $\mathcal{C}$ with $\mathcal{R}^2$.

Let $D$ be the set of all smooth functions with compact support not containing $0$. Then:

(a) $A$ and $B$ are essentially selfadjoint on $D$

(b) $A$ and $B$ map $D$ onto $D$

(c) for all $x \in D$ we have $A B x = B A x$

(d) $\exp(i t A)$ and $\exp(i s B)$ do not commute.

Only part (a) needs further explanation...

## References

Chapter VIII of the following classic volume is devoted to unbounded operators:

* Reed, M.; Simon, B.: _Methods of modern mathematical physics_. Volume 1, Functional Analysis 

Nelson's example is taken from the above reference, the original reference is this:

* Edward Nelson: _Analytic Vectors_ Ann.Math. 70, p.572-615, 1959

[[!redirects unbounded operators]]
[[!redirects unbounded Operators]]
[[!redirects Unbounded Operators]]
[[!redirects Unbounded Operator]]
[[!redirects unbounded Operator]]
[[!redirects closable operator]]
[[!redirects closed operator]]
[[!redirects essentially selfadjoint operator]]