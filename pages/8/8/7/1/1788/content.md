+-- {: .num_prop}
###### Proposition

Let $A$ be a finite dimensional local Artin $k$-algebra, i.e. $A \simeq_k k \oplus n_A$. with $(n_A)^s = 0$ for some $s \in \mathbb{N}$.

Then every [[projective module]] $N$ over $A$ is a [[free module]].

=--

+-- {: .proof}
###### Proof that dualizes

First consider the projection

$$
  N \longrightarrow N/(n_A N)
$$

and choose a splitting as $k$ vector space

$$
  N \;\simeq_k\; V \oplus n_A N
  \,.
$$

Hence we get a surjective (right??) homomorphism of $A$-modules 

$$
  A \otimes_K V \longrightarrow N
$$

by setting

$$
  (a,v) \mapsto a v
  \,.
$$

By the fact that $N$ is assumed to be projective, there is then a homomorphism $\phi$ making the following diagram commute:

$$
  \array{
     && A \otimes V
     \\
     & {}^{\mathllap{\phi}}\nearrow & \downarrow^{\mathrlap{epi}}
     \\
     N &\underset{id}{\longrightarrow}& N
  }
$$

Observe that $\phi$ is also surjective (right??): All of $V \simeq k \otimes_k V \hookrightarrow A \otimes_K V$ has to be in the image, for the diagram to commute,  and so for $\hat v$ a preimage of some $v$, then $a \hat v$ maps to $(a, \hat v)$, by the homomorphism property.

Hence we have factored the identity by two epimorphisms, and so both of these need to be isomorphisms, hence

$$
  N \simeq A \otimes V
$$


=--
