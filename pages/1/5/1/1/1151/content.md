+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea ## 

There are various different-looking definitions of the general notion of _cohomology_ in different contexts, some familiar, some more exotic. 

The claim is all these notions of cohomology are special cases of -- and in many instances special concrete _models_ for -- the following general idea:

Cohomology is something associated to a given [[(∞,1)-topos]] $\mathbf{H}$. For $X, A$ two objects of $\mathbf{H}$, the **cohomology of $X$ with coefficients in $A$** is the set of connected components of the [[∞-groupoid]] of morphisms from $X$ to $A$ in $\mathbf{H}$:

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$


+-- {: .standout}

**Slogan.**

Thousands of definitions of notions of cohomology and its variants. From the [[nPOV]], just a single concept: an [[derived hom space|∞-categorical hom-space]] in an [[(∞,1)-topos]]. 

=--

A non-technical introduction to some concepts in cohomology from this perspective is at 

* [[motivation for sheaves, cohomology and higher stacks]].

The following section 

* [Overview](#Overview)

gives a tour through the zoo of cohomology theories traditionally known, indicating how they all fit into this picture. Then the section

* [Definition](#Definition)

gives the very general formal definition and discusses very general properties of and constructions in cohomology theory, such as the terminology of _[[cocycle]]s_ and _coboundaries_ of _[[principal ∞-bundle|objects classified]]_ by cohomology, of _[[characteristic class]]es_ of these objects, of [[Postnikov tower in an (infinity,1)-category|Postnikov towers]] and [[Whitehead tower in an (infinity,1)-topos|Whitehead towers]], and so on. In particular the section

* [Extra structure on cohomology](#ExtraStruc)

describes addtitional [[stuff, structure, property]] that may be present for certain choices of coefficient objects -- such as _gradings_ , [[cohomology group]]- and ring-structures -- and aspects of which are in different parts of the traditional literature often _required_ (differently) on cohomology.

The straightforward definition of cohomology in terms of mapping spaces in an [[(∞,1)-topos]] has some slight, but similarly straightforward, variants, notably that of _twisted cohomology_ (which includes other cases such as [[differential cohomology]]) and of [[equivariant cohomology]] (with its different flavors such as Borel-equivariant and [[Bredon cohomology]]). These are discussed in the section

* [Variants](#Variants)

before the next main section 

* [Examples](#Examples)

then starts going through concrete examples in detail. The reader uneasy with the abstract generality of our perspective is advised to skip ahead to this section and find from a long list of examples discussed his or her favorite 
traditional notion of cohomology and how it fits into the general structure. 

Finally we discuss _why_ the notion of cohomology is related to that of [[(∞,1)-topos]]es in 

* [Relation to (∞,1)-topos theory](#ToposTheory) .

Essentially nothing about this perspective on cohomology is really new, many aspects of it have been made explicit in the literature here and there. In fact, to some extent everything here is just an afterthought of the old seminal article

* [[Kenneth Brown]], _[[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]_ (1973),

in the light of fully fledged [[(∞,1)-topos|(∞,1)-topos theory]], of which it is effectively the seed, by noticing that this article secretly discusses precisely the [[homotopy category of an (infinity,1)-category|homotopy categories]] of [[hypercomplete (∞,1)-topos]]es. At the same time, to some extent everything here is also an afterthought of the theory of cohomology in [[category theory|1-categorical]] [[topos theory]] as reviewed for instance in

* [[Ieke Moerdijk]], _Classifying Spaces and Classifying Topoi_ , section I.4

by noticing that the constructions on [[simplicial object]]s in [[topos]]es used there secretly precisely compute the [[derived hom-space|(∞,1)-categorical hom-objects]] of an [[(∞,1)-topos]] as presented by the [[model structure on simplicial sheaves]] on the underlying site.

This and a list of other releated references and historical developments is given at

* [References](#References).


## Tour through notions of cohomology {#Overview}

The statement of the above slogan is well familiar for the special case that $\mathbf{H} = $ [[Top]] is the [[(∞,1)-topos]] of [[topological space]]s. In this context for instance for $A := K(\mathbb{Z}, n)$ an [[Eilenberg-MacLane space]], we have that for $X$ any topological space that

$$
  \pi_0 \mathbf{H}(X,K(\mathbb{Z},n)) = H^n(X,\mathbb{Z})
$$

coincides with the "ordinary" [[integral cohomology]] of $X$, modeled as its [[singular cohomology]].

This definition in [[Top]] alone already goes a long way. By the [[Brown representability theorem]] all cohomology theories that are called [[generalized (Eilenberg-Steenrod) cohomology]] theories are of this form, for $A$ a topological space that is part of a [[spectrum]]. This includes everything that is traditionally just called "a [[cohomology theory]]", such as [[K-theory]], [[elliptic cohomology]], [[tmf]], [[complex cobordism cohomology theory|complex cobordism]], etc.

Another big complex of notions of cohomology that on first sight maybe does not seem to fit into this pattern is [[abelian sheaf cohomology]]. Usually this is introduced and defined in the language of [[derived functor]]s. However, derived functors are nothing but a tool, or presentation, for encoding [[(∞,1)-categorical hom-space]]s such as $\mathbf{H}(X,A)$ in cases where $\mathbf{H}$ is [[presentable (∞,1)-category|presented]] by a [[homotopical category]] or [[model category]].

Indeed, it turns out that an old result from the 1960s, **Verdier's hypercovering theorem** effectively shows that what was introduced as [[abelian sheaf cohomology]] is really nothing but an instance of the above general setup. A particularly clear-sighted understanding of this fact was presented in 

* [[Kenneth Brown]], [[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]].

Therein Brown considers essnetially the [[model structure on simplicial presheaves]] -- which today is known to be one of the standard [[models for ∞-stack (∞,1)-toposes]] $\mathbf{H}$ -- rederives Verdier's hypercovering theorem and shows that ordinary [[abelian sheaf cohomology]] is indeed nothing but $\pi_0 \mathbf{H}(X,A)$ in such an [[(∞,1)-topos]], for the special case that the [[simplicial presheaf]] $A$ happens to be objectwise in the image of the [[Dold-Kan correspondence]], i.e. for the special case that $A$ is a _maximally abelian_ [[∞-stack]].

One can then understand various "cohomology theories" as nothing but tools for _computing_ $\pi_0 \mathbf{H}(X,A)$ using the known presentations of [[(∞,1)-categorical hom-space]]s: for instance [[?ech cohomology]] computes these spaces by finding cofibrant models for the domain $X$, called [[?ech nerve]]s. Dual to that, most texts on [[abelian sheaf cohomology]] find fibrant models for the codomain $A$: called injective resolutions. Both algorithms in the end compute the same intrinsically defined $(\infty,1)$-categorical hom-space.

In other words, [[abelian sheaf cohomology]] is of the exact same nature as the familiar cohomology of [[topological space]]s (and hence of [[spectrum|spectra]]) if only we switch from the archetypical [[(∞,1)-topos]] [[Top]] to a more general [[(∞,1)-category of (∞,1)-sheaves|∞-stack (∞,1)-topos]]. And abelian sheaf cohomology in turn subsumes many special cases, such as [[Deligne cohomology]], [[deRham cohomology]], [[etale cohomology]], [[crystalline cohomology]], [[syntomic cohomology]], etc. You name it.

But this also shows that abelian sheaf cohomology itself is just a very special case of cohomology in an $\infty$-stack $(\infty,1)$-topos: the [[stable (infinity,1)-category|stable]] or _maximally abelian_ case. For coefficient objects $A \in \mathbf{H}$ that are not maximally abelian (for instance not degreewise in the image of the [[Dold-Kan correspondence]] for sheaf cohomology) the cohomology of an $\infty$-stack topos is a [[nonabelian cohomology]]. 

Often in the literature the term "nonabelian cohomology" is restricted to [[nonabelian group cohomology]], which is indeed one special case. Another familiar special case is cohomology in [[Top]] with coefficients in the [[classifying space]] $\mathcal{B}G$ of a (possibly nonabelian) [[group]] $G$ (which is of course not part of a [[spectrum]], in general). This degree 1 nonabelian cohomology classifies $G$-[[principal bundle]]s. 

If the group $G$ here is generalized to a (possibly nonabelian) [[2-group]], the coefficient object $\mathcal{B}G$ gives degree 2 nonabelian cohomology in [[Top]], which classifies nonabelian [[gerbe]]s and, more generally, [[principal 2-bundle]]s. The celebrate treatise by Giraud _Cohomologie non ab&#233;lienne_ is concerned with this case. In fact, Giraud considered [[gerbe]]s on [[stack]]s and hence was implicitly really computing cohomology in a [[stack]] [[2-topos]] with both the domain and the coefficient object allowed to have nontrivial [[homotopy group (of an infinity-stack)|homotopy groups of stacks]] in degree 2.

Conceptually, with [[higher topos theory]] in hand, there is no problem in generalizing nonabelian cohomology and its relation to gerbes and principal bundles further from stacks to [[∞-stack]]s. For instance, while the discussion of [[spin group|spin structure]] on a [[space]]/[[∞-stack]] requires a 1-stack coefficient object and classifies principal bundles, and the discussion of [[string structure]] requires a 2-stack coefficient object and classifies [[gerbe]]s and [[principal 2-bundle]]s, the next case of [[fivebrane group|fivebrane structure]] requires 6-stack coefficient objects and classifies principal 6-bundles. Generally, we may speak of [[principal ∞-bundle]]s in any [[(∞,1)-topos]] $\mathbf{H}$: these are nothing but the [[homotopy fiber]]s of the corresponding ("nonabelian") [[cocycle]]s, which are just morphisms $X \to A$ in $\mathbf{H}$.

Various other notions of cohomology are special cases of this. For instance [[group cohomology]] is nothing but the cohomology in $\mathbf{H} = $ [[∞Grpd]] on objects $X = \mathbf{B}G$ that are [[delooping]]s of [[group]]s. What is called [[nonabelian group cohomology]] is nothing but the general case of this where there is no restriction on the coefficient object $A$. Here we can once again replace $\infty Grpd$ -- which is the $(\infty,1)$-topos of $\infty$-stacks on the point -- by a more general $\infty$-stack $(\infty,1)$-topos. For instance if we take the underlying [[site]] to be [[Diff]], the category of smooth [[manifold]]s, then the objects of $\mathbf{H} = Sh_{(\infty,1)}(Diff)$ are [[Lie ∞-groupoid]]s. Their cohomology is generalized group cohomology that knows about smooth structure: _smooth group cohomology_ . In this context for instance one can give cohomological interpretations of smooth realizations of the [[string 2-group]] or the [[fivebrane 6-group]].

Conversely, given an unconstrained (unstable) [[(∞,1)-topos]] $\mathbf{H}$ with its general notion of [[nonabelian cohomology]], one can systematically find its [[stable (∞,1)-category|stable]] or _abelian_ content by considering objects that are components of [[spectrum object]]s in $\mathbf{H}$. These form the [[stabilization]] of $\mathbf{H}$ to a [[stable (∞,1)-category]]. 

An example of this is [[motivic cohomology]] and motivic [[homotopy]]: this is the cohomology given by [[derived hom space|(∞,1)-categorical hom spaces]] in the [[(∞,1)-topos]] of [[∞-stack]]s on the [[Nisnevich site]]: motivic cohomology proper is that where the coefficient objects happen to be components of [[spectrum object]]s and [[A1-homotopy theory|A1-homotopy invariant]]. For instance the [[Chow group]]s are precisely the cohomology in this sense with coefficients in the [[Eilenberg-MacLane object]]s of this [[(∞,1)-topos]]. From this perspective, hom-spaces into more general objects in this $(\infty,1)$-topos could be called _nonabelian motivic cohomology_ . 

A noteworthy example for the restriction to homotopy invariant objects in an $(\infty,1)$-topos, hence to its [[homotopy localization]], is the internal cohomology of the $(\infty,1)$-topos of $\infty$-stacks on the [[site]] [[Top]] (topological $\infty$-stacks): when restricted to homotopy local objects this turns out to be just the ordinary cohomology in [[Top]]. This is described in more detail at [[topological ∞-groupoid]].

There are some slight variations on the theme that cohomology is all about connected components of hom-spaces in [[(∞,1)-topos]]es: by looking at [[homotopy fiber]]s of such  [[derived hom space|(∞,1)-categorical hom-spaces]] instead, one finds [[twisted cohomology]]. The most prominent example is [[twisted K-theory]]: in degree 0 this is the study of the homotopy fiber of the morphism of $(\infty,1)$-categorical hom-space $Top(-,\mathcal{B}PU(n)) \to Top(-,\mathcal{B}^2 U(1))$ that sends a projective [[unitary group|unitary]] [[principal bundle]] (hence its [[associated bundle|associated]] [[vector bundle]]) to the [[lifting gerbe]] for the lift of its structure group to the full [[unitary group]].

Another example of [[twisted cohomology]] is [[differential cohomology]]: differential cohomology refinements of abelian [[generalized (Eilenberg-Steenrod) cohomology]] theories with coefficient objects a [[spectrum]] $E$ is the study of the [[homotopy fiber]]s of the [[Chern character]] map $ch : \mathbf{H}(X,E) \to \Omega^\bullet_{dR}(X)\otimes \pi_\bullet(E)$ from $E$-cohomology to [[deRham cohomology]]. 
This classifies (abelian versions of) [[connection on a bundle|connections]] on the underlying bundles, for instance [[Simons-Sullivan structured bundle]]s (vector bundles with connection).

By generalizing the notion of [[Chern character]] to richer $(\infty,1)$-toposes, one obtains by the same token a notion of [[schreiber:differential cohomology in an (∞,1)-topos]] encoding connections on general [[principal ∞-bundle]]s and associated [[schreiber:∞-vector bundle]]s.



## Definition {#Definition}

We give now the very general definition of cohomology and describe very general properties of and very general constructions in cohomology theory. 

### General definition

Given an [[(∞,1)-topos]] $\mathbf{H}$, for any two [[objects]] $X$, $A$ of $\mathbf{H}$ we have the [[derived hom space|(∞,1)-categorical hom-space]] $\mathbf{H}(X,A)$ -- an [[∞-groupoid]]. For $H = Ho_{\mathbf{H}}$ the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathbf{H}$, its set of connected components is $\pi_0 \mathbf{H}(X,A) = Ho_{\mathbf{H}}(X,A)$.

* The [[objects]] $ (c : X \to A) \in \mathbf{H}(X,A)$ are 
  called **[[cocycle]]s** on $X$ with coefficients in $A$;

* if $A$ is understood to be equipped with the structure ${*} \to A$ of 
  a [[pointed object]], then the cocycle $X \to {*} \to A$ is the
  **trivial cocycle** $c_{triv}$;

* the [[morphism]]s $\lambda : c_1 \to c_2$ in $\mathbf{H}(X,A)$ are the
  **coboundaries**. Two cocycles connected by a coboundary 
  are **cohomologous**. (More specifically, a cocycle cohomologous to the
  trivial cocycle is called a coboundary.)

* the equivalence classes $[c] \in \pi_0 \mathbf{H}(X,A)$ of 
  cohomologous are the **cohomology classes**;

* the set of cohomology classes is the $A$-**cohomology set**

  $$
    H(X,A) := Ho_{\mathbf{H}}(X,A) = \pi_0 \mathbf{H}(X,A)
  $$

  of $X$.

* for $c \in \mathbf{H}(X,A)$ a cocycle on $X$ and 
  $k \in \mathbf{H}(A,B)$ a cocycle on $A$, the class of the composite
  cocycle
  
  $$
     [k(c)] := [X \stackrel{c}{\to} A \stackrel{k}{\to} B] \in H(X,B)
  $$

  is the **[[characteristic class]]** of $c$ with respect to $k$.

**Remark** Notice that there is **no notion of cochain** in this general setup. What are called _cochains_ are specifically components of certain specific [[model category|models]] for $\mathbf{H}(X,A)$. More on this in the section on [abelian cohomology](#abelian) below.

### Objects classified by cohomology

For $g : X \to A$ a cocycle, one says that its [[homotopy fiber]] $P \to X$ is the object **classified by the cohomology class*.

Such an object usually has the interpretation of a [[principal ∞-bundle]]. Special cases of this are [[principal bundles]], [[gerbes]], [[principal 2-bundles]], etc. If the domain object $X$ itself is a [[groupoid object in an (infinity,1)-category|group object]], then $P \to X$ is a [[group extension]]. For that reason in abelian cohomology $\mathbf{H}(X,A)$ is often denoted $Ext(X,A)$ and a [[cocycle]] is then called an [[Ext functor|Ext]].

### Characteristic classes

For $A \in \mathbf{H}$ some coefficient object and $\{c_n : A \to E_n\}$ a collection of [[cocycle]]s on the coefficient object with values in objects $E_n \in \mathbf{H}$ -- typically chosen to be [[Eilenberg-MacLane object]]s -- composition of morphism in $\mathbf{H}$ induces a map of cohomology [[∞-groupoid]]s

$$
  c_n : \mathbf{H}(X,A) \to \mathbf{H}(X,E_n)
$$

and hence of cohomology classes

$$
  c_n : H(X,A) \to H(X,E_n)
$$

that sends each $A$-cocycle $g$ to its **characteristic class** $c_n(g)$. Typically, for $P \to X$ is the [[principal ∞-bundle]] clasified by $g$ one speaks of the characteristic class $c_n(P)$ of this principal $\infty$-bundle.


### Extra structure on cohomology {#ExtraStruc}

Extra [[stuff, structure, property]] on the coefficient object $A$ will induce corresponding stuff, structure or property on the cohomology sets $H(X,A)$.

#### Gradings {#Grading}

##### Integer grading

In the case that the coefficient object $A$ admits $(n \in \mathbb{N})$ [[delooping]]s to objects $\mathbf{B}^n A$ one writes

$$
  H^n(X,A) := \pi_0 \mathbf{H}(X, \mathbf{B}^n A)
$$

and speaks of **$A$-cohomology in degree $n$**.

Similarly, [[loop space object|looping]] defines negative degree cohomology:

$$
  H^{-n}(X,A) := \pi_0 \mathbf{H}(X, \Omega^n A) 
  \,.
$$

Because [[loop space object]]s are defined by an $(\infty,1)$-[[pullback]] and the [[derived hom space|(∞,1)-categorical hom]] -- as any [[hom-functor]] -- preserves [[limit]]s in its second argument, this is the same as 

$$
  \begin{aligned}
    H^{-n}(X,A) &\simeq \pi_0 \Omega^n \mathbf{H}(X, A) 
    \\
     & \simeq \pi_n \mathbf{H}(X,A)
    \,.
  \end{aligned}
  \,.
$$

This means that all the non-positive degree cohomology identifies with the [[simplicial homotopy group|homotopy group]]s of the [[∞-groupoid]] $\mathbf{H}(X,A)$. 

##### Bigrading {#BiGrading}

If the underlying [[topos]] of $\mathbf{H}$ is a [[lined topos]], the line object $I$ canonically has the structure of an [[interval object]] and induces a [[cosimplicial object]] $\Delta_I : \Delta \to \mathbf{H}$ of _geometric_ $n$-simplices in addition to the _categorical_ standard cellular simplices. Accordingly there are then two differnt loop objects, 

* the **categorical 1-sphere** (or simplicial loop ) $S^1 = \Delta^1/\partial \Delta^1$;

* the **geometric 1-sphere** $S^1_I = \Delta_I^1/ \partial \Delta_I^1$.

> (Warning: one has to be careful with different ways how to interpret $\Delta_I^1/ \partial \Delta_I^1$. More later. See the example of [[motivic cohomology]].)

The notion of [[loop space object]] and of [[delooping]] have _geometric_ analogs in this case and so a second integer grading is induced on cohomology, now coming from the geometric loops.
Both gradings may be considered at once, which makes the cohomology theory bigraded:

$$
  H^{-p,-q}(X,A) := \pi_0 \mathbf{H}(X, \Omega^p \Omega^q_I A)
  \,.
$$

This bigrading is traditionally considered in [[motivic cohomology]] where the line object is that of [[A1-homotopy theory]], but the general construction depends only on the presence and choice of an [[interval object]].

+--{.query}
Marc: I am confused about the origin of the bigrading in motivic cohomology: despite the warning, I don't see how the geometric 1-sphere $\mathbb{G}_m$ is given by $S^1_I = \Delta_I^1/ \partial \Delta_I^1$. I'd interpret the latter as being the sheaf $\mathbb{A}^1/\{0,1\}$ which is equivalent to the _categorical_ sphere $S^1$, not to the geometric one. In fact I believe that in any site with interval that the two families of spheres given above coincide after I-localization, and that this explains why any sheaf of simplicial sets becomes equivalent to a sheaf of sets. Am I wrong?
=--

##### Exotic grading

In some cases one considers geometric spheres $S^V$ that do not necessarily arise from a single [[interval object]]. One can still follow the general procedure and define a corresponding graded cohomology

$$
  H^{V}(X,A) := \pi_0 \mathbf{H}(X, S^V A)
  \,.
$$

This is notably the standard case in [[Bredon cohomology|Bredon]] [[equivariant cohomology]] used in [[equivariant stable homotopy theory]], where the $S^V$ are one-point compactifications of [[representation]] [[vector space]]s of a [[group]] $G$.

+-- {: .query}

[[Urs Schreiber]]: I am still hoping that if we work hard enough, we can see that this is actually a special case of the above general construction somehow. Or else that we find a more systematic way to understand this "exotic" grading.

=--
 
#### Abelian and stable cohomology {#abelian}

Often the coefficient object $A \in \mathbf{H}$ for cohomology is taken to be indefinitely [[delooping|deloopable]] -- an $\infty$-[[loop space object]] -- or, more generally, a component of a [[spectrum object]] in the [[stabilization]] $Stab(\mathbf{H})$ of the [[(∞,1)-topos]] $\mathbf{H}$ to a [[stable (∞,1)-category]].

In terms of the [[stabilization]] [[adjunction]]

$$
  \mathbf{H} \stackrel{\stackrel{\Omega^\infty}{\leftarrow}}{\underset{\Sigma^\infty}{\to}}
  Stab(\mathbf{H})
$$

this means that $A$ is of the form 

$$
  A = E_n := \Omega^\infty \circ \Sigma^n E
$$

for some [[spectrum object]] $E$, and some [[integer]] $n$ (not necessarily a [[natural number]]).

One single such spectrum object this way yields a $\mathbb{Z}$-graded tower of cohomologies

$$
  H^n(X, E) := \pi_0 \mathbf{H}(X, \Omega^\infty \Sigma^n E)
$$

which taken together, denoted $H^\bullet(X,E)$ is called a [[cohomology theory]]. For the case that $\mathbf{H} =$ [[Top]] this special case of cohomology is called [[generalized (Eilenberg-Steenrod) cohomology]].

As above in the discussion of gradings, the same discussion goes through analogously in the presence of an [[interval object]] that induces a notion of geometric loops. Notably in [[motivic cohomology]] coefficient objects are taken to be stable with respect to both categorical and geometric looping and [[delooping]].

#### Cohomology groups and rings {#CohomGroup}

If $A$ happens to be a 
[[groupoid object in an (infinity,1)-category|group object]] 
in $\mathbf{H}$ then the cohomology _set_ naturally inherits the structure of a [[group]] and then $H(X;A)$ is called the
$A$-**[[cohomology group]]** of $X$.  If $A$ is at least an $E_2$ object, then $H(X;A)$ is abelian.

This is in particular necessarily the case if $A$ is a component of a [[spectrum object]] in abelian cohomology in the sense described above, i.e. of the form $\Omega^\infty \Sigma^n A'$.

If the corresponding [[spectrum object]] $A'$ in addition carries the structure of a [[ring]] &#8212; in which case it is a [[ring spectrum]] or [[E-∞ ring]] &#8212; then we speak of a [[multiplicative cohomology theory]] and the [[cohomology group]]s
$H^\bullet(X,A)$ form a graded [[ring]], the **cohomology ring** of $X$ with coefficients in $A$.




### Variants {#Variants}

#### Twisted cohomology

Given $A \in \mathbf{H}$ an object and $k : A \to B$ cocycle on $A$, classifying its [[homotopy fiber]] $C \to A$, the $A$-cohomology with specified $B$-[[characteristic class]] $[k]$ is $k$-**twised $C$-cohomology.

For the moment see

* [[twisted cohomology]]



#### Differential cohomology

A special type [[characteristic class]] is the [[Chern character]].
The [[twisted cohomology]] with respect to the Chern character is **differential cohomology**.

* [[differential cohomology|differential abelian cohomology]] 

* [schreiber:schreiber:differential cohomology in an (∞,1)-topos]]

#### Equivariant cohomology

Various related but different variations of cohomology are obtained by domain objects, or coefficient objects or both with [[action groupoid]]s of [[action]]s  by some [[groupoid object in an (infinity,1)-category|group object]], or by more general groupoids ("[[orbifold]]s").

For the moment see

* [[equivariant cohomology]]

for more details.

#### Relative cohomology

For the moment see 

* [[relative cohomology]]


### Homotopy

By abstract [[duality]], cohomology is dual to [[homotopy (as an operation)]]:

the cohomology _of_ $X$ with coefficients in $A$ is the [[homotopy]] of $A$ with co-coefficients in $X$.

Notably, when $\mathbf{H}$ is a [[lined topos]] there is for 
each $n \in \mathbb{N}$ a [[sphere object]] $S^n$ in $\mathbf{H}$.

For any $A \in \mathbf{H}$ the set $H(S^n, A)$ is equivalently

1. the $A$-cohomology of $S^n$.

2. the $n$th homotopy group of $A$.

One could argue that a more suitable term for cohomology is [[cohomotopy]]. Unfortunately, of course, this term is traditonally used only for a very special case of what it should mean generally...





## Examples {#Examples}

### Long list of examples

Classes of special cases of cohomologies with their own entries include

* [[chain homology and cohomology]]

* [[groupoid cohomology]]

  * [[group cohomology]]

  * [[nonabelian group cohomology]]

  * [[cohomology of a category]]

* [[generalized (Eilenberg-Steenrod) cohomology]]

  * [[integral cohomology]]

  * [[K-theory]]
  
  * [[elliptic cohomology]]
  
  * [[tmf]]

  * [[complex cobordism cohomology theory|complex cobordism]]

* [[abelian sheaf cohomology]]

  * [[Deligne cohomology]]

    * [[de Rham cohomology]]

  * [[etale cohomology]]

  * [[crystalline cohomology]]

  * [[syntomic cohomology]]

* [[motivic cohomology]]

* [[nonabelian cohomology]]

  * [[principal bundle]]

  * [[gerbe]]/[[principal 2-bundle]]

  * [[principal ∞-bundle]]
 
  * [[orientation]], [[spin structure]], [[string structure]], [[fivebrane structure]]

* [[cohomology with constant coefficients]]

* [[cohomology with a local system of coefficients]]

* [[Hochschild cohomology]] / [[cyclic cohomology]]

* [[?ech cohomology]]

* [[hypercohomology]]

* [[twisted cohomology]]

* [[equivariant cohomology]]

* [[differential cohomology]], [[Chern-Weil theory]]

  * [[schreiber:differential cohomology in an (∞,1)-topos]]

  * [[∞-Chern-Weil theory]]


### Chain cohomology {#ChainCohomology}

The probably most familiar kind of cohomology is that of a [[cochain complex]] dual to a [[chain complex]]. 

Using the [[Dold-Kan correspondence]] [[chain complex]]es are understood as components of strict [[spectrum object]]s in the archetypical [[(∞,1)-topos]] [[∞Grpd]] of [[∞-groupoid]]s: namely those [[∞-groupoid]]s with the structure of a _[[group object|strict]]_ abelian [[groupoid object in an (∞,1)-category|group object]]: as [[Kan complex]]es these are abelian [[simplicial group]]s.


This way ordinary chain cohomology is seen to be a special case of general cohomology in $\mathbf{H} = $ [[∞Grpd]]. A more detailed discussion of how from this perspective the usual formulas for cochains and cocycles appear is at 

* [[chain homology and cohomology]].

### Cohomology in $Top$

The archetypical example for [[nonabelian cohomology]] theory is the [[(∞,1)-topos]] $H = $ [[Top]], the [[(∞,1)-category]] of [[topological spaces]]. For $X$ and $A$ two topological spaces, the cohomology classes of $X$ with values in $A$ are the homotopy classes of continuous maps $X \to A$. For $A = K(a,n)$ an [[Eilenberg-Mac Lane space]] with $a$ an abelian group this reproduces "ordinary cohomology" of spaces. For $n \gt 1$ this special case happens to be actually abelian.
 For $A = B G$ a [[classifying space]] of a topological [[group]] $G$, this reproduces degree 1 [[nonabelian cohomology]] $H^1(X,G)$. In general, for $A$ an $n$-type, $H(X,A)$ is topological degree-$n$ [[nonabelian cohomology]].

* The archetypical example for abelian cohomology theory is the [[stable (∞,1)-topos]] $H = $ [[Spec]], the [[stable (∞,1)-category]] of [[spectrum|spectra]]. This is the case in the literature often addressed as [[generalized cohomology]], since it generalizes the entities specified by the Eilenberg--Steenrod axioms. But really, the general concept of cohomology is more general than this "generalized cohomology". 

  * "ordinary" cohomology is cohomology with coefficients in the [[Eilenberg-MacLane spectrum]]

  * K-theory is cohomology with coefficients in the [[K-theory spectrum]]

  * elliptic cohomology is somehow subsumes by cohomology with coefficients in [[tmf]].


> some left-over material, to be merged...

> Ordinary nonabelian cohomology in degree 1 of a 'nice' topological space $X$ with values in a discrete (and possibly nonabelian) group $G$ can be defined as  the pointed set of homotopy classes of maps of topological spaces from $X$ into the classifying space $B G$. The content of *nonabelian cohomology* is the generalization of this statement to cohomology in higher degree. The content of general  nonabelian *differential* cohomology is moreover the generalization of nonabelian cohomology to generalized spaces with extra structure, in particular with smooth structure.

>Henceforth we will refer to * spaces * meaning perhaps some generalization or restriction, e.g. smooth spaces, and occasionally specify the nature of the generalization.   For spaces $X$,$A$,  we denote by $\mathcal{H}(X,A) = \mathrm{Maps}(X,A)$  the $(\infty,0)$-category of maps from $X$ to $A$. To emphasize the relation to cohomology,  we name these maps as cocycles and refer to $\mathcal{H}(X,A) = \mathrm{Maps}(X,A)$ as the cohomology of X with coefficients in A: the objects in $\mathrm{Maps} (X,A)$ are the $A$-valued cocycles on $X$, the morphisms are homotopies (or coboundaries) between these and the higher morphisms  are homotopies between homotopies, etc. The connected components in $\mathrm{Map}(X,A)$ are the cohomology classes, $H(X,A)=\pi_0 \mathrm{Map}(X,A)$. These are the sets of morphisms in the homotopy category $H$ of $\mathcal{H}$.

>For instance for $G$ an ordinary abelian group and $X$ a nice topological space, the choice $A = K(G,n)$ (an Eilenberg-Mac Lane space) yields the ordinary cohomology $H^n(X,G) = H(X,K(G,n)) = \pi_0\mathcal{H}(X,A)$.

>If $A$ is pointed in that it is equipped with a morphism ${}_* \overset{\mathrm{pt}_A}\rightarrow A $, then $\mathcal{H}(X,A)$ is naturally pointed with point $X \to {}_* \overset{\mathrm{pt}_A}\rightarrow A,$ the trivial $A$-cocycle on $X$. In particular, if $A$ is the delooping,  $A = \mathbf{B}G$, of a group-like space $G$ in $\mathcal{H}$ (an $\infty$-group or $A_\infty$-space) and if $g : X \to \mathbf{B}G$ is a cocycle, then the homotopy fiber of $g$, i.e. the   homotopy pullback $P \to X$ of the point of $A$ in 
$$
  \array{
    P          & \rightarrow            & {}_* \\
    \downarrow &                        & \downarrow \\
    X          & \overset{g}\rightarrow & \mathbf{B}G
  }
$$
>is the $G$-principal bundle classified by the cocycle $g$.







### $(\infty,1)$-Sheaf-cohomology / $\infty$-stack-cohomology

A Grothendieck--Rezk--Lurie [[(∞,1)-topos]] is an [[(∞,1)-category of (∞,1)-sheaves]]. Its objects are often called [[∞-stacks]] or
[[derived stack]]s.


#### Abelian sheaf cohomology

* [[abelian sheaf cohomology|Abelian sheaf cohomology]] for complexes of sheaves in non-negative degree is cohomology of the sub-[[(∞,1)-topos]] of $\infty$-stacks which take values in [[∞-groupoids]] which, under the [[Dold-Kan correspondence]] come from [[chain complexes]].

* [[abelian sheaf cohomology|Abelian sheaf cohomology]] for unbounded complexes of sheaves is stable cohomology of the [[stable (∞,1)-topos]] of [[spectrum]]-valued [[(∞,1)-sheaves]].

Several familiar "cohomology theories" are not so much genuine cohomology theories as rather computational techniques for computing certain cohomology classes in an [[(∞,1)-category]] by using 1-categorical tools of [[homotopy coherent category theory]] such as [[model categories]], [[derived categories]] and the like.

* [[?ech cohomology]] is the technique of computing $H(X,A)$ by computing 1-categorical [[hom-sets]] $C(\hat X,A)$ on _resolutions_ of the domain object $X$.

* The technique of computing [[abelian sheaf cohomology]] by computing the [[derived global section functor]] is similarly a technique of computing $H(X,A)$ in terms of 1-categorical [[hom-sets]] $C(X,\hat A)$ into _resolutions_ of the coefficient object (namely [[injective resolution]]s).

+--{.query}
Zoran: I am not happy with this assertion. First of all the notion of the derived functor is fundamental and it makes sense even in setups when the injective resolutions do not exist. Abelian sheaf cohomology IS a derived functor of the global sections functor, not a specific technique to computing it. On the other hand, the injective resolutions ARE a specific technique to compute the derived functor. It is also not clear in this entry if it is about sheaves on topological spaces or on sites or some more general setup. 

Urs: I have posted a reply [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=391&page=1#Item_5). Let's sort this out, improve the entry and remove this query box here.
=--


#### Nonabelian sheaf cohomology with constant coefficients {#NonabelianSheafCohomology}

For $X$ a [[topological space]] and $A$ an [[∞-groupoid]], the standard way to define the [[nonabelian cohomology]] of $X$ with coefficients in $A$ is to define it as the intrinsic cohomology as seen in [[∞Grpd]] $\simeq$ [[Top]]:

$$
  H(X,A) := \pi_0 Top(X, |A|) \simeq \pi_0 \infty Func(Sing X, A)
  \,,
$$

where $|A|$ is the [[geometric realization]] of $A$ and $Sing X$ the [[fundamental ∞-groupoid]] of $X$.

But both $X$ and $A$ here naturally can be regarded, in several ways, as objects of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf (∞,1)-topos]]es $\mathbf{H} = Sh_{(\infty,1)}(C)$ over nontrivial [[(∞,1)-site]]s $C$. The intrinsic cohomology of such $\mathbf{H}$ is a [[nonabelian cohomology|nonabelian sheaf cohomology]]. The following discusses two such choices for $\mathbf{H}$ such that the corresponding nonabelian sheaf cohomology coincides with $H(X,A)$ (for [[paracompact space|paracompact]] $X$).

##### Petit $(\infty,1)$-sheaf $(\infty,1)$-topos

For $X$ a [[topological space]] and $Op(X)$ its [[category of open subsets]] equipped with the canonical structure of an [[(∞,1)-site]], let 

$$
  \mathbf{H}
  :=
  Sh_{(\infty,1)}(X) := Sh_{(\infty,1)}(Op(X))
$$

be the [[(∞,1)-category of (∞,1)-sheaves]] on $X$. The space $X$ itself is naturally identified with the [[terminal object]] $X = * \in Sh_{(\infty,1)}(X)$. This is the [[petit topos]] incarnation of $X$.

Write

$$
  (LConst \dashv \Gamma) :  Sh_{(\infty,1)}(X)
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

be the [[global section]]s terminal [[geometric morphism]]. 

Under the [[constant (∞,1)-sheaf]] functor $LConst$ an an [[∞-groupoid]] $A \in \infty Grpd$ is regarded as an object $LConst A \in Sh_{(\infty,1)}(X)$. 

There is therefore the _intrinsic_ [[cohomology]] of the $(\infty,1)$-topos $Sh_{(\infty,1)}(X)$ with coefficients in the [[constant ∞-stack|constant (∞,1)-sheaf]] on $A$
  
$$
  H'(X,A) := \pi_0 Sh_{(\infty,1)}(X)(X, LConst A)
  \,.
$$

Notice that since $X$ is in fact the [[terminal object]] of $Sh_{(\infty,1)}(X)$ and that $Sh_{(\infty,1)}(X)(X,-)$ is in fact that [[global section]]s functor, this is equivalently

$$
  \cdots \simeq \pi_0 \Gamma LConst A
  \,.
$$

+-- {: .un_theorem }
###### Theorem

If $X$ is a [[paracompact space]], then these two definitins of [[nonabelian cohomology]] of $X$ with [[constant ∞-stack|constant coefficients]] $A \in \infty Grpd$ agree:

$$
  H(X,A) := \pi_0 \infty Grpd(Sing X,A)  \simeq Sh_{(\infty,1)}(X)(X,LConst A)
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, theorem 7.1.0.1]]. See also [[(∞,1)-category of (∞,1)-sheaves]] for more.


##### In terms of covering spaces {#InTermsOfCoveringSpaces}

There is an equivalence between $(\infty,1)$-sheaves on $X$ and topological spaces over $X$, as described in detail at [[(∞,1)-sheaves and over-spaces]].

Suppose that $X$ is a [[locally compact space|locally compact]] [[CW complex]].  In particular, this implies that it is "hereditarily [[m-cofibrant space|m-cofibrant]]," i.e. every open subset of $X$ has the [[homotopy type]] of a CW complex.  That's what you need in order to conclude that taking sheaves of sections of spaces over $X$ is well-behaved homotopically, since only m-cofibrant spaces are good for mapping out of homotopically.  

In

* [[Mike Shulman]], _Parametrized spaces model locally constant homotopy sheaves_ ([artXiv:0706.2874](http://arxiv.org/abs/0706.2874))

it is proved that the "sheaf of sections" functor

$$ Top/X \to [Op(X)^{op},sSet] $$

is the [[right adjoint]] in a [[right Quillen embedding]], i.e. a [[Quillen adjunction]] whose  [[derived functor|derived]] right adjoint is [[full and faithful functor|fully faithful]].  In other words, the homotopy theory of spaces over $X$ embeds in the homotopy theory of $(\infty,1)$-sheaves on $X$.  

One can also identify its image as consisting of the [[locally constant (∞,1)-sheaves]].  This is a homotopical version of the identification of [[covering space]]s with [[locally constant sheaves]].

Furthermore, if $f\colon X\to Y$ is a map of such spaces, then the pullback functor $f^*\colon Top/Y \to Top/X$ agrees with the [[inverse image]] functor $f^*$ for $(\infty,1)$-sheaves.  In particular, when $Y$ is a point and $A$ a space, then the constant $(\infty,1)$-sheaf $Const(A)$ is identified with (the sheaf of sections of) the space $X^* A = X\times A$ over $X$.  Therefore, the nonabelian cohomology of $X$ with coefficients in $Const(A)$ is the same as the maps in $Top/X$ from $X$ (the terminal object of $Top/X$) to $X^* A$.  Since the left adjoint of $X^*:Top \to Top/X$ just forgets the structure map to $X$, this is the same as maps in $Top$ from $X$ to $A$.

Thereby we recover Lurie's theorem, in the case when $X$ is a locally compact CW complex.

...

##### Gros $(\infty,1)$-sheaf $(\infty,1)$-topos

Another alternative is to regard the space $X$ as an object in the [[gros topos|gros]] [[(∞,1)-sheaf]] topos $Sh_{(\infty,1)}(CartSp)$ over the [[site]] [[CartSp]], as described at [[∞-Lie groupoid]]. This has the special property that it is a [[locally ∞-connected (∞,1)-topos]], which means that the [[global section|terminal]] [[geometric morphism]] is an [[essential geometric morphism]]

$$
  (\Pi \dashv LConst \dashv \Gamma)
  :
  Sh_{(\infty,1)}(CartSp)
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
  \,,
$$

with the further [[left adjoint]] $\Pi$ to $LConst$ being the intrinsic [[schreiber:path ∞-groupoid]] functor.  The intrinsic [[nonabelian cohomology]] in there also coincides with nonabelian cohomology in [[Top]]; even the full [[cocycle]] [[∞-groupoid]]s are equivalent:

+-- {: .un_theorem }
###### Theorem

For [[paracompact space|paracompact]] $X$ we have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  Sh_{(\infty,1)}(CartSp)(X, LConst A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H(X,A) \simeq \pi_0   Sh_{(\infty,1)}(CartSp)(X, LConst A)
$$

=--

+-- {: .proof}
###### Proof

The key point is that for paracompact $X$, the [[nerve theorem]] asserts that $\Pi(X)$ is [[weak homotopy equivalence|weak homotopy equivalent]] to $Sing X$, the standard [[fundamental ∞-groupoid]] of $X$. This is discussed in detail in the section <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#GeomReal">geometric realization</a> at [[schreiber:path ∞-groupoid]].

Using this, the statement follows by the [[adjoint (∞,1)-functor|(∞,1)-adjunction]] $(\Pi \dashv LConst)$, that is discussed in detail at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#Unstruc">Unstructured homotopy ∞-groupoid</a>.

=--


#### Motivic cohomology

[[motivic cohomology|Motivic cohomology]] is the cohomology of
the [[(∞,1)-topos]] of [[∞-stack]]s on the [[Nisnevich site]],
usually restricted to coefficient objects that are 
[[spectrum object|stable]] and [[A1-homotopy theory|A1-homotopy]]
invariant.


#### Hochschild and cyclic cohomology

[[Hochschild cohomology]] 
is the cohomology $\mathbf{H}(\mathcal{L}X , C)$ of 
[[free loop space object]]s $\mathcal{L}X$ in a [[derived stack]]
[[(∞,1)-topos]] $\mathbf{H}$ with coefficients in 
[[quasicoherent ∞-stack|quasicoherent ∞-stacks of modules]] $C$.
There is a natural [[action]] of the circle $S^1$ on 
the [[free loop space object]] $\mathcal{L}X$ and the corresponding $S^1$-[[equivariant cohomology]] is [[cyclic cohomology]].


#### Algebraic K-theory

[[K-theory]] in its general form of [[algebraic K-theory]] is a way of turning a [[stable (∞,1)-category]] (which may be the [[derived category]] induced by an [[abelian category]] or [[Quillen exact category]]) into a [[spectrum]].

Accordingly, an [[∞-stack]] with values in srable $(\infty,1)$-categories induces a spectrum valued $\infty$-stack after passing to its K-theory. Homming objects $X$ into these spectrum-valued $\infty$-stacks then produces the corresponding **K-cohomology** of $X$.

This, too, goes back all the way to [[BrownAHT]], where in the second part the homotopy categories of spectrum-valued $\infty$-stacks is considered.

...


## Tools for computing cohomology

Various notions called "cohomology" in the literature are not
so much specific examples of cohomology theories 
(specific choices of ambient [[(∞,1)-topos]]es) as rather
specific _tools_ or _algorithms_ for constructing 
$\mathbf{H}(X,A)$.

### &#268;ech cohomology

For the moment see

* [[?ech cohomology]]

### $Ext$-functor and derived global-sections functor

Using a [[model category]] [[presentable (infinity,1)-category|presentation]] for $\mathbf{H}$ one can
compute $\mathbf{H}(X,A)$ using the [[derived functor]] of the
[[hom-functor]]: called the [[Ext functor]].

Specifically for the [[model structure on simplicial sheaves]]
and $X$ [[representable functor|representable]], one has
by [[Yoneda lemma]] that $Hom(X,A) \simeq A(X)$ which is often
written as $\simeq \Gamma(A,X)$ and called the _global section functor_
$\Gamma(A,-)$ applied to $X$. Accordingly its [[derived functor]]
is another way to think of $\mathbf{H}(X,A)$.



### Monadic cohomology

* [[monadic descent|Monadic cohomology]], like [[?ech cohomology]], is a way to compute [[cocycle]]s using tools from [[universal algebra]] in general and the theory of [[monad]]s in particular in the presence of extra 


## Relation to (∞,1)-topos theory {#ToposTheory}

Some of the abstract concepts in cohomology mentioned above make sense in any [[(∞,1)-category]]: we could in principle define [[cocycle]], [[characteristic class]], [[fiber sequence|long sequence in cohomology]], [[twisted cohomology]], etc. the way we did in an $(\infty,1)$-category that is not an [[(∞,1)-topos]], by defining it to be, respectively, a morphism $c : X \to A$, a morphism $\lambda : A \to B$, the [[homotopy fiber]] of $c$, the pullback along the morphism induced by postcomposition with $\lambda$, etc.

Since all these concepts are so simple in the [[(∞,1)-category theory]] context, they seem to work very generally. One may therefore ask why it is that we require an $(\infty,1)$-topos structure in order to interpret these conceptually simple ingredients in terms of cohomology.

There are two ways to answer this question: one is to observe that essentially all cohomology theories that have been considered do happen to have an interpretation in terms of intrinsic $(\infty,1)$-topos cohomology. This is discussed in 

* [Historical aspects](ToposTheoryHistoricalAspects) .

Given that, one can ask what it is _abstractly_ that we want to the notion of cohomology to do and to be, that forces the concept of $(\infty,1)$-topos on us. This is discussed in

* [Abstract aspects](#ToposTheoryAbstractAspects).

### Historical aspects {#ToposTheoryHistoricalAspects}


As we have seen in the list of examples above, large numbers of examples of notions of cohomology do happen to have a natural interpretation in terms of intrinsic $(\infty,1)$-topos cohomology. There are some definitions of cohomology in the literature that are not equivalent to hom-spaces in an $(\infty,1)$-topos. But these tend to be _wrong_ definitions, as illustrated by the following example.


In the literature there is a _naive_ definition of Lie group cohomology and and topological group cohomology, which is not interpretable in terms of hom-spaces in a more general $(\infty,1)$-category, either. But later it was found by Segal and then independently by Brylinski that there is a refinement of this definition, which is better behaved. This refinement, it turns out, does have an interpretation in terms of homs in an $(\infty,1)$-topos. This is described at [[group cohomology]].

...

### Abstract aspects {#ToposTheoryAbstractAspects}

Apart from there being cocycles and coboundaries, in order to speak of _cohomology_ we tend to require these to do something: namely to classify something.

Cocycles on some object $X$ do come with a notion of clasification of certain structures over $X$ in $(\infty)$-topos, as described in detail at [[principal ∞-bundle]]. As discussed in the proof there, for that classification to work, however, one needs 

* [[pullback]]s, 

* [[colimit]]s, 

* [[universal colimits]],

* [[groupoid object in an (infinity,1)-category|effective group objcts]]

in the ambient [[(∞,1)-category]]. 

Pullbacks are needed in order to obtain the [[principal ∞-bundle]] classified by a cocycle (as its [[homotopy fiber]]), universal colimits and effective group objects are needed in order to show that every principal $\infty$-bundle does come from a cocycle this way.

But this list of properties is essentially that of the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-topos#GiraudAxioms">(∞,1)-Giraud axioms</a> that characterize those $(\infty,1)$-categories that are $(\infty,1)$-toposes.

> ... needs to be expanded... 

## History and references {#References}


The general perspective on cohomology was essentially established 35 years ago in

* [[Kenneth Brown]], [[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]] 

and apparently known in one form or other before that.

This article establishes that 

* all of [[abelian sheaf cohomology]] 

  * with all its special cases like, say, [[Deligne cohomology]], 

* all [[generalized (Eilenberg-Steenrod) cohomology]] 

  * with simple things like [[Eilenberg-MacLane spectrum|ordinary cohomology]] and more intricate things like [[K-theory spectrum|K-theory]] and [[tmf]]), 

* as well as [[nonabelian cohomology]] 

  * classifying [[gerbes]] and [[principal ∞-bundles]] 

* as well as the more mundane special cases of this like [[group cohomology]] and, yes, cohomology of cochain complexes itself

are naturally special cases of one single concept: that of hom-sets 

$$
  H(X,A) := Ho_{SSh}(X,A)
$$ 

in the [[homotopy category]] of [[∞-groupoid]]-valued [[sheaves]].

The only fundamental new addition to this insight that is available now and wasn't available 35 years ago is that 


* These categories $H = Ho_{SSh}$ are precisely the [[homotopy category of an (infinity,1)-category|hom-wise decategorification]] of [[(∞,1)-category of (∞,1)-sheaves]] otherwise known as the [[(∞,1)-topoi]] of [[∞-stacks]].


This is propositon 6.5.2.1 in [[Jacob Lurie]]'s [[Higher Topos Theory]] and builds on the fundamental work by K. Brown, Joyal and Jardine and others on the 
[[model structure on simplicial presheaves]].

For a _motivation_ of these definitions from the point of view of cohomology as a homotopy hom-set of $\infty$-stacks see for instance the introductory pages of

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf)) .

The general abstract picture of cohomology as connected components of mapping spaces in [[(∞,1)-topos]]es is the topic of section 7.2.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Notice that the discussion there is, as often in the literature, given from the perspective of a [[petit topos]], i.e. where one thinks of the [[(∞,1)-topos]] $\mathcal{X}$ as that of [[∞-stack]]s on a given [[space]] $X$ (instead of as a [[gros topos]] of _all_ generalized spaces, as we do in the above entry). Accordingly then from that perspective one wants to study the cohomology of $X$ itself, which corresponds to the [[terminal object]] in the $(\infty,1)$-topos. Accordingly, the cohomology in that section 7.2.2 is defined for the terminal coefficient object and for an [[Eilenberg-MacLane object]] $K(A,n)$:

$$
  H^n(\mathcal{X},A) := \pi_0\mathcal{X}({*}, K(A,n))
$$

(definition 7.2.2.14).

Another reference with a  discussion of cohomology in the general sense discussed above, using tools of [[model category]] theory for [[simplicial object]]s, is

* [[Brian Conrad]], _Cohomological descent_ ([pdf](http://math.stanford.edu/~conrad/papers/hypercover.pdf))

For more on the pre-history of the notion of cohomology see 

* MO entry, <a href="http://mathoverflow.net/questions/39597/timeline-of-cohomology-1935-to-1938">Timeline of cohomology (1935 to 1938)</a>




[[!redirects cohomologies]]