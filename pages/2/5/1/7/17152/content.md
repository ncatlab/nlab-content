
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[free construction|free]] [[infinite loop space]] on a given [[pointed topological space]].

## Definition

Write

$$
  Q\;\colon\; Top^{\ast/} \longrightarrow Top^{*/}
$$

for the [[endofunctor]] on [[pointed topological spaces]] given as the [[colimit]]

$$
  Q X \coloneqq \underset{\longrightarrow}{\lim}_k \Omega^k \Sigma^k X
$$

over iterated [[suspension]] and [[loop space]] construction. 

This is the degree-0 part of [[spectrification]] of [[suspension spectra]].

Equivalently this is

$$
  Q X \simeq \Omega^\infty \Sigma^\infty X
$$

for

$$
 (\Sigma^\infty \dashv \Omega^\infty)
  \;\colon\;
  Ho(Spectra)
   \underoverset{\underset{\Omega^\infty}{\longrightarrow}}{\overset{\Sigma^\infty}{\longleftarrow}}{}
  Ho(Top)
$$

the [[stabilization]] [[adjunction]] between the [[homotopy category]] [[Ho(Top)]] and the [[stable homotopy category]] $Ho(Spectra)$.


## Related concepts

* [[spectrification]]

* [Omega spectrum -- Completion of a suspension spectrum](Omega-spectrum#CompletionOfSuspensionSpectra)

* [[stable homotopy group]]


## References

* {#Malkiewich11} [[Cary Malkiewich]], _Some facts about $Q X$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/Q.pdf))

[[!redirects free infinite loop spaces]]