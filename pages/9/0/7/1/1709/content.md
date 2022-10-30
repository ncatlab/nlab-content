

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
* automatic table of contents goes here
{:toc}

## Idea 

Given a morphism $f : \hat B \to B$ in an [[(∞,1)-topos]] $\mathbf{H}$, regarded as exhibiting a [[characteristic class]] on $\hat B$ with values in $B$, the $f$-**twisted cohomology** at [[generalized element|stage]] $X$ is the fiber of $f$ over a given [[generalized element|element]] of $B$.

This is such that if $f : \hat B \to *$ is the [[nLab:terminal object|terminal]] morphism, $f$-twisted cohomology is precisely the ordinary [[cohomology]] in $\mathbf{H}$ with coefficients in $\hat B$.

## Definition



+-- {: .un_defn}
###### Definition


For 

* $\mathbf{H}$ an [[(∞,1)-topos]];

* $f:\hat B \to B$ a morphism in $\mathbf{H}$ (a [[characteristic class]] on $\hat B$-cohomology);

* $X\in \mathbf{H}$ an object of $\mathbf{H}$;

* and $c \in \mathbf{H}(X,B)$ a $B$-[[cocycle]] on $X$ with [[cohomology]] class $[c] \in \pi_0 \mathbf{H}(X,B)$

the $(f,[c])$-**twisted cohomology** of $X$ is the set of equivalence classes

$$
  H_{[c]}(X,f) := \pi_0\mathbf{H}_{[c]}(X,f)
$$

of the [[homotopy fiber]] $\mathbf{H}_{[c]}(X,f)$  of the morphism $f:\hat B \to B$ over the [[generalized element]] $c$ of $B$. 

More explicitly, $\mathbf{H}_{[c]}(X,f)$ is 
the [[∞-groupoid]] defined as the [[homotopy pullback]]

$$
  \array{
    \mathbf{H}_{[c]}(X,f) &\to& {*}
    \\
    \downarrow && \;\downarrow^{\mathrlap{{*}\mapsto c}}
    \\
    \mathbf{H}(X,\hat B) &\to& \mathbf{H}(X,B)
  }
  \,.
$$

=--

## Properties


### Formulation in terms of sections {#InTermsOfSections}

Twisted cohomology may be reformulated equivalently in terms of collections of [[section]]s as follows:

Given the twisting cocycle $c : X \to B$, let $P_f \to X$ be the $\infty$-[[pullback]] ([[homotopy pullback]]) of $\hat B \to B$ along this cocycle:

$$
  \array{
    P_f &\to& {\hat{B}}
     \\
     \downarrow && \downarrow{f}
     \\ 
     X  &\stackrel{c}{\to}& B
  }\,.
$$

Write $\Gamma(P_f) = \mathbf{H}_X(X, P_f)$ for the $\infty$-groupoid of [[section]]s of $P_f \to X$.



+-- {: .un_prop}
###### Proposition

This collection of sections is the $(f,[c])$-twisted cohomology of $X$:

$$
 \pi_0 \Gamma(P_f) \simeq H_{[c]}(X,f)
$$

=--

+-- {: .proof}
###### Proof


By the universal property of ([[homotopy pullback|homotopy]]) [[pullback]]s, homotopy classes of sections $X \to P_f$, are in bijection with homotopy classes of homotopy comutative cones of the form

$$
  \array{
     && X
     \\
     & {}^{id}\swarrow && \searrow
     \\
     X &\stackrel{c}{\to}& B
     &\stackrel{f}\leftarrow& \hat{B}
  }
  \,.
$$

These in turn are manifestly the homotopy classes of maps $X \to \hat{B}$ such that $X \to \hat{B} \to B$ is homotopic to $c$. 

=--

More generally:

+-- {: .un_prop}
###### Proposition

We have a natural equivalence

$$
  \mathbf{H}_{[c]}(X,f)  
  \simeq
  \mathbf{H}_{/B}(c,f)
  \,,
$$

where on the right we have the [[derived hom space]] in the [[over-(∞,1)-topos]] over $B$ from the twisting cocycle $c : X \to X$ to the morphism $f : \hat B \to B$.

=--

+-- {: .proof}
###### Proof

Use the characterization of the [homotopy fibers of (∞,1)-functor categories](http://ncatlab.org/nlab/show/fiber+sequence#OfFuncCats) (as described there) in terms of [[hom-object in a quasi-category|hom-object]] in the [[over quasi-category|over (∞,1)-category]] $\mathbf{H}_{/B}$.

On the right, the objects are morphism $X \to \hat B$ equipped with equivalences from $X \to \hat B \stackrel{f}{\to} B$ to $c : X \to B$.

=--



### Twisted cohomology with trivial twisting cocycle

Let  ${*} \to B$ be a [[pointed object]]. Then

* we say that the [[cocycle]] 

  $(X \to * \to B) \in \mathbf{H}(X,B)$ 

  is the **trivial $B$-cocycle** on $X$.

*  the morphism $f:\hat{B}\to B$ induces a [[fibration sequence]] 

   $A \to \hat B \stackrel{f}{\to} B$ 

   in $\mathbf{H}$.


+-- {: .un_prop}
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

+-- {: .un_remark}
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

#### ... and $\infty$-sections as twisted $\infty$-functions {#InfSections}

Regarded this way, the above discussion has a generalization to the case where the [[monoid]] $\mathbb{C}$ is replaced with any [[ring spectrum]] $R$ and we consider

$$
  X \stackrel{\tau}{\to} R Line \hookrightarrow R Mod
  \,.
$$

Twisted cohomology in terms of such morphisms $\tau$ is effectively considered in

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_ ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))

and in unpublished work of [[Ulrich Bunke]] et al. For more on this see the discussion at [[(∞,1)-vector bundle]].


### twisted K-theory 

In the context of [[generalized (Eilenberg?Steenrod) cohomology]] a coefficient object for [[cohomology]] is a [[spectrum]] $A$: the $A$-cohomology of a [[topological space]] $X$ with coefficients in $A$ is the set of homotopy classes of maps $X \to A$. For instance, as a model of the degree-$0$ space in the [[K-theory spectrum]] one can take $A = Fred(H)$, the space of Fredholm operators on a separable Hilbert space $H$. There is a canonical action on this space of the projective unitary group $G = P U(H)$ of $H$. Since $P U(H)$ has the homotopy type of an [[Eilenberg?Mac Lane space]] $K(\mathbb{Z},2)$, a $P U(H)$-[[principal bundle]] $P \to X$ defines a class $c \in H^3(X,\mathbb{Z})$ in [[Eilenberg-MacLane spectrum|ordinary integral cohomology]] (this may also be thought of as the class of a twisting [[bundle gerbe]]). The twisted K-theory (in degree $0$) of $X$ with that class as its twist is the set of homotopy classes of sections $X \to P \times_{P U(H)} Fred(H)$ of the associated bundle. 


### $G$-Actions on spectra  

The above example generalizes straightforwardly to the case that 

* $A$ is a [[spectrum|connective spectrum]], i.e. [[topological space]] that is an infinite [[loop space]]. (We need to assume a connective spectrum given by an infinite loop space so that $A$ can be regarded as living in the category of topologicall spaces along with the other objects, such as classifying spaces $\mathbf{B}G$ of nonabelian groups);

* with a (topological) [[group]] $G$ acting on $A$ by automorphisms and 

* a $G$-[[principal bundle]] $P \to X.$ 

In this case there is an established definition of [[generalized (Eilenberg?Steenrod) cohomology]] with coefficients $A$ _twisted_ by a $G$-[[principal bundle]] as follows.

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


+-- {: .un_remark}
###### Remark

Since the associated bundle $P \times_G A$ is in general no longer itself a spectrum, twisted cohomology is not an example of [[generalized (Eilenberg-Steenrod) cohomology|generalized Eilenberg?Steenrod cohomology]]. 

To stay within the spectrum point of view, May&#8211;Sigurdsson suggested that twisted cohomology should instead be formalized in terms of _parameterized homotopy theory_, where one thinks of $P \times_G A$ as a parameterized family of spectra. 

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


## Related entries

* [[local coefficient bundle]]

* [[relative cohomology]]

* <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos+--+structures#TwistedCohomology">twisted cohomology</a> in [[cohesive (∞,1)-topos -- structures]]

## References 

A discussion of $\pi_1(X)$-twisted ordinary cohomology is in 

* M. Bullejos, E. Faro, M. A. Garc&iacute;a-Mu&ntilde;oz, _Homotopy colimits and cohomology with local coefficients_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 44 no. 1 (2003), p. 63-80 ([numdam](http://www.numdam.org/item?id=CTGDC_2003__44_1_63_0))

For the special case of [[generalized (Eilenberg?Steenrod) cohomology]] twisted by a $G$-[[principal bundle]] see section 22.1 of

* [[Peter May|May]], Sigurdsson, _[[Parametrized Homotopy Theory]]_ ([pdf]( http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))

This in turn is based on the definition of twisted K-theory given in 

* [[Michael Atiyah]] and [[Graeme Segal]], _Twisted K-theory_ . Ukr. Mat. Visn., 1(3):287&#8211;330, 2004.
<http://front.math.ucdavis.edu/0407.5054>

Details on Larmore's work on twisted cohomology are at

* [[Larmore twisted cohomology]].

The above discussion of $c$-twisted cohomology as the homotopy fiber of $\mathbf{H}(X,\hat B) \to \mathbf{H}(X,B)$ over $c \in \mathbf{H}(X,B)$ etc. is in 

* [[schreiber:Principal ∞-bundles -- theory, presentations and applications]]

### Chronology of literature on twisted cohomology 


The oldest meaning of twisted cohomology is that of **cohomology with local coefficients** (see above).

For more on the history of that notion see

* [[History of cohomology with local coefficients]]

In the following we shall abbreviate

* tc = twisted cohomology

Searching MathSciNet for _twisted cohomology_ led to the following chronology: It missed older references in which the phrase was not used but the concept was in the sense of local coefficient systems &#8211; ancient and honorable.

Most notably missing are

* Reidemeister (1938) (But note that reprints appear, sans reviews. There is a short English and longer German review on Zentralblatt)

* Steenrod (1942,1943)

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

* 1998 Farber, Katz, Levine Morse theory

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






