
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

More generally, if the groupoid carries a [[line 2-bundle]] then (in its incarnation as a [[bundle gerbe]]-like transition bundle) the space of morphisms carries a [[line bundle]] (satisfying some compatibility conditions) and one can consider convolution algebras not just of functions, but of [[sections]] of this line bundle. The resulting algebra is called the _twisted groupoid convolution algebra_, twisted by the [[characteristic class]] of the [[line 2-bundle]].

For "bare" categories/groupoids (i.e.: [[internal category|internal]] to [[Set]]) these constructions are canonical. But under mild conditions or else when equipped some suitable extra [[stuff, structure, property|structure]], it generalizes to [[internal categories]]/[[internal groupoids]] in [[geometry|geometric]] contexts, notably in [[topology]] ([[topological groupoids]]) [[differential geometry]] ([[Lie groupoids]]) and [[algebraic geometry]]. In such geometric situations a groupoid algebra is also called a _[[Hopf algebroid]]_ and may be used to _characterize_ the geometric groupoid.

Therefore to some extent one may think of the relation between categories and their category algebras as an incarnation of the [[Isbell duality|general duality]] between [[geometry]] and [[algebra]]. Since category/groupoid algebras are generically non-commutative, this relation identifies groupoids/categories as certain spaces in [[noncommutative geometry]]. From this point of view groupoid convolution algebras have been highlighted and developed notably in ([Connes 94](#Connes094)). Due to this relation the groupoid convolution product is also referred to as a [[star product]] and denoted "$\star$".

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

then [[pullback of functions]] along this map makes is an [[involution]] of the convolution algebra of $\mathcal{C}$ and hence makes it into a [[star-algebra]]. 

More generally for $\mathcal{C}$ equipped with the structure of a [[dagger-category]], pullback along the dagger-fuctor

$$
  \dagger \colon \mathcal{C}_1 \to \mathcal{C}_1
$$

makes the convolution algebra a star-algebra.

=--

### For Lie groupoids


+-- {: .num_remark #ForLieGroupoids}
###### Remark

If $\mathcal{C}$ is a groupoid with extra [[geometry|geometric]] structure, then there are natural variants of the above definition.

Notably if $\mathcal{C}$ is a [[Lie groupoid]] then there is a variant where the functions in remark \ref{AsConvolutionAlgebra} are taken to be [[smooth functions]] and where the convolution [[sum]] is replaced by an [[integration]]. In order for this to make sense one needs to consider in fact functions with values in half-[[densities]] over the [[manifold]] $\mathcal{C}_1$.

More generally, for a [[bundle gerbe]] over a Lie groupoid $\mathcal{C}$, hence a multiplicative [[line bundle]] over $\mathcal{C}_1$, one can consider a convolution product on [[sections]] of this line bundle tensored with half-densities.

=--

See the [References -- For continuous/smooth geometry](#ReferencesForSmoothGeometry).


+-- {: .num_defn #ContinuousCategoryAlgebraWithHalfDensities}
###### Definition

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

(Here we regard the integrand naturally as taking values in actual [[densities]] tensored with the pullback of $\sqrt{Omega}$ along the composition map. This defines the [[integration]] of density-factor which then takes values in $\sqrt{\Omega}$.)

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

+-- {: .num_remark}
###### Remark

With suitable definitions, this construction constituts a [[2-functor]] from [[differentiable stacks]] to [[C-star-algebras]] and [[Hilbert bimodules]] between them, ([Muhly-Renault-Williams 87](#MuhleReaultWilliams87), [Landsman 00](#Landsman00)).

=--


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

+-- {: .num_example}
###### Example

The convolution algebra of a [[set]]/[[manifold]] $X$ regarded as a [[discrete groupoid]]/[[Lie groupoid]] with only [[identity]] [[morphisms]] is the ordinary [[function algebra]] of $X$.

=--

+-- {: .num_example}
###### Example

For $X$ a [[set]] the convolution algebra of the [[pair groupoid]] $Pair(X)_\bullet$ is the [[matrix algebra]] of ${\vert X\vert} \times {\vert X\vert}$ matrices.

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



## References

### For discrete geometry


The [[homotopy colimit]]-interpretation of category algebras over discrete categories is discussed in

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ ([arXiv](http://arxiv.org/abs/0905.0731))
 {#FHLT}

Groupoid algebras of geometrically discrete groupoids twisted by [[principal 2-bundles]]/[[bundle gerbes]]/[[central extension of groupoids|groupoid central extension]] is reviwed in

* Eitan Angel, _A Geometric Construction of Cyclic Cocycles on Twisted Convolution Algebras_, PhD thesis (2010)

  Cyclic cocycles on twisted convolution algebras, ([arXiv.1103.0578](http://arxiv.org/abs/1103.0578)) 




### For continuous/smooth geometry
 {#ReferencesForSmoothGeometry}


#### Convolution $C^\ast$-algebras

The study of convolution [[C-star algebras]] of [[Lie groupoids]] goes back to

* [[Jean Renault]], _A groupoid approach to $C^\ast$ algebras_,
Springer Lecture Notes in Mathematics, 793, Springer-Verlag, New York,
1980.
 {#Renault80}

Where the [[integration]] is performed against a fixed [[Haar measure]].
A good survey is in 

* PlanetMath, _[groupoid $C^\ast$-convolution algebras](http://planetmath.org/groupoidcconvolutionalgebras)_

The construction via [[sections]] of [[bundles]] of [[half-densities]] (avoiding a choice of Haar measure) is due to

* [[Alain Connes]], _A survey of foliations and operator algebras_, Proc. Sympos. Pure Math., AMS Providence, 32 (1982), 521&#8211;628
 {#Connes82}

A review is on page 106 of 

* [[Alain Connes]], _[[Noncommutative Geometry]]_, Academic Press, San Diego, CA, (1994)
 {#Connes94}

More along these lines is in

* [[Paul Muhly]], Dana P. Williams, _Continuous trace groupoid $C^\ast$-algebras II_  Math. Scand. 70 (1992), no. 1, 127&#8211;145; MR 93i:46117). ([pdf](http://www.math.dartmouth.edu/~dana/dpwpdfs/muhwil-ms90.pdf))

* [[Paul Muhly]], [[Jean Renault]], Dana P. Williams, _Continuous trace groupoid $C^\ast$-algebras III_ , Transactions of the AMS, vol 348, Number 9 (1996) ([jstor]( http://www.jstor.org/stable/2155247))

* M&#259;d&#259;lina Roxana Buneci, _Groupoid Representations,_ Ed. Mirton: Timishoara (2003). 

*  M&#259;d&#259;lina Roxana Buneci, _Groupoid $C^\ast$-Algebras_, Surveys in Mathematics and its Applications, Volume 1: 71&#8211;98. ([pdf](http://www.utgjiu.ro/math/mbuneci/preprint/p0024.pdf))

* M&#259;d&#259;lina Roxana Buneci, _Convolution algebras for topological groupoids with locally compact fibers_ (2011) ([pdf](http://journals.bg.agh.edu.pl/OPUSCULA/31-2/31-2-02.pdf))

A review in the context of [[geometric quantization]] is in section 4.3 of 

* [[Rogier Bos]], _Groupoids in geometric quantization_ PhD Thesis (2007) [pdf](http://www.math.ist.utl.pt/~rbos/ProefschriftA4.pdf)
 {#Bos}

Specifically the convolution $C^\ast$-algebras of [[bundle gerbes]] regarded as [[centrally extended groupoids]] (algebras whose [[modules]] (see [below](#ReferencesModulesOverConvolutionAlgebra)) are [[gerbe modules]]/[[twisted bundle]]) is discussed in section 5 of 

* [[Alan Carey]], Stuart Johnson, [[Michael Murray]], _Holonomy on D-Branes_, J. Geom. Phys. 52 (2004) 186-216 ([arXiv:hep-th/0204199](http://arxiv.org/abs/hep-th/0204199))

A discussion of convolution algebras of [[symplectic groupoids]] (in the context of [[geometric quantization of symplectic groupoids]]) is in 

* [[Eli Hawkins]], _A groupoid approach to quantization_ ([arXiv:math.SG/0612363](http://arxiv.org/abs/math.SG/0612363))
  {#EH}

That the construction of $C^\ast$-convolution algebras defines a (2-)functor from [[differentiable stacks]] to $C^\ast$-algebras with [[Hilbert bimodules]] between them is discussed in 

* [[Paul Muhly]], [[Jean Renault]], D. Williams, _Equivalence and isomorphism for groupoid $C^\ast$-algebras_, J. Operator Theory 17 (1987), no. 1, 3&#8211;22.
 {#MuhleReaultWilliams87}

* [[Klaas Landsman]], _The Muhly-Renault-Williams theorem for Lie groupoids and its classical counterpart_, Lett. Math. Phys. 54 (2000), no. 1, 43&#8211;59. ([arXiv:math-ph/0008005](http://arxiv.org/abs/math-ph/0008005))
 {#Landsman00}

#### Convolution Hopf algebroids
 {#ReferencesConvolutionHopfAlgebroids}

A characterization of the convolution algebras of [[étale groupoids]] with their [[Hopf algebroid]] structure is in

* [[Janez Mrčun]], _On spectral representation of coalgebras and Hopf algebroids_ ([arXiv:math/0208199](http://arxiv.org/abs/math/0208199))  

* [[Jure Kališnik]], [[Janez Mrčun]], _Equivalence between the Morita categories of etale Lie groupoids and of locally grouplike Hopf algebroids_ ([arXiv:math/0703374](http://arxiv.org/abs/math/0703374))

#### Modules over Lie groupoid convolution algebras
 {#ReferencesModulesOverConvolutionAlgebra}

Discussion of [[modules]] over Lie groupoid convolution algebras is in the following articles.

In ([Renault80](#Renault80)) [[measurable space|measurable]] representations of topological groupoids are related to modules over their $L^1$ convolution [[star algebra]] [[Banach algebras]] hence over their envoloping $C^\ast$-algebras. 

In ([Bos, chapter 7](#Bos)) is discussion refining this to continuous representations and representation of a convolution $C^\ast$-algebra, also in section 4 of:

* [[Rogier Bos]], _Continuous representations of groupoids_ ([arXiv:math/0612639](http://arxiv.org/abs/math/0612639))

Representation of convolution algebras of [[étale groupoids]] is in

* [[Jure Kališnik]], _Groupoid representations and modules over the convolution algebras_ ([arXiv:0806.1832](http://arxiv.org/abs/0806.1832))


[[!redirects category algebras]]
[[!redirects groupoid algebra]]
[[!redirects groupoid algebras]]

[[!redirects groupoid convolution algebra]]
[[!redirects groupoid convolution algebras]]

[[!redirects category convolution algebra]]
[[!redirects category convolution algebras]]

