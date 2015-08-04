
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### In solid state physics
 {#InSolidStatePhysics}

In [[physics]], specifically in _[[solid state physics]]_, _elasticity_ is the tendency of solid materials to return to their original shape after being deformed. 

Mathematical elasticity theory ([Landau-Lifshitz 59](#LandauLifshitz59)) encodes the [[forces]] acting on a [[solid]] by a [[stress tensor]], and the amount of deformation by a _[[strain tensor]]_. 

One distinguishes different types of elasticity:

* linear elasticity: here the [[strain tensor]] is related by a [[linear equation]] to the [[stress tensor]] (a generalization of [[Hooke's law]]). To first [[infinitesimal]] order every type of material is approximately linearly elastic, the topic of _[infinitesimal strain theory](http://en.wikipedia.org/wiki/Infinitesimal_strain_theory)_.


* non-linear elasticity

  * hyperelasticity: exhibited by (soft) rubber

...

### Analogy with a quality of space
 {#AnalogyWithAQualityOfSpace}

Elasticity is commonly used as an illustration via [[analogy]] of the nature of [[space]] in [[physics]], specifically that of [[manifolds]] and [[spacetimes]].

#### In natural philosophy

In [[Georg Hegel]]'s _[[Encyclopedia of the Philosophical Sciences]]_ (1817) there is discussion (in the section _[Physik -- Die Koh&#228;sion](Science%20of%20Logic#Kohaesion)_) of the _[[cohesion]]_ and _elasticity_ of some [[substance]] which Hegel says is is the [[unity of opposites|unity]] of [[space]] and [[time]] ([PN&#167;261](Science%20of%20Logic#PN261)). 

#### In categorical logic / topos theory
 {#InCategoricalLogic}

[[William Lawvere]] argued that the "[[objective logic]]" of this discussion is to be formalized via [[categorical logic]] by the axiomatics of [[cohesive toposes]] (see there for references), i.e. by [[modal type theory]] equipped with [[shape modality]] and [[flat modality]].

But Hegel goes on to speak of cohesion being refined to _elasticity_:

> [PN&#167;297Zusatz](Science+of+Logic#PN297Zusatz) Elasticity is the whole of cohesion.

According to [PN&#167;298](Science+of+Logic#PN298) this elasticity is related to the [[unity of opposites]] that consistute [[Zeno's paradox of motion]], hence to the modern concept of [[differentiation]] via a [[limit of a sequence]].  In terms of [[categorical logic]] this is precisely what is encoded in the [[infinitesimal shape modality]] and [[infinitesimal flat modality]] of "[[differential cohesion]]" (see there for detail). 

Sticking to imagery from [[solid state physics]], these modalities are reminiscent of concepts in [infinitesimal strain theory](http://en.wikipedia.org/wiki/Infinitesimal_strain_theory). Notice that this applies to 

> {#RelativelyStiffElasticity} structures built from relatively stiff elastic materials 



#### Rubber-sheet geometry
 {#RubberSheetGeometry}

These modalities [above](#InCategoricalLogic) induce an axiomatization of _[manifolds and &#233;tale groupoids](differential+cohesive+%28infinity%2C1%29-topos#EtaleObjects)_ ("[[derived schemes]]") for which a common imagery in mathematics is given by elastic rubber sheets, reflecting the fact that these spaces on top of their [[cohesion]] have a more rigid [[shape modality|shape]], namely [[infinitesimal shape modality|infinitesimal shape]].

In this context the [[topology]] of [[manifolds]] is often referred to as _rubber-sheet geometry_ (e.g.[Wikipedia](http://simple.wikipedia.org/wiki/Topology), [Britton](#Britton)).


#### Elasticity analogy of gravity
 {#RubberSheetAnalogyOfGravity}


Moreover, these modalities [above](#InCategoricalLogic) induce an axiomatization of [[Cartan geometry]], hence in particular of [[pseudo-Riemannian geometry]] and hence of [[gravity]] ("[[general relativity]]") on these manifolds. 

<div style="float:left;margin:0 10px 10px 0;"><img src="http://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/GPB_circling_earth.jpg/450px-GPB_circling_earth.jpg" alt="mass curving spacetime" /></div>


A popular imagery for that illustrates the gravitational effect of massive bodies on light by a deformation of spacetime visualizes as an elastic wire frame. This is known as the _rubber-sheet analogy_ for gravity (e.g. [Das 11, p. 69](#Das), [Gabor](#Gabor), [Volk, fig. 4 on p. 537](#Volk)).

This seems to go back to the technical result of ([Sakharov 67](#Sakharov67)), which is informally summarized in the seminal textbook ([Misner-Thorne-Wheeler 73](#MisnerThorneWheeler73)) as saying that

> gravity is "an elasticity of space that arises from particle physics"

Further discussion of the analogy between the mathematical theory of elasticity and that of gravity include ([Tartaglia 95](#Tartaglia95),[Middleton-Langston 13](#MiddletonLangston13), [Wikipedia](#WikipediaRubberSheetModelForGravity)).

In order to think of not just [[topology]] but [[Riemannian geometry]] in the [above](#RubberSheetGeometry) context of elasticity, the _rigidity_ mentioned [further above](#RelativelyStiffElasticity) seems advisable. A _rigidly elastic_ body is to be expected to produce sound when struck. This is a common imagery in Riemannian geometry, as in "[[hearing the shape of a drum]]".



## Related entries

* [[formal smooth infinity-groupoid]]

* [[super formal smooth infinity-groupoid]]

* [[cohesion]], [[solidity]]

## References

### In solid state physics

* {#LandauLifshitz59} [[Lev Landau]], [[Evgeny Lifshitz]], _Theory of Elasticity_, part VII of  _[[Course of Theoretical Physics]]_, 1959, 1970

### As an analogy for topology/differential geometry

* {#Britton} Jill Britton, _[Rubber sheet geometry](http://jwilson.coe.uga.edu/EMT668/EMAT6680.F99/Estes/unit/dayten/topology1.html)_

### As an analogy for gravity

The "rubber-sheet analogy of gravity" might go back to results in

* {#Sakharov67} [[Andrei Sakharov]], _Vacvuum fluctuations in curved space and the theory of gravitation_, Doklady Akad. Nauk S.S.S.R. 177 70-71 (1967)

which were informally summarized in 

* {#MisnerThorneWheeler73} [[Charles Misner]], [[Kip Thorne]], [[John Wheeler]], _[[Gravitation]]_, 1973

* [[John Wheeler]], _Sakharov: A man of humility, understanding and leadership_, in _Andrei Sakharov, Facets of a Life_ ([GoogleBooks](https://books.google.co.uk/books?id=BTIziWmTX_0C&pg=PA647#v=onepage&q&f=false))

as saying that gravity is "an elasticity of space that arises from particle physics".

The mathematical similarity between gravity and the physics of elasticity is discussed further in 


* {#Tartaglia95} A. Tartaglia, _Four Dimensional Elasticity and General Relativity_ ([arXiv:gr-qc/9509043](http://arxiv.org/abs/gr-qc/9509043))

* {#MiddletonLangston13} Chad A. Middleton, Michael Langston, _Circular orbits on a warped spandex fabric_ ([arXiv:1312.3893](http://arxiv.org/abs/1312.3893), [talk video](https://www.youtube.com/watch?v=F80HIolrsoc))


The analogy is mentioned for expositional purpose for instance in 

* {#WikipediaRubberSheetModelForGravity} Wikipedia, _[Gravity well -- The rubber-sheet model](http://en.wikipedia.org/wiki/Gravity_well#The_rubber-sheet_model)_

* {#Gabor} Gabor, _[Gravity: Space as a rubber sheet](http://theory.uwinnipeg.ca/users/gabor/black_holes/slide5.html)_

* {#Volk} Greg Volk, _19th Natural Philosophy Alliance Proceedings_ ([online](https://books.google.de/books?id=tZnZAwAAQBAJ&pg=PA537&lpg=PA537&dq=manifold+"rubber-sheet"&source=bl&ots=WAhzUMxkOR&sig=p2qNCPCR9-gnPi6_nb1S_Bz3-AI&hl=en&sa=X&ei=8Ob2VLmSIcvNygOTjoGIBA&ved=0CCIQ6AEwAA#v=onepage&q=manifold%20%22rubber-sheet%22&f=false))

*  {#Das11} [[Ashok Das]], _Lectures on Gravitation_, WorldScientific 2011 ([publisher](http://www.worldscientific.com/worldscibooks/10.1142/7990), [GoogleBooks](https://books.google.de/books?id=oupB7VUGzGcC&pg=PA69&lpg=PA69&dq=manifold+"rubber-sheet"&source=bl&ots=ajbiJu7T_m&sig=MPsA2KWds_Mmf_UCscieaGVJzJk&hl=en&sa=X&ei=8Ob2VLmSIcvNygOTjoGIBA&ved=0CCUQ6AEwAQ#v=onepage&q=manifold%20%22rubber-sheet%22&f=false))



[[!redirects elasticity theory]]

[[!redirects rubber-sheet geometry]]
[[!redirects rubber-sheet analogy of gravity]]

[[!redirects elastic]]

