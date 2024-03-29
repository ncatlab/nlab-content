
#Contents#
* table of contents
{:toc}

##Overview##

We are interested in the local structure of zeros of [[analytic function]]s in $\mathbb{C}^n$ as well as in analogues, e.g. in [[rigid analytic geometry]]. 

In one variable, a holomorphic function $f$, locally holomorphic around $z_0$, can be represented as $f(z)=(z-z_0)^n u(z)$ where $u(z_0)\neq 0$, $u$ is holomorphic and $n$ is a [[natural number|nonnegative integer]]; therefore the solution set is discrete. In many variables, these zero sets are more complicated but far from arbitrary; in fact the analytic sets are often pretty close to [[algebraic varieties]]: for example, analytic subsets of the [[projective space]] are algebraic.

The Weierstrass preparation theorem and related facts (Weierstrass division theorem and Weierstrass formula) provide the most basic relations between [[polynomial]]s and holomorphic functions.

Let $n\geq 2$; then we separate the first $(n-1)$ complex coordinates $z = (z_1,\ldots,z_{n-1})$ and the $n$-th coordinate which will be denoted by $w$. We consider an analytic function $f = f(z_1,\ldots, z_{n-1},w)$ vanishing at origin $f(0,\ldots, 0)=0$, and such that it is not identically zero on the $w$-axis. 


##Weierstrass polynomial##

The __Weierstrass polynomial__ of $w$ is a polynomial of the form 
$$
w^d + a_1(z) w^{d-1}+\ldots+a_d(z),\,\,\,\,\,a_i(0)=0.
$$
The integer $d$ is called *the degree of the Weierstrass polynomial*.


## Weierstrass preparation theorem in $\mathbb{C}^n$##

Let $f$ be a function which is holomorphic in some neighborhood of origin $0\in\mathbb{C}^n$ and not identically equal to zero on the $w$-axis. Then there is a neighborhood of origin such that $f$ is *uniquely* representable in the form

$$
f = P\cdot h
$$

where $P$ is a Weierstrass polynomial of degree $d$ of $w$ and $h(0) \neq 0$.


##Weierstrass division theorem##

Let $\mathcal{O}_{n,a}$ be the [[local ring]] of [[germs]] of holomorphic functions at $a\in\mathbb{C}^n$ and $\mathcal{O}_n:=\mathcal{O}_{n,0}$. Let $g=g(z,w)\in\mathcal{O}_{n-1}[w]$ be a Weierstrass polynomial of degree $k$ of $w$. Then every holomorphic function $f\in\mathcal{O}_n$ can be represented as 
$$
f = g\cdot h+r
$$
where $r = r(z,w)$ is a polynomial of degree $\lt k$. 

As a corollary, if another function $h$ vanishes on the zero set of $f$, then $f$ divides $h$ in $\mathcal{O}_n$.


##Ingredients of proofs##

Weierstrass's original result considered the ring of holomorphic functions, and therefore used analytic methods such as the [[residue theorem]] and [[Cauchy integral formula]] are used. Analogous results are now known in the ring of formal power series, as well as for power series over non-Archimedean fields; in these settings, the proof can be made fully algebraic.

## References

Named after [[Karl Weierstraß]].

* Wikipedia, _[Weierstrass preparation theorem](https://en.wikipedia.org/wiki/Weierstrass_preparation_theorem)_

category: analysis, geometry