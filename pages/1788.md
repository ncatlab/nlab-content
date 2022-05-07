


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

$$
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
$$


\begin{prop}
  Then the [[zero-section]] of the [[Thom space]] of the universal $\mathbb{K}$-line bundle
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
       \big\downarrow
       \\
       B \big(
         S(\mathbb{K})
       \big)
    } 
  $$  
  is a [[weak homotopy equivalence]].
\end{prop}


\begin{remark}
  \label{ComplexEOrientationsFromFirstEChernClass}
  **(complex $E$-orientations from first $E$-Chern class)**

To see that a generalized Chern class $c^E_1$ indeed has to do with _complex orientations_, namely of, first of all, [[fibers]] of [[complex line bundles]], notice that any [[complex projective space]] is equivalently the [[Thom space]] of the [[dual vector bundle|dual]] [[tautological line bundle]] (see [there](tautological+line+bundle#DualTautologicalLineBundle)) on the [[complex projective space]] of one complex dimension lower:

\begin{xymatrix@R=20pt@C=30pt}
    \mathllap{
      S^{2}
      =
      \;\;
    }
    \mathbb{C}P^1
    \ar@{^{(}->}[r]
    &
    \mathbb{C}P^2
    \ar@{=}[d]
    \ar@{^{(}->}[r]
    &
    \;\;
    \cdots
    \;\;
    \ar@{^{(}->}[r]
    &
    \mathbb{C}P^{n+1}
    \ar@{=}[d]
    \;
    \ar@{^{(}->}[rr]
      |-{
        \;
        \scalebox{.76}{
        \raisebox{-5pt}{$
          \cdots
        $}
        }
      \;}
    &
    &
    \mathbb{C}P^{\infty}
    \ar@{=}[d]
    \\
    &
    \mathrm{Th}
    \big(
      \mathcal{L}^\ast_{\mathbb{C}P^1}
    \big)
    \ar@{^{(}->}[r]
    &
    \;\;
    \cdots
    \;\;
    \ar@{^{(}->}[r]
    &
    \mathrm{Th}
    \big(
      \mathcal{L}^\ast_{\mathbb{C}P^n}
    \big)
    \;
    \ar@{^{(}->}[rr]
      |-{
        \;
        \scalebox{.76}{
        \raisebox{-5pt}{$
          \cdots
        $}
        }
      \;}
    &
    &
    \mathrm{Th}
    \big(
      \mathcal{L}^\ast_{\mathbb{C}P^\infty}
    \big)
    \ar@{=}[r]
    &
    \mathrm{Th}
    \big(
      E \mathrm{U}(1)
        \!\!
        \underset{\scalebox{.63}{$\mathrm{U}(1)$}}{\times}
        \!\!
      \mathbb{C}
    \big)
    \\
    \\
    &
    \mathllap{
      S^{2}
      =
      \;\;
    }
    \mathbb{C}P^1
    \ar@{^{(}->}[r]
    \ar[uu]
     |-{
       0_{{}_{
         \mathrm{Th}
         (
           \mathcal{L}^\ast_{\mathbb{C}P^1}
         )
       }}
       \mathclap{\phantom{\vert_{\vert_{\vert_{\vert}}}}}
     }
    &
    \;\;\cdots\;\;
    \ar@{^{(}->}[r]
    &
    \mathbb{C}P^{n}
    \ar[uu]
     |-{
       0_{{}_{
         \mathrm{Th}
         (
           \mathcal{L}^\ast_{\mathbb{C}P^n}
         )
       }}
       \mathclap{\phantom{\vert_{\vert_{\vert_{\vert}}}}}
     }
    \;
    \ar@{^{(}->}[rr]
      |-{
        \;
        \scalebox{.76}{
        \raisebox{-5pt}{$
          \cdots
        $}
        }
      \;}
    &
    &
    \mathbb{C}P^{\infty}
    \ar[uu]
     |-{
       0_{{}_{
         \mathrm{Th}
         (
           \mathcal{L}^\ast_{\mathbb{C}P^\infty}
         )
       }}
       \mathclap{\phantom{\vert_{\vert_{\vert_{\vert}}}}}
     }
     \ar@{=}[r]
     &
     B \mathrm{U}(1)
     \ar[uu]
     |-{
       \hspace{3pt}
       \scalebox{.7}{
         \rotatebox{-90}{$
           \;\simeq\;
         $}
       }
     }
\end{xymatrix}

The morphism of [E-cohomology Milnor sequences](lim1+and+Milnor+sequences#MilnorSequenceForGeneralizedCohomology) that this transformation induces shows (see the proof of Prop. \ref{CohomologyRingOfBU1ForComplexOrientedCohomologyTheory} for details) that [[pullback in cohomology|pullback]] along the [[zero section]] identifies the $E$-cohomology of the [[Thom space]] of the [[universal complex line bundle]] with that of the base [[classifying space]]:


\begin{xymatrix@R=26pt@C=30pt}
    \widetilde E {}^\bullet
    \big(
      S^2
    \big)
    \ar@{=}[d]
    \ar@{<-}[rr]^-{
      \mbox{
        \tiny
        \color{blue}
        \bf
        restriction to fiber
      }
    }
    &&
    \widetilde E {}^\bullet
    \Big(
      \mathrm{Th}
      \big(
        E \mathrm{U}(1)
          \underset{\scalebox{.6}{$\mathrm{U}(1)$}}{\times}
        \mathbb{C}
      \big)
    \Big)
    \ar[d]
     |-{
       \hspace{3pt}
       \scalebox{.7}{
         \rotatebox{-90}{$
           \;\simeq\;
         $}
       }
     }
    &
    \mathrm{th}^E_1
    \ar@{|->}[d]
    \\
    \widetilde E^{\bullet}
    \big(
      S^2
    \big)
    \ar@{<-}[rr]_-{
      \mbox{
        \tiny
        \color{blue}
        \bf
        restriction to $\mathbb{C}P^1 \subset \mathbb{C}P^\infty$
      }
    }
    &&
    \widetilde E {}^{\bullet}
    \big(
      B\mathrm{U}(1)
    \big)
    &
    c^E_1
\end{xymatrix}

(In fact the [[zero-section]] of the [[Thom space]] of the [[universal complex line bundle]] is itself a [[weak homotopy equivalence]], see [this Lemma](universal+complex+orientation+on+MU#UniversalComplexLineBundleThomSpace).)

But this shows the $E$-Chern class $c^E_1$ has a unique pre-image which is an $E$-[[Thom class]] $th^E_1$ on the [[universal complex line bundle]], and hence [[pullback in cohomology|pulls back]] to an $E$-[[Thom class]] on any [[complex line bundle]].

In fact more is true: The choice of $c^E_1$ induces a sequence of [[universal characteristic class|universal]] [[Conner-Floyd Chern classes]] $c^E_n$ for all $n \in \mathbb{N}$, and by an elaboration of the previous argument these are [[pullback in cohomology|pullbacks]] along the [[zero-section]] of universal $E$-[[Thom classes]] on the [[universal complex vector bundle]] of any [[rank]] $n$ (see [this Lemma](universal+complex+orientation+on+MU#UniversalComplexVectorBundleThomSpace)).



\linebreak

\linebreak



$$
  \array{
     \widetilde E {}^{\bullet}
     \big(
       S^2
     \big)     
     &\longleftarrow&
     \widetilde E {}^{\bullet}
     \Big(
       Th
       \big(
         E \mathrm{U}(1) \underset{\mathrm{U}(1)}{\times} \mathbb{C}
       \big)
     \Big)
     \\
     \big\downarrow^{  }     
     &&
     \big\downarrow^{  }
     \\ 
     \widetilde E {}^{\bullet}
     \big(
       S^2
     \big)     
     &\longleftarrow&
     \widetilde E {}^\bullet
     \big(
       B \mathrm{U}(1)
     \big)
  }
$$


\end{remark}

$$
  \array{
    [(v,z)]
    &\mapsto&
    [v,z] 
    &\mapsto& 
    [(0,v),z]
    &\mapsto& 
    [(0,v,z)]
    \\
    k P^{n+1}
    &=&
    Th
    \big(
      \mathcal{L}^\ast_{k P^n}
    \big)
    &
    \overset{\;\;\;\;\;\;}{\hookrightarrow}
    &
    Th
    \big(
      \mathcal{L}^\ast_{k P^{n+1}}
    \big)
    &=&
    k P^{n+2}
    \\
    &&
    {}^{\mathllap{zero \atop section}}
    \big\uparrow
    &{}^{{}_{(pb)}}&
    \big\uparrow
    {}^{\mathrlap{zero \atop section}}
    \\
    k P^n
    &=&
    k P^n
    &
    \overset{\;\;\;\;\;\;}{\hookrightarrow}
    &
    k P^{n+1}
    &=&
    k P^{n+1}
    \\
    [v]
    &\mapsto&
    [v] 
    &\mapsto& 
    [(0,v)]
    &\mapsto&
    [(0,v)]
    \,.
  }
$$



$$
  \array{
    \mathcal{L}^\ast_{k P^n}
    \overset{\;\;\;\;\;\;}{\hookrightarrow}
    \mathcal{L}^\ast_{k P^{n+1}}
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    k P^n
    &
    \overset{\;\;\;\;\;\;}{\hookrightarrow}
    &
    k P^{n+1}
    &
    \\
    [v] &\mapsto& [(0,v)]
  }
$$

\linebreak

\linebreak


$$
    x
    {\sqrt{1- 2 \delta y^2 + \epsilon y^4}}
    + 
    y 
    {\sqrt{1- 2 \delta x^2 + \epsilon x^4}}
$$


\begin{xymatrix@R=24pt@C=40pt}
  &
  S^2 \times S^2 
  \ar[d]
  \ar[rr]
    ^-{
      \scalebox{.65}{$
      {\begin{array}{l}
        \phantom{= -}
        c_1\big( \mathcal{L}_{\mathbb{C}P^1}  \big)
        \times 
        c_1\big( \mathcal{L}_{\mathbb{C}P^1}  \big)       
        \\
        =
        {\color{blue}-}
        c_1\big( \mathcal{L}^{\color{blue}\ast}_{\!\!\!\mathbb{C}P^1}  \big)
        \times
        c_1\big( \mathcal{L}_{\mathbb{C}P^1}  \big)       
      \end{array}
      }
      $}
    }
  && 
  E^2 \times E^2
  \ar[d]
  \\
  &
  S^2 \wedge S^2
  \ar@{-->}[rr]
    |-{
      \Sigma^2 (1^E) \wedge \Sigma^2 (1^E)
    }
  \ar@{=}[d]
  &&
  E^2 \wedge E^2
  \ar[d]
    |-{
      \mathclap{\phantom{\vert^{\vert}}}
      m^E
      \mathclap{\phantom{\vert_{\vert}}}
    }
  \\
  \mathbb{C}P^3
  \ar[r]
  \ar[d]
  &
  \mathbb{H}P^1
  \ar@{-->}[rr]
    |-{
      \; \Sigma^4(1^E) \;
    }
  \ar[d]
  &&
  E^4
  \\
  \mathbb{C}P^{\infty}
  \ar[r]
  &
  \mathbb{H}P^\infty
  \ar@{=}[r]
  &
  B \mathrm{SU}(2)
  \ar[ur]_-{ c_2 }
\end{xymatrix}


