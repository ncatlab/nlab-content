+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A relevant monad is a special kind of monad which is related to [[relevance logic]].

## Definition

Let $\mathcal{C}$ be a [[category]] with [[cartesian products|Cartesian products]]. Let $(T, \mu,\eta)$ be a [[monad]] on $\mathcal{C}$.

Recall that $T$ is said to be **right-strong** with respect to the Cartesian product (see [[strong monad]]) if it is equipped with a natural transformation $\alpha_{X,Y} : T(X)\times Y\to T(X\times Y)$ satisfying some coherence conditions which can be found on the linked page.

In what follows, fix a monad $(T, \mu,\eta)$ together with a choice of [[strength|right strength]] $\alpha$ for the Cartesian product.

Using the [[symmetric monoidal category|symmetry isomorphism]] of the Cartesian product it is possible to give a [[strength|left strength]] $\alpha'_{A,B} : A\times T(B)\to T(A\times B)$ by
\begin{equation}
A\times T(B) \cong T(B)\times A \xrightarrow{\alpha_{B,A}}T(B\times A)\cong T(A\times B)
\end{equation}

\begin{definition}
Let $T$ be a strong monad. The **right double-strength** on $T$ is the [[natural transformation]]
\begin{equation}
dst_{X,Y} : T(X)\times T(Y)\xrightarrow{\alpha_{X,T(Y)}}T(X\times T(Y))\xrightarrow{T(\alpha^{'}_{X,Y})}T^2(X\times Y)\xrightarrow{\mu}T(X\times Y)
\end{equation}
\end{definition}

\begin{definition}
If $(T,\mu,\eta)$ is a right-strong monad with respect to the Cartesian product, then $T$ is said to be 
**relevant** if the following diagrammatic law holds:

\begin{centre}
\begin{tikzcd}
      T(X\times Y)\arrow[dr,equal]
      \arrow[d,"(T(\pi_{X}){,}T(\pi_{Y}))"']\\
      T(X)\times T(Y)\arrow[r,"dst_{X,Y}"] &T(X\times Y)
\end{tikzcd}
\end{centre}
\end{definition}

\section{References}

Concept was first introduced here, see Prop 2.2:

- [[Anders Kock]], _Bilinearity and Cartesian-Closed Monads_ In: Mathematica Scandinavica 29.2 (1971), pp. 161–74. [JSTOR: 24491025](https://www.jstor.org/stable/24491025), [pdf](https://users-math.au.dk/kock/BCCM.pdf) 

Jacobs is probably the first one to introduce the name 'relevant monad':

- [[Bart Jacobs]], _Semantics of Weakening and Contraction_ In: Annals of
Pure and Applied Logic 69.1 (Sept. 1994), pp. 73–106. issn: 01680072.
[doi: 10.1016/0168-0072(94)90020-5]( https://linkinghub.elsevier.com/retrieve/pii/0168007294900205) 

See also:

- Louis Parlant et al., _Preservation of Equations by Monoidal Monads_, July 7, 2020, [arXiv: 2001.06348 [cs, math]](http://arxiv.org/abs/2001.06348)