+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

In broad generality, the relation between (non-[[equivariant stable homotopy theory|stable]]) [[global equivariant homotopy theory]] and $G$-[[equivariant homotopy theory]] for any fixed admissible [[equivariance group]] $G$ may be organized and formalized as follows: 

The [[slice (infinity,1)-topos|slice]] of [[global equivariant homotopy theory]] over the archetypical $G$-[[orbi-singularity]] $\prec G$ is [[cohesive (infinity,1)-topos|cohesive]] over $G$-[[equivariant homotopy theory]]. In particular: 

1. $G$-equivariant homotopy theory [[full sub-(infinity,1)-category|faithfully embeds]] into the $\prec G$-slice of the global theory in two different ways, one of them interpreted as the inclusion of [[G-spaces]] $X$ as [[global quotient orbifold|global]] [[orbispaces]] $X \sslash G$, 

1. these inclusions have a compatible pair of [[reflective sub-(infinity,1)-category|reflections]], one of which forms the [[spaces of sections]] over the $G$-singularity $\prec G$.


This observation is due to [Rezk 2014](#Rezk14), where this is proven by direct construction of the respective [[adjoint quadruple]] of [[(infinity,1)-functors|$\infty$-functors]]. Below we discuss how the evident [[reflective (infinity,1)-category|reflection]] of the $G$-[[orbit category]] inside the $\prec G$-[[slice (infinity,1)-category|slice]] of the "[[global orbit category]]" (see Rem. \ref{TerminologySingularities} below) immediately induces this cohesive relation by [[(infinity,1)-Kan extension|$\infty$-Kan extension]].


## Preliminaries

\begin{remark}
**equivariance groups)**
\linebreak
Throughout we consider [[discrete group|discrete]] [[equivariance groups]], not necessarily [[finite group|finite]] (though [[subgroups]] of interest will be finite, as in [[proper equivariant homotopy theory]]). Much of the following also works for equivariance groups which are [[compact Lie groups]], but some definitions become a tad more laborious to state and the relation to [[smooth infinity-groupoids|smooth cohesion]] gets messed up.
\end{remark}

\begin{definition}\label{CategoryOfOrbiSingularities}
**(canonical orbi-singularities)**
  We write 
  $$
    \array{
    Snglrt
    &\coloneqq&
    Grpd^{fin}_{1, \geq 1}
    &\xhookrightarrow{\;}&
    Grp_\infty
    \\
    \prec G && \mapsto && B G
    }
  $$
  for the [ful sub-(infinity,1)-category|full sub-$\infty$-category]]  of all [[infinity-groupoids|$\infty$-groupoids]] on those that are

1. [[n-connected object of an (infinity,1)-topos|0-connected]]

1. [[n-truncated object of an (infinity,1)-category|1-truncated]]

1. [[pi-finite homotopy type|$\pi$-finite]],

hence, [[equivalence of (infinity,1)-categories|equivalently]], the full sub-[[(2,1)-category]] of [[Grpd]] on the [[delooping grouopoids]] $\mathbf{B}G$ of [[finite groups]] $G$, hence with [[functors]] as [[1-morphisms]] and [[natural transformations]] (necessarily [[natural isomorphisms]]) as [[2-moprhisms]].
\end{definition}
\begin{remark}\label{TerminologySingularities}
**(terminology: singularities vs. "global orbits")**
\linebreak
  The $(2,1)$-category in Def. \ref{CategoryOfOrbiSingularities}
is sometimes called the *[[global orbit category]]*, though other times that name refers to its non-full subcategory on the [[faithful functors]]. But *neither* of these two actually is a "category of orbits" -- instead, orbit categories are full subcategories of their slices!, by Prop. ... below). On the other hand, application of [[global equivariant homotopy theory]] to [[orbifolds]] identifies the category in Def. \ref{CategoryOfOrbiSingularities} with the category of archetypical local models for [[orb-singularities]]. Therefore the choice of notation in Def. \ref{CategoryOfOrbiSingularities}.
\end{remark}

\begin{definition}
For $\mathbf{H}$ an [[(infinity,1)-topos|$\infty$]] write

$$
  Glo \mathbf{H}
  \;\coloneqq\;
  Sh_\infty( Singlrt ,\, \mathbf{H} )
$$

for the [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-topos of $\infty$-presheaves]] on $Snglrt$ (Def. \ref{CategoryOfOrbiSingularities}), to be called the *[[global equivariant homotopy theory]]* over $\mathbf{H}$.

Moreover, for $G \,\in\, Grp(FinSet)$, write

$$
  G \mathbf{H}
  \;\coloneq\;
  Sh_\infty( G Orbt ,\, \mathbf{H} )
$$

for the [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-topos of $\infty$-presheaves]] on the $G$-[[orbit category]] $G Orbt$ (Def. \ref{}), to be called the $G$-*[[equivariant homotopy theory]]* over $\mathbf{H}$.
\end{definition}

## Statement

\begin{proposition}

\begin{tikzcd}[row sep=0pt]
  \mathrm{Sngrlt}_{/\prec G}
  \ar[
    rr,
    shift left=7pt,
    "\tau_0"
  ]
  &&
  G Orbt
  \ar[
    ll,
    hook,
    shift left=7pt
  ]
  \ar[
    ll,
    phantom,
    "{ \scalebox{.5}{$\bot$} }"
  ]
  \\
  \left(
  \!\!
  \begin{array}{c}
    \prec\!\! H
    \\
    \downarrow^{\mathrlap{\scalebox{.7}{$\prec\! i_H$}}}
    \\  
    \prec\!\! G
  \end{array}
  \right)
  \ar[
    rr,
    phantom,
    "{ \mapsto }"{description, rotate=180}
  ]
  &&
  G/H
\end{tikzcd}
\end{proposition}

\begin{prop} 
\begin{tikzcd}[column sep=30pt]
  \mathrm{Glo} \mathbf{H}
      \ar[
        rr,
        "{ \tau_\ast \,\simeq\, i^\ast    }"{description}
      ]
      \ar[
        rr,
        shift left=32pt,
        "{ \tau_! }"{description, pos=.35},
        "\mathclap{\times}"{description, pos=0}
      ]
      &&
     G \mathbf{H}
      \ar[
        ll,
        hook',
        shift right=16pt,
        "{ \tau^\ast \,\simeq\, i_! }"{description}
      ]
      \ar[
        ll,
        hook',
        shift right=-15pt,
        "{ i_\ast }"{description, pos=.35}
      ]
      \ar[
        ll,
        phantom,
        shift right=8pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=22pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=-8pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
\end{tikzcd}
\end{prop}
\begin{proof}
  By [[(infinity,1)-Kan extension|Kan extension]].
\end{proof}


## References

The observation and original proof of the relation is due to:

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)

Some of the notation and terminology above follows:

* {#SatiSchreiber20} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))
