
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

\tableofcontents

## Definition

\begin{definition}
A **simplicial $\infty$-groupoid** or **simplicial [[anima]]** is an [[(∞,1)-functor]]

$$
  X \colon \Delta^{op} \to \infty\mathrm{Grpd}
$$

from the [[opposite category]] of the [[simplex category]] into the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoids]].
\end{definition}

## Examples

* A $(\infty,1)$-precategory $\mathcal{C}$ is a simplicial infinity-groupoid which satisfies the [[Segal conditions]];

* A $(\infty,1)$-category is a $(\infty,1)$-precategory which also satisfies the [[univalence axiom]];

* An $\infty$-groupoid or discrete $(\infty,1)$-category is a $(\infty,1)$-category all of whose [[morphisms]] are [[equivalences]] under composition.

## (∞,1)-category of simplicial ∞-groupoids

The $(\infty,1)$-category of simplicial $\infty$-groupoids and morphisms between them is the [[(∞,1)-category of (∞,1)-functors]]

$$
  \infty\mathrm{Grpd}^{\Delta^{op}}
  = 
  Func_\infty(\Delta^{op}, \infty\mathrm{Grpd})
  \,.
$$

$\infty\mathrm{Grpd}^{\Delta^{op}}$ is the [[classifying (infinity,1)-topos|classifying $(\infty,1)$-topos]] for [[linear intervals]]. 

There is an inclusion

$$
  \infty\mathrm{Grpd}
  \hookrightarrow
  (\infty,1)\mathrm{Cat}
  \hookrightarrow
  \infty\mathrm{Grpd}^{\Delta^{op}}
$$

of $\infty$-groupoids and of $(\infty,1)$-categories inside $\infty\mathrm{Grpd}^{\Delta^{op}}$. Furthermore, the [[Sierpinski (infinity,1)-topos|Sierpinski $(\infty,1)$-topos]] embeds into $\infty\mathrm{Grpd}^{\Delta^{op}}$

$$
  \infty\mathrm{Grpd}^{\Delta^1}
  \hookrightarrow 
  \infty\mathrm{Grpd}^{\Delta^{op}}
$$

There is also an [[automorphism|automorphic]] [[(infinity,1)-functor|$(\infty,1)$-functor]] 

$$
  (-)^\op : \infty\mathrm{Grpd}^{\Delta^\op} \to \infty\mathrm{Grpd}^{\Delta^\op}
$$

on $\infty\mathrm{Grpd}^{\Delta^{op}}$ which takes a simplicial $\infty$-groupoid to its [[opposite simplicial infinity-groupoid|opposite simplicial $\infty$-groupoid]]. When restricted to the $(\infty,1)$-subcategory $(\infty,1)\mathrm{Cat} \hookrightarrow \infty\mathrm{Grpd}^{\Delta^\op}$, the $(-)^\op$ $(\infty,1)$-functor takes [[(infinity,1)-category|$(\infty,1)$-categories]] to its [[opposite (infinity,1)-category|opposite $(\infty,1)$-category]]. 

The simplicial interval $\Delta^1 \in \infty\mathrm{Grpd}^{\Delta^{op}}$ (regarded under [[(∞,1)-Yoneda embedding]]) is a [[tiny object]]: there is an [[amazing right adjoint]]

$$
  (-)^{1/\Delta^1} : \infty\mathrm{Grpd}^{\Delta^\op} \to \infty\mathrm{Grpd}^{\Delta^\op}
$$

on $\infty\mathrm{Grpd}^{\Delta^{op}}$. 

### Cohesion

Since $\infty\mathrm{Grpd}$ is an [[(∞,1)-topos]], $\infty\mathrm{Grpd}^{\Delta^{op}}$ is a [[cohesive (∞,1)-topos]] over $\infty\mathrm{Grpd}$:

$$
  \infty\mathrm{Grpd}^{\Delta^{op}}
  \stackrel{\Pi_I}{\stackrel{\longrightarrow}{\stackrel{\overset{Disc_I}{\longleftarrow}}{\stackrel{\overset{\Gamma_I}{\longrightarrow}}{\underset{coDisc_I}{\longleftarrow}}}}}
  \infty\mathrm{Grpd}
  \,.
$$

Here

* $\Pi_I$ sends a simplicial $\infty$-groupoid to the [[homotopy colimit]] over its components, hence to its "[[geometric realization]]" as seen in $\infty\mathrm{Grpd}$.

* $\Gamma_I$ evaluates on the 0-simplex;

* $Disc_I$ sends a simplicial $\infty$-groupoid to the simplicial object which is simplicially constant on $A$.

Hence cohesion of $\infty\mathrm{Grpd}^{\Delta^{op}}$ relative to $\infty\mathrm{Grpd}$ expresses the existence of a discrete and directed notion of path. 

The simplicial interval $\Delta^1 \in \infty\mathrm{Grpd}^{\Delta^{op}}$ (regarded under [[(∞,1)-Yoneda embedding]]) _[[cohesive (infinity,1)-topos#A1ExhibitingCohesion|exhibits the cohesion]]_ of $\infty\mathrm{Grpd}^{\Delta^{op}}$ over $\infty\mathrm{Grpd}$, in that the relative [[shape modality]] $\Pi_I$ is equivalent to the [[localization]] at $\Delta^1$

$$
  \Pi_I \simeq L_{\Delta^1}
  \,.
$$

### Internal logic

The $(\infty,1)$-category of simplicial $\infty$-groupoids is the [[internal logic]] is given by [[simplicial type theory]], a [[cohesive type theory|cohesive]] [[modal type theory|modal]] [[homotopy type theory]] equipped with the axioms for a [[linear interval]] and an [[axiom of cohesion]] for the linear interval. 

## Models

Simplicial $\infty$-groupoids can be modeled by [[bisimplicial sets]]. 

## Related concepts

* [[infinity-groupoid]]

* [[cubical infinity-groupoid]]

* [[(infinity,1)-functor]]

* [[simplex category]]

* [[simplicial object in an (infinity,1)-category]]

* [[simplicial set]]

* [[simplicial object]]

* [[simplicial type theory]]

* [[bisimplicial set]]

* [[opposite simplicial infinity-groupoid]]

[[!redirects simplicial infinity-groupoid]]
[[!redirects simplicial infinity-groupoids]]

[[!redirects simplicial ∞-groupoid]]
[[!redirects simplicial ∞-groupoids]]

[[!redirects simplicial anima]]
[[!redirects simplicial animas]]

[[!redirects ∞GrpdΔop]]

[[!redirects AniΔop]]

[[!redirects (∞,1)-category of simplicial infinity-groupoids]]
[[!redirects (∞,1)-categories of simplicial infinity-groupoids]]

[[!redirects (∞,1)-category of simplicial ∞-groupoids]]
[[!redirects (∞,1)-categories of simplicial ∞-groupoids]]

[[!redirects (∞,1)-category of simplicial anima]]
[[!redirects (∞,1)-categories of simplicial anima]]

[[!redirects (∞,1)-category of simplicial animas]]
[[!redirects (∞,1)-categories of simplicial animas]]

[[!redirects (infinity,1)-category of simplicial infinity-groupoids]]
[[!redirects (infinity,1)-categories of simplicial infinity-groupoids]]

[[!redirects (infinity,1)-category of simplicial ∞-groupoids]]
[[!redirects (infinity,1)-categories of simplicial ∞-groupoids]]

[[!redirects (infinity,1)-category of simplicial anima]]
[[!redirects (infinity,1)-categories of simplicial anima]]

[[!redirects (infinity,1)-category of simplicial animas]]
[[!redirects (infinity,1)-categories of simplicial animas]]

[[!redirects (∞,1)-topos of simplicial infinity-groupoids]]
[[!redirects (∞,1)-toposes of simplicial infinity-groupoids]]
[[!redirects (∞,1)-topoi of simplicial infinity-groupoids]]

[[!redirects (∞,1)-topos of simplicial ∞-groupoids]]
[[!redirects (∞,1)-toposes of simplicial ∞-groupoids]]
[[!redirects (∞,1)-topoi of simplicial ∞-groupoids]]

[[!redirects (∞,1)-topos of simplicial anima]]
[[!redirects (∞,1)-toposes of simplicial anima]]
[[!redirects (∞,1)-topoi of simplicial anima]]

[[!redirects (∞,1)-topos of simplicial animas]]
[[!redirects (∞,1)-toposes of simplicial animas]]
[[!redirects (∞,1)-topoi of simplicial animas]]

[[!redirects (infinity,1)-topos of simplicial infinity-groupoids]]
[[!redirects (infinity,1)-toposes of simplicial infinity-groupoids]]
[[!redirects (infinity,1)-topoi of simplicial infinity-groupoids]]

[[!redirects (infinity,1)-topos of simplicial ∞-groupoids]]
[[!redirects (infinity,1)-toposes of simplicial ∞-groupoids]]
[[!redirects (infinity,1)-topoi of simplicial ∞-groupoids]]

[[!redirects (infinity,1)-topos of simplicial anima]]
[[!redirects (infinity,1)-toposes of simplicial anima]]
[[!redirects (infinity,1)-topoi of simplicial anima]]

[[!redirects (infinity,1)-topos of simplicial animas]]
[[!redirects (infinity,1)-toposes of simplicial animas]]
[[!redirects (infinity,1)-topoi of simplicial animas]]