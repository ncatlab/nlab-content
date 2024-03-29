
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
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

+-- {: .num_defn}
###### Definition

We say an object $X$ is **$n$-concrete** if the canonical morphism 
$X \to coDisc \Gamma X$ is [[n-truncated|(n-1)-truncated]].

If a [[0-truncated]] object $X$ is $0$-concrete, we call it just **concrete**.


=--


+-- {: .num_prop}
###### Proposition

For $C$ an [[∞-cohesive site]], a 0-truncated object in the 
[[(∞,1)-topos]] over $C$ is concrete precisely if it is
a [[concrete sheaf]] in the traditional sense.

=--

+-- {: .num_defn #NConcretification}
###### Definition

For $X \in \mathbf{H}$ and $n \in \mathbb{N}$, the 
**$(n+1)$-concretification** of $X$ is the morphism

$$
  X \to conc_{n+1} X
$$

that is the left factor in the decomposition with respect to the 
[[n-connected/n-truncated factorization system]] of the 
$(\Gamma \dashv coDisc)$-[[unit of an adjunction|unit]]

$$
  \array{   
    && conc_{n+1} X
    \\
    & \nearrow && \searrow
    \\
    X &&\to&& coDisc \Gamma X
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

By that very [[n-connected/n-truncated factorization system]]
we have that $conc_{n+1} X$ is an ${n+1}$-concrete object.

=--




## Examples

* [[concrete smooth ∞-groupoid]]

## Related concepts

* [[concrete sheaf]]

* **concrete $(\infty,1)$-sheaf**

## References

This entry goes back to some observations by [[David Carchedi]].

[[!redirects concrete (∞,1)-sheaves]]
[[!redirects concrete (∞,1)-sheaf]]
