
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

### Statement

The original _Deligne conjecture_ on the structure of [[Hochschild cohomology]] of an [[associative algebra]] and more generally an [[A-∞ algebra]] states that Hochschild cohomology naturally has the structure of a [[BV-algebra]] and that moreover the full Hochschild cohomology complex has the structure of an [[algebra over an operad]] over the ([[framed little disk operad|framed]]) [[little disk operad]]. (The second statement implies the first since ([[BV-algebra|BV]]-)[[nLab:Gerstenhaber algebra]]s are [[algebras over an operad]] over the (framed) little disk operad.)

Proofs of the conjecture have been given first by  [McClure-Smith](#McClureSmith) and others, then also by [Kontsevich-Soibelman](#KontsevichSoibelman), and [Tamarkin](#Tamarkin).

A proof for general [[Ek-algebra]]s in [[symmetric monoidal (∞,1)-categories]] is in ([Lurie, section 2.5](#Lurie)).

### Geometric interpretation

A general geometric ([[higher geometry|higher geometric]]) interpretation has been indicated in [Ben-ZviFrancisNadler](#Ben-ZviFrancisNadler). They observed (see [[Hochschild cohomology]] for details) that the Hochschild _homology_ of $\mathcal{O}(X)$ is naturally interpreted as the algebra of functions on the [[derived loop space]] $\mathcal{L}X$. In the presence of good 
[[geometric ∞-function theory]] this naturally induces an action of the [[little disk operad]] on $\mathcal{O}(\mathcal{L}X)$. Since a [[Gerstenhaber algebra]] is an algebra over the [[homology]] of the [[little disk operad]], this immediately explains the existence of this structure.

### For higher algebras and higher monoidal categories

More generally, analogs of the statement of the Deligne conjecture exist and work for $(\infty,n)$-algebras: [[k-tuply monoidal n-categories]]. This is closely related to the statement (and proofs) of the [[delooping hypothesis]].

This case is discussed in ([Francis](#Francis)) and ([Lurie](#Lurie)).

In ([KockToen](#KockToen)) it is shown that in a [[monoidal model category]] that is also a [[simplicial model category]] the [[derived hom-space]] $\mathbb{R} Hom(I,I)$ from the tensor unit to itself is a [[Ek-algebra|E-2 algebra]].

### History

Historically it was first found that there is the structure of a [[Gerstenhaber algebra]] on $HH^\bullet(A,A)$.  By ([Cohen](#Cohen)) it was known that Gerstenhaber algebras arise as the [[homology]] of [[E2-algebra]]s in [[chain complex]]es. In a letter in 1993 Deligne wondered whether the [[Gerstenhaber algebra]] structure on the Hochschild cohomology $HH^\bullet(A,A)$ lifts to an [[E2-algebra]]-structure on the cochain complex $C^\bullet(A,A)$.

In [GerstenhaberVoronov (1994)](#GerstenhaberVoronov) a resolution of the Gerstenhaber algebra structure was given, but the relationship to $E_2$-algebras remained unclear.

In ([Tamarkin (1998)](#Tamarkin)) a genuine resolution in the [[model structure on operads]] of the Gerstenhaber operad was given and shown to act via the Gerstenhaber-Voronov construction on $C^\bullet(A,A)$. This proved Deligne's conjecture.

Various authors later further refined this result. A summary of this history can be found in ([Hess](#Hess)).

In [Hu-Kriz-Voronov (2003)](#HuKrizVoronov) it was further shown that for $A$ an [[En-algebra]], $C^\bullet(A,A)$ is an $E_{n+1}$-algebra.




## References

Direct proofs of the Deligne conjecture have been given in.

* James McClure, Jeffrey Smith, *A solution of Deligne's conjecture* ([arXiv:math/9910126](http://arxiv.org/abs/math/9910126))
{#McClureSmith}


* [[Maxim Kontsevich]], [[Yan Soibelman]], *Deformations of algebras over operads and Deligne's conjecture* ([arXiv:math/0001151](http://arxiv.org/abs/math/0001151))
{#KontsevichSoibelman}

* [[Dmitry Tamarkin]], *Another proof of M. Kontsevich formality theorem* ([arXiv:math/9803025](http://arxiv.org/abs/math/9803025))
{#Tamarkin}

* [[Clemens Berger]], [[Benoit Fresse]], *Combinatorial operad actions on cochains* ([arXiv:math/0109158](http://arxiv.org/abs/math/0109158))

A review is in 

* [[Kathryn Hess]], _Deligne's Hochschild cohomology conjecture_ ([pdf](http://sma.epfl.ch/~hessbell/Pub_DeligneColloq.pdf))
{#Hess}

* Cohen
{#Cohen}

* Gertstenhaber-Voronov
{#GerstenhaberVoronov}

* Hu, Kriz, Voronov
{#HuKrizVoronov}

A transparent [[higher geometry|higher geometric]] interpretation in a suitably dualizable context is indicated in 

* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], 
  _[[geometric infinity-function theory|Integral transforms and Drinfeld centers in derived algebraic geometry]]_ ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))
{#Ben-ZviFrancisNadler}

* [[John Francis]], PhD thesis ([web](http://dspace.mit.edu/handle/1721.1/43792))
{#Francis}

Section 2.5 of

* [[Jacob Lurie]], _[[Ek-Algebras]]_
{#Lurie}

A construction in [[monoidal model categories]] is in

* [[Joachim Kock]], [[Bertrand Toen]], _Simplicial localization of monoidal structures, and a non-linear version of Deligne's conjecture_ Compositio Math. 141 (2005), 253-261 ([arXiv](http://arxiv.org/abs/math.AT/0304442))
{#KockToen}


[[!redirects Deligne conjectures]]