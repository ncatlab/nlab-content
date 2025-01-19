
## Idea

Length is the [[volume]] of [[curves]].

## Definition

Let $(X,d)$ be a [[metric space]], and let $c:[0,1]\to X$ be a continuous [[curve]]. The **length of $c$** is the [[number]] (possibly [[infinite]]) given by 
$$
|c| \;\coloneqq\; \sup_{n, t_0,\dots,t_n} \sum_{i=1}^n d\big( c(t_{i-1}), c(t_i)\big),
$$
where the [[supremum]] is taken over all finite [[partitions]] of the interval $0=t_0 \le t_1\le \dots\le t_n =1$.

### For Riemannian manifolds

If $X$ is a [[Riemannian manifold]] (with the induced metric) and $c$ is a [[smooth]] curve, the length of $c$, sometimes called the **arc length**, is equivalently given by the formula
$$
|c| \;=\; \int_0^1 |c'(t)|\,d t,
$$
where $c'(t)$ is the [[tangent vector]], and $|c'(t)|$ its length, given in terms of the [[Riemannian metric]].

## Examples

* [[circumference of a circle]]

## Related concepts

* [[area]]

* [[volume]]

* [[curve]]

* [[length scale]]

* [[wave length]]

* [[Planck length]]

* [[Compton wavelength]]

* [[string length]]

[[!redirects lengths]]