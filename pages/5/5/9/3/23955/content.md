
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[quiver]] $Q$, a *[[linear representation]]* of $Q$ (over some [[ground field]] $\mathbb{K}$) is:

1. a $\mathbb{K}$-[[vector space]] $V_v$ for each [[vertex]] $v \in Q_0$,

1. a [[linear map]] $V_v \xrightarrow{\rho(e)} V_{v'}$ for each [[edge]] $e \in Q_1$.

Notice that there is *no* further compatibility condition, in particular if there are edges forming a [[triangle]], then the associated [[linear maps]] are *not required* to be related under [[composition]].

A [[homomorphism]] between two quiver representations is a [[linear map]] $V_v \xrightarrow{\phi_v} V'_v$ for each [[vertex]], such that for each [[edge]] $v \xrightarrow{e} v'$ the following [[commuting diagram|diagram commutes]] in [[Vect]]${}_{\mathbb{K}}$:

\begin{tikzcd}
  V_v
  \ar[r, "{ \rho(e)}"]
  \ar[d, "{\phi_v}"]
  &
  V_{v'}
  \ar[d, "{\phi_{v'}}"]
  \\
  V'_v
  \ar[r, "{\rho'(e)}"]
  &
  V'_{v'}
  \mathrlap{\,.}
\end{tikzcd}

This makes a [[category]] of quiver representations of $Q$ over $\mathbb{K}$, typically denoted $Rep_{\mathbb{K}}(Q)$, or similar.


In other words, if one regards $Q$ as the [[directed graph]] that it is, and considers its [[free category]] $FrCat(Q)$, then 

1. a quiver representation is a [[functor]]

   $$
     FrCat(Q) \xrightarrow{\rho} Vect_{\mathbb{K}}
     \,,
   $$

1. a [[morphism]] of quiver representations is a [[natural transformation]]

   $$
     \phi \;\colon\; \rho \Rightarrow \rho'
     \,,
   $$

1. and the [[category of quiver representations]] is [[equivalence of categories|equivalently]] the [[functor category]] from the [[free category]] of the quiver to the [[category of vector spaces]]:

   $$
     Rep_{\mathbb{K}}(Q)
     \;\simeq\;
     Func
     \big(
       FrCat(Q)
       ,\,
       Vect_{\mathbb{K}}
     \big)
     \,.
   $$


## Related concepts

* [[Gabriel's theorem]]



## References

Review: 

* Harm Derksen, Jerzy Weyman, *Quiver Representations*, Notices of the AMS **52** 2 (2005) $[$[pdf](https://www.ams.org/notices/200502/fea-weyman.pdf)$]$

Textbook accounts:

* [[Ralf Schiffler]], *Quiver Representations*, CMS Books in Mathematics, Springer  (2014) $[$[doi:10.1007/978-3-319-09204-1](https://doi.org/10.1007/978-3-319-09204-1)$]$

Introduction in the context of [[persistent homology]] and [[topological data analysis]]:

* {#Oudot15} [[Steve Y. Oudot]], *Persistence Theory: From Quiver Representations to Data Analysis*, Mathematical Surveys and Monographs **209** AMS (2015) $[$[ISBN:978-1-4704-3443-4](https://bookstore.ams.org/surv-209/), [pdf](https://geometrica.saclay.inria.fr/team/Steve.Oudot/books/o-pt-fqrtda-15/surv-209.pdf)$]$


[[!redirects quiver representations]]
[[!redirects representation of a quiver]]

[[!redirects representations of a quiver]]
[[!redirects representations of quivers]]

[[!redirects category of quiver representations]]
[[!redirects categories of quiver representations]]



