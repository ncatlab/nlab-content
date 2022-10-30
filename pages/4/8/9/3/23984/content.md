> This page is about the notion in [[homotopy type theory|homotopy]] [[type theory]]. For *[[parallel transport]]* via [[connections]] in [[differential geometry]] see there. For the relation see [below](#RelationToParallelTransport).

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea ##
 {#Idea}

[[Gottfried Leibniz]] said (in translation from [Lewis 1918, p. 373](#Lewis18) with original Latin terms in parenthesis; see also [Cartwright 1971, p. 119](#Cartwright71) and [Gries & Schneider 1998](#GriesSchneider98))

> Two terms are the same (eadem) if one can be substituted for the otherwithout altering the truth of any statement (salva veritate). If we have $P$ and $Q$, and $P$ enters into some true proposition, and the substitution of $Q$ for $P$ wherever it appears results in a new proposition that is likewise true, and if this can be done for every proposition, then $P$ and $Q$ are said to be the same; conversely, if $P$ and $Q$ are the same, they can be substituted for one another.

The converse mentioned at the end of the last sentence is known as the **principle of substitution** or the **indiscernibility of identicals**. In any simply typed first-order theory, this principle is formalized as 

$$x =_T y \implies \forall \; \mathrm{properties} \; P. P(x) \iff P(y)$$

In the interpretation of [[propositions as types]] in [[type theory]], propositions are interpreted as types, and the above statement has a generalization from the types which are propositions to all types: the [[universal quantifier]] becomes a [[dependent product type]], the [[predicate]] becomes a [[type family]], [[implication]] becomes a [[function]], and [[logical equivalence]] of [[propositions]] becomes [[equivalence in homotopy type theory|equivalence of types]]. This results in what is known as *transport* in type theory, the function 

$$\mathrm{transport}(x, y): x =_T y \to \prod_{P:T \to \mathcal{U}} P(x) \simeq P(y)$$

## Definitions

### Martin-Löf type theory

In [[Martin-Löf type theory]], given 

* a [[type]] $A$, 

* a [[judgment]] $z \colon A \vdash B(z)\ \mathrm{type}$ (hence an $A$-[[dependent type]] $B$), 

* [[terms]]$\,$ $x \colon A$ and $y \colon A$, 

* an [[term]] of their [[identity type]] $p \colon (x =_A y)$, 

then there are compatible **transport functions** 

\[
  \label{TheTransportFunctions}
  \overrightarrow{\mathrm{tr}}_{B}^{p}
  \,\colon\, 
  B(x) \longrightarrow B(y) 
  \;\;\;
  \text{and}
  \;\;\;
  \overleftarrow{\mathrm{tr}}_{B}^{p}
  \,\colon\, B(y) \longrightarrow B(x)
  \,,
\] 

such that for all $v:B(y)$, the ([[homotopy fiber|homotopy]]) [[fiber]] of $\overrightarrow{\mathrm{tr}}_{B}^{p}$ at $v$ is [[contractible]], and for all $u:B(x)$, the [[fiber]] of $\overleftarrow{\mathrm{tr}}_{B}^{p}$ at $u$ is [[contractible]]. 

### Cubical type theory

...

### Higher observational type theory

...

## Examples and applications

\begin{remark}\label{RelationToParallelTransport}
**(relation to parallel transport -- [[schreiber:differential cohomology in a cohesive topos|dcct §3.8.5]], [ScSh12 §3.1.2](cohesive+homotopy+type+theory#SchreiberShulman2012))**
\linebreak
  In [[cohesive homotopy type theory]] the [[shape modality]] $\esh$ has the [[shape via cohesive path ∞-groupoid|interpretation]] of turning any cohesive type $X$ into its [[path infinity-groupoid|path $\infty$-groupoid]] $\esh X$: The [[1-morphisms]] $p \colon (x =_{\esh X} y)$ of $\esh X$ have the [[shape via cohesive path ∞-groupoid|interpretation]] of being (whatever identities existed in $X$ composed with) cohesive (e.g. [[continuous function|continuous]] or [[smooth function|smooth]]) *[[paths]]* in $X$, and similarly for the higher order paths-of-paths.

Accordingly, an [[shape modality|$\esh X$]]-[[dependent type]] $B$ has the interpretation of being a "[[local system]]" of $B$-[[coefficients]] over $X$, namely a $B(x)$-[[fiber infinity-bundle|fiber $\infty$-bundle]] equipped with a [[flat infinity-connection|flat $\infty$-connection]]. 

In this case, the identity transport (eq:TheTransportFunctions) along paths in [[shape modality|$\esh X$]] has the interpretation of being the *[[parallel transport]]* (in the original sense of [[differential geometry]]) with respect to this [[flat infinity-connection|flat $\infty$-connection]] (and the [[higher parallel transport]] when applied to paths-of-paths).
\end{remark}

## See also ##

* [[identity type]]

* [[dependent identity type]]

* [[identity of indiscernibles]]

## References ##

* [[Univalent Foundations Project|UVP]], [§2.3 "Type families and fibrations"](https://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf#page=81) in: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

Some more details are spelled out in:

* [[Egbert Rijke]], pp. 18 in: *Homotopy Type Theory* (2012) &lbrack;[pdf](https://studenttheses.uu.nl/bitstream/handle/20.500.12932/11704/hott.pdf?sequence=1)&rbrack;

Implementation in [[Agda]]:

* [[Martín Hötzel Escardó]], *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580), [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/)&rbrack;

Leibniz's original paragraph (from an unpublished manuscript probably written after 1683) is reproduced in the Latin Original in

* {#Gerhard1890} K. Gerhard (ed.), Section XIX, [p. 228](https://archive.org/details/diephilosophisc00gerhgoog/page/228/mode/2up) in: *Die philosophischen Schriften von Gottfried Wilhelm Leibniz*, Siebenter Band, Weidmannsche Buchhandlung (1890) &lbrack;[archive.org](https://archive.org/details/diephilosophisc00gerhgoog/page/n7/mode/2up)&rbrack;

and in English translation in:

* {#Lewis18} [[Clarence I. Lewis]], Appendix (p. 373) of: *A Survey of Symbolic Logic*, University of California (1918) &lbrack;[[LewisAppendix-LeibnizIndiscernibles.pdf:file]]&rbrack;

and further discussed in:

* {#Cartwright71} [[Richard Cartwright]], *Identity and Substitutivity*, p. 119-133 of: Milton Munitz (ed.) *Identity and Individuation*, New York University Press (1971) &lbrack;[[Cartwright-IdentityAndSubstitutivity.pdf:file]]&rbrack;

* {#GriesSchneider98} David Gries, Fred Schneider, *Formalizations Of Substitution Of Equals For Equals* (1998) &lbrack;[pdf](https://ecommons.cornell.edu/bitstream/handle/1813/7340/98-1686.pdf?sequence=1&isAllowed=y), [ecommons:1813/7340](https://ecommons.cornell.edu/handle/1813/7340)

The understanding of transport in HoTT as expressing [[Leibniz]]'s principle of "[[indiscernibility of identicals]]" (aka "substitution of equals", "substitutivity") has been made explicit in:

* {#LadymanPresnell15} [[James Ladyman]], [[Stuart Presnell]], §6.3 in: *Identity in Homotopy Type Theory, Part I: The Justification of Path Induction*, Philosophia Mathematica **23** 3 (2015) 386–406 &lbrack;[doi:10.1093/philmat/nkv014](https://doi.org/10.1093/philmat/nkv014), [pdf](http://philsci-archive.pitt.edu/11079/1/Identity_in_HTT_public.pdf)&rbrack;

* [[Benedikt Ahrens]], [[Paige Randall North]], §3.1 in: *Univalent foundations and the equivalence principle*, in: *Reflections on the Foundations of Mathematics*, Synthese Library **407** Springer (2019)  &lbrack;[arXiv:2202.01892](https://arxiv.org/abs/2202.01892), [doi:10.1007/978-3-030-15655-8](https://doi.org/10.1007/978-3-030-15655-8)&rbrack;

The converse implication of [[path induction]] from transport (together with the uniqueness principle for id-types) is made explicit in:

* [Ladyman & Presnell 2015, §6.3](#LadymanPresnell15)

* Lennard Götz, §4.2 of: *Martin-Löf's J-rule*, LMU (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Goetz.pdf)&rbrack; 

[[!redirects transports]]
[[!redirects transporting]]

[[!redirects identity transport]]
[[!redirects identity transports]]

[[!redirects type transport]]
[[!redirects type transports]]

[[!redirects indiscernibility of identicals]]

[[!redirects principle of substitutivity]]
[[!redirects principle of substitution]]
[[!redirects principle of substitution of equals for equals]]
[[!redirects principle of substituting equals for equals]]