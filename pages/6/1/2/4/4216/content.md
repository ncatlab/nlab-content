In [[logic]], logical conjunction is the [[meet]] in the [[poset]] of [[truth values]].

Assuming that (as in [[classical logic]]) the only truth values are true ($T$) and false ($F$), then the conjunction $p \wedge q$ of the truth values $p$ and $q$ may be defined by a truth table:

|$p$|$q$| |$p \wedge q$|
|---|---|-|------------|
|$T$|$T$| |$T$|
|$T$|$F$| |$F$|
|$F$|$T$| |$F$|
|$F$|$F$| |$F$|

That is, $p \wedge q$ is true if and only if $p$ and $q$ are both true.  Conjunction also exists in nearly every non-classical logic.

More generally, if $p$ and $q$ are any two [[relations]] on the same domain, then we define their conjunction pointwise, thinking of a relation as a [[function]] to truth values.  If instead we think of a relation as a [[subset]] of its domain, then conjunction becomes [[intersection]].

As truth values form a poset, which is a degenerate kind of [[category]], so truth values under conjunction form a [[meet-semilattice]], which is a degenerate kind of [[cartesian monoidal category]].  Self-referentially, a [[poset]] is (up to [[equivalence of categories|equivalence]]) simply a [[category enriched]] over the cartesian monoidal category of truth values.  With [[implication]] as [[internal hom]], truth values form a [[closed cartesian category]].

Like any meet, conjunction is an associative operation, so we can take the conjunction of any finite positive whole number of truth values; the conjunction is true if and only if all of the individual truth values are true.  Conjunction also has an [[identity element]], which is the [[truth|true]] truth value.  Some logics allow a notion of infinitary conjunction.  Indexed conjunction is [[universal quantification]].


[[!redirects logical conjunction]]
