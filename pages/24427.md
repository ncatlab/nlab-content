## Idea

A graded bimonoid is like a [[bimonoid]] but graded, as a [[graded monoid]]. We don't look as an object $A$ but as a [[graded object]] $(A_{n})_{n \ge 0}$. The multiplication, comultiplication, unit and counit are defined as morphisms which respect the grading.

## Definition

A graded bimonoid in a [[CMon-enriched symmetric monoidal category]] is given by a family $(A_{n})_{n \ge 0}$ of objects, a family $(\nabla_{n,p}:A_{n} \otimes A_{p} \rightarrow A_{n+p})_{n,p \ge 0}$ of morphisms, a family $(\Delta_{n,p}:A_{n+p} \rightarrow A_{n} \otimes A_{p})_{n,p \ge 0}$ of morphisms, a morphism $\eta:I \rightarrow A_{0}$ and a morphism $\epsilon:A_{0} \rightarrow I$ which verify some coherences:

* $((A_{n})_{n \ge 0},(\nabla_{n,p})_{n,p \ge 0}, \eta)$ is a [[graded monoid]]
* $((A_{n})_{n \ge 0},(\Delta_{n,p})_{n,p \ge 0}), \epsilon)$ is a [[graded comonoid]]
* Compatibility multiplication/comultiplication:
* Compatibility unit/multiplication:
* Compatibility counit/comultiplication:
* Compatibility unit/counit:

## Related concepts

[[bimonoid]]

[[symmetric powers in symmetric monoidal categories enriched over modules over a (Q plus)-algebra]]

[[graded codifferential category]]

[[Hasse-Schmidt derivative]]