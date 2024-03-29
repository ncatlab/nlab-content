
# Tautologies
* table of contents
{: toc}

## Idea

In common language, a *tautology* refers to a [[proposition]]  whose [[truth]] is felt to be "trivial" or "completely obvious" or "not requiring argument or highlighting", for instance since it follows just by unwinding definitions ("true by definition").

In [[classical logic|boolean]] [[propositional logic]], a _tautology_ is any [[proposition]] whose validity is unconditional --- independent of the validity of its propositional variables. Several generalizations are possible. On the one hand, the family of boolean tautologies is also the family of boolean [[theorems]]: a proposition is a boolean tautology iff it has a boolean proof. On the other hand, construing a boolean proposition as a [[universal quantification|universalized]] [[equation]] in the language of [[boolean algebras]], the boolean propositions are also the (universal, first-order) propositions of the form $P(x_1,...,x_n) = \top$ that are valid in every boolean algebra.

Of course, tautologies exist in other logics besides boolean logic, although boolean logic is perhaps the simplest nontrivial case.


## Definition

Given a [[logic]], a [[context]] $\Gamma$ within that logic, and a class of [[models]] of $\Gamma$, a __tautology__ is a [[proposition]] $\phi$ in $\Gamma$ that is true in all models; that is,
$$ \mathcal{M} \vDash \phi $$
for every model $\mathcal{M}$.


## Discussion

Compare the notion of __[[theorem]]__, sometimes called a _syntactic tautology_, which asks that $\phi$ be *provable* in $\Gamma$:

$$ 
 \Gamma 
   \;\vdash\; 
 \phi
  \,. 
$$

In the best behaved cases, each context has a [[free model]] such that the theorems are precisely the tautologies for the free model.  (For example, in the case of boolean propositional logic, the free model for the context with $n$ variables is the [[free object|free]] [[boolean algebra]] on $n$ generators.)  Even without this, there may be a class of models that can be proved to be [[soundness theorem|sound]] (every theorem is a tautology) and [[completeness theorem|complete]] (every tautology is a theorem).

## Related concepts

[[!include mathematical statements --- contents]]

## References

See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Tautology_(language)">Tautology (language)</a>*

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Tautology_(logic)">Tautology (logic)</a>*

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Tautology_(rule_of_inference)">Tautology (rule of inference)</a>*




[[!redirects tautology]]
[[!redirects tautologies]]
