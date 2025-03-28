
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[algebraic topology]], _power operations_ are [[cohomology operations]] in [[multiplicative cohomology theory]] which are higher-degree analogs of [[cup product]]-squares [[symmetric algebra|symmetrized]] in the appropriate [[homotopy theory|homotopy-theoretic sense]].

+-- {: .num_remark #AsPDerivations}
###### Remark

At least to some extent, power operations may be understood as the [[higher algebra]]-generalization of the ordinary $p$-power map $(-)^p$ on a [[commutative ring]], the one that appears in the definition of [[Fermat quotients]], [[p-derivations]] and [[Frobenius morphisms]].

See for instance [Lurie, from remark 2.2.7 on](#Lurie) for relation to the [[Frobenius homomorphism]] and see the example [below](#OnK1LocalKUAlgebras). See [Guillot 06](#Guillot06), [Morava-Santhanam 12](#MoravaSanthanam12) for further discussion and speculation in this direction.

=--

For $E$ an [[E-∞ ring]] and $X$ a [[topological space]] ([[∞-groupoid]], [[homotopy type]]), a map $a\;\colon\;X \to E$ is a [[cocycle]] in the [[Whitehead-generalized cohomology]] of $X$ with [[coefficients]] in $E$. 

The $n$-th [[cup product]] power of this $a$ is the composite

$$
  a^n 
    \;\colon\; 
  X^{\times n} 
    \overset{\;\;\;
      (a,\cdots,a)
    \;\;\;}{\longrightarrow} 
  E^{\times n} 
    \overset{\;\; \mu \;\;}{\longrightarrow} 
  E
  \,,
$$

where the second map is given the [[multiplication]] operation in the [[ring spectrum]] $E$. Since this is, by assumption, commutative up to coherent higher homotopy, this map factors through the [[homotopy quotient]] by the [[∞-action]] of the [[symmetric group]] $\Sigma_n$:

$$
  a^n 
    \;\colon\; 
  X \times \ast \sslash \Sigma_n 
   \longrightarrow   
  X^n \sslash \Sigma_n 
    \longrightarrow 
  E
  \,.
$$

The cohomology class of this $E$-cocycle on $X \times B \Sigma_n$ is the $n$-th (symmetric) power of $a$.





## Examples

### Steenrod squares and Steenrod power operations
 {#SteenrodPowerOperations}

On [[ordinary cohomology]] over a [[topological space]], the power operations are the [[Steenrod operations]];

Specifically for $n = 2$ and $E = H \mathbb{Z}_2$, the second (symmetric) power of $a \in H(X,\mathbb{Z}_2)$ is an element in $H^\bullet(\mathbb{R}P^\infty \times X, \mathbb{Z}_2) \simeq H^\bullet(X,\mathbb{Z}_2)[x]$ and the [[coefficients]] of this [[polynomial]] in $x$ are the [[Steenrod operations]] on $a$.

For $p \gt 2$ there are the Steenrod power operations (e.g. [Rognes 12, around theorem 3.3](#Rognes12), quick exposition [here](https://www.math.purdue.edu/~pvankoug/talks/steenrod16.pdf#page=3)).

### Kudo-Araki-Dyer-Lashof operations

On an [[infinite loop space]] the power operations are the [[Kudo-Araki-Dyer-Lashof operations]]

### Adams operations

In the context of  [[complex K-theory]] power operations are the [[Adams operations]].


### On $K(1)$-local $KU$-algebras
 {#OnK1LocalKUAlgebras}

> From [this MO comment](http://mathoverflow.net/a/178627/381) by [[Akhil Mathew]]:

Let $R$ be a [[K(n)-local stable homotopy theory|K(1)-local]] [[E-∞ ring]] under ([[p-completion|p-adic]]) [[complex K-theory]] [[KU]]. Then there exists a basic power operation $\theta \colon \pi_0 R \to \pi_0 R$ (see [Hopkins](#Hopkins)) such that : 

*  $\psi(x) \stackrel{\mathrm{def}}{=} x^p + p \theta(x)$ defines a [[ring homomorphism]] from $\pi_0 R \to \pi_0 R$.

* $\theta$ satisfies all the identities needed to make $\psi$ a ring-homomorphism after "division by $p$." For instance $\psi(x+y) = \psi(x) + \psi(y)$ implies that 

  $$
    \theta(x+y) = \theta(x) + \theta(y) + \frac{x^p - y^p - (x+y)^p}{p}
    \,,
  $$ 

  where the last term is an integral polynomial in $x,y$ and is interpreted as such. 

(see also [Rezk 09, example 1.3](#Rezk09))

This is a "$\theta$-algebra."/[[p-derivation]] as in remark \ref{AsPDerivations} above.

Notice that $\psi$ is, in particular, a lift of the [[Frobenius homomorphism]]. There are generalizations of $\psi, \theta$ at higher [[chromatic levels]], too, and there is a modular interpretation of the resulting algebraic structure in ([Rezk 09](#Rezk09)).

By ([Strickland 98](#Strickland98)) we have that if $G$ is the [[formal group]] associated to a [[Morava E-theory]], then Frobenius lifts (twhich corresponds to degree $p^k$ subgroups of $G$) are classified by maps into $E^0(B \Sigma_{p^r})/I_{t r}$ where $I_{t r}$ is the transfer ideal. So, for example, the map $\psi$ above corresponds to a universal map $KU^0 \to KU^0(B \Sigma_p)/I_{t r} \simeq KU^0$.

## Related concepts

* [[Adams operation]]

* [[logarithmic cohomology operation]]

* [[spectral symmetric algebra]]

## References

The basic idea is nicely described in 

* [[Charles Rezk]], [MO comment](http://mathoverflow.net/a/6384/381) Nov 09

(from which some of the above text is adapted).

More technical surveys include

* [[Charles Rezk]], _Lectures on power operations_ ([dvi](http://www.math.uiuc.edu/~rezk/power-operation-lectures.dvi)) (2006)

* [[Charles Rezk]], _Power operations in Morava E-theory --  a survey_ (2009) ([pdf](http://www.math.uiuc.edu/~rezk/midwest-2009-power-ops.pdf))

* {#Rezk14} [[Charles Rezk]], _Isogenies, power operations, and homotopy theory_, article ([pdf](http://www.math.uiuc.edu/~rezk/rezk-icm-talk-posted.pdf)) and talk at ICM 2014 ([pdf](http://www.math.uiuc.edu/~rezk/rezk-icm-2014-slides.pdf))

Lecture notes on the Steenrod squares and power operations include

* {#Rognes12} [[John Rognes]], section 3 of _The Adams spectral sequence_, 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

The original articles are

* {#Rezk06} [[Charles Rezk]], _The units of a ring spectrum and a logarithmic cohomology operation_, J. Amer. Math. Soc. 19 (2006), 969-1014 ([arXiv:math/0407022](http://arxiv.org/abs/math/0407022))

* [[Charles Rezk]], _Power operations for Morava E-theory of height 2 at the prime 2_ ([arXiv:0812.1320](http://arxiv.org/abs/0812.1320))

* {#Rezk09} [[Charles Rezk]], _The congruence criterion for power operations in Morava E-theory_, Homology, Homotopy and Applications, 11(2), 327-379 ([arXiv:0902.2499](http://arxiv.org/abs/0902.2499))

More discussion in the generality of [[E-infinity arithmetic geometry]] is in 

* {#Lurie} [[Jacob Lurie]], _[[Rational and p-adic Homotopy Theory]]_

Discussion for $K(1)$-local $E_\infty$-rings is in 

* {#Hopkins} [[Michael Hopkins]], _$K(1)$-local $E_\infty$-Ring spectra_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/knlocal.pdf))

and discussion of power operations in [[Morava E-theory]] is in 

* [[Matthew Ando]], _Isogenies of formal group laws and power operations in the cohomology theories $E_n$_, Duke Math. J. Volume 79, Number 2 (1995), 423-485 ([Euclid](http://projecteuclid.org/euclid.dmj/1077285158))

* {#Strickland98} [[Neil Strickland]], _Morava E-theory of symmetric groups_ ([arXiv:math/9801125](http://arxiv.org/abs/math/9801125))

Comments on the analogy between power operations in homotopy theory and [[Lambda ring]] [[structure]] in [[Borger's absolute geometry]]:

* {#Guillot06} [[Pierre Guillot]], _Adams operations in cohomotopy_ &lbrack;[arXiv:0612327](http://arxiv.org/abs/math/0612327)&rbrack;

* {#MoravaSanthanam12} [[Jack Morava]], Rakha Santhanam: _Power operations and Absolute geometry_ (2012) &lbrack;[pdf](/nlab/files/AbsolutePower.pdf)&rbrack;

[[!redirects power operations]]