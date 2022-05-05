
## Basic notions of Categorical algebra

We have seen that the existence of [[Cartesian products]] in a [[category]] $\mathcal{C}$ equips is with a [[functor]] of the form

$$
  \mathcal{C} \times \mathcal{C}
    \overset{ (-) \times (-) }{\longrightarrow}
  \mathcal{C}
$$

which is directly analogous to the operation of [[multiplication]] in an [[associative algebra]] or even just in a [[semigroup]] (or [[monoid]]), just "[[categorification|categorified]]" (Example \ref{CartesianMonoidalCategory} below). This is made precise by the concept of a _[[monoidal category]]_ (Def. \ref{MonoidalCategory} below).

This relation between [[category theory]] and [[algebra]] leads to the fields of _[[categorical algebra]]_ and of _[[universal algebra]]_.

Here we are mainly interested in [[monoidal categories]] as a foundations for [[enriched category theory]], to which we turn [below](#EnrichedCategories).

$\,$

### Monoidal categories

+-- {: .num_defn #MonoidalCategory}
###### Definition
**([[monoidal category]])**

An_[[monoidal category]]_ is a [[category]] $\mathcal{C}$ (Def. \ref{Categories}) equipped with

1. a [[functor]] (Def. \ref{Functors})

   $$
      \otimes
        \;\colon\;
      \mathcal{C} \times \mathcal{C}
       \longrightarrow
      \mathcal{C}
   $$

   out of the [[product category]] of $\mathcal{C}$ with itself (Example \ref{ProductCategory}), called the **[[tensor product]]**,

1. an [[object]]

   $$
     1 \in Obj_{\mathcal{C}}
   $$

   called the **[[unit object]]** or **[[tensor unit]]**,

1. a [[natural isomorphism]] (Def. \ref{NaturalTransformations})

   $$
     a
       \;\colon\;
     ((-)\otimes (-)) \otimes (-)
       \overset{\simeq}{\longrightarrow}
     (-) \otimes ((-)\otimes(-))
   $$

   called the **[[associator]]**,

1. {#MonoidalCategoryUnitors} a [[natural isomorphism]]

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

   $$
     \array{
       && (w \otimes x) \otimes (y \otimes z)
       \\
       & {}^{\mathllap{\alpha_{w \otimes x, y, z}}}\nearrow
        &&
       \searrow^{\mathrlap{\alpha_{w,x,y \otimes z}}}
       \\
       ((w \otimes x ) \otimes y) \otimes z
        && &&
       (w \otimes (x \otimes (y \otimes z)))
       \\
       {}^{\mathllap{\alpha_{w,x,y}} \otimes id_z }\downarrow
        && &&
       \uparrow^{\mathrlap{ id_w \otimes \alpha_{x,y,z} }}
       \\
       (w \otimes (x \otimes y)) \otimes z
         && \underset{\alpha_{w,x \otimes y, z}}{\longrightarrow} &&
       w \otimes ( (x \otimes y) \otimes z )
     }
   $$


=--


+-- {: .num_example #CartesianMonoidalCategory}
###### Example
**([[cartesian monoidal category]])**

Let $\mathcal{C}$ be a [[category]] in which all [[finite products]] exist.
Then $\mathcal{C}$ becomes a [[monoidal category]] (Def. \ref{MonoidalCategory}) by

1. taking the [[tensor product]] to be the [[Cartesian product]]

   $$
     X \otimes Y \;\coloneqq\; X \times Y
   $$

1. taking the [[unit object]] to be the [[terminal object]] (Def. \ref{InitialObject})

   $$
     I \;\coloneqq\; \ast
   $$

Monoidal categories of this form are called _[[cartesian monoidal categories]]_.

=--


+-- {: .num_lemma #kel1}
###### Lemma
**([Kelly 64](monoidal+category#Kelly))**

Let $(\mathcal{C}, \otimes, 1)$ be a [[monoidal category]], def. \ref{MonoidalCategory}. Then the left and right [[unitors]] $\ell$ and $r$ satisfy the following conditions:

1. $\ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1$;

1. for all objects $x,y \in \mathcal{C}$ the following [[commuting diagram|diagrams commutes]]:

   $$
     \array{
       (1 \otimes x) \otimes y  & &
       \\
       {}^\mathllap{\alpha_{1, x, y}} \downarrow
       & \searrow^\mathrlap{\ell_x \otimes id_y} &
       \\
       1 \otimes (x \otimes y)
       & \underset{\ell_{x \otimes y}}{\longrightarrow} & x \otimes y
     }
     \,;
   $$

   and

   $$
     \array{
       x \otimes (y \otimes 1) & &
       \\
       {}^\mathllap{\alpha^{-1}_{1, x, y}} \downarrow
       & \searrow^\mathrlap{id_x \otimes r_y} &
       \\
       (x \otimes y) \otimes 1
         &
           \underset{r_{x \otimes y}}{\longrightarrow}
         &
       x \otimes y
     }
     \,;
   $$

=--

For **proof** see at _[[monoidal category]]_ [this lemma](monoidal+category#kel1) and [this lemma](monoidal+category#kel2).

+-- {: .num_remark #CoherenceForMonoidalCategories}
###### Remark

Just as for an [[associative algebra]] it is sufficient to demand $1 a = a$ and $a 1 = a$ and $(a b) c = a (b c)$ in order to have that expressions of arbitrary length may be re-bracketed at will, so there is a _[[coherence theorem for monoidal categories]]_ which states that all ways of freely composing the [[unitors]] and [[associators]] in a [[monoidal category]] (def. \ref{MonoidalCategory}) to go from one expression to another will coincide. Accordingly, much as one may drop the notation for the bracketing in an [[associative algebra]] altogether, so one may, with due care, reason about monoidal categories without always making all unitors and associators explicit.

(Here the qualifier "freely" means informally that we must not use any non-formal identification between objects, and formally it means that the diagram in question must be in the image of a [[strong monoidal functor]] from a _free_ monoidal category. For example if in a particular monoidal category it so happens that the object $X \otimes (Y \otimes Z)$ is actually _equal_ to $(X \otimes Y)\otimes Z$, then the various ways of going from one expression to another using only associators _and_ this equality no longer need to coincide.)

=--

+-- {: .num_defn #BraidedMonoidalCategory}
###### Definition
**([[braided monoidal category]])**

A **[[braided monoidal category]]**, is a [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]] (Def. \ref{NaturalTransformations})

\[
  \label{BraidingIsomorphism}
  \tau_{x,y} \colon x \otimes y \to y \otimes x
\]

called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved ("hexagon identities"):

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

A **[[symmetric monoidal category]]** is a [[braided monoidal category]] (def. \ref{BraidedMonoidalCategory}) for which the [[braiding]]

$$
   \tau_{x,y} \colon x \otimes y \to y \otimes x
$$

satisfies the condition:

$$
  \tau_{y,x} \circ \tau_{x,y} = 1_{x \otimes y}
$$

for all objects $x, y$

=--

+-- {: .num_remark #SymmetricMonoidalCategoriesCoherenceTheorem}
###### Remark

In analogy to the [[coherence theorem for monoidal categories]] (remark \ref{CoherenceForMonoidalCategories}) there is a [[coherence theorem for symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}), saying that every diagram built freely (see remark \ref{SymmetricMonoidalCategoriesCoherenceTheorem}) from [[associators]], [[unitors]] and [[braidings]] such that both sides of the diagram correspond to the same [[permutation]] of objects, coincide.

=--



+-- {: .num_defn #ClosedMonoidalCategory}
###### Definition
**([[symmetric monoidal category|symmetric]] [[closed monoidal category]])**

Given a [[symmetric monoidal category]] $\mathcal{C}$ with [[tensor product]] $\otimes$ (def. \ref{SymmetricMonoidalCategory}) it is called a _[[closed monoidal category]]_ if for each $Y \in \mathcal{C}$ the [[functor]] $Y \otimes(-)\simeq (-)\otimes Y$ has a [[right adjoint]], denoted $hom(Y,-)$

\[
  \label{InternalHomAdjunction}
  \mathcal{C}
    \underoverset
      {\underset{ [Y,-]}{\longrightarrow}}
      {\overset{(-) \otimes Y}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,,
\]

hence if there are [[natural bijections]]

$$
  Hom_{\mathcal{C}}(X \otimes Y, Z)
   \;\simeq\;
  Hom_{\mathcal{C}}{C}(X, [Y,Z])
$$

for all objects $X,Z \in \mathcal{C}$.

Since for the case that $X = 1$ is the [[tensor unit]] of $\mathcal{C}$ this means that

$$
  Hom_{\mathcal{C}}(1, [Y,Z]) \simeq Hom_{\mathcal{C}}(Y,Z)
  \,,
$$

the object $[Y,Z] \in \mathcal{C}$ is an enhancement of the ordinary [[hom-set]] $Hom_{\mathcal{C}}(Y,Z)$ to an object in $\mathcal{C}$.
Accordingly, it is also called the **[[internal hom]]** between $Y$ and $Z$.

The [[adjunction counit]] (Def. \ref{AdjunctionUnitFromHomIsomorphism}) in this case is called the _[[evaluation]] morphism_

\[
  \label{EvaluationMorphism}
  X \otimes [X,Y] \overset{ev}{\longrightarrow} Y
\]

=--


+-- {: .num_example #SetIsCartesianClosed}
###### Example
**([[Set]] is a [[cartesian closed category]])**

The [[category]] [[Set]] of all [[sets]] (Example \ref{CategoryOfSets}) equipped with its [[cartesian monoidal category]]-structure (Example \ref{CartesianMonoidalCategory}) is a [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}), hence a _[[cartesian closed category]]_. The [[Cartesian product]] is the original [[Cartesian product]] of sets, and the [[internal hom]] is the [[function set]] $[X,Y]$ of functions from $X$ to $Y$

=--

+-- {: .num_example #ExampleAbelianGroupsOfMonoidalCategory}
###### Example
**([[tensor product]] of [[abelian groups]] is [[closed monoidal category]] [[symmetric monoidal category|symmetric]] [[monoidal category]]-[[structure]])**

The category [[Ab]] of [[abelian groups]] (as in Example \ref{ExamplesOfConcreteCategories}) becomes a [[symmetric monoidal category]] (Def. \ref{SymmetricMonoidalCategory}) with [[tensor product]] the actual [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ and with [[tensor unit]] the additive group $\mathbb{Z}$ of [[integers]]. Again the [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident ones coming from the underlying sets.

This is a [[closed monoidal category]] with [[internal hom]] $hom(A,B)$ being the set of [[homomorphisms]] $Hom_{Ab}(A,B)$ equipped with the pointwise group structure for $\phi_1, \phi_2 \in Hom_{Ab}(A,B)$ then $(\phi_1 + \phi_2)(a) \coloneqq \phi_1(a) + \phi_2(b) \; \in B$.

This is the archetypical case that motivates the notation "$\otimes$" for the pairing operation in a [[monoidal category]].

=--


+-- {: .num_example #GrpdIsACartesianClosedCategory}
###### Example
**([[Cat]] and [[Grpd]] are [[cartesian closed categories]])**

The [[category]] [[Cat]] (Example \ref{CategoriesOfSmallCategories}) of all [[small categories]] (Example \ref{SmallCategory}) is a
[[cartesian monoidal category]]-structure (Example \ref{CartesianMonoidalCategory}) with [[Cartesian product]] given by forming [[product categories]] (Example \ref{ProductCategory}).


Inside this, the [[full subcategory]] (Example \ref{FullSubcategoryOnClassOfObjects}) [[Grpd]] (Example \ref{CategoriesOfSmallCategories}) of all [[small groupoid|small]] [[groupoids]] (Example \ref{Groupoid}) is itself a
[[cartesian monoidal category]]-structure (Example \ref{CartesianMonoidalCategory}) with [[Cartesian product]] given by forming [[product categories]] (Example \ref{ProductCategory}).

In both cases this yields a [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}), hence a [[cartesian closed category]]: the [[internal hom]] is given by the [[functor category]] construction (Example \ref{FunctorCategory}).


=--

+-- {: .num_example #CartesianClosedMonoidalnessOfCategoriesOfPresheaves}
###### Example
**([[categories of presheaves are cartesian closed]])**

Let $\mathcal{C}$ be a [[category]] and write $[\mathcal{C}^{op}, Set]$ for its [[category of presheaves]] (Example \ref{CategoryOfPresheaves}).

This is

1. a [[cartesian monoidal category]] (Example \ref{CartesianMonoidalCategory}), whose [[Cartesian product]] is given objectwise in $\mathcal{C}$ by the [[Cartesian product]] in [[Set]]:

   for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$, their [[Cartesian product]] $\mathbf{X} \times \mathbf{Y}$ exists and is given by

   $$
     \mathbf{X} \times \mathbf{Y}
     \;\;\colon\;\;\phantom{A}
     \array{
       c_1 &\mapsto& \mathbf{X}(c_1) \times \mathbf{Y}(c_1)
       \\
       {}^{\mathllap{f}}\big\downarrow
         &&
       \big\uparrow^{ \mathrlap{ \mathbf{X}(f) \times \mathbf{Y}(f) } }
       \\
       c_2 &\mapsto& \mathbf{X}(c_2) \times \mathbf{Y}(c_2)
     }
   $$

1. a [[cartesian closed category]] (Def. \ref{ClosedMonoidalCategory}), whose [[internal hom]] is given for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ by

   $$
     [\mathbf{X}, \mathbf{Y}]
     \;\;\colon\;\;\phantom{A}
     \array{
       c_1 &\mapsto& Hom_{[\mathcal{C}^{op}, Set]}( y(c_1) \times \mathbf{X}, \mathbf{y} )
       \\
       {}^{ \mathllap{ f } }\big\downarrow
         &&
       \big\uparrow^{ \mathrlap{ Hom_{[\mathcal{C}^{op}, Set]}( y(f) \times \mathbf{X}, \mathbf{y} ) } }
       \\
       c_2 &\mapsto& Hom_{[\mathcal{C}^{op}, Set]}( y(c_2) \times \mathbf{X}, \mathbf{y} )
     }
   $$

   Here $y \;\colon\; \mathcal{C} \to [\mathcal{C}^{op}, Set]$ denotes the [[Yoneda embedding]] and $Hom_{[\mathcal{C}^{op}, Set]}(-,-)$ is the [[hom-functor]] on the [[category of presheaves]].

=--

+-- {: .proof}
###### Proof

The first statement is a special case of the general fact that [[limits of presheaves are computed objectwise]] (Example \ref{LimitsOfPresheavesAreComputedObjectwise}).

For the second statement, first assume that $[\mathbf{X}, \mathbf{Y}]$ does exist. Then by the adjunction hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) we have for any other presheaf $\mathbf{Z}$ a [[natural isomorphism]] of the form

\[
  \label{InternalHomIsoInPresheaves}
  Hom_{[\mathcal{C}^{op}, Set]}(\mathbf{Z}, [\mathbf{X},\mathbf{Y}])
    \;\simeq\;
  Hom_{[\mathcal{C}^{op}, Set]}(\mathbf{Z} \times \mathbf{X}, \mathbf{Y})
  \,.
\]

This holds in particular for $\mathbf{Z} = y(c)$ a [[representable presheaf]] (Example \ref{RepresentablePresheaves}) and so the [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) implies that if it exists, then $[\mathbf{X}, \mathbf{Y}]$ must have the claimed form:

$$
  \begin{aligned}
    [\mathbf{X}, \mathbf{Y}](c)
    & \simeq
    Hom_{[\mathcal{C}^{op}, Set]}( y(c), [\mathbf{X}, \mathbf{Y}] )
    \\
    & \simeq Hom_{ [\mathcal{C}^{op}, Set] }( y(c) \times \mathbf{X}, \mathbf{Y} )
    \,.
  \end{aligned}
$$

Hence it remains to show that this formula does make (eq:InternalHomIsoInPresheaves) hold generally.

For this we use the equivalent characterization of [[adjoint functors]] from Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor}, in terms of the [[adjunction counit]] providing a system of [[universal arrows]] (Def. \ref{UniversalArrow}).

Define a would-be [[adjunction counit]], hence a would-be _[[evaluation]]_ morphism (eq:EvaluationMorphism), by

$$
  \array{
    \mathbf{X} \times [\mathbf{X} , \mathbf{Y}]
    &\overset{ev}{\longrightarrow}&
    \mathbf{Y}
    \\
    \mathbf{X}(c) \times Hom_{[\mathcal{C}^{op}, Set]}(y(c) \times \mathbf{X}, \mathbf{Y})
    &\overset{ev_c}{\longrightarrow}&
    \mathbf{Y}(c)
    \\
    (x, \phi) &\mapsto& \phi_c( id_c, x )
  }
$$

Then it remains to show that for every morphism of presheaves of the form
$ \mathbf{X} \times \mathbf{A} \overset{\phantom{A}f\phantom{A}}{\longrightarrow} \mathbf{Y} $ there is a _unique_  morphism
$\widetilde f \;\colon\; \mathbf{A} \longrightarrow [\mathbf{X}, \mathbf{Y}]$ such that

\[
  \label{UniversalArrowConditionForEvaluationMapInPresheaves}
  \array{
    \mathbf{X} \times \mathbf{A}
    && \overset{ \mathbf{X} \times \widetilde f  }{\longrightarrow} &&
    \mathbf{X} \times [\mathbf{X}, \mathbf{Y}]
    \\
    & {}_{\mathllap{ \mathrlap{f} }}\searrow
      &&
    \swarrow_{ \mathrlap{  ev } }
    \\
    && \mathbf{Y}
  }
\]

The [[commuting diagram|commutativity]] of this diagram means in components at $c \in \mathcal{C}$ that, that for all $x \in \mathbf{X}(c)$ and $a \in \mathbf{A}(c)$ we have

$$
  \begin{aligned}
    ev_c( x, \widetilde f_c(a) )
    & \coloneqq
    (\widetilde f_c(a))_c( id_c, x )
    \\
    & = f_c( x, a )
  \end{aligned}
$$

Hence this fixes the component $\widetilde f_c(a)_c$ when its first argument is the [[identity morphism]] $id_c$. But let $g \;\colon\; d \to c$ be any morphism and chase $(id_c, x )$ through the naturality diagram for $\widetilde f_c(a)$:

$$
  \array{
    Hom_{\mathcal{C}}(c,c) \times \mathbf{X}(c)
    &\overset{ (\widetilde f_c(a))_c }{\longrightarrow}&
    \mathbf{Y}(c)
    \\
    {}^{\mathllap{ g^\ast }}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{ g^\ast }}
    \\
    Hom_{\mathcal{C}}(d,c) \times \mathbf{X}(d)
    &\overset{ (\widetilde f_c(a))_d }{\longrightarrow}&
    \mathbf{Y}(d)
  }
  \phantom{AAAA}
  \array{
    \{ (id_c, x ) \} &\longrightarrow& \{ f_c( x, a ) \}
    \\
    \big\downarrow && \big\downarrow
    \\
    \{ (g, g^\ast(x)) \}  &\longrightarrow& \{ f_d( g^\ast(x), g^\ast(a) ) \}
  }
$$

This shows that $(\widetilde f_c(a))_d$ is fixed to be given by

\[
  \label{ComponentFormulaForEvaluationMapInPresheaves}
  (\widetilde f_c(a))_d( g, x' )
  \;=\;
  f_d( x', g^\ast(a) )
\]

at least on those pairs $(g,x')$ such that $x'$ is in the image of $g^\ast$.

But, finally, $(\widetilde f_c(a))_d$ is also natural in $c$

$$
  \array{
    \mathbf{A}(c)
    &\overset{ \widetilde f_c }{\longrightarrow}& [\mathbf{X},\mathbf{Y}](c)
    \\
    {}^{\mathllap{g^\ast}}\big\downarrow && \big\downarrow^{\mathrlap{g^\ast}}
    \\
    \mathbf{A}(d)
    &\overset{ \widetilde f_d }{\longrightarrow}& [\mathbf{X},\mathbf{Y}](d)
  }
$$

which implies that (eq:ComponentFormulaForEvaluationMapInPresheaves) must hold generally. Hence naturality implies that (eq:UniversalArrowConditionForEvaluationMapInPresheaves) indeed has a unique solution.

=--



$\,$

The [[internal hom]] (Def. \ref{ClosedMonoidalCategory}) turns out to share all the abstract properties of the ordinary (external) [[hom-functor]] (Def. \ref{HomFunctor}), even though this is not completely manifest from its definition. We make this explicit by the following three propositions.

+-- {: .num_prop #InternalHomBifunctor}
###### Proposition
**([[internal hom]] [[bifunctor]])**

For $\mathcal{C}$ a [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}), there is a unique [[functor]] (Def. \ref{Functors}) out of the [[product category]] (Def. \ref{ProductCategory}) of $\mathcal{C}$ with its [[opposite category]] (Def. \ref{OppositeCategory})

$$
  [-,-]
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{C}
$$

such that for each $X \in \mathcal{C}$ it coincides with the [[internal hom]] $[X,-]$ (eq:InternalHomAdjunction) as a functor in the second variable, and such that there is a [[natural isomorphism]]

$$
  Hom(X, [Y,Z])
  \;\simeq\;
  Hom(X \otimes Y, Z)
$$

which is natural not only in $X$ and $Z$, but also in $Y$.

=--

+-- {: .proof}
###### Proof

We have a natural isomorphism for each fixed $Y$, and hence in particular for fixed $Y$ and fixed $Z$ by (eq:InternalHomAdjunction). With this the statement follows by Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject}.

=--


In fact the 3-variable adjunction from Prop. \ref{InternalHomBifunctor} even holds internally:


+-- {: .num_prop #TensorHomAdjunctionIsoInternally}
###### Proposition
**(internal tensor/hom-adjunction)**

In a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) there are [[natural isomorphisms]]

$$
  [X \otimes Y, Z]
   \;\simeq\;
  [X, [Y,Z]]
$$

whose image under $Hom_{\mathcal{C}}(1,-)$ (see also Example \ref{ChangeOfCosmosFromVToSet} below) are the defining [[natural bijections]] of Prop. \ref{InternalHomBifunctor}.

=--

+-- {: .proof}
###### Proof

Let $A \in \mathcal{C}$ be any object. By applying the natural bijections from Prop. \ref{InternalHomBifunctor}, there are composite [[natural bijections]]

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(A , [X \otimes Y, Z])
    & \simeq
    Hom_{\mathcal{C}}(A \otimes (X \otimes Y), Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}((A \otimes X)\otimes Y, Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}(A \otimes X, [Y,Z])
    \\
    & \simeq
    Hom_{\mathcal{C}}(A, [X, [Y,Z]])
  \end{aligned}
$$

Since this holds for all $A$, the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding}) says that there is an isomorphism $[ X\otimes Y, Z ] \simeq [X, [Y,Z]]$. Moreover, by taking $A = 1$ in the above and using the left [[unitor]] isomorphisms $A \otimes (X \otimes Y) \simeq X \otimes Y$ and $A\otimes X \simeq X$  we get a [[commuting diagram]]

$$
  \array{
    Hom_{\mathcal{C}}(1, [X\otimes Y, Z ))
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(1, [X, [Y,Z]])
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\mathcal{C}}(X \otimes Y, Z)
     &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(X, [Y,Z])
  }
  \,.
$$

=--

Also the key [[hom-functor preserves limits|respect]] of the [[hom-functor]] for [[limits]] is inherited by [[internal hom]]-functors

+-- {: .num_prop #InternalHomPreservesLimits}
###### Proposition
**([[internal hom]] preserves [[limits]])**

Let $\mathcal{C}$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with [[internal hom]]-[[bifunctor]] $[-,-]$ (Prop. \ref{InternalHomBifunctor}). Then this bifunctor [[preserved limit|preserves]] [[limits]] in the second variable, and sends [[colimits]] in the first variable to limits:

$$
  [X, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} Y(j)]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [X, Y(j)]
$$

and

$$
  [\underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j),X]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j),X]
$$



=--


+-- {: .proof}
###### Proof

For $X \in \mathcal{X}$ any object, $[X,-]$ is a [[right adjoint]] by definition, and hence preserves limits by Prop. \ref{AdjointsPreserveCoLimits}.

For the other case, let $Y \;\colon\; \mathcal{L} \to \mathcal{C}$ be a [[diagram]] in $\mathcal{C}$, and let $C \in \mathcal{C}$ be any object. Then there are isomorphisms

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(C, \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X )
    & \simeq
    Hom_{\mathcal{C}}( C \otimes \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X )
    \\
    & \simeq
    Hom_{\mathcal{C}}( \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} (C \otimes Y(j)), X )
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( (C \otimes Y(j)), X )
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( C, [Y(j), X] )
    \\
    & \simeq
    Hom_{\mathcal{C}}( C, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] )
  \end{aligned}
$$

which are [[natural isomorphism|natural]] in $C \in \mathcal{C}$, where we used that the ordinary [[hom-functor preserves limits]] (Prop. \ref{HomFunctorPreservesLimits}), and that the left adjoint $C \otimes (-)$ preserves colimits, since [[left adjoints preserve colimits]] (Prop. \ref{AdjointsPreserveCoLimits}).

Hence by the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]], there is an isomorphism

$$
  \left[ \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X \right]
  \overset{\simeq}{\longrightarrow}
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X]
  \,.
$$


=--

$\,$

Now that we have seen [[monoidal categories]] with various extra [[properties]], we next look at [[functors]] which preserve these:

+-- {: .num_defn #LaxMonoidalFunctor}
###### Definition
**([[monoidal functors]])**

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two [[monoidal categories]] (def. \ref{MonoidalCategory}). A _[[lax monoidal functor]]_ between them is

1. a [[functor]] (Def. \ref{Functors})

   $$
     F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,,
   $$

1. a [[morphism]]

   \[
     \label{UnitComponentOfMonoidalFunctor}
     \epsilon \;\colon\; 1_{\mathcal{D}} \longrightarrow F(1_{\mathcal{C}})
   \]

1. a [[natural transformation]] (Def. \ref{NaturalTransformations})

   \[
     \label{MonoidalComponentsOfMonoidalFunctor}
     \mu_{x,y}
       \;\colon\;
     F(x) \otimes_{\mathcal{D}} F(y)
       \longrightarrow
     F(x \otimes_{\mathcal{C}} y)
   \]

   for all $x,y \in \mathcal{C}$

satisfying the following conditions:

1. **([[associativity]])** For all objects $x,y,z \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (F(x) \otimes_{\mathcal{D}} F(y)) \otimes_{\mathcal{D}} F(z)
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

If $\epsilon$ and alll $\mu_{x,y}$ are [[isomorphisms]], then $F$ is called a **[[strong monoidal functor]]**.

If moreover $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are equipped with the structure of [[braided monoidal categories]] (def. \ref{BraidedMonoidalCategory}) with [[braidings]] $\tau^{\mathcal{C}}$ and $\tau^{\mathcal{D}}$, respectively, then the lax monoidal functor $F$ is called a **[[braided monoidal functor]]** if in addition the following [[commuting diagram|diagram commutes]] for all objects $x,y \in \mathcal{C}$

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

A [[homomorphism]] $f\;\colon\; (F_1,\mu_1, \epsilon_1) \longrightarrow (F_2, \mu_2, \epsilon_2)$ between two (braided) lax monoidal functors is a **[[monoidal natural transformation]]**, in that it is a [[natural transformation]] $f_x \;\colon\; F_1(x) \longrightarrow F_2(x)$ of the underlying functors

compatible with the product and the unit in that the following [[commuting diagram|diagrams commute]] for all objects $x,y \in \mathcal{C}$:

$$
  \array{
    F_1(x) \otimes_{\mathcal{D}} F_1(y)
      &\overset{f(x)\otimes_{\mathcal{D}} f(y)}{\longrightarrow}&
    F_2(x) \otimes_{\mathcal{D}} F_2(y)
    \\
    {}^{\mathllap{(\mu_1)_{x,y}}}\downarrow
     &&
    \downarrow^{\mathrlap{(\mu_2)_{x,y}}}
    \\
    F_1(x\otimes_{\mathcal{C}} y)
     &\underset{f(x \otimes_{\mathcal{C}} y ) }{\longrightarrow}&
    F_2(x \otimes_{\mathcal{C}} y)
  }
$$

and

$$
  \array{
    && 1_{\mathcal{D}}
    \\
    & {}^{\mathllap{\epsilon_1}}\swarrow && \searrow^{\mathrlap{\epsilon_2}}
    \\
    F_1(1_{\mathcal{C}})
     &&\underset{f(1_{\mathcal{C}})}{\longrightarrow}&&
    F_2(1_{\mathcal{C}})
  }
  \,.
$$

We write $MonFun(\mathcal{C},\mathcal{D})$ for the resulting [[category]] of lax monoidal functors between monoidal categories $\mathcal{C}$ and $\mathcal{D}$, similarly $BraidMonFun(\mathcal{C},\mathcal{D})$ for the category of braided monoidal functors between [[braided monoidal categories]], and $SymMonFun(\mathcal{C},\mathcal{D})$ for the category of braided monoidal functors between [[symmetric monoidal categories]].

=--

+-- {: .num_remark #SymmetricMonoidalFunctor}
###### Remark

In the literature the term "monoidal functor" often refers by default to what in def. \ref{LaxMonoidalFunctor} is called a _strong monoidal functor_.  But for the purpose of the discussion of [[functors with smash product]] [below](#FunctorsWithSmashProduct), it is crucial to admit the generality of lax monoidal functors.

If $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) then a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between them  is often called a **[[symmetric monoidal functor]]**.

=--

+-- {: .num_prop #MonoidalFunctorComp}
###### Proposition

For $\mathcal{C} \overset{F}{\longrightarrow} \mathcal{D} \overset{G}{\longrightarrow} \mathcal{E}$ two composable [[lax monoidal functors]] (def. \ref{LaxMonoidalFunctor}) between [[monoidal categories]], then their composite $F \circ G$ becomes a lax monoidal functor with structure morphisms

$$
  \epsilon^{G\circ F}
    \;\colon\;
  1_{\mathcal{E}}
    \overset{\epsilon^G}{\longrightarrow}
  G(1_{\mathcal{D}})
    \overset{G(\epsilon^F)}{\longrightarrow}
  G(F(1_{\mathcal{C}}))
$$

and

$$
  \mu^{G \circ F}_{c_1,c_2}
  \;\colon\;
  G(F(c_1)) \otimes_{\mathcal{E}} G(F(c_2))
   \overset{\mu^{G}_{F(c_1), F(c_2)}}{\longrightarrow}
  G( F(c_1) \otimes_{\mathcal{D}} F(c_2) )
    \overset{G(\mu^F_{c_1,c_2})}{\longrightarrow}
  G(F( c_1 \otimes_{\mathcal{C}} c_2 ))
  \,.
$$

=--


### Enriched categories
 {#EnrichedCategories}

The plain definition of [[categories]] in Def. \ref{Categories} is phrased in terms of [[sets]]. Via Example \ref{CategoryOfSets} this assigns a special role to the category [[Set]] of all sets, as the "base" on top, or the "[[cosmos]]" inside which [[category theory]] takes place. For instance, the fact that [[hom-sets]] in a plain [[category]] are indeed sets, is what makes the [[hom-functor]] (Example \ref{HomFunctor}) take values in [[Set]], and this, in turn, governs the form of the all-important [[Yoneda lemma]] (Prop. \ref{YonedaLemma}) and [[Yoneda embedding]] (Prop. \ref{YonedaEmbedding}) as statements about [[presheaves]] of sets (Example \ref{CategoryOfPresheaves}).

At the same time, [[category theory]] witnesses the utility of abstracting away from concrete choices to their abstract properties that are actually used in constructions. This makes it natural to ask if one could replace the category [[Set]] by some other category $\mathcal{V}$ which could similarly serve as a "[[cosmos]]" inside which category theory may be developed.

Indeed, such $\mathcal{V}$-[[enriched category theory]] (see Example  \ref{UnderlyingCategoryOfTopEnrichedCategory} below for the terminology) exists, beginning with the concept of $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory} below) and from there directly paralleling, hence generalizing, plain category theory, as long as one assumes the "cosmos" category $\mathcal{V}$ to share a minimum of abstract properties with [[Set]] (Def. \ref{Cosmos} below).

This turns out to be most useful. In fact, the perspective of [[enriched categories]] is helpful already when $\mathcal{V} = $ [[Set]], in which case it reproduces plain category theory (Example \ref{SetEnrichedCategoriesArePlainCategories} below), for instance in that it puts the [[limit|(co)limits]] of the special form of [[end|(co)ends]] (Def. \ref{EndAndCoendInTopcgSmash} below) to the forefront (discussed [below](#TopologicalEndsAndCoends)).

$\,$

+-- {: .num_defn #Cosmos}
###### Definition
**([[cosmos]])**

A _[[Jean Benabou|Bénabou]] [[cosmos]] for [[enriched category theory]]_, or just _[[cosmos]]_, for short, is a [[symmetric monoidal category|symmetric]] (Def. \ref{SymmetricMonoidalCategory}) [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}) $\mathcal{V}$  which has all [[limits]] and [[colimits]].

=--

+-- {: .num_example #ExamplesOfCosmoi}
###### Example
**(examples of [[cosmoi]] for [[enriched category theory]])**

The following are examples of [[cosmoi]] (Def. \ref{Cosmos}):

1. [[Set]] (Def. \ref{CategoryOfSets}) equipped with its [[cartesian closed category]]-structure (Example \ref{SetIsCartesianClosed})

1. [[Grpd]] (Def. \ref{CategoriesOfSmallCategories}) equipped with its [[cartesian closed category]]-structure (Example \ref{GrpdIsACartesianClosedCategory}).

=--

+-- {: .num_example #ChangeOfCosmosFromVToSet}
###### Example
**underlying [[set]] of an object in a [[cosmos]]**

Let $\mathcal{V}$ be a [[cosmos]] (Def. \ref{Cosmos}), with $1 \in \mathcal{V}$ its [[tensor unit]] (Def. \ref{MonoidalCategory}). Then the [[hom-functor]] (Def. \ref{HomFunctor}) out of $1$

$$
  Hom_{\mathcal{V}}(1,-)
  \;\colon\;
  \mathcal{V}
    \longrightarrow
  Set
$$

admits the [[structure]] of a [[lax monoidal functor]] (Def. \ref{LaxMonoidalFunctor}) to [[Set]], with the latter regarded with its [[cartesian monoidal category|cartesian monoidal]] [[structure]] from Example \ref{SetIsCartesianClosed}.

Given $V \in \mathcal{V}$, we call

$$
  Hom_{\mathcal{V}}(1,V) \;\in\; Set
$$

also the _underlying_ set of $V$.

=--


+-- {: .proof}
###### Proof

Take the monoidal transformations (eq"MonoidalComponentsOfMonoidalFunctor) to be


$$
  \array{
    Hom_{\mathcal{V}}(1, V_1)
    \times
    Hom_{\mathcal{V}}(1, V_2)
    \longrightarrow
    Hom_{\mathcal{V}}(1, V_1 \otimes V_2)
    \\
    \big( 1 \overset{f_1}{\to} V_1\;,\; 1 \overset{f_2}{\to} V_2 \big)
    &\mapsto&
    \big(
      1 \overset{\simeq}{\to} 1 \otimes 1
        \overset{f_1 \otimes f_2}{\longrightarrow}
      V_1 \otimes V_2
    \big)
  }
$$

and take the unit transformation (eq:UnitComponentOfMonoidalFunctor)

$$
  \array{
    \ast
      &\longrightarrow&
    Hom_{\mathcal{V}}(1,1)
  }
$$

to pick $id_1 \in Hom_{\mathcal{V}}(1,1)$.


=--

+-- {: .num_example #UnderlyingSetOfInternalHomIsHomSet}
###### Example
*(underlying set of [[internal hom]] is [[hom-set]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $X,Y \in Obj_{\mathcal{V}}$ be two [[objects]]. Then the underlying set (Def. \ref{ChangeOfCosmosFromVToSet}) of their [[internal hom]] $[X,Y] \in \mathcal{V}$ (Def. \ref{ClosedMonoidalCategory}) is the [[hom-set]] (Def. \ref{Categories}):

$$
  \mathcal{Hom}_{\mathcal{V}}\left( 1, [X,Y]\right)
  \;\simeq\;
  Hom_{\mathcal{V}}(X,Y)
  \,.
$$

This identification is the adjunction isomorphism (eq:HomIsomorphismForAdjointFunctors) for the internal hom adjunction (eq:InternalHomAdjunction) followed composed with a [[unitor]] (Def. \ref{MonoidalCategory}).

=--


+-- {: .num_defn #TopEnrichedCategory}
###### Definition
**([[enriched category]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), a  **$\mathcal{V}$-[[enriched category]]** $\mathcal{C}$ is:

1. a [[class]] $Obj_{\mathcal{C}}$, called the **class of [[objects]]**;

1. for each $a, b\in Obj_{\mathcal{C}}$, an [[object]]

   $$
     \mathcal{C}(a,b)\in \mathcal{V}
     \,,
   $$

   called the **$\mathcal{V}$-[[object of morphisms]]** between $a$ and $b$;

1. for each $a,b,c\in Obj(\mathcal{C})$ a [[morphism]] in $\mathcal{V}$

   $$
     \circ_{a,b,c}
       \;\colon\;
      \mathcal{C}(a,b)\times \mathcal{C}(b,c)
        \longrightarrow
      \mathcal{C}(a,c)
   $$

   out of the [[tensor product]] of [[hom-objects]], called the _[[composition]]_ operation;

1. for each $a \in Obj(\mathcal{C})$ a morphism  $Id_a \colon \ast \to  \mathcal{C}(a,a)$, called the _[[identity]]_ morphism on $a$

such that the composition is [[associativity|associative]] and [[unitality|unital]].

If the [[class]] $Obj_{\mathcal{C}}$ happens to be a [[set]] (hence a [[small set]] instead of a [[proper class]]) then we say the $\mathcal{V}$-enriched category $\mathcal{C}$ is _[[small category|small]]_, as in Def. \ref{SmallCategory}.

=--

+-- {: .num_example #SetEnrichedCategoriesArePlainCategories}
###### Example
**([[Set]]-[[enriched categories]] are plain [[categories]])**

An [[enriched category]] (Def. \ref{TopEnrichedCategory}) over the [[cosmos]] $\mathcal{V} = $ [[Set]], as in Example \ref{ExamplesOfCosmoi}, is the same as a plain [[category]] (Def. \ref{Categories}).

=--

+-- {: .num_example #UnderlyingCategoryOfTopEnrichedCategory}
###### Example
**(underlying [[category]] of an [[enriched category]])**

Let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}).

Using the [[lax monoidal functor|lax monoidal]] [[structure]] (Def. \ref{LaxMonoidalFunctor}) on the
[[hom functor]] (Example \ref{ChangeOfCosmosFromVToSet})

$$
  Hom_{\mathcal{V}}(1,-)
  \;\colon\;
  \mathcal{V} \longrightarrow Set
$$

out of the [[tensor unit]] $1 \in \mathcal{C}$ this induces a [[Set]]-[[enriched category]] $\vert \mathcal{C}\vert$ with hence an ordinary [[category]] (Example \ref{SetEnrichedCategoriesArePlainCategories}), with

* $Obj_{\vert \mathcal{C}\vert} \;\coloneqq\; Obj_{\mathcal{C}}$;

* $Hom_{\vert \mathcal{C}\vert}( X, Y )
   \;\coloneqq\;
  Hom_{\mathcal{V}}(1, \mathcal{C}(X,Y))$.

It is in this sense that $\mathcal{C}$ is a plain [[category]] ${\vert \mathcal{C}\vert}$ equipped with [[extra structure]], and hence an "[[enriched category]]".


=---



The archetypical example is $\mathcal{V}$ itself:

+-- {: .num_example #TopkAsATopologicallyEnrichedCategory}
###### Example
**($\mathcal{V}$ as a $\mathcal{V}$-[[enriched category]])**

Evert [[cosmos]] $\mathcal{C}$ (Def. \ref{Cosmos})  canonically obtains the structure of a $\mathcal{V}$-[[enriched category]], def. \ref{TopEnrichedCategory}:

the [[hom-objects]] are the [[internal homs]]

$$
  \mathcal{v}(X,Y)
    \coloneqq
  [X,Y]
$$

and with [[composition]]

$$
  [X,Y] \times [Y,Z]
    \longrightarrow
  [X,Z]
$$

given by the [[adjunct]] under the ([[Cartesian product]]$\dashv$ [[internal hom]])-[[adjunction]] of the [[evaluation morphisms]]

$$
  X \otimes  [XmY] \otimes [Y,Z]
    \overset{(ev, id)}{\longrightarrow}
  Y \otimes [Y,Z]
    \overset{ev}{\longrightarrow}
  Z
  \,.
$$


=--

The usual construction on categories, such as that of [[opposite categories]] (Def. \ref{OppositeCategory}) and [[product categories]] (Def. \ref{ProductCategory}) have evident enriched analogs


+-- {: .num_defn #OppositeAndProductOfPointedTopologicallyEnrichedCategory}
###### Definition
**([[enriched category|enriched]] [[opposite category]] and [[product category]])**

For $\mathcal{V}$ a [[cosmos]], let $\mathcal{C}, \mathcal{D}$ be $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}).

1. The **[[opposite category|opposite]] [[enriched category]]** $\mathcal{C}^{op}$ is the [[enriched category]] with the same [[objects]] as $\mathcal{C}$, with [[hom-objects]]

   $$
     \mathcal{C}^{op}(X,Y)
     \coloneqq
     \mathcal{C}(Y,X)
   $$

   and with [[composition]] given by [[braiding]] (eq:BraidingIsomorphism) followed by the [[composition]] in $\mathcal{C}$:

   $$
     \mathcal{C}^{op}(X,Y)
     \otimes
     \mathcal{C}^{op}(Y,Z)
     =
     \mathcal{C}(Y,X) \otimes \mathcal{C}(Z,Y)
     \underoverset{\simeq}{\tau}{\longrightarrow}
     \mathcal{C}(Z,Y) \otimes \mathcal{C}(Y,X)
       \overset{\circ_{Z,Y,X}}{\longrightarrow}
     \mathcal{C}(Z,X)
     =
     \mathcal{C}^{op}(X,Z)
     \,.
   $$

1. the **[[enriched category|enriched]] [[product category]]** $\mathcal{C} \times \mathcal{D}$ is the [[enriched category]] whose [[objects]] are [[pairs]] of objects $(c,d)$ with $c \in \mathcal{C}$ and $d\in \mathcal{D}$, whose [[hom-spaces]] are the [[tensor product]] of the separate [[hom objects]]

   $$
     (\mathcal{C}\times \mathcal{D})((c_1,d_1),\;(c_2,d_2) )
       \coloneqq
     \mathcal{C}(c_1,c_2)\otimes \mathcal{D}(d_1,d_2)
   $$

   and whose [[composition]] operation is the [[braiding]] (eq:BraidingIsomorphism) followed by the [[tensor product]] of the separate composition operations:

   $$
     \array{
       (\mathcal{C}\times \mathcal{D})((c_1,d_1), \; (c_2,d_2))
         \otimes
       (\mathcal{C}\times \mathcal{D})((c_2,d_2), \; (c_3,d_3))
       \\
       {}^{\mathllap{=}}\downarrow
       \\
       \left(\mathcal{C}(c_1,c_2) \otimes \mathcal{D}(d_1,d_2)\right)
         \otimes
       \left(\mathcal{C}(c_2,c_3) \otimes \mathcal{D}(d_2,d_3)\right)
       \\
       \downarrow^{\mathrlap{\tau}}_{\mathrlap{\simeq}}
       \\
       \left(\mathcal{C}(c_1,c_2) \otimes \mathcal{C}(c_2,c_3)\right)
         \otimes
       \left( \mathcal{D}(d_1,d_2) \otimes  \mathcal{D}(d_2,d_3)\right)
         &\overset{
             (\circ_{c_1,c_2,c_3}) \otimes (\circ_{d_1,d_2,d_3})
           }{\longrightarrow}
         &
       \mathcal{C}(c_1,c_3) \otimes \mathcal{D}(d_1,d_3)
       \\
       && \downarrow^{\mathrlap{=}}
       \\
       && (\mathcal{C}\times \mathcal{D})((c_1,d_1),\; (c_3,d_3))
     }
    \,.
   $$

=--




+-- {: .num_defn #TopologicallyEnrichedFunctor}
###### Definition
**([[enriched functor]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ and $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}).

A _$\mathcal{V}$-[[enriched functor]]_ from $\mathcal{C}$ to $\mathcal{D}$

$$
  F \;\colon\;  \mathcal{C}  \longrightarrow \mathcal{D}
$$

is

1. a [[function]]

   $$
     F_{Obj} \;\colon\; Obj_{\mathcal{C}} \longrightarrow Obj_{\mathcal{D}}
   $$

   of [[objects]];

1. for each $a,b \in Obj_{\mathcal{C}}$ a [[morphism]] in $\mathcal{V}$

   $$
     F_{a,b}
       \;\colon\;
     \mathcal{C}(a,b)
       \longrightarrow
     \mathcal{D}(F_0(a), F_0(b))
   $$

   between [[hom-objects]]

such that this preserves [[composition]] and [[identity]] morphisms in the evident sense.

=--

+-- {: .num_example #EnrichedHomFunctor}
###### Example
**([[enriched hom-functor]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). Then there is a $\mathcal{V}$-[[enriched functor]] out of the enriched [[product category]] of $\mathcal{C}$ with its enriched [[opposite category]] (Def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory})

$$
  \mathcal{C}(-,-)
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{V}
$$

to $\mathcal{V}$, regarded as a $\mathcal{V}$-[[enriched category]] (Example \ref{TopkAsATopologicallyEnrichedCategory}), which sends a [[pair]] of [[objects]] $X,Y \in \mathcal{C}$ to the [[hom-object]] $\mathcal{C}(X,Y) \in \mathcal{V}$, and which acts on morphisms by [[composition]] in the evident way.

=--

+-- {: .num_example #EnrichedPresheaf}
###### Example
**([[enriched presheaves]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]] (Def. \ref{TopEnrichedCategory}). Then a $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor})

$$
  F \;\colon\; \mathcal{C} \longrightarrow \mathcal{V}
$$

to the archetypical $\mathcal{V}$-[[enriched category]] from Example \ref{TopkAsATopologicallyEnrichedCategory} is:

1. an [[object]] $F_a \in Obj_{\mathcal{V}}$ for each object $a \in Obj_{\mathcal{C}}$;

1. a [[morphism]] in $\mathcal{V}$ of the form

   $$
     F_a \otimes \mathcal{C}(a,b) \longrightarrow F_b
   $$

   for all pairs of objects $a,b \in Obj(\mathcal{C})$

   (this is the [[adjunct]] of $F_{a,b}$ under the [[adjunction]] (eq:InternalHomAdjunction) on $\mathcal{V}$)

such that composition is respected, in the evident sense.

For every object $c \in \mathcal{C}$, there is an enriched [[representable functor]], denoted

$$
  y(c) \;\coloneqq\; \mathcal{C}(c,-)
$$

(where on the right we have the [[enriched hom-functor]] from Example \ref{EnrichedHomFunctor})

which sends objects to

$$
  y(c)(d) = \mathcal{C}(c,d) \in \mathcal{V}
$$

and whose action on morphisms is, under the above identification, just the [[composition]] operation in $\mathcal{C}$.

=--


More generally, the following situation will be of interest:

+-- {: .num_example #PointedTopologicalFunctorOnProductCategory}
###### Example
**([[enriched functor]] on [[enriched category|enriched]] [[product category]] with [[opposite category]])**

An $\mathcal{V}$-[[enriched functor]] (Def. \ref{TopologicallyEnrichedFunctor}) into $\mathcal{V}$ (Example \ref{TopkAsATopologicallyEnrichedCategory})  out of
an [[enriched category|enriched]] [[product category]] (Def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory})

$$
  F
    \;\colon\;
  \mathcal{C} \times \mathcal{D}
    \longrightarrow
  \mathcal{V}
$$

(an "enriched [[bifunctor]]") has component morphisms of the form

$$
  F_{(c_1,d_1),(c_2,d_2)}
    \;\colon\;
  \mathcal{C}(c_1,c_2)
  \otimes
  \mathcal{D}(d_1,d_2)
    \longrightarrow
  \big[ F_0((c_1,d_1)),F_0((c_2,d_2)) \big]
  \,.
$$

By functoriality and under passing to [[adjuncts]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) under (eq:InternalHomAdjunction)  this is equivalent to two commuting _[[actions]]_


$$
  \rho_{c_1,c_2}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \otimes F_0((c_1,d))
    \longrightarrow
  F_0((c_2,d))
$$

and

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{D}(d_1,d_2) \otimes F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$

In the special case of a functor out of the [[enriched category|enriched]] [[product category]] of some $\mathcal{V}$-[[enriched category]] $\mathcal{C}$ with its enriched [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory})

$$
  F
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{V}
$$

then this takes the form of a "pullback action" in the first variable

$$
  \rho_{c_2,c_1}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \otimes F_0((c_2,d))
    \longrightarrow
  F_0((c_1,d))
$$

and a "pushforward action" in the second variable

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{C}(d_1,d_2) \otimes F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$


=--


+-- {: .num_defn #EnrichedNaturalTransformation}
###### Definition
**([[enriched natural transformation]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$ and $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}) and let

$$
  \mathcal{C}
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {}
  \mathcal{D}
$$

be two $\mathcal{V}$-[[enriched functors]] (Def. \ref{TopologicallyEnrichedFunctor}) from $\mathcal{C}$ to $\mathcal{D}$.

Then a $\mathcal{V}$-[[enriched natural transformation]]

$$
  \mathcal{C}
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\overset{F}{\longrightarrow}}
      {\phantom{AA}\Downarrow{\mathrlap{\eta}}\phantom{AA}}
  \mathcal{D}
$$

is

* for each $c \in Obj_{\mathcal{C}}$ a choice of [[morphism]]

  $$
    \eta_c \;\colon\; I \longrightarrow \mathcal{D}(F(c),G(c))
  $$

  such that for each [[pair]] of [[objects]] $c,d \in \mathcal{C}$ the two [[morphisms]] (in $\mathcal{V}$)

\[
  \label{OneComposite}
  \eta_d \circ F(-)
   \;\colon\;
  \mathcal{C}(c,d)
    \overset{r}{\simeq}
  \mathcal{C}(c,d) \otimes I
    \overset{ G_{c,d} \otimes \eta_c }{\longrightarrow}
  \mathcal{D}(G(c),G(d)) \otimes \mathcal{D}( F(c), G(c) )
    \overset{\circ_{F(c), G(c), G(d)}}{\longrightarrow}
  \mathcal{D}(F(c), G(d))
\]

and

\[
  \label{OtherComposite}
  G(-) \circ \eta_c
    \;\colon\;
  \mathcal{C}(c,d)
    \overset{\ell}{\simeq}
  I \otimes  \mathcal{C}(c,d)
    \overset{ \eta_d \otimes F_{c,d} }{\longrightarrow}
  \mathcal{D}(F(d), G(d)) \otimes \mathcal{D}(F(c), F(d))
    \overset{\circ_{F(c),F(d), G(d)}}{\longrightarrow}
  \mathcal{D}(F(c), G(d))
\]

agree.

=--

+-- {: .num_example #CategoryOfEnrichedFunctors}
###### Example
**([[functor category]] of [[enriched functors]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos})
let $\mathcal{C}$, $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}). Then there is a [[category]] (Def. \ref{Categories}) of [[enriched functors]] (Def. \ref{TopologicallyEnrichedFunctor}), to be denoted

$$
  [\mathcal{C}, \mathcal{D}]
$$

whose [[objects]] are the [[enriched functors]] $\mathcal{C} \overset{F}{\to} \mathcal{D}$ and whose [[morphisms]] are the [[enriched natural transformations]] between these (Def. \ref{EnrichedNaturalTransformation}).

In the case that $\mathcal{V} = $ [[Set]], via Def. \ref{ExamplesOfCosmoi}, with $Set$-enriched categories identified with plain categories via Example \ref{SetEnrichedCategoriesArePlainCategories}, this coincides with the [[functor category]] from Example \ref{FunctorCategory}.

Notice that, at this point, $[\mathcal{C}, \mathcal{D}]$ is a plain [[category]], not itself a $\mathcal{V}$-[[enriched category]], unless $\mathcal{V} = $ [[Set]]. But it may be enhanced to one, this is Def. \ref{PointedTopologicalFunctorCategory} below.

=--

+-- {: .num_defn #TensoringAndPoweringOfTopologicallyEnrichedCopresheaves}
###### Definition
**([[tensoring]] and [[powering]] of [[enriched presheaves]])**

Let $\mathcal{C}$ be a $\mathcal{V}$-[[enriched category]], def. \ref{TopEnrichedCategory}, with $[\mathcal{C}, \mathcal{V}]$ its [[functor category]] of [[enriched functors]] (Example \ref{CategoryOfEnrichedFunctors}).

1. Define a [[functor]]

   $$
     (-)\cdot(-)
       \;\colon\;
     [\mathcal{C}, \mathcal{V}] \times \mathcal{V}
      \longrightarrow
     [\mathcal{C}, \mathcal{V}]
   $$

   by forming objectwise [[tensor products]]

   $$
     F \cdot X \;\colon\; c \mapsto F(c) \otimes X
     \,.
   $$

   This is called the **[[tensoring]]** of $[\mathcal{C}, \mathcal{V}]$ over $\mathcal{V}$.

1. Define a functor

   $$
     (-)^{(-)}
       \;\colon\;
     \mathcal{V}^{op} \times [\mathcal{C}, \mathcal{V}]
       \longrightarrow
     [\mathcal{C}, \mathcal{V}]
   $$

   by forming objectwise [[internal homs]] (Def. \ref{ClosedMonoidalCategory})

   $$
     F^X \;\colon\; c \mapsto [X,F(c)]
     \,.
   $$

   This is called the **[[powering]]** of $[\mathcal{C}, \mathcal{V}]$ over $\mathcal{V}$.


=--

There is now the following evident generalization of the concept of _[[adjoint functors]]_ (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}) from plain [[category theory]] to [[enriched category theory]]:

+-- {: .num_defn #EnrichedAdjunction}
###### Definition
**([[enriched adjunction]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$, $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}). Then an _[[adjoint pair]] of $\mathcal{V}$-[[enriched functors]]_ or _[[enriched adjunction]]_

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

is a [[pair]] of $\mathcal{V}$-[[enriched functors]] (Def. \ref{TopologicallyEnrichedFunctor}), as shown, such that there is a $\mathcal{V}$-[[enriched natural isomorphism]] (Def. \ref{EnrichedNaturalTransformation}) between [[enriched hom-functors]] (Def. \ref{EnrichedHomFunctor}) of the form

\[
  \label{EnrichedAdjunctionIsomorphism}
  \mathcal{C}(L(-),-)
  \;\simeq\;
  \mathcal{D}(-,R(-))
  \,.
\]

=--


+-- {: .num_defn #EnrichedEquivalenceOfCategories}
###### Definition
**([[enriched category theory|enriched]] [[equivalence of categories]])**

For $\mathcal{V}$ a [[cosmos]] (Def. \ref{Cosmos}), let $\mathcal{C}$, $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]] (Def. \ref{TopEnrichedCategory}). Then an _equivalence of enriched categories_

$$
  \array{
    \mathcal{C}
      \underoverset
        {\underset{R}{\longrightarrow}}
        {\overset{L}{\longleftarrow}}
        {\phantom{AA} \simeq \phantom{AA}}
    \mathcal{D}
  }
$$

is a [[pair]] of $\mathcal{V}$-[[enriched functors]] back and forth, as shown (Def. \ref{TopologicallyEnrichedFunctor}), together with $\mathcal{V}$-[[enriched natural isomorphisms]] (Def. \ref{EnrichedNaturalTransformation}) between their [[composition]] and the [[identity functors]]:

$$
  id_{\mathcal{D}} \overset{\simeq}{\Rightarrow} R \circ L
  \phantom{AAA}
   \text{and}
  \phantom{AAA}
  L \circ R \overset{\simeq}{\Rightarrow} id_{\mathcal{C}}
  \,.
$$


=--

