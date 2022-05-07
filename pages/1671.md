
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Countable choice
* table of contents
{: toc}

## Idea

The axiom of __countable choice__ ($CC$), also called $AC_\omega$ or $AC_N$, is a weak form of the [[axiom of choice]]; it says that the set of [[natural number]]s is a [[projective object]] in [[Set]].  (Recall that the full axiom of choice states that *every* set is projective.)

In [[classical mathematics]], countable choice is usually accepted because the full axiom of choice is accepted.  In [[constructive mathematics]] the situation is more subtle.  For varying reasons, some schools of constructive mathematics accept countable choice (though they reject the full axiom of choice).  On the other hand, countable choice is not valid in the [[internal logic]] of a general topos, so if one desires this level of generality then it should not be assumed.  There are also philosophical constructivist arguments against it.  [[Fred Richman]] [(RichmanFTA)](#RichmanFTA) has said that

> Countable choice is a blind spot for constructive mathematicians in much the same way as excluded middle is for classical mathematicians.

All the reasoning in this page is [[constructive mathematics|constructive]].

## Definition

More explicitly, let $X$ be any [[set]] and let $p\colon X \to \mathbf{N}$ be a [[surjection]].  Then the axiom of countable choice states that $p$ has a [[section]].  If you phrase the axiom of choice in terms of [[entire relations]], then countable choice states that any entire relation from $\mathbf{N}$ to any other set contains (in the [[2-poset]] [[Rel]]) a [[functional relation|functional]] entire relation.

## Consequences

Here we collect some consequences of the countable axiom of choice.

* The [[Cauchy real numbers]] and [[Dedekind real numbers]] coincide (the [[law of excluded middle]] also separately implies this).

* The [[Rosolini dominance]] is a [[dominance]] (the [[law of excluded middle]] also separately implies this).

* [[countable unions of countable sets are countable]]

## Variations

### $COSHEP$ & $DC$

Unlike the full axiom of choice, countable choice is often considered to be a [[constructive mathematics|constructively]] acceptable principle.  In particular, it does not imply the principle of [[excluded middle]].  It is a consequence of [[COSHEP]].  A stronger version of countable choice, also a consequence of $COSHEP$, is the axiom of [[dependent choice]] ($DC$).  In general, $DC$ is enough to justify results in [[analysis]] involving [[sequences]].


### $AC_{00}$

Sometimes in foundations it is useful to consider a weaker version of countable choice, called __$AC_{00}$__.  This states that any entire relation from $\mathbf{N}$ to itself contains a functional entire relation.  In terms of surjections, this states that any surjection $p\colon X \to \mathbf{N}$ has a section if $X$ is a [[subset]] of $\mathbf{N} \times \mathbf{N}$ and $p$ is the [[restriction]] to $X$ of a product projection.  $AC_{00}$ is enough to prove that every [[Dedekind real number]] is a [[Cauchy real number]] (the converse is always true).


### Weak countable choice {#WCC}

The axiom of __weak countable choice__ ($WCC$) states that a surjection $p\colon X \to \mathbf{N}$ has a section if, whenever $m \neq n$, at least one of the [[preimages]] $p^*(m)$ and $p^*(n)$ is a [[singleton]].  $WCC$ follows (for different reasons) from either $CC$ or [[excluded middle]].  On the other hand, $WCC$ is enough to prove that the [[fundamental theorem of algebra]] in the sense that every non-constant complex polynomial has a root; see [Bridges et al (1998)](#BRS). 

### Very weak countable choice

An even weaker form of countable choice was proposed by [Martin Escardo](#EscardoCN); it states that any surjection of the form $A \sqcup (\mathbf{N}\times B) \to \mathbf{N}$ has a section, where $A\to \mathbf{N}$ is a [[decidable subset]] and $B$ is an arbitrary set with $\mathbf{N}\times B \to \mathbf{N}$ the projection.  This follows from WCC and also from the [[limited principle of omniscience]]; see the [constructivenews discussion](#EscardoCN).

### Topos violating the CAC
Discussion [here](https://mathoverflow.net/questions/79807/example-of-a-topos-that-violates-countable-choice). This example uses a [[Fraenkel-Mostowski model]].

## References

*  {#BRS}Douglas Bridges, Fred Richman, and Peter Schuster (1998). A weak countable choice principle. [PDF](http://math.fau.edu/richman/docs/wcc.pdf) [AMS PDF](http://www.ams.org/proc/2000-128-09/S0002-9939-00-05327-2/)

*  {#EscardoCN}Martin Escardo et. al., *Special case of countable choice*, message and discussion to the constructivenews list, [google groups](https://groups.google.com/d/msg/constructivenews/PeLsQWDFJNg/7piOmUHbAAAJ)

*  {#RichmanFTA} [[Fred Richman]], *The fundamental theorem of algebra: a constructive development without choice*.  [pdf](http://math.fau.edu/richman/docs/Fta.pdf)

See also 

* Wikipedia, _[Axiom of countable choice](https://en.wikipedia.org/wiki/Axiom_of_countable_choice)_

category: foundational axiom

[[!redirects countable choice]]
[[!redirects countable axiom of choice]]
[[!redirects axiom of countable choice]]

[[!redirects AC00]]

[[!redirects weak countable choice]]
[[!redirects WCC]]
