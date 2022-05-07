
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Integration theory
+-- {: .hide}
[[!include integration theory - contents]]
=--
=--
=--

# Integrals and integration
* table of contents
{: toc}

## Idea

_Integration_ is a process by which local data over a [[manifold]] or similar is _accumulated_ to an _integral_.

In its simplest form, this is a limiting notion of the process of forming [[sums]], known then as _[[Riemann integration]]_ or _[[Lebesgue integration]]_, where the integration pairs a [[function]] on a space against a _[[measure]]_ which indicates, roughly, how much a local contribution of the function contributes to the whole accumulation process.
Direct variants and refinements of this kind of integration is _[[integration of differential forms]]_ and similar.

The integration of differential forms induces a more general notion of integration, namely [[integration in differential cohomology]] and hence [[integration in generalized cohomology]]. Here the choice of a [[measure]] is replaced by a choice of _[[orientation in generalized cohomology]]_.

| analytic integration | cohomological integration |
|--|--|
| [[measure]] | [[orientation in generalized cohomology]] |
| [[Lebesgue integration]], [[integration of differential forms|of differential forms]] | [[push-forward in generalized cohomology]]/[[fiber integration in differential cohomology|in differential cohomology]] |


## Terminology

The quantity whose integral we are taking is the __integrand__.  Depending on context, we may view the integrand as a [[function]], a [[differential form]], a [[measure]], or otherwise.  The result of integrating the integrand is the __value__ of the integral.  The __integral__ itself may be thought of as its value, but also (especially if this value fails to exist as we would like) could mean the entire expression.  (Contrast this with the case of [[series]], where 'series' means the entire expression but 'sum' means the result of evaluating it.)  Thus, in $\int_a^b f(x) \,\mathrm{d}x$, any of $f$, $f(x)$, $f(x) \,\mathrm{d}x$, with or without the additional data of the set $[a,b]$ or the proposition $a \leq x \leq b$, may be thought of as the integrand.  The integral is $\int_a^b f(x) \,\mathrm{d}x$, which may be thought of as consisting of all of the data in this expression or as simply being the final result of evaluating the expression.

An integral of the type considered here is sometimes called a __definite integral__ to contrast with an [[indefinite integral|indefinite]] (or semidefinite) integral.  Whereas a definite integral is typically a number or some other definite quantity, an indefinite integral is typically another variable quantity of the same type as the integrand (or even more indefinitely, an equivalence class of such quantities).  Thus, $\int_a^b f(x) \,\mathrm{d}x$ is a definite integral, $\int_a f(x) \,\mathrm{d}x$ is a semidefinite integral, and $\int f(x) \,\mathrm{d}x$ is an indefinite integral.

__Integration__ in the most narrow sense is a process involved in defining or computing integrals.


## Analytic integration
 {#AnalyticIntegration}

### Generalizing sums
 {#GeneralizingSums}

A __[[sum]]__ $\sum_{s \in S} a_s$ is defined over a domain $S$ which is, as a rule, a _discrete_ set. This set is also typically fixed in the sense that no subdivision is assumed in its definition, except sometimes for convergence purposes. Thus a general sum takes two arguments: a set $S$ and a function on $S$ and outputs a value. In the case of sum of an infinite series the order may matter as the limiting procedure is taken into account.

An __integral__ is a generalization of a sum where the domain is typically not a discrete set, but some mathematical object, which may be (typically not in a single fixed way, but in many possible ways) approximated or split into pieces.
The function to be integrated over the range, 
is some object which is thought of
as living over the range, some sort of a cocycle or a distribution. 
The basic property from the integral is that it should behave nicely (typically additively in some sense) with respect to combining its values on pieces in the range and that, for a reasonable set of subdivisions the result should be the same (sometimes after passing to a limit). 

For a fixed range, integral is typically an operator/functional on a set/space of allowed objects over the range.  


### Integration as opposite to differentiation

Many integrals are supposed to be inverse to differentiation procedures of various kinds. Indeed, if integral is a generalization of a sum, then a difference between two partial sums is a value to be added at a step of summation, and its generalization is some sort of [[differentiation]]. Of course, the initial value has to be determined as the differentiation gives just a step of the addition.


### Solving differential equations and constraints

In some cases, one solves a differential equation by reducing it to a relation of the form $d F = g$ and then $F = \int g$. One says that the equation is
solvable in quadratures. Thus the integration is used in examples of solving differential equations and differential relations, hence finding objects satisfying some differential constraints is often also considered a sort of integration. For example, finding integral curves of vector fields and more generally finding integral submanifolds of distributions, is also called an integration. In this vain, also a Lie group is a global object which integrates a Lie algebra (indeed, infinitesimally this reduces to solving the Maurer-Cartan equations). For resolving differential relations there are solvability conditions/obstructions/constraints which are often of cohomological nature. There is sometimes a relation to [[rational homotopy theory]].


## Topological integration 
 {#TopologicaIntegration}

(...)

* [[integration in generalized cohomology]]
(...)


## Zoo of integrals and concepts of integration 

We list a bunch more notions of integration. Should eventually be turned into something more coherent...

See also [[measure theory]] (and [[measurable space]], [[measure space]]) which is a basis for many kinds of integrals, especially the [[Lebesgue integral]]. 

Basic kinds of integrals in (super)analysis: the [[Daniell integral]], the [[Riemann integral]] (possibly [[one-sided Riemann integral|upper or lower]], [[improper Riemann integral|improper]], or [[Henstock integral|generalised]]), the [[Lebesgue integral]], the [[Henstock integral]] (same as the generalised Riemann integral or the improper Lebesgue integral), the [[Stieltjes integral|Stieltjes]] variations of the above, the [[Berezin integral]], [[line integrals]].

Special examples of the above include the [[Batalin-Vilkovisky integral]], the [[Kontsevich integral]], the [[Selberg integral]],the [[elliptic Selberg integral]].

Integration is involved in [[integral transform]]s, [[integral transforms on sheaves]], in various formulas for pairings, e.g. of chains and cochains .... 
Some statements involving integrals include the [[Stokes theorem]].


A special topic includes some infinite-dimensional versions including the well-defined [[Wiener integral]] and the more problematic [[path integral]], cf. also

* [[fermionic path integral]],
* [[path integral as a pull-push transform]].

The basic problem with the path integral comes from the fact that there is no translation-invariant [[Lebesgue measure]] on an infinite-dimensional real vector space with a finite nonzero value on the unit ball.

* [[fiber integration]]

* in [[differential geometry]]

  *  [[differential forms]] are involved in integration over differentiable manifolds, see at _[[integration of differential forms]]_ ; more generally, one can integrate currents (cf. [[geometric measure theory]]

  * [[fiber integration in ordinary differential cohomology]]

*  in [[supergeometry]]

   * [[Berezin integral]]
  
   * [[integration over supermanifolds]]
* [[path integral]]
* [[Lie integration]] (the name comes from its relation to the integration of
differential equations and finding integral curves of 
vector fields and flows)

* stratified versions related to Grothendieck rings and valuations:
[[Euler integration]], [[motivic integration]]


## Properties

* [[Cauchy integral theorem]]

(...)


## Related concepts

* [[integrand]]

* [[closed midpoint algebra]]

* [[Lebesgue integration]]

* [[Lebesgue space]]

* [[integration of differential forms]]

* [[change of integration variables]]

* [[density]], [[volume form]]

* [[integration over infinite-dimensional manifolds]]

* [[fiber integration]], [[fiber integration in differential cohomology]]

* [[Gaussian integral]], [[Feynman diagram]]

* [[Lie integration]]

* [[geometric integration theory]]

* [[cohomological integration]]

* [[adelic integration]]

[[!include infinitesimal and local - table]]


## References

An introduction to the basic notions of [[integration of differential forms]], with an eye towards applications in [[physics]] is in section 3 of 

* [[Theodore Frankel]], _[[The Geometry of Physics - An Introduction]]_ 

Discussion of integration similarly with an eye towards applications in physics but from a more [[general abstract]] perspective is in 

* _[[geometry of physics]] -- [integration](geometry+of+physics#Integration)_

A proof of the [[Riesz representation theorem]] in [[constructive mathematics]] is given in

* [[Thierry Coquand]], [[Bas Spitters]], _Integrals and Valuations_, Logic and Analysis (2009) 1(3) p.1-22, [arXiv:0808.1522](http://arxiv.org/abs/0808.1522), [doi](http://dx.doi.org/10.4115/jla.2009.1.3)


category: analysis

[[!redirects integral]]
[[!redirects integrals]]
[[!redirects integration]]
[[!redirects integrations]]

[[!redirects definite integral]]
[[!redirects definite integrals]]
[[!redirects definite integration]]
[[!redirects definite integrations]]
