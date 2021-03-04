+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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



# Indexed monoidal $(\infty,1)$-categories

* table of contents
{:toc}

## Idea

An _indexed monoidal $(\infty,1)$-category_ is the [[(∞,1)-category|(∞,1)-categorical]] version of an [[indexed monoidal category]].  That is, it consists of a "base" $(\infty,1)$-category $\mathcal{C}$ together with, for each $X\in \mathcal{C}$, a [[monoidal (∞,1)-category]] $Mod(X)$ varying functorially with $X$.  In one of the fundamental examples, $\mathcal{C}$ is the $(\infty,1)$-category of [[∞-groupoids]] ("spaces"), while $Mod(X)$ is that of [[parametrized spectra]].

Indexed monoidal $(\infty,1)$-categories are conjectured to be the [[categorical semantics]] of [[linear homotopy type theory]].

## Definition


+-- {: .num_defn #SemanticsForLinearHomotopyTypeTheory}
###### Definition

An __indexed monoidal $(\infty,1)$-category__ is

1. an [[(∞,1)-category]] $\mathcal{C}$ with [[finite (∞,1)-limits]];

1. an [[(∞,1)-functor]] $Mod \colon \mathcal{C}^{op} \to SymMonCat_\infty$ to [[symmetric monoidal (∞,1)-categories]];

such that

1. each $Mod(X)$ is [[closed monoidal (infinity,1)-category|closed]] (with [[internal hom]] to be denoted $[-,-]$);

1. for each $f \colon \Gamma_1 \to \Gamma_2$ in $Mor(\mathcal{C})$ the assigned [[(∞,1)-functor]] $f^\ast \colon Mod(\Gamma_2) \to Mod(\Gamma_1)$ has a [[left adjoint]] $f_!$ and a [[right adjoint]] $f_\ast$;

1. The adjunction $(f_! \dashv f^\ast)$ satisfies [[Frobenius reciprocity]] and the [[Beck-Chevalley condition]].

=--

In the conjectural syntax of dependent linear type theory, the objects of $\mathcal{C}$ correspond to [[contexts]], which is why we sometimes write them as $\Gamma$.  Similarly, we may sometimes write $f_!$ and $f_\ast$ as $\sum_f$ and $\prod_f$ respectively.

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

For each example we also spell out some of the abstract constructions (discussed in _[Structures](#Structures)_ below) realized in that model.  We also include some examples of [[indexed monoidal category|indexed monoidal 1-categories]] (which are a special case).

+--{: .query}
Although probably those examples should be moved to [[indexed monoidal category]].
=--


### Slices of a topos

+-- {: .num_example}
###### Example

For $\mathbf{H}$ a [[topos]], then its system $\mathbf{H}_{/(-)} \colon \mathbf{H}^{op} \to CartMonCat \to MonCat$ of [[slice toposes]] is an indexed monoidal category, hence an indexed monodial $(\infty,1)$-category.

=--

+-- {: .num_remark}
###### Remark

This example for dependent linear type theory is extremely "non-linear".  For instance, it has almost no [[dualizable objects]]; the only one is the terminal object in each slice.  Given that the formulas below for secondary integral transforms (def.\ref{SIT}) assume dualizable objects, this means that in this non-linear context there will be no nontrivial secondary integral transforms.

=--

We now pass gradually to more and more linear examples.x


### Parameterized pointed objects
 {#PointedObjects}

A first step away from the Cartesian example above towards more genuinely linear types is the following.

+-- {: .num_defn #PointedObjectsInSlice}
###### Definition

Let $\mathbf{H}$ be a [[topos]]. For $X \in \mathbf{H}$ any [[object]], write

$$
  \mathcal{C}_X \coloneqq \mathbf{H}_{/X}^{X/}
$$

for the [[category of pointed objects]] in the [[slice topos]] $\mathbf{H}_{/X}$. Equipped with the [[smash product]] $\wedge_X$ this is a [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}_X, \wedge_X, X \coprod X)$.

=--

+-- {: .num_prop}
###### Proposition

For $f \colon X \longrightarrow Y$ any [[morphism]] in $\mathbf{H}$, the [[base change]] [[inverse image]] $f^\ast$ restricts to a functor $f^\ast \colon \mathcal{C}_Y \longrightarrow \mathcal{C}_X$ and this makes

$$
  \mathbf{H}_{/(-)}^{(-)/}
  \;\colon\;
  \mathbf{H}^{op}
  \longrightarrow
  MonCat
$$

an indexed monoidal category.

=--

This appears as ([Shulman 08, examples 12.13 and 13.7](#Shulman08)) and ([Shulman 12, example 2.33](#Shulman12)).

+-- {: .proof}
###### Proof

For $f \colon X \longrightarrow Y$ any [[morphism]] in $\mathbf{H}$ then the [[base change]] [[inverse image]] $f^\ast \colon \mathbf{H}_{/Y} \longrightarrow \mathbf{H}_{/X}$ preserves pointedness, and the [[pushout]] functor $f_! \colon \mathbf{H}^{X/} \longrightarrow \mathbf{H}^{Y/}$ preserves co-pointedness. These two functors hence form an [[adjoint pair]]
$(f_! \dashv f^\ast) \colon \mathcal{C}_X \longrightarrow \mathcal{C}_Y$.
Moreover, since [[colimits]] in the under-over category $\mathbf{H}_{/X}^{X/}$ are computed as colimits in $\mathbf{H}$ of [[diagrams]] with an [[initial object]] adjoined, and since by the [[Giraud axioms]] in the [[topos]] $\mathbf{H}$ [[pullback]] preserves these colimits, it follows that $f^\ast \colon \mathcal{C}_Y \to \mathcal{C}_X$ preserves colimits.
Finally by the discussion at _[[category of pointed objects]]_ we have that $\mathcal{C}_X$ and $\mathcal{C}_Y$ are [[locally presentable categories]], so that by the [[adjoint functor theorem]] it follows that $f^\ast$ has also a [[right adjoint]] $f_\ast \colon \mathcal{C}_X \to \mathcal{C}_Y$.

To see that $f^\ast$ is a [[strong monoidal functor]] observe that the [[smash product]] is, by the discussion there, given by a [[pushout]] over [[coproducts]] and [[products]] in the [[slice topos]]. As above these are all preserved by [[pullback]]. Finally to see that $f^\ast$ is also a [[strong closed functor]] observe that the [[internal hom]] on [[pointed objects]] is, by the discussion there, a [[fiber product]] of cartesian internal homs. These are preserved by the above case, and the fiber product is preserved since $f^\ast$ preserves all limits. Hence $f^\ast$ preserves also the internal homs of pointed objects.

=--


### Parameterized modules
 {#ParameterizedModules}

The examples of genuinely linear objects in the sense of [[linear algebra]] are the following.

+-- {: .num_prop #IndexedMonoidalCategoryOfModuleBundles}
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

which is an indexed monoidal category.

=--

+-- {: .num_example #MatrixAsIntegralKernel}
###### Example

In the context of prop. \ref{IndexedMonoidalCategoryOfModuleBundles}
consider $E = k$ a [[field]]. Then $k Mod \simeq Vect_k$ is the [[category]] [[Vect]] of $k$-[[vector spaces]].

For $X \in Set$ a set, an $X$-dependent object $A \in Mod(X)\simeq Vect_k(X)$ is just a collection of ${\vert X\vert}$ vector spaces $A_x$ for $x\in X$.

For $X \in FinSet \hookrightarrow Set$ a [[finite set]], the [[dependent sum]] and [[dependent product]] operations coincide and produce the [[direct sum]] of vector spaces:

$$
  \underset{X}{\sum} A \simeq \underset{X}{\prod} A \simeq
  \underset{x\in X}{\oplus} A_x
  \in Vect_k(\ast)
  \,.
$$

Under this identification every morphism $f \in Mor(Set)$ with finite fibers carries a canonical untwisted fiberwise fundamental class, def. \ref{FiberwiseFundamentalClass}, $[f]_{canonical}$.

For

$$
  \array{
    && X_1 \times X_2
    \\
    & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
    \\
    X_1 && && X_2
  }
$$

a product corrrespondence of [[finite sets]], then an [[integral kernel]] $K$ on this, according to def. \ref{IntegralKernel}, with $A_i = 1_{X_i}$, is equivalently an ${\vert X_1\vert}\times {\vert X_2\vert}$-array of elements in $k$, hence a [[matrix]] $K_{\bullet,\bullet}$.

=--



### Parametrized module spectra
 {#ParameterizedModuleSpectra}

The example of parameterized modules [above](#ParameterizedModules) has an evident generalization from [[linear algebra]] to [[stable homotopy theory]] with [[abelian categories|abelian]] [[categories of modules]] refined to [[stable (∞,1)-categories|stable]] [[(∞,1)-categories of ∞-modules]]. Despite what this [[higher category theory]]-terminology might make the reader feel, this refinement flows naturally along the same lines as the 1-categorical situation. One may view the axiomatics of an indexed monoidal $(\infty,1)$-category as neatly characterizing precisely this intimate similarity.

| [[linear algebra]] | [[brave new algebra]] |
|--------------------|-----------------------|
| [[abelian group]]  | [[spectrum]] |
| [[commutative ring]] | [[E-∞ ring|E-∞]] [[ring spectrum]] |
| [[module]] | [[∞-module]] spectrum |
| [[abelian category|abelian]] [[category of modules]] | [[stable (∞,1)-category|stable]] [[(∞,1)-category of ∞-modules]] |

+-- {: .num_prop #ParameterizedModuleSpectraAreAnIndexedMonoidalCategory}
###### Proposition

Let $E$ be an [[E-∞ ring]] spectrum and write $E Mod$ for its [[(∞,1)-category of ∞-modules]]. For $X \in $ [[∞Grpd]] write

$$
  E Mod(X) \coloneqq Func(X,E Mod)
$$

for the [[(∞,1)-category of (∞,1)-functors]] from $X$ (regarded as an [[(∞,1)-category]]) to $E Mod$, hence for the [[parameterized spectra]] over $X$ with $E$-[[∞-module]] structure. Equipped with the [[smash product of spectra]] this is a [[symmetric monoidal (∞,1)-category]] $E Mod^\otimes$ This construction yields an [[(∞,1)-functor]]

$$
  E Mod \;\colon\; \infty Grpd^{op} \longrightarrow SymMonCat_\infty
$$

This is an indexed monoidal $(\infty,1)$-category.

=--

([Hopkins-Lurie](#HopkinsLurie), [Schreiber 14](#Schreiber14))

+-- {: .num_remark}
###### Remark

In the case that $E = \mathbb{S}$ is the [[sphere spectrum]], then $\mathbb{S}Mod \simeq Spectra$ is just the plain [[(∞,1)-category of spectra]] and then the above is the theory of plain [[parameterized spectra]].

In this case the corresponding [[(∞,1)-Grothendieck construction]] is the [[tangent (∞,1)-topos]] $T(\infty Grpd)$ of [[∞Grpd]]. This happens to be itself an [[(∞,1)-topos]], and as such is conjecturally semantics for *ordinary* [[homotopy type theory]].  If ordinary homotopy type theory is enhanced with rules and axioms motivated by such models, it also becomes able to speak about stable homotopy theory and parametrized stable objects; the relation between this theory and [[dependent linear type theory]] remains to be explored.

=--

+-- {: .num_prop}
###### Proposition

The $\Sigma$-functor, def. \ref{Sigma}, in the model of parameterized $E$-module spectra, 
prop. \ref{ParameterizedModuleSpectraAreAnIndexedMonoidalCategory}, is the [[suspension spectrum]] construction $\Sigma^\infty$ followed by [[smash product]] of spectra with $E$:

$$
  \Sigma(X) \simeq \Sigma^\infty(X)\wedge E
  \,.
$$

This is the $E$-[[generalized homology]]-spectrum of the [[∞-groupoid]] $X$.

This construction does have a [[right adjoint]] $\Omega^\infty$, where $(\Sigma^\infty \dashv \Omega^\infty)$ is the $E$-[[stabilization]]-adjunction for [[∞Grpd]]. Hence [[parameterized spectra]] have an [[exponential modality]], def. \ref{SemanticsForExponentialModality}.

=--

+-- {: .num_prop}
###### Proposition

In the class of models of prop. \ref{ParameterizedModuleSpectraAreAnIndexedMonoidalCategory}, an indexed monoidal $(\infty,1)$-category encodes the theory of [[twisted generalized cohomology]].

[[!include twisted generalized cohomology in linear homotopy type theory -- table]]

=--

### Parameterized formal moduli problems

+-- {: .num_defn #ParameterizedFormalModuliProblems}
###### Definition

For $\mathbf{H}$ a [[differential cohesive (∞,1)-topos]] with [[infinitesimal shape modality]] $\Pi_{inf}$ write for any object $X\in \mathbf{H}$

$$
  Mod(X)
  \hookrightarrow
   \mathbf{H}_{/X}^{X/}
$$

for the [[full sub-(∞,1)-category]] of that of pointed objects over $X$, def. \ref{PointedObjectsInSlice}, on those that are in the kernel of $\Pi_{inf}$.

=--


+-- {: .num_remark}
###### Remark

The construction in \ref{ParameterizedFormalModuliProblems} has the interpretation as  the category of generalized [[formal moduli problems]] parameterized over $X$. The genuine formal moduli problems satisfy one an extra exactness property of the kind discussed at _[[cohesive (∞,1)-presheaf on E-∞ rings]]_.

=--

+-- {: .num_prop}
###### Proposition

Parameterized formal moduli problems as in def. \ref{ParameterizedFormalModuliProblems} conjecturally form semantics for non-unital
linear homotopy-type theory.

=--


### Quasicoherent sheaves of modules
 {#ForQuasicoherentSheaves}

Pull-push of [[quasicoherent sheaves]] is usually discussed as a [[Grothendieck context]] of [[six operations]], but under some conditions it also becomes a [[Wirthmüller context]] and hence an indexed monoidal $(\infty,1)$-category

Using results of Lurie this follows in the full generality of [[E-∞ geometry]] ([[spectral geometry]]).

Consider quasi-compact and quasi-separated [[E-∞ scheme|E-∞ algebraic spaces]] ([[spectral geometry|spectral algebraic spaces]]). (This includes precisely those [[spectral Deligne-Mumford stacks]] which have a [[scallop decomposition]], see [here](derived+Deligne-Mumford+stack#RelationToDerivedAlgebraicSpaces).)

If $f \;\colon\; X \longrightarrow Y$ is a map between these which is

1. locally almost of finite presentation;

1. strongly proper;

1. has finite [[Tor-amplitude]]

then the left adjoint to pullback of [[quasicoherent sheaves]] exists

$$
  (f_! \dashv f^\ast)
    \;\colon\;
  QCoh(X)
    \stackrel{\overset{f_!}{\longrightarrow}}{\underset{f^\ast}{\longleftarrow}}
  QCoh(Y)
  \,.
$$

([[Proper Morphisms, Completions, and the Grothendieck Existence Theorem|LurieProper, proposition 3.3.23]])

If $f$ is

* quasi-affine

then the right adjoint exists

$$
  (f^\ast \dashv f_\ast)

    \;\colon\;
  QCoh(X)
    \stackrel{\overset{f^\ast}{\longleftarrow}}{\underset{f_\ast}{\longrightarrow}}
  QCoh(Y)
  \,.
$$

([[Quasi-Coherent Sheaves and Tannaka Duality Theorems|LurieQC, prop. 2.5.12]], [[Proper Morphisms, Completions, and the Grothendieck Existence Theorem|LurieProper, proposition 2.5.12]])

The [[projection formula]] in the dual form

$$
  f_\ast A \otimes B \longrightarrow f_\ast (A\otimes f^\ast B)
$$

for $f$ quasi-compact and quasi-separated appears as ([[Proper Morphisms, Completions, and the Grothendieck Existence Theorem|LurieProper, remark 1.3.14]]).

Now if all the conditions on $f$ hold, so that $(f_! \dashv f^\ast \dashv f_\ast) \;\colon\; QCoh(X) \longrightarrow QCoh(Y)$, then passing to opposite categories $QCoh(X)^{op} \longrightarrow QCoh(Y)^{op}$ exchanges the roles of $f_!$ and $f_\ast$, makes the projection formula be as in the above discussion and hence yields a Wirthm&#252;ller context.

The existence of [[dualizing modules]] $K$

$$
  D X = [X,K]
$$

is discussed in ([[Representability theorems|Lurie, Representability theorems, section 4.2]].)

### Stable homotopy theory of $G$-equivariant spectra

For a finite group, $G$, consider the spectral [[Mackey functors]] on the category of finite $G$-sets. These are [[G-spectrum|genuine G-spectra]] (see [equivariant stable homotopy theory](equivariant+stable+homotopy+theory#in_terms_of_mackeyfunctors)) which together constitute a $G$-equivariant $\infty$-category (or $G$-$\infty$-category, see [[Parametrized Higher Category Theory and Higher Algebra]]). This sends any orbit $G/H$, for $H$ a subgroup of $G$, to the monoidal $\infty$-category of genuine $H$-spectra. 

This forms an indexend monoidal $(\infty,1)$-category, as do other instances of $(\infty, 1)$-categories of $T$-spectra, for $T$ an [orbital](Parametrized+Higher+Category+Theory+and+Higher+Algebra#AtomicOrbital) $\infty$-category.

## Structures in an indexed monoidal $(\infty,1)$-category
 {#Structures}

We discuss here structures (constructions) that may be defined and studied within an indexed monoidal $(\infty,1)$-category.


### Exponential modality and Fock spaces
 {#TheCanonicalComodality}

The original axiomatics for [[linear type theory]] in ([Girard 87](#Girard87)) contain in addition to the structures corresponding to a ([[star-autonomous category|star-autonomous]]) [[symmetric monoidal category|symmetric]] [[closed monoidal category]] a certain (co-)[[modality]] traditionally denoted "$!$", the _[[exponential modality]]_.

In ([Benton 95, p.9,15](#Benton95), [Bierman 95](#Bierman95))
it is noticed (reviewed in ([Barber 97, p. 21 (26)](#Barber97))) that a natural [[categorical semantics]] for this modality identifies it with the [[comonad]] that is induced from a [[strong monoidal adjunction]]

$$
  (\Sigma \dashv \Omega)
  \;\colon\;
  Mod(\ast)
  \stackrel{\overset{\Sigma}{\leftarrow}}{\underset{\Omega}{\longrightarrow}}
  \mathcal{C}
$$

between the [[closed monoidal category|closed]] [[symmetric monoidal category]] $Mod(\ast)$ which interprets the given [[linear type theory]] and a [[cartesian monoidal category]] $\mathcal{C}$.

If there is only the [[strong monoidal functor]] $\Sigma \;\colon\; \mathcal{C} \longrightarrow Mod(\ast)$ without possibly a [[right adjoint]] $\Omega$, then ([Barber 97, p. 21 (27)](#Barber97)) speaks of the _structural [[fragment]]_ of [[linear type theory]].


In ([Ponto-Shulman 12](#PontoShulman12)) it is observed that this in turn is canonically induced if $Mod(\ast)$ is the [[linear type theory]] over the trivial context $\ast$ of a dependent linear type theory ([[indexed closed monoidal category]]) with category of contexts being $\mathcal{C}$:

+-- {: .num_defn #Sigma}
###### Definition

Let $Mod \colon \mathcal{C}^{op} \to MonCat$ be an indexed monoidal $(\infty,1)$-category. Then for $X \in \mathcal{C}$ an object, set


$$
  \Sigma(X) \coloneqq \underset{X}{\sum} 1_X
  \in Mod(\ast)
$$

and for $f \;\colon\; Y \longrightarrow X$ a [[morphism]] in $\mathcal{C}$ set

$$
  \Sigma(f)
    \coloneqq
   \Sigma(Y)
    =
  \underset{Y}{\sum} 1_Y
  \stackrel{\simeq}{\to}
  \underset{X}{\sum} \underset{f}{\sum} f^\ast 1_X
  \stackrel{\underset{X}{\sum}(\epsilon_f)}{\longrightarrow}
  \underset{X}{\sum} 1_X
  =
  \Sigma(X)
  \,.
$$

=--

(In the typical kind of model this means to assign to a [[space]] $X$ the linear space of [[sections]] of the trivial [[line bundle]] over it.)

+-- {: .num_prop #SigmaFunctor}
###### Proposition

The construction in def. \ref{Sigma} gives a [[strong monoidal functor]]

$$
  \Sigma
  \;\colon\;
  \mathcal{C}
  \longrightarrow
  Mod(\ast)
$$

=--

This is ([Ponto-Shulman 12, (4.3)](#PontoShulman12)).

+-- {: .num_remark }
###### Remark

Below in example \ref{SigmaFunctorAsSecondaryTransform} we see that the functor $\Sigma$ in prop. \ref{SigmaFunctor} is a special case of a general construction of secondary integral transforms in an indexed monoidal $(\infty,1)$-category.

=--


This suggests the following definition.

+-- {: .num_defn #SemanticsForExponentialModality}
###### Definition

Given an indexed monoidal $(\infty,1)$-category such that the functor $\Sigma$ from prop. \ref{SigmaFunctor} has a strong monoidal [[right adjoint]]

$$
  \Omega \colon Mod(\ast) \longrightarrow \mathcal{C}
$$

we refer to the  [[comonad]] of the $(\Sigma \dashv \Omega)$-[[adjunction]]

$$
  ! \coloneqq \Sigma \circ \Omega \colon Mod(\ast) \to Mod(\ast)
  \,.
$$

as the _[[exponential modality]]_ in the conjectural [[linear type theory]] over the point whose semantics is $Mod(\ast)$.

=--

+-- {: .num_remark}
###### Remark


The condition in def. \ref{SemanticsForExponentialModality} that $\Sigma$ (and its relative/dependent versions) has a [[right adjoint]] $\Omega$ may also be understood as saying that the dependent linear type theory satisfies the _[[axiom of comprehension]]_. See at _[comprehension -- Examples -- In dependent linear type theory](http://ncatlab.org/nlab/show/axiom+of+separation#ExamplesDependentLinearTypeTheory)_ for more.

=--

### Dependent linear deMorgan duality

+-- {: .num_defn #LinearNegation}
###### Definition

For $\mathcal{C}^\otimes$ a [[closed monoidal category]] with [[unit object]] $1$ and [[internal hom]] $[-,-]$ write

$$
  \mathbb{D} \coloneqq [-,1]
$$

for the [[functor]] given by internal hom into the unit object.  Syntactically this corresponds to the _linear [[negation]]_ operation.

=--

+-- {: .num_prop #DependentLinearDeMorganDuality}
###### Proposition
**(dependent linear de Morgan duality)**

In an indexed monoidal $(\infty,1)$-category, linear negation, def. \ref{LinearNegation}, intertwines dependent sum and dependent product:

$$
  \underset{f}{\prod} \mathbb{D}
  \simeq
  \mathbb{D} \underset{f}{\sum}
$$

=--

For proof see [here](Wirthm&#252;ller%20context#ComparisonOfPushForwardsAndWirthmuelleriso) at _[[Wirthmüller context]]_.


### Primary integral transforms
 {#PrimaryIntegralTransform}

+-- {: .num_defn #PolynomialFunctorsAndCorrespondences}
###### Definition

Given an indexed monoidal $(\infty,1)$-category $Mod\colon \mathcal{C}^{op}\to SymMonCat$, and given objects $X_1, X_2$ of $\mathcal{C}$ then a **linear [[polynomial functor]]**

$$
  P \colon Mod(X_1) \to Mod(X_2)
$$

is a functor of the form

$$
  P \simeq \underset{f_2}{\sum} \underset{g}{\prod} f_1^\ast
$$

for a [[diagram]] in $\mathcal{C}$ of the form

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


### Fundamental classes
 {#FundamentalClasses}

+-- {: .num_defn #FiberwiseFundamentalClass}
###### Definition

A _fiberwise twisted fundamental class_ $[f]$ on a morphism $f \colon X\to Y$ in $\mathcal{C}$ is

1. a choice of dualizable object $\tau \in Mod(Y)$ (the _twist_);

1. a choice of equivalence

   $$
     \underset{f}{\sum} f^\ast 1_X
     \stackrel{\simeq}{\longrightarrow}
     \underset{f}{\prod} f^\ast \tau
     \,.
   $$

=--

In this form this is stated in ([Schreiber 14](#Schreiber14)).

+-- {: .num_remark #FundamentalClassFromAmbidexterity}
###### Remark

A special case of def. \ref{FiberwiseFundamentalClass} is obtained when the twist vanishes, $\tau = 1$, and when dependent sum and dependent product are naturally equivalent for all objects, $\sum_f \simeq \prod_f$. In this case the two adjoints to $f^\ast$ coincide to form an [[ambidextrous adjunction]]. This case is considered in ([Hopkins-Lurie](#HopkinsLurie)).

=--

+-- {: .num_remark }
###### Remark

In view of dependent linear de Morgan duality, prop. \ref{DependentLinearDeMorganDuality}, a fiberwise twisted fundamental class in def. \ref{FiberwiseFundamentalClass} is equivalently a choice of equivalence


$$
  \underset{f}{\sum} f^\ast 1_X
  \stackrel{\simeq}{\longrightarrow}
  \mathbb{D}\underset{f}{\sum} f^\ast \mathbb{D}\tau
  \,,
$$

hence an identification of the dependent sum of the unit with the dual of the dependent sum of the twist.

=--

+-- {: .num_prop #WirthmullerIsomorphism}
###### Proposition

A twisted fiberwise fundamental class $[f]$, def. \ref{FiberwiseFundamentalClass}, induces for all dualizable $A\in Mod(X)$ a [[natural equivalence]]

$$
  \mathbb{D} \underset{f}{\sum} f^\ast \mathbb{D}(A\otimes \tau)
  \simeq
  \underset{f}{\sum}f^\ast A
  \,.
$$

=--

This is the "[Wirthm&#252;ller isomorphism](Wirthm&#252;ller%20context#ComparisonOfPushForwardsAndWirthmuelleriso)".

+-- {: .num_defn #ComponentOfFiberwiseClass}
###### Definition

For $[f]$ a twisted fiberwise fundamental class and for $A$ dualizable, write

$$
  [f]_A
  \;\colon\;
  A \otimes \tau
  \stackrel{\mathbb{D}_{\epsilon_{\mathbb{D}(A \otimes \tau)}}}{\longrightarrow}
  \mathbb{D} \underset{f}{\sum} f^\ast (\mathbb{D}(A\otimes \tau))
  \stackrel{\simeq}{\longrightarrow}
  \underset{f}{\sum}f^\ast A
$$

for the composite of the linear dual of the $(\sum_f \dashv f^\ast)$-[[counit of an adjunction|adjunction counit]] and the Wirthm&#252;ller isomorphism, prop. \ref{WirthmullerIsomorphism}.

=--

+-- {: .num_remark }
###### Remark

The key point is that the morphism in def. \ref{ComponentOfFiberwiseClass} goes in the reverse direction of the [[counit of an adjunction|adjunction counit]]. In this way it plays a role in the construction of secondary integral transforms [below](#SecondaryIntegralTransforms).

=--


### Secondary integral transforms
 {#SecondaryIntegralTransforms}

+-- {: .num_defn #IntegralKernel}
###### Definition

For

$$
  \array{
    && Z
    \\
    & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
    \\
    X_1
    && &&
    X_2
  }
$$

a [[correspondence]] as in def. \ref{PolynomialFunctorsAndCorrespondences}, then an _[[integral kernel]]_ for it is the choice of

1. two dualizable objects $A_i \in Mod(X_i)$;

1. a morphism between their pullbacks to the correspondence space:

   $$
     f_1^\ast A_1 \stackrel{K}{\longleftarrow} f_2^\ast A_2
     \,.
   $$

=--

+-- {: .num_defn #SIT}
###### Definition

Given

1. a [[correspondence]] $X_1 \stackrel{f_1}{\longleftarrow} Z \stackrel{f_2}{\longrightarrow} X_2$ as in def. \ref{PolynomialFunctorsAndCorrespondences};

1. an [[integral kernel]] $K$ as in def. \ref{IntegralKernel};

1. a $\tau$-twisted fundamental class $[f_2]$ as in def. \ref{FiberwiseFundamentalClass}

we say that the induced _secondary integral transform_ is the morphism

$$
  \int_Z \Xi d \mu_f
  \;\colon\;
  \mathbb{D} \underset{X_1}{\sum} A_1
  \longrightarrow
  \mathbb{D}\underset{X_2}{\sum} (A_2\otimes \tau)
$$

which is the dual (the image under $\mathbb{D}(-)$) of the following composite:

$$
  \underset{X_1}{\sum} A_1
  \stackrel{\underset{X_1}{\sum}\epsilon_{A_1}}{\longleftarrow}
  \underset{X_1}{\sum}
  \underset{f_1}{\sum}
  f_1^\ast A_1
  \stackrel{\simeq}{\leftarrow}
  \underset{Z}{\sum}f_1^\ast A_1
  \stackrel{\underset{Z}{\sum} K}{\longleftarrow}
  \underset{Z}{\sum}f_2^\ast A_2
  \stackrel{\simeq}{\leftarrow}
  \underset{X_2}{\sum}\underset{f_2}{\sum} f_2^\ast A_2
  \stackrel{\underset{X_2}{\sum}[f_2]_{A_2}}{\longleftarrow}
  \underset{X_2}{\sum} (A_2\otimes \tau)
  \,,
$$

where the morphism on the left is the [[counit of an adjunction|adjunction counit]], the morphism in the middle is the given [[integral kernel]], and the morphism on the right is the given fundamental class.

=--

In this form this appears in ([Schreiber 14](#Schreiber14)). Specialized to the ambidextrous case of remark \ref{FundamentalClassFromAmbidexterity}, this is equivalent to the construction in ([Hopkins-Lurie](#HopkinsLurie)).

+-- {: .num_remark}
###### Remark

A [[correspondence]] $X_1 \stackrel{f_1}{\longleftarrow} Z \stackrel{f_2}{\longrightarrow} X_2$ may be thought of as a space $Z$ of "paths" or "trajectories" that connect points in $X_2$ to points in $X_1$. From this point of view definition \ref{SIT} is a linear map that takes functions on $X_2$ to functions on $X_1$ by pointwise forming a sum over paths connecting these points and adding all the contributions of the given [[integral kernel]] along these paths.

This is conceptually just how the [[path integral]] in [[physics]] is supposed to work, only that mostly it doesn't, due to lack of a proper definition. However, at least some path integrals for [[topological field theories]] may be realized as secondary integral transforms of the above kind.

Notice that while in [[modal type theory]] the ([[comonad|co-]])[[monads]] $(f^\ast \sum_f \dashv f^\ast \prod_f)$ are pronounced as _[[possibility]]_ and _[[necessity]]_, the monad $\prod_f f^\ast$ appearing above, via def. \ref{FiberwiseFundamentalClass}, may be pronounced _randomness_, see at _[[function monad]]_ for more.

=--

+-- {: .num_example #SigmaFunctorAsSecondaryTransform}
###### Example

Consider the special case def. \ref{SIT} where the right leg of the correspondence is the identity

$$
  \array{
    && Z
    \\
    & {}^{\mathllap{f}}\swarrow && \searrow^{\mathrlap{=}}
    \\
    X && && Z
  }
$$

and where the integral kernel is the identity

$$
  K = id_{1_Z} \colon id_Z^\ast 1_Z = 1_Z \to 1_Z = f^\ast 1_X
  \,.
$$

Then the associated secondary integral transform, def. \ref{SIT}, is the morphism

$$
  \underset{X}{\sum} 1_X
  \stackrel{\underset{\epsilon_f}{\sum}}{\longleftarrow}
  \underset{X}{\sum} \underset{f}{\sum} f^\ast 1_X
  \stackrel{\simeq}{\longleftarrow}
  \underset{Z}{\sum} 1_Z
  \,.
$$

This is just the $\Sigma$-functor of def. \ref{Sigma}:


$$
  \mathbb{D}\int_Z id \, d\mu_f
  =
  \Sigma(f)
  \;
  \colon
  \;
  \Sigma(Z)
  \stackrel{\Sigma(f)}{\longleftarrow}
  \Sigma(X)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

Given a correspondence with integral kernel as in example \ref{MatrixAsIntegralKernel}, then the induced secondary integral transform according to def. \ref{SIT} is the [[linear function]]

$$
  k^{\vert X_1\vert}
  \longleftarrow
  k^{\vert X_2\vert}
$$

represented by that matrix.

=--





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

The [[categorical semantics|categorical interpretation]] of Girard's $!$-[[modality]] as a [[comonad]] is due to

* P. N. Benton, G. M. Bierman, [[Martin Hyland]], [[Valeria de Paiva]], _Term assignment for intuitionistic linear logic_, Technical Report 262,
Computer Laboratory, University of Cambridge, August 1992.

and that this is naturally to be thought of as arising from a [[monoidal adjunction]] between the closed [[symmetric monoidal category]] and a [[cartesian closed category]] is due to

* {#Bierman95} G. Bierman, _On Intuitionistic Linear Logic_ PhD thesis, Computing
Laboratory, University of Cambridge, 1995 ([pdf](http://research.microsoft.com/~gmb/papers/thesis.pdf))

* {#Benton95} N. Benton, _A mixed linear and non-linear logic; proofs, terms and
models_, In _Proceedings of Computer Science Logic_ '94, vol. 933 of
Lecture Notes in Computer Science. Verlag, June 1995.  ([[BentonLinearLogic.pdf:file]])

A review of all this and further discussion is in

* {#Barber97} Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))

The 1-categorical version of [[indexed closed monoidal categories]] is discussed in

* {#Shulman08} [[Mike Shulman]], _Framed bicategories and monoidal fibrations_, in  Theory and Applications of Categories,  Vol. 20, 2008, No. 18, pp 650-738.  ([arXiv:0706.1286](http://arxiv.org/abs/0706.1286), [TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html))

* {#PontoShulman12} [[Kate Ponto]], [[Mike Shulman]], _Duality and traces for indexed monoidal categories_, Theory and Applications of Categories, Vol. 26, 2012, No. 23, pp 582-659 ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555))

* {#Shulman12} [[Mike Shulman]], _Enriched indexed categories_ ([arXiv:1212.3914](http://arxiv.org/abs/1212.3914))

Comments on the formalization of secondary [[integral transforms]] and [[path integral]] [[quantization]] in an indexed monoidal $(\infty,1)$-category are in

* {#Schreiber14} [[Urs Schreiber]], _[[schreiber:Quantization via Linear homotopy types]]_ ([arXiv:1402.7041](http://arxiv.org/abs/1402.7041))

* {#HopkinsLurie} [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_

[[!redirects indexed monoidal (infinity,1)-categories]]
[[!redirects indexed monoidal (∞,1)-category]]
[[!redirects indexed monoidal (∞,1)-categories]]
[[!redirects indexed monoidal infinity-category]]
