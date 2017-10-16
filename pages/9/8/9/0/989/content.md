
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### Over ordinary rings

For $R$ a [[commutative ring]], an **associative unital $R$-algebra** 
is equivalently 

* a [[monoid]] [[internalization|internal to]] $R$[[Mod]] equipped with the [[tensor product of modules]] $\otimes$;

* a [[pointed object|pointed]] one-object category [[enriched category|enriched over]] $(R Mod, \otimes)$;

* a pointed $R$-[[algebroid]] with one object;

* an  $R$-[[module]] $V$ equipped with [[linear maps]] $p : V \otimes V \to V$ and $i : R \to V$ satisfying the associative and unit laws;

* a [[ring]] $A$ [[under category|under]] $R$ such that the corresponding map $R \to A$ lands in the [[center]] of $A$.

If there is no danger for confusion, one often says simply 'associative algebra', or even only '[[algebra]]'.

More generally, a (merely) **associative algebra** need not have $i: R \to V$; that is, it is a [[semigroup]] instead of a monoid.

Less generally, a **[[commutative algebra]]** (where associative and unital are usually assumed) is an [[abelian monoid]] in $Vect$.

### Over monoids in a monoidal category
 {#OverMonoidsInAMonoidalCategory}

+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, then a **[[monoid in a monoidal category|monoid internal to]]** $(\mathcal{C}, \otimes, 1)$ is

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

Moreover, if $(\mathcal{C}, \otimes , 1)$ has the structure of a [[symmetric monoidal category]]  $(\mathcal{C}, \otimes, 1, B)$ with symmetric [[braiding]] $\tau$, then a monoid $(A,\mu, e)$ as above is called a **[[commutative monoid in a symmetric monoidal category|commutative monoid in]]** $(\mathcal{C}, \otimes, 1, B)$ if in addition

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

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, and given $(A,\mu,e)$ a [[monoid in a monoidal category|monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), then a **left [[module object]]** in $(\mathcal{C}, \otimes, 1)$ over $(A,\mu,e)$ is

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

This is naturally a (pointed) [[topologically enriched category]] itself.

=--

+-- {: .num_defn #TensorProductOfModulesOverCommutativeMonoidObject}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$, given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), and given $(N_1, \rho_1)$ and $(N_2, \rho_2)$ two left $A$-[[module objects]] (def.\ref{MonoidsInMonoidalCategory}), then the **[[tensor product of modules]]** $N_1 \otimes_A N_2$ is, if it exists, the [[coequalizer]]

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

Given a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}), and given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}). If all [[coequalizers]] exist in $\mathcal{C}$, then the [[tensor product of modules]] $\otimes_A$ from def. \ref{TensorProductOfModulesOverCommutativeMonoidObject} makes the [[category of modules]] $A Mod(\mathcal{C})$ into a [[symmetric monoidal category]], $(A Mod, \otimes_A, A)$ with [[tensor unit]] the object $A$ itself.

=--

+-- {: .num_defn #AAlgebra}
###### Definition

Given a [[monoidal category|monoidal]] [[category of modules]] $(A Mod , \otimes_A , A)$ as in prop. \ref{MonoidalCategoryOfModules}, then a [[monoid in a monoidal category|monoid]] $(E, \mu, e)$ in  $(A Mod , \otimes_A , A)$ (def. \ref{MonoidsInMonoidalCategory}) is called an **$A$-[[associative algebra|algebra]]**.

=--

+-- {: .num_prop }
###### Proposition

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


## Variants

* A [[cosimplicial algebra]] is a [[cosimplicial object]] in the category of algebras.

* A [[dg-algebra]] is a [[monoid]] not in [[Vect]] but in the category of (co)[[chain complex]]es.

* A [[smooth algebra]] is an associative $\mathbb{R}$-algebra that has not only the usual binary product induced from the product $\mathbb{R}\times \mathbb{R} \to \mathbb{R}$, but has a $n$-ary product operation for every [[smooth function]] $\mathbb{R}^n \to \mathbb{R}$.

  This may be understood as a special case of an [[algebra over a Lawvere theory]], here the [[Lawvere theory]] [[CartSp]].

## Examples

* [[function algebra]]

## Properties

### Tannaka duality

[[!include structure on algebras and their module categories - table]]

## Related concepts

* [[noncommutative algebra]]

* [[nonassociative algebra]]

* [[nonunital algebra]]

* [[finitely generated algebra]], [[finitely presented algebra]]

* [[power-associative algebra]]

* [[augmented algebra]]

* [[unitisation of C*-algebras]]

* [[differential algebra]]

* [[differential graded algebra]], [[A-infinity algebra]]

## References

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], _[[Rings, modules and algebras in stable homotopy theory]]_, AMS Mathematical Surveys and Monographs Volume 47 (1997) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/EKMM.pdf))




[[!redirects associative unital algebra]]
[[!redirects associative unital algebras]]
[[!redirects unital associative algebra]]
[[!redirects unital associative algebras]]
[[!redirects associative algebra]]
[[!redirects associative algebras]]
[[!redirects unital algebra]]
[[!redirects unital algebras]]