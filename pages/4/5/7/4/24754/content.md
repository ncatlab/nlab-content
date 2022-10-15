+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[dependent type theory]], propositional truncation is an operation which takes a [[type]] and turns it into a [[subsingleton]], which are commonly called [[h-propositions]] in dependent type theory. By the [[relation between type theory and category theory]], it should be possible to do the same process and turn an [[object]] of a [[category]] into a [[subterminal object]]. These are the **propositional truncation objects** in category theory. 

## Definition

The propositional truncation object $[X]$ of an object $X$ in a [[cartesian monoidal category]] $C$ is the [[coequalizer]] of the [[product]] projection morphisms $\pi_1:X \times X \to X$ and $\pi_2:X \times X \to X$

$$\array{
    X \times X
    && 
      \stackrel{\overset{\pi_1}{\longrightarrow}}{\underset{\pi_2}{\longrightarrow}}
    &&
    X
    \\
    & \searrow && \swarrow_{\mathrlap{p}}
    \\
    && [X]
  }.$$


## See also

* [[subsingleton]]
* [[subterminal object]]
* [[complete loop graph]]
* [[product]]
* [[coequalizer]]
* [[propositional truncation]]