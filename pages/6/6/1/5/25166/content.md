

> This entry currently contains mistakes, see the discussion page [here](https://nforum.ncatlab.org/discussion/15838/fundamental-theorem-of-identity-types/?Focus=114709#Comment_114709).

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

There are two different fundamental theorems of [[identity types]], depending on whether identity types are defined with plain identity induction or with based identity induction. 

### With identity induction
 {#WithIdentityInduction}

The **fundamental theorem of identity types** states that given a [[type]] $A$, a [[type family]] $x:A, y:A \vdash B(x, y)$ and a [[dependent function|family of functions]] 

$$
  x \colon A, 
  y \colon A 
  \;\vdash\; 
  f(x, y)
  \,\colon\,
  (x =_A y) 
    \to 
  B(x, y)
$$

the following conditions are equivalent:

1. For each $x:A$ the [[dependent sum type]] of the type family $y:A \vdash B(x, y)$ is a [[contractible type]]. 
$$x:A \vdash \mathrm{ftid}(x):\mathrm{isContr}\left(\sum_{y:A} B(x, y)\right)$$

1. There is a family of [[equivalence in type theory|equivalences]] 
$$x:A, y:A \vdash \mathrm{ftid}(x, y):(x =_A y) \simeq B(x, y)$$

1. $B(x, y)$ is an [[identity system]]. 

1. For each $x:A$ and $y:A$, the function $f(x, y)$ is an [[equivalence of types]]
$$x:A, y:A, \vdash \mathrm{ftid}(x, y):\mathrm{isEquiv}(f(x, y))$$

1. $f(x, y)$ is a [[retraction]] 
$$x:A, y:A \vdash \mathrm{ftid}(x, y):B(x, y) \to (x =_A y)$$
$$x:A, y:A, r:B(x, y) \vdash G(x, y):f(x, y, \mathrm{ftid}(x, y, r)) =_{B(x, y)} r$$

1. $R(x, y)$ with the function $f(x, y)$ satisfies the [[universal property]] of the [[unary sum]] of $x =_A y$. 

### With based identity induction

The **fundamental theorem of identity types** states that given a [[type]] $A$, an [[term|element]] $a:A$, a [[type family]] $x:A \vdash B(x)$ and a [[dependent function|family of functions]] 

$$x:A \vdash f(x):(a =_A x) \to B(x)$$

the following conditions are equivalent:

1. The dependent sum type of the type family $x:A \vdash B(x)$ is a [[contractible type]]. 
$$\mathrm{ftid}:\mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$

1. There is a family of equivalences 
$$x:A \vdash \mathrm{ftid}(x):(a =_A x) \simeq B(x)$$

1. $B(x)$ equipped with $f(\mathrm{refl}_A(a)):B(a)$ is an [[identity system]]. 

1. For each $x:A$, the function $f(x)$ is an [[equivalence of types]]
$$x:A \vdash \mathrm{ftid}(x):\mathrm{isEquiv}(f(x))$$

1. For each $x:A$, $f(x)$ is a [[retraction]] 
$$x:A \vdash \mathrm{ftid}(x):B(x) \to (a =_A x)$$
$$x:A, b:B(x) \vdash G(x):f(x, \mathrm{ftid}(x, r)) =_{B(x)} r$$

1. For each $x:A$, $B(x)$ with the function $f(x)$ satisfies the [[universal property]] of the [[unary sum]] of $a =_A x$. 

## Proofs that the conditions are the same

### Proof that conditions 1 and 2 are the same

Suppose the equivalence type used in the second definition is a [[weak equivalence type]]. It is possible to show that definitions 1 and 2 are the same. 

Definition 1 implies definition 2, because both $\sum_{x:A} (a =_A x)$ and $\sum_{x:A} B(x)$ are [[contractible types]], there is a [[weak equivalences of types]] 
$$f'(x):\left(\sum_{x:A} (a =_A x)\right) \simeq \left(\sum_{x:A} B(x)\right)$$

Given any two families $x:A vdash B(x)$ and $x:A \vdash C(x)$, there is an weak equivalence of types
$$\mathrm{tot}:\left(\left(\sum_{x:A} B(x)\right) \simeq \left(\sum_{x:A} C(x)\right)\right) \simeq \left(\prod_{x:A} B(x) \simeq C(x)\right)$$

Thus, there is a family of weak equivalences of types
$$x:A \vdash \mathrm{tot}(f'(x)):\prod_{x:A} (a =_A x) \simeq B(x)$$
and we define $\mathrm{ftid}'(x) \coloneqq \mathrm{tot}(f(x))(y)$. 

Definition 2 implies definition 1, as we begin with a family of weak equivalences 
$$x:A \vdash \mathrm{ftid}(x):(a =_A x) \simeq B(x)$$

or equivalently

$$\mathrm{ftid}:\prod_{x:A} (a =_A x) \simeq B(x)$$

We can get a weak equivalences
$$f':\left(\sum_{x:A} (a =_A x)\right) \simeq \left(\sum_{x:A} B(x)\right)$$
by defining 
$$f' \coloneqq \mathrm{tot}^{-1}(\mathrm{ftid})$$

The type $\sum_{x:A} (a =_A x)$ is always contractible; this means the type $\sum_{x:A} B(x)$ is contractible as well, since the two types are equivalent to each other. Thus, one could construct a witnesses
$$\mathrm{ftid}':\mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$

### Proof that conditions 2 and 4 are the same

Suppose the equivalence type used in the second definition is a [[weak equivalence type]]. Then definitions 2 and 3 are the same because given any type $A$ and $B$, there is a equivalence

$$\delta_\simeq(A, B):(A \simeq B) \simeq \prod_{f:A \to B} \mathrm{isEquiv}(f)$$

Thus, in one direction, we define 
$$\mathrm{ftid}'(x) \coloneqq \delta_\simeq(a =_A x, B(x))^{-1}(f(x))$$

and in the other direction, we inductively define $\mathrm{ftid}'(x)$ by induction on reflexivity

$$\mathrm{ftid}'(a, \mathrm{refl}_A(a)) \coloneqq \delta_\simeq(a =_A a, B(a))(\mathrm{ftid}(a))(\mathrm{refl}_A(a))$$

### Proof that condition 4 implies condition 5

Suppose that for every $x:A$ we have a witness that the function $f(x)$ is an [[equivalence of types]]
$$x:A, \vdash \mathrm{ftid}(x, y):\mathrm{isEquiv}(f(x, x))$$

For every type $A$ and $B$, there is a family of functions 
$$f:A \to B \vdash \mathrm{isEquivtoQInv}(f):\mathrm{isEquiv}(f) \to \mathrm{QInv}(f)$$

which takes a witness that $f$ is an equivalence to a [[quasi-inverse function]] of $f$. The [[retraction]] of $f(x)$ is represented by 
$$\mathrm{isEquivtoQInv}(f(x))$$

### Proof that condition 5 implies condition 1

This proof is adapted from [[Dan Licata]] in [Licata 16](#Licata16): 

Suppose that for every $x:A$ we have a function 
$$\mathrm{ftid}(x):B(x) \to (a =_A x)$$ 
and a family of homotopies 
$$G(x):f(x)(\mathrm{ftid}(x)(r) =_{B(x)} r$$ 
This exhibits $B(x)$ as a [[retract]] of $a =_A x$, hence $\sum_{x:A} B(x)$ as a [[retract]] of the [[contractible type]] $\sum_{x:A} a =_A x$, so there is an element
$$\mathrm{ftid}:\mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$

## See also

* [[identity type]]

* [[identity system]]

* [[univalent reflexive graph]]

* [[univalent universe]]

## References

The fundamental theorem of identity types appears in section 11.2 of 

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

Definition 5 arises as a generalization of this proof by [[Dan Licata]] for [[univalent universes]]:

* [[Dan Licata]], *weak univalence with "beta" implies full univalence* ([web](https://groups.google.com/forum/#!msg/homotopytypetheory/j2KBIvDw53s/YTDK4D0NFQAJ)) 