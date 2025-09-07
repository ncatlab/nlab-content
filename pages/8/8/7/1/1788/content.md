> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***


## Definition


A satisfactory definition of "topological order" is not readily manifest from existing literature. For example, the presence of "[[anyons]]" understood as [[solitons]] or [[defects]] (and that distinction itself is typically not properly made in the literature) localized in 2D space (as for [[fractional quantum Hall systems]]) should be an *example* of topological order, but the actual definition should not presuppose this specific incarnation of the general phenomenon. Instead, the [[quantum adiabatic theorem]], being the tacit general principle behind topological order, ought to explicitly appear in the definition.


\begin{definition}\label{ADefinition}
**(topological order)**

We shall say that a [[quantum system]] exhibits (*proper*) *topological order* if the following three conditions are satisfied:

**(1. -- holonomy)** The [[Hilbert spaces]] $\mathscr{H}_p$ of [[spectral gap|gapped]] [[quantum state|quantum]] [[ground states]] of the system *[[dependent linear type|depends]]* [[differentiable function|differentiably]] on [[classical physics|classical]] external parameters $p$ varying in some parameter [[space]] $P$.

By the [[quantum adiabatic theorem]], it follows thereby that adiabatic tuning (meaning: slow with respect to the [[quantum system]]'s relaxation time) of the parameters along [[continuous function|continuous]] [[paths]] $\gamma$ in $P$ induces (asymptotically) [[unitary transformations]] $U_\gamma$ of the quantum system:
 
\begin{imagefromfile}
    "file_name": "QuantumAdiabaticTransport.png",
    "width": 180,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

**(2. -- homotopy)** This dependency on parameter paths is "[[topological physics -- contents|topological]]" (which is [[physics]] jargon for what in [[mathematics]] really is: *[[homotopy theory|homotopica]]*) in that continuous deformations $\sigma \colon \gamma \Rightarrow \gamma'$ of parameter paths (*[[homotopies]]*, keeping their endpoints fixed) does not affect the induced [[unitary transformations]]:

\begin{imagefromfile}
    "file_name": "QuantumHomotopyInvariance-250907.png",
    "width": 190,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}


**(3. -- monodromy)** The [[fundamental group]] $\pi_1$ (of any [[connected component]]) of $P$ is non-[[trivial group|trivial]] (properly: [[non-abelian group|non-abelian]]), in that some such [[pairs]] of parameter paths with the same endpoints do *not admit* (\#) continuous deformations into each other:

\begin{imagefromfile}
    "file_name": "NondegenerateQuantumHolonomy.png",
    "width": 190,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

and the induced unitary representation of the [[fundamental group]]  

\begin{imagefromfile}
    "file_name": "QuantumMonodromy-250907.png",
    "width": 210,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

is non-[[trivial representation|trivial]] (properly: [[direct sum|contains]] [[irreps]] of [[dimension of a vector space|dimension]] $\gt 1$).

\end{definition}

\begin{remark}
**(interpretation)**

Physically, the 1st condition in Def. \ref{ADefinition} says that tuning of parameters induces transformations on gapped quantum ground states like *[holomonic quantum gates](adiabatic+quantum+computation#ReferencesGeometricPhaseGates)*, the 2nd condition says that this operation is "topological" (really: *homotopical*) in that it is insensitive to local deformation (noise!) in the parameter paths, and the 3rd condition ensures that there are non-trivial such topological processes inducing non-trivial transformations on the quantum system. Beware that no experimentalist needs to actually execute such topological processes in order for the system's ground states to represent them, but that actually executing them amounts to operating *[[topological quantum computing|topological quantum gates]]* on the system.

In mathematical jargon, the 1st condition makes the Hilbert spaces form a *[[vector bundle|bundle]] [[connection on a bundle|with connection]]* over $P$ whose *[[parallel transport]]* are the unitaries $\gamma \mapsto U_\gamma$, the 2nd condition says that this connection is *[[flat connection|flat]]*, making the bundle of Hilbert spaces a *[[local system]]*, and the 3rd condition says that this local system is non-trivial (properly: non-abelian).

\end{remark}

Now first to see how this general definition reduces to the traditional case:

\begin{example}\label{TraditionalAnyonicTopologicalOrder}
**(traditional anyonic topological order)**
For cases like plain [[FQH systems]] on a surface $\Sigma^2$, the parameter space is that of configurations of (quasi-hole/vortex) positions, known as the surface's *[[configuration space of points]]*:
\[
  \label{ConfigurationSpaceOfPoints}
  P_{{}_{\mathrm{FQH}}}
  \,\equiv\,
  \mathrm{Conf}\big(\Sigma^2\big)
  \,\coloneqq\,
  \Big\{
    S \subset \Sigma^2
    \,\big\vert\,
    S \in FinSet
  \Big\}
  \mathrlap{\,.}
\]

The theoretical identification of [FQH anyons](quantum+Hall+effect#BraidingPhase) via the [[quantum adiabatic theorem]] applied to this situation goes back to [Arovas, Schrieffer & Wilczek 1984](quantum+Hall+effect#ArovasSchriefferWilczek84), [Su 1986](quantum+Hall+effect#Su86). 

The fundamental groups of the configuration space (eq:ConfigurationSpaceOfPoints), in the connected component of $n$ vortices, are the *[[surface braid groups]]*
\[
  \mathrm{Br}_n(\Sigma^2)
  \,\equiv\,
  \pi_1\big(
    \mathrm{Conf}(\Sigma^2)
    ,
    n
  \big)
  \mathrlap{\,,}
\end{equation}
and their linear representations are the *[[braid representations]]*, exhibiting "[[braid group statistics]]" of the anyonic vortices.

Incidentally, flat bundles of Hilbert spaces over the parameter space \eqref{ConfigurationSpaceOfPoints} famously (but not exclusively) arise as [[Knizhnik-Zamolodchikov connections]] on spaces of [[conformal blocks]], the resulting braid representations are often known (somewhat undescriptively) as *monodromy representations*.
\end{example}

But the external parameter space $P$ of a topological quantum could be very different from the traditional situation in Ex. \ref{TraditionalAnyonicTopologicalOrder} and *yet* the system may exhibit topological order.




