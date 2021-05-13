

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
 {#Idea}


By the discussion at _[[cohomology]]_, plain cohomology is the study of 

* [[(∞,1)-categorical hom-spaces]] in [[(∞,1)-toposes]] (for "[[nonabelian cohomology]]") 

* or their [[stabilizations]]  to [[stable (∞,1)-categories]] of [[spectrum objects]] (for "[[generalized (Eilenberg-Steenrod) cohomology]]") 

* or generally in  [[symmetric monoidal (∞,1)-categories]] 

and maybe fully generally in any [[(∞,1)-category]] $\mathcal{C}$ whatsoever.

So for $A \in \mathcal{C}$ any [[object]] the [[cohomology]] of any other object $X$ with [[coefficients]] in $A$ is the [[mapping space]] $\mathcal{C}(X,A)$. Notice that this is equivalently the [[homotopy type]] of [[sections]] $\mathcal{C}_{/X}(X, X \times A)$ of the trivial $A$-[[fiber ∞-bundle]] over $X$. The idea of _twisted cohomology_ then is to consider general $A$-[[fiber ∞-bundles]] $\chi$ over $X$ and take the $\chi$-twisted cohomology of $X$ to the type of [[sections]] of this.


| [[cohomology]] | twisted cohomology |
|--|--|
| [[homotopy types]] of [[mapping spaces]] | [[homotopy types]] of spaces of [[sections]] |

Given an $\infty$-topos $\mathbf{H}$, then also its arrow $\infty$-category $\mathbf{H}^I$ is an $\infty$-topos, over $\infty Grpd^I$ and it also sits over $\mathbf{H}$ by the [[codomain fibration]], constituting an "[[extension]]" of $\mathbf{H}$ by itself:

$$
  \array{
    \mathbf{H}
    \\
    \downarrow^{\mathrlap{incl}}
    \\
    \mathbf{H}^I
    \\
   \downarrow^{\mathrlap{cod}}
     \\
    \mathbf{H}
  }
  \,.
$$

The intrinsic cohomology of $\mathbf{H}^I$ under this fibration is [[nonabelian cohomology|nonabelian]] twisted cohomology as discussed in some detail in _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_.

Notice that "stable cohomology", which is traditionally called [[generalized (Eilenberg-Steenrod) cohomology]] may be thought of as the lowest order [[Goodwillie calculus|Goodwillie]] approximation to [[nonabelian cohomology]]: where a cocycle in nonabelian cohomology is a map to any [[homotopy type]], a cocycle in [[generalized (Eilenberg-Steenrod) cohomology]] is a map into a [[stable homotopy type]].

In this sense the [[tangent (infinity,1)-topos]] $T \mathbf{H}$ is the lowest order linear approximation to the [[codomain fibration]]

$$
  \array{
    \Stab(\mathbf{H})
    \\
    \downarrow^{\mathrlap{incl}}
    \\
    T\mathbf{H}
    \\
   \downarrow^{\mathrlap{cod}}
     \\
    \mathbf{H}
  }
  \,.
$$

Higher-order approximations should involve a notion of higher-order forms of the tangent (∞,1)-topos, in parallel with the relationship between the [[jet bundles]] and [[tangent bundle]] of a manifold. It is clear that whatever we may say in detail about the $k$th-[[jet (∞,1)-category|jet (∞,1)-topos]] $J^k \mathbf{H}$, its intrinsic cohomology is a version of twisted cohomology which is in between [[nonabelian cohomology]] and stable i.e. [[generalized (Eilenberg-Steenrod) cohomology]].

It seems that a layered analysis of nonabelian cohomology this way in higher homotopy theory should eventually be rather important, even if it hasn't received any attention at all yet. It seems plausible that a generalization of [[Chern-Weil theory]] which approximates classes of [[principal infinity-bundles]] not just by [[universal characteristic classes]] in [[ordinary cohomology]] and hence in stable cohomology, but that one wants to consider the whole Goodwillie Taylor tower of approximations to it.

## Definition
 {#Definition}


We discuss concrete realizations of the above [general idea](#Idea) in some cases of interest:

* _[In an ∞-topos](#InAnInfinityTopos)_

* _[In a stabilized ∞-topos ](#InAStabilizedInfinityTopos)_

* _[In a general symmetric monoidal ∞-category](#InASymmetricMonoidalInfinityCategory)_


### In an $\infty$-topos -- twisted nonabelian (sheaf) cohomology
 {#InAnInfinityTopos}


Let $\mathcal{C} = \mathbf{H}$ be an [[(∞,1)-topos]]. Let $A \in \mathbf{H}$ be any [[object]], to be called the [[coefficient]] object.

Write $\mathbf{Aut}(A) \in Grp(\mathbf{H})$ for the [[automorphism ∞-group]] of $A$ and $\mathbf{B}\mathbf{Aut}(A) \in \mathbf{H}$ for its [[delooping]]. There is a canonical  [[∞-action]] of $\mathbf{Aut}(A)$ on $A$ exhibited by the corresponding universal [[associated ∞-bundle]]

$$
  \array{
    A &\to& A//\mathbf{Aut}(A)
    \\
    && \downarrow^{\mathrlap{\rho_A}}
    \\
    && \mathbf{B}\mathbf{Aut}(A)
  }
  \,.
$$

Let $X \in \mathbf{H}$ be any object.
 
+-- {: .num_defn}
###### Definition

A **twist** for $A$-[[cohomology]] on $X$ is a morphism $\chi \colon X \to \mathbf{B}\mathbf{Aut}(A)$ in $\mathbf{H}$. The corresponding [[associated ∞-bundle|associated]] $A$-[[fiber ∞-bundle]] over $X$ which is the [[homotopy pullback]]

$$
  \array{
    \chi^\ast \rho_A &\to& A//\mathbf{Aut}(A)
    \\
    \downarrow && \downarrow^{\mathrlap{\rho_A}} 
    \\
    X &\stackrel{\chi}{\to}& \mathbf{B}\mathbf{Aut}(A)
  }
$$

we call the [[local coefficient ∞-bundle]] for twisted $A$-cohomology classified by $\chi$. 

The *[[cocycle]] [[∞-groupoid]] of $\chi$-twisted $A$-cohomology* is 

$$
  \Gamma_X(\chi^\ast \rho_A) \in \infty Grpd
  \,.
$$

The **$\chi$-twisted cohomology set** of $X$ is 

$$
  \pi_0 \Gamma_X(\chi^\ast \rho_A) \in Set
$$

=--

Special cases of this definition are implicit in traditional literature. The above statement appears in this form in ([Nikolaus-Schreiber-Stevenson 12](#NikolausSchreiberStevenson12)).

+-- {: .num_remark}
###### Remark

The $\chi$-twisted cohomology is equivalently the ordinary cohomology of $\chi$ with [[coefficients]] in $\rho_A$ in the [[slice (∞,1)-topos]] of $\mathbf{H}$ over $\mathbf{B}\mathbf{Aut}(A)$:

$$
  \Gamma_X(\chi^\ast \rho_A)
  \simeq
  \mathbf{H}_{/\mathbf{B}\mathbf{Aut}(A)}(\chi, \rho_A)
  \,.
$$

=--




### In a stabilized $\infty$-topos -- twisted ES-type (sheaf) cohomology
 {#InAStabilizedInfinityTopos}

Let now $\mathcal{C} = Stab(\mathbf{H})$ be an [[stable (∞,1)-category]] of [[spectrum objects]] in an ambient [[(∞,1)-topos]] $\mathbf{H}$. Let $E \in CRing_\infty(\mathbf{H})$ be a corresponding [[E-∞ ring]] object. Write

$$
  GL_1(E) \hookrightarrow \mathbf{Aut}(E)
  \in 
  Grp(\mathbf{H})
$$

for the [[∞-group of units]] of $E$. 

Now a twist $\chi \;\colon\; X \to \mathbf{B}GL_1(E)$ classifies an [[(∞,1)-module bundle]] of $E$-lines. The $\chi$-twisted $E$-cohomology is again the (stable) homotopy type of sections of this.

For the case of [[twisted K-theory]] (see the references there) this description goes back to [[Jonathan Rosenberg]]. The above general abstract description is developed in ([Ando-Blumberg-Gepner 10](#ABG10)).

For more details see 

* at _[[(∞,1)-module bundle]]_ the section _[Sections and twisted cohomology](%28infinity%2C1%29-module+bundle#SectionsAndTwistedCohomology)_

* at _[[twisted bivariant cohomology]]_ the section _[Axiomatization in homotopy theory](bivariant+cohomology+theory#AxiomatizazionInHomotopyTheory)_ .

+-- {: .num_remark #PicardGeneralizingGL1}
###### Remark

There are canonical maps

$$
  \mathbf{B}GL_1(E) \simeq E Line \hookrightarrow Pic(E Mod)
  \hookrightarrow E Mod
  \,,
$$

where $Pic(E Mod)$ denotes the [[Picard ∞-groupoid]]. This suggest to speak not just of twists of the form $\chi \colon X \to \mathbf{B}GL_1(E) \simeq E Line \hookrightarrow E Mod$ but more generally of twists of the form $\chi \colon Pic(E Mod) \hookrightarrow E Mod$. While these in general no longer define $E$-[[fiber ∞-bundles]] (so that sections of them are strictly speaking in general no longer locally $E$-cohomology cocycles), this more general notion has the advantage that it makes sense also in [[symmetric monoidal (∞,1)-categories]] different from those of the form $Stab(\mathbf{H})$. 

This we turn to [below](#InASymmetricMonoidalInfinityCategory).

=--


### In a general symmetric monoidal $\infty$-category
 {#InASymmetricMonoidalInfinityCategory}


+-- {: .num_remark }
###### Remark

If in the above situation we write $[X, E Mod]$ for the [[symmetric monoidal (∞,1)-category]] of $E$-[[(∞,1)-module bundles]] on $X$, then given an object $\chi \in [X,E Mod]$ its homotopy type of sections, hence the $\chi$-twisted cohomology of $X$ is equivalently

$$
  Hom_{[X, E Mod]}(\mathbb{I}_X, \chi)
  \in 
  \infty Grpd
  \,,
$$

where $\mathbb{I}_X$ is the [[tensor unit]] object, the trivial $E$-[[(∞,1)-module bundle]] over $X$.

=--

In view of this and remark \ref{PicardGeneralizingGL1} one considers the following.

Let $(\mathcal{C}, \otimes)$ be a [[symmetric monoidal (∞,1)-category]]. 

+-- {: .num_defn }
###### Definition

An object $\chi \in Pic(\mathcal{C})$ of the [[Picard ∞-groupoid]] of $\mathcal{C}$ we call a _twist_ for [[cohomology]] in $\mathcal{C}$. For $X, A \in \mathcal{C}$ any two [[objects]], we say that the *$\chi-twisted$ cohomology of $X$ with [[coefficients]] in $A$* is

$$
  \mathcal{C}(X, \chi \otimes A) \in \infty Grpd
  \,.
$$

=--


## Properties





### Twisted cohomology with trivial twisting cocycle

> old material, to be harmonized...

Let  ${*} \to B$ be a [[pointed object]]. Then

* we say that the [[cocycle]] 

  $(X \to * \to B) \in \mathbf{H}(X,B)$ 

  is the **trivial $B$-cocycle** on $X$.

*  the morphism $f:\hat{B}\to B$ induces a [[fibration sequence]] 

   $A \to \hat B \stackrel{f}{\to} B$ 

   in $\mathbf{H}$.


+-- {: .num_prop}
###### Proposition

The $([*],f)$-twisted cohomology with trivial twisting cocycle is equivalent to the ordinary [[cohomology]] with coefficients in the [[homotopy fiber]] $A$ of $f$:

$$
  \mathbf{H}_{[*]}(X,f) \simeq \mathbf{H}(X,A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition, the [[homotopy fiber]] of $A$ is the [[homotopy pullback]]

$$ 
  \array{
    A &\to& *
    \\
    \downarrow && \downarrow
    \\
    \hat B &\stackrel{f}{\to}& B
  }
$$

in $\mathbf{H}$. Since the $\infty$-groupoid valued [[derived hom-space|hom]] in an [[(∞,1)-category]] is [[exact functor|exact]] with respect ot [[homotopy limits]] (by definition of homotopy limits), it follows that for every object $X$, there is  fibration sequence of [[cocycle]] [[∞-groupoids]]

$$
  \array{
    \mathbf{H}(X,A) &\to& {*}
    \\
    \downarrow && \downarrow^{\mathrlap{const_{*}}}
    \\
    \mathbf{H}(X,\hat B) &\to& \mathbf{H}(X,B)
  }
  \,.
$$

By definition of twisted cohomology, this identifies

$$
  \mathbf{H}(X,A) \simeq \mathbf{H}_{[*]}(X,f)
  \,.
$$

=--

For this reason, when $B$ is pointed,
it is customary to call the set of equivalence classes $\pi_0\mathbf{H}_{[c]}(X;f)$ the **$c$-twisted $A$-cohomology of $X$**, and to denote it by the symbol

$$
  H_{[c]}(X,A)
$$

+-- {: .num_remark}
###### Remark
The cohomology fibration sequence $\mathbf{H}(X,A) \to \mathbf{H}(X,\hat B) {\to} \mathbf{H}(X,B)$ can be seen as an **obstruction problem** in cohomology:

* the **obstruction** to lifting a $\hat B$-cocycle to an $A$-cocycle is its image in $B$-cohomology (all with respect to the given [[fibration sequence]])

But it also says:

* $A$-cocycles are, up to equivalence, precisely those $\hat B$-cocycles whose class in $B$-cohomology is the class of the trivial $B$-cocycle.

=--


## Examples 

### Sections as twisted functions... {#SectionsAsTiwstedFunctions}

For $V$ a [[vector space]] and $X$ a manifold, both regarded a 0-[[truncated]] objects in the $(\infty,1)$-topos on the site [[CartSp]] (that of [[Lie infinity-groupoid]]s), a [[cocycle]] $X \to V$ is simply smooth $V$-valued function on $X$.

Now let $G$ be a Lie group with smooth [[delooping]] groupoid $\mathbf{B}G$ and let $\rho : \mathbf{B}G \to Vect$ be a [[representation]] of $G$ on $V$, i.e. $\rho(\bullet) = V$. Then the corresponding [[action groupoid]] $V//G$ sits in the [[fibration sequence]]

$$
  V \to V//G \stackrel{p}{\to} \mathbf{B}G
  \,.
$$

Hence we can ask for the $p$-twisted cohomology of $X$ with values in $V$. Now, a cocycle $g : X \to \mathbf{B}G$ is one classifying a $G$-[[principal bundle]] on $X$. By looking at this in [[Cech cohomology]] it is immediate to convince onself that cocycles $X \to V//G$ such that the composite $X \to V//G \stackrel{p}{\to} \mathbf{B}G$ is equivalent to the given $g$ are precisely the [[section]]s of the $\rho$-[[associated bundle|associated vector bundle]]:

on a patch $U_i$ of a good cover over wich $P$ has been trivialized, the cocycle $X \to V//G$ is simply a $V$-valued function $\sigma_i : U_i \to V$. Then on double overlaps it is a smooth [[natural transformation]] $\sigma_i|_{U_{i j}} \to \sigma_j|_{U_i j}$ whose components in $G$ are required to be those of the given cocycle $g$. That means exactly that the functions $(\sigma_i)$ are glued on double overlaps precisely as the local trivializations of a global section $\sigma : X \to P \times_G V$ would.

Hence we find the $p$-twisted cohomology is

$$
  H_{[g]}(X,V) = 
  \{sections\; of\; P \times_G V\}
  \,.
$$

In this sense **a section is a twisted function**.

Notice that $V//G \stackrel{p}{\to} \mathbf{B}G$ is not itself a homotopy fiber, but is a _lax_ fiber, in that we have a [[2-limit|lax pullback]] (really a _comma object_ )

$$
  \array{
    V//G &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\to& Vect
  }
  \,,
$$

where in the bottom right corner we have [[Vect]] (regarded as a [[stack]] on $CartSp$ in the evident way) and where the right vertical morphism sends the point to the ground field vector space $k$ (or rather sends $U \in CartSp$ to the trivial vector bundle $U \times k$ ).

We may paste to this the homotopy pullback along the cocycle $g : X \to \mathbf{B}G$ to obtain

$$
  \array{
    P\times_G V &\to& V//G &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G &\to& Vect
  }
  \,.
$$

This makes is manifest that a section $\sigma : X \to P \times_G V$ is also the same as a natural transformation from $const_k : X \to Vect$ to $X \stackrel{g}{\to} \mathbf{B}G \to Vect$.

Notice moreover that in the special case that $G = U(1)$ and for ground field $k = \mathbb{C}$ we may think of $\mathbf{B}U(1)$ as the category $\mathbb{C} Line \hookrightarrow \mathbb{C} Mod = Vect$ and think of the twisting cocycle $g$ as

$$
  X \stackrel{g}{\to} \mathbb{C}Line \hookrightarrow \mathbb{C}Mod
  \,.
$$

#### ... and $\infty$-sections as twisted $\infty$-functions  
 {#InfSections}

Regarded this way, the above discussion has a generalization to the case where the [[monoid]] $\mathbb{C}$ is replaced with any [[ring spectrum]] $R$ and we consider

$$
  X \stackrel{\tau}{\to} R Line \hookrightarrow R Mod
  \,.
$$

Twisted cohomology in terms of such morphisms $\tau$ is effectively considered in

* {#AndoBlumbergGepner10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in [[Jonathan Rosenberg]] et al. (eds.), _Superstrings, Geometry, Topology, and $C^\ast$-algebras_, volume 81 of _Proceedings of Symposia in Pure Mathematics_, 2009 ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))

and in unpublished work of [[Ulrich Bunke]] et al. For more on this see the discussion at _[[(∞,1)-vector bundle]]_.

More generally one can hence twist with maps

$$
  X \to Pic(R) \hookrightarrow R Mod
$$

into the [[Picard ∞-group]] of $R Mod$. 

See also at _[∞-group of units -- augmented definition](infinity-group+of+units#AugmentedDefinition)_.

### twisted K-theory 

In the context of [[generalized (Eilenberg-Steenrod) cohomology]] a coefficient object for [[cohomology]] is a [[spectrum]] $A$: the $A$-cohomology of a [[topological space]] $X$ with coefficients in $A$ is the set of homotopy classes of maps $X \to A$. For instance, as a model of the degree-$0$ space in the [[K-theory spectrum]] one can take $A = Fred(H)$, the space of Fredholm operators on a separable Hilbert space $H$. There is a canonical action on this space of the projective unitary group $G = P U(H)$ of $H$. Since $P U(H)$ has the homotopy type of an [[Eilenberg-Mac Lane space]] $K(\mathbb{Z},2)$, a $P U(H)$-[[principal bundle]] $P \to X$ defines a class $c \in H^3(X,\mathbb{Z})$ in [[Eilenberg-MacLane spectrum|ordinary integral cohomology]] (this may also be thought of as the class of a twisting [[bundle gerbe]]). The twisted K-theory (in degree $0$) of $X$ with that class as its twist is the set of homotopy classes of sections $X \to P \times_{P U(H)} Fred(H)$ of the associated bundle. 


### $G$-Actions on spectra  

The above example generalizes straightforwardly to the case that 

* $A$ is a [[spectrum|connective spectrum]], i.e. [[topological space]] that is an infinite [[loop space]]. (We need to assume a connective spectrum given by an infinite loop space so that $A$ can be regarded as living in the category of topologicall spaces along with the other objects, such as classifying spaces $\mathbf{B}G$ of nonabelian groups);

* with a (topological) [[group]] $G$ acting on $A$ by automorphisms and 

* a $G$-[[principal bundle]] $P \to X.$ 

In this case there is an established definition of [[generalized (Eilenberg-Steenrod) cohomology]] with coefficients $A$ _twisted_ by a $G$-[[principal bundle]] as follows.

From the $G$-[[principal bundle]] $P \to X$ we obtain the associated $A$-bundle $P \times_G A \to X$. Then a twisted $A$-cocycle on $X$ is defined to be a [[section]] $X \to P \times_G A$ of this associated bundle. The collection of homotopy classes of these sections is the _twisted $A$-cohomology of $X$_ with the twist specified by the class of $P$.

This is the definition of twisted cohomology as it appears for instance essentially as definition 22.1.1 of the May&#8211;Sigursson reference below (when comparing with their definition take their $G$ to be the trivial group and identify their $\Gamma$ and $\Pi$ with our $G$).

It is clearly a particular case of the general definition of twisted cohomology given above:
 
* the $(\infty,1)$-topos $\mathbf{H}$ is the $(\infty,1)$-category of [[Top]] of topological spaces

* the object $B$ is the [[delooping]] $\mathbf{B}G$ of the [[group]] $G$.

* the object $\hat{B}$ is the homotopy quotient $A//G\simeq \mathbf{E}G\times_G A$.

* the twisting cocycle $c$ is the element in $\mathbf{Top}(X,\mathbf{B}G)$ defining the principal $G$-bundle $P\to X$.

Indeed, $B$ is pointed, we have a fibration sequence
$$
A \to A//G \to \mathbf{B}G
$$
and the homotopy pullback
$$
  \array{
    P_A &\to& {A//G}
     \\
     \downarrow && \downarrow{f}
     \\ 
     X  &\stackrel{c}{\to}& \mathbf{B}G
  }\,
$$
is the $A$-bundle $P\times_G A\to X$.

The obstruction problem described by this example reads as folllows:

*  the obstruction to lifting a ("nonabelian" or "twisted") $A//G$-cocycle $g : X \to A//G$ to an $A$-cocycle $\hat g : X \to A$ is its image $\delta g $ in first $G$-cohomology  $\delta g \in H^1(X,G) :=\pi_0 \mathbf{Top}(X, \mathbf{B} G)$.

Read the other way round it says:

* $A$-cocycles are precisely those $G$-twisted $A$-cocycles whose twist vanishes.


+-- {: .num_remark}
###### Remark

Since the associated bundle $P \times_G A$ is in general no longer itself a spectrum, twisted cohomology is not an example of [[generalized (Eilenberg-Steenrod) cohomology|generalized Eilenberg-Steenrod cohomology]]. 

To stay within the spectrum point of view, May&#8211;Sigurdsson suggested that twisted cohomology should instead be formalized in terms of _[[parameterized homotopy theory]]_, where one thinks of $P \times_G A$ as a [[parameterized spectrum|parameterized family of spectra]]. 

=--







### Group cohomology with coefficients in a module 

Some somewhat trivial examples of this appear in various context. For instance [[group cohomology]] on a group with coefficients in a nontrivial module can be regarded as an example of twisted cohomology. See there for more details.

Compare this to the example below of cohomology "with local coefficients". It is the same principle in both cases.



### Twisted bundles


To get a feeling for how the definition does, it is 
instructive to see how for the fibration sequence coming from an ordinary central extension $K \to \hat G \to G$ of ordinary groups as

$$
  \mathbf{B}\hat G \to \mathbf{B}G \stackrel{\omega}{\to}
  \mathbf{B}^2 K
$$

classified by a [[group cohomology|group 2-cocycle]] $\omega$, $c$-twisted $\hat G$-cohomology produces precisely the familiar notion of [[twisted bundles]], with the twist being the lifting [[gerbe]] that obstructs the lift of a $G$-bundle to a $\hat G$-bundle.

This is also the first example in the list
in the last section of

* [[schreiber:Background fields in twisted differential nonabelian cohomology|Background fields in twisted differential nonabelian cohomology]]

and contains examples that are of interest in the wider context of [[string theory]].

See also [Twisted Differential String- and Fivebrane-Structures](http://golem.ph.utexas.edu/category/2009/03/twisted_differential_string_an.html).




### Cohomology with local coefficients 

What is called **cohomology with local coefficients** is twisted cohomology with the twist given by the class represented by the universal cover space of the base space, which is to say: by the action of the fundamental group of the base space.

In the classical case of ordinary cohomology, C. A. Robinson in 1972 constructed a _twisted_ $K(\pi,n)$,
denoted $\tilde K(\pi,n)$, so that, for nice spaces,
the cohomology with local coefficients $\tilde H^n(X,\pi)$
with respect to a homomorphism $\varepsilon:\pi_1(X)\to Aut(\pi)$ is 
given by homotopy classes of maps $X\to \tilde K(\pi,n)$ compatible with $\varepsilon.$

More generally, for any space $X$, let $A$ be a coefficient object that is equipped with an action of the first [[fundamental group]] $\pi_1(X)$ of $X$. (Such an action is also called an $A$-valued [[local system]] on $X$).

Then there is the [[fibration sequence]]

$$
  A \to A//\pi_1(X) \to \mathbf{B} \pi_1(X)
$$ 

of this action. 

Notice that there is a canonical map $c : X \to \mathbf{B} \pi_1(X)$, the one that classifies the universal cover of $X$.

Then **$A$-cohomology with local coefficients** on $X$ is nothing but the $c$-twisted $A$-cohomology of $X$ in the above sense.

#### Effective computation of cohomology with local coefficients

By _effective_, we mean involving as much as possible only calculations within finite dimensional linear algebra. For definiteness, we work in the smooth context and require the locally constant sheaf $\mathcal{A}$ to have stalks of finite dimensional vector spaces over a field $k$ ($\mathbb{R}$ or $\mathbb{C}$). Let $X$ be a connected $n$-dimensional manifold. The sheaf $\mathcal{A}$ can then be seen as the sheaf of germs of locally constant sections of a vector bundle $A\to X$ endowed with a flat connection $\nabla$. The fibers of $A$ are isomorphic with the stalks of $\mathcal{A}$, all of which are isomorphic to some finite dimensional vector space $\bar{A}$. Let $\tilde{X} \to X$ denote the universal cover of $X$ and $\pi = \pi_1(X)$ its fundamental group. It is well known that $\pi$ acts by [[deck transformation]] diffeomorphisms on $\tilde{X}$ and also induces a [[holonomy]] representation $\rho\colon \pi \to \mathbf{Aut}(\bar{A})$ on $\bar{A}$.

Consider the vector bundles $\Lambda^p X \otimes_X A$, where $\Lambda^p X$ is the bundle of differential $p$-forms, with $\Omega^p_A(-)$ denoting the sheaf of its sections (differential forms _twisted_ by $A$). Let $d_\nabla \colon \Omega^p_A \to \Omega^{p+1}_A$ denote the correspondingly twisted de Rham differential, defined by the property that
\[ d_\nabla(\omega \otimes a) = d\omega \otimes a + (-1)^{|\omega|} \omega \wedge \nabla a , \]
where $d$ is the ordinary de Rham differential, $\nabla a$ is seen as a section of $\Lambda^1 X \otimes_X A$, and with the wedge operation acting in the obvious way. The complex of sheaves $(\Omega^\bullet_A(-),d_\nabla)$ is then a [[soft|soft sheaf]] resolution of the sheaf $\mathcal{A}$ of locally constant sections of $A$. Its cohomology $H^p(X;A,\nabla) = H^p(\Omega^\bullet_A(X),d_\nabla)$ is then isomorphic to the sheaf cohomology of $X$ with coefficients in the locally constant sheaf $\mathcal{A}$, $H^p(X,\mathcal{A}) \simeq H^p(X;A,\nabla)$.

Now, the bundle $A\to X$ and the connection $\nabla$ both pull back to the universal covering space $\tilde{X}$, that is to $\tilde{A} \to \tilde{X}$ and $\tilde{\nabla}$. Since now $\tilde{X}$ is simply connected, we can globally trivialize this bundle as $\tilde{A} \simeq \tilde{X} \times \bar{A}$ and $\tilde{\nabla}$ to the trivial connection thereon. Similarly, the structure of the sheaf of twisted differential forms can be simplified to $\Omega^p_{\tilde{A}}(-) \simeq \Omega^p(-) \otimes \bar{A}$, with the action of the twisted de Rham differential given by $d_{\tilde{\nabla}} (\omega \otimes \bar{a}) = d\omega \otimes \bar{a}$. This observation allows us to conclude that, on the universal covering space, we have the isomorphism $H^p(\tilde{X}; \tilde{A},\tilde{\nabla}) \simeq H^p(\tilde{X}) \otimes \bar{A}$, where $H^p(\tilde{X})$ denotes the ordinary de Rham cohomology.

The pull back along a deck transformation diffeomorphism, induces a linear action of $\pi$ on forms $\Omega^p(\tilde{X})$. Combined with the holonomy representation of $\pi$ on $\bar{A}$, this defines a representation of $\pi$ on $\Omega^p_{\tilde{A}}(X)$. Let $\Omega^p_{\tilde{A}}(\tilde{X})^\pi \subseteq \Omega^p_{\tilde{A}}$ denote the subspace of twisted forms that is invariant under the action of $\pi$. It is not hard to notice the isomorphism of complexes $(\Omega^\bullet_\tilde{A}(\tilde{X})^\pi, d_{\tilde{\nabla}}) \simeq (\Omega^\bullet_A(X), d_\nabla)$ and hence of their cohomologies, $H^p(X; A,\nabla) \simeq H^p(\Omega^\bullet_{\tilde{A}}(\tilde{X})^\pi, d_{\tilde{\nabla}})$. Furthermore, the action of $\pi$ on $\Omega^p_{\tilde{A}}(\tilde{X})$ commutes with the differential $d_{\tilde{\nabla}}$ and hence induces an action on $H^p(\tilde{X}; \tilde{A},\tilde{\nabla}) \simeq H^p(\tilde{X}) \otimes \bar{A}$, where $\pi$ also acts in the obvious and compatible way on each tensor factor. Let $(H^p(\tilde{X})\otimes \bar{A})^\pi$ denote the corresponding $\pi$-invariant subspace.

+-- {: .num_prop}
###### Proposition

Suppose that there exists a decomposition $\Omega^p_{\tilde{A}}(\tilde{X}) \simeq \Omega^p_{\tilde{A}}(\tilde{X})^\pi \oplus \Omega^p_{\tilde{A}}(\tilde{X})^{\hat{\pi}}$ as representations of $\pi$, with $\Omega^p_{\tilde{A}}(\tilde{X})^{\hat{\pi}}$ having no $\pi$-invariant subspace. Then we have the following isomorphism for each $p$: $H^p(X,\mathcal{A}) \simeq (H^p(\tilde{X})\otimes \bar{A})^\pi$.

=--

Whether the decomposition hypothesis actually holds may depend on the properties of the group $\pi$. For instance, it does hold if $\pi$ is compact (finite, in particular). Other cases, have to be examined individually.

+-- {: .proof}
###### Proof

Start with the short exact sequence of complexes
\[ 0 \to \Omega^\bullet_{\tilde{A}}(\tilde{X})^\pi
  \to \Omega^\bullet_{\tilde{A}}(\tilde{X})
  \to \Omega^\bullet_{\tilde{A}}(\tilde{X})^{\hat{\pi}}
  \to 0 . \]
The corresponding long exact sequence in cohomology is equivalent to the short exact sequences
\[ 0 \to H^p(X,\mathcal{A})
  \to H^p(\tilde{X}) \otimes \bar{A}
  \to H^p(\Omega^\bullet_{\tilde{A}}(\tilde{X})^{\hat{\pi}}, d_{\tilde{\nabla}})
  \to 0 \]
for each value of $p$. The reason that all the connecting maps in the long exact sequence are zero is representation theoretic, since all the relevant maps are $\pi$-equivariant. Since, $H^{p+1}(X,\mathcal{A})$ carries a trivial representation by $\pi$, while the $H^p(\Omega^\bullet_{\tilde{A}}(\tilde{X})^{\hat{\pi}}, d_{\tilde{\nabla}})$ representation has no $\pi$-invariant subspace, by [[Schur's lemma]], the only equivariant map from the latter to the former is zero. From the same observation, we easily see that the inclusion of $H^p(X,\mathcal{A})$ must coincide with the $\pi$-invariant subspace $(H^p(\tilde{X}) \otimes \bar{A})^\pi$.

=--

The presentation of cohomology of $X$ with local coefficients $\mathcal{A}$ as $\pi$-invariant de Rham cohomology of the universal covering space $\tilde{X}$ twisted by the holonomy representation on the stalk $\bar{A}$ is originally due to ([Eilenberg 47](#Eil47)). It is also discussed in Chapter VI of ([Whitehead 78](#Whit78)). The idea to look at the $\pi$-invariant subspace of the twisted de Rham cohomology of the universal covering space scan be found in an answer by [Peter Michor](#MichorMO) on [MathOverlflow](http://mathoverflow.net/).

The above result can be seen as an effective way to compute the sheaf cohomology groups $H^p(X,\mathcal{A})$ since all it requires is the knowledge of the following finite dimensional representations of the fundamental group $\pi = \pi_1(X)$: the deck transformations on the de Rham cohomology $H^k(\tilde{X})$ of the covering space, and the holonomy representation on a typical stalk $\bar{A}$ of the locally constant sheaf $\mathcal{A}$. Obtaining the invariant subspace of their tensor product can then be done using usual representation theory methods, which involve only finite dimensional linear algebra. Unfortunately, it appears that the requirement that $\pi$ is finite is rather important for the argument. It is not entirely clearly how to proceed if, for instance $\pi = \mathbb{Z}$ or is non-abelian and infinite.

## Related entries

* [[local coefficient bundle]]

* [[twisted Umkehr map]]

* [[twisted differential cohomology]]

* [[relative cohomology]]

* [[twisted equivariant cohomology]]

* <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos+--+structures#TwistedCohomology">twisted cohomology</a> in [[cohesive (∞,1)-topos -- structures]]

* [[twisted ordinary cohomology]], [[twisted K-theory]], [[twisted tmf]]

**Examples**

* [[twisted ordinary cohomology]], [[twisted Bredon cohomology]]

* [[twisted K-theory]], [[twisted equivariant K-theory]]

* [[twisted Cohomotopy]]

* [[twisted equivariant cohomology]]

## References 

### General

The case of $\pi_1(X)$-twisted [[ordinary cohomology]]:

* M. Bullejos, E. Faro, M. A. Garc&iacute;a-Mu&ntilde;oz, _Homotopy colimits and cohomology with local coefficients_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 44 no. 1 (2003), p. 63-80 ([numdam:CTGDC_2003__44_1_63_0](http://www.numdam.org/item?id=CTGDC_2003__44_1_63_0))

The case of twisted [[generalized (Eilenberg-Steenrod) cohomology]] twisted by a $G$-[[principal bundle]]:

* [[Peter May]], [[Johann Sigurdsson]], Section 22.1 of: _[[Parametrized Homotopy Theory]]_,  Mathematical Surveys and Monographs, vol. 132, AMS 2006 ([ISBN:978-0-8218-3922-5](https://bookstore.ams.org/surv-132), [arXiv:math/0411656](https://arxiv.org/abs/math/0411656), [pdf](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))

* [[Chris Douglas]], _Twisted stable homotopy theory_ PhD thesis 2005 ([dspace:1721.1/7582](http://dspace.mit.edu/handle/1721.1/7582))

 
This in turn is based on the definition of twisted K-theory given in 

* [[Michael Atiyah]] and [[Graeme Segal]], _Twisted K-theory_, Ukr. Mat. Visn., 1(3):287&#8211;330, 2004. <http://front.math.ucdavis.edu/0407.5054>

Details on Larmore's work on twisted cohomology are at

* [[Larmore twisted cohomology]].

The abstract discussion of twisted nonabelian cohomology in $\infty$-toposes is in 

* {#NikolausSchreiberStevenson12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]],  _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_
  


The abstract discussion of twisted ES-type cohomology in the [[stable (infinity,1)-category of spectra]] is in

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics 81, American Mathematical Society 2010 ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004), [ISBN:978-0-8218-4887-6](https://bookstore.ams.org/pspum-81))
 

* {#ABGHR14} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _An $\infty$-categorical approach to $R$-line bundles, $R$-module Thom spectra, and twisted $R$-homology_, Journal of Topology Volume 7, Issue 3 2014 Pages 869&#8211;893  ([arXiv:1403.4325](http://arxiv.org/abs/1403.4325), [doi:10.1112/jtopol/jtt035](https://doi.org/10.1112/jtopol/jtt035))


The presentation of cohomology with local coefficients in terms $\pi_1$-equivariant de Rham cohomology on the universal covering space is discussed in

* {#Eil47} [[Samuel Eilenberg]], _Homology of spaces with operators I_, Trans. Amer. Math. Soc. 6 (1947), 378-417. ([doi](http://dx.doi.org/10.1090/S0002-9947-1947-0021313-4))
 

* {#Whit78} [[George Whitehead]], *Elements of homotopy theory*, Springer-Veriag, 1978.
 
* [Peter Michor](http://mathoverflow.net/users/26935/peter-michor), [answer](http://mathoverflow.net/a/129246/2622) to MathOverflow question [_de Rham cohomology and flat vector bundles_](http://mathoverflow.net/q/129246), (version: 2013-04-30).
 {#MichorMO}


### Chronology of literature on twisted cohomology 


The oldest meaning of twisted cohomology is that of **cohomology with local coefficients** (see above).

For more on the history of that notion see

* [[History of cohomology with local coefficients]]

In the following we shall abbreviate

* tc = twisted cohomology

Searching MathSciNet for _twisted cohomology_ led to the following chronology: It missed older references in which the phrase was not used but the concept was in the sense of local coefficient systems &#8211; ancient and honorable.

Most notably missing are

* [[Kurt Reidemeister]] (1938) Topologie der Polyeder und kombinatorische 

Topologie der Komplexe_, Mathematik und ihre Anwendungen in 
Physik und Technik,_(But note that reprints appear, sans reviews. There is a short English and longer German review on Zentralblatt)

* [[Norman Steenrod]] (1942,1943)

* Olum (thesis 1947, published 1950)


Next come several that involve twisted differentials more generally.

Few are in terms of homotopy of spaces

tc ops should be treated as a single phrase &#8211; it may be that the ops are twisted, not the cohomology

* 1966 McClendon thesis &#8211; summarized in

* 1967  Emery Thomas  tc ops

* 1967 Larmore tc ops 

* 1969 McClendon tc ops

* 1969 Larmore tc

* 1970 Peterson tc ops

* 1971 McClendon tc ops

* 1972 Deligne Weil conjecture for K3 tc &#8211; meaning?

* 1972 Larmore tc

* 1973 Larmore and Thomas tc

* 1973 Larmore tc

* gap

* 1980 Coelho & Pesennec tc

* 1980 Tsukiyama sequel to McClendon

* 1983 Coelho & Pesennec tc

* 1985 Morava but getsted at 1975 ??

* 1986 Fried tc

* 1988 Baum & Connes ??

* 1989 Lott torsion

* 1990 Dwork ??

* 1993 Gomez&#8211;Tato tc minimal models

* 1993 Duflo & Vergne diff tc

* 1993 Vaisman tc and connections

* 1993 Mimachi tc and holomorphic

* 1994 Kita tc and intersection

* 1995 Cho, Mimachi and Yoshida tc and configs

* 1995 Cho, Mimachi tc and intersection

* 1996 Iwaski and Kita tc de rham

* 1996 Asada nc geom and strings

* 1997 H Kimura tc de Rham and hypergeom

* 1998 [[Michael Farber]], [[Gabriel Katz]], [[Jerome Levine]], [Morse theory of harmonic forms](http://www.sciencedirect.com/science/article/pii/S0040938397827309), Topology, (Volume 37, Issue 3, May 1998, Pages 469&#8211;483)

* 1998 Knudson tc SL_n

* 1998 Morita  tc de Rham

* 1999 Kachi, Mtsumoto, Mihara tc and intersection

* 1999 Hanamura & Yoshida Hodge tc

* 1999 Felshtyn & Sanchez&#8211;Morgado Reidemeister torsion

* 1999 Haraoka hypergeom

* 2000 Tsou & Zois tc de rham

* 2000 Manea tc Czech

* 2001 Royo Prieto tc Euler

* 2001 Takeyama q-twisted

* 2001 Gaberdiel &Schaefr&#8211;Nameki tc of Klein bottle

* 2001 Iwaskai  tc deRham

* 2001 Proc Rims tc and DEs and several papers in this book

* 2001 Knudson tc SL_n

* 2001 Royo Prieto tc as $d+k\wedge$

* 2001 Barlewtta & Dragomir tc and integrability

* 2002 Lueck $L^2$

* 2002 Verbitsky HyperKahler, torsion, etc

* 2003 Etingof & Grana tc of Carter, Elhamdadi and Saito

* 2003 Cruikshank tc of Eilenberg

* 2003 various in Proc NATO workshop

* 2003 Dimca tc of hyperplanes

* 2004 Kirk & Lesch tc and index

* 2004 Bouwknegt, Evslin, Mathai tc and tK

* 2004 Bouwknegt, Hannbuss, Mathai tc in re: T-duality

* 2005 Bouwknegt, Hannbuss, Mathai tc in re: T-duality

* 2005 Bunke & Schick tc in re: T-duality

* 2006 Dubois tc and Reidemeister (elsewhere he considers twisted Reidemesiter)

* 2006 Bunke & Schick tc in re: T-duality

* 2006 Sati

* 2006 Atiyah & Segal tc and tK

* 2007 Mickelsson & Pellonpaa tc and tK

* 2007 Sugiyama in re: Galois and Reidemeister

* 2007 Bunke, Schick, Spitzweck tc in re: gerbes

* 2008 Kawahara hypersurfaces


[[!redirects twisted generalized cohomology]]

[[!redirects cohomology with local coefficients]]

[[!redirects twisted cohomology theory]]
[[!redirects twisted cohomology theories]]

