
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Opetopic type theory_ ([Finster 12](#Finster12)) is a higher dimensional [[directed homotopy type theory|directed]] [[homotopy type theory|homotopy]] [[type theory]] for [[omega-categories]], i.e. of [[infinity-categories]] in the full sense of [[(infinity,infinity)-categories]].  Specifically it realizes the higher-dimensional [[horn]]-filler conditions in the definition of [[opetopic omega-categories]] [due to Palm](opetopic+omega-category#DefinitionByPalm) as [[inference rules]] of [[term introduction]] for a higher-dimensional kind of [[formal logic]] (but it presently ignores the saturation condition on the thin cells).

Where in [[homotopy type theory]] there is an [[identity type]] of any type axiomatizing the [[infinity-groupoid]] structure of that type in, effectively, the style of a [[globular omega-groupoid]], in opetopic type theory there is axiomatized instead a type of [[k-morphisms]] for all $k$ in the [[geometric shape for higher structures|shape]] of [[opetopes]].

Hence given a base type $\mathbf{B}\mathcal{U}$ -- and a priori there is just one, to be thought of as the categorically delooped [[type universe]], see below  -- a type is thus effectively identified with the shape of an [[opetope]] and thought of as the type of [[k-morphisms]] in $\mathbf{B}\mathcal{U}$, the only other data being a possible marking that identifies it as just the sub-type of $k$-[[equivalences]] of the given opetopic shape.

The only [[natural deduction|deduction rule]] is opetopic [[type formation]] and a [[term introduction]] rule which expresses the evident [[Kan complex|Kan filler-like]] condition saying that if a term of given opetopic shape is an outer [[horn]] (here: a "nook") of $k$-cells, then a $k$-dimensional filler term is deduced, and if an outer or inner [[horn]] has a boundary by equivalences then a filler term marked as an equivalence is deduced.

Due to the genuinely [[infinity-category|omega-categorical]] nature of the setup, it makes sense to think of the (a priori) unique base type $\mathbf{B}\mathcal{U}$ as the categorical [[delooping]] of a [[type universe]] $\mathcal{U}^\times$ being a [[monoidal (infinity,n)-category]] [[omega-category]], and hence of the 1-[[endomorphisms]] (hence the terms of shape the [[interval category|directed interval]]  $(\mathbf{B}\mathcal{U}\to \mathbf{B}\mathcal{U})$ ) as being the [[types]] in that universe. Composition of 1-morphism hence implies a [[type formation]] for [[multiplicative conjunction]]-types in a directed kind of [[linear homotopy type theory]].

Introducing an [[axiom]] to this system just means postulating terms of (the type of) the shape of prescribed [[opetopes]]. For example: 

* **$n$-truncation** -- For the language inside an [[(infinity,n)-category]] one demands that all [[k-morphisms]] for $k \geq n+1$ are marked as [[equivalences]];

* **$k$-adjoints** -- To axiomatize that two $k$-morphism are [[left adjoint]] and [[right adjoint]] to each other, respectively, one postulates the existence of $k+1$-morphisms serving as [[unit of an adjunction]] and [[counit of an adjunction]] and of a [[3-morphism]] marked as [[equivalence]] which axiomatizes the [[zig-zag identities]].

Imposing $n$-trunction and adjoints for all [[k-morphisms]] for $0 \leq k \leq n$ therefore axiomatizes the language for a [[free construction|free]] [[(infinity,n)-category with adjoints]] on a single object. Categorical looping (which is immediate and primitive in the system, as above) hence gives the [[free construction|free]] [[(infinity,n)-category with duals]] on a single object. 

This is the structure to which the [[cobordism hypothesis]] applies. Of course the proof of the cobordism hypothesis is not formulated in opetopic type theory and one would have to show that the language it is formulated in is suitably equivalent to that of opetopic type theory, but inspection in low dimension shows that the [[higher dimensional traces]] that opetopic type theory produces are of just the right kind.

## Related entries

[[!include proof assistants and formalization projects -- list]]

## References
 {#References}

Opetopic type theory is due to

* {#Finster12} [[Eric Finster]], _Type Theory and the Opetopes_, talk at [Polish Seminar on Category Theory and its Applications, June 2012](http://www.mimuw.edu.pl/~zawado/SemTK/OSTKA.html) 
([[FinsterTypesAndOpetopes2012.pdf:file]])


It [[syntax|syntactically]] implements the definition of [[opetopic omega-category]] due to 

* {#Palm} [[Thorsten Palm]], ...

by interpreting the higher-dimensional [[horn]]-filler conditions given there as [[inference rules]].

([Palm](#Palm) shows that any opetopic set satisfying these filler conditions satisfies the property of [[Michael Makkai]]'s definition of a opetopic set that qualifies as an [[opetopic omega-category]]. The converse is presently unknown.)


The higher dimensional [[string diagram]]-notation used here for opetopes was introduced (as "zoom complexes" in section 1.1) in

* {#KockJoyalBataninMascari07} [[Joachim Kock]], [[André Joyal]], [[Michael Batanin]], [[Jean-François Mascari]], _Polynomial functors and opetopes_ ([arXiv:0706.1033](http://arxiv.org/abs/0706.1033)) 

Animated exposition of this higher-dimensional string-diagram notation is in 

* [[Eric Finster]], _Opetopic Diagrams 1 - Basics_ ([video](http://www.youtube.com/watch?v=OANwLohwJqk))

* [[Eric Finster]], _Opetopic Diagrams 2 - Geometry_ ([video](http://www.youtube.com/watch?v=E7OvuA1jRKM))

A computer [[proof assistant]] for working with opetopic type theory is 

* [[Eric Finster]], _Orchard_ ([GitHub repository](https://github.com/ericfinster/orchard))

* [[Eric Finster]], _[Opetope!](http://sma.epfl.ch/~finster/opetope/opetope.html)_ (online opetopic type theory system)

A video tutorial for Orchard is 

* [[Eric Finster]], _Orchard 1 - Introduction_ ([video](http://www.youtube.com/watch?v=sEVJJCwohW0&list=PLWAw3zSOqFVKZ-LzAq4hQaKIVj8zjtfCs))

* [[Eric Finster]], _Orchard 2 - Modifying the shape_ ([video](http://www.youtube.com/watch?v=sEVJJCwohW0&list=PLWAw3zSOqFVKZ-LzAq4hQaKIVj8zjtfCs))

* [[Eric Finster]], _Orchard 3 - Composition and associativity_ ([video](http://www.youtube.com/watch?v=Vxnf_3Bxj2o&index=5&list=PLWAw3zSOqFVKZ-LzAq4hQaKIVj8zjtfCs))

* [[Eric Finster]], _Orchard 4 - Identities and invertibility_ ([video](http://www.youtube.com/watch?v=DRFjUSaNexQ&list=PLWAw3zSOqFVKZ-LzAq4hQaKIVj8zjtfCs&index=6))

Apparently Orchard is discontinued in favour of an online version of similar functionality:

* [[Eric Finster]], _Opetopic_ ([GitHub repository](https://github.com/ericfinster/opetopic)) ([Website](http://opetopic.net/))

Something like an implementation of aspects of opetopic type theory _within_ [[homotopy type theory]] is described in

* {#Finster18} [[Eric Finster]], _[[homotopytypetheory:Eric Finster, Towards Higher Universal Algebra in Type Theory|Towards Higher Universal Algebra in Type Theory]]_, [Homotopy Type Theory Electronic Seminar](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest.html) 2018 ([recording](https://www.youtube.com/watch?v=hlCVHVtAlqQ), [[Agda]] [code](https://github.com/ericfinster/higher-alg))

* {#AlliouxFinsterSozeau21} [[Antoine Allioux]], [[Eric Finster]], [[Matthieu Sozeau]], _Types are internal infinity-groupoids_, 2021 ([hal:03133144](https://hal.inria.fr/hal-03133144), [pdf](https://hal.inria.fr/hal-03133144/document))

