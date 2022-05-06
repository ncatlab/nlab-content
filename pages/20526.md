
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

In [[string theory]] the term _swampland_ had been introduced ([Vafa 05](#Vafa05)) to publically highlight the basic fact that many [[effective quantum field theory]] [[vacuum state|vacua]] will not admit a [[UV-completion]] to a [[string theory vacuum]], hence that admitting a completion to a [[string theory vacuum]] is a strong constraint, hence that [[string theory]] predicts many more conditions to be satisfied by [[gauge groups]], [[field (physics)|field content]] and [[coupling constants]] than predicted by plain [[quantum field theory]].

The terminology was motivated since the collection of [[string theory vacua]] had previously come to be called the _[[landscape of string theory vacua]]_. The idea is to imagine the remaining [[effective field theory|EFTs]] not "in" this landscape to form a space "away from the landscape", whence the colorful imagery of a swampland.

More in detail, there is supposedly a map

\[
  \label{PointParticleLimitMap}
  StringVacua
  \overset{\;\;ppl\;\;}{\longrightarrow}
  eQFTVacua
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
    StringVacua
    &\overset{\;\;ppl\;\;}{\longrightarrow}&
    eQFTVacua
    \\
    \left\{
    \array{
      \text{D-brane RR-flux}
      \\
      \text{in K-theory}
    }
    \right\}
    &\overset{\text{Chern character}}{\longrightarrow}&
    \left\{
    \array{
      \text{RR-field in}
      \\
      \text{ordinary cohomology}
    }
    \right\}
  }
$$

The [[Chern character]] in general does have non-trivial [[cokernel]] ("swampland RR-fields") and [[kernel]] (choices of [[UV-completion]] of the effective RR-fields). In fact it fits not just in a [[short exact sequence]], but in the [[differential cohomology hexagon]] (see there for more) of [[K-theory]].



## References

The terminology originates with

* {#Vafa05} [[Cumrun Vafa]], _The String Landscape and the Swampland_ ([arXiv:hepth/0509212](http://arxiv.org/abs/hepth/0509212))

Comprehensive review is in:

* Eran Palti, _The Swampland: Introduction and Review_, lecture notes ([arXiv:1903.06239](https://arxiv.org/abs/1903.06239))

Beware that the landscape literature is presently compltely dominated by non-rigorous hand-wavy [[string phenomenology]].

See also

* {#BrennanCartaVafa17} T. Daniel Brennan, Federico Carta, [[Cumrun Vafa]], _The String Landscape, the Swampland, and the Missing Corner_ ([arXiv:1711.00864](https://arxiv.org/abs/1711.00864))

* Ben Heidenreich, [[Matthew Reece]], Tom Rudelius, _Emergence and the Swampland Conjectures_ ([arXiv:1802.08698](https://arxiv.org/abs/1802.08698))

Implications of the possible non-existence of [[de Sitter spacetime]] [[string theory vacua]] are explored in

* {#ObiedOoguriSpodyneikoVafa18} Georges Obied, [[Hirosi Ooguri]], Lev Spodyneiko, [[Cumrun Vafa]], _De Sitter Space and the Swampland_ ([arXiv:1806.08362](https://arxiv.org/abs/1806.08362))

* {#AgrawalObiedSteinhardtVafa18} Prateek Agrawal, Georges Obied, Paul Steinhardt, [[Cumrun Vafa]], _On the Cosmological Implications of the String Swampland_ ([arXiv:1806.09718](https://arxiv.org/abs/1806.09718))

* {#Vafa18} [[Cumrun Vafa]], _Cosmology and the String Swampland_, talk at _[Strings 2018](https://indico.oist.jp/indico/event/5/)_ ([pdf slides](https://indico.oist.jp/indico/event/5/picture/96.pdf), [recording](https://www.youtube.com/watch?v=fU8sJRCRz24&t=1904s))

* [[Frederik Denef]], Arthur Hebecker, Timm Wrase, _The dS swampland conjecture and the Higgs potential_ ([arXiv:1807.06581](https://arxiv.org/abs/1807.06581))

