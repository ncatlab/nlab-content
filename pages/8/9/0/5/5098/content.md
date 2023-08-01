
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


# Contents #
* table of contents
{:toc}

## Idea

The flavor of _[[modal logic]]_ called $K$ is [[propositional logic]] equipped with a single [[modality]] usually written "$\Box$" subject to the rules that for all [[propositions]] $p, q \colon Prop$ we have

* $\Box K \colon \Box(p \to q) \to (\Box p \to \Box q)$ ([[K modal logic]])

Often one adds to this the following further axioms

* $\Box T \colon \Box p \to p$ ([[T modal logic]])

* $\Box 4 \colon \Box p \to \Box \Box p$. ([[S4 modal logic]]).

$K$ is the basic [[epistemic logic]].  


## Properties

### Axiomatisation

* (Taut)  All (instances of ) propositional tautologies.

*   For each $i = 1,\ldots, m$, the axiom, ($K_i$):

$$(K_i\phi \wedge K_i(\phi \to \psi))\to K_i\psi.$$


### Derivation rules

* (MP) 

$$\frac{\phi \quad \phi\to \psi}{\psi} \quad$$

 (i.e. _modus ponens_);

* (Generalisation) 

$$\frac{\phi}{K_i\phi}.$$

The second deduction rule corresponds to the idea that _if a statement has been proved, then it is known to all 'agents'_.

### Normality

This logic is the smallest [[normal modal logic]].


## Semantics

The semantics of $K_{(m)}$ is just the [[Kripke semantics]] of this context, so a [[frame (modal logic)|frame]], $\mathfrak{F}$ is just a set, $W$  of [[possible worlds]] with $m$ [[relations]] $R_i$. A [[geometric models for modal logics|model]], $\mathfrak{M} = (\mathfrak{F},V)$, is a frame in that sense together with a valuation, $V \colon Prop \to \mathcal{P}(W)$, and the satisfaction relation is as described in [[geometric models for modal logics]] with just the difference implied by the fact that that page correspond to the use of $\Diamond_i = M_i$ whilst this uses $K_i$.  This means that 

* $\mathfrak{M},w \models K_i \phi$ if and only if, for all $v \in W$ such that $ R_i w v$, $\mathfrak{M},v \models \phi$.

## Related concepts

[[!include flavors of modal logics and relations -- table]]


* [[modal logic]], [[epistemic modal logic]]

* [[necessity and possibility]]

* [[T modal logic]]

* [[S4 modal logic]]

* [[S5 modal logic]]

* [[axiom K (modal logic)]]


## References

The notation "K" for a modal operator meant to express [[epistemic modality]] originates with:

* [[K. Jaakko J. Hintikka]], *Knowledge and belief: An introduction to the logic of the two notions*, Cornell University Press (1962) &lbrack;[ark:/13960/t9k437s65](https://archive.org/details/knowledgebeliefi00hint_0)&rbrack;


[[!redirects the logic K(m)]]
[[!redirects The logic K(m)]]
[[!redirects The logic $K_{(m)}$]]
[[!redirects K(m)]]



