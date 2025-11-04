

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

An *antilinear map* or *conjugate linear map* is much like a [[linear map]], but instead of commuting with "[[scalar]] [[multiplication]]" it "anti-commutes" with it, in that multiplication by a scalar $c$ is mapped to multiplication by the scalar's [[star-conjugation|conjugate]] $\overline{c}$.

In order to make sense of this notion, the [[ground ring]] of the [[modules]] (or [[ground field]] of the [[vector spaces]]) that serve as the map's [[source|domain]] and [[codomain]] must have the additional structure of an [[involution]], to serve as the [[star-conjugation|conjugation]] map $c \mapsto \overline{c}$.

An antilinear map has a central role in the concept of [[star-algebra]]. Conversely, an antilinear map can be seen as built on a star-algebra, in that the [[involution]] makes the [[ground ring]] into a [[star-algebra]] over itself.


## Definition

### General

Consider as [[ground ring]] a [[commutative ring]] (often a [[field]], or possibly just a [[rig]]) $K$, equipped with an [[involution]] $x \mapsto \overline{x}$, meaning an [[endomorphism]] with $\overline{\overline{x}} = x$ for all $x \in K$ (such as a [[star algebra]], such as the [[complex numbers]] or [[quaterionions]], with their [[complex conjugation]] [[involution]]).

Then:

\begin{definition}
\label{GeneralDefinition}
For $K$-[[modules]] (or $K$-[[linear spaces]]) $V, W$, a __$K$-antilinear map__ is a function $T \colon V \to W$ such that for all $x, y \in V$ and $r \in K$,

$$ 
  T(r \cdot x + y) 
  \;=\; 
  \overline{r} \cdot T(x) + T(y) 
  \,.
$$
\end{definition}

This differs from the definition of a [[linear map]] in the appearance of $\overline{(-)}$ on the right-hand side.


### On Hermitian/Hilbert spaces
 {#DefinitionOnHermitianSpaces}

\begin{definition}
\label{HermitianConjugate}
Given a [[complex numbers|complex]] antilinear operator $A$ (Def. \ref{GeneralDefinition}) on a [[complex numbers|complex]] [[Hermitian inner product|Hermitian]] [[inner product space]] (like a [[Hilbert space]]) $\mathscr{H}, \langle -,-\rangle$, its *[[adjoint operator]]* $A^\dagger$ is defined not by the same formula as for [[linear operators]] (which would not type-check) but by

\[
  \label{HermitianAdjoint}
  \underset{v,w \in \mathscr{H}}{\forall}
  \;\;\;\;
  \big\langle
    v , A w
  \big\rangle
  =
  \overline{
  \big\langle
    A^\dagger v , w
  \big\rangle
  }
  \equiv
  \big\langle
    w, A^\dagger v
  \big\rangle
  \,.
\]
\end{definition}
(cf. [Uhlmann 2016 Def. 3.1](#Uhlmann2016))

## Examples

### Simple general examples

Every $K$-linear map is also a $K$-antilinear map, for $K$ regarded as equipped with the [[identity function|identity]] [[involution]].

Any involution $\overline{(-)} \colon K \to K$ is itself an antilinear map.


### Complex vector spaces

A motivating class of examples is when $K = \mathbb{C}$ is the [[complex numbers]], and $\overline{(-)}$ is [[complex conjugation]].

In particular, the [[Hermitian adjoint]] is an antilinear map from a space of $\mathbb{C}$-linear operators to itself.


### Further examples

A [[star-algebra|$*$-algebra]] requires by definition its [[anti-involution]] to be antilinear.



## Related concepts

* [[real structure]]

* [[anti-dual linear space]]

* [[antiunitary operator]]

* [[star-algebra]]


## References

Review:

* {#Uhlmann2016} Armin Uhlmann: *Anti- (Conjugate) Linearity*, Sci. China Phys. Mech. Astron. **59** (2016) 630301  &lbrack;[arXiv:1507.06545](https://arxiv.org/abs/1507.06545), [doi:10.1007/s11433-015-5777-1](https://doi.org/10.1007/s11433-015-5777-1)&rbrack;


See also:

* Wikipedia, *[Antilinear map](https://en.wikipedia.org/wiki/Antilinear_map)*

* references at *[[Wigner's theorem]]*.

* Santtu Ruotsalainen: *On a Weyl-von Neumann -type Theorem for Antilinear Self-adjoint Operators* &lbrack;[arXiv:1203.4670](https://arxiv.org/abs/1203.4670)&rbrack;


[[!redirects antilinear maps]]

[[!redirects anti-linear map]]
[[!redirects anti-linear maps]]

[[!redirects anti-linear operator]]
[[!redirects anti-linear operators]]


[[!redirects antilinear function]]
[[!redirects antilinear functions]]

[[!redirects conjugate linear map]]
[[!redirects conjugate linear maps]]

[[!redirects conjugate linear function]]
[[!redirects conjugate linear function]]


