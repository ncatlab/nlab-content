
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Dependent linear type theory is the combination of _[[dependent type theory]]_ and _[[linear type theory]]_, hence a [[type theory]] where linear types may dependent on ordinary intuitionistic types. An extension of the [[LF]] [[syntax]] by dependent linear types appears in ([Pfenning 96](#Pfenning96), [WCFW 03](#WCFW03)) and a dependent linear extension of [[system L]] in ([Spiwack 14, section 5](#Spiwack14)). What should be the [[categorical semantics]] of dependent linear type theory was discussed in ([Shulman 08](#Shulman08), [Ponto-Shulman 12](#PontoShulman12), [Shulman 12](#Shulman12), [Schreiber 14](#Schreiber14)). A proposal for an actual [[syntax]] for dependent linear type theory appears in ([V&#225;k&#225;r 14](#Vakar14)).


 
Following the notion of [[hyperdoctrine]] this should mean, in terms of [[categorical semantics]], that dependent linear type theory is for each [[context]] $\Gamma$ a [[linear type theory]]/possibly-non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal category|symmetric]] [[closed monoidal category]] $(\mathcal{C}_{\Gamma}, \otimes, 1)$ and for each [[homomorphism]] of [[contexts]] $f \;\colon\; \Gamma_1 \longrightarrow \Gamma_2$ functorially an [[adjoint triple]] of [[functors]]

$$
  (f_! \dashv f^\ast \dashv f_\ast) 
    \;\colon\; 
   \mathcal{C}_{\Gamma_1}
    \stackrel{\stackrel{f_!}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\longrightarrow}}{\underset{f_\ast}{\leftarrow}}}
    \mathcal{C}_{\Gamma_2}
  \,.
$$

where $f^\ast$ is [[context extension]] and where the [[left adjoint]] $f_!$ and [[right adjoint]] $f_\ast$ are to be thought of as linear analogs of [[dependent sum]] and [[dependent product]], respectively. Moreover this should satisfy [[Frobenius reciprocity]], hence $f^\ast$ should be a strong [[closed monoidal functor]]. 

Equivalently this is an [[indexed closed monoidal category]] with fiberwise [[dual object|duals]].

Typically one would in addition demand the [[Beck-Chevalley condition]] for consecutive such adjoint triples.

In [[geometry]]/[[topos theory]] such a "linear hyperdoctrine" is known as _[[six operations]] yoga in [[Wirthmüller context|Wirtmüller flavor]]_. In fact there this appears in [[geometric homotopy theory]] ("[[derived functors]] on [[quasicoherent sheaves]]") hence as _dependent linear [[homotopy type theory]]_.

## Semantic definition

We define here the [[categorical semantics]] that linear homotopy type theory is supposed to have. So its [[syntax|syntactic]] definition is to be such that at least all of the following constitute [[models]] for the theory. In order to indicate the semantic level we will try to keep a hyphen  in "linear homotopy-type theory".

### Dependent linear type theory

Notice that the following relation between syntax and semantics are well established (see at _[[relation between type theory and category theory]]_ for details):

|  [[syntax]] | [[semantics]] |
|-------------|---------------|
| [[linear type theory|multiplicative intuitionistic linear type theory]] | [[symmetric monoidal category|symmtric]] [[closed monoidal categories]] |
| [[dependent type theory]] | [[locally cartesian closed categories]] |

Here the correspondence in the second line works by forming for any [[locally cartesian closed category]] $\mathcal{C}$ its system of [[slice categories]] $[\Gamma] \mapsto \mathcal{C}_{/[\Gamma]}$, each of which is a [[cartesian monoidal category|cartesian]] [[closed monoidal category]], and then interpreting that as the [[semantics]] for [[dependent type theory]] in the [[context]] $\Gamma$:

$$
  \left\{
    \Gamma \vdash a \colon A 
  \right\}
  \leftrightarrow
  \left\{
     (\ast \stackrel{[a]}{\longrightarrow} [A])
     \in Mor(\mathcal{C}_{/[\Gamma]})
  \right\}
  \,.
$$

Moreover, the system of slice categories has good [[base change]] in that for every morphism $[f] \colon [\Gamma_1]\to [\Gamma_2]$ in $\mathcal{C}$ there is an [[adjoint triple]] of [[functors]]

$$ 
   \mathcal{C}_{[\Gamma_1]}
    \stackrel{\stackrel{[f]_!}{\longrightarrow}}{\stackrel{\overset{[f]^\ast}{\longrightarrow}}{\underset{[f]_\ast}{\leftarrow}}}
    \mathcal{C}_{[\Gamma_2]}
$$

satisfying [[Frobenius reciprocity]]. These serve as the semantics for the the [[context extension]] along a map $f\colon \Gamma_1 \to \Gamma_2$ of contexts, and for the [[dependent sum]] $\sum$, and the [[dependent product]] of the dependent type theory syntax, respectively:

$$
  \left\{
     \underset{f^{-1}(-)}{\sum}
     , \; f \;,
     \underset{f^{-1}(-)}{\prod}
  \right\}
  \leftrightarrow
  \left\{
    [f]_! \dashv [f]^\ast \dashv [f]_\ast  
  \right\}
  \,.
$$


Now since a [[cartesian monoidal category]] is in particular a [[symmetric monoidal category]], this immediately suggest to generalize the assignments
$[\Gamma] \mapsto (\mathcal{C}_{/[\Gamma]})^\times$ to assignments
$[\Gamma] \mapsto (\mathcal{C}_{[\Gamma]})^\otimes$ of [[symmetric monoidal categories]] (possibly but not necessarily the [[slice categories]] of $\mathcal{C}$) such that there still is good [[base change]] in the above way. The resulting structure may be called a _symmetric closed [[indexed monoidal category]]_.

So any $\mathcal{C}_{[\Gamma]}$ here is a [[symmetric monoidal category]] and hence is [[categorical semantics]] for [[linear types]], while at the same times these types depend on the "non-linear" type $[\Gamma]$. In this way the system ("[[hyperdoctrine]]") $[\Gamma] \mapsto (\mathcal{C}_{[\Gamma]})^\otimes$ is semantics a _dependent linear type theory_.

The [[syntax]] of which such "[[hyperdoctrines]] of [[symmetric monoidal categories]]" are the semantics should be called _dependent linear type theory_. This is fairly straightforward. Details are written out in ([Vakar 14](#Vakar14)).

+-- {: .num_defn #SemanticsForDependentLinearTypeTheory}
###### Definition

A _semantics for dependent linear type theory_ is

1. an [[category]] $\mathcal{C}$;

1. an [[functor]] $Mod \colon \mathcal{C}^{op} \to ClosedSymMonCat$ to [[symmetric monoidal categories]];

such that 

1. each $Mod(X)^\otimes$ is [[closed monoidal categor|closed]] (with [[internal hom]] to be denoted $[-,-]$);

1. for each $[f] \colon [\Gamma_1] \to [\Gamma_2]$ in $Mor(\mathcal{C})$ the assigned [[functor]] $f^\ast \colon Mod([\Gamma_2]) \to Mod([\Gamma_1])$ has a [[left adjoint]] $f_!$ and a [[right adjoint]] $f_\ast$;

1. $f_!$ satsifies [[Frobenius reciprocity]].

If in addition the [[Beck-Chevalley condition]] is satisfied by $(f_1\dashv f^\ast)$, then we speak of _linear homotopy-type theory with Beck-Chevalley condition_.

=--

+-- {: .num_defn }
###### Remark

That $f^\ast$ is a morphism of [[symmetric monoidal category]] means that it is a [[strong monoidal functor]], preserving the [[tensor product]]

$$
  f^\ast(X\otimes Y)\simeq (f^\ast X)\otimes (f^\ast Y)
  \,.
$$

The condition of [[Frobenius reciprocity]] is equivalent to $f^\ast$ also being a [[strong closed functor]] in that it preserves the [[internal hom]]

$$
  f^\ast [X,Y] \simeq [f^\ast X, f^\ast Y]
  \,.
$$

In total a semantics for linear dependent type theory is hence a natural system of six functors

$$
  (f_! \dashv f^\ast),\; (f^\ast \dashv f_\ast),\; (\otimes \dashv [-,-])
$$

satisfying some compatibility conditions. This is precisely Grothendieck's [[yoga of six functors]] for the special case that the right adjoint of $f_!$ coincides with the left adjoint of $f_\ast$. This special case is also known as the _[[Wirthmüller context]]_ version of the yoga of six functors.


=--


+-- {: .num_defn}
###### Definition (Notation)

In view of the perspective of semantics for type theory, we will omit in the following the notational distinction between contexts and the objects that interpret them, and between dependent sum/product and the functors that interpret them. We will write the [[base change]] as

$$
   \left(
     \underset{f}{\sum}
     \dashv 
     f^\ast
     \dashv
     \underset{f}{\prod}
   \right)  
    \;\colon\; 
   Mod(\Gamma_1)
    \stackrel{\stackrel{f_!}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\longrightarrow}}{\underset{f_\ast}{\leftarrow}}}
    Mod(\Gamma_2)
  \,.
$$

=--

The statement of [[Frobenius reciprocity]] then equivalently reads as

$$
  \underset{f}{\sum}
  \left(
    X \otimes f^\ast Y
  \right)
  \simeq
  \left(
    \underset{f}{\sum} X 
  \right)
  \otimes 
  Y
  \,.
$$





### Linear homotopy type theory


All this has a straightforward refinement to [[homotopy theory]]. To appreciate this, notice that the following relation is well established (see again at _[[relation between type theory and category theory]]_ for details):


|  [[syntax]] | [[semantics]] |
|-------------|---------------|
| [[homotopy type theory]]  | [[locally cartesian closed (∞,1)-categories]] |
| [[homotopy type theory]] with [[univalence|univalent]] weak [[type universes]] | [[(∞,1)-toposes]] |

This works very much along the lines of the above relation between [[dependent type theory]] and [[locally cartesian closed categories]]. The central new ingredient is that one requires the locally cartesian closed category $\mathcal{C}$ to be equipped with a suitable structure of a [[model category]]. Using this there is then a notation of [[fibrant replacement]] of morphisms. The key point is that where in [[extensional type theory]] the [[identity type]] $(X \vdash Id_X \colon Type)$ of a type $X$ has semantics given by the [[diagonal]] morphism $\Delta_{[X]} \in \mathcal{C}_{/{[X]}}$, here in [[homotopy type theory]] it has semantics in the [[fibrant replacement]] $\hat \Delta_{[X]} \in \mathcal{C}_{/X}$. Such a fibrant replacement of the diagonal is [[path space object]] of $X$, reflecting the [[equivalences]]/[[homotopies]] "inside" the type $X$.

Taking all this together, we set:

+-- {: .num_defn #SemanticsForLinearHomotopyTypeTheory}
###### Definition

A _semantics for linear homotopy type theory_ is

1. an [[(∞,1)-category]] $\mathcal{C}$;

1. an [[(∞,1)-functor]] $Mod \colon \mathcal{C}^{op} \to SymMonCat_\infty$ to closed [[symmetric monoidal (∞,1)-categories]];


such that 

1. each $Mod(X)$ is closed;

1. for each $[f] \colon [\Gamma_1] \to [\Gamma_2]$ in $Mor(\mathcal{C})$ the assigned [[(∞,1)-functor]] $f^\ast \colon Mod([\Gamma_2]) \to Mod([\Gamma_1])$ has a [[left adjoint]] $f_!$ and a [[right adjoint]] $f_\ast$;

1. $f_!$ satsifies [[Frobenius reciprocity]].

If in addition the [[Beck-Chevalley condition]] is satisfied by $(f_1\dashv f^\ast)$, then we speak of _linear homotopy-type theory with Beck-Chevalley condition_.

=--

For brevity we will omit in the following the notational distinction between contexts and the objects that interpret them, and between dependent sum/product and the functors that interpret them. We will write the [[base change]] as

$$
   \left(
     \underset{f}{\sum}
     \dashv 
     f^\ast
     \dashv
     \underset{f}{\prod}
   \right)  
    \;\colon\; 
   Mod(\Gamma_1)
    \stackrel{\stackrel{f_!}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\longrightarrow}}{\underset{f_\ast}{\leftarrow}}}
    Mod(\Gamma_2)
  \,.
$$

The statement of [[Frobenius reciprocity]] then is that 

$$
  \underset{f}{\sum}
  \left(
    X \otimes f^\ast Y
  \right)
  \simeq
  \left(
    \underset{f}{\sum} X 
  \right)
  \otimes 
  Y
  \,.
$$



## Examples

### Slices of a topos

For $\mathbf{H}$ a [[topos]] and $f \colon X \longrightarrow Y$
any [[morphism]], then in the induced [[base change]] [[etale geometric morphism]]

$$
  (\sum_f \dashv f^\ast \dashv \prod_f)
  \;\colon\;
  \mathbf{H}_{/X}
  \longrightarrow
  \mathbf{H}_{/Y}
$$

the [[inverse image]]/[[context extension]] is a [[cartesian closed functor]] (see there for the proof). Therefore any base change of [[toposes]] constitutes a cartesian Wirthm&#252;ller context.

Conversely, this means that systems of Wirthm&#252;ller contexts are generalizations of [[categorical logic]] ([[hyperdoctrines]]) to non-cartesian contexts (see at _[[dependent linear type theory]]_). 

Notice that in a cartesian Wirthm&#252;ller context duality is trivial, in that $\mathbb{D}X \simeq 1$ for all objects $X$. Therefore to the extent that the [[six operations]] yoga involves duality, it is interesting only the more non-cartesian (non-classical) the ambient Wirthm&#252;ller context is.

For instance the [[projection formula]] $\overline{\gamma}$ in def. \ref{ComparisonMaps} for base change along a pointed connected type $\mathbf{B}G \to \ast$ equivalently says that genuine ([[Bredon cohomology|Bredon]]) [[equivariant cohomology]] reduces to [[Borel equivariant cohomology]] when tne action on the coefficients is trivial. See at _[[equivariant cohomology]]_ for more on this.

### Parameterized pointed objects
 {#PointedObjects}

A first step away from the Cartesian example [above](#CartesianWirthmuellerContexts) is the following.

Let $\mathbf{H}$ be a [[topos]]. For $X \in \mathbf{H}$ any [[object]], write 

$$
  \mathcal{C}_X \coloneqq \mathbf{H}_{/X}^{X/}
$$

for the [[category of pointed objects]] in the [[slice topos]] $\mathbf{H}_{/X}$. Equipped with the [[smash product]] $\wedge_X$ this is a [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}_X, \wedge_X, X \coprod X)$.

+-- {: .num_prop}
###### Proposition

For $f \colon X \longrightarrow Y$ any [[morphism]] in $\mathbf{H}$, the [[base change]] [[inverse image]] $f^\ast$ restricts to a functor $f^\ast \colon \mathcal{C}_Y \longrightarrow \mathcal{C}_X$ which is a Wirthm&#252;ller context.

=--

This appears as ([Shulman 08, examples 12.13 and 13.7](#Shulman08)) and ([Shulman 12, example 2.33](#Shulman12)).

+-- {: .proof}
###### Proof

For $f \colon X \longrightarrow Y$ any [[morphism]] in $\mathbf{H}$ then the [[base change]] [[inverse image]] $f^\ast \colon \mathbf{H}_{/Y} \longrightarrow \mathbf{H}_{/X}$ preserves pointedness, and the [[pushout]] functor $f_! \colon \mathbf{H}^{X/} \longrightarrow \mathbf{H}^{/Y}$ preserves co-pointedness. These two functors hence form an [[adjoint pair]]
$(f_1 \dashv f^\ast) \colon \mathcal{C}_X \longrightarrow \mathcal{C}_Y$.
Moreover, since [[colimits]] in the under-over category $\mathbf{H}_{/X}^{X/}$ are computed as colimits in $\mathbf{H}$ of [[diagrams]] with an [[initial object]] adjoined, and since by the [[Giraud axioms]] in the [[topos]] $\mathbf{H}$ [[pullback]] preserves these colimits, it follows that $f^\ast \colon \mathcal{C}_Y \to \mathcal{C}_X$ preserves colimits. 
Finally by the discussion at _[[category of pointed objects]]_ we have that $\mathcal{C}_X$ and $\mathcal{C}_Y$ are [[locally presentable categories]], so that by the [[adjoint functor theorem]] it follows that $f^\ast$ has also a [[right adjoint]] $f_\ast \colon \mathcal{C}_X \to \mathcal{C}_Y$.

To see that $f^\ast$ is a [[strong monoidal functor]] observe that the [[smash product]] is, by the discussion there, given by a [[pushout]] over [[coproducts]] and [[products]] in the [[slice topos]]. As above these are all preserved by [[pullback]]. Finally to see that $f^\ast$ is also a [[strong closed functor]] observe that the [[internal hom]] on [[pointed objects]] is, by the discussion there, a [[fiber product]] of cartesian internal homs. These are preserved by [the above case](#CartesianWirthmuellerContexts), and the fiber product is preserved since $f^\ast$ preserves all limits. Hence $f^\ast$ preserves also the internal homs of pointed objects.

 
=--


### Parameterized modules

+-- {: .num_prop}
###### Proposition

Let $E$ be a [[commutative ring]]. Write $E Mod$ for its [[category of modules]]. For $X\in $ [[Set]] write

$$
  E Mod(X) \coloneqq Func(X, E Mod) \simeq (E Mod)^{\times_{\vert X \vert}}
$$

for the [[functor category]] from $X$ (regarded as a [[category]]) to $E Mod$, hence for the [[bundles]] of $E$-[[modules]] over the [[discrete space]] $X$. Equipped with the [[tensor product of modules]] this is a [[symmetric monoidal category]] $E Mod^{\otimes}$. This construction yields a [[functor]]

$$
  E Mod \;\colon\; Set^{op} \longrightarrow SymMonCat
  \,.
$$

This is semantics for dependent linear type theory in the above sense.

=--


### Parametrized module spectra

+-- {: .num_prop #ParameterizedModuleSpectra}
###### Proposition

Let $E$ be an [[E-∞ ring]] spectrum and write $E Mod$ for its [[(∞,1)-category of ∞-modules]]. For $X \in $ [[∞Grpd]] write

$$
  E Mod(X) \coloneqq Func(X,E Mod)
$$

for the [[(∞,1)-category of (∞,1)-functors]] from $X$ (regarded as an [[(∞,1)-category]]) to $E Mod$, hence for the [[parameterized spectra]] over $X$ with $E$-[[∞-module]] structure. Equipped with the [[smash product of spectra]] this is a [[symmetric monoidal (∞,1)-category]] $E Mod^\otimes$ This construction yields an [[(∞,1)-functor]]

$$
  E Mod \;\colon\; \infty Grpd^{op} \longrightarrow SymMonCat_\infty
$$

This is semantics for linear homotopy type theory in the sense of def. \ref{SemanticsForLinearHomotopyTypeTheory}. It also satisfies the [[Beck-Chevalley condition]].

=--

+-- {: .num_prop #ParameterizedModuleSpectra}
###### Proposition

In the class of models of prop. \ref{ParameterizedModuleSpectra}, linear homotopy-type theory encodes the theory of [[twisted generalized cohomology]].

[[!include twisted generalized cohomology in linear homotopy type theory -- table]]

=--

## Structures in linear homtopy-type theory

We discuss here structures (constructions) that may be defined and studied within linear homotopy-type theory.


### Exponential modality and Fock spaces
 {#TheCanonicalComodality}

The original axiomatics for [[linear type theory]] in ([Girard 87](#Girard87)) contain in addition to the structures corresponding to a ([[star-autonomous category|star-autonomous]]) [[symmetric monoidal category|symmetric]] [[closed monoidal category]] a certain (co-)[[modality]] traditionally denoted "$!$", the [[!-modality]].
 
In ([Benton 95, p.9,15](#Benton95), [Bierman 95](#Bierman95))
it is noticed (reviewed in ([Barber 97, p. 21 (26)](#Barber97))) that a natural [[categorical semantics]] for this modality identifies it with the [[comonad]] that is induced from a [[strong monoidal adjunction]]

$$
  (\Sigma \dashv R)
  \;\colon\;
  \mathcal{C}
  \stackrel{\overset{\Sigma}{\leftarrow}}{\underset{R}{\longrightarrow}}
  S
$$

between the [[closed monoidal category|closed]] [[symmetric monoidal category]] $\mathcal{C}$ which interprets the given [[linear type theory]] and a [[cartesian monoidal category]] $S$.


If there is only the [[strong monoidal functor]] $\Sigma \;\colon\; S \longrightarrow \mathcal{C}$ without possibly a [[right adjoint]], then ([Barber 97, p. 21 (27)](#Barber97)) speaks of the _structural fragment_ of [[linear type theory]].


In ([Ponto-Shulman 12](#PontoShulman12)) it is observed that this in turn is canonically induced if $\mathcal{C} \simeq \mathcal{C}_\ast$ is the linear type theory over the trivial context of a dependent linear type theory/[[indexed closed monoidal category]] with category of contexts being $S$.

Namely in this case it is natural to set for $X \in S$

$$
  \Sigma(X) \coloneqq (\pi_X)_! (\pi_X)^\ast 1_{\ast}
  \,,
$$

where $\pi_X \;\colon\; X \longrightarrow \ast$ is the canonical morphism to the [[terminal object]] in $S$; and to set for $\phi \;\colon\; X \longrightarrow Y$ any [[morphism]] in $S$

$$
  \Sigma(\phi) 
    \coloneqq 
   \Sigma(X)
    =
  (\pi_X)_! (\pi_X)^\ast 1_\ast
  \stackrel{\simeq}{\to}
  (\pi_Y)_! \phi_! \phi^\ast (\pi_Y)^\ast 1_\ast
  \stackrel{(\phi_Y)_!(\epsilon_\phi)}{\longrightarrow}
  (\pi_Y)_! \phi_! (\pi_Y)^\ast 1_\ast
  =
  \Sigma(Y)
  \,.
$$

(In the typical kind of model this means to assign to a [[space]] $X$ the linear space of [[sections]] of the trivial [[line bundle]] over it.)

One checks that this indeed makes $\Sigma$ be a [[strong monoidal functor]] ([Ponto-Shulman 12, (4.3)](#PontoShulman12)).

The condition that this $\Sigma$ (and its relative/dependent versions) has a [[right adjoint]] may also be understood as saying that the dependent linear type theory satisfies the _[[axiom of comprehension]]_. See at _[comprehension -- Examples -- In dependent linear type theory](http://ncatlab.org/nlab/show/axiom+of+separation#ExamplesDependentLinearTypeTheory)_ for more.

### Dependent linear deMorgan duality

+-- {: .num_defn #LinearNegation}
###### Definition

For $\mathcal{C}^\otimes$ a [[closed monoidal category]] with [[unit object]] $1$ and [[internal hom]] $[-,-]$ write

$$
  \mathbb{D} \coloneqq [-,1] 
$$

for the [[functor]] given by internal hom into the unit object. In regarding $\mathcal{C}^\otimes$ as [[categorical semantics]] for [[linear type theory]] one may call this the _linear [[negation]]_ operation.

=--

+-- {: .num_prop }
###### Proposition

In semantics for a dependent linear type theory, def. \ref{SemanticsForDependentLinearTypeTheory}, linear negation, def. \ref{LinearNegation}, intertwines dependent sum and dependent product:

$$
  \underset{f}{\prod} \mathbb{D}
  \simeq
  \mathbb{D} \underset{f}{\sum}
$$

=--

For proof see [here](Wirthm&#252;ller%20context#ComparisonOfPushForwardsAndWirthmuelleriso) at _[[Wirthmüller context]]_.


### Primary integral transforms

+-- {: .num_defn }
###### Definition

Given semantics $Mod\colon \mathcal{C}^{op}\to SymMonCat$ for dependent linear type theory, def. \ref{SemanticsForDependentLinearTypeTheory}, and given objects $X_1, X_2$ of $\mathcal{C}$ then a **linear [[polynomial functor]]** 

$$
  P \colon Mod(X_1) \to Mod(X_2)
$$ 

is a functor of the form

$$
  P \simeq \underset{f_2}{\sum} \underset{g}{\prod} f_1^\ast
$$

for a [[diagram]]in $\mathcal{C}$ of the form

$$
  \array{
    && Y &\stackrel{g}{\longrightarrow}& Z
    \\
    & {}^{\mathllap{f_1}}\swarrow  & && & \searrow^{\mathrlap{f_2}} 
    \\
    X_1
    &&
    && 
    &&
    X_2
  }
  \,.
$$

If here $g = id$ then this diagram is a [[correspondence]]

$$
  \array{
    &&  Z
    \\
    & {}^{\mathllap{f_1}}\swarrow  & & \searrow^{\mathrlap{f_2}} 
    \\
    X_1
    &&
    &&
    X_2
  }
$$

and the resulting $P \simeq \underset{f_2}{\sum}f_1 ^\ast$ is called a **linear polynomial functor** or **primary [[integral transform]]**.

=--

+-- {: .num_prop }
###### Proposition

Given a [[correspondence]] as above, then the primary integral transform through it is equivalent to the pull-tensor-push operation through the [[product]] 

$$
  \underset{f_2}{\sum} \circ f_1^\ast
  \simeq
  \underset{p_2}{\sum}
  \circ
  \left( \left(f_1,f_2\right)_!\left(1_Z\right) \otimes \left(-\right)\right)
  \circ
  p_1^\ast
  \,.
$$

=--

+-- {: .proof}
###### Proof

By [[Frobenius reciprocity]].

=--


### Fundamental classes and measures

### Secondary integral transforms

### Dagger-structure



## Related concepts

* [[type theory]], [[homotopy type theory]]

* [[modal type theory]]

* [[stable homotopy type]]

* [[geometric homotopy type theory]]

* [[cohesive homotopy type theory]]

## References
 {#References}

Plain [[linear type theory]] originates in

*  [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))
 {#Girard87}

The [[categorical semantics|categorical interpretation]] of Girard's $!$-[[modality]] as the [[comonad]] 

is due to 

* P. N. Benton, G. M. Bierman, [[Martin Hyland]], [[Valeria de Paiva]], _Term assignment for intuitonistic linear logic_, Technial Report 262, 
Computer Laboratory, University of Cambridge, August 1992.

and that this is naturally to be thought of as arising from a [[monoidal adjunction]] between the closed [[symmetric monoidal category]] and a [[cartesian closed category]] is due to

* {#Bierman95} G. Bierman, _On Intuitionistic Linear Logic_ PhD thesis, Computing
Laboratory, University of Cambridge, 1995 ([pdf](http://research.microsoft.com/~gmb/papers/thesis.pdf))
 
* {#Benton95} N. Benton, _A mixed linear and non-linear logic; proofs, terms and
models_, In _Proceedings of Computer Science Logic_ '94, vol. 933 of
Lecture Notes in Computer Science. Verlag, June 1995.  ([[BentonLinearLogic.pdf:file]])
 
A review of all this and further discussion is in 

* {#Barber97} Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))

A [[syntax]] extending [[LF]] with linear dependent types was first published in 
 
* {#Pfenning96} Iliano Cervesato, [[Frank Pfenning]], _A Linear Logical Framework_, 1996, ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.21.1152))

Note that this framework was restricted to the _negative_ fragment of [[intuitionistic linear logic]] and [[dependent type theory]] (i.e., $\multimap$, $\&$ and $\Pi$).  The problem of extending [[LF]] to positive connectives ($\otimes,1,!,\exists$) while retaining a reasonable notion of [[canonical form]] was later addressed by

* {#WCFW03} Kevin Watkins, Iliano Cervesato, [[Frank Pfenning]], David Walker, _A concurrent logical framework I: Judgments and properties_, CMU technical report CMU-CS-02-101, revised May 2003 ([web](http://www.cs.cmu.edu/~fp/papers/CMU-CS-02-101.pdf))

A dependent linear version of [[system L]] is considered in 

* {#Spiwack14} [[Arnaud Spiwack]], section 5 of _A dissection of L_, preprint [pdf](http://assert-false.net/arnaud/papers/A%20dissection%20of%20L.pdf)

More recent work in the type-theoretic literature includes:

* [[Ugo Dal Lago]], _Linear Dependent Types in a Subrecursive Setting_, in _Bounded Linear Logic Workshop_ Fontainebleau, 2013.

* [[Ugo Dal Lago]], M. Gaboardi, _Linear Dependent Types and Relative Completeness-, in _Logical Methods in Computer Science_ Vol. 8(4:11), 2012.

* [[Ugo Dal Lago]] and B. Petit, _Linear dependent types in a call-by-value scenario_, in _Science of Computer Programming 84_, 2014.

* F.N. Forsberg, _Restricted linear dependent types for resource allocation_, in _Bounded Linear Logic Workshop_, Fontainebleau, 2013.

* M. Gaboardi et al., _Linear Dependent Types for Differential Privacy_, in POPL '13, 2013.

Discussion of what should be the [[categorical semantics]] of dependent linear type theory, namely [[indexed closed monoidal categories]], is in 

* {#Shulman08} [[Mike Shulman]], _Framed bicategories and monoidal fibrations_, in  Theory and Applications of Categories,  Vol. 20, 2008, No. 18, pp 650-738.  ([arXiv:0706.1286](http://arxiv.org/abs/0706.1286), [TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html))
 

* {#PontoShulman12} [[Kate Ponto]], [[Mike Shulman]], _Duality and traces for indexed monoidal categories_, Theory and Applications of Categories, Vol. 26, 2012, No. 23, pp 582-659 ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555))
 

* {#Shulman12} [[Mike Shulman]], _Enriched indexed categories_ ([arXiv:1212.3914](http://arxiv.org/abs/1212.3914))
 

Comments on the formalization of secondary [[integral transforms]] and [[quantization]] in dependent linear homotopy type theory are at

* {#Schreiber14} [[Urs Schreiber]] _[[schreiber:Quantization via Linear homotopy types]]_ ([arXiv:1402.7041](http://arxiv.org/abs/1402.7041))

A first published proposal for a genuine syntax of dependent linear type theory is in 

* {#Vakar14} [[Matthijs Vákár]], _Syntax and Semantics of Linear Dependent Types_ ([arXiv:1405.0033](http://arxiv.org/abs/1405.0033))


[[!redirects dependent linear type theories]]

[[!redirects linear dependent type theory]]
[[!redirects linear dependent type theories]]

[[!redirects linear dependent homotopy type theory]]
[[!redirects linear dependent homotopy type theories]]

[[!redirects dependent linear homotopy type theory]]
[[!redirects dependent linear homotopy type theories]]

[[!redirects linear homotopy type theory]]
[[!redirects linear homotopy type theories]]

[[!redirects linear homotopy-type theory]]
[[!redirects linear homotopy-type theories]]


[[!redirects dependent linear type]]
[[!redirects dependent linear types]]