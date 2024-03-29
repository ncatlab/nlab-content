
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


# The Extreme Value Theorem
* table of contents
{: toc}

## Idea

The classical _extreme value theorem_ states that a [[continuous function]] on the [[bounded subset|bounded]] [[closed interval]] $[0,1]$ with values in the [[real numbers]] does attain its [[maximum]] and its [[minimum]] (and hence in particular is a [[bounded function]]). This is a special case in [[analysis]] of the more general statement in [[topology]] that [[continuous images of compact spaces are compact]].

Although the Extreme Value Theorem (EVT) is often stated as a theorem about [[continuous maps]], it\'s really about [[semicontinuous maps]].

Recall that the [[lower real numbers]] are more general than the [[real numbers]] in just the way needed to guarantee that any [[inhabited subset|inhabited]] set of lower reals has a [[supremum]] (by including $\infty$, and in [[constructive mathematics]] by additionally relaxing the requirements of [[located real number|locatedness]]).  Consequently, the [[range]] of any lower-real-valued function with an [[inhabited set|inhabited]] [[domain]] must have a supremum.

The Extreme Value Theorem states that such a range must also have an [[infimum]] when certain conditions are met.  Specifically, we move to the realm of [[topology]], where the natural lower-real-valued functions are the [[semicontinuous map|lower semicontinuous]] ones.  So long as the [[domain]] of a lower semicontinuous map is [[compact space|compact]] (and inhabited), says the EVT, the range has an infimum, and furthermore this infimum is attained, becoming a [[minimum]].


## Statements

We first discuss the statement

* [for continuous functions](#ForContinuousFunctions)

and then the general case

* [for semicontinuous function](#ForSemicontinuousFunctions).

### For continuous functions
 {#ForContinuousFunctions}

+-- {: .num_prop}
###### Proposition
**(extreme value theorem)**

Let $C$ be a [[compact topological space]], and let 

$$
  f \;\colon\; C \longrightarrow \mathbb{R}
$$

be a [[continuous function]] to the [[real numbers]] equipped with their [[Euclidean space|Euclidean]] [[metric topology]]. 

Then $f$ attains its [[maximum]] and its [[minimum]], i.e. there exist $x_{min}, x_{max} \in C$ such that for all $x \in C$ it is true that

$$
  f(x_{min})
    \leq
  f(x)
   \leq 
  f(x_{max})
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

Since [[continuous images of compact spaces are compact]] the image $f([a,b]) \subset \mathbb{R}$ is a [[compact topological space|compact]] [[subspace]]. 

Suppose this image did not contain its maximum. Then $\{(-\infty,x)\}_{x \in f([a,b])}$ were an [[open cover]] of the image, and hence, by its compactness, there would be a finite subcover, hence a finite set $(x_1 \lt x_2 \lt \cdots \lt x_n)$ of points $x_i \in f([a,b])$, such that the union of the $(-\infty,x_i)$ and hence the single set $(-\infty, x_n)$ alone would cover the image. This were in contradiction to the assumption that $x_n \in f([a,b])$ and hence we have a [[proof by contradiction]].

Similarly for the minimum.

=--


+-- {: .num_example }
###### Example
**(classical extreme value theorem)**

Let 

$$
  f \;\colon\; [a,b] \longrightarrow \mathbb{R}
$$

be a [[continuous function]] from a [[bounded set|bounded]] [[closed interval]] ($a \lt b \in \mathbb{R}$)
regarded as a [[topological subspace]] of [[real numbers]] to the [[real numbers]], with the
latter regarded with their [[Euclidean space|Euclidean]] [[metric topology]].

Then $f$ attains its [[minimum]] $f(x_{min})$ and [[maximum]] $f(x_{max})$ and the [[image]] of $f$ is the [[closed interval]]


$$
  f([a,b]) = [f(x_{min}), f(x_{max})]
  \,.
$$

=--


+-- {: .proof}
###### Proof

Since [[continuous images of compact spaces are compact]] the image $f([a,b]) \subset \mathbb{R}$ is a [[compact topological space|compact]] [[subspace]]. 

By the [[Heine-Borel theorem]] the image, being compact, is a [[bounded set|bounded]] [[closed subset]], hence a [[finite set|finite]] union of bounded [[closed intervals]] and [[singleton]] subsets. By continuity of $f$, this union cannot be disjoint, for if $f([a,b])$ were a disjoint union $C_1 \sqcup C_2$ of closed inhabited subsets, then also the pre-image were a disjoint union of closed inhabited subsets $f^{-1}(C_1) \sqcup f^{-1}(C_2)$, contradicting the fact that the pre-image of the image is the connected interval $[a,b]$.

=--


### For semicontinuous functions
 {#ForSemicontinuousFunctions}

If $I$ is a [[compact space]], and if $f$ is an [[upper semicontinuous function]] from $I$ to the [[upper real numbers]] $[{-\infty,\infty}[$, then the [[range]] of $f$ is not only bounded above and not only has a finite [[supremum]], but it actually has a [[maximum]] value (unless $I$ is [[empty space|empty]]).

Similarly, and consequently (by replacing $f$ with $-f$), if $f$ is [[lower semicontinuous function|lower semicontinuous]] to the [[lower real numbers]] $]{-\infty,\infty}]$, then $\ran f$ is bounded below by a finite [[infimum]] which is its [[minimum]] value.  Consequently, if $f$ is [[continuous function|continuous]] to the [[real numbers]] $]{-\infty,\infty}[$, then $\ran f$ is [[bounded subset|bounded]] and has both a maximum and a minimum.)

In [[constructive mathematics]], this statement is correct in [[locale theory]] (in a sense that we should explain here!), but if we are speaking of pointwise functions defined on a real interval, then it fails in general.  However, we have approximate versions; in particular, it is constructive that $\ran f$ is bounded and has (if real-valued and pointwise-continuous) a real infimum and supremum.  However, the EVT interacts subtly with the [[fan theorem]]; the fan theorem is equivalent to the statement that whenever a pointwise-continuous real-valued function $f$ on $[0,1]$ satisfies $m \lt f \lt M$, then $m \lt \inf f$ and $\sup f \lt M$, which (once the existence of $\inf f$ and $\sup f$ is granted) may be viewed as a contrapositive form of the EVT.  (In fact, the fan theorem is separately equivalent to the statement that every continuous function on $[0,1]$ is [[uniformly continuous map|uniformly continuous]] and to the statement that every uniformly continuous function on $[0,1]$ has this contrapositive property.)  But without the fan theorem, even this contrapositive form cannot be proved (in marked contrast to similar theorems such as the [[intermediate value theorem]] and the [[mean value theorem]]), and in fact it is false in [[Russian constructivism]] (give a counterexample?).  (Does the full semicontinuous version follow from the fan theorem?)

## Related concepts

* [[continuous images of compact spaces are compact]]

## References

* Wikipedia, _[Extreme value theorem](https://en.wikipedia.org/wiki/Extreme_value_theorem)_

* Karin U. Katz, Mikhail G. Katz, Taras Kudryk, _Toward a clarity of the extreme value theorem_ ([arXiv:1404.5658](http://arxiv.org/abs/1404.5658))


[[!redirects extreme value theorem]]
[[!redirects extreme value theorems]]
[[!redirects Extreme Value Theorem]]
[[!redirects EVT]]
