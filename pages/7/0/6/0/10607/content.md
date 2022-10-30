[[!redirects adjoint cylinder]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of [[adjunction]] as such expresses a [[duality]]. The stronger concept of an _adjoint cylinder_ or _adjoint [[modality]]_ is specifically an [[adjunction]] between [[idempotent monad|idempotent (co-)monads]] and is meant to express specifically a _duality between opposites_. 

In terms of the corresponding [[adjoint triple]] of [[reflective subcategory|(co-)reflections]] and [[localizations]] the concept was suggested in ([Lawvere 91, p. 7](#Lawvere91), [Lawvere 94, p. 11](#Lawvere94)) to capture the phenomena of "Unity and Identity of Opposites" as they appear informally in [[Georg Hegel]]'s _[[Science of Logic]]_. 
(One might therefore say the notion is meant to capture the idea of "dialectic", though there is some debate as to whether Hegel's  somewhat mythical "creation out of [[paradox]]" should really go by this term, see [this Wikipeda entry](#Wikipedia) ).

In terms of [[adjoint pairs]] of [[modal operators]] in the context of [[modal logic]]/[[modal type theory]] and thought of as [[Galois connections]] the concept appears in ([Reyes-Zolfaghari 91](#ReyesZolfaghari91)). Further developments along these lines include ([DJK 14](#DJK14)).


## Definition

In ([Lawvere 94](#Lawvere94)) an _adjoint cylinder_ is defined to be an [[adjoint triple]] such that the induced [[adjoint pair]] on one of the two sides consists of [[identity]] functors.

This means equivalently that the other [[adjoint pair]] consists of an [[idempotent monad|idempotent]] [[monad]] and [[comonad]] ([[adjoint monads]]), either of the form

$$
  U \;\colon\; modality \dashv comodality
  \,,
$$

or in the form

$$
  U \;\colon\; comodality \dashv modality
  \,,
$$

hence is an [[adjoint pair]] of [[modal operators]] (as in _[[modal type theory]]_). A category equipped with an adjoint modality of the second form is called a _[[category of being]]_ in ([Lawver 91](#Lawvere91)). If the category is a [[topos]] then this is also called a _[[level of a topos]]_.

Given any such, we may say that the "unity" expressed by the two opposites is exhibited by the canonical [[natural transformation]]

$$
  U X 
  \;\colon\;
  \array{
    comodal X &\longrightarrow& X &\longrightarrow& modal X
    \\
    opposite\;1 && unity && opposite\;2
  }
$$

which is the composite of the [[counit of a comonad|counit of the comodality]] and the [[unit of a monad|unit of the modality]].

If for two [[level of a topos|levels]] the next one contains the [[modal types]] of the [[idempotent comonad]] of the former, then [[Lawvere]] speaks of "[[Aufhebung]]" (see there for more).

One can consider longer sequences of such adjoints of co/modalities, but the longer they get, the less likely they are to be non-trivial. The longest that still has good nontrivial models seems to be [[adjoint triples]] of modalities. Of these there is then similarly either the form

$$
  modality \dashv comodality \dashv modality
$$

(the "Yin triple") as for instance in the definition of _[[cohesion]]_ and

$$
  comodality \dashv modality \dashv comodality
$$

(the "Yang triple") as for instance in the definition of _[[differential cohesion]]_.

## Examples

### Werden : Sein $\dashv$ Nichts
 {#Werden}

For $\mathbf{H}$ a [[topos]]/[[(∞,1)-topos]] consider the "initial topos", the [[terminal category]] $\ast \simeq Sh(\emptyset)$ ([[category of sheaves]] on the empty site).

There is then an [[adjoint triple]]

$$
  \mathbf{H}
   \stackrel{\overset{\vdash \ast}{\longleftarrow}}{\stackrel{\overset{}{\longrightarrow}}{\underset{\vdash \emptyset}{\longleftarrow}}}
  \ast
$$

given by including the [[initial object]] $\emptyset$ and the [[terminal object]] $\ast$ into $\mathbf{H}$.

In the [[type theory]] of $\mathbf{H}$ this corresponds to the [[adjoint pair]] of [[modalities]]

$$
  \emptyset \dashv \ast
$$

which are constant on the [[initial object]]/[[terminal object]], respectively.

The induced unity transformation is

$$
  \array{
    \emptyset \longrightarrow X \longrightarrow \ast
  }
$$

hence the unique factorization of the unique function $\emptyset \longrightarrow \ast$ through any other [[type]].


Looking through ([Hegel 1812, vol 1, book 1, section 1, chapter 1](#Hegel1812)) one might call $\emptyset$ "nothing", call $\ast$ "being" and then call this unity of opposites "becoming". In particular in &#167;174 of _[[Science of Logic]]_ it says

> there is nothing which is not an intermediate state between being and nothing

which seems to be well-captured by the above unity transformation.

### Quantity : discreteness $\dashv$ continuity
 {#Mengen}

The adjoint modality in a [[local topos]] is that given by
[[flat modality]] $\dashv$ [[sharp modality]]

$$
  \flat \dashv \sharp
  \,.
$$

Capturing [[discrete objects]]/[[codiscrete objects]].

The corresponding unity transformation is

$$
    \flat X \longrightarrow X \longrightarrow \sharp X
$$

According to ([Lawvere 94, p. 6](#Lawvere94)) this unity captures the duality that in a [[set]] all [[elements]] are distinct and yet indistinguishable, an apparent [[paradox]] that may be traced back to [[Georg Cantor]].  

Looking through Hegel's [[Science of Logic]] at _[On discreteness and repulsion](#Science+of+Logic#OnDiscretenessAndRepulsion)_ one can see that matches with what Hegel calls

> (par 398) Quantity is the unity of these moments of continuity and discreteness

$$
  \array{
    \flat X &\longrightarrow& X &\longrightarrow& \sharp X
    \\
    {moment\;of \atop discreteness} && && {moment\;of \atop continuity}
  }
$$


### Continuuum : repulsion $\dashv$ cohesion
 {#ContinuumRepulsionCohesion}

For $\mathbf{H}$ a [[cohesive topos]]/[[cohesive (∞,1)-topos]]
the [[shape modality]] $\dashv$ [[flat modality]] constitute an adjoint cylinder

$$
  \int \dashv \flat
  \,.
$$

The corresponding unity-transformation is the [points-to-pieces transform](cohesive%20topos#CanonicalComparison)

$$
  \array{
    \flat X \longrightarrow X \longrightarrow \int X
  }
$$

Looking through ([Hegel 1812, vol 1, book 1, section 2, chapter 1](#Hegel1812)) one might call $\flat$ "repulsion", call $\int$ "attraction"/"[[cohesion]]" and then call this unity of opposites "[[continuum]]". Indeed, by the discussion at _[[cohesive topos]]_, this does quite well capture the geometric notion of continuum geometry.

### Infinitesimal Continuuum : infin. repulsion $\dashv$ infinit. cohesion
 {#ContinuumRepulsionCohesion}

For $\mathbf{H}$ equipped moreover with [[differential cohesion]],
there is the [[infinitesimal object|infinitesimal]] version of 
[[shape modality]] $\dashv$ [[flat modality]]  namely the adjoint modality

[[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]]


$$
  \int^{inf} \dashv \flat^{inf}
  \,.
$$

The corresponding unity-transformation is the 

$$
  \array{
    \flat^{inf} X \longrightarrow X \longrightarrow \int^{inf} X
  }
$$

maps from the [[coefficients]] for [[crystalline cohomology]] to the [[de Rham space]] of types $X$, where all infinitesimal neighbour points are identified. 

In view of the above the unity exhibited here is clearly to be called the "infinitesimal continuum".



### Cohesive sets

The combination of the above two examples of [Continuum](#ContinuumRepulsionCohesion) and [Quantity](#Mengen) is an [[adjoint triple]] of [[modalities]]

$$
  \int \;\dashv\; \flat \;\dashv\; \sharp
$$

[[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]

characteristic of a [[cohesive topos]].

### Skeleta and Co-Skeleta

[[simplicial skeleton]] $\dashv$ [[simplicial coskeleton]]


### Formal completion $\dashv$ Torsion approximation
 {#FormalCompletionAndTorsionApproximation}

For $A$ a [[commutative ring]] or more generally an [[E-∞ ring]] and $\mathfrak{a}\subset \pi_0 A$ a suitable ideal, then $\mathfrak{a}$-[[adic completion]] and $\mathfrak{a}$-[[torsion approximation]] form an adjoint modality on $A MMod$ the [[stable (∞,1)-category|stable]] [[(∞,1)-category of ∞-modules]] $A Mod_\infty$ over $A$. 

  ($\mathfrak{a}$-adic completion) $\dashv$ ($\mathfrak{a}$-torsion approximation)

+-- {: .num_prop #CompletionTorsionAdjointModalityForModuleSpectra}
###### Proposition

Let $A$ be an [[E-∞ ring]] and let $\mathfrak{a} \subset \pi_0 A$ be a [[generators and relations|finitely generated]] ideal in its underlying [[commutative ring]].

Then there is an [[adjoint triple]] of [[adjoint (∞,1)-functors]]

$$
  \array{
    \underoverset{
      A Mod_{\mathfrak{a}comp}^{op}}
    {A Mod_{\mathfrak{a}tors}^{op}}
    {\simeq}
    &\stackrel{\overset{\Pi_{\mathfrak{a}}}{\longleftarrow}}{\stackrel{\hookrightarrow}{\underset{\flat_{\mathfrak{a}}}{\longleftarrow}}}&
    A Mod^{op}
  }
$$

where

* $A Mod$ is the [[stable (∞,1)-category|stable]] [[(∞,1)-category of modules]], i.e. of [[∞-modules]] over $A$;

* $A Mod_{\mathfrak{a}tor}$ and $A Mod_{\mathfrak{a} comp}$ are the [[full sub-(∞,1)-categories]] of $\mathfrak{a}$-[[torsion approximation|torsion]] and of $\mathfrak{a}$-[[completion of a module|complete]] $A$-[[∞-modules]], respectively;

* $(-)^{op}$ denotes the [[opposite (∞,1)-category]];

* the [[equivalence of (∞,1)-categories]] on the left is induced by the restriction of $\Pi_{\mathfrak{a}}$ and $\flat_{\mathfrak{a}}$.

=--

+-- {: .proof}
###### Proof

This is effectively the content of ([Lurie "Proper morphisms", section 4](#LurieProper)):

* the existence of $\Pi_{\mathfrak{a}}$ is corollary 4.1.16 and remark 4.1.17

* the existence of $\flat_{\mathfrak{a}}$ is lemma 4.2.2 there;

* the equivalence of sub-$\infty$-categories is proposition 4.2.5 there.

=--


See at _[[fracture theorem]]_ for more.

### Totally distributive categories

For $\mathcal{K}$ a [[totally distributive category]]
it induces on its [[category of presheaves]] an adjoint modality whose [[right adjoint]] is the [[Yoneda embedding]] $Y$ postcomposed with its [[left adjoint]] $X$.

## Related concepts

* [[Aufhebung]]

* [[modal type theory]]

* [[category of being]]

* [[Galois connection]]

## References

### In terms of adjoint triples of (co-)reflections and localizations

In terms of [[adjoint triples]] of [[reflective subcategory|(co-)reflections]] and [[localization of a category|localizations]] the concept appears in 

* {#Lawvere91} [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ in A. Carboni, M. Pedicchio, G. Rosolini, _Category Theory_  , [[Como|Proceedings of the International Conference held in Como]], Lecture Notes in Mathematics 1488, Springer (1991)
 

* {#Lawvere94} [[William Lawvere]], _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_, Philosophia Mathematica (3) Vol. 2 (1994), pp. 5-15. ([[LawvereCohesiveToposes.pdf:file]])
  

* {#Lawvere96} [[William Lawvere]],  _[[Unity and Identity of Opposites in Calculus and Physics]]_,  Proceedings of ECCT 1994 Tours Conference,  Applied Categorical Structures, 4: 167-174 Kluwer Academic Publishers, (1996).
 

motivated as a formalization of ideas expressed in

* {#Hegel1812} [[Georg Hegel]], _[[Science of Logic]]_, 1812
 
But according to 

* {#Lambek} [[Joachim Lambek]], _The Influence of Heraclitus on Modern Mathematics_, In _Scientific Philosophy Today: Essays in Honor of Mario Bunge_, edited by Joseph Agassi and Robert S Cohen, 111&#8211;21. Boston: D. Reidel Publishing Co.

the thought that [[adjunction]] is the formal incarnation of dialectic philosophical sentiment going back at least to [[Heraclitus]] emerged in discussion between Lambek and Lawvere in 1965-66

* {#Wikipedia} Wikipedia, _[Hegelian dialectic](http://en.wikipedia.org/wiki/Hegelian_dialectic)_

### In terms of adjoint pairs of modal operators
  
In terms of [[adjoint pairs]] of [[modal operators]] and hence of [[Galois connections]], the concept appears in 

* {#ReyesZolfaghari91} [[Gonzalo  Reyes]], H. Zolfaghari, _Topos-theoretic approaches to modality_, Lecture Notes in Mathematics 1488 (1991), 359-378.

* {#Reyes91} [[Gonzalo Reyes]], _A topos-theoretic approach to reference and modality_, Notre Dame J. Formal Logic Volume 32, Number 3 (1991), 359-391 ([Euclid](http://projecteuclid.org/euclid.ndjfl/1093635834))

with further developments in 

* M. Sadrzadeh, R. Dyckho, _Positive logic with adjoint modalities: Proof
theory, semantics and reasoning about information_, Electronic Notes in Theoretical
Computer Science 249, 451-470, 2009, in _Proceedings of the 25th Conference on
Mathematical Foundations of Programming Semantics_ (MFPS 2009).

* {#Hermida10} [[Claudio Hermida]], section 3.3. of _A categorical outlook on relational modalities and simulations_, 2010 ([pdf](http://maggie.cs.queensu.ca/chermida/papers/sat-sim-IandC.pdf))

* {#DJK14} Wojciech Dzik, Jouni J&#228;rvinen, Michiro Kondo, _Characterising intermediate tense logics in terms of Galois connections_ ([arXiv:1401.7646](http://arxiv.org/abs/1401.7646))

For an overview of the role of adjunctions in modal logic see:

* [[Matías Menni|M. Menni]], C. Smith, _Modes of Adjointness_ , J. Philos. Logic **43** no.3-4 (2014) pp.365-391.

### Examples

* {#LurieProper} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_ 

[[!redirects adjoint cylinders]]

[[!redirects adjoint modality]]
[[!redirects adjoint modalities]]

[[!redirects opposite]]
[[!redirects opposites]]

[[!redirects unity of opposites]]
[[!redirects unity and identity of opposites]]

[[!redirects dialectic]]
[[!redirects dialectics]]

[[!redirects duality of opposites]]
[[!redirects dualities of opposites]]