
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In the context of [[complex analytic geometry]], the term "exponential exact sequence" typically referes to the [[short exact sequence]]

$$
  0 \to ker(\exp) \longrightarrow \mathbb{G}_{a} \stackrel{\exp(\tfrac{i}{\hbar}(-))}{\longrightarrow} \mathbb{G}_m \to 0
$$

given by the [[exponential map]] $\exp(\tfrac{i}{\hbar}(-))$ from the [[additive group]] to the [[multiplicative group]]. Here $\hbar$ is any element of $\mathbb{R}^\times$ ("[[Planck's constant]]") but is traditionally set either to $1$ or to $1/2 \pi$. 

Hence more explicitly over the [[complex numbers]] this is 

$$
  0 \to \hbar2\pi\mathbb{Z} \longrightarrow \mathbb{C} \stackrel{\exp(\tfrac{i}{\hbar}(-))}{\longrightarrow} \mathbb{C}^\times \to 0
  \,,
$$

where $\mathbb{C}$ denotes the complex numbers as the additive [[abelian group]] and where $\mathbb{C}^\times = \mathbb{C} - \{0\}$ is the [[group of units]] of the [[ring]] structure of the complex numbers.

Often this is considered and displayed [[slice topos|relative]] to a [[complex analytic space]] $X$, where in terms of the [[structure sheaf]] $\mathcal{O}_{X}$ it reads

$$
  0 \to Lconst(\mathbb{Z}) \longrightarrow \mathcal{O}_X \stackrel{\exp(\tfrac{i}{\hbar}(-))}{\longrightarrow} \mathcal{O}_X^\times \to 0
  \,.
$$

In this form the sequence is then also called the _exponential sheaf sequence_.


## Properties

### Long sequence in cohomology
 {#LongSequenceInCohomology}

The [[connecting homomorphisms]] of the [[long exact sequence in cohomology]] induces by the exponential exact sequence

$$
  H^n(-,\mathbb{G}_m) \longrightarrow H^{n+1}(-,\mathbb{Z})
$$

encode the canonical [[characteristic classes]] of [[line n-bundles]].
 
* For $n=1$ this is the [first Chern class in complex analytic geometry](first+Chern+class#InComplexAnalyticGeometry) defined on the [[Picard group]] of [[holomorphic line bundles]]; 

* for $n = 2$ this is the complex analytic-analog of the [[Dixmier-Douady class]] of [[holomorphic 2-line bundles]], defined on the [[bigger Brauer group]];

and so on.

### In logarithmic geometry
 {#InLogarithmicGeometry}

In [[algebraic geometry]] there is no exponential sequence, the closest analogs being the [[Kummer sequence]] and the [[Artin-Schreier sequence]]. But in [[logarithmic geometry]] there is again a kind of exponential sequence (e.g. [Ogus 01, chapter IV, remark 1.1.7](#Ogus01), [Brylinski 94, page 15](#Brylinski94))

## Related concepts

* [[Kummer exact sequence]]

* [[Artin-Schreier exact sequence]]

* [[Kummer-Artin-Schreier-Witt exact sequence]]

 
## References

* Wikipedia, _[Exponential sheaf sequence](http://en.wikipedia.org/wiki/Exponential_sheaf_sequence)_

Discussion in [[real analytic geometry]]:

* {#Huisman02} [[Johannes Huisman]], _The exponential sequence in real algebraic geometry and Harnack's Inequality for proper reduced real schemes_, Communications in Algebra, Volume 30, Issue 10, 2002 ([pdf](http://pageperso.univ-brest.fr/~huisman/rech/publications/exphi.pdf))

Discussion in [[logarithmic geometry]]

* {#Brylinski94} [[Jean-Luc Brylinski]], _Holomorphic gerbes and the Beilinson regulator_, Ast&#233;risque 226 (1994): 145-174 ([[Brylinski94.pdf:file]])

* {#Ogus01} [[Arthur Ogus]], _Lectures on logarithmic algebraic geometry_, TeXed notes, 2001, [pdf](http://math.berkeley.edu/~ogus/preprints/log_book/logbook.pdf)


[[!redirects exponential exact sequences]]

[[!redirects exponential sequence]]
[[!redirects exponential sequences]]

[[!redirects exponential short exact sequence]]
[[!redirects exponential short exact sequences]]