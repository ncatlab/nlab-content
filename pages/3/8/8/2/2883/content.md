
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



## Definition ##

+-- {: .num_prop }
###### Proposition


Given a [[scheme]] $X$ of finite type, the small [[étale site]] $X_{et}$ is the [[category]] whose [[objects]] are [[étale morphisms]] $Spec R \to X$ and whose morphisms $(f:Spec R\to X)\to (f':Spec R'\to X)$ are morphisms $\alpha: Spec(R)\to Spec(R')$ of schemes completing triangles: $f'\circ\alpha=f$ (notice that the morphisms between &#233;tale morphisms are automatically &#233;tale). This category naturally carries a [[Grothendieck topology]] that makes it a [[site]], the [[étale site]].

For $A \in Sh(X_{et}, Ab)$ an [[abelian sheaf]] on $X$, the **&#233;tale cohomology** $H_{et}^\bullet(X,A)$ of $X$ with [[coefficients]] in $A$  is the [[abelian sheaf cohomology]] with respect to this site.

=--

## Basic properties
 {#BasicProperties}

The following are some basic properties of &#233;tale [[cohomology groups]] for various standard choices of [[coefficients]]. 

### Relation to Zariski cohomology 
 {#RelationZariskiEtaleCohomology}

+-- {: .num_remark }
###### Remark

A [[cover]] in the [[Zariski topology]] on [[schemes]] is an [[open immersion of schemes]] and hence is in particular an [[étale morphism of schemes]]. Hence the [[étale site]] is finer than the [[Zariski site]] and so every &#233;tale [[sheaf]] is a Zariski sheaf, but not necessarily conversely. 

=--



+-- {: .num_remark #LerayForInclusionOfZariskiIntoEtale}
###### Remark

For $X$ a [[scheme]], the inclusion

$$
  \epsilon \;\colon\; X_{Zar} \longrightarrow X_{et}
$$

of the [[Zariski site]] into the [[étale site]] is indeed a [[morphism of sites]]. Hence there is a [[Leray spectral sequence]] which computes &#233;tale cohomology in terms of Zariski cohomology 

$$
  E^{p,q}_2 = H^p(X_{Zar}, R^q \epsilon^\ast \mathcal{F})
  \Rightarrow
  E^{p+q} = H^{p+q}(X_{et}, \mathcal{F})
  \,.
$$

=--

This is originally due to ([[Grothendieck]], [[SGA]] 4 (Chapter VII, p355)). Reviews include ([Tamme, II 1.3](#Tamme)).


### With coefficients in coherent modules
 {#WithCoefficientsInCoherentModules}

+-- {: .num_prop #CohomologyWithCoeffsInCoherentModules}
###### Proposition

For $N$ a [[quasi-coherent sheaf]] of $\mathcal{O}_X$-[[modules]] and $N_{et}$ the induced &#233;tale sheaf (by the discussion at [&#233;tale topos -- Quasicohetent sheaves](etale+topos#QuasiCoherentModules)),
then the [[edge morphism]]

$$
  H^p_{Zar}(X, N)
  \longrightarrow
  H^p_{et}(X,N_{et})
$$

of the [[Leray spectral sequence]] of remark \ref{LerayForInclusionOfZariskiIntoEtale} is an  [[isomorphism]] for all $p$, itentifying the [[abelian sheaf cohomology]] on the [[Zariski site]] with [[coefficients]] in $N$ with the &#233;tale cohomology with coefficients in $N_{et}$.

Moreover, for $X$ affine we have

$$
  H^p_{et}(X, N_{et}) \simeq 0
  \,.
$$


=--

This is due to ([[Grothendieck]], [[FGA]] 1). See also for instance ([Tamme, II (4.1.2)](#Tamme)).

+-- {: .proof}
###### Proof

By the discussion at _[[edge morphism]]_ it suffices to show that 

$$
  R^q \epsilon_\ast (N) = 0 \;\,,\;\;\; for \;\; p \gt 0
  \,.
$$

By the discussion at _[[direct image]]_ (also at _[[abelian sheaf cohomology]]_), $R^q \epsilon_\ast N$ is the [[sheaf]] on the [[Zariski topology]] which is the [[sheafification]] of the [[presheaf]] given by

$$
  U \mapsto H^q(X_{et}|U, N)
  \,,
$$

hence it is sufficient that this vanishes, or rather, by locality ([[sheafification]]) it suffices to show this vanishes for $X = U = Spec(A)$ an affine [[algebraic variety]].

By the existence of [cofinal affine &#233;tale covers](etale+site#CofinalAffineCovers) the [[full subcategory]] $X_{et}^{a} \hookrightarrow X_{at}$ with the induced [[coverage]] is a [[dense subsite]] of affines. Therefore it suffices to show the statement there. 
Moreover, by the finiteness condition on [[étale morphisms]]  every cover of $X_{et}^{a}$ may be refined by a finite cover, hence by an affine covering map 

$$
  Spec(B) \longrightarrow Spec(A)
  \,.
$$

It follows (by a discussion such as e.g. at [[Sweedler coring]]) that the corresponding [[Cech cohomology]] complex

$$
  N_{et}(Spec(A)) \to C^0(\{Spec(B) \to Spec(A)\}, N_{et}) \to C^1(\{Spec(B) \to Spec(A)\}, N_{et}) \to \cdots
$$

is of the form

$$
  0 \to N \to N \otimes_A B \to N \otimes_{A} B \otimes_A B \to \cdots
  \,.
$$

known as the [[Amitsur complex]].

Since $A \to B$ is a [[faithfully flat morphism]] it follows by the [[descent theorem]] that this is [[exact sequence|exact]], hence that the cohomology indeed vanishes.


=--

### With coefficients in a cyclic group
 {#WithCoefficientsInACyclicGroup}

+-- {: .num_prop}
###### Proposition

If $X = Spec(A)$ is an affine [[reduced scheme]] of [[characteristic]] a [[prime number]] $p$, then its [[étale cohomology]] with [[coefficients]] in $\mathbb{Z}/p\mathbb{Z}$ is

$$
  H^q(X, (\mathbb{Z}/p\mathbb{Z})_X)
  \simeq
  \left\{
    \array{
      A/(F - id)A & if\; q = 1
      \\
      0 & if \; q \gt 0
    }
  \right.
  \,.
$$


=--

+-- {: .proof}
###### Proof

Under the given assumptions, the [[Artin-Schreier sequence]] (see there) induces a [[long exact sequence in cohomology]] of the form

$$
  \begin{aligned}
    0 & \to 
    H^0(X_{et}, \mathbb{Z}/p\mathbb{Z}) \to H^0(X_{et}, \mathcal{O}_X) \stackrel{F-id}{\to} H^0(X_{et}, \mathcal{O}_X)
   \\
    & \to
     H^1(X_{et}, \mathbb{Z}/p\mathbb{Z}) \to H^1(X_{et}, \mathcal{O}_X) \stackrel{F-id}{\to} H^1(X_{et}, \mathcal{O}_X)
   \\
    & \to
     H^2(X_{et}, \mathbb{Z}/p\mathbb{Z}) \to H^2(X_{et}, \mathcal{O}_X) \stackrel{F-id}{\to} H^2(X_{et}, \mathcal{O}_X) \to \cdots
  \end{aligned}
  \,,
$$

where $F(-) = (-)^p$ is the [[Frobenius endomorphism]]. 
By prop. \ref{CohomologyWithCoeffsInCoherentModules}
the terms of the form $H^{p \geq 1}(X, \mathcal{O}_X)$ vanish,
and so from [[exact sequence|exactness]] we find an [[isomorphism]]

$$
  H^0(X_{et}, \mathcal{O}_X)/(F-id)(H^0(X_{et}, \mathcal{O}_X))
    \stackrel{\simeq}{\to}
  H^1(X_{et}, \mathbb{Z}/p\mathbb{Z})
  \,,
$$

hence the claimed isomorphism

$$
  A/(F-id)(A)
    \stackrel{\simeq}{\to}
  H^1(X_{et}, \mathbb{Z}/p\mathbb{Z})
  \,.
$$

By the same argument all the higher cohomology groups vanish, as claimed.


=--

### With coefficients in the multiplicative group

the &#233;tale cohomology groups with [[coefficients]] in the [[multiplicative group]] $\mathbb{G}_m$ in the first few degrees go by special names:

* $H^0_{et}(-, \mathbb{G}_m)$: [[group of units]];

* $H^1_{et}(-, \mathbb{G}_m)$: [[Picard group]] ([[Hilbert's theorem 90]], [Tamme, II 4.3.1](#Tamme));

* $H^2_{et}(-, \mathbb{G}_m)$: [[Brauer group]];


### With coefficients in groups of roots of unity

* [[Kummer sequence]] 

([Tamme, II, 4.4](#Tamme))

(...)

## Main theorems
 {#MainTheorems}

The following are the main theorems characterizing properties of &#233;tale cohomology. Together these theorems imply that &#233;tale cohomology, in its variant as [[l-adic cohomology]], is a [[Weil cohomology theory]].

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




## Related concepts

* [[basics of étale cohomology]]

* [[étale morphism]], [[étale site]], &#233;tale cohomology

* [[étale (∞,1)-site]], [[étale topos]]

* [[étale homotopy]]

* [[Weil conjecture]]

* [[continuous étale cohomology]]

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