## Definition

Let $M$ be a [[category]] with two closed [[model category|model structures]] $(C_q,W_q,F_q)$ and $(C_h,W_h,F_h)$, and assume that $F_h\subseteq F_q$ and $W_h \subseteq W_q$.  

+-- {: .un_theorem}
###### Theorem
There is a (necessarily unique closed) **mixed model structure** $(C_m,W_q,F_h)$ on $M$ in which the fibrations are the $h$-fibrations, but the weak equivalences are the $q$-equivalences.
=--

## Properties

\begin{proposition}
Suppose $i$ and $j$ are _m_-cofibrations in the commutative diagram

\begin{tikzcd}
 & A \dlar[swap]{i} \drar{j} & \\
 X \arrow{rr}{f} & & Y
\end{tikzcd}

1. If $f$ is a _q_-equivalence, then it is an _h_-equivalence. In particular, a _q_-equivalence between _m_-cofibrant objects is an _h_-equivalence.

2. If $f$ is an _h_-cofibration, then it is an _m_-cofibration. In particular, an _h_-cofibration between _m_-cofibrant objects is an _m_-cofibration.

\end{proposition}
([May–Ponto 2012, proposition 17.3.4](#MayPonto2012))

\begin{theorem}
A map $i \colon A \to X$ is an _m_-cofibration iff it is an _h_-cofibration which is a composition

$$
  A \stackrel{j}{\to} K \stackrel{w}{\to} X
$$

of a _q_-cofibration $j$ and an _h_-equivalence $w$. In particular, an object $X$ is _m_-cofibrant iff it is _h_-equivalent to a _q_-cofibrant object.

\end{theorem}
([May–Ponto 2012, theorem 17.3.5](#MayPonto2012))

## Examples

* From the Quillen and Str&#248;m [[model structures on topological spaces]], we obtain a mixed model structure in which the weak equivalences are the [[weak homotopy equivalences]], the fibrations are the [[Hurewicz fibrations]], and the cofibrant objects are those of the [[m-cofibrant space|homotopy type of a CW complex]].  (This example influences the notation above; the $q$-model structure is the Quillen one, the $h$-model structure is the "Hurewicz" (or "homotopy") one.)

* Similarly, we can mix the $q$- and $h$- [[model structures on chain complexes]].

* Let $T$ be an [[accessible functor|accessible]] [[strict 2-monad]] on a [[locally finitely presentable category|locally finitely presentable]] [[strict 2-category]] $K$.  Then by a theorem of Lack, the category $T Alg_s$ of strict $T$-[[algebra over a monad|algebras]] admits a [[transferred model structure]] from the [[2-trivial model structure]] on $K$, where the weak equivalences and fibrations are the morphisms which become internal equivalences and internal isofibrations in $K$.

  On the other hand, $T Alg_s$ has its own 2-trivial model structure.  Since the forgetful functor $T Alg_s \to K$ preserves equivalences and isofibrations (the latter since it has a strict left 2-adjoint), we can mix these two model structures to obtain one whose weak equivalences are the equivalences in $K$ (which are also the equivalences in the category $T Alg$ of $T$-algebras and [[pseudo morphisms]]), but whose fibrations are the isofibrations in $T Alg_s$.

## See also

* [[intermediate model structure]]

## References

The original paper is

* [[Michael Cole]], _Mixing model structures_, Top. Appl. 153 (2006) 1016&#8211;1032

There is also an exposition in

* {#MayPonto2012} [[Peter May]] and [[Kate Ponto]], _More Concise Algebraic Topology_ (2012), section 17.3.
