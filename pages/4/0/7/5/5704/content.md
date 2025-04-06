
> This entry is about the concept in [[topology]]. For _[[quotient vector spaces]]_ in [[linear algebras]] see there.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

# Quotient spaces
* table of contents
{: toc}

## Idea

A *quotient space* is a [[quotient object]] in some [[category]] of [[spaces]], such as [[Top]] (of [[topological spaces]]), or [[Loc]] (of [[locales]]), etc.

Often the construction is used for the quotient $X/A$ by a subspace $A \subset X$ (example \ref{QuotientBySubspace} below).

Beware that [[quotient objects]] in the [[category]] [[Vect]] of [[vector spaces]] also traditionally called 'quotient space', but they are really just a special case of [[quotient modules]], very different from the other kinds of quotient space.  However in _[[topological vector spaces]]_ both concepts come together.

## Definitions

### In $Top$

+-- {: .num_defn #QuotientTopologicalSpace}
###### Definition
**(quotient topological space)**

Let $(X,\tau_X)$ be a [[topological space]]  and let

$$
  R_\sim \subset X \times X
$$

be an [[equivalence relation]] on its underlying set. Then the _quotient topological space_  has

* as underlying set the [[quotient set]] $X/\sim$, hence the set of [[equivalence classes]],

and

* a subset $O \subset X/\sim$ is declared to be an [[open subset]] precisely if its [[preimage]] $\pi^{-1}(O)$ under the canonical [[projection map]]

  $$
    \pi \;\colon\; X \to X/\sim
  $$

  is open in $X$.

To see that this indeed does define a topology on $X/\sim$ it is sufficient to observe that taking pre-images commutes with taking unions and with taking intersections.


Often one considers this with input datum not the equivalence relation, but any [[surjection]]

$$
  \pi \;\colon\; X \longrightarrow Y
$$

of sets. Of course this identifies $Y = X/\sim$ with $(x_1 \sim x_2) \Leftrightarrow (\pi(x_1) = \pi(x_2)) $.
Hence the _quotient topology_ on the codomain set of a function out of any topological space has as open subsets
those whose pre-images are open.

Equivalently this is the _[[final topology]]_ or _[[strong topology]]_ induced on $Y$ by the function $X \to Y$, see at _[Top -- Universal constructions](Top#UniversalConstructions)_.

=--

For this construction the function $X \to Y$ need not even be surjective, and we could generalize to a [[sink]] instead of a single map; in such a case one generally says *[[final topology]]* or *[[strong topology]]*.  See also at _[[topological concrete category]]_. 




### In $Loc$

A quotient space in $Loc$ is given by a [[regular subobject]] in [[Frm]].

(More details needed.)

## Examples

+-- {: .num_example #CircleAsQuotientOfClosedIntervalIdentifyingEndpoints}
###### Example

The [[trigonometric function]]

$$
  (cos(-),sin(-))
    \;\colon\; 
  [0,2\pi]
    \longrightarrow
  S^1
   \subset 
  \mathbb{R}^2
$$

from the [[closed interval]] with its [[Euclidean space|Euclidean]] [[metric topology]] to the unit [[circle]] equipped with the [[subspace topology]] of the [[Euclidean space|Euclidean]] [[plane]] 

descends to a [[homeomorphism]] on the quotient space $[0,2 \pi]/(0 \sim 2 \pi)$ by the equivalence relation which identifies the two endpoints of the open interval.

$$
  \array{
    [0,2\pi] &\overset{(cos(-),sin(-))}{\longrightarrow}& S^1
    \\
    \downarrow & \nearrow_{\mathrlap{\simeq}}
    \\
    [0,2\pi]/\simeq
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the [[universal property]] of the quotient it follows that $[0,2\pi]/(0 \sim 2\pi) \to S^1$ is a [[continuous function]]. Moreover, it is a [[bijection]] on the underlying sets by the $2\pi$-periodicity of sine and coside. Hence it is sufficient to see that it is an [[open map]] (by [this prop.](homeomorphism#HomeoContinuousOpenBijection)).

Since the open subsets of $[0,2\pi]$ are unions of 

1. the [[open intervals]] $(a,b)$ with $0 \lt a \lt b \lt 2\pi$,

1. the [[half-open intervals]]  $[0,b)$ and $(a,2\pi]$ with $0 \lt a,b  \lt 2\pi$ 

and since the projection map $\pi \colon [0,2\pi] \to [0,2\pi]/(0 \sim 2\pi)$ is injective on $(0, 2\pi)$, the open subsets of $[0,2\pi]/(0 \sim 2\pi)$ are unions of

1. the [[open intervals]] $(a,b)$ with $0 \lt a \lt b \lt 2\pi$,

1. the glued [[half-open intervals]]  $(b,2\pi]/(0\sim 2\pi) \cup [0,a)/(0 \sim 2\pi)$ for $0 \lt a,b \lt 2\pi$.

By the $2\pi$-periodicity of $(cos(-),sin(-))$, the image of the latter under $(cos(-),sin(-))$ is the same as the image of $(b, 2\pi + a)$. Since the function $(cos(-),sin(-)) \colon \mathbb{R} \to S^1$ is clearly an open map, it follows that the images of these open subsets in $S^1$ are open.



=--


+-- {: .num_example #QuotientBySubspace}
###### Example
**(quotient by a subspace)**

Let $X$ be a [[topological space]] and $A \subset X$ a [[inhabited set|non-empty]] [[subset]].
Consider the [[equivalence relation]] on $X$ which identifies all points in $A$ with each other. The resulting quotient space (def. \ref{QuotientTopologicalSpace}) is often simply denoted $X/A$.

Notice that $X/A$ is canonically a [[pointed topological space]], with base point the [[equivalence class]] $A/A \subset X/A$ of $A$.

If $A = \emptyset$ is the [[empty space]], then one defines 

$$
  X/\emptyset \coloneqq X_+ \coloneqq X \sqcup \ast
$$ 

to be the [[disjoint union space]] of $X$ with the [[point space]]. This is no longer a quotient space, but both constructions are unified by the _[[pushout]]_ $i \colon A \to X$ along the map $A \to \ast$, equivalently the [[cokernel]] of the inclusion:

$$
  \array{
    A &\overset{i}{\hookrightarrow}& X
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& X/A
  }
  \,.
$$

This kind of quotient space plays a central role in the discussion of [[long exact sequences in cohomology]], see at _[[generalized (Eilenberg-Steenrod) cohomology]]_.

=--

+-- {: .num_example #QuotientOfRealNumbersByTranslationByRationalNumbers}
###### Example

Consider the [[real numbers]] $\mathbb{R}$ equipped with their [[Euclidean space|Euclidean]] [[metric topology]]. Consider on $\mathbb{R}$ the [[equivalence relation]] which identifies all real numbers that differ by a [[rational number]]:

$$
  (x_1 \sim_{\mathbb{Q}} x_2)
    \Leftrightarrow
  \left(
     x_2 - x_1 \in \mathbb{Q} \subset \mathbb{Q}
  \right)
  \,.
$$

Then the quotient space $\mathbb{R}/\sim_{\mathbb{Q}}$ is a [[codiscrete topological space]].

=--

+-- {: .proof}
###### Proof


We need to check that the only open subsets of $X/\sim_{\mathbb{Q}}$ are the empty set and the entire set $X/\sim_{\mathbb{Q}}$. 

So let $U \subset \mathbb{R}/\sim$ be a non-empty subset. 

Write $\pi \colon \mathbb{R} \to \mathbb{R}/\sim_{\mathbb{Q}}$ for the quotient projection. By definition $U$ is open precisely if its pre-image $\pi^{-1}(U) \subset \mathbb{R}$ is open. By the Euclidean topology, this is the case precissely if $\pi^{-1}(U)$ is a union of [[open intervals]]. Since by assumption $\pi^{-1}(U)$ is non-empty, it contains at least one open interval $(a,b) \subset \mathbb{R}$, with $a \lt b$. By the density of the rational numbers, there exists a rational number $q \in \mathbb{Q} \subset \mathbb{R}$ with

$$
  0 \lt q \lt b - a
  \,.
$$

By definition of $\sim_{\mathbb{Q}}$ we have for all $n \in \mathbb{Z}$ that all elements in $(a + n q, b + n q) \subset \mathbb{R}$ are $\sim_{\mathbb{Q}}$-equivalent to elements in $(a,b)$, hence that also $(a+q,b+q) \subset \pi^{-1}(U)$. But the union of these open intervals is all of $\mathbb{R}$

$$
  \underset{n \in \mathbb{Z}}{\cup} (q + n q, b + n q)
  \;=\;
  \mathbb{R}
$$

and so $\pi^{-1}(U) = \mathbb{R}$.

=--




## Properties

1. Recall that a map $q \colon X \to Y$ is [[open map|open]] if $q(U)$ is open in $Y$ whenever $U$ is open in $X$. It is not the case that a quotient map $q \colon X \to Y$ is necessarily open. Indeed, the identification map $q \colon I \sqcup \{\ast\} \to S^1$, where the endpoints of $I$ are identified with $\ast$, takes the open point $\ast$ of the domain to a non-open point in $S^1$. 

1. Nor is it the case that a quotient map is necessarily a closed map; the classic example is the projection map $\pi_1 \colon \mathbb{R}^2 \to \mathbb{R}$, which projects the closed locus $x y = 1$ onto a non-closed subset of $\mathbb{R}$. (This is a quotient map, by the next remark.) 

1. It is easy to prove that a continuous open surjection $p \colon X \to Y$ is a quotient map. For instance, projection maps $\pi \colon X \times Y \to Y$ are quotient maps, provided that $X$ is inhabited. Likewise, a continuous closed surjection $p: X \to Y$ is a quotient map: $p^{-1}(U)$ is open $\Rightarrow$ $p^{-1}(\neg U)$ is closed $\Rightarrow$ $p(p^{-1}(\neg U)) = \neg U$ is closed $\Rightarrow$ $U$ is open. For example, a continuous surjection from a compact space to a Hausdorff space is a quotient map. 


+-- {: .num_prop #DetectViaSaturatedSubsetsContinuousQuotientMap}
###### Proposition

A [[continuous function]]

$$
  f \;\colon\; (X, \tau_X) \longrightarrow (Y,\tau_Y)
$$

whose underlying function $f \colon X \longrightarrow Y$ is [[surjective function|surjective]]
exhibits $\tau_Y$ as the corresponding [[quotient topological space|quotient topology]]
precisely if $f$ sends open and $f$-[[saturated subsets]] in $X$ to open subsets of $Y$.
By [this lemma](saturated+subset#ComplementOfSaturatedSubsetIsSaturated)  this is the case precisely if it sends
closed and $f$-saturated subsets to closed subsets.

=--




## Related concepts

* [[Sullivan model of finite G-quotient]]

* [[image]]

* [[subspace]], [[subframe]]

* [[quotient]], [[quotient stack]], [[quotient type]]

[[!include universal constructions of topological spaces -- table]]


[[!redirects quotient space]]
[[!redirects quotient spaces]]
[[!redirects identification space]]
[[!redirects identification spaces]]

[[!redirects quotient topology]]
[[!redirects quotient topologies]]
[[!redirects identification topology]]
[[!redirects identification topologies]]

[[!redirects quotient locale]]
[[!redirects quotient locales]]

[[!redirects quotient topological space]]
[[!redirects quotient topological spaces]]

[[!redirects topological quotient space]]
[[!redirects topological quotient spaces]]

[[!redirects quotient space topology]]
[[!redirects quotient space topologies]]
