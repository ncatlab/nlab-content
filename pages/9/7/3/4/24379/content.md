
> Not to be confused with *[[group completion]]*.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of comtents
{:toc}


## Idea

(...)

## Definition


\begin{definition}\label{RCompleteGroup}
**($R$-complete group)**
\linebreak
For $R$ a [[solid ring]], a [[group]] $G$ is called *$R$-complete* if it has a [[central series]]

$$
  G
  \,=\,
  G_0 
    \supset 
  G_1 
    \supset
  \cdots 
    \supset
  G_k
  \,=\,
  1
$$

(i.e. such that under [[commutator subgroups]] $[-,-]$ we have $[G, G_i] \subset G_{i+1}$)

such that each [[quotient group]] $G_j/G_{j+1}$ (which is an [[abelian group]] by the previous property) carries the [[mathematical structure|structure]] of an $R$-[[module]].
\end{definition}

\begin{proposition}\label{CompletionOfAGroup}
**(completion of a group)**
\linebreak
Given a [[solid ring]] $R$ and any group $G$, there is a [[universal construction]] of an $R$-complete group $G \xrightarrow{\;\;} G_{\widehat{R}}$ -- the *$R$-completion* of $G$ -- given by the [[limit]]

$$
  G_{\widehat{R}}
  \;\simeq\;
  \underset{
    \underset{
      { G \to C \in }
      \atop 
      { Grp^{G/}_{/R CompGrp} }
    }{\longleftarrow}
  }{\lim}
  \;C\;
$$

over the [[codomain]] [[functor]] from the [[comma category]] of $R$-complete groups under $G$.
\end{proposition}

More generally: 

\begin{definition}
**(fiberwise $R$-complete group)**
\linebreak
A [[short exact sequence]] of [[groups]]

\[
  \label{AShortExactSequenceOfGroups}
  1 
  \to
  N
  \longrightarrow
  \widehat{G}
  \longrightarrow
  G
  \to
  1
\]

is *fiberwise* or *relative* $R$-complete if $N$ is so (in the sense of Def. \ref{RCompleteGroup}).
\end{definition}

\begin{proposition}\label{FiberwiseCompletionOfAGroup}
**(fiberwise completion of a group)**
\linebreak
Given a [[solid ring]] $R$ and any [[short exact sequence]] of [[groups]] (eq:AShortExactSequenceOfGroups), there is a [[universal construction]] of a fiberwise $R$-complete exact sequence 
$$
 \array{
  1 
  &\to&
  N
  &\longrightarrow&
  \widehat{G}
  &\longrightarrow&
  G
  &\to&
  1
  \\
  &&
  \big\downarrow
  &&
  \big\downarrow
  &&
  \big\downarrow
  \mathrlap{{}^{=}}
  \\
  1
  &\to&
  N_{\widehat{R}}
  &\longrightarrow&
  \widehat{G}_{\widehat{R}_G}
  &\longrightarrow&
  G
  &\to&
  1
 }
$$
\end{proposition}


([Bousfield & Kan 1971, §2](#BousfieldKan71))


## Properties

### Special cases

\begin{example}\label{ExampleProfiniteCompletion}
**([[profinite completion]])**
\linebreak
For $R = \mathbb{Z}/p$ (a [[cyclic group]] of [[prime number|prime]] [[order of a group|order]]) and applied to [[finitely generated groups]], $R$-completion coincides with $p$-[[profinite completion of a group|profinite completion]].
\end{example}

\begin{example}\label{ExampleMalcevCompletion}
**([[Malcev completion]])**
\linebreak
For $R = \mathbb{Q}$ (the [[rational numbers]]) and applied to [[nilpotent groups]], $R$-completion coincides with [[Malcev completion]].
\end{example}

(e.g. [Bousfield & Kan 1972, p. 99](#BousfieldKan72))

## Related concepts

* [[completion of a ring]]

* [[completion of a space]]

  * [[p-completion]], [[p-adic homotopy theory]]
  
  * [[rationalization]], [[rational homotopy theory]]

* [[solid ring]]

## References

Original articles:

* {#BousfieldKan71} [[Aldridge Bousfield]], [[Daniel Kan]], §2 of: *Localization and completion in homotopy theory*, Bull. Amer. Math. Soc. **77** 6 (1971) 1006-1010 &lbrack;[doi:10.1090/S0002-9904-1971-12837-9](https://doi.org/10.1090/S0002-9904-1971-12837-9), [pdf](https://www.ams.org/journals/bull/1971-77-06/S0002-9904-1971-12837-9/S0002-9904-1971-12837-9.pdf)&rbrack;

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], Chapter IV of: _[[Homotopy limits, completions and localizations]]_, Lecture Notes in Mathematics, **304** Springer (1972) &lbrack;[doi:10.1007/978-3-540-38117-4](https://doi.org/10.1007/978-3-540-38117-4)&rbrack;

Further developments:

* [[Carles Casacuberta]], [[An Descheemaeker]], *Relative group completions*, Journal of Algebra, **285** 2 (2005) 451-469 &lbrack;[doi:10.1016/j.jalgebra.2004.10.023](https://doi.org/10.1016/j.jalgebra.2004.10.023)&rbrack;


[[!redirects completions of a group]]
[[!redirects completion of groups]]
[[!redirects completions of groups]]

[[!redirects R-completion of a group]]
[[!redirects R-completions of a group]]
[[!redirects R-completion of groups]]
[[!redirects R-completions of groups]]

[[!redirects complete group]]
[[!redirects complete groups]]

[[!redirects R-complete group]]
[[!redirects R-complete groups]]


