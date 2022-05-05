

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

In [[physics]] ([[field theory]]) a _local observable_ is an [[observable]] which is an average of a function of the values of the [[field (physics)|fields]] and their [[derivatives]] at each fixed spacetime point.

If $\Phi$ is a [[field (physics)|field configuration]] over some [[spacetime]] $\Sigma$ then a local observable is a function of $\Phi$ which, assigns values of the form

$$
  \Phi
    \;\mapsto\;
  \int_\Sigma f(\Phi(x), \nabla \Phi(x), \nabla^2 \Phi(x), \cdots) b(x) dvol_\Sigma(x)
$$

where $f$ is some [[smooth function]] of its arguments and $b$ is some [[bump function]] on [[spacetime]].

This is in contrast to an observable which combines the values of fields at different spacetime points other than by forming spacetime averages. For instance if $x \neq y \in \Sigma$ are two distinct spacetime points, then 


$$
  \Phi \mapsto \Phi(x) \Phi(y)
$$

is a smooth function on the space of fields, hence an [[observable]], but it is not a local observables.

More in detail, if 

$$
  \array{
    E 
    \\
    \downarrow^{\mathrlap{fb}}
    \\
    \Sigma
  }
$$

is a [[fiber bundle]] regarded as the [[field bundle]] that defines the given [[field theory]], then a local observables is a function on the the space of field configurations, hence the [[space of sections]] $\Gamma_\Sigma(E)$ (or else on the subspace of those which solve the [[equations of motion]], the [[shell]]) which arises as the [[transgression of variational differential forms|transgression]] of a [[horizontal differential form]] of degree $dim(\Sigma)$ on the [[jet bundle]] $J^\infty_\Sigma(E)$ of $E$.

Products of local observables are called _multilocal observables_.

[[!include perturbative observables -- table]]

## Definition

For the moment see at _[[geometry of physics -- A first idea of quantum field theory]]_ [this def.](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#LocalObservables)

## Properties


+-- {: .num_example #PolynomialLocalObservablesArePolynomialObservables}
###### Example
**([[polynomial]] [[local observables]] are [[polynomial observables]])**

A [[local observable]] which comes form a [[variational differential form|horizontal differential form]] which is a [[polynomial]] in the fields and their jets times the [[volume form]] on [[spacetime]] is a [[polynomial observable]].

These happen to be also [[microcausal observables]] ([this example](microcausal+functional#CompactlySupportedPolynomialLocalDensities)).

=--

The resultiing inclusion

$$
  LocPolyObs(E) \hookrightarrow PolyObs(E)_{cm}
$$

of the local polynomial observables into the [[microcausal polynomial observables]] is a [[dense subspace]]-inclusion. ([Fredenhagen-Rejzner 12, p. 23](#FredenhagenRejzner12))



## Related concepts



* [[Wick algebra]]


## References

* {#BrunettiFredenhagen09} [[Romeo Brunetti]], [[Klaus Fredenhagen]], section 5.4.1 of _Quantum Field Theory on Curved Backgrounds_, chapter 5 in [[Christian Bär]], [[Klaus Fredenhagen]] (eds.), _Quantum Field Theory on Curved Spacetime_, Springer 2009

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], section 3.2 of_Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

* {#FredenhagenRejzner12} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative algebraic quantum field theory_, In _Mathematical Aspects of Quantum Field Theories_, Springer 2016 ([arXiv:1208.1428](https://arxiv.org/abs/1208.1428))

* {#Rejzner16} [[Katarzyna Rejzner]], def. 3.14 in _[[Perturbative Algebraic Quantum Field Theory]]_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


* {#Duetsch18} [[Michael Dütsch]], def. 1.2 in _[[From classical field theory to perturbative quantum field theory]]_, 2018


[[!redirects local observables]]

[[!redirects multilocal observable]]
[[!redirects multilocal observables]]
