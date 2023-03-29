
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In as far as a [[bireflective subcategory]] inclusion 
$$
  \mathcal{C} 
    \xhookrightarrow{\phantom{-} \iota \phantom{-}}
  \mathcal{B} 
    \xrightarrow{\phantom{-} \beta \phantom{-}}  \mathcal{C}
  \,,
  \;\;\;\;\;\;\;
  \beta \dashv \iota \dashv \beta
$$ 

is understood as an inclusion (via forming of [[zero object]]-bundles) of a [[category]] $\mathcal{C}$ of "classical" [[objects]] into a category $\mathcal{B}$ of [[bundles]] of [[infinitesimal objects|infinitesimal]] [[fibers]] over these  (as in [[infinitesimal cohesion]]), it makes sense to address the corresponding [[bireflective subcategory|bireflecting]] [[idempotent monad|idempotent]] [[Frobenius monad]] 

$$
  \natural 
    \,\coloneqq\, 
  \iota \circ \beta 
    \;\colon\; 
  \mathcal{B} \longrightarrow \mathcal{B}
$$ 

as the [[modal operator]] which projects out the "[[modal objects|mode of being]] classical", hence the *classical modality*.

For example, interpreting a [[tangent (infinity,1)-topos|tangent $\infty$-topos]] $T \mathbf{H}$ (generally an [[(infinity,1)-topos|$\infty$-topos]] of [[parameterized spectrum|parameterized]] [[module spectra]]) as the home of a kind of higher [[quantum information theory]] (as discussed at *[[motivic quantization]]* and *[[quantum circuits via dependent linear types]]*) then its [[infinitesimal cohesion]] $\iota \,\colon\, \mathbf{H} \hookrightarrow T \mathbf{H}$ characterizes exactly the "classical objects" in the standard sense of [[classical mechanics|classical]] vs [[quantum mechanics]].

A [[modal homotopy type theory|modal homotopy type theoretic]] formulation of the classical modality $\natural \,\colon\, T \mathbf{H} \to T \mathbf{H}$ in the [[internal language]] of such [[tangent (infinity,1)-topos|tangent $\infty$-toposes]] is proposed in [Riley, Finster & Licata (2021)](#RileyFinsterLicata21), its combination with a [[linear type theory|linear]] [[multiplicative conjunction]] $\otimes$ (and the required [[bunched logic]]) has been developed by [Riley (2022)](#Riley22Thesis) and the interpretation as a "classical modality" in the sense of [[classical mechanics|classical]]/[[quantum mechanics]] is discussed in [Myers et al. (2023)](#MyersEtAl).

## Related concepts

[[!include cohesion - table]]

## References

A system of [[inference rules]] for a classical modality added to [[homotopy type theory]] has been proposed in

* {#RileyFinsterLicata21} [[Mitchell Riley]], [[Eric Finster]], [[Daniel R. Licata]], *Synthetic Spectra via a Monadic and Comonadic Modality* &lbrack;[arXiv:2102.04099](https://arxiv.org/abs/2102.04099)&rbrack;

and combined with a [[linear type theory|linear]] [[multiplicative conjunction]] and the necessary [[bunched logic]] in

* {#Riley22Thesis} [[Mitchell Riley]], *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139), [ir:3269](https://digitalcollections.wesleyan.edu/object/ir%3A3269),  [pdf](https://mvr.hosting.nyu.edu/pubs/thesis.pdf)&rbrack;

The role as a "classical modality" (and introducing this terminology) making the resulting [[linear homotopy type theory]] a [[quantum programming language|formal quantum language]] is indicated in

* {#MyersEtAl} [[David Jaz Myers]], [[Mitchell Riley]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Quantum Certification via Linear Homotopy Types]]*

with further exposition in:

* [[Urs Schreiber]]: *Quantum Data Types via Linear Homotopy Type Theory*, talk at *[Workshop on Quantum Software](https://quasar.unina.it/qtml2022/workshop.php)* @ *[QTML 2022](https://quasar.unina.it/qtml2022.html)*, Naples (Nov 2022) &lbrack;slides:[pdf](/schreiber/files/QuantumDataInLHoTT-221117.pdf)&rbrack; 

[[!redirects classical modalities]]

