
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The _point space_ $\ast$ is the [[topological space]] whose underlying set is [[generalized the|the]] [[singleton]], and equipped with the unique topology that this set carries.


## Properties

### General

The point space is the [[terminal object]] in the [[category]] [[Top]] of topological spaces.

For $X$ any [[topological space]], then for every element of its underlying set there is a [[continuous function]] from the point space

$$
  \ast \longrightarrow X
$$

whose image is that point, and every such continuous function arises this way


### Relation to irreducible closed subspaces


For the following we write the point space explicitly as

$$
  \ast =
  \left\{
     \{1\}, \, \tau_\ast = \left\{ \emptyset, \{1\} \right\}
  \right\}
$$

+-- {: .num_prop #FrameHomomorphismsToPointAreIrrClSub}
###### Proposition

For $(X,\tau)$ a [[topological space]], then there is a [[bijection]] between
the [[irreducible closed subspaces]] of $(X,\tau)$ and the
[[frame]] [[homomorphisms]] from $\tau_X$ to $\tau_\ast$ from the [[frame of opens]] of $X$ to that of the point space. Moreover, this is  given by

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

Now according to prop. \ref{OpenSubsetVersionOfClosedIrreducible}
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


## Related concepts

[[!include universal constructions of topological spaces -- table]]


* [[Sierpinski space]]

[[!redirects point spaces]]

[[!redirects point topological space]]
[[!redirects point topological spaces]]
