A **finite set** is a set $A$ for which there exists a [[bijection]] between $A$ and the set $\{k\in N | k\lt n\}$ for some $n\in N$, where $N$ is the natural numbers.

Classically, the finite sets are the [[finitely presentable object|finitely presentable objects]] in [[Set]].

## Finiteness in constructive mathematics ##

In [[constructivism|constructive mathematics]] (and, thus, internally to a [[topos]]) a number of classically equivalent notions of finiteness become distinguishable.  In addition to the above notion (for which one generally reserves "finite"), we have the following.

* A set is **subfinite** if it admits an injection into some finite set.

* A set is **finitely indexed** or **Kuratowski-finite** (or even sometimes, confusingly, _subfinite_) if it is a surjective image of some finite set.

* A set is **subfinitely indexed** if it admits a surjection from a subfinite set, or equivalently admits an injection to a finitely indexed set; that is, it is a [[subquotient]] of a finite set.

Finite sets are always [[projective object|projective]]; that is, the "finite [[axiom of choice]]" always holds.  However, if any finite set greater than 1 is [[choice object|choice]], or if every 2-indexed set is projective, then the logic must be classical (see [[excluded middle]] for a proof).

* A set is **Dedekind-finite** if any injection from it to itself must be a bijection.  In contrast to the previous three notions, Dedekind-finite infinite sets can coexist with [[excluded middle|PEM]], although [[countable choice]] suffices to banish them.

All of these definitions can be phrased to make sense even without an axiom of infinity (and thus in a topos without a [[natural numbers object]]). Basically, you define (for a given set $S$) the concept of 'collection of subsets of $S$ that includes all of the finite subsets' by requiring it to be closed under inductive operations appropriate for the sense of 'finite' that you want; then $S$ is finite if and only if it is an element of all such collections.

+--{.query}
Challenge: Can you think of a way to define it [[predicativism|predicatively]]?
=--