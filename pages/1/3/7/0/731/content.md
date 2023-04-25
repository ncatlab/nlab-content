
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



# Dwyer-Kan loop groupoid
* table of contents
{:toc}

## Idea

The *Dwyer-Kan loop groupoid* &lbrack;[Dwyer & Kan (1984), §3.1](#DwyerKan84)&rbrack; of a [[simplicial set]] $K$ is the [[simplicial groupoid]] whose [[objects]] are the [[vertices]] of $K$ and whose [[hom object|hom]]-[[simplicial set]] between a [[pair]] of such picks up the composable sequences of higher dimensional simplices, where the zeroth [[vertex]] is thought of as the [[domain]] [[object]] and the first [[vertex]] as the [[codomain]].

Applied to the special case of a [[reduced simplicial set]] this construction reduces to the *[[Kan loop group]]* construction.

The Dwyer-Kan loop groupoid construction is a [[left Quillen functor|left]] [[Quillen equivalence]] ([[right adjoint]] to a groupoidal [[simplicial classifying space]]-construction) from the [[classical model structure on simplicial sets]] to the [[model structure on simplicial groupoids]] &lbrack;[Dwyer & Kan (1984), Thm. 3.3](#DwyerKan84)&rbrack;,
and as such exhibits the [[homotopy theory]] of [[simplicial groupoids]] as an [[equivalence of (infinity,1)-categories|equivalent]] incarnation of [[classical homotopy theory]].


## Definition

The **loop groupoid functor** is a [[functor]]  of [Dwyer & Kan (1984), §3.1](#DwyerKan84)

$$
  \mathcal{G} 
    \colon 
  sSet 
  \longrightarrow 
  sGrpd
  \,,
$$

takes a [[simplicial set]] $S$ to the Dwyer-Kan [[simplicial groupoid]] (i.e. [[sSet]]-[[enriched groupoid]]) $\mathcal{G}(S)$, whose

* [[objects]] are the [[vertices]] of $S$:

  $Obj\big(\mathcal{G}(K)\big) \,\coloneqq\, K_0$;

* [[morphisms]] in degree $n \in \mathbb{N}$ form the [[groupoid]] which is the [[quotient object|quotient]] 

  $$
    \array{
      S_{n+1} 
        &\overset{\phantom{----}}{\rightrightarrows}
      & S_0
      \\
      \mathllap{{}^{q}}\Big\downarrow 
      && 
      \Big\downarrow\mathrlap{{}^=}
      \\
      \mathcal{G}(S)_n
        &\overset{\phantom{----}}{\rightrightarrows}&
      Obj\big(\mathcal{G}(S)\big)
    }
  $$

  of the [[free groupoid]] on the [[graph]] 

  $$
    s,t 
     \,\colon\, 
    S_{n+1} 
      \overset{\phantom{--}}{\rightrightarrows} 
    S_0,
    \,,
  $$

  * with [[domain]]-function $s \coloneqq d_0 \circ d_2 \cdot d_3 \cdots d_{n+1}$ 

    and [[codomain]]-function $t \coloneqq d_1 \circ d_2 \cdot d_3 \cdots d_{n+1}$, 

  by the [[relations]] 

  $q(s_0 \sigma_n) \,\sim\, id_{d_1 \cdots d_n \sigma_n}$, for all $\sigma_n \in S_n$.  

* The [[face and degeneracy maps]] are given on generators by 

  * $d_0\big(q(\sigma)\big) \,\coloneqq\, q\big(d_1(\sigma_n)\big)^{-1}$

  * $d_i\big(q(\sigma)\big) \,\coloneqq\,q\big(d_{i+1}(\sigma)\big)$ for $i \gt 0$

  * $s_i\big(q(\sigma)\big) \,\coloneqq\,q\big(s_{i+1}(\sigma)\big)$ for $i \geq 0$.
 
\begin{remark}
The loop groupoid functor has a [[right adjoint]], $\overline{W}$ &lbrack;[Dwyer & Kan (1984) §3.2](#DwyerKan84)&rbrack; also called the *[[simplicial classifying space]] functor*.  
\end{remark}

## References

The original reference:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]], §3.1 in *Homotopy theory and simplicial groupoids*, Indagationes Mathematicae (Proceedings) **87** 4 (1984) 379-385 &lbrack;<a href="https://doi.org/10.1016/1385-7258(84)90038-6">doi:10.1016/1385-7258(84)90038-6</a>&rbrack;



[[!redirects Dwyer-Kan loop groupoid]]
[[!redirects Dwyer–Kan loop groupoid]]
[[!redirects Dwyer--Kan loop groupoid]]
[[!redirects Dwyer-Kan loop groupoids]]
[[!redirects Dwyer–Kan loop groupoids]]
[[!redirects Dwyer--Kan loop groupoids]]

[[!redirects Dwyer-Kan loop group]]
[[!redirects Dwyer-Kan loop groups]]

