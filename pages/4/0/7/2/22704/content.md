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

Just as a [[groupoid]] is the [[oidification]] of a [[group]] and a [[ringoid]] is the oidification of a [[ring]], a [[loopoid]] should be the oidification of a [[loop]]. 

## Definition

A __loopoid__ $Q$ is a [[magmoid]] where every object $a \in Ob(Q)$ has an [[identity morphism]] $id_a: a \to a$, such that for any morphism $f:a \to b$, $f \circ id_a = f$, and for any morphism $g:c \to a$, $id_a \circ g = g$, where every [[span]] 

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

in $Q$ has morphisms $i:x\to y$ and $j:y \to x$ such that $i \circ f = g$ and $j \circ g = f$, and where every [[cospan]] 

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

in $Q$ has morphisms $d:a\to b$ and $e:b \to a$ such that $g \circ d = f$ and $f \circ e = g$. 

## Examples

* A [[groupoid]] is a [[loopoid]]. 

* A loopoid with only one object is called a [[loop]]. 

## Related concepts

* [[loop]]

* [[oidification]]

[[!redirects loopoids]]