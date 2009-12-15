<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

# Defnition #

+-- {: .un_defn}
###### Definition
A **lined topos** $(\mathcal{T}, R)$ is

* a [[ringed topos]] $(\mathcal{T}, k)$
 
  (usually with the [[internalization|internal]] [[ring]] object $(k,+,\cdot)$ assumed to be commutative)

* and equipped with a choice $(R,+,\cdot)$ of [[internalization|internal]] commutative [[algebra]] object $(R,+,\cdot)$ over $k$ -- the **line object**.

=--


# Variations #

* A [[smooth topos]] is a lined topos where the line is required to be a smooth differentiable space with [[infinitesimal object|infinitesimal]] subspaces in a certain way. This is the basic type of object studied in [[synthetic differential geometry]].

* A [[super smooth topos]] is a lined topos that is a [[smooth topos]] and in which the $k$-algebra structure on $R$ is refined to that of a $k$-[[superalgebra]].



# Constructions in lined toposes #

## Path objects 

The line object $R$ in a lined topos $\mathcal{T}$ canonically has the structure of a [[interval object|cartesian interval object]]. 

As described there, this canonically induces 

* a [[cosimplicial object]] $\Delta_R : \Delta \to \mathcal{T}$

* a functor $\Pi : \mathcal{T} \to S \mathcal{T}$

  that sends each object in the topos to a [[simplicial object]]

  $$
    X \mapsto $X^{\Delta_R^\bullet}$
  $$

  ( which may be interpreted as presenting the 
    [[schreiber:path ∞-groupoid|path ∞-groupoid]] of $X$).


## Contractible objects {#ContractibleObjects}

The following terminology is sometimes useful.

+-- {: .un_defn}
###### Terminology
**(contractible object)**

Let $(\mathcal{T} = Sh(C), R)$ be a lined [[Grothendieck topos]] with respect to a [[site]] $C$.

Call an object $X \in \mathcal{T}$  **contractible** with respect to the [[interval object]] $R$, if the [[simplicial presheaf|simplicial sheaf]] $\Pi(X) = X^{\Delta_R^\bullet} : C^{op} \to$ [[SSet]] sends each object to a [[contractible space|contractible]] [[simplicial set]].

=--

**Examples**

* Let $Top'$ be a [[small category|small]] version of the category of sufficiently nice [[topological space]]s, for instance connected [[CW complex]]es. The canonical line object in $Sh(Top)$ is ${*} \stackrel{0}{\to} [0,1] \stackrel{1}{\leftarrow} {*}$ the standard topological interval. For $X \in Top$, $\Pi(X) = X^{\Delta_R^\bullet}$ is the [[singular simplicial complex]] of $X$.  This is contractible in the above sense precisely if $X$ is a [[contractible space]] in the standard sense.

* Let [[CartSp]] be the full subcategory of [[Diff]] on smooth [[manifold]]s of the form $\mathbb{R}^n$, for $n \in \mathbb{N}$. The canonical line object in $\mathcal{T} = Sh(CartSp)$ is the real line regarded as an [[interval object]]

  $$
    R = ({*} \stackrel{0}{\to} \mathbb{R} \stackrel{1}{\leftarrow} {*})
    \,.
  $$

  +-- {: .num_lemma}
  ###### Lemma
 
  In the lined topos $(\mathcal{T} = Sh(CartSp), R = \mathbb{R})$ 
  the [[representable functor|representable]] 
  objects $\mathbb{R}^n$ are contractible with respect to $R$.

  =--

  +-- {: .proof}
  ###### Proof

  This is not quite as entirely trivial as it may seem on first sight, 
  but follows directly from the [[Tietze extension theorem]] 
  for smooth manifolds:

  we check that for all $V \in $ [[CartSp]] 
  every  [[boundary of a simplex]] 
  $\partial \Delta[k] \to \Pi(\mathbb{R}^n)(V)$ extends through
  $\partial \Delta[k] \hookrightarrow \Delta[k]$:

  by the [construction of the cosimplicial object](http://ncatlab.org/nlab/show/interval+object#FundGeomInftCat) 
  $\Delta_R : \Delta \to Sh(CartSp)$ we have that morphisms 
  $\partial \Delta[k] \to \Pi(\mathbb{R}^n)(V)$ correspond to smooth 
  maps from the
  boundary of a $V$-cylinder over the
  standard $k$-simplex in $\mathbb{R}^k \times V 
  \to \mathbb{R}^n$.
  Since this is a closed subset of $\mathbb{R}^k \times V$, 
  by the [[Tietze extension theorem]] these maps extend (apply the theorem
  to each of their components) to all of $\mathbb{R}^k \times V$, 
  hence in particular
  to the standard $k$-simplex inside $\mathbb{R}^k$ defined by the 
  interval object. This constitutes the required extension to a 
  $V$-family of $k$-simplices in $\mathbb{R}^n$

  $$
    \array{
      \partial \Delta[n] &\to& (\mathbb{R}^n)^{\Delta_R^\bullet}(V)
      \\
      \downarrow & \nearrow
      \\
      \Delta[n]
    }
    \,.
  $$
 

  =--

