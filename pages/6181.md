
## Idea

Let $X$ be a [[finite homotopy type|finite]] [[CW complex]]
and $X \subseteq S^{n+1}$. Then there is a map

$$ X \times (S^{n+1}\backslash X) \to S^n,\,\,\,\,\,\, (x,y) \mapsto \frac{x-y}{\|x - y\|}.$$

This element determines an element
$$\delta \in H^n( X \times (S^{n+1}\backslash X)).$$

In [[topology]] there is a [[slant product]] operation, sort of _dividing_,
and in this case one can do slant product with $\delta$.
This way one obtains a map
$$
\delta_{/}  : H_{i}(X)\to H^{n-i}(S^{n+1}\backslash{X}).
$$

This map is an isomorphism and it is called the __Alexander-&#268;ech duality__ (or sometimes simply Alexander duality).
It can be considered for infinite complexes as well, but in that
case one has to change the flavour of (co)homology theories
involved. $H_i$ is then the **Steenrod-Sitnikov homology**
and $H^{n-i}$ has to be cohomology (?).

The [[Spanier-Whitehead duality]] is a generalization, where $S^{n+1}\backslash X$ is
replaced by any space $D_n(X)$, together with an element
$\delta$ such that the corresponding map

$$\delta_/ : H_i(X) \to H^{n-i}(\mathcal{D}_n X)$$

is an isomorphism. It follows that one may replace $\mathcal{D}_n X$ by its
suspension and so on, hence the stable homotopy theory is
a natural setup for this duality.


## References

Named after [[James W. Alexander]] and [[Eduard Čech]].

[[!redirects Alexander duality]]
