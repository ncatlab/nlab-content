
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

#Contents#
* table of contents
{:toc}

## Idea


A [[model category]] structure for [[excisive functors]] on [[functors]] from ([[finite homotopy type|finite]]) pointed simplicial sets to pointed simplicial sets ([Lydakis 98, theorem 9.2](#Lydakis98), [Biedermann-Chorny-R&#246;ndings 06, section 9](#BiedermannChornyRondings06)), hence (see [here](excisive+%28∞%2C1%29-functor#SpectrumObjects)) a [[model structure for spectra]] ([Lydakis 98, theorem 11.3](#Lydakis98)). 

Special case of a [[model structure for n-excisive functors]].

## Definition

### The underlying categories
 {#TheUnderlyingCategories}

+-- {: .num_defn #SimplicialSetsPointedAndFinite}
###### Definition

Write 

* [[sSet]] for the [[category]] of [[simplicial sets]];

* $sSet^{\ast/}$ for the category of [[pointed object|pointed]] simplicial sets;

* $sSet_{fin}^{\ast/}\simeq s(FinSet)^{\ast/} \hookrightarrow sSet^{\ast/}$ for the [[full subcategory]] of [[pointed object|pointed]] [[simplicial object|simplicial]] [[finite sets]].

Write

$$
  sSet^{\ast/}
  \stackrel{\overset{(-)_+}{\longleftarrow}}{\underset{u}{\longrightarrow}}
  sSet
$$

for the [[free-forgetful adjunction]], where the [[left adjoint]] functor $(-)_+$ freely adjoins a base point.

Write

$$
  \wedge \colon sSet^{\ast/} \times sSet^{\ast/} \longrightarrow sSet^{\ast/}
$$

for the [[smash product]] of [[pointed object|pointed]] [[simplicial sets]], similarly for its restriction to $sSet_{fin}^{\ast}$:

$$
  X \wedge Y 
    \coloneqq 
  cofib\left(
    \; 
    \left(\,
      (u(X),\ast) \sqcup (\ast, u(Y)) 
    \,\right) 
      \longrightarrow 
     u(X) \times u(Y) 
    \;
  \right)
  \,.
$$

This gives $sSet^{\ast/}$ and $sSet^{\ast/}_{fin}$ the structure of a [[closed monoidal category]] and we write 

$$
  [-,-]_\ast \;\colon\; (sSet^{\ast/})^{op} \times sSet^{\ast/} \longrightarrow sSet^{\ast/}
$$

for the corresponding [[internal hom]], the pointed [[function complex]] functor.

=--

+-- {: .num_remark }
###### Remark

For $X,Y\in sSet^{\ast/}$, the internal hom $[X,Y] \in sSet^{\ast/}$ is the simplicial set

$$
  [X,Y]_n = Hom_{sSet^{\ast/}}(X \wedge \Delta[n]_+, Y)
$$

regarded as pointed by the [[zero morphism]] (the one that factors through the base point), and the [[composition]] morphism

$$
  \circ \:\colon\; [X,Y] \wedge [Y,Z] \longrightarrow [X,Z]
$$

is given by

$$
  \begin{aligned}
    \circ_n 
      & \;\colon\; 
    ( 
      X \wedge \Delta[n]_+ \stackrel{f}{\longrightarrow} Y \;,\; Y \wedge \Delta[n]_+ \stackrel{g}{\longrightarrow} Z 
    )
    \\
    &
    \mapsto
    (
      X \wedge \Delta[n]_+
        \stackrel{X \wedge (diag_{\Delta[n]})_+}{\longrightarrow}
      X \wedge (\Delta[n] \times \Delta[n])_+
        \simeq
      X \wedge \Delta[n]_+ \wedge \Delta[n]_+
        \stackrel{f \wedge id}{\longrightarrow}
      Y \wedge \Delta[n]_+
        \stackrel{g}{\longrightarrow}
      Z
    )
  \end{aligned}
  \,.
$$

=--


We regard all the categories in def. \ref{SimplicialSetsPointedAndFinite} canonically as [[simplicially enriched categories]], and in fact regard $sSet^{\ast/}$ and $sSet^{\ast/}_{fin}$ as $sSet^{\ast/}$-[[enriched categories]]. 

+-- {: .num_remark }
###### Remark

The [[smash product]] as an $sSet^{\ast/}$-[[enriched functor]] takes

$$
  \wedge \;\colon\; [X_1,Y_1] \wedge [X_2, Y_2] \longrightarrow [X_1 \wedge X_2, Y_1\wedge Y_2]
$$ 

by

$$
  \begin{aligned}
    \wedge_n 
    & \colon
    ( 
      X_1 \wedge \Delta[n]_+ \stackrel{f_1}{\longrightarrow} Y_1 \;,\;
      X_2 \wedge \Delta[n]_+ \stackrel{f_2}{\longrightarrow} Y_2
    )
    \\
    & \mapsto
    X_1 \wedge X_2 \wedge \Delta[n]_+
      \stackrel{id \wedge diag_+}{\longrightarrow}
    X_1 \wedge X_2 \wedge (\Delta[n] \times \Delta[n])_+
      \simeq
    X_1 \wedge X_2 \wedge \Delta[n]_+ \wedge \Delta[n]_+
      \simeq
    (X_1 \wedge \Delta[n]_+) \wedge (X_2 \wedge \Delta[n]_+)
      \stackrel{(f_1)_n \wedge (f_2)_n}{\longrightarrow}
    Y_1 \wedge Y_2
  \end{aligned}
$$

=--

The category that is discussed [below](#TheModelStructures) to support a model structure for [[excisive functors]] is the  $sSet^{\ast/}$-[[enriched functor category]]

$$
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]
  \,.
$$

([Lydakis 98, example 3.8, def. 4.4](#Lydakis98))

In order to compare this to model structures for [[sequential spectra]] we consider also the following variant.
 
+-- {: .num_defn #CategoriesOfStandardSpheres}
###### Definition

Write $S^1_{std} \coloneqq \Delta[1]/\partial\Delta[1]\in sSet^{\ast/}$ for the standard minimal pointed simplicial [[1-sphere]].

Write 

$$
  \iota \;\colon\; StdSpheres \longrightarrow sSet^{\ast/}_{fin}
$$

for the non-full $sSet^{\ast/}$-[[enriched category|enriched]] [[subcategory]] of pointed [[simplicial object|simplicial]] [[finite sets]], def. \ref{SimplicialSetsPointedAndFinite} whose

* [[objects]] are the [[smash product]] powers $S^n_{std} \coloneqq (S^1_{std})^{\wedge^n}$ (the standard minimal simplicial [[n-spheres]]);

* [[hom-objects]] are

  $$
    [S^{n}_{std}, S^{n+k}_{std}]_{StdSpheres}
    \coloneqq
    \left\{
      \array{
        \ast & for & k \lt 0
        \\
        im(S^{k}_{std} \stackrel{}{\to} [S^n_{std}, S^{n+k}_{std}]_{sSet^{\ast/}_{fin}})
        & otherwise
      }
    \right.
  $$

=--

([Lydakis 98, def. 4.2](#Lydakis98))



+-- {: .num_prop }
###### Proposition

There is an $sSet^{\ast/}$-[[enriched functor]] 

$$
  (-)^seq
  \;\colon\;
  [StdSpheres,sSet^{\ast/}]
    \longrightarrow
  SeqPreSpec(sSet)
$$

(from the category of $sSet^{\ast/}$-[[enriched presheaves|enriched copresheaves]] on the categories of standard simplicial spheres of def. \ref{CategoriesOfStandardSpheres} to the category of [[sequential prespectra]] in [[sSet]]) given on objects by sending $X \in [StdSpheres,sSet^{\ast/}]$ to the sequential prespectrum $X^{seq}$ with components

$$
  X^{seq}_n \coloneqq X(S^n_{std})
$$

and with structure maps

$$
  \frac{S^1_{std} \wedge X^{seq}_n \stackrel{\sigma_n}{\longrightarrow} X^{seq}_n}{S^1_{std} \longrightarrow [X^{seq}_n, X^{seq}_{n+1}]}
$$

given by

$$
  S^1_{std} 
    \stackrel{\widetilde{id}}{\longrightarrow}
  [S^n_{std}, S^{n+1}_{std}]
    \stackrel{X_{S^n_{std}, S^{n+1}_{std}}}{\longrightarrow}
  [X^{seq}_n, X^{seq}_{n+1}]
  \,.
$$

This is an $sSet^{\ast/}$ [[enriched category theory|enriched]] [[equivalence of categories]].

=--

([Lydakis 98, prop. 4.3](#Lydakis98))


### The model structures
 {#TheModelStructures}

Consider the $sSet^{\ast/}$-[[enriched functor category]] $[sSet^{\ast/}_{fin}, sSet^{\ast/}]$ from [above](#TheUnderlyingCategories).

With $S^1_{std} \coloneqq \Delta[1]/\partial\Delta[1] \in sSet^{\ast/}$ we take [[looping and delooping]] $(\Sigma \dashv \Omega)$ to mean concretely the operation on [[smash product]] and pointed [[exponential]] with this particular $S^1_{std}$:

$$
  (\Sigma \dashv \Omega) \coloneqq ( S^1_{std}\wedge(-) \dashv [S^1_{std},-] ) \colon sSet^{\ast/} \longrightarrow sSet^{\ast/}
  \,.-
$$

These operations extend objectwise to $[sSet^{\ast/}_{fin}, sSet^{\ast/}]$, where we denote them by the same symbols.


+-- {: .num_defn #Tinfinity }
###### Definition

Write

$$
  T 
    \;\colon\; 
  [sSet^{\ast/}_{fin}, sSet^{\ast/}] 
    \longrightarrow 
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]
$$

for the [[functor]] given on $X$ by

$$
  T X \colon K \mapsto \Omega X(\Sigma K)
  \,.
$$

Write

$$
  \tau \;\colon\; id \longrightarrow T
$$

for the [[natural transformation]] whose component $\tau_{X}(K) \;\colon\; X(K) \to \Omega (X(\Sigma K))$ is the $(\Sigma \dashv \Omega)$-[[adjunct]] of the canonical morphism $\Sigma X(K) \longrightarrow X(\Sigma K)$ induced from

$$
  X
  \left(
  \array{
    K & \longrightarrow & \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \ast &\longrightarrow& \Sigma K
  }
  \right)
  \;\;\;\;
    =
  \;\;\;\;
  \array{
     X(K) &&\longrightarrow&& \ast
     \\
     \downarrow &&& \swarrow & \downarrow
     \\
     \downarrow && \Sigma X(K) && \downarrow
     \\
     \downarrow & \nearrow && \searrow^{\mathrlap{\tau_{X}(K)}}& \downarrow
     \\
     \ast &&\longrightarrow &&  X(\Sigma K)
  }
  \,.
$$
 
Write 

$$
  T^\infty
    \;\colon\; 
  [sSet^{\ast/}_{fin}, sSet^{\ast/}] 
    \longrightarrow 
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]
$$

for the functor given by $X$ by the [[sequential colimit]]

$$
  T^\infty X 
    \coloneqq 
  \underset{\longrightarrow}{\lim}
  \left(
    X 
      \stackrel{\tau_X}{\longrightarrow} 
    T X
      \stackrel{T(\tau_X)}{\longrightarrow}
    T (T X)
       \stackrel{}{\longrightarrow}
      \simeq 
  \right)
  \,.
$$

Write $Fib \colon sSet^{\ast} \to sSet^{\ast}$ for any [[Kan fibrant replacement]] functor.

Say that the _stabilization_ ([[spectrification]]) of $X$ is 

$$
  stab(X) \coloneqq T^\infty (Fib(Lan X(Fib(-))))
  \,,
$$

where $Lan X \colon sSet^{\ast/} \to sSet^{\ast}$ is the [[left Kan extension]] of $X$ along the inclusion $sSet^{\ast/}_{fin} \hookrightarrow sSet^{\ast/}$.

=--


+-- {: .num_defn #ClassesOfMorphismsForModelStructureForExcisiveFunctors}
###### Definition

Say that a morphism $f \colon X \to Y$ in $[sSet^{\ast/}_{fin}, sSet^{\ast/}]$ is 

* a _stable weak equivalence_ if its stabilization, def. \ref{Tinfinity}, takes value on each  $K \in sSet^{\ast/}$ in [[weak homotopy equivalences]] in $sSet^{\ast/}$;

* a _stable cofibration_ if it has the [[left lifting property]] against those morphisms whose value on every $K \in sSet^{\ast/}$ is a [[Kan fibration]].

=--

([Lydakis 98, def. 9.1, def. 7.1](#Lydakis98))

+-- {: .num_prop #LydakisModelStructure}
###### Proposition

The classes of morphisms of def. \ref{ClassesOfMorphismsForModelStructureForExcisiveFunctors}, define a [[model category]] structure

$$
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]_{Ly}
  \,.
$$

=--

([Lydakis 98, theorem 9.2](#Lydakis98))


## Properties

### Relation to BF-model structure on sequential spectra
 {#ModelStructureForSpectra}

There is a [[Quillen equivalence]] between the [[Bousfield-Friedlander model structure]] on [[sequential spectra]] and the Lydakis model structure $[sSet^{\ast/}_{fin}, sSet^{\ast/}]_{Ly}$ from prop. \ref{LydakisModelStructure}.

+-- {: .num_prop #SequentialSpectraAsSimplicialFunctorsOnStandardSpheres}
###### Proposition

There is an $sSet^{\ast/}$-[[enriched functor]] 

$$
  (-)^seq
  \;\colon\;
  [StdSpheres,sSet^{\ast/}]
    \longrightarrow
  SeqPreSpec(sSet)
$$

(from the category of $sSet^{\ast/}$-[[enriched presheaves|enriched copresheaves]] on the categories of standard simplicial spheres of def. \ref{CategoriesOfStandardSpheres} to the category of sequential prespectra in [[sSet]]) given on objects by sending $X \in [StdSpheres,sSet^{\ast/}]$ to the sequential prespectrum $X^{seq}$ with components

$$
  X^{seq}_n \coloneqq X(S^n_{std})
$$

and with structure maps

$$
  \frac{S^1_{std} \wedge X^{seq}_n \stackrel{\sigma_n}{\longrightarrow} X^{seq}_n}{S^1_{std} \longrightarrow [X^{seq}_n, X^{seq}_{n+1}]}
$$

given by

$$
  S^1_{std} 
    \stackrel{\widetilde{id}}{\longrightarrow}
  [S^n_{std}, S^{n+1}_{std}]
    \stackrel{X_{S^n_{std}, S^{n+1}_{std}}}{\longrightarrow}
  [X^{seq}_n, X^{seq}_{n+1}]
  \,.
$$

This is an $sSet^{\ast/}$ [[enriched category theory|enriched]] [[equivalence of categories]].

=--

([Lydakis 98, prop. 4.3](#Lydakis98))




+-- {: .num_prop #QuillenEquivalenceBetweenSequentialSpectraAndExcisiveFunctors}
###### Proposition

The [[adjunction]]

$$
  (\iota_\ast \dashv \iota^\ast)
  \;\colon\;
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]_{Ly}
    \stackrel{\overset{\iota_\ast}{\longleftarrow}}{\underset{\iota^\ast}{\longrightarrow}}
  [StdSpheres, sSet^{\ast/}]
    \underoverset{\simeq}{(-)^{seq}}{\longrightarrow}
  SeqPreSpec(sSet)_{BF}
$$

(given by restriction $\iota^\ast$ along the defining inclusion $\iota$ of def. \ref{CategoriesOfStandardSpheres} and by left [[Kan extension]] $\iota_\ast$ along $\iota$, and combined with the equivalence $(-)^{seq}$ of prop. \ref{SequentialSpectraAsSimplicialFunctorsOnStandardSpheres}) is a  [[Quillen adjunction]] and in fact a [[Quillen equivalence]] between the [[Bousfield-Friedlander model structure]] on sequential prespectra and Lydakis' model structure for excisive functors, prop. \ref{LydakisModelStructure}.

=--

### Symmetric monoidal smash product
 {#SmashProduct}


The [[excisive functors]] naturally carry a [[smash product]] ([Lydakis 98, def. 5.1](#Lydakis98)) making the model structure for 1-excisive functors a [[symmetric monoidal model category]] ([Lydakis 98, section 12](#Lydakis98)). Via  the translation to [[sequential spectra]] of prop. \ref{LydakisModelStructure} this is a model for the [[smash product of spectra]] ([Lydakis 98, theorem 12.5](#Lydakis98)); hence it is a [[symmetric smash product on spectra]].

A  [[monoid]] with respect to this smash product (hence a [[ring spectrum]]) is equivalently a [[functor with smash products]] ("FSP") as earlier considered in ([B&#246;kstedt 86](#B&#246;kstedt86)).

+-- {: .num_defn #DayConvolutionStructureOnExcisiveFunctors}
###### Definition

Since $(sSet^{\ast/}, \wedge)$ (def. \ref{SimplicialSetsPointedAndFinite}) is a [[symmetric monoidal category]], $[sSet^{\ast}_{fin}, sSet^{\ast/}]$ canonically becomes symmetric monoidal itself via the induced [[Day convolution product]]. We write

$$
  \left(\, [sSet^{\ast/}_{fin}, sSet^{\ast/}], \; \wedge_{Say} \right)
$$

for this [[symmetric monoidal category]].

=--

+-- {: .num_prop #LydakisTensorProductIsDayConvolution}
###### Proposition

The smash product on $[sSet^{\ast/}_{fin}, sSet^{\ast/}]$ considered ([Lydakis 98, def. 5.1](#Lydakis98)) coincides with the [[Day convolution product]] of def. \ref{DayConvolutionStructureOnExcisiveFunctors}.

=--

+-- {: .proof}
###### Proof

As in ([MMSS00](Day%20convolution#MMSS00)), the Day convolution product is characterized by making a [[natural isomorphism]] of the form

$$
  [sSet^{\ast/}_{fin}, sSet^{\ast/}](X \wedge Y, Z) \simeq [sSet^{\ast/}_{fin} \times sSet^{\ast/}_{fin}, sSet^{\ast/}](X \tilde{\wedge} Y, Z \circ \wedge)
$$

where the _external smash product_ $\tilde {\wedge}$ on the right is defined by $X \tilde{\wedge} Y  \coloneqq  \wedge \circ (X,Y) $. Now, ([Lydakis 98, def. 5.1](#Lydakis98)) sets 

$$
  X \wedge Y \coloneqq \wedge_\ast (X \tilde{\wedge} Y) 
$$

where, by ([Lydakis 98, prop. 3.23](#Lydakis98)),  $\wedge_\ast$ is the [[left adjoint]] to $\wedge^\ast(-) \coloneqq (-)\circ \wedge$. Hence the [[adjunction]] isomorphism gives the above characterization.

=--

+-- {: .num_prop }
###### Proposition

Under the Quillen equivalence of prop. \ref{QuillenEquivalenceBetweenSequentialSpectraAndExcisiveFunctors} the symmetric monoidal [[Day convolution product]] on excisive simplicial functors (prop. \ref{LydakisTensorProductIsDayConvolution}) is identified with the [[smash product of spectra]].

=--

([Lydakis 98, theorem 12.5](#Lydakis98))

This implies that any incarnation of the [[sphere spectrum]] in $[sSet^{\ast}_{fin}, sSet^{\ast/}]$, possibly suitably replaced acts as the [[tensor unit]] up to stable weak equivalence. The following says that the canonical incarnation of the sphere spectrum actually is the genuine (1-categorical) tensor unit:

+-- {: .num_defn #StandardSphereSpectrum}
###### Definition

Write 

$$
  \mathbb{S}_{std}\in [sSet^{\ast/}_{fin}, sSet^{\ast/}]
$$

for the canonical inclusion $sSet^{\ast/}_{fin} \hookrightarrow sSet^{\ast/}$.

(the standard incarnatin of the [[sphere spectrum]] in the model structure for excisive functors).

=--

+-- {: .num_prop}
###### Proposition

The object $\mathbb{S}_{std}$ of def. \ref{StandardSphereSpectrum} is (up to [[isomorphism]]) the [[tensor unit]] in  $([sSet^{\ast/}_{fin}, sSet^{\ast}], \wedge_{Day})$.


=--

+-- {: .proof}
###### Proof

This is ([Lydakis 98, theorem 59](#Lydakis98)), but it is immediate with prop. \ref{LydakisTensorProductIsDayConvolution}, using that the tensor unit for Day convolution is the functor [[representable functor|represented]] by the tensor unit in the underlying site.

=--

+-- {: .num_prop }
###### Proposition

Equipped with the [[Day convolution]] tensor product (prop. \ref{LydakisTensorProductIsDayConvolution}) the Lydakis model category 
of prop. \ref{LydakisModelStructure} becomes a [[monoidal model category]]

$$
  \left(
    [sSet^{\ast/}_{fin}, sSet^{\ast/}]_{Ly}, \; \wedge_{Day}
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The [[pushout product axiom]] is  ([Lydakis 98, theorem 12.3](#Lydakis98)).
Moreover ([Lydakis 98, theorem 12.4](#Lydakis98)), shows that tensoring with cofibrant objects preserves all stable weak equivalences, hence in particular preserves cofibrant resolution of the tensor unit.

=--


## Related concepts

* [[model structure on functors]]

* [[model structure for spectra]]

* [[model structure for n-excisive functors]]

## References

Model structure for [[excisive functors]] on [[simplicial sets]] (hence also a [[model structure for spectra]]) is discussed in:

* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))

A similar model structure on functors on topological spaces was given in

* [[William Dwyer]], _Localizations_, In _Axiomatic, enriched and motivic homotopy theory_, volume 131 of NATO Sci. Ser. II Math. Phys. Chem., pages 3&#8211;28. Kluwer Acad. Publ., Dordrecht, 2004

The [[functors with smash products]] ("FSP"s) appearing in ([Lydakis 98, remark 5.12](#Lydakis98)) had earlier been considered in 

* {#B&#246;kstedt86} [[Marcel Bökstedt]], _Topological Hochschild homology_. Preprint, Bielefeld, 1986

Further generalization of the model structure for excisive functor, in particular to [[enriched functors]] and to a [[model structure for n-excisive functors]] for $n \geq 1$ is discussed in

* {#BiedermannChornyRondings06} [[Georg Biedermann]], [[Boris Chorny]], Oliver R&#246;ndigs, _Calculus of functors and model categories_, Advances in Mathematics 214 (2007) 92-115 ([arXiv:math/0601221](http://arxiv.org/abs/math/0601221))

* [[Georg Biedermann]], Oliver R&#246;ndigs, _Calculus of functors and model categories II_ ([arXiv:1305.2834v2](http://arxiv.org/abs/1305.2834v2))


[[!redirects model structure for excisive functors]]
[[!redirects model structures for excisive functors]]


[[!redirects model structure on excisive functors]]
[[!redirects model structures on excisive functors]]