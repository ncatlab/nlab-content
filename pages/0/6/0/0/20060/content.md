> This page is about [[de Morgan algebras]] satisfying an extra condition.  For Kleene star algebras in relation to [[regular expressions]], see there.

# Kleene algebra

* table of contents
{: toc}

## Definition

A **Kleene algebra** is a [[de Morgan algebra]] $D$ satisfying $x \wedge \neg x \le y \vee \neg y$ for all $x,y\in D$. Since the order is definable in terms of the lattice operators, this can be stated as the equation

$$ x \wedge \neg x \wedge (y \vee \neg y) = x \wedge \neg x. $$

## Examples

* Any [[Boolean algebra]] is a Kleene algebra, with $\neg$ the logical negation.
* The unit interval $[0,1]$ is a Kleene algebra, with $\neg x = (1-x)$. 

## Related concepts

* Kleene algebras are used in one form of [[cubical type theory]]

[[!redirects Kleene algebras]]
