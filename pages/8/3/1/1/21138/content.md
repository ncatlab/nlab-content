

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contrents#
* table of contents
{:toc}

## Idea

### Statement

A famous [[conjecture]] in [[non-perturbative effect|non-perturbative]] [[string theory]] says ([Minasian-Moore 97](#MinasianMoore97), [Witten 98](#Witten98), reviewed in [Witten 00](#Witten00), [Moore 02](#Moore02), [Manjarín 04](#Manjarin04), [Evslin 06](#Evslin06), [Fredenhagen 08](#Fredenhagen08)) that [[D-brane charge]] and [[RR-field]] [[fluxes]] are [[Dirac charge quantization|quantized]] in the [[Whitehead-generalized cohomology theory]] known as [[topological K-theory]], specifically in [[KU]]-cohomology for [[type II string theory]] and more generally in [[KR cohomology theory]] in the presence of [[orientifolds]], reducing to [[KO]]-cohomology in [[type I string theory]] right on the [[O-planes]].

More generally, the [[conjecture]] says that the [[fluxes]] of the NS [[B-field]] and of the [[RR-fields]] are jointly [[Dirac charge quantization|flux-quantized]] in [[twisted topological K-theory]], with the [[B-field]] constituting the twist.

Yet more generally, the conjecture says that, over [[orbifolds]], the [[Dirac charge quantization|charge quantization]] is in [[orbifold K-theory]], hence in [[equivariant K-theory]] for the usual [[global quotient orbifolds]], hence in [[twisted equivariant K-theory]] for the combined [[B-field]]/[[RR-fields]]. A sketch of how to state this more precisely is in [Distler-Freed-Moore 09](#DistlerFreedMoore09).

This means, or would mean, that the full massless [[field (physics)|physical fields]] in [[type II string theory]], including their higher "[[gauge potentials]]", are [[cocycles]] in a [[differential cohomology]]-version of these [[twisted cohomology|twisted]] [[generalized cohomology theories]], hence in [[differential K-theory]] if the B-field is ignored, in [[twisted differential K-theory]] if the B-field is included, and in [[twisted equivariant differential K-theory]] if also [[orbifolds]] are taken into account.

### Motivation

An immediate way to motivate the conjecture is to notice that the image of the $H^3$-[[twisted Chern character]] on [[twisted K-theory]] (say in degree 0, hence in [[type IIA string theory]], for definitess) 

\begin{imagefromfile}
    "file_name": "TwistedChernCharacterAndRRFluxBianchi.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [SS20](https://ncatlab.org/schreiber/show/Twisted+Cohomotopy+implies+M5-brane+anomaly+cancellation))"
\end{imagefromfile}


takes values in $H_3$-[[twisted de Rham cohomology]], whose [[cocycles]] are collections of [[differential forms]] satisfying exactly the [[Bianchi identities]] 

$$
  d \, H_3 = 0
  \,,
  \;\;\;
  d\, F_{2k + 2} = H_3 \wedge F_{2k}
$$

expected of the [[B-field]] [[flux]] $H_3$ and the [[RR-field]] [[fluxes]] $F_{2k}$. This is ultimately what underlies the observation in [Minasian-Moore 97](#MinasianMoore97), as brought out clearly in [Brodzki-Mathai-Rosenberg-Szabo 06](#BrodzkiMathaiRosenbergSzabo06).


\begin{imagefromfile}
    "file_name": "AntiBraneAnnihilationAsKGroupEquivRelation.jpg",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Sch 18](https://ncatlab.org/schreiber/show/Equivariant+Stable+Cohomotopy+and+Branes)"
\end{imagefromfile}

A conceptual picture of why [[topological K-theory]] would capture [[D-brane]] charge was suggested in [Witten 98, Section 3](#Witten98): The [[tachyon condensation]] expected (this is _[[Sen's conjecture]]_ from [Sen 98](Sen's+conjecture#ReferencesForSuperstrings)) for [[open strings]] between [[D-brane]]/[[anti-D-branes]] plausibly implements on their [[Chan-Paton gauge field|Chan-Paton]] [[vector bundles]] the defining [[equivalence relation]] ([here](topological+K-theory#eq:DefiningEquivalenceRelation)) of [[topological K-theory]], as indicated in the figure.

While plausible and widely accepted in the string theory [[folklore]], this picture remains to be checked (see [below](#CheckingChenConjecture)).


## Open problems
 {#OpenProblems}

While the conjecture that D-brane charge is in K-theory has become widely accepted [[folklore]] in much of the [[string theory]]-community, it remains unproven -- just as many and most [[folklore]]-statements involving [[non-perturbative effect|non-perturbative]] [[brane]]-physics, not the least because an actual [[theory (physics)|theory]] of non-perturbative string theory (aka [[M-theory]]) remains missing (see also at _[M-theory -- the open problem](M-theory#TheOpenProblem)_).

Moreover, there are a number of indications that the conjecture can not actually be true without some modification, as in parts it seems to be in contradiction with other accepted facts about string theory. We list some of these issues in the following.

Since the full [[non-perturbative effect|non-perturbative]] [[M-theory]]-completion of [[string theory]] is thought to involve not [[D-branes]] coupled to the [[B-field]]/[[RR-fields]]], but their lift (through the [[duality between type IIA string theory and M-theory]]) to [[M-branes]] coupled to the [[supergravity C-field|C-field]], what is arguably missing ([BDHKMMS 01, Sec. 4.6.5](#BDHKMMS01))
is an [[M-brane]]/[[supergravity C-field|C-field]] [[Dirac charge quantization|charge/flux quantization]] law, which would reduce to something close to K-theoretic charge quantization in the appropriate limit. See the last item [below](#LiftToMTheory).


### Checking Sen's conjecture
 {#CheckingChenConjecture}

While the proposal of  [Witten 98, Section 3](#Witten98) to explain the K-theory charge quantization conjecture via [[Sen's conjecture]] on [[tachyon condensation]] for [[open string|open]] [[superstrings]] stretched between [[D-brane]]/[[anti D-brane]] pairs has become widely accepted [[folklore]], the closest available towards an actual check of this argument via [[Sen's conjecture|open superstring tachyon condensation]] seems to be [Erler 13](#Erler13) which, however, concludes (on [p. 32](https://arxiv.org/pdf/1308.4400.pdf#page=32)) with:

> It would also be interesting to see if these developments can shed light on the long-speculated relation between string field theory and the K-theoretic description of D-brane charge $[$[75, 76, 77](D-brane#DBraneChargeQuantizationInTopologicalKTheory)$]$. We leave these questions for future work.

See also [Erler 19](#Erler19) which still lists this (on [p. 112](https://arxiv.org/pdf/1912.00521.pdf#page=113)) among open problems of [[string field theory]]:

> Are there topological invariants of the open string star algebra representing D-brane charges?

### Incompatibility with S-duality

Taken at face value, the K-theory conjecture applied to [[type IIB string theory]] breaks the expected [[S-duality]] symmetry of the theory: Under this [[duality in string theory|duality]] the [[B-field]] $H_3$-flux form and the [[RR-field]] 3-flux $F_3$ appear on the same footing and in particular mix as [[linear combinations]] (jointly coupling to _[[(p,q)-strings]]_), while in [[twisted K-theory]] $H_3$ is part of the twist, while $F_3$ is part of what is being twisted, with no evident way to mix these two concepts.

(see also [Evslin 06, Sec. 8.3](#Evslin06))



### Spurious fractional D-brane charges

An old argument of [BDHKMMS 01, Sec. 4.5.2](#BDHKMMS01) says that [[equivariant K-theory]] by itself produces spurious [[fractional D-brane]] charges that need to be eliminated by some modification of the K-theory conjecture. 

Evidence that this correction is provided by lifting to [[equivariant stable Cohomotopy]] instead ([[schreiber:Hypothesis H]]) is offered in [[schreiber:Lift of fractional D-brane charge to equivariant Cohomotopy theory|BSS 20]].


### Spurious D-brane charges on group manifolds

Similarly, the analysis of [[boundary conformal field theory]] describing [[open strings]] on [[Lie groups]] ([[WZW models]]) does not seem to always agree with the conjectured K-theory classification of the corresponding [[D-branes]]:

[Fredenhagen-Quella 05](#FredenhagenQuella05):

> It might surprise that despite all the progress that has been made in understanding branes on group manifolds, there are usually not enough D-branes known to explain the whole charge group predicted by (twisted) K-theory.

### Lift to M-theory
 {#LiftToMTheory}

Finally, the lift of the putative [[D-brane]] [[Dirac charge quantization|charge quantization]] in [[string theory]] to an [[M-brane]] [[Dirac charge quantization|charge quantization]] in [[M-theory]] has remained largely open and problematic, as maybe first highlighted in [BDHKMMS 01, Sec. 4.6.5](#BDHKMMS01) for a variety of reasons.

However, a highly non-trivial check in [DMW 00](#DMW00) successfully matched
the first non-trivial differential in the [[Atiyah-Hirzebruch spectral sequence]] for [[topological K-theory]], applied on the RR-flux component $F_4$, to a constraint on the [[supergravity C-field|C-fied]] flux $G_4$ obtained from a [[path integral]]-argument in [[D=11 supergravity]].

Incidentally, this and related conditions on the [[supergravity C-field|C-field]] derived in [DMW 00](#DMW00) from a [[path integral]]-argument in [[D=11 supergravity]] are all implied also by the [[schreiber:Hypothesis H]] that the [[supergravity C-field|C-field]], in turn, is [[Dirac charge quantization|charge quantized]] in [[twisted Cohomotopy theory]] ([[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation on 8-manifolds|FSS 19]]).

## Properties

### Holographic relation to topological phases of matter

Under [[AdS/CFT duality in solid state physics]] the [[K-theory classification of topological phases of matter]] corresponds to the [[K-theory classification of D-brane charge]] ([Ryu-Takayanagi 10a](#RyuTakayanagi10a), [Ryu-Takayanagi 10v](#RyuTakayanagi10b)).


## Related concepts

* [[Dirac charge quantization]]

* [[shifted C-field flux quantization]]

* [[K-theory classification of topological phases of matter]]

## References


[[!include D-brane charge quantization in topological K-theory -- references]]




[[!redirects D-brane charge quantization in topological K-theory]]

[[!redirects K-theory classification of D-brane charge]]

