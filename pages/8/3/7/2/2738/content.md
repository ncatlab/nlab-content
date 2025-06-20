
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

A dendroidal set is something that consists of [[tree category|trees]] or "[[dendrices]]" in the way that a [[simplicial set]] consists of [[simplex|simplices]]: the trees represent the [[free construction|free]] [[Set]]-[[operads]] over them, and so a dendroidal set is a structure defined as having consistent probes by free $Set$-operads.

More precisely, the [[category]] [[dSet]] of dendroidal sets serves to complete the following [[commuting diagram]] of [[functors]]

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
 {#DendroidalSets}

+-- {: .num_defn }
###### Definition

Write [[Operad]] for the category of [[operads]], specifically for

* [[Set]]-enriched;

* [[symmetric operad|symmetric]];

* multi-coloured

operads, also known as _[[symmetric multicategories]]_.

=--

+-- {: .num_defn #FreeOperadCategory}
###### Definition

The symmetric [[tree category]] is the [[full subcategory]]

$$
  \Omega \hookrightarrow Operad
$$

of [[Operad]] on those [[symmetric operads]] that are [[free construction|free]] on finite rooted non-planar [[trees]].

=--

See ([below](#Trees)) for details on the trees appearing here.

+-- {: .num_defn #DendroidalSet}
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

* For $X$ a dendroidal set and $T$ a tree, the set $dSet(\Omega[T],X) \simeq X(T)$ (using the [[Yoneda lemma]]) is the set of $T$-shaped **[[dendrices]]** in $X$. One of its elements is called a $T$-shaped **dendrex**, analogous to a [[simplex]] in a [[simplicial set]].

### Trees and their free operads
 {#Trees}

We expand on the notion of symmetric/non-planar trees used in definition \ref{DendroidalSet}
of dendroidal sets (see for instance ([Weiss, section 2.1](#Weiss))).

+-- {: .num_defn }
###### Definition

A **finite symmetric rooted tree** -- or just **tree** for short, in the following --  is a [[finite set|finite]] [[poset]] $(T, \leq)$
such that

* it has a [[bottom]] element;

* for each element $e \in T$ the set $\{y \in T | y \leq e\}$ is a [[linear order]] under $\leq$;

and equipped with a subset $L \subset max(T)$ of the maximal elements of $T$.


=--

One has the following terminology

+-- {: .num_defn }
###### Terminology

Let $((T, \leq), L)$ be a tree.

* An element $e \in T$ is called an **edge** of the tree.

* The [[bottom]] element is called the **root** of the tree.

* An edge in $L \subset T$ is a **leaf** of the tree.

* An edge which is either a leaf or the root is called an **outer edge**.

* An edge which is neither a leaf nor the root is called an **inner edge**.

* Given a non-leaf edge $e$, another edge $e'$ is called an **incoming edge** of $e$ if it is a direct succesor of $e$, hence if

  1. $e \leq e'$;

  1. for any $x \in T$ with $e \leq x \leq e'$ either $x = e$ or $x = e'$.

  Write $in(e)$ for the set of incoming edges of $e$.

* For $e$ a non-leaf edge, the subset $v_e := \{e\} \cup in(e)$ is called a **vertex** of $(T, \leq)$. $e$ is called the **outgoing edge** of $v$, and the ingoing edges of $e$ are also called _ingoing edges of $v_e$_, $in(v_e) := in(e)$.

* The **valence** of a vertex $v$ is the [[cardinality]] ${\vert in(v)\vert}$.

=--

+-- {: .num_example #ATypicalTree}
###### Example

A typical tree as above is

$$
  \left\{
     \array{
        {}_{\mathllap{e}}\searrow && \swarrow_{\mathrlap{f}}
        \\
        & \bullet_v 
        \\
        && {}_{\mathllap{b}}\searrow && \swarrow_{\mathrlap{c}}
        \\
        & && \bullet_u & \stackrel{d}{\leftarrow} & \bullet_w
        \\
        & && \downarrow^{\mathrlap{r}}
     }
  \right\}
  \,,
$$

where

* the arrows depict the edges;

* the bullets depict vertices;

* the arrows not starting at a bullet depict leaf edges.

* the arrow not ending at a bullet depicts the root edge.

The set of incoming edges of $v$ is $\{e,f\}$, the outgoing edge of $v$ is $b$. The set of incoming edges of $u$ is $\{b,c,d\}$, its outgoing edge is the root edge $r$. The set of ingoing edges of $e$ is the [[empty set]], its outgoing edge is $b$.

The valence of $v$ is 2, that of $u$ is 3 and that of $w$ is 0.

Notice that there is _no_ order on the incoming edges of any vertex implied, the fact that there is one in the above picture is an artefact of being a planar diagram for visualization purposes. As a tree, the above is _equal_ to, for instance

$$
  \left\{
     \array{
        {}_{\mathllap{f}}\searrow && \swarrow_{\mathrlap{e}}
        \\
        & \bullet_v 
        \\
        && {}_{\mathllap{b}}\searrow && \swarrow_{\mathrlap{c}}
        \\
        & && \bullet_u & \stackrel{d}{\leftarrow} & \bullet_w
        \\
        & && \downarrow^{\mathrlap{r}}
     }
  \right\}
  \,,
$$


=--

+-- {: .num_defn }
###### Definition

For $((T, \leq ), L)$ a tree, the corresponding [[symmetric operad]]
over [[Set]] is the one

* whose set of colours is is $T$ (the set of edges);

* whose operations are freely generated from the set of vertices of $T$, where the generating operation corresponding to a vertex $v$ goes from $in(v)$ to the outgoing edge $c$ of $v$.

More precisely, for every vertex $v$ and every choice of order 
$(c_1, \cdots, c_n)$ on $in(v)$ there is a generating operation

$$
  (c_1, \cdots, c_n) \to c
$$

and the action of an element of the [[symmetric group]] 
$\sigma \in S_n$ takes this to the generator

$$
  (c_{\sigma(1)}, \cdots, c_{\sigma(n)}) \to c
  \,.
$$

=--

+-- {: .num_example }
###### Example

The operad corresponding to the tree from example \ref{ATypicalTree}

* has six colours;

* has precisely six non-identity operations:

  * the generators $v$, $u$, $w$;

  * the composites $u \circ (v, id_c, id_d)$ and $u \circ (id_b, id_c, w)$ and $u \circ (v, id_c, w)$.

=--

The inclusion $\Omega \hookrightarrow$ [[Operad]] is the [[full subcategory]] on those operads that arise from trees in this way.

Some non-typical trees of importance are the following.

+-- {: .num_example #LinearTree}
###### Example

For every $n \in \mathbb{N}$ there is the **linear tree**

$$
  L_n
  :=
  \left\{
    \array{
      \downarrow^{0}
      \\
      \bullet_{01}
      \\
      \downarrow^{1}
      \\
      \bullet_{02}
      \\
      \vdots
      \\
      \downarrow^{n}
    }
  \right\}
$$

with $(n+1)$ colors and only unary operations.

The map that sends the [[simplicial set|simplicial]] [[simplex]] $\Delta^n$ to $L_n$
extends to a functor

$$
  \Delta \hookrightarrow \Omega
$$

which exhibits the [[simplex category]] as a [[full subcategory]] of the [[tree category]].

=--

+-- {: .num_example #Corolla}
###### Example

For each $n \in \mathbb{N}$ there is the **corolla tree**

$$
  C_n :=
  \left\{
    \array{
      {}_{\mathrlap{l_1}}\searrow & \cdots & \swarrow_{\mathrlap{l_n}}
      \\
      & \bullet 
      \\
      & \downarrow
    }
  \right\}
$$

with $n$ leaves and precisely one vertex.

=--

+-- {: .num_remark }
###### Remark

The trees $L_0$ and $C_0$ differ. $L_0$ is the tree

$$
  \left\{
    \downarrow
  \right\}
$$

with no vertex, while $C_0$ is the tree

$$
  \left\{
    \array{
      \bullet
      \\
      \downarrow
    }
  \right\}
$$

with a single vertex, which has valence 0.

=--


### Operations -- Faces and horns of trees
 {#OperationsFacesHorns}

A dendroidal set encodes composition of _operations_ in analogy to how a [[simplicial set]] encodes composition of edges: by way of _[[horn]] extensions_. In order to formalize this one uses the dendroidal analog of _faces_ of a [[simplex]], generalized from the [[simplex category]] to the [[tree category]].

To motivate the definition of dendroidal face maps, first consider the reformulation of simplicial faces under the map $i_! : sSet \to dSet$.

Under this embedding the $n$-simplex $\Delta[n]$ becomes the operad corresponding to the linear tree $L_n$, example \ref{LinearTree}

$$
  \stackrel{a}{\to} \bullet_{01} \stackrel{b}{\to} \bullet_{02} \stackrel{c}{\to} \cdots \to \bullet_{(n-1) n} \to
$$

with unary operations $\bullet_{i (i+1)}$.

The face inclusion $\delta_i : \Delta[n-1] \to \Delta[n]$ which simplicially omits the $i$th vertex, operadically contracts away the $i$th color, i.e it is the morphism of operads that sends the unary operation $\bullet_{(i-1)i}$ to the unary operation 

$$
  \bullet_{i (i+1)} \circ \bullet_{(i-1) i }
$$

and sends all other generating unary operation to generating unary operations.

From this it is clear that for any tree the map that exhibits the contraction of one edge should be a dendroidal face map. However, there are also some more cases to be taken care of. One has


1. inner face maps -- obtained by contracting an inner edge 

1. outer face maps -- obtained by 

   1. removing an outer input vertex

   1. removing a vertex whose output is the root and which has precisely one inner incoming edge (which becomes the new root)

   1. a corolla face -- any one of the inclusions of the tree with no vertex into a tree with precisely one vertex


+-- {: .num_defn }
###### Definition

For $T \in \Omega$ a tree and $e$ an _inner edge_ , write $T/e$ for the tree obtained by contracting/discarding this inner edge. There is a canonical inclusion 

$$
  \partial_e : T/e \to T
$$ 

in $\Omega$.

This is called an **inner face map** of $T$.

=--


+-- {: .num_example #ExampleForInnerFace}
###### Example

Let

$$
  T = 
   \left\{
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
  \right\}
$$

then 

$$
  T/e = 
   \left\{
    \array{
     \searrow && \searrow& & \swarrow 
     \\
      & \bullet &\to& \bullet &\to& 
     \\
     \nearrow
    }
  \right\}
$$

and the inclusion $T/e \to T$ is the operad morphism that is the identity on the operation  $
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

=--


In contrast to that, _outer_ edges are always removed together: 

+-- {: .num_defn }
###### Definition


If $v$ is a vertex of $T$ such that all but one edge incident on it are outer, then denote by $T/v$ the tree obtained by discarding $v$ and all the outer edges indicent on it. There is then again a canonical inclusion

$$
  \partial_v : T/v \to T
  \,.
$$

This is called an **outer face map**.

=--

+-- {: .num_example }
###### Example

With $T$ as from example \ref{ExampleForInnerFace}, we have

$$
  T/v 
   = 
   \left\{
    \array{
     \searrow & & \searrow^e
     \\
      & \bullet &\to& \bullet &\to& 
     \\
     \nearrow
    }
  \right\}
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

Let $T$ be a corolla tree, example \ref{Corolla}.
There are $n+1$ injections of the tree $L_0$ with no vertex $|$ into the corolla with $n$ inputs. 

$$
  | \hookrightarrow
  \array{
    \searrow &\cdots & \swarrow
    \\
    & \bullet
    \\
    & \downarrow
  }
  \,.
$$

These are called **corolla face maps** and counted as _outer face maps_.

=--

In terms of these face maps there is now a notion of _boundary_ and _horn_ of a tree in direct analogy to the notion of _[[boundary of a simplex]]_ and _[[horn]]_ in a simplex.

+-- {: .num_defn }
###### Definition

Let $T$ be a tree and let $Faces(T) \subset \Omega_{/T}$ be the set of all its face maps $\partial_\alpha \Omega[T] \to \Omega[T]$ , as defined above. The **boundary** of $T$ is the dendroidal set

$$
  \partial \Omega[T] := \coprod_{\alpha \in Faces(T)} \partial_\alpha \Omega[T]
$$ 

given by the [[union]] of all these faces in $\Omega[T]$.

For given $\alpha \in Faces(T)$, the $\alpha$-**horn** $\Lambda^\alpha[T] \in dSet$ of $T$ is the union of 
all faces except this one:

$$
  \Lambda^\alpha[T] 
   :=
  \coprod_{(\beta \neq \alpha) \in Faces(T)} \partial_\beta \Omega[T]
  \,.
$$

A horn is called an **outer horn** or an **inner horn** depending on whether the omitted face is outer or inner, respectively.

The inner horn corresponding to the inner face map given by contraction an edge $e$ is canonically denoted $\Lambda^a \Omega[T]$.

=--

These definitions are due to ([Weiss (thesis)](#WeissThesis)) and 
([MoerdijkWeiss](#MoerdijkWeiss)).


+-- {: .num_remark }
###### Remark

This is a genuine generalization of the notion of horns and boundaries of simplices. The outer/inner horns of the $n$-[[simplex]] $\Delta[n]$ are taken by $i_! : sSet \to dSet$ precisely to the outer/inner hors of the linear tree $L_n = i_!(\Delta^n)$.

=--

+-- {: .num_defn }
###### Definition

For $\Lambda^\alpha \Omega[T] \to \Omega[T]$ a horn inclusion and for $X \in dSet$ a dendroidal set, an **$\alpha$-horn in $X$** is a morphism of simplicial set

$$
  \Lambda^\alpha \Omega[T] \to X
  \,. 
$$

A **filler** of this horn in $X$ is an extension $\sigma$ in

$$
  \array{
    \Lambda^\alpha \Omega[T] &\to& X
    \\
    \downarrow & \nearrow
    \\
    \Omega[T]
  }
  \,. 
$$

=--

+-- {: .num_remark }
###### Remark

Choices of dendroidal _inner horn_ fillers correspond to _choices of composites_ of operations.

A dendrex $\Omega[T] \to X$ encodes a collection of operations and choices of theor composite in $X$. 

An inner horn $\Lambda^e \Omega[T] \to X$ encodes a choice of operations in $X$ and their composites _except_ a choice for the composition of operations along $e$. Picking a filler for this inner horn is picking such a choice.

The outer horn fillers have different interpretation. They correspond to choices of a) inverses of linear operations 2) invertible elements of $n$-ary operation. 

For more on this see _[[model structure on dendroidal sets]]_.

=--


### Skeletal filtration
  {#SkeletalFiltration}

+-- {: .num_defn #SkeletalFiltration}
###### Definition

For $X \in dSet$ a dendroidal set and $n \in \mathbb{N}$, write
$Sk_n(X) \in dSet$ for the dendroidal set which is generated from the 
non-degenerate $T$-dendrices for ${\vert T\vert} \leq n$.

The sequence of inclusions

$$
  Sk_0(X) \hookrightarrow Sk_1(X) \hookrightarrow Sk_2(X) \hookrightarrow
  \cdots \hookrightarrow X
$$

is called the **skeletal filtration** of $X$.

=--



### Normal monomorphisms and normal dendroidal sets
 {#NormalMonomorphisms}

A key fact in the theory of [[simplicial sets]] is that the [[monomorphisms]] there are generated under [[pushout]], [[transfinite composition]] and [[retracts]] from the [[boundary of a simplex|boundary inclusions]] (indeed the [[model structure on simplicial sets]] is a [[cofibrantly generated model category]] with generating cofibrations the boundary inclusions). 

For dendroidal sets the boundary inclusions turn out not to generate all monomorphisms, but just a subclass called the _normal_ monomorphisms. We discuss now the definition and some basic propoerties of normal monomorphisms. Most of these are a specialization of the general notion of [normal morphisms over a generalized Reedy category](http://ncatlab.org/nlab/show/generalized+Reedy+category#NormalMorphisms) to the [[generalized Reedy category]] $\Omega$.

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

+-- {: .num_defn #NormalMorphism}
###### Definition

A [[monomorphism]] $X \to Y$ of dendroidal sets is called **normal** if for any tree $T$, any non-degenerate dendrex $y \in Y(T)$ which does not belong to the image of $X(T)$ has a trivial [[stabilizer subgroup]] $Aut(T)_y \subset Aut(T)$ of the [[automorphism group]] of $T$.

A dendroidal set $X$ is called **normal** if $\emptyset \hookrightarrow X$ is a normal monomorphism. 

=--

+-- {: .num_remark}
###### Remark 

This is unrelated to the notion of _[[normal monomorphism]]_ in a context with [[zero morphisms]].  

=--

Here are some equivalent characterizations of normality.

+-- {: .num_prop}
###### Proposition

A dendroidal set $X$ is normal precisely if 
for every $n \in \mathbb{N}$ the canonical [[commuting diagram]]

$$
  \array{
    \coprod_{[\Omega[T] \stackrel{nd}{\to} X]} \partial \Omega[T]
    &\to&
    Sk_n(X)
    \\
    \downarrow && \downarrow
    \\
    \coprod_{[\Omega[T] \stackrel{nd}{\to} X]} \Omega[T]
    &\to&
    Sk_{n+1}(X)    
  }
$$

is a [[pushout]] diagram, where $\{Sk_n(X)\}$ is the skeletal filtration, def. \ref{SkeletalFiltration} and where the coproduct is over [[isomorphism classes]] of non-degenerate dendrices.

=--

+-- {: .num_prop}
###### Proposition

A monomorphism $f : X \to Y$ in [[dSet]] is normal precisely if for every $T \in \Omega$ the [[action]] of the [[automorphism group]] $Aut(T)$ on $Y(T)-X(T)$ is a [[free action]].

Accordingly, a dendroidal set $Y$ is normal precisely if for every $T \in \Omega$ the action of $Aut(T)$ on $Y(T)$ is [[free action|free]].

=--

This is  ([CisMoer09, prop 1.5](#CisMoer09)).

+-- {: .num_cor}
###### Corollary

For $f : X \to Y$ any morphism between dendroidal sets, then

* if $Y$ is normal, then $X$ is normal;

* if $Y$ is normal and $f$ is [[monomorphism|monic]], then $f$ is normal.

=--

+-- {: .num_example}
###### Example

* For every tree $T$, the dendroidal set $\Omega[T]$ is normal.

* For every [[simplicial set]], the dendroidal set $i_!(X)$ is normal.

=--



+-- {: .num_prop}
###### Proposition

The class of normal morphisms in [[dSet]] is generated from the boundary inclusions under 

* [[pushouts]];

* [[transfinite compositions]];

* [[retracts]].

In particular it is closed under these operations.

=--

This is  ([CisMoer09, prop 1.4](#CisMoer09)).


### Boardman-Vogt tensor product
 {#BoardmanVogtTensorProduct}

As any [[category of presheaves]], [[dSet]] is a [[cartesian monoidal category]]. However, the cartesian [[tensor product]] is not the natural one with respect to the inclusion of [[operads]] into dendroidal sets. The natural monoidal structure on [[Operad]] is rather a generalization of the [[Boardman-Vogt tensor product]].

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

With respect to this tensor product is [[dSet]] a colax symmetric monoidal category ( [Theorem 6.3.4 of HHM13](#HeutsHinichMoerdijk13)). This is discussed [below](#ClosedMonoidalStructure).

+-- {: .num_prop}
###### Proposition

For $A \to B$ and $X \to Y$ in [[dSet]] two normal monomorphisms, def. \ref{NormalMorphism}, 
the canonical morphism out of their [[pushout-product axiom|pushout product]]

$$
  (A \otimes Y) \coprod_{A \otimes X} (B \otimes X)
  \to
  B \otimes Y
$$

is also normal.

=--

This is ([CisMoer09, prop 1.9](#CisMoer09)).


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

* $i_!$ is a [[full and faithful functor]] defined equivalently as

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


The dendroidal set $i_!([n])$ that corresponds to the $n$-[[simplex]] is the linear tree; example \ref{LinearTree}, with $(n+1)$-edges:

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

The embedding of simplicial sets into dendroidal sets compatibly relates the [[cartesian monoidal category|Cartesian monoidal structure]] $(sSet, \times)$ with the [Boardman-Vogt monoidal structure](#BoardmanVogtTensorProduct) $(dSet, \otimes_{BV})$

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

in [[dSet]]. 

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

The **[[dendroidal homotopy coherent nerve]]** of a [[simplicial operad]] $P$ is the dendroidal set $hcN_d(P)$ given by

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

(or $W_!$ as [[model structure on dendroidal sets|here]])
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

Some [[mathematical structure|structure]] carried by the [[category]] [[dSet]] of [[dendroidal sets]]:

### Homotopical monoidal structure
 {#ClosedMonoidalStructure}

[Heuts-Hinich-Moerdijk 13, section 6.3](#HeutsHinichMoerdijk13)

### $sSet$-enriched structure 

Using the fact that [[dSet]] is a [[closed monoidal category]] with [[internal hom]] dendroidal sets $[C,D]$ for dendroidal sets $C$ and $D$, and using the functor $i^* : dSet \to SSet$ we obtain canonically the structure of an [[simplicially enriched category]] / [[sSet]]-[[enriched category]] on $dSet$ with the hom-simplicial set between $C$ and $D$ being $i^*[C,D]$.


### Model category structure

The category $dSet$ carries the Cisinski-Moerdijk [[model structure on dendroidal sets]]. With this model structure it forms a [[monoidal model category]]. 

Together with the fact that $i^*: dSet \to sSet$ is a [[right Quillen functor]] (with respect to the [[model structure for quasi-categories]]) this imples that [[dSet]] is an $sSet_{Joyal}$-[[enriched model category]] (but not, without further work, an $sSet_{Quillen}$-enriched model category!).

## Related concepts

* [[dSet]]

* [[model structure on dendroidal sets]]

* [[Cartesian fibration of dendroidal sets]]

* [[minimal dendroidal fibration]]

* [[simplicial set]], [[globular set]], [[cubical set]], [[cellular set]]

## References 
 {#References}

Textbook account:

* [[Gijs Heuts]], [[Ieke Moerdijk]], _Simplicial and Dendroidal Homotopy Theory_, Ergebnisse der Mathematik und ihrer Grenzgebiete **75**, Springer (2022) &lbrack;ISBN 9783031104473, 9783031104473, [doi:10.1007/978-3-031-10447-3](https://doi.org/10.1007/978-3-031-10447-3)&rbrack;

Surveys:

* [[Ieke Moerdijk]], _Lectures on dendroidal sets_ , lectures given at the Barcelona workshop on _[Simplicial methods in higher categories](http://www.crm.es/HigherCategories/)_ (2008) ([preliminary writeup](http://www.crm.cat/HigherCategories/hc1.pdf))

* {#Weiss} [[Ittay Weiss]], _From operads to dendroidal sets_ , in _[[Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, AMS (2011)
 
Dendroidal sets were introduced in 

* {#MoerdijkWeiss}  [[Ieke Moerdijk]] [[Ittay Weiss]], _Dendroidal sets_,  Algebraic & Geometric Topology 7 (2007) 1441&#8211;1470,  ([doi:10.2140/agt.2007.7.1441](http://msp.warwick.ac.uk/agt/2007/07/p056.xhtml), [arXiv:math.AT/0701293](http://arxiv.org/abs/math.AT/0701293))
 

A discussion of dendroidal inner Kan complexes (see also at _[[model structure on dendroidal sets]]_) appeared in

* [[Ieke Moerdijk]], [[Ittay Weiss]], _On inner Kan complexes in the category of dendroidal sets_, [math.CT/0701295](http://arxiv.org/abs/math/0701295)

The thesis

* [[Ittay Weiss]], _Dendroidal sets_ PhD thesis ([web](http://igitur-archive.library.uu.nl/dissertations/2007-0918-200833/UUindex.html))
 {#WeissThesis}

contains essentially the material of these two articles, together with a discussion of broad posets.

The [[model structure for dendroidal complete Segal spaces]] and the [[model structure for Segal operads]] was constructed in 

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal Segal spaces and infinity-operads_, ([arxiv:1010.4956](http://arxiv.org/abs/1010.4956))

Normal morphisms of dendroidal sets are discussed for instance around prop. 1.4 of

* {#CisMoer09} [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets as models for homotopy operads_ ([arXiv:0902.1954](http://arxiv.org/abs/0902.1954))
 
See also

* {#HeutsHinichMoerdijk13} Gijs Heuts, Vladimir Hinich, Ieke Moerdijk, _On the equivalence between Lurie's model and the dendroidal model for infinity-operads_ ([arXiv:1305.3658](https://arxiv.org/abs/1305.3658))


[[!redirects dendroidal sets]]

[[!redirects dendroidal nerve]]