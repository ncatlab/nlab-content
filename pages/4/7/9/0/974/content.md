<div class="rightHandSide toc">
[[!include compact object - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A locally presentable category is one where every [[object]] is a [[colimit]] over a [[set]] of [[small object]]s.

## Definition ##

A [[category]] $C$ is called **locally presentable** if

* $C$ is [[locally small category]];

* it has all small [[colimit]]s;

* there exists a [[set]] $S$ (not a proper [[class]]) of [[object]]s that generates $C$ under colimits

  (every object may be written as a colimit over a diagram with objects in $S$)

* every object is a [[small object]],

More abstractly, this is equivalently characterized by saying

* Locally presentable categories are precisely the categories of [[sketch|models of limit-sketches]].

### Variations ###


* If the generating set $S$ consists of $\kappa$-small objects (usually called "$\kappa$-presentable" in this context), then the category is said to be "locally $\kappa$-presentable."  Of particular importance are [[locally finitely presentable categories]], the special case when $\kappa=\omega$.

*  The generalization of the concept to the context of [[(infinity,1)-category|(infinity,1)-categories]] is [[presentable (infinity,1)-category]].



### Terminology ###

The _locally_ in _locally presentable category_ refers to the fact that it is the _objects_ that are presentable, not the category as such:

(For instance, consider the notion of "locally finitely presentable category," in which the generating set $S$ consists of [[finitely presentable object]]s, i.e. $\omega$-small ones. If you drop the word "locally" then you would get "[[finitely presentable category]]" which means something completely different, namely a finitely presentable ($\omega$-small) object of [[Cat]].)

Another notion of "presentable category" is [[algebraic category|equationally presentable category]].


## Examples and applications ##

### Locally finitely presentable categories ###

A locally presentable category is _finitely_ presentable if it is locally $\kappa$-representable for $\kappa = \Aleph_0$.

* [[Set]] is locally finitely presentable: every [[set]] is the directed colimit of all its finite [[subset]]s, and there is a countable set of finite sets.

* Analogously categories such as [[Grp]] are locally finitely presentable.

* a [[poset]], regarded as a category, is locally finitely presentable if it is a complete [[lattice]] which is algebraic (each element is a directed [[join]] of finite elements).

**Counterexamples**

* the category [[FinSet]] of _finite_ sets is not locally finitely presentable, as it does not have all countable colimits.

* [[Top]] is not locally finitely presentable.

### Locally presentable categories

* the category [[SSet]] of [[simplicial set]]s;

* for $C$ a [[small category]], the [[functor category]] $Funct(C,SSet)$. 

### Combinatorial model categories ###

A [[combinatorial model category]] is a [[model category]] that is in particular a locally presentable category.

The left [[Bousfield localization]] of a left [[proper model category|proper]] [[combinatorial model category]] is again combinatorial and hence again locally presentable. 


## References ##

The definition is due to

* P. Gabriel and F. Ulmer (1971)

The standard textbook is

* Jiri Adamek, Jiri Rosicky, _Locally presentable and accessible categories_

See also section A.1.1 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]

where locally presentable categories are called just [[presentable category|presentable categories]].


## Discussion ##

A previous version of this entry led to the following discussion.

+-- {: .query}
Do you mean __*locally* presentable__?  Or are you following Lurie now?  Should we change the terminology below?

[[Urs Schreiber]]: oh, sorry, this is a result of bad copy-and-pasting, I had meant to type locally presentable -- but now that we are discussing this, maybe we can sort this out: what's the point of saying "locally" presentable? Which reasons would there be not to follow Lurie on this? 

_Toby_:  The only thing that I can think of offhand is to distinguish from [[algebraic category|equationally presentable category]].  (Actually, what I really mean is that if I Google `"presentable category"`, then I mostly get hits with 'locally' in them, and if I Google `"presentable category" -locally`, then I mostly get hits with 'equationally' in them.)

[[Urs Schreiber]]: I have changed the wording in the first sentence now.

_Toby_:  OK.  Is there any reason for having [[presentable category]] separate now?  (Or not to move this to [[presentable category]]?)

Incidentally, how related is an equationally presented category?  It seems to me not much ....

[[Urs Schreiber]]: right, so I flagged [[presentable category]] for deletion

and I removed the "related" in the sentence on equationally presented categories -- I don't actually know what these are! 

But I guess the point remains that "locally presentable category" serves to distinguish from "equationally presentable category".

On the other hand, _locally_ presentable then still seems like a bad choice of terminology, as it indicates nothing about the kind of presentation and in fact it remains a mystery to me what is supposed to be local about the above notion. (It's not the local smallness, or is it?) 

But then it gets a bit worse even when we look at the generalizations. I have firmly followed Lurie with the terminology at [[presentable (infinity,1)-category]] that is supposed to generalize the notion here, and there it turns out to be pretty good terminology, as those $(\infty,1)$-categories are, among a whole list of equivalent characterizations, precisely those that are given by combinatorial simplicial model categories. I have used that nice fact to consistently say "a model category [[presentable (infinity,1)-category|presents]] an $(\infty,1)$-category" with the "presents" linking to _presentable $(\infty,1)$-category_ .

Anyway, with this entry being titled _locally presentable category_ and having a redirect from presentable category we seem to be at least on the safe side.

_Toby_:  OK.  Remember when making an existing page into a redirect now, you should also change its name to something with `-- history` in it so that the redirection will work.  (And remove the automatic redirection command that this creates in the history page.)  I\'ve done that now.

_Urs_: ah, thanks. What's that last step? Do we have a HowTo on that?

_Toby_:  It\'s discussed very briefly at [[redirect]]; you can find much more on the Forum [here](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=16&page=1#Item_33).  But I probably should write something clear at [[HowTo]].

[[Mike Shulman]]: Coming into this discussion late, let me speak up in favor of "locally presentable."  I agree that "locally" is a poor choice (and an overworked word), but the important point is that it is the _objects_ of the category which are presentable, rather than the category itself.  For instance, consider the notion of "locally _finitely_ presentable category," in which the generating set $S$ consists of finitely presentable objects, i.e. $\omega$-small ones.  If you drop the word "locally" then you would get "finitely presentable category" which means something completely different, namely an $\omega$-small object of [[Cat]].
=--

+-- {: .query}
[[Mike Shulman]]: I agree that "locally" is a poor choice (and an overworked word), but I think that merely "presentable" is worse; some adjective must be used and "locally" has the weight of history behind it.  The important point requiring the adjective is that it is the _objects_ of the category which are presentable, rather than the category itself.  For instance, consider the notion of "locally _finitely_ presentable category," in which the generating set $S$ consists of finitely presentable objects, i.e. $\omega$-small ones.  If you drop the word "locally" then you would get "finitely presentable category" which means something completely different, namely an $\omega$-small object of [[Cat]].

I'm guessing that when you say "presentable category" you are thinking of the set $S$ as "presenting" the category in some way, but I think this is wrong.  The notion of "presentable object" has a precise meaning in the very theory we are discussing, so we shouldn't apply it unqualified to the category as well with a different meaning.
=--



[[!redirects presentable category]]
[[!redirects locally presentable categories]]
[[!redirects presentable categories]]
