
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _0-sphere_ $S^0$ is the [[n-sphere]] for $n = 0$: The [[disjoint union]] of two [[points]],

$$
  S^0 \;\;\simeq\;\; \ast \sqcup \ast
  \,.
$$

This definition (even if possibly not be familiar from standard texts of [[point-set topology]]) is certainly justified by the fact that the 2-element set is clearly:

* the [[unit sphere]] inside the [[real line]] $\mathbb{R}^1$,

  and as such part of the general pattern that the [[n-sphere]] is the [[unit sphere]] inside $\mathbb{R}^{n+1}$;

* the [[topological space]]/[[homotopy type]] whose [[suspension]] is equivalently the [[1-sphere]] (the [[circle]]):

  $$
    S^1 \,\simeq\, \mathrm{S} S^0
    \,,
  $$

  thus being the base case of the [[induction|inductive]] definition of the [[n-spheres|$n$-spheres]]:

  $$
    S^{n+1} 
      \;\simeq\; 
    \mathrm{S} S^{n}
      \;\simeq\;
    \mathrm{S} \mathrm{S} S^{n-1}
      \;\simeq\;
    \mathrm{S}^{n+1} S^0
    \,.
  $$

In fact, with [[suspension]]  $\mathrm{S}X$ understood as the [[homotopy pushout]] of the [[terminal object|terminal]] [[map]] $X \to \ast$ along itself, one has also

$$
  S^0 \;\coloneqq\; \mathrm{S} S^{-1}
$$

for $S^{-1} \,\coloneqq\, \varnothing$ the [[empty set]].

These spheres of degenerate dimensions play an imprtant role in [[homotopy theory]], see for instance the [[cofibrantly generated model category|generating cofibrations]] in the [[classical model structure on topological spaces]] ([here](classical+model+structure+on+topological+spaces#TopologicalGeneratingCofibrations)).



Of course, the underlying object of $S^0$, simple as it is, plays various other roles, too:

* in [[topos theory]], the two element set plays the role of the [[subobject classifier]] among [[Sets]];

* in [[formal logic]] this is also known as the [[classical mathematics|classical]] *[[boolean domain]]*: the [[set]] of [[classical mathematics|classical]] [[truth values]];

  and in [[data type|data]]-[[type theory]] one also speaks of the [[type]] $Bit$ of [[bits]];

* that same type regarded in [[homotopy type theory]] again plays the role of the $0$-sphere in the sense of *[[sphere types]]* -- see also at *[boolean domain -- In HoTT](boolean+domain#InHomotopyTypeTheory)*;

* in [[category theory]] the [[disjoint union]] of two copies of the [[terminal object]] (be it the 2-element [[set]] or the corresponding [[discrete category]], etc.) is often denoted "$\mathbf{2}$"

  (cf. e.g. at *[[Stone duality]]*).



## Related concepts

* [[1-sphere]]

* [[2-sphere]]

* [[4-sphere]]

* [[7-sphere]]

[[!redirects 0-spheres]]

[[!redirects (-1)-sphere]]
[[!redirects (-1)-spheres]]


