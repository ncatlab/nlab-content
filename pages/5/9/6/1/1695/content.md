Let $Top$ be a [[nice category of spaces|nice category of topological spaces]], in particular one which is finitely complete and cartesian closed. Let $(S^1, pt)$ be the circle, i.e., 1-dimensional sphere, with chosen basepoint, and let $(X, *)$ be a space with a chosen basepoint. Then the **loop space** of $X$ (at $*$) is the space of continuous basepoint-preserving maps $f: (S^1, pt) \to (X, *)$. Categorically, it is the pullback in $Top$ 

$$\array{
\Omega X & \to & 1\\
\downarrow & & \downarrow *\\
X^{S^1} & \underset{X^{pt}}{\to} & X^1
}$$

The loop space functor $\Omega: Top \to Top$ has a left adjoint $S: Top \to Top$, called the **suspension functor**. The space $S X$ is formed as the pushout 

## Structure of loop spaces

A loop space is an example of a [[homotopy-associative space]], or H-space. In fact, loop spaces admit a rich algebraic structure which arises from the fact that the based space $S^1$ carries a correspondingly rich co-algebraic structure, starting from the fact that the based space $S^1$ is an H-cogroup. 

An important theoretical consideration is when an H-space, and particularly one having the type of a [[CW-complex]], has the homotopy type of a loop space of another CW-complex: $X \simeq \Omega Y$. In this circumstance, one calls $Y$ a **delooping** of $X$; an important example is where $X$ is carries a topological group structure $G$, and $Y$ is the [[classifying space]] of $G$. 

The most basic fact about deloopings is the shift in homotopy groups: 

* $\pi_n(\Omega Y) \cong \pi_{n+1}(Y)$ 

The modern study of when a space admits a delooping was inaugurated by [[Jim Stasheff]]. The basic theorem is as follows (all spaces assumed to be CW-complexes): 

**Theorem:** An H-space $X$ admits a delooping if and only if the monoid $\pi_0(X)$ induced from the H-space structure is a group, and the H-space $X$ structure can be extended to a structure of algebra over the Stasheff operad $K$. 