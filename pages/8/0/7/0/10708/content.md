
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For each [[prime]] $p \in \mathbb{N}$ and for each [[natural number]]  $n \in \mathbb{N}$ there is a [[Bousfield localization of spectra]]

$$
  L_n \coloneqq L_{K(0)\vee \cdots \vee K(n)}
  \,,
$$

where $K(n)$ is the $n$th [[Morava K-theory]] (for the given [[prime]] $p$). These arrange into the _[[chromatic tower]]_ which for each spectrum $X$ is of the form

$$  
  X \to \cdots \to L_n X \to L_{n-1} X \to \cdots \to L_0 X
  \,.
$$

The _chromatic convergence theorem_ states mild conditions under which the [[homotopy limit]] over this tower is the $p$-[[Bousfield localization of spectra|localization]] 

$$
  X \to X_{(p)}
$$

of $X$. 

In particular if $X$ is a [[finite spectrum|finite]] [[p-local spectrum]] then the chromatic convergence theorem says that the [[homotopy limit]] over the [[chromatic tower]] of $X$ reproduces $X$.

Since moreover $L_n X$ is the [[homotopy fiber product]]

$$
  L_n X \simeq L_{K(n)}X \underset{L_{n-1}L_{K(n)}X}{\times} L_{n-1}X
$$

(see at _[[smash product theorem]]_ and see [this remark](fracture+theorem#ExampleOfChromaticFracturing) at _[[fracture square]]_ )
it follows that in principle one may study any [[spectrum]] $X$ by understanding all its "chromatic pieces" $L_{K(n)} X$. This is the topic of [[chromatic homotopy theory]].

## Related concepts

* [[chromatic layer]]

* [[smash product theorem]]

## References

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 32 _The chromatic convergence theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture32.pdf)) 


