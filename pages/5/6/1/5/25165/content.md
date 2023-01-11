
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

In [[dependent type theory]], there are multiple notions of [[equivalence types]] in [[dependent type theory]], which can be used for a definition of univalence for a [[reflexive graph]] $(A, R)$; these include

* [[judgmentally strict equivalence types]]
* [[propositionally strict equivalence types]]
* various notions of [[weak equivalence types]]
  * the type of [[functions]] with [[contractible type|contractible]] [[fiber type|fibers]]
  * the type of [[spans]] with contractible fibers
  * the type of [[multivalued partial functions]] which are single-valued and [[total function|total]] and have contractible fibers
  * the type of [[one-to-one correspondences]]
* type of $U$-small equivalences, given a [[type universe]] $U$ and a definition of equivalence above

Now, assuming a notion of equivalence type $\simeq$, a [[reflexive graph]] is a **univalent reflexive graph** if one of the following conditions hold:

1. That for each $x:A$ the type of elements $y:A$ such that $R(x, y)$ is a [[contractible type]]. 
$$x:A \vdash \mathrm{ua}(x):\mathrm{isContr}\left(\sum_{y:A} R(x, y)\right)$$

1. That there is a family of equivalences 
$$x:A, y:A \vdash \mathrm{ua}(x, y):(x =_A y) \simeq R(x, y)$$

1. That $R(x, y)$ is an [[identity system]]. 

1. That for each $x:A$ and $y:A$, the function $\mathrm{idtofam}(x, y)$ is an [[equivalence of types]]
$$x:A, y:A, \vdash \mathrm{ua}(x, y):\mathrm{isEquiv}(\mathrm{idtofam}(x, y))$$

1. That $\mathrm{idtofam}(x, y)$ has a [[retraction]] 
$$x:A, y:A \vdash \mathrm{ua}(x, y):R(x, y) \to (x =_A y)$$
$$x:A, y:A, r:R(x, y) \vdash G(x, y):\mathrm{idtofam}(x, y, \mathrm{ua}(x, y, r)) =_{R(x, y)} r$$

### Proof that definitions 1, 2, and 3 are the same

Suppose the equivalence type used in the second definition is a [[weak equivalence type]]. It is possible to show that definitions 1, 2, and 3 above are the same, as this is just a special case of the [[fundamental theorem of identity types]]:

Definition 1 implies definition 2, because both $\sum_{y:A} (x =_A y)$ and $\sum_{y:A} R(x, y)$ are [[contractible types]], there is a family of [[weak equivalences of types]] 
$$x:A \vdash f'(x):\left(\sum_{y:A} (x =_A y)\right) \simeq \left(\sum_{y:A} R(x, y)\right)$$

Given any two families $x:A vdash B(x)$ and $x:A \vdash C(x)$, there is an weak equivalence of types
$$\mathrm{tot}:\left(\left(\sum_{x:A} B(x)\right) \simeq \left(\sum_{x:A} C(x)\right)\right) \simeq \left(\prod_{x:A} B(x) \simeq C(x)\right)$$

Thus, for univalent reflexive graphs, there is a family of weak equivalences of types
$$x:A \vdash \mathrm{tot}(f'(x)):\prod_{y:A} (x =_A y) \simeq R(x, y)$$
and we define $\mathrm{ua}'(x, y) \coloneqq \mathrm{tot}(f(x))(y)$. 

Definition 2 implies definition 1, as we begin with a family of weak equivalences 
$$x:A, y:A \vdash \mathrm{ua}(x, y):(x =_A y) \simeq R(x, y)$$

or equivalently

$$x:A \vdash \mathrm{ua}(x):\prod_{y:A} (x =_A y) \simeq R(x, y)$$

We can get a family of weak equivalences
$$x:A \vdash f'(x):\left(\sum_{y:A} (x =_A y)\right) \simeq \left(\sum_{y:A} R(x, y)\right)$$
by defining 
$$f'(x) \coloneqq \mathrm{tot}^{-1}(\mathrm{ua}(x))$$

The type $\sum_{y:A} (x =_A y)$ is always contractible; this means the type $\sum_{y:A} R(x, y)$ is contractible as well, since the two types are equivalent to each other. Thus, one could construct an family of witnesses
$$x:A \vdash \mathrm{ua}'(x):\exists!y:A.R(x, y)$$

### Proof that definitions 2 and 4 are the same

Suppose the equivalence type used in the second definition is a [[weak equivalence type]]. Then definitions 2 and 3 are the same because given any type $A$ and $B$, there is a equivalence

$$\delta_\simeq(A, B):(A \simeq B) \simeq \prod_{f:A \to B} \mathrm{isEquiv}(f)$$

Thus, in one direction, we define 
$$\mathrm{ua}'(x, y) \coloneqq \delta_\simeq(x =_A y, R(x, y))^{-1}(\mathrm{idtofam}(x, y))$$

and in the other direction, we inductively define $\mathrm{ua}'(x, y)$ by induction on reflexivity

$$\mathrm{ua}'(x, x, \mathrm{refl}_A(x)) \coloneqq \delta_\simeq(x =_A x, R(x, x))(\mathrm{ua}(x, x))(\mathrm{refl}_A(x))$$

### Proof that definition 4 implies definition 5

Suppose that for every $x:A$ and $y:A$ we have a witness that the function $\mathrm{idtofam}(x, y)$ is an [[equivalence of types]]
$$x:A, y:A, \vdash \mathrm{ua}(x, y):\mathrm{isEquiv}(\mathrm{idtofam}(x, y))$$

For every type $A$ and $B$, there is a family of functions 
$$f:A \to B \vdash \mathrm{isEquivtoQInv}(f):\mathrm{isEquiv}(f) \to \mathrm{QInv}(f)$$

which takes a witness that $f$ is an equivalence to a [[quasi-inverse function]] of $f$. The [[retraction]] of $\mathrm{idtofam}(x, y)$ is represented by 
$$\mathrm{isEquivtoQInv}(\mathrm{idtofam}(x, y))$$

### Proof that definition 5 implies definition 1

This proof is adapted from [[Dan Licata]] in [Licata 16](#Licata16): 

Suppose that for every $x:A$ and $y:A$ we have a function 
$$\mathrm{ua}(x, y):R(x, y) \to (x =_A y)$$ 
and a family of homotopies 
$$G(x, y):\mathrm{idtofam}(x, y)(\mathrm{ua}(x, y)(r) =_{R(x, y)} r$$ 
This exhibits $R(x, y)$ as a [[retract]] of $x =_A y$, hence $\sum_{y:A} R(x, y)$ as a [[retract]] of the [[contractible type]] $\sum_{y:A} x =_A y$, so there is a family of elements
$$x:A \vdash \mathrm{ua}'(x):\mathrm{isContr}\left(\sum_{y:A} R(x, y)\right)$$

## Examples

There are many examples of univalent reflexive graphs in mathematics. These include [[posets]], [[T0-spaces]], [[metric spaces]], [[univalent categories]], [[univalent groupoids]],  [[univalent dagger categories]], [[univalent bicategories]], [[univalent setoids]], and [[univalent universes]]. 

## See also

* [[reflexive graph]]

## References

The definitions and proofs are generalized to general univalent reflexive graphs from the various definitions of univalent universes found in the [[homotopy type theory]] literature:

* [[UF-IAS-2012|Univalent Foundations Project]], p. 4 & Sec. 2.10 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013)  &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082)) 

* [[Dan Licata]], *weak univalence with "beta" implies full univalence* ([web](https://groups.google.com/forum/#!msg/homotopytypetheory/j2KBIvDw53s/YTDK4D0NFQAJ))

[[!redirects univalent reflexive graph]]
[[!redirects univalent reflexive graphs]]