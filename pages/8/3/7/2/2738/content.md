
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



## Idea ##

Dendroidal sets are a [[geometric definition of higher categories|geometric]] model for [[(∞,1)-operad|higher]] _[[operads]]_ (precisely: multi-coloured [[symmetric operads]] / [[symmetric multicategories]]).

They are to [[operads]] and to [[(∞,1)-operads]] as [[simplicial sets]] are to [[category|categories]] and [[(∞,1)-categories]].

A dendroidal set is something that consists of [[tree category|trees]] in the way a [[simplicial set]] consists of [[simplex|simplices]]: the trees represent the [[free construction|free]] [[Set]]-[[operads]] over them, and so a dendroidal set is a structure defined as having consistent probes by free $Set$-operads.

More precisely, the [[category]] $dSet$ of dendroidal sets serves to complete the following [[commuting diagram]] of [[functors]]

$$
  \array{
    Cat &\hookrightarrow& Operad
    \\
    {}^{\mathllap{N}}\downarrow &&
    {}^{\mathllap{N_d}}\downarrow
    \\
    sSet
    &\hookrightarrow&
    dSet
  }
  \,,
$$

where the left vertical functor is the [[nerve]] $N :$ [[Cat]] $\to$ [[sSet]], and where the top horizontal functor includes categories into [[Set]]-enriched operads as those operads with only unary operations.

Moreover, $dSet$ completes this diagram even as a diagram of most of the evident pairs of [[adjoint functors]]. For details see _[The full diagram of relations](#FullDiagram)_ below.

Finally, there is a [[model structure on dendroidal sets]] which is the operadic analog of the [[model structure for quasi-categories]].

## Definition ##

### Dendroidal sets

+-- {: .num_defn }
###### Definition

Write [[Operad]] for the category of [[operads]], specifically for

* [[Set]]-enriched;

* [[symmetric operad|symmetric]];

* multi-colored

operads, also known as _[[symmetric multicategories]]_.

=--

+-- {: .num_defn #FreeOperadCategory}
###### Definition

The symmetric [[tree category]] is the [[full subcategory]]

$$
  \Omega \hookrightarrow Operad
$$

of [[Operad]] on those [[symmetric operads]] that are [[free construction|free]] on the symmetric collections given by finite rooted trees. (...)

=--

+-- {: .num_defn}
###### Definition

A **dendroidal set** is a [[presheaf]] on the [[tree category]] $\Omega$. 

The [[category]] of dendroidal sets is the [[functor category]]

$$
  dSet = [\Omega^{op}, Set]
  \,.
$$

=--

Some **terminology and notation**:

* For $T \in \Omega$ a tree, write $\Omega[T] := \Omega(-,T)$ for the dendroidal set that it [[representable functor|represents]].

* For $X$ a dendroidal set and $T$ a tree, the set $dSet(\Omega[T],X) \simeq X(T)$ (using the [[Yoneda lemma]]) is the set of $T$-shaped **dendrices** in $X$. One of its elements is called a $T$-shaped **dendrex**, analogous to a [[simplex]] in a [[simplicial set]].


### Faces of trees and dendroidal sets 

A dendroidal set encodes actual _operations_ in analogy to how a [[simplicial set]] encodes composition by way of _[[horn]] extensions_. In order to formalize this one needs the dendroidal analog of _faces_ of a [[simplex]], generalized from the [[simplex category]] to the [[tree category]].

To motivate the definition of dendroidal face maps, first consider the reformulation of simplicial faces under the map $i_! : sSet \to dSet$.

Under this embedding the $n$-simpley $\Delta[n]$ becomes the operad that is deficted by

$$
  \stackrel{a}{\to} \bullet_{01} \stackrel{b}{\to} \bullet_{02} \stackrel{c}{\to} \cdots \to \bullet_{(n-1) n} \to
$$

with unary operations $\bullet_{i (i+1)}$.

The face inclusion $\delta_i : \Delta[n-1] \to \Delta[n]$ which simplicially omits the $i$th vertex, operadically contracts away the $i$th color, i.e it is the morphism of operads that sends the unary operation $\bullet_{(i-1)i}$ to the unary operation 

$$
  \bullet_{i (i+1)} \circ \bullet_{(i-1) i }
$$

and sends all other generating unary operation to generating unary operations.

From this it is clear that for any try the map that exhibits the contraction of one edge should be a dendroidal face map. However, there are also some more cases to be taken care of. One has


1. inner face maps -- obtained by contracting an inner edge 

1. outer face maps -- obtained by 

   1. removing an outer input vertex

   1. removing a vertex whose output is the root and which has precisely one inner incoming edge (which becomes the new root)

   1. a corolla face -- any one of the inclusions of the tree with no vertex into a tree with precisely one vertex



#### Inner faces

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


#### Outer face maps

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

#### Corolla faces

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

### Normal morphisms and normal dendroidal sets


+-- {: .num_lemma }
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

+-- {: .num_defn}
###### Definition

A [[monomorphism]] $X \to Y$ of dendroidal sets is called **normal** if for any tree $T$, any non-degenerate dendrex $y \in Y(T)$ which does not belong to the image of $X(T)$ has a trivial stabilizer $Aut(T)_y \subset Aut(T)$. 

A dendroidal set $X$ is **normal** if $\emptyset \hookrightarrow X$ is a normal monomorphism. 

=--

For instance for any tree $T$, the dendroidal set $\Omega[T]$ is normal.

+-- {: .num_remark}
###### Remark 

This has nothing to do with the notion of [[normal monomorphism]] in a context with [[zero morphisms]].  

=--


+-- {: .num_prop}
###### Proposition

The class of morphisms in $dSet$ generated from the boundary inclusions under [[pushout]] and [[transfinite composition]] is precisely the class of **normal monomorphisms**.

=--

+-- {: .proof}
###### Proof

This is prop 1.4 in [CisMoer09](http://arxiv.org/abs/0902.1954).

=--

### Boardman-Vogt tensor product
 {#BoardmanVogtTensorProduct}

As any [[category of presheaves]], $dSet$ is a [[cartesian monoidal category]]. However, the cartesian [[tensor product]] is not the natural one with respect to the inclusion of [[operads]] into dendroidal sets. The natural monoidal structure on [[Operad]] is rather a generalization of the [[Boardman-Vogt tensor product]].

+-- {: .num_defn #BVTensorProduct}
###### Definition

Write

$$
  N_d(-\otimes -)
  :
  \Omega \times \Omega
  \hookrightarrow
  Operad \times Operad
  \hookrightarrow
  Operad
  \stackrel{N_d}{\to}
  dSet
$$

for the functor that forms the [[Boardman-Vogt tensor product]] of the free operads given by two trees, and then regards the result as a dendroidal set by the dendroidal nerve, def. \ref{DendroidalNerve}.

The **tensor product of dendroidal sets** is the [[Yoneda extension]] 

$$
  -\otimes - : dSet \times dSet \to dSet
$$

of this functor, hence the unique such functor which preserves [[colimits]] in both variables and coincides with the BV-tensor product of operads on $\Omega$.

=--

With respect to this tensor product is $dSet$ a [[closed monoidal category]]. This is discussed [below](#ClosedMonoidalStructure).


## Properties

### Relation to simplicial sets 
  {#RelationToSimplicialSets}

Write $0$ for the tree consisting of a single edge. Let $\Omega/0$ be the [[over category]]. By inspection one sees that

+-- {: .num_prop }
###### Proposition

There is an [[equivalence of categories]] 

$$
  \Omega/0 \simeq \Delta
$$

of the slice with the [[simplex category]].


Moreover, the over-category of all dendroidal sets over $\eta := \Omega[0]$ is the category [[sSet]] of [[simplicial set]]s

$$
  dSet/\Omega[0] \simeq sSet
  \,.
$$

=--

By general properties of [[Kan extension]] we have the following

+-- {: .num_prop }
###### Proposition

The corresponding canonical [[forgetful functor]]

$$
  i : \Delta \stackrel{\simeq}{\to} \Omega/0 \to \Omega
$$

is 

1. a [[full and faithful functor]];

1. a [[sieve]].

=--

+-- {: .num_prop }
###### Proposition


The functor $i : \Delta \to \Omega$ induces an [[adjoint triple]]

$$
  (i_! \dashv i^* \dashv i_*) 
   : 
   sSet
  \stackrel{
    \overset{i_!}{\hookrightarrow}
  }{
    \stackrel{\overset{i^*}{\leftarrow}}{\underset{i_*}{\hookrightarrow}}
  }
  dSet
  \,,
$$

where

* $i^*$ is given by precomposition with $i$;

* $i_*$ is a [[full and faithful functor]] defined equivalently as

  * the [[left adjoint]] to $i^*$;

  * the left [[Kan extension]] of $i$;

  * the canonical functor $sSet \stackrel{\simeq}{\to} dSet/\Omega[0] \to dSet$;

  * the functor that sends  $X \in sSet$ to 

    $$
      i_!(X) 
       : 
     T 
     \mapsto 
      \left\{
        \array{
          X_n & if\,T\,is\,linear\,with\,n\,vertices;
          \\
          \emptyset & otherwise
        }
      \right.
      \,.
    $$

Hence $i_!$ is a [[full and faithful functor]], and hence (see the discussion at [[adjoint triple]]) so is $i_*$.

Accordingly, $i : sSet \hookrightarrow dSet$ is an [[open geometric morphism|open]] [[geometric embedding]] of [[presheaf toposes]].

=--

+-- {: .num_remark }
###### Remark


The dendroidal set $i_!([n])$ that corresponds to the $n$-[[simplex]] is to be visualized as the linear tree with $(n+1)$-edges:

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

=--

The embedding of simplicial sets into dendroidal sets compatibly relates the [[cartesian monoidal category|Cartesian monoidal structure]] $(sSet, \times)$ with the [Boradman-Vogt monoidal structure](#BoardmanVogtTensorProduct) $(dSet, \otimes_{BV})$

+-- {: .num_prop }
###### Proposition

The functor 

$$
  i_! : (sSet, \times) \to (dSet, \otimes_{BV})
$$

is a [[strong monoidal functor]], in that for all $X, Y \in sSet$
there is a [[natural isomorphism]]

$$
  i_!(X \times Y) \simeq i_!(Y) \otimes_{BV} i_!(Y)
$$

in $dSet$. 

Moreover, $(i_! \dashv i^*)$ respects the [[internal hom]] of dendroidal sets, prop. \ref{TheClosedMonoidalStructure}, in that for all $X,Y \in sSet$ and $D \in dSet$

* $i^* [i_!(X), D]_{BV} \simeq [X, i^*(D)]$;

and hence in particular

* $i^* [i_!(X), i_!(Y)]_{BV} \simeq [X, Y]$.

=--

This appears as ([Moerdijk-Weiss, prop. 5.3](#MoerdijkWeiss)).



### Relation to $Set$-operads -- dendroidal nerve
 {#RelationToOperads}

By the general notion of [[nerve and realization]], the 
inclusion $\Omega \hookrightarrow Operad$ from def. \ref{FreeOperadCategory}
induces a [[nerve]] operation on [[operads]] with values in 
[[simplicial sets]].

+-- {: .num_defn #DendroidalNerve}
###### Definition

For $O \in Operad$ an [[operad]], its **[[dendroidal nerve]]**
is the dendroidal set given by

$$
  N_d(O) : T \mapsto Hom_{Operad}(T, O)
  \,.
$$

This extends to a [[functor]]

$$
  N_d : Operad \to dSet
  \,.
$$

=--

By general properties of [[nerve and realization]] we have:

+-- {: .num_prop}
###### Proposition

The dendroidal nerve has the following properties.

* It extends the simplicial nerve of operads in that

  $$
    i^* \circ N_d = N
    \,.
  $$

* It has a [[left adjoint]]

  $$
    \tau_d : dSet \to Operad
  $$

  given by [[left Kan extension]].

* $N_d$ is a [[full and faithful functor]], equivalently there is a [[natural isomorphism]]

  $$
    \tau_d \circ N_d \simeq id
    \,.
  $$

=--

See for instance ([Moerdijk-Weiss, section 4](#MoerdijkWeiss)).

For $X$ a dendroidal set, $\tau_d(X)$ is also called the **operad generated by** $X$.

In conclusion we find [[reflective subcategory]]

$$
  (\tau_d \dashv N_d)
   :
  Operad
    \stackrel{\overset{\tau_d}{\leftarrow}}{\underset{N_d}{\hookrightarrow}}
  dSet
  \,.
$$

This is compatible with the [[Boardman-Vogt tensor product]] as defined [above](#BoardmanVogtTensorProduct):

+-- {: .num_prop}
###### Proposition

The functor $\tau_d : (dSet, \otimes) \to (Operad, \otimes_{BV})$ is a [[strong monoidal functor]], in that for all $X, Y \in dSet$ there is a [[natural isomorphism]]

$$
  \tau_d(X \otimes Y ) \simeq \tau_d(X) \otimes_{BV} \tau_d(Y)
  \,.
$$


=--

This appears as ([Moerdijk-Weiss, prop. 5.2](#MoerdijkWeiss)).

+-- {: .num_remark}
###### Remark

Since $\tau_d N_d \simeq id$ in particular we have for all $P, Q \in Operad$
an isomorphism

$$
  \tau_d (N_d(P) \otimes N_d(Q)) \simeq P \otimes_{BV} Q
  \,.
$$

=--

### Relation to $sSet$-operads -- homotopy coherent dendroidal nerve
 {#HomotopyCoherentNerve}


The dendroidal nerve of [[Set]]-[[operads]] discussed 
[above](#RelationToOperads) is important for setting up the model of
dendroidal sets. But the usefulness of the model comes from 
its relation to [[sSet]]/[[Top]]-enriched operads ([[topological operads]])
via an operadic generalization of the [[homotopy coherent nerve]] that sends [[sSet-enriched categories]] to [[simplicial sets]].

Write $Operad_sSet$ for the category of [[sSet]]-enriched operads ([[simplicial operads]]). Write

$$ 
  W_H : Operad_sSet \to Operad_sSet
$$

for the [[Boardman-Vogt resolution]] functor.

The restriction of this along the inclusion of free Set-operads

$$
  \Omega \hookrightarrow Operad
  \hookrightarrow
  Operad_{sSet}
  \stackrel{W_H}{\to}
  Operad_{sSet}
  \,,
$$

which will also be denoted just $W_H$ in the following, 
canonically induces [[nerve and realization]] functors:

+-- {: .num_defn }
###### Definition

The **homotopy coherent nerve** of a simplicial operad $P$ is the dendroidal set $hcN_d(P)$ given by

$$
  hcN_d(P) : T \mapsto Hom_{Operad_{sSet}}(W_H(T), P)
 \,.
$$

This extends to a [[functor]]

$$  
  hcN_d : Operad_{sSet} \to dSet
  \,.
$$

=--

+-- {: .num_defn }
###### Definition


We write

$$
  {\vert -\vert}_H : dSet \to Operad_{sSet}
$$

for the corresponding [[left adjoint]] [[nerve and realization|realization]].

=--

Via this [[adjunction]]

$$
  ({\vert -\vert}_H \dashv hcN_d)
  : 
  Operad_{sSet}
  \to dSet
$$

we may understand generally the theory of dendroidal sets as being about BV-resolutions of simplicial operads.

+-- {: .num_prop }
###### Proposition

Let $P \in Operad_{sSet}$. 

There is an [[isomorphism]] of simplicial operads

$$
  W_H(P) \stackrel{\simeq}{\to}
  {\vert hcN_d P \vert}_H
$$

between the [[Boardman-Vogt resolution]] $W_H(P)$ of $P$ and the homotopy-realization of its homotopy-coherent dendroidal nerve.

=--

All of this is an operadic generalization of the _[[relation between quasi-categories and simplicial categories]]_.

### The full diagram of relations
 {#FullDiagram}

The above functors between dendroidal sets and 
simplicial sets ([here](#RelationToSimplicialSets))
and operads ([here](#RelationToOperads)) 
arrange into the following [[diagram]]



$$
  \array{
     sSet 
     &\stackrel{\overset{i_!}{\to}}{\underset{i^*}{\leftarrow}}&
     dSet
     \\
     {}^\mathllap{\tau} \downarrow
     \uparrow^{\mathrlap{N}}
     &&
     {}^{\mathllap{\tau_d}}
     \downarrow
     \uparrow^{N_d}
     \\
     Cat
     &
     \stackrel{\overset{j_!}{\to}}{\underset{j^*}{\leftarrow}}
     &
     Operad
  }
  \,,
$$

where functors on the left and on top are [[left adjoint|left adjoints]] to those on the right and on the bottom, respectively.

This commutes in three of four possible ways, up to [[natural isomorphism]] 
in that

1. $j_! \tau \simeq \tau_d i_!$;

1. $N j^* \simeq i^* N_d$;

1. $i_! N \simeq N_d j_!$.

There is also a [[natural transformation]]

$$
  \tau i^* \Rightarrow j^* \tau_d
  \,,
$$

but not all of its components are isomorphisms.

Moreover, $N, N_d$,$i_!, j_!$ are [[full and faithful functors]] 
and hence (see the properties of [[adjoint functors]])

1. $\tau N \simeq id$;

1. $\tau_d N_d \simeq id$;

1. $i^* i_! \simeq id$;

1. $j^* j_! \simeq id$.


## Structure on $dSet$ ##


### Closed symmetric monoidal structure
 {#ClosedMonoidalStructure}

+-- {: .num_prop #TheClosedMonoidalStructure}
###### Proposition

There exists an essentially unique [[symmetric monoidal category|symmetric]] [[closed monoidal category]] structure $(dSet, \otimes)$ on $dSet$ such that for all $S, T \in \Omega \hhokrightarrow Operad$ there is a [[natural isomorphism]]

$$
  \Omega[S] \otimes \Omega[T] \simeq N_d(\, S \otimes_{BV} T \,)
$$

with $\otimes_{BV}$ the [[Boardman-Vogt tensor product]] on operads, and with $N_d$ the dendroidal nerve, def. \ref{DendroidalNerve}.

This is given as discussed [above](#BoardmanVogtTensorProduct). The corresponding [[internal hom]] $[-,-]_{BV} : dSet^{op} \times dSet \to dSet$ is given by the formula

$$
  [X,Y]_{BV} : T \mapsto dSet(\Ometa(T) \otimes X, Y)
  \,.
$$

=--

This appears as ([Moerdijk-Weiss, prop. 5.1](#MoerdijkWeiss)).

### $SSet$-enriched structure ###

Using the fact that $dSet$ is a [[closed monoidal category]] with [[internal hom]] dendroidal sets $[C,D]$ for dendroidal sets $C$ and $D$, and using the functor $i^* : dSet \to SSet$ we obtain canonically the structure of an [[SSet]]-[[enriched category]] on $dSet$ with the hom-simplicial set between $C$ and $D$ being $i^*[C,D]$.


### Model category structure

The category $dSet$ carries the Cisinski-Moerdijk [[model structure on dendroidal sets]]. With this model structure it forms a [[monoidal model category]]. 

Together with the fact that $i^*: dSet \to sSet$ is a [[right Quillen functor]] (with respect to the [[model structure for quasi-categories]]) this imples that $dSet$ is an $sSet_{Joyal}$-[[enriched model category]] (but not, without further work, an $sSet_{Quillen}$-enriched model category!).


## References ##

Surveys of the theory as developed currently include

* [[Ieke Moerdijk]], _Lectures on dendroidal sets_ , lectures given at the Barcelona workshop on _[Simplicial methods in higher categories](http://www.crm.es/HigherCategories/)_ (2008) ([preliminary writeup](http://www.crm.cat/HigherCategories/hc1.pdf))

* [[Ittay Weiss]], _From operads to dendroidal sets_ , in _[[Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, AMS (2011)


An expanded and polished version has meanwhile been written up by Javier Guiti&#233;rrez and should appear in print soon. An electronic copy is probably available on request.


The PhD thesis that gave the original definition of dendroidal sets is:

* [[Ittay Weiss]], _Dendroidal sets_ PhD thesis ([web](http://igitur-archive.library.uu.nl/dissertations/2007-0918-200833/UUindex.html))

The publication derived from that:

* [[Ieke Moerdijk]] [[Ittay Weiss]], _Dendroidal sets_ Algebraic & Geometric Topology 7 (2007) 1441&#8211;1470,  ([journal](http://msp.warwick.ac.uk/agt/2007/07/p056.xhtml), [arXiv:math.AT/0701293](http://arxiv.org/abs/math.AT/0701293))
 {#MoerdijkWeiss} 

A discussion of inner Kan complexes (see also [[model structure on dendroidal sets]]):

* [[Ieke Moerdijk]], [[Ittay Weiss]], _On inner Kan complexes in the category of dendroidal sets_, [math.CT/0701295](http://arxiv.org/abs/math/0701295)

* Denis-Charles Cisinski, Ieke Moerdijk, _Dendroidal Segal spaces and infinity-operads_, [arxiv/1010.4956](http://arxiv.org/abs/1010.4956)

Here two blog entries with some summaries and pointers to the literature

* $n$cafe: [Dendroidal sets and infinity-operads](http://golem.ph.utexas.edu/category/2009/02/dendroidal_sets.html)

* $n$cafe: [Moerdijk on infinity-operads](http://golem.ph.utexas.edu/category/2009/02/moerdijk_on_infinityoperads.html)


[[!redirects dendroidal sets]]

[[!redirects dendroidal nerve]]