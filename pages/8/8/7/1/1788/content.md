
Let's denote [[cyclic groups]] for $n \in \mathbb{N}$ by
$$
  \mathbb{Z}_{n}
  \;\coloneqq\;
  \left\{
  \begin{array}{lcl}
    \mathbb{Z} &\vert& n = 0
    \\
    \mathbb{Z}/(n) &\vert& \text{otherwise}
  \end{array}
  \right.
$$

Observe that the second [[group cohomology]] of the [[free abelian group]] $\mathbb{Z}^2$ is
$$
  \begin{array}{ccl}
    H^2_{Grp}(\mathbb{Z}^2;\, \mathbb{Z}_n)
    &\simeq&
    H^2(B \mathbb{Z}^2;\, \mathbb{Z}_n)    
    \\
    &\simeq&
    H^2(T^2;\, \mathbb{Z}_n)    
    \\
    &\simeq&
    H^2(S^1_a \vee S^1_b \vee S^2;\, \mathbb{Z}_n)    
    \\
    &\simeq&
    H^2(S^2;\, \mathbb{Z}_n)    
    \\
    &\simeq&
    \mathbb{Z}_n
  \end{array}
$$
where we used, in order of the appearance:

1. that [[group cohomology]] is [[ordinary cohomology]] of the domain group's [[classifying space]];

1. that the [[classifying space]] of the [[integers]] is the [[circle]] and that this respects [[Cartesian products]];

1. that the [[stable homotopy type]] of the [[2-torus]] is the [[wedge sum]] of two [[circles]] with a [[2-sphere]] (see [there](torus#AsAHomotopyType)).

The generator of this [[cohomology group]] must be the [[group cohomology|group 2-cocycle]] 

$$
  \alpha \,\in\, H^2_{Grp}\big(
    \mathbb{Z}^2
    ;\,
    \mathbb{Z}_n
  \big)
$$

given by

$$
  \begin{array}{ccc}
    \mathbb{Z}^2 
    \times
    \mathbb{Z}^2
    &\xrightarrow{\; \alpha \;}&
    \mathbb{Z}_{n}
    \\
    \big(
      (a,b), (a',b')
    \big)
    &\mapsto&
    [a b']
  \end{array}
$$

(whose cocycle condition
$
  [a b'] + [(a+a')b'']
  =
  [a(b'+b'')] + [a' b'']
$
is evidently satisfied due to the [[distributive law]] in the [[ring]] $\mathbb{Z}$)

whose [corresponding](group+extension#CentralExtensionClassificationByGroupCohomology) [[central extension]]
$$
  1 
    \to 
  \mathbb{Z}_n
    \longrightarrow
  H
    \longrightarrow
  \mathbb{Z}^2
    \to
  1
$$
is, for $n = 0$, the [[subgroup]] of the [[simply-connected topological space|simply-connected]] version of the [[Heisenberg group]] of $\mathbb{R}^2$ obtained by restriction along the canonical inclusion $\mathbb{Z}^2 \hookrightarrow \mathbb{R}^2$ (an "integer Heisenberg group", cf. [Lee & Packer 1996 (1.2)](Heisenberg+group#LeePacker96)).


