


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a (not necessarily [[commutative ring|commutative]]) [[unital ring]] $R$, an $R$-[[module]] is _finitely presented_ (or of finite presentation) if there exists an [[exact sequence]] $R^q\to R^p\to M\to 0$ where $p,q$ are [[natural numbers]]. 

## Equivalent characterisations

\begin{proposition}
For a module $M$ over a ring $R$, the following are equivalent :

1. $M$ is finitely presented ;
1. $M$ is a [[compact object]] of the category of $R$-modules.

\end{proposition}

\begin{proposition}
For a module $M$ over a ring $R$, the following are equivalent :

1. $M$ is finitely presented ;
1. for every family $\{Q_\alpha\}_{\alpha \in A}$ of $R$-modules, the canonical map
$$
  M \otimes_R \prod_\alpha Q_\alpha \rightarrow \prod_\alpha M \otimes_R Q_\alpha
$$ 
is an isomophism ;
1. for every $R$-module $Q$ and every set $A$, the canonical map
$$
  M \otimes_R R^A \rightarrow M^A 
$$
is an isomorphism.

\end{proposition}

\begin{proof}
$1 \Rightarrow 2$. Using a finite presentation $R^q \to R^p \to M$
of $M$ one can write the commutative diagram
\begin{centre}
    \begin{tikzcd}
        R^q \otimes \prod_\alpha Q_\alpha \ar[r] \dar["\simeq"]
       & R^p \otimes \prod_\alpha Q_\alpha \rar \dar["\simeq"]
       & M \otimes \prod_\alpha Q_\alpha \dar \rar & 0
       \\
        \prod_\alpha R^q \otimes Q_\alpha \ar[r]
       & \prod_\alpha R^p \otimes Q_\alpha \rar
       & \prod_\alpha M \otimes Q_\alpha \rar & 0
    \end{tikzcd}
\end{centre}
and deduce the isomorphism.

$2 \Rightarrow 3$. Obvious

$3 \Rightarrow 1$. The map $M \otimes R^M \to M^M$ is surjective, so there exists a finite number of elements $\{m_i\}_{i \in I}$ and a finite number of functions $\{f_i\}_{i \in I} : M \to R$ such that the sum $\sum_i m_i f^i$ be the identity of $M$. As a consequence $M$ must be finitely generated.

Consider a short exact sequence $0 \to K \to R^p \to M \to 0$.
Then using the commutative diagram
\begin{centre}
    \begin{tikzcd}
        {} &
        K \otimes R^K \ar[r] \dar
       & R^p \otimes R^K \rar \dar["\simeq"]
       & M \otimes R^K \dar["\simeq"] \rar & 0
       \\
        0 \rar &
        K^K \ar[r]
       & (R^p)^K \rar
       & M^K \rar & 0
    \end{tikzcd}
\end{centre}
one gets that $K \otimes R^K \to K^K$ is surjective and thus that $K$ is finitely generated.
\end{proof}

## Related concepts

* [[finitely presented object]]

* [[finitely generated module]]

* [[coherent module]]

* [[dualizable module]]

[[!redirects finitely presented modules]]