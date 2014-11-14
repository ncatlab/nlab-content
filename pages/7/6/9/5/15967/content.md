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
  M_n^{\leq 1}
  := \{(a_{ij})\in M_n,\;\max_{i,j}|a_{ij}|\leq 1\}
$$
in the (non-strict analytic) [[affine space]] $M_n=\mathbb{A}^{n^2}$ of [[matrices]],
and define the $n$-dimensional global unitary group to be given by
the subspace of $M_n^{\leq 1}\times_R M_n^{\leq 1}$ defined by
$$
  U(n)
  \coloneqq 
  \{(A,B)\in M_n^{\leq 1}\times_R M_n^{\leq 1},\;A B = B A = I\}
  \,.
$$
The dagger algebra of functions on $U(n)$ is defined by
$$A_{U(n)}:=R\{(a_{ij}),(b_{ij})\}^\dagger/(A B = B A = I).$$

Over $(\mathbb{Z},|\cdot|_0)$, the scheme (i.e., strict analytic space over a trivially normed ring) $U(n)$  is isomorphic to $GL_{n,\mathbb{Z}}$, but over $(\mathbb{Z},|\cdot|_\infty)$, the group $U(n)$ is closer to what people usually denote $\GL_n(\mathbb{F}_{\{\pm 1\}})$, where $\mathbb{F}_{\{\pm 1\}}$ denotes the [[field with one element]] in Durov's sense. Over $\mathbb{C}$, the group $U(n)$ contains the classical unitary group $U(n)(\C)$, since one has, for every complex matrix $A=(a_{ij})$, a natural inequality
$$\|A\|_{max}:=\max(|a_{ij}|)\leq \|A\|_2,$$
where $\|A\|_2$ is the operator norm for the hermitian norm on $\mathbb{C}^n$.
It is also clearly compact (contained in a product of polydiscs) and contained in the non-strict analytic group $\GL_{n}(\mathbb{C})$. Since $U(n)(\mathbb{C})$ is a maximal compact subgroup, we have that $U(n)$ is indeed the complex unitary group over $\mathbb{C}$.

###  Arithmetic principal unitary bundles

The good properties of the global analytic unitary group **may** imply that there is a natural bijection
$$
\pi_0(BU(n)(\mathbb{Z},|\cdot|_\infty))\cong
K\backslash \GL_n(\mathbb{A})/\GL_n(\mathbb{Q}),$$
where $K$ is the maximal compact subgroup $O(n,\mathbb{R})\times \GL_n(\hat{\mathbb{Z}})$ of $\GL_n(\mathbb{A})$.
It is thus quite a tempting idea to try to formulate the arithmetic [[Langlands program]] in geometric terms (similar to the ones used in the [[geometric Langlands correspondence]] over a function field) using the classifying stack $BU(n)$ of principal $U(n)$-bundles on strict global analytic spaces. 

## Reference

* [[Frédéric Paugam]] _Overconvergent global analytic geometry_ ([arXiv:1410.7971](http://arxiv.org/abs/1410.7971))


