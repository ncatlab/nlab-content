
# The axiom of extensionality
* table of contents
{: toc}

## Idea

In material [[set theory]], the _axiom of extensionality_ says that the global membership relation $\in$ is an [[extensional relation]] on the class of all [[pure sets]].

Since any relation becomes extensional on its [[extensional quotient]], one can interpret this axiom as a definition of [[equality]].  However, because the extensional quotient map need not reflect the relation, there is still content to the axiom: if two sets would be identified in the extensional quotient, then they must be members of the same sets and have the same sets as members.

If one models [[pure sets]] in structural [[set theory]], then this property may be made to hold by construction.

## Statements

### Weak extensionality

#### In unsorted set theories

In any [[unsorted set theory]], the **axiom of [[weak extensionality]]** states that given a set $A$ and a set $B$, $A = B$ if and only if for all $C$, $C \in A$ if and only if $C \in B$. 

If the set theory does not have [[equality]] as a primitive, we could define equality as the predicate 

$$A = B \coloneqq \forall C.(C \in A) \iff (C \in B)$$

The axiom of weak extensionality is a foundational axiom in most [[material set theories]], such as Zermelo set theory and Mac Lane set theory, both which do not have the [[axiom of foundation]], as well as [[ZFC]] which does have the [[axiom of foundation]]. 

In [[fully formal ETCS]], where the basic objects of the theory are functions, $0$ represents both the [[empty set]] and the [[identity function]] on the empty set, and $1$ represents the [[singleton]], the [[identity function]] of the singleton, and the sole [[element]] of the singleton all at the same time, there are three possible notions of sets:

* as [[identity functions]] $\mathrm{set}(a) \coloneqq \mathrm{dom}(a) = a$ or $\mathrm{set}(a) \coloneqq \mathrm{codom}(a) = a$

* as [[functions]] into the [[singleton]] $\mathrm{set}(a) \coloneqq (\mathrm{codom}(a) = 1)$

* as functions from the [[empty set]] $\mathrm{set}(a) \coloneqq (\mathrm{dom}(a) = 0)$

The elements are functions with domain $1$, $\mathrm{element}(a) \coloneqq (\mathrm{dom}(a) = 1)$

When sets are defined as functions into the singleton, the membership relation $a \in b$ is defined by the function $a$ being an element, the function $b$ being a set, and the codomain of $a$ being $b$
$$a \in b \coloneqq \mathrm{set}(a) \wedge \mathrm{element}(b) \wedge \mathrm{codom}(a) = b$$

Weak extensionality is a theorem in this case. By the universal property of the singleton, any two sets $A$ and $B$ with the same domain are equal to each other, which means that any proposition $P$ between $A$ and $B$ implies that $A = B$, and thus that $\forall C.(C \in A) \iff (C \in B)$ implies that $A = B$. The converse follows from [[indiscernibility of identicals]].

#### In two-sorted set theories

In any [[two-sorted set theory]], the **axiom of [[weak extensionality]]** states that given a set $A:Set$ and a set $B:Set$, $A =_{Set} B$ if and only if for all $a:Element$, $a \in A$ if and only if $a \in B$. 

If the set theory does not have [[equality]] of sets as a primitive, we could define equality of sets as the predicate 

$$A =_{Set} B \coloneqq \forall a:Element.(a \in A) \iff (a \in B)$$

### Material strong extensionality

Let $\sim$ be a [[bisimulation]], a binary relation such that for all sets $A$ and $B$ such that $A \sim B$, the following conditions hold:

* for all sets $C$ such that $C \in A$, there exists a set $D$ such that $D \in B$ and $C \sim D$
* for all sets $D$ such that $D \in B$, there exists a set $C$ such that $C \in A$ and $C \sim D$

The **axiom of strong extensionality** states that for every bisimulation $\sim$ and for every set $A$ and $B$, $A \sim B$ implies that $A = B$. 

If the set theory does not have [[equality]] as a primitive, we could define equality as the [[terminal]] [[bisimulation]], as the bisimulation $=$ such that for every bisimulation $\sim$ and for every set $A$ and $B$, $A \sim B$ implies that $A = B$.

In any set theory with the [[axiom of foundation]], the axiom of weak extensionality implies the axiom of strong extensionality. 

### Structural strong extensionality

In any [[structural set theory]], the axiom of strong extensionality states that for all sets $A$ and $B$ with an [[injection]] $i:A \hookrightarrow B$, the two definitions of $i$ being a [[bijection]] are logically equivalent to each other: 

* there exists a function $i^{-1}:B \to A$ such that for all elements $a \in A$ and $b \in B$, $i^{-1}(i(a)) = a$ and $i(i^{-1}(b)) = b$ 
* for every element $x \in B$ there exists an element $y \in A$ such that $i(y) = x$. 

Similar to how in material set theory one can use the axiom of extensionality to define [[equality]] of sets, in structural set theory one can use the axiom of strong extensionality to define [[bijection]] of sets. 

## In dependent type theory

In [[dependent type theory]], it is possible to define a [[Tarski universe]] $(V, \in)$ of [[pure sets]] which behaves as a [[material set theory]]. The universal type family of the Tarski universe is given by the type family $x:V \vdash \sum_{y:V} y \in x$. The **axiom of extensionality** is given by the following [[inference rule]]:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{extensionality}_V:\prod_{x:V} \prod_{y:V} (x =_V y) \simeq \prod_{z:V} (z \in x) \simeq (z \in y)}$$

### Power sets

For [[power sets]], the *[[axiom of extensionality]]* is a property of [[power sets]], and states that given a [[type]] $A$ and [[subtypes]] $B:\mathcal{P}(A)$ and $C:\mathcal{P}(A)$, there is an [[equivalence of types]] between the [[identity type]] $B =_{\mathcal{P}(A)} C$ and the [[dependent function type]] $\prod_{x:A} (x \in_A B) \simeq (x \in_A C)$, where $(\Omega, \mathrm{El}_\Omega)$ is the [[type of all propositions]] and $x \in_A B \coloneqq \mathrm{El}_\Omega(B(x))$ is the local membership relation between elements $x:A$ and subtypes $B:\mathcal{P}(A)$. The axiom of extensionality holds in the [[dependent type theory]] if and only if [[function extensionality]] holds. 

## See also

* [[extensionality]]
* [[identity of indiscernibles]]

## References

* [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

* [[Håkon Robbestad Gylterud]], [[Elisabeth Stenholm]], [[Niccolò Veltri]], *Terminal Coalgebras and Non-wellfounded Sets in Homotopy Type Theory* &lbrack;[arXiv:2001.06696](https://arxiv.org/abs/2001.06696)&rbrack;

category: foundational axiom, logic

[[!redirects Axiom of extensionality]]

[[!redirects axiom of extensionality]]
[[!redirects axiom of weak extensionality]]
[[!redirects axiom of strong extensionality]]