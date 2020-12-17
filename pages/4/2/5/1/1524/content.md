
# Markov\'s Principle
* table of contents
{: toc}

## Definition

In [[constructive mathematics]], Markov\'s principle is the (classically trivial) statement that any infinite [[sequence]] of $0$ and $1$ that is not all $1$s must have a $0$ somewhere.  Stated in a more [[logic]]al form, if $P$ is a predicate on [[natural number]]s, then
$$ \forall{n}\, \big(P(n) \vee \neg{P(n)}\big) \Rightarrow \neg\forall{n}\, P(n) \Rightarrow \exists{n}\, \neg{P(n)} .$$
Compare this to
$$ \neg\exists{n}\, P(n) \Rightarrow \forall{n}\, \neg{P(n)} ,$$
which is a theorem of [[intuitionistic logic]].
More generally, a [[set]] $S$ may be called _Markovian_ if this principle holds for all predicates on $S$.  Every Kuratowski-[[finite set]] is Markovian, for example.

Markov\'s principle is often stated in terms of [[infinite sequences]] of natural numbers, using Greek letters for sequences and Latin letters for individual numbers:
$$ \forall{\alpha}\, \big(\neg\forall{n}\, (\alpha_n = 0) \Rightarrow \exists{n}\, (\alpha_n \ne 0)\big) .$$
Here, $P(n)$ is the statement that $\alpha_n = 0$, and the hypothesis $\forall{n} (P(n) \vee \neg{P(n)})$ is true for any sequence of natural numbers.  Conversely, given any predicate $P$ satisfying this hypothesis, we can define $\alpha$ by $\alpha_n = 0$ if $P(n)$ is true and $\alpha_n = 1$ if $P(n)$ is false, so the two versions of Markov\'s principle are equivalent.


## Discussion

In standard constructive mathematics (such as in the [[internal logic]] of a [[topos]]), it is possible that the only Markovian sets are the Kuratowski-[[finite sets]].  Thus, Markov\'s principle, stating that the set of natural numbers is Markovian, is nontrivial.  (It is true, of course, in a [[Boolean topos]]; that is, Markov\'s principle follows from the principle of [[excluded middle]].)

[[А. А. Марков Jr]] (the one who proved undecidability theorems, and son of the great stochastician) belonged to the [[Russian constructivism|Russian school of constructivism]], which saw mathematics as about computability.  From this perspective, Markov\'s principle is justified as follows:  We are justified in concluding $\exists{n}\, \neg{P(n)}$ if we can actually compute a value of $n$ such that $\neg{P(n)}$ can be proved; since $P$ is decidable, it\'s enough to compute $n$ such that $\neg{P(n)}$ is true.  And to compute this, you just set a computer working, deciding $P(0), P(1), P(2), \ldots$, until it finds $n$.  Other constructivists find this argument unconvincing, since they\'re not convinced that the computer will ever stop, even though it\'s impossible that it continue forever.

Equivalent forms:

*  If a [[Turing machine]] does not run forever, then it halts.
*  If an [[extended natural number system|extended natural number]] is not infinite, then it is finite.
*  If a [[Cauchy real number]] does not equal zero, then it is [[apartness relation|apart]] from zero in that it has a multiplicative inverse.

Note that the contrapositives of these are all valid regardless of Markov\'s principle.

The other major historical school of constructivism, Brouwer\'s [[intuitionism]], rejects Markov\'s principle. Brouwer\'s viewpoint has since his time been formalized, and via this formalization Markov\'s principle can be proved false. Namely, [[Kripke's schema]] with MP proves Excluded Middle, and Excluded Middle is incompatible with [[Brouwer continuity principle|continuity]]. Several models have been built satisfying Kripke\'s schema and continuity, thereby falsifying MP. These include topological models (e.g. M. Krol, ``A Topological model for intuitionistic analysis with Kripke's
Scheme," Zeitschr. f. math. Logic und Grundlagen d. Math. 24, p. 427-436, 1978), Beth models (e.g. D. van Dalen, ``An interpretation of intuitionistic analysis," Annals of Mathematical Logic 13(1), p. 1-43), realizability models (e.g. J. van Oosten, Realizability, Elsevier, 2008), and a [[Kripke model]] [BridgesRichman, p138](#BridgesRichman).  Note however that some intuitionists have advocated in favour of Markov\'s principle (and presumably then against Kripke\'s schema).


## Weak Markov\'s Principle

More recently, a weakened form of Markov\'s principle has been identified (first in ([Mandelkern 1988](#Mandelkern))) and seen to be of interest, aptly named Weak Markov\'s Principle. It states that if a binary sequence is pseudo-positive then it is positive:

$$
\forall \alpha \, \Big(\forall \beta \, \Big(\neg\neg\exists n \, (\beta(n)=1)\vee \neg\neg\exists n \, \big((\alpha(n)=1)\wedge(\beta(n)=0)\big)\Big)\rightarrow\exists n \, (\alpha(n)=1)\Big).
$$


## Analytic Markov\'s Principle

Markov\'s principle is equivalent to the assertion that if a [[Cauchy real number]] is $\ge 0$ and $\neq 0$, then it is $\gt 0$.  Another way to say this is that the standard [[apartness]] relation on Cauchy reals coincides with [[inequality]].

The analogous statement for [[Dedekind real numbers]] might be called the **analytic Markov\'s principle**, by analogy with the [analytic LPO](principle+of+omniscience#analytic).  The [[Russian constructivism|Russian constructivists]], who used Markov\'s principle most, accepted [[countable choice]], or at least $AC_{0,0}$, which implies that these two principles are equivalent.  However, in other varieties of constructive mathematics, the analytic Markov\'s principle is stronger.


## References

* {#Mandelkern} Mark Mandelkern, _Constructively Complete Finite Sets_, Mathematical Logic Quarterly **34**, issue 2 (1988) 97–103, doi:[10.1002/malq.19880340202](https://doi.org/10.1002/malq.19880340202).


For a recent comparison see:

* Matt Hendtlass and Robert Lubarsky, _Separating fragments of WLEM, LPO, and MP_, [PDF](http://math.fau.edu/lubarsky/Separating%20LLPO.pdf).
  {#HendtlassLubarsky}

* Douglas Bridges and Fred Richman, _Varieties of Constructive Mathematics_.
  {#BridgesRichman}


category: foundational axiom

[[!redirects Markov principle]]
[[!redirects Markov's principle]]
[[!redirects Markov's principle]]
[[!redirects Markov\'s principle]]
[[!redirects Markov/'s principle]]
[[!redirects Марков principle]]
[[!redirects Марков's principle]]
[[!redirects Марков's principle]]
[[!redirects Марков\'s principle]]
[[!redirects Марков/'s principle]]
[[!redirects Markov Principle]]
[[!redirects Markov's Principle]]
[[!redirects Markov's Principle]]
[[!redirects Markov\'s Principle]]
[[!redirects Markov/'s Principle]]
[[!redirects Марков Principle]]
[[!redirects Марков's Principle]]
[[!redirects Марков's Principle]]
[[!redirects Марков\'s Principle]]
[[!redirects Марков/'s Principle]]

[[!redirects Markov axiom]]
[[!redirects Markov's axiom]]
[[!redirects Markov's axiom]]
[[!redirects Markov\'s axiom]]
[[!redirects Markov/'s axiom]]
[[!redirects Марков axiom]]
[[!redirects Марков's axiom]]
[[!redirects Марков's axiom]]
[[!redirects Марков\'s axiom]]
[[!redirects Марков/'s axiom]]
[[!redirects Markov Axiom]]
[[!redirects Markov's Axiom]]
[[!redirects Markov's Axiom]]
[[!redirects Markov\'s Axiom]]
[[!redirects Markov/'s Axiom]]
[[!redirects Марков Axiom]]
[[!redirects Марков's Axiom]]
[[!redirects Марков's Axiom]]
[[!redirects Марков\'s Axiom]]
[[!redirects Марков/'s Axiom]]

[[!redirects Markov rule]]
[[!redirects Markov's rule]]
[[!redirects Markov's rule]]
[[!redirects Markov\'s rule]]
[[!redirects Markov/'s rule]]
[[!redirects Марков rule]]
[[!redirects Марков's rule]]
[[!redirects Марков's rule]]
[[!redirects Марков\'s rule]]
[[!redirects Марков/'s rule]]
[[!redirects Markov Rule]]
[[!redirects Markov's Rule]]
[[!redirects Markov's Rule]]
[[!redirects Markov\'s Rule]]
[[!redirects Markov/'s Rule]]
[[!redirects Марков Rule]]
[[!redirects Марков's Rule]]
[[!redirects Марков's Rule]]
[[!redirects Марков\'s Rule]]
[[!redirects Марков/'s Rule]]
