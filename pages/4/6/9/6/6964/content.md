
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Uniformly continuous maps
* table of contents
{: toc}

## Idea

Recall that a [[continuous map]] $f$ between [[spaces]] $X$ and $Y$ has the property that $f$ maps nearby points to nearby points, which may be formalised by first picking one point, then considering how nearby you want the points to be, then picking another point sufficiently nearby.

The concept of _uniformly continuous map_ $f$ is based on the same intuition but a different formalisation: first you pick how nearby you want the points to be, then you pick two points sufficiently nearby.  This results in a stronger criterion, definable in a less general context.

Traditionally this is formalized 

* for [[Archimedean fields]] (def. \ref{BetweenArchimedeanFields} below) 

* for [[metric spaces]] (def. \ref{BetweenMetricSpaces} below) 

but the definition makes sense more generally 

* for [[uniform spaces]] (def. \ref{BetweenUniformSpaces} below) 

and in fact 

* for [[quasi-uniform spaces]] (def. \ref{BetweenQuasiuniformSpaces} below).


## Definitions

+-- {: .num_defn #BetweenUniformSpaces}
###### Definition
**(uniform continuous map between [[uniform spaces]])


Let $X$ and $Y$ be [[uniform spaces]], each defined as a [[set]] equipped with a collection of [[entourages]].  A __uniformly continuous map__ from $X$ to $Y$ is a [[function]] between their [[underlying set]]s such that, given any [[entourage]] $E$ on $Y$, there is an entourage $D$ on $X$ such that $f(a)$ and $f(b)$ are $E$-close in $Y$ whenever $a$ and $b$ are $D$-close in $X$:
$$ \forall\, E\colon \mathcal{U}Y,\; \exists\, D\colon \mathcal{U}X,\; \forall\, a, b\colon X,\; a \approx_D b \;\Rightarrow\; f(a) \approx_E f(b) .$$

=--

A definition may also be given in terms of [[uniform covers]].  


+-- {: .num_remark}
###### Remark

The definition \ref{BetweenUniformSpaces} is exactly like the definition of _[[continuous map]]_ between uniform spaces, except for the order of the [[quantifiers]] $\exists\, D$ and $\forall\, a$.

=--

+-- {: .num_defn #BetweenQuasiuniformSpaces}
###### Definition
**(uniformly continuous map between [[quasiuniform spaces]])**


The definition \ref{BetweenUniformSpaces} in terms of [[entourages]] extends immediately to [[quasiuniform spaces]], in which case we may speak of __quasiuniformly continuous maps__ since some authors use 'uniformly continuous' for a map which is uniformly continuous between the spaces\' symmetrisations.  

=--

+-- {: .num_defn #AntiuniformlyContinuousMaps}
###### Definition
**(antiuniformly continuous map)**

An __antiuniformly continuous map__, is defined as a uniform map, but such that the order in which the points are compared is reversed:
$$ \forall\, E\colon \mathcal{U}Y,\; \exists\, D\colon \mathcal{U}X,\; \forall\, a, b\colon X,\; a \approx_D b \;\Rightarrow\; f(b) \approx_E f(a) .$$

=--

+-- {: .num_remark}
###### Remark

Between uniform spaces viewed as symmetric quasiuniformly continuous spaces, quasiuniformly continuous maps (def. \ref{BetweenQuasiuniformSpaces}), antiuniformly continuous maps (def. \ref{AntiuniformlyContinuousMaps}), and uniformly continuous maps (def. \ref{BetweenUniformSpaces}) are the same.

=--

In the particular case of [[metric spaces]], it is common to see this definition in elementary form:  


+-- {: .num_defn #BetweenMetricSpaces}
###### Definition
**(uniformly continuous map between [[metric spaces]])**

Given [[metric spaces]] $X$ and $Y$, a __uniformly continuous map__ from $X$ to $Y$ is a function between their underlying sets such that, given any [[positive number|positive]] [[real number]] $\epsilon$, there is a positive number $\delta$ such that the distance in $Y$ between $f(a)$ and $f(b)$ is less than $\epsilon$ whenever the distance in $X$ between $a$ and $b$ is less than $\delta$:
$$ \forall\, \epsilon \gt 0,\; \exists\, \delta \gt 0,\; \forall\, a, b\colon X,\; d_X(a, b) \lt \delta \;\Rightarrow\; d_Y(a, b) \lt \epsilon .$$
Again, this is exactly like the definition of [[continuous map]] between metric spaces, except for the order of the quantifiers $\exists\, \delta$ and $\forall\, a$.

=--

+-- {: .num_defn #BetweenArchimedeanFields}
###### Definition
**(uniformly continuous map between [[Archimedean fields]])**

Given [[Archimedean fields]] $X$ and $Y$, a __uniformly continuous map__ from $X$ to $Y$ is a function between their underlying sets such that, given any positive element $\epsilon \gt 0$, there is a positive element $\delta \gt 0$ such that the maximum of $f(a) - f(b)$ and $f(b) - f(a)$ is less than $\epsilon$ whenever the maximum of $a - b$ and $b - a$ is less than $\delta$:
$$ \forall\, \epsilon \gt 0,\; \exists\, \delta \gt 0,\; \forall\, a, b\colon X,\; \max(a - b, b - a) \lt \delta \;\Rightarrow\; \max(f(a) - f(b), f(b) - f(a)) \lt \epsilon .$$
Again, this is exactly like the definition of [[continuous map]] between Archimedean fields, except for the order of the quantifiers $\exists\, \delta$ and $\forall\, a$.

=--

+-- {: .num_defn }
###### Definition

A __uniform [[homeomorphism]]__ is a uniformly continuous [[bijection]] whose [[inverse]] is also uniformly continuous (which is *not* automatic).  Two (quasi)uniform spaces are __uniformly homeomorphic__ if there exists a uniform homeomorphism between them.  We may also speak of __antiuniform homeomorphisms__ between __antiuniformly homeomorphic__ quasiuniform spaces.

=--

## Properties

Every uniformly continuous map between uniform spaces is [[continuous map|continuous]] (between the underlying [[topological spaces]]) and in fact [[Cauchy map|Cauchy continuous]] (between the underlying [[Cauchy spaces]]).  Also, every uniformly continuous or antiuniformly continuous map between quasiuniform spaces is Cauchy continuous.  Conversely, every [[short map|short]] or even [[Lipschitz map|Lipschitz]] map between metric spaces (or Lipschitz [[manifolds]]) is uniformly continuous.

A [[composite]] of uniformly continuous maps is uniformly continuous, as is any [[identity function]] between (quasi)uniform spaces.  The composite of two antiuniformly continuous maps is uniformly continuous.  Thus uniform spaces are the [[objects]] of a [[category]] whose morphisms are the uniformly continuous maps as [[morphisms]], and quasiuniform spaces are the objects of two categories: one with uniformly continuous maps as morphisms and one with both uniformly continuous maps and antiuniformly continuous maps as morphisms (so that quasiuniform spaces are the objects of an $\mathcal{M}$-[[M-category|category]]).

## Examples

* [[continuous metric space valued function on compact metric space is uniformly continuous]]

## Related concepts

* [[uniform convergence]]

* [[uniform property]]

[[!redirects uniform continuity]]
[[!redirects uniformly continuous]]
[[!redirects uniformly continuous map]]
[[!redirects uniformly continuous maps]]
[[!redirects uniformly continuous function]]
[[!redirects uniformly continuous functions]]
[[!redirects uniform homeomorphism]]
[[!redirects uniform homeomorphisms]]
[[!redirects uniformly homeomorphic]]

[[!redirects quasiuniform continuity]]
[[!redirects quasi-uniform continuity]]
[[!redirects quasiuniformly continuous]]
[[!redirects quasiuni-formly continuous]]
[[!redirects quasiuniformly continuous map]]
[[!redirects quasi-uniformly continuous map]]
[[!redirects quasiuniformly continuous maps]]
[[!redirects quasi-uniformly continuous maps]]
[[!redirects quasiuniformly continuous function]]
[[!redirects quasi-uniformly continuous function]]
[[!redirects quasiuniformly continuous functions]]
[[!redirects quasi-uniformly continuous functions]]
[[!redirects quasiuniform homeomorphism]]
[[!redirects quasi-uniform homeomorphism]]
[[!redirects quasiuniform homeomorphisms]]
[[!redirects quasi-uniform homeomorphisms]]
[[!redirects quasiuniformly homeomorphic]]
[[!redirects quasi-uniformly homeomorphic]]

[[!redirects antiuniform continuity]]
[[!redirects anti-uniform continuity]]
[[!redirects antiuniformly continuous]]
[[!redirects anti-uniformly continuous]]
[[!redirects antiuniformly continuous map]]
[[!redirects anti-uniformly continuous map]]
[[!redirects antiuniformly continuous maps]]
[[!redirects anti-uniformly continuous maps]]
[[!redirects antiuniformly continuous function]]
[[!redirects anti-uniformly continuous function]]
[[!redirects antiuniformly continuous functions]]
[[!redirects anti-uniformly continuous functions]]
[[!redirects antiuniform homeomorphism]]
[[!redirects anti-uniform homeomorphism]]
[[!redirects antiuniform homeomorphisms]]
[[!redirects anti-uniform homeomorphisms]]
[[!redirects antiuniformly homeomorphic]]
[[!redirects anti-uniformly homeomorphic]]
