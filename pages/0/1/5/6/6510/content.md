# Contents
* table of contents
{: toc}

## Idea 

In any [[Lie algebra]] we can define the **triple commutator** of three elements by 

$$ [a,b,c] = [[a,b],c], $$

and this obeys axioms which form the definition of a **Lie triple system**.  Furthermore, the space of elements of odd degree in any $\mathbb{Z}/2$-graded [[Lie algebra]] forms a Lie triple system, and thus so does the tangent space of a [[symmetric space]] at any point.

## Definition 

A **Lie triple system** is a vector space $V$ equipped with a trilinear map $[\cdot,\cdot,\cdot] \colon V \times V \times V \to V$ obeying the following three identities:

$$ [u,v,w] = -[v,u,w] $$

$$ [u,v,w] + [w,u,v] + [v,w,u] = 0 $$

$$ [u,v,[w,x,y]] = [[u,v,w],x,y] + [w,[u,v,x],y] + [w,x,[u,v,y]]. $$

The first two identities abstract the [[skew symmetry]] and [[Jacobi identity]] for the triple commutator in a Lie algebra. The third identity, which also holds for the triple commutator in a Lie algebra, says that the linear map $L_{u,v} \colon L \times L \to L$ defined by $L_{u,v}(w) = [u,v,w]$, is a derivation of of the triple product, in the following sense:

$$ L_{u,v}[w,x,y] = [L_{u,v} w, x, y] + [w, L_{u,v} x, y] + [w, x, L_{u,v} y] .$$

The identity also implies that the space of linear operators 

$$ \mathfrak{g}_0 = \text{span}\{L_{u,v}: u, v \in V \} $$ 

is closed under commutators, hence a Lie algebra.

## Relation to $\mathbb{Z}/2$-graded Lie algebras

Given any Lie algebra $\mathfrak{g}$ and any linear subspace $V \subseteq \mathfrak{g}$ closed under the triple commutator

$$ [u,v,w] = [[u,v], w] ,$$

$V$ becomes a Lie triple system.  Thus, given a $\mathbb{Z}/2$-graded Lie algebra (not a Lie superalgebra, an ordinary Lie algebra with a $\mathbb{Z}/2$ grading), say $\mathfrak{g} = \mathfrak{g}_0 \oplus \mathfrak{g}_1$, the space $\mathfrak{g}_1$ of odd elements becomes a Lie triple system.   

Conversely, given any Lie triple system $V$, if we define 

$$ \mathfrak{g}_0 = \text{span}\{L_{u,v}: u, v \in V \} $$ 

$$ \mathfrak{g}_1 = V $$

then $\mathfrak{g} = \mathfrak{g}_0 \oplus \mathfrak{g}_1$ becomes a $\mathbb{Z}/2$-graded Lie algebra with bracket given by

$$ [(L,u),(M,v)] = ([L,M]+L_{u,v}, L(v) - M(u)) $$

for $L,M \in \mathfrak{g}_0, u,v \in \mathfrak{g}_1$.

These two constructions define adjoint functors between the category of Lie triple systems and $\mathbb{Z}/2$-graded Lie algebras (CHECK).  However, this adjunction is not an equivalence, since if we start with any abelian $\mathbb{Z}/2$-graded Lie algebra, convert it into a Lie triple system, and then convert that back into a $\mathbb{Z}/2$-graded Lie algebra, the space of even elements is zero-dimensional.

## References

* William G. Lister, _A structure theory of Lie triple systems_, Trans. Amer. Math. Soc. __72__ (1952), 217-242, [doi](http://dx,doi.org/10.1090/S0002-9947-1952-0045702-9), [pdf](http://www.ams.org/journals/tran/1952-072-02/S0002-9947-1952-0045702-9/S0002-9947-1952-0045702-9.pdf) 
* Florian Girelli, _[[Snyder space]]-time: K-loop and Lie triple system_, SIGMA Symmetry Integrability Geom. Methods Appl. __6__ (2010), Paper 074, 19 pp. [journal](http://www.emis.de/journals/SIGMA/2010/074) [pdf](http://www.emis.de/journals/SIGMA/2010/074/sigma10-074.pdf) [arxiv/1009.4762](http://arxiv.org/abs/1009.4762)
* [[Nathan Jacobson]], _Lie and Jordan triple systems_, American Journal of Mathematics, __71__ (1949) 149–170, [jstor](https://www.jstor.org/stable/2372102).  In: Nathan Jacobson, Collected Mathematical Papers. Contemporary Mathematicians. Birkhäuser Boston 1989 [doi](https://doi.org/10.1007/978-1-4612-3694-8_2) 