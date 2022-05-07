
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

A _partition of unity_ is a [[partition]] of the unit function on a [[topological space]] into a sum of continuous functions that are each non-zero only on small parts of the space.


## Definition

Let $X$ be a [[topological space]]. A (point finite) **partition of unity** on $X$ is a collection $\{u_j\}_{j \in J}$ of [[continuous functions]] $u_j \colon X \to [0,1]$, $j\in J$ to the [[closed interval]] with its [[Euclidean space|Euclidean]] [[metric topology]] such that

 1. For each $x\in X$, there is only a [[finite number]] of $j\in J$ such that $u_j(x) \neq 0$ (point finiteness condition);

 1. $\sum_{j \in J} u_j(x) = 1$ for all $x\in X$.


A partition of unity defines an [[open cover]] of $X$, consisting of the open sets $u_j^{-1}(0,1]$. Call this the **induced cover**.

Sometimes (rarely) the condition that $\{u_j\}_J$ is point finite is dropped. In this case we refer to a _non-point finite_ partition of unity (see [[red herring principle]]). In this case for each point of $X$ at most countably-many of the functions $u_j$ are non-zero, and we have to interpret the sum in 1. above as being a [[convergence|convergent]] infinite [[series]].

Given a [[cover]] $\mathcal{U} = \{U_j\}_{j\in J}$ of a [[topological space]] ([[open cover]] or closed or neither), the partition of unity $\{u_j\}_J$ is **subordinate** to $\mathcal{U}$ if for all $j\in J$,
$$
\overline{u_j^{-1}(0,1]} \subset U_j.
$$

What this means is that the open sets $u_j^{-1}(0,1]$ form an open cover _refining_ the cover $\mathcal{U}$.

## Examples

+-- {: .num_example #PartitionOfUnityOnTheRealLine}
###### Example

Consider $\mathbb{R}$ with its [[Euclidean space|Euclidean]] [[metric topology]].

Let $\epsilon \in (0,\infty)$  and consider the [[open cover]]
$$
  \{
    (n-1-\epsilon , n+1 +  \epsilon) \subset \mathbb{R}
  \}_{n \in \mathbb{Z} \subset \mathbb{R} }.
$$

Then a partition of unity $\{ f_n \colon \mathbb{R} \to [0,1] \}_{n \in \mathbb{N}}$ subordinate to this cover is given by
$$
  f_n(x)
    \coloneqq
  \left\{
    \array{
      x - (n - 1)  &\vert& n - 1 \leq x \leq n
      \\
      1- (x-n) &\vert& n \leq x \leq n+1
      \\
      0 &\vert& \text{otherwise}
    }
  \right\}.
$$

=--


## Properties

### Existence on paracompact topological spaces

+-- {: .num_prop #ParacompactHausdorffEquivalentToexistenceOfParititionsOfUnity}
###### Proposition
**([[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]])**

Assuming the [[axiom of choice]] then:

Let $(X,\tau)$ be a [[topological space]]. Then the following are equivalent:

1. $(X,\tau)$ is a [[paracompact Hausdorff space]].

1. Every [[open cover]] of $(X,\tau)$ admits a subordinate partition of unity.

=--

Similarly [[normal spaces]] are equivalently those such that every [[locally finite cover]] has a subordinate partition of unity (reference Bourbaki, Topology Generale - find this!)

### The case of non-Hausdorff spaces

Slightly more generally,
a [[topological space]] (not necessarily Hausdorff)
is [[fully normal]] if and only every [[open cover]] admits a subordinate partition of unity.

A [[T1-space]] is [[fully normal]] if and only if it is [[paracompact]],
in which case it is also Hausdorff.

For [[topological spaces]] that are not [[T1-spaces]],
the condition of being [[fully normal]] is strictly stronger than [[paracompactness]].

### The case of locales

A [[regular locale]] is [[fully normal]] if and only if it is [[paracompact]].

The usual proof of the existence of partitions of unity
goes through for such locales since it does not make any use of points.

### Existence on smooth manifolds
 {#ExistenceOnSmoothManifolds}

Paracompact [[smooth manifolds]] even have _smooth_ partitions of unity subordinate to any open cover (this follows from the existence of a smooth [[bump function]] on $[-1,1]$). It is not true, however, that [[analytic manifolds]] have analytic partitions of unity - the aforementioned [[bump function]] is smooth but not analytic:

+-- {: .num_lemma #SmoothManifoldClosedBallRefinementOfCover}
###### Lemma
**([[open cover]] of [[smooth manifold]] admits [[locally finite cover|locally finite]] [[refinement]] by [[closed balls]])**

Let $X$ be a [[smooth manifold]] and let 
$\{U_i \subset X\}_{i \in I}$ be an [[open cover]]. 
Then there exists cover

$$
  \left\{
    B_0(\epsilon_j) 
      \underoverset{\simeq}{\psi_j}{\to}
    V_j
      \subset 
    X
  \right\}_{i \in J}
$$

which is a [[locally finite cover|locally finite]] [[refinement]] of $\{U_i \subset X\}_{i \in I}$ with each patch [[diffeomorphism|diffeomorphic]] to a [[closed ball]] in [[Euclidean space]].


=--

+-- {: .proof}
###### Proof

First consider the special case that $X$ is [[compact topological space]]. 

Let 

$$
  \left\{
    \mathbb{R}^n
      \underoverset{\simeq}{\phi_j}{\longrightarrow}
    V_j
    \subset X
  \right\}
$$

be a smooth [[atlas]] representing the [[smooth structure]] on $X$. The [[intersections]]

$$
  \left\{
    U_i \cap V_j
  \right\}_{i \in I, j \in J}
$$

still form an open cover of $X$. Hence for each point $x \in X$ there is $i \in I$ and $j \in J$ with $x \in U_i \cap V_j$. By the nature of the [[Euclidean topology]], there exists a [[closed ball]] $B_x$ around $\phi_j^{-1}(x)$ in $\phi_j^{-1}(U_i \cap V_j) \subset \mathbb{R}^n$. Its [[image]] $\phi_j(B_x) \subset X$ is a neighbourhood of  $x \in X$ diffeomorphic to a closed ball.

The [[interiors]] of these balls form an [[open cover]]

$$
  \left\{
    Int(B_x)
     \subset 
    X
  \right\}_{x \in X}
$$
 
of $X$ which, by construction, is a refinement of $\{U_i \subset X\}_{i \in I}$. By the assumption that $X$ is compact, this has a finite subcover

$$
  \left\{
    Int(B_l)
    \subset 
    X
  \right\}_{l \in L}
$$

for $L$ a [[finite set]]. Hence 

$$
  \left\{
    B_l
    \subset 
    X
  \right\}_{l \in L}
$$

is a finite cover by closed balls, hence in particular locally finite, and by construction it is still a refinement of the orignal cover.
This shows the statement for $X$ compact.

Now for general $X$, notice that without restriction we may assume that $X$ is [[connected topological space|connected]], for if it is not, then we obtain the required refinement on all of $X$ by finding one on each [[connected component]].

But if a locally Euclidean paracompact Hausdorff space $X$ is connected, then it is [[sigma-compact topological space|sigma-compact]] and in fact admits a countable increasing exhaustion

$$
  V_0 \subset V_1 \subset V_2 \subset \cdots
$$

by [[open subsets]] whose [[topological closures]]

$$
  K_0 \subset K_1 \subset K_2 \subset \cdots
$$

exhaust $X$ by [[compact topological space|compact]] subspaces $K_n$ (by the proof of [this prop.](topological+manifold#RegularityConditionsForTopologicalManifoldsComparison)).

For $n \in \mathbb{N}$, consider the open subspace

$$
  V_{n+2} \setminus K_{n-1}
    \;\subset\;
  X
$$

which canonically inherits the structure of a smooth manifold ([this prop.](differentiable+manifold#OpenSubsetsOfDifferentiableManifoldsAreDifferentiableManifolds)). As above we find a refinement of the restriction of $\{U_i \subset X\}_{i \in I}$ to this open subset by closed balls and since the further subspace $K_{n+1}\setminus K_n$ is still compact (by [this lemma](compact+space#UnionsAndIntersectionOfCompactSubspaces)) there is a finite set $L_n$ such that 

$$
  \{B_{l_n} \subset V_{n+2} \setminus K_{n-1} \subset X \}_{l_n \in L_n}
$$

is a finite cover of $K_{n+1} \setminus K_n$ by closed balls refining the original cover.


It follows that the union of all these 

$$
  \left\{
   B_{l_n} \subset X
  \right\}_{n \in \mathbb{N}, l_n \in L_n}
$$

is a refinement by closed balls as required. Its local finiteness follows by the fact that each $B_{l_n}$ is contained in the "strip" $V_{n+2} \setminus K_{n-1}$, each strip contains only a finite set of $B_{l_n}$-s and each strip intersects only a finite number of other strips. (Hence an open subset around a point $x$ which intersects only a finite number of elements of the refined cover is given by any one of the balls $B_{l_n}$ that contain $x$.)


=--


+-- {: .num_prop #SmoothManifoldAdmitsSmoothPartitionsOfUnity}
###### Proposition
**([[smooth manifolds]] admit smooth partitions of unity)**

Let $X$ be a paracompact [[smooth manifold]]. Then every [[open cover]] $\{U_i \subset X\}_{i \in I}$ has a subordinate partition of unity by functions $\{f_i \colon U_i \to \mathbb{R}\}_{i \in I}$ which are _[[smooth functions]]_.

=--


+-- {: .proof}
###### Proof

By lemma \ref{SmoothManifoldClosedBallRefinementOfCover} the given cover
has a [[locally finite cover|locally finite]] [[refinement]]
by [[closed subsets]] [[diffeomorphism|diffeomorphic]] to [[closed balls]]:

$$
  \left\{
    B_0(\epsilon_j) 
      \underoverset{\simeq}{\psi_j}{\to}
    V_j
      \subset 
    X
  \right\}_{j \in J}
  \,.
$$

Given this, let

$$
  h_j \;\colon\; X \longrightarrow \mathbb{R}
$$

be the function which on $V_j$ is given by a smooth [[bump function]] 

$$
  b_j \;\colon\; \mathbb{R} \longrightarrow \mathbb{R}
$$

with [[support]]  $supp(b_j) = B_0(\epsilon_j)$:

$$
  h_j
  \;\colon\;
  x 
  \mapsto
  \left\{
    \array{
      b_j(\psi_j^{-1}(x)) &\vert& x \in V_j
      \\
      0 &\vert& \text{otherwise}
    }
  \right.
  \,.
$$

By the nature of [[bump functions]] this is indeed a [[smooth function]] on all of $X$. By local finiteness of the cover by closed balls, the function

$$
  h \;\colon\; X \longrightarrow \mathbb{R}
$$

given by

$$
  h(x) 
    \coloneqq 
  \underset{j \in J}{\sum} h_j(x)
$$

is well defined (the sum involves only a finite number of non-vanishing contributions) and is smooth. Therefore setting

$$
  f_j \;\coloneqq\; \frac{h_j}{h}
$$

then 

$$
 \left\{
    f_j
 \right\}_{j \in J}
$$

is a subordinate partition of unity by smooth functions as required.



=--


### From a non-point finite partition of unity to a partition of unity

+-- {: .num_defn}
###### Definition

A collection of functions $\mathcal{U} = \{u_i : X \to [0,1]\}$ such that every $x\in X$ is in the support of some $u_i$. Then $\mathcal{U}$ is called _locally finite_ if the cover $u_i^{-1}(0,1]$ (i.e. the induced cover) is [[locally finite cover|locally finite]].
=--

+-- {: .num_prop}
###### Proposition
(Mather, 1965)

Let $\{u_i\}_J$ be a non-point finite partition of unity. Then there is a locally finite partition of unity $\{v_i\}_{i\in J}$ such that the induced cover of the latter is a refinement of the induced cover of the former.
=--

(For a proof, see p.354 of Dold's Lectures on algebraic topology. [Google books link to page 354](https://books.google.com.au/books?id=4AmzD9XhGDkC&lpg=PA354&vq=locally%20finite%20oartition%20unity&pg=PA354#v=onepage&q&f=false), which may or may not be visible.  Alternatively, see Lemma 5.1.8 on page 301 of Engelking.)

This implies that (loc. finite) [[numerable covers]] are cofinal in induced covers arising from collections of functions as in the definition. In particular, given the [[Milnor classifying space]] $\mathcal{B}^M G$ of a [[topological group]] $G$, which comes with a countable family of 'coordinate functions' $\mathcal{B}^M G \to [0,1]$, has a numerable cover. This is shown by Dold to be a trivialising cover for the universal bundle constructed by Milnor, and so the universal bundle is [[numerable bundle|numerable]].


## Applications 

### Maps to geometric realizations

Partitions of unity can be used in constructing maps from spaces to [[geometric realization]]s of [[simplicial spaces]] (incl. simplicial sets) - for example a [[classifying map]] for a $G$-[[bundle]] where $G$ is a [[Lie group]].


### Coboundaries for Cech cocycles {#CechCoboundaries}

Partitions of unity can be used to give explicit coboundaries for the cocycles of the complex of functions on a cover.

Let $\{U_i \to X\}$ be a [[open cover]] and $\{\rho_i \in C(X,\mathbb{R})\}$ a collection of functions with

* $(x \notin U_i) \Rightarrow \rho_i(x) = 0$

* $\sum_i \rho_i = const_1$.

Write $C(\{U_i\}) : \Delta^{op} \to Top$ for the [[Cech nerve]] of the cover and $C(C(\{U_i\}), \mathbb{R})$ for the [[cosimplicial ring]] of functions on this [[simplicial object|simplicial]] topological space; and $(C_\bullet(C(\{U_i\}), \mathbb{R}), \delta)$ for the corresponding (normalized) [[Moore complex|cochain complex]]: its differential is the alternating sum of the pullbacks of functions along the face maps, i.e. along the restriction maps

$$
  \delta = \sum_k (-1)^k \delta_{k}^*
  \,.
$$

For instance for $f = \{f_{i_1, i_2, \cdots, i_n} \in C(U_{i_1} \cap \cdots \cap U_{i_{n+1}})\}$ a collection of functions in degree $n$, we have

$$
  (\delta f)_{i_0 \cdots i_n i_{n+1}} =
  \sum_{k = 0}^{n+1} (-1)^k f_{i_0 \cdots i_{k-1} i_{k+1} \cdots i_{n+1}}
  \,.
$$ 

This cochain complex has vanishing [[cochain cohomology]] in positive degree. We can explicitly construct corresponding coboundaries using the partion of unity:

assume that with the above notation $f$ is a cocycle in positive degree, in that $\delta f  = 0$. Then define the $(n-1)$-cochain

$$
  \lambda_{i_1 \cdots i_n}
  :=
  \sum_{i_0} \rho_{i_0} f_{i_0 i_1 \cdots i_n}
  \,.
$$

Here in the summands on the right the product is defined on $U_{i_0} \cap U_{i_1} \cap \cdots \cap U_{i_n}$ and extended as 0 to all of $U_{i_1} \cap \cdots \cap U_{i_n}$.

With this definition we have

$$
  \delta \lambda = f
  \,.
$$

To see this we compute

$$
  \begin{aligned}
    (\delta \lambda)_{i_1 \cdots i_{n+1}}
    & :=
    \sum_{i_0} \rho_{i_0} \sum_{k=1}^n (-1)^k f_{i_0 i_1 \cdots i_{k-1} i_{k+1} \cdots i_{n+1}}
    \\
    & =
    \pm 
    \sum_{i_0} \rho_{i_0} 
    f_{i_1 \cdots i_{n+1}}
    \\
    & = f_{i_1 \cdots i_{n+1}}
  \end{aligned}
  \,,
$$

where in the second step we used the condition $\delta f = 0$ and in the last step we used the property of the partition of unity.

This construction is used a lot in [[Cech cohomology]]. For instance it can be used to show in Chech cocycles that every [[principal bundle]] admits a [[connection on a bundle]] (see there for the details).


## References

* [[Albrecht Dold]], _Partitions of unity in the theory of fibrations_, Ann. of Math. 78. (1963), 223-255.

* [[Albrecht Dold]], _Lectures on algebraic topology_, Springer Classics in Mathematics (1980), p.354.

* Engleking, _General topology_, (1989), p. 301

* M. Mather, _Paracompactness and partitions of unity_, PhD thesis, Cambridge (1965).

Discussion of partitions of unity in [[constructive mathematics]] is in

* {#Waaldijk96} [[Frank Waaldijk]], section 3.1 of _modern intuitionistic topology_, 1996 ([pdf](http://www.fwaaldijk.nl/modern%20intuitionistic%20topology.pdf))


[[!redirects partition of unity]]
[[!redirects partitions of unity]]
[[!redirects Partition of unity]]
[[!redirects Partitions of unity]]
