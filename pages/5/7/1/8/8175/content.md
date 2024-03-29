+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
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

The _Atiyah-Hirzebruch spectral sequence_ (AHSS) is a type of [[spectral sequence]] that generalizes the [[Serre spectral sequence]] from [[ordinary cohomology]] $H^\bullet$ to any [[generalized (Eilenberg-Steenrod) cohomology]] theory $E^\bullet$.

For any ([[finite homotopy type|finite]]) [[homotopy fiber sequence]]

$$
  \array{
    F &\longrightarrow& P
    \\
    && \downarrow
    \\
    && X
  }
$$

then the corresponding $E$-Atiyah-Hirzebruch spectral sequence has on its second page the [[ordinary cohomology]] of $X$ with [[coefficients]] in the $E$-[[cohomology groups]] of the [[fiber]] and converges to the proper $E$-cohomology of the total space:

$$
  E_2^{p,q} =
  H^p(X,E^q(F))
  \Rightarrow
  E^{\bullet}(P)
  \,.
$$

This is of interest already for $F \simeq \ast$, as then it expresses generalized cohomology in terms of ordinary cohomology with coefficients in the base cohomology ring. 

+-- {: .num_remark #NoteOnTerminology}
###### Remark
**(note on terminology)** 

Often the terminology "Atiyah-Hirzebruch spectral sequence" is taken to refer to only this case with $F = \ast$, while the general case is then referred to as "Serre spectral sequence for generalized cohomology" or similar. In ([Atiyah-Hirzebruch 61,p. 17](#AtiyahHirzebruch61)) the case $F = \ast$ is labeled "Theorem", while the general case, stated right after the theorem, is labeled "2.2 Remark". 

The proof of the theorem that is given is very short, it just says that since topological K-theory satisfies the [exactness axiom](generalized+%28Eilenberg-Steenrod%29+cohomology#ExactnessUnreduced)  of a generalized cohomology theory, it is immediate that the conditions for a spectral sequence stated as Axioms (SP.1)-(SP.5) in ([Cartan-Eilenberg 56, section XV.7](#CartanEilenberg56)) are met. Indeed Example 2 in ([Cartan-Eilenberg 56, section XV.7](#CartanEilenberg56)) observes that the spectral sequence in question exists for $E$  "some fixed [[cohomology theory]]"  because "Axioms (SP.1)-(SP.4) are consequences of usual properties of cohomology groups". 

In view of this, the contribution of ([Atiyah-Hirzebruch 61](#AtiyahHirzebruch61)) would not be so much the observation of what is now called the AHSS, rather than the proof that K-theory satisfies the axioms of a generalized cohomology theory. Indeed, according to ([Adams 74, p. 127-128, 215](#Adams74)), the AHSS was earlier observed by [[George Whitehead]] and "then became a folk-theorem" which was "eventually published by Atiyah and Hirzebruch".

Maybe it should be called the "Cartan-Eilenberg-Whitehead spectral sequence".

=--

There is a generalization to [[equivariant cohomology theory]] ([Davis-Lueck 98, theorem 4.7](#DavisLueck98)).

For [[genuine G-spectrum|genuine G-equivariance]], with [[RO(G)-grading]] for [[representation spheres]] $S^V$, then for $P \to X$ an $F$-fibration of [[topological G-spaces]] and for $A$ any $G$-[[Mackey functor]], the equivariant Serre spectral sequence looks like ([Kronholm 10, theorem 3.1](#Kronholm10)):

$$
  E_2^{p,q} = H^p(X, H^{V+q}(F,A)) \,\Rightarrow\, H^{V+p+q}(P,A)
  \,,
$$

where on the left in the $E_2$-page we have [[ordinary cohomology]] with [[coefficients]] in the genuine equivariant cohomology groups of the fiber.


## Construction
 {#Construction}

### Statement
 {#Statement}

+-- {: .num_prop}
###### Proposition


Let $A^\bullet$ be a an [additive](#UnreducedAdditivity)  unreduced  [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology functor]]  ([def.](Introduction+to+Stable+homotopy+theory+--+S#ReducedGeneralizedCohomologyHomotopyHomotopicalFunctor)). Let $B$ be a [[CW-complex]] and let $X \stackrel{\pi}{\to} B$ be a [[Serre fibration]], such that all its [[fibers]] are [[weakly contractible topological space|weakly contractible]] or such that $B$ is [[simply connected topological space|simply connected]]. In either case all [[fibers]] are identified with a typical fiber $F$ up to [[weak homotopy equivalence]] by connectedness ([this example](Introduction+to+Stable+homotopy+theory+--+P#FibersOfSerreFibrations)), and well-defined up to unique iso in the homotopy category by simply-connectedness: 

$$
  \array{
    F &\longrightarrow& X
    \\
    && 
    \Big\downarrow\mathrlap{{}^{\in Fib_{cl}}}
    \\
    && B
  }
  \,.
$$

If at least one of the following two conditions is met

* $B$ is [[finite number|finite]]-dimensional as a [[CW-complex]];

* $A^\bullet(F)$ is bounded below in degree and the sequences $\cdots \to A^p(X_{n+1}) \to A^p(X_n) \to \cdots$ satisfy the [[Mittag-Leffler condition]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#MittagLefflerCondition)) for all $p$;

then there is a cohomology [[spectral sequence]], ([def.](Introduction+to+Stable+homotopy+theory+--+S#CohomologySpectralSequence)), whose $E_2$-page is the [[ordinary cohomology]] $H^\bullet(B,A^\bullet(F))$ of $B$ with [[coefficients]] in the $A$-[[cohomology groups]] $A^\bullet(F)$ of the fiber, and which converges to the $A$-cohomology groups of the total space

$$
  E_2^{p,q} 
    = 
  H^p(B, A^q(F)) 
   \;
    \Rightarrow 
   \;
  A^\bullet(X)
$$ 

with respect to the filtering given by

$$
  F^p A^\bullet(X) 
   \coloneqq 
  ker\left(
    A^\bullet(X) 
      \to 
    A^\bullet(X_{p-1})
  \right)
  \,,
$$

where $X_{p} \coloneqq \pi^{-1}(B_{p})$ is the fiber over the $p$th stage of the [[CW-complex]] $B = \underset{\longleftarrow}{\lim}_n B_n$.

Generally, without assumptions on the connectivity of $B$, there is a spectral sequence of this form with ordinary cohomology with coefficients in $A^\bullet(F)$ replaced by ordinary cohomology with [[local coefficients]] $(b \mapsto A^\bullet(F_b))$.

=--

### Construction by filtering the base space
 {#ConstructionByFilteringTheBaseSpace}

The [following proof](#ProofOfAHSS) is the standard and original argument due to ([Atiyah-Hirzebruch 61, p. 17](#AtiyahHirzebruch61)).  


+-- {: .proof #ProofOfAHSS}
###### Proof

The [exactness axiom](#ExactnessUnreduced) for $A$ gives an [[exact couple]], ([def.](Introduction+to+Stable+homotopy+theory+--+S#ExactCoupleAndDerivedExactCouple)), of the form

$$
  \array{
    \underset{s,t}{\prod} A^{s+t}(X_{s})
    &&
      \stackrel{}{\longrightarrow} 
    &&
    \underset{s,t}{\prod} A^{s+t}(X_{s})
    \\
    & \nwarrow && \swarrow
    \\
    && \underset{s,t}{\prod} A^{s+t}(X_{s}, X_{s-1})
  }
  \;\;\;\;\;\;\;
  \left(
      \array{
        A^{s+t}(X_s) & \longrightarrow & A^{s+t}(X_{s-1})
        \\
        \uparrow && \downarrow_{\mathrlap{\delta}}
        \\
        A^{s+t}(X_s, X_{s-1}) && A^{s+t+1}(X_{s}, X_{s-1})
      }
  \right)
  \,,
$$

where we take $X_{\gg 1} = X$ and $X_{\lt 0} = \emptyset$. 

In order to determine the $E_2$-page, we analyze the $E_1$-page: By definition

$$
  E_1^{s,t}
   =
  A^{s+t}(X_s, X_{s-1})
$$


Let $C(s)$ be the set of $s$-dimensional cells of $B$, and notice that for $\sigma \in C(s)$ then 

$$
  (\pi^{-1}(\sigma), \pi^{-1}(\partial \sigma)) \simeq (D^n, S^{n-1}) \times F_\sigma
  \,,
$$

where $F_\sigma$ is [[weak homotopy equivalence|weakly homotopy equivalent]] to $F$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#FibersOfSerreFibrations)).
 
This implies that 

$$
  \begin{aligned}
    E_1^{s,t}
    & \coloneqq
    A^{s+t}(X_s, X_{s-1})
    \\
    & \simeq \tilde A^{s+t}(X_s/X_{s-1})
    \\
    & \simeq \tilde A^{s+t}(\underset{\sigma \in C(n)}{\vee} S^s \wedge F_+)
    \\
    & \simeq \underset{\sigma \in C(s)}{\textstyle{\prod}} \tilde A^{s+t}(S^s \wedge F_+)
    \\
    & \simeq \underset{\sigma \in C(s)}{\textstyle{\prod}} \tilde A^t(F_+)
    \\
    & \simeq \underset{\sigma \in C(s)}{\textstyle{\prod}} A^t(F)
    \\
    & \simeq C^s_{cell}(B,A^t(F))
  \end{aligned}
  \,,
$$

where we used the relation to [[reduced cohomology]] $\tilde A$, ([prop.](Introduction+to+Stable+homotopy+theory+--+S#ReducedToUnreducedGeneralizedCohomology)) together with ([lemma](Introduction+to+Stable+homotopy+theory+--+S#EvaluationOfCohomologyTheoryOnGoodPairIsEvaluationOnQuotient)), 
then the [wedge axiom](Introduction+to+Stable+homotopy+theory+--+S#WedgeAxiom) and the [suspension isomorphism](Introduction+to+Stable+homotopy+theory+--+S#SuspensionIsomorphismForReducedGeneralizedCohomology) of the latter. 

The last group $C^s_{cell}(B,A^t(F))$ appearing in this sequence of isomorphisms is that of [[cellular cohomology|cellular cochains]] ([def.](Introduction+to+Stable+homotopy+theory+--+I#CellularChainComplex)) of degree $s$ on $B$ with [[coefficients]] in the group $A^t(F)$. 

Since [[cellular cohomology]] of a [[CW-complex]] agrees with its [[singular cohomology]] ([thm.](Introduction+to+Stable+homotopy+theory+--+I#CelluarEquivalentToSingularFromSpectralSequence)), hence with its [[ordinary cohomology]], to conclude that the $E_2$-page is as claimed, it is now sufficient to show that the differential $d_1$ coincides with the differential in the [[cellular cochain complex]] ([def.](Introduction+to+Stable+homotopy+theory+--+I#CellularChainComplex)). 

We discuss this now for $\pi = id$, hence $X = B$ and $F = \ast$. (The general case works the same, just with various factors of $F$ replacing the point.)
 
Consider the following diagram, which [[commuting diagram|commutes]] due to the [[natural transformation|naturality]] of the [connecting homomorphism](#ConnectingHomomorphismOfUnreducedCohomology) $\delta$ of $A^\bullet$:

$$
  \array{
    \partial^\ast
     \colon
    & C^{s-1}_{cell}(X,A^t(\ast))
      & =&  \underset{i \in I_{s-1}}{\prod} A^t(\ast)
      && \longrightarrow &&
    \underset{i \in I_s}{\prod} A^t(\ast)
    & = & 
    C_{cell}^{s}(X,A^t(\ast))
    \\
    && & {}^{\mathllap{\simeq}}\downarrow && && \downarrow^{\mathrlap{\simeq}}
    \\
    && & \underset{i \in I_{s-1}}{\prod} \tilde A^{s+t-1}(S^{s-1}) 
      && &&
    \underset{i \in I_s}{\prod} \tilde A^{s+t}(S^{s}) 
    \\
    && & {}^{\mathllap{\simeq}}\downarrow && && \downarrow^{\mathrlap{\simeq}}
    \\
    && d_1 \colon &
    A^{s+t-1}(X_{s-1}, X_{s-2})
      &\overset{}{\longrightarrow}&
    A^{s+t-1}(X_{s-1})
      &\overset{\delta}{\longrightarrow}&
    A^{s+t}(X_s, X_{s-1})
    \\
    && & 
    \downarrow && \downarrow && \downarrow
    \\
    && & 
    A^{s+t-1}(S^{s-1}, \emptyset)
      &\overset{}{\longrightarrow}&
    A^{s+t-1}(S^{s-1})
      &\overset{\delta}{\longrightarrow}&
    A^{s+t}(D^s , S^{s-1})
  }
  \,.
$$

Here the bottom vertical morphisms are those induced from any chosen cell inclusion $(D^s , S^{s-1}) \hookrightarrow (X_s, X_{s-1})$.

The differential $d_1$ in the spectral sequence is the middle horizontal composite. From this the vertical isomorphisms give the top horizontal map. But the bottom horizontal map identifies this top horizontal morphism componentwise with the restriction to the boundary of cells. Hence the top horizontal morphism is indeed the coboundary operator $\partial^\ast$ for the [[cellular cohomology]] of $X$ with coefficients in $A^\bullet(\ast)$ ([def.](Introduction+to+Stable+homotopy+theory+--+I#CellularChainComplex)). This cellular cohomology coincides with [[singular cohomology]] of the [[CW-complex]] $X$ ([thm.](https://ncatlab.org/nlab/show/Introduction+to+Stable+homotopy+theory+--+I#CelluarEquivalentToSingularFromSpectralSequence)), hence computes the [[ordinary cohomology]] of $X$.

Now to see the convergence. If $B$ is finite dimensional then the convergence condition as stated in [this prop.](Introduction+to+Stable+homotopy+theory+--+S#CohomologicalSpectralSequenceOfAnExactCouple) is met.  Alternatively, if $A^\bullet(F)$ is bounded below in degree, then by the above analysis the $E_1$-page has a horizontal line below which it vanishes. Accordingly the same is then true for all higher pages, by each of them being the cohomology of the previous page. Since the differentials go right and down, eventually they pass beneath this vanishing line and become 0. This is again the condition needed in the proof of [this prop.](Introduction+to+Stable+homotopy+theory+--+S#CohomologicalSpectralSequenceOfAnExactCouple) to obtain convergence. 

By that proposition the convergence is to the [[inverse limit]]

$$
  \underset{\longleftarrow}{\lim}
  \left(
    \cdots \stackrel{}{\to} A^\bullet(X_{s+1}) \longrightarrow A^\bullet(X_{s})
    \to \cdots
  \right)
  \,.
$$

If $X$ is finite dimensional or more generally if the sequences that this limit is over satisfy the [[Mittag-Leffler condition]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#MittagLefflerCondition)), then this limit is $A^\bullet(X)$, by [this prop.](Introduction+to+Stable+homotopy+theory+--+S#Lim1VanihesUnderMittagLeffler).


=--

### Construction by filtering the coefficient spectrum
 {#ConstructionByFilteringTheCoefficientSpectrum}

One also gets the Atiyah-Hirzebruch spectral sequence, up to isomorphism, by instead using the filtering given by the [[Postnikov tower]] of an [[Omega-spectrum]] [[Brown representability theorem|representing]] the given generalized cohomology theory.

This is due to ([Maunder 63, theorem 3.3](#Maunder63))

This alternative construction should be the one that is discussed in ([Shulman 13](#Shulman13)) from the perspective of [[homotopy type theory]].

[[!include Lurie spectral sequences -- table]]


## Properties

### Multiplicative structure

for $E$ a [[ring spectrum]], then the AHSS is multiplicative...

([MO discussion](http://mathoverflow.net/q/225579/381))

### Kronecker pairing

+-- {: .num_prop #KroneckerPairingOnAHSS}
###### Proposition

For $E$ a [[ring spectrum]] and $X$ a [[CW complex]] of finite [[dimension]], then the [[Kronecker pairing]] $\langle -,-\rangle \colon E^\bullet(X)\otimes E_\bullet(X)\to \pi_\bullet(E)$ passes to a page-wise pairing of the corresponding Atiyah-Hirzebruch spectral sequences for $E$-cohomology/homology

$$
  \langle-,-\rangle_r
  \;\colon\;
  \mathcal{E}_r^{n,-s}
  \otimes
  \mathcal{E}^r_{n,t}
  \longrightarrow
  \pi_{s+t}(E)
$$

such that

1. on the $\mathcal{E}_2$-page this restricts to the Kronecker pairing for [[ordinary cohomology]]/[[ordinary homology]] with [[coefficients]] in $\pi_\bullet(E)$;

1. the [[differentials]] act as [[derivations]] 

   $$
     \langle d_r(-),-\rangle = \langle -, d^r(-)\rangle
     \,,
   $$

1. The pairing on the $\mathcal{E}_\infty$-page is compatible with the Kronecker pairing. 

=--

([Kochman 96, prop. 4.2.10](#Kochman96))


## Examples and Applications

### To complex oriented cohomology theory

...([Adams 74](#Adams74))....

### For topological K-theory
 {#ForKTheory}

For $E = $ [[KU]], hence for [[topological K-theory]], the differential $d_3$ of the Atiyah-Hirzebruch spectral sequence with $F = \ast$ is given by a [[Steenrod square]] operation

$$
  d_3 = Sq^3
$$

([Atiyah-Hirzebruch 61](#AtiyahHirzebruch61)).

For [[twisted K-theory]] this picks up in addition the [[cup product]] with the 3-class $H$ of the twist:

$$
  d_3 = Sq^3 + H \cup(-)
$$

([Rosenberg 82](#Rosenberg82), [Atiyah-Segal 05 (4.1)](#AtiyahSegal05)). The higher differentials $d_5$ and $d_7$ here are given by higher [[Massey products]] with the twisting class ([Atiyah-Segal 05 sections 5-7](#AtiyahSegal05)).


### D-brane charges in string theory
 {#ApplicationDBraneChargesInStringTheory}

In [[string theory]] [[D-brane charges]] are classes in $E = KU$-cohomology, i.e. in [[K-theory]]. The second page of of the corresponding Atiyah-Hirzebruch spectral sequence (see [above](#ForKTheory)) for $F = \ast$ hence expresses ordinary cohomology in all even or all odd degrees, and being in the kernel of all the differentials is hence the constraint on such ordinary cohomology data to lift to genuine K-theory classes, hence to genuine D-brane charges. In this way the Atiyah-Hirzebruch spectral sequences is used in ([Maldacena-Moore-Seiberg 01](#MaldacenaMooreSeiberg01), [Evslin-Sati 06](#EvslinSati06))



## References

### General

The statement of the existence of the spectral sequence first appears in print (with $E = $ [[topological K-theory]]) in

* {#AtiyahHirzebruch61} [[M. F. Atiyah]], [[F. Hirzebruch]], _Vector bundles and homogeneous spaces_, 1961, Proc. Sympos. Pure Math., Vol. III pp. 7&#8211;38 American Mathematical Society, Providence, R.I. ([web](http://hirzebruch.mpim-bonn.mpg.de/87/), <a href="https://doi.org/10.1142/9789814401319_0008">doi:10.1142/9789814401319_0008</a>, [MR 0139181](http://www.ams.org/mathscinet-getitem?mr=0139181))

but the proof given consists essentially in pointing to section XV.7 ("a more general setting in which the theory of spectral sequences may be developed") of

* {#CartanEilenberg56} [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_, Princeton Univ. Press (1956)

This is by filtering over the stages of the base space CW-complex. That one gets an isomorphic spectral sequence by instead filtering over the [[Postnikov tower]] of any [[Omega-spectrum]] [[Brown representability theorem|representing]] the given [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] theory is due to

* {#Maunder63} [[C. R. F. Maunder]], *The spectral sequence of an extraordinary cohomology theory*, Mathematical Proceedings of the Cambridge Philosophical Society **59** 3 (1963) 567- 574 $[$[doi:10.1017/S0305004100037245](https://doi.org/10.1017/S0305004100037245)$]$
 
Early lecture notes:

* {#Adams74} [[Frank Adams]], part III section 7 of _[[Stable homotopy and generalised homology]]_, 1974

where the idea is attributed to [[George Whitehead]]:

> the Atiyah-Hirzebruch spectral sequence, which was really invented by G. W. Whitehead but not published by him ([Adams 74, p. 127-128](#Adams74))

> These spectral sequences were probably first invented by G. W. Whitehead, but he got them just after he wrote the paper $[$Whitehead 56 'Homotopy groups of joins and unions'$]$ in which they ought to have appeared. They then became a folk-theorem and were eventually published by Atiyah and Hirzebruch ([Adams 74, p. 215](#Adams74))

A more detailed account of the proof is in 

* {#Kochman96} [[Stanley Kochman]], theorem 4.2.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

Further discussion of the case of [[twisted K-theory]]:

* {#Rosenberg82} [[Jonathan Rosenberg]], _Homological Invariants of Extensions of $C^\ast$-algebras_, Proc. Symp. Pure Math 38 (1982) 35.

* {#AtiyahSegal05} [[Michael Atiyah]], [[Graeme Segal]], _Twisted K-theory and cohomology_, Nankai Tracts Math. 11, World Sci. Publ., Hackensack, NJ, pp. 5&#8211;43,  ([arXiv:math/0510674](http://arxiv.org/abs/math/0510674))

* [[Dale Husemöller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin  Schottenloher]], Section 21 of: _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Springer Lecture Notes in Physics __726__, 2008, ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726.pdf), [doi:10.1007/978-3-540-74956-1](https://link.springer.com/book/10.1007/978-3-540-74956-1))

An analogous spectral sequence for higher [[twisted de Rham cohomology]] is discussed in [Li, Liu & Wang 2009](twisted+de+Rham+cohomology#LiLiuWang09).

A discussion of the $E$-AHSS as the spectral sequence of a tower induced by forming [[mapping spectra]] $[X,-]$ into the [[Postnikov tower]] is due to 

* {#Shulman13} [[Mike Shulman]], _[[homotopytypetheory:spectral sequences]]_ (2013)

### Equivariant version
 {#EquivariantVersion}

Discussion of the AHSS in [[Bredon cohomology|Bredon]] [[equivariant stable homotopy theory]]/[[equivariant cohomology]] includes

* {#DavisLueck98} [[James Davis]], [[Wolfgang Lueck]], _Spaces over a category and assembly maps in isomorphism conjectures in K- and L-theory_, K-Theory 15: 201&#8211;252, 1998 ([pdf](http://www.indiana.edu/~jfdavis/papers/assembly.pdf), [K-Theory archive](http://www.math.uiuc.edu/K-theory/0131/))

Discussion in genuine equivariant cohomology, i.e. including [[RO(G)-grading]], is in

* {#Kronholm10} [[William Kronholm]], _The $RO(G)$-graded Serre spectral sequence_, Homology Homotopy Appl. Volume 12, Number 1 (2010), 75-92. ([pdf](http://www.swarthmore.edu/NatSci/wkronho1/serre.pdf), [Euclid](https://projecteuclid.org/euclid.hha/1296223823))



### Examples

Application for the case of [[K-theory]] to [[D-brane charges]] in [[string theory]] is discussed in

* {#MaldacenaMooreSeiberg01} [[Juan Maldacena]], [[Gregory Moore]], [[Nathan Seiberg]], _D-Brane Instantons and K-Theory Charges_, JHEP 0111:062,2001 ([arXiv:hep-th/0108100](http://arxiv.org/abs/hep-th/0108100))

* {#EvslinSati06} [[Jarah Evslin]], [[Hisham Sati]], _Can D-Branes Wrap Nonrepresentable Cycles?_, JHEP0610:050,2006 ([arXiv:hep-th/0607045](http://arxiv.org/abs/hep-th/0607045))

and detailed review of this is in 

* [[Fabio Ruffino]], _Topics on topology and superstring theory_ ([arXiv:0910.4524](http://arxiv.org/abs/0910.4524))

Discussion for the $\mathbb{Z}/2$-equivariant [[KR cohomology theory]] (relevant for D-branes in [[orientifolds]]) includes

* [[Daniel Dugger]], _An Atiyah-Hirzebruch spectral sequence for KR-theory_ ([arXiv:math/0304099](http://arxiv.org/abs/math/0304099)

Discussion for the case of [[Morava K-theory]] and [[Morava E-theory]] with comments on application to charges of [[M-branes]] is in 

* {#SatiWesterland11} [[Hisham Sati]], [[Craig Westerland]], _Twisted Morava K-theory and E-theory_ ([arXiv:1109.3867](http://arxiv.org/abs/1109.3867))

Application to [[motivic homotopy theory|motivic]] [[cobordism cohomology theory]] is discussed in

* Nobuaki Yagita, _Applications of the Atiyah-Hirzebruch spectral sequences for motivic cobordisms_ ([pdf](http://www.math.uiuc.edu/K-theory/0627/ah.pdf))

Application to the [[K-theory classification of topological phases of matter]]:

* [[Ken Shiozaki]], [[Masatoshi Sato]], [[Kiyonori Gomi]], *Atiyah-Hirzebruch Spectral Sequence in Band Topology: General Formalism and Topological Invariants for 230 Space Groups*, Phys. Rev. B **106** (2022) 165103 &lbrack;[arXiv:1802.06694](https://arxiv.org/abs/1802.06694), [doi:10.1103/PhysRevB.106.165103](https://doi.org/10.1103/PhysRevB.106.165103)&rbrack;


[[!redirects Atiyah-Hirzebruch spectral sequence]]
[[!redirects Atiyah-Hirzebruch spectral sequences]]


[[!redirects Atiyah-Hirzeburch spectral sequence]]

