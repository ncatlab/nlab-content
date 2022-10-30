
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


The [[Dold-Kan correspondence]] [[stabilization|stabilizes]]
to identify _unbounded_ [[chain complexes]] with certain [[spectra]].


## Statement

### In terms of abelian combinatorial spectra


The following theorem was established in ([Kan 63, prop. 5.8](#Kan63)) 

+-- {: .num_theorem}
###### Theorem

The [[category of unbounded chain complexes]] is [[equivalence of categories|equivalent]] to the
category of [[combinatorial spectra]] [[internalization|internal]] to [[abelian groups]].

=--

Similarly to the unstable case,
the above categories, when interpreted as ∞-categories,
are also equivalent to the ∞-category of module spectra over
the Eilenberg-MacLane ring spectrum of the integers.
See the section _[stable Dold-Kan correspondence](module+spectrum#StableDoldKanCorrespondence)_
at _[[module spectrum]]_.

### In terms of EM-module spectra
 {#InTermsOfEMModuleSpectra}


+-- {: .num_theorem #StableDoldKan}
###### Theorem

For $R$ any [[ring]] (or [[ringoid]], even) there is a [[Quillen equivalence]] 

$$
  H R ModSpectra \simeq Ch_\bullet(R Mod)
$$

between a model structure on  $H R$-[[module spectra]] over the [[Eilenberg-MacLane spectrum]] $H R$ and the [[model structure on unbounded chain complexes]] of ordinary $R$-[[modules]].

This presents a corresponding [[equivalence of (∞,1)-categories]]. If $R$ is a [[commutative ring]], then this is an equivalence of [[symmetric monoidal (∞,1)-categories]].

=--

This equivalence on the level of [[homotopy categories]] is due to ([Robinson](#Robinson)). The refinement to a [[Quillen equivalence]] is ([SchwedeShipley, theorem 5.1.6](#SchwedeShipley)). See also the discussion at _[[stable model categories]]_. A direct description as an [[equivalence of (∞,1)-categories]] appears as ([[Higher Algebra|Lurie HA, theorem 7.1.2.13]]).

For $R = \mathbb{Q}$ the [[rational numbers]], then theorem \ref{StableDoldKan} may be thought of as a stable analog of classical [[rational homotopy theory]], see at _[[rational stable homotopy theory]]_ for more on this.

More generally:

+-- {: .num_theorem #HRAlgerasAreRdgAlgebras}
###### Theorem

For $R$ a [[commutative ring]], then there is a [[zig-zag]] of [[Quillen equivalences]] between a [[model structure for ring spectra]] over $H R$ and [[model structure on dg-algebras]] over $R$. 

In particular the induced [[total derived functors]] constitute an [[equivalence of categories|equivalence]] of [[homotopy categories]]:


$$
  H R AlgSpec
   \underoverset
     {\underset{\Theta}{\longrightarrow}}
     {\overset{H}{\longleftarrow}}
     {\simeq}
  dgAlg_R
$$

=--

([Shipley 02, theorem 1.1](#Shipley02))


+-- {: .num_theorem #HAModueSpectraAreAdgModules}
###### Theorem

For $A$ any [[dg-algebra]], then there is a [[Quillen equivalence]]

$$
  (H A) ModSpec \simeq_{Quillen} A Mod
$$

between $H A$-[[module spectra]] and [[dg-modules]] over $A$.

Dually, for $E$ an $H \mathbb{Z}$-[[algebra spectrum]], then there is a [[Quillen equivalence]]

$$
  E ModSpec \simeq_{Quillen} (\Theta E) Mod
$$

where $H(-)$ and $\Theta(-)$ are from theorem \ref{HRAlgerasAreRdgAlgebras}.

=--

([Shipley 02, corollary 2.15](#Shipley02))


+-- {: .num_remark}
###### Remark

The [[forgetful functor|forgetful]] [[(∞,1)-functor]] $H R Mod \longrightarrow $ [[Spectra]] preserves [[(∞,1)-limits]], so that (after [[simplicial localization]] $L$) we have an [[(∞,1)-functor]]

$$
  DK
  \;\colon\;
  L_{qi} Ch_\bullet(R) 
    \stackrel{\simeq}{\longrightarrow}
  H R Mod
   \stackrel{}{\longrightarrow}
  Spectra
$$

from the [[(∞,1)-category of chain complexes]] to the [[(∞,1)-category of spectra]] which preseres [[(∞,1)-limits]]. In particular therefore a [[presheaf]] of [[chain complexes]] (as it appears in [[abelian sheaf cohomology]]/[[hypercohomology]]) which satisfies [[descent]] (for some given [[(∞,1)-site]] structure, hence which is an [[(∞,1)-sheaf]]/[[∞-stack]] of chain complexes) maps under the stable Dold-Kan correspondence $DK$ to an [[(∞,1)-sheaf of spectra]].

=--



+-- {: .num_example}
###### Example

For $X$ a [[topological space]] and $R$ a ring, let $C_\bullet(X, R)$ be the standard [[chain complex]] for [[singular homology]] $H_\bullet(X, R)$ of $X$ with coefficients in $R$.

Under the stable Dold-Kan correspondence, prop. \ref{StableDoldKan}, this ought to be identified with the [[smash product]] $(\Sigma^\infty_+ X) \wedge H R$ of the [[suspension spectrum]] of $X$ with the [[Eilenberg-MacLane spectrum]]. Notice that by the general theory of [[generalized homology]] the [[homotopy groups]] of the latter are again singular homology

$$
  \pi_\bullet( (\Sigma^\infty_+ X) \wedge H R) \simeq H_\bullet(X, R)
  \,.
$$

While the correspondence $(\Sigma^\infty_+ X) \wedge H R \sim C_\bullet(X,R)$ under the above equivalence is suggestive, maybe nobody has really checked it in detail. It is sort of stated as true for instance on <a href="http://arxiv.org/PS_cache/arxiv/pdf/0906/0906.5198v1.pdf#page=15">p. 15 </a> of ([BCT](#BCT)).

=--

### Monoidal version in terms of EM-module specta

More in detail we have the following statement.

Let $R \coloneqq H \mathbb{Z}$ be the [[Eilenberg-MacLane spectrum]] for the [[integers]]. 

+-- {: .num_prop}
###### Proposition

There is a zig-zag of [[monoidal Quillen adjunction|lax monoidal]] [[Quillen equivalences]]

$$
  H \mathbb{Z} Mod
    \stackrel{\overset{Z}{\longrightarrow}}{\underset{U}{\leftarrow}}
  Sp^\Sigma(sAb)
    \stackrel{\overset{L}{\leftarrow}}{\underset{\phi^* N}{\longrightarrow}}
  Sp^\Sigma(Ch_+)
   \stackrel{\overset{D}{\longrightarrow}}{\underset{R}{\leftarrow}}
  Ch_\bullet
  \,,
$$

between [[monoidal model categories]] satisfying the [[monoid axiom in a monoidal model category]]:

* the model structure for $H \mathbb{Z}$-[[module spectra]];

* the [[model structure on symmetric spectrum objects]] in [[simplicial abelian group]]s and in [[chain complex]]es;

* and the [[model structure on chain complexes]] (unbounded).

This induces a [[Quillen equivalence]] between the corresponding [[model structures on monoids]] in these [[monoidal category|monoidal categories]], which on the left is the model structure on $H \mathbb{Z}$-algebra spectra and on the right the [[model structure on dg-algebras]]:

$$
  H \mathbb{Z} Alg \simeq dgAlg_\mathbb{Z}
  \,.
$$

=--

This is due to ([Shipley 02](#Shipley02)). The corresponding [[equivalence of (∞,1)-categories]] for $R$ a commutative rings with the intrinsically defined [[(∞,1)-category]] of [[En-algebra|E1-algebra]] objects on the left appears as ([[Higher Algebra|Lurie HA, prop. 7.1.4.6]]).

+-- {: .num_remark}
###### Remark

This is a stable version of the [[monoidal Dold-Kan correspondence]]. See there for more details.

=--

## Related concepts

* [[∞-Dold-Kan correspondence]]

## References

* {#Kan63} [[Daniel Kan]], _Semisimplicial spectra_, Illinois J. Math. Volume 7, Issue 3 (1963), 463-478. ([Euclid](http://projecteuclid.org/euclid.ijm/1255644953))

* {#Robinson} Alan Robinson, _The extraordinary derived category_ , Math. Z. 196 (2) (1987) 231&#8211;238.
 
* {#SchwedeShipley} [[Stefan Schwede]], [[Brooke Shipley]], _Stable model categories are categories of modules_ , Topology 42 (2003), 103-153 ([pdf](http://www.math.uic.edu/~bshipley/classTopFinal.pdf))

* {#Shipley02} [[Brooke Shipley]], _$H \mathbb{Z}$-algebra spectra are differential graded algebras_ , Amer. Jour. of Math. 129 (2007) 351-379. ([arXiv:math/0209215](http://arxiv.org/abs/math/0209215))
 
* {#Jardine91} [[John Frederick Jardine]], _Stable Dold-Kan theory_, section 4.6 of _Generalized &Eacute;tale cohomology theories_, Modern Birkh&#228;user classics (1991)

* {#BCT} [[Andrew Blumberg]], [[Ralph Cohen]], [[Constantin Teleman]], _Open-closed field theories, string topology and Hochschild homology_ ([arXiv:0906.5198](http://arxiv.org/abs/0906.5198))
 
* [[Jacob Lurie]], section 7.1.4 of _[[Higher Algebra]]_

* [[Jacob Lurie]], _[[Deformation Theory]]_ 
 