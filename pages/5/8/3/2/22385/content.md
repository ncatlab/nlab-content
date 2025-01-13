+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Setoids
* table of contents
{: toc}

## Disambiguation
 {#Disambiguation}

In [[constructive mathematics]], such as in [[intuitionistic type theory]], the notion of *setoids* &lbrack;[Hofmann (1995)](#Hofmann95)&rbrack; is a formalization of the idea of *[[Bishop sets]]* (following [Bishop (1967)](#Bishop67)) and serves as a way of "constructively" speaking about [[quotient sets]] without, in a sense, actually constructing these: A setoid is essentially a [[set]] equipped with an [[equivalence relation]] or a similar [[structure]] (such as a *[[pseudo-equivalence relation]]*), and thought of as a stand-in for the would-be [[quotient set]] ([[quotient type]]) by that relation.

{#UsageInTheLiterature} Accounts which take setoids to be...

* ...actual [[equivalence relations]], i.e. $Setoids \coloneqq (X \colon Set) \times (R \colon X \times X \to {\color{purple}Prop}) \times ReflSymTrans(R)$: 

  [Hofmann (1995), §5.1.1](#Hofmann95); [Barthe, Capretta & Pons (2003), §2.1](#BartheCaprettaPons03); [Stacks Project](https://stacks.math.columbia.edu/tag/04S9); [hackage.haskell](https://hackage.haskell.org/package/setoid-0.1.0.0/docs/Data-Setoid.html);  [Wikipedia](https://en.wikipedia.org/wiki/Setoid);

* ...[[pseudo-equivalence relations]], i.e. $Setoids \coloneqq (X \colon Set) \times (R \colon X \times X \to {\color{purple}Set}) \times ReflSymTrans(R)$: 

  [Wilander (2012), §4](#Wilander12); [Palmgren & Wilander (2014), §2, §6](#PalmgrenWilander14); [Emmenegger & Palmgren (2020), §6](#EmmeneggerPalmgren20);  [Cipriano (2020), Def. 1.1.1](#Cipriano20),

* ... either:

  [van den Berg & Moerdijk (2018)](#vdBergMoerdijk18)

{#PointOfFirstDefinition} Here the definition of setoids in terms of [[equivalence relations]] may be closer to the original intention of [Bishop (1967)](#Bishop67) (though this remains a little vague) and is natural from the point of view of [[category theory]]/[[homotopy theory]] where setoids in this sense, and with equivalence of elements regarded as [[isomorphism]], are exactly those [[groupoids]] which are [[equivalence of categories|equivalent]] to sets (the [[0-truncated]] groupoids).

Another perspective is that setoids in the sense of equivalence relations consitute the [[ex/reg completion]] of [[Sets]], while those in terms of pseudo-equivalence relations constitute the [[ex/lex completion]] of [[Sets]].

In terms of [[type theory]], the definition in terms of [[equivalence relations]] is natural under the *[[propositions as some types]]*-paradigm, while the definition in terms of [[pseudo-equivalence relations]] is natural under the *[[propositions-as-types|types as propositions]]*-paradigm.



{#TerminologyDiffers} In any case, beware that terminology and definitions may differ significantly across authors, cf. [Palmgren (2005)](#Palmgren05) [p. 9](https://ncatlab.org/nlab/files/Palmgren-BishopSetTheory.pdf#page=9).

Setoids are also sometimes used in "impoverished" [[foundations of mathematics]] that lack a primitive notion of [[quotient set]]; see for instance *[[Bishop set]]*.

## Applications

In [[constructive mathematics]], we want the [[real numbers]] to form a [[linearly ordered set|linearly ordered]] [[Heyting field]] $R$ with completeness for located [[Dedekind cuts]].  Using [[power sets]] and a set $N$ of [[natural numbers]], one may form $R$ directly as a [[subset]] of $\mathcal{P}N$ (or something equivalent), but what if you wish to be (at least weakly) [[predicative mathematics|predicative]]? Using [[function sets]], one may form the Cauchy reals as a [[subquotient]] of $N^N$, but these are complete in the desired sense only if a weak form of [[countable choice]] (which follows from either the presentation axiom or [[excluded middle]]) holds. (Essentially, there may not be enough [[sequences]] of natural numbers.) Alternatively, if you have them, you can use [[prefunction]] sets and form $R$ as a subquotient of the set of _presequences_ of natural numbers.

The construction of $R$ above may also be done with entire relations if the [[axiom of fullness]] holds (see also [[real numbers object]]). Conversely, the axiom of fullness follows from the existence of sets of prefunctions; in addition to defining a functional entire prerelation, a prefunction between sets also defines an entire relation, and the set of these satisfies fullness.  (This is related to the idea that prefunctions between sets may be formalised as entire relations.)

See also the discussion at [[net]] about how to force the domain of a net to be [[partially ordered|partial order]], by using either entire relations or prefunctions as nets.

More generally, setoids (defined using [[equivalence relations]]) are [[thin category|thin]] [[groupoids]]. As a result, various concepts translate from the setting of [[category theory]] to setoid theory, such as

* [[monoidal setoid]]
* [[braided monoidal setoid]]
* [[groupal setoid]] (i.e. [[locally thin 2-category|locally thin]] [[2-groups]])
* [[braided groupal setoid]]
* [[ring setoid]]
* [[braided ring setoid]]

## Fixing inadequate foundations

Sometimes one finds a [[foundation]] of [[predicative mathematics]] in which it appears to be impossible to construct [[quotient sets]], leading to much hand-wringing. (For a simple example, simply remove the axiom of [[power sets]] from [[ZFC]] as normally presented.)  

Assuming (as usual) that the original foundation had equality relations on its sets, there will be identity prerelations on the presets, leading to a special class of sets which we may again call the __completely presented sets__. 

When you do this, the new kind of set is called a setoid, and then there may be hand-wringing about the need to use setoids instead of sets as one would like.  But if you didn\'t have quotient sets originally, then you shouldn\'t have been talking about 'sets' in the first place; theories of sets without quotient sets are really theories of presets. 

Some foundations also adopt an [[axiom of choice]] for functions which do not preserve the equivalence relation that, together with the identity relations, proves the [[presentation axiom]] for general sets, which means that free sets are completely presented sets. 

If you are willing to accept the [[presentation axiom]], then you can define a notion of setoid internal to a given theory of sets: as a [[projective set]]. (With the full axiom of choice, therefore, a setoid is simply a set.) Alternatively, you might forgo setoid as such but define a [[prefunction]] between sets to be an entire relation.

A similar result holds for [[SEAR plus epsilon|SEAR+$\epsilon$]].

## Related concepts

* [[Bishop set]]

* [[completely presented set]]

* [[equivalence relation]], [[pseudo-equivalence relation]]

* [[homotopy exact completion]]

* [[affine set]]

## References

The notion of "[[Bishop sets]]" goes to back the definition of sets in [[constructive mathematics]]/[[constructive analysis]] according to:

* {#Bishop67} [[Errett Bishop]], *[[Foundations of Constructive Analysis]]*, Mcgraw-Hill (1967)

* {#BishopBridges85} [[Errett Bishop]], [[Douglas Bridges]], p. 15 of:  *[[Constructive Analysis]]*, Grundlehren der mathematischen Wissenschaften **279**, Springer (1985) &lbrack;[doi:10.1007/978-3-642-61667-9](https://doi.org/10.1007/978-3-642-61667-9)&rbrack;

The connection to [[dependent type theory]] and the term *setoid* is due to 

* {#Hofmann95} [[Martin Hofmann]], §1.3, §5.1 in: _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh (1995), Distinguished Dissertations, Springer (1997) &lbrack;[ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]], [doi:10.1007/978-1-4471-0963-1](https://doi.org/10.1007/978-1-4471-0963-1)&rbrack;

Survey of further developments:

* {#BartheCaprettaPons03} [[Gilles Barthe]], Venanzio Capretta, [[Olivier Pons]], *Setoids in type theory*, Journal of Functional Programming **13** 2 (2003) 261-293 &lbrack;[doi:10.1017/S0956796802004501](https://doi.org/10.1017/S0956796802004501)&rbrack;

* {#Palmgren05} [[Erik Palmgren]],  _Bishop's set theory_ (2005) &lbrack;[pdf](http://www.cse.chalmers.se/research/group/logic/TypesSS05/Extra/palmgren.pdf), [[Palmgren-BishopSetTheory.pdf:file]]&rbrack;

See also:

* {#Wilander12} [[Olov Wilander]], *Constructing a small category of setoids*, Mathematical Structures in Computer Science **22** 1 (2012) 103-121 &lbrack;[doi:10.1017/S0960129511000478](https://doi.org/10.1017/S0960129511000478), [pdf](http://www.diva-portal.org/smash/get/diva2:399799/FULLTEXT01.pdf)&rbrack;

* {#PalmgrenWilander14} [[Erik Palmgren]], [[Olov Wilander]], *Constructing categories and setoids of setoids in type theory*, Logical Methods in Computer Science, **10** 3 (2014) lmcs:964 &lbrack;[arXiv:1408.1364](https://arxiv.org/abs/1408.1364), <a href="https://doi.org/10.2168/LMCS-10(3:25)2014">doi:10.2168/LMCS-10(3:25)2014</a>&rbrack;

* {#vdBergMoerdijk18} [[Benno van den Berg]], [[Ieke Moerdijk]], *Exact completion of path categories and algebraic set theory: Part I: Exact completion of path categories*, Journal of Pure and Applied Algebra **222** 10 (2018) 3137-3181 &lbrack;[doi:10.1016/j.jpaa.2017.11.017](https://doi.org/10.1016/j.jpaa.2017.11.017)&rbrack;


* {#EmmeneggerPalmgren20} [[Jacopo Emmenegger]], [[Erik Palmgren]], *Exact completion and constructive theories of sets*, J. Symb. Log. **85** 2  (2020) &lbrack;[arXiv:1710.10685](https://arxiv.org/abs/1710.10685), [doi:10.1017/jsl.2020.2](https://doi.org/10.1017/jsl.2020.2)&rbrack;


* {#Cipriano20} Cioffo Cipriano Junior, Def. 1.1.1 in: *Homotopy setoids and generalized quotient completion* &lbrack;[pdf](https://air.unimi.it/retrieve/d7ab68cc-fc12-4fe9-8a21-617deb888f36/phd_unimi_R12371.pdf), [[Cipriano-HomotopySetoids.pdf:file]]&rbrack;

* hackage.haskell, *[Data-Setoid.html](https://hackage.haskell.org/package/setoid-0.1.0.0/docs/Data-Setoid.html)*

* [[Stacks Project]], *Categories fibred in setoids* &lbrack;[tag:04S9](https://stacks.math.columbia.edu/tag/04S9)&rbrack;

* Wikipedia, *[Setoid](https://en.wikipedia.org/wiki/Setoid)*

category: disambiguation

[[!redirects setoids]]