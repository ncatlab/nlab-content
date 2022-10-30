
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $K$ a [[locally presentable (∞,1)-category]] whose objects we think of as [[space]]s of sorts, its **tangent $(\infty,1)$-category**

$$
  (T_{K^{op}})^{op} \to K
$$

is an [[(∞,1)-category]] over $K$, whose objects may be thought of as spaces that are **[[infinitesimal space|infinitesimal]] thickenings** of those of $K$.

More concretely, the tangent $(\infty,1)$-category $T_C \to C$ for $C = K^{op}$ is the fiberwise [[stabilization]] of the [[codomain fibration]] $Func(\Delta[1], C) \to C$.  

This generalizes -- as discussed at [[deformation theory]] -- the classical example of the [[bifibration]] [[Mod]] $\to$ [[CRing]] of the category of all [[module]]s over the cateory [[CRing]] of all commutative rings: 

the fiber of the tangent $(\infty,1)$-category $T_C$ over an object $A \in C$ may be thought of as the $(\infty,1)$-category of **square-0-extensions** $A \oplus N$ of $A$, for $N$ a [[module]] over $A$. Dually, in $K = C^{op}$ we may think of these as being infinitesimal neighbourhoods of 0-sections of [[vector bundle]]s -- or rather of [[quasicoherent sheaves]] -- over whatever [[space]] $A$ is regarded to be the algebra of functions on.
 
A remarkable amount of information about the geometry of these spaces/objects in $K$ is encoded in the fiber of the tangent $(\infty,1)$-category over them. Notably the [[left adjoint|left]] [[adjoint (∞,1)-functor]] 

$$
  \Omega : C \to T_C
$$

to the domain projection $dom : T_C \to C$ turns out to send each $A$ to its [[cotangent complex]] $\Omega(A)$, to be thought of as the module of [[Kähler differential]]s on the space that $A$ is functions on.

A [[category theory|1-categorical]] approximation to the notion of tangent $(\infty,1)$-category is that of [[tangent category]].

## Definition

Let $C$ be a [[locally presentable (∞,1)-category]].

+-- {: .num_defn}
###### Definition
**(fiberwise stabilization)**

For $C' \to C$ a [[model structure for quasi-categories|categorical fibration]], [[generalized the|the]] **fiberwise stabilization** $Stab(C' \to C)$ is -- roughly -- the fibration universal with the property that for each $A \in C$ its [[fiber]] over $A$ is the [[stabilization]] $Stab(C'_A)$ of the fiber $C'_A$ over $A$.


=--

This is ([Lurie, section 1.1](#Lurie)) formulated in view of ([Lurie, remark 1.1.8](#Lurie)). There $Stab(C' \to C)$ is called the _stable envelope_ .

+-- {: .num_defn}
###### Definition
**(tangent $(\infty,1)$-category)**

[[generalized the|The]] **tangent $(\infty,1)$-category** $T_C \to C$ [[generalized the|the]] _fiberwise stabilization_ of the [[codomain fibration]]  $cod : Func(\Delta[1], C) \to C$:

$$
  (T_C \stackrel{p}{\to} C) := Stab(Func(\Delta[1], C) \stackrel{cod}{\to} C  )
  \,.
$$

=--

This is [[Deformation Theory|DT, def 1.1.12]].



## Properties

### General

+-- {: .num_prop}
###### Proposition

The tangent $(\infty,1)$-category $T_C$ of the [[locally presentable (∞,1)-category]] $C$ is itself a locally presentable $(\infty,1)$-category.

In particular, it admits all [[(∞,1)-limit]]s and [[(∞,1)-colimit]]s.

=--

This is ([Lurie, prop. 1.1.13](#Lurie)).


### Relation to modules
 {#RelationToModules}

We discuss how the tangent $(\infty,1)$-category construction indeed generalizes the equivalence between the [[tangent category]] over [[CRing]] and the category [[Mod]] of all [[modules]] over commutative rings.

+-- {: .num_prop}
###### Proposition

Let $\mathcal{O}^\otimes$ be a [[coherent (∞,1)-operad]] and let $\mathcal{C}^\otimes \to \mathcal{O}^\otimes$ be a [[stable (∞,1)-category|stable]] $\mathcal{O}$-[[monoidal (∞,1)-category]]. 

Let 

$$
  A \in Alg_\mathcal{O}(\mathcal{C})
$$

be an $\mathcal{O}$-[[algebra over an (infinity,1)-operad|algebra]] in $\mathcal{C}$. Then the [[stabilization]] of the [[over-(∞,1)-category]] over $A$ is canonically equivalent to $Func_\mathcal{O}(\mathcal{O}, Mod_A^\mathcal{O}(\mathcal{C}))$

$$
  Stab( Alg_\mathcal{O}(\mathcal{C})/A)
  \simeq
  Func_\mathcal{O}(\mathcal{O}, Mod_A^\mathcal{O}(\mathcal{C}))
  \,.
$$

=--

This is ([Lurie, theorem 1.5.14](#Lurie)).

+-- {: .num_prop}
###### Proposition

Let $\mathcal{O}^\otimes$ be a [[coherent (∞,1)-operad]] and let $\mathcal{C}^\otimes \to \mathcal{O}^\otimes$ be a [[presentable (∞,1)-category|presentable]] [[stable (∞,1)-category|stable]] $\mathcal{O}$-[[monoidal (∞,1)-category]]. Then there is a canonical [[equivalence of (∞,1)-categories|equivalence]]

$$
  \phi : T_{Alg_\mathcal{O}(\mathcal{C})}
    \stackrel{\simeq}{\to}
  Alg_\mathcal{O}(\mathcal{C}) 
   \times_{Func(\mathcal{O}, Alg_\mathcal{O}(\mathcal{C}))}
  Func_\mathcal{O}(\mathcal{O}, Mod^\mathcal{O}(\mathcal{C}))
$$

of presentble [[Cartesian fibration|fibrations]] over $Alg_\mathcal{O}(\mathcal{C})$.

=--

This is ([Lurie, theorem, 1.5.19](#Lurie)).

In words this says that under the given assumptions, objects of $T_{\mathcal{C}}$ may be identified with pairs

$$
  (A, N)
$$

where 

* $A$ is an $\mathcal{O}$-[[∞-algebra over an (∞,1)-operad|algebra]] in $\mathcal{C}$;

* $N$ is an $A$-[[∞-module over an ∞-algebra over an (∞,1)-operad|module]].


## Cotangent complex

From its definition as the fiberwise stabilization of the [[codomain fibration]] $cod : Func(\Delta[1], C) \to C$ the tangent $(\infty,1)$-category $p : T_C \to C$ inherits a second $(\infty,1)$-functor to $C$, coming from the _domain_ evaluation

$$
  dom : T_C \to C
  \,.
$$ 

+-- {: .num_prop}
###### Definition/Proposition
**(cotangent complex)**

The domain evaluation $dom : T_C \to C$ admits a [[left adjoint|left]] [[adjoint (∞,1)-functor]]

$$
  (\Omega \dashv dom) : T_C \stackrel{\overset{\Omega}{\leftarrow}}{\underset{dom}{\to}}
  C
$$

that is also a [[section]] of $p : T_C \to C$ in that 

$$
  (C \stackrel{\Omega}{\to} T_C \stackrel{p}{\to} C) \simeq Id_C
$$ 

and hence that $C$ is a [[retract]] of $T_C$.

This $\Omega$ is the **cotangent complex $(\infty,1)$-functor** : for $A \in C$ the object $\Omega(A)$ is the [[cotangent complex]] of $A$.

=--


This is ([Lurie, def. 1.1.2, remark 1.2.3](#Lurie)).


## Examples 

### Of $E_\infty$-rings

+-- {: .num_cor}
###### Corollary

Let $E_\infty$ be the [[(∞,1)-category]] of [[E-∞ ring]]s and let $A \in E_\infty$. Then the [[stabilization]] of the [[over-(∞,1)-category]] over $A$ 

$$
  Stab(E_\infty/A) \simeq A Mod(Spec)
$$

is equivalentl to the category of $A$-[[module spectra]].

=--

([Lurie, cor. 1.5.15](#Lurie)).

## References

The definition and study of the notion of _tangent $(\infty,1)$-categories_ is from 

* [[Jacob Lurie]], _[[Deformation Theory]]_
 {#Lurie}

and section 8.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_

[[!redirects tangent (infinity,1)-categories]]
[[!redirects tangent (∞,1)-category]]
[[!redirects tangent (∞,1)-categories]]

