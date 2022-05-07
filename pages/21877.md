
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[projective spaces]] over [[ground ring]] $\mathbb{K}$ being the [[real numbers]] $\mathbb{R}$, [[complex numbers]] $\mathbb{C}$, [[quaternions]] $\mathbb{H}$ or [[octonions]] $\mathbb{O}$ admit, respectively, [[CW-complex|CW-]]-[[cell complex]] [[mathematical structure|structure]] with a single cell in each dimension $k$, $2 k$, $4 k$ or $8k$, respectively.

We discuss the cases $\mathbb{K} \,\in\, \{\mathbb{R}, \mathbb{C}, \mathbb{H}\}$. For the case $\mathbb{K} \,=\, \mathbb{O}$ see [Lackman 19, Lemma 3.4](#Lackman19)

## Preliminaries


Let $\mathbb{K} \,\in\, \big\{ \mathbb{R}, \mathbb{C}, \mathbb{H} \big\}$
be one of the [[associative algebra|associative]] [[real normed division algebras]], hence either the [[real numbers]], or the [[complex numbers]] or the [[quaternions]]. We regard this as a [[topological ring]] with respect to the canonical underlying [[topological space|topology]] of the [[Euclidean space]] $\mathbb{R}^{ dim_{_{\mathbb{R}}}(\mathbb{K}) }$.

For $n \in \mathbb{N}$, consider

$$
  \mathbb{K}P^n 
  \;\;
  \coloneqq
  \;\;
  \big(
    \mathbb{K}^{n+1} \setminus \{0\}
  \big) / \mathbb{K}^\times
$$

the $\mathbb{K}$-[[projective space]], i.e. the [[topological space|topological]] [[quotient space]] of the [[complement]] of zero in the $n+1$-fold [[Cartesian product]] of $\mathbb{K}$ by the right (say) [[multiplication]] [[action]] by the [[group of units]] $\mathbb{K}^\times \,=\, \mathbb{K} \setminus \{0\}$.

Notice the canonical [[topological subspace|subspace]] inclusion

$$
  \array{
    \mathbb{K}P^n
    &\hookrightarrow&
    \mathbb{K}P^{n+1}
    \\
    \big[
      z_0 \,:\, \cdots \,:\, z_n
    \big]
    &\mapsto&
    \big[
      z_0 \,:\, \cdots \,:\, z_n \,:\, 0
    \big]
    \,.
  }
$$

with induced [[complement]] $\mathbb{K}P^{n+1} \setminus \mathbb{K}P$ with [[topological boundary]]

$$
  \partial
  \big(
    \mathbb{K}P^{n+1} \setminus \mathbb{K}P
  \big)
  \;\;
    \coloneqq
  \;\;
  \overline{
    \big(
      \mathbb{K}P^{n+1} \setminus \mathbb{K}P
    \big)
  }
  \setminus
  \big(
    \mathbb{K}P^{n+1} \setminus \mathbb{K}P
  \big)
  \,.
$$

\linebreak

## Statement

+-- {: .num_prop #CellStructureOfKProjectiveSpace} 
###### Proposition
**(cell structure of $\mathbb{K}$-projective space)**

We have a [[pushout diagram]] in [in topological spaces](Top#UniversalConstructions) of the form

$$
  \array{
    D^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) }
    &\longrightarrow&
    \mathbb{K}P^{n+1}
    \\
    \big\uparrow
    &{}_{^{(po)}}&
    \big\uparrow
    \\
    S^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) - 1 }
    &\longrightarrow&
    \mathbb{K}P^n
  }
$$

exhibiting $\mathbb{K}P^{n+1}$ as the result of an $(n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K})$-[[cell attachment]] to $\mathbb{K}P^{n}$ with [[attaching map]] the canonical projection

$$
  \array{
     S^{(n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K})-1}
     \;\simeq\;
     \big(
       \mathbb{K}^{n+1} \setminus \{0\}
     \big) / \mathbb{R}_+^\times
     &\longrightarrow&
     \big(
       \mathbb{K}^{n+1} \setminus \{0\}
     \big) / \mathbb{K}^\times
     \;\simeq\;
     \mathbb{K}P^n
     \,.
  }
$$

=--


\begin{proof}
If we coordinatize the inclusion of consecutive projective spaces as
\[
  \label{CanonicalInclusionsOfProjectiveSpacesByInsertingZeroOnTheRight}
  \array{
    \mathbb{K}P^n
    &\overset{\;\;\;}{\hookrightarrow}&
    \mathbb{K}P^{n+1}
    \\
    [z_0 \colon \cdots \colon z_n ]
    &\mapsto&
    [z_0 \colon \cdots \colon z_n \colon 0]
  }
\]
then the [[complement]] of this inclusion inherits coordinatization as
$$
  \mathbb{K}P^{n+1}
  \setminus
  \mathbb{K}P^{n}
  \;=\;
  \big\{
    \left.
    [z_0 \colon \cdots \colon z_n \colon z_{n + 1}]
    \,\right\vert\,
    z_{n + 1} \neq 0
  \big\}
  \;\subset\;
  \mathbb{K}P^{n+1}
  \,.
$$

In terms of these coordinates, observe the following [[homeomorphism]]:

\[
  \label{TheHomeomorphism}
  \array{
    \mathbb{K}P^{n+1} \setminus \mathbb{K}P^n
    &\overset{\;\;\;\simeq\;\;\;}{\longrightarrow}&
    Int
    \big(
      D^{(n+1) dim_{{}_{\mathbb{R}}}(\mathbb{K})}
    \big)
    \,\simeq\,
    \left\{
      \big(
        y_0, \cdots, y_n, (1-r)
      \big)
      \,\left\vert\,
      \array{
         r \in [0,1) \subset \mathbb{R}\,,
         \\
         \left\vert \vec y \right\vert^2 + (1-r)^2  = 1 
      }
      \right.
    \right\}
    & 
    \subset 
    \mathbb{K}^{n+2}
    \\
    \big[
      z_0
      \,\colon\,
      \cdots
      \,\colon\,
      z_n
      \,\colon\,
      z_{n+1}
    \big]
    &\mapsto&
    \tfrac{1}{\left\vert \vec z\right\vert}
    \Big(
      z_0
      \cdot
      \tfrac{ z^\ast_{n+1} }{ \left\vert z_{n+1}\right\vert }
      \,,\,
      \cdots
      \,,\,
      z_n
      \cdot
      \tfrac{ z^\ast_{n+1} }{ \left\vert z_{n+1}\right\vert }
      \,,\,
      \left\vert z_{n+1}\right\vert
    \Big)
    \,.
  }
\]

In words this says: Given the class of a set of homogeneous coordinates with the last one non-zero, form the unique representative vector subject to the condition that:

1. its last coordinate is [[real number|real]];

1. its [[norm]] is unity.

Noticing that (eq:TheHomeomorphism) takes the [[topological boundary]] on the left to the boundary sphere as $r \to 1$ on the right, we see that the [[inverse morphism|inverse]] of this homeomorphism gives horizontal [[isomorphisms]] in a [[commuting square]] of the following form:

$$
  \array{
    D^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) }
    &\overset{\;\;\simeq\;\;}{\longrightarrow}&    
    \overline{
      \mathbb{K}P^{n+1}
      \setminus
      \mathbb{K}P^n
    }
    \\
    \big\uparrow
    &&
    \big\uparrow
    \\
    S^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) - 1 }
    &\overset{\;\;\simeq\;\;}{\longrightarrow}&    
    \partial
    \big(
      \mathbb{K}P^{n+1}
      \setminus
      \mathbb{K}P^n
    \big)
    \,.
  }
$$


But since $\mathbb{K}P^{n+1}$ is manifestly the union of its subspace $\mathbb{K}P^n$ with the [[topological closure]] of the [[complement]] of this subspace,
we have a pushout square as on the right of the following [[pasting diagram]]:

$$
  \array{
    D^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) }
    &\overset{\;\;\simeq\;\;}{\longrightarrow}&    
    \overline{
      \mathbb{K}P^{n+1}
      \setminus
      \mathbb{K}P^n
    }
    &\longrightarrow&
    \mathbb{K}P^{n+1}
    \\
    \big\uparrow
    &&
    \big\uparrow
    &{}_{^{(po)}}&
    \big\uparrow
    \\
    S^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) - 1 }
    &\overset{\;\;\simeq\;\;}{\longrightarrow}&    
    \partial
    \big(
      \mathbb{K}P^{n+1}
      \setminus
      \mathbb{K}P^n
    \big)
    &\longrightarrow&
    \mathbb{K}P^n
  }
$$

It follows that the total rectangle is a pushout (if you wish: by the [[pasting law]], using that all commuting squares with parallel isomorphisms are pushouts).
\end{proof}


+-- {: .num_prop #CellStructureOfKProjectiveSpace} 
###### Corollary
**([[CW-complex]]-[[mathematical structure|structure]] on $\mathbb{K}$-[[projective spaces]])**

The $\mathbb{K}$-[[projective spaces]] appear in [[cotowers]]

$$
  \ast \,\simeq\,
  \mathbb{K}P^0
  \overset{\phantom{AAA}}{\hookrightarrow}
  \mathbb{K}P^1
  \overset{\phantom{AAA}}{\hookrightarrow}
  \mathbb{K}P^2
  \overset{\phantom{AAA}}{\hookrightarrow}
  \cdots
  \overset{\phantom{AAA}}{\hookrightarrow}
  \mathbb{K}P^\infty
$$

which at each stage $n$ exhibit [[CW-complex]]-[[mathematical structure|structure]] on $\mathbb{K}P^n$ with single cells in degree $k \cdot dim_{\mathbb{R}}(\mathbb{K})$.


=--

## Consequences
 {#Consequences}

Fixing an [[orthonormal basis]] $\mathrm{i}, \mathrm{j}, \mathrm{k} \,\in\, \mathbb{H}$ of [[imaginary number|imaginary]] [[quaternions]] with $\mathrm{i} \cdot \mathrm{j} \,=\, \mathrm{k}$ induces, in particular, a [[star-algebra]] inclusion of the [[complex numbers]] into the [[quaternions]]

\begin{xymatrix@C=20pt}
  \mathbb{C}
  \;
  \ar@{^{(}->}[rr]
  &&
  \mathbb{H}
\end{xymatrix}

and a [[direct sum]] decomposition of $\mathbb{H}$ as a $\mathbb{C}$-[[bimodule]], with right action by direct right multiplication but left action by [[complex conjugation|complex conjugate]] left multiplication in the second variable:

\begin{xymatrix@C=20pt@R=6pt}
  \mathbb{C} \oplus \mathbb{C}^\ast
  \ar[rr]^-{ \simeq }
  &&
  \mathbb{H}
  \\
  ( z, z' )
  \ar@{|->}[rr]
  &&
  z + \mathrm{j} \cdot z' 
\end{xymatrix}


\begin{proposition}
  \label{CellStructureCompatibleUnderPassingFromCToH}
  Under a decomposition $\mathbb{H} \,\simeq\, \mathbb{C} \oplus \mathbb{C}^\ast$ as above, the cell structures on [[complex projective spaces]] and [[quaternionic projective spaces]] from Prop. \ref{CellStructureOfKProjectiveSpace} are compatible, in that for all $k \in \mathbb{N}$ we have a [[pasting diagram]] of the form

\begin{xymatrix@C=20pt}
  S^{4k+3}
  \;
  \ar@{^{(}->}[r]
  \ar[d]
  \ar@{}[dr]
    |-{
      \mbox{\tiny\rm(po)}
    }
  &
  D^{4k+4}
  \ar[d]
  \\
  \mathbb{C}P^{2k+1}
  \;
  \ar@{^{(}->}[r]
  \ar[d]
  \ar@{}[dr]
    |-{
      \mbox{\tiny\rm(po)}
    }
  &
  \mathbb{C}P^{2k+2}
  \ar[d]
  \\
  \mathbb{H}P^k
  \;
  \ar@{^{(}->}[r]
  &
  \mathbb{K}P^{k+1}
  \,,
\end{xymatrix}

where the top square and the total rectangle are the [[pushout]]-squares from Prop. \ref{CellStructureOfKProjectiveSpace}, while in the bottom square

1. the bottom left vertical morphism is the canonical projection (the "[[twistor fibration]]" for $k = 1$);

1. the bottom right vertical morphism is the canonical inclusion $\mathbb{C}P^{2k + 2} \hookrightarrow \mathbb{C}P^{2k+3}$ (eq:CanonicalInclusionsOfProjectiveSpacesByInsertingZeroOnTheRight) followed by that canonical projection.

In particular, it follows by the [[pasting law]] that this bottom square is also a [[pushout]].

\end{proposition}

\begin{proof}
  First, the bottom left morphism clearly has to be the claimed projection for the total left morphism to be the assumed projection.

  Next, by the [[universal property]] of the top [[pushout]], the bottom right morphism is unique once it is such as to induce the given total rectangle. So we just have to check that the total right vertical morphism factors as claimed. This is a straightforward unwinding of the construction of these morphisms in the proof of Prop. \ref{CellStructureOfKProjectiveSpace}. 

The following diagram means to make this evident for the case that $k = 1$:

\begin{xymatrix@R=6pt@C=4pt}
    &&
    &&
    \left\{
    \!
    \frac{
      (z_0 + \mathrm{j} \cdot z_1,
      z'_0 + \mathrm{j} \cdot z'_1, 0)
    }{
      \left\vert
        (z_0 + \mathrm{j} \cdot z_1,
         z'_0 + \mathrm{j} \cdot z'_1)
      \right\vert
    }
    \!
    \right\}
    \ar@{=}[d]
    \;
    \ar@{^{(}->}[rr]
    &&
    \left\{
    \!
    \frac{
      (z_0 + \mathrm{j} \cdot z_1,
      z'_0 + \mathrm{j} \cdot z'_1, 1-r)
    }{
      \left\vert
        (z_0 + \mathrm{j} \cdot z_1,
         z'_0 + \mathrm{j} \cdot z'_1, 1-r)
      \right\vert
    }
    \!
    \right\}
    \ar@{=}[d]
    \\
    S^7
    \;
    \ar@{^{(}->}[rr]
    \ar[dd]
    \ar@{}[ddrr]
    &&
    D^8
    \ar[dd]
    &&
    \left\{
    \!
    \frac{
      (z_0, z_1, z'_0, z'_1, 0)
    }{
      \left\vert  
        (z_0, z_1, z'_0, z'_1)
      \right\vert
    } 
    \!
    \right\}
    \;
    \ar@{^{(}->}[rr]
    \ar[dd]
    &&
    \left\{
    \!
    \frac{
      (z_0, z_1, z'_0, z'_1, 1-r)
    }{
      \left\vert
        (z_0, z_1, z'_0, z'_1, 1-r)
      \right\vert
    }
    \!
    \right\}    
    \ar[dd]
    \\
    \\
    \mathbb{C}P^3
    \;
    \ar@{^{(}->}[rr]
    \ar[dd]
    &&
    \mathbb{C}P^4
    \ar[dd]
    &&
    \big\{
      \!
      \scalebox{.7}{$
      \big[
        z_0 : z_1 :
        z'_0. : z'_1
      \big]
      \!
      $}
    \big\}
    \;
    \ar@{^{(}->}[rr]
    \ar[dd]
    &&
    \big\{
      \!
      \scalebox{.7}{$
      \big[
        z_0 : z_1 :
        z'_0. : z'_1 :
        1 - r
      \big]
      $}
      \!
    \big\}
    \ar[dd]
    \\
    \\
    \mathbb{H}P^1
    \;
    \ar@{^{(}->}[rr]
    &&
    \mathbb{H}P^2    
    && 
    \big\{
    \!
    \scalebox{.7}{$
      \big[
        z_0 + \mathrm{j} \cdot z_1
        :
        z'_0 + \mathrm{j} \cdot z'_1
      \big]
    $}
    \!
    \big\}
    \;
    \ar@{^{(}->}[rr]
    &&
    \big\{
    \!
    \scalebox{.7}{$
      \big[
        z_0 + \mathrm{j} \cdot z_1
        :
        z'_0 + \mathrm{j} \cdot z'_1
        :
        1 - r
      \big]
    $}
    \!
    \big\}
\end{xymatrix}

Here the notation closely alludes to the construction inside the proof of Prop. \ref{CellStructureOfKProjectiveSpace}: In particular $1-r$ denotes a _real_ number (regarded inside the complex numbers or quaternions under the chosen embedding above), using that there is always a homogeneous coordinate representative with the last entry of this form. With this understood, the maps are given by sending coordinate labels "to themselves", and, if necessary, by including a last coordinate $1 - r = 0$.

\end{proof}

## Related statements

* [[zero-section into Thom space of universal line bundle is weak equivalence]]

## References

The case of [[octonionic projective space]]:

* {#Lackman19} [[Malte Lackmann]], Lemma 3.4 in: _The octonionic projective plane_ ([arXiv:1909.07047](https://arxiv.org/abs/1909.07047))

[[!redirects cell structure of projective space]]

[[!redirects cell structure of K-projective spaces]]
[[!redirects cell structure of K-projective space]]

