


\tableofcontents


## Idea

In the context of [[control theory]] and [[automata theory]], *controllability* and *observability* are [[dual]] concepts describing the capacities (1) to control the state of a system and (2) to detect the state of a [[dynamical system|system]] from observations. In automata theory, the alternative term *reachability* is frequently used in place of controllability.

## Linear systems

A simple case is given by the example of finite-dimensional linear systems. Given a system of [[linear differential equations]] of the form

\[
  \begin{aligned}
    \dot{x} & = A x + B u 
    \\
    y & = C x
  \end{aligned}
\]

where $x$ is the state vector, $u$ is the control vector and $y$ is the output vector, then controllability is based on the [[rank]] of the [[matrix]] $P$:

$$
  P \,=\, \big[ B, A B, A^2B, ..., A^{n-1}B \big]
  \mathrlap{\,,}
$$

where $n$ is the [[dimension of a vector space|dimension]] of the state vector space, full controllability corresponding to $rank P = n.$

Similarly observability is based on the rank of the matrix, 

$$Q =
\begin{bmatrix}
  C \\
  C A \\
  CA^2 \\
  \vdots \\
  CA^{n-1}
\end{bmatrix}$$

full observability corresponding to $rank(Q) = n$

The dual system is given by

\[
  \begin{aligned}
  \dot{z} & = A^{\top}z + C^{\top}v 
  \\
  w & = B^{\top} z
  \mathrlap{\,.}
  \end{aligned}
\]

Now controllability of the original system corresponds to observability of the dual, and *vice versa*.

Duality in this vein extends to many kinds of automata, nonlinear dynamical systems, hidden Markov models, etc.


## Bialgebraic description

Often dualities of this form can be set in the framework of a [[bialgebra]] where a [[dynamical system|system]]'s evolution and its outputs are described as $F(X) \to X \to G(X)$ for $X$ an object of a category $\mathcal{C}$ and two endofunctors, $F$ and $G$, on $\mathcal{C}$. 

Suppose $F$ has an [[initial algebra for an endofunctor|initial algebra]], $\mu F$, and $G$ has a [[terminal coalgebra for an endofunctor|terminal coalgebra]], $\nu G$, the unique map from $\mu F$ to $X$ being an [[epimorphism]] corresponds to controllability, and the unique map from $X$ to $\nu G$ being a [[monomorphism]] corresponds to observability.

There is often a [[contravariant endofunctor]], $D$, which plays a dualizing role, and then [[natural transformations]] $F D \to D G$ and $D F \to G D$ allow us to see $D(X)$ also as a bialgebra, $F D(X) \to D G(X) \to D(X) \to D F(X) \to G D(X).$ 

One example of this is given in [[Set]] where $F(X) = 1 + A \times X$ and $G(X) = 2 \times X^A$. A bialgebra here is a finite state automaton with inputs given by $A$, and an initial state, $i:1 \to X$ and a final accepting costate $f: X \to 2$ with update function $u: A \times X \to X$, [[curried]] to $\hat{u}:X \to X^A$. The state space of $\mu F$ is $A^{\ast}$, the set of words on $A$, and the state space of $\nu G$ is $2^{A^{\ast}}$. The dual automaton has state space, $D(X) = 2^X$. Here $D F(X) \cong G D(X)$.

In the finite linear case, the relevant bialgebra is $U \oplus X \to X \to Y \oplus X$. The initial algebra is $\bigoplus_{i \in \mathbb{N}} U$, and the terminal coalgebra is $\prod_{i \in \mathbb{N}} Y$. These are infinite-dimensional and correspond to finite sequences of elements of $U$ and streams of elements of $Y$.

## References  

The founding paper:

* R. E. Kalman: *On the General Theory of Control Systems*, Proceedings of the First International Congress on Automatic Control **1** 1, Butterworth, London (1960) 481--493 \[<a href="http://doi.org/10.1016/S1474-6670(17)70094-8">doi:10.1016/S1474-6670(17)70094-8</a>\]

On the bialgebraic formulation:

* Filippo Bonchi, Marcello M. Bonsangue, Helle H. Hansen, Prakash Panangaden, Jan JMM Rutten, Alexandra Silva: *Algebra-coalgebra duality in Brzozowski's minimization algorithm* ACM Transactions on Computational Logic (TOCL) **15** 1 (2014) 1--29 \[<a href="http://doi.org/10.1145/2490818">doi:10.1145/2490818</a>, [pdf](https://dl.acm.org/doi/pdf/10.1145/2490818)\]


[[!redirects controllability]]
[[!redirects observability]]
[[!redirects reachability]]
