
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Inside a [[local (∞,1)-topos]] $\mathbf{H}$ there are objects that may be thought of as [[∞-groupoid]]s equipped with [[stuff, structure, property|extra structure]] ("cohesive structure" if $\mathbf{H}$ is even a [[cohesive (∞,1)-topos]]). These are the _concrete objects_ in $\mathbf{H}$.

## Definition

Let $\mathbf{H}$ be a [[local (∞,1)-topos]]. 

$$
  \mathbf{H}
  \stackrel{\stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}}{\underset{Codisc}{\leftarrow}}
  \infty Grpd
  \,.
$$

Since $Codisc$ is by definition a [[full and faithful (∞,1)-functor]] this means that 

$$
  \infty Grpd
  \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  \mathbf{H}
$$

is a [[geometric embedding]]. By the discussion at [[reflective sub-(∞,1)-category]] this means that $\Gamma$ is the [[localization of an (∞,1)-category]] at a class $S \in Mor \mathbf{H}$ of [[morphism]]s.  It factors therefore canonically through the [[(∞,1)-quasitopos]] of $S$-separated $(\infty,1)$-sheaves

$$
  \infty Grpd
   \stackrel{\overset{\Gamma}{\leftarrow}}{\hookrightarrow}   
  Conc(\mathbf{H})
   \stackrel{\overset{concretize}{\leftarrow}}{\hookrightarrow}
   \mathbf{H}
  \,.
$$

We call $Conc(\mathbf{H})$ the [[(∞,1)-quasitopos]] of **concrete objects** of the local $(\infty,1)$-topos $\mathbf{H}$.

## Related concepts

* [[concrete sheaf]]

* **concrete $(\infty,1)$-sheaf**

## References

This entry goes back to some observations by [[David Carchedi]].

[[!redirects concrete (∞,1)-sheaves]]
[[!redirects concrete (∞,1)-sheaf]]
