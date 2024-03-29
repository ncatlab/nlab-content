
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A __ringed space__ is a pair $(X,O_X)$ where $X$ is a [[topological space]] and $O_X$ is a [[sheaf]] of unital [[ring]]s. The sheaf $O_X$ is called the __[[structure sheaf]]__ of the ringed space $(X,O_X)$. 

If all [[stalks]] of the structure sheaf are [[local ring]]s, it is called a [[locally ringed space]].

A __morphism of ringed spaces__ $(f,f^\sharp):(X,O_X)\to (Y,O_Y)$ is a pair
where $f:X\to Y$ is a continuous map and the __[[comorphism]]__ $f^\sharp : O_Y\to f_* O_X$ is a morphism of [[sheaf|sheaves]] of rings over $Y$. Here $f_*$ denotes the [[direct image]] [[functor]] for [[sheaf|sheaves]]. Any sheaf of abelian modules $\mathcal{M}$ equipped with actions $O_X(U)\times\mathcal{M}(U)\to\mathcal{M}(U)$ making $\mathcal{M}(U)$ left $O_X$-modules, and such that the actions strictly commute with the restrictions,
is called a __sheaf of left $O_X$-modules__.

## Remarks

* Every ringed space induces a [[ringed site]]: To a ringed space $(X,O_X)$ assign the ringed site $(Op_X,O_X)$ where $Op_X$ is the [[category of open subsets]] (with [[morphisms]] their inclusions) equipped with the [[Grothendieck pretopology]] of [[open covers]], and $O_X$ is regarded as a [[structure sheaf]] of [[rings]] on $Op_X$.

* In [toric geometry](http://en.wikipedia.org/wiki/Toric_variety) and sometimes in relation to the "absolute" [algebraic geometry over](http://en.wikipedia.org/wiki/Field_with_one_element) $F_1$, one talks about monoided or monoidal space (Kato; Deitmar); which is a topological space together with a sheaf of [[monoid]]s. N. Durov on the other hand develops a generalized algebraic geometry based on a notion of generalized ringed space, which is a space equipped with a sheaf of (commutative) generalized rings, which are finitary (= [[algebraic monad|algebraic]]) monads in $\mathrm{Set}$ with a commutativity condition (which are related to higher analogues of [[Eckmann-Hilton argument]]).



## Related concepts

* [[locally ringed space]]

* [[ringed site]], [[locally ringed site]] 

* [[ringed topos]], [[locally ringed topos]]

* [[locally algebra-ed topos]]

* [[structured (∞,1)-topos]]

## References

Textbook accounts:

* [[Siegfried Bosch]], p. 247-248 in *Algebraic Geometry and Commutative Algebra*, Universitext, Springer (2017) &lbrack;[doi:10.1007/978-1-4471-4829-6](https://doi.org/10.1007/978-1-4471-4829-6)&rbrack;

*  Ulrich Görtz, Torsten Wedhorn, p. 55 in: *Algebraic Geometry I: Schemes*, Springer (2020) &lbrack;[doi:10.1007/978-3-658-30733-2](https://doi.org/10.1007/978-3-658-30733-2)&rbrack;

See also:

* {#deJong} [[Aise Johan de Jong]], _[[The Stacks Project]]_, _Ringed spaces_, ([tag 0090](https://stacks.math.columbia.edu/tag/0090))

* [[eom]], *[Ringed spaces](https://encyclopediaofmath.org/wiki/Ringed_space)*

Also see references at *[[ringed topos]]*.


[[!redirects ringed spaces]]