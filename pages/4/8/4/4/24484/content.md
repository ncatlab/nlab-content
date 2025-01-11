
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

The notion of a *Dedekind-Hasse norm* is a generalization of the notion of the degree function in a [[Euclidean domain]]. It makes clear the links between a [[principal ideal domain]] and an [[Euclidean domain]]: a pid is like an Euclidean domain but with a weaker notion of Euclidean division.

## Definition and characterization of pids

\begin{definition}
Let $R$ be an [[integral domain]]. A *Dededekind-Hasse* norm is a function $v \colon R \rightarrow \mathbb{N}$ such that:

* $v(s)=0 \Leftrightarrow s=0$

* $\forall a \in R$, $\forall (b \neq 0) \in R$:

   * $b|a$, or

   * $\exists p,q,r \in R$ such that $pa = bq + r$ and $0 \lt v(r) \lt v(b)$ 

\end{definition}

\begin{proposition}
Let $R$ be an integral domain. Then it is a principal ideal domain iff it possesses a Dedekind-Hasse norm.
\end{proposition}
\begin{proof}
Suppose that $R$ possesses a Dedekind-Hasse norm. Let $I$ be a non-zero ideal. Let $b$ be a non-zero element of $I$ of minimal norm. We know that $(b) \subseteq I$. Let $a$ be an element of $I$. Suppose that $b$ doesn't divide $a$. Then, there exists $p,q,r \in R$ such that $pa = bq+r$ and $0 \lt v(r) \lt v(b)$. Thus, $r=pa-bq \in I$, $r \neq 0$ and $v(r) \lt v(b)$, absurd! Therefore $b|a$ and $a \in (b)$. Thus, $I \subseteq (b)$ and $I = (b)$. We have proved that $R$ is a pid.

Suppose that $R$ is a pid. Thus, it is a [[unique factorization domain| UFD]]. Put $v(s)=0$ if $s=0$, and $v(s)$ equal to $2^{n}$ where $n$ is the number of irreducible elements in the factorization of $n$, if $s \neq 0$. Let $a \in R$ and $(b \neq 0) \in R$. Suppose that $b$ doesn't divide $a$. We know that $(a,b) = (r)$ and thus there exists $p,q,r \in R$ such that $pa+bq = r$.  $r$ divides $b$ but $b$ doesn't divide $r$ because it would imply that $b$ divides $a$. Thus, there is strictly less irreducible elements in the factorization of $r$ than in the one of $b$ and $v(r) \lt v(b)$. Moreover $r \neq 0$ because $(a,b) = (r)$ and $b \neq 0$. Thus $0 \lt v(r) \lt v(b)$. We have proved that $v$ is a Dedekind-Hasse norm.
\end{proof} 

### In constructive mathematics ###

In constructive mathematics, there are different types of integral domains, yielding different types of Dedekind-Hasse norms. For example, if the integral domain has a [[tight apartness relation]] $a # b$, such as in a [[Heyting integral domain]], then one can use the tight apartness relation instead of [[denial inequality]] in the second condition

* $v(s)=0 \Leftrightarrow s=0$

* $\forall a \in R$, $\forall (b \# 0) \in R$:

   * $b|a$, or

   * $\exists p,q,r \in R$ such that $pa = bq + r$ and $0 \lt v(r) \lt v(b)$ 

In constructive mathematics, integral domains with Dedekind-Hasse norms are not the same as [[principal ideal domains]] in [[constructive mathematics]]: the [[integers]] is a [[discrete integral domain]] with a Dedekind-Hasse norm because it is a [[Euclidean domain]], but is not a [[principal ideal domain]] unless [[excluded middle]] holds. 

It remains to see if integral domains with Dedekind-Hasse norms are still the same as [[Bézout domain|Bézout]] [[unique factorization domains]] or [[Noetherian ring|Noetherian]] [[Bézout domains]] in [[constructive mathematics]]. 

## References

Named after [[Helmut Hasse]].

* Wikipedia, *[Dedekind-Hasse norm](https://en.wikipedia.org/wiki/Dedekind%E2%80%93Hasse_norm)*

[[!redirects integral domain with Dedekind-Hasse norm]]
[[!redirects integral domains with Dedekind-Hasse norm]]

[[!redirects integral domain with a Dedekind-Hasse norm]]
[[!redirects integral domains with a Dedekind-Hasse norm]]
