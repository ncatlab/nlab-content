
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
  L_n \coloneqq L_{E(n)}
  \,,
$$

where $E(n)$ is the $n$th [[Morava E-theory]] (for the given [[prime]] $p$). These arrange into the _chromatic tower_ which for each spectrum $X$ is of the form

$$  
  X \to \cdots \to L_n X \to L_{n-1} X \to \cdots \to L_0 X
  \,.
$$

The [[homotopy fibers]] of each stage of the tower

$$
  M_n(X) \coloneqq fib(L_{E(n)}X \longrightarrow L_{E(n-1)}(X))
$$

is called the $n$th _monochromatic layer_ of $X$.

## References

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 34 _Monochromatic layers_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture34.pdf))
 {#LurieLect34}

[[!redirects monochromatic layers]]