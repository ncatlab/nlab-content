
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[string theory]] the term _swampland_ had been introduced ([Vafa 05](#Vafa05)) to publicly highlight the basic fact that many [[effective quantum field theory]] [[vacuum state|vacua]] will not admit a [[UV-completion]] to a [[string theory vacuum]], hence that admitting a completion to a [[string theory vacuum]] is a strong constraint, hence that [[string theory]] predicts many more conditions to be satisfied by [[gauge groups]], [[field (physics)|field content]] and [[coupling constants]] than predicted by plain [[quantum field theory]].

The terminology was motivated since the collection of [[string theory vacua]] had previously come to be called the _[[landscape of string theory vacua]]_. The idea is to imagine the remaining [[effective field theory|EFTs]] not "in" this landscape to form a space "away from the landscape", whence the colorful imagery of a swampland.

More in detail, there is supposedly a map

\[
  \label{PointParticleLimitMap}
  \text{String Vacua}
  \overset{\;\;ppl\;\;}{\longrightarrow}
  \text{effective QFT Vacua}
\]

that takes [[string theory vacua]] to their low-energy approximation by [[vacuum state|vacua]] of [[effective quantum field theories]]. One way to possibly formalize this is to take the point-particle limit (ppl) of [[2d SCFTs]] to obtain [[spectral triples]] (as discussed at _[[2-spectral triple]]_) taking [[string]] [[worldsheets]] to [[Feynman diagrams]]:

<img src="https://ncatlab.org/nlab/files/PointParticleLimitOfStringDiagram.png" width="300">

> graphics grabbed from [Schubert 96](worldline+formalism#Schubert96)

Then with language of [[homological algebra]] or more generally of [[category theory]] we may begin to formalize the situation as follows:

1. the [[domain]] of (eq:PointParticleLimitMap) is the [[landscape of string theory vacua]];

1. the [[image]] of (eq:PointParticleLimitMap) is the landscape of corresponding [[effective quantum field theories|eQFTs]] that admit stringy [[UV-completion]];

1. the [[cokernel]] of (eq:PointParticleLimitMap) is the _swampland_;

1. the [[kernel]] of (eq:PointParticleLimitMap), or more generally its [[fiber]] over any [[effective quantum field theory|EFT]], is the space of different choices of stringy [[UV-completion]] of the same [[effective quantum field theory]].

Making this fully precise requires saying more about what the [[domain]] and [[codomain]] in (eq:PointParticleLimitMap) actually are, and in which ambient [[category]] (they will be some kind of [[moduli stacks]] in an ambient [[(∞,1)-category]] which may not quite be [[stable (∞,1)-category|stable]], whence "[[cokernel]]" may need to be interpreted in a non-abelian sense; but such details don't change the general idea here).

For example, part of what it means to specify a [[string theory vacuum]] is to declare the [[D-brane charge]] contained in this vacuum (subject to [[RR-field tadpole cancellation]] against [[O-plane]]-charges). In actual [[string theory]] this [[RR-field]] [[charge]] is supposed to be (see [there](D-brane#ReferencesKTheoryDescription)) a [[cocycle]] in some flavour of [[topological K-theory]] ([[twisted K-theory|twisted]] [[equivariant K-theory|equivariant]] [[differential K-theory|differential]] [[KR-theory]]), while its image in the underlying [[effective field theory]] is in the corresponding flavour of [[ordinary cohomology]]/[[de Rham cohomology]]. The map that relates the two incarnations of RR-field charge is the _[[Chern character]]_, which is what formalizes the map (eq:PointParticleLimitMap) in in the D-brane charge "sector" of the theory

$$
  \array{
    \text{String Vacua}
    &\overset{\;\;ppl\;\;}{\longrightarrow}&
    \text{effective QFT Vacua}
    \\
    \left\{
    \array{
      \text{D-brane RR-charge}
      \\
      \text{in K-theory}
    }
    \right\}
    &\overset{\text{Chern character}}{\longrightarrow}&
    \left\{
    \array{
      \text{flux forms in}
      \\
      \text{ordinary cohomology}
    }
    \right\}
  }
$$

The [[Chern character]] in general does have non-trivial [[cokernel]] ("swampland RR-fields") and [[kernel]] (choices of [[UV-completion]] of the effective RR-fields). In fact it fits not just in a [[short exact sequence]], but in the [[differential cohomology hexagon]] (see there for more) of [[K-theory]].

<center>
<img src="https://ncatlab.org/nlab/files/CohomotopySwampland.jpg" width="700">
</center>

> graphics grabbed from [SS 18](#SS18)

In contrast to this example, the literature on the "swampland" phenomenon is currently dominated by informal hand-wavy arguments. Starting with [Ooguri-Vafa 06](#OoguriVafa06) is an attempt to guess semi-precise rules-of-thumb for recognizing [[effective field theory|EFTs]] in the swampland, now known as the _swampland conjectures_. Motivated by the re-opening of the question whether [[de Sitter spacetime]] actually appears in [[string theory vacua]] or not ([Danielsson-van Riet 18](#DanielssonVanRiet18)), these swampland conjecture currently revolve around bounds on the [[cosmological constant]] in relation to [[scalar fields]] in the theory.

An argument that much of the existing swampland literature does not even live up to the level of rigour of [[folklore]] string theory, and in fact that it is fundamentally flawed, is made in [Banks 19](#Banks19).


## References

### General

The terminology originates with

* {#Vafa05} [[Cumrun Vafa]], _The String Landscape and the Swampland_ ([arXiv:hepth/0509212](http://arxiv.org/abs/hepth/0509212))

Comprehensive review is in:

* Eran Palti, _The Swampland: Introduction and Review_, lecture notes ([arXiv:1903.06239](https://arxiv.org/abs/1903.06239))

Further discussion includes

* {#OoguriVafa06} [[Hirosi Ooguri]], [[Cumrun Vafa]], _On the Geometry of the String Landscape and the Swampland_, Nucl.Phys.B766:21-33, 2007 ([arXiv:hep-th/0605264](https://arxiv.org/abs/hep-th/0605264))

* {#BrennanCartaVafa17} T. Daniel Brennan, Federico Carta, [[Cumrun Vafa]], _The String Landscape, the Swampland, and the Missing Corner_ ([arXiv:1711.00864](https://arxiv.org/abs/1711.00864))

* [[Ben Heidenreich]], [[Matthew Reece]], [[Tom Rudelius]], _Emergence and the Swampland Conjectures_ ([arXiv:1802.08698](https://arxiv.org/abs/1802.08698))

See also 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Swampland_(physics)">Swampland_(physics)</a>_

Beware that the landscape literature is presently dominated by non-rigorous hand-wavy [[string phenomenology]]:

* {#Banks19} [[Tom Banks]], _On the Limits of Effective Quantum Field Theory: Eternal Inflation, Landscapes, and Other Mythical Beasts_ ([arxiv:1910.12817](https://arxiv.org/abs/1910.12817))

  from pages 14-22:

  > these considerations lead to conclusions at odds with the seemingly similar arguments of $[$ the [[swampland conjectures]] $]$. $[\cdots]$  Perturbative moduli space completely distorts the true nature of the class of consistent models.

  > It’s important to realize that the entire procedure just outlined for finding (meta) stable AdS minima of a non-perturbative effective potential is purely hypothetical and has no basis in well founded string theory calculations. $[\cdots].$ 

  > The hypothesis of the String Landscape is entirely based on low energy effective field theory ideas about finding "vacua" by minimizing an effective potential.  Everything that’s been said above indicates that this idea has no validity in genuine models of quantum gravity. $[\cdots]$

  > The most serious issue,  in  my  opinion,  is  the  contention  that  one  can  make  the  AdS  radius  much  larger  thanthe size of the compact manifold.  All well established examples of large radius AdS/CFT havea compact manifold of dimension 2 or greater whose radius is comparable to that of the AdSspace.  In Appendix A we’ll present an argument based on the properties of AdS black holes,that this is in fact necessary.

  > The next step in the construction of "realistic" models involves "adding an anti-brane to break supersymmetry and make the c.c.  positive".  This is supposed to be a small modification of the model, calculable in low energy effective field theory, and that seems manifestly incorrect. $[\cdots]$.

  > even if one believes that the construction of meta-stable dS models is reliable, there is no clear argument about  what  the  proper  observables  of  the  model  are  nor  that different  dS  constructions are part of the same model.  Neither is there an interpretation of these correlators as transition amplitudes in a quantum mechanical model. $[\cdots]$

  > The conclusion  that  effective  field  theorists  should  draw  from  this is that unlike super-symmetric string models in flat or AdS space-time, many of which have at least perturbative definitions as mathematical models obeying the axioms of quantum mechanics, all literature on the String Landscape is speculation based on the unfounded notion that all string models with a given amount of SUSY are part of one single model and that it makes sense to define an effective action that encompasses all string models. Every single non-perturbative construction of string models contradicts this claim $[\cdots]$

Identification of the swampland charge structure with the [[cokernel]] of the [[Chern character]]:

* {#SS18} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Lift of fractional D-brane charge to equivariant Cohomotopy theory|Lift of fractional D-brane charge to equivariant Cohomotopy theory]]_ ([arXiv:1812.09679](https://arxiv.org/abs/1812.09679), [Python code](https://arxiv.org/src/1812.09679v1/anc))


### de Sitter vacua

One question is if [[de Sitter spacetime]]-vacua belong to the swampland or not:

* {#DanielssonVanRiet18} [[Ulf Danielsson]], [[Thomas Van Riet]],  _What if string theory has no de Sitter vacua?_, International Journal of Modern Physics D, Vol. 27, No. 12, 1830007 (2018)  ([arXiv:1804.01120](https://arxiv.org/abs/1804.01120), [doi:10.1142/S0218271818300070](https://doi.org/10.1142/S0218271818300070))

* {#vanRiet18} [[Thomas Van Riet]], _Is dS space in the Swampland_, talk at [StringPheno18](http://sp18.fuw.edu.pl/) ([pdf slides](http://sp18.fuw.edu.pl/wp-content/uploads/participants-database/thomasvanriet.pdf))

* {#vanRiet18a} [[Thomas Van Riet]], _Status of KKLT_, talk at _[Simons summer workshop 2018](http://scgp.stonybrook.edu/archives/24870)_ ([recording](http://scgp.stonybrook.edu/video_portal/video.php?id=3730))

* {#ObiedOoguriSpodyneikoVafa18} Georges Obied, [[Hirosi Ooguri]], Lev Spodyneiko, [[Cumrun Vafa]], _De Sitter Space and the Swampland_ ([arXiv:1806.08362](https://arxiv.org/abs/1806.08362))

* {#AgrawalObiedSteinhardtVafa18} Prateek Agrawal, Georges Obied, Paul Steinhardt, [[Cumrun Vafa]], _On the Cosmological Implications of the String Swampland_ ([arXiv:1806.09718](https://arxiv.org/abs/1806.09718))

* {#Vafa18} [[Cumrun Vafa]], _Cosmology and the String Swampland_, talk at _[Strings 2018](https://indico.oist.jp/indico/event/5/)_ ([pdf slides](https://indico.oist.jp/indico/event/5/picture/96.pdf), [recording](https://www.youtube.com/watch?v=fU8sJRCRz24&t=1904s))

* [[Frederik Denef]], Arthur Hebecker, Timm Wrase, _The dS swampland conjecture and the Higgs potential_ ([arXiv:1807.06581](https://arxiv.org/abs/1807.06581))

* {#Danielsson18} [[Ulf Danielsson]], _The quantum swampland_ ([arXiv:1809.04512](https://arxiv.org/abs/1809.04512))

  (argues that the issue with [[string theory|stringy]] de Sitter [[moduli stabilization]] raised in [Sethi 17](#Sethi17) is related to the de Sitter instability seen in QFT, according to the references [above](de+Sitter+spacetime#InPerturbativeQuantumGravity))

[[!redirects swampland conjecture]]
[[!redirects swampland conjectures]]
