An _algebraic theory_ is a concept in [[universal algebra]] that describes a specific type of algebraic gadget, such as [[group|groups]] or [[ring|rings]]. An individual group or ring is a _model_ of the appropriate theory. Roughly speaking, an algebraic theory consists of a specification of operations and laws that these operations must satisfy.

Traditionally, algebraic theories were described in terms of [[logic]].  But _finitary_ algebraic theories (that is, those involving only finitary operations) can be understood category-theoretically as [[Lawvere theory|Lawvere theories]].  More generally, algebraic theories involving only operations of arity bounded by some [[cardinal number]] can be understood category-theoretically with a suitably generalization of Lawvere theories.  However, there are also algebraic theories with operations of unbounded arity, such as  the theory of algebras in which arbitrary sums are possible (one model of which is $[0,\infty]$), or the theory of [[complete lattice]]s; these can also be modeled by certain 'large Lawvere theories,' but the notion is not as well-behaved as in the bounded case; see [this thread](http://golem.ph.utexas.edu/cgi-bin/MT-3.0/sxp-comments.fcgi?entry_id=1949;parent_id=23188).

Algebraic theories (finitary or otherwise) can also be understood through [[monad]]s; in fact, some category theorists define an [[algebraic category]] to be one that is [[monadic functor|monadic]] over [[Set]] (although there are some size issues here).

+--{: .query}
[[Mike Shulman|Mike]]: What size issues?
=--

For example, the theory of a [[compact Hausdorff space]] $X$ can be seen as algebraic, with one operation for each [[direction|directed set]] $D$ that takes an [[net|ultranet]] indexed by $D$ to its limit; this is a finitary operation only when $D$ is finite (which is really the trivial case).  There is no Lawvere theory for compact Hausdorff spaces (at least, no small one), yet there is a monad for it, which maps each set $S$ to its set of [[ultrafilter]]s.

_[[essentially algebraic theory|Essentially algebraic theories]]_ allow for partially-defined operations.  Just as finitary algebraic theories can be understood as Lawvere theories, which live in the [[doctrine]] of [[cartesian monoidal category|cartesian monoidal categories]], so finitary essentially algebraic theories can be understood by a generalisation to [[finitely complete category|finitely complete categories]].
