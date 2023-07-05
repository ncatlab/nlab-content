
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A natural [[tensor product]] of [[chain complexes]] that makes the [[category of chain complexes]] into a [[closed monoidal category]].

## Definition

Let $R$ be a [[commutative ring]] and $\mathcal{A} = R$[[Mod]] the [[category]] of [[modules]] over $R$. Write $Ch_\bullet(\mathcal{A})$ for the [[category of chain complexes]] of $R$-modules. 


+-- {: .num_defn #TheTensorProdComplex}
###### Definition

For $X, Y \in Ch_\bullet(\mathcal{A})$ write  $(X \otimes Y)_\bullet \in Ch_\bullet(\mathcal{A})$ for the [[chain complex]] whose component in degree $n$ is given by the [[direct sum]]

$$
  (X \otimes Y)_n \coloneqq \oplus_{i + j = n} X_i \otimes_R Y_j
$$

over all tensor products of components whose degrees sum to $n$,
and whose [[differential]] is given on elements $(x,y)$ of homogeneous degree by

$$
  \partial^{X \otimes Y} (x, y) = (\partial^X x, y) + 
  (-1)^{deg(x)} (x, \partial^Y y)
  \,.
$$

Its unit $1_{Ch}$ is $R$ considered as a chain complex concentrated in degree 0.

=--


## Properties

### As a total complex of a double complex

The tensor product of chain complexes is equivalently the [[total complex]] of the [[double complex]] which is the objectwise tensor product:

+-- {: .num_defn #DoubleComplexTensor}
###### Definition

For $X, Y \in Ch_\bullet(\mathcal{A})$ write  $X_\bullet \otimes Y_\bullet \in Ch_\bullet(Ch_\bullet(\mathcal{A}))$ for the [[double complex]] whose component in degree $(n_1, n_2)$ is given by the [[tensor product]]

$$
  X_{n_1} \otimes Y_{n_2} \in \mathcal{A}
$$

whose horizontal differential is $\partial^{hor} \coloneqq \partial^X \otimes id_Y$ and whose vertical differential is $\partial^{vert} \coloneqq id_{X} \otimes \partial^Y$.

=--

+-- {: .num_prop #AsTotalComplex}
###### Proposition

The tensor product of chain complexes, def. \ref{TheTensorProdComplex} is isomorphic to the [[total complex]] of the [[double complex]] of def. \ref{DoubleComplexTensor}:

$$
  Tot_\bullet (X_\bullet \otimes Y_\bullet)
  \simeq
  (X \otimes Y)_\bullet
  \,.
$$

=--

+-- {: .proof}
###### Proof

By direct unwinding of the definitions.

=--


### As Day convolution

The following section is copied form an answer by [[Alexander Campbell]]
on [MathOverflow](https://mathoverflow.net/revisions/359316/6).

The tensor product of chain complexes is a [[Day convolution]] product. The important thing to note is that, to define a [[Day convolution]] [[monoidal structure]] on the $\mathcal{V}$-[[enriched functor]] category $[\mathcal{C},\mathcal{V}]$ (where $\mathcal{V}$ is a complete and cocomplete [[symmetric monoidal closed category]], e.g. $\mathbf{Ab}$), we needn't demand $\mathcal{C}$ to be a monoidal $\mathcal{V}$-category: it suffices for $\mathcal{C}$ to be a **[[promonoidal]]** $\mathcal{V}$-category. This is the generality at which [[Day convolution]] was originally defined in [Day's thesis](http://web.science.mq.edu.au/~street/DayPhD.pdf) (see also [his earlier paper in the Reports of the Midwest Category Seminar IV](https://web.math.rochester.edu/people/faculty/doug/otherpapers/DayReport.pdf), where the word "premonoidal" was used).

A [[promonoidal structure]] on a small $\mathcal{V}$-category $\mathcal{C}$ consists of tensor product and unit "[[profunctors]]", i.e. $\mathcal{V}$-functors $P \colon \mathcal{C}^\mathrm{op}\times\mathcal{C}^\mathrm{op} \times \mathcal{C} \to \mathcal{V}$ and $J \colon \mathcal{C} \to \mathcal{V}$, together with associativity and unit constraints subject to the usual two 
"[[pentagon]]" and "triangle" axioms. Given a [[promonoidal structure]] on $\mathcal{C}$, we may construct the **[[Day convolution]]** [[monoidal structure]] on $[\mathcal{C},\mathcal{V}]$, whose tensor product is given at a pair of $\mathcal{V}$-functors $F,G \in [\mathcal{C},\mathcal{V}]$ by the coend
$$F\ast G = \int^{A,B \in \mathcal{C}} P(A,B;-) \otimes FA \otimes GB$$
in $\mathcal{V}$, 
and whose unit object is the $\mathcal{V}$-functor $J \in [\mathcal{C},\mathcal{V}]$, and so on. This [[monoidal structure]] on $[\mathcal{C},\mathcal{V}]$ is biclosed (i.e., the tensor product $\mathcal{V}$-functor has a right $\mathcal{V}$-adjoint -- equivalently, preserves (weighted) [[colimits]] -- in each variable). In fact, every [[biclosed monoidal structure]] on $[\mathcal{C},\mathcal{V}]$ arises in this way from some [[promonoidal structure]] on $\mathcal{C}$. (For instance, one recovers the $\mathcal{V}$-functor $P$ from the tensor product $\ast$ by $P(A,B;C) = (\mathcal{C}(A,-) \ast \mathcal{C}(B,-))C$.)

So, since the $\mathbf{Ab}$-category $\mathbf{Ch}$ of chain complexes is (equivalent to) an $\mathbf{Ab}$-[[enriched functor]] category $[\mathcal{C},\mathbf{Ab}]$ (for the $\mathbf{Ab}$-category $\mathcal{C}$ described in the question to which you linked), and since the standard [[monoidal structure]] on $\mathbf{Ch}$ is $\mathbf{Ab}$-enriched and biclosed, this [[monoidal structure]] must be the [[Day convolution]] [[monoidal structure]] for some [[promonoidal]] structure on $\mathcal{C}$. And it isn't too hard to describe that [[promonoidal]] structure. For instance, (presuming I haven't bungled the calculation) the functor $P$ is defined on objects by 

$$
P(i,j;k) = \begin{cases}
\mathbb{Z}  & \mathrm{if } \, i+j=k, \\
\mathbb{Z} \oplus \mathbb{Z} &  \mathrm{if } \, i+j=k+1, \\
\mathbb{Z} &  \mathrm{if } \, i+j=k+2, \\
0 & \mathrm{else}.
\end{cases} 
$$

### Canonical Forgetful Functor
 {#CanonicalForgetfulFunctor}

Every $\mathcal{V}$-[[enriched monoidal category]] $(\mathcal{C}, \otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ has a canonical [[forgetful functor]] 

$$
  U_{\mathcal{C}} 
  \;\coloneqq\; 
  \mathcal{C}(1_{\mathcal{C}},-) 
  \;\colon\; 
  \mathcal{C} \longrightarrow \mathcal{V}
$$

given by forming [[hom-objects]] out of the [[tensor unit]]. 

This functor is automatically [[lax monoidal functor|lax monoidal]] and if $\mathcal{C}$ is [[closed monoidal category|closed monoidal]] with [[internal hom]] $[-,-]_{\mathcal{C}}$ then we further have $U_{\mathcal{C}}[-,-]_{\mathcal{C}} \cong \mathcal{C}(-,-)$. This functor is particularly important to the theory of enriched categories.

+-- {: .num_prop #CanonicalForgetfulFunctor} 
###### Proposition

$U_{Ch} \colon Ch_\bullet(R) \longrightarrow R\text{Mod}$ takes a chain complex to its [[cycles]]/closed elements of degree 0.

=--

\begin{proof}
  Since the [[tensor unit]] $I \,\in\, Ch_\bullet(R)$ is the chain complex concentrated on $R$ in degree 0, hence with all [[differentials]] being 0, a [[chain map]] out of $I$  

1. is fixed by its value on $1 \in R$ (by $R$-[[linear map|linearity]]) 

1. must take values in elements of degree 0 whose differential also vanishes (by the chain map property).

\end{proof}

\begin{remark}
In particular $U_{Ch}$ does not simply take a chain complex to its term at degree 0. That would of course give a different forgetful functor.
\end{remark}

## Examples

### Square as tensor product of interval with itself
 {#SquareAsIntervalSquared}

+-- {: .num_example }
###### Example


For $R$ some [[ring]], let $I_\bullet \in Ch_\bullet(R Mod)$ be the chain complex given by

$$
  I_\bullet =
  \left[
     \cdots \to 0 \to 0 \to R \stackrel{\partial^{I}_0}{\to} R \oplus R
  \right]
  \,,
$$

where $\partial^I_0 = (-id, id)$. 

This is the [[normalized chain complex]] of the [[chain on a simplicial set|simplicial chain complex]] of the standard simplicial interval, the 1-[[simplex]] $\Delta_1$, as follows: we may think of 

$$
 I_0 = R \oplus R \simeq R[ \{(0), (1)\} ]
$$

as the $R$-[[linear span]] of two [[basis]] elements labelled "$(0)$" and "$(1)$", to be thought of as the two 0-[[chain on a simplicial set|chains]] on the endpoints of the interval. Similarly we may think of

$$
  I_1 = R \simeq R[\{(0 \to 1)\}]
$$

as the free $R$-module on the single basis element which is the unique non-degenerate 1-[[simplex]] $(0 \to 1)$ in $\Delta^1$.

Accordingly, the [[differential]] $\partial^I_0$ is the oriented [[boundary]] map of the interval, taking this basis element to

$$
  \partial^I_0 : (0 \to 1) \mapsto (1) - (0) 
$$

and hence a general element $r\cdot(0 \to 1)$ for some $r \in R$ to 

$$
  \partial^I_0 : r\cdot(0 \to 1) \mapsto r\cdot (1) - r\cdot(0) 
  \,.
$$

We now write out in full details the tensor product of chain complexes of $I_\bullet$ with itself, according to def. \ref{TheTensorProdComplex}:

$$
  S_\bullet \coloneqq I_\bullet \otimes I_\bullet
  \,.
$$

By definition and using the above choice of [[basis]] element, this is in low degree given as follows:

$$
  \begin{aligned}
    S_0 
    &=  
    I_0 \otimes I_0 
    \\
    & =
    (R \oplus R) \otimes (R \oplus R)
    \\
    & \simeq R \oplus R \oplus R \oplus R
    \\
    & = 
    \left\{
       r_{00} \cdot ((0),(0)')
       +
       r_{01} \cdot ((0),(1)')
       +
       r_{10} \cdot ((1),(0)')
       +
       r_{11} \cdot ((1),(1)')
       |
       r_{\cdot, \cdot} \in R
    \right\}
  \end{aligned}
  \,,
$$

where in the last line we express a general element as a linear combination of the canonical basis elements which are obtained as tensor products $(a,b) \in R\otimes R$ of the previous basis elements. Notice that by the definition of [[tensor product of modules]] we have relations like

$$
  r ( (0), (1)') = (r(0), (1)') = ((0), r(1)')
$$

etc. 

Similarly then, in degree-1 the tensor product chain complex is

$$
  \begin{aligned}
     (I \otimes I)_1 
     & =
     (I_0 \otimes I_1) \oplus (I_1 \otimes I_0)
     \\
     & \simeq
     R \otimes (R \oplus R) \oplus (R \oplus R) \otimes R
     \\
     & \simeq
     R \oplus R \oplus R \oplus R
     \\
     & \simeq
     \left\{
       r_{0} \cdot ((0),(0\to 1)')
       + 
       r_{1} \cdot ((1), (0 \to 1)')
       + 
       \bar r_0 \cdot ((0\to 1), (0)')
       +
       \bar r_1 \cdot ((0 \to 1), (1)')
       |
       r_{\cdot}, \bar r_{\cdot} \in R
     \right\}
  \end{aligned}
  \,.
$$

And finally in degree 2 it is 

$$
  \begin{aligned}
     (I \otimes I)_2
     & \simeq
     I_1 \otimes I_1
     \\
     & \simeq
     R \otimes R
     \\
     & \simeq R
     \\
     & \simeq
     \left\{
       r\cdot ((0 \to 1), (0 \to 1)')
       |
       r \in R
     \right\}
  \end{aligned}
  \,.
$$

All other contributions that are potentially present in $(I \otimes I)_\bullet$ vanish (are the [[trivial group|0-module]]) because all higher terms in $I_\bullet$ are.

The tensor product basis elements appearing in the above expressions have a clear [[geometry|geometric]] interpretation: we can label a square with them as follows

$$
  \array{
     ((0),(1)')
     &&\underset{((0\to 1),(0))}{\to}&&
     ((1),(1)')
     \\
     \\
     {}^{\mathllap{((0),(0\to 1)')}}\uparrow 
     &&\righttoleftarrow^{((0 \to 1), (0\to 1)')}&& 
     \uparrow^{\mathrlap{((1),(0 \to 1)')}}
     \\
     \\
     ((0),(0)')
     &&\underset{((0\to 1),(0)')}{\to}&&
     ((1),(0)')
  }
  \,.
$$

This diagram indicates a [[cellular complex|cellular]] square and identifies its canonical [[singular chains]] with the elements of $(I \otimes I)_\bullet$. The arrows indicate the orientation. For instance the fact that

$$
  \begin{aligned}
    \partial^{I \otimes I} ((0 \to 1), (0)')
    & =
    (\partial^I (0 \to 1), (0)')
    + (-1)^1
    ((0\to 1), \partial^I (0))
    \\
    & = 
    ( (1) - (0), \;(0)' )
    - 0
    \\
    & = 
    ((1), (0)') - ((0), (0)')
  \end{aligned} 
$$

says that the oriented [[boundary]] of the bottom morphism is the bottom right element (its target) minus the bottom left element (its source), as indicated. Here we used that the differential of a degree-0 element in $I_\bullet$ is 0, and hence so is any tensor product with it.

Similarly the oriented boundary of the square itself is computed to

$$
  \begin{aligned}
    \partial^{I \otimes I} ((0 \to 1), (0 \to 1)')
    &=
    (\partial^I (0 \to 1), (0 \to 1)')
    - 
    ((0 \to 1), \partial^I(0 \to 1))
    \\
    & = 
    ((1)- (0), (0 \to 1)')
    -
    ((0 \to 1), (1)' - (0)')
    \\
    & = 
    ((1), (0 \to 1)')
    -
    ((0), (0 \to 1)')
    -
    ((0 \to 1), (1)')
    +
    ((0 \to 1), (0)')
  \end{aligned}
  \,,
$$

which can be read as saying that the boundary is the evident boundary thought of as oriented by drawing it _counterclockwise_ into the plane, so that the right arrow (which points up) contributes with a +1 prefactor, while the left arrow (which also points up) contributes with a -1 prefactor.


=--

### Singular chain complex

For $X,Y \in $ [[Top]] two [[topological spaces]], the [[Eilenberg-Zilber theorem]] asserts a [[quasi-isomorphism]]

$$
  C_\bullet(X \times Y)
  \to
  (C(X) \otimes C(Y))_\bullet
$$

between the [[singular chain complex]] of the [[product topological space]] and the tensor product of chain complexes of the separate singular chain complexes.

### Filtering and spectral sequences

As for any [[total complex]] of a double complex, the tensor product of chain complexes is naturally a [[filtered chain complex]], either by the degree of the first of by that of the second chain complex factor.

+-- {: .num_prop }
###### Proposition

Let $R$ be a [[commutative ring]]. For $A, B \in R$[[Mod]], the two ways of computing the [[Tor]] [[left derived functor]] coincide

$$
  (L_n ((-)\otimes_R B))(A) \simeq (L_n (A \otimes_R (-)))(B)
$$

and hence we can consistently write $Tor_n(A,B)$ for either.

=--

+-- {: .proof}
###### Proof

Let $Q^A_\bullet \stackrel{\simeq_{qi}}{\to} A$ and $Q^B_\bullet \stackrel{\simeq_{qi}}{\to} B$ be [[projective resolutions]] of $A$ and $B$, respectively. The corresponding [[tensor product of chain complexes]] 
$Tot (Q^A_\bullet\otimes Q^B_\bullet)$, hence by prop. \ref{AsTotalComplex} the [[total complex]] of the degreewise [[tensor product of modules]] [[double complex]] carries the [[filtered chain complex|filtration]] by horizontal degree as well as that by vertical degree.

Accordingly there are the corresponding two [[spectral sequences of a double complex]], to be denoted here $\{{}^{A}E^r_{p,q}\}_{r,p,q}$ (for the filtering by $A$-degree) and $\{{}^{B}E^r_{p,q}\}_{r,p,q}$ (for the filtering by $B$-degree). By the discussion there, both converge to the chain homology of the total complex. 

We find the value of both spectral sequences on low degree pages according to the general discussion at _[spectral sequence of a double complex - low degree pages](spectral+sequence+of+a+double%20complex#LowDegreePages)_. 

The 0th page for both is

$$
  {}^A E^0_{p,q} = {}^B E^0_{p,q} \coloneqq Q^A_p \otimes_R Q^B_q  
  \,.
$$

For the first page we have

$$  
  \begin{aligned}
    {}^A E^1_{p,q} 
    & \simeq H_q(C_{p,\bullet}) 
    \\
    & \simeq  H_q( Q^A_p \otimes Q^B_\bullet )
  \end{aligned}
$$

and

$$  
  \begin{aligned}
    {}^B E^1_{p,q} 
    & \simeq H_q(C_{\bullet,p}) 
    \\
    & \simeq  H_q( Q^A_\bullet \otimes Q^B_p )
  \end{aligned}
  \,.
$$

Now using the [[universal coefficient theorem]] [in homology](universal%20coefficient%20theorem#InHomology) and the fact that $Q^A_\bullet$ and $Q^B_\bullet$ is a [[resolution]] by [[projective objects]], by construction, hence of tensor [[acyclic objects]] for which all [[Tor]]-modules vanish, this simplifies to

$$
  \begin{aligned}
     {}^A E^1_{p,q} 
     & \simeq Q^A_p \otimes H_q(Q^B_\bullet)
     \\
     & \simeq \left\{
       \array{
           Q^A_p \otimes_R B & if\; q = 0
           \\
           0 & otherwise
       }
     \right.
  \end{aligned}
$$

and similarly

$$
  \begin{aligned}
     {}^B E^1_{p,q} 
     & \simeq H_q(Q^A_\bullet) \otimes_R Q^B_p
     \\
     & \simeq \left\{
       \array{
           A \otimes_R Q^B_p & if\; q = 0
           \\
           0 & otherwise
       }
     \right.
  \end{aligned}
  \,.
$$

It follows for the second pages that

$$
  \begin{aligned}
    {}^A E^2_{p,q} 
    & \simeq
    H_p(H^{vert}_q(Q^A_\bullet \otimes Q^B_\bullet))
    \\
   & \simeq 
   \left\{
     \array{
     (L_p( (-)\otimes_R B ))(A) & if \; q = 0
     \\
     0 & otherwise    
     }
  \right.
  \end{aligned}
$$

and

$$
  \begin{aligned}
    {}^B E^2_{p,q} & \simeq
    H_p(H^{hor}_q(Q^A_\bullet \otimes Q^B_\bullet))
    \\
   & \simeq 
   \left\{
     \array{
       (L_p ( A \otimes_R (-) ))(B) & if \; q = 0
       \\
       0 \; otherwise
     }
   \right.
  \end{aligned}
  \,.
$$

Now both of these second pages are concentrated in a single row and hence have converged on that page already. Therefore, since they both converge to the same value:

$$
  L_p((-)\otimes_R B)(A)
  \simeq
  {}^A E^2_{p,0}
  \simeq
  {}^A E^\infty_{p,0}
  \simeq
  {}^B E^2_{p,0}
  \simeq
  L_p(A \otimes_R (-))(B)
  \,.
$$

=--

## Applications

* A [[monoid]] with respect to the tensor product of chain complexes is a [[differential graded algebra]].

## Related concepts

* [[internal hom of chain complexes]]

* [[tensor product]]

  * [[tensor product of abelian groups]]

  * [[tensor product of modules]]

## References

Textbook accounts:

* [[Charles Weibel]], Section 2.7 of: *[[An Introduction to Homological Algebra]]*, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9781139644136](https://doi.org/10.1017/CBO9781139644136), [pdf](https://web.math.rochester.edu/people/faculty/doug//otherpapers/weibel-hom.pdf)&rbrack;

[[!redirects tensor products of chain compexes]]
[[!redirects tensor product of cochain complexes]]
[[!redirects tensor products of cochain complexes]]
