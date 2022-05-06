
The definition of the $E$-Chern classes according to [Conner-Floyd 66, Theorem 7.5](#ConnerFloyd66) proceeds as follows.

Let $n \in \mathbb{N}$. Let $c_1^E$ in

$$
  \array{
    \mathbb{C}P^1
    &
      \overset
        { \Sigma^2 (1^E) }
        {\longrightarrow}
    &
    E_2
    \\
    \big\downarrow & \nearrow_{ \mathrlap{ c_1^E } }
    \\
    \mathbb{C}P^n
  }
$$

be a rank-$(n+1)$ [[complex oriented cohomology|complex orientation]].

For $\mathcal{V} \longrightarrow X$ a [[complex vector bundle]] of [[rank of a vector bundle|rank]] $n + 1$ consider the diagram

\[
  \label{ProjectiveBundleInConstructionOfConnerFloydClasses}
  \array{
    &&
    \mathcal{V}' 
      \oplus
    \mathcal{L}_{{}_{P(\mathcal{V})}}
    &\longrightarrow&
    \mathcal{V}
    \\
    &&
    \big\downarrow
    & 
      {}^{_{(pb)}} 
    &
    \big\downarrow
    \\
    \mathbb{C}P^n
    &
      \underset{
        fib_x
      }{
        \longrightarrow
      }
    &
    P(\mathcal{V})
    &
      \underset
        {\pi}
        {\longrightarrow}
    &
    X
  }
\]

where 

$$
  P(\mathcal{V}) 
  \;\coloneqq\;  
  \big(
    \mathcal{V} \setminus \{ X \times \{0\} \} 
  \big) / \mathbb{C}^\times
  \;\simeq\; 
  S(\mathcal{V})/\mathrm{U}(1)
$$

is the [[projective bundle]] of $\mathcal{V}$, with [[typical fiber]] the [[complex projective spaces]] $\mathbb{C}P^n$, and where in the middle we are displaying the [[splitting principle|splitting]] of the [[pullback bundle]] of $E$ into a [[direct sum of vector bundles|direct sum]] of a [[line bundle]] $\mathcal{L}$ with a remaining vector bundle $\mathcal{V}'$ of rank just $n$.

Using the defining conditions on the total Conner-Floyd Chern class 

$$
  c^E(\mathcal{V})
  \;\coloneqq\;
  1 
    + 
  c_1^E(\mathcal{V})
    + 
  c_2^E(\mathcal{V})
    + 
  c_3^E(\mathcal{V})
    + 
  \cdots
$$

that

1. on a line bundle we have $c^E(\mathcal{L}) =  1 + c_1^E(\mathcal{L})$ for the given complex orientation $c_1^E$;

1. on a [[direct sum of vector bundles]] we have the [Whitney sum formula](Chern+class#WhitneySumFormula) $c^E(\mathcal{V} \oplus \mathcal{W}) \;=\; c^E(\mathcal{V}) \cdot c^E(\mathcal{W})$

we see from (eq:ProjectiveBundleInConstructionOfConnerFloydClasses) that

$$
  \pi^\ast
  \big(
    c^E(\mathcal{V})  
  \big)
  \;=\;
  c^E(\mathcal{V}')
  \cdot
  \big(
    1 + c^E_1(\mathcal{L})
  \big)
  \;\;\;
  \in
  \;
  E^\bullet\big( P(\mathcal{V}) \big)
$$

and hence

$$
  \begin{aligned}
    c^E(\mathcal{V}')
    & =\;
    \pi^\ast 
    c^E(\mathcal{V})
    \cdot
    \big(
      1 + c_1^E(\mathcal{L}) 
    \big)^{-1}
    \\
    & \coloneqq\;
    \pi^\ast
    \big(
      c^E(\mathcal{V})
    \big)
    \cdot
    \underset{i}{\sum} 
    (-1)^k 
    \big(
      c_1^E(\mathcal{L})
    \big)^k
  \end{aligned}
  \,,
$$

But since $\mathcal{V}'$ is just of rank $n$, we must have $c^E_{n+1}(\mathcal{V}') = 0$, and hence in degree $2(n+1)$ this condition reads as follows:

\[
  \label{DefiningConditionOnConnerFloydChernClasses}
  0
  \;=\;
  \pi^\ast
  \big(
    {\color{blue}
      c^E_{n+1}(\mathcal{V})
    }
  \big)
  -
  \pi^\ast
  \big(
    {\color{blue}
      c^E_{n}(\mathcal{V})
    }
  \big)
  \cdot
  {\color{orange}
    c_1^E(\mathcal{L})
  }
  + 
  \pi^\ast
  \big(
    {\color{blue}
      c^E_{n-1}(\mathcal{V})
    }
  \big)
  \cdot
  {\color{orange}
  \big(
    c_1^E(\mathcal{L})
  \big)^2
  }
  - 
  \cdots
  \,.
\]

It is now sufficient to observe that 

1. the $E$-cohomology of $P(\mathcal{V})$ is a [[free module|free]] $E^\bullet(X)$-[[module]] spanned by the first cup powers of $c_1^E(\mathcal{L})$

   \[
     \label{ECohomologyOfProjectiveBundle}
     E^\bullet\big( P(\mathcal{V})  \big) 
       \;\simeq\; 
     E^\bullet(X)\Big\langle 1, c_1^E(\mathcal{L}), \big(c_1^E(\mathcal{L})\big)^2, \cdots  \rangle]
   \]

1. and in particular 

   $$
     \pi^\ast \;\colon\; E^\bullet( X ) \longrightarrow E^\bullet\big( P(\mathcal{V}) \big)
   $$ 

   is an [[injective function]],

because together this means that (eq:DefiningConditionOnConnerFloydChernClasses) has a unique solution for classes $c_n^E(\mathcal{V}) \,\in\, E^{2n}(X)$ -- these are the Conner-Floyd Chern classes of $\mathcal{V}$.

But (eq:ECohomologyOfProjectiveBundle) holds on $\mathbb{C}P^n$ after pullback along $fib_x$ (by basic arguments in [[complex oriented cohomology theory]], e.g. [Lurie 10, Lecture 4, Example 8](#LurieLecture)) and hence holds on $P(\mathcal{V})$ by the generalized-cohomology version of the [[Leray-Hirsch theorem]] ([Conner-Floyd 66, Thm. 7.4](#ConnerFloyd66))

* {#LurieLecture} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture notes, 2010 ([web](http://www.math.harvard.edu/~lurie/252x.html))

  Lecture 4 _Complex-oriented cohomology theories_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf))


* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Theorem 7.5 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__, Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))



$$
  (1 + p)
  \cdot
  \underset{k}{\sum}
  (-1)^k 
  \cdot
  p^k
$$

M$\Omega$SU(k)


* [[Mladen Bestvina]] (notes by [[Adam Keenan]]), Chapter 16 in _Differentiable Topology and Geometry, 2002 ([pdf](http://www.math.utah.edu/~keenan/manifoldsnotes.pdf), [[BestvinaKeenanDifferentialTopology.pdf:file]])


$$
  \array{
    T \Sigma
    &\hookrightarrow& 
    T \Sigma \oplus N \Sigma
    &\longrightarrow&
    N \Sigma
    \\
    {}^{\mathllap{tfr}}\big\downarrow{}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{tnfr}}\big\downarrow{}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{nfr}}\big\downarrow{}^{\mathrlap{\simeq}}
    \\
    \Sigma \times \mathbb{R}^d
    &\hookrightarrow&
    \Sigma \times \mathbb{R}^{d + n}
    &\longrightarrow&
    \Sigma \times \mathbb{R}^n
  }
$$

***


* [[Lev Pontryagin]], _Homotopy classification of mappings of an $(n+2)$-dimensional sphere on an $n$-dimensional one_, Doklady Akad. Nauk SSSR (N.S.) 19(1950), 957–959, (Russian) ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/pont3.pdf))

* [[George Whitehead]], _The $(n+2)$nd Homotopy Group of the $n$-Sphere_, Annals of Mathematics Second Series, Vol. 52, No. 2 (Sep., 1950), pp. 245-247  ([jstor:1969466](https://www.jstor.org/stable/1969466))

* H. B. Nielsen, P. Olesen, _Vortex-line models for dual strings_, Nuclear Physics B Volume 61, 24 September 1973, Pages 45-61 (<a href="https://doi.org/10.1016/0550-3213(73)90350-7">doi:10.1016/0550-3213(73)90350-7</a>)

* [[Luis Alvarez-Gaume]], Frederic Zamora, p. 6 of: _Duality in Quantum Field Theory (and String Theory)_, AIP Conference Proceedings 423, 46 (1998) ([arXiv:hep-th/9709180](https://arxiv.org/abs/hep-th/9709180))

* S. J. Chapman, around (2.33) of: _A Hierarchy of Models for Type-II Superconductors_, IAM Review Vol. 42, No. 4 (Dec., 2000), pp. 555-598 ([jstor:2653134](https://www.jstor.org/stable/2653134))

* Carsten Timm, p. 27 of: _Theory of Superconductivity_, 2020 ([pdf](https://tu-dresden.de/mn/physik/itp/cmt/ressourcen/dateien/skripte/Skript_Supra.pdf?lang=en))

\linebreak

**Prop.** Let $\mathbb{T}$ be of presheaf type. Then $Set[\mathbb{T}]\simeq  [\mathbb{T}\text{-}Mod_{fp}(Set),Set]$.

Proof. By assumption $Set[\mathbb{T}]\simeq [\mathcal{C}, Set]$. Since $[\mathcal{C},Set]\simeq [\hat{\mathcal{C}}, Set]$ (by Elephant, p.10) we can assume that $\mathcal{C}$ is Cauchy complete.

We have:

* $Ind\text{-}\mathcal{C}\simeq Flat(\mathcal{C}^{op}, Set)$ (by Elephant, p.723, or Caramello, p.198)

* $(Ind\text{-}\mathcal{C})_{fp}\simeq \mathcal{C}$ (by Elephant 4.2.2.(iii), p.724)

* $\mathbb{T}\text{-}Mod(Set)\simeq Flat(\mathcal{C}^{op}, Set)$ (from Diaconescu’s theorem).

Whence $(Ind\text{-}\mathcal{C})_{fp}\simeq (\mathbb{T}\text{-}Mod (Set))_{fp} =\mathbb{T}\text{-}Mod_{fp}(Set)\simeq \mathcal{C}$ and, accordingly, $[\mathcal{C},Set]]\simeq  [\mathbb{T}\text{-}Mod_{fp}(Set),Set]$. $\qed$


***

\begin{center}
  \begin{tikzcd}
    1 \ar[r, "z"] \ar[rd, "z"] & 
    \mathbb{Z} \ar[r, "s"] \ar[d, "n"] \ar[ld, "id_\mathbb{Z}"] &
    \mathbb{Z} \ar[d, "n"]  \\
    \mathbb{Z} & \mathbb{Z} \ar[l, "n"] & \mathbb{Z} \ar[l, "s"]
  \end{tikzcd}
\end{center}