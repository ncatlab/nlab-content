
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

## Examples

### Chromatic layers of the sphere spectrum

Discussion of the first chromatic layer of the [[sphere spectrum]]
is due to ([Miller-Ravenel-Wilson 77](#MillerRavenelWilson77)). Review is in ([Knudsen 13](#Knudsen13)). This is the [[image of the J-homomorphism]].


## Related concepts

* [[chromatic convergence theorem]]

* [[smash product theorem]]

## References

General lecture notes include

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 34 _Monochromatic layers_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture34.pdf))
 {#LurieLect34}

Discussion of the chromatic layers of the [[sphere spectrum]] is in

* [[Haynes Miller]], [[Doug Ravenel]], Stephen Wilson, _Periodic phenomena in the Adams-Novikov spectral sequence_ ([JSTOR](http://www.jstor.org/stable/1971064))
 {#MillerRavenelWilson77}

Lecture notes on this  include

* Ben Knudsen, _First chromatic layer of the sphere spectrum = homotopy of the $K(1)$-local sphere_, talk at _[2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php)_ ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-04-04-Rob-Legg-K1-local-sphere.pdf))
 {#Knudsen13}

* Johan Konter, _The $K(n)$-local sphere_, talk at _[Talbot 2013: Chromatic homotopy theory](http://math.mit.edu/conferences/talbot/index.php?year=2013&sub=talks)_ ([pdf](http://math.mit.edu/conferences/talbot/2013/8-Konter-LK(n)S.pdf))

* Drew Heard, _Resolutions of the $K(2)$-local sphere_, talk at _[Talbot 2013: Chromatic homotopy theory](http://math.mit.edu/conferences/talbot/index.php?year=2013&sub=talks)_ ([pdf](http://math.mit.edu/conferences/talbot/2013/19-Lawson-thefuture.pdf))


[[!redirects monochromatic layers]]

[[!redirects chromatic layer]]
[[!redirects chromatic layers]]