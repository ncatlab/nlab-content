
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

What has been called _Geometry of Interaction_ ([Girard 89](#Girard89)) is a kind of [[semantics]] for [[linear logic]]/[[linear type theory]] that is however different in method from the usual [[categorical semantics]] in [[monoidal categories]]. Instead of interpreting a [[proof]] of a linear entailment $A\vdash B$ as a [[morphism]] between [[objects]] $A$ and $B$ in a [[monoidal category]] as in [[categorical semantics]], the _Geometry of Interaction_ interprets it as an [[endomorphism]] on the object $A\multimap B$. This has been named _operational semantics_ to contrast with the traditional _denotational semantics_.

That also the "operational semantics" of GoI has an interpretation in [[category theory]], though, namely in [[compact closed categories]] induced from [[traced monoidal categories]] was first suggested in ([Joyal-Street-Verity 96](#JoyalStreetVerity96)) and then developed in ([Haghverdi 00](#Haghverdi00), [Abramsky-Haghverdi-Scott 02](#AbramskyHaghverdiScott02), [Haghverdi-Scott 05](#HaghverdiScott05)). See ([Shirahata](#Shirahata)) for a good review.

## Properties

### Relation to superoperators and quantum operations
 {#RelationToQuantumOperations}


We discuss a relation of the GoI to [[superoperators]]/[[quantum operations]] in [[quantum physics]].


According to ([Abramsky-Haghverdi-Scott 02, remark 5.8](#AbramskyHaghverdiScott02), [Haghverdi 00b, section 6](#Haghverdi00b)) all the standard and intended interpretations of the GoI take place in those [[compact closed categories]] $Int(\mathcal{C})$ free on a [[traced monoidal category]] $\mathcal{C}$ (as discussed there). In these references therefore the notation $Int(-)$ from ([Joyal-Street-Verity 96](#JoyalStreetVerity96)) is changed to $\mathcal{G}(-)$, for "Geometry of Interaction construction" (see [Abramsky-Haghverdi-Scott 02, p. 11](#AbramskyHaghverdiScott02)).

The objects of $Int(\mathcal{C})$ are pairs $(A^+, A^-)$ of objects of $\mathcal{C}$, a morphism $(A^+ , A^-) \to (B^+ , B^-)$ in $Int(\mathcal{C})$ is given by a morphism in $\mathcal{C}$ of the form 

$$
  \array{
    A^+\otimes B^- 
    \\
    \downarrow
    \\ 
    A^- \otimes B^+
  }
$$ 

in $\mathcal{C}$, and [[composition]] of two such morphisms $(A^+ , A^-) \to (B^+ , B^-)$ and $(B^+ , B^-) \to (C^+ , C^-)$ is given by [[trace|tracing out]] $B^+$ and $B^-$ in the evident way.

We observe now that subcategories of such $Int(\mathcal{C})$ are famous in [[quantum physics]] as "categories of [[superoperators]]" or "categories of [[quantum operations]]", formalizing [[linear maps]] on spaces of [[operators]] on a [[Hilbert spaces]] that takes [[density matrices]] (hence mixed [[quantum states]]) to density matrices ("[[completely positive maps]]").

First notice that if the [[traced monoidal category]] structure on $\mathcal{C}$ happens to be that induced by a [[compact closed category]] structure, then by compact closure the morphisms $(A^+ , A^-) \to (B^+ , B^-)$ in $Int(\mathcal{C})$ above are equivalently morphisms in $\mathcal{C}$ of the form

$$
  (A^-)^\ast \otimes A^+ \longrightarrow (B^-)^\ast \otimes B^+
$$

and if moreover one concentrates on the case where $A \coloneqq A^- \simeq A^+$ etc. then these are morphisms of the form

$$
  End(A) \longrightarrow End(B)
  \,.
$$

Under this identification the somewhat curious-looking composition in $Int(\mathcal{C})$ given by tracing in $\mathcal{C}$ becomes just plain composition in $\mathcal{C}$.

Subcategories (non-full) of $Int(\mathcal{C})$ consisting of morphisms of this form in some ambient $\mathcal{C}$ have been considered in ([Selinger 05](#Selinger05)), there denoted $CPM(\mathcal{C})$, and shown to formalize the concept of [[quantum operations]] in [[quantum physics]]. For a quick review of Selinger's construction see for instance ([Coecke-Heunen 11, section 2](#CoeckeHeunen11)). Comments related to the relation between GoI and such constructions appear in ([Abramsky-Coecke 02](#AbramskyCoecke02)).

Now the $CPM(-)$ construction requires and assumes that $\mathcal{C}$ has all [[dual objects]] (which in the standard model means to restrict to [[Hilbert spaces]] of [[quantum states]] with are of [[finite]] [[dimension]]). To generalize away from this requirement a more general definition of quantum operations in $\mathcal{C}$ is given in  ([Coecke-Heunen 11, def. 1](#CoeckeHeunen11)), there denoted $CP(\mathcal{C})$. Direct inspection shows that $CP(\mathcal{C})$ is still a (non-full) subcategory of $Int(\mathcal{C})$. 


## Related concepts

* [[transcendental syntax]]


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

* [[Jean-Yves Girard]], Part VI of _[[Lectures on Logic]]_

* Masaru Shirahata, _Geometry of Interaction explained_, ([pdf](http://www.kurims.kyoto-u.ac.jp/~hassei/algi-13/kokyuroku/19_shirahata.pdf))
 {#Shirahata}

* [[Samson Abramsky]], E. Haghverdi and P. Scott, "Geometry of Interaction and linear combinatory algebra," Mathematical Structures in Computer Science (2002), vol. 12, pp. 625-665. ([ps](http://www.cs.ox.ac.uk/files/328/ahs.ps))

* [[Samson Abramsky]] and R. Jagadeesan, "New Foundations for the Geometry of Interaction," Proceedings 7th Annual IEEE Symp. on Logic in Computer Science, LICS'92, Santa Cruz, CA, USA, 22&#8211;25 June 1992. ([pdf](http://www.cs.ox.ac.uk/files/300/nfgoi.pdf))

* Harry G. Mairson, "From Hilbert Spaces to Dilbert Spaces: Context Semantics Made Simple", Proceedings of FST TCS 2002. ([pdf](http://www.cs.brandeis.edu/~mairson/Papers/fsttcs02.pdf))

* Linear Logic Wiki, _[Geometry of Interaction](http://llwiki.ens-lyon.fr/mediawiki/index.php/Geometry_of_interaction)_

* {#Murfet14} [[Daniel Murfet]], section 5 of _Logic and linear algebra: an introduction_ ([arXiv:1407.2650](http://arxiv.org/abs/1407.2650))


The operational categorical semantics in [[traced monoidal categories]] is due to 

* [[André Joyal]], [[Ross Street]], [[Dominic Verity]], _Traced monoidal categories_, Math. Proc. Camb. Phil. Soc. (1996), 119, 447 ([pdf](http://sci-prew.inf.ua/v119/3/S0305004100074338.pdf))
 {#JoyalStreetVerity96}

* [[Esfandir Haghverdi]],  _A Categorical Approach to Linear Logic_, Geometry of Proofs and Full Completeness, PhD Thesis, University of Ottawa, Canada 2000.
 {#Haghverdi00}

* [[Esfandir Haghverdi]], _Unique Decomposition Categories, Geometry of Interaction, and Combinatory Logic, Math. Struc. in Comp. Sci., 10, pp. 205-231.
 {#Haghverdi00b}

* [[Samson Abramsky]], [[Esfandir Haghverdi]],  [[Philip Scott]], _Geometry of Interaction and Linear Combinatory Algebras_. MSCS, vol. 12(5), 2002, 625-665, CUP (2002) ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.24.7818))
  {#AbramskyHaghverdiScott02}

* [[Esfandir Haghverdi]], [[Philip Scott]], _A categorical model for the geometry of interactions_ ,Theoretical Computer Science, 2005 ([pdf](http://xavier.informatics.indiana.edu/~ehaghver/HS-TCS-04.pdf))
 {#HaghverdiScott05}

Discussion of [[quantum operations]]/[[completely positive maps]] mentioned above is in 

* [[Peter Selinger]], _Dagger-compact closed categories and completely positive maps_, Electronic Notes in Theoretical Computer
Science (special issue: Proceedings of the 3rd International Workshop on Quantum Programming Languages). 2005 ([[SelingerPositiveMaps.pdf:file]], [ps](http://www.mscs.dal.ca/~selinger/papers/dagger.ps))
 {#Selinger05}

* [[Samson Abramsky]], [[Bob Coecke]], _Physical Traces: Quantum vs. Classical Information Processing_, Electronic Notes in Theoretical Computer Science 69 (2003) ([arXiv:0207057](http://arxiv.org/abs/cs/0207057))
 {#AbramskyCoecke02}

* [[Bob Coecke]], [[Chris Heunen]], _Pictures of complete positivity in arbitrary dimension_, EPTCS 95, 2012, pp. 27-35 ([arXiv:1110.3055](http://arxiv.org/abs/1110.3055))
 {#CoeckeHeunen11}


[[!redirects Geometry of interaction]]
[[!redirects geometry of interaction]]

[[!redirects Geometry of Interactions]]
[[!redirects geometry of interactions]]