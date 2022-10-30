
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
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

In [[quantum field theory]] what has come to be known as the _holographic principle_ is the fact that the [[partition function]]s of some [[quantum field theories]] of [[dimension]] $n$ may be identified with [[state]]s of [[TQFT]]s of dimension $n + 1$.

Notice that for $\Sigma$ an $(n+1)$-dimensional manifold with $n$-dimensional [[boundary]] $\partial \Sigma$, regarded as a [[cobordism]] $\Sigma : \emptyset \to \partial \Sigma$, an $(n+1)$-dimensional TQFT assigns a morphism

$$
  Z(\Sigma) : 1 \to Z(\partial \Sigma)
  \,,
$$

hence an element of the space $Z(\partial \Sigma)$. Under holography, this element is identified with the [[partition function]] of an $n$-dimensional QFT evaluated on the manifold (without boundary) $\partial \Sigma$.

The idea that some systems in physics are governed by other systems "localized at a boundary" in this kind of way was originally suggested by the behaviour of [[black hole]]s in [[general relativity]]: their [[black hole entropy]] is proportional to their "surface", as reflected by the [[generalized second law of thermodynamics]]. This made [[Gerard 't Hooft]] suggest a general principle, called the _holographic principle_ , which however remained somewhat vague.

Later two more precise classes of correspondences were identified, that are regarded now as precise examples of the general idea of the holographic principle:

1. Systems of [[Chern-Simons theory]] and [[higher dimensional Chern-Simons theory]] can be shown explicitly to have spaces of states that are canonically identified with correlator spaces of [[CFT]]s ([[conformal block]]s) and [[self-dual higher gauge theory]] on their boundary. 

1. Systems of [[quantum gravity]] in various dimensions as given by [[string theory]] on asymptocially [[anti de Sitter spacetime]]s have been checked not in total but in a multitude of special aspects in special cases to be dual to [[supersymmetric]] [[CFT]]s on their asymptotic boundary -- this is called [[AdS/CFT correspondence]].


+-- {: .num_remark}
###### Remark

In view of these two classes of examples it is maybe noteworthy that one can see that also closed [[string field theory]], which is supposed to be one side of the [[AdS/CFT correspondence]], has the form of an [[schreiber:infinity-Chern-Simons theory]], as discussed there, for the [[L-infinity algebra]] of closed string correlators. So maybe the above two different realizations of the holographic principle are really aspects of one single mechanism for $\infty$-Chern-Simons theory. 

Evidence for this also comes from the details of the AdS/CFT mechanism. In ([Witten98](#Witten98)) it is discussed how the [SYM/IIB duality](#SYMAds5) is carried by the Chern-Simons term $\int B_{NS} \wedge d B_{RR}$ in the [[type II string theory]] action, the [6d(2,0)/AdS7 duality](#6dAdS7) - is induced by the Chern-Simons term $\int C_3 \wedge d C_3 \wedge d C_3$ of the [[11-dimensional supergravity]] action. 

=--

Below at _[Examples](Examples)_ we list some systems for which something along these lines is known.

### More details
 {#MoreDetails}

We discuss in a bit more detail the central idea of holography, roughly for the case of Chern-Simons type theories and making some simplifications, but giving a precise statement.

Consider some $n$-dimensional [[FQFT]] $Z_B$ and assume that that spaces of states that it assigns to any $(n-1)$-dimensional manifold $X$ are of finite [[dimension]] (over some ground field $\mathbb{C}$):

$$
  dim Z_B(X) \lt \infty
  \,.
$$

Then for $\Sigma : \partial_{in}{\Sigma} \to \partial_{out}{\Sigma}$ any [[cobordism]] of dimension $n$, the [[correlator]]

$$
  Z_B(\Sigma) : Z_B(\partial_{in} \Sigma) \to Z_B(\partial_{out} \Sigma)
$$

that $Z_B$ assigns may naturally be identified, under the [[closed monoidal category|closed monoidal structure]] of [[Vect]], as an element 

$$
  \begin{aligned}
  \overline{Z_B(\Sigma)} 
  & \in 
  Z_B(\partial_{in} \Sigma)^{*} \otimes Z_B(\partial_{out} \Sigma)
   \\
   & \simeq
   Z_B(\partial \Sigma)
  \end{aligned}
  \,.
$$

Stated differently: the vector space $Z_B(\partial \Sigma)$ is the space of all "potential correlators" of $Z_B$ and $\overline{Z_B(\Sigma)}$ is the particular one chosen by the given model. 

If $Z_B$ is really a [[CFT]] one calls a subspace $Bl_B(\Sigma) \subset Z(\partial\Sigma)$ of elements that respect conformal invariance in a certain way the space of _[[conformal block]]s_ and calls the assignment $\Sigma \mapsto Bl_B(\sigma)$ the [[modular functor]] of the model.

Notice that by looking at all "potential correlators" this way we are suddenly assigning vector spaces in codimension 0 (on $\Sigma$), even though the axioms of an [[FQFT]] a priori only mention vector spaces (of states) assigned in codimension 1. Given all these spaces of "[[conformal block]]s", the (re)construction of $Z_B$ consists of choosing inside each $Bl_B(\Sigma)$ the actual correlator $\overline{Z_B(\Sigma)}$ (this way of looking at [[TQFT]]s $B$ is actually the way in which [Atiyah]() originally formuated the axioms of [[FQFT]]).

But since we are dealing now with vector spaces assigned to $n$-dimensional $\Sigma$, we can ask the following question:

is there an $(n+1)$-dimensional [[extended TQFT]] $A$ such that

1. there is an [[isomorphism]]

   $$
     Z_A(\Sigma) \simeq Z_B(\partial \Sigma) = Bl_B(\Sigma)
   $$

1. such that whenever $\hat \Sigma$ cobounds $\Sigma$ the linear map

$$
  Z_A : \mathbb{C} = Z_A(\hat \Sigma)
 \stackrel{Z_A(\hat \Sigma)}{\to}
  Z_A(\partial \hat \Sigma)
  \simeq
  Bl_B(\Sigma)
$$

sends $1 \in \mathbb{C}$ to $\overline{Z_B(\Sigma)}$.

If so, we say that $A$ is a **holographic dual** to $B$.

Notice that $Z_A(\Sigma)$ is the space of **[[state]]s** of $A$ over $\Sigma$, while $Bl_B(\Sigma)$ is the space of possible **[[correlator]]s** of $B$ over $\Sigma$. Under holography, the states of $A$ are identified with the correlators of $B$.

## Examples
 {#Examples}

### Of higher Chern-Simons/CFT-type

#### RT-3d TQFT / rational 2d CFT

The class of examples of "Chern-Simons-type holography" we mention now has fairly completely and rigorously been understood. It is in turn a special and comparatively simple (but far from trivial) case of the historically earliest class of examples: [ordinary Chern-Simons theory dual to a 2d WZW model](OrdinaryCSWZWModel) below.

Given any [[modular tensor category]] $C$ the [[Reshetikhin-Turaev construction]] procides a 3-dimensional [[TQFT]] $Z_C$. It space of states over a 2-dimensional surface can be identified (after some work) with a space of [[conformal block]]s for a [[WZW-model]]-liked $2d$ CFT. The [[FRS formalism]] provides a way to show that the states of $Z_C$ provides [[correlators]] that solve the [[sewing constraint]]s.



#### Ordinary Chern-Simons theory / WZW-model
 {#OrdinaryCSWZWModel}

Ordinary 3-dimensional [[Chern-Simons theory]] for a group $G$ is holographically dual to the 2-dimensional [[WZW-model]].

#### Poisson $\sigma$-model / quantum mechanics

Ordinary [[quantum mechanics]] induced by [[quantization]] of a [[Poisson manifold]] -- which may be regarded as a 1-dimensional QFT -- is holographically dual to the 2-dimensional [[Poisson sigma-model]] 
(implicitly observed by ([Kontsevich](#Kontsevich)) made explicit by ([CattaneoFelder](#CattaneoFelder)).

(Notice the [[Poisson sigma-model]] is the $(n = 2)$-case of the [[AKSZ sigma-model]] which is indeed an example of a [[schreiber:infinity-Chern-Simons theory]], as discussed there.)

#### A-model / quantum mechanics

Similarly the [[A-model]] on certain [[D-brane]]s gives a holographic description of ordinary [[quantum mechanics]]. ([Witten](#WittenAModel)).

See

* [[quantization via the A-model]]

Notice that the A-model arises from the [[Poisson sigma-model]], as discussed there.



#### Higher dimensional Chern-Simons theory / Self-dual higher gauge theory
 {#HigherDimCSAndSelfDualQFT}

##### Idea and examples

Generally, [[higher dimensional Chern-Simons theory]]
in dimension $4k+3$ (for $k \in \mathbb{N}$) is holographically related to [[self-dual higher gauge theory]] in dimension $4k+2$ (at least in the abelian case). 

* $(k=0)$: ordinary 3-dimensional [[Chern-Simons theory]] is related to a [[string]] [[sigma-model]] on its boundary;

* $(k=1)$: 7-dimensional Chern-Simons theory is related to a [[fivebrane]] model on its boundary;

* $(k=2)$: 11-dimensional Chern-Simons theory is related to a parts of a [[type II string theory]] on its bounday (or that of the space-filling 9-[[brane]], if one wishes) ([BelovMoore](#BelovMoore)).


##### Some details

We indicate why [[higher dimensional Chern-Simons theory]] is -- if holographically related to anything -- holographically related to [[self-dual higher gauge theory]].

The [[phase space]] of [[higher dimensional Chern-Simons theory]] in [[dimension]] $4k+3$ on $\Sigma \times \mathbb{R}$ can be identified with the space of [[curvature|flat]] $2k+1$-forms on $\Sigma$. The [[presymplectic form]] on this space is given by the pairing

$$
  (\delta B_1, \delta B_2) \mapsto
  \int_\Sigma \delta B_1 \wedge \delta B_2
  \,.
$$

The [[geometric quantization]] of the theory requires that we choose a polarization of the [[complexification]] of this space (split the space of forms into "coordinates" and their "canonical momenta"). 

One way to achieve this is to choose a [[conformal structure]] on $\Sigma$. The corresponding [[Hodge star operator]]

$$
  \star : \Omega^{2k+1}(\Sigma) \to \Omega^{2k+1}(\Sigma)
$$

provides the polarization by splitting into self-dual and anti-self-dual forms: 

notice that (by the formulas at [[Hodge star operator]]) we have on mid-dimensional forms

$$
  \star \star B = (-1)^{(2k+1)(4k+3)} B
  = - B
  \,.
$$

Therefore it provides a [[complex structure]] on $\Omega^{2k+1}(\Sigma) \otimes \mathbb{C}$.

We see that the symplectic structure on the space of forms can equivalently be rewritten as

$$
  \begin{aligned}
    \int_X B_1 \wedge B_2
    & = - \int_X B_1 \wedge \star \star B_2 
  \end{aligned}
  \,.
$$

Here on the right now the [[Hodge star operator|Hodge inner product]] of $B_1$ with $\star B_2$ appears, which is invariant under applying the Hodge star to both arguments.

We then decompose $\Omega^{2k+1}(\Sigma)$ into the $\pm i$-[[eigenspace]]s of $\star$: say $B \in \Omega^{2k+1}(\Sigma)$ is  _imaginary self-dual_ if

$$
  \star B = i B
$$

and _imaginary anti-self-dual_ if

$$
  \star B = - i B
  \,.
$$

Then for imaginary self-dual $B_1$ and $B_2$ we find that the symplectic pairing is

$$
  \begin{aligned}
    (B_1, B_2)
    &=
    -i \int_X B_1 \wedge \star B_2
    \\
    & =
    -i \int_X (\star B_1) \wedge \star (\star B_2)
    \\
    & =    
    +i \int_X B_1 \wedge \star B_2
  \end{aligned} 
  \,.
$$

Therefore indeed the symplectic pairing vanishes on the self-dual and on the anti-selfdual forms. Evidently these provide a decomposition into [[Lagrangian subspace]]s.


Therefore a [[state]] of higher Chern-Simons theory on $\Sigma$ may locally be thought of as a function of the self-dual forms on $\Sigma$. Under holography this is (therefore) identified with the [[correlator]] of a [[self-dual higher gauge theory]] on $\Sigma$.



### Of AdS gravity/CFT-type


#### Type II on $AdS_5 \times S^5$ and $d = 4$ super Yang-Mills
 {#SYMAds5}

Conjecturally, [[type II string theory]] on a [[anti-de Sitter space]] background is holographically dual to [[super Yang-Mills theory]] on the asymptotic boundary.

See [[AdS/CFT correspondence]].

#### M-theory on $AdS_7 \times S_4$ and 6d $(2,0)$-SCFT on M5 branes
 {#6dAdS7}

[[11-dimensional supergravity|M-theory]] on $AdS_7 \times S^4$ is supposed to have as holographic boundary the [[6d (2,0)-superconformal QFT]]. See there for references.

#### M-theory on $AdS_4 \times S^7/\mathbb{Z}_k$ and Chern-Simons on M2 branes

See [[ABJM theory]].



## Related concepts

* [[holographic principle of higher category theory]]


## References

### General

The idea of the holographic principle originates in

* [[Gerard 't Hooft]], _Dimensional Reduction in Quantum Gravity_  ([gr-qc/9310026](http://arxiv.org/abs/gr-qc/9310026)).

* [[Leonard Susskind]], _The World as a hologram_ , J. Math. Phys. 36 (1995) 6377&#8211;6396, ([hep-th/9409089](http://arxiv.org/abs/hep-th/9409089))

A review is

* R. Bousso, _The holographic principle_, Rev. Mod. Phys. __74__ (2002) 825-874, ([MR2003m:83048](http://www.ams.org/mathscinet-getitem?mr=1925130), [doi](http://link.aps.org/doi/10.1103/RevModPhys.74.825), [arXiv:hep-th/0203101](http://arxiv.org/abs/hep-th/0203101))

### AdS/CFT

See the references at [[AdS/CFT correspondence]].

### Chern-Simons / CFT

#### RT-TQFT and rational 2d CFT

An exhaustive list of references should be at _[[FRS formalism]]_ . One article that contains a survey of much of the story is 

* Jens Fjelstad, J&#252;rgen Fuchs, [[Ingo Runkel]], [[Christoph Schweigert]], _Uniqueness of open/closed rational CFT with given algebra of open states_ ([arXiv:hep-th/0612306](http://arxiv.org/abs/hep-th/0612306)) .

Amplification of how the [[FRS formalism]] is inevitable once one adopts holography and [[QFT with defects]] is in 

* [[Anton Kapustin]], [[Natalia Saulina]], _Surface operators in 3d TFT and 2d Rational CFT_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ AMS, 2011

#### Self-dual higher gauge fields and higher abelian Chern-Simons

The idea of describing [[self-dual higher gauge theory]] by abelian Chern-Simons theory in one dimension higher originates in 

* [[Edward Witten]], _Five-brane effective action in M-Theory_, J. Geom. Phys. __22__ (1997), no. 2, 103&#8211;133, [hep-th/9610234](http://arxiv.org/abs/hep-th/9610234)

* [[Edward Witten]], _Duality relations among topological effects in string theory_, J. High Energy Phys. 2000, no. 5, Paper 31, 31 pp. [arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086), [doi](http://dx.doi.org/10.1088/1126-6708/2000/05/031)

More discussion of the general principle is in 

* Dmitriy Belov, [[Greg Moore]], _Holographic action for the self-dual field_, [arXiv:hep-th/0605038](http://arxiv.org/abs/hep-th/0605038)
 {#BelovMoore}

A quick exposition of the basic idea is in

* [[Jacques Distler]], _Actions for self-dual gauge fields_ ([blog](http://golem.ph.utexas.edu/~distler/blog/archives/000809.html))

The application of this to the description of type II [[string theory]] in 10-dimensions to 11-dimensional Chern-Simons theory is in the followup 

* Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv](http://arxiv.org/abs/hep-th/0611020))

#### Poisson $\sigma$-model/A-model and quantum mechanics

* [[Maxim Kontsevich]], ...
 {#Kontsevich}

* [[Alberto Cattaneo]], [[Giovanni Felder]], ...
 {#CattaneoFelder}

* [[Edward Witten]], ...
 {#WittenAModel}

#### 3d Chern-Simons theory / 2d CFT

3-dimensional [[Chern-Simons theory]] in the context of holography is discussed for instance in

* Victor O. Rivelles, _Holographic Principle and AdS/CFT Correspondence_ ([arXiv](http://arxiv.org/abs/hep-th/9912139))

#### Chern-Simons/CFT in AdS/CFT

In

* [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 
 {#Witten98}

it is argued that in the [[AdS/CFT correspondence]] it is in fact just the Chern-Simon terms inside the corresponding [[supergravity]] theories whose states control the [[conformal block]]s of the dual [[CFT]]. So the CS/CFT correspondence is a part (a crucial part) of the AdS/CFT correspondence, at least for $AdS_5/CFT_4$ and $AdS_7/CFT_6$.


### General abstract formulation

An identification of boundary conditions and [[QFT with defects|defects]] as [[natural transformation]]s between higher dimensional [[FQFT]]s is discussed in

* [[Chris Schommer-Pries]], _Topological defects and classifying local topological field theories in low dimension_ ([[SchommerPriesDefects.pdf:file]])
{#SchommerPries}

See [[holographic principle of higher category theory]] for more on this.

[[!redirects holographic duality]]

[[!redirects holography]]