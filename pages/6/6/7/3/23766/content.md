

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[solid state physics]], the *Kane-Mele invariant* (after [Kane & Mele 05b](#KaneMele05b)) or *Fu-Kane-Mele invariant* (after [Fu, Kane & Mele 2007](#FuKaneMele07)) is an element in [[cyclic group of order two|$\mathbb{Z}/2$]] naturally assigned to [[time-reversal symmetry|time-reversal symmetric]] [[spin|spinful]] [[insulators]], whose non-triviality partially detects whether the insulator is in a non-trivial [[topological phase of matter|topological phase]], hence whether it is a *[[topological insulator]]*.

Concretely, for 3d materials the Kane-Mele invariant is obtained from the [[Chern-Simons invariant]] of the [[Berry connection]] on the [[Brillouin torus]] (eg. [KLW 16, Sec. 4.3](#KLW16)).

Under the expected [[K-theory classification of topological phases of matter]], [[time-reversal symmetry|time-reversal symmetric]] and spinful [[topological insulators]] are classified by the class of their [[valence bundle]] in [[KO-theory]] of degree 4 (hence in [[KQ-theory]]) equipped with the time-reversal [[involution]] $\tau$. The Kane-Mele invariant is a  non-trivial group homomorphism from that K-theory group to $\mathbb{Z}/2$ ([Bunk & Szabo 20, Prop. 2.25, Pro. 5.22(4)](#BunkSzabo20)):

$$
  K Q
  \big(
    \mathbb{T}^d, \tau
  \big)
  \xrightarrow{\text{KM invariant}}
  \mathbb{Z}/2
  \,.
$$

## Related concepts

* [[Haldane model]]

## References

The idea originates in:

* {#KaneMele05b} [[Charles Kane]], [[Eugene Mele]],  *$Z_2$ Topological Order and the Quantum Spin Hall Effect*, Phys. Rev. Lett. **95** (2005) 146802 ([doi:10.1103/PhysRevLett.95.146802](https://doi.org/10.1103/PhysRevLett.95.146802))

* [[Liang Fu]], [[Charles L. Kane]]: *Time Reversal Polarization and a $\mathbb{Z}_2$ Adiabatic Spin Pump*, Phys. Rev. B **74** (2006) 195312 &lbrack;[arXiv:cond-mat/0606336](https://arxiv.org/abs/cond-mat/0606336), [doi:10.1103/PhysRevB.74.195312](https://doi.org/10.1103/PhysRevB.74.195312)&rbrack;

* {#FuKaneMele07} [[Liang Fu]], [[Charles L. Kane]], [[Eugene J. Mele]]: *Topological Insulators in Three Dimensions*, Phys. Rev. Lett. **98**  (2007) 106803 &lbrack;[arXiv:cond-mat/0607699](https://arxiv.org/abs/cond-mat/0607699), [arXiv:10.1103/PhysRevLett.98.106803](https://doi.org/10.1103/PhysRevLett.98.106803)&rbrack;

This was motivated by the observation that [[graphene]] appears as a [[topological insulator]] with a non-trivial MK-invariant when its [[spin-orbit coupling]] is resolved, due to a [[quantum spin Hall effect]]:

* {#KaneMele05a} [[Charles Kane]], [[Eugene Mele]], _Quantum Spin Hall Effect in Graphene_, Phys. Rev. Lett. **95** 226801 (2005) ([arXiv:cond-mat/0411737](https://arxiv.org/abs/cond-mat/0411737), [doi:10.1103/PhysRevLett.95.226801](https://doi.org/10.1103/PhysRevLett.95.226801))

Discussion relating to a previously defined FKMM invariant:

* Giuseppe De Nittis, [[Kiyonori Gomi]]: *Classification of "Quaternionic" Bloch-bundles: Topological Quantum Systems of type AII*, Commun. Math. Phys. **339** (2015) 1–55 &lbrack;[arXiv:1404.5804](https://arxiv.org/abs/1404.5804), [doi:10.1007/s00220-015-2390-0](https://doi.org/10.1007/s00220-015-2390-0)&rbrack;


On the relation of the Kane-Mele invariant to the [[K-theory classification of topological phases of matter]]:

* {#KLW16} [[Ralph M. Kaufmann]], Dan Li, Birgit Wehefritz-Kaufmann, *Notes on topological insulators*, Rev. Math. Phys. **28** 10 (2016) 1630003 ([arXiv:1501.02874](https://arxiv.org/abs/1501.02874), [doi:10.1142/S0129055X1630003X](https://doi.org/10.1142/S0129055X1630003X))

* {#BunkSzabo20} [[Severin Bunk]], [[Richard Szabo]], *Topological Insulators and the Kane-Mele Invariant: Obstruction and Localisation Theory*,  Reviews in Mathematical Physics **32** 06 (2020) 2050017  ([arXiv:1712.02991](https://arxiv.org/abs/1712.02991), [doi:10.1142/S0129055X20500178](https://doi.org/10.1142/S0129055X20500178))


[[!redirects Kane-Mele invariants]]

[[!redirects Kane-Mele model]]
[[!redirects Kane-Mele models]]

[[!redirects Fu-Kane-Mele invariant]]
[[!redirects Fu-Kane-Mele invariants]]

