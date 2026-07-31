
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



\tableofcontents


## Definition

### For topological spaces
 {#ForTopologicalSpace}

A [[topological space]] $X$ is **contractible** if the canonical map $X \to \ast$ is a [[homotopy equivalence]]. It is **weakly contractible** if this map is a [[weak homotopy equivalence]], hence if all [[homotopy groups]] of $X$ are trivial.

Where the [[Whitehead theorem]] does not apply, we may find examples of weakly contractible but not contractible spaces, such as the [double comb space](http://topospaces.subwiki.org/wiki/Double_comb_space) in [[Top]].

### For $\infty$-groupoids

Since the [[Whitehead theorem]] applies in [[∞Grpd]] (and generally in any [[hypercomplete (∞,1)-topos]]), being weakly equivalent to the point is the same as there being a contraction. So an [[∞-groupoid]] is **weakly contractible** if and only if it is **contractible**.

$$
  (C \;\text{is weakly contractible}) \Leftrightarrow
  (C \stackrel{\simeq}{\to} *)
  \,.
$$

In this context one tends to drop the "weakly" qualifier.

Sometimes one allows also the empty object $\emptyset$ to be contractible. To distinguish this, we say

* an $\infty$-groupoid is **(-1)-[[truncated]]** (is a [[(-1)-groupoid]]) if it is either empty or equivalent to the point;

* an $\infty$-groupoid is **(-2)-[[truncated]]** (is a [[(-2)-groupoid]]) if it is equivalent to the point.


### For cohesive $\infty$-groupoids
 {#ForCohesiveInfinityGroupoids}

An object $X$ of a [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]] may be contractible (or not) in different ways (*[[modality|modes]]*):

* The object $X$ itself may by contractible in that it is [[n-truncated object of an (infinity,1)-category|(-2)-truncated]]. This is an extremely strong notion: It says that $X$ is [[generalized the|the]] [[terminal object]]: [[generalized the|the]] [[point]], $X \simeq \ast$.

* The [[flat modality|underlying $\infty$-groupoid]] $\flat X$ may be contractible, $\flat X \simeq \ast$.

  This condition is slightly weaker than full contractibility. For instance an [[infinitesimally thickened point]] $\mathbb{D}$, regarded as a [[0-truncated object|0-truncated]]  [[haloed smooth infinity-groupoid|haloed smooth $\infty$-groupoid]], is generally not the actual point, but has $\flat \mathbb{D} \simeq \ast$.

* Its [[shape modality|shape]] $\esh X \in Grpd_\infty$ may be contractible, $\esh X \simeq \ast$.

  This is the *geometric* (or *cohesive*) notion of contractibility.

  For instance a [[Cartesian space]] ([[vector space]]) $\mathbb{R}^n$, regarded as a [[0-truncated object|0-truncated]] [[smooth infinity-groupoid|smooth $\infty$-groupoid]] has contractible shape, $\esh \mathbb{R}^n \simeq \ast$. 

  More generally, a [[topological space]] (or [[smooth manifold]]) $X$, has contractible shape when regarded as a [[0-truncated object|0-truncated]] [[Euclidean-topological infinity-groupoid|Euclidean-topological $\infty$-groupoid]] ([[smooth infinity-groupoid|smooth $\infty$-groupoid]]) precisely if it is a weakly contractible topological space in the traditional sense ([above](#ForTopologicalSpace)).

* Its [[sharp modality|codiscrete]] aspect $\sharp X$ may be contractible, $\sharp X \simeq \ast$.

  But (since $\flat \sharp \simeq \flat$ and $\sharp \circ \flat \simeq \sharp$,  and $\flat \ast \simeq \ast$) this is equivalent to $\flat X$ being contractible.



## Examples

* An [[inhabited set|inhabited]] [[convex set|convex]] (or even just [[star-convex set|star-convex]]) subset of a [[topological vector space]] over [[real numbers|$\mathbb{R}$]] or [[complex numbers|$\mathbb{C}$]] is contractible.

* The [[infinite-dimensional sphere|infinite-dimensional unit sphere]] in a [[separable Hilbert space|separable infinite-dimensional]] [[Hilbert space]] is contractible, unlike the case of [[n-sphere|finite-dimensional spheres]].

* By [[Kuiper's theorem]] the [[unitary group]] [[U(ℋ)]] of such a Hilbert space is contractible, where the [[topological space|topology]] can be either of the two main topologies ([[norm topology]], or [[strong operator topology]]).

* The total space of any [[universal principal bundle]] is contractible.


## Related concepts

* [[locally contractible space]]

* [[contractible chain complex]]

* [[contractible type]]

[[!include homotopy n-types - table]]


## References

See also:

* Ponaki Das, Sainkupar Marwein Mawiong: *On Weakly Contractible Non-Contractible Finite Topological Spaces of Ten Points* &lbrack;[arXiv:2605.06155](https://arxiv.org/abs/2605.06155)&rbrack;






[[!redirects contractible]]

[[!redirects contractible space]]
[[!redirects contractible spaces]]

[[!redirects weakly contractible space]]
[[!redirects weakly contractible spaces]]

[[!redirects contractible topological space]]
[[!redirects contractible topological spaces]]

[[!redirects weakly contractible topological space]]
[[!redirects weakly contractible topological spaces]]

[[!redirects contractible homotopy type]]
[[!redirects contractible homotopy types]]

[[!redirects weakly contractible homotopy type]]
[[!redirects weakly contractible homotopy types]]
