
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

\tableofcontents

## Idea

In a [[local topos]] there is a notion of _[[concrete objects]]_. These form a [[reflective subcategory]]. The corresponding reflector is the _concretification map_ which universally approximates any object by a concrete object.

## Definition


A [[local topos]] is a [[topos]] equipped with a [[sharp modality]] $\sharp$. 

\begin{definition}
\label{Concretification}

For $X$ any object of the topos, the [[image]] projection of the [[unit of a monad|unit]] $\eta^{\sharp}_X \colon X \to \sharp X$ is the _concretification_ of $X$

\[
  \label{ConcretificationAsSharpUnitImage}
  (X \to \sharp_1 X) 
  \coloneqq
  \big(
    X \twoheadrightarrow im(\eta^\sharp_X) 
  \big)
  \,.
\]

\end{definition}

## Properties
 {#Properties}

\begin{lemma}  
Given a [[morphism]] $f \colon X \longrightarrow Y$ into a [[concrete object]] $Y$, in that $Y \overset{\sim}{\twoheadrightarrow} \sharp_1 Y $, it factors uniquely through the concretification unit $\eta^\sharp_X$, so that we have a [[natural bijection]] of [[hom-sets]]
$$
  Y\;\text{concrete}
  \;\;\;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;\;\;
  Hom\big(
    \sharp_1 X
    ,\, 
    Y
  \big)
  \xrightarrow[\sim]{\phantom{--}
    \big(
      X \twoheadrightarrow \sharp_1 X
    \big)^\ast 
  \phantom{--}}
  Hom\big(
    X
    ,\, 
    Y
  \big)
  \mathrlap{\,.}
$$

\end{lemma}
\begin{proof}
This is a special case of the [[functor|functoriality]] of [[image factorization]]:

Consider the following [[diagram]] of given solid arrows, which [[commuting diagram|commutes]] by [[natural transformation|naturality]] of the [[unit of a monad|$\sharp$-unit]] and where we show the [[(epi,mono)-factorization]] of the vertical maps through their [[images]], hence through the concretifications (eq:ConcretificationAsSharpUnitImage):

\begin{tikzcd}
  X 
  \ar[
    d,
    ->>
  ]
  \ar[
    dd,
    bend right=30,
    "{ \eta^\sharp_X }"{swap}
  ]
  \ar[
    rr,
    "{ f }"
  ]
  &&
  Y
  \ar[
    d,
    equals
  ]
  \ar[
    dd,
    bend left=30,
    "{ \eta^\sharp_Y }"
  ]
  \\
  \sharp_1 X
  \ar[
    rr,
    dashed,
    "{ \sharp_1 f }"
  ]
  \ar[
    d,
    hook,
  ]
  &&
  \sharp_1 Y
  \ar[
    d,
    hook
  ]
  \\
  \sharp X
  \ar[
    rr,
    "{ \sharp f }"
  ]
  &&
  \sharp Y
\end{tikzcd}

By construction, the top left morphism is thus an [[epimorphism]] and the bottom right is a [[morphism]], as shown. Therefore the [[orthogonal factorization system|orthogonality]] of the [[(epi,mono) factorization system]] implies that there exists a unique dashed [[lift]] as shown
\end{proof}



## References

### General

(...)

### Of smooth sets

On concretification in the [[cohesive topos]] of [[smooth sets]], taking values in [[diffeological spaces]]:

* [[Urs Schreiber]], Def. 1.2.60 in: *[[schreiber:differential cohomology in a cohesive topos|Differential cohomology in a cohesive $\infty$-topos]]* &lbrack;[arXiv:1310.7930](https://arxiv.org/abs/1310.7930)&rbrack;


[[!redirects concretifications]]
[[!redirects differential concretification]]
[[!redirects differential concretifications]]