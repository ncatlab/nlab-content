[[!redirects The logic K(m)]]
[[!redirects The logic $K_{(m)}$]]

#Contents#
* table of contents
{:toc}
##The epistemic logics $K$ and $K_{(m)}$##

This is the basic [[epistemic logic]].  It is 'basic' with not much structure relating to any ideas of how 'knowledge' behaves.

($K$ is the usual notation for $K_{(1)}$.)

##Axiomatisation##

* (Taut)  All (instances of ) propositional tautologies.

*   For each $i = 1,\ldots, m$, the axiom, ($K_i$):

$$(K_i\phi \wedge K_i(\phi \to \psi))\to K_i\psi.$$

##Derivation rules##

* (MP) 

$$\frac{\phi \quad \phi\to \psi}{\psi} \quad$$

 (i.e. _modus ponens_);

* (Generalisation) 

$$\frac{\phi}{K_i\phi}.$$

The second deduction rule corresponds to the idea that _if a statement has been proved, then it is known to all 'agents'_.


##K##
This logic is the smallest [[normal modal logic]].

##Semantics##
The semantics of $K_{(m)}$ is just the Kripke semantics of this context, so a [[frame (modal logic)|frame]], $\mathfrak{F}$ is just a set, $W$  of possible worlds with $m$ relations $R_i$. A [[geometric models for modal logics|model]], $\mathfrak{M} = (\mathfrak{F},V)$, is a frame in that sense together with a valuation, $V: Prop \to \mathcal{P}(W)$, and the satisfaction relation is as described in [[geometric models for modal logics]] with just the difference implied by the fact that that page correspond to the use of $\Diamond_i = M_i$ whilst this uses $K_i$.  This means that 

* $\mathfrak{M},w \models K_i \phi$ if and only if, for all $v \in W$ such that $ R_i w v$, $\mathfrak{M},v \models \phi$.
=--
