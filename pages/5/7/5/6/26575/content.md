+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a [[category]] with all [[products]], one can take finite products of objects, and hence one has a [[monoidal category]].
One can however also take _infinite products_. In some situations, such as in [[categorical probability]], one is interesting in taking a infinitary version of a tensor product. 

In measure-theoretic [[probability theory]], such a construction is provided by [[Kolmogorov's extension theorem]], and the same idea can be used in general:

- In a category with products, an infinite product can be expressed as a [[cofiltered limit]] of finite products.
- Similarly, one can define an *infinitary tensor product* as a cofiltered limit, if it exists, of finite *tensor* products*.


## Definition

Let $(C,\otimes,I)$ be a [[symmetric monoidal category]] equipped with a distinguished map $del_X:X\to I$ for each object $I$. 
(This happens for example if $C$ is [[cartesian monoidal category|cartesian]] [[semicartesian monoidal category|semicartesian]], or if it has a [[Markov category|Markov or copy-discard structure]].)

Let $J$ be a possibly infinite set, and let $(X_i)_{i\in J}$ be a $J$-indexed collection of objects of $C$. 

For every finite subset $F\subseteq J$, denote by 
$$
\bigotimes_{i\in F} X_i
$$
the tensor product of the family $(X_i)_{i\in F}$. (Note that $F$ is not ordered, but the ordering of the terms in the tensor product does not matter up to coherent isomorphism, since $C$ is symmetric monoidal.)

Consider now finite subsets $F\subseteq G$ of $J$. 
We have a canonical "projection" morphism 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
\bigotimes_{i\in G} X_i \ar{r}{\pi_{G,F}} & \bigotimes_{i\in F} X_i
\end{tikzcd}
defined as follows.
First of all, for $i\in G$, let 
$$
Y_i = \begin{cases}
X_i & i\in F ; \\
I & i\notin F.
\end{cases}
$$
Similarly, let $e_i:X_i\to Y_i$ be
$$
e_i = \begin{cases}
id_{X_i} & i\in F ; \\
del_{X_i} & i\notin F.
\end{cases}
$$
The map $\pi_{G,F}$ is given by the tensor product of the $e_i$ as follows,
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
\bigotimes_{i\in G} X_i \ar{rr}{\otimes_{i\in G} e_i} && \bigotimes_{i\in G} Y_i \ar{r}{\cong} & \bigotimes_{i\in F} X_i
\end{tikzcd}
where the isomorphism on the right is given by the [[unitors]] of the monoidal category.

Let now $Fin(J)$ be the [[poset]] of finite subsets of $G$. The union of finite subsets is finite, so $Fin(J)$ is a [[directed set]], hence a [[filtered category]]. 
The functor $Fin(J)^op\to C$ mapping the inclusion $F\subseteq G$ to $\pi_{G,F}$ defined above is hence a [[cofiltered diagram]].

We say that an object is an **infintary tensor product of the family $(X_i)_{i\in J}$** in $C$, and denote it by $X_J$, if 

* It is a [[cofiltered limit]] of the functor $Fin(J)^op\to C$ described above, and moreover
* For every object $A$, the functor $A\otimes-:C\to C$ preserves this limit.


## Examples

* In a [[cartesian monoidal category]], every infinite product, if it exists, is an infinitary tensor product.

* In a [[Markov category]], [[Markov category#kolmogorov_products|Kolmogorov products]] are particular infinitary products compatible with the copy-discard structure. In particular, the category [[BorelStoch]] has all countable infinitary tensor products.

* Reversing all arrows, the *infinite tensor product of rings* is defined as the [[filtered colimit]] of all the finitary tensor products. (The canonical arrows $I\to X$ are the units of the rings.)


## See also 

* [[monoidal category]], [[cartesian monoidal category]]
* [[filtered category]], [[filtered limit]]
* [[Markov category]], [[Kolmogorov extension theorem]]


## References

* {#fritzrischel} [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _Infinite products and zero-one laws in categorical probability_, Compositionality 2(3) 2020. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))


[[!redirects infinitary tensor products]]
[[!redirects infinite tensor product]]
[[!redirects infinite tensor products]]