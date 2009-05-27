In [[constructive mathematics]], Markov\'s principle is the (classically trivial) statement that any infinite [[sequence]] of $0$ and $1$ that is not all $1$s must have a $0$ somewhere.  Stated in a more [[logic]]al form, if $P$ is a predicate on [[natural number]]s, then
$$ (\forall n, P(n) \vee \neg{P(n)}) \Rightarrow \neg(\forall n, P(n)) \Rightarrow \exists n, \neg{P(n)} .$$
Compare this to
$$ \neg(\exists n, P(n)) \Rightarrow \forall n, \neg{P(n)} ,$$
which is a theorem of [[intuitionistic logic]].
More generally, a [[set]] $S$ may be called _Markovian_ if this principle holds for all predicates on $S$.

In standard constructive mathematics (such as in the [[internal logic]] of a [[topos]]), it is possible that the only Markovian sets are the Kuratowski-[[finite set]]s.  Thus, Markov\'s principle, stating that the set of natural numbers is Markovian, is nontrivial.  (It is true, of course, in a [[Boolean topos]]; that is, it follows from the principle of [[excluded middle]].)

&#1040;. &#1040;. &#1052;&#1072;&#1088;&#1082;&#1086;&#1074; Jr (the one who proved undecidability theorems, and son of the great stochastician) belonged to the Russian school of constructivism, which saw mathematics as about computability.  From this perpsective, Markov\'s principle is justified as follows:  We are justified in concluding $\exists n, \neg{P(n)}$ if we can actually compute a value of $n$ such that $P(n)$ can be proved; since $P$ is decidable, it\'s enough to compute $n$ such that $P(n)$ is true.  And to compute this, you just set a computer working, deciding $P(0), P(1), P(2), \ldots$, until it finds $n$.  Other constructivists find this argument unconvincing, since they\'re not convinced that the computer will ever stop, even though it\'s impossible that it continue forever.

Equivalent forms:
*  If a Turing machine does not run forever, then it halts.
*  If an [[extended natural number system|extended natural number]] is not infinite, then it is finite.
*  If a located [[real number]] does not equal zero, then it is [[apartness relation|apart]] from zero in that it has a multiplicative inverse.

Note that the contrapositives of these are all valid regardless of Markov\'s principle.