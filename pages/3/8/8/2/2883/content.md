
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
* table of contents
{:toc}

## Idea ##

Traditional _&#233;tale cohomology_ (e.g. [Deligne 77](#Deligne77)) is the [[abelian sheaf cohomology]] for [[sheaf|sheaves]] on the [[étale site]] of a [[scheme]] (which is an analog of the [[category of open subsets]] of a [[topological space]]).

A certain [[inverse limit]] over &#233;tale cohomology groups for different [[coefficients]] yields [[ℓ-adic cohomology]], which is a [[Weil cohomology theory]].

More generally, there is &#233;tale [[generalized cohomology theory]] with [[coefficients]] in [[sheaves of spectra]] on the [[étale site]] ([Jardine 97](#Jardine97)). Still more generally, there is &#233;tale generalized cohomology on the [[étale (∞,1)-site]] ([Antieau-Gepner 12](#AntieauGepner12), [Lurie](#Lurie)).



## Details ##

Given a [[scheme]] $X$ of finite type, the small [[étale site]] $Et(X)$ is the [[category]] whose [[object]]s are [[etale morphism|étale morphism]]s $Spec R \to X$ and whose morphisms $(f:Spec R\to X)\to (f':Spec R'\to X)$ are morphisms $\alpha: Spec(R)\to Spec(R')$ of schemes completing triangles: $f'\circ\alpha=f$ (notice that the morphisms between &#233;tale morphisms are automatically &#233;tale). This category naturally carries a [[Grothendieck topology]] that makes it a [[site]].

The **&#233;tale cohomology** $H_{et}^\bullet(X,A)$ for $A \in Sh(Et(X), Ab)$ of $X$ is the [[abelian sheaf cohomology]] with respect to this site.

## Properties

### With values in the multiplicative group

the &#233;tale cohomology groups with values in the [[multiplicative group]] $\mathbb{G}_m$ in the first few degrees go by special names:

* $H^0_{et}(-, \mathbb{G}_m)$: [[group of units]];

* $H^1_{et}(-, \mathbb{G}_m)$: [[Picard group]];

* $H^2_{et}(-, \mathbb{G}_m)$: [[Brauer group]];

## Related concepts

* [[étale morphism]], [[étale site]], &#233;tale cohomology

* [[étale (∞,1)-site]]

* [[Weil conjecture]]

## References

&#201;tale cohomology was conceived by [[Artin]], [[Deligne]], [[Alexander Grothendieck|Grothendieck]] and [[Verdier]] in 1963. It was used by Deligne to prove the [[Weil conjectures]]. Some useful remarks on this are in the begining of

* Spencer Bloch, Review of Milne's _&#201;tale cohomology_ ([pdf](http://www.ams.org/bull/1981-04-02/S0273-0979-1981-14894-1/S0273-0979-1981-14894-1.pdf); publisher's [book page](http://www.worldscibooks.com/mathematics/7773.html))


The classical references include [[SGA]], esp.

* [[Pierre Deligne]] et al., _Cohomologie &#233;tale_ , Lecture Notes in Mathematics __569__, Springer-Verlag, 1977.
{#Deligne77}

* [[James Milne]], _Etale cohomology_, Princeton Mathematical Series __33__, 1980. xiii+323 pp.

* [[Barry Mazur]], _Notes on &#233;tale cohomology of number fields_, [pdf](http://modular.math.washington.edu/edu/2010/582e/refs/mazur-notes_on_etale_cohomology_of_number_fields_original.pdf)

* Thomas H. Geisser, _Weil-etale motivic cohomology_, [K-th archive](http://www.math.illinois.edu/K-theory/0565)

A modern textbook, though largely based on the material in SGA is 

* Lei Fu, _Etale cohomology theory_, Nankai Tracts in Math. __13__, World Sci. 2011; ([toc pdf](http://www.worldscibooks.com/etextbook/7773/7773_toc.pdf); Preface [pdf](http://www.worldscibooks.com/etextbook/7773/7773_preface.pdf); chap. 1 Descent theory [pdf](http://www.worldscibooks.com/etextbook/7773/7773_chap01.pdf)) 

A comprehensive set of lecture notes is in

* [[James Milne]], _Lectures on &#201;tale cohomology_ ([html](http://www.jmilne.org/math/CourseNotes/lec.html), [pdf](http://www.jmilne.org/math/CourseNotes/LEC.pdf))

* [[Aise Johan de Jong]], _&#201;tale cohomology_ 2009, in _[[The Stacks Project]]_ ([pdf](http://math.columbia.edu/~pugin/Teaching/Etale_files/EtaleCohomology.pdf))
{#deJong}

* Antoine Ducros, _&#201;tale cohomology of schemes and analytic spaces_, [pdf](http://www.math.jussieu.fr/~ducros/Cohetale.pdf)

Discussion of [[generalized cohomology theory]] on the [[étale site]] but with [[coefficients]] in [[sheaves of spectra]] is in 

* [[Rick Jardine]], _Generalized &#201;tale cohomology theories_, 1997 Progress in mathematics volume 146
 {#Jardine97}

Discussion of generalized &#233;tale cohomology over the [[étale (∞,1)-site]] (hence in [[higher topos theory]]/[[higher algebra]]) is in 

* [[Benjamin Antieau]], [[David Gepner]], _Brauer groups and &#233;tale cohomology in derived algebraic geometry_ ([arXiv:1210.0290](http://arxiv.org/abs/1210.0290))
 {#AntieauGepner12}

* [[Jacob Lurie]], _Descent theorems_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XI.pdf))
  {Lurie}

[[!redirects étale cohomology]]

[[!redirects generalized étale cohomology]]
[[!redirects generalized étale cohomologies]]

[[!redirects generalized etale cohomology]]
[[!redirects generalized etale cohomologies]]
