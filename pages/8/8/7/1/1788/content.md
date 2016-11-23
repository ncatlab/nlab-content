
### Modules in tensor categories and Super vector bundles
 {#Modules InTensorCategories}

Above (in def. \ref{Affines}) we considered spaces $X$ from a dual perspective, as determined by their [[algebras of functions]] $\mathcal{O}(X)$. In the same spirit then we are to express various constructions on and with spaces in terms of dual algebraic constructions.

A key such construction is that of [[vector bundles]] over $X$. Suppose that $X$ is a [[smooth manifold]], and $V \stackrel{p}{\to} X$ is an ordinary smooth real [[vector bundle]] over $X$. A [[section]] of this vector bundle is a smooth function $\sigma \colon X \to V$ such that $p \circ \sigma = id$

$$
  \array{
     && V
    \\ & {}^{\mathllap{\sigma}}\nearrow & \downarrow^{\mathrlap{p}}
    \\
    X &=& X
  }
  \,.
$$


Write $\Gamma_X(V)$ for the set of all such sections. Observe that this set inherits various extra [[stuff, structure, property|structure]]. 

First of all, since $V \to X$ is a vector bundle, we have [[fiber]]-wise the vector space operations. This means that
given two elements $c_1, c_2 \in \mathbb{R}$ in the [[real numbers]], and given two sections $\sigma_1$ and $\sigma_2$, we may form in each [[fiber]] $V_x$ the [[linear combination]] $c_1 \sigma_1(x) + c_2 \sigma_2(x)$. This hence yields a new section $c_1 \sigma_1 + c_2 \sigma_2$. Hence the set of sections of a vector bundle naturally forms itself a vector space.

But there is more structure. We need not multiply with the same element $c \in \mathbb{R}$ in each fiber, but we may multiply the section in each fiber by a different element, as long as the choice of element varies smoothly with the fibers, so that the resulting section is still smooth.

In other words, every element $f \in C^\infty(X)$ in the $\mathbb{R}$-algebra of [[smooth functions]] on $X$, takes a smooth section $\sigma$ of $V$ to a new smooth section $f \cdot \sigma$. This operation enjoys some evident properties. It is [[bilinear map|bilinear]] in the real vector spaces $C^\infty(X)$ and $\Gamma_X(V)$, and it satisfies the "[[action|action property]]" 

$$
  (f g) \cdot \sigma = f\cdot (g \cdot \sigma)
$$

for any two smooth functions $f,g \in C^\infty(X)$.

One says that a [[vector space]] such as $\Gamma_X(V)$ equipped with an [[action]] of an algebra $R$ this way is a _[[module]]_ over $R$.

In conclusion, any [[vector bundle]] $V \to X$ gives rise to an $C^\infty(X)$-[[module]] $\Gamma_X(V)$.

The _[[Serre-Swan theorem]]_ states sufficient conditions on $X$ such that the converse holds. 

+-- {: .num_prop} 
###### Proposition
**([Swan 62](Serre-Swan+theorem#Swan))**

Given a [[Hausdorff space|Hausdorff]] [[compact space]] $X$, the [[category]] of [[finitely generated module|finitely generated]] [[projective modules]] over the [[continuous function|continuous]]-[[function algebra]] $C(X)$ is [[equivalence of categories|equivalent]] to the category of finite-[[rank]] [[vector bundles]] on $X$, where the equivalence is established by sending a vector bundle to the its module of continuous [[sections]].

=--


This allows to _identify_ suitable $\mathcal{O}(X)$-modules with vector bundles over $X$. But then, if the suitable conditions do not hold, $R$-modules still behave a lot like sections of vector bundles over $Spec(R)$, and hence may be regarded as generalized vector bundles ([[quasi-coherent sheaves]]).



+-- {: .num_defn #ModulesInMonoidalCategory}
###### Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidalCategory}), and given $(A,\mu,e)$ a [[monoid in a monoidal category|monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), then a **left [[module object]]** in $(\mathcal{C}, \otimes, 1)$ over $(A,\mu,e)$ is

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
       && N
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


=--

+-- {: .num_example #EveryObjectIsModuleOverTensorUnit}
###### Example

Given a [[monoidal category]] $(\mathcal{C},\otimes, 1)$ (def. \ref{MonoidalCategory}) with the [[tensor unit]] $1$ regarded as a [[monoid in a monoidal category]] via example \ref{MonoidGivenByTensorUnit}, then the left [[unitor]]

$$
  \ell_C 
    \;\colon\;
  1\otimes C \longrightarrow C
$$

makes every object $C \in \mathcal{C}$ into a left module, according to def. \ref{ModulesInMonoidalCategory}, over $C$. The action property holds due to lemma \ref{kel1}. This gives an [[equivalence of categories]]

$$
  \mathcal{C} \simeq 1 Mod(\mathcal{C})
$$

of $\mathcal{C}$ with the [[category of modules]] over its tensor unit.


=--

+-- {: .num_example #RingsAreMonoidsInAb}
###### Example

The topic of general [[algebra]], not necessarily over [[ground fields]], is the above general concepts of mnoids and their modules spcialized to the ambient [[symmetric monoidal category]] being the category [[Ab]] of  [[abelian groups]] regarded as a [[symmetric monoidal category]] via the [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ (whose [[tensor unit]] is the additive group of [[integers]] $\mathbb{Z}$):

1. A [[monoid in a monoidal category|monoid in]] $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[ring]]. 

1. A [[commutative monoid in a symmetric monoidal category|commutative monoid in]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[commutative ring]] $R$.

1. An $R$-[[module object]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{ModulesInMonoidalCategory}) is equivalently an $R$-[[module]];

1. The tensor product of $R$-module objects (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[tensor product of modules]].

1. The [[category of modules|category of module objects]] $R Mod(Ab)$ (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[category of modules]] $R Mod$.

=--




+-- {: .num_prop #MonoidModuleOverItself} 
###### Proposition

In the situation of def. \ref{ModulesInMonoidalCategory}, the monoid $(A,\mu, e)$ canonically becomes a left module over itself by setting $\rho \coloneqq \mu$. More generally, for $C \in \mathcal{C}$ any object, then $A \otimes C$ naturally becomes a left $A$-module by setting:

$$
  \rho
  \;\colon\;
  A \otimes (A \otimes C)
   \underoverset{\simeq}{a^{-1}_{A,A,C}}{\longrightarrow}
  (A \otimes A) \otimes C
    \overset{\mu \otimes id}{\longrightarrow}
  A \otimes C
  \,.
$$

The $A$-modules of this form are called **[[free modules]]**.

The [[free functor]] $F$ constructing free $A$-modules is [[left adjoint]] to the [[forgetful functor]] $U$ which sends a module $(N,\rho)$ to the underlying object $U(N,\rho) \coloneqq N$.

$$
  A Mod(\mathcal{C})
    \underoverset
     {\underset{U}{\longrightarrow}}
     {\overset{F}{\longleftarrow}}
     {\bot}
  \mathcal{C}
  \,.
$$

=--

+-- {: .proof}
###### Proof

A homomorphism out of a free $A$-module is a morphism in $\mathcal{C}$ of the form

$$
  f \;\colon\; A\otimes C \longrightarrow N
$$

fitting into the diagram (where we are notationally suppressing the [[associator]])

$$
  \array{
    A \otimes A \otimes C
      &\overset{A \otimes f}{\longrightarrow}&
    A \otimes N
    \\
    {}^{\mathllap{\mu \otimes id}}\downarrow 
      && 
    \downarrow^{\mathrlap{\rho}}
    \\
    A \otimes C
      &\underset{f}{\longrightarrow}&
    N
  }
  \,.
$$

Consider the composite

$$
  \tilde f
    \;\colon\;
  C
    \underoverset{\simeq}{\ell_C}{\longrightarrow}
  1 \otimes C
    \overset{e\otimes id}{\longrightarrow}
  A \otimes C
    \overset{f}{\longrightarrow}
  N
  \,,
$$

i.e. the restriction of $f$ to the unit "in" $A$. By definition, this fits into a [[commuting square]] of the form (where we are now notationally suppressing the [[associator]] and the [[unitor]])

$$
  \array{
   A \otimes C
     &\overset{id \otimes \tilde f}{\longrightarrow}&
   A \otimes N
   \\
   {}^{\mathllap{id \otimes e \otimes id}}\downarrow 
     && 
   \downarrow^{\mathrlap{=}}
   \\
   A \otimes A \otimes C
    &\underset{id \otimes f}{\longrightarrow}&
   A \otimes N
  }
  \,.
$$

Pasting this square onto the top of the previous one yields

$$
  \array{
   A \otimes C
     &\overset{id \otimes \tilde f}{\longrightarrow}&
   A \otimes N
   \\
   {}^{\mathllap{id \otimes e \otimes id}}\downarrow 
     && 
   \downarrow^{\mathrlap{=}}
    \\
    A \otimes A \otimes C
      &\overset{A \otimes f}{\longrightarrow}&
    A \otimes N
    \\
    {}^{\mathllap{\mu \otimes id}}\downarrow 
      && 
    \downarrow^{\mathrlap{\rho}}
    \\
    A \otimes C
      &\underset{f}{\longrightarrow}&
    N
  }
  \,,
$$

where now the left vertical composite is the identity, by the unit law in $A$. This shows that $f$ is uniquely determined by $\tilde f$ via the relation

$$
  f = \rho \circ (id_A \otimes \tilde f)
  \,.
$$

This natural bijection between $f$ and $\tilde f$ establishes the adjunction.


=--

+-- {: .num_defn #TensorProductOfModulesOverCommutativeMonoidObject}
###### Definition

Given a [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}, def. \ref{ClosedMonoidalCategory}), given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), and given $(N_1, \rho_1)$ and $(N_2, \rho_2)$ two left $A$-[[module objects]] (def.\ref{MonoidsInMonoidalCategory}), then 

1. the **[[tensor product of modules]]** $N_1 \otimes_A N_2$ is, if it exists, the [[coequalizer]]

   $$
     N_1 \otimes A \otimes N_2
     \underoverset
       {\underset{\rho_{1}\circ (\tau_{N_1,A} \otimes N_2)}{\longrightarrow}}
       {\overset{N_1 \otimes \rho_2}{\longrightarrow}}
       {\phantom{AAAA}}
     N_1 \otimes N_1
       \overset{coeq}{\longrightarrow}
     N_1 \otimes_A N_2
   $$

   and if $A \otimes (-)$ preserves these coequalizers, then this is equipped with the left $A$-action induced from the left $A$-action on $N_1$ 

1. the **function module** $hom_A(N_1,N_2)$ is, if it exists, the [[equalizer]]

   $$
     hom_A(N_1, N_2)
       \overset{equ}{\longrightarrow}
     hom(N_1, N_2)
       \underoverset
         {\underset{hom(A \otimes N_1, \rho_2)\circ (A \otimes(-))}{\longrightarrow}}
         {\overset{hom(\rho_1,N_2)}{\longrightarrow}}
         {\phantom{AAAAAA}}
       hom(A \otimes N_1, N_2)
     \,.
   $$

   equipped with the left $A$-action that is induced by the left $A$-action on $N_2$ via

   $$
     \frac{
       A \otimes hom(X,N_2) \longrightarrow hom(X,N_2)
     }{
      A \otimes hom(X,N_2) \otimes X 
        \overset{id \otimes ev}{\longrightarrow}
      A \otimes N_2 \overset{\rho_2}{\longrightarrow} N_2
     }
     \,.
   $$

=--

(e.g. [Hovey-Shipley-Smith 00, lemma 2.2.2 and lemma 2.2.8](#HoveyShipleySmith00))



+-- {: .num_prop #MonoidalCategoryOfModules}
###### Proposition

Given a [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}, def. \ref{ClosedMonoidalCategory}), and given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}). If all [[coequalizers]] exist in $\mathcal{C}$, then the [[tensor product of modules]] $\otimes_A$ from def. \ref{TensorProductOfModulesOverCommutativeMonoidObject} makes the [[category of modules]] $A Mod(\mathcal{C})$ into a [[symmetric monoidal category]], $(A Mod, \otimes_A, A)$ with [[tensor unit]] the object $A$ itself, regarded as an $A$-module via prop. \ref{MonoidModuleOverItself}.

If moreover all [[equalizers]] exist, then this is a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) with [[internal hom]] given by the function modules $hom_A$ of def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}.

=--

(e.g. [Hovey-Shipley-Smith 00, lemma 2.2.2, lemma 2.2.8](#HoveyShipleySmith00))

+-- {: .proof}
###### Proof sketch

The associators and braiding for $\otimes_{A}$ are induced directly from those of $\otimes$ and the [[universal property]] of [[coequalizers]]. That $A$ is the tensor unit for $\otimes_{A}$ follows with the same kind of argument that we give in the proof of example \ref{FreeModulesTensorProduct} below.

=--

+-- {: .num_example #FreeModulesTensorProduct}
###### Example

For $(A,\mu,e)$ a [[monoid in a monoidal category|monoid]] (def. \ref{MonoidsInMonoidalCategory}) in a [[symmetric monoidal category]] $(\mathcal{C},\otimes, 1)$ (def. \ref{MonoidalCategory}), the [[tensor product of modules]] (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) of two [[free modules]] (def. \ref{MonoidModuleOverItself}) $A\otimes C_1$ and $A \otimes C_2$ always exists and is the free module over the tensor product in $\mathcal{C}$ of the two generators:

$$
  (A \otimes C_1) \otimes_A (A \otimes C_2)
  \simeq
  A \otimes (C_1 \otimes C_2)
  \,.
$$

Hence if $\mathcal{C}$ has all [[coequalizers]], so that the [[category of modules]] is a [[monoidal category]] $(A Mod, \otimes_A, A)$ (prop. \ref{MonoidalCategoryOfModules}) then the free module functor (def. \ref{MonoidModuleOverItself}) is a [[strong monoidal functor]] (def. \ref{LaxMonoidalFunctor})

$$
  F
    \;\colon\;
  (\mathcal{C}, \otimes, 1)
    \longrightarrow
  (A Mod, \otimes_A, A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is sufficient to show that the diagram

$$
  A \otimes A \otimes A
   \underoverset
    {\underset{id \otimes \mu}{\longrightarrow}}
    {\overset{\mu \otimes id}{\longrightarrow}}
    {\phantom{AAAA}}
  A \otimes A
    \overset{\mu}{\longrightarrow}
  A 
$$

is a [[coequalizer]] diagram (we are notationally suppressing the [[associators]]), hence that $A \otimes_A A \simeq A$, hence that the claim holds for $C_1 = 1$ and $C_2 = 1$.

To that end, we check the [[universal property]] of the [[coequalizer]]:

First observe that $\mu$ indeed coequalizes $id \otimes \mu$ with $\mu \otimes id$, since this is just the [[associativity]] clause in def. \ref{MonoidsInMonoidalCategory}. So for $f \colon A \otimes A \longrightarrow Q$ any other morphism with this property, we need to show that there is a unique morphism $\phi \colon A \longrightarrow Q$ which makes this [[commuting diagram|diagram commute]]:

$$
  \array{
    A \otimes A &\overset{\mu}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow & \swarrow_{\mathrlap{\phi}}
    \\
    Q
  }
  \,.
$$

We claim that 

$$
  \phi 
    \;\colon\;
  A 
    \underoverset{\simeq}{r^{-1}}{\longrightarrow} 
  A \otimes 1 
    \overset{id \otimes e}{\longrightarrow}
  A \otimes A
    \overset{f}{\longrightarrow}
  Q
  \,,
$$

where the first morphism is the inverse of the right [[unitor]] of $\mathcal{C}$.

First to see that this does make the required triangle commute, consider the following pasting composite of [[commuting diagrams]]

$$
  \array{
    A \otimes A &\overset{\mu}{\longrightarrow}& A
    \\
    {}^{\mathllap{id \otimes r^{-1}}}_{\mathllap{\simeq}}\downarrow 
      &&
    \downarrow^{\mathrlap{r^{-1}}}_{\simeq}
    \\
    A \otimes A \otimes 1 
      &\overset{\mu \otimes id}{\longrightarrow}&
    A \otimes 1
    \\
    {}^{\mathllap{id \otimes e}}\downarrow 
      && 
    \downarrow^{\mathrlap{id \otimes e} }
    \\
    A \otimes A \otimes A 
      &\overset{\mu \otimes id}{\longrightarrow}&
    A \otimes A
    \\
    {}^{\mathllap{id \otimes \mu}}\downarrow
      &&
    \downarrow^{\mathrlap{f}}
    \\
    A \otimes A 
      &\underset{f}{\longrightarrow}& 
    Q
  }
  \,.
$$

Here the the top square is the [[natural transformation|naturality]] of the right [[unitor]], the middle square commutes by the functoriality of the tensor product $\otimes \;\colon\; \mathcal{C}\times \mathcal{C} \longrightarrow \mathcal{C}$ and the definition of the [[product category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), while the commutativity of the bottom square is the assumption that $f$ coequalizes $id \otimes \mu$ with $\mu \otimes id$. 

Here the right vertical composite is $\phi$,  while, by [unitality](#UnitalityMonoid) of $(A,\mu ,e)$, the left vertical composite is the identity on $A$, Hence the diagram says that $\phi \circ \mu = f$, which we needed to show.

It remains to see that $\phi$ is the unique morphism with this property for given $f$. For that let $q \colon A \to Q$ be any other morphism with $ q\circ \mu = f$. Then consider the [[commuting diagram]]

$$
  \array{
    A \otimes 1 &\overset{\simeq}{\longleftarrow}& A
    \\
    {}^{\mathllap{id\otimes e}}\downarrow & \searrow^{\simeq}
    & \downarrow^{\mathrlap{=}}
    \\
    A \otimes A &\overset{\mu}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow & \swarrow_{\mathrlap{q}}
    \\
    Q
  }
  \,,
$$

where the top left triangle is the [unitality](#UnitalityMonoid) condition and the two isomorphisms are the right [[unitor]] and its inverse. The commutativity of this diagram says that $q = \phi$. 


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

When thinking of commutative monoids in some tensor category as [[formal duals]] to certain [[spaces]], then we are interested in forming [[Cartesian products]] and more generally [[fiber products]] of these spaces. Dually this is given by [[coproducts]] of commutative monoids and commutative $R$-algebras. The following says that these may be computed just as the [[tensor product of modules]]:


+-- {: .num_prop #CoproductsInCMon}
###### Proposition

Suppose that $\mathcal{C}$ is 

* a [[symmetric monoidal category]];

* with [[reflexive coequalizers]]

* that are preserved by the [[tensor product]] functors $A \otimes (-) \colon \mathcal{C} \to \mathcal{C}$ for all objects $A$ in $\mathcal{C}$.

Then for $f \colon A \to B$ and $g \colon A \to C$ two morphisms in the category $CMon(\mathcal{})$ of _[[commutative monoids]]_ in $\mathcal{C}$, the underlying object in $\mathcal{C}$ of the [[pushout]] in $CMon(\mathcal{C})$ coincides with that of the pushout in the category $A$[[Mod]] of $A$-[[modules]]

$$
  U(B \coprod_A C) \simeq  B \otimes_A C 
  \,.
$$

Here $B$ and $C$ are regarded as equipped with the canonical $A$-module structure induced by the morphisms $f$ and $g$, respectively.

Dually this means that the [[opposite category]] $CMon(\mathcal{A})^{op}$ has [[finite products]] and hence the structure of a [[Cartesian monoidal category]]:

$$
  Spec(A_1) \times Spec(A_2) \simeq Spec(A_1 \otimes_R A_2)
  \,.
$$

=--

This appears for instance as ([[Sketches of an Elephant|Johnstone, page 478, cor. 1.1.9]]).





