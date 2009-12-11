
#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The [[Denis-Charles Cisinski|Cisinski]]--[[Ieke Moerdijk|Moerdijk]] [[model category]] structure on the [[category]] $dSet$ of [[dendroidal set]]s models [[(∞,1)-operad]]s in generalization of the way the [[Andre Joyal|Joyal]] [[model structure on simplicial sets]] models [[(∞,1)-category|(∞,1)-categories]].

## Overview ##


We have the following diagram of [[model category|model categories]]:

$$
  \array{
    SSet\text{-}Operad 
     &\stackrel{\simeq}{\to}& 
    dSet
     &\stackrel{\simeq}{\to}& 
    dSpaces
    &&&&& models\;for\;(\infty,1)\text{-}operads
    \\
    \uparrow && \uparrow && \uparrow
    \\
    SSet\text{-}Cat 
     &\stackrel{\simeq}{\to}& 
    sSet
     &\stackrel{\simeq}{\to}& 
    sSpaces   
    &&&&&
    models;for\;(\infty,1)\text{-}categories
  }
  \,,
$$

where the entries are

* the category $SSet Cat$ of [[simplicially enriched category|simplicially enriched categories]] equipped with the [[Julie Bergner|Bergner]] model structure;

* the category [[SSet]] of [[simplicial set]]s equipped with the [[model structure on simplicial sets|Joyal model structure]] for [[quasi-category|quasi-categories]];

* the category $dSet$ of [[dendroidal set]]s

and where 

* the horizontal morphisms are [[Quillen equivalence]]s

* the vertical morphisms are [[homotopy full functor|homotopy full]] embeddings.

## Definition ##


### Special morphisms ###

Recall frrom the entry on [[dendroidal set]]s the definition of inner and outer faces, boundaries and inner and outer horns.

The following definition are the obvious generalizations of the corresponding notions for the [[model structure on simplicial sets]], in particular for the [[Andre Joyal|Joyal]] model structure.

+-- {: .un_defn}
###### Definition (inner anodyne extension)

The class of morphisms in $dSet$ generated from the inner horn inclusions $\Lambda^e \Omega[T] \to \Omega[T]$ under

* [[pushout]]

* [[transfinite composition]]

* [[retract]]s

is called the **inner anodyne extensions**.

=--

+-- {: .un_defn}
###### Definition (inner Kan fibration)

A [[morphism]] $A \to B$ in $dSet$ is an **inner Kan fibration** if it has the [[right lifting property]] with respect to all inner horn inclusions.

$$
  \array{
    \Lambda^e[T] &\to& A
     \\
    \downarrow && \downarrow
    \\
    \Omega[T] &\to& B
  }
$$

or equivalently with respect to the class of inner anodyne extensions.

=--


+-- {: .un_defn}
###### Definition (inner Kan complex / quasi-operad)

A dendroidal set $X$ is an **inner Kan complex** or **quasi-operad** if the canonical morphism $X\to {*}$ to the [[terminal object]] is an inner Kan fibration.

=--

+-- {: .un_defn}
###### Definition (trivial fibration)

A morphism $A \to B$ of dendroidal sets is an **acyclic fibration** if it has the [[right lifting property]] with respect to all monomorphisms (equivalently: with respect to all normal monomorphisms).

=--




### The model structure ###

A **quasi-operad** is a [[dendroidal set]] such that...

A _trivial fibration of quasi-operads_ is a morphism of [[dendroidal set]]s such that...

An **inner anodyne extension** of [[dendroidal set]]s is a morphism such that... 

+-- {: .un_def }
###### Definition (model structure on dendroidal sets)

On the category of [[dendroidal set]]s let

* the cofibrations be the normal monomorphisms

* the fibrant objects are the weak Kan complexes/quasi-operads

* the fibrations between fibrant objects are the are the inner Kan fibrations $f : A \to B$ between quasi-operads such that the image $\tau_d(f)$ under the functor $\tau_d : dSet \to Operads$ is an operadic fibration

* the weak equivalences form the smallest class of maps that satisfy

  * [[category with weak equivalences|2-out-of-3]]

  * every inner anodyne extension is a weak equivalence

  * every trivial fibration between quasi-operads is a weak equivalence.

=--

## Properties ##


+-- {: .un_theorem }
###### Theorem

The above choices of cofibrations, fibrations and weak equivalences equips the category of dendroidal with the structure of a [[model category]]. This model structure is

* a left [[proper model category]]

* a [[cofibrantly generated model category]]

* a [[combinatorial model category]]

* a [[symmetric monoidal category|symmetric]] [[monoidal model category]]. 

=--

+-- {: .proof}
###### Proof

This is prop. 2.6 in [CisMoe](http://arxiv.org/abs/0902.1954).

=--

The [[cofibrantly generated model category|generating cofibrations]] $I$ are the boundary inclusion of [[tree]]s

$$
  I = \{\partial \Omega[T] \hookrightarrow \Omega[T]\}
  \,.
$$

A set of generating cofibrations is guaranteed to exist, but no good explicit characterization is known to date.

+-- {: .un_corollary }
###### Corollary

With this model structure and the standard [[model structure on operads]] the dendroidall [[nerve]] [[adjunction]]

$$
  \tau_d : dSet \stackrel{\leftarrow}{\to} Operad : N
$$

is a [[Quillen adjunction]] and both functors preserve all weak equivalences. So in particular a morphism of operads is a weak equivalence precisely if the induced morphism between dendroidal nerves is a weak equivalence.

=--

+-- {: .proof}
###### Proof

This is cor. 6.17 in [CisMoe](http://arxiv.org/abs/0902.1954).

=--



## References ##

A useful discussion of of the model structure on dendroidal sets is section 8 of





#Contents#
* automatic table of contents goes here
{:toc}



## Idea ##

Dendroidal sets are to [[operad]]s and [[(∞,1)-operad]]s as [[simplicial set]]s are to [[category|categories]] and [[(∞,1)-category|(∞,1)-categories]].

A dendroidal set is something that consists of [[tree category|trees]] in the way a [[simplicial set]] consists of [[simplex|simplices]]. 


## Definition ##

A **dendroidal set** is a [[presheaf]] on the [[tree category]] $\Omega$. 

The category of dendroidal sets is the [[functor category]]

$$
  dSet = [\Omega^{op}, Set]
  \,.
$$

Some terminology and notation:

* For $T \in \Omega$ a tree, write $\Omega[T] := \Omega(-,T)$ for the dendroidal set that it [[representable functor|represents]].

* For $X$ a dendroidal set and $T$ a tress, the set $dSet(T,X) \simeq X(T)$ (using the [[Yoneda lemma]]) is the set o $T$-shaped **dendrices** in $X$. One of its elements is called a $T$-shaped **dendrex**, analogous to a [[simplex]] in a [[simplicial set]].

## Relation to simplicial sets ##

Write $0$ for the tree consisting of a single edge. Let $\Omega/0$ be the [[over category]]. This is canonically isomorphic to the [[simplex category]]

$$
  \Omega/0 \simeq \Delta
  \,.
$$


Moreover, the over-category of all dendroidal sets over $\eta := \Omega[0]$ is the category [[SSet]] of [[simplicial set]]s

$$
  SSet \simeq dSet/\Omega[0]
  \,.
$$

The corresponding canonical [[functor]]

$$
  i : \Delta = \Omega/0 \to \Omega
$$

is a [[full and faithful functor]] and induces an [[adjunction]]

$$
  i_* : SSet :  \stackrel{\leftarrow}{\to} : 
        dSet : i^*
  \,,
$$

where $i_*$ is a [[full and faithful functor]] defined equivalently as

* the [[left adjoint]] to $i^*$;

* the left [[Kan extension]] of $i$;

* the canonical functor $SSet \stackrel{=}{\to} dSet/\Omega[0] \to dSet$.

A morphism $X \to i_* Y$ of dendroidal sets exists only for $X$ itself a simplicial set, i.e. $X$ itself in the image of $i_*$.

The dendroidal set $i([n])$ that corresponds to the $n$-[[simplex]] is to be visualized as the linear tree with $(n+1)$-edges:

$$
  i([n])
  =
  \left(
  \stackrel{0}{\to} 
    \bullet
  \stackrel{1}{\to}
    \bullet
  \stackrel{2}{\to}
  \cdots 
  \bullet
  \stackrel{n}{\to} 
  \right)
  \,.
$$

We think of each bullet as a unary operation -- an ordinary [[morphism]] -- $\stackrel{n}{\to}\bullet \stackrel{n+1}{\to}$ from the [[object]] $n$ to the object $(n+1)$. 


Notice that this is hence Poincar&#233;-dual to how one tends to visualize $[n]$ itself

$$
  [n] = (0 \to 1 \to 2 \to \cdots \to n)  
$$

and how one tends to visualize morphisms $n \to (n+1)$.


## Faces of trees and dendroidal sets ##

The _face maps_ on trees, regarded as dendroidal sets, are morphisms that generalize the face maps in the [[simplex category]] $\Delta$. Defining them in $\Omega$ requires a few case distinctions:

there are

1. inner face maps -- obtained by contracting an inner edge 

1. outer face maps -- obtained by 

   1. removing an outer input vertex

   1. removing a vertex whose output is the root and which has precisely one inner incoming edge (which becomes the new root)

   1. a corolla face -- any one of the inclusions of the tree with no vertex into a tree with precisely one vertex



### Inner faces

For $T \in \Omega$ and $e$ an _inner edge_ (in the obvious sense), write $T/e$ for the tree obtained by contracting/discarding this inner edge. There is then a canonical inclusion

$$
  \partial_e : T/e \to T
  \,.
$$ 

This is called an **inner face map**.


For example let 

$$
  T = 
   \left(
    \array{
     \searrow && \swarrow
     \\
     & v
     \\
     \searrow & & \searrow^e
     \\
      & \bullet &\to& \bullet &\to& 
     \\
     \nearrow
    }
  \right)
$$

then 

$$
  T/e = 
   \left(
    \array{
     \searrow && \searrow& & \swarrow 
     \\
      & \bullet &\to& \bullet &\to& 
     \\
     \nearrow
    }
  \right)
$$

and the inclusion $T/e \to T$ the the operad morphism that is the identity on the operation  $
  \array{
    \searrow
    \\
    & \bullet & \to
    \\
    \nearrow
  }
$
and which sends the trinary operation
$
  \array{
     \searrow && \swarrow
     \\
     \to & \bullet & \to
  }
$
to the composite trinary operation
$
    \array{
     \searrow && \swarrow
     \\
     & \bullet
     \\
      & & \searrow^e
     \\
      & &\to& \bullet &\to& 
     \\
    }
$


### Outer face maps

In contrast to that, _outer_ edges are always removed together: 

if $v$ is a vertex of $T$ such that all but one edge incident on it are outer, then denote by $T/v$ the tree obtained by discarding $v$ and all the outer edges indicent on it. There is then again a canonical inclusion

$$
  \partial_v : T/v \to T
  \,.
$$

This is called an **outer face map**.

In the above example for $T$ we have

$$
  T/v 
   = 
   \left(
    \array{
     \searrow & & \searrow^e
     \\
      & \bullet &\to& \bullet &\to& 
     \\
     \nearrow
    }
  \right)
$$

### Corolla faces

If the tree has precisely one vertex it is called a **corolla**. There are $n+1$ injections of the tree with no vertex $|$ into the corolla with $n$ inputs. All these are outer face maps.

$$
  | \hookrightarrow
  \array{
    \searrow && \swarrow
    \\
    & {*}
    \\
    & \downarrow
  }
  \,.
$$


### Properties


+-- {: .un_lemma }
###### Lemma (face maps are the monomorphisms)

The inner and outer face morphisms $\partial_e$ and $\partial_v$ are precisely the [[monomorphism]]s in the [[tree category]] $\Omega$. 

=--

+-- {: .proof}
###### Proof

Lemma 3.1 in [MoeWei07](http://cat.inist.fr/?aModele=afficheN&cpsidt=20087314).

=--


The **boundary of a tree** is the union of all its face dendroidal sets

$$
  \partial \Omega[T] = \cup_{e \in Edges(T)} \Omega[\partial_e T] \cup_{v \in Vertices(T)} \Omega[\partial_v T] 
  \,.
$$

Compare to [[boundary of a simplex]].

Analogously then to the notion of [[horn]] of a [[simplex]], for $d$ an edge of $T$ the union

$$
  \Lambda^e \Omega[T] = \cup_{e \neq d \in Edges(T)} \Omega[\partial_e T] \cup_{v \in Vertices(T)} \Omega[\partial_v T] 
$$

of dendroidal sets is the **inner horn** of $T$ at $e$, and for $w$ an outer face the union

$$
  \Lambda^w \Omega[T] = \cup_{e \neq d \in Edges(T)} \Omega[\partial_e T] \cup_{v \neq w \in Vertices(T)} \Omega[\partial_v T] 
$$

is the **outer horn** at $w$.

We have the canonical **boundary inclusions**

$$
  \partial \Omega[T] \to \Omega[T]
$$

and **horn inclusions**

$$
  \Lambda^\alpha \Omega[T] \to \Omega[T]
  \,.
$$

+-- {: .un_defn}
###### Definition

A [[monomorphism]] $X \to Y$ of dendroidal sets is called **normal** if for any tree $T$, any non-degenerate dendrex $y \in Y(T)$ which does not belong to the image of $X(T)$ has a trivial stabilizer $Aut(T)_y \subset Aut(T)$. 

A dendroidal set $X$ is **normal** if $\emptyset \hookrightarrow X$ is a normal monomorphism. 

=--

For instance for any tree $T$, the dendroidal set $\Omega[T]$ is normal.

+-- {: .un_remark}
###### Remark 

This has nothing to do with the notion of [[normal monomorphism]] in a context with [[zero morphisms]].  

=--


+-- {: .un_prop}
###### Proposition

The class of morphisms in $dSet$ generated from the boundary inclusions under [[pushout]] and [[transfinite composition]] is precisely the class of **normal monomorphisms**.

=--

+-- {: .proof}
###### Proof

This is prop 1.4 in [CisMoer09](http://arxiv.org/abs/0902.1954).

=--

+-- {: .un_prop}
###### Proposition
**(compatibility with the Joyal model structure)**

Let $|$ be the tree with one color and no vertex (corresponding to the 0-[[simplex]]). The [[overcategory]] $dSet$ is canonically isomorphic to [[SSet]]

$$
  dSet/\Omega[|] \simeq SSet
  \,.
$$

The [[model structure on an overcategory]] induced on $SSet$ this way from the above model structure on $dSet$ coincides with the Joyal [[model structure on simplicial sets]] (the one whose fibrant objects are [[weak Kan complex]]es).

=--

+-- {: .proof}
###### Proof

This is for instance proposition 8.4.3 in the lecture notes listed below.

=--



## Structure on $dSet$ ##


### Closed symmetric monoidal structure ###

The category $dSet$ of dendroidal sets carries the structure of a [[symmetric monoidal category]], defined as follows:

in analogy to the [[nerve]] [[adjunction]]

$$
  \tau : SSet \stackrel{\leftarrow}{\to} Cat : N
$$

between ordinary [[category|categories]] and [[simplicial set]]s, there is an adjunction

$$
  \tau_d : dSet \stackrel{\leftarrow}{\to} Operad : N_d
$$

between [[operad]]s and dendroidal sets. 

The category $Operad$ carries the [[Boardman-Vogt tensor product]] $\otimes_{BV}$ and the symmetric monoidal structure on $dSet$ is taken to be the unique one 

* that makes $\tau_d$ a [[symmetric monoidal functor]];

* such that for any two trees $T,S$ we have

  $$
    \Omega[T] \otimes \Omega[S] = N_d(T \otimes_{BV} S)
    \,.
  $$

With respect to this monoidal struucture $dSet$ is a [[closed monoidal category]]. 

### $SSet$-enriched structure ###

Using the fact that $dSet$ is a [[closed monoidal category]] with [[internal hom]] dendroidal sets $[C,D]$ for dendroidal sets $C$ and $D$, and using the functor $i^* : dSet \to SSet$ we obtain canonically the structure of an [[SSet]]-[[enriched category]] on $dSet$ with the hom-simplicial set between $C$ and $D$ being $i^*[C,D]$.


### Model category structure ###

The category $dSet$ also carries the Cisinski-Moerdijk [[model structure on dendroidal sets]]. This structure is compatible with the above structures in that it makes $dSet$
into a [[simplicial model category]] and a [[monoidal model category]], respectively.


## References ##

A good survey of the theory as developed currently is

* [[Ieke Moerdijk]], _Lectures on dendroidal sets_ , notes typed by Javier Guiti&#233;rrez on lectures given at the Barcelona workshop on _Homotopy theory and higher categories_ (2008) (to appear in print soon)




The model structure was originally given in 

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets as models for homotopy operads_ ([arXiv](http://arxiv.org/abs/0902.1954))

A detailed discussion of the finbrant objects in the model structure is in

* [[Ieke Moerdijk]] [[Ittay Weiss]], _On inner Kan complexes in the category of dendroidal sets_ ([web](http://www.sciencedirect.com/science?_ob=ArticleURL&_udi=B6W9F-4VM2KC8-1&_user=457046&_rdoc=1&_fmt=&_orig=search&_sort=d&_docanchor=&view=c&_searchStrId=1115574112&_rerunOrigin=google&_acct=C000021878&_version=1&_urlVersion=0&_userid=457046&md5=5eb2307e02ed1aa9e6fe2c7809346546))
