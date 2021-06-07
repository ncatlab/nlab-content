+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

If $\mathcal{O}(X)$ is the topology on a [[topological space]] $X$ (i.e. its [[frame of opens]]), and if a map $\mathcal{O}(X) \to \mathcal{O}(1)$ that preserves finite [[meets]] and arbitrary [[joins]] (a [[homomorphism]] of [[frames]]) is considered an instance of "seeing a point $1 \to X$", then $X$ is _sober_ precisely if every point we see is really there (i.e., is induced from a [[continuous function]] $1 \to X$), and if we never see double. 

The condition that a [[topological space]] be _sober_ is an extra condition akin to a [[separation axiom]]. In fact with [[classical logic]] it is a condition implied by the $T_2$ [[separation axiom]] ([[Hausdorff implies sober]]) and implying $T_0$.

| [[separation axioms]]                 |
|---------------------------------------|
| $\array{\\ &&& T_2 = \text{Hausdorff}  \\ && \swArrow && \seArrow \\ \, & T_1 && && \text{sober} & \, \\ && \seArrow && \swArrow \\ &&& T_0 = \text{Kolmogorov} \\ }  $ |

(Note that this diagram is not a pullback -- there are [[Hausdorff implies sober|$T_1$ sober spaces which are not Hausdorff]].)

But the sobriety condition on a topological space has deeper meaning. It means that [[continuous functions]] between sober topological spaces are entirely determined by their [[inverse image]] functions on the [[frames of opens]], disregarding the underlying sets of points. Technically this means that the sober topological spaces are precisely the [[locales]] among the topological spaces.

## Definition

A [[topological space]] $X$ is **sober** if its [[points]] are exactly determined by its [[lattice of open subsets]].  Different equivalent ways to say this are:

* The [[continuous map]] from $X$ to the space of points of the [[locale]] that it gives rise to (see there for details) is a [[homeomorphism]].

* The [[function]] from points of $X$ to the _[[completely prime filter|completely prime filters]]_ of its open-set lattice is a [[bijection]].

* (Assuming classical logic) every [[irreducible closed set]] (non-empty closed set that is not the [[union]] of any two proper closed subsets) is the [[topological closure|closure]] of a unique point.

In each case, half of the definition is that $X$ is [[T0]], the other half states that $X$ has __enough points__:

+-- {: .num_defn #EnoughPointsOfATopologicalSpace}
###### Definition

A [[topological space]] $X$ has _enough points_ if the following equivalent conditions hold:

* The [[continuous map]] from $X$ to the space of points of the [[locale]] that it gives rise to (see there for details) is a [[quotient space|quotient map]].

* The [[function]] from points of $X$ to the _[[completely prime filter|completely prime filters]] of its [[lattice of open subsets|open-set lattice]] is a [[surjection]].

* (Assuming classical logic) every [[irreducible closed set]] (non-empty closed set that is not the [[union]] of any two proper closed subsets) is the [[topological closure|closure]] of a point.

=--

## Properties

### Separation

* Sobriety is a [[separation property]] that is stronger than [[T0]], but incomparable with [[T1]].  With [[classical logic]], every [[Hausdorff space]] is sober (see at _[[Hausdorff implies sober]]_), but this can fail [[constructive mathematics|constructively]].

$$
  Hausdorff = T_2 \Rightarrow sober \Rightarrow T_0
$$

### As locales with enough points
 {#AsLocalesWithEnoughPoints}

What makes the concept of sober topological spaces special is that
for them the concept of [[continuous functions]] may be expressed entirely in terms
of the relations between their [[open subsets]], disregarding the underlying set of points of which these open are in fact subsets. 
In order to express this
property (proposition \ref{FrameMorphismsBetweenOpensOfSoberSpaces} below), we first introduce the following terminology:

+-- {: .num_defn #HomomorphismOfFramesOfOpens}
###### Definition

Let $(X,\tau_X)$ and $(Y,\tau_Y)$ be [[topological spaces]].
Then a function

$$
  \tau_X \longleftarrow \tau_Y \;\colon\; \phi
$$

between their [[frame of opens|sets of open subsets]] is called a _[[frame]] [[homomorphism]]_
if it preserves

1. arbitrary [[unions]];

1. [[finite number|finite]] [[intersections]].

In other words, $\phi$ is a frame homomorphism if

1. for every [[set]] $I$ and every $I$-indexed set $\{U_i \in \tau_Y\}_{i \in I}$ of elements of $\tau_Y$, then

   $$
     \phi\left(\underset{i \in I}{\cup} U_i\right) \;=\; \underset{i \in I}{\cup} \phi(U_i)\;\;\;\;\in \tau_X
     \,,
   $$

1. for every [[finite set]] $J$ and every $J$-indexed set $\{U_j \in \tau_Y\}$ of elements in $\tau_Y$, then

   $$
     \phi\left(\underset{j \in J}{\cap} U_j\right)
       \;=\;
     \underset{j \in J}{\cap} \phi(U_j)
     \;\;\;\;\in \tau_X
     \,.
   $$

=--

+-- {: .num_remark #PreservationOfInclusionsByFrameHomomorphism}
###### Remark

A [[frame]] [[homomorphism]] $\phi$ as in def. \ref{HomomorphismOfFramesOfOpens}
necessarily also preserves inclusions in that 

* for every inclusion $U_1 \subset U_2$ with $U_1, U_2 \in \tau_Y \subset P(Y)$ then

  $$
    \phi(U_1) \subset \phi(U_2) \;\;\;\;\;\;\; \in \tau_X
    \,.
  $$
  
This is because inclusions are witnessed by unions

$$
  (U_1 \subset U_2)
    \;\Leftrightarrow\;
  \left( U_1 \cup U_2 = U_2 \right)
$$

and by finite intersections:

$$
  (U_1 \subset U_2)
    \;\Leftrightarrow\;
  \left(
    U_1 \cap U_2 = U_1
  \right)
  \,.
$$

=--

+-- {: .num_example}
###### Example

For

$$
  f \;\colon\; (X,\tau_X) \longrightarrow (Y, \tau_Y)
$$

a [[continuous function]], then its function of [[pre-images]]

$$
  \tau_X \longleftarrow \tau_Y \;\colon\; f^{-1}
$$

is a frame homomorphism according to def. \ref{HomomorphismOfFramesOfOpens}.

=--

For sober topological spaces the converse holds:

+-- {: .num_prop #FrameMorphismsBetweenOpensOfSoberSpaces}
###### Proposition

If $(X,\tau_X)$ and $(Y,\tau_Y)$ are [[sober topological spaces]], then
for every frame homomorphism (def. \ref{HomomorphismOfFramesOfOpens})

$$
  \tau_X \longleftarrow \tau_Y \;\colon\; \phi
$$

there is a unique [[continuous function]] $f \colon X \to Y$ such that $\phi$ is the function
of forming [[pre-images]] under $f$:

$$
  \phi = f^{-1}
  \,.
$$

=--

We prove this [below](#ProofOfFrameMorphismsBetweenOpensOfSoberSpaces), after the following lemma.

Let $\ast = (\{1\}, \tau_\ast = \left\{\emptyset, \{1\}\right\})$ be the [[point]] [[topological space]].


+-- {: .num_lemma #FrameHomomorphismsToPointAreIrrClSub}
###### Lemma

For $(X,\tau)$ a [[topological space]], then there is a [[bijection]] between 
the [[irreducible closed subspaces]] of $(X,\tau)$ and the
[[frame]] [[homomorphisms]] from $\tau_X$ to $\tau_\ast$, given bys

$$
  \array{
    Hom_{Frame}(\tau_X, \tau_\ast) 
      &\underoverset{\simeq}{}{\longrightarrow}&
    IrrClSub(X)
    \\
    \phi 
      &\mapsto& 
    X \backslash U_\emptyset(\phi)
  }
$$

where $U_\emptyset(\phi)$ is the [[union]] of all elements $U \in \tau_x$ such that $\phi(U) = \emptyset$:

$$
  U_{\emptyset}(\phi)
    \coloneqq
  \underset{{U \in \tau_X} \atop {\phi(U) = \emptyset} }{\cup}
   U
  \,.
$$


=--

See also ([[Stone Spaces|Johnstone 82, II 1.3]]).

+-- {: .proof}
###### Proof

First we need to show that the function is well defined in that given
a frame homomorphism $\phi \colon \tau_X \to \tau_\ast$ then  $X \backslash U_\emptyset(\phi)$
is indeed an irreducible closed subspace.

To that end observe that:

$(\ast)$ _If there are two elements $U_1, U_2 \in \tau_X$ with $U_1 \cap U_2 \subset U_{\emptyset}(\phi)$
then $U_1 \subset U_{\emptyset}(\phi)$ or $U_2 \subset U_{\emptyset}(\phi)$._

This is because

$$
  \begin{aligned}
    \phi(U_1) \cap \phi(U_2)
    & =
    \phi(U_1 \cap U_2)
    \\
    & \subset \phi(U_{\emptyset}(\phi))
    \\
    & =
    \emptyset
  \end{aligned}
  \,,
$$

where the first equality holds because $\phi$ preserves finite intersections by def. \ref{HomomorphismOfFramesOfOpens}, the inclusion holds because $\phi$ respects
inclusions by remark \ref{PreservationOfInclusionsByFrameHomomorphism}, and the second equality holds because $\phi$ preserves arbitrary unions
by def. \ref{HomomorphismOfFramesOfOpens}.
But in $\tau_\ast = \{\emptyset, \{1\}\}$ the intersection of two open subsets is empty precisely if at least one of them is empty,
hence $\phi(U_1) = \emptyset$ or $\phi(U_2) = \emptyset$. But this means that $U_1 \subset U_{\emptyset}(\phi)$ or $U_2 \subset U_{\emptyset}(\phi)$, as claimed.

Now according to [this prop.](irreducible+closed+subspace#OpenSubsetVersionOfClosedIrreducible),
the condition $(\ast)$ identifies the [[complement]]
$X \backslash U_{\emptyset}(\phi)$ as an [[irreducible closed subspace]] of $(X,\tau)$.

Conversely, given an irreducible closed subset $X \backslash U_0$, define $\phi$ by

$$
  \phi
    \;\colon\;
  U
    \mapsto
  \left\{
    \array{
      \emptyset & \vert \, \text{if} \, U \subset U_0
      \\
      \{1\} & \vert \, \text{otherwise}
    }
  \right.
  \,.
$$

This does preserve

1. arbitrary unions

   because $\phi(\underset{i}{\cup} U_i) = \{\emptyset\}$ precisely if $\underset{i}{\cup}U_i \subset U_0$ which is the
   case precisely if all $U_i \subset U_0$, which means that all $\phi(U_i) = \emptyset$ and because $\underset{i}{\cup}\emptyset = \emptyset$;

   while $\phi(\underset{i}{\cup}U_1) = \{1\}$ as soon as one of the $U_i$ is not contained in $U_0$, which means that
   one of the $\phi(U_i) = \{1\}$ which means that $\underset{i}{\cup} \phi(U_i) = \{1\}$;

1. finite intersections

   because if $U_1 \cap U_2 \subset U_0$, then by $(\ast)$ $U_1 \in U_0$ or $U_2 \in U_0$, whence $\phi(U_1) = \emptyset$
   or $\phi(U_2) = \emptyset$, whence with $\phi(U_1 \cap U_2) = \emptyset$ also $\phi(U_1) \cap \phi(U_2) = \emptyset$;

   while if $U_1 \cap U_2$ is not contained in $U_0$ then neither $U_1$ nor $U_2$ is contained in $U_0$ and hence with
   $\phi(U_1 \cap U_2) = \{1\}$ also $\phi(U_1) \cap \phi(U_2) = \{1\} \cap \{1\} = \{1\}$.

Hence this is indeed a frame homomorphism $\tau_X \to \tau_\ast$.

Finally, it is clear that these two operations are inverse to each other.

=--

+-- {: .proof #ProofOfFrameMorphismsBetweenOpensOfSoberSpaces}
###### Proof 
of prop. \ref{FrameMorphismsBetweenOpensOfSoberSpaces}


We first consider the special case of frame homomorphisms of the form

$$
  \tau_\ast \longleftarrow \tau_X \;\colon\; \phi
$$

and show that these are in bijection to the underlying set $X$, identified with the continuous functions
$\ast \to (X,\tau)$.

By lemma \ref{FrameHomomorphismsToPointAreIrrClSub}, the frame homomorphisms $\phi \colon \tau_X \to \tau_\ast$
are identified with the irreducible closed subspaces $X \backslash U_\emptyset(\phi)$ of $(X,\tau_X)$.
Therefore by assumption of [[sober topological space|sobriety]] of $(X,\tau)$ there is a unique point
$x \in X$ with $X \backslash U_{\emptyset} = Cl(\{x\})$. In particular this means that for $U_x$ an open
neighbourhood of $x$, then $U_x$ is not a subset of $U_\emptyset(\phi)$, and so it follows that $\phi(U_x) = \{1\}$.
In conclusion we have found a unique $x \in X$ such that

$$
  \phi
    \;\colon\;
  U \mapsto
  \left\{
    \array{
      \{1\} & \vert \,\text{if}\, x \in U
      \\
      \emptyset & \vert \, \text{otherwise}
    }
  \right.
  \,.
$$

This is precisely the [[inverse image]] function of the continuous function $\ast \to X$ which sends $1 \mapsto x$.

Hence this establishes the bijection between frame homomorphisms of the form $\tau_\ast \longleftarrow \tau_X$
and continuous functions of the form $\ast \to (X,\tau)$.

With this it follows that a general frame homomorphism of the form $\tau_X \overset{\phi}{\longleftarrow} \tau_Y$
defines a function of sets $X \overset{f}{\longrightarrow} Y$ by [[composition]]:

$$
  \array{
    X &\overset{f}{\longrightarrow}& Y
    \\
    (\tau_\ast \leftarrow \tau_X)
    &\mapsto&
    (\tau_\ast \leftarrow \tau_X \overset{\phi}{\longleftarrow} \tau_Y)
  }
  \,.
$$

By the previous analysis, an element $U_Y \in \tau_Y$ is sent to $\{1\}$ under this composite precisely if
the corresponding point $\ast \to X \overset{f}{\longrightarrow} Y$ is in $U_Y$, and similarly for
an element $U_X \in \tau_X$. It follows that $\phi(U_Y) \in \tau_X$ is precisely that subset of
points in $X$ which are sent by $f$ to elements of $U_Y$, hence that $\phi = f^{-1}$ is the [[pre-image]]
function of $f$. Since $\phi$ by definition sends open subsets of $Y$ to open subsets of $X$, it follows
that $f$ is indeed a continuous function. This proves the claim in generality.

=--




### Soberification reflection
 {#Reflection}

The [[category]] of sober spaces is [[reflective subcategory|reflective]] in the category of all topological spaces; the [[left adjoint]] is called the **soberification**.  

This reflection is also induced by the [[idempotent adjunction]] between spaces and [[locales]]; thus sober spaces are precisely those spaces that are the spaces of points of some [[locale]], and the [[category]] of sober spaces is [[equivalence of categories|equivalent]] to the category of [[locales with enough points]]. 

We now say this in detail.

Recall again the [[point]] topological space $\ast \coloneqq ( \{1\}, \tau_\ast = \left\{ \emptyset, \{1\}\right\} )$.


+-- {: .num_defn #SoberificationConstruction}
###### Definition

Let $(X,\tau)$ be a [[topological space]]. 

Define $S X$ to be the set

$$
  S X \coloneqq Hom_{Frame}( \tau_X, \tau_\ast )
$$

of [[frame]] [[homomorphisms]] from the [[frame of opens]] of $X$ to that of the point. Define a [[topological space|topology]] $\tau_{S X} \subset P(S X)$ on this set by declaring it to have one element $\tilde U$ for each element $U \in \tau_X$ and given by

$$
  \tilde U
    \;\coloneqq\;
  \left\{
    \phi \in S X
    \,\vert\,
    \phi(U) = \{1\}
  \right\}
  \,.
$$

Consider the function

$$
  \array{
    X &\overset{s_X}{\longrightarrow}& S X
    \\
    x &\mapsto& (const_x)^{-1}
  }
$$

which sends an element $x \in X$ to the function which assigns [[inverse images]] of the [[constant function]] $const_x \;\colon\; \{1\} \to X$ on that element.

=--

+-- {: .num_lemma #SoberificationConstructionWellDefined}
###### Lemma

The construction $(S X, \tau_{S X})$ in def. \ref{SoberificationConstruction} is a [[topological space]], and the function $s_X \colon X \to S X$ is a [[continuous function]]

$$
  s_X \colon (X, \tau_X) \longrightarrow (S X, \tau_{S X})
$$

=--

+-- {: .proof #ProofOfSoberificationConstructionWellDefined}
###### Proof

To see that $\tau_{S X} \subset P(S X)$ is closed under arbitrary unions and finite intersections, observe that the function

$$
  \array{
    \tau_X &\overset{\widetilde{(-)}}{\longrightarrow}& \tau_{S X}
    \\
    U &\mapsto& \tilde U
  }
$$

in fact preserves arbitrary unions and finite intersections. Whith this the statement follows by the fact that $\tau_X$ is closed under these operations.

To see that $\widetilde{(-)}$ indeed preserves unions, observe that (e.g. [Johnstone 82, II 1.3 Lemma](#Johnstone82))

$$
  \begin{aligned}
    p \in \underset{i \in I}{\cup} \widetilde{U_i} \;
    & \Leftrightarrow
    \underset{i \in I}{\exists} p(U_i) = \{1\}
    \\
    & \Leftrightarrow \underset{i \in I}{\cup} p(U_i) = \{1\}
    \\
    & \Leftrightarrow p\left(\underset{i \in I}{\cup} U_i\right) = \{1\}
    \\
    & \Leftrightarrow p \in \widetilde{ \underset{i \in I}{\cup} U_i }
  \end{aligned}
  \,,
$$

where we used that the frame homomorphism $p \colon \tau_X \to \tau_\ast$ preserves unions. Similarly for intersections, now with $I$ a [[finite set]]:

$$
  \begin{aligned}
    p \in \underset{i \in I}{\cap} \widetilde{U_i} \;
    & \Leftrightarrow
    \underset{i \in I}{\forall} p(U_i) = \{1\}
    \\
    & \Leftrightarrow \underset{i \in I}{\cap} p(U_i) = \{1\}
    \\
    & \Leftrightarrow p\left(\underset{i \in I}{\cap} U_i\right) = \{1\}
    \\
    & \Leftrightarrow p \in \widetilde{ \underset{i \in I}{\cap} U_i }
  \end{aligned}
  \,,
$$

where now we used that the frame homomorphism $p$ preserves finite intersections. 

To see that $s_X$ is continuous, observe that $s_X^{-1}(\tilde U) = U$, by construction.

=--

+-- {: .num_lemma #UnitIntoSXDetectsT0AndSoberity}
###### Lemma

For $(X, \tau_X)$ a [[topological space]],
the function $s_X \colon X \to S X$ from def. \ref{SoberificationConstruction} is

1. an [[injection]] precisely if $X$ is [[separation axiom|T0]];

1. a [[bijection]] precisely if $X$ is sober. 

   In this case $s_X$ is in fact a [[homeomorphism]].

=--

+-- {: .proof}
###### Proof

By lemma \ref{FrameHomomorphismsToPointAreIrrClSub} there is an identification $S X \simeq IrrClSub(X)$ and via this $s_X$ is identified with the map $x \mapsto Cl(\{x\})$. 

Hence the second statement follows by definition, and the first statement by [this prop.](separation+axioms#T0InTermsOfClosureOfPoints).

That in the second case $s_X$ is in fact a homeomorphism follows from the definition of the opens $\tilde U$: they are identified with the opens $U$ in this case (...expand...).

=--


+-- {: .num_lemma #SoberificationIsIndeedSober}
###### Lemma

For $(X,\tau)$ a [[topological space]], then the topological space $(S X, \tau_{S X})$ from def. \ref{SoberificationConstruction}, lemma \ref{SoberificationConstructionWellDefined} is sober. 

=--

(e.g. [Johnstone 82, lemma II 1.7](#Johnstone82))

+-- {: .proof}
###### Proof

Let $S X \backslash \tilde U$ be an [[irreducible closed subspace]] of $(S X, \tau_{S X})$. We need to show that it is the [[topological closure]] of a unique element $\phi \in S X$.

Observe first that also $X \backslash U$ is irreducible. 

To see this use [this prop.](irreducible+closed+subspace#OpenSubsetVersionOfClosedIrreducible), saying that irreducibility of $X \backslash U$ is equivalent to $U_1 \cap U_2 \subset U \Rightarrow (U_1 \subset U) or (U_2 \subset U)$. But if $U_1 \cap U_2 \subset U$ then also $\tilde U_1 \cap \tilde U_2 \subset \tilde U$ (as in the [proof](#ProofOfSoberificationConstructionWellDefined) of lemma \ref{SoberificationConstructionWellDefined}) and hence by assumption on $\tilde U$ it follows that $\tilde U_1 \subset \tilde U$ or $\tilde U_2 \subset \tilde U$. By lemma \ref{FrameHomomorphismsToPointAreIrrClSub} this in turn implies $U_1 \subset U$ or $U_2 \subset U$.  In conclusion, this shows that also $X \backslash U$ is irreducible . 

By lemma \ref{FrameHomomorphismsToPointAreIrrClSub} this irreducible closed subspace corresponds to a point $p \in S X$. By that same lemma, this frame homomorphism $p \colon \tau_X \to \tau_\ast$ takes the value $\emptyset$ on all those opens which are inside $U$. This means that the [[topological closure]] of this point is just $S X \backslash \tilde U$. 

This shows that there exists at least one point of which $X \backslash \tilde U$ is the topological closure. It remains to see that there is no other such point.

So let $p_1 \neq p_2 \in S X$ be two distinct points. This means that there exists $U \in \tau_X$ with $p_1(U) \neq p_2(U)$. Equivalently this says that $\tilde U$ contains one of the two points, but not the other. This means that $(S X, \tau_{S X})$ is [[separation axiom|T0]]. By [this prop.](separation+axioms#T0InTermsOfClosureOfPoints) this is equivalent to there being no two points with the same topological closure.

=--

+-- {: .num_prop}
###### Proposition

For $(X, \tau_X)$ any [[topological space]], for $(Y,\tau_Y^{sob})$ a sober topological space, and for $f \colon (X, \tau_X) \longrightarrow (Y, \tau_Y)$ a [[continuous function]], then it factors uniquely through the soberification $s_X \colon (X, \tau_X) \longrightarrow(S X, \tau_{S X})$ from def. \ref{SoberificationConstruction}, lemma \ref{SoberificationConstructionWellDefined}

$$
  \array{
    (X, \tau_X) &\overset{f}{\longrightarrow}& (Y, \tau_Y^{sob})
    \\
    {}^{\mathllap{s_X}}\downarrow & \nearrow_{\exists !}
    \\
    (S X , \tau_{S X})
  }
  \,.
$$

=--


+-- {: .proof}
###### Proof

By the construction in def. \ref{SoberificationConstruction}, we find that the outer part of the following square [[commuting square|commutes]]:

$$
  \array{
    (X, \tau_X) &\overset{f}{\longrightarrow}& (Y, \tau^{sob}_Y)
    \\
    {}^{\mathllap{s_X}}\downarrow & \nearrow& \downarrow^{\mathrlap{s_{S X}}}
    \\
    (S X, \tau_{S X})
     &\underset{S f}{\longrightarrow}&
    (S S X, \tau_{S S X})
  }
  \,.
$$

By lemma \ref{SoberificationIsIndeedSober} and lemma \ref{UnitIntoSXDetectsT0AndSoberity}, the right vertical morphism $s_{S X}$ is an isomorphism (a [[homeomorphism]]), hence has an [[inverse morphism]]. This defines the diagonal morphism, which is the desired factorization.

To see that this factorization is unique, consider two factorizations $\tilde f, \overline{f} \colon \colon (S X, \tau_{S X}) \to (Y, \tau_Y^{sob})$ and apply the soberification construction once more to the triangles

$$
  \array{
    (X, \tau_X) &\overset{f}{\longrightarrow}& (Y, \tau_Y^{sob})
    \\
    {}^{\mathllap{s_X}}\downarrow & \nearrow_{ \tilde f, \overline{f}}
    \\
    (S X , \tau_{S X})
  }
  \phantom{AAA}
    \mapsto
  \phantom{AAA}
  \array{
    (S X, \tau_{S X}) &\overset{S f}{\longrightarrow}& (Y, \tau_Y^{sob})
    \\
    {}^{\simeq}\downarrow & \nearrow_{ \tilde f, \overline{f}}
    \\
    (S X , \tau_{S X})
  }
  \,.
$$

Here on the right we used again lemma \ref{UnitIntoSXDetectsT0AndSoberity} to find that the vertical morphism is an isomorphism, and that $\tilde f$ and $\overline{f}$ do not change under soberification, as they already map between sober spaces. But now that the left vertical morphism is an isomorphism, the commutativity of this triangle for both $\tilde f$ and $\overline{f}$ implies that $\tilde f = \overline{f}$.

=--

### Enough points

A topological space has enough points in the sense of def. \ref{EnoughPointsOfATopologicalSpace} if and only if its $T_0$ quotient is sober.  The category of topological spaces with enough points is a [[reflective subcategory]] of the category [[Top]] of all topological spaces, and a topological space is [[T0]] iff this reflection is sober.


## Examples and Non-examples

* With [[classical logic]], every [[Hausdorff space]] is sober, but this can fail [[constructive mathematics|constructively]]. See at _[[Hausdorff implies sober]]_.

  {#NonComparisonToT1} Since the Hausdorff condition implies the $T_1$ [[separation axiom]], this means that ([[classical logic|classically]]) there is a large [[intersection]] of the [[classes]] of $T_1$-topological spaces and sober topological spaces. But neither class is contained in the other, as the following counter-examples show:

  * The [[Sierpinski space]] is sober, but not $T_1$.

  * The [[cofinite topology]] on a non-[[finite set]] is $T_1$ but not sober. 

 
* The topological space underlying any [[scheme]] is sober. See at _[[schemes are sober]]_.


Further examples of spaces that are _not_ sober includes the following:

* Any nontrivial [[indiscrete space]] is not sober, since it is not $T_0$. 

More interestingly: 

* For $R$ a [[commutative ring]], then the space $R^2$ with the [[Zariski topology]] is $T_1$ but not sober, since every subvariety is an irreducible closed set which is not the [[topological closure|closure]] of a point.  Its _soberification_ is, unsurprisingly, the [[scheme]] $Spec(R[x,y])$, which contains "generic points" whose closures are the subvarieties. 

The following non-example shows that sobriety is not a hereditary separation property, i.e., [[topological subspaces]] of sober spaces need not be sober:

* The [[Alexandroff topology]] on a [[poset]] is also not, in general, sober.  For instance, if $P$ is the infinite binary tree (the set of finite $\{0,1\}$-words ([[lists]]) with the "extends" preorder), then the soberification of its Alexandroff topology is [[Wilson space]], the space of finite or infinite $\{0,1\}$-words ([[streams]]).


## Related concepts

* [[nice topological space]]


## References

* [[Francis Borceux]], volume 3, section 1.9  of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)


* {#Johnstone82} [[Peter Johnstone]], section II.1, from II.1 on in _[[Stone Spaces]]_, Cambridge Studies in Advanced Mathematics __3__, Cambridge University Press 1982. xxi+370 pp. [MR85f:54002](http://www.ams.org/mathscinet-getitem?mr=698074), reprinted 1986.


* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], around definition IX.3.2 in _[[Sheaves in Geometry and Logic]]_


* Sober spaces in the [$\pi$-base](http://topology.jdabbs.com/properties/73).

[[!redirects sober]]
[[!redirects sober topological space]]
[[!redirects sober topological spaces]]
[[!redirects sober topology]]
[[!redirects sober topologies]]
[[!redirects sober space]]
[[!redirects sober spaces]]

[[!redirects sobrification]]
[[!redirects sobrifications]]

[[!redirects soberification]]
[[!redirects soberifications]]

[[!redirects sober reflection]]
[[!redirects sober reflections]]

[[!redirects soberification reflection]]
[[!redirects soberification reflections]]


[[!redirects topological space with enough points]]
[[!redirects topological spaces with enough points]]


