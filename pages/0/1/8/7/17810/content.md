
> this entry contains one section of _[[geometry of physics -- supergeometry]]_


#Contents#
* table of contents
{:toc}


In [[nLab:Klein geometry]] and [[nLab:Cartan geometry]] the fundamental geometric concept is the [[nLab:symmetry group]] $G$ of the local model [[nLab:space]], which is then recovered as some [[nLab:coset space]] $G/H$. These symmetry groups $G$ are reflected in their [[nLab:categories of representations]] $Rep(G)$, which are certain nice [[nLab:tensor categories]]. In terms of [[nLab:physics]] via [[nLab:Wigner classification]], the [[nLab:irreducible objects]] in  $Rep(G)$ label the possible [[nLab:fundamental particle]] species on the [[nLab:spacetime]] $G/H$. Hence if we regard the [[nLab:tensor category]] $Rep(G)$ as the actual fundamental concept, then the natural question is that of _[[nLab:Tannaka duality|Tannaka reconstruction]]_: Given any nice [[nLab:tensor category]], is it [[nLab:equivalence of categories|equivalent]] to $Rep(G)$ for some symmetry group $G$? For [[nLab:rigid monoidal category|rigid]] [[nLab:tensor categories]] in [[nLab:characteristic zero]] subject only to a mild size constraint this is answered by **[[nLab:Deligne's theorem on tensor categories]]** (theorem \ref{TheTheorem} below) : all of them are, but only if we allow $G$ to be a "[[nLab:supergroup]]".


## **Model layer**


### Superalgebra
  {#Superalgebra}

The beauty of [[supercommutative superalgebra]] is that it is just [[commutative algebra]]
"[[internalization|internal]]" to the [[tensor category]] of [[super vector spaces]].
For instance an (affine algebraic) [[supergroup]] (i.e. super [[symmetry group|symmetry-group]], i.e. a [[supersymmetry|super-symmetry]] group)
is just a [[commutative Hopf algebra]] internal to super vector spaces.
The beauty of [[super vector spaces]], in turn, is that these are just $\mmathbb{Z}/2$-[[graded vector spaces]]
equipped with the _unique_ non-trivial [[symmetric monoidal category|symmetric braiding]].
Better yet, _all_ [[tensor categories]] subject to a mild size constraint are [[equivalence of categories|equivalently]]
[[categories of representations]] of [[supergroups]]. This is the main theorem of this section, theorem \ref{TheTheorem}
below ([[Deligne's theorem on tensor categories]]).

<img src="https://ncatlab.org/schreiber/files/DeligneSuperFiberFunctor.png" width="600">

Here we introduce and explain all this.

We start by introducing the basic concepts of [[tensor categories]] along with the basic examples of [[vector spaces]] and [[super vector spaces]]:

* _[Tensor products and Tensor categories](#TensorProductsAndMonoidalCategories)_

This allows to speak of [[commutative algebra]] [[internalization|internal]] to tensor categories. Specializing this to the tensor category of [[super vector spaces]] yields [[supercommutative superalgebras]]. The [[formal duals]] of these are the [[affine variety|affine]] [[super schemes]]. This we discuss in

* _[Commutative algebra in tensor categories and Affine super-spaces](#CommutativeAlgebraInTensorCategories)_


In the same dual spirit, [[super vector bundles]] over affine [[super schemes]] are algebraically
incarnated as ([[finitely generated object|finitely generated]] [[projective module|projctive]]) [[modules]]
over [[supercommutative superalgebras]]. This we discuss in

* _[Modules in tensor categories and Super vector bundles](#ModulesInTensorCategories)

Next we introduce the concept of [[commutative monoids]] equipped with the structure of a [[commutative Hopf algebras]] and explain how these are [[formal duals]] to [[group objects|groups]]. Then we use this to motivate and explain the concept of (affine algebraic) [[supergroups]] as [[formal duals]] to [[commutative Hopf algebras]] internal to the tensor category of [[super vector spaces]], namely [[supercommutative Hopf algebras]]:

* _[Super-Groups as Super-commutative Hopf algebras](#GroupsAsHopfAlgebras)_

Then we discuss how under this relationo, then [[linear representations]] of groups correspond to [[comodules]] over their formally dual [[commutative Hopf algebras]], and we introduce the key class of categories of interest here: tensor-[[categories of representations]] of groups and of super-representations of super-groups:

* _[Linear super-representations as comodules](#LinearRepresentationsAsComodules)_

All such [[categories of representations]] carry a [[fiber functor]]: the [[forgetful functor]] that sends
any representation to its underlying representation space. Simple as this is, fiber functors turn out to be
the key concept in [[representation theory]]. Notably, every _abstractly_ defined super fiber functor gives rise
to an affine algebraic supergroup, namely its [[automorphism group]]. We introduce the basics in

* _[Super Fiber functors and their automorphism supergroups](#FiberFunctors)_

And in fact, under mild conditions this supergorup  of automorphisms of the fiber functor of a tensor category
is such that the tensor category is equivalently its [[category of representations]]. This
statement of [[Tannaka duality]] for [[complex numbers|complex]]-linear tensor categories,
due to [[Pierre Deligne]] gives [[superalgebra]] a [[general abstract]] _raison d'&#234;tre_. We state
the theorem and give some broad indication as to how the proof proceeds in the last sub-section

* _[Tannaka duality between tensor categories and supergroups](#TannakaDualityForTensorCategoriesAndSupergroups)_


#### Tensor products and Tensor categories
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

1. Say that $\mathcal{C}$ has **[[direct sums]]** if it has [[finite products]] and [[finite coproducts]] and if the canonical comparison  morphism between these is an [[isomorphism]]. We write $V \oplus W$ for the direct sum of two objects of $\mathcal{C}$ in this.

1. Say that $\mathcal{C}$ is an **[[additive category]]** if it has [[direct sums]] and in addition it is [[Ab-enriched category|enriched in abelian groups]], meaning that every [[hom-set]] is equipped with the structure of an [[abelian group]] such that [[composition]] of morphisms is a [[bilinear map]].

1.Say that $\mathcal{C}$ is an **[[abelian category]]** if it is an [[additive category]] and has property that its [[monomorphisms]] are precisely the inclusions of [[kernels]] and its [[epimorphisms]] are precisely the projections onto [[cokernels]].

=--

We also make the following definition of $k$-linear category, but notice that conventions differ as to which extra properties beyond [[Vect]]-[[enriched category|enrichment]] to require on a linear category:

+-- {: .num_defn #LinearCategory}
###### Definition

For $k$ a [[field]] (or more generally just a [[commutative ring]]), call a [[category]] $\mathcal{C}$ a **$k$-[[linear category]]** if

1. it is an [[abelian category]] (def. \ref{AdditiveAndAbelianCategories});

1. its [[hom-sets]] have the structure of $k$-[[vector spaces]] (generally $k$-[[modules]]) such that [[composition]] of morphisms in $\mathcal{C}$ is a [[bilinear map]]

and the underlying additive [[abelian group]] structure of these [[hom-spaces]] is that of the underlying [[abelian category]].

In other words, a $k$-linear category is an [[abelian category]] with the additional structure of a [[Vect]]-[[enriched category]] (generally $k$[[Mod]]-enriched) such that the underlying [[Ab-enriched category|Ab-enrichment]] according to def. \ref{AdditiveAndAbelianCategories} is obtained from the $Vect$-enrichment under the [[forgetful functor]] $Vect \to Ab$.

A [[functor]] between $k$-linear categories is called a **$k$-[[linear functor]]** if its component functions on [[hom-sets]] are [[linear maps]] with respect to the given $k$-linear structure.

=--

+-- {: .num_example}
###### Example

The category [[Vect]]${}_k$ of [[vector spaces]] (def. \ref{VectorSpaces}) is a $k$-[[linear category]] according to def. \ref{LinearCategory}.

Here the abstract [[direct sum]] is the usual direct sum of [[vector spaces]], whence the name of the general concept.

For $V,W$ two $k$-vector spaces, the vector space structure on the [[hom-set]] $Hom_{Vect}(V,W)$ of [[linear maps]] $\phi \colon V \to W$ is given by "pointwise" multiplication and addition of functions:

$$
  (k_1 \phi_1 + k_2 \phi_2)
  \;\colon\,
   v \;\mapsto\;
   k_1 \phi_1(v) + k_2 \phi_2(v)
  \,.
$$


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

(Here the qualifier "freely" means informally that we must not use any non-formal identification between objects, and formally it means that the diagram in question must be in the image of a [[strong monoidal functor]] from a _free_ monoidal category. For example if in a particular monoidal category it so happens that the object $X \otimes (Y \otimes Z)$ is actually _equal_ to $(X \otimes Y)\otimes Z$, then the various ways of going from one expression to another using only associators _and_ this "accidental" equality no longer need to coincide.)

=--

The above discussion makes it clear that a [[monoidal category]] is like a [[monoid]]/[[semi-group]], but "[[categorified]]". Accordingly we may consider additional properties of [[monoids]]/[[semi-groups]] and correspondingly lift them to monoidal categories. A key such property is _[[commutative ring|commutativity]]_. But while for a monoid, commutativity is just an extra [[property]], for a [[monoidal category]] it involves choices of commutativity-[[isomorphisms]] and hence is [[stuff, structure and property|extra structure]]. This might  seem like a subtle point, but in fact, as we will see [below](#SuperGroupsAsSuperHopfAlgebras), this is the very source of [[superalgebra]].

The [[categorification]] of "commutativity" comes in two stages, [[braiding]] and [[symmetric monoidal category|symmetric braiding]].

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

for the [[full subcategory]] on those $L \in \mathcal{C}$ which are [[invertible objects]] under the [[tensor product]], i.e. such that there is an object $L^{-1} \in \mathcal{C}$ with $L \otimes L^{-1} \simeq 1$ and $L^{-1} \otimes L \simeq 1$. Since the [[tensor unit]] is clearly in $Line(L)$ (with $1^{-1} \simeq 1$) and since with $L_1, L_2 \in Line(\mathcal{C}) \hookrightarrow \mathcal{C}$ also $L_1 \otimes L_2 \in Line(\mathcal{C})$ (with $(L_1 \otimes L_2)^{-1} \simeq L_2^{-1} \otimes L_1^{-1}$) the [[monoidal category]] structure on $\mathcal{C}$ restricts to $Line(\mathcal{C})$.


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
  k^{0 \vert 1} \otimes_k k^{0 \vert 1} \simeq k^{1 \vert 0}
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
  \trunc_1 \Omega \mathbb{S}
  \,.
$$

It has been suggested (in [Kapranov 15](super+algebra#Kapranov15)) that this and other phenomena are evidence that in the wider context of [[homotopy theory]]/[[stable homotopy theory]] super-grading (and hence [[superalgebra]]) is to be regarded as but a shadow of grading in [[higher algebra]] over the [[sphere spectrum]]. Notice that the [[sphere spectrum]] is just the analog of the group of [[integers]] in [[stable homotopy theory]].

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
    \hookrightarrow
  (sVect, \otimes_k, k, \tau^{super})
$$

of the [[symmetric monoidal category]] of [[super vector spaces]] from example \ref{CategoryOfSuperVectorSpaces}, on those of finite total dimension is a [[rigid monoidal category]].

Here we say that a [[super vector space]] $V$ has [[dimension]

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

We consider now various types of size constraints on tensor categories. The Tannaka reconstructin theorem (theorem \ref{TheTheorem} below) only assumes one of them (subexponential growth, def. \ref{SubexponentialGrowth}), but the others appear in the course of the proof of the theorem.

1. finiteness (def. \ref{FiniteTensorCategory})

1. finite $\otimes$-generation (def. \ref{FiniteTensorGeneration})

1. subexponential growth (def. \ref{SubexponentialGrowth})

Recall the concept of [[length of an object]] in an [[abelian category]], a generalization of the concept of [[dimension]] of a [[free module]]/[[vector space]].


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

The tensor category $k$-[[FinVect]] of [[finite dimensional vector spaces]] from example \ref{FiniteDimensionalVectorSpaces} has subexponential growth (def. \ref{SubexponentialGrowth}), for $N_X = dim(X)$ the [[dimension]] of a vector space $X$, we have

$$
  dim\left( X^{\otimes^n} \right) = \left(dim(X)\right)^n
  \,.
$$

=--


Finally we discuss categories of [[ind-objects]] in tensor categories

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




#### Commutative algebra in tensor categories and Affine super-spaces
 {#CommutativeAlgebraInTensorCategories}

The key idea of [[supercommutative superalgebra]] is that it is nothing but plain [[commutative algebra]] but "[[internalization|internalized]]" not in ordinary [[vector spaces]], but in [[super vector spaces]]. This is made precise by def. \ref{MonoidsInMonoidalCategory} and ef. \ref{SupercommutativeSuperalgebra} below.

The key idea then of [[supergeometry]] is to define super-[[spaces]] to be spaces whose [[algebras of functions]] are [[supercommutative superalgebras]]. This is not the case for any "ordinary" space such as a [[topological space]] or a [[smooth manifold]]. But these spaces may be _characterized_ via their algebras of functions, and hence it makes sense to generalize the latter.

For [[smooth manifolds]] the statement is the following

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

This says that we may _identify_ [[smooth manifolds]] as the  "[[formal duals]]" of certain [[associative algebras]], namely those in the image of the above full embedding. Accordingly then, any larger class of associative algebras than this may be thought of as the class of [[formal duals]] to a generalized kind of manifold, defines thereby. Given any associative algebra $A$, then we think of as representing a space which is such that it has $A$ as its algebra of functions.

The [[duality]] between certain  [[spaces]] and their [[algebras of functions]] is profound. In [[physics]] it has always been used implicitly, in fact it was so ingrained into theoretical physics that it took much effort to abstract away from [[coordinate system|coordinate functions]] to discover global [[Riemannian geometry]] in the guise of"[[general relativity]]". As mathematics, an early prominent duality theorem is [[Gelfand duality]] (between [[topological spaces]] and [[C*-algebras]]) which served as motivation for the very definition of [[algebraic geometry]], where [[affine schemes]] are nothing but the [[formal duals]] of [[commutative rings]]/[[commutative algebras]]. Passing to [[non-commutative algebras]] here yields [[non-commutative geometry]], and so forth. In great generality this duality betwee spaces and their function algebras appears as "[[Isbell duality]]" between [[presheaves]] and [[copresheaves]].

In [[supergeometry]] we are concerned with spaces that are formally dual to associative algebras which are "very mildly" non-commutative, namely [[supercommutative superalgebras]], which are in fact [[commutative algebras]] when viewed internal to [[super vector spaces]]. The corresponding [[formal dual]] spaces are, depending on some technical details _[[super schemes]]_ or _[[supermanifolds]]_. In the [[physics]] literature, such spaces are usually just called _[[superspace]]_.

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

It is useful to introduce the following [[formal dual|formally dual]] perspective:

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

+-- {: .num_example #MonoidsInVectAreAssociativeAlgebras}
###### Example

A [[monoid object]] according to def. \ref{MonoidsInMonoidalCategory} in the [[monoidal category]] of [[vector spaces]] from from example \ref{TensorProductOfVectorSpaces} is equivalently an ordinary [[associative algebra]] over the given [[ground field]]. Similarly a [[commutative monoid]] in $Vect$ is an ordinary [[commutative algebra]]. Moreover, in both cases the [[homomorphisms]] of monoids agree with usual algebra homomorphisms. Hence there are [[equivalences of categories]].

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
  sCalg_k \;\colon\; CMon(sVct_k)
  \,.
$$

Unwinding what this means, then a [[supercommutative superalgebra]] $A$ is

1. a $\mathbb{Z}/2$-graded associative algebra according to example \ref{GradedAlgebras};

1. such that for any two elements $a, b$ of homogeneous degree, their product satisfies

   $$
     a b \; = \; (-1)^{deg(a) deg(b)}\, b a
     \,.
   $$

The [[formal dual]] $Spec(A)$ of a supercommutative superalgebra $A$, according to def. \ref{Affines}, we call an **affine [[super scheme]]**.

=--

+-- {: .num_remark}
###### Remark

In view of def. \ref{SupercommutativeSuperalgebra} we may define a non-necessarily supercommutative superalgebra to be a [[monoid]] (not necssarily commutative) in [[sVect]], and write

$$
  sAlg_k \coloneqq Mon(sVect)
  \,.
$$

However, since the definition of not-necessarily commutative monoids does not invoke the [[braiding]] of the ambient [[tensor category]], and since [[super vector spaces]] differ from $\mathbb{Z}/2$-[[graded vector spaces]] only via their [[braiding]], this yields equivalently just $\mathbb{Z}/2$-graded algebras (example \ref{GradedAlgebras}):

$$
  sAlg_k \simeq Alg_k^{\mathbb{Z}/2}
  \,.
$$

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

=--

(e.g. [arXiv:1303.1916, 7.5](http://arxiv.org/abs/1303.1916))


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










#### Modules in tensor categories and Super vector bundles
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

In conclusion, any [[vector bundle]] $V \to X$ gives rise to an $C^\infty(X)$-[[module]] $\Gamma_X(V)$.

The _[[smooth Serre-Swan theorem]]_ states sufficient conditions on $X$ such that the converse holds. Together with the [[embedding of smooth manifolds into formal duals of R-algebras]] (prop \ref{EmbeddingOfSmoothManifoldsIntoRAlgebras}), this states that [[differential geometry]] is "more algebraic" than it might superficially seem:

+-- {: .num_prop}
###### Proposition
**([[smooth Serre-Swan theorem]], [Nestruev 03](smooth+Serre-Swan+theorem#Nestruev03))**

For $X$ a [[smooth manifold]], then the construction which sends a smooth [[vector bundle]] $V \to X$ to its $C^\infty(X)$-[[module]] $\Gamma_X(V)$ of [[sections]] is an [[equivalence of categories]]

$$
  VectBund_X^{fin}
    \stackrel{\simeq}{\longrightarrow}
  C^\infty(X) Mod_{proj}^{fin\,gen}
$$

between that of smooth [[vector bundles]] of finite [[rank]] over $X$ and that of [[finitely generated object|finitely generated]] [[projective modules]] over the $\mathbb{R}$-[[associative algebra|algebra]] $C^\infyt(X)$ of [[smooth functions]] on $X$.

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

The topic of general [[algebra]], not necessarily over [[ground fields]], is the above general concepts of monoids and their modules spcialized to the ambient [[symmetric monoidal category]] being the category [[Ab]] of  [[abelian groups]] regarded as a [[symmetric monoidal category]] via the [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ (whose [[tensor unit]] is the additive group of [[integers]] $\mathbb{Z}$):

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

When thinking of commutative monoids in some tensor category as [[formal duals]] to certain [[spaces]], then we are interested in forming [[Cartesian products]] and more generally [[fiber products]] of these spaces. Dually this is given by [[coproducts]] of commutative monoids and commutative $R$-algebras. The following says that these may be computed just as the [[tensor product of modules]]:


+-- {: .num_prop #CoproductsInCMon}
###### Proposition

Let $\mathcal{C}$ be a [[symmetric monoidal category]] such that

1. it has [[reflexive coequalizers]]

1. that are preserved by the [[tensor product]] functors $A \otimes (-) \colon \mathcal{C} \to \mathcal{C}$ for all objects $A$ in $\mathcal{C}$.

Then for $f \colon A \to B$ and $g \colon A \to C$ two morphisms in the category $CMon(\mathcal{})$ of _[[commutative monoids]]_ in $\mathcal{C}$, the underlying object in $\mathcal{C}$ of the [[pushout]] in $CMon(\mathcal{C})$ coincides with the [[tensor product]] in the monoidal category $A$[[Mod]] (according to prop. \ref{MonoidalCategoryOfModules}):

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

   (where we are regarding $A_2$ as a commutative monoid in $A_1$-modules via prop. \ref{AlgebrasOverAAreMonoidsUnderA}) and eqipped by the evident [[action]] induced by the multiplication in $A_2$


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













#### (Super-)Groups as (super-)commutative Hopf algebras
 {#GroupsAsHopfAlgebras}

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
  C^\infty(X) \longleftarrow C^\infty(Y) \;\colon\; f^\ast
$$

and the associatioon $f \mapsto f^\ast$ is a [[natural bijection]].
Of course, for any two composable smooth functions $f,g$ then $(g \circ f )^\ast = f^\ast \circ g^\ast$ and if $f = id$ is the identity smooth function, then $f^\ast = id$ is the identity homomomorphism of smooth algebras.

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
A **[[commutative Hopf algebroid]]** in $\mathcal{A}$ is an [[internal groupoid]] in the [[opposite category]] $CMon(\mathcal{A})^{op}$ of [[commutative monoids]] in $\mathcal{A}$, regarded with its [[cartesian monoidal category]] structure according to prop. \ref{CoproductsInCMon}.

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

The key basic fact to use now is prop. \ref{CoproductsInCMon} the [[tensor product]] of commutative monoids exhibits the [[cartesian monoidal category]] structure on $CMon(\mathcal{A})^{op}$, :
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


By internalizing all of the above from $Vect$ to $sVect$, we obtain the concept of supergrous

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

For $G$ an ordinary (affine algebraic) group, regarded as a supergroup with trivial odd-graded part, then every element $\epsilon \in Z(G)$ in the [[center]] defines an inner parity, def. \ref{InnerParity}.

=--

([Deligne 02, 0.4 i)](#Deligne02))

+-- {: .num_remark}
###### Remark

In view of remak \ref{InnerParityInBosonicSupergroup}, specifying an involutive central element in an ordinary group is a faint shadow of genuine supergroup structure. In fact such pairs are being referred to as "supergroups" in ([M&#252;ger 06](#Mueger06)).

=--

Demanding the existence of inner parity is not actually a restriction of the theory:

+-- {: .num_example}
###### Example

For $H$ any supergroup, def. \ref{Supergroup}, and $\mathbb{Z}_2 = \{id,par\}$ acting on it by parity involution, def. \ref{ParityAutomorphism}  then the [[semidirect product]] $\mathbb{Z}_2 \ltimes G$ has inner parity, def. \ref{InnerParity}, given by $\epsilon \coloneqq par \in \mathbb{Z}_2 \hookrightarrow \mathbb{Z}_2 \ltimes G$.

=--

([Deligne 02, 0.4 ii)](#Deligne02))













#### Linear super-representations as Comodules
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

* a [[comodule]] $V$ (def. \ref{CommutativeHopfAlgebroidComodule}) in [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}) for the [[formal dual|formally dual]] [[commutative Hopf algebra]] \mathcal{O}(G)$.

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

The [[category of representations]] $Rep(G,\epsilon)$ of def. \ref{Superrepresentation} of an affine algebraic [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$ (def. \ref{InnerParity}}) on finite-dimensional super vector spaces (example \ref{FiniteDimensionalSuperVectorSpaces}) and equippd with the tensor product of comodules from def. \ref{TensorProductOfComodulesOverAHopfAlgebra} is a $k$-[[tensor category]] (def. \ref{TensorCategory}) of subexponential growth (def. \ref{SubexponentialGrowth}).

=--

([Deligne 02, 1.21](#Deligne02))

Moreover, any finite dimensional [[faithful representation]] (which always exists, [prop.](faithful+representation#AlgebraicGroupHasFinDimFaithfulRepresentations)) serves as an $\otimes$-generator (def. \ref{FiniteTensorGeneration}).

See ([this prop.](faithful+representation#AnyFinDimRepOfAffineAlgebraicGroupOverFieldIsSubquotientsOfFaithfulRep)).





#### Super Fiber functors and their automorphism supergroups
 {#FiberFunctors}

The first step in exhibiting a given [[tensor category]] $\mathcal{A}$ as being a [[category of representations]] is to exhibit its objects as having an [[forgetful functor|underlying]] representation space of sorts, and then an [[action]] represented on that space. Hence a necessary condition on $\mathcal{A}$ is that there exists a [[forgetful functor]]

$$
   \omega \;\colon\; \mathcal{A} \longrightarrow \mathcal{V}
$$

to some other [[tensor category]], such that $\omega$ satisfies a list of properties, in particular it should be a [[symmetric monoidal functor|symmetric]] [[strong monoidal functor]].

Such functors are called _[[fiber functors]]_. The idea is that we think of $\mathcal{A}$ as a [[bundle]] over $\mathcal{V}$, and over each $V \in \mathcal{V}$ we find the [[fiber]] $\omega^{-1}(V)$ of that "bundle", consisting of all those objects in $\mathcal{A}$ whose underlying object in the given $V$.

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

If here $\mathcal{T} = $ [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}), then this is called a **super fiber functor**.

=--

([Deligne 02, 3.1](#Deligne02))

Given a super fiber functor $\omega \colon \mathcal{A} \to sVect_k$ (def. \ref{FiberFunctor}) there is an evident notion of its [[automorphism group]]: a [[homomorphism]] between [[functors]] is a [[natural transformation]], and that between [[monoidal functors]] is a [[monoidal natural transformation]], according to def. \ref{LaxMonoidalFunctor}, and this is an [[automorphism]] of functors if it is a [[natural automorphism]]. We write

$$
  Aut(\omega) \in Grp
$$

for this automorphism group.

So far this is a group without geometric structure (a [[discrete group]]). But it is naturally equipped with [[supergeometry]] (super-[[algebraic geometry]]) exhibited by a rule for what the "geometrically parameterized families" of its elements are. (For exposition of this perspective see at _[[motivation for sheaves, cohomology and higher stacks]]_).

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

which, with the [[Yoneda embedding understood]], we write simply as

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

+-- {: .prop #AutOfFibFuncIsImagUnderFibFuncOfFundamentalGroup}
###### Proposition

For $\mathcal{A}$ a $k$-[[tensor category]] equipped with a [[super fiber functor]] $\omega \colon \mathcal{A} \to sVect$ (def. \ref{FiberFunctor}), then the automorphism supergroup of $\omega$ is the image under the super fiber functor $\omega$ of the fundamental group of $\mathcal{A}$, according to def. \ref{FundamentalSupergroup}:

$$
  \underline{Aut}(\omega)
    \simeq
  \omega(\pi(\mathcal{A}))
  \,.
$$

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
  \eta(\pi(\mathcal{A_1}))
$$

from the fundamental group of $\mathcal{A}_1$ (def. \ref{FundamentalSupergroup}) to the image under $\eta$ of the fundamental group of $\mathcal{A}_2$.

=--

([Deligne 90, 8. 15. 2](#Deligne90))








#### Super-exterior powers and Schur functors

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











#### {#TannakaDualityForTensorCategoriesAndSupergroups} Tannaka duality between tensor categories and supergroups

Above we saw that

1. every [[tensor category]] equipped with a [[fiber functor|super fiber functor]] gives rise to an affine supergroup (prop. \ref{AutomorphismSupergroupOfFiberFunctorIsRepresentable});

1. the [[category of representations]] of an affine [[supergroup]] is a tensor category, prop. \ref{RegularTensorCategoriesOfSuperrepresentations}.

Indeed, the relation between tensor categories and supergroups is intimate. The following states that under mild size constraints, _every_ tensor category is the category of representations of _some_ affine algebraic supergroup. This shows that the concept of [[supergroups]] is
fundamental and not accidental.

+-- {: .num_theorem #TheTheorem}
###### Theorem

Every $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) such that

1. $k$ is an [[algebraically closed field]] of [[characteristic zero]] (e.g. the field of [[complex numbers]])

1. $\mathcal{A}$ is of subexponential growth according to def. \ref{SubexponentialGrowth}

then there exists

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

This is due to ([Deligne 02, theorem 0.6](#Deligne02))

We outline key steps of the proof of theorem \ref{TheTheorem}, given in [Deligne 02](#Deligne02).
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

If for every object of a $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) there exists a [[Schur functor]] (def. \ref{SchurFunctor}) that annihilates it, then there exists a [[fiber functor|super fiber functor]] (def. \ref{FiberFunctor}) over $k$:

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











### Supergeometry
 {#Supergeometry}


### Fundamental super $p$-branes

this section is at _[[geometry of physics -- fundamental super p-branes]]_


#### Motivation and survey


The _[[Green-Schwarz action functional]]_ is an [[action functional]] for a [[sigma-model]] that describes the propagation of a fundamental $p$-[[brane]] $\Sigma$ on a [[supermanifold]] [[spacetime]].

* For $p = 0$ this is the **Green-Schwarz [[superparticle]]**.

* For $p = 1$ the **Green-Schwarz [[superstring]]** (at the center of attention in [[string theory]]). This model is in contrast to the _[[NSR-string]]_ model, which instead has manifest [[worldsheet]] [[supersymmetry]]. See at _[[superstring]]_ for more on this.


[[perturbation theory|Perturbative]] [[string theory]] on geometric backgrounds is defined by the [[Neveu-Schwarz-Ramond model]], namely by [[sigma-model]] [[2d super conformal field theories]] (of [[central charge]] 15) on [[worldsheets]] $\Sigma$ that are [[super Riemann surfaces]], with [[target spaces]] $X$ that are ordinary (i.e. "bosonic") [[spacetime]] [[manifolds]].

These worldsheet field theories are induced from _[[action functionals]]_, namely variants of the standard [[energy functional]] ([[Polyakov action]]) on the space $[\Sigma,X]$ of smooth functions

$$
  \phi \;\colon\; \Sigma \longrightarrow X
  \,.
$$

The central theorem of perturbative superstring theory says that the spectrum of such a 2d SCFT are the quanta of the [[perturbation theory|perturbations]] of a higher dimensional [[effective field theory|effective]] [[supergravity]] [[field theory]] on target spacetime, hence transforms under [[supersymmetry]] on target spacetime.

This is the fundamental prediction of the assumption of fundamental strings: assuming 1) that the particles that run in [[Feynman diagrams]] are fundamentally strings, and demanding 2) that there are fermionic particles among these, first implies that the strings must be [[spinning strings]] (have fermions on their worldsheet), which implies that they are [[superstrings]] (worldsheet [[supersymmetry]] mixes the worldsheet bosons and fermions), which then in addition implies that their target space [[effective field theory]] is [[supergravity]], hence that also the effective target space fields exhibit local supersymmetry.

$$
  \underset{spinning\; string}{\underbrace{fermions \;+\; strings}}
  \;=\;
  superstring \;\Rightarrow\; supergravity
  \,.
$$

The first step in this implications (spinning string is superstring) is straightforward, but the second step appears as a miracle from the point of view of the NSR string. It comes out this way by non-trivial computation, but is not manifest in the theory.

In order to improve on this situation, Green and Schwarz searched and found ([Green-Schwarz 81](#GreenSchwarz81), [Green-Schwarz 82](#GreenSchwarz82) [Green-Schwarz 84](#GreenSchwarz84), for the history see [Schwarz 16, slides 24-25](#Schwarz16)) a suitably equivalent string [[action functional]]  that would manifestly exhibit spacetime supersymmetry. This is now called the _[[Green-Schwarz action functional]]_.

| [[action functional]] for [[superstring]] | manifest [[supersymmetry]] |
|----|---|
| [[Ramond-Neveu-Schwarz string]] | on [[worldsheet]]  |
| Green-Schwarz string | on [[target space|target]] [[spacetime]] |

The basic idea is to pass to the evident [[supergeometry|supergeometric]] analogue of the bosonic string action:

Let $\Sigma$ be a [[closed manifold]] of [[dimension]] 2 -- representing the abstract _[[worldsheet]]_ of a string. Let $(X,g)$ be a [[pseudo-Riemannian manifold]] -- representing a purely [[gravity|gravitational]] [[spacetime]] background. Then the [[action functional]] governing the [[bosonic string]] propagating in this spacetime is the functional

$$
  \exp(\tfrac{i}{\hbar} S_{bos})
  \;\colon\;
  [\Sigma,X]
   \longrightarrow
  \mathbb{R}/_{\hbar}\mathbb{Z}
$$

on the [[smooth space|smooth]] [[mapping space]] $[\Sigma,X]$ of [[smooth functions]] $\Sigma \to X$, that simply assigns the proper relativistic [[volume]] of the image of the [[worldsheet]] $\Sigma$ in [[spacetime]]:

$$
  (\Sigma\overset{\phi}{\longrightarrow} X)
    \;\mapsto\;
  \int_\Sigma vol_{\phi^\ast g}
  \,.
$$

(This is the _[[Nambu-Goto action]]_. It is classically equivalently to the [[Polyakov action]] which is the genuine starting point for the quantum [[Neveu-Schwarz-Ramond string]]. Howver, since, as we discuss below, the Green-Schwarz action naturally generalizes to that of other $p$-[[branes]] it is more natural to consider the Nambu-Goto form of the action here.)

When here $(X,g)$ is generalized to a [[superspacetime]] [[supermanifold]] with [[orthogonal structure]] encoded by a [[super-vielbein]] $e$ (see at _[[super Cartan geometry]]_ for details), then the same form of the action functional still makes sense and produces a functional on the [[supergeometry|supergeometric]] [[mapping space]] $[\Sigma,X]$. Moreover, by construction this action functional is invariant under the [[superisometry group]] of $(X,g)$, hence under spacetime [[supersymmetry]].


$$
\array{
  \text{symmetry of worldsheet theory}
  \\
  \array{
    && \Sigma
    \\
    & {}^{\mathllap{\phi}}\swarrow && \searrow^{\mathrlap{\phi'}}
    \\
    X &&\underset{\simeq}{\longrightarrow}&& X
  }
  \\
  \text{super-isometry of target spacetime}
}
$$

However, Green and Schwarz noticed that this [[kinetic action]] functional $\phi \mapsto \int_\Sigma vol_{\phi^\ast e}$ does _not_ quite yield dynamics that is equivalent to that of the NSR string: when the [[equations of motion]] hold ("on shell") it has more fermionic degrees of freedom than present in the NSR string. The key insight of Green and Schwarz was that one may add an extra summand to the action functional to the plain super-Nambu-Goto action, such that the resulting functional enjoys a further 1-parameter symmetry, called _[[kappa-symmetry]]_,  and such that restricting to the $\kappa$-symmetric states, then the action functionals do become classically equivalent.

Moreover, they showed that in [[light-cone gauge]] the resulting quantum dynamics is equivalent to that of the [[NSR string]], thus providing a conceptual proof for the observed local spacetime supersymmetry for backgrounds that admit two lightlike Killing vectors. (The quantization of the GS-string away from lightcone gauge however remains an open problem.)


Green-Schwarz's extra [[kappa-symmetry]] term serves a clear purpose, but originally its geometrically meaning was mysterious. However, in ([Henneaux-Mezincescu 85](#HenneauxMezincescu85)) it was observed (expanded on in ([Rabin 87](#Rabin87), [Azcarraga-Townsend 89](#AzcarragaTownsend89), [Azcarraga-Izquierdo 95,chapter 8](#AzcarragaIzquierdo95))), that the Green-Schwarz-action functional describing the string in $d+1$-dimensions has a neat geometrical interpretation: it is simply the ([[parameterized WZW model|parameterized]]) [[WZW-model]] for

1. target space being locally [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1|\mathbf{N}}$ regarded as the [[coset]] [[supergroup]]

   $$
     \mathbb{R}^{d-1,1\vert \mathbf{N}}
       \;\simeq\;
     Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}}) / Spin(d-1,1)
   $$

   for $\mathbf{N}$ a real [[spin representation]] (the "number of supersymmetries"), $Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}})$ the corresponding [[super Poincaré group]] and $Spin(d-1,1)$ its [[Lorentzian manifold|Lorentz-signature]] [[spin group|Spin]] [[subgroup]];

1. [[WZW-term]] being a local potential for the the unique (up to rescaling, if it exists) $Spin(d-1,1)$-invariant [[group cocycle|group 3-cocycle]] $\mu_3$ on $Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}})$, with component locally given by the Gamma-matrices of the given [[Clifford algebra]] representation.

More in detail, just as ordinary [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ may be identified with the [[translation group]] with canonical basis of [[left invariant 1-forms]] given by the canonical [[vielbein]] field

$$
  \{e^a \coloneqq \mathbf{d}x^a\}_{a = 0}^{d-1}
  \,,
$$

where $\{x^a\}$ are the canonical [[coordinates]] on $\mathbb{R}^{d-1,1}$, so [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ for some real [[spin representation]] $\mathbf{N}$ is characterized as the [[supergroup]] whose [[left invariant 1-forms]] consitute the $\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$-bigraded differential with generators the [[super-vielbein]]

$$
  \underset{deg = (1,even)}{\underbrace{e^a}}
    \;\coloneqq\;
  \mathbf{d}x^a + \tfrac{i}{2}\overline{\theta}\Gamma^a \mathbf{d} \theta
  \;\;\;\,,\;\;\;\;\;\;\;\;\;\;
  \underset{deg = (1,odd)}{\underbrace{\psi^\alpha}} \;\coloneqq\; \mathbf{d}\theta^\alpha
  \,,
$$

where $(x^a, \theta^\alpha)$ are the canonical coordinates on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, with the odd-graded elements $\{\theta^\alpha\}$ spanning the given real [[spin representation|Spin(d-1,1)-representation]] $\mathbf{N}$ with [[Clifford algebra]] generators $\{\Gamma^a\}$.

Now while ordinary [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ is an [[abelian group]], reflected by the fact that its [[left-invariant 1-forms]] are all closed

$$
  \mathbf{d}e^a = 0 \;\;\;\;\;\; on \; \mathbb{R}^{d-1,1}
  \,,
$$

the key phenomenon of [[supersymmetry]] (that two [[fermions]] pair to a [[bosons]]) means that $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ is slightly non-abelian, reflected by the fact that the [[super-vielbein]] is not closed

$$
  \mathbf{d} e^a = \tfrac{i}{2} \overline{\psi} \Gamma^a \psi
  \;\,,\;\;\;\;\;\;
  \mathbf{d} \psi^\alpha = 0
  \,.
$$

This is the source of all the rich structure seen in Green-Schwarz theory.

In particular, for special combinations of spacetime dimension $d$ and number of supersymmetries $\mathbf{N}$ the 3-form


$$
  \mu_3 \;\coloneqq\;  \overline{\psi} \wedge \Gamma_a \psi \wedge e^a
$$

is a non-trivial [[super Lie algebra|super]] [[Lie algebra cocycle]] on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, in that $\mathbf{d}\mu_3 = 0$ and so that there is no [[left invariant differential form]] $b$ with $\mathbf{d}b = \mu_3$.

This happens notably for $d = 10$ and $\mathbf{N} = (1,0)$ ([[heterotic string]]) or $\mathbf{N} = (2,0)$ ([[type IIB superstring]]) and $\mathbf{N} = (1,1)$ ([[type IIA superstring]]). (It also happens in some lower dimensions, where however the corresponding NSR-string develops a [[conformal anomaly]] after quantization ("non-critical strings"). This classification of cocycles is part of what has come to be known as the _[[brane scan]]_ in superstring theory, see below.)

In this equivalent formulation, the Green-Schwarz action functional for the superstring has the following simple form:

Let $(X,e)$ be a [[superspacetime]], hence a [[supermanifold]] $X$ equipped with a [[super-vielbein]] $e$ (super-[[orthogonal structure]]) which is locally modeled on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ (technically: a [[torsion of a G-structure|torsion]]-free [[super-Cartan geometry]] modeled on $Spin(d-1,1) \hookrightarrow Iso(\mathbb{R}^{d-1,1\vert \mathbf{N}})$). Write $\mu_3^X \in \Omega^3(X)$ be the [[super differential form]] on $X$ which is the induced [[definite globalization of WZW term|definite globalization]] of the cocycle $\mu_3$ over $X$. For $U \subset X$ any contractible subspace, then the restriction of $\mu^X_3|_{U} \in \Omega^3(U)$ of $\mu_3^X$ to $U$ is exact, and hence admits a potential $B_U \in \Omega^2(U)$, i.e. such that $d B = \mu^X_3|_U$.

Then for $\Sigma$ a 2-dimensional [[closed manifold]], the Green-Schwarz action functional

$$
  \exp(\tfrac{i}{\hbar} S_{GS})
  \;\colon\;
  [\Sigma,X]_U
    \longrightarrow
  \mathbb{R}/_{\hbar} \mathbb{Z}
$$

is the function on the super-[[smooth space]] $[\Sigma,X]_U$ of smooth maps of supermanifolds $\phi \colon \Sigma \to X$ which factor through $U$, given by

$$
  \phi
    \;\mapsto\;
  \int_\Sigma vol_{\phi^\ast e}
   \;+\;
  \int_\Sigma \phi^\ast B_U
  \;\;\;\,,\;\;\;\;\;\;\;\;\;
  \mathbf{d} B_U = \mu^X_3|_U
  \,.
$$

In order to get rid of the restriction to some $U \subset X$ one needs to add global data. The need for this is at least mentioned briefly in ([Witten 86, p. 261 (17 of 20)](#Witten86)), but had otherwise been ignored in the physics literature. The general solution is to promote the local potentials $B$ to the connection $\hat B$ on a [[Super Gerbes|super gerbe]] ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)). This is a choice of [[higher prequantization]]

$$
  \array{
    && \mathbf{B}^{2}(\mathbb{R}/_\hbar \mathbb{Z}) & \text{prequantization}
    \\
    & {}^{\mathllap{\hat B}}\nearrow & \downarrow^{\mathrlap{curv}}
    \\
    X
     &\underset{\mu^X_3}{\longrightarrow}&
    \mathbf{\Omega}^3
    &
    \text{3-form curvature}
  }
  \,.
$$


Writing $\int_\Sigma \phi^\ast \hat B$ for the [[volume holonomy]] of a [[circle 2-bundle with connection]] $\hat B$, then the globally defined Green-Schwarz sigma model

$$
  \exp(\tfrac{i}{\hbar} S_{GS})
  \;\colon\;
  [\Sigma, X]
    \longrightarrow
  \mathbb{R}/_\hbar\mathbb{Z}
$$

is given by

$$
  \phi \;\mapsto\; \int_\Sigma vol_{\phi^\ast} + \int_\Sigma \phi^\ast \hat B
  \;\;\,,
  \;\;\;\;\;\;\;
  curv(\hat B) = \mu_3^X
  \,.
$$

This form of the Green-Schwarz action functional for the string has evident generalization to other $p$-[[branes]]. Whenever there is a Lorentz-invariant $(p+2)$-cocycle $\mu_{p+2}$ on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$, then one may ask for a higher gerbe ([[higher prequantum line bundle]]) $\hat C$ with [[curvature]] $\mu^X_{p+2}$ and consider the analogous functional.

The triples $(d,\mathbf{N},p)$ (spacetime dimension, number of supersymmetries, dimension of brane) such that

$$
  \mu_{p+2}
    \;\coloneqq\;
  \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
$$

is a nontrivial cocycle, hence for which there is such a Green-Schwarz action functional for $p$-branes on $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ may be classified and form what is called the _[[brane scan]]_ ([Ach&#250;carro-Evans-TownsendWiltshire 87](#AETW87), [Brandt 12-13](#Brandt12-13)):

{#DuffBraneScan} <div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/DuffBraneScan.jpg" height="600">
</div>

The graphics on the left is from ([Duff 87](#Duff87)). The diagonal lines indicate [[double dimensional reduction]], taking a $(p+1)$-brane in $(d+1)$ dimensions to a $p$-brane in $d$-dimensions.

For instance for $(d = 11, \; \mathbf{N} = \mathbf{32}, \; p = 2)$ one finds a cocycle, and the corresponding GS-action functional is that of the fundamental [[M2-brane]].

This was a striking confluence of brane physics and classification of [[super Lie algebra|super]] [[Lie algebra cohomology]]. But just as striking as the matching, was what it lacked to match: the [[D-branes]] and the [[M5-brane]] ($d = 11$, $p = 5$) are lacking from the old brane scan. Incidentally, these lacking branes are precisely those branes on which the branes that do appear on the brane scan may end, equivalently those branes that have [[higher gauge fields]] on their [[worldvolume]] (tensor multiplets).

An action functional for the [[M5-brane]] vaguely analogous to a Green-Schwarz action functional was found in ([BLNPST 97](#BLNPST97), [APPS 97](#APPS97)). It is again the sum of a kinetic term and a WZW-like term, but the WZW-like term does not come from a cocycle on a (super-)group.

In order to deal with this, it was suggested in ([CAIB 99](#CAIB99), [Sakaguchi 00](#Sakaguchi00), [Azcarraga-Izquierdo 01](#AzcarragaIzquierdo01)) that there is an algebraic structure called "[[extended super-Minkowski spacetimes]]" that generalizes [[super Minkowski spacetime]] and serves to unify the Green-Schwarz-like models for the D-branes and the M5-brane with the original Green-Schwarz models for the string and the M2-brane.

These [[extended super-Minkowski spacetimes]] carry algebraic analogs of super Lie algebra cocycles, such that the relevant terms for the [[D-branes]] and the [[M5-brane]] do appear after all, hence such that all the branes in [[string theory]]/[[M-theory]] are unified. In fact these "[[extended super-Minkowski spacetimes]]" are precisely the "FDA"s that have been introduced before in the [[D'Auria-Fré formulation of supergravity]] and what became identified as the 7-cocycle for the [[M5-brane]] this way had earlier been recognized algebraically as an stepping stone for an elegant re-derivation of [[11-dimensional supergravity]] ([D'Auria-Fr&#233; 82](#DAuriaFre82)).

The ([[higher differential geometry|higher]]) geometric meaning of these constructions was found in ([Fiorenza-Sati-Schreiber 13](#FiorezaSatiSchreiber13)): these algebraic structures of "[[extended super-Minkowski spacetimes]]"/FDAs are precisely the [[Chevalley-Eilenberg algebras]] of [[super Lie n-algebra]]-extensions of [[super-Minkowski spacetime]] which are classified by the cocycles that serve as the GS-WZW terms of the $p_1$-branes that may end on those $p_2$-branes whose cocycles are carried by the extended super-Minkowski spacetime.

Hence the missing $p$-branes in the old [[brane scan]] (classifying just cocycles on [[super Lie algebras]]) do appear as one generalizes (super) Lie algebras to (super) [[strong homotopy Lie algebras]] = [[L-infinity algebras]]. Moreover, each brane intersection law (one brane species may end on another) is now matched to a super $L_\infty$-algebra [[extension]] and so the old brane scan is generalized to a tree of branes _[[schreiber:The brane bouquet]]_:

<img src="https://dl.dropboxusercontent.com/u/12630719/BraneBouquet.JPG" alt="the brane bouquet" width="900" />

Each item in this bouquet denotes a [[super L-infinity algebra]] and each arrow denotes an [[L-infinity extension]] classified by a cocycle which encodes the GS-WZW term of the brane named by the domain of the arrow. Moreover, arrows pass exactly from one brane species to the brane species that may end on the former.

In ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)) it is shown that all these [[super L-infinity algebras]] [[Lie integration|Lie integrate]] to [[smooth super-n-groups]], and all the cocycles [[Lie integration|Lie integrate]] to [[Super Gerbes|super-gerbes]] on these, such that the induced [[volume holonomy]] is the relevant generalized GS-WZW term. For detailed exposition see at _[[schreiber:Structure Theory for Higher WZW Terms]]_.

With this generalized perspective, now the Green-Schwarz-type action functionals describe _all_ the [[p-branes]] in [[string theory]]/[[M-theory]].

Again, in order to make this generally true one needs to apply a [[higher prequantization]] -- a choice of [[line n-bundle with connection|line (p+1)-bundle with connection]] -- in order to globalize the [[WZW-terms]] ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13))

$$
  \array{
    && \mathbf{B}^{p+1}(\mathbb{R}/_\hbar \mathbb{Z}) & \text{prequantization}
    \\
    & {}^{\mathllap{\hat A_{p+1}}}\nearrow & \downarrow^{\mathrlap{curv}}
    \\
    X
     &\underset{\mu^X_{p+2}}{\longrightarrow}&
    \mathbf{\Omega}^{p+2}
    &
    (p+2)\text{-form curvature}
  }
  \,.
$$

Hence $\hat A_{p+1}$ is the actual [[background field]] that the $p$-brane couples to. There is considerably more information in $\hat A_p$ than in its curvature $curv(\hat A_{p+1}) = \mu_{p+2}$. For instance for the [[M2-brane]] one may find the local super [[moduli space]] for local choices of $\hat A_{p+1}$ for the given $\mu_{4}$ on [[KK-compactifications]] to $d = 4$. It turns out that the bosonic [[body]] of this moduli space is the [[exceptional tangent bundle]] on which the [[U-duality]] group [[E7]] has a canonical action (see at _[[schreiber:From higher to exceptional geometry]]_).

This highlights that Green-Schwarz functionals capture fundamental ("microscopic") aspects of $p$-branes. In contrast, often $p$-branes are discussed in their [[soliton|solitonic]] incarnation as _[[black branes]]_. These solitonic branes sit at asymptotic boundaries of [[anti-de Sitter spacetime]] and carry [[conformal field theories]], related to the ambient [[supergravity]] by [[AdS-CFT duality]].

This phenomenon is indeed a consequence of the fundamental Green-Schwarz branes:

Consider a 1/2-[[BPS state]] solution of [[type II supergravity]] or [[11-dimensional supergravity]], respectively. These solutions locally happen to have the same classification as the Green-Schwarz branes. Hence we may consider a configuration $\phi \colon \Sigma \to X$ of the corresponding fundamental $p$-brane which embeds $\Sigma$ into the asymptotic AdS boundary of the given 1/2 BPS spacetime $X$. Then it turns out that restricting the Green-Schwarz action functional to small fluctuations around this configuration, and applying a [[diffeomorphism]] [[gauge fixing]], then the resulting action functional is that of a [[supersymmetry|supersymmetric]] [[conformal field theory]] on $\Sigma$ as in the [[AdS-CFT]] dictionary:

| fundamental $p$-brane | -fluctuations about asymptotic AdS configuration$\to$ |  solitonic $p$-brane |
|----|-----|---|
| Green-Schwarz action functional |  | [[supersymmetric|super]]-[[conformal field theory]] |

([Claus-Kallosh-Proeyen 97](#ClausKalloshProeyen97), [Claus-Kallosh-Kumar-Townsend 98](#ClausKalloshKumarTownsend98), [AFFFTT 98](#AFFFTT98) [Pasti-Sorokin-Tonin 99](#PastiSorokinTonin99))

In fact the [[BPS-state]] condition itself is neatly encoded in the Green-Schwarz action functionals: by construction they are invariant under the [[spacetime]] [[superisometry group]]. Hence the [[Noether theorem]] implies that there are corresponding [[conserved currents]], whose [[Dickey bracket]] forms a super-[[Lie algebra extension]] of the Lie algebra of supersymmetries.

$$
  \array{
    \left\{
    \array{
      X && \overset{=}{\longrightarrow} && X
      \\
      & {}_{\mathllap{\hat C}}\searrow
        &\swArrow&
      \swarrow_{\mathrlap{\hat C}}
      \\
      && \mathbf{B}^{p+1}(\mathbb{R}/_{\hbar} \mathbb{Z})
    }
    \right\}
      &\longrightarrow&
    \left\{
    \array{
      X && \overset{\simeq}{\longrightarrow} && X
      \\
      & {}_{\mathllap{\hat C}}\searrow
        &\swArrow&
      \swarrow_{\mathrlap{\hat C}}
      \\
      && \mathbf{B}^{p+1}(\mathbb{R}/_{\hbar} \mathbb{Z})
    }
    \right\}
     &\longrightarrow&
    \left\{
      \array{
        X && \overset{\simeq}{\longrightarrow} && X
      }
    \right\}
    \\
    \text{topological currents}
    &&
    \text{Noether currents}
    &&
    \text{symmetries}
  }
$$

Here the "$\swArrow$" filling the triangles is the non-trivial gauge transformation by which the [[WZW term]] (as any WZW term) is preserved under the symmetries (instead of being fixed identically). It is the information in this transformations which makes the currents form an extension of the symmetries.

Here this yields the famous brane charge extensions of the super-isometry super Lie algebra of the schematic form

$$
  \{Q_\alpha, Q_\beta\}
  \;=\;
  (C \Gamma^a_{\alpha \beta}) P_a
  \;+\;
  (C \Gamma^{a_1 \cdots a_p})_{\alpha \beta} Z_{a_1, \cdots, a_p}
$$

(for $Q$ a [[Killing spinor]] and $P$ its corresponding [[Killing vector]]) known as the [[type II supersymmetry algebra]] and the [[M-theory supersymmetry algebra]], respectively ([Azc&#225;rraga-Gauntlett-Izquierdo-Townsend 89](#AGIT89)). In fact it yields super-[[L-infinity algebra extensions|Lie n-algebra extensions]] of which the familiar super Lie algebra extensions are the 0-truncation ([Sati-Schreiber 15](#SatiSchreiber15), [[schreiber:Local prequantum field theory|Khavkine-Schreiber 16]]).

In summary, the nature and classification of Green-Schwarz action functionals captures in a mathematically precise way a good deal of the core structure of [[string theory|string]]/[[M-theory]].

In fact, the [[super L-infinity algebra|super L-infinity algebraic]] perspective on the Green-Schwarz functionals via [[schreiber:The brane bouquet]] also solves the following open problem on [[M-branes]]:

it is famously known from [[Freed-Witten anomaly]]-cancellation that the [[D-brane charges]] are not in fact just in [[de Rham cohomology]] in every second degree, but are in [[twisted K-theory]], hence [[rational homotopy theory|rationally]] in [[twisted de Rham cohomology]], with the twist being the [[F1-brane]] charge (from the fundamental). It is an open problem to determine what becomes of these [[twisted K-theory]] charge groups as one lifts F1/D$p$-branes in string theory to M2/M5-branes in [[M-theory]].


|   | intersecting branes | charges in [[generalized cohomology theory]]
|-----|--------------|----------------------|
| [[string theory]] | [[F1-brane|F1]]/[[D-brane|Dp-branes]] | [[twisted K-theory]] |
| [[M-theory]]  | [[M2-brane|M2]]/[[M5-branes]] | ??? |

Notice that there are "microscopic degrees of freedom" of the theory encoded by the choice of [[generalized cohomology theory]] here, generalizing the extra degrees of freedom in the choice of a WZW-term already mentioned above. In general for $E$ a cohomology theory and $E \longrightarrow E \otimes \mathbb{Q}$ its [[Chern character]] map (for instance from [[topological K-theory]] to [[ordinary cohomology]] in every second degree), then a choice of genuine charges is the extra information encoded in a lift

$$
  \array{
    && E
    \\
    & {}^{\mathllap{\text{true charge}}}\nearrow & \downarrow^{\mathrlap{ch}}
    \\
    X &\underset{\text{rational} \atop  \text{charge}}{\longrightarrow}& E \otimes \mathbb{Q}
  }
$$

But [[rational homotopy theory|rationally]] [[schreiber:The brane bouquet]] allows to derive this from first principles:

Above we saw that the naive cocycles of the [[D-branes]] and of the [[M5-brane]] are not defined on the actual [[spacetime]],  but on some "extended" spacetime, which is really a [[smooth super infinity-groupoid]] extension of spacetime. Hence we should ask if these cocycles [[descent|descend]] to the actual super-spacetime while picking up some twists.

One may prove that:

* the F1/D$p$-brane GS-WZW cocycles descend to 10d type II superspacetime to form a single cocycle in rational twisted K-theory, just as the traditional lore reqires ([Fiorenza-Sati-Schreiber 16](#FiorenzaSatiSchreiber16));

* the M2/M5 GS-WZW cocycles descent to 11d superspacetime to form a single cocycle with values in the [[rational n-sphere|rational 4-sphere]] ([Fiorenza-Sati-Schreiber 16](#FiorenzaSatiSchreiber16)).

This has implications on some open conjectures regarding [[M-theory]], for more on this see _[[schreiber:Equivariant cohomology of M2/M5-branes]]_.









#### Super Lie $n$-algebras

(...)

 [[super L-infinity algebra]]

 (...)

The [[Chevalley-Eilenberg algebras]] which in def. \ref{CEAlgebra} and def. \ref{SuperLieAlgebraViaCE} we used to _characterize_ the corresponding (super) Lie algebras are of course traditionally introduced as the [[cochain complexes]] whose [[cochain cohomology]] is [[Lie algebra cohomology]]. We may conceptualize this as follows:

+-- {: .num_defn #SiteCartSp}
###### Definition

For $n \in \mathbb{N}$ write $\mathbb{R}^{1|0}[n]$ for the _[[line Lie n-algebra|line Lie (n+1)-algebra]]_, the [[super L-infinity algebra]] defined simply as the [[formal dual]] to the $(\mathbb{Z},\mathbb{Z}_2)$-graded commutative [[dg-algebra]]

$$
  CE(\mathbb{R}^{1|0}[n]) \coloneqq
  \left(
    \wedge^\bullet \mathbb{R}^{1|0}[n],
    \;
    d = 0
  \right)
$$

whose underlying [[graded algebra]] is freely generated from a single generator in degree $(n,even)$, and whose differential vanishes.

=--

+-- {: .num_remark #LieAlgebraCohomologAsHomomorphism}
###### Remark

Recall that being a "[[formal dual]]" to a dg-algebra here simply means that for $\mathfrak{g}$ any [[super Lie algebra]], the homomorphisms of [[super L-infinity algebras]] of the form

$$
  \mu \;\colon\; \mathfrak{g} \longrightarrow \mathbb{R}^{1|0}[n]
$$

are equivalently (by definition!) homomorphisms of [[dg-algebras]] of the form

$$
  CE(\mathfrak{g})
  \longleftarrow
  CE(\mathbb{R}^{1|0}[n])
  \,.
$$

Since the underlying graded algebra of $CE(\mathbb{R}^{1|0}[n])$ is free on a single generator $c$ in degree $n+1$, such a homomorphism is determined by the image of this generator

$$
  c \mapsto \mu \in CE(\mathfrak{g})
  \,.
$$

Moreover, the condition that this map respects the differentials, and since the differential on $CE(\mathbb{R}^{1|0}[n])$ vanishes by definition, this means that

$$
  \array{
     c &\mapsto& && \mu
     \\
     \downarrow^{\mathrlap{d_{\mathbb{R}^{1|0}[n]}}}
     && &&
    \downarrow^{\mathrlap{d_{\mathfrak{g}}}}
     \\
     0 &\mapsto& 0 &=& d_{\mathfrak{g}}\mu
  }
  \,.
$$

Hence such a moprhism $\mu$ is equivalently a _closed_ element of degree $(n+1)$ in $CE(\mathfrak{g})$, hence is equivalently a [[Lie algebra cohomology|super Lie algebra cocycle]] of degree $n+1$ on $\mathfrak{g}$.

This way [[line Lie n-algebra|line Lie (n+1)-algebra]] $\mathbb{R}^{1|0}[n]$ is the _[[moduli stack|moduli object]]_ for degree-$(n+1)$ Lie algebra cohomology in direct [[analogy]] of how for instance the familiar [[Eilenberg-MacLane space]] $B^{n+1}\mathbb{R} = K(\mathbb{Z},n+1)$ is the classifying space for degree $n+1$ [[ordinary cohomology]] of [[topological spaces]].

=--

One advantange of conceptualizing Lie algebra cocycles as in remark \ref{LieAlgebraCohomologAsHomomorphism} is that it neatly connects to the formulation of [[Lie algebra valued forms]] according to def. \ref{LieAlgValuedFormsViaDgAlgHoms}, def. \ref{SuperLieAlgValuedDiffForms}:


+-- {: .num_remark }
###### Remark

A $\mathbb{R}^{1|0}[n]$-valued differential form is simply an even closed differential $(n+1)$-form:

$$
  \Omega^1(\mathbb{R}^{p|q}, \mathbb{R}^{1|0}[n])
  \simeq
  Hom(CE(\mathbb{R}^{1|0}[n]), \Omega^\bullet(\mathbb{R}^{p|q}))
  \simeq
  \Omega^{n+1}(\mathbb{R}^{p|q})_{even,closed}
  \,.
$$

Hence a super Lie algebra $(n+1)$-cocycle $\mu$ on
$\mathfrak{g}$ naturally determines a map


$$
  \mu(-)
  \colon
  \Omega^1(\mathbb{R}^{p|q},\mathfrak{g})
  \longrightarrow
  \Omega^{n+1}(\mathbb{R}^{p|q})_{even,closed}
$$

given by forming the composite with the morphism representing the cocycle $\mu$

$$
  \left(
    \Omega^\bullet(\mathbb{R}^{p|q})
     \stackrel{A}{\longleftarrow}
  CE(\mathfrak{g})
  \right)
  \mapsto
  \left(
  \Omega^\bullet(\mathbb{R}^{p|q})
   \stackrel{A}{\longleftarrow}
  CE(\mathfrak{g})
  \stackrel{\mu^\ast}{\longleftarrow}
  CE(\mathbb{R}^{1|0}[n])
  \right)
$$

sending a [[Lie algebra valued form]] $A$ to a closed differential form $\mu(A)$.


=--











#### The old brane scan
 {#TheOldBraneScan}

+-- {: .num_defn #LineLienAlgebra}
###### Definition

For $p \in \mathbb{N}$ write $b^{p+1}\mathbb{R}$ for the [[line Lie n-algebra|Line Lie (p+2)-algebra]], given by the [[Chevalley-Eilenberg algebra]] of the form

$$
  CE(b^{p+1}\mathbb{R})
  \coloneqq
  (\langle g_{p+2} \rangle,  d g_{p+2} = 0)
  \,.
$$

=--


+-- {: .num_defn #ThePsiPsiTermsInCEOfSuperMinkowski}
###### Definition

For $\mathbb{R}^{d-1,1\vert \mathbf{N}}$ a [[super Minkowski spacetime]], def. \ref{SuperPoincareAndSuperMinkowski}, regarded as a [[super Lie algebra]], write

$$
  \mu_{p+2}\in CE(\mathbb{R}^{d-1,1\vert \mathbf{N}})
$$

for the element of its [[Chevalley-Eilenberg algebra]] of the form

$$
  \mu_{p+2}
  \coloneqq
  \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The study of the CE-elements in def. \ref{ThePsiPsiTermsInCEOfSuperMinkowski} goes back to ([D'Auria-Fr&#233; 82](#DAuriaFre82)). These authors write $\frac{i}{2}\overline{(-)}\Gamma (-)$ for the bilinear pairing which we write just $\overline{(-)}\Gamma (-)$.

=--

One finds that the elements $\mu_{p+2}$ in def. \ref{ThePsiPsiTermsInCEOfSuperMinkowski} are CE-closed, hence are super Lie algebra cocycles for given $(d,p,N)$, precisely if there is a [[super p-brane]] in $N$-supersymmetric super-Minkowski spacetime on which no other super $p$-brane may end. For "$N=1$" there are (non-trivial) cocycles in dimension $d$ and degree $(p+2)$ as shown in this table:

| $\stackrel{d}{=}$ |  $p =$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 |  8 |  9 |
|--|--------|---|---|---|---|---|---|---|----|----|
| 11 | |  |  [[M2-brane|M2]] |  |   |  |   |   |   |   |
| 10 |  | [[F1-brane|F1]]   |   |  |   | [[NS5-brane|NS5]] |   |   |   |   |
| 9 | |   |   |  | $\ast$  |  |   |   |   |   |
| 8 | |   |   | $\ast$ |   |  |   |   |   |   |
| 7 | |   | $\ast$  |  |   |  |   |   |   |   |
| 6 | |  $\ast$  |  | [[3-brane in 6d|S3]] |   |  |   |   |   |   |
| 5 | |  | $\ast$   | |   |  |   |   |   |   |
| 4 | | $\ast$  | [[super 2-brane in 4d|M2]]$_{cmp}$   | |   |  |   |   |   |   |
| 3 | | [[super 1-brane in 3d|F1]]$_{cmp}$  |  | |   |  |   |   |   |   |










#### The full brane scan

Every Lie algebra cocycle $\mu_{p+2} \colon \mathfrak{g} \longrightarrow b^{p+1}\mathbb{R}$ induces a [[L-∞ algebra cohomology|higher extension]] of its domain, namely the [[Lie n-algebra|Lie (p+1)-algebra]] $\hat \mathfrak{g}$ which is the [[homotopy fiber]] of $\mu_{p+2}$ in the [[homotopy theory of L-∞ algebras]]:

$$
  \array{
     \hat \mathfrak{g}
     \\
     \downarrow
     \\
     \mathfrak{g}
     &\stackrel{\mu_{p+2}}{\longrightarrow}&
     b^{p+1}\mathbb{R}
  }
  \,.
$$

For the cocycles on [[super Minkowski spacetime]] from the [old brane scan](#TheOldBraneScan) these extensions are known as _[[extended super Minkowski spacetimes]]_.

$$
  \array{
     \hat \mathbb{R}^{d-1,1\vert \mathbf{N}}
     \\
     \downarrow
     \\
     \mathbb{R}^{d-1,1\vert \mathbf{N}}
     &\stackrel{\mu_{p+2}}{\longrightarrow}&
     b^{p+1}\mathbb{R}
  }
  \,.
$$

Now the extended super Minkowski spacetime $\hat \mathbb{R}^{d-1,1\vert \mathbf{N}}$ may carry further cocycles, that do not come from ordinary super Minkowski spacetime. Including these yields the full brane scan.

This complete brane scan is no longer just a table, but is a tree, a bouquet, where each edge is an $L_\infty$-extension.









##### The M5-brane




+-- {: .num_defn #RationalSphereAlgebra}
###### Definition

For $p \in \mathbb{N}_{even}$, write

$b^{2p+2} \mathbb{R}/b^p \mathbb{R}$ for the [[L-∞ algebra]] given by the [[Chevalley-Eilenberg algebra]]

$$

  CE(b^{2p+2} \mathbb{R}/b^p \mathbb{R})
  =
  \left(\left\langle g_{p+2}, g_{2p+3}\right\rangle), {{d g_{p+2} = 0} \atop {d g_{2p+3} = g_{p+2} \wedge g_{p+2}}}\right)
  \,.
$$

=--

+-- {: .num_remark #RationalSpheres}
###### Remark

Regarded as a [[Sullivan model]] in [[rational homotopy theory]], then the [[dg-algebra]] of def. \ref{RationalSphereAlgebra} is a minimal model for the [[rationalization]] of the $(p+2)$-[[sphere]].

=--

By the [recognition theorem for L-∞ extensions](model+structure+for+L-infinity+algebras#HomotopyFiberProducts) we get:

+-- {: .num_prop #b2RactionOnb2p2R}
###### Proposition

For $p \in \mathbb{N}_{even}$, there is a [[homotopy fiber sequence]] in the [[homotopy theory of L-∞ algebras]] of the form

$$
  \array{
    b^{2p+2} \mathbb{R}
    \\
    \downarrow
    \\
    b^{2p+2} \mathbb{R}/b^{p}\mathbb{R}
    &\stackrel{}{\longrightarrow}&
    b^{p+1}\mathbb{R}
  }
$$

where on [[formal dual]] [[Chevalley-Eilenberg algebras]] in terms of our defining generating elements the horizontal map is given by $g_{p+4}\mapsto g_{p+4}$ and the vertical map by $g_{p+4}\mapsto 0$ and $g_{2p+3}\mapsto g_{2p+3}$.

By the discussion at _[[∞-action]]_ this exhibits a $b^{p}\mathbb{R}$-action on $b^{2p+2}\mathbb{R}$, for which $b^{2p+2} \mathbb{R}/b^{p}\mathbb{R}$ is the [[homotopy quotient]], whence the notation.

=--

+-- {: .num_example}
###### Example

For $p=2$ and regarded as a statement in [[rational homotopy theory]] via remark \ref{RationalSpheres}, then the extension in prop. \ref{b2RactionOnb2p2R} is a [[Sullivan minimal model]] for the rationalized [[Hopf fibration]]

$$
  \array{
    S^3 &\longrightarrow& S^7
    \\
    && \downarrow
    \\
    && S^4
  }
$$

=--


+-- {: .num_defn #CocyclesOn11dSuperMinkowski}
###### Proposition

The elements $\mu_4, \mu_7 \in CE(\mathbb{R}^{10,1\vert \mathbf{32}})$,
def. \ref{ThePsiPsiTermsInCEOfSuperMinkowski}, satisfy

1. $d \mu_4 = 0$;

1. $d \mu_7 = 15 \, \mu_4 \wedge \mu_4$

=--

As a mathematical statement prop. \ref{CocyclesOn11dSuperMinkowski} is originally due to ([D'Auria-Fr&#233; 82, p.18](#DAuriaFre82)), where it is considered as an ingredient for constructing the [[action functional]] of [[11-dimensional supergravity]] in the [[D'Auria-Fré formulation of supergravity]]. The statement has been rediscovered in ([BLNPST 97, (9)](#BLNPST97)), finding its interpretation as giving the [[geometry of physics -- WZW terms|WZW term]] of the [[Green-Schwarz sigma model]] for the [[M5-brane]].


+-- {: .num_defn #m2braneLie3Algebra}
###### Definition

Write $\mathfrak{m}2\mathfrak{brane} \in sL_\infty Alg$ for the [[super L-∞ algebra]] which is the [[homotopy fiber]] of $\mu_4$ in prop. \ref{CocyclesOn11dSuperMinkowski}.

$$
  \array{
     \mathfrak{m}2\mathfrak{brane}
     \\
     \downarrow
     \\
     \mathbb{R}^{10,1\vert \mathbf{32}}
     &\stackrel{\mu_4}{\longrightarrow}&
     b^3 \mathbb{R}
  }
  \,.
$$

and specifically for the representive of this homotopy fiber which, by the [recognition theorem for L-∞ extensions](model+structure+for+L-infinity+algebras#HomotopyFiberProducts), is given by having the [[Chevalley-Eilenberg algebra]]

$$
  CE(\mathfrak{m}2\mathfrak{brane}) = (CE(\mathbb{R}^{10,1\vert \mathbf{32}})\otimes \langle h_3\rangle, d h_3 = -\mu_4)
  \,.
$$

=--

In terms of def. \ref{m2braneLie3Algebra}, the second item in prop. \ref{CocyclesOn11dSuperMinkowski} reads as follows:


+-- {: .num_cor #The7CocycleOnm2brane}
###### Corollary

There is a super $L_\infty$-cocycle of the form

$$
  \mathfrak{m}2\mathfrak{brane}
  \stackrel{h_3 \wedge \mu_4 + \frac{1}{15} \mu_7}{\longrightarrow}
  b^6 \mathbb{R}
  \,.
$$

=--

But since $\mathfrak{m}2\mathfrak{brane}$ is a $b^2 \mathbb{R}$-[[principal ∞-bundle]], it is natural to ask whether $h_3 \wedge \mu_4 + \frac{1}{15} \mu_7$ is $b^2 \mathbb{R}$-[[equivariant cohomology|equivariant]] with respect to some natural $b^2\mathbb{R}$-[[∞-action]] on $b^6 \mathbb{R}$. Such a natural action is given by prop. \ref{b2RactionOnb2p2R}. To exhibit in components the equivariance of the 7-cocycle in corollary \ref{The7CocycleOnm2brane} with respect to this action we need a [[resolution]] of [[super Minkowski spacetime]]:

+-- {: .num_defn}
###### Definition

Write $\mathbb{R}_{res}^{10,1\vert \mathbf{32}}$ for the [[super L-∞ algebra]] whose [[Chevalley-Eilenberg algebra]] is obtained from that of [[super Minkowski spacetime]] by


$$
  CE\left(
   \mathbb{R}_{res}^{10,1\vert \mathbf{32}}
  \right)
  \coloneqq
  \left(
   CE\left(
     \mathbb{R}^{10,1\vert \mathbf{32}}\right)\otimes \left\langle h_3, g_4\right\rangle ,
     {{d h_3 = g_4 - \mu_4} \atop {d g_4 = 0}}
  \right)
  \,.
$$


=--

+-- {: .num_prop}
###### Proposition

The canonical morphism

$$
  \mathbb{R}_{res}^{10,1\vert \mathbf{32}}
  \stackrel{\simeq}{\longrightarrow}
  \mathbb{R}^{10,1\vert \mathbf{32}}
$$

given dually by $\psi^\alpha \mapsto \psi^\alpha$, $e^a \mapsto e^a$, is an equivalence of $L_\infty$-algebras. It factors the morphism $\mathfrak{m}2\mathfrak{brane} \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}$ from def. \ref{m2braneLie3Algebra} through a morphism $\mathfrak{m}2\mathfrak{brane}  \longrightarrow \mathbb{R}^{10,1\vert \mathbf{32}}_{res}$ which on [[nLab:formal dual]] CE-elements is given by $h_3 \mapsto 0$, $g_4 \mapsto 0$ and by being the identity on all other generators.


=--

+-- {: .num_prop #7CocycleOnM2BraneDescends}
###### Proposition

There is a [[diagram]] of [[L-∞ algebras]] of the form

$$
  \array{
    && \vdots && && \vdots
    \\
    && \downarrow \downarrow && && \downarrow \downarrow
    \\
    &&
    \mathfrak{m}2\mathfrak{brane}
    &&
      \stackrel{h_3 \wedge \mu_4  + \frac{1}{15}\mu_7 }{\longrightarrow}
    &&
    b^6 \mathbb{R}
    \\
    &&
    \downarrow && && \downarrow
    \\
    \mathbb{R}^{10,1\vert\mathbf{32}}
    &\stackrel{\simeq}{\longleftarrow}&
    \mathbb{R}_{res}^{10,1\vert\mathbf{32}}
    &&
      \stackrel{h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7 }{\longrightarrow}
    &&
    b^6 \mathbb{R}/b^2 \mathbb{R}
    \\
    &&
    & {}_{\mathllap{}}\searrow && \swarrow
    \\
    &&
    && b^3 \mathbb{R}
  }
$$

=--

+-- {: .proof}
###### Proof

That the diagram exists and commutes at the level of the underlying graded algebras of the [[formal dual]] CE-algebras is immediate in terms of the defining generators: each generator is mapped to the generator of the same name, if present, in the codomain, or to zero otherwise, except for $g_7 \in CE(b^6 \mathbb{R})$ which is sent to $h_3 \wedge \mu_4  + \frac{1}{15}\mu_7$ and $g_7 \in CE(b^6 \mathbb{R}/b^2 \mathbb{R})$, which is sent to $h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7 $, as indicated.

It remains to check that the middle horizontal map respects the CE-differentials: by prop. \ref{CocyclesOn11dSuperMinkowski} we have

$$
  \begin{aligned}
    d(h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7)
    &=
    (g_4 - \mu_4) \wedge (g_4 + \mu_4) + \mu_4 \wedge \mu_4
    \\
    & = g_4 \wedge g_4
  \end{aligned}
$$

and by def. \ref{RationalSphereAlgebra} this says indeed that $g_7 \mapsto h_3 \wedge (g_4 + \mu_4) + \frac{1}{15}\mu_7$ respects the CE-differentials.

=--

+-- {: .num_remark}
###### Remark

The form of the equivariant cocycle in prop. \ref{7CocycleOnM2BraneDescends} is that of the [[curvature]] of the [[geometry of physics -- WZW terms|WZW term]] of the [[sigma model]] describing the [[M5-brane]] as considered in ([BLNPST 97, (6),(8)](#BLNPST97)).

=--


+-- {: .num_remark}
###### Remark

In view of remark \ref{RationalSpheres}, prop. \ref{7CocycleOnM2BraneDescends} says that the CE-elements $\mu_4$ and $\mu_7$ of prop. \ref{CocyclesOn11dSuperMinkowski} define a cocycle with values in the rational 4-sphere. In the discussions in _[[geometry of physics -- WZW terms]]_ and _[[geometry of physics -- BPS charges]]_ we see that under [[Lie integration]] and globalization in [[higher Cartan geometry]], these elements encode the [[supergravity C-field]] and its [[electric-magnetic duality|magnetic dual]]. That these fields should take values in the 4-sphere was first suggested in ([Sati 13, section 2.5](Hisham+Sati#Sati13)).

=--










##### The D-branes

(...)








#### Summary

[[!include brane scan]]


<div style="float:left;margin:0 10px 10px 0;"><img src="https://dl.dropboxusercontent.com/u/12630719/BraneBouquet.JPG" alt="the brane bouquet" /></div>








## **Semantics layer**









### The modal operators

+-- {: .num_remark #SequenceOfSites}
###### Remark

The [[sites]] in question are alternatingly (co-)[[reflective subcategories]] of each other (we always display [[left adjoints]] above their right adjoints)

$$
  \ast
  \stackrel{\longleftarrow}{\hookrightarrow}
  CartSp
  \stackrel{\hookrightarrow}{\longleftarrow}
  CartSp\rtimes InfPoint
  \stackrel{\longleftarrow}{\stackrel{\hookrightarrow}{\longleftarrow}}
  CartSp \rtimes SuperPoint
  \,.
$$


Here

* the first inclusion picks the [[terminal object]] $\mathbb{R}^0$;

* the second inclusion is that of [[reduced objects]]; the coreflection is [[reduction]], sending an algebra to its [[reduced algebra]];

* the third inclusion is that of even-graded algebras, the reflection sends a $\mathbb{Z}_2$-graded algebra to its even-graded part, the co-reflection sends a $\mathbb{Z}_2$-graded algebra to its quotient by the ideal generated by its odd part, see at _[superalgebra -- Adjoints to the inclusion of plain algebras](super+algebra#AdjointsToInclusionOfPlainAlgebra)_.

=--

+-- {: .num_remark }
###### Remark

Passing to [[(∞,1)-categories of (∞,1)-sheaves]], this yields, via [[(∞,1)-Kan extension]], a sequence of [[adjoint quadruples]] as follows:

$$
  \array{
    & && && &\longleftarrow&
    \\
    & && &\hookrightarrow& &\hookrightarrow&
    \\
    & &\longleftarrow& &\longleftarrow& &\longleftarrow&
    \\
    \Delta \colon
    &
    \infty Grpd
    &\hookrightarrow&
    Smooth \infty Grpd
    &\hookrightarrow&
    FormalSmooth \infty Grpd
    &\hookrightarrow&
    SuperFormalSmooth \infty Grpd
    \\
    & &\longleftarrow& &\longleftarrow&
    \\
    & &\hookrightarrow&
  }
$$

=--

+-- {: .num_prop #TheProcessOfModalities}
###### Proposition

Passing to the [[adjoint triples]] of [[idempotent monads]] and [[idempotent comonads]] which this induces, then yields

* on the left the [[shape modality]] $\int$, [[flat modality]] $\flat$ and [[sharp modality]] $\sharp$,

* in the middle yields the [[reduction modality]] $\Re$, the [[infinitesimal shape modality]] $\Im$ and the [[infinitesimal flat modality]] $\&$.

* on the right we get an adjoint triple whose whose middle bit $\rightsquigarrow$ is the [[bosonic modality]] and whose left piece $\rightrightarrows$ produces _super-even_ components, containing all the "[[fermion]] [[currents]]" if one wishes , which in this [[unity of opposites]] hence deserves to be called the _[[fermionic modality]]_. The further right adjoint $R$ is the [[rheonomy modality]].

Hence we get a process of [[adjoint modalities]] of the form

$$
  \array{
    && id &\dashv& id
    \\
    && \vee && \vee
    \\
    &\stackrel{fermionic}{}& \rightrightarrows &\dashv& \rightsquigarrow & \stackrel{bosonic}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{bosonic}{} & \rightsquigarrow &\dashv& Rh & \stackrel{rheonomic}{}
    \\
    && \vee && \vee
    \\
    &\stackrel{reduced}{} & \Re &\dashv& \Im & \stackrel{infinitesimal}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{infinitesimal}{}& \Im &\dashv& \& & \stackrel{\text{&#233;tale}}{}
    \\
    && \vee && \vee
    \\
    &\stackrel{contractible}{}& &#643; &\dashv& \flat & \stackrel{discrete}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{discrete}{}& \flat &\dashv& \sharp & \stackrel{differential}{}
    \\
    && \vee && \vee
    \\
    && \emptyset &\dashv& \ast
  }
$$

where "$\vee$" denotes inclusion of [[modal types]]. The first level is [[cohesion]], the second is [[differential cohesion]] ([[elasticity]]), the third is a further refinement given by supergeometry, which takes further "square roots" of all infinitesimal generators.

=--

+-- {: .proof}
###### Proof

All the sites are [[∞-cohesive sites]], which gives that we have an [[cohesive (infinity,1)-topos]]. The composite inclusion on the right is an [∞-cohesive neighbourhood site](differential+cohesive+%28infinity%2C1%29-topos#PresentationOnInfinitesimalNeighbourhoodSites), whence the inclusion $Smooth\infty Gpd\hookrightarrow SuperFormalSmooth\infty Grpd$ exhibits [[differential cohesion]].

With this the rightmost adjoint quadruple gives the [[Aufhebung]] of $\Re \dashv \Im$ by $\rightsquigarrow \dashv \R$ and the further opposition $\rightrightarrows \dashv \rightsquigarrow$.


=--

For convenience, from now on we notationally abbreviate:

$$

  \mathbf{H} \coloneqq SuperFormalSmooth0Type
  \,.
$$

+-- {: .num_remark #FromAdjunctionsToMonads}
###### Remark

Any [[reflective subcategory]]

$$
  \mathcal{C}
  \stackrel{\overset{L}{\longleftarrow}}{\underset{i}{\hookrightarrow}}
  \mathbf{H}
$$

induces an [[idempotent monad]] on $\mathbf{H}$, i.e. an [[endofunctor]]

$$
  \bigcirc \;\coloneqq\; i \circ L \;\colon\; \mathbf{H} \longrightarrow \mathbf{H}
$$

equipped with a [[natural transformation]]

$$
  \epsilon_X \;\colon\; X \longrightarrow \bigcirc X
$$

such that applying $\bigcirc$ again to that transformation it becomes an [[isomorphism]].

Dually, any [[coreflective subcategory]]

$$
  \mathcal{C}
  \stackrel{\overset{i}{\hookrightarrow}}{\underset{R}{\longleftarrow}}
  \mathbf{H}
$$

induces an [[idempotent comonad]]

$$
  \Box \;\coloneqq\; i \circ R \;\colon\; \mathbf{H} \longrightarrow \mathbf{H}
  \,.
$$

If moreover these two cases combine to an [[adjoint triple]] of the form

$$
  \mathcal{C}
   \stackrel{\hookrightarrow}{\stackrel{\longleftarrow}{\hookrightarrow}}
  \mathbf{H}
$$


or of the form

$$
  \mathcal{C}
   \stackrel{\longleftarrow}{\stackrel{\hookrightarrow}{\longleftarrow}}
  \mathbf{H}
$$


then these (co-)monads themselves are [[adjunction|adjoint]] to each other as

$$
  \Box \dashv \bigcirc
$$

or as

$$
  \bigcirc \dashv \Box
  \,,
$$

respectively, forming an "[[adjoint cylinder]]".





=--

Notice the following:

+-- {: .num_prop }
###### Proposition

The total composite labeled $\Delta$ in prop. \ref{CoReflectonsOfToposes}
is indeed the [[locally constant sheaf]]-functor for $SuperFormalSmooth0Type$.

=--

+-- {: .proof}
###### Proof

Let $X$ be any object in image of this total functor, and let $U \times D_s \in CartSp \rtimes SupeInfPoint$. Then by adjunction $SuperFormalSmooth0Type(U\times D_s, X)$ is equivalently homs in $FormalSmooth0Type$ out of the dual of the Weil algebra which is the quotient of the original one by the ideal generated by its odd part. Hence this, in turn, is equivalently homs in $Smooth0Type$ out of $U$ and that finally is equivalently homs in $Set$ out of $\ast$ into the given set.

=--

+-- {: .num_cor #SystemOfModalities}
###### Corollary

Passing, via remark \ref{FromAdjunctionsToMonads}, from the sequence of [[adjoint quadruples]] in prop. \ref{CoReflectonsOfToposes}, yields the following system of [[adjoint triples]] of [[idempotent monads]] and [[idempotent comonads]]:


$$
  \array{
    && id &\dashv& id
    \\
    && \vee && \vee
    \\
    &\stackrel{fermionic}{}& \rightrightarrows  &\dashv& \rightsquigarrow & \stackrel{bosonic}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{bosonic}{} & \rightsquigarrow &\dashv& Rh & \stackrel{rheonomic}{}
    \\
    && \vee && \vee
    \\
    &\stackrel{reduced}{} & \Re &\dashv& \Im & \stackrel{infinitesimal}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{infinitesimal}{}& \Im &\dashv& \& & \stackrel{\text{&#233;tale}}{}
    \\
    && \vee && \vee
    \\
    &\stackrel{contractible}{}& &#643; &\dashv& \flat & \stackrel{discrete}{}
    \\
    && \bot && \bot
    \\
    &\stackrel{discrete}{}& \flat &\dashv& \sharp & \stackrel{differential}{}
    \\
    && \vee && \vee
    \\
    && \emptyset &\dashv& \ast
  }
$$

where $\vee$ denotes inclusion of [[modal types]].

=--

We pronounce the operations in corollary \ref{SystemOfModalities} as follows.

* [[solidity]]

  * **[[fermionic modality]] $\rightrightarrows$** -- the spaces it sends to the point are purely fermionic, the [[odd line]];

  * **[[bosonic modality]] $\rightsquigarrow$** -- sends a super-space to the underlying bosonic space;

  * **[[rheonomy modality]] $\Rh$**;

* [[elasticity]]

  * **[[reduction modality]] $\Re$** -- removes infinitesimal thickening;

  * **[[infinitesimal shape modality]] $\Im$** -- sends a space to its [[de Rham space]];

  * **[[infinitesimal flat modality]] $\&$**;

* [[cohesion]]

  * **[[shape modality]]  $\int$** -- sends a space to its set $\pi_0$ of [[connected components]]; or rather, once we lift the discussion here from [[sheaves]] to [[infinity-stacks]], then this sends a space to its [[fundamental infinity-groupoid]];

  * **[[flat modality]] $\flat$** -- sends a space to the [[discrete space]] formed by its points;

  * **[[sharp modality]] $\sharp$**.



+-- {: .num_example }
###### Example

* For $X \in SmoothMfd \hookrightarrow Smooth0Type \hookrightarrow FormalSmooth0Type \hookrightarrow SuperFormalSmooth0Type$  any ordinary [[smooth manifold]], this is a [[bosonic modality|bosonic]] [[modal type]] $\stackrel{\rightsquigarrow}{X} \simeq X$.

* The [[odd line]] $\mathbb{R}^{0|1}$ is purely [[fermionic modality|fermionic]] in that it is an $\e$-[[comodal type]]: $\stackrel{\rightrightarrows}{\mathbb{R}^{0|1}}\simeq \ast$.

* All [[super Cartesian spaces]] $\mathbb{R}^{p|q}$ have [[contractible]] [[shape]] in that $\int \mathbb{R}^{p|q} \simeq \ast$.

=--

By applying [[universal constructions]] to the [[unit of a monad|units]]/[[counit of a comonad|counits]] of these [[modalities]], we obtain various further operations that will be useful

+-- {: .num_defn #InfinitesimalDiskBundle}
###### Definition

Given $X \in \mathbf{H}$, its _infinitesimal disk bundle_ $T_{inf} X\to X$
is the [[pullback]] of the [[unit of a monad|unit]] of the
[[infinitesimal shape modality]] along itself

$$
  \array{
    T_{inf} X &\stackrel{}{\longrightarrow}& X
    \\
    \downarrow && \downarrow
    \\
    X &\longrightarrow& \Im X
  }
  \,.
$$

Given a point $x \;\colon\;  \ast \to X$, then the [[infinitesimal neighbourhood]]
$\ast \to \mathbb{D}_x \to X$ of that point is the further [[pullback]] of the infinitesimal disk bundle to this point:

$$
  \array{
    \mathbb{D}_x &\longrightarrow & T_{inf} X &\stackrel{}{\longrightarrow}& X
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \ast &\stackrel{x}{\longrightarrow} & X &\longrightarrow& \Im X
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is the input for the formulation of [[frame bundles]] below around
prop. \ref{FrameBundle}.

=--

It is natural not to pick any point, but to collect all infinitesimal disks around _all_ the points of a space:

+-- {: .num_defn #RelativeFlat}
###### Definition

The _[[relative shape modality]]_ is the operation $\flat^{rel}$ that sends $X \in \mathbf{H}$ to the [[homotopy pullback]]

$$
  \array{
    \flat^{rel} &\longrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    \flat X &\longrightarrow& \Im X
  }
  \,.
$$

=--

There are some further relations between the modalities to take note of:

+-- {: .num_prop #Sublations}
###### Proposition

We have the following [[Aufhebung]]-relations:

* $\sharp \emptyset \simeq \emptyset$ (the [[codiscrete objects]] form a [[dense subtopos]])

* $\rightsquigarrow \Im \simeq \Im$.

=--

+-- {: .proof}
###### Proof

For any $X \in \mathbf{H}$ and any $U \times D_s\in CartSp \rtimes SuperInfPoint \hookrightarrow \mathbf{H}$ we have by [[adjunction]] [[natural equivalences]]

$$
  \begin{aligned}
    \mathbf{H}(U \times D_s , \stackrel{\rightsquigarrow}{\Im X})
    & \simeq
    \mathbf{H}(\stackrel{\rightrightarrows}{U \times D_s} , \Im X)
    \\
    &\simeq
    \mathbf{H}(\Re(\stackrel{\rightrightarrows}{U \times D_s}) , X)
    \\
    & \simeq
    \mathbf{H}(U, X)
    \\
    & \simeq
    \mathbf{H}(\Re(U \times D_s), X)
    \\
    & \simeq \mathbf{H}(U \times D_s, \Im X)
  \end{aligned}
  \,.
$$

=--





## References

The following first mentions

* [General accounts](#GeneralReading)

that might usefully be held on to during the seminar. Then I list

* [Special literature](#MoreDetails)

with refernces to original results and to reviews of these. Then I list pointers to my own work with collaborators on

* [Higher super Cartan geometry](#ReferencesHigherSuperCartan)


### General accounts
 {#GeneralReading}

An excellent general textbook for our purposes is

* {#CDF} [[nLab:Leonardo Castellani]], [[nLab:Riccardo D'Auria]], [[nLab:Pietro Fré]], _[[nLab:Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

This is written by physicists in physics style, but the development is careful and thorough, and the "geometric perspective" in the title is nothing but the perspective of higher [[nLab:super Cartan geometry]] in slight disguise. See also at _[[nLab:D'Auria-Fré formulation of supergravity]]_.

Lecture notes closely related to the seminar are in

* {#StructureTheory} [[nLab:Urs Schreiber]], _[[Structure Theory for Higher WZW Terms]]_, lectures at _[Higher Structures in String Theory and Quantum Field Theory](http://www.esi.ac.at/activities/events/2015/higher-structures-in-string-theory-and-quantum-field-theory)_, ESI Vienna, November 30-December 4, 2015

### More specialized literature
 {#MoreDetails}

[[nLab:Deligne's theorem on tensor categories]] is due to

* {#Deligne02} [[nLab:Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

building on his general work on [[nLab:Tannakian categories]]

* [[nLab:Pierre Deligne]], _[[nLab:Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp.111-195. ([pdf](https://publications.ias.edu/sites/default/files/60_categoriestanna.pdf))

A brief survey is in

* {#Ostrik04} [[nLab:Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))

and a more comprehensive texbook account is in chapter 9.11 of

* {#EGNO15} [[nLab:Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[nLab:Victor Ostrik]], _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))



The observation that [[nLab:supergeometry]] is naturally regarded as ordinary geometry inside the [[nLab:sheaf topos]] over [[nLab:superpoints]] is due to

* {#Schwarz84} [[nLab:Albert Schwarz]], _On the definition of superspace_, Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 37&#8211;42, ([russian original pdf](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

* {#KonechnySchwarz97} Anatoly Konechny, [[nLab:Albert Schwarz]],  _On $(k \oplus l|q)$-dimensional supermanifolds_ in _Supersymmetry and Quantum Field Theory_ (D. Volkov memorial volume) Springer-Verlag, 1998, Lecture Notes in Physics, 509 , J. Wess and V. Akulov (editors)([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 - 486

A nice account is in

* {#Sachse08} [[nLab:Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))

Useful discussion of [[nLab:Majorana spinors]] and the induced [[nLab:supersymmetry]] algebras includes

* [CDF, II.7.3](#II.7.3)

* {#FigueroaOFarrill} [[nLab:José Figueroa-O'Farrill]], _Majorana spinors_ ([pdf](http://www.maths.ed.ac.uk/~jmf/Teaching/Lectures/Majorana.pdf))

The close relation between [[nLab:supersymmetry and division algebras]] was first observed in

* {#KugoTownsend83} Taichiro Kugo, [[nLab:Paul Townsend]], _Supersymmetry and the division algebras_, Nuclear Physics B, Volume 221, Issue 2 (1983) p. 357-380. ([spires](http://inspirehep.net/record/181889), [pdf](http://cds.cern.ch/record/140183/files/198301032.pdf))

A clean survey is in

* {#BH09} [[nLab:John Baez]], [[nLab:John Huerta]], _Division algebras and supersymmetry I_, in  R. Doran, G. Friedman, [[nLab:Jonathan Rosenberg]](eds.) _Superstrings, Geometry, Topology, and $C^\ast$-algebras_,  Proc. Symp. Pure Math. 81, AMS, Providence, 2010, pp. 65-80 ([arXiv:0909.0551](http://arxiv.org/abs/0909.0551))

and the discussion of the spinor bilinear pairings from this perspective is in

* {#BH10} [[nLab:John Baez]], [[nLab:John Huerta]], _Division algebras and supersymmetry II_, Adv. Math. Theor. Phys. 15 (2011), 1373-1410 ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))

The seminal analysis of [[nLab:torsion of G-structures]] is due to

* {#Guillemin65} [[nLab:Victor Guillemin]], _The integrability problem for $G$-structures_, Trans. Amer. Math. Soc. 116 (1965), 544&#8211;560. ([JSTOR](http://www.jstor.org/stable/1994134))

Discussion of [[nLab:torsion of G-structures]] in the context of [[nLab:supergeometry]] ([[nLab:supertorsion]]) is in

* {#Lott01} [[nLab:John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

An elegant construction of [[nLab:11-dimensional supergravity]], right in the spirit of [[nLab:super Cartan geometry]], is due to

* {#DAuriaFre82}  [[nLab:Riccardo D'Auria]], [[nLab:Pietro Fré]]; _Geometric Superravity in D=11 and its hidden supergroup_, Nuclear Physics B201 (1982) 101-140 ([pdf](https://ncatlab.org/nlab/files/GeometricSupergravity.pdf))

This is the main original result on which the [[nLab:D'Auria-Fré formulation of supergravity]] is based, as laid out in [CDF](#CDF).

The observation that the [[nLab:equations of motion]] of bosonic solutions of [[nLab:11-dimensional supergravity]] are equivalent simply to vanishing of the [[nLab:supertorsion]] is due to

*  {#CandielloLechner93} A. Candiello, K. Lechner, _Duality in Supergravity Theories_, Nucl.Phys. B412 (1994) 479-501 ([arXiv:hep-th/9309143](http://arxiv.org/abs/hep-th/9309143))

* {#Howe97} [[nLab:Paul Howe]], _Weyl Superspace_, Physics Letters B
Volume 415, Issue 2, 11 December 1997, Pages 149&#8211;155 ([arXiv:hep-th/9707184](http://arxiv.org/abs/hep-th/9707184))

Discussion of [[nLab:Fierz identities]] includes

* [CDF, II.8](#CDF)

The classification of the invariant super Lie algebra cocycles on super-Minkowski spacetime, hence that of [[nLab:super p-branes]] without gauge fields on their worldvolume, is due to

* {#AETW87} Anna Ach&#250;carro, [[nLab:Jonathan Evans]], [[nLab:Paul Townsend]], [[nLab:David Wiltshire]], _Super $p$-Branes_, Phys. Lett. B **198** (1987) 441 ([spire](http://inspirehep.net/record/22286?ln=en))

The extension of this classification to [[nLab:D-branes]] and to the [[nLab:M5-brane]] using [[nLab:extended super Minkowski spacetime]] is due to

* {#CAIB99} C. Chrysso&#8204;malakos, [[nLab:José de Azcárraga]], J. M. Izquierdo and C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nuclear Physics B Volume 567, Issues 1&#8211;2, 14 February 2000, Pages 293&#8211;330 ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))

* {#Sakaguchi00} Makoto Sakaguchi, _IIB-Branes and New Spacetime Superalgebras_, JHEP 0004 (2000) 019 ([arXiv:hep-th/9909143](https://arxiv.org/abs/hep-th/9909143))

The M5-brane cocycle on the "M2-brane extended super-Minkowski spacetime" that appears here has in fact been observed, as a cocycle, all the way back in [D'Auria-Fr&#233; 82](#DAuriaFre82). But there it was seen just as a means for constructing [[nlab:11-dimensional supergravity]]. That it indeed gives the [[nLab:higher WZW term]] in the [[nLab:Green-Schwarz action functional|Green-Schwarz type action functional]] that defines the fundamental [[nLab:M5-brane]] has been argued in

* {#BLNPST97} [[nLab:Igor Bandos]], [[nLab:Kurt Lechner]], Alexei Nurmagambetov, [[nLab:Paolo Pasti]], [[nLab:Dmitri Sorokin]], Mario Tonin, _Covariant Action for the Super-Five-Brane of M-Theory_, Phys.Rev.Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))

The observation that [[nLab:super p-branes]] on curved [[nLab:super spacetimes]] require [[nLab:definite globalization of WZW term|definite globalization]] of super Lie algebra cocycles from Minkowski spacetime over the supermanifold is due to

* {#BergshoeffSezginTownsend86} [[nLab:Eric Bergshoeff]], [[nLab:Ergin Sezgin]], [[nLab:Paul Townsend]], _Superstring actions in $D = 3, 4, 6, 10$ curved superspace_, Phys.Lett., B169, 191, (1986) ([spire](http://inspirehep.net/record/223138/?ln=en))

* {#BergshoeffSezginTownsend87}  [[nLab:Eric Bergshoeff]], [[nLab:Ergin Sezgin]], [[nLab:Paul Townsend]], _Supermembranes and eleven dimensional supergravity_, Phys.Lett. B189 (1987) 75-78, In [[nLab:Mike Duff]],  (ed.), _[[nLab:The World in Eleven Dimensions]]_ 69-72 ([pdf](http://streaming.ictp.trieste.it/preprints/P/87/010.pdf), [spire](http://inspirehep.net/record/248230?ln=en))

The formulation of [[nLab:topological T-duality]] is due to

* {#BouwknegtEvslinMathai04} [[nLab:Peter Bouwknegt]], [[nLab:Jarah Evslin]], [[nLab:Varghese Mathai]], _T-Duality: Topology Change from H-flux_, Commun.Math.Phys.249:383-415,2004 ([hep-th/0306062](http://arxiv.org/abs/hep-th/0306062))

and in an alternative form due to

* {#BunkeRumpfSchick08} {#BunkeRumpfSchick08} [[nLab:Ulrich Bunke]], P. Rumpf, [[nLab:Thomas Schick]], _The topology of $T$-duality for $T^n$-bundles_,  Rev. Math. Phys. 18, 1103 (2006). ([arXiv:math.GT/0501487](http://arxiv.org/abs/math.GT/0501487))



The suggestion that there ought to be "[[nLab:T-folds]]" or "[[nLab:double field theory|doubled geometry]]" is due to

* {#Hull04} [[nLab:Chris Hull]], _A Geometry for Non-Geometric String Backgrounds_, JHEP0510:065,2005 ([arXiv:hep-th/0406102](http://arxiv.org/abs/hep-th/0406102))

* {#Hull06} [[nLab:Chris Hull]], _Doubled geometry and T-folds_ JHEP0707:080,2007  ([arXiv:hep-th/0605149](http://arxiv.org/abs/hep-th/0605149))

The mathematical formalization of this idea in terms of [[nLab:principal 2-bundles]] for the [[nLab:T-duality 2-group]] was claimed in

* {#Nikolaus14} [[nLab:Thomas Nikolaus]], _T-Duality in K-theory and elliptic cohomology_, talk at _String Geometry Network Meeting_, Feb 2014, ESI Vienna ([website](http://www.ingvet.kau.se/juerfuch/conf/esi14/esi14_34.html))


### Higher super Cartan geometry
 {#ReferencesHigherSuperCartan}

The following articles develop the higher super Cartan geometry that we give an exposition of in the second part of the seminar.

The mathematical foundation of higher supergeometry:

* {#dcct} [[nLab:Urs Schreiber]], _[[differential cohomology in a cohesive topos]]_, Thesis, ([v1 arXiv:1310.7930](http://arxiv.org/abs/1310.7930v1), [v2](https://dl.dropboxusercontent.com/u/12630719/dcct.pdf))

The general idea of [[The brane bouquet]] and the general construction of [[nLab:higher WZW terms]] from higher $L_\infty$-cocycles:

* {#FSS13} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]],   _[[The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ International Journal of Geometric Methods in Modern Physics Volume 12, Issue 02 (2015) 1550018, ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

The homotopy-[[nLab:descent]] of the [[nLab:M5-brane]] cocycle and of the type IIA [[nLab:D-brane]] cocycles:

* {#FSS16} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[Rational sphere valued supercocycles in M-theory]]_, to appear in Journal of Geometry and Physics ([arXiv:1606.03206](http://arxiv.org/abs/1606.03206))

The derivation of supersymmetric [[nLab:topological T-duality]], rationally, and of the higher super Cartan geometry for [[nLab:super T-folds]]:

* {#FSS16a} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[T-Duality from super Lie n-algebra cocycles for super p-branes]]_ ([arXiv:1611.06536](https://arxiv.org/abs/1611.06536))

The derivation of the process of higher invariant extensions that leads from the [[nLab:superpoint]] to [[nLab:11-dimensional supergravity]]:

* {#MTheoryFromTheSuperpoint} [[nLab:John Huerta]], [[nLab:Urs Schreiber]], _[[M-Theory from the Superpoint]]_


