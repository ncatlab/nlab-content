<div class="rightHandSide toc">
[[!include physicscontents]]
</div>



> under construction

Quantum information refers to data that can be physically stored in a [[quantum mechanics|quantum system]]. 

Quantum information theory is the study of how such information can be encoded, measured, and manipulated. A notable sub-field is _quantum computation_, a term often used synonymously with quantum information theory, which studies protocols and algorithms that use quantum systems to perform computations.

Categorical quantum information refers to a program in which the cogent aspects of [[Hilbert space]]-based quantum information theory are abstracted to the level of [[symmetric monoidal categories]].

#Contents#
* automatic table of contents goes here
{:toc}

## Hilbert space quantum mechanics

+--{: .query}
TODO: decide whether to shift this section to [[quantum mechanics]].
=--

In pure state quantum mechanics, physical states are encoded as vectors in a [[Hilbert space]]. Often Dirac "bra-ket" notation is used to represent such vectors, where $|\psi\rangle$ represents a state and $\langle\psi|$ represents its linear adjoint. State evolutions are expressed as unitary maps. Self-adjoint operators represent physical quantities such such as position and [[momentum]] and are called observables. Measurements are expressed as sets of projectors onto the eigenvectors of an observable.

In mixed state quantum mechanics, physical states are represented as density operators $\rho$, state evolution as maps of the form $\rho \mapsto U^\dagger \rho U$ for unitary maps $U$, and measurements are positive operator-valued measures (POVM's). There is a natural embedding of pure states into the space of density matrices: $|\psi\rangle \mapsto |\psi\rangle\langle\psi|$. So, one way to think of mixed states is a probabilistic mixture of pure states.

\[ \rho = \sum_i a_i |\psi_i\rangle\langle\psi_i| \]

Composite systems are formed by taking the tensor product of Hilbert spaces. If a pure state $|\Psi\rangle \in H_1 \otimes H_2$ can be written as $|\psi_1\rangle \otimes |\psi_2\rangle$ for $|\psi_i\rangle \in H_i$ it is said to be _separable_. If no such $|\psi_i\rangle$ exist, $|\Psi\rangle$ is said to be _entangled_. If a mixed state is separable if it is the sum of separable pure states. Otherwise, it is entangled.

States, state evolutions, and observables are all special cases of [[quantum channels]] which can be used to describe the exchange of classical and quantum [[information]].

### Quantum protocols and algorithms

Brief synopsis of teleportation, entanglement swapping, BB84, E91, Deutsch-Jozsa, Shor.

+--{: .query}
[[Ian Durham]]: Should we maybe somehow link the quantum mechanics section to this?  Teleportation and entanglement, to me, are quantum phenomena that transcend their use in quantum information theory (the others, I agree, are purely information-theoretical).

[[Aleks Kissinger]]: Entanglement I agree with, though the description of teleportation as a protocol (as opposed to a phenomenon) probably belongs here.

[[Ian Durham]]: Yes, I'd agree with that.  It's description is usually in terms of a protocol.  Actually, I suppose it's status as a "phenomenon" is somewhat debatable.
=--

## Categorical formulation

The linear adjoint $(-)^\dagger$ gives Hilbert spaces the structure of a [[†-category]]. The category of Hilb of Hilbert spaces forms a **&#8224;-symmetric monoidal category**, that is, a [[symmetric monoidal category]] equipped with a symmetric monoidal functor $(-)^\dagger$ from $Hilb^{op}$ to $Hilb$. Furthermore, the category FHilb of _finite dimensional_ Hilbert spaces forms a **&#8224;-compact closed category**, or a [[compact closed category]] such that $A_*$ := $(A^*)^\dagger = (A^\dagger)^*$ and $(\eta_A)^\dagger = \epsilon_{A^*}$.

## Graphical notation

+--{: .query}
[[Aleks Kissinger]]: This should probably have its own page. "Graphical notation for monoidal categories"
=--

Morphisms in a monoidal category (and 2-categories in general) are inherently two dimensional, where $\circ$ is _vertical_ composition and $\otimes$ is _horizontal_ composition. These satisfy an interchange law:

\[ (f_1 \otimes f_2) \circ (g_1 \otimes g_2) = (f_1 \circ g1) \otimes (f_2 \circ g_2) \]

So, if w think of these four morphisms as occupying a spot in 2 dimensional space:

+--{: .query}
[[Aleks Kissinger]]: TODO: figure
=--

we realize that the bracketing from above is essentially meaningless syntax. This notion is the guiding concept for the graphical notation of monoidal categories, or string diagrams. In this notation, we represent objects $A,B$ as directed strings and arrows $f : A \rightarrow B$ as boxes.

<div style="text-align:center">
<svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 width="60px" height="109px" viewBox="-39 3 60 109" enable-background="new -39 3 60 109" xml:space="preserve">
<line fill="none" stroke="#000000" stroke-width="2" x1="-9.5" y1="12" x2="-9.5" y2="102"/>
<text transform="matrix(1 0 0 1 -0.5 30)" font-family="Helvetica" font-size="12">A</text>
<text transform="matrix(1 0 0 1 -0.5 93)" font-family="Helvetica" font-size="12">B</text>
<rect x="-27.5" y="39" fill="#CCCCEE" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-14,22.5 -9.5,27 -5,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-14,86 -9.5,90.5 -5,86 "/>
<text transform="matrix(1 0 0 1 -14.4805 66.0322)" font-family="Helvetica" font-style="italic" font-size="24">f</text>
</svg>
</div>

We represent the tensor product as juxtaposition.

<div style="text-align:center">
<svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 width="234px" height="108px" viewBox="-60 0 174 108" xml:space="preserve">
<line fill="none" stroke="#000000" stroke-width="2" x1="62.5" y1="12" x2="62.5" y2="102"/>
<text transform="matrix(1 0 0 1 71.5 30)" font-family="'Helvetica'" font-size="12">A</text>
<text transform="matrix(1 0 0 1 71.5 93)" font-family="'Helvetica'" font-size="12">B</text>
<rect x="44.5" y="39" fill="#CECBE6" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="58,22.5 62.5,27 67,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="58,86 62.5,90.5 67,86 "/>
<text transform="matrix(1 0 0 1 57.5195 66.0322)" font-family="Helvetica" font-style="italic" font-size="24">f</text>
<line fill="none" stroke="#000000" stroke-width="2" x1="116.5" y1="12" x2="116.5" y2="102"/>
<text transform="matrix(1 0 0 1 125.5 30)" font-family="'Helvetica'" font-size="12">C</text>
<text transform="matrix(1 0 0 1 125.5 93)" font-family="'Helvetica'" font-size="12">D</text>
<rect x="98.5" y="39" fill="#99CCCC" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="112,22.5 116.5,27 121,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="112,86 116.5,90.5 121,86 "/>
<text transform="matrix(1 0 0 1 108.5195 63.0322)" font-family="Helvetica" font-style="italic" font-size="24">g</text>
<line fill="none" stroke="#000000" stroke-width="2" x1="-63.5" y1="12" x2="-63.5" y2="102"/>
<text transform="matrix(1 0 0 1 -54.5 30)" font-family="'Helvetica'" font-size="12">A</text>
<text transform="matrix(1 0 0 1 -54.5 93)" font-family="'Helvetica'" font-size="12">B</text>
<rect x="-81.5" y="39" fill="#CECBE6" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-68,22.5 -63.5,27 -59,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-68,86 -63.5,90.5 -59,86 "/>
<text transform="matrix(1 0 0 1 -68.4805 66.0322)" font-family="Helvetica" font-style="italic" font-size="24">f</text>
<line fill="none" stroke="#000000" stroke-width="2" x1="-0.5" y1="12" x2="-0.5" y2="102"/>
<text transform="matrix(1 0 0 1 8.5 30)" font-family="'Helvetica'" font-size="12">C</text>
<text transform="matrix(1 0 0 1 8.5 93)" font-family="'Helvetica'" font-size="12">D</text>
<rect x="-18.5" y="39" fill="#99CCCC" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-5,22.5 -0.5,27 4,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-5,86 -0.5,90.5 4,86 "/>
<text transform="matrix(1 0 0 1 -8.4805 63.0322)" font-family="Helvetica" font-style="italic" font-size="24">g</text>
<text transform="matrix(1 0 0 1 25.1362 62.2832)" font-family="Helvetica" font-size="18">=</text>
<text transform="matrix(1 0 0 1 -39.5469 62.1729)" font-family="Helvetica" font-size="17.9327">&#8855;</text>
</svg>
</div>

## Extensions

CPM, classical structures, ...

[[!redirects quantum information theory]]
[[!redirects quantum computing]]
[[!redirects quantum computation]]