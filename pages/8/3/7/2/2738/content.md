
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

A dendroidal set $X$ is normal if $\emptyset \hookrightarrow X$ is a normal monomorphism. 

=--

For instance for any tree $T$, the dendroidal set $\Omega[T]$ is normal.

+-- {: .un_remark}
###### Remark 

This has nothing to do with the notion of [[normal monomorphism]] in a context with [[zero morphisms]].  

=--


+-- {: .un_prop}
###### Proposition

The class of morphisms in $dSet$ generated from the boundary inclusions under [[pushout]] and [[transfinite composition]] is preecisely the class of **normal monomorphisms**.

=--

+-- {: .proof}
###### Proof

This is prop 1.4 in [CisMoer09](http://arxiv.org/abs/0902.1954).

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

The PhD thesis that gave the original definition:

* [[Ittay Weiss]], _Dendroidal sets_ PhD thesis ([web](http://igitur-archive.library.uu.nl/dissertations/2007-0918-200833/UUindex.html))

The publication derived from that:

* [[Ieke Moerdijk]] [[Ittay Weiss]], _Dendroidal sets_ ([web](http://cat.inist.fr/?aModele=afficheN&cpsidt=20087314))

A discussion of inner Kan complexes (see also [[model structure on dendroidal sets]]):

* [[Ieke Moerdijk]] [[Ittay Weiss]], _On inner Kan complexes in the category of dendroidal sets_ ([web](http://www.sciencedirect.com/science?_ob=ArticleURL&_udi=B6W9F-4VM2KC8-1&_user=457046&_rdoc=1&_fmt=&_orig=search&_sort=d&_docanchor=&view=c&_searchStrId=1115574112&_rerunOrigin=google&_acct=C000021878&_version=1&_urlVersion=0&_userid=457046&md5=5eb2307e02ed1aa9e6fe2c7809346546))

Here two blog entries with some summaries and pointers to the literature

* [Dendroidal sets and infinity-operad](http://golem.ph.utexas.edu/category/2009/02/dendroidal_sets.html)

* [Moerdijk on infinity-operads](http://golem.ph.utexas.edu/category/2009/02/moerdijk_on_infinityoperads.html)


[[!redirects dendroidal sets]]