\tableofcontents

## Definition

(Definition 2.1 in Bhatt–Scholze.)

Fix a prime $p$.
A __δ-ring__ is a pair $(R,\delta)$,
where $R$ is a [[commutative ring]]
and $\delta\colon R\to R$ is a map of underlying sets
such that $\delta(0)=0$, $\delta(1)=0$,
$$\delta(x y)=x^p \delta(y)+y^p \delta(x) + p\delta(x)\delta(y),$$
and
$$\delta(x+y)=\delta(x)+\delta(y)+(x^p+y^p-(x+y)^p)/p.$$

## Properties

If $(R,\delta)$ is a δ-ring,
then the map $\phi\colon R\to R$
given by $\phi(x)=x^p + p\delta(x)$
is a ring homomorphism
that lifts the [[Frobenius endomorphism]] on $R/p$.

For $p$-torsionfree rings,
the above correspondence between δ-structures
and lifts of the Frobenius endomorphism on $R/p$ to $R$
is bijective.
This motivates the identities in the definition of a δ-structure.

## Related entries

* [[perfectoid ring]]

* [[perfectoid space]]

* [[prism]]

* [[prismatic cohomology]]

## References

The original notion is due to [[André Joyal]]:

* [[André Joyal]], δ-anneaux et vecteurs de Witt, C. R. Math. Rep. Acad. Sci. Canada 7 (1985), no. 3, 177–182.


Recent developments can be found in

* [[Bhargav Bhatt]], [[Peter Scholze]], _Prisms and prismatic cohomology_, [arXiv](http://arxiv.org/abs/1905.08229v3).