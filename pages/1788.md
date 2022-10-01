
## Quantum circuits via dependent linear tyoes

The following indicates how quantum protocols in [[quantum information theory]], hence  [[quantum circuits]] consisting of general [[quantum gates]] with classical control, including [[decoherence|de-coherent]] [[quantum measurement]]-gates, are naturally formulated in [[dependent linear type theory]], with classically controlled [[quantum states]] regarded as having dependent linear data types. The key observation is that:

1. The [[necessity]] [[modality]] $\box_C \coloneqq (p_C)^\ast (p_C)_\ast$ on [[linear types]] dependent on a given classical [[context]] $C$ (which includes classical control parameters as well as eventual [[quantum measurement]]-outcomes on the same footing) knows all about controlled [[quantum gates]]: namely these are identified with the [[morphisms]] in its [[co-Kleisli]]-category, with the $\box_C$-[[counit of a comonad]] reflecting the operation [[quantum measurement]] (and the [[comultiplication]] encoding the [[superposition]]-principle).

1. The [[external tensor product]] of dependent linear types gives the compilation of [[quantum gates]] into [[quantum circuits]], essentially as familiar from the quantum [[string diagram]]-calculus of [Abramsky & Coecke 2004](finite+quantum+mechanics+in+terms+of+dagger-compact+categories#AbramskyCoecke04) with respect to the plain [[tensor product]], but now taking into account all classical control and all potential measurement outcomes. 

In summary, the following shows that every dependent linearly-typed programming language as in 



