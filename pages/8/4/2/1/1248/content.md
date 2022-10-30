
# Cantor\'s Theorem
* table of contents
{: toc}

## Summary

[[Georg Cantor]] proved many theorems, but the one usually called _Cantor\'s theorem_ is the first nontrivial theorem of Cantor\'s new [[set theory]]: that some infinities are bigger than others; in particular, any infinite [[cardinal number]] (or [[infinite set]]) generates a larger one by taking the [[power set]].

(The theorem applies to all sets, not just infinite ones, although it\'s fairly obvious for [[finite sets]].)

Cantor\'s theorem should not be confused with the Cantor--Schroeder--Bernstein theorem (see [[cardinal number]]), which is different (but related, as it is important to justify Cantor\'s interpretation of his theorem).


## History

Prior to Cantor, people tended to think of infinity (whether they believed in it or not) as an absolute concept: all infinities are equivalent.  It had been noticed (by [[Galileo Galilei|Galileo]], for example) that it\'s possible to give an [[infinite set]] a [[self-function|self]]-[[injection]] that is not a [[surjection]]; for example, the inclusion of the even integers into the integers by doubling.  Thus here are two infinities ---the infinity $E$ of even integers and the infinity $N$ of all integers--- that are actually equivalent, even though at first glance it would appear that $E$ is smaller.

Cantor showed that such an equivalence *fails* with the [[real numbers]] $R$: no map from $N$ to $R$ can be surjective (so that $R$ is [[uncountable set|uncountable]]).  His first argument was ad hoc, but he then generalised this with the _diagonal argument_ to show that no map from any set $S$ to its [[power set]] $\mathcal{P}S$ could be surjective.  (This covered the uncountability of $R$, since Cantor found a [[bijection]] between $R$ and $\mathcal{P}N$, which we can now regard as an instance of the [[Cantor–Schröder–Bernstein Theorem]].)  As there is an obvious injective map (the [[singleton]] map) from $S$ to $\mathcal{P}S$, Cantor concluded that the cardinality of the one is strictly smaller than the cardinality of the other.

Cantor\'s argument, like his whole set theory, was controversial at the time.  Those who, like [[Leopold Kronecker|Kronecker]], believed that all mathematics should be [[finite mathematics]], considered it meaningless.  Even more moderate early [[constructive mathematics|constructivists]], such as [[Jan Brouwer|Brouwer]] and [[Hermann Weyl|Weyl]], found that it had little point.  (In particular, it says nothing directly about $R$, since the bijection between $R$ and $\mathcal{P}N$ is not constructively valid, although Cantor\'s original proof that $R$ is uncountable can be made to work.)

However, the versions of the theorem stated below are constructively valid, and Theorem \ref{lawvere} is even [[predicative mathematics|predicatively]] valid (as long as one has [[function sets]]); modern constructivists generally accept these as theorems.  (The interpretation, however, is not so clear.)  They are in fact theorems in the [[internal logic|internal language]] of any [[topos]] (and Theorem \ref{lawvere} is a theorem in any $\Pi$-[[pretopos]]).


## Statements and proofs

+-- {: .num_theorem #lawvere}
###### Theorem
(Lawvere\'s version.)

Given sets $S$ and $V$, suppose that there is a [[surjection]] from $S$ to the [[function set]] $S \to V$ (also written $V^S$).  Then every map $n\colon V \to V$ has a [[fixed point]]; that is, $n(x) = x$ for some $x\colon V$.
=--

(This generalizes to _[[Lawvere's fixed point theorem]]_.)

+-- {: .proof}
###### Proof

Let $f\colon S \to (S \to V)$ be any function, and consider the function $g\colon S \to V$ given by
$$ g(a) = n(f(a)(a)) .$$
That is, if one uses [[currying]] to interpret $f$ as a function from $S \times S$ to $V$, then $g$ is defined using the [[diagonal map]] $\Delta_S$ as
$$ S \stackrel{\Delta_S}\to S \times S \stackrel{f}\to V \stackrel{n}\to V .$$

Now suppose that $f$ is surjective.  Then there must be some element $a\colon S$ such that $f(a) = g$.  But then
$$ g(a) = n(f(a)(a)) = n(g(a)) ,$$
so $g(a)$ is a fixed point of $n$.
=--

The presence of the diagonal map $\Delta_S$ here explains why this proof is called the _diagonal argument_.  (This explanation is anachronistic but morally correct.) Lawvere's proof also explains (in fact generalizes) the $Y$&#8209; or [[fixed-point combinator]] in [[untyped lambda-calculus]], where $Y(n)$ is a fixed-point for any term $n$. 

It immediately follows (even constructively) that if $V$ has a [[self-mapping]] with no fixed point, then no map from $S$ to $S \to V$ can be a surjection.  In fact, we have something slightly stronger than (but classically equivalent to) the failure of $f$ to be a surjection: there actually exists an element $g$ of $S \to V$ that is not equal to any value in the range of $f$.  (If $V$ has an [[apartness relation]], then you can get an even stronger result for a correspondingly stronger hypothesis on $n$, but that doesn\'t apply to the versions below.)

+-- {: .num_theorem #cantor}
###### Theorem
(Cantor\'s version.)

Given a set $S$, there is no surjection from $S$ to the [[power set]] $\mathcal{P}S$.
=--

+--{: .proof}
###### Proof

Let $V$ be the set of [[truth values]], and let $n\colon V \to V$ be [[negation]].  Since $n$ has no fixed point, apply Theorem \ref{lawvere}.
=--

Note that although negation doesn\'t have all of its usual properties in constructive mathematics, $p = \neg{p}$ is still impossible.

The next version is classically equivalent to the previous version (at least if you check that $\mathcal{P}S$ is [[inhabited set|inhabited]]), but not constructively equivalent.  (Indeed, unlike Theorem \ref{lawvere}, it apparently has no constructive analogue when $\mathcal{P}S$ is replaced by $V^S$.)  This argument is from Proposition 2.8.8 of Taylor\'s _[[Practical Foundations]]_ (although I don\'t know if it really originated there).

+-- {: .num_theorem #taylor}
###### Theorem
(Taylor\'s version.)

Given a set $S$, there is no [[injection]] from $\mathcal{P}S$ to $S$.
=--

+-- {: .proof}
###### Proof

Let $i\colon \mathcal{P}S \to S$ be any function.  Define $f\colon S \to \mathcal{P}S$ as follows:
$$ f(a) = \{ b\colon S \;|\; \forall (U\colon \mathcal{P}S),\; i(U) = a \;\Rightarrow\; b \in U \} .$$
If $i$ is an injection, then $f$ is a [[retraction]] of $i$ and hence a surjection, which is impossible by Theorem \ref{cantor}.
=--

Of course, Cantor also proved Theorem \ref{taylor}, but his proof was not constructive.

We can combine Theorems \ref{cantor} and \ref{taylor} into the following even more general statement, taken from D4.1.8 of Johnstone\'s _[[Elephant]]_.

+-- {: .num_theorem #johnstone}
###### Theorem
(Johnstone\'s version.)

Given a set $S$, its power set $\mathcal{P}S$ cannot be expressed as a [[subquotient]] of $S$.
=--

+-- {: .proof}
###### Proof

Suppose we had a set $B$, an injection $i\colon B \hookrightarrow S$ and a surjection $f\colon B \to \mathcal{P}S$.  Then the [[preimage]] function $i^*\colon\mathcal{P}S \to \mathcal{P}B$ would be a surjection (because $i^\ast \exists_i = 1_{\mathcal{P}B}$), as would the [[image]] function $\exists_f\colon \mathcal{P}B \to \mathcal{P}\mathcal{P}S$ (because $\exists_f f^\ast = 1_{\mathcal{P}\mathcal{P}S}$).  Thus their composite would be a surjection $\mathcal{P}S \to \mathcal{P}\mathcal{P}S$, which is impossible by Theorem \ref{cantor}.
=--


## Interpretation

Note that there exists an [[injection]] from $S$ to $\mathcal{P}S$, given by the [[singleton]] map.  So in the arithmetic of [[cardinal numbers]], we have
$$ {|S|} \leq {|\mathcal{P}S|} .$$
But as there is no such surjection, there certainly is no [[bijection]], and we have
$$ {|S|} \ne {|\mathcal{P}S|} .$$
So we conclude that
$$ {|S|} \lt {|\mathcal{P}S|} .$$
That is, each set is strictly smaller in cardinality than its power set.

This interpretation relies on a good relationship between $\leq$ and $=$ on the class of cardinal numbers; in particular, the Cantor--Schroeder--Bernstein theorem that $\leq$ is [[antisymmetric relation|antisymmetric]].  In [[constructive mathematics]], this relationship is lacking, and it is quite possible for two sets to each be strictly smaller than each other in the sense above.  Thanks to Theorem \ref{taylor}, this is not possible for a set and its power set, but it does mean that the interpretation of $\lt$ as relative size is problematic ---indeed almost as problematic as the idea that there are fewer even integers than integers!

[[Paul Taylor]] has argued that the essential value of Cantor\'s Theorem is the lemma, implicit in Cantor\'s proof, that [[Bill Lawvere]] isolated as Theorem \ref{lawvere}.  As the main interpretation of Theorem \ref{cantor} is meaningful only in a specific set-theoretic context (particularly, one where the Cantor--Schroeder--Bernstein theorem holds), it may not survive a 'revolution' that overthrows the primacy of that context.  But Lawvere\'s lemma will survive, since it 'does the work' while Cantor\'s theorem 'takes the credit'.  (See [Taylor 2009](#Taylor2009) below for further discussion of 'Lemmas that do the work and Theorems that take the credit'.)

## In posets 

A theorem analogous to Cantor's theorem for sets can be formulated for other [[cartesian closed categories]]. In particular, one may ask whether it is possible to have a surjection $X \to 2^X$ between posets, where the base $2$ is not the discrete poset $\{0, 1\}$ but rather the order $\{0 \leq 1\}$. 

The answer is there is no such surjection $f: X \to 2^X$, but this does not follow from a simple application of Lawvere's fixed-point theorem, where one tries to rule out such $f$ by invoking existence of a map $2 \to 2$ that has no [[fixed point]] (there is no such poset map $2 \to 2$!). Nor can we appeal to some crude cardinality argument; for example, if $X$ is the ordinal $\omega$, then $2^X$ is the order $\bot \sqcup \omega^{op}$ (freely adjoin a bottom element $\bot$ to $\omega^{op}$), which has the same cardinality. So some other proof must be sought. 

Proving there is no surjection $X \to 2^X$ is an amusing exercise. One line of attack (which internalizes to any topos) may be found [here](https://ncatlab.org/toddtrimble/published/Cantor's+theorem+for+posets). 



## Related concepts

* [[Lawvere's fixed point theorem]]

## References

*  Taylor 2009 June 20:  On the categories mailing list, Message-ID [E1MJ5TV-00066b-BI@mailserv.mta.ca](http://www.mta.ca/~cat-dist/archive/2009/09-6).
   {#Taylor2009}

*  On constructivenews, a [discussion](https://groups.google.com/group/constructivenews/browse_thread/thread/5f65c7ac479c15dd) about Theorem \ref{taylor} in the case where $S$ and $V$ are both the set of [[natural numbers]].  (Apparently this fails in certain [[realizability topos]]es.)


[[!redirects Cantor theorem]]
[[!redirects Cantor Theorem]]
[[!redirects Cantor's theorem]]
[[!redirects Cantor's Theorem]]
[[!redirects Cantor's theorem]]
[[!redirects Cantor's Theorem]]
[[!redirects cantor theorem]]
[[!redirects cantor Theorem]]
[[!redirects cantor's theorem]]
[[!redirects cantor's Theorem]]
[[!redirects cantor's theorem]]
[[!redirects cantor's Theorem]]
