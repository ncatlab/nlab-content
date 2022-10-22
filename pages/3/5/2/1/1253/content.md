
# The axiom of extensionality
* table of contents
{: toc}

## Idea

In material [[set theory]], the _axiom of extensionality_ says that the global membership relation $\in$ is an [[extensional relation]] on the class of all [[pure sets]].

Since any relation becomes extensional on its [[extensional quotient]], one can interpret this axiom as a definition of [[equality]].  However, because the extensional quotient map need not reflect the relation, there is still content to the axiom: if two sets would be identified in the extensional quotient, then they must be members of the same sets and have the same sets as members.

If one models [[pure sets]] in structural [[set theory]], then this property may be made to hold by construction.

## Statements

### Weak extensionality

The **axiom of [[weak extensionality]]** states that given a set $A$ and a set $B$, $A = B$ if and only if for all $C$, $C \in A$ if and only if $C \in B$. 

If the set theory does not have [[equality]] as a primitive, we could define equality as the predicate 

$$A = B \coloneqq \forall C.(C \in A) \iff (C \in B)$$

The axiom of weak extensionality is a foundational axiom in most [[material set theories]], such as Zermelo set theory and Mac Lane set theory, both which do not have the [[axiom of foundation]], as well as [[ZFC]] which does have the [[axiom of foundation]]. 

In [[fully formal ETCS]], where the basic objects of the theory are functions, and $1$ represents the [[singleton]], the [[identity function]] of the singleton, and the sole [[element]] of the singleton all at the same time, weak extensionality is a theorem. The sets are represented by the functions with codomain $1$, $\mathrm{set}(a) \coloneqq (\mathrm{codom}(a) = 1)$ the elements are functions with domain $1$, $\mathrm{element}(a) \coloneqq (\mathrm{dom}(a) = 1)$, and the membership relation $a \in b$ is defined by the function $a$ being an element, the function $b$ being a set, and the codomain of $a$ being $b$
$$a \in b \coloneqq \mathrm{set}(a) \wedge \mathrm{element}(b) \wedge \mathrm{codom}(a) = b$$
By the universal property of the singleton, any two sets $A$ and $B$ with the same domain are equal to each other, which means that any proposition $P$ between $A$ and $B$ implies that $A = B$, and thus that $\forall C.(C \in A) \iff (C \in B)$ implies that $A = B$. The converse follows from [[indiscernibility of identicals]].

### Strong extensionality

Let $\sim$ be a [[bisimulation]], a binary relation such that for all sets $A$ and $B$ such that $A \sim B$, the following conditions hold:

* for all sets $C$ such that $C \in A$, there exists a set $D$ such that $D \in B$ and $C \sim D$
* for all sets $D$ such that $D \in B$, there exists a set $C$ such that $C \in A$ and $C \sim D$

The **axiom of strong extensionality** states that for every bisimulation $\sim$ and for every set $A$ and $B$, $A \sim B$ implies that $A = B$. 

If the set theory does not have [[equality]] as a primitive, we could define equality as the [[terminal]] [[bisimulation]], as the bisimulation $=$ such that for every bisimulation $\sim$ and for every set $A$ and $B$, $A \sim B$ implies that $A = B$.

In any set theory with the [[axiom of foundation]], the axiom of weak extensionality implies the axiom of strong extensionality. 

## See also

* [[extensionality]]

## References

* [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

* [[Håkon Robbestad Gylterud]], [[Elisabeth Bonnevier]], *Non-wellfounded sets in HoTT* ([arXiv:2001.06696](https://arxiv.org/abs/2001.06696))

category: foundational axiom

[[!redirects axiom of extensionality]]
[[!redirects axiom of weak extensionality]]
[[!redirects axiom of strong extensionality]]