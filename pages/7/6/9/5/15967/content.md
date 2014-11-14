[[!redirects Overconvergent global analytic geometry]]
[[!redirects overconvergent global analytic geometry]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Overconvergent [[global analytic geometry]] is a setting for global analytic geometry that allows the definition of strict and non-strict analytic spaces over an arbitrary [[Banach rings]] or [[ind-object|ind-]]Banach ring. It also gives a notion of [[analytic motivic homotopy theory]] and [[derived global analytic geometry]].

## Basic ideas
 {#BasicIdeas}

The basic building blocks for overconvergent global analytic geometry over a given [[Banach ring]] $(R,{\vert\cdot\vert})$ are given by [[polydiscs]] of [[radius]] $1$ (in the strict situation) or arbitrary real radius (in the non-strict situation), and more generally, by strict (or non-strict) rational domains in them. This gives two categories $RatAlg_R^s$ and $RatAlg_R$ of rational domain algebras that actually form [pre-geometries](geometry+%28for+structured+%28infinity%2C1%29-toposes%29#Pregeometry) in the sense of Lurie.

One then defines analytic (resp. derived analytic) algebras as functors (resp. homotopical functors) of functions on the categories of rational domain algebras. The various types of finitely presented analytic algebras define various types of [[geometry (for structured (infinity,1)-toposes)|geometries]] in Lurie's sense. One may then define analytic (resp. derived analytic) stacks as functors (resp. homotopical functors) of functions on analytic (resp. derived analytic) algebras.

This gives in particular four categories $An_R^\dagger$, $An_R^{\dagger,s}$, $DAn_R^\dagger$ and $DAn_R^{\dagger,s}$ of strict and non-strict overconvergent derived and non-derived analytic spaces.

## Examples

### Projective line
 {#ProjectiveLine}

One may define the strict [[projective line]] $\mathbb{P}^1_R$ over $R$ by pasting the overconvergent unit disc $D^1=\mathbb{M}(R\{T\}^\dagger)$ with itself along its boundary $U(1)=\mathbb{M}(R\{T,S\}^\dagger/(ST-1))$ by the map $T\mapsto 1/T$. This gives a strict analytic space over $R$. This strict construction of the projective line is particularly interesting when the base Banach ring is the ring $\mathbb{Z}$ of [[integers]] equipped with its usual [[archimedean absolute value]]. This strict structure is intuitively very close to what people call an archimedean compactification, e.g., in [[Arakelov geometry]].

### Unitary group
 {#UnitaryGroup}

One may try a similar construction to define higher dimensional global [[unitary groups]]: one may simply start from the strict [[polydisc]]

$$
  D^1 M_n
  =
  \mathbb{M}(R\{(a_{ij})_{1\leq i,j\leq n}\}^\dagger)
  \,,
$$
in the (non-strict analytic) [[affine space]] $M_n=\mathbb{A}^{n^2}$ of [[matrices]],
and consider the rational domain $R_n\subset D^1 M_n$ defined by
$$R_n:=\{(a_{ij}),\;|na_{ij}|\leq 1\;\forall 1\leq i,j\leq n\}.$$


One then define the $n$-dimensional global unitary group to be given by

$$
  U(n)
  \coloneqq 
  \mathbb{M}(R\{((a_{ij}),(b_{ij})\}^\dagger/A B = B A = I)
  \,.
$$

Over $(\mathbb{Z},|\cdot|_0)$, we have $U(n)(\mathbb{Z})\cong GL_n(\mathbb{Z})$, but over $(\mathbb{Z},|\cdot|_\infty)$, the group $U(n)(\mathbb{Z})$ is closer to what people usually denote $\GL_n(\mathbb{F}_{\{\pm 1\}})$, where $\mathbb{F}_{\{\pm 1\}}$ denotes the [[field with one element]] in Durov's sense.

## Reference

* [[Frédéric Paugam]] _Overconvergent global analytic geometry_ ([arXiv:1410.7971](http://arxiv.org/abs/1410.7971))


