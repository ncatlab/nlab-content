[[!redirects locally ringed space]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A __locally ringed space__ is a [[ringed space]] $(X,\mathcal{O})$ such that the [[stalks]] of the [[structure sheaf]] $\mathcal{O}$ are [[local ring]]s. 

A [[morphism]] of locally ringed spaces is a morphism of ringed spaces $(f,f^\sharp)\colon (X,\mathcal{O}_X)\to (Y,\mathcal{O}_Y)$, where $f:X\to Y$, such that $f_\sharp : f^*\mathcal{O}_Y \to \mathcal{O}_X$ is a morphism of [[local rings]] (that is, a map of rings which respects the [[maximal ideal]] (reflects invertibility)), where $f_\sharp$ is the [[adjunct]] of the [[comorphism]] $f^\sharp:\mathcal{O}_Y\to f_*\mathcal{O}_X$. Here we are considering $\mathcal{O}_X$ and $\mathcal{O}_Y$ to be local rings defined in the [[internal logic]] of the respective [[sheaf topos]]es, and $f^*\mathcal{O}_Y$ is an internal local ring because the [[inverse image]] functor $f^*$ preserves [[geometric logic]].

## Examples

\begin{example}\label{ExampleSchemes}
**([[schemes]])**
\linebreak
Historically, *[[schemes]]* are thought of as locally ringed spaces and this application of the notion to [[algebraic geometry]] motivated much of its development. 

(However, already [Grothendieck (1973)](functorial+geometry#Grothendieck73) pointed out that it is often more frutiful to view [[schemes]] instead via their [[functor of points]], see at *[[functorial geometry]]* for more.)
\end{example}


\begin{example}\label{ExampleSmoothManifolds}
**([[smooth manifolds]])**
\linebreak
The [[category]] [[SmthMfd]] of [[smooth manifolds]] has a canonical [[fully faithful functor|embedding]] into the category of locally ringed spaces: 

Indeed, any smooth manifold $M$ comes equipped with a [[sheaf]] of [[real numbers|real]]-valued [[smooth functions]] $\mathcal{C}^{\infty}_M$, and the [[maximal ideal]] in a given stalk consists precisely of [[germs]] of smooth functions which vanish at that point. Moreover, a [[smooth map]] $f \colon M \to N$ determines a [[comorphism]] $f^\sharp: \mathcal{C}^{\infty}_N \to f_* \mathcal{C}^{\infty}_M$ by the usual precomposition. 

This inclusion of smooth manifolds into locally ringed spaces is [[fully faithful functor|fully faithful]]. For a proof, see Lucas Braune's comment at [Math.SE:511604](https://math.stackexchange.com/a/511604/58526).

(In fact, already the [[embedding of smooth manifolds into formal duals of R-algebras]] is [[fully faithful functor|fully faithful]], which means that all smooth manifolds are even "[[affine schemes|affine]]" locally ringed spaces, in a sense.)
\end{example}


## On the locality condition

The condition that all stalks $\mathcal{O}_{X,x}$ are local rings can be reformulated without referring to the points of $X$:

* The only open subset $U$ such that $\mathcal{O}_X(U)$ is the zero ring is $U = \emptyset$.
* Let $f, g \in \mathcal{O}_X(U)$ be local sections such that $f + g$ is invertible in $\mathcal{O}_X(U)$. Then there is an open covering $U = V \cup W$ such that $f|_V \in \mathcal{O}_X(V)$ and $g|_W \in \mathcal{O}_X(W)$ are invertible. (It's allowed that $V$ or $W$ are empty.)

## Related concepts

* [[ringed space]], **locally ringed space**

* [[ringed locale]], [[locally ringed locale]]

* [[ringed site]], [[locally ringed site]]

* [[ringed topos]], [[locally ringed topos]]

* [[locally algebra-ed topos]]

* [[structured (∞,1)-topos]]

## References
 {#References}

Textbook accounts:

* [[Siegfried Bosch]], p. 247-248 in *Algebraic Geometry and Commutative Algebra*, Universitext, Springer (2017) &lbrack;[doi:10.1007/978-1-4471-4829-6](https://doi.org/10.1007/978-1-4471-4829-6)&rbrack;

*  Ulrich Görtz, Torsten Wedhorn, p. 55 in: *Algebraic Geometry I: Schemes*, Springer (2020) &lbrack;[doi:10.1007/978-3-658-30733-2](https://doi.org/10.1007/978-3-658-30733-2)&rbrack;

See also:

* [[Aise Johan de Jong]], _[[The Stacks Project]]_, _Locally ringed spaces_ ([tag 01HA](http://stacks.math.columbia.edu/tag/01HA))
{#deJong}

* [[James Milne]], section 4 of _[[Lectures on Étale Cohomology]]_

* [[eom]], *[Ringed spaces](https://encyclopediaofmath.org/wiki/Ringed_space)*

See also references at *[[locally ringed topos]]*.

[[!redirects locally ringed topological spaces]]


[[!redirects locally ringed spaces]]

