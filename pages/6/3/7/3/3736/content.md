

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

An object in a [[model category]] is fibrant if all morphisms into it have extensions along acyclic cofibrations. An **algebraic fibrant object** is a fibrant object equipped with a _choice_ of such extensions.

Under mild conditions, the category $Alg C$ of algebraic fibrant objects in a model category $C$ forms itself naturally a model category which is [[Quillen equivalence|Quillen equivalent]] to $C$, and in which all objects are fibrant.  Notably, $Alg C$ is always a [[category of fibrant objects]].


## Definition

+-- {: .un_defn}
###### Definition

Let $C$ be a [[cofibrantly generated model category]] such that 
all acyclic cofibrations are [[monomorphism]]s. 

Choose a set $\{A_j \to B_j\}_{j \in J}$ of acyclic cofibrations such that an object $X \in C$ is fibrant precisely if it has the [[right lifting property]] against these morphisms.

An **algebraic fibrant object** in $C$ is a fibrant object of $C$ together with a choice of lifts ("fillers") $\sigma_j : B_j \to X$ in

$$
  \array{
    A_j &\to& X
    \\
    \downarrow & \nearrow_{\mathrlap{\sigma_j}}
    \\
    B_j
  }
$$

for each morphism $A_j \to X$, $j \in J$. 

Write $ALg C$ for the category whose objects are algebraic fibrant objects in $C$ and whose morphisms are morphisms in $C$ that respect the chosen lifts.

=--

+-- {: .un_remark}
###### Remark

The set $J$ can always be taken to be that of all generating acyclic cofibrations. But often there are smaller subsets that still characterize all fibrant objects.

=--

+-- {: .un_theorem}
###### Theorem

The [[forgetful functor]] [[adjunction]]

$$
  (F \dashv U) : Alg C \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C 
$$

induces the [[transferred model structure]] on $Alg C$: the fibrations
and weak equivalences in $Alg C$ are those of the underlying morphisms in $C$.

In particular, every object in $Alg C$ is fibrant.

The [[Quillen adjunction]] $(F \dashv U)$ is a [[Quillen equivalence]].


=--


This is ([Nikolaus, theorem 2.18](#Nikolaus))

+-- {: .un_remark}
###### Remark

Since fibrations in $Alg C$ are created in $C$, and any algebraically fibrant object is, in particular, fibrant, every object in the model category $Alg C$ is fibrant.  Thus almost any model category is equivalent to one in which all objects are fibrant.  However, in general not all objects in $Alg C$ will be cofibrant, even if this was true in $C$ itself.

=--

## Details

### The left adjoint

We describe explicitly the [[left adjoint]] $F : C \to Alg C$. This follows [[Richard Garner]]'s improved version of the [[small object argument]] ([Garner](#Garner)).


For $X \in C$ define a new object $X_\infty$ inductively as follows.

+-- {: .un_defn}
###### Definition

$X_1$ is the [[pushout]] (in $C$) 

$$
  \array{
     \coprod A_j &\to& X
     \\
     \downarrow && \downarrow
     \\
     \coprod B_j &\to& X_1
  }
  \,,
$$

here the disjoint unition is taken over all $j$ and all morphisms $A_j \to X$.

=--

+-- {: .un_defn}
###### Remark

This pushout adds all possible "horn" fillers to $X$, given by the $B_j \to X_1$. However, after adding the new fillers there may also appear new horns. So we continue this procedure iteratively by filling these new horn.

Since $\coprod A_j \to \coprod B_j$ is an acylcic cofibration in $C$, so is its its pushout, hence by assumption the pushout $X \to X_1$ is a monomorphism. This implies that if an $A_j \to X_1$ factors through $X \to X_1$ then it does so uniquely.

=--

+-- {: .un_defn}
###### Definition

Let $X_2$ be the [[pushout]]

$$
  \array{
     \coprod A_j &\to& X_1
     \\
     \downarrow && \downarrow
     \\
     \coprod B_j &\to& X_2
  }
  \,,
$$

where now the coproduct is over those morphisms $A_j \to X$ that do _not_ factor throuth $X \to X_1$.

Proceeding this way yields a sequence of acyclic cofibrations

$$
  X \to X_1 \to X_2 \to X_3 \to \cdots 
  \,.
$$

We set

$$
  X_\infty :=  \lim_\to (X \to X_1 \to X_2 \to X_3 \to \cdots )
$$

be the [[colimit]] over this sequence.

=--

+-- {: .un_observation}
###### Observation

The object $X_\infty$ inherits canonical fillers: since by the assumption on a [[cofibrantly generated model category]] that all $A_j$ are [[small object]]s with respect to [[transfinite composition|transfinitite composites]] of pushouts of the generating cofibrations we have that every morphism $A_j \to X_\infty$ factors through one of the intermediate $X_i$. Then for any of the morphisms $A_j \to B_j$ in $J$ the corresponding morphism $B_j \to X_{i+1} \to X_\infty$ provides a filler. 

=--

+-- {: .un_prop}
###### Proposition

The assignment  $F : X \to X_\infty$ with $X_\infty$ regarded as an algebraic fibrant objects as above constitutes a left [[adjoint functor]] $F : C \to Alg C$ to the [[forgetful functor]] $U : Alg C \to C$.

The unit of this [[adjunction]] is the inclusion $X \to X_\infty$ given by the above construction and is hence a weak equivalence.

=--

+-- {: .proof}
###### Proof

We establish the hom-isomorphism of the [[adjunction]] and its construction by the unit of the adjunction: For any $Z \in Alg C$ and $\phi : X \to U(Z)$ any morphism in $C$, we need to show that there is a unique [[commuting diagram]]

$$
  \array{
    X &\stackrel{\phi}{\to}& Z
    \\
    \downarrow & \nearrow_{\exists ! \phi_\infty}
    \\
    X_\infty
  }
  \,.
$$

Since by assumption $Z$ has all fillers we have commuting diagrams

$$
  \array{
      A_j &\to& X 
     \\
     \downarrow && \downarrow^{\mathrlap{\phi}}
     \\
     B_j &\to& Z
  }
  \,.
$$

By the universality of the pushout these induce unique morphisms 

$$
  \array{
    X &\stackrel{\phi}{\to}& Z
    \\
    \downarrow & \nearrow_{\phi_1 }
    \\
    X_1
  }
  \,.
$$

By induction this induces morphisms $\phi_n : X_n \to Z$ that form a [[cocone]] under $(X \to X_1 \to X_2 \to \cdots )$. Therefore there is a unique morphusm $\phi_\infty$ as indicated.

=--

+-- {: .un_corollary}
###### Corollary

The morphisms $F(j) : F A_j \to F B_j$ have [[retract]]s.

=--


+-- {: .proof}
###### Proof

Since $F$ is [[left adjoint]] to $U$ the condition that $F A_j \to F B_j \stackrel{r}{\to} F A_j$ is the [[identity]] is equivalent to its [[adjunct]], the diagonal in

$$
  \array{
    A_j &\stackrel{j}{\to}& B_j &\stackrel{r}{\to}& A_j
    \\
    \downarrow && \downarrow &\searrow^{\mathrlap{\tilde r}}& \downarrow
    \\
    U F A_j &\stackrel{U F (j)}{\to}& U F B_j &\stackrel{U F r}{\to} & U F A_j
  }
$$

being the unit of the adjunction $A_j \to U F A_j$. Take $\tilde r$ to be the (unique) filler for this morphism.

=--

### Monadicity

We now give a formal justification for calling the objects of $Alg C$ _algebraic_ objects by showing that $Alg C$ is the category of algebras over an [[algebraic theory]] in $C$, or more precisely that it is the category of [[algebras over a monad|algebra over the monad]] $F \circ U$ on $C$ 

+-- {: .un_theorem}
###### Theorem

The functor $U : Alg C \to C$ is [[monadic]].

=--

This is ([Nikolaus, prop. 24](#Nikolaus))


+-- {: .proof}
###### Proof

(...)

=--
## Examples

### Algebraic $\infty$-groupoids {#AlgebaicHigherCategories}

The standard [[model structure on simplicial sets]] $sSet_{Quillen}$ models the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoid]]s: its fibrant objects are precisely the [[Kan complex]]es. But a Kan complex is a model for an $\infty$-groupoid in which composites and inverses of [[k-morphism]]s are only guaranteed to exist, but are not specifically _chosen_ .

An algebraic fibrant object in $sSet_{Quillen}$ is a [[Kan complex]] with a chosen filler for each [[horn]]: an **[[algebraic Kan complex]]** (see [[simplicial T-complex]] for a related but much stricter notion). This means precisely that all possible composites and all possible inverses are chosen. So the Quillen equivalence

$$
  sSet_{Quillen} \stackrel{\leftarrow}{\to} Alg sSet_{Quillen} 
$$

induces an equivalence from an [[algebraic definition of higher category|algebraic definition of ∞-groupoids]] to a [[geometric definition of higher categories|geometric definition]].

### Algebraic $(\infty,1)$-categories

Similarly, the [[model structure for quasi-categories]] $sSet_{Joyal}$ models [[(∞,1)-categories]]: its fibrant objects are precisely the [[quasi-categories]]: an **[[algebraic quasi-category]]**. Again, these form a model for $(\infty,1)$-categories in which composition is only a relation, not an operation.

But equipping a quasi-category with the structure of an algebraic fibrant object precisely means choosing such composites. Accordingly, the [[Quillen equivalence]]

$$
  sSet_{Joyal} \stackrel{\leftarrow}{\to} Alg sSet_{Joyal} 
$$

establishes an equivalence of an algebraic with the standard geometric model for $(\infty,1)$-categories.


## References

The model structure on algebraic fibrant objects was introduced and discussed in

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))
{#Nikolaus}

A survey is in

* [[Thomas Nikolaus]] Talk on _Algebraic models for higher categories_ ([here](http://www.math.uni-hamburg.de/home/nikolaus/AlgMod.pdf))

The refined [[small object argument]] that is being used in the construction of the left adjoint $F : C \to Alg C$ is along the lines of the discussion in

* [[Richard Garner]], _Understanding the small object argument_ Applied Categorical Structures, 17(3):247&#8211;285, 2009 ([pdf](http://www.dpmms.cam.ac.uk/~rhgg2/CT07/CT07.pdf))
{#Garner}