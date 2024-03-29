
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--



A (binary) [[relation]] $\sim$ on a set $A$ is __antisymmetric__ if any two elements that are related in both orders are [[equality|equal]]:
$$\forall (x, y: A),\; x \sim y \;\wedge\; y \sim x \;\Rightarrow\; x = y$$

In the language of the $2$-poset-with-duals [[Rel]] of sets and relations, a relation $R: A \to A$ is __antisymmetric__ if its intersection with its reverse is contained in the identity relation on $A$:
$$R \cap R^{op} \subseteq \id_A$$
If an antisymmetric relation is also [[reflexive relation|reflexive]] (as most are in practice), then this containment becomes an equality.

## See also ##

* [[internal antisymmetric relation]]

[[!redirects antisymmetry]]
[[!redirects antisymmetric]]
[[!redirects antisymmetric relations]]