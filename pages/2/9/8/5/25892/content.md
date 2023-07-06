
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[dependent type theory]], a type $A$ is [[decidable]] if it comes with an element of type 
$$\mathrm{isDecidable}(A) \coloneqq A + \neg A$$ 
where $\neg A \coloneqq A \to \emptyset$. 
A [[function]] $f:A \to B$ is **decidable** if for all elements $b:B$ the [[fiber type|fiber]] of $f$ at $b$ is decidable
$$\mathrm{isDecidable}(f) \coloneqq \prod_{b:B} \mathrm{isDecidable}(\mathrm{fiber}(f, b))$$

The type of all decidable functions is represented as $A \to_d B$ and is defined as 

$$A \to_d B \coloneqq \sum_{f:A \to B} \mathrm{isDecidable}(f)$$

## See also

* [[function]]

## References

Decidable maps are defined in proposition 17.6.1 of:

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press (2023) &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&lbrack;

[[!redirects decidable function]]
[[!redirects decidable functions]]
[[!redirects decidable map]]
[[!redirects decidable maps]]

[[!redirects decidable function type]]
[[!redirects decidable function types]]
[[!redirects type of decidable functions]]
[[!redirects types of decidable functions]]