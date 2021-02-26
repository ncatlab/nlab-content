
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The concept of _super-scheme_ is the generalization of that of _[[scheme]]_ from [[commutative algebra]] to [[supercommutative superalgebra]]: where an ordinary [[scheme]] is a space locally modeled on the [[formal dual]] of a [[commutative ring]] (i.e. an [[affine scheme]]), so a superscheme is a space locally modeled on the formal dual of a [[supercommutative algebra]] (i.e. on affine superschemes, def. \ref{AffineSuperSchemes} below).


### Affine superschemes

The following is a detailed and conceptual introduction of the concept of affine super-schemes. This is taken from _[[geometry of physics -- superalgebra]]_.

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

are **[[affine super schemes]]** over $k$.

=--

+-- {: .num_example #OrdinaryCAlgAssCAlg}
###### Example

For $A \in CAlg_{\mathbb{R}}$ an ordinary [[commutative algebra]] over $\mathbb{R}$,
then of course this becomes a [[supercommutative superalgebra]] by regarding it
as being concentrated in even degrees. Accordingly, via def. \ref{Affines}, ordinary [[affine schemes]]
[[full subcategory|fully embed]] into [[affine super schemes]] (def. \ref{AffineSuperSchemes})

$$
  Aff(Vect_k)
    \hookrightarrow
  Aff(sVect_k)
  \,.
$$

In particular for $\mathbb{R}^p$ an ordinary [[Cartesian space]], this becomes
an [[affine superscheme]] in even degree, under the above embedding. As such, it is usually
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

+-- {: .num_example #SuperCartesianSpace}
###### Example

Combining example \ref{OrdinaryCAlgAssCAlg} with example \ref{Superpoint},
and using prop. \ref{ProductsInAff}, we obtain the  [[affine super schemes]]

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

Dually, via def. \ref{Affines}, this means that every [[affine super scheme]] has a canonical [[involution]].

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










## Related concepts

* [[supergroup]]

* [[Deligne's theorem on tensor categories]]

* [[spectral super-scheme]]

## References

General accounts include

* Carmeli-Caston-Fioresi: _Mathematical foundations of supersymmetry_, EMS Series of Lectures in Mathematics, EMS 2011

* [[Mikhail Kapranov]]  [[Eric Vasserot]], _Supersymmetry and the formal loop space_, Advances in Math. 227 (2011), 1078-1128 ([arXiv:1005.4466](https://arxiv.org/abs/1005.4466))

* [[Ugo Bruzzo]], Daniel Hernandez Ruiperez, [[Alexander Polishchuk]], _Notes on fundamental algebraic supergeometry. Hilbert and Picard superschemes_ ([arXiv:2008.00700](https://arxiv.org/abs/2008.00700))



Discussion of [[crystalline cohomology]] of super-schemes:


* Martin Luu, _Crystalline cohomology of superschemes_ ([pdf](http://math.uiuc.edu/~mluu/Luu-crystalline.pdf))


[[!redirects super-schemes]]

[[!redirects super scheme]]
[[!redirects super schemes]]

[[!redirects superscheme]]
[[!redirects superschemes]]

[[!redirects affine super scheme]]
[[!redirects affine super schemes]]
[[!redirects affine super-scheme]]
[[!redirects affine super-schemes]]
[[!redirects affine superscheme]]
[[!redirects affine superschemes]]
