+-- {: .un_theorem }
###### Main theorem of classical Galois theory

Let $K \subset L$ be a [Galois extension](#GaloisExtension) of fields with [Galois group](#GaloisGroup) $G$. Then the intermediate fields of $K \subset L$ correspond bijectively to the closed subgroups of $G$.

More precisely, the maps 

$$
  \{E | E\;is\;a\;subfield\;of\;L\;containing\;K\}
  \stackrel{\overset{\phi}{\to}}{\underset{\psi}{\leftarrow}}
   \{H|H\;is\;a\;closed\;subgroup\;of\;G\}
$$

defined by

$$
  \phi(E) = Aut_E(L)
$$

and

$$
  \psi(H) = L^H
$$

are bijective and inverse to each other. This correspondence reverses the inclusion relation: $K$ corresponds to $G$ and $L$ to $\{id_L\}$.

If $E$ corresponds to $H$, then we have

1. $K \subset E$ is finite precisely if $H$ is open (in the profinite topology on $G$)

   $[E:K] \simeq index[G:K]$ if $H$ is open;

1. $E \subset L$ is Galois with $Gal(L/E) \simeq H$ (as [[topological group]]s);

1. for every $\sigma \in G$ we have that $\sigma[E]$ corresponds to $\sigma H \sigma^{-1}$;

1. $L \subset E$ is Galois precisely if $H$ is a [[normal subgroup]] of $G$;

   $Gal(E/K) \simeq G/H$ (as [[topological group]]s) if $K \subset E$ is Galois. 

=--

This appears for instance as [Lenstra, theorem 2.3](#Lenstra).

This suggests that more fundamental than the subgroups of a Galois group $G$ are its quotients by subgroups, which can be identified with transitive $G$-sets.  This naturally raises the question of what corresponds to non-transitive $G$-sets.

category: Galois theory