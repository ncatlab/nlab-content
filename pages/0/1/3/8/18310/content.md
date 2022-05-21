
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### In set theory

A [[monoid]] $(A, \cdot, 1)$ is called _left cancellative_ if 

$$
  \underset{a,b,z \in A}{\forall}
  \left(
    \left(
      z \cdot a = z \cdot b
   \right)
     \Rightarrow
   \left(
     a = b
   \right)
  \right)
$$ 

and called _right cancellative_ if 

$$
  \underset{a,b,z \in A}{\forall}
  \left(
    \left(
      a \cdot z = b \cdot z
   \right)
     \Rightarrow
   \left(
     a = b
   \right)
  \right)
$$ 

It is called _cancellative_ if it is both _left cancellative_ and _right cancellative_. 

### In infinity-groupoid theory

A [[monoid]] ([[n-truncated|$0$-truncated]] [[An-space|$A_3$-space]]) $(A, \cdot, 1)$ is called _left cancellative_ if for all objects $a \in A$ and $b \in A$ the [[homotopy fiber]] of the functor $L:A \to A$, defined as $L_a(z) \coloneqq a \cdot z$, at $b$ is $(-1)$-truncated, and is called _right cancellative_ if for all elements $a \in A$ and $b \in B$ the [[homotopy fiber]] of the functor $R:A \to A$, defined as $R_a(z) \coloneqq z \cdot a$ at $b$ is $(-1)$-truncated. It is called _cancellative_ if it is both _left cancellative_ and _right cancellative_. 

## Related concepts

* [[Grothendieck group]]
* [[cancellative category]]
* [[integral monoid]]
* [[GCD ring]]
* [[multiplicative submonoid of cancellative elements]]
* [[cancellative binary function]]

[[!include oidification - table]]

## References

See also

* Wikipedia, _[Cancellative semigroup](https://en.wikipedia.org/wiki/Cancellative_semigroup)_

[[!redirects cancellative monoids]]

[[!redirects cancellative semi-group]]
[[!redirects cancellative semi-groups]]

[[!redirects left cancellative]]
[[!redirects left-cancellative]]

[[!redirects right cancellative]]
[[!redirects right-cancellative]]