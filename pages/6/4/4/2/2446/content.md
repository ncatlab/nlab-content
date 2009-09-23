<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>

#Idea#

the [[super Lie group]] that generalizes the [[Euclidean group]] or [[Galileo group]].

#Details#

Construction of $Eucl(\mathbb{R}^{d|\delta})$ for 

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

