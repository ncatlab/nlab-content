
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[dependent type theory]], given a type $A$, a type $T$ is a **$A$-null type** if the function 

$$\lambda x:T.\lambda y:A.x:T \to (A \to T)$$

is an [[equivalence of types]]. 

More generally, given a type $A$ and a type family $B(a)$ indexed by $a:A$, a type $T$ is a **$B$-null type** if the function 

$$\lambda x:T.\lambda y:B(a).x:T \to (B(a) \to T)$$

is an [[equivalence of types]] for all $a:A$. 

## Examples

* Every type is $A$-null if the type $A$ is a [[contractible type]]. 

* Every [[contractible type]] is [[empty set|$\emptyset$]]-null. 

* Every [[mere proposition]] is [[boolean]]-null. 

* Every [[h-set]] is [[circle type|$S^1$]]-null. 

## Related concepts

* [[localization of a type]]

* [[axiom of cohesion]]

* [[local object]]

## References

* {#RSS20} [[Egbert Rijke]], [[Mike Shulman]], [[Bas Spitters]], *Modalities in homotopy type theory*,  Logical Methods in Computer Science, **16** 1 (2020) &lbrack;[arXiv:1706.07526](https://arxiv.org/abs/1706.07526), [episciences:6015](https://lmcs.episciences.org/6015), <a href="https://doi.org/10.23638/LMCS-16(1:2)2020">doi:10.23638/LMCS-16(1:2)2020</a>&rbrack;

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects null type]]
[[!redirects null types]]