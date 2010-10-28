
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _inverter_ is a special kind of [[2-limit]] in a [[2-category]].

## Definition

The [[2-limit]] over a [[diagram]] of the form

$$
  \array{
     & \nearrow & \searrow \\
    x &&\Downarrow&& y \\
    & \searrow & \nearrow 
  }
$$

is called an **inverter**.

The **inverter** of a [[2-morphism]] $\alpha:f\to g:A\to B$ is a universal object $V$ with a morphism $v:V\to A$ such that $\alpha v$ is invertible.

## References

In 

* [[Peter Johnstone]], _[[Elephant]]_

inverters appear in B1.1.4. The inverter of a transformation between [[geometric morphism]]s of [[topos]]es is constructed in the proof of corollary 4.1.7 in section B4.1. Coinverters are discussed in section B4.5 there.

[[!redirects inverters]]