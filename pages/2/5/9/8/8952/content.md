
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

What is called _observational type theory_ (OTT) is a flavor of [[type theory]] in between [[extensional type theory]] and [[intensional type theory]].

This may be regarded as a first-stage approximation to 
[[homotopy type theory]] (HoTT, and for more motivation see at *[[higher observational type theory]]*): 

The [[propositions]] of OTT correspond to the [[h-propositions]] of HoTT, and the [[types]] in OTT correspond to [[h-sets]] in HoTT.  The notion of [[equality]] on OTT is based on [[symmetric prosets]], which is a special case of [[internal category in an (infinity,1)-category|higher internal groupoids]].  Since equality is defined type-by-type, OTT enjoys [[function extensionality]], and a form of [[propositional extensionality]] at least for a specified universe of propositions (not necessarily including all [[h-propositions]]).

There are a few technical differences (e.g. proofs of propositions are [[definitional equality|definitionally equal]] in OTT, whereas proofs of hprops are only [[propositional equality|propositionally equal]] in HoTT) but on the whole HoTT looks a lot like a [[higher homotopy]] version of OTT.

## See also

* [[higher observational type theory]]

* [[structure identity principle]]

## References


Observational type theory was introduced in:

* [[Thorsten Altenkirch]], [[Conor McBride]], _Towards observational type theory_, draft (2006) &lbrack;[pdf](http://strictlypositive.org/ott.pdf), [pdf](https://www.cs.nott.ac.uk/~psztxa/publ/ott-conf.pdf), [[AltenkirchMcBrided-TowardsOTT.pdf:file]]&rbrack;

* {#AltenkirchMcBrideSwierstra07} [[Thorsten Altenkirch]], [[Conor McBride]], [[Wouter Swierstra]], *Observational Equality, Now!*, PLPV '07: Proceedings of the 2007 workshop on Programming languages meets program verification (2007) 57-68 &lbrack;ISBN:978-1-59593-677-6, [doi:10.1145/1292597.1292608](http://doi.org/10.1145/1292597.1292608), [pdf](https://www.cs.nott.ac.uk/~psztxa/publ/obseqnow.pdf)&rbrack;

A blog post about an [[Agda]] implementation, including [[propositional extensionality]] (which is not mentioned in [ABS07](#AltenkirchMcBrideSwierstra07)):

* [[Conor McBride]], [Hier Soir, an OTT Hierarchy](http://mazzo.li/epilogue/index.html%3Fp=1098.html)

The above comparison between OTT and HoTT is taken from 

* [[Dan Licata]], _[comment](http://homotopytypetheory.org/2012/11/12/abstract-types-with-isomorphic-types/#comment-2476)_ (2012)


[[!redirects observational type theory]]
[[!redirects observational type theories]]
[[!redirects OTT]]
