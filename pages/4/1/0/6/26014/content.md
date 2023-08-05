
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Traditionally, a *[[global symmetry|global]] [[symmetry]]* is defined as [[invariance]] (e.g. of a physical system) under a [[group action]]. This definition is well-suited for physical systems such as in [[classical mechanics]], where symmetries appear as [[symplectomorphisms]] leaving a [[Hamiltonian]] invariant. 

However, many systems of interest depart, or **generalize**, from this setting in two different ways: as a [[classical field theory]], or as a [[quantum system]] (or as both, as a [[quantum field theory]]). A natural question to ask is what happens to the mathematical objects realizing the notion of symmetry when these generalizations are considered. The former case leads to the [[vertical categorification]] of groups to [[n-groups|$n$-groups]], as observed in [[higher prequantum geometry]]. The latter case leads to a [[ring]] (or [[algebra]]) structure. The concept of **generalized global symmetries** is thought to be the appropriate notion of symmetry when both of these generalizations take place at the same time. 

{#OriginOfTheTerminology} The terminology *generalized global symmetry* for such a situation is due to [Gaiotto, Kapustin, Seiberg & Willett (2014)](#GaiottoKapustinSeibergWillett14). As described therein (at a very in-formal level) classical symmetries (described by a group) that survive the quantization process are thought to become "[[operators]]" that can be "inserted" (namely into the [[integrand]] of a [[path integral]], though this step and its details are left implicit) along [[submanifolds]] (of [[spacetime]]) of [[positive number|positive]] [[codimension]]. 
These operators are supposed to be "topological", in the sense that they should only depend on the homology class of said submanifold. [GKSW14](#GaiottoKapustinSeibergWillett14) propose to regard any quantum operator with the topological property as a symmetry of the quantum system even if they do not have inverses. It is in this sense that the concept of symmetry is regarded as being generalized.

As emphasized by [Freed, Moore & Teleman (2022)](#FMT22), such phenomena should be controlled by [[higher algebra]]. Of course this is not quite a new observation, ideas broadly in this direction date back to [Roberts (1979)](John+Elias+Roberts#Roberts79). Concretly, "non-invertible symmetry insertions" are at least close to what elsewhere has long been known as *[[QFT with defects|defects in QFT]]* which have routinely been described via [[higher algebra|higher]] [[categorical algebra]], cf. eg. [Lurie (2009) §4.3](QFT+with+defects#Lurie09); [Davydov, Runkel & Kong (2011)](QFT+with+defects#DavydovRunkelKong11); [Fuchs, Schweigert & Valentino (2013)](QFT+with+defects#FuchsSchweigertValentino13).


The upshot is that just as groups correctly describe the symmetries of classical mechanics, higher algebra is thought to describe the "generalized global symmetries" of a quantum field theory.

In this sense, the concept may be better understood as **higher quantum symmetries** (even though the name "quantum symmetries" is already used in the Physics literature for a "dual" symmetry that arises after gauging a symmetry, originating in [Vafa 1989](#Vafa89)).


## References

The terminology of *generalized global symmetries* in the above sense is due to:

* {#GaiottoKapustinSeibergWillett14} [[Davide Gaiotto]], [[Anton Kapustin]], [[Nathan Seiberg]], [[Brian Willett]], *Generalized Global Symmetries*  J. High Energ. Phys. **2015** 172 (2015) &lbrack;[arXiv:1412.5148](https://arxiv.org/abs/1412.5148), <a href="https://doi.org/10.1007/JHEP02(2015)172">doi:10.1007/JHEP02(2015)172</a>&rbrack;

A proposal to formalize the concept (purely at the quantum level, with caveats) is in

* {#FMT22} [[Daniel Freed]], [[Gregory Moore]], [[Constantin Teleman]], *Topological symmetry in quantum field theory* (2022) &lbrack;[arXiv:2209.07471](https://arxiv.org/abs/2209.07471)&rbrack;

Other references:

* {#Vafa89} [[Cumrun Vafa]], *Quantum Symmetries of String Vacua* (1989) &lbrack;[doi:10.1142/S0217732389001842](https://doi.org/10.1142/S0217732389001842)&rbrack;


[[!redirects generalized global symmetries]]

[[!redirects generalized symmetry]]
[[!redirects generalized symmetries]]

