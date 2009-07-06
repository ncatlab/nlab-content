#Idea#

A _group object_ in an [[(infinity,1)-topos]] is the generalization of [[Jim Stasheff|Stasheff]] [[H-space]]  from [[Top]] to more general [[infinity-stack]] [[(infinity,1)-topos]]es: an object that comes equipped with an associative and invertible [[monoid]] structure, up to coherent [[homotopy]]. 

Of particular relevance are such group objects that are [[quotient object|effective]]: these are [[delooping|deloopable]]. 

A _groupoid object_ is then accordingly the many-object version of a group object. A groupoid object being effective means that it is a [[Cech nerve]]. Therefore groupoid objects in an $(\infty,1)$-category play a central role in the theory of [[principal infinity-bundle]]s.

Notice that one of the four characterizing properties of an [[(infinity,1)-topos]] is that every groupoid object is effective. 




#Details#


In section 6.1.2 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

a notion of [[groupoid]] object [[internalization|internal]] to an [[(infinity,1)-category]] $\mathbf{C}$ is defined
as [[homotopy]]-[[simplicial object]] in $\mathbf{C}$ given by an [[(infinity,1)-functor]]

$$
  C : \Delta^{op} \to \mathbf{C}
$$

satisfying some conditions that make it look like the [[nerve]] of an [[internal category|internal]] [[groupoid]] (proposition 6.2.2.6 in [[Higher Topos Theory|HTT]]).

Such a groupoid object with $C_0 = {*}$ is a group object.

If $C$ is the [[Cech nerve]] of a morphism $C_0 \to C_{-1}$ then the groupoid object is [[delooping|deloopable]] (called _effective_; the $(\infty,1)$-analog of a [[quotient object]]) and we write

$$
  C_{-1} := \mathbf{B}C
  \,.
$$

In an [[(infinity,1)-topos]] every groupoid object is [[delooping|deloopable]].