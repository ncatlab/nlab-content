
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
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

Deligne's theorem on tensor categories ([Deligne 02](#Deligne02), recalled as theorem \ref{TheTheorem} below) establishes [[Tannaka duality]] between linear [[tensor categories]] in [[characteristic zero]] subject to just a mild size constraint (subexponential growth, def. \ref{SubexponentialGrowth} below), and [[supergroups]] ("[[supersymmetries]]"), realizing these tensor categories as [[categories of representations]] of these supergroups.


## Relevance

### For supersymmetry

Since the concept of linear [[tensor categories]] arises very naturally in [[mathematics], the theorem gives a purely mathematical "reason" for the relevance of [[superalgebra]] and [[supergeometry]. It is reasonable to wonder why of all possible generalizations of [[commutative algebra]], it is [[supercommutative superalgebras]] that are singled out (from alternatives such as plain $\mathbb{Z}/2$-[[graded algebras]], or in fact $\mathbb{Z}/n$-graded algebras or general [[noncommutative algebras]] or, the like), as they are notably in theoretical [[physics]] ("[[supersymmetry]]"), but also in mathematical fields such as [[spin geometry]] (e.g. via the relation between [[Majorana spinors]] and supersymmetry, [here](Majorana+spinor#Supersymmetry)) and [[topological K-theory]] (for instance via its incarnation as _[[Karoubi K-theory]]_, or via the descriptioon of[[twisted K-theory]] by _[[super line 2-bundles]]_). 

But with $k$-linear [[tensor categories]] appearing on general abstract grounds as the canonical structure to consider in [[representation theory]], Deligne's theorem serves to base supercommutative superalgebra on this same general abstract foundation, showing that this is precisely the context in which full $k$-linear tensor categories exhibit full [[Tannaka duality]].

More concretely, in [[quantum field theory]], under the [[Wigner classification]], [[fundamental particles]] are identified with [[irreducible representations]] of the [[isometry group]] of the local model of [[spacetime]]. Forming the [[tensor product]] of two such representations corresponds to combining them as two [[subsystems]] of a joint system. Therefore it is natural to demand that physical particle species should form complex-linear [[tensor categories]]. Deligne's theorem then gives that [[supersymmetry]] is the most general context in which this works out. (In physics the irreducible representation in this context here are called the _[[supermultiplets]]_.)

### For Tannaka duality of Hopf algebras
 {#RelevanceForHopfAlgebras}

By [[Tannaka duality]] rigid symmetric monoidal categories in general are [[categories of modules]] of [[triangular Hopf algebras]]. Hence Deligne's theorem here implies that those triangular Hopf algebras whose category of representation has subexponential growth (def. \ref{SubexponentialGrowth} below) are equivalent to supercommutative Hopf algebras. See ([Etingof-Gelaki 02](#EtingofGelaki02)) for more.

[[!include structure on algebras and their module categories - table]]


## Background

This section provides exposition of the necessary background for the statement of Deligne's theorem (theorem \ref{TheTheorem} below).

We recall the incarnation of [[groups]] a [[Hopf algebras]], the corresponding incarnation of [[linear representations]] as [[comodules]], and the [[tensor product]] structure on these. Then we recall the definition of [[symmetric monoidal categories]] and consider the category of [[super vector spaces]] [[sVect]] as an example for a non-trivial symmetric [[braiding]]. Using this we discuss [[supercommutative superalgebra]] as ordinary [[commutative algebra]] but [[internalization|internal]] to [[sVect]] and thus obtain the definition of (affine algebraic) [[supergroups]] and their [[linear representations]] as [[formal duals]] of [[supercomutative Hopf algebras]] and of [[comodules]] over these, respectively.



### Groups as Hopf algebras

We are interested in [[groups]] equipped with [[geometry]]. 

A familiar example is [[differential geometry]], where one considers groups whose underlying set is promoted to a [[smooth manifold]] and all whose operations (product, inverses) are [[smooth functions]]. These are of course [[Lie groups]]. 

A **[[linear representation]]** of a [[Lie group]] $G$ on a [[vector space]] $V$ is a [[smooth function]]

$$
  \rho \;\colon\; G \times V \longrightarrow V 
$$

such that 

1. ([[linear map|linearity]]) for all elements $g \in G$ the function

   $$
     \rho(g) \colon V \longrightarrow V
   $$

   is a [[linear function]]

1. ([[unitality]]) for $e \in G$ the [[neutral element]] then $\rho(e)$ is the [[identity]] function;

1. ([[action]] property) for $g_1, g_2 \in G$ any two elements, then acting with them consecutively is the same as acting with their product:

   $$
      \rho(g_2) \circ  \rho(g_1) = \rho(g_2 g_1)
      \,.
   $$

But here we need to consider groups with more general geometric structure. The key to the generalization is to regard [[spaces]] dually via their [[algebras of functions]].

The [[duality]] between (local) [[spaces]] and their [[algebras of functions]] is profound. In [[physics]] it has always been used implicitly, in fact it was so ingrained into theoretical physics that it took much effort to abstract away from [[coordinate system|coordinate functions]] to discover global [[Riemannian geometry]] in the guise of"[[general relativity]]". As mathematics, an early prominent duality theorem is [[Gelfand duality]] which served as motivation for the very definition of [[]algebraic geometry]. In great generality it appears as "[[Isbell duality]]".

In the above example, write $C^\infty(X)$ for the [[smooth algebra]] of [[smooth functions]] on a [[smooth manifold]] $X$. The assignment

$$
  C^\infty(-) \;\colon\; SmthMfd \longrightarrow SmthAlg_{\mathbb{R}}
$$

is a [[contravariant functor]], which is [[fully faithful functor|fully faithful]].  This means that for 

$$
  f \;\colon\; X \longrightarrow Y
$$

any [[smooth function]], then precomposition of smooth functions on $Y$ with $f$ yields a homomorphism of smooth algebras going the other way around

$$
  C^\infty(X) \longleftarrow C \infty(Y) \;\colon\; f^\ast
$$

and the associatioon $f \mapsto f^\ast$ is a [[natural bijection]].
Of course, for any two composable smooth functions $f,g$ then $(g \circ f )^\ast = f^\ast \circ g^\ast$ and if $f = id$ is the identity smooth function, then f^\ast = id$ is the identity homomomorphism of smooth algebras.

Moreover, the functor $C^\infty(-)$ sends [[Cartesian products]] of smooth manifolds to "completed tensor products" $\otimes^c$ of function algebras (namely to the [[coproduct]] of [[smooth algebras]], see there)

$$
  C^\infty(X \times Y) \simeq C^\infty(X) \otimes^c C^\infty(Y)
  \,.
$$

Together this means that if $X = G$ is equipped with the structure of a [[group object]], then the product operation in the group induces a "[[coproduct]]" operation on its smooth algebra of smooth functions:

$$
  \array{
    product &\colon& G \times G &\longrightarrow& G
    \\
    && C^\infty(G) \otimes^c C^\infty(G) &\longleftarrow& C^\infty(G) &\colon& product^\ast 
  }
  \,.
$$

Now the [[associativity]] of the group product translates into a corresponding dual property of its dual, called "[[co-associativity]]", and so forth. The resulting algebraic structure is called a **[[Hopf algebra]]**.
 
What actually appears in the main theorem \ref{TheTheorem} below are "affine algebraic super-groups". One way to say this is that they are [[super-scheme|super-]][[group schemes]] whose underlying [[super-scheme]] is a [[super-scheme|super-]][[affine variety]]. Some of these are [[super Lie groups]], namely [[group objects]] in [[supermanifolds]].  But by their affine-ness, affine algebraic supergroups have a direct algebraic, description as [[Hopf algebras]], and we make this explicit now. 


So the explicit definition of a _[[Hopf algebra]]_ may look involved at first sight. But Hopf algebras are simply [[formal duals]] of [[groups]]. Since this perspectiv is straightforward, we may just as well consider it in the generality of [[groupoids]]:

+-- {: .num_defn #CommutativeHopfAlgebroid}
###### Definition

A **[[commutative Hopf algebroid]]** is an [[internal groupoid]] in the [[opposite category]] [[CRing]]${}^{op}$ of [[commutative rings]], regarded with its [[cartesian monoidal category]] structure.

=--

(e.g. [Ravenel 86, def. A1.1.1](commutative+Hopf+algebroid#Ravenel86))

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

* $\eta_L, \etaR$ are called the left and right _[[unit]] maps_;

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

e.g. ([Ravenel 86, def. A1.1.1](commutative+Hopf+algebroid#Ravenel86))


### Linear representations as Comodules

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

+-- {: .num_defn #TensorProductOfComodulesOverAHopfAlgebra}
###### Definition

Given two comodules $N_1, N_2$ over a [[commutative Hopf algebra]] $\Gamma$ over $k$, then their **[[tensor product]]** is the the [[tensor product of modules]] $N_1 \otimes_k N_2$ equipped with the following co-action

$$
  N_1 \otimes_k N_2
    \overset{\Psi1 \otimes_k \Psi_2}{\longightarrow}
  \Gamma \otimes_k N_1 \otimes_k \Gamma \otimes N_2
    \overset{}{\longrightarrow}
  \Gamma \otimes_k \Gamma \otimes_k N_1 \otimes_k N_2
      \overset{((-)\cdot (-)) \otimes_k id_{N_1} \otimes_k id_{N_2} }{\longrightarrow}
  \Gamma \otimes_k N_1 \otimes_k N_2
  \,.
$$

=--

This is the [[formal dual]] of the [[tensor product of representations]], the action on which is induced by

$$
  G \times V_1 \times V_2
     \overset{\Delta_G \times id}{\longrightarrow}
  G \times G \times V_1 \times V_2
     \simeq
   G \times V_1 \times G \times V_1
     \overset{\rho_1 \times \rho_2}{\longrightarrow}
   V_1 \times V_2
  \,.
$$

Under the tensor product of co-modules (def. \ref{TensorProductOfComodulesOverAHopfAlgebra}), these form a [[symmetric monoidal category]]. We now recall what recall what that means. 

### Tensor products and Monoidal categories

+-- {: .num_defn #VectorSpaces} 
###### Definition

For $k$ a [[field]], we write $Vect_k$ for the [[category]] whose

* [[objects]] are $k$-[[vector spaces]];

* [[morphisms]] are $k$-[[linear functions]] between these.

When the [[ground field]] $k$ is understood or when its precise nature is irrelevant, we will often notationally suppress it and speak of just the category [[Vect]] of vector spaces.

This is the category inside which [[linear algebra]] takes place.

=--

Of course the category [[Vect]] has some special properties. Not only are its objects "linear spaces", but the whole category inherits linear structure of sorts. This is traditionally captured by the following terminology for **[[additive and abelian categories]]**. Notice that there are several different but equivalent ways to state the following properties (discussed behind the relevant links).

+-- {: .num_defn #AdditiveAndAbelianCategories} 
###### Definition

Let $\mathcal{C}$ be a [[category]]. 

1. Say that $\\mathcal{C}$ has **[[direct sums]]** if its has [[finite products]] and [[finite coproducts]] and if the cannical comparison  morphism between these is an [[isomorphism]]. We write $V \oplus W$ for the direct sum of two objects of $\mathcal{C}$ in this.

1. Say that $\mathcal{C}$ is an **[[additive category]]** if it has [[direct sums]] and in addition it is [[Ab-enriched category|enriched in abelian groups]], meaning that every [[hom-set]] is equipped with the stucture of an [[abelian group]] such that [[composition]] of morphisms is a [[bilinear map]].

1.Say that $\mathcal{C}$ is an **[[abelian category]]** if it is an [[additive category]] and has property that its [[monomorphisms]] are precisely the inclusions of [[kernels]] and its [[epimorphisms]] are precisely the projections onto [[cokernels]].

=--

We also make the following definition of $k$-linear category, but notice that conventions differ as to which extra properties beyond Vect-enrichment to require:

+-- {: .num_defn #LinearCategory} 
###### Definition

For $k$ a [[field]], call a [[category]] $\mathcal{C}$ a **$k$-[[linear category]]** if

1. it is an [[abelian category]] (def. \ref{AdditiveAndAbelianCategories});

1. its [[hom-sets]] have the structure of $k$-[[vector spaces]] such that [[composition]] of morphisms is a [[bilinear map]] 

and the underlying additive [[abelian group]] structure of these [[hom-spaces]] is that of the underlying [[abelian category]].

=--

+-- {: .num_example} 
###### Example

$Vect_k$ is a $k$-linear category.


=--

Recall the basic construction of the [[tensor product of vector spaces]].

+-- {: .num_defn #TensorProductOfVectorSpaces} 
###### Definition

Given two [[vector spaces]] over some [[field]] $k$,  $V_1, V_2 \in Vect_k$, their [[tensor product of vector spaces]] is the vector space denoted

$$
  V_1 \otimes_k V_2 \in Vect
$$

whose elements are [[equivalence classes]] of  [[tuples]] of elements $(v_1,v_2)$ with $v_i \in V_i$, for the [[equivalence relation]] given by

$$
  (k v_1 , v_2) \;\sim\; (v_1, k v_2)
$$

$$
  (v_1 + v'_1 , v_2) \; \sim \; (v_1,v_2) + (v'_1, v_2)
$$

$$
  (v_1 , v_2 + v'_2) \; \sim \; (v_1,v_2) + (v_1, v'_2)
$$

More abstractly this means that the [[tensor product of vector spaces]] is the vector space characterized by the fact that

1. it receives a [[bilinear map]]
   
   $$
     V_1 \times V_2 \longrightarrow V_1 \otimes V_2
   $$

   (out of the [[Cartesian product]] of the underlying sets)

1. any other [[bilinear map]] of the form

   $$
     V_1 \times V_2 \longrightarrow V_3
   $$

   factors through the above bilinear map via a unique [[linear map]]

   $$
     \array{
        V_1 \times V_2 &\overset{bilinear}{\longrightarrow}& V_3
        \\
        \downarrow & \nearrow_{\mathrlap{\exists ! \, linear}}
         \\
         V_1 \otimes_k V_2
     }
   $$

=--

The existence of the [[tensor product of vector spaces]], def. \ref{TensorProductOfVectorSpaces}, equips the category [[Vect]] of vector spaces with extra structure, which is a "[[categorification]]" of the familair structure of a [[semi-group]]. One also says "[[monoid]]" for [[semi-group]] and therefore [[categories]] equippd with a [[tensor product]] operation are also called  _[[monoidal categories]]_:
 

+-- {: .num_defn #MonoidalCategory} 
###### Definition

A **[[monoidal category]]** is a [[category]] $\mathcal{C}$ equipped with 

1. a [[functor]]

   $$ 
      \otimes 
        \;\colon\; 
      \mathcal{C} \times \mathcal{C}  
       \longrightarrow
      \mathcal{C}
   $$

   out of the [[product category]] of $\mathcal{C}$ with itself, called the **[[tensor product]]**, 

1. an object

   $$ 
     1 \in \mathcal{C} 
   $$

   called the **[[unit object]]** or **[[tensor unit]]**, 

1. a [[natural isomorphism]] 

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

As expected, we have the following basic example:

+-- {: .num_example #VectAsAMonoidalCategory} 
###### Example

For $k$ a [[field]], the category [[Vect]]${}_k$ of $k$-[[vector spaces]] becomes a [[monoidal category]] (def. \ref{MonoidalCategory}) as follows

* the abstract [[tensor product]] is the [[tensor product of vector spaces]] $\otimes_k$ from def. \ref{TensorProductOfVectorSpaces} 

* the [[tensor unit]] is the [[field]] $k$ itself, regarded as a 1-dimensional vector space over itself;

* the [[associator]] is the map that on representing [[tuples]] acts as

  $$
    \alpha_{V_{1}, V_2, V_3} 
       \;\colon\; 
   ((v_1, v_2), v_3) \mapsto (v_1, (v_2,v_3))
  $$

* the left [[unitor]] is the map that on representing [[tuples]] is given by

  $$
    \ell_{V} \colon (k,v) \mapsto k v
  $$

  and the right unitor is similarly given by

  $$
    r_V \colon (v,k) \mapsto k v
    \,.
  $$

That this satisifes the [[pentagon identity]] (def. \ref{MonoidalCategory}) and the left and right unit identities is immediate on representing tuples.

=--

But the point of the abstract definition of [[monoidal categories]] is that there are also more exotic examples. The followig one is just a minimal enrichment of example \ref{VectAsAMonoidalCategory}, and yet it will be important.

+-- {: .num_example #GradedVectorSpacesAsAMonoidaCategory} 
###### Example

Let $G$ be a [[group]] (or in fact just a [[monoid]]/[[semi-group]]). A **$G$-[[graded vector space]]** $V$ is a [[direct sum]] of vector spaces labeled by the elements in $G$:

$$
  V = \underset{g \in G}{\oplus} V_g
  \,.
$$

A [[homomorphism]] 

$$
  \phi \;\colon\; V \longrightarrow W
$$

of $G$-graded vector spaces is a [[linear map]] that respects this direct sum structure, hence equivalently a [[direct sum]] of [[linear maps]] 

$$
  \phi_g \;\colon\; V_g \longrightarrow W_g
$$

for all $g \in G$, such that

$$
  \phi = \underset{g \in G}{\oplus} \phi_g
  \,.
$$

This defines a [[category]], denoted $Vect^G$. Equip this category with a [[tensor product]] which on the underlying vector spaces is just the [[tensor product of vector spaces]] from def. \ref{TensorProductOfVectorSpaces}, equipped with the $G$-grading with is obtained by multiplying degree labels in $G$:

$$
  (V \otimes W)_g
    \;\coloneqq\;
  \underset{{g_1, g_2 \in G} \atop {g_1 g_2 = g}}{\oplus}
   V_{g_1} \otimes_k V_{g_2} 
  \,.
$$

The [[tensor unit]] for the tensor product is the ground field $k$, regarded as being in the degree of the [[neutral element]] $e \in G$

$$
  1_g
  \;=\;
  \left\{
    \array{
      k & | g = e
      \\
      0 | otherwise
    }
  \right.
  \,.
$$

The [[associator]] and [[unitors]] are just those of the monoidal structure on plain vector spaces, from example \ref{VectAsAMonoidalCategory}.

=--

One point of abstracting the concept of a [[monoidal category]] is that it allows to prove general statements uniformly for all kinds of tensor products, familar ones and more exotic ones. The following lemma \ref{kel1} and remark \ref{CoherenceForMonoidalCategories} are two important such statements.

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

The above discussion makes it clear that a [[monoidal category]] is like a [[monoid]]/[[semi-group]], but "[[categorified]]". Accordingly we may consider additional properties of [[monoids]]/[[semi-groups]] and correspondingly lift them to monoidal categories. A key such property is _[[commutative ring|commutativity]]_. But while for a monoid, commutativity is just an extra [[property]], for a [[monoidal category]] it involves choices of commutativity-[[isomorphisms]] and hence is [[stuff, structure and property|extra structure]]. This may seem like a subtle point, but in fact, as we will see [below](#SuperGroupsAsSuperHopfAlgebras), this is the very source of [[superalgebra]].

+-- {: .num_defn #BraidedMonoidalCategory} 
###### Definition

A **[[braided monoidal category]]**, is a [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]]

$$ 
  \tau_{x,y} \colon x \otimes y \to y \otimes x 
$$

(for all [[objects]] $x,y in \mathcal{C}$) called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved ("hexagon identities"):

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

Consider the simplest non-trivial special case of $G$-[[graded vector spaces]] from example \ref{GradedVectorSpacesAsAMonoidaCategory}, the case where $G = \mathbb{Z}/2$ is the [[cyclic group of order two]].

+-- {: .num_example #Z2Zgradedvectorspaces}
###### Example

A **$\mathbb{Z}/2$-[[graded vector space]]** is a [[direct sum]] of two vector spaces

$$
  V = V_{even} \oplus V_{odd}
  \,,
$$

where we think of $V_{even}$ as the summand that is graded by the [[neutral element]] in $\mathbb{Z}/2$, and of $V_{odd}$ as being the summand that is graded by the single non-trivial element. 

A [[homomorphism]] of $\mathbb{Z}/2$-graded vector spaces

$$
  f \;\colon\; V_1 \longrightarrow V_2
$$

is a [[linear map]] of the underlying vector spaces that respects the grading, hence equivalently a pair of linear maps 

$$
  f_{even} \;\colon\; (V_1)_{even} \longrightarrow (V_1)_{even}
$$

$$
  f_{odd} \;\colon\; (V_1)_{odd} \longrightarrow (V_1)_{odd}
$$

between then summands in evem degree and in odd degree, respectively:

$$
  f = f_{even} \oplus f_{odd}
  \,.
$$

The [[tensor product]] of $\mathbb{Z}/2$-graded vector space is the [[tensor product of vector spaces]] of the underlying vector spaces, but with the grading obtained from multiplying the original gradings in $\mathbb{Z}/2$. Hence

$$
  (V_1 \otimes V_2)_{even}
    \coloneqq
  (V_1)_{even} \otimes (V_2)_{even}
    \oplus
  (V_1)_{odd} \otimes (V_2)_{odd}
$$

and

$$
  (V_1 \otimes V_2)_{odd}
    \coloneqq
  (V_1)_{even} \otimes (V_2)_{odd}
    \oplus
  (V_1)_{odd} \otimes (V_2)_{even}
  \,.
$$

As in example \ref{GradedVectorSpacesAsAMonoidaCategory}, this definition makes $\mathbb{Z}/2$ a [[monoidal category]] def. \ref{MonoidalCategory}. 

=--

+-- {: .num_prop #TheTwoNontrivialBraidingsOnZ2GradedVectorSpaces} 
###### Proposition

There are, up to [[braided monoidal functor|braided monoidal]] [[equivalence of categories]], precisely two choices for a [[symmetric monoidal category|symmetric]] [[braiding]] (def. \ref{SymmetricMonoidalCategory})

$$
  V_1 \otimes V_2 
     \stackrel{\tau_{V_1,V_2}}{\longrightarrow}
  V_2 \otimes V_1
$$


on the [[monoidal category]] $(Vect_k^{\mathbb{Z}/2}, \otimes_k)$ of $\mathbb{Z}/2$-[[graded vector spaces]] from def. \ref{Z2Zgradedvectorspaces}.

1. the **trivial braiding** whch is the [[natural transformation|natural]] [[linear map]] given on tuples $(v_1,v_2)$ representing an element in $V_1 \otimes V_2$ (according to def. \ref{TensorProductOfVectorSpaces}) by

   $$
     \tau^{triv}_{V_1, V_2} \;\colon\; (v_1,v_2) \mapsto (v_2, v_1)
   $$

1. the **super-braiding** which is the [[natural transformation|natural]] [[linear function]] given on tuples $(v_1,v_2)$ of _homogeneous degree_ (i.e. $v_i \in (V_i)_{\sigma_i} \hookrightarrow V_i$, for $\sigma_i \in \mathbb{Z}/2$) by 

   $$
     \tau^{super}_{V_1, V_2} 
        \;\colon\;
     (v_1, v_2)
        \mapsto
     (-1)^{deg(v_1) deg(v_2)}
     \,
     (v_2,v_1)
     \,.
   $$

=--

+-- {: .proof}
###### Proof

For $(\mathcal{C}, \otimes, 1)$ a [[monoidal category]], write

$$
  (Line(\mathcal{C}), \otimes, 1)
    \hookrightarrow
  (\mathcal{C}, \otimes, 1)
$$ 

for the [[full subcategory]] on those $L \in \mathcal{C}$ which are [[invertible objects]] under the [[tensor product]], i.e. such that there is an object $L^{-1} \in \mahcal{C}$ with $L \otimes L^{-1} \simeq 1$ and $L^{-1} \otimes L \simeq 1$. Since the [[tensor unit]] is clearly in $Line(L)$ (with $1^{-1} \simeq 1$) and since with $L_1, L_2 \in Line(\mathcal{C}) \hookrightarrow \mathcal{C}$ also $L_1 \otimes L_2 \in Line(\mathcal{C})$ (with $(L_1 \otimes _2)^{-1} \simeq L_2^{-1} \otimes L_1^{-1}$) the [[monoidal category]] structure on $\mathcal{C}$ restricts to $Line(\mathcal{C})$. 


Accordingly any [[braiding]] on $(\mathcal{C}, \otimes,1)$ restricts to a braiding on $(Line(\mathcal{C}), \otimes, 1)$. Hence it is sufficient to show that there is an essentially unique non-trivial symmetric braiding on $(Line(\mathcal{C}), \otimes, 1)$, and that this is the restriction of a braiding on $(\mathcal{C}, \otimes, 1)$.

Now $(Line(\mathcal{C}, \otimes , 1))$ is necessarily a [[groupoid]] (the "[[Picard groupoid]]" of $\mathcal{C}$) and in fact is what is called a _[[2-group]]_. As such we may regard it equivalently as a [[homotopy 1-type]] with group structure, and as such it it is equivalent to its [[delooping]]

$$
  B_\otimes Line(\mathcal{C})
$$

regarded as a [[pointed homotopy type]]. (See at _[[looping and delooping]]_).

The [[Grothendieck group]] of $(\mathcal{C}, \otimes, 1)$ is 

$$
  \pi_0(Line(\mathcal{C}))
    \simeq
  \pi_1(B Line(\mathcal{C}))
$$

the [[fundamental group]] of the delooping space. 

Now a symmetric braiding on $Line(\mathcal{C})$ is precisely the structure that makes it a [[symmetric 2-group]] which is equivalently the structure of a second [[delooping]] $B^2 Line(\mathcal{C})$ (for the braiding) and then a third delooping $B^3 Line(\mathcal{C})$ (for the symmetry), regarded as a [[pointed homotopy type]].

This way we have rephrased the question equivalently as a question about the possible [[k-invariants]] of spaces of this form.

Now in the case at hand, $Line(Vect^{\mathbb{Z}/2})$ has precisely two [[isomorphism classes]] of objects, namely the [[ground field]] $k$ itself, regarded as being in even degree and regarded as being in odd degree. We write $k^{1\vert 0}$ and $k^{0 \vert 1}$ for these, respectively. By the rules of the tensor product of [[graded vector spaces]] we have

$$
  k^{1\vert 0} \otimes_k k^{1\vert 0} \simeq k^{1\vert 0}
$$

$$
  k^{1\vert 0} \otimes_k k^{0\vert 1} \simeq k^{0\vert 1}
$$

and

$$
  k^{0 \vert 1} \otimes_k^{0 \vert 1} \simeq k^{1 \vert 0}
  \,.
$$

In other words

$$
  \pi_0(Line(Vect^{\mathbb{Z}/2})) \simeq \mathbb{Z}/2
  \,.
$$

Now under the above homotopical identification the non-trivial braiding is identified with the elements

$$
  1 =
  k^{1 \vert 0} 
     \simeq 
  k^{0\vert 1} \otimes_k k^{0 \vert 1}
    \stackrel{\tau^{super}_{k^{0\vert 1}, k^{0 \vert 1}}}{\longrightarrow}
  k^{0\vert 1} \otimes_k k^{0\vert 1}
    \simeq
  k^{1 \vert 0}
  = 1  
$$

Due to the symmetry condition, 

$$
  (\tau^{super}_{k^{0\vert 1}, k^{0 \vert 1}})^2 = id
$$

and hence 

$$
  \tau^{super}_{k^{0\vert 1}, k^{0 \vert 1}}
  \in 
  \{+ id, -id\}
  \,.
$$

Therefore for classifying just the symmetric braidings, it is sufficient to restrict the [[hom-spaces]] in $Line(Vect^{\mathbb{Z}/2})$ from being either $k$ or empty, to [[hom-sets]] being $\mathbb{Z}/2 = \{+1-1\} \hookrightarrow k$ or empty. Write $\widetilde{Line}(sVect)$ for the resulting [[2-group]].

In conclusion then the [[equivalence classes]] of possible [[k-invariants]] of $B^3 Line(sVect)$, hence the possible symmetric braiding on $Line(Vect^{\mathbb{Z}/2})$ are in the degree-4 [[ordinary cohomology]] of the [[Eilenberg-MacLane space]] $K(\mathbb{Z}/2,3)$ with [[coefficients]] in $\mathbb{Z}/2$. One finds (...)


$$
  H^4(K(\mathbb{Z}/2, 3), \mathbb{Z}/2)
  \;\simeq\;
  \mathbb{Z}/2
  \,.
$$


=--


+-- {: .num_defn #CategoryOfSuperVectorSpaces} 
###### Definition

The [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) 

* whose underlying [[monoidal category]] is that of $\mathbb{Z}/2$-[[graded vector spaces]] (example \ref{Z2Zgradedvectorspaces});

* whose [[braiding]] (def. \ref{BraidedMonoidalCategory}) is the unique non-trivial symmtric grading $\tau^{super}$ from prop. \ref{TheTwoNontrivialBraidingsOnZ2GradedVectorSpaces} is called the **[[category of super vector spaces]]**

$$
  sVect_k 
    \;\coloneqq\;
  (Vect_k^{\mathbb{Z}/2}, \otimes = \otimes_k, 1 = k, \tau = \tau^{super} )
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The non-full symmetric monoidal subcategory

$$
  (\widetilde{Line}(sVect), \otimes_k, k, \tau^{super})
$$

of 

$$
  (Line(sVect) , \otimes_k, k, \tau^{super}) 
    \hookrightarrow
  (sVect, \otimes_k, k, \tau^{super})
$$

(on the two objects $k^{1\vert 0} $ and $k^{0\vert 1}$ and with [[hom-sets]] restricted to $\{+1,-1\} \subset k$, as in the proof of prop. \ref{TheTwoNontrivialBraidingsOnZ2GradedVectorSpaces}) happens to be the [[truncated object of an (infinity,1)-category|1-truncation]] of the [[looping]] of the [[sphere spectrum]] $\mathbb{S}$, regarded as a group-like [[E-infinity space]] ("[[abelian infinity-group]]")

$$
  (\widetilde{Line}(sVect), \otimes, k, \tau^{super})
  \;\simeq\;
  \tau_1 \Omega \mathbb{S}
  \,.
$$

It has been suggested (in [Kapranov 15](super+algebra#Kapranov15)) that this and other phenomena are evidence that in the wider context of [[homotopy theory]]/[[stable homotopy theory]] super-grading (and hence [[superalgebra]]) is to be regarded as but a shadow of grading in [[higher algebra]] over the [[sphere spectrum]]. Notice that the [[sphere spectrum]] is just the analog of the group of [[integers]] in [[stable homotopy theory]].

=--

We now discuss one more extra property on monoidal categories

+-- {: .num_defn #DualizableObject}
###### Definition

Let $(\mathcal{C},\otimes, 1)$ be a [[monoidal category]] (def. \ref{MonoidalCategory})

Then right **[[duality]]** between objects $A, A^\ast \in (\mathcal{C}, \otimes, 1)$

consists of

1. a [[morphism]] of the form

   $$
     ev_A\;\colon\;A^\ast \otimes A \longrightarrow 1
   $$

   called the _counit_ of the duality, or the _[[evaluation]] map_;

1. a [[morphism]] of the form

   $$
     i_A \;\colon\; 1 \longrightarrow A \otimes A^\ast
   $$

   called the _unit_ or _coevaluation map_

such that

* ([[triangle identity]]) the following [[commuting diagram|diagrams commute]]

  $$
    \array{
       A^\ast \otimes (A \otimes A^\ast)
         &\overset{id_{A^\ast} \otimes i_A}{\longleftarrow}&
       A^\ast \otimes 1
       \\
       {}^{\mathllap{\alpha^{-1}_{A^\ast,A, A^\ast}}}_{\mathllap{\simeq}}\downarrow
       &&
       \downarrow^{\mathrlap{\ell^{-1}_A \circ r_A}}_{\mathrlap{\simeq}}
       \\
       (A^\ast \otimes A) \otimes A^\ast
         &\underset{ev_A \otimes id_{A^\ast}}{\longrightarrow}&
       1 \otimes A^\ast
    }
  $$

  and

  $$
    \array{
       (A \otimes A^\ast)  \otimes A
         &\overset{i_A \otimes id_A}{\longleftarrow}&
       1 \otimes A
       \\
       {}^{\mathllap{\alpha_{A,A^\ast, A}}}_{\mathllap{\simeq}}\downarrow
       &&
       \downarrow^{\mathrlap{r_A^{-1}\circ \ell_A}}_{\mathrlap{\simeq}}
       \\
       A \otimes (A^\ast \otimes A)
         &\underset{id_A \otimes ev_A}{\longrightarrow}&
       A \otimes 1
    }
  $$

  where $\alpha$ denotes the [[associator]] of the [[monoidal category]] $\mathcal{C}$, and $\ell$ and $r$ denote the left and right [[unitors]], respectively.

We say that $A^\ast$ is the right [[dual object]] to $A$. Similarly a left dual for $A$ is an object $A^\ast$ and the structure of $A$ as a right dual of $A^\ast$. If $(\mathcal{C}, \otimes, 1)$ is equipped with the structure of a [[braided monoidal category]], then every right dual is canonically also a left dual.

If in a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ every object has a left and right dual, then it is called a **[[rigid monoidal category]]**.

=--


+-- {: .num_example #FiniteDimensionalVectorSpaces}
###### Example

Let 

$$
  FinVect_k \hookrightarrow Vect_k
$$

be the [[full subcategory]] of that of all [[vector spaces]] (over the given [[ground field]] $k$) on those which are **[[finite dimensional vector spaces]]**.

Clearly the [[tensor product of vector spaces]] (def. \ref{TensorProductOfVectorSpaces}) restricts to those of [[finite number|finite]] [[dimension]], and so there is the induced [[monoidal category]] structure from example \ref{VectAsAMonoidalCategory}

$$
  (FinVect_k, \otimes = \otimes_k, 1 = k )
   \hookrightarrow
  (Vect_k, \otimes_k, k)
  \,.
$$

This is a a [[rigid monoidal category]] (def. \ref{DualizableObject}) in that for $V$ any [[finite dimensional vector spaces]], its ordinary linear [[dual vector space]] 

$$
  V^\ast \coloneqq hom(V,k)
$$

is a  [[dual object]] in the abstract sense of def. \ref{DualizableObject}. 

Here the evaluation map is literally the defining [[evaluation]] map of linear duals (whence the name of the abstract concept)

$$
  ev_{V} \;\colon\;  V^\ast \otimes_k V \simeq hom(V,k) \otimes_k k \overset{}{\longrightarrow} k
$$
$$
  ev
    \;\colon\;
  (V \stackrel{\phi}{\to} k, v)
  \;\;\mapsto \;\;
  \phi(v)
  \,.
$$

The co-evaluation map 

$$
  i_V
    \;\colon\;
  k \longrightarrow V \otimes V^\ast
$$

is the linear map that sends $1 \in k$ to $id_V \in End(V) \simeq V \otimes_k V^\ast$ under the canonical identification of $V \otimes_k V^\ast$ with the linear space of [[linear map|linear]] [[endomorphisms]] of $V$.

If we choose a [[linear basis]] $\{e_i\}$ for $V$ and a corresponding dual bases $\{e^i\}$ of $V^\ast$, then the evaluation map is given by

$$
  ev \;\colon\; (e^i, e_j) \mapsto e^i(e_j) =  \delta^i_j
$$

(with the [[Kronecker delta]] on the right) and the co-evaluation map is given by

$$
  1 \mapsto \underset{i}{\sum} (e_i,  e^i)
  \,.
$$

In this perspective the [[triangle identities]] are the statements that

$$
  \underset{j}{\sum} e^i(e_j) e^j = e^i
$$

and

$$
  \underset{j}{\sum} e_j e^j(e_i) = e_i
  \,.
$$

Physicists will recognize this as just the basic rules for [[tensor]] calculus in index-notation.

=--


+-- {: .num_example #FiniteDimensionalSuperVectorSpaces}
###### Example

Similarly, the full subcategory

$$
  (sFinVect, \otimes_k, k, \tau^{super})
    &#180;\hookrightarrow
  (sVect, \otimes_k, k, \tau^{super})
$$

of the [[symmetric monoidal category]] of [[super vector spaces]] from example \ref{CategoryOfSuperVectorSpaces}, on those of finite total dimension is a [[rigid monoidal category]].

Here we say that a [[super vector space]] $V$ has dimension $(p\vert q)$ its even part has dimension $p$ and its odd part has dimension $q$:

$$
  dim(V) = (p\vert q)
   \;\;\;
   \Leftrightarrow
   \;\;\;
  ( dim(V_{even}) = p \;\;\text{and}\;\;\;\; dim(V_{odd}) = q )
  \,.
$$

The [[dual object]] of such a finite dimensional super vector space is just the linear [[dual vector space]] as in example \ref{FiniteDimensionalVectorSpaces} with the evident grading:

$$
  V = V_{even} \oplus V_{odd}
  \;\;\;\; \Rightarrow
  \;\;\;\;
  V^\ast = (V_{even}^\ast) \oplus (V_{odd}^\ast)
  \,.
$$

=--


### Super-groups as super-Hopf algebras
  {#SuperGroupsAsSuperHopfAlgebras}

hence we may internalize definition of commutative Hopf algebra
into $sVect$...



## Statement
 {#Statement}

Throughout, let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).


### Tensor categories

There are slight variants of what people mean by a "[[tensor category]]". Here we mean precisely the following: 

+-- {: .num_defn #TensorCategory}
###### Definition

For $k$ an [[algebraically closed field]] of [[characteristic zero]], then a _$k$-[[tensor category]]_ $\mathcal{A}$ is an 

1. [[essentially small category|essentially small]]

1. [[abelian category|abelian]] 

1. [[rigid monoidal category|rigid]] (def. \ref{DualizableObject})

1. [[symmetric monoidal category|symmetric]] (def. \ref{SymmetricMonoidalCategory})

1. [[braided monoidal category|braided]] (def. \ref{BraidedMonoidalCategory}})

1. [[monoidal category]] (def. \ref{MonoidalCategory})

1. [[enriched category|enriched]] over $k$[[Mod]] = $k$[[Vect]] (i.e. $k$-linear), compatible with the [[Ab-enriched category|Ab-enrichment]] implied from [[abelian category|abelianness]] under $U \colon k Vect \to Ab$

such that 

1. the [[tensor product]] functor $\otimes \colon \mathcal{A} \times \mathcal{A} \longrightarrow \mathcal{A}$ is in both arguments separately

   1. $k Mod$-[[enriched functor|enriched]] (i.e. $k$-linear);

   1. [[exact functor|exact]]


1. $End(1) \simeq k$ (the [[endomorphism ring]] of the [[tensor unit]] coincides with $k$).

=--

([Deligne 02, 0.1](#Deligne02))

We consider now various types of size constraints on tensor categories. The main theorem (theorem \ref{TheTheorem} below) only assumes one of them (subexponential growth, def. \ref{SubexponentialGrowth}), but the others appear in the course of the proof of the theorem.

1. finiteness (def. \ref{FiniteTensorCategory})

1. finite $\otimes$-generation (def. \ref{FiniteTensorGeneration})

1. subexponential growth (def. \ref{SubexponentialGrowth})

Recall the concept of [[length of an object]] in an [[abelian category]], a generalization of the concept of [[dimension]] of a [[free module]]/[[vector space]]. 


+-- {: .num_defn #FiniteTensorCategory} 
###### Definition

A $k$[[tensor category]] (def. \ref{TensorCategory}) is called **finite** (over $k$) if 

1. There are only [[finite number|finitely many]] [[simple objects]] in $C$ (hence it is a [[finite abelian category]]), and each of them admits a [[projective presentation]]. 

1. Each object $a$ is of [[object of finite length|finite length]]; 

1. For any two [[objects]] $a$, $b$ of $C$, the [[hom-object]] ($k$-[[vector space]]) $\hom(a, b)$ has [[finite]] [[dimension]]; 

=--

+-- {: .num_example} 
###### Example

The category of [[finite dimensional vector spaces]] over $k$ is a finite tensor category according to def. \ref{FiniteTensorCategory}. It has a single isomorphism class of [[simple objects]], namely $k$ itself.

Also category of finite dimensional [[super vector spaces]] is a finite tensor category. This has two isomorphism classes of simple objects, $k = k^{1 \vert 0}$ regarded in even degree, and $k^{0\vert 1}$ regarded in odd degree.

=--


The following finiteness condition is useful in the proof of the main theorem, but not necessary for its statement (according to [Deligne 02, bottom of p. 3](#Deligne02)):

+-- {: .num_defn #FiniteTensorGeneration}
###### Definition

A $k$-[[tensor category]] (def. \ref{TensorCategory}) is called _finitely $\otimes$-generated_ if there exists an [[object]] $E \in \mathcal{A}$ such that every other object $X \in \mathcal{A}$ is a [[subquotient]] of a [[direct sum]] of [[tensor products]] $E^{\otimes^n}$, for some $n \in \mathbb{N}$:

$$
  \array{
    && \underset{i}{\oplus} E^{\otimes^{n_i}}
    \\
    && \downarrow
    \\
    X &\hookrightarrow& (\underset{i}{\oplus} E^{\otimes^{n_i}})/Q
  }
  \,.
$$

Such $E$ is called an _$\otimes$-generator_ for $\mathcal{A}$.

=--

([Deligne 02, 0.1](#Deligne02))


The following is the main size constraint needed in the theorem. Notice that it is a "mild" constraint at least in the intuitive sense that it states just a minimum assumption on the expected behaviour of dimension ([[length of an object|lengh]]) under tensor powers.

+-- {: .num_defn #SubexponentialGrowth}
###### Definition

A [[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) is said to have _subexponential growth_ if the [[length]] of tensor exponentials is no larger than the exponential of the length: for every [[object]] $X$ there exists a [[natural number]] $N_X$ such that $X$ is of [[length of an object|length]] at most $N_X$, and that also all [[tensor product]] powers of $X$ are of length bounded by the corresponding powers of $N_X$:

$$
  \underset{X \in \mathcal{A}}{\forall}
  \underset{N_X \in \mathbb{N}}{\exists}
  \underset{n \in \mathbb{N}}{\forall}
    \;\;
   length(X^{\otimes^n}) \leq (N_X)^n
  \,.
$$

=--

(e.g. [EGNO 15, def. 9.11.1](#EGNO15))

The evident example is the following:

+-- {: .num_example}
###### Example

The tensor category $k$[[FinVect]] of [[finite dimensional vector spaces]] has subexponential growth (def. \ref{SubexponentialGrowth}), for $N_X = dim(X)$ the [[dimension]] of a vector space $X$, we have

$$
  dim(X^{\otimes^n}) = (dim(X))^n
  \,.
$$

=--

Of coure the assumption of the existence of [[dual objects]] ([[rigid monoidal category|rigidity]]) in def. \ref{TensorCategory} is already a finiteness condition itself. The following construction lifts that condition:

+-- {: .num_prop #IndObjectsInATensorCategory} 
###### Proposition

Let $\mathcal{A}$ a [[tensor category]] (def. \ref{TensorCategory}), such that 

1. all [[object of finite length|objects have finite length]];

1. all [[hom spaces]] are of [[finite number|finite]] [[dimension]] over $k$

then for its [[category of ind-objects]] $Ind(\mathcal{A})$ the following holds

1. $Ind(\mathcal{A})$ is an [[abelian category]]

1. $\mathcal{A} \hookrightarrow Ind(\mathcal{A})$ is a [[full subcategory]] 

   1. which stable under forming [[subquotients]]

   1. such that that every [[object]] $X \in Ind(\mathcal{A})$ is the [[filtered colimit]] of those of its [[subobjects]] that are in $\mathcal{A}$;

1. $\Ind(\mathcal{A})$ inherits a [[tensor product]] by 

   $$
     \begin{aligned}
       X \otimes Y
         & \simeq 
       (\underset{\longrightarrow}{\lim}_i X_i)
       \otimes
       (\underset{\longrightarrow}{\lim}_i Y_i)
       \\
       & \simeq
       \underset{\longrightarrow}{\lim}_{i,j} (X_i \otimes X_j)
     \end{aligned}
   $$

   where $X_i,X_j \in \mathcal{A}$, by the above.

1. $Ind(\mathcal{A})$ satisfies all the axioms of def. \ref{TensorCategory} except that it fails to be [[essentially small category|essentially small]] and [[rigid category]]. In detail

   1. an object in $Ind(\mathcal{A})$ is [[dualizable object|dualizable]] precisely if it is in $\mathcal{A}$.

=--

### Fiber functors

The first step in exhibiting a given [[tensor category]] $\mathcal{A}$ as being a [[category of representations]] is to exhibit its objects as having an [[forgetful functor|underlying]] representation space, and then an [[action]] represented on that space. Hence a necessary condition on $\mathcal{A}$ is that there exists a [[forgetful functor]]

$$
   \omega \;\colon\; \mathcal{A} \longrightarrow \mathcal{V}
$$

to another [[tensor category]] of sorts, such that $\omega$ satisfies a list of properties, in particular it should be a [[symmetric monoidal functor|symmetric]] [[strong monoidal functor]].

Such functors are called _[[fiber functors]]_. The idea is that we think of $\mathcal{A}$ as a [[bundle]] over $\mathcal{V}$, and over each $V \in \mathcal{V}$ we find the [[fiber]] $\omega^{-1}(V)$ of that "bundle", consisting of all those objects in $\mathcal{A}$ whose underlying object in the given $V$.

The main point of [[Tannaka duality]] of tensor categories is the observation that if $\mathcal{A}$ is a [[category of representations]] of some [[group]] $G$, then $G$ also [[action|acts]] by [[automorphisms]] on that [[fiber functor]] (i.e. via [[natural isomorphisms]] of functors). In good cases then this may be turned around, and the full [[automorphism group]] of a fiber functor identified with the group $G$ for which the objects in its fibers are [[representations]], this is the process of [[Tannaka reconstruction]].

There are slight variants on what one requires of a fiber functor. For the present purpose we fix the following definition

+-- {: .num_defn #FiberFunctor} 
###### Definition

Let $\mathcal{A}$ and $\mathcal{T}$ be two $k$[[tensor categories]] (def. \ref{TensorCategory}) such that 

1. all [[object of finite length|objects have finite length]];

1. all [[hom spaces]] of [[finite number|finite]] [[dimension]] over $k$.

Let $R \in CMon(Ind(\mathcal{T}))$ be a [[commutative monoid in a symmetric monoidal category|in]] in the category of [[ind-objects]] in $\mathcal{T}$ (prop. \ref{IndObjectsInATensorCategory}).  

Then a **[[fiber functor]] on $\mathcal{A}$ over $R$** is a [[functor]]

$$
  \omega \;\colon\; \mathcal{A} \longrightarrow R Mod(Ind(\mathcal{T}))
$$ 

from $\mathcal{A}$ to the category of [[module objects]] over $R$ in the [[category of ind-objects]] $Ind(\mathcal{T})$ (def. \ref{IndObjectsInATensorCategory}), which is

1. a [[braided monoidal functor|braided]] [[strong monoidal functor]];

1. an [[exact functor]] in both variables.

If here $\mathcal{T} = $ [[sVect]], then this is called a **super fiber functor**.

=--

([Deligne 02, 3.1](#Deligne02))

+-- {: .num_prop #MonoidalTransformationBetweenFiberFunctorIsIso} 
###### Proposition

Ever [[monoidal natural transformation]] between two [[fiber functors]] (def. \ref{FiberFunctor}) is an [[isomorphism]] (i.e. a [[natural isomorphism]]).

=--

([Deligne 02, lemma 3.2](#Deligne02))


### Schur functors

A [[finite dimensional vector space]] $V$ has the property that a high enough [[alternating power]] of it vanishes $\wedge^n V = 0$, namely this is the case for all $n \gt dim(V)$, and hence this vanishing is just another reflection of the finiteness of the [[dimension]] of $V$. For a [[super vector space]] $V$ of degreewise finite dimension an analog statement is still true, but one needs to form not just alternating powers but also [[symmetric powers]] (prop. \ref{SchurFunctorAnnihilatingFiniteDimensionalSuperVectorSpace} below), in fact one needs to apply a generalization of both of these constructions, a _[[Schur functor]]_. 


The operation of forming [[symmetric powers]] and [[alternating powers]] makes sense in every [[tensor category]]. Moreover, these operations are the two extreme cases of the more general concept of [[Schur functors]]: Given any [[object]] $X$ and given any choice of [[irreducible representation]] $V_\lambda$ of the [[symmetric group]] $\Sigma_n$, then one consider the [[subobject]] $S_\lambda(X^{\otimes^n})$ of the $n$-fold [[tensor power]] that is [[invariant]] under this action.

The first step in the proof of the main theorem (theorem \ref{TheTheorem} below) is the proposition (prop. \ref{LengthOfObjectIsBounded} below) that all objects that have subexponential growth of length (def. \ref{SubexponentialGrowth}) are actually annihilated by some [[Schur functor]] for the [[symmetric group]]. 


+-- {: .num_defn #SchurFunctor}
###### Definition

For $(\mathcal{A},\otimes)$ a $k$-[[tensor category]] as in def.\ref{TensorCategory}, for $X \in \mathcal{A}$ an [[object]], for $n \in \mathbb{N}$ and $\lambda$ a [[partition]] of $n$, regarded as a [[Young diagram]] and hence as a [[representation]] of the [[symmetric group]] $V_\lambda$, say that the value of the [[Schur functor]] $S_\lambda$ on $X$ is 

$$
  \begin{aligned}
    S_{\lambda}(X) 
      & \coloneqq 
    (V_\lambda \otimes X^{\otimes_n})^{S_n}
    \\
    & = 
    \left(
      \frac{1}{n!}
      \underset{g\in S_n}{\sum}
      \rho(g)
    \right)
    \left(
      V_\lambda \otimes X^{\otimes_n}
    \right)
  \end{aligned}
$$

where

* $(-)^{S_n}$ is the subobject of [[invariants]];

* $S_n$ is the [[symmetric group]] on $n$ elements;

* $V_\lambda$ is the [[irreducible representation]] of $S_n$ corresponding to $\lambda$;

* $\rho$ is [[diagonal action]] of $S_n$ on $V_\lambda \otimes X^{\otimes_n}$, coming from the canonical [[permutation]] action on $X^{\otimes_n}$;

* $(-)^{S_n}$ denotes the subspace of [[invariants]] under the action $\rho$ 

* the second expression just rewrites the invariants as the image of all elements under [[group averaging]].

=--

([Deligne 02, 1.4](#Deligne02))

+-- {: .num_example}
###### Example

For $\lambda = (n)$, then $V_{(n)} = k$ equipped with the trivial action of the symmetric group. In this case the corresponding [[Schur functor]] (def. \ref{SchurFunctor}) forms the $n$th [[symmetric power]]

$$
  S_{(n)}(X) = Sym^n(X)
  \,.
$$

For the dual case where $\lambda = (1,1, \cdots, 1)$ then $V_{(1,1,\cdots, 1)} = k$ equipped with the action by multiplication with the [[signature of a permutation]] and the corresponding [[Schur functor]] forms the [[alternating power]]

$$
  S_{(1,1, \cdots, 1)}(X) = \wedge^n X
  \,.
$$

=--

+-- {: .num_prop #SchurFunctorAnnihilatingFiniteDimensionalSuperVectorSpace} 
###### Proposition

Let $V = V_{even} \oplus V_{odd}$ be a [[super vector space]] of degreewise finite dimension $d_{even}, d_{odd} \in \mathbb{N}$. Then there exists a [[Schur functor]] $S_\lambda$ (def. \ref{SchurFunctor}) that annihilated $V$:

$$
  S_\lambda(V) \simeq 0
  \,.
$$

Speicifically, this is the case precisely if the corresponding [[Young tableau]] $[\lambda]$ satifies

$$
  [\lambda] \subset \left\{ (i,j)\;\vert\; i \leq d_{even}, j \leq d_{odd} \right\}
  \,.
$$

=--

([Deligne 02, corollary 1.9](#Deligne02))

Generally:

+-- {: .num_prop #LengthOfObjectIsBounded}
###### Proposition

For [[tensor category]], then the following are equivalent:

1. it has subexponential growth (def. \ref{SubexponentialGrowth});

1. for every object $X$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, on $X$ vanishes: $S_\lambda(X) = 0$. 

=--

([Deligne 02, prop. 05](#Deligne02))




### Supergroups

+-- {: .num_defn #Supergroup}
###### Definition

An affine algebraic _[[supergroup]]_ $G$ is the [[formal dual]] of a [[super-commutative Hopf algebra]] $\mathcal{O}(G)$.

=--

We will just say "supergroup" for short in all of the following. We assume throughout that $\mathcal{O}(G)$ is a finitely generated $k$-algebra.

+-- {: .num_defn #ParityAutomorphism}
###### Definition

Given a [[superalgebra]] such as $\mathcal{O}(G)$, its _parity involution_ is the algebra [[automorphism]] which on homogeneously graded elements $a$ of degree $deg(a) \in \{even,odd\} = \mathbb{Z}/2\mathbb{Z}$ is multiplication by the degree

$$
  a \mapsto (-1)^{deg(a)}a
  \,.
$$

(e.g. [arXiv:1303.1916, 7.5](http://arxiv.org/abs/1303.1916)). On [[formal duals]] $G$ this induces correspondingly an involutive _parity automorphism_

$$
  par \colon G \stackrel{\simeq}{\longrightarrow} G
  \,.
$$ 

=--

It is convenient in the following to assume that parity involution is an [[inner automorphism]]:

+-- {: .num_defn #InnerParity}
###### Definition

An _inner parity_ of a [[supergroup]] $G$, def. \ref{Supergroup} is an element $\epsilon \in G_{even}$ (i.e. an algebra homomorphism $\mathcal{O}(G) \to k$), which is [[involution|involutive]] i.e. $\epsilon^2 = 1$ and such that its [[adjoint action]] on $G$ is the parity involution of def. \ref{ParityAutomorphism}.

=--

([Deligne 02, 0.3](#Deligne02))

+-- {: .num_example}
###### Example

For $G$ an ordinary (affine algebraic) group, regarded as a supergroup with trivial odd-graded part, then every element $\epsilon \in Z(G)$ in the [[center]] defines an inner parity, def. \ref{InnerParity}. 

=--

([Deligne 02, 0.4 i)](#Deligne02))

+-- {: .num_remark}
###### Remark

In this sense, specifying an involutive central element in an ordinary group is a faint shadow of genuine supergroup structure. In fact such pairs are being referred to as "supergroups" in ([M&#252;ger 06](#Mueger06)).

=--

Demanding the existence of inner parity is not actually a restriction of the theory:

+-- {: .num_example}
###### Example

For $H$ any supergroup, def. \ref{Supergroup}, and $\mathbb{Z}_2 = \{id,par\}$ acting on it by parity involution, def. \ref{ParityAutomorphism}  then the [[semidirect product]] $\mathbb{Z}_2 \ltimes G$ has inner parity, def. \ref{InnerParity}, given by $\epsilon \coloneqq par \in \mathbb{Z}_2 \hookrightarrow \mathbb{Z}_2 \ltimes G$.

=--

([Deligne 02, 0.4 ii)](#Deligne02))

### Representation categories

+-- {: .num_defn #Superrepresentation}
###### Definition

A _super-[[representation]]_ of a [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$, def. \ref{InnerParity}, is a [[linear representation]] of $G$ on a [[finite number|finite]] [[dimension|dimensional]] [[vector space]] $V$ over $k$ such that when $V$ is equipped with the grading by $\pm1$-[[eigenspaces]] of $\epsilon$, even/odd elements of $G$ act with even/odd parity on $V$.

=--

+-- {: .num_defn #Superrepresentation_Deligne_def}
###### Remark

In ([Deligne 02, p. 3, above 0.4)](#Deligne02)) a super-representation of a supergroup $G$ is defined in a different but equivalent way. The vector space $V$ is considered to come equipped a priori with a grading, making it a [[super vector space]], and the following conditions are required to hold:

1. even/odd elements of $G$ act with even/odd parity on $V$

1. in addition such that $\epsilon$ is taken to the parity endomorphism of $V$ (which is the identity on even graded vectors and multiplication with $(-1)$ on odd-graded vectors).
=--

The given definition \ref{Superrepresentation} is preferable to this one as it doesn't ask for extra [[structure]] on $V$ and then for a property relative to that structure. Also in the following example, one _naturally_ finds that the super vector space on which the ordinary group is represented contains no odd part, and is hence merely an ordinary vector space.

+-- {: .num_example}
###### Example

For $G$ an ordinary (affine algebraic) group regarded as a supergroup with trivial odd-graded part, and for $\epsilon = 1$ its neutral element taken as the inner parity, then $Rep(G,\epsilon)$ in the sense of def. \ref{Superrepresentation} is just the ordinary [[category of representations]] of $G$.

=--

([Deligne 02, 0.4 i)](#Deligne02))

+-- {: .num_prop #RegularTensorCategoriesOfSuperrepresentations}
###### Proposition

The super-[[representation category]] $Rep(G,\epsilon)$, def. \ref{Superrepresentation} of an algebraic [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$ is a $k$-[[tensor category]] (def. \ref{TensorCategory}) of subexponential growth (def. \ref{SubexponentialGrowth}).
 
=--

([Deligne 02, 1.21](#Deligne02))

Any finite dimensional [[faithful representation]] (which always exists, [prop.](faithful+representation#AlgebraicGroupHasFinDimFaithfulRepresentations)) serves as a generator ([prop.](faithful+representation#AnyFinDimRepOfAffineAlgebraicGroupOverFieldIsSubquotientsOfFaithfulRep)).

+-- {: .num_theorem #TheTheorem}
###### Theorem

Every $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}), of subexponential growth (def. \ref{SubexponentialGrowth}) is [[equivalence of categories|equivalent]] to a [[category of representations]] $Rep(G,\epsilon)$, according to example \ref{RegularTensorCategoriesOfSuperrepresentations}, for some [[supergroup]] $G$.

=--

([Deligne 02, theorem 0.6](#Deligne02))


## References

The theorem is due to

* {#Deligne02} [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

building on the more general work on [[Tannakian categories]]

* [[Pierre Deligne]], _[[Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp.111-195.

Review is in 

* {#Ostrik04} [[Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))

* {#EGNO15} [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], section 9.11 in _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))

Further discussion in view of the theory of [[triangular Hopf algebras]] is in 

* {#EtingofGelaki02} [[Pavel Etingof]], [[Shlomo Gelaki]], _The classification of finite-dimensional triangular Hopf algebras over an algebraically closed field of characteristic 0_ ([arXiv:0202258](http://de.arxiv.org/abs/math/0202258))


Tannaka duality for ordinary compact groups regarded as supergroups (hence equipped with "inner parity", def. \ref{InnerParity}, here just being an involutive central element) is discussed in# Back

* {#Mueger06} [[Michael Müger]], _Abstract Duality Theory for Symmetric Tensor $*$-Categories_ appendix ([pdf](http://www.math.ru.nl/~mueger/PDF/16.pdf)), in [[Hans Halvorson]],  _Algebraic quantum field theory_ ([arXiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036)), in J. Butterfield & J. Earman (eds.) _Handbook of Philosophy and Physics_ 

as a proof of [[Doplicher-Roberts reconstruction]]

[[!redirects Deligne theorem on tensor categories]]

[[!redirects Deligne reconstruction theorem]]