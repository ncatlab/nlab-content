
#Contents#
* table of contents
{:toc}

## Idea

A formal difference (with respect to [[direct sum]]/[[Whitney sum]]) of [[vector bundles]]. Appears as representative for classes in [[topological K-theory]]. A virtual vector bundle $[E] - [F]$ has a _virtual rank_ $rk([E]-[F])$, which is the integer $rk(E) - rk(F)$.

## Properties

+-- {: .num_prop} 
###### Proposition 
Let X be a space that is locally compact and regular. Then any virtual vector bundle of virtual rank 0 has some tensor power that is 0 in K-theory.
=-- 

The following argument comes from ([Karoubi 1978](#Karoubi78), Theorem II.5.9), but generalised to take into account non-compact spaces which are introduced in the following pages.

+--{: .proof}
###### Proof
For closed subsets $Y_1$ and $Y_2$, then the ring structure on K-theory means
$$
K_{Y_1}(X)\cdot K_{Y_2}(X) \subset K_{Y_1\cap Y_2}(X)
$$
where $K_{Y_i}(X) := ker(K(X) \to K(Y_i))$. We can likewise consider the same for a sequence $Y_1,\ldots ,Y_n$.

If $e = [E] - [\underline{rk(E)}]$ is in $ker(rk)$ (i.e. reduced K-theory $\tilde K(X)$) with $supp(e)$ in some compact set $C$ (recall that vector bundle K-theory elements are differences of vector bundles that are isomorphic outside a compact set. Without loss of generality such an element can be represented as $[E] - [\underline{V}]$ where $\underline{V}$ is a trivial bundle with fibre $V$), cover $C$ by finitely many closed neighbourhoods $Y_1,\ldots ,Y_n$ over which $E$ trivialises. Thus $e$ is in $K_{Y_i}(X)$ for each $i=1,\ldots n$.

Thus $e$ is in the intersection of all the $K_{Y_i}(X)$ as well as $K_Z(X)$ for $Z$ the complement of $supp(e)$. Thus $e^{n+1}$ is in $K_{\cup Y_i \cup Z}(X) = K_X(X) = 0$.

Hence for every element in $ker(rk)$, some power of it is zero, hence $ker(rk)$ is a [[ideal|nil ideal]].
=-- 




## Related concepts

* [[virtual representation]]

## References

* {#Karoubi78} [[Max Karoubi]], _K-Theory: An Introduction_, Grundlehren der mathematischen Wissenschaften 226, (1978) Springer-Verlag

[[!redirects virtual vector bundles]]

[[!redirects virtual vector space]]
[[!redirects virtual vector spaces]]