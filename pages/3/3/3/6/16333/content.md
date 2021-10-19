## Idea

The typing rules for [[simply typed lambda calculus]]

$$
\frac{\Gamma \vdash t: \sigma\to \tau \quad \Gamma \vdash u:\sigma}{\Gamma \vdash t(u) : \tau}
\qquad
\frac{\Gamma,x:\sigma \vdash t:\tau}{\Gamma \vdash \lambda x.t : \sigma \to \tau}
$$

can be seen as defining a family of sets of [[terms]], indexed by context and by type, while the computation rule $(\lambda x.t)u = t[u/x]$ can be seen as considering the [[quotient]] of this family of sets by the $\beta$ axiom (defined in terms of the [[substitution]] operation).

But suppose that we collapse all of the types into one "universal" type $U$, so that terms need no longer be simply-typed:

$$
\frac{\Gamma \vdash t: U \quad \Gamma \vdash u: U}{\Gamma \vdash t(u) : U}
\qquad
\frac{\Gamma,x: U \vdash t: U}{\Gamma \vdash \lambda x.t:U}
$$

Now, these rules can be seen as defining a family of sets of terms indexed only by the _length_ of the context (corresponding to the number of free variables).  Together with the action of substitution and after quotienting by the $\beta$ axiom, this family of sets can then be considered as a cartesian [[operad]] defining an [[algebraic theory]] of [[pure lambda calculus]] terms.

## Definition

Let $L : Fin \to Set$ be a cartesian operad (i.e., essentially a [[Lawvere theory]]).  A **semi-closed structure** ([Hyland](#Hyland13)) on $L$ is a family of maps 

$$\rho : L(n) \to L(n+1) \quad \lambda : L(n+1) \to L(n)$$
$$\rho \circ \lambda = id$$

natural in $n$, which are compatible with the operadic structure in an appropriate sense.  A **lambda theory** is a cartesian operad equiped with a semi-closed structure.

## Scott's representation theorem

Any lambda theory is isomorphic to the endomorphism lambda theory of a [[reflexive object]] in a [[cartesian closed category]].  In particular, let $L$ be a lambda theory, then for the associated reflexive object $U^U \lhd U$ we simply take $U = L$ itself, seen as an object of the [[presheaf]] category $[Fin,Set]$ together with its associated ccc structure (see [[closed monoidal structure on presheaves]]).  We have that the exponential $U^U$ is isomorphic to $L(-+1)$, and thus a retract of $U$ by the semi-closed structure of $L$.  Moreover, we have that $[Fin,Set](U^n,U) \cong L(n)$ naturally in $n$.

## Related concepts

* [[reflexive object]]

## References


* {#Hyland13} [[Martin Hyland]]. _Classical lambda calculus in modern dress_ Mathematical Structures in Computer Science, 27(5) (2017) 762-781. doi:[10.1017/S0960129515000377](https://doi.org/10.1017/S0960129515000377). [arxiv:1211.5762](http://arxiv.org/abs/1211.5762)
