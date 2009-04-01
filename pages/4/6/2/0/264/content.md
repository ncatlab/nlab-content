#Definition#

Given a [[category with weak equivalences]] (such as a [[model category]]), its __homotopy category__ $Ho(C)$ is the [[category]] which is universal with the property that there is a [[functor]]

$$
 p :  C \to Ho(C)
$$

which sends every weak equivalence in $C$ to an [[isomorphism]] in $Ho(C)$, i.e. 

$$
  Ho_C := W^{-1}C
$$

is the [[localization]] of $C$ at the collection $W$ of weak equivalences.

# Remarks #



* As described at [[localization]], in general, the morphisms of $Ho(C)$ must be constructed using zigzags of morphisms in $C$ in which the backwards-pointing arrows are weak equivalences.  This means that in general, $Ho(C)$ need not be [[locally small category|locally small]] even if $C$ is.  However, in many cases (such as any [[model category]]) there is a more direct description of the morphisms in $Ho(C)$ as [[homotopy]] classes of maps in $C$ between suitably "good" (fibrant and cofibrant) objects.

* In classical topology, _the_ homotopy category refers to the homotopy category of $Top$ with weak homotopy equivalences, which can equivalently be constructed as the category of homotopy classes of maps between [[CW complex|CW complexes]].

* In [[2-limit|2-categorical terms]], the homotopy category $Ho(C)$ is the _coinverter_ of the canonical 2-cell
$$\array{& \to \\ W & \Downarrow & C\\ & \to}$$
where $W$ is the category whose objects are morphisms in $W$ and whose morphisms are commutative squares in $C$.
