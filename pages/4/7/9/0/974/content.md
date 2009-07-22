A [[category]] $C$ is **locally presentable** -- sometimes called just **presentable** -- if


* $C$ is [[locally small category]]

* it has all small [[colimit]]s;

* there exists a [[set]] $S$ (i.e. not a proper class) of [[object]]s that generates $C$ under colimits

  (every object may be written as a colimit over a diagram in $S$)

* every object is a [[small object]],

More abstract, this is characterized by saying

* Locally presentable categories are precisely the categories of [[sketch|models of limit-sketches]].

# Remarks #

* A related notion is that of [[algebraic category|equationally presentable category]]. The "locally" in "locally presentable" is apparently usually used to distinguish from that notion.

* The generalization of the concept to the context of [[(infinity,1)-category|(infinity,1)-categories]] is [[presentable (infinity,1)-category]].


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
=--


[[!redirects presentable category]]