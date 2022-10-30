
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


## Examples

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

The [[singular homology]] of product topological spaces is informed by

* [[Eilenberg-Zilber theorem]]

* [[Künneth theorem]]

## Related concepts

* [[tensor product of chain complexes]]




[[!redirects product topological spaces]]

[[!redirects product space]]
[[!redirects product spaces]]
