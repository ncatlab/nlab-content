
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[C*-algebra]] $A$, not necessarily [[commutative C*-algebra|commutative]], write $ComSub(A)$ for its [[poset of commutative subalgebras]], whose [[morphisms]] are the inclusion maps. By [[Gelfand duality]], the [[presheaf topos]] $PSh(ComSub(A))$ over this contains a canonical [[object]], namely the [[presheaf]] 

$$
  \Sigma \;\colon\; C \mapsto \Sigma_C
$$

which maps a [[commutative C*-algebra]] $C \hookrightarrow A$ to (the point set underlying) its [[Gelfand spectrum]] $\Sigma_C$. This is called the _spectral presheaf_ of $A$ ([Isham-D&#246;ring 07](#IshamDoering07))

## Properties

The [[Kochen-Specker theorem]] of [[quantum mechanics]] is equivalent to the statement that for $H$ a (complex) [[Hilbert space]] of [[dimension]] greater than 2, then the spectral presheaf of the [[algebra of bounded operators]] $\mathcal{B}(H)$ (the [[quantum observables]]) has no [[global element]] ([Butterfield-Hamilton-Isham 98](#ButterfieldHamiltonIsham)). (This observation motivates the topos-theoretic development in ([Isham-D&#246;ring 07](#IshamDoering07))).

See at _[[Kochen-Specker theorem]]_ and at _[[Bohr topos]]_ for more on this.

## Related concepts

* [[Bohr topos]]

* [[daseinisation]]

## References

The term "spectral presheaf" was introduced in 

* [[Jeremy Butterfield]], John Hamilton, [[Chris Isham]], _A topos perspective on the Kochen-Specker theorem_, _I. quantum states as generalized valuations_, Internat. J. Theoret. Phys. 37(11):2669--2733, 1998, [MR2000c:81027](http://www.ams.org/mathscinet-getitem?mr=1669557), [doi](http://dx.doi.org/10.1023/A:1026680806775); _II. conceptual aspects and classical analogues_ Int. J. of Theor. Phys. 38(3):827--859, 1999, [MR2000f:81012](http://www.ams.org/mathscinet-getitem?mr=1697983), [doi](http://dx.doi.org/10.1023/A:1026652817988); _III. Von Neumann algebras as the base category_, Int. J. of Theor. Phys. 39(6):1413--1436, 2000, [arXiv:quant-ph/9911020](http://arxiv.org/abs/quant-ph/9911020), [MR2001k:81016](http://www.ams.org/mathscinet-getitem?mr=1788498),[doi](http://dx.doi.org/10.1023/A:1003667607842); _IV. Interval valuations_, Internat. J. Theoret. Phys. __41__ (2002), no. 4, 613&#8211;639, [MR2003g:81009](http://www.ams.org/mathscinet-getitem?mr=1902067), [doi](http://dx.doi.org/10.1023/A:1015276209768)    {#ButterfieldHamiltonIsham}


* [[Chris Isham]], [[Andreas Döring]], _A Topos Foundation for Theories of Physics_, ([arXiv:quant-ph/0703060](http://arxiv.org/abs/quant-ph/0703060), [arXiv:quant-ph/0703062](http://arxiv.org/abs/quant-ph/0703062), [arXiv:quant-ph/0703066](http://arxiv.org/abs/quant-ph/0703066))
 {#IshamDoering07}

[[!redirects spectral presheaves]]