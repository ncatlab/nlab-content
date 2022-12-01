
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

\tableofcontents

## Idea

The [[proposition]] "2 + 2 = 5" is a statement, usually formuated in the [[natural numbers]], that is false in traditional mathematics, and is usually taken as a statement which is self-evidently false. However, in weak enough [[foundations]], 2 + 2 = 5 cannot be proved to be false, and in fact, there exist models where "2 + 2 = 5" is a true statement in the natural numbers. 

## Independence in weak enough foundations

We work in bare [[Martin-Löf type theory]] with no [[type universes]]; this consists solely of [[dependent product types]], [[dependent sum types]], [[sum types]], [[empty type]], [[unit type]], [[natural numbers type]] and [[identity types]], and we do not assume [[UIP]] or [[axiom K]] in our type theory. This is enough for the [[propositions as types]] interpretation of [[type theory]]. 

We define the symbol $2$ to be [[judgmentally equal]] to $s(s(0))$, and we define the symbol $5$ to be [[judgmentally equal]] to $s(s(s(s(s(0)))))$. Addition is a binary operation $(-)+(-):\mathbb{N} \times \mathbb{N} \to \mathbb{N}$ with identities $n:\mathbb{N} \vdash \mathrm{basecase}(n):0 + n = n$ and $m:\mathbb{N}, n:\mathbb{N} \vdash \mathrm{indcase}(m, n):s(m) + n = s(m + n)$. When we say that 2 + 2 = 5 is true, we mean that the aforementioned identity type is a [[pointed type]], and when we say that 2 + 2 = 5 is false, we mean that the function type from said identity type to the empty type is a pointed type. 

There exists a model of [[Martin-Löf type theory]] where 2 + 2 = 5 is false in the natural numbers: we include a [[univalent universe]] which is closed under all the types above in our [[Martin-Löf type theory]]. Now suppose that there is an identity $p:2 + 2 =_\mathbb{N} 5$. This means that $\mathbb{N}$ is a [[contractible type]]; however, this contradicts the universe being [[univalent]]. Thus, 2 + 2 = 5 is false. 

There exists a model of [[Martin-Löf type theory]] where 2 + 2 = 5 is true in the natural numbers: we include a (-1)-truncation axiom in the vein of [[propositional logic as a dependent type theory]] which makes every type an [[h-proposition]]. By definition of h-proposition, given any two elements $a:A$ and $b:A$ of a type $A$, there is an identity $p(a, b):a =_A b$. This means there is an identity $p:2 + 2 =_\mathbb{N} 5$. Thus, 2 + 2 = 5 is true. 

Thus, the [[axiom]] "2 + 2 = 5" is independent of our bare [[Martin-Löf type theory]]. This indicates that one could literally take "2 + 2 = 5" as an axiom in our theory. 

## Philosophical consequences

This phenomenon has implications in the [[philosophy of mathematics]]. In particular, in the [[epistemology of mathematics]], this gives credence to epistemic relativism, which states that what may be true in one person's conception of mathematics may be false in another person's conception of mathematics, and may be unprovable or independent in a third person's conception of mathematics. If we take "conception of mathematics" to be formally encoded in some [[foundations of mathematics]], the above example indicates that different foundations lead to different validities for "2 + 2 = 5", resulting in epistemic relativism. This contradicts the conventional belief that the falsehood of "2 + 2 = 5" is self-evident (see [Chambers 1728](#Chambers1728)), as the falsehood of "2 + 2 = 5" only holds in foundations where the natural numbers are provably not a [[subsingleton]] or [[h-proposition]]. 

On the other hand, an alternate statement used in [Chambers 1728](#Chambers1728) for self-evident falsehood, "$2 + 2 \neq 4$", is still false. 

> Thus, a Proposition would be absurd, that should affirm, that two and two make five; or that should deny 'em to make four. [Chambers 1728](#Chambers1728)

This is the case regardless of what foundations, since "2 + 2 = 4" is always true regardless of the status of "2 + 2 = 5". Even in [[paraconsistent mathematics]], which denies the [[principle of explosion]], $2 + 2 \neq 4$ is false, since in the event that $2 + 2 \neq 4$ is true, it is both true and false. 

The fact that "2 + 2 = 4" is always true regardless of the status of "2 + 2 = 5" was expressed by the writer Samuel Johnson, who stated 

> You may have a reason why two and two should make five, but they will still make four. [Wilson 1970](#Wilson1970) 

## See also

* [[foundations of mathematics]]
* [[reverse mathematics]]

## References

* {#Chambers1728} Chambers, Ephraim (1728). Cyclopædia: or, An Universal Dictionary of Arts and Sciences (1 ed.). London: James & John Knapton; John Darby; and others. Two volumes in folio.

* {#Wilson1970} Wilson, F. P. (1970). The Oxford Dictionary of English Proverbs (3rd ed.). Oxford: Clarendon Press. p. 849. ISBN 0198691181.

## External links

* Wikipedia, *[2 + 2 = 5](https://en.wikipedia.org/wiki/2_%2B_2_%3D_5)*

[[!redirects two plus two equals five]]
[[!redirects 2 plus 2 equals 5]]