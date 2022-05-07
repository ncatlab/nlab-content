
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

The _codiscrete groupoid_ on a [[set]] is the [[groupoid]] whose [[objects]] are the elements of the [[set]] and which has a _unique [[morphism]]_ for every ordered pair of objects.

This is also called the **pair groupoid** of $X$ and sometimes also the __chaotic groupoid__ (this is explained [below](#Adjointness)), __indiscrete groupoid__, or __coarse groupoid__ on $X$, in older literature also [[Brandt groupoid]].


## Definition

\begin{definition}\label{CodiscreteGroupoid}
**(codiscrete groupoid)** \linebreak
For $X \in Set$, the **codiscrete groupoid** of $X$ is the [[groupoid]] 

$$
  Codisc(X)
  \;\coloneqq\;
  X \times X
    \underoverset
      {pr_2}
      {pr_1}
      {\rightrightarrows}
$$

whose object of objects is

* $Obj(X) = X$,

whose objects of morphisms is the [[Cartesian product]] of $X$ with itself

* $Mor(X) = X \times X$,

whose [[source]] and [[target]] morphism are the two canonical [[projections]] out of the product, and whose [[composition]] operation is the unique one compatible with this:

$$
  X \times X \times X
  \xrightarrow{\; (pr_1, pr_3) \; }
  X \times X
$$

\end{definition}

\begin{remark}
Def. \ref{CodiscreteGroupoid} manifestly makes sense in the generality of [[internal groupoids]] [[internalization|internal]] to any category with [[finite limits]] (in fact only [[finite products]] are involved in the definition of codiscrete groupoids).
\end{remark}



## Properties

### General

* Every codiscrete groupoid on an [[inhabited set]] is [[contractible space|contractible]]: [[equivalence of categories|equivalent]] to the [[terminal groupoid]] (the [[point]]). More generally, any codiscrete groupoid is equivalent to a [[truth value]].

* For $X$ a [[finite set]] of [[cardinality]] $n \gt 0$, the [[category algebra]] of $Codisc(X)$ is the algebra of $n\times n$ matrices. The contractibility of $Codisc(X)$ is reflected in the fact that this algebra is [[Morita equivalence|Morita equivalent]] to the [[ground ring]], which is the category algebra of the [[point]].

  This maybe serves to illustrate: even though codiscrete groupoids are pretty trivial, they are not too trivial to be entirely without interest. Often it is useful to have big puffed-up versions of the point available (see [[cofibrant resolution]]).

*  The [[underlying]] [[directed graph]] of a codiscrete groupoid is a [[complete graph]] (in that there is one *and only one* edge between any ordered pair of vertices).

### Adjointness
 {#Adjointness}

The [[1-category]] [[Grpd]] of [[groupoids]] is related to [[Set]] by an [[adjoint quadruple]] of [[functors]]

\begin{tikzcd}
  \mathrm{Grpd}
  \ar[
    rr,
    shift left=26pt,
    "{
      \pi_0
    }"{description}
  ]
  \ar[
    rr,
    "{
      (-)_0
    }"{description}
  ]
  &&
  \mathrm{Set}
  \ar[
    ll,
    shift right=13pt,
    "{
      \mathrm{Disc}
    }"{description}
  ]
  \ar[
    ll,
    shift left=13pt,
    "{
      \mathrm{Codisc}
    }"{description}
  ]
\end{tikzcd}

Here 

$$
  (-)_0
  \;\;
  \colon
  \;\;
  \big(  
    X_1 
    \rightrightarrows
    X_0 
  \big)
  \;\;\;
    \mapsto 
  \;\;\;
  X_0
$$

sends a groupoid to its set of [[objects]].

The [[right adjoint]] to this functor sends a set to its codiscrete groupoid according to Def. \ref{CodiscreteGroupoid}. To see this, observe the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) that reflects this adjunction:

For $\mathcal{X} = \big( \mathcal{X}_1 \rightrightarrows \mathcal{X}_0\big)\,\in\,$ [[Grpd]] and for $S \,\in\, $ [[Set]], a [[morphism]] of groupoids (i.e. a [[functor]]) of the form

$$
  \mathcal{X}
    \xrightarrow{\;\; F \;\;} 
  CoDisc(S) 
$$

is uniquely determined as soon as its component function 

$$
  \mathcal{X}_0 
    \xrightarrow{\;\; F_0 \;\;}
  CoDisc(S) = S
$$

is chose, because for every morphism $(x \xrightarrow{f} y) \,\in\,\mathcal{X}_1$  there is one and only one morphism $F_0(x) \to F_0(y)$ that it may be sent to, and making this unique choice for each $f$ does constitute a functor $F$ for every choice of $F_0$.

This association there gives a [[natural bijection]] of [[hom-sets]]

$$
  Grpd
  \big(
    \mathcal{X}
    ,\,
    CoDisc(S)
  \big)
  \;\;
  \simeq
  \;\;
  Set
  \big(
    \mathcal{X}_0
    ,\,
    S
  \big)
$$

and hence witnesses the claimed [[adjunction]]

$$
  CoDisc
    \;\; \dashv  \;\; 
  (-)_0 
  \,.
$$

It has been argued in [Lawvere 1984](chaos#Lawvere84) that such [[codiscrete object]]-constructions, [[right adjoint]] to [[forgetful functors]], deserve to be called "chaotic".

Correspondingly, [[nerves]] of codiscrete groupoids are precisely the [[codiscrete objects]] in [[sSet]], regarded as a [[cohesive topos]] over [[Set]].







## Examples
 {Example}

\begin{example}\label{UniversalGPrincipalBundle}
**(chaotic groupoids as models for [[universal principal bundles]])**
\linebreak
  For $G \in Grp(Set)$ a [[group]], the [[pair groupoid]] on $G$ is [[isomorphism|isomorphic]] 

$$
  \big(
    G \times G
    \underoverset
      {pr_2}
      {pr_1}
      {\rightrightarrows} G
  \big)
  \;\;
   \simeq
  \;\;
  \mathbf{E}G
$$

to the [[action groupoid]] of the right (say) [[group action]] of $G$ on itself by right group-multiplication:

$$
  \mathbf{E}G
  \;\coloneqq\;
  G \times G
  \underoverset
    {(-) \cdot (-)}
    {pr_1}
    {\rightrightarrows}
  G  
$$

The [[nerve]] of the latter is *equal* to the standard incarnation (since we chose right action) of the [[universal principal simplicial complex]] $W G \, \in \, sSet$:

$$
  N(\mathbf{E}G)
  \;\;
  =
  \;\;
  W G
  \,.
$$

The residual left multiplication action of $G$ on itself makes $\mathbf{E}G$ a $G$-[[action object]] [[internalization|internal to]] [[Grpd]]

$$
  \mathbf{E}G
  \;\;\;
  \in
  \;
  G Act(Grpd)
  \,.
$$

Since the nerve operation is a [[right adjoint]] ([this Prop.](nerve+and+realization#NerveAndRealizationAreAdjoint)) it [[preserved limit|preserves]] [[action objects]], and the result

$$
  W G
  \;=\;
  N(\mathbf{E}G)
  \;\;\;
  \in
  \;
  G Act(sSet)
$$

is the standard $G$-action on the [[universal principal simplicial complex]] of $G$.

The [[quotient]] of the group action on $\mathbf{E}G$ yields the [[delooping groupoid]] $\mathbf{B}G$ of $G$

\[
  \label{CoprojectionFromEGToBG}
  \mathbf{E}G
  \xrightarrow{\;\;}
  (\mathbf{E}G)/G
  \;=\;
  \mathbf{B}G
  \,.
\]

While the [[nerve]] operation does not in general preserve [[colimits]] ([this Exp.](nerve#NervesDoNotPreserveQuotientOfDeloopingByNormalSubgroup)) it does preserve (by [this Exp.](nerve#NerveDoesPreserveQuotientOfPairGroupoidOfGroupByGroupAction)) this particular colimit [[coprojection]] \eqref{CoprojectionFromEGToBG}. The resulting [[Kan fibration]]

$$
  N(\mathbf{E}G)
  \;=\;
  W G
  \xrightarrow{\;\;}
  (W G)/G
  \;=\;
  \overline{W}G
  \;=\;
  N(\mathbf{B}G)
  \;=\;
  N\big((\mathbf{E}G)/G\big)
$$

is the [[universal simplicial principal bundle]] with [[structure group]] $G \,\in\, Grp(Set) \xhookrightarrow{Disc} Grp(sSet)$ regarded as a [[simplicial group]].

Finally, the [[geometric realization]] of this into [[compactly generated topological spaces|compactly generated]] [[topological spaces]] is the standard model for the [[universal principal bundle]] of $G$:

$$
  E G 
    \;=\; 
  \big\vert 
    N(\mathbf{E}G)  
  \big\vert
    \xrightarrow{\;\;} 
  \big\vert 
    N(\mathbf{B}G)  
  \big\vert
    \;=\;
  B G
$$

over its [[classifying space]] $B G \simeq K(G,1)$ (which here is an [[Eilenberg-MacLane space]], since $G$ was assumed to be [[discrete group]] -- but this was just for simplicitiy of exposition, the analogous discussion applies to the chaotic [[topological groupoid]] of a [[topological group]] $G$).

\end{example}

## Related concepts

* [[delooping groupoid]]

* [[discrete groupoid]]

* [[indiscrete category]]

[[!redirects codiscrete groupoid]]
[[!redirects codiscrete groupoids]]

[[!redirects codiscrete category]]
[[!redirects codiscrete categories]]

[[!redirects pair groupoid]]
[[!redirects pair groupoids]]

[[!redirects chaotic groupoid]]
[[!redirects chaotic groupoids]]
