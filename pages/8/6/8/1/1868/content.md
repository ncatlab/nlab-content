
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A _twisted principal-bundle_ is the object classified by a cocycle in [[twisted cohomology]] the way an ordinary [[principal bundle]] is the object classified by a cocycle in plain [[cohomology]] (generally in [[nonabelian cohomology]]).

For $\hat G$ a [[group]], a $\hat G$-[[principal bundle]] is classified in degree 1 [[nonabelian cohomology]] with coefficients in the [[delooping|delooped]] [[groupoid]] $\mathbf{B} \hat G$.

Given a realization of $\hat G$ as an abelian extension 

$$
  A \to \hat G \to G
$$

of groups, i.e. given a [[fibration sequence]]

$$
  \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G
$$

of [[groupoid]]s such that $\mathbf{B}A$ is once [[delooping|deloopable]] so that the [[fibration sequence]] continues to the right at least one step as

$$
  \mathbf{B}\hat G \to \mathbf{B}G \to \mathbf{B}^2 A
$$


the general mechanism of [[twisted cohomology]] induces a notion of _twisted_ $\hat G$-cohomology. The fibrations classified by this are the twisted $\hat G$-bundles.

## Definition 

We give a discussion of twisted bundles as a realization of [[twisted cohomology]] in any [[cohesive (∞,1)-topos]] $\mathbf{H}$ as described in the section <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#TwistedCohomology">cohesive (∞,1)-topos -- twisted cohomology</a>. For the cases that $\mathbf{H} = $ [[ETop∞Grpd]] or $\mathbf{H} = $ [[Smooth∞Grpd]] this reproduces the traditional notion of [[topology|topological]] and [[smooth structure|smooth]] twisted bundles, respectively, whose twists are correspondingly topological or smooth [[bundle gerbe]]s/[[circle n-bundle]]s.

### Setup

Let $\mathbf{B}U(1) \in \mathbf{H}$ be the [[circle n-group]]. We shall concentrate here for definiteness on twists in $\mathbf{B}^2 U(1)$-[[cohomology]], since that reproduces the usual notions of twisted bundles found in the literature. But every other choice would work, too, and yield a corresponding notion of twisted bundles.

Fix once and for all an [[∞-group]] $G \in \mathbf{H}$ and a [[cocycle]]

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^2 U(1)
$$

representing a [[characteristic class]] 

$$
  [\mathbf{c}] \in H_{Smooth}^2(\mathbf{B}G,U(1)
$$

Notice that if $G$ is a [[compact space|compact]] [[Lie group]], as usual for the discussion of twisted bundles where $G = P U(n)$ is the [[projective unitary group]] in some dimension $n$, then by <a href="http://nlab.mathforge.org/nlab/show/smooth%20infinity-groupoid#CohomologyOfLieGroups">this theorem</a> we have that 

$$
  H_{Smooth}^2(\mathbf{B}G, U(1)) \simeq H^3(B G, \mathbb{Z})
  \,,
$$

where on the right we have the ordinary [[integral cohomology]] of the [[classifying space]] $B G \in$ [[Top]] of $G$.

### The abstract definition

Let $G$ an $\mathbf{c}$ as above.  

+-- {: .num_defn #TheGroupExtension}
###### Definition

Write

$$
  \mathbf{B}\hat G \to \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^2 U(1)
$$

for the [[homotopy fiber]] of $\mathbf{c}$.

=--

This identifies $\hat G$ as the [[group extension]] of $\mathbf{G}$ by the 2-[[cocycle]] $\mathbf{c}$.


+-- {: .num_note #TheGroupExtensionAsACircleBundle}
###### Note

Equivalently this means that 

$$
  \mathbf{B}U(1) \to \mathbf{B}\hat G \to \mathbf{B}G
$$

is the smooth [[circle n-bundle|circle 2-bundle]]/[[bundle gerbe]] classified by $\mathbf{c}$ and its [[loop space object]]

$$
  U(1) \to \hat G \to G
$$

the corresponding [[circle group]] [[principal bundle]] on $G$.

=--

Let $X \in \mathbf{H}$ be any object. From _[[twisted cohomology]]_ we have the following notion.


+-- {: .num_defn #AbstractDefinition}
###### Definition

The degree-1 **total twisted cohomology** 

$$
  H_{tw}^1(X, \hat G)
$$

of $X$ with coefficients in $\hat G$, def. \ref{TheGroupExtension}, relative to the characteristic class $[\mathbf{c}]$ is the set 

$$
  H^1_{tw}(X, \hat G) := \pi_0 \mathbf{H}_{tw}(X, \mathbf{G}\hat H)
$$ 

of connected cpomonets of the [[(∞,1)-pullback]]

$$
  \array{  
    \mathbf{H}_{tw}(X, \mathbf{B}\hat G) &\stackrel{tw}{\to}& 
      H_{Smooth}^3(X,U(1))
    \\
     \downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}G)
     &\stackrel{\mathbf{c}_*}{\to}&
    \mathbf{H}(X, \mathbf{B}^2 U(1))
  }
  \,,
$$

where the right verticsl morphism is any [[section]] of the truncation projection from cocycles to cohomology classes.

Given a twisting class $[\alpha] \in H^2_{smooth}(U(1))$ we say that

$$
  H_{[\alpha]}^1(X,\hat G)
  :=
  H^1_{tw}(X, \hat G) \times_{[\alpha]} *
$$

is the $[\alpha]$-**twisted cohomology** of $X$ with coefficients in $\hat G$ relative to $\mathbf{c}$.


=--

+-- {: .num_note #VanishingTwistGivesOrdinaryBundles}
###### Note

For $[\alpha] = 0$ the trivial twist, $[\alpha]$-twisted cohomology coincides with ordinary cohomology:

$$
  H^1_{[\alpha] = 0}(X, \hat G)
  \simeq
  H^_{Smooth}(X, \hat G)
  \,.
$$

=--

By the discussion at _[[principal ∞-bundle]]_ we may identify the elements of $H^1_{Smooth}(X, \hat G)$ with $\hat G$-[[principal ∞-bundle]]s $P \to X$. In particular if $\hat G$ is an ordinary [[Lie group]] and $X$ is an ordinary [[smooth manifold]], then these are ordinary $\hat G$-[[principal bundle]]s over $X$. This justifies equivalently calling the elements of $H^1_{tw}(X,\hat G)$ **twisted principal $\infty$-bundles**. And we shall also write

$$
  \hat G TwBund(X) := H^1_{tw}(X, \hat G)
  \,,
$$

where throughout we leave the characteristic class $[\mathbf{c}]$ with respect to which the twisting is defined implcitly understood.


## Details

One may unwrap this abstract definition to obtain a concrete cocycle formula for twisted bundles.

For that purpose the above [[homotopy pullback]] is conveniently computed as an ordinary [[pullback]] after making the fibrant replacement

$$
  \array{
    \mathbf{H}(X,\mathbf{B}(A \to \hat G)) 
     &\to & 
    \mathbf{H}(X,\mathbf{B}^2 A)
    &\leftarrow&
    {*}
    \\
    \downarrow^{\simeq}
    &&
    \downarrow^{Id}
    &&
    \downarrow^{Id}
    \\
    \mathbf{H}(X,\mathbf{B}G) 
     &\to & 
    \mathbf{H}(X,\mathbf{B}^2 A)
    &\leftarrow&
    {*}
  }
  \,,
$$

where $(A \to \hat G)$ denotes the [[2-group]] corresponding to the [[crossed module]] obtained from the central extension $\hat G$.

Similarly identifying $\mathbf{B}^2 A = \mathbf{B}(A \to 1)$ as the [[delooping]] of the [[2-group]] coming from the [[crossed module]] $(A \to 1)$
the morphism $\mathbf{H}(X,\mathbf{B}(A \to G)) \to \mathbf{H}(X,\mathbf{B}^2 A)$ is now induced from the obvious projection of [[crossed module]]s

$$
 (A \to G) \to (A \to 1)
 \,.
$$

This then says that $c$-twisted $\mathbf{B}\hat G$-cocycles are precisely those $\mathbf{B}(A \to \hat G)$-cocycles whose projection to an $\mathbf{B}(A\to 1)$-cocycle is the prescribed twisting cocycle $c$.

We may consider a [[?ech cohomology|?ech cocycle]] relative to a cover $\{U_i \to X\}$, i.e. an [[anafunctor]] 

$$
  \array{
    C(U) &\stackrel{\hat g_{tw}}{\to}& 
      \mathbf{B}(A \to \hat G)
    \\
    \downarrow
    \\
    X
  }
$$

out of a [[?ech nerve]] $C(U)$ and notice that the functor $\hat g_{tw}$ is an assignment

$$
  \hat g_{tw}
  \;\;
  :
  \;\;
  \array{
    && (x,j)
    \\
    & \nearrow &\Downarrow& \searrow
    \\
    (x,i)
    &&\to&&
    (x,k)
  }
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    && \bullet
    \\
    & {}^{\hat g_{i j}(x)}\nearrow 
     &\Downarrow^{c_{i j k}(x)}& 
     \searrow^{\hat g_{j k}(x)}
    \\
    \bullet
    &&\stackrel{\hat g_{i k}(x)}{\to}&&
    \bullet
  }
$$

As already indicated by the notation, the further projection

$$
  C(U) \stackrel{\hat g_{tw}}{\to} 
  \mathbf{B}(A \to \hat G)
  \to 
  \mathbf{B}^2 A
$$

is constrained to be the cocycle $c$. Using the rules for [[crossed module]]s one reads off that the existence of the triangular cell on the right in $\mathbf{B}(A \to \hat G)$ is equivalent to the equation

$$
  \hat g_{i j}(x)
  \hat g_{j k}(x)
  =
  \hat g_{i k}(x)
  c_{i j k}(x)
  \,.
$$

In this cocycle equation form twisted bundles traditionally appear in the literature. Alternatively, allowing a general surjective submersion instead of an open cover, this yields the description of twisted bundles as prefered in the literature on [[bundle gerbe]]s, where they are called [[bundle gerbe module]]s: the $\mathbf{B}^2 A$-cocycle $c$ represents the $A$-bundle gerbe.


## Properties

### General

### Twisted K-theory

[[equivalence class|Equivalence classes]] of twisted $U(n)$-bundles for fixed $\mathbf{B}U(1)$-twist $\alpha$ form a model for [[topological K-theory|topological]] $\alpha$-[[twisted K-theory]]. See there for details.

## References

### General

The notion and term _twisted bundle_ (with finite rank) apparently first appears in 

* [[Marco Mackaay]], _A note on the holonomy of connections in twisted bundles_ ([arXiv](http://arxiv.org/abs/math/0106019)) .

The equivalent notion of [[gerbe module]] apparently appears first in

* [[Ernesto Lupercio]], [[Bernardo Uribe]], _Gerbes over Orbifolds and Twisted K-theory_ ([arXiv](http://arxiv.org/abs/math/0105039)) ,

there explicitly in terms of [[Cech cohomology|Cech cocycles]] relative to an [[open cover]]. The generalization to infinite rank and arbitrary covering morphisms was amplified in ([CBMMS](#CBMMS)) below.

### In twisted K-theory 

Just as [[vector bundle]]s model cocycles in [[K-theory]], twisted vector bundles model cocycles in [[twisted K-theory]].

For twists $c$ that are torsion class (i.e. have finite order as group elements in the [[cohomology group]] $H(X,\mathbf{B}^2 A)$ ) this was realized in

* [[Alan Carey]], [[Peter Bouwknegt]], [[Varghese Mathai]], [[Michael Murray]] and [[Danny Stevenson]], _K-theory of bundle gerbes and twisted K-theory_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv](http://arxiv.org/abs/hep-th/0106194))
  {#CBMMS} 

which also, apparently, is the source where gerbe modules as such were first introduced.

The generalization of this construction to non-torsion twists requires using [[vectorial bundle]]s instead of plain [[vector bundle]]s. Full twisted K-theory in terms of twisted vectorial bundles was realized in

* Kiyonori Gomi, _Twisted K-theory and finite-dimensional approximation_ ([arXiv](http://arxiv.org/abs/0803.2327))

There the twisted cocycle equation discussed above appears on the bottom of page 7.



[[!redirects twisted bundles]]