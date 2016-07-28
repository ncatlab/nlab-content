
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


This page collects material related to

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], 
  
  _Model categories of diagram spectra_, 

  Proceedings of the London Mathematical Society Volume 82, Issue 2, 2000 

  ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

on a unified construction and comparison of the [[Bousfield-Friedlander model structure|model structure on sequential spectra]], [[model structure on symmetric spectra]], [[model structure on orthogonal spectra]], [[model structure on excisive functors]].

Related references include

* {#Piacenza91} [[Robert Piacenza]], _Homotopy theory of diagrams and CW-complexes over a category_, Can. J. Math. Vol 43 (4), 1991 ([[Piazenza91.pdf:file]])

  also chapter VI of [[Peter May]] et al., _Equivariant homotopy and cohomology theory_, 1996 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf))

* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))


* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_ (2012)

***


#Contents#
* table of contents
{:toc}

## Part I. Diagram spaces and diagram spectra
 {#PartI}

This part gives a unified discussion of the categories of

1. [[sequential spectra]]

1. [[symmetric spectra]]

1. [[orthogonal spectra]]

1. pre-[[excisive functors]]

(all in [[topological spaces]]) as [[categories of modules]] with respect to [[Day convolution]] monoidal structures on [[Top]]-[[enriched functor categories]] over restrictions to [[faithful functor|faithful]] sub-[[sites]] of the canonical representative of the [[sphere spectrum]] as an excisive functor on $Top^{\ast/}_{fin}$.

Throughout, write 

* $Top \coloneqq Top_{cg}$ for the [[category]] of  [[compactly generated topological spaces]]; this is a [[cartesian monoidal category]] $(Top, \times)$ (in fact a [[cartesian closed category]]);

* $Top^{\ast/}$ for the corresponding [[pointed topological spaces]]; this is a [[symmetric monoidal category]] equipped with the [[smash product]] $\wedge$ of pointed objects;

* $Top_{Quillen}$ for the [[classical model structure on topological spaces]] ([[compactly generated topological spaces]]); in particular this is a [[monoidal model category]] $(Top_{Quillen}, \times)$;

* $Top^{\ast/}_{Quillen}$ for the corresponding [[classical model structure on pointed topological spaces]], in particular this is a [[monoidal model category]] $(Top_{Quillen}^{\ast/}, \wedge)$.


Throughout part I we are dealing with $(Top^{\ast/},\wedge)$-[[enriched categories]],  $(Top^{\ast/}, \wedge)$-[[enriched functors]], etc., and then in [part II](#PartII) we are dealing with $(Top_{Quillen}^{\ast/}, \wedge)$-[[enriched model categories]] etc.

### $\mathbb{S}$-modules


+-- {: .num_defn #TopologicalDiagramCategoriesForSpectra}
###### Definition

Define the following [[pointed topologically enriched categories|pointed topologically enriched]] [[symmetric monoidal category|symmetric]] [[closed monoidal categories]] (the [[tensor product]] is a [[pointed topologically enriched functor]]):

1. $Seq$ has as objects the [[natural numbers]] and has only identity morphisms, tensor product is the addition of natural numbers, tensor unit is 0. As a $Top^{\ast/}$-[[enriched category]] the hom-spaces are

   $$
     Seq(n_1,n_2) = 
     \left\{
       \array{
          S^0 & for\; n_1 = n_2
          \\
          \ast & otherwise
       }
    \right.
   $$

1. $Sym$ is the standard [[skeletal category|skeleton]] of the [[core]] of [[FinSet]], objects are the sets $\{1, \cdots,n\}$ for $n \in \mathbb{N}$, all morphisms are [[automorphisms]] and the [[automorphism group]] of $\{1,\cdots,n\}$ is the [[symmetric group]] $\Sigma_n$, tensor product is the [[disjoint union]] of sets, tensor unit is the [[empty set]]; we turn this into a $Top^{\ast/}$-[[enriched category]] by adjoining a basepoint:

   $$
     Sym(n_1, n_2) =
     \left\{
       \array{
          (\Sigma_{n_1})_+ & for \; n_1 = n_2
          \\
          \ast & otherwise
       }
     \right.
   $$

1. $Orth$ has as objects finite dimenional real linear [[inner product spaces]] $(V, \langle -,-\rangle)$ and as morphisms the [[linear map|linear]] [[isometry|isometric]] [[isomorphisms]] between these; hence the [[automorphism group]] of the object $(V, \langle -,-\rangle)$ is the [[orthogonal group]] $O(V)$; the monoidal product is [[direct sum]] of linear spaces, the tensor unit is the 0-vector space; again we turn this into a $Top^{\ast/}$-enriched category by adjoining a basepoint to the hom-spaces;
  
  $$
    Orth(V_1,V_2) 
    \simeq
    \left\{
       \array{
         O(V_1)_+ & for \; dim(V_1) = dim(V_2)
         \\
         \ast & otherwise
       }
    \right.
  $$


1. $Top_{fin}^{\ast/}$ is the [[full subcategory]] of [[pointed topological space]] on those [[homeomorphism|homeomorphic]] to [[finite CW-complexes]], tensor product is their [[smash product]], tensor unit is the [[0-sphere]] $S^0$.

Denote the canonical [[faithful functor|faithful]] [[subcategory]] inclusions by

$$
 \array{
   Seq 
     &\stackrel{seq}{\hookrightarrow}& 
   Sym 
    &\stackrel{sym}{\hookrightarrow}& 
   Orth 
     &\stackrel{orth}{\hookrightarrow}& 
   Top_{fin}^{\ast/}
   \\
   n 
    &\mapsto& 
   \{1,\cdots, n\} 
     &\mapsto& 
   \mathbb{R}^n 
    &\mapsto& 
   S^n
   \\
    && 
    && 
   V
    &\mapsto& 
   S^V
  }
  \,,
$$

where $S^V$ denotes the [[one-point compactification]] of $V$. On morphisms $sym \colon (\Sigma_n)_+ \hookrightarrow (O(n))_+$ is the inclusion of [[permutation]] matrices into [[orthogonal group|orthogonal]] matrices and $orth \colon O(V)_+ \hookrightarrow Aut(S^V)$ is on $O(V)$ the topological subspace inclusions of the pointed [[homeomorphisms]] $S^V \to S^V$ that are induced under forming [[one-point compactification]] from linear isometries of $V$.

=--

+-- {: .num_prop #PropertiesOfTopologicalDiagramCategoriesForSpectra}
###### Proposition

The sequence of inclusions in def. \ref{TopologicalDiagramCategoriesForSpectra} satisfies the following properties:

1. All three inclusions are [[strong monoidal functors]].

1. Under passing to [[enriched functor categories]], restriction $(-)^\ast$ along these inclusions and [[left Kan extension]] $(-)_!$ along them yields a sequence of [[adjunctions]]

   $$
    \array{
      [Top_{fin}^{\ast/}, Top^{\ast/}]
        \stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}
      [Orth, Top^{\ast/}]
        \stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}
      [Sym, Top^{\ast/}] 
        \stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}
      [Seq, Top^{\ast/}] 
    }
     \,.
   $$

1. All four [[enriched functor categories]] become [[symmetric monoidal categories]] with the [[Day convolution]] monoidal product structure induced by the monoidal structure of their [[sites]]. 

1. With respect to this all [[adjunctions]] above are symmetric [[monoidal adjunctions]] (the [[right adjoint]] is a [[symmetric monoidal functor|symmetric]] [[lax monoidal functor]], the [[left adjoint]] is even a [[symmetric monoidal functor|symmetric]] [[strong monoidal functor]]).

=--

(e.g. [MMSS 00, I.3](#MMSS00))



Notice the following:

+-- {: .num_lemma #DayConvolutionTensorUnitIsYonedaImageOfTensorUnitInSite}
###### Lemma

For $\mathcal{C}$ a $V$-[[enriched category|enriched]] [[monoidal category]], under the [[Yoneda embedding]]

$$
  y \colon \mathcal{C}^{op} \hookrightarrow [\mathcal{C}, Top^{\ast/}]
$$

the [[tensor unit]] in $\mathcal{C}$ goes to the tensor unit of the induced [[Day convolution]] structure on $[\mathcal{C}, Top^{\ast/}]$.

=--

(see at _[[Day convolution]]_ [this lemma](Day+convolution#DayConvolutionTensorUnitIsYonedaImageOfTensorUnitInSite))


+-- {: .num_defn #StandardRepresentativeOfTheSphereSpectrum}
###### Definition

Write

$$
  \mathbb{S} \coloneqq y(S^0) \in [Top_{fin}^{\ast/}, Top^{\ast/}]
$$

for the image under the [[Yoneda embedding]] of the [[tensor unit]] in $Top_{fin}^{\ast/}$ with its [[smash product]] (the [[0-sphere]]), which by lemma \ref{DayConvolutionTensorUnitIsYonedaImageOfTensorUnitInSite} is the tensor unit in $([Top_{fin}^{\ast/}, Top^{\ast/}], \otimes_{Day})$.

Since this is going to be the standard presentation of the [[sphere spectrum]] in the [[model structure for excisive functors]] on $[Top_{fin}^{\ast/}, Top^{\ast/}]$ we refer to it as _[[generalized the|the]] [[sphere spectrum]]_.

For its restrictions along the above sub-site inclusions, prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra}, write

$$
  \mathbb{S}_{Orth} \coloneqq orth^\ast \mathbb{S} 
  \,,
  \;
  \mathbb{S}_{Sym} \coloneqq sym^\ast \mathbb{S}_{orth} 
  \,,
  \;
  \mathbb{S}_{Seq} \coloneqq seq^\ast \mathbb{S}_{sym} 
  \,.
$$


=--

+-- {: .num_remark #RestrictionsOfSphereSpectrumAreStillMonoidObjects}
###### Remark

While $\mathbb{S}$ in def. \ref{StandardRepresentativeOfTheSphereSpectrum} is the [[tensor unit]] in $([Top_{fin}^{\ast/}, Top^{\ast/}], \otimes_{Day})$, neither of its restrictions $\mathbb{S}_{Orth},\mathbb{S}_{Sym}, \mathbb{S}_{Seq}$ is the tensor unit in $([Orth, Top^{\ast/}],\otimes_{Day}), ([Sym, Top^{\ast/}],\otimes_{Day}), ([Seq, Top^{\ast/}],\otimes_{Day})$, respectively. 

Nevertheless, because by prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra} the restriction functors are [[strong monoidal functors]] and because the tensor unit $\mathbb{S}$ canonically has the structure of a [[monoid object]], each of $\mathbb{S}_{Orth},\mathbb{S}_{Sym}, \mathbb{S}_{Seq}$ inherts the structure of a [[monoid object]] in the respective [[Day convolution]] [[monoidal category]].

Moreover, $\mathbb{S}_{Orth}$ and $\mathbb{S}_{Sym}$ are [[commutative monoid objects]], while $\mathbb{S}_{Seq}$ is not commutative (due to the [graded commutativity in the smash product of spheres](smash+product+of+spectra#GradedCommutativity) which is not reflected in the trivial symmetry of the tensor product on $Seq$).

| | $\mathbb{S}$ | $\mathbb{S}_{Orth}$ | $\mathbb{S}_{Sym}$ | $\mathbb{S}_{Seq}$ |
|--|--------------|---------------------|--------------------|-------------------|
| [[monoid object]] | yes | yes | yes | yes |
| [[commutative monoid object]] | yes | yes | yes | no |
| [[tensor unit]] | yes | no | no | no |

Explicitly, by the discussion at _[Day convolutions -- Properties -- Monoids](Day+convolution#Monoids)_, monoids with respect to Day convolution are equivalently [[lax monoidal functors]] on the site, and as such $\mathbb{S}_{Orth}$ is the one given by the canonical [[natural transformations]]

$$
  S^{V_1} \wedge S^{V_2} \longrightarrow S^{V_1 \oplus V_2}
$$

and $\mathbb{S}_{Sym}$ and $\mathbb{S}_{Seq}$ the ones given by the canonical natural transformations

$$
  S^{n_1} \wedge S^{n_2} \longrightarrow S^{n_1 + n_2}
  \,.
$$


=--


Therefore we may consider [[module objects]] over the restrictions of [[generalized the|the]] [[sphere spectrum]] from def. \ref{StandardRepresentativeOfTheSphereSpectrum}.

+-- {: .num_prop #HighlyStructuredSpectraAsDayConvolutionSModules}
###### Proposition

The category of right [[module objects]] over $\mathbb{S}_{Orth}$, $\mathbb{S}_{Sym}$ and $\mathbb{S}_{Seq}$ from def. \ref{StandardRepresentativeOfTheSphereSpectrum}, which are [[monoid objects]] by prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra}, remark \ref{RestrictionsOfSphereSpectrumAreStillMonoidObjects}, are [[equivalence of categories|equivalent]], respectively, to the categories of [[orthogonal spectra]], [[symmetric spectra]] and [[sequential spectra]] (in [[compactly generated topological spaces]]):

$$
  \mathbb{S}_{Orth} Mod_r \simeq OrthSpec(Top)
$$

$$
  \mathbb{S}_{Sym} Mod_r \simeq SymSpec(Top)
$$

$$
  \mathbb{S}_{Seq} Mod_r \simeq SeqSpec(Top)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Write $\mathbb{S}_{dia}$ for any of the three monoids. By the discussion at _[Day convolutions -- Properties -- Monoids](Day+convolution#Monoids)_, right modules with respect to [[Day convolution]] are equivalently right [[modules over monoidal functors]] over the monoidal functor corresponding to $\mathbb{S}_{dia}$ as in remark \ref{RestrictionsOfSphereSpectrumAreStillMonoidObjects}. This means that for $\mathbb{S}_{Sym}$ and $\mathbb{S}_{Seq}$ they are functors $X \colon Sym \longrightarrow sSet^{\ast/}$ or $X \colon Seq \longrightarrow sSet^{\ast/}$, respectively equipped with [[natural transformations]]

$$
  X_p \wedge S^{q}  \longrightarrow X_{p+q}
$$

satisfying the evident [[categorification|categorified]] [[action]] property. In the present case this action property says that these morphisms are determined by 

$$
  X_p \wedge S^1 \longrightarrow X_{p+1}
$$

under the isomorphisms $S^p \simeq S^1 \wedge S^{p-1}$. Naturality of all these morphisms as functors on $Sym$ is the equivariance under the symmetric group actions in the definition of [[symmetric spectra]]. 

Similarly, modules over $\mathbb{S}_{Orth}$ are equivalently functors

$$
  X_V \wedge S^{W}  \longrightarrow X_{V \oplus W}
$$

etc. and their functoriality embodies the [[orthogonal group]]-equivariance in the definition of [[orthogonal spectra]].


=--

+-- {: .num_remark #PreExcisiveFunctorsAreSModules}
###### Remark

For completeness, we may, trivially, add to the three statements in prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} the equivalence

$$
  \mathbb{S} Mod_r \simeq [Top^{\ast/}_{fin}, Top^{\ast/}]
  \,,
$$

which holds tautologically because by def. \ref{StandardRepresentativeOfTheSphereSpectrum} $\mathbb{S}$ is in fact the [[tensor unit]] in $([Top^{\ast/}_{fin}, Top^{\ast/}],\otimes_{Day})$, so that every object here is canonically a module object over $\mathbb{S}$.

Now the [[model structure on excisive functors]] shows that the category $[Top^{\ast/}_{fin}, Top^{\ast/}]$ constitutes a model for [[stable homotopy theory]], while this is not the case for either of its restrictions. 

Hence we may read prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} as saying that while restricting the domain of [[excisive functors]] breaks their property of being a model for [[stable homotopy theory]], but at the same time retaining the correspondingly restricted [[sphere spectrum]]-[[module]] structure first of all becomes non-tautological after restriction and second restores the property of the objects to model spectra.

=--

+-- {: .num_defn #SymmetricSmashProductOfDiagramSpectra}
###### Definition

By remark \ref{RestrictionsOfSphereSpectrumAreStillMonoidObjects} the categories $\mathbb{S}_{Sym} Mod_r$, $\mathbb{S}_{Orth} Mod_r$ and $\mathbb{S}_{Orth} Mod_r$ are [[categories of modules]] over a [[commutative monoid object]] and as such they inherit [[symmetric monoidal category]] structure 

$$
  (\mathbb{S}_{dia} Mod, \wedge_{\mathbb{S}_{dia}})
$$

Via prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} this is equivalently symmetric monoidal product structure 

$$
  (SymSpec(Top), \wedge)
$$

on the category of [[symmetric spectra]] and 

$$
  (OrthSpec(Top), \wedge)
$$

on that of [[orthogonal spectra]]. This is called the _[[symmetric monoidal smash product of spectra]]_.

=--


+-- {: .num_remark #SystemOfStructuredSpectraAndDiagrams}
###### Remark

Combined with the [[free-forgetful adjunctions]] for [[module objects]] ([[free modules]] $\dashv$ underlying objects) the situation described by prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra} and prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} jointly is the following diagram of [[adjunctions]]

$$
 \array{
   && OrthSpec(Top) && SymSpec(Top) && SeqSpec(Top)
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_r && \mathbb{S}_{Orth} Mod_r && \mathbb{S}_{Sym} Mod_r && \mathbb{S}_{Seq} Mod_r
   \\
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   \\
   [Top_{fin}^{\ast/}, Top^{\ast/}]
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   [Orth, Top^{\ast/}]
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   [Sym, Top^{\ast/}] 
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   [Seq, Top^{\ast/}] 
 }
  \,.
$$

=--

In order to conveniently speak about all columns of the system of adjunctions in remark \ref{SystemOfStructuredSpectraAndDiagrams} in a unified way, we introduce the following notation.

+-- {: .num_defn #NotationForGenericDiagramSpectra}
###### Definition

We write $dia \in \{Top^{\ast/, Orth, Sym, Seq}\}$ generically for any one of the four sites in def. \ref{TopologicalDiagramCategoriesForSpectra}.

Accordingly we write $\mathbb{S}_{dia} \in \{\mathbb{S}, \mathbb{S}_{Orth}, \mathbb{S}_{Sym}, \mathbb{S}_{Seq}\}$ generically for any one of the four incarnations of [[generalized the|the]] [[sphere spectrum]] according to def. \ref{StandardRepresentativeOfTheSphereSpectrum}, over these sites.

Finally we will write


$$
  \mathbb{S}_{dia}Mod 
   \stackrel{\overset{seq!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}
  \mathbb{S}_{Seq}Mod
  \simeq
  SeqSpec(Top)
$$

for the [[composition]] of the sequence of [[adjunctions]] to the right of the corresponding category of modules in the diagram below in prop. \ref{SystemOfAdjunctionsForDiagramSpectra}, regarded via prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules} and landing in the category of [[sequential spectra]].

=--



We would like to lift the horizontal adjunctions in the diagram in remark \ref{SystemOfStructuredSpectraAndDiagrams} from the bottom row to the top row. To that end, oberve that the [[categories of modules]] involved here are themselves still [[enriched functor categories]]:

+-- {: .num_lemma #SModulesAsEnrichedFunctors}
###### Lemma

Let ${dia} \in \{Top^{\ast/}, {Orth}, {Sym}, {Seq}\}$ be any one of the sites in def. \ref{TopologicalDiagramCategoriesForSpectra}. 

1. There is an [[equivalence of categories]]

   $$
     \mathbb{S}_{dia} Mod \simeq [ \mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/} ]
   $$

   between the corresponding [[category of modules]] (prop.   \ref{HighlyStructuredSpectraAsDayConvolutionSModules}) and the $Top^{\ast/}$-[[enriched functor category]] over the [[opposite category|opposite]] of its [[full subcategory]] on the [[free modules]].

1. If $\mathbb{S}_{dia}$ is a [[commutative monoid]] (hence for $dia \in \{Top^\ast/, Orth,Sym\}$ but not for $dia = Seq$) then $\mathbb{S}_{dia} FreeMod^{op}$ carries a [[symmetric monoidal category]] structure such that under the above equivalence its [[Day convolution]] is the [[tensor product of modules]].

1. There is a $Top^{\ast/}$-[[enriched functor]]

   $$
     \delta \colon dia \longrightarrow \mathbb{S}_{dia} FreeMod^{op}
   $$

   which is monoidal when $\mathbb{S}_{dia}$ is commutative and which is such that the ([[free module]]$\dashv$[[forgetful functor]])-adjunction is equivalently the [[base change]] along $\delta$:

   $$
     \array{
       \mathbb{S}_{dia} Mod 
         &\simeq&
       [ \mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/}] 
       \\
       {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
       &&
       {}^{\mathllap{\delta^\ast}}\downarrow \uparrow^{\mathrlap{\delta_!}}
       \\
       [dia, Top^{\ast/}] 
         &=&
       [dia, Top^{\ast/}] 
     }
     \,.
   $$

=--


This is a general statement about modules with respect to [[Day convolution]] monoidal structures, see [this proposition](Day+convolution#ModulesInDayConvolutionAreFunctorsOnFreeModulesOp)  ([MMSS 00, theorem 2.2](#MMSS00)). 

+-- {: .num_example #SequentialSpectraAsFunctorsOnFreeSSequModules}
###### Example

For the sequential case $dia = Seq$, then the opposite category $\mathbb{S}_{Seq} FreeMod^{op}$ of [[free modules]] over $\mathbb{S}_{Seq}$ (def. \ref{StandardRepresentativeOfTheSphereSpectrum}) in lemma \ref{SModulesAsEnrichedFunctors} is identified as the non-full subcategory $StdSpheres$ of $Top^{\ast/}$ whose objects are the standard spheres $S^n \coloneqq (S^1)^{\wedge^n}$ and whose hom spaces are the canonical image of $S^{n_2-n_1}$ in the hom space $Top^{\ast/}(S^{n_1},S^{n_2})$ (the image under the smash$\dashv$hom-[[adjunct]] of the identity) if $n_2 \gt n_1$, and the point otherwise:

$$
  \begin{aligned}
    \mathbb{S}_{Seq}FreeMod^{op}(F(n_1), F(n_2))
    & =
    StdSpheres(S^{n_1}, S^{n_2})
    \\
    & \coloneqq
    \left\{
      \array{
        im(S^{n_2-n_2} \to Top^{\ast/}(S^{n_1}, S^{n_2})) & for \; n_1 \leq n_2
        \\
        \ast & otherwise
      }
    \right.
  \end{aligned}
  \,.
$$

Hence according to lemma \ref{SModulesAsEnrichedFunctors} [[sequential spectra]] are equivalently $Top^{\ast/}$-enriched functors on StdSpheres:

$$
  SeqSpec
  \simeq
  [StdSpheres, Top^{\ast/}]
  \,.
$$

=--

In this form the statement appears also as ([Lydakis 98, prop. 4.3](#Lydakis98)). See also at _[sequential spectra -- As diagram spectra](sequential+spectrum#AsDiagramSpectra)_.


+-- {: .proof}
###### Proof

The free $\mathbb{S}_{Dia}$ modules are those of the form $y(d)\wedge \mathbb{S}_{Dia}$, where $d \in Dia$ is an object, and $y$ denotes the [[Yoneda embedding]]. For the case $Dia = Seq$ this means that they are labeled by $k \in \mathbb{N}$, their underlying functor $F(k) \in [Seq,Top^{\ast/}]$ is given by

$$
  F(k)
  \;\colon\;
  n 
  \mapsto
  \left\{
    \array{
      S^{n-k} & for\; n \geq k
      \\
      \ast & otherwise
    }
  \right.
$$

and the $\mathbb{S}_{Seq}$-[[action]] on these is, expressed as [[modules over monoidal functors]] (via [this fact](Day+convolution#DayMonoidsAreLaxMonoidalFunctorsOnTheSite) about modules with respect to [[Day convolution]]) by the canonical identifications

$$
  S^{n_1} \wedge F(k)_{n_2}
  =
  S^{n_1} \wedge S^{n_2-k}
  \overset{}{\longrightarrow}
  S^{n_1 + n_2 - k}
  =
  F(k)_{n_1+ n_2}
$$

whenever $n_2 \geq k$, and by the [[zero morphism]] otherwise.

Now for $R$ any other $\mathbb{S}_{Seq}$-module, with action

$$
  S^{n_1} \wedge R_{n_2} \overset{\rho_{n_1,n_2}}{\longrightarrow} R_{n_1 + n_2}
$$

then a homomorphism of $\mathbb{S}_{Seq}$-modules $\phi \colon F(k)\to R$ has components $\phi_{n}\colon S^{n-k} \to R_n$ fitting into commuting diagrams of the form

$$
  \array{
     S^{n_1} \wedge S^{n_2 - k} &\overset{\simeq}{\longrightarrow}& S^{n_1 + n_2 - k}
     \\
     {}^{\mathllap{(id,\phi_{n_2})}}\downarrow 
       && 
     \downarrow^{\mathrlap{\phi_{n_1+n_2}}}
     \\
     S^{n_1} \wedge R_{n_2} &\overset{\rho_{n_1,n_2}}{\longrightarrow}& R_{n_1+n_2}
  }
$$

for $n_2 \geq k$. By the fact that the top morphism here is an isomorphism, all the components $\phi_{n \geq k}$ are uniquely fixed by the component $\phi_k$ as 

$$
  \phi_{n geq k} = \rho_{n-k,k} \circ \phi_k 
$$

(and $\phi_{n \lt k} = 0$). Of course this just confirms the [[free property]] of free spectra: morphisms of $\mathbb{S}_{Seq}$-modules $F(k) \longrightarrow R$ are equivalent to morphisms in $[Seq,Top^{\ast/}]$ from $y(k)$ to $R$, which by the [[Yoneda lemma]] form the space $R_k \in Top^{\ast/}$.

Specialized to $R$ a free spectrum itself this verifies that the hom-spaces between free $\mathbb{S}_{Seq}$-modules are as claimed:

$$
  \mathbb{S}_{Seq}FreeMod(F(k_2),F(k_1))
  \simeq
  F(k_1)_{k_2} 
  \simeq
  \left\{
    \array{
      S^{k_2-k_1} & for \; k_2 \geq k_1
      \\
      \ast & otherwise
    }
  \right.
  \,.
$$

Of course this is just the defining free property. But now comparison with the above commuting square for the case $n_1 = k_1$ and $n_2 = k_2$ shows that composition in $\mathbb{S}_{Seq} FreeMod^{op}$ is indeed the composition in $Top^{\ast/}$ under the identification of $F(k)$ with $S^k$ and of the above hom-space $S^{k_2-k_1}$ with its image under $S^{k_2-k_1} \to Top^{\ast/}(S^{k_1},S^{k_2})$.

=--

From lemma \ref{SModulesAsEnrichedFunctors} we immediately get the following:


+-- {: .num_prop #SystemOfAdjunctionsForDiagramSpectra}
###### Proposition

The horizontal adjunctions in remark \ref{SystemOfStructuredSpectraAndDiagrams} lift to adjunctions between categories of modules, such as to give a [[commuting diagram]] of adjunctions as follows:

$$
 \array{
   && OrthSpec(Top) && SymSpec(Top) && SeqSpec(Top)
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_r 
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   \mathbb{S}_{Orth} Mod_r 
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   \mathbb{S}_{Sym} Mod_r 
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   \mathbb{S}_{Seq} Mod_r
   \\
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   \\
   [Top_{fin}^{\ast/}, Top^{\ast/}]
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   [Orth, Top^{\ast/}]
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   [Sym, Top^{\ast/}] 
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   [Seq, Top^{\ast/}] 
 }
  \,.
$$

=--

([MMSS 00, prop. 3.4 with construction 2.1](#MMSS00))


We consider now, prop. \ref{StrictModelStructureOnDiagramSpectra} below, "strict" [[model category]] structures on the above categories of spectra, which regard spectra only as diagrams of topological spaces, ignoring the fact that it is not the degreewise [[homotopy groups]] but the [[stable homotopy groups]] that are to be invariants of [[stable homotopy types]] (this is def. \ref{StableEquivalencesForDiagramSpectra} below with an extra subtlety in the case of symmetric spectra, see prop. \ref{RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra} below). Incorporating the latter is accomplished by a [[Bousfield localization of model categories|left Bousfield localizatiob]] of the strict model structures to the genuine stable model structures [below](#ProofOfTheStableModelStructure).

+-- {: .num_prop #StrictModelStructureOnDiagramSpectra}
###### Proposition

Write $[Seq, Top^{\ast/}_{Quillen}]$ for the [[model category]] structure on $\mathbb{N}$-parameterized sequences of pointed topological spaces, whose weak equivalences, fibrations and cofibrations are degreewise those of the [[classical model structure on pointed topological spaces]]. (This is equivalently the injective as well as the  projective [[model structure on functors]] over the discrete category $\mathbb{N}$).

Then for each of the categories in the diagram of prop. \ref{SystemOfAdjunctionsForDiagramSpectra}, say that the **strict model structure** on it is the [[transferred model structure]] from $[Seq, Top^{\ast/}_{Quillen}]$ along the composite adjunction connecting the two in that diagram, so that we get a diagram of [[Quillen adjunctions]]

$$
 \array{
   && OrthSpec(Top)_{strict} && SymSpec(Top)_{strict} && SeqSpec(Top)_{strict}
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_{strict}
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   \mathbb{S}_{Orth} Mod_{strict}
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   \mathbb{S}_{Sym} Mod_{strict}
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   \mathbb{S}_{Seq} Mod_{strict}
   \\
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   &&
   {}^{\mathllap{U}}\downarrow \uparrow^{\mathrlap{F}}
   \\
   [Top_{fin}^{\ast/}, Top^{\ast/}]_{strict}
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underset{orth^\ast}{\longrightarrow}}&
   [Orth, Top^{\ast/}]_{strict}
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underset{sym^\ast}{\longrightarrow}}&
   [Sym, Top^{\ast/}]_{strict} 
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underset{seq^\ast}{\longrightarrow}}&
   [Seq, Top^{\ast/}_{Quillen}] 
 }
  \,.
$$

Equivalently, under the identification 

$$
  \mathbb{S}_{dia} Mod \simeq [\mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/}]
$$

of lemma \ref{SModulesAsEnrichedFunctors}, the strict model structure is the projective [[model structure on enriched functors]] ([Piacenza 91](#Piacenza91)) see [here](classical model structure on topological spaces#ModelStructureOnTopEnrichedFunctors).

=--

([MMSS 00, def. 6.1](#MMSS00))

+-- {: .proof}
###### Proof

To see that indeed all the adjunctions here are [[Quillen adjunctions]], use that by prop. \ref{PropertiesOfTopologicalDiagramCategoriesForSpectra} and lemma \ref{SModulesAsEnrichedFunctors} all [[right adjoints]] are given by restrictions of [[sites]]. By definition of the strict model structures and transferred model structures their fibrations and acyclic fibrations are objectwise so, and hence are preserved by these restriction functors.

=--


+-- {: .num_remark #TheStrictModelStructuresOnDiagramSpectra}
###### Remark

The model structure 

$$
  \mathbb{S}_{seq} Mod_{strict}
  \simeq
  SeqSpec(Top)_{strict}
$$ 

in prop. \ref{StrictModelStructureOnDiagramSpectra}
is the _[strict model structure on topological sequential spectra](model+structure+on+topological+sequential+spectra#TheStrictModelStructure)_.

=--

The strict model structures of prop. \ref{StrictModelStructureOnDiagramSpectra} [[presentable (infinity,1)-category|present]] the [[homotopy theory]] of the given diagrams of homotopy types, hence a homotopy theory of pre-spectra. To obtain from this the genuine [[stable homotopy theory]] of genuine spectra we need to restrict this to [[Omega-spectra]], in the following sense.

+-- {: .num_defn #StableEquivalencesForDiagramSpectra}
###### Definition

For any of the four categories of spectra in prop. \ref{SystemOfAdjunctionsForDiagramSpectra}, we say (with notation from def. \ref{NotationForGenericDiagramSpectra}) that:

1. an object $X$ is an _Omega-spectrum_ if $seq^\ast X $ is an [[Omega spectrum]] in the standard sense of [[sequential spectra]];

1. a morphism $f$ is a _stable weak homotopy equivalence_ if $seq^\ast(f)$ is a [[stable weak homotopy equivalence]] in the standard sense of [[sequential spectra]] (an [[isomorphism]] on all [[stable homotopy groups]] of sequential spectra);

1. a morphism $f$ is a _stable equivalence_ if for all Omega-spectra $X$ in the above sense, the morphism $[f,E]_{strict}$ is a [[bijection]] (where $[-,E]_{strict}$ is the [[hom-functor]] of the [[homotopy category]] of the strict model structure of prop. \ref{StrictModelStructureOnDiagramSpectra}.


=--

([MMSS00, def. 8.3 with the notation from p. 21](#MMSS00))


The following proposition says that def. \ref{StableEquivalencesForDiagramSpectra} makes sense, in that if the [[Bousfield localization of model categories|left Bousfield localization]] of the strict model structures at the stable equivalences exists (which we check [below](ProofOfTheStableModelStructure)) then it indeed localizes the homotopy theory to the [[Omega-spectra]].

+-- {: .num_prop #StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences}
###### Proposition

The weak equivalences in the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}) and the stable equivalences of def. \ref{StableEquivalencesForDiagramSpectra} are related as follows:

1. Every weak equivalence with respect to the strict model structure is a stable equivalence.

1. Every stable equivalence between Omega-spectra (def. \ref{StableEquivalencesForDiagramSpectra}) is a weak equivalence in the strict model structure.

=--

([MMSS 00, lemma 8.11](#MMSS00))

+-- {: .proof}
###### Proof

The first statement follows by def. \ref{StableEquivalencesForDiagramSpectra} since weak equivalences become isomorphisms in the [[homotopy category]].

For the second statement, let $f \colon X \to Y$ be a stable equivalence between Omega-spectra. Then by definition, in particular

$$
  [f,X]_{strict} \;\colon\; [Y,X]_{strict} \longrightarrow [X,X]_{strict}
$$

is a [[bijection]]. Therefore the pre-image of $[id_X] \in [X,X]_{strict}$ is an inverse to $f$ in the [[homotopy category]] of the strict model structure. Hence $f$ represents an isomorphism in the strict homotopy category and is hence a weak equivalence in the strict model structure.

=--





###  Free spectra
 {#FreeSpectra}

> This is a technical section with discussion of certain [[free construction|free]] objects  in the categories of spectra of prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules}. The discussion here provides technical lemmas that are used in the proof of the stable model structures [below](#ProofOfTheStableModelStructure), the proof of the Quillen equivalences between them [further below](#QuillenEquivalencesOfStableModelStructures) and [then](#MonoidalStableModelStructure) the proof that the model structure is monoidal.

The concept of _[[free spectrum]]_ is a generalization of that of _[[suspension spectrum]]_. In fact the [[stable homotopy types]] of free spectra are precisely those of iterated [[loop space objects]] of [[suspension spectra]]. But for the development of the theory what matters is free spectra before passing to stable homotopy types, for as such they play the role of the basic cells for the stable [[model structures on spectra]] analogous to the role of the [[n-spheres]] in the [[classical model structure on topological spaces]] (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} below).

Moreover, while free [[sequential spectra]] are just re-indexed [[suspension spectra]], free [[symmetric spectra]] and free [[orthogonal spectra]] in addition come with suitably freely generated [[actions]] of the [[symmetric group]] and the [[orthogonal group]]. It turns out that this is not entirely trivial; it leads to a subtle issue (lemma \ref{AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences} below) where the [[adjuncts]] of certain canonical inclusions of free spectra are [[stable weak homotopy equivalences]] for sequential and orthogonal spectra, but _not_ for symmetric spectra.  The fine analysis of this phenomenon is crucial in the proof of the [[Quillen equivalences]] between the stable model structures on the four models of spectra (theorem \ref{QuillenEquivalencesBetweenStableModelStructuresOnDiagramSpectra}). 


+-- {: .num_defn #FreeStructuredSpectrum}
###### Definition

For $dia \in \{Top^{\ast/}_{fin}, Orth, Sym, Seq\}$ and for each $n \in \mathbb{N}$, the functor 

$$
  (-)_n
  \;\colon\;
  \mathbb{S}_{dia}Mod \stackrel{seq^\ast}{\longrightarrow} \mathbb{S}_{Seq}Mod \simeq SeqSpec(Top) \stackrel{(-)_n}{\longrightarrow} Top^{\ast/}
$$

that sends a [[structured spectrum]] (notation as in def. \ref{NotationForGenericDiagramSpectra}) to the $n$th component space of its underlying [[sequential spectrum]] has a [[left adjoint]]

$$
  F^{dia}_n \;\colon\; Top^{\ast/} \longrightarrow \mathbb{S}_{dia}Mod
  \,.
$$

This is called the _[[free structured spectrum]]_-functor.

The [[adjunction units]] in the sequence of adjunctions equip these with canonical [[natural transformations]]

$$
  F_n^{Seq}
    \stackrel{f_n^{Seq}}{\longrightarrow}
  F_n^{Sym}
    \stackrel{f_n^{Sym}}{\longrightarrow}
  F_n^{Orth}
    \stackrel{f_n^{Orth}}{\longrightarrow}
  F_n^{Top^{\ast/}_{fin}}
  \,.
$$

=--

([MMSS 00, section 8](#MMSS00))

+-- {: .num_lemma #ExplicitExpressionForFreeSpectra}
###### Lemma

Under the equivalence of lemma \ref{SModulesAsEnrichedFunctors}

1. the [[free spectrum]] on $K \in Top^{\ast/}$ is 

   $$
     F^{dia}_n K
      \;=\;
     \mathbb{S}_{dia}FreeMod( - , y(n)\wedge \mathbb{S}_{dia} ) \wedge K
      \;\in\; 
     [ \mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/}]
      \;\stackrel{\simeq}{\to}\;
     \mathbb{S}_{dia}Mod
     \,,
   $$

   where $y(n)$ denotes the [[representable functor|functor represented]] by $dia(n)$ (i.e. by $n$ if $dia = Seq$, by $\{1,\cdots,n\}$ if $dia = Sym$, by $\mathbb{R}^n$ if $dia = Orth$ and by $S^n$ if $dia = Top^{\ast/}_{fin}$).

1. On the free $\mathbb{S}_{dia}$-module on $e \in Dia^{op} \stackrel{y}{\hookrightarrow} [Dia, Top^{\ast/}]$ this takes the value

  $$
    (F^{dia}_n K)(e)
      \;=\;
    \underset{\underset{e_1 \otimes e_2 \to e}{\longrightarrow}}{\lim}
    Dia(n,e_1)\wedge \mathbb{S}_{dia}(e_2) \wedge K
    \,.
  $$

=--

([MMSS00, p. 7 with theorem 2.2](#MMSS00))

+-- {: .proof}
###### Proof

Generally, for $\mathcal{C}$ a $V$-[[enriched category|enriched]] [[symmetric monoidal category]], and for $c\in \mathcal{C}$ an object, then there is an [[adjunction]]

$$
  [\mathcal{C}, V]
    \stackrel{\overset{y(d)\otimes(-)}{\longleftarrow}}{\underset{(-)_c}{\longrightarrow}}
  V
$$

whose characterizing [[natural isomorphism]] is the combination of that of [[tensoring]] with the [[Yoneda embedding]]:

$$
  [\mathcal{C},V]( y(d) \otimes K, F )
    \simeq
  V( K, [\mathcal{C},V]( y(d), F ) )
    \simeq
  V(K, F(d))
  \,.
$$ 

Specializing this to our case with $V = Top^{\ast/}$ and $\mathcal{C} = \mathbb{S}_{dia} FreeMod^{op}$ yields the first statement. The second follows from similar yoga, see the formula at _[Day convolution -- Modules](Day+convolution#FreeModulesOverAMonoidInDayConvolution)_.

=--

+-- {: .num_prop #ExplicitFormOfFreeSpectra}
###### Proposition

Explicitly, the [[free spectra]] according to def. \ref{FreeStructuredSpectrum}, look as follows:

For [[sequential spectra]]: $(F^{Seq}_n K)_q \simeq K \wedge S^{q-n}$;

for [[symmetric spectra]]: $(F^{Sym}_n K)_q \simeq \Sigma(q)_+ \wedge_{\Sigma(q-n)} K \wedge S^{q-n}$.

for [[orthogonal spectra]]: $(F^{Orth}_n K)_q \simeq O(q)_+ \wedge_{O(q-n)} K \wedge S^{q-n}$.

In particular: 

1. $F_0 K = \Sigma^\infty K$;

1. $F_n^{Seq}S^n$ is like the [[suspension spectrum]] of the point (the standard sequential [[sphere spectrum]]) but with its first $n$ components simply removed.


=--

(e.g. [Schwede 12, example 3.20](#Schwede12))

+-- {: .proof}
###### Proof

By working out the formula in item 2 of lemma \ref{ExplicitExpressionForFreeSpectra}. In the sequential case $(Dia = Seq)$ there exists a morphism $k_1 \otimes k_2 \to k_3$ only if $k_1 + k_2 = k_3$ and then there is a unique such. Hence here the colimit in the formula becomes a [[coproduct]] and we find

$$
  \begin{aligned}
    (F^{Seq}_n K)(q)
      & \simeq
    \underset{e_1+e_2 = q}{\coprod} 
    \underset{\simeq\left\{ \array{S^0 & if\, n = e_1 \\ \ast & otherwise}\right.}{\underbrace{Seq(n,e_1)}} \wedge \mathbb{S}_{dia}(e_2) \wedge K
    \\
     & \simeq
      S^{q-n}\wedge K
  \end{aligned}
  \,.
$$

In the symmetric case ($Dia = Sym$) the formula is similar except that $S^0 = Seq(q,q)_+$ is replaced by $Sym(q,q)_+ = \Sigma(q)_+$ and the colimit goes over the automorphisms that fix $q-n$ elements, thereby producing the partial smash tensor shown in the statement. Analogously for the orthogonal case ($Dia = Orth$).

=--

One use of free spectra, important in the verification of the stable model structures [below](#ProofOfTheStableModelStructure) and in the dicussion of the stable equivalences [further below](#RelatingStableEquivalencesAndStableWeakHomotopyEquivalences), is that they serve to co-represent adjuncts of structure morphisms of spectra. To this end, first consider the following general existence statement.

+-- {: .num_lemma #CorepresentingOfAdjunctsOfStructureMapsExists}
###### Lemma

For each $n \in \mathbb{N}$ there exists a morphism

$$
  \lambda_n
    \;\colon\;
  F_{n+1}^{dia}S^1
    \longrightarrow
  F_n^{dia} S^0
$$

such that for every $X\in \mathbb{S}_{dia} Mod$ the operation $\lambda_n^\ast$ of precomposition with $\lambda_n$ forms a [[commuting diagram]] of the form

$$
  \array{
    \mathbb{S}_{dia}Mod(F^{dia}_n S^0, X) &\simeq& Top^{\ast/}(S^0,X_n) &\simeq& X_n
    \\
    \downarrow^{\mathrlap{\lambda_n^\ast}}
    && &&
    \downarrow^{\mathrlap{\tilde \sigma^X_n}}
    \\
    \mathbb{S}_{dia}Mod(F^{dia}_{n+1} S^1, X)
    &\simeq&
    Top^{\ast/}(S^1, X_{n+1})
    &\simeq&
    \Omega X_{n+1}
  }
  \,,
$$

where the horizontal equivalences are the [[adjunction]] isomorphisms and the canonical identification, and where the right morphism is the $(\Sigma \dashv \Omega)$-[[adjunct]] of the structure map $\sigma_n$ of the [[sequential spectrum]] $seq^\ast X$ underlying $X$ (def. \ref{NotationForGenericDiagramSpectra}).

=--

+-- {: .proof}
###### Proof

Since all prescribed morphisms in the diagram are [[natural transformations]], this is in fact a diagram of copreheaves on $\mathbb{S}_{dia} Mod$

$$
  \array{
    \mathbb{S}_{dia}Mod(F^{dia}_n S^0, -) &\simeq& Top^{\ast/}(S^0,(-)_n) &\simeq& (-)_n
    \\
    \downarrow^{\mathrlap{}}
    && &&
    \downarrow^{\mathrlap{\tilde \sigma^{(-)}_n}}
    \\
    \mathbb{S}_{dia}Mod(F^{dia}_{n+1} S^1, -)
    &\simeq&
    Top^{\ast/}(S^1, (-)_{n+1})
    &\simeq&
    \Omega (-)_{n+1}
  }
  \,.
$$

With this the statement follows by the [[Yoneda lemma]].

=--

Now we say explicitly what these maps are:

+-- {: .num_defn #CorepresentationOfAdjunctsOfStructureMaps}
###### Definition

For $n \in \mathbb{N}$, write

$$
  \lambda_n \;\colon\; F_{n+1} S^1 \longrightarrow F_n S^0
$$

for the [[adjunct]] under the ([[free structured spectrum]] $\dashv$ $n$-component)-[[adjunction]] in def. \ref{FreeStructuredSpectrum} of the composite morphism

$$
  S^1 
    \stackrel{=}{\to}
  (F_n^{Seq}(S^0))_{n+1}
    \stackrel{(f_n^{Seq})_{n+1}}{\hookrightarrow} 
  (F^{dia}_n S^0)_{n+1}
  \,,
$$

where the first morphism is via prop. \ref{ExplicitFormOfFreeSpectra} and the second comes from the adjunction units according to def. \ref{FreeStructuredSpectrum}.

=--

([MMSS 00, def. 8.4](#MMSS00), [Schwede 12, example 4.26](#Schwede12))

+-- {: .num_lemma #IndeedCorepresentationOfAdjunctsOfStructureMaps}
###### Lemma

The morphisms of def. \ref{CorepresentationOfAdjunctsOfStructureMaps} are those whose existence is asserted by prop. \ref{CorepresentingOfAdjunctsOfStructureMapsExists}.
 
=--

([MMSS 00, lemma 8.5](#MMSS00), following [Hovey-Shipley-Smith 00, remark 2.2.12](#HoveyShipleySmith00))


+-- {: .proof}
###### Proof

Consider the case $Dia = Seq$ and $n = 0$. All other cases work analogously.

By prop. \ref{ExplicitFormOfFreeSpectra}, in this case the morphism $\lambda_0$ has components like so:

$$
  \array{
    \vdots && \vdots
    \\
    S^3 &\stackrel{id}{\longrightarrow}& S^3
    \\
    S^2 &\stackrel{id}{\longrightarrow}& S^2
    \\
    S^1 &\stackrel{id}{\longrightarrow}& S^1
    \\
    \ast &\stackrel{0}{\longrightarrow}& S^0
    \\
    \underbrace{\,\,\,} && \underbrace{\,\,\,}
    \\
    F_1 S^1 &\stackrel{\lambda_0}{\longrightarrow}& F_0 S^0
  }
  \,.
$$

Now for $X$ any sequential spectrum, then a morphism $f \colon F_0 S^0 \to X$ is uniquely determined by its 0th component $f_0 \colon S^0 \to X_0$ (that's of course the free property of $F_0 S^0$); as the compatibility with the structure maps forces the first component, in particular, to be $\sigma_0^X\circ \Sigma f$:

$$
  \array{
    \Sigma S^0 &\stackrel{\Sigma f}{\longrightarrow}& \Sigma X_0
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\sigma_0^X}}
    \\
    S^1 &\stackrel{\sigma_0^X \circ \Sigma f}{\longrightarrow}& X_1
  }
$$

But that first component is just the component that similarly determines the precompositon of $f$ with $\lambda_0$, hence $\lambda_0^\ast f$ is fully fixed as being the map $\sigma_0^X \circ \Sigma f$. Therefore $\lambda_0^\ast$ is the function

$$
  \lambda_0^\ast
  \;\colon\;
  X_0 
  = 
  Maps(S^0, X_0)
  \stackrel{f \mapsto \sigma_0^X \circ \Sigma f}{\longrightarrow}
  \Maps(S^1, X_1)
  =
  \Omega X_1
  \,.
$$

It remains to see that this is the $(\Sigma \dashv \Omega)$-[[adjunct]] of $\sigma_0^X$. By the general formula for adjuncts, this is

$$
  \tilde \sigma_0^X 
    \;\colon\; 
  X_0 
     \stackrel{\eta}{\longrightarrow} 
  \Omega \Sigma X_0
     \stackrel{\Omega \sigma_0^X}{\longrightarrow}
  \Omega X_1
  \,.
$$

To compare to the above, we check what this does on points: $S^0 \stackrel{f_0}{\longrightarrow} X_0$ is sent to the composite

$$
   S^0 
     \stackrel{f_0}{\longrightarrow}
   X_0 
     \stackrel{\eta}{\longrightarrow} 
   \Omega \Sigma X_0
     \stackrel{\Omega \sigma_0^X}{\longrightarrow}
   \Omega X_1
   \,.
$$

To identify this as a map $S^1 \to X_1$ we use the adjunction isomorphism once more to throw all the $\Omega$-s on the right back to $\Sigma$-s the left, to finally find that this is indeed

$$
  \sigma_0^X \circ \Sigma f
    \;\colon\;
  S^1 = \Sigma S^0 \stackrel{\Sigma f}{\longrightarrow} \Sigma X_0 \stackrel{\sigma_0^X}{\longrightarrow} X_1
  \,.
$$

=--

The following property of the maps from def. \ref{CorepresentationOfAdjunctsOfStructureMaps} to be or not to be stable weak homotopy equivalences will be the key technical fact that implies ([below](#RelatingStableEquivalencesAndStableWeakHomotopyEquivalences)) that stable equivalences of spectra are or are not the same as stable weak homotopy equivalences.

+-- {: .num_lemma #AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences}
###### Lemma

The maps $\lambda_n \;\colon\; F_{n+1} S^1 \longrightarrow F_n S^0$  in def. \ref{CorepresentationOfAdjunctsOfStructureMaps} are 

1. stable equivalences, according to def. \ref{StableEquivalencesForDiagramSpectra}, for all four cases of spectra, ${Dia} \in \{Top^{\ast/}, Orth, Sym, Seq\}$;

1. stable weak homotopy equivalences, according to def. \ref{StableEquivalencesForDiagramSpectra}, for sequential spectra, symmetric spectra and pre-excisive functors ${Dia} \in \{Top^{\ast/}, Orth, Seq\}$;


1. **not** stable weak homotopy equivalences for the case of symmetric spectra ${Dia} = {Sym}$.



=--

([Hovey-Shipley-Smith 00, example 3.1.10](#HoveyShipleySmith00), [MMSS 00, lemma 8.6](#MMSS00), [Schwede 12, example 4.26](#Schwede12))

+-- {: .proof}
###### Proof

The first statement is an immediate consequence of lemma \ref{IndeedCorepresentationOfAdjunctsOfStructureMaps}.

The other two statements follow from inspection of the explicit form of the maps, via prop. \ref{ExplicitFormOfFreeSpectra}, in each case separately:

**sequential case**

Here the components of the morphism eventually stabilize to isomorphisms

$$
  \array{
    & \vdots && \vdots
    \\
    (\lambda_n)_{n+3} & S^3 &\stackrel{id}{\longrightarrow}& S^3
    \\
    (\lambda_n)_{n+2} & S^2 &\stackrel{id}{\longrightarrow}& S^2
    \\
    (\lambda_n)_{n+1} & S^1 &\stackrel{id}{\longrightarrow}& S^1
    \\
    (\lambda_n)_n \colon & \ast &\stackrel{0}{\longrightarrow}& S^0
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \vdots && \vdots
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \underbrace{\,\,\,} && \underbrace{\,\,\,}
    \\
    \lambda_n \colon & F_{n+1} S^1 &\stackrel{}{\longrightarrow}& F_n S^0
  }
$$

and this immediately gives that $\lambda_n$ is an isomorphism on stable homotopy groups.

**orthogonal case**

Here for $q \geq n+1$ the $q$-component of $\lambda_n$ is the [[quotient]] map

$$
  (\lambda_n)_q 
    \;\colon\;
  O(q)_+ \wedge_{O(q-n-1)} S^{q-n}
   \simeq
  O(q)_+ \wedge_{O(q-n-1)} S^1 \wedge S^{q-n-1}
  \longrightarrow
  O(q)_+ \wedge_{O(q-n)}S^{q-n}
  \,.
$$

By the [suspension isomorphism](homotopy+group+of+a+spectrum#SuspensionIsomorphismOfStableHomotopyGroups) for [[stable homotopy groups]], $\lambda_n$ is a stable weak homotopy equivalence precisely if any of its [[reduced suspension|suspensions]] is. Hence consider instead $\Sigma^n \lambda_n \coloneqq S^n \wedge \lambda_n$, whose $q$-component is 

$$
  (\Sigma^n\lambda_n)_q 
    \;\colon\;
  O(q)_+ \wedge_{O(q-n-1)} S^{q}
    \longrightarrow
  O(q)_+ \wedge_{O(q-n)}S^{q}
  \,.
$$

Now due to the fact that $O(q-k)$-action on $S^q$ lifts to an $O(q)$-action, the quotients of the diagonal action of $O(q-k)$ equivalently become quotients of just the left action. Formally this is due to the existence of the [[commuting diagram]]

$$
  \array{
    O(q)_+ \wedge S^q 
     &\stackrel{id}{\longrightarrow}& 
    O(q)_+ \wedge S^q 
     &\stackrel{id}{\longrightarrow}& 
    O(q)_+ \wedge S^q 
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{p_2}}
    \\
    Q(q)_+ \wedge_{Q(q-k)} S^q 
     &\longrightarrow&
    Q(q)_+ \wedge_{Q(q)} S^q
    & \stackrel{\simeq}{\longrightarrow} & S^q
  }
$$

which says that the image of any $(g,s) \in O(q)_+  \wedge S^q$ in the quotient $Q(q)_+ \wedge_{Q(q-k)} S^q$ is labeled by $([g],s)$.

It follows that $(\Sigma^n\lambda_n)_q$ is the smash product of a projection map of [[coset spaces]] with the identity on the sphere:

$$
  (\Sigma^n\lambda_n)_q 
    \simeq
  proj_+ \wedge id_{S^q} 
    \;\colon\;
  O(q)/O(q-n-1)_+ \wedge S^q
    \longrightarrow
  O(q)/O(q-n)_+ \wedge S^{q}
  \,.
$$

Now finally observe that this projection function

$$
  proj
  \;\colon\;
  O(q)/O(q-n-1) 
    \longrightarrow
  O(q)/O(q-n)
$$

is $(q - n -1 )$-connected (see [here](coset+space#CofiberSequencesOfCosetsOfOrthogonalGroups)). Hence its smash product with $S^q$ is $(2q - n -1 )$-connected.

The key here is the fast growth of the connectivity with $q$. This implies that for each $s$ there exists $q$ such that $\pi_{s+q}((\Sigma^n \lambda_n)_q)$ becomes an isomorphism. Hence $\Sigma^n \lambda_n$ is a stable weak homotopy equivalence and therefore so is $\lambda_n$.

**symmetric case**
 
Here the morphism $\lambda_n$ has the same form as in the orthogonal case above, except that all occurences of [[orthogonal groups]] are replaced by just their sub-[[symmetric groups]].

Accordingly, the analysis then proceeds entirely analogously, with the key difference that the projection

$$
  \Sigma(q)/\Sigma(q-n-1) 
    \longrightarrow
  \Sigma(q)/\Sigma(q-n)
$$

does _not_ become highly connected as $q$ increases, due to the [[discrete topological space]] underlying the symmetric group. Accordingly the conclusion now is the opposite: $\lambda_n$ is not a stable weak homotopy equivalence in this case.

=--

Another use of free spectra is that their [[pushout products]] may be explicitly analyzed, and checking the [[pushout-product axiom]] for general cofibrations may be reduced to checking it on morphisms between free spectra.

+-- {: .num_lemma #SmashProductOfFreeSpectra}
###### Lemma

For $A, B \in Top^{\ast/}$ and for $k,\ell \in \mathbb{N}$, then the [[symmetric monoidal smash product of spectra]], def. \ref{SymmetricSmashProductOfDiagramSpectra}, applied to the corresponding [[free spectra]] from def. \ref{FreeStructuredSpectrum} relates to the plain [[smash product]] of [[pointed topological spaces]] via [[natural isomorphisms]]

$$
  (F_k A)\wedge_{\mathbb{S}_{dia}} (F_\ell B)
  \simeq
  F_{k+\ell}(A\wedge B)
  \,.
$$

=--

([MMSS 00, lemma 1.8, lemma 21.3](#MMSS00))

+-- {: .proof}
###### Proof

Consider the following sequence of [[natural isomorphisms]]

$$
  \begin{aligned}
    [\mathbb{S}_{dia} FreeMod^{op},Top^{\ast/}]((F_k A)\wedge_{\mathbb{S}_{dia}} (F_\ell B), Z)
    & \simeq
     [\mathbb{S}_{dia} FreeMod^{op}\times \mathbb{S}_{dia} FreeMod^{op}, Top^{\ast/}]((F_k A)\tilde \wedge (F_\ell B), Z \circ \wedge)
    \\
    & \simeq 
    Top^{\ast/}( A\wedge B, F_{k+\ell})
    \\
    & \simeq
    [\mathbb{S}_{dia} FreeMod^{op},Top^{\ast/}](
      F_{k+\ell}(A \wedge B), Z
    )    
  \end{aligned}
  \,,
$$

where we used the adjoint characterization ([here](Day+convolution#DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor)) of the [[Day convolution]]. Since this is natural in $Z$, the [[Yoneda lemma]] implies the claim.

=--

+-- {: .num_lemma #PushoutSmashProductOfFreeSpectraOnGeneratingCofibrationsOfTop}
###### Lemma

The [[symmetric monoidal smash product of spectra]] of the [[free spectrum]] constructions (def. \ref{FreeStructuredSpectrum}) on the generating cofibrations $\{S^{n-1}\overset{i_n}{\hookrightarrow} D^n\}_{n \in \mathbb{B}}$ of the [[classical model structure on topological spaces]] is given by addition of indices

$$
  (F_k i_{n_1}) \Box_{\mathbb{S}_{dia}} (F_\ell i_{n_2})
  \simeq
  F_{k+\ell}( i_{n_1 + n_2})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{SmashProductOfFreeSpectra} the [[commuting diagram]] defining the [[pushout product]] of [[free spectra]]

$$
  \array{
    && F_k S^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} S^{n_2-1}_+
    \\
    & \swarrow && \searrow
    \\
    F_k D^{n_1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} S^{n_2-1}_+
    &&
    &&
    F_k S^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} D^{n_2-1}_+
    \\
    & \searrow && \swarrow
    \\
    && F_k D^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_k D^{n_2-1}_+
  }
$$

is equivalent to this diagram:

$$
  \array{
    && F_{k+\ell}((S^{n_1-1}\times S^{n_2-1})_+)
    \\
    & \swarrow && \searrow
    \\
    F_{k+\ell}((D^{n_1} \times S^{n_2-1})_+)
    &&
    &&
    F_{k+\ell}((S^{n_1-1} \times D^{n_2})_+)
    \\
    & \searrow && \swarrow
    \\
    && F_{k+ \ell}( (D^{n_1}\times D^{n_2})_+ )
  }
  \,.
$$

Since the [[free spectrum]] construction is a left adjoint, it preserves pushouts, and so 

$$
  (F_{k}i_{n_1}) 
    \Box_{\mathbb{S}_{dia}}
  (F_{\ell}i_{n_2})
   \simeq
  F_{k + \ell}( i_{n_1} \Box i_{n_2})
   \simeq
  F_{k + \ell}( i_{n_1 + n_2})
 \,,
$$

where in the second step we used [this lemma](pushout-product#PushoutProductOfSpheresInclusionsIntoDisks).

=--

## Part II. Model categories of diagram spectra
 {#PartII}


We now discuss equipping the diagram categories of [part I](#PartI) with [[model category]] structures, each presenting the [[stable homotopy theory]] (the [[stable (infinity,1)-category of spectra]]), and how the system of [[adjunctions]] between these categories becomes a system of [[Quillen equivalences]] between these model structures.

### 5.-10.) Model structures on plain spectra
 {#ModelStructuresForPlainSpectra}

Here we discuss model structures for plain spectra, [below](ModelStructuresOnRingSpectraAndModuleSpectra) we discuss model structures for [[ring spectra]] and [[module spectra]].

#### The stable model structures
 {#ProofOfTheStableModelStructure}


+-- {: .num_theorem #StableModelStructuresOnDiagramSpectra}
###### Theorem

The [[Bousfield localization of model categories|left Bousfield localization]] of the strict model structures of prop. \ref{StrictModelStructureOnDiagramSpectra} at the stable equivalences of def. \ref{StableEquivalencesForDiagramSpectra} exists, to be called the _stable model structures_. 

Explicitly, there is a model structure $\mathbb{S}_{dia} Mod_{stable}$ whose

* cofibrations are those of the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra});

* weak equivalences are the stable equivalences (def. \ref{StableEquivalencesForDiagramSpectra})

and the identity functors constitute a [[Quillen adjunction]] of the form

$$
  \mathbb{S}_{dia} Mod_{stable}
    \stackrel{\overset{id}{\longleftarrow}}{\underset{id}{\longrightarrow}}
  \mathbb{S}_{dia} Mod_{strict}
  \,.
$$


Moreover $\mathbb{S}_{dia} Mod_{stable}$ is a

1. [[compactly generated model category]];

1. [[proper model category]];

1. $Top^{\ast/}_{Quillen}$-[[enriched model category]].

Specifically, this specializes to 

* fro $Dia = Seq$: the standard [[model structure on topological sequential spectra]];

* for $Dia = Sym$: the standard standard [[model structure on symmetric spectra]];

* for $Dia = Orth$: the standard topological [[model structure on orthogonal spectra]];

* for $Dia = Top^{\ast/}_{CW}$: the topological [[model structure for excisive functors]];


=--

([MMSS00, theorem 9.2](#MMSS00)) 

We give the proof of theorem \ref{StableModelStructuresOnDiagramSpectra} [below](#StableModelStructureOnDiagramSpectraProof), it involves the following definitions and lemmas.

The generating cofibrations and acylic cofibrations are going to be the those induced via [[tensoring]] of representables from the [[classical model structure on topological spaces]] (giving the strict model structure), together with an additional set of morphisms to the generating acylic cofibrations that will force fibrant objects to be Omega-spectra. To that end we need the following little preliminary.


+-- {: .num_remark #CorepresentingForAdjunctOfStructureMapsAreStableEquivalences}
###### Remark

By construction, the morphisms $\lambda_n$ of lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists} are 
stable equivalences according to def. \ref{StableEquivalencesForDiagramSpectra}.

=--

We need to in addition resolve them by suitable cofibrations:

+-- {: .num_defn #ResolutionOfCorepresentationOfAdjunctsOfStructureMaps}
###### Definition

For $n \in \mathbb{N}$ let

$$
  \lambda_n 
    \colon 
  F_{n+} \stackrel{k_n}{\longrightarrow}
    Cyl(\lambda_n)
  \stackrel{def.retr.}{\longrightarrow}
  F_n S^0
$$

be a factorization of the morphism $\lambda_n$ of lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists} and def. \ref{CorepresentationOfAdjunctsOfStructureMaps} through a strict cofibration followed by a strict weak equivalence (e.g. through its [[mapping cylinder]] followed by a [[deformation retraction]] (see [here](mapping+cylinder#FactorizationOfMapThroughMappingCylinderFollowedByDeformationRetraction))).

=--

With this we may state the classes of morphisms that are going to be shown to be the classes of generating (acyclic) cofibrations for the stable model structures:

+-- {: .num_defn #GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}
###### Definition

Recall the sets

$$
  I \coloneqq \{S^{n-1} \hookrightarrow D^n\}_{n \in \mathbb{N}}
$$

$$
  J \coloneqq \{D^n \hookrightarrow D^n \times I\}_{n \in \mathbb{N}}
$$

of generating cofibrations and generating acyclic cofibrations, respectively, of the [[classical model structure on topological spaces]].

Write

$$
  F I \coloneqq \{ y(x) \otimes i_+ \}_{{x \in \mathbb{S}_{Dia} FreeMod} \atop {i \in I}}
$$

for the class of [[free spectra]], def. \ref{FreeStructuredSpectrum}, on the class $I$ above, which by lemma \ref{ExplicitExpressionForFreeSpectra} is equivalently the set of morphisms arising as the [[tensoring]] with a topological generating cofibration of a [[representable functor|representable]] over the [[site]] $\mathbb{S}_{dia} FreeMod$ (the [[site]] for $\mathbb{S}_{dia}Mod$ from lemma \ref{SModulesAsEnrichedFunctors}).
 
Similarly, write

$$
  F J \coloneqq \{ y(x) \otimes j_+ \}_{{x \in \mathbb{S}_{Dia}FreeMod} \atop {j \in J}}
  \,,
$$

for the set of morphisms arising as the [[tensoring]] of a [[representable functor|representable]] with a generating acyclic cofibration of the [[classical model structure on topological spaces]] (with basepoint adjoined).

Finally write 

$$
  K 
  \coloneqq
  F J
  \;\sqcup\;
  \{
    k_n \Box i_+
  \}_{{n \in \mathbb{N}} \atop {i \in I}}
$$

for the [[disjoint union]] of $F J$ with the [[pushout products]] of the resolved maps $k_n$ from def. \ref{ResolutionOfCorepresentationOfAdjunctsOfStructureMaps} with the elements in $I$.

=--

([MMSS 00, def. 9.3](#MMSS00))

+-- {: .num_prop #CofibrantGenerationOfStrictModelStructure}
###### Proposition

The sets $F I$ and $F J$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} (disregarding the set $K$ there) are, respectively sets of [[generating cofibrations]] and generating acyclic cofibrations for the strict model structure $\mathbb{S}_{Dia}Mod_{strict}$ (prop. \ref{StrictModelStructureOnDiagramSpectra}).

=--

+-- {: .proof}
###### Proof

By prop. \ref{StrictModelStructureOnDiagramSpectra} the strict model structure is equivalently the projective pointed  [[model structure on enriched functors|model structure on topologically enriched functors]]

$$
  \mathbb{S}_{Dia}Mod_{strict} \simeq [\mathbb{S}_{Dia}FreeMod^{op}, Top^{\ast/}]_{proj}
  \,.
$$

With this the statement follows by the proof of [this](classical+model+structure+on+topological+spaces#ProjectiveModelStructureOnTopEnrichedFunctors) theorem.

=--

+-- {: .num_lemma #ElementsOfKAreStableEquivalencesAndStrictCofibrations}
###### Lemma

Every element in $K$ (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) is both:

1. a cofibration with respect to the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra});

1. a stable equivalence (def. \ref{StableEquivalencesForDiagramSpectra}).

=--

+-- {: .proof}
###### Proof 

First regarding strict cofibrations: By the [[Yoneda lemma]], the elements in $F J$ have [[right lifting property]] against the strict fibrations, hence in particular they are strict cofibrations. Moreover, by [[Joyal-Tierney calculus]], $k_n \Box i_+$ has left lifting against any acyclic strict fibration $f$ precisely if $k_n$ has left lifting against $f^i$. By $\mathbb{S}_{dia} Mod_{strict}$ behaving like a $Top$-[[enriched model category]] for one argument a relative CW-complex, the latter is still a strict acyclic fibration. Since $k_n$ by construction is a strict cofibration, the lifting follows and hence also $k_n \Box i_+$ is a strict cofibration.

Regarding stable equivalences: The morphisms in $F J$ by design are strict weak equivalences, hence they are in particular stable equivalences. Similarly, the morphisms $k_n$ by construction, by [[two-out-of-three]] and by remark \ref{CorepresentingForAdjunctOfStructureMapsAreStableEquivalences} are stable equivalences. Hence the derived hom (...expand...) out of $k_n \Box i_+$ is the homotopy pullback of a weak equivalence, hence is a weak equivalence, hence on the homotopy category an iso.

=--


The point of the class $K$ in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} is to make the following true:

+-- {: .num_lemma #KInjectivesAreAcyclicCofibrations}
###### Lemma

A morphism $f \colon X \to Y$ in $\mathbb{S}_{dia} Mod$ is a $K$-[[injective morphism]] (for $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) precisely if 

1. it is a fibration in the strict model structure (hence degreewise a fibration)

1. for all $n \in \mathbb{N}$ the [[commuting squares]] of structure map compatibility on the underlying [[sequential spectra]] 

   $$
     \array{
       X_n  &\overset{\tilde\sigma}{\longrightarrow}& \Omega X_{n+1}
       \\
       \downarrow && \downarrow
       \\
       Y_n &\underset{\tilde \sigma}{\longrightarrow}& \Omega Y_{n+1}
     }
   $$

   exhibit [[homotopy pullbacks]].  

=--

([MMSS 00, prop. 9.5](#MMSS00))

+-- {: .proof}
###### Proof

By prop \ref{CofibrantGenerationOfStrictModelStructure}, lifting against $F J$ alone characterizes strict fibrations, hence degreewise fibrations. Lifting against the remaining [[pushout product]] morphism $k_n \Box i_+$ is, by [[Joyal-Tierney calculus]], equivalent to left lifting $i_+$ against the dual pullback product of $f^{k_n}$, which means that $f^{k_n}$ is a weak homotopy equivalence. But by construction (lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists}) $f^{k_n}$ is the comparison morphism into the homotopy pullback under consideration. 

=--

+-- {: .num_cor #KInjectivesObjectsAreOmegaSpectra}
###### Corollary

The $K$-[[injective objects]] (for $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) are precisely the [[Omega-spectra]], def. \ref{StableEquivalencesForDiagramSpectra}.

=--


+-- {: .num_lemma #KInjectiveStableEquivalencesAreStrictEquivalences}
###### Lemma

A morphism in $\mathbb{S}_{dia}Mod$ which is both 

1. a stable equivalence (def. \ref{StableEquivalencesForDiagramSpectra});

1. a $K$-[[injective morphisms]] (with respect to $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) 

is an acyclic fibration in the strict model structure of prop. \ref{StrictModelStructureOnDiagramSpectra}, hence is degreewise a [[weak homotopy equivalence]] and [[Serre fibration]] of topological spaces;

=--

([MMSS 00, corollary 9.8](#MMSS00))

+-- {: .proof}
###### Proof

Let $f\colon X \to B$ be both a stable equivalence as well as a $K$-injective morphism. Since $K$ contains, by prop. \ref{CofibrantGenerationOfStrictModelStructure}, the generating acyclic cofibrations for the strict model structure of prop. \ref{StrictModelStructureOnDiagramSpectra}, $f$ is in particular a strict fibration, hence a degreewise fibration. Therefore the fiber $F$ of $f$ is its [[homotopy fiber]] in the strict model structure. 

> We now want to claim that:

It follows that $F \to \ast$ is a stable equivalence.

> {#WhyFIsStablyEquivalentToThePoint} This needs some explanation:

> Consider for any $E \in \mathbb{S}_{dia}Mod$ the cofiber sequence

> $[B,E]_{strict} \overset{p^\ast}{\longrightarrow} [X,E]_{strict} \overset{}{\longrightarrow} [hocof(p),E]_{strict} \longrightarrow [\Sigma B, E]_{strict} \overset{\Sigma p^\ast}{\longrightarrow}[\Sigma X,E]_{strict}$

> This kind of sequence is long exact for every pointed model category, not necessarily stable. Then let $E$ be any Omega-spectrum. By assumption it follows then that $p^\ast$ and $\Sigma p^\ast$ are isomorphisms, so that exactness implies that $[hocof(p),E]_{strict} = 0$ for all Omega-spectra $E$.

> Now use that on underlying sequential spectra there is a stable weak homotopy equivalence $hocof(p) \longrightarrow \Sigma hofib(p) = \Sigma F$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1#HomotopyCofiberSequencesAreHomotopyFiberSequencesInSpectra)). Since suspension is preserved by passing to underlying sequential spectra, and since stable homotopy groups by definition are those of the underlying sequential spectra, and since stable weak  equivalences are in particular stable equivalences (prop. \ref{StableWeakHomotopyEquivalenceIsStableEquivalence} below) it follows that $[\Sigma F, E]_{strict}$ for all Omega-spectra $E$, hence $[F, \Omega E]_{strict} = 0$ for all Omega-spectra.

> We are to conclude that hence $F \to \ast$ is a stable equivalence. But to conclude this we now need to know that every Omega-spectrum in $\mathbb{S}_{dia}Mod$ is in the image under $\Omega$ of an Omega-spectrum, up to strict equivalence. Indeed one shows that there is a shift functor $sh$ on structured spectra and that $E \overset{}{\longrightarrow} \Omega sh E$ is degreewise a weak homotopy equivalence.

Observe also that $F$, being the pullback of a $K$-injective morphisms (by the standard [closure properties](injective+or+projective+morphism#ClosureProperties)) is a $K$-[[injective object]], so that by corollary \ref{KInjectivesObjectsAreOmegaSpectra} $F$ is an Omega-spectrum. Together this implies with prop. \ref{StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences} that $F \to \ast$ is a weak equivalence in the strict model structure, hence degreewise a [[weak homotopy equivalence]]. From this the [[long exact sequence of homotopy groups]] implies that $\pi_{\bullet \geq 1}(f_n)$ is a [[weak homotopy equivalence]] for all $n$ and for each homotopy group in positive degree. 



To infer from this the remaining case that also $\pi_0(f_0)$ is an isomorphism, observe that, by assumption of $K$-injectivity, lemma \ref{KInjectivesAreAcyclicCofibrations} gives that $f_n$ is a homotopy pullback (in topological spaces) of $\Omega (f_{n+1})$. But, by the above, $\Omega (f_{n+1})$ is a weak homotopy equivalence, since $\pi_\bullet(\Omega(-)) = \pi_{\bullet+1}(-)$. Therefore $f_n$ is the homotopy pullback of a weak homotopy equivalence and hence itself a weak homotopy equivalence.

=--

+-- {: .num_lemma #RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations}
###### Lemma

For $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}  the [[retracts]] of $K$-[[relative cell complexes]] are precisely the morphisms which are

1. stable equivalences (def. \ref{StableEquivalencesForDiagramSpectra}), 

1. as well as cofibrations with respect to the strict model structure  of prop. \ref{StrictModelStructureOnDiagramSpectra}.

=--

([MMSS 00, prop. 9.9 (i)](#MMSS00))


+-- {: .proof}
###### Proof

Since all elements of $K$ are stable equivalences and strict cofibrations by lemma \ref{ElementsOfKAreStableEquivalencesAndStrictCofibrations}, it follows that every retract of a relative $K$-cell complex has the same property.

In the other direction, if $f$ is a stable equivalence and strict cofibration, by the [[small object argument]] it factors $f \colon \stackrel{i}{\to}\stackrel{p}{\to}$ as a relative $K$-cell complex $i$ followed by a $K$-[[injective morphism]] $p$. By the previous statement $i$ is a stable equivalence, and so by assumption and by [[two-out-of-three]] so is $p$. Therefore lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalences} implies that $p$ is a strict acyclic fibration. But then the assumption that $f$ is a strict cofibration means that it has the [[left lifting property]] against $p$, and so the [[retract argument]] implies that $f$ is a retract of the relative $K$-cell complex $i$.


=--

+-- {: .num_cor #KInjectivesAreIndeedTheStableFibrations}
###### Corollary

For $K$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}  the $K$-[[injective morphisms]]
are precisely those which are
[[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable equivalences.

=--

([MMSS 00, prop. 9.9 (ii)](#MMSS00)) 


+-- {: .num_lemma #StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations}
###### Lemma

A morphism in $\mathbb{S}_{dia}Mod$ is both

1. a stable equivalence (def. \ref{StableEquivalencesForDiagramSpectra})

1. [[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable equivalences;

precisely if it is an acylic fibration in the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}).

=--

([MMSS 00, prop. 9.9 (iii)](#MMSS00))

+-- {: .proof}
###### Proof

Every acyclic fibration in the strict model structure is injective with respect to strict cofibrations by the strict model structure; and it is a stable equivalence by item 1 of prop. \ref{StableEquivalencesBetweenOmegaSpectraAreStrictWeakEquivalences}.

Conversely, a morphism injective with respect to strict cofibrations that are stable equivalences is a $K$-[[injective morphism]] by corollary \ref{KInjectivesAreIndeedTheStableFibrations}, and hence if it is also a stable equivalence then by lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalences} it is a strict acylic fibration.

=--

+-- {: .proof #StableModelStructureOnDiagramSpectraProof}
###### Proof
(of theorem \ref{StableModelStructuresOnDiagramSpectra})

The non-trivial points to check are the two [[weak factorization systems]].

That $(cof_{stable}\cap weq_{stable} \;,\; fib_{stable})$ is a weak factorization system follows from lemma \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations} and the [[small object argument]]. 

By lemma \ref{StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations} the stable acyclic fibrations are equivalently the strict acyclic fibrations and hence the weak factorization system $(cof_{stable} \;,\; fib_{stable} \cap we_{stable})$ is identified with that of the strict model structure $(cof_{strict} \;,\; fib_{strict} \cap we_{strict})$.

=--

#### Stable equivalences 
 {#RelatingStableEquivalencesAndStableWeakHomotopyEquivalences}

Here we discuss that the two concepts of _stable equivalences_ and of _stable weak homotopy equivalences_ in def. \ref{StableEquivalencesForDiagramSpectra} actually agree in the cases of a) pre-[[excisive functors]], b) [[orthogonal spectra]] and c) [[sequential spectra]], while in the case of [[symmetric spectra]] the class of stable equivalences includes but is strictly larger than that of stable weak homotopy equivalences.

This is important in practice, since while the stable equivalences are the weak equivalences in the stable model structure of theorem \ref{StableModelStructuresOnDiagramSpectra}, it is the [[stable weak homotopy equivalences]] that are typically more readily identified.


+-- {: .num_theorem #RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra}
###### Theorem

In $\mathbb{S}Mod$, $\mathbb{S}_{Orth} Mod$ and in $\mathbb{S}_{Seq} Mod$ we have for the concepts from def. \ref{StableEquivalencesForDiagramSpectra} that

$$
  stable\;weak\;homotopy\;equivalence 
  \;\Leftrightarrow\;
  stable \; equivalence
  \,.
$$

In $\mathbb{S}_{Sym}Mod$ however we only have

$$
  stable\;weak\;homotopy\;equivalence 
  \;\Rightarrow\;
  stable \; equivalence
$$

but the reverse implication is false.

=--

([MMSS00, prop. 8.7, prop. 8.8](#MMSS00))

We break up this statement below as prop. \ref{StableWeakHomotopyEquivalenceIsStableEquivalence} and prop. \ref{StableEquivalencesThatAreStableWeakHomotopyEquivalences}.

The argument that every stable weak homotopy equivalence is in particular a stable equivalence is fairly formal; this we turn to first in prop. \ref{StableWeakHomotopyEquivalenceIsStableEquivalence} below. The converse statement in prop. \ref{StableEquivalencesThatAreStableWeakHomotopyEquivalences} however relies on explicit analysis of the class $K$ of generating acylic cofibrations in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}. 

+-- {: .num_defn #AKindOfAlmostSpectrification}
###### Definition

For $\lambda_0 \colon F^{dia}_1 S^1 \to F^{dia}_0 S^0$ from lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists}, write

$$
  (X \longrightarrow R X)
    \coloneqq
  F(\lambda_0, X)
$$

for the [[mapping spectrum]] construction out of $\lambda_1$ into $X$.

Write

$$
  R^\infty X
  \coloneqq
  \underset{\longrightarrow}{ho\lim}
  \left(
    X 
     \stackrel{\lambda_0^\ast(X)}{\longrightarrow}
    R X
     \stackrel{R(\lambda_0^\ast(X))}{\longrightarrow}
    R R X  
     \stackrel{R R(\lambda_0^\ast(X))}{\longrightarrow}
    \cdots
  \right)
$$

for the [[homotopy colimit]] over the resulting sequence of iterations (formed with respec to the strict model structure of prop. \ref{StrictModelStructureOnDiagramSpectra}). Write 

$$
  r_X \colon X \longrightarrow R^\infty X
$$

for the 0th-component map into the colimit.

=--


+-- {: .num_lemma #PropertiesOfAKindOfAlmostSpectrification}
###### Lemma

The functor $R^\infty$ from def. \ref{AKindOfAlmostSpectrification} has the following properties.

1. for $E$ an Omega-spectrum according to def. \ref{StableEquivalencesForDiagramSpectra}, then, by lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists}, $\lambda_0^\ast(E)$ is weak equivalence in the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra}), and hence so is $r_E$;

1. for $f\colon X \longrightarrow Y$ a stable weak homotopy equivalence according to def. \ref{StableEquivalencesForDiagramSpectra}, then $R^\infty f \colon R^\infty X \longrightarrow R^\infty Y$ is a weak equivalence in the strict model structure.

=--

([MMSS 00, prop. 8.8](#MMSS00))

+-- {: .proof}
###### Proof

For the first item, use that the [[homotopy colimit]] is represented by the [[mapping telescope]]. Then [this lemma](classical+model+structure+on+topological+spaces#CompactSubsetsAreSmallInCellComplexes) implies that every element of the homotopy groups of the homotopy colimit is represented at some finite stage. This implies that the telescope of level-wise weak homotopy equivalences is a level-wise weak homotopy equivalence.

For the second item, observe that by the defining adjunctions and by lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists} (...) we have

$$
  (R^n X)_q \simeq \Omega^n X(n+q)
$$

and 

$$
  \pi_q((R^\infty X)_n) \simeq \pi_{q-n}(X)
  \,.
$$


=--

+-- {: .num_prop #StableWeakHomotopyEquivalenceIsStableEquivalence}
###### Proposition

In def. \ref{StableEquivalencesForDiagramSpectra} every stable weak homotopy equivalence is a stable equivalence.

=--

([MMSS 00, prop. 8.8](#MMSS00), following [Hovey-Shipley-Smith 00, theorem 3.1.11](#HoveyShipleySmith00))


+-- {: .proof}
###### Proof

Let $E$ be an Omega-spectrum. Then by the first item of lemma \ref{PropertiesOfAKindOfAlmostSpectrification}, for every $X$ the morphism

$$
  [X,r_E]_{strict}
    \;\colon\; 
  [X,E]_{strict} 
    \longrightarrow 
  [X, R^\infty E]_{strict}
$$

is an isomorphism. Since $r_{(-)}$ is a [[natural transformation]] (by def. \ref{AKindOfAlmostSpectrification}), the naturality squares give a factorization of this morphism as

$$
  [X,r_E]_{strict}
    \;\colon\;
  [X,E]_{strict} 
    \stackrel{R^\infty}{\longrightarrow}
  [R^\infty X, R^\infty E]_{strict}
    \stackrel{[r_X,E]_{strict}}{\longrightarrow}
  [X, R^\infty E]_{strict}  
  \,.
$$

Combining this with vertical morphisms as below, which are isomorphisms again by item 1 of lemma \ref{PropertiesOfAKindOfAlmostSpectrification},

$$
  \array{
     &
      &&
    [R^\infty X, E]_{strict}
      &\stackrel{[r_X, E]_{strict}}{\longrightarrow}&
    [X, E]_{strict}  
    \\
    & &\nearrow& 
    {}^{\mathllap{\simeq}}\downarrow^{\mathrlap{[R^\infty X,r_E]_{strict}}} 
     && 
    {}^{\mathllap{\simeq}}\downarrow^{\mathrlap{[X,r_E]_{strict}}}
    \\
    [X,r_E]_{strict}
      \;\colon\;
     &
    [X,E]_{strict} 
      &\stackrel{R^\infty}{\longrightarrow}&
    [R^\infty X, R^\infty E]_{strict}
      &\stackrel{[r_X, R^\infty E]_{strict}}{\longrightarrow}&
    [X, R^\infty E]_{strict}  
  }
$$

exhibits a [[retraction]] 

$$
  id \colon [X,E]_{strict} \longrightarrow [R^\infty X,E]_{strict} \longrightarrow [X,E]_{strict}
  \,,
$$ 

which is natural in $X$ (that the bottom and right composite is indeed the identity is again the naturality of $r_{(-)}$). This naturality now implies a retraction of morphisms

$$
  \array{
    id_{[Y,E]_{strict}} \colon & [Y,E]_{strict} &\longrightarrow& [R^\infty Y,E]_{strict} &\longrightarrow& [Y,E]_{strict}
    \\
    & \downarrow^{\mathrlap{[f,E]_{strict}}} && \downarrow^{\mathrlap{[R^\infty f,E]_{strict}}}
     &&
     \downarrow^{\mathrlap{[f,E]_{strict}}}
    \\
    id_{[X,E]_{strict}} \colon & [X,E]_{strict} &\longrightarrow& [R^\infty X,E]_{strict} &\longrightarrow& [X,E]_{strict}
  }
  \,.
$$

Finally, by the second item of lemma \ref{PropertiesOfAKindOfAlmostSpectrification}, the middle vertical morphism here is an isomorphism, hence $[f^\ast, E]_{strict}$ is the retract of an iso and hence ([here](retract#RetractOfIso)) an isomorphism itself, for all Omega-spectra $E$. This means by definition that $f$ is a stable equivalence.


=--


Now for the converse.



+-- {: .num_prop #StableEquivalencesThatAreStableWeakHomotopyEquivalences}
###### Proposition

In the case $Dia \in \{Top^{\ast/}, Orth, Seq\}$, hence for [[sequential spectra]], [[orthogonal spectra]] and pre-[[excisive functors]], stable equivalences are stable weak homotopy equivalences (def. \ref{StableEquivalencesForDiagramSpectra}).

=--

([MMSS 00, p.31-32](#MMSS00))

+-- {: .proof}
###### Proof idea

By theorem ref. \ref{StableModelStructuresOnDiagramSpectra}, and by lemmas  \ref{KInjectiveStableEquivalencesAreStrictEquivalences} and \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations}, every stable weak equivalence factors as a $K$-[[relative cell complex]] followed by weak equivalence in the strict model structure. Since the latter is degreewise a [[weak homotopy equivalence]] it is in particular a [[stable weak homotopy equivalence]]. Hence we are reduced to showing that every $K$-[[relative cell complex]] is a stable weak homotopy equivalence.

Observe now that we know this to be true for the elements of $K$ itself (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}): first of all, the elements in $F J$ are [[retracts]] of [[deformation retracts]] and therefore [[stable weak homotopy equivalences]]. Second, the morphisms denoted $k_n$ in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}, which resolve the maps $\lambda_n$ from def. \ref{CorepresentationOfAdjunctsOfStructureMaps}, are stable weak homotopy equivalences by lemma \ref{AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences}.  This implies that so are their [[pushout products]] $k_n \Box i$. 

=--

This completes the proof of theorem \ref{RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra}.



#### Quillen equivalences between the stable model structures
 {#QuillenEquivalencesOfStableModelStructures}

+-- {: .num_theorem #QuillenEquivalencesBetweenStableModelStructuresOnDiagramSpectra}
###### Theorem

The sequence of [[Quillen adjunctions]] between the strict model structures of prop. \ref{StrictModelStructureOnDiagramSpectra} remain Quillen adjunctions for the stable model structures of theorem \ref{StableModelStructuresOnDiagramSpectra} and indeed become a sequence of [[Quillen equivalences]] 

$$
 \array{
   && OrthSpec(Top)_{stable} && SymSpec(Top)_{stable} && SeqSpec(Top)_{stable}
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_{stable}
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underoverset{orth^\ast}{\simeq_{Qu}}{\longrightarrow}}&
   \mathbb{S}_{Orth} Mod_{stable}
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underoverset{sym^\ast}{\simeq_{Qu}}{\longrightarrow}}&
   \mathbb{S}_{Sym} Mod_{stable}
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underoverset{seq^\ast}{\simeq_{Qu}}{\longrightarrow}}&
   \mathbb{S}_{Seq} Mod_{stable}
 }
  \,.
$$

=--

([MMSS 00, section 10](#MMSS00))

We give the proof [below](#ProofOfQuillenEquivalencesOfStableModelStructures), after a few preliminaries.


+-- {: .num_lemma #AdjunctionsBetweenDiagramSpectraAreStableQuillenAdjunctions}
###### Lemma

The sequence of adjunctions between the categories $\mathbb{S}_{dia}Mod$ from prop. \ref{SystemOfAdjunctionsForDiagramSpectra} are [[Quillen adjunctions]] with respect to the stable model structures of theorem \ref{StableModelStructuresOnDiagramSpectra}

$$
 \array{
   && OrthSpec(Top)_{stable} && SymSpec(Top)_{stable} && SeqSpec(Top)_{stable}
   \\
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_{stable}
     &\stackrel{\overset{orth_!}{\longleftarrow}}{\underoverset{orth^\ast}{}{\longrightarrow}}&
   \mathbb{S}_{Orth} Mod_{stable}
     &\stackrel{\overset{sym_!}{\longleftarrow}}{\underoverset{sym^\ast}{}{\longrightarrow}}&
   \mathbb{S}_{Sym} Mod_{stable}
      &\stackrel{\overset{seq_!}{\longleftarrow}}{\underoverset{seq^\ast}{}{\longrightarrow}}&
   \mathbb{S}_{Seq} Mod_{stable}
 }
 \,.
$$


=--

([MMSS 00, lemma 10.1](#MMSS00))

+-- {: .proof}
###### Proof

By lemma \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations} the stable fibrations are equivalently the $K$-[[injective morphisms]].
By lemma \ref{KInjectivesAreAcyclicCofibrations} these are characterized by data that is preserved by right Quillen functors with respect to the strict model structure. Moreover by lemma \ref{StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations} the stable acyclic fibrations are equivalently the strict acyclic fibrations, which are of course also preserved by right Quillen functors for the strict model structure. Therefore the statement follows with prop. \ref{StrictModelStructureOnDiagramSpectra}.

=--

+-- {: .proof #ProofOfQuillenEquivalencesOfStableModelStructures}
###### Proof idea
(of theorem \ref{QuillenEquivalencesBetweenStableModelStructuresOnDiagramSpectra})

With lemma \ref{AdjunctionsBetweenDiagramSpectraAreStableQuillenAdjunctions} it is sufficient to show that all the total [[derived functors]] are [[adjoint equivalences]]. By [[two-out-of-three]] for Quillen equivalences, it is sufficient to show this for all the (composite) adjunctions whose right adjoint does _not_ point to $\mathbb{S}_{Sym}Mod$.

In these cases, theorem \ref{RelationBetweenStableEquivalencesAndStableWeakHomotopyEquivalencesForDiagramSpectra} implies that the right adjoint functor preserves and reflects weak equivalence (a morphism in its domain is a stable equivalence precisely if its image is).

In such a case, for checking a Quillen equivalence it is sufficient to check that the [[adjunction unit]] is a weak equivalence on all cofibrant objects (...citation...).

Since both adjoints in the present case preserve [[colimits]], [[tensoring]] with $Top^{\ast/}$ and the [[homotopy lifting property]], and since (...)

(...)

(...)

=--



### 11.-16.) Model structures on ring spectra and module spectra
 {#ModelStructuresOnRingSpectraAndModuleSpectra}

#### Monoidal model structure
 {#MonoidalStableModelStructure}


+-- {: .num_theorem}
###### Theorem

The stable model structures from theorem \ref{StableModelStructuresOnDiagramSpectra} on the [[categories of modules]] from prop. \ref{HighlyStructuredSpectraAsDayConvolutionSModules}, remark \ref{PreExcisiveFunctorsAreSModules}

$$
  \mathbb{S}Mod_r \simeq [Top_{fin}^{\ast/}, Top^{\ast/}]
$$

$$
  \mathbb{S}_{Orth} Mod_r \simeq OrthSpec(Top)
$$

$$
  \mathbb{S}_{Sym} Mod_r \simeq SymSpec(Top)
$$

are compatible with their [[monoidal category]] structure given by the [[symmetric monoidal smash product of spectra]] $\wedge$ of def. \ref{SymmetricSmashProductOfDiagramSpectra}, in that $(\mathbb{S}_{dia} Mod_{stable}, \wedge_{\mathbb{S}_{dia}})$ in these cases

1. is a [[stable model category]];

1. satisfying the [[monoid axiom in a monoidal model category]].

=--

([MMSS 00, theorem 12.1 (iii) with prop. 12.3](#MMSS00)) 

We give the proof below (...) after a sequence of lemmas.

+-- {: .num_lemma #PushoutSmashProductOfStableCofibsIsStableCofib}
###### Lemma

The [[pushout product]] of two cofibrations in $\mathbb{S}_{dia}Mod_{stable}$ is again a cofibration.

=--

+-- {: .proof}
###### Proof

A general abstract fact about [[pushout-products]] ([Hovey-Shipley-Smith 00, prop. 5.3.4](#HoveyShipleySmith00), see _[here](pushout-product#PushoutProductOfCofClassIsCofClassOfPushoutProduct)_) is that for $I_1, I_2$ two classes of morphisms in a [[symmetric monoidal category|closed]] [[symmetric monoidal category]] with [[finite limits]] and [[finite colimits]], and writing $I_i Cof$ for their saturated classes, then under [[pushout-product]] $\Box$:

$$
  (I_1 Cof) \Box (I_2 Cof)
  \subset 
  (I_1 \Box I_2) Cof
  \,.
$$

Since the cofibrations of the stable model structure, theorem \ref{StableModelStructuresOnDiagramSpectra}, are elements in


$$
  Cof_{stable} = (F I) Cof
$$

with $F I$ the class of [[free spectra]] on the class of generating cofibrations $I$ of the [[classical model structure on topological spaces]], def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}, this implies in the present case that 

$$
  Cof_{stable} \Box Cof_{stable}
  \subset
  (F I \Box F I) Cof
  \,.
$$

Now lemma \ref{PushoutSmashProductOfFreeSpectraOnGeneratingCofibrationsOfTop} implies that 

$$
  F I \Box F I
  =
  F(I \Box I)
  =
  F I 
$$

and hence the claim follows.

=--



+-- {: .num_lemma }
###### Lemma

Let $Y \in \mathbb{S}_{dia} Mod_{stable}$ be cofibrant.
Then the [[smash product of spectra]]-[[functor]] (def. \ref{SymmetricSmashProductOfDiagramSpectra})

$$
  X \wedge_{\mathbb{S}_{dia}}(-)
    \;\colon\;
  \mathbb{S}_{dia} Mod
    \longrightarrow
  \mathbb{S}_{dia} Mod
$$

preserves [[stable weak homotopy equivalences]] as well as stable equivalences (def. \ref{StableEquivalencesForDiagramSpectra}).

=--

([MMSS 00, prop. 12.3](#MMSS00))

+-- {: .num_lemma }
###### Lemma

For every $X \in \mathbb{S}_{dia} Mod$, the functor

$$
  X \wedge_{\mathbb{S}_{dia}}(-)
    \;\colon\;
  \mathbb{S}_{dia} Mod
    \longrightarrow
  \mathbb{S}_{dia} Mod
$$

sends acylic cofibrations in the stable model structure to morphisms that are stable equivalences and [[h-cofibrations]].

=--

([MMSS 00, prop. 12.5](#MMSS00))

+-- {: .num_prop #StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom}
###### Proposition

The [[symmetric monoidal smash product of spectra]] $\wedge_{\mathbb{S}_{dia}}$ on $\mathbb{S}_{dia} Mod$, def. \ref{SymmetricSmashProductOfDiagramSpectra} satisfies the [[pushout-product axiom]] with respect to the stable model structure $\mathbb{S}_{dia} Mod$ of theorem \ref{StableModelStructuresOnDiagramSpectra}.

=--

([MMSS 00, prop. 12.6](#MMSS00))

+-- {: .proof}
###### Proof

That the pushout product of two stable cofibrations is again a stable cofibration is the content of lemma \ref{PushoutSmashProductOfStableCofibsIsStableCofib}. It remains to show that if at least one of them is a stanble equivalence, def. \ref{StableEquivalencesForDiagramSpectra}, then so is the pushout-product.
That follows with a laborious argument using the above lemmas (...).

=--

(...)



### 17.-18.) Relation to $\Gamma$-spaces

(...)

### 19.) Simplicial and topological diagram spectra

(...)

## Part III. Symmetric monoidal categories and FSPs


### Topological ends and coends
 {#TopologicalEndsAndCoends}

For working with pointed [[topologically enriched functors]], a certain shape of [[limits]]/[[colimits]] is particularly relevant: these are called (pointed topological enriched) _[[ends]]_ and _[[coends]]_. We here introduce these and then derive some of their basic properties, such as notably the expression for topological [[left Kan extension]] in terms of [[coends]] (prop. \ref{TopologicalLeftKanExtensionBCoend} below). Further below it is via left Kan extension along the ordinary smash product of pointed topological spaces ("[[Day convolution]]") that the [[symmetric monoidal smash product of spectra]] is induced.

+-- {: .num_defn #OppositeAndProductOfPointedTopologicallyEnrichedCategory}
###### Definition

Let $\mathcal{C}, \mathcal{D}$ be pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)), i.e. [[enriched categories]] over $(Top_{cg}^{\ast/}, \wedge, S^0)$ from example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}. 

1. The **pointed topologically enriched [[opposite category]]** $\mathcal{C}^{op}$ is the [[topologically enriched category]] with the same [[objects]] as $\mathcal{C}$, with [[hom-spaces]]

   $$
     \mathcal{C}^{op}(X,Y)
     \coloneqq
     \mathcal{C}(Y,X) 
   $$

   and with [[composition]] given by [[braiding]] followed by the composition in $\mathcal{C}$:

   $$
     \mathcal{C}^{op}(X,Y)
     \wedge
     \mathcal{C}^{op}(Y,Z)
     =
     \mathcal{C}(Y,X)\wedge \mathcal{C}(Z,Y)
     \underoverset{\simeq}{\tau}{\longrightarrow}
     \mathcal{C}(Z,Y) \wedge \mathcal{C}(Y,X)
       \overset{\circ_{Z,Y,X}}{\longrightarrow}
     \mathcal{C}(Z,X)
     =
     \mathcal{C}^{op}(X,Z) 
     \,.
   $$

1. the **pointed topological [[product category]]** $\mathcal{C} \times \mathcal{D}$ is the [[topologically enriched category]] whose [[objects]] are [[pairs]] of objects $(c,d)$ with $c \in \mathcal{C}$ and $d\in \mathcal{D}$, whose [[hom-spaces]] are the [[smash product]] of the separate hom-spaces

   $$
     (\mathcal{C}\times \mathcal{D})((c_1,d_1),\;(c_2,d_2) )
       \coloneqq
     \mathcal{C}(c_1,c_2)\wedge \mathcal{D}(d_1,d_2)
   $$

   and whose [[composition]] operation is the [[braiding]] followed by the [[smash product]] of the separate composition operations:

   $$
     \array{
       (\mathcal{C}\times \mathcal{D})((c_1,d_1), \; (c_2,d_2))
         \wedge
       (\mathcal{C}\times \mathcal{D})((c_2,d_2), \; (c_3,d_3))
       \\
       {}^{\mathllap{=}}\downarrow
       \\
       \left(\mathcal{C}(c_1,c_2) \wedge \mathcal{D}(d_1,d_2)\right)
         \wedge
       \left(\mathcal{C}(c_2,c_3) \wedge \mathcal{D}(d_2,d_3)\right)
       \\
       \downarrow^{\mathrlap{\tau}}_{\mathrlap{\simeq}}
       \\
       \left(\mathcal{C}(c_1,c_2)\wedge \mathcal{C}(c_2,c_3)\right)
         \wedge
       \left( \mathcal{D}(d_1,d_2)\wedge \mathcal{D}(d_2,d_3)\right)
         &\overset{
             (\circ_{c_1,c_2,c_3})\wedge (\circ_{d_1,d_2,d_3})
           }{\longrightarrow}
         &
       \mathcal{C}(c_1,c_3)\wedge \mathcal{D}(d_1,d_3)
       \\
       && \downarrow^{\mathrlap{=}}
       \\
       && (\mathcal{C}\times \mathcal{D})((c_1,d_1),\; (c_3,d_3))
     }
    \,.
   $$

=--

+-- {: .num_example #PointedTopologicalFunctorOnProductCategory}
###### Example

A pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) into $Top^{\ast/}_{cg}$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) out of a pointed topological [[product category]] as in def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory} 

$$
  F 
    \;\colon\;
  \mathcal{C} \times \mathcal{D}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

(a "pointed topological [[bifunctor]]") has component maps of the form

$$
  F_{(c_1,d_1),(c_2,d_2)}
    \;\colon\;
  \mathcal{C}(c_1,c_2)
  \wedge
  \mathcal{D}(d_1,d_2)
    \longrightarrow
  Maps(F_0((c_1,d_1)),F_0((c_2,d_2)))_\ast
  \,.
$$

By functoriallity and under passing to [[adjuncts]] ([cor.](Introduction+to+Stable+homotopy+theory+--+P#SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces)) this is equivalent to two commuting _[[actions]]_


$$
  \rho_{c_1,c_2}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \wedge F_0((c_1,d)) 
    \longrightarrow
  F_0((c_2,d))
$$

and

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{D}(d_1,d_2) \wedge F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$

In the special case of a functor out of the [[product category]] of some $\mathcal{C}$ with its [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory})

$$
  F 
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

then this takes the form

$$
  \rho_{c_2,c_1}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \wedge F_0((c_2,d)) 
    \longrightarrow
  F_0((c_1,d))
$$

and

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{C}(d_1,d_2) \wedge F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$


=--


+-- {: .num_defn #EndAndCoendInTopcgSmash}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)), i.e. an [[enriched category]] over $(Top_{cg}^{\ast/}, \wedge, S^0)$ from example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}. Let

$$
  F 
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

be a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) out of the pointed topological [[product category]] of $\mathcal{C}$ with its [[opposite category]], according to def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}.


1. The  **[[coend]]** of $F$, denoted $\overset{c \in \mathcal{C}}{\int} F(c,c)$, is the [[coequalizer]] in $Top_{cg}^{\ast}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [exmpl.](Introduction+to+Stable+homotopy+theory+--+P#CoequalizerInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) of the two actions encoded in $F$ via example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c,d \in \mathcal{C})}{\coprod} \mathcal{C}(c,d) \wedge F(c,d)
      \underoverset
        {\underset{\underset{c,d}{\sqcup} \rho_{(d,c)}(c) }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \rho_{(c,d)}(d) }{\longrightarrow}}
        {\phantom{AAAAAAAA}}
     \underset{c \in \mathcal{C}}{\coprod} F(c,c)
      \overset{coeq}{\longrightarrow}
     \overset{c\in \mathcal{C}}{\int} F(c,c)
     \,.
   $$

1. The **[[end]]** of $F$, denoted $\underset{c\in \mathcal{C}}{\int} F(c,c)$, is the **[[equalizer]]** in $Top_{cg}^{\ast/}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [exmpl.](Introduction+to+Stable+homotopy+theory+--+P#EqualizerInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) of the [[adjuncts]] of the two actions encoded in $F$ via example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c\in \mathcal{C}}{\int} F(c,c)
       \overset{\;\;equ\;\;}{\longrightarrow}
     \underset{c \in \mathcal{C}}{\prod} F(c,c)
      \underoverset   
        {\underset{\underset{c,d}{\sqcup} \tilde \rho_{(c,d)}(d)  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \tilde\rho_{d,c}(c)}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
      \underset{c\in \mathcal{C}}{\prod}
      Maps\left( \mathcal{C}\left(c,d\right), \;  F\left(c,d\right) \right)_\ast
     \,.
   $$

=--

+-- {: .num_example #NaturalTransformationsViaEnds}
###### Example

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For 
$
  F,G
  \;\colon\;
  \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$
two pointed [[topologically enriched functors]], then the [[end]] (def. \ref{EndAndCoendInTopcgSmash}) of $Maps(F(-),G(-))_\ast$ is a topological space whose underlying [[pointed set]] is the pointed set of [[natural transformations]] $F\to G$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor))

$$
  U
  \left(
    \underset{c \in \mathcal{C}}{\int} Maps(F(c),G(c))_\ast
  \right)
  \;\simeq\;
  Hom_{[\mathcal{C},Top^{\ast/}_{cg}]}(F,G)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The underlying pointed set functor $U\colon Top^{\ast/}_{cg}\to Set^{\ast/}$ [[preserved limit|preserves]] all [[limits]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [prop.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)). Therefore there is an [[equalizer]] diagram in $Set^{\ast/}$ of the form

$$
  U
  \left(
    \underset{c\in \mathcal{C}}{\int}
    Maps(F(c),G(c))_\ast
  \right)
    \overset{equ}{\longrightarrow}
  \underset{c\in \mathcal{C}}{\prod} Hom_{Top^{\ast/}_{cg}}(F(c),G(c))
      \underoverset   
        {\underset{\underset{c,d}{\sqcup} U(\tilde \rho_{(c,d)}(d))  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} U(\tilde\rho_{d,c}(c))}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
   \underset{c,d\in \mathcal{C}}{\prod}
    Hom_{Top^{\ast/}_{cg}}(
      \mathcal{C}(c,d),
      Maps(F(c),G(d))_\ast
    )
  \,.
$$

Here the object in the middle is just the set of collections of component morphisms $\left\{ F(c)\overset{\eta_c}{\to} G(c)\right\}_{c\in \mathcal{C}}$. The two parallel maps in the equalizer diagram take such a collection to the functions which send any $c \overset{f}{\to} d$ to the result of precomposing

$$
  \array{
    F(c)
    \\
    {}^{\mathllap{f(f)}}\downarrow
    \\
    F(d) &\underset{\eta_d}{\longrightarrow}& G(d)
  }
$$

and of postcomposing

$$
  \array{
    F(c) &\overset{\eta_c}{\longrightarrow}& G(c)
    \\
    && \downarrow^{\mathrlap{G(f)}}
    \\
    && G(d)
  }
$$

each component in such a collection, respectively. These two functions being equal, hence the collection $\{\eta_c\}_{c\in \mathcal{C}}$ being in the equalizer, means precisley that for all $c,d$ and all $f\colon c \to d$ the square

$$
  \array{
    F(c) &\overset{\eta_c}{\longrightarrow}& G(c)
    \\
    {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{G(f)}}
    \\
    F(d) &\underset{\eta_d}{\longrightarrow}& G(g)
  }
$$

is a [[commuting square]]. This is precisley the condition that the collection $\{\eta_c\}_{c\in \mathcal{C}}$ be a [[natural transformation]].

=--

Conversely, example \ref{NaturalTransformationsViaEnds} says that [[ends]] over [[bifunctors]] of the form $Maps(F(-),G(-)))_\ast$ constitute [[hom-spaces]] between pointed [[topologically enriched functors]]:

+-- {: .num_defn #PointedTopologicalFunctorCategory}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). Define the structure of a pointed [[topologically enriched category]] on the category $[\mathcal{C}, Top_{cg}^{\ast/}]$ of pointed [[topologically enriched functors]] to $Top^{\ast/}_{cg}$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) by taking the [[hom-spaces]] to be given by the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) of example \ref{NaturalTransformationsViaEnds}:

$$
  [\mathcal{C},Top^{\ast/}_{cg}](F,G)
    \;\coloneqq\;
  \int_{c\in \mathcal{C}} Maps(F(c),G(c))_\ast
$$

and by taking the composition maps to be the morphisms induced by the maps

$$
  \left(
    \underset{c\in \mathcal{C}}{\int} Maps(F(c),G(c))_\ast
  \right)
  \wedge
  \left(
    \underset{c \in \mathcal{C}}{\int} Maps(G(c),H(c))_\ast
  \right)
    \overset{}{\longrightarrow}
  \underset{c\in \mathcal{C}}{\prod}
    Maps(F(c),G(c))_\ast \wedge Maps(G(c),H(c))_\ast
  \overset{(\circ_{F(c),G(c),H(c)})_{c\in \mathcal{C}}}{\longrightarrow}
  \underset{c \in \mathcal{C}}{\prod}
    Maps(F(c),H(c))_\ast
$$

by observing that these equalize the two actions in the definition of the [[end]].

The resulting pointed [[topologically enriched category]] $[\mathcal{C},Top^{\ast/}_{cg}]$ is also called the **$Top^{\ast/}_{cg}$-[[enriched functor category]]** over $\mathcal{C}$ with coefficients in $Top^{\ast/}_{cg}$.

=--

First of all this yields a concise statement of the pointed topologically [[enriched Yoneda lemma]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedYonedaLemma))

+-- {: .num_prop #YonedaReductionTopological}
###### Proposition
**(topologically [[enriched Yoneda lemma]])**

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For $F \colon \mathcal{C}\to Top^{\ast/}_{cg}$ a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) and for $c\in \mathcal{C}$ an object, there is a [[natural isomorphism]]

$$
  [\mathcal{C}, Top^{\ast/}_{cg}](\mathcal{C}(c,-),\; F)
  \;\simeq\;
  F(c)
$$

between the [[hom-space]] of the pointed topological functor category, according to def. \ref{PointedTopologicalFunctorCategory}, from the [[representable functor|functor represented]] by $c$ to $F$, and the value of $F$ on $c$.

In terms of the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) defining these [[hom-spaces]], this means that

$$
  \underset{d\in \mathcal{C}}{\int} Maps(\mathcal{C}(c,d), F(d))_\ast
    \;\simeq\;
  F(c)
  \,.
$$

In this form the statement is also known as **[[Yoneda reduction]]**.

=--

The **proof** of prop. \ref{YonedaReductionTopological} is essentially dual to the proof of the next prop. \ref{TopologicalCoYonedaLemma}.

Now that [[natural transformations]] are phrased in terms of [[ends]] (example \ref{NaturalTransformationsViaEnds}), as is the Yoneda lemma (prop. \ref{YonedaReductionTopological}), it is natural to consider the [[formal duality|dual]] statement involvng [[coends]]:

+-- {: .num_prop #TopologicalCoYonedaLemma}
###### Proposition
**([[co-Yoneda lemma]])**

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For $F \colon \mathcal{C}\to Top^{\ast/}_{cg}$ a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) and for $c\in \mathcal{C}$ an object, there is a [[natural isomorphism]]

$$
  F(-)
    \simeq
  \overset{c \in \mathcal{C}}{\int}
  \mathcal{C}(c,-) \wedge F(c)
  \,.
$$

Moreover, the morphism that hence exhibits $F(c)$ as the [[coequalizer]] of the two morphisms in def. \ref{EndAndCoendInTopcgSmash} is componentwise the canonical action 

$$
  \mathcal{C}(d,c) \wedge F(c)
   \longrightarrow
  F(d)
$$

which is [[adjunct]] to the component map $\mathcal{C}(d,c) \to Maps(F(c),F(d))_{\ast}$ of the [[topologically enriched functor]] $F$.

=--

(e.g. [MMSS 00, lemma 1.6](#MMSS00))

+-- {: .proof}
###### Proof

The coequalizer of pointed topological spaces that we need to consider has underlying it a coequalizer of underlying pointed sets  ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [prop.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)). That in turn is the colimit over the diagram of underlying sets with the basepointe adjoined to the diagram ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects)). For a coequalizer diagram adding that extra point to the diagram clearly does not change the colimit, and so we need to consider the plain coequalizer of sets.

That is just the set of [[equivalence classes]] of [[pairs]]

$$
  ( c \overset{}{\to} c_0,\; x \in F(c) )
  \,,
$$

where two such pairs

$$
  ( c \overset{f}{\to} c_0,\; x \in F(c) )
  \,,\;\;\;\;
  ( d \overset{g}{\to} c_0,\; y \in F(d) )  
$$

are regarded as equivalent if there exists

$$
  c \overset{\phi}{\to} d
$$

such that 

$$
  f = g \circ \phi
  \,,
  \;\;\;\;\;and\;\;\;\;\;
  y = \phi(x)
  \,.
$$

(Because then the two pairs are the two images of the pair $(g,x)$ under the two morphisms being coequalized.)

But now considering the case that $d = c_0$ and $d = id_{c_0}$, so that $f = \phi$ shows that any pair

$$
  ( c \overset{\phi}{\to} c_0, \; x \in F(c))
$$

is identified, in the coequalizer, with the pair

$$
  (id_{c_0},\; \phi(x) \in F(c_0))
  \,,
$$ 

hence with $\phi(x)\in F(c_0)$. 

This shows the claim at the level of the underlying sets. To conclude it is now sufficient ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop)) to show that the topology on $F(c_0) \in Top^{\ast/}_{cg}$ is the [[final topology]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#InitialAndFinalTopologies)) of the system of component morphisms

$$
  \mathcal{C}(d,c) \wedge F(c)
    \longrightarrow
  \underset{c}{\int} \mathcal{C}(c,c_0) \wedge F(c)
$$

which we just found. But that system includes 

$$
  \mathcal{C}(c,c) \wedge F(c) \longrightarrow F(c)
$$

which is a [[retraction]]

$$
  id \;\colon\; F(c) \longrightarrow \mathcal{C}(c,c) \wedge F(c)
  \longrightarrow F(c)
$$

and so if all the preimages of a given subset of the coequalizer under these component maps is open, it must have already been open in $F(c)$.


=--


+-- {: .num_remark}
###### Remark

The statement of the [[co-Yoneda lemma]] in prop. \ref{TopologicalCoYonedaLemma} is a kind of [[categorification]] of the following statement in [[analysis]] (whence the notation with the integral signs):

For $X$ a [[topological space]], $f \colon X \to\mathbb{R}$ a [[continuous function]] and $\delta(-,x_0)$ denoting the [[Dirac distribution]], then

$$
  \int_{x \in X} \delta(x,x_0) f(x)
  = 
  f(x_0)
  \,.
$$

=--

It is this analogy that gives the name to the following statement:

+-- {: .num_prop #CoendsCommuteWithEachOther}
###### Proposition
**([[Fubini theorem]] for (co)-ends)**

For $F$ a pointed topologically enriched [[bifunctor]] on a small pointed topological [[product category]] $\mathcal{C}_1 \times \mathcal{C}_2$ (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), i.e.

$$
   F 
  \;\colon\;
  \left(
    \mathcal{C}_1\times\mathcal{C}_2
  \right)^{op}
  \times
  (\mathcal{C}_1 \times\mathcal{C}_2)
  \longrightarrow
  Top^{\ast/}_{cg}
$$

then its [[end]] and [[coend]] (def. \ref{EndAndCoendInTopcgSmash}) is equivalently formed consecutively over each variable, in either order:

$$
  \overset{(c_1,c_2)}{\int} F((c_1,c_2), (c_1,c_2))
  \simeq
  \overset{c_1}{\int}
  \overset{c_2}{\int}
  F((c_1,c_2), (c_1,c_2))
  \simeq
  \overset{c_2}{\int}
  \overset{c_1}{\int}
  F((c_1,c_2), (c_1,c_2))
$$

and

$$
  \underset{(c_1,c_2)}{\int} F((c_1,c_2), (c_1,c_2))
  \simeq
  \underset{c_1}{\int}
  \underset{c_2}{\int}
  F((c_1,c_2), (c_1,c_2))
  \simeq
  \underset{c_2}{\int}
  \underset{c_1}{\int}
  F((c_1,c_2), (c_1,c_2))
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because [[limits]] commute with limits, and [[colimits]] commute with colimits.

=--



+-- {: .num_remark #MappingSpacePreservesEnds}
###### Remark

Because the pointed compactly generated [[mapping space]] functor ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace)) 

$$
  Maps(-,-)_\ast
  \;\colon\;
  \left(Top^{\ast/}_{cg}\right)^{op}
  \times
  Top^{\ast/}_{cg}
  \longrightarrow
  Top^{\ast/}_{cg}
$$

takes [[colimits]] in the first argument and [[limits]] in the second argument to limits ([cor.](Introduction+to+Stable+homotopy+theory+--+P#MappingSpacesSendsColimitsInFirstArgumentToLimits)), it also takes [[coends]] in the first argument and [[ends]] in the second argument, to ends (def. \ref{EndAndCoendInTopcgSmash}):

$$
  Maps( X, \; \int_{c} F(c,c))_\ast
  \simeq
  \int_c Maps(X, F(c,c)_\ast)
$$

and

$$
  Maps( \int^{c} F(c,c),\; Y  )_\ast
  \simeq
  \underset{c}{\int} Maps( F(c,c),\; Y )_\ast
  \,.
$$

=--

+-- {: .num_prop #TopologicalLeftKanExtensionBCoend}
###### Proposition
**(left Kan extension via coends)**

Let $\mathcal{C}, \mathcal{D}$ be [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) and let 

$$
  p \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
$$

be a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)). Then precomposition with $p$ constitutes a functor

$$
  p^\ast 
  \;\colon\;
  [\mathcal{D}, Top^{\ast/}_{cg}]
  \longrightarrow
  [\mathcal{C}, Top^{\ast/}_{cg}]
$$

$G\mapsto G\circ p$. This functor has a [[left adjoint]] $Lan_p$, called **left [[Kan extension]]** along $p$

$$
  [\mathcal{D}, Top^{\ast/}_{cg}]
    \underoverset
      {\underset{p^\ast}{\longrightarrow}}
      {\overset{Lan_p }{\longleftarrow}}
      {\bot}
  [\mathcal{C}, Top^{\ast/}_{cg}]
$$

which is given objectwise by a [[coend]] (def. \ref{EndAndCoendInTopcgSmash}):

$$
  (Lan_p F)
  \;\colon\;
  c 
  \;\mapsto \;
  \overset{c\in \mathcal{C}}{\int}
   \mathcal{D}(p(c),d) \wedge F(c)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Use the expression of natural transformations in terms of ends (example \ref{NaturalTransformationsViaEnds} and def. \ref{PointedTopologicalFunctorCategory}), then use the respect of $Maps(-,-)_\ast$ for ends/coends (remark \ref{MappingSpacePreservesEnds}),  use the smash/mapping space adjunction ([cor.](Introduction+to+Stable+homotopy+theory+--+P#SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces)), use the [[Fubini theorem]] (prop. \ref{CoendsCommuteWithEachOther}) and finally use [[Yoneda reduction]] (prop. \ref{YonedaReductionTopological}) to obtain a sequence of [[natural isomorphisms]] as follows:

$$
  \begin{aligned}
    [\mathcal{D},Top^{\ast/}_{cg}]( Lan_p F, \, G )
    & =
   \underset{d \in \mathcal{D}}{\int}
    Maps( (Lan_p F)(d), \, G(d) )_\ast
   \\
   & =
   \underset{d\in \mathcal{D}}{\int}
   Maps\left(
     \overset{c \in \mathcal{C}}{\int} \mathcal{D}(p(c),d) \wedge F(c)
     ,\;
     G(d)
   \right)_\ast
    \\
  &\simeq
  \underset{d \in \mathcal{D}}{\int}
  \underset{c \in \mathcal{C}}{\int}
  Maps(
    \mathcal{D}(p(c),d)\wedge F(c) \,,\; G(d)
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  \underset{d\in \mathcal{D}}{\int}
  Maps(F(c), 
    Maps(
     \mathcal{D}(p(c),d) , \, G(d)
    )_\ast
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  Maps(F(c), 
   \underset{d\in \mathcal{D}}{\int}
   Maps(
    \mathcal{D}(p(c),d) , \, G(d)
   )_\ast
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  Maps(F(c), G(p(c))
  )_\ast  
  \\
  & =
  [\mathcal{C}, Top^{\ast/}_{cg}](F,p^\ast G)
  \end{aligned}
  \,.
$$

=--

### Monoidal topological categories

We recall the basic definitions of [[monoidal categories]] and of [[monoid in a monoidal category|monoids]] and [[module object|modules]] [[internalization|internal]] to monoidal categories. All examples are at the end of this section, starting with example \ref{TopAsASymmetricMonoidalCategory} below.

+-- {: .num_defn #MonoidalCategory} 
###### Definition

A **(pointed) [[topologically enriched category|topologically enriched]] [[monoidal category]]** is a (pointed) [[topologically enriched category]] $\mathcal{C}$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) equipped with 

1. a (pointed) [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor))

   $$ 
      \otimes 
        \;\colon\; 
      \mathcal{C} \times \mathcal{C}  
       \longrightarrow
      \mathcal{C}
   $$

   out of the (pointed) topologival [[product category]] of $\mathcal{C}$ with itself (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), called the **[[tensor product]]**, 

1. an object

   $$ 
     1 \in \mathcal{C} 
   $$

   called the **[[unit object]]** or **[[tensor unit]]**, 

1. a [[natural isomorphism]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor))

   $$
     a 
       \;\colon\; 
     ((-)\otimes (-)) \otimes (-)
       \overset{\simeq}{\longrightarrow}
     (-) \otimes ((-)\otimes(-))
   $$

   called the **[[associator]]**, 

1. a [[natural isomorphism]] 

   $$
     \ell
       \;\colon\; 
     (1 \otimes (-)) 
       \overset{\simeq}{\longrightarrow}
     (-)
   $$

   called the **[[left unitor]]**, and a natural isomorphism 

   $$
     r \;\colon\; (-) \otimes 1 \overset{\simeq}{\longrightarrow} (-)
   $$

   called the **[[right unitor]]**, 

such that the following two kinds of [[commuting diagram|diagrams commute]], for all objects involved:

1. **triangle identity**:

   $$
     \array{
        & (x \otimes 1) \otimes y &\stackrel{a_{x,1,y}}{\longrightarrow} & x \otimes (1 \otimes y)
         \\     
         & {}_{\rho_x \otimes 1_y}\searrow       
         && \swarrow_{1_x \otimes \lambda_y}
         & 
        \\
        &&
        x \otimes y
        &&
     }
   $$


1. the **[[pentagon identity]]**:

+-- {: style="text-align:center"}
[[!include monoidal category > pentagon]]
=--


=--


+-- {: .num_defn #BraidedMonoidalCategory} 
###### Definition

A **(pointed) [[topologically enriched category|topological]] [[braided monoidal category]]**, is a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]]

$$ 
  \tau_{x,y} \colon x \otimes y \to y \otimes x 
$$

called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved:

$$
  \array{
   (x \otimes y) \otimes z 
   &\stackrel{a_{x,y,z}}{\to}&
   x \otimes (y \otimes z)
   &\stackrel{\tau_{x,y \otimes z}}{\to}&
   (y \otimes z) \otimes x
   \\
   \downarrow^{\tau_{x,y}\otimes Id}
   &&&&
   \downarrow^{a_{y,z,x}}
   \\
   (y \otimes x) \otimes z
   &\stackrel{a_{y,x,z}}{\to}&
   y \otimes (x \otimes z)
   &\stackrel{Id \otimes \tau_{x,z}}{\to}&
   y \otimes (z \otimes x)
  }
$$

and

$$
  \array{
   x \otimes (y \otimes z) 
   &\stackrel{a^{-1}_{x,y,z}}{\to}&
   (x \otimes y) \otimes z
   &\stackrel{\tau_{x \otimes y, z}}{\to}&
   z \otimes (x \otimes y)
   \\
   \downarrow^{Id \otimes \tau_{y,z}}
   &&&&
   \downarrow^{a^{-1}_{z,x,y}}
   \\
   x \otimes (z \otimes y)
   &\stackrel{a^{-1}_{x,z,y}}{\to}&
   (x \otimes z) \otimes y
   &\stackrel{\tau_{x,z} \otimes Id}{\to}&
   (z \otimes x) \otimes y
  }
  \,,
$$

where $a_{x,y,z} \colon (x \otimes y) \otimes z \to x \otimes (y \otimes z)$ denotes the components of the [[associator]] of $\mathcal{C}^\otimes$. 

=--

+-- {: .num_defn #SymmetricMonoidalCategory} 
###### Definition

A **(pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]]** is a (pointed) topological [[braided monoidal category]] (def. \ref{BraidedMonoidalCategory}) for which the [[braiding]] 

$$ 
   \tau_{x,y} \colon x \otimes y \to y \otimes x 
$$

satisfies the condition:

$$ 
  \tau_{y,x} \circ \tau_{x,y} = 1_{x \otimes y}  
$$

for all objects $x, y$

=--

+-- {: .num_defn #ClosedMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $\mathcal{C}$ with [[tensor product]] $\otimes$ (def. \ref{SymmetricMonoidalCategory}) it is called a **[[closed monoidal category]]** if for each $X\in \mathcal{X}$ the functor $X \otimes(-)\simeq (-)\otimes X$ has a [[right adjoint]], denoted

$$
  \mathcal{C}
    \underoverset
      {\underset{[X,-]}{\longrightarrow}}
      {\overset{X\otimes(-)}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,.
$$

For any other object $Y$, the object $[X,Y] \in \mathcal{C}$ is then called the **[[internal hom]]** object between $X$ and $Y$. 

=--

+-- {: .num_example #TopAsASymmetricMonoidalCategory} 
###### Example

The category [[Set]] of [[sets]] and [[functions]] between them, regarded as enriched in [[discrete topological spaces]], becomes a [[symmetric monoidal category]] according to def. \ref{SymmetricMonoidalCategory} with [[tensor product]] the [[Cartesian product]] $\times$ of sets. The [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident (almost unnoticable but nevertheless nontrivial) canonical identifications.

Similarly the $Top_{cg}$ of [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#kTop)) becomes a [[symmetric monoidal category]] with [[tensor product]] the corresponding [[Cartesian products]], hence the operation of forming k-ified ([cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) [[product topological spaces]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#ProductTopologicalSpace)). The underlying functions of the [[associator]], [[unitor]] and [[braiding]] isomorphisms are just those of the underlying sets, as above. 
 
Symmetric monoidal categories, such as these, for which the tensor product is the [[Cartesian product]] are called _[[Cartesian monoidal categories]]_.

=--

+-- {: .num_example #PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory} 
###### Example

The category $Top_{cg}^{\ast/}$ of [[pointed topological space|pointed]] [[compactly generated topological spaces]] with [[tensor product]] the  [[smash product]] $\wedge$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects)) 

$$
  X \wedge Y \coloneqq \frac{X\times Y}{X\vee Y}
$$

is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) with [[unit object]] the pointed [[0-sphere]] $S^0$.

The components of the [[associator]], the [[unitors]] and the [[braiding]] are those of [[Top]] as in example \ref{TopAsASymmetricMonoidalCategory}, descended to the [[quotient topological spaces]] which appear in the definition of the [[smash product]]). This works for pointed [[compactly generated spaces]] (but not for general pointed topological spaces) by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductInTopcgIsAssociative).

=--


+-- {: .num_example #ExampleAbelianGroupsOfMonoidalCategory}
###### Example

The category [[Ab]] of [[abelian groups]], regarded as enriched in [[discrete topological spaces]], becomes a [[symmetric monoidal category]] with tensor product the actual [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ and with [[tensor unit]] the additive group $\mathbb{Z}$ of [[integers]]. Again the [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident ones coming from the underlying sets, as in example \ref{TopAsASymmetricMonoidalCategory}.

This is the archetypical case that motivates the notation "$\otimes$" for the pairing operation in a [[monoidal category]]: 

1. A [[monoid in a monoidal category|monoid in]] $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[ring]]. 

1. A [[commutative monoid in a symmetric monoidal category|commutative monoid in]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[commutative ring]] $R$.

1. An $R$-[[module object]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{ModulesInMonoidalCategory}) is equivalently an $R$-[[module]];

1. The tensor product of $R$-module objects (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[tensor product of modules]].

1. The [[category of modules|category of module objects]] $R Mod(Ab)$ (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[category of modules]] $R Mod$.

=--

+-- {: .num_defn #LaxMonoidalFunctor}
###### Definition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two (pointed) [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}). A topologically enriched **lax monoidal functor** between them is

1. a [[topologically enriched functor]] 

   $$
     F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,,
   $$

1. a morphism

   $$
     \epsilon \;\colon\; 1_{\mathcal{D}} \longrightarrow F(1_{\mathcal{C}})
   $$  

1. a [[natural transformation]]

   $$
     \mu_{x,y} 
       \;\colon\; 
     F(x) \otimes_{\mathcal{D}} F(y) 
       \longrightarrow 
     F(x \otimes_{\mathcal{C}} y)
   $$

   for all $x,y \in \mathcal{C}$

satisfying the following conditions:

1. **([[associativity]])** For all objects $x,y,z \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (F(x) \otimes_{\mathcal{D}} F(y)) \otimes_{\mathcal{D}} F(Z)
         &\underoverset{\simeq}{a^{\mathcal{D}}_{F(x),F(y),F(z)}}{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}( F(y)\otimes_{\mathcal{D}} F(z) )
       \\
       {}^{\mathllap{\mu_{x,y} \otimes id}}\downarrow 
         && 
       \downarrow^{\mathrlap{id\otimes \mu_{y,z}}}
       \\
       F(x \otimes_{\mathcal{C}} y) \otimes_{\mathcal{D}} F(z)
        &&
       F(x) \otimes_{\mathcal{D}} ( F(x \otimes_{\mathcal{C}} y) )
       \\
       {}^{\mathllap{\mu_{x \otimes_{\mathcal{C}} y , z} } }\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{ x, y \otimes_{\mathcal{C}} z  }}}
       \\
       F( ( x \otimes_{\mathcal{C}} y ) \otimes_{\mathcal{C}} z  )
         &\underset{F(a^{\mathcal{C}}_{x,y,z})}{\longrightarrow}&
       F( x \otimes_{\mathcal{C}} ( y \otimes_{\mathcal{C}} z ) )
     }
     \,,
   $$

   where $a^{\mathcal{C}}$ and $a^{\mathcal{D}}$ denote the [[associators]] of the monoidal categories;


1. **([[unitality]])** For all $x \in \mathcal{C}$ the following [[commuting diagram|diagrams commutes]]

   $$
     \array{
       1_{\mathcal{D}} \otimes_{\mathcal{D}} F(x)
         &\overset{\epsilon \otimes id}{\longrightarrow}&
       F(1_{\mathcal{C}}) \otimes_{\mathcal{D}} F(x)
       \\
       {}^{\mathllap{\ell^{\mathcal{D}}_{F(x)}}}\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{1_{\mathcal{C}}, x }}}
       \\
       F(x) 
         &\overset{F(\ell^{\mathcal{C}}_x )}{\longleftarrow}&
       F(1 \otimes_{\mathcal{C}} x  )
     }
   $$

   and  

   $$
     \array{
       F(x) \otimes_{\mathcal{D}}  1_{\mathcal{D}}
         &\overset{id \otimes \epsilon }{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}  F(1_{\mathcal{C}}) 
       \\
       {}^{\mathllap{r^{\mathcal{D}}_{F(x)}}}\downarrow 
         && 
       \downarrow^{\mathrlap{\mu_{x, 1_{\mathcal{C}} }}}
       \\
       F(x) 
         &\overset{F(r^{\mathcal{C}}_x )}{\longleftarrow}&
       F(x \otimes_{\mathcal{C}} 1  )
     }
     \,,
   $$

   where $\ell^{\mathcal{C}}$, $\ell^{\mathcal{D}}$, $r^{\mathcal{C}}$, $r^{\mathcal{D}}$ denote the left and right [[unitors]] of the two monoidal categories, respectively.

If $\epsilon$ and alll $\mu_{x,y}$ are [[isomorphisms]], then $F$ is called a **strong monoidal functor**. 

If moreover $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are equipped with the structure of [[braided monoidal categories]] (def. \ref{BraidedMonoidalCategory}), then the lax monoidal functor $F$ is called a **[[braided monoidal functor]]** if in addition the following [[commuting diagram|diagram commutes]] for all objects $x,y \in \mathcal{C}$

$$
  \array{
    F(x) \otimes_{\mathcal{C}} F(y)
      &\overset{\tau^{\mathcal{D}}_{F(x), F(y)}}{\longrightarrow}&
    F(y) \otimes_{\mathcal{D}} F(x)
    \\
    {}^{\mathllap{\mu_{x,y}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{y,x}}}
    \\
    F(x \otimes_{\mathcal{C}} y )
      &\underset{F(\tau^{\mathcal{C}}_{x,y}  )}{\longrightarrow}&
    F( y \otimes_{\mathcal{C}} x )
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

In the literature often the term "monoidal functor" refers by default to what in def. \ref{LaxMonoidalFunctor} is called a strong monoidal functor.  But for the purpose of the discussion of [[functors with smash product]] [below](#FunctorsWithSmashProduct), it is crucial to admit the generality of lax monoidal functors.

If $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) then a braided monoidal functor (def. \ref{LaxMonoidalFunctor}) between them  is often called a **[[symmetric monoidal functor]]**. 

=--

### Algebras and modules
 {#AlgebrasAndModules}


+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, then a **[[monoid in a monoidal category|monoid internal to]]** $(\mathcal{C}, \otimes, 1)$ is

1. an [[object]] $A \in \mathcal{C}$;

1. a morphism $e \;\colon\; 1 \longrightarrow A$ (called the _[[unit]]_)

1. a morphism $\mu \;\colon\; A \otimes A \longrightarrow A$ (called the _product_); 

such that

1. ([[associativity]]) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A\otimes A) \otimes A 
         &\underoverset{\simeq}{a_{A,A,A}}{\longrightarrow}&
       A \otimes (A \otimes A)
         &\overset{A \otimes \mu}{\longrightarrow}&
       A \otimes A
       \\
       {}^{\mathllap{\mu \otimes A}}\downarrow  
         && &&
       \downarrow^{\mathrlap{\mu}}
       \\
       A \otimes A
         &\longrightarrow&
         &\overset{\mu}{\longrightarrow}&
       A
     }
     \,,
   $$

   where $a$ is the associator isomorphism of $\mathcal{C}$;

1. ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \otimes A 
         &\overset{e \otimes id}{\longrightarrow}&
       A \otimes A
         &\overset{id \otimes e}{\longleftarrow}& 
       A \otimes 1
       \\
       & {}_{\mathllap{\ell}}\searrow 
       & \downarrow^{\mathrlap{\mu}} &
       & \swarrow_{\mathrlap{r}}
       \\
       && A
     }
     \,,
   $$

   where $\ell$ and $r$ are the left and right unitor isomorphisms of $\mathcal{C}$.

Moreover, if $(\mathcal{C}, \otimes , 1)$ has the structure of a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) $(\mathcal{C}, \otimes, 1, B)$ with symmetric [[braiding]] $\tau$, then a monoid $(A,\mu, e)$ as above is called a **[[commutative monoid in a symmetric monoidal category|commutative monoid in]]** $(\mathcal{C}, \otimes, 1, B)$ if in addition

* (commutativity) the following [[commuting diagram|diagram commutes]]

  $$
    \array{
      A \otimes A 
        && \underoverset{\simeq}{\tau_{A,A}}{\longrightarrow} &&
      A \otimes A
      \\
      & {}_{\mathllap{\mu}}\searrow && \swarrow_{\mathrlap{\mu}}
      \\
      && A
    }
    \,.
  $$

A [[homomorphism]] of monoids $(A_1, \mu_1, e_1)\longrightarrow (A_2, \mu_2, f_2)$ is a morphism

$$
  f \;\colon\; A_1 \longrightarrow A_2
$$ 

in $\mathcal{C}$, such that the following two [[commuting diagram|diagrams commute]]

$$
  \array{
    A_1 \otimes A_1 
      &\overset{f \otimes f}{\longrightarrow}&
    A_2 \otimes A_2
    \\
    {}^{\mathllap{\mu_1}}\downarrow && \downarrow^{\mathrlap{\mu_2}}
    \\
    A_1 &\underset{f}{\longrightarrow}& A_2
  }
$$

and

$$
  \array{
    1_{\mathcal{c}} &\overset{e_1}{\longrightarrow}& A_1
    \\
    & {}_{\mathllap{e_2}}\searrow & \downarrow^{\mathrlap{f}}
    \\
    && A_2
  }
  \,.
$$

Write $Mon(\mathcal{C}, \otimes,1)$ for the [[category of monoids]] in $\mathcal{C}$, and $CMon(\mathcal{C}, \otimes, 1)$ for its subcategory of commutative monoids.


=--

+-- {: .num_defn #ModulesInMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, and given $(A,\mu,e)$ a [[monoid in a monoidal category|monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), then a **left [[module object]]** in $(\mathcal{C}, \otimes, 1)$ over $(A,\mu,e)$ is

1. an [[object]] $N \in \mathcal{C}$;

1. a [[morphism]] $\rho \;\colon\; A \otimes N \longrightarrow N$ (called the _[[action]]_);

such that 

1. ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \otimes N 
         &\overset{e \otimes id}{\longrightarrow}&
       A \otimes N
       \\
       & {}_{\mathllap{\ell}}\searrow 
       & \downarrow^{\mathrlap{\rho}} 
       \\
       && A
     }
     \,,
   $$

   where $\ell$ is the left unitor isomorphism of $\mathcal{C}$.


1. (action property) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A\otimes A) \otimes N
         &\underoverset{\simeq}{a_{A,A,N}}{\longrightarrow}&
       A \otimes (A \otimes N)
         &\overset{A \otimes \rho}{\longrightarrow}&
       A \otimes N
       \\
       {}^{\mathllap{\mu \otimes N}}\downarrow  
         && &&
       \downarrow^{\mathrlap{\rho}}
       \\
       A \otimes N
         &\longrightarrow&
         &\overset{\rho}{\longrightarrow}&
       N
     }
     \,,
   $$

A [[homomorphism]] of left $A$-module objects 

$$
  (N_1, \rho_1) \longrightarrow (N_2, \rho_2)
$$

is a morphism 

$$
  f\;\colon\; N_1 \longrightarrow N_2
$$

in $\mathcal{C}$, such that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    A\otimes N_1 &\overset{A \otimes f}{\longrightarrow}& A\otimes N_2
    \\
    {}^{\mathllap{\rho_1}}\downarrow 
      && 
    \downarrow^{\mathrlap{\rho_2}}
    \\
    N_1 &\underset{f}{\longrightarrow}& N_2
  }
  \,.
$$

For the resulting **[[category of modules]]** of left $A$-modules in $\mathcal{C}$ with $A$-module homomorphisms between them, we write

$$
  A Mod(\mathcal{C})
  \,.
$$

This is naturally a (pointed) [[topologically enriched category]] itself.

=--

+-- {: .num_defn #TensorProductOfModulesOverCommutativeMonoidObject}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}), given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), and given $(N_1, \rho_1)$ and $(N_2, \rho_2)$ two left $A$-[[module objects]] (def.\ref{MonoidsInMonoidalCategory}), then the **[[tensor product of modules]]** $N_1 \otimes_A N_2$ is, if it exists, the [[coequalizer]]

$$
  N_1 \otimes A \otimes N_2
  \underoverset
    {\underset{\rho_{1}\circ (\tau_{N_1,A} \otimes N_2)}{\longrightarrow}}
    {\overset{N_1 \otimes \rho_2}{\longrightarrow}}
    {\phantom{AAAA}}
  N_1 \otimes N_1
    \overset{coequ}{\longrightarrow}
  N_1 \otimes_A N_2
$$

=--

+-- {: .num_prop #MonoidalCategoryOfModules}
###### Proposition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}), and given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}). If all [[coequalizers]] exist in $\mathcal{C}$, then the [[tensor product of modules]] $\otimes_A$ from def. \ref{TensorProductOfModulesOverCommutativeMonoidObject} makes the [[category of modules]] $A Mod(\mathcal{C})$ into a [[symmetric monoidal category]], $(A Mod, \otimes_A, A)$ with [[tensor unit]] the object $A$ itself.

=--

+-- {: .num_defn #AAlgebra}
###### Definition

Given a [[monoidal category|monoidal]] [[category of modules]] $(A Mod , \otimes_A , A)$ as in prop. \ref{MonoidalCategoryOfModules}, then a [[monoid in a monoidal category|monoid]] $(E, \mu, e)$ in  $(A Mod , \otimes_A , A)$ (def. \ref{MonoidsInMonoidalCategory}) is called an **$A$-[[associative algebra|algebra]]**.

=--

+-- {: .num_prop #AlgebrasOverAAreMonoidsUnderA}
###### Propposition

Given a [[monoidal category|monoidal]] [[category of modules]] $(A Mod , \otimes_A , A)$ in a [[monoidal category]] $(\mathcal{C},\otimes, 1)$ as in prop. \ref{MonoidalCategoryOfModules}, and an $A$-algebra $(E,\mu,e)$ (def. \ref{AAlgebra}), then there is an [[equivalence of categories]]

$$
  A Alg_{comm}(\mathcal{C}) 
    \coloneqq 
  CMon(A Mod)
   \simeq
  CMon(\mathcal{C})^{A/}
$$

between the [[category of commutative monoids]] in $A Mod$ and the [[coslice category]] of commutative monoids in $\mathcal{C}$ under $A$, hence between commutative $A$-algebras in $\mathcal{C}$ and commutative monoids $E$ in $\mathcal{C}$ that are equipped with a homomorphism of monoids $A \longrightarrow E$.

=--

(e.g. [EKMM 97, VII lemma 1.3](#EKMM97))

+-- {: .proof}
###### Proof

In one direction, consider a $A$-algebra $E$ with unit $e_E \;\colon\; A \longrightarrow E$ and product $\mu_{E/A} \colon E \otimes_A E \longrightarrow E$. There is the underlying product $\mu_E$ 

$$
  \array{
    E \otimes A \otimes E
    & 
    \underoverset
      {\underset{}{\longrightarrow}}
      {\overset{}{\longrightarrow}}
      {\phantom{AAA}}
    &
    E \otimes E
     &\overset{coeq}{\longrightarrow}&
    E \otimes_A E
    \\
    && & {}_{\mathllap{\mu_E}}\searrow & \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    && && E
  }
  \,.
$$

By considering a diagram of such coequalizer diagrams with middle vertical morphism $e_E\circ e_A$, one find that this is a unit for $\mu_E$ and that $(E, \mu_E, e_E \circ e_A)$ is a commutative monoid in $(\mathcal{C}, \otimes, 1)$.

Then consider the two conditions on the unit $e_E \colon A \longrightarrow E$. First of all this is an $A$-module homomorphism, which means that

$$
  (\star)
  \;\;\;\;\;
  \;\;\;\;\;
  \array{
    A \otimes A &\overset{id \otimes e_E}{\longrightarrow}& A \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow && \downarrow^{\mathrlap{\rho}}
    \\
    A &\underset{e_E}{\longrightarrow}& E
  }
$$

[[commuting diagram|commutes]]. Moreover it satisfies the unit property

$$
  \array{
    A \otimes_A E 
      &\overset{e_A \otimes id}{\longrightarrow}&
    E \otimes_A E
    \\
    & {}_{\mathllap{\simeq}}\searrow & \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    && E
  }
  \,.
$$

By forgetting the tensor product over $A$, the latter gives

$$
  \array{
    A \otimes E 
      &\overset{e \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    \downarrow && \downarrow^{\mathrlap{}}
    \\
    A \otimes_A E 
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes_A E
    \\
    {}^{\mathllap{\simeq}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    E &=& E
  }
  \;\;\;\;\;\;\;\;
   \simeq
  \;\;\;\;\;\;\;\;
  \array{
    A \otimes E 
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\rho}}\downarrow && \downarrow^{\mathrlap{\mu_{E}}}
    \\
    E &\underset{id}{\longrightarrow}& E  
  }
  \,,
$$

where the top vertical morphisms on the left the canonical coequalizers, which identifies the vertical composites on the right as shown. Hence this may be [[pasting|pasted]] to the square $(\star)$ above, to yield a [[commuting square]]

$$
  \array{
    A \otimes A
     &\overset{id\otimes e_E}{\longrightarrow}&
    A \otimes E 
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow
      &&
    {}^{\mathllap{\rho}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{E}}}
    \\
    A &\underset{e_E}{\longrightarrow}& E &\underset{id}{\longrightarrow}& E  
  }  
  \;\;\;\;\;\;\;\;\;\;
   =
  \;\;\;\;\;\;\;\;\;\;
  \array{
    A \otimes A 
     &\overset{e_E \otimes e_E}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_E}}
    \\
    A &\underset{e_E}{\longrightarrow}& E
  }
  \,.
$$

This shows that the unit $e_A$ is a homomorphism of monoids $(A,\mu_A, e_A) \longrightarrow (E, \mu_E, e_E\circ e_A)$.

Now for the converse direction, assume that $(A,\mu_A, e_A)$ and $(E, \mu_E, e'_E)$ are two commutative monoids in $(\mathcal{C}, \otimes, 1)$ with $e_E \;\colon\; A  \to E$ a monoid homomorphism. Then $E$ inherits a left $A$-[[module]] structure by

$$
  \rho
    \;\colon\;
  A \otimes E 
    \overset{e_A \otimes id}{\longrightarrow} 
  E \otimes E
    \overset{\mu_E}{\longrightarrow}
  E
  \,.
$$

By commutativity and associativity it follows that $\mu_E$ coequalizes the two induced morphisms $E \otimes A \otimes E \underoverset{\longrightarrow}{\longrightarrow}{\phantom{AA}} E \otimes E$. Hence the [[universal property]] of the [[coequalizer]] gives a factorization through some $\mu_{E/A}\colon E \otimes_A E \longrightarrow E$. This shows that $(E, \mu_{E/A}, e_E)$ is a commutative $A$-algebra.

Finally one checks that these two constructions are inverses to each other, up to isomorphism.

=--


### Day convolution



+-- {: .num_defn #TopologicalDayConvolutionProduct}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}) with [[tensor product]] denoted $\otimes_{\mathcal{C}} \;\colon\; \mathcal{C} \times\mathcal{C} \to \mathcal{C}$. 

Then the **[[Day convolution]] tensor product** on the pointed topological [[enriched functor category]] $[\mathcal{C},Top^{\ast/}_{cg}]$ (def. \ref{PointedTopologicalFunctorCategory}) is the [[functor]]

$$
  \otimes_{Day} 
    \;\colon\; 
  [\mathcal{C},Top^{\ast/}_{cg}] \times [\mathcal{C},Top^{\ast/}_{cg}] 
    \longrightarrow 
  [\mathcal{C},Top^{\ast/}_{cg}]
$$

out of the pointed topological [[product category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) given by the following [[coend]] (def. \ref{EndAndCoendInTopcgSmash})

$$
  X \otimes_{Day} Y
    \;\colon\;
  c 
    \;\mapsto\;
  \overset{(c_1,c_2)\in \mathcal{C}\times \mathcal{C}}{\int}
    \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c) \wedge X(c_1) \wedge Y(c_2)
  \,.
$$

=--

+-- {: .num_example}
###### Example

Let $Seq$ denote the category with objects the [[natural numbers]], and only the [[zero morphisms]] and [[identity morphisms]] on these objects:

$$
  Seq(n_1,n_2)
  \coloneqq
  \left\{
    \array{
      S^0 & if\; n_1 = n_2
      \\
      \ast & otherwise
    }
  \right.
  \,.
$$

Regard this as a pointed topologically enriched category in the unique way. The operation of addition of natural numbers $\otimes = +$ makes this a monoidal category.

An object $X_\bullet \in [Seq, Top_{cg}^{\ast/}]$ is an $\mathbb{N}$-sequence of pointed topological spaces. Given two such, then their Day convolution according to def. \ref{TopologicalDayConvolutionProduct} is

$$
  \begin{aligned}
    (X \otimes_{Day} Y)_n
    & =
    \overset{(n_1,n_2)}{\int}
     Seq(n_1 + n_2 , n)
     \wedge 
     X_{n_1} \wedge X_{n_2}
    \\
    & = \underset{{n_1+n_2} \atop {= n}}{\coprod} \left(X_{n_1}\wedge X_{n_2}\right)
  \end{aligned} 
  \,.
$$

=--


We observe now that [[Day convolution]] is equivalently a [[left Kan extension]] (def. \ref{TopologicalLeftKanExtensionBCoend}). This will be key for understanding [[monoids]] and [[modules]] with respect to Day convolution.

+-- {: .num_defn #ExternalTensorProduct}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)).  Its **[[external tensor product]]** is the pointed [[topologically enriched functor]]

$$
  \overline{\wedge} 
   \;\colon\; 
  [\mathcal{C},Top^{\ast/}_{cg}] 
    \times 
  [\mathcal{C},Top^{\ast/}_{cg}] 
    \longrightarrow 
  [\mathcal{C}\times \mathcal{C}, Top^{\ast/}_{cg}]
$$

given by 

$$
  X \overline{\wedge} Y  
    \;\coloneqq\; 
  \wedge \circ (X,Y)
  \,,
$$

i.e.

$$
  (X \overline\wedge Y)(c_1,c_2)
  =
  X(c_1)\wedge X(c_2)
  \,.
$$

=--


+-- {: .num_prop #DayConvolutionViaKanExtensionOfExternalTensorAlongTensor}
###### Proposition

The [[Day convolution]] product (def. \ref{TopologicalDayConvolutionProduct}) of two functors is equivalently the [[left Kan extension]] (def. \ref{TopologicalLeftKanExtensionBCoend}) of their external tensor product (def. \ref{ExternalTensorProduct}) along the tensor product $\otimes_{\mathcal{C}}$: there is a [[natural isomorphism]]

$$
  X \otimes_{Day} Y
  \simeq
  Lan_{\otimes_{\mathcal{C}}} (X \overline{\wedge} Y)
  \,.
$$

Hence the [[adjunction unit]] is a [[natural transformation]] of the form

$$
  \array{
    \mathcal{C} \times \mathcal{C}
    &&
      \overset{X \overline{\wedge} Y}{\longrightarrow}
    &&
      Top^{\ast/}_{cg}
    \\
    & {}^{\mathllap{\otimes}}\searrow 
     &\Downarrow&
    \nearrow_{\mathrlap{X \otimes_{Day} Y}}
    \\
    && \mathcal{C}
  }
  \,.
$$

=--

This perspective is highlighted in ([MMSS 00, p. 60](#MMSS00)).

+-- {: .proof}
###### Proof

By prop. \ref{TopologicalLeftKanExtensionBCoend} we may compute the left Kan extension as the following [[coend]]:

$$
  \begin{aligned}
     Lan_{\otimes_{\mathcal{C}}} (X\overline{\wedge} Y)(c)
     &
     \simeq
      \overset{(c_1,c_2)}{\int} 
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c )
      \wedge
      (X\overline{\wedge}Y)(c_1,c_2)
     \\
    & =
    \overset{(c_1,c_2)}{\int}
    \mathcal{C}(c_1\otimes c_2) 
    \wedge
     X(c_1)\wedge X(c_2) 
  \end{aligned} 
  \,.
$$


=--

+-- {: .num_cor #DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor}
###### Corollary

The [[Day convolution]] $\otimes_{Day}$ (def. \ref{TopologicalDayConvolutionProduct}) is universally characterized by the property that there are [[natural isomorphisms]]

$$
  [\mathcal{C},Top^{\ast/}_{cg}](X \otimes_{Day} Y, Z) 
    \simeq 
  [\mathcal{C}\times \mathcal{C},Top^{\ast/}_{cg}](
    X \overline{\wedge} Y,\; Z \circ \wedge
  )
  \,,
$$

where $\overline{\wedge}$ is the external product of def. \ref{ExternalTensorProduct}.

=--


Write

$$
  y \;\colon\; \mathcal{C}^{op} \longrightarrow [\mathcal{C}, Top^{\ast/}_{cg}]
$$

for the $Top^{\ast/}_{cg}$-[[Yoneda embedding]], so that for $c\in \mathcal{C}$ any [[object]], $y(c)$ is the [[representable functor|corepresented functor]] $y(c)\colon d \mapsto \mathcal{C}(c,d)$.


+-- {: .num_prop #DayConvolutionYieldsMonoidalCategoryStructure}
###### Proposition

For $\mathcal{C}$ a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}), the [[Day convolution]] tensor product $\otimes_{Day}$ of def. \ref{TopologicalDayConvolutionProduct} makes the pointed topologically [[enriched functor category]]

$$
  ( [\mathcal{C}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1))
$$

a pointed topological [[monoidal category]] (def. \ref{MonoidalCategory}) with [[tensor unit]] $y(1)$ [[representable functor|co-represented]] by the tensor unit $1$ of $\mathcal{C}$. 

=--

+-- {: .proof}
###### Proof

Regarding [[associativity]], observe that

$$
  \begin{aligned}
    (X \otimes_{Day} ( Y \otimes_{Day} Z ))(c)
    & \simeq
    \overset{(c_1,c_2)}{\int}
      \mathcal{C}(c_1 \otimes_{\mathcal{D}} c_2, \,c) 
        \wedge
      X(c_1) 
       \wedge
      \overset{(d_1,d_2)}{\int}
       \mathcal{C}(d_1 \otimes_{\mathcal{C}} d_2, c_2 )
       (Y(d_2) \wedge Z(d_2))
    \\
    &\simeq \overset{c_1, d_1, d_2}{\int}
    \underset{\simeq \mathcal{C}(c_1 \otimes_{\mathcal{C}} d_1 \otimes_{\mathcal{C}} d_2, c )}{
      \underbrace{
       \overset{c_2}{\int} 
         \mathcal{C}(c_1 \otimes_{\mathcal{D}} c_2 , c)
           \wedge
         \mathcal{C}(d_1 \otimes_{\mathcal{C}}d_2, c_2 )
      }
    }
    \wedge X(c_1) \wedge (Y(d_1) \wedge Z(d_2))
    \\
    &\simeq 
    \overset{c_1, d_1, d_2}{\int}
     \mathcal{C}(c_1\otimes_{\mathcal{C}} d_1 \otimes_{\mathcal{C}} d_2, c ) 
       \wedge  
     X(c_1) \wedge (Y(d_1) \wedge Z(d_2))
  \end{aligned}
  \,,
$$

where we used the [[Fubini theorem]] for [[coends]] (prop. \ref{CoendsCommuteWithEachOther}) and then twice the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}). An analogous formula follows for $X \otimes_{Day}  (Y \otimes_{Day} Z)))(c)$, and so associativity follows via prop. \ref{DayConvolutionViaKanExtensionOfExternalTensorAlongTensor} from the associativity of the [[smash product]] and of the tensor product $\otimes_{\mathcal{C}}$.

To see that $y(1)$ is the tensor unit for $\otimes_{Day}$, 
use the [[Fubini theorem]] for [[coends]] (prop. \ref{CoendsCommuteWithEachOther}) and then twice the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}) to get for any $X \in [\mathcal{C},Top^{\ast/}_{cg}]$ that

$$
  \begin{aligned}
     X \otimes_{Day} y(1)
     & 
     =
     \overset{c_1,c_2 \in \mathcal{C}}{\int}
     \mathcal{C}(c_1\otimes_{\mathcal{D}} c_2,-) 
      \wedge 
     X(c_1) \wedge \mathcal{C}(1,c_2)
     \\
     & \simeq 
     \overset{c_1\in \mathcal{C}}{\int}
      X(c_1) 
        \wedge  
      \overset{c_2 \in \mathcal{C}}{\int}  
        \mathcal{C}(c_1\otimes_{\mathcal{C}} c_2,-)
        \wedge 
        \mathcal{C}(1,c_2) 
    \\
    & \simeq 
      \overset{c_1\in \mathcal{C}}{\int}
      X(c_1) 
         \wedge
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} 1, -)
    \\
    & \simeq 
      \overset{c_1\in \mathcal{C}}{\int}
      X(c_1) 
         \wedge
      \mathcal{C}(c_1, -)
    \\
    & \simeq
    X(-)
    \\
    & \simeq 
    X
  \end{aligned}
  \,.
$$

=--


+-- {: .num_prop #DayMonoidalStructureIsClosed}
###### Proposition

For $\mathcal{C}$ a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}) with [[tensor product]] denoted $\otimes_{\mathcal{C}} \;\colon\; \mathcal{C} \times\mathcal{C} \to \mathcal{C}$, the [[monoidal category]] with [[Day convolution]] $([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1))$ from def. \ref{DayConvolutionYieldsMonoidalCategoryStructure} is a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}). Its [[internal hom]] $[-,-]_{Day}$ is given by the [[end]] (def. \ref{EndAndCoendInTopcgSmash})

$$
  [X,Y]_{Day}(c)
  \simeq
   \underset{c_1,c_2}{\int}
      Maps\left( 
        \mathcal{C}(c \otimes_{\mathcal{C}} c_1,c_2),
        \;
        Maps(X(c_1) ,  Y(c_2))_\ast 
      \right)_\ast       
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using the [[Fubini theorem]] (def. \ref{CoendsCommuteWithEachOther}) and the [[co-Yoneda lemma]] (def. \ref{TopologicalCoYonedaLemma}) and in view of definition \ref{PointedTopologicalFunctorCategory} of the [[enriched functor category]], there is the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
     [\mathcal{C},V]( X, [Y,Z]_{Day} )
       & \simeq
     \underset{c}{\int} 
     Maps\left(
        X(c), 
        \underset{c_1,c_2}{\int}
        Maps\left( 
          \mathcal{C}(c \otimes_{\mathcal{C}} c_1 , c_2),
          Maps(Y(c_1), Z(c_2))_\ast 
        \right)_\ast
     \right)_\ast
     \\
     &
     \simeq
     \underset{c}{\int}
     \underset{c_1,c_2}{\int}
     Maps\left(
       \mathcal{C}(c \otimes_{\mathcal{C}} c_1, c_2)
         \wedge
       X(c)
         \wedge
       Y(c_1)
       ,\;
       Z(c_2)
     \right)_\ast
     \\
     & \simeq
     \underset{c_2}{\int}
     Maps\left(
       \overset{c,c_1}{\int}
       \mathcal{C}(c \otimes_{\mathcal{C}} c_1, c_2)
         \wedge
       X(c)
         \wedge 
       Y(c_1)
       ,\;
       Z(c_2)
     \right)_\ast
     \\
     &\simeq
     \underset{c_2}{\int}
       Maps\left(
         (X \otimes_{Day} Y)(c_2),
         Z(c_2)
       \right)_\ast
     \\
     &\simeq
     [\mathcal{C},V](X \otimes_{Day} Y, Z)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

In the situation of def. \ref{DayConvolutionYieldsMonoidalCategoryStructure}, the [[Yoneda embedding]] $c\mapsto \mathcal{C}(c,-)$  constitutes a  [[strong monoidal functor]] (def. \ref{LaxMonoidalFunctor})

$$
  (\mathcal{C},\otimes_{\mathcal{C}}, I) \hookrightarrow ([\mathcal{C},V], \otimes_{Day}, y(I))
  \,.
$$

=--

+-- {: .proof}
###### Proof

That the [[tensor unit]] is respected is part of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure}. To see that the [[tensor product]] is respected, apply the [[co-Yoneda lemma]] (prop \ref{TopologicalCoYonedaLemma}) twice to get the following natural isomorphism

$$
  \begin{aligned}
    (y(c_1) \otimes_{Day} y(c_2))(c)
    &
    \simeq
    \overset{d_1, d_2}{\int} 
      \mathcal{C}(d_1 \otimes_{\mathcal{C}} d_2, c )
    \wedge
      \mathcal{C}(c_1,d_1)
    \wedge
      \mathcal{C}(c_2,d_2)
    \\
    & \simeq \mathcal{C}(c_1\otimes_{\mathcal{C}}c_2 , c )
    \\
    & 
    = y(c_1 \otimes_{\mathcal{C}} c_2 )(c)
  \end{aligned}
  \,.
$$

=--



### Functors with smash product
 {#FunctorsWithSmashProduct}


+-- {: .num_prop #DayMonoidsAreLaxMonoidalFunctorsOnTheSite}
###### Proposition

Let $(\mathcal{C},\otimes I)$ be a pointed [[topologically enriched category]] ([[symmetric monoidal category]]) [[monoidal category]] (def. \ref{MonoidalCategory}). Regard $(Top_{cg}^{\ast/}, \wedge , S^0)$ as a topological [[symmetric monoidal category]] as in example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}.

Then ([[commutative monoid in a symmetric monoidal category|commutative]]) [[monoid in a monoidal category|monoids in]] (def. \ref{MonoidsInMonoidalCategory}) the [[Day convolution]] monoidal category $([\mathcal{C}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))$ of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure} are equivalent to ([[braided monoidal functor|braided]]) [[lax monoidal functors]] (def. \ref{LaxMonoidalFunctor}) of the form

$$
  (\mathcal{C},\otimes, I) \longrightarrow (Top^{\ast}_{cg}, \wedge, S^0)
  \,,
$$

called **[[functors with smash products]]** on $\mathcal{C}$, i.e. there are [[equivalences of categories]] of the form

$$
  \begin{aligned}
    Mon([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))
      &\simeq
    MonFunc(\mathcal{C},Top^{\ast/}_{cg})
    \\
    CMon([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))
      &\simeq
    SymMonFunc(\mathcal{C},Top^{\ast/}_{cg})
  \end{aligned}
  \,.
$$

Moreover, [[module objects]] over these monoid objects are equivalent to the corresponding [[modules over monoidal functors]].

=--

This is stated in some form in ([Day 70, example 3.2.2](Day+convolution#Day70)). It is highlighted again in ([MMSS 00, prop. 22.1](#MMSS00)). 

+-- {: .proof}
###### Proof

By definition \ref{LaxMonoidalFunctor}, a [[lax monoidal functor]] $F \colon \mathcal{C} \to Top^{\ast/}_{cg}$ is a topologically enriched functor equipped with a morphism of [[pointed topological spaces]] of the form

$$
  S^0 \longrightarrow F(1_{\mathcal{C}})
$$

and equipped with a [[natural transformation|natural]] system of maps of pointed topological spaces of the form

$$
  F(c_1) \wedge F(c_2) \longrightarrow F(c_1 \otimes_{\mathcal{C}} c_2)
$$

for all $c_1,c_2 \in \mathcal{C}$.

Under the [[Yoneda lemma]] (prop. \ref{YonedaReductionTopological}) the first of these is equivalently a morphism in $[\mathcal{C}, Top^{\ast/}_{cg}]$ of the form

$$
  y(S^0) \longrightarrow F
  \,.
$$

Moreover, under the [[natural isomorphism]] of corollary \ref{DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor} the second of these is equivalently a morphism in $[\mathcal{C}, Top^{\ast/}_{cg}]$ of the form

$$
  F \otimes_{Day} F \longrightarrow F
  \,.
$$

Translating the conditions of def. \ref{LaxMonoidalFunctor} satisfied by a [[lax monoidal functor]] through these identifications gives precisely the conditions of def. \ref{MonoidsInMonoidalCategory} on a ([[commutative monoid in a symmetric monoidal category|commutative]]) [[monoid in a monoidal category|monoid in]] object $F$ under $\otimes_{Day}$.

Similarly for [[module objects]] and [[modules over monoidal functors]].

=--


+-- {: .num_prop #PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution}
###### Proposition

Let $f \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[lax monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between pointed [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}). Then the induced functor

$$
  f^\ast
    \;\colon\;
  [\mathcal{D}, Top^{\ast/}_{cg}]
    \longrightarrow
  [\mathcal{C}, Top_{cg}^{\ast}]
$$

given by $(f^\ast X)(c)\coloneqq X(f(c))$ preserves [[monoid in a monoidal category|monoids]] under [[Day convolution]]

$$
  f^\ast
    \;\colon\;
  Mon([\mathcal{D}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{D}}))
    \longrightarrow
  Mon([\mathcal{C}, Top_{cg}^{\ast}], \otimes_{Day}, y(1_{\mathcal{C}})
$$


Moreover, if $\mathcal{C}$ and $\mathcal{D}$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) and $f$ is a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}), then $f^\ast$ also preserves [[commutative monoids in a symmetric monoidal category|commutative monoids]]

$$
  f^\ast
    \;\colon\;
  CMon([\mathcal{D}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{D}}))
    \longrightarrow
  CMon([\mathcal{C}, Top_{cg}^{\ast}], \otimes_{Day}, y(1_{\mathcal{C}})
  \,.
$$


=--

+-- {: .proof}
###### Proof

This is an immediate corollary of prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite}, since the composite of two (braided) lax monoidal functors is itself canonically a (braided) lax monoidal functor.

=--


### Monoidal homotopy theory

We now combine the concepts of [[model category]] and [[monoidal category]].


+-- {: .num_defn #MonoidalModelCategory}
###### Definition

A (symmetric) **monoidal model category** is [[model category]] $\mathcal{C}$
equipped with the structure of a  [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, I)$
such that the following two compatibility conditions are satisfied

1. ([[pushout-product axiom]]) For every pair of cofibrations $f \colon X \to Y$ and $f' \colon X' \to Y'$, their [[pushout-product]], hence the induced morphism out of the cofibered [[coproduct]] over ways of forming the tensor product of these objects

   $$
     (X \otimes Y') \coprod_{X \otimes X'} (Y \otimes X')
     \longrightarrow
     Y \otimes Y'
     \,,
   $$

   is itself a cofibration, which, furthermore, is acyclic if $f$ or $f'$ is.

   (Equivalently this says that the [[tensor product]] $\otimes : C \times C \to C$ is a left [[Quillen bifunctor]].)

1. (unit axiom) For every cofibrant object $X$ and every cofibrant resolution $\emptyset \hookrightarrow Q I \stackrel{p_I}{\longrightarrow} \ast$ of the [[tensor unit]] $I$, the resulting morphism

   $$
     Q I \otimes X \stackrel{p_I \otimes X}{\longrightarrow} I\otimes X \stackrel{\simeq}{\longrightarrow} X
   $$ 

  is a weak equivalence.


=--

+-- {: .num_remark }
###### Remark

The [[pushout-product axiom]] in def. \ref{MonoidalModelCategory} implies that for $X$ a cofibrant object, then the functor $X \otimes (-)$ preserves cofibrations and acyclic cofibrations.

In particular if the [[tensor unit]] $I$ happens to be cofibrant, then the unit axiom in def. \ref{MonoidalModelCategory} is implied by the pushout-product axiom. 

=--

+-- {: .num_defn #MonoidAxiom}
###### Definition

We say a [[monoidal model category]], def. \ref{MonoidalModelCategory}, satisfies the **[[monoid axiom]]**, def. \ref{MonoidalModelCategory}, if every morphism that is obtained as a [[transfinite composition]] of [[pushouts]] of [[tensor products]] $X\otimes f$ of acyclic cofibrations $f$ with any object $X$ is a weak equivalence.

=--

([Schwede-Shipley 00, def. 3.3.](#SchwedeShipley)).

+-- {: .num_remark}
###### Remark

In particular, the axiom in def. \ref{MonoidAxiom} says that for every object $X$ the functor $X \otimes (-)$ sends acyclic cofibrations to weak equivalences.

=--


+-- {: .num_prop #MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}
###### Proposition

Let $(\mathcal{C}, \otimes, I)$ be a [[monoidal model category]]. Then the [[left derived functor]] of the tensor product exsists and makes the [[homotopy category of a model category|homotopy category]] into a [[monoidal category]] $(Ho(\mathcal{C}), \otimes^L, \gamma(I))$.

If in in addition $(\mathcal{C}, \otimes)$ satisfies the [[monoid axiom in a monoidal model category|monoid axiom]], then the [[localization]] functor $\gamma\colon \mathcal{C}\to Ho(\mathcal{C})$ carries the structure of a [[lax monoidal functor]]

$$
  \gamma
  \;\colon\;
  (\mathcal{C}, \otimes, I)
   \longrightarrow
  (Ho(\mathcal{C}), \otimes^L , \gamma(I))
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the explicit model of $Ho(\mathcal{C})$ as the category of fibrant-cofibrant objects in $\mathcal{C}$ with left/right-homotopy classes of morphisms between them (discussed at _[[homotopy category of a model category]]_).

A [[derived functor]] exists if its restriction to this subcategory preserves weak equivalences. Now the [[pushout-product axiom]] implies that on the subcategory of cofibrant objects the functor $\otimes$ preserves acyclic cofibrations, and then the preservation of all weak equivalences follows by [[Ken Brown's lemma]]. 

Hence $\otimes^L$ exists and its [[associativity]] follows simply by restriction. It remains to see its [[unitality]].

To that end, consider the construction of the localization functor $\gamma$ via a fixed but arbitrary choice of (co-)fibrant replacements $Q$ and $R$, assumed to be the identity on (co-)fibrant objects. We fix notation as follows:

$$
\emptyset \underoverset{\in Cof}{i_X}{\longrightarrow} Q X \underoverset{\in W \cap Fib}{p_x}{\longrightarrow} X
\;\;\,,\;\;
X \underoverset{\in W \cap Cof}{j_X}{\longrightarrow} R X \underoverset{\in Fib}{q_x}{\longrightarrow} \ast
  \,.
$$

 
Now to see that $\gamma(I)$ is the [[tensor unit]] for $\otimes^L$, notice that in the [[zig-zag]]

$$
  (R Q I) \otimes (R Q X)
    \overset{j_{Q I} \otimes (R Q X)}{\longleftarrow}
  (Q I) \otimes (R Q X)
    \overset{(Q I)\otimes j_{Q X}}{\longleftarrow}
  (Q I) \otimes (Q X)
    \overset{p_I \otimes (Q X)}{\longrightarrow}
  I \otimes Q X
    \simeq
  Q X
$$

all morphisms are weak equivalences: For the first two this is due to the [[pushout-product axiom]], for the third this is due to the unit axiom on a monoidal model category. It follows that under $\gamma(-)$ this zig-zig gives an isomorphism

$$
  \gamma(I) \otimes^L \gamma(X)\simeq \gamma(X)
$$

and similarly for tensoring with $\gamma(I)$ from the right.

To exhibit lax monoidal structure on $\gamma$, we need to construct a [[natural transformation]]

$$
  \gamma(X) \otimes^L \gamma(Y) \longrightarrow \gamma(X \otimes Y)
$$

and show that it satisfies the the appropriate [[associativity]] and [[unitality]] condition.

By the definitions at _[[homotopy category of a model category]]_, the morphism in question is to be of the form

$$
  (R Q X) \otimes (R Q Y) \longrightarrow R Q (X\otimes Y)
$$


To this end, consider the [[zig-zag]]

$$
  (R Q X) \otimes (R Q Y)
   \underoverset{\in Cof \cap W}{j_{Q X} \otimes R Q Y}{\longleftarrow}
  (Q X) \otimes (R Q Y)
    \underoverset{\in Cof \cap W}{(Q X) \otimes  j_{Q Y} }{\longleftarrow}
  (Q X) \otimes (Q Y)
    \overset{p_X \otimes (Q Y)}{\longrightarrow}
  X \otimes (Q Y)
    \overset{Y \otimes p_Y}{\longrightarrow}   
  X \otimes Y
  \,,
$$

and observe that the two morphisms on the left are weak equivalences, as indicated, by the [[pushout-product axiom]] satisfied by $\otimes$.

Hence applying $\gamma$ to this zig-zag, which is given by the two horizontal part of the following digram

$$
  \array{
    (R Q X) \otimes (R Q Y) &\longleftarrow& R( Q X \otimes Q Y ) &\longrightarrow& R Q (X \otimes Y)
    \\
    \uparrow^{\mathrlap{id}} && \uparrow^{\mathrlap{j_{Q X \otimes Q Y}}} && \uparrow^{\mathrlap{j_{Q(X \otimes Y)}}}
    \\
    \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{p_{X\otimes Y}}}
    \\
    (R Q X) \otimes (R Q Y)
     &\underoverset{\in Cof \cap W}{j_{Q X} \otimes j_{Q Y}}{\longleftarrow}&
    (Q X) \otimes (Q Y)
      &\overset{p_X \otimes p_Y}{\longrightarrow}&
    X \otimes Y
  }
  \,,
$$

and inverting the first two morphisms, this yields a natural transformation as required. 


To see that this satisfies associativity if the monoid axiom holds, tensor the entire diagram above on the right with $(R Q Z)$ and consider the following [[pasting]] composite:

$$
  \array{
    (R Q X) \otimes (R Q Y) \otimes (R Q Z) &\longleftarrow& R( Q X \otimes Q Y ) \otimes (R Q Z) &\longrightarrow& (R Q (X \otimes Y)) \otimes (R Q Z)
    \\
    \uparrow^{\mathrlap{id}} && \uparrow^{\mathrlap{j_{Q X \otimes Q Y} \otimes id }} && \uparrow^{\mathrlap{j_{Q(X \otimes Y)}\otimes id }}
    \\
    && && Q(X \otimes Y) \otimes (R Q Z) &\overset{id \otimes j_{Q Z}}{\longleftarrow}& Q(X\otimes Y) \otimes (Q Z)
    \\
       \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{id}} 
    && 
      \downarrow^{\mathrlap{p_{(X\otimes Y)} \otimes id }} 
    &(\star)& 
     \downarrow^{\mathrlap{p_{(X \otimes Y)} \otimes id}}
    \\
    (R Q X) \otimes (R Q Y) \otimes (R Q Z)
     &\underoverset{\in Cof \cap W}{j_{Q X} \otimes j_{Q Y} \otimes id}{\longleftarrow}&
    (Q X) \otimes (Q Y) \otimes (R Q Z)
      &\overset{p_X \otimes p_Y \otimes id}{\longrightarrow}&
    X \otimes Y \otimes (R Q Z)
      &\underset{id \otimes j_{Q Z}}{\longleftarrow}&
    X\otimes Y \otimes Q Z 
      &\overset{id \otimes p_Z}{\longrightarrow}& 
    X \otimes Y \otimes Z  
  }
  \,,
$$

Observe that under $\gamma$ the total top [[zig-zag]] in this diagram gives

$$
  (\gamma(X) \otimes^L \gamma(Y)) \otimes^L \gamma(Z)
  \to \gamma(X\otimes Y)\otimes^L \gamma(Z)
  \,.
$$

Now by the [[monoid axiom in a monoidal model category|monoid axiom]] (but not by the pushout-product axiom!), the horizontal maps in the square in the bottom right (labeled $\star$) are weak equivalences. This implies that the total horizontal part of the diagram is a [[zig-zag]] in the first place, and that under $\gamma$ the total top zig-zag is equal to the image of that total bottom zig-zag. But by functoriality of $\otimes$, that image of the bottom zig-zag is 

$$
  \gamma(p_X \otimes p_Y \otimes p_Z) 
  \circ 
  \gamma(j_{Q X} \otimes j_{Q Y} \otimes j_{Q Z})^{-1}
  \,.
$$

The same argument applies to left tensoring with $R Q Z$ instead of right tensoring, and so in both cases we reduce to the same morphism in the homotopy category, thus showing the associativity condition on the transformation that exhibits $\gamma$ as a lax monoidal functor.

=--




[[!redirects Model Categories of diagram spectra]]

category: reference