
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

## Idea

Lepage forms are certain [[differential forms]] on [[jet bundles]]. When of maximal horizontal degree then they may be identified with sums $\mathbf{L} + \theta$ of a [[local Lagrangian]] $\mathbf{L}$ with its induced presymplectic potential current $\theta$ (as discussed at [[covariant phase space]]). Lepage _equivalents_ associated with a local Lagrangian in particular allow to get the [[Euler-Lagrange form]] (which vanishes along the pullback of any section that satisfies the [[Euler-Lagrange equation]]) from its de Rham differential, thus avoiding the need to use the [[Euler operator]].

Lepage forms play a central role in the theory of [[variational sequences]].

## Definition

+-- {: .num_defn}
###### Definition

Given a [[smooth function|smooth]] [[bundle]] $E \to \Sigma$, then a [[differential n-form]] $\rho$ on its [[jet bundle]] $Jet(E)$ is called a _Lepage form_ if for every [[vector field]] $v$ on the jet bundle, the horizontal part $h(\iota_v \mathbf{d}\rho)$ (with respect to the [[variational bicomplex]]) of the contraction of $v$ into the [[de Rham differential]] of $\rho$ depends only on the projection of $v$ to a vector field on $E$ itself.

=--

e.g. [GMS 09, 2.1.2](#GMS09)

## In variational calculus

Let $\Sigma$ be of [[dimension]] $n$. Then a horizontal $n$-form $\mathbf{L} \in \Omega^{n,0}(Jet(E))$, may be regarded a [[local Lagrangian]]. Its de Rham differential has a unique decomposition

$$
  d \mathbf{L} = \mathbf{E} - d_H \theta
$$

where $E$ is a [[source form]], the [[Euler-Lagrange form]] of $\mathbf{L}$, and $\theta$, the induced presymplectic potential current, is defined up to addition of a horizontally exact form (e.g. [Zuckerman 87, section 2](#Zuckerman87)).

Then the combination

$$
  \rho \coloneqq \mathbf{L} + \theta
$$

is a Lepage form, and in fact such a form being Lepage is equivalent to $d \mathbf{L} + d_h \theta$ being a [[source form]].

The differential 

$$
  d \rho = \mathbf{E} + \omega
$$

is the sum of the [[Euler-Lagrange form]] and the presymplectic current density $\omega = d_V \theta$.

To obtain the [[Euler-Lagrange form]] one needs to apply an operator, called the [[Euler operator]] to $\mathbf{L}$. In contrast, the same Euler-Lagrange form may be obtained from $\mathbf{L}+\theta$ by applying the usual de Rham operator. This serves as a motivation to replace the Lagrangian $\mathbf{L}$ with the form $\mathbf{L}+\theta$. Consistent replacements are known as _Lepage equivalents_.

###### Definition

Let $E \to \Sigma$ be a [[smooth function|smooth]] [[bundle]] with $\Sigma$ of [[dimension]] $n$. Given a horizontal $n$-form $\mathbf{L} \in \Omega^{n,0}(Jet(E))$, regarded as a [[local Lagrangian]] , a _Lepage equivalent_ $\rho_L$ is a $n$-form $\rho_L\in\Omega^n(Jet(E))$ (not necessarily horizontal) such that *a.* The horizontal component of $\rho_L$ is $mathbf{L}$, and *b.* The (n,1)-component of $d \rho_L$ is the [[Euler-Lagrange form]] $E$ of $\mathbf{L}$.

Lepage equivalents are rarely unique, and many times fail to be globally-defined even if the Lagrangian itself is globally defined. A notable exception is [[classical mechanics]] with $F$ a finite-dimensional smooth manifold and order-1 Lagrangian (meaning it depends on at most first-order derivatives fields), for which there is a unique Lepage equivalent, called the _Poincaré-Cartan form_. 

Note that the definition of Lepage equivalent only involves restrictions on the horizontal and 1-vertical components. This means that given a Lepage equivalent $\rho_L$, one can shift by forms of bidegree $(n-k,k)$ for $k\geq 2$ and still obtain a Lepage equivalent even though this affects the resulting pre-$n$-plectic form. One way towards addressing this problem is to demand a further condition called _closure property_ , which removes the contributions from trivial Lagrangians.

###### Definition

A Lepage equivalent $\rho_L$ is said to satisfy the _closure property_ if whenever the [[Euler-Lagrange form]] $E$ of the Lagrangian $\mathbf{L}$ is _identically_ zero, then $d\rho_L=0$ vanishes identically too.



## Related concepts

* [[variational sequence]]

* [[multisymplectic geometry]]

* [[n-plectic geometry]]

## References

Lepage was a student of [[Théophile de Donder]] and did his work on the [[calculus of variations]] around the 1930s. Only much later, [[Demeter Krupka]] was responsible for naming Lepage forms around the 1970s.

See for instance

* {#GMS09} Giovanni Giachetta, Luigi Mangiarotti, Gennadi Sardanashvily, _Advanced classical field theory_, World Scientific, 2009


* {#Zuckerman87} [[Gregg Zuckerman|G. J. Zuckerman]], _Action principles and global geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259&#8364;284. ([[ZuckermanVariation.pdf:file]]) 

Exposition of [[variational calculus]] in terms of [[jet bundles]] and Lepage forms and aimed at examples from [[physics]] is in

* {#MusilovaHronek16} [[Jana Musilová]],  [[Stanislav Hronek]], _The calculus of variations on jet bundles as a universal approach for a variational formulation of fundamental physical theories_, Communications in Mathematics, Volume 24, Issue 2 (Dec 2016) ([doi.org/10.1515/cm-2016-0012]( https://doi.org/10.1515/cm-2016-0012))

* [[Demeter Krupka]]. _Introduction to global variational geometry_. Vol. 1. Amsterdam: Atlantis Press, (2015). ([doi:10.2991/978-94-6239-073-7] (https://doi.org/10.2991/978-94-6239-073-7}))


[[!redirects Lepage forms]]
