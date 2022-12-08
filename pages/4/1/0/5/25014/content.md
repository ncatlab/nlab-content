
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

\tableofcontents

## Idea

The *common* meaning of "an inequality" in [[mathematics]] is the statement that a given [[pair]] of expressions, $x, y$, with values in some [[linear order|linearly ordered]] [[set]] of [[numbers]] (such as [[natural number|natural]], [[rational numbers|rational]] or [[real numbers]]) are in ordered [[relation]] to each other, such as 

$$
  x \lt y
$$

or

$$
  x \gt y
  \mathrlap{\,.}
$$

This is in contrast to the statement of their *[[equality]]*

$$ 
  x = y
  \mathrlap{\,,}
$$

whence the terminology  --- but, of course, there are other ways in which a pair of expressions can be "in-equal".
Generally, inequality may  just be the statement that a pair of [[terms]] of any [[type]] are *not equal*, though in non-classical [[foundations of mathematics]] there may be slightly different notions of "inequality relation" in this general sense, see the disambiguation [below](#InequalityRelation).

## Inequality relations
 {#InequalityRelation}

In [[classical mathematics]], an *inequality relation* is simply the [[negation]] ($\not$) of [[equality]] ($=$). However, in [[constructive mathematics]], due to the lack of [[excluded middle]], there are multiple different notions of inequality. These include:

* [[denial inequality]]
* [[tight inequality]] and [[tight apartness relation]]

More generally, an *inequality relation* is a [[relation]] $\neq$ which satisfies

* $\neg(a \neq a)$
* $a \neq b$ implies $b \neq a$
* one of these two equivalent [[contrapositive]] statements:
  * $\neg(a = b)$ implies $\neg \neg (a \neq b)$
  * $\neg(a \neq b)$ implies $\neg \neg (a = b)$

Denial inequality is precisely an inequality relation in which the inequality relation is [[stable proposition|stable]]. Tight inequality is precisely an inequality relation which implies that equality is [[stable equality|stable]]. And tight apartness is a tight inequality which is also a [[comparison]]. 

There are also the more general relations which do not make reference to [[equality]] at all, which are sometimes called "inequality relations" in constructive mathematics:

* [[apartness relation]]
* [[irreflexive symmetric relation]]

## References

See also:

* Wikipedia, *<a href="https://en.m.wikipedia.org/wiki/Inequality_(mathematics)">Inequality (mathematics)</a>*

[[!redirects inequality]]
[[!redirects inequalities]]

[[!redirects tight inequality]]
[[!redirects tight inequalities]]

[[!redirects inequality relation]]
[[!redirects inequality relations]]

[[!redirects tight inequality relation]]
[[!redirects tight inequality relations]]