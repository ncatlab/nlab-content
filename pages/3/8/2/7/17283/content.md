
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _commutative Hopf algebroid_ is a [[Hopf algebroid]] where all multiplication operations (as opposed to the [[comultiplication]] operation) is required to be commutative. This concept is the [[formal dual]] to [[internal groupoids]] in the [[opposite category]] of [[CRing]].

A commutative Hopf algebroid is in particular a _[[Hopf algebroid over a commutative base]]_, but the latter may be more general.

Commutative Hopf algebroids appear prominently in [[stable homotopy theory]]/[[higher algebra]] as the [[dual Steenrod algebras]] of certain classes of [[multiplicative cohomology theory|multiplicative]] [[generalized homology theories]] $E$. As such they play a key role in the $E$-[[Adams spectral sequence]].

## Definition

### Commutative Hopf algebroids

+-- {: .num_defn #CommutativeHopfAlgebroid}
###### Definition

A **[[commutative Hopf algebroid]]** is an [[internal groupoid]] in the [[opposite category]] [[CRing]]${}^{op}$ of [[commutative rings]], regarded with its [[cartesian monoidal category]] structure.

=--

(e.g. [Ravenel 86, def. A1.1.1](#Ravenel86))

+-- {: .num_remark #CommutativeHopfAlgebroidSpelledOut}
###### Remark

We unwind def. \ref{CommutativeHopfAlgebroid}.  For $R \in CRing$, write $Spec(R)$ for same same object, but regarded as an object in $CRing^{op}$. 

An [[internal category]] in $CRing^{op}$ is a [[diagram]] in $CRing^{op}$ of the form

$$
  \array{
    Spec(\Gamma) \underset{Spec(A)}{\times} Spec(\Gamma)
    \\
    \downarrow^{\mathrlap{\circ}}
    \\
    Spec(\Gamma)
    \\
    {}^{\mathllap{s}}\downarrow \; \uparrow^{\mathrlap{i}} \downarrow^{\mathrlap{t}}
    \\
    Spec(A)
  }
  \,,
$$

(where the [[fiber product]] at the top is over $s$ on the left and $t$ on the right) such that the pairing $\circ$ defines an [[associativity law|associative]] [[composition]] over $Spec(A)$, [[unitality|unital]] with respect to $i$. This is an [[internal groupoid]] if it is furthemore equipped with a morphism

$$
  inv \;\colon\; Spec(\Gamma) \longrightarrow Spec(\Gamma)
$$

acting as assigning [[inverses]] with respect to $\circ$.

The key basic fact to use now is that [[tensor product]] of commutative rings exhibits the [[cartesian monoidal category]] structure on $CRing^{op}$, see at _[CRing -- Properties -- Cocartesian comonoidal structure](CRing#CocartesianComnonoidalStructure)_:

$$
  Spec(R_1) \underset{Spec(R_3)}{\times} Spec(R_2) 
  \simeq
  Spec(R_1 \otimes_{R_3} R_2)
  \,.
$$

This means that the above is equivalently a diagram in [[CRing]] of the form

$$
  \array{
    \Gamma \underset{A}{\otimes} \Gamma
    \\
    \uparrow^{\mathrlap{\Psi}}
    \\
    \Gamma 
    \\
    {}^{\mathllap{\eta_L}}\uparrow 
    \downarrow^{\mathrlap{\epsilon}} \;
    \uparrow^{\mathrlap{\eta_R}}
    \\
    A
  }
$$

as well as

$$
  c \; \colon \; \Gamma \longrightarrow \Gamma
$$

and satisfying [[formal duality|formally dual]] conditions, spelled out as def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents} below. Here 

* $\eta_L, \eta_R$ are called the left and right _[[unit]] maps_;

* $\epsilon$ is called the _co-unit_;

* $\Psi$ is called the _[[comultiplication]]_;

* $c$ is called the _[[antipode]]_ or _conjugation_



=--

+-- {: .num_remark #HopfAlgebrasAsHopfAlgebroids}
###### Remark

Generally, in a commutative Hopf algebroid, def. \ref{CommutativeHopfAlgebroid}, the two morphisms $\eta_L, \eta_R\colon A \to \Gamma$ from remark \ref{CommutativeHopfAlgebroidSpelledOut} need not coincide, they make $\Gamma$ genuinely into a [[bimodule]] over $A$, and it is the [[tensor product]] of [[bimodules]] that appears in remark \ref{CommutativeHopfAlgebroidSpelledOut}. But it may happen that they coincide:

An [[internal groupoid]] $\mathcal{G}_1 \stackrel{\overset{s}{\longrightarrow}}{\underset{t}{\longrightarrow}}$ for which the [[domain]] and [[codomain]] morphisms coincide, $s = t$, is euqivalently a [[group object]] in the [[slice category]] over $\mathcal{G}_0$.

Dually, a [[commutative Hopf algebroid]] $\Gamma \stackrel{\overset{\eta_L}{\longleftarrow}}{\underset{\eta_R}{\longleftarrow}} A$ for which $\eta_L$ and $\eta_R$ happen to coincide is equivalently a **commutative [[Hopf algebra]]** $\Gamma$ over $A$.

=--

Writing out the formally dual axioms of an [[internal groupoid]] as in remark \ref{CommutativeHopfAlgebroidSpelledOut} yields the following equivalent but maybe more explicit definition of commutative Hopf algebroids, def. \ref{CommutativeHopfAlgebroid}

+-- {: .num_defn #CommutativeHopfAlgebroidDefinitionInExplicitComponents}
###### Definition

A **[[commutative Hopf algebroid]]** is

1. two [[commutative rings]], $A$ and $\Gamma$;

1. ring [[homomorphisms]]

   1. (left/right unit) 
  
      $\eta_L,\eta_R \colon A \longrightarrow \Gamma$; 

   1. (comultiplication) 
 
      $\Psi \colon \Gamma \longrightarrow \Gamma \underset{A}{\otimes} \Gamma$;

   1. (counit) 
 
      $\epsilon \colon \Gamma \longrightarrow A$;

   1. (conjugation) 

      $c \colon \Gamma \longrightarrow \Gamma$

such that

1. (co-[[unitality]])

   1. (identity morphisms respect source and target) 

      $\epsilon \circ \eta_L = \epsilon \circ \eta_R = id_A$;

   1. (identity morphisms are units for composition) 

      $(id_\Gamma \otimes_A \epsilon) \circ \Psi  = (\epsilon \otimes_A id_\Gamma) \circ \Psi = id_\Gamma$;

   1. (composition respects source and target) 

      1. $\Psi \circ \eta_R = (id \otimes_A \eta_R) \circ \eta_R$;

      1. $\Psi \circ \eta_L = (\eta_L \otimes_A id) \circ \eta_L$

1. (co-[[associativity]]) $(id_\Gamma \otimes_A \Psi) \circ \Psi = (\Psi \otimes_A id_\Gamma) \circ \Psi$;

1. ([[inverses]])

   1. (inverting twice is the identity) 

      $c \circ c = id_\Gamma$;

   1. (inversion swaps source and target) 

      $c \circ \eta_L = \eta_R$; $c \circ \eta_R = \eta_L$;

   1. (inverse morphisms are indeed left and right inverses for composition) 

      the morphisms $\alpha$ and $\beta$ induced via the [[coequalizer]] property of the [[tensor product]] from $(-) \cdot c(-)$ and $c(-)\cdot (-)$, respectively

      $$
        \array{
          \Gamma \otimes A \otimes \Gamma
            &
            \underoverset
              {\longrightarrow}
              {\longrightarrow}
              {}
            &
          \Gamma \otimes \Gamma
             &
             \overset{coeq}{\longrightarrow}
             &
          \Gamma \otimes_A \Gamma
           \\
           &&
           {}_{\mathllap{(-)\cdot c(-)}}\downarrow 
           & 
            \swarrow_{\mathrlap{\alpha}}
           \\
           && \Gamma
        }
      $$

      and

      $$
        \array{
          \Gamma \otimes A \otimes \Gamma
            &
            \underoverset
              {\longrightarrow}
              {\longrightarrow}
              {}
            &
          \Gamma \otimes \Gamma
             &
             \overset{coeq}{\longrightarrow}
             &
          \Gamma \otimes_A \Gamma
           \\
           &&
           {}_{\mathllap{c(-)\cdot (-)}}\downarrow 
           & 
            \swarrow_{\mathrlap{\beta}}
           \\
           && \Gamma
        }
      $$

      satisfy 

      $\alpha \circ \Psi = \eta_L \circ \epsilon $

      and

      $\beta \circ \Psi = \eta_R \circ \epsilon $.
   
=--

e.g. ([Ravenel 86, def. A1.1.1](#Ravenel86))


### Comodules

+-- {: .num_defn #HopfComoduleRing}
###### Definition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$ as in def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}, hence an [[internal groupoid]] in $CRing^{op}$, then a **comodule ring** over it is an [[action]] in $CRing^{op}$ of that internal groupoid.

=--

In the same spirit, a **[[comodule]]** over a commutative Hopf algebroid (not necessarily a comodule ring) is a [[quasicoherent sheaf]] on the corresponding [[internal groupoid]] (regarded as a ([[algebraic stack|algebraic]]) [[stack]]) (e.g. [Hopkins 99, prop. 11.6](#Hopkins99)). Explicitly in components:

+-- {: .num_defn #CommutativeHopfAlgebroidComodule}
###### Definition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents},
then a **left [[comodule]]** over $\Gamma$ is

1. an $A$-[[module]] $N$;

1. an $A$-[[module]] [[homomorphism]] (co-action)

   $\Psi_N \;\colon\; N \longrightarrow \Gamma \otimes_A N$;

such that

1. (co-[[unitality]])

   $(\epsilon \otimes_A id_N) \circ \Psi_N = id_N$;

1. (co-action property)

   $(\Psi \otimes_A id_N) \circ \Psi_N = (id_\Gamma \otimes_A \Psi_N)\circ \Psi_N$.

A [[homomorphism]] between comodules $N_1 \to N_2$ is a homomorphism of underlying $A$-modules making [[commuting diagrams]] with the co-action morphism. Write

$$
  \Gamma CoMod
$$

for the resulting [[category]] of (left) comodules over $\Gamma$. Analogously there are right comodules.

=--

+-- {: .num_example #ComoduleStructureOnGroundRing}
###### Example

For $(\Gamma,A)$ a [[commutative Hopf algebroid]], then $A$ becomes a left $\Gamma$-comodule (def. \ref{CommutativeHopfAlgebroidComodule}) with coaction given by the right unit

$$
  A \overset{\eta_R}{\longrightarrow} \Gamma \simeq \Gamma \otimes_A A
  \,.
$$

=--

+-- {: .proof}
###### Proof

The required co-unitality property is the dual condition in def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}

$$
  \epsilon \circ \eta_R  = id_A
$$

of the fact in def. \ref{CommutativeHopfAlgebroid} that identity morphisms respect sources:

$$
  id
    \;\colon\;
  A 
    \overset{\eta_R}{\longrightarrow} 
  \Gamma
    \simeq
  \Gamma \otimes_A A
    \overset{\epsilon \otimes_A id}{\longrightarrow}
  A \otimes_A A
    \simeq
  A
$$

The required co-action property is the dual condition 

$$
  \Psi \circ \eta_R = (id \otimes_A \eta_R) \circ \eta_R
$$ 

of the fact in def. \ref{CommutativeHopfAlgebroid} that composition of morphisms in a groupoid respects sources

$$
  \array{
    A 
      &\overset{\eta_R}{\longrightarrow}&
    \Gamma
    \\
    {}^{\mathllap{\eta_R}}\downarrow
      &&
    \downarrow^{\mathrlap{\Psi}}
    \\
    \Gamma \simeq \Gamma \otimes_A A
      &\underset{id \otimes_A \eta_R}{\longrightarrow}&
    \Gamma \otimes_A \Gamma
  }
  \,.
$$


=--


## Properties

### Co-free Comodules

+-- {: .num_prop #CoFreeComodules}
###### Proposition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, there is a [[free-forgetful adjunction]]

$$
  \Gamma CoMod
   \underoverset
     {\underset{forget}{\longrightarrow}}
     {\overset{co-free}{\longleftarrow}}
     {\bot}
  A Mod
$$

between the [[category]] of $\Gamma$-[[comodules]], def. \ref{CommutativeHopfAlgebroidComodule} and the [[category of modules]] over $A$, where the [[cofree functor]] is [[right adjoint]]. 

The co-free $\Gamma$-[[comodule]] on an $A$-module $N$ is $\Gamma \otimes_A N$ equipped with the [[coaction]] induced by the [[comultiplication]] $\Psi$ in $\Gamma$.

=--

The proof is [[formal dual|formally dual]] to the characterization of [[free modules]], but we spell it out for completenss:


+-- {: .proof}
###### Proof


A homomorphism into a co-free $\Gamma$-comodule is a morphism of $A$-modules of the form

$$
  f \;\colon\; N \longrightarrow \Gamma \otimes_A C
$$

making the following [[commuting diagram|diagram commute]]

$$
  \array{
    N &\overset{f}{\longrightarrow}& \Gamma \otimes_A C
    \\
    {}^{\mathllap{\Psi_N}}\downarrow 
      &&
    \downarrow^{\mathrlap{\Psi \otimes_A id}}
    \\
    \Gamma \otimes_A N
      &\underset{id \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A \Gamma \otimes_A C
  }
  \,.
$$

Consider the composite

$$
  \tilde f
  \;\colon\;
  N 
    \overset{f}{\longrightarrow}
  \Gamma \otimes_A C
    \overset{\epsilon \otimes_A id}{\longrightarrow}
  A \otimes_A C
    \simeq
  C
  \,,
$$

i.e. the "corestriction" of $f$ along the counit of $\Gamma$. By definition this makes the following square commute

$$
  \array{
    \Gamma \otimes_A N 
      &\overset{id \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A \Gamma \otimes_A C
    \\
    {}^{\mathllap{=}}\downarrow
      &&
    \downarrow^{\mathrlap{id \otimes_A \epsilon \otimes_A id}}
    \\
    \Gamma \otimes_A N
      &\underset{id \otimes_A \tilde f}{\longrightarrow}&
    \Gamma \otimes_A C
  }
  \,.
$$

Pasting this square onto the bottom of the previous one yields

$$
  \array{
    N &\overset{f}{\longrightarrow}& \Gamma \otimes_A C
    \\
    {}^{\mathllap{\Psi_N}}\downarrow 
      &&
    \downarrow^{\mathrlap{\Psi \otimes_A id}}
    \\
    \Gamma \otimes_A N
      &\underset{id \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A \Gamma \otimes_A C
    \\
    {}^{\mathllap{=}}\downarrow
      &&
    \downarrow^{\mathrlap{id \otimes_A \epsilon \otimes_A id}}
    \\
    \Gamma \otimes_A N
      &\underset{id \otimes_A \tilde f}{\longrightarrow}&
    \Gamma \otimes_A C
  }
  \,.
$$

Now due to co-unitality, the right right vertical composite is the identity on $\Gamma \otimes_A C$. But this means by the commutativity of the outer rectangle that $f$ is uniquely fixed in terms of $\tilde f$ by the relation

$$
  f = (id \otimes_A f) \circ \Psi
  \,.
$$

This establishes a [[natural bijection]] 

$$
  \frac{
    N \overset{f}{\longrightarrow} \Gamma \otimes_A C
  }{
    N \overset{\tilde f}{\longrightarrow} C
  }
$$

and hence the adjunction in question.



=--


### Cotensor product of comodules

+-- {: .num_prop #LeftComodulesToRightComodules}
###### Proposition

Consider a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}.
Any left comodule $N$ over $\Gamma$ (def. \ref{CommutativeHopfAlgebroidComodule}) becomes a right comodule via the coaction

$$
  N
    \overset{\Psi}{\longrightarrow}
  \Gamma \otimes_A N
    \overset{\simeq}{\longrightarrow}
  N \otimes_A \Gamma
    \overset{id \otimes_A c}{\longrightarrow}
  N \otimes_A \Gamma
  \,,
$$

where the isomorphism in the middle the is [[braiding]] in $A Mod$ and where $c$ is the conjugation map of $\Gamma$.

Dually, a right comodule $N$ becoomes a left comodule with the coaction

$$
  N
    \overset{\Psi}{\longrightarrow}
  N \otimes_A \Gamma
    \overset{\simeq}{\longrightarrow}
  \Gamma \otimes_A N
    \overset{c \otimes_A id}{\longrightarrow}
  \Gamma \otimes_A N
  \,.
$$



=--


+-- {: .num_defn #CotensorProductOfComodules}
###### Definition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents},
and given $N_1$ a right $\Gamma$-comodule and $N_2$ a left comodule (def. \ref{CommutativeHopfAlgebroidComodule}), then their **[[cotensor product]]** $N_1 \Box_\Gamma N_2$ is the [[kernel]] of the difference of the two coaction morphisms:

$$
  N_1 \Box_\Gamma N_2
    \;\coloneqq\;
  ker
  \left(
    N_1 \otimes_A N_2
    \overset{\Psi_{N_1}\otimes_{A} id - id \otimes_A \Psi_{N_2} }{\longrightarrow}
    N_1 \otimes_A \Gamma \otimes_A N_2
  \right)
  \,.
$$

If both $N_1$ and $N_2$ are left comodules, then their cotensor product is the cotensor product of $N_2$ with $N_1$ regarded as a right comodule via prop. \ref{LeftComodulesToRightComodules}.

=--

e.g. ([Ravenel 86, def. A1.1.4](#Ravenel86)).

+-- {: .num_prop}
###### Proposition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents},
and given $N_1, N_2$ two left $\Gamma$-comodules (def. \ref{CommutativeHopfAlgebroidComodule}), then their [[cotensor product]] (def. \ref{CotensorProductOfComodules}) is commutative, in that there is an [[isomorphism]]

$$
  N_1 \Box N_2 \;\simeq\; N_2 \Box N_1
  \,.
$$

=--

(e.g. [Ravenel 86, prop. A1.1.5](#Ravenel86)) 

+-- {: .num_lemma #ComoduleHomInTermsOfCotensorProduct}
###### Lemma

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents},
and given $N_1, N_2$ two left $\Gamma$-comodules (def. \ref{CommutativeHopfAlgebroidComodule}), such that $N_1$ is [[projective module|projective]] as an $A$-[[module]], then

1. The morphism

   $$
      Hom_A(N_1, A)
       \overset{f \mapsto (id \otimes_A f) \circ \Psi_{N_1}}{\longrightarrow}
      Hom_A(N_1, \Gamma \otimes_A A)
       \simeq
      Hom_A(N_1, \Gamma)
       \simeq
      Hom_A(N_1, A) \otimes_A \Gamma
   $$
 
   gives $Hom_A(N_1,A)$ the structure of a right $\Gamma$-comodule;

1. The [[cotensor product]] (def. \ref{CotensorProductOfComodules}) with respect to this right comodule structure is isomorphic to the hom of $\Gamma$-comodules:

   $$
     Hom_A(N_1, A) \Box_\Gamma N_2
     \simeq
     Hom_\Gamma(N_1, N_2)
     \,.
   $$

   Hence in particular

   $$
     A \Box_\Gamma N_2 
      \;\simeq\;
     Hom_\Gamma(A,N_2)
   $$

=--

(e.g. [Ravenel 86, lemma A1.1.6](#Ravenel86))

+-- {: .num_remark}
###### Remark

In computing the second page of $E$-[[Adams spectral sequences]], the second statement in lemma \ref{ComoduleHomInTermsOfCotensorProduct} is the key translation that makes the comodule [[Ext]]-groups on the page be equivalent to a [[Cotor]]-groups. The latter lend themselves to computation, for instance via [[Lambda-algebra]] or via the [[May spectral sequence]].

=--





### Homological algebra of comodules
 {#HomologicalAlgebraOfHopfComodules}

We discuss aspects of the [[homological algebra]] in [[categories]] of comodules over commutative Hopf algebroids, def. \ref{CommutativeHopfAlgebroidComodule}.

+-- {: .num_prop #CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}
###### Proposition

If a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents} is such that $\eta_L, \eta_R \colon A \longrightarrow \Gamma$ is a [[flat morphism]], then the [[category]] $\Gamma CoMod$ of [[comodules]] over $\Gamma$, def. \ref{CommutativeHopfAlgebroidComodule}, is an [[abelian category]].

=--

(e.g. [Ravenel 86, theorem A1.1.3](#Ravenel86)) 

+-- {: .proof}
###### Proof

It is clear that, without any condition the Hopf algebroid, $\Gamma CoMod$ is an [[additive category]]. 

We need to show that with the assumption that $\Gamma$ is flat over $A$, then this is also a [[pre-abelian category]] in that [[kernels]] and [[cokernels]] exist. Let $f \colon (N_1,\Psi_{N_1}) \longrightarrow (N_2,\Psi_{N_2})$ be a morphism of comodules, hence a [[commuting diagram]] in $A$[[Mod]] of the form

$$
  \array{
    N_1 &\stackrel{f}{\longrightarrow}& N_2
    \\
    \downarrow^{\mathrlap{\Psi_{N_1}}} && \downarrow^{\mathrlap{\Psi_{N_2}}}
    \\
    \Gamma \otimes_A N_1
    &\stackrel{id_\Gamma \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A N_2
  }
  \,.
$$

Consider the kernel $ker(f)$ of $f$ in $A$[[Mod]] and its image under $\Gamma \otimes_A (-)$

$$
  \array{
    ker(f) &\longrightarrow& N_1 &\stackrel{f}{\longrightarrow}& N_2
    \\
    \downarrow && \downarrow^{\mathrlap{\Psi_{N_1}}} && \downarrow^{\mathrlap{\Psi_{N_2}}}
    \\
    \Gamma \otimes_A ker(f) 
      &\longrightarrow& 
    \Gamma \otimes_A N_1
      &\stackrel{id_\Gamma \otimes_A f}{\longrightarrow}&
    \Gamma \otimes_A N_2
  }
  \,.
$$

By the assumption that $\Gamma$ is a [[flat module]] over $A$, also $\Gamma \otimes_A ker(f) \simeq ker(\Gamma \otimes_A f)$ is a [[kernel]]. By its [[universal property]] this induces uniquely a morphism as shown on the left, making the above [[commuting diagram|diagram commute]]. This means that the $A$-module $ker(f)$ uniquely inherits the structure of a $\Gamma$-comodule such as to make $ker(f) \to N_1$ a comodule homomorphism. By the same universal property it follows that $ker(f)$ with this comodule structure is in fact the kernel of $f$ in $\Gamma CoMod$.

The argument for the existence of [[cokernels]] proceeds [[formal dual|formally dually]]. Therefore it follows that the comparison morphism

$$
  coker(ker(f)) \longrightarrow ker(coker(f))
$$

formed in $\Gamma CoMod$ has underlying it the corresponding comparison morphism in $A Mod$. There this is an [[isomorphism]], hence it is an isomorphism also in $\Gamma CoMod$, and so the latter is not just a [[pre-abelian category]] but in fact an [[abelian category]] itself.

=--

+-- {: .num_prop #CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}
###### Proposition

If a [[commutative Hopf algebroid]] $\Gamma$ over $A$, def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents} is such that $\eta_L, \eta_R \colon A \longrightarrow \Gamma$ is a [[flat morphism]], then 

1. every co-free $\Gamma$-[[comodule]], def. \ref{CoFreeComodules}, on an [[injective module]] over $A$ is an [[injective object]] in $\Gamma CoMod$;

1. $\Gamma CoMod$ has [[enough injectives]] (if the [[axiom of choice]] holds in the ambient [[set theory]]).

=--

(e.g. [Ravenel 86, lemma A1.2.2](#Ravenel86))

+-- {: .proof}
###### Proof

First of all, assuming the [[axiom of choice]], then the [[category of modules]] $A Mod$ has [[enough injectives]] (see [this proposition](injective+object#AbHasEnoughInjectives)).
Now by prop. \ref{CoFreeComodules} we have the [[adjunction]]

$$
  \Gamma CoMod
   \underoverset
     {\underset{forget}{\longrightarrow}}
     {\overset{co-free}{\longleftarrow}}
     {\bot}
  A Mod
 \,.
$$

Observe that the [[left adjoint]] is a [[faithful functor]] (being a [[forgetful functor]]) and that, by the proof of prop. \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat}, it is an [[exact functor]]. With this a standard lemma applies ([here](injective+object#TransferOfEnoughInjectivesAlongAdjunctions)) which says that

1. with $I \in A Mod$ an [[injective module]], then the co-free comodule $\Gamma \otimes_A I$ is an [[injective object]] in $\Gamma CoMod$;

1. for $N \in \Gamma CoMod$ any object, and for $i \colon U(N) \hookrightarrow I$ a monomorphism of $A$-modules into an injective $A$-module, then the [[adjunct]] $\tilde i \colon N \hookrightarrow \Gamma\otimes_A I$ is a monomorphism in $\Gamma CoMod$ (and into an injective comodule).

=--


+-- {: .num_prop #CoFreeHopfComodulesAreHomNAcyclicForProjectiveN}
###### Proposition

Let $\Gamma$ be a [[commutative Hopf algebroid]] over $A$, def. \ref{CommutativeHopfAlgebroid}, \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}, such that $\eta_L, \eta_R \colon A \longrightarrow \Gamma$ is a [[flat morphism]], 
Let $N \in \Gamma CoMod$ be a Hopf [[comodule]], def. \ref{CommutativeHopfAlgebroidComodule}, such that the underlying $A$-module is a [[projective module]] (a [[projective object]] in $A$[[Mod]]). 

Then  (assuming the [[axiom of choice]]) every co-free commodule, prop. \ref{CoFreeComodules}, is an $F$-[[acyclic object]] for $F$ the [[hom functor]] $Hom_{\Gamma CoMod}(N,-)$.

=--

+-- {: .proof}
###### Proof

We need to show that the [[derived functors in homological algebra|derived functors]] $R^{\bullet} Hom_{\Gamma}(N,-)$ vanish in positive degree on all co-free comodules, hence on $\Gamma \otimes_A K$, for $K \in A Mod$. 

To that end, let $I^\bullet$ be an [[injective resolution]] of $K$ in $A Mod$. By prop. \ref{CategoryOfHopfComodulesIsAbelianIfHopfAlgebroidIsFlat} then $\Gamma \otimes_A I^\bullet$ is a sequence of [[injective objects]] in $\Gamma CoMod$ and by the assumption that $\Gamma$ is flat over $A$ it is an [[injective resolution]] of $\Gamma \otimes_A K$ in $\Gamma CoMod$. Therefore the derived functor in question is given by

$$
  \begin{aligned}
    R^{\bullet \geq 1} Hom_\Gamma(N, \Gamma \otimes_A K)
    & \simeq
    H_{\bullet \geq 1}( Hom_\Gamma( N, \Gamma \otimes_A I^\bullet ) )
    \\
    & \simeq H_{\bullet \geq 1}( Hom_A(N, I^\bullet) )
    \\
    & \simeq 0
  \end{aligned}
  \,.
$$

Here the second equivalence is the cofree/forgetful adjunction isomorphism of prop. \ref{CoFreeComodules}, while the last equality then follows from the assumption that the $A$-module underlying $N$ is a [[projective module]] (since [[hom functors]] out of [[projective objects]] are [[exact functors]] ([here](projective+object#EquivalenceOfDefinitionsInAbelian)) and since derived functors of exact functors vanish in positive degree ([here](derived+functor+in+homological+algebra#DerivedFunctorOfExactFunctor))).


=--

+-- {: .num_remark}
###### Remark

In the application to Hopf algebroids induced from [[commutative ring spectra]] $E$ ([below](#FromRingSpectra)), lemma \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} is the key statement that identifies the entries of the second page of the $E$-[[Adams spectral sequence]] with [[Ext]]-groups of Hof comodules. See at _[Adams spectral sequence -- The second page](Adams+spectral+sequence#TheE2TermOfTheEAdamsSpectralSequence)_.

=--


### Ext-groups 


+-- {: .num_lemma #CoModuleExtFromAToAForPrimitivelyGeneratedExteriorAlgebra}
###### Lemma

If $(\Gamma,A)$ graded commutative Hopf algebra such that 

1. the underlying algebra is free graded commutative;

1. $\eta \colon A \to \Gamma$ is a [[flat morphism]];

1. $\Gamma$ is generated by [[primitive elements]] $\{x_i\}_{i\in I}$

then the [[Ext]] of $\Gamma$-comodules from $A$ and itself is the (graded) polynomial algbra on these generators:

$$
  Ext_\Gamma(A,A) \simeq A[\{x_i\}_{i \in I}]
  \,.
$$


=--

([Ravenel 86, lemma 3.1.9](#Ravenel86), [Kochman 96, prop. 3.7.5](#Kochman96))

+-- {: .proof}
###### Proof

Consider the co-free left $\Gamma$-comodule ([prop.](commutative+Hopf+algebroid#CoFreeComodules))

$$
  \Gamma \otimes_A A[\{y_i\}_{i \in I}] 
$$

and regard it as a [[chain complex]] of left comodules by defining a [[differential]] via

$$
  d \colon x_i \mapsto y_i
$$

$$
  d \colon y_i \mapsto 0
$$

and extending as a graded [[derivation]]. 

We claim that $d$ is a homomorphism of left comodules: Due to the assumption that all the $x_i$ are primitive we have on generators that

$$
  \begin{aligned}
    (id,d) ( \Psi(x_i)  )
    & =
    (id,d) ( x_i \otimes 1 + 1 \otimes x_i )
    \\
    & =
    \underset{= 0}{x_i  \otimes \underbrace{(d 1)} }
     + 
    \underset{= y_i}{ 1 \otimes \underbrace{(d x_i)} } 
    \\
    & =
    \Psi( d x_i )
  \end{aligned}
$$

and 

$$
  \begin{aligned}
    (id,d)( \Psi(y_i) )
    & =
    (id,d) ( 1, y_i )
    \\
    & =
    (1, d y_i)
    \\
    & =
    0
    \\
    & =
    \Psi( 0 )
    \\
    & =
    \Psi(d y_i)
  \end{aligned}
  \,.
$$

Since $d$ is a graded derivation on a free graded commutative algbra, and $\Psi$ is an algebra homomorphism, this implies the statement for all other elements.

Now observe that the canonical [[chain map]]

$$
  (\Gamma \otimes_A A[\{y_i\}_{i \in I}]  ,\; d)
    \overset{\simeq_{qi}}{\longrightarrow}
  A
$$

(which projects out the generators $x_i$ and $y_i$ and is the identity on $A$), is a [[quasi-isomorphism]], by construction. Therefore it constitutes a co-free resolution of $A$ in left $\Gamma$-comodules.

Since the counit $\eta$ is assumed to be flat, and since $A$ is trivially a [[projective module]] over itself, prop. \ref{CoFreeHopfComodulesAreHomNAcyclicForProjectiveN} now implies that the above is an [[acyclic resolution]] with respect to the functor $Hom_{\Gamma}(A,-) \colon \Gamma CoMod \longrightarrow A Mod$. Therefore it computes the [[Ext]]-functor. Using that forming co-free comodules is [[right adjoint]] to forgetting $\Gamma$-comodule structure over $A$ ([prop.](commutative+Hopf+algebroid#CoFreeComodules)), this yields:

$$
  \begin{aligned}
    Ext^\bullet_\Gamma(A,A)
    & \simeq
    H_\bullet(Hom_\Gamma(A,  \Gamma \otimes_A A[\{y_i\}_{i \in I}] ), d)
    \\
    & \simeq 
    H_\bullet(Hom_A(A,  A[\{y_i\}_{i \in I}] ), d= 0 )
    \\
    & \simeq
    Hom_A(A,  A[\{y_i\}_{i \in I}] )
    \\
    & \simeq
    A[\{y_i\}_{i \in I}]
  \end{aligned}
  \,.
$$

=--


## Examples

### From ring spectra
 {#FromRingSpectra}

The [[cosimplicial object|cosimplicial]] spectra of certain [[commutative ring spectra]] $E$ (their [[Amitsur complexes]]) yield commutative Hopf algebroids when truncated. The Hopf algebroids appearing this way govern the corresponding $E$-[[Adams spectral sequences]].

+-- {: .num_defn #FlatE}
###### Definition

Call a [[commutative ring spectrum]] $E$ _flat_ if one, equivalently both, of the morphisms

$$
  \eta_L \coloneqq \pi_\bullet(e \wedge id) 
  \;\colon\; 
  E_\bullet \longrightarrow E_\bullet(E)
$$

$$
  \eta_r 
  \;\coloneqq\; 
  \pi_\bullet(id \wedge e) \colon E_\bullet \longrightarrow E_\bullet(E)
$$

is a [[flat morphism]].

=--

+-- {: .num_example }
###### Example

Examples of ring spectra that are flat according to def. \ref{FlatE} include
$E = $

* [[sphere spectrum|S]], 

* [[HR]] for $R = \mathbb{F}_p$ a [[prime field]],

* [[MO]], [[MU]], [[MSp]], 

* [[KO]], [[KU]].


=--

+-- {: .num_example}
###### Example

Examples of ring spectra that are _not_ flat in the sense of def. \ref{FlatE} include [[HA|H]][[integers|Z]], and $M S U$.

=--


The key consequence of the assumption that $E$ is flat in the sense of def. \ref{FlatE} is the following.

+-- {: .num_prop #FlatnessOfEImpliesKeyConsequence}
###### Proposition

If $E$ is flat, def. \ref{FlatE}, then for all spectra $X$ there is a [[natural isomorphisms]]

$$
  E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
    \stackrel{}{\longrightarrow}
  \pi_\bullet(E \wedge E \wedge X)
$$

and hence for all $n \in \mathbb{N}$ there are isomorphisms

$$
  \pi_\bullet(E^{\wedge^{(n+2)}}\wedge X  )
    \simeq
  \underset{n+1\,factors}{
  \underbrace{E_\bullet(E)
    \otimes_{\pi_\bullet(E)}
    \cdots
    \otimes_{\pi_\bullet(E)}
  E_\bullet(E)
  }}
    \otimes_{\pi_\bullet(E)}
  E_\bullet(X)
  \,.
$$


=--

(e.g. [Adams 96, part III, lemma 12.5](#Adams96), [Schwede 12, prop. 6.20](#Schwede12))

+-- {: .proof}
###### Proof

The desired natural homomorphism

$$
  E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
  \longrightarrow
  \pi_\bullet(E \wedge E \wedge X)
$$

is given on $[\alpha] \in \pi_\bullet(E \wedge E)$ and $[\beta] \in \pi_\bullet(E \wedge X)$ by $([\alpha, \beta])\mapsto [(id \wedge \mu \wedge id) \circ (\alpha \wedge \beta)]$.

To see that this is an isomorphism, observe that by flatness of $E$, the assignment $X \mapsto E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(-)$ is a [[generalized homology]] functor, hence [[Brown representability theorem|represented]] by some spectrum. The above morphism, natural in $X$, thus constitutes a homomorphism  of generalized homology theories, and so for these to be equivalent it is sufficient to check that they induce isomorphisms on the point. This is manifestly the case.

Finally we get the claimed isomorphisms for all $n$ by [[induction]]:

$$
  \begin{aligned}
    \pi_\bullet(E^{\wedge^{n+2}} \wedge X)
    & \simeq
    \pi_\bullet(E \wedge E \wedge E^{\wedge^n} \wedge X))
    \\
    &\simeq 
     E_\bullet(E) 
         \otimes_{\pi_\bullet(E)} 
     E_\bullet( E^{\wedge^n} \wedge X )
     \\
     & = 
     E_\bullet(E) 
         \otimes_{\pi_\bullet(E)} 
     \pi_\bullet( E^{\wedge^{n+1}} \wedge X )       
  \end{aligned}
  \,.
$$

=--

Now we may identify the commutative Hopf algebroids arising from flat commutative ring spectra.

+-- {: .num_prop #HopfAlgebroidStructureOnDualEOperations}
###### Proposition

If a [[commutative ring spectrum]] $E$ is flat according to def. \ref{FlatE}, then, via the isomorphism of proposition \ref{FlatnessOfEImpliesKeyConsequence}, the cosimplicial spectrum $E^{\wedge^\bullet} \wedge X$ (the $E$-standard resolution of $X$ from example \ref{StandardEResolution}) exhibits:

1. for $X = E$: [[Hopf algebroid]]-structure, def. \ref{CommutativeHopfAlgebroid}, remark \ref{CommutativeHopfAlgebroidSpelledOut}, on $E_\bullet(E)$ over $\pi_\bullet(E)$ -- called the **dual $E$-[[Steenrod algebra]]**;

1. for general $X$: [[comodule]]-structure on $E_\bullet(X)$ over the dual $E$-[[Steenrod algebra]].

=--

(e.g. [Baker-Lazarev 01, theorem 1.1](#BakerLazarev01))

+-- {: .proof}
###### Proof

Via prop. \ref{FlatnessOfEImpliesKeyConsequence}, the image under $\pi_\bullet(-)$ of the cosimplicial spectrum $E^{\wedge^\bullet}(E)$ is identified as on the right of the following diagram

$$
  \array{
    \pi_\bullet(E\wedge E \wedge E) &\simeq& E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(E)
    \\
    \uparrow^{\mathrlap{\pi_\bullet(id \wedge e \wedge id)}}
    &&
    \uparrow^{\mathrlap{\Psi}}
    \\
    \pi_\bullet(E \wedge E) &=& E_\bullet(E)
    \\
    {}^{\mathllap{\pi_\bullet(e \wedge id)}}\uparrow
     \downarrow^{\mathrlap{\pi_\bullet(\mu)}}
     \;\;\;\;\;\;
     \uparrow^{\mathrlap{\pi_\bullet(id \wedge e)}}
     &&
     {}^{\mathllap{\eta_L}}\uparrow 
     \downarrow^{\mathrlap{\epsilon}} 
     \uparrow^{\mathrlap{\eta_R}}
    \\
    \pi_\bullet(E) &=& \pi_\bullet(E)
  }
  \,.
$$

Analogously the [[coaction]] is induced as on the right of the following diagram

$$
  \array{
    \pi_\bullet(E\wedge E \wedge X) &\simeq& E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(X)
    \\
    \uparrow^{\mathrlap{\pi_\bullet(id \wedge e \wedge id)}}
    &&
    \uparrow^{\mathrlap{\Psi_X}}
    \\
    \pi_\bullet(E \wedge X) &=& E_\bullet(X)
  }
  \,.
$$

=--


+-- {: .num_example}
###### Example

Examples of [[commutative ring spectra]] $E$ for which the dual $E$-[[Steenrod algebra]] $E_\bullet(E)$ over $\pi_\bullet(E)$ of corollary \ref{HopfAlgebroidStructureOnDualEOperations} happens to be a [[commutative Hopf algebra]] over $\pi_\bullet(E)$ instead of a more general [[commutative Hopf algebroid]], according to remark \ref{HopfAlgebrasAsHopfAlgebroids}, includes the cases

$E = $

* [[HA|H]]$\mathbb{F}_p$,

* ...

=--

The key use of the Hopf coalgebroid structure of prop. \ref{HopfAlgebroidStructureOnDualEOperations} for the purpose of the $E$-[[Adams spectral sequence]] is that it is extra structure inherited from maps of spectra under smashing with $E$:

+-- {: .num_example #SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms}
###### Example

For $Y,N$ any two [[spectra]], the morphism (of $\mathbb{Z}$-[[graded abelian groups]]) given by [[smash product of spectra|smash product]] with $E$

$$
  \pi_\bullet(E \wedge -)
    \;\colon\;
  \pi_\bullet([Y,N])
    \longrightarrow
  Hom^\bullet_{Ab}(E_\bullet(Y), E_\bullet(N))
$$

factors through $E_\bullet(E)$-[[comodule]] [[homomorphisms]] over the dual $E$-[[Steenrod algebra]]:

$$
  \pi_\bullet(E \wedge -)
    \;\colon\;
  \pi_\bullet([Y,N])
    \longrightarrow
  Hom^\bullet_{E_\bullet(E)}(E_\bullet(Y), E_\bullet(N))
    \longrightarrow
  Hom^\bullet_{Ab}(E_\bullet(Y), E_\bullet(N))
  \,.
$$

=--

In order to make use of this we need to invoke a [[universal coefficient theorem]] in the following form.

+-- {: .num_prop #AdamsUCT}
###### Proposition

If $E$ is among the examples [[sphere spectrum|S]], [[HR]] for $R = \mathbb{F}_p$, [[MO]], [[MU]], [[MSp]], [[KO]], [[KU]], then for all $E$-[[module spectra]] $N$ with [[action]] $\rho \colon E\wedge N \to N$
the morphism of $\mathbb{Z}$-[[graded abelian groups]]

$$
 \pi_\bullet[Y,N] 
   \stackrel{\phi \mapsto \rho \circ (id\wedge \phi)}{\longrightarrow}
  Hom_{\pi_\bullet(E)}^\bullet(E_\bullet(Y), \pi_\bullet N)_\bullet
$$

(from the [[stable homotopy group]] of the [[mapping spectrum]] to the [[hom-object|hom groups]] of $\pi_\bullet(E)$-[[modules]])

is an [[isomorphism]].


=--

This is the [[universal coefficient theorem]] of ([Adams 74, chapter III, prop. 13.5](#Adams74)), see also ([Schwede 12, chapter II, prop. 6.20](#Schwede12)).

With this we finally get the following statement, which serves to identity maps of certain spectra with their induced maps on $E$-homology:

+-- {: .num_prop}
###### Proposition

If the assumptions of prop. \ref{AdamsUCT} hold, then for $X,N$ any two [[spectra]], the morphism of $\mathbb{Z}$-[[graded abelian groups]] from example \ref{SmashingMapsWithEFactorsThroughSteenrodComoduleHomomorphisms} in the form

$$
 \pi_\bullet(E\wedge (-))
   \;\colon\;
 \pi_\bullet[Y, E\wedge N] 
   \stackrel{}{\longrightarrow}
  Hom_{E_\bullet(E)}^\bullet(E_\bullet(Y), E_\bullet(Y)))
$$

is an [[isomorphism]].

=-- 

([Adams 74, part III, page 323](#Adams74))


+-- {: .proof}
###### Proof

By the general formula for expressing [[adjuncts]], the morphism fits into the following [[commuting diagram]]

$$
  \array{
    [Y, E \wedge N]
      &\stackrel{\pi_\bullet(E\wedge(-))}{\longrightarrow}&
    Hom_{E_\bullet(E)}(
      E_\bullet(Y), 
      E_\bullet(E \wedge N)
    )
    \\
    {}^{\mathllap{{\phi \mapsto} \atop {\mu \circ (id \wedge \phi)}}}
      \downarrow^{\mathrlap{\simeq}}
    && \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\pi_\bullet(E)}(E_\bullet(Y), E_\bullet(N))
      &\stackrel{\simeq}{\longleftarrow}& 
    Hom_{E_\bullet(E)}(
      E_\bullet(Y), 
      E_\bullet(E) \otimes_{\pi_\bullet(E)} E_\bullet(E)
    )
  }
  \,,
$$

where 

1. the right vertical map comes from the isomorphism of prop. \ref{FlatnessOfEImpliesKeyConsequence};

1. the bottom isomorphism is the cofree/forgetful [[adjunction]] isomorphism of prop. \ref{CoFreeComodules};

1. the the left vertical morphism is an isomorphism by prop. \ref{AdamsUCT}. 

Therefore also the top morphism is an iso.

=--

## Related concepts

* [[Hopf E-infinity-algebra]]

* [[Deligne's theorem on tensor categories]]


## References

* {#Adams74} [[Frank Adams]],  _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

* {#Ravenel86} [[Doug Ravenel]], chapter 2 and appendix A.1 of  _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))

* {#Kochman96} [[Stanley Kochman]], _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


* {#Hopkins99} [[Mike Hopkins]], section 5 of _[[Complex oriented cohomology theories and the language of stacks]]_, course notes 1999 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/coctalos.pdf))


* [[Paul Goerss]], _Quasi-coherent sheaves on the moduli stack of formal groups_, [pdf](http://www.math.northwestern.edu/~pgoerss/papers/modfg.pdf)

* [[Mark Hovey]], _Homotopy theory of comodules over a Hopf algebroid_, [pdf](http://math.wesleyan.edu/~mhovey/papers/comodule.pdf); _Morita theory of Hopf algebroids_ ([pdf](http://math.wesleyan.edu/~mhovey/talks/hopfalgebroids.pdf))

* Barry Walker, _Hopf algebroids and stacks_  ([pdf](http://www.math.umn.edu/~tlawson/old/stackstalk.pdf))


* {#BakerLazarev01} [[Andrew Baker]], [[Andrey Lazarev]], _On the Adams Spectral Sequence for R-modules_, Algebr. Geom. Topol. 1 (2001) 173-199 ([arXiv:math/0105079](http://arxiv.org/abs/math/0105079))
 

* {#BakerJeanneret02} [[Andrew Baker]], Alain Jeanneret, _Brave new Hopf algebroids and extensions of $MU$-algebras_, Homology Homotopy Appl. __4__:1 (2002), 163-173, [MR1937961](http://www.ams.org/mathscinet-getitem?mr=1937961), [euclid](http://projecteuclid.org/euclid.hha/1139840059)
 

See also 

* {#Schwede12} [[Stefan Schwede]], chapter II, section 10.3 of  _[[Symmetric spectra]]_, 2012


[[!redirects commutative Hopf algebroids]]

[[!redirects graded commutative Hopf algebroid]]
[[!redirects graded commutative Hopf algebroids]]

[[!redirects commutative Hopf algebra]]
[[!redirects commutative Hopf algebras]]

[[!redirects graded commutative Hopf algebra]]
[[!redirects graded commutative Hopf algebras]]

[[!redirects super-commutative Hopf algebra]]
[[!redirects super-commutative Hopf algebras]]

[[!redirects supercommutative Hopf algebra]]
[[!redirects supercommutative Hopf algebras]]
