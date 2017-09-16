By analogy with [[poset]] and [[toset]], we may define a **proset** to be a set equipped with a [[preorder]].  This terminology is less common but tempting.

+-- {: .query}
[[Tim Porter]]: I see a potential problem with this terminology.   Proset has an already accepted meaning as a pro-object in Sets and that terminology dates back to early days of Grothendieck on Descent, so is well established. There are several situations in the various pages and entries that will lead to pro-objects (i.e. projective systems in ...) so feel it might be better to avoid the term proset here.

_Toby_:  Does one write that 'proset', 'pro-set', or both?

[[Tim Porter|Tim]]: It depends on how lazy one is feeling! I have used both. Pro-set is probably more correct, but the other does occur. It is perhaps unfortunate that poset is so well established otherwise 'porset' might be used with 'torset' etc as a consequence, but I wander!!!!

_Mike_: Good point, Tim!  Can't we just use "preorder" to mean "set equipped with a preorder"?  That usage seems to be fairly common.

_Toby_:  Well, you can if you want, but I don\'t.  Seriously, 'proset' is not something that I pulled out of thin air, and in fact I\'ve seen it more often than 'toset' (although that probably doesn\'t mean much given my interests).  Google `+proset preorder` to keep out the false positives and see its occasional independent usage for yourselves.  It\'s as good a term as 'poset'.

But don\'t let this matter be conflated with the weighty question of whether things should be kept at separate pages!  The distinction between [[linear order]] and [[loset]] is probably the best example of how they would look if kept separate, while [[apartness relation]] is probably the closest example of something where there is even now only one page.  (By 'things' here, I mean [[poset]]/[[partial order]] and [[toset]]/[[total order]] in addition to ones already considered.  Since a [[quasiorder]] cannot define equality, I don\'t think that [[quoset]] is necessary, and of course a [[woset]] is the same as (one kind of) [[ordinal number]], so it may not come up either; anyway, we haven\'t even written [[well-order]] yet.)

[[Tim Porter|Tim]]: On [[proset]] I suggest that we use the word 'synonym'! Something like, 'proset' is often used in the literature as a synonym for 'preordered set'.  This meaning should not be confused with that of a projective system in the category of sets, that is a pro-object in Sets.

I am not that worried about this, but do feel that we are hitting 'Disambiguation' problems at various points and may need a discussion on how we should handle those technically see the Wikipedia page on Disambiguation, which you all probably know well.

_Toby_:  [[simplicial category]] is pretty much a disambiguation page, although with some content too.  There a couple of others like it.

[[Tim Porter|Tim]]:  I had noticed that as a good example of how one might proceed. We don't necessarily need a single way of doing this Disambiguation, but rather one or two examples of what we collectively think of as 'good practice'. 

Perhaps also I should create an entry on pro-objects which would link with profinite groups. (More work!)

Your other point about separate pages needs thought.  My view would be that we need to think both of the main users (i.e. us an co!) and external users since as we make reference to the nLab more and more people are likely to use it as one entry point for definitions etc. 

[[Mike Shulman|Mike]]: Toby, I wasn't saying you pulled "proset" out of thin air; I've never seen it in the literature but clearly I read different literature than you do.  (-:  My point was rather about what terminology we should use here on the nLab.  I think having "proset" be a disambiguation page is a good idea, but since there is potential ambiguity I would prefer that we avoid its use elsewhere on the nLab.

I'm all in favor of having lots of pages, but I'm not really in favor of duplicating _content_.  I'd rather have [[toset]] just link to [[total order]], which in turn mentions that "toset" is a sometimes-used terminology for "totally ordered set."

_Toby_:  Mike, except for briefly summarising a definition, there is no content duplicated between [[linear order]] and [[loset]].  (Some of the other pairs haven\'t been cleaned up so well, but I will happily do that.)  So my question is, is that a better way of organising things, or is [[poset]] (from which I have removed nothing to [[partial order]] yet) a better way?

I am torn.  If the original page names [[poset]] and [[preorder]] had been consistent (one way or the other), I\'d have just gone with it.  (I have a better formed opinion that *if* we put everything on one page, then [[preorder]] is better and [[poset]] is worse.)  If we have to make an except for [[proset]], then that\'s a different matter.  (Although I think that we should be able to distinguish [[proset]] from [[pro-set]] if we want.)

Tim, I would like to see [[pro-object]] (which I see you have already written!) and [[pro-set]], but I don\'t think that you have to write them just to convince me that 'proset' can be ambiguous.  I\'ll take your word for it that these are useful concepts.

[[Mike Shulman|Mike]]: No, there is no actual content duplicated between [[linear order]] and [[loset]], but it seems completely arbitrary to me which content is on which of the two pages.  Shouldn't the examples be on the same page that gives the definition and other discussion?

I actually don't think that [[poset]] and [[preorder]] are inconsistent, since as I said, "preorder" can mean the same thing as "set equipped with a preorder."  This is actually fairly common, especially in set theory one speaks of "a linear order" or "a well-ordering" without specifying explicitly the set on which it lives (since, of course, it has to live on some set).  It's a similar sort of abuse to when we say "let $G$ be a group" rather than "let $(G,\cdot,e)$ be a group" (only maybe in reverse).

_Toby_:  Ha, it\'s funny that you say that 'let $G$ be a group' is in reverse, since I think of that as perfectly correct and later discussion of $G$ as a mere set to be the abuse.  But anyway ...

The difference between [[loset]] and [[linear order]] is that the latter is about all of the linear orders that can be put on a set, while the former talks about only one set at time (at least one set per linear order, there should also be stuff about morphisms).  As the set of linear orders on $S$ forms a subcategory of the category of all linearly ordered sets, there is a certain amount of arbitrariness there, but I think no more than in other fine distinctions.

Do you really not see how having both [[preorder]] and [[poset]] was inconsistent?  Yes, you can speak of a 'preorder' or a 'linear order' or a 'well ordering' without specifying the set ahead of time, but the same thing is true of a 'partial order'!  All in all, I see your arguments as suggesting that we should put everything on the same page, and that page should be [[preorder]]/[[partial order]]/etc rather than [[proset]]/[[poset]]/etc, but you make an arbitrary exception for [[poset]] (and maybe [[toset]], that\'s not clear).

_Mike_: Okay, there's a fine distinction between what's on [[loset]] and what's on [[linear order]].  But I don't think its a fine distinction worth perpetuating; I have trouble imagining someone wanting to read what's on one of those pages but not what's on the other one.  Is there a specific reason not to put all the content on one page and have the other one be a redirect?

I admit that having both preorder and poset is not completely uniform terminology, but I draw a fine distinction between nonuniformity and inconsistency.  (-:O  However, if you really want uniform terminology, I would be okay with putting everything on [[preorder]], [[partial order]], [[total order]], etc. with [[proset]], [[poset]], [[toset]], etc. as redirects.

_Toby_:  The way I envision someone reading [[linear order]] but not [[loset]] (the converse is unlikely) is if they\'re reading about some subject on the wiki and someone remarks that such and such is a linear order.  They don\'t know what that is, or just want to review the definition, so they read [[linear order]], read the definition, learn that classically they can think of it as the same as a total order, etc.  Obviously the definition of [[loset]] is there (with a link if they want more), but they don\'t need to see examples or learn about morphisms between them, since they\'ve already got an example on the referring page, and that\'s the only that\'s relevant.

I can see the other side too, however.  Just put it all on one page and let people read whichever sections they want.  Given the links and pages on the wiki when I decided to write all of this, it was most natural to write things separately, but if you\'re convinced that it\'s better to have them combined, then I can accept that too.

_Mike_: I do think it's better to have them combined.  It might be nice if we could get a third opinion, but apparently no one else is paying much attention to our petty disputes.  (-:


[[Tim Porter|Tim]]  I could not ignore that last comment so here is my pennyworth! Too many unnecessary links may be a bad thing.  Why not have something of the form 'Most common terminology' then small list of synonyms after the definition i.e. near the top.  If someone then want to use loset rather than linear order they can then use  linear order|loset88 (where 8 stands for a square bracket either right or left. Clicking on loset will bring up the definition and the word loset will be bold (or whatever) and they can see it more or less immediately. There can also be warnings such as I felt were needed about proset i.e. 'proset' can also refer to a pro-object in the category of sets. For more on that meaning click ****** .

_Mike_: Yes, I like that.  I think it would be even better if we could do like Wikipedia does and have loset automatically redirect to linear order, but instiki doesn't appear to have that capability.

_Toby_:  Well, I guess that I\'ll move things around then.  We can still discuss whether [[proset]] should simply redirect to [[preorder]] or should be a more explicit disambiguation page.  (For now, I\'ll move things so that it redirects, but I\'ll do that last, so feel free to make more comments in the meantime.)

=--
