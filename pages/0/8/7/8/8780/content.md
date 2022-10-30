
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Schubert calculus#
* table of contents
{:toc}

## Idea

Schubert calculus is a formal calculus in [[enumerative geometry]], which geometrically reduces to the combinatorics and [[intersection theory]] of so-called __Schubert cells__ in [[Grassmannians]]. 

Schubert calculus is concerned with the [[ring]] structure on the [[cohomology]] of [[flag varieties]] and [[Schubert varieties]]. Traditionally this is considered for [[ordinary cohomology]] (see [References -- traditional](#ReferencesTraditional)) later also for [[generalized cohomology theories]] (see [References -- In generalized cohomology](#ReferencesInGeneralizedCohomology)), notably in [[complex oriented cohomology theory]] such as [[K-theory]], [[elliptic cohomology]] and [[algebraic cobordism]].

The rigorous foundations of Schubert calculus is the content of 15th of [[Hilbert's problems]].

## Details

### Flag varieties and Schubert varieties

The basic data to be fixed is a sequence of inclusions

$$
  T \subset B \subset G
$$

where

* $G$ is a [[connected topological space|connected]] [[complex geometry|complex]] [[reductive group|reductive]] [[algebraic group]]

* $B$ is a [[Borel subgroup]]

* $T$ is a [[maximal torus]].

This induces

* the [[Weyl group]] $W_0 = N(T)/T$;

* the [[character lattice]] $\mathfrak{h}_{\mathbb{Z}}^\ast = Hom(T, \mathbb{C}^\times)$;

* the [[cocharacter lattice]] $\mathfrak{h}_{\mathbb{C}} = Hom(\mathbb{C}^\times, T)$.

* a _[[standard parabolic subgroup]]_ of $G$ is a subgroup $P_J$ including $B$ such that $G/P$ is a [[projective variety]];

   [[parabolic subgroup]] is one [[conjugation|conjugate]] to the standard parabolic subgroup.

* the [[flag variety]] $G/B$;

* the _[[partial flag varieties]]_ $G/P_J$

* the [[Bruhat decomposition]] is the [[coproduct]] decomposition

  $$
    G = \underset{w \in W_0}{\coprod} B w B
  $$

  $$
    G =  \underset{u \in W^J}{\coprod} B u P_j
  $$

  with 

  * $W_J \coloneqq \{v \in W_0 | v T  \subset P_J\}$

  * $W^J \coloneqq \{coset\; representatives\; u \; of \; cosets \; in W_0/W_J\}$

* into the [[Schubert varieties]]

  $$
    X_W = \overline{B w B} \subset G/B
  $$

  $$
    X_u^J = \overline{B u P_J} \subset G/P_J
    \,.
  $$

## Related concepts

* [[Dirac induction]]

* [[twistor space]]

## References

### Traditional
 {#ReferencesTraditional}

* [eom]: Frank Sotile, [Schubert calculus](http://www.encyclopediaofmath.org/index.php/Schubert_calculus)
* wikipedia [Schubert calculus](http://en.wikipedia.org/wiki/Schubert_calculus)
* H. Schubert, _Kalk&#252;l der abz&#228;hlenden Geometrie_, Springer (1879) (Reprinted (with an introduction by S. Kleiman): 1979), [MR0555576](http://www.ams.org/mathscinet-getitem?mr=0555576)

* S.L. Kleiman, D. Laksov, _Schubert calculus_, Amer. Math. Monthly __79__ (1972) pp. 1061&#8211;1082, [MR0323796](http://www.ams.org/mathscinet-getitem?
mr=0323796), [jstor](http://www.jstor.org/stable/2317421)

### In generalized cohomology theory
 {#ReferencesInGeneralizedCohomology}

Discussion of Schubert calculus in [[generalized cohomology theories]] is in

* [[Paul Bressler]], Sam Evens. _The Schubert calculus, braid relations,
and generalized cohomology_. Trans. Amer. Math. Soc.,
317(2):799&#8211;811, 1990
 {#BresslerEvens90}

* [[Paul Bressler]], Sam Evens, _Schubert calculus in complex cobordism_
Trans. Amer. Math. Soc., 331(2):799&#8211;813, 1992

* Baptiste Calm&#232;s, Victor Petrov,  Kirill Zainoulline, _Invariants,
torsion indices and oriented cohomology of complete flags_
May 200 ([web](http://front.math.ucdavis.edu/0905.1341))

* Jens Hornbostel, Valentina Kiritchenko, _Schubert calculus for
algebraic cobordism_. J. Reine Angew. Math., 656:59&#8211;85, 2011

* [[Nora Ganter]], [[Arun Ram]], _Generalized Schubert calculus_, [arxiv/1212.5742](http://arxiv.org/abs/1212.5742)


[[!redirects Hilbert's 15th problem]]


category: combinatorics, algebraic geometry