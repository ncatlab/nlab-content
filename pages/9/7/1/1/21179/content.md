#Contents#
* table of contents
{:toc}

## Idea


A cotangent complex is a certain [[spectrum object]] which exerts full control of the linear-order deformation & obstruction theory in a [[moduli problem]]. Consequently, a construction of a cotangent complex constitutes a complete understanding of the deformation theory of the situation.

There's both a *local* and *global* version of this idea. Let $X$ be a derived prestack. One can seek the following objects:

- $\mathbb{L}_{X, x} \in QCoh(U)$, for  a "point" $U \xrightarrow{x} X \in Aff_{/X}$. The local/point-wise cotangent complex.

- $\mathbb{L}_X \in QCoh(X)$. The global cotangent complex.

In the case that $X$ is a nice geometric object (e.g. an n-geometric stack), $\mathbb {L}_{X, x}$ can be viewed as the (derived) cotangent space at a point, and $\mathbb {L}_X$ the global cotangent bundle.

That being said, the global cotangent complex exist for a much broader class of prestacks $X$ than just the geometric ones, allowing one to talk about the "existence of a good deformation theory everywhere" even when the moduli problem is not representable.



## Universal Properties

### Local Case

We begin by discussing what it means for the cotangent complex to control deformation/obstruction theory.

Let

- $x: U \rightarrow X \in Aff_{/X}$
- $\iota_M: U \hookrightarrow U^M$ the *trivial* square-0 thickening by a $M \in QCoh(U)$.

The space of derivations is the [[$\infty$-groupoid]] encoding all extensions of $x$ along $\iota_M$. This can be written as a (homotopy) fiber diagram in the $\infty$-category of spaces:

\begin{definition}
$$Der_{X, x}(M)  := Map_{pSt}(U^M, X)  \times_{Map_{pSt}(U, X)}\{x\}$$
\end{definition}

Formation of these homotopy fibers is functorial in $M \in QCoh(U)$, hence determines a functor

$$Der_{X, x}: QCoh(U) \rightarrow Spaces$$

\begin{definition}
A cotangent complex for $X$ and $x$ is a object in $QCoh(U)$ corepresenting the functor $Der_{X, x}$. Such an object is denoted $\mathbb {L}_{X, x}$
\end{definition}

Hence, a cotangent complex controls, up to homotopy, the deformation theory of $x$ in $X$ by the following mechanism. 

$$
[\text{extensions of x along }  U\hookrightarrow U^M] \simeq [\mathbb {L}_{X, x} \to M] 
$$

Hence this construction translates the geometric situation on the left to the *linear* situation on the right.

### Global Case

## Properties