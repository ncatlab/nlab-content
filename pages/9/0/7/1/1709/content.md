<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

In the context of [[generalized (Eilenberg?Steenrod) cohomology]] a coefficient object for [[cohomology]] is a [[spectrum]] $A$: the $A$-cohomology of a [[topological space]] $X$ with coefficients in $A$ is the set of homotopy classes of maps $X \to A$.


The standard example, in this generality,  is [[twisted K-theory]]: let $A$ be a model of the degree-$0$ space in the [[K-theory spectrum]], i.e. for instance $A = \mathbb{Z} \times B U$ or $A = Fred(H)$, the space of Fredholm operators on a separable Hilbert space $H$. There is a canonical action on this space of the projective unitary group $G = P U(H)$ of $H$.

Since $P U(H)$ has the homotopy type of an [[Eilenberg?Mac Lane space]] $K(\mathbb{Z},2)$, a $P U(H)$-[[principal bundle]] $P \to X$ defines a class $c \in H^3(X,\mathbb{Z})$ in [[Eilenberg-MacLane spectrum|ordinary integral cohomology]].

The twisted K-theory (in degree $0$) of $X$ with that class as its twist is the set of homotopy classes of sections $X \to P \times_{P U(H)} Fred(H)$ of the associated bundle.

This generalizes straightforwardly to the case that 

* $A$ is a [[spectrum|connective spectrum]], i.e. [[topological space]] that is an infinite [[loop space]]. (We need to assume a connective spectrum given by an infinite loop space so that $A$ can be regarded as living in the category of topologicall spaces along with the other objects, such as classifying spaces $\mathbf{B}G$ of nonabelian groups).

* with a (topological) [[group]] $G$ acting on $A$ by automorphisms and 

* a $G$-[[principal bundle]] $P \to X,$ 

then one says that the collection of homotopy classes of [[section]]s 

$$
  X \to P \times_G A
$$

(where $P \times_G A \to X$ is the associated bundle of spectra)
 is the _twisted $A$-cohomology of $X$_ with the twist specified by the class of $P$.

+-- {: .un_remark}
###### Remark

Since the associated bundle $P \times_G A$ is in general no longer itself a spectrum, twisted cohomology is not an example of [[generalized (Eilenberg-Steenrod) cohomology|generalized Eilenberg?Steenrod cohomology]]. 

To stay within the spectrum point of view, May&#8211;Sigurdsson suggested that twisted cohomology should instead be formalized in terms of _parameterized homotopy theory_, where one thinks of $P \times_G A$ as a parameterized family of spectra. This is discussed below.

=--


In our context for $H(X;A)$, a coefficient object for [[cohomology|cohomology]] is a (possibly generalized) space $A$: the $A$-cohomology $H(X;A)$ of a [[topological space|topological space]] $X$ with coefficients in $A$ is the set of homotopy classes of maps $X \to A$:



$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$

In the special case of $\mathbf{H}$ =  [[Top]] this is the usual

$$
  H(X,A) = \pi_0 Maps(X,A) = [X,A]
  \,.
$$

+-- {: .un_remark}
###### Remark

To distinguish the general notion of [[cohomology|cohomology]] in an arbitrary [[(infinity,1)-topos|(∞,1)-topos]] from the specific one woth coefficients in [[spectra|spectrum]] one sometimes says [[nonabelian cohomology]] for the former. But notice that apart from allowing "nonabelian spaces" like $P \times_G A$ as coefficients, it also allows objects more general than (infinite-loop) topological spaces, namely generally [[∞-stack]]s.

=--

The upshot of this is that the general [[(∞,1)-topos]]-context suggests that the notion of twisted cohomology should be one that makes use only of natural [[(infinity,1)-category|(∞,1)-categorical]] constructions. Or, more simply, in any
context in which the usual operations of [[homotopy theory]] make sense.

To see what these might be, one may notice that the [[action]] of a group $G$ on an object $A$ is entirely encoded in the corresponding [[action groupoid]] [[fibration sequence]]

$$
  A \to A//G \to \mathbf{B} G
  \,,
$$

where $\mathbf{B} G$ is the [[delooping]] of $G$, which in the case of $\mathbf{H} = $ [[Top]] is just the familiar [[classifying space]] of $G$. In that case, the object $A//G$ is traditionally modeled in terms of the _Borel construction_ and written $A_G = A//G \simeq E G \times_G A$. This is the $A$-bundle associated to the _universal_ $G$-[[principal bundle]].

Moreover, one can see, as described in detail below, that for a given $G$-principal bundle $P \to X$ that is classified by an element $ c \in \pi_0 Top(X,\mathbf{B}G) =: H^1(X,G)$ 

+-- {: .query}
[[Jim Stasheff]] REMEMBER: DEFINE BEFORE USING

[[Urs Schreiber]] isn't that standard notation? In any case I put a "=:" now to indicate that this _is_ the definition
=--

 the set of homotopy classes of sections $X \to P \times_G A$ is the set of connected components of the [[homotopy pullback]]

$$
  \array{
    Top_{[c]}(X,A) &\to& {*}
    \\
    \downarrow && \;\;\downarrow^{{*} \mapsto c}
    \\
    Top(X,A//G) &\to& Top(X, B G)
  }
  \,.
$$

+-- {: .query}
[[Jim Stasheff]] INDICATE WHY THAT IS TRUE - I.E. A SECTION OF A PULLBACK IS THE SAME AS...

[[Urs Schreiber]] above it says that this is discussed in more detail below. I have now made this statement a formal proposition with a detailed proof. See below.
=--

The above discussion  suggests a general notion of twisted cohomology for twists more general than given by a group action:

for 

* any [[fibration sequence]] 
  $$
    F \to A \to B
  $$


* and for any $B$-[[cohomology|cocycle]] 

  $$
    c \in \mathbf{H}(X,B)
  $$ 

it makes sense to say that the connected components

$$
  H_{[c]}(X,A) := \pi_0 \mathbf{H}_{c}(X,A)
$$ 

in the homotopy pullback

$$
  \array{
    \mathbf{H}_{c}(X,A) &\to& {*}
    \\
    \downarrow && \;\;\downarrow^{{*} \mapsto c}
    \\
    \mathbf{H}(X,\hat B) &\to& \mathbf{H}(X, B)
  }
$$

are the **$[c]$-twisted $A$-cohomology classes of $X$**.

+-- {: .query}
[[Jim Stasheff]] IT WOULD MAKE EQUALLY GOOD SENSE AND CLOSER TO THE ABOVE TO SAY THAT the **$[c]$-twisted $A$-cohomology classes of $X$** ARE THE CONNECTED COMPONENTS OF THE SPACE OF SECTIONS...
=--


#Definition#

We now say this again, more formally and more in detail.


Let $\mathbf{H}$ be an [[(infinity,1)-topos|(∞,1)-topos]]. 
Let $H=\pi_0 \mathbf{C}$ be the corresponding [[homotopy category of an (infinity,1)-category|homotopy category]].

Recall  that for $X$ and $A$ objects in $\mathbf{H}$ we
denote by $\mathbf{H}(X,A)$ the [[infinity-groupoid|∞-groupoid]] whose cells we think of as follows:

* objects of $\mathbf{H}(X,A)$ are $A$-valued **cocycles** on $X$:

* morphisms in $\mathbf{H}(X,A)$ are **coboundaries** between these cocycles;

* equivalence classes in $\mathbf{H}(X,A)$ are [[cohomology]] classes,

* so that the [[homotopy category of an (infinity,1)-category|homotopy]] [[hom-set]]
  $$
    H(X,A) := \pi_0 \mathbf{H}(X,A) 
  $$
  is the $A$-valued **cohomology** set of $X$. It is a group if $A$ is [[k-tuply groupal n-groupoid|groupal]].


+-- {: .query}
[[Jim Stasheff]]THAT DOSN'T SEEM TO NEED THE HIGHER CELLS?

[[Urs Schreiber]]: taking classes forgets the higher cells, but in order to have the correct homotopy pullback properties etc we need to keep them. that's the point of using $(\infty,1)$-categories, that the homotopy pullbacks etc. work correctly
=--

## Obstruction theory ##

Now consider the **obstruction problem** in cohomology:

let $A \to \hat B \to B$ be a [[fibration sequence]] in $\mathbf{H}$, i.e. a sequence such that the square

$$
  \array{
    A &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \hat B &\to& B
  }
$$

is a [[homotopy pullback]] square, with ${*}$ denoting [[generalized the|the]] [[point]] ([[generalized the|the]] [[terminal object]]).

Since the $\infty$-groupoid valued hom in an [[(∞,1)-category]] is [[exact functor|exact]] with respect ot [[homotopy limits]], it follows that for every object $X$, there is  fibration sequence of cocycle [[∞-groupoids]]

$$
  \array{
    \mathbf{H}(X,A) &\to& {*}
    \\
    \downarrow && \downarrow^{const_{*}}
    \\
    \mathbf{H}(X,\hat B) &\to& \mathbf{H}(X,B)
  }
  \,.
$$


This may be read as:

* the **obstruction** to lifting a $\hat B$-cocycle to an $A$-cocycle is its image in $B$-cohomology (all with respect to the given [[fibration sequence]])

But it also says:

* $A$-cocycles are, up to equivalence, precisely those $\hat B$-cocycles whose class in $B$-cohomology is the trivial class (given by the trivial cocycle $const_{*} : {*} \to $).

This may motivate the following definition 

+-- {: .un_defn}
###### Definition (twisted cohomology)

For 

* $\mathbf{H}$ an [[(∞,1)-topos]];

* $A \to \hat B \to B$ a [[fibration sequence]] in $\mathbf{H}$;

* $X\in \mathbf{H}$ an object of $\mathbf{H}$;

* and $c \in \mathbf{H}(X,B)$ a $G$-cocycle on $X$

the **$c$-twisted $A$-cohomology of $X$** is the the set of equivalence classes

$$
  H^{[c]}(X,A) := \pi_0 \mathbf{H}^c(X,A)
$$

of the [[∞-groupoid]] $\mathbf{H}^c(X,A)$ that is defined as the [[homotopy pullback]]

$$
  \array{
    \mathbf{H}^{c}(X,A) &\to& {*}
    \\
    \downarrow && \;\downarrow^{{*}\mapsto c}
    \\
    \mathbf{H}(X,\hat B) &\to& \mathbf{H}(X,B)
  }
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

Notice that compared to the previous [[fibration sequence]] arising in the obstruction problem, the [[homotopy limit]] in the above definition replaces the trivial cocycle $const_{*}$ by the prescribed $G$-cocycle $c$.
=--


# Relation to other definitions #

The usual definition of twisted cohomology is a special case of this where

* the $(\infty,1)$-topos $\mathbf{H} :=$ [[Top]] is the $(\infty,1)$-category of topological spaces

* the object $B := B G$ is the [[delooping]] of a [[group]] $G$.

* the object $A$ is a (connective) [[spectrum]] (an infinitely [[delooping|deloopable]] topological space).

* there is an [[action]] of $G$ on $A$.


In this case there is an established definition of [[generalized (Eilenberg?Steenrod) cohomology]] with coefficients $A$ _twisted_ by a $G$-[[principal bundle]] as follows.

From the $G$-[[principal bundle]] $P \to X$ we obtain the associated $A$-bundle $P \times_G A \to X$. Then a twisted $A$-cocycle on $X$ is defined to be a [[section]] $X \to P \times_G A$ of this associated bundle.

This is the definition of twisted cohomology as it appears for instance essentially as definition 22.1.1 of the May&#8211;Sigursson reference below.

(When comparing with their definition take their $G$ to be the trivial group and identify their $\Gamma$ and $\Pi$ with our $G$).

We now discuss how this is a special case of the above definition of twisted cohomology.

A pair consisting of a space $A$ acted on by a group $G$ can be equivalently thought of as one single space: the homotopy quotient of $A$ by $G$, a concrete realization of which is the Borel construction $\mathbf{E}G \times_G A$. (Of course this construction works for any space $A$ with $G$-action, it need not be a spectrum.

The fact that  $G$ acts on  $A$ is witnessed by the existence of a left-long [[fibration sequence]]

$$
  \cdots \to A \to A//G \to \mathbf{B}G.
$$

i.e. a there is a homotopy pullback square

$$
  \array{
     A &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     A//G &\stackrel{\delta}{\to}& \mathbf{B}G
  }
$$

The universal property of this homotopy pullback says precisely that:

*  the obstruction to lifting a ("nonabelian" or "twisted") $A//G$-cocycle $g : X \to A//G$ to an $A$-cocycle $\hat g : X \to A$ is its image $\delta g $ in first $G$-cohomology  $\delta g \in H^1(X,G) := H(X,B G) = [X, B G]$ under the above horizontal map. 

* this image $\delta g$ is the twist in question.

(Notice that $H^1(X,G)$ is the standard notation for $[X, B G] := \pi_0 \mathbf{H}(X, B G)$.)

Read the other way round it says:

* $A$-cocycles are precisely those $G$-twisted $A$-cocycles whose twist vanishes.

More formally, but without adding any genuine new information, since cohomology is just connected components of the [[(∞,1)-categorical hom-space|(infinity,1)-categorical hom-space]] in our context, we know that for any $X$ we have a [[fibration sequence]]

$$
  \array{
     \mathbf{H}(X,A) &\to& {*}
     \\
     \downarrow && \downarrow^{{*} \mapsto {*}}
     \\
     \mathbf{H}(X,A//G) &\to& \mathbf{H}(X,\mathbf{B}G)
  }
  \,.
$$

of mapping $\infty$-groupoids (which as topological spaces are the mapping spaces with compact-open topology).


So if we fix the twisting cocycle 

$$
  c \in \mathbf{H}(X, \mathbf{B}G)
$$

defining the class

$$
  [c] \in \pi_0 \mathbf{H}(X, \mathbf{B}G) =: H^1(X,G)
$$ 


then the $[c]$-twisted $A$-cohomology is precisely that bit of $\mathbf{H}(X,A//G)$ that sits in the homotopy fiber over $c$.

Therefore we may say that the $c$-twisted cohomology is the connected components $H^{[c]}(X,A)$ of the homotopy pullback $\mathbf{H}^c(X,A)$ in 

$$
  \array{
     \mathbf{H}^c(X,A) &\to& {*}
     \\
     \downarrow && \;\downarrow^{{*} \mapsto c}
     \\
     \mathbf{H}(X,A//G) &\to& \mathbf{H}(X,\mathbf{B}G)
  }
  \,.
$$


## in terms of sections ##

To see that this does indeed reproduce the description in terms of sections of associated bundles, look at the long fibration sequence one step down the row, where it reads

$$
  \array{
    A//G \simeq \mathbf{E}G\times_G A &\to& {*}
     \\
     \downarrow && \downarrow
     \\ 
     \mathbf{B}G  &\stackrel{\rho}{\to}& \mathbf{B}A
  }
$$

and exhibts $A//G$ as the bundle with fiber $A$ that is $\rho$-associated to the universal $G$-bundle.

For the given $G$-cocycle $X \to \mathbf{B}G$ the corresponding associated bundle with fiber $A$ over $X$ is the further homotopy pullback $P$ in

$$
  \array{
    P &\to&
    A//G \simeq \mathbf{E}G\times_G A &\to& {*}
     \\
     \downarrow &&
     \downarrow && \downarrow
     \\ 
     X &\to&
     \mathbf{B}G  &\stackrel{\rho}{\to}& \mathbf{B}A
  }
$$



And again it is precisely the universal property of the homotopy pullback that asserts that sections $X \to P$ of this bundle are in bijection, up to homotopy, with those maps $X \to A//G$ whose projection to $X \to \mathbf{B}G$ reproduces the prescribed twist.


+-- {: .un_prop }
###### Proposition

The connected components of $\mathbf{H}_{[c]}(X,A)$ are in bijection with the homotopy classes of sections of the $A$-bundle $P \to X$ associated to the fibration classified by $c$:

$\pi_0 \Gamma(P) \simeq H_{[c]}(X,A)$.

=--

+-- {: .proof}
###### Proof

By definition of homotopy pullback 

$$
  \array{
     \mathbf{H}_{[c]}(X,A)
     &\to&
     {*}
     \\
     \downarrow && \downarrow
     \\
     \mathbf{H}(X,A//G)
     &\to&
     \mathbf{H}(X,\mathbf{B}G)
  }
$$

an element of $\mathbf{H}_{[c]}(X,A)$ is an $A//G$-cocycle $X \to A//G$ whose image $X \to A//G \to \mathbf{B}G$ represents $ [c] \in H(X,\mathbf{B}G)$.

On the other hand, the associated bundle $P \to X$ sits in the double homotopy pullback

$$
  \array{
    P &\to&
    A//G \simeq \mathbf{E}G\times_G A &\to& {*}
     \\
     \downarrow &&
     \downarrow && \downarrow
     \\ 
     X &\stackrel{c}{\to}&
     \mathbf{B}G  &\stackrel{\rho}{\to}& \mathbf{B}A
  }
  \,.
$$

By the universal property of the left homotopy pullback, homotopy classes of sections $X \to P$, are in bijection with homotpy classes of homotopy comutative cones of the form

$$
  \array{
     && X
     \\
     & {}^{id}\swarrow && \searrow
     \\
     X &\stackrel{c}{\to}& \mathbf{B}G
     &\leftarrow& A//G
  }
  \,.
$$

These in turn are manifestly the maps $X \to A//G$ such that $X \to A//G \to \mathbf{B}G$ is homotopic to $c$. So it is the same set as before.

=--


We may summarize this by a 

+-- {: .un_remark}
###### Principle

* Higher [[nonabelian cohomology]] disguises as twisted higher abelian cohomology;

* conversely: twisted higher abelian cohomology is really nonabelian cohomology
=--




# Examples #

## group cohomology with coefficients in a module ##

Some somewhat trivial examples of this appear in various context. For instance [[group cohomology]] on a group with coefficients in a nontrivial module can be regarded as an example of twisted cohomology. See there for more details.

Compare this to the example below of cohomology "with local coefficients". It is the same principle in both cases.

## twisted bundles ##


To get a feeling for how the definition does, it is 
instructive to see how for the fibration sequence coming from an ordinary central extension $K \to \hat G \to G$ of ordinary groups as

$$
  \mathbf{B}\hat G \to \mathbf{B}G \stackrel{\omega}{\to}
  \mathbf{B}^2 K
$$

classified by a [[group cohomology|group 2-cocycle]] $\omega$, $c$-twisted $\hat G$-cohomology produces precisely the familiar notion of [[twisted bundles]], with the twist being the lifting [[gerbe]] that obstructs the lift of a $G$-bundle to a $\hat $G$-bundle$.

This is also the first example in the list
in the last section of

* [[schreiber:Background fields in twisted differential nonabelian cohomology|Background fields in twisted differential nonabelian cohomology]]

and contains examples that are of interest in the wider context of [[string theory]].

See also [Twisted Differential String- and Fivebrane-Structures](http://golem.ph.utexas.edu/category/2009/03/twisted_differential_string_an.html).


## twisted K-theory ##

The example of the definition of twisted cohomology as sections of an assoociated bundle of spectra that has been the motivating example is [[twisted K-theory]]. The group $P U(H)$ of projective unitary operators on a seperable Hilbert space acts canonically on the classifying space $Fred(H)$ (the space of Fredholm operators) of the $K^0$ [[Grothendieck group]] of [[topological K-theory]].

Since $PU(H)$ is topologically an [[Eilenberg?Mac Lane space]] $K(\mathbb{Z},2)$, a twisting cocycle in this case is a class in $H^3(X,\mathbb{Z})$. This may also be thought of as the class of a twisting [[bundle gerbe]].


## cohomology with local coefficients ##

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


# References #

For the special case of [[generalized (Eilenberg?Steenrod) cohomology]] twisted by a $G$-[[principal bundle]] see section 22.1 of

* May, Sigurdsson, _Parametrized homotopy theory_ ([pdf]( http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))

This in turn is based on the definition of twisted K-theory given in 

* Michael Atiyah and Graeme Segal. _Twisted K-theory_ . Ukr. Mat. Visn., 1(3):287&#8211;330, 2004.
<http://front.math.ucdavis.edu/0407.5054>

Details on Larmore's work on twisted cohomology are at

* [[Larmore twisted cohomology]].

The above definition of $c$-twisted cohomology as the homotopy fiber of $\mathbf{H}(X,\hat B) \to \mathbf{H}(X,B)$ over $c \in \mathbf{H}(X,B)$ has, to the best of my ([[Urs Schreiber]]) knowledge not been stated this way in the literature before. This arose in the course of the work 

* [[schreiber:Background fields in twisted differential nonabelian cohomology|Background fields in twisted differential nonabelian cohomology]].

See there for examples and applications.


## chronology of literature on twisted cohomology ##


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















