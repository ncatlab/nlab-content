
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
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

What has been called _Geometry of Interaction_ ([Girard 89](#Girard89)) is a kind of [[semantics]] for [[linear logic]]/[[linear type theory]] that is however different in method from the usual [[categorical semantics]] in [[monoidal categories]]. Instead of interpreting a [[proof]] of linear implication $A\multimap B$ as a [[morphism]] between [[objects]] $A$ and $B$ in a [[monoidal category]] as in [[categorical semantics]], the _Geometry of Interaction_ interprets it as an [[endomorphism]] on the object $A\multimap B$. This has been named _operational semantics_ to contrast with thr traditional _denotational semantics_.

That also the "operational semantics" of GoI has an interpretation in [[category theory]], though, namely in [[traced monoidal categories]] was first suggested in ([Joyal-Street-Verity 96](#JoyalStreetVerity96)) and then developed out in ([Haghverdi 00](#Haghverdi00), [Abramsky-Haghverdi-Scott 02](#AbramskyHaghverdiScott02),[Haghverdi-Scott 05](#HaghverdiScott05)). See ([Shirahata](#Shirahata)) for a good review.

## References

The original references are

* [[Jean-Yves Girard]]. Towards a geometry of interaction. In Categories in Computer Science and Logic, pages 69 &#8211; 108, Providence, 1989. American Mathematical Society. Proceedings of Symposia in Pure Mathematics n92.
 {#Girard89}

* [[Jean-Yves Girard]]. Geometry of interaction I: interpretation of system F. In Ferro, Bonotto, Valentini, and Zanardo, editors, Logic Colloquium '88, pages 221 &#8211; 260, Amsterdam, 1989. North-Holland.

* [[Jean-Yves Girard]]. Geometry of interaction II : deadlock-free algorithms. In Martin-L&#246;f and Mints, editors, Proceedings of COLOG 88, volume 417 of Lecture Notes in Computer Science, pages 76 &#8211; 93, Heidelberg, 1990. Springer-Verlag.

* [[Jean-Yves Girard]]. Geometry of interaction III : accommodating the additives. In Girard, Lafont, and Regnier, editors, Advances in Linear Logic, pages 329 &#8211; 389, Cambridge, 1995. Cambridge University Press.

* [[Jean-Yves Girard]]. Geometry of interaction IV : the feedback equation. In Stoltenberg-Hansen and V&#228;&#228;n&#228;nen, editors, Logic Colloquium '03, pages 76 &#8211; 117. Association for Symbolic Logic, 2006.

* [[Jean-Yves Girard]]. Geometry of interaction V : logic in the hyperfinite factor, in memoriam Claire Delaleu (1991-2009). Fully revised version (October 2009). ([pdf](http://iml.univ-mrs.fr/~girard/GdI5.1.pdf))

* [[Jean-Yves Girard]]. Geometry of Interaction VI: a blueprint for Transcendental Syntax, January 2013, revised August 28th 2013. ([pdf](http://iml.univ-mrs.fr/~girard/blueprint.pdf))

Reviews include

* Masaru Shirahata, _Geometry of Interaction explained_, ([pdf](http://www.kurims.kyoto-u.ac.jp/~hassei/algi-13/kokyuroku/19_shirahata.pdf))
 {#Shirahata}

* [[Samson Abramsky]], E. Haghverdi and P. Scott, "Geometry of Interaction and linear combinatory algebra," Mathematical Structures in Computer Science (2002), vol. 12, pp. 625-665.

* [[Samson Abramsky]] and R. Jagadeesan, "New Foundations for the Geometry of Interaction," Proceedings 7th Annual IEEE Symp. on Logic in Computer Science, LICS'92, Santa Cruz, CA, USA, 22&#8211;25 June 1992.

* Linear Logic Wiki, _[Geometry of Interaction](http://llwiki.ens-lyon.fr/mediawiki/index.php/Geometry_of_interaction)_

The operational categorical semantics in [[traced monoidal categories]] is due to 

* [[André Joyal]], [[Ross Street]], [[Dominic Verity]], _Traced monoidal categories_, Math. Proc. Camb. Phil. Soc. (1996), 119, 447 ([pdf](http://sci-prew.inf.ua/v119/3/S0305004100074338.pdf))
 {#JoyalStreetVerity96}

* [[Esfandir Haghverdi]],  _A Categorical Approach to Linear Logic_, Geometry of Proofs and Full Completeness, PhD Thesis, University of Ottawa, Canada 2000.
 {#Haghverdi00}

* [[Samson Abramsky]], [[Esfandir Haghverdi]],  [[Philip Scott]], _Geometry of Interaction and Linear Combinatory Algebras_. MSCS, vol. 12(5), 2002, 625-665, CUP (2002) ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.24.7818))
  {#AbramskyHaghverdiScott02}

* [[Esfandir Haghverdi]], [[Philip Scott]], _A categorical model for the geometry of interactions_ ,Theoretical Computer Science, 2005 ([pdf](http://xavier.informatics.indiana.edu/~ehaghver/HS-TCS-04.pdf))
 {#HaghverdiScott05}


[[!redirects Geometry of interaction]]
[[!redirects geometry of interaction]]

[[!redirects Geometry of Interactions]]
[[!redirects geometry of interactions]]