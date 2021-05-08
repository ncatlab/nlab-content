
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _differential equation_ is an [[equation]] involving [[terms]] that are [[derivatives]] (or [[differentials]]).  One sometimes distinguishes _partial_ differential equations (which involve [[partial derivatives]]) from _[[ordinary differential equation|ordinary]]_ differential equations (which don\'t).


## As sub-$\infty$-groupoids of tangent and jet bundle

Analogous to how ordinary equations determine and are determined by their spaces of solutions -- the corresponding [[scheme]]s -- accordingly differential equations $F(\partial^i x)$ on sections of a bundle $E \to X$ determine and are determined by their solution spaces, which are sub-[[D-scheme]]s of the [[jet bundle]] D-scheme:

$$
  \array{
    Solutions(F) &&\hookrightarrow&& Jet(E)
    \\
    & \searrow && \swarrow
    \\
    && \Im(X)
  }
$$

In fact there is an [[equivalence of categories]] between the [[Eilenberg-Moore category]] of the [[jet comonad]] over $X$ and the category of partial differential equations with variables in $X$ ([Marvan 86](#Marvan86)). 

At least in nice cases for differential equations on functions on $X$ this is equivalently modeled by sub-[[Lie algebroid]]s of [[tangent Lie algebroid]]s.

$$
  \array{
    Solutions(F) &&\hookrightarrow&& T X
  }
$$




see [[exterior differential system]] for details

## In terms of synthetic differential geometry
  {#InSynthDiff}

A perspective on differential equations from the [[nPOV]] of [[synthetic differential geometry]] is given in 

* [[William Lawvere]], _Toposes of laws of motion_ , transcript of a talk in Montreal, Sept. 1997 ([pdf](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf))

  (on the description of [[differential equation]]s in terms of synthetic differential geometry)

See also the appendix of

* _Outline of synthetic differential geometry_ , seminar notes (1998) ([pdf](http://www.acsu.buffalo.edu/~wlawvere/SDG_Outline.pdf))

### First order homogeneous ODEs as extension problems in a smooth topos

In a [[smooth topos]] with $X$ and $A$ any two objects and $D = \{x \in R | x^2 = 0\}$ the [[infinitesimally thickened point|abstract tangent vector]], a [[diagram]], of the form

$$
  \array{
    {*}&\to& D &\stackrel{v}{\to}& X
    \\
    &{}_{\mathllap{v(f)(x)}}\searrow& {}^{\mathllap{v(f)}}\downarrow & \swarrow_{\mathrlap{f}}
    \\
    && A
  }
$$

may be read as

* $f$ is a smooth function on $X$ with values in $A$;

* whose derivative along the [[tangent vector]] $v \in T_x X \subset T X = X^D$...

* ...is the tangent vector $v(f) \in T_{f(x)} A \subset T A = A^D$.

Accordingly, the diagram 

$$
  \array{
    D &\stackrel{v}{\to}& X
    \\
    {}_{\mathllap{\alpha}}\downarrow    
    \\
    A
  }
$$

may be read as encoding the differential equation $v(f)_x = \alpha$ (at one point) whose solutions $f \in A^X$ are the extensions that complete this diagram.

To get differential equations in the more common sense that they impose a condition on the derivative of $f$ at each single point of $X$ and varying smoothly with $X$, we think of  $f : X \to A$ in terms of the [[exponential object|exponential map]]

$$
  f^X : X^X \to A^X
$$

and consider

$$
  \array{
    &&{*}
    \\
    && \downarrow & \searrow^{\mathrlap{Id_X}}
    \\
    {*}&\to& D &\stackrel{v}{\to}& X^X
    \\
    &{}_{\mathllap{f}}\searrow&{}^{\mathllap{\alpha}}\downarrow & \swarrow_{\mathrlap{f^X}}
    \\
    &&A^X
  }
  \,.
$$

In this diagram now

* $v : D \to X^X$ is the [[adjunct]] of a [[vector field]] $X \to T X = X^D$ on $X$;

  (the commutativity of the top  right triangle ensures that indeed this $X \to T X$ is a [[section]] of the [[tangent bundle]] projection $T X \to X$);

* $\alpha : D \to A^X$ is the [[adjunct]] of a map $X \to T A = A^D$ that sends each point $x \in X$ to a tangent vector in $T_{f(x)} A$ 

  (enforced by the commutativity of the left bottom triangle)

* and the commutativity of the right lower triangle is the **differential equation**

  $$
    v(f) = \alpha
    \,.
  $$

## Examples

* [[heat equation]]

* [[wave equation]], [[Klein-Gordon equation]]

* [[Navier-Stokes equation]]

* [[Schrödinger equation]]

* [[Dirac equation]]

* ...

* [[Green hyperbolic partial differential equation]]


## Related concepts

* [[differentiation]], [[differential calculus]]

* [[diffiety]]

* [[ordinary differential equation]], [[partial differential equation]]

* [[linear differential equation]]

* [[integrable differential equation]],  [[formally integrable differential equation]]

* [[generalized solution of a PDE]]

* [[Green's function]]

* [[Sturm–Liouville theory]]

* [[initial value problem]]

* [[differential Galois theory]]

* [[D-module]], [[D-geometry]]

* [[homotopy analysis method]]

## References

### General

General accounts include

* [[Sergiu Klainerman]], _PDE as a unified subject_ 2000 ([pdf](http://www.math.princeton.edu/~seri/homepage/papers/telaviv.pdf))

* Boris Kruglikov, Valentin Lychagin, _Geometry of differential equations_, [pdf](http://www.math.uit.no/seminar/Preprints/07-01-BKVL.pdf)

* Arthemy Kiselev, _The twelve lectures in the (non)commutative geometry of differential equations_, preprint IHES M/12/13 [pdf](http://preprints.ihes.fr/2012/M/M-12-13.pdf)

* Yves Andre, _Solution algebras of differential equations and quasi-homogeneous varieties_, [arXiv:1107.1179](http://arxiv.org/abs/1107.1179)

* [[Mikhail Gromov]], _Partial differential relations_, Ergebnisse der Mathematik und ihrer Grenzgebiete (3) [Results in Mathematics and Related Areas (3)], 9. Springer-Verlag, Berlin, 1986. x+363 pp.

* [[Peter Olver]], _Applications of Lie groups to differential equations_, Springer; _Equivalence, invariants, and symmetry_, Cambridge Univ. Press 1995.

On the partial differential equations appearing in [[physics]]:

* [[Robert Geroch]], _Partial Differential Equations of Physics_, in: _[General Relativity: Proceedings](https://inspirehep.net/literature/328567)_ Edited by G.S. Hall and J.R. Pulham. Edinburgh, IOP Publishing, 1996. p. 19 ([arXiv:gr-qc/9602055](http://arxiv.org/abs/gr-qc/9602055))


### Via jet bundles and D-modules


Discussion of the spaces of solutions is in 

* Batu G&#252;neysu, [[Markus Pflaum]], _The profinite dimensional manifold structure of formal solution spaces of formally integrable PDE's_ ([arXiv:1308.1005](https://arxiv.org/abs/1308.1005))

Characterization of the category of partial differential equations as the [[Eilenberg-Moore category]] of [[coalgebras]] over the [[jet comonad]]:

* {#Marvan86} [[Michal Marvan]], _A note on the category of partial differential equations_, in _Differential geometry and its applications_, Proceedings of the Conference August 24-30, 1986, Brno ([[MarvanJetComonad.pdf:file]])

Discussion in [[differential cohesion]]:

* [[Igor Khavkine]], [[Urs Schreiber]], _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))

Discussion in differentially cohesive [[modal homotopy type theory|modal]] [[homotopy type theory]]:

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, 2017


In the language of [[D-modules]] and hence for the special case of _linear_ differential equations, this appears as prop. 3.4.1.1 in 

* {#GaitsgoryRozenblyum11} [[Dennis Gaitsgory]], [[Nick Rozenblyum]], _Crystals and D-modules_ ([arXiv:1111.2087](http://arxiv.org/abs/1111.2087))


### Other

A [[domain specific programming language]] for differential equations is presented in

* {#ALORW12} Martin S. Alnaes, Anders Logg, Kristian B. Oelgaard, Marie E. Rognes, Garth N. Wells, _Unified Form Language: A domain-specific language for weak formulations of partial differential equations_, [arXiv:1211.4047](http://arxiv.org/abs/1211.4047)

See also

* _[Dispersive Wiki](http://wiki.math.toronto.edu/DispersiveWiki/index.php/Main_Page)_


[[!redirects differential equation]]
[[!redirects differential equations]]

[[!redirects partial differential equation]]
[[!redirects partial differential equations]]
[[!redirects PDE]]
[[!redirects PDEs]]
[[!redirects PDE-s]]
[[!redirects PDE's]]
[[!redirects PDE\'s]]
[[!redirects PDE/'s]]
[[!redirects PDE's]]

[[!redirects PDE theory]]
