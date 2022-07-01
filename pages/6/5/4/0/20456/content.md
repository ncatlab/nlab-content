+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A type of [[cohomology]] attached to prisms, which are $\delta$-rings equipped with an ideal satisfying some conditions. (The pair $(A, I)$ is a prism when $I$ is an [[ideal]] of a $\delta$-ring $A$ defining a [[Cartier divisor]] on its [[spectrum of a commutative ring|spectrum]] $Spec(A)$ such that $A$ is derived $(p,I)$-complete, and $p \in I + \phi(I)A$.)

Roughly, it is a unified construction of various $p$-adic cohomology theories, including [[étale cohomology]], [[de Rham cohomology]] and [[crystalline cohomology]], as well as the so far conjectural $q$-de Rham cohomology of [[Peter Scholze]].

## Definition

Let $(A,I)$ be a prism as defined above. Let $R$ be a formally smooth $A/I$-algebra. The _prismatic site_ $(R/A)_{\Delta}$ has objects which are prisms $(B,IB)$ over $(A,I)$ together with a map $R\to B/IB$ over $A/I$. Such an object is written $(R\to B/IB\leftarrow B)$.

We have functors $\mathcal{O}_{\Delta}$ and $\overline{\mathcal{O}}_{\Delta}$ which sends $(R\to B/IB\leftarrow B)$ to $B$ and $B/IB$ respectively.

The _prismatic cohomology_ of $R$ is defined to be $\Delta_{R/A}:=R\Gamma((R/A)_{\Delta},\mathcal{O}_{\Delta})$.

## Comparison theorems

We have the following comparison theorems:
\begin{theorem}[crystalline comparison]
$\phi_{A}^{*}\Delta_{R/A}^{\wedge}=R\Gamma_{crys}(R/A)$
\end{theorem}

\begin{theorem}[etale comparison]
$R\Gamma_{\et}(\mathrm{Spec}(R[1/p]),\mathbb{Z}/p^{n})=(\Delta_{R/A}[1/d]/p^{n})^{\phi=1}$
\end{theorem}

## Related entries

* [[arithmetic differential geometry]]
* [[Borger's absolute geometry]]

## References

* [[Bhargav Bhatt]], _Prismatic cohomology_, course at Columbia University, 2018 [lecture notes](http://www-personal.umich.edu/~bhattb/teaching/prismatic-columbia/)

* [[Bhargav Bhatt]], [[Peter Scholze]], _Prisms and Prismatic Cohomology_, preprint (2019) arXiv:[1905.08229](https://arxiv.org/abs/1905.08229)

For some introductory comments see

* [[Terence Tao]], _Prismatic cohomology_, ([blog post](https://terrytao.wordpress.com/2019/03/19/prismatic-cohomology/))

* Riccardo Pengo ([MO answer](https://mathoverflow.net/a/333062/447))