## Outline

In response to a [request](http://golem.ph.utexas.edu/category/2009/09/towards_a_computeraided_system.html#c027419), this page explains how to define a [[small category]] using [[SEAR]] as [[foundations]].  Note that, while SEAR speaks no [[evil]] in that one cannot compare arbitrary sets for equality, it has no provision for small types with no notion of equality.  Thus we will be formalising small [[strict category|strict categories]], and it will be possible to say evil things about them.

There are actually two ways to interpret this programme.  One is to accept every set in SEAR as 'small' and consider categories that are small in that sense.  So the category of *all* SEAR sets cannot be formalised this way, but any category whose set of objects and hom-sets are sets in SEAR can be formalised in this way.  Another way is to declare a [[family of sets]] within SEAR to be the family of 'small' sets; then only categories with a set of morphisms that belongs to this family can be formalised in this way.  (This way is even more [[evil]] in that one can even consider equality of categories, not only equality of objects within a given category.)  There is small category (in the first sense) of all small categories (in the second sense).

We call these two interpretations the 'large universe' and 'small universe' interpretations.


## Large universe version

A __category__ is a syntactic quintuple that consists of

*  a set $O$ (called the set of _objects_),
*  a set $M$ (called the set of _morphisms_),
*  a function $s: M \to O$ (the _source_ map),
*  a function $t: M \to O$ (the _target_ map),
*  and a partial function $c: M \times M \dashrightarrow M$ (the _composition map_)

satsifying these conditions:

*  For $f, g$ elements of $M$, $c(f,g)$ is defined if and ony if $s(f) = t(g)$.
*  In that case, $s(c(f,g)) = s(g)$ and $t(c(f,g)) = t(f)$.
*  For every element $x$ of $O$, there exists an element $i$ of $M$ such that
   *  $s(i) = x$ and $t(i) = x$,
   *  $c(i,f) = f$ for every element $f$ of $M$ such that $x = t(f)$, and
   *  $c(f,i) = f$ for every element $f$ of $M$ such that $s(f) = x$.
*  For $f, g, h$ elements of $M$ such that $s(f) = t(g)$ and $s(g) = t(h)$, we have $c(c(f,g),h) = c(f,c(g,h))$.

Note that a partial function from $p: X \dashrightarrow Y$ is formalised as a [[functional relation]], that is a relation $\phi: X \to Y$ such that $b = c$ whenever $\phi(a,b)$ and $\phi(a,c)$ both hold (for elements $a$ of $X$ and $b,c$ of $Y$).  We say that $p(x)$ is _defined_ if there is $y$ such that $\phi(x,y)$ holds; in that case, such $y$ is unique and we denote it $p(x)$.  This notation can be eliminated from the language using existential quantification, the same as when $p$ is a function.


## Small universe version

Take a relation $m \: U \looparrowright E$ as the _family of small sets_.  Then a __small category__ is an element of ... such that ....  Along with the set of small categories, we consider the relations ..., which are respectively the families of _sets of objects_, _sets of morphisms_, _source maps_, _target maps_, and _composition maps_.