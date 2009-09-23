<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>

#Idea#

The ordinary [[Euclidean group]] of $\mathbb{R}^n$ is the group generated from the rigid translation action of $\mathbb{R}^n$ on itself and rotations about the origin.

The _super Euclidean group_ is analogously the [[supergroup]] of translations and rotations of the [[supermanifold]] $\mathbb{R}^{p|q}$.

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

