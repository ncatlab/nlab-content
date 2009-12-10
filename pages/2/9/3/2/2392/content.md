<div class="rightHandSide toc">
[[!include higher category theory - contents]]

***

[[!include higher algebra - contents]]

</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _$(\infty,1)$-operad_ is to that of [[(∞,1)-category]] as [[operad]] is to [[category]].

So, roughly, an $(\infty,1)$-operad is an algebraic structure that has for each given type of input and one type of output an [[∞-groupoid]] of operations that take these inputs to that output.

## Definitions

Two models for $(\infty,1)$-operads exist to date, one by Cisinski-[[Ieke Moerdijk|Moerdijk]], the other by [[Jacob Lurie|Lurie]].

### In terms of dendroidal sets

Here [[simplicial set]]s are generalized to [[dendroidal set]]s. The theory of $(\infty,1)$-operads is then formulated in terms of dendroidal sets in close analogy to how the theory of [[(∞,1)-category|(∞,1)-categories]] is formulated in terms of [[simplicial set]]s.

There is a [[model  structure on dendroidal sets]] whose fibrant objest are the **quasi-operad**s in direct analogy to the notion of [[quasi-category]]. 

Here are two blog entries on talks on this stuff:

* [Dendroidal Sets and Infinity-Operads](http://golem.ph.utexas.edu/category/2009/02/dendroidal_sets.html)

* [Moerdijk on Infinity Operads](http://golem.ph.utexas.edu/category/2009/02/moerdijk_on_infinityoperads.html)

### In terms of $(\infty,1)$-categories of operators

Every [[operad]] $A$ encodes and is encoded by its [[category of operators]] $C_A$. In the approach to $(\infty,1)$-operators described below, the notion of category of operators is generalized to an [[(∞,1)-category]] of operators.

In this approach an $(\infty,1)$-operad $C^\otimes$ is regarded as an [[(∞,1)-category]] $C$ -- the unary part of the $(\infty,1)$-operad to be described-- with extra structure that determines [[(∞,1)-functor]]s $C^{\times n} \to C$.

This and the conditions on these are encoded in requiring that $C^\otimes$ is an $(\infty,1)$-functor $C^\otimes \to \Gamma$ over [[Segal's category]] $\Gamma$ of pointed finite sets, satisfying some conditions.

In particular, any [[symmetric monoidal (∞,1)-category]] yields an example of an $(\infty,1)$-operad in this sense.  In fact, symmetric monoidal $(\infty,1)$-categories can be *defined* as $(\infty,1)$-operads such that the functor $C^\otimes \to \Gamma$ is a [[coCartesian fibration]].  (For the moment, see [[monoidal (infinity,1)-category]] for more comments and references on higher operads in this context.)

This is the approach described in (the new version of !)

* [[Jacob Lurie]], _Commutative algebra_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-III.pdf))

### Model for $(\infty,1)$-categories of operators {#ModelForinfOpera}

There is a [[model category]] that [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category]] $(\infty,1)Cat_{Oper}$ of $(\infty,1)$-categories of operations.

+-- {: .un_prop}
###### Proposition

There exists a 

* [[proper model category|left proper]]

* [[combinatorial model category|combinatorial]]

[[model category]] $\mathcal{P} Op_{(\infty,1)}$

* whose underlying [[category]] has

  * [[object]]s are [[marked simplicial set]] $S$ equipped with a morphism $S \to N(FinSet_*)$ such that marked edges map to inert morphisms in $FinSet_*$ (those for which the preimage of te marked point contains just the marked point)

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

+-- {: .proof}
###### Proof

This is prop 1.8 4 in

* [[Jacob Lurie]], _Commutative algebra_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-III.pdf))


=--

## Relation between the two definitions {#relation}

+-- {: .standout}

At the time of this writing there is no discussion in "the literature" of the relation between the definition of $(\infty,1)$-operads in terms of dendroidal sets (Cisinski,  Moerdijk, Weiss) and $(\infty,1)$-categories of operators (Lurie). The following are some tentative observations. - [[Urs Schreiber|Urs]]

=--


There is an obvious way to regard as [[tree]] as an $(\infty,1)$-category of operators:

+-- {: .un_defn}
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

+-- {: .un_defn}
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



+-- {: .un_prop}
###### Proposition

The dendroidal nerve functor has the following properties:

* it sends fibrant objects to fibrant objects 
  
  i.e. it sends $(\infty,1)$-categories of 
  operations to $(\infty,1)$-operads 
  in their incarnation as "quasi-operads";

* it sends objects $\pi : A \to N(FinSet_*)$ that come 
  from grouplike [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[∞-groupoid]]s to fully Kan dendroidal sets (that have the extension property with respect to all horns)

* it sends objects $\pi : A \to N(FinSet_*)$ that come 
  from 
  [[symmetric monoidal (infinity,1)-category|symmetric monoidal (∞,1)-categories]] to dendroidal sets that have the extension property with respect to at least one outer horn $\Lambda_{v} T$ for $v \in T$ an $n$-corolla, for all $n \in \mathbb{N}$.

=--


+-- {: .proof}
###### Proof

**respect for fibrant objects**. If $A \to N(FinSet_*)$ is fibrant, then in particual $A$ is a [[weak Kan complex]] hence has the extension property with respect to all inner [[horn]] inclusions of [[simplex|simplices]]. We need to show that this implies that $N_d(A)$ has the extension property with respect to all inner horn inclusions of [[tree]]s.

By an (at the moment unpublished) result by [[Ieke Moerdijk|Moerdijk]], right [[lifting property]] with respect to inner horn inclusions of trees is equivalend to right lifting property with respect to inclusions of [[spine]]s of trees: the union over all the corollas in a tree.

For this the extension property means that if we find a collection $\{C_{k_i} \to N_d(A)\} = Sp(T)$ of corollas in $N_d(A)$ that match at some inputs and output, then these can be composed to an image $T \to N_d(A)$ of the corresponding tree $T$ in $N_d(A)$. 

An image of $T$ in $N_d(A)$ is an image of $\omega(T)$ in $A$. In the [[category of operators]] $\omega(A)$ every tree may be represented as the composite of a sequence of morphisms each of which consists of precisely one of the corollas $C_{k_i}$ in parallel to a identity morphisms. This way gluing the tree from the corollas is a matter of composing a sequence of edges in $A$. But this is guaranteed to be possible if $A$ is a [[weak Kan complex]].

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


=--



[[!redirects (∞,1)-operad]]
[[!redirects (∞,1)-operads]]
[[!redirects (infinity,1)-operads]]