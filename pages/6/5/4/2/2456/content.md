A **(global) choice operator** is structure included in some [[foundations]] of [[mathematics]] which provides a uniform way to choose an element of every [[inhabited set|inhabited]] [[set]] or [[class]].

In Hilbert's original formulation, for any property $P(x)$ we can form a term $\epsilon x.P(x)$ such that
$$\exists x.P(x) \;\Rightarrow\; P\big(\epsilon x.P(x)\big).$$
In other words, if $P$ holds of anything at all, then it holds of the particular term $\epsilon x.P(x)$.  A similar operator was used by [[Bourbaki]] and appears in [[FMathL]].

+--{: .query}
[[Mike Shulman]]: I think this was Hilbert's original version, but history is not my strong point; maybe someone can correct?
=--

One use of the choice operator is to eliminate undesirable details of implementation.  For example, if $P(x)$ is "$x$ is a Dedekind-complete totally ordered field," then we can define "the real numbers" to be $\epsilon x.P(x)$.  Any of the numerous constructions of the [[real numbers]] can then be used to show that there exists an $x$ such that $P(x)$, after which point we can discard whichever explicit construction and work only with $\mathbb{R}=\epsilon x.P(x)$.  This way we can no longer assert that real numbers (elements of $\mathbb{R}$) *are* Cauchy sequences, or Dedekind cuts, or anything in particular, since the axioms provide no rules about how $\epsilon x.P(x)$ must be chosen other than that it must satisfy $P$.  So $\mathbb{R}$ *might* consist of Cauchy sequences, or Dedekind cuts, or any other way to construct the reals, but we have no way of knowing, and thus we cannot make use of any such definition in a proof about $\mathbb{R}$; we are forced to use only its formal properties.

In many cases, the assumption of a global choice operator implies the [[axiom of choice]], since for any family $(A_u)$ of inhabited sets, a choice function is given by $u\mapsto (\epsilon x.x\in A_u)$.  In fact, in the form given above it often implies the stronger *global* axiom of choice, which applies to proper classes as well as sets.  However, in some foundations it seems to be possible to avoid this conclusion (if it is unwanted) by not requiring the choice operator to be extensional, i.e. it may not be the case that $A=B$ implies $\epsilon x.A = \epsilon x.B$.

+--{: .query}
[[Mike Shulman]]: Is there a formal statement in some formal system along the lines of "a non-extensional choice operator does not imply AC"?
=--

Like the [[axiom of choice]], the existence of a global choice operator is consistent with the other axioms of most foundations.  For example, in ZF, the [[constructible universe]] (which models $ZF + (V=L)$, the [[axiom of constructibility]]) admits a natural [[well-ordering]] of the entire universe, giving rise to a naturally defined global choice operator (namely, $\epsilon x.P$ = the smallest $x$ such that $P$ in the global well-ordering).
