
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The following terminology for the ([[higher morphism|higher]]) [[morphisms]] in the [2-category of monads](monad#BicategoryOfMonads) have appeared in the literature or are otherwise sensible:

| author(s) | [[1-morphisms]] | [[2-morphisms]] |
|---------|-----------------|-----------------|
| [Frei 1969](#Frei69), <br/>[Pumplün 1970](#Pumplün70), <br/> [Borceux 1994](#Borceux94) | "morphisms of monads" | ---  |
| [Street 1972](#Street72) | "monad functors" | "monad functor transformations" |
| [Moggi 1989](#Moggi89) | "monad-morphisms" | --- |
| [Espinosa 1995](#Espinosa95), <br/> [Liang, Hudak & Jones 1995](#LiangHudakJones95) | "[[monad transformers]]" ${}^1$ | ---
| [Lack & Street 2002](#LackStreet02) | "monad morphisms" | "monad transformations" |
| --- | "monad [[1-morphisms]]" | "monad [[2-morphisms]]" |
| --- | "[[lax natural transformation|lax transformations]]" of monads | "[[modifications]]" of monads |

${}^1$: Notice here that the "[[monad transformers]]" in [Espinosa 1995](#Espinosa95), [Liang, Hudak & Jones 1995](#LiangHudakJones95) (as commonly understood now in [[Haskell]]) are indeed 1-morphisms of monads, but understood with additional structure, namely appearing in [[natural transformation|natural]] families constituting a [[pointed endofunctor]] on the category of monads (made explicit in [Winitzki 2022 p. 474](#Winitzki22)).

Of course, monads are often referred to via their [[underlying]] [[functors]], the morphisms between which are, of course, commonly known as *transformations*, too: [[natural transformations]]. Therefore (for the usual monads in [[Cat|$Cat$]]) monad morphisms are, in any case, *natural transformation of functors, respecting their monad structure*.

Similarly, if one thinks of monads as [[lax functors]] $\ast \to Cat$ (which is where they get their name from!, see [here](monad#Etymology)) then their 1-morphisms are by default to be called *[[lax natural transformations]]* (and their 2-morphisms *[[modifications]]*).


## Related entries

* [[monad transformer]]

* [[transformation of adjoints]]

## References

* {#Frei69} [[Armin Frei]], *Some remarks on triples*, Mathematische Zeitschrift **109** (1969) 269–272 &lbrack;[doi:10.1007/BF01110118](https://doi.org/10.1007/BF01110118)&rbrack;
   
* {#Pumplün70} [[Dieter Pumplün]], *Eine Bemerkung über Monaden und adjungierte Funktoren*, Mathematische Annalen **185** (1970) 329-337 &lbrack;[eudml:161964](https://eudml.org/doc/161964), [[Pumpluen-Monaden.pdf:file]]&rbrack;

* {#Street72} [[Ross Street]], *The formal theory of monads*, Journal of Pure and Applied Algebra **2** 2 (1972) 149-168 &lbrack;<a href="https://doi.org/10.1016/0022-4049(72)90019-9">doi:10.1016/0022-4049(72)90019-9</a>&rbrack;

* {#Moggi89} [[Eugenio Moggi]], *An abstract View of Programming Languages*, LFCS report ECS-LFCS-90-113 (1989) &lbrack;[web](http://www.lfcs.inf.ed.ac.uk/reports/90/ECS-LFCS-90-113), [[Moggi-AbstractView.pdf:file]]&rbrack;

* {#Borceux94} [[Francis Borceux]], Def. 4.5.8 in: *[[Handbook of Categorical Algebra]]*, Vol. 2: *Categories and Structures*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865)&rbrack;

* {#Espinosa94} [[David A. Espinosa]], *Building Interpreters by Transforming Stratified Monads* (1994) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-StratifiedMonads.pdf:file]]&rbrack;

* {#Espinosa95} [[David A. Espinosa]], *Semantic Lego*, PhD thesis, Columbia University (1995) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-SemanticLego.pdf:file]], slides:[pdf](https://github.com/davidespinosa01/papers/blob/346c2ded6af78805701106d51daee8f7a756c948/E/Espinosa%20David/espinosa-thesis-slides.pdf), [[Espinosa-SemanticLego-slides.pdf:file]]&rbrack;


* {#LiangHudakJones95} Sheng Liang, [[Paul Hudak]], [[Mark Jones]], *Monad transformers and modular interpreters*, POPL '95 (1995) 333–343 &lbrack;[doi:10.1145/199448.199528](https://doi.org/10.1145/199448.199528)&rbrack;

* {#LackStreet02} [[Stephen Lack]], [[Ross Street]], *The formal theory of monads II*, Journal of Pure and Applied Algebra **175** 1–3 (2002) 243-265 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00137-8">doi:10.1016/S0022-4049(02)00137-8</a>&rbrack;

* {#Winitzki22} [[Sergei Winitzki]], Section 14 of: *The Science of Functional Programming -- A tutorial, with examples in Scala* (2022) &lbrack;[leanpub:sofp](https://leanpub.com/sofp), [github:sofp](https://github.com/winitzki/sofp)&rbrack;





  


[[!redirects monad transformations]]

[[!redirects monad morphism]]
[[!redirects monad morphisms]]

category: disambiguation
