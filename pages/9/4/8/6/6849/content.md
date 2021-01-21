
# Directional derivatives
* table of contents
{: toc}

## Idea

A directional derivative, or G&#226;teaux derivative, is a [[partial derivative]] of a [[function]] on a [[manifold]] along the direction given by a [[tangent vector]].


## Definitions

Let $F$ and $G$ be [[locally convex topological vector space]]s, $U \subseteq F$ an [[open subspace]] and $P\colon U \to G$ a [[continuous map]]. The __derivative__ of $P$ at the point $f \in U$ in the __direction__ $h \in F$ is the [[convergence|limit]]
$$
D P_f h = \lim_{t \to 0} \frac{1}{t} (P(f + t h) - P(f))
.$$

If the limit exists for every $f \in U$ and every $h \in F$ then one can define a map
$$
D P\colon U \times F \to G
.$$
If the limit exists and $D P$ is [[continuous map|continuous]] (jointly in both variables), we say that $P$ is __[[continuously differentiable map|continuously differentiable]]__ or $C^1$.

A simple but nontrivial example is the operator
$$
P\colon C^{\infty}[a, b] \to C^{\infty}[a, b]
$$
given by
$$
P(f) \coloneqq f f'
$$
with the derivative
$$
D P(f) h = f' h + f h'
.$$

In the context of a [[Fréchet space]], it may be that the directional derivative in every direction exists but the [[Fréchet derivative]] does not; however the existence of Fr&#233;chet derivative implies the existence of directional derivatives in all directions. 

The notion of directional derivatives extends to [[smooth manifolds]] (including infinite-dimensional ones based on [[Fréchet spaces]]) using local coordinates; the differentiability does not depend on the choice of a local chart. In this case we have (if everything is defined)
$$
D P\colon T(U) \to G
,$$
where $T(U)$ is the [[tangent space]] of $U$ (an open subspace of $T(F)$.


## References

* Wikipedia (English): [G&#226;teaux derivative](http://en.wikipedia.org/wiki/G%C3%A2teaux_derivative)

* [[eom]]: [G&#226;teaux derivative](http://eom.springer.de/g/g043360.htm), [G&#226;teaux variation](http://eom.springer.de/G/g043390.htm), [Ren&#233; G&#226;teaux](http://en.wikipedia.org/wiki/Ren%C3%A9_G%C3%A2teaux)

* R. G&#226;teaux, _Sur les fonctionnelles continues et les fonctionnelles analytiques_, C.R. Acad. Sci. Paris S&#233;r. I Math. __157__ (1913)  pp. 325&#8211;327; _Fonctions d'une infinit&#233;s des variables ind&#233;pendantes_,  Bull. Soc. Math. France __47__  (1919) 70&#8211;96, [numdam](http://www.numdam.org/item?id=BSMF_1919__47__70_1); _Sur diverses questions du calcul fonctionnel_, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France tome __50__ (1922) 1&#8211;37, [numdam](http://www.numdam.org/item?id=BSMF_1922__50__1_0)

An analogue of the directional derivative and Faa di Bruno formula in the Goodwillie calculus are in

* [[Kristine Bauer]], Brenda Johnson, Christina Osborne, [[Emily Riehl]], Amelia Tebbe, _Directional derivatives and higher order chain rules for abelian functor calculus_ ([arxiv/1610.01930](https://arxiv.org/abs/1610.01930))

[[!redirects directional derivative]]
[[!redirects directional derivatives]]
[[!redirects Gâteaux derivative]]
[[!redirects Gâteaux derivatives]]
[[!redirects Gateaux derivative]]
[[!redirects Gateaux derivatives]]
[[!redirects Gâteaux differentiability]]
