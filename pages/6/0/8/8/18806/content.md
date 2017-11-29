# The mix rule

* table of contents
{: toc}

## Definition

The **mix rule** is an [[inference rule]] that can be added to [[linear logic]].  The most common mix rule is the binary mix rule

$$ \frac{\Gamma\vdash \Delta \quad \Gamma'\vdash\Delta'}{\Gamma,\Gamma' \vdash \Delta,\Delta'} $$

but to be consistent one should also consider the nullary mix rule

$$ \frac{ }{\top\vdash \bot} $$

which together are equivalent to $\top\cong\bot$, and imply "$n$-ary" mix rules for all $n$.

## Semantics

Ordinary linear logic has semantics in [[polycategories]], [[linearly distributive categories]], and [[star-autonomous categories]], depending on how many connectives are assumed.  A linearly distributive category satisfies the binary mix rule if there is a morphism $\bot\to\top$ satisfying a certain coherence axiom.  It additionally satisfies the nullary mix rule if this morphism is an isomorphism.  In [CS97](#CS97) these are called **mix categories** and **isomix categories** respectively.

## References

* [[Robin Cockett]] and [[R.A.G. Seely]], *Proof theory for full intuitionistic linear logic, bilinear logic, and mix categories*, 1997.  [TAC](http://tac.mta.ca/tac/volumes/1997/n5/3-05abs.html)
 {#CS97}

[[!redirects mix rules]]
[[!redirects MIX rule]]
[[!redirects MIX rules]]

[[!redirects mix category]]
[[!redirects MIX category]]
[[!redirects mix categories]]
[[!redirects MIX categories]]

[[!redirects isomix category]]
[[!redirects isoMIX category]]
[[!redirects isomix categories]]
[[!redirects isoMIX categories]]
[[!redirects iso-mix category]]
[[!redirects iso-MIX category]]
[[!redirects iso-mix categories]]
[[!redirects iso-MIX categories]]
