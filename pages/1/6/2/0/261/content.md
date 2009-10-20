#Content#
* automatic table of contents goes here
{:toc}

#Idea#

A _simplicial set_ is like a combinatorial space built up out of gluing abstract [[simplex|simplices]] to each other. Equivalently, it is an object equipped with a rule for how to consistently map the objects of the [[simplex category]] into it.

More concretely, a simplicial set $S$ is a collection of [[sets]] $S_n$ for $n \in \mathbb{N}$, so that elements in $S_n$ are to be thought of as one $n$-[[simplex|simplices]], equipped with a rule that says:

* which $(n-1)$-simplices in $S_{n-1}$ are faces of which elements of $S_n$;
* which $(n+1)$-simplices are [[thin element|thin]] in that they are really just $n$-simplices regarded as degenerate $(n+1)$-simplices.

One of the main uses of simplicial sets is as combinatorial _models_ for [[topological spaces]]. They can also be taken as models for [[∞-groupoids]]. This is encoded in the [[model structure on simplicial sets]].

#Definition#

A **simplicial set**  is a [[presheaf]] on the [[simplex category]] $\Delta$, that is, a functor $X : \Delta^{op} \to Sets$.

This is, of course, a [[simplicial object]] in the category [[Set]] of sets.

With the standard morphisms of [[presheaf|presheaves]] as morphisms, simplicial sets form the category [[SimpSet]] (also called $SSet$ or $sSet$).

#Remarks#

## simplicial sets as spaces built of simplices ##

* The definition is to be understood from the point of view of [[space and quantity]]: a **simplicial set** is a space characterized by the fact that and how it may be _probed_ by mapping standard simplices into it: the set $S_n$ assigned by a simplicial set to the standard $n$-simplex $[n]$ is the **set of $n$-simplices** in this space, hence the way of mapping a standard $n$-simplex into this spaces.

* For $S$ a simplicial set, the **face map** 
  $$
    d_i := S(\delta^i): S_n \rightarrow S_{n-1}
  $$ 
  is dual to the unique injection $\delta^i : [n-1] \rightarrow [n]$ in the category $\Delta$ whose image omits the element $i \in [n]$. 

* Similarly, the **degeneracy map** 
  $$
    s_i := S(\sigma^i) : S_n \rightarrow S_{n+1}
  $$ 
  is dual to the unique surjection $\sigma^i : [n+1] \rightarrow [n]$ in $\Delta$ such that $i \in [n]$ has two elements in its preimage. 

* The maps $\delta^i$ and $\sigma^i$ satisfy certain obvious relations -- the [[simplicial identities]] -- dual to those  spelled out at [[simplex category]].


## Visualisation
(based on [[cubical set]])

The **face maps**  go from sets $S_{n+1}$ of $(n+1)$-dimensional simplices to the corresponding set $S_{n}$ of $n$-dimensional simplices and can be thought of as sending each simplex in the simplicial set to one of its faces, for instance for $n=1$ the set $S_2$ of 2-simplices would be sent in three different ways by three different face maps to the set of $1$-simplices, for instance one of the face maps would send

$$
  \left(
  \array{
       &          & b
     \\
       & \nearrow & \Downarrow^F & \searrow
     \\
     a &          & \rightarrow  &          & c
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
       &          & b
     \\
       & \nearrow
     \\
     a
  }
  \right)
$$

another one would send

$$
  \left(
  \array{
       &          & b
     \\
       & \nearrow & \Downarrow^F & \searrow
     \\
     a &          & \rightarrow  &          & c
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
     a &          & \rightarrow  &          & c
  }
  \right)
  \,.
$$

On the other hand, the **degeneracy maps** go the other way round and send sets $S_n$ of $n$-simplices to sets $S_{n+1}$ of $(n+1)$-simplices by regarding an $n$-simplex as a degenerate or "thin" $(n+1)$-simplex in the various different ways that this is possible. For instance again for $n=1$ a degeneracy map may act by sending

$$
  \left(
  \array{
     a
     &\stackrel{f}{\to}&
     b
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
       &            & b
     \\
       & \nearrow_f & \Downarrow^{Id} & \searrow^{Id}
     \\
     a &            & \stackrel{f}\to &               & b
  }
  \right)
  \,.
$$

Notice the $Id$-labels, which indicate that the edges and faces labeled by them are "[[thin element|thin]]" in much the same way as an [[identity morphism]] is thin (notice however that a simplicial set by itself is not equipped with a notion of composition of simplices. If it were, we'd call it a [[simplicial category]]).


## simplicial complexes ##

Simplicial sets generalize the idea of [[simplicial complex]]: a simplicial set can be thought of as something consisting of a set of $n$-simplices for all $n \in \mathbb{N}$ together with face and degeneracy functions. More precisely, if $X$ is a simplicial set, we write $X_n$ to denote the set of $n$-simplices. The **face** maps (also called **boundary** maps) are functions $d_i : X_n \rightarrow X_{n-1}$ for each $0\leq i \leq n$, which associate to each $n$-simplex one of its $n+1$ faces, themselves $(n-1)$-simplices. The **degeneracy** maps are functions $s_i : X_n \rightarrow X_{n+1}$ for each $0\leq i \leq n$, which allow one to regard an $n$-simplex as a degenerate $(n+1)$-simplex. 



#Examples#

* Let $[n]$ denote the object of $\Delta$ corresponding to the totally ordered set $\{ 0, 1, 2,\ldots, n\}$. Then the represented presheaf $\Delta(-, [n])$, which we typically write as $\Delta[n]$ is an example of a simplicial set. By the Yoneda lemma, the $n$-simplices of a simplicial set $X$ are in natural bijective correspondence to maps $\Delta[n] \rightarrow X$ of simplicial sets.

* If $C$ is a small category, the **nerve** of $C$ is a simplicial set which we denote $NC$. If we intepret the poset $[n]$ defined above as a category, we define the $n$-simplices of $NC$ to be the set of functors $[n] \rightarrow C$. Equivalently, the $0$-simplices of $NC$ are the objects of $C$, the $1$-simplices are the morphisms, and the $n$-simplices are strings of $n$ composable arrows in $C$. Face maps are given by composition (or omission, in the case of $d_0$ and $d_n$) and degeneracy maps are given by inserting identity arrows.

* Recall from [[simplex category]] or [[geometric realization]] the standard functor $\Delta \to Top$ which sends $[n] \in \Delta$ to the standard topological $n$-simplex.  This functor induces for every [[topological space]] $X$ the simplicial set
$$
  S X : [n] \mapsto Hom_{Top}(\Delta^n, X)
$$
called the **simplicial singular complex** of $X$. This simplicial set is always a [[Kan complex]] and may be regarded as the [[fundamental ∞-groupoid]] of $X$.



* A [[symmetric set]] is a simplicial set equipped with additional *transposition maps* $t^n_i: X_n \to X_n$ for $i=0,\ldots,n-1$.  These transition maps generate an [[action]] of the [[symmetric group]] on $X_n$ and satisfy certain commutation relations with the face and degeneracy maps.

#The category of simplicial sets#

Like all categories of [[presheaf|presheaves]] on a [[small category]], the [[category]] [[SimpSet]] of simplicial sets is complete and cocomplete (with [[limits]] and [[colimits]] constructed levelwise) and [[cartesian closed category|cartesian closed]]. In fact, like all [[presheaf|presheaf categories]], it is a [[topos]]. 

### monoidal structure ##

As described at [[closed monoidal structure on presheaves]]
the cartesian tensor product $S \otimes T = S \times T$ of simplicial sets $S$ and $T$ is the simplicial set
$$
  (S \otimes T) : [n] \mapsto S_n \times T_n
  \,,
$$
where the product on the right is the cartesian product in [[Set]].

One cental reason why simplicial sets are useful and important is that this simple monoidal structure ("disturbingly simple minded" in the words of [Friedman08, p. 24](http://arxiv.org/PS_cache/arxiv/pdf/0809/0809.4221v1.pdf#page=24)) actually does fully capture the standard monoidal structure on [[topological spaces]] under [[geometric realization]] $|\cdot| : SSet \to Top$

+-- {: .un_prop}
###### Proposition

For $S$ and $T$ simplicial sets, we have
$$
  |S \times T| \simeq |S| \times |T|
  \,,
$$
where on the right the cartesian product is in the [[nice category of spaces|nice category]] of compactly generated Hausdorff spaces.
=--

## closed structure ##

As described at [[closed monoidal structure on presheaves]]
the [[internal hom]]  $[S,T]$ of simplicial sets is the simplicial set
$$
  [S,T] : [n] \mapsto Hom_{SSet}(S \times \Delta^n, T)
  \,,
$$
where $\Delta^n = Y([n])$ is the standard simplicial $n$-[[simplex]], the image of $[n] \in \Delta$ under the [[Yoneda embedding]].


# Adjunctions #

The maps $N: \Cat \rightarrow \Simp\Set$ and $S: \Top \rightarrow \Simp\Set$ described in the examples are actually functors, both of which have left adjoints. These adjoint pairs are examples of a very general sort of adjunction involving simplicial sets, of which there are many examples.

Let $E$ be any cocomplete category and let $F: \Delta \rightarrow E$ be a functor. We define the right adjoint $R : E \rightarrow \Simp\Set$ as follows. Given an object $e \in E$ the $n$-simplices of $Re$ are defined to be the set $E(F[n],e)$ of morphisms in $E$ from $F[n]$ to $e$. Face and degeneracy maps are given by precomposition by the appropriate (dual) maps in the image of $F$. $R$ is defined on morphisms by postcomposition. 

The left adjoint $L$ is defined to be the left [[Kan extension]] of $F$ along the Yoneda embedding $y: \Delta \rightarrow \Simp\Set$. Because the $y$ is full and faithful, we will have $Ly = F$, i.e., $L (\Delta[n]) = F[n]$. By specifying $F$, we have already defined a functor to $E$ on the represented simplicial sets; $L$ is the unique cocontinuous extension of this functor to $\Simp\Set$. It can be described explicitly on objects as a [[end|coend]], or as a [[weighted limit|weighted colimit]].

(Easy) abstract nonsense shows that $L$ and $R$ form an adjoint pair $L \dashv R$.

Here are some examples:

* Let $E = \Cat$ and $F$ be the functor $[n] \mapsto [n]$ (the inclusion of posets into categories). The right adjoint is the nerve functor $N$ described above. The left adjoint ${\tau}_1$ takes a simplicial set to its **fundamental category**. 

* Let $E = \Top$ and $F$ be the functor $[n] \mapsto {\Delta}_n$. The right adjoint is the total singular complex functor $S$ described above. The left adjoint $|-|$ is called **geometric realization**.  As a consequence of the Kan extension construction, the geometric realization of the represented simplicial set $\Delta[n]$ is the standard $n$-simplex ${\Delta}_n$.

* (Barycentric) subdivision and extension $\sd: \Simp\Set \leftrightarrow \Simp\Set :\ex$.

* The [[homotopy coherent nerve]] functor and its left adjoint $\Simp\Set \leftrightarrow \Simp\Cat$ where [[SimpCat]] denotes the category of [[simplicially enriched category|simplicially enriched categories]], i.e., categories enriched in $\Simp\Set$.

+-- {: .query}
[[Tim Porter|Tim]]: What is the reference for this simplicial nerve? (I do not like that terminology.)  Is it what I would call the homotopy coherent nerve (as explicitly first introduced by Cordier)? If so it needs an entry for itself.

[[Urs Schreiber|Urs]]: I guess it should be the notion introduced in 

* Cordier, J. M. Sur la notion de diagramme homotopiquement coh&#180;erent. Cahiers Top. et Geom. Diff.
XXIII 1, 1982, 93-112.

Over at [[geometric ∞-function theory]] I am asking for an entry titled [[simplicial nerve of simplicial categories]]. Likely not a good term either. I took "simplicial nerve" from [section 1.1.5, p. 26](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=26) of [[Higher Topos Theory|HTT]].

=--

* The adjunction $- \times X: \SimpSet \leftrightarrow \SimpSet :(-)^X$ between the product with a simplicial set $X$ and the internal-hom, which makes $\Simp\Set$ into a [[cartesian closed category]].

#References#

A pedagogical introduction to simplicial sets is

* Greg Friedman, _An elementary illustrated introduction to simplicial sets_ ([arXiv](http://arxiv.org/abs/0809.4221))

A useful (if old) survey article is: 

*  E. Curtis, _Simplicial Homotopy Theory_, Advances in Math., 6, (1971), 107 &#8211; 209.


More advanced treatments include 

* P. G. Goerss and J. F. Jardine, 1999, _Simplicial Homotopy Theory_, number 174 in Progress in Mathematics, Birkhauser. ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

+--{: .query}
[[Tim Porter|Tim]]:  We seem to have managed to have two notations for the basic simplices in simplicial sets.  There are pages with $\Delta[n]$ and those with $\Delta^n$. (I prefer the former.) This is confusing! 

My preferred notation is $\Delta[n]$ for the representable simplicial set $\Delta(-,[n])$, with its geometric realisation being $\Delta^n$. These are quite different beasties and it seems a shame to use the same notation for both. Should we rationalise/standardise the notation?

[[Urs Schreiber|Urs]]: would be fine with me 
(I am probably responsible for much of the $\Delta^n$s) -- on the other hand, globally consistent notation over the $n$Lab will generally be a challange. But we should try. Yes.

=--

[[!redirects simplicial sets]]