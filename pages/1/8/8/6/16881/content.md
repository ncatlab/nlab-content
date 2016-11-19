
# The Extreme Value Theorem
* table of contents
{: toc}

## Idea

Although the Extreme Value Theorem (EVT) is often stated as a theorem about [[continuous maps]], it\'s really about [[semicontinuous maps]].

Recall that the [[lower real numbers]] are more general than the [[real numbers]] in just the way needed to guarantee that any [[inhabited subset|inhabited]] set of lower reals has a [[supremum]] (by including $\infty$, and in [[constructive mathematics]] by additionally relaxing the requirements of [[located real number|locatedness]]).  Consequently, the [[range]] of any lower-real-valued function with an [[inhabited set|inhabited]] [[domain]] must have a supremum.

The Extreme Value Theorem states that such a range must also have an [[infimum]] when certain conditions are met.  Specifically, we move to the realm of [[topology]], where the natural lower-real-valued functions are the [[semicontinuous map|lower semicontinuous]] ones.  So long as the [[domain]] of a lower semicontinuous map is [[compact space|compact]] (and inhabited), says the EVT, the range has an infimum, and furthermore this infimum is attained, becoming a [[minimum]].


## Statements

If $I$ is a [[compact space]] (such as a closed bounded [[interval]] in the [[real line]] and especially the [[unit interval]] $[{0,1}]$), and if $f$ is an [[upper semicontinuous function]] from $I$ to the [[upper real numbers]] $[{-\infty,\infty}[$, then the [[range]] of $f$ is not only bounded above and not only has a finite [[supremum]], but it actually has a [[maximum]] value (unless $I$ is [[empty space|empty]]).

Similarly, and consequently (by replacing $f$ with $-f$), if $f$ is [[lower semicontinuous function|lower semicontinuous]] to the [[lower real numbers]] $]{-\infty,\infty}]$, then $\ran f$ is bounded below by a finite [[infimum]] which is its [[minimum]] value.  Consequently, if $f$ is [[continuous function|continuous]] to the [[real numbers]] $]{-\infty,\infty}[$, then $\ran f$ is [[bounded subset|bounded]] and has both a maximum and a minimum.)

In [[constructive mathematics]], this statement is correct in [[locale theory]] (in a sense that we should explain here!), but if we are speaking of pointwise functions defined on a real interval, then it fails in general.  However, we have approximate versions; in particular, it is constructive that $\ran f$ is bounded and has (if real-valued and pointwise-continuous) a real infimum and supremum.  However, the EVT interacts subtly with the [[fan theorem]]; the fan theorem is equivalent to the statement that whenever a pointwise-continuous real-valued function $f$ on $[0,1]$ satisfies $m \lt f \lt M$, then $m \lt \inf f$ and $\sup f \lt M$, which (once the existence of $\inf f$ and $\sup f$ is granted) may be viewed as a contrapositive form of the EVT.  (In fact, the fan theorem is separately equivalent to the statement that every continuous function on $[0,1]$ is [[uniformly continuous map|uniformly continuous]] and to the statement that every uniformly continuous function on $[0,1]$ has this contrapositive property.)  But without the fan theorem, even this contrapositive form cannot be proved (in marked contrast to similar theorems such as the [[intermediate value theorem]] and the [[mean value theorem]]), and in fact it is false in [[Russian constructivism]] (give a counterexample?).  (Does the full semicontinuous version follow from the fan theorem?)


## References

* Karin U. Katz, Mikhail G. Katz, Taras Kudryk. Toward a clarity of the extreme value theorem. [arXiv:1404.5658](http://arxiv.org/abs/1404.5658).


[[!redirects extreme value theorem]]
[[!redirects extreme value theorems]]
[[!redirects Extreme Value Theorem]]
[[!redirects EVT]]
