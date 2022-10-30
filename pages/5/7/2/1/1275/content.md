
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

Given a [[monoidal category]] $\mathcal{M}$ and a [[coalgebra]] $C$ in $\mathcal{M}$ denote by $\mathcal{M}^{C}$ ($ resp. {}^{C}\mathcal{M}$)
the category of right (resp. left) ${C}$-[[comodules]]; similarly for an algebra $E$, denote by ${}_E\mathcal{M}$ (resp. $\mathcal{M}_E$) the [[category of modules|category of left E-modules]]
(right $E$-modules). If the monoidal category is [[symmetric monoidal category|symmetric]] or there is instead an appropriate [[distributive law]], then there are extensions of this notation to [[bimodules]], [[bicomodules]], relative [[Hopf modules]], entwined modules etc. e.g. Write ${}_E\mathcal{M}^B$ for left-right relative $(E,B)$-Hopf modules where $E$ is a $B$-comodule algebra over a bialgebra $B$. 

Let $k$ be a commutative unital [[ring]], and let $\mathcal{M}$ be $k$-linear (in particular it has [[zero morphisms]]). 

+-- {: .num_defn }
###### Definition

Given a [[coalgebra]] $C$ in $\mathcal{M}$, a left $C$-[[comodule]] $(N,\rho_N \colon N\to N\otimes C)$, a right $C$-comodule $(M,\rho_M \colon M\to C\otimes M)$, their __cotensor product__ is an object in $\mathcal{M}$ given by the [[kernel]]

$$
  N \Box M  
  \coloneqq
  \mathrm{ker} (\rho_N \otimes \mathrm{id}_M - \mathrm{id}_N \otimes \rho_M ).
$$

=--

If [[equalizers]] exist in $\mathcal{M}$, this formula extends to a [[bifunctor]]

$$
   {}\Box = \Box^{C}  
  \colon
\mathcal{M}^{C} \times {}^{C}\mathcal{M} \rightarrow \mathcal{M}
  \,.
$$

If $B$ is a [[bialgebra]] in $\mathcal{M}$ and $E$ is a right $B$-comodule algebra then the same formula defines a bifunctor

$$
  \Box 
    \colon 
  {}_{E}\mathcal{M}^{B} \times {}^{B}\mathcal{M} \rightarrow
{}_{E}\mathcal{M}
  \,.
$$ 


## Properties

### Relation to tensor product

Let now $\mathcal{M}=({}_k\mathrm{Mod},\otimes_k)$ be the symmetric monoidal category of $k$-modules.

Let $D$ be another $k$-coalgebra, with coproduct $\Delta_C$.
If $D$ is [[flat module|flat]] as a $k$-module
(e.g. $k$ is a field), and $N$ a left $D$- right $C$-bicomodule,
then the cotensor product $N \Box M$ is a $D$-subcomodule of the [[tensor product]] $N \otimes_k M$. In particular, under the flatness assumption, if $\pi \colon D \rightarrow C$ is a surjection of coalgebras then $D$ is a left $D$- right $C$-bicomodule via $\Delta_D$ and $(\id \otimes \pi) \circ \Delta_D$
respectively, hence $\mathrm{Ind}^D_C \coloneqq D \Box^C -$
is a functor from left $C$- to left
$D$-comodules called the [[induced comodule|induction]] functor for left comodules from $C$ to $D$. 

### For comodules over commutative Hopf coalgebroids
 {#ForComodulesOverCommutativeHopfCoalgebroids}

+-- {: .num_prop #LeftComodulesToRightComodules}
###### Proposition

Consider a [[commutative Hopf algebroid]] $\Gamma$ over $A$ ([def.](commutative+Hopf+algebroid#CommutativeHopfAlgebroidDefinitionInExplicitComponents)). Any left comodule $N$ over $\Gamma$ ([def.](commutative+Hopf+algebroid#CommutativeHopfAlgebroidComodule)) becomes a right comodule via the coaction

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

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$, ([def.](commutative+Hopf+algebroid#CommutativeHopfAlgebroidDefinitionInExplicitComponents)), and given $N_1$ a right $\Gamma$-comodule and $N_2$ a left comodule ([def.](commutative+Hopf+algebroid#CommutativeHopfAlgebroidComodule)), then their **cotensor product** $N_1 \Box_\Gamma N_2$ is the [[kernel]] of the difference of the two coaction morphisms:

$$
  N_1 \Box_\Gamma N_2
    \;\coloneqq\;
  ker
  \left(
    N_1 \otimes_A N_2
    \overset{\Psi_{N_1}\otimes_{A} id - id \otimes_A \Psi_{N_2} }{\longrightarrow}
  \right)
  \,.
$$

If both $N_1$ and $N_2$ are left comodules, then their cotensor product is the cotensor product of $N_2$ with $N_1$ regarded as a right comodule via prop. \ref{LeftComodulesToRightComodules}.

=--

e.g. ([Ravenel 86, def. A1.1.4](#Ravenel86)).


+-- {: .num_prop}
###### Proposition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$,
and given $N_1, N_2$ two left $\Gamma$-comodules , then their [[cotensor product]] (def. \ref{CotensorProductOfComodules}) is commutative, in that there is an [[isomorphism]]

$$
  N_1 \Box N_2 \;\simeq\; N_2 \Box N_1
  \,.
$$

=--

(e.g. [Ravenel 86, prop. A1.1.5](#Ravenel86)) 

+-- {: .num_lemma #ComoduleHomInTermsOfCotensorProduct}
###### Lemma

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$,
and given $N_1, N_2$ two left $\Gamma$-comodules, such that $N_1$ is [[projective module|projective]] as an $A$-[[module]], then

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


## Related concepts

* The [[derived functor]] of cotensoring is called _[[Cotor]]_.

## References

Cotensor products in [[noncommutative geometry]] appear in the role of [[space of sections]] of [[associated bundle|associated]] [[vector bundles]] of [[quantum principal bundle]]s (which in affine case correspond to [[Hopf-Galois extensions]]). See e.g.

* [[Shahn Majid]], _Foundations of quantum groups theory_, 2nd extended edition, paperback, Cambridge Univ. Press 2000.

For a nonaffine extension of the sections of associated quantum vector bundle, using [[localization]] theory see

* [[Zoran Škoda]], _Coherent states for Hopf algebras_,
Lett. Math. Phys. 81 (2007), no. 1, 1--17. ([arXiv:math.QA/0303357](http://front.math.ucdavis.edu/0303.5357))

In [[Hopf algebra]] theory, cotensor products appear as early as in 

* [[John Milnor]], [[John Moore]], On the structure of Hopf algebras.  Ann. of Math. (2)  81  1965 211--264.

The authors mention that they learned the notion from Mac Lane who knew it earlier in more general contexts. 

A textbook account is in 

* [[Doug Ravenel]], section A1.1 of _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986/2003

An important problem is that the cotensor product of bicomodules is in general (even for $\mathcal{M}={}_k\mathrm{Mod}$) *not associative*, even up to an isomorphism. 

Cotensor products play a prominent role in various treatments of [[Galois theory]] in [[noncommutative geometry]]; a particularly geometric approach is within a version of [[noncommutative algebraic geometry]] based on usage of monoidal categories, as sketched in 

* [[Tomasz Maszczyk]], Noncommutative geometry through monoidal categories I, [arXiv:0707.1542](http://front.math.ucdavis.edu/0707.1542)

[[!redirects cotensor products]]
