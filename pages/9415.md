
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### In Lie theory

In [[Lie theory]], a _Weyl group_ is a [[group]] associated with a [[compact Lie group]] that can either be abstractly defined in terms of a [[root system]] or in terms of a [[maximal torus]]. More generally there are Weyl groups associated with [[symmetric spaces]].

The Weyl group of a [[compact Lie group]] $G$ is equivalently the [[quotient group]] of the [[normalizer]] of any [[maximal torus]] $T$ by that torus.

$$
  W \simeq N_G T / T
  \,.
$$

### In equivariant homotopy theory
  {#InEquivariantHomotopyTheory}

In [[equivariant homotopy theory]] one uses the term _Weyl group_ more generally for the [[quotient group]] 

$$
  W_G H = (N_G H) / H
$$ 

of the [[normalizer]] of a given [[subgroup]] $H \hookrightarrow G$ by that subgroup (e.g. [May 96, p. 13](#May96)). 

The relevance of the Weyl group in this sense is that it is the maximal group which canonically [[action|acts]] on $H$-[[fixed points]] of a [[topological G-space]]. (See at _[Change of equivariance group and fixed loci](topological+G-space#ChangeOfGroupsAndFixedLoci)_ for details and, at, e.g., _[[tom Dieck splitting]]_ for applications.)

This may be seen from the fact that the Weyl group of $H \subset G$ is the [[automorphism group]] of the [[coset space]] $G/H$ in the [[orbit category]] of $G$:

$$
  End_{G Orbits}
  \big(
    G/H
  \big)
  \;\;
  =
  Aut_{G Orbits}
  \big(
    G/H
  \big)
  \;\;
    \simeq
  \;\;
  W_G(H)
  \,.
$$

Notice that $W_G G = 1$ and $W_G 1 = G$.

{#WeylGroupOfNormalSubgroup} On the other hand, if $H  = N \subset G$ is a [[normal subgroup]], then its [[normalizer]] is $G$ itself, in which case the Weyl group is just the plain [[quotient group]]

$$
  W_G N \;\simeq\; G/N
  \,.
$$


## Definition

Given a [[compact Lie group]] $G$ with chosen 
[[maximal torus]] $T$, its __Weyl group__ $W(G)=W(G,T)$ is the [[group of automorphisms]] of $T$ which are restrictions of [[inner automorphisms]] of $G$. 

This is the [[quotient group]] of the [[normalizer subgroup]] of $T \subset G$ by $T$

$$
  W \simeq N_G(T)/T
  \,.
$$
 
## Properties

* The [[maximal torus]] is of [[finite index subgroup|finite index]] in its [[normalizer]]; the [[quotient]] $N(T)/T$ is [[isomorphism|isomorphic]] to $W(G)$. 


* The [[cardinality]] of $W(G)$ for a compact connected $G$, equals the [[Euler characteristic]] of the [[homogeneous space]] $G/T$ ("[[flag variety]]"). 


* An important approach to the representations of the Weyl groups is the [[Springer theory]].

## Related concepts

* [[Schubert calculus]]

## References

* [[eom]]: [Weyl group](http://eom.springer.de/W/w097710.htm); wikipedia [Weyl group](http://en.wikipedia.org/wiki/Weyl_group)
* N. Chriss, V. Ginzburg, _Representation theory and complex geometry_, Birkh&#228;user 1997. x+495 pp.
* Walter Borho, Robert MacPherson, _Repr&#233;sentations des groupes de Weyl et homologie d'intersection pour les vari&#233;t&#233;s nilpotentes_, C. R. Acad. Sci. Paris S&#233;r. I Math. 292 (1981), no. 15, 707&#8211;710 [MR82f:14002](http://www.ams.org/mathscinet-getitem?mr=618892)

* {#May96} [[Peter May]], _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. 
With contributions by M. Cole, G. Comezana, S. Costenoble, A. D. Elmendorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/alaska1.pdf), [cbms-91](https://bookstore.ams.org/cbms-91))



[[!redirects Weyl groups]]