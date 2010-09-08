
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Lie integration is a process in that assigns to a [[Lie algebra]] $\mathfrak{g}$ -- or more generally an [[L-∞-algebra|∞-Lie algebra]] or [[∞-Lie algebroid]] -- a [[Lie group]] -- or more generally [[∞-Lie groupoid]] -- that is [[infinitesimal space|infinitesimally]] modeled by $\mathfrak{g}$.

If the [[∞-Lie algebroid]]s $\mathfrak{a}$ involved are incarnated dually in the form of their [[Chevalley-Eilenberg algebra]]s $CE(\mathfrak{a})$ then the bare [[∞-groupoid]] integrating them (i.e. ignoring the smooth structure) is effectively given by the [[Sullivan construction]] applied to the [[dg-algebra]] $CE(\mathfrak{a})$.


## Definition

Let $\mathfrak{a}$ be an [[∞-Lie algebroid]] (for instance a [[Lie algebra]], or a [[Lie algebroid]] or an [[L-∞-algebra]]). 

For $n \in \mathbb{N}$ write $\Delta^n$ for the $n$-[[simplex]] regarded as a [[smooth manifold]] (with boundary and corners).  

For $d \in \mathbb{N}$, a **$d$-path** in the $\infty$-Lie algebroid is a morphism of $\infty$-Lie algebroids

$$
  \Sigma : T \Delta^d_{Diff} \to \mathfrak{a}
$$ 

from the [[tangent Lie algebroid]] $T \Delta^d_{Diff}$ of the standard smooth $d$-simplex to $\mathfrak{a}$.


Dually this a morphism of [[dg-algebra]]

$$
  \Omega^\bullet(\Delta^n) \leftarrow CE(\mathfrak{a}) : \Sigma^*
$$

from the [[Chevalley-Eilenberg algebra]] of $\mathfrak{a}$ to the [[de Rham complex]].



### Integration to a bare $\infty$-groupoid {#IntToBareGrpd}

Here we discuss the bare [[∞-groupoid]]s underlying the [[∞-Lie groupoid]]s to which an [[∞-Lie algebroid]] integrates.

For $\mathfrak{a}$ an $\infty$-Lie algebroid, the $d$-paths in $\mathfrak{a}$ naturally form a [[simplicial set]] 

$$
  \exp(\mathfrak{a})_{bare}
  :=
  \left(
   \cdots    
   Hom(T \Delta^2, \mathfrak{a})
   \stackrel{\t}{\stackrel{\to}{\to}}
   Hom(T \Delta^1, \mathfrak{a})
   \stackrel{\to}{\to}
   Hom(T \Delta^0, \mathfrak{g})
  \right)
$$

which is a [[Kan complex]] under mild technical fine-tuning of the definition of $d$-paths.

Since morphisms of [[∞-Lie algebroid]]s are dually equivalent to [[dg-algebra]] morphisms of their [[Chevalley-Eilenberg algebra]], the above is equivalent to

$$
   \exp(\mathfrak{a})_{bare}
   :=
   (
   \cdots 
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^2))
   \stackrel{\to}{\stackrel{\to}{\to}}
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^1))
   \stackrel{\to}{\to}
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^0))
   )
  \,.
$$

This is nothing but the [[Sullivan construction]] in [[rational homotopy theory]] applied to the dg-algebra $CE(\mathfrak{a})$.

This gives the universal $\infty$-groupoid integrating $\mathfrak{a}$. If $\mathfrak{a}$ is $n$-[[truncated]] then this construction will not yield in general an $n$-truncated [[∞-groupoid]] $\exp(\mathfrak{a})$. Instead one wants to truncate it to its $(n+1)$-[[coskeleton]]

$$
  \mathbf{cosk}_{n+1}\exp(\mathfrak{a})_{bare}  
  \,.
$$


### Integration to an $\infty$-Lie groupoid

We now discuss Lie integration of $\infty$-Lie algebroids to [[∞-Lie groupoid]]s.

For discussing smooth families of $d$-paths we need the following technical notion.

+-- {: .un_defn}
###### Definition

We say a [[differential form]] $\omega$ on the $n$-simplex $\Delta^n$ has **sitting instants** if for all $k \in \mathbb{N}$ we have that each $k$-face $\delta_k^i(\Delta^n)$ of $\Delta^n$ has an open neighbourhood $U_{\delta_k^i(\Delta^n)} \subset \Delta^n$ such that $\omega$ restricted to that neighbourhood is constant in the direction perpendicular to the boundary.

$$
  \mathcal{L}_{v^\perp} \omega|_{U_{\delta_k^i(\Delta^n)}} = 0
  \,.
$$

Define $\Omega^\bullet_{si}(\Delta^n) \subset \Omega^\bullet(\Delta^n)$ to be the sub-[[dg-algebra]] of the [[de Rham complex]] on those forms that have sitting instants. 

=--

We may at times, here or in other entries, abuse notation and just write $\Omega^\bullet(\Delta^n)$ instead, when the context of Lie integration is clear.

+-- {: .un_defn}
###### Definition

For a [[smooth manifold]] $U$ and $C^\infty(U)$ its $\mathbb{R}$-algebra of [[smooth function]]s, we write $C^\infty(U)\otimes \Omega^\bullet_{si}(\Delta^n)$ for the ordinary algebraic [[tensor product]] over $\mathbb{R}$. This becomes a [[dg-algebra]] by regarding $C^\infty(U)$ as a dg-algebra concentrated in degree 0.

=--

For the following definition, we use from the discussion at [[∞-Lie groupoid]] that $\infty$-Lie groupoids may be modeled by [[simplicial presheaves]] on the [[site]] [[CartSp]] $\subset$ [[Diff]].

+-- {: .un_defn}
###### Definition

For $\mathfrak{a}$ an [[∞-Lie algebroid]] define the [[simplicial presheaf]] $\exp(\mathfrak{a})$ by

$$  
  \exp(\mathfrak{a})
  : 
  (U,[n]) \mapsto 
  Hom_{dgAlg}(CE(\mathfrak{a}), C^\infty(U)\otimes \Omega^\bullet(\Delta^n))
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

Compared to the integration to bare $\infty$-groupoids [above](#IntToBareGrpd) this definition knows about $U$-parameterized _smooth families_ of $n$-paths in $\mathfrak{a}$.

The bare $\infty$-groupoid is recoverd as that of the $\mathbb{R}^0 = *$-parameterized family:

$$
  \exp(\mathfrak{a}) : \mathbb{R}^0 \mapsto \exp(\mathfrak{a})_{bare}
  \,.
$$

=--

+-- {: .un_defn}
###### Definition

Write $\mathbf{cosk}_{n+1} \exp(a)$ for the simplicial preshaf obtained by postcomposting $\exp(\mathfrak{a}) : CartSp^{op} \to sSet$ with the $(n+1)$-[[coskeleton]] functor $\mathbf{cosk}_{n+1} : sSet \stackrel{tr_n}{\to} sSet_{\leq n+1} \stackrel{cosk_{n+1}}{\to} sSet$.

=--



## Examples

For more on this see (for the moment) <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegrated">Lie integrated ∞-Lie groupoids</a>.


### Integration of Lie algebras

In 

* [[Marius Crainic]], [[Rui Fernandes]], _Integrability of Lie brackets_ ([arXiv](http://arxiv.org/abs/math/0105033))

it is effectively shown that for $\mathfrak{g}$ a (finite-dimensional) [[Lie algebra]] we have

$$
  \tau_1 \exp(\mathfrak{g}) = \mathbf{B}G
$$

is the [[delooping]] one-object groupoid of the simply connected [[Lie group]] $G$ corresponding to $G$ under [[Lie's three theorems]].



### Integration of Lie 2-algebras

If $\mathfrak{g}_\mu$ is the [[string Lie 2-algebra]] it is effectively shown in 

* Andr&eacute; Henriques, _Integrating $L_\infty$ algebras_,([arXiv](http://arxiv.org/abs/math.AT/0603563))

that 

$$
  \tau_2 \exp(\mathfrak{g}_\mu) \simeq \mathbf{B}String(G)
$$

is the [[string 2-group]]. 

### Higher line $n$-groupoids

(...)

$$
  \exp(b^{k-1} \mathbb{R})_{bare}
  : 
  [n] \mapsto \Omega^k_{closed}(\Delta^n)
$$

(...)


$$
  \int_{\Delta^\bullet} : \exp(b^{k-1}\mathbb{R})
  \stackrel{\simeq}{\to}
  \mathbf{B}^k \mathbb{R}
   \,.
$$

(...)


## References

The basic idea of identifying the [[Sullivan construction]] applied to [[Chevalley-Eilenberg algebra]]s as Lie integration to bare $\infty$-groupoids appears in

* [[Vladimir Hinich]], _Descent of Deligne groupoids_, Internat. Math. Res. Notices, 5:223&#8211;239, 1997 ([doi](http://dx.doi.org/10.1155/S1073792897000160), [preprint ddg.pdf](http://math.haifa.ac.il/hinich/WEB/mypapers/ddg.pdf))

and for general [[∞-Lie algebra]]s in

* [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$ algebras_, ([math.AT/0404003](http://arxiv.org/abs/math/0404003))

(whose main point is the discussion of a gauge condition applicable for nilpotent $L_\infty$-algebras that cuts down the result of the Sullivan construction to a much smaller but equivalent model) .

This was refined from integration to bare $\infty$-groupoids to an integration to [[internal ∞-groupoid]]s in [[Banach manifold]]s in

* [[André Henriques]], _Integrating $L_\infty$ algebras_, Compos. Math. __144__  (2008), no. 4, 1017--1045 ([doi](http://dx.doi.org/10.1112/S0010437X07003405),[math.AT/0603563](http://arxiv.org/abs/math.AT/0603563))

(whose origin possibly preceeds that of Getzler's article).

For general [[∞-Lie algebroid]]s the general idea of the integration process by "$d$-paths" had been indicated in 

* [[Pavol ?evera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv:math.SG/0105080](http://arxiv.org/abs/math.SG/0105080)).

A detailed review of how the traditional Lie integration of [[Lie algebra]]s and [[Lie algebroid]]s to [[Lie group]]s and [[Lie groupoid]]s (including the smooth structure) is reproduced in terms of $d$-pathis is given in

* [[Marius Crainic]], [[Rui Fernandes]], _Integrability of Lie brackets_ ([arXiv:math.DG/0105033](http://arxiv.org/abs/math/0105033))

