
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### In ordinary cohomology
  {#InOrdinaryCohomology}

The _Serre spectral sequence_ or _Leray-Serre spectral sequence_
is a [[spectral sequence]] for computation of [[ordinary cohomology]] ([[ordinary homology]]) of [[topological spaces]] in a [[Serre fibration|Serre]]-[[fiber sequence]] of [[topological spaces]].

\begin{proposition}\label{OrdinaryCohomologicalSerreSpectralSequence}
**(ordinary cohomology Serre spectral sequence)**\linebreak

Given a [[homotopy fiber sequence]]

$$
  \array{
     F &\longrightarrow& E
     \\
     && \downarrow^{\mathrlap{p}}
     \\
     && X
  }
$$

over a [[connected topological space]] $X$,
such that the canonical [[group action]] of the [[fundamental group]] $\pi_1(X)$ on the [[ordinary cohomology]] of the [[fiber]] $F$ is [[trivial action|trivial]] (for instance if $X$ is a [[simply connected topological space]]), then there exists a *cohomology Serre spectral sequence* of the form:

\[
  \label{SecondPageAndConvergenceOfOrdinaryCohomologicalSerreSpectralSequence}
  E_2^{p,q}
  \;=\; 
  H^p
  \big(
    X, 
    \,
    H^q(F)
  \big) 
  \;\Rightarrow\; 
  H^{p+q}(E)
  \,.
\]

\end{proposition}

(e.g. [Hatcher, Thm. 1.14](#Hatcher))

{#ConvergenceOfTheOrdinaryCohomologySSS} Hence for $n \in \mathbb{N}$ we have a [[filtration]] of [[abelian groups]]

\[
  \label{FilteringForOrdinaryCohomologySerreSpectralSequence}
  0
  \xhookrightarrow{
    \;\;
    E^{n,0}_\infty
    \;\;
  }
  F^n_n
  \xhookrightarrow{
    E^{n-1,1}_\infty
  }
  F^n_{n-1}
  \xhookrightarrow{\;\;\;\;\;}
  \cdots
  \xhookrightarrow{\;\;\;\;\;}
  F^n_{1}
  \xhookrightarrow{
    \;\;
    E^{0,n}_\infty
    \;\;
  }
  F^n_0
  \;=\;
  H^n(E)
  \,,
\]

where

$$
  F^n_{p+1}
  \xhookrightarrow{
    E^{p,n-p}_\infty
  }
  F^n_{p}
  {\phantom{AAAA}}
  \text{means that}
  {\phantom{AAAA}}
  0 
  \to
  F^n_{p+1}
  \xhookrightarrow{\;}
  F^n_{p}
  \twoheadrightarrow
  E^{p,n-p}_\infty
  \to
  0
  \,,
$$

hence that -- iteratively as $p$ *decreases* -- $F^n_p$ is an [[algebra extension|extension]] of $E^{p,n-p}_\infty$ by $F^n_{p+1}$.


### In generalized cohomology

The generalization of this from [[ordinary cohomology]] to [[generalized (Eilenberg-Steenrod) cohomology]] is the _[[Atiyah-Hirzebruch spectral sequence]]_, see there for details.

### In relative cohomology
 {#InRelativeCohomology}

There are two kinds of **relative Serre spectral sequences**.

For $F \to E \to X$ as above and $A \hookrightarrow X$ a subspace, the induced restriction of the fibration

$$
  \array{   
    F & \simeq & F
    \\
    \downarrow && \downarrow
    \\
    p^{-1}(A) &\longrightarrow& E
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    A &\hookrightarrow& X
  }
$$

induces a spectral sequence in [[relative cohomology]] of the base space of the form

$$
  E_2^{p,q}
  =
  H^p(X,A; H^q(F))
    \;\Rightarrow\;
  H^\bullet(E, p^{-1}(A))
  \,.
$$

(e.g. [Davis 91, theorem 9.33](#Davis91))

Conversely, for 

$$
  \array{   
    F' & \hookrightarrow & F
    \\
    \downarrow && \downarrow
    \\
    E' &\hookrightarrow& E
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    X &\hookrightarrow& X
  }
$$

a sub-fibration over the same base, then this induces a spectral sequence for [[relative cohomology]] of the the total space in terms of ordinary cohomology with coefficients in the relative cohomology of the fibers:

$$
  E^{p,q}_2 = H^p(X; H^q(F,F'))
    \;\Rightarrow\;
  H^\bullet(E,E')
  \,.
$$

(e.g. [Kochman 96, theorem 2.6.3](#Kochman96), [Davis 91, theorem 9.34](#Davis91))

### In equivariant cohomology

There is also a generalization to [[equivariant cohomology]]: for [cohomology with coefficients in a Mackey functor](Mackey+functor#Cohomology) with[[RO(G)-grading]] for [[representation spheres]] $S^V$, then for $E \to X$ an $F$-fibration of [[topological G-spaces]] and for $A$ any $G$-[[Mackey functor]], the equivariant Serre spectral sequence looks like ([Kronholm 10, theorem 3.1](#Kronholm10)):

$$
  E_2^{p,q} = H^p(X, H^{V+q}(F,A)) \,\Rightarrow\, H^{V+p+q}(E,A)
  \,,
$$

where on the left in the $E_2$-page we have [[ordinary cohomology]] with [[coefficients]] in the genuine equivariant cohomology groups of the fiber.


## Details

For details on the plain Serre spectral sequence see at _[[Atiyah-Hirzebruch spectral sequence]]_ and take $E = H R$ to be ordinary cohomology.  

## Examples


\begin{example}\label{IntegralCohomologyOfHomotopyQuotientOf4SphereByADEAction}
**([[integral cohomology]] of [[homotopy quotient]] of [[4-sphere]] by [[finite subgroup of SU(2)]])** \linebreak

  Let 

  * $G \xhookrightarrow{\;i\;} Sp(1) \simeq SU(2) \simeq Spin(3)$ be a [[finite subgroup of SU(2)]];

  * $\mathbb{H} \,\in\, G Actions(VectorSpaces_{\mathbb{R}})$ the [[linear representation]] of $G$ on the [[quaternions]], regarded as a 4d [[real vector space]], which is the [[restricted representation]] of the defining representation of [[Sp(1)]];

  * $S^{\mathbb{H}} \in G Actions(TopologicalSpaces)$ the corresponding [[representation sphere]].

Then the [[integral cohomology]] in degree 4 of the [[homotopy quotient]] is the [[direct sum]]

\[
  \label{Integral4CohomologyOfHomotopyQuotientOf4SphereByFiniteSubgroupOfSU2}
  H^4
  \big(
    S^{\mathbb{H}} \!\sslash\! G,
    \,
    \mathbb{Z}
  \big)
  \;\;
  \simeq
  \;\;
  \mathbb{Z} \oplus (\mathbb{Z}/\left\vert G \right\vert)
\]

of the [[integers]] with the [[cyclic group]] of [[order of a group|order]] that of $G$.

\end{example}
\begin{proof}
By the [[Borel construction]] we have a [[homotopy fiber sequence]] of the form
\[
  \label{BorelConstructionFor4SphereActedOnByADESubgroup}
  \array{
    S^4 &\longrightarrow& S^{\mathbb{H}} \!\sslash\! G
    \\
    && \big\downarrow
    \\
    && B G
  }
\]

over the [[classifying space]] of $G$. 

Here the [[integral cohomology]] of the [[4-sphere]] [[fiber]] is (e.g. by the nature of the [[Eilenberg-MacLane space]] $K(\mathbb{Z},4)$)

\[
  \label{IntegralCohomologyOfThe4Sphere}
  H^n
  \big(
    S^4,
    \,
    \mathbb{Z}
  \big)
  \;\simeq\;
  \left\{
  \array{
    \mathbb{Z} & for & n \in \{0,4\}
    \\
    0 & \text{otherwise} \,.
  }
  \right.
\]

We claim that the [[group action]] of $\pi_1(B G) \simeq G$ (by [this Prop.](simplicial+classifying+space#HomotopyGroupsOfBarWG)) on the [[integral cohomology]] of the [[fiber]] is [[trivial action|trivial]]. This follows by observing that: 

1. we have an [[isomorphism]] of [[topological G-spaces]] between the [[representation sphere]] of $\mathbb{H}$ and the [[unit sphere]] in $\mathbb{R} \oplus \mathbb{H}$ (by [this Prop.](representation+sphere#RepresentationSpheresAsUnitSpheres)):

   $$
     S^{\mathbb{H}}
     \;\simeq_{G}\;
     S(\mathbb{R} \oplus \mathbb{H})
     \,;
   $$


1. the [[group action]] of [[Sp(1)]] on $\mathbb{H} \simeq_{\mathbb{R}} \mathbb{R}^4$ is through the defining action of [[SO(4)]], hence the action on $\mathbb{R} \oplus \mathbb{H}$ is through [[SO(5)]], 

   because [[quaternions]] are a [[normed division algebra]], so that left-multiplication by unit-[[norm]] quaternions $q \in$ [[Sp(1)]] $= S(\mathbb{H})$ preserves the [[norm]] (e.g [[schreiber:Equivariant homotopy and super M-branes|HSS 18, Rem. A.8]]);

1. the generator of $H^4(S^4,\mathbb{Z})$ may be identified with the [[volume form]] (under the [[Hopf degree theorem]] and the [[de Rham theorem]]) which is manifestly preserved by the action of the [[special orthogonal group]] $SO(5)$.

Therefore, the [[integral cohomology|integral]]-cohomological Serre spectral sequence (Prop. \ref{OrdinaryCohomologicalSerreSpectralSequence}) applies to the Borel fiber sequence (eq:BorelConstructionFor4SphereActedOnByADESubgroup).

Now, noticing that the [[integral cohomology]] of a [[classifying space]] of a [[discrete group]] is its [[group cohomology]]

$$
  H^\bullet(B G, \mathbb{Z})
  \;\simeq\;
  H^\bullet_{grp}(G, \mathbb{Z})
$$

we have for the given [[finite subgroup of SU(2)]] (by [this Prop](finite+rotation+group#GroupCohomologyOfFiniteSubgroupsOfSU2)) that:

\[
  \label{IntegralCohomologyOfClassifyingSpaceOfFiniteSubgroupOfSU2}
  H^4(B G, \mathbb{Z})
  \;\simeq\;
  \left\{
  \array{
    \mathbb{Z} &\vert& n = 0
    \\
    G^{ab} &\vert&  n = 2 \, mod \, 4
    \\
    \mathbb{Z}/{\vert G \vert} 
    &\vert& 
    n \, \text{positive multiple of} \, 4
    \\
    0 &\vert& \text{otherwise} \,,
  }
  \right.
\]

where $G^{ab} \coloneqq G / [G,G]$ denotes the [[abelianization]] of $G$.


Using the cohomology groups
(eq:IntegralCohomologyOfThe4Sphere)
and
(eq:IntegralCohomologyOfClassifyingSpaceOfFiniteSubgroupOfSU2) 
in the fomula 
(eq:SecondPageAndConvergenceOfOrdinaryCohomologicalSerreSpectralSequence)
for the second page $E_2^{\bullet, \bullet}$
of the cohomology Serre spectral sequence (Prop. \ref{OrdinaryCohomologicalSerreSpectralSequence}) shows that this is of the following form:

\begin{tikzcd}[row sep={between origins, 21pt}, column sep={between origins, 21pt}]
      {}
      &
      {}
      \\[-12pt]
      {}
          &
      {}
      \\
      &
      \vdots
      &
      \vdots
      &
      \vdots
      &
      \vdots
      &
      \vdots
      &
      \vdots
      &
      \vdots
      &
      \vdots
      \\
      {}
      \ar[
        ddddddrrrrrr,
        -,
        line width=19pt,
        shift left=1pt,
        opacity=.15,
        color=blue
      ]
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      \cdots
      \\
      &
      \mathbb{Z}
      \ar[  
        drr
      ]
      &
      0
      %\ar[
      %  drr
      %]
      &
      G^{\mathrm{ab}}
      \ar[
        drr
      ]
      &
      0
      &
      \mathbb{Z}_{\left\vert G\right\vert}
      \ar[
        drr
      ]
      &
      0
      &
      G^{\mathrm{ab}}
      \ar[
        drr
      ]
      &
      0
      &
      \cdots
      \\
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      \cdots
      \\
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      \cdots
      \\
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      0
      &
      \cdots      
      \\
      \ar[
        rrrrrrrrrr,
        color=lightgray,
        shift right=5pt,
        "B G"{below, color=black, pos=.95}
      ]
      &
      \mathbb{Z}
      &
      0
      &
      G^{\mathrm{ab}}
      &
      0
      &
      \mathbb{Z}_{\left\vert G\right\vert}
      &
      0
      &
      G^{\mathrm{ab}}
      &
      0
      &
      \cdots
      &
      {}
      \\
      & 
      \ar[
        uuuuuuuuu,
        color=lightgray,
        shift left=5pt,
        "S^4"{left, color=black, pos=.93}
      ]
      &{}&{}&{}&{}&{}
\end{tikzcd}

Since the [[codomains]] of the [[differentials]] on all the following pages are translated diagonally (downwards and rightwards, by the [general formula](spectral+sequence#eq:FormOfDifferentialInCohomologySpectralSequence)) from the codomains seen above, one sees that for every differential on every page, the [[domain]] or the [[codomain]] is the [[zero group]]. 

This means that all differentials are the [[zero morphism]], hence that the spectral sequence collapses already on this second page:

$$
  E^{\bullet, \bullet}_\infty
  \;\;
  \simeq
  \;\;
  E^{\bullet, \bullet}_2
  \,.
$$

Therefore the convergence statement (eq:FilteringForOrdinaryCohomologySerreSpectralSequence) says that the degree-4 cohomology group in question is a [[group extension]] of 

$$
  E^{0,4}_\infty 
  \;\simeq\;
  H^0\big(B G, \, H^4(S^4; \mathbb{Z}) \big) 
  \;\simeq\; 
  H^0\big( B G, \, \mathbb{Z}\big)
  \;\simeq\;
  \mathbb{Z}
$$

by

$$
  E^{4,0}_\infty 
  \;\simeq\;
  H^4\big(B G, \, H^0(S^4; \mathbb{Z}) \big) 
  \;\simeq\; 
  H^4\big( B G, \, \mathbb{Z}\big)
  \;\simeq\;
  \mathbb{Z}/\left\vert G \right\vert
$$

in that we have a [[short exact sequence]] of the form

$$ 
  0 
  \to
  \mathbb{Z}/\left\vert G\right\vert
  \hookrightarrow
  H^4\big( S^4 \!\sslash\! G;\, \mathbb{Z} \big)
  \twoheadrightarrow
  \mathbb{Z}
  \to 
  0
  \,.
$$

But since the [[Ext-group]] of the [[integers]] is [[trivial group|trivial]] ([this Expl.](Ext#ExtensionsOfTheIntegersAreTrivial)) this extension must be the [[direct sum]]

$$
  H^4\big( S^4 \!\sslash\! G;\, \mathbb{Z} \big)
  \;\simeq\;
  \mathbb{Z}_{\left\vert G\right\vert}
  \oplus
  \mathbb{Z}
  \,.
$$

This is the claim (eq:Integral4CohomologyOfHomotopyQuotientOf4SphereByFiniteSubgroupOfSU2) to be proven.
\end{proof}



## Consequences

* [[Serre long exact sequence]]

* [[Thom-Gysin sequence]]

## Related concepts

* [[long exact sequence in cohomology]]

  * [[long exact sequence in generalized cohomology]]


## References

### General

The original article is 

* [[Jean-Pierre Serre]], _Homologie singuli&#233;re des espaces fibr&#233;s_ Applications, Ann. of Math. 54 (1951), 

Textbook accounts:

* {#Hatcher} [[Alan Hatcher]], _[Spectral sequences in algebraic topology](https://pi.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _I: The Serre spectral sequence_ ([pdf](https://pi.math.cornell.edu/~hatcher/SSAT/SSch1.pdf), [[Hatcher_SerreSpectralSequence.pdf:file]])

* {#Kochman96} [[Stanley Kochman]], section 2.2. of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Davis91} Davis, _Lecture notes in algebraic topology_, 1991

Lecture notes etc. includes

* [[Greg Friedman]], _Some extremely brief notes on the Leray spectral sequence_ ([pdf](http://faculty.tcu.edu/richardson/Seminars/Gregspecseq.pdf))

Discussion in [[homotopy type theory]] includes

* [[Mike Shulman]], _[Spectral Sequences](http://homotopytypetheory.org/2013/08/08/spectral-sequences/)_, 2013

and implementation in [[Lean]] is in 

* [[Floris van Doorn]], [[Egbert Rijke]], [[Ulrik Buchholtz]], [[Favonia]], [[Steve Awodey]], [[Jeremy Avigad]], [[Mike Shulman]], [[Jonas Frey]],  _Spectral_ ([github.com/cmu-phil/Spectral](https://github.com/cmu-phil/Spectral))

### In equivariant cohomology

In [[equivariant cohomology]], for [[Bredon cohomology]]:

* [[Ieke Moerdijk]], J.-A. Svensson, _The Equivariant Serre Spectral Sequence_, Proceedings of the American Mathematical Society Vol. 118, No. 1 (May, 1993), pp. 263-278 ([JSTOR](http://www.jstor.org/stable/2160037))

and for genuine equivariant cohomology, i.e. for [[RO(G)-grading|RO(G)]]-graded [cohomology with coefficients in a Mackey functor](Mackey+functor#Cohomology):

* {#Kronholm10} [[William Kronholm]], _The $RO(G)$-graded Serre spectral sequence_, Homology Homotopy Appl. Volume 12, Number 1 (2010), 75-92. ([pdf](http://www.swarthmore.edu/NatSci/wkronho1/serre.pdf), [Euclid](https://projecteuclid.org/euclid.hha/1296223823))

See also

* [[Megan Shulman]], _Equivariant Spectral Sequences for Local Coefficients_ ([arXiv:1005.0379](http://arxiv.org/abs/1005.0379))



[[!redirects Serre spectral sequences]]

[[!redirects Leray-Serre spectral sequence]]
[[!redirects Leray-Serre spectral sequences]]