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
**(traditional anyon braiding)**
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
and their linear representations are the *[[braid representations]]*, exhibiting "[[braid group statistics]]" of the [[anyon|anyonic]] [[vortices]].

\begin{imagefromfile}
    "file_name": "BraidTransport.png",
    "width": 250,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

Incidentally, [[flat bundles]] of [[finite-dimensional Hilbert spaces]] over the parameter space \eqref{ConfigurationSpaceOfPoints} famously (but not exclusively) arise as [[Knizhnik-Zamolodchikov connections]] on spaces of [[conformal blocks]], the resulting [[braid representations]] are often known (somewhat undescriptively) as *monodromy representations*.
\end{example}

The phenomenology of the following example reproduces traditional lore about topological order often interpreted in terms of anyons, but it does not involve any anyon position parameters. We suggest that the way we obtain this now as another special case of Def. \ref{TopologicalOrder} speaks to the untility of this definition.



\begin{example}\label{TraditionalTopologicalOrderOverTorus}
**(traditional topological order over the torus)**

The phenomenology of the following example reproduces traditional lore about topological order often interpreted in terms of anyons --- but it does not involve any anyon position parameters. We suggest that the way we obtain this now as another special case of Def. \ref{ADefinition} speaks to the relevance of this definition.

Namely, it is commonly expected (cf. [Tong 2016](quantum+Hall+effect#Tong16) [(5.28)](https://ncatlab.org/nlab/files/Tong-QuantumHallEffect.pdf#page=168)) that the algebra of topological quantum observables of an FQH system on the plain torus, $\Sigma^2 \equiv T^2$, is generated by a [[pair]] of [[unitary operators]] $A$, $B$ subject to the [[commutator|commutation]] relation
\begin{equation}
  \label{TopologicalTorusObservables}
  A \, B
  =
  \zeta^2
  \,
  B A 
  \,,
\end{equation}
where $\zeta \in \mathbb{C}$ is a [[root of unity]] identified with the FQH anyon [braiding phase](quantum+Hall+effect#BraidingPhase).

This topological observable algebra (eq:TopologicalTorusObservables) is traditionally argued by appeal to an [[effective field theory|effective]] [[abelian Chern-Simons theory|abelian Chern-Simons field theory]] thought to describe the large-scale ("infrared") dynamics of the [[FQH system]]. (Experimental verification of this expectation has been out of reach: While it might barely be possible to constrain a 2D electron gas to a torus, it seems nigh impossible to then have it penetrated by an everywhere transverse magentic field. Which makes it all the more remarkable that, as we pass to FQAH systems, the torus topology becomes not only experimentally viable but the default --- now for a \emph{momentum space} torus.)

So we are to ask:

> *Does the relation (eq:TopologicalTorusObservables) represent the fundamental group of some parameter space $P$ associated with FQH systems?*

Remarkably --- the answer is, yes, of the parameter space of exotic topological magnetic flux quanta on the torus.

Namely, the parameter space of ordinary topological magnetic flux through a surface $\Sigma^2$, as predicted by the time-honored *[[Dirac charge quantization|Dirac flux quantization condition]]*, is the [[mapping space|space of maps]] to the [[classifying space]] 
\begin{equation}
  \label{MaxwellClassifyingSpace}
  \mathbb{C}P^\infty \simeq B \mathrm{U}(1)
\end{equation}
for $\mathrm{U}(1)$ [[Maxwell theory|Maxwell]] [[gauge fields]]:
\begin{equation}
  \label{ConfigurationsOfMaxwellFields}
  P
  \equiv
  \mathrm{Map}\big(
    \Sigma^2
    ,
    B \mathrm{U}(1)
  \big)
  \,.
\end{equation}
However, this has [[abelian group|abelian]] [[fundamental group]]
\begin{equation}
  \pi_1
  \,
    \mathrm{Map}\big(
    T^2
    ,
    B \mathrm{U}(1)
  \big)
  \simeq
  \mathbb{Z}^2
  \mathrlap{\,,}
\end{equation}
whose representations are given by the algebras of Maxwell Wilson loop observables $A,B$, satisfying
\begin{equation}
  A B 
  =
  B A
  \,.
\end{equation}
On the other hand, \eqref{ConfigurationsOfMaxwellFields} describes, of course,  the free magnetic field and ignores its interaction with a 2D electron gas that we are concerned with here. Instead, the surplus magnetic flux quanta on a backdrop of a fractional filling fraction making an FQH system are associated with vortices in a strongly-coupled electron system and as such of exotic nature. To reflect this in their configuration topology we may ask for a deformation of the classical classifying space \eqref{MaxwellClassifyingSpace}. Since $\mathbb{C}P^\infty \defneq \bigcup_{n \in \mathbb{N}} \mathbb{C}P^n$, a suggestive choice of deformation is the first stage in this sequence,
\begin{equation}
  \mathbb{C}P^1 \simeq S^2
  \,,
\end{equation}
leading to an exotic topological flux parameter space
\begin{equation}
  P
  \defneq
  \mathrm{Map}\big(
    \Sigma^2
    ,
    S^2
  \big)
  \,.
\end{equation}
Remarkably, the fundamental group of this space is the nonabelian *[[integer Heisenberg group]]* at level 2
\begin{equation}
  \pi_1
  \,
  \mathrm{Map}\big(
    \Sigma^2
    ,
    S^2
  \big)
  \simeq
  \widehat{\mathbb{Z}^2}
\end{equation}
whose representations are exactly of the form \eqref{TopologicalTorusObservables}, in that its [[group algebra]] is
\begin{equation}
  \mathbb{C}\Big[
  \pi_1
  \,
  \mathrm{Map}\big(
    \Sigma^2
    ,
    S^2
  \big)
  \Big]
  \simeq
  \mathbb{Z}\big[
    A, B , \underset{central}{\zeta}
  \big]\Big/
  \Big(
    A B = \zeta^2 B A 
  \Big)
  \mathrlap{\,.}
\end{equation}

\end{example}





