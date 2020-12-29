


> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}




## Idea

(...)

## Definition

For $n \in \mathbb{N}$, $n \geq 1$, consider the [[composition|composite]] [[morphism]] of [[homotopy types]]

$$
  B \Omega^2 SU(n)
  \simeq
  \Omega SU(n)
  \simeq
  \Omega^2
  B SU(n)
  \overset{
    \Omega^2 B i
  }{
   \longrightarrow
  }
  \Omega^2 B U
  \underoverset
    {\simeq}
    {\beta}
    {\longrightarrow}
  B U
  \longrightarrow
  B O
  \,,
$$ 

where 

1. On the left we have [[looping and delooping]] [[weak homotopy equivalence|equivalences]] ([this Prop.](May+recognition+theorem#RecognitionForGroupsInAnInfinityTopos)), using that the [[based loop space]] $\Omega SU(n)$ is [[connected homotopy type|connected]];

1. $SU(n) \overset{i}{\longrightarrow} SU \coloneqq \underset{\underset{k}{\longrightarrow}} SU(k)$ is the [[coprojection]] of [[SU(n)]] into the [[stable unitary group]]:

1. $\beta$ is the [[Bott periodicity]] [[weak homotopy equivalence|equivalence]].

Regarded as a universal [[tangential structure]], this induces the corresponding [[Thom spectrum]] $M\big(\Omega^2 SU(n)\big)$ (introduced as "$X(n)$" in [Ravenel 84, Section 3](#Ravenel84)).

(...)



## Properties

(...)

This carries the finite-rank analog of the [[universal complex orientation of MU]]: [Hopkins 84, Prop. 1.2.1](#Hopkins84)

(...)

## Examples

(...)

For $n=1$ we have the [[sphere spectrum]]

$$
  M \Omega^2 SU(1) 
  \simeq
  M 1
  \simeq
  \mathbb{S}
$$

For $n = \infty$ we have [[MU]]:

$$
  \underset{
     \underset{n}{\longrightarrow}
   }{lim}
   M \Omega^2 SU(n)
   \simeq
   M \Omega^2 SU
   \simeq
   M U
$$


## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

[[!include finite-rank complex orientation and MΩSUn -- references]]

[[!redirects MOmegaSUn]]

[[!redirects Ravenel spectrum]]
[[!redirects Ravenel spectra]]






