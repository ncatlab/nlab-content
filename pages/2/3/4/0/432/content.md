# Idea #

**Predicative mathematics** is a version of [[constructivism|constructive mathematics]] which, in addition to rejecting the [[axiom of choice]] and the principle of [[excluded middle]], rejects _impredicative definitions_.

Informally, a definition is _impredicative_ if it refers to a totality which includes the thing being defined.  For example, the definition of a particular real number $x$ as the least upper bound of a given set $A$ is impredicative, because it characterizes $x$ as a particular element of some set (the upper bounds of $A$) which includes $x$.

# Impredicative axioms #

Two set-theoretic axioms which are commonly rejected by predicativists as leading to impredicative definitions are the axiom of unbounded [[separation]] and the axiom that any set has a power set.  In particular, the rejection of the latter means that predicativists do not believe the category of sets is a [[topos]], and that conversely predicative mathematics is naturally interpreted in the [[internal logic]] of categories more general than toposes, such as [[pretopos]]es.

However, many predicativists do accept the existence of the [[exponential]] $B^A$ for any sets $A,B$ (that is, the set of functions $A\to B$).  These predicativists believe that the category of sets is [[locally cartesian closed category|locally cartesian closed]], and their mathematics can be interpreted in any locally cartesian closed pretopos.  Some predicativists also assume stronger axioms, such as the "fullness" or "[[subset collection]]" axiom of Aczel's theory CZF, or the existence of [[W-type|W-types]] (equivalently, [[inital algebra]]s of polynomial functors, a strong form of the axiom of infinity).

# Discussion #

_[[Mike Shulman|Mike]]_: Is there a formal definition of "impredicative" other than "whatever predicativists don't like?" In particular, I don't understand why exponentials are any less problematic than power sets.  If I have the set $B^A$, can't I then use it to define a new function $A\to B$ in terms of this set that contains the function being defined?

_Toby_: Arguably, Brouwer\'s school doesn\'t accept exponentiation, although they accept some cases of it (such as $N^N$). I\'ve never heard them call it 'impredicative', however. Someday I want to figure out how much can be done using both W-types and co-W-types (equivalently, final coalgebras of polynomial functors) but not exponentiation. (So far, I can construct $A^N$ as the final coalgebra of $X \mapsto A \times X$, but I can\'t prove that it *is* $A^N$!)