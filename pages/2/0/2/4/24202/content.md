
In classical [[algebraic topology]] we have four [[Hopf fibrations]] (of spheres):

1. $S^0 \hookrightarrow S^1 \to S^1$ The [[real Hopf fibration]]
2. $S^1 \hookrightarrow S^3 \to S^2$ The usual [[complex Hopf fibration]]
3. $S^3 \hookrightarrow S^7 \to S^4$ The [[quaternionic Hopf fibration]]
4. $S^7 \hookrightarrow S^15 \to S^8$ The [[octonionic Hopf fibration]]

These can be constructed in HoTT as part of a more general construction:

A [[H-space]] structure on a pointed type $A$ gives a fibration over $\Sigma A$ via the hopf construction. This fibration can be written classically as: $A \to A\ast A \to \Sigma A$ where $A\ast A$ is the join of $A$ and $A$. This is all done in the HoTT book. Note that $\Sigma A$ can be written as a homotopy pushout $\Sigma A := \mathbf 1 \sqcup^A \mathbf 1 $, and there is a lemma in the HoTT book allowing you to construct a fibration on a pushout (the equivalence $A \to A$ needed is simply the multiplication from the H-space $\mu(a,-)$).

Thus the problem of constructing a hopf fibration reduces to finding a H-space structure on the [[spheres]]: the $S^1$, $S^3$ and $S^7$.

* The space $S^0=\mathbf 2(\equiv Bool)$ is not [[connected]] so we cannot perform the construction from the book on it. However it is very easy to construct a [[family]] $S^1 \to \mathcal{U}$ with fiber $Bool$ by induction on $S^1$.  (Note: loop maps to $ua(neg)$ where $neg$ is the equivalence of negation and $ua$ is the [[univalence axiom]].

* For $S^1$ [[Peter Lumsdaine]] gave the construction in 2012 and [[Guillaume Brunerie]] proved it was correct in 2013. By [[induction]] on the [[circle]] we can define the multiplication: $\mu(base)\equiv id_{S^1}$, and $ap_\mu(loop)\equiv funext(h)$ where $h : (x : S^1) \to (x = x)$ is also defined by [[circle]] [[induction]]: $h(base) = loop$ and $ap_h(loop) = refl$. $funext$ denotes [[functional extensionality]].

* For $S^3$ [Buchholtz-Rijke 16](#BuchholtzRijke16) solved this through a [[homotopy theory|homotopy  theoretic]] version of the [[Cayley-Dickson construction]]. This has been formalised in Lean.

* For $S^7$ this is still an open problem.

It is still an open problem to show that these are the only spheres to have a H-space structure. This would be done by showing these are the only spheres with hopf invariant $1$ which has been defined in [On the homotopy groups of spheres in homotopy type theory](https://arxiv.org/abs/1606.05916).

## References

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* {#BuchholtzRijke16} [[nLab:Ulrik Buchholtz]], [[nLab:Egbert Rijke]], _The Cayley-Dickson Construction in Homotopy Type Theory_ ([arXiv:1610.01134](https://arxiv.org/abs/1610.01134)) 


category: homotopy theory