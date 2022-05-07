
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

The _codiscrete groupoid_ on a [[set]] is the [[groupoid]] whose [[object]]s are the elements of the [[set]] and which has a _unique [[morphism]]_ for every ordered pair of objects.

This is also called the **pair groupoid** of $X$ and sometimes also the __chaotic groupoid__ , __indiscrete groupoid__, or __coarse groupoid__ on $X$, in older literature also [[Brandt groupoid]].


## Definition

For $X$ set, the **codiscrete groupoid** of $X$ is the groupoid $Codisc(X)$ with

* $Obj(X) = X$;

* $Mor(X) = X \times X$.

This definition makes sense also [[internal category|internally]], for $X$ an object in any category with finite [[limit]]s. (In fact, this is one of those cases where the category can easily be defined with some limits lacking; we need only finite [[product]]s of $X$.)



**Remark** The codiscrete groupoid on $X$ is also sometimes called 
the _chaotic groupoid_ on $X$. The intuition is probably that "everything being connected with everything else sounds pretty chaotic", but one can argue that the term "chaotic groupoid" exactly misses the true intrinsic nature of codiscrete groupoids: since these are all just "puffed up versions of the point" they are "maximally homogenous" things. Which space would be less chaotic than the point?




## Properties

* Every codiscrete groupoid on an [[inhabited set]] is [[contractible space|contractible]]: [[equivalence of categories|equivalent]] to the [[point]]. More generally, any codiscrete groupoid is equivalent to a [[truth value]].

* For $X$ a [[finite set]] of cardinality $n \gt 0$, the [[category algebra]] of $Codisc(X)$ is the algebra of $n\times n$ matrices. The contractibility of $Codisc(X)$ is reflected in the fact that this algebra is [[Morita equivalence|Morita equivalent]] to the [[ground ring]], which is the category algebra of the [[point]].

  This maybe serves to illustrate: even though codiscrete groupoids are pretty trivial, they are not too trivial to be entirely without interest. Often it is useful to have big puffed-up versions of the point available.

*  The underlying [[quiver]] of a codiscrete groupoid is a [[complete graph]] (in that there is one *and only one* edge between any ordered pair of vertices).

* The [[nerves]] of codiscrete groupoids are precisely the [[codiscrete objects]] in [[sSet]], regarded as a [[cohesive topos]].

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
      {\rightrightarrows}
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
