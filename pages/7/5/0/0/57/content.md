
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

Lie integration assigns to a [[Lie algebra]] $\mathfrak{g}$ -- or more generally an [[L-∞-algebra|∞-Lie algebra]] or [[∞-Lie algebroid]] -- a [[Lie group]] -- or more generally [[∞-Lie groupoid]] -- that is [[infinitesimal space|infinitesimally]] modeled by $\mathfrak{g}$.

If the [[∞-Lie algebroid]]s $\mathfrak{a}$ involved are incarnated dually in the form of their [[Chevalley-Eilenberg algebra]]s $CE(\mathfrak{a})$ then the bare [[∞-groupoid]] (that is: without the smooth structure) integrating them is effectively given by the [[Sullivan construction]] from [[rational homotopy theory]] which turns a [[dg-algebra]] into a [[simplicial set]] (and then into a [[topological space]] by [[geometric realization]]) applied here to the [[dg-algebra]] $CE(\mathfrak{a})$.

This construction applied to an ordinary [[Lie algebra]] reproduces the _integration method by paths_ in standard [[Lie theory]] (maybe less widely known than other integration methods). See our first example [below](#LieAlgebrasToLieGroups).

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

This is (up to fine-tuning of the nature of the differential forms on the simplices) the [[Sullivan construction]] of [[rational homotopy theory]] that tuns a dg-algvebra into a simplicial set, applied to the dg-algebra $CE(\mathfrak{a})$.


+-- {: .un_remarl}
###### Remark
**(spurious homotopy groups)**

For $\mathfrak{a}$ a [[infinity-Lie algebroid|Lie n-algebroid]] (an $n$-[[truncated]] $\infty$-Lie algebroid) this construction will not yield in general an $n$-[[truncated]] [[∞-groupoid]] $\exp(\mathfrak{a})$. 

To see this, consder the example (discussed in detail [below](#LieAlgebrasToLieGroups)) that $\mathfrak{a} = \mathfrak{g}$ is an ordinary [[Lie algebra]]. Then $\exp(\mathfrak{g})_n$ is canonically identified with the set of smooth based maps $\Delta^n \to G$ into the simply connected [[Lie group]] that integrates $\mathfrak{g}$ in ordinary [[Lie theory]]. This means that the simplicial [[homotopy group]]s of $\exp(\mathfrak{g})$ are the topological homotopy groups of $G$, which in general (say for $G$ the [[orthogonal group]] or [[unitary group]]) will be non-trivial in arbitrarily higher degree, even though $\mathfrak{g}$ is just a Lie 1-algebra. This phenomenon is well familiar from [[rational homotopy theory]], where a classical theorem asserts that the rational homotopy groups of $\exp(\mathfrak{g})$ are generated from the generators in a [[minimal Sullivan model]] resolution of $\mathfrak{g}$. 

=--

For the purposes of $\infty$-Lie theory therefore instead one wants to [[truncated|truncate]] $\exp(\mathfrak{g})$ to its $(n+1)$-[[coskeleton]]

$$
  \mathbf{cosk}_{n+1}\exp(\mathfrak{a})_{bare}  
  \,.
$$


This divides out [[k-morphism|n-morphisms]] by $(n+1)$-morphisms and forgets all higher higher nontrivial morphisms, hence all higher homotopy groups.


### Integration to an $\infty$-Lie groupoid {#SmoothIntegration}

We now discuss Lie integration of $\infty$-Lie algebroids to [[∞-Lie groupoid]]s.

For discussing smooth families of $d$-paths we need the following technical notion.

+-- {: .un_defn}
###### Definition

We say a [[differential form]] $\omega$ on the $n$-simplex $\Delta^n$ has **sitting instants** if it satisfies the following recursive condition:

For $n = 0$, every differential form has sitting instants. For $n \geq 1$, $\omega$ has sitting instants if 

1. for every $(n-1)$-face $\partial_i \Delta^{n-1} \hookrightarrow \Delta^n$ of $\Delta^n$ there is a neighbourhood of that face in $\Delta^n$ such that $\omega$ restricted to that neighbourhood is constant in the direction perpendicular to the boundary on its value at that boundary;

   (so near a $(k \lt p)$-dimensional face a $p$-form with sitting instants needs to vanish, but near a $(k \geq p)$-dimensional face it just needs to become perpendicularly constant).

1. the restriction $\partial_i^* \omega$ has sitting instants on $\Delta^{n-1}$.

Define $\Omega^\bullet_{si}(\Delta^n) \subset \Omega^\bullet(\Delta^n)$ to be the sub-[[dg-algebra]] of the [[de Rham complex]] on those forms that have sitting instants. Similarly, for $U \in Diff$, let $\Omega^\bullet_{si}(U \times \Delta^n)$ be the subcomplex of forms on $U \times \Delta^n$ that have sitting instant with respect to $\Delta^n$.

Finally, we write $\Omega^\bullet(U \times \Delta^n)_{vert}$ for the dg-algebra of forms with sitting instants that are also [[vertical differential form]]s with respect to the projection $U \times \Delta^n \to U$.

=--

+-- {: .un_remark}
###### Remark

The condition of sitting instants serves to make smooth differential forms not be affected by the boundaties and corners of $\Delta^n$. Notably for $\omega_j \in \Omega^\bullet_{si}(\Delta^{n-1})$ a collection of forms with sitting instants on the $(n-1)$-cells of a horn $\Lambda^n_i$ that coincide on adjacent boundaries, and for

$$
  p : \Delta^n \to \Lambda^{n-1}_i
$$

a standard piecewise smooth [[retract]]s, the pullbacks

$$
  p^* \omega_i 
$$

glue to a single smooth form (with sitting instants) on $\Delta^n$.

=--

+-- {: .un_remark}
###### Remark

Notice that $\omega \in \Omega^\bullet(\Delta^n)$ having sitting instants does not imply that there is a neighbourhood of the boundary of $\Delta^n$ on which $\omega$ is entirely constant. It is important for the following constructions that in the vicinity of the boundary $\omgea$ is allowed to vary parallel to the boundary, just not perpendicular to it.

=--

We may at times, here or in other entries, abuse notation and omit the subscript ${}_{si}$ when the context of Lie integration is understood.



For the following definition, we use from the discussion at [[∞-Lie groupoid]] that $\infty$-Lie groupoids may be modeled by [[simplicial presheaves]] on the [[site]] [[CartSp]] $\subset$ [[Diff]].

+-- {: .un_defn}
###### Definition

For $\mathfrak{a}$ an [[∞-Lie algebroid]] define the [[simplicial presheaf]] $\exp(\mathfrak{a}) : CartSp^{op} \to sSet$ by

$$  
  \exp(\mathfrak{a})
  : 
  (U,[n]) \mapsto 
  Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(U \times \Delta^n)_{vert})
  \,,
$$

where $U \in $ [[CartSp]] and $[n] \in \Delta$. 

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

Write $\mathbf{cosk}_{n+1} \exp(a)$ for the simplicial preshaf obtained by postcomposting $\exp(\mathfrak{a}) : CartSp^{op} \to sSet$ with the $(n+1)$-[[coskeleton]] [[functor]] $\mathbf{cosk}_{n+1} : sSet \stackrel{tr_n}{\to} sSet_{\leq n+1} \stackrel{cosk_{n+1}}{\to} sSet$.

=--



## Examples

For more on this see (for the moment) <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegrated">Lie integrated ∞-Lie groupoids</a>.


### Interating Lie algebras to Lie groups {#LieAlgebrasToLieGroups}

Let $\mathfrak{g}$ be an ordinary (finite dimensonal) [[Lie algebra]].

Standard [[Lie theory]] (see [[Lie's three theorems]]) provides a [[simply connected]] [[Lie group]] $G$ integrating $\mathfrak{g}$.

If we take that standard procedure for granted, then it is easy to see that:


+-- {: .un_prop}
###### Proposition

There is a weak equivalence (in $[CartSp^{op}, sSet]_{proj}$)

$$
  \mathbf{cosk}_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G
  \,,
$$

where on the right we have the [[delooping]] [[Lie groupoid]] of $G$.

=--


This follows from the following observation.

+-- {: .un_lemma}
###### Lemma

For $X$ a [[simply connected]] [[smooth manifold]] and $x_0 \in X$ a basepoint, there is a canonical [[bijection]]

$$
  \Omega^1_{flat}(X,\mathfrak{g}) \simeq C^\infty_*(X,G)
$$

between the set of [[Lie-algebra valued 1-form]]s on $X$ whose [[curvature]] 2-form vanishes, and the set of [[smooth function]]s $X\to G$ that take $x_0$ to the neutral element $e \in G$.

=--

+-- {: .proof}
###### Proof

The bijection is given as follows. For $A \in \Omega^1_{flat}(X,\mathfrak{g})$ a flat 1-form, the corresponding function $f_A : X \to G$ sends $x \in X$ to the [[parallel transport]] along any path $x_0 \to x$ from the base point to $x$

$$
  f_A : x \mapsto tra_A(x_0 \to x)
  \,.
$$

Because of the assumption that the [[curvature]] 2-form of $A$ vanishes and the assumption that $X$ is [[simply connected]], this assignment is independent of the choice of path.

Conversely, for every such function $f : X \to G$ we recover $A$ as the pullback of the [[Maurer-Cartan form]] on $G$

$$
  A = f^* \theta
  \,.
$$

=--

From this we obtain

+-- {: .proof}
###### Proof of the proposition

The $\infty$-groupoid $\mathbf{cosk}_2 \exp(\mathfrak{g})$ is equivalent to the [[groupoid]] with a single object (no non-trivial 1-form on the point) whose morphisms are equivalence classes of smooth based paths $\Delta^1 \to G$ (with sitting instants), where two of these are taken to be equivalent if there is a smooth [[homotopy]] $D^2 \to G$ (with sitting instant) between them.

Since $G$ is [[simply connected]], these equivalence classes are labeled by the endpoints of these paths, hence are canonically identified with $G$.

=--

We don't need to fall back to classical Lie theory to obtain $G$ in the above argument. A detailed discussion of how to find $G$ with its group structure and smooth structure from $d$-paths in $\mathfrak{g}$ is in ([Crainic](#Crainic)).





### Integrating to line/circle Lie $n$-groups


+-- {: .un_def}
###### Definition

Write $b^n \mathbb{R}$ for the [[L-∞-algebra]] whose [[Chevalley-Eilenberg algebra]] is given by a single generator in degree $(n+1)$ and vanishing differential.

Write $e b^n \mathbb{R}$ for the dg-algebra on one generator in degree $(n+1)$ and one in degree $(n+2)$ and the differential taking the former to the latter.

=--

+-- {: .un_lemma}
###### Observation

$$
  \exp(b^{k-1} \mathbb{R})_{bare}
  : 
  [n] \mapsto \Omega^k_{closed}(\Delta^n)
$$

is the simplicial set that in degree $n$ is the set of closed $k$-forms on the $n$-simplex.

=--


+-- {: .un_lemma}
###### Lemma

For each $n \in \mathbb{N}$ the diagram

$$
  \array{
    \exp(b^n \mathbb{R}) &\to& *
    \\
    \downarrow && \downarrow
    \\
    \exp(e b^n \mathbb{R}) &\to& \exp(b^{n+1}\mathbb{R})
  }
$$

is a pullback diagram in $sPSh(CartSp)$. Moreover, there is a morphism of diagrams

$$
  \array{
    \exp(b^{n} \mathbb{R})
    &\to&
    \exp(e b^{n} \mathbb{R})
    &\to& 
    \exp(b^{n+1} \mathbb{R})
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{B}^n \mathbb{R} &\to& \mathbf{E}\mathbf{B}^n \mathbb{R}
    &\to&
    \mathbf{B}^{n+1} \mathbb{R}
  }
$$

where the vertical morphisms are acyclic fibrations, induced by sending differential $n$-forms on the $n$-simplex to their [[integration]] over that $n$-simplex. 

=--

+-- {: .proof}
###### Proof

The key fact underlying this is that a closed smooth $n$-form on the $n$-sphere may be extended smoothly to a closed $n$-form on the $(n+1)$-ball precisely if its integral over the sphere vanishes. 

From this it follows that also every closed $n$-form on the $k$-sphere for $k \gt n$ may be extended as a closed $n$-form to the $(n+1)$-ball. The same holds for smooth families of forms. This implies that $\exp(b^n \mathbb{R}) \to \mathbf{B}^n \mathbb{R}$ is an acyclic fibration for all $n$.

=--


### Integrating the string Lie 2-algebra to the string Lie 2-group

Let $\mathfrak{string} = mathfrak{g}_\mu$ be the [[string Lie 2-algebra]].

Then $\mathbf{cosk}_3 \exp(\mathfrak{g}_\mu)$ is equvalent to the [[2-groupoid]] $\mathbf{B}String$ 

* with a single object;

* whose morphisms are based paths in $G$;

* whose 2-morphisms are equivalence class of pairs $(\Sigma,c)$, where 

  * $\Sigma : D^2_*  \to D$ is a smooth based map (where we use a [[homeomorphism]] $D^2 \simeq \Delta^2$ which away from the corners is smooth, so that forms with sitting instants there do not see any non-smoothness, and the basepoint of $D^2_*$ is the 0-vertex of $\Delta^2$) 

  * and $c \in U(1)$, and where two such are equivalent if the maps coincides at their boundary and if for any 3-ball $\phi : D^3 \to G$ filling them the labels $c_1, c_2 \in U(1)$ differ by the integral $\int_{D^3} \phi^* \mu(\theta) \;\; mod \;\; \mathbb{Z}$,,

where $\theta$ is the [[Maurer-Cartan form]], $\mu(\theta) = \langle \theta\wedge [\theta \wedge \theta]\rangle $ the 3-form obtained by plugging it into the cocycle.

This is the [[string Lie 2-group]]. It's construction in terms of integration by paths is due to ([Henriques](#Henriques))





## References

The basic idea of identifying the [[Sullivan construction]] applied to [[Chevalley-Eilenberg algebra]]s as Lie integration to bare $\infty$-groupoids appears in

* [[Vladimir Hinich]], _Descent of Deligne groupoids_, Internat. Math. Res. Notices, 5:223&#8211;239, 1997 ([doi](http://dx.doi.org/10.1155/S1073792897000160), [preprint ddg.pdf](http://math.haifa.ac.il/hinich/WEB/mypapers/ddg.pdf))

and for general [[∞-Lie algebra]]s in

* [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$ algebras_, ([math.AT/0404003](http://arxiv.org/abs/math/0404003))

(whose main point is the discussion of a gauge condition applicable for nilpotent $L_\infty$-algebras that cuts down the result of the Sullivan construction to a much smaller but equivalent model) .

This was refined from integration to bare $\infty$-groupoids to an integration to [[internal ∞-groupoid]]s in [[Banach manifold]]s in

* [[André Henriques]], _Integrating $L_\infty$ algebras_, Compos. Math. __144__  (2008), no. 4, 1017--1045 ([doi](http://dx.doi.org/10.1112/S0010437X07003405),[math.AT/0603563](http://arxiv.org/abs/math.AT/0603563))
{#Henriques}

(whose origin possibly preceeds that of Getzler's article).

For general [[∞-Lie algebroid]]s the general idea of the integration process by "$d$-paths" had been indicated in 

* [[Pavol ?evera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv:math.SG/0105080](http://arxiv.org/abs/math.SG/0105080)).

A detailed review of how the traditional Lie integration of [[Lie algebra]]s and [[Lie algebroid]]s to [[Lie group]]s and [[Lie groupoid]]s (including the smooth structure) is reproduced in terms of $d$-pathis is given in

* [[Marius Crainic]], [[Rui Fernandes]], _Integrability of Lie brackets_ ([arXiv:math.DG/0105033](http://arxiv.org/abs/math/0105033))
{#Crainic}
