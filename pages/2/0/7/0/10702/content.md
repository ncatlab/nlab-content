
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[complex line bundle]] $L$ over a [[space]] $X$ its $k$th [[tensor product of vector bundles|tensor power]] $L^{\otimes k}$ is another line bundle for any $k \in \mathbb{N}$.  The line bundles define certain elements of [[complex topological K-theory]] group $K(X)$, and there is a unique operation $\psi^k \colon K(X) \to K(X)$, the _$k$th Adams operation_, such that:

* $\psi^k([L]) = [L^{\otimes k}]$ if $[L]$ is the K-theory class of any line bundle,

* $\psi^k \colon K(X) \to K(X)$ is a [[group homomorphism]], 

* $\psi^k$ is a [[natural transformation]]: any map $f: X \to Y$ induces a map $f^* : K(Y) \to K(X)$ on $K$-theory, and $\psi^k \circ f^* = f^* \circ \psi^k$.

More abstractly, Adams operations can be defined on any [[Lambda-ring]]. They are an example of [[power operations]].

## Definition
 {#Definition}

The Adams operations have an explicit definition in terms of the [[Lambda-ring]] structure on [[topological K-theory]], this we state as def. \ref{DefinitionInTermsOfLambdaRing} below. While explicit, this definition may look contrived on first sight. But it turns out that it satisfies a list of properties, of which two simple ones already uniquely characterize the Adams operations.  This is proposition \ref{TheBasicProperties} below.

+-- {: .num_prop #LambdaRingStructureOnKTheory}
###### Definition
**(Lambda-ring structure on topological K-theory)**

Let $X$ be a [[compact topological space]] and write $K(X)$ for its [[topological K-theory]] [[ring]]. For $E$ a [[vector bundle]] over $X$, write $[E] \in K(X)$ for its class in K-theory.  Given $E$, write

$$
  \lambda_t[E]
  \;\coloneqq\;
  \underoverset{k = 0}{\infty}{\sum}
  [\wedge^k_X E] t^k
  \;\;\in\;\;
  K(X)[ [t] ] 
$$

for the [[formal power series]] with [[coefficients]] in the ring $K(X)$ being the K-theory classes of the skew-symmetrized [[tensor product of vector bundles]] of $E$ with itself. 

Since the constant term of this power series is always the unit $[\wedge^0 E] = 1$, hence

$$
  \lambda_t[E] \in 1 + (t) \cdot K(X)[ [t] ]
$$

there exists a multiplicative inverse formal power series $\lambda_t[E]^{-1}$.

Then given the class of a [[virtual vector bundle]] $[E] - [F] \in K(X)$, define more generally

$$
  \lambda_t[[E- F]]
  \;\;\coloneqq\;\,
  \lambda_t[E] \cdot \lambda_t[F]^{-1}
  \;\;\in\;\;
  K(X)[ [t] ]
  \,.
$$


=--

+-- {: .num_prop #DefinitionInTermsOfLambdaRing}
###### Definition
**(explicit definition of Adams operation)**

For $E$ a [[vector bundle]] over some [[topological space]] $X$, write 

$$
  \psi^0(E) \coloneqq rank(E)
$$ 

for the [[bundle]] which over each [[connected component]] of $X$ is the [[trivial bundle|trivial]] vector bundle of the same [[rank of a vector bundle|rank]] as $E$ over that component.

Define a [[formal power series]] with [[coefficients]] in the K-theory ring $K(X)$ by

$$
  \begin{aligned}
    \psi_t(E)
    & \coloneqq
   \underoverset{\infty}{k = 0}{\sum}
   \psi^k(E) t^k
   \\
    & \coloneqq
    \psi^0(E)
      -
     t \frac{d}{d t} log \lambda_{-t}(E)
    \;\;\in\;\;
    K(X)[ [t] ]
  \end{aligned}
  \,,
$$

where $\lambda_t$ is the [[Lambda-ring]] operation from def. \ref{LambdaRingStructureOnKTheory}.

Here the [[derivative]] of the [[logarithm]] of formal power series stands for the usual expression in terms of the [[geometric series]]:


$$
  \begin{aligned}
    \frac{d}{d t} log \lambda_{-t}(E)
    & =
    \frac{1}{\lambda_{-t}(E)}
    \frac{d}{d t}
     \lambda_{-t}(E)
     \\
     & =
     \underoverset{\infty}{k = 0}{\sum}
     \left(
        1  - \lambda_{-t}(E)
     \right)^k
    \cdot
     \frac{d}{d t} \lambda_{-t}(E)
  \end{aligned} 
  \,.
$$

The **$k$th Adams operation** is the [[cohomology operation]] on [[topological K-theory]]


$$
  \psi^k \;\colon\; K(-) \longrightarrow K(-)
$$


which is the coefficient of $t^k$ in $\psi_t$.


=--


+-- {: .num_prop #TheBasicProperties}
###### Proposition
**(basic properties and characterization of Adams operations)**

The Adams operations

$$
  \psi^k \;\colon\; K(X) \longrightarrow K(X)
$$

have the following properties, for all elements $x,y \in K(X)$ and $k, l \in \mathbb{N}$ and $p \; \text{prime}$:

1. $\psi^k(x + y) = \psi^k(x) + \psi^k(y)$

   ($\psi^k$ is a [[natural transformation|natural]] [[abelian group]] [[homomorphism]])

1. $x \,\text{a line} \;\;\Rightarrow\;\; \psi^k(x) = x^k$

   (applied to a class $x \coloneqq [L]$ represented by a [[line bundle]] $L$, $\psi^k$ is the $k$th [[tensor power]])

1. $\psi^k(x \cdot y) = \psi^k(x) \cdot \psi^k(y)$

   ($\psi^k$ is in fact a [[natural transformation|natural]] [[ring]] [[homomorphism]])

1. $\psi^k(\psi^l(x)) = \psi^{k l}(x)$

1. $\psi^p(x) = x^p \, \text{mod}\, p$

1. if $x \in \tilde K(S^{2n})$ ([[reduced cohomology]]) then 

   $x \in \tilde K(S^{2n}) \hookrightarrow K(S^{2n}) \;\;\Rightarrow\;\;\psi^k(x) = k^n \cdot x$.

Moreover, the first two of these already uniquely characterize the Adams operations.

=--

e.g. [Wirthmuller 12, section 11](#Wirthmuller12)



## Properties

### Basic properties

+-- {: .num_prop #AdamsOperationOnComplexTopologicalKtheoryOfnSpheres} 
###### Proposition
**(Adams operations on [[complex topological K-theory]] of [[n-spheres]])**

For $n \in \mathbb{N}$, the [[Adams operations]] on the [[reduced K-theory]] of the [[n-sphere|2n-sphere]] are given by:

$$
  \array{
    \widetilde K
    \big( 
      S^{2n}
    \big)
    &
    \overset{ \;\;\; \psi^k\;\;\; }{\longrightarrow}
    &
    \widetilde K
    \big( 
      S^{2n}
    \big)
    \\
    V &\mapsto& k^n \cdot V
  }
$$

=--

(e.g. [Wirthmüller, Prop. on p. 45 (47 of 67)](#Wirthmuller12))


### Compatibility with complexification
 {#CompatibilityWithComplexification}

The Adams operations are compatible with the [[complexification]] map $(-) \otimes_{\mathbb{R}} \mathbb{C}$ from [[real vector bundles]] to [[complex vector bundles]], hence from [[KO-cohomology]] to [[KU-cohomology]], in that the following [[commutative diagram|diagram commutes]], for all $k$:

$$
  \array{
    KO(X) 
      &\overset{ \psi^k }{\longrightarrow}&
    KO(X)
    \\
    {}^{ \mathllap{ (-) \otimes_{\mathbb{R}} \mathbb{C} } }
    \big\downarrow
      &&
    \big\downarrow
      {}^{ \mathrlap{ (-) \otimes_{\mathbb{R}} \mathbb{C} } }
    \\
    KO(X) 
      &\overset{ \psi^k }{\longrightarrow}&
    KO(X)
  }
$$

([Adams 62, Thm. 5.1. (iv)](#Adams62), [Karoubi 78, Prop. IV.7.25](#Karoubi78))



### Compatibility with the Chern character
 {#CompatibilityWithTheChernCharacter}


The Adams operation are compatible with the [[Chern character map]] in the following way:

+-- {: .num_defn #AdamsLikeOperationsOnRationalCohomology}
###### Definition
**(Adams-like operations on [[rational cohomology]])**

For $X$ a [[topological space]], with [[rational cohomology]] in even degrees denoted 

$$
  H^{ev}(X;\, \mathbb{Q})
  \;\coloneqq\;
  \underset{r \in \mathbb{N}}{\prod}
  H^{2 r}(X;\, \mathbb{Q})
$$

define graded [[linear maps]]

$$
  \psi^k_{H} \;\colon\; H^{ev}(X) \longrightarrow H^{ev}(X)
$$

for $k \in \mathbb{N}$ by taking their restriction to degree $2r$ to act by multiplication with $k^r$


$$
  \array{
    H^{2r}(X;\mathbb{Q})
    &\overset{\;\;\;\psi^k_H\;\;\;}{\longrightarrow}&
    H^{2r}(X;\mathbb{Q})
    \\
    \alpha_{2k} &\mapsto& k^{r} \cdot \alpha_{2r}
    \,.
  }
$$


=--

+-- {: .num_prop #AdamsOperationsAreCompatibleWithTheChernCharacter }
###### Proposition
**([[Adams operations compatible with the Chern character]])**

For $X$ a [[topological space]] with a finite [[CW-complex]]-[[mathematical structure]], the [[Chern character]] $ch$ on the [[complex topological K-theory]] of $X$ intertwines the [[Adams operations]] $\psi^n$ on K-theory with the Adams-like operations $\psi^n_H$ on [[rational cohomology]] from Def. \ref{AdamsLikeOperationsOnRationalCohomology}, for $k \geq 1$, in that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    K(X)
      &\overset{\;\;\;ch\;\;\;}{\longrightarrow}&
    H^{ev}(X;\,\mathbb{Q})
    \\
    {}^{ \mathllap{ \psi^k } }
    \big\downarrow
    &&
    \big\downarrow
    {}^{ \mathrlap{ \psi^k_H } }
    \\
    K(X)
      &\overset{\;\;\;ch\;\;\;}{\longrightarrow}&
    H^{ev}(X;\,\mathbb{Q})
    \,,
  }
$$

=--

([Adams 62, Thm. 5.1. (vi)](#Adams62), review in [Karoubi 78, Chapter V, Theorem 3.27](#Karoubi78), [Maakestad 06, Thm. 4.9](#Maakestad06))

+-- {: .proof}
###### Proof idea

Use the exponentional-formula for the [[Chern character]] with the  [[splitting principle]].

=--




\linebreak

### Adams conjecture

The [[Adams conjecture]] (a [[theorem]]) says that for all $k \in \mathbb{N}$ and $V \in K(X)$ there is $n \in \mathbb{N}$ such that the [[spherical fibration]] assigned to the [[K-theory]] class $k^n (\psi^k(V)-V)$ under the [[J-homomorphism]] is trivial, hence that


$$
  J
  \left(
     k^n \left(
       \psi^k(V) - V
     \right)
  \right)
  = 0
  \,.
$$


## Related concepts

* [[Lambda-ring]]

* [[Steenrod square]]

* [[Steenrod operation]]

* [[power operation]]

* [[Adams operation on Jacobi diagrams]]

## References

### General

The original article:

* {#Adams62} [[John Adams]], Section 5 of: _Vector fields on spheres_, Bull. Amer. Math. Soc. Volume 68, Number 1 (1962), 39-41 ([euclid:bams/1183524456](https://projecteuclid.org/euclid.bams/1183524456), [pdf](https://www.math.ens.fr/~benoist/refs/Adams.pdf))

Review:

* {#Karoubi78} [[Max Karoubi]], Section IV.7 in in: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften 226, Springer 1978 ([pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007/978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3))

* {#AguilarGitlerPrieto} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, Section 10 of: _Algebraic topology from a homotopical viewpoint_, Springer (2002)

* {#Maakestad06} Helge Maakestad, _Notes on the Chern-character_, Journal of Generalized Lie Theory and Applications, 2017, 11:1 ([arXiv:math/0612060](https://arxiv.org/abs/math/0612060), [doi:10.4172/1736-4337.100025](https://www.hilarispublisher.com/open-access/notes-on-the-cherncharacter-.pdf))

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lecture 10 in: _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])

* {#Wirthmuller12} [[Klaus Wirthmüller]], Section 11 of: _Vector Bundles and K-theory_, 2012 ([[wirthmueller-vector-bundles-and-k-theory.pdf:file]])

* {#Hatcher} [[Allen Hatcher]], section 2.3 of _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* Wikipedia, _[Adams operation](http://en.wikipedia.org/wiki/Adams_operation)_

* [[Jacob Lurie]], remark 2 in: _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 35 _The image of $J$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture35.pdf))
 
### In representation theory
 {#ReferencesInRepresentationTheory}

Adams operations on the [[representation ring]] (the [[equivariant K-theory]] of the point) are discussed in

* {#tomDieck79} [[Tammo tom Dieck]], section 3.5 of _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766 Springer 1979

* Robert Boltje, _A characterization of Adams operations on representation rings_, 2001 ([pdf](https://boltje.math.ucsc.edu/publications/p01v.pdf))

* [[Dai Tamaki]], [[Akira Kono]], Section 4.3 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))


* {#tomDieck09} [[Tammo tom Dieck]], section 6.2 of  _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

* [[Michael Boardman]], _Adams operations on Group representations_, 2007 ([pdf](http://www.math.jhu.edu/~jmb/note/adamrept.pdf))


* Ehud Meir, Markus Szymik, _Adams operations and symmetries of representation categories_ ([arXiv:1704.03389](https://arxiv.org/abs/1704.03389))

### In knot theory

Adams operations on [[Jacobi diagrams]] [[quotient vector space|modulo]] [[STU relations]] ([[Adams operation on Jacobi diagrams]]) are discussed in 

* {#BarNatan95} [[Dror Bar-Natan]], Theorem 7, Def. 3.11 and Section 6.3.4 of:  _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

[[!redirects Adams operations]]