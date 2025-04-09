
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[simplicial type theory]], a **covariant type family** over $A$ is a [[type family]] $x:A \vdash B(x)$ such that for all elements $x:A$, $y:A$, $f:\mathrm{hom}_A(x, y)$, and $u:B(x)$, [[uniqueness quantifier|there exists a unique]] element $v:B(y)$ with an morphism of the [[heterogeneous hom-type]] $\mathrm{hhom}_{B(f)}(u, v)$

$$\mathrm{isCovariant}(t:A.B(t)) \coloneqq \prod_{x:A} \prod_{y:A} \prod_{f:\mathrm{hom}_A(x, y)} \prod_{u:B(x)} \exists!v:B(y).\mathrm{hhom}_{B(f)}(u, v)$$

## Properties

\begin{theorem}
Given a [[Segal type]] $A$, a type family $x:A \vdash B(x)$ is a covariant type family if and only if for all elements $f:\mathrm{hom}_A(x, y)$, and $u:B(x)$, there is a unique lifting of $f$ that starts at $u$. 
\end{theorem}

## Related concepts

* [[hom type]]

* [[directed univalence]]

* [[contravariant type family]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))