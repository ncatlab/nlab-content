In [[representation theory]], **Frobenius reciprocity** (sometimes _Frobenious_) is the statement that the [[induction functor]] for [[group representation|representations of groups]] (or in some other [[algebraic categories]]) is [[left adjoint]] to the [[restriction]] functor.

In [[category theory]], Frobenius reciprocity is a condition on the [[inverse image|inverse]] and [[direct image]] maps in a [[hyperdoctrine]].  In general, suppose $S$ is a category and $P \colon S^{op} \to Cat$ is an $S$-[[indexed category]] such that each category $S X$ is [[cartesian closed]] and each functor $f^* = S f$ has a left adjoint $\exists_f$ (also written $f_!$).  Then $P$ is said to satisfy Frobenius reciprocity, or the Frobenius condition, if each of the left adjoints $\exists_f$ preserves exponentials, that is if $\exists_f(B^A) \cong \exists_f(B)^{\exists_f(A)}$.

This condition is equivalent to asking that, for each $f\colon X \to Y$ in $S$ and each $A \in S X$ and $B \in S Y$, the canonical morphism $\exists_f(A \times f^*B) \to (\exists_f A) \times B$ is an [[isomorphism]].  This clearly makes sense if the categories $S X$ are [[cartesian category|cartesian]] but not [[closed category|closed]], and is the usual formulation found in the literature.


[[!redirects Frobenius reciprocity]]
[[!redirects Frobenious reciprocity]]
