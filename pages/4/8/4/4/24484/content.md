
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

## Idea

A Dedekind-Hasse norm is a generalization of the degree function in an [[Euclidean domain]]. It makes clear the links between a [[principal ideal domain]] and an [[Euclidean domain]]: a pid is like an Euclidean domain but with a weaker notion of Euclidean division.

## Definition and characterization of pids

\begin{definition}
Let $R$ be an [[integral domain]]. A Dededekind-Hasse norm is a function $v:R \rightarrow \mathbb{N}$ such that:

* $v(r)=0 \Leftrightarrow r=0$
* $\forall a \in R$, $\forall (b \neq 0) \in R$:
   * $b|a$, or
   * $\exists p,q,r \in R$ such that $pa = bq + r$ and $0 \lt v(r) \lt v(b)$ 

\end{definition}

\begin{proposition}
Let $R$ be an integral domain. Then it is a principal ideal domain iff it possesses a Dedekind-Hasse norm.
\end{proposition}

## References

Wikipedia, *[Dedekind-Hasse norm](https://en.wikipedia.org/wiki/Dedekind%E2%80%93Hasse_norm)*