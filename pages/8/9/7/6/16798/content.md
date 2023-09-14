
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a [[smooth function|smooth]] [[bundle]] $E \to \Sigma$, then a [[differential form]] on its [[jet bundle]] $J^\infty_\Sigma(E)$ is called a _source form_ if it is of vertical degree 1 (with respect to the [[variational bicomplex]]) and its evaluation on a [[vector field]] depends only on the projection of that vector field to a vector field on $E$ itself (e.g. [Zuckerman 87, p. 6](#Zuckerman87)):

$$
  \Omega^{k,1}_{\Sigma,source}(E)
  \;\coloneqq\;
  \Omega^{k,0}_\Sigma(E) \wedge \delta C^\infty(E) 
  \,.
$$

## In variational calculus

Given a [[local Lagrangian]] $\mathbf{L}$, i.e. a horizontal form on $Jet(E)$ of maximal horizontal degree, then there is a unique source form $\mathbf{E}$ such that 

$$
  d \mathbf{L} = \mathbf{E} - d_H \theta
$$

for some form $\theta$. This $\mathbf{E}$ is the [[Euler-Lagrange form]] of $\mathbf{L}$. 

The sum

$$
  \rho \coloneqq \mathbf{L} + \theta
$$

is the corresponding [[Lepage form]].

## Related concepts

* [[variational bicomplex]]

* [[evolutionary vector field]], [[evolutionary derivative]]

## References

* {#Zuckerman87} [[Gregg J. Zuckerman]], *Action principles and global geometry*, in: [[Shing-Tung Yau]] (ed.) *Mathematical Aspects of String Theory*, World Scientific (1987) 259-284 &lbrack;[[ZuckermanVariation.pdf:file]], [doi:10.1142/0383](https://doi.org/10.1142/0383)&rbrack;

[[!redirects source forms]]