
In [[analysis]], _uniform convergence_ refers to a type of [[convergence]] of [[sequences]] $(f_n)_{n \in \mathbb{N}}$ of [[functions]] $f_n \colon X \to \mathbb{R}$  into the [[real numbers]]. In terms of [[epsilontic analysis]] such a sequence convrges uniformly to some function $f \colon X \to \mathbb{R}$ if for each [[positive real number]] $\epsilon \gt 0$ there exists a [[natural number]] $N_\epsilon \in \mathbb{N}$ such that if $n \geq N(\epsilon)$ then for _all_ points $x \in X$ the difference (in [[absolute value]]) between the value of $f_n$ at that point and that of $f$ at that point is smaller than $\epsilon$:

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

What us _uniform_ about this convergence is that the bound $N(\epsilon)$ is required to work for all $x \in X$ (hence uniformly over $x$). This is in contrast to [[pointwise convergence]] where one allows a different bound $N$ to exist for each $\epsilon$ and each point $x \in X$ separately. Since for non-[[finite set|finite]] $X$ the [[maximum]] of all such local choices of $N$ in general does not exist, uniform convergence is a stronger condition than [[pointwise convergence]].


## References

* Wikipedia, _[Uniform convrgence](https://en.wikipedia.org/wiki/Uniform_convergence)_

