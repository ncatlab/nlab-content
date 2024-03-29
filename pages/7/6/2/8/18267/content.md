[[!redirects model complete theory ]]
[[!redirects model complete theory ]]
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
Model completeness is a [[property]] of [[first-order theories]] (in the same way that [[existential closedness]] is a [[property]] of [[first-order structures]]) meant to generalize the properties of the theory [[ACF]] of [[algebraically closed fields]].

As discussed in Hodges' [Model theory](#Hodges1993):

> In the early 1950s [[Abraham Robinson]] noticed that certain maps studied by algebraists are in fact [[elementary embeddings]]. If you choose a map at random, the chances of it being an elementary embedding are negligible. So Robinson reckoned that there must be a systematic reason for the appearance of these elementary embeddings, and he set out to find what the reason was.

> In the course of this quest he introduced the notions of model complete theories, companionable theories and [[model companion|model companions]]. These notions have become essential tools for the model theory of algebra.

## Definition

We say a [[first-order theory]] $T$ is *model complete* if every embedding (not necessarily elementary) between models of $T$ _is_ elementary.

The following characterization appears as Theorem 8.3.1 in ([Hodges93](#Hodges1993)):

+-- {: .num_theorem}
###### Theorem

Let $T$ be as above. The following are equivalent:

1. $T$ is model complete.

2. Every model of $T$ is [[existentially closed model|existentially closed]].

3. For every embedding $A \hookrightarrow B$ where $A$ and $B$ model $T$, there exists an [[elementary extension]] $D$ of $A$ and an embedding $g : B \to D$ such that the triangle commutes.

4. Every [[existentially closed model|existential formula]] is equivalent (mod $T$) to a [[existentially closed model|universal formula]].

5. Every formula is equivalent (mod $T$) to a universal formula.

=--

## Examples

* Since [[quantifier elimination]] is equivalent to [[substructure completeness]], which is stronger than model completeness, every theory which eliminates quantifiers is model complete. So, for example, [[ACF]], [[DLO]], [[RCF]], and the theory of the [[countable random graph]] are all model complete (and so their models are [[existentially closed]].)

## Remarks

* A theory $T$ is model complete if and only if for every _model_ $A$ of $T$, the [[quantifier-free diagram]] $T_{\mathsf{Diag}(A)}$ (whose models are precisely the models of $T$ containing $A$ as an embedded substructure) is _complete_.

* Analogously, a theory $T$ is [[substructure complete]] if and only if for every model $A$ of $T$ and every _substructure_ $B \subseteq A$, the [[quantifier-free diagram]] $T_{\mathsf{Diag}(B)}$ is _complete_.

* A model complete theory is an "existentially closed theory" in the sense that all of its models are [[existentially closed model|existentially closed models]].

* As mentioned above, [[substructure completeness]] implies model completeness because every elementary submodel is also a substructure. The proposition below shows that the converse holds with some additional assumptions.

## Model completeness + amalgamation property implies substructure completeness

+-- {: .num_prop #substructureconverse}
###### Proposition

Suppose the [[first-order theory]] $T$ in the language $\mathcal{L}$ is model complete and has the property that for any two models $X,Y \models T$ and a mutual $\mathcal{L}$-substructure $A \hookrightarrow X,Y$, the latter [[span]] in the category of $\mathcal{L}$-structures and embeddings has a [[cocone]] $Z$ which is also a model of $T$.

Then $T$ is [[substructure complete]].

=--

This property of being able to "amalgamate" the models $X$ and $Y$ over the common substructure $A$ is sometimes called the **amalgamation property**, though this terminology is rather overloaded (c.f. [[Fraisse limit]]).

+-- {: .proof}
###### Proof

Let $A$ be a substructure of some model $M \models T$. Append the [[quantifier-free diagram]] of $A$ to $T$ to form $T_{\mathsf{Diag}(A)}$. Suppose towards a contradiction that $\varphi$ is a sentence which is undecided by $T_{\mathsf{Diag}(A)}$; let $X$ and $Y$ be models of $T_{\mathsf{Diag}(A)}$ which witness this, so that $X \models \varphi$ while $Y \models \neg \varphi$.

Let $Z$ amalgamate $X$ and $Y$ over $A$.

By [[model completeness]], the theory $T_{\mathsf{Diag}(X)}$ of $T$-models (not necessarily [[elementary embedding|elementarily]]) embedding $X$ is complete. Abuse notation and replace the instances of constants from $A$ in $\varphi$ with their images in $X$. Either $T_{\mathsf{Diag}(X)} \models \varphi$ or $T_{\mathsf{Diag}(X)} \models \neg \varphi$. Since $X$ certainly embeds itself and $X \models \varphi$, $T_{\mathsf{Diag}(X)} \models \varphi$.

Similarly, $T_{\mathsf{Diag}(Y)} \models \neg \varphi.$

Now, on one hand, the theory $T_{\mathsf{Diag}(X)} \cup T_{\mathsf{Diag}(Y)}/A$ (where we glue along the copies of $A$ in $\mathsf{Diag}(X)$ and $\mathsf{Diag}(Y)$) entails both $\varphi$ and $\neg \varphi$, which makes it inconsistent. This theory therefore has no models.

On the other hand, this theory axiomatizes the class of amalgams of $X$ and $Y$ over $A$ in the category of $\mathcal{L}$-structures and embeddings, so in particular is modelled by $Z$, a contradiction.
=--


## Related concepts

* [[quantifier elimination]]

* [[model companion]]

* [[substructure completeness]]

* [[existentially closed model]]

## References 

* {#Hodges1993}Wilfrid Hodges, _Model theory_, Cambridge Univ. Press 1993

[[!redirects model completeness]]
[[!redirects model-complete theory]]
[[!redirects model-completeness]]
[[!redirects model complete]]