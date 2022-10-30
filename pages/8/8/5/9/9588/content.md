
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
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

There are several [[cohomology theories]] that are being called _Morava E-theory_ at times:

* $B P\langle n\rangle$, the truncated [[Brown-Peterson spectrum]];

* $E(n)$, the [[Johnson-Wilson spectrum]], a localization of $B P \langle n\rangle$ at $v_n$;

* $\widehat{E(n)}$ the complete Johnson-Wilson spectrum

* $E(k,\Gamma)$ the [[Lubin-Tate spectrum]] associated to the universal deformation of a [[formal group law]] $\Gamma$ over $k$.

## Definition

Choose

* $k$ be a [[perfect field]] of [[characteristic]] $p$;

* $f$ be a [[formal group]] of [[height of a formal group|height]] $n$ over $k$.

Write

$$
  R \coloneqq W(k)[ [ v_1, \cdots, v_{n-1} ] ]
$$

for the [[Lubin-Tate ring]] of $f$, classifying its universal deformation.

By the discussion there, this is [[Landweber exactness|Landweber exact]], hence defines a [[cohomology theory]]. Therefore by the [[Landweber exact functor theorem]] there is an [[even periodic cohomology theory]] $E(n)^\bullet$ [[Brown representability theorem|represented by]] a [[spectrum]] $E(n)$ with the property that its [[homotopy groups]] are

$$
  \pi_\bullet(E(n))
  \simeq
  W(k)[ [v_1, \cdots, v_{n-1} ] ] [ \beta^{\pm 1} ]
$$

for $\beta$ of degree 2. This is called alternatively $n$th _Morava E-theory_, or _[[Lubin-Tate theory]]_ or _[[Johnson-Wilson theory]]_.

(e.g. [Lurie, lect 22](#LurieLect22))

## Properties

### As a localization of the $\infty$-group $\infty$-ring on $B^{n+1}\mathbb{Z}_p$

There is a [[Snaith theorem]] for the [[homotopy fixed points]] of 
the Morava E-theory spectrum $E_n$ for the canonical [[infinity-action|action]] of a certain group, which identifies these with a localization of the [[∞-group ∞-ring]] on the [[n-group|(n+1)-group]] $B^{n+1} \mathbb{Z}_p$. ([Westerland 12, theorem 1.2](#Westerland12))

See at _[Snaith-like theorem for Morava E-theory](Snaith+theorem#ForMoravaETheory)_ for more.

### Bousfield localization and chromatic filtration
 {#BousfieldLocalizationAndChromaticFiltration}

The [[Bousfield localization of spectra]] $L_{E(n)}$ at $n$th Morava E-theory is called _[[chromatic localization]]. It_ behaves on [[complex oriented cohomology theories]] like the restriction to the closed substack

$$
  \mathcal{M}_{FG}^{\leq n+1}
  \hookrightarrow
  \mathcal{M}_{FG} \times Spec \mathbb{Z}_{(p)}
$$

of the [[moduli stack of formal groups]] on those of [[height of a formal group|height]] $\geq n+1$. 

(e.g. [Lurie, lect 22, above theorem 1](#LurieLect22))

In this way the localization tower at the Morava E-theories
exhibits the [[chromatic filtration]] in [[chromatic homotopy theory]].


[[!include chromatic tower examples - table]]




### Smash product theorem

A version of the [[smash product theorem]]

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

 ([Lurie 10, lect 23, theorem 4](#LurieLect23))



### Bousfield equivalence class
 {#BousfieldEquivalenceClass}

For all $n$, $E(n)$ is [[Bousfield equivalence|Bousfield equivalence]] to $E(n-1) \times K(n)$, where the last factor is $n$th [[Morava K-theory]].

([Lurie 10, lect. 23, prop. 1](#LurieLect23))

## Related concepts

* [[Morava K-theory]]

* orthogonal form: [[EO(n)]]

* [[real-oriented cohomology theory|real]] form [[ER-theory]]

* [[Morava E-theoretic Chern character]]

* [[chromatic homotopy theory]]

Not to be confused with [[C*-algebra]]-[[E-theory]].

## References

Relevant background lecture notes include

* [[Mike Hopkins]], _Complex oriented cohomology theories and the language of stacks_, course notes ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

and more specifically see the lectures 

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture notes, ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture22.pdf)), Lecture 22 _Morava E-theory and Morava K-theory_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture22.pdf))
 {#LurieLect22}


* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture notes, ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture22.pdf))  Lecture 23 _The Bousfield Classes of $E(n)$ and $K(n)$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture23.pdf))
 {#LurieLect23}

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture notes, ([pdf]  Lecture 24 _Uniqueness of Morava K-theory_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture24.pdf))

also

* _Report of $E$-theory conjectures seminar_ (2013) ([pdf](http://math.berkeley.edu/~ericp/latex/misc/mit-ethy.pdf))


Discussion of the $E_\infty$-algebra structure over $B P$ is in

* [[Andrew Baker]], _Brave new Hopf algebroids_ ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/brave-ha.pdf))
 {#Baker}

based on 

* [[Neil Strickland]], _Products on $MU$-modules_, Trans. Amer. Math. Soc. 351 (1999), 2569-2606.
 {#Strickland99}


Discussion of [[twisted cohomology|twists]] of Morava E-theory is in 

* [[Hisham Sati]], [[Craig Westerland]], _Twisted Morava K-theory and E-theory_ ([arXiv:1109.3867](http://arxiv.org/abs/1109.3867))
 {#SatiWesterland11}

A [[Snaith theorem]]-line characterization of Morava E-theory is given in 

* [[Craig Westerland]], _A higher chromatic analogue of the image of J_ ([arXiv:1210.2472](http://arxiv.org/abs/1210.2472))
 {#Westerland12}

[[!redirects Morava E-theories]]