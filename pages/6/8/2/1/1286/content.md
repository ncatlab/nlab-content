#Idea#

A _derived stack_ is an [[(infinity,1)-sheaf]] whose domain is not a [[1-category]].

One says _derived stack_ in order to distinguish from the traditional notion of [[infinity-stack]] which is an [[(infinity,1)-sheaf]] whose domain is still a 1-categorical [[site]].

For recall that a [[sheaf]] is a [[functor]] $F : C^{op} \to Set$ satisfying some [[descent]]-condition.
So there are two steps in which the notion of [[sheaf]] may be [[vertical categorification|categorified]]:

1. the codomain is categorified and the domain remains a 1-category
1. the codomain and the domain are categorified.

The categorification of the codomain leads to the notion of [[stack]]s when [[Set]] replaced by [[Grpd]], and further to [[infinity-stack]]s, when sets are replaced by [[infinity-groupoid]]s. 

But there is no natural reason why the domain should in general remain a 1-category if one passes to an [[infinity-category|infinity-categorical]]-context. A _derived stack_ is a generalization of the notion of sheaf where both domain and codomain are taken to be $\infty$-categorical.

In practice one often looks at the model of derived stacks obtained from generalizing the theory of [[simplicial presheaf|simplicial presheaves]]: so a derived pre-stack is often modeled as a [[SSet]]-[[enriched category theory|enriched]] functor $F : C^{op} \to SSet$ from an [[SSet]]-enriched category to $SSet$.

# Fiber products #

One general idea for the use of higher and derived stacks is that

* passing to a higher categorical codomain  -- i.e. from Set-values [[sheaf|sheaves]] to higher [[groupoid]] valued sheaves -- is a means to complete under colimits. For instance in the category [[Diff]] of manifolds the quotient by a non-free action of a group may not exist, but in [[stack]]s $[Diff^{op}, Grpd]$ it exists as the corresponding smooth [[action groupoid]] or [[orbifold]].

* passing to higher categorical domain -- i.e. from presheaves on categories to presheaves on higher categories, is analogously a means to complete under limits. For instance (... standard example should go here ...)

#Examples#

* passing from [[sheaf|sheaves]] or [[infinity-stack]]s on the domain [[CRing]] of commutative rings to the [[simplicially enriched category]] (hence an [[(infinity,1)-category]]) $SimpCRing$ of simplicial commutative rings corresponds, under the [[Dold-Kan correspondence]] to passing from spaces with an ordinary function algebra to spaces with a [[differential graded algebra]] as a function algebra. These are generalized [[NQ-supermanifold]]s. (...more details and context should go here ...)


#References#

An overview is provided in 

* B. To&#235;n;  _Higher and derived stacks: a global overview_ ([arXiv](http://arxiv.org/abs/math.AG/0604504))

Details modeled on [[simplicially enriched category|simplicial categories]] have been developed in the series of articles by To&#235;n and Vezossi.

This article generalizes the notion of [[site]] and [[model structure on simplicial presheaves]] from 1-categorical sites to [[simplicially enriched category|simplicial sites]]:

* B. To&#235;n, G. Vezzosi, _Homotopical Algebraic Geometry I: Topos theory_ ([arXiv](http://arxiv.org/abs/math.AG/0207028))

Of central interest in derived algebraic geometry is the simplicial site of _simplicial algebras_, which generalizes the familiar site of algebra used in algebraic geometry. This is introduced and studied in

* B. To&#235;n, G. Vezzosi, _Homotopical Algebraic Geometry II: geometric stacks and applications_ ([arXiv](http://arxiv.org/abs/math.AG/0404373))

Further developments in this direction are in

* B. To&#235;n, G. Vezzosi, _From HAG to DAG: derived moduli stacks_ in Axiomatic, enriched
and motivic homotopy theory, 173&#8211;216, NATO Sci. Ser. II Math. Phys. Chem., 131, Kluwer
Acad. Publ., Dordrecht, 2004. ([arXiv](http://arxiv.org/abs/math.AG/0210407))


The unifying picture, in particular independent of the choice of model for the [[(infinity,1)-category|(infinity,1)-categories]] is presented in

* [[Jacob Lurie]], [[Higher Topos Theory]]

Derived ($\infty$-)stacks are currently mostly, maybe exclusively, studied on algebraic sites $S$, where the category $S^{op} := $ [[Alg]] is replaced with a category of "$\infty$-algebras" of sorts. The theory of these $\infty$-algebras is described in great detail in


* Jacob Lurie, _Derived Algebraic Geometry II: Noncommutative Algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))
