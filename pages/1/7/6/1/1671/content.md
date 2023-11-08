
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

### In set theory

More explicitly, let $X$ be any [[set]] and let $p\colon X \to \mathbf{N}$ be a [[surjection]].  Then the axiom of countable choice states that $p$ has a [[section]].  If you phrase the axiom of choice in terms of [[entire relations]], then countable choice states that any entire relation from $\mathbf{N}$ to any other set contains (in the [[2-poset]] [[Rel]]) a [[functional relation|functional]] entire relation.

### In dependent type theory

In [[dependent type theory]], **countable choice** says that the [[dependent product type|dependent product]] of a family of inhabited sets indexed by the [[natural numbers]] is itself inhabited:

$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma \vdash \mathrm{AC}_\mathbb{N}^A:\left(\prod_{n:\mathbb{N}} \mathrm{isSet}(A(n))\right) \to \left(\prod_{n:\mathbb{N}} [A(n)]\right) \to \left[\prod_{n:\mathbb{N}} A(n)\right]}$$

Alternatively, the axiom of countable choice states that given a family of sets $A(n)$ indexed by natural numbers $n$ and a family of propositions $P(n, x)$ indexed by natural numbers $n$ and element $x:A(n)$, if for all natural numbers $n$ there merely exists an element $x:A(n)$ such that $P(n, x)$, then there merely exists a dependent function $g:\prod_{n:\mathbb{N}} A(n)$ such that for all natural numbers $n$, $P(n, g(n))$:

$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type} \quad \Gamma, n:\mathbb{N}, x:A(n) \vdash P(n, x) \; \mathrm{type}}{\Gamma \vdash \mathrm{AC}_\mathbb{N}^{A, P}:\left(\prod_{n:\mathbb{N}} \mathrm{isSet}(A(n)) \times \prod_{x:A(n)} \mathrm{isProp}(P(n, x))\right) \to \left(\prod_{n:\mathbb{N}} \exists x:A(n).P(n, x)\right) \to \exists g:\prod_{n:\mathbb{N}} A(n).\prod_{n:\mathbb{N}} P(n, g(n))}$$

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

One easy example is the category $Sh([0,1])$, the sheaves on the unit interval, since in that topos the [[real numbers object#classical_dedekind_real_numbers|Dedekind real numbers]] and the [[real numbers object#cauchy_real_numbers|Cauchy real numbers]] are not isomorphic, and this is a consequence of the internal countable choice.

Discussion [here](https://mathoverflow.net/questions/79807/example-of-a-topos-that-violates-countable-choice). 

### In higher category theory

To formulate a version of the axiom of countable choice in a higher category, one has to make an appropriate choice of the meaning of "epimorphism". In most cases, it is best to choose [[effective epimorphisms|effective epimorphism in an (infinity,1)-category]] or a related notion such as [[eso morphisms]].

There are multiple version of the axiom of countable choice, depending on what [[truncated object|truncation]] requirements, if any, are applied to the domain. 

* An $(\infty,1)$-category satisfies the **axiom of countable $n$-choice**, or $CC_n$, if every $n$-[[truncated morphism]] into the [[natural numbers object]] has a section. We write $CC_\infty$ for the **axiom of countable infinity-choice**: the statement that *every* morphism with codomain the [[natural numbers object]] has a section.

These are stronger axioms as $n$ increases. 

There are also "internal" versions of these axioms.

* In [[homotopy type theory]] (the internal logic of an $(\infty,1)$-topos), the internal version of $CC_n$ is "every surjection onto the natural numbers type with $n$-type fibers has a section", or equivalently
  $$\prod_{(Y:\mathbb{N}\to n Type)} \Big( \prod_{(x:\mathbb{N})} \Vert Y(x)\Vert \to \Big\Vert \prod_{(x:\mathbb{N})} Y(x) \Big\Vert \Big) $$

* More generally, we can replace the $(-1)$-truncation by the $k$-truncation to obtain a family of axioms $CC_{k,n}$.

* We can also replace the $(-1)$-truncation by the assertion of $k$-connectedness, obtaining the **axiom of countable $k$-connected choice**.

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

[[!redirects countable n-choice]]
[[!redirects countable axiom of n-choice]]
[[!redirects axiom of countable n-choice]]

[[!redirects countable infinity-choice]]
[[!redirects countable axiom of infinity-choice]]
[[!redirects axiom of countable infinity-choice]]

[[!redirects AC00]]

[[!redirects weak countable choice]]
[[!redirects WCC]]
