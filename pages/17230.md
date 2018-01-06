

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Idea

In [[perturbative quantum field theory]] the _Schwinger-Dyson equation_ equates, [[on-shell]], the [[time-ordered product]] of the [[functional derivative]] of the [[action functional]] $S$ and another [[observable]] $A$ with the [[time ordered product|time ordering]] of the corresponding [[functional derivative]] of just $A$ itsels, times $i \hbar$:

$$
  \mathcal{T}
  \left(
    \underset{\Sigma}{\int}
      \frac{\delta S}{\delta \mathbf{\Phi}^a(x)}
      \cdot
      A^a(x)
      \, dvol_\Sigma(x)
  \right)
  \;=\;
  i \hbar
  \mathcal{T}
  \left(
    \underset{\Sigma}{\int}
    \frac{\delta A^a(x)}{\delta \mathbf{\Phi}^a(x)}
    \,
    dvol_\Sigma(x)     
  \right)  
  \phantom{AAA}
  \text{on-shell}
  \,.
$$

(e.q. [Rejzner 16, remark 7.](#Rejzner16)).

Traditionally this is displayed before spacetime-smearing of observables in terms of [[operator products]] of [[operator-valued distributions]] 

$$
  A^a(x) 
    \;\coloneqq\;
  \delta(x-x_0) \delta^a_{a_0} 
  \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
$$

in which case the first term above becomes

$$
  \underset{\Sigma}{\int}
    A^a(x) 
    \frac{\delta S'}{\delta \mathbf{\Phi}^a(x)}
   \, dvol_\Sigma
   \;=\;
  \frac{\delta S'}{\delta \mathbf{\Phi}^{a_0}(x_0)}
  \cdot 
  \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
$$

while the second becomes

$$
  \underset{\Sigma}{\int}
    \frac{\delta A^a (x)}{\delta \mathbf{\Phi}^a(x)}
  \, dvol_\Sigma
  \;=\;
  \mathbf{\Phi}^{a_1}(x_1)
    \cdots
  \mathbf{\Phi}^{a_{k-1}}(x_{k-1})
    \cdot
  \delta(x_0 - x_k) \delta^{a_0}_{a_k}
    \cdots
  \mathbf{\Phi}^{a_{k+1}}(x_{k+1})
    \cdots
  \mathbf{\Phi}^{a_n}(x_m)
$$

so that now the [[distribution|distributional]] [[Schwinger-Dyson equation]] reads

$$
  \mathcal{T}
  \left(
    \frac{\delta S'}{\delta \mathbf{\Phi}^{a_0}(x_0)}
      \cdot 
    \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
  \right)
  \;=\;
  i \hbar
  \mathcal{T}\left( 
    \mathbf{\Phi}^{a_1}(x_1)
      \cdots
    \mathbf{\Phi}^{a_{k-1}}(x_{k-1})
      \cdot
    \delta(x_0 - x_k) \delta^{a_0}_{a_k}
      \cdots
    \mathbf{\Phi}^{a_{k+1}}(x_{k+1})
      \cdots
    \mathbf{\Phi}^{a_n}(x_m)
  \right)
$$

(e.q. [Dermisek 09](#Dermisek09))

In particular this means that if $(x_0,a_0) \neq (x_k, a_k)$ for all $k \in \{1,\cdots ,n\}$

## Related concepts

* [[path integral]]

* [[Feynman diagram]]

## References

The traditional informal account in terms of [[path integral]]-heuristics is discussed for instance in

* {#Dermisek09} [[Radovan Dermisek]], _Schwinger-Dyson equations_, 2009  ([pdf](http://www.physics.indiana.edu/~dermisek/QFT_09/qft-II-4-4p.pdf))

A rigorous derivation in [[causal perturbation theory]]/[[pAQFT]] is discussed in

* {#Rejzner16} [[Katarzyna Rejzner]], p. 152 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


[[!redirects Schwinger-Dyson equations]]

[[!redirects Dyson-Schwinger equation]]
[[!redirects Dyson-Schwinger equations]]

