

#Contents#
* table of contents
{:toc}

##Idea

In the context of [[control theory]] and [[automata theory]], *controllability* and *observability* are [[dual]] concepts describing the capacities (1) to control the state of a system and (2) to detect the state of a system from observations. In automata theory, the alternative term *reachability* is frequently used in place of controllability.

##Linear systems
A simple case is given by the example of finite-dimensional linear systems. Given a system 

\begin{equation}
\begin{array}{lcl}
\dot{x} = A x + B u \\
y = C x
\end{array}
\end{equation}

where $x$ is the state vector, $u$ is the control vector and $y$ is the output vector, then controllability is based on the [[rank]] of the matrix $P$:

$P = [B, A B, A^2B, ..., A^{n-1}B]$

where $n$ is the dimension of the state vector, full controllability corresponding to $rank P = n.$

Similarly observability is based on the rank of the matrix, $Q$ 

$\begin{bmatrix}
C \\
C A \\
CA^2 \\
\vdots \\
CA^{n-1}
\end{bmatrix}$

full observability corresponding to $rank(Q) = n$

The dual system is given by

\begin{equation}
\begin{array}{lcl}
\dot{z} = A^{\top}z + C^{\top}v \\
w = B^{\top}z
\end{array}
\end{equation}

Now controllability of the original system corresponds to observability of the dual, and *vice versa*.

Duality in this vein extends to many kinds of automata, nonlinear dynamical systems, hidden Markov models.


##Bialgebraic description

Often dualities of this form can be set in the framework of a [[bialgebra]]. A system's evolution and its outputs are described as $F(X) \to X \to G(X)$ for $X$ an object of a category $\mathcal{C}$ and two endofunctors, $F$ and $G$, on $\mathcal{C}$. 

Suppose $F$ has an [[initial algebra for an endofunctor|initial algebra]], $\mu F$, and $G$ has a [[terminal coalgebra for an endofunctor|terminal coalgebra]], $\nu G$, the unique map from $\mu F$ to $X$ being an [[epimorphism]] corresponds to controllability, and the unique map from $X$ to $\nu G$ being a [[monomorphism]] corresponds to 

There is often a [[contravariant endofunctor]], $D$, which plays a dualizing role and then comparison maps $F D \to D G$ and $D F \to G D$ allow us to see $D(X)$ also as a bialgebra, $F D(X) \to D G(X) \to D(X) \to D F(X) \to G D(X).$ 

One example of this is given in [[Set]] where $F(X) = 1 + A \times X$ and $G(X) = 2 \times X^A$. A bialgebra here is a finite state automaton with inputs given by $A$, and an initial state, $i:1 \to X$ and a final accepting costate $f: X \to 2$ with update function $u: A \times X \to X$.  

The state space of $\mu F$ is $A^{\ast}$, the set of words on $A$, and the state space of $\nu G$ is $2^{A^{\ast}}$. The dual automaton has state space, $D(X) = 2^X$. Here $D F(X) \cong G D(X)$.

## References  


[[!redirects controllability]]
[[!redirects observability]]
[[!redirects reachability]]
