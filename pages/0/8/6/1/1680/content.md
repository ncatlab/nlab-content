As a [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[infinity-groupoid]] the _Eilenberg--Mac Lane_ [[spectrum]] is the integers

$$
  E_{EM} := \mathbb{Z}
  \,.
$$

Here the set $\mathbb{Z}$ is regarded as a [[discrete category|discrete groupoid]] (one object per integer, no nontrivial morphisms) whose symmetric monoidal structure is that given by the additve group structure on the integers.

Accordingly, the infinite tower of suspensions induced by this is the sequence of [[infinity-groupoid]]s

$$
  \mathbb{Z}, \mathbf{B} \mathbb{Z}, \mathbf{B}^2 \mathbb{Z}, \mathbf{B}^3 \mathbb{Z}, \cdots
$$

that in this case happen to be [[strict omega-groupoid]]s. The [[strict omega-groupoid]] $\mathbf{B}^n \mathbb{Z}$ has only [[identity]] $k$-morphisms for all $k$, except for $k = n$, where $\mathrm{Mor}_n(\mathbf{B}^n \mathbb{Z}) = \mathbb{Z}$ are the endomorphisms of the unique identity $(n-1)$-morphism. 

The strict $\infty$-grouopoid $\mathbf{B}^n \mathbb{Z}$ is the one given under the [[Dold-Kan correspondence]] by the [[crossed complex]] of groupoids that is trivial everywhere and has the group $\mathbb{Z}$ in degree $n$.

$$
  \begin{aligned}
    [\mathbf{B}^n \mathbb{Z}] &=
     (  \cdots \to [\mathbf{B}^n\mathbb{Z}]_{n+1} \to [\mathbf{B}^n\mathbb{Z}]_{n} \to 
     [\mathbf{B}^n\mathbb{Z}]_{n-1} \cdots \to [\mathbf{B}^n\mathbb{Z}]_{1} \stackrel{\to}{\to} [\mathbf{B}^n\mathbb{Z}]_{0})
      \\ &=
    (  \cdots \to {*} \to \mathbb{Z} \to 
    {*} \cdots \to {*} \stackrel{\to}{\to} {*})
  \end{aligned}
  \,.
$$

Under the [[Quillen equivalence]]

$$
  |-| : \infty Grpds \to Top
$$

between [[infinity-groupoid]]s and [[topological space]]s this sequence of suspensions of $\mathbb{Z}$ maps to the sequence of [[Eilenberg–Mac Lane space]]s

$$
  |\mathbf{B}^n \mathbb{Z}|
  \simeq
  K(\mathbb{Z}, n)
$$

that give the Eilenberg--Mac Lane spectrum 

$$
  (E_n) := (K(\mathbb{Z},n))
$$

its name.


[[!redirects Eilenberg-MacLane spectrum]]
[[!redirects Eilenberg--MacLane spectrum]]
[[!redirects Eilenberg--Mac Lane spectrum]]
[[!redirects Eilenberg–MacLane spectrum]]
[[!redirects Eilenberg–Mac Lane spectrum]]
[[!redirects Eilenberg-MacLane spectra]]
[[!redirects Eilenberg-Mac Lane spectra]]
[[!redirects Eilenberg--MacLane spectra]]
[[!redirects Eilenberg--Mac Lane spectra]]
[[!redirects Eilenberg–MacLane spectra]]
[[!redirects Eilenberg–Mac Lane spectra]]