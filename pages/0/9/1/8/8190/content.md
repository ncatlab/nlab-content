
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The formalism of _de Donder-Weyl_ is a formulation of [[variational calculus]] related to [[multisymplectic geometry]].

For $L$ a [[local Lagrangian]] of fields $\{\phi^i\}$ on a space $\Sigma$, and their first derivatives $\partial_\mu \phi^i$, the [[Euler-Lagrange equations]]

$$
  \partial_\mu
  \frac{\delta L }{\delta (\partial_\mu \phi^i)} 
   = 
  \frac{\delta L}{ \delta \phi^i}
$$

are equivalently rewritten, under the generalized [[Legendre transform]] (if it exists)

$$
  H := \pi^\mu_i \partial_\mu \phi^i - L
$$


(with $\pi^\mu_i$ the "$\mu$-th [[momentum]] of the $i$-th field" )
as the first-order system of "covariant" [[Hamilton equations]]

$$
  \partial_\mu \phi^i
    =
  - \frac{\delta H}{\delta \pi_i^\mu} 
  \,,
  \;\;\;\;
  \partial_\mu \pi^\mu_i
   =
  \frac{\delta H}{ \delta \phi^i} 
  \,.
$$

This $H$ is also called the _de Donder-Weyl Hamiltonian_.

In terms of the [[multisymplectic form]]

$$
  \Omega 
   \coloneqq 
   \mathbf{d} \pi^\mu_i \wedge  \mathbf{d} \phi^i  
   \wedge (\iota_{\partial_\mu} vol_\Sigma) 
    + 
    \mathbf{d} H \wedge vol_\Sigma
$$

the critical field configurations are precisely those whose top-degree multi-tangent spaces annihilate $\Omega$.

(...)

## Related concepts

* [[Hamiltonian n-vector field]]


## References

Reviews include

* Wikipedia, _[De Donder-Weyl theory](http://en.wikipedia.org/wiki/De_Donder%E2%80%93Weyl_theory)_

* Narciso Rom&#225;n-Roy, _Multisymplectic Lagrangian and Hamiltonian Formalisms of Classical Field Theories_, SIGMA 5 (2009), 100 ([journal](http://www.emis.de/journals/SIGMA/2009/100/), [arXiv:math-ph/0506022](http://arxiv.org/abs/math-ph/0506022)) 

* [[Frédéric Hélein]], _Hamiltonian formalisms for
multidimensional calculus of variations and perturbation theory_, ([arXiv:math-ph/0212036](http://arxiv.org/abs/math-ph/0212036))

See also

* I.V. Kanatchikov, _DeDonder-Weyl theory and a hypercomplex extension of quantum mechanics to field theory_ , ([arXiv:hep-th/9810165](http://arxiv.org/abs/hep-th/9810165))


For more see the references at _[[multisymplectic geometry]]_.

[[!redirects de Donder-Weyl hamiltonian]]
[[!redirects de Donder-Weyl Hamiltonian]]

