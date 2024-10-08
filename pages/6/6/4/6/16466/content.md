
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

_Deligne's theorem on tensor categories_ ([Deligne 02](#Deligne02), recalled as theorem \ref{TheTheorem} below) establishes [[Tannaka duality]] between 

1. linear [[tensor categories]] in [[characteristic zero]] subject to just a mild size constraint (subexponential growth, def. \ref{SubexponentialGrowth} below), 

1. [[supergroups]] ("[[supersymmetries]]"), realizing these tensor categories as [[categories of representations]] of these supergroups.

As explained [[[tensor categories|there]], by tensor category we assume a symmetric braiding.


## Relevance

### For supersymmetry
 {#RelevanceForSupersymmetry}

Since the concept of linear [[tensor categories]] arises very naturally in [[mathematics]], the theorem gives a purely mathematical "reason" for the relevance of [[superalgebra]] and [[supergeometry]]. It is reasonable to wonder why of all possible generalizations of [[commutative algebra]], it is [[supercommutative superalgebras]] that are singled out (from alternatives such as plain $\mathbb{Z}/2$-[[graded algebras]], or in fact $\mathbb{Z}/n$-graded algebras or general [[noncommutative algebras]] or the like), as they are notably in theoretical [[physics]] ("[[supersymmetry]]"), but also in mathematical fields such as [[spin geometry]] (e.g. via the relation between [[Majorana spinors]] and supersymmetry, [here](Majorana+spinor#Supersymmetry)) and [[topological K-theory]] (for instance via its incarnation as _[[Karoubi K-theory]]_, or via the descriptioon of [[twisted K-theory]] by _[[super line 2-bundles]]_).

But with $k$-linear [[tensor categories]] appearing on general abstract grounds as the canonical structure to consider in [[representation theory]], Deligne's theorem serves to base supercommutative superalgebra on this same general abstract foundation, showing that this is precisely the context in which full $k$-linear tensor categories exhibit full [[Tannaka duality]].

More concretely, in [[quantum field theory]], under the [[Wigner classification]], [[fundamental particles]] are identified with [[irreducible representations]] of the [[isometry group]] of the local model of [[spacetime]] (which are induced from [[finite dimensional vector space|finite dimensional]] representations of the "[[Wigner classification|Wigner's]] [[little group]]" ([Mackey 68](Wigner+classification#Mackey68)) ). Forming the [[tensor product]] of two such representations corresponds to combining them as two [[subsystems]] of a joint system. Therefore it is natural to demand that physical particle species should form complex-linear [[tensor categories]]. Deligne's theorem then gives that [[supersymmetry]] is the most general context in which this works out. (In physics the irreducible representation in this context here are called the _[[supermultiplets]]_.)

More exposition of this point is at:

* PhysicsForums Insights, _[Supersymmetry and Deligne's theorem](https://www.physicsforums.com/insights/supersymmetry-delignes-theorem/)_


### For Tannaka duality of Hopf algebras
 {#RelevanceForHopfAlgebras}

By [[Tannaka duality]], [[rigid monoidal category|rigid]] [[symmetric monoidal categories]] in general are [[categories of modules]] of [[triangular Hopf algebras]]. Hence Deligne's theorem here implies that those triangular Hopf algebras over [[algebraically closed fields]] of [[characteristic zero]] whose category of representation has subexponential growth (def. \ref{SubexponentialGrowth} below) are equivalent to [[supercommutative Hopf algebras]]. See ([Etingof-Gelaki 02](#EtingofGelaki02)) for more.

[[!include structure on algebras and their module categories - table]]


## Background

This section provides exposition of the necessary background for the statement of Deligne's theorem (theorem \ref{TheTheorem} below).

We start by introducing the basic concepts of [[tensor categories]] along with the basic examples of [[vector spaces]] and [[super vector spaces]]:

* _[Tensor categories](#TensorProductsAndMonoidalCategories)_

This allows to speak of [[commutative algebra]] [[internalization|internal]] to tensor categories. Specializing this to the tensor category of [[super vector spaces]] yields [[supercommutative superalgebras]]. The [[formal duals]] of these are the [[affine variety|affine]] [[super schemes]]. This we discuss in

* _[Commutative algebra in tensor categories and Affine super-spaces](#CommutativeAlgebraInTensorCategories)_

Next we introduce the concept of [[commutative monoids]] equipped with the structure of a [[commutative Hopf algebras]] and explain how these are [[formal duals]] to [[group objects|groups]]. Then we use this to motivate and explain the concept of (affine algebraic) [[supergroups]] as [[formal duals]] to [[commutative Hopf algebras]] internal to the tensor category of [[super vector spaces]], namely [[supercommutative Hopf algebras]]:

* _[(Super-)Groups as (Super-)commutative Hopf algebras](#GroupsAsHopfAlgebras)_

Finally we discuss how under this relation [[linear representations]] of groups correspond to [[comodules]] over their formally dual [[commutative Hopf algebras]], and we introduce the key class of categories of interest here: tensor-[[categories of representations]] of groups and of super-representations of super-groups:

* _[Linear representations as comodules](#LinearRepresentationsAsComodules)_







### Tensor products and Super vector spaces
 {#TensorProductsAndMonoidalCategories}

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

1. Say that $\mathcal{C}$ has **[[direct sums]]** if it has [[finite products]] and [[finite coproducts]] and if the canonical comparison  morphism between these is an [[isomorphism]]. We write $V \oplus W$ for the direct sum of two objects of $\mathcal{C}$.

1. Say that $\mathcal{C}$ is an **[[additive category]]** if it has [[direct sums]] and in addition it is [[Ab-enriched category|enriched in abelian groups]], meaning that every [[hom-set]] is equipped with the structure of an [[abelian group]] such that [[composition]] of morphisms is a [[bilinear map]].

1. Say that $\mathcal{C}$ is an **[[abelian category]]** if it is an [[additive category]] and has property that its [[monomorphisms]] are precisely the inclusions of [[kernels]] and its [[epimorphisms]] are precisely the projections onto [[cokernels]].

=--

We also make the following definition of $k$-linear category, but notice that conventions differ as to which extra properties beyond [[Vect]]-[[enriched category|enrichment]] to require on a linear category:


+-- {: .num_defn #LinearCategory}
###### Definition

For $k$ a [[field]] (or more generally just a [[commutative ring]]), call a [[category]] $\mathcal{C}$ a **$k$-[[linear category]]** if

1. it is an [[abelian category]] (def. \ref{AdditiveAndAbelianCategories});

1. its [[hom-sets]] have the structure of $k$-[[vector spaces]] (generally $k$-[[modules]]) such that [[composition]] of morphisms in $\mathcal{C}$ is a [[bilinear map]]

and the underlying additive [[abelian group]] structure of these [[hom-spaces]] is that of the underlying [[abelian category]].

In other words, a $k$-linear category is an [[abelian category]] with the additional structure of a [[Vect]]-[[enriched category]] (generally $k$[[Mod]]-enriched) such that the underlying [[Ab-enriched category|Ab-enrichment]] according to def. \ref{AdditiveAndAbelianCategories} is obtained from the $Vect$-enrichment under the [[forgetful functor]] $Vect \to Ab$.

A [[functor]] between $k$-linear categories is called a **$k$-[[linear functor]]** if its component functions on [[hom-sets]] are [[linear maps]] with respect to the given $k$-linear structure, hence if it is a [[Vect]]-[[enriched functor]].

=--

+-- {: .num_example}
###### Example

The category [[Vect]]${}_k$ of [[vector spaces]] (def. \ref{VectorSpaces}) is a $k$-[[linear category]] according to def. \ref{LinearCategory}.

Here the abstract [[direct sum]] is the usual direct sum of [[vector spaces]], whence the name of the general concept.

For $V,W$ two $k$-vector spaces, the vector space structure on the [[hom-set]] $Hom_{Vect}(V,W)$ of [[linear maps]] $\phi \colon V \to W$ is given by "pointwise" multiplication and addition of functions:

$$
  (c_1 \phi_1 + c_2 \phi_2)
  \;\colon\,
   v \;\mapsto\;
   c_1 \phi_1(v) + c_2 \phi_2(v)
$$

for all $c_1, c_2 \in k$ and $\phi_1, \phi_2 \in Hom_{Vect}(V,W)$.


=--

Recall the basic construction of the [[tensor product of vector spaces]]:

+-- {: .num_defn #TensorProductOfVectorSpaces}
###### Definition

Given two [[vector spaces]] over some [[field]] $k$,  $V_1, V_2 \in Vect_k$, their [[tensor product of vector spaces]] is the vector space denoted

$$
  V_1 \otimes_k V_2 \;\in\; Vect
$$

whose elements are [[equivalence classes]] of  [[tuples]] of elements $(v_1,v_2)$ with $v_i \in V_i$, for the [[equivalence relation]] given by

$$
  (c v_1 , v_2) \;\sim\; (v_1, c v_2)
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

The existence of the [[tensor product of vector spaces]], def. \ref{TensorProductOfVectorSpaces}, equips the category [[Vect]] of vector spaces with extra structure, which is a "[[categorification]]" of the familiar structure of a [[semi-group]]. One also says "[[monoid]]" for [[semi-group]] and therefore [[categories]] equipped with a [[tensor product]] operation are also called  _[[monoidal categories]]_:


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

* the abstract [[tensor product]] is the [[tensor product of vector spaces]] $\otimes_k$ from def. \ref{TensorProductOfVectorSpaces};

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

This defines a [[category]], denoted $Vect^G$. Equip this category with a [[tensor product]] which on the underlying vector spaces is just the [[tensor product of vector spaces]] from def. \ref{TensorProductOfVectorSpaces}, equipped with the $G$-grading which is obtained by multiplying degree labels in $G$:

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
      0 & | otherwise
    }
  \right.
  \,.
$$

The [[associator]] and [[unitors]] are just those of the monoidal structure on plain vector spaces, from example \ref{VectAsAMonoidalCategory}.

=--

One advantage of abstracting the concept of a [[monoidal category]] is that it allows to prove general statements uniformly for all kinds of tensor products, familar ones and more exotic ones. The following lemma \ref{kel1} and remark \ref{CoherenceForMonoidalCategories} are two important such statements.

+-- {: .num_lemma #kel1}
###### Lemma
**([Kelly 64](#Kelly64))**

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

(Here the qualifier "freely" means informally that we must not use any non-formal identification between objects, and formally it means that the diagram in question must be in the image of a [[strong monoidal functor]] from a _free_ monoidal category. For example if in a particular monoidal category it so happens that the object $X \otimes (Y \otimes Z)$ is actually _equal_ to $(X \otimes Y)\otimes Z$, then the various ways of going from one expression to another using only associators _and_ this "accidental" equality no longer need to coincide.)

=--

The above discussion makes it clear that a [[monoidal category]] is like a [[monoid]]/[[semi-group]], but "[[categorified]]". Accordingly we may consider additional properties of [[monoids]]/[[semi-groups]] and correspondingly lift them to monoidal categories. A key such property is _[[commutative ring|commutativity]]_. But while for a monoid commutativity is just an extra [[property]], for a [[monoidal category]] it involves choices of commutativity-[[isomorphisms]] and hence is [[stuff, structure and property|extra structure]].
We will see [below](#SuperGroupsAsSuperHopfAlgebras) that this is the very source of [[superalgebra]].

The [[categorification]] of "commutativity" comes in two stages: [[braiding]] and [[symmetric monoidal category|symmetric braiding]].

+-- {: .num_defn #BraidedMonoidalCategory}
###### Definition

A **[[braided monoidal category]]**, is a [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]]

$$
  \tau_{x,y} \;\colon\; x \otimes y \to y \otimes x
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

between then summands in even degree and in odd degree, respectively:

$$
  f = f_{even} \oplus f_{odd}
  \,.
$$

The [[tensor product]] of $\mathbb{Z}/2$-graded vector space is the [[tensor product of vector spaces]] of the underlying vector spaces, but with the grading obtained from multiplying the original gradings in $\mathbb{Z}/2$. Hence

$$
  (V_1 \otimes V_2)_{even}
    \;\coloneqq\;
  \left((V_1)_{even} \otimes (V_2)_{even}\right)
    \oplus
  \left((V_1)_{odd} \otimes (V_2)_{odd}\right)
$$

and

$$
  (V_1 \otimes V_2)_{odd}
    \;\coloneqq\;
  \left((V_1)_{even} \otimes (V_2)_{odd}\right)
    \oplus
  \left((V_1)_{odd} \otimes (V_2)_{even}\right)
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


on the [[monoidal category]] $(Vect_k^{\mathbb{Z}/2}, \otimes_k)$ of $\mathbb{Z}/2$-[[graded vector spaces]] from def. \ref{Z2Zgradedvectorspaces}:

1. the **trivial braiding** which is the [[natural transformation|natural]] [[linear map]] given on tuples $(v_1,v_2)$ representing an element in $V_1 \otimes V_2$ (according to def. \ref{TensorProductOfVectorSpaces}) by

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

for the [[full subcategory]] on those $L \in \mathcal{C}$ which are [[invertible objects]] under the [[tensor product]], i.e. such that there is an object $L^{-1} \in \mathcal{C}$ with $L \otimes L^{-1} \simeq 1$ and $L^{-1} \otimes L \simeq 1$. Since the [[tensor unit]] is clearly in $Line(L)$ (with $1^{-1} \simeq 1$) and since with $L_1, L_2 \in Line(\mathcal{C}) \hookrightarrow \mathcal{C}$ also $L_1 \otimes L_2 \in Line(\mathcal{C})$ (with $(L_1 \otimes L_2)^{-1} \simeq L_2^{-1} \otimes L_1^{-1}$) the [[monoidal category]] structure on $\mathcal{C}$ restricts to $Line(\mathcal{C})$.


Accordingly any [[braiding]] on $(\mathcal{C}, \otimes,1)$ restricts to a braiding on $(Line(\mathcal{C}), \otimes, 1)$. Hence it is sufficient to show that there is an essentially unique non-trivial symmetric braiding on $(Line(\mathcal{C}), \otimes, 1)$, and that this is the restriction of a braiding on $(\mathcal{C}, \otimes, 1)$.

Consider furthermore the [[groupoid]] [[core]] (non-[[full subcategory|full]] [[subcategory]] including all the [[isomorphisms]])

$$
  Line(\mathcal{C}, \otimes , 1)_{iso}
  \;\in\;
  2 Grp
$$  

The [[tensor product]] now makes this a  _[[2-group]]_, known as the "[[Picard groupoid of a monoidal category|Picard groupoid]]" of $\mathcal{C}$. As such we may regard it equivalently as a [[homotopy 1-type]] with group structure, and as such it it is equivalent to its [[delooping]]

$$
  B_\otimes Line(\mathcal{C})_{iso}
$$


regarded as a [[pointed homotopy type]]. (See at _[[looping and delooping]]_).

The [[Grothendieck group]] of $(\mathcal{C}, \otimes, 1)$ is

$$
  \pi_0(Line(\mathcal{C})_{iso})
    \simeq
  \pi_1(B Line(\mathcal{C})_{iso})
$$

the [[fundamental group]] of the delooping space.

Now a symmetric braiding on $Line(\mathcal{C})_{iso}$ is precisely the structure that makes it a [[symmetric 2-group]] which is equivalently the structure of a second [[delooping]] $B^2 Line(\mathcal{C})$ (for the braiding) and then a third delooping $B^3 Line(\mathcal{C})$ (for the symmetry), regarded as a [[pointed homotopy type]].

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
  k^{0 \vert 1} \otimes_k k^{0 \vert 1} \simeq k^{1 \vert 0}
  \,.
$$

In other words

$$
  \pi_0(Line(Vect^{\mathbb{Z}/2})_{iso}) \simeq \mathbb{Z}/2
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

Due to the [[symmetric monoidal category|symmetry]] condition (def. \ref{SymmetricMonoidalCategory}) we have

$$
  (\tau^{super}_{k^{0\vert 1}, k^{0 \vert 1}})^2 = id
$$

which implies that

$$
  \tau^{super}_{k^{0\vert 1}, k^{0 \vert 1}}
  \in
  \{+ id, -id\}
  \,.
$$

Therefore for classifying just the symmetric braidings, it is sufficient to restrict the [[hom-spaces]] in $Line(Vect^{\mathbb{Z}/2})$ from being either $k$ or empty, to [[hom-sets]] being $\mathbb{Z}/2 = \{+1-1\} \hookrightarrow k$ or empty. Write $\widetilde{Line}(Vect^{\mathbb{Z}/2})$ for the resulting [[2-group]].

In conclusion then the [[equivalence classes]] of possible [[k-invariants]] of $B^3 Line(Vect^{\mathbb{Z}/2})$, hence the possible symmetric braiding on $Line(Vect^{\mathbb{Z}/2})$ are in the degree-4 [[ordinary cohomology]] of the [[Eilenberg-MacLane space]] $K(\mathbb{Z}/2,3)$ with [[coefficients]] in $\mathbb{Z}/2$. One finds (...)


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
  \trunc_1 \Omega \mathbb{S}
  \,.
$$

It has been suggested (in [Kapranov 15](super+algebra#Kapranov15)) that this and other phenomena are evidence that in the wider context of [[homotopy theory]]/[[stable homotopy theory]] super-grading (and hence [[superalgebra]]) is to be regarded as but a shadow of grading in [[higher algebra]] over the [[sphere spectrum]]. Notice that the [[sphere spectrum]] is just the analog of the group of [[integers]] in [[stable homotopy theory]].

=--



The following is evident but important

+-- {: .num_defn #InclusionOfVectorSpacesIntoSupervectorSpaces}
###### Proposition

The canonical inclusion

$$
  Vect_k \hookrightarrow sVect_k
$$

of the category of vector spaces (def. \ref{VectorSpaces}) into that of
[[super vector spaces]] (def. \ref{CategoryOfSuperVectorSpaces}) given by
regarding a vector space as a super-vector space concentrated in even degree,
extends to a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}).

=--

+-- {: .num_defn #ClosedMonoidalCategory}
###### Definition

Given a [[symmetric monoidal category]] $\mathcal{C}$ with [[tensor product]] $\otimes$ (def. \ref{SymmetricMonoidalCategory}) it is called a **[[closed monoidal category]]** if for each $Y \in \mathcal{C}$ the functor $Y \otimes(-)\simeq (-)\otimes Y$ has a [[right adjoint]], denoted $hom(Y,-)$

$$
  \mathcal{C}
    \underoverset
      {\underset{hom(Y,-)}{\longrightarrow}}
      {\overset{(-) \otimes Y}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,,
$$

hence if there are [[natural bijections]]

$$
  Hom_{\mathcal{C}}(X \otimes Y, Z)
   \;\simeq\;
  Hom_{\mathcal{C}}{C}(X, hom(Y,Z))
$$

for all objects $X,Z \in \mathcal{C}$.

Since for the case that $X = 1$ is the [[tensor unit]] of $\mathcal{C}$ this means that

$$
  Hom_{\mathcal{C}}(1,hom(Y,Z)) \simeq Hom_{\mathcal{C}}(Y,Z)
  \,,
$$

the object $hom(Y,Z) \in \mathcal{C}$ is an enhancement of the ordinary [[hom-set]] $Hom_{\mathcal{C}}(Y,Z)$ to an object in $\mathcal{C}$.
Accordingly, it is also called the **[[internal hom]]** between $Y$ and $Z$.

=--


In a [[closed monoidal category]], the adjunction isomorphism between [[tensor product]] and [[internal hom]] even holds internally:

+-- {: .num_prop #TensorHomAdjunctionIsoInternally}
###### Proposition

In a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) there are [[natural isomorphisms]]

$$
  hom(X \otimes Y, Z)
   \;\simeq\;
  hom(X, hom(Y,Z))
$$

whose image under $Hom_{\mathcal{C}}(1,-)$ are the defining [[natural bijections]] of def. \ref{ClosedMonoidalCategory}.

=--

+-- {: .proof}
###### Proof

Let $A \in \mathcal{C}$ be any object. By applying the defining natural bijections twice, there are composite natural bijections

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(A , hom(X \otimes Y, Z))
    & \simeq
    Hom_{\mathcal{C}}(A \otimes (X \otimes Y), Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}((A \otimes X)\otimes Y, Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}(A \otimes X, hom(Y,Z))
    \\
    & \simeq
    Hom_{\mathcal{C}}(A, hom(X,hom(Y,Z)))
  \end{aligned}
  \,.
$$

Since this holds for all $A$, the [[Yoneda lemma]] (the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]]) says that there is an isomorphism $hom(X\otimes Y, Z) \simeq hom(X,hom(Y,Z))$. Moreover, by taking $A = 1$ in the above and using the left [[unitor]] isomorphisms $A \otimes (X \otimes Y) \simeq X \otimes Y$ and $A\otimes X \simeq X$  we get a [[commuting diagram]]

$$
  \array{
    Hom_{\mathcal{C}}(1,hom(X\otimes Y, ))
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(1,hom(X,hom(Y,Z)))
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\mathcal{C}}(X \otimes Y, Z)
     &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(X, hom(Y,Z))
  }
  \,.
$$

=--

+-- {: .num_defn #LaxMonoidalFunctor}
###### Definition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two (pointed) [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}). A **lax monoidal functor** between them is

1. a [[functor]]

   $$
     F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,,
   $$

1. a [[morphism]]

   $$
     \epsilon \;\colon\; 1_{\mathcal{D}} \longrightarrow F(1_{\mathcal{C}})
   $$

1. a [[natural transformation]]

   $$
     \mu_{x,y}
       \;\colon\;
     F(x) \otimes_{\mathcal{D}} F(y)
       \longrightarrow
     F(x \otimes_{\mathcal{C}} y)
   $$

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

If $\epsilon$ and all $\mu_{x,y}$ are [[isomorphisms]], then $F$ is called a **[[strong monoidal functor]]**.

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

In the literature the term "monoidal functor" often refers by default to what in def. \ref{LaxMonoidalFunctor} is called a _strong monoidal functor_.

If $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) then a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between them  is often called a **[[symmetric monoidal functor]]**.

=--

+-- {: .num_example}
###### Example

Let $\mathcal{A}$ be the [[symmetric monoidal category]] of $\mathbb{Z}/2$-[[graded vector spaces]]
$Vect^{\mathbb{Z}/2}$ (example \ref{Z2Zgradedvectorspaces}) or of
[[super vector spaces]] $sVect$ (example \ref{CategoryOfSuperVectorSpaces}). Then there is an evident [[forgetful functor]]

$$
  \mathcal{A} \longrightarrow Vect
$$

to the category of plain [[vector spaces]], which forgets the grading.

In both cases this is a [[strong monoidal functor]] (def. \ref{LaxMonoidalFunctor})
For $\mathcal{A} = Vect^{\mathbb{Z}/2}$ it is also a [[braided monoidal functor]], but for
$\mathcal{A} = sVect$ it is not.

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
  FinDimVect_k \hookrightarrow Vect_k
$$

be the [[full subcategory]] [[FinDimVect]] of that of all [[vector spaces]] (over the given [[ground field]] $k$) on those which are **[[finite dimensional vector spaces]]**.

Clearly the [[tensor product of vector spaces]] (def. \ref{TensorProductOfVectorSpaces}) restricts to those of [[finite number|finite]] [[dimension]], and so there is the induced [[monoidal category]] structure from example \ref{VectAsAMonoidalCategory}

$$
  (FinDimVect_k, \otimes = \otimes_k, 1 = k )
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
  (sFinDimVect, \otimes_k, k, \tau^{super})
    \hookrightarrow
  (sVect, \otimes_k, k, \tau^{super})
$$

of the [[symmetric monoidal category]] of [[super vector spaces]] from example \ref{CategoryOfSuperVectorSpaces}, on those of finite total dimension is a [[rigid monoidal category]].

Here we say that a [[super vector space]] $V$ has [[dimension]]

$$
  (p\vert q)
  \in \mathbb{N} \times \mathbb{N}
$$

if its even part has dimension $p$ and its odd part has dimension $q$:

$$
  dim(V) = (p\vert q)
   \;\;\;
   \Leftrightarrow
   \;\;\;
  \left( dim(V_{even}) = p \;\;\;\;\text{and}\;\;\;\; dim(V_{odd}) = q \right)
  \,.
$$

The [[dual object]] of such a finite dimensional super vector space is just the linear [[dual vector space]] as in example \ref{FiniteDimensionalVectorSpaces}, equipped with the evident grading:

$$
  V = V_{even} \oplus V_{odd}
  \;\;\;\; \Rightarrow
  \;\;\;\;
  V^\ast = (V_{even}^\ast) \oplus (V_{odd}^\ast)
  \,.
$$

=--

+-- {: .num_prop #CompactClosedMonoidalCategory}
###### Proposition

Every [[rigid monoidal category|rigid]] [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory})  is a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) with [[internal hom]] between two objects given by the [[tensor product]]
of the [[codomain]] object with the [[dual object]] of the domain object

$$
  [A,B] \simeq A^* \otimes B
  \,.
$$


(The closed monoidal categories arising this way are called **[[compact closed categories]]**).

=--

+-- {: .proof}
###### Proof

The [[natural isomorphism]] that characterizes the [[internal hom]] $[A,-]$ as being [[right adjoint]] to the
[[tensor product]] $A \otimes (-)$ is given by the [[adjunction]] natural isomorphism that characterizes [[dual objects]]:

$$
  \mathcal{C}(C,[A,B])
  \simeq
  \mathcal{C}(C, A^\ast \otimes B)
    \simeq
  \mathcal{C}(C \otimes A, B)
  \,.
$$


=--


There are many [[monoidal categories]] whose "[[tensor product]]" operation is quite unlike the [[tensor product of vector spaces]]. Hence one says _[[tensor category]]_ for monoidal categories that are also $k$-[[linear categories]] and such that the tensor product functor  suitably reflects that linear structure.
There are slight variants of what people mean by a "[[tensor category]]". Here we mean precisely the following:

+-- {: .num_defn #TensorCategory}
###### Definition

For $k$ a [[field]], then a **$k$-[[tensor category]]** $\mathcal{A}$ is an

1. [[essentially small category|essentially small]]

1. [[linear category|k-linear]] (def. \ref{LinearCategory})

1. [[rigid monoidal category|rigid]] (def. \ref{DualizableObject})

1. [[symmetric monoidal category|symmetric]] (def. \ref{SymmetricMonoidalCategory})

1. [[monoidal category]] (def. \ref{MonoidalCategory})

such that

1. the [[tensor product]] functor $\otimes \colon \mathcal{A} \times \mathcal{A} \longrightarrow \mathcal{A}$ is in both arguments separately

   1. $k$-linear (def. \ref{LinearCategory});

   1. [[exact functor|exact]].


1. $End(1) \simeq k$ (the [[endomorphism ring]] of the [[tensor unit]] coincides with $k$).

=--

In this form this is considered in ([Deligne 02, 0.1](#Deligne02)).

We consider now various types of size constraints on tensor categories. The Tannaka reconstruction theorem (theorem \ref{TheTheorem} below) only assumes one of them (subexponential growth, def. \ref{SubexponentialGrowth}), but the others appear in the course of the proof of the theorem.

1. finiteness (def. \ref{FiniteTensorCategory})

1. finite $\otimes$-generation (def. \ref{FiniteTensorGeneration})

1. subexponential growth (def. \ref{SubexponentialGrowth})

Recall the concept of [[length of an object]] in an [[abelian category]], a generalization of the concept of [[dimension]] of a [[free module]]/[[vector space]].


+-- {: .num_defn #FiniteLength}
###### Definition

Let $\mathcal{C}$ be an [[abelian category]].
Given an [[object]] $X \in \mathcal{C}$, then a _[[Jordan-Hölder sequence]]_ or _[[composition series]]_ for $X$ is a finite [[filtration]], i.e. a finite sequence of [[subobject]] unclusions into $X$, starting with the [[zero objects]]

$$
  0 = X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X_{n-1} \hookrightarrow X_n = X
$$

such that at each stage $i$ the [[quotient]] $X_i/X_{i-1}$ (i.e. the [[coimage]] of the [[monomorphism]] $X_{i-1} \hookrightarrow X_i$) is a [[simple object]] of $\mathcal{C}$.

If a Jordan-H&#246;lder sequence for $X$ exists at all, then $X$ is said to be of _finite length_.

=--

(e.g. [EGNO 15, def. 1.5.3](#EGNO15))

+-- {: .num_prop #JordanHolderSequenceHasDefiniteLength}
###### Proposition
**([[Jordan-Hölder theorem]])**

If $X \in \mathcal{C}$ has finite length according to def. \ref{FiniteLength}, then in fact all Jordan-H&#246;lder sequences for $X$ have the same length $n \in \mathbb{N}$.

=--

(e.g. [EGNO 15, theorem 1.5.4](#EGNO15))

+-- {: .num_defn #LengthOfAnObject}
###### Definition

If an object $X \in \mathcal{C}$ has finite length according to def. \ref{FiniteLength}, then the length $n \in \mathbb{N}$ of any of its Jordan-H&#246;lder sequences, which is uniquely defined according to prop. \ref{JordanHolderSequenceHasDefiniteLength}, is called the _length of the object_ $X$.

=--

(e.g. [EGNO 15, def. 1.5.5](#EGNO15))


+-- {: .num_defn #FiniteTensorCategory}
###### Definition

A $k$-[[tensor category]] (def. \ref{TensorCategory}) is called **finite** (over $k$) if

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


The following is the main size constraint needed in the theorem. Notice that it is a "mild" constraint at least in the intuitive sense that it states just a minimum assumption on the expected behaviour of dimension ([[length of an object|length]]) under tensor powers.

+-- {: .num_defn #SubexponentialGrowth}
###### Definition

A [[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) is said to have **subexponential growth*** if the [[length]] of tensor exponentials is no larger than the exponential of the length: for every [[object]] $X$ there exists a [[natural number]] $N_X$ such that $X$ is of [[length of an object|length]] at most $N_X$, and that also all [[tensor product]] powers of $X$ are of length bounded by the corresponding powers of $N_X$:

$$
  \underset{X \in \mathcal{A}}{\forall}
  \,
  \underset{N_X \in \mathbb{N}}{\exists}
  \,
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

The tensor category $k$-[[FinDimVect]] of [[finite dimensional vector spaces]] from example \ref{FiniteDimensionalVectorSpaces} has subexponential growth (def. \ref{SubexponentialGrowth}), for $N_X = dim(X)$ the [[dimension]] of a vector space $X$, we have

$$
  dim\left( X^{\otimes^n} \right) = \left(dim(X)\right)^n
  \,.
$$

=--

Categories that do not satisfy sub-exponential growth have come to be known as *Deligne categories*, see e.g. [Hu 2024](#Hu24).

While many linear monoidal categories of interest do not satisfy
finiteness or [[rigid monoidal category|rigidity]] (def. \ref{DualizableObject}), often they
are such that all their objects are (formal) [[inductive limits]] over "small" objects
that do form a [[rigid monoidal category]].


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

   * an object in $Ind(\mathcal{A})$ is [[dualizable object|dualizable]] precisely if it is in $\mathcal{A}$.

=--


+-- {: .num_example}
###### Example

The category of all vector spaces is the category of [[ind-objects]] of the [[tensor category]]
of [[finite dimensional vector spaces]] (example \ref{FiniteDimensionalVectorSpaces}):

$$
  Vect \simeq Ind(FinDimVect)
  \,.
$$

Similarly the category of all [[super vector spaces]] (def. \ref{CategoryOfSuperVectorSpaces})
is the category of ind-objects of that of finite-dimensional super vector spaces
(example \ref{FiniteDimensionalSuperVectorSpaces})

$$
  sVect \simeq Ind(sFinDimVect)
  \,.
$$

=--







### Commutative algebra in tensor categories and Affine super-spaces
 {#CommutativeAlgebraInTensorCategories}

The key idea of [[supercommutative superalgebra]] is that it is nothing but plain [[commutative algebra]] but "[[internalization|internalized]]" not in ordinary [[vector spaces]], but in [[super vector spaces]]. This is made precise by def. \ref{MonoidsInMonoidalCategory} and ef. \ref{SupercommutativeSuperalgebra} below.

The key idea then of [[supergeometry]] is to define super-[[spaces]] to be spaces whose [[algebras of functions]] are [[supercommutative superalgebras]]. This is not the case for any "ordinary" space such as a [[topological space]] or a [[smooth manifold]]. But these spaces may be _characterized dually_ via their algebras of functions, and hence it makes sense to generalize the latter.

For [[smooth manifolds]] the [[duality]] statement is the following:

+-- {: .num_prop #EmbeddingOfSmoothManifoldsIntoRAlgebras}
###### Proposition
**([[embedding of smooth manifolds into formal duals of R-algebras]])**

The [[functor]]

$$
  C^\infty(-) \;\colon\; SmoothMfd \longrightarrow Alg_{\mathbb{R}}^{op}
$$

which sends a [[smooth manifold]] ([[finite number|finite]] [[dimension|dimensional]], [[paracompact topological space|paracompact]], [[second countable topological space|second countable]]) to (the [[formal dual]] of) its $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth functions]] is a [[full and faithful functor]].

In other words, for two [[smooth manifolds]] $X,Y$ there is a [[natural bijection]] between the [[smooth functions]] $X \to Y$ and the $\mathbb{R}$-[[associative algebra|algebra]] [[homomorphisms]] $C^\infty(X)\leftarrow C^\infty(Y)$.

=--

A **proof** is for instance in ([Kolar-Slovak-Michor 93, lemma 35.8, corollaries 35.9, 35.10](embedding+of+smooth+manifolds+into+formal+duals+of+R-algebras#KolarSlovakMichor93)).

This says that we may _identify_ [[smooth manifolds]] as the  "[[formal duals]]" of certain [[associative algebras]], namely those in the image of the above full embedding. Accordingly then, any larger class of associative algebras than this may be thought of as the class of [[formal duals]] to a generalized kind of manifold, defined thereby. Given any associative algebra $A$, then we may think of it as representing a space
$Spec(A)$ which is such that it has $A$ as its [[algebra of functions]].

This [[duality]] between certain  [[spaces]] and their [[algebras of functions]] is profound. In [[physics]] it has always been used implicitly, in fact it was so ingrained into theoretical physics that it took much effort to abstract away from [[coordinate system|coordinate functions]] to discover global [[Riemannian geometry]] in the guise of"[[general relativity]]". As mathematics, an early prominent duality theorem is [[Gelfand duality]] (between [[topological spaces]] and [[C*-algebras]]) which served as motivation for the very definition of [[algebraic geometry]], where [[affine schemes]] are nothing but the [[formal duals]] of [[commutative rings]]/[[commutative algebras]]. Passing to [[non-commutative algebras]] here yields [[non-commutative geometry]], and so forth. In great generality this duality between spaces and their function algebras appears as "[[Isbell duality]]" between [[presheaves]] and [[copresheaves]].

In [[supergeometry]] we are concerned with spaces that are formally dual to associative algebras which are "very mildly" non-commutative, namely [[supercommutative superalgebras]]. These are in fact [[commutative algebras]] when viewed internal to [[super vector spaces]]
(def. \ref{SupercommutativeSuperalgebra} below).
The corresponding [[formal dual]] spaces are, depending on some technical details, _[[super schemes]]_ or _[[supermanifolds]]_. In the [[physics]] literature, such spaces are usually just called _[[superspaces]]_.

We now make this precise.

+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def \ref{MonoidalCategory}), then a **[[monoid in a monoidal category|monoid internal to]]** $(\mathcal{C}, \otimes, 1)$ is

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

   where $a$ is the [[associator]] isomorphism of $\mathcal{C}$;

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

Moreover, if $(\mathcal{C}, \otimes , 1)$ has the structure of a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) $(\mathcal{C}, \otimes, 1, \tau)$ with symmetric [[braiding]] $\tau$, then a monoid $(A,\mu, e)$ as above is called a **[[commutative monoid in a symmetric monoidal category|commutative monoid in]]** $(\mathcal{C}, \otimes, 1, B)$ if in addition

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


+-- {: .num_example #MonoidsInVectAreAssociativeAlgebras}
###### Example

A [[monoid object]] according to def. \ref{MonoidsInMonoidalCategory} in the [[monoidal category]] of [[vector spaces]] from example \ref{TensorProductOfVectorSpaces} is equivalently an ordinary [[associative algebra]] over the given [[ground field]]. Similarly a [[commutative monoid]] in $Vect$ is an ordinary [[commutative algebra]]. Moreover, in both cases the [[homomorphisms]] of monoids agree with usual algebra homomorphisms. Hence there are [[equivalences of categories]].

$$
  Mon(Vect_k) \simeq Alg_k
$$

$$
  CMon(Vect_k) \simeq CAlg_k
  \,.
$$

=--

+-- {: .num_example #GradedAlgebras}
###### Example

For $G$ a [[group]], then a **$G$-[[graded algebra|graded]] [[associative algebra]]** is a [[monoid object]] according to def. \ref{MonoidsInVectAreAssociativeAlgebras} in the [[monoidal category]] of $G$-[[graded vector spaces]] from example \ref{GradedVectorSpacesAsAMonoidaCategory}.

$$
  Alg_k^G \simeq Mon(Vect_k^G)
  \,.
$$

This means that a $G$-graded algebra is

1. a $G$-[[graded vector space]] $A = \underset{g\in G}{\oplus} A_g$

1. an [[associative algebra]] structure on the underlying vector space $A$

such that for two elements of homogeneous degree, i.e. $a_1 \in A_{g_1} \hookrightarrow A$ and $a_2 \in A_{g_2} \hookrightarrow A$ then their product is in degre $g_1 g_2$

$$
  a_{g_1} a_{g_2} \in A_{g_1 g_2} \hookrightarrow A
  \,.
$$


=--

Example \ref{MonoidsInVectAreAssociativeAlgebras} motivates the following definition:

+-- {: .num_defn #SupercommutativeSuperalgebra}
###### Definition

A **[[supercommutative superalgebra]]** is a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}) in the [[symmetric monoidal category|symmetric monoidal]] [[category of super vector spaces]] (def. \ref{CategoryOfSuperVectorSpaces}). We write $sCAlg_k$ for the [[category]] of [[supercommutative superalgebras]] with the induced [[homomorphisms]] between them:

$$
  sCAlg_k \;\coloneqq\; CMon(sVect_k)
  \,.
$$

Unwinding what this means, then a [[supercommutative superalgebra]] $A$ is

1. a $\mathbb{Z}/2$-graded associative algebra according to example \ref{GradedAlgebras};

1. such that for any two elements $a, b$ of homogeneous degree, their product satisfies

   $$
     a b \; = \; (-1)^{deg(a) deg(b)}\, b a
     \,.
   $$

=--

+-- {: .num_remark}
###### Remark

In view of def. \ref{SupercommutativeSuperalgebra} we might define a not-necessarily supercommutative superalgebra to be a [[monoid]] (not necessarily commutative) in [[sVect]], and write

$$
  sAlg_k \coloneqq Mon(sVect)
  \,.
$$

However, since the definition of not-necessarily commutative monoids (def. \ref{MonoidsInMonoidalCategory}) does not invoke the [[braiding]] of the ambient [[tensor category]], and since [[super vector spaces]] differ from $\mathbb{Z}/2$-[[graded vector spaces]] only via their [[braiding]] (example \ref{CategoryOfSuperVectorSpaces}), this yields equivalently just the $\mathbb{Z}/2$-graded algebras froom example \ref{GradedAlgebras}:

$$
  sAlg_k \simeq Alg_k^{\mathbb{Z}/2}
  \,.
$$

Hence the heart of [[superalgebra]] is _[[supercommutative superalgebra|super-commutativity]]_.

=--


+-- {: .num_example #GrassmannAlgebra}
###### Example

The [[supercommutative superalgebra]] which is [[free construction|freely generated]] over $k$ from $n$ generators
$\{\theta_i\}_{i = 1}^n$ is the [[quotient]] of the [[tensor algebra]] $T^\bullet \mathbb{R}^n$,
with the generators $\theta_i$ in odd degree, by the ideal generated by the
relations

$$
  \theta_i \theta_j = - \theta_j \theta_i
$$

for all $i,j \in \{1, \cdots, n\}$.

This is also called a _[[Grassmann algebra]]_, in honor of ([Grassmann 1844](#Grassmann1844)), who introduced and
studied the super-sign rule in def. \ref{SupercommutativeSuperalgebra} a century ahead of his time.

We also denote this algebra by

$$
  \wedge^\bullet_{\mathbb{R}}(\mathbb{R}^n)
    \;\in\;
   sCAlg_{\mathbb{R}}
   \,.
$$

=--

+-- {: .num_example #HomotopyCommutativeRingSpectrum}
###### Example

Given a [[homotopy commutative ring spectrum]] $E$ (i.e., via the [[Brown representability theorem]], a [[multiplicative cohomology theory|multiplicative]] [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theory]]), then its [[stable homotopy groups]] $\pi_\bullet(E)$ inherit the structure of a super-commutative ring.

See at _[[Introduction to Stable homotopy theory]]_ in the section [1-2 Homotopy commutative ring spectra](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyRingSpectra) [this proposition](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum).

=--

The following is an elementary but fundamental fact about the relation between
commutative algbra and supercommutative superalgebra. It is implicit in much of the
literature, but maybe the only place where it has been made explicit before is
([Carchedi-Roytenberg 12, example 3.18](#CarchediRoytenberg12)).


+-- {: .num_prop #InclusionOfCAlgIntosCAlg}
###### Proposition

There is a [[full subcategory]] inclusion

$$
  \array{
     CAlg_k &\hookrightarrow& sCAlg_k
     \\
     = && =
     \\
     CMon(Vect_k) &\hookrightarrow& CMon(sVect_k)
  }
$$

of [[commutative algebras]] (example \ref{MonoidsInVectAreAssociativeAlgebras})
into [[supercommutative superalgebras]] (def. \ref{SupercommutativeSuperalgebra})
induced via prop. \ref{MonoidsPreservedByLaxMonoidalFunctor} from the full inclusion

$$
  i \;\colon\; Vectk \hookrightarrow sVect_k
$$

of [[vector spaces]] (def. \ref{VectorSpaces}) into [[super vector spaces]]
(def. \ref{CategoryOfSuperVectorSpaces}), which is a [[braided monoidal functor]]
by prop. \ref{InclusionOfVectorSpacesIntoSupervectorSpaces}. Hence this regards a
commutative algebra as a superalgebra concentrated in even degree.

This inclusion functor has both a [[left adjoint|left]] [[adjoint functor]] and a [[right adjoint|right]] [[adjoint functor]] ,
(an [[adjoint triple]] exibiting a [[reflective subcategory]] and [[coreflective subcategory]] inclusion, an "[[adjoint cylinder]]"):

$$
  CAlg_k
    \underoverset
      {\underset{(-)_{even}}{\longleftarrow}}
      {\overset{(-)/(-)_{odd}}{\longleftarrow}}
      {\hookrightarrow}
  sCAlg_k
  \,.
$$

Here

1. the [[right adjoint]] $(-)_{even}$ sends a supercommutative superalgebra to its even part $A \mapsto A_{even}$;

1. the [[left adjoint]] $(-)/(-)_{even}$ sends a supercommutative superalgebra to the [[quotient]] by the ideal which is generated by its odd part $A \mapsto A/(A_{odd})$ (hence it sets all elements to zero which may be written as a product such that at least one factor is odd-graded).

=--

+-- {: .proof}
###### Proof

The full inclusion $i$ is evident. To see the [[adjunctions]] observe their characteristic
[[natural bijections]] between [[hom-sets]]:
If $A_{ordinary}$ is an ordinary commutative algebra regarded as a superalgeba $i(A_{ordinary})$ concentrated in even degree,
and if $B$ is any superalgebra,

1. then every super-algebra homomorphism of the form $A_{ordinary} \to B$ must factor
   through $B_{even}$, simply because super-algebra homomorpism by definition respect the $\mathbb{Z}/2$-grading. This gives a natual bijection

   $$
     Hom_{sCAlg_k}(i(A_{ordinary}), B) \simeq Hom_{CAlg_k}(A_{ordinary,B_{even}})
     \,,
   $$

1. every super-algebra homomorphism of the form $B \to i(A_{ordinary})$ must send every odd element of $B$ to 0, again because homomorphism have to respect the $\mathbb{Z}/2$-grading, and since homomorphism of course also preserve products, this means that the entire ideal generated by $B_{odd}$ must be sent to zero, hence the homomorphism must facto through the [[projection]] $B \to B/B_{odd}$, which gives a natural bijection

   $$
     Hom_{sCalg_k}(B, i(A_{ordinary}))
       \simeq
     Hom_{Alg_k}(B/B_{odd}, A_{ordinary})
     \,.
   $$

=--


It is useful to make explicit the following [[formal dual|formally dual]] perspective on [[supercommutative superalgebras]]:

+-- {: .num_defn #Affines}
###### Definition

For $\mathcal{C}$ a [[symmetric monoidal category]], then we write

$$
  Aff(\mathcal{C}) \coloneqq CMon(\mathcal{C})^{op}
$$

for the [[opposite category]] of the [[category of commutative monoids]] in $\mathcal{C}$, according to def. \ref{MonoidsInMonoidalCategory}.

For $R \in CMon(\mathcal{C})$ we write

$$
  Spec(A)
  \in
  Aff(\mathcal{C})
$$

for the same object, regarded in the opposite category. We also call this the **[[affine scheme]]** of $A$. Conversely, for $X \in Aff(\mathcal{C})$, we write

$$
  \mathcal{O}(X) \in CMon(\mathcal{C})
$$

for the same object, regarded in the category of commutative monoids. We also call this the **[[algebra of functions]]** on $X$.

=--

+-- {: .num_defn #AffineSuperSchemes}
###### Definition

For the special case that $\mathal{C} = $ [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces})
in def. \ref{Affines}, then we say that the objects in

$$
  Aff(sVect_k) = scAlg_k^{op} =  CMon(sVect_k)^{op}
$$

are **affine [[super schemes]]** over $k$.

=--

+-- {: .num_example #OrdinaryCAlgAssCAlg}
###### Example

For $A \in CAlg_{\mathbb{R}}$ an ordinary [[commutative algebra]] over $\mathbb{R}$,
then of course this becomes a [[supercommutative superalgebra]] by regarding it
as being concentrated in even degrees. Accordingly, via def. \ref{Affines}, ordinary [[affine schemes]]
[[full subcategory|fully embed]] into affine [[super schemes]] (def. \ref{AffineSuperSchemes})

$$
  Aff(Vect_k)
    \hookrightarrow
  Aff(sVect_k)
  \,.
$$

In particular for $\mathbb{R}^p$ an ordinary [[Cartesian space]], this becomes
an affine [[superscheme]] in even degree, under the above embedding. As such, it is usually
written

$$
  \mathbb{R}^{p \vert 0}
    \in
  Aff(sVect_k)
  \,.
$$


=--


+-- {: .num_example #Superpoint}
###### Example

The formal dual space, according to def. \ref{Affines} (example \ref{Affines}) to a [[Grassmann algebra]] $\wedge^\bullet_{\mathbb{R}}(\mathbb{R}^q)$
(example \ref{GrassmannAlgebra}) is to be thought of as a space which is "so tiny" that
the coefficients of the [[Taylor expansion]] of any real-valued function on it
become "so very small" as to be actually equal to zero, at least after the $q$-th power.

For instance for $q = 2$ then a general element of $\wedge^\bullet_{\mathbb{R}}(\mathbb{R}^q)$
is of the form

$$
  f = a_0 + a_1 \theta_1 + a_2 \theta_2 + a_{12} \theta_1 \theta_2
  \;\;\;\in
  \wedge^\bullet_{\mathbb{R}}(\mathbb{R}^q)
  \,.
$$

for $a_1,a_2, a_{12} \in \mathbb{R}$,
to be compared with the [[Taylor expansion]] of a [[smooth function]] $g \colon \mathbb{R}^2 \to \mathbb{R}$,
which is of the form

$$
  g(x_1, x_2) =
  g(0) + \frac{\partial g}{\partial x_1}(0)\, x_1 + \frac{\partial g}{\partial x_2}(0)\, x_2
    +
    \frac{\partial^2 g}{\partial x_1 \partial x_2}(0) \, x_1 x_2
     +
      \cdots
  \,.
$$

Therefore the [[formal dual]] [[space]] to a [[Grassmann algebra]] behaves like an infinitesimal neighbourhood of a point.
Hence these are also called **[[superpoints]]** and one writes

$$
  \mathbb{R}^{0\vert q}
    \coloneqq
  Spec(\wedge^\bullet_{\mathbb{R}}(\mathbb{R}^q))
  \,.
$$


=--

+-- {: .num_example}
###### Example

Combining example \ref{OrdinaryCAlgAssCAlg} with example \ref{Superpoint},
and using prop. \ref{ProductsInAff}, we obtain the affine [[super schemes]]

$$
  \mathbb{R}^{p \vert q}
    \coloneqq
  \mathbb{R}^{p\vert 0}
    \times
  \mathbb{R}^{0\vert q}
    \simeq
  Spec\left(
     \underbrace{C^\infty(\mathbb{R}^p)}
       \otimes_{\mathbb{R}}
     \wedge^\bullet_{\mathbb{R}} \mathbb{R}^q
  \right)
  \,.
$$

These may be called the **[[super Cartesian spaces]]**.
The play the same role in the theory of [[supermanifolds]] as the ordinary
[[Cartesian spaces]] do for [[smooth manifolds]]. See at _[[geometry of physics -- supergeometry]]_ for more on this.

=--


+-- {: .num_defn #ParityAutomorphism}
###### Definition

Given a [[supercommutative superalgebra]] $A$ (def. \ref{SupercommutativeSuperalgebra}), its **parity involution** is the algebra [[automorphism]]

$$
  par \;\colon\; A \overset{\simeq}{\longrightarrow} A
$$

which on homogeneously graded elements $a$ of degree $deg(a) \in \{even,odd\} = \mathbb{Z}/2\mathbb{Z}$ is multiplication by the degree

$$
  a \mapsto (-1)^{deg(a)}a
  \,.
$$

(e.g. [arXiv:1303.1916, 7.5](http://arxiv.org/abs/1303.1916))

Dually, via def. \ref{Affines}, this means that every affine [[super scheme]] has a canonical [[involution]].

=--



Here are more general and more abstract examples of commutative monoids, which will be useful to make explicit:

+-- {: .num_example #MonoidGivenByTensorUnit}
###### Example

Given a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidalCategory}), then the [[tensor unit]] $1$ is a [[monoid in a monoidal category|monoid in]] $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}) with product given by either the left or right [[unitor]]

$$
  \ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1
  \,.
$$

By lemma \ref{kel1}, these two morphisms coincide and define an [[associativity|associative]] product with unit the identity $id \colon 1 \to 1$.

If $(\mathcal{C}, \otimes , 1)$ is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}), then this monoid is a [[commutative monoid in a symmetric monoidal category|commutative monoid]].

=--

+-- {: .num_example #TensorProductOfTwoCommutativeMonoids}
###### Example

Given a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}), and given two [[commutative monoid in a symmetric monoidal category|commutative monoids]] $(E_i, \mu_i, e_i)$, $i \in \{1,2\}$ (def. \ref{MonoidsInMonoidalCategory}), then the [[tensor product]] $E_1 \otimes E_2$ becomes itself a commutative monoid with unit morphism

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



Monoids are preserved by [[lax monoidal functors]]:

+-- {: .num_prop #MonoidsPreservedByLaxMonoidalFunctor}
###### Proposition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D}, \otimes_{\mathcal{D}},1_{\mathcal{D}})$ be two [[monoidal categories]] (def. \ref{MonoidalCategory}) and let $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[lax monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between them.

Then for $(A,\mu_A,e_A)$ a [[monoid in a monoidal category|monoid in]] $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}), its image $F(A) \in \mathcal{D}$ becomes a monoid $(F(A), \mu_{F(A)}, e_{F(A)})$ by setting

$$
  \mu_{F(A)}
   \;\colon\;
  F(A) \otimes_{\mathcal{C}} F(A)
    \overset{}{\longrightarrow}
  F(A \otimes_{\mathcal{C}} A)
    \overset{F(\mu_A)}{\longrightarrow}
  F(A)
$$

(where the first morphism is the structure morphism of $F$) and setting

$$
  e_{F(A)}
    \;\colon\;
  1_{\mathcal{D}}
    \longrightarrow
  F(1_{\mathcal{C}})
    \overset{F(e_A)}{\longrightarrow}
  F(A)
$$

(where again the first morphism is the corresponding structure morphism of $F$).

This construction extends to a functor

$$
  Mon(F)
   \;\colon\;
  Mon(\mathcal{C}, \otimes_{\mathcal{C}}, 1_{\mathcal{C}})
    \longrightarrow
  Mon(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}})
$$

from the [[category of monoids]] of $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}) to that of $\mathcal{D}$.

Moreover, if $\mathcal{C}$ and $\mathcal{D}$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) and $F$ is a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}) and $A$ is a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}) then so is $F(A)$, and this construction extends to a functor

$$
  CMon(F)
   \;\colon\;
  CMon(\mathcal{C}, \otimes_{\mathcal{C}}, 1_{\mathcal{C}})
    \longrightarrow
  CMon(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}})
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows immediately from combining the associativity and unitality (and symmetry) constraints of $F$ with those of $A$.

=--






### Modules in tensor categories and Super vector bundles
 {#ModulesInTensorCategories}

Above (in def. \ref{Affines}) we considered spaces $X$ from a dual perspective, as determined by their [[algebras of functions]] $\mathcal{O}(X)$. In the same spirit then we are to express various constructions on and with spaces in terms of dual algebraic constructions.

A key such construction is that of [[vector bundles]] over $X$. Here we discuss the corresponding algebraic incarnation of these, namely as _[[modules]]_ over [[algebras of functions]].

Suppose that $X$ is a [[smooth manifold]], and $V \stackrel{p}{\to} X$ is an ordinary smooth real [[vector bundle]] over $X$. A [[section]] of this vector bundle is a smooth function $\sigma \colon X \to V$ such that $p \circ \sigma = id$

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

In conclusion, any [[vector bundle]] $V \to X$ gives rise to an $C^\infty(X)$-[[module]] $\Gamma_X(V)$ of [[sections]].

The _[[smooth Serre-Swan theorem]]_ states sufficient conditions on $X$ such that the converse holds. Together with the [[embedding of smooth manifolds into formal duals of R-algebras]] (prop \ref{EmbeddingOfSmoothManifoldsIntoRAlgebras}), this means that [[differential geometry]] is "more algebraic" than it might superficially seem, hence that its "algebraic deformation" to [[supergeometry]] is
more natura than it might superficially seem:

+-- {: .num_prop}
###### Proposition
**([[smooth Serre-Swan theorem]], [Nestruev 03](smooth+Serre-Swan+theorem#Nestruev03))**

For $X$ a [[smooth manifold]], then the construction which sends a smooth [[vector bundle]] $V \to X$ to its $C^\infty(X)$-[[module]] $\Gamma_X(V)$ of [[sections]] is an [[equivalence of categories]]

$$
  VectBund_X^{fin}
    \stackrel{\simeq}{\longrightarrow}
  C^\infty(X) Mod_{proj}^{fin\,gen}
$$

between that of smooth [[vector bundles]] of finite [[rank]] over $X$ and that of [[finitely generated object|finitely generated]] [[projective modules]] over the $\mathbb{R}$-[[associative algebra|algebra]] $C^\infty(X)$ of [[smooth functions]] on $X$.

=--

One may turn the [[Serre-Swan theorem]] around to regard for $R$ any [[commutative monoid]] in some [[symmetric monoidal category]] (def. \ref{MonoidsInMonoidalCategory}), the [[modules]] over $R$ as "generalized vector bundles" over the space $Spec(R)$ (def. \ref{Affines}). These "generalized vector bundles" are called "[[quasicoherent sheaves]]" over affines. Specified to the case that $\mathcal{C} = $ [[sVect]], this hence yields a concept of **super vector bundles**.

We now state the relevant definitions and constructions formally.


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

The following degenerate example turns out to be important for the general development of the theory below.

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

The classical subject of  [[algebra]], not necessarily over [[ground fields]], is the
above general concepts of monoids and their modules specialized to the ambient [[symmetric monoidal category]] being the category [[Ab]] of  [[abelian groups]] regarded as a [[symmetric monoidal category]] via the [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ (whose [[tensor unit]] is the additive group of [[integers]] $\mathbb{Z}$):

1. A [[monoid in a monoidal category|monoid in]] $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[ring]].

1. A [[commutative monoid in a symmetric monoidal category|commutative monoid in]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[commutative ring]] $R$.

1. An $R$-[[module object]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{ModulesInMonoidalCategory}) is equivalently an $R$-[[module]];

1. The tensor product of $R$-module objects (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[tensor product of modules]].

1. The [[category of modules|category of module objects]] $R Mod(Ab)$ (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[category of modules]] $R Mod$.

=--


+-- {: .num_example #ModulesOverGGroupRing}
###### Example

Let $G$ be a [[discrete group]] and write $k[G]$ for its [[group algebra]] over the [[ground field]] $k$.
Then $k[G]$-[[modules]] in [[Vect]] are equivalently [[linear representations]] of $G$.


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

Given a [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ with  [[braiding]] denoted $\tau$ (def. \ref{SymmetricMonoidalCategory}, def. \ref{ClosedMonoidalCategory}), given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), and given $(N_1, \rho_1)$ and $(N_2, \rho_2)$ two left $A$-[[module objects]] (def.\ref{MonoidsInMonoidalCategory}), then

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

When thinking of commutative monoids in some tensor category as [[formal duals]] to certain [[spaces]],
as in def. \ref{Affines}, then we are interested in forming [[Cartesian products]] and more generally [[fiber products]] of these spaces. Dually this is given by [f[coproducts]] of commutative monoids and commutative $R$-algebras. The following says that these may be computed just as the [[tensor product of modules]]:


+-- {: .num_prop #CoproductsInCMon}
###### Proposition

Let $\mathcal{C}$ be a [[symmetric monoidal category]] such that

1. it has [[reflexive coequalizers]]

1. which are preserved by the [[tensor product]] functors $A \otimes (-) \colon \mathcal{C} \to \mathcal{C}$ for all objects $A$ in $\mathcal{C}$.

Then for $f \colon A \to B$ and $g \colon A \to C$ two morphisms in the category $CMon(\mathcal{C})$ of _[[commutative monoids]]_ in $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}), the underlying object in $\mathcal{C}$ of the [[pushout]] in $CMon(\mathcal{C})$ coincides with the [[tensor product]] in the monoidal category $A$[[Mod]] (according to prop. \ref{MonoidalCategoryOfModules}):

$$
  U\left(B \sqcup_A C\right) \simeq  B \otimes_A C
  \,.
$$

Here $B$ and $C$ are regarded as equipped with the canonical $A$-module structure induced by the morphisms $f$ and $g$, respectively.


=--


This appears for instance as ([[Sketches of an Elephant|Johnstone, page 478, cor. 1.1.9]]).

+-- {: .num_remark #AssumptionsOnCoproductInCMonGenericallySatisfied}
###### Remark

In every [[tensor category]] (def. \ref{TensorCategory}) the conditions
in prop. \ref{CoproductsInCMon} are satisfied.

=--

+-- {: .proof}
###### Proof

By definition, every [[tensor category]] is an [[abelian category]] (def. \ref{AdditiveAndAbelianCategories}).
The [[coequalizer]] of two [[parallel morphisms]] $f,g$ in an abelian category is isomorphic to the [[cokernel]]
of the difference $f-g$ (formed in the [[abelian group]] struture on the [[hom-space]]). Hence all
coequalizers exist, in particlar the [[split coequalizers]] required in prop. \ref{CoproductsInCMon}.


Moreover, by definition every [[tensor category]] is a [[rigid monoidal category]]. This implies that it is
also a [[closed monoidal categories]], by prop. \ref{CompactClosedMonoidalCategory}, and this means that the
functors $A \otimes (-)$ are [[left adjoint]] functors, and such preserve all colimits.

=--

+-- {: .num_prop #ProductsInAff}
###### Proposition

Let $\mathcal{A}$ be a [[tensor category]], and let $R \in CMon(\mathcal{A})$
be a [[commutative monoid]] in $\mathcal{A}$.

Then for $A_1, A_2$ two
$R$-algebas according to def. \ref{AAlgebra}, regarded as affine schemes
$Spec(A_1), Spec(A_2) \in Aff(R Mod(\mathcal{C}))$ according to
prop. \ref{MonoidalCategoryOfModules} and def. \ref{Affines}
the [[Cartesian product]] of $Spec(A_1)$ with $Spec(A_2)$ exists in $Aff(R Mod(\mathcal{C}))$
and is the [[formal dual]] of the tensor product algebra $A_1 \otimes_R A_2$
according to example \ref{TensorProductOfTwoCommutativeMonoids}:

$$
  Spec(A_1) \times Spec(A_2) \simeq Spec(A_1 \otimes_R A_2)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{AlgebrasOverAAreMonoidsUnderA} the [[formal dual]] of the statement is given by prop. \ref{CoproductsInCMon},
which does apply, according to remark \ref{AssumptionsOnCoproductInCMonGenericallySatisfied}.

=--

+-- {: .num_defn #ExtensionOfScalars}
###### Proposition

Let $\mathcal{C}$ be a [[symmetric monoidal category]], let $A_1, A_2 \in CMon(\mathcal{C})$ be two [[commutative monoids]] in $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}) and

$$
  \phi \;\colon\; A_1 \longrightarrow A_2
$$

a [[homomorphism]] [[commutative monoids]] (def. \ref{MonoidsInMonoidalCategory}).

Then there is a pair of [[adjoint functors]] between the [[categories of modules]] (def. \ref{ModulesInMonoidalCategory})

$$
  A_1 Mod(\mathcal{C})
    \underoverset
      {\underset{\phi^\ast}{\longleftarrow}}
      {\overset{\phi_\ast}{\longrightarrow}}
      {}
  A_2 Mod(\mathcal{C})
$$

where

1. the [[right adjoint]], called **[[restriction of scalars]]**, sends an $A_2$-[[module]] $(N, \rho)$ to the $A_1$-module $(N,\rho')$ whose [[action]] is given by precomposition with $\phi$:

   $$
     A_1 \otimes N
      \stackrel{\phi \otimes id}{\longrightarrow}
     A_2 \otimes N
      \stackrel{\rho}{\longrightarrow}
     N
     \,.
   $$

1. the [[left adjoint]], called **[[extension of scalars]]** sends an $A_1$-module $(N,\rho)$ to the [[tensor product]]

   $$
     \phi_\ast(N) \coloneqq A_2 \otimes_{A_1} N
   $$

   (where we are regarding $A_2$ as a commutative monoid in $A_1$-modules via prop. \ref{AlgebrasOverAAreMonoidsUnderA}) and equipped with the evident [[action]] induced by the multiplication in $A_2$:


  $$
    A_2 \otimes \phi^\ast(N)
     =
    A_2 \otimes A_2 \otimes_{A_1} N
      \stackrel{\mu_{A_2} \otimes_{A_1} N }{\longrightarrow}
    A_2 \otimes_{A_1} N
     =
    \phi^\ast(N)
  \,.
  $$

=--

+-- {: .proof}
###### Proof

By prop. \ref{AlgebrasOverAAreMonoidsUnderA}
the [[adjunction]] in question has the form

$$
  A_1 Mod(\mathcal{C})
   \underoverset
     {\underset{U}{\longleftarrow}}
     {\overset{F}{\longrightarrow}}
     {}
  A_2 Mod( (A_1 Mod, \otimes_{A_1}, A_1) )
$$

and hence the statement follows with prop. \ref{MonoidModuleOverItself}.

=--

+-- {: .num_remark}
###### Remark

In the dual interpretation of $R$-[[modules]] as generalized [[vector bundles]] (namely: [[quasicoherent sheaves]]) over $Spec(R)$ (def. \ref{Affines}) then $\phi \colon A_1 \to A_2$ becomes a map of spaces

$$
  Spec(\phi)
   \colon
  Spec(A_2)
    \longrightarrow
  Spec(A_1)
$$

and then [[extension of scalars]] according to prop. \ref{ExtensionOfScalars} corresponds to the [[pullback]] of vector bundles from $Spec(A_1)$ to $Spec(A_2)$.

=--















### Super-Groups as super-commutative Hopf algebras
 {#GroupsAsHopfAlgebras}

Above we have considered affine spaces $Spec(A)$ (def. \ref{Affines}) in [[symmetric monoidal categories]] $\mathcal{C}$.
Now we discuss what it means to equip these with the stucture of [[group objects]], hence to form
affine groups in $\mathcal{C}$.

A (possibly) familiar example arises in [[differential geometry]], where one considers groups whose underlying set is promoted to a [[smooth manifold]] and all whose operations (product, inverses) are [[smooth functions]]. These are of course the _[[Lie groups]]_.

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


In the above example, write $C^\infty(X)$ for the [[smooth algebra]] of [[smooth functions]] on a [[smooth manifold]] $X$. The assignment

$$
  C^\infty(-) \;\colon\; SmthMfd \hookrightarrow SmthAlg_{\mathbb{R}}^{op}
$$

is the [[embedding of smooth manifolds into formal duals of R-algebras]] from prop. \ref{EmbeddingOfSmoothManifoldsIntoRAlgebras}.

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
    && C^\infty(G) \otimes^c C^\infty(G) &\longleftarrow& C^\infty(G) &\colon& product^\ast = coproduct
  }
  \,.
$$

Now the [[associativity]] of the group product translates into a corresponding dual property of its dual, called "[[co-associativity]]", and so forth. The resulting algebraic structure is called a **[[Hopf algebra]]**.


While the explicit definition of a _[[Hopf algebra]]_ may look involved at first sight, Hopf algebras are simply [[formal duals]] of [[groups]]. Since this perspective is straightforward, we may just as well consider it in the generality of [[groupoids]].

A simple illustrative archetype of the following construction of commutative Hopf algebroids from homotopy commutative ring spectra is the following situation:

For $X$ a [[finite set]] consider

$$
  \array{
    X \times X \times X
    \\
    \downarrow^{\mathrlap{\circ = (pr_1, pr_3)}}
    \\
    X \times X
    \\
    {}^{\mathllap{s = pr_1}}\downarrow
     \uparrow
    \downarrow^{\mathrlap{t = pr_2}}
    \\
    X
  }
$$

as the ("[[codiscrete groupoid|codiscrete]]") [[groupoid]] with $X$ as [[objects]] and precisely one morphism from every object to every other. Hence the [[composition]] operation $\circ$, and the [[source]] and [[target]] maps are simply projections as shown. The identity morphism (going upwards in the above diagram) is the [[diagonal]].

Then consider the image of this structure under forming the [[free abelian groups]] $\mathbb{Z}[X]$, regarded as [[commutative rings]] under pointwise multiplication.

Since

$$
  \mathbb{Z}[X \times X]
    \simeq
  \mathbb{Z}[X] \otimes \mathbb{Z}[X]
$$

this yields a diagram of homomorphisms of commutative rings of the form

$$
  \array{
    (\mathbb{Z}[X] \otimes \mathbb{Z}[X] )
      \otimes_{\mathbb{Z}[X]}
    (\mathbb{Z}[X] \otimes \mathbb{Z}[X])
    \\
    \uparrow^{\mathrlap{} }
    \\
    \mathbb{Z}[X] \otimes \mathbb{Z}[X]
    \\
    \uparrow
     \downarrow
    \uparrow
    \\
    \mathbb{Z}[X]
  }
$$

satisfying some obvious conditions. Observe that here

1. the two morphisms $\mathbb{Z}[X] \rightrightarrows \mathbb{Z}[X] \otimes \mathbb{Z}[X]$ are $f \mapsto f \otimes e$ and $f \mapsto e \otimes f$, respectively, where $e$ denotes the unit element in $\mathbb{Z}[X]$;

1. the morphism $\mathbb{Z}[X] \otimes \mathbb{Z}[X] \to \mathbb{Z}[X]$ is the multiplication in the ring $\mathbb{Z}[X]$;

1. the morphism

   $$
     \mathbb{Z}[X] \otimes \mathbb{Z}[X]
       \longrightarrow
     \mathbb{Z}[X] \otimes \mathbb{Z}[C] \otimes \mathbb{Z}[C]
       \overset{\simeq}{\longrightarrow}
     (\mathbb{Z}[X] \otimes \mathbb{Z}[X] ) \otimes_{\mathbb{Z}[X]} (\mathbb{Z}[X] \otimes \mathbb{Z}[X])
   $$

   is given by $f \otimes g \mapsto f \otimes e \otimes g$.

We now say this again, in generality:

+-- {: .num_defn #CommutativeHopfAlgebroid}
###### Definition

Let $\mathcal{A}$ be a [[tensor category]] (def. \ref{TensorCategory}).
A **[[commutative Hopf algebroid]]** in $\mathcal{A}$ is an [[internal groupoid]] in the [[opposite category]] $CMon(\mathcal{A})^{op}$ of [[commutative monoids]] in $\mathcal{A}$, regarded with its [[cartesian monoidal category]] structure according to prop. \ref{ProductsInAff}.

=--

(e.g. [Ravenel 86, def. A1.1.1](commutative+Hopf+algebroid#Ravenel86))

We unwind def. \ref{CommutativeHopfAlgebroid}.  For $R \in CMon(\mathcal{A})$, write $Spec(R)$ for same same object, but regarded as an object in $CMon(\mathcal{A})^{op}$.


+-- {: .num_prop #CommutativeHopfAlgebroidSpelledOut}
###### Proposition


An [[internal category]] in $CMon(\mathcal{A})^{op}$ is a [[diagram]] in $CMon(\mathcal{A})^{op}$ of the form

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

The key fact to use now is prop. \ref{ProductsInAff}: the [[tensor product]] of commutative monoids exhibits the [[cartesian monoidal category]] structure on $CMon(\mathcal{A})^{op}$, :
$$
  Spec(R_1) \underset{Spec(R_3)}{\times} Spec(R_2)
  \simeq
  Spec(R_1 \otimes_{R_3} R_2)
  \,.
$$

This means that def. \ref{CommutativeHopfAlgebroid} is equivalently a diagram in $CMon(\mathcal{A})$ of the form

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

An [[internal groupoid]] $\mathcal{G}_1 \stackrel{\overset{s}{\longrightarrow}}{\underset{t}{\longrightarrow}} \mathcal{G}_0$ for which the [[domain]] and [[codomain]] morphisms coincide, $s = t$, is euqivalently a [[group object]] in the [[slice category]] over $\mathcal{G}_0$.

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


By internalizing all of the above from $Vect$ to $sVect$, we obtain the concept of [[supergroups]]:

+-- {: .num_defn #Supergroup}
###### Definition

An affine algebraic _[[supergroup]]_ $G$ is equivalently

* a pointed, one-object [[internal groupoid]] in the [[opposite category]] $Aff(sVect) = CMon(sVect_k)^{op}$ (def. \ref{Affines}) of [[supercommutative superalgebras]] from def. \ref{SupercommutativeSuperalgebra}

* the [[formal dual]] of a **[[super-commutative Hopf algebra]]**, namely a [[commutative Hopf algebra]] (prop. \ref{CommutativeHopfAlgebroidSpelledOut}, remark \ref{HopfAlgebrasAsHopfAlgebroids}).

=--

We will often just say "supergroup" for short in the following. If $H$ is the corresponding [[supercommutative Hopf algebra]] then we also write $Spec(H)$ for this supergroup.


The following asks that the parity involution (def. \ref{ParityAutomorphism}) on a supergroup is  an [[inner automorphism]]:

+-- {: .num_defn #InnerParity}
###### Definition

An **inner parity** of a [[supergroup]] $G$, def. \ref{Supergroup} is an element $\epsilon \in G_{even}$ such that

1. it is [[involution|involutive]] i.e. $\epsilon^2 = 1$

1. its [[adjoint action]] on $G$ is the parity involution of def. \ref{ParityAutomorphism}.

Dually this mean that an inner pariy is an algebra homomorphism $\epsilon^\ast \colon\mathcal{O}(G) \to k$ such that

1. the composite

   $$
     \mathcal{O}(G) \stackrel{\Psi}{\longrightarrow} \mathcal{O}(G) \otimes_k \mathcal{O}(G) \stackrel{\epsilon^\ast \otimes_k \epsilon^\ast}{\longrightarrow} k \otimes_k k \simeq k
   $$

   is the counit of the Hopf algebra (hence the formal dual of the neutral element)

1. the parity involution $\mathcal{O}(G) \stackrel{\simeq}{\longrightarrow} \mathcal{O}(G)$ conincides with the composite

   $$
     \mathcal{O}(G)
       \stackrel{(id \otimes_k \Psi) \circ \Psi}{\longrightarrow}
    \mathcal{O}(G) \otimes_k \mathcal{O}(G) \otimes_k \mathcal{O}(G)
      \stackrel{\epsilon^\ast \otimes_k id \otimes_k (c \circ \epsilon^\ast)}{\longrightarrow}
       k \otimes_k \mathcal{O}(G) \otimes_k k
   $$

=--

([Deligne 02, 0.3](#Deligne02))

+-- {: .num_example #InnerParityInBosonicSupergroup}
###### Example

For $G$ an ordinary affine [[algebraic group]], regarded as a supergroup with trivial odd-graded part, then every element $\epsilon \in Z(G)$ in the [[center]] defines an inner parity, def. \ref{InnerParity}.

=--

([Deligne 02, 0.4 i)](#Deligne02))

+-- {: .num_remark}
###### Remark

In view of remak \ref{InnerParityInBosonicSupergroup}, specifying an involutive central element in an ordinary group is a faint shadow of genuine supergroup structure. In fact such pairs are being referred to as "supergroups" in ([M&#252;ger 06](#Mueger06)).

=--

Demanding the existence of inner parity is not actually a restriction of the theory:

+-- {: .num_example}
###### Example

For $H$ any supergroup, def. \ref{Supergroup}, and $\mathbb{Z}_2 = \{id,par\}$ acting on it by parity involution, def. \ref{ParityAutomorphism}  then the [[semidirect product group]] $\mathbb{Z}_2 \ltimes G$ has inner parity, def. \ref{InnerParity}, given by $\epsilon \coloneqq par \in \mathbb{Z}_2 \hookrightarrow \mathbb{Z}_2 \ltimes G$.

=--

([Deligne 02, 0.4 ii)](#Deligne02))














### Linear super-representations as Comodules
 {#LinearRepresentationsAsComodules}

+-- {: .num_defn #CommutativeHopfAlgebroidComodule}
###### Definition

Given a [[commutative Hopf algebroid]] $\Gamma$ over $A$ (def. \ref{CommutativeHopfAlgebroidDefinitionInExplicitComponents}) in some [[tensor category]] (def. \ref{TensorCategory}), then a **left [[comodule]]** over $\Gamma$ is

1. an $A$-[[module object]] $N$ in $\mathcal{A}$ (def. \ref{ModulesInMonoidalCategory}) i;

1. an $A$-[[module]] [[homomorphism]] (co-action)

   $\Psi_N \;\colon\; N \longrightarrow \Gamma \otimes_A N$;

such that

1. (co-[[unitality]])

   $(\epsilon \otimes_A id_N) \circ \Psi_N = id_N$;

1. (co-action property)

   $(\Psi \otimes_A id_N) \circ \Psi_N = (id_\Gamma \otimes_A \Psi_N)\circ \Psi_N$.

A [[homomorphism]] between comodules $N_1 \to N_2$ is a homomorphism of underlying $A$-modules making [[commuting diagrams]] with the co-action morphism. Write

$$
  \Gamma CoMod(\mathcal{A})
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

Under the tensor product of co-modules (def. \ref{TensorProductOfComodulesOverAHopfAlgebra}), these form a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}).



+-- {: .num_defn #Superrepresentation}
###### Definition

A _[[linear representation]]_ of a [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$, def. \ref{InnerParity}, is

* a [[comodule]] $V$ (def. \ref{CommutativeHopfAlgebroidComodule}) in [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}) for the [[formal dual|formally dual]] [[commutative Hopf algebra]] $\mathcal{O}(G)$.

such that

* the innr parity element $\epsilon$ acts as the identity on $V_{even}$ and by multiplicatin with $-1$ on $V_{odd}$.

=--


+-- {: .num_example}
###### Example

For $G$ an ordinary (affine algebraic) group regarded as a supergroup with trivial odd-graded part, and for $\epsilon = e $ its [[neutral element]] taken as the inner parity, then $Rep(G,\epsilon)$ in the sense of def. \ref{Superrepresentation} is just the ordinary [[category of representations]] of $G$.

=--

([Deligne 02, 0.4 i)](#Deligne02))

+-- {: .num_prop #RegularTensorCategoriesOfSuperrepresentations}
###### Proposition

The [[category of representations]] $Rep(G,\epsilon)$ of def. \ref{Superrepresentation} of an affine algebraic [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$ (def. \ref{InnerParity}) on finite-dimensional super vector spaces (example \ref{FiniteDimensionalSuperVectorSpaces}) and equippd with the tensor product of comodules from def. \ref{TensorProductOfComodulesOverAHopfAlgebra} is a $k$-[[tensor category]] (def. \ref{TensorCategory}) of subexponential growth (def. \ref{SubexponentialGrowth}).

=--

([Deligne 02, 1.21](#Deligne02))

Moreover, any finite dimensional [[faithful representation]] (which always exists, [prop.](faithful+representation#AlgebraicGroupHasFinDimFaithfulRepresentations)) serves as an $\otimes$-generator (def. \ref{FiniteTensorGeneration}).

See ([this prop.](faithful+representation#AnyFinDimRepOfAffineAlgebraicGroupOverFieldIsSubquotientsOfFaithfulRep)).



### Super Fiber functors and their automorphism supergroups
 {#FiberFunctors}

The first step in exhibiting a given [[tensor category]] $\mathcal{A}$ as being a [[category of representations]] is to exhibit its objects as having an [[forgetful functor|underlying]] representation space of sorts, and then an [[action]] represented on that space. Hence a necessary condition on $\mathcal{A}$ is that there exists a [[forgetful functor]]

$$
   \omega \;\colon\; \mathcal{A} \longrightarrow \mathcal{V}
$$

to some other [[tensor category]], such that $\omega$ satisfies a list of properties, in particular it should be a [[symmetric monoidal functor|symmetric]] [[strong monoidal functor]].

Such functors are called _[[fiber functors]]_. The idea is that we think of $\mathcal{A}$ as a [[bundle]] over $\mathcal{V}$, and over each $V \in \mathcal{V}$ we find the [[fiber]] $\omega^{-1}(V)$ of that bundle, consisting of all those objects in $\mathcal{A}$ whose underlying object in the given $V$.

The main point of [[Tannaka duality]] of tensor categories is the observation that if $\mathcal{A}$ is a [[category of representations]] of some [[group]] $G$, then $G$ also [[action|acts]] by [[automorphisms]] on that [[fiber functor]] (i.e. via [[natural isomorphisms]] of functors). In good cases then this may be turned around, and the full [[automorphism group]] of a fiber functor is identified with the group $G$ for which the objects in its fibers are [[representations]], this is the process of [[Tannaka reconstruction]].

There are slight variants on what one requires of a fiber functor. For the present purpose we fix the following definition

+-- {: .num_defn #FiberFunctor}
###### Definition

Let $\mathcal{A}$ and $\mathcal{T}$ be two $k$-[[tensor categories]] (def. \ref{TensorCategory}) such that

1. all [[object of finite length|objects have finite length]];

1. all [[hom spaces]] are of [[finite number|finite]] [[dimension]] over $k$.

Let $R \in CMon(Ind(\mathcal{T}))$ be a [[commutative monoid in a symmetric monoidal category|commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}) in the category of [[ind-objects]] in $\mathcal{T}$ (prop. \ref{IndObjectsInATensorCategory}).

Then a **[[fiber functor]] on $\mathcal{A}$ over $R$** is a [[functor]]

$$
  \omega \;\colon\; \mathcal{A} \longrightarrow R Mod(Ind(\mathcal{T}))
$$

from $\mathcal{A}$ to the [[category of modules|category of]] [[module objects]] over $R$ (def. \ref{ModulesInMonoidalCategory}) in the [[category of ind-objects]] $Ind(\mathcal{T})$ (def. \ref{IndObjectsInATensorCategory}), which is

1. a [[braided monoidal functor|braided]] [[strong monoidal functor]];

1. an [[exact functor]] in both variables.

If here $\mathcal{T} = $ [[sFinDimVect]] (def. \ref{FiniteDimensionalSuperVectorSpaces}), then this is called a **super fiber functor**.

=--

([Deligne 02, 3.1](#Deligne02))


+-- {: .num_defn #TannakianCategory}
###### Definition

A [[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) is called

1. a **neutral [[Tannakian category]]** if it admits a fiber functor (def. \ref{FiberFunctor}) to $Vect_k$ (example \ref{VectAsAMonoidalCategory}) ([Deligne-Milne 12, def. 2.19](#DeligneMilne12))

1. a **neutral super [[Tannakian category]]** if it admits a fiber functor (def. \ref{FiberFunctor}) to $sVect_k$ (def. \ref{CategoryOfSuperVectorSpaces})

1. (not needed here) a general **[[Tannakian category]]** if the [[stack]] on $Aff_k$ which sends $R \in CRing$ to the groupoid of fiber functors to $R Proj \hookrightarrow R Mod$ ([[projective modules]] over $R$) is an affine [[gerbe]] such that its category of representations is equivalent to $\mathcal{A}$ ([Deligne-Milne 12, def. 3.7](#DeligneMilne12)).

=--




Given a super fiber functor $\omega \colon \mathcal{A} \to sVect_k$ (def. \ref{FiberFunctor}) there is an evident notion of its [[automorphism group]]: a [[homomorphism]] between [[functors]] is a [[natural transformation]], and that between [[monoidal functors]] is a [[monoidal natural transformation]], according to def. \ref{LaxMonoidalFunctor}, and this is an [[automorphism]] of functors if it is a [[natural automorphism]]. We write

$$
  Aut(\omega) \in Grp
$$

for this automorphism group.

So far this is a group without geometric structure (a [[discrete group]]). But it is naturally equipped with [[supergeometry]] (super-[[algebraic geometry]]) exhibited by a rule for what the geometrically parameterized families of its elements are. (For exposition of this perspective see at _[[motivation for sheaves, cohomology and higher stacks]]_).


Concretely, this means that for each [[supercommutative superalgebra]] $A$ with corresponding affine [[super scheme]] $Spec(A)$ (def. \ref{Affines}, def. \ref{SupercommutativeSuperalgebra}) we are to say what the set

$$
  \underline{Aut}(\omega)(Spec(A))
   \in
  Set
$$

of $Spec(A)$-parameterized elements of $Aut(\omega)$ is. In fact, under parameter-wise multiplication in the group, any such set must inherit group structure, so that we should have not one discrete group, but a system of them, labeled by supercommutative superalgebras:

$$
  \underline{Aut}(\omega)(Spec(A))
   \in
  Grp
  \,.
$$

Moreover, if $A_1 \longrightarrow A_2$ is an algebra homomorphism, hence

$$
  Spec(A_2) \longrightarrow Spec(A_1)
$$

a map of affine super schemes according to def. \ref{SupercommutativeSuperalgebra}, then there should be a group homomorphism

$$
  \underline{Aut}(\omega)(Spec(A_2))
    \longleftarrow
  \underline{Aut}(\omega)(Spec(A_1))
$$

that expresses how a $Spec(A_1)$-parameterized family of elements of $Aut(\omega)$ becomes a $Spec(A_1)$-parameterized family, under this map.

For a minimum of consistency, this assignment must be such that the identity map on $Spec(A)$ induces the identity on $\underline{Aut}(\omega)(Spec(A))$, and that the composite of two maps of affine superschemes goes to the correspondng composite group homomorphisms.

In conclusion, this says that an algebraic supergeometric structure on $Aut(\omega)$ is the datum of a [[presheaf]] of groups, hence of a [[functor]]

$$
  \underline{Aut}(\omega)
   \;\colon\;
  Aff(sVect)^{op} \simeq CMon(sVect)
   \longrightarrow
  Grp
$$

such that the underlying points are those of $Aut(\omega)$:

$$
  \underline{Aut}(\omega)(Spec(k))
  \simeq
  Aut(\omega)
  \,.
$$


+-- {: .num_defn #RepresentableAutomorphismGroup}
###### Definition

We say that a functor

$$
  \underline{Aut}(\omega)
   \;\colon\;
  Aff(sVect)^{op}
    =
  CMon(sVect)
     \longrightarrow
  Grp
$$

is **[[representable functor|representable]]** if there exists a [[supercommutative Hopf algebra]] $H$, hence an affine [[algebraic group]] $Spec(H)$ (def. \ref{Supergroup}) and a [[natural isomorphism]] with the [[hom functor]] into $Spec(H)$:


$$
  \underline{Aut}(\omega)
  \simeq
  Hom_{CMon(sVect)}(H,-)
    =
  Hom_{Aff(sVect)}(-,Spec(H))
  \,.
$$


=--

+-- {: .num_defn #AutomorphismGroupOfFiberFunctor}
###### Definition

Let $\omega \colon \mathcal{A} \to \mathcal{B}$ be a  [[fiber functor]]  (def \ref{FiberFunctor}).

For $A \in CMon(\mathcal{B})$ a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}), write

$$
  \omega_A
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  \mathcal{B}
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(\mathcal{B})
$$

for its image under [[extension of scalars]] along $1 \to A$ to $A$ (prop. \ref{ExtensionOfScalars}).

With this, the **automorphism group** of $\omega$

$$
  \underline{Aut}(\omega)
  \in
  PSh(Aff(\mathcal{B}))
$$

is defined to be the functor which on objects assigns the [[discrete group]] of [[natural automorphisms]] of the image $\omega_A$ of $\omega$ under [[extension of scalars]] as above

$$
  \underline{Aut}(\omega)(Spec(A))
   \coloneqq
  Aut(\omega_{A})
$$

and which to a homomorphism of algebras

$$
  \phi \;\colon\; A_1 \longrightarrow A_2
$$

assigns the action of the [[extension of scalars]]-functor along $\phi$:

$$
  \phi_\ast
    \;\colon\;
  Aut(\omega_{A_1})
    \longrightarrow
  Aut(\omega_{A_2})
  \,.
$$

This is clearly a presheaf, by [[functor|functoriality]] of [[extension of scalars]].


=--

Specializing def. \ref{AutomorphismGroupOfFiberFunctor} to $\mathcal{B} = $ [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}), where a commutative monoid is a [[supercommutative superalgebra]] (def. \ref{SupercommutativeSuperalgebra}) it reads as follows:

+-- {: .num_example #AutomorphismSuperGroupOfSuperFiberFunctor}
###### Example

Let $\omega \colon \mathcal{A} \to sVect$ be a  [[fiber functor|super fiber functor]]  (def \ref{FiberFunctor}).

For $A \in CMon(sVect)$ a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}), write

$$
  \omega_A
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  sVect
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(sVect)
$$


For $A \in CMon(sVect)$ a [[supercommutative algebra]], write

$$
  \omega_A
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  sVect
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(sVect)
$$

for its image under [[extension of scalars]] to $A$ (prop. \ref{MonoidModuleOverItself}).

With this, the **automorphism super-group** of $\omega$

$$
  \underline{Aut}(\omega)
  \in
  PSh(Aff(sVect))
$$

is defined by

$$
  \underline{Aut}(\omega)(Spec(A))
   \coloneqq
  Aut(\omega_{A})
  \,.
$$

=--



+-- {: .num_prop #AutomorphismSupergroupOfFiberFunctorIsRepresentable}
###### Proposition

For $k$ an [[algebraically closed field]] of [[characteristic zero]], and for $\mathcal{A}$ a $k$-[[tensor category]] equipped with a [[fiber functor|super fiber functor]] $\omega$, then its automorphism supergroup (def. \ref{AutomorphismSuperGroupOfSuperFiberFunctor}) is [[representable functor|representable]] (def. \ref{RepresentableAutomorphismGroup}): there exists a [[supercommutative Hopf algebra]] $H_\omega$ and a [[natural isomorphism]]

$$
  \underline{Aut}(\omega)
    \simeq
  Hom_{CMon(sVect)}(H_\omega,-)
   =
  Hom_{Aff(sVect)}(-, Spec(H_\omega))
  \,,
$$

which, with the [[Yoneda embedding]] understood, we write simply as

$$
  \underline{Aut}(\omega)
    \simeq
  Spec(H_\omega)
  \,.
$$

=--

([Deligne 90, prop. 8.11](#Deligne90))

The following says that in fact all homomorphisms between fiber functors are necessarily [[isomorphisms]]:

+-- {: .num_lemma #MonoidalTransformationBetweenFiberFunctorIsIso}
###### Lemma

Every [[monoidal natural transformation]] (def. \ref{LaxMonoidalFunctor}) between two [[fiber functors]] (def. \ref{FiberFunctor}) is an [[isomorphism]] (i.e. a [[natural isomorphism]]).

=--

([Deligne 90, 8.11 (ii)](#Deligne90), [Deligne 02, lemma 3.2](#Deligne02))


+-- {: .num_defn #FundamentalSupergroup}
###### Definition

Let $\mathcal{A}$ be a [[tensor category]] and regard the [[identity]] functor on it as a fiber functor (def. \ref{FiberFunctor}). Then the automorphism group of $id_{\mathcal{A}}$ according to def. \ref{AutomorphismSuperGroupOfSuperFiberFunctor} is called the **fundamental group** of $\mathcal{A}$, denoted:

$$
  \pi(\mathcal{A})
   \coloneqq
  \underline{Aut}(id_{\mathcal{A}})
$$


=--

([Deligne 90, 8.12, 8.13](#Deligne90))

+-- {: .num_example #FundamentalGroupOfCategoryOfSuperVectorSpaces}
###### Example

The fundamental group (def. \ref{FundamentalSupergroup}) of the [[category of super vector spaces]] [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}) is $\mathbb{Z}/2$:

$$
  \pi(sVect)
    \simeq
  \mathbb{Z}/2
  \,.
$$

The non-trivial element in $\pi(sVect)$ acts on any super-vector space as the [[endomorphism]] which is the identity on even graded elements, and multiplication by $(-1)$ on odd graded elements.

=--

([Deligne 90, 8.14 iv)](#Deligne90))

+-- {: .num_prop #AutOfFibFuncIsImagUnderFibFuncOfFundamentalGroup}
###### Proposition

For $\mathcal{A}$ a $k$-[[tensor category]] equipped with a [[fiber functor|super fiber functor]] $\omega \colon \mathcal{A} \to sVect$ (def. \ref{FiberFunctor}), then the automorphism supergroup of $\omega$ is the image under the super fiber functor $\omega$ of the fundamental group of $\mathcal{A}$, according to def. \ref{FundamentalSupergroup}:

$$
  \underline{Aut}(\omega)
    \simeq
  \omega(\pi(\mathcal{A}))
  \,.
$$

Here on the right we are using that $\omega$ is a [[strong monoidal functor]] so that it preserves
[[commutative monoids]] as well as [[comonoids]] by prop. \ref{MonoidsPreservedByLaxMonoidalFunctor},
hence preserves [[commutative Hopf algebras]].


=--

([Deligne 90 (8.13.1)](#Deligne90))


+-- {: .num_prop #HomomorphismFromPiT2ToEtaPiT1}
###### Proposition

Let $\mathcal{A}_1, \mathcal{A}_2$ be two $k$-[[tensor categories]] and let

$$
  \eta \;\colon\; \mathcal{A}_1 \longrightarrow \mathcal{A}_2
$$

be a [[functor]] which is $k$-linear, [[strong monoidal functor|monoidal]] and [[exact functor]]. Then there is induced a canonical group homomorphism


$$
  \pi(\mathcal{A}_2)
   \longrightarrow
  \eta(\pi(\mathcal{A}_1))
$$

from the fundamental group of $\mathcal{A}_1$ (def. \ref{FundamentalSupergroup}) to the image under $\eta$ of the fundamental group of $\mathcal{A}_2$.

=--

([Deligne 90, 8. 15. 2](#Deligne90))





### Super-exterior powers and Schur functors

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

Let $V = V_{even} \oplus V_{odd}$ be a [[super vector space]] of degreewise finite dimension $d_{even}, d_{odd} \in \mathbb{N}$. Then there exists a [[Schur functor]] $S_\lambda$ (def. \ref{SchurFunctor}) that annihilates $V$:

$$
  S_\lambda(V) \simeq 0
  \,.
$$

Specifically, this is the case precisely if the corresponding [[Young tableau]] $[\lambda]$ satifies

$$
  [\lambda] \subset \left\{ (i,j)\;\vert\; i \leq d_{even}, j \leq d_{odd} \right\}
  \,.
$$

=--

([Deligne 02, corollary 1.9](#Deligne02))


## Statement of the theorem
 {#Statement}


+-- {: .num_theorem #TheTheorem}
###### Theorem

Every $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) such that

1. $k$ is an [[algebraically closed field]] of [[characteristic zero]] (e.g. the field of [[complex numbers]])

1. $\mathcal{A}$ is of subexponential growth according to def. \ref{SubexponentialGrowth}

then $\mathcal{A}$ is a neutral super [[Tannakian category]] (def. \ref{TannakianCategory}) and  there exists

1. an affine algebraic [[supergroup]] $G$ (def. \ref{Supergroup}) whose [[algebra of functions]] $\mathcal{O}(G)$ is a [[finitely generated object|finitely generated]] $k$-algebra.

1. a tensor-[[equivalence of categories]]

   $$
     \mathcal{A}
        \simeq
     Rep(G,\epsilon)
     \,.
   $$

   between $\mathcal{A}$ and the [[category of representations]] of $G$ of finite dimension, according to def. \ref{Superrepresentation} and prop. \ref{RegularTensorCategoriesOfSuperrepresentations}.

=--

([Deligne 02, theorem 0.6](#Deligne02))

## Proof

We outline key steps of the proof of theorem \ref{TheTheorem}, given in [Deligne 02](#Deligne02).


Throughout, let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).


The proof proceeds in three main steps:

1. **Proposition \ref{LengthOfObjectIsBounded}** states that in a $k$-[[tensor category]] an object $X$ is of subexponential growth (def. \ref{SubexponentialGrowth}) precisely if there exists a [[Schur functor]] that annihilates it, hence if some power of $X$, skew-symmetrized in sme variables and symmetrized in others, vanishes.

   This proposition is where the [[symmetric group]] and its [[permutation]] [[action]] on [[tensor powers]] appears, from just a kind of finite-dimensionality assumption.

1. **Proposition \ref{SchurFinitenessImpliesExistenceOfSuperFiberFunctor}** in turn says that if every object in $\mathcal{A}$ is annihilated by some [[Schur functor]], then there exists a super [[fiber functor]] on $\mathcal{A}$ over some [[supercommutative superalgebra]] $R$, hence then every object of $\mathcal{A}$ has underlying it a [[super vector space]] with some extra structure.

   This proposition is where [[superalgebra]] proper appears.

1. **Proposition \ref{DeligneTannakaReconstruction}** states that every $k$-[[tensor category]] equipped with a super fiber functor $\omega \colon \mathcal{A} \to sVect$, is equivalent to the category of super-representations of the automorphism supergroup of $\omega$.

   This proposition is the instance of general [[Tannaka reconstruction]] applied to the case of fiber functors with values in super vector spaces. This is where the "supersymmetry" supergroup is extracted.


+-- {: .num_prop #LengthOfObjectIsBounded}
###### Proposition

For $\mathcal{A}$ a $k$-[[tensor category]] (def. \ref{TensorCategory}), then the following are equivalent:

1. the category $\mathcal{A}$ has subexponential growth (def. \ref{SubexponentialGrowth});

1. for every object $X \in \mathcal{A}$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, on $X$ vanishes: $S_\lambda(X) = 0$.

=--

([Deligne 02, prop. 05](#Deligne02))


+-- {: .num_prop #SchurFinitenessImpliesExistenceOfSuperFiberFunctor}
###### Proposition

If for every object of a $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) there exists a [[Schur functor]] (def. \ref{SchurFunctor}) that annihilates it, then there exists a [[fiber functor|super fiber functor]] (def. \ref{FiberFunctor}) over $k$,
hence then $\mathcal{A}$ is a neutral super [[Tannakian category]] (def. \ref{TannakianCategory}).

$$
  \omega
    \;\colon\;
  \mathcal{A}
    \longrightarrow
  sVect
  \,.
$$

=--

([Deligne 02, prop. 2.1 "r&#233;sultat cl&#233; de l'article", together with prop. 4.5](#Deligne02))

+-- {: .proof}
###### Proof idea

First ([Deligne 02, middle of p. 16](#Deligne02)) consider the [[tensor category]]

$$
  s \mathcal{A}
    \coloneqq
  (\mathcal{A}^{\mathbb{Z}/2}, \tau_{super} )
$$

which is that of $\mathbb{Z}/2$-graded objects of $\mathcal{A}$, and whose [[braiding]] is given on objects $X,Y$ of homogeneous degree by that of $\mathcal{A}$ multiplied with $(-1)^{deg(X) deg(Y)}$.

Write $1$ and $\overline{1}$ for the [[tensor unit]] of $\mathcal{A}$, regarded in even degree and in odd degree in $s \mathcal{A}$, respectively.

For $A \in CMon(\mathcal{A})$ a [[commutative monoid]], write

$$
  \mathcal{A}
  \simeq
  1 Mod(\mathcal{A})
     \underoverset{\underset{U}{\longleftarrow}}{\overset{(-)_A \coloneqq F}{\longrightarrow}}
 {}
  A Mod(\mathcal{A})
$$

for the [[extension of scalars]] operation $A \otimes(-)$, [[left adjoint]] to [[restriction of scalars]] (prop. \ref{ExtensionOfScalars}).

Show then that the condition that an object $X$ is annihilated by some [[Schur functor]] is equivalent to the existence of an algebra $A$ such that

$$
  X_A \simeq 1^p \oplus \overline{1}^q
$$

for some $p,q \in \mathbb{N}$, hence that each such object is _$A$-locally_ a [[super vector space]].

([Deligne 02, prop. 2.9](#Deligne02)).

Moreover, for each [[short exact sequence]]

$$
  0 \to X \to Y \to Z \to 0
$$

in $s \mathcal{A}$, there exists an algebra $A$ such that

$$
  0 \to X_A \to Y_A \to Z_A \to 0
$$

is a [[split exact sequence]], (hence every short exact sequence is _locally_ split).

([Deligne 90, 7.14](#Deligne90), [Deligne 02, rappel 2.10](#Deligne 02))

Now ([Deligne 02, middle of p. 17](Deligne02)) let $A$ be the commutative monoid which is the [[tensor product]] of commutative monoids (example \ref{TensorProductOfTwoCommutativeMonoids}) over all [[isomorphism classes]] of [[objects]] and of [[short exact sequences]] in $\mathcal{A}$ of choices of commutative monoids for which these objects/exact sequencs are locally split, as above.

Then for an $A$-module $N$, write $\rho(N)$ for the [[subobject]] of $N$ inside $sVect \simeq Ind\langle 1, \overline{1}\rangle \hookrightarrow s \mathcal{A}$.

Check ([Deligne 02, bottom of p. 17](Deligne02)) that $\rho(A)$ inherits the structure of a commutative monoid, and that $\rho(N)$ inherits the structure of a module over $\rho(N)$.

Set

$$
  R \coloneqq \rho(A)
  \,.
$$

Hence for every object $X$, then

$$
  \omega(X)
    \coloneqq
  \rho(X_A)
$$

has the structure of an $R$-module. By $A$-local splitness of all short exact sequence, $\omega$ is an [[exact functor]].

Hence

$$
  \omega \;\colon\; s \mathcal{A} \longrightarrow R Mod(sVect)
$$

is a super fiber functor on $s\mathcal{A}$ over $R$. This restricts to a super fiber functor over $R$ on  $\mathcal{A}$, regarded as the sub-category of even-graded objects in $s \mathcal{A}$:

$$
  \mathcal{A}
    \hookrightarrow
  s \mathcal{A}
   \overset{\omega}{\longrightarrow}
  R Mod(sVect)
  \,,
$$

Finally check ([Deligne 02, prop. 4.5](#Deligne02)) that
if a $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) admits a [[fiber functor|super fiber functor]] (def. \ref{FiberFunctor}) over a [[supercommutative superalgebra]] $R$ over $k$

$$
  \mathcal{A}
    \longrightarrow
  R Mod(sVect)
$$

then it also admits a super fiber functor over $k$ itself, i.e. a fiber functor to [[sVect]]

$$
  \mathcal{A}
    \longrightarrow
  k Mod(sVect)
  \simeq
  sVect
  \,.
$$

This is argued by expressing $R$ as an [[inductive limit]]

$$
  R = \underset{\longrightarrow}{\lim}_\beta R_\beta
$$

over [[supercommutative superalgebras]] $R_\beta$ of finite type over $k$ and observing (...) that there exists $\beta$ such that $\omega_\beta$ is still a fiber functor and such that there exists an algebra homomorphism $R_\beta \to k$.

Finally then the fiber functor in question is

$$
  \omega_\beta \otimes_{R_\beta} k
   \;\colon\;
  \mathcal{A}
    \longrightarrow
  sVect_k
  \,.
$$

=--

+-- {: .num_prop #DeligneTannakaReconstruction}
###### Proposition

For every $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) and a [[fiber functor|super fiber functor]] over $k$ (def. \ref{FiberFunctor})

$$
  \omega
    \;\colon\;
   \mathcal{A}
     \longrightarrow
   sVect_k
$$

then $\omega$ induces an [[equivalence of categories]]

$$
  \mathcal{A}
     \stackrel{\simeq}{\longrightarrow}
   Rep( \underline{Aut}(\omega),\epsilon)
$$

of $\mathcal{A}$ with the [[category of representations|category of finite dimensional representations]], according to def. \ref{Superrepresentation} and prop. \ref{RegularTensorCategoriesOfSuperrepresentations}, of the automorphism supergroup $\underline{Aut}(\omega)$ (example. \ref{AutomorphismSuperGroupOfSuperFiberFunctor}, prop. \ref{AutomorphismSupergroupOfFiberFunctorIsRepresentable}) of the super fiber functor, where $\epsilon$ is te image of the unique nontrivial element in

$$
  \underline{Aut}(sVect) \simeq \mathbb{Z}/2
$$

(according to example \ref{FundamentalGroupOfCategoryOfSuperVectorSpaces}) under the group homomorphism

$$
  \pi(sVect) \longrightarrow \omega(\pi(\mathcal{A}))
  \simeq \underline{Aut}(\omega)
$$

from prop. \ref{HomomorphismFromPiT2ToEtaPiT1} and using the isomorphism from prop. \ref{AutOfFibFuncIsImagUnderFibFuncOfFundamentalGroup}.

=--


This is the main [[Tannaka reconstruction]] theorem ([Deligne 90, 8.17](#Deligne90))
specialized to super fiber functors ([Deligne 90, 8.19](#Deligne90)).



## References

The theorem is due to

* {#Deligne02} [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf), [[DeligneTensorCategories02.pdf:file]])

building on the general results on [[Tannakian categories]] in

* {#Deligne90} [[Pierre Deligne]], _[[Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp. 111-195 ([pdf](https://publications.ias.edu/sites/default/files/60_categoriestanna.pdf))

which are reviewed and further generalized in

* {#DeligneMilne12} [[Pierre Deligne]], [[James Milne]], _Tannakian categories_, 2012 ([pdf](http://www.jmilne.org/math/xnotes/tc.pdf))

Review is in

* {#Ostrik04} [[Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))

* {#EGNO15} [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], section 9.11 in _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf))

Further discussion in view of the theory of [[triangular Hopf algebras]] is in

* {#EtingofGelaki02} [[Pavel Etingof]], [[Shlomo Gelaki]], _The classification of finite-dimensional triangular Hopf algebras over an algebraically closed field of characteristic 0_ ([arXiv:0202258](https://arxiv.org/abs/math/0202258))


Tannaka duality for ordinary compact groups regarded as supergroups (hence equipped with "inner parity", def. \ref{InnerParity}, here just being an involutive central element) is discussed in

* {#Mueger06} [[Michael Müger]], _Abstract Duality Theory for Symmetric Tensor $*$-Categories_ appendix ([pdf](http://www.math.ru.nl/~mueger/PDF/16.pdf)), in [[Hans Halvorson]],  _Algebraic quantum field theory_ ([arXiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036)), in J. Butterfield & J. Earman (eds.) _Handbook of Philosophy and Physics_

as a proof of [[Doplicher-Roberts reconstruction]]

Commutative algebra internal to symmetric monoidal categories is discussed in

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], _Rings, modules and algebras in stable homotopy theory_, AMS 1997, 2014

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))

and specifically for [[commutative Hopf algebroids]] in

* {#Ravenel86} [[Doug Ravenel]], chapter 2 and appendix A.1 of  _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))

(These authors are motivated by the application of the general theory of algebra in monoidal categories
to "[[higher algebra]]" ("[[brave new algebra]]") in [[stable homotopy theory]].
This happens to also be a version of [[supercommutative superalgebra]], see at
_[[Introduction to Stable homotopy theory]]_ the section [1-2 Homotopy commutative ring spectra](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyRingSpectra).)

For an attempt to generalize Deligne's theorem to [[positive characteristic]], see

* [[Victor Ostrik]], _On symmetric fusion categories in positive characteristic_, ([arXiv:1503.01492](https://arxiv.org/abs/1503.01492))

This was realised for [[Frobenius exact category|Frobenius exact]] tensor categories in [[positive characteristic]] in:

* {#CoulembierEtingofOstrik21} [[Kevin Coulembier]], [[Pavel Etingof]], [[Victor Ostrik]], _On Frobenius exact symmetric tensor categories_ $[$[arXiv:2107.02372](https://arxiv.org/abs/2107.02372)$]$

where $Vect$ and $sVect$ are replaced by more exotic targets.

Discussion relating to [[2-rings]] and the [[spin-statistics theorem]] is in

* {#JohnsonFreyd15} [[Theo Johnson-Freyd]], _Spin, statistics, orientations, unitarity_, Algebraic and Geometric Topology ([arXiv:1507.06297](https://arxiv.org/abs/1507.06297))

On Deligne categories:

* {#Hu24} Serina Hu. *An Introduction to Deligne Categories* (2024). ([arXiv:2404.08689](https://arxiv.org/abs/2404.08689)).

[[!redirects Deligne theorem on tensor categories]]

[[!redirects Deligne reconstruction theorem]] 




