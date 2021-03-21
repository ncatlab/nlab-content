
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An [[object]] in an [[(∞,1)-topos]] is said to have _cohomological dimension_ $\leq n$ if all [[cohomology group]]s of degree $k \gt n$ vanish on that object.

## Definition

+-- {: .num_defn}
###### Definition

For $\mathbf{H}$ an [[(∞,1)-topos]] and $n \in \mathbb{N}$ , an [[object]] $X \in \mathbf{H}$ is said to have **cohomological dimension $\leq n$** if for all [[Eilenberg-MacLane object]]s $\mathbf{B}^k A$ for $k \gt n$ the [[cohomology]] of $X$ with these coefficients vanishes:


$$
  H^k(X, A) := \pi_0 \mathbf{H}(X,\mathbf{B}^k A) \simeq *
  \,.
$$ 

We say the [[(∞,1)-topos]] $\mathbf{H}$ itself has cohomological dimension $\leq n$ if its [[terminal object in an (∞,1)-category|terminal object]] does.

=--

This appears as [[Higher Topos Theory|HTT, def. 7.2.2.18]].

## Properties


+-- {: .num_prop}
###### Proposition

If $\mathcal{X}$ has [[homotopy dimension]] $\leq n$ then it also has cohomology dimension $\leq n$.

The converse holds if $\mathcal{X}$ has finite homotopy dimension an $n \geq 2$. 

=--

This appears as [[Higher Topos Theory|HTT, cor. 7.2.2.30]].



## Related concepts

[[!include notions of dimension -- contents]]




## References

The general $(\infty,1)$-topos-theoretic notion is discussed in section 7.2.2 of

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_






[[!redirects cohomology dimension]]

