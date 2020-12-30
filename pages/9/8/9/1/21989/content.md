

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

Due to [[Bott periodicity]], the [[coprojection]] $SU(n) \hookrightarrow \mathrm{U}$ of any [[special unitary group]] $SU(n)$ into the [[stable unitary group]] induces a map $\Omega SU(n) \longrightarrow B \mathrm{U} \to B\mathrm{O}$ from the [[based loop space]] of $SU(n)$ to the [[classifying space]] of $\mathrm{U}$ and hence of $\mathrm{O}$. This may be regarded as defining a notion of $\Omega^2 SU(n)$-[[tangential structure]]. 

The corresponding [[Thom spectra]] $M \big(\Omega^2 SU(n)\big)$ were denoted "$X(n)$" in [Ravenel 84, Section 3](#Ravenel84), used there for analysis of the [[Adams spectral sequence]] (see also [Ravenel 86, Section 6.5](#Ravenel86)) and influential on [[Ravenel's conjectures]] (notably the [[nilpotence theorem]]); and thus have come to be known as _Ravenel's spectra_. 

These spectra turn out to be finite-rank analogs of [[MU]] in [[complex oriented cohomology theory]] as one passes from full complex orientation to complex orientation up to rank ("degree") $n$ ([Hopkins 84, Section 1.2](#Hopkins84)). For instance, just as [[MU]] is [[p-local spectrum|p-locally]] a [[wedge sum]] of [[suspensions]] of [[BP]], so Ravenel's spectra are $p$-locally wedge sums of suspensions of spectra that Ravenel denoted $T(k)$.


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

1. $SU(n) \overset{i}{\longrightarrow} SU \coloneqq \underset{\underset{k}{\longrightarrow}} SU(k)$ is the [[coprojection]] of [[SU(n)]] into the [[special unitary group|special]] [[stable unitary group]]:

1. $\beta$ is the [[Bott periodicity]] [[weak homotopy equivalence|equivalence]].

Regarded as a universal [[tangential structure]], this induces the corresponding [[Thom spectrum]] $M\big(\Omega^2 SU(n)\big)$ (introduced as "$X(n)$" in [Ravenel 84, Section 3](#Ravenel84)).

(...)



## Properties

(...)

This carries the finite-rank analog of the [[universal complex orientation of MU]]: [Hopkins 84, Prop. 1.2.1](#Hopkins84)

(...)

## Examples

For $n=1$ we have that $SU(1) = 1$ is the [[trivial group]], so that Ravenel's spectrum at this stage is the [[sphere spectrum]]

$$
  M \Omega^2 SU(1) 
  \simeq
  M 1
  \simeq
  \mathbb{S}
$$

On the other hand, the [[colimit]] of Ravenel's spectra as $n \to \infty$  is [[MU]], essentially by construction:

$$
  \underset{
     \underset{n}{\longrightarrow}
   }{lim}
   M \Omega^2 SU(n)
   \simeq
   M \Omega^2 SU
   \simeq
   M U
   \,.
$$

Hence the [[tower]] of Ravenel's spectra interpolates between the [[sphere spectrum]] and [[MU]]

$$
  \mathbb{S}
  \longrightarrow
  M \Omega^2 SU(2)
  \longrightarrow
  M \Omega^2 SU(3)
  \longrightarrow
  \cdots
  \longrightarrow
  M U
  \,.
$$

Accordingly, the [[Brown representability theorem|corresponding]] [[tower]] of [[Whitehead generalized cohomology theories]] interpolated between [[stable Cohomotopy]] and complex [[cobordism cohomology]].


## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

[[!include finite-rank complex orientation and MΩSUn -- references]]

[[!redirects Ravenel's spectra]]

[[!redirects MΩΩSU(n)]]
[[!redirects MOmegaSUn]]

[[!redirects Ravenel spectrum]]
[[!redirects Ravenel spectra]]






