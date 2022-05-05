
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

A [[monoid]] $(A, \cdot)$ is called _left cancellative_ if 

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
      a \cdot z = a \cdot z
   \right)
     \Rightarrow
   \left(
     a = b
   \right)
  \right)
$$ 

It is called _cancellative_ if it is both _left cancellative_ and _right cancellative_. 

## Related concepts

* [[Grothendieck group]]
* ([[left cancellative category|left]], [[right cancellative category]]) [[cancellative category]]
* [[integral monoid]]
* [[GCD ring]]

[[!include oidification - table]]

## References

See also

* Wikipedia, _[Cancellative semigroup](https://en.wikipedia.org/wiki/Cancellative_semigroup)_

[[!redirects cancellative monoids]]

[[!redirects cancellative semi-group]]
[[!redirects cancellative semi-groups]]
