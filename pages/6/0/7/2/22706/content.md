+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
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

Just as a [[groupoid]] is the [[oidification]] of a [[group]] and a [[ringoid]] is the oidification of a [[ring]], an associative quasigroupoid should be the oidification of an [[associative quasigroup]]. 

## Definition

An __associative quasigroupoid__ is a [[magmoid]] $Q$ such that for every [[diagram]] 

$$
  a\underset{\quad f \quad}{\to}b\underset{\quad g \quad}{\to}c\underset{\quad h \quad}{\to}d
  \,,
$$

$$
  h \circ (g \circ f) = (h \circ g) \circ f
  \,,
$$

for every [[span]] 

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

* Every [[groupoid]] is an associative quasigroupoid. 

* A one-object associative quasigroupoid is an [[associative quasigroup]]. 

## Related concepts

[[!include oidification - table]]