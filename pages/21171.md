
#Contents#
* table of contents
{:toc}


## Idea

Steenrod's _generalized cup products_ generalize the usual simplicial [[cup products]] on [[simplicial cochains]].

Taken together, all generalized cup products organize into the [[sequence operad]].
This operad is an [[E-infinity operad]] and it acts on [[simplicial cochains]],
turning them into an [[E-infinity algebra]].

## Definition

First, we define an operation on [[simplicial chains]]
that decomposes simplices in a manner similar
to how the usual simplicial [[cup product]] decomposes
a simplex into the tensor product of a simplex
consisting of the initial $(p+1)$ vertices
and a simplex consisting of the last $(q+1)$ vertices,
with $p+q$ being the dimension of the original simplex.

\begin{definition}
(Definition 2.10(a) in [McClure-Smith 01](#Cochain).)
Given a surjection $f\colon\{1,\ldots,m\}\to\{1,\ldots,k\}$
and a simplex $\sigma\colon\Delta^p\to X$,
define
$$\sigma[f]\in(C(X))^{\otimes k}$$
as
$$\sigma[f]=\sum_A (-1)^{\epsilon(f,A)}\bigotimes_{1\le i\le k}\sigma\left(\coprod_{f(j)=i}A_j\right).$$
The variable $A$ is indexed over all overlapping partitions of $\{0,\ldots,p\}$ with $m$ parts.
\end{definition}

Here
$$\epsilon(f,A)=\sum_{j\lt j',f(j)\gt f(j')}dim(A_j)dim(A_{j'})+\sum_{1\le j\le m}dim(A_j)(\tau_f(j)-f(j)),$$
(Definition 2.9 in \cite{Cochain})
where
$$\tau_f(j)=card\{j'\in\{1,\ldots,m\}\mid f(j')\lt f(j) or f(j')=f(j) and j'\le j\}$$
(Definition 2.7 in \cite{Cochain}).
Also, $dim(B)=card(B)-1$ denotes the dimension of the simplex with the set of vertices $B$
(Notation 2.6 in \cite{Cochain}).

We are now ready to define generalized cup products.

\begin{definition}
(See Definition 2.10(b) in \cite{Cochain}.)
Given a surjection $f\colon \{1,\ldots,m\}\to\{1,\ldots,k\}$,
the natural transformation
$$\langle f\rangle=\cup_f\colon (C^*(X))^{\otimes k}\to C^*(X)$$
is defined by
$$\langle f\rangle(x_1\otimes\cdots\otimes x_k)(\sigma)=(-1)^{m-k}(x_1\otimes\cdots\otimes x_k)(\sigma[f]).$$
\end{definition}

\begin{remark}
(See Lemma 2.12, Definition 2.13, and Definition 2.14 in \cite{Cochain}.)
If $f(l)=f(l+1)$ for some $1\le l\lt m$, then $\langle f\rangle=0$.
Thus, in the [[sequence operad]] such degenerate operations must be modded out.
The remaining operations form a basis of the [[sequence operad]].
\end{remark}

\begin{remark}
(See Remark 2.11 in \cite{Cochain}.)
If $k=2$, we recover the traditional cup-$i$ products $\cup_i$ defined by Steenrod as follows.
Define $f\colon\{1,\ldots,m\}\to\{1,2\}$
to be the function with alternating values 1, 2, 1, 2, …
Now $\langle f\rangle=\cup_{m-2}$.
In particular for $m=2$ (the sequence 12) we recover the [[cup product]]
and for $m=3$ (the sequence 121) we recover $\cup_1$.
\end{remark}

## Related concepts

* [[cup product]]

* [[sequence operad]]

## References


* {#Cochain} [[James E. McClure]], [[Jeffrey H. Smith]],
_Multivariable cochain operations and little $n$-cubes_
([arXiv:math/0106024](https://arxiv.org/abs/math/0106024))


[[!redirects generalized cup products]]
