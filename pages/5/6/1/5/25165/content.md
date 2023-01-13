
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[dependent type theory]], a *[[reflexive graph]]* is a [[type]] $A$ with a [[type family]] $x:A, y:A \vdash R(x, y)$ and a [[family of functions]] $x:A, y:A \vdash \mathrm{idtofam}(x, y):(x =_A y) \to R(x, y)$. 

Such a [[reflexive graph]] is a **univalent reflexive graph** if the following conditions hold, which are all equivalent by the [[fundamental theorem of identity types]]:

1. For each $x:A$ the type of elements $y:A$ such that $R(x, y)$ is a [[contractible type]]. 
$$x:A \vdash \mathrm{ua}(x):\mathrm{isContr}\left(\sum_{y:A} R(x, y)\right)$$

1. There is a family of equivalences 
$$x:A, y:A \vdash \mathrm{ua}(x, y):(x =_A y) \simeq R(x, y)$$

1. $R(x, y)$ is an [[identity system]]. 

1. For each $x:A$ and $y:A$, the function $\mathrm{idtofam}(x, y)$ is an [[equivalence of types]]
$$x:A, y:A, \vdash \mathrm{ua}(x, y):\mathrm{isEquiv}(\mathrm{idtofam}(x, y))$$

1. $\mathrm{idtofam}(x, y)$ has a [[retraction]] 
$$x:A, y:A \vdash \mathrm{ua}(x, y):R(x, y) \to (x =_A y)$$
$$x:A, y:A, r:R(x, y) \vdash G(x, y):\mathrm{idtofam}(x, y, \mathrm{ua}(x, y, r)) =_{R(x, y)} r$$

1. That $R(x, y)$ with the function $\mathrm{idtofam}(x, y)$ satisfies the [[universal property]] of the [[unary sum]] of $x =_A y$. 

## Examples

There are many examples of univalent reflexive graphs in mathematics. These include [[posets]], [[T0-spaces]], [[metric spaces]], [[univalent categories]], [[univalent groupoids]],  [[univalent dagger categories]], [[univalent bicategories]], [[univalent setoids]], and [[univalent universes]]. 

## See also

* [[reflexive graph]]

* [[fundamental theorem of identity types]]

## References

The definitions and proofs are generalized to general univalent reflexive graphs from the various definitions of univalent universes found in the [[homotopy type theory]] literature:

* [[UF-IAS-2012|Univalent Foundations Project]], p. 4 & Sec. 2.10 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013)  &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082)) 

* [[Dan Licata]], *weak univalence with "beta" implies full univalence* ([web](https://groups.google.com/forum/#!msg/homotopytypetheory/j2KBIvDw53s/YTDK4D0NFQAJ))

[[!redirects univalent reflexive graph]]
[[!redirects univalent reflexive graphs]]