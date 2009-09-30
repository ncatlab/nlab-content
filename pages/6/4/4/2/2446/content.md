<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>

#Idea#

The ordinary [[Euclidean group]] of $\mathbb{R}^n$ is the group generated from the rigid translation action of $\mathbb{R}^n$ on itself and rotations about the origin.

The _super Euclidean group_ is analogously the [[supergroup]] of translations and rotations of the [[supermanifold]] $\mathbb{R}^{p|q}$.

Its [[super Lie algebra]] should be the [[super Poincare Lie algebra]] (up to the signature of the metric).

#Details#

> **incomplete** for the moment, to be finished off tomorrow

The following description of the super Euclidean group (once it is finished, and polished) is due to [[Stephan Stolz]] and [[Peter Teichner]].

The data needed to define the super Euclidean group is


1. $V$ a $d$-dimensional inner product space

1. a [[spinor representation]] $\Delta^*$ of $Spin(V)$

1. a $Spin(V)$-equivariant map

   $$
      \Gamma : \Delta^* \otimes_{\mathbb{C}}
       \Delta^* \to V \otimes_{\mathbb{R}} \mathbb{C}
   $$

where $Spin(V)$ is the [[Spin group]] (see [[Clifford algebra]] for the moment).

Here is the construction of $Eucl(\mathbb{R}^{d|\delta})$ for 

* $d = dim_{\mathbb{R}} V$

**remark** $\delta$ is a multiple of $2^{[\frac{d-1}{2}]}$

set

$$
  X = \Pi
  \left(
    \array{ V \times \Delta^* \\ \downarrow \\ V}
  \right)
  = 
  V \times \Pi \Delta^*
$$

is a [[complex supermanifold]] of dimension $(d|\delta)$

$$
  C^\infty(V \times \Pi \Delta^*)
  =
  C^\infty(V) \otimes 
  \wedge^\bullet \Delta
  = 
  C^\infty(V, \wedge^\bullet(\Delta))
$$

for $\delta = 1$ this is

$$
  \cdots = C^\infty(C, \wedge^\bullet \Delta)^{ev}
    \oplus
   C^\infty(C, \wedge^\bullet \Delta)^{odd}
$$

$$
  \cdots \simeq
    C^\infty(V) \oplus C^\infty(V, \wedge^\bullet \Delta)
$$

where the last factor is $\simeq C^\infty(V; \Delta) \simeq C^\infty(V, S^+)$ where $S^+$ is the [[spinor bundle]]

now define the multiplication 

$$
  (V \times \Pi \Delta^*)
  \times
  (V \times \Pi \Delta^*)
  \stackrel{\mu}{\to}
  (V \times \Pi \Delta^*)  
$$

by sayin what it does on sets of probes by $S$

$$
  (V \times \Pi \Delta^*)(S)
  \times
  (V \times \Pi \Delta^*)(S)
  \stackrel{\mu(S)}{\to}
  (V \times \Pi \Delta^*)(S)
$$

here on the left we have the sets of sections

$$
  C^\infty(S)^{ev} \otimes V
  \times
  C^\infty(S)^{ev} \otimes \Delta^*
$$

so we can map these as

$$
  ((v_1, \theta_1),
   (v_2, \theta_2)
  )
  \mapsto
  (v_1 + v_2 + \Gamma(\theta_1 \otimes \theta_2), 
   \theta_1 + \theta_2)
$$


**Remark**

if the data $(V, \Delta^*, \Gamma)$ and 
$(V', (\Delta^*)', \Gamma')$ is [[isomorphism|isomorphic]] we get compatible notions of structures

But if $d = 0,1,2$ and $\delta = 1$ then there is a _unique_ such triple with non-degenerate pairing $\Gamma$ up to isomorphism.

**Definition**

The structure of a  **[[Euclidean supermanifold]]** on a $(d|\delta)$-dimensional [[supermanifold]] $Y$ is a $(V \times \Pi \Delta^*, End(V, \Delta^*, \Gamma))$-structure. See there for details.

#Examples#


recall the [[Clifford algebra]] table:

$$
  \array{
      d & Cl(\mathbb{R}^d)^{ev} & Spin(\mathbb{R}^d)
      \\
      \\
      1 & \mathbb{R} & \{\pm 1\}
      \\
      2 & (\mathbb{R} 1 \oplus \mathbb{R} e_1 e_2, e_i^2 = 1) \simeq \mathbb{C} & S^1
  }
$$

the group structure on $V \times \Pi \Delta^*$ is that of the "translations" and "rotations"

it will be defined on [[generalized element]]s with domain $S$ by maps of sets

$$
  \mu:
  (V \times \Pi \Delta^*)(S)
  \times
  (V \times \Pi \Delta^*)(S)
  \to
  (V \times \Pi \Delta^*)(S)
$$

$$
  (v_1, \theta_1) , (v_2, \theta_2)
  \mapsto
  (v_1+ v_2 + \Gamma(\theta_1 \otimes \theta_2),
  \theta_1 + \theta_2)
$$
 
## $d = 1$

$\Delta^* = \mathbb{C}$

$$
  \Gamma : \Delta^* \otimes \Delta^* \to V \otimes_{\mathbb{R}} \mathbb{C}
$$

$$
  \mathbb{C} \otimes \mathbb{C}
  \to
  \mathbb{R} \otimes_{\mathbb{R}} \mathbb{C}
$$

$$
  1 \otimes 1 \mapsto 1 \otimes 1
$$

so here this is the [[supergroup|super translation group]].

## $d = 2$

$\Delta^* = \mathbb{C}$

$$
  u \in S^1 \simeq U(1) \simeq Spin(\mathbb{R}^2)
$$


$$
  \Delta^* \otimes_{\mathbb{C}}
  \Delta^*
  \stackrel{\Gamma}{\to}
  \mathbb{R}^2 \otimes \mathbb{R}
  \simeq \mathbb{C} \oplus \mathbb{C}
$$

the first map is multiplication by $u^{-1}$ and then the isomorphism on the right sends

$$
  (x,y)\otimes 1 \mapsto (z, \bar z)
$$

where $z = x + i y$

translation group $V \times \Pi \Delta^* \simeq \mathbb{R}^{2|1}$


multiplication on $S$-elements

$$
  \mathbb{R}^{2|1}(S) \times
  \mathbb{R}^{2|1}(S)
  \to 
  \mathbb{R}^{2|1}(S)
$$

given by

$$
  (z_1,\bar z_1, \theta_1),
  (z_2,\bar z_2, \theta_2)
  \mapsto
  (z_1 + z_2, \bar z_1 + \bar z_2 + \theta_1 \theta_2, \theta_1 + \theta_2)  
$$

