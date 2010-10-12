This entry lists examples for pairs of [[adjoint functor]]s. 

For examples of the other [[universal construction]]s see 

* [[limits and colimits by example]]

* [[examples of Kan extensions]].

#Free/forgetful functors#

The classical examples of pairs of [[adjoint functor]]s are $L \dashv R$ where the right adjoint $R : C' \to C$ [[stuff, structure, property|forgets structure]] in that it is a [[faithful functor]]. In these case the left adjoint $L : C \to C'$ usually is the [[free functor]] that "adds structure freely". 

In fact, one usually turns this around and _defines_ the free $C'$-structure on an object $c$ of $C$ as the image of that object under the left adjoint (if it exists) to the functor $R : C' \to C$ that forgets this structure.

For instance

* forgetful right adjoint $R:$ [[Grp]] $\to$ [[Set]] forgets the group structure on a group and just remembers the underlying set -- the left adjoint  $L : Set \to Grp$ sends each set to the [free group](http://en.wikipedia.org/wiki/Free_group) over it.

#Nerves and realization#

For $C$ a category equipped with cosimplicial objects $\Delta_C : \Delta \to C$ and [[copower|tensored]] over $Set$;

$N_D : C \to Set^{\Delta^{op}}$

[[nerve]]

$$
  |-|_C : Set^{\Delta^{op}} \to C
$$


$$
  N_D(c) : \Delta^{op} \stackrel{\Delta_C^{op}}{\to} C^{op} \stackrel{C(-,C)}{\to} Set
$$


[[geometric realization|realization]]

$$
  |-|_C : Set^{\Delta^{op}} \to C
$$

$$
  |S_\bullet|_C = \int^{[n] \in \Delta} S_n \cdot \Delta_C[n]
$$

adjunction $|-|_C \dashv N_D$


