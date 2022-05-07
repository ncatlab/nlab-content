
> This entry is about a notion in [[formal logic]] ([[type theory]]). For the notion in [[homotopy theory]] see at *[[mapping telescope]]*.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[formal logic]] such as [[type theory]] a _telescope_ $\Delta$ is a [[finite]] [[list]] of [[terms in context]], whose elements/terms/inhabitants are [[substitutions]]. 

## Definition

In [[dependent type theory]], telescopes are defined inductively with the following rules

$$\frac{}{\epsilon\ \mathrm{tel}} \qquad \frac{\Delta\ \mathrm{tel} \quad \Delta \vdash A \mathrm{type}}{(\Delta,x:A)\ \mathrm{tel}}$$

The substitutions of telescopes are defined inductively with the following rules

$$\frac{}{():\epsilon} \qquad \frac{\delta:\Delta \quad \Delta \vdash A \mathrm{type} \quad a:A[\delta]}{(\delta,a):(\Delta,x:A)}$$

which are mutually defined with their action on terms and types. 

$$\frac{\Delta \vdash A\ \mathrm{type} \quad \delta:\Delta}{A[\delta]\ \mathrm{type}} \qquad \frac{\Delta \vdash a:A \quad \delta:\Delta}{a[\delta]:A[\delta]}$$

## See also

* [[term in context]]

* [[dependent type]]

* [[dependent identity type]]

## References

* Mike Shulman, Towards a Third-Generation HOTT Part 2 ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU))

[[!redirects telescopes]]