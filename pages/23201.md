[[!redirects groupoid objects in an (infinity,1)-topos are effective]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[higher category theory|higher]] generalization ([[categorification]]) of how all [[equivalence relations]] in a [[Grothendieck topos]] have [[effective quotients]], so in an [[(infinity,1)-category of (infinity,1)-sheaves|$\infty$-sheaf]] [[(infinity,1)-topos|$\infty$-topos]] all "$\infty$-equivalence relations", constituted by [[groupoid object in an (infinity,1)-category|$\infty$-groupoid objects]] have [[effective epimorphism in an (infinity,1)-category|effective $\infty$-quotients]]. Where the former statement is one of the [[Giraud axioms]] that characterize [[sheaf toposes]], the latter is one of the [[Giraud-Rezk-Lurie axioms]] that characterize [[(infinity,1)-category of (infinity,1)-sheaves|$\infty$-sheaf]] [[(infinity,1)-topos|$\infty$-toposes]].

## Statement


In an [[(infinity,1)-topos|$\infty$-topos]] $\mathbf{H}$, let $X_\bullet \,\colon\, \Delta^{op} \xrightarrow{\phantom{---}} \mathbf{H}$ be a [[simplicial object]] and write

\[
  \label{InfinityQuotientCoprojection}
  X_0 
  \xrightarrow{\;\; q \;\;}
  \left\vert X_\bullet \right\vert
  \,\coloneqq\,
  \underset{\underset{[n] \in \Delta^{op}}{\longrightarrow}}{\lim} X_n
  \;\;\;
  \in
  \;
  \mathbf{H}
\]

for the *$\infty$-quotient coprojection*, i.e. induced universal morphism from $X_0$ to the [[(infinity,1)-colimit|$\infty$-colimit]]. Then:

\begin{proposition}
\label{GroupoidObjectsInAnInfinityToposAreEffective}
**(groupoid objects in an $\infty$-topos are effective)**
\linebreak
If $X_\bullet$ is a [[groupoid object in an (infinity,1)-category|groupoid object]] in that it satisfies the groupoidal [[Segal conditions]], then the $\infty$-quotient coprojection (eq:InfinityQuotientCoprojection) is an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] in that $X_\bullet$ [[equivalence in an (infinity,1)-category|equivalent]] to its [[Cech nerve]]:

$$
  \underset{[n] \in \Delta^{op}}{\prod}
  \Big(
    X_n
    \;\simeq\;
    \underset{n \; \text{factors}}
    {
      \underbrace{
        X_0 
          \underset{\left\vert X_\bullet\right\vert}{\times}
           \cdots
          \underset{\left\vert X_\bullet\right\vert}{\times}
        X_0 
      }
    }
  \Big)
$$
\end{proposition}
([Lurie 2009, Def. 6.1.2.14, Prop. 6.1.0.6 (3.iv)](#Lurie09))

Morever, this correspondence extends to morphisms:
\begin{proposition}
In any [[(infinity,1)-topos|$\infty$-topos]] $\mathbf{H}$ 
the correspondence of Prop. \ref{GroupoidObjectsInAnInfinityToposAreEffective}
extends to an  [[equivalence of (infinity,1)-categories|equivalence of $\infty$-categories]] 
\[
  \label{EquivalenceOfEffectiveEpimorphisms}
  Grpd(\mathbf{H})
  \underoverset
    { 
       \underset{
         (-)_0 
          \to 
         \underset{\longrightarrow}{\lim}(-)
       }
       {\longrightarrow} 
    }         
    { 
       \overset{ 
         (-)^{\times_\bullet} 
       }
       {\longleftarrow}
    }
    {\sim}
  \big(
    \mathbf{H}^{\Delta[1]}
  \big)_{eff}
\]
between 
the [[groupoid objects in an (infinity,1)-category|groupoid objects in $\mathbf{H}$]]
and
the [[full sub-(infinity,1)-category|full sub-$\infty$-category]] of the [[arrow category]] on the [[effective epimorphism in an (infinity,1)-category|effective epimorphisms]].
\end{proposition}
([Lurie 2009, below Cor. 6.2.3.5](#Lurie09))

Here the [[(infinity,1)-functors|$\infty$-functors]] are the [[restriction]] of  $L \colon Func(\Delta^{op}, \mathbf{H}) \to \Func([1], \mathbf{H})$ which sends a [[simplicial object]] to the universal morphism from $X_0$ to its [[(infinity,1)-colimit|$\infty$-colimit]] and $R \colon \Func([1], \mathbf{H}) \to Func(\Delta^{op}, \mathbf{H})$ sends a morphism to its Cech nerve.

This follows since the correspondence in both directions is computed by taking a Kan extension to $Func(\Delta_+^{op}, \mathbf{H})$ followed by a restriction, and this identifies both sides with the same full subcategory of $Func(\Delta_+^{op}, \mathbf{H})$.


## Literature

* {#Lurie09} [[Jacob Lurie]], *[[Higher Topos Theory]]*, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))



[[!redirects groupoid objects in an infinity1-topos are effective]]

