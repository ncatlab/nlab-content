
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A __$*$-algebra__ is an [[algebra]] $A$ ([[associative algebra|associative]] or [[nonassociative algebra|non-associative]])  equipped with an [[anti-involution]]:

$$
  (-)^\ast \;\colon\; A \longrightarrow A
  \;\;\;\;
  \text{s.t.}
  \;\;\;\;
  \underset{a,b \in A}{\forall} \; 
  (a b)^\ast \;=\; b^\ast a^\ast
  \,,
  \;\;\;\;\;\;
  \underset{a \in A}{\forall} \; \left((a)^\ast\right)^\ast \;=\; a
  \,.
$$


## Definition

In more detail, begin with a [[commutative ring]] (often a [[field]], or possibly just a [[rig]]) $K$ equipped with an [[involution]] (a [[homomorphism]] whose square is the [[identity morphism|identity]]), written $x \mapsto \bar{x}$.  (The usual example for $K$ is the field of [[complex numbers]] with involution given by [[complex conjugation]], but the concept of $*$-algebra makes sense in more general contexts.  Note that we can take *any* commutative ring $K$ and simply define $\bar{x} \coloneqq x$.)

a __$K$-$*$-algebra__ (a $*$-algebra over $K$) is a $K$-[[module]] $A$ equipped with a $K$-[[bilinear map]] $A\times A \to A$, written as multiplication (and often assumed to be [[associativity|associative]]) and a $K$-antilinear map $A \to A$, written as $x \mapsto x^*$, such that

* $x^{**} = x$ for all $x$ in $A$ (so we have an [[involution]] on the underlying $K$-module), and
* $(x y)^* = y^* x^*$ for all $x,y$ in $A$ (so it is an [[anti-involution]] on $A$ itself).

The claim that the anti-involution is $K$-antilinear means that $(r x)^* = \overline{r} x^*$ for all $r$ in $K$ and all $x$ in $A$ (as well as $(x + y)^* = x^* + y^*$).

If a $K$-$*$-algebra $A$ is itself commutative, then it is in particular a commutative ring with involution, and one can consider $A$-$*$-algebras as well.  On the other hand, a commutative ring with involution is simply a commutative $*$-algebra over the ring of [[integers]] (with trivial involution), and similarly for rigs and [[natural numbers]].


### $*$-Rings

A __$*$-ring__ is simply a $*$-algebra over the ring of [[integers]] (with trivial involution).  Similarly, a __$*$-rig__ is a $*$-algebra over the rig of [[natural numbers]].

Arguably, when we began this article with a commutative ring $K$ equipped with involution, we should have begun it with a ring with *anti*-involution instead.  However, since the ring (or rig) is commutative, there is no difference.


### Banach $*$-algebras

When $K$ is the field $\mathbb{C}$ of [[complex numbers]] (or the field $\mathbb{R}$ of [[real numbers]], with trivial involution), we can additionally ask that the $*$-algebra be a [[Banach algebra]]; then it is a __Banach $*$-algebra__.  Special cases of this are 

* $C^*$-[[C-star-algebra|algebras]] (aka $B^*$-algebras)

* and [[von Neumann algebras]] (aka $W^*$-algebras)

Arguably, one should require that the map $*$ be an [[isometry]] (which follows already if it is required to be [[short map|short]]); some authors require this and some don\'t.  However, this is automatic in the case of $C^*$-algebras (and hence also von Neumann algebras).


## Examples

### General
 {#General}

\begin{example}\label{TrivialStarStructure}
**(trivial star-structure)**\linebreak
Any plain [[algebra]] becomes a star-algebra by equipping it with the [[identity morphism|identity]] anti-involution.
\end{example}

\begin{example}\label{ComplexConjugation}
**([[complex conjugation]])**\linebreak
  The [[complex numbers]] -- regarded as an [[associative algebra]] over the [[real numbers]] -- form a star-algebra with anti-involution (which here  is an involution, since the product is [[commutative algebra|commutative]]) given by [[complex conjugation]].
\end{example}

\begin{example}
**([[Cayley-Dickson construction]])**
The [[Cayley-Dickson construction]] takes any star-algebra over the [[real numbers]] to a new star algebra.

Applied to the [[real numbers]] trivially regarded as a star-algebra (via Example \ref{TrivialStarStructure}), this yields, successively, the star-algebras of

* [[real numbers]] (Example \ref{TrivialStarStructure})

* [[complex numbers]] (Example \ref{ComplexConjugation})

* [[quaternions]]

* [[octonions]] 

(which are the four [[real normed division algebras]]) and then further the

* [[sedenions]]

* ...

In each case the star-operation may be thought of as [[complex conjugation]], given by changing the sign of the [[imaginary part]] and keeping the [[real part]] intact.

\end{example}

\begin{example}
**([[C-star algebras]])**
A _[[C-star algebra]]_ is a star-algebra where the anti-involution is compatible with the [[norm]] of the underlying [[Banach algebra]].
\end{example}


### Involutive Hopf algebras
 {#InvolutiveHopfAlgebras}

\begin{example}\label{InvolutiveHopfAlgebrasAreStarAlgebras}
**([[involutive Hopf algebras]] are [[star-algebras]])** \linebreak
  Any [[involutive Hopf algebra]] is a star-algebra, with star-involution given by the [[antipode]] (by [this Prop.](Hopf+algebra#AntipodeIsAnAntihomomorphism)).
\end{example}

\begin{example}
**(groupoid algebras are star-algebras)**
  A [[group algebra]] and, more generally, a [[groupoid convolution algebra]], is a star-algebra, with the star-[[involution]] given by pullback along the [[inverse|inversion]] operation of the groupoid.

Yet more generally, the [[category convolution algebra]] of a [[dagger-category]] is a $*$-algebra, with the involution being the pullback along the $\dagger$ operation.

All these are [[involutive Hopf algebras]] (since taking [[inverses]] and taking [[dagger-category|dagger-operations]] squares to the identity) and as such are special cases of Example \ref{InvolutiveHopfAlgebrasAreStarAlgebras}
\end{example}

\begin{example}\label{StarAlgebraOfHorizontalChordDiagrams}
**(star-algebra of [[horizontal chord diagrams]])** \linebreak
The algebra of [[horizontal chord diagrams]] is a star-algebra under reversal of orientation of strands (see [here](horizontal+chord+diagram#StarAlgebraStructure), [CSS 21, Prop. 2.9](#CSS21)).

Since [[horizontal chord diagrams are the homology of the loop space of configuration space]] and the [[homology of a loop space]] is an [[involutive Hopf algebra]], this is a special case of Example \ref{InvolutiveHopfAlgebrasAreStarAlgebras}.
\end{example}




## Related concepts

* [[real part]], [[imaginary part]]

* [[state on a star-algebra]]

* [[star-representation]]

[[!include states and observables -- content]]


## References

See also:

* Wikipedia, _[star-algebra](https://en.wikipedia.org/wiki/*-algebra)_

Discussion for [[group algebras]]:

* Antonio Giambruno, Cesar Polcino Milies and Sudarshan K. Sehgal, *Star-group identities on units of group algebras: The non-torsion case*, Forum Mathematicum Volume 30 Issue 1 ([doi:10.1515/forum-2016-0266](https://doi.org/10.1515/forum-2016-0266))


Discussion of the Example \ref{StarAlgebraOfHorizontalChordDiagrams} of [[horizontal chord diagrams]]:

* {#CSS21} [[David Corfield]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Fundamental weight systems are quantum states]]* ([arXiv:2105.02871](https://arxiv.org/abs/2105.02871))


[[!redirects star-algebra]]
[[!redirects star-algebras]]
[[!redirects star algebra]]
[[!redirects star algebras]]
[[!redirects *-algebra]]
[[!redirects *-algebras]]
[[!redirects * algebra]]
[[!redirects * algebras]]

[[!redirects star-ring]]
[[!redirects star-rings]]
[[!redirects star ring]]
[[!redirects star rings]]
[[!redirects *-ring]]
[[!redirects *-rings]]
[[!redirects * ring]]
[[!redirects * rings]]

[[!redirects star-rig]]
[[!redirects star-rigs]]
[[!redirects star rig]]
[[!redirects star rigs]]
[[!redirects *-rig]]
[[!redirects *-rigs]]
[[!redirects * rig]]
[[!redirects * rigs]]

[[!redirects Banach star-algebra]]
[[!redirects Banach star-algebras]]
[[!redirects Banach star algebra]]
[[!redirects Banach star algebras]]
[[!redirects Banach *-algebra]]
[[!redirects Banach *-algebras]]
[[!redirects Banach * algebra]]
[[!redirects Banach * algebras]]
