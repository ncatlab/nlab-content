
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
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
 {#Idea}

The [[space]] of [[functions]] $\mathcal{C}_1 \to R$ on the [[space]] of [[morphisms]]  $\mathcal{C}_1$ of a [[small category]] $\mathcal{C}_\bullet$ (with [[coefficients]] in some [[ring]] $R$) naturally inherits a [[convolution algebra]] structure from the [[composition]] operation on morphisms. This is called the _category convolution algebra_ or just _category algebra_ for short.

Often this is considered specifically for [[groupoids]] and hence accordingly called _groupoid convolution algebra_ or just _groupoid algebra_ for short. (For one-object [[delooping]] groupoids of [[groups]], groupoid algebras reduce to [[group algebras]].) The [[inverse|inversion operation]] of the groupoid naturally makes its groupoid algebra into a [[star-algebra]] (this is generally the case for category algebras of [[dagger categories]]) and accordingly groupoid algebras play a role in [[C-star-algebra]] theory.

More generally, if the groupoid carries a [[line 2-bundle]] then (in its incarnation as a [[bundle gerbe]]-like transition bundle) the space of morphisms carries a [[line bundle]] (satisfying some compatibility conditions) and one can consider convolution algebras not just of functions, but of [[sections]] of this line bundle. The resulting algebra is called the _twisted groupoid convolution algebra_, twisted by the [[characteristic class]] of the [[line 2-bundle]] ([TXLG](#TXLG)).

For "bare" categories/groupoids (i.e.: [[internal category|internal]] to [[Set]]) these constructions are canonical. But under mild conditions or else when equipped some suitable extra [[stuff, structure, property|structure]], it generalizes to [[internal categories]]/[[internal groupoids]] in [[geometry|geometric]] contexts, notably in [[topology]] ([[topological groupoids]]), [[differential geometry]] ([[Lie groupoids]]), and [[algebraic geometry]]. In such geometric situations a groupoid convolution algebra equipped with its canonical [[coalgebra]] structure over the functions on its canonical [[atlas]] is also called a _[[Hopf algebroid]]_ and may be used to _characterize_ the geometric groupoid.

Therefore to some extent one may think of the relation between groupoids/categories and their groupoid/category algebras as an incarnation of the [[Isbell duality|general duality]] between [[geometry]] and [[algebra]]. Since category/groupoid algebras are generically non-commutative, this relation identifies groupoids/categories as certain spaces in [[noncommutative geometry]]. From this point of view groupoid convolution algebras have been highlighted and developed notably in ([Connes 94](#Connes094)). Due to this relation the groupoid convolution product is also referred to as a [[star product]] and denoted "$\star$". Groupoid [[C*-algebras]] form a rich sub-class of all [[C*-algebras]], including [[crossed product C*-algebras]], [[Cuntz algebras]].

Groupoid convolution algebras may also be understood as generalizations of [[matrix algebras]], to which they reduce for the case of the [[pair groupoid]]. In ([Connes 94, 1.1](#Connes094)) it was famously argued that when [[Werner Heisenberg]] (re-)discovered (infinite-dimensional) [[matrix algebras]] as [[algebras of observables]] in [[quantum mechanics]], conceptually he rather considered groupoid convolution algebras. This perspective has since been fully developed: in ([EH 06](#EH)) [[strict deformation quantization]] is given fairly generally by twisted groupoid convolution algebras. See at _[[geometric quantization of symplectic groupoids]]_ for more on this. For the [[discrete groupoid|discrete]] but [[higher geometry]] of [[infinity-Dijkgraaf-Witten theory]] quantization by higher groupoid convolution algebras is indicated in ([FHLT 09](#FHLT)).


## Definition

### For bare categories (discrete geometry)

+-- {: .num_defn #CategoryAlgebra}
###### Definition

Let $\mathcal{C}$ be a [[small category]] and let $R$ be a [[ring]].

The **category algebra** or **[[convolution algebra]]** $R[\mathcal{C}]$ of $\mathcal{C}$ over $R$ is the $R$-[[associative algebra|algebra]]

* whose underlying $R$-[[module]] is the [[free module]] $R[\mathcal{C}_1]$ over the set of [[morphisms]] of $\mathcal{C}$;

* whose product operation is defined on [[basis]]-elements $f,g \in \mathcal{C}_1 \hookrightarrow R[\mathcal{C}]$ to be their [[composition]] if they are composable and zero otherwise:

  $$
    f \cdot g := \left\lbrace
      \array{
        g \circ f & if\;composable
        \\
        0 & otherwise
      }
    \right.
   \,.
  $$ 

=--

+-- {: .num_remark #AsConvolutionAlgebra}
###### Remark

We may identify elements in $R[\mathcal{C}_1]$ with [[functions]] $\mathcal{C}_1 \to R$ with the property that they are non-vanishing only on finitely many elements. Under this identification for $\phi_1, \phi_2$ two such functions, their product in $R[\mathcal{C}]$ is given by the formula

$$
  \phi_1 \cdot \phi_2
  \;
   \colon
  \;
  f \mapsto
  \sum_{f_2 \circ f_1 = f}
  \phi_2(f_2)
  \cdot
  \phi_1(f_1)   
  \,,
$$

where $f,f_1,f_2 \in \mathcal{C}_1$. In particular if $\mathcal{C}$ is a [[groupoid]] so that every [[morphisms]] $f$ has an [[inverse]] $f^{-1}$ then this is equivalently

$$
  \phi_1 \cdot \phi_2
  \;
   \colon
  \;
  f \mapsto
  =
  \sum_{g \in \mathcal{C}_1}
  \phi_2(f \circ g^{-1})
  \cdot
  \phi_1(g) 
  \,.
$$

This expresses [[convolution]] of functions.


=--


+-- {: .num_defn #InvolutionByPullbackAlongInversion}
###### Remark

If the small category $\mathcal{C}_\bullet$ is a [[groupoid]], hence equipped with an [[inverse|inversion]] map

$$
  inv \colon \mathcal{C}_1 \to \mathcal{C}_1
$$

then [[pullback of functions]] along this map is an [[involution]] of the convolution algebra of $\mathcal{C}$ and hence makes it into a [[star-algebra]]. 

More generally for $\mathcal{C}$ equipped with the structure of a [[dagger-category]], pullback along the dagger-functor

$$
  \dagger \colon \mathcal{C}_1 \to \mathcal{C}_1
$$

makes the convolution algebra a star-algebra.

=--
+-- {: .num_defn #catalgebraIsWeakHopfalgebra}
###### Remark

If the category has finitely many objects and finitely many morphisms, then the category algebra is also a coalgebra via the unique comultiplication where every morphism in $C_1\subset R[C_1]$ is group like; the structure of the coalgebra and that of an algebra are compatible in the sense that they form a [[weak Hopf algebra]].

=--

### For Lie groupoids
 {#ForLieGroupoids}


We discuss groupoid convolution [[C*-algebras]] for [[Lie groupoids]]/[[differentiable stacks]] (def. \ref{ContinuousCategoryAlgebraWithHalfDensities}, prop. \ref{GroupoidConvolutionIs2Functor} below).

+-- {: .num_remark #ForLieGroupoids}
###### Remark

If $\mathcal{C}$ is a groupoid with extra [[geometry|geometric]] structure, then there are natural variants of the above definition.

Notably if $\mathcal{C}$ is a [[Lie groupoid]] then there is a variant where the functions in remark \ref{AsConvolutionAlgebra} are taken to be [[smooth functions]] and where the convolution [[sum]] is replaced by an [[integration]]. In order for this to make sense one needs to consider in fact functions with values in half-[[densities]] over the [[manifold]] $\mathcal{C}_1$.

More generally, for a [[bundle gerbe]] over a Lie groupoid $\mathcal{C}$, hence a multiplicative [[line bundle]] over $\mathcal{C}_1$, one can consider a convolution product on [[sections]] of this line bundle tensored with half-densities.

=--

See the [References -- For continuous/smooth geometry](#ReferencesForSmoothGeometry).


+-- {: .num_defn #ContinuousCategoryAlgebraWithHalfDensities}
###### Definition
**([[Lie groupoid convolution algebra]])**

Let $\mathcal{G}_\bullet$ be a [[Lie groupoid]]. Write $C^\infty_c(\mathcal{G}_1, \sqrt{\Omega})$ for the space of smooth [[half-densities]] in $T_{d s = 0}\Gamma_1 \oplus T_{d t = 0}\Gamma_1$ of [[compact support]] on its [[manifold]] $\mathcal{G}_1$ of [[morphisms]]. Let the  [[convolution product]] 

$$
  \star \;\colon\; C_c(\mathcal{G}_1, \sqrt{\Omega}) \times C_c(\mathcal{G}_1, \sqrt{\Omega}) \to C_c(\mathcal{G}_1, \sqrt{\Omega})
$$

be given on elements $f,g \in C_c(\mathcal{G}_1, \sqrt{\Omega})$ over any element $\gamma \in \mathcal{G}_1$ by the [[integral]]

$$
  (f \star g) \colon \gamma
  \mapsto
  \int_{\gamma_2\circ \gamma_1 = \gamma}
  f(\gamma_1) \cdot f(\gamma_2)
  \,.
$$

(Here we regard the integrand naturally as taking values in actual [[densities]] tensored with the pullback of $\sqrt{\Omega}$ along the composition map. This defines the [[integration]] of density-factor which then takes values in $\sqrt{\Omega}$.)

The algebra $(C_c^\infty(\mathcal{G}_1, \sqrt{\Omega}), \star)$ is the **groupoid convolution algebra** of smooth compactly supported functions. As in remark \ref{AsConvolutionAlgebra}, this is naturally a [[star-algebra]] with [[involution]] $inv^\ast$.

=--

This construction originates around ([Connes 82](#Connes82)).

+-- {: .num_prop}
###### Proposition/Definition

For $\mathcal{G}_\bullet$ a [[Lie groupoid]] and for $x \in \mathcal{G}_0$ any point in the manifold of [[objects]]
there is an involutive [[representation]] $\pi_x$ of the convolution algebra
$(C_c^\infty(\mathcal{G}_1, \sqrt{\Omega}), \star, inv^\ast)$ of def. \ref{ContinuousCategoryAlgebraWithHalfDensities} on the [[canonical Hilbert space of half-densities]] $L^2(s^{-1}(x))$ of the source fiber of $x$  given on any $\xi \in L^2(s^{-1}(x))$ by

$$
\pi_x(f) \xi \colon \gamma
 \mapsto 
  \int_{\gamma_1 \in t^{-1}(\gamma)}
  f(\gamma_1) \xi(\gamma_1^{-1}\gamma)
  \,.
$$

This defines a [[norm]] $|{\Vert \Vert}$ on the [[vector space]] $C_c^\infty(\mathcal{G}_1, \Omega)$ given by the [[supremum]] of the norms in $L^2(s^{-1}(x))$ over all points $x$:

$$
  {\Vert f\Vert}
  \coloneqq
  Sup_{x \in \mathcal{G}_0} {\Vert \pi_x(f)\Vert}
  \,.
$$

The [[Cauchy completion]] of the [[star algebra]] $(C_c^\infty(\mathcal{G}_1, \sqrt{\Omega}), \star, inv^\ast)$ with respect to this [[norm]] is a [[C-star-algebra]], the **convolution $C^\ast$-algebra** of the Lie groupoid $\mathcal{G}_\bullet$.


=--

This is recalled at ([Connes 94, prop. 3 on p. 106](#Connes94)).

+-- {: .num_remark #ExtensionToBibundlesAndBimodules}
###### Remark

With suitable definitions, this construction constitutes something at least close to a [[2-functor]] from [[differentiable stacks]] to [[C-star-algebras]] and [[Hilbert bimodules]] between them:

In ([Mr&#269;un 99](#Mrcun99)) the convolution algebra construction for [[étale Lie groupoids]] is extended to groupoid [[bibundles]] and shown to produce a [[functor]] to [[C-star-algebras]] with (isomorphism classes of) [[bimodules]] between them. In ([Kali&#353;nik-Mr&#269;un 07](#KalisnikMrcun)) it is shown that if one remembers the additional [[Hopf algebroid]] structure on the convolution $C^\ast$-alegras (the algebraic analog of remebering the [[atlas]] of the [[differentiable stack]] of a Lie groupoid) then this construction becomes a [[full subcategory]] inclusion of &#233;tale Lie groupoids into their convolution Hopf algebroids.

In ([Muhly-Renault-Williams 87](#MuhleReaultWilliams87), [Landsman 00](#Landsman00)) the generalization of the construction of a $C^\ast$-bimodule from a groupoid [[bibundle]] to general [[Lie groupoids]] is discussed (not necessarily [[étale Lie groupoid|étale]]), but only equivalence-bibundles are considered and are shown to yield [[Morita equivalence]] bimodules (no discussion of composition and functoriality here).

=--

A precise form of this statement is the following [Nuiten 13, theorem 3.3.1](#Nuiten13)

+-- {: .num_prop #GroupoidConvolutionIs2Functor}
###### Proposition
**([[groupoid convolution algebra]] is [[(2,1)-functor]] from [[differentiable stacks]] to [[C*-algebras]])**

The above construction of groupoid convolution algebras (def. \ref{ContinuousCategoryAlgebraWithHalfDensities}) extends to a [[(2,1)-functor]]

$$
  C^\ast(-)
  \;\colon\;
  DiffStack^{prop}
    \overset{\phantom{AAA}}{\longrightarrow}
  C^\ast Alg^{op}_{bim}
$$

between 

1. the [[(2,1)-category]] $DiffStack_{prop}$ of [[differentiable stacks]] (i.e. [[Lie groupoids]] regarded as [[smooth stacks]]) with proper morphisms between them ([Nuiten 13, def. 2.2.35](#Nuiten13))

1. the [[opposite 2-category|opposite]] [[(2,1)-category]] of [[C*-algebras]] with [[Hilbert bimodules]] between them and [[intertwiners]] between those.

=--

([Nuiten 13, theorem 3.3.1](#Nuiten13))

This way, much of [[noncommutative geometry]] is exhibited as actually being the [[higher geometry]] of [[differentiable stacks]] inside all [[smooth stacks]]. In particular, [[groupoid K-theory]] is realized as the [[KK-theory]] of convolution C*-algebras.

## Equivalent characterizations

We discuss equivalent characterizations of category algebras/groupoid algebras that are useful in certain context

* [As a weak colimit over a constant 2Vect-valued functor
](#WeakColimit)

* [In terms of composition of spans](#InTermsOfCompositionOfSpans)

### As a weak colimit over a constant $2Vect$-valued functor
 {#WeakColimit}

Apparently for $\mathcal{C}$ a [[groupoid]] the 
category algebra of $C$ is the [[weak limit|weak colimit]] over $\mathcal{C}$ of the functor $\mathcal{C} \to Vect\text{-}Mod$
constant on the ground field algebra.

This statement is for instance in ([FHLT, section 8.4](#FHLT)).

The 2-cell in the universal co-cone corresponding
to the morphism $f \in C$ is the $k\text{-}k[C]$-bimodule
homomorphism $f \cdot (-) :  A \to A$ that multiplies
by $f \in k[C]$ from the left.

$$
  \array{
     x &&\stackrel{f}{\to}&& y
     \\
     k &&\stackrel{k}{\to}&& k
     \\
     & {k[C]}_{\mathllap{}}\searrow 
      &\swArrow_{f \cdot (-)}& 
     \swarrow_{\mathrlap{k[C]}}
     \\
     && k[C]
  }
$$

This description should be compared with the analogous description of the [[action groupoid]] by a weak colimit. One sees that the groupoid algebra is a linear incarnation of the action groupoid in some sense.




### In terms of composition of spans
 {#InTermsOfCompositionOfSpans}

The category algebra of a category $C$ is a special case of a general construction of [[spans]] (see also at _[[bi-brane]]_). 

In order not to get distracted by inessential technicalities, consider the case of a finite [[category]] $C$, i.e. an [[internal category]] in [[FinSet]]. This is a [[span]]
$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&&&
     C_0
  }
$$
equipped with a composition operation: a morphism
of spans from the composite span 
$$
  \array{
     &&&&
     C_1 \times_{t,s} C_1
     \\
     &&& \swarrow && \searrow
     \\
     && C_1
     &&&& C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
      && {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&&&
     C_0
     &&&&
     C_0
  }
$$
to the original one, i.e. a morphism 
$$
  comp : C_1 \times_{t,s} C_1 \to C_1
$$ 
which respects source and target morphisms. 

Given this, consider the trivial vector bundle on the set of objects $C_0$. This is nothing but an assignment
$$
  I : C_0 \to Vect_k
$$
of the [[ground field]] $k$ to each element of $C_0$. There are two different ways to pull this vector bundle on objects back to a vector bundle on morphisms, once along the source, once along the target map. 

Then notice that the set of natural transformations between these two vector bundles
$$
  Hom_{[Sets,Vect_k]}(s^* I , t^* I)
$$
whose elements are 2-arrows of the form
$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }
$$
are canonically in bijection with $k$-calued functions on $C_1$, hence with the vector space spanned by $C_1$, hence with the vector space underlying the category algebra
$$
  Hom_{[Sets,Vect_k]}(s^* I , t^* I)
  \simeq
  k[C]
  \,.
$$

The algebra structure on $k[C]$ is similarly encoded in the diagrammatics: given two elements
$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }

  \;\;\;\; 
  and
  \;\;\;\;

  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{g}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }
$$
their pre-composite is the diagram
$$
  \array{
     &&&&
     C_1 \times_{t,s} C_1
     \\
     &&& \swarrow && \searrow
     \\
     && C_1
     &&&& C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
      && {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     &&\stackrel{g}{\Rightarrow}&&
     C_0
     \\
     & \searrow &&& 
     \downarrow &&& \swarrow
     \\
     && \to &&Vect_k&& \leftarrow  
  }
  \,.
$$

This is a composite transformation between three trivial vector bundles on the set $C_1 \times_{t,s} C_1$ of composable morphisms in $C$. As such, it is a function, which on the element consisting of the composable pair $\stackrel{r}{\to}\stackrel{s}{\to}$ takes the value $f(r)\cdot g(s)$.

In order to get back a transformation between vector bundles on $C_1$, hence a transformation between vector bundles on $C_1$, we _push forward_ along the composition map $comp: C_1 \times_{t,s} C_1 \to C_1$. This just means that we add up the values on the fibers of this map.

The result is the [[convolution product]]
$$
  (f\star g) : t \mapsto \sum_{s\circ r = t}
  f(r)\cdot g(s)
  \,.
$$
This is indeed the product in the category algebra.

Looking at category algebras realizes them as a puny special case of a bigger story which involves [[bi-brane]]s as morphisms between $n$-bundles/$(n-1)$-gerbes which live on spaces connected by correspondence spaces. This is related to a bunch of things,  such as T-duality, Fourier-Mukai transformations and other issues of quantization. A description of this perspective is in

* [[schreiber:Nonabelian cocycles and their quantum symmetries]].

This is related to observations such as described here:


* [[John Baez]], [_Quantization and Cohomology (Week 17)_](http://golem.ph.utexas.edu/category/2007/03/quantization_and_cohomology_we_16.html)

* Urs Schreiber, [_QFT of Charged n-Particle: T-Duality_](http://golem.ph.utexas.edu/category/2007/02/qft_of_charged_nparticle_tdual.html)


## Examples

### Basic examples

+-- {: .num_example}
###### Example

The convolution algebra of a [[set]]/[[manifold]] $X$ regarded as a [[discrete groupoid]]/[[Lie groupoid]] with only [[identity]] [[morphisms]] is the ordinary [[function algebra]] of $X$.

=--

+-- {: .num_example}
###### Example

For $X$ a [[set]] the convolution algebra of the [[pair groupoid]] $Pair(X)_\bullet$ is the [[matrix algebra]] of ${\vert X\vert} \times {\vert X\vert}$ matrices.

=--

+-- {: .num_example}
###### Example

For $X$ a [[smooth manifold]] and $Pair(X)_\bullet$ its [[pair groupoid]] regarded as a [[Lie groupoid]] its smooth convolution algebra is the algebra of [[smoothing kernels]] on $X$.

=--

+-- {: .num_example}
###### Example

$\mathcal{C} = \mathbf{B}G$ is the [[delooping]] [[groupoid]] of a [[discrete group]] $G$ (the groupoid with a single object and $G$ as its set of morphisms), then def. \ref{CategoryAlgebra} reduces to that of the [[group algebra]] of $G$: 
$$
  R[\mathbf{B}G] \simeq R[G]
  \,.
$$

=--

### Incidence algebras (poset convolution algebras)

See at [[Möbius inversion#IncidenceAlgebrasZetaFn]].

### Higher groupoid convolution algebras and n-vector spaces/n-modules
 {#HigherGroupoidConvolutionAlgebras}

> under construction

We discuss here a natural generalization of the notion of [[groupoid convolution algebras]] to [[higher algebra|higher algebras]] for [[n-groupoid|higher groupoids]]. 

There may be several sensible such generalizations. The one discussed now follows the principle of iterated [[internalization]] and naturally matches to the concept of [[n-modules]] ([[n-vector spaces]]) as they appear in [[extended prequantum field theory]].

In order to disentangle conceptual from technical aspects, we first discuss [[discrete ∞-groupoid|geometrically discrete higher groupoids]]. The results of this discussion then in particular help to suggest what the right definition of "higher Lie groupoid" in the context of higher convolution algebras should be in the first place.

The considerations are based on the following

+-- {: .num_remark}
###### Remark

By the discussion at _[[2-module]]_ we may think of the [[2-category]] $k Alg_b$ of $k$-[[associative algebras]] and [[bimodules]] between them as a model for the 2-category [[2Mod]] of $k$-[[2-modules]] that admit a 2-[[basis]] ([[2-vector spaces]]). Hence the groupoid convolution algebra constructiuon is a 2-functor 

$$
  C \;\colon\; Grpd \to 2 Mod
  \,.
$$


There is then the following systematic refinement of this to higher groupoids and higher algebra: by the discussion at _[[n-module]]_, 3-modules are algebra objects in [[2Mod]] and maps between them are [[bimodule]] objects in there. An algebra object in  $k Alg_b$ is equivalently a [[sesquialgebra]], an algebra equipped with a second algebra structure up to coherent homotopy, that is exhibited by structure bimodules. 

Special cases of this are [[bialgebras]], for which these structure bimodules come from actual algebra homomorphisms. Examples of these in turn are [[Hopf algebras]]. These we naturally re-discover as special higher groupoid convolution higher algebras in example \ref{DoubleGroupoid2AlgebraOfDeloopingOfFiniteGroup} below. 

=--


This iterated internalization on the codomain of the groupoid convolution algebra functor has a natural analog on its domain: a 2-groupoid we may present by a [[double groupoid]], namely a [[groupoid object in an (∞,1)-category]] in [[Grpd]] which is 3-[[coskeleton|coskeletal]] as a [[simplicial object]] in [[Grpd]].

+-- {: .num_remark}
###### Remark

Given a [[groupoid object in an (∞,1)-category|groupoid object]] $\mathcal{G}_\bullet$ in the [[(2,1)-topos]] [[Grpd]] hence a [[double groupoid]], applying the groupoid convolution algebra $(2,1)$-functor $C$ to the corresponding [[simplicial object]] $\mathcal{G}_\bullet \in Grpd^{\Delta^{op}}$ yields:

* groupoid convolution algebras $C(\mathcal{G}_0)$ and $C(\mathcal{G}_1)$,

* a $C(\mathcal{G}_1) \otimes_{C(\mathcal{G}_{0,1})} C(\mathcal{G}_1)-C(\mathcal{G}_{0})$-bimodule, assigned to the [[composition]] functor $\partial_1 \colon \mathcal{G}_1 \underset{\mathcal{G}_0}{\times} \mathcal{G}_1 \to \mathcal{G}_1$.

Under the 2-functoriality of $C$, the [[Segal conditions]] satisfied by $\mathcal{G}_\bullet$ make this bimodule exhibit a [[sesquialgebra]] structure over $C(\mathcal{G}_{0,1})$.

This sesquialgebra we call the the **double groupoid convolution 2-algebra** of $\mathcal{G}_\bullet$.

(Here we make invariant sense of the [[tensor product]] by evaluating on a [[Reedy model structure|Reedy fibrant]] representative.)

=--

+-- {: .num_example #DoubleGroupoid2AlgebraOfDeloopingOfFiniteGroup}
###### Example

Let $G$ be a [[finite group]]. Write $\mathbf{B}G$ for its [[delooping]] [[groupoid]] (the connected groupoid with $\pi_1 = G$). Since this is just a [[1-groupoid]], there are two natural ways to present $\mathbf{B}G$ as a [[double groupoid]]:

1. $\underset{\longrightarrow}{\lim}(\cdots \mathbf{B}G\stackrel{\to}{\stackrel{\to}{\to}} \mathbf{B}G \stackrel{\overset{id}{\to}}{\underset{id}{\to}} \mathbf{B}G) \simeq \mathbf{B}G$;

1. $\underset{\longrightarrow}{\lim}(\cdots G \times G \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} *) \simeq \mathbf{B}G$.

(The first is "vertically constant", the second is "horizontally constant").

Applying the [[groupoid convolution algebra]] functor to the first presentation yields the groupoid convolution algebra $C(\mathbf{B}G)$ equipped with a trivial multiplication bimodule, hence just the group convolution algebra $C(\mathbf{B}G) \simeq C_{conv}(G)$.

Applying however the groupoid convolution algebra functor to the second presentation yields the _commutative_ algebra of functions $C(G)$ equipped with the multiplication bimodule which is $C(G \times G)$ regarded as a $(C(G\times G), C(G))$-bimdodule, where the right action is induced by pullback along the group product map $G \times G \to G$.

This bimodule is in the image of the functor $Alg \to Alg_b$ that sends algebra homomorphisms to their induced bimodules, by sending $f \colon A \to B$ to $A$ regarded as an $(A,B)$-bimodule with the canonical left action on itself and the right action induced by $f$. Namely this bimdoule correspondonds to the map

$$
  \Delta \colon C(G) \to C(G \times G) \simeq C(G) \otimes C(G)
$$

given on $\phi \in C(G)$ and $g_1, g_2 \in G$ by

$$
  \Delta \phi \colon (g_1, g_2) \mapsto \phi(g_1 \cdot g_2)
  \,.
$$

This is that standard [[coalgebra|coproduct]] on the standard dual [[Hopf algebra]] associated with $G$.

In summary this means that (for $G$ a finite group):

1. If we regard $\mathbf{B}G$ as presented as a  double groupoid constant on $\mathbf{B}G$, then the corresponding groupoid convolution [[sesquialgebra]] (basis for a [[n-module|3-module]]) is the convolution algebra of $G$;

1. If instead we regard $\mathbf{B}G$ as presented as the double groupoid which is degreewise constant as a groupoid, then the corresponding groupoid convolution sesquialgebra is the standard ("dual") [[Hopf algebra]]  structure on the commutative pointwise product algebra of functions on $G$.

=--




## Properties

### Relation to (twisted) K-theory
 {#RelationToTwistedKTheory}

The [[operator K-theory]] of the convolution $C^\ast$-algebra of a [[topological groupoid]] $\mathcal{X}_\bullet$ may be thought of as the [[topological K-theory]] of the corresponding [[topological stack]]. More generally, for $\mathcal{X} \to \mathbf{B}^2 U(1)$ a [[principal 2-bundle]] ([[bundle gerbe]]) on the groupoid/stack, the [[operator K-theory]] of the corresponding twisted convolution algebra is the [[twisted K-theory]] of the stack.

([Tu, Xu, Laurent-Gengoux 04](#TXLG))

## Related concepts

* [[groupoid quantale]] - an analogue of groupoid ring/algebra where free abelian groups/vector spaces are replaced by free [[sup-lattice]]s

* [[noncommutative topology]], [[noncommutative geometry]]

  [[KK-theory]]

* [[bibundle]], [[bimodule]]

## References

### For partial orders

* [[Gian-Carlo Rota]], _On the foundations of combinatorial theory I: theory of M&#246;bius functions_ , Z. Wahrscheinlichkeitstheorie und Verw. Gebiete 2 (1964), 340&#8211;368.
 {#Rota64}


### For discrete geometry

* [[Alberto Ibort]], [[Miguel A. Rodriguez]], chapter 10 of: *An Introduction to Groups, Groupoids and Their Representations*, CRC Press (2021) &lbrack;[ISBN:9781032086767](https://www.routledge.com/An-Introduction-to-Groups-Groupoids-and-Their-Representations/Ibort-Rodriguez/p/book/9781032086767?srsltid=AfmBOoqc0EH7Qjc1_0C-TYQtUbhTWpdb3Juy61vwE9TfRC5oaJwjlYfN), [doi:10.1201/b22019](https://doi.org/10.1201/b22019)&rbrack;




The [[homotopy colimit]]-interpretation of category algebras over discrete categories is discussed in

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ ([arXiv](http://arxiv.org/abs/0905.0731))
 {#FHLT}

Groupoid algebras of geometrically discrete groupoids twisted by [[principal 2-bundles]]/[[bundle gerbes]]/[[central extension of groupoids|groupoid central extension]] is reviewed in

* Eitan Angel, _A Geometric Construction of Cyclic Cocycles on Twisted Convolution Algebras_, PhD thesis (2010)

  Cyclic cocycles on twisted convolution algebras, ([arXiv.1103.0578](http://arxiv.org/abs/1103.0578)) 




### For continuous/smooth geometry
 {#ReferencesForSmoothGeometry}


#### Convolution $C^\ast$-algebras

The study of convolution [[C-star algebras]] of [[Lie groupoids]] goes back to

* {#Renault80} [[Jean Renault]]: *A groupoid approach to $C^\ast$ algebras*, Springer Lecture Notes in Mathematics **793**, Springer (1980) &lbrack;[doi:10.1007/BFb0091072](https://doi.org/10.1007/BFb0091072)&rbrack;
 
where the [[integration]] is performed against a fixed [[Haar measure]].

Surveys:

* [[Nigel Higson]]: *Groupoids, $C^\ast$-algebras and Index theory*, lecture notes (2014) &lbrack;[[Higson-GroupoidCStarAlgebras.pdf:file]]&rbrack;

* [[Planet Math]]: _[groupoid $C^\ast$-convolution algebras](http://planetmath.org/groupoidcconvolutionalgebras)_


The construction via [[sections]] of [[bundles]] of [[half-densities]] (avoiding a choice of Haar measure) is due to

* {#Connes82} [[Alain Connes]], _A survey of foliations and operator algebras_, Proc. Sympos. Pure Math., AMS Providence, 32 (1982), 521&#8211;628
 
Review:

* {#Connes94} [[Alain Connes]], p. 106: _[[Noncommutative Geometry]]_, Academic Press, San Diego, CA, (1994)
 
Groupoid algebras as [[strict deformation quantization]] of [[Lie-Poisson structures]] given by [[Lie algebroids]]:

* [[Nicolaas P. Landsman]], B. Ramazan, *Quantization of Poisson algebras associated to Lie algebroids*, in: *Groupoids in Analysis, Geometry, and Physics*, Contemporary Mathematics **282** (2001) &lbrack;[arXiv:math-ph/0001005](https://arxiv.org/abs/math-ph/0001005), [ams:conm/282](http://www.ams.org/books/conm/282)&rbrack;

  > (specifically [[Weyl algebras]] induced from [[tangent Lie algebroids]] in Ex. 11.3)


Specifically of [[symplectic groupoids]] in the context of [[geometric quantization of symplectic groupoids]]

* {#EH} [[Eli Hawkins]], _A groupoid approach to quantization_ ([arXiv:math.SG/0612363](http://arxiv.org/abs/math.SG/0612363))
 



See also:

* {#Nuiten13} [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis, August 2013


More along these lines is in

* [[Paul Muhly]], Dana P. Williams, _Continuous trace groupoid $C^\ast$-algebras II_  Math. Scand. 70 (1992), no. 1, 127&#8211;145; MR 93i:46117). ([pdf](http://www.math.dartmouth.edu/~dana/dpwpdfs/muhwil-ms90.pdf))

* [[Paul Muhly]], [[Jean Renault]], Dana P. Williams, _Continuous trace groupoid $C^\ast$-algebras III_ , Transactions of the AMS, vol 348, Number 9 (1996) ([jstor]( http://www.jstor.org/stable/2155247))

* M&#259;d&#259;lina Roxana Buneci, _Groupoid Representations,_ Ed. Mirton: Timishoara (2003). 

*  M&#259;d&#259;lina Roxana Buneci, _Groupoid $C^\ast$-Algebras_, Surveys in Mathematics and its Applications, Volume 1: 71&#8211;98. ([pdf](http://www.utgjiu.ro/math/mbuneci/preprint/p0024.pdf))

* M&#259;d&#259;lina Roxana Buneci, _Convolution algebras for topological groupoids with locally compact fibers_ (2011) ([pdf](http://journals.bg.agh.edu.pl/OPUSCULA/31-2/31-2-02.pdf))

A review in the context of [[geometric quantization]] is in section 4.3 of 

* {#Bos} [[Rogier Bos]], _Groupoids in geometric quantization_ PhD Thesis (2007) [pdf](http://www.math.ist.utl.pt/~rbos/ProefschriftA4.pdf)
 

Specifically the convolution $C^\ast$-algebras of [[bundle gerbes]] regarded as [[centrally extended groupoids]] (algebras whose [[modules]] (see [below](#ReferencesModulesOverConvolutionAlgebra)) are [[gerbe modules]]/[[twisted bundle]]) is discussed in section 5 of 

* [[Alan Carey]], Stuart Johnson, [[Michael Murray]], _Holonomy on D-Branes_, J. Geom. Phys. 52 (2004) 186-216 ([arXiv:hep-th/0204199](http://arxiv.org/abs/hep-th/0204199))

  

Functoriality of the construction of $C^\ast$-convolution algebras (its extension to groupoid-[[bibundles]]) is discussed in 

* {#MuhleReaultWilliams87} [[Paul Muhly]], [[Jean Renault]], D. Williams, _Equivalence and isomorphism for groupoid $C^\ast$-algebras_, J. Operator Theory 17 (1987), no. 1, 3&#8211;22.
 

* {#Mrcun99} [[Janez Mrčun]], _Functoriality of the bimodule associated to a Hilsum-Skandalis map_. K-Theory 18 (1999) 235&#8211;253.
 

* {#Landsman00} [[Klaas Landsman]], _The Muhly-Renault-Williams theorem for Lie groupoids and its classical counterpart_, Lett. Math. Phys. 54 (2000), no. 1, 43&#8211;59. ([arXiv:math-ph/0008005](http://arxiv.org/abs/math-ph/0008005))
 

* [[Klaas Landsman]], _Operator Algebras and Poisson Manifolds Associated to Groupoids_, Commun. Math. Phys. 222, 97 &#8211; 116 (2001) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.7.2716))


#### Convolution Hopf algebroids
 {#ReferencesConvolutionHopfAlgebroids}

A characterization of the convolution algebras of [[étale groupoids]] with their [[Hopf algebroid]] structure is in

* [[Janez Mrčun]], _On spectral representation of coalgebras and Hopf algebroids_ ([arXiv:math/0208199](http://arxiv.org/abs/math/0208199))  

* {#KalisnikMrcun} [[Jure Kališnik]], [[Janez Mrčun]], _Equivalence between the Morita categories of etale Lie groupoids and of locally grouplike Hopf algebroids_ ([arXiv:math/0703374](http://arxiv.org/abs/math/0703374))
 

#### Modules over Lie groupoid convolution algebras and K-theory
 {#ReferencesModulesOverConvolutionAlgebra}

Discussion of [[modules]] over Lie groupoid convolution algebras is in the following articles.

In ([Renault80](#Renault80)) [[measurable space|measurable]] representations of topological groupoids are related to modules over their $L^1$ convolution [[star algebra]] [[Banach algebras]] hence over their envoloping $C^\ast$-algebras. 

In ([Bos, chapter 7](#Bos)) is discussion refining this to continuous representations and representation of a convolution $C^\ast$-algebra, also in section 4 of:

* [[Rogier Bos]], _Continuous representations of groupoids_ ([arXiv:math/0612639](http://arxiv.org/abs/math/0612639))

Representation of convolution algebras of [[étale groupoids]] is in

* [[Jure Kališnik]], _Groupoid representations and modules over the convolution algebras_ ([arXiv:0806.1832](http://arxiv.org/abs/0806.1832))

The [[operator K-theory]] of groupoid convolution algebras (the [[topological K-theory]] of the corresponding [[differentiable stacks]]) is discussed in

* {#TXLG} [[Jean-Louis Tu]], [[Ping Xu]], [[Camille Laurent-Gengoux]], _Twisted K-theory of differentiable stacks_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure (2004) Volume: 37, Issue: 6, page 841-910 ([arXiv:math/0306138](http://arxiv.org/abs/math/0306138))
 

Construction of cocycles in [[KK-theory]] and [[spectral triples]] from groupoid convolution is in 

* {#Meland} Bram Mesland, _Groupoid cocycles and K-theory_ ([arXiv:1005.3677](http://arxiv.org/abs/1005.3677))
 




[[!include quantum observables as groupoid convolution -- references]]




[[!redirects category algebras]]
[[!redirects groupoid algebra]]
[[!redirects groupoid algebras]]

[[!redirects incidence algebra]]
[[!redirects incidence algebras]]

[[!redirects groupoid convolution algebra]]
[[!redirects groupoid convolution algebras]]

[[!redirects convolution algebra of a Lie groupoid]]
[[!redirects convolution algebras of a Lie groupoid]]

[[!redirects convolution algebra of Lie groupoids]]
[[!redirects convolution algebras of Lie groupoids]]

[[!redirects Lie groupoid convolution algebra]]
[[!redirects Lie groupoid convolution algebras]]

[[!redirects category convolution algebra]]
[[!redirects category convolution algebras]]

[[!redirects twisted groupoid algebra]]
[[!redirects twisted groupoid algebras]]

[[!redirects twisted groupoid convolution algebra]]
[[!redirects twisted groupoid convolution algebras]]

[[!redirects groupoid convolution C*-algebra]]
[[!redirects groupoid convolution C*-algebras]]
[[!redirects groupoid convolution C-star-algebra]]
[[!redirects groupoid convolution C-star-algebras]]

[[!redirects groupoid convolution product]]
[[!redirects groupoid convolution products]]
