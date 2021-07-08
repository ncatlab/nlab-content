
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
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

Rational stable homotopy theory is the simple special case of [[stable homotopy theory]] under [[rationalization]].

It is a classical fact that the [[rationalization]] of classical [[homotopy theory]] (of [[topological spaces]] or [[simplicial sets]]) -- called _[[rational homotopy theory]]_ -- is considerably more tractable than general [[homotopy theory]], as exhibited by the existence of small concrete [[dg-algebra|dg-algebraic]] models for [[rational homotopy types]]: [[minimal Sullivan algebras]] or equivalently their [[dual]] [[dg-coalgebras]]. A similar statement holds for the rationalization of [[stable homotopy theory]] i.e. the [[homotopy theory]] of [[spectra]] (of [[topological spaces]] or [[simplicial sets]]): rational spectra are equivalent to rational [[chain complexes]], i.e. to [[dg-modules]] over $\mathbb{Q}$. This is a dg-model for _rational stable homotopy theory_ compatible with that of classical rational homotopy theory in that the [[stabilization]] adjunction that connects classical [[homotopy theory]] to [[stable homotopy theory]] is, under these identifications, modeled by the [[forgetful functor]] from dg-(co-)algebras to [[chain complexes]]

$$
  \array{
    & \text{classical homotopy theory}
     &&
    \text{stable homotopy theory}
    \\
    & spaces & \underoverset{\underset{\Sigma^\infty}{\longrightarrow}}{\overset{\Omega^\infty}{\longleftarrow}}{} & spectra
    \\
    & & \text{stabilization}
    \\
    \text{rationally}
    &
    \text{dg(co)algebras}
    &
     \underoverset{\underset{underlying}{\longrightarrow}}{\overset{free}{\longleftarrow}}{}
    &
    \text{chain complexes}
  }
$$

## Rational spectra

+-- {: .num_theorem #RationalStableDoldKanCorrespondence}
###### Theorem


By the [[stable Dold-Kan correspondence]], the ([[stable homotopy theory|stable]]) [[homotopy theory]] of _[[rationalization|rationalized]] [[spectra]]_, namely of $H \mathbb{Q}$-[[module spectra]] is [[equivalence of (infinity,1)-categories|equivalent]] to that of [[chain complexes]] of [[modules]]/[[vector space]] over the [[rational numbers]] 

$$
  H \mathbb{Q} ModSpectra
   \;\simeq\;
  Ch_\bullet(\mathbb{Q})
  \,.
$$

=--

([Schwede-Shipley 03, theorem 5.1.6](#SchwedeShipley03), see also at _[[stable Dold-Kan correspondence]]_).

+-- {: .num_remark}
###### Remark

Observe that $H \mathbb{Q}$-module spectra are just the rational spectra. Since [[rationalization]] of spectra is the [[smashing localization]] $(-)\wedge H \mathbb{Q}$ ([here](rationalization#RationalizationOfSpectra)) every rational spectrum $X \simeq H \mathbb{Q} \wedge X$ carries an $H \mathbb{Q}$-module structure. Conversely, just as a $\mathbb{Q}$-[[module]] structure on an [[abelian group]] is unique if it exists, so an $H \mathbb{Q}$-[[module spectrum]] structure on a [[spectrum]] is essentially unique if it exists, due to the fact that the multiplication map $H \mathbb{Q} \wedge H \mathbb{Q} \to H \mathbb{Q}$ is an [[equivalence in an (infinity,1)-category|equivalence]].

=--

Theorem \ref{RationalStableDoldKanCorrespondence} parallels that of classical [[rational homotopy theory]]: 


+-- {: .num_theorem #ClassicalRationalHomotopyTheory}
###### Theorem

There is an [[equivalence of (infinity,1)-categories|equivalence of homotopy theories]] between the [[homotopy theory]] of [[nilpotent topological space|nilpotent]] [[rational topological spaces]] [[of finite type]] with that of cochain [[dgc-algebras]] over $\mathbb{Q}$ in non-negative degree

$$
  \infty Grpd_{\mathbb{Q}, nil,fin}
    \;\simeq\;
  dgcAlg^{\geq 0}_{\mathbb{Q},nil,fin}
$$

=--

## Rational stabilization
 {#RationalStabilization}


+-- {: .num_prop #RationalStabilizationModel}
###### Proposition

The following composite total [[derived functors]]

$$
  \array{
    \mathrm{Ho}( \mathrm{Spectra}_{\mathbb{Q}, \mathrm{fin}} )
    \\
    \downarrow \simeq \uparrow
    \\
    \mathrm{Ho}( \mathrm{Ch}_{\mathbb{Q},\bullet,\mathrm{fin}} )
     &
      \underoverset
        \underset{\mathbb{R}\mathrm{cn}_2}{\longrightarrow}
        \overset{\mathbb{L} i_2}{\longleftarrow}
        {\bot}
     &
    \mathrm{Ho}( \mathrm{Ch}_{\mathbb{Q}, \gt 1, \mathrm{fin}} )
    \\
    &&
    \downarrow \simeq \uparrow^{(-)^\ast}
    \\
    &&
    \mathrm{Ho}( \mathrm{Ch}^{\gt 1}_{\mathbb{Q}, \mathrm{fin}}   )^{\mathrm{op}}
     &
      \underoverset
       \underset{ (\mathbb{L}\mathrm{Sym}_{/\mathbb{Q}[0]})^{\mathrm{op}} }{\longrightarrow}
       \overset{ (\mathbb{R}( U \circ \mathrm{ker}(\epsilon_{(-)}) ))^{\mathrm{op}} }{\longleftarrow}    
       {\bot}
     &
   \mathrm{Ho}( \mathrm{dgcAlg}^{\gt 0}_{\mathbb{Q}, \mathrm{fin}})_{/\mathbb{Q}[0]} )^{\mathrm{op}}
    \\
   && && \updownarrow \simeq
    \\
    && &&
    \mathrm{Ho}(\mathrm{Top}_{\mathbb{Q}, \gt 1 , \mathrm{fin}})
  }
$$

(where the key part in the middle right, involving $Sym$, is from prop. \ref{dgcAlgChAdjunction}, the left middle part involving connectivity is from prop. \ref{ChainComplexesConnectiveCover}, and the equivalences on the far left and far right are those from theorem \ref{RationalStableDoldKanCorrespondence} and theorem \ref{ClassicalRationalHomotopyTheory}, respectively)

agree with the restriction of the
[[stabilization]] [[adjoint (infinity,1)-functor|infinity-adjunction]]

$$
  Spectra
    \underoverset
      {\underset{\Omega^\infty}{\longrightarrow}}
      {\overset{\Sigma^\infty}{\longleftarrow}}
      {\bot}
  \infty Grpd^{\ast/}
$$

to simply connected rational homotopy types of finite type.

=--

+-- {: .proof}
###### Proof

By the nature of the classical model structure on topological spaces,
every simply connected object of $\mathrm{Ho}(\mathrm{Top}^{\ast/})$ is represented by one that is a [[retract]] of a [[transfinite composition]] of [[pushouts]] of the pointed connected generating cofibrations $S^n \to D^n$, for $n \geq 1$. More abstractly, the [[(∞,1)-category]] of simply connected homotopy types is generated under [[(∞,1)-colimits]] from the [[n-spheres]] of dimension $n \geq 2$. (See the analogous argument used in the [[Brown representability theorem]] [here](Brown%20representability%20theorem#TheClassicalPointedConnectedHomotopyCategoryAsDomainForTheAbstractBrownRepresentabilityTheorem)).

Since $\Sigma^\infty$ is a left adjoint functor it is sufficient to check that the two functors agree on $S^n$ for $n \geq 1$. That they agree on $D^n$ is immediate. We hence need to consider their value on the positive
dimensional $n$-spheres:

Let $n$ be odd. Then the [[minimal Sullivan model]] for $S^n$ is $\mathrm{Sym}( \mathbb{R}[n] )$.
Since every dgc-algebra is fibrant in the projective model structure, the value of
$\mathbb{R}(U \circ \mathrm{ker}(\epsilon_{(-)}))$ on this model is represented by
the value of $U \circ \mathrm{ker}(\epsilon_{(-)})$ on that model, which is the cochain complex
$\mathbb{Q}[n]$, hence equivalently the corresponding chain complex. This is indeed the
rationalization of $\Sigma^\infty S^n$.

Next let $n$ be even with $n \geq 1$. Then the minimal Sullivan model for $S^n$ is
$\mathrm{Sym}( \mathbb{R}[n] \oplus \mathbb{R}[2n-1], d c_{2n-1} = c_{n} \wedge c_n  )$.
The underlying chain complex of the augmentation ideal is spanned by the elements
$c_{n}^{\wedge^k}$  in degree $n k$ and by the elements
$c_{n}^{\wedge^k} \wedge c_{2n-1}$ in degree $nk+2n-1$. The former elements are all closed,
but except for $k = 1$ are all in the image of the latter elements, none of which is closed.
Hence this chain complex is quasi-isomorphic to $\mathbb{R}[n]$. Again, this is indeed
the rationalization of $\Sigma^\infty S^{n}$


=--

## Appendix

Here we collect some background definitions, notations and facts for ease of reference in the main text above.

### Chain complexes

Throughout, let $k$ be a [[field]] of [[characteristic zero]].


+-- {: .num_defn}
###### Definition

Write

1. $\mathrm{Ch}_{k,\bullet}$ for the [[category of chain complexes]] of $k$-[[vector spaces]], i.e. the category of $\mathbb{Z}$-graded $k$-vector spaces $V$ equipped with a linear map $\partial_V : V \to V$ of degree -1 such that $\partial_V \circ \partial_V = 0$ (the [[differential]]);

1. $\mathrm{Ch}_k^\bullet$ for the category of [[cochain complexes]] of $k$-vector spaces, i.e. as before, but with differential $d_V$ of degree +1.

For $V$ a $k$-vector space, and $n \in \mathbb{N}$ we write $V[n]$ for the (co-)chain complex concentrated on
$V$ in degree $k$.

For $n \in \mathbb{Z}$ write
$$
    \mathrm{Ch}_{k, \geq n}
      \overset{i_n}{\hookrightarrow}
    \mathrm{Ch}_{k,\bullet}
$$
$$
    \mathrm{Ch}_k^{\geq n}
      \overset{i^n}{\hookrightarrow}
    \mathrm{Ch}_k^\bullet
$$

for the [[full subcategories]] on the (co-)chain complexes that are concentrated in degrees $\geq n$.

=--

+-- {: .num_prop #ChainComplexesConnectiveCover}
###### Proposition

The inclusions from def. \ref{Complexes} have right resp. left adjoints, which we denote by


$$
    \mathrm{Ch}_{k,\bullet}
      \underoverset
        {\underset{\mathrm{cn}_n}{\longrightarrow}}
        {\overset{i_n}{\longleftarrow}}
        {\bot}
    \mathrm{Ch}_{k, \geq n}
$$

and

$$
    \mathrm{Ch}^{\geq 0}_k
      \underoverset
       {\underset {i_n}{\longrightarrow}}
       {\overset{\mathrm{cn}^n}{\longleftarrow}}
       {\bot}
    \mathrm{Ch}^\bullet_k
  \,.
$$

These are [[Quillen adjunctions]] with respect to the [[projective model structure on chain complexes]].


=--

### dgc-Algebras

+-- {: .num_defn #dgcalgebras}
###### Definition

We write $\mathrm{dgcAlg}^\bullet_k$
for the category of [[differential graded-commutative algebras]] over $k$, i.e. commutative monoids in
$\mathrm{Ch}^\bullet_k$. We write $(\mathrm{dgcAlg}^\bullet_k)_{/k[0]}$
for its [[slice category]] over $k = (k[0], d = 0) \in \mathrm{dgcAlg}^{\geq 0}$, hence for the category of [[augmented algebra|augmented]] dgc-algebras,
hence for dgc-algebras $A$ equipped with a homomorphism $\epsilon_A : A \to (k[0], d = 0)$.

Finally we write
$$
  \mathrm{dgcAlg}^{\geq 0}_k
    \hookrightarrow
  \mathrm{dgcAlg}^\bullet_k
$$
for the full subcategory of the dgc-algebras in non-negative degree, hence for the commutative monoids
in $\mathrm{Ch}^{\geq 0}$, and similarly for the augmented case
$$
  (\mathrm{dgcAlg}^{\geq 0}_k)_{/k[0]}
    \hookrightarrow
  (\mathrm{dgcAlg}^{\bullet}_k)_{/k[0]}
  \,.
$$


=--

+-- {: .num_prop #dgcAlgChAdjunction}
###### Proposition

There are [[adjunctions]] between the categories from def. \ref{dgcalgebras} of the form

$$
    \mathrm{dgcAlg}^{\geq 0}_k
     \underoverset
      {\underset{U}{\longrightarrow}}
      {\overset{\mathrm{Sym}}{\longleftarrow}}
      {\bot}
    \mathrm{Ch}^{\geq 0}_k
$$
and
$$
    (\mathrm{dgcAlg}^{\geq 0}_k)_{/k[0]}
     \underoverset
      {\underset{U \circ \mathrm{ker}(\epsilon_{(-)})}{\longrightarrow} }
      {\overset{\mathrm{Sym}_{/k[0]}}{\longleftarrow}}
      {\bot}
    \mathrm{Ch}^{\geq 0}_k
$$

where

1. $U$ forms the underlying chain complex;

1. $\mathrm{ker}(\epsilon_{(-)})$ forms the [[augmentation ideal]];

1. $\mathrm{Sym}$ forms the free graded-commutative dg-algebra;

1. $\mathrm{Sym}_{/k[0]}$ forms the free graded-commutative dg-algebra and regards it with its canonical augmentation over $k$.

Moreover, these are [[Quillen adjunctions]]: the first with respect to the [[projective model structure on chain complexes]] and the [[projective model structure on dgc-algebras]] and the second with respect to the corresponding [[slice model structure]].

=--


## Related concepts

* [[stable Dold-Kan correspondence]]

* [[rational homotopy theory]]

* [[rational parameterized stable homotopy theory]]

* [[rational equivariant homotopy theory]]

* [[rational equivariant stable homotopy theory]]

## References

* {#SchwedeShipley03} [[Stefan Schwede]], [[Brooke Shipley]], _Stable model categories are categories of modules_, Topology 42 (2003), 103-153 ([arXiv:math/0108143](https://arxiv.org/abs/math/0108143), <a href="https://doi.org/10.1016/S0040-9383(02)00006-X">doi:10.1016/S0040-9383(02)00006-X</a> [pdf](http://www.math.uic.edu/~bshipley/classTopFinal.pdf))


[[!redirects stable rational homotopy theory]]


