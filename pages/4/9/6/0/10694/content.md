
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
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

A _May spectral sequence_ ([May 64](#May64), [May 74](#May74), [Ravenel 86, 3.2](#Ravenel86)) is a certain type of [[spectral sequence]] that computes the second page of the [[classical Adams spectral sequence]]. More generally, it computes [[Ext]]-groups (or [[Cotor]]-groups, via [this lemma](cotensor+product#ComoduleHomInTermsOfCotensorProduct)) of [[comodules]] over [[commutative Hopf algebras]] (the [[dual Steenrod algebra]] in the classical case) starting from the corresponding $Ext$-groups over just an [[associated graded]] Hopf algebra.

The May spectral sequence is the [[spectral sequence of a filtered complex]] induced by suitably filtering the canonical (but intractable) [[bar complex]] model for [[Ext]]/[[Cotor]] (see [Ravenel 86, chapter 3, section 2](#Ravenel86), [Kochman 96, section 5.3](#Kochman96)).




## Preliminaries


### Cobar complex

+-- {: .num_prop #ComoduleStructureOnGroundRing}
###### Proposition

Given $(\Gamma,A)$ a [[graded commutative Hopf algebroid]], then $A$ becomes a left comodule over $\Gamma$ with coaction given by the right unit

$$
  A \overset{\eta_R}{\longrightarrow} \Gamma \simeq \Gamma \otimes_A A
$$

and it becomes a right comodule with coaction given by the left unit

$$
  A \overset{\eta_L}{\longrightarrow} \Gamma \simeq A \otimes_A \Gamma
  \,.
$$


=--

+-- {: .proof}
###### Proof

Dually this is the action of morphisms on objects given by evaluation at the source or target, respectively. 

=--

+-- {: .num_defn #UnitCoidealInCommutativeHopfAlgebra}
###### Definition

Let $(\Gamma,A)$ be a [[commutative Hopf algebra]], hence a [[commutative Hopf algebroid]] for which the left and right units coincide $\eta \;\colon\; A \longrightarrow \Gamma$. 

Then the **unit coideal** of $\Gamma$ is the [[cokernel]] 

$$
  \overline{\Gamma}
    \coloneqq
  coker( A \overset{\eta}{\longrightarrow} \Gamma)
  \,.
$$ 

=--

+-- {: .num_lemma #PropertiesOfUnitCoideal}
###### Lemma

Let $(\Gamma,A)$ be a [[commutative Hopf algebra]], hence a [[commutative Hopf algebroid]] for which the left and right units coincide $\eta \;\colon\; 
A \longrightarrow \Gamma$. 

Then the unit coideal $\overline{\Gamma}$ (def. \ref{UnitCoidealInCommutativeHopfAlgebra}) carries the structure of an $A$-[[bimodule]] such that the [[projection]] morphism

$$
  \Gamma \longrightarrow \overline{\Gamma}
$$

is an $A$-bimodule homomorphism. Moreover, the coproduct $\Psi \;\colon\; \Gamma \longrightarrow \Gamma \otimes_A \Gamma$ descends to a coproduct $\overline{\Gamma} \;\colon\; \overline{\Gamma} \longrightarrow \overline{\Gamma} \otimes_A \overline{\Gamma}$ such that the projection intertwines the two coproducts.

=--

+-- {: .proof}
###### Proof

For the first statement, consider the [[commuting diagram]]

$$
  \array{
    A \otimes A 
      &\overset{A \otimes \eta}{\longrightarrow}&
    A \otimes \Gamma
      &\longrightarrow&
    A \otimes \overline{\Gamma}
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{\exists}}
    \\
    A 
      &\underset{\eta}{\longrightarrow}&
    \Gamma
      &\longrightarrow&
    \overline{\Gamma}
  }
  \,,
$$

where the left [[commuting square]] exhibits the fact that $\eta$ is a homomorphism of left $A$-modules.

Since the [[tensor product of abelian groups]] $\otimes$ is a [[right exact functor]] it preserves cokernels, hence $A \otimes \overline{\Gamma}$ is the cokernel of $A \otimes A \to A\otimes \Gamma$ and hence the right vertical morphisms exists by the [[universal property]] of cokernels. This is the compatible left module structure on $\overline{\Gamma}$. Similarly the right $A$-module structure is obtained.

For the second statement, consider the [[commuting diagram]]

$$
  \array{
    A 
      &\overset{\eta}{\longrightarrow}&
    \Gamma
      &\longrightarrow&
    \overline{\Gamma}
    \\
    {}^{\mathllap{\eta}}\downarrow
      &&
    \downarrow^{\mathrlap{\Psi}}
      &&
    \downarrow^{\mathrlap{\exists}}
    \\
    \Gamma \simeq \Gamma \otimes_A A 
      &\underset{id \otimes_A \eta}{\longrightarrow}&
    \Gamma \otimes_A \Gamma
      &\longrightarrow&
    \overline{\Gamma} \otimes_A \overline{\Gamma}
  }
  \,.
$$

Here the left square commutes by one of the co-unitality conditions on $(\Gamma,A)$, equivalently this is the co-action property of $A$ regarded canonically as a $\Gamma$-comodule. 

Since also the bottom morphism factors through zero, the [[universal property]] of the cokernel $\overline{\Gamma}$ implies the existence of the right vertical morphism as shown.

=--



+-- {: .num_defn #CobarComplex}
###### Definition
**(cobar complex)**

Let $(\Gamma,A)$ be a [[commutative Hopf algebra]], hence a [[commutative Hopf algebroid]] for which the left and right units coincide $A \overset{\eta}{\longrightarrow} \Gamma$. Let $N$ be a left $\Gamma$-comodule.

The **cobar complex** $C^\bullet_\Gamma(N)$ is the [[cochain complex]] of abelian groups with terms

$$
  C^s_\Gamma(N)
   \coloneqq
    \underset{s\; factors}{
    \underbrace{
    \overline{\Gamma}
      \otimes_A
      \cdots
      \otimes_A
    \overline{\Gamma}
    }
    }
  \otimes_A N
$$

(for $\overline{\Gamma}$ the unit coideal of def. \ref{UnitCoidealInCommutativeHopfAlgebra}, with its $A$-bimodule structure via lemma \ref{PropertiesOfUnitCoideal})

and with [[differentials]] $d_s \colon C^s_\Gamma(N) \longrightarrow C^{s+1}_\Gamma(N)$ given by the alternating sum of the coproducts via lemma \ref{PropertiesOfUnitCoideal}.
 
=--

([Ravenel 86, def. A1.2.11](#Ravenel86))

+-- {: .num_prop #CobarComplexGivesExtGroupsOutOfA}
###### Proposition

Let $(\Gamma,A)$ be a [[commutative Hopf algebra]], hence a [[commutative Hopf algebroid]] for which the left and right units coincide $A \overset{\eta}{\longrightarrow} \Gamma$. Let $N$ be a left $\Gamma$-comodule.

Then the [[cochain cohomology]] of the cobar complex $C^\bullet_\Gamma(N)$ (def. \ref{CobarComplex}) is the [[Ext]]-groups of comodules from $A$ (regarded as a left comodule via def. \ref{ComoduleStructureOnGroundRing}) into $N$

$$
  H^\bullet(C^\bullet_\Gamma(N))
    \;\simeq\;
  Ext^\bullet_\Gamma(A,N)
  \,.
$$

=--

([Ravenel 86, cor. A1.2.12](#Ravenel86), [Kochman 96, prop. 5.2.1](#Kochman96))

### Self-Ext of free graded commutative coalgebras

Throughout, let $A$ be a [[commutative ring]] and let $\Gamma$ be a graded [[commutative Hopf algebroid|commutative Hopf algebra]] over $A$. We write $(\Gamma,A)$ for this data.


+-- {: .num_lemma #CoModuleExtFromAToAForPrimitivelyGeneratedExteriorAlgebra}
###### Lemma


Let $(\Gamma,A)$ be a graded [[commutative Hopf algebra]] such that 

1. the underlying algebra is free graded commutative;

1. $\eta \colon A \to \Gamma$ is a [[flat morphism]];

1. $\Gamma$ is generated by [[primitive elements]] $\{x_i\}_{i\in I}$

then the [[Ext]] of $\Gamma$-comodules from $A$ and itself is the (graded) polynomial algbra on these generators:


$$
  Ext_\Gamma(A,A) \simeq A[\{x_i\}_{i \in I}]
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

Since the counit $\eta$ is assumed to be flat, and since $A$ is trivially a [[projective module]] over itself, [this prop.](commutative+Hopf+algebroid#CoFreeHopfComodulesAreHomNAcyclicForProjectiveN) now implies that the above is an [[acyclic resolution]] with respect to the functor $Hom_{\Gamma}(A,-) \colon \Gamma CoMod \longrightarrow A Mod$. Therefore it computes the [[Ext]]-functor. Using that forming co-free comodules is [[right adjoint]] to forgetting $\Gamma$-comodule structure over $A$ ([prop.](commutative+Hopf+algebroid#CoFreeComodules)), this yields:

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



+-- {: .num_lemma #SpectralSequenceConvergingToExtForFilteredHopfAlgebra}
###### Lemma


If $(\Gamma,A)$ is equipped with a [[filtering]] right/left $\Gamma$-comodules $N_1$ and $N_2$ are compatibly filtered, then there is a [[spectral sequence]]

$$
  \mathcal{E}_1
  =
  Ext_{gr_\bullet \Gamma}(gr_\bullet N_1, gr_\bullet N_2)
  \;\Rightarrow\;
  Ext_{\Gamma}(N_1, N_2)
$$

converging to the [[Ext]] over $\Gamma$ between $N_1$ and $N_2$, whose first page is the Ext over the [[associated graded]] Hopf algebra $gr_\bullet \Gamma$ between the associated graded modules $gr_\bullet N_1$ and $gr_\bullet N_2$.

=--

([Ravenel 86, lemma 3.1.9](#Ravenel86), [Kochman 96, prop. 3.7.5](#Kochman96))

+-- {: .proof}
###### Proof

The filtering induces a filtering on the standard cobar complex (def. \ref{CobarComplex}) which computes $Cotor(A,A)$. The spectral sequence in question is the corresponding [[spectral sequence of a filtered complex]]. Its first page is the homology of the associated graded complex (by this [prop.](spectral+sequence+of+a+filtered+complex#FirstPages)).

=--




## Construction of the May spectral sequence


Let now $A \coloneqq \mathbb{F}_2$,  $\Gamma \coloneqq \mathcal{A}^\bullet_{\mathbb{F}_2}$ be the mod 2 [[dual Steenrod algebra]]. By [Milnor's theorem](Steenrod+algebra#MilnorTheoremOnDualSteenrodAlgebra), as an $\mathbb{F}_2$-algebra this is

$$
  \mathcal{A}^\bullet_{\mathbb{F}_2} 
  = 
  \mathbb{F}_2[\xi_1, \xi_2, \cdots]
  \,.
$$

and the coproduct is given by

$$
  \Psi(\xi_n)
  =
  \underoverset{k = 0}{i}{\sum} \xi_{i - k}^{2^k} \otimes \xi_k
  \,,
$$

where we set $\xi_0 \coloneqq 1$.




+-- {: .num_defn #hGeneratorsInClassicalAdamsSpectralSequence}
###### Definition

Set

$$
  h_{i,n} \coloneqq \xi_i^{2^n}
  \,.
$$

Also one abbreviates

$$
  h_n \coloneqq h_{1,n} = \xi_1^{2^n}
  \,.
$$


=--

By binary expansion of powers, there is a unique way to express every monomial in $\mathbb{F}_2[\xi_1, \xi_2, \cdots]$ as a product of the elements $h_{i,n}$ from def. \ref{hGeneratorsInClassicalAdamsSpectralSequence}, such that each such element appears at most once in the product. E.g.

$$
  \begin{aligned}
    \xi_i^5 \xi_j^7 
      & = 
    \xi_i^{2^0 + 2^2} \xi_j^{2^0 + 2^1 + 2^2}
     \\
     & = 
     h_{i,0} h_{i,2} h_{j,0} h_{j,1} h_{j,2}
  \end{aligned}
  \,.
$$

+-- {: .num_prop #CoproductOnDualSteenrodInTermsOfAdaptedGenerators}
###### Proposition

In terms of the generators $\{h_{i,n}\}$, the coproduct on $\mathcal{A}^\ast_{\mathbb{F}_2}$ takes the following simple form

$$
  \Psi(h_{i,n})
  \;=\; 
  \underoverset{k = 0}{i}{\sum} h_{i-k,n+k}\otimes h_{k,n}
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using that the coproduct of a [[bialgebra]] is a [[homomorphism]] for the algebra structure and using [[freshman's dream]] arithmetic over $\mathbb{F}_2$, one computes:

$$
  \begin{aligned}
    \Psi(h_{i,n})
    & = 
    \Psi\left(\xi_i^{2^n}\right)
    \\
    & = (\Psi(\xi_i))^{2n}
    \\
    & = 
    \left(\underoverset{k = 0}{i}{\sum} \xi_{i-k}^{2^k} \otimes \xi_k\right)^{2^n}
    \\
    & = \underoverset{k = 0}{i}{\sum} \left(\xi_{i-k}^{2^k}\right)^{2^n} \otimes \xi^{2^n}_k
    \\
    & = \underoverset{k = 0}{i}{\sum} \xi_{i-k}^{2^k \cdot 2^n} \otimes \xi^{2^n}_k
    \\
    & = \underoverset{k = 0}{i}{\sum} \xi_{i-k}^{2^{(k+n)}} \otimes \xi^{2^n}_k
    \\
    & = \underoverset{k = 0}{i}{\sum} h_{i-k,n+k}\otimes h_{k,n}
  \end{aligned}
  \,.
$$

=--

Define a [[graded algebra|grading]] on $\mathcal{A}^\bullet_{\mathbb{F}_2}$ by setting (this is due to ([Ravenel 86, p.69](#Ravenel86)))

$$
  {\vert h_{i,n} \vert}
    \coloneqq
  2i-1
$$

and extending this additively to these unique representative.


For instance

$$
  \begin{aligned}
    \vert \xi_i^5 \xi_j^7\vert
    & = 
    {\vert h_{i,0} h_{i,2} h_{j,0} h_{j,1} h_{j,2} \vert} 
    \\
    & =
    2(2i-1) + 3(2j-1)
  \end{aligned}
  \,.
$$


Consider the corresponding [[filtered object|filtering]]

$$
  \cdots 
   \subset
  F_p \mathcal{A}^\ast_{\mathbb{F}_2}
   \subset
  F_{p+1} \mathcal{A}^\ast_{\mathbb{F}_2}
    \subset 
  \cdots 
    \subset
  \mathcal{A}^\ast_{\mathbb{F}_2}
$$

with filtering stage $p$ containing all elements of total degree $\leq p$.

Observe that

$$
  \begin{aligned}
    \Psi(\xi_i)
    &
   =
   \underset{deg = 2i-1}{\underbrace{\xi_{i} \otimes 1}}
   +
    \underoverset{0 \lt k \lt i}{}{\sum} 
     \underset{deg = 2i-2}{\underbrace{\xi_{i-k}^{p^k} \otimes \xi_k}}
   +
    \underset{deg = 2i-1}{\underbrace{1 \otimes \xi_i}}
  \end{aligned}
  \,.
$$

This means that after projection to the [[associated graded]] Hopf algebra

$$
  F_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}
   \longrightarrow
  gr_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}
$$ 

all the generators $h_{i,n}$ become [[primitive elements]]:

$$
  \begin{aligned}
    \Psi(h_{i,n})
    &
   =
   h_{i,n}\otimes 1
   +
   1 \otimes h_{i,n}
   \;\;\;\;\;
   \in 
   gr_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}
   \otimes
   gr_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}
  \end{aligned}
  \,.
$$


Hence lemma \ref{CoModuleExtFromAToAForPrimitivelyGeneratedExteriorAlgebra} applies and says that thet $Ext$ from $\mathbb{F}_2$ to itself over the [[associated graded]] Hopf algebra is the polynomial algebra in these generators:

$$
  Ext_{gr \mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)
  =
  \mathbb{F}_2[\{h_{i,n}\}_{{i \geq 1,} \atop {n \geq 0}}]  
  \,.
$$

Moreover, lemma \ref{SpectralSequenceConvergingToExtForFilteredHopfAlgebra} says that this is the first page of a spectral sequence that converges to the $Ext$ over the original Hopf algebra:

$$
  \mathcal{E}_1 
  = 
  \mathbb{F}_2[\{h_{i,n}\}_{{i \geq 1} \atop {n \geq 0}}]
  \;\Rightarrow\;
  Ext_{\mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)
  \,.
$$

This is the _May spectral sequence_ for the computation of $Ext_{\mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)$. Notice that since everything is $\mathbb{F}_2$-linear, its [extension problem](spectral+sequence#ExtensionProblem) is trivial.

Moreover, again by lemma \ref{SpectralSequenceConvergingToExtForFilteredHopfAlgebra}, the differentials on any $r$-page are the restriction of the differentials of the bar complex to the $r$-almost cycles ([prop.](Introduction+to+Stable+homotopy+theory+--+I#DifferentialsOnAlmostChains)). The differential of the bar complex is the alternating sum of the coproduct on $\mathcal{A}^\ast_{\mathbb{F}_2}$, hence by prop.  \ref{CoproductOnDualSteenrodInTermsOfAdaptedGenerators} this is:

$$
  d_1 (h_{i,n})
  =
  \underoverset{k = 0}{i}{\sum} h_{i-k,n+k}\otimes h_{k,n}  \,.
$$



## The second page of the classical Adams spectral sequence
 {#TheSecondPageOfTheClassicalAdamsSpectralSequence}


Now we use the above formula to explicitly compute the cohomology of the second page of the [[classical Adams spectral sequence]].

In doing so it is now crucial that the differential in the standard cobar complex (def. \ref{CobarComplex}) for $Cotor$ lands in $\overline{\Gamma} \coloneqq coker(\eta)$ where the generator $h_{0,n} = \xi_0 = 1$ disappears.

Recall the further abbreviation

$$
  h_n \coloneqq h_{1,n}
  \,.
$$

Hence we find using the formula from prop. \ref{CoproductOnDualSteenrodInTermsOfAdaptedGenerators}, that

$$
  \begin{aligned}
    d_1(h_n)
    & \coloneqq
    d_1(h_{1,n})
    \\
    & =   
    \overline{\Psi}(h_{1,n})
    \\
    & =
    h_{1,n} \otimes \underset{= 0}{\underbrace{ h_{0,n} }}
    + 
    \underset{= 0}{\underbrace{ h_{0,n+1} }} \otimes h_{1,n}
    \\
    & = 
    0
  \end{aligned}
$$

and hence all the elements $h_n$ are cocycles.

$$
  d_1(h_{2,0}) 
    = 
  h_{2,0} \otimes \underset{= 0}{\underbrace{h_{0,0}}}
  + 
  h_{1,1} \otimes h_{1,0}
  +
  \underset{= 0}{\underbrace{h_{0,2}}} h_{2,0}
$$

$$
  d_1( h_{2,1} )
    =
  h_{2,1} \otimes \underset{= 0}{\underbrace{h_{0,n}}}
    +
  h_{1,2} \otimes h_{1,1}
    +
  \underset{ = 0}{\underbrace{h_{0,3}}} \otimes h_{2,1}
$$

$$
  d_1( h_{2,2} )
    =
  h_{1,3} \otimes h_{1,2}
$$

$$
  d_1( h_{2,3} )
    =
  h_{1,4} \otimes h_{1,3}
$$

$$
  d_1( h_{3,0} )
    =
  h_{2,1} \otimes h_{1,0}# 
    +
  h_{1,2} \otimes h_{2,0}
$$





+-- {: .num_lemma }
###### Lemma

In the range $t - s \leq 13$, the second page of the May spectral sequence for $Ext_{\mathbb{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)$ has as generators all the 

* $h_n$

* $b_{i,n} \coloneqq (h_{i,n})^2$

as well as the element

*  $x_7 \coloneqq h_{2,0} h_{2,1} + h_{1,1} h_{3,0}$

subject to the relations

* $h_n h_{n+1} = 0$

* $h_2 b_{2,0} = h_0 x_7$

* $h_2 x_7 = h_0 b_{2,1}$.

The differentials in this range are

1. $d_r(h_{n}) = 0$

1. $d_2(b_{2,n}) = h_n^2 h_{n+2} + h_{n+1}^3$

1. $d_2(x_7) = h_0 h_2^2$

1. $d_2(b_{3,0}) = h_1 b_{2,1} + h_3 b_{2,0}$

1. $d_4(b_{2,0}^2) = h_0^4 h_3$.

=--

e.g. ([Ravenel 86, lemma 3.2.8 and lemma 3.2.10](#Ravenel86), [Kochman 96, lemma 5.3.2 and lemma 5.3.3](#Kochman96))

Hence this solves the May spectral sequence, hence gives the second page of the classical Adams spectral sequence. Inspection just of the degrees then shows that in this range there is no non-trivial differential in the Adams spectral sequece in this range. This way one arrives at:

+-- {: .num_theorem}
###### Theorem

In low $t-s$ the group $Ext_{\mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)$ is spanned by the items in the following table

<img src="http://ncatlab.org/nlab/files/ClassicalAdamsSpectralSequence.jpg" width="600" >

(graphics taken from ([[Symmetric spectra|Schwede 12]]))


=--

([Ravenel 86, theorem 3.2.11](#Ravenel86), [Kochman 96, prop. 5.3.6](#Kochman96))

Hence the first dozen [[stable homotopy groups of spheres]] 2-locally are


| $k =$ | 0 | 1 | 2 | 3 | 4  | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $\pi_k(\mathbb{S}\otimes \mathbb{Z}_{(2)}) = $ | $\mathbb{Z}_{(2)}$  | $\mathbb{Z}/2$  |  $\mathbb{Z}/2$ |  $\mathbb{Z}/8$ |  $0$ |  $0$ | $\mathbb{Z}/2$ |   $\mathbb{Z}/16$ | $(\mathbb{Z}/2)^2$ |  $(\mathbb{Z}/2)^3$ | $\mathbb{Z}/2$ | $\mathbb{Z}/8$ | $0$ | $0$ | 

Remark: The full answer turns out to be this:


| $k =$ | 0 | 1 | 2 | 3 | 4  | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | $\cdots$ | 
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $\pi_k(\mathbb{S}) = $ | $\mathbb{Z}$  | $\mathbb{Z}_2$  |  $\mathbb{Z}_2$ |  $\mathbb{Z}_{24}$ |  $0$ |  $0$ | $\mathbb{Z}_2$ |   $\mathbb{Z}_{240}$ | $(\mathbb{Z}_2)^2$ |  $(\mathbb{Z}_2)^3$ | $\mathbb{Z}_6$ | $\mathbb{Z}_{504}$ | $0$ | $\mathbb{Z}_3$ | $(\mathbb{Z}_2)^2$ | $\mathbb{Z}_{480} \oplus \mathbb{Z}_2$ | $\cdots$ |



## Related concepts

* [[Curtis algorithm]]

## References

The origin is in 

* {#May64} [[Peter May]],  _The cohomology of restricted Lie algebras and of Hopf algebras; application to the Steenrod algebra_, Thesis,  Princeton 1964

* {#May66} [[Peter May]],  _The cohomology of restricted Lie algebras and of Hopf algebras_, Journal of Algebra 3, 123-146 (1966) ([pdf](http://math.uchicago.edu/~may/PAPERS/3.pdf))

* [[Peter May]], _Some remarks on the structure of Hopf algebras_, Proceedings of the AMS, vol 23, No. 3 (1969) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/9.pdf))
 
Further computational improvements and a computation of the first 70 differentials (for the case of the mod 2 [[Steenrod algebra]]) was given in

* {#Tangora17} [[Martin Tangora]], _On the cohomology of the Steenrod algebra_, Math. Z. 116, 18-64 (1970)

More on the $E_2$-term is in 

* {#May74} [[Peter May]], _The Steenrod algebra and its associated graded algebra_, University of Chicago preprint, 1974.


Review includes

* {#Ravenel86} [[Doug Ravenel]], chapter 3, section 2 of _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986

* {#Kochman96} [[Stanley Kochman]], section 5.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* Wikipedia, _[May spectral sequence](http://en.wikipedia.org/wiki/May_spectral_sequence)_

[[!redirects May spectral sequences]]