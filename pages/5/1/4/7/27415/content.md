
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

Two [[propositions]] $P$ and $Q$ are said to be **mutually exclusive** if $\neg (P \wedge Q)$ holds. 

By [[currying]], both $P \Rightarrow \neg Q$ and $Q \Rightarrow \neg P$ hold. As a result, in the [[antithesis interpretation]] of [[intuitionistic logic]], $P$ is *a* [[negation]] of $Q$ and $Q$ is *a* negation of $P$. In addition, $P$ is **affirmative** and $Q$ is **refutative** if the [[implication]] $Q \Rightarrow \neg P$ is a [[logical equivalence]] $Q \iff \neg P$; i.e. $Q$ is the Heyting negation of $P$. Conversely, $P$ is **refutative** and $Q$ is **affirmative** if the [[implication]] $P \Rightarrow \neg Q$ is a [[logical equivalence]] $P \iff \neg Q$; i.e. $P$ is the Heyting negation of $Q$. $P$ and $Q$ are both **[[stable proposition|stable]]** if they are both affirmative and refutative. $P$ and $Q$ are **[[decidable propositions|decidable]]** if $P \vee Q$ holds. 

In [[dependent type theory]] under the [[propositions as types]] interpretation, two [[types]] $P$ and $Q$ are **mutually exclusive** if there is an element $p:(P \times Q) \to \emptyset$ of the [[function type]] from the [[product type]] $P \times Q$ to the [[empty type]] $\emptyset$. 

## Related concepts

* [[type of mutually exclusive propositions]]

* [[antithesis interpretation]]

## References

* Wikipedia, *[Mutual exclusivity](https://en.wikipedia.org/wiki/Mutual_exclusivity)*

[[!redirects mutual exclusivity]]
[[!redirects mutual exclusion]]

[[!redirects mutually exclusive]]

[[!redirects mutually exclusive propositions]]