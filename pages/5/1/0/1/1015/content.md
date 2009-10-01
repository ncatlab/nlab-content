A __set theory__ is a theory of [[sets]].

__Na&#239;ve set theory__ is the basic algebra of the [[subsets]] of any given set $U$, together with a few levels of [[power sets]], say up to $\mathcal{P}\mathcal{P}\mathcal{P}U$ and possibly no further.  Often students see this first for the set of [[real numbers]] as $U$ (although in fact one could start with the set of [[natural numbers]] and go one level further for an equivalent theory).  One could also use [[function sets]] instead of power sets as the basic set-forming operation (especially for a [[predicative mathematics|predicative]] theory).

Once you start thinking very much about the nature of sets in general (rather than merely _using_ na&#239;ve set theory), it quickly becomes clear that one must be careful about how one can and cannot form sets.  Georg Cantor is credited with being the first to think about sets this deeply; although he did not propose a system of general rules for valid set-making operations, he recognised that some sets were 'inconsistent'.  Gottlob Frege\'s set theory was found (by Bertrand Russell) to be logically trivial because he was too careless in this regard.

There are two ways to go about doing a more careful __axiomatic set theory__.  The more ambitious is to develop a __foundational set theory__:  set theory as [[foundations]] for all of mathematics.  This is what Frege proposed (although he failed through inconsistency); Ernst Zermelo is credited with the first consistent foundational set-theory.  A variation of Zermelo\'s system (developed by Fraenkel and Skolem and called Zermelo--Fraenkel set theory or ZFC) is the orthodox foundations today, although it needs to be supplemented by [[Grothendieck universes]] (or something along those lines) to handle modern [[category theory]].

On the nlab we distinguish between two types of foundational set theory: __material set theory__ and __structural set theory__.  ZFC is an example of a material set theory, while [[ETCS]] is an example of a structural one.

The distinguishing feature of a material set theory (also called a *membership-based set theory*) is that the elements of a set exist  before the set does; a set merely collects a bunch of pre-existing objects as its elements. 

+--{: .query}
[[Arnold Neumaier]]: I doubt that this statement means anything. ZF has no notion of time, hence nothing exists there before anything else. In a model of ZF all sets exist simultaneously, and without a model of ZF no set exists.
Thus the notion of pre-existence might be a property of your private model of ZF (which apparently has extra accidental structure) but it is not one of ZF.

Thus I am at a loss to see what this distinguishing feature should mean. 

[[Todd Trimble]]: It seems clear to me that the preceding paragraphs are written informally, trying to convey a _feeling_ behind what is meant (here) by "material" vs. "structural". So the objection about the formal theory ZF seems improper --- let's give Mike some credit; he knows very well there's no concept of time in the formal theory. 

By "pre-existing", I think he means that _given_ a bunch of objects, you can (under pretty general conditions, made precise by ZF for instance) collect them into a set. He actually said that, I just noticed. But structural set theories work a bit differently. 

=--

Frequently in material set theory one takes everything to be a [[pure set]], including the elements of sets themselves.   Therefore, any two sets may be meaningfully compared to ask if they are [[equal]] or if one is a member of the other.  As a slight variation (still material set theory), one may also accept ur-elements (or atoms) as elements.  The main distinguishing feature of a material set theory is a global membership predicate, whereby it is meaningful to ask, given any object and a set, whether the object is an element of the set.

+--{: .query}
[[Arnold Neumaier]]: Here is a second attempt to define the distinguishing feature. is that supposed to be an equivalent form of the previous one, or a different one? 
What if only one of the features are present? 

[[Todd Trimble]]: If I may presume to speak again before Mike, I gather that he is elaborating on what the sorts of (informal) collecting-into-sets operations typical for the spirit of material set theory would entail for the basic _shape_ or form that the axiomatic theories actually take. In other words, to axiomatize those sorts of operations, one needs to posit a global membership relation/predicate -- at least that's the case for all such known theories. 

_Toby_:  I like the latter 'distinguishing feature', so much that I\'m surprised that I didn\'t write it myself!  All that stuff about time is just a metaphor.
=--

A structural set theory, on the other hand, looks more like [[type theory]].  Here, the elements of a set have no existence or structure apart from their identity as elements of that set. 
+--{: .query}
[[Arnold Neumaier]]: Do you mean by this that they are not pre-existent in your private model of it?
=--
In particular, they are not themselves sets, and cannot be elements of any other set.  Thus, elements of different sets cannot be compared (by default) and no two sets can be compared for equality.  Among category theorists, it\'s popular to state the axioms of a structural set theory by specifying elementary properties of [[Set|the category of sets]]; the orthodoxy here (to the extent that there is one) is probably Bill Lawvere\'s [[ETCS]].  It is weaker than ZFC and must be supplemented to handle some esoteric parts of modern mathematics, although it suffices for most everyday uses.  Another structural set theory, which is stronger than ETCS and less closely tied to category theory, is [[SEAR]].

As remarked above, both material set theory and structural set theory are **foundational set theories**.  
+--{: .query}
[[Arnold Neumaier]]: ''As remarked above'' suggests that pure set theory is synonymous with material set theory.
May I conclude that the pure set theory constructed 
elsewhere in the n-Lab within ETCS is a material set 
theory? Thus a structural set theory has material aspects? 

_Toby_:  I wouldn\'t conclude anything like that from comparing different articles in the Lab.  They\'re written by different people, usually without consultation.  Not that there\'s anything wrong with your question!  But my answer is simply that the word here should be 'material' rather than 'pure'.  (However, I would also agree that both material and structural foundations have aspects of each other in them, in the sense that the basic concepts of each can be formalised in the other.)
=--
It is also possible to make a **definitional set theory**, in which one defines sets in terms of some more primitive concept.  Lawvere also proposed a foundation based on [[Cat|the category of categories]]; then a set may be defined as a [[discrete category]].  In [[constructive mathematics]], a foundation based on [[type theory]] is popular, with types interpreted as _[[tobybartels:preset|presets]]_ (sets without [[equality]]); then a set may be defined as a preset equipped with an [[equivalence relation]] (the term [[setoid]] is also used for such a gadget).  In [[computer science]], a foundation based on the [[lambda-calculus]] is sometimes seen; in these terms, the concept of _[[list]]_ is more natural than set, with the difference being that sets have a coarser notion of equality.

Category theory can provide a common [[model theory]] to compare all of these notions.  Although only structural set theories like ETCS treat the elementary properties of the category $Set$ of sets as fundamental, one can ask for any set theory what properties $Set$ satisfies and compare them in those terms.  At the very least, $Set$ should be a [[pretopos]].


# Remarks #

* There is also [[algebraic set theory]], in which a material set theory (such as ZFC) is interpreted in the [[internal logic]] of some [[ambient category]], often called a "category of classes".


[[!redirects material set theory]]
[[!redirects structural set theory]]
