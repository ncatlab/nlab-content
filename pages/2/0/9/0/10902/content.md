## Idea

A _closed morphism_ is a continuous map such that the image of any closed subset is closed.

## In topology

## In locale theory

A map $f : X \to Y$ of [[locales]] is _closed_ iff for any $u \in O(X)$ and $v \in O(Y)$ the reciprocity relation
$$ f_*(u \vee f^*v) = f_*(u) \vee v $$
holds. ("$\geq$" is trivially always satisfied.) The map $f_* : O(X) \to O(Y)$ is the monotone right adjoint to $f^* : O(Y) \to O(X)$, explicitly given by
$$ f_*(u) = \sup\{ v \in O(Y) \,|\, f^*(v) \leq u \}. $$

## In topos theory

+-- {: .num_defn}
###### Definition

A geometric morphism $f : \mathcal{F} \to \mathcal{E}$ is _closed_ iff for any object $A \in \mathcal{E}$, the induced locale morphism
$$ \mathrm{Sub}_{\mathcal{F}/f^*A}(1) \to \mathrm{Sub}_{\mathcal{E}}(1) $$
between the spaces of subobjects of the corresponding terminal objects is closed.
=--

+-- {: .num_example}
###### Example

Let $A$ be an object of a topos $\mathcal{E}$. Then the canonical geometric morphism $\mathcal{E}/A \to A$ is closed iff $A$ fulfills the following condition, formulated in the [[internal language]]:
$$ \mathcal{E} \models \forall U \subseteq A{:} \forall p \in \Omega{:} \quad A \subseteq (U \cup \{ x \in A \,|\, p \}) \quad\Rightarrow\quad (A \subseteq U) \vee p. $$
Note that this condition is satisfied for any $A$ whatsoever if the internal language of $\mathcal{E}$ is boolean.
=--

+-- {: .num_example}
###### Example

Let $f : A \to B$ be a morphism in a topos $\mathcal{E}$. Then the induced geometric morphism $\mathcal{E}/A \to \mathcal{E}/B$ is closed iff, in the internal language of $\mathcal{E}$, the fibers of $f$ fulfill the condition displayed at the previous example.
=--

+-- {: .num_remark}
###### Remark

A geometric morphism $f : \mathcal{F} \to \mathcal{E}$ is closed iff the locale $f_* \Omega_{\mathcal{F}}$ internal to $\mathcal{E}$ satisfies
$$ \mathcal{E} \models \ulcorner \mathrm{the locale map $f_* \Omega_{\mathcal{F}} \to 1$ is closed} \urcorner. $$
=--
