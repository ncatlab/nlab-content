
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


A [[model category]] structure for [[excisive functors]] on [[functors]] from ([[finite homotopy type|finite]]) pointed simplicial setrs to pointed simplicial sets ([Lydakis 98, theorem 9.2](#Lydakis98),[Biedermann-Chorny-R&#246;ndings 06, section 9](#BiedermannChornyRondings06)), hence (see [here](excisive+%28∞%2C1%29-functor#SpectrumObjects)) a [[model structure for spectra]] ([Lydakis 98, theorem 11.3](#Lydakis98)). 

Special case of a [[model structure for n-excisive functors]].

## Definition

### The underlying category

+-- {: .num_defn #SimplicialSetsPointedAndFinite}
###### Definition

Write 

* [[sSet]] for the [[category]] of [[simplicial sets]];

* $sSet^{\ast/}$ for the category of [[pointed object|pointed]] simplicial sets;

* $sSet_{fin}^{\ast/}\simeq s(FinSet)^{\ast/}$ for the [[category]] of [[pointed object|pointed]] [[simplicial object|simplicial]] [[finite sets]] . 

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

The category we are interested in is the $sSet^{\ast/}$-[[enriched functor category]]

$$
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]
  \,.
$$

([Lydakis 98, example 3.8, def. 4.4](#Lydakis98))


## Properties

### Model structure for spectra
 {#ModelStructureForSpectra}

The model structure for 1-excisive functors (from pointed finite homotopy types to pointed homotopy types) is [[Quillen equivalence|Quillen equivalent]] to the [[Bousfield-Friedlander model structure]] [[model structure for spectra|for spectra]] ([Lydakis 98, theorem 11.3](#Lydakis98)).

### Symmetric monoidal smash product
 {#SmashProduct}


The [[excisive functors]] naturally carry a [[smash product]] ([Lydakis 98, def. 5.1](#Lydakis98)) making the model structure for 1-excisive functors a [[symmetric monoidal model category]] ([Lydakis 98, section 12](#Lydakis98)), hence a [[symmetric smash product on spectra]]. A  [[monoid]] with respect to this smash product (hence a [[ring spectrum]]) is equivalently a [[functor with smash products]] ("FSP") as earlier considered in ([B&#246;kstedt 86](#B&#246;kstedt86)).

+-- {: .num_prop }
###### Proposition

The smash product on $[sSet^{\ast/}_{fin}, sSet^{\ast/}]$ of ([Lydakis 98, def. 5.1](#Lydakis98)) is the [[Day convolution product]] with respect to the plain [[smash product]] of [[pointed objects]] $\wedge \colon sSet^{\ast/} \times sSet^{\ast/} \longrightarrow sSet^{\ast/}$ .

=--

+-- {: .proof}
###### Proof

As in ([MMSS00](Day%20convolution#MMSS00)), the Day convolution product is characterized by making a [[natural isomorphism]] of the form

$$
  [sSet^{\ast/}_{fin}, sSet^{\ast/}](X \wedge Y, Z) \simeq [sSet^{\ast/}_{fin} \times sSet^{\ast/}_{fin}, sSet^{\ast/}](X \overline{\wedge} Y, Z \circ \wedge)
$$

where the _external smash product_ $\overline{\wedge}$ on the right is defined by $X \overline{\wedge} Y  \coloneqq  \wedge \circ (X,Y) $. Now, ([Lydakis 98, def. 5.1](#Lydakis98)) sets 

$$
  X \wedge Y \coloneqq \wedge_\ast (X \overline{\wedge} Y) 
$$

where, by ([Lydakis 98, prop. 3.23](#Lydakis98)),  $\wedge_\ast$ is the [[left adjoint]] to $\wedge^\ast(-) \coloneqq (-)\circ \wedge$. Hence the [[adjunction]] isomorphism gives the above characterization.

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




