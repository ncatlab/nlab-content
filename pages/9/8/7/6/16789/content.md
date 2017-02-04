
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[sphere]] of [[dimension]] 4.

## Properties

### Homotopy groups

The [[homotopy groups]] of the 4-sphere in low degree are

| $k$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11  | 12 |
|-----|---|---|---|---|---|---|---|---|---|---|----|-----|----|
| $\pi_k(S^4)$ | $\ast$ | 0 | 0 | 0 | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z} \times \mathbb{Z}_2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_{24} \times \mathbb{Z}_3$ | $\mathbb{Z}_{15}$ | $\mathbb{Z}_2$ | 

### As part of the quaternionic Hopf fibration

The 4-sphere participates in the [[quaternionic Hopf fibration]], the analog of the complex [[Hopf fibration]] with the field of [[complex numbers]] replaced by the division ring of [[quaternions]] or Hamiltonian numbers $\mathbb{H}$.

$$
  \array{
    S^3 &\hookrightarrow& S^7
    \\
    && \downarrow^\mathrlap{p}
    \\
    && S^4 &\stackrel{}{\longrightarrow}& \mathbf{B} SU(2)
  }
$$

Here the idea is that $S^7$ can be construed as $\{(x, y) \in \mathbb{H}^2: {|x|}^2 + {|y|}^2 = 1\}$, with $p$ mapping $(x, y)$ to $x/y$ as an element in the [[projective line]] $\mathbb{P}^1(\mathbb{H}) \cong S^4$, with each [[fiber]] a [[torsor]] parametrized by quaternionic [[scalars]] $\lambda$ of unit [[norm]] (so $\lambda \in S^3$).  This canonical $S^3$-bundle (or $SU(2)$-bundle) is classified by a map $S^4 \to \mathbf{B} SU(2)$. 

### Exotic smooth structures

It is open whether the 4-sphere admits an [[exotic smooth structure]]. See ([Freedman-Gompf-Morrison-Walker 09](#FreedmanGompfMorrisonWalker09)) for review.


### Circle action
  {#CircleAction}

The [[3-sphere]] carries a [[free action|free]] [[circle action]], whose [[quotient]] [[projection]] $S^3 \to S^2$ is the [[complex Hopf fibration]]. Under [[suspension]] this yields a circle action on $S^4$, which however is _not_ [[free action|free]] anymore. Hence the suspension of the complex Hopf fibration is of the form

$$
  S^4 \longrightarrow S^3
  \,.
$$

The ordinary [[quotient]] of the induced [[circle action]] on $S^4$ is the [[suspension]] of $S^2$, hence is $S^3$:

$$
  S^4 / S^1 \simeq S^3
$$

The [[fixed point]] set of the action is the two poles introduced by the suspension, hence forms the [[0-sphere]] space. Since this is not the [[empty set]], the [[homotopy quotient]] $S^4 // S^1$ of the [[circle action]] differs from $S^3$, but there is still the canonical [[projection]]

$$
  S^4//S^1 \longrightarrow S^4 / S^1 \simeq S^3
  \,.
$$ 

Hence both $S^4$ and $S^4 // S^1$ are canonically [[homotopy types]] over $S^3$. A [[KS-model]] in [[rational homotopy theory]] of these projections is given in [Roig & Saralegi-Aranguren 00, second page](#RoigSaralegiAranguren00):

Write

$$
  CE(\mathfrak{l}(S^3))) = Sym^\bullet \langle \underset{\text{deg 3}}{\underbrace{h_3}} \rangle
$$

for the [[minimal Sullivan model]] of the [[3-sphere]]. Then [[minimal KS-models]] for $S^4$ and $S^4 // S^1$, as [[dg-modules]] over $CE(\mathfrak{l}(S^3))$ are given as follows:

$$
  S^4 
  \;\;:\;\;
  Sym^\bullet \langle h_3\rangle 
  \otimes
  \langle 
     f_{2p}, \omega_{2(p+1)} \,\vert\, p \in \mathbb{N} 
  \rangle
  \,,
  d \colon
  \left\{
    \begin{aligned}
      f_0 & \mapsto 0 
      \\
      f_2 & \mapsto h_3
      \\
      f_{2p+4} & \mapsto h_3 \wedge f_{2p+2}
      \\
      \omega_{4} & \mapsto 0
      \\
      \omega_{2p+6} & \mapsto h_3 \wedge \omega_{2p+4}
    \end{aligned}
    \right.
$$

{#MinimaldgmoduleForRationalS4ModS1}
$$
  S^4 // S^1
  \;\;\colon\;\;
  Sym^\bullet  \langle h_3 , \omega_2 \rangle 
   \otimes
  \langle 
     f_{2p}, \omega_{2(p+1)} \,\vert\, p \in \mathbb{N}
  \rangle
  \,,
  d \colon
  \left\{
    \begin{aligned}
      f_0 & \mapsto 0
      \\
      f_2 & \mapsto h_3
      \\
      f_{2p+4} &\mapsto h_3 \wedge f_{2p+2}
      \\
      \omega_2 & \mapsto 0
      \\
      \omega_{2p+2} & \mapsto h_3 \wedge \omega_{2p}
    \end{aligned}
  \right.
$$


Notice how we changed the notation of the generators compared to [Roig & Saralegi-Aranguren 00, second page](#RoigSaralegiAranguren00), to bring out the pattern:

|    Roig    |       here      |
|------------|-----------------|
|     $a$    |        $h_3$    |
|     $1$    |       $f_0$     |
|  $c_{2n}$  |    $f_{2n+2}$   |
| $c_{2n+1}$ | $\omega_{2n+4}$ |
|    $e$     |    $\omega_2$   |




## References

* {#FreedmanGompfMorrisonWalker09} [[Michael Freedman]], [[Robert Gompf]], [[Scott Morrison]], [[Kevin Walker]], _Man and machine thinking about the smooth 4-dimensional Poincar&#233; conjecture_, Quantum Topology, Volume 1, Issue 2 (2010), pp. 171-208 ([arXiv:0906.5177](http://arxiv.org/abs/0906.5177))

* {#RoigSaralegiAranguren00} [[Agustí Roig]], [[Martintxo Saralegi-Aranguren]], _Minimal Models for Non-Free Circle Actions_, Illinois Journal of Mathematics, volume 44, number 4 (2000) ([arXiv:math/0004141](https://arxiv.org/abs/math/0004141))


[[!redirects 4-spheres]]