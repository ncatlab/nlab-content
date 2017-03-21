
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[ring spectrum]] $R$ and [[module spectrum]] $E$ over $R$, there is the [[free construction|free]] $R$-[[algebra spectrum]] induced by $E$, this is the _symmetric algebra_ spectrum $Sym_R E$, in direct analogy to the construction of [[symmetric algebras]] on [[vector spaces]] (e.g. [Khan 16}(#Khan16)).

The underlying spectrum of the symmetric algebra is simply the [[direct sum]] ([[wedge sum]] of spectra) of all the $n$-fold [[smash products]] of $E$ over $R$ [[homotopy quotient|homotopy quotiented]] by the canonical [[∞-action]] of the [[symmetric group]] $\Sigma(n)$ (by [[permutation]] of factors):

$$
  Sym_R E 
  \;\coloneqq\;
  \underset{n \in \mathbb{N}}{\vee}
  (E^{\wedge^n})/\Sigma(n)
  \,.
$$

In contrast to ordinary [[symmetric algebras]] on ordinary [[modules]] over ordinary [[rings]], this means that the symmetric algebra on $R$ itself, regarded as a [[module spectrum]] itself has interesting structure:

$$
  \begin{aligned}
    Sym_R R
    & \simeq
    \underset{n \in \mathbb{N}}{\vee} 
     R / \Sigma(n)
    \\
    & \simeq
    \underset{n \in \mathbb{N}}{\vee} R \wedge (B \Sigma(n))_+
    \\
    & \simeq
    R \wedge
    \left(
      \underset{n \in \mathbb{N}}{\coprod}
      B \Sigma(n)
    \right)_+
  \end{aligned}
  \,,
$$

where $B \Sigma_n$ denotes the [[homotopy type]] of the [[classifying space]] of the [[symmetric group]] on $n$ elements (given for instance by the [[topological space]] $Emb(\{1, \cdots, n\}, \mathbb{R}^{\infty})/\Sigma(n)$).

In particular for $R = \mathbb{S}$ the [[sphere spectrum]], then  the _absolute [[spectral affine line]]_ $Sym_{\mathbb{S}}\mathbb{S}$ is nontrivial. This, and its structure of a [[Hopf ring spectrum]], is discussed in [Strickland-Turner 97](#StricklandTurner97).

More generally, 

$$
  R\{x_1, \cdots, x_n\} \coloneqq Sym_R (R^{\vee^n})
$$

is like a [[polynomial ring|polynomial]] [[algebra spectrum]] over $R$. 
Beware that there is a similar construction that is in general different, namely

$$
  R[X_1, \cdots, x_n] \coloneqq R \wedge \Sigma^\infty(\mathbb{N}_+)
$$

where on the right we have the "monoid $\infty$-algebra" of the [[natural numbers]], directly analogous to the [[∞-group ∞-ring]] construction. There is a canonical comparison homomorphisms

$$
  R\{x_1, \cdots, x_n\} \longrightarrow R[x_1, \cdots, x_n]
  \,.
$$

This is an [[equivalence]] if $R$ is of [[characteristic zero]] ([Khan 16, prop. 2.7.4](#Khan16)).


{#OnSuspensionOfGroundRingInIntroduction} Similarly, if $E = \Sigma^n R \simeq R \wedge S^n$ is a [[suspension]] of $R$, regarded as an $R$-[[module spectrum]], then
$$
  \begin{aligned}
    Sym_R(\Sigma^n R)
    & \simeq
    R \wedge \left(
      \underset{n \in \mathbb{N}}{\coprod} S^n/\Sigma(n)
    \right)_+
    \\
    & \simeq 
    R \wedge \left(
      \underset{n \in \mathbb{N}}{\coprod}
      (B \Sigma(n))^{\tau_n}
    \right)
  \end{aligned}
  \,,
$$
where on the right we have the [[Thom space]] of the [[vector bundle]] $\tau_n$ [[associated bundle|associated]] to the $\Sigma(n)$-[[universal principal bundle]] via the canonical [[action]] of $\Sigma(n)$ on $\mathbb{R}^n$ (see also at [symmetric group -- Classifying space and Thom space](permutation#ClassifyingSpaceAndThomSpace)).


The operation $Sym_R$ is of course functorial, and hence any choice of $R$-linear map $f_x \colon R \to E$ induces morphisms

$$
  R \wedge B \Sigma(n)_+ \simeq Sym^n_R(R) \longrightarrow Sym_R^n(E)
  \,.
$$

These correspond to [[power operation]] in [[generalized (Eilenberg-Steenrod) cohomology]] ([Rezk 10, slide 4](#Rezk10)).

## Examples

### Spectral affine lines

For $R$ a ([[connective spectrum|connective]]) [[E-∞ ring]], the 

$$
  \mathbb{A}^1_R \coloneqq Spec( Sym_R(R) )
$$

is the [[spectral affine line]] over $R$.

### Spectral superpoints

By the discussion at _[[spectral super scheme]]_, it makes good sense to regard the concept of a [[spectral scheme]] over an [[even cohomology theory|even]] [[periodic ring spectrum]] $R$ as the lift to [[spectral geometry]] of the concept of ordinary [[super schemes]]. Under this identification the ordinary [[superpoint]], which is the [[spectrum of a commutative ring]] of the graded symmetric algebra on a single odd generator ("[[ring of dual numbers]]")

$$
  \mathbb{A}_k^{0 \vert 1}
  \;\simeq\;
  Spec( Sym_k (k[1]) )
$$ 

is given by the corresponding [[spectral scheme]] given by the spectral symmetric algebra on the [[suspension spectrum]] of $R$:

$$
  \begin{aligned}
    R^{0 \vert 1}
     &\coloneqq
    Spec
    \left(
      Sym_R (\Sigma R)
    \right)
    \\
    & \simeq
    R \wedge
    Sym_{\mathbb{S}}(\Sigma \mathbb{S})
  \end{aligned}
$$


## References

The symmetric algebra spectrum of the [[sphere spectrum]], and its structure as a [[Hopf ring spectrum]] is discussed in

* {#StricklandTurner97} [[Neil Strickland]], [[Paul Turner]], _Rational Morava $E$-theory and $D S^0$_, Topology Volume 36, Issue 1, January 1997, Pages 137-151 ([pdf](http://hopf.math.purdue.edu/Strickland-PTurner/rme.pdf))

Symmetric algebras in the context of [[power operation]] on [[generalized (Eilenberg-Steenrod) cohomology]] are discussed in 

* {#Rezk 09} [[Charles Rezk]], _Power operations in Morava E-theory --  a survey_ (2009) ([pdf](http://www.math.uiuc.edu/~rezk/midwest-2009-power-ops.pdf)) 

* {#Rezk10} [[Charles Rezk]] _Power operations in Morava $E$-Theory_ (2010) ([pdf](http://www.math.uiuc.edu/~rezk/baltimore-2010-power-ops-handout.pdf))

* {#Rezk14} [[Charles Rezk]], _Isogenies, power operations, and homotopy theory_, article ([pdf](http://www.math.uiuc.edu/~rezk/rezk-icm-talk-posted.pdf)) and talk at ICM 2014 ([pdf](http://www.math.uiuc.edu/~rezk/rezk-icm-2014-slides.pdf))

See also

* {#Khan16} [[Adeel Khan]], sections 2.6 and 2.7 of _Brave new motivic homotopy theory I_ ([arXiv:1610.06871](https://arxiv.org/abs/1610.06871))

[[!redirects spectral symmetric algebra]]

[[!redirects symmetric algebra spectra]]

[[!redirects symmetric algebra spectrum]]

[[!redirects spectral polynomial algebra]]
[[!redirects spectral polynomial algebras]]

[[!redirects spectral polynomial ring]]
[[!redirects spectral polynomial rings]]

