
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

The *common* meaning of "an inequality" in [[mathematics]] is the statement that a given [[pair]] of expressions, $x, y$, with values in some [[strictly totally ordered]] [[set]] of [[numbers]] (such as [[natural number|natural]], [[rational numbers|rational]] or [[real numbers]]) are in ordered [[relation]] to each other, such as 

$$
  x \lt y
$$

or

$$
  x \gt y
  \mathrlap{\,.}
$$

This is in contrast to the statement of their *[[equality]]*, expressed by an *[[equation]]*

$$ 
  x = y
  \mathrlap{\,,}
$$

whence the terminology. But, of course, there are other ways in which a pair of expressions can be "in-equal"; see at *[Inequality relations](#InequalityRelations)* below.

On the other hand, in practice one also calls the non-strict [[total order]]

$$
  x \leq y
$$

an "inequality". Many famous inequalities are of this form (starting with the [[triangle inequality]]), often accompanied with statement of conditions when exactly the actual [[equality]] holds.

## Examples
 {#Examples}

* [[triangle inequality]]

* [[Minkowski's inequality]]

* [[Cauchy-Schwarz inequality]]

* [[Young's inequality]]

* [[Hölder's inequality]]

* [[Cramer-Rao inequality]]

* [[Grothendieck's inequality]]

* [[Bell's inequality]]

## Inequality relations
 {#InequalityRelations}

More generally, inequality may just be the statement that a pair of [[terms]] of any [[type]] are *[[negation|not]] [[equality|equal]]*.  (To distinguish this from order relations as discussed above, one may also call it *disequality*.)

In  the [[foundations of mathematics]], sometimes one talks about a particular [[relation]] called the *inequality relation*. 

In [[classical mathematics]], the *inequality relation* is defined as the [[negation]] ($\not$) of [[equality]] ($=$). However, in [[constructive mathematics]], due to the lack of [[excluded middle]], there are multiple different notions of inequality relation. The two most commonly used notions are the [[denial inequality relation]] and the [[tight apartness relation]]. Other relations which have been called "inequality relation" in the constructive mathematics literature are listed in [[irreflexive symmetric relation#ConstructiveMathematics]]. 

More generally, any [[irreflexive relation]] $R(x, y)$ can be considered an "inequality" because by definition of irreflexive, $R(x, y)$ and equality $x = y$ are [[mutually exclusive]] for all $x$ and $y$, and the relation $R(x, y)$ gives rise to an [[irreflexive symmetric relation]] $x \nsim y \coloneqq R(x, y) \vee R(y, x)$. The equivalent for irreflexive relations of a tight irreflexive symmetric relation is a connected irreflexive relation. 

## See also

* [[equality]], [[equation]]

* [[denial inequality]]

## References

See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Inequality_(mathematics)">Inequality (mathematics)</a>*

[[!redirects inequality]]
[[!redirects inequalities]]

[[!redirects tight inequality]]
[[!redirects tight inequalities]]

[[!redirects connected inequality]]
[[!redirects connected inequalities]]

[[!redirects inequality relation]]
[[!redirects inequality relations]]

[[!redirects tight inequality relation]]
[[!redirects tight inequality relations]]

[[!redirects connected inequality relation]]
[[!redirects connected inequality relations]]

[[!redirects not equal]]
[[!redirects not equal to]]