
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn}
###### Definition

The **framed little 2-disk operad** is the [[operad]] $fD_2$ in [[Top]] whose [[topological space]] $fD_2(n)$ of $n$-ary operations is the space of maps

$$
  \coprod_n D \to D
$$

from $n$-copies of the 2-[[ball]] to itself, which restrict on each component to a map that is a combination of 

* a translation

* a dilation

* a rotation

of the disk (regarded via its standard [[embedding]] $D \hookrightarrow \mathbb{R}^2$ into the 2-dimensional [[Cartesian space]]) such that the images of all disks are disjoint.
=--

+-- {: .num_remark}
###### Remark

This differs from the [[little 2-disk operad]] by the fact that rotations of the disks are admitted. Under passing to chains and then to [[homology]], this operation gives rise to the BV-operator in a [[BV-algebra]]. See [Properties](#Properties) below.

=--

## Properties {#Properties}


+-- {: .num_theorem}
###### Theorem

The [[homology]] of the framed little 2-disk operad in chain complexes is the [[BV-operad]] $BV$ the operad for [[BV-algebra]]s:


$$
  BV \simeq H_\bullet(fD_2)
  \,.
$$

=--

This is due to ([Getzler](#Getzler)).

+-- {: .num_theorem}
###### Theorem

The framed little disk operad is [[formal dg-algebra|formal]] in characteristic zero. 

This means that there is a zig-zag of [[quasi-isomorphism]]s

$$
  C_\bullet(fD_2) 
   \stackrel{\simeq}{\leftarrow}
   \stackrel{\simeq}{\to}
   \cdots 
   \stackrel{\simeq}{\leftarrow}
   \stackrel{\simeq}{\to}
   H_\bullet(fD_2)
  \,.
$$

=--

This is due to [Severa 09](#Severa09),
[Giansiracusa-Salvatore 09)](#GiansiracusaSalvatore09). See also ([Valette, slide 35](#Valette)).

Accordingly one makes the following definition:

+-- {: .num_defn}
###### Definition

The operad for [[homotopy BV-algebra]]s is any cofibrant [[resolution]] of $BV \simeq  H_\bullet(fD_2)$, or equivalently of $C_\bullet(fD_2)$.

=--

+-- {: .num_defn}
###### Definition

Write $R \beta_j$ for the [[ribbon braid group]] on $j$ elements and $P R \beta_j$ for the [[kernel]] of the surjection $R \beta_j \to \Sigma_j$ onto the [[symmetric group]].

Say that a [[ribbon operad]] $P$ is an **$R_\infty$-operad** if the [[ribbon braid group]]s  act freely and properly on $P$ and if each [[topological space]] $P(k)$ is [[contractible]].

=--

+-- {: .num_theorem}
###### Theorem


If $P$ is an $R_\infty$-operad, then the sequence of quotient spaces $\{P(n)/P R \beta_n\}$  forms a symmetric operad equivalent to the frame little disks operad.

=--

This is ([Wahl, lemma 1.5.17](#Wahl)).

## Related concepts

* **framed little 2-disk operad**

* [[framed little n-disk operad]]

* [[BD operad]]

[[!include deformation quantization - table]]

## References

The framed little 2-disk operad was introduced in

* {#Getzler} [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159 (1994), no. 2, 265&#8211;285. ([arXiv](http://arxiv.org/abs/hep-th/9212043))


For the relation to ribbons see

* {#Wahl} [[Nathalie Wahl]], _Ribbon braids and related operads_ PhD thesis, Oxford (2001) ([pdf](http://eprints.maths.ox.ac.uk/43/1/wahl.pdf)).


The formality of $fD_2$ was shown in 

* {#GiansiracusaSalvatore09} [[Jeffrey Giansiracusa]], [[Paolo Salvatore]], _Formality of the framed little 2-discs operad and semidirect products_ , in: _Homotopy theory of function spaces and related topics_, Cont. Math. 519, AMS, pp. 115-121  ([arxiv 0911.4428](http://arxiv.org/PS_cache/arxiv/abs/0911/0911.4428))
 

and 

* {#Severa09} [[Pavol Severa]], _Formality of the chain operad of framed little disks_,  ([arxiv AT 0902.3576](http://arxiv.org/PS_cache/arxiv/abs/0902/0902.3576))


Discussion of [[homotopy BV-algebra]]s is in 

* [[Imma Galvez-Carrillo]], [[Andy Tonks]], [[Bruno Valette]], _Homotopy Batalin-Vilkovisky algebras_ ([arXiv:0907.2246](http://arxiv.org/abs/0907.2246))

see also 

* [[Imma Galvez-Carrillo]], [[Vassily Gorbounov]], [[Andy Tonks]], _Homotopy Gerstenhaber structures and vertex algebras_, [math/0611231.QA](https://arxiv.org/abs/math/0611231)

Slides of a talk summarizing this are at

* {#Valette} [[Bruno Valette]], _Homotopy Batalin-Vilkovisky algebras_ ([pdf](http://math.unice.fr/~brunov/download/Homotopy%20BV.pdf))

[[!redirects E2-operad]] 
[[!redirects E2-operads]] 

[[!redirects E2 operad]] 
[[!redirects E2 operads]] 


[[!redirects framed little disk operad]]
[[!redirects framed little disks operad]]

[[!redirects framed little disk operads]]
[[!redirects framed little disks operads]]

[[!redirects framed little disc operad]]
[[!redirects framed little discs operad]]

[[!redirects framed little disc operads]]
[[!redirects framed little discs operads]]

[[!redirects BV-operad]]


