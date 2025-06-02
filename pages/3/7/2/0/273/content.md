
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

The notion of [[cohomology]] finds its natural general formulation in terms of [[hom-spaces]] in an [[(∞,1)-topos]], as described at *[[cohomology]]*. Many of the cohomologies which have been traditionally considered, such as [[abelian sheaf cohomology|sheaf cohomology]], turn out to be just a special case of the general situation, for objects which are sufficiently abelian in the sense of [[stable (infinity,1)-category|stable (∞,1)-categories]].

Therefore to amplify that one is looking at general [[cohomology]] without restricting to [[abelian sheaf cohomology|abelian cohomology]] one speaks of  **nonabelian cohomology**. 

\linebreak

To say this in a bit more detail (following [[schreiber:The Character Map in Equivariant Twistorial Cohomotopy|SS24]]):


### Cohomology via classifying spaces

It is a classical and yet possibly undervalued fact that *reasonable [[cohomology]] theories have [[classifying spaces]]* (and more generally *[[moduli stacks|classifying stacks]]*). To quickly recall (more details and pointers in [FSS23, §2](#FSS23)):

**Ordinary cohomology.**
This begins with the observation that ([[reduced cohomology|reduced]]) [[ordinary cohomology|ordinary]] [[singular cohomology]], with [[coefficients]] in a [[discrete group|discrete]] [[abelian group]] $A$, is classified in degree $n$ by [[Eilenberg-MacLane spaces]] $K(A,n)$ -- in that on well-behaved topological spaces $X$, notably on [[smooth manifolds]], there are [[natural isomorphisms]] between the ordinary [[cohomology groups]] and the [[connected components]] of the respective ([[pointed topological space|pointed]]) [[mapping spaces]]:
\[
  \label{OrdinaryCohomologyRepresented}
  H^n(X;\, A)
  \;\simeq\;
  \pi_0
  \,
  \mathrm{Maps}
  \big(
    X,\,
    K(A,n)
  \big)
  \,,
  \;\;\;\;\;\;\;\;\;\;\;
  \widetilde H^n(X;\, A)
  \;\simeq\;
  \pi_0
  \,
  \mathrm{Maps}^{\ast/\!}
  \big(
    X,\,
    K(A,n)
  \big)
  \,.
\]
This equivalence makes manifest the [characteristic properties](Whiethead-generalized+cohomology#AxiomsReduced) of cohomology: homotopy invariance, exactness and wedge property, since these are now immediately implied by general abstract properties of mapping spaces.

Moreover, these EM-spaces are in fact [[loop spaces]] of each other, via [[weak homotopy equivalences]]
\[
  \label{LoopingEquivOnEmSpaces}
  \sigma_n
  \;\colon\;
    K(A,n)
    \xrightarrow{\;\sim\;}
    \Omega K(A,n+1)
\]
that thereby represent the *[[suspension isomorphisms]]* between ordinary cohomology groups, as follows: 

$$
  \widetilde H^{n}(X;A)
    \;\simeq\;
  \mathrm{Maps}^{\ast/\!}\big(
    X
    ,\,
    K(A,n)
  \big)
  \xrightarrow{
    (\sigma_n)_\ast
  }
  \mathrm{Maps}^{\ast/\!}\big(
      X
      ,\,
      \Omega
      K(A,n+1)
  \big)
  \;\simeq\;
  \mathrm{Maps}^{\ast/\!}\big(
      \Sigma
      X
      ,\,
      K(A,n+1)
    \big)
    \;\simeq\;
    \widetilde H^{n+1}\big(
      \Sigma X
      ;\,
      A
    \big)
    \,.
$$


\linebreak

**Ordinary non-abelian cohomology.**
Note here that it is the loop space property \eqref{LoopingEquivOnEmSpaces}, and hence the corresponding [[suspension isomorphism]], which reflect the fact that the coefficient $A$ has been assumed to be an *abelian* group:
For a non-abelian group $G$, an Eilenberg-MacLane space $K(G, 1) \,\simeq\, B G$ still exists (cf. *[[classifying space]]*), but is *not a loop space*.

While the suspension isomorphism is thus lost for non-abelian coefficients, the assignment
\[
  \label{OrdinaryNonAbelianCohomology}
  X
  \;\;
   \mapsto
  \;\;
  H^1\big(
    X
    ;\, 
    G
  \big)
  \;\;
  \coloneqq
  \;\;
  \pi_0
  \,
  \mathrm{Maps}\big(
    X
    ,\,
    B G
  \big)
  \;\;\;
  \in\;
  \mathrm{Set}^{\ast/}
\]
still satisfies homotopy invariance, exactness and wedge property, just as before by the general properties of mapping spaces, and hence has all the characteristic properties of ordinary cohomology -- except for its abelian-ness.
Accordingly, (eq:OrdinaryNonAbelianCohomology) is known as *non-abelian cohomology*, famous from early applications in [[Chern-Weil theory]].

\linebreak

**Whitehead-generalized cohomology.** If or as long as we do insist on abelian cohomology groups related by suspension isomorphisms, we may still immediately generalize ordinary cohomology in the form (eq:OrdinaryCohomologyRepresented), simply by using any other sequence of classifying spaces $(E_n)_{n=0}^\infty$, being successive loop spaces of each other as in (eq:LoopingEquivOnEmSpaces),
$$
  \sigma_n \,:\,
    E_n
    \xrightarrow{\; \sim \;}
    \Omega
    E_{n+1}
    \,,
$$
as such called a *[[sequential spectrum|sequential]] [[Omega-spectrum|$\Omega$-spectrum]] of spaces*, or just a *[[spectrum]]*, for short. The [[Brown representability theorem]] says that the resulting assignments
$$
  X
  \;\;
  \mapsto
  \;\;
  E^n(X)
  \,\coloneqq\,
  \pi_0
  \,
  \mathrm{Maps}\big(
    X
    ,\,
    E_n
  \big)
$$
are equivalently the "[[Whitehead-generalized cohomology|generalized cohomology theories]]" as introduced by Whitehead, including examples such as [[K-theory]], [[elliptic cohomology]] and [[cobordism cohomology]].

\linebreak

**Non-abelian generalized cohomology.** But as we just saw, suspension isomorphisms are to be regarded as *[[extra structure|extra]]* [[structure]] on cohomology. Not necessarily requiring them leads to consider *any pointed space* $\mathscr{A}$ (which we may as well assume to be [[connected topological space|connected]]) as the classifying space of a *non-abelian generalized cohomology* theory, defined in evident generalization of (eq:OrdinaryNonAbelianCohomology) simply by
\[
  \label{NonabelianCohomology}
  H^1\big(
    X
    ;\,
    \Omega\mathscr{A}
  \big)
  \;\;
  \coloneqq
  \;\;
  \pi_0
  \,
  \mathrm{Maps}\big(
    X
    ,\,
    \mathscr{A}
  \big)
  \,.
\]
Here the notation on the left is suggestive of the fact that any loop space $\Omega \mathscr{A}$ canonically carries the structure of a higher homotopy-coherent group -- a groupal $A_\infty$-space or [[infinity-group|$\infty$-group]], for short --  whose de-looping [is equivalent](May+recognition+theorem#statement) to the connected component of the original space:
\[
  \label{DeloopingEquivalence}
  \mathscr{A}
  \;\;
  \simeq
  \;\;
  B \, \Omega \mathscr{A}
  \,.
\]

For example, in the archetypical case where
$\mathscr{A} \,\equiv\, S^n$ is the [[n-sphere|$n$-sphere]], then the non-abelian generalized cohomology theory that it classifies is known as (unstable) [[Cohomotopy]] $\pi^n$
\[
  \label{Cohomotopy}
  \widetilde H^1\big(
    X
    ;\, 
    \Omega S^n
  \big)
  \;\;
  \equiv
  \;\;
  \pi_0
  \,
  \mathrm{Maps}^{\ast/\!}\big(
    X
    ,\,
    S^n
  \big)
  \;\;
  \equiv
  \;\;
  \pi^n(X)
  \,,
\]
in dual reference to the familar *[[homotopy groups|homotopy]]* groups
$$
  \pi_n(X)
  \;\;
  \simeq
  \;\;
  \pi_0
  \,
  \mathrm{Maps}^{\ast/\!}\big(
    S^n
    ,\,
    X
  \big)
  \,.
$$

Another example of non-abelian generalized cohomology is [[unstable topological K-theory]], whose classifying spaces are taken to be finite stages $\mathrm{U}(n)$ of the sequential colimits which construct the classifying spaces of [[topological K-theory]].

### Developing non-abelian cohomology

Fundamental, elementary and compelling as the notion of non-abelian generalized cohomology in (eq:NonabelianCohomology) is, it has long remained underappreciated. For example, none of the original authors on [[Cohomotopy]] (eq:Cohomotopy) address their subject as a cohomology theory, instead the early development revolves around partial fixes for the perceived defect of co-homotopy sets to not in general carry group structure.
The situation does not improve with the early development of "[[non-abelian gerbes]]", whose original description appears unwieldy. 

Explicit acknowledgement of (stacky) non-abelian generalized cohomology  in the transparent guise (eq:NonabelianCohomology)
appears only in a lecture of [Toën 2002](#Toen02), (possibly following [Simpson 2002](#Simpson02) where non-abelian generalization of [[de Rham cohomology]] is considered). 

Two independent developments around 2009 put non-abelian generalized cohomology into practical context: 

* The discovery of [[nonabelian Poincaré duality]] ([Lurie 2009 §3.8](nonabelian+Poincaré+duality#Lurie09)), relating non-abelian cohomology (as later made explicit in [Lurie 2014 Def. 6](#Lurie14)) of manifolds  to "non-abelian *homology*" in the guise of "[[topological chiral homology]]" (which, in contrast to non-abelian cohomology, takes work to define); 

* The observation in theoretical physics ([SS 2008](#SS08), [Sc 2009](#Schreiber09)) that [[geometry of physics -- flux quantization|charge/flux-quantization laws]] for [[higher gauge fields]] are generally in non-abelian cohomology.

\linebreak

With non-abelian generalized cohomology thus recognized as a worthwhile subject, one is led to generalize familiar constructions in abelian cohomology, as far as possible, and to explore the consequences.

First, one may straightforwardly equip non-abelian cohomology with further attributes: Considering the right hand side of (eq:NonabelianCohomology) not just for plain spaces but for sheaves of spaces ([[infinity-stack|higher stacks]]) leads to non-abelian generalized sheaf cohomology, including, in particular, non-abelian generalized versions of [[twisted cohomology]], of [[equivariant cohomology]] and [[nonabelian differential cohomology]].

\linebreak

**Equivariant non-abelian cohomology.** Via the above identification of cohomology sets with homotopy-classes of maps to a classifying space, every flavor of [[homotopy theory]] comes with its corresponding flavor of cohomology theories. 

In *[[equivariant homotopy theory]]* one considers topological spaces $\mathscr{A}$ equipped with the [[group action|action]] $G \curvearrowright \mathscr{A}$ of a (finite, for our purposes) group $G$ and with $G$-equivariant maps between them -- and the corresponding flavor of cohomology is *equivariant cohomology*:
\[
  \label{EquivariantCohomology}
  H^1_G\big(
    X;\,
    \Omega\mathscr{A}
  \big)
  \;\;
  =
  \;\;
  \pi_0
  \, 
  \mathrm{Maps}\big(
    G \curvearrowright X
    ,\,
    G \curvearrowright \mathscr{A}
  \big)^G
  \,.
\]

Here the notion of $G$-homotopy equivalence of maps is straightforward but, at face value, technically cumbersome to reason about. However, [[Elmendorf's theorem]] reveals that $G$-homotopy equivalences (between $G$-cell complexes) are nothing but systems of ordinary weak homotopy equivalences between the $H$-fixed spaces $\mathscr{A}^H$ for all subgroups $H \subset G$. These systems of fixed spaces are conveniently re-packaged as presheaves on a small category called the *[[orbit category]]* $\mathrm{Orb}(G)$ of $G$, whence $G$-equivariant homotopy theory is equivalently the homotopy theory of [[(infinity,1)-presheaf|presheaves of spaces]] on $\mathrm{Orb}(G)$.

\linebreak

**Twisted non-abelian cohomology.** 
Somewhat similarly, given any space $\mathscr{B}$ in any homotopy theory, the *[[slice (infinity,1)-category|$\mathscr{B}$-slice]]* is the [[homotopy theory]] whose objects are spaces fibered over $\mathscr{B}$ with maps between them respecting the fibration up to specified homotopy. If we assume, without essential restriction, that the base space is connected, then we may identify it as $\mathscr{B} \,\simeq\, B \mathscr{G}$, as in (eq:DeloopingEquivalence), which exhibits any fibration over it as the [[Borel construction]] $\mathscr{A} \sslash \mathscr{G}$ of the homotopy-quotient of a homotopy-coherent action $\mathscr{G} \acts \mathscr{A}$.

If we now think of a domain object $X \xrightarrow{\tau} B\mathscr{G}$ in this $B \mathscr{G}$-slice as a *twist* and of a codomain object $\mathscr{A} \sslash \mathscr{G} \xrightarrow{p}  B \mathscr{G}$ as a *[[local coefficient bundle]]*, then the corresponding non-abelian cohomology is just the homotopy classes of sections of the $\tau$-associated $\mathscr{A}$-fiber bundle, and as such is $\tau$-twisted $\mathscr{A}$-cohomology:

\begin{imagefromfile}
    "file_name": "TwistedNonalianCohomologyB.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This works generally: If all spaces here are *in addition* equipped with $G$-actions as in (eq:EquivariantCohomology), hence if we are looking at a slice of equivariant homotopy, then the above is automatically *twisted equivariant* non-abelian cohomology.


\linebreak


**The non-abelian character.**
One famous construction on abelian cohomology is the *[[Chern-Dold character map]]* to [[de Rham cohomology]], which in the case of [[topological K-theory|K-cohomology]] becomes the familar [[Chern character]] (and which on ordinary cohomology is essentially just the [[de Rham theorem]]). 
One may think of the Chern-Dold character as universally extracting the [[torsion subgroup|non-torsion]] data of cohomology. 
Its generalization to non-abelian cohomology was developed in [FSS23](#FSS23): 

Observing that the Chern-Dold character is essentially just the [[cohomology operation]] induced by  *[[rationalization]]* of the [[classifying space]], 
$$
  \mathscr{A}
  \xrightarrow{
    \phantom{--}
    \eta^{\mathbb{Q}}
    \phantom{--}
  }    
  L^{\!\mathbb{Q}}\mathscr{A}
$$
as such it makes sense in the generality of non-abelian classifying spaces (immediately so under mild technical assumptions, such as [[nilpotent topological space|nilpotency]], but with more work also more generally). In view of this, the [[fundamental theorem of dg-algebraic rational homotopy theory]] may be re-cast as a *[[non-abelian de Rham theorem]]* which identifies, over smooth manifolds $X$, the resulting non-abelian rational cohomology with the [[concordance classes]] of [[flat L-infinity algebra valued differential form|flat differential forms having coefficients]] in the real [[Whitehead algebra|Whitehead-bracket $L_\infty$-algebra]] $\mathfrak{l}\mathscr{A}$ of the classifying space:

\begin{imagefromfile}
    "file_name": "NonabelianCharacterMap.jpg",
    "width": 670,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Since generalized cohomology theories are typically hard to analyze, in particular non-abelian ones, this character map may be regarded as extracting the first non-trivial stage of more tractable invariants. For instance, the character of a non-abelian class is the first [[obstruction]] to the trivialization of that class.

\linebreak

{#NACGauge} **Nonabelian cohomology and gauge fields.**
In the mentioned application to physics, the [[flux densities]] of a [[higher gauge field]] are sourced by charges which appear as classes in [[non-abelian de Rham cohomology]] on the right, and the completion of the higher gauge theory by a [[geometry of physics -- flux quantization|flux-quantization law]] means to lift these charges through the character map to classes in a chosen non-abelian cohomology theory on the left.

[[!include cohomology and gauge fields -- table]]

\linebreak


## More details
 {#MoreDetails}

\linebreak

### Ordinary Principal Bundles

For $G$ a [[Hausdorff space|Hausdorff]]-[[topological group]], a *[[principal bundle|principal $G$-bundle]]* $P$ over a base space $X$ is a [[map]] $P \xrightarrow{\;} X$ such that there exists an [[open cover]] $C \coloneqq \coprod_i U_i \overset{\iota}{\twoheadrightarrow} X$ over which $P$ is identified with the trivial fibration $C \!\times\! G$ in a way that the [[fibers]] are identified by $G$-valued [[transition functions]] $g \,:\, C \!\times_X\! C \xrightarrow{\;} G$ on double overlaps of charts, $C \times_X C \,=\, \underset{i,j}{\coprod} \, U_i \cap U_j$:

\begin{imagefromfile}
    "file_name": "PrncBundlLocTriv-Schematics.jpg",
    "width": 860,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

These [[transition functions]] clearly satisfy on triple overlaps $C \times_X C \times_X C$ the *Čech cocycle* condition

\begin{imagefromfile}
    "file_name": "CechCocycle-Schematics.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


and transform under a principal bundle [[isomorphism]] $P \xrightarrow{ \phi } P'$ by the *Čech coboundary* relation

\begin{imagefromfile}
    "file_name": "CechCoboundary-Schematics.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


whence the [[isomorphism classes]] of principal bundles map to the *[[Čech cohomology]]* of the base space:

$$
  \mathrm{Prncpl}G\mathrm{Bndl}(X)_{\!\big/\sim}
  \xrightarrow{\phanrtom{--} \sim \phantom{--}}
  H^1\big(X;\, G\big)
  \,.
$$

As indicated, this map is in fact a [[bijection]] (for well-behaved $X$, such as [[smooth manifolds]]), as one finds effectively by reading the above construction in reverse.

The outer parts of these diagrams then also show that if we write 

* [[delooping groupoid|$\mathbf{B}G$]] for the [[topological groupoid]] with a single object and $G$ worth of morphisms, 

* [[Cech groupoid|$\widehat X$]] for the [[topological groupoid]] with $C$ as its manifold of objects and $C \!\times_X\! C$ as its manifold of morphisms, 

  for $C \xrightarrow{\iota} X$ a [[good open cover|*good* open cover]] (over which every $G$-bundle trivializes),

then the groupoid of principal $G$-bundles is identified with the groupoid of [[Top|continuous]] [[internal functor|functors]] $g \,\colon\, \widehat{X} \xrightarrow{\;} \mathbf{B}G$ with [[Top|continuous]] [[internal natural transformation|natural transformations]] between these:

\begin{imagefromfile}
    "file_name": "CechCohomology-Schematics.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


\linebreak

### Ordinary Nonabelian Cohomology
 {#OrdinaryNonabelianCohomology}

A deeper but classical theorem says (cf. [[schreiber:Equivariant principal infinity-bundles|SS25]] [Thm. 4.1.3](https://arxiv.org/pdf/2112.13654#page=171))  that this situation is preserved by the  "[[topological realization]]" of [[topological groupoids]] to [[topological spaces]]
$$
  \left\vert-\right\vert 
    \,\colon\,
  SmthGrpd
  \longrightarrow
  TopSpc
$$
under which a continuous functor $g \,\colon\, \widehat X \xrightarrow{\;} \mathbf{B}G$ becomes a [[continuous map]] $\left\vert g\right\vert \;\colon\; \vert\widehat{X}\vert \xrightarrow{\;}  \vert\mathbf{B}G\vert$ from $\vert\widehat{X}\vert \simeq X$ to the *[[classifying space]]* $B G \,\coloneqq\, \left\vert\mathbf{B}G\right\vert$ -- which still represents isomorphism classes of principal $G$-bundles:

\begin{imagefromfile}
    "file_name": "PrncBndlToNonabCohomology.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


This is the **[[ordinary nonabelian cohomology]]** of $X$.

\linebreak

### Ordinary Abelian Cohomology
 {#OrdinaryAbelianCohomology}

In the special case that $G \,\equiv\, A$ an *[[abelian group|abelian]] [[topological group|group]]*, one readily sees that there is a [[fiber]]-wise $A$-[[tensor product]] of principal $A$-bundles

\begin{tikzcd}[sep=0pt]
    \mathrm{Prnc}A\mathrm{Bndl}(X)_{/\sim}
    \,\times\,
    \mathrm{Prnc}A\mathrm{Bndl}(X)_{/\sim}
    \ar[
      rr
    ]
    &&
    \mathrm{Prnc}A\mathrm{Bndl}(X)_{/\sim}    
    \\
    \big(
      \,
      [P],
      \,
      [P']
      \,
    \big)
    &\longmapsto&
    \big[
      P \times_A P'
    \big]
\end{tikzcd}

given by
$$
  (P \times_A P')_x
  \;\coloneqq\;
  \Big\{
    (p, p')
    \,\in \,
    P_x \times P'{}_{\!\!\!x}
  \Big\}\Big/\Big(
    (a \cdot p,\, p')
    \sim
    (p,\, a^{-1} \cdot p')
  \Big)
  \,,
$$
which makes the isomorphism classes naturally form an abelian group. 

> (NB: As a tensor product of fibrations this exists also for non-abelian $G$, but the commutativity of $A$ is needed for its principality, namely for the resulting transition functions to again by given by group multiplication.)


Under the classification of principal $A$-bundles by $A$-cohomology, this means that
the classifying space $B A$ (may be chosen such that it) carries topological group structure itself!, so that the construction iterates:

$$
  A \;\in\; 
  \mathrm{AbGrp}(\mathrm{TopSpc})
  \;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;
  \left\{
  \begin{array}{l}
  B^2 A
  \;\coloneqq\;
  B(B A)
  \\
  B^3 A
  \;\coloneqq\;
  B\big(B(B A)\big)
  \\
  \;\;\;\vdots
  \\
  B^{1+n} \;\coloneqq\; B\big(B^n A\big)
  \mathrlap{\,.}
  \end{array}
  \right.
$$

For a *[[discrete group|discrete]]* abelian group $A$ (such as [[integers|$A = \mathbb{Z}$]]) these higher-order classifying spaces are also denoted "$K(A,n)$" and called "[[Eilenberg-MacLane spaces]]":

$$
  A \,\in\,
  \mathrm{AbGrp}(\mathrm{Set})
  \;\;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;\;
  K(A,n)
  \;\;
  \coloneqq
  \;\;
  B^n A
  \,.
$$

But this means that for abelian group coefficients $A$ there is *higher-degree $A$-cohomology* appearing as a special case of non-abelian cohomology, as follows:

$$
  H^{1+n}\big(
    X
    ;\,
    A
  \big)
  \;\;
  \coloneqq
  \;\;
  H^1\big(
    X
    ;\,
    B^nA
  \big)
  \;\;
  \coloneqq
  \;\;
  \pi_0
  \, \mathrm{Maps}\big(
    X
    ,\,
    B^{1+n} A
  \big)
  \,.
$$

Of course, when $A$ is discrete then there is also *[[Čech cohomology]]* and *[[singular cohomology]]* with coefficients in $A$. A classical theorem says that (on our smooth manifold domain $X$) all these notions of [[ordinary cohomology]] agree, hence that

$$
   Ordinary \; A\text{-}cohomology \; has \; classifying \; spaces \; B^n A \,=\, K(A,n).
$$

\linebreak

### Ordinary Characteristic Classes
  {#OrdinaryCharacteristicClasses}

Thereby we obtain an immediate means to *approximate non-abelian cohomology by abelian cohomology*: Every map of classifying spaces $c \colon B G \xrightarrow{\phantom{--}} B^n A$, hence every *[[universal characteristic class]]*
$$
  [c]
  \;\in\;
  H^n\big(
    B G
    ;\,
    A
  \big)
  \,,
$$
induces a *[[cohomology operation]]* from non-abelian to abelian cohomology, simply by [[composition]] of classifying maps:

\begin{imagefromfile}
    "file_name": "CharacteristicClassSchematics.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


For example, the [[frame bundle]] $\mathrm{Fr}_X$ of a [[Riemannian manifold]] $X$ is an [[orthogonal group|$O(d)$]]-[[principal bundle]], whose [[classifying space]] carries universal [[Pontrjagin classes]] $p_n \,\in\, H^{4n}\big(B \mathrm{O}(d);\, \mathbb{Z}\big)$, which evaluate to the Pontrjagin classes of $X$:
$$
  p_n[X]
  \;\coloneqq\;
  p_n[T X]
  \;\coloneqq\;
  p_n[\mathrm{Fr}_X]
  \;\coloneqq\;
  \big[
    X
    \xrightarrow{
      \vdash \mathrm{Fr}_X
    }
    B\mathrm{O}(d)
    \xrightarrow{p_n}
    B^{4n}\mathbb{Z}
  \big]
  \;\;
  \in
  \;\;
  H^{4n}(X; \,\mathbb{Z})
  \,.
$$

We see again that:
$$
  \begin{array}{c}
  In \; terms \; of \; classifying \; spaces,
  \\
  cohomology \; and \; characteristic \; classes
  \\
  become \; conceptually \; very \; transparent.
  \end{array}
$$

\linebreak

### Ordinary Character Map
 {#OrdinaryCharacterMap}

One more notion of cohomology available on [[smooth manifolds]] $X$ is *[[de Rham cohomology]]* $H^{n}_{\mathrm{dR}}(X)$, which we may understand -- non-traditionally but equivalently [FSS23 Prop. 6.4](#FSS23) -- as equivalence classes of closed differential forms modulo *[[concordance]]* of [[closed differential form|closed forms]]:
$$
  H^n_{\mathrm{dR}}(X)
  \;\;
  =
  \;\;
  \Omega^n_{\mathrm{dR}}(X)_{\mathrm{clsd}}
  \big/
  \Big(
    \omega^{(0)} 
      \,\sim\,
    \omega^{(1)}
    \;\;\;
    \mbox{iff}
    \;\;
    \exists
    \;
    {
      \widehat{\omega}
      \,\in\,
      \Omega^n_{\mathrm{dR}}(
        [0,1]
          \times 
        X 
      )_{\mathrm{clsd}}
    }
    \;
    \mbox{s.t.}
    \;\,
    \widehat{\omega}_{\vert_0}
    =
    \omega^{(0)}
    ,\;
    \widehat{\omega}_{\vert_1}
    =
    \omega^{(1)}
  \Big)
  \,.
$$
By the [[de Rham isomorphism]], this, too, coincides with a special case of our general notion of cohomology, namely with abelian cohomology for coefficients the real numbers $\mathbb{R}$ (regarded as a [[discrete group|discrete]] topological group). 

Combined with the cohomology operation induced by [[extension of scalars]] $\mathbb{Z} \hookrightarrow \mathbb{R}$, hence by the induced $B^n \mathbb{Z} \xrightarrow{\;} B^n \mathbb{R}$, this gives a map from [[integral cohomology|integral]] to [[de Rham cohomology]], which we may call the *ordinary character map*

\begin{imagefromfile}
    "file_name": "OrdinaryCharacterMap.jpg",
    "width": 520,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Beware that this character map is not in general [[injective function|injective]], in fact it forgets exactly the *[[torsion subgroups]]* of the [[integral cohomology]] group.
Nevertheless --- or rather: therefore! --- the ordinary character map provides the *first approximation* to integral cohomology, which is generally more readily computed than the full integral cohomology.

In consequence, when applied to integral characteristic classes then the ordinary character gives a useful first approximation to ordinary non-abelian cohomology. Specifically for [[unitary group|unitary]] principal bundles we obtain a sequence of *Chern-de Rham classes*:

\begin{imagefromfile}
    "file_name": "ChernDeRhamClasses.jpg",
    "width": 750,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


But since de Rham cohomology is a local differential-geometric notion, the question arises: 

$$
\begin{array}{c}
Is \; it \; possible \; to \; construct \; the \; Chern\text{-}de \; Rham \; classes
\\
directly \; by \; differential \; geometry \; on \; principal \; bundles
\\
without \; going \; through \; these \; topological constructions?
\end{array}
$$

[[principal connection|Connections]] are the answer to this question.

\linebreak


### Ordinary Connections
 {#OrdinaryConnections}

For $G$ a [[Lie group]] and $\mathfrak{g}$ its [[Lie algebra]], we denote the  ([[presheaf|functor assigning]]) flat [[Lie algebra valued differential forms|$\mathfrak{g}$-valued differential forms]] by
$$
  \Omega^1_{\mathrm{dR}}\big(
    -
    ;\,
    \mathfrak{g}
  \big)_{\mathrm{flat}}
  \;\;
  \coloneqq
  \;\;
  \Big\{
    A \in \Omega^1_{\mathrm{dR}}(
      -
      ;\,
      \mathfrak{g}
    )
    \;\Big\vert\;
    \mathrm{d} A 
    +
    \tfrac{1}{2}
    [A \wedge A]
    \,=\,
    0
  \Big\}
  \mathrlap{\,.}
$$

There is a *universal* such flat form, called the *[[Maurer-Cartan form]]*
$
  \theta 
  \;\in\;
  \Omega^1_{\mathrm{dR}}(G;\, \mathfrak{g})_{\mathrm{flat}}
$,
in that the flat forms on any [[Cartesian space]] $\mathbb{R}^n$, $n \in \mathbb{N}$, are the [[pullback of differential forms|pullbacks]] of the MC-form along [[smooth maps]] $\phi \colon \mathbb{R}^n \xrightarrow{\;} G$, unique up to rigid translation along the group:

\begin{imagefromfile}
    "file_name": "UniversalPropertyOfMCForm.jpg",
    "width": 280,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}



Hence on a trivial $G$-bundle $P = X \times G$ we have a flat form $A \,\coloneqq\, \mathrm{pr}_G^\ast \theta$ which restricts on each fiber to the MC-form.

On a non-trivial principal $G$-bundle $P$ we still find a $\mathfrak{g}$-valued differential form $A \in \Omega^1_{\mathrm{dR}}(P;\, \mathfrak{g})$ that restricts on each fiber to the MC-form, but it may not itself be flat anymore, the failure being its *[[curvature 2-form|curvature]]*
$$
  F_A
  \,\coloneqq\,
  \mathrm{d}A
  +
  \tfrac{1}{2}
  [A \wedge A]
  \;\in\;
  \Omega^2_{\mathrm{dR}}(P;\, \mathfrak{g})
  \,,
$$
which is therefore a measure for the non-triviality of $P$, at least if we also demand that it is a *[[horizontal form]]* in that it vanishes on vectors tangent to the fibers -- in this case $A$ is called a *[[Ehresmann connection|principal connection]]*. 

[[Cartan calculus]] then shows that all [$\mathrm{ad}$](adjoint+action#OfALieAlgebraOnItself)-*[[invariant polynomials]]* $\langle -, \cdots, -\rangle \;\in\; \mathrm{Sym}(\mathfrak{g}^\ast)^{\mathfrak{g}}$ evaluated on the curvature 2-form are in fact closed *[[basic differential form|basic forms]]* in that they are [[pullback of differential forms|pulled back]] from closed forms on the base manifold:

\begin{imagefromfile}
    "file_name": "EhresmannConditionsDiagramB.jpg",
    "width": 580,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Thus: *Connections on principal bundles extract de Rham classes on their base space measuring their non-triviality.*

That these indeed give the above Chern-de Rham classes is the content of the *[[Chern-Weil theorem]]*.



\linebreak

## More history

It was originally apparently [[John Roberts]] who understood (remarkably: while thinking about [[quantum field theory]] in the guise of [[AQFT]]) that general cohomology is about coloring simplices in $\infty$-categories.  

* [[John E. Roberts]], *Mathematical Aspects of Local Cohomology*, in: *Algèbres d’opérateurs et leurs applications en physique mathématique*, Colloques Internationaux du Centre National de la Recherche Scientifique (C.N.R.S) **274**, Paris (1979) 321–332 &lbrack;ISBN:2-222-02441-2, [pdf](https://dmitripavlov.org/scans/roberts-mathematical-aspects-of-local-cohomology.pdf), [[Roberts-LocalCohomology.pdf:file]]&rbrack;

This is recounted in

* [[Ross Street]], pages 9-10 of: *An Australian conspectus of higher category theory*, talk at Institute for Mathematics and its Applications Summer Program: *$n$-Categories: Foundations and Applications* at the University of Minnesota (Minneapolis, 7–18 June 2004), in: *[[Towards Higher Categories]]*, The IMA Volumes in Mathematics and its Applications **152**, Springer (2010) 237-264 &lbrack;[pdf](http://www.math.uchicago.edu/~may/IMA/Street.pdf), [[Street-Conspectus.pdf:file]], [doi:10.1007/978-1-4419-1524-5](https://link.springer.com/book/10.1007/978-1-4419-1524-5)&rbrack;


Parallel to this development of the notion of [[descent|descent and codescent]] there was the development of [[homotopical cohomology theory]] as described in

* [[Kenneth S. Brown]], _Abstract Homotopy Theory and Generalized Sheaf Cohomology_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458 ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Abstract%20homotopy%20theory%20and%20generalized%20sheaf%20cohomology.pdf))

The two approaches are different, but closely related. Their relation is via the notion of [[descent|codescent]].

There is a chain of inclusions

$$
  AbelianGroups \hookrightarrow
  ChainComplexesOfAbelianGroups
  \hookrightarrow
  CrossedComplexes
  \hookrightarrow
  \omega Groupoids
  \hookrightarrow
  \omega Categories
$$

along which one can generalize the coefficient objects of ordinary cohomology. (See [[strict omega-groupoid]], [[strict omega-category]]). Since doing so in particular generalizes abelian groups to nonabelian groups (but goes much further!) this is generally addressed as leading to _nonabelian cohomology_.

Depending on the [[model category|models]] chosen, there are different concrete realizations of nonabelian cohomology. 

For instance nonabelian [[Čech cohomology]] played a special role in the motivation of the notion of [[gerbe]]s (see in particular [[gerbe (in nonabelian cohomology)]]), concretely thought of in terms of [[pseudofunctor]]s at least in the context of nonabelian [[group cohomology]], while more abstract (and less explicit) [[homotopy theory]] methods dominate the discussion of [[infinity-stack]]s.

Either way, one obtains a notion of _cohomology on $\infty$-categories with coefficients in $\infty$-catgories_. This is, most generally, the setup of "[[nonabelian cohomology]]".

This is conceptually best understood today in terms of [[Higher Topos Theory|higher topos theory]], using [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-categories of (infinity,1)-sheaves]]. 

This perspective on nonabelian cohomology is discussed for instance in [Toen 02](#Toen02)


## Properties

### Postnikov decomposition and Whitehead principle

In an [[(∞,1)-topos]] every object has a [[Postnikov tower in an (∞,1)-category]]. This means that in some sense general nonabelian cohomology can be decomposed into nonabelian cohomology in degree 1 and abelian cohomology in higher degrees, twisted by this nonabelian cohomology. This has been called ([To&#235;n](#Toen02)) the [[Whitehead principle of nonabelian cohomology]].

## Special cases

### Nonabelian group cohomology

Sometimes the term _nonabelian cohomology_ is used in a more restrictive sense. Often people mean 
[[nonabelian group cohomology]] when they say nonabelian cohomology, hence restricting to the domains to [[group|groups]], which are [[groupoid|groupoids]] with a single object.

This kind of nonabelian cohomology is discussed for instance in

* [[John Baez]], [[Mike Shulman]], [[Lectures on n-Categories and Cohomology]] ([arXiv](http://arxiv.org/abs/math.CT/0608420)).

That and how ordinary [[group cohomology]] is reproduced from the [[homotopical cohomology theory]] of [[strict omega-groupoid|strict omega-groupoids]] is discussed in detail in chapter 12 of 

* [[Ronnie Brown]], P. Higgins, R. Sivera, [[nonabelian algebraic topology|Nonabelian algebraic topology]].

For more see

* [[nonabelian group cohomology]].



### Nonabelian sheaf cohomology with constant coefficients {#NonabelianSheafCohomology}

For $X$ a [[topological space]] and $A$ an [[∞-groupoid]], the standard way to define the [[nonabelian cohomology]] of $X$ with coefficients in $A$ is to define it as the intrinsic cohomology as seen in [[∞Grpd]] $\simeq$ [[Top]]:

$$
  H(X,A) 
   \;\coloneqq\; 
  \pi_0 Top(X, |A|) \simeq \pi_0 \infty Func(Sing X, A)
  \,,
$$

where $|A|$ is the [[geometric realization]] of $A$ and $Sing X$ the [[fundamental ∞-groupoid]] of $X$.

But both $X$ and $A$ here naturally can be regarded, in several ways, as objects of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf (∞,1)-topos]]es $\mathbf{H} = Sh_{(\infty,1)}(C)$ over nontrivial [[(∞,1)-site]]s $C$. The intrinsic cohomology of such $\mathbf{H}$ is a [[nonabelian cohomology|nonabelian sheaf cohomology]]. The following discusses two such choices for $\mathbf{H}$ such that the corresponding nonabelian sheaf cohomology coincides with $H(X,A)$ (for [[paracompact space|paracompact]] $X$).

#### Petit $(\infty,1)$-sheaf $(\infty,1)$-topos

For $X$ a [[topological space]] and $Op(X)$ its [[category of open subsets]] equipped with the canonical structure of an [[(∞,1)-site]], let 

$$
  \mathbf{H}
    \;\coloneqq\;
  Sh_{(\infty,1)}(X) 
    \;\coloneqq\; 
  Sh_{(\infty,1)}(Op(X))
$$

be the [[(∞,1)-category of (∞,1)-sheaves]] on $X$. The space $X$ itself is naturally identified with the [[terminal object]] $X = * \in Sh_{(\infty,1)}(X)$. This is the [[petit topos]] incarnation of $X$.

Write

$$
  (LConst \dashv \Gamma) :  Sh_{(\infty,1)}(X)
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

be the [[global section]]s terminal [[geometric morphism]]. 

Under the [[constant (∞,1)-sheaf]] functor $LConst$ an an [[∞-groupoid]] $A \in \infty Grpd$ is regarded as an object $LConst A \in Sh_{(\infty,1)}(X)$. 

There is therefore the _intrinsic_ [[cohomology]] of the $(\infty,1)$-topos $Sh_{(\infty,1)}(X)$ with coefficients in the [[constant ∞-stack|constant (∞,1)-sheaf]] on $A$
  
$$
  H'(X,A) 
  \;\coloneqq\; 
  \pi_0 Sh_{(\infty,1)}(X)(X, LConst A)
  \,.
$$

This is [[cohomology with constant coefficients]].

Notice that since $X$ is in fact the [[terminal object]] of $Sh_{(\infty,1)}(X)$ and that $Sh_{(\infty,1)}(X)(X,-)$ is in fact that [[global section]]s functor, this is equivalently

$$
  \cdots \simeq \pi_0 \Gamma LConst A
  \,.
$$

+-- {: .un_theorem }
###### Theorem

If $X$ is a [[paracompact space]], then these two definitins of [[nonabelian cohomology]] of $X$ with [[constant ∞-stack|constant coefficients]] $A \in \infty Grpd$ agree:

$$
  H(X,A) 
  \;\coloneqq\; 
  \pi_0 \infty Grpd(Sing X,A)  \simeq Sh_{(\infty,1)}(X)(X,LConst A)
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, theorem 7.1.0.1]]. See also [[(∞,1)-category of (∞,1)-sheaves]] for more.


#### Gros $(\infty,1)$-sheaf $(\infty,1)$-topos

Another alternative is to regard the space $X$ as an object in the [[cohesive (∞,1)-topos]] [[ETop∞Grpd]]. 

$$
  (\Pi \dashv LConst \dashv \Gamma)
  :
  ETop\infty Grpd
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
  \,,
$$

with the further [[left adjoint]] $\Pi$ to $LConst$ being the intrinsic [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] functor.  The intrinsic [[nonabelian cohomology]] in there also coincides with nonabelian cohomology in [[Top]]; even the full [[cocycle]] [[∞-groupoid]]s are equivalent:

+-- {: .un_theorem }
###### Theorem

For [[paracompact space|paracompact]] $X$ we have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  ETop\infty Grpd(X, LConst A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H(X,A) \simeq \pi_0   ETop\infty Grpd(X, LConst A)
$$

=--

+-- {: .proof}
###### Proof

See [[ETop∞Grpd]].

=--

## Examples

Examples of *generalized* nonabelian cohomology (with general classifying spaces):

* [[unstable topological K-theory]]

* [[Cohomotopy]]


## Objects classified by nonabelian cohomology

For $g : X \to A$ a [[cocycle]] in nonabelian cohomology, we say the [[fibration sequence|homotopy fibers]] of $g$ is the object _classified_ by $g$.

For examples and discussion of this see

* [[principal bundle]]

* [[principal 2-bundle]], [[gerbe]]

* [[principal 3-bundle]], [[2-gerbe]]

* [[principal ∞-bundle]], [[∞-gerbe]]

* [[twisted form|twisted forms]] .

## Related concepts

* [[nonabelian Poincaré duality]]

* [[nonabelian de Rham cohomology]]

* [[differential non-abelian cohomology]]

* [[generalized cohomology]]

* [[Chern-Weil theory]]

## References
 {#References}

### Classical theory -- bundles and groups

The classical notion of non-abelian ([[Čech cohomology|Čech]]-)cohomology in degree 1 and its relation to [[fiber bundles]]/[[principal bundles]]:


* [[Alexander Grothendieck]], Chapter V of: *A General Theory of Fibre Spaces With Structure Sheaf*, University of Kansas, Report No. 4 (1955, 1958) &lbrack;[pdf](https://webusers.imj-prg.fr/~leila.schneps/grothendieckcircle/Kansasnotes.pdf), [[Grothendieck-FibreSpaces.pdf:file]]&rbrack;

* [[Jean Frenkel]], *Cohomologie à valeurs dans un faisceau non abélien*, C. R. Acad. Se., t. 240 (1955) 2368-2370
 
* [[Jean Frenkel]], *Cohomologie non abélienne et espaces fibrés*, Bulletin de la Société Mathématique de France, **85** (1957) 135-220 &lbrack;[numdam:BSMF_1957__85__135_0](http://www.numdam.org/item/BSMF_1957__85__135_0)&rbrack;

Review:

* [[Torsten Wedhorn]], *Torsors and Non-abelian Čech Cohomology*, chapter 7 in: *Manifolds, Sheaves, and Cohomology*, Springer (2016) &lbrack;[doi:10.1007/978-3-658-10633-1](https://doi.org/10.1007/978-3-658-10633-1)&rbrack;

Review in topological spaces (via [[classifying spaces]]):

* Nicolas Addington, _Fiber bundles and nonabelian cohomology_, talk at *[Graduate Student Topology Conference](https://www.math.uchicago.edu/~gstc/)* (2007) &lbrack;[pdf](http://pages.uoregon.edu/adding/notes/gstc2007.pdf)&rbrack;

* {#Mitchell11} [[Stephen Mitchell]], around Theorem 7.4 in: _Notes on principal bundles and classifying spaces_, Lecture Notes. University of Washington (2011) &lbrack;[pdf](https://sites.math.washington.edu/~mitchell/Notes/prin.pdf), [[MitchellPrincipalBundles.pdf:file]]&rbrack;

* {#RudolfSchmidt17} [[Gerd Rudolph]], [[Matthias Schmidt]], Thm. 3.5.1 of: *Differential Geometry and Mathematical Physics Part II. Fibre Bundles, Topology and Gauge Fields*, Springer (2017) &lbrack;[doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8)&rbrack;

See also:

*  Jinpeng An. Zhengdong Wang, _Nonabelian cohomology with coefficients in Lie groups_, Trans. Amer. Math. Soc. **360** (2008) 3019-3040 &lbrack;[doi:10.1090/S0002-9947-08-04278-5](https://doi.org/10.1090/S0002-9947-08-04278-5)&rbrack;


The case of [[nonabelian group cohomology]]:

* {#Milne17} [[James Milne]], Section 27.a (of the [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf), not present in the published version) of: *Algebraic Groups*, Cambridge University Press 2017  ([doi:10.1017/9781316711736](https://doi.org/10.1017/9781316711736), [webpage](http://www.jmilne.org/math/Books/iag.html), [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf))


### Categorified theory -- 2-bundles/gerbes 
 {#CategorifiedTheory}

Early discussion, of higher non-abelian cohomology with [[coefficients]] in certain [[2-groups]] (implicitly):

* [[Paul Dedecker]], *Cohomologie à coefficients non abéliens et espaces fibrés*,  Bulletins de l'Académie Royale de Belgique **41** (1955) 1132-1146 &lbrack;[persee:barb_0001-4141_1955_num_41_1_69497](https://www.persee.fr/doc/barb_0001-4141_1955_num_41_1_69497)&rbrack;

* [[Paul Dedecker]], *Cohomologie de dimension 2 à coefficients non abéliens*, C. R. Acad. Sci. Paris **247** (1958) 1160-1163 &lbrack;[BnF](https://gallica.bnf.fr/ark:/12148/bpt6k7258/f192.item.r=dedecker)&rbrack;

* [[Paul Dedecker]], *Sur La Cohomologie Non Abelienne I (Dimension Deux)*, Canadian Journal of Mathematics **12** (1960) 231-251 &lbrack;[doi:10.4153/CJM-1960-019-7](https://doi.org/10.4153/CJM-1960-019-7)&rbrack;

and with coefficients in certain [[3-groups]] presented by [[crossed squares]]:

* [[Paul Dedecker]], A. Frei, _Les relations d'&#233;quivalence des morphismes de la suite exacte de cohomologie non ab&#234;lienne_, C. R. Acad. Sci. Paris **262** (1966) 1298-1301

* [[Paul Dedecker]], _Three dimensional non-abelian cohomology for groups_, Category theory, homology theory and their applications, II (Battelle Institute Conf.) 1969 ([MathSciNet](http://www.ams.org/mathscinet/pdf/263894.pdf?pg1=IID&s1=55880&vfpref=html&r=15))


The correct definition using [[crossed modules]] of sheaves then appeared in 

* {#Debremaeker76} Raymond Debremaeker, _Cohomologie met waarden in een gekruiste groepenschoof op een situs_, PhD thesis, 1976 (Katholieke Universiteit te Leuven). English translation: 
_Cohomology with values in a sheaf of crossed groups over a site_, arXiv:[1702.02128](https://arxiv.org/abs/1702.02128)

Of [[algebra|algebraic]] [[structures]]:

*  [[René Lavendhomme]], J. R. Roisin, _Cohomologie non abélienne de structures algèbriques_, Journal of Algebra **67** 2 (1980) 385-414 &lbrack;<a href="https://doi.org/10.1016/0021-8693(80)90168-4">doi:10.1016/0021-8693(80)90168-4</a>&rbrack;


Discussion in terms of [[gerbes]]:

* [[Jean Giraud]], _Cohomologie non ab&#233;lienne_ , Springer  (1971) &lbrack;[doi:10.1007/978-3-662-62103-5](https://link.springer.com/book/10.1007/978-3-662-62103-5)&rbrack;

  > (aspects of classification of $G$-[[gerbes]] by cohomology with coefficients in the [[automorphism 2-group]] $AUT(G)$, but imposes extra constraints)


* [[Larry Breen]], _Bitorseurs et cohomologie non-Ab&#233;lienne_, The Grothendieck Festschrift: a collection of articles written in honour of the 60th birthday of Alexander Grothendieck, Vol. I, edited P.Cartier, et al., Birkh&#228;user, Boston, Basel, Berlin, 401-476, (1990) ([doi:10.1007/978-0-8176-4574-8_10](https://doi.org/10.1007/978-0-8176-4574-8_10))

* [[John Duskin]]: _Non-abelian cohomology in a topos_, reprinted as: Reprints in Theory and Applications of Categories **23** (2013) 1-165 &lbrack;[tac:tr23](http://www.tac.mta.ca/tac/reprints/articles/23/tr23abs.html)&rbrack;

* [[Ieke Moerdijk]]: _Lie Groupoids, Gerbes, and Non-Abelian Cohomology_, K-Theory **28** 3 (2003) 207-258 &lbrack;[journal](http://www.springerlink.com/content/ul554x3077444545/), [doi:10.1023/A:1026251115381](http://dx.doi.org/10.1023/A:1026251115381)&rbrack;

* [[Amnon Yekutieli]], *Combinatorial descent data for gerbes*, Journal of Noncommutative Geometry **8** 4 (2014) 1083–1099 &lbrack;[arXiv:1109.1919](https://arxiv.org/abs/1109.1919), [webpage](https://www.math.bgu.ac.il/~amyekut/publications/comb-descent/comb-descent.html)&rbrack;

* [[Alexander Campbell]], _A higher categorical approach to Giraud's non-abelian cohomology_, PhD thesis, Macquarie University (2016) &lbrack;[hdl:1959.14/1261186](http://hdl.handle.net/1959.14/1261186)&rbrack;


Existence of [[classifying spaces]] for [[principal 2-bundles]]/[[nonabelian gerbes]]:

* [[John Baez]], [[Danny Stevenson]], _The Classifying Space of a Topological 2-Group_,  In: Baas N., Friedlander E., Jahren B., Østvær P. (eds.) *Algebraic Topology*, Abel Symposia, vol 4. Springer 2009 ([arXiv:0801.3843](https://arxiv.org/abs/0801.3843), [doi:10.1007/978-3-642-01200-6_1](https://doi.org/10.1007/978-3-642-01200-6_1))


### General theory -- $\infty$-bundles/$\infty$-gerbes

Discussion of the general theory via [[principal ∞-bundles]] and/or [[∞-gerbes]] and/or [[∞-stacks]]:

* [[Paul Glenn]], _Realization of cohomology classes in arbitrary exact categories_, J. Pure Appl. Algebra 25, 1982, no. 1, 33- 105 (<a href="https://doi.org/10.1016/0022-4049(82)90094-9">doi:10.1016/0022-4049(82)90094-9</a>)

In a context of [[nonabelian Hodge theory]]:

* [[Carlos Simpson]], _The Hodge filtration on nonabelian cohomology_, in: János Kollár, Robert Lazarsfeld, [[David Morrison]] (eds.) _Algebraic Geometry Santa Cruz 1995, Part 2_, Proceedings of Symposia in Pure Mathematics Volume 62.2, AMS 1997 ([arXiv:alg-geom/9604005](http://arxiv.org/abs/alg-geom/9604005), [doi:10.1090/pspum/062.2](https://doi.org/10.1090/pspum/062.2))

* [[Carlos Simpson]], _Secondary Kodaira-Spencer classes and nonabelian Dolbeault cohomology_ ([arXiv:alg-geom/9712020](http://arxiv.org/abs/alg-geom/9712020))

* {#Simpson02} [[Carlos Simpson]]: _Algebraic aspects of higher nonabelian Hodge theory_,  in: [[Fedor Bogomolov]], [[Ludmil Katzarkov]] (eds.), _Motives, polylogarithms and Hodge theory, Part II_ (Irvine, CA, 1998), Int. Press Lect. Ser., 3, II, Int. Press, (2002, 2016) 417-604 &lbrack;[arXiv:math/9902067](http://arxiv.org/abs/math/9902067), [ISBN:9781571462909](https://www.intlpress.com/site/pub/pages/books/items/00000089/index.php)&rbrack;

* [[Carlos Simpson]], [[Tony Pantev]], [[Ludmil Katzarkov]], _Nonabelian mixed Hodge structures_ ([arXiv:math/0006213](http://arxiv.org/abs/math/0006213))

Generally:

* {#Toen02} [[Bertrand Toën]], Def. 6.0.6 in: _Stacks and Non-abelian cohomology_, lecture at _[Introductory Workshop on Algebraic Stacks, Intersection Theory, and Non-Abelian Hodge Theory](https://www.msri.org/realvideo/index04.html)_, MSRI (2002) &lbrack;[slides](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/index.html), [ps](http://www.msri.org/publications/ln/msri/2002/introstacks/toen/1/meta/aux/toen.ps), [pdf](https://perso.math.univ-toulouse.fr/btoen/files/2015/02/msri2002.pdf), [[ToenStacksAndNonabelianCohomology.pdf:file]]&rbrack;

* [[J. F. Jardine]], Z. Luo, _Higher principal bundles_, Mathematical Proceedings of the Cambridge Philosophical Society,  Volume 140, Issue 2 March 2006 , pp. 221-243 ([pdf](http://www.math.uiuc.edu/K-theory/0681/cocycles6.pdf), [doi:10.1017/S0305004105008911](https://doi.org/10.1017/S0305004105008911))

* [[J. F. Jardine]], _Cocycle categories_, In: [[Nils Baas]], [[Eric Friedlander]], B. Jahren , [[Arne Østvær]] (eds.) _Algebraic Topology_, Abel Symposia, vol 4. Springer 2009 ([arXiv:math/0605198](https://arxiv.org/abs/math/0605198), [doi:10.1007/978-3-642-01200-6_8]( https://doi.org/10.1007/978-3-642-01200-6_8))

* [[Jacob Lurie]], Thm. 7.1.0.1 in: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))


* {#Wendt} [[Matthias Wendt]], *Classifying spaces and fibrations of simplicial sheaves*, Journal of  Homotopy and Related Structures **6** 1 (2011) 1-38  &lbrack;[arXiv:1009.2930](http://arxiv.org/abs/1009.2930), [JHRS:6-1](http://tcms.org.ge/Journals/JHRS/volumes/2011/volume6-1.htm)&rbrack;

* {#RobertsStevenson16} [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundles in parametrized spaces_, New York Journal of Mathematics Volume 22 (2016) 405-440 ([arXiv:1203.2460](https://arxiv.org/abs/1203.2460), [nyjm:22-19](http://nyjm.albany.edu/j/2016/22-19.html))

* [[Danny Stevenson]], _Classifying theory for simplicial parametrized groups_ ([arXiv:1203.2461](https://arxiv.org/abs/1203.2461))

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- General theory]]_, Journal of Homotopy and Related Structures **10** 4 (2015) 749-801 &lbrack;[doi:10.1007/s40062-014-0083-6](http://link.springer.com/article/10.1007/s40062-014-0083-6), [arXiv:1207.0248](http://arxiv.org/abs/1207.0248)&rbrack;

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- Presentations]]_, Journal of Homotopy and Related Structures **10** 3 (2015) 565-622 &lbrack;[doi:10.1007/s40062-014-0077-4](http://link.springer.com/article/10.1007/s40062-014-0077-4), [arXiv:1207.0249](http://arxiv.org/abs/1207.0249)&rbrack;

* [[John F. Jardine]]: *Non-abelian Cohomology*, chapter 9 in: *[[Local Homotopy Theory]]*, Springer Monographs in Mathematics (2015) &lbrack;[doi:10.1007/978-1-4939-2300-7_9](https://doi.org/10.1007/978-1-4939-2300-7_9)&rbrack;

On [[cohomology operations]] on components of [[Whitehead-generalized cohomology theories]] seen in non-abelian cohomology:

* [[John Michael Boardman]], [[David Copeland Johnson]], [[W. Stephen Wilson]], _Unstable Operations in Generalized Cohomology_ ([pdf](https://hopf.math.purdue.edu/Boardman-Johnson-Wilson/bjw.pdf)), in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))

The suggestion that *every* ([[pointed topological space|pointed]]) [[topological space|space]]/[[infinity-stack|$\infty$-stack]] may be regarded as being the [[classifying space]] of a non-abelian cohomology theory, and that this is what defines non-abelian cohomology in general:

* [Toën 2002](#Toen02)

* {#SS08} [[Hisham Sati]], [[Urs Schreiber]] et al., p 41 of: *Twisted differential nonabelian cohomology* (2008) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schreiber/nactwist.pdf), [[Schreiber-nactwist.pdf:file]]&rbrack;

* {#Schreiber09} [[Urs Schreiber]]: *[[schreiber:Background fields in twisted differential nonabelian cohomology|Background fields in twisted differential nonabelian cohomology]]*, talk at *[[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]*, Oberwolfach Report **28** (2009) 1578-1582 &lbrack;[[OWR_2009_28.pdf:file]], [doi:10.4171/owr/2009/28](https://doi.org/10.4171/owr/2009/28)&rbrack;
 > (in [[twisted cohomology|twisted]] and [[differential cohomology|differential]] generality)

* {#Lurie14} [[Jacob Lurie]], Def. 6 in: *Nonabelian Poincaré Duality*, Lecture 8 in *[Tamagawa Numbers via Nonabelian Poincaré Duality (282y)](https://www.math.ias.edu/~lurie/282y.html)* (2014) &lbrack;[pdf](http://www.math.harvard.edu/~lurie/282ynotes/LectureVIII-Poincare.pdf), [[Lurie-NonabPoincareDuality.pdf:file]]&rbrack;
  > (in view of [[nonabelian Poincaré duality]])

* {#FSS23} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The Character Map in Nonabelian Cohomology --- Twisted, Differential, Generalized]]_, World Scientific (2023) &lbrack;[arXiv:2009.11909](https://arxiv.org/abs/2009.11909), [doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;
  > (generalizing the [[Chern-Dold character]] to nonabelian cohomology in this sense)


[[!include unstable classification of topological phases -- references]]



[[!redirects non-abelian cohomology]]

[[!redirects nonabelian cohomology theory]]
[[!redirects nonabelian cohomology theories]]

[[!redirects non-abelian cohomology theory]]
[[!redirects non-abelian cohomology theories]]

[[!redirects ordinary nonabelian cohomology]]
[[!redirects ordinary nonabelian cohomology theory]]
[[!redirects ordinary nonabelian cohomology theories]]

[[!redirects ordinary non-abelian cohomology]]
[[!redirects ordinary non-abelian cohomology theory]]
[[!redirects ordinary non-abelian cohomology theories]]



