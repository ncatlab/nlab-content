
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[moduli space]] of [[connections on bundles]] over some prescribed [[space]].

Often one considers [[flat connections]] ([[local systems]]) only, see at _[[moduli space of flat connections]]_.

## Properties

### Compactness

If $\Sigma$ is a [[compact topological space|compact]] [[smooth manifold]], then the [[moduli space]] of [[flat connections]] over $\Sigma$ is compact. 

### Over complex manifolds / complex varieties

Over a [[complex manifold]]/[[complex variety]], the [[Koszul-Malgrange theorem]] identifies holomorphic [[flat connections]] on [[complex vector bundles]] with [[holomorphic vector bundles]]. This identifies the moduli space of flat connections as a [[complex manifold]] with (a non-abelian version of) the first Griffiths [[intermediate Jacobian]]. See at _[intermediate Jacobian -- Examples -- k=0](http://nlab.mathforge.org/nlab/show/intermediate+Jacobian#ExamplePicard)_.

More specifically over a [[Riemann surface]] _[[Narasimhan–Seshadri theorem]]_ identifies the [[moduli spaces of flat connections]] with that of certain [[complex manifold|complex]] spaces of [[stable vector bundle|stable]] [[holomorphic vector bundles]].  This space appears as the [[phase space]] for [[Chern-Simons theory]] over that surface. See there for more.

More generally, the [[Donaldson-Uhlenbeck-Yau theorem]] similarly gives a [[Kähler structure]] on the moduli space of flat connections also over higher dimensional K&#228;hler manifolds ([Scheinost-Schottenloher 96, corollary 1.16](#ScheinostSchottenloher96)).

## Examples

### Flat connections over a torus
  {#FlatConnectionsOverATorus}

Let $G$ be a [[compact Lie group]]. Assume either that $G$ is [[simply connected]] or is a [[torus]] (what we really need below is that any two commuting elements in $G$ sit jointly in one [[maximal torus]]). 

The moduli space of $G$ [[flat connections]] on a 2-dimensional [[torus]] $A \simeq S^1 \times S^1$ (e.g. underlying a complex [[elliptic curve]]) has the following description:

first, the [[moduli stack]] of flat connections is

$$
  \begin{aligned}
    [\Pi(A), \mathbf{B}G] 
    & \simeq [B [A, S^1], \mathbf{B}G]
    \\
    & \simeq Hom_{Grp}(\mathbb{Z} \times \mathbb{Z}, G)//_{ad} G
  \end{aligned}
$$

(see also the discussion at _[characters and fundamental groups of tori](http://ncatlab.org/nlab/show/group+character#CharactersAndFundamentalGroupsOfTori)_).

Here a single [[flat connection]] is just a choice of pair of two commuting elements in $G$, and $G$ acts on that by [[conjugation]]. Now any two commuting elements can be taken to sit in a [[maximal torus]] $T \hookrightarrow G$, and up to [[conjugation]] we can take this to be one fixed maximal torus. This means that the moduli space is actually

$$
  \pi_0 \left(
    Hom_{Grp}([A,S^1], G)//_{ad} G
  \right)
  \simeq
  Hom_{Grp}([A, S^1], T)/W
  \,,
$$

where $W$ is the [[Weyl group]] $W = N_G(T)/T$. 

Moreover, by [[Pontryagin duality]] this may be re-expressed as

$$
  \cdots \simeq Hom_{Grp}([T,S^1], A)/W
  \,.
$$

where now $[T,S^1]$ is the [[character group]] of the [[maximal torus]].

In this form the moduli space of flat connections appears prominently for instance in the discussion of [[equivariant elliptic cohomology]]. But beware that the above interpretation in [[algebraic geometry]] is at least more subtle, see ([Lurie 15](#Lurie15)).


## Related concepts

* [[Donaldson-Uhlenbeck-Yau theorem]]

* [[Tamagawa numbers]]

* [[Hitchin connection]]


[[!include moduli spaces -- contents]]


## References

Original articles include 

* [[Michael Atiyah]], [[Raoul Bott]], _The Yang-Mills equations over Riemann surfaces_, Philosophical Transactions of the Royal Society of London. Series A, Mathematical and Physical Sciences
Vol. 308, No. 1505 (Mar. 17, 1983), pp. 523-615 ([jstor](http://www.jstor.org/stable/37156), [lighning summary](http://math.stackexchange.com/a/295505/58526))

* [[Nigel Hitchin]], _Flat connections and geometric quantization_, Comm.Math.Phys., 131 (1990) 347-380

* Nan-Kuo Ho, Chiu-Chu Melissa Liu, _On the connectedness of moduli spaces of flat connections over compact surfaces_, Canad. J. Math. 56(2004) 1228-1236 [doi](https://doi.org/10.4153/CJM-2004-053-3)

Review and lecture notes, mostly for the case of [[flat connections]]:

* Remi Janner, _Notes on the moduli space of flat connections_, 2005 ([pdf](https://www.researchgate.net/publication/265223952_Notes_on_the_moduli_space_of_flat_connections))

* Daan Michiels, _Moduli spaces of flat connections_, Master Thesis Leuven 2013 ([pdf](http://www.staff.science.uu.nl/~Schat001/Daan_thesis.pdf))

* {#Teschner14} [[Jörg Teschner]], _Quantization of moduli spaces of flat connections and Liouville theory_, proceedings of the International Congress of Mathematics 2014 ([arXiv:1405.0359](http://arxiv.org/abs/1405.0359))

* {#FockGoncharov14} [[Vladimir V. Fock]], [[Alexander G. Goncharov]], _Symplectic double for moduli spaces of G-local systems on surfaces_ ([arXiv:1410.3526](http://arxiv.org/abs/1410.3526))

and for the case of general and [[logarithmic connections]]

* {#BiswasMunoz} Indranil Biswas, V.Munoz, _Moduli spaces of connections on a Riemann surface_  ([pdf](http://www.mat.ucm.es/~vmunozve/Moduli.pdf))

Introcuction of [[Fock-Goncharov coordinates]] on [[moduli spaces of flat connections]]:

* {#FockGoncharov06} [[Vladimir V. Fock]], [[Alexander B. Goncharov]], _Moduli spaces of local systems and higher Teichm&#252;ller theory_, Publ. Math. Inst. Hautes &#201;tudes Sci. **103**, 1-211 (2006) &lbrack;[arXiv:math/0311149](https://arxiv.org/abs/math/0311149), [doi:10.1007/s10240-006-0039-4](https://doi.org/10.1007/s10240-006-0039-4)&rbrack;


Detailed discussion of moduli space of flat connections also on higher dimensional base spaces is in

* {#ScheinostSchottenloher96} Peter Scheinost, [[Martin Schottenloher]], pp. 154 (11 of 76) of _Metaplectic quantization of the moduli spaces of flat and parabolic bundles_, J. reine angew. Mathematik, 466 (1996) ([web](https://eudml.org/doc/153753)) 

For more references see at _[[Hitchin connection]]_.

Discussion in [[algebraic geometry]] includes

* {#Lurie15} [[Jacob Lurie]], _[MO comment](http://mathoverflow.net/a/226716/381)_ 2015


[[!redirects moduli spaces of connections]]

[[!redirects moduli stack of connections]]
[[!redirects moduli stacks of connections]]

