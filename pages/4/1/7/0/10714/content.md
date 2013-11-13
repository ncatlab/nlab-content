
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

## Statement


### A

For $X$ a [[homotopy type]]/[[spectrum]] and for all $n$, there is a [[homotopy pullback]]

$$
  \array{
    L_{E(n)}X &\longrightarrow& L_{K(n)}X
    \\
    \downarrow && \downarrow
    \\
    L_{E(n-1)}X &\longrightarrow& L_{E(n-1)}L_{K(n-1)}X
  }
  \,,
$$

where $L_{K(n)}$ denotes the [[Bousfield localization of spectra]] at $n$th [[Morava K-theory]] and similarly $L_{E(n)}$ denotes localization at [[Morava E-theory]].

([Lurie 10, lect 23, theorem 4](#LurieLecture23))

This implies that for understanding the [[chromatic tower]] of any [[spectrum]] $X$, it is in principle sufficient to understand all its "chromatic pieces" $L_{K(n)} X$. This is the subject of [[chromatic homotopy theory]].

### B


Let $E$ be a [[ring spectrum]] and $X$ an arbitrary [[spectrum]]. Suppose that there exists an [[integer]] $s \geq 1$ such that, for every [[finite spectrum]] $F$, the $E$-based [[Adams spectral sequence]] for $X \otimes F$ has $E^{p,q}_s$ for $p \geq s$.

If $E$ and $X$ are moreover a [[p-local spectra]] then $L_E X$ is a [[smashing localization]].

([Lurie 10, lect 31](#LurieLect31))


## References

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, 
Lecture 23 _The Bousfield Classes of $E(n)$ and $K(n)$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture23.pdf))
 {#LurieLecture23}

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 30 _Localizations and the Adams-Novikov spectral sequence_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture30.pdf))
 {#LurieLect30} 

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010,  Lecture 31 _The smash product theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture31.pdf))
 {#LurieLect31}