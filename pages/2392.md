

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The notion of _$(\infty,1)$-operad_ is to that of [[(∞,1)-category]] as [[operad]] is to [[category]].

So, roughly, an $(\infty,1)$-operad is an algebraic structure that has for each given type of input and one type of output an [[∞-groupoid]] of operations that take these inputs to that output.

There is a fairly evident notion of [[∞-algebra over an (∞,1)-operad]]s. Examples include

* [[E-∞ algebra]]s

* [[L-∞ algebra]]s;

* [[A-∞ algebra]]s.

$(\infty,1)$-Operads form an [[(∞,2)-category]] [[(∞,1)Operad]].

## Definitions

Two models for $(\infty,1)$-operads exist to date, one by [[Denis-Charles Cisinski|Cisinski]]--[[Ieke Moerdijk|Moerdijk]]--[[Ittay Weiss|Weiss]], the other by [[Jacob Lurie|Lurie]]. It is expected though not yet entirely proved that the two are equivalent ([[Higher Algebra]], draft, Remark 2.0.0.8).

The first one models $(\infty,1)$-operads as [[dendroidal set]]s in close analogy to (in fact as a generalization of how) [[simplicial set]]s model [[(∞,1)-category|(∞,1)-categories]].

The second models the [[(∞,1)-category]] version of a [[category of operators]] of an operad.




### In terms of dendroidal sets

Here [[simplicial set]]s are generalized to [[dendroidal set]]s. The theory of $(\infty,1)$-operads is then formulated in terms of dendroidal sets in close analogy to how the theory of [[(∞,1)-category|(∞,1)-categories]] is formulated in terms of [[simplicial set]]s.

There is a [[model  structure on dendroidal sets]] whose fibrant objest are the **quasi-operad**s in direct analogy to the notion of [[quasi-category]]. 

So the [[model structure on dendroidal sets]] is a [[presentable (∞,1)-category|presention]] of the [[(∞,1)-category]] of $(\infty,1)$-operads. It is [[Quillen equivalence|Quillen equivalent]] to the standard [[model structure on operads]] enriched over [[Top]] or [[sSet]]. Therefore, conversely, the traditional homotopy-theoretic constructions on topological and chain operads (such as cofibrant [[resolution]]s in order to present homtopy algebras such as [[A-∞ algebra]]s, [[L-∞ algebra]]s, [[homotopy BV-algebra]]s and the like) are also indeed presentations of $(\infty,1)$-operads.

### In terms of $(\infty,1)$-categories of operators
 {#InTermsOfInfinityCategoriesOfOperators}

Every [[operad]] $A$ encodes and is encoded by its [[category of operators]] $C_A$. In the approach to $(\infty,1)$-operators described below, the notion of category of operators is generalized to an [[(∞,1)-category]] of operators.

In this approach an $(\infty,1)$-operad $C^\otimes$ is regarded as an [[(∞,1)-category]] $C$ -- the unary part of the $(\infty,1)$-operad to be described-- with extra structure that determines [[(∞,1)-functor]]s $C^{\times n} \to C$.

This and the conditions on these are encoded in requiring that $C^\otimes$ is an $(\infty,1)$-functor $C^\otimes \to \Gamma$ over [[Segal Gamma-category|Segal's category]] $\Gamma$ of pointed finite sets, satisfying some conditions.

In particular, any [[symmetric monoidal (∞,1)-category]] yields an example of an $(\infty,1)$-operad in this sense.  In fact, symmetric monoidal $(\infty,1)$-categories can be *defined* as $(\infty,1)$-operads such that the functor $C^\otimes \to \Gamma$ is a [[coCartesian fibration]].  (For the moment, see [[monoidal (infinity,1)-category]] for more comments and references on higher operads in this context.)

This is the approach described in ([LurieCommutative](#LurieCommutative))

#### Basic definitions
 {#BasicDefinitions}




We are to generalize the following construction from [[categories]] to [[(∞,1)-categories]].


+-- {: .num_defn}
###### Definition

For $\mathcal{O}$ a [[symmetric multicategory]], write $\mathcal{O}^\otimes \to FinSet^{*/}$ for its [[category of operators]].

Here $\mathcal{O}^\otimes$ is the [[category]] whose

* [[objects]] are finite sequences ([[tuples]]) of objects of $\mathcal{O}$;

* [[morphisms]] $(X_1, \cdots, X_{n_1}) \to (Y_1, \cdots, Y_{n_2})$ are given by a morphism $\alpha \colon \langle n_1\rangle \to \langle n_2\rangle$ in $FinSet_*$ together with a collection of [[multimorphisms]]

  $$
    \left\{
      \phi_j \in \mathcal{O}\left( \left\{ X_i\right\}_{i \in \alpha^{-1}\left\{j\right\}} , Y_j \right)
    \right\}_{1 \leq j \leq n_2}
    \,.
  $$

The [[functor]] $p \colon \mathcal{O}^\otimes \to FinSet^{*/}$ is the evident [[forgetful functor]].

=--

In ([Lurie](#Lurie)) this is construction 2.1.1.7.

This motivates the following definition of the generalization of this situation to [[(∞,1)-category theory]].

+-- {: .num_defn #FinSetPointed}
###### Definition

Write $FinSet^{*/}$ for the category of [[pointed object|pointed]] [[finite set]] ([[Segal Gamma-category|Segal's Gamma-category]]).

For $n \in \mathbb{N}$ we write 

$$
  \langle n\rangle
  \coloneqq
  {*} \coprod [n]
  \in 
  FinSet^{*/}
$$

for the [[pointed set]] with $n+1$ elements.

A morphism in $FinSet^{*/}$ 

* is called an  **[[inert morphism]]** if it is a surjection, and an [[injection]] on those elements that are not sent to the base point. That is, the preimage of every non-base point is a singleton.

* called an **[[active morphism]]** if only the basepoint goes to the basepoint.

For $n \in \mathbb{N}$ and $1 \leq i \leq n$ write

$$
  \rho^i \colon \langle n\rangle \to \langle 1\rangle
$$

for the inert morphism that sends all but the $i$th element to the basepoint. 

Notice that for each $n \in \mathbb{N}$ there is a unique [[active morphism]] $\langle n\rangle \to \langle 1\rangle$.

=--

([Lurie, def. 2.1.1.8](#Lurie))

+-- {: .num_defn #InfinityOperadByCategoryOfOperators}
###### Definition

The **$(\infty,1)$-category of operators of an $(\infty,1)$-operad** is a morphism

$$
  p \colon \mathcal{O}^\otimes \to FinSet^{*/}
$$

of [[quasi-categories]] such that the following conditions hold:

1. For every [[inert morphism]] in $FinSet^{*/}$ and every [[object]] over it, there is a lift to a $p$-[[coCartesian morphism]] in $\mathcal{O}^\otimes$. In particular, for $f \colon \langle n_1\rangle \to \langle n_2\rangle$ inert, there is an induced [[(∞,1)-functor]]

   $$
     f_! 
       \colon 
     \mathcal{O}^\otimes_{\langle n_1\rangle}
      \to
     \mathcal{O}^\otimes_{\langle n_2\rangle}
     \,.
   $$

1. The coCartesian lifts of the inert projection morphisms induce an equivalence of [[derived hom-spaces]] in $\mathcal{O}^{\otimes}$ between maps into multiple objects and the products of the maps into the separete objects:

   For $f \colon \langle n_1 \rangle \to \langle n_2 \rangle$ write $\mathcal{O}^\otimes_f(-,-) \hookrightarrow \mathcal{O}^\otimes(-,-)$ for the components of the [[derived hom-space]] covering $f$, then the $(\infty,1)$-functor

   $$  
     \mathcal{O}^\otimes_f(C_1,C_2)
     \to
     \underset{1 \leq k \leq n_2}{\prod}
     \mathcal{O}^\otimes_{\rho^i\circ f}(C_1,(C_2)_i)
   $$ 

   induced as above is an [[equivalence of infinity-groupoids|equivalence]].

1. For every finite collection of objects $C_1, \cdots c_n \in \mathcal{O}^\otimes_{\langle 1\rangle}$ there exists a multiobject $C \in \mathcal{O}^\otimes_{\langle n\rangle}$ and a collection of $p$-[[coCartesian morphisms]] $\{C \to C_i\}$ covering $\rho^i$.

   Equivalently (given the first two conditions): for all $n \in \mathbb{N}$ the $(\infty,1)$-functors $\{(\rho^i)_!\}_{1 \leq i \leq n}$ induce an [[equivalence of (∞,1)-categories]]

   $$
     \mathcal{O}^\otimes_{\langle n\rangle}
     \to
     (\mathcal{O}^\otimes_{\langle 1\rangle})^{\times^n}
   $$

=--

([Lurie, def. 2.1.1.10, remark 2.1.1.14](#Lurie))

+-- {: .num_remark }
###### Remark

The conditions in def. \ref{InfinityOperadByCategoryOfOperators} mean that $p \colon \mathcal{O}^\otimes \to FinSet^{*/}$ encodes

1. an [[(∞,1)-category]] $\mathcal{O} \coloneqq \mathcal{O}^\otimes_{\langle 1\rangle}$;

1. for each $n \in \mathbb{N}$ an $n$-ary operation given by the $(\infty,1)$-functor

   $$
     \mathcal{O}^{n}
     =
     (\mathcal{O}^\otimes_{\langle 1\rangle})^{\times n}
     \simeq
     \mathcal{O}^{\otimes}_{\langle n\rangle}
     \to 
     \mathcal{O}^\otimes_{\langle 1\rangle}
     = 
     \mathcal{O}
   $$

   induced by the unique [[active morphism]] $\langle n\rangle \to \langle 1\rangle$

1. a coherently associative multicomposition of these operations.

=--

+-- {: .num_remark }
###### Remark

The notion of def. \ref{InfinityOperadByCategoryOfOperators} may also be called a **symmetric $(\infty,1)$-multicategory** or **colored $(\infty,1)$-operad**. The _colors_ are the [[objects]] of $\mathcal{O}$.

=--

We now turn to the definition of [[homomorphisms]] of $(\infty,1)$-operads.

+-- {: .num_defn #InertMorphismsInInfinityOperad}
###### Definition

Given an $(\infty,1)$-operad $p \colon \mathcal{O}^\otimes \to FinSet^{*/}$ as in def. \ref{InfinityOperadByCategoryOfOperators}, a [[morphism]] $f$ in $\mathcal{O}^\otimes$ is called an **inert morphism** if 

1. $p(f)$ is an [[inert morphism]] in $FinSet^{*/}$ by def. \ref{FinSetPointed};

1. $f$ is a $p$-[[coCartesian morphism]].

=--


+-- {: .num_defn #MorphismOfInfinityOperads}
###### Definition

A **[[morphism of (∞,1)-operads]]** is a map between their [[(∞,1)-categories of operators]] over $FinSet^{*/}$ that preserves the inert morphisms of def. \ref{InertMorphismsInInfinityOperad}.

=--

Morphisms of operads $\mathcal{O}_1 \to \to \mathcal{O}_2$ can be understood equivalently as exhibiting an $\mathcal{O}_1$-[[algebra over an operad|algebra]] in $\mathcal{O}_2$. Therefore:

+-- {: .num_defn }
###### Definition

For $\mathcal{O}_1, \mathcal{O}_2$ to $(\infty,1)$-operads, write

$$
  Alg_{\mathcal{O}_1}(\mathcal{O}_2)
  \hookrightarrow
  qCat_{/FinSet^{*/}}(\mathcal{O}_1, \mathcal{O}_2)
$$

for the full [[sub-(∞,1)-category]] of the [[(∞,1)-functor (∞,1)-category]] on those that are [[morphisms of (∞,1)-operads]] by def. \ref{MorphismOfInfinityOperads}.

=--

([Lurie, def. 2.1.2.7](#Lurie)).

We also have the notion of

* _[[fibration of (∞,1)-operads]]_;

* _[[coCartesian fibration of (∞,1)-operads]]_.

See there for more details.


#### Model for $(\infty,1)$-categories of operators {#ModelForinfOpera}


There is a [[model category]] that [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category]] $(\infty,1)Cat_{Oper}$ of $(\infty,1)$-categories of operations.

+-- {: .num_prop}
###### Proposition

There exists a 

* [[proper model category|left proper]]

* [[combinatorial model category|combinatorial]]

[[model category]] $\mathcal{P} Op_{(\infty,1)}$

* whose underlying [[category]] has

  * [[object]]s are [[marked simplicial set]] $S$ equipped with a morphism $S \to N(FinSet_*)$ such that marked edges map to inert morphisms in $FinSet_*$ (those for which the preimage of the marked point contains just the marked point)

  * [[morphism]]s are morphisms of [[marked simplicial set]]s $S \to T$ such that the triangle

    $$
      \array{
        S &&\to&& T
        \\
        & \searrow && \swarrow
        \\
        && N(FinSet_*)
      }
    $$
    
    commutes;

* which is canonically an [[SSet]]-[[enriched category]];  

* and whose [[model category|model structure]] is given by

  * cofibrations are those morphisms whose underlying morphisms of [[simplicial set]]s ate cofibrations, hence [[monomorphism]]s
  
  * weak equivalences are those morphisms $S \to T$ such that for all $A \to N(FinSet_*)$ that are $(\infty,1)$-categories of operations by the above definition, the morphism of [[SSet]]-[[hom object]]s

    $$
      \mathcal{P}Op_\infty(T,A) \to 
      \mathcal{P}Op_\infty(S,A)
    $$

    is a homotopy equivalence of simplicial sets.

  * an object is fibrant if and only if it is an $(\infty,1)$-category of operations, by the above definition.

=--

This is prop 1.8 4 in

* [[Jacob Lurie]], _Commutative algebra_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-III.pdf))



## Examples

We list some examples of $(\infty,1)$-operads incarnated as their [[(∞,1)-categories of operators]] by def. \ref{InfinityOperadByCategoryOfOperators}.

The first basic examples to follow are in fact all given by [[1-categories]] [[category of operators|of operators]].

+-- {: .num_example}
###### Example

The [[identity]] functor on $FinSet^{*/}$ exhibits an $(\infty.1)$-operad. This is the **[[commutative operad]]**

$$
  Comm^\otimes = FinSet^{*/} \stackrel{id}{\to} FinSet^{*/}
  \,.
$$

The [[(∞,1)-algebras over an (∞,1)-operad]] over this $(\infty,1)$-operad are [[E-∞ algebras]].

=--

+-- {: .num_example}
###### Example

The **[[associative operad]]** has $Assoc^\otimes$ the category whose objects are the natural numbers, whose $n$-ary operations
are labeled by the [[total orders]] on $n$ elements, equivalently the elements of the [[symmetric group]] $\Sigma_n$, and whose composition is given by forming consecutive total orders in the obvious way.

The [[(∞,1)-algebras over an (∞,1)-operad]] over this $(\infty,1)$-operad are [[A-∞ algebras]]


=--

In ([Lurie](#Lurie)) this is remark 4.1.1.4.


+-- {: .num_example}
###### Example

The **[[operad for modules over an algebra]]** $LM$ is the [[colored operad|colored]] [[symmetric operad]] whose

* [[objects]] are two elements, to be denoted $\mathfrak{a}$ and $\mathfrak{n}$;

* [[multimorphisms]] $(X_i)_{i = 1}^n \to Y$ form

  * if $Y = \mathfrak{a}$ and $X_i = \mathfrak{a}$ for all $i$ then: the set of [[linear orders]] on $n$ elements, equivalently the elements of the [[symmetric group]] $\Sigma_n$;

  * if $Y = \mathfrak{n}$ and exactly one of the $X_i = \mathfrak{n}$ then: the set of linear order $\{i_1 \lt \cdots \lt i_n\}$ such that $X_{i_n} = \mathfrak{n}$ 

  * otherwise: the empty set;

* [[composition]] is given by composition of linear orders as for the [[associative operad]].

The [[(∞,1)-algebras over an (∞,1)-operad]] over this $(\infty,1)$-operad are pairs consisting of [[A-∞ algebras]] with [[(∞,1)-modules]] over them.


=--

In ([Lurie](#Lurie)) this appears as def. 4.2.1.1.

+-- {: .num_defn}
###### Definition

The **[[operad for bimodules over algebras]]** $BMod$ is the [[colored operad|colored]] [[symmetric operad]] whose

* [[objects]] are three elements, to be denoted $\mathfrak{a}_-, \mathfrak{a}_+$ and $\mathfrak{n}$;

* [[multimorphisms]] $(X_i)_{i = 1}^n \to Y$ form

  * if $Y = \mathfrak{a}_-$ and all $X_i = \mathfrak{a}_-$ then: the set of [[linear orders]] of $n$ elements;

  * if $Y = \mathfrak{a}_*$ and all $X_i = \mathfrak{a}_*$ then again: the set of [[linear orders]] of $n$ elements;

  * if $Y = \mathfrak{n}$: the set of linear orders $\{i_1 \lt \cdots \lt i_n\}$ such that there is exactly one index $i_k$ with $X_{i_k} = \mathfrak{n}$ and $X_{i_j} = \mathfrak{a}_-$ for all $j \lt k$ and $X_{i_j} = \mathfrak{a}_+$ for all $k \gt k$.

* [[composition]] is given by the composition of linear orders as for the [[associative operad]].

The [[(∞,1)-algebras over an (∞,1)-operad]] over this $(\infty,1)$-operad are pairs consisting of two [[A-∞ algebras]] with an [[(∞,1)-bimodule]] over them.

=--


## Properties


### Relation between the two definitions 
  {#relation}

+-- {: .standout}

At the time of this writing there is no discussion in "the literature" of the relation between the definition of $(\infty,1)$-operads in terms of dendroidal sets (Cisinski, Moerdijk, Weiss) and $(\infty,1)$-categories of operators (Lurie). The following are some tentative observations. - [[Urs Schreiber|Urs]]

update: meanwhile this has been worked out by some people. Results should appear in preprint form soon.

=--


There is an obvious way to regard a [[tree]] as an $(\infty,1)$-category of operators:

+-- {: .num_defn}
###### Definition
**(dendroidal $(\infty,1)$-category of operators)**

Let 

$$
  \omega : \Omega \hookrightarrow Op \stackrel{C_{(-)}}{\to}
  Cat/FinSet_* \stackrel{N}{\to}
  \mathcal{P}Op_{(\infty,1)}
$$

be the dendroidal object given by the following composition:

* $\Omega \hookrightarrow Op$ is the functor from the [[tree category]] $\Omega$ to the category of symmetric colored [[operad]]s (over [[Set]]) that sends a tree to the operad freely generated from it;

* $Op \stackrel{C_{(-)}}{\to} Cat/FinSet_*$ sends an [[operad]] to its [[category of operators]];

* $Cat/FinSet_* 
  \stackrel{N}{\to} \mathcal{P}Op_{(\infty,1)}$ takes 
  the [[nerve]] of this category, regarded as 
  a  [[marked simplicial set]] over $N(FinSet_*)$,
  whose marked edges are the inert morphisms in 
  the category of operations.

=--

Following the general pattern of [[nerve and realization]], we get:

+-- {: .num_defn}
###### Definition
**(dendroidal nerve of Lurie-$\infty$-operad)**

The functor

$$
  N_d := 
   Hom_{\mathcal{P}Op_{(\infty,1)}}(\omega(-), -):
   \mathcal{P}Op_{(\infty,1)} \to dSet
$$

that sends a [[marked simplicial set]] $A \to N(FinSet_*)$ to the [[dendroidal set]] which sends a [[tree]] $T$ to the set of morphisms of $\omega(T)$ into $A$

$$
  N_d(A) : T \mapsto Hom_{\mathcal{P}Op_{(\infty,1)}}(\omega(T), A)
$$

is the **dendroidal nerve** of $A$.


=--



+-- {: .standout}

One expects that $N_d$ induces a [[Quillen adjunction]] and indeed a [[Quillen equivalence]] between the above model category structure on $\mathcal{P}Op_{(\infty,1)}$ and the [[model structure on dendroidal sets]]. The following is as far as I think I can prove aspects of this. -[[Urs Schreiber|Urs]].

=--



+-- {: .num_prop}
###### Proposition

The dendroidal nerve functor has the following properties:

* it is the [[right adjoint]] of a [[SSet]]-[[enriched functor|enriched]] [[adjunction]]

  $$
    C_{(-)} : dSet \stackrel{\leftarrow}{\to} \mathcal{P}Op_{(\infty,1)}
   : N_d
  $$

* it sends fibrant objects to fibrant objects 
  
  i.e. it sends $(\infty,1)$-categories of 
  operations to $(\infty,1)$-operads 
  in their incarnation as "quasi-operads";

* it sends objects $\pi : A \to N(FinSet_*)$ that come 
  from grouplike [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[∞-groupoid]]s to fully Kan dendroidal sets (that have the extension property with respect to all horns)

* it sends objects $\pi : A \to N(FinSet_*)$ that come 
  from 
  [[symmetric monoidal (infinity,1)-category|symmetric monoidal (∞,1)-categories]] to dendroidal sets that have the extension property with respect to at least one outer horn $\Lambda_{v} T$ for $v \in T$ an $n$-corolla, for all $n \in \mathbb{N}$.

* its [[left adjoint]] sends cofibrations to cofibrations and acyclic cofibrations with cofibrant domain to acyclic cofibrations.


=--


+-- {: .proof}
###### Proof

**respect for fibrant objects**. If $A \to N(FinSet_*)$ is fibrant, then in particual $A$ is a [[weak Kan complex]] hence has the extension property with respect to all inner [[horn]] inclusions of [[simplex|simplices]]. We need to show that this implies that $N_d(A)$ has the extension property with respect to all inner horn inclusions of [[tree]]s.

By an (at the moment unpublished) result by [[Ieke Moerdijk|Moerdijk]], right [[lifting property]] with respect to inner horn inclusions of trees is equivalend to right lifting property with respect to inclusions of [[spine]]s of trees: the union over all the corollas in a tree.

For this the extension property means that if we find a collection $\{C_{k_i} \to N_d(A)\} = Sp(T)$ of corollas in $N_d(A)$ that match at some inputs and output, then these can be composed to an image $T \to N_d(A)$ of the corresponding tree $T$ in $N_d(A)$. 

An image of $T$ in $N_d(A)$ is an image of $\omega(T)$ in $A$. In the [[category of operators]] $\omega(A)$ every tree may be represented as the composite of a sequence of morphisms each of which consists of precisely one of the corollas $C_{k_i}$ in parallel to identity morphisms. This way gluing the tree from the corollas is a matter of composing a sequence of edges in $A$. But this is guaranteed to be possible if $A$ is a [[weak Kan complex]].

**symmetric monoidal product and outer horn lifting**

As described at [[cartesian morphism]], an edge $f : \Delta^1 \to A$ in $A$ is coCartesian if for all diagrams

$$
  \array{
    \Delta^{0,1}
    \\
    \downarrow & \searrow^f
    \\
    \Lambda^n_0 &\to & A
    \\
    \downarrow && \downarrow
    \\
    \Delta^n &\to& N(FinSet_*)
  }
$$

of 0-horn lifting problems where the first edge of the horn is $f$ itself, there exists a lift

$$
  \array{
    \Delta^{0,1}
    \\
    \downarrow & \searrow^f
    \\
    \Lambda^n_0 &\to & A
    \\
    \downarrow &\nearrow & \downarrow
    \\
    \Delta^n &\to& N(FinSet_*)
  }
  \,.
$$

For $f$ the parallel application of an $n$-corolla with a collection of identity morphisms this implies that any outer horn $\Lambda_v T \to N_d(A)$ for which the vertex $v : C_n \to N_d(A)$ maps to $f$, the dendroidal set $N_d(A)$ has the extension property with respect to the inclusion $\Lambda_d T \hookrightarrow T$.

**the left adjoint and its respect for cofibrations**

By general nonsense the [[left adjoint]] to $N_d$ is given by the [[coend]]

$$
  C_{(-)} : dSet \to \mathcal{P}Op_{(\infty,1)}
$$

$$
  C_P = \int^{T \in \Omega} \omega(T) \cdot P(T)
  \,,
$$

where in the integrand we have the tautological [[copower|tensoring]] of $\mathcal{P}Op_{(\infty,1)}$ over [[Set]].

Notice that $\omega : \Omega \to \mathcal{P}Op_{(\infty,1)}$ is an [[SSet]]-[[enriched functor]] for the ordinary category $\Omega$ regarded as a simplicially enriched category by the canonical embedding $Set \hookrightarrow SSet$. Therefore this adjunction $F \dashv N_d$ is defined entirely in [[SSet]]-[[enriched category theory]] and hence is a simplicial adjunction.

The [[model structure on dendroidal sets]] has a set of [[cofibrantly generated model category|generating cofibrations]] given by the boundary inclusions of trees. $\partial \Omega[T] \hookrightarrow \Omega[T]$. Tese evidenly map to monomorphisms of underlying simplicial sets under $F$, hence to cofibrations.

For $f : P \hookrightarrow Q$ an acyclic cofibration with cofibrant domain, we need to check that $C_f : C_X \to C_Y$ is a weak equivalence in $\mathcal{P}Op_{(\infty,1)}$. This is by definition the case if for every fibrant object $A$ the morphism

$$
  \mathcal{P}Op_{(\infty,1)}(C_Y,A) \to 
  \mathcal{P}Op_{(\infty,1)}(C_X,A)
$$

is a weak equivalence in the standard [[model structure on simplicial sets]]. By the simplicial adjunction $F \dashv N_d$ this is equivalent to

$$
  dSet(f,N_d(A))
  :
  dSet(Y,N_d(A)) \to 
  dSet(X,N_d(A))
$$

being a weak equivalence. By the above $N_d(A)$ is fibrant. By section 8.4 of the lecture notes on dendroidal sets cited at [[model structure on dendroidal sets]] a morphism between cofibrant dendroidal sets is a weak equivalence precisely if homming it into any fibrant dendroidal set produces an equivalence of homotopy categories. 

Since $f$ is a weak equivalence between cofibrant objects by assumption, it follows that indeed $dSet(f,N_d(A))$ is a weak equivalence for all fibrant $A$. 

> (AHM, or does it? there is a prob here, but I need to run now...) 

Hence $C_f$ is a weak equivalence.

=--


## Related concepts

* [[table - models for (∞,1)-operads]]

* [[algebraic theory]] / [[Lawvere theory]] /  [[(∞,1)-algebraic theory]]

* [[monad]] / [[(∞,1)-monad]]

* [[operad]] / **$(\infty,1)$-operad**, [[model structure on operads]]

  * [[morphism of (∞,1)-operads]], [[fibration of (∞,1)-operads]]

  * [[generalized (∞,1)-operad]], [[family of (∞,1)-operads]]

  * [[algebra over an (∞,1)-operad]], [[model structure on algebras over an operad]]

    * [[module over an algebra over an (∞,1)-operad]], [[model structure on modules over an algebra over an operad]]

  * [[coherent (∞,1)-operad]]

* [[operadic (∞,1)-Grothendieck construction]]

* [[cohomology of operads]]



## References

The formulation in terms of [[dendroidal sets]] is due to

* [[Ieke Moerdijk]], [[Ittay Weiss]], _Dendroidal sets_ ([web](http://cat.inist.fr/?aModele=afficheN&cpsidt=20087314))

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets as models for homotopy operads_ ([arXiv](http://arxiv.org/abs/0902.1954)) .

Here are two blog entries on talks on this stuff:

* [Dendroidal Sets and Infinity-Operads](http://golem.ph.utexas.edu/category/2009/02/dendroidal_sets.html)

* [Moerdijk on Infinity Operads](http://golem.ph.utexas.edu/category/2009/02/moerdijk_on_infinityoperads.html)


The formulation in terms of an $(\infty,1)$-version of the [[category of operators]] is introduced in

* [[Jacob Lurie]], _[[Commutative Algebra]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-III.pdf))
{#LurieCommutative}

and further discussed in

* _[[Ek-Algebras]]_ .

Now in section 2 of the textbook

* _[[Higher Algebra]]_
 {#Lurie}

The equivalence between the [[dendroidal set]]-formulation and the one in terms of $(\infty,1)$-categories of operators is shown in 

* [[Gijs Heuts]], [[Vladimir Hinich]], [[Ieke Moerdijk]], _The equivalence between Lurie's model and the dendroidal model for infinity-operads_ ([arXiv:1305.3658](http://arxiv.org/abs/1305.3658))

Further equivalence to Barwick's complete Segal operads is discussed in

* Hongyi Chu, [[Rune Haugseng]], [[Gijs Heuts]], _Two models for the homotopy theory of $\infty$-operads_ ([arXiv:1606.03826](https://arxiv.org/abs/1606.03826))

For an account in terms of _analytic_ [[monads]], that is, monads that are cartesian (multiplication and unit transformations are cartesian) and the underlying endofunctor preserves sifted colimits and wide pullbacks (or equivalently all weakly contractible limits), see

* [[David Gepner]], [[Rune Haugseng]], [[Joachim Kock]], _∞-Operads as Analytic Monads_, ([arXiv:1712.06469](https://arxiv.org/abs/1712.06469))



[[!redirects (∞,1)-operad]]
[[!redirects (∞,1)-operads]]
[[!redirects (infinity,1)-operads]]