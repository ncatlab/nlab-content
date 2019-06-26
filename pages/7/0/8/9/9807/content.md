
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[equivariant cohomology|equivariant]] version of [[de Rham cohomology]].

## Properties

### Models

Let 

1. $X$ be a [[smooth manifold]] with [[de Rham algebra]] denoted $\big( \Omega^\bullet(X), d_{dR} \big)$,

1. $G$ a [[Lie group]] with [[Lie algebra]] denoted $\big(\mathfrak{g}, [-,-]\big)$,

1. $X \times G \overset{\rho}{\longrightarrow} X$ a [[smooth function|smooth]] [[action]] of $G$ on $X$.



Various [[dg-algebras]] are used to model the corresponding $G$-equivariant de Rham cohomology $X$, known as 

* _[the Weil model](#TheWeilModel)_

* _[the Cartan model](#TheCartanModel)_



#### The Weil model
 {#TheWeilModel}


Let $\big( W(\mathfrak{g}), d_W \big)$ denote the [[Weil algebra]] of $\mathfrak{g}$. If $\{t_a\}$ is a [[linear basis]] for $\mathfrak{g}$ 

\[
  \label{LinearBasisForG}
  \mathfrak{g}
  \;=\;
  span\big(  \{t_a\} \big)
\]

with induced structure constants for the [[Lie bracket]] being $\big\{f_{b c}^a\big\}_{a,b,c}$ 

\[
  \label{StructureConstants}
  [t_a, t_b] \;=\; f_{a b}^c t^b \wedge t^c
\]

(using the [[Einstein summation convention]] throughout)

then the [[Weil algebra]] is the [[dgc-algebra]] explicitly given by [[generators and relations]] as follows:

\[
  \label{ExplicitWeilAlgebra}
  W(\mathfrak{g})
  \;\coloneqq\;
  \mathbb{R}\big[ 
    \{ 
      \underset
        { deg = 1 }
        {
          \underbrace{ t^a } 
        }
      \}_a,
    \{ 
      \underset
        { deg = 2 }
        {
          \underbrace{ r^a } 
        }
      \}_a
  \big]
  \Big/
  \left(
    \begin{aligned}
      d_W \, t^a & =  - \tfrac{1}{2}f^a_{b c} t^b \wedge t^c + r^a
      \\
      d_W \, r^a & = f^a_{b c} t^b \wedge r^c
    \end{aligned}
  \right)
\]

Now consider the [[tensor product of algebras|tensor product of]] [[dgc-algebras]] of the [[de Rham algebra]] of $X$ with the [[Weil algebra]] of $\mathfrak{g}$

\[
  \label{TensorProductOfdeRhamAlgebraWithWeilAlgebra}
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g}), 
    \, 
    d_{dR} + d_W
  \Big)  
  \,.
\]

On this consider the following joint [[Cartan calculus]] operations: for each fKalbasis element $t_a$ (eq:LinearBasisForG) a graded [[derivation]] of degree -1 (contraction)

\[
  \label{WeilModelContractionOperation}
  \iota_a
  \;\colon\;
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^\bullet
  \longrightarrow
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^{\bullet - 1 }
\]

and a graded derivation of degree 0 (generalized [[Lie derivative]])

\[
  \label{WeilModelLieDerivative}
  \mathcal{L}_a
  \;\colon\;
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^\bullet
  \longrightarrow
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^{\bullet}
\]

defined on $\omega \in \Omega^\bullet(X)$ any [[differential form]] and $t^a, r^a$ as in (eq:ExplicitWeilAlgebra) as follows

\[
  \label{WeilModelContractionOnGenerators}
  \iota_a \;\colon\;
  \left\{
    \begin{aligned}
      \omega & \mapsto \iota_{v^a} \omega
      \\
      t^b &\mapsto \delta^a_b
      \\
      r^b & \mapsto 0
    \end{aligned}
  \right.
\]

and

\[
  \label{WeilModelLieDerivativeOnGenerators}
  \mathcal{L}_a 
  \;\colon\;
  \left\{
    \begin{aligned}
      \omega & \mapsto \mathcal{L}_{v^a} \omega
      \\
      t^b &\mapsto f_{a c}^b t^c
      \\
      r^b & \mapsto f_{a c}^b r^c
    \end{aligned}
  \right.
\]


where 

$$
  v^a
  \;\colon\;
  X 
  \overset{
    \big( (e,t_a), 0 \big)
  }{\hookrightarrow}
  T G \times T X
  \simeq
  T ( G \times X )
  \overset{ d \rho } {\longrightarrow}
  T X
$$

is the [[vector field]] on $X$ which is the [[derivative]] of the [[action]] $\rho$ of $G$ along the [[Lie algebra]]-element $t_a \in \mathfrak{g} \simeq T_e G$, 

and where $\iota_{v^a}$ is ordinary contraction of [[vector fields]] into [[differential forms]] and $\mathcal{L}_{v^a} = [d_{dR}, \iota-{v^a}]$ is [[Lie derivative]] of differential forms.

With this one defines the sub-[[chain complex]] of _[[horizontal differential forms]]_ as the joint [[kernel]] of the contraction operators (eq:WeilModelContractionOperation)

\[
  \label{WeilModelHorizontalForms}
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{hor}
  \overset{
    ker\big( \{\iota_a\}_a \big)
  }{\hookrightarrow}
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)
\]

(this subspace need not be preserved by the differential, but the following further subspace is)

and the further sub-[[dgc-algebra]] of _basic differential forms_, which are in addition in the [[kernel]] of the [[Lie derivatives]] (eq:WeilModelLieDerivative)

\[
  \label{WeilModelBasicForms}
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{basic}
  \overset{
    ker\big( \{\mathcal{L}_a\}_a \big)
  }{\hookrightarrow}
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{hor}
  \overset{
    ker\big( \{\iota_a\}_a \big)
  }{\hookrightarrow}
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)
\]

Since the [[differential]] $d_{dR} + d_W$ (eq:TensorProductOfdeRhamAlgebraWithWeilAlgebra) graded-commutes with $\iota_a$ to $\mathcal{L}_a$ (by definition and by [[Cartan's magic formula]]) and hence graded-commutes with the [[Lie derivative]] $\mathcal{L}_a$ itself, it restricts to this joint [[kernel]], thus defining a sub-[[dgc-algebra]] (just no longer [[semi-free dg-algebra|semi-free]], in generaL)

\[
  \label{WeilModel}
  \Big(
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{basic}
  , 
  d_{dR} + d_W
  \Big)
\]

This [[dgc-algebra]] is called the _Weil model_ for $G$-equivariant de Rham cohomology of $X$. 

(see [Atiyah-Bott 84](#AtiyahBott84), [Mathai-Quillen 86, Sec. 5](#MathaiQuillen86) [Kalkman 93, Sec.2.1](#Kalkman93), [Miettinen 96, Sec. 2](#Miettinen96)).



#### The Cartan model
 {#TheCartanModel}

The Cartan model follows from the Weil model [above](#TheWeilModel) by algebraically solving the horizontality constraint (eq:WeilModelHorizontalForms). This we discuss first [below](#LabelCartanViaHorizontalProjection). Then we summarize state the resulting dgc-algebra further [below](#CartanModelDirectDefinition).

Reviews include ([Mathai-Quillen 86, Sec. 5](#MathaiQuillen86), [Kalkman 93, section 2.2](#Kalkman93))

##### Via horizontal projection of the Weil model
  {#LabelCartanViaHorizontalProjection}

The _Cartan model_ arises form the Weil model [above](#TheWeilModel) by the observation that the first of the two constraints defining basic differential forms (eq:WeilModelBasicForms), namely the constrain for [[horizontal differential forms]] (eq:WeilModelHorizontalForms), may be uniformly solved:

+-- {: .num_lemma #ProjectionOntoHorizontalDifferentialForms}
###### Lemma
**([[projection operator]] onto [[horizontal differential forms]])**

Consider the [[normal ordering|normal ordered]] [[exponential]] of minus the sum of the contraction [[derivations]] (eq:WeilModelContractionOperation) followed by wedge product with the corresponding degree-1 generator (eq:ExplicitWeilAlgebra)

\[
  \label{ExponentialProjectionOperator}
  :
    \exp
    \big(
      - \theta^a \iota_a
    \big)
  :
  \;=\;
  1 
  - \underset{a}{\sum} \theta^a \iota_a
  + \tfrac{1}{2} \underset{a,b}{\sum} \theta^a \theta^b \iota_b \iota_a
  - \cdots
  \;\;\colon\;\;
  \Omega^\bullet
  \big(
    X 
  \big)
  \otimes
  W(\mathfrak{g})
  \longrightarrow
  \Omega^\bullet
  \big(
    X 
  \big)
  \otimes
  W(\mathfrak{g})
\]

We have:

1. This is the [[projection operator]] onto the sub-space of [[horizontal differential forms]] (eq:WeilModelHorizontalForms).

1. The restriction of this projector to $\Omega^\bullet\big(X \big)$ is a [[graded algebra]]-[[isomorphism]] onto the horizontal forms in $CE(\mathfrak{g}) \otimes \Omega^\bullet\big(X \big)$

   $$
     \Omega^\bullet\big(X \big)
     \underoverset{\simeq}{ :\exp\big( - \theta^a \iota_a \big):  }{\longrightarrow}
     \big( CE(\mathfrak{g}) \otimes \Omega^\bullet(X) \big)_{hor}    
   $$

1. Hence the further [[tensor product]] with $\mathbb{R}\big[ \{r^a\}_a \big]$ is an algebra isomorphism onto the full subspace of [[horizontal differential forms]] (eq:WeilModelHorizontalForms)

   $$
     \mathbb{R}\big[ \{r^a\}_a \big] 
     \otimes
     \Omega^\bullet\big(X \big)
     \underoverset{\simeq}{ 
       :\exp\big( - \theta^a \iota_a \big):  
     }{
       \longrightarrow
     }
     \big( CE(\mathfrak{g}) \otimes \Omega^\bullet(X) \big)_{hor}    
   $$

1. The operator commutes with the [[Lie derivative]] (eq:WeilModelLieDerivative) and hence restricts to an isomorphism onto the sub-[[dgc-algebra]] of basic differential forms (eq:WeilModelBasicForms)

   \[
     \label{IsomorphisamCartanToWeilModel}
     \big(
       \mathbb{R}\big[ \{r^a\}_a \big] 
       \otimes
       \Omega^\bullet\big(X \big)
     \big)^G
     \underoverset{\simeq}{ 
       \;\;\;
       :\exp\big( - \theta^a \iota_a \big): 
       \;\;\;
     }{
       \longrightarrow
     }
     \big( CE(\mathfrak{g}) \otimes \Omega^\bullet(X) \big)_{bas}    
   \]

1. The [[inverse function|inverse]] of (eq:IsomorphisamCartanToWeilModel)

   \[
     \label{IsomorphismWeilToCartanModel}
     \big(
       \mathbb{R}\big[ \{r^a\}_a \big] 
       \otimes
       \Omega^\bullet\big(X \big)
     \big)^G
     \underoverset{\simeq}{ 
       \;\;\;
       \epsilon
       \;\;\;  
     }{
       \longleftarrow
     }
     \big( CE(\mathfrak{g}) \otimes \Omega^\bullet(X) \big)_{bas}    
   \]

   is the [[algebra homomorphism]] given setting all generaotors $\theta^a$ in (eq:ExplicitWeilAlgebra)  to zero

   \[
     \label{WeilAugmentationOverCartan}
     \epsilon \;\colon\;
     \left\{
       \array{
          \omega & \mapsto \omega
          \\
          \theta^a & \mapsto 0
          \\
          r^a & \mapsto r^a
       }
     \right.
   \]

1. The induced [[differential]] on the left, which hence makes $: \exp\big( - \theta^a \iota_a\big) :$ a [[dgc-algebra]]-[[isomorphism]] and hence in particular a [[quasi-isomorphism]] is

   \[
     \label{InducedDifferentialOnCartanModel}
     \epsilon
     \circ
     \big( d_{dR} + d_W\big)     
     \circ
     : \exp\big(  -\theta^a \iota_a \big) :
     \;=\;
     d_{dR}
     +
     r^a \iota_{v^a}
     \,.
   \]

=--

([Cartan 50, Sec. 6](#Cartan50), see e.g. [Mathai-Quillen 86, around (5.9)](#MathaiQuillen86))

+-- {: .proof}
###### Proof

Observe that the operator (eq:ExponentialProjectionOperator) is equal to the product

$$
  :
    \exp
    \big(
      - \theta^a \iota_a
    \big)
  :
  \;=\;
  \big(
    id - \theta^1 \iota_1
  \big)
  \big(
    id - \theta^2 \iota_2
  \big)
  \cdots
  \big(
    id - \theta^{dim(\mathfrak{g})} \iota_{dim(\mathfrak{g})}
  \big)
  \,.
$$

Here all factors commute with each other, and each factor is itself a [[projection operator]], with [[image]] the [[kernel]] of the corresponding single contraction operator, e.g.

$$
  im
  \big(
    1 - \theta^1 \iota_1
  \big)
  \;\simeq\;
  ker\big( \iota_1\big)
$$

etc.

Hence the joint image is the joint kernel of the contraction operators. 

It is clear by inspection that $\epsilon$ in (eq:IsomorphismWeilToCartanModel) is a [[linear map|linear]] [[inverse function|inverse]] to $: \exp\big( - \theta^a \iota_a\big) :$. Therefore, since $\epsilon$ is manifestly an [[algebra homomorphism]], so is $: \exp\big( - \theta^a \iota_a\big) :$.

This implies that the induced differential (eq:InducedDifferentialOnCartanModel) is a graded [[derivation]] and hence that it may be identified by its action on generators. Direct inspection indeed yields

for all generators $r^a$

$$
  \begin{aligned}
     \epsilon
     \circ
     \big( d_{dR} + d_W\big)     
     \circ
     : \exp\big(  -\theta^a \iota_a \big) :
     \big(
       r^a
     \big)
     & = 0
     \\
     & =
     \big( d_{dR} + r^a \iota_{v^a} \big) ( r^a ) 
  \end{aligned}
$$

and for all differential forms $\omega \in \Omega^\bullet\big( X \big)$:

$$
  \begin{aligned}
     \epsilon
     \circ
     \big( d_{dR} + d_W\big)     
     \circ
     : \exp\big(  -\theta^a \iota_a \big) :
     \big( \omega \big)
     & =
     \epsilon
     \circ
     \big( d_{dR} + d_W\big)     
     \big(
       \omega
       - 
       \theta^a \iota_{v^a} \omega
       + 
       \cdots
     \big)
     \\
     & =
     \epsilon
     \circ
     \big(
       d_{dR} \omega
       +
       \underset{a}{\sum} 
       \theta^a 
       d_{dR} \iota_{v^a} \omega
       + 
       \big( r^a - \tfrac{1}{2}f^a_{b c} t^b \wedge t^c \big) 
       \iota_{v^a} \omega
       + 
       \cdots
     \big)
     \\
     & =
       d_{dR} \iota_{v^a} ( \omega)
       + 
       r^a \iota_{v^a} (\omega)
  \end{aligned}
$$


because $\epsilon$ annihilates, by (eq:WeilAugmentationOverCartan), all summands containing a $\theta^a$-factor.

=--

The left hand side [[graded algebra]] of the isomorphism (eq:IsomorphisamCartanToWeilModel) equipped with the induced differential (eq:InducedDifferentialOnCartanModel) is called the _Cartan model_, and that isomorphism exhibits it as equivalent to the Weil model:

$$
  \array{
  \Big(
     \Big(
       \Omega^\bullet\big(X \big)
       \otimes
       \mathbb{R}\big[ \{r^a\}_a \big] 
     \Big)^G
     \,,\,
     d_{dR} + r^a \iota_{v^a}
  \Big)
  &
  \underoverset{\simeq}{
     : \exp\big( - \theta^a \iota_a \big) :
  }{\longrightarrow}
  &
  \Big(
  \Big(
    \Omega^\bullet
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)_{basic}
  , 
  d_{dR} + d_W
  \Big)
  \\
  \text{Cartan model}
  &&
  \text{Weil model}
  }
$$


\linebreak

In summary, the Cartan model is explicitly the following dgc-algebra:


##### Direct definition
  {#CartanModelDirectDefinition}

Write

$$
  (\Omega^\bullet(G, \mathfrak{g}^\ast[1])^G  
  \hookrightarrow
  \Omega(G, \mathfrak{g}^\ast[1])
$$

for the $G$-[[invariant differential forms]] on $G$ with [[coefficients]] in the [[linear dual]] of the Lie algebra $\mathfrak{g}$, shifted up in degree. So for $\{F^a\}$ a dual [[basis]], a general element of this space in degree $2 p + q$ is of the form

$$
   \omega
   \;=\; 
   F^{a_1} \wedge \cdots F^{a_p} 
     \wedge  
    \omega_{a_1,\cdots ,a_q}
  \,,
$$

where $\omega_{\cdots}$ are [[differential n-form|differential q-forms]], such that for each $t_a \in \mathfrak{g}$ the [[Lie derivative]] of these forms satisfies

$$
  \mathcal{L}_{v^a} \omega_{a_1, a_2 \cdots , a_p}
  = 
  f_{a a_1}{}^b \omega_{b , a_2, \cdots , a_p}
  + 
  f_{a a_2}^{}^b \omega_{a_1 ,  b,  \cdots , a_p}
  + 
  \cdots
  \,, 
$$ 

where $\{f_{a b}{}^b\}$ are the structure constants of $\mathfrak{g}$ (eq:StructureConstants).

Equip this [[graded vector space]] $\Omega^\bullet(G, \mathfrak{h}^\ast[1])^G$ with a [[differential]] $d$ by 

$$
  d 
    \colon 
  \omega 
    \mapsto 
  d_{dR}\omega - F^a \iota_{v^a} \omega
$$

(e.g. [Kalkman 93 (1.15)](#Kalkman93)).

The resulting [[dgc-algebra]] $(\Omega^\bullet(G,\mathfrak{g}^\ast[1])^G, d)$ is the _Cartan model_ for $G$-equivariant de Rham cohomology on $X$.

\linebreak

## Related concepts

* [[gauged WZW model]]

* [[action Lie algebroid]], [[BRST complex]]

## References
  {#References}

Due to 

* {#Cartan50} [[Henri Cartan]], _La transgression dans un groupe de Lie et dans un espace fibré principal_, Colloque de topologie (espaces fibrés). Bruxelles, 1950

Review is in 

* Oliver Goertsches, Leopold Zoller, _Equivariant de Rham Cohomology: Theory and Applications_, São Paulo J. Math. Sci. (2019) ([arXiv:1812.09511](https://arxiv.org/abs/1812.09511), [doi:10.1007/s40863-019-00129-4](https://doi.org/10.1007/s40863-019-00129-4))

Early discussion of the Weil model includes

* {#AtiyahBott84} [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_, Topology 23, 1 (1984) (<a href="https://doi.org/10.1016/0040-9383(84)90021-1">doi:10.1016/0040-9383(84)90021-1</a>, [pdf](https://www.math.stonybrook.edu/~mmovshev/MAT570Spring2008/BOOKS/atiyahbott_moment.pdf))
 

A good account of the Weil model, the Cartan model and their equivalence is in 

* {#MathaiQuillen86} [[Varghese Mathai]], [[Daniel Quillen]], _Superconnections, Thom classes and equivariant differential forms_, Topology 25, 85 (1986)  (<a href="https://doi.org/10.1016/0040-9383(86)90007-8">doi:10.1016/0040-9383(86)90007-8</a>)
 

A review of the Weil model and the Cartan model and the introduction of the "BRST model" (Kalkman model) is in

* {#Kalkman93} Jaap Kalkman, _BRST model applied to symplectic geometry_, Ph.D. Thesis, Utrecht, 1993 ([arXiv:hep-th/9308132](https://arxiv.org/abs/hep-th/9308132), [cds:9308132](http://cds.cern.ch/record/568522), [euclid:1104252784](http://projecteuclid.org/euclid.cmp/1104252784))

  (original arXiv pdf broken)

Discussion in the broader context of [[equivariant cohomology|equivariant]] [[differential cohomology]] is in

* Andreas Kübel, [[Andreas Thom]], _Equivariant Differential Cohomology_, Transactions of the American Mathematical Society (2018) ([arXiv:1510.06392](https://arxiv.org/abs/1510.06392))
 

Discussion in the context of the [[gauged WZW model]] includes

* {#Witten92} [[Edward Witten]], appendix of _On holomorphic factorization of WZW and coset models_,  Comm. Math. Phys. Volume 144, Number 1 (1992), 189-212. ([EUCLID](http://projecteuclid.org/euclid.cmp/1104249222))

* {#FigueroaOFarrillStanciu94} [[José Figueroa-O'Farrill]], S Stanciu, _Gauged Wess-Zumino terms and Equivariant Cohomology_, Phys.Lett. B341 (1994) 153-159 ([arXiv:hep-th/9407196](http://arxiv.org/abs/hep-th/9407196))

* [[José de Azcárraga]],  J. C. Perez Bueno, _On the general structure of gauged Wess-Zumino-Witten terms_ ([arXiv:hep-th/9802192](http://arxiv.org/abs/hep-th/9802192))

Discussion in view of [[supersymmetry]]:

* {#Miettinen96} Mauri Miettinen, _Weil Algebras and Supersymmetry_ ([arXiv:hep-th/9612209](https://arxiv.org/abs/hep-th/9612209), [cds:317377](http://cds.cern.ch/record/317377), [spire:427720](http://inspirehep.net/record/427720))

* {#GuilleminSternberg99} [[Victor Guillemin]], [[Shlomo Sternberg]], _Supersymmetry and equivariant de Rham theory_, Springer, (1999) ([doi:10.1007/978-3-662-03992-2](https://link.springer.com/book/10.1007/978-3-662-03992-2))
  
 

[[!redirects Weil model]]
[[!redirects Weil models]]
[[!redirects Cartan model]]
[[!redirects Cartan models]]
[[!redirects Kalkman model]]
[[!redirects Kalkman models]]

[[!redirects Weil model for equivariant cohomology]]
[[!redirects Cartan model for equivariant cohomology]]
[[!redirects Kalkman model for equivariant cohomology]]