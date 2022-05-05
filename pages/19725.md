

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[representation theory]], a _Schur_ index is a measure for how much an [[irreducible representation]] $V$ over some [[field]] $k$ becomes the [[direct sum]] of several irreducible representations as one passes from the [[ground field]] $k$ to some [[field extension]] $\widehat k$ of $k$.

There are two different-looking but equivalent perspectives on Schur indices, one via [[Galois theory]], the other via the [[lambda-ring]]-structure on [[representation rings]] $R_{\widehat k}(G)$. 


## Definition


Throughout, $G$ is a [[finite group]] with [[order of a group|order]] denoted ${\vert G\vert} \in \mathbb{N}$.

Given a [[field]] $k$, we write $R_K(G)$ for the [[representation ring]] of $G$ over $k$.

### Galois action and Adams operations

+-- {: .num_remark #RepresentationRingIsLambdaRing}
###### Remark
**([[representation ring]] is a [[lambda-ring]])**

Let $k$ be a [[field]] of [[characteristic zero]].

The [[representation ring]] $R_k(G)$ is canonically a [[lambda-ring]]. 

Hence, in particular, for each $n \in \mathbb{N}$, there exists the corresponding [[Adams operation]]

$$
  \psi^n 
    \;\colon\;
  R_k(G)
    \longrightarrow
  R_k(G)
  \,.
$$

Notice that for $k = \mathbb{C}$ the [[complex numbers]], the [[representation ring]] is identified with the $G$-[[equivariant K-theory]] of the point

$$
  R_{\mathbb{C}}(G)
  \;\simeq\;
  KU^0_G(\ast)
$$

and under this identification the [[Adams operations]] here are those familiar from K-theory.

=--

([tom Dieck 79, section 3.5](#tomDieck79))

+-- {: .num_prop #AdamsOperationActionOnCharacters}
###### Proposition
**([[Adams operation]]-[[action]] on [[characters]])** 

Let $k$ be a [[field]] of [[characteristic zero]]. 

Then the $n$th Adams operation on the [[representation ring]] (Remark \ref{RepresentationRingIsLambdaRing})

$$
  \psi^n 
    \;\colon\;
  R_k(G)
    \longrightarrow
  R_k(G)
  \,.
$$

has the following simple explicit description in terms of the [[characters]] $\chi_V$ of representations $V \in R_{k}(G)$:

$$
  \chi_{\psi^n V}
  =
  \chi_{V}\left( (-)^n \right)
$$

hence for all $g \in G$

$$
  \chi_{\psi^n(V)}(g)
  \;=\;
  \chi_V( g^n )
$$

=--

[tom Dieck 79, Prop. 3.5.1](#tomDieck79)

+-- {: .num_prop #AdamsOperationsRepresentGaloisAction}
###### Proposition
**([[Adams operations]] represent [[Galois group|Galois]] [[action]])**

Now let $\widehat k$ be a [[splitting field]] for $G$, for instance the [[complex numbers]] $\mathbb{C}$, but containing at least the [[cyclotomic field]] $\mathbb{Q}\left[ \exp(2 \pi i/e(G) \right]$, where $e(G) \in \mathbb{N}$ is the [[exponent of a group|exponent]] of $G$.

Then the [[action]] of the [[Adams operations]] (Remark \ref{RepresentationRingIsLambdaRing}) 

$$
  \psi^n 
    \;\colon\;
  R_{\widehat k}(G)
    \longrightarrow
  R_{\widehat k}(G)
  \,.
$$

for $n$ [[coprime integer|coprime]] to the [[order of a group|order]] of the group,

$$
  (n, {\vert G \vert}) = 1
  \,,
$$

equals the canonical [[action]] of the [[Galois group]] of $\mathbb{Q}\left[ e^{2 \pi i/e(G)} \right]$ over $\mathbb{Q}$ on $R_{\widehat k}(G)$ by [[field]] [[automorphisms]], which in turns is [[isomorphism|isomorphic]] to the [[multiplicative group of integers modulo n|multiplicative group of integers modulo e(G)]]:

$$
  Gal\left(
    \mathbb{Q}\left[ e^{2 \pi i/e(G)} \right] 
    \;:\;
    \mathbb{Q} 
  \right)
  \;\simeq\;
  \left( 
    \mathbb{Z}/{e(G)}
  \right)^{\times}
  \;\simeq\;
  \big\{
    \psi^{n} \;\vert\; (n,{\vert G\vert}) = 1
  \big\}
$$

One hence also says that $\psi^n V$ is a _Galois translate_ of $V$.

Moreover, if $V \in R_{\widehat k}(G)$ is an [[irreducible representation]], then also its Galois translate $\psi^n V$ is an irreducible representation, for $n$ coprime to ${\vert G \vert}$.

=--

([tom Dieck 79, Prop. 3.5.2](#tomDieck79))


### The Schur index

+-- {: .num_defn #GaloisGroupAveraging}
###### Definition
**([[Galois group|Galois]] [[group averaging]] on [[representations]])**

For $V \in R_{\widehat k}(G)$ an [[irreducible representation]], say that its _[[group averaging]]_ with respect to the [[Galois group]]/[[Adams operations]] from Prop. \ref{AdamsOperationsRepresentGaloisAction} is the smallest representation $V_{avg}$ containing $V$ as a [[subrepresentation]] such that 

$$
  \Psi^n\left(V_{avg}\right) - V_{avg}
  \;=\;
  0
  \;\;\;\;\;
  \in 
  R_{\widehat{k}}(G)
$$

for all $n$ [[coprime integer|coprime]] to ${\vert G\vert}$. (See also at _[[Adams conjecture]]_.)

By Prop. \ref{AdamsOperationsRepresentGaloisAction} this is equivalently the [[direct sum]]

$$
  V + \Psi^{n_1}\left(V\right) + \psi^{n_2}\left(V\right) + \cdots
$$

of $V$ with all of its _distinct_ Galois translates.

=--


+-- {: .num_prop #SchurIndexForComplexToRational}
###### Proposition
**(Schur index for complex-to-rational)**

Let $k = \mathbb{Q}$ be the [[rational numbers]] and let $\widehat k$ be the [[complex numbers]] or at least the [[cyclotomic field]] $\mathbb{Q}\left[e^{2 \pi i/e(G)}\right]$ for $e(G) \in \mathbb{Z}$ the [[exponent of a group|exponent]] of $G$. 

Then for 

$$
  V \in R_{\widehat k}(G)
$$ 

a $\widehat k$-linear [[representation]], its _Schur index_

$$
  s_V \in \mathbb{N}
$$ 

is the smallest [[natural number]] such that there exists a rational [[irreducible representation]] $W \in R_{\mathbb{Q}}(G)$ whose [[extension of scalars]] (e.g. [[complexification]]) is $s$ times the Galois group averaging $V_{avg}$ (Def. \ref{GaloisGroupAveraging}) of $V$:

$$
  W \otimes_{\mathbb{Q}} \mathbb{C}
  \;\simeq\;
  s_V \cdot V_{avg}
$$

Such irreducible $W$ exists uniquely. 

=--

(e.g. [tom Dieck 09, theorem 6.2.1](#tomDieck09))

+-- {: .num_remark #EquivariantJHomomorphism}
###### Remark
**([[equivariant J-homomorphism]]?)**

The uniqueness of the rational irrep $W$ in Prop. \ref{SchurIndexForComplexToRational} means that the Schur index construction there  provides a [[linear map]] (not necessarily a [[ring homomorphism]])

$$
  \array{
    R_{\widehat k}(G)
      \;
      &\overset{J_{\mathbb{Q}}}{\longrightarrow}&
      \;
    R_{\mathbb{Q}}(G) 
    \\
    V &\mapsto& s_V \cdot \big(V + \Psi^{n_1}(V) + \cdots \big)
  }
  \,.
$$

For some [[finite groups]] $G$ the [[permutation representation]]-assigning map 

$$
  A(G) \overset{\beta}{\longrightarrow} R_{\mathbb{Q}}(G)
$$ 

from the [[Burnside ring]] to the rational [[representation ring]] is [[surjective map|surjective]] ([this Prop.](permutation+representation#WhenAllVirtualLinearRepsAreVirtualPermutationReps)) and admits a canonical [[section]]; for $G = C_n$ a [[cyclic group]] it is actually an [[isomorphism]]. Hence in these cases we may regard the Schur index construction of Prop. \ref{SchurIndexForComplexToRational} as a [[linear map]] of the form

$$
  J 
    \;\colon\;
  R_{\mathbb{C}}(G)
    \longrightarrow
  A(G)
$$

hence going from the [[equivariant K-theory]] of the point to [[equivariant stable cohomotopy]] of the point

$$
  J 
    \;\colon\;
  KU^0_G(\ast)
    \longrightarrow
  \mathbb{S}_G^0(\ast)
  \,.
$$

> Question: 

> Is this the $G$-[[equivariant J-homomorphism]] over the point?

Notice that, by the construction in Prop. \ref{SchurIndexForComplexToRational} this map satisfies

$$
  J \big( \Psi^n(V) - V \big)  
  \;=\;
  0
$$

for all $n$ [[coprime integer|coprime]] to ${\vert G \vert}$.

> Question:

> Is this the $G$-[[equivariant Adams conjecture]]-statement over the point?

=--

## References

Lecture notes include

* {#tomDieck09} [[Tammo tom Dieck]], section 6.2 of _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

Textbook accounts include

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766, Springer 1979

* Bertram Huppert, chapter 38 of _Character theory of finite groups_, de Gruyter 1998