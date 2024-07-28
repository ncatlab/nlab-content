
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

In [[set theory]], the [[support of a set]] turns the set into a [[subsingleton]]. In [[dependent type theory]], [[propositional truncation]] or the [[bracket type]] is an operation which takes a [[type]] and turns it into a [[h-propositions]], which are the type theoretic equivalent of subsingletons. By the [[relation between type theory and category theory]] and the relation between set theory and [[topos theory]], it should be possible to do the same process and turn an [[object]] of a [[category]] into a [[subterminal object]]. These are the **support objects**, **bracket objects**, or **propositional truncation objects** in category theory. 

## Definition

### In category theory

The support object $[X]$ of an object $X$ in a [[regular category]] $C$ is the [[image]] of the unique morphism into the [[terminal object]] $X \to 1$. 

$$X \to [X] \hookrightarrow 1$$

As a result, that all support objects exist is equivalent to the condition that every morphism into the terminal object has an [[image factorization]]. 

### In allegory theory

The support object $[X]$ of an object $X$ in a [[unitary tabular allegory]] $C$ is the [[tabulation]] of the unique map from $X$ into the allegorical unit $1$. 

## Properties

In any [[well-pointed pretopos]] $\mathcal{E}$, the support is the [[coequalizer]] of the [[product]] projection morphisms $\pi_1:X \times X \to X$ and $\pi_2:X \times X \to X$

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

* [[support]]
* [[subsingleton]]
* [[subterminal object]]
* [[complete loop graph]]
* [[product]]
* [[coequalizer]]
* [[propositional truncation]]
* [[inhabited object]]
* [[choice operator]] 

[[!include types and logic - table]]

[[!redirects support object]]
[[!redirects support objects]]

[[!redirects bracket object]]
[[!redirects bracket objects]]

[[!redirects propositional truncation object]]
[[!redirects propositional truncation objects]]