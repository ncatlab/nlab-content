In any [[2-category]] $K$, a morphism $f:A\to B$ is called **eso** if for any [[ff morphism]] $m:C\to D$, the following square is a [[2-categorical limit|(bicategorical)]] pullback:
$$\array{K(B,C) & \to & K(B,D)\\
\downarrow & & \downarrow \\
K(A,C) & \to & K(A,D)}$$
One easily checks that in [[Cat]] this is equivalent to $f$ being an [[essentially surjective functor]].

# Remarks #

* If $K$ has finite limits, then $f:A\to B$ is eso if and only if whenever $f\cong m g$ where $m$ is ff, then $m$ is an [[equivalence]].

* Any coinserter, co-isoinserter, coinverter, coequifier, or (lax or oplax) codescent morphism is eso.

* If $K$ has finite limits and $f:A\to B$ is eso, then for any $Z$ the functor $K(B,Z)\to K(A,Z)$ is [[faithful functor|faithful]] and [[conservative functor|conservative]].
