
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $T$ be an abelian [[Lawvere theory]] (one containing the theory of [[abelian groups]]). Write $\mathbb{A}^1$ for its canonical [[line object]] and $\mathbb{G}_m$ for the corresponding [[multiplicative group]]-object.

The **projective space** $\mathbb{P}_n$ of $T$ is the [[quotient]]

$$
  \mathbb{P}_n 
  \coloneqq
  (\mathbb{A}^{n+1} \setminus \{0\})/\mathbb{G}_m
$$

of the [[complement]] of yhe origin inside the $(n+1)$-fold [[Cartesian product]] of the line with itself by the canonical [[action]] of $\mathbb{G}_m$.

Any point $(x_0,x_1,\ldots,x_n)\in \mathbb{A}^{n+1} - \{0\}$ gives _homogeneous coordinates_ for its image under the quotient map. When considered in this fashion, one often writes $[x_0:x_1:\ldots:x_n]$. Homogeneous  coordinates were introduced in [M&#246;bius 27](#Mobius27)

More generally, for $(X,0)$ a [[pointed topological space]] with (pointed) $\mathbb{G}_m$-[[action]], the quotient

$$
 \mathbb{P}(X) 
  \;\coloneqq\;
  (X \setminus\{0\})
  /
  \mathbb{G}_m
$$

is the corresponding projective space.

If instead of forming the [[quotient]] one forms the [[quotient stack]]/[[action groupoid]], one speaks of the [[projective stack]]

$$
  \hat \mathbb{P}(X) 
  \coloneqq 
  (X\setminus\{0\})//\mathbb{G}_m
  \,.
$$




## Examples

### For commutative rings and algebras

For $T$ the theory of commutative [[ring]]s or more generally commutative [[associative algebra]]s over a ring $k$, $\mathbb{A}_k^1$ is the standard [[affine line]] over $k$. In this case $\mathbb{P}^n_k$ is (...) A closed sub[[scheme]] of $\mathbb{P}^n_k$ is a [[projective scheme]].

+-- {: .un_prop}
###### Proposition

For $R$ a commutative $k$-algebra, there is a [[natural isomorphism]] between

* $\mathbb{Z}$-[[graded algebra|gradings]] on $R$;

* $\mathbb{G}_m$-[[action]]s on $Spec R$.

=--

The proof is spelled out at _[[affine line]]_.


### Real and complex projective space
 {#RealAndComplexProjectiveSpace}

We discuss how complex projective space for $k$ the [[real numbers]] or the [[complex numbers]] equipped with their [[Euclidean space|Euclidean]] [[metric topology]] is a [[topological manifold]] and naturally carries the structure of a [[smooth manifold]] (prop. \ref{SmoothManifoldRealComplexProjectiveSpace} below).

* For $\mathbb{R}P^n$ is called _[[real projective space]]_,

* $\mathbb{C}P^n$  is called _[[complex projective space]]_,

  * $\mathbb{C}P^1$ is called the [[Riemann sphere]].

similarly

* $\mathbb{H}P^n$ is called _[[quaternionic projective space]]_.

For more see at these entries.

\linebreak

+-- {: .num_defn #TopologicalProjectiveSpace}
###### Definition
**(topological projective space)**

Let $n \in \mathbb{N}$. Consider the [[Euclidean space]] $k^{n+1}$ equipped with its [[metric topology]], let $k^{n+1} \setminus \{0\} \subset k^{n+1}$ be the [[topological subspace]] which is the [[complement]] of the origin, and consider on its underlying set the [[equivalence relation]] which identifies two points if they differ by [[multiplication]] with some $c \in k$ (necessarily non-zero):

$$
  (\vec x_1 \sim \vec x_2)
   \;\Leftrightarrow\;
  \left(
    \underset{c \in k}{\exists}
    ( \vec x_2 = c \vec x_1 )
  \right)
  \,.
$$

The [[equivalence class]] $[\vec x]$ is traditionally denoted

$$
  [x_1 : x_2 : \cdots : x_{n+1}]
  \,.
$$


Then the _[[projective space]]_ $k P^n$ is the corresponding [[quotient topological space]]

$$
  k P^n \;\coloneqq\; \left(k^{n+1} \setminus \{0\}\right) / \sim
  \,.
$$

=--

+-- {: .num_lemma #CanonicalInclusionOfProjectiveSpaces}
###### Lemma
**(canonical inclusion of projective spaces)**

For $n \in \mathbb{N}$ the function between topological projective spaces from def. \ref{TopologicalProjectiveSpace} given by

$$
  \array{
    k P^n &\overset{}{\longrightarrow}& k P^{n+1}
    \\
    [x_1 : \cdots : x_{n+1}] &\mapsto& [ x_1 : \cdots : x_{n+1} : 0]
  }
$$

is a [[continuous function]].

=--

+-- {: .proof}
###### Proof

There is a [[commuting square]] of functions of underlying sets of the form

$$
  \array{
    (x_1, \cdots, x_{n+1}) &\mapsto& (x_1, \cdots, x_{n+1}, 0)
    \\
    k^{n+1} & \overset{}{\longrightarrow} & k^{n+2}
    \\
    \downarrow &\searrow& \downarrow
    \\
    k P^n &\longrightarrow& k P^{n+1}
    \\
    [x_1 : \cdots : x_{n+1}] &\mapsto& [ x_1 : \cdots : x_{n+1} : 0]
  }
  \,,
$$

where the two vertical functions are the defining quotient co-projections, which are continuous functions by nature of [[quotient spaces]]. The top function is clearly continuous ([[polynomials are continuous]]) and hence so is its composite with the right co-projection, inducated by the diagonal arrow in the above diagram.

This implies that the bottom function is continuous by the nature (the [[universal property]]) of the quotient space topology.

=--

+-- {: .num_prop #QuotientOfnSphereTopologicalProjectiveSpace}
###### Proposition
**(projective space as quotient space of an $n$-sphere)**

For $n \in \mathbb{C}$ there are [[homeomorphisms]]

1. $S^{n}/(\mathbb{Z}/2) \simeq \mathbb{R}P^n$

   between

   1. the [[quotient space]] of the [[Euclidean space|Euclidean]] [[n-sphere]] canonically regarded as a [[subspace]] of the [[Euclidean space]] $\mathbb{R}^{n+1}$ by the [[equivalence relation]] which identifies two points $\vec p \in \mathbb{R}^{n+1}$ if they differ by multiplication by $-1$

   1. [[real projective space]] (def. \ref{TopologicalProjectiveSpace})

1. $S^{2n+1}/S^1 \simeq \mathbb{C}P^{n}$

   between

   1. the [[quotient space]] of the [[Euclidean space|Euclidean]] [[n-sphere|(2n+2)-sphere]], canonically regarded as a [[subspace]] of the [[Euclidean space]] $\mathbb{R}^{2n+2} \simeq \mathbb{C}^{n+1}$ by the [[equivalence relation]] which identifies two points $\vec p \in \mathbb{C}^{n+1}$ if they differ by multiplication by an complex number of unit norm

   1. [[complex projective space]] (def. \ref{TopologicalProjectiveSpace}).

=--

+-- {: .proof}
###### Proof

It is clear that there is a [[bijection]] of underlying sets as claimed: Under the equivalence relation defining projective space, every element $\vec x = (x_1, \cdots, x_{n+1}) \in k^{n+1}$ is equivalent to one of unit norm, namely $\frac{1}{\vert \vec x\vert} \vec x$, hence lying on the unit sphere. Representatives of this form are unique up to further multiplication by elements in $k \setminus \{0\}$ of unit norm.

It remains to see that this bijection is a [[homeomorphism]]. For definiteness of notation, we discuss this for the case $k = \mathbb{C}$, the case $k = \mathbb{R}$ works verbatim the same, with the evident substitutions.

So we have a [[commuting diagram]] of functions of underlying sets

$$
  \array{
    S^{2n+1} &\hookrightarrow& \mathbb{C}^{n+1} \setminus \{0\}
    \\
    {}^{\mathllap{q_{S^{2n+1}}}}\downarrow &\searrow^{\mathrlap{f}}& \downarrow^{\mathrlap{q_{\mathbb{C}^{n+1}}}}
    \\
    S^{2n+1}/S^1 &\longrightarrow& \mathbb{C}P^n
  }
$$

where the top horizontal and the two vertical functions are continuous, and where the bottom function is
is a bijection.  Since the diagonal composite is also continuous, the nature of the [[quotient space topology]]
implies that the bottom function is also continuous. To see that it is a [[homeomorphism]] it hence remains to
see that it is an [[open map]] (by [this prop.](homeomorphism#HomeoContinuousOpenBijection)).

So let $U \subset S^{2n+1}/S^1$ be an open set, which means that $q_{S^{2n+1}}^{-1}(U) \subset S^{2n+1}$ is an open set.
We need to see that $f(q_{S^{2n+1}}^{-1}(U)) \subset \mathbb{C}P^{n}$ is open, hence that
$q_{\mathbb{C}^{n+1}}^{-1}(f(q_{S^{2n+1}}^{-1}(U))) \subset \mathbb{C}^{n+1}$ is open.
Now by the nature of the [[Euclidean space|Euclidean]] [[metric topology]], the open subset $q_{S^{2n+1}}^{-1}(U)$
is a union of open balls $B^\circ_x(\epsilon)$ in $\mathbb{C}^{n+1}$ intersected with $S^{2n+1}$. But then $q_{\mathbb{C}^{n+1}}^{-1}(f(B^\circ_x(\epsilon)\vert_{S^{2n+1}}))$
is their [[orbit]] under the multiplicative action by $\mathbb{C} \setminus \{0\}$,
hence is a [[cylinder]] $B^\circ_x(\epsilon)\vert_{S^{2n+1}} \times (\mathbb{C} \setminus \{0\})$. This is clearly open.

=--


+-- {: .num_prop #CellComplexStructureOnTopologicalProjectiveSpace}
###### Proposition

There is a [[CW-complex]] structure on [[real projective space]] $\mathbb{R}P^n$ (def. \ref{TopologicalProjectiveSpace}) for $n \in \mathbb{N}$, given by [[induction]], where $\mathbb{R}P^{n+1}$ arises from $\mathbb{R}P^n$ by attaching a single cell of dimension $n+1$ with attaching map the [[projection]] $S^{n} \longrightarrow \mathbb{C}P^n$ from prop. \ref{QuotientOfnSphereTopologicalProjectiveSpace}:

$$
  \array{
     S^{n} &\longrightarrow& S^{n}/(\mathbb{Z}/2) \simeq \mathbb{R}P^n
     \\
     {}^{\mathllap{\iota_{n+1}}}\downarrow
       &(po)& \downarrow
     \\
     D^{n+1} &\underset{q}{\longrightarrow}& \mathbb{R}P^{n+1}
  }
  \,.
$$


Similarly, there is a [[CW-complex]] structure on [[complex projective space]] $\mathbb{C}P^n$ (def. \ref{TopologicalProjectiveSpace}) for $n \in \mathbb{N}$, given by [[induction]], where $\mathbb{C}P^{n+1}$ arises from $\mathbb{C}P^n$ by attaching a single cell of dimension $2(n+1)$ with attaching map the [[projection]] $S^{2n+1} \longrightarrow \mathbb{C}P^n$ from prop. \ref{QuotientOfnSphereTopologicalProjectiveSpace}:

$$
  \array{
     S^{2n+1} &\longrightarrow& S^{2n+1}/S^1 \simeq \mathbb{C}P^n
     \\
     {}^{\mathllap{\iota_{2n+2}}}\downarrow
       &(po)& \downarrow
     \\
     D^{2n+2} &\underset{q}{\longrightarrow}& \mathbb{C}P^{n+1}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

we discuss the case $k = \mathbb{C}$. The case $k= \mathbb{R}$ works verbatim the same, with the evident substitutions.

Given [[homogeneous coordinates]] $(z_0 ,  z_1 ,  \cdots ,  z_n ,  z_{n+1} ,  z_{n+2}) \in \mathbb{C}^{n+2}$ for $\mathbb{C}P^{n+1}$, let

$$
  \phi \coloneqq -arg(z_{n+2})
$$

be the [[phase]] of $z_{n+2}$. Then under the equivalence relation defining $\mathbb{C}P^{n+1}$ these coordinates represent the same element as

$$
  \frac{1}{\vert \vec z\vert}(e^{i \phi} z_0, e^{i \phi}z_1,\cdots, e^{i \phi}z_{n+1}, r)
  \,,
$$

where

$$
  r = {\vert z_{n+2}\vert}\in [0,1) \subset \mathbb{C}
$$

is the [[absolute value]] of $z_{n+2}$. Representatives $\vec z'$ of this form (${\vert \vec z' \vert = 1}$ and $z'_{n+2} \in [0,1]$) parameterize the [[n-disk|2n+2-disk]] $D^{2n+2}$  with [[boundary]] the $(2n+1)$-sphere at $r = 0$.

The resulting function $q \colon D^{2n+2} \to \mathbb{C}P^{n+1}$ is continuous: It may be factored as

$$
  \array{
    q_{D^{2n+2}} \colon & D^{2n+2} &\overset{\phantom{AAA}}{\hookrightarrow}& \mathbb{C}^{n+2} \setminus \{0\} &\overset{q_{\mathbb{C}^{n+2}}}{\longrightarrow}&  \mathbb{C}P^{n+1}
    \\
    & (Re(z_1), Im(z_1),  \cdots, Re(z_{n+1}), Im(z_{n+1}), r) &\mapsto& (z_1, \cdots, z_{n+1}, r)  &\mapsto& [ z_1 : \cdots : z_{n+1} : r ]
  }
$$

and here the first map is the [[embedding of topological spaces|embedding]] of the disk $D^{2n+2}$ as a [[hemisphere]] in $\mathbb{R}^{2n+1} \hookrightarrow \mathbb{R}^{2n+2} \simeq \mathbb{C}^{2n+2}$, while the second is the defining quotient space projection.
Both of these are continuous, and hence so is their composite.

The only remaining part of the action of $\mathbb{C}-\{0\}$ which fixes the conditions ${\vert z'\vert} = 0$ and $z'_{n+2}$ is
$S^1 \subset \mathbb{C} \setminus \{0\}$ acting on the elements with $ r = \{z'_{n+2}\} = 0$ by phase shifts on the $z_0, \cdots, z_{n+1}$.
The quotient of this remaining action on $D^{2(n+1)}$ identifies 
its boundary $S^{2n+1}$-sphere with $\mathbb{C}P^{n}$, by prop. \ref{QuotientOfnSphereTopologicalProjectiveSpace}.

This shows that the above square is a [[pushout]] diagram of underlying sets.

By the nature of [[colimits]] in [[Top]] ([this prop.](Top#DescriptionOfLimitsAndColimitsInTop))
it remains to see that the
[[topological space|topology]] on $\mathbb{C}P^{n+1}$ is the [[final topology]] induced by the functions
$D^{2n+2} \to \mathbb{C}P^{n+1}$ and $\mathbb{C}P^n \to \mathbb{C}P^{n+1}$, hence that a subset of
$\mathbb{C}P^{n+1}$ is open precisely if its pre-images under these two functions are open.

We saw above that $q_{D^{2n+2}}$ is continuous.
Moreover, also the function
$i_n \colon \mathbb{C}P^n \to \mathbb{C}P^{n+1}$ is continuous (by [this lemma](projective+space#CanonicalInclusionOfProjectiveSpaces)).

This shows that if a subset of $\mathbb{C}P^{n+1}$ is open, then its pre-images under these functions are open.
It remains to see that if $S \subset \mathbb{C}P^{n+1}$ is a subset with $q_{S^{2n+2}}^{-1}(S) \subset D^{2n+2}$ open and
$i_n^{-1}(S) \subset \mathbb{C}P^n$ open, then $S \subset \mathbb{C}P^{n+1}$ is open.

Notice that $q_{\mathbb{C}^{n+2}}^{-1}(S)$ contains with every point also its [[orbit]] under the [[action]]
of $\mathbb{C} \setminus \{0\}$, and that every open subset of $D^{2n+2}$ is a unions of open balls.
By the above factorization of $q_{D^{2n+2}}$ this means that if $q_{D^{2n+2}}^{-1}(S)$ is open, then
$q_{\mathbb{C}^{n+2}}^{-1}(S)$ is a union of open cyclinders, hence is open. By the nature of the
[[quotient topology]], this means that $S \subset \mathbb{C}P^n$ is open.

=--



+-- {: .num_defn #TopologicalProjectiveSpaceStandardOpenCover}
###### Definition
**(standard open cover of topological projective space)**

For $n \in \mathbb{N}$ the _standard open cover_ of the projective space $k P^n$ (def. \ref{TopologicalProjectiveSpace}) is

$$
  \left\{
    U_i \subset k P^n
  \right\}_{i \in \{1, \cdots, n+1\}}
$$

with

$$
  U_i
    \coloneqq
  \left\{
    [x_1 : \cdots : x_{n+1}] \in k P^n
    \;\vert\;
    x_i \neq 0
  \right\}
  \,.
$$

To see that this is an open cover:

1. This is a cover because with the orgin removed in $k^n \setminus \{0\}$ at every point $[x_1: \cdots : x_{n+1}]$
   at least one of the $x_i$ has to be non-vanishing.

1. These subsets are open in the [[quotient topology]] $k P^n = (k^n \setminus \{0\})/\sim$, since their [[pre-image]] under the quotient co-projection $k^{n+1} \setminus \{0\} \to k P^n$ coincides with the pre-image $(pr_i\circ\iota)^{-1}( k \setminus \{0\} )$ under the [[projection]] onto the $i$th coordinate in the [[product topological space]] $k^{n+1} = \underset{i \in \{1,\cdots, n\}}{\prod} k$ (where we write $k^n \setminus \{0\} \overset{\iota}{\hookrightarrow} k^n \overset{pr_i}{\to} k$).

=--

+-- {: .num_prop #nSphereAsCoveringSpaceOverRealProjectiveSpace}
###### Proposition
**([[n-sphere]] projecting to real projective space is [[covering space]] projection)

For $n \in \mathbb{N}$, the [[continuous function]] $p \;\colon\; S^n \to \mathbb{R}P^n$ from prop. \ref{QuotientOfnSphereTopologicalProjectiveSpace} 
is a [[covering space]] projection.

=--

+-- {: .proof}
###### Proof

We need to produce an [[open cover]] $\{U_i \subset \mathbb{R}P^n\}_{i \in I}$ such that the restrictions of the projection to this cover are [[homeomorphism|homeomorphic]] over the base to a [[product topological space]]

$$
  \array{
     U_i \times Disc(\mathbb{Z}_2)
       && \overset{\simeq}{\longrightarrow} && 
    S^n|_{U_i}
    \\
    & \searrow && \swarrow
    \\
    && U_i 
  }
  \,.
$$

Consider the standard open cover from def. \ref{TopologicalProjectiveSpaceStandardOpenCover}. Hence $i \in \{1, \cdots, n+1\}$
and $U_i$ consists of those lines through the origin in $\mathbb{R}^{n+1}$ which do not lie in the subspace defined by $x_i = 0$. The intersection of this subspace with the unit sphere $S^n \subset \mathbb{R}^{n+1}$ is an [[equator]] of the $n$-sphere, and so the [[complement]] of this equator is the [[disjoint union]] of the two open [[hemispheres]] $D_i^\pm \subset S^n$. Hence 

$$
  \array{
     S^n\vert_{U_i} & \simeq D_i^+ \sqcup D_i^- 
   }
  \,.
$$

Moreover, each line in $\mathbb{R}^{n+1}$ which corresponds to an element in $U_i$ intersects $D^+_i$ as well as $D^-_i$ exactly once. In particular therefore the $\mathbb{Z}_2$-action on $S^n$ restricts over $U_i$ to the interchange of these two hemispheres, and hence prop. \ref{QuotientOfnSphereTopologicalProjectiveSpace} gives the required homeomorphism as above.



=--


+-- {: .num_prop #ProjectiveSpaceOpenCoverIsAtlas}
###### Proposition
**(standard open cover is [[atlas]])**

The charts of the standard open cover of def. \ref{TopologicalProjectiveSpaceStandardOpenCover} are [[homomorphism|homeomorphic]] to [[Euclidean space]] $k^n$.

=--

+-- {: .proof}
###### Proof

If $x_i \neq 0$ then

$$
  [x_1 : \cdots : x_i : \cdots : x_{n+1}]
  =
  \left[
    \frac{x_1}{x_i} : \cdots : 1 : \cdots \frac{x_{n+1}}{x_i}
  \right]
$$

and the representatives of the form on the right are _unique_.

This means that

$$
  \array{
    \mathbb{R}^n &\overset{\phi_i}{\longrightarrow}& U_i
    \\
    (x_1, \cdots, x_{i-1}, x_{i+1}, \cdots, x_{n+1})
    &\mapsto&
    [x_1: \cdots: 1: \cdots : x_n+1]
  }
$$

is a bijection of sets.

To see that this is a [[continuous function]], notice that it is the composite

$$
  \array{
    && \mathrlap{\mathbb{R}^{n+1} \setminus \{x_i = 0\}}
    \\
    & {}^{\mathllap{\hat \phi_i}}\nearrow & \downarrow
    \\
    \mathbb{R}^n
     &
      \underset{\phi_i}{\longrightarrow}
     &
     U_i
  }
$$

of the function

$$
  \array{
    \mathbb{R}^n &\overset{\hat \phi_i}{\longrightarrow}& \mathbb{R}^{n+1} \setminus \{x_i = 0\}
    \\
    (x_1, \cdots, x_{i-1}, x_{i+1}, \cdots, x_{n+1})
    &\mapsto&
    (x_1, \cdots, 1, \cdots ,x_n+1)
  }
$$

with the quotient projection. Now $\hat \phi_i$ is a [[polynomial]] function and since [[polynomials are continuous]], and since the projection to a [[quotient topological space]] is continuous, and since composites of continuous functions are continuous, it follows that $\phi_i$ is continuous.

It remains to see that also the [[inverse function]] $\phi_i^{-1}$ is continuous.
Since

$$
  \array{
    \mathbb{R}^{n+1} \setminus \{x_i = 0\}
      &\overset{}{\longrightarrow}&
    U_i
      &\overset{\phi_i^{-1}}{\longrightarrow}&
    \mathbb{R}^n
    \\
    (x_1, \cdots, x_{n+1})
    && \mapsto &&
    ( \frac{x_1}{x_i}, \cdots, \frac{x_{i-1}}{x_i}, \frac{x_{i+1}}{x_i}, \cdots , \frac{x_{n+1}}{x_i})
  }
$$

is a [[rational function]], and since [[rational functions are continuous]], it follows, by nature of the [[quotient topology]], that $\phi_i$ takes open subsets to open subsets, hence that $\phi_i^{-1}$ is continuous.

=--

+-- {: .num_prop #SmoothManifoldRealComplexProjectiveSpace}
###### Proposition
**(real/complex projective space is [[smooth manifold]])**

For $k \in \{\mathbb{R}, \mathbb{C}\}$ the topological projective space $k P^n$ (def. \ref{TopologicalProjectiveSpace}) is a [[topological manifold]].

Equipped with the standard open cover of def. \ref{TopologicalProjectiveSpaceStandardOpenCover} regarded as an [[atlas]] by prop. \ref{ProjectiveSpaceOpenCoverIsAtlas}, it is a [[differentiable manifold]], in fact a [[smooth manifold]].

=--

+-- {: .proof}
###### Proof

By prop. \ref{ProjectiveSpaceOpenCoverIsAtlas} $k P^n$ is a [[locally Euclidean space]]. Moreover, $kP^n$ admits the structure of a [[CW-complex]] (by prop. \ref{CellComplexStructureOnTopologicalProjectiveSpace})
and therefore it is a [[paracompact Hausdorff space]] since [[CW-complexes are paracompact Hausdorff spaces]]. This means that it is a [[topological manifold]].

It remains to see that the [[gluing functions]] of this atlas are [[differentiable functions]] and in fact [[smooth functions]]. But by prop. \ref{ProjectiveSpaceOpenCoverIsAtlas} they are even [[rational functions]].

=--



## Related concepts

* [[projective plane]]

* [[projective variety]]

* [[Grassmannian]]

* [[projective G-space]]

  [[infinite complex projective G-space]]

* [[projective geometry]], [[synthetic projective geometry]]

* [[projective linear group]]

* [[tautological line bundle]]

* [[projective bundle]]

* [[affine space]], [[conical space]]

* [[direction of a vector]]

## References

* {#Mobius27} [[August Ferdinand Möbius]], _Der barycentrische Calc&#252;l_ (1827)

An introduction to projective spaces over the theory of ordinary commutative rings is in

* Miles Reid, _Graded rings and varieties in weighted projective space_ ([pdf](http://www.warwick.ac.uk/~masda/surf/more/grad.pdf))

* [[Aurelio Carboni]], [[Marco Grandis]] , _Categories of projective spaces_ , JPAA **110** (1996) pp.241-258.

[[!redirects projective spaces]]

[[!redirects homogeneous coordinates]]

