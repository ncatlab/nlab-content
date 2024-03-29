
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _dendroidal homotopy coherent nerve_ is an [[operad|operadic]] generalization of the standard [[homotopy coherent nerve]]. It is a [[functor]]

$$
  hcN_d : Top Operad \to dSet
$$

from the [[category]] of [[Top]]-[[operads]] to that of [[dendroidal sets]], given by

$$
  hcsN_d(P) : T \mapsto dSet(W_H(T), P)
  \,,
$$

where $T$ is an object of the [[tree category]], regarded as a free [[symmetric operad]], and $W_H(T)$ is its [[Boardman-Vogt resolution]].

## Definition

Throughout, let $\mathcal{E}$ be a [[symmetric monoidal category|symmetric]] [[monoidal model category]] equipped with an [[interval object]] $H$ as discussed at _[[model structure on operads]]_ and  at _[[Boardman-Vogt resolution]]_. We consider multi-coloured [[symmetric operads]] ([[symmetric multicategories]]) enriched in $\mathcal{E}$.

Standard examples are $\mathcal{E} = $ [[Top]], [[sSet]], which yields [[topological operads]] and [[simplicial operads]], respectively.




### BV resolution of trees
 {#BVResolutionOfTrees}

We discuss in detail what the [[Boardman-Vogt resolution]] of [[operads]] free on an object in the [[tree category]] $\Omega$ is like (see _[[dendroidal set]]_ for details on trees as operads).

Let

$$
  Symm : \mathcal{E} Operad_{planar} \to \mathcal{E} Operad
$$

be the symmetrization functor, the [[left adjoint]] to the [[forgetful functor]] from [[symmetric operads]] to [[planar operads]]. 



+-- {: .num_prop}
###### Proposition

The BV resolution commutes with symmetrization: if $T = Symm(\bar T)$, then 

$$
  W(T) = Symm(W(\bar T))
  \,.
$$

=--

Therefore we describe in the following explicitly the BV-resolution of planar trees, that of non-planar trees then being the symmetrization of that construction.


+-- {: .num_prop #ComponentDescriptionofBVofTrees}
###### Proposition

For $T \in \Omega_{planar}$, and $(e_1, \cdots, e_n; e)$ a tuple of colours (edges) of $T$, notice that the set of operations $T(e_1, \cdots, e_n, e)$ is the set of those subtrees $V \subset T$ such that $\{e_1, \cdots, e_n\}$ is the set of leaves and $e$ is the root of $V$.

First regard $T$ as a [[topological operad]] (with a [[discrete space]] of operations in each degree). The corresponding [[Boardman-Vogt resolution]] $W(T)$ of $T$ is the topological operad whose [[topological space]] of operations $W(T)(e_1, \cdots, e_n; e)$ is the space of _labeled trees_ as follows.

A point is a set of _lengths_ $\ell(e) \in [0,1]$, one for each inner edge $e \in I(T)$ of $T$. (...)

Hence 

$$
  W(T)(e_1, \cdots, e_n; e) 
    \simeq 
  \coprod_{V \in T(e_1, \cdots, e_n; e)}
  (\Delta^1)^{\times i(V)}
$$

where the [[coproduct]] ranges over the set of subtrees $V$, as just discussed (which therefore is either the singleton set or is empty), and where $i(V)$ is the set of inner edges of $V$.


Regard then $T$ as a [[simplicial operad]]. The corresponding [[Boardman-Vogt resolution]] $W(T)$ of $T$ is the simplicial operad whose [[simplicial sets]] of operations are

$$  
  W(T)(e_1, \cdots, e_n; e)
  =
  \coprod_{V \in T(e_1, \cdots, e_n; e)}
  \Delta[1]^{\times i(V)}
  \,.
$$

In general, when $T$ is regarded as an $\mathcal{E}$-operad, we have

$$  
  W(T)(e_1, \cdots, e_n; e)
  =
  \coprod_{V \in T(e_1, \cdots, e_n; e)}
  H^{\otimes i(V)}
  \,,
$$

where $H$ is the given [[interval object]].

=--


+-- {: .num_prop #CompositioninWT}
###### Observation

The composition operations in $W(T)$

$$
  \array{
    W(T)(e_1, \cdots, e_n; e_0) \otimes W(T)(f_1, \cdots, f_k; e_i)
    \\
    \downarrow^{\mathrlap{\circ_i}}
    \\
    W(T)(e_1, \cdots, e_{i-1}, f_1, \cdots, f_k, e_{i+1}, \cdots, e_n)
  }
$$

correspond to grafting of trees $T_\sigma, T_\rho \subset T$ and "assigning unit length to the new inner edge". On the components as discussed above it is given by

$$
  \array{
    H^{\otimes i(T_\sigma)} \otimes H^{\otimes i(T_\rho)}
    &&
    H^{\otimes i(T_\sigma \circ_i T_\rho)}
    \\
    \downarrow^{\mathrlap{\simeq}}
    &&
    \uparrow^{\mathrlap{\simeq}}
    \\
    H^{\otimes i(T_\sigma) \cup i(T_\rho)} \otimes I
     &\stackrel{id \otimes i_1}{\to}&
    H^{\otimes (i(T_\sigma) \cup i(T_\rho))} \otimes H
  }
$$

=--


+-- {: .num_prop #BVResolutionAsFunctorOnOmega}
###### Proposition

The BV-resolution of trees extends to a [[functor]] on the category of [[simplicial operad]]

$$
  W : \Omega \to sSet Operad
$$

as follows

* on an inner face map $\delta_e : \partial^e\Omega[T] \to \Omega[T]$ the component of $W(\delta)$ on a subtree $V$ of $T$ that contains the edge $e$ is the product of the inclusion
 
  $$
    i_0 : I \to H
  $$

  with the identity on $H^{i(V)-\{e\}}$

  (meaning: if the label of an inner edge in a tree is 0, then the operations that it connects may be composed);

* on a degenracy map $\sigma $ that sends two given unary vertices to a single one, the component of $W(\sigma)$ on subtrees containing these removes one of the factors $H$ by the map

  $$
    H \otimes H \to H
  $$
  
  given by the [[interval object]] $H$. For both [[simplicial operads]] and [[topological operads]] this may be taken to be the map

  $$
    max : \Delta^1 \times \Delta^1 \to \Delta^1
  $$

  that sends $(x,y)$ to $max(x,y)$.

=--

This is discussed in section 4.2 of ([Cisinski-Moerdijk](#CisinskiMoerdijk)).

### The homotopy coherent nerve

By the general discussion at _[[nerve and realization]]_, the functor

$$
  W
  : 
  \Omega 
  \to  
  sSet Operad
$$

from prop. \ref{BVResolutionAsFunctorOnOmega} induces a [[nerve]] functor as follows.

+-- {: .num_defn}
###### Definition

The **dendroidal homotopy coherent nerve** functor is the [[functor]]

$$
  hcN_d : sSet Cat \to dSet
$$

given by 

$$
  P \mapsto ( T \mapsto sSet Operad(W(T), P) )
  \,.
$$

Its [[left adjoint]] (the corresponding "[[geometric realization]]") we denote

$$
  W_! : dSet \to sSet Operad
  \,.
$$


=--



## Properties


### Specialization to categories

+-- {: .num_prop}
###### Proposition

When restricted to $\mathcal{E}$-[[enriched categories]], the dendroidal homotopy coherent nerve reproduces the [[homotopy coherent nerve]] of enriched categories

$$
  \array{
    \mathcal{E} Cat &\hookrightarrow& \mathcal{E} Operad
    \\
    {}^{\mathllap{hcN}}\downarrow && \downarrow^{\mathrlap{hcN_d}}
    \\
    sSet &\hookrightarrow& dSet
  }
  \,.
$$

In particular for $\mathcal{E} = $ [[Top]] / [[sSet]] it reproduces the original definition of homotopy coherent nerve.

=--


### Dendroidal inner Kan complexes
 {#DendroidalInnerKanComplexes}


+-- {: .num_prop #hcNOfLocllyFibrantOperadIsFibrant}
###### Proposition

Let $P \in \mathcal{E} Operad$ be such that each object of operations is fibrant in $\mathcal{E}$. Then its homotopy coherent nerve $hcN_d(P)$ is a [[model structure on dendroidal sets|dendroidal inner Kan complex]].

=--

This is ([Moerdijk-Weiss, theorem 7.1](#MoerdijkWeiss)).
This statement will also follow as a corollary from prop. \ref{WIsLeftQuillen} below.

+-- {: .proof}
###### Proof

Consider a tree $T$ and an inner edge $e$ of it. For each morphism 
$\phi : \Lambda^e[T] \to X$ we need to find a filler $\psi$ in

$$
  \array{
    \Lambda^e[T] &\to& hcN_d(X)
    \\
    \downarrow & \nearrow_{\mathrlap{\psi}}
    \\
    \Omega[T]
  }
  \,.
$$

Write $\Lambda^e[T] = \cup_{i \neq e}\partial^{i \neq e} \Omega[T]$. 

By the definition of dendroidal nerve, this is equivalently a diagram

$$
  \array{
    \cup_{i \neq e } W(\partial^i \Omega[T]) &\to& X
    \\
    \downarrow & \nearrow_{\mathrlap{\hat \psi}}
    \\
    W(\Omega[T])
  }
  \,.
$$

The undetermined component to fill is that corresponding to the subtree $\tau$ of $T$ which is $T$ itself. According to prop. \ref{ComponentDescriptionofBVofTrees} on this 
the operad $W(\Omega[T])$ has the component 

$$
  H^{\otimes i(\tau)} \simeq H^{\otimes i(\tau)- \{e\}}\otimes H
  \,.
$$

The map $\hat \psi$ has to send this into $X$ while being compatible with the given faces. By prop. \ref{BVResolutionAsFunctorOnOmega} this means that its precomposition with all the inclusions

$$
  (id, \cdots, id, i_0, id, \cdots, id) \otimes id
  : 
  H \otimes \cdots \otimes H \otimes I \otimes H \otimes \cdots \otimes H \otimes H
  \to 
  H^{\otimes i(\tau)- \{e\}}\otimes H
$$

is fixed. Moreover, the assignment needs to be compatible with the composition operations, which by prop. \ref{CompositioninWT} means that also the precomposition with all the maps 

$$
  (id, \cdots, id, i_1, id, \cdots, id)
  : 
  H \otimes \cdots \otimes H \otimes I \otimes H \otimes \cdots \otimes H
  \to 
  H^{\otimes i(\tau)}
$$

is fixed. In total this means that the components of $\hat \psi$ need to form an extension of the form

$$
  \array{
    (\partial H^{\otimes i(\tau)- \{e\}})
    \otimes H
    \cup
    H^{\otimes i(\tau) - \{e\}}\otimes I
    &\to& X(\tau)
    \\
    \downarrow & \nearrow
    \\
    H^{\otimes i(\tau)}
  }
$$

in $\mathcal{E}$, where 

$$
  \partial H^n := 
    (I \coprod I) \otimes H^{n-1}
    \coprod
    H (I \coprod I) \otimes H^{n-2}
    \coprod
    \cdots
    \stackrel{(i_0,i_1)\otimes id \coprod \cdots}{\to}
    H^n
  \,.
$$

One sees that the left vertical morphism is an acyclic cofibration, by the [[pushout-product axiom]] in the [[monoidal model category]] $\mathcal{E}$. Therefore by the assumption that $X(\tau)$ is fibrant, such a lift does exist.

=--


### Left adjoint 
  {#LeftAdjoint}

+-- {: .num_defn}
###### Definition

Write

$$
  W_! : dSet \to sSet Operad
$$

for the [[Yoneda extension]] of 

$$
  \Omega \hookrightarrow Operad \hookrightarrow sSet Operad \stackrel{W}{\to} sSet Operad
  \,;
$$

hence for the [[functor]] from [[dendroidal sets]] to [[simplicial operads]], which 

* preserves [[colimits]];

* on trees $\Omega \hookrightarrow Operad \hookrightarrow sSet Operad$ 
  is given by the [[Boardman-Vogt resolution]] as discussed [above](#BVResolutionOfTrees).

=--

By the general lore of [[nerve and realization]] we have

+-- {: .num_prop}
###### Proposition

$W_!$ is [[left adjoint]] to $hcN_d$

$$
  (W_! \dashv hcN_d)
  : 
  sSet Operad
  \stackrel{\overset{N_d}{\leftarrow}}{\underset{hcN_d}{\to}}
 dSet
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

For $P \in sSet Operad$, the [[unit of an adjunction|counit]]

$$
  W_! hcN_d (P) \to P
$$

is essentially the [[Boardman-Vogt resolution]] of $P$.

For a cofibrant and fibrant $X \in dSet$, the [[unit of an adjunction|unit]]

$$
  X \to hcN_d W_!(X)
$$

may be viewed as a "strictification" of the [[(infinity,1)-operad]] given by $X$, in that  $W_!(X)$, being a simplicial operad, has strictly associative composition.

=--

### Relation to ordinary dendroidal nerve

By the general properties of the [[Boardman-Vogt resolution]] 
(but also immediately checked directly) we have

+-- {: .num_prop #CounitOfResolutionOnTrees}
###### Proposition

There is a [[natural transformation]]

$$
  \epsilon : W \Rightarrow \Omega(-) : \Omega \to sSet Operad
$$

$$
  \epsilon_T : W(T) \to T
$$

(natural in the tree $T \in \Omega$), which is a bijection on colors and is 
on the components of prop. \ref{ComponentDescriptionofBVofTrees} the canonical map

$$
  \Delta[1]^{i(V)} \to *
  \,.
$$

Each $\epsilon_T$ is hence a weak equivalence of simplicial operads. In particular

$$
  \pi_0(W(T)) \to T
$$

is an [[isomorphism]].

=--

This induces hence a [[natural transformation]]

$$
  W_! \Rightarrow \tau_d : dSet \to sSet Operad
$$

to the left adjoint $\tau_d$ of the ordinary [[dendroidal nerve]] (the "fundamental operad" construction).

+-- {: .num_prop}
###### Proposition

For every [[dendroidal set]] $X$, the natural morphism

$$
  \pi_0 W_!(X) \to \pi_0 \tau_d (X) = \tau_d(X)
$$

is an [[isomorphism]] of simplicial operads.

=--

This appears as [Cisinski-Moerdijk, prop. 4.4](#CisinskiMoerdijk).

+-- {: .proof}
###### Proof

The functors $\pi_0 W_!$ and $\tau_d$, being [[left adjoints]], both preserve small [[colimits]]. Therefore it is sufficient to check the statement for $X = \Omega[T]$ a tree. There it is prop. \ref{CounitOfResolutionOnTrees}.

=--



### Quillen equivalence

+-- {: .num_theorem }
###### Theorem

The [[adjunction]] $(W_! \dashv hcN_d)$ from [above](#LeftAdjoint) is a [[Quillen equivalence]] between the [[model structure on operads]] over [[Top]]/[[sSet]] and the [[model structure on dendroidal sets]].

=--

We discuss some input to this statement.

+-- {: .num_prop #WIsLeftQuillen}
###### Proposition

The functor $W_! : dSet \to sSet Operad$ sends normal monomorphisms to cofibrations, and inner 
[[anodyne extensions]] to [[acyclic cofibrations]] in the [[model structure on sSet-operads]].

=--

This appears as [Cisinski-Moerdijk, prop. 4.5](#CisinskiMoerdijk).

+-- {: .proof}
###### Proof

Observe that the morphism classes in question are, as discussed at _[[dendroidal set]]_, the saturated classes generated by the dendroidal boundary inclusions and by the dendroidal horn inclusions, respectively.

Since $W_!$ is left adjoint, it therefore suffices to check the statement on these generating inclusions. Moreover, by construction, on trees $W_!$ coincides with the [[Boardman-Vogt resolution]] of the operads free on these trees.

It follows that the generating inclusions are sent by $W_!$ to morphisms of simplicial operads which are

* bijective on objects;

* isomorphisms on all but one simplicial set of operations: that corresponding to the maximal subtree;

* on this remaining simplicial set of operations a product of identities with cofibrations of simplicial sets (monomorphisms), and following through the combinatorics shows that these are acyclic for the case of anodyne extensions.

It follows that these morphisms of simplicial operads have the left lifting property again operation-object-wise [[Kan fibrations]] (there is no further composition to be respected, since the maximal subtree operation has no further non-trivial composites), and hence against the fibrations of the [[model structure on sSet-operads]].


=--

+-- {: .num_remark}
###### Remark

Prop.\ref{hcNOfLocllyFibrantOperadIsFibrant} is, in turn, a direct consequence of this.

=--

### Resolution and rectification

+-- {: .num_prop}
###### Proposition

Let $P$ be an [[operad]] in [[Set]], regarded as an $\mathcal{E}$-operad. Then the $(W_! \dashv hcN_d)$-[[unit of an adjunction|counit]]

$$
  W_! N_d(P) = W_! hcN_d (P) \to P
$$

is isomorphic to the [[Boardman-Vogt resolution]] $W_H(P)$ of $P$.

In particular, therefore, there is a [[natural isomorphism]]

$$
  Hom_{\mathcal{E}Operad}(W_H(P), Q)
  \simeq
  Hom_{dSet}(N_d(P), hcN_d(Q))
  \,.
$$

=--

(Here we are using that on a discrete operad $P$ the homotopy coherent dendroidal nerve trivially coincides with the ordinary dendroidal nerve $N_d$.)

+-- {: .proof}
###### Proof

By inspection of the relevant formulas.

=--

+-- {: .num_prop}
###### Proposition

For a cofibrant and fibrant dendroidal set $X$, the $(W_! \dashv hcN_d)$-[[unit of an adjunction|unit]] 

$$ 
  X \to hcN_d W_! X
$$

is an equivalence.

=--

+-- {: .num_remark}
###### Remark

Since composition of operations in a simplicial operad is strictly associative,  this may be understood as producing a semi-strictification of the $\infty$-operad $X$.

=--

## Related concepts

[[!include table - models for (infinity,1)-operads]]
  

## References

The fact that the homotopy coherent nerve if a locally fibrant operad is inner Kan is shown in section 7 of 

* [[Ieke Moerdijk]], [[Ittay Weiss]], _On inner Kan complexes in the category of dendroidal sets_, ([math.CT/0701295](http://arxiv.org/abs/math/0701295))
 {#MoerdijkWeiss}

The Quillen adjunction properties of the homotopy coherent dendroidal nerve are discussed in section 4 of

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets and simplicial operads_ ([arXiv:1109.1004](http://arxiv.org/abs/1109.1004))
 {#CisinskiMoerdijk}

Lecture notes on these two topics are in section 6 and 9 of

* [[Ieke Moerdijk]], _Lectures on dendroidal sets_ , lectures given at the Barcelona workshop on _[Simplicial methods in higher categories](http://www.crm.es/HigherCategories/)_ (2008) ([preliminary writeup](http://www.crm.cat/HigherCategories/hc1.pdf))



[[!redirects homotopy coherent dendroidal nerve]]
