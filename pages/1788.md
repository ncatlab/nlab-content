
$\ldots$

$\infty$


Please do not delete the following example for the moment!

An article by \cite{vandenBergGarner2011} and another by \cite{MarraReggio2020}.

\section{Van Kampen's Theorem}
Beep beep! Van Kampen's theorem concerns the [[fundamental group]] of a topological space.


\section{References}

\bibitem{MarraReggio2020}

\bibitem{vandenBergGarner2011}

\bibitem{AdámekRosícky2020}

\bibitem{FongSpivakTuyeras2017}

\linebreak

\bibitem{Witten1995}

\linebreak

$$
  \frac{13}{48}
  (
    p_2 - \frac{1}{4} p_1^2
  )
  -
  \frac{1}{4}
  (\frac{1}{4} p_1^2)
$$

$$
  \frac{13}{12}
  (
    p_2 - \frac{1}{4} p_1^2
  )
  -
  (\frac{1}{4} p_1^2)
$$

$$
  \frac{13}{12}
    p_2 

  -
  \frac{25}{12}
  (\frac{1}{4} p_1^2)
$$

$$
  13
  p_2 
  -
  5
  p_1^2
$$


* Claudia Cornella, Darius A. Faroughy, Javier Fuentes-Martin, [[Gino Isidori]], [[Matthias Neubert]], _Reading the footprints of the B-meson flavor anomalies_ ([arXiv:2103.16558](https://arxiv.org/abs/2103.16558))

> With the recent result $[$ of [[LHCb]] $]$, for the first time a single observable affected by negligible theoretical uncertainties exhibits a deviation from the SM exceeding the $3 \sigma$ level.  Equally striking is the overall coherence of the picture that emerges, especially in $b \to s \ell^+ \ell^-$ −transitions.  As we shall show in this paper, combining all the $b \to s \ell^+ \ell^-$−observables in a very conservative way, the significance of the New Physics (NP) hypothesis formulated in 2014–2015 of a purely left-handed LFU-violating contact interaction has now reached a [[statistical significance|significance]] of $4.6 \sigma$.

> $[\ldots]$  A more structural way of addressing the flavor structure of the model is the idea of implementing [[GUT|Pati-Salam unification]]

* {#Buras20}  [[Andrzej Buras]], _Gauge Theory of Weak Decays (2020) ([doi:10.1017/9781139524100](https://doi.org/10.1017/9781139524100) [CERN review](https://cerncourier.com/a/the-hitchhikers-guide-to-weak-decays/))

\begin{tikzcd}
  \mathrm{U} \times \Gamma
  \ar[
    out=180-66,
    in=66,
    looseness=3.5,
    "
    \scalebox{.77}{$
      \phantom{\cdot}
      \mathclap{
        \Gamma \rtimes_\alpha G
      }
      \phantom{\cdot}
    $}
    "{
      description
    },
    shift right=1
  ]
  \ar[rr]
  \ar[d]
  \ar[
    drr,
    phantom,
    "\mbox{\tiny\rm(pb)}"
  ]
  &&
  \mathrm{P}
  \ar[
    out=180-66,
    in=66,
    looseness=3.5,
    "
    \scalebox{.77}{$
      \phantom{\cdot}
      \mathclap{
        \Gamma \rtimes_\alpha G
      }
      \phantom{\cdot}
    $}
    "{
      description
    },
    shift right=1
  ]
  \ar[d]
  \\
  \mathllap{
    \exists
    \;
    \;\;
  }
  \mathrm{U}
  \ar[
    out=-180+66,
    in=-66,
    looseness=3.5,
    "
      \scalebox{.77}{$
        \mathclap{G}
      $}
    "{
      description
    },
    shift left=1
  ]
  \ar[
    ->>,
    rr,
    "
     \mbox{
       \tiny
       \rm
       open
     }
    "{
      below
    }
  ]
  &&
  \mathrm{X}
  \ar[
    out=-180+66,
    in=-66,
    looseness=3.5,
    "
      \scalebox{.77}{$
        \mathclap{G}
      $}
    "{
      description
    },
    shift left=1
  ]
\end{tikzcd}

\begin{tikzcd}
  U_x \times \Gamma
  \ar[
    out=180-66,
    in=66,
    looseness=3.5,
    "
    \scalebox{.77}{$
      \phantom{\cdot}
      \mathclap{
        \Gamma \rtimes_\alpha G_x
      }
      \phantom{\cdot}
    $}
    "{
      description
    },
    shift right=1
  ]
  \ar[rr]
  \ar[d]
  \ar[
    drr,
    phantom,
    "\mbox{\tiny\rm(pb)}"
  ]
  &&
  \mathrm{P}
  \ar[
    out=180-66,
    in=66,
    looseness=3.5,
    "
    \scalebox{.77}{$
      \phantom{\cdot}
      \mathclap{
        \Gamma \rtimes_\alpha G_x
      }
      \phantom{\cdot}
    $}
    "{
      description
    },
    shift right=1
  ]
  \ar[d]
  \\
  \mathllap{
    \exists
    \;
    \;\;
  }
  U_x
  \ar[
    out=-180+66,
    in=-66,
    looseness=3.5,
    "
      \scalebox{.77}{$
        \mathclap{G}
      $}
    "{
      description
    },
    shift left=1
  ]
  \ar[
    ->>,
    rr,
    "
     \mbox{
       \tiny
       \rm
       open
     }
    "{
      below
    }
  ]
  &&
  X
  \ar[
    out=-180+66,
    in=-66,
    looseness=3.5,
    "
      \scalebox{.77}{$
        \mathclap{G}
      $}
    "{
      description
    },
    shift left=1
  ]
\end{tikzcd}


\begin{defn}
 aaa
\end{defn}

### Notions of equivariant local triviality
 {#NotionsOfEquivariantLocalTriviality}

In the internal definition
[above](#EquivariantLocalTriviality),
we demanded an equivariant fiber/principal bundle to be locally trivial in the evident sense *[[internalization|internal]]* to [[TopologicalGActions]]. But in the literature various variants of this notion are considered. We discuss how (some of) these are related to each other:



\begin{definition}
**(tom Dieck's equivariant local triviality condition -- [tom Dieck 69, Def. 2.3](#tomDieck69), [tom Dieck 87, p. 58](#tomDieck87))**
  An equivariant principal bundle 
  (Def. \ref{EquivariantPrincipalBundles}, Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles})  
  $$
    P \overset{p}{\longrightarrow} B
    \;\;
    \in
    \;
    (\Gamma,\alpha)PrincipalBundles
  $$
  is **[[locally trivial]]** if there exists 

1. an index-[[set]] $I$,

1. an $I$-[[indexed set]] of [[topological subspace|sub]]-[[topological G-space|G-spaces]]
 
   $$
     U_i \;\subset\; B
     \;\;
     \in
     G Actions
     \big(
      TopologicalSpaces 
     \big)
   $$

1. an $I$-[[indexed set]] of [[closed subgroup]] $H_i \subset G$;

1. an $I$-[[indexed set]] of $E_i \overset{p_i}{\to} G/H_i \;\in\; (\Gamma,\alpha)PrincipalBundles$ over their [[coset spaces]];

such that 

1. $\big\{ U_i \hookrightarrow B \big\}_{i \in I}$ is an [[open cover]] in [[TopologicalSpaces]];

1. for each $i \in I$ there is a [[homomorphism]] of $(\Gamma,\alpha)PrincipalBundles$

   $$
     \array{
       E_{\vert U_i}
       &
         \overset{}{\longrightarrow}
       &
       E_i
       \\
       \big\downarrow
       &
         {}^{{}_{(pb)}}
       &
       \big\downarrow {}^{\mathrlap{p}}
       \\
       U_i
       &\longrightarrow&
       G/H
     }
   $$

   from the restriction of $E$ to $U_i$ and the given  equivariant bundle over the coset space.

\end{definition}

\begin{definition}
**(Bierstone's equivariant local triviality condition -- [Bierstone 78, Sec. 4, p. 619-620](#Bierstone78))**
  An equivariant principal bundle 
  (Def. \ref{EquivariantPrincipalBundles}, Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles})  

  $$
    P \overset{p}{\longrightarrow} X
    \;\;
    \in
    \;
    (\Gamma,\alpha)PrincipalBundles
  $$

  is **[[locally trivial]]** if for each point $x \in X$ (with [[isotropy 
group]]/[[stabilizer group]] denoted $G_x \coloneqq Stab_G(x) \subset X$) there exists 

1. an [[open neighbourhood]] 

   $$
     U_x 
       \;\subset\; 
     X \;\; \in \; G_x Actions(TopologicalSpaces)
   $$

1. an [[isomorphism]] of $G_x Actions(TopologicalSpaces)_{/U_x}$

   $$
     \array{
       P_{\vert U_x}
       &
         \longrightarrow
       &
       U_x \times p^{-1}(\{x\})
       \\
       {}^{\mathllap{ p_{\vert U_x} }}
       \big\downarrow
         &&
       \big\downarrow
       {}^{
         \mathrlap{ pr_1 }
       }
       \\
       U_x &=& U_x
     }
   $$

   from the restriction of $P$ to $U_x$ to the [[Cartesian product]] of $U_x$ with the [[fiber]] of $P$ over $x$.

\end{definition}



