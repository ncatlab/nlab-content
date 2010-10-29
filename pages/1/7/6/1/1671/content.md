
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--



# Countable choice
* table of contents
{: toc}

## Definitions

The axiom of __countable choice__ (CC), also called $AC_\omega$ or $AC_N$, is a weak form of the [[axiom of choice]]; it says that the set of [[natural number]]s is a [[projective object]] in [[Set]].  (Recall that the full axiom of choice states that *every* set is projective.)

More explicitly, let $X$ be any [[set]] and let $p\colon X \to \mathbf{N}$ be a [[surjection]].  Then the axiom of countable choice states that $p$ has a [[section]].  If you phrase the axiom of choice in terms of [[entire relations]], then countable choice states that any entire relation from $\mathbf{N}$ to any other set contains (in the [[2-poset]] [[Rel]]) a [[functional relation|functional]] entire relation.

Unlike the full axiom of choice, countable choice is often considered to be a [[constructive mathematics|constructively]] acceptable principle.  In particular, it does not imply the principle of [[excluded middle]].  It is a consequence of [[COSHEP]].  A stronger version of countable choice, also a consequence of COSHEP, is the axiom of [[dependent choice]].

Sometimes in foundations it is useful to consider a weaker version of countable choice, called __$AC_{00}$__.  This states that any entire relation from $\mathbf{N}$ to itself contains a functional entire relation.  In terms of surjections, this states that any surjection $p\colon X \to \mathbf{N}$ has a section if $X$ is a [[subset]] of $\mathbf{N} \times \mathbf{N}$ and $p$ is the [[restriction]] to $X$ of a product projection.

The axiom of __weak countable choice__ (WCC) states that a surjection $p\colon X \to \mathbf{N}$ has a section if, whenever $m \neq n$, at least one of the [[preimages]] $p^*(m)$ and $p^*(n)$ is a [[singleton]].  WCC follows (for different reasons) from either CC or [[excluded middle]].  On the other hand, WCC is enough to prove that every [[Dedekind real number]] is a [[Cauchy real number]] (the converse is always true); more generally, WCC is enough to justify sequential reasoning in [[analysis]].  See Briges et al (1998).


## References

*  Douglas Bridges, Fred Richman, and Peter Schuster (1998). A weak countable choice principle. Available from [Fred Richman's Documents](http://www.math.fau.edu/Richman/HTML/DOCS.HTM).


category: foundational axiom

[[!redirects countable choice]]
[[!redirects countable axiom of choice]]
[[!redirects axiom of countable choice]]

[[!redirects AC00]]

[[!redirects weak countable choice]]
