There is much code after this line in the [source](https://ncatlab.org/nlab/source/Sandbox), but it is not displaying.

+-- {: .num_example }
###### Example

The problem is caused by the character immediately after the following closing tag:

=--

Test



In [[mathematics]], a *[[topos]]* is, from one perspective, a context in which the core machinery of mathematics can *take place* (whence the name: *τόπος*, ancient Greek for "place"). For instance, the familiar category of sets (with plain maps between them) is a topos, and most of the rigorous mathematics of the 20th century (tacitly) takes place in this default topos of sets. 

But there are other toposes. For example, there is a topos of *[[smooth sets]]* with *[[smooth maps]]* between them, where [[smooth manifolds]] are [[objects]] at the same ontological level as discrete sets! Given the fundamental role that smooth manifolds and smooth maps between them play in modern physics, this is a first hint that topos theory can inform mathematical physics.

The remarkable insight of ("[[elementary topos|elementary]]") topos theory is that mathematical definitions and theorems may be transported from plain sets to such smooth sets -- or to any other topos -- if only they are *[[constructive mathematics|constructive]]*, meaning essentially that they do not invoke the usual "[[axiom of choice]]".

This is not mysterious but already the first example of physical intuition aligning with topos theory: Notice that in the topos of sets, the axiom of choice says equivalently that every [[surjective map]] $E \twoheadrightarrow B$ ("[[epimorphism]]") admits a *[[section]]*, namely a *choice* $\sigma(b) \,\in\, E_b$ of elements in the [[fiber]] $E_b$ over each point $b \in B$ in the base:

\begin{tikzcd}[sep=15pt]
  && E
     \ar[
       dd, ->>
     ]
  \\
  \\
  B 
    \ar[rr, equals] 
    \ar[
      uurr, 
      dashed, 
      "{ \exists\,  ? \, \sigma }"
   ]
  && 
  B
\end{tikzcd}

Whatever one may think of this axiom in the case of plain sets, it is clearly *un*justified for *smooth sets*, where a surjection as above is a *smooth bundle*, such as a [[fiber bundle]] or a [[principal bundle]]. Even if we assume (as one usually does) that we can choose elements $\sigma(b)$ in each fiber of the bundle separately, for a non-trivial principal bundle there is no way to make theses choices *smoothly* to arrange into a smooth map $\sigma \,\colon\, B \to E$ as above. The failure of the axiom of choice in smooth sets is the reason why in physics one sees crucial phenomena like flux quantization, soliton/instanton sectors or fermionic anomalies!

This may suggest that reasoning in mathematical physics is naturally reflected in constructive mathematics. 
Here it is fundamentally not a coincidence that the main application of constructive mathematics has been to computer science, where one cares not about hypothetical existence, say of choices as above, but about algorithmic construction by computation, ultimately by physical processes executed by a physical computing machine. 

Toposes are essentially the possible *models* of such constructive ("physical") reasoning.
There are many topos models relevant for the discussion of physics. 

For example, there is a topos of [[super smooth sets]] which includes also [[super-manifolds]] on the same ontological level as smooth manifolds (and plain sets). One can argue that it is (only) in a topos like this that much of the discussion of "super-fields" in the physics literature really finds its precise home.

Despite traditional "super"-terminology, the [[super-geometry]] embodied by the topos of [[super smooth sets]] is not exclusive to discussion of *[[supersymmetry]]* (though this is captured, too, if one cares) but is much more fundamentally concerned with fermionic geometry: The fact that fermion fields appear as *anti*-commuting variables in the Dirac Lagrangian (such as the leptons and quarks in the standard model of particle physics)






