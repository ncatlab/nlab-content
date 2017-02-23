
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Any model of [[material set theory]] gives rise to a [[category]] of [[sets]], which is a model of [[structural set theory]].  Conversely, from any [[structural set theory]] we can construct a model of material set theory by using [[graphs]] to model hereditary membership relations, as described at _[[pure set]]_.  Viewed in the correct context, these two constructions are a pair of [[adjoint functors]].  Moreover, the adjunction is [[idempotent adjunction|idempotent]], and thus induces an equivalence between models of the two types of set theory which satisfy appropriate "foundation-type" axioms.

## Definition

One has to be a little careful in defining the relevant categories of models in order to make this precise.  Of course, there are also many different variants depending on how strong or weak the set theories in question are.  There is also an additional subtlety in that models of material set theory naturally form a [[1-category]], while models of structural set theory naturally form a [[2-category]].

...

## Idempotence

The adjunction is [[idempotent adjunction|idempotent]], and therefore restricts to an equivalence between the full images of the two functors involved.  In the well-founded case, we can characterize these as follows:

* A model of material set theory is in the fixed subcategory if it satisfies the [[axiom of foundation]], it has [[transitive closure|transitive closures]], and it satisfies [[Mostowski's principle]].

* A model of structural set theory is in the fixed subcategory if every set can be embedded into an extensional well-founded relation.

If we use a non-well-founded construction of pure sets as the right adjoint, then the axiom of foundation must be replaced by an appropriate [[axiom of anti-foundation]].  Note that axioms of anti-foundation usually include appropriate ill-founded generalizations of Mostowski's principle and the existence of transitive closures.  Similarly, on the structural side the necessary axiom becomes embeddability of all sets into a suitable type of [[extensional relation]].

## References

The material-structural adjunction was first observed, for a particular pair of theories, in:

* William Mitchell 1973, _Categories of Boolean topoi_, Journal of Pure and Applied Algebra 3(3), pp. 193-201. ([link](http://dx.doi.org/10.1016/0022-4049%2873%2990009-1))
