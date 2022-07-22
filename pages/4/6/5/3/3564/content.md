+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A __Heyting prealgebra__ is simply a [[preorder]] whose [[poset]]al reflection is a [[Heyting algebra]]; i.e., it is a preorder which is a [[bicartesian closed category]].

In most contexts, there is little need to maintain a difference between Heyting algebras whose carriers are preorders vs. those whose carriers are strictly posets; indeed, in most contexts, there is no need to consider such a distinction to even be meaningful, the only relevant notion of equality being that derived from the preorder structure.  See [[principle of equivalence]].

However, in contexts where there _is_ a separately provided relevant notion of equality on the carrier which is potentially finer-grained than that provided by the preorder structure alone (i.e., in situations where a Heyting algebra carries further structure $x = y$ not necessarily provided simply by $x \leq y \wedge y \leq x$), then it may be worthwhile to track such differences.

## Examples

* The [[propositions]] in a [[formal logic|logic]] naturally form a Heyting prealgebra under [[entailment]].

  One can take the quotient under bi-entailment to get a poset and a Heyting algebra, or (as discussed above) one can say that bi-entailment is the only relevant notion of equality so that the preorder is really already a poset. But if one wants to simultaneously talk about the syntactic equality of terms, then there will be unequal terms that entail each other, and so one has only a Heyting prealgebra.


## See also

* [[Heyting prealgebra object]]

[[!redirects Heyting prealgebras]]
[[!redirects bicartesian closed preorder]]
[[!redirects bicartesian closed preorders]]
[[!redirects bicartesian closed preordered set]]
[[!redirects bicartesian closed preordered sets]]
[[!redirects bicartesian closed proset]]
[[!redirects bicartesian closed prosets]]
