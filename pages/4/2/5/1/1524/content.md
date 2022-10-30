# Markov\'s Principle
* table of contents
{: toc}

In [[constructive mathematics]], Markov\'s principle is the (classically trivial) statement that any infinite [[sequence]] of $0$ and $1$ that is not all $1$s must have a $0$ somewhere.  Stated in a more [[logic]]al form, if $P$ is a predicate on [[natural number]]s, then
$$ (\forall n, P(n) \vee \neg{P(n)}) \Rightarrow \neg(\forall n, P(n)) \Rightarrow \exists n, \neg{P(n)} .$$
Compare this to
$$ \neg(\exists n, P(n)) \Rightarrow \forall n, \neg{P(n)} ,$$
which is a theorem of [[intuitionistic logic]].
More generally, a [[set]] $S$ may be called _Markovian_ if this principle holds for all predicates on $S$.

In standard constructive mathematics (such as in the [[internal logic]] of a [[topos]]), it is possible that the only Markovian sets are the Kuratowski-[[finite set]]s.  Thus, Markov\'s principle, stating that the set of natural numbers is Markovian, is nontrivial.  (It is true, of course, in a [[Boolean topos]]; that is, Markov\'s principle follows from the principle of [[excluded middle]].)

[[А. А. Марков Jr]] (the one who proved undecidability theorems, and son of the great stochastician) belonged to the [[Russian constructivism|Russian school of constructivism]], which saw mathematics as about computability.  From this perpsective, Markov\'s principle is justified as follows:  We are justified in concluding $\exists n, \neg{P(n)}$ if we can actually compute a value of $n$ such that $P(n)$ can be proved; since $P$ is decidable, it\'s enough to compute $n$ such that $P(n)$ is true.  And to compute this, you just set a computer working, deciding $P(0), P(1), P(2), \ldots$, until it finds $n$.  Other constructivists find this argument unconvincing, since they\'re not convinced that the computer will ever stop, even though it\'s impossible that it continue forever.

Equivalent forms:
*  If a [[Turing machine]] does not run forever, then it halts.
*  If an [[extended natural number system|extended natural number]] is not infinite, then it is finite.
*  If a [[Cauchy real number]] does not equal zero, then it is [[apartness relation|apart]] from zero in that it has a multiplicative inverse.

Note that the contrapositives of these are all valid regardless of Markov\'s principle.

The other major school of constructivism, Brouwer\'s intuitionism, rejects Markov\'s principle. Brouwer\'s viewpoint has since his time been formalized, and via this formalization Markov\'s principle can be proved false. Namely, Kripke\'s schema with MP proves Excluded Middle, and Excluded Middle is incompatible with continuity. Several models have been built satisfying Kripke\'s schema and continuity, thereby falsifying MP. These include topological models (e.g. M. Krol, ``A Topological model for intuitionistic analysis with Kripke's
Scheme," Zeitschr. f. math. Logic und Grundlagen d. Math. 24, p. 427-436, 1978), Beth models (e.g. D. van Dalen, ``An interpretation of intuitionistic analysis," Annals of Mathematical Logic 13(1), p. 1-43), and realizability models (e.g. J. van Oosten, Realizability, Elsevier, 2008).

More recently, a weakened form of Markov\'s principle has been identified (first in M. Mandelkern, ``Constructively complete finite sets," Zeitschr. f. math. Logic und Grundlagen d. Math. 34, p. 97-103, 1988) and seen to be of interest, aptly named Weak Markov\'s Principle. It states that if a binary sequence is pseudo-positive then it is positive:

$
\forall \alpha \; [\forall \beta \; (\neg\neg\exists n \; (\beta(n)=1)\vee \neg\neg\exists n \; (\alpha(n)=1\wedge\beta(n)=0))\rightarrow\exists n \; \alpha(n)=1].
$


category: foundational axiom

[[!redirects Markov principle]]
[[!redirects Markov's principle]]
[[!redirects Markov's principle]]
[[!redirects Markov\'s principle]]
[[!redirects Марков principle]]
[[!redirects Марков's principle]]
[[!redirects Марков's principle]]
[[!redirects Марков\'s principle]]

[[!redirects Markov axiom]]
[[!redirects Markov's axiom]]
[[!redirects Markov's axiom]]
[[!redirects Markov\'s axiom]]
[[!redirects Марков axiom]]
[[!redirects Марков's axiom]]
[[!redirects Марков's axiom]]
[[!redirects Марков\'s axiom]]

[[!redirects Markov rule]]
[[!redirects Markov's rule]]
[[!redirects Markov's rule]]
[[!redirects Markov\'s rule]]
[[!redirects Марков rule]]
[[!redirects Марков's rule]]
[[!redirects Марков's rule]]
[[!redirects Марков\'s rule]]
