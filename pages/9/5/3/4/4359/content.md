
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

## Definition

+-- {: .num_defn #ClosedIrreducible}
###### Definition

Given a [[topological space]] $X$, a [[closed subspace]] $F$ of $X$ is __irreducible__ if it is [[inhabited]] and not the [[union]] of two closed proper (i.e. smaller) subspaces. In other words, $F$ is irreducible if whenever $F_1$ and $F_2$ are closed subsets of $X$ such that 

$$
  F = F_1 \cup F_2
$$

then $F_1 = F$ or $F_2 = F$.

=--

Equivalently this may be expressed in terms of [[open subsets]]:

+-- {: .num_prop #OpenSubsetVersionOfClosedIrreducible}
###### Proposition

Let $(X, \tau)$ be a [[topological space]], and let $P \in \tau \subset P(X)$ be a proper [[open subset]],
so that the [[complement]] $F \coloneqq X\backslash P$ is an [[inhabited]] [[closed subspace]]. Then $F$ 
is [[irreducible closed subspace|irreducible]] in the sense of def. \ref{ClosedIrreducible} precisely if whenever $U_1,U_2 \in \tau$ are open subsets
with $U_1 \cap U_2 \subset P$ then $U_1 \subset P$ or $U_2 \subset P$:

$$
  X \backslash P \,\text{irreducible}
  \;\Leftrightarrow\;
  \left(
    \underset{U_1, U_2 \in \tau}{\forall } 
    \left(
      \left(
        U_1 \cap U_2 \subset P
      \right) 
      \;\Rightarrow\;
      \left(U_1 \subset P \;\text{or}\; U_2 \subset P\right)
    \right)
  \right)
$$

=--

+-- {: .proof}
###### Proof

Every [[closed subset]] $F_i \subset F$ may be exhibited as the [[complement]]

$$
  F_i = F \backslash U_i
$$

for some open subset $U_i \in \tau$. Observe that under this identification the condition
that $U_1 \cap U_2 \subset P$ is equivalent to the condition that $F_1 \cup F_2 = F$,
because it is equivalent to the equation labeled $(\star)$ in the following sequence of equations:

$$
\begin{aligned}
  F_1 \cup F_2
  & = 
  (F \backslash U_1) \cup (F \backslash U_2) 
  \\
  & 
  = \left( X \backslash (P \cup U_1) \right) \cup \left( X \backslash P \cup U_2 \right)
  \\
  & = X \backslash ( P \cup (U_1 \cap U_2)  )  
  \\
  & \stackrel{(\star)}{=}   X \backslash P 
  \\
  & = F  
\end{aligned}
\,.
$$

Similarly, the condition that $U_i \subset P$ is equivalent to the condition that $F_i = F$,
because it is equivalent to the equality $(\star)$ in the following sequence of equalities:

$$
  \begin{aligned}
    F_i &= F \backslash U_i
    \\
    & = X \backslash ( P \cup U_i )
    \\
    & \stackrel{(\star)}{=} X \backslash P
    \\
    & = 
    F
  \end{aligned}
  \,.
$$

Under these equivalences, the two conditions are manifestly the same.

=--

Yet another equivalent characterization is in terms of frame homomorphisms:

In the following we write

$$
  \ast \coloneqq (\{1\}, \tau_\ast = \left\{ \emptyset, \{1\}\right\})
$$

for the [[point]], regarded, uniquely, as a topological space, the [[point space]].

+-- {: .num_prop #FrameHomomorphismsToPointAreIrrClSub}
###### Proposition

For $(X,\tau)$ a [[topological space]], then there is a [[bijection]] between
the [[irreducible closed subspaces]] of $(X,\tau)$ and the
[[frame]] [[homomorphisms]] from $\tau_X$ to $\tau_\ast$, given by

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
    & \subset \phi(U_{\emptyset}(\emptyset))
    \\
    & =
    \emptyset
  \end{aligned}
  \,,
$$

(where the first equality holds because $\phi$ preserves finite intersections, the inclusion holds because $\phi$ respects
inclusions, and the second equality holds because $\phi$ preserves arbitrary unions).
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

   because $\phi(\underset{i}{\cup} U_i) = \emptyset$ precisely if $\underset{i}{\cup}U_i \subset U_0$ which is the
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

+-- {: .num_remark #locales}
###### Remark

Note that frame homomorphisms from $\tau_X$ to $\tau_\ast$ are the same thing as [[continuous maps]] from the [[locale]] $\mathcal{O}_\ast$ to the locale $\mathcal{O}_X$ (that is, in the other direction, regarding the frames of opens as instead being locales).  Thus, the irreducible closed subspaces correspond to what *should* be the points of the space, if we regard it as much as possible as a locale, that is the [[points of the locale]] $\mathcal{O}_X$.  At a more elementary level, these are also the same thing as the [[completely prime filters]] in the frame $\tau_X$.
=--


## Properties

Note that the [[closure]] of (the [[singleton]] set on) any [[point]]/[[element]] of $X$ is an irreducible closed subspace.  $X$ is [[sober space|sober]] if and only if every irreducible closed subspace is the closure of a unique point of $X$.  In general, the irreducible closed subspaces of $X$ correspond to the [[point of a locale|points]] of the [[topological locale]] $\Omega(X)$, which are (by definition) the [[completely prime filters]] on the [[frame of open subspaces]] of $X$.  Specifically, given an irreducibly closed subspace, the filter of open subspaces that contain it is completely prime; conversely, given a completely prime filter of open subspaces, the closure of its intersection is irreducible.

The theory of irreducible closed subspaces is not useful in [[constructive mathematics]]; instead, one must use the [[completely prime filters]] directly.  While one might hope that the irreducibly open subsets (that is those that satisfy the conditions of Proposition \ref{OpenSubsetVersionOfClosedIrreducible}) might be more tractible constructively, they are in fact no better.  (We should probably put in the classical proof and see where it goes wrong.)


## Related concepts

* [[closed point]]


## References

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], around definition IX.3.2 in _[[Sheaves in Geometry and Logic]]_


[[!redirects irreducible closed subspace]]
[[!redirects irreducible closed subspaces]]
[[!redirects irreducible closed subset]]
[[!redirects irreducible closed subsets]]
[[!redirects irreducible closed set]]
[[!redirects irreducible closed sets]]