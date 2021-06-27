

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A **topological stack** is a [[geometric stack]] on the [[site]] [[Top]]: a [[topological groupoid]] regarded as presenting an object in the [[(2,1)-sheaf]] [[(2,1)-topos]] $Sh_{(2,1)}(Top)$.


## Definition

Let [[Top]] be the [[category]] of [[compactly generated space]]s and [[continuous function]]. When equipped with a [[Grothendieck topology]] given by usual [[open cover]]s this becomes a [[subcanonical coverage|subcanonical]] [[large site]]. 

Consider the [[(2,1)-topos]] [[(2,1)-sheaves]]=[[stack]]s

$$
  TopStack := Sh_{(2,1)}(Top)
$$

of [[groupoid]]s on $\mathrm{Top}$; by [[Yoneda embedding|Yoneda]] $\mathrm{Top}$ is a full [[sub-(∞,1)-category|sub-(2,1)-category]]

$$
  Top \hookrightarrow TopStack
  \,.
$$

By analogy with the case of [[algebraic stack]]s one says that a morphism of 1-stacks $f:X\to Y$ in $\mathrm{TopStack}$ is a **[[representable morphism of stacks]]** if for any morphism of 1-stacks $T\to Y$ from a (stack associated to a) topological space $T$ to $Y$ the pullback $T\times_Y X$ is (2-isomorphic to the stack associated to) a [[topological space]]. 

Let $P$ be a property of a map of topological spaces. $P$ is said to be __invariant under change of base__ if for all $f: Y \to X$ with property $P$, if $g:Z \to X$ is any continuous map, the induced map $Z \times_X Y \to Z$ also has property $P$. $P$ is said to be __invariant under restriction__ if this holds whenever $g$ is an embedding. A property $P$ which is invariant under restriction is said to be __local on the target__ if any $f: Y \to X$ for which there exists an open cover $\left(U_\alpha \to X\right)$ such that the induced map $\coprod_{\alpha}  {U_\alpha  }  \times_{X} Y \to \coprod_\alpha  {U_\alpha  } $ has property $P$, must also have property $P$.

Examples of such properties are being an [[open map]], [[covering]] map, [[closed map]], [[local homeomorphism]] etc.

A [[representable morphism of stacks|representable map]] $f:\X \to \Y$ of stacks is said to have property $P$ if for any map $T \to \Y$ from a topological space, the induced map $T \times_{\Y} \X \to T$ has property $P$



+-- {: .un_defn}
###### Definition

A 1-[[stack]] $X$ of [[groupoid]]s over $\mathrm{Top}$ having a representable epimorphism from a [[topological space]] $X_0 \to X$ is a __topological stack__. Such an representable epimorphism is called an [[atlas]] (or [[chart]]).

=--

This is what is called  __pretopological stack__  in [Noohi](#Noohi) . The terminology __topological stack__  is reserved for those stacks whose [[atlas]] can be chosen to belong to a class of "local fibrations"; there are axioms which the class of local fibrations have to satisfy; there are several natural choices of this class which modify the variant of topological stacks considered.

Any map from a topological space $S$ to a topological stack $X$ is representable (i.e. diagonal $X\to X\times X$ is always representable). For a topological stack $Y$, if $P$ is invariant under restriction and local on the target, a representable morphism $f : X \to Y$ of 1-stacks has this property if there exists an atlas $T\to Y$ such that the induced map $X\times_Y T\to T$ has property $P$. 

If $X_0 \to X$ is an atlas for a topological stack, then $X_0 \times_{X} X_0 \rightrightarrows X_0$ is a [[topological groupoid]], $\mathbf{X}$. The [[stackification]] of the presheaf of groupoids $T \mapsto Hom((T^{id},\mathbf{X}))$ is (2-iso to) $X$ (where $T^{id}$ is $T$ considered as a [[topological groupoid]] with only identity arrows).

Conversely, given a topological groupoid $G$, we can consider the stackification of $Hom(blank,G):= \left[ G\right]$. By direct inspection, one sees that $\left[ G\right](T)$ is the groupoid of principal G-bundles over $T$, $Bun_G(T)$. The canonical map $(G_0)^id \to G$ yields a map $a:G_0 \to \left[ G\right]$. If $p:T \to \left[ G\right]$ is any map from a space, then $T \times_{\left[ G\right]} G_0$ is the total space of the principal $G$-bundle over $T$ which $p$ corresponds to via Yoneda. If under the correspondence between [[principal bundle]]s and generalized homomorphims $p$ corresponds to a map $T^{id} \to G$, then $p$ factors through the map $a:G_0 \to \left[ G\right]$. If $p$ instead corresponds to a map $T_U \to G$ where $U \to T$ is a cover, then $p$ factors through $a$ locally, hence, $a$ is an epimorphism. Therefore an alternative definition of a topological stack is:

+-- {: .un_defn}
###### Definition

A 1-[[stack]] $X$ of [[groupoid]]s over $\mathrm{Top}$ is a __topological stack__ if it is [[equivalence in an (infinity,1)-category|equivalent]] to the stack  $G Bund$ of groupoid-[[principal bundle]] for some [[topological groupoid]] $G$.

=--

By the [[Yoneda lemma]], $Hom(T,Bun_G) \cong Bun_G(T)$ for all $T$. Moreover, if $H$ is another topological groupoid, $Hom(Bun_H,Bun_G) \cong Bun_G(H)$, where $Bun_G(H)$ is the groupoid of principal $G$-bundles over $H$. In fact, one can use this to show that the 2-category of topological stacks is equivalent to the [[bicategory]] of topological groupoids and principal bundles. One may also show that topological stacks are equivalent to the [[bicategory of fractions]] of topological groupoids with respect to formally inverting Morita-equivalences.

## Related concept

* [[geometric stack]]

  * [[algebraic stack]]

  * **topological stack**, [[topological groupoid]], [[topological infinity-groupoid]]

  * [[differentiable stack]], [[Lie groupoid]]

* [[geometric ∞-stack]]

* [[cohesive (∞,1)-topos|cohesive ∞-groupoid]]

  * [[discrete ∞-groupoid]]

  * [[Euclidean-topological ∞-groupoid]]

  * [[smooth ∞-groupoid]]

  * [[synthetic differential ∞-groupoid]]


## References

Basics


* {#Noohi}[[Behrang Noohi]], *Foundations of Topological Stacks I* ([arXiv:math.AG/0503247](http://arxiv.org/abs/math.AG/0503247))

* {#Carchedi11} [[David Carchedi]], _Categorical Properties of Topological and Diffentiable Stacks_, PhD thesis, Universiteit Utrecht, 2011 ([dspace:1874/208971](https://dspace.library.uu.nl/handle/1874/208971), [pdf](http://math.gmu.edu/~dcarched/Thesis_David_Carchedi.pdf). [[CarchediDifferentiableStacks.pdf:file]])

* [[David Carchedi]], _Compactly Generated Stacks: A Cartesian Closed Theory of Topological Stacks_, Advances in Mathematics, Vol.229(6) (2012) 3339-3397, doi:[10.1016/j.aim.2012.02.006](http://dx.doi.org/10.1016/j.aim.2012.02.006), ([arXiv:0907.3925](http://arxiv.org/abs/0907.3925))

* Metzler, _Topological and smooth stacks_ ([arXiv:math/0306176](http://arxiv.org/abs/math/0306176))

On [[geometric realization of topological stacks]]:

* {#Noohi}[[Behrang Noohi]], *Homotopy types of topological stacks*, Advances in Mathematics Volume 230, Issues 4–6, July–August 2012, Pages 2014-2047 ([arXiv:0808.3799](https://arxiv.org/abs/0808.3799))

* [[Johannes Ebert]], *The homotopy type of a topological stack* ([arXiv:0901.3295](https://arxiv.org/abs/0901.3295))


On [[mapping stacks]] of [[topological stacks]]:

* {#Noohi08} [[Behrang Noohi]], _Mapping stacks of topological stacks_ ([arXiv:0809.2373](http://arxiv.org/abs/0809.2373))
 
and in the special case of [[free loop stacks]]:

* [[Kai Behrend]], [[Gregory Ginot]], [[Behrang Noohi]], [[Ping Xu]], _String topology for stacks_ ([arXiv:0712.3857](http://front.math.ucdavis.edu/0712.3857))


[[!redirects topological stack]]
[[!redirects topological stacks]]
