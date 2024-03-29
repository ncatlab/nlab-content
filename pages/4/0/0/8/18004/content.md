
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

In [[analysis]], _uniform convergence_ refers to a type of [[convergence]] of [[sequences]] $(f_n)_{n \in \mathbb{N}}$ of [[functions]] $f_n \colon X \to \mathbb{R}$  into the [[real numbers]]. In terms of [[epsilontic analysis]] such a sequence converges uniformly to some function $f \colon X \to \mathbb{R}$ if for each [[positive real number]] $\epsilon \gt 0$ there exists a [[natural number]] $N_\epsilon \in \mathbb{N}$ such that if $n \geq N(\epsilon)$ then for _all_ points $x \in X$ the difference (in [[absolute value]]) between the value of $f_n$ at that point and that of $f$ at that point is smaller than $\epsilon$:

$$
  \underset{\epsilon \gt 0}{\forall} 
   \;
  \underset{N(\epsilon) \in \mathbb{N}}{\exists}
   \;
  \underset{n \geq N(\epsilon)}{\forall}
   \;
  \underset{x \in X}{\forall}  
   \;
  \,
  \vert f_n(x) - f(x) \vert \lt \epsilon
  \,.
$$

What is _uniform_ about this convergence is that the bound $N(\epsilon)$ is required to work for all $x \in X$ (hence uniformly over $x$). This is in contrast to [[pointwise convergence]] where one allows a different bound $N$ to exist for each $\epsilon$ and each point $x \in X$ separately. Since for non-[[finite set|finite]] $X$ the [[maximum]] of all such local choices of $N$ in general does not exist, uniform convergence is a stronger condition than [[pointwise convergence]].

## Examples

+-- {: .num_prop #FunctionsUniformCauchySequence}
###### Proposition

Let 

1. $X$ be a [[set]];

1. $Y$ a [[complete space|complete]] [[metric space]].

Consider the set $F(X,Y)$ of [[functions]] $X \to Y$ as a [[metric space]] via the [[supremum norm]]. Then this is again [[complete space|complete]]: every [[Cauchy sequence]] of functions converges uniformly.

If $X$ is equipped with the structure of a [[topological space]] and if the Cauchy sequence of functions consist of [[continuous functions]], then also the [[limit of a sequence|limit]] function is continuous.

=--

(e.g. [Gamelin-Greene 83, theorem I 2.5 and II 3.5](#GamelnGreene83))


## Related concepts

* [[pointwise convergence]]

* [[uniformly continuous map]]

* [[uniform property]]

* [[topology of uniform convergence]]

## References

* Wikipedia, _[Uniform convergence](https://en.wikipedia.org/wiki/Uniform_convergence)_

## References

* {#GamelinGreene83} Theodore Gamelin, Robert Greene, _Introduction to Topology_, Dover (1983, 199)

