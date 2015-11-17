
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _super line 2-bundle_ is a [[line 2-bundle]] in ([[higher geometry|higher]]) [[supergeometry]].

We discuss line 2-bundles in [[supergeometry]] and their relation to [[twisted K-theory]]. This follows the discussion in chapter 1 of ([Freed](#Freed12)), which in turn follows the classical text ([Donovan-Karoubi](#DonovanKaroubi)) on [[twisted K-theory]] and ([Wall](#Wall)) on _[Picard 2-groupoids of superalgebras](super+algebra#Picard2Groupoid)_. What we add to this here, following ([Fiorenza-Sati-Schreiber 12](#FSS)) is that we make explit the incarnation of these constructions as the [[∞-stack|higher stack]] on [[supermanifolds]] $2\mathbf{sLine}$ of super line 2-bundles. This is a supergeometric refinement of the [[moduli infinity-stack|moduli 2-stack]] $\mathbf{B}^2\mathbb{C}^\times$ for bare complex line 2-bundles, $\mathbb{C}^\times$-[[principal 2-bundles]].


## Definition

+-- {: .num_defn}
###### Definition

Let $\mathbf{H} \coloneqq $ [[SmoothSuper∞Grpd]] be the [[cohesive (∞,1)-topos]] of [[SmoothSuper∞Grpd|smooth super-∞-groupoids]]. With [[CartSp]]${}_{th}$ the [[site]] given by the [[full subcategory]] of the category of [[supermanifolds]] on those of the form $\mathbb{R}^{p|q}$ for $p,q \in \mathbb{N}$ this is the corresponding [[(∞,1)-category of (∞,1)-sheaves]]

$$
  SmoothSuper\infty Grpd \simeq Sh_\infty(CartSp_{th})
$$

This is cohesive over [[Super∞Grpd]] $ \simeq Sh_\infty(SuperPoints)$

$$
  \Gamma \colon SmoothSuper\infty Grpd  \to Super \infty Grpd
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

Let $\mathbb{K} \in \mathbf{H}$ be the canonical [[affine line|affine]] [[line object]], whose underlying sheaf of sets assigns 

$$
  \mathbb{K} \colon \mathbb{R}^{p|q} \mapsto C^\infty(\mathbb{R}^p, \mathbb{C})\otimes (\wedge^\bullet \mathbb{C}^q)_{even}
 \,.
$$

=--

+-- {: .num_remark}
###### Remark

By the discussion at _[[superalgebra]]_ we have that $\Gamma(\mathbb{K})$-algebras in [[Super∞Grpd]] are, externally, superalgebras over the [[complex numbers]].

=--

+-- {: .num_defn}
###### Defintion

Write

$$
  2\mathbf{sVect} \in SmoothSuper \infty Grpd
$$

for the object which over $\mathbb{R}^{p|q}$ is the [[2-groupoid]] whose 

* objects are semisimple $\mathbb{K}(\mathbb{R}^{p|q})$-algebras;

* [[1-morphisms]] are invertible [[bimodules]];

* [[2-morphisms]] are invertible bimodule homomorphisms.

This is naturally a [[braided monoidal 2-category]] object. Write

$$
 2 \mathbf{sLine} \in SmoothSuper \infty Grpd
$$

for the maximal [[braided 3-group]] inside this on the invertible objects.

=--

## Properties

We now want to analyse the super 2-stack $2 \mathbf{sLine}$. In order to do so, first notice the following classical results about the [[Picard 3-group]] of superalgebras.

### The Brauer 3-group of superalgebras

+-- {: .num_theorem #AzumayaAreCentralSimple}
###### Theorem

A superalgebra is invertible/Azumaya (see [here](super+algebra#Azumaya)) precisely if it is finite dimensional and central simple (see [here](super+algebra#CentralSimple)).

=--

This is due to ([Wall](#Wall)).

+-- {: .num_theorem }
###### Theorem

The [[Brauer group]] of superalgebras over the [[complex numbers]] is the [[cyclic group of order 2]]. That over the [[real numbers]] is cyclic of order 8:

$$
  sBr(\mathbb{C}) \simeq \mathbb{Z}_2
$$
$$
  sBr(\mathbb{R}) \simeq \mathbb{Z}_8
  \,.
$$

The non-trivial element in $sBr(\mathbb{R})$ is that presented by the superalgebra $\mathbb{C} \oplus \mathbb{C} u$ of the example [here](super+algebra#ComplexCl1), with $u \cdot u = 1$.

=--

This is due to ([Wall](#Wall)).

The following generalizes this to the higher [[homotopy groups]].

+-- {: .num_prop }
###### Proposition

The [[homotopy groups]] of the [[braided 3-group]] $sAlg^\times$ of Azumaya superalgebra are

| | $sAlg^\times_{\mathbb{C}}$ | $sAlg^\times_{\mathbb{R}}$ |
|--|--|--|
| $\pi_2$ | $\mathbb{C}^\times$ | $\mathbb{R}^\times$
| $\pi_1$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$
| $\pi_0$ | $\mathbb{Z}_2$ | $\mathbb{Z}_8$

where the [[groups of units]] $\mathbb{C}^\times$ and $\mathbb{R}^\times$ are regarded as [[discrete groups]].

=--

This is recalled for instance in ([Freed 12, (1.38)](#Freed12)).

### The homotopy type of the 2-stack of super 2-lines
 {#HomtopyTypeOfSuper2Lines}

Now we can analyse the super 2-stack $2\mathbf{sLine}$ of super 2-line 2-bundles.

+-- {: .num_prop}
###### Proposition

The object $2\mathbf{sLine} \in SmoothSuper\infty Grpd$ is equivalent to that which to $\mathbb{R}^{p|q}$ assigns the 2-groupoid whose

* objects are the algebra $C^\infty(\mathbb{R}^p, \mathbb{C})\otimes (\wedge^\bullet \mathbb{C}^q)_{even}$ and that algebra tensored with $Cl_1(\mathbb{C})$;

* morphisms are $C^\infty(\mathbb{R}^p, \mathbb{C})\otimes (\wedge^\bullet \mathbb{C}^q)_{even}$ regarded as a bimodule over itself and that bimodule tensored with $Cl_1(\mathbb{C})$;

* 2-morphisms form the group $C^\infty(\mathbb{R}^p, \mathbb{C}^\times)$.

=--

+-- {: .proof}
###### Proof

First, the $\mathbb{K}$-algebras in the topos of supergeometry are externally the ordinary [[superalgebras]], by the discussion at _[superalgebra -- As algebras in the topos over superpoints](super+algebra#AlgebraOverSuperpoints)_. 

With this the statement is a straightforward generalization of the discussion at  _[superalgebra -- Picard 2-groupoid](super+algebra#Picard2Groupoid)_ from superalgebras over $\mathbb{C}$ to those over $C^\infty(\mathbb{R}^p, \mathbb{C})$.

While the invertible ordinary $\mathbb{C}^\infty(\mathbb{R})$-algebras are equivalent to that algebra itself (hence there is only one, up to equivalence); the invertible superalgebras are equivalent either to the ground field or to the complex [[Clifford algebra]] $Cl_1(\mathbb{C})$ (hence there are two, up to equivalence, the two elements in the [[Brauer group]] $\mathbb{Z}_2 = \pi_0(2\mathbf{sLine})$ ). Similarly for the invertible bimodules. Finally the invertible intertwiners are pointwise $\mathbb{C}^\times$.

=--

It follows that

+-- {: .num_prop }
###### Proposition

The [[homotopy groups]] of the [[geometric realization]] 
${\vert 2\mathbf{sLine} \vert}$ of $2\mathbf{sLine}$ are

| | ${\vert 2\mathbf{sLine}_{\mathbb{C}} \vert}$ | ${\vert 2\mathbf{sLine}_{\mathbb{R}} \vert}$ |
|--|--|--|
| $\pi_3$ | $\mathbb{Z}$ | $\mathbb{Z}$ |
| $\pi_2$ | 0 | 0 |
| $\pi_1$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ |
| $\pi_0$ | $\mathbb{Z}_2$ | $\mathbb{Z}_8$ |


=--


+-- {: .num_remark}
###### Remark

Therefore we have a canonical morphism

$$
  \mathbf{B}^2 \mathbb{C}^\times \simeq 2\mathbf{Line} \to 2\mathbf{sLine}
$$

in [[SmoothSuper∞Grpd]] (a [[n-monomorphism|2-monomorphism]]) from the [[moduli ∞-stack|moduli 2-stack]] of $\mathbb{C}^\times$-[[principal 2-bundles]]/[[bundle gerbes]], which picks the "ordinary" super 2-line bundle (as opposed to its "superpartner"), ignores the odd auto-[[gauge transformations]] of that and keeps all the [[higher gauge transformations]].

=--

+-- {: .num_remark}
###### Remark

In [[bosonic string theory]] over a [[spacetime]] $X$ the [[background gauge field]] called the [[B-field]] is a line 2-bundle [[circle n-bundle with connection|with connection]] given by a morphism 

$$
  X \to 2\mathbf{Line} \simeq \mathbf{B}^2 \mathbb{C}^\times
  \,.
$$

However in [[type II superstring theory]] the [[B-field]] is actually a super line 2-bundle, hence given by a morphism

$$
  X \to 2\mathbf{sLine} 
$$

in [[SmoothSuper∞Grpd]]. This observation (formulated in less stacky language) is due to the analysis of [[orientifold]] background fields in ([Precis](#Precis)).

=--

+-- {: .num_prop #FirstKInvariant}
###### Proposition

The first [[k-invariant]] of $\vert 2\mathbf{sLine}\vert$ is the essentially unique nontrivial

$$
  \mathbb{Z}_2 \to \mathbf{B}^2 \mathbb{Z}_2
$$

given by the [[Steenrod square]]. This is represented by the [[braided monoidal category|braiding]] equivalence on the [[tensor product]] of $Cl_1^{\mathbb{C}} \simeq \langle 1, e\rangle_{[e^2 = 1]}$ 

$$
  Cl_1^{\mathbb{C}}
  \otimes_{\mathbb{C}}
  Cl_1^{\mathbb{C}}
  \stackrel{\simeq}{\to}
  Cl_1^{\mathbb{C}}
  \otimes_{\mathbb{C}}
  Cl_1^{\mathbb{C}}
$$

given by the algebra homomorphism


$$
  \begin{aligned}
    1 \otimes 1 & \mapsto 1 \otimes 1
    \\
    e \otimes e & \mapsto - e \otimes e
    \\
    1 \otimes e & \mapsto e \otimes 1
    \\
    e \otimes 1 & \mapsto 1 \otimes e
  \end{aligned}
$$

(exchange the tensor factors and introduce a sign when exchanging two odd graded ones).

=--

For instance ([Freed 12, 1.42](#Freed12)).

+-- {: .num_prop #SecondKInvariant}
###### Proposition

The second [[k-invariant]]

$$
  \mathbf{B}\mathbb{Z}_2 \to \mathbf{B}^4 \mathbb{Z}
$$

is the delooping of that of super lines $\mathbf{sLine}$, being the image under the [[Bockstein homomorphism]] of

$$
  \mathbf{B}\mathbb{Z}_2 \to \mathbf{B}^3 U(1)
$$

which sends $\mathbb{Z}_2 \times \mathbb{Z}_2 \times \mathbb{Z}_2 \to \mathbb{Z}_2 \hookrightarrow U(1)$.


(...)


=--

For instance ([Freed 12, 1.44](#Freed12)).


+-- {: .num_remark}
###### Remark

Comparison with the notation and terminology of 
([Freed-Hopkins-Teleman 07](#FreedHopkinsTeleman)):

the "$\mathcal{B}\mathbb{T}^{\pm}$" on the top of p. 14 there is 
$\Omega (2\mathbf{sLine})$ here; a graded line bundle over some $X$ there is a map of stacks $X \to \Omega (2\mathbf{sLine})$ here.

For $X$ 1-truncated, hence a groupoid, a graded central extension in the sense there is a map $X \to 2\mathbf{sLine}$ which factors as 
$X \to \mathbf{B}\Omega (2\mathbf{sLine}) \to 2\mathbf{sLine}$.

=--

### Relation to the unconnected delooping of the $\infty$-group of units of $KU$
 {#RelationToUnconnectedDeloopingOfUnitsOfKU}

In ([Sagave 11](#Sagave11)) is introduced a "non-connected delooping" $bgl_1^\ast(E)$ of the [[∞-group of units]] $gl_1(E)$ of an [[E-∞ ring]] $E$, fitting into a [[homotopy cofiber sequence]]

$$
  gl_1(E) \to gl_1^J(E) \to \mathbb{S} \to bgl_1^\ast(E)
  \,.
$$


See at _[∞-Group of units -- Augmented definition](infinity-group+of+units#AugmentedDefinition)_.

By ([Sagave 11, theorem 12 and example 4.10](#Sagave11)) and comparing to the above discussion we have an [[equivalence]]

$$
  {\vert 2\mathbf{sLine}\vert}
  \simeq
  bgl_1^\ast(KU) \langle0,..,4\rangle
$$

of the [[geometric realization]] of the super-2-stack of super line 2-bundles with the [[n-truncated object in an (infinity,1)-category|4-truncation]] of the connected delooping of the [[infinity-group of units]] of $KU$.

hitting the Donovan-Karoubi twists of K-theory. This is what in ([Freed-Distler-Moore](#Precis), [Freed](#Freed12)) is written $R^{-1}$.

(...)

## References

Line 2-bundles in [[supergeometry]] as a model for the [[B-field]] and [[orientifolds]] are discussed (even if not quite explicitly in the language of higher bundles) in 

* {#Freed12} [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_, lectures at ESI Vienna, 2012 ([[FreedESI2012.pdf:file]])

based on the old results about the [[Picard 2-groupoid]] of complex [[super algebras]]

* {#Wall} [[C. T. C. Wall]], _Graded Brauer groups_, J. Reine Angew. Math. 213 (1963/1964), 187-199. 
 
and based on the discussion of [[twisted K-theory]] in 

* {#DonovanKaroubi} [[Peter Donovan]], [[Max Karoubi]], _Graded Brauer groups and $K$-theory with local coefficients_, Publications Math&#233;matiques de l'IH&#201;S, 38 (1970), p. 5-25  ([numdam](http://www.numdam.org/item?id=PMIHES_1970__38__5_0))
 

as refined in 

* {#FreedHopkinsTeleman} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Loop groups and twisted K-theory I_,  Journal of Topology (2011) 4 (4): 737-798 ([arXiv:0711.1906](http://arxiv.org/abs/0711.1906)) 
 

and developing constructions in 

* {#Precis} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))
 
See also

* [[Tadeusz Józefiak]], _Semisimple Superalgebras_,  Volume 1352 of the series Lecture Notes in Mathematics pp 96-113.


Similar comments appear earlier on p. 8 and following of

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Consistent Orientation of Moduli Spaces_ ([arXiv:0711.1909](http://arxiv.org/abs/0711.1909))

The above higher supergeometric story is made explicit in 

* {#FSS} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_
 

The "unconnected delooping" of the [[infinity-group of units]] of an $E_\infty$-ring $E$ is introduced in 

* {#Sagave11} [[Steffen Sagave]], _Spectra of units for periodic ring spectra_ ([arXiv:1111.6731](http://arxiv.org/abs/1111.6731))
 
and the specific example for the case of  $E = KU$ is in example 4.10 there.

[[!redirects super line 2-bundles]]

[[!redirects super 2-line bundle]]
[[!redirects super 2-line bundles]]