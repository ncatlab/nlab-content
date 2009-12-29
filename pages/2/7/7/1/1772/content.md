#Contents#
* automatic table of contents goes here
{:toc}

## Idea

When regarding a [[sheaf]] as a [[space and quantity|generalized space]] defined by how it is probed by test spaces, a _concrete sheaf_ is a generalized space that has (at least) an _underlying [[set]] of points_ out of which it is built.

So a concrete sheaf models a [[space and quantity|generalized space]] that is given by a set of points and a choice of which morphisms of [[set]]s from concrete test spaces into it count as "structure preserving" (e.g. count as smooth, when the sheaf models a [[smooth space]]).

More in the intrinsic language of [[sheaf|sheaves]], a _concrete sheaf_ is a [[sheaf]] on a [[concrete site]] $C$ that, while perhaps not [[representable functor|representable]], is "quasi-representable" in that it is a [[subobject]] of a sheaf of the form

$$
  U \mapsto Hom_{Set}(|U|, S)
$$

where $S$ is a [[set]] and $|U|$ is the [[set]] $|U| := Hom_C({*}, U)$ of points underlying the object $U$ in the [[concrete site]] $C$.

## Remarks

* While the [[category of sheaves|category of all sheaves]] $Sh(C)$ on $C$ is a [[topos]] (a [[Grothendieck topos]]), a category of concrete sheaves $CSh(C)$ is a [[quasitopos]].

## References 

Categories of concrete sheaves, with special attention to sheaves on [[Diff]], i.e. to [[diffeological space]]s, are discussed in detail in 

* [[John Baez]], [[Alex Hoffnung]], _Convenient Categories of Smooth Spaces_ ([arXiv](http://arxiv.org/abs/0807.1704))