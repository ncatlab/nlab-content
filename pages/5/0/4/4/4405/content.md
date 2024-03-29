
#Contents
* table of contents
{:toc}

## Definition 

Let $R$ be an [[order]]ed [[field]]. A **semialgebraic set** is a subset of a product space $R^n$ that is a Boolean combination of sets defined by polynomial inequalities: 

$$\{(x_1, \ldots, x_n) \in R^n: p(x_1, \ldots, x_n) \geq 0\}$$ 

In other words, a semialgebraic set is a finite union of loci defined by systems of polynomial inequalities 

$$p_1(x_1, \ldots, x_n) \geq 0, \ldots, p_k(x_1, \ldots, x_n) \geq 0, q_1(x_1, \ldots, x_n) = 0, \ldots, q_l(x_1, \ldots, x_n) = 0$$ 

## The Tarski-Seidenberg theorem
 {#TarskiSeidenbergTheorem}

The fundamental theorem for semialgebraic sets over [[real closed field]]s $R$ is as follows. 

+-- {: .num_theorem}
######Theorem 
**([[Tarski-Seidenberg theorem|Tarski-Seidenberg]])**
The image of a semialgebraic set in $R^{n+1}$ under the projection map 
$$\pi: R^{n+1} \to R^n: (x_1, \ldots, x_{n+1}) \mapsto (x_1, \ldots, x_n)$$ 
is also a semi-algebraic set. 
=-- 

This remarkable theorem has far-reaching consequences for the theory of ordered fields. For one, it is called a "quantifier elimination" result because it says that any first-order [[predicate]] in the theory of ordered fields (with [[signature]] $(0, 1, +, -, \cdot, \lt)$) is equivalent to a predicate which is [[quantifier]]-free. This follows from a straightforward induction coupled with the observation that the Tarski--Seidenberg theorem directly says that if a predicate $R(x_1, \ldots, x_n, y)$ is a Boolean combination of atomic formulas (thus defining a semi-algebraic set), then  

$$\{(x_1, \ldots, x_n): \exists_y R(x_1, \ldots, x_n, y)\}$$ 

is also definable by a Boolean combination of atomic formulas; hence the existential quantifier can be eliminated. 

From here, it may be shown that the theory of real closed fields is *decidable*: that each sentence in the theory is provably true or provably false. In fact, a real closed field is elementarily equivalent to the ordered field of real numbers, and so the theory of the real numbers (as ordered field) is decidable. As special cases, we have that 

* Euclidean geometry is decidable. 

* Differential calculus over the real numbers is decidable. 

The collection of semialgebraic sets is the archetypal example of an [[o-minimal structure]]. 

## Semialgebraic relations 

A **semialgebraic relation** of arity $m \to n$ is an ordered triple $(m, n, R)$ where $R$ is a semialgebraic subset of $R^{m+n}$. 

The composite of two semialgebraic relations $R: m \to n$, $S: n \to p$ is the triple $(m, p, S \circ R)$ where 

$$S \circ R = \{(x, z) \in R^m \times R^p: \exists_{y \in R^n} R(x, y) \wedge S(y, z)\};$$ 

here $S \circ R$ is semialgebraic by the Tarski-Seidenberg theorem. In brief, semialgebraic relations form a [[cartesian bicategory]] of relations. 



[[!redirects semi-algebraic set]]