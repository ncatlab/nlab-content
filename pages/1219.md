{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

[Roman Sikorski](http://www.ams.org/mathscinet/search/author.html?mrauthid=162010) defined the term "differential module" in 1971/72.
[Mark Mostow](http://www.ams.org/mathscinet/search/author.html?mrauthid=127450) further developed the theory in 1979.
The following definition of a differentiable space (a kind of [[generalized smooth space]]) comes from Mostow's paper where it is attributed to Sikorski.

+-- {: mynumdef #DiffSp}
###### Definition
A _differentiable space_ is a topological space $X$ together with, for each open $U$ in $X$, a collection $C^\infty(U)$ of continuous real-valued functions on $U$, satisfying the closure conditions:

1. The rule $U \to C^\infty(U)$ defines a sheaf on $X$ (denoted $C^\infty X$).
2. For any $n$, if $f_1, \dots, f_n \in C^\infty(U)$ and $g \in C^\infty(\mathbb{R}^n)$ (with the usual meaning), then $g(f_1, \dots, f_n) \in C^\infty(U)$.

The elements of $C^\infty(X)$ are called _smooth functions_ on $X$.
=--

# References #
* [Differential modules](http://www.ams.org/mathscinet-getitem?mr=482794) 1971/72
* [The differentiable space structures of Milnor classifying spaces, simplicial complexes, and geometric realizations](http://www.ams.org/mathscinet-getitem?mr=587553) 1979.