+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

By a _bireflective subcategory_ one may mean a [[subcategory]] $\mathcal{B} \hookrightarrow \mathcal{C}$ which is both [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]] --- i.e. a [[fully faithful functor]] possessing both [[left adjoint|left]] and [[right adjoints]]. 

The [[adjoint pair]] induced from the [[adjoint triple]] given by reflection, inclusion and coreflection of a bireflective subcategory is an [[adjoint modality]]. See there for more.

The terminology "bireflective" was coined in [FOPTST99](#FOPTST99) where --- beware --- it is in addition required that:

1. the left and right adjoints are equal, hence forming an [[ambidextrous adjoint]], 

1. such that the [[adjunction unit]] followed by the [[adjunction counit]] is the [[identity morphism]].


## References

* {#FOPTST99} [[Peter Freyd]], [[Peter O’Hearn]],  [[A. John Power]], [[M. Takeyama]], [[Ross Street]], [[Robert D. Tennent]], *Bireflectivity*, Theoretical Computer Science **228** 1–2 (1999) 49-76 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00354-5">doi:10.1016/S0304-3975(98)00354-5</a>&rbrack;

In a context of [[categorical semantics]] for [[linear homotopy type theory]]:

* [[Mitchell Riley]], [[Eric Finster]], [[Daniel R. Licata]], Section 7.1 in: *Synthetic Spectra via a Monadic and Comonadic Modality* &lbrack;[arXiv:2102.04099](https://arxiv.org/abs/2102.04099)&rbrack;



[[!redirects bireflective subcategories]]


