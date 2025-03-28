
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An $n$th _root of unity_ in a [[ring]] $R$ is an element $x$ such that $x^n = 1$ in $R$, hence is a [[root]] of the [[equation]] $x^n-1 = 0$.

## Properties

### Over a field

\begin{proposition}\label{SumOfRootsOfUnity}
**(sum of roots of unity)**
\linebreak
For $k \in \mathbb{N}_{\gt 0}$, let $\zeta$ be a $k$th root of unity in a [[field]], $\zeta^k = 1$. Then

\[
  \label{SumOfPowersOfRootOfUnity}
  \tfrac{1}{k}
  \sum_{n=0}^{k-1}
  \zeta^n
  \;=\;
  \left\{
  \begin{array}{lcl}
    1 &\vert& \zeta = 1
    \\
    0 &\vert& otherwise
  \end{array}
  \right.
  \,.
\]
\end{proposition}
\begin{proof}
  The case $\zeta = 1$ is immediate.
  For the case $\zeta \neq 1$ observe that
  $$
    (1 - \zeta)
    \sum_{n=0}^{k-1}
    \zeta^n
    \;=\;
    1 - \zeta^{k}
    \;=\;
    0
    \,.
  $$
\end{proof}
This may be understood as expressing the [[discrete Fourier transform]] of the [[Kronecker delta]]. For more subtle variants of the expression (eq:SumOfPowersOfRootOfUnity) see at *[[Gauss sum]]*.

\linebreak


In a [[field]] $k$, a [[torsion subgroup|torsion]] element of the multiplicative group $k^\ast$ is a [[root of unity]] by definition. Moreover we have the following useful result:

+-- {: .num_theorem} 
###### Theorem 
Let $G$ be a [[finite group|finite]] [[subgroup]] of the [[multiplicative group]] $k^\ast$ of a field $k$. Then $G$ is [[cyclic group|cyclic]]. 
=-- 

+-- {: .proof} 
###### Proof 
Let $e$ be the _[[exponent of a group|exponent]]_ of $G$, i.e., the smallest $n \gt 0$ such that $g^n = 1$ for all $g \in G$, and let $m = order(G)$. Then each element of $G$ is a root of $x^e - 1$, so that $\prod_{g \in G} (x - g)$ divides $x^e - 1$, i.e., $m \leq e$. But of course $g^m = 1$ for all $g \in G$, so $e \leq m$, and thus $e = m$. 

This is enough to force $G$ to be cyclic. Indeed, consider the prime factorization $e = p_1^{r_1} p_2^{r_2} \ldots p_k^{r_k}$. Since $e$ is the least common multiple of the orders of elements, the exponent $r_i$ is the maximum multiplicity of $p_i$ occurring in orders of elements; any element realizing this maximum will have order divisible by $p_i^{r_i}$, and some power $y_i$ of that element will have order exactly $p_i^{r_i}$. Then $y = \prod_i y_i$ will have order $e = m$ by the following lemma and induction, so that powers of $y$ exhaust all $m$ elements of $G$, i.e., $y$ generates $G$ as desired. 
=-- 

+-- {: .num_lemma}
###### Lemma 
If $m, n$ are relatively prime and $x$ has order $m$ and $y$ has order $n$ in an abelian group, then $x y$ has order $m n$. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose $(x y)^k = x^k y^k = 1$. For some $a, b$ we have $a m - b n = 1$, and so $1 = x^{k a m} y^{k a m} = y^{k a m} = y^k y^{k b n} = y^k$. It follows that $n$ divides $k$. Similarly $m$ divides $k$, so $m n = lcm(m, n)$ divides $k$, as desired. 
=--  

Clearly there is at most one subgroup $G$ of a given order $n$ in $k^\ast$, which will be the set of $n^{th}$ [[roots of unity]]. If $G$ is a finite subgroup of order $n$ in $k^\ast$, then a generator of $G$ is called a **primitive** $n^{th}$ [[root of unity]] in $k$. 

+-- {: .num_cor}
###### Corollary 

Every [[finite field]] has a [[cyclic group|cyclic]] [[multiplicative group]]. 

=-- 




### Inside the multiplicative group

Given a base [[commutative ring]] $R$, such that the [[affine line]] is

$$
  \mathbb{A}^1 = Spec( R[t] )
$$

and the [[multiplicative group]] is 

$$
  \mathbb{G}_m = Spec(R[t,t^{-1}])
$$

then the group of $n$th roots of units is

$$
  \mu_n = Spec( R[t]/(t^n - 1) ) 
  \,.
$$

(For review see e.g. [Watts, def. 2.3](#Watts), [Sutherland, example 6.7](#Sutherland)).

As such this is part of the [[Kummer sequence]]

$$
  \mu_n \longrightarrow \mathbb{G}_m \stackrel{(-)^n}{\longrightarrow} \mathbb{G}_m
$$

## Related concepts

* [[Gauss sum]]

* [[Q/Z]]

* [[Tate twist]]

## References

* {#Watts} Jordan Watts, _The Kummer sequence_ ([pdf](http://www.math.toronto.edu/jwatts/papers/galois.pdf), [archived](https://web.archive.org/web/20160910001550/http://www.math.toronto.edu:80/jwatts/papers/galois.pdf))

* {#Sutherland} Tom Sutherland, _&#201;tale cohomology_ ([pdf](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=c198d690816bce3df411cad5cd0a96da2df0b474))

[[!redirects roots of unity]]

[[!redirects primitive root of unity]]
[[!redirects primitive roots of unity]]
