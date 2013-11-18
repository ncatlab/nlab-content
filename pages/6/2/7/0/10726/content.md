


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

is called the $n$th _[[monochromatic layer]]_ of $X$.

The _[[chromatic convergence theorem]]_ states mild conditions under which the [[homotopy limit]] over this tower is the $p$-[[Bousfield localization of spectra|localization]] 

$$
  X \to X_{(p)}
$$

of $X$. 

Since moreover $L_n X$ is the [[homotopy fiber product]]

$$
  L_n X \simeq L_{K(n)}X \underset{L_{n-1}L_{K(n)}X}{\times} L_{n-1}X
$$

(see at [[smash product theorem]]) it follows that in principle one can study a spectrum $X$ by understanding all its "chromatic pieces" $L_{K(n)} X$. This is the topic of [[chromatic homotopy theory]].

## Properties

### Chromatic spectral sequence

The [[spectral sequence of a filtered stable homotopy type]] associated with the chromatic tower (regarded as a [[filtered object in an (infinity,1)-category]]) is the _[[chromatic spectral sequence]]_ ([Wilson 13, section 2.1.2](#Wilson13))

[[!include Lurie spectral sequences -- table]]


## Examples

[[!include chromatic tower examples - table]]


## Related concepts


* [[Postnikov tower]], [[Taylor tower]]



## References

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, 
Lecture 29 _Telescopic vs $E_n$-localization_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture29.pdf))

* [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the
Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php) ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))
 {#Wilson13}


[[!redirects chromatic towers]]
