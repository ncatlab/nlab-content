
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[Thom space]] of the [[universal complex line bundle]] is [[weak homotopy equivalence|weakly homotopy equivalent]] to the base space of the line bundle, hence to the [[classifying space]] for the [[circle group]], and this is equivalence is exhibited by the [[zero section]] of the universal line bundle, followed by its inclusion into its [[Thom space]] ([Adams 74, Part I, Example 2.1](#Adams74)).

This statement plays a key role in the discussion of [[complex oriented cohomology]], as it implies that any choice of [[universal characteristic class|universal]] first [[Conner-Floyd Chern class]] $c^E_1$ is equivalent to a choice of universal [[Thom class]] on the [[universal complex line bundle]], and hence induces a Thom class, hence a "fiberwise complex orientation" on any [[complex line bundle]]. (See at _[Conner-Floyd E-Chern classes are E-Thom classes](universal+complex+orientation+on+MU#ConnerFloydChernClassesAreThomClasses)_ for more on this.) 

In this context the statement is naturally stated in the form

$$
  B \mathrm{U}(1) \overset{\simeq}{\longrightarrow} M \mathrm{U}(1)
  \,,
$$

where on the right the [[Thom space]] is thought of as the component space in degree 2 (complex degree 1) of the universal [[unitary group|unitary]] [[Thom spectrum]] [[MU]]. 

The analogous statement is true also for the universal [[real vector bundle|real]]- and [[quaternionic line bundle|quaternionic]] [[line bundles]], and it implies the analogous consequence for [[quaternionic oriented cohomology theory]], etc., notably

$$
  B Sp(1) \overset{\simeq}{\longrightarrow} M Sp(1)
  \,,
$$


where on the right the [[Thom space]] is thought of as the component space in degree 4 (quaternionic degree 1) of the universal [[quaternionic unitary group|quaternionic unitary]] [[Thom spectrum]] [[MSp]]. 




## Preliminaries

### The universal line bundle


Let $\mathbb{K} \,\in\, \{\mathbb{R}, \mathbb{C}, \mathbb{H}\}$
be the [[real numbers]] or [[complex numbers]] or [[quaternions]].
Write 

\[
  \label{GroupOfUnitNormElements}
  S(\mathbb{K})
  \;\coloneqq\;
  \big\{
    q \in \mathbb{K}
    \;\big\vert\;
    q q^\ast =1
  \big\}
  \;\;
  \in
  \;
  Groups
\]

for its [[multiplicative group]] of unit-[[norm]] elements. Specifically this is the [[cyclic group of order 2]], the [[circle group]] or the [[quaternionic unitary group]]/[[SU(2)]]:

$$
  S(\mathbb{R})
  \,\simeq\,
  \mathbb{Z}/2
  \,,
  \phantom{AA}
  S(\mathbb{C})
  \,\simeq\,
  \mathrm{U}(1)
  \,,
  \phantom{AA}
  S(\mathbb{H})
  \,\simeq\,
  Sp(1) \,\simeq\, SU(2)
$$

By either left or right multiplication in $\mathbb{K}$ this group [[action|acts]] on $\mathbb{K}$, $\mathbb{R}$-[[linear map|linearly]], making $\mathbb{K}$ a [[linear representation]]

\[
  \label{KAsSKRepresentation}
  \mathbb{K} 
    \,\in\,
  S(\mathbb{K})
  Representations_{\mathbb{R}}
  \,.
\]

Hence with

$$
  E
  \big(
    S(\mathbb{K}) 
  \big)
  \overset{\;\;\;}{\longrightarrow}
  B 
  \big(
    S(\mathbb{K}) 
  \big)
$$

denoting the $S(\mathbb{K})$-[[universal principal bundle]] over the [[classifying space]] for the group (eq:GroupOfUnitNormElements), the [[real vector bundle]] underlying the [[universal complex line bundle|universal K-line bundle]] is the corresponding [[associated bundle]] via the above action (eq:KAsSKRepresentation):

\[
  \label{UniversalKLineBundle}
  \array{
     E 
     \big(
       S(\mathbb{K})
     \big) 
     \underset{
       S(\mathbb{K})
     }{\times}
     \mathbb{K}
     \\
     \big\downarrow
     \\
     B 
     \big( 
       S(\mathbb{K})
     \big)
  } 
\]

### Thom spaces

The [[Thom space]] of a [[real vector bundle|real]] [[topological vector bundle]] $\mathcal{V}_X$ over some base space $X$ is the [[homotopy cofiber]] of its associated [[spherical fibration]]:

\[
  \label{ThomSpaceAsHomotopyCofiber}
  S_X(\mathcal{V}_X)
  \overset{ p_{S(\mathcal{V}_X)} }{\longrightarrow} 
  X
  \overset{ hocofib }{\longrightarrow} 
  Th(X)
  \,.
\]

When the [[topological space]] $X$ has the [[mathematical structure|structure]] of a [[CW-complex]] then a [[cofibration]] which models the [[homotopy type]] of $p_{S(\mathcal{V}_X)}$ in the [[classical model structure on topological spaces]] is the inclusion of the unit [[sphere bundle]]  into the unit disk bundle $D_X(\mathcal{V}_X)$ of $\mathcal{V}_X$ (with respect to any choice of fiberwise [[metric]]) since this is then a [[relative cell complex]]-inclusion. Therefore the homotopy cofiber (eq:ThomSpaceAsHomotopyCofiber) is then represented by the [[1-category|1-category theoretic]] [[cofiber]]

\[
  \label{ThomSpaceAsActualCofiber}
  S_X(\mathcal{V}_X)
  \overset{ i_{S_X(\mathcal{V}_X)} }{\longrightarrow} 
  D_X(\mathcal{V}_X)
  \overset{ cofib }{\longrightarrow} 
  Th(X)
  \,.
\]

Finally, since the [[zero section]] of the unit disk bundle is manifestly the  [[weak homotopy equivalence]] that exibits this [[cofibrant resolution]], we may call

\[
  \label{ZeroSectionIntoTheThomSpace}
  0_X
  \;\colon\;
  X
    \underoverset
    {\simeq}
    {
      0_{D_X(\mathcal{V}_X)}
    }
    {\longrightarrow}
  D(\mathcal{V}_X)
   \overset
    {cofib\big(  i_{S_X(\mathcal{V}_X)} \big)}
    {\longrightarrow}
  Th(X)
\]

the zero-section _into_ the Thom spaces.




## Statement

\begin{prop}
  The zero-section (eq:ZeroSectionIntoTheThomSpace) into the [[Thom space]] of the universal $\mathbb{K}$-line bundle (eq:UniversalKLineBundle)

  $$
    \array{
       Th
       \Big( 
         E (S(\mathbb{K})) 
         \underset{
           S(\mathbb{K})
         }{\times}
         \mathbb{K}
       \Big)
       \\
       {}^{{}_{\mathllap{
         0_{
           B \big(
             S(\mathbb{K})
           \big)        
         }
       }}}
       \big\uparrow 
       {}^{{}_{
         \mathrlap{\simeq}}
       }
       \\
       B \big(
         S(\mathbb{K})
       \big)
    } 

  $$  
  is a [[weak homotopy equivalence]].
\end{prop}

\begin{proof}
  The point is that for the universal _line_ bundle, the associated [[sphere bundle]] is [[homotopy equivalent]] to the [[universal principal bundle]] and hence [[contractible homotopy type|contractible]]:

$$
  S_{B \big(S(\mathbb{K})\big)}
  \Big(
    E\big(S(\mathbb{K})\big)
I       \underset{S(\mathbb{K})}{\times}
    \mathbb{K}
  \Big)
  \;=\;
  \Big(
    E\big(S(\mathbb{K})\big)
      \underset{S(\mathbb{K})}{\times}
    S(\mathbb{K})
  \Big)
   \;=\;
  E\big(S(\mathbb{K})\big)
    \;\simeq\;
  \ast
  \,.
$$

This means that we have the following solid [[commuting diagram]], where the solid vertical morphisms are all [[weak homotopy equivalences]]:

\begin{xymatrix@R=25pt@C=50pt}
      && &&
      B(S(\mathbb{K}))
      \ar[d]
        _-{
           0
        }
        |-{
          \hspace{3pt}
          \scalebox{.7}{
            \rotatebox{-90}{$
              \;\simeq\;
            $}
          }
        }
      \\
      \ast
      \;
      \ar@{^{(}->}[rr]_-{ \in \, \mathrm{Cofibrations} }
      \ar[d]
        |-{
          \hspace{3pt}
          \scalebox{.7}{
            \rotatebox{-90}{$
              \;\simeq\;
            $}
          }
        }
      &&
      D_{B(S(\mathbb{K}))}
      \Big(
        E\big( S(\mathbb{K}) \big)
          \underset{S(\mathbb{K})}{\times}
        \mathbb{K}
      \Big)
      \ar[rr]
        ^-{ \mbox{\tiny cofiber} }
        _-{ \mbox{\tiny $\Rightarrow$ homotopy cofiber} }
      \ar@{=}[d]
      &&
      D_{B(S(\mathbb{K}))}
      \Big(
        E\big( S(\mathbb{K}) \big)
          \underset{S(\mathbb{K})}{\times}
        \mathbb{K}
      \Big)
      \ar@{-->}[d]
      \\
      S_{B(S(\mathbb{K}))}
      \Big(
        E\big( S(\mathbb{K}) \big)
          \underset{S(\mathbb{K})}{\times}
        \mathbb{K}
      \Big)
      \;
      \ar@{^{(}->}[rr]
        _-{ \in \, \mathrm{Cofibrations} }
      &&
      D_{B(S(\mathbb{K}))}
      \Big(
        E\big( S(\mathbb{K}) \big)
          \underset{S(\mathbb{K})}{\times}
        \mathbb{K}
      \Big)
      \ar[rr]
        ^-{ \mbox{\tiny cofiber} }
        _-{ \mbox{\tiny $\Rightarrow$ homotopy cofiber} }
      &&
      \mathrm{Th}
      \Big(
        E\big( S(\mathbb{K}) \big)
          \underset{S(\mathbb{K})}{\times}
        \mathbb{K}
      \Big)
\end{xymatrix}

(Here the left vertical map picks any point of the sphere bundle. There is then a unqique horizontal map on the left to make the left square [[commuting diagram|commute]].)

Now, since the [[classifying space]] $B(S(\mathbb{K}))$ does have the structure of a [[CW-complex]] (given, for instance, by its realization as infinite [[real projective space|real]]/[[complex projective space|complex]]/[[quaternionic projective space|quaternionic]] [[projective space]] $\mathbb{K}P^\infty$), the bottom [[cofiber]] here represents, as in (eq:ThomSpaceAsActualCofiber), the defining [[homotopy cofiber]]. 

Since [[homotopy cofibers]] are preserved, up to [[weak equivalence]], by weak equivalences of their diagrams (by [this Prop.](Introduction+to+Homotopy+Theory#FiberOfFibrationIsCompatibleWithWeakEquivalences)), it follows that the dashed vertical morphism is a weak equivalence in the [[classical model structure on topological spaces]], hence a [[weak homotopy equivalence]]. 

This is the statement that was to be shown. Or more explicitly: By [[two-out-of-three]] also the [[composition|composite]] vertical morphism on the right is a weak homotopy equivalence, which is the desired morphism in the form (eq:ZeroSectionIntoTheThomSpace).
\end{proof}

## Related statements

* [Conner-Floyd E-Chern classes are E-Thom classes](universal+complex+orientation+on+MU#ConnerFloydChernClassesAreThomClasses)

See also:


* [[complex oriented cohomology]], [[universal complex orientation on MU]]

* [[quaternionic oriented cohomology]]

## References

Early appearance of the statement:

* {#Adams74} [[Frank Adams]], Part I, Example 2.1 in: _[[Stable homotopy and generalised homology]]_, 1974



[[!redirects zero-section into Thom space of universal line bundle is weak homotopy equivalence]]
