
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

In [[simplicial homotopy type theory]], given a [[type]] $A$ and a [[type family]] 
$$x:A \vdash B(x) \; \mathrm{type}$$ 
let us define the type family 
$$x:A, y:A, f:\mathrm{hom}_A(x, y), u:B(x), v:B(y) \vdash \mathrm{hom}_{B(f)}(u, v) \; \mathrm{type}$$
as 
$$\mathrm{hom}_{B(f)}(u, v) \coloneqq \left\langle\prod_{t:\mathbb{2}} C(f(t)) \vert_{[u,v]}^{\partial \Delta^1} \right\rangle$$
where $\mathbb{2}$ is the directed interval primitive, $\Delta^1$ is the $1$-simplex probe shape, and $\partial \Delta^1$ is its boundary.

Then a **contravariant type family** over $A$ is a [[type family]] $x:A \vdash B(x) \; \mathrm{type}$ such that given elements $x:A$, $y:A$, $f:\mathrm{hom}_A(x, y)$, and $v:B(y)$, the type
$$\sum_{u:B(x)} \mathrm{hom}_{B(f)}(u, v)$$
is a [[contractible type]]. 

## Related concepts

* [[hom type]]

* [[covariant type family]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$