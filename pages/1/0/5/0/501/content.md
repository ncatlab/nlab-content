A **finite set** is a set $A$ for which there exists a [[bijection]] between $A$ and the set $\{k\in N | k\lt n\}$ for some $n\in N$, where $N$ is the natural numbers.

Classically, the finite sets are the [[finitely presentable object|finitely presentable objects]] in [[Set]].

## Finiteness in constructive mathematics ##

In [[constructivism|constructive mathematics]] (and, thus, internally to a [[topos]]) a number of classically equivalent notions of finiteness become distinguishable.  In addition to the above notion (for which one generally reserves "finite"), we have the following.

* A set is **subfinite** if it admits an injection into some finite set.

* A set is **finitely indexed** or **Kuratowski-finite** (or even sometimes, confusingly, _subfinite_) if it is a surjective image of some finite set.  (This can be phrased differently to make sense even in a topos without a [[natural numbers object]].)  

* A set is **subfinitely indexed** if it admits a surjection from a subfinite set, or equivalently admits an injection to a finitely indexed set; that is, it is a [[subquotient]] of a finite set.

Finite sets are always [[projective object|projective]]; that is, the "finite [[axiom of choice]]" always holds.  However, if any finite set greater than 1 is [[choice object|choice]], or if every 2-indexed set is projective, then the logic must be classical (see [[excluded middle]] for a proof).

* A set is **Dedekind-finite** if any injection from it to itself must be a bijection.  In contrast to the previous three notions, Dedekind-finite infinite sets can coexist with [[excluded middle|PEM]], although [[countable choice]] suffices to banish them.
