

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An **adjoint quadruple** is a sequence of three [[adjunctions]]

$$
  f_! \dashv f^* \dashv f_* \dashv f^!
$$

between a [[quadruple]] of [[morphisms]].  That is, it is an [[adjoint string]] of length 4.

## Properties

### General

Every adjoint quadruple 

$$
  (f_! \dashv f^* \dashv f_* \dashv f^!)
  :
  C 
    \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\stackrel{\overset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}}
  D
$$ 

induces an [[adjoint triple]] on $C$


$$
  (f^* f_! \dashv f^* f_* \dashv f^! f_*)
  :
  C \to C
  \,,
$$

(hence a [[monad]] [[left adjoint]] to a [[comonad]] left adjoint to a monad) and an adjoint triple

$$
  (f_! f^* \dashv f_* f^* \dashv f_* f^!) : D \to D
$$

on $D$.

Since moreover every [[adjoint triple]] $(F \dashv G \dashv H)$ induces an [[adjoint functor|adjoint pair]] $(G F \dashv G H)$ and an adjoint pair $(F G \dashv H G)$, the adjoint quadruple above induces four adjoint pairs, such as 

$$
  (f^* f_* f^* f_! \dashv f^* f_* f^! f_*) : C \to C
  \,.
$$

$\,$

### Canonical natural transformation

Let 

$$
  (p_! \dashv p^* \dashv p_*\dashv p^!) 
    \;\colon\; 
  \mathcal{E} 
    \longrightarrow 
  \mathcal{S}
$$

be an  [[adjoint quadruple]] of [[adjoint functor]]s such that $p^*$ and $p^!$ are [[full and faithful functor]]s. We record some general properties of such a setup.

We write 

$$
  \eta \;\colon\; id \to p^* p_!
$$

etc. for [[unit of an adjunction|units]] and

$$
  \epsilon \;\colon\; p_! p^* \to id
$$

etc. for counits.

+-- {: .num_prop #TheCanonicalMorphisms}
###### Proposition/Definition

We have [[commuting diagrams]], [[natural transformation|natural]] in $X \in \mathcal{E}$, $S \in \mathcal{S}$

$$
  \array{
    p_*X  &\underoverset{\simeq}{\epsilon_{p^* X}^{-1}}{\longrightarrow}& p_! p^* p_*X
    \\
    {}^{\mathllap{p_*(\eta_X)}}\downarrow 
    &\searrow^{\mathrlap{\theta_X}}& 
    \downarrow^{\mathrlap{p_!(\epsilon_X)}}
    \\
    p_* p^* p_! X &\stackrel{\eta_{p_!X}^{-1}}{\longrightarrow}& p_! X
  }
$$

and

$$
  \array{
    p^* S &\stackrel{\eta_{p^* S}}{\longrightarrow}& p^! p_* p^* S
    \\
    {}^{\mathllap{p^* \epsilon_S^{-1}}}\downarrow 
    &\searrow^{\mathrlap{\phi_X}}& \downarrow^{\mathrlap{p^!(\eta_S^{-1})}}
    \\
    p^* p_* p^!S  &\stackrel{{\epsilon}_{p_!S }}{\longrightarrow}& p^!S
  }
  \,.
$$

where the diagonal morphisms

$$
  \theta_X : p_* X \to p_! X
$$

and 

$$
  \phi_S : p^* S \to p^! S
$$

are defined to be the equal composites of the sides of these diagrams.

=--

This appears as ([Johnstone 11, lemma 2.1, corollary 2.2](#Johnstone11)).

+-- {: .num_prop #TheEpiAndTheMono}
###### Proposition

The following conditions are equivalent:


* for all $X \in \mathcal{E}$ the morphism $\theta_X : p_*X \to p_! X$ is an [[epimorphism]];

* for all $S \in \mathcal{S}$,, the morphism $\phi_S : p^*S \to p^! S$ 
  is a [[monomorphism]];

* $p_*$ is [[faithful functor|faithful]] on morphisms of the form $A \to p^* S$.

=--

This appears as ([Johnstone 11, lemma 2.3](#Johnstone11)).



+-- {: .proof}
###### Proof

By the above definition, $\phi_S$ is a [[monomorphism]] precisely if $\eta_{p^* S} : p^* S \to p^! p_* p^* S$ is. This in turn is so (see [[monomorphism]]) precisely if the first [[function]] in

$$  
    \mathcal{E}(A,p^* X) 
     \stackrel{(\eta_{p^* X}) \circ (-)}{\longrightarrow} 
    \mathcal{E}(A, p^! p_* p^* S)
     \stackrel{\simeq}{\longrightarrow}
    \mathcal{S}(p_* A, p_* p^* S)
$$

and hence the composite is a monomorphism in [[Set]].

By definition of [[adjunct]] and using the $(p_* \dashv p^!)$-[[zig-zag identity]], this is equal to the action of $p_*$ on morphisms

$$
  (\eta_{p^* X}) \circ (-)  : 
  (A \to p^* S) \mapsto p_*(A \to p^* S)  
  \,.
$$

Similarly, by the above definition the morphism $\theta_X$ is an epimorphism precisely if $p_!(\epsilon_X) : p_! p^* p_* X \to p_! X$ is so, which is the case precisely if the top morphism in

$$
  \array{
    \mathcal{S}(p_! X, S) 
      &\stackrel{(-) \circ p_!(\epsilon_X)}{\longrightarrow} &
    \mathcal{S}(p_! p^* p_* X, S)
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    && \mathcal{E}(p^* p_* X, p^* S)
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    \mathcal{E}(X, p^* S) &\stackrel{p_*}{\longrightarrow}& \mathcal{S}(p_* X, p_* p^* S)
  }
$$

and hence the bottom morphism is a monomorphism in [[Set]],
where again the commutativity of this diagram follows from the 
definition of [[adjunct]] and the 
$(p_! \dashv p^*)$-[[zig-zag identity]].

=--

$\,$



## Examples

### Via Kan extension of adjoint pairs
 {#ViaKanExtensionOfAdjointPairs}

A rich source of adjoint quadruples arises form [[adjoint pairs]] between [[small categoires]] by left/right [[Kan extension]] to their [[categories of presheaves]]. 

More interesting examples of adjoint quadruples tend to arise from these presheaf constructions when the quadruple ([[corestriction|co]])[[restriction|restricts]] to sub-[[categories of sheaves]].

We spell out two proofs of this fact, the first using [[coend]]-calculus in the generality of [[enriched category theory]], the second using more elementary [[colimit]]-notation.

\begin{prop}\label{KanExtensionOfAdjointPairIsAdjointQuadruple}
**([[Kan extension]] of [[adjoint pair]] is [[adjoint quadruple]])**
\linebreak
For $\mathcal{V}$ a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with all [[limits]] and [[colimits]], let $\mathcal{C}$, $\mathcal{D}$ be two [[small category|small]] $\mathcal{V}$-[[enriched categories]]and let

$$
  \mathcal{C}
    \underoverset
      {\underset{p}{\longrightarrow}}
      {\overset{q}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

be a $\mathcal{V}$-[[enriched adjunction]]. Then there are $\mathcal{V}$-[[enriched natural isomorphisms]]


$$
  (q^{op})^\ast \;\simeq\; Lan_{p^{op}}
  \;\colon\;
  [\mathcal{C}^{op},\mathcal{V}]
    \longrightarrow
  [\mathcal{D}^{op},\mathcal{V}]  
$$

$$
  (p^{op})^\ast \;\simeq\; Ran_{q^{op}}
  \;\colon\;
  [\mathcal{D}^{op},\mathcal{V}]
    \longrightarrow
  [\mathcal{C}^{op},\mathcal{V}]  
$$

between the precomposition on [[enriched presheaves]] with one functor and the left/right [[Kan extension]] of the other.

By essential uniqueness of [[adjoint functors]] ([this Prop.](adjoint+functor#UniquenessOfAdjoints)), this means that the two [[Kan extension]] [[adjoint triples]] of $q$ and $p$ 

$$
  \array{
    Lan_{q^{op}} &\dashv& (q^{op})^\ast &\dashv& Ran_{q^{op}}
    \\
    && Lan_{p^{op}} &\dashv& (p^{op})^\ast &\dashv& Ran_{p^{op}}
  }
$$

merge into an [[adjoint quadruple]]

$$
  \array{
    Lan_{q^{op}} &\dashv& (q^{op})^\ast &\dashv& (p^{op})^\ast &\dashv& Ran_{p^{op}}
  }
  \;\colon\;
  [\mathcal{C}^{op},\mathcal{V}]
    \leftrightarrow
  [\mathcal{D}^{op}, \mathcal{V}]
$$

\end{prop}
\begin{proof}
For every [[enriched presheaf]] $F \;\colon\; \mathcal{C}^{op} \to \mathcal{V}$ we have a sequence of $\mathcal{V}$-[[enriched natural isomorphism]] as follows

$$
  \begin{aligned}
    (Lan_{p^{op}} F)(d)
      & \simeq
    \int^{ c \in \mathcal{C} } \mathcal{D}(d,p(c)) \otimes F(c)
    \\
    & \simeq
    \int^{ c \in \mathcal{C} } \mathcal{C}(q(d),c) \otimes F(c)
    \\
    & \simeq
    F(q(d))
    \\
    & = \left( (q^{op})^\ast F\right) (d)
    \,.    
  \end{aligned}
$$

Here the first step is the [[coend]]-formula for [[left Kan extension]] ([here](Kan+extension#PointwiseByCoEnds)), the second step is the [[enriched adjunction]]-isomorphism for $q \dashv p$ and the third step is the [[co-Yoneda lemma]].

This shows the first statement. By essential uniqueness of adjoints ([this Prop.](adjoint+functor#UniquenessOfAdjoints)), the other statements follow.
\end{proof}


The following is the same argument without using coend-calculus. This argument applies verbatim also, for instance, in [[(infinity,1)-category theory|$\infty$-category theory]] using results from standard sources:

\begin{prop}\label{AdjointPairInducesAdjointQuadrupleUnderKanExtension}
Given a pair of [[adjoint functors]] between [[small categories]]
\begin{tikzcd}
    \mathcal{S}_1
    \ar[
      rr,
      shift left=7pt,
      "{ \ell }"{above}
    ]
    &&
    \mathcal{S}_2
    \ar[
      ll,
      shift left=7pt,
      "{ r }"{below}
    ]
    \ar[
      ll,
      phantom,
      "{ \scalebox{.6}{$\bot$} }"
    ]
\end{tikzcd}
the induced operations of pre-composition on [[categories of presheaves]] are adjoint to each other, $\ell^\ast \,\dashv\, r^\ast$, and their [[adjoint triples]] of [[Kan extensions]] overlap:

\begin{tikzcd}[column sep=large]
      \mathrm{PSh}(\mathcal{S}_1)
      \;\;
      \ar[
        rr,
        shift left=-7pt,
        "{ \ell_\ast \,\simeq\, r^\ast    }"{description}
      ]
      \ar[
        rr,
        shift left=32pt-7pt,
        "{ \ell_! }"{description, pos=.4}
      ]
      &&
      \;\;
      \mathrm{PSh}(\mathcal{S}_2)
      \ar[
        ll,
        shift right=16pt-7pt,
        "{ \ell^\ast \,\simeq\, r_! }"{description}
      ]
      \ar[
        ll,
        shift right=-16pt-7pt,
        "{ r_\ast }"{description, pos=.4}
      ]
      \ar[
        ll,
        phantom,
        shift right=8pt-7pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=24pt-7pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=-8pt-7pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
\end{tikzcd}
\end{prop}
\begin{proof}
The [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) which is characteristic of the adjunction $\ell^\ast \dashv r^\ast$ is the following sequence of [[natural bijections]]:

$$
  \begin{aligned}
      &
      \mathrm{PSh}(\mathcal{S}_1)
      \big(
        X_1
        ,\,
        r^\ast(X_2)
      \big)
      \\
      &
      \;\simeq\;
      \mathrm{PSh}(\mathcal{S}_1)
      \Big(
         \underset{
           \underset{
             s_1 \to X_1
           }{\longrightarrow}
         }{\lim}
         \,
        y(s_1)
        \,
        ,\,
        r^\ast
        \big(
         \underset{
           \underset{
             s_2 \to X_2
           }{\longrightarrow}
         }{\lim}
         \,
        y(s_2)
        \big)
      \Big)
      \\
      &
      \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \mathrm{PSh}(\mathcal{S}_1)
      \Big(
        y(s_1)
        ,\,
         \underset{
           \underset{
             s_2 \to X_2
           }{\longrightarrow}
         }{\lim}
         \,
        r^\ast
        \big(
          y(s_2)
        \big)
      \Big)
      \\
      &
      \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \,
         \underset{
           \underset{
             s_2 \to X_2
           }{\longrightarrow}
         }{\lim}
      \mathrm{PSh}(\mathcal{S}_1)
      \Big(
        y(s_1)
        ,\,
        r^\ast
        \big(
          y(s_2)
        \big)
      \Big)
      \\
      & \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \;
      \underset{
        \underset{
          s_2 \to X_2
        }{\longrightarrow}
      }{\lim}
      \mathcal{S}_2
      \big(
        r(s_1)
        ,\,
        s_2
      \big)
      \\
      & \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \;
      \underset{
        \underset{
          s_2 \to X_2
        }{\longrightarrow}
      }{\lim}
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        y\big(r(s_1)\big)
        ,\,
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        y\big(r(s_1)\big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        y\big(r(s_1)\big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        \mathcal{S}_2
        \big(
          (-)
          ,\,
          r(s_1)
        \big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        \mathcal{S}_2
        \big(
          \ell(-)
          ,\,
          s_1
        \big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
    PSh(\mathcal{S}_2)
      \Big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        \ell^\ast
        \big(
          y(s_1)
        \big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
    PSh(\mathcal{S}_2)
      \Big(
        \ell^\ast
        \big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        y(s_1)
        \big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
    PSh(\mathcal{S}_2)
      \Big(
        \ell^\ast
        (
          X_1
        )
        ,\,
        X_2
      \Big)
  \end{aligned}
$$
Here we used repeatedly

* the [[co-Yoneda lemma]] in the form

  $$
    X
    \;\simeq\;
    \underset{
      \underset{y(s) \to X}{\longrightarrow}
    }{\lim}
    \,y(s)
    \,,
  $$

  expressing a [[presheaf]] $X \,\in\, PSh(S)$ as a [[colimit]] of [[representable functors]] $y(s)$ (the colimit is over the [[comma category]] $y \downarrow X$, but that does not even matter in the proof above),

* the fact that any [[hom-functor preserves limits|hom-functor sends colimits in its first argument to limits]],

* the strong [[Yoneda lemma]] which says that $PSh(\mathcal{S})\big(y(s), X\big) \,\simeq\, X(s)$,

* the fact that [[colimits of presheaves are computed objectwise]].

As before, the adjunction $\ell^\ast \dashv r^\ast$ implies the overlapping adjoint triples by essential uniqueness of [[adjoint functors]] ([this Prop.](adjoint+functor#UniquenessOfAdjoints)).
\end{proof}



### Cohesion
 {#CohesiveToposes}


\begin{prop}\label{KanExtensionOfFiniteProductPreservingReflectionIsCohesiveAdjointQuadruple}
**(Kan extension of finite product preserving reflection is cohesive adjoint quadruple)**
\linebreak
  Let 

\begin{tikzcd}
  \mathcal{S}_1
  \ar[
    r,
    shift left=7pt,
    "{ p }"{above},
    "{ \mathclap{\times} }"{description, pos=.0}
  ]
  &
  \mathcal{S}_2
  \ar[
    l,
    shift left=7pt,
    hook',
    "{ i }"{below}
  ]
  \ar[
    l,
    phantom,
    "{\scalebox{.6}{$\bot$}}"{description}
  ]
\end{tikzcd}

be a pair of [[adjoint functors]] between [[small categories]] with [[finite products]], such that 

1. the [[right adjoint]] $i$ is [[fully faithful functor|fully faithful]],

1. the [[left adjoint]] $p$ [[preserves limits|preserves]] [[finite products]].

Then the induced adjoint quadruple of Kan extensions from Prop. \ref{AdjointPairInducesAdjointQuadrupleUnderKanExtension} is [[cohesive topos|cohesive]] in that

1. the two reverse functors are [[fully faithful functor|fully faithful]].

1. the leftmost adjoint $p_!$ [[preserved limit|preserves]] [[finite products]];

\begin{tikzcd}
  \mathrm{PSh}(\mathcal{S}_1)
      \ar[
        rr,
        "{ p_\ast \,\simeq\, i^\ast    }"{description}
      ]
      \ar[
        rr,
        shift left=40pt,
        "{ p_! }"{description, pos=.39},
        "\mathclap{\times}"{description, pos=0}
      ]
      &&
  \mathrm{PSh}(\mathcal{S}_1)
      \ar[
        ll,
        hook',
        shift right=20pt,
        "{ p^\ast \,\simeq\, i_! }"{description}
      ]
      \ar[
        ll,
        hook',
        shift right=-20pt,
        "{ i_\ast }"{description, pos=.39}
      ]
      \ar[
        ll,
        phantom,
        shift right=10pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=30pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=-10pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
\end{tikzcd}


\end{prop}
\begin{proof}
  The preservation of finite products by the leftmost adjoint follows by Prop. \ref{LeftKanExtensionOfFinProdPreservingIsFinProdPreserving} below.

The fully faithfulness of $i_!$ follows by Prop. \ref{LeftKanExtensionOfFullyFaithfulIsFullyFaithful} below. This implies that also $i_\ast$ is fully faithful, by [this Prop.](adjoint+triple#FullyFaithful).
\end{proof}

\begin{example}
Consider a [[site]] $\mathcal{S}$ with [[finite products]], in particular with a [[terminal object]]. Then the inclusion of the [[full subcategory]] on this  terminal object, which is the [[terminal category]] $\ast$ is an adjunction of the form

$$
  \mathcal{S}
  \underoverset
    {\underset{}{\hookleftarrow}}
    {\overset{}{\longrightarrow}}
    {\;\;\;\bot\;\;\;}
   \ast
  \,.
$$

If $\mathcal{S}$ is a *[[cohesive site]]* then the 
induced adjoint quadruple from Prop. \ref{KanExtensionOfFiniteProductPreservingReflectionIsCohesiveAdjointQuadruple} ([[corestriction|co]])[[restriction|restricts]] to the [[category of sheaves]] $Sh(\mathcal{S}) \xhookrightarrow{\;} PSh(\mathcal{S})$ and exhibits it as a [[cohesive topos]].
\end{example}

\linebreak

We now spell out the proof of the lemmas used in the proof of Prop. \ref{KanExtensionOfFiniteProductPreservingReflectionIsCohesiveAdjointQuadruple}.

\begin{lemma}\label{LeftKanExtensionIsOriginalFunctorOnRepresentables}
  Given a functor $\mathcal{S}_1 \xrightarrow{\;f\;} \mathcal{S}_2$ between [[small categories]], its [[left Kan extension]]
$f_! \;\colon\; PSh(\mathcal{S}_1) \xrightarrow{\;\;} PSh(\mathcal{S}_1)$ restricts to $f$ on [[representable functor|representables]], in that for $s_1 \,\in\, \mathcal{S}_1$ we have a [[natural isomorphism]]
$$
  f_!\big( y(s_1) \big)
  \;\simeq\;
  y\big(
    f(s_1)
  \big)
  \,.
$$
\end{lemma}
\begin{proof}
For $X \,\in\, PSh(\mathcal{S}_2)$
we have the following sequence of [[natural isomorphism]]:
$$
   \begin{aligned}
     PSh(\mathcal{S}_2)
     \left(
       f_!
       \left(
         y(s_1)
       \right)
       ,\,
       X
     \right)
         & \;\simeq\;
     PSh(\mathcal{S}_1)
     \left(
       y(s_1)
       ,\,
       f^\ast(X)
     \right)
     \\
     &
     \;\simeq\;
     X\left( f(s_1) \right)
     \\
     &
     \;\simeq\;
     PSh(\mathcal{S}_2)
     \left(
       y\left(f(s_1)\right)
       ,\,
       X
     \right)
     \,.
   \end{aligned}
$$  
The first line is the defining adjointness of $f_!$, the second line the [[Yoneda lemma]] over $\mathcal{S}_1$ and the definition of $f^\ast$, while the last line is the Yoneda lemma over $\mathcal{S}_2$.

Since the composite of these isomorphisms is natural, the [[Yoneda lemma]] over $PSh(\mathcal{S}_2)^{op}$ (which is [[large category|large]] but [[locally small category|locally small]], so that the lemma does apply) implies the claim.
\end{proof}
\begin{lemma}\label{LeftKanExtensionOfBinProductPreservingIsBinProductPres}
  Let $\mathcal{S}_1$ and $\mathcal{S}_2$ be [[small categories]] with [[binary products]] and $\mathcal{S}_1 \xrightarrow{\;f\;} \mathcal{S}_2$ a [[functor]] which [[preserved limit|preserves]] these, in that for $s, s' \,\in\, \mathcal{S}_1$ there is a [[natural isomorphism]] $f(s \times s') \,\simeq\, f(X_1) \times f(X_2)$. Then also the [[left Kan extension]] $f_!$ [[preserved limit|preserves]] [[binary products]], in that for $X, X' \,\in\, PSh(\mathcal{S}_1)$ there is a [[natural isomorphism]] 
$$
  f_!(X \times X')
  \;\simeq\;
  f_!(X) \times f_!(X')
  \,.
$$
\end{lemma}
\begin{proof}
This is the composite of the following sequence of [[natural isomorphisms]]:
$$
  \begin{aligned}
    f_!(X \times X')
       & \;\simeq\;
    f_!
    \Big(\!
      \big(
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
        \,
        y(s)
      \big)
      \times
      \big(
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
        \,
        y(s')
      \big)
    \!\Big)
    \\
    & \;\simeq\;
    f_!
    \Big(
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
        \;
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
        \,
      \left(
        y(s)
        \times
        y(s')
      \right)
    \!\!\Big)
    \\
    & \;\simeq\;
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
        \;
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
    \,
    f_!
      \big(
        y(s)
        \times
        y(s')
      \big)
    \\
    & \;\simeq\;
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
        \;
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
    \,
    f_!
      \big(
         y(s \times s')
      \big)
    \\
    & \;\simeq\;
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
        \;
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
    \,
    y\big(  f(s \times s') \big)
    \\
    & \;\simeq\;
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
        \;
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
    \,
    y\big(  f(s) \times f(s') \big)
    \\
    & \;\simeq\;
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
        \;
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
    \,
    y\big(  f(s) \big) 
      \times 
    y\big(f(s') \big)
    \\
    & \;\simeq\;
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
        \;
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
    \,
    f_!
      \left(
        y(s)
      \right)
   \times
    f_!
      \left(
        y(s')
      \right)
    \\
    & \;\simeq\;
    \Big(\,
        \underset{
          \underset{ s \to X}{\longrightarrow}
        }{\lim}
    \,
    f_!
      \left(
        y(s)
      \right)
   \!\!\Big)
   \times
   \Big(\,
        \underset{
          \underset{ s' \to X}{\longrightarrow}
        }{\lim}
    \,
    f_!
      \left(
        y(s')
      \right)
  \!\!\Big).
  \end{aligned}
$$  
Here 

* the first line is the [[co-Yoneda lemma]], expressing the [[presheaves]] as [[colimits]] of [[representable functor|representables]]. 

* The second line uses that in a [[topos]] (like [[Set]] or whatever the [[base topos]] may be) [[universal colimits|colimits are pullback-stable]] and in particular distribute over [[products]]. 

* The third line uses that $f_!$ is a [[left adjoint]] and that [[left adjoints preserve colimits]].

* Then inside the two colimits we use

  1. that the [[Yoneda embedding]] preserves [[limits]], in particular [[products]],

  1. Lem. \ref{LeftKanExtensionIsOriginalFunctorOnRepresentables}, to evaluate $f_!$ on representables as $f$,

  1. the assumption that $f$ preserves products.

* The last step is the first two steps in reverse.

\end{proof}

In conclusion:
\begin{prop}\label{LeftKanExtensionOfFinProdPreservingIsFinProdPreserving}
  If a [[functor]] $\mathcal{S}_1 \xrightarrow{\;f\;} \mathcal{S}_2$ between [[small categories]] with [[finite products]] [[preserved limit|preserves]] these, then so does its [[left Kan extension]] $f_! \,\colon\, PSh(\mathcal{S}_1) \xrightarrow{\;} PSh(\mathcal{S}_2)$.
\end{prop}
\begin{proof}
  We need to show that $f_!$ preserves (1) the [[terminal object]] and (2) [[binary products]]. With the given assumption on $f$, the first follows with Lem. \ref{LeftKanExtensionIsOriginalFunctorOnRepresentables} while the second follows with Lem. \ref{LeftKanExtensionOfBinProductPreservingIsBinProductPres}.
\end{proof}

\begin{proposition}\label{LeftKanExtensionOfFullyFaithfulIsFullyFaithful}
The left Kan extension $f_!$ of a [[fully faithful functor]] $f$ between [[small categories]] is itself fully faithful:
\begin{tikzcd}
    \mathcal{S}_1
    &
    \mathcal{S}_2
    \ar[
      l,
      hook',
      "{i}"{above}
    ]
  &
  \;\;\;\;  
  \Rightarrow
  \;\;\;\;
  &
    \mathrm{PSh}(\mathcal{S}_1)
    &
    \mathrm{PSh}(\mathcal{S}_2)
    \ar[
      l,
      hook',
      "{i_!}"{above}
    ]
\end{tikzcd}
\end{proposition}
\begin{proof}
  We need to show for $X, X' \,\in\, PSh(\mathcal{S}_2)$ the morphism
$$
  PSh(\mathcal{S}_2)
  (X,\, X')
  \xrightarrow{ \; (i_!)_{X, X'} \; }
  PSh(\mathcal{S}_`)
  \big(
    i_!(X)
    ,\, 
   i_!( X')
  \big)
$$
is an equivalence. But since $i_!$ is a left adjoint and since $X$ and $X'$ are colimits of representables, this morphism is the unique one which reduces to 
\[
  \label{ComponentIsomorphismOfAFullyFaithfulFunctor}
  \mathcal{S}_2
  (s,\, s')
  \xrightarrow{ \; i_{s, s'} \; }
  \mathcal{S}_1
  \big(
    i(s)
    ,\, 
   i( s')
  \big)
\]
on representables, where this is an isomorphism by the assumption that $i$ is fully faithful. If follows that $(i_!)_{X, X'}$, is the compostite of the following isomorphisms, and hence an isomorphism:
$$
  \begin{aligned}
    &
    PSh(\mathcal{S}_1)
    \big(
      i_!(X_1)
      ,\,
      i_!(X_2)
    \big)
    \\
    &
    \;\simeq\;
    PSh(\mathcal{S}_1)
    \Big(
      i_!
      \big(
      \underset{
        \underset{s \to X}{\longrightarrow}
      }{\lim}
        y(s)
      \big)
      ,\,
      i_!
      \big(
        \underset{
          \underset{s' \to X'}{\longrightarrow}
        }{\lim}
        y(s')
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    PSh(\mathcal{S}_1)
    \Big(
      \underset{
        \underset{s \to X}{\longrightarrow}
      }{\lim}
        i_!
        \big(
          y(s)
        \big)
      ,\,
      \underset{
        \underset{s' \to X'}{\longrightarrow}
      }{\lim}
        i_!
        \big(
          y(s')
        \big)
    \Big)
    \\
    &
    \;\simeq\;
    PSh(\mathcal{S}_1)
    \Big(
      \underset{
        \underset{s \to X}{\longrightarrow}
      }{\lim}
        y
        \big(
          i
          (s)
        \big)
      ,\,
      \underset{
        \underset{s' \to X'}{\longrightarrow}
      }{\lim}
        y
        \big(
          i(s')
        \big)
    \Big)
    \\
    &
    \;\simeq\;
    \underset{
    }{\lim}
      \underset{
        \underset{s' \to X'}{\longrightarrow}
      }{\lim}
    PSh(\mathcal{S}_1)
    \Big(
        y
        \big(
          i
          (s)
        \big)
      ,\,
        y
        \big(
          i(s')
        \big)
    \Big)
    \\
    &
    \;\simeq\;
    \underset{
      \underset{s \to X}{\longleftarrow}
    }{\lim}
      \underset{
        \underset{s' \to X'}{\longrightarrow}
      }{\lim}
    \mathcal{S}_1
    \big(
      i(s)
      ,\,
      i(s')
    \big)
    \\
    &
    \;\simeq\;
    \underset{
      \underset{s \to X}{\longleftarrow}
    }{\lim}
      \underset{
        \underset{s' \to X'}{\longrightarrow}
      }{\lim}
    \mathcal{S}_2
    \big(
      s
      ,\,
      s'
    \big)
    \\
    &
    \;\simeq\;
    \underset{
      \underset{s \to X}{\longleftarrow}
    }{\lim}
      \underset{
        \underset{s' \to X'}{\longrightarrow}
      }{\lim}
    PSh(\mathcal{S}_2)
    \big(
      y(s)
      ,\,
      y(s')
    \big)
    \\
    &
    \;\simeq\;
    PSh(\mathcal{S}_2)
    \Big(
      \underset{
        \underset{s \to X}{\longrightarrow}
      }{\lim}
      y(s)
      ,\,
      \underset{
        \underset{s' \to X'}{\longrightarrow}
      }{\lim}
      y(s')
    \Big)
    \\
    &
    \;\simeq\;
    PSh(\mathcal{S}_2)
    \big(
      X
      ,\,
      X'
    \big)
  \end{aligned}
$$
Here the first and last steps are the [[co-Yoneda lemma]] and the preservation of its colimits as in the proofs before. In the middle steps we are using Lem. \ref{LeftKanExtensionIsOriginalFunctorOnRepresentables} to evaluate $i_!$ on representables and then (eq:ComponentIsomorphismOfAFullyFaithfulFunctor) inside the (co)limits.
\end{proof}


## Related concepts

* [[adjunction]], [[adjoint functor]]

* [[adjoint triple]], [[adjoint string]]


## References

Prop. \ref{TheCanonicalMorphisms} is from:

* {#Johnstone11} [[Peter Johnstone]], _Remarks on punctual local connectedness_, Theory and Applications of Categories, Vol. 25, 2011, No. 3, pp 51-63.  ([tac](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))



[[!redirects adjoint quadruples]]