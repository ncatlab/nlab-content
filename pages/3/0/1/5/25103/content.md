
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 
 {#Idea}

By a *stucture identity principle* one means a statement of the form that all "identifications" of [[mathematical structures]] of a given [[type]] are necessarily *structure respecting* identifications (see also *[[structuralism]]*).

The source of the exact term "structure identity principle" seems to be [Aczel (2011, slide 7)](#Aczel11), but the idea will have occurred earlier (see also the *[[principle of equivalence]]*).

The literature on the subject arguably suffers from absence of global conventions on how to name different notions of "identification" (*identity*, *equality*, *isomorphism*, *equivalence*, ...), which can be confusing when speaking about a principle that is all about the fine-print of identifying two nominally different notions of identifications... But the general idea is always the same: Faced with notions of "direct"- and of "structure preserving"-identifications, a structure-identity-principle asserts that they are suitably identical.

Concretely,  [Aczel (2011, p. 9)](#Aczel11) declares that the structure identity principle (SIP) in [[homotopy type theory]] *is* the [[univalence axiom]]: This of course identifies [[terms]] $p \,\colon\, Id_{Type}(A,B)$ of [[identification type]] between [[types]] $A,B \,\colon\, Type$ with [[functions]] that are  [[equivalence in type theory|type-theoretic equivalences]] $f \,\colon\,  A \stackrel{\sim}{\longrightarrow} B$. 

The latter is what [Aczel (2011, p. 22)](#Aczel11) calls "[[isomorphisms]]". While this matches the usage of the term "[[isomorphism]]" in abstract [[category theory]] to mean "[[invertible morphism]]", to complete the notion of "structure identity" one may want a further argument to verify that such isomorphisms really are invertible [[homomorphisms|*homo*-morphism]] with respect to some given [[mathematical structure]] (such as [group structure](structure#GroupDataStructure) etc.). Such enhancement of Aczel's notion of SIP is considered in [Coquand & Danielsson (2013)](#CoquandDanielsson13) (who do not use the terminology "structure udentity principle") and in [UFP (2013, §9.8)](#UFP13), [Escardó (2019, §3.33.1)](#Escardó19) (who do).


## Examples
 {#Examples}

To make this more concrete and more manifest, we may notice that:

1. at least a large class of kinds of [[mathematical structures]] on a base type $B \,\colon\, Type$ are expressible as nothing but "[[telescope type|telescopes]]" of [[dependent pairs]] of $B$ with an iteration of further [[dependent pair]]- and [[dependent function]]- and [[identification types]] (for examples, such as [[group object|group structure]], see [here](structure#InDependentTypeTheory));

1. the [[univalence axiom]] implies extensionality principles for all three of these [[type formations]] (so with regards to [UFP13](#UFP13) this is now using §2, instead), namely [[dependent function|dependent]] [[function extensionality]] ([here](function+extensionality#InTypeTheory)) and its analog for dependent pairs ([here](dependent+sum+type#ExtensionalityPrinciple)):

\[
  \label{ExtensionalityPrinciples}
\]

<img src="/nlab/files/DependentPairExtensionality-230121.jpg" width="660">

<img src="/nlab/files/DependentFunctionExtensionality-230121.jpg" width="660">


Together this means exactly that 

* identifications of two structured types which both are iterated dependent function-, dependent pair- and identity-types of the same form 

* are equivalent to giving the corresponding dependent function- and dependent pairing of componenwise identifications... 

  ...and this is just what one wants to mean by "preserving" this structure as in the notion of *[[homomorphisms]]*.

\linebreak

For example, with the type of [[group object|group structures]] defined as 

<img src="/nlab/files/GroupDataType-230121.jpg" width="710">

then the above extensionality principles (eq:ExtensionalityPrinciples) imply that the [[type of identifications]] of groups is equivalently that of [[bijections]] of the underlying types and equipped with the [[group homomorphism]]-property:

<img src="/nlab/files/GroupDataTypeIdentification-230121.jpg" width="760">



## Related concepts


* [[principle of equivalence]]

* [[structure]]

* [[structuralism]]

* [[homotopy type theory]]

* The idea of building the structure identity principle right into the [[inference rules]] for identifications in a [[type theory]] leads to the notion of ([[higher observational type theory|higher]]) [[observational type theory]].



## References
  
* {#Aczel11} [[Peter Aczel]], *On Voevodsky’s Univalence Axiom*, talk at  Third European Set Theory Conference (2011) &lbrack;[pdf](http://www.cs.man.ac.uk/~petera/Recent-Slides/Edinburgh-2011-slides_pap.pdf), [[Aczel-Univalence.pdf:file]]&rbrack; 

* {#CoquandDanielsson13} [[Thierry Coquand]], [[Nils Anders Danielsson]], *Isomorphism is equality*, Indagationes Mathematicae **24** 4 (2013) 1105-1120 &lbrack;[doi:10.1016/j.indag.2013.09.002](https://doi.org/10.1016/j.indag.2013.09.002)&rbrack;

* {#UFP13} [[Univalent Foundations Project]], §9.8 but also §2 of: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Escardó19} [[Martín Escardó]], *[A structure identity principle for a standard notion of structure](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#sns)*, §3.33.1 in: *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580),  [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html)&rbrack;

  > (formalized in the [[Agda]] [[proof assistant]])


* [[Benedikt Ahrens]], [[Paige Randall North]], [[Michael Shulman]], [[Dimitris Tsementzis]], *A Higher Structure Identity Principle*, LICS '20 (2020) 53–66 &lbrack;[arXiv:2004.06572](https://arxiv.org/abs/2004.06572), [doi:10.1145/3373718.3394755](https://doi.org/10.1145/3373718.3394755)&rbrack;

* [[Benedikt Ahrens]], [[Paige Randall North]], *Univalent foundations and the equivalence principle*, in: *[[Reflections on the Foundations of Mathematics]]*, Synthese Library **407** Springer (2019)  &lbrack;[arXiv:2202.01892](https://arxiv.org/abs/2202.01892), [doi:10.1007/978-3-030-15655-8](https://doi.org/10.1007/978-3-030-15655-8)&rbrack;

Discussion in the context of the [[philosophy]] of [[structuralism]]:

* [[Dimitris Tsementzis]], §5.1 in: *Univalent foundations as structuralist foundations*, Synthese **194** 9 (2017) 3583–3617 &lbrack;[jstor:26748765](https://www.jstor.org/stable/26748765), [doi:10.1007/s11229-016-1109-x](https://doi.org/10.1007/s11229-016-1109-x), [pdf](https://core.ac.uk/download/pdf/157866891.pdf)&rbrack;


[[!redirects structure identity principle]]
[[!redirects structure identity principles]]
