
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
 {#Setup}

Let $\mathbf{B}^{n-1}U(1) \in \mathbf{H}$ be the [[circle n-group]]. We shall concentrate here for definiteness on twists in $\mathbf{B}^2 U(1)$-[[cohomology]], since that reproduces the usual notions of twisted bundles found in the literature. But every other choice would work, too, and yield a corresponding notion of twisted bundles.

Fix once and for all an [[∞-group]] $G \in \mathbf{H}$ and a [[cocycle]]

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^2 U(1)
$$

representing a [[characteristic class]] 

$$
  [\mathbf{c}] \in H_{Smooth}^2(\mathbf{B}G,U(1))
$$

Notice that if $G$ is a [[compact space|compact]] [[Lie group]], as usual for the discussion of twisted bundles where $G = P U(n)$ is the [[projective unitary group]] in some dimension $n$, then by <a href="http://nlab.mathforge.org/nlab/show/smooth%20infinity-groupoid#CohomologyOfLieGroups">this theorem</a> we have that 

$$
  H_{Smooth}^2(\mathbf{B}G, U(1)) \simeq H^3(B G, \mathbb{Z})
  \,,
$$

where on the right we have the ordinary [[integral cohomology]] of the [[classifying space]] $B G \in$ [[Top]] of $G$.


### The abstract definition

Let $G$ and $\mathbf{c}$ be as [above](#Setup).  

+-- {: .num_defn #TheGroupExtension}
###### Definition

Write

$$
  \mathbf{B}\hat G \to \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^2 U(1)
$$

for the [[homotopy fiber]] of $\mathbf{c}$.

=--

This identifies $\hat G$ as the [[group extension]] of $G$ by the 2-[[cocycle]] $\mathbf{c}$.


+-- {: .num_note #TheGroupExtensionAsACircleBundle}
###### Note

Equivalently this means that 

$$
  \mathbf{B}U(1) \to \mathbf{B}\hat G \to \mathbf{B}G
$$

is the smooth [[circle n-bundle|circle 2-bundle]]/[[bundle gerbe]] classified by $\mathbf{c}$; and its [[loop space object]]

$$
  U(1) \to \hat G \to G
$$

the corresponding [[circle group]] [[principal bundle]] on $G$.

=--

Let $X \in \mathbf{H}$ be any object. From _[[twisted cohomology]]_ we have the following notion.


+-- {: .num_defn #AbstractDefinition}
###### Definition

The degree-1 **total twisted cohomology** $H_{tw}^1(X, \hat G)$
of $X$ with coefficients in $\hat G$, def. \ref{TheGroupExtension}, relative to the characteristic class $[\mathbf{c}]$ is the set 

$$
  H^1_{tw}(X, \hat G) := \pi_0 \mathbf{H}_{tw}(X, \mathbf{G}\hat H)
$$ 

of connected components of the [[(∞,1)-pullback]]

$$
  \array{  
    \mathbf{H}_{tw}(X, \mathbf{B}\hat G) &\stackrel{tw}{\to}& 
      H_{Smooth}^2(X,U(1))
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

Given a twisting class $[\alpha] \in H^2_{Smooth}(U(1))$ we say that

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
  H^1_{Smooth}(X, \hat G)
  \,.
$$

=--

By the discussion at _[[principal ∞-bundle]]_ we may identify the elements of $H^1_{Smooth}(X, \hat G)$ with $\hat G$-[[principal ∞-bundle]]s $P \to X$. In particular if $\hat G$ is an ordinary [[Lie group]] and $X$ is an ordinary [[smooth manifold]], then these are ordinary $\hat G$-[[principal bundle]]s over $X$. This justifies equivalently calling the elements of $H^1_{tw}(X,\hat G)$ **twisted principal $\infty$-bundles**; and we shall write

$$
  \hat G TwBund(X) := H^1_{tw}(X, \hat G)
  \,,
$$

where throughout we leave the characteristic class $[\mathbf{c}]$ with respect to which the twisting is defined implcitly understood.


### Explicit cocycles

We unwind the abstract definition, def. \ref{AbstractDefinition}, to obtain the explicit definition of twisted bundles by [[Cech cohomology|Cech cocycles]] the way they appear in the traditional literature (see the [General References](#GeneralReferences) below).

+-- {: .num_prop #CechCocyclesForTwisted1Bundles}
###### Proposition

Let $U(1) \to \hat G \to G$ be a [[group extension]] of [[topological group]]s.

Let $X \in $ [[Mfd]] $\hookrightarrow$ [[ETop∞Grpd]] $=: \mathbf{H}$ be a [[paracompact topological space|paracompact]] [[topological manifold]] with [[good open cover]] $\{U_i \to X\}$.

1. Relative to this every twisting cocycle $[\alpha] \in H^2_{ETop}(X, U(1))$ is a [[Cech cohomology]] representative given by a collection of functions

   $$
     \{ \alpha_{i j k} : U_i \cap U_j \cap U_k \to U(1) \}
   $$

   satisfying on every quadruple intersection the equation

   $$
     \alpha_{i j k} \alpha_{i k l} = \alpha_{j k l} \alpha_{i j l}
     \,.
   $$

1. I terms of this cocycle data the twisted cohomology $H^1_{[\alpha]}(X, \hat G)$ is given by [[equivalence class]]es of [[cocycle]]s consisting of

   1. collections of functions

      $$
        \{g_{i j} : U_i \cap U_j \to \hat G \}
      $$

      subject to the condition that on each triple overlap the equation
 
      $$
        g_{i j} \dot g_{j k} = g_{i k} \cdot \alpha_{i j k}
      $$

      holds, where on the right we are injecting 
      $\alpha_{i j k}$ via $U(1) \to \hat G$ into $\hat G$  
      and then form the product there;

   1. subject to the [[equivalence relation]] that identifies two such collections of cocycle data $\{g_{i j}\}$ and $\{g'_{i j}\}$ if there exists functions

      $$
        \{h_i : U_i \to \hat G\}
      $$

      and

      $$
        \{\beta_{i j} : U_i \cap U_j \to \hat U(1)\}
      $$

      such that

      $$
        \beta_{i j} \beta_{j k} = \beta_{i k}
      $$

      and

      $$
        g'_{i j} = h_i^{-1} \cdot g_{i j} \cdot h_j \cdot \beta_{i j}   
        \,.
      $$

=--

+-- {: .proof}
###### Proof

We pass to the standard [[presentable (∞,1)-category|presentation]] of [[ETop∞Grpd]] by the projective local [[model structure on simplicial presheaves]] over the [[site]] [[CartSp]]. We then compute the defining [[(∞,1)-pullback]] by a [[homotopy pullback]] there.

Write $\mathbf{B}\hat G_{c}, \mathbf{B}^2 U(1)_c \in [CartSp^{op}, sSet]$ etc. for the standard models of the abstract objects of these names by simplicial presheaves. Write accordingly $\mathbf{B}(U(1) \to \hat G)_c$ for the delooping of the [[crossed module]] associated to the central extension $\hat G \to G$.

In terms of this the [[characteristic class]] $\mathbf{c}$ is represented by the  [[∞-anafunctor]]

$$
  \array{
    \mathbf{B}(U(1) \to \hat G)_c &\stackrel{\mathbf{c}}{\to}&
     \mathbf{B}(U(1) \to 1)_c
     =
     \mathbf{B}^2 U(1)_c
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}G_c
  }
  \,,
$$

where the top horizontal morphism is the evident projection onto the $U(1)$-labels.
Moreover, the [[Cech nerve]] of the good open cover $\{U_i \to X\}$ forms a cofibrant [[resolution]]

$$
  \emptyset \hookrightarrow C(\{U_i\}) \stackrel{\simeq}{\to} X
$$

and so $\alpha$ is presented by an [[∞-anafunctor]]

$$
  \array{
     C(\{U_i\}) &\stackrel{\alpha}{\to}& \mathbf{B}^2 U(1)_c
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
  \,.
$$

Using that $[CartSp^{op}, sSet]_{proj}$ is a [[simplicial model category]] this means in conclusion that the [[homotopy pullback]] in question is given by the ordinary [[pullback]] of [[simplicial set]]s

$$
  \array{
     \mathbf{H}^1_{[\alpha]}(X,\hat G) &\to& *
     \\
     \downarrow && \downarrow^{\mathrlap{\alpha}}
     \\
     [CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}(U(1) \to \hat G)_c)
     &\stackrel{\mathbf{c}_*}{\to}&
     [CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}^2 U(1)_c)
  }
  \,.
$$

An object of the resulting simplicial set is then seen to be a simplicial map $g : C(\{U_i\}) \to \mathbf{B}(U(1) \to \hat G)_c$ that assigns

$$
  g
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
    & {}^{\mathllap{g_{i j}(x)}}\nearrow 
     &\Downarrow^{\alpha_{i j k}(x)}& 
     \searrow^{\mathrlap{g_{j k}(x)}}
    \\
    \bullet
    &&\underset{g_{i k}(x)}{\to}&&
    \bullet
  }
$$

such that projection out along $\mathbf{B}(U(1) \to \hat G)_c \to \mathbf{B}(U(1) \to 1)_c = \mathbf{B}^2 U(1)_c$ produces $\alpha$.

Similarily for the morphisms. Writing out what these diagrams in $\mathbf{B}(U(1) \to \hat G)_c$ mean in equations, one finds the formulas claimed above.

=--


## Properties

### General

(...)

Consider the extension $U(1) \to U(n) \to P U(n)$ of the [[projective unitary group]] to the [[unitary group]] for all $n$. Then [[direct sum]] of matrices gives a sum operation

$$
  H^1_{[\alpha]}(X, P U(n_1))
  \times
  H^1_{[\alpha]}(X, P U(n_2))
  \to 
  H^1_{[\alpha]}(X, P U(n_1 + n_2))  
$$

and a tensor product operation

$$
  H^1_{[\alpha_1]}(X, P U(n))
  \times
  H^1_{[\alpha_2]}(X, P U(n))
  \to 
  H^1_{[\alpha_1]+ [\alpha_2]}(X, P U(n_1 \cdot n_2))  
$$


(...)

### Twisted K-theory

[[equivalence class|Equivalence classes]] of twisted $U(n)$-bundles for fixed $\mathbf{B}U(1)$-twist $\alpha$ form a model for [[topological K-theory|topological]] $\alpha$-[[twisted K-theory]]. See there for details.

## Related concepts

* [[twisted K-theory]]

* [[Chan-Paton bundle]]

* [[twisted spin structure]]

* [[twisted ∞-bundle]]

* [[equivariant bundle]]


## References
 {#References}

### General
 {#GeneralReferences}

The notion and term _twisted bundle_ (with finite rank) apparently first appears in 

* [[Marco Mackaay]], _A note on the holonomy of connections in twisted bundles_ ([arXiv:math/0106019](http://arxiv.org/abs/math/0106019)) .

The equivalent notion of [[gerbe module]] apparently appears first in

* [[Ernesto Lupercio]], [[Bernardo Uribe]], _Gerbes over Orbifolds and Twisted K-theory_ ([arXiv:math/0105039](http://arxiv.org/abs/math/0105039)) ,

there explicitly in terms of [[Cech cohomology|Cech cocycles]] relative to an [[open cover]]. The generalization to infinite rank and arbitrary covering morphisms was amplified in ([CBMMS](#CBMMS)) below.

Discussion of a [[splitting principle]] for twisted vector bundles (phrased in terms of [[gerbe modules]]) is in

* {#Tomoda07} [[Atsushi Tomoda]], _On the splitting principle of bundle gerbe modules_, Osaka J. Math. Volume 44, Number 1 (2007), 231-246. ([Euclid](https://projecteuclid.org/euclid.ojm/1174324334), talk slides [pdf](http://ton.prosou.nu/official/ryousi2005.pdf))


### In twisted K-theory 

Just as [[vector bundle]]s model cocycles in [[K-theory]], twisted vector bundles model cocycles in [[twisted K-theory]].

For twists $c$ that are torsion class (i.e. have finite order as group elements in the [[cohomology group]] $H(X,\mathbf{B}^2 A)$ ) this was realized in

* [[Alan Carey]], [[Peter Bouwknegt]], [[Varghese Mathai]], [[Michael Murray]] and [[Danny Stevenson]], _K-theory of bundle gerbes and twisted K-theory_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv](http://arxiv.org/abs/hep-th/0106194))
  {#CBMMS} 

which also, apparently, is the source where gerbe modules as such were first introduced.

The generalization of this construction to non-torsion twists requires using [[vectorial bundle]]s instead of plain [[vector bundle]]s. Full twisted K-theory in terms of twisted vectorial bundles was realized in

* [[Kiyonori Gomi]], _Twisted K-theory and finite-dimensional approximation_ ([arXiv](http://arxiv.org/abs/0803.2327))

There the twisted cocycle equation discussed above appears on the bottom of page 7.

Then there is

* [[Max Karoubi]], _Twisted bundles and twisted K-theory_, Clay Mathematics Proceedings, Volume 19 (2011) ([pdf](http://www.math.jussieu.fr/~karoubi/Publications/89.pdf))
 {#Karoubi}

* [[Ulrich Pennig]], _Twisted K-theory with coefficients in $C^\ast$-algebras_, ([arXiv:1103.4096](http://arxiv.org/abs/1103.4096))
 {#Pennig}


### As 2-sections of 2-bundles
 {#ReferencesAsSectionsOf2Bundles}

The observation that twisted vector bundles may be understood as higher-order [[sections]] of [[2-vector bundle]]s associated with [[circle n-bundle with connection|circle 2-bundles]]/[[bundle gerbes]] appears in

* [[Urs Schreiber]], _Quantum 2-States: Sections of 2-vector bundles_ Talk at _Higher categories and their applications_, Fields institute (2007) ([[Schreiber2States.pdf:file]]).

A discussion of this with [[connection on a bundle|2-connections]] taken into account is in section 4.4.3 of 

* [[Urs Schreiber]], [[Konrad Waldorf]], _Connections on non-abelian Gerbes and their Holonomy_ ([arXiv:0808.1923](http://arxiv.org/abs/0808.1923))

A discussion in the context of [[principal infinity-bundles]] (as opposed to higher vector bundles), is in section "2.3.5 Twisted cohomology and sections" and then in section  "3.3.7.2 Twisted 1-bundles -- twisted K-theory"

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_.


The observation then re-appears independently in 

* [[Chris Rogers]], _Higher geometric quantization_, talk at _Higher Structures_ in G&#246;ttingen (2011) ([pdf slides](http://www.crcg.de/wiki/Higher_geometric_quantization))


[[!redirects twisted bundles]]

[[!redirects twisted vector bundle]]
[[!redirects twisted vector bundles]]

[[!redirects twisted unitary bundle]]
[[!redirects twisted unitary bundles]]
