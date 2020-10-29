
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

The [[equivariant cohomology]]-generalization of [[de Rham cohomology]].

| [[cohomology]] | [[Borel equivariant cohomology|Borel]]-[[equivariant cohomology]] |
|---|---|
| [[real cohomology|real]] [[ordinary cohomology]] | real [[equivariant ordinary cohomology]] |
| [[de Rham cohomology]] | [[equivariant de Rham cohomology]]

## Properties


Throughout we consider the following setup:

+-- {: .num_defn #SmoothGManifold}
###### Definition
**([[smooth manifold]] with [[smooth function|smooth]] [[action]] of a [[Lie group]])**

Let

1. $X$ be a [[smooth manifold]] with [[de Rham algebra]] denoted $\big( \Omega^\bullet(X), d_{dR} \big)$,

1. $G$ a [[Lie group]] with [[Lie algebra]] denoted $\big(\mathfrak{g}, [-,-]\big)$,

1. $X \times G \overset{\rho}{\longrightarrow} X$ a [[smooth function|smooth]] [[action]] of $G$ on $X$.

Often this data is called a _smooth $G$-manifold $X$_, or similar.

=--


### Models
 {#Models}


Given a smooth $G$-manifold $X$ (Def. \ref{SmoothGManifold}) various [[dg-algebras]] are used to model the corresponding $G$-equivariant de Rham cohomology $X$, known as 

* _[the Weil model](#TheWeilModel)_

* _[the Cartan model](#TheCartanModel)_

* _the BRST/Kalkman model_



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

On this consider the following joint [[Cartan calculus]] operations: for each basis element $t_a$ (eq:LinearBasisForG) a graded [[derivation]] of degree -1 (contraction)

\[ \label{WeilModelContractionOperation}
  \iota_a
  \;\colon\;
  \Big(
    \Omega
    \big(
      X 
    \big)
    \otimes
    W(\mathfrak{g})
  \Big)^{\bullet}
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

and the further sub-[[dgc-algebra]] of _[[basic differential forms]]_, which are in addition in the [[kernel]] of the [[Lie derivatives]] (eq:WeilModelLieDerivative)

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

The Cartan model follows from the Weil model [above](#TheWeilModel) by algebraically solving the horizontality constraint (eq:WeilModelHorizontalForms). This we discuss first [below](#LabelCartanViaHorizontalProjection). Then we describe the resulting dgc-algebra further [below](#CartanModelDirectDefinition).

Reviews include ([Mathai-Quillen 86, Sec. 5](#MathaiQuillen86), [Kalkman 93, section 2.2](#Kalkman93))

##### Via horizontal projection of the Weil model
  {#LabelCartanViaHorizontalProjection}

The _Cartan model_ arises form the Weil model [above](#TheWeilModel) by the observation that the first of the two constraints defining [[basic differential forms]] (eq:WeilModelBasicForms), namely the constrain for [[horizontal differential forms]] (eq:WeilModelHorizontalForms), may be uniformly solved:

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

1. The operator commutes with the [[Lie derivative]] (eq:WeilModelLieDerivative) and hence restricts to an isomorphism onto the sub-[[dgc-algebra]] of [[basic differential forms]] (eq:WeilModelBasicForms)

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

This is the _Mathai-Quillen isomorphism_ ([Mathai-Quillen 86, around (5.9)](#MathaiQuillen86)).

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

\[
  \label{QuasiIsoFromCartanToWeilModel}
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
\]

This statement is originally due to [Cartan 50, Sec. 6](#Cartan50).

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


### Equivariant de Rham theorem
 {#EquDeRhamTheorem}

The point of the [above](#Models) dgc-algebra models is that, under suitable conditions, their [[cochain cohomology]] computes the [[real cohomology]] of the [[homotopy type]] of the [[homotopy quotient]] $X \sslash H$, which, as an actual [[topological space]], may be presented by the [[Borel construction]] $X \times_G E G$, hence the [[Borel equivariant cohomology|Borel equivariant]] [[de Rham cohomology]] of $X$.

This is the [[equivariant cohomology]]-generalization of the plain [[de Rham theorem]]:

+-- {: .num_prop #EquivariantDeRhamTheorem}
###### Proposition
**([[equivariant de Rham theorem]])**

Let 

1. $G$ be a [[Lie group]] which is

   1. [[compact Lie group|compact]];

   1. [[connected topological space|connected]];

1. $X$ be a smooth $G$-manifold (Def. \ref{SmoothGManifold}).

Then the [[cochain cohomology]] of (the [[cochain complex]] underlying) the Weil model [[dgc-algebra]] (eq:WeilModel), and hence, by Lemma \ref{ProjectionOntoHorizontalDifferentialForms}, also of the Cartan model [[dgc-algebra]] (eq:QuasiIsoFromCartanToWeilModel). is [[isomorphism|isomorphic]] to the [[real cohomology]] of the [[homotopy quotient]] $X \!\sslash\! G$ of the action on (the [[topological space]] underlying) $X$ by the ([[topological group]] underlying) $G$, hence in particular of the [[Borel construction]] $X \times_G E G \simeq  X \!\sslash\! G $:

\[
  \array{
  \text{Cartan model cohomology}
  \\
  H^\bullet
  \Big(
     \Big(
       \Omega^\bullet\big(X \big)
       \otimes
       \mathbb{R}\big[ \{r^a\}_a \big] 
     \Big)^G
     \,,\,
     d_{dR} + r^a \iota_{v^a}
  \Big)
  \\
  {}^{\simeq}
  \Big\downarrow
  {}^{
     H^\bullet\big( : \exp\big( - \theta^a \iota_a \big) : \big)
  }
  \\
  H^\bullet
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
  &\underoverset{\simeq}{\;\;\;\;\;\;\;\;\;\;\;\;\;}{\longrightarrow}&
  H^\bullet
  \big(
    X \!\!\sslash\!\! G
    \,,\,
    \mathbb{R}
  \big)
  \\
  \text{Weil model cohomology}
  &&
  \mathclap{
    \text{equivariant real cohomology}
  }
  }
\]

=--

(e.g [Meinrenken 06, Theorem 6.1](#Meinrenken06))

+-- {: .proof #ProofOfEquivariantDeRhamTheorem}
###### Proof idea

Recall that the [[product topological space]] $X \times E G$ of $X$ with the total space $E G$ of the [[universal principal bundle]], equipped with the [[diagonal action]] by the group $G$, constitutes a [[resolution]] of $X$ as a [[topological G-space]], in that the [[projection]]

$$
  X \times  E G
  \underoverset{\simeq_{whe}}{ \;\;\; pr_1 \;\;\; }{\longrightarrow}
  X
$$

is a $G$-[[equivariant function]] which is a [[weak homotopy equivalence]] (since $E G$ is a [[weakly contractible topological space]]) and the [[diagonal action|diagonal]] $G$-[[action]] on $X \times E G$ is [[free action|free]] (since the action on $E G$ is). Therefore the [[homotopy quotient]] of $X$ by $G$ is presented by the ordinary [[quotient space]] of $X \times E G$ by $G$, which is what is called the [[Borel construction]]

$$
  X \times_G E G 
    \;\coloneqq\;
  \big(
    X \times E G
  \big)/G
  \;\simeq_{whe}\;
  X \sslash G
$$

The point now is that the Weil model (eq:WeilModel) for equivariant cohomology is exactly the analog of the Borel construction in terms of dgc-algebraic [[rational homotopy theory]]-type models in [[real cohomology]]:

By the ordinary [[de Rham theorem]] the image of the smooth manifold $X$ in dgc-algebra [[rational homotopy theory]] (with [[real number]]-[[coefficients]]) is given by the [[de Rham algebra]] $\Omega^\bullet(X)$, and the image of $E G$ is the [[Weil algebra]] $W(\mathfrak{g})$: The [[contractible topological space|contractability]] of $E G$ corresponds to the free propery ([here](Weil+algebra#FreeProperty)) of the Weil algebra, and the $G$-[[action]] on $E G$ corresponds to the canonical $\mathfrak{g}$-[[Cartan calculus]] on $W(\mathfrak{g})$.

Since for a [[free action]] the invariant forms are the [[basic differential forms]], this shows that/how the Weil model is the image of the [[Borel construction]] in dgc-algebraic [[rational homotopy theory]]:

\begin{xymatrix}
  &
  X \times E G \ar@(ul,ur)^G
  \ar[d]^-{ q }
  &
  \Omega^\bullet( X )
  \otimes 
  W(g)
  \ar@(ur,ul)_{ g }
  \ar@{<-^{)}}[d]^-{ q^\ast }
  \\
  \;
  X // G
  \ar@{}[r]|-{
    \simeq_{\mathrm{whe}}
  }
  &  
  \big(
    X \times E G 
  \big)/G
  &
  \big(
    \Omega^\bullet( X )
    \otimes 
    W(g)
  \big)_{\mathrm{basic}} 
  \ar@{<-}[r]^-{ :\exp\big( t^a \iota_a\big): }_-{\simeq}
  &
  \big(
    \Omega^\bullet( X )\big[ r^a \big]
  \big)^G
  \\
  &
  \mbox{Borel construction}
  &
  \mbox{Weil model}
  &
  \mbox{Cartan model}
\end{xymatrix}


$\,$


=--

+-- {: .num_remark}
###### Remark

A generalization of the [[equivariant de Rham theorem]] to non-[[compact Lie group|compact]] Lie groups exists ([Getzler 94](#Getzler94)) but this uses the [[simplicial de Rham complex]] of the [[action groupoid]] $X \sslash G$ ([Bott-Shulman-Stasheff 76](#BottShulmanStasheff76)) and is thus a fair bit more complicated, computationally.

=--


### Cartan's map
  {#CartanMap}

If the [[G-space|G-manifold]] $X$ has a [[free action]], hence is the total space $X = P$ of a $G$-[[principal bundle]] $P \to B$, then the _Cartan map_ (or _[[Cartan's map]]_ or similar) is a [[quasi-isomorphism]] from the [[Cartan model]] for the [[equivariant de Rham cohomology]] of $X = P$ to the ordinary [[de Rham complex]] model for the ordinary [[de Rham cohomology]] of the base manifold $B$

$$
  \array{
    \bigg(
       \Big(
         \Omega^\bullet\big(P \big)
         \otimes
         \mathbb{R}\big[ \{r^a\}_a \big] 
       \Big)^G
       \,,\,
       d_{dR} + r^a \iota_{v^a}
    \bigg)
    &
    \overset{
       \simeq_{qi}
    }{\longrightarrow}
    &
    \Big(
      \Omega^\bullet_{dR}(B),
      \,
      d_{dR}
    \Big)
    \\
    \omega \otimes \langle - \rangle
    &
    \mapsto
    &
    \omega_{hor} \otimes \langle F_\nabla\rangle
  }
$$

given by choosing an [[Ehresmann connection]] $\nabla$ on $P \to B$ and inserting its [[curvature form]] into the [[invariant polynomials]] $\langle-\rangle$ (essentially the [[Chern-Weil homomorphism]]).

([Guillemin-Sternberg 99, Chapter 5](#GuilleminSternberg99), [Albin-Melrose 09, Theorem 11.1](#AlbinMelrose09))

\linebreak





## Related concepts

* [[equivariant localization]]

* [[equivariant ordinary differential cohomology]]

* [[equivariant PL de Rham complex]], [[equivariant PL de Rham theorem]]

* [[gauged WZW model]]

* [[action Lie algebroid]], [[BRST complex]]


## References
  {#References}

The Cartan model for equivariant de Rham cohomology is originally due to

* {#Cartan50} [[Henri Cartan]], _La transgression dans un groupe de Lie et dans un espace fibré principal_, Colloque de topologie (espaces fibrés). Bruxelles, 1950

Review includes

* {#Meinrenken06} [[Eckhard Meinrenken]], _Equivariant cohomology and the Cartan model_, in: _Encyclopedia of Mathematical Physics_, Pages 242-250 Academic Press 2006 ([pdf](http://www.math.toronto.edu/mein/research/enc.pdf), [doi:10.1016/B0-12-512666-2/00344-8](https://doi.org/10.1016/B0-12-512666-2/00344-8))

* Oliver Goertsches, Leopold Zoller, _Equivariant de Rham Cohomology: Theory and Applications_, São Paulo J. Math. Sci. (2019) ([arXiv:1812.09511](https://arxiv.org/abs/1812.09511), [doi:10.1007/s40863-019-00129-4](https://doi.org/10.1007/s40863-019-00129-4))

See also 

* Camilo Arias Abad, [[Marius Crainic]], Sec. 1 of: _The Weil algebra and the Van Est isomorphism_ ([arXiv:0901.0322](https://arxiv.org/abs/0901.0322))

Early discussion of the Weil model includes

* {#AtiyahBott84} [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_, Topology 23, 1 (1984) (<a href="https://doi.org/10.1016/0040-9383(84)90021-1">doi:10.1016/0040-9383(84)90021-1</a>, [pdf](https://www.math.stonybrook.edu/~mmovshev/MAT570Spring2008/BOOKS/atiyahbott_moment.pdf))
 
The slick proof of the equivalence between the Weil model and the the Cartan model via the _Mathai-Quillen isomorphism_ (Lemma \ref{ProjectionOntoHorizontalDifferentialForms}) is due to

* {#MathaiQuillen86} [[Varghese Mathai]], [[Daniel Quillen]], Sec. 5 of _Superconnections, Thom classes and equivariant differential forms_, Topology 25, 85 (1986)  (<a href="https://doi.org/10.1016/0040-9383(86)90007-8">doi:10.1016/0040-9383(86)90007-8</a>)
 
A review of the Weil model and the Cartan model and the introduction of the "BRST model" (Kalkman model) is in

* {#Kalkman93} [[Jaap Kalkman]], _BRST model applied to symplectic geometry_, Ph.D. Thesis, Utrecht, 1993 ([arXiv:hep-th/9308132 (broken)](https://arxiv.org/abs/hep-th/9308132), [cds:9308132](http://cds.cern.ch/record/568522), [pdf](http://cds.cern.ch/record/568522/files/9308132.pdf))

* [[Jaap Kalkman]], _BRST Model for Equivariant Cohomology and  Representatives for the Equivariant Thom Class_, Comm. Math. Phys. Volume 153, Number 3 (1993), 447-463. ([euclid:1104252784](http://projecteuclid.org/euclid.cmp/1104252784))


Generalization of the [[equivariant de Rham theorem]] to non-compact Lie groups is due to 

* {#Getzler94} [[Ezra Getzler]], _The Equivariant Chern Character for Non-compact Lie Groups_, Advances in Mathematics Volume 109, Issue 1, November 1994, Pages 88-107 ([doi:10.1006/aima.1994.1081](https://doi.org/10.1006/aima.1994.1081))

based on the [[simplicial de Rham complex]]

* {#BottShulmanStasheff76} [[Raoul Bott]], [[Herbert Shulman]], [[Jim Stasheff]], _On the de Rham theory of certain classifying spaces_, Advances in Mathematics, Volume 20, Issue 1, April 1976, Pages 43-56 (<a href="https://doi.org/10.1016/0001-8708(76)90169-9">doi:10.1016/0001-8708(76)90169-9</a>, [pdf](https://core.ac.uk/download/pdf/82496263.pdf))

Review with emphasis on [[equivariant localization]] formulas:

* [[Vasily Pestun]], _Review of localization in geometry_ ([arXiv:1608.02954](https://arxiv.org/abs/1608.02954)), chapter in: [[Vasily Pestun]], [[Maxim Zabzine]] (eds.) _Localization techniques in quantum field theories_,  J. Phys. A: Math. Theor. 50 440301, 2017 ([doi:10.1088/1751-8121/aa63c1](https://iopscience.iop.org/article/10.1088/1751-8121/aa63c1), [arXiv:1608.02952](https://arxiv.org/abs/1608.02952), [full pdf](http://pestun.ihes.fr/pages/LocalizationReview/LocQFT.pdf))

Discussion in relation to [[resolution of singularities]]:

* {#AlbinMelrose09} Pierre Albin, [[Richard Melrose]], _Equivariant cohomology and resolution_ ([arXiv:0907.3211](https://arxiv.org/abs/0907.3211))


See also

* Hugo Garcia-Compean, Pablo Paniagua, [[Bernardo Uribe]], _Equivariant extensions of differential forms for non-compact Lie groups_ ([arXiv:1304.3226](https://arxiv.org/abs/1304.3226))

Some related discussion for equivariant [[Riemannian geometry]] in

* [[Peter Michor]], _Basic Differential Forms for Actions of Lie Groups_, Proceedings of the American Mathematical Society Vol. 124, No. 5 (May, 1996), pp. 1633-1642 ([jstor:](ttps://www.jstor.org/stable/2161476))

Discussion in the broader context of [[equivariant ordinary differential cohomology]] is in

* Andreas Kübel, [[Andreas Thom]], _Equivariant Differential Cohomology_, Transactions of the American Mathematical Society (2018) ([doi:10.1090/tran/7315](https://doi.org/10.1090/tran/7315), [arXiv:1510.06392](https://arxiv.org/abs/1510.06392))
 

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

[[!redirects equivariant de Rham theorem]]
