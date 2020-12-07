
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### Langlands correspondence
+--{: .hide}
[[!include Langlands correspondence -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Electric-magnetic duality is a lift of [[Hodge star operator|Hodge duality]] from [[de Rham cohomology]] to [[ordinary differential cohomology]].


## Description

Consider a [[circle n-bundle with connection]] $\nabla$ on a space $X$. Its [[higher parallel transport]] is the [[action functional]] for the [[sigma-model]] of  $(n-1)$-dimensional objects ($(n-1)$-branes) propagating in $X$.

For $n = 1$ this is the coupling of the [[electromagnetic field]] to particles. For $n = 2$ this is the coupling of the [[Kalb-Ramond field]] to strings.

The [[curvature]] $F_\nabla \in \Omega^{n+1}(X)$ is a closed $(n+1)$-form. The condition that its image $\star F_\nabla$ under the [[Hodge star operator]]  is itself closed

$$
  d_{dR} \star F_\nabla = 0
$$

is the [[Euler-Lagrange equation]] for the standard (abelian [[Yang-Mills theory]]-[[action functional]] on the space of circle n-bundle with connection.

If this is the case, it makes sense to ask if $\star F_\nabla$ itself is the curvature $(d-(n+1))$-form of a circle $(d-(n+1)-1)$-bundle with connection $\tilde \nabla$, where $d = dim X$ is the [[dimension]] of $X$.

If such $\tilde \nabla$ exists, its [[higher parallel transport]] is the gauge interaction [[action functional]] for $(d-n-3)$-dimensional objects propagating on $X$.

In the special case of ordinary [[electromagnetism]] with $n=1$ and $d = 4$ we have that electrically charged 0-dimensional particles couple to $\nabla$ and magnetically charged $(4-(1+1)-2) = 0$-dimensional particles couple to $\tilde \nabla$.

In analogy to this case one calls generally the $d-n-3$-dimensional objects coupling to $\tilde \nabla$ the **magnetic duals** of the $(n-1)$-dimensional objects coupling to $\nabla$.

## Generalizations

For $d= 4$ EM-duality is the special abelian case of [[S-duality]] for [[Yang-Mills theory]]. Witten and Kapustin argued that this is governed by the [[geometric Langlands correspondence]].

## Examples

* In [[N=2 D=4 super Yang-Mills theory]] electric-magnetic duality is studied as _[[Seiberg-Witten theory]]_.

* In [[heterotic string theory]] one considers 1-dimensional objects in $d=10$-dimensional spaces electrically charged (under the [[Kalb-Ramond field]]). Their magnetic duals are 5-dimensional objects (fivebranes), studied in [[dual heterotic string theory]].

* [[!include electric-magnetic duality -- table]]

* [[M2-brane]] and [[M5-brane]]: the 4-form $G_4$ which the M2-brane couples to is the Hodge-dual of the 7-form $G_7$ which the M5-brane couples to 

$$
  G_7 = \star G_4
$$

as imposed by the equations of motion for 11d [[supergravity]] (see [here](https://ncatlab.org/nlab/show/torsion+constraints+in+supergravity#Examples11dSuGra)). The associated [[C3-field]] and [[C6-field]] are electric-magnetic duals. 

## Related concepts

[[duality in physics]], [[duality in string theory]]

* [[parent action functional]]

* [[S-duality]]

  * **electro-magnetic duality**

    * [[Montonen-Olive duality]]

    * [[dual graviton]]

    * [[dual photon]]

  * [[Seiberg duality]]

  * [[geometric Langlands correspondence]]

  * [[quantum geometric Langlands correspondence]]



## References

Detailed review is in 

* [[José Figueroa-O'Farrill]], _Electromagnetic Duality for Children_ (1998) ([[FigueroaElectromagneticDuality.pdf:file]])

It was originally noticed in

* {#GNO77} P. Goddard, J. Nuyts, and [[David Olive]], _Gauge Theories And Magnetic Charge_, Nucl. Phys. B125 (1977) 1-28.

that where [[electric charge]] in [[Yang-Mills theory]] takes values in the [[weight lattice]] of the [[gauge group]], then [[magnetic charge]] takes values in the lattice of what is now called the [[Langlands dual group]].

This led to the electric/magnetic duality conjecture formulation in

* [[Claus Montonen]], [[David Olive]], _Magnetic Monopoles As Gauge Particles?_ Phys. Lett. B72 (1977) 117-120 ([spire:121372](https://inspirehep.net/literature/121372), <a href="https://doi.org/10.1016/0370-2693(77)90076-4">doi:10.1016/0370-2693(77)90076-4</a>)

According to ([Kapustin-Witten 06, pages 3-4](#KapustinWitten06)) the observation that the Montonen-Olive dual charge group coincides with the [[Langlands dual group]] is due to 

* [[Michael Atiyah]], private communication to [[Edward Witten]], 1977

See also the references at _[[S-duality]]_.

The insight that the Montonen-Olive duality works more naturally in [[super Yang-Mills theory]] is due to

* [[David Olive]], [[Edward Witten]], _Supersymmetry Algebras That Include Topological Charges_, Phys. Lett. B78 (1978) 97-101.

and that it works particularly for [[N=4 D=4 super Yang-Mills theory]] is due to

* H. Osborn, _Topological Charges For $N = 4$ Supersymmetric Gauge Theories And Monopoles Of Spin 1_, Phys. Lett. B83 (1979) 321-326.

The observation that the $\mathbb{Z}_2$ electric/magnetic duality extends to an $SL(2,\mathbb{Z})$-action in this case is due to 

* [[John Cardy]], E. Rabinovici, _Phase Structure Of Zp Models In The Presence Of A Theta Parameter_, Nucl. Phys. B205 (1982) 1-16; 

* [[John Cardy]], _Duality And The Theta Parameter In Abelian Lattice Models_, Nucl. Phys. B205 (1982) 17-26.

* A. Shapere and [[Frank Wilczek]], _Selfdual Models With Theta Terms_, Nucl. Phys. B320 (1989) 669-695.

and specifically the embedding of this into [[string theory]] [[S-duality]] originates in

* [[Ashoke Sen]], _Dyon - Monopole Bound States, Self-Dual Harmonic Forms on the Multi-Monopole Moduli Space, and $SL(2,\mathbb{Z})$ Invariance in String Theory_ ([arXiv:hep-th/9402032](http://arxiv.org/abs/hep-th/9402032))


The understanding of this $SL(2,\mathbb{Z})$-symmetry as a remnant conformal transformation on a 6-dimensional [[principal 2-bundle]]-theory -- the [[6d (2,0)-superconformal QFT]] -- compactified on a torus is described in 

* {#Witten95a} [[Edward Witten]], pages 4-5 of _Some Comments On String Dynamics_, Proceedings of _String95_ ([arXiv:hepth/9507121](http://arxiv.org/abs/hepth/9507121))

* {#Witten95b} [[Edward Witten]], _On S-Duality in Abelian Gauge Theory_ ([arXiv:hep-th/9505186](http://arxiv.org/abs/hep-th/9505186))

* [[Cumrun Vafa]], _Geometric Origin of Montonen-Olive Duality_, Adv.Theor.Math.Phys.1:158-166, 1998 ([arXiv:hep-th/9707131](https://arxiv.org/abs/hep-th/9707131))

* {#Witten07} [[Edward Witten]], _[[Conformal field theory in four and six dimensions]]_, in [[Ulrike Tillmann]], _Topology, Geometry and Quantum Field Theory: Proceedings of the 2002 Oxford Symposium in Honour of the 60th Birthday of Graeme Segal_,  London Mathematical Society Lecture Note Series (2004) ([arXiv:0712.0157](http://arxiv.org/abs/0712.0157))


The relation of S-duality to [[geometric Langlands duality]] was understood in

* {#KapustinWitten06} [[Anton Kapustin]], [[Edward Witten]], _Electric-Magnetic Duality And The Geometric Langlands Program_ , Communications in number theory and physics, Volume 1, Number 1, 1&#8211;236 (2007) ([arXiv:hep-th/0604151](http://arxiv.org/abs/hep-th/0604151))

Exposition of this is in 

* [[Edward Frenkel]],  _What Do Fermat's Last Theorem and Electro-magnetic Duality Have in Common?_ KITP talk 2011 ([web](http://online.kitp.ucsb.edu/online/bblunch/frenkel/))

A perspective unifying EM-duality of [[higher gauge theories]]  with [[non-abelian T-duality]]:

* [[Ján Pulmann]], [[Pavol Ševera]], [[Fridrich Valach]], _A non-abelian duality for (higher) gauge theories_ ([arXiv:1909.06151](https://arxiv.org/abs/1909.06151))


[[!redirects electric-magnetic dualities]]

[[!redirects electro-magnetic duality]]
[[!redirects electro-magnetic dualities]]

[[!redirects electromagnetic duality]]
[[!redirects electromagnetic dualites]]
