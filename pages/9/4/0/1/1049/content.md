
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contemts#
* table of contents
{:toc}

## Definition

A **bimorphism** is a morphism which is simultenously [[epimorphism|epic]] and [[monomorphism|mono]]. Such a morphism in general does not need to be [[isomorphism|iso]]. If every bimorphism in a category is an [[isomorphism]] we say that the category is [[balanced category|balanced]]. 


## Discussion

+--{: .query}
[[Mike Shulman|Mike]]: I don't like the word "bimorphism."  If I've been thinking about [[bicategory|bicategories]] then it sounds like something that is "a morphism up to isomorphism," while if I've been thinking about [[biproduct|biproducts]] it sounds like something that is "both a morphism and a comorphism."  Are monic epics really an important enough concept to deserve its own word?  Can't we just say "monic and epic" or even just "monic epic"?

_Toby_:  It makes sense to me.  Using 'bi' in bicategories is bad anyway.  But it's much like 'bi' in 'biproduct', although I suppose technically one ought to say 'bimonomorphism'.  You\'re right that they may not be that important; I see them mostly as a way to say give counterexamples to the na&#239;ve student's guess that all categories are balanced.  But then, are balanced categories an important concept?

_Mike_: Of course, "bi" in bicategories is bad, but because of people who are used to "bi-" meaning "weak" I think it is better to avoid "bi-" altogether whenever possible.  I wouldn't object too strongly to "bimonomorphism."  But "monic epic" is the same number of syllables as "bimorphism," fewer syllables than "bimonomorphism," and its meaning is (to me) more obvious than either.

I don't think that balanced categories are a very important object of study in their own right, but it is sometimes useful to know that a particular category, or a particular type of category (such as a [[pretopos]]), is balanced.

_Toby_: As it doesn\'t matter too much, we can avoid 'bimorphism' here. But surely you realise that it\'s cheating to compare 'monic epic' and 'bimonomorphism'; you can compare the adjectives 'monic epic' and 'bimonic' or compare the nouns 'monic epimorphism' and 'bimonomorphism' (or compare their abbreviations 'monic epi' and 'bimono' if you like those, although I tend not to use those in writing).

_Mike_: Yes, of course you're right for the syllable count.  I still maintain that the _meaning_ of "monic epic" is more obvious than either "bimorphism" or "bimonic," which is the more important thing, especially for a little-used concept.

_Mike_: I just remembered another reason I dislike "bimorphism."  One context where people use it is in the study of [[reflective subcategory|reflective]] subcategories, where one talks about "mono-reflective" and "epi-reflective" subcategories to mean that the unit of the reflection is monic or epic, and some people say "bireflective" to mean that the unit is a bimorphism.  But to me, bireflective "obviously" means "reflective and coreflective;" this confused me for quite a whole once.

_Toby_:  O yeah, I agree with you there!  The best that I can say for 'bimorphism' is that it\'s got some sense to it; but as the right way to follow that sense would be 'bimonomorphism', there\'s still something wrong with it.

_Zoran_ I am used to say "reflective and coreflective", never bireflective. Looks esoteric term. I never likes bimorphism either.
=--

[[!redirects bimorphisms]]