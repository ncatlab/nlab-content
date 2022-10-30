
> This entry contains one chapter of the material at _[[geometry of physics]]_.

> previous chapter: _[[geometry of physics -- smooth spaces|smooth sets]]_

> next chapter:_[[geometry of physics -- groups|groups]]_

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## **Smooth homotopy types**
 {#SmoothnGroupoids}
 {#SmoothGroupoids}


Fundamental physics is all based on the _[[gauge principle]]_. This says in particular that it is wrong to think of two different _[[gauge field]] configurations_ (discussed in detail below in _[Fields](#Fields)_) as being [[equality|equal]] or not. Instead it makes sense to ask if there is (or not) a _[[gauge transformation]]_ from one to the other that exibits an gauge [[equivalence]] between the two fields. The simplest example of this is described in detail below in  _[Gauge transformations in electromagnetism](#GaugeTransformationsInElectromagnetism)_.

But this means that the collection of [[gauge fields]] on a [[spacetime]] $X$, which we will write as a [[mapping space]] $[X, \mathbf{B}G_{conn}]$, cannot be a [[smooth space]] as considered above, for if it were such a smooth space, then we could ask if two gauge fields $\nabla_1, \nabla_2 \colon * \to [X,\mathbf{B}G_{conn}]$ were equal or not. 

Notice that this already applies to a single gauge field: given any $\nabla \colon * \to [X,\mathbf{B}G_{conn}]$ it is certainly equal to itself, but is nevertheless also _gauge equivalent_ to itself, but the latter it may be in several non-equivalent ways: there may be non-trivial auto-gauge transformations $\nabla \to \nabla$. Since these can be composed, are, by definition, invertible, and contain the trivial gauge transformaiton, these form a _[[group]]_, the group of auto-gauge equivalences of $\nabla$. (Groups are discussed in detail below in _[Groups](#Groups)_) If that gauge field $\nabla$ is itself the trivial gauge field, $\nabla = \nabla_0$, then this group of auto-gauge equivalences is the _[[gauge group]]_ of the given [[gauge theory]]:

$$
  G \simeq Aut(\nabla_0) \simeq \{\nabla_0 \stackrel{\simeq}{\to} \nabla_0\}
  \,.
$$

For this reason, the collection of _all_ gauge fields and all gauge transformations between them form something that is a [[group]] over ever fixed element, but which generalizes the notion of a group in that there are not only auto-equivalences, but also equivalences going from one element to another. Such a structure is called a _[[groupoid]]_. Gauge fields form not a [[set]] with smooth structure, a [[smooth space]], but a [[groupoid]] with smooth structure: a _[[smooth groupoid]]_. 

At least ordinary gauge fields do. More generally, the gauge princple goes further: it is in general also a mistake to assume that given two gauge transformations $\lambda_1, \lambda_2 \colon \nabla_1 \to \nabla_2$ between two gauge fields, it makes good sense to ask whether they are equal or not. Again, the gauge prinicle says that we should instead ask if there is a _[[gauge-of-gauge transformation]]_ between them, that exhibits a gauge [[equivalence]] $\rho \colon \lambda_1 \simeq \lambda_2$. If these gauge-of-gauge equivalences are nontrivial it would seem that gauge fields form a generalization of the notion of a [[groupoid]] called a _[[2-groupoid]]_. But in general the gauge principle goes on: we can in general never decide if two $n$-fold gauge-of-gauge transformations are actually equal, all we have is, possibly, an $(n+1)$-fold gauge transformation going between them which exhibits their gauge equivalence, this being so for all $0 \lt n \lt \infty$. One therefore says that gauge fields in general form an _[[∞-groupoid]]_ whose _[[n-morphisms]]_ are $n$-fold [[gauge-of-gauge transformations]]. These $\infty$-groupoids are also called _[[homotopy types]]_. And since at the same time there is still a notion of gauge fields varying smoothly, these are _[[smooth ∞-groupoids]]_ or _[[smooth homotopy types]]_. This is what we discuss here. 

Remarkably, the same concept appears in [[constructive mathematics]]: there it is in general wrong to consider an [[equality]] between two [[terms]] $\nabla_1, \nabla_2 \colon [X, \mathbf{B}G_{conn}]$, instead one is to consider an explicit [[proof]] that they are equal, provide an explicit [[equivalence]] between them. Such a proof $\lambda$ is itself a [[term]], of [[identity type]], written just as before, $\lambda \colon (\nabla_1 \simeq \nabla_2)$. And, in turn, the same applies to these proofs of equivalence themselves: in [[constructive mathematics]] one demands a [[proof]] $\rho$ that two equivalences $\lambda_1, \lambda_2 \colon (\nabla_1 \simeq \nabla_2)$ are equivalent, and hence a term $\rho \colon (\lambda_1 \simeq \lambda_2)$ of a higher [[identity type]]. If this goes ever on, and one speak of _[[intensional type theory]]_ or _[[homotopy type theory]]_.

This remarkable matching of [[higher gauge theory]] and [[homotopy type theory]] is what drives the discussion here.  

+-- {: bluebox }
###### Contents:

1. [Model layer](#SmoothHomotopyTypesModelLayer)

   This introduces _[[groupoids]]_, then _[[smooth groupoids]]_ and eventually _[[∞-groupoids]]_ modeled as _[[Kan complexes]]_ and then _[[smooth ∞-groupoids]]_.

1. [Semantics layer](#SmoothHomotopyTypesSemanticLayer)

   This introduces the general abstract framework for [[smooth ∞-groupoids]] which is _[[cohesion]]_ of [[(∞,1)-toposes]].

1. [Syntactic layer](#SmoothHomotopyTypesSyntacticLayer)

   This introduces the [[internal language]] of [[cohesive (∞,1)-toposes]], called _[[cohesive homotopy type theory]]_.

**Remark** _The reader who is after elementary exposition may want to skip over this discussion of [[homotopy theory]] on first reading to the next chapter _[Groups](#Groups)_ and only come back here for reference as need arises.

=--



### Model Layer
 {#SmoothHomotopyTypesModelLayer}

#### Groupoids
 {#Groupoids}


> For the content of this section currently see at _[Essence of gauge theory: Groupoids and basic homotopy 1-type theory](#GroupoidsAndBasicHomotopy1TypeTheory)_ below.


#### Gauge transformations in electromagnetism
 {#GaugeTransformationsInElectromagnetism}

The mathematical notion of _[[groupoid]]_ is well familiar, in slight disguise, in basic _[[gauge theory]]_. Here we make this explicit for basic [[electromagnetism]].

We have seen in _[The electromagnetic field strength](#ElectromagneticFieldStrength)_ that a configuration of the electromagnetic field on $\mathbb{R}^4$ is given by a [[differential 1-form]] $A \in \Omega^1(\mathbb{R}^4)$, the "[[electromagnetic potential]]". It describes a field configuration with [[field strength]] Lorentz tensor (with respect to the canonical [[coordinates]] $(t, x^1, x^2, x^3) \coloneqq (x^i)_{i = 1}^4 = $ on $\mathbb{R}^4$)

$$
  \begin{aligned}
    F & = \mathbf{d}A 
      \\
      & =
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
      \\
      & 
       + B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3
       + B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1
       + B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2
  \end{aligned}     
$$

with electric [[field strength]] $(E_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ and magnetic [[field strength]] $(B_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ given  that is given by the [[de Rham differential]] of $A$:

$$
  \begin{aligned}
    F = \mathbf{d}A
  \end{aligned}
  \,.
$$

After Maxwell it was thought that $F \in \Omega^2(\mathbb{R}^4)$ alone genuinely reflects the configuration of the electromagnetic field. But with the discovery of [[quantum mechanics]] it became clear that it is indeed the potential $A$ itself that reflects the configuration of the electromagnetic field: in the presence of [[magnetic flux]] or other topoligical constraints, there can be different $A, A' $ with the _same_ $F = \mathbf{d}A = \mathbf{d}A'$ which nevertheless describe experimentally distinguishable electromagnetic field configurations. (Distinguishable by the [[Aharonov-Bohm effect]] and also to some extent by [[Dirac charge quantization]]; this is discussed at _[Circle-principal connections](#CirclePrincipalConnections)_ below.)

However, not all different gauge potentials describe different physics. The actual configuration space of electromagnetism on a [[spacetime]] $X$ is finer than $\mathbf{\Omega}^2_{cl}(X)$ but coarser than $\mathbf{\Omega}^1(X)$. And it is not quite a smooth space itself, but a _[[smooth groupoid]]_:

one finds that two electromagnetic potentials $A, A' \in \Omega^1(\mathbb{R}^4)$ for which there is a function $\lambda \in C^\infty(\mathbb{R}^4)$ such that 

$$
  A' = A + \mathbf{d}\lambda
$$

represent _different but [[equivalence|equivalent]]_ field configurations. One says that _$\lambda$ induces a [[gauge transformation]] from $A$ to $A'$_. We write $\lambda \colon A \stackrel{\simeq}{\to} A'$ to reflect this.

So the configuration space of electromagnetism does not just have points and coordinate systems. But it is also equipped with the information of a space of gauge transformations between any two coordinate systems laid out in it (which may be empty). 

To see what the structure of such a _smooth gauge groupoid_ should be, notice that the above defines an [[action]] of smooth functions $\lambda$ on smooth $1$-forms $A$, 


+-- {: .num_defn #ActionOfFunctionsOnForms}
###### Definition

For any $U \in $ [[CartSp]], Write $\Omega^1_{vert}(X \times U)$ for the set of [[differential 1-forms]] on $X \times U$ with no components along $U$, and write $C^\infty(X \times U , U(1))$ for the [[group]] of [[circle group]] valued [[smooth functions]]. There is an [[action]] of this group on the 1-forms 

$$
  \rho_U 
   \colon 
  \Omega^1_{vert}(X \times U) \times C^\infty(X \times U, U(1))
    \to
  \Omega^1_{vert}(X \times U)
$$

given by

$$
  \rho_U \colon (A,\lambda) \mapsto A + \mathbf{d}_X \lambda
  \,.
$$

=--

Given such an action of a [[discrete group]] on a [[set]], we might be demoted to form the [[quotient]] set $\Omega^1_{vert}(X\times U)/C^\infty(X \times U, U(1))$. This set contains the gauge [[equivalence classes]] of $U$-parameterized collections of electromagnetic gauge fields on $X$. But it turns out that this is too little information to correctly capture physics. For that instead we need to remember not just that two gauge fields are equivalent, but how they are equivalent. That is, we for $\lambda$ a gauge transformation from $A_1$ to $A_2$, we should have an [[equivalence]] $\lambda \colon A_1 \stackrel{\simeq}{\to} A_2$.

+-- {: .num_defn #EMGaugeGroupoidOverU}
###### Definition

The [[action groupoid]]

$$
  \Omega^1_{vert}(X\times U)\sslash C^\infty(X \times U, U(1))
  \coloneqq
  (
    \Omega^1_{vert}(X\times U) \times C^\infty(X \times U, U(1))
    \stackrel{\overset{t = \rho}{\to}}{\underset{s = p_1}{\to}}
    \Omega^1_{vert}(X\times U)
  )
$$

is the [[groupoid]] whose 

* [[objects]] are $U$-parameterized collections of gauge potentials $A \in \Omega^1_{vert}(X \times U)$;

* [[morphisms]] are pairs $(A,\lambda)$ with $A$ an object and $\lambda \in C^\infty(X \times U, U(1))$, with [[domain]] $A$ and [[codomain]] $A + \mathbf{d}_X \lambda$;

* [[composition]] is given by multiplication of the $\lambda$-labels in the group $C^\infty(X \times U, U(1))$.

=--

This is the discrete _gauge groupoid_ for $U$-parameterized collections of fields. It refines the _[[gauge group]]_, which is recoverd as its [[fundamental group]]:

+-- {: .num_prop }
###### Proposition

Let $A_0 \coloneqq 0 \in \Omega^1_{vert}(X \times U)$ be the trivial gauge field. Then its [[automorphism group]] in the gauge groupoid of def. \ref{EMGaugeGroupoidOverU} is the group of [[circle]]-group valued functions on $U$:

$$
  \pi_1(\Omega^1_{vert}(X\times U)\sslash C^\infty(X \times U, U(1)), A_0)
  =
  Aut(A_0)
  \simeq
  C^\infty(U,U(1))
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition, an automorphism of $A_0$ is given by a function 
$\lambda \in C^\infty(X \times U, U(1))$ such that $A_0 = A_0 + \mathbf{d}_X \lambda$. This is the case precisely if $\mathbf{d}_X \lambda = 0$, hence if $\lambda$ is contant along $X$. But a function on $X \times U$ which is constant along $X$ is canonically identified with a function on just $U$.

=--

All this data in in fact [[natural transformation|natural]] in $U$. Recall that $\Omega^1_{vert}(X \times U) = \mathbf{\Omega}^1(X)(U)$ is the set of $U$-charts of the smooth moduli space $\mathbf{\Omega}^1(X)$ of smooth 1-forms on $X$. Similarly $C^\infty(X \times U) = \mathbf{C}^\infty(X)(U)$.

+-- {: .num_prop }
###### Proposition

There is a homomorphism of [[smooth spaces]] (def. \ref{HomomorphismOfSmoothSpaces})

$$
  \rho \colon \mathbf{\Omega}^1(X)\times \mathbf{C}^\infty(X) \to \mathbf{\Omega}^1(X)
$$

from the product smooth space, def. \ref{ProductOfSmoothSpaces}, of the smooth moduli spaces of 1-forms and 0-forms on $X$, def. \ref{SmoothSpaceOfFormsOnSmoothSpace}, to that of smooth functions, def. \ref{SmoothSpaceOfSmoothFunctions}, whose component over $U \in $ [[CartSp]] is the action 

$$
  \rho_U \colon (A,\lambda) \mapsto  A + \mathbf{d}\lambda
$$

of def. \ref{ActionOfFunctionsOnForms}.

=--

We then also want to consider a _smooth action groupoid_.

+-- {: .num_defn }
###### Definition

Write 

$$
  \mathbf{\Omega}^1(X) \sslash \mathbf{C}^\infty(X, U(1))
  : 
  CartSp^{op}
  \to 
  Grpd
$$

for the [[contravariant functor]] from coordinate systems to the [[category]] of [[groupoids]], which assigns to $U \in CartSp$ the discrete action groupoid of $U$-collections of gauge fields of def. \ref{EMGaugeGroupoidOverU}.

$$
  U \mapsto \Omega^1_{vert}(X \times U)\sslash C^\infty(X\times U, U(1))
  \,.
$$

=--

Such a structure _[[presheaf]]_ of [[groupoids]] is a common joint generalization of the notion of [[discrete groupoids]] and [[smooth spaces]]. We call them _[[smooth groupoids]]_. This is what we turn to in _[Smooth groupoids](#SmoothGroupoids)_

#### Smooth groupoids
 {#SmoothGroupoids}


+-- {: .num_defn }
###### Definition

Write [[Grpd]]${}_1$ for the [[category]] of [[groupoids]] and [[functors]] between them. Write then

$$
  gPsh(CartSp) \coloneqq Funct(CartSp^{op}, Grpd)
$$

for the [[category]] of [[groupoid]]-valued [[presheaves]].

=--

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$, and $0 \lt r \lt 1 \in \mathbb{R}$ let 

$$
  \mathbb{R}^n \simeq D^n_r \hookrightarrow \mathbb{R}^n
$$

Be the smooth function that regards $\mathbb{R}^n$ as the standard $n$-[[disk]] of radius $r$ around the origin in $\mathbb{R}^n$.

For $X \in gPSh(CartSp)$ we write

$$
  (D^n)^* X \coloneqq {\lim_\to}_r X(D^n_r) \in Grpd
$$

for the [[stalk]] of $X$ at the origin of $\mathbb{R}^n$. This is a [[functor]]

$$
  (D^n)^* \colon gPSh(CartSp) \to Grpd
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

A morphism $f \colon X \to Y$ in $gPSh(CartSp)$ we call a 
_local [[weak equivalence]]_ if for every $n \in \mathbb{N}$
the stalk 

$$
  (D^n)^* f \colon (D^n)^* X \to (D^n)^* Y
$$

is an [[equivalence of groupoids]].

=--

+-- {: .num_defn }
###### Definition

Write 

$$
  Smooth1Type 
   \coloneqq
  L_{lwe} gPSh(CartSp)
$$

for the [[(2,1)-category]] which is the [[simplicial localization]] of groupoid-valued presheaves at the local weak equivalences.

An [[object]] $X \in Smooth1Type$ we call a **[[smooth groupoid]]** or
**[[smooth homotopy type|smooth homotopy 1-type]]**.

=--


+-- {: .num_example }
###### Example

Every [[smooth space]] is canonically a [[smooth groupoid]] with only identity morphisms.

=--

+-- {: .num_prop }
###### Proposition

The canonical identification yields a [[full subcategory]]

$$
  Smooth0Type \hookrightarrow Smooth1Type
  \,.
$$

=--

+-- {: .num_example }
###### Example

For $X$ a [[smooth space]] and $G$ a [[smooth group]] and 

$$\rho : X \times G \to X
$$ 

an [[action]] then  the [[action groupoid]]
 
$$
  X \sslash G \in Smooth1Type

$$

$$
  X \sslash G = 
  \left(
    X \times G 
     \stackrel{\overset{\rho}{\longrightarrow}}{\underset{p_1}{\longrightarrow}}
    X
  \right)
$$

is a [[smooth groupoid]].

=--

##### Smooth path groupoid

* [[smooth path groupoid]]

##### Differential 1-forms are smooth incremental path measures
 {#1FormsAsSmoothFunctors}

We give a more intrinsic characterization of [[differential 1-forms]].

+-- {: .num_defn #SmoothPath}
###### Definition

A **smooth path with sitting instants** in $\mathbb{R}^k$ is a [[smooth function]] $\gamma \colon \mathbb{R} \to \mathbb{R}^k$ such 

1. the value of $\gamma$ converges to two points $x = \underset{t \to -\infty}{\lim} \gamma \in \mathbb{R}^k$ and $y = \underset{t \to \infty}{\lim} \gamma \in \mathbb{R}^k$;

1. the value of all [[derivatives]] of $\gamma$ converges to 0 at $t \to \pm \infty$.

A **localized diffeomorphism** $\phi \colon \mathbb{R} \to \mathbb{R}$ is a [[diffeomorphism]] such that there is an an open ball in $\mathbb{R}$ outside of which $\phi$ restricts to the identity.

Write

$$
  [\mathbb{R}, \mathbb{R}^k]\sslash Diff(\mathbb{R}) 
  \in 
  Smooth0Type
$$

for the smooth quotient space of smooth paths modulo localized diffeomorphism.

=--

+-- {: .num_defn #SmoothFunctorOnPathsInRkWithValuesInBR}
###### Definition

Say that a **smooth functor** $\mathbf{P}_1(\mathbb{R}^k) \to \mathbf{B}\mathbb{R}$ from the [[smooth path groupoid]] of $\mathbb{R}^k$ is

* a [[homomorphism]] of smooth space 

  $$
    S \colon [\mathbb{R}, \mathbb{R}^k] \to \mathbb{R}
  $$

* such that 

  1. composition of paths $\gamma_1, \gamma_2$ is sent to addition in $\mathbb{R}$

     $$
       S(\gamma_2\circ \gamma_1) = S(\gamma_1) + S(\gamma_2)
       \,.
     $$
  
  1. the constant path is sent to 0.

=--

+-- {: .num_prop }
###### Proposition

There is an [[equivalence]]

$$
  [\mathbf{P}_1(-), \mathbf{B}\mathbb{R}]
  \stackrel{\overset{\int_{(-)}(-)}{\leftarrow}}{\underset{}{\to}}
  DK(C^\infty(-) \stackrel{\mathbf{d}}{\to} \Omega^1(-)
  \,.
$$

=--

([SchreiberWaldorf](#SchreiberWaldorf)).

#### $\infty$-Groupoids and Kan complexes

An [[∞-groupoid]] is first of all supposed to be a structure that has [[k-morphism]]s for all $k \in \mathbb{N}$, which for $k \geq 1$ go between $(k-1)$-morphisms. A useful tool for organizing such collections of morphisms is the notion of a [[simplicial set]]. This is a [[functor]] on the [[opposite category]] of the  [[simplex category]] $\Delta$, whose objects are the abstract cellular $k$-[[simplex|simplices]], denoted $[k]$ or $\Delta[k]$ for all $k \in \mathbb{N}$, and whose morphisms $\Delta[k_1] \to \Delta[k_2]$ are all ways of mapping these into each other. So we think of such a simplicial set given by a functor

$$
  K : \Delta^{op} \to Set
$$

as specifying

* a set $[0] \mapsto K_0$ of [[object]]s;

* a set $[1] \mapsto K_1$ of [[morphism]];

* a set $[2] \mapsto K_2$ of [[2-morphism]];

* a set $[3] \mapsto K_3$ of [[3-morphism]];

and generally

* a set $[k] \mapsto K_k$ of [[k-morphism]]s

as well as specifying

* functions $([n] \hookrightarrow [n+1]) \mapsto (K_{n+1} \to K_n)$
  that send $n+1$-morphisms to their boundary $n$-morphisms;

* functions $([n+1] \to [n]) \mapsto (K_{n} \to K_{n+1})$
  that send $n$-morphisms to [[identity]] $(n+1)$-morphisms
  on them.

The fact that $K$ is supposed to be a [[functor]] enforces that these assignments of sets and functions satisfy conditions that make consistent our interpretation of them as sets of $k$-morphisms and source and target maps between these. 
These are called the [[simplicial identities]].

But apart from this source-target matching, a generic simplicial set does not yet encode a notion of [[composition]] of these morphisms. 

For instance for $\Lambda^1[2]$ the simplicial set consisting of two attached 1-cells 

$$
  \Lambda^1[2] = \left\{
    \array{
       && 1
       \\
       & \nearrow && \searrow
       \\
       0 &&&& 2
    }
  \right\}
$$

and for $(f,g) : \Lambda^1[2] \to K$ an image of this situation in $K$, hence a pair $x_0 \stackrel{f}{\to} x_1 \stackrel{g}{\to} x_2$ of two _composable_ 1-morphisms in $K$, we want to demand that there exists a third 1-morphisms in $K$ that may be thought of as the [[composition]] $x_0 \stackrel{h}{\to} x_2$ of $f$ and $g$. But since we are working in [[higher category theory]] (and not to be [[evil]]), we want to identify this composite only up to a [[2-morphism]] equivalence

$$
    \array{
       && x_1
       \\
       & {}^{\mathllap{f}}\nearrow &\Downarrow^{\mathrlap{\simeq}}& 
       \searrow^{\mathrlap{g}}
       \\
       x_0 &&\stackrel{h}{\to}&& x_2
    }
  \,.
$$

From the picture it is clear that this is equivalent to demanding that for $\Lambda^1[2] \hookrightarrow \Delta[2]$ the obvious inclusion of the two abstract composable 1-morphisms into the 2-simplex we have a diagram of morphisms of simplicial sets

$$
  \array{
    \Lambda^1[2] &\stackrel{(f,g)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists h}}
    \\
    \Delta[2]
  }
  \,.
$$

A simplicial set where for all such $(f,g)$ a corresponding such $h$ exists may be thought of as a collection of higher morphisms that is equipped with a notion of composition of adjacent 1-morphisms. 

For the purpose of describing [[groupoid]]al composition, we now want that this composition operation has all [[inverse]]s. For that purpose, notice that for 

$$
  \Lambda^2[2] = \left\{
    \array{
       && 1
       \\
       & && \searrow
       \\
       0 &&\to&& 2
    }
  \right\}
$$

the simplicial set consisting of two 1-morphisms that touch at their end, hence for 

$$
  (g,h) : \Lambda^2[2] \to K
$$

two such 1-morphisms in $K$, then if $g$ had an inverse $g^{-1}$ we could use the above composition operation to compose that with $h$ and thereby find a morphism $f$ connecting the sources of $h$ and $g$. This being the case is evidently equivalent to the existence of diagrams of morphisms of simplicial sets of the form

$$
  \array{
    \Lambda^2[2] &\stackrel{(g,h)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists f}}
    \\
    \Delta[2]
  }
  \,.
$$

Demanding that all such diagrams exist is therefore demanding that we have on 1-morphisms a composition operation with inverses in $K$. 

In order for this to qualify as an $\infty$-groupoid, this composition operation needs to satisfy an [[associativity law]] up to [[coherent]] [[2-morphism]]s, which means that we can find the relevant [[tetrahedra]]s in $K$. These in turn need to be connected by _pentagonators_ and ever so on.  It is a nontrivial but true and powerful fact, that all these [[coherence]] conditions are captured by generalizing the above conditions to all dimensions in the evident way:

let $\Lambda^i[n] \hookrightarrow \Delta[n]$ be the simplicial set -- called the $i$th $n$-[[horn]] -- that consists of all cells of the $n$-[[simplex]] $\Delta[n]$ except the interior $n$-morphism and the $i$th $(n-1)$-morphism.

Then a simplicial set is called a [[Kan complex]], if for all images $f : \Lambda^i[n] \to K$ of such horns in $K$, the missing two cells can be found in $K$- in that we can always find a _horn filler_ $\sigma$ in the diagram

$$
  \array{
     \Lambda^i[n] &\stackrel{f}{\to}& K
     \\
     \downarrow & \nearrow_{\mathrlap{\sigma}}
     \\
     \Delta[n]
  }
  \,.
$$

The basic example is the [[nerve]] $N(C) \in sSet$ of an ordinary [[groupoid]] $C$, which is the [[simplicial set]] with $N(C)_k$ being the set of sequences of $k$ composable morphisms in $C$. The nerve operation is a [[full and faithful functor]]  from 1-groupoids into Kan complexes and hence may be thought of as embedding 1-groupoids in the context of general [[∞-groupoid]]s.

#### Model categories

* [[model structure on simplicial sets]]

* [[model structure on simplicial presheaves]]

#### Cohesive $\infty$-Groupoids and locally Kan simplicial presheaves

But we need a bit more than just bare [[∞-groupoid]]s. In generalization to [[Lie groupoid]]s, we need [[∞-Lie groupoid]]s. A useful way to encode that an $\infty$-groupoid has extra structure modeled on geometric test objects that themselves form a category $C$ is to remember the rule which for each test space $U$ in $C$ produces the $\infty$-groupoid of $U$-parameterized families of $k$-morphisms in $K$.  For instance for an [[∞-Lie groupoid]] we could test with each [[Cartesian space]] $U = \mathbb{R}^n$ and find the $\infty$-groupoids $K(U)$ of smooth $n$-parameter families of $k$-morphisms in $K$.

This data of $U$-families arranges itself into a [[presheaf]] with values in Kan complexes

$$
  K : C^{op} \to KanCplx \hookrightarrow sSet
$$

hence with values in simplicial sets. This is equivalently a [[simplicial presheaf]] of sets. The [[functor category]] $[C^{op}, sSet]$ on the [[opposite category]] of the category of test objects $C$ serves as a model for the [[(∞,1)-category]] of $\infty$-groupoids with $C$-structure.

While there are no [[higher morphism]]s in this functor 1-category that could for instance witness that two $\infty$-groupoids are not [[isomorphic]], but still [[equivalence of categories|equivalent]], it turns out that all one needs in order to reconstruct _all_ these higher morphisms (up to equivalence!) is just the information of which morphisms of simplicial presheaves would become invertible if we were keeping track of higher morphism. These would-be invertible morphisms are called _weak equivalences_ and denoted $K_1 \stackrel{\simeq}{\to} K_2$. 

For common choices of $C$ there is a well-understood way to define the weak equivalences $W \subset mor [C^{op}, sSet]$, and equipped with this information the category of simplicial presheaves becomes a _[[category with weak equivalences]]_ . There is a well-developed but somewhat intricate theory of how exactly this 1-cagtegorical data models the full higher category of structured groupoids that we are after, but for our purposes we essentially only need to work inside the [[category of fibrant objects]] of a [[model category]] structure [[model structure on simplicial presheaves|on simplicial presheaves]], which in practice amounts to the fact that we use the following three basic constructions:

1. **[[∞-anafunctor]]s** -- A morphisms $X \to Y$ between $\infty$-groupoids with $C$-structure is not just a morphism $X\to Y$ in $[C^{op}, sSet]$, but is a [[span]] of such ordinary morphisms

   $$
     \array{  
        \hat X &\to& Y
        \\
        \downarrow^{\mathrlap{\simeq}}
        \\
        X
     }
   $$

   where the left leg is a weak equivalence. This is sometimes called an _$\infty$-anafunctor_ from $X$ to $Y$.
 
1. **[[homotopy pullback]]** -- For $A \to B \stackrel{p}{\leftarrow} C$ a [[diagram]], the [[(∞,1)-pullback]] of it is the ordinary [[pullback]] in $[C^{op}, sSet]$ of a replacement diagram $A \to B \stackrel{\hat p}{\leftarrow} \hat C$, where $\hat p$ is a _good replacement_  of $p$ in the sense of the following factorization lemma.

1. **[[factorization lemma]]** -- For $p : C \to B$ a morphism in $[C^{op}, sSet]$, a _good replacement_ $\hat p : \hat C \to B$ is given by the composite vertical morphism in the ordinary [[pullback]] diagram

   $$
     \array{
       \hat C &\to& C
       \\
       \downarrow && \downarrow^{\mathrlap{p}}
       \\
       B^{\Delta[1]} &\to& B
       \\
       \downarrow
       \\
       B
     }
     \,,
   $$

  where $B^{\Delta[1]}$ is the [[path object]] of $B$: 
  the simplicial presheaf that is over each $U \in C$ the
  simplicial path space $B(U)^{\Delta[1]}$.

* [[simplicial presheaf]]

* [[model structure on simplicial presheaves]]

##### Good covers and split hypercovers

* [[Cech nerve]]

* [[good open cover]]

* [[split hypercover]]

+-- {: .num_prop #DifferentiablyGoodCoverGivesSPlitHyperCoverOverCartSp}
###### Proposition

For $X$ a [[smooth manifold]] let $\{U_i \hookrightarrow X\}_i$ be an [[open cover]]. This is a _differentiably good open cover_, def. \ref{DifferentiallyGoodOpenCover}, precisely if the corresponding  [[Cech nerve]] $C(\{U_i\}) \to X$ in $sPh(CartSp)_{proj,loc}$ is a [[split hypercover]].

=--



### Semantic Layer
 {#SmoothHomotopyTypesSemanticLayer}

#### $\infty$-Toposes

* [[(∞,1)-topos]]

##### Slice $\infty$-toposes
 {#SlicedInfinityToposes}

* [[slice (∞,1)-topos]]


##### Local, $\infty$-connected and cohesive $\infty$-toposes

* [[local (∞,1)-topos]] $(\flat \dashv \sharp)$

* [[locally ∞-connected (∞,1)-topos]] $(\mathbf{\Pi} \dashv \flat)$

* [[cohesive (∞,1)-topos]] $(\mathbf{\Pi} \dashv \flat \dashv \sharp)$

[[!include cohesion - table]]

Some terminology:

+-- {: .num_defn #ShapeTerminology}
###### Definition

For $X \in \mathbf{H}$ locally $\infty$-connected, we say $\mathbf{\Pi}(X)$ is the **[[shape]] of $X$**. If $\mathbf{H}$ is in addition cohesive we also say that $\mathbf{\Pi}(X)$ is the **[[geometric realization]]** of $X$ or the **[[fundamental ∞-groupoid]]** of $X$.

If $\mathbf{\Pi}(X) \simeq *$ we say that $X$ is **geometrically contractible**.

=--


#### The $\infty$-topos of smooth $\infty$-groupoids

* [[Lie groupoid]], [[differentiable stack]]

* [[smooth ∞-groupoid]]

##### Local $\infty$-Connectedness   {#InfinityConnectednessOfSmoothInfinityGrpd}

(...)

##### Locality 

(...)

##### Cohesion 

(...)

### Syntactic Layer
 {#SmoothHomotopyTypesSyntacticLayer}

#### Identity types
 {#IdentityTypes}

* [[identity type]]



#### Homotopy type theory

* [[h-level]]


* [[homotopy type theory]]


#### Cohesive modality II: flat types

**flat type** $\flat A$

maps $X \to \flat \mathbf{B}G$ are flat $G$-connections


$$
  \mathbf{B}G \colon Type
  \;\vdash\;
  UnderlyingBundle_{\mathbf{B}G} \colon \flat \mathbf{B}G \to \mathbf{B}G
$$
