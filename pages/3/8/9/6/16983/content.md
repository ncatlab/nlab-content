

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



# Taboos
* table of contents
{: toc}

## Idea

A **taboo**, for a particular flavor of mathematics or formal system, is a simple statement that is known to be not provable therein, and that can therefore be used to establish the unprovability of other statements without the need to descend into metamathematical considerations (such as syntactic analysis or construction of countermodels) or, in some cases, even to decide on a particular formal system to be working in.

For example, the [[law of excluded middle]] (LEM) is a taboo for [[constructive mathematics]].  Therefore, if some statement $P$ implies LEM, then one can be sure that $P$ is also not provable in constructive mathematics.

## Examples

### Constructive taboos

These taboos are unprovable in [[constructive mathematics]].

* [[law of excluded middle]]
* [[principle of omniscience]]
* [[axiom of choice]].

### Homotopical taboos

These taboos are unprovable in [[homotopy type theory]], even if we assume constructive taboos such as LEM and AC.

* [[uniqueness of identity proofs]]

### Constructive-homotopical taboos

These taboos are unprovable in constructive homotopy type theory, but they may be provable if we assume a constructive taboo *or* a homotopical taboo.

* [[sets cover]]

## Related entries

* [[constructive set theory]]

## References
 {#References}

* [[Peter Aczel]], slide 8 of: *Constructive Set Theory*, 2008 ([pdf](http://www.cs.man.ac.uk/~petera/mathlogaps-slides.pdf))

> A mathematical taboo is a statement that we may not want
to assume false, but we definitely do not want to be able to prove.


* {#AczelRathjen01} [[Peter Aczel]], [[Michael Rathjen]], Section 2.3 of: _Notes on Constructive Set theory_, 2001 ([pdf](https://events.math.unipd.it/3wftop/pdf/AczelRathjen.pdf), [[AczelRathjenCST.pdf:file]])


> Certain basic principles of classical mathematics are taboo for the constructive mathematician. Bishop called them *principles of omniscience*.


See also:

* [[Michael J. Beeson]], Footnote 3, p. 6 (27 of 484) in: *Foundations of Constructive Mathematics*,  Ergebnisse der Mathematik und ihrer Grenzgebiete **3** 6, Springer 1985 ([doi:10.1007/978-3-642-68952-9](https://link.springer.com/book/10.1007/978-3-642-68952-9), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-642-68952-9.pdf))

> Peter Aczel has introduced the word *taboo* in this context. The  decidability of equality on the  reals is taboo in the sense that any proposition which has been shown to imply it will be regarded as essentially  non-constructive. When we refute a proposition, we show that it implies a 
contradiction, an absurdity. If instead we show that it implies the decidability of equality on the reals, we have shown its essential non-constructivity, but in a weaker way than by actually refuting it. In other  words, $0 = 1$ is the most taboo of all taboos. There are several other  common taboos besides the decidability of equality, which we shall soon  encounter.

* [[Hannes Diener]], Section 0.3 and 0.4 of: *Constructive Reverse Mathematics*, 2018 ([arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306))

>  the full axiom of choice is a definite constructive taboo

[[!redirects taboos]]
[[!redirects constructive taboo]]
[[!redirects constructive taboos]]
[[!redirects homotopical taboo]]
[[!redirects homotopical taboos]]
[[!redirects constructive-homotopical taboo]]
[[!redirects constructive-homotopical taboos]]
