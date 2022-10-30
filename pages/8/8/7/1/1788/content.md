
## Quantum circuits via dependent linear types

The following indicates how quantum protocols in [[quantum information theory]] -- hence  [[quantum circuits]] consisting of general [[quantum gates]] with classical control, including [[decoherence|de-coherent]] [[quantum measurement]]-gates -- are naturally formulated in [[dependent linear type theory]], with classically controlled [[quantum states]] regarded as having [[linear type|linear data types]] [[dependent type|dependent]] on the classical control parameters and measurement results. The key observation is that:

1. The [[necessity]] [[modality]] $\Box_C \coloneqq (p_C)^\ast (p_C)_\ast$ on [[linear types]] dependent on a given classical [[context]] $C$ (which includes classical control parameters as well as eventual [[quantum measurement]]-outcomes on the same footing) knows all about controlled [[quantum gates]]: These are identified with the [[morphisms]] in its [[co-Kleisli category]], with the $\Box_C$-[[counit of a comonad|counit]] (taking a linear type "out of the comonad") reflecting the operation of [[quantum measurement]] (and the [[comultiplication]] encoding the [[superposition]]-principle).

1. The [[external tensor product]] of dependent linear types gives the compilation of [[quantum gates]] into [[quantum circuits]], essentially as familiar from the quantum [[string diagram]]-calculus of [Abramsky & Coecke 2004](finite+quantum+mechanics+in+terms+of+dagger-compact+categories#AbramskyCoecke04) with respect to the plain [[tensor product]], but now taking into account all classical control and all potential measurement outcomes. 

All this flows readily from the abstract theory, the only extra observation involved is that the necessity modality respects the external tensor product -- and hence that these classically controlled quantum circuits are unambiguously defined --, which follows when the [[modality]] of *[[necessity]]* $\Box_C \mathscr{H}_\bullet$ coincides with that of *[[possibility]]* $\bigcirc_C \mathscr{H}_C$ on the quantum data types $\mathbb{H}_\bullet$ involved -- hence (in full generality) when the linear types are [[dualizable object|dualiable]] in the sense of [[ambidextrous adjunction|ambidextrous]] and specifically (in the traditional model) when [[space of quantum states|quantum state spaces]] are [[finite-dimensional vector space|finite dimensional]], as usual in [[quantum information theory]].

In summary, the following shows that every [[dependent linear type theory|dependent linearly-typed]] [[programming language]] as in [Riley 2022](dependent+linear+type+theory#Riley22Thesis) *automatically* is a [[quantum programming language]] for classically controlled [[quantum circuits]] (as such somewhat akin to [[Quipper]] but entirely avoiding Quipper's problem of needing "dynamical lifting" of "bits back into the context", see [below](#NoticeTheTypingOfAQbit)). 

### General

We assume a [[dependent linear type theory]] which [[functor|functorially]] obtains (as anticipated in [Schreiber 2014](dependent+linear+type+theory#Schreiber14), [§3.2](https://arxiv.org/pdf/1402.7041.pdf#page=39) and established in [Riley 2022](dependent+linear+type+theory#Riley22Thesis), [§2.4](https://digitalcollections.wesleyan.edu/islandora/object/ir:3269)):

1. from a classical ("intuitionistic") [[type]] $X : Type$ a (large) type $LinType_X$ of [[linear types]] [[dependent type|dependent]] on $X$, equipped with [[symmetric monoidal category|symmetric]] [[closed monoidal category|closed monoidal structure]] $(-) \otimes (-)$ ([[tensor product]]) and $[-,\,-]$ ([[internal hom]]);

1. from a [[function]] $f : X_1 \xrightarrow{\;} X_2$ between classical types a [[yoga of six operations]] (specifically: a "[[Wirthmüller context]]") between their types of dependent linear types, hence a [[contravariant functor|contravariant]] [[substitution]]/[[pullback]] operation $f^\ast$ which is [[strong monoidal functor|strong monoidal]], [[strong closed functor|strong closed]] and extends to a [[base change]] [[adjoint triple]] (with [[left adjoint]] $f_!$ a version of [[dependent sum]] and [[right adjoint]] a version of [[dependent product]]):

\begin{imagefromfile}
    "file_name": "QCwthLHT-BaseChange-221001.jpg",
    "width": "650",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Notice that before emposing a further condition, classical [[dependent type theory]] provides an example of this [[yoga of six operations]] (fic distinct operations, in our case), with 

1. tensor product given by [[product types]]

1. [[internal hom]] given by [[function types]]

1. $f^\ast$ given by [[context extension]]

1. $f_!$ given by [[dependent coproduct]] 

1. $f_\ast$ given by [[dependent product]]. 

In this classical situation the ([[comonad|co]]-)[[monad]] [[adjoint pair]] induced by the adjoint triple is readily found (see [here](necessity+and+possibility#InFirstOrderLogicAndTypeTheory)) to reflect the [[necessity]]-[[modality]] and the [[possibility]]-[[modality]] with respect to the given context:

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

The default [[categorical semantics]] for this situation is that of [[bundles]] of [[finite dimensional vector spaces]] (finite-dimensional complex [[Hilbert spaces]]) over [[finite sets]] of: In this case both $(p_C)_!$ as well as $(p_C)_\ast$ yield the [[direct sum]] of the [[fibers]] (a [[biproduct]]). Since this is the [[categorical semantics]] under which the following type theory describes the traditional [[quantum circuits]], we will adopt our notation to this case and denote the generic [[dependent linear type]] by $\mathcal{H}_\bullet : FDLinType_C$ and its generic [[term]] by the usual notation for [[quantum states]]: 

$$
  c : C \;\vdash\; \vert \psi_c \rangle \;\colon\; \mathcal{H}_c
  \,.
$$

Concretely, the [[linear homotopy type theory]] of [Riley 2022](dependent+linear+type+theory#Riley22Thesis) should have [[categorical semantics]] in the [[(infinity,1)-topos|$\infty$-topos]] of [[parameterized spectrum|parameterized]] [[Eilenberg-MacLane spectrum|$H\mathbb{C}$]]-[[module spectra]] ([[schreiber:Quantization via Linear homotopy types|S. 2014, Ex. 3.11]]) and complex [[vector spaces]] embed into this [[stable homotopy theory]] under passage to the [[Eilenberg-MacLane spectra]] of their underlying [[abelian group]].

In terms of this semantics, notice that on finite-dimensional linear types, $\Box_C$-**actualization is the measurement process** --  in that it implements exactly the rule for [[wavefunction collapse]] (due to [Lüders 1951](wave+function+collapse#Lüders51), following [von Neumann 1932, §III.3 and §VI](wave+function+collapse#vonNeumann32)) with regards to measurements in the $C$-indexed basis of the total Hilbert space 
$
  \mathcal{H} \coloneqq \box_C \mathcal{H}_\bullet
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





One checks that for finite-dimensional dependent linear types, the [[necessity]]-[[modality]] respects the [[external tensor product]]:

\[
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


 
\linebreak

### QBits
 {#QCwthLHT-QBits}

The [[dependent linear type]] of a  *[[qbit]]*:


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

The [[quantum measurement]]-process on such a qbit type, as seen by the [[necessity]]-[[counit of a comonad|counit]] gives the expected projection rule:

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

{#NoticeTheTypingOfAQbit} Notice that one might be tempted[^1] to think  of this formula as outputting the classical bit $b : \mathrm{Bool}$, but that the dependent typing of the above expression is a little more subtle than that:  The output bit is instead part of the *context* inside which the collapsed wavefunction qbit appears -- which, being in the 1-dimensional Hilbert space $\mathbb{C}$ in this case, may often be disregarded as a global phase, but is nevertheless the actual output of the measurement process.

[^1]: Indeed, in *[[Quipper]]* the measurement process on a qbit is originally typed as "$\QBit \to \Bit$" and further language design is needed to "bring the output bit back into the context", see references on "dynamical lifting".


In particular, by retaining the quantum type of the measurement result, we retain the ability to speak about repeated quantum measurement, which leads to a *proof* that the second measurement necessarily gives the same result as the first (the experimental observation of this fact is what led [[John von Neumann]] to formulate the projection postulate, in [von Neumann 1932, §III.3 and §VI](wave+function+collapse#vonNeumann32)):

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

In the other direction, the dependent linear type of the measurement of a [[pair]] of [[qbits]] is this:

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




Dually, the [[possibility]]-[[unit of a monad|unit]] on [[qbits]] is their *conditional state preparation*:

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

and we denote $\mathrm{const}_0 : \Bool \to \Bool$ 
the function constant on $0$, then  the unconditional state preparation is the base change of the conditional state preparation along this map:

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

The dependent linear type of a quantum gate controlled by a classical bit:

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


(...)


