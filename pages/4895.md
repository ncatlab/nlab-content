
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[quantum field theory]] what has come to be known as the _holographic principle_ is the fact that the [[correlators]]/[[partition functions]] of some [[quantum field theories]] of [[dimension]] $n$ may be identified with [[states]] of a [[TQFT]] of dimension $n + 1$.

[[!include holographic principle -- table]]

### Some details


Notice that for $\Sigma$ an $(n+1)$-dimensional manifold with $n$-dimensional [[boundary]] $\partial \Sigma$, regarded as a [[cobordism]] $\Sigma : \emptyset \to \partial \Sigma$, an $(n+1)$-dimensional TQFT assigns a morphism

$$
  Z(\Sigma) : 1 \to Z(\partial \Sigma)
  \,,
$$

hence an element of the space $Z(\partial \Sigma)$. Under holography, this element is identified with the [[partition function]] of an $n$-dimensional QFT evaluated on the manifold (without boundary) $\partial \Sigma$.

The idea that some systems in physics are governed by other systems "localized at a boundary" in this kind of way was originally suggested by the behaviour of [[black holes]] in [[general relativity]]: their [[black hole entropy]] is proportional to their "surface", as reflected by the [[generalized second law of thermodynamics]]. This made [[Gerard 't Hooft]] suggest a general principle, called the _holographic principle_, which however remained somewhat vague ([t'Hooft 93](#tHooft93), [Susskind 94](#Susskind94)).

Later, two more precise classes of correspondences were identified, that are regarded now as precise examples of the general idea of the holographic principle:

1. Systems of [[Chern-Simons theory]] and [[higher dimensional Chern-Simons theory]] can be shown explicitly to have spaces of states that are canonically identified with correlator spaces of [[CFT]]s ([[conformal block]]s) and [[self-dual higher gauge theory]] on their boundary. 

   (The relation of traditional 3d [[Chern-Simons theory]] to the 2d [[WZW model]] originates in ([Witten 89](#Witten89)) and hence precedes the proposal of ([t'Hooft 93](#tHooft93), [Susskind 94](#Susskind94)), but this relation was not recognized from this perspective earlier.)

1. Systems of [[quantum gravity]] in various dimensions as given by [[string theory]] on asymptotically [[anti de Sitter spacetime]]s have been checked not in total but in a multitude of special aspects in special cases to be dual to [[supersymmetric]] [[CFT]]s on their asymptotic boundary -- this is called [[AdS/CFT correspondence]].


+-- {: .num_remark}
###### Remark

In view of these two classes of examples it is maybe noteworthy that one can see that also closed [[string field theory]], which is supposed to be one side of the [[AdS/CFT correspondence]], has the form of an [[schreiber:infinity-Chern-Simons theory]], as discussed there, for the [[L-infinity algebra]] of closed string correlators. So maybe the above two different realizations of the holographic principle are really aspects of one single mechanism for $\infty$-Chern-Simons theory. 

Evidence for this also comes from the details of the AdS/CFT mechanism. In ([Witten98](#Witten98)) it is discussed how the [SYM/IIB duality](#SYMAds5) is carried by the Chern-Simons term $\int B_{NS} \wedge d B_{RR}$ in the [[type II string theory]] action, the [6d(2,0)/AdS7 duality](#6dAdS7) - is induced by the Chern-Simons term $\int C_3 \wedge d C_3 \wedge d C_3$ of the [[11-dimensional supergravity]] action. 

=--

Below at _[Examples](Examples)_ we list some systems for which something along these lines is known.

### More details
 {#MoreDetails}

We discuss in a bit more detail the central idea of holography, roughly for the case of Chern-Simons type theories and making some simplifications, but giving a precise statement.

The general idea is that [[field (physics)|fields]] $\phi$ in the bulk theory are identified with [[source fields]] in the [[correlation functions]] of the boundary theory. 

The archetypical example is the relation between the [[correlators]] of the [[WZW model]] on a [[Lie group]] $G$ with the [[space of quantum states]] of 3d $G$-[[Chern-Simons theory]], as reviewed for instance on page 30 of ([Gaw&#281;dzki 99](#Gawedzki99)):

a [[correlator]] for the WZW model with source field $A$ has to satisfy a conformal transformation property called a [[Ward identity]]. The space of all suitable functionals satisfying these identities is the space of [[conformal blocks]]. That space is equivalently identified with the space of [[wave functions]] of Chern-Simons theory depending on the fields $A$, hence the quantum states of the CS theory. 

More generally, consider some $n$-dimensional [[FQFT]] $Z_B$ and assume that the [[spaces of states]] that it assigns to any $(n-1)$-dimensional manifold $X$ are of finite [[dimension]] (over some ground field $\mathbb{C}$):

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

If $Z_B$ is really a [[CFT]] one calls a subspace $Bl_B(\Sigma) \subset Z(\partial\Sigma)$ of elements that respect conformal invariance in a certain way the space of _[[conformal block]]s_ and calls the assignment $\Sigma \mapsto Bl_B(\Sigma)$ the [[modular functor]] of the model.

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

### Poisson holography
 {#PoissonHolography}


One of the key statements of the holographic principle is that
[[field (physics)|fields]] of a [[bulk field theory]] correspond to [[sources]] in its [[boundary field theory]].

One set-up where this can be made a formal [[theorem]] is for [[2d Chern-Simons theory]] which is a [[non-perturbative field theory|non-perturbative]] [[Poisson sigma-model]]. This theorem is discussed at 

* _[off-shell Poisson bracket -- boundary field theory interpretation](http://ncatlab.org/nlab/show/off-shell+Poisson+bracket#BoundaryFieldTheoryInterpretation)_.

* _[motivic quantization -- Poisson holography](motivic+quantization#PoissonHolography)_.

### Holography of higher Chern-Simons/CFT-type
 {#3dCS-2dCFT}

See also _[[AdS3-CFT2 and CS-WZW correspondence]]_.

#### RT-3d TQFT / rational 2d CFT

The class of examples of "Chern-Simons-type holography" we mention now has fairly completely and rigorously been understood. It is in turn a special and comparatively simple (but far from trivial) case of the historically earliest class of examples: [ordinary Chern-Simons theory dual to a 2d WZW model](#OrdinaryCSWZWModel) below.

For more see at _[[AdS3-CFT2 and CS-WZW correspondence]]_.

Given any [[modular tensor category]] $C$ the [[Reshetikhin-Turaev construction]] produces a 3-dimensional [[TQFT]] $Z_C$. Its space of states over a 2-dimensional surface can be identified (after some work) with a space of [[conformal block]]s for a [[WZW-model]]-liked $2d$ CFT. The [[FRS formalism]] provides a way to show that the states of $Z_C$ provides [[correlators]] that solve the [[sewing constraints]].



#### Ordinary Chern-Simons theory / WZW-model
 {#OrdinaryCSWZWModel}

For a given [[Lie group]] $G$, ordinary 3-dimensional $G$-[[Chern-Simons theory]] for a group $G$ is holographically dual to the 2-dimensional [[WZW-model]] describing the [[string]] propagating on $G$.

Here is a list with aspects of this correspondence:

1. At the level of [[action functionals]] the relation is directly seen by observing that on a 3-d [[manifold with boundary]] the [[Chern-Simons theory]] action is not gauge invariant, but has a boundary term depending on the gauge transformation. Since the gauge transformation is a function on the 2d boundary with values in $G$, this boundary term is like an action functional for a [[sigma-model]] with [[target space]] $G$, and indeed it is that (subject to some fine-tuning) of the $G$-[[WZW model]].

   A random source reviewing this is for instance ([Arcioni-Blau-Loughlin, p. 6](#ArcioniBlauLoughlin)).

1. More abstractly, at least for simply connected compact $G$, the action functionals are also related by [[transgression]] of [[moduli stacks]] as discussed at _[[schreiber:infinity-Chern-Simons theory]]_. The action functional of $G$-Chern-Simons theory is induced by the morphism 

   $$
     \mathbf{c}_{conn} : \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}
   $$

   from the [[smooth infinity-groupoid|smooth]] [[moduli stack]] of $G$-[[connection on a bundle|bundles with connection]] to the [[smooth infinity-groupoid|smooth]] [[moduli infinity-stack|moduli 3-stack]] of [[circle n-bundle with connection|circle 3-bundles with connection]] (discussed in detail at [[differential string structure]] ) in that for $\Sigma_3$ a compact 3d-dimensional surface the Chern-Simons action is the composite

   $$
     \exp(i S_{CS}(-)) : [\Sigma_3, \mathbf{B} G_{conn}] \stackrel{[\Sigma_3, \mathbf{c}_{conn}]}{\to} [\Sigma_3, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_3}(-))}{\to} U(1)
     \,,
   $$

   where the last morphism is given by [[fiber integration in ordinary differential cohomology]]. 

   Topological term in the WZW-model (the [[B-field]] [[background gauge field]]) is similarly the term appearing in [[codimension]] 2. This is discussed at _[Chern-Simons theory -- Geometric quantization -- In higher codimension](Chern-Simons%20theory#GeometricQuantHigher)_.

1. At the level of matching [[space of states]] of CS-theory with the [[partition function]] of the WZW model this is a computation obtained from the [[geometric quantization]] of the CS-action, originally due to ([Witten](#Witten)). A review is in ([Gawedzki, section 5](#Gawedzki)).

1. If one accepts  that the [[quantization]] of the $G$-Chern-Simons [[action functional]] yields the [[TQFT]] given by the [[Reshetikhin-Turaev construction]] applied to the [[modular tensor category]] of $G$-[[loop group]] representations, then a detailed construction of the correspondence CS-TQFT/WZW-CFT is what the [[FFRS-formalism]] achieves. See there for more details. 


   More comments on the holographic interpretation of this formalism are in ([Kapustin-Saulina](#KapustinSaulina), [Fuchs-Schweigert-Valentino](#FuchsSchweigertValentino)). 



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

* $(k=2)$: 11-dimensional Chern-Simons theory is related to a parts of a [[type II string theory]] on its boundary (or that of the space-filling 9-[[brane]], if one wishes) ([BelovMoore](#BelovMoore)).


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



### Holography of AdS gravity/CFT-type


#### Type II on $AdS_5 \times S^5$ and $d = 4$ super Yang-Mills
 {#SYMAds5}

Conjecturally, [[type II string theory]] on a [[anti-de Sitter space]] background is holographically dual to [[super Yang-Mills theory]] on the asymptotic boundary.

See [[AdS/CFT correspondence]].

#### M-theory on $AdS_7 \times S^4$ and 6d $(2,0)$-SCFT on M5 branes
 {#6dAdS7}

[[11-dimensional supergravity|M-theory]] on $AdS_7 \times S^4$ is supposed to have as holographic boundary the [[6d (2,0)-superconformal QFT]]. See there for references.

#### M-theory on $AdS_4 \times S^7/\mathbb{Z}_k$ and Chern-Simons on M2 branes

See [[ABJM theory]].



## Related concepts

* [[holographic entanglement entropy]]

* [[holographic principle of higher category theory]]

* [[firewall problem]]

## References

### General

The idea of the holographic principle originates in

* [[Gerard 't Hooft]], _Dimensional Reduction in Quantum Gravity_  ([gr-qc/9310026](http://arxiv.org/abs/gr-qc/9310026)).
 {#tHooft93}

* [[Leonard Susskind]], _The World as a hologram_ , J. Math. Phys. 36 (1995) 6377&#8211;6396, ([hep-th/9409089](http://arxiv.org/abs/hep-th/9409089))
 {#Susskind94}

A review is

* R. Bousso, _The holographic principle_, Rev. Mod. Phys. __74__ (2002) 825-874, ([MR2003m:83048](http://www.ams.org/mathscinet-getitem?mr=1925130), [doi](http://link.aps.org/doi/10.1103/RevModPhys.74.825), [arXiv:hep-th/0203101](http://arxiv.org/abs/hep-th/0203101))

See also

* [Oxford Holography Group](http://www-thphys.physics.ox.ac.uk/people/AndreiStarinets/oxford_holography_group/holography_seminar/group_members.html), _[Background material for holography](http://www-thphys.physics.ox.ac.uk/people/AndreiStarinets/oxford_holography_group/holography_seminar/material.html)_

### AdS/CFT

See the references at [[AdS/CFT correspondence]].

### Chern-Simons / CFT
 {#ReferencesCS-CFT}

#### On the level of action functionals

The identification of the [[space of quantum states]] of 3d $G$-[[Chern-Simons theory]] with the space of [[conformal blocks]] of the [[WZW model]] on $G$ is due to 

* [[Edward Witten]] _Quantum Field Theory and the Jones Polynomial_ Commun. Math. Phys. 121 (3) (1989) 351&#8211;399. MR0990772 ([EUCLID](http://projecteuclid.org/euclid.cmp/1104178138))
 {#Witten89}


A review of the standard holographic relation between 3d $G$-[[Chern-Simons theory]] and the [[WZW model]] on $G$ is for instance around p. 30 of

* [[Krzysztof Gawędzki]], _Conformal field theory: a case study_ ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))
 {#Gawedzki99}


Discussion of how [[gauge transformations]] of the [[action functional]] of [[Chern-Simons theory]] reproduce overe [[boundaries]] the action functional of the [[WZW model]] are for instance on p. 6 of

* Giovanni Arcioni, [[Matthias Blau]], Martin O'Loughlin, _On the boundary dynamics of Chern-Simons gravity_ ([arXiv:0210089](http://arxiv.org/abs/hep-th/0210089))
 {#ArcioniBlauLoughlin}

(And many other references. )

#### Matching of spaces of states to conformal blocks

The observation that the [[space of states]] in the [[geometric quantization]] of 3d [[Chern-Simons theory]] matches with the [[partition function]] of the [[WZW model]] is originally due to 

* [[Edward Witten]] _Quantum Field Theory and the Jones Polynomial_ Commun. Math. Phys. 121 (3) (1989) 351&#8211;399. MR0990772 ([project EUCLID](http://projecteuclid.org/euclid.cmp/1104178138))
 {#Witten}

A review is in section 5 of 

* [[Krzysztof Gawedzki]], _Conformal field theory: a case study_  ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))
 {#Gawedzki}

#### Reshetikhin-Turaev 3d TQFT and rational 2d CFT
 {#RTAnd2dCFT}


Using the hypothesized relation between $G$-Chern-Simons [[TQFT]] to that given by the [[Reshetikhin-Turaev construction]] applied to the [[modular tensor category]] of $G$-[[loop group]] representations, a detailed discussion of the relation CS/WZW in given by the [[FFRS formalism]]. See there for more details

One article that contains a survey of much of the story is 

* Jens Fjelstad, J&#252;rgen Fuchs, [[Ingo Runkel]], [[Christoph Schweigert]], _Uniqueness of open/closed rational CFT with given algebra of open states_ ([arXiv:hep-th/0612306](http://arxiv.org/abs/hep-th/0612306)) .

The isomorphism between the RT-theory modular functor and the CFT conformal blocks is also discussed in 

* {#AndersenUeno} [[Jørgen Andersen]], [[Kenji Ueno]], _Construction of the Reshetikhin-Turaev TQFT from conformal field theory_ ([arXiv:1110.5027](http://arxiv.org/abs/1110.5027))
 

Amplification of how the [[FRS formalism]] is inevitable once one adopts holography and [[QFT with defects]] is in 

* [[Anton Kapustin]], [[Natalia Saulina]], _Surface operators in 3d TFT and 2d Rational CFT_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ AMS, 2011
 {#KapustinSaulina}

More along these lines is in

* [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Alessandro Valentino]], _Bicategories for boundary conditions and for surface defects in 3-d TFT_ ([arXiv:1203.4568](http://arxiv.org/abs/1203.4568))
 {#FuchsSchweigertValentino}

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

### Black hole / CFT correspondence

* Monica Guica, Thomas Hartman, Wei Song, [[Andrew Strominger]], _The Kerr/CFT Correspondence_ ([arXiv:0809.4266](http://arxiv.org/abs/0809.4266))

* Alejandra Castro, Alexander Maloney, [[Andrew Strominger]], _Hidden Conformal Symmetry of the Kerr Black Hole_ ([arXiv:1004.0996](http://arxiv.org/abs/1004.0996))

### General abstract formulation

An identification of boundary conditions and [[QFT with defects|defects]] as [[natural transformation]]s between higher dimensional [[FQFT]]s is discussed in

* [[Chris Schommer-Pries]], _Topological defects and classifying local topological field theories in low dimension_ ([[SchommerPriesDefects.pdf:file]])
{#SchommerPries}

See [[holographic principle of higher category theory]] for more on this.

Further discussion of formalization in [[extended TQFT]] is in 

* [[Dan Freed]], _[[4-3-2 8-7-6]]_, talk at _[ASPECTS of Topology](https://people.maths.ox.ac.uk/tillmann/ASPECTS.html)_ Dec 2012


[[!redirects holographic duality]]

[[!redirects holography]]
[[!redirects holographic dual]]
[[!redirects holographic duals]]