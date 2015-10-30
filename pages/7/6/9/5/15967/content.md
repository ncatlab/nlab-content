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

Overconvergent [[global analytic geometry]] is a setting for global analytic geometry that allows the definition of strict and non-strict analytic spaces over an arbitrary [[Banach rings]], [[ind-object|ind-]]Banach ring, or more [[ind-object|ind-]][[pseudo-Banach ring]]. It also gives a notion of [[analytic motivic homotopy theory]] and [[derived global analytic geometry]].

## Basic ideas
 {#BasicIdeas}

The basic building blocks for overconvergent global analytic geometry over a given [[Banach ring]] $(R,{\vert\cdot\vert})$ are given by [[polydiscs]] of [[radius]] $1$ (in the strict situation) or arbitrary real radius (in the non-strict situation), and more generally, by strict (or non-strict) rational domains in them. This gives two categories $RatAlg_R^s$ and $RatAlg_R$ of rational domain algebras that actually form [pre-geometries](geometry+%28for+structured+%28infinity%2C1%29-toposes%29#Pregeometry) in the sense of Lurie.

One then defines analytic (resp. derived analytic) algebras as functors (resp. homotopical functors) of functions on the categories of rational domain algebras. The various types of finitely presented analytic algebras define various types of [[geometry (for structured (infinity,1)-toposes)|geometries]] in Lurie's sense. One may then define analytic (resp. derived analytic) stacks as functors (resp. homotopical functors) of points on analytic (resp. derived analytic) algebras.

This gives in particular four categories $An_R^\dagger$, $An_R^{\dagger,s}$, $DAn_R^\dagger$ and $DAn_R^{\dagger,s}$ of strict and non-strict overconvergent derived and non-derived analytic spaces.

## Examples

### Projective line
 {#ProjectiveLine}

One may define the strict [[projective line]] $\mathbb{P}^1_R$ over $R$ by pasting the overconvergent unit disc $D^1=\mathbb{M}(R\{T\}^\dagger)$ with itself along its boundary $U(1)=\mathbb{M}(R\{T,S\}^\dagger/(ST-1))$ by the map $T\mapsto 1/T$. This gives a strict analytic space over $R$. This strict construction of the projective line is particularly interesting when the base Banach ring is the ring $\mathbb{Z}$ of [[integers]] equipped with its usual [[archimedean absolute value]]. This strict structure is intuitively very close to what people call an archimedean compactification, e.g., in [[Arakelov geometry]].

### Unitary group
 {#UnitaryGroup}

One may try to use a similar construction to define higher dimensional global analogs of [[unitary groups]]: one may simply start from the strict [[polydisc]]

$$
  M_n^{\leq 1}
  := \{(a_{ij})\in M_n,\;\max_{i,j}|a_{ij}|\leq 1\}
$$
in the (non-strict analytic) [[affine space]] $M_n=\mathbb{A}^{n^2}$ of [[matrices]].
Since matrix multiplication on $M_n$ does not restrict to a morphism
$$M_n^{\leq 1}\times_R M_n^{\leq 1}\to M_n^{\leq 1},$$
this matrix polydisc is not a monoid. This implies that the naive definition of a global analytic version of $U(n)$, given by
$$
U(n)
\coloneqq
\{(A,B)\in M_n^{\leq 1},\;A B = B A = I\},
$$
only gives a strict analytic space that is not equipped with an analytic group structure
(except if one works in a non-archimedean setting).

One may however associate to $M_n^{\leq 1}$ a [[simplicial object|simplicial]] [[analytic space]] (a kind of [[nerve]]) given by forcing the multiplication to be defined:
$$
BM_n^{\leq 1}_{[k]}\coloneqq
\{(A_i)\in (M_n^{\leq 1})^{k},\;
\prod_{j\in [s]} A_j\in (M_n^{\leq 1})^{s}\;\forall f:[s]\hookrightarrow [k]\}.
$$
One may then define the $n$-dimensional global unitary [[infinity-groupoid]] $BU(n)$ to be given by the analytic sub-groupoid of $B\GL_n$ defined by
$$
  BU(n)
  \coloneqq 
  B\GL_n\cap BM_n^{\leq 1}
  \,.
$$

Remark now that $BM_n^{\leq 1}$ is a strict simplicial analytic space, because it is a subspace of the strict simplicial space $[k]\mapsto (M_n^{\leq 1})^k$ defined
by strict inequalities. One may also see $BU(n)$ as a closed strict simplicial analytic
subspace of $BM_n^{\leq 1}\times BM_n^{\leq 1}$ of pairs $(A,B)$ such that
$AB=BA=I$.

We may now look at what we get over various standard Banach rings:

* Over $(\mathbb{Z},|\cdot|_0)$, the scheme (i.e., strict analytic space over a trivially normed ring) $U(n)$  is isomorphic to $GL_{n,\mathbb{Z}}$.

* Over $(\mathbb{Q}_p,|\cdot|_p)$, the rigid analytic space $U(n)$ is such that
$U(n)(\mathbb{Q}_p)=\GL_n(\mathbb{Z}_p)$.

* Over $(\mathbb{Z},|\cdot|_\infty)$, the space $U(n)$ is not an analytic group, and $U(n)(\mathbb{Z},|\cdot|_\infty)$ is closer to what people usually denote $\GL_n(\mathbb{F}_{\{\pm 1\}})$, where $\mathbb{F}_{\{\pm 1\}}$ denotes the [[field with one element]] in Durov's sense.

* Over $\mathbb{C}$, the space $U(n)$ contains the classical unitary group $U(n)(\mathbb{C})$, since one has, for every complex matrix $A=(a_{ij})$, a natural inequality
$$\|A\|_{max}:=\max(|a_{ij}|)\leq \|A\|_2,$$
where $\|A\|_2$ is the operator norm for the hermitian norm on $\mathbb{C}^n$.
This thus gives a natural morphism
$$BU_{n}(\mathbb{C})\to BU(n)(\mathbb{C})$$
from the simplicial classifying space of the classical unitary group $U_{n}(\C)$ to the complex points of the simplicial "classifying space" $BU(n)$.

It is also clearly compact (contained in a product of polydiscs) and contained in the non-strict analytic group $\GL_{n}(\mathbb{C})$. Since $U(n)(\mathbb{C})$ is a maximal compact subgroup, we have that $U(n)$ is indeed the complex unitary group over $\mathbb{C}$.

###  Arithmetic principal unitary bundles

The good properties of the global analytic unitary group **may** imply that there is a natural bijection
$$
\pi_0(BU(n)(\mathbb{Z},|\cdot|_\infty))\cong
K\backslash \GL_n(\mathbb{A})/\GL_n(\mathbb{Q}),$$
where $K$ is the maximal compact subgroup $O(n,\mathbb{R})\times \GL_n(\hat{\mathbb{Z}})$ of $\GL_n(\mathbb{A})$.
It is thus quite a tempting idea to try to formulate the arithmetic [[Langlands program]] in geometric terms (similar to the ones used in the [[geometric Langlands correspondence]] over a function field) using the classifying stack $BU(n)$ of principal $U(n)$-bundles on strict global analytic spaces. 

## Related entries

[[derived analytic geometry]]

[[global Hodge theory]]

[[global analytic index theory]]

[[generalized global analytic geometry]]


## Reference

* [[Frédéric Paugam]] _Overconvergent global analytic geometry_ ([arXiv:1410.7971](http://arxiv.org/abs/1410.7971))

