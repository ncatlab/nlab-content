
# Positive elements
* table of contents
{: toc}

## Idea

In [[classical mathematics]], an element of a [[preordered set]] is positive if and only if it not a [[bottom element]].

A more subtle definition is needed in [[constructive mathematics]]; analogously to how "nonempty sets" may need to be replaced by [[inhabited sets]].  In mathematics that is both constructive and [[predicative mathematics|predicative]], positivity can be axiomatised but not defined.


## Definitions

Let $L$ be a [[preordered set]], and let $x$ be an element of $L$.

+-- {: .num_defn #preddef}
###### Definition
**(in [[classical mathematics]], and in [[predicative mathematics]] with [[classical logic]])**

An element $x \in L$ is __positive__ if it is not a [[bottom element]], equivalently if there exists an element $y \in L$ such that $x \leq y$ is false: $\neg(x \leq \bigvee \empty)$.
=--

+-- {: .num_defn #constdef}
###### Definition
**(in [[classical mathematics]], and in impredicative [[constructive mathematics]])**

An element $x$ of $L$ is __positive__ if whenever $x$ is the [[join]] of some [[subset]] $A$ of $\{x\}$ in $L$, $A$ is [[inhabited subset|inhabited]] (and so all of $\{x\}$): $\forall P\colon Prop,\; x = \bigvee \{x \;|\; P\} \;\Rightarrow\; P$.
=--

It follows that any arbitrary subset $A$ of $L$ is inhabited if $x$ is the join of $A$.  (This is because if $x = \bigvee A$, then $x = \bigvee \{x \;|\; A\ is\ inhabited\}$.)  But it\'s important that the definition only quantifies over [[truth values]], which is why this definition is classically predicative, and may even be acceptable to some constructive predicativists who don\'t accept [[function sets]].

+-- {: .num_defn #predconstdef}
###### Definition
**(in [[predicative mathematics|predicative]] [[constructive mathematics|constructive]] mathematics)**

A **positivity predicate** on $L$ is a [[predicate]] $\lozenge{x}$, pronounced "$x$ is positive", such that

*  If $x$ is the join of a subset and $x$ is positive, then some element of that subset is positive: $\lozenge{x} \;\wedge\; x = \bigvee A \;\vdash\; \exists\, u \in A,\; \lozenge{u}$.

*  If $x$ equals a join on the assumption that $x$ is positive, then $x$ really is that join: $\lozenge{x} \;\Rightarrow\; x = \bigvee A \;\vdash\; x = \bigvee A$.
=--

These definitions are equivalent under certain circumstances.  Specifically:

* In predicative mathematics with classical logic, one can prove that every preorder has a unique positivity predicate, which must match Definition \ref{preddef}.

* In impredicative constructive mathematics, one can prove that if a preorder admits a positivity predicate, then it is given by Definition \ref{constdef}.  However, in general, the predicate defined in Definition \ref{constdef} is not a positivity predicate in the sense of Definition \ref{predconstdef}.

* In [[classical mathematics]] (with [[classical logic]] and impredicativity), all of the definitions are equivalent.


## Examples

Every [[power set]] has a positivity predicate: $x$ is positive iff $x$ is [[inhabited subset|inhabited]].  (Of course, there are few power sets in predicative mathematics, but often it is enough to think of the power set as a [[proper class]].)

The positive predicate on a [[locale]] plays a role in the definition of an [[overt space]].  Locale theory is often considered constructively but impredicatively; in predicative constructive mathematics, a positivity predicate is used in the corresponding theory of [[formal topology]].

In impredicative constructive mathematics, a sufficient condition for a complete poset to possess a positivity predicate is that any element is a join of positive elements. To show this, it suffices to prove that for any element $a$, it holds that $a = \bigvee \{ a \;|\; \lozenge{a} \}$ (that is, $a = \bigvee \{ b \;|\; b = a \;\wedge\; \lozenge{b} \}$). The remaining properties can then be easily verified. By assumption, $a = \sup B$ for some set $B$ containing only positive elements. For any $b \in B$, it holds that $b \leq a$, thus that $a$ is positive and thus that $b \leq \bigvee \{ a \;|\; \lozenge{a} \}$. Therefore $\sup B \leq \bigvee \{ a \;|\; \lozenge{a} \}$ holds as well. The other inequality is trivial.

Every [[atom]] of $L$ is positive, and indeed an atom is precisely a [[minimal element|minimal]] positive element.


## Properties

Although classically trivial, a key property of positivity in the constructive context is this:
$$ \bigvee A = \bigvee A^+ ,$$
where $A^+$ is the set of positive elements of $A$.
A special case is
$$ a = \bigvee \{a\}^+ = \bigvee \{ a | \lozenge{a} \} $$
for any element $a$.
But note that in impredicative constructive matematics, Definition \ref{constdef} does *not* necessarily satisfy this; rather, that definition satisfies either property (hence both) if and only if it satisfies Definition \ref{predconstdef}.  So these properties are really for Definitions \ref{preddef} and \ref{predconstdef} only.


[[!redirects positive element]]
[[!redirects positive elements]]
[[!redirects positivity predicate]]
[[!redirects positivity predicates]]
