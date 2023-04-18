
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


# Dwyer--Kan loop groupoid
* table of contents
{:toc}

## Idea

The *Dwyer-Kan loop groupoid* &lbrack;[Dwyer & Kan (1984), §3.1](#DwyerKan84)&rbrack; of a [[simplicial set]] $K$ is the [[simplicial groupoid]] whose [[objects]] are the [[vertices]] of $K$ and whose [[hom object|hom]]-[[simplicial set]] between a [[pair]] of such picks up the composable sequences of higher dimensional simplices, where the zeroth [[vertex]] is thought of as the [[domain]] [[object]] and the first [[vertex]] as the [[codomain]].

Applied to the special case of a [[reduced simplicial set]] this construction reduces to the *[[Kan loop group]]* construction.

The Dwyer-Kan loop groupoid construction is a [[left Quillen functor|left]] [[Quillen equivalence]] ([[right adjoint]] to a groupoidal [[simplicial classifying space]]-construction) from the [[classical model structure on simplicial sets]] to the [[model structure on simplicial groupoids]] &lbrack;[Dwyer & Kan (1984), Thm. 3.3](#DwyerKan84)&rbrack;,
and as such exhibits the [[homotopy theory]] of [[simplicial groupoids]] as an [[equivalence of (infinity,1)-categories|equivalent]] incarnation of [[classical homotopy theory]].


## Definition

The **loop groupoid functor of Dwyer and Kan** is a [[functor]] 

$$
  \mathcal{G} 
    \colon 
  sSet 
  \longrightarrow 
  sGrpd
  \,,
$$

which takes a [[simplicial set]] $K$ to the [[simplicial groupoid]] $\mathcal{G}(K)$, where for each $n \in \mathbb{N}$:

* $\mathcal{G}(K)_n$ is the [[free groupoid]] on the [[graph]]

  $$
    s,t \colon K_{n+1} \rightarrow K_0,
    \,,
  $$

* with [[domain]]-function $s \coloneqq (d_1)^{n+1}$ 

  and [[codomain]]-function $t \coloneqq d_0(d_2)^n$, 

* [[quotient|quotiented]] by the [[relations]] 

  $s_0 \sigma_n \overset{!}{=} id$, for all $\sigma_n \in K_n$.  

* The [[face and degeneracy maps]] are given on generators by 

  *   $s_i^{\mathcal{G}(K)}(x) \coloneqq s_{i+1}^K(x),$

  *   $d_i^{\mathcal{G}(K)}(x) \coloneqq d_{i+1}^K(x)$, for $x \in K_{n+1}$, $1 \lt i \leq n$, and 

  *   $d_0^{\mathcal{G}(K)}(x) = (d_0^K(x))^{-1}(d_1^K(x))$. 

\begin{remark}
This is indeed a simplicial groupoid (as discussed [there](simplicial+groupoid#Definition)) in the sense of Dwyer & Kan, in that the face and degeneracy maps are constant on the objects.
\end{remark}

\begin{remark}
The loop groupoid functor has a [[right adjoint]], $\overline{W}$ &lbrack;[Dwyer & Kan (1984) §3.2](#DwyerKan84)&rbrack; called the [[simplicial classifying space]] functor.  
\end{remark}

## References

The original reference:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]],  *Homotopy theory and simplicial groupoids*, Indagationes Mathematicae (Proceedings) **87** 4 (1984) 379-385 &lbrack;<a href="https://doi.org/10.1016/1385-7258(84)90038-6">doi:10.1016/1385-7258(84)90038-6</a>&rbrack;



[[!redirects Dwyer-Kan loop groupoid]]
[[!redirects Dwyer–Kan loop groupoid]]
[[!redirects Dwyer--Kan loop groupoid]]
[[!redirects Dwyer-Kan loop groupoids]]
[[!redirects Dwyer–Kan loop groupoids]]
[[!redirects Dwyer--Kan loop groupoids]]

[[!redirects Dwyer-Kan loop group]]
[[!redirects Dwyer-Kan loop groups]]
