
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[logic]], the __De Morgan laws__ refer to the the following laws:
$$ \array {
   \neg(p \wedge q) \;\iff\; \neg{p} \vee \neg{q} ,
   \\
   \neg(p \vee q) \;\iff\; \neg{p} \wedge \neg{q} .
} $$

More generally, the __De Morgan laws__ are the statements, valid in various forms of logic, that [[De Morgan duality]] is mediated by [[negation]]. 

## In constructive mathematics

In the [[foundations]] of [[constructive mathematics]], __De Morgan\'s Law__ usually means the statement
$$ \neg(p \wedge q) \Rightarrow \neg{p} \vee \neg{q} ,$$
since every other aspect of the first two lines is already constructively valid, the claim that negation mediates the De Morgan self-duality already has a name (the [[double negation]] law, equivalent to the principle of [[excluded middle]]), and no other line involves only operators that appear in intuitionstic [[propositional calculus]]. 

### Equivalent statements

This de Morgan's law is equivalent to the following: 

* [[weak excluded middle]] 

* That the [[negation]] of every [[equivalence relation]] is an [[apartness relation]]

## In homotopy type theory

In the context of [[homotopy type theory]], there are two versions of the constructive De Morgan's law, depending on whether the "or" in the law is interpreted as a [[propositional truncation|propositionally truncated]] [[sum type]] 
$$ \prod_{A,B} \neg(A \wedge B) \to \Vert \neg A + \neg B \Vert $$
or as an untruncated sum type: 
$$ \prod_{A,B} \neg(A \wedge B) \to (\neg A + \neg B). $$

However, [[Martin Escardo]] proved that the truncated and untruncated versions of De Morgan's law are the same: 

+-- {: .un_lemma}
###### Lemma
Truncated De Morgan's law implies [[weak excluded middle|weak]] [[excluded middle]]:
$$ \prod_{A} \neg A + \neg\neg A.$$
=--
Note that truncation or its absence is irrelevant in weak excluded middle, since $\neg A$ and $\neg\neg A$ are [[mutually exclusive proposition|mutually exclusive]] so that $\neg A + \neg\neg A$ is always a proposition.
+-- {: .proof}
###### Proof
Let $B=\neg A$ in the truncated De Morgan's law, and notice that $\neg(A\wedge \neg A)$ always holds.
=--

+-- {: .un_lemma}
###### Lemma
Weak excluded middle implies that binary sums of negations have split support:
$$\prod_{A,B} \Vert \neg A + \neg B \Vert \to (\neg A + \neg B). $$
=--
+-- {: .proof}
###### Proof
By weak excluded middle, either $\neg A$ or $\neg\neg A$.  In the first case, $\neg A + \neg B$ is just true.  In the second case, either $\neg B$ or $\neg\neg B$.  In the first subcase, $\neg A + \neg B$ is again just true.  In the second subcase, we have $\neg\neg A$ and $\neg\neg B$, whence $(\neg A + \neg B) = 0$ and in particular is a proposition.
=--

+-- {: .un_theorem}
###### Theorem
Truncated De Morgan's law implies untruncated De Morgan's law,
$$ \prod_{A,B} \neg(A \wedge B) \to (\neg A + \neg B) $$
=--
+-- {: .proof}
###### Proof
Combine the two lemmas.
=--

## In the theory of lattice-ordered abelian groups

Peter Freyd's definition of a [[lattice-ordered abelian group]] in [Freyd 08](#Freyd08) is equational, and so is a [[Lawvere theory]] and could be defined in a category with finite products and a generic object $A$ where every object is equivalent to a finite product of $A$. 

Freyd then showed that the de Morgan laws are satisfied in any [[lattice-ordered abelian group]]:

$$-(p \vee q) = (-p) \wedge (-q)$$
$$-(p \wedge q) = (-p) \vee (-q)$$

with the join and meet being the lattice operations and negation being the negation of the abelian group. 

In particular, the de Morgan laws are valid for the [[integers]], the [[rational numbers]], and the [[Dedekind real numbers]], with the join being the maximum function and the meet being the minimum function. 


## Related concepts

* [[De Morgan Heyting algebra]]

* [[De Morgan Heyting category]]

* [[De Morgan algebra]]

* [[De Morgan topos]]

* [[excluded middle]]

* [[De Morgan duality]]


## References

Named after *[[Augustus De Morgan]]*.

* {#Freyd08} [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

See also: 

* Wikipedia, *[De Morgan's laws](https://en.wikipedia.org/wiki/De_Morgan%27s_laws)*


[[!redirects De Morgan law]]
[[!redirects De Morgan laws]]
[[!redirects de Morgan law]]
[[!redirects de Morgan laws]]
[[!redirects De Morgan's law]]
[[!redirects De Morgan's laws]]
[[!redirects de Morgan's law]]
[[!redirects de Morgan's laws]]
[[!redirects De Morgan's law]]
[[!redirects De Morgan's laws]]