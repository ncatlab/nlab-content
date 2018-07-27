

+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ (Def. \ref{MonoidalCategory}), then a **[[monoid in a monoidal category|monoid internal to]]** $(\mathcal{C}, \otimes, 1)$ is

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

1. {#UnitalityMonoid} ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

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

Write $Mon(\mathcal{C}, \otimes,1)$ for the **[[category of monoids]]** in $\mathcal{C}$, and $CMon(\mathcal{C}, \otimes, 1)$ for its subcategory of commutative monoids.


=--

+-- {: .num_example #MonoidGivenByTensorUnit}
###### Example

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ (Def. \ref{MonoidalCategory}), the [[tensor unit]] $1$ is a [[monoid in a monoidal category|monoid in]] $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}) with product given by either the left or right [[unitor]]

$$
  \ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1
  \,.
$$

By lemma \ref{kel1}, these two morphisms coincide and define an [[associativity|associative]] product with unit the identity $id \colon 1 \to 1$.

If $(\mathcal{C}, \otimes , 1)$ is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}), then this monoid is a [[commutative monoid in a symmetric monoidal category|commutative monoid]].

=--

+-- {: .num_example #TensorProductOfTwoCommutativeMonoids}
###### Example

Given a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}), and given two [[commutative monoid in a symmetric monoidal category|commutative monoids]] $(E_i, \mu_i, e_i)$ $i \in \{1,2\}$ (def. \ref{MonoidsInMonoidalCategory}), then the [[tensor product]] $E_1 \otimes E_2$ becomes itself a commutative monoid with unit morphism

$$
  e \;\colon\;
  1
    \overset{\simeq}{\longrightarrow}
  1 \otimes 1
    \overset{e_1 \otimes e_2}{\longrightarrow}
  E_1 \otimes E_2
$$

(where the first isomorphism is, $\ell_1^{-1} = r_1^{-1}$ (lemma \ref{kel1})) and with product morphism given by

$$
  E_1 \otimes E_2
   \otimes
  E_1 \otimes E_2
   \overset{id \otimes \tau_{E_2, E_1} \otimes id}{\longrightarrow}
  E_1 \otimes E_1 \otimes E_2 \otimes E_2
   \overset{\mu_1 \otimes \mu_2}{\longrightarrow}
  E_1 \otimes E_2
$$

(where we are notationally suppressing the [[associators]] and where $\tau$ denotes the [[braiding]] of $\mathcal{C}$).

That this definition indeed satisfies associativity and commutativity follows from the corresponding properties of $(E_i,\mu_i, e_i)$, and from the hexagon identities for the braiding (def. \ref{BraidedMonoidalCategory}) and from symmetry of the braiding.

Similarly one checks that for $E_1 = E_2 = E$ then the unit maps

$$
  E \simeq E \otimes 1
    \overset{id \otimes e}{\longrightarrow}
  E \otimes E
$$

$$
  E \simeq 1 \otimes E
    \overset{e \otimes 1}{\longrightarrow}
  E \otimes E
$$

and the product map

$$
  \mu
    \;\colon\;
  E \otimes E
    \longrightarrow
  E
$$

and the braiding

$$
  \tau_{E,E}
    \;\colon\;
  E \otimes E
    \longrightarrow
  E \otimes E
$$

are monoid homomorphisms, with $E \otimes E$ equipped with the above monoid structure.


=--


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

The archetypical case in which all these abstract concepts reduce to the basic familiar ones is the symmetric monoidal category [[Ab]] of [[abelian groups]] from example \ref{ExampleAbelianGroupsOfMonoidalCategory}.

1. A [[monoid in a monoidal category|monoid in]] $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[ring]].

1. A [[commutative monoid in a symmetric monoidal category|commutative monoid in]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[commutative ring]] $R$.

1. An $R$-[[module object]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{ModulesInMonoidalCategory}) is equivalently an $R$-[[module]];

1. The tensor product of $R$-module objects (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[tensor product of modules]].

1. The [[category of modules|category of module objects]] $R Mod(Ab)$ (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[category of modules]] $R Mod$.

=--

+-- {: .num_example #dgAlgebraAreMonoidsInChainComplexes}
###### Example

Closely related to the example \ref{RingsAreMonoidsInAb}, but closer to the structure we will see below for spectra, are [[monoid in a monoidal category|monoids]] in the [[category of chain complexes]] $(Ch_\bullet, \otimes, \mathbb{Z})$ from example \ref{SymmetricMonoidalCategoryOfChainComplexes}. These monoids are equivalently [[differential graded algebras]].


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

Here the the top square is the [[natural transformation|naturality]] of the right [[unitor]], the middle square commutes by the functoriality of the tensor product $\otimes \;\colon\; \mathcal{C}\times \mathcal{C} \longrightarrow \mathcal{C}$ and the definition of the [[product category]] (spring), while the commutativity of the bottom square is the assumption that $f$ coequalizes $id \otimes \mu$ with $\mu \otimes id$.

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
