
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The original theorem by Snaith ([Snaith 79](#Snaith79)) identifies the [[complex K-theory spectrum]] [[KU]] simply as the localization of the [[∞-group ∞-ring]] $\mathbb{S}[B U(1)]$ of the [[circle 2-group]] away from the [[Bott element]] $\beta$:

$$
  KU \simeq \mathbb{S}[B U(1)][\beta^{-1}]
  \,.
$$

Later, further instances of such characterizations of familiar [[E-∞ rings]] have been given:

* in ([Gepner-Snaith 08](#GepnerSnaith08)) the analogous statement for [[algebraic K-theory]] is formulated in terms of [[motivic spectra]];

* in ([Westerland 12](#Westerland12)) the tower of [[Morava E-theories]] (or some [[homotopy fixed point]] [[spectra]] of these) is shown to be localizations of the [[∞-group ∞-rings]] of $B^{n+1} \mathbb{Z}_p$, for all $n \in \mathbb{N}$.

## Statement

### Preliminaries

For $A$ an [[abelian ∞-group]] write $E \coloneqq \mathbb{S}[A] = \Sigma^\infty_+ A$ for its [[∞-group E-∞ ring]].

+-- {: .num_defn}
###### Definition

For $\beta \in \pi_n(E)$ an element of the $n$th stable [[homotopy group]], then _multiplication by $\beta$_ is a homomorphism

$$
  \beta_\ast
  \;\colon\;
  E
  \to
  \Sigma^{-n} E
  \,.
$$

The _localization_ of $E$ at $\beta$ is the [[homotopy colimit]] over the iterated multiplication with $\beta$

$$
  E[\beta^{-1}]
  \coloneqq
  \underset{\to}{\lim}
  \left[
    E \stackrel{\beta_\ast}{\to}
    \Sigma^{-n}E
    \stackrel{\Sigma^{-n} \beta_\ast}{\to}
   \Sigma^{-2n} E
   \to
   \cdots
  \right]
$$

which has the [[universal property]] that $\mu_\beta$ becomes an [[equivalence]] on $E[\beta^{-1}]$.

=--



### For complex topological K-theory
 {#ForComplexTopologicalKTheory}

The original formulation of Snaith's theorem ([Snaith 79, theorem 2.12](#Snaith70), spring) for complex [[topological K-theory]].

#### Preliminaries

Write $(Ho(Top), \times, \ast)$ for the [[classical homotopy category]], regarded as a [[symmetric monoidal category]] under forming [[product spaces]], with [[tensor unit]] the [[point space]].

Write $(Ho(Top^{\ast/}), \wedge , S^0)$ for the homotopy category of [[pointed topological spaces]] with [[tensor product]] the [[smash product]] of pointed spaces and [[tensor unit]] the [[0-sphere]]

Write $(Ho(Spectra), \wedge, \mathbb{S})$ be the [[stable homotopy category]] with its [[symmetric monoidal smash product of spectra]] $\wedge$ whose [[tensor unit]] is the [[sphere spectrum]] $\mathbb{S}$.

For $A,B \in Ho(Spectra)$ two [[spectra]], we write

$$
  [A,B] \coloneqq Hom_{Ho(Spectra)}(A,B) \in Ab
$$

for [[hom-set]] in the [[stable homotopy category]] and write

$$
  [A,B]_\bullet \coloneqq [\Sigma^\bullet A, B]
$$

for the corresponding $\mathbb{Z}$-graded group ([this def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)).

There are two pairs of ([[derived functor|derived]]) [[adjoint functors]]

$$
  Ho(Spectra)
    \underoverset
      {\underset{\Omega^\infty}{\longrightarrow}}
      {\overset{\Sigma^\infty}{\longleftarrow}}
      {}
  Ho(Top^{\ast/})
    \underoverset
      {\underset{U}{\longrightarrow}}
      {\overset{(-)_+}{\longleftarrow}}
      {\bot}
  Ho(Top)
$$

which are [[strong monoidal functors]] (by [this example](pointed+object#WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces) and [this prop](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsIndeedStabilizationOfClassicalHomotopyCategory)). The left adjoint composite

$$
  \mathbb{S}[-]
    \;\colon
  \Sigma^\infty((-)_+)
$$

hence takes [[H-spaces]] and in particular [[H-groups]] $G$ to [[ring spectra]].

More in detail, an [[H-space]] structure is a $G \in Ho(Top)$ equipped with morphisms

$\mu \;\colon\; G \times G \longrightarrow G$

$e \;\colon\; \ast \longrightarrow G$

satisfying [[associativity]] and [[unitality]] in $Ho(Spectra)$, and the corresponding ring spectrum has product

$$

  \left(\Sigma^\infty(G_+)\right)
    \wedge
  \left( \Sigma^\infty G_+\right)
   \;\simeq\;
  \Sigma^\infty( (G \times G)_+ )
    \overset{\Sigma^\infty (e_+)}{\longrightarrow}
  \Sigma^\infty (G_+)
$$

and unit

$$
  \mathbb{S}
    \simeq
  \Sigma^\infty( \ast_+)
    \overset{ \Sigma^\infty(e_+) }{\longrightarrow}
  \Sigma^\infty(G_+)
$$


We call

$$
  \mathbb{S}[G] \coloneqq \Sigma^\infty(G_+)
$$

equipped with this monoid structure
the _[[H-group ring spectrum]]_ of $G$. See [there](∞-group+∞-ring#HGroupRingSpectra) for more.


#### The ring spectrum of the circle 2-group

One such [[H-group]] is the _[[circle 2-group]]_, hence (the [[homotopy type]] of) the [[classifying space]] $B U(1)$ for [[complex line bundles]], equivalently the [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$, canonically presented by the [[complex projective space]] $\mathbb{C}P^\infty$


$$
  K(\mathbb{Z},2) \simeq B U(1) \simeq \mathbb{C}P^\infty
  \;\in\;
  Ho(Spaces)
  \,.
$$

This being the [[classifying space]] for [[complex line bundles]], it becomes an [[H-group]] via the map

$$
  B U(1) \times B U(1) \longrightarrow B U(1)
$$

which classifies the [[tensor product of vector bundles|tensor product of line bundles]], with inverses given by the map

$$
  B U(1) \longrightarrow B U(1)
$$

which form [[dual vector bundle|dual line bundles]].

Hence its [[H-group ring spectrum]] is

$$
  \mathbb{S}[B U(1)]
   \;=\;
  \Sigma^\infty( B U(1)_+ )
  \,.
$$

Therefore for $X \in Ho(Top^{\ast/})$ a [[pointed topological space]], then

$$
  [\Sigma^\infty X,\Sigma^\infty(G_+)]_\bullet
$$

is a graded ring, with the product of elements

$$
  \left(
    \Sigma^{n_i} \Sigma^\infty X
     \overset{\alpha_i}{\longrightarrow}
   \Sigma^\infty(G_+)
  \right)
  \;\in\;
  [\Sigma^\infty X, \Sigma^\infty(G_+)]_{n_i}
$$

for $i \in \{1,2\}$ given by

$$
  \Sigma^{n_1 + n_2}
  \Sigma^\infty X
    \overset{\Sigma^{n_1+ n_2} \Sigma^\infty \Delta_X}{\longrightarrow}
  \Sigma^{n_1 + n_2}
  \Sigma^\infty (X \wedge X)
   \simeq
  \left(
    \Sigma^{n_1} \Sigma^\infty X
  \right)
    \wedge
  \left(
     \Sigma^{n_2} \Sigma^\infty X
  \right)
    \overset{ \alpha_1 \wedge \alpha_2 }{\longrightarrow}
  \left(
    \Sigma^\infty (G_+)
  \right)
    \wedge
  \left(
    \Sigma^\infty (G_+)
  \right)
    \overset{\Sigma^\infty (\mu_+)}{\longrightarrow}
  \Sigma^\infty (G_+)
  \,.
$$

Here the isomorphism on the left is the combination of the strong monoidalness of $\Sigma^\infty$ with the respect of suspension $\Sigma$ for the smash product of spectra (the [[tensor triangulated category]] structure on $Ho(Spectra)$, [this prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)).


Observe that we have a splitting

$$
  \Sigma^\infty(B U(1)_+)
   \;\simeq\;
  \left(
    \Sigma^\infty (B U(1))
  \right)
    \;\oplus\;
  \mathbb{S}
$$

(by [this remark](∞-group+∞-ring#HGroupRingSpectrumSplitsAsDirectSumWithSphereSpectrum)) and hence a canonical morphism

$$
  \Sigma^\infty (B U(1))
    \longrightarrow
  \Sigma^\infty (B U(1)_+)
  \,.
$$

Via this splitting, the morphism in $Ho(Top^{\ast/})$

$$
  h \colon S^2 \longrightarrow B U(1)
$$

in $[S^2, B U(1)] \simeq \pi_2(B U(1)) \simeq \mathbb{Z}$ which classifies the [[basic complex line bundle on the 2-sphere]] and represents $1 \in \mathbb{Z}$, induces a morphism

$$
  \beta
    \;\colon\;
  \Sigma^2 \mathbb{S}
    \simeq
  \Sigma^\infty S^2
    \overset{ \Sigma^\infty( h ) }{\longrightarrow}
  \Sigma^\infty B U(1)
    \overset{}{\longrightarrow}
  \Sigma^\infty (B U(1)_+)
$$

hence an element in $[\mathbb{S}, \Sigma^\infty(B U(1)_+)]_2$.


#### The map to the K-theory spectrum
 {#MapToKTheorySpacetum}


The [[spectrum]] [[KU]] which [[Brown representability theorem|represents]]  complex [[topological K-theory]]
has in degree 0 the the [[product space]]

$$
  \Omega^\infty KU \simeq B U \times \mathbb{Z} \in Ho(Top^{\ast/})
$$

of the stable [[classifying space]] $B U$ for [[complex vector bundles]] and the [[integers]]. The base point is $(\ast, 0)$.

The [[projection]]

$$
  B U \times \mathbb{Z} \longrightarrow \mathbb{Z}
$$

classifies the virtual [[rank of a vector bundle|rank]] of [[virtual vector bundle]].

Hence the inclusion of classifying spaces

$$
  B U \simeq B U \times \{0\} \hookrightarrow  B U \times \mathbb{Z}
$$

classifies the inclusion $\tilde K_{\mathbb{C}}(-) \hookrightarrow K_{\mathbb{C}}(-)$ of [[reduced K-theory]].


There is a canonical morphism

$$
  \Sigma^\infty(B U(1)_+)
    \overset{\Phi}{\longrightarrow}
  K U
$$

in $Ho(Spectra)$, being the $(\Sigma^\infty \dashv \Omega^\infty)$-[[adjunct]] of

$$
  B U(1)_+ \longrightarrow B U \times \mathbb{Z} \simeq \Omega^\infty K U
$$

in $Ho(Top^{\ast/})$, which in turn is the $((-)_+ \dashv U)$-[[adjunct]] of the canonical

$$
  \mathcal{O}(1) \;\colon\; B U(1) \longrightarrow B U \simeq B U \times \{1\} \hookrightarrow B U \times \mathbb{Z}
$$

in $Ho(Top)$.

Since the [[formal group law]] for K-theory says that $\mu^\ast ( \mathcal{O}(1) ) \simeq pr_1^\ast (\mathcal{O}(1)) \otimes pr_2^\ast(\mathcal{O}(2))$ $\Phi$ is  a homomoprhism of ring spectra.

Under the above splitting, the morphism $\Phi$ decomposes as

$$
  \Phi
    \;\colon\;
  \Sigma^\infty (B U(1)_+)
    \simeq
  \Sigma^\infty B U(1)  \oplus \mathbb{S}
    \overset{ ( \tilde i , e_{KU})  }{\longrightarrow}
  KU
$$

Since, by the above, morphisms $\Sigma^\infty B U(1) \longrightarrow K U$ in $Ho(Spectra)$,
hence equivalently morphisms $B U(1) \longrightarrow B U \times \mathbb{Z}$ in $Ho(Top^{\ast/})$,
hence equivalently morphisms $B U(1) \to B U$ in $Ho(Top)$  correspond to the reduced K-theory of
$B U(1)$, and since morphisms $\mathbb{S} \to KU$ in $Ho(Spectra)$, hence equivalently morphism $\ast \to B U \times \mathbb{Z}$
in $Ho(Top)$ correspond to the K-theory of the point, and since over (colimits of) [[compact topological spaces]]
K-theory splits as $K(X) \simeq \tilde K(X) \oplus K(\ast)$ via $[E]- n \mapsto ([E] - rk(E)) + ( rk(E) - n )$
([this prop](topological+K-theory#KGrupDirectSummandReducedKGroup)) it follows that

1. $\tilde i$ takes the canonical line bundle $\mathcal{O}(1)$ on $B U(1)$ to its image $\mathcal{O}(1)-1$ in reduced K-theory

   $$
     B U(1) \overset{\mathcal{O}(1) \mapsto (\mathcal{O}(1)-1)}{\longrightarrow} B U \simeq B U \times \{0\} \hookrightarrow B U \times \mathbb{Z} \simeq \Omega^\infty K U
   $$

1. $e_{K U}$ is adjunct to $\ast \simeq (\ast,1) \hookrightarrow B U \times \mathbb{Z}$ ( is the ring spectrum unit of $K U$).

Now observe that $\Phi$ takes multiplication by $\beta$ to multiplication with the [[Bott element]] $(h-1)$:

This is because multiplication by $\beta$ is the outer right boundary of the following diagram

$$
  \array{
     \Sigma^\infty S^2 \wedge \Sigma^n \Sigma^\infty X
     \\
     {}^{\mathllap{ (h \oplus 0) \wedge id }}\downarrow
     \\
     \left(\Sigma^\infty( B U(1) ) \oplus \mathbb{S}\right) \wedge \Sigma^n \Sigma^\infty X
     \\
     {}^{\mathllap{id \wedge \alpha}}\downarrow
     \\
     \Sigma^\infty(B U(1)_+) \wedge \Sigma^n \Sigma^\infty( B U(1)_+ )
       &\overset{\Sigma^n\Sigma^\infty (\mu_+)}{\longrightarrow}&
     \Sigma^n \Sigma^\infty (B U(1)_+)
     \\
     \downarrow && \downarrow
     \\
     K U \wedge \Sigma^n K U &\longrightarrow & \Sigma^n K U
  }
$$

and since the bottom square commutes (since tensor product of line bundles corresponds to their product in K-theory)
this is equivalent to the left and bottom boundary, which, by the above discussion, is multiplication with the
[[Bott element]] $(h-1)$.

Since the Bott element is invertible in $K U$, this means for all $X \in Ho(Top^\ast/)$ that the morphism

$$
  [\Sigma^\infty X , \Sigma^\infty ( B (1)_+ ) ]_\bullet
    \overset{\Phi_X \coloneqq \Phi \circ (-)}{\longrightarrow}
  [\Sigma^\infty X, K U]_\bullet
    \simeq
  \tilde K_{\mathbb{C}}^\bullet(X)
$$

extends to the quotient ring

$$
  [\Sigma^\infty X, \Sigma^\infty ( B U(1)_+ )]_{\bullet}[\beta^{-1}]
$$

in which two elements are identified if they differ by multiplication by $\beta$, as above:

$$
  \array{
    [\Sigma^\infty X, \Sigma^\infty( B U(1)_+ )]  &\overset{\Phi}{\longrightarrow}& \tilde K_{\mathbb{C}}^\bullet(X)
    \\
    \downarrow & \nearrow_{\mathrlap{\exists \Phi}}
    \\
    [\Sigma^\infty X, \Sigma^\infty( B U(1)_+ )]_\bullet [\beta^{-1}]
  }
  \,.
$$

#### Isomorphy



+-- {: .num_theorem}
###### Theorem

If $X \in Ho(Top^{\ast/})$ has the homotopy type of a [[finite CW-complex]], then the [[natural transformation]]

$$
  \Phi_X
    \;\colon\;
  [X, \Sigma^\infty ( B U(1)_+ )]_\bullet [\beta^{-1}]
    \longrightarrow
  \tilde K^\bullet(X)
$$

is a [[natural isomorphism]].

=--

([Snaith 81, theorem 2.12](#Snaith81), [Hopkins-Mathew](#HopkinsMathew))

That (before localization) the map is an epimorphism is due to ([Segal 73, prop. 1](#Segal73)), see [this prop.](complex+projective+space#HGroupRingSpectrumSurjectsOntoTopologicalKTheory). The analog of this statement for [[real projective space]] $\mathbb{R}P^\infty \simeq B \mathbb{Z}/2$ instead of [[complex projective space]] $\mathbb{C}P^\infty \simeq B U(1)$ is the [[Kahn-Priddy theorem]].



### For periodic complex cobordism

+-- {: .num_theorem}
###### Theorem

The [[periodic complex cobordism spectrum]] is the [[∞-group ∞-ring]] of the [[classifying space]] for stable [[complex vector bundles]] (the classifying space for [[topological K-theory]]) localized at the [[Bott element]] $\beta$:

   $$
     PMU \simeq (\mathbb{S}[B U])[\beta^{-1}]
     \,.
   $$

=--

([Snaith 81, theorem 2.7](#Snaith81))

### For algebraic K-theory

+-- {: .num_remark}
###### Remark

The analog of this result for the periodic [[algebraic cobordism spectrum]] and [[algebraic K-theory]] as [[motivic spectra]] is discussed in ([GepnerSnaith 08](#GepnerSnaith08)).

=--

### For smooth spectra and differential K-theory

Refinement of the Snaith theorem for [[KU]] to [[smooth spectra]] and to [[differential K-theory]] is in ([Bunke-Nikolaus-V&#246;lkl 13, section 6.3](#BunkeNikolausVoelkl13)). See at _[differential cohomology diagram -- Smooth Snaith K-theory](differential%20cohomology%20diagram#ViaSmoothSnaithTheorem)_.



### Snaith-like theorem for Morava $E$-theories
 {#ForMoravaETheory}

Write $\Gamma_n$ for the [[Honda formal group]]. The [[automorphism group]] $Aut(\Gamma_n)$ induces for each prime $p$ a canonical [[determinant]] morphism

$$
  det \;\colon\; \mathbb{G}_n \longrightarrow \mathbb{Z}_p^\times
$$

from the [[Morava stabilizer group]] $\mathbb{G}_n \coloneqq Gal(\mathbb{F}_{p^n}/\mathbb{F}_p) \ltimes Aut(\Gamma_n)$.

Write

$$
  S \mathbb{G}_n \coloneqq ker(det)
$$

for the [[kernel]]. This naturally [[infinity-action|acts]] on the [[Morava E-theory]] spectrum $E_n$. Write $E^{S\mathbb{G}_n}$ for the corresponding [[homotopy fixed point]] [[spectrum]]. ([Westerland 12, 1.1](#Westerland12)).

Write $L_{K(n)} \mathbb{S}[B^{n+1} \mathbb{Z}_p]$ for the $K(n)$-localization of the [[∞-group ∞-ring]] of the [[n-group|(n+1)-group]] $B^n \mathbb{Z}_p$.

+-- {: .num_theorem}
###### Theorem

There is a [[generalized element]] $\rho_n$ of the [[E-∞ ring]] $L_{K(n)} \mathbb{S}[B^{n+1} \mathbb{Z}_p]$ such that localization at that element yields the [[Morava E-theory]] spectrum $S\mathbb{G}_n$[[homotopy fixed points]]:

$$
  L_{K(n)} \mathbb{S}[B^{n+1} \mathbb{Z}_p] [\rho_n^{-1}]

  \stackrel{\simeq}{\longrightarrow}
  E_n^{S\mathbb{G}_n}
  \,.
$$

=--

([Westerland 12, theorem 1.2](#Westerland12))


## Related concepts

* [[splitting principle]]

* [[algebraic cobordism]]

## References

The theorem is due to

* {#Snaith79} [[Victor Snaith]], _Algebraic Cobordism and K-theory_, Mem. Amer. Math. Soc. no 221 (1979) 

with a simpler proof given in

* {#Snaith81} [[Victor Snaith]], _Localized stable homotopy of some classifying spaces_, Math. Proc. Cambridge Philos. Soc. 89 (1981), no. 2, 325-330. MR 600247 (82g:55006) ([pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/S0305004100058205), [doi:10.1017/S0305004100058205](https://doi.org/10.1017/S0305004100058205))

using results from

* {#Segal73} [[Graeme Segal]], _The stable homotopy of complex of projective space_, The quarterly journal of mathematics (1973) 24 (1): 1-5. ([[Segal72.pdf:file]], [doi:10.1093/qmath/24.1.1]( https://doi.org/10.1093/qmath/24.1.1))


Another proof due to [[Mike Hopkins]] is in

* {#HopkinsMathew} [[Akhil Mathew]] (following [[Mike Hopkins]]), _Snaith's construction of complex K-theory_ ([pdf](http://math.uchicago.edu/~amathew/snaith.pdf), [[MathewSnaithTheorem.pdf:file]])

Refinement to [[smooth spectra]] and [[differential K-theory]] is in

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], section 6.3 of _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

Discussion of the [[E-∞ ring]] structure involved is around theorem 3.1 of

* [[Jacob Lurie]],  _[[A Survey of Elliptic Cohomology]]_

A version for [[motivic spectra]] [[algebraic K-theory]] is discussed in

* [[David Gepner]], [[Victor Snaith]], _On the motivic spectra representing algebraic cobordism and algebraic K-theory_, Documenta Math.  2008 ([arXiv:0712.2817](http://arxiv.org/abs/0712.2817))
 {#GepnerSnaith08}

and for [[motivic cohomology]] in

* [[Markus Spitzweck]], [[Paul Arne Østvær]], _The Bott inverted infinite projective space is homotopy algebraic K-theory_ ([pdf](http://folk.uio.no/paularne/bott.pdf))

Higher [[chromatic homotopy theory|chromatic]] analogs for [[Morava E-theory]] are discussed in

* {#Westerland12} [[Craig Westerland]], _A higher chromatic analogue of the image of J_ ([arXiv:1210.2472](http://arxiv.org/abs/1210.2472))

* {#LindSatiWesterland16} [[John Lind]], [[Hisham Sati]], [[Craig Westerland]], _A higher categorical analogue of topological T-duality for sphere bundles_ ([arXiv:1601.06285](http://arxiv.org/abs/1601.06285))

A unifying [[general abstract]] perspective is discussed in

* {#Arndt17} [[Peter Arndt]], section 3.2 of _Abstract motivic homotopy theory_, thesis 2017 ([web](https://repositorium.ub.uni-osnabrueck.de/handle/urn:nbn:de:gbv:700-2017021015476?mode=full),  [pdf](https://repositorium.ub.uni-osnabrueck.de/bitstream/urn:nbn:de:gbv:700-2017021015476/6/thesis_arndt.pdf), [[ArndtAbstractMotivic.pdf:file]])

   {#Arndth19} exposition: lecture at _[Geometry in Modal HoTT](www.andrew.cmu.edu/user/fwellen/abstracts.html)_, 2019 ([recording I](https://www.youtube.com/watch?v=f0wpcNs8hQo), [recording II](https://www.youtube.com/watch?v=sTl8637a2Zo))



See also at _[[spherical T-duality]]_.

[[!redirects Snaith's theorem]] 