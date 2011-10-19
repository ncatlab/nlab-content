Let F and G be [[locally convex topological vector space]]s, $U \subseteq F$ open and $P: U \to G$ a continuous map. The derivative of P at the point $f \in U$ in the direction $h \in F$ is the limit
$$
DP_f h = \lim_{t \to 0} \frac{1}{t} ( P(f + t h) - P(f))
$$

If the limit exists for every $h\in U$ and every $h\in F$ then one can define a map
$$
DP: U \times F \to G
$$
If the limit exists and is jointly continuous in both variables we say that $P$ is continuous differentiable or $C^1$.

A simple, but nontrivial example is the operator 
$$
P: C^{\infty}[a, b] \to C^{\infty}[a, b]
$$
$$
P(f) := f f'
$$
with the derivative
$$
DP(f) h = f'h + f h'
$$

In the context of [[Fréchet space]], it may be that the directional derivative in every direction exists but the Fr&#233;chet derivative does not; however the existence of Fr&#233;chet derivative implies the existence of directional derivatives in all directions. 

The notion of directional derivatives extends to smooth manifolds (including infinite-dimensional) using local cooridnates; the differentiability does not depend on the choice of a local chart. 

See also [[Fréchet space]].

* wikipedia [G&#226;teaux derivative](http://en.wikipedia.org/wiki/G%C3%A2teaux_derivative)
* [[eom]]: [G&#226;teaux derivative](http://eom.springer.de/g/g043360.htm), [G&#226;teaux variation](http://eom.springer.de/G/g043390.htm), [Ren&#233; G&#226;teaux](http://en.wikipedia.org/wiki/Ren%C3%A9_G%C3%A2teaux)
* R. G&#226;teaux, _Sur les fonctionnelles continues et les fonctionnelles analytiques_, C.R. Acad. Sci. Paris S&#233;r. I Math. __157__ (1913)  pp. 325&#8211;327; _Fonctions d'une infinit&#233;s des variables ind&#233;pendantes_,  Bull. Soc. Math. France __47__  (1919) 70&#8211;96, [numdam](http://www.numdam.org/item?id=BSMF_1919__47__70_1); _Sur diverses questions du calcul fonctionnel_, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France tome __50__ (1922) 1&#8211;37, [numdam](http://www.numdam.org/item?id=BSMF_1922__50__1_0)
[[!redirects Gâteaux derivative]]
[[!redirects Gateaux derivative]]