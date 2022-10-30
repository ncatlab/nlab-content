

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Idea
 {#Idea}

The notion of _spectral sequence_ is an [[algorithm]] or computational tool in [[homological algebra]] and more generally in [[homotopy theory]] which allows to compute [[chain homology|chain homology groups]]/[[homotopy groups]] of _bi_-[[graded objects]] from the homology/homotopy of the two graded components. 

Notably there is a spectral sequence for computing the homology of the [[total complex]] of a [[double complex]] from the homology of its row and column complexes separately.
This in turn allows to compute [[derived functors]] of composite functors $G\circ F$ from the double complex $\mathbb{R}^\bullet G (\mathbb{R}^\bullet F(-))$ obtained by non-totally deriving the two functors separately (called the [Grothendieck spectral sequence](#GrothendieckSpectralSequence)). By choosing various functors $F$ and $G$ here this gives rise to various important classes of examples of spectral sequences, see [below](#SpecialGrothendieckSpectralSequence).

More concretely, a homology spectral sequence is a sequence of graded chain complexes that provides the higher order corrections to the _na&#239;ve_ idea of computing the homology of the [[total complex]] $Tot(V)_\bullet$ of a [[double complex]] $V_{\bullet, \bullet}$: by first computing those of the vertical differential, then those of the horizontal differential induced on these vertical homology groups (or the other way around). This simple idea in general does not produce the correct homology groups of $Tot(V)_\bullet$, but it does produce a "first-order approximation" to them, in a useful sense. The spectral sequence is the sequence of higher-order corrections that make this naive idea actually work.

Being, therefore, an iterative perturbative approximation scheme of bigraded differential objects, fully-fledged spectral sequences can look a bit intricate. However, a standard experience in mathematical practice is that for most problems of practical interest the relevant spectral sequence "perturbation series" yields the exact result already at the second stage. This reduces the computational complexity immensely and makes spectral sequences a wide-spread useful computational tool.

Traditionally, as in the example of the total complex of a double complex, spectral sequences are considered in the context of [[model structure on chain complexes|model categories of chain complexes]] in some [[abelian category]] for which [[fibrant replacement]] is given by [[injective resolution]] of [[chain complexes]].
But more generally there is a notion of [[nonabelian cohomology|nonabelian]]/unstable spectral sequences, called **homotopy spectral sequences**.

Despite their name, there is nothing specifically "spectral" about spectral sequences, for none of the technical meanings of the word [[spectrum]]. Together with the concept, this term was introduced by [[Jean Leray]] and has long become standard, but was never really motivated (see p. 5 of [Chow](#Chow)).

## Definition

We give the general definition of a (co)homology spectral sequence. For motivation see the example _[Spectral sequence of a filtered complex](#SpectralSequenceOfFilteredComplex)_ below.

Throughout, let $\mathcal{A}$ be an [[abelian category]]. 

### Spectral sequence

+-- {: .num_defn}
###### Definition

A __cohomology spectral sequence__ in $\mathcal{A}$ is 

* a family $(E^{p,q}_r)$ of [[objects]] in $\mathcal{A}$, for all [[integers]] $p,q,r$ with $r\geq 1$ 

  (for a fixed $r$ these are said to form the __$r$-th page__ of the spectral sequence)

* for each $p,q,r$ as above a [[morphism]] (called the __differential__) 
  
  $$
    d^{p,q}_r:E^{p,q}_r\to E^{p+r,q-r+1}_r
  $$ 

  satisfying $d_r^2 = 0$ (more precisely, $d_r^{p+r,q-r+1}\circ d_r^{p,q} = 0$)

* [[isomorphisms]] $\alpha_r^{p,q}: H^{p,q}(E_r)\to E^{p,q}_{r+1}$ where 
  the [[chain cohomology]] is given by
  
  $$
    H^{p,q}(E_r) = \mathrm{ker} d^{p,q}_r/ \mathrm{im} d^{p-r,q+r-1}_r
   \,.
  $$

=--

Analogously a **homology spectral sequence** is collection of objects $(E_{p,q}^r)$ with the differential $d_r$ of degree $(-r,r-1)$.



### Convergence

+-- {: .num_defn}
###### Definition
**(convergence)**

A component of a spectral sequence $(E_r)$ **converges** at $(p,q)$ if there exists finite $r$ such that $E_r^{p,q} \simeq E_{r+1}^{p,q} \cdots =: E_\infty^{p,q} $. One writes this as

$$
  E^{p,q}_r \Rightarrow E^{p,q}_\infty
  \,.
$$

A spectral sequence is said to **degenerate** in the $E_r$-term if $d^{p,q}_{r'} = 0$ for all $r'\geq r$. Then clearly it converges degreewise.

A spectral sequence is called **bounded** if for each $r$ and $n$ there are only finitely many non-vanishing terms of the form $E_r^{p,n-p}$. Also a bounded spectral sequence converges degreewise.

A spectral sequence $(E_r)$ **converges** if it converges degreewise to a graded filtration: if there is a graded object $(H^n)_{n \in \mathbb{Z}}$ equipped in each degree with a _finite_ filtration

$$
  0 \subset \cdots \subset F^{p} H^n \subset F^{p-1}H^n  \subset \cdots \subset F^0 H^n := H^n
$$

such that

$$
  E_\infty^{p,q}  \simeq F^p H^{p+q} / F^{p+1}H^{p+q}
  \,.
$$

The notation for this is

$$
  E_r^{p,q} \Rightarrow H^{p+q}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

In applications one is interested in computing the $H^n$ and uses spectral sequences converging to this as tools for approximating $H^n$ in terms of the given filtration.

Therefore usually spectral sequences are required to converge in each degree, or even that for each pair $(p,q)$ there exists an $r_0$ such that for all $r\geq r_0$, $d_r^{p-r,q+r-1} = 0$.

=--

+-- {: .num_defn}
###### Definition
**(Collapse)**

A spectral sequence **collapses** at $r$ if in $E_r^{p,q}$ only a single row or a single column in non-vanishing.

=--

+-- {: .num_lemma}
###### Observation


If $(E_r)$ collapses at $r$, then it converges to $H^\bullet$ with $H^n$ being the unique entry $E^{p,q}_r$ on the non-vanishing row/column with $p+q = n$.

=--

### Graphical presentation

(...)

## Examples
 {#Examples}

The basic class of examples are

* [Spectral sequences of filtered complexes](#SpectralSequenceOfFilteredComplex)

which compute the cohomology of a [[filtered object|filtered complex]] from the cohomologies of its [[associated graded objects]]. 

From this one obtains as a special case the class of 

* [Spectral sequences of double complexes](#SpectralSequenceOfADoubleComplex)

which compute the cohomology of the [[total complex]] of a [[double complex]] using the two canonical filtrations of this by row- and by column-degree.

From this in turn one obtains as a special case the class of

* [Grothendieck spectral sequences](#GrothendieckSpectralSequence)

which compute the [[derived functor]] $\mathbb{R}^\bullet(G \circ F (-))$ of the composite of two functors from the spectral sequence of the double complex $\mathbb{R}^\bullet (F (\mathbb{R}^\bullet G (-)))$.

Many special cases of this for various choices of $F$ and $G$ go by special names, this we tabulate at

* _[List of examples](#ListOfExamples)_.




### Spectral sequence of a filtered complex
 {#SpectralSequenceOfFilteredComplex}

The fundamental example of a spectral sequence, from which essentially all the other examples arise as special cases, is the _[[spectral sequence of a filtered complex]]_. (See there for details).

If a [[cochain complex]] $C^\bullet$ is equipped with a [[filtered object|filtration]] $F^\bullet C^\bullet$, there is an induced filtration $F^\bullet H(C)$ of its [[cohomology groups]], according to which levels of the filtration contain representatives for the various cohomology classes.

A filtration $F$ also gives rise to an  [[associated graded object]] $Gr(F)$, whose grades are the successive level inclusion [[cokernels]].  Generically, the operations of grading and cohomology do not commute: 

$$
  Gr(F^\bullet H^\bullet(C)) \neq H^\bullet (Gr(F^\bullet) C)
  \,.
$$

But the [[spectral sequence of a filtered complex|spectral sequence associated to a filtered complex]] $F^\bullet C^\bullet$, passes through $H^\bullet (Gr(F^\star) C)$ in the page $E_{(1)}$ and in good cases converges to $Gr(F^* H^\bullet(C))$.


### Spectral sequence of a double complex
 {#SpectralSequenceOfADoubleComplex}

The [[total complex]] of a [[double complex]] is naturally filtered in two ways: by columns and by rows. By the above [[spectral sequence of a filtered complex]] this gives two different spectral sequences associated computing the cohomology of a double complex from the cohomologies of its rows and columns. Many other classes of spectral sequences are special cases of this cases, notably the [[Grothendieck spectral sequence]] and _its_ special cases. 

This is discussed at _[[spectral sequence of a double complex]]_.


### Spectral sequences for hyper-derived functors 
  {#HyperDerivedFunctors}

From the [[spectral sequence for a double complex]] one obtains as a special case a spectral sequence that computes [[hyper-derived fuctors]]. 

(...)

### Grothendieck spectral sequence 
 {#GrothendieckSpectralSequence}

The _[[Grothedieck spectral sequence]]_ computes the composite of two [[derived functors]] from the two derived functors separately.

Let $\mathcal{A} \stackrel{F}{\to} \mathcal{B} \stackrel{G}{\to} \mathcal{C}$ be two [[left exact functors]] between [[abelian categories]].

Write $R^p F : \mathcal{D} \to Ab$ for the [[cochain cohomology]] of the [[derived functor]] of $F$ in degree $p$ etc. 


+-- {: .num_theorem}
###### Theorem

If $F$ sends [[injective objects]] of $\mathcal{A}$ to $G$-[[acyclic objects]] in $\mathcal{B}$ then for each $A \in \mathcal{A}$ there is a [first quadrant](#FirstQuadrant) cohomology spectral sequence

$$
  E_r^{p,q} := (R^p G \circ R^q F)(A) 
$$

that converges to the right [[derived functor]] of the composite functor


$$
  E_r^{p,q} \Rightarrow R^{p+q} (G \circ F)(A).
$$

Moreover

1. the edge maps in this spectral sequence are the canonical morphisms
 
   $$
     R^p G (F A) \to R^p (G \circ F)(A)
   $$

   induced from applying $F$ to an injective resolution 
   $A \to \hat A$ and the [[isomorphism]]

   $$
     R^q (G \circ F)(A) \to G(R^q F (A))
     \,.
   $$

1. the [[exact sequence]] of low degree terms is

   $$
     0 \to (R^1 G)(F(A)) \to R^1(G \circ F)(A)
      \to F(R^1(G(A)))
      \to (R^2 F)(G(A))
      \to R^2(G \circ F)(A)
   $$

=--

This is called the _[[Grothendieck spectral sequence]]_.

+-- {: .proof}
###### Proof

Since for $A \to \hat A$ an injective [[resolution]] of $A$ the complex $F(\hat A)$ is a chain complex not concentrated in a single degree, we have that $R^p (G \circ F)(A)$ is equivalently the [[hyper-derived functor]] evaluation $\mathbb{R}^p(G) (F(A))$.

Therefore the second spectral sequence discussed at [hyper-derived functor spectral sequences](#HyperDerivedFunctors) converges as

$$
  (R^p G)H^q(F(\hat A)) \Rightarrow R^p (G \circ F)(A)
  \,.
$$

Now since by construction $H^q(F(\hat A)) = R^q F(A)$ this is a spectral sequence

$$
  (R^p G)(R^q F) A) \Rightarrow R^p (G \circ F)(A)
  \,.
$$

This is the Grothendieck spectral sequence.

=--

### Special Grothendieck spectral sequences 
 {#SpecialGrothendieckSpectralSequence}

* [Leray spectral sequence](#LeraySpectralSequence)

* [Hochschild-Serre spectral sequence](#HochschildSerreSpectralSequence)

* [Base-change spectral sequence](#BaseChangeSpectralSequence)

#### Leray spectral sequence
 {#LeraySpectralSequence}

The _[[Leray spectral sequence]]_ is the special case of the 
[[Grothendieck spectral sequence]] for the case where the two functors being composed are a [[direct image|push-foward]] of [[sheaves]] of [[abelian groups]] along a [[continuous map]] $f : X \to Y$ followed by the push-forward $X \to *$ to the point. This yields a spectral sequence that computes the [[abelian sheaf cohomology]] on $X$ in terms of the abelian sheaf cohomology on $Y$.

+-- {: .num_theorem}
###### Theorem

Let $X, Y$ be suitable [[sites]] and $f : X \to Y$ be a morphism of sites. () Let $\mathcal{C} = Ch_\bullet(Sh(X,Ab))$ and $\mathcal{D} = Ch_\bulle(Sh(Y,Ab))$ be the [[model structure on chain complexes|model categories of complexes of sheaves of abelian groups]]. The [[direct image]] $f_*$ and [[global section]] functor $\Gamma_Y$ compose to $\Gamma_X$:

$$
  \Gamma_X : \mathcal{C} \stackrel{f_*}{\to} \mathcal{D} \stackrel{\Gamma_Y}{\to} Ch_\bullet(Ab)
  \,.
$$

Then for $A \in Sh(X,Ab)$ a sheaf of abelian groups on $X$ there is a cohomology spectral sequence

$$
  E_r^{p,q} := H^p(Y, R^q f_* A)
$$

that converges as

$$
  E_r^{p,q} \Rightarrow H^{p+q}(X, A)
$$

and hence computes the cohomology of $X$ with coefficients in $A$ in terms of the cohomology of $Y$ with coefficients in the push-forward of $A$.

=--

#### Base change spectral sequence for $Tor$ and $Ext$
 {#BaseChangeSpectralSequence}

For $R$ a [[ring]] write $R$[[Mod]] for its category of [[modules]].
Given a [[homomorphism]] of [[ring]]s $f : R_1 \to R_2$ and an $R_2$-[[module]] $N$ there are composites of [[base change]] along $f$ with the [[hom-functor]] and the [[tensor product]] functor

$$
  R_1 Mod \stackrel{\otimes_{R_1} R_2}{\to} R_2 Mod \stackrel{\otimes_{R_2} N}{\to} Ab
$$

$$
  R_1 Mod \stackrel{Hom_{R_1 Mod}(-,R_2)}{\to}
  R_2 Mod
  \stackrel{Hom_{R_2}(-,N)}{\to}
  Ab
  \,.
$$

The [[derived functor]]s of $Hom_{R_2}(-,N)$ and $\otimes_{R_2} N$ are the [[Ext]]- and the [[Tor]]-functors, respectively, so the Grothendieck spectral sequence applied to these composites yields a  [[base change]] spectral sequence for these.

#### Hochschild-Serre spectral sequence
 {#HochschildSerreSpectralSequence}

* [[Hochschild-Serre spectral sequence]]

### Exact couples
 {: #exact_couples}

The above examples are all built on the [spectral sequence of a filtered complex](#SpectralSequenceOfFilteredComplex). An alternatively universal construction builds spectral sequences from _exact couples_.

An **[[exact couple]]** is an exact sequence of three arrows among two objects

$$ E \overset{j}{\to} D \overset{\varphi}{\to} D \overset{k}{\to} E \overset{j}{\to}. $$

These creatures construct spectral sequences by a two-step process:

*  first, the composite $ d \coloneqq k j \colon E\to E$ is nilpotent, in that $d^2=0$
*  second, the homology $E'$ of $(E,d)$ supports a map $j':E'\to \varphi D$, and receives a map $k':\varphi D\to E'$.  Setting $D'=\varphi D$, by general reasoning

$$ 
  E' \overset{j'}{\to} D' \overset{\varphi}{\to} D' \overset{k'}{\to} E' \overset{j'}{\to}
  \,. 
  $$
is again an exact couple.

The sequence of complexes $(E,d),(E',d'),\dots$ is a spectral sequence, by construction.

Examples of exact couples can be constructed in a number of ways.  Importantly, any short exact sequence involving two distinct chain complexes provides an exact couple among their total homology complexes, via the Mayer-Vietoris long exact sequence; in particular, applying this procedure to the relative homology of a filtered complex gives precisely the spectral sequence of the filtered complex described (???) somewhere else on this page.  For another example, choosing a chain complex of flat modules $(C^\dot,d)$, tensoring with the short exact sequence
$$ \mathbb{Z}/p\mathbb{Z} \to \mathbb{Z}/p^2\mathbb{Z} \to \mathbb{Z}/p\mathbb{Z} $$
gives the exact couple

$$ 
  H^\bullet(d,\mathbb{Z}/p^2\mathbb{Z})
    \overset{[\cdot]}{\to} 
  H^\bullet(d,\mathbb{Z}/p\mathbb{Z})
   \overset{\beta}{\to}
  H^\bullet(d,\mathbb{Z}/p\mathbb{Z})
   \overset{p}{\to}H^\bullet(d,\mathbb{Z}/p^2\mathbb{Z})\cdots
$$

in which $\beta$ is the _mod-$p$ Bockstein_ homomorphism.

The exact couple recipe for spectral sequences is notable in that it doesn't mention any grading on the objects $D,E$; trivially, an exact couple can be specified by a short exact sequence $\coker \varphi\to E\to \ker\varphi$, although this obscures the focus usually given to $E$.  In applications, a bi-grading is usually induced by the context, which also specifies bidegrees for the initial maps $j,k,\varphi$, leading to the conventions mentioned earlier.


### List of examples
 {#ListOfExamples}

(using material from [Wikipedia](#Wikipedia))

* [[Adams spectral sequence]] in [[stable homotopy theory]]

* [[Adams–Novikov spectral sequence]], a generalization to [[extraordinary cohomology theories]];

* [[Atiyah–Hirzebruch spectral sequence]] of an [[extraordinary cohomology theory]];


* [[Bar spectral sequence]] for the [[homology]] of the [[classifying space]] of a [[group]]

* [[Barratt spectral sequence]] converging to the [[homotopy]] of the initial space of a [[cofibration]]

* [[Bloch–Lichtenbaum spectral sequence]] converging to the [[algebraic K-theory]] of a [[field]]
    
* [[Bockstein spectral sequence]] relating the [[homology]] with $mod p$ coefficients and the homology reduced $mod p$

* [[Bousfield–Kan spectral sequence]] converging to the [[homotopy colimit]] of a [[functor]]

* [[Cartan–Leray spectral sequence]] converging to the [[homology]] of a [[quotient space]]

* [[Cech-to-derived functor spectral sequence]] from [[Čech cohomology]] to [[abelian sheaf cohomology]]
 
* [[change of rings spectral sequences]] for calculating [[Tor]] and [[Ext]] groups of modules

*  [[Chromatic spectral sequence]] for calculating the initial terms of the [[Adams–Novikov spectral sequence]]

* [[Connes spectral sequences]] converging to the [[cyclic homology]] of an algebra

* [[EHP spectral sequence]] converging to [[stable homotopy groups of spheres]]

* [[Eilenberg–Moore spectral sequence]] for the [[singular cohomology]] of the [[pullback]] of a [[fibration]]

* [[Federer spectral sequence]] converging to [[homotopy groups]] of a function space

* [[Frölicher spectral]] sequence starting from the [[Dolbeault cohomology]] and converging to the algebraic [[de Rham cohomology]] of a [[variety]]

* [[Green's spectral sequence]] for [[Koszul cohomology]]

* [[Grothendieck spectral sequence]] for composing [[derived functors]]

* [[Hodge–de Rham spectral sequence]] converging to the algebraic [[de Rham cohomology]] of a [[variety]]

* [[Hurewicz spectral sequence]] for calculating the [[homology]] of a space from its [[homotopy groups]]

* [[hyperhomology spectral sequence]] for calculating [[hyperhomology]]
 
* [[Künneth spectral sequence]] for calculating the homology of a [[tensor product]] of [[differential gradedalgebras]]

* [[Leray spectral sequence]] converging to [[abelian sheaf cohomology]]

* [[Leray–Serre spectral sequence]] of a [[fibration]]

* [[Lyndon–Hochschild–Serre spectral sequence]] in [[group cohomology]]

* [[May spectral sequence]] for calculating the [[Tor]] or [[Ext]] groups of an algebra

* [[Miller spectral sequence]] converging to the $mod p$ [[stable homology]] of a space

* [[Quillen spectral sequence]] for calculating the homotopy of a [[simplicial group]]
    
* [[spectral sequence of a double complex]] for computing the homology of a [[total complex]]

* [[spectral sequence of an exact couple]]

* [[Universal coefficient spectral sequence]]

* [[van Est spectral sequence]] converging to relative [[Lie algebra cohomology]]

* [[van Kampen spectral sequence]] for calculating the homotopy of a wedge of spaces.



## Properties

### Basic lemmas

+-- {: .num_lemma}
###### Lemma
**(mapping lemma)**

If $f : (E_r^{p,q} \to (F_r^{p,q}))$ is a morphism of spectral sequences such that for some $r$ we have that $f_r : E_r^{p,q} \toF_r^{p,q}$ is an isomorphism, then also $f_s$ is an isomorphism for all $s \geq r$.

=--

+-- {: .num_lemma}
###### Lemma
**(classical convergence theorem)**

(...)

=--

This is recalled in ([Weibel, theorem 5.51](#Weibel)).

### First quadrant spectral sequence 
 {#FirstQuadrant}

+-- {: .num_defn}
###### Definition

A **first quadrant spectral sequence** is one for wich all pages are concentrated in the first quadrant of the $(p,q)$-plane, in that

$$
  ((p \lt 0) or (q \lt 0))
  \;\;
  \Rightarrow
  E_r^{p,q} = 0
  \,.
$$


=--

+-- {: .num_lemma}
###### Observation

If the $r$th page is concentrated in the first quadrant, then so the $(r+1)st$ page. So if the first one is, then all are.

=--


+-- {: .num_lemma}
###### Observation

Every first quadrant spectral sequence converges at $(p,q)$ from $r \gt max(p,q+1)$ on

$$
  E_{max(p,q+1)+1}^{p,q} = E_\infty^{p,q}
  \,.
$$


=--

+-- {: .num_lemma}
###### Observation

If a first quadrant spectral sequence converges

$$
  E_r^{p,q} \Rightarrow H^{p+q}
$$

then each $H^n$ has a filtration of length $n+1$

$$
  0 = F^{n+1}H^n \subset F^n H^n \subset \cdots \subset F^1 H^n \subset F^0 H^n = H^n
$$

and we have

* $F^n H^n \simeq E_\infty^{n,0}$

* $H^n/F^1 H^n \simeq E_\infty^{0,n}$.

=--




## References



### Abelian/stable theory

An elementary pedagogical introduction is in 

* [[Timothy Chow]], _You could have invented spectral sequences_, Notices of the AMS (2006) ([pdf](http://www.ams.org/notices/200601/fea-chow.pdf))
 {#Chow}

Standard textbook references are 

* [[John McCleary]], _A User's Guide to Spectral Sequences_, Cambridge University Press 

chapter 5 of 

* [[Charles Weibel]], _An introduction to homological algebra_ Cambridge studies in advanced mathematics 38 (1994)
{#Weibel}

and section 14 of

* [[Raoul Bott]], [[Loring Tu]], _Differential forms in algebraic topology_, Graduate Texts in Mathematics __82__, Springer 1982. xiv+331 pp.

and

* [[Hal Schenck]], _Chapter 9: Cohomology and spectral sequences_ ([pdf](http://www.math.uiuc.edu/~schenck/tapp.pdf)) .


A textbook with a focus on applications in [[algebraic topology]] is

* [[Alan Hatcher]], _Spectral sequences in algebraic topology_ ([web](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html))
 {#Hatcher}

Reviews of and lecture notes on standard definitions and facts about spectral sequences include 

* Matthew Greenberg, _Spectral sequences_ ([pdf](http://www.math.mcgill.ca/goren/SeminarOnCohomology/specseq.pdf))

* [[Michael Hutchings]], _Introduction to spectral sequences_ ([pdf](http://math.berkeley.edu/~hutching/teach/215b-2011/ss.pdf))

* Daniel Murfet, _Spectral sequences_ ([pdf](http://therisingsea.org/notes/SpectralSequences.pdf))

* [[Neil Strickland]], _Spectral sequences_ ([pdf](http://neil-strickland.staff.shef.ac.uk/courses/bestiary/ss.pdf))

* Ravi Vakil, _Spectral Sequences: Friend or Foe?_ ([pdf](http://math.stanford.edu/~vakil/0708-216/216ss.pdf)) 

* Brandon Williams, _Spectral sequences_ ([pdf](http://www.math.sunysb.edu/~mbw/notes/orals/Spectral%20Sequences.pdf))

See also 

* Wikipedia, _[Spectral sequence](http://en.wikipedia.org/wiki/Spectral_sequence)_
 {#Wikipedia}

* A. Romero, J. Rubio, F. Sergeraert, _Computing spectral sequences_ ([pdf](http://www-fourier.ujf-grenoble.fr/~sergerar/Papers/Ana-JSC.pdf))

### Nonabelian / unstable theory {#ReferencesNonabelian}

Homotopy spectral sequences in model categories are discussed in 

* [[Aldridge Bousfield]], _Cosimplicial resolutions and homotopy spectral sequences in model categories_ ([arXiv:math/0312531](http://arxiv.org/abs/math/0312531)).

Spectral sequences in general categories with [[zero morphisms]] are discussed in 

* [[Marco Grandis]], _Homotopy spectral sequences_ ([arXiv:1007.0632](http://arxiv.org/abs/1007.0632))

### History

* [[John McCleary]], _A history of spectral sequences: Origins to 1953_, in _History of Topology_, edited by Ioan M. James, North Holland (1999) 631&#8211;663

[[!redirects spectral sequences]] 

