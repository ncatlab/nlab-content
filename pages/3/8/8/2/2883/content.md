
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

_&#201;tale cohomology_ is the [[abelian sheaf cohomology]] for [[sheaf|sheaves]] on the [[étale site]] of a [[scheme]] (which is an analog of the [[category of open subsets]] of a [[topological space]]).

## History ##

Etale cohomology was conceived by Artin, Deligne, [[Alexander Grothendieck|Grothendieck]] and Verdier in 1963. It was used by Deligne to prove the [[Weil conjecture]]s.

Some useful remarks on this are in the begining of

* Spencer Bloch, Review of Milne's _&#201;tale cohomology_ ([pdf](http://www.ams.org/bull/1981-04-02/S0273-0979-1981-14894-1/S0273-0979-1981-14894-1.pdf))

Milne's lectures (basically a slightly watered-down version of the text mentioned above) is available at

* John Milne, _Lectures on &#201;tale cohomology_ ([pdf](http://www.jmilne.org/math/CourseNotes/LEC.pdf))

## Details ##

Given a [[scheme]] $X$ of finite type, the small [[étale site]] $Et(X)$ is the [[category]] whose [[object]]s are [[etale morphism|étale morphism]]s $Spec R \to X$ and whose morphisms $(f:Spec R\to X)\to (f':Spec R'\to X)$ are morphisms $\alpha: Spec(R)\to Spec(R')$ of schemes completing triangles: $f'\circ\alpha=f$ (notice that the morphisms between &#233;tale morphisms are automatically &#233;tale). This category naturally carries a [[Grothendieck topology]] that makes it a [[site]].

The **&#233;tale cohomology** $H_{et}^\bullet(X,A)$ for $A \in Sh(Et(X), Ab)$ of $X$ is the [[abelian sheaf cohomology]] with respect to this site.


## References


The classical references are

* [[Pierre Deligne]] et al., _Cohomologie &#233;tale_ , Lecture Notes in Mathematics, no. 569, Springer-Verlag, 1977.
{#Deligne}

* [[James Milne]], _Etale cohomology_, Princeton Mathematical Series __33__, 1980. xiii+323 pp.

Lecture notes are

* [[James Milne]], _Lectures on etale cohomology_ ([pdf](http://www.jmilne.org/math/CourseNotes/LEC.pdf))

* [[Aise Johan de Jong]], _&#201;tale cohomology_ ([pdf](http://math.columbia.edu/~pugin/Teaching/Etale_files/EtaleCohomology.pdf))
{#deJong}




[[!redirects étale cohomology]]