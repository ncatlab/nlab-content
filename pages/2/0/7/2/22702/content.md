+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Just as a [[groupoid]] is the [[oidification]] of a [[group]] and a [[ringoid]] is the oidification of a [[ring]], a [[quasigroupoid]] should be the oidification of a [[quasigroup]]. 

## Definition

A __quasigroupoid__ is a [[magmoid]] $Q$ such that for every [[span]] 

$$
  \array{
     && s
      \\
      & {}^{f}\swarrow
      && \searrow^{g}
     \\
     x
     &&&&
     y
  }
$$

in $Q$, there exists morphisms $i:x\to y$ and $j:y \to x$ such that $i \circ f = g$ and $j \circ g = f$, and for every [[cospan]] 

$$
  \array{
     && a &&&& b
      \\
      & 
      && {}_{f}\searrow
       &
       & \swarrow_g
      && 
     \\     
     &&&&
     c
     &&&&
  }
$$

in $Q$, there exists morphisms $d:a\to b$ and $e:b \to a$ such that $g \circ d = f$ and $f \circ e = g$. 

## Examples

* Every [[groupoid]] is a quasigroupoid. 

* Every [[loopoid]] and [[associative quasigroupoid]] is a quasigroupoid.

* A one-object quasigroupoid is a [[quasigroup]]. 

## Related concepts

* [[oidification]]

  * [[magmoid]], [[magma]]

  * [[unital magmoid]], [[unital magma]]

  * __quasigroupoid__, [[quasigroup]]

  * [[loopoid]], [[loop]]

  * [[semicategory]], [[semigroup]]

  * [[category]], [[monoid]]

  * [[associative quasigroupoid]], [[associative quasigroup]]

  * [[groupoid]], [[group]]