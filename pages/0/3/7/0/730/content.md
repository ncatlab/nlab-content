
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
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

## Definition

The [[category]] $SimpSet$, or $sSet$ for short, is the category of [[simplicial set]]s.

This is the [[functor category]] from the [[opposite category]] $\Delta^{op}$ of the [[simplex category]] $\Delta$ to the category [[Set]] of sets:

$$
  Simp Set := [\Delta^{op}, Set]
  \,.
$$

Its [[object]]s are [[simplicial set]]s.

## Properties


Like all categories of [[presheaf|presheaves]] on a [[small category]], the [[category]] [[SimpSet]] of simplicial sets is complete and cocomplete (with [[limits]] and [[colimits]] constructed levelwise) and [[cartesian closed category|cartesian closed]]. In fact, like all [[presheaf|presheaf categories]], it is a [[topos]]. 

### Monoidal structure

As described at [[closed monoidal structure on presheaves]]
the cartesian tensor product $S \otimes T = S \times T$ of simplicial sets $S$ and $T$ is the simplicial set
$$
  (S \otimes T) : [n] \mapsto S_n \times T_n
  \,,
$$
where the product on the right is the cartesian product in [[Set]].

One central reason why simplicial sets are useful and important is that this simple monoidal structure ("disturbingly simple minded" in the words of [Friedman08, p. 24](http://arxiv.org/PS_cache/arxiv/pdf/0809/0809.4221v1.pdf#page=24)) actually does fully capture the standard monoidal structure on [[topological spaces]] under [[geometric realization]] $|\cdot| : SSet \to Top$

+-- {: .un_prop}
###### Proposition

For $S$ and $T$ simplicial sets, we have
$$
  |S \times T| \simeq |S| \times |T|
  \,,
$$
where on the right the cartesian product is in the [[nice category of spaces|nice category]] of compactly generated Hausdorff spaces.
=--


See also [[products of simplices]].


### Closed structure

As described at [[closed monoidal structure on presheaves]]
the [[internal hom]]  $[S,T]$ of simplicial sets is the simplicial set
$$
  [S,T] : [n] \mapsto Hom_{SSet}(S \times \Delta[n], T)
  \,,
$$
where $\Delta[n] = Hom_{\mathbf{\Delta}}(-,[n])$ is the standard simplicial $n$-[[simplex]], the image of $[n] \in \mathbf{\Delta}$ under the [[Yoneda embedding]]. This formula is clearly representing a Kan extension. 


### Adjunctions 

The maps $N: \Cat \rightarrow \Simp\Set$ and $S: \Top \rightarrow \Simp\Set$ described in the examples are actually functors, both of which have left adjoints. These adjoint pairs are examples of a very general sort of adjunction involving simplicial sets, of which there are many examples.

Let $E$ be any cocomplete category and let $F: \Delta \rightarrow E$ be a functor. We define the right adjoint $R : E \rightarrow \Simp\Set$ as follows. Given an object $e \in E$ the $n$-simplices of $Re$ are defined to be the set $E(F[n],e)$ of morphisms in $E$ from $F[n]$ to $e$. Face and degeneracy maps are given by precomposition by the appropriate (dual) maps in the image of $F$. $R$ is defined on morphisms by postcomposition. 

The left adjoint $L$ is defined to be the left [[Kan extension]] of $F$ along the Yoneda embedding $y: \Delta \rightarrow \Simp\Set$. Because the $y$ is full and faithful, we will have $Ly = F$, i.e., $L (\Delta[n]) = F[n]$. By specifying $F$, we have already defined a functor to $E$ on the represented simplicial sets; $L$ is the unique cocontinuous extension of this functor to $\Simp\Set$. It can be described explicitly on objects as a [[end|coend]], or as a [[weighted limit|weighted colimit]].

(Easy) [[category theory|abstract nonsense]] shows that $L$ and $R$ form an [[adjunction|adjoint pair]] $L \dashv R$.

Here are some examples:

* Let $E = \Cat$ and $F$ be the functor $[n] \mapsto [n]$ (the inclusion of posets into categories). The right adjoint is the nerve functor $N$ described above. The left adjoint ${\tau}_1$ takes a simplicial set to its **fundamental category**. 

* Let $E = \Top$ and $F$ be the functor $[n] \mapsto {\Delta}_n$. The right adjoint is the total singular complex functor $S$ described above. The left adjoint $|-|$ is called **[[geometric realization]]**.  As a consequence of the Kan extension construction, the geometric realization of the represented simplicial set $\Delta[n]$ is the standard $n$-simplex ${\Delta}^n$.

* (Barycentric) subdivision and extension $\sd: \Simp\Set \leftrightarrow \Simp\Set :\ex$.

* The [[homotopy coherent nerve]] functor and its left adjoint $\Simp\Set \leftrightarrow \Simp\Cat$ where [[SimpCat]] denotes the category of [[simplicially enriched category|simplicially enriched categories]], i.e., categories enriched in $\Simp\Set$.

* The adjunction $- \times X: \SimpSet \leftrightarrow \SimpSet :(-)^X$ between the product with a simplicial set $X$ and the internal-hom, which makes $\Simp\Set$ into a [[cartesian closed category]].






### Model category structures

There are important [[model category]] structures on $sSet$.

* The standard [[model structure on simplicial sets]] [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoid]]s.

* The [[model structure for quasi-categories]] on $sSet$ presents the [[(∞,2)-category]] of [[(∞,1)-categories]] [[(∞,1)Cat]].

## Related concepts

* **sSet**, [[asSet]]


category: category

[[!redirects SSet]]
[[!redirects sSet]]
[[!redirects Simp Set]]

