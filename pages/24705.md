

## Quantum circuits via dependent linear types

The following discussion indicates[^1] how a natural [[quantum programming language]] for [[quantum information]]-processing protocols --- hence  for [[quantum circuits]] consisting of general [[quantum gates]] with classical control, including [[decoherence|de-coherent]] [[quantum measurement]]-gates and subsequent coherent quantum gates depending on these --- is elegantly subsumed within any [[dependent linear type theory|dependent linearly typed]] [[programming language]] which expresses the "[[yoga of six operations]]", such as is the case in the [[linear homotopy type theory]] of [Riley 2022](dependent+linear+type+theory#Riley22Thesis). 

[^1]: Full details to appear at: *[[schreiber:Topological Quantum Programming in Linear Homotopy Type Theory]]*.

This works by regarding classically controlled [[quantum states]] as having [[linear type|linear data types]] [[dependent type|dependent]] on classical control parameters and on measurement results, and then making the following key observations:

1. The "[[necessity]]" [[modality]] $\Box_C \coloneqq (p_C)^\ast (p_C)_\ast$ on [[linear types]] dependent on a given classical [[context]] $C$ (which includes classical control parameters as well as eventual [[quantum measurement]]-outcomes on the same footing) knows all about controlled [[quantum gates]]: These are identified just with the [[morphisms]] of the $\Box_C$-[[co-Kleisli category]], where the $\Box_C$-[[counit of a comonad|counit]] (taking a linear type "out of the comonad") reflects the [[quantum state collapse]] of [[quantum measurement]], and where the $\Box_C$-[[comultiplication]] encodes the [[superposition]]-principle.

1. The [[external tensor product]] of dependent linear types gives the compilation of [[quantum gates]] into [[quantum circuits]], essentially as familiar from the quantum [[string diagram]]-calculus of [Abramsky & Coecke 2004](finite+quantum+mechanics+in+terms+of+dagger-compact+categories#AbramskyCoecke04) with respect to the plain [[tensor product]], but now taking into account dependency on classical control and potential measurement outcomes. 

All constructions and proofs here flow readily from just the [[six operation yoga]] and [[co-Kleisli category|co-Kleisli theory]]. One key point is (eq:NecessityRespectsExternalTensorProduct) that the [[necessity]] [[modality]] respects the [[external tensor product]] -- so that these classically controlled quantum circuits are unambiguously defined --, under the assumption that it coincides with the [[formal duality|dual]] *[[possibility]]* modality $\lozenge_C \mathscr{H}_C$  on the quantum data types $\mathcal{H}_\bullet$ involved -- hence (in full generality) when the linear types are [[dualizable object|dualizable]] in the sense of [[ambidextrous adjunction|ambidexterity]] and specifically (in the traditional models) when [[space of quantum states|quantum state spaces]] are [[finite-dimensional vector space|finite dimensional]], as is the case in [[quantum information theory]].



Aspects of the following have a resemblance to some variants and categorical interpretations of the [[quantum programming language]] "[[Quipper]]" (see the references [there](Quipper#ReferencesDependentLinearTypesAndCategoricalSemantics)), but avoids (see [below](#NoticeTheTypingOfAQbit)) Quipper's problem of needing "dynamical lifting" (see [there](Quipper#ReferencesDynamicLifting)) of "measurement bits back into the context": The linear [[necessity]]-modality knows right away that measurement outcomes are recorded in the context. 

\linebreak

### General

We assume a [[dependent linear type theory]] which [[functor|functorially]] obtains (as anticipated in [Schreiber 2014](dependent+linear+type+theory#Schreiber14), [§3.2](https://arxiv.org/pdf/1402.7041.pdf#page=39) and established in [Riley 2022](dependent+linear+type+theory#Riley22Thesis), [§2.4](https://digitalcollections.wesleyan.edu/islandora/object/ir:3269)):

1. from a classical ("intuitionistic") [[type]] $X : Type$ a (large) type $LinType_X$ of [[linear types]] [[dependent type|dependent]] on $X$, equipped with [[symmetric monoidal category|symmetric]] [[closed monoidal category|closed monoidal structure]] $(-) \otimes (-)$ ([[tensor product]]) and $[-,\,-]$ ([[internal hom]]);

1. from a [[function]] $f : X_1 \xrightarrow{\;} X_2$ between classical types a [[yoga of six operations]] (specifically: a "[[Wirthmüller context]]") between their types of dependent linear types, hence a [[contravariant functor|contravariant]] [[substitution]]/[[pullback]] operation $f^\ast$ which is [[strong monoidal functor|strong monoidal]], [[strong closed functor|strong closed]] and extends to a [[base change]] [[adjoint triple]] (with [[left adjoint]] $f_!$ a version of [[dependent sum]] and [[right adjoint]] a version of [[dependent product]]):

\begin{imagefromfile}
    "file_name": "QCwthLHT-BaseChange-221001.jpg",
    "width": "730",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

First observe that (without imposing a further condition) also classical ("non-linear") [[dependent type theory]] provides an example of this [[yoga of six operations]] (actually five distinct operations, in the present case of [[Wirthmüller contexts]]), with:

1. [[tensor product]] given by [[product types]],

1. [[internal hom]] given by [[function types]],

1. $f^\ast$ given by [[context extension]],

1. $f_!$ given by [[dependent coproduct]],

1. $f_\ast$ given by [[dependent product]]. 

In this classical situation, the ([[comonad|co]]-)[[monad]] [[adjoint pair]] $\lozenge_C \dashv \Box_C$ induced by the [[adjoint triple]] is readily found (see [here](necessity+and+possibility#InFirstOrderLogicAndTypeTheory)) to reflect the [[necessity]]-[[modality]] and the [[possibility]]-[[modality]] of a kind of [[modal logic]] which regards the potential measurement outcomes $c : C$ as "[[possible worlds semantics|possible worlds]]":

\begin{imagefromfile}
    "file_name": "QCwthLHT-ClassicalNecessity-221001.jpg",
    "width": "900",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

We will say that a $C$-dependent linear type $\mathscr{H}_\bullet : LinType_C$ is *finite dimensional* if its [[possibility]]-aspect agrees with is [[necessity]] aspect, and we write $FDLinTyp_C$ for the subtype of the dependent linear types which are finite-dimensional. 

> (This finite-dimensionality needs more discussion...)

The default [[categorical semantics]] for this situation is that of [[bundles]] of [[finite dimensional vector spaces]] (finite-dimensional complex [[Hilbert spaces]]) over [[finite sets]]: In this case both $(p_C)_!$ as well as $(p_C)_\ast$ yield the [[direct sum]] of the [[fibers]] (a [[biproduct]]). Since this is the [[categorical semantics]] under which the following type theory describes the traditional [[quantum circuits]], we will adopt our notation to this case and denote the generic [[dependent linear type]] by $\mathcal{H}_\bullet : FDLinType_C$ and its generic [[term]] by the usual notation for [[quantum states]]: 

$$
  c : C 
  \;\;\;
  \vdash
  \;\;\; 
  \vert \psi_c \rangle \;\colon\; \mathcal{H}_c
  \,.
$$

Concretely, the [[linear homotopy type theory]] of [Riley 2022](dependent+linear+type+theory#Riley22Thesis) should have [[categorical semantics]] in the [[(infinity,1)-topos|$\infty$-topos]] of [[parameterized spectrum|parameterized]] [[Eilenberg-MacLane spectrum|$H\mathbb{C}$]]-[[module spectra]] ([[schreiber:Quantization via Linear homotopy types|S. 2014, Ex. 3.11]]) and [[complex vector spaces]] embed into this [[stable homotopy theory]] under passage to their [[Eilenberg-MacLane spectra]] (see the [[stable Dold-Kan correspondence]]).

In terms of this [[categorical semantics]], notice that on finite-dimensional linear types, $\Box_C$-**actualization is the measurement process** --  in that it implements exactly the rule for [[wavefunction collapse]] (due to [Lüders 1951](wave+function+collapse#Lüders51), following [von Neumann 1932, §III.3 and §VI](wave+function+collapse#vonNeumann32)) with regards to [[quantum  measurements]] in the $C$-indexed basis of the total Hilbert space 
$
  \mathcal{H} \coloneqq \Box_C \mathcal{H}_\bullet
$
which is encoded by its direct sum decomposition $\mathcal{H}_\bullet$:

\begin{imagefromfile}
    "file_name": "QCwthLHT-QuantumNecessity-221001.jpg",
    "width": "900",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


(Of course, in general there may be richer dependency on classical contexts. In the next simplest case the [[base change]] is along the [[projection]] map out of a [[Cartesian product]] of classical types, which makes one of them label potential upcoming measurement results as before, while the other encodes further dependency on classical parameters, such as on previous measurement results:

\begin{imagefromfile}
    "file_name": "QCwthLHT-RelativeBaseChange-221002.jpg",
    "width": "670",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This plays a role for classically-controlled quantum gates, [below](#ClassicallyControlledQuantumGate)).


Notice that it is the ambidexterity assumption --- $\lozenge \mathscr{H}_\bullet \simeq \Box \mathscr{H}_\bullet$ --- on linear dependent types  which,  in terms of [[modal logic]], formalizes the [[Gell-Mann principle]] of quantum physics:

$$
  \array{
    \llap{\text{The}}\;\text{possible}
    &
    \text{is} 
    &
    \text{necessary}
    &
    \text{and hence} 
    &
    \text{actualized}
    \\
    \lozenge \mathcal{H}_\bullet
    &
    \simeq
    &
    \Box \mathcal{H}_\bullet 
    &
    \xrightarrow{\phantom{--} \epsilon \phantom{--}} 
    &
    \mathcal{H}_{
      \bullet   
      \;
      \mathrlap{\text{with some probability}}
    }
  }
$$



With this observation in hand, it is a straightforward matter to verify that the [[morphisms]] in the [[co-Kleisli category]] of $\Box_C$ represent general [[quantum gates]], as we will illustrate [below](#QCwthLHT-QBits) for the case of traditional [[qbit]]-[[quantum gates]]:

\begin{imagefromfile}
    "file_name": "QCwthLHT-QuantumGates-221001.jpg",
    "width": "800",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


While quantum gates have [[horizontal composition]] in the [[co-Kleisli category]], they also have a [[vertical composition]] given by [[external tensor product]]:

\begin{imagefromfile}
    "file_name": "QCwthLHT-ExternalTensorProduct-221001.jpg",
    "width": "690",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

The point here is that the [[external tensor product]] records not just the [[tensor product]] on the given linear/quantum types, but also the fact that under combining two quantum gates/circuits, the types $C$ and $C'$ of their potential classical measurement outcomes combine into the type $C \times C'$ of [[pairs]] of outcomes (the [[Cartesian product]]) --- see the example of pairs of qbits, [below](#CombinationOfAPairOfQBits).



One checks that for ambidextrous/finite-dimensional dependent linear types, the [[necessity]]-[[modality]] respects the [[external tensor product]]:

\[
  \label{NecessityRespectsExternalTensorProduct}
  \Box_{C \times C'}
  \big(
    \mathscr{H}_\bullet
    \boxtimes
    \mathscr{H}'_\bullet
  \big)
  \;\simeq\;
  \Big(
    \big(
      \Box_{C}
      \mathscr{H}_\bullet
    \big)
    \boxtimes
    \big(
      \Box_{C '}
      \mathscr{H}'_\bullet
    \big)
  \Big)
\]


This implies that well-defined [[quantum circuits]] may be compiled from iterating between

1. horizontally composing morphisms in the [[co-Kleisli category]] of a [[necessity]]-modality applicable to given quantum types;

1. vertically adjoining such morphisms via their [[external tensor product]].

We illustrate [below](#QCwthLHT-QBits) how this provides a (programming) language for all tranditional quantum circuits compiled from [[qbits]].

But the expressiveness of the ambient [[linear homotopy type theory]] is considerably larger and allows to handle more general notions of [[quantum circuits]] with the same language structures. For instance:

1. We may use (in fact: construct) quantum types as building blocks which are not just [[qbits]] but much richer spaces of [[conformal blocks]] ([[schreiber:Topological Quantum Programming in TED-K|SS22]]). This allows to natively compile quantum programs for [[anyon]] [[braid representation|braid gates]] as used in [[topological quantum computation]].

1. Instead of just (parameterized) [[complex vector spaces]], the language of [[linear homotopy type theory]] in [Riley 2022](dependent+linear+type+theory#Riley22Thesis) handles more general ([[parameterized spectra|parameterized]]) [[Eilenberg-MacLane spectra|$H\mathbb{C}$]]-[[module spectra]], and in fact ([[parameterized spectra|parameterized]]) $R$-[[module spectra]] over any [[E-infinity ring|$E_\infty$-]][[ring spectrum]] $R$. 

  (A first example of [[quantum gates]] operating on [[spectra]] appears in the above-mentioned construction of [[conformal block]] if one just omits the fiberwise [[0-truncation]] in the last step.)




 
\linebreak

### QBits
 {#QCwthLHT-QBits}

A moment of reflection reveals that the [[linear type]] of a single (in-)coherent *[[qbit]]* is as follows, [[dependent linear type|depending]] on the classical [[type]] of [[booleans]] (which here we denote by "0" and "1" instead of "[[false]]" and "[[true]]") .


\begin{imagefromfile}
    "file_name": "QCwthLHT-QuantumBit-221001.jpg",
    "width": "840",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

The [[quantum measurement]]-process on such a qbit type, as seen by the [[necessity]]-[[counit of a comonad|counit]], verifies the [[wavefunction collapse|projection postulate]] of measurements in [[quantum mechanics]]:

\begin{imagefromfile}
    "file_name": "QCwthLHT-QBitMeasurement-221001.jpg",
    "width": "500",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

{#NoticeTheTypingOfAQbit} Notice that one might be tempted[^2] to think  of this formula as outputting the classical bit $b : \mathrm{Bool}$, but that the dependent typing of the above expression is a little more subtle than that:  The output bit is instead part of the *[[context]]* inside which the collapsed wavefunction qbit appears -- which, being in the 1-dimensional Hilbert space $\mathbb{C}$ in this case, may often be disregarded as a global phase, but is nevertheless the actual output of the measurement process.

[^2]: Indeed, in *[[Quipper]]* the measurement process on a qbit is originally typed as "$\QBit \to \Bit$" and further language design is needed to "bring the output bit back into the context", see references on "[dynamic lifting](Quipper#ReferencesDynamicLifting)".


In particular, by retaining the quantum type of the measurement result, we retain the ability to speak about repeated quantum measurement, which leads to a *proof* that the second measurement necessarily gives the same result as the first (the experimental observation of this fact is what originally led to the formulation of the projection postulate, in [von Neumann 1932, §III.3](wave+function+collapse#vonNeumann32)):

\begin{imagefromfile}
    "file_name": "QCwthLHT-QBitMeasurementRepeated-221001.jpg",
    "width": "400",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

{#CombinationOfAPairOfQBits} In the other (vertical) direction, the dependent linear type of the measurement of a [[pair]] of [[qbits]] comes out as expected, where the point to notice is how the [[external tensor product]] keeps track of the fact that a pair of qbits has $2 \times 2 = 4$ potential measurement outcomes:

\begin{imagefromfile}
    "file_name": "QCwthLHT-QBitPairMeasurement-221001.jpg",
    "width": "770",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}




Dually, the [[possibility]]-[[unit of a monad|unit]] on [[qbits]] is their *conditional state preparation* (this is the operation denoted "$\underline{a} \xleftarrow{\;} a$" in [Knill 1996](quantum+programming+language#Knill96), [p. 8](https://www.ncatlab.org/nlab/files/Knill-QuantumPseudocode.pdf#page=8)):

\begin{imagefromfile}
    "file_name": "QCwthLHT-QBitStatePreparationCondt-221001.jpg",
    "width": "400",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

From this, if we denote $\mathrm{const}_0 : \Bool \to \Bool$ 
the function [[constant function|constant]] on $0$, then  the *unconditional state preparation* (the operation denoted "$\underline{a} \xleftarrow{\;} 0$" in [Knill 1996](quantum+programming+language#Knill96), [p. 8](https://www.ncatlab.org/nlab/files/Knill-QuantumPseudocode.pdf#page=8)) is the base change of the conditional state preparation along this map:

\begin{imagefromfile}
    "file_name": "QCwthLHT-QBitStatePreparation-221001.jpg",
    "width": "400",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


The dependent linear type of the [[Hadamard gate]]:

\begin{imagefromfile}
    "file_name": "QCwthLHT-HadamardGate-221001.jpg",
    "width": "650",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

The dependent linear type of the [[CNOT gate]]:

\begin{imagefromfile}
    "file_name": "QCwthLHT-QuantumCNOTGate-221001.jpg",
    "width": "850",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


{#ClassicallyControlledQuantumGate} The dependent linear type of a quantum gate controlled by a classical bit:


\begin{imagefromfile}
    "file_name": "QCwthLHT-BitControlledQGate-221001.jpg",
    "width": "930",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}



This establishes all the ingredients of traditional [[quantum circuits]]. For instance, we obtain the measurement-controlled circuit that exhibits the [[quantum teleportation]]-protocol:

(...)


