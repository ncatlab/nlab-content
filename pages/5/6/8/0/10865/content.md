
> In ([Lawvere 67](#Lawvere67), [Lawvere 79](#Lawvere79)) is proposed a notion of _[[toposes of laws of motion]]_ meant to formalize [[classical mechanics|classical]] [[continuum mechanics]] in [[synthetic differential geometry]]/in [[topos theory]]. This page gives an introductory survey of the refinements possible when lifting from [[topos theory]] to [[(infinity,1)-topos theory|higher topos theory]].

> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Introduction and motivation

Urban legend has it that there was a time when only three people understood [[Einstein]]'s [[theory (physics)|theory]] of [[classical field theory|classical]] [[gravity]] -- "[[general relativity]]". 

Whether true or not, one of the three was [[David Hilbert]]. He made sure every beginning student today can understand [[general relativity]], he did so by giving it a clear and precise (= rigorous) formalization in [[mathematics]]:

classical Einstein gravity is simply the study of the [[critical points]] of the [[integral]] of the [[scalar curvature]] [[density]] [[action functional|functional]] on the [[moduli space]] of [[pseudo-Riemannian metrics]] on [[spacetime]].

By realizing this mathematical formalization of what [[Einstein]] did, [[Hilbert]] was able to essentially scoop him, that's why this functional is now called the _[[Einstein-Hilbert action functional]]_.

To promote this success, in his famous list of [[Hilbert's problems]] in mathematics, from 1900, [[Hilbert's 6th problem]] asks [[mathematics|mathematicians]] generally to find [[axioms]] for [[theory (physics)|theories]] in [[physics]]. 

Since then a list of such axiomatizations has been found, for instance

| [[physics]] | [[mathematics]] |
|--|--|
| [[mechanics]] | [[symplectic geometry]] |
| [[gravity]] | [[Riemannian geometry]] |
| [[gauge theory]] | [[Chern-Weil theory]] |
| [[quantum mechanics]] | [[operator algebra]] |
| [[TFT|topological]] [[local quantum field theory]] | [[monoidal (∞,n)-category]] theory |
| $\vdots$ | $\vdots$ |

Two aspects of this list are noteworthy: one the one hand, it contains crown jewels of mathematics, on the other the items appear unrelated and piecemeal.

As a student, [[William Lawvere]] was exposed to the proposal to axiomatize [[thermodynamics]] as what was called "[[rational thermodynamics]]". He realized that a fundamental [[foundation]] of such [[continuum physics]] first of all requires a good foundation of [[differential geometry]] itself. 
Looking over his life publication record (see [[William Lawvere|here]]) one sees that he pursued the following grand plan.

**Plan.**

1. lay the [[foundations]] of [[mathematics]] in [[topos theory]] ("[[ETCS]]")

1. lay the foundations of [[geometry]] in [[topos theory]] ([[synthetic differential geometry]], [[cohesion]])

1. lay the foundations of [[classical mechanics|classical]] [[continuum physics]] in [[synthetic differential geometry]] ([[toposes of laws of motion]]).

Lawvere became famous for his groundbreaking contributions to the first two items ([[categorical logic]], [[topos theory|elementary topos theory]], [[algebraic theories]], [[synthetic differential geometry|SDG]]). For some reason the motivation of all this by the third item is not as widely recognized, even thought Lawvere continuously emphasized this third point, see the [list of quotations here](William%20Lawvere#MotivationFromFoundationsOfPhysics).

Grandiose as this plan is, we have to note that in the above form it falls short in each item, by modern standards:

1. modern [[mathematics]] is naturally founded not in [[topos theory]]/[[type theory]], but in [[(infinity,1)-topos theory|higher topos theory]]/[[homotopy type theory]].

1. modern [[geometry]] is not just about "variable sets" ([[sheaves]]) but is [[higher geometry]] about "variable [[homotopy types]]",  "[[geometric homotopy types]]", "[[infinity-stack|higher stacks]]";

1. modern [[physics]] goes beyond [[classical mechanics|classical]] [[continuum physics]]; at high [[energy]] (small distance) classical physics is refined by [[quantum physics]], specifically by [[quantum field theory]].


Therefore what is needed is a foundation of [[high energy physics]] in [[higher differential geometry]] formulated in [[higher topos theory]].

In the following we illustrate three aspects of such a refined theory, following ([dcct](#dcct), [sythQFT](#syntheticQFT)). We close by indicating how this theory serves to solve subtle open problems in modern [[quantum field theory]] and [[string theory]].


## **I)** Mapping spaces in gauge theory and General covariance 
 {#HigherMappingSpaces}

One basic point emphasized in ([Lawvere 67](#Lawvere67)) is that central to the formulation of [[physics]] is the existence of _[[mapping spaces]]_ which satisfy the [[exponential law]]. 

(notice: [[mapping space]] ... space of [[trajectories]] ... [[path integral]])

Indeed, generically a [[physical system]] is specified by

* a [[space]] $\Sigma$ called _[[spacetime]]_ or _[[worldvolume]]_;

* a [[space]] $X$ called _[[target space]]_ or _[[field bundle]]_ or _[[moduli space]] of [[field (physics)|fields]]_.

such that a _[[trajectory]]_ or _history_ of [[physical field|field configurations]] is a [[map]]

$$
  \Sigma \longrightarrow X
  \,.
$$

For instance for $\Sigma = \mathbb{R}$ the abstract [[worldline]] and $X$ [[spacetime]], then $\Sigma \to X$ may be taken to be the [[trajectory]] of a [[particle]] in [[spacetime]].

Hence the [[mapping space]] $[\Sigma,X]$ is the space of all [[trajectories]] (the _[[path space]]_, famous as the [[domain]] of the infamous _[[path integral]]_).

Lawvere observed that this not only needs to exist as a decent "space", it also needs to satisfy the axiom of an [[cartesian closed category|cartesian]] [[internal hom]]. Because if we consider a split

$$
  \Sigma \coloneqq \mathbb{R} \times \Sigma_{d-1}
$$

into [[time]] and [[space]], then we want that spacetime field configurations

$$
  \mathbb{R} \times \Sigma_{d-1} \longrightarrow X
$$

are equivalently trajectories of fields on space

$$
  \mathbb{R}  \longrightarrow [\Sigma_{d-1}, X]
$$

and also equivalently a collection of field trajectories for each point of space

$$
  \Sigma_{d-1}  \longrightarrow [\mathbb{R}, X]
  \,.
$$


This led Lawvere to recognize that physics ([[prequantum field theory|prequantum physics]], to be precise) is to be formulated in a [[cartesian closed category]], such as a [[topos]].

The [[category]] $SmthMfd$ of [[smooth manifolds]] is too small to accomplish this. But the [[category of sheaves]] $Sh(SmthMdf)$ on the [[site]] of smooth manifolds is the canonical improvement. Objects in here include [[smooth manifolds]], also [[diffeological spaces]] and generall [[smooth spaces]]. 

Better still, there is the [[category of sheaves]] $Sh(FSmthMfd)$ on the site of  [[formal smooth manifolds]] -- known as the _[[Cahiers topos]]_ . This also contains [[infinitesimal objects]] and indeed interprets the [[axioms]] of [[synthetic differential geometry]]. 

But actually in modern physics one needs a bit more than this. Physics is fundamentally governed by [[gauge equivalence]], which means that there is no sense in askking if [[field (physics)|field]] configurations are equal, we must ask if they are [[equivalence|equivalent]].

A fundamental example of this is [[Einstein]]'s notion of _[[general covariance]]_. This says that if 

$$
  s \;\colon\; U \hookrightarrow \Sigma
$$

is a region in [[spacetime]], and $\phi \colon \Sigma \stackrel{\simeq}{\longrightarrow} \Sigma$ is a [[diffeomorphism]] acting on spacetime, then the "translated region"

$$
  \phi^\ast s \;\colon\; U \hookrightarrow \Sigma \stackrel{\simeq}{\longrightarrow} \Sigma
$$

is "the same", for all physical purposes. Stated this way in ordinary [[topos theory]] this is confusing, and historically it was confusing: this confusion is essentially what is known as the "[[hole paradox]]".

This apparent [[paradox]] is resolved in [[higher topos theory]]. Here a [[space]] $S$ has internal symmetries, it is a _[[groupoid]]_, a _[[homotopy type]]_. This means that it is not sensible to ask if two maps into it are equal, but between any two maps there is a space of equivalences between them.

For [[general covariance]] this means by the above that spacetime is not actually the spacetime [[manifold]] $\Sigma$, but is the [[action groupoid]]/[[quotient stack]]

$$
  \Sigma//Diff(\Sigma)
$$

of $\Sigma$ by its [[diffeomorphism group]] (regarded as a [[diffeological group]]). By the very definition of "[[stack]]", this $\Sigma//Diff(\Sigma)$ is the thing which is such that maps $U \longrightarrow \Sigma//Diff(\Sigma)$ into it behave jsut as they should as demanded by general covariance. 

This is the formalization of "[[general covariance]]" for regions _inside_ spacetime. The other thing now is general covariance for [[field (physics)|fields]] _on_ spacetime. It turns out that the formalism automatically handles these now:

For notice that the abobve means now that we also need to consider the [[mapping spaces]] refined to  higher topos theory. A fundamental fact is that for $G \in Grp(\mathbf{H})$ [[group object in an (infinity,1)-category|group object]] then the [[slice (infinity,1)-topos|higher slice topos]] over its [[delooping]] is equivalently the collection of [[infinity-action|G-actions]]

$$
  \mathbf{H}_{/\mathbf{B}G} \simeq G Act(\mathbf{H})
  \,.
$$ 

Under this equivalence a [[infinity-action|higher action]] is identified with the universal [[associated infinity-bundle|associated bundle]] which it induces

$$
  \left(
  \array{
    \Sigma &\longrightarrow& \Sigma//Diff(\Sigma)
    \\
    && \downarrow
    \\
    && \mathbf{B}Diff(\Sigma)
  }
  \right)
  \;\;
  \in
  \;\;
  \mathbf{H}_{/\mathbf{B}Diff(\Sigma)}
  \simeq Diff(\Sigma)Act(\mathbf{H})
  \,.
$$

Lawvere also introduced [[categorical logic]] and understood [[dependent product]] $\prod$ and [[dependent sum]] $\sum$ as [[base change]]. In [[(infinity,1)-topos theory|higher topos theory]] this becomes [[representation theory]] as follows:

[[!include homotopy type representation theory -- table]]

Using this we have the mapping space of [[general covariance|covariant]] [[field (physics)|fields]] formed in the [[context]] of $Diff(\Sigma)$-covariance/[[equivariance]]


$$
  \mathbf{B}Diff(\Sigma)
  \;\;
   \vdash
  \;\;
   \left[
     \Sigma//Diff(\Sigma)
     \,,\;
      X
   \right]
$$


**Theorem.** Down in the absolute [[context]], under [[dependent sum]], this is

$$
   \vdash
  \;\;
   \underset{\mathbf{B}Diff(\Sigma)}{\sum}
   \left[
     \Sigma//Diff(\Sigma)
     \,,\;
      X
   \right]
   \;\;
   \simeq
   \;\;
   [\Sigma, X]//Diff(\Sigma)
  \,.
$$

Here $[\Sigma, X]$ is the space of fields on spacetime as one would find it in ordinary topos theory, and $[\Sigma,X]//Diff(\Sigma)$ is its [[homotopy quotient]] by the [[action]] of the [[diffeomorphism group]] by pullback of fields. This is precisely the group of [[gauge equivalences]] on fields in [[general relativity]].

So we obtain a formalization of the famous insight of [[Einstein]], derived by lifting [[Lawvere]]'s argument about [[mapping spaces]] in [[physics]] from [[topos theory]] to [[higher topos theory]].

In a slogan we may conclude, in view of the above table, that in the formalization of [[physics]] in [[(infinity,1)-topos theory|higher topos theory]] we have:

* _[[general covariance]] is homotopy [[coinvariants]]_

in [[mapping spaces]].


## **II)** Toposes of laws of motion and Hamilton-Jacobi-Lagrange mechanics


In ([Lawvere 97](#Lawvere97)) it was observed that [[equations of motion]] in [[physics]] can (almost, see below) be formalized in [[synthetic differential geometry]] as follows.

Let $\mathbf{H}$ be an ambient [[smooth topos|synthetic differential]] [[topos]] (such as the [[Cahiers topos]] of [[smooth spaces]] and [[formal smooth manifolds]]).

The canonical [[line object]] $\mathbb{A}^1 = \mathbb{R}$ of this models the [[continuum]] line, the abstract [[worldline]]. Let

$$
  D \hookrightarrow \mathbb{R}
$$

be the inclusion of the first order [[infinitesimally thickened point|infinitesimal]] neighbourhood of the origin of $\mathbb{R}$ -- in the [[internal logic]] this is $D = \{x \in \mathbb{R}| x^2 = 0\}$, externally it is the [[spectrum of a commutative ring|spectrum]] of the [[ring of dual numbers]] over $\mathbb{R}$.

Then for $X \in \mathbf{H}$ any [[object]] which we are going to think of as a [[configuration space]] of a [[physical system]]. For instance if the system is a [[particle]] propagating on a [[spacetime]], then $X$ is that spacetime. Or $X$ may be the [[phase space]] of the system.

Accordingly the [[mapping space]] $[\mathbb{R}, X] \in \mathbf{H}$ is the [[smooth space|smooth]] [[path space]] of $X$. This is the space of potential [[trajectories]] of the [[physical system]].

If $X$ is thought of as [[phase space]], then every point in there determines a unique [[trajectory]] starting at that point. This means that time evolution is then an [[action]] of $\mathbb{R}$ on $X$. As $X$ here might be any space, we have the collection 

$$
  \mathbb{R}Act(\mathbf{H}) \in Topos
$$ 

of all $\mathbb{R}$-[[actions]] on objects in $\mathbf{H}$. This is again a [[topos]], and hence this is a first version of what one might call a _[[topos of laws of motion]]_.

On the other hand, if we think of $X$ as [[configuration space]], then it is (in the simplest but common case of [[physical systems]]) a [[tangent vector]] in $X$ that determines a [[trajectory]], hence a point in $[D,X]$. There is the canonical projection $[\mathbb{R},X] \longrightarrow [D,X]$ from the smooth [[path space]] to the [[tangent bundle]], which sends each path to its [[tangent vector]]/[[derivative]] at $0 \in \mathbb{R}$. A [[section]] of this map is hence an assignment that sends each tangent vector to a [[trajectory]] which starts out with this tangent. Specifying such a section is hence part of what it means to have [[equations of motion]] in [[physics]]. Accordingly in _[[Toposes of laws of motion]]_ [[Lawvere]] called the collection of such data a Galilian [[topos of laws of motion]].

Of course this is not quite yet what is actually used and needed in physics.  On p. 9 of ([Lawvere 97](#Lawvere97)) this problem is briefly mentioned:

> But what about actual dynamical systems in the spirit of [[Galileo]], for example, second-order ODE's? (Of course, the [[symplectic geometry|symplectic]] or [[Hamiltonian mechanics|Hamiltonian systems]] that are also much studied do address this question of states of [[becoming|Becoming]] versus locations of [[being|Being]], but in a special way which it may not be possible to construe as a topos;

It turns out that it does exist as a "[[higher topos theory|higher topos]]".

In _[[schreiber:Classical field theory via Cohesive homotopy types]]_ it is observed that if $\mathbf{H}$ to be not just a [[topos]] but an [[(infinity,1)-topos|infnity-topos]], then genuine [[classical mechanics]] governed by [[Hamilton's equations]] and [[Hamilton-Jacobi theory]] arises by actions of $\mathbb{R}$ on objects in the [[slice (infinity,1)-topos]] $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$, where $\mathbf{B}U(1)_{conn} \in \mathbf{H}$ is the [[moduli stack]] of [[circle group]]-[[principal connections]]. 


> here goes a brief version of the discussion at _[[prequantized Lagrangian correspondence]]_):

Here $\mathbf{B}U(1)_{conn} \simeq \mathbf{\Omega}^1//U(1)$.


A [[presymplectic form]] on some $X$ is $\omega \;\colon\; X \longrightarrow \mathbf{\Omega}^2$


A [[prequantization]] is

$$
  \array{
    X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}U(1)_{conn}
    \\
    & {}_{\mathllap{\omega}}\searrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    && \mathbf{\Omega}^2
  }
$$

We find

$$
  \mathbb{R}Act\left(
    \mathbf{H}_{/\mathbf{B}U(1)_{conn}}
  \right)
$$

is actually a "topos of laws of motion" in the sense of Hamilton-Lagrange-Jacobi [[classical mechanics]]. For more on this see _[[Higher toposes of laws of motion]]_.






## **III)** Extensive/intensive duality and Cohomological quantization


In [[physics]] and especially in [[continuum mechanics]] and [[thermodynamics]], a physical quantity associated with a [[physical system]] extended in [[space]] is called

* _[[intensive]]_ if it is a [[function]] on (the physical system extended in) space;

* _[[extensive]]_ if it is a [[density]] or [[linear distribution]] on (the physical system extended in) space.

For instance for a [[solid body]] its [[temperature]] is intensive, but its [[mass]] is extensive: there is a temperature assigned to every point of the body (in the idealization of [[classical mechanics|classical]] [[continuum mechanics]] anyway) but a mass is assigned only to every little "extended" piece of the body, not to a single point.

This terminology in [[physics]] apparently originates with [[Richard Tolman]] in 1917.


In ([Lawvere 86](#Lawvere86)) it is amplified that this [[duality]] is generally a fundamental one also in [[mathematics]]: given a [[topos]] $\mathbf{H}$ with a [[commutative ring|commutative]] [[ring object]] $R \in CRing(\mathbf{H})$, then 

* the space of _intensive quantities_ on an [[object]] $X \in \mathbf{H}$ is the [[mapping space]] $[X,R]_{\mathbf{H}} \in CRing(\mathbf{H})$ formed in $\mathbf{H}$;

* the space of _extensive quantities_ on $X$ is the $R$-linear dual, namely the mapping space $[X,R]^\ast \coloneqq [[X,R], R]_{R Mod}$ formed in $R$-[[modules]] in $\mathbf{H}$.

* the [[integration]] map is the canonical [[evaluation]] pairing

  $$
    \int_X \;\colon\; [X,R] \times [X,R]^\ast  \longrightarrow R
    \,.
  $$


Viewed this way, this naturally generalizes to the case where $\mathbf{H}$ is in fact an [[(∞,1)-topos]] and $R \in CRing(\mathbf{H})$ an [[E-∞ ring]]. In this case $[X,R]$ is called the  $R$-[[cohomology]] [[spectrum]] of $X$ and $[X,R]^\ast$ is the corresponding [[generalized homology]] spectrum. In this form intensive and extensive properties appear in [[physics]] in the context of [[motivic quantization]] of [[local prequantum field theory]]. 

More generally, for $\chi$ an $R$-[[(∞,1)-line bundle]] over $X$ then the corresponding extensive object is the $\chi$-twisted [[Thom spectrum]] $R_{\bullet + \chi}(X)$ and the intensive object is the $\chi$-[[twisted cohomology]] [[spectrum]] $R^{\bullet + \chi}(X) = [R_{\bullet+ \chi}(X),R]_{R Mod}$. See at _[[motivic quantization]]_ for how this appears in [[physics]].

In particular ordinary [[quantum mechanics]] is recovered by settin 

$R = $ [[KU]].

([Nuiten 13](#Nuiten13))

The [[monoidal (infinity,1)-category]] $KU Mod$ is the refined ambient home for $Hilb = \mathbb{C} Mod$ (used for [[finite quantum mechanics in terms of dagger-compact categories]]).





## An application -- What is it all good for?


On first sight, formalization of [[physics]] in ([[higher topos theory|higher]]) [[topos theory]] might seem like a fruitless exercise. But indeed on the contrary, it is hardly possible to understand the deep structure of [[quantum field theory]] without such ([[geometric homotopy theory|geometric]]) [[homotopy theory]].

We close here by briefly indicating one example problem of recent interest, concerned with  the fine-structure of [[quantum anomaly cancellation]] in 2d [[QFT]].

One reason why the need for geometric homotopy theory in QFT is not mentioned  in the bulk of the QFT literature is that the of the discussion of [[quantum field theory]] is in [[perturbation theory]] (both in [[Planck's constant]] and in terms of the [[coupling constant]]). This perspective tends to hide the rich nature of what QFT fundamentally is, as [[non-perturbative quantum field theory]].

Phenomena like [[quantum anomaly cancellation]] are intrinsically phenomena in [[homotopy theory]]/[[(infinity,1)-topos theory]].

For instance a famous quantum anomaly in 2-dimensional QFT is the [[Freed-Witten-Kapustin anomaly]]. It roughly implies that the [[RR-field]] is a [[cocycle]] in [[twisted K-theory]] twisted by the [[B-field]] which is a  [[cocycle]] in [[ordinary cohomology]].

But this is not the full story. Actually the [[RR-field]] is a [[cocycle]] in [[twisted cohomology|twisted]] [[differential K-theory]] twisted by the 
[[B-field]] which is a  [[cocycle]] in [[ordinary differential cohomology]].

[[higher gauge fields]]

In ([DFM 09](#DFM09)) is indicated the rich subtleties in the quantum anomaly consistency conditions on these [[background fields]], assuming that [[twisted differential K-theory]] exists with some properties, but without having constructed it.

This is central for the discussion of 2d QFT. 

The infamous "[[landscape of string theory vacua]]" is essentially
the [[moduli space]] of certain 2d field theories satisfying consistency  conditions like this.

The central problem in showing the existence of a [[differential cohomology]] theory is to show the "differential cohomology diagram"

Then recently in 

([BunkeNikolausV&#246;lkl 13](#BunkeNikolausVoelkl13), [Bunke Nikolaus](#BunkeNikolaus)): realizable in [[tangent cohesion]].

this was solved: this diagram exists universally for every object in [[tangent cohesion|stable]] [[cohesive (infinity,1)-topos]]



For $\mathbf{H}$ a [[cohesive (∞,1)-topos]]
every [[stable homotopy type]] $A \in Stab(\mathbf{H}) \hookrightarrow T \mathbf{H}$ sits inside a [[diagram]] of the form

$$
  \array{
    &&  \Pi_{dR} \Omega A && \longrightarrow && \flat_{dR}\Sigma A
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_A}} && \searrow
    \\
    \flat \Pi_{dR} \Omega A  && && A && && \Pi \flat_{dR}\Sigma A
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{\Pi \theta_A}}
    \\
    && \flat A && \longrightarrow && \Pi A
  }
  \,,
$$

where the two squares are [[homotopy pullback]] squares and the two diagonals are the [[fiber sequences]] of the [[Maurer-Cartan form]] $\theta_A$ and its dual.


The bottom horizontal morphisms in the diagram in prop. \ref{TheDifferentialDiagram} are the canonical [points-to-pieces transform](cohesive%20topos#CanonicalComparison).




## References


* [[William Lawvere]] _[[Categorical dynamics]]_, 1967 Chicago lectures ([pdf](http://www.mat.uc.pt/~ct2011/abstracts/lawvere_w.pdf))
 {#Lawvere67}

* [[William Lawvere]], Introduction to _[[Categories in Continuum Physics]], Lectures given at a Workshop held at SUNY, Buffalo 1982. Lecture Notes in Mathematics 1174. 1986
 {#Lawvere86}


* [[William Lawvere]], _[[Toposes of laws of motion]]_, 1997
 {#Lawvere97}

* _[[schreiber:Classical field theory via Cohesive homotopy types]]_

* _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))
 {#dcct}

* _[[schreiber:Synthetic Quantum Field Theory]]_
 {#syntheticQFT}

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local boundary prequantum field theory]]_
 {#Nuiten13}


* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))
 {#DFM09}



* [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))
  {#BunkeNikolausVoelkl13}

* [[Ulrich Bunke]], [[Thomas Nikolaus]], _Twisted differential cohomology_
 {#BunkeNikolaus}
