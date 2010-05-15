<div class="rightHandSide toc">
[[!include monoidal categories - contents]]
</div>

An object $A$ in a [[monoidal category]] $C$ is **dualizable** if it has an [[adjunction|adjoint]] when regarded as a 1-cell in the one-object [[bicategory]] $\mathbf{B}C$ corresponding to $C$.  Its adjoint in $\mathbf{B}C$ is called its **dual** in $C$ and often written as $A^*$.

If $C$ is [[braided monoidal category|braided]] then left and right adjoints in $\mathbf{B}C$ are equivalent; otherwise one speaks of $A$ being **left dualizable** or **right dualizable**.  Unfortunately, conventions on left and right vary and sometimes contradict their use for adjoints.  But if we define right duals to be the same as right adjoints in $\mathbf{B}C$, then a right dual of $A$ is an object $A^*$ equipped with a **unit** (or *coevaluation*)
$$i: I \to A^* \otimes A $$
and **counit** (or *evaluation*)
$$e : A \otimes A^* \to I $$
satisfying the 'triangle identities' familiar from the concept of [[adjunction]].

If every object of $C$ has a left and right dual, then $C$ is called a [[rigid monoidal category]] or an [[autonomous monoidal category]].  If it is additionally symmetric, it is called a [[compact closed category]].  See [[category with duals]] for more discussion.

Dualizable objects also support a good abstract notion of [[trace]].


[[!redirects dual object]]
[[!redirects dual objects]]
[[!redirects dualizable object]]
[[!redirects dualizable objects]]
[[!redirects dualisable object]]
[[!redirects dualisable objects]]