
> This entry contains one chapter of the material at _[[geometry of physics]]_.

> previous chapter: _[[geometry of physics -- smooth sets|smooth sets]]_

> next chapter: _[[geometry of physics -- integration|integration]]_

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


## **Differentiation**
 {#Differentiation}

We introduce the standard concept of _[[nLab:differential forms]]_ in _[Model Layer](#DifferentialFormsLayerMod)_, adding to the traditional discussion a precise version of the statement that differential forms are equivalently "incremental smooth $n$-dimensional measures", which accurately captures the role that they play in [[physics]], notably in [[local action functionals]].

We define differential forms on general smooth spaces seamlessly in terms of the smooth [[moduli space]] $\Omega^\in \in Smooth0Type$ of differential forms. This has the special property that it is, for $n \geq 1$, a _non-[[concrete object|concrete]]_ smooth space. In _[Semantic Layer](#DifferentialFormsLayerSem)_ below we take this as occasion to discuss the notion of [[concrete objects]] in a [[local topos]], such as the topos of smooth spaces. We show how the _concretification_ of the smooth mapping space $[X,\Omega^n]$ for any smooth space $X$ is the _smooth (moduli) space of differential forms on $X$_. Below in _[Action functionals for Chern-Simons type gauge theories](#ActionFunctionalsForChernSimonsTypeGaugeTheories)_ the theory of _concretification_ in a local topos is a central ingredient in the _canonical existence_ of certain [[nLab:action functionals]].

The process of concretification involves the general abstract notion of _[[image|images]]_. The type-theory of this notion we discuss in [Syntactic Layer](#DifferentialFormsLayerSyn) here.


### Model Layer
 {#DifferentialFormsLayerMod}

We have seen above in _[The continuum real (world-)line](TheContinuumRealWorldLine)_ that that [[real line]] $\mathbb{R}$ is the basic [[kinematics|kinematical structure]] in the [[differential geometry]] of [[physics]]. Notably the smooth [[path spaces]] $[\mathbb{R}, X]$ from example \ref{SmoothPathSpace} are to be thought of as the smooth spaces of _trajectories_ (for instance of some [[particle]]) in a [[smooth space]] $X$, hence of smooth maps $\mathbb{R} \to X$.

But moreover, _[[dynamics]]_ in [[physics]]  is encoded by _[[linear functionals|functionals]] on such trajectories_: by "[[action functionals]]". In the simplest case these are for instance homomorphisms of smooth spaces

$$
  S \colon \left[I, X\right] \to \mathbb{R}
  \,,
$$

where $I \hookrightarrow \mathbb{R}$ is the standard unit [[interval]].

Such [[action functionals]] we discuss in their own right in _[Variational calculus](#VariationalCalculus)_ below. Here we first examine in detail a fundamental property they all have: they are supposed to be _[[local action functional|local]]_.

Foremost this means that the value associated to a trajectory is _built up incrementally_ from small contributions associated to small sub-trajectories: if a trajectory $\gamma$ is decomposed as a trajectory $\gamma_1$ followed by a trajectory $\gamma_2$, then the action functional is additive

$$
  S(\gamma) = S(\gamma_1) + S(\gamma_2)
  \,.
$$

As one takes this property to the limit of iterative subdivision, one finds that action functionals are entirely determined by their value on _[[infinitesimal space|infinitesimal]] displacements_ along the worldline. If $\gamma \colon \mathbb{R} \to X$ denotes a path and "$\dot \gamma(x)$" denotes the corresponding "infinitesimal path" at worldline parameter $x$, then the value of the action functional on such an infinitesimal path is traditionally written as

$$
  \mathbf{d}S(\dot \gamma)_x  \in \mathbb{R}
  \,,
$$

to be read as "the small change $\mathbf{d}S$ of $S$ along the infinitesimal path $\dot \gamma_x$". 

This function $\mathbf{d}S$ that assigns numbers to infinitesimal paths is called a _[[differential form]]_. Etymologically this originates in the use of "form" as in _[[bilinear form]]_: something that is evaluated. Here it is evaluated on _infinitesimal differences_, referred to as _differentials_.



We define smooth differential forms on [[Cartesian spaces]] in 

* _[Differential forms on abstract coordinate sysetms](#DifferentialFormsOnAbstractCoordinateSystem)_

Then we discuss how this induces a notion of smooth differential forms on general [[smooth spaces]] in 

* _[Smooth universal moduli space of differential forms](#SmoothUniversalModuliSpaceOfDifferentialForms)_.

Further below we provide a precise version of the statement that "Differential 1-forms are differential measures along paths." in 

* _[Differential 1-forms are smooth incremental path measures](#1FormsAsSmoothFunctors)_.


#### Differential forms on abstract coordinate systems
 {#DifferentialFormsOnAbstractCoordinateSystem}

We introduce the basic concept of a smooth [[differential form]] on a [[Cartesian space]] $\mathbb{R}^n$. Below in _[Differential forms on smooth spaces](#SmoothUniversalModuliSpaceOfDifferentialForms)_ we use this to define differential forms on any [[smooth space]].

+-- {: .num_defn #Differential1FormsOnCartesianSpaces}
###### Definition

For $n \in \mathbb{N}$ a **[[smooth differential 1-form]]** $\omega$ on a [[Cartesian space]] $\mathbb{R}^n$ is an $n$-[[tuple]] 

$$
  \left(\omega_i \in CartSp\left(\mathbb{R}^n,\mathbb{R}\right)\right)_{i = 1}^n
$$

of [[smooth functions]], which we think of equivalently as the [[coefficients]] of a [[formal linear combination]]

$$
  \omega = \sum_{i = 1}^n f_i \mathbf{d}x^i
$$

on a [[set]] $\{\mathbf{d}x^1, \mathbf{d}x^2, \cdots, \mathbf{d}x^n\}$ of [[cardinality]] $n$.

Write 

$$
  \Omega^1(\mathbb{R}^k) \simeq CartSp(\mathbb{R}^k, \mathbb{R})^{\times k}\in Set
$$

for the set of smooth [[differential 1-forms]] on $\mathbb{R}^k$.

=--

+-- {: .num_remark}
###### Remark

We think of $\mathbf{d} x^i$ as a measure for [[infinitesimal space|infinitesimal]] displacements along the $x^i$-[[coordinate]] of a [[Cartesian space]]. This idea is made precise below in _[Differential 1-forms are smooth increnemental path measures](#1FormsAsSmoothFunctors)_.

=--

If we have a measure of infintesimal displacement on some $\mathbb{R}^n$ and a smooth function $f \colon \mathbb{R}^{\tilde n} \to \mathbb{R}^n$, then this induces a measure for infinitesimal displacement on $\mathbb{R}^{\tilde n}$ by sending whatever happens there first with  $f$ to $\mathbb{R}^n$ and then applying the given measure there. This is captured by the following definition.

+-- {: .num_defn #PullbackOfDifferential1FormsOnCartesianSpaces}
###### Definition

For $\phi \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^k$ a [[smooth function]], the **[[pullback of differential forms|pullback of differential 1-forms]]** along $\phi$ is the [[function]]

$$
  \phi^* \colon \Omega^1(\mathbb{R}^{k}) \to \Omega^1(\mathbb{R}^{\tilde k})
$$

between sets of differential 1-forms, def. \ref{Differential1FormsOnCartesianSpaces}, which is defined on [[basis]]-elements by

$$
  \phi^* \mathbf{d} x^i \coloneqq \sum_{j = 1}^{\tilde k} \frac{\partial \phi^i}{\partial \tilde x^j} \mathbf{d}\tilde x^j
$$

and then extended linearly by

$$
  \begin{aligned}
    \phi^* \omega & = \phi^* \left( \sum_{i} \omega_i \mathbf{d}x^i \right)
    \\
    & \coloneqq
     \sum_{i = 1}^k \left(\phi^* \omega\right)_i \sum_{j = 1}^{\tilde k} \frac{\partial \phi^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
    \\
    & = 
     \sum_{i = 1}^k  \sum_{j = 1}^{\tilde k} (\omega_i \circ \phi) \cdot \frac{\partial \phi^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The term "pullback" in _[[pullback of differential forms]]_ is not really related, certainly not historically, to the term _[[pullback]]_ in [[category theory]]. One can relate the pullback of differential forms to categorical pullbacks, but this is not really essential here. The most immediate property that both concepts share is that they take a [[morphism]] going in one direction to a map between structures over domain and codomain of that morphism which goes in the other direction, and in this sense one is "pulling back structure along a morphism" in both cases.

=--

Even if in the above definition we speak only about the [[set]] $\Omega^1(\mathbb{R}^k)$ of differential 1-forms, this set naturally carries further [[structure]].

+-- {: .num_defn #ModuleStructureOn1FormsOnRk}
###### Definition

1. The set $\Omega^1(\mathbb{R}^k)$ is naturally an [[abelian group]] with addition given by componentwise addition

   $$
      \begin{aligned}
         \omega + \lambda & =
          \sum_{i = 1}^k \omega_i \mathbf{d}x^i + \sum_{j = 1}^k \lambda_j \mathbf{d}x^j
         \\
         & = \sum_{i = 1}^k(\omega_i + \lambda_i) \mathbf{d}x^i
      \end{aligned}
      \,,
   $$

1. The abelian group $\Omega^1(\mathbb{R}^k)$ is naturally equipped with the structure of a [[module]] over the [[ring]] $C^\infty(\mathbb{R}^k,\mathbb{R}) = CartSp(\mathbb{R}^k, \mathbb{R})$ of [[smooth functions]], where the [[action]] $C^\infty(\mathbb{R}^k,\mathbb{R}) \times\Omega^1(\mathbb{R}^k) \to \Omega^1(\mathbb{R}^k)$ is given by componentwise multiplication

   $$
     f \cdot \omega = \sum_{i = 1}^k( f \cdot \omega_i) \mathbf{d}x^i
     \,.
   $$

=--

+-- {: .num_defn }
###### Remark

More abstractly, this just says that $\Omega^1(\mathbb{R}^k)$ is the [[free module]] over $C^\infty(\mathbb{R}^k)$ on the set $\{\mathbf{d}x^i\}_{i = 1}^k$.

=--

The following definition captures the idea that if $\mathbf{d} x^i$ is a measure for displacement along the $x^i$-[[coordinate]], and $\mathbf{d}x^j$ a measure for displacement along the $x^j$ coordinate, then there should be a way te get a measure, to be called $\mathbf{d}x^i \wedge \mathbf{d} x^j$, for infinitesimal _surfaces_ (squares) in the $x^i$-$x^j$-plane. And this should keep track of the [[orientation]] of these squares, whith 

$$
  \mathbf{d}x^j \wedge \mathbf{d}x^i = - \mathbf{d}x^i \wedge \mathbf{d} x^j
$$

being the same infinitesimal measure with orientation reversed.

+-- {: .num_defn #DifferentialnForms}
###### Definition

For $k,n \in \mathbb{N}$, the **smooth [[differential forms]]** on $\mathbb{R}^k$ is the [[exterior algebra]]

$$
  \Omega^\bullet(\mathbb{R}^k) 
   \coloneqq
  \wedge^\bullet_{C^\infty(\mathbb{R}^k)} \Omega^1(\mathbb{R}^k)
$$

over the [[ring]] $C^\infty(\mathbb{R}^k)$ of [[smooth functions]] of the [[module]] $\Omega^1(\mathbb{R}^k)$ of smooth 1-forms, prop. \ref{ModuleStructureOn1FormsOnRk}.

We write $\Omega^n(\mathbb{R}^k)$ for the sub-module of degree $n$ and call its elements the **smooth [[differential n-forms]]**.

=--

+-- {: .num_remark}
###### Remark

Explicitly this means that a [[differential n-form]] $\omega \in \Omega^n(\mathbb{R}^k)$ on $\mathbb{R}^k$ is a [[formal linear combination]] over $C^\infty(\mathbb{R}^k)$ of [[basis]] elements of the form $\mathbf{d} x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n}$ for $i_1 \lt i_2 \lt \cdots \lt i_n$:

$$
  \omega = \sum_{1 \leq i_1 \lt i_2 \lt \cdots \lt i_n \lt k} \omega_{i_1, \cdots, i_n} \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n}
  \,.
$$


=--

+-- {: .num_defn #PullbackOfDifferentialForms}
###### Definition

The [[pullback of differential forms|pullback of differential 1-forms]] of def. \ref{Differential1FormsOnCartesianSpaces} extends as an $C^\infty(\mathbb{R}^k)$-[[associative algebra|algebra]] [[homomorphism]] to $\Omega^n(-)$, given for a smooth function $f \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^k$ on basis elements by

$$
  f^* \left(  \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n} \right)
  = 
  \left(f^* \mathbf{d}x^{i_1} \wedge \cdots \wedge f^* \mathbf{d}x^{i_n} \right)
  \,. 
$$ 

=--


#### Differential forms on smooth spaces
 {#SmoothUniversalModuliSpaceOfDifferentialForms}

Above we have defined differential $n$-form on abstract coordinate systems. Here we extend this definition to one of differential $n$-forms on arbitrary [[smooth spaces]]. We start by observing that the space of _all_ differential $n$-forms on cordinate systems themselves naturally is a smooth space.

+-- {: .num_prop}
###### Proposition

The assignment of differential $n$-forms

$$
  \Omega^n(-) \colon \mathbb{R}^k \mapsto \Omega^n(\mathbb{R}^k)
$$

of def. \ref{DifferentialnForms} together with the [[pullback of differential forms]]-functions of def. \ref{PullbackOfDifferentialForms}

$$
  \array{
    \mathbb{R}^{k_1} &\mapsto & \Omega^1(\mathbb{R}^{k_1})
    \\
    \uparrow^{\mathrlap{f}} && \downarrow^{\mathrlap{f^*}}
    \\
    \mathbb{R}^{k_2} &\mapsto& \Omega^1(\mathbb{R}^{k_2})
  }
$$

defines a [[smooth space]] in the sense of def. \ref{SmoothSpace}:

$$
  \Omega^n(-) \in Smooth0Type
  \,.
$$

=--

+-- {: .num_defn #SmoothModuliSpaceOfnForms}
###### Definition


We call this 

$$
  \Omega^n \colon Smooth0Type
$$

the **universal smooth [[moduli space]]** of differential $n$-forms. 

=--

The reason for this terminology is that homomorphisms of smooth spaces into $\Omega^1$ _modulate_ differential $n$-forms on their [[domain]], by prop. \ref{YonedaForSmoothSpaces} (and hence by the [[Yoneda lemma]]):

+-- {: .num_example}
###### Example

For the [[Cartesian space]] $\mathbb{R}^k$ regarded as a smooth space by example \ref{CartesianSpaceAsSmoothSpace}, there is a [[natural bijection]]

$$
  \Omega^n(\mathbb{R}^k) \simeq Hom(\mathbb{R}^k, \Omega^1)
$$

between the set of smooth $n$-forms on $\mathbb{R}^n$ according to def. \ref{Differential1FormsOnCartesianSpaces} and the set of homomorphism of smooth spaces, $\mathbb{R}^k \to \Omega^1$, according to def. \ref{HomomorphismOfSmoothSpaces}.

=--

In view of this we have the following elegant definition of smooth $n$-forms on an arbitrary smooth space.

+-- {: .num_defn #DifferentialnFormOnSmoothSpace}
###### Definition

For $X \in Smooth0Type$ a [[smooth space]], def. \ref{SmoothSpace}, a **[[differential n-form]]** on $X$ is a [[homomorphism]] of [[smooth spaces]] of the form

$$
  \omega \colon X \to \Omega^n(-)
  \,.
$$

Accordingly we write

$$
  \Omega^n(X) \coloneqq Smooth0Type(X,\Omega^n)
$$

for the set of smooth $n$-forms on $X$.

=--

We may unwind this definition to a very explicit description of differential forms on smooth spaces. This we do in a moment in remark \ref{DifferentialFormOnSmoothSpaceAsSystemOfDiffFormsOnCoordinates}.

Notice that differential 0-forms are equivalently smooth $\mathbb{R}$-valued functions.

+-- {: .num_prop #SpaceOf0FormsIsRealLine}
###### Proposition

$\Omega^0 \simeq \mathbb{R}$

=--


+-- {: .num_defn #PullbackOfDifferentialFormsOnSmoothSpaces}
###### Definition

For $f \colon X \to Y$ a [[homomorphism]] of [[smooth spaces]], def. \ref{HomomorphismOfSmoothSpaces}, the **[[pullback of differential forms]]** along $f$ is the [[function]]

$$
  f^* \colon \Omega^n(Y) \to \Omega^n(X)
$$

given by the [[hom-functor]] into the smooth space $\Omega^n$ of def. \ref{SmoothModuliSpaceOfnForms}:

$$
 f^* \coloneqq Hom(-, \Omega^n)
 \,.
$$

This means that it sends an $n$-form $\omega \in \Omega^n(Y)$ which is modulated by a homomorphism $Y \to \Omega^n$ to the $n$-form $f^* \omega \in \Omega^n(X)$ which is modulated by the [[composition|composite]] $X \stackrel{f}{\to} Y \to \Omega^n$.

=--

+-- {: .num_defn}
###### Proposition

For $X = \mathbb{R}^{\tilde k}$ and $Y = \mathbb{R}^{k}$ definition \ref{PullbackOfDifferentialFormsOnSmoothSpaces} reproduces def. \ref{PullbackOfDifferentialForms}.

=--

+-- {: .proof}
###### Proof

Again by the [[Yoneda lemma]].

=--

+-- {: .num_remark #DifferentialFormOnSmoothSpaceAsSystemOfDiffFormsOnCoordinates}
###### Remark

Using def. \ref{PullbackOfDifferentialFormsOnSmoothSpaces}

Unwinding def. \ref{DifferentialnFormOnSmoothSpace} yields the following explicit description:

a differential $n$-form $\omega \in \Omega^n(X)$ on a smooth space $X$ is

1. for each way $\phi \colon \mathbb{R}^k \to X$ of laying out a coordinate system $\mathbb{R}^k$ in $X$ a differential $n$-form

   $$
     \phi^* \omega \in \Omega^n(\mathbb{R}^k)
   $$

   on the abstract coordinate system, as given by def. \ref{DifferentialnForms};

1. for each abstract [[coordinate transformation]] $f \colon \mathbb{R}^{k_2} \to \mathbb{R}^{k_1}$ a corresponding compatibility condition between local differential forms $\phi_1 \colon \mathbb{R}^{k_1} \to X$ and $\phi_2 \colon \mathbb{R}^{k_2} \to X$ of the form

   $$
     f^* \phi_1^* \omega = \phi_2^* \omega
     \,.
   $$

Hence a differential form on a smooth space is simply a collection of differential forms on all its coordinate systems such that these glue along all possible coordinate transformations.

=--


The following adds further explanation to the role of $\Omega^n \in Smooth0Tye$ as a _[[moduli space]]_. Notice that since $\Omega^n$ is itself a [[smooth space]], we may speak about differential $n$-forms on $\Omega^n$ itsefl.

+-- {: .num_defn #UniversalDifferentialnForm}
###### Definition

The **universal differential $n$-forms** is the differential $n$-form

$$
  \omega^n_{univ} \in \Omega^n(\Omega^n)
$$

which is modulated by the [[identity]] [[homomorphism]] $id \colon \Omega^n \to \Omega^n$.

=--

With this definition we have:

+-- {: .num_prop}
###### Proposition

For $X \in Smooth0Type$ any [[smooth space]], every differential $n$-form on $X$, $\omega \in \Omega^n(X)$ is the pullback of differential forms, def. \ref{PullbackOfDifferentialFormsOnSmoothSpaces}, of the universal differential $n$-form, def. \ref{UniversalDifferentialnForm}, along a homomorphism $f$ from $X$ into the moduli space $\Omega^n$ of differential $n$-forms:

$$
  \omega = f^* \omega^n_{univ}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This statement is of course in a way a big tautology. Nevertheless it is a very useful tautology to make explicit. The whole concept of differential forms on smooth spaces here may be thought of as simply a variation of the theme of the [[Yoneda lemma]].

=--

+-- {: bluebox }
###### 

This ends the Model-layer discussion of differential forms. We now pass to a more advanced discussion of this topic in the [Semantics layer below](#DifferentialFormsLayerSem). The reader wishing to stick to more elementary discussion for the time being should skip ahead to the Model-layer discussion of [differentiation below](#Differentiation). 

=--


### Semantic Layer
 {#DifferentialFormsLayerSem}

#### Concrete smooth spaces
 {#ConcreteObjects}

The smooth universal moduli space of differential forms $\Omega^n(-)$
from def. \ref{SmoothModuliSpaceOfnForms}
is noteworthy in that it has a property not shared by 
many smooth spaces that one might think of more naively: while evidently being "large" (the space of all differential forms!) it has "very few points" and "very few $k$-dimensional subspaces" for low $k$.  In fact 

+-- {: .num_prop}
###### Proposition

For $k \lt n$ the smooth space $\Omega^n$ admits only a unique probe by $\mathbb{R}^k$:

$$
  Hom(\mathbb{R}^k, \Omega^n(-))
  \simeq
  \Omega^n(\mathbb{R}^k)
  = 
  \{0\}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the [[Yoneda lemma]] a smooth morphism $\mathbb{R}^k \to \Omega^n$ is a [[differential n-form]] $\omega \in \Omega^n(\mathbb{R}^k)$. But for $n \gt k$ there is only the 0 element.

=--

So while $\Omega^n()$ is a large smooth space, it is "not supported on probes" in low dimensions in as much as one might expect, from more naive notions of smooth spaces.

We now formalize this. The formal notion of an smooth space which _is_ supported on its probes is that of a _[[concrete object]]_. There is a univeral map that sends any smooth space to its _concretification_. The universal moduli spaces of differential forms turn out to be _non-concrete_ in that their concetrification is the point.

+-- {: .num_defn #ConcreteObjectsAndConcretification}
###### Definition

Let $\mathbf{H}$ be a [[local topos]]. Write $\sharp \colon \mathbf{H} \to \mathbf{H}$ for the corresponding sharp modality, def. \ref{SharpModalityOfLocalTopos}. Then. 

1. An object $X \in \mathbf{H}$ is called a **[[concrete object]]** if

   $$
     DeCoh_X \colon X \to \sharp X
   $$

   is a [[monomorphism]].

1. For $X \in \mathbf{H}$ any object, its  **concretification** $Conc(X) \in \mathbf{H}$ is the [[image]] factorization of $DeCoh_X$, hence the factorization into an [[epimorphism]] followed by a [[monomorphism]]

   $$
     DeCoh_X : X \to Conc(X) \hookrightarrow \sharp X
     \,.
   $$

=--

+-- {: .num_remark}
###### Remark

Hence the concretification $Conc(X)$ of an object $X$ is itself a [[concrete object]] and it is [[universal property|universal]] with this property. (...)

=--

+-- {: .num_prop #DecohesOverASiteWithTerminalObject}
###### Proposition

Let $C$ be a [[site]] of definition for the [[local topos]]
$\mathbf{H}$, with [[terminal object]] $*$. Then for 
$X \colon C^{op} \to Set$ a sheaf, $DeCoh_X$
is given over $U \in C$ by

$$
  X(U)
  \underoverset{Yoneda}{\simeq}{\to}
  \mathbf{H}(U, X)
  \stackrel{\Gamma_{U,X}}{\to}
  Set(\Gamma(U),\Gamma(X))
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

For $n \geq 1$ we have 

$$
  Conc(\Omega^n) \simeq *
  \,.
$$

=--

In this sense the smooth moduli space of differential $n$-forms is _maximally non-concrete_.

#### Smooth moduli space of differential forms on a smooth space
 {#SmoothModuliSpaceOfDifferentialForms}

We discuss the smooth space of differential forms _on a fixed smooth space_ $X$. 

+-- {: .num_remark}
###### Remark

For $X$ a [[smooth space]], the smooth mapping space $[X, \Omega^n] \in Smooth0Type$ is the smooth space whose $\mathbb{R}^k$-plots are differential $n$-forms on the [[product]] $X \times \mathbb{R}^k$

$$
  [X, \Omega^n] \colon \mathbb{R}^k \mapsto \Omega^n(X \times \mathbb{R}^k)
  \,.
$$

This is not _quite_ what one usually wants to regard as an $\mathbb{R}^k$-parameterized of differential forms on $X$. That is instead usually meant to be a differential form $\omega$ on $X \times \mathbb{R}^k$ which has "no leg along $\mathbb{R}^k$". Another way to say this is that the family of forms on $X$ that is represented by some $\omega$ on $X \times \mathbb{R}^k$ is that which over a point $v \colon * \to \mathbb{RR}^k$ has the value $(id_X,v)^* \omega$. Under this [[pullback of differential forms]] any components of $\omega$ with "legs along $\mathbb{R}^k$" are identified with the 0 differential form 

=--

This is captured by the following definition.

+-- {: .num_defn #SmoothSpaceOfFormsOnSmoothSpace}
###### Definition

For $X \in Smooth0Type$ and $n \in \mathbb{N}$, the **smooth space of differential $n$-forms** $\mathbf{\Omega}^n(X)$ on $X$ is the concretification, def. \ref{ConcreteObjectsAndConcretification}, of the smooth mapping space $[X, \Omega^n]$, def. \ref{SmoothFunctionSpace}, into the smooth moduli space of differential $n$-forms, def. \ref{SmoothModuliSpaceOfnForms}:

$$
  \mathbf{\Omega}^n(X) \coloneqq Conc([X, \Omega^n])
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The $\mathbb{R}^k$-plots of $\mathbf{\Omega}^n(\mathbb{R}^k)$
are indeed smooth differential $n$-forms on $X \times \mathbb{R}^k$ which are such that their evaluation on vector fields tangent to $\mathbb{R}^k$ vanish.

=--

+-- {: .proof}
###### Proof (sketch)

By def. \ref{Decohese}, def. \ref{ConcreteObjectsAndConcretification} and 
prop. \ref{DecohesOverASiteWithTerminalObject} the set of plots of $\mathbf{\Omega}^n(X)$ over $\mathbb{R}^k$ is the [[image]] of the [[function]]

$$
  \Omega^n(X \times \mathbb{R}^k)
  \simeq
   Hom_{Smooth0Type}(\mathbb{R}^k, [X,\Omega^n])
   \stackrel{\Gamma_{ \mathbb{R}^k, [X,\Omega^n] }}{\to}
   Hom_{Set}(\Gamma(\mathbb{R}^k), \Gamma [X, \Omega^n])
   \simeq
   Hom_{Set}(\mathbb{R}^k_s, \Omega^n(X))
  \,,
$$

where on the right $\mathbb{R}^k_s$ denotes, just for emphasis, the underlying set of $\mathbb{R}^k$. This function manifestly sends a smooth differential form $\omega \in \Omega^n(X \times \mathbb{R}^k)$ to the function from points $v$ of $\mathbb{R}^k$ to differential forms on $X$ given by

$$
  \omega \mapsto \left(v \mapsto  (id_X, v)^* \omega \right)
  \,.
$$

Under this function all components of differential forms with a "leg along" $\mathbb{R}^k$ are sent to the 0-form. Hence the image of this function is the collection of smooth forms on $X \times \mathbb{R}^k$ with "no leg along $\mathbb{R}^k$".

=--

+-- {: .num_remark }
###### Remark

For $n = 0$ we have (for any $X\in Smooth0Type$)

$$
  \begin{aligned}
    \mathbf{\Omega}^0(X) 
      & \coloneqq Conc [X, \Omega^0]
    \\
    & \simeq Conc [X, \mathbb{R}]
    \\
    & \simeq [X, \mathbb{R}]
  \end{aligned}
  \,,
$$

by prop. \ref{SpaceOf0FormsIsRealLine}.

=--

### Syntactic Layer
 {#DifferentialFormsLayerSyn}

#### Images

+-- {: .num_prop}
###### Proposition

Let a morphism $f \colon X \to Y$ in $\mathbf{H}$ be the [[categorical semantics]] of the [[syntax]]

$$
  x \colon X \; \vdash \; f(x) \colon Y
  \,.
$$

Then the syntax for the [[infinity-image|image]] $i_f \colon im(f) \hookrightarrow Y$ is

$$
  \vdash\;
   \left(
     \sum_{y \colon Y} \exists_{x \colon X} \left(f\left(x\right) = y\right)
   \right)
   \colon
   Type
  \,.
$$

=--

Here $\exists_{\cdots} \cdots =_{def} \left[ \sum_{\cdots} \cdot\right]$ is the [[bracket type]] of the [[dependent sum type]].

Accordingly the syntax for the smooth moduli space of differential $n$-forms, def. \ref{SmoothSpaceOfFormsOnSmoothSpace},
on a smooth space $X$, 


$$
  \sum_{\omega \colon \sharp [X, \Omega^n]}
  \exists_{\lambda \colon [X,\Omega^n]}
  (\omega = DeCoh_X(\lambda)) 
  \,.
$$

(...)
