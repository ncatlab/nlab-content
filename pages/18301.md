+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
One wants an equivalent and purely [[semantics|semantic]] characterization of [[quantifier elimination]].

A [[first-order theory|theory]] $T$ is substructure complete if after fixing a _substructure_, the theory of the [[elementary class]] of all $T$-models into which that substructure embeds is _complete_.

## Definition

+-- {: .num_defn}
###### Definition

A [[first-order theory]] $T$ in a language $\mathcal{L}$ is **substructure complete** if for any $M \in \mathbf{Mod}(T)$ and any $\mathcal{L}$-[[first-order structure|substructure]] $A \hookrightarrow M,$ the theory $T_{\mathsf{Diag}(A)}$ (expansion by $A$'s [[quantifier-free diagram]])---whose models are precisely those models $N \in \mathbf{Mod}(T)$ such that there exists an embedding of $\mathcal{L}$-structures $A \hookrightarrow N$---is complete.

=--

## Equivalence with quantifier elimination

+-- {: .num_theorem #QEiffsubstructurecomplete}
###### Theorem

$T$ [[quantifier elimination|eliminates quantifiers]] if and only if $T$ is substructure-complete.

=--

+-- {: .proof}
###### Proof

$(\Rightarrow)$ Suppose $T$ eliminates quantifiers. Fix a substructure $A$. Since quantifier-free sentences are automatically transferred by embeddings (whereas without the additional property of quantifier-freeness, we would require the additional property that an embedding be [[elementary embedding|elementary]]), then for any two models $M, N \in \mathbf{Mod}(T)$

$$
M \leftarrow A \rightarrow N
$$

containing $A$, we have that for every sentence $\varphi$ satisfied by $N$, $T \models \varphi \leftrightarrow \psi$ where $\psi$ is quantifier-free. Therefore, $\psi$ transfers to $A$ and $M$, so $M \models \varphi$ as well, and vice-versa.

$(\Leftarrow)$ Now suppose $T$ is substructure complete. Fix $\varphi(x)$ an $\mathcal{L}$-formula. Consider the [[type (in model theory)|type]] $\Phi$ of its quantifier-free consequences,i .e.

$$
\Phi(x) \overset{\operatorname{df}}{=} \{\varphi^*(x) \text{ quantifier-free } \operatorname{|} T \models \varphi \implies \varphi^*\}.
$$

(This thing is like the quantifier-free principal ultrafilter on $\varphi$ in the Boolean algebra of definable sets.)

Let $d_1, \dots, d_n$ be distinct new constant symbols. Write $d = \vec{d} = (d_1, \dots, d_n)$.

Claim: $T \cup \Phi(d) \models \varphi(d).$

(This claim says, roughly, that knowing the principal ultrafilter of quantifier-free definable sets containing $\varphi(x)$ suffices to pin down $\varphi(x)$. After establishing the claim, it will be easy to improve it to full quantifier elimination.)

Proof of claim: suppose towards a contradiction that there exists an $A \models T \cup \Phi(d) \cup \{\not \varphi(d)\}.$ (This is a structure in the language $\mathcal{L}$ of $T$, expanded by $d$.) Let $d^A$ be the interpretation of the new constants $d$ in $A$. Consider the finitely-generated $\mathcal{L}$-substructure of $A$ around $d^A$:

$$
C \overset{\operatorname{df}}{=} \langle d^A \rangle_{\mathcal{L}}.
$$

Subclaim: $T \cup \{\varphi(d^A)\} \cup \mathsf{Diag}(C)$ _is_ satisfiable.

(This subclaim amounts to saying that while $A$ models $\neg \varphi(d^A)$, we can find another model $B \models T$, embedding $C$, such that $B$ _does_ models $\varphi(d^A)$.)

Proof of subclaim: this will be a standard [[compactness theorem|compactness argument]]. Suppose not; by compactness there exist finitely many sentences $\theta_1, \dots, \theta_m \in \mathsf{Diag}(C)$ such that

$$
T \cup \{\varphi(d^A)\} \cup \{\theta_i\}_{1 \leq i \leq m}
$$ 

is not satisfiable. By the definition of [[quantifier-free diagram]],  we can write $\theta_i = \theta'_i(d^A)$, where $\theta'_i$ is a quantifier-free $\mathcal{L}$-formula.

Therefore,

$$
T \cup \{\varphi(d^A), \theta'_0(d^A), \theta'_1(d^A), \dots, \theta_m'(d^A)\}
$$

is not satisfiable, where (remembering that $d^A$ is now just a tuple of constant symbols) $\theta'_0(x)$ specifies that all the entries of $x$ are distinct.

Therefore,

$$
T \models \varphi(d^A) \rightarrow \bigvee_{i = 0}^m \neg \theta'_i(d^A).
$$

Since there are no constraints on the constant symbols $d^A$ and $\theta'_0$ specifies that they are all distinct, we may generalize them, so that 

$$
T \models \forall x \left( \varphi(x) \to \bigvee_{i = 0}^m \neg \theta'_i(x) \right)
$$

hence

$$
\bigvee_{i = 0}^m \neg \theta'_i(x) \in \Phi(x).
$$

Now, by assumption, $A \models \Phi(d)$. This means in particular that $A \models \bigvee_{i = 0}^m \neg \theta'_i(d^A).$

Since that disjunction is quantifier-free, it transfers down to $C$. Therefore, there is some $0 \leq j \leq m$ such that $C \models \neg \theta'_j(d^A).$ Since the $d^A$ were distinct when we obtained $A$ (from which we obtained $C$), we can rule out $j \neq 0$. But for each $j = 1, \dots, m$, $\theta_j = \theta'_j(d^A) \in \mathsf{Diag}(C)$. This is a contradiction.

This proves the subclaim.

Now we proceed with proving the claim.

Let $\mathbf{B} \models T \cup \{\varphi(d^A)\} \cup \mathsf{Diag}(C).$

Then:

$$
A \models \neg \varphi(d^A), \text{ and } B \models \varphi(d^A),
$$

which contradicts substructure completeness over $C$.

This proves the claim.

Now we proceed with proving the theorem.

With the claim in hand, the [[compactness theorem]] tells us that the entailment $T \cup \Phi(x) \models \varphi(d)$ is finitely supported, so that there are finitely many $\varphi^*_1, \dots, \varphi^*_m \in \Phi(x)$ such that

$$
T \cup \{\varphi_i^*(d)\}_{i \leq m} \models \varphi(d).
$$

Write $\varphi^* \overset{\operatorname{df}}{=} \bigvee_{i \leq m} \varphi_i^*.$ Again, we generalize the constants $d$, obtaining

$$
T \models \forall x \left( \varphi \leftrightarrows \varphi^* \right).
$$

Since the $\varphi^*_i$ are all quantifier-free, and $\varphi$ was arbitrary, we have proved that $T$ eliminates quantifiers.
=--

## Examples

* By the above theorem, any theory which [[quantifier elimination|eliminates quantifiers]] is substructure complete.

* So e.g. the [[countable random graph]], the theory [[ACF]] of algebraically closed fields, the theory [[DLO]] of dense linear orders...

## Remarks
* The analogous (and weaker) property where one asks that the theory of the elementary class of $T$-models embedding a fixed $T$-model is complete is called [[model complete theory | model completeness]].

* Of course, substructure-completeness implies model-completeness.

## Related concepts
* [[quantifier elimination]]

* [[model complete theory]]

* [[existentially closed model]]

* [[diagram of a first-order structure]]

## References

* {#Marker}Dave Marker, _Model theory: an introduction_, theorem 3.14

[[!redirects substructure-complete]]

[[!redirects substructure completeness]]

[[!redirects substructure-completeness]]

[[!redirects substructure complete theories]]

[[!redirects substructure-complete theories]]

[[!redirects substructure complete]]
