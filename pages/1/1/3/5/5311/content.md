
> This entry is about the notion of _root_ in [[algebra]]. For the notion in [[representation theory]] see at _[[root (in representation theory)]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

A __[[square root]]__ of an element $a$ in a [[monoid]] $M$ is a solution to the equation $x^2 = a$ within $M$. If $M$ is the multiplicative monoid of non-zero elements of a (commutative) [[field]] or [[integral domain]] $K$ (or a submonoid of this, such as the [[group of units]]), then there are exactly two square roots, denoted $\pm \sqrt{a}$, if there are any; the element $0$ has only one square root, $\pm \sqrt{0} = 0$.  But if $K$ is even a non-integral domain or a non-commutative [[skew field]], then there may be more; in the skew field $\mathbb{H}$ of [[quaternions]], there are [[continuum|continuumly]] many square roots of $-1$.

More generally, for $n \in \mathbb{N}$ a solution to the [[equation]] $x^n = a$ is called an **$n$th root** of $a$. Specifically for $a = 1$ and working in the [[field]] of [[complex number]]s, one speaks of an **$n$th [[root of unity]]**. This terminology can be applied to other fields as well; for example, the field of [7-adic numbers](http://ncatlab.org/nlab/show/p-adic+number) contains non-trivial cube (or $3^{rd}$) [[roots of unity]]. 

More generally, for any [[polynomial]] $P(x)$ of $x$ with coefficients in a field $K$, a solution to $P(x) = 0$ in $K$ is called a __root__ of $P$. When $P(x) \in K[x]$ has no solution in $k$, one can speak of a [[splitting field]] obtained by "adjoining roots" of $P$ to $K$, meaning that one considers roots in an [[extension field]] $i: K \hookrightarrow E$ of the corresponding polynomial $Q = (i \otimes_K K[x])(P) \in E[x]$, i.e., applying the evident composite map 
$$K[x] \cong K \otimes_K K[x] \stackrel{i \otimes_K 1}{\to} E \otimes_K K[x] \cong E[x]$$ 
to $P$ to get $Q$, and passing the smallest [[intermediate subfield]] between $K$ and $E$ that contains the designated roots of $Q$ (often writing $P$ for $Q$ by abuse of language). 

More generally still, one may refer to roots even of non-polynomial [[functions]] $f$ defined on a field, for example of [[meromorphic functions]] $f \colon \mathbb{C} \to \mathbb{C}$, although it is much more usual to speak of _zeroes_ of $f$ instead of roots of $f$ (e.g., zeroes of the [[Riemann zeta function]]); see [[zero set]] and [[intermediate value theorem]]. 


## Roots of unity in fields {#rootsunity}

In a [[field]] $k$, a [[torsion subgroup|torsion]] element of the multiplicative group $k^\ast$ is a [[root of unity]] by definition. Moreover we have the following useful result. 

+-- {: .num_theorem} 
###### Theorem 
Let $G$ be a [[finite group|finite]] [[subgroup]] of the [[multiplicative group]] $k^\ast$ of a field $k$. Then $G$ is [[cyclic group|cyclic]]. 
=-- 

+-- {: .proof} 
###### Proof 
Let $e$ be the _[[exponent of a group|exponent]]_ of $G$, i.e., the smallest $n \gt 0$ such that $g^n = 1$ for all $g \in G$, and let $m = order(G)$. Then each element of $G$ is a root of $x^e - 1$, so that $\prod_{g \in G} (x - g)$ divides $x^e - 1$, so $m \leq e$ by comparing [[polynomial|degrees]]. But of course $g^m = 1$ for all $g \in G$, so $e \leq m$, and thus $e = m$. 

This is enough to force $G$ to be cyclic. Indeed, write $e = p_1^{r_1} p_2^{r_2} \ldots p_k^{r_k}$. Since $e$ is the least common multiple of the orders of elements, the exponent $r_i$ is the maximum multiplicity of $p_i$ occurring in orders of elements; any element realizing this maximum will have order divisible by $p_i^{r_i}$, and some power $y_i$ of that element will have order exactly $p_i^{r_i}$. Then $y = \prod_i y_i$ will have order $e = m$ by the following lemma and induction, so that powers of $y$ exhaust all $m$ elements of $G$, i.e., $y$ generates $G$ as desired. 
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



## Related concepts

* **root**

* [[square root]]

* [[Newton's method]]

* [[Chern root]]

* [[simple root]]

* [[real nth root function]]

[[!redirects root]]
[[!redirects roots]]

