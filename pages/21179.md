

#Contents#
* table of contents
{:toc}

## Idea


A _cotangent complex_ is a certain [[spectrum object]] which exerts full control of the linear-order [[deformation theory|deformation]] & [[obstruction]] theory in a [[moduli problem]]. Consequently, a construction of a cotangent complex constitutes a complete understanding of the [[deformation theory]] of the situation.

There's both a *local* and *global* version of this idea. Let $X$ be a derived prestack. One can seek the following objects:

- $\mathbb{L}_{X, x} \in QCoh(U)$, for  a "point" $U \xrightarrow{x} X \in Aff_{/X}$. The local/point-wise cotangent complex.

- $\mathbb{L}_X \in QCoh(X)$. The global cotangent complex.

In the case that $X$ is a nice geometric object (e.g. an n-[[geometric stack]]), $\mathbb {L}_{X, x}$ can be viewed as the ([[derived geometry|derived]]) [[cotangent space]] at a point, and $\mathbb {L}_X$ the global [[cotangent bundle]].

That being said, the global cotangent complex exist for a much broader class of prestacks $X$ than just the geometric ones, allowing one to talk about the "existence of a good deformation theory everywhere" even when the moduli problem is not representable.



## Universal Properties

### Ideas & Summary

Before diving into the various variants of cotangent complexes, we summarize their relationships here.

- Local cotangent complex can be obtained from global tangent complex by restriction (when the latter exists)
- The absolute tangent complexes can be obtained from the relative ones by considering the morphism $X \to pt$. 

We've already explained the global/local distinction above, we briefly discuss the absolute/relative distinction now.

In [[algebraic geometry]], relative notions are notions about families. e.g. [[flat morphism|flatness]]/[[formally smooth morphism|smoothness]]/[[formally etale morphism|etaleness]] over a base [[scheme]]/[[algebraic stack|stack]]. Relative cotangent complexes encode deformation theory of families. Of course these are analogous to [[vertical tangent bundle|relative]] cotangent bundles in [[differential geometry]].

We also note that even if one is only interested in finding an absolute cotangent complex, some of the most useful computational lemmas require you to compute relative cotangent complexes. Hence the notion is truly ubiquitous in deformation theory.


### Local Cotangent Complex

We begin by discussing what it means for the cotangent complex to control deformation/obstruction theory.

Let

- $x: U \rightarrow X \in Aff_{/X}$
- $\iota_M: U \hookrightarrow U^M$ the *trivial* square-0 thickening by a $M \in QCoh(U)$.

The  [[$\infty$-groupoid]] encoding all extensions of $x$ along $\iota_M$ is called the space of derivations. This can be written as a (homotopy) fiber diagram in the $\infty$-category of spaces:

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

### Global Cotangent Complex

\begin{definition}
An object $\mathbb{L}_X \in QCoh(X)$ is said to be a *global cotangent complex* if for all $x: U \rightarrow X \in Aff_{/X}$, $x^*\mathbb {L}_X \in QCoh(U)$ is a cotangent local complex at $x$. 
\end{definition}

Hence, one can informally write the condition as existence of a compatible system of equivalences $x^*\mathbb {L}_X \simeq \mathbb {L}_{X, x}$.


### Relative Cotangent Complexes

Both the local and global notions above can be relativized...

## Basic Properties

### Cotangent Exact Sequence

\begin{lemma}
Let $X \xrightarrow{a} Y \xrightarrow{b} Z \in Fun(\Delta^2, pSt)$ such that each arrow has a global relative cotangent complex, the following diagram

$$
a^*\mathbb{L}_{Y/Z} \to \mathbb{L}_{X/Z} \to \mathbb{L}_{X/Y} 
$$

is a fiber (and hence cofiber) diagram in the stable $\infty$ category $QCoh(X)$.
\end{lemma}

For example, taking $Z \simeq pt$ exhibits the $\mathbb{L}_{X/Y}$ as the cofiber of $f^*\mathbb{L}_{Y} \to \mathbb{L}_{X}$

### Excision

## Constructions

There are several ways to demonstrate the existence of cotangent complexes via explicit constructions:

- **Derived functors**: in the setting of dg-algebras, one can take left derived functors of the classical Kahler differentials functor $L\Omega_{(-)}$.  For example, concretely one can take a quasi-free resolution and apply $\Omega$ degree-wise. 
- **Stabilization**: when $X$ is geometric (e.g. a spectral Deligne Mumford stack), there is a construction via the "tangent $\infty$-category", which is a sort of relative stabilization procedure.

Some elaboration of these ideas are found in the article  [[cotangent complex]].