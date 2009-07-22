A [[category]] $C$ is **locally presentable** -- sometimes called just **presentable** -- if

* $C$ is [[locally small category]]

* it has all small [[colimit]]s;

* there exists a [[set]] $S$ (i.e. not a proper class) of [[object]]s that generates $C$ under colimits

  (every object may be written as a colimit over a diagram in $S$)

* every object is a [[small object]],

More abstract, this is characterized by saying

* Locally presentable categories are precisely the categories of [[sketch|models of limit-sketches]].


# Remarks #

*  In the Lab, we tend to use 'presentable' for a locally presentable category.  But another notion of when a category is 'presentable' is given by an [[algebraic category|equationally presentable category]].

*  The generalization of the concept to the context of [[(infinity,1)-category|(infinity,1)-categories]] is [[presentable (infinity,1)-category]].


#References#

The definition is due to

* P. Gabriel and F. Ulmer (1971)

See also section A.1.1 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]

where locally presentable categories are called just [[presentable category|presentable categories]].


#Discussion#

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

=--


[[!redirects presentable category]]