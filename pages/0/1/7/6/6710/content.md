


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

### Topological

For $n \in \mathbb{N}$ the [[Lie group]] [[spin^c|spin<sup><i>c</i></sup>]] is a [[central extension]] 

$$
  U(1) \to Spin^c(n) \to SO(n)
$$

of the [[special orthogonal group]] by the [[circle group]]. This comes with a long [[fiber sequence]]

$$
  \cdots \to B U(1) \to B Spin^c(n)  \to B SO(n) \stackrel{W_3}{\to} B^2 U(1)
  \,,
$$

where $W_3$ is the _third [[integral Stiefel-Whitney class]]_ . 

An [[oriented]] manifold $X$ **has $Spin^c$-structure** if the [[characteristic class]] $[W_3(X)] \in H^3(X, \mathbb{Z})$

$$
  W_3(X) \coloneqq W_3(T X) 
  \;\colon\;
  X \stackrel{T X}{\to} B SO(n) \stackrel{W_3}{\to} B^2 U(1) \simeq K(\mathbb{Z},3)
$$

is trivial. This is the [[Dixmier-Douady class]] of the [[circle n-bundle|circle 2-bundle]]/[[bundle gerbe]] that [[obstruction|obstructs]] the existence of a $Spin^c$-[[principal bundle]] [[lift of structure group|lifting]] the given [[tangent bundle]].

A manifold $X$ is **equipped with $Spin^c$-structure** $\eta$ if it is equipped with a choice of trivializaton 

$$
  \eta : 1 \stackrel{\simeq}{\to} W_3(T X)
  \,.
$$

The [[homotopy type]]/[[∞-groupoid]] of $Spin^c$-structures on $X$ is the [[homotopy fiber]] $W_3 Struc(T X)$ in the [[pasting diagram]] of [[homotopy pullback]]s

$$
  \array{
    W_3 Struc(T X) &\to& W_3 Struc(X) &\to& * 
    \\
    \downarrow && \downarrow && \downarrow 
    \\
    * &\stackrel{T X}{\to}& Top(X, B SO(n)) 
    &\stackrel{W_3}{\to}&
    Top(X,B^2 U(1))
  }
  \,.
$$

If the class does not vanish and if hence there is no $Spin^c$-structure, it still makes sense to discuss the structure that remains as _[[twisted spin^c structure|twisted spin<sup><i>c</i></sup> structure]]_ . 


### Smooth

Since $U(1) \to Spin^c \to SO$ is a sequence of [[Lie group]]s, the above may be lifted from the [[(∞,1)-topos]] $L_{whe}$ [[Top]] $\simeq$ [[∞Grpd]] of [[discrete ∞-groupoids]] to that of [[smooth ∞-groupoids]], [[Smooth∞Grpd]].

More in detail, by the discussion at [[Lie group cohomology]] (and [[smooth ∞-groupoid -- structures]]) the characteristic map $W_3 : B SO \to B^2 U(1)$ in $\infty Grpd$ has, up to equivalence, a unique lift

$$
  \mathbf{W}_3 : \mathbf{B} SO \to \mathbf{B}^2 U(1)
$$

to [[Smooth∞Grpd]], where on the right we have the [[delooping]] of the smooth [[circle n-group|circle 2-group]]. 

Accordingly, the [[2-groupoid]] of _smooth $spin^c$-structures_ $\mathbf{W}_3 Struc(X)$ is the joint [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{W}_3 Struc(T X) &\to& \mathbf{W}_3 Struc(X) &\to& * 
    \\
    \downarrow && \downarrow && \downarrow 
    \\
    * &\stackrel{T X}{\to}& Smooth \infty Grpd(X, \mathbf{B} SO(n)) 
    &\stackrel{\mathbf{W}_3}{\to}&
    Smooth \infty Grpd(X,\mathbf{B}^2 U(1))
  }
  \,.
$$

### Higher $spin^c$-structures
 {#Higher}

In parallel to the existence of [higher spin structures](spin+structure#Higher) there are higher analogs of $Spin^c$-structures, related to [[quantum anomaly]] cancellation of theories of higher dimensional [[branes]].

* [[string^c structure|string<sup><i>c</i></sup> structure]]



## Properties

### Of $Spin^c$
 {#PropertiesOfSpinC}

+-- {: .num_defn}
###### Definition

The group $Spin^c$ is the [[fiber product]]

$$
  \begin{aligned}
    Spin^c & := Spin \times_{\mathbb{Z}_2} U(1)
    \\
    & = (Spin \times U(1))/{\mathbb{Z}_2}
    \,,
  \end{aligned}
$$

where in the second line the [[action]] is the diagonal action induced from the two canonical embeddings of [[subgroups]] $\mathbb{Z}_2 \hookrightarrow \mathbb{Z}$
and $\mathbb{Z}_2 \hookrightarrow U(1)$.

=--

+-- {: .num_prop #SpinCAsHomotopyFiberProductW2C1}
###### Proposition

We have a [[homotopy pullback]] diagram

$$
  \array{
     \mathbf{B} Spin^c &\to& \mathbf{B}U(1)
     \\
     \downarrow && \downarrow^{\mathrlap{\mathbf{c}_1 mod 2}}
     \\
     \mathbf{B} SO &\stackrel{w_2}{\to}&
     \mathbf{B}^2 \mathbb{Z}_2 
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

We present this as usual by [[simplicial presheaves]] and [[∞-anafunctors]].

The first [[Chern class]] is given by the [[∞-anafunctor]]

$$
  \array{
     \mathbf{B}(\mathbb{Z} \to \mathbb{R})
     &\stackrel{c_1}{\to}&
     \mathbf{B}(\mathbb{Z} \to 1)
     = 
     \mathbf{B}^2 \mathbb{Z}
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{B} U(1)     
  }
  \,.
$$

The second [[Stiefel-Whitney class]] is given by

$$
  \array{
    \mathbf{B}(\mathbb{Z}_2 \to Spin)
    &\stackrel{w_2}{\to}&
    \mathbf{B}(\mathbb{Z}_2 \to 1)
    = 
    \mathbf{B}^2 \mathbb{Z}_2
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B} SO
  }
  \,.
$$

Notice that the top horizontal morphism here is a [[fibration]].

Therefore the [[homotopy pullback]] in question is given by the ordinary pullback

$$
  \array{
    Q
    &\to& 
    \mathbf{B}(\mathbb{Z} \to \mathbb{R})
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}(\mathbb{Z}_2 \to Spin)
    &\to&
    \mathbf{B}^2 \mathbb{Z}_2
  }
  \,.
$$

This pullback is $\mathbf{B}(\mathbb{Z} \stackrel{\partial}{\to} Spin \times \mathbb{R})$, where 

$$
  \partial : n \mapsto ( n mod 2 , n)
  \,.
$$

This is equivalent to 

$$
  \mathbf{B}(\mathbb{Z}_2 \stackrel{\partial'}{\to} Spin \times U(1))
$$

where now

$$
  \partial' : \sigma \mapsto (\sigma, \sigma)
  \,.
$$

This in turn is equivalent to 

$$
  \mathbf{B} (Spin \times_{\mathbb{Z}_2} U(1))
  \,,
$$

which is the original definition.

=--

This factors the above characterization of $\mathbf{B}Spin^c$ as the homotopy fiber of $\mathbf{W}_3$:

+-- {: .num_prop }
###### Proposition

We have a [[pasting diagram]] of [[homotopy pullbacks]] of [[smooth infinity-groupoids]] of the form

$$
  \array{
    \mathbf{B} Spin^c &\to& \mathbf{B}U(1) &\to& \ast
    \\
    \downarrow && \downarrow^{\mathrlap{c_1 \, mod\, 2}}
    && \downarrow
    \\
   \mathbf{B}SO 
    &\stackrel{\mathbf{w}_2}{\to}&
   \mathbf{B}^2 \mathbb{Z}_2
   &\stackrel{\mathbf{\beta}_2}{\to}&
   \mathbf{B}^2 U(1)
  }
  \,.
$$

=--


This is discussed at _[Spin^c -- Properties -- As the homotopy fiber of smooth w3](spin%5Ec#AsHomotopyFiberOfSmoothW3)_.

### As $KU$-orientation

For $X$ an [[orientation|oriented]] [[manifold]], the map $X \to \ast$ is [[orientation in generalized cohomology|generalized oriented]] in [[periodic complex K-theory]] precisely if $X$ has a $Spin^c$-structure.

### Relation to metaplectic structures
 {#RelationToMetaplecticStructures}

Let $(X,\omega)$ be a [[compact topological space|compact]] [[symplectic manifold]] equipped with a [[Kähler polarization]] $\mathcal{P}$ hence a [[Kähler manifold]] structure $J$. A [[metaplectic structure]] of this data is a choice of square root $\sqrt{\Omega^{0,n}}$ of the [[canonical line bundle]]. This is equivalently a [[spin structure]] on $X$ (see the discussion at _[[Theta characteristic]]_).

Now given a [[prequantum line bundle]] $L_\omega$, in this case the [Dolbault quantization](geometric+quantization#IndexOfDolbeaultDiracOperator) of $L_\omega$ coincides with the [[spin^c quantization|spin<sup><i>c</i></sup> quantization]] of the [[spin^c structure|spin<sup><i>c</i></sup> structure]] induced by $J$ and $L_\omega \otimes \sqrt{\Omega^{0,n}}$.

This appears as ([Paradan 09, prop. 2.2](#Paradan09)).






## Examples

### From almost complex structures
 {#FromAlmostComplexStructures}

An [[almost complex structure]] canonically induces a $Spin^c$-structure:

+-- {: .num_prop}
###### Proposition

For all $n \in \mathbb{N}$ we have a homotopy-[[commuting diagram]]

$$
  \array{
    \mathbf{B}U(n) &\to& \mathbf{B}U(1)
    \\
    \downarrow 
     &\swArrow& 
    \downarrow^{\mathrlap{\mathbf{c_1} mod 2}}
    \\
    \mathbf{B}SO(2n) &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
  }
  \,,
$$

where the vertical morphism is the canonical morphism induced from the identification of real vector spaces $\mathbb{C} \to \mathbb{R}^2$, and where the top morphism is the canonical projection $\mathbf{B}U(n) \to \mathbf{B}U(1)$ (induced from $U(n)$ being the [[semidirect product group]] $U(n) \simeq SU(n) \rtimes U(1)$).

=--

+-- {: .proof}
###### Proof

By the general relation between $c_1$ of an [[almost complex structure]] and $w_2$ of the underlying orthogonal structure, discussed at _[Stiefel-Whitney class -- Relation to Chern classes](#Stiefel-Whitney+class#RelationToChernClasses)_.

=--

+-- {: .num_remark}
###### Remark


By prop. \ref{SpinCAsHomotopyFiberProductW2C1} and the [[universal property]] of the [[homotopy pullback]] this induces a canonical morphism

$$  
  k \colon \mathbf{B}U(n) \to \mathbf{B}Spin^c
  \,.
$$

=--

and this is the universal morphism from almost complex structures:

+-- {: .num_defn}
###### Definition


For $c \colon X \to \mathbf{B}U(n)$ modulating an [[almost complex structure]]/[[complex vector bundle]] over $X$, the composite

$$
  k c \colon X \stackrel{c}{\to} \mathbf{B}U(n) \stackrel{k}{\to} \mathbf{B}Spin^c
$$

is the corresponding $Spin^c$-structure.

=--

## Related concepts

* [[spin^c|spin<sup><i>c</i></sup>]], [[MSpin^c|MSpin<sup><i>c</i></sup>]]

* [[twisted differential c-structures|(twisted, differential) c-structures]]

  * [[orientation]]

  * [[spin structure]], [[twisted spin structure]], [[differential spin structure]]

    **$spin^c$ structure**, [[twisted spin^c structure|twisted spin<sup><i>c</i></sup> structure]],

    [[K-orientation]]

    [[Spin^c Dirac operator|Spin<sup><i>c</i></sup> Dirac operator]]

  * [[Spin^h structure]]

  * [[string structure]], [[twisted differential string structure]],

  * [[string^c 2-group|string<sup><i>c</i></sup> 2-group]], [[string^c structure|string<sup><i>c</i></sup> structure]]

  * [[fivebrane structure]], [[twisted differential fivebrane structure]]

* [[spin^c quantization|spin<sup><i>c</i></sup> quantization]]


## References

### General

A canonical textbook reference is

* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], Appendix D in: _[[Spin geometry]]_, Princeton University Press (1989)

Other accounts include

* Blake Mellor, _$Spin^c$-manifolds_ ([[BlakeSpinC.pdf:file]])

* _Stable complex and $Spin^c$-structures_ ([[StableComplexSpinC.pdf:file]])

* [[Peter Teichner]], Elmar Vogt, _All 4-manifolds have $Spin^c$-structures_ ([pdf](http://people.mpim-bonn.mpg.de/teichner/Papers/spin.pdf))

See also 

* {#Gompf97} [[Robert Gompf]], _$Spin^c$ structures and homotopy equivalences_, Geom. Topol. 1 (1997) 41-50 ([arXiv:math/9705218](https://arxiv.org/abs/math/9705218))


### As $KU$-orientation/anomaly cancellation in type II string theory

That the $U(1)$-[[gauge field]] on a [[D-brane]] in [[type II string theory]] in the absense of a [[B-field]] is rather to be regarded as part of a $spin^c$-structure was maybe first observed in 

* [[Edward Witten]], _Baryons and Branes In Anti de Sitter Space_, JHEP 9807:006 (1998) ([arXiv:hep-th/9805112](http://arxiv.org/abs/hep-th/9912086)).

The [[twisted spin^c structure|twisted spin<sup><i>c</i></sup> structure]] (see there for more details) on the [[worldvolume]] of [[D-branes]] in the presence of a nontrivial [[B-field]] was discussed in

* [[Daniel Freed]], [[Edward Witten]], _Anomalies in String Theory with D-Branes_ ([arXiv:hep-th/9907189](http://arxiv.org/abs/hep-th/9907189))

See at _[[Freed-Witten-Kapustin anomaly cancellation]]_.

A more recent review is provided in

* Kim Laine, _Geometric and topological aspects of Type IIB D-branes_ ([arXiv:0912.0460](http://arxiv.org/abs/0912.0460))

See also

* [[Hisham Sati]], _Geometry of $Spin$ and $Spin^c$ structures in the M-theory partition function_ ([arXiv:1005.1700](http://arxiv.org/abs/1005.1700))


The relation to [[metaplectic corrections]] is discussed in 

* {#Paradan09} [[Paul-Emile Paradan]], _Spin-quantization commutes with reduction_ ([arXiv:0911.1067](http://arxiv.org/abs/0911.1067))
 

See also

* O. Hijazi, S. Montiel, F. Urbano, _$Spin^c$-geometry of K&#228;hler manifolds and the Hodge Laplacian on minimal Lagrangian submanifolds_ ([pdf](http://hal.archives-ouvertes.fr/docs/00/09/81/71/PDF/lagrangian0412.pdf))

[[!redirects spin^c structure]]
[[!redirects spin^c structures]]
[[!redirects Spin^c structure]]
[[!redirects Spin^c structures]]
[[!redirects spin-c structure]]
[[!redirects spin-c structures]]
[[!redirects Spin-c structure]]
[[!redirects Spin-c structures]]

[[!redirects spin^c-structure]]
[[!redirects spin^c-structures]]
[[!redirects Spin^c-structure]]
[[!redirects Spin^c-structures]]
[[!redirects spin-c-structure]]
[[!redirects spin-c-structures]]
[[!redirects Spin-c-structure]]
[[!redirects Spin-c-structures]]

