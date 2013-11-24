
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

Traditional _&#233;tale cohomology_ (e.g. [Deligne 77](#Deligne77)) is the [[abelian sheaf cohomology]] for [[sheaf|sheaves]] on the [[étale site]] of a [[scheme]] -- which is an analog of the [[category of open subsets]] of a [[topological space]] $X$ , or rather the analog of the category of [[étale spaces]] over $X$, with [[finite set|finite]] [[fibers]].

A certain [[inverse limit]] over &#233;tale cohomology groups for different [[coefficients]] yields [[ℓ-adic cohomology]], which is a [[Weil cohomology theory]].

More generally, there is &#233;tale [[generalized cohomology theory]] with [[coefficients]] in [[sheaves of spectra]] on the [[étale site]] ([Jardine 97](#Jardine97)). Still more generally, there is &#233;tale generalized cohomology on the [[étale (∞,1)-site]] ([Antieau-Gepner 12](#AntieauGepner12), [Lurie](#Lurie)).



## Details ##

Given a [[scheme]] $X$ of finite type, the small [[étale site]] $Et(X)$ is the [[category]] whose [[object]]s are [[etale morphism|étale morphism]]s $Spec R \to X$ and whose morphisms $(f:Spec R\to X)\to (f':Spec R'\to X)$ are morphisms $\alpha: Spec(R)\to Spec(R')$ of schemes completing triangles: $f'\circ\alpha=f$ (notice that the morphisms between &#233;tale morphisms are automatically &#233;tale). This category naturally carries a [[Grothendieck topology]] that makes it a [[site]].

The **&#233;tale cohomology** $H_{et}^\bullet(X,A)$ for $A \in Sh(Et(X), Ab)$ of $X$ is the [[abelian sheaf cohomology]] with respect to this site.

## Properties

### Proper base change theorem

* [[proper base change theorem]]

([Milne, section 17](#Milne))


### Comparison theorem: Relation to singular cohomology

* [[comparison theorem (étale cohomology)]]

([Milne, section 21](#Milne))

### K&#252;nneth formula
 {#K&#252;nnethFormula}

([Milne, section 22](#Milne))

### Cycle map
 {#CycleMap}

([Milne, section 23](#Milne))

### Poincar&#233; duality
 {#PoincareDuality}

([Milne, section 24](#Milne))

### Lefschetz fixed-point formula

[K&#252;nneth formula](#K&#252;nnethFormula) + [cycle map](#CycleMap) + [Poincar&#233; duality](#PoincareDuality) $\Rightarrow$ [[Lefschetz fixed-point formula]]
 

([Milne, section 25](#Milne))



### With coefficients in the multiplicative group

the &#233;tale cohomology groups with [[coefficients]] in the [[multiplicative group]] $\mathbb{G}_m$ in the first few degrees go by special names:

* $H^0_{et}(-, \mathbb{G}_m)$: [[group of units]];

* $H^1_{et}(-, \mathbb{G}_m)$: [[Picard group]];

* $H^2_{et}(-, \mathbb{G}_m)$: [[Brauer group]];


### Relation to Zariski cohomology
 {#RelationZariskiEtaleCohomology}

+-- {: .num_remark #LerayForInclusionOfZariskiIntoEtale}
###### Remark

For $X$ a [[scheme]], the inclusion

$$
  \epsilon \;\colon\; X_{Zar} \longrightarrow X_{et}
$$

of the [[Zariski site]] into the [[étale site]] is indeed a [[morphism of sites]]. Hence there is a [[Leray spectral sequence]] which computes &#233;tale cohomology in terms of Zarsiki cohomology 

$$
  E^{p,q}_2 = H^p(X_{Zar}, R^q \epsilon^\ast \mathcal{G})
  \Rightarrow
  E^{p+q} = H^{p+q}(X_{et}, \mathcal{F})
  \,.
$$

=--

(e.g. [Tamme, II 1.3](#Tamme))

+-- {: .num_defn }
###### Definition

For $N$ a [[quasi-coherent sheaf]] of $\mathcal{O}_X$-[[modules]],
the edge morphism 

$$
  H^p_{Zar}(X, N)
  \longrightarrow
  H^p_{et}(X,N)
$$

of the [[Leray spectral sequence]] of remark \ref{LerayForInclusionOfZariskiIntoEtale} is an  [[isomorphism]] for all $p$


=--

e.g. ([Tamme, II (4.1.2)](#Tamme))

+-- {: .proof}
###### Proof

(...)

=--



## Related concepts

* [[étale morphism]], [[étale site]], &#233;tale cohomology

* [[étale (∞,1)-site]], [[étale topos]]

* [[étale homotopy]]

* [[Weil conjecture]]


## References

### History, motivation and original accounts

&#201;tale cohomology was conceived by [[Artin]], [[Deligne]], [[Alexander Grothendieck|Grothendieck]] and [[Verdier]] in 1963. It was used by Deligne to prove the [[Weil conjectures]]. Some useful (and also funny) remarks on this are in the beginning of

* [[Spencer Bloch]], Review of [[Milne]]'s _[[Étale Cohomology]]_ ([pdf](http://www.ams.org/bull/1981-04-02/S0273-0979-1981-14894-1/S0273-0979-1981-14894-1.pdf); publisher's [book page](http://www.worldscibooks.com/mathematics/7773.html))

See also

* MathOverflow _[&#201;tale cohomology &#8212; Why study it?](http://mathoverflow.net/questions/6070/etale-cohomology-why-study-it)_

The classical references include [[SGA]], esp.

* [[Pierre Deligne]] et al., _Cohomologie &#233;tale_ , Lecture Notes in Mathematics __569__, Springer-Verlag, 1977.
{#Deligne77}

* [[James Milne]], _[[Étale Cohomology]]_, Princeton Mathematical Series __33__, 1980. xiii+323 pp.

See also

* [[Barry Mazur]], _Notes on &#233;tale cohomology of number fields_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 6 no. 4 (1973), p. 521-552  ([Numdam](http://www.numdam.org/item?id=ASENS_1973_4_6_4_521_0), [pdf](http://modular.math.washington.edu/edu/2010/582e/refs/mazur-notes_on_etale_cohomology_of_number_fields_original.pdf))



### Reviews and modern accounts

* [[Günter Tamme]], _[[Introduction to Étale Cohomology]]_, 1994
 {#Tamme}

A modern textbook, though largely based on the material in SGA is 

* Lei Fu, _&#201;tale cohomology theory_, Nankai Tracts in Math. __13__, World Sci. 2011; ([toc pdf](http://www.worldscibooks.com/etextbook/7773/7773_toc.pdf); Preface [pdf](http://www.worldscibooks.com/etextbook/7773/7773_preface.pdf); chap. 1 Descent theory [pdf](http://www.worldscibooks.com/etextbook/7773/7773_chap01.pdf)) 


Lecture notes include

* [[James Milne]], _[[Lectures on Étale Cohomology]]_ ([html](http://www.jmilne.org/math/CourseNotes/lec.html), [pdf](http://www.jmilne.org/math/CourseNotes/LEC.pdf))
 {#Milne}

* [[Aise Johan de Jong]], _&#201;tale cohomology_ 2009, in _[[The Stacks Project]]_ ([pdf](http://math.columbia.edu/~pugin/Teaching/Etale_files/EtaleCohomology.pdf))
{#deJong}

* [[Evan Jenkins]], _&#201;tale cohomology seminar_  ([web](http://math.uchicago.edu/~ejenkins/etale/))

* Donu Arapura, _An introduction to &#201;tale cohomology_ ([pdf](http://www.math.purdue.edu/~dvb/preprints/etale.pdf))

* Antoine Ducros, _&#201;tale cohomology of schemes and analytic spaces_, ([pdf](http://www.math.jussieu.fr/~ducros/Cohetale.pdf))

See also


* Edgar Costa, _&#201;tale cohomology_ ([pdf](https://dspace.ist.utl.pt/bitstream/2295/686086/1/tese.pdf))

* Thomas H. Geisser, _Weil-etale motivic cohomology_, [K-th archive](http://www.math.illinois.edu/K-theory/0565)


Discussion of [[generalized cohomology theory]] on the [[étale site]] but with [[coefficients]] in [[sheaves of spectra]] is in 

* [[Rick Jardine]], _Generalized &#201;tale cohomology theories_, 1997 Progress in mathematics volume 146
 {#Jardine97}

Discussion of generalized &#233;tale cohomology over the [[étale (∞,1)-site]] (hence in [[higher topos theory]]/[[higher algebra]]) is in 

* [[Benjamin Antieau]], [[David Gepner]], _Brauer groups and &#233;tale cohomology in derived algebraic geometry_ ([arXiv:1210.0290](http://arxiv.org/abs/1210.0290))
 {#AntieauGepner12}

* [[Jacob Lurie]], _Descent theorems_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XI.pdf))
  {#Lurie}

[[!redirects étale cohomology]]

[[!redirects generalized étale cohomology]]
[[!redirects generalized étale cohomologies]]

[[!redirects generalized etale cohomology]]
[[!redirects generalized etale cohomologies]]