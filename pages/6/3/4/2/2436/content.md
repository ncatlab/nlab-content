

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **super vector space** is an [[object]] in the non-trivial [[symmetric monoidal category]] structure on the [[monoidal category]] of $\mathbb{Z}/2$-[[graded vector spaces]]: as an object it is just a $\mathbb{Z}/2$-[[graded vector space]], but the [[braiding]] of the underlying [[tensor product of vector spaces]] is taken to be the non-trivial linear map which on elements of homogeneous degree is given by

$$ 
  \tau^{super} 
   \;\colon\; 
  v \otimes w \;\mapsto\; (-1)^{deg(v) deg(w)} \, w \otimes v 
  \,.
$$

Super vector spaces form the basis of [[superalgebra]] (over [[ground rings]] which are [[fields]]) in direct analogy of how ordinary vector spaces form the basis of ordinary [[algebra]]. For more on this see [below](#StructuresInternalToSuperVectorSpaces).

## Background

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


## Definition

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

for the [[full subcategory]] on those objects $L \in \mathcal{C}$ which are invertible under the [[tensor product]], i.e. such that there is an object $L^{-1} \in \mahcal{C}$ with $L \otimes L^{-1} \simeq 1$ and $L^{-1} \otimes L \simeq 1$. Since the [[tensor unit]] is clearly in $Line(L)$ (with $1^{-1} \simeq 1$) and since with $L_1, L_2 \in Line(\mathcal{C}) \hookrightarrow \mathcal{C}$ also $L_1 \otimes L_2 \in Line(\mathcal{C})$ (with $(L_1 \otimes _2)^{-1} \simeq L_2^{-1} \otimes L_1^{-1}$) the [[monoidal category]] structure on $\mathcal{C}$ restricts to $Line(\mathcal{C})$. 


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


+-- {: .num_defn #CatgeoryOfSuperVectorSpaces} 
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

## Properties

### Structures internal to super-vector spaces
 {#StructuresInternalToSuperVectorSpaces}

By [[internalization|internalizing]] [[algebra]] and [[geometry]] in the category $sVect$ of super vector spaces, one obtains the corresponding [[superalgebra]] and [[supergeometry]].

For example

* [[monoids]] in $sVect$ are [[super algebras]]] and, more interstingly, [[commutative monoids]] in $sVect$ are [[supercommutative superalgebra]];

* hence for example [[commutative Hopf algebras]] in $sVect$ are equivalently [[supercommutative Hopf algebras]], which are the [[formal duals]] of affine algebraic [[supergroups]];

* [[Lie algebras]] in $sVect$ are [[super Lie algebras]];

* [[manifolds]] modeled on objects of $sVect$ are [[supermanifolds]]

* etc.

By the above definition, any structure in $sVect$ works just like the corresponding structure in [[Vect]], but with a sign inserted whenever two odd-graded symbols are interchanged. For more on this see also at _[[signs in supergeometry]]_.

### Deligne's theorem on tensor categories

[[Deligne's theorem on tensor categories]] says that all suitable [[tensor categories]] of subexponential growth have a [[fiber functor]] to $sVect$ and are equivalent to [[categories of representations]] of affine algebraic [[supergroups]].

## Related concepts

* [[supertrace]]


## References


* {#Varadarajan04} [[Veeravalli Varadarajan]], section 3.1 of  _[[Supersymmetry for mathematicians]]: An introduction_, Courant lecture notes in mathematics, American Mathematical Society Providence, R.I 2004
 

[[!redirects sVect]]
[[!redirects SuperVect]]


[[!redirects super vector space]]
[[!redirects super vector spaces]]
[[!redirects supervector space]]
[[!redirects supervector spaces]]
[[!redirects super-vector space]]
[[!redirects super-vector spaces]]

[[!redirects category of super vector spaces]]
[[!redirects category of super-vector spaces]]
[[!redirects category of supervector spaces]]
