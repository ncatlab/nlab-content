<div class="rightHandSide toc">[[!include differential graded objects - contents]]</div>


#Definition#

A **differential object** in a [[category with translation]] $T : C \to C$ is an [[object]] $V$ equipped with a [[morphism]] $d_V : V \to T V$.

# Remarks #

* This says that a differential object is a [[coalgebra]] for the endofunctor $T$.

#Further constructions#

* Usually, when addressing [[coalgebra]]s for $T$ as  _differential objects_ one considers these in [[additive category|additive categories]] and requires that they are _nilpotent_ in that 
$V \stackrel{d_V }{\to} T V \stackrel{T d_V}{\to} T T V$
is the [[zero morphism]]. Such a differential object is called a [[chain complex]]. 

* In a differential object $d_V : V \to T V$ in an [[additive category]] $C$ the **shifted differential object** is $T V$ with differential given by
$
  d_{T V} = - T(d_V)
$. The minus sign here is crucial in many constructions such as that of the [[mapping cone]]. It is naturally understood in terms of [[fiber sequence]]s in [[stable infinity-category|stable infinity-categories]].


