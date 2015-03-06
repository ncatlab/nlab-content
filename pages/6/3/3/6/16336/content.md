
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Where a [[vertex operator algebra]] encodes one chiral half of a [[2d CFT]], a _full field algebra_ combines two vertex operator algebras to produce a genuine 2d CFT defined on the [[complex plane]] (i.e. on [[genus]] 0, notice that to define it on all genera one needs still more information, see at _[[FRS-theorem]]_).

## Properties

The following result establishes which pairs of [[vertex operator algebras]] can appear as the left and right chiral parts of a _[[full field algebra]]_ in the sense of ([Huang-Kong 05](#HuangKong05)), etc. (see [[vertex operator algebra]]).

+-- {: .num_defn}
###### Definition

Two [[modular tensor categories]] are said to have the same **Witt class**
if there exist two [[spherical categories]] $S$ and $T$ such that
we have an [[equivalence of categories|equivalence]] of [[ribbon categories]]

$$
  C \boxtimes \mathcal{Z}(S) \simeq D \boxtimes \mathcal{Z}(T)
$$

=--

Here $\mathcal{Z}(S)$ is the category whose objects are pairs $(Z, z)$ consisting of an
object $Z \in S$ and a [[natural isomorphism]] 
$z_X : Z \otimes X \stackrel{\simeq}{\to} X \otimes Z$, such that for al
objects $X, Y \in S$ we have

$$
  \array{
    Z \otimes X \otimes Y &&\stackrel{z_{X \otimes Y}}{\to}&& 
    X \otimes Y \otimes Z
    \\
    & {}_{\mathllap{z_x \otimes Id}}\searrow && \nearrow_{Id \otimes \mathrlap{z_y^{-1}}}
    \\
    && X \otimes Z \otimes Y
  }
$$

This becomes a monoidal category itself by setting

$$
  (Z,z) \otimes (W,w) := (Z \otimes W, z \otimes w)
  \,.
$$

+-- {: .num_theorem}
###### Theorem
**([[Michael Müger]])**

If $S$ is a [[spherical category]] then $\mathcal{Z}(S)$ is a [[modular tensor category]].

=--

+-- {: .num_theorem}
###### Theorem
**([[Michael Müger]])**


If $C$ is a [[modular tensor category]] then there is an equivalence of 
[[ribbon categories]]

$$
  \mathcal{Z}
  \stackrel{\simeq}{\leftarrow}
  C \boxtimes \bar C
$$

=--


+-- {: .num_theorem}
###### Theorem

Two [[vertex operator algebra]]s $V$ may appear as the left and right chiral 
halfs of a full conformal field theory precisely if their [[modular tensor categories]] of representations have the same
Witt class.

=--

## Related concepts

* [[chiral algebra]]

## References

* {#HuangKong05} [[Yi-Zhi Huang]], [[Liang Kong]], _Full field algebras_, Commun.Math.Phys.272:345-396,2007 ([arXiv:0511328](http://arxiv.org/abs/math/0511328))

* {#Kong06} [[Liang Kong]], _Full field algebras, operads and tensor categories_, Adv. Math.213:271-340, 2007 ([arXiv:0603065](http://arxiv.org/abs/math/0603065))

Survey and review includes

* {#Kong11} [[Liang Kong]] _Conformal field theory and a new geometry_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ ([arXiv:1107.3649](http://arxiv.org/abs/1107.3649))
 