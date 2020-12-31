
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of [[Chern classes]] of [[complex vector bundles]], as [[universal characteristic classes]] in [[ordinary cohomology]], generalizes to any [[complex oriented cohomology|complex oriented]] [[generalized cohomology theory]]: the _Conner-Floyd Chern classes_ ([Conner-Floyd 66, Section 7](#ConnerFloyd66), [Adams 74, Section I.4](#Adams74), review in [Kochmann 96, Section 4.3](#Kochmann96), [Lurie 10, Lectures 4 and 5](#Lurie10)):

For $E$ a [[generalized cohomology theory]], the analog of the [[first Chern class]] in $E$-cohomology is what appears in the very definition of [[complex oriented cohomology]]. The higher generalized Chern classes are induced from this by the [[splitting principle]]. See also at _[complex oriented cohomology -- the cohomology ring of BU(n)](complex+oriented+cohomology+theory#TheCohomologyRingOfBUn)_.

The Conner-Floyd Chern classes in top degree serve as the generalized [[Thom classes]] that make every [[complex vector bundle]] have [[orientation in generalized cohomology]] with respect to any [[complex oriented cohomology theory]] ([Lurie 10, lecture 5, prop. 6](#Lurie10)).

## Definition
 {#Definition}

The definition of the $E$-Chern classes according to [Conner-Floyd 66, Theorem 7.6](#ConnerFloyd66) proceeds as follows.

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
    \mathbb{C}P^\infty
  }
$$

be a [[complex oriented cohomology|complex orientation]] in $E$-cohomology.

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

is the [[projective bundle]] of $\mathcal{V}$, with [[typical fiber]] the [[complex projective spaces]] $\mathbb{C}P^n$, and where in the middle we are displaying the [[splitting principle|splitting]] ([here](projective+bundle#Splitting)) of the [[pullback bundle]] of $E$ into a [[direct sum of vector bundles|direct sum]] of a [[line bundle]] $\mathcal{L}$ with a remaining vector bundle $\mathcal{V}'$ of rank just $n$.

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

1. on a [[complex line bundle]] we have $c^E(\mathcal{L}) =  1 + c_1^E(\mathcal{L})$ for the given complex orientation $c_1^E$;

1. on a [[direct sum of vector bundles]] we have the [Whitney sum formula](Chern+class#WhitneySumFormula) $c^E(\mathcal{V} \oplus \mathcal{W}) \;=\; c^E(\mathcal{V}) \cdot c^E(\mathcal{W})$

we see from (eq:ProjectiveBundleInConstructionOfConnerFloydClasses) that

$$
  \pi^\ast
  \big(
    {\color{blue}
      c^E(\mathcal{V})  
    }
  \big)
  \;=\;
  c^E(\mathcal{V}')
  \cdot
  \big(
    1 
      + 
    {\color{orange} 
      c^E_1(\mathcal{L})
    }
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
    \big(
      {\color{blue}
        c^E(\mathcal{V})
      }
    \big)
    \cdot
    \big(
      1 + 
      {
        \color{orange}
        c_1^E(\mathcal{L}) 
      }
    \big)^{-1}
    \\
    & \coloneqq\;
    \pi^\ast
    \big(
      {\color{blue}
      c^E(\mathcal{V})
      }
    \big)
    \cdot
    \underset{k}{\sum} 
    (-1)^k 
    \big(
      {\color{orange}
        c_1^E(\mathcal{L})
      }
    \big)^k
    \,.
  \end{aligned}
$$

But since $\mathcal{V}'$ is just of rank $n$, we must have $c^E_{n+1}(\mathcal{V}') = 0$, and hence in degree $2(n+1)$ this condition reads as follows:

\[
  \label{DefiningConditionOnConnerFloydChernClasses}
  \begin{aligned}
  0
  & =\;
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
  \big(
    {\color{orange}
      c_1^E(\mathcal{L})
    }
  \big)^2
  - 
  \cdots
  +
  (-1)^n
  \pi^\ast
  \big(
    {\color{blue}
      c^E_{1}(\mathcal{V})
    }
  \big)
  \cdot
  \big(
    {\color{orange}
      c_1^E(\mathcal{L})
    }
  \big)^n
  \\
  & 
  \phantom{=}
  + 
  (-1)^{n+1}
  \big(
    {\color{orange}
      c_1^E(\mathcal{L})
    }
  \big)^{n+1}
  \,.
  \end{aligned}
\]

It is now sufficient to observe that 

1. the $E$-cohomology of $P(\mathcal{V})$ is a [[free module|free]] $E^\bullet(X)$-[[module]] [[linear span|spanned]] by the first [[cup product|cup powers]] of $c_1^E(\mathcal{L})$:

   \[
     \label{ECohomologyOfProjectiveBundle}
     E^\bullet\big( P(\mathcal{V})  \big) 
       \;\simeq\; 
     E^\bullet(X)
    \Big\langle 
      1, 
      {\color{orange}
        c_1^E(\mathcal{L})
      }
      , 
      \big(
        {\color{orange}
          c_1^E(\mathcal{L})
        }
      \big)^2
      , 
      \cdots
      ,  
      \big(
        {\color{orange}
          c_1^E(\mathcal{L})
        }
      \big)^n
    \Big\rangle
    \,;
   \]

1. and in particular 

   $$
     \pi^\ast 
       \;\colon\; 
     E^\bullet( X ) 
       \overset{\;\;\;\;\;}{\hookrightarrow}
     E^\bullet\big( P(\mathcal{V}) \big)
   $$ 

   is an [[injective function]],

because this means that (eq:DefiningConditionOnConnerFloydChernClasses) has a unique solution for the classes ${\color{blue} c_k^E(\mathcal{V})} \,\in\, E^{2k}(X)$ -- these are the Conner-Floyd Chern classes of $\mathcal{V}$.

But (eq:ECohomologyOfProjectiveBundle) holds on $\mathbb{C}P^n$ after [[pullback in cohomology|pullback]] along $fib_x$ (by standard arguments in [[complex oriented cohomology theory]], e.g. [Lurie 10, Lecture 4, Example 8](#LurieLecture)) and hence holds on $P(\mathcal{V})$ by the generalized-cohomology version of the [[Leray-Hirsch theorem]] ([Conner-Floyd 66, Thm. 7.4](#ConnerFloyd66)).

Since this construction is natural, one finds the following [[universal characteristic classes]] in $E$-cohomology:

+-- {: .num_prop #ConnerFloyedClasses}
###### Proposition

Given a [[complex oriented cohomology theory]] $E$ with complex orientation $c_1^E$, then the $E$-[[generalized cohomology]] of the [[classifying space]] $B U(n)$ is freely generated over the [[graded commutative ring]] $\pi_\bullet(E)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)) by classes $c_k^E$ for $0 \leq k \leq n$ of degree $2k$, these are called the **[[Conner-Floyd-Chern classes]]**

$$
  E^\bullet(B U(n))
    \;\simeq\;
  \pi_\bullet(E)[ [ c_1^E, c_2^E, \cdots, c_n^E ] ]
  \,.
$$

Moreover, pullback along the canonical inclusion $B U(n) \to B U(n+1)$ is the [[identity]] on $c_k^E$ for $k \leq n$ and sends $c_{n+1}^E$ to zero.

For $E = $ [[HA|HZ]] this reduces to the standard [[Chern classes]].

=--



## References

The concept was introduced for:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Theorems 7.5, 7.6 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

  > (with the example of [[MSp]]- and of [[MU]]-cohomology theory in Section 8)

An early account in a broader context of [[complex oriented cohomology theory]]:

* {#Adams74} [[Frank Adams]], part I.4, part II.2, part III.10 of _[[Stable homotopy and generalised homology]]_, 1974

More recent accounts:

* {#Kochmann96} [[Stanley Kochmann]], Section 4.3 of: _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, 2010, lecture 4 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf)) and lecture 5 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture5.pdf))




[[!redirects Conner-Floyd Chern classes]]

[[!redirects Conner-Floyd class]]
[[!redirects Conner-Floyd classes]]


[[!redirects Conner-Floyd-Chern class]]
[[!redirects Conner-Floyd-Chern classes]]


[[!redirects generalized Chern class]]
[[!redirects generalized Chern classes]]

[[!redirects generalised Chern class]]
[[!redirects generalised Chern classes]]