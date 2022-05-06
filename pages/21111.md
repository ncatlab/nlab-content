+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!i
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _Kolmogorov product_ is a way of forming infinite [[tensor products]] in a [[semicartesian monoidal category]] which is not necessarily [[cartesian]]. In a [[cartesian monoidal category]] it coincides with the usual infinite [[cartesian product]] (if it exists). 

If the category in question is a [[poset]], Kolmogorov products correspond to a [[finitary complete monoid]] structure (up to reversing the arrows). 


## Definition

In what follows, let $(C,\otimes 1)$ be a [[semicartesian monoidal category]]. 


Let $X_1$ and $X_2$ be objects of $C$. The unique map $!:X_1\to 1$ induces a map
\begin{tikzcd}
X_1\otimes X_2 \ar{r}{!\otimes X_2} & X_2 ,
\end{tikzcd}
sometimes called the **projection** (or _[[marginal]]_ in the probability literature). This projection is natural in $X_2$, and there is a commutative diagram
\begin{tikzcd}
& X_1\otimes X_2 \ar{dl}[swap]{X_1\otimes !} \ar{dr}{!\otimes X_2} \\
X_1 \ar{dr}[swap]{!} && X_2 \ar{dl}{!}\\
& 1
\end{tikzcd}

More generally, let $\{X_1, \dots, X_n\}$ be a finite set of objects of $C$. All the possible projections of their product onto the factors form a finite [[Boolean lattice]].

We call this lattice the **lattice of projections**.

Even more generally, let now $\{X_i\}_{i\in I}$ be a set of objects of $C$, possibly infinite. We can form the lattice of all the finite products of the $X_i$ and their projections, with the arrows in the form 
$$
\bigotimes_{i\in F} X_i \to \bigotimes_{j\in S} X_j , 
$$
where $F$ is a finite subset of $I$, and $S\subseteq F$.
This is again a lattice (it may be infinite, but it is closed under finite [[joins]] and [[meets]]), which we call the **lattice of finite projections**. In particular, this is a [[cofiltered diagram]]. 
We call the **Kolmogorov product** of the set $\{X_i\}_{i\in I}$ the [[cofiltered limit]] of this diagram. We denote it by 
$$
\bigotimes_{i\in I} X_i .
$$


## Examples 

(...)


## See also 

* [[filtered category]], [[filtered limit]]
* [[finitary complete monoid]]
* [[monoidal category]], [[cartesian monoidal category]], [[semicartesian monoidal category]]
* [[Kolmogorov extension theorem]]


## References

(...)

* [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _The zero-one laws of Kolmogorov and Hewitt--Savage in categorical probability_, 2019. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))