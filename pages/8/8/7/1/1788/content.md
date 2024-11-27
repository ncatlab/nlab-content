
**The Problem of Contemporary Quantum Computing.**

Ordinary quantum computing architectures 

> (such as with [spin resonance](nuclear+magnetic+resonance#SpinResonanceQBitsReferences), [superconducting qbits](superconductivity#SuperconductingQBitsReferences), [[trapped-ion quantum computing|trapped ions]], ...)

suffer from an intrinsic tension:

1. [[quantum gates]] are **implemented via [[interaction]]** between [[subsystems]],

1. but [[quantum coherence|coherence]] requires **avoiding interaction**

> (cf. [CCEHRSZ 07](quantum+computation#CCEHRSZ07) p 272: "*Quantum logic gates involving two atomic qubits must overcome the problem of the short range coherent interaction of neutral atoms, while maintaining atom confinement and suppressing decoherence. The main challenge is to perform the gate sufficiently fast compared to typical decoherence and relaxation times.*")

This is the problem that haunts contemporary [NISQ](quantum+computation#ReferencesNISQ) devices (whence "Quantum Winter", cf. [McKenzie 2024](quantum+computation#McKenzie2024)) 

\linebreak

**The bold idea of Topological Quantum Computing** is to cut this Gordian knot:

Find **quantum gates operating without interaction**!

Can this work? In principle: Yes! 

> (By a phenomenon known as the "[[quantum adiabatic theorem]]".)

\linebreak

For this we need a quantum system (like a crystalline material) with the following properties:

1. **degenerate ground states**:

   even when completely frozen at [[absolute zero]] [[temperature]]

   the system has more than one state to be in (even up to phase)

   > (Meaning: The [[Hilbert space]] $\mathscr{H}$ of [[quantum states]] with [[energy]] [[eigenvalue]] $E = 0$ is of [[dimension of a vector space|dimension]] $\geq 2$.)

2. an **energy gap** $\epsilon \gt 0$:

   every excitation of the ground state has energy larger than $\epsilon$

   so that ([[light]]) [[quanta]] impacting the material have **no interaction** as long as they carry energy $\lt \epsilon$.

   > (Meaning: The material's [[Hamiltonian]] has a [[spectral gap]] above the [[ground state]].)
  
3. **control parameters**:

   the above properties hold for a range of external tunable parameters

   such as [[strain]] or [[voltage]] applied to the crystal

   > (Meaning: A [[vector bundle]] of ground state Hilbert spaces $\mathscr{H}_p$ over a [[topological space]] $P$ of parameter values $p \in P$.)

\linebreak

**Adiabatic Transformation of Ground States.**

Under these conditions:

* after cooling such a system to its ground state,

* sufficiently slow ("[[quantum adiabatic theorem|adiabatic]]") variation of the external parameters

* does not excite the system: it remains in a ground state

* but **the different ground states may transform into each other**

  > (Meaning: Each parameter path $\gamma \,\colon\, p \to p'$ induces a [[Berry phase]] [[unitary operator]] $U_\gamma \,\colon\, \mathscr{H}_p \xrightarrow{\;} \mathscr{H}_{p'}$ )


\linebreak

This is part of a general phenomenon of [[quantum physics]]:

While [[quantum fluctuations]] are much like classical fluctuations

one key difference is that they remain present at [[absolute zero]].

> (Compare *[[quantum phase transitions]]*.)


\linebreak

Such operations on ground states are called **[holonomic quantum gates](adiabatic+quantum+computation#ReferencesGeometricPhaseGates)**

> (From "[[holonomy]]" for the [[parallel transport]] for a [[Berry connection]] along [[loops]].)

these are **protected from external noise** quanta of energy $\lt \epsilon$

**but** may still be sensitive no **noise in the parameter paths**.

\linebreak

**Topological invariance.**

To overcome this last issue, look for such quantum systems which in addition have

1. **parameter topology**

   the parameter space has "holes", in that

   some closed parameter paths cannot continuously be deformed to constant paths

   > (Meaning: The [[fundamental group]] of parameter space is non-[[trivial group|trivial]].)

1. **local parameter independence**

   all parameter paths with the same endpoints

   that are continuous deformations of each other

   yield the same transformation on ground states

   > (Meaning: The [[Berry connection]] is [[flat connection|flat]].)

[[quantum materials]] with all these properties are called [[topological order|topologically ordered]]

the resulting adiabatic quantum processes are **[[topological quantum computation|topological quantum gates]]**

\linebreak

In principle these are:

* protected against external noise quanta of energy $\lt \epsilon$

* *and* protected again any noise in the parameter path

in fact, the quantum operation induced by a parameter variation will

depend *only* on **how much the path winds around the holes** of parameter space

<center>
<a href="https://arxiv.org/pdf/2303.02382#page=21">
<img src="/nlab/files/TopologicalGateSchematics.jpg" width="740">
</a>
</center>

\linebreak

This way, 

topological quantum architecture may in principle 

(be necessary to) solve the problem of quantum computing.

> (cf. [Sau 2017](#Sau17), [Das Sarma 2022](topological+quantum+computation#DasSarma22))

\linebreak

This is the **theory behind topological quantum gates**

on the one hand it is extremely general: 

* any kind of topologically parameterized quantum system would do

on the other hand it is very ambitious: 

* suitable such system have yet to be devised in the labs

but the range of possibilities has hardly been explored,

most attention has been given to a single approach:

* braiding of anyonic defects in position space

This is what we discuss next. 


\linebreak



