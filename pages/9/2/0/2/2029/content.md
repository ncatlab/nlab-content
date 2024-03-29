
#Contents#
* table of contents
{:toc}

## Idea

A [[scheme]] is _reduced_ if it has no "purely [[infinitesimal object|infinitesimal]] directions". 


## Definition

An algebraic [[scheme]] is __reduced__ if all [[stalks]] of the [[structure sheaf]] are [[local rings]] without nonzero nilpotent elements. 

This means that it is a [[reduced object]] in the sense of [[synthetic differential geometry]].

Equivalently a scheme $X$ is reduced iff it can be covered by a family $\{U_\alpha\}_\alpha$ of [[open sets]] such that $\mathcal{O}_X(U)$ has no nonzero nilpotent elements. Equivalently, every open $U\subset X$ has the property that $\mathcal{O}_X(U)$ has no nonzero nilpotent elements.

Reducedness can also be characterized by the [[internal language]] of the sheaf topos $\mathrm{Sh}(X)$: $X$ is reduced iff $\mathcal{O}_X$ is a reduced ring in $\mathrm{Sh}(X)$ iff $\mathcal{O}_X$ is a [[field|residue field]] in $\mathrm{Sh}(X)$ (i.e. every non-unit is zero). This can be used to give an internal proof of the fact that $\mathcal{O}_X$-modules of [[coherent sheaf|finite type]] over a reduced scheme are locally free iff their [[rank]] is constant (by internalizing the constructive proof of the linear algebra fact that [[finitely generated modules]] over residue fields are [[free module|free]], provided the minimal number of elements needed to generate the module exists as a natural number).

## Examples

For instance the dual $Spec k[\epsilon](\epsilon^2)$ of the [[ring of dual numbers]] is *not* reduced, since it is the point with an infinitesimal extension added to it. Its reduction is the point itself. Generally, [[formal schemes]] are not reduced.


## Related concepts

* [[formal scheme]]

* [[reduced object]]

* [[de Rham space]]

* [[formally smooth scheme]]

category: algebraic geometry
[[!redirects reduced schemes]]