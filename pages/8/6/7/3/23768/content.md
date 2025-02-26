

> This entry is about a notion in [[dependent type theory]]. For the notion in [[homotopy theory]] see at *[[mapping telescope]]*.

***


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

In [[dependent type theory]],  by a *telescope type* or just *telescope* (terminology due to [[Nicolaas de Bruijn|de Bruijn]]'s work on *[[Automath]]* in the early 1970s) one means &lbrack;[Zucker (1975, §10.2)](#Zucker75), [de Bruijn (1991)](#deBruijn91)&rbrack; an iterated [[dependent pair]]-[[type]], hence (in the notation [[dependent functions and dependent pairs -- table|here]]) a type of the form 

$$
  \Gamma 
  \;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;
  \big(
    d_1 \colon D_1
  \big)
  \times 
  \big(
    d_2 \colon D_2(d_1)
  \big)
  \times
  \big(
    d_3 \colon D_3(d_1, d_2)
  \big)
  \times
  \cdots
  \times
  \big(
    d_{n+1} \colon D_{n+1}(d_1, \cdots , d_{n})
  \big)
  \;\;\;
  \colon
  \;\;\;
  Type
  \,.
$$

The notion was motivated by and still plays a key role in the formalization of data structures/[[mathematical structures]] in [[dependent type theory|dependently typed]] [[proof assistants]], which typically appear as such *telescope types* (also: "record types", "type classes", cf. [Coen & Tassi (2008, p. 2)](#CoenTassi08), [Garillot, Gonthier, Mahboubi & Rideau (2009, §2.3)](#GarillotGonthierMahboubiRideau09)) starting with an underlying data base type and successively adding access functions and then consistency certificates: see the examples listed [there](structure#InDependentTypeTheory).



## See also

* [[term in context]]

* [[dependent type]]

* [[structure]], [[structure identity principle]]


## References

The notion of telescope types in the sense of iterated [[dependent pairs]] goes back to [[Nicolaas de Bruijn]]'s axiomatization of [[mathematical structures]] via the [[Automath]] [[proof assistant]] in the early 1970s, as such referenced in:

* {#Zucker75} [[Jeffery Zucker]], §10.2 of *Formalization of Classical Mathematics in Automath*, Colloques Internationaux du Centre National de la Recherche Scientifique **249** (1975) 135-145 &lbrack;[web](https://www.win.tue.nl/automath/archive/webversion/aut042/aut042.html), [pdf](https://www.win.tue.nl/automath/archive/pdf/aut042.pdf)&rbrack;

  also in: Studies in Logic and the Foundations of Mathematics **133** (1994) 127-139 &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)70202-7">doi:10.1016/S0049-237X(08)70202-7</a>&rbrack;

> &lbrack;[Zucker (1975, §10.2)](#Zucker1975):&rbrack; Now a general framework in which to view linear orders, or other algebraic  structures, has been proposed by de Bruijn. It uses the notion of “telescope”. &lbrack;...&rbrack; A telescope therefore functions like a “generalized $\sum$”.


and eventually published by de Bruijn in:

* {#deBruijn91} [[Nicolaas de Bruijn]], *Telescopic mappings in typed lambda calculus*, Information and Computation **91** 2 (1991) 189-204 &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90066-B">doi:10.1016/0890-5401(91)90066-B</a>&rbrack;

The notion is used in much of the [[dependent type theory|dependent type theoretic]] [literature](structure#ReferencesInDependentTypeTheory) on formalizing [[mathematical structures]], e.g.:

* {#CoenTassi08} Claudio Sacerdoti Coen, Enrico Tassi, p. 2 of: *Working with Mathematical Structures in Type Theory*, in: *Types for Proofs and Programs. TYPES 2007*, Lecture Notes in Computer Science **4941** Springer (2008) &lbrack;[doi:10.1007/978-3-540-68103-8_11](https://doi.org/10.1007/978-3-540-68103-8_11), [pdf](https://www.cs.unibo.it/~sacerdot/PAPERS/types07.pdf)&rbrack;

* {#GarillotGonthierMahboubiRideau09} François Garillot, [[Georges Gonthier]], Assia Mahboubi, Laurence Rideau, §2.3 in: *Packaging Mathematical Structures*, in: *Theorem Proving in Higher Order Logics. TPHOLs 2009*, Lecture Notes in Computer Science **5674**, Springer (2009) &lbrack;[doi:10.1007/978-3-642-03359-9_23](https://doi.org/10.1007/978-3-642-03359-9_23)&rbrack;

and more widely, often without attribution, for instance in:

* {#Winterhalter20} [[Théo Winterhalter]], p. 100, 111 in: *Formalisation and Meta-Theory of Type Theory*, Nantes (2020) &lbrack;[pdf](https://github.com/TheoWinterhalter/phd-thesis/releases/download/v1.2.1/TheoWinterhalter-PhD-v1.2.1.pdf), [github](https://github.com/TheoWinterhalter/phd-thesis)&rbrack;

* {#Shulman22} [[Mike Shulman]], p. 5-6 in *Towards a Third-Generation HOTT* Part 2 (2022) &lbrack;slides [pdf](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU)&rbrack;

* {#KS23} [[Astra Kolomatskaia]], [[Michael Shulman]], p. 16-18 in *Displayed Type Theory and Semi-Simplicial Types* &lbrack;[arXiv:2311.18781](https://arxiv.org/abs/2311.18781)&rbrack; 

[[!redirects type telescopes]]

[[!redirects telescope]]
[[!redirects telescopes]]

[[!redirects telescope type]]
[[!redirects telescope types]]

