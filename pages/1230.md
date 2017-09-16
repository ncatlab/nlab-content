See [[n-fibration]].

+--{+ .query}
[[Zoran Skoda]]: I like the expansion (by Mike I guess) which is now in the entry n-fibration, it is instructive and a strong novelty of the nlab (is there more to read on the weak case somewhere?). However, I would prefer that for the case of STRICT n-categories, for which I intended the fibered n category entry when I created it; that we keep the original name and original definition (thus talking about n-cartesian
cells, regardless that it is evil, and one should expand on that). Grothendieck, Gabriel and Gray discovered fibered (strict) 1- and 2- categories and called them fibered 1- or 2-categories; Hermida generalized to strict n and Bunge is following , also under the same name: so let us keep the explicit version for the strict n-categories under the name fibered n category and with "evil" definition (which is very useful in my practice, at least for n=2); and lets us keep homotopically-biased title n-fibration for the weak n-category version. Of course, no hurry, in due time...And also having an entry fibered 2-category for the case of strict 2-categories where hermida has two different but equivalent definitions. Does that make sense to you ? Mike, Toby, Urs ?

[[Toby Bartels]]:  If these are useful to you, then we should certainly have an article on them.  But can we put it at [[strict fibered n-category]]? (or [[fibered strict n-category]] if you don\'t want to imply that there\'s anything strict about how the strict $n$-category is fibred).  Besides the hyphen (which is a technicality), one of the biases of the $n$-Lab is that the default notion of $n$-category is weak.  Of course, people who work with strict $n$-categories don\'t share that bias, so we won\'t quite match their language.

[[Mike Shulman|Mike]]: I'm with Toby.  When we mean strict, we should say strict.  I don't think '$n$-fibration' is 'homotopically biased' either; plenty of people say 'fibration' rather than 'fibered category.'

The level of strictness in Hermida's definition is a bit puzzling to me.  A 2-fibration $E\to B$ in his sense corresponds to an (appropriately contravariant) functor $B\to 2Cat$, but neither to a fully strict 3-functor nor a fully weak one.  (This has nothing to do with the evilness of requiring on-the-nose cartesian lifts rather than up-to-iso ones, that is rather about strictness of the equivalence between fibrations and pseudofunctors.)  But if you think it is important, we should certainly have a page on it.

[[Zoran Skoda]]: I am not really a conformer to the nlab conventions, I always say weak when I mean weak in my own work; but I am happy with conforming in the nlab entry (i just did not think of weak case when writing the oroiginal entry). I also agree iwth the hyphen, I noticed that afvter submitting v1. As far as "plenty of people say 'fibration' rather than 'fibered category.'" Yes, people doing homotopy/topology, not a single algebraic geometer, 
who are the main consumers of
Grothendieck's definition, and have direct and inverse image functors all over the place. Thus the terminology is homotopically biased, at least in social sense. I am a bit puzzled about the statement of semi-strictness you say; I used this definition in a number of examples of mine and it was always working' maybe my perception of what should be a 2-pseudofunctor is not good as well. But one should also compare with Gray's universal property in the formal/adjointness book. I think fibered strict n-category is better than strict fibered n-category. The thing is that sometimes in expositions people use fibered category actually for pseudofunctor, then one would think that strict
in the sense of functor. There is also a curiousity (used by Thomason) that Grothendieck construction works for lax functors in fact. Gorghendieck construction for n=2 has been studied by hermida (though he has just few words on it) so I doubt he woudl not have the correspondence with teh coprrect generality of 2-pseduofunctors. Igro and I were doing some ground work on the 2-Groth constr but we did not do complete equivalence of 2-categories, just some other aspects, so i can not claim myself. 

_Mike_: I don't always use the nLab terminology in my own work either; I tend to be more Australian and say "2-category" for the strict notion.  But I've been convinced that it is valuable for the nLab to have a consistent terminological convention, and for $n\gt 2$ the weak notions are (most of us believe) so much more important than the strict ones that they deserve the unadorned name.

And I agree that "fibered strict $n$-category" is better than "strict fibered $n$-category," although perhaps "strictly fibered strict $n$-category" would be even better in view of the relative strictness of Hermida's definition.  If I am remembering correctly, I think that Hermida's 2-fibrations over a 2-category $B$ correspond to pseudofunctors from $B^{coop}$ into $Str2Cat$, the 2-category of strict 2-categories, strict 2-functors, and strict 2-natural transformations.  A fully weak version would of course land in the 3-category of 2-categories, (weak) 2-functors, (pseudo) natural transformations, and modifications.

I disagree that algebraic geometers are the main consumers of fibrations.  They are used plenty by category theorists as well, and people working in related fields such as categorical topology.  (And they _should_ be used by more topologists, an oversight I am working to correct.)

Yes, actually the category of elements (aka lax colimit, aka one of Grothendieck's constructions) works for lax functors landing in $Prof$ and not just in $Cat$, and that way it recaptures all functors, not just fibrations.  Probably there is a similar version of this in the $n$-case.

[[Zoran Skoda]] Yes, Hermida has pseudofunctors into 2Cat;
the target is strict but the pseudo- is in the weakest 3-categorical sense. I think "strict fibration of strict n-categories" is unnecessarily precise: you see if one wants to consider strict categories as non-strict then one can just say that; I think that fibration of strict n-categories is enough; one can always in concrete case say fibration of n-categories where the domain and target happen to be 
strict. For an example, look at the category of internal categories (taken as descent data in the spirit of MacLane-Pare article) in an indexed category is a 2-fibered strict 2-category. There is a reason more, that I woudl not like "strict fibered strict n-catgeory"; usually one starts 
developing theory by saying what a category over category is; so here what a strict 2-category over a strict 2-category is; prefix fibered is just about modifying this
to a sub-2-category of such. So really starting with strict 2-categories viewed as nonstrict, means that we modify nonstrict (2-category over 2-category); but if you are strongly inclined it is OK, at least for the lexicon. 

[[Mike Shulman|Mike]]: I am skeptical that the pseudo- is in the weakest 3-categorical sense; what reference are you looking at?

I wasn't really serious about "strictly fibered strict $n$-category;" I think [[fibered strict n-category]] would be fine.

[[Zoran Skoda]]: In my memory, Igor checked that the Gordon-Power-Street style of a weak 3 functor when the codomain is 2Cat as a strict 3 category, and domain is a strict 2-category in the case of invertible coherences corresponds to what is the input for Grothendieck construction for Hermida case. I did not check his calculation (whose outcome was partly even typed). We did not check if the Grothendieck construction gives an equivalence of 2- or 3- categories of such objects; it would be more work. 
=--

category: redirect
