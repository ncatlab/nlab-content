Georg Cantor proved many theorems, but the one usually called _Cantor\'s theorem_ is the first nontrivial theorem of Cantor\'s new [[set theory]]: that some infinities are bigger than others; in particular, any infinite [[cardinal number]] (or [[infinite set]]) generates a larger one by taking the [[power set]].

Note that the theorem applies to all sets, not just infinite ones, although it\'s fairly obvious for [[finite set]]s.

Cantor\'s theorem should not be confused with the Cantor--Schroeder--Bernstein theorem (see [[cardinal number]]), which is important to justify Cantor\'s interpretation.

# History #

Prior to Cantor, people tended to think of infinity (whether they believed in it or not) as an absolute concept: all infinities are equivalent.  It had been noticed (by Galileo, for example) that it\'s possible to give an [[infinite set]] a self-[[injection]] that was not a [[surjection]]; for example, the inclusion of the even integers into the integers by doubling.  Thus here are two infinities &#8212;the infinity $E$ of even integers and the infinity $N$ of all integers&#8212; that are actually equivalent, even though at first glance it would appear that $E$ is smaller.

Cantor showed that such an equivalence *fails* with the [[real number]]s $R$: no map from $N$ to $R$ can be surjective (so that $R$ is _uncountable_).  His first argument was ad hoc, but he then generalised this with the _diagonal arugment_ to show that no map from any set $S$ to its [[power set]] $\mathcal{P}S$ could be surjective.  (This covered the uncountability of $R$, since Cantor found a [[bijection]] between $R$ and $\mathcal{P}N$.)  As there is an obvious injective map (the [[singleton]] map) from $S$ to $\mathcal{P}S$, Cantor concluded that the cardinality of the one is strictly smaller than the cardinality of the other.

Cantor\'s argument, like his whole set theory, was controversial at the time.  Those who, like Kronecker, believed that all mathematics should be [[finite mathematics]], considered it meaningless.  Even more moderate early [[constructive mathematics|constructivists]], such as Brouwer and Weyl, found that it had little point.  (In particular, it says nothing directly about $R$, since the bijection between $R$ and $\mathcal{P}N$ is not constructively valid.)

However, the versions of the theorem stated below are constructively valid, and Theorem \ref{general} is even [[predicative mathematics|predicatively]] valid (as long as one has [[function set]]s); modern constructivists generally accept these as theorems.  (The interpretation, however, is not so clear.)  They are in fact theorems in the [[internal logic|internal language]] of any [[topos]] (and Theorem \ref{general} is a theorem in any $\Pi$-[[pretopos]]).

# Statements and proofs #

+--{: .num_theorem #general}
###### Theorem
(General version.)
Given sets $S$ and $V$, let $n: V \to V$ be a map with no fixed points; that is, $n(x) \ne x$ for all $x: V$.  Then there is no [[surjection]] from $S$ to the [[function set]] $S \to V$ (also written $V^S$).
=--

+--{: .proof}
###### Proof
Let $f: S \to (S \to V)$ be any function, and consider the function $g: S \to V$ given by
$$ g(a) = n(f(a)(a)) .$$
That is, if one uses [[internal hom|currying]] to interpret $f$ as a function from $S \times S$ to $V$, then $g$ is defined using the diagonal map $\Delta_S$ as
$$ S \stackrel{\Delta_S}\to S \times S \stackrel{f}\to V \stackrel{n}\to V .$$

Now suppose that $f$ is surjective.  Then there must be some element $a: S$ such that $f(a) = g$.  But then
$$ g(a) = n(f(a)(a)) = n(g(a)) ,$$
which is impossible, as $n$ has no fixed points.  Therefore, no such surjection exists.
=--

The presence of the diagonal map $\Delta_S$ here explains why this proof is called the _diagonal argument_.  (This is anachronistic but morally correct.)

As the theorem states that something is impossible, this proof by contradiction is constructively valid.  In fact, the result is slightly stronger than (but classically equivalent to) the failure of $f$ to be a surjection: there actually exists an element $g$ of $S \to V$ that is not equal to any value in the range of $f$.  (If $V$ has an [[apartness relation]], then you can get an even stronger result for a correspondingly stronger hypothesis on $n$, but that doesn\'t apply to the versions below.)

+--{: .num_theorem #cantor}
###### Theorem
(Cantor\'s version.)
Given a set $S$, there is no surjection from $S$ to the [[power set]] $\mathcal{P}S$.
=--

+--{: .proof}
###### Proof
Let $V$ be the set of [[truth value]]s, and let $n: V \to V$ be [[negation]].  Now apply Theorem \ref{general}.
=--

Note that although negation doesn\'t have all of its usual properties in constructive mathematics, $p = \neg{p}$ is still impossible.

The next version is classically equivalent to the previous version (at least if you check that $\mathcal{P}S$ is [[inhabited set|inhabited]]), but not constructively.  (Indeed, unlike Theorem \ref{general}, it apparently has no constructive analogue when $\mathcal{P}S$ is replaced by $V^S$.)  This argument is from Proposition 2.8.8 of Paul Taylor\'s [[Practical Foundations]] (although I don\'t know if it really originated there).


+--{: .num_theorem #taylor}
###### Theorem
(Taylor\'s version.)
Given a set $S$, there is no [[injection]] from $\mathcal{P}S$ to $S$.
=--

+--{: .proof}
###### Proof
Let $i: \mathcal{P}S$ to $S$ be any function.  Define $f: S \to \mathcal{P}S$ as follows:
$$ f(a) = \{ b: S \;|\; \forall (U: \mathcal{P}S),\; i(U) = a \;\Rightarrow\; b \in U \} .$$
If $i$ is an injection, then $f$ is a [[retraction]] of $i$ and hence a surjection, which is impossible by Theorem \ref{cantor}.
=--

We can combine Theorems \ref{cantor} and \ref{taylor} into the following even more general statement, taken from D4.1.8 of the [[Elephant]].

+-- {: .num_theorem #johnstone}
###### Theorem
Given a set $S$, its power set $\mathcal{P}S$ cannot be expressed as a [[subquotient]] of $S$.
=--
+--{: .proof}
###### Proof
Suppose we had an injection $f:B\hookrightarrow S$ and a surjection $g:B \to \mathcal{P}S$.  Then $f^{-1}:\mathcal{P}S \to \mathcal{P}B$ would be a surjection, as would the [[image]] function $\exists_f: \mathcal{P}B \to \mathcal{P P}S$.  Thus their composite would be a surjection $\mathcal{P}S \to \mathcal{P P}S$, which is impossible by Theorem \ref{cantor}.
=--



# Interpretation #

Note that there exists an [[injection]] from $S$ to $\mathcal{P}S$, given by the [[singleton]] map.  So in the arithmetic of [[cardinal number]]s, we have
$$ |S| \leq |\mathcal{P}S| .$$
But as there is no such surjection, there certainly is no [[bijection]], and we have
$$ |S| \ne |\mathcal{P}S| .$$
So we conclude that
$$ |S| \lt |\mathcal{P}S| .$$
That is, each set is strictly smaller in cardinality than its power set.

This interpretation relies on a good relationship between $\leq$ and $=$ on the class of cardinal numbers; in particular, the Cantor--Schroeder--Bernstein theorem that $\leq$ is [[antisymmetric relation|antisymmetric]].  In [[constructive mathematics]], this relationship is lacking, and it is quite possible for two sets to each be strictly smaller than each other in the sense above.  Thanks to Theorem \ref{taylor}, this is not possible for a set and its power set, but it does mean that the interpretation of $\lt$ as relative size is problematic &#8212;indeed almost as problematic as the idea that there are fewer even integers than integers!