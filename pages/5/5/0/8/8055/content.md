
# The inclusion-exclusion principle
* table of contents
{: toc}

## Idea

The principle of inclusion and exclusion is essentially a [[sheaf]] condition for [[measures]]; it allows one to calculate the total measure of a space in terms of a [[cover]].  It applies also to [[cardinality]], that is to [[counting measure]].


## Statement

Let $X$ be a [[measure space]] with measure $\mu$.  Typical examples are a [[probability space]] or subprobability space, or an arbitrary [[set]] with [[counting measure]].  (In the latter case, we may let the measure take values in all [[cardinal numbers]], so that the measure of a subset is its cardinality.)

Now let $U$ be a measurable [[finite cover]] of $X$.  (That is, we have a [[finite set|finite]] index set $I$ and a function mapping an index $j$ in $I$ to a [[measurable subspace]] $U_j$ of $X$, such that the [[union]] $\bigcup_j U_j$ of all of these subspaces is all of $X$.)  Then given any [[natural number]] $k$ and any $k$-combination $\sigma$ from $I$ (a [[subset]] of $I$ of [[cardinality]] $k$), let the __measure__ of $\sigma$ be $\mu(\bigcap_{j \in \sigma} U_j)$, the measure of the [[intersection]] of the subspaces assigned to the indexes in $\sigma$.  We will call $k$ the __size__ of the $k$-combination $\sigma$.  Note that for $k = 0$ (so $\sigma = \empty$), $\bigcap_{j \in \empty} U_j = X$.

+-- {: .num_theorem}
###### Theorem

The sum of the measures of the combinations of even size equals the sum of the measures of the combinations of odd size.
=--

If we drop the requirement that $U$ be a cover of $X$ (that the union of $U$ be $X$), we simply have that $U$ is a cover of the actual union of $U$; the only difference is that the measure of the $0$-combination is now the measure of this union instead of the measure of all of $X$.  Then the principle for small values of $n$ looks like this:

*  $\mu(\empty) = 0$,
*  $\mu(A) = \mu(A)$,
*  $\mu(A \cup B) + \mu(A \cap B) = \mu(A) + \mu(B)$ (\*),
*  $\mu(A \cup B \cup C) + \mu(A \cap B) + \mu(A \cap C) + \mu(B \cap C) = \mu(A) + \mu(B) + \mu(C) + \mu(A \cap B \cap C)$,
*  etc.

If subtraction is available (as when $\mu$ is a [[finite measure]]), we may solve for the first term on the left (the term from the $0$-combination, that is the measure of the union):

*  $\mu(\empty) = 0$,
*  $\mu(A) = \mu(A)$,
*  $\mu(A \cup B) = \mu(A) + \mu(B) - \mu(A \cap B)$,
*  $\mu(A \cup B \cup C) = \mu(A) + \mu(B) + \mu(C) - \mu(A \cap B) - \mu(A \cap C) - \mu(B \cap C) + \mu(A \cap B \cap C)$,
*  etc.

The general formula is $\mu(\underset{1 \le i \le n}{\bigcup A_{i}}) = \underset{(I  \neq \emptyset)\subseteq [1,n]}{\sum}(-1)^{|I|+1}\mu(\underset{i \in I}{\bigcap}A_{i})$.

This explains the term 'inclusion-exclusion'; we are alternately adding (including) and subtracting (excluding) various intersections.


## Proof

The proof is for all subspaces of a given measure space, by induction on the cardinality $n$ of the index set $I$.  Although it is atypical, one may take, as one of the basic axioms of a measure, the formula (\*), that is the inclusion-exclusion formula (on all measurable subspaces) for $n = 2$; in any case, this is easy to prove.  Then the formula for $n \gt 2$ may be proved by induction.  (The formula for $n = 0$ is the axiom that the measure of the [[empty set]] is [[zero]], and the formula for $n = 1$ is trivial.)


## As a definition of measure

The principle applies perfectly well to finitely additive measures (charges) taking values in any [[abelian monoid]].  On the other hand, the statement of inclusion-exclusion makes sense even when the cover $U$ is not finite; and if we require it whenever $U$ is [[countable set|countable]], then we force the measure to be countably additive.  If we require inclusion-exclusion for arbitrary (even uncountable) $U$, then we get the definition of a [[normal measure]].

In [[constructive mathematics]], the inclusion-exclusion principle fails in that $\mu$ may satisfy $\mu(A \cup B) = \mu(A) \cup \mu(B)$ when $A$ and $B$ are [[disjoint sets|disjoint]] without necessarily satisfying (\*).  On the other hand, we may adopt (\*) as the proper clause in the *definition* of measure.  For measures on a [[Cheng space]] (which is the best established constructive theory of measure in general), inclusion-exclusion follows from finite additivity (for disjoint sets) and the principle that intersection with [[full sets]] (which are specified for a Cheng space before any measure is given) preserves measure, so in that sense it makes no difference which axiom we take.  But (\*) is not valid constructively for cardinality in general; counting measure is a Cheng measure only on sets with [[decidable equality]].

In both cases, we see that we can adopt the principle of inclusion-exclusion (which ultimately is motivated by cardinality of finite sets) as the only principle necessary to *define* what we mean by a measure (although we must already have a [[measurable space]] to define it on).


[[!redirects inclusion-exclusion]]
[[!redirects inclusion-exclusion principle]]
