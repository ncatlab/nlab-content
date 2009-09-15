<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


## Idea

A topos is a [[category]] that resembles the category of sets and functions enough that we can use it as a 'universe' to do ordinary mathematics in.  Ordinary mathematical reasoning (with some restrictions) suffices to prove results [[internalisation|internal]] to any topos.

A topos in this sense is sometimes called an __elementary topos__ or a __Lawvere--Tierney topos__ to distinguish it from the original but more specific [[Grothendieck topos]].

For a longer introduction, try:

* John Baez, [Topos Theory in a Nutshell](http://math.ucr.edu/home/baez/topos.html).


## Definition

A quick formal definition is that an **(elementary) topos** is a category which

1. has [[finitely complete category|finite limits]],
1. is [[cartesian closed category|cartesian closed]], and
1. has a [[subobject classifier]].

There are alternative ways to state the definition; for instance,

1. finite limits and
2. [[power objects]].

In a way, however, these concise definitions can be misleading, because a topos has a great deal of other structure, which plays a very important role but just happens to follow automatically from these basic axioms.  Most importantly, a topos is:

*  [[locally cartesian closed category|locally cartesian closed]],
*  [[finitely cocomplete category|finitely cocomplete]],
*  a [[Heyting category]],
*  a [[pretopos]].

The last two imply that it has an [[internal logic]] that resembles ordinary mathematical reasoning, and the presence of exponentials and power objects means that this logic is [[higher order logic|higher order]].


## Reasoning in a topos

Any result in ordinary mathematics whose proof is [[finite mathematics|finitist]] and [[constructive mathematics|constructive]] automatically holds in any topos.  If you remove the restriction that the proof be finitist, then the result holds in any topos with a [[natural numbers object]]; if you remove the restrictions that the proof be constructive, then the result holds in any [[boolean topos]].  On the other hand, if you add the restriction that the proof be predicative in the weaker sense used by constructivists, then the result may fail in some toposes but holds in any $\Pi$-[[Pi-pretopos|pretopos]]; if you add the restriction that the proof by predicative in a stronger sense, then the result holds in any [[Heyting pretopos]].

Therefore, one can prove results in toposes and similar categories by reasoning, not about the [[objects]] and [[morphisms]] in the topos themselves, but instead about [[sets]] and [[functions]] in the normal language of structural [[set theory]], which is more familiar to most mathematicians.  One merely has to be careful about what axioms one uses to get results of sufficient generality.

For more on this idea, see [[internal logic]].


[[!redirects topoi]]
[[!redirects toposes]]
[[!redirects Lawvere-Tierney topos]]
[[!redirects Lawvere--Tierney topos]]
[[!redirects Lawvere–Tierney topos]]
[[!redirects elementary topos]]
[[!redirects Lawvere-Tierney topoi]]
[[!redirects Lawvere--Tierney topoi]]
[[!redirects Lawvere–Tierney topoi]]
[[!redirects elementary topoi]]
[[!redirects Lawvere-Tierney toposes]]
[[!redirects Lawvere--Tierney toposes]]
[[!redirects Lawvere–Tierney toposes]]
[[!redirects elementary toposes]]