
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given two [[topological spaces]] $(X_1,\tau_1)$ and $(X_2, \tau_2)$, then the [[Cartesian product]] of their underlying sets $X_1 \times X_2$ is naturally equipped with a [[topological space|topology]] $\tau_{X_1 \times X_2}$ itself, generated from the [[base of a topology|base opens]] which are themselves Cartesian product $U_1 \times U_2 \subset X_1 \times X_2$, of [[open subsets]] of the original spaces: $U_i \subset X_i$. The resulting topological space

$$
  (X_1 \times X_2 , \tau_{X_1 \times X_2})
$$

is called the _product topological space_ of the two original spaces.

The [[formal duality|formally dual]] concept is that of [[disjoint union topological spaces]].

More generally, consider any index [[set]] $I$ and an $I$-indexed set $\{X_i, \tau_i\}_{i \in I}$ of [[topological spaces]]. Then the _product topology_ $\tau_{prod}$ or _[[Tychonoff topology]]_ on the [[Cartesian product]] $\underset{i \in I}{\prod} X_i$ of underlying sets is equivalently

1. the topology generated from the [[sub-base of a topology|sub-base]] given by products $\underset{i \in I}{\prod} U_i$ with $U_i \subset X_i$ open, but _all except one of the factors_ equal to the corresponding $X_i$, 

   hence the topology whose open subsets are precisely those obtained as arbitrary unions of finite intersections of such subsets;

1. the topology generated from the [[base of a topology|base]] given by products $\underset{i \in I}{\prod} U_i$ with $U_i \subset X_i$ open, but _all except a finite number of factors_ equal to the corresponding $X_i$,

   hence the topology whose open subsets are precisely those obtained as arbitrary unions of such subsets.

This product topology is singled out by the fact that the resulting product topological space is the [[category theory|category theoretic]]  [[product]] of the original space in the [[category]] [[Top]] of topological spaces:

$$
  \left(
     \underset{i \in I}{\prod} X_i
     ,\;
     \tau_{prod}
  \right)
  \;\simeq\;
  \underset{i \in I}{\prod} (X_i, \tau_i)
  \,.
$$

This means that the product topology enjoys the [[universal property]] that for any topological space $(Y,\tau_Y)$ then sets of [[continuous functions]] $\{(Y, \tau_Y) \overset{\phi_i}{\to} (X_i, \tau_i)\}_{i \in I}$ into the factor spaces are in [[natural bijection]] with continuous functions $(\phi_i)_{i \in I} \colon (Y, \tau_Y) \to \left(\underset{i \in I}{\prod} X_i, \tau_{prod}\right)$ into the product topological space.


Beware that (among others) there is also the _[[box topology]]_ $\tau_{box}$ on the Cartesian product of underlying sets $\underset{i\in I}{\prod} X_i$, whose open subsets are the unions of those of the for $\underset{i \in I}{\prod} U_i$ with $U_i \subset X_i$ open and with _no_ further restriction on the factors. 

For $I$ a [[finite set]], then these two topologies coincide, but for 
$I$ not finite then the box topology is a strictly [[fine topology|finer topology]]

$$
  \tau_{prod} \subset \tau_{box}
$$

and hence in this case it does _not_ enjoy the [[universal property]] of the product topology above. 

[[!include universal constructions of topological spaces -- table]]

## Definition

+-- {: .num_defn #ProductTopologicalSpace}
###### Definition

Let $\{(X_i, \tau_i)\}_{i \in I}$ be a [[set]] of [[topological spaces]]. Then their _product topological space_ has as underlying set the [[Cartesian product]] $\underset{i \in I}{\prod} X_i$ of the underlying sets, and has as topology $\tau_{prod} \subset P(\underset{i \in I}{\prod} X_i)$ the [[coarse topology|coarsest topology]] such that all the [[projection]] maps

$$
   p_i 
  \;\colon\;
   \underset{i \in I}{\prod} X_i
   \longrightarrow
    X_i
$$

become [[continuous functions]] (calle the _Tychonoff topology_). 

This means equivalently that $\tau_{prod}$ is the topology generated from the [[sub-base of a topology|sub-base]] 

$$
   \beta_{prod}
   \;\coloneqq\;
   \left\{
      p_i^{-1}(U_i) \subset \underset{i \in I}{\prod} X_i
      \;\vert\;
      i \in I, U_i \subset X_i \, \text{open} 
   \right\}
   \,.
$$

=---

Notice that 

$$
  p_i^{-1}(U_i)
  =
  U_i 
  \times
  \left(\underset{j \in I \backslash \{i\}}{\prod} X_j\right)
$$

and that 

$$
  p_i^{-1}(U_i)
  \cap
  p_j^{-1}(U_j)
  =
  U_i \times U_j
  \times
  \left(\underset{k \in I \backslash \{i,j\}}{\prod} X_k\right)
$$

etc.

## Examples

+-- {: .num_example #ProductWithDiscreteFiniteTopologicalSpace}
###### Example

Let $X$ be any [[topological space]] and write $Disc(\{1,2\})$ for the [[discrete topological space]] on a set with two elements. Then there is a [[homeomorphism]]

$$
  X \times Disc(\{0,1\})
    \;\simeq\;
  X \sqcup X
$$

between the product space of $X$ with $Disc(\{1,2\})$ and the [[disjoint union space]] of $X$ with itself.

=--

+-- {: .proof}
###### Proof

By definition of [[disjoint union]] there is a [[bijection]] of underlying sets 
$X \sqcup X \simeq X \times \{1,2\}$.

By unwinding the definitions 

1. the open subsets of $X \times Disc(\{0,1\})$ are unions of those of the form $U \times S$, where $U \subset X$ is an open subset and $S \subset \{1,2\}$ is any subset

1. the open subsets of $X \sqcup X$ are of the form $U \sqcup V$ with $U,V \subset X$ open.

Under the above bijection the we have 

$$
  U \sqcup V = \left(U \times \{1\}\right) \cup \left( V \times \{2\}\right)
  \,.
$$

Conversely, every union of elements of the form $U' \times \{1\}$, $V' \times \{2\}$ and $W \times \{1,2\} = W \times \{1\} \cup W \times \{2\}$ is of the form $U \times \{1\} \cup V \times \{2\}$. 

This shows that the above bijection of underlying sets induces a bijection of the corresponding open subsets, hence is a homeomorphism.

=--


+-- {: .num_example}
###### Example

For $n \in \mathbb{N}$ consider the [[Cartesian space]] $\mathbb{R}^n$ with the [[metric topology]] induced from its [[Euclidean space|Euclidean metric]] structure. Then the product topological spaces satisfy

$$
  \mathbb{R}^{n_1}\times \mathbb{R}^{n_2}
  \simeq
  \mathbb{R}^{n_1 + n_2}
  \,.
$$


=--

+-- {: .num_example #InfiniteProductOfDiscreteSpaces}
###### Example

Let $Disc(S)$ be a [[discrete topological space]] on a set with at least two elements. Then the infinite product space

$$
  \underset{n \in \mathbb{Z}}{\prod} Disc(S)
$$

is itself _not_ a discrete space.

=--

+-- {: .proof}
###### Proof

The open subsets of a discrete space include _all_ the subsets of the underlying set. Hence we need to see that there are subsets of the [[Cartesian product]] set   $\underset{n \in \mathbb{Z}}{\prod} Disc(S)$ which are not open subsets in the Tychonoff topology.

But by definition the open subsets in the Tychnoff topology are unions of products of open subsets of the factor spaces such that only a finite number of the factors is not the total space.

Since $S$ is assumed to contain at least two elements let $1 \in S$ be one of these. Then $\{1\} \subset S$ is a proper subset. Accordingly the product subset

$$
  \underset{n \in \mathbb{B}}{\prod} \{1\}
  \;\subset\;
  \underset{n\in \mathbb{N}}{\prod} Disc(S)
$$

is not open. For if it were, it would have to be the union of product subsets that contain the total set $S$ in at least one entry, which by construction it is not.

=--




+-- {: .num_example #CantorSpace}
###### Example
**([[Cantor space]])**

Write $Disc(\{0,1\})$ for the the [[discrete topological space]] with two points. Write $\underset{n \in \mathbb{N}}{\prod} Disc(\{0,2\})$ for the [[product topological space]] of a [[countable set]] of copies of this discrete space with itself (i.e. the corresponding [[Cartesian product]] of sets $\underset{n \in \mathbb{N}}{\prod} \{0,1\}$ equipped with the Tychonoff topology induced from the [[discrete topology]] of $\{0,1\}$).

Then consider the [[function]]

$$
  \array{
    \underset{n \in \mathbb{N}}{\prod}
      &\overset{\kappa}{\longrightarrow}&
    [0,1]
    \\
    (a_i)_{i \in \mathbb{N}}
    &\overset{\phantom{AAAA}}{\mapsto}&
    \underoverset{i = 0}{\infty}{\sum} \frac{2 a_i}{ 3^n}
  }
$$

which sends an element in the product space, hence a [[sequence]] of binary digits, to the value of the [[power series]] as shown on the right.

One checks that this is a [[continuous function]] (from the [[product topology]] to the [[Euclidean space|Euclidean]] [[metric topology]] on the [[closed interval]]). Moreover with its [[image]] $\kappa\left( \underset{n \in \mathbb{N}}{\prod} \{0,1\}\right) \subset [0,1]$ equipped with its [[subspace topology]], then this is a [[homeomorphism]] onto its image:

$$
  \underset{n \in \mathbb{N}}{\prod} Disc(\{0,1\})
    \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow}
  \kappa\left(
    \underset{n \in \mathbb{N}}{\prod} Disc(\{0,1\})
  \right)
    \overset{\phantom{AAAA}}{\hookrightarrow}
  [0,1]
  \,.
$$

This image is the _[[Cantor space]]_ as a subspace of the closed interval.


=--


## Properties

### Basic properties

+-- {: .num_prop #ProjectionsAreOpenMaps}
###### Proposition
**([[projections]] are [[open maps]])**

For $\{X_i\}_{i \in I}$ a set of topological spaces, the for each $j \in I$ the [[projection]] out of their product space into the $j$th component

$$
 p_j \;\colon\; \underset{i \in I}{\prod} X_i \longrightarrow X_j
$$

is an [[open map]].

=--

+-- {: .proof}
###### Proof

Since images preserve unions ([this prop.](interactions+of+images+and+pre-images+with+unions+and+intersections#PreservationOfUnionsAndIntersectionsOfSets)) it is sufficient to check that the image under $p_j$ of a [[base fo the topology|base open]] is still open. But base opens in the product topology by definition are, in particular, products of open subsets.

=--



### Universal property

The product topological space construction from def. \ref{ProductTopologicalSpace} is the [[limit]] in [[Top]] over the [[discrete category|discrete]] [[diagram]] consisting of the factor spaces, hence the [[category theory|category theoretic]] [[product]]. 

For **proof** see at [Top -- Universal constructions](Top#UniversalConstructions).

### The Tychonoff theorem

The [[Tychonoff theorem]] states that the product space of any set of [[compact topological spaces]] (with its Tychonoff topology) is itself compact.

### Relation to smash product of pointed spaces

+-- {: .num_prop #OnePointCompactificationAndSmashProduct}
###### Proposition
**([[one-point compactification intertwines Cartesian product with smash product]])

On the [[subcategory]] $Top_{LCHaus}$ of [[Top]] on the [[locally compact Hausdorff spaces]] with [[proper maps]] between them, the [[functor]] of [[one-point compactification]] (Prop. \ref{OnePointCompactificationFunctor})

$$
  (-)^{cpt}
  \;\colon\;
  Top_{LCHaus}
  \longrightarrow 
  Top^{\ast/}
$$

sends [[Cartesian products]] ([[product topological spaces]]) to [[smash products]] of [[pointed topological spaces]], hence constitutes a [[strong monoidal functor]], in that there is a [[natural transformation|natural]] [[homeomorphism]]:

$$
  \big(
    X \times Y 
  \big)^{cpt}
  \;\simeq\;
  X^{cpt} \wedge Y^{cpt}
  \,.
$$

=--

This is briefly mentioned in [Bredon 93, p. 199](one-point+compactification#Bredon93).
The argument is spelled out in: [MO:a/1645794/](https://math.stackexchange.com/a/1645794/58526), [Cutler 20, Prop. 1.6](one-point+compactification#Cutler20).

### Relation to singular (co)homology

The [[singular homology]] of product topological spaces is informed by

* [[Eilenberg-Zilber theorem]]

* [[Künneth theorem]]

## Related concepts

* [[product manifold]]

* [[tensor product of chain complexes]]

[[!include universal constructions of topological spaces -- table]]


## References

The _Tychonoff topology_ is named after [[A. N. Tychonoff]].

* [[Terence Tao]], _Notes on products of topological spaces_ ([pdf](http://www.math.ucla.edu/~tao/resource/general/121.1.00s/product.pdf))

* [[Florian Herzig]], _Product topology_ ([pdf](http://www.math.toronto.edu/~herzig/MAT327-lecturenotes08.pdf))

* {#Terilla14} [[John Terilla]],  _Notes on categories, the subspace topology and the product topology_ 2014 ([pdf](https://math.mit.edu/~jhirsh/terilla_subspace_quotient.pdf))


[[!redirects product topological spaces]]

[[!redirects product space]]
[[!redirects product spaces]]


[[!redirects Tychonoff product]]
[[!redirects Tychonoff products]]
[[!redirects Tychonov product]]
[[!redirects Tychonov products]]
[[!redirects Tykhonoff product]]
[[!redirects Tykhonoff products]]
[[!redirects Tykhonov product]]
[[!redirects Tykhonov products]]
[[!redirects Tichonoff product]]
[[!redirects Tichonoff products]]
[[!redirects Tichonov product]]
[[!redirects Tichonov products]]
[[!redirects Tikhonoff product]]
[[!redirects Tikhonoff products]]
[[!redirects Tikhonov product]]
[[!redirects Tikhonov products]]
[[!redirects Тиьонов product]]
[[!redirects Тиьонов products]]

[[!redirects Tychonoff topology]]
[[!redirects Tychonoff topologies]]
[[!redirects Tychonov topology]]
[[!redirects Tychonov topologies]]
[[!redirects Tykhonoff topology]]
[[!redirects Tykhonoff topologies]]
[[!redirects Tykhonov topology]]
[[!redirects Tykhonov topologies]]
[[!redirects Tichonoff topology]]
[[!redirects Tichonoff topologies]]
[[!redirects Tichonov topology]]
[[!redirects Tichonov topologies]]
[[!redirects Tikhonoff topology]]
[[!redirects Tikhonoff topologies]]
[[!redirects Tikhonov topology]]
[[!redirects Tikhonov topologies]]
[[!redirects Тиьонов topology]]
[[!redirects Тиьонов topologies]]

[[!redirects topological product]]
[[!redirects topological products]]

[[!redirects product topology]]
[[!redirects product topologies]]

