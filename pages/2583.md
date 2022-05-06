
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents goes here
{:toc}

## Idea

The _string 2-group_ is a [[smooth ∞-groupoid|smooth 2-group]]-refinement of the [[topological group]] called the [[string group]]. It is the [[∞-group extension]] induced by the smooth/stacky version of the [[first fractional Pontryagin class]]/[[second Chern class]].


## Definition

A string 2-group extension $String(G)$ is defined for every [[simple Lie group|simple]] [[simply connected topological space|simply connected]] [[compact Lie group]] $G$, such as the [[spin group]] $G = Spin(n)$ or the [[special unitary group]] $G = SU(n)$ (for non-low $n$).

Since [[string structures]] arise predominantly as higher analogs of [[spin structures]], the default choice is $G = Spin$ and in that case one usually just writes $String = String(Spin)$, for short. 

Recall first that the [[string group]] in [[Top]] is one step in the [[Whitehead tower]] of the [[orthogonal group]].

+-- {: .num_defn #AbstractDefinitionDiscrete}
###### Definition

For $n \in \mathbb{N}$ let $Spin(n)$ denote the [[spin group]], regarded as a [[topological group]]. Write $B Spin(n) \in $ [[Top]] for its [[classifying space]] and 

$$
  \frac{1}{2}p_1 : B Spin(n) \to B^4 \mathbb{Z}
$$

for a representative of the [[characteristic class]] called the first fractional [[Pontryagin class]]. Its [[homotopy fiber]] in the [[(∞,1)-topos]] [[Top]] $\simeq$ [[∞Grpd]] is denoted $B String(n) := B O(n)\langle 7 \rangle$

$$
  \array{
     B String(n) &\to& * 
     \\
     \downarrow && \downarrow
     \\
     B Spin(n) &\stackrel{\frac{1}{2} p_1}{\to}& B^4 \mathbb{Z}
  }
  \,.
$$

The [[loop space]] 

$$
  String(n) := \Omega B String(n)
$$

is the [[∞-group]]-object in [[Top]] called the **[[string group]]**.

=--

Write now

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc)
   :
  Smooth\infty Grpd
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}
  \infty Grpd
    \simeq 
  Top
$$

for the [[(∞,1)-topos]] [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s, regarded as a [[cohesive (∞,1)-topos]] over [[∞Grpd]]. 

+-- {: .num_prop #SmoothFractionalPontryaginClass}
###### Proposition

There is a lift through $\Pi$ of $\frac{1}{2} p_1$ to the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth first fractional Pontryagin class</a>

$$
  \frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin(n) \to \mathbf{B}^3 U(1)
$$

in [[Smooth∞Grpd]], where

* $\mathbf{B}Spin$ is the [[delooping]] [[Lie groupoid]] of $Spin(n)$ regarded as a [[Lie group]] (see <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#LieGroups">Smooth ∞-groupoids -- Cohesive ∞-groups -- Lie groups</a>);

* $\mathbf{B}^3 U(1)$ is the three-fold delooping of the [[circle group]], regarded as a [[Lie group]] (see <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">Smooth ∞-groupoids -- Cohesive ∞-groups -- Circle Lie n-group</a>);

* $\frac{1}{2}\mathbf{p}_1$ is the image under [[Lie integration]] of the canonical [[Lie algebra cohomology|cocycle]]
  
  $$
    \mu = \langle -,[-,-]\rangle : \mathfrak{so}(n) \to b^2 \mathbb{R}
    \,.
  $$
    
  on the [[orthogonal Lie algebra]].

=--

This is shown in ([FSS](#FSS)).


+-- {: .num_defn #AbstractDefinitionSmooth}
###### Definition

Write $\mathbf{B}String(n)$ for the [[homotopy fiber]] of the smooth
first fractional Pontryagin class

$$
  \array{
    \mathbf{B}String &\to& * 
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}Spin &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}&
    \mathbf{B}^3 U(1)
  }
$$

in [[Smooth∞Grpd]]. Its [[loop space object]]

$$
  String(n) := \Omega \mathbf{B}String(n)
$$

is the [[∞-Lie group|smooth ∞-group]] called [[generalized the|the]] **smooth string 2-group**.


=--

## Properties
 {#Properties}

Write

$$
  \vert - \vert := \vert\Pi(-)\vert :
  Smooth \infty Grpd
    \stackrel{\Pi}{\to}
  \infty Grpd
    \stackrel{\vert - \vert}{\to}
  Top
$$

for the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Homotopy">intrinsic geometric realization</a> in [[Smooth∞Grpd]].

+-- {: .num_prop}
###### Proposition

The smooth string 2-group, def. \ref{AbstractDefinitionSmooth},
indeed maps under $\vert-\vert$ to the topological string group:

$$
  \vert \mathbf{B}String(n) \vert
  \simeq
  B String(n)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since $\mathbf{B}^3 U(1)$ is presented by a simplicial presheaf that is degreewise presented by a paracompact smooth manifold (a finite product of the [[circle group]] with itself), it follows from the general properties of $\Pi$ discussed at [[Smooth∞Grpd]] that $\Pi$ preserves the [[homotopy fiber]] of $\frac{1}{2}\mathbf{p}_1$.

=--


## Presentations

Several explicit presentations of the string Lie 2-group are known.


### By Lie integration of the string Lie 2-algebra 
 {#ByLieIntegrationOfStringLie2Algebra}

We discuss a presentation of the smooth string 2-group by [[Lie integration]] of the skeletal version of the [[string Lie 2-algebra]].

Recall the identification of [[L-∞ algebra]]s $\mathfrak{g}$ with their dual [[Chevalley-Eilenberg algebra]]s $CE(\mathfrak{g})$.

+-- {: .num_defn}
###### Definition

Write

$$
  \mu := \langle - ,[-,-]\rangle
  : 
  \mathfrak{so}(n) \to b^2 \mathbb{R}
$$

for the canonical degree-3 [[cocycle]] in the [[Lie algebra cohomology]] of the [[special orthogonal group]], normalized such that the 3-form

$$
  \Omega^\bullet(Spin(n)) \hookleftarrow
  CE(\mathfrak{so}(n))
  \stackrel{\mu}{\leftarrow}
  CE(b^2 \mathbb{R})
$$

represents the image in [[de Rham cohomology]] of a generators of the [[integral cohomology]] group $H^3(G,\mathbb{Z}) \simeq \mathbb{Z}$.

Define the **[[string Lie 2-algebra]]**

$$
  \mathfrak{string}(n) := \mathfrak{so}(n)_\mu
$$

to be given by the [[Chevalley-Eilenberg algebra]]

$$
  CE(\mathfrak{string}(n)) := \wedge^\bullet ( \mathfrak{so}(n)^* \oplus \langle b\rangle , d_{\mathfrak{string}})
$$

which is that of $\mathfrak{so}(n)$ with a single generator $b$ in degree 3 adjoined and the differential given by

$$
  d_{\mathfrak{string}}|_{\mathfrak{so}(n)^*} = d_{\mathfrak{so}(n)};
$$

$$
  d_{\mathfrak{string}} : b \mapsto \mu
  \,.
$$

=--

+-- {: .num_prop #HomotopyFiberOfLInftyAlgebraCocycle}
###### Proposition

We have a [[pullback]] square in $L_\infty Alg$

$$
  \array{
    \mathfrak{string}(n) &\to& e b \mathbb{R}
    \\
    \downarrow && \downarrow
    \\
    \mathfrak{so}(n) &\stackrel{\mu}{\to}& b^2 \mathbb{R}
  }
  \,.
$$

=--

See [[string Lie 2-algebra]] for more discussion.

+-- {: .num_prop}
###### Proposition

The [[Lie integration]] of $\mathfrak{string}(n)$ yields a presentation of the 
smooth String 2-group, def. \ref{AbstractDefinitionSmooth}

$$
  \mathbf{cosk}_3 \exp(\mathfrak{string}(n))
  \simeq
  \mathbf{B} String(n)
  \,.
$$

=--

This is essentially the model considered in ([Henriques](#Henriques)), discussed here in the context of [[Smooth∞Grpd]] as described in ([FSS](#FSS)).

+-- {: .proof}
###### Proof

We observe the image under [[Lie integration]] of the $L_\infty$-algebra pullback diagram from prop. \ref{HomotopyFiberOfLInftyAlgebraCocycle} is a pullback diagram in $[CartSp_{smooth}^{op}, sSet]_{proj}$ that presents the defining [[homotopy fiber]]. Before applying the [[coskeleton]] operation we have immediately


$$
  \exp(-) 
    \; :\; 
  \left(
   \array{
     \mathfrak{string}(n) &\to& e b \mathbb{R}
     \\
     \downarrow && \downarrow
     \\
     \mathfrak{so}(n) &\stackrel{\mu}{\to}& b^2 \mathbb{R}
   }
  \right)
  \;\mapsto \;
  \left(
   \array{
     \exp(\mathfrak{string}(n)) &\to& \exp(e b \mathbb{R})
     \\
     \downarrow && \downarrow
     \\
     \exp(\mathfrak{so}(n)) &\stackrel{\mu}{\to}& \exp(b^2 \mathbb{R})
   }
  \right)
$$

such that on the right we still have a [[pullback]] diagram. 

We discuss the descent o this pullback diagram along the projection $\exp(\mathfrak{so}(n)) \to \mathbf{cosk}_3 \exp(\mathfrak{so}(n))$.

Notice from [[Lie integration]] the weak equivalence

$$
  \int_{\Delta^\bullet} : \exp(b^n \mathbb{R}) \simeq \mathbf{B}^{n+1}\mathbb{R}_c
  \,.
$$

Let $I$ be the set of maps $\partial \Delta[4] \to \exp(b^2 \mathbb{R})$ 
that fit into a diagram

$$
  \array{
    \partial \Delta[4] &\to& \exp(b^2 \mathbb{R})
    \\
    \downarrow && \downarrow^{\mathrlap{\int_{\Delta^\bullet}}}
    \\
    && \mathbf{B}^3 \mathbb{R}_c
    \\
    \downarrow && \downarrow 
    \\
    \Delta[4] &\to& \mathbf{B}^3 (\mathbb{Z} \to \mathbb{R})_c
  }
$$
    
(closed 3-forms on 3-balls whose integral is an integer).

Write

$$
  \exp(b^2 \mathbb{R}/\mathbb{Z}) 
    :=
  \mathbf{cosk}_3
   \left(
     (I \times \Delta[4])\coprod_{I \times \partial \Delta[4]} \mathbf{cosk_3} \exp(b^2 \mathbb{R})
   \right)
$$

for the result of filling all these by 4-cells. Similarly define
$\exp(e b \mathbb{R}/\mathbb{Z})$.


Then applying the [[coskeleton]] functor to the above pullback 
diagram and using the projection ([FSS](#FSS))

$$
  \array{
    \exp(\mathfrak{so}(n)) &\stackrel{\exp(\mu)}{\to}& \exp(b^2 \mathbb{R})
    \\
    \downarrow && \downarrow
    \\
    \mathbf{cosk}_3\exp(\mathfrak{so}(n)) 
      &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}&
    \exp(b^2 \mathbb{R}/\mathbb{Z})
  }
$$

we get the diagram

$$
  \array{
    \mathbf{cosk}_3 (\mathfrak{string}(n)) 
      &\to&
    \exp(e b \mathbb{R}/\mathbb{Z})
    \\
    \downarrow && \downarrow
    \\
    \mathbf{cosk}_3 \exp(\mathfrak{so})
    &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}&
    \exp(b^2 \mathbb{R}/\mathbb{Z})
  }
  \,.
$$

This is again a pullback diagram of a fibration resolution of the point inclusion, hence presents the homotopy fiber in question.


=--



### By strict Lie $2$-group
 {#PresentationByStrictTwoGroups}

A realization of the string 2-group as a [[strict 2-group]] [[internalization|internal]] to [[diffeological space]]s was given in ([BCSS](#BCSS)).


This is one of three different (there should be more), weakly equivalent such [[strict 2-group]] [[internalization|internal]] to [[diffeological space]] models that are discussed in the (to date unpublished)

* [nactwist, section 5.2.3](http://www.math.uni-hamburg.de/home/schreiber/nactwist.pdf#page=91)

(This particular section, and its results, are joint work of [[Urs Schreiber]] and [[Danny Stevenson]]).

We have the following pattern of routes through [[Lie integration]]:

$$
  \array{
    StrLie \omega Grpd
    &&&&
    StrLie \omega Grpd
    &\stackrel{\simeq}{\leftarrow}&
    LieCrsdCmplx
    \\
    \uparrow^{\Pi_n S CE}
    &&&&
    \uparrow
    &&
    \uparrow^{\exp(-)}
    \\
    L_\infty Algebras
    &&
    \leftarrow&&
    Str L_\infty Algebras
    &\to&
    DiffCrsdCmplx
  }
$$

Here $StrLie \omega Grpd$ is [[strict omega-groupoid]]s internal to [[diffeological space]]s, $LieCrsCmplx$ is accordingly smooth [[crossed complex]]es , $L_\infty Algebra$ is all [[L-infinity algebra]]s and $Str L_\infty Algebra$ is _strict_ $L_\infty$-algebras. The vertical morphism on the right is term-wise ordinary [[Lie integration]]. The other vertical morphisms take an [[L-infinity algebra]], form the [[sheaf]] on [[Diff]] of flat [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid differential form]]s, and then take [[path n-groupoid]] $\Pi_n(-)$ of that. 

For the String-case this yields

$$
  \array{
    \Pi_2(\Omega^\bullet_{fl}(-,\mathfrak{so}_{\mu_3}))
    &\stackrel{\simeq}{\mapsto}&
    \mathbf{B} String_{Mick}
    &\stackrel{\simeq}{\mapsto}&
    \mathbf{B} String_{BCSS}
    &\leftarrow|&
    (\hat \Omega Spin \to P Spin)
    \\
    \uparrow &&&\nearrow& \uparrow  && \uparrow
    \\
    \mathfrak{so}_{\mu_3}
    &&\stackrel{\simeq}{\mapsto}&&
    \mathfrak{string}
    &\mapsto&
    (\hat \Omega \mathfrak{so} \to P \mathfrak{so})    
  }
  \,,
$$

where 

* $\mathfrak{so}_{\mu_3}$ denotes the weak, skeletal [[String Lie 2-algebra]]

* $\mathfrak{string}$ its equivalent strict version given by BCSS

* the diagonal morphism is the construction in BCSS.

* the strict 2-groupoid $\Pi_2(\Omega^\bullet_{fl}(-,\mathfrak{g}_{\mu_3}))$ has, notice, as morphism smooth paths in $Spin(n)$ that are composed by concatenation

* the 2-groupoid $\mathbf{B}String_{Mick}$ is a version of the String Lie 2-group that manifestly uses the [[Mickelsson cocycle]] (morphism are paths in $Spin(n)$ that are composed using the group product) 

* the 2-groupoid $\mathbf{B}String_{BCSS}$ is the version given in BCSS (morhisms again are paths in $Spin(n)$ that are composed using the group product).


### As a finite-dimensional weak Lie 2-group 

([Schommer-Pries](#Schommer-Pries))

### As an automorphism 2-group of fermionic CFT

The string 2-group also appears as a certain [[automorphism 2-group]] inside the [[3-category of fermionic conformal nets]] ([Douglas-Henriques](#DouglasHenriques))

### As the automorphisms of the Wess-Zumino-Witten gerbe 2-connection

For $G$ a compact simply connected simple [[Lie group]], there is the "[[WZW gerbe]]", hence the [[circle n-bundle with connection|circle 2-bundle with connection]] on $G$ whose [[curvature]] 3-form is the [[left invariant differential form|left invariant]] extension $\langle \theta \wedge [\theta \wedge \theta]\rangle$ of the canonical Lie algebra 3-cocycle to the group

$$
  \mathcal{L}_{WZW} \;\colon\; G \longrightarrow \mathbf{B}^2U(1) 
  \,.
$$

+-- {: .num_prop }
###### Proposition

The string 2-group is the [[smooth infinity-group|smooth 2-group]] of [[automorphism infinity-group|automorphism]] of $\mathcal{L}_{WZW}$ which cover the left [[action]] of $G$ on itself (hence the "[[Heisenberg 2-group]]" of $\mathcal{L}_{WZW}$ regarded as a [[prequantum 2-bundle]])

$$
  \mathbf{Aut}(\mathcal{L}_{WZW}) \simeq String(G)
  \,,
$$

=--

This is due to ([Fiorenza-Rogers-Schreiber 13, section 2.6.1](#FiorenzaRogersSchreiber13)).




## Related concepts

* [[Platonic 2-group]]

[[fivebrane 6-group]] $\to$ **string 2-group** $\to$ [[spin group]] $\to$ [[special orthogonal group]] $\to$ [[orthogonal group]] $\hookrightarrow$ [[general linear group]]


* [[spin group]], [[spin structure]], [[twisted spin structure]]

* [[spin^c]], [[spin^c structure]], [[twisted spin^c structure]]

* [[string group]], [[string 2-group]], [[string structure]], [[twisted string structure]]

* [[T-duality 2-group]]

* [[string^c 2-group]]

* [[fivebrane group]], [[fivebrane 6-group]]



## References

A [[crossed module]] presentation of a topological realization of the string 2-group is implicit in 

* [[Stephan Stolz]], [[Peter Teichner]], _What is an elliptic object?_ ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.146.5463&rep=rep1&type=pdf))
{#StolzTeichner}

A realization of the string 2-group in [[∞-groupoid]]s [[internalization|internal to]] [[Banach space]]s by [[Lie integration]] of the skeletal version of the [[string Lie 2-algebra]] is in

* {#Henriques} [[Andre Henriques]], _Integrating $L_\infty$-algebras_, Compositio Mathematica, Volume 144, Issue 4 July 2008 , pp. 1017-1045 ([arXiv:math/0603563](http://arxiv.org/abs/math/0603563), [doi:10.1112/S0010437X07003405](https://doi.org/10.1112/S0010437X07003405))


A realization of the string 2-group in [[strict 2-group]]s internal to [[Frechet manifold]]s by  [[Lie integration]] of a [[strict Lie 2-algebra]] incarnation of the [[string Lie 2-algebra]] in in

* {#BCSS} [[John Baez]], [[Alissa Crans]], [[Urs Schreiber]], [[Danny Stevenson]], _From loop groups to 2-groups_, Homology Homotopy Appl. Volume 9, Number 2 (2007), 101-135. ([arXiv:math/0504123](https://arxiv.org/abs/math/0504123), [euclid:hha/1201127333](https://projecteuclid.org/euclid.hha/1201127333))

A realization of the string 2-group as a [[2-group]] in finite-dimensional [[smooth manifold]]s in in

* {#Schommer-Pries} [[Chris Schommer-Pries]], _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ ([arXiv:0911.2483](http://arxiv.org/abs/0911.2483))


A discussion as an [[∞-group]] object in [[Smooth∞Grpd]] and the realization of the smooth first fractional Pontryagin class is in

* {#FSS} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cech cocycles for differential characteristic classes_ (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#FSS">web</a>)


and in section 4.1 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

A 2-group model which has a smoothening of the _topological_ [[string group]] in lowest degree has been given in 

* [[Thomas Nikolaus]], [[Christoph Sachse]], [[Christoph Wockel]], _A Smooth Model for the String Group_,  International Mathematics Research Notices, Volume: 2013 , Issue: 16 , 2013   ([arXiv:1104.4288](http://arxiv.org/abs/1104.4288), [doi:10.1093/imrn/rns154](https://doi.org/10.1093/imrn/rns154))

A construction explicitly in terms of the "basic" [[bundle gerbe]] on $G$ is discussed in 

* [[Konrad Waldorf]], _A Construction of String 2-Group Models using a Transgression-Regression Technique_ ([arXiv:1201.5052](http://arxiv.org/abs/1201.5052))

Via fermionic nets/[[2-Clifford algebra]]:

* {#DouglasHenriques} [[Chris Douglas]], [[André Henriques]], _Geometric string structures_ ([pdf](http://www.staff.science.uu.nl/~henri105/PDF/TringWP.pdf))
 

The realization of the string 2-group as the [[Heisenberg 2-group]] of the [[WZW gerbe]] is due to 

* {#FiorenzaRogersSchreiber13} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_, 2013 ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))
  
A model of the string 2-group using the smooth [[free loop space]] (instead of the based [[loop space]]) is dicussed in


* {#MurrayRobertsWockel17} [[Michael Murray]], [[David Roberts]], [[Christoph Wockel]], _Quasi-periodic paths and a string 2-group model from the free loop group_ ([arXiv:1702.01514](https://arxiv.org/abs/1702.01514))

Discussion in the context of [[matrix factorizations]] and [[equivariant K-theory]] is in

* {#FreedTeleman14} [[Daniel S. Freed]], [[Constantin Teleman]], _Dirac families for loop groups as matrix factorizations_, [arxiv/1409.6051](http://arxiv.org/abs/1409.6051)

Discussion of a general definition of smooth [[string group]] extensions $A\rightarrow \mathrm{String}(H)\rightarrow H$ of a [[compact]] [[simply connected]] [[Lie group]] $H$, with $A$ not necessarily chosen to be $\mathbf{B}U(1)$ but only of the same [[homotopy type]], in

* [[Severin Bunk]], _Principal $\infty$-Bundles and Smooth String Group Models_, [arXiv:2008.12263](http://arxiv.org/abs/2008.12263)


[[!redirects String 2-group]]
[[!redirects String Lie 2-group]]
[[!redirects string Lie 2-group]]

[[!redirects smooth string 2-group]]