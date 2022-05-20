# Equivalence classes
* table of contents
{: toc}

## Idea

An equivalence class is an [[element]] of a [[quotient set]].


## Definitions

There are a variety of ways to make this precise.


### Axiomatic

Let $S$ be a [[set]], and let ${\sim}$ be an [[equivalence relation]] on $S$.  Then there exists a set $S/{\sim}$, the __quotient set__ of $S$ modulo $\sim$.  Given any element $x$ of $S$, there is an element $[x]_{\sim}$ of $S/{\sim}$, the __equivalence class__ of $x$ modulo ${\sim}$.  Every element of $S/{\sim}$ is of this form.  Furthermore, $[x]_{\sim}$ and $[y]_{\sim}$ are equal in $S/{\sim}$ if and only if $x \sim y$ in $S$.

The [[axiom of quotients]] is an axiom of [[set theory]] which states that the paragraph above is true.  It corresponds to the clause in the definition of a [[pretopos]] (or in [[Giraud's axioms]] for a [[Grothendieck topos]]) that every [[congruence]] has a [[coequaliser]].  In most formulations of set theory, this axiom is not needed; instead, it is a theorem when equivalence classes are defined in one of the ways below.


### As subsets

Again, let $S$ be a set, and let ${\sim}$ be an equivalence relation on $S$.  Let $x$ be an element of $S$.  Then the __equivalence class__ of $x$ modulo ${\sim}$ is the [[subset]] of $S$ consisting of those elements of $S$ that are equivalent to $x$:
$$ [x]_{\sim} \coloneqq \{ y\colon S \;|\; x \sim y \} .$$
Then the __quotient set__ $S/{\sim}$ is the collection of these equivalence classes.

We may construct this collection using the [[power set]] of $S$; therefore, this may be done in any [[elementary topos]] as well as in such diverse set theories as [[ZFC]], [[SEAR]], and [[ETCS]].  This definition of equivalence class is quite natural in [[material set theory]], since it immediately produces a set (assuming that subsets are sets).

Any element $x$ of $S$ is a __representative__ of its equivalence class $[x]$.  Every equivalence class has at least one representative, and its representatives are all equivalent.  The set of representatives *is* the equivalence class in the material set-theoretic sense.

One usually defines properties of equivalence classes and functions on quotient sets by defining them for an arbitrary representative, then proving that the result is independent of the representative chosen.  This does *not* require the [[axiom of choice]].


### Redefined equality

In some [[foundations of mathematics]], sets are not fundamental, but are defined as more basic [[presets]] (sometimes called [[types]] or, confusingly, sets).  By definition, a set (sometimes called a [[setoid]]) is a preset equipped with an equivalence (pre)relation.

Once more, let $S$ be a set, and let ${\sim}$ be an equivalence relation on $S$.  Then the quotient set $S/{\sim}$ is the the underlying preset of $S$ equipped with $\sim$ (in place of the original equality on $S$), and the equivalence class $[x]_{\sim}$ is simply $x$.


### As objects of a groupoid

One can also consider sets as [[groupoids]] (or $\infty$-[[infinity-groupoid|groupoids]]) with the property of being [[discrete groupoid|discrete]].

So again, let $S$ be a set, and let ${\sim}$ be an equivalence relation on $S$.  Then the quotient set $S/{\sim}$ is the (higher) groupoid whose objects are the same as those of $S$ and with a single morphism from $x$ to $y$ iff $x \sim y$ (and none otherwise); $[x]_{\sim}$ is simply $x$ again.

## Examples

* [[isomorphism class]]

* [[homotopy class]]




[[!redirects equivalence class]]
[[!redirects equivalence classes]]
