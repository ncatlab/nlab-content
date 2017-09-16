A __ringed space__ is a pair $(X,O_X)$ where $X$ is a [[topological space]] and $O_X$ is a [[sheaf]] of unital [[ring]]s. The sheaf $O_X$ is called the __structure ring__ of the ringed space $(X,O_X)$. A __morphism of ringed spaces__ $(f,f^\sharp):(X,O_X)\to (Y,O_Y)$ is a pair
where $f:X\to Y$ is a continuous map and the __comorphism__ $f^\sharp : O_Y\to f_* O_X$ is a morphism of [[sheaf|sheaves]] of rings over $Y$. Here $f_*$ denotes the [[direct image]] [[functor]] for [[sheaf|sheaves]]. Any sheaf of abelian modules $\mathcal{M}$ equipped with actions $O_X(U)\times\mathcal{M}(U)\to\mathcal{M}(U)$ making $\mathcal{M}(U)$ left $O_X$-modules, and such that the actions strictly commute with the restrictions,
is called a __sheaf of left $O_X$-modules__.

#Remarks#

* Every ringed space induces a [[ringed site]]: To a ringed space $(X,O_X)$ assign the ringed site $(Op_X,O_X)$ where $Op_X$ is the category of open sets and inclusions equipped with the pretopology of open covers and $O_X$ is just viewed as a sheaf of rings on $Op_X$.

* In [toric geometry](http://en.wikipedia.org/wiki/Toric_variety) and sometimes in relation to the "absolute" [algebraic geometry over](http://en.wikipedia.org/wiki/Field_with_one_element) $F_1$, one talks about monoided or monoidal space (Kato; Deitmar); which is a topological space together with a sheaf of [[monoid]]s. N. Durov on the other hand develops a generalized algebraic geometry based on a notion of generalized ringed space, which is a space equipped with a sheaf of (commutative) generalized rings, which are finitary (= [[algebraic monad|algebraic]]) monads in $\mathrm{Set}$ with a commutativity condition (which are related to higher analogues of [[Eckmann-Hilton argument]]).

* The generalization of the notion of ringed spaces to generalized rings is a [[structured generalized space]].