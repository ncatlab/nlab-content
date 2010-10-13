

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **local geometric morphism** $f : E \to S$ between [[topos]]es $E,S$ is 

* a [[geometric morphism]]

  $$
    (f^* \dashv f_*) : E \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}
    {\to}}  S
  $$

* such that a further [[right adjoint]] $f^! : E \to S$ exists 

  $$
    (f^* \dashv f_* \dashv f^!) : 
    E
    \stackrel{\overset{f^*}{\leftarrow}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    S
  $$


If $f : E \to S$ is the [[global section]] geometric morphism in the category of toposes over $S$, then we say that $E$ is a **local topos**.


## Examples

### Sheaves on $CartSp$

Let $E = Sh(CartSp)$ be the [[gros topos]] of [[sheaves]] on the [[site]] [[CartSp]] of [[Cartesian space]]s with the [[good open cover]] [[coverage]]. This is a local topos.

The further right adjoint
is 

$$
  Codisc : Set \to Sh(CartSp)
$$

the functor that sends a set to the [[diffeological space]] on that set with _codiscrete_ smooth structure (every map of sets is smooth). 

(Thanks to [[David Carchedi]].)


## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* **local topos** / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]


## References

* [[Peter Johnstone]], [[Ieke Moerdijk]], _Local maps of toposes_  Proc. London Math. Soc.  (1989)   s3-58  (2):  281-305.  ([pdf](http://plms.oxfordjournals.org/content/s3-58/2/281.full.pdf+html))



[[!redirects local geometric morphisms]]

[[!redirects local topos]]