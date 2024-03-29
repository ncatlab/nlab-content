

{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***



$\,$


This entry is a detailed introduction to [[stable homotopy theory]], hence to  the [[stable homotopy category]] and to its key computational tool, the [[Adams spectral sequence]]. To that end we introduce the modern tools, such as [[model categories]] and [[highly structured ring spectra]]. In the accompanying [[Introduction to Stable homotopy theory -- S|seminar]] we consider applications to [[cobordism theory]] and [[complex oriented cohomology]] such as to converge in the end to a glimpse of the modern picture of [[chromatic homotopy theory]].



$\,$

***



{#AA} Lecture notes. $\;\;\;\;\;\;\;$ (web version requires Firefox browser -- [free download](https://www.mozilla.org/en-US/firefox/new/))
<br/>
<br/>



_[[Introduction to Stable homotopy theory -- P|Prelude -- Classical homotopy theory]]_ ([[IntroductionToStableHomotopyTheory-P-170509.pdf:file]] 111 pages)
<br/>
<br/>
_[[Introduction to Stable homotopy theory -- 1|Part 1 -- Stable homotopy theory]]_ 
<br/>
<br/>
$\,\,$ _[[Introduction to stable homotopy theory -- 1-1|Part 1.1 -- Sequential Spectra]]_ ([[IntroductionToStableHomotopyTheory-1-1-170509.pdf:file]], 79 pages)
<br/>
<br/>
$\,\,$ _[[Introduction to Stable homotopy theory -- 1-2|Part 1.2 -- Structured Spectra]]_ ([[IntroductionToStableHomotopyTheory-1-2-170509.pdf:file]], 75 pages)
<br/>
<br/>
_[[Introduction to Stable homotopy theory -- I|Interlude -- Spectral sequences]]_ ([[IntroductionToStableHomotopyTheory-I-170509.pdf:file]], 15 pages)
<br/>
<br/>
_[[Introduction to Stable homotopy theory -- 2|Part 2 -- Adams spectral sequences]]_ ([[IntroductionToStableHomotopyTheory-2-170509.pdf:file]], 53 pages)
<br/>
<br/>
_[[Introduction to Cobordism and Complex Oriented Cohomology|Examples and Applications -- Cobordism and Complex Oriented Cohomology]]_ ([[IntroductionToStableHomotopyTheory-S-161227.pdf:file]], 76 pages)
<br/>
<br/>
**total file** ([[IntroductionToStableHomotopyTheory-170509.pdf:file]], 418 pages)
<br/>
<br/>
Background reading:
<br/>
<br/>
_[[schreiber:Introduction to Homological algebra|Background -- Introduction to Homological algebra]]_ ([[IntroductionToHomologicalAlgebra-170509.pdf:file]], 83 pages)
<br/>
<br/>
_[[Introduction to Topology|Background -- Introduction to Topology]]_ ([pdf](https://ncatlab.org/nlab/files/IntroductionToTopologyI-170509.pdf), 122 pages)

***


$\,$

$\,$

#Contents#
* table of contents
{:toc}


<div style="float:right;margin:0 10px 10px 0;"> <img src="https://ncatlab.org/nlab/files/HopfFibration.jpg" width="200" />  </div>

$\,$

***

$\,$

> My initial inclination was to call this book [[The Music of the Spheres]], but I was dissuaded from doing so by my diligent publisher, who is ever mindful of the sensibilities of librarians. ([Ravenel 86, preface](#Ravenel86))


## Survey
 {#Introduction}

We are concerned with the theory of _[[spectra]]_ in the sense of [[algebraic topology]]: the proper generalization of [[abelian groups]] to [[homotopy theory]]. 

### 1) Stable homotopy theory
 {#StableHomotopyTheorySurvey}

A [[group]] in homotopy theory is equivalently a [[loop space]] under concatenation of loops ("[[∞-group]]"). A double loop space is a group with some commutativity structure ("[[Eckmann-Hilton argument]]"), a triple loop space has more commutativity structure, and so forth. A _spectrum_ is where this progression of [[looping and delooping]] _stabilizes_ (an "$\infty$-abelian group"). Therefore one speaks of _[[stable homotopy theory]]_:

$$
  Spaces
  \;\;
  \underoverset{(linearization)}{stabilization}{\mapsto}
  \;\;
  Spectra
  \,.
$$

Most of [[linear algebra]] and [[algebraic geometry]] passes along as [[abelian groups]] are generalized to [[spectra]] and turns into something remarkably rich, called _[[brave new algebra]]_, _[[higher algebra]]_ and _[[E-∞ geometry|spectral geometry]]_. In particular the analog of the theory of ([[commutative ring|commutative]]) [[rings]] and their [[modules]] exists, given by ([[commutative ring spectrum|commutative]]) [[ring spectra]] ([[E-∞ rings]], [[A-∞ rings]]) and [[module spectra]] ([[∞-modules]]). 

### 2) Adams spectral sequences
 {#ANSS}

Since spectra are considerably richer than abelian groups, stable homotopy is much concerned with "[[fracture theorem|fracturing]]" stable homotopy types into more tractable components:

To that end, notice that from the point of view of [[arithmetic geometry]], an [[abelian group]] $A$ is equivalently a [[quasicoherent sheaf]] over [[Spec(Z)]]. 

$$
  AbelianGroups \simeq QCoh(Spec(\mathbb{Z}))
  \,.
$$

This point of view generalizes to homotopy theory and turns out to be very fruitful there. The analog of the [[integers]] $\mathbb{Z}$ is the [[sphere spectrum]] $\mathbb{S}$, and this is naturally the [[initial object in an (infinity,1)-category|initial]] [[commutative ring spectrum]] ("[[E-∞ ring]]"), just as $\mathbb{Z}$ is the [[initial object|initial]] [[commutative ring]]. The [[formal dual]]  [[Spec(S)]] of $\mathbb{S}$ is hence the [[terminal object in an (infinity,1)-category|terminal]] [[space]] in [[E-∞ arithmetic geometry]] ("[[spectral geometry]]") and [[spectra]] are equivalently the [[quasicoherent ∞-stacks]] over $Spec(\mathbb{S})$

$$
  Spectra \simeq QCoh(Spec(\mathbb{S}))
  \,.
$$

Therefore the study of spectra "[[fracture theorem|fractures]]" into the various [[localizations]] and [[formal completions]] of $Spec(\mathbb{S})$. Since this is like the white light of $Spec(\mathbb{S})$ decomposing into various wavelengths, one speaks of _[[chromatic homotopy theory]]_. 

In particular, an  [[E-∞ ring]] $E$ is [[formal dual|dually]] a morphism of $E_\infty$-algebraic spaces $Spec(E) \longrightarrow Spec(\mathbb{S})$ and under good conditions the [[1-image]] of this map is the formal dual of the [[Bousfield localization of spectra|localization]] $L_E \mathbb{S}$ at $E$:

$$
  Spec(E) \stackrel{epi_1}{\longrightarrow} Spec(L_E \mathbb{S}) \stackrel{mono_1}{\longrightarrow} Spec(\mathbb{S})
 \,.
$$

This means that $Spec(E) \longrightarrow Spec(L_E \mathbb{S})$ is a [[cover]] and that hence $E$-local spectra are equivalently [[quasicoherent ∞-stacks]] on $Spec(E)$ equipped with [[descent data]]: [[formal dual|dually]] they are [[∞-modules]] over $E$ equipped with [[comodule]] structure over the [[Hopf algebroid]] ([[Sweedler coring]]) $E \otimes_{\mathbb{S}} E$.

The computation of [[homotopy groups]] of spectra that make use of their decomposition this way into $E$-[[∞-modules]] equipped with [[descent]] data is the _$E$-[[Adams spectral sequence]]_, a central tool of the theory.

### S) Complex oriented cohomology

For this reason special importance is carried by those [[E-∞ rings]] such that $Spec(E) \to Spec(\mathbb{S})$ is already a [[covering]], in a suitable sense, for these the $E$-[[∞-modules]] equipped with descent data give an equivalent, but in general more tractable, incarnation of the stable homotopy theory of spectra.

Curiously, this way a good bit of [[differential topology]] -- [[cobordism theory]] -- arises within stable homotopy theory: the archetypical $Spec(E)$ which covers $Spec(\mathbb{S})$ in a suitable sense is $E = $ [[MU]], the [[Thom spectrum]] representing [[complex cobordism cohomology]].

An [[commutative ring spectrum]] $E$ over $MU$, hence a $Spec(E)\to Spec(MU)$ is now a [[multiplicative cohomology theory|multiplicative]] "[[complex oriented cohomology theory]]". 

$\,$

***

$\,$


## **Prelude) Classical homotopy theory**
 {#ClassicalHomotopyTheory}

$\,$


This section is at: _[[Introduction to Stable homotopy theory -- P]]_

$\,$

$\,$


## **Part 1) Stable homotopy theory**
 {#StableHomotopyTheory}

$\,$

This section is at _[[Introduction to Stable homotopy theory -- 1]]_

$\,$

$\,$


## **Interlude) Spectral sequences**
 {#SpectralSequences}

$\,$


This section is at _[[Introduction to Stable homotopy theory -- I]]_

$\,$

$\,$


## **Part 2) Adams spectral sequences**

$\,$

This section is at _[[Introduction to Stable homotopy theory -- 2]]_

$\,$

$\,$


## **Seminar) Complex oriented cohomology**
 {#ComplexOrientedCohomology}

$\,$


This section is at _[[Introduction to Stable homotopy theory -- S]]_

$\,$


$\,$

***

$\,$

## References
 {#References}

### Basic reading

For **Prelude) Classical homotopy theory** a concise and self-contained re-write of the proof ([Quillen 67](#Quillen67)) of the [[classical model structure on topological spaces]] is in

* {#Hirschhorn15} [[Philip Hirschhorn]], _The Quillen model category of topological spaces_ ([arXiv:1508.01942](http://arxiv.org/abs/1508.01942)).

For general [[model category]] theory a decent concise account is in

* {#DwyerSpalinski95} [[William Dwyer]], J. Spalinski, _[[Homotopy theories and model categories]]_ ([pdf](http://folk.uio.no/paularne/SUPh05/DS.pdf)) in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ 1995

For the restriction to the [[convenient category of topological spaces|convenient category]] of [[compactly generated topological spaces]] good sources are

* {#Lewis78} [[Gaunce Lewis]], _Compactly generated spaces_ ([pdf](http://www.math.uchicago.edu/~may/MISC/GaunceApp.pdf)), appendix A of _The Stable Category and Generalized Thom Spectra_ PhD thesis Chicago, 1978

* {#Strickland09} [[Neil Strickland]], _The category of CGWH spaces_, 2009 ([pdf](http://neil-strickland.staff.shef.ac.uk/courses/homotopy/cgwh.pdf))

For section **1) Stable homotopy theory** we follow the modern picture of the stable homotopy category for which an enjoyable survey may be found in

* {#Malkiewich14} [[Cary Malkiewich]], _The stable homotopy category_, 2014 ([pdf](http://math.uiuc.edu/~cmalkiew/stable.pdf)).

The classical account in ([Adams 74, part III sections 2, 4-7](#Adams74)) is still a good read, but ignore the "[[Adams category]]"-construction of the [[stable homotopy category]] in sections III.2 and III.3. What we actually do follows 

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))

For the discussion of [[ring spectra]] we pass to [[symmetric spectra]] and [[orthogonal spectra]]. A compendium on the former is in

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))


For **Interlude: Spectral sequences** a discussion streamlined for our purposes is in ([Rognes 12, section 2](#Rognes12)).

In **2) Adams spectral sequence** for the general theory we follow 

* {#Adams74} [[Frank Adams]], _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

* {#Bousfield79} [[Aldridge Bousfield]], sections 5 and 6 of _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))


For the special case of the [[classical Adams spectral sequence]] we follow ([Kochman 96, chapter V](#Kochman96)).


For the **Seminar on Complex oriented cohomology** an excellent textbook to hold on to is

* {#Kochman96} [[Stanley Kochman]], _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

Specifically for **S.1) Generalized cohomology** a neat account is in:

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))


For **S.2) Cobordism theory** an efficient collection of the highlights is in

* {#Malkiewich11} [[Cary Malkiewich]], _Unoriented cobordism and $M O$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/cobordism.pdf))

except that it omits proof of the [[Leray-Hirsch theorem]]/[[Serre spectral sequence]] and that of the [[Thom isomorphism]], but see the references there and see ([Kochman 96](#Kochman96), [Aguilar-Gitler-Prieto 02, section 11.7](#AguilarGitlerPrieto02)) for details.
 
For **S.3) Complex oriented cohomology** besides ([Kochman 96, chapter 4](#Kochman96)) have a look at [Adams 74, part II](#Adams74) and

* {#Lurie10} [[Jacob Lurie]], lectures 1-10 of _[[Chromatic Homotopy Theory]]_, 2010

(These overlap, pick the one that seems more inviting on first reading.)

### Further reading

The two originals

* {#Quillen67} [[Daniel Quillen]], _Axiomatic homotopy theory_ in  _Homotopical algebra_, Lecture Notes in Mathematics, No. 43 43, Berlin (1967)

* {#Brown73} [[Kenneth Brown]], _[[Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458  ([JSTOR](http://www.jstor.org/stable/1996573))

are still an excellent source. For further reading on homotopy theory and stable homotopy theory a useful collection is

* {#James95} [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_ 1995

The modern chromatic picture originates around

* {#Hopkins99} [[Mike Hopkins]], _[[Complex oriented cohomology theories and the language of stacks]]_, 1999 

a useful survey is in

* {#Wilson13} [[Dylan Wilson]] section 1.2 of _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at _[2013 Pre-Talbot Seminar](http://math.harvard.edu/~hirolee/pretalbot2013/)_, March 2013 ([[DylanWilsonOnANSS.pdf:file]])

a wealth of details is in

* {#Ravenel86} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1987/2003 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))

and new foundations have been laid in

* {#LurieHigherAlgebra} [[Jacob Lurie]], _[[Higher Algebra]]_



[[!redirects Introduction to Stable homotopy theory]]


[[!redirects geometry of physics -- stable homotopy types]]
[[!redirects geometry of physics -- stable homotopy theory]]
