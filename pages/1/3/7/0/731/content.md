
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


## Definitions

There are different choices of how to define a DK-type loop group functor, depending, for instance, on which [[pair]] of [[vertices]] in the [[n-simplex|$n$-simplex]] of a simpilcial set are to be regarded as the [[source]]- and [[target]]-[[object]] of the corresponding [[morphism]] in the loop groupoid. In the original definition [Dwyer & Kan (1984), §3.1](#DwyerKan84) took the direction of the morphism to point from the $1$st to the 0th vertex, $1 \to 0$. But the modern convention in analogous constructions for [[Segal spaces]] etc. is to instead take $0 \to 1$.

Moreover, apparently the original definition in [Dwyer & Kan (1984), §3.1](#DwyerKan84) had a mistake in its definition of $d_0$ (according to [Ehlers (1991), p. 10](#Ehlers91)). Both issues are claimed to be fixed in [Ehlers (1991), pp. 10](#Ehlers91).

Other definitions have been given, too (all necessarily isomorphic to each after their [[left adjoint|left adjointness]] to the [[simplicial classifying space]]-construction has been established, by [uniqueness of adjoint](adjoint+functor#UniquenessOfAdjoints)).


In any case, the DK loop groupoid construction is a [[functor]]

$$
  \mathcal{G} 
    \colon 
  sSet 
  \longrightarrow 
  sGrpd
  \,,
$$

which takes a [[simplicial set]] $S$ to a Dwyer-Kan [[simplicial groupoid]] (i.e. [[sSet]]-[[enriched groupoid]]) $\mathcal{G}(S)$.

### Original definition, fixed
 {#OriginalDefinition}

The following is a slight modification of the original [Dwyer & Kan (1984), §3.1](#DwyerKan84), due to [Ehlers (1991), pp. 10](#Ehlers91):

For $S \in sSet$ the simplicial groupoid $\mathcal{G}(S)$ is defined as follows:

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

  * with [[domain]]-function $s \coloneqq d_1 \circ d_2 \cdot d_3 \cdots d_{n+1}$, 

    and [[codomain]]-function $t \coloneqq d_0 \circ d_2 \cdot d_3 \cdots d_{n+1}$ 

  by the [[relations]] 

  $q(s_0 \sigma_n) \,\sim\, id_{d_1 \cdots d_n \sigma_n}$, for all $\sigma_n \in S_n$.  

* The [[face and degeneracy maps]] are given on generators by 

  * $d_0\big(q(\sigma)\big) \,\coloneqq\, q\big(d_1(\sigma_n)\big) \cdot q\big( d_0(\sigma_n)\big)^{-1}$

  * $d_i\big(q(\sigma)\big) \,\coloneqq\,q\big(d_{i+1}(\sigma)\big)$ for $i \gt 0$

  * $s_i\big(q(\sigma)\big) \,\coloneqq\,q\big(s_{i+1}(\sigma)\big)$ for $i \geq 0$.


### By Goerss & Jardine
 {#DefinitionByGoerssJardine}

Here is the definition given in [Goerss & Jardine (1999) p. 322, (2009) p. 302](#GoerssJardine09):


<img src="/nlab/files/DefinitionByGoerssJardine.jpg" width="620">

## Properties
 
\begin{remark}
The loop groupoid functor has a [[right adjoint]], $\overline{W}$ &lbrack;[Dwyer & Kan (1984) §3.2](#DwyerKan84)&rbrack; also called the *[[simplicial classifying space]] functor*.  
\end{remark}

## References

The original reference:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]], §3.1 in *Homotopy theory and simplicial groupoids*, Indagationes Mathematicae (Proceedings) **87** 4 (1984) 379-385 &lbrack;<a href="https://doi.org/10.1016/1385-7258(84)90038-6">doi:10.1016/1385-7258(84)90038-6</a>&rbrack;

Their definition doesn't quite work, as the $\delta_0$ does not generalise that of Kan's original loop group definition. This  was fixed in work by Joyal and Tierney, as discussed in:

* {#Ehlers91} [[Philip Ehlers]], pp. 10 in: _Simplicial groupoids as models for homotopy type_, Master's thesis (1991) &lbrack;[pdf](https://ncatlab.org/nlab/files/Ehlers-MSc-thesis.pdf)&rbrack;


See also:

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.7 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack; 

Relating the Dwyer-Kan loop groupoid-construction to the [[homotopy coherent nerve]]-construction:

* {#MinichielloRiveraZeinalian23} [[Emilio Minichiello]], [[Manuel Rivera]], [[Mahmoud Zeinalian]], Def. 3.1 in: *Categorical models for path spaces*, Advances in Mathematics **415** (2023) 108898 &lbrack;[arXiv:2201.03046](https://arxiv.org/abs/2201.03046), [doi:10.1016/j.aim.2023.108898](https://doi.org/10.1016/j.aim.2023.108898)&rbrack;


[[!redirects Dwyer-Kan loop groupoid]]
[[!redirects Dwyer–Kan loop groupoid]]
[[!redirects Dwyer--Kan loop groupoid]]
[[!redirects Dwyer-Kan loop groupoids]]
[[!redirects Dwyer–Kan loop groupoids]]
[[!redirects Dwyer--Kan loop groupoids]]

[[!redirects Dwyer-Kan loop group]]
[[!redirects Dwyer-Kan loop groups]]

