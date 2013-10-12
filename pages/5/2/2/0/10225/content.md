
# Steady functions
* table of contents
{: toc}

## Idea

A steady function is one equipped with a certain sort of "witness of [[constant function|constancy]]".  However, in [[higher category theory]] and [[homotopy theory]], it is debatable whether or not this witness really exhibits "constancy", hence the use of a different word.  (The word "steady" was suggested by [[Andrej Bauer]].)


## Definition

In [[homotopy type theory]], a function $f:A\to B$ is **steady** if we have a term of type
$$ \prod_{(x,y:A)} (f x = f y). $$
By regarding homotopy type theory as the [[internal logic]] of an [[(∞,1)-topos]], we obtain a definition that makes sense in any higher category with binary products: a morphism $f:A\to B$ is **steady** if the two composites $A\times A \rightrightarrows A \xrightarrow{f} B$ are equivalent.


## Relationship to constancy

If $f$ is [[constant function|constant]] in the sense that it factors through the [[terminal object]] (i.e. we have $f = \lambda x. b$ for some $b:B$), then $f$ is obviously steady.  The converse holds if we know that the domain $A$ is [[inhabited type|inhabited]], for if $a_0:A$, then $f a = f a_0$ for all $a:A$.  However, the [[identity function]] of the [[empty type]] is steady, yet not equal to $\lambda x.b$ for any $b:\emptyset$ (since no such $b$ exists).

More generally, if $f$ factors through the [[propositional truncation]] ${\|A\|}$, then it is steady, since any two elements of ${\|A\|}$ are equal (i.e. it is an [[h-proposition]]).  In fact, this is true if $f$ factors through *any* h-proposition (in which case it in fact also factors through ${\|A\|}$, by the universal property of the latter).

The converse to this last implication does hold for some specific $f:A\to B$, such as:

* If $B$ is an [[h-set]].  For then $f$ factors through the 0-truncation ${\|A\|_0}$, and the set-[[coequalizer]] of the two projections ${\|A\|_0} \times {\|A\|_0} \to {\|A\|_0}$ is the propositional truncation.

* If $A$ has [[split support]].  For then we have a composite ${\|A\|} \to A \xrightarrow{f} B$, whose restriction to $A$ is equal to $f$ by steadiness.

* If $A=P+Q$, with $P$ and $Q$ h-propositions.  For then ${\|A\|}$ is the [[join]] $P*Q$ of $P$ and $Q$, i.e. the [[pushout]] of the two projections $P \leftarrow P\times Q \to Q$.  The universal property of this pushout says exactly that any steady map $P+Q\to B$ factors through $P*Q = \Vert P+Q\Vert$.

* If $A=B$ (see below).

However, it can fail in general, even when $A$ is [[mere proposition|merely]] inhabited (i.e. ${\|A\|}= 1$).  For instance, let $A=P+Q+R$ for h-propositions $P$, $Q$, and $R$, and let $B$ be the triple pushout of $P$, $Q$, and $R$ under $P\times Q$, $P\times R$, and $Q\times R$.  Then there is a steady map $f:A\to B$, but there exist models in which ${\|A\|} = 1$ but $B$ has no [[global element].  The most straightforward such model is [[presheaves]] on the [[poset]] of proper [[subsets]] of $\{a,b,c\}$, with $P=\{a,b\}$, $Q=\{b,c\}$, and $R=\{a,c\}$.  In this model, we have $B(S) = 1$ for all nonempty proper subsets $S$, while $B(\emptyset) = S^1$, and $B$ has no global sections.

See [this discussion](https://groups.google.com/d/msg/homotopytypetheory/FeBAScTgwzg/Dx6E3-ezdxIJ).

In general, being steady may be regarded as an "incoherent approximation" to constancy in the sense of factoring through an h-proposition.  Indeed for a set $A$, its propositional truncation is the set-coequalizer of $A\times A\rightrightarrows A$.  However, in general such a construction requires the realization of a whole simplicial diagram (the simplicial kernel of the map $A\to 1$).


## Steady endomaps

While an arbitrary steady function is not very coherent, a steady [[endofunction]] $f:A\to A$ has some extra degree of "coherence", as witnessed by the following results of [(KECA)](#KECA).

+-- {: .un_lemma}
###### Lemma
If $f:A\to A$ is steady, then the type $Fix(f) \coloneqq \sum_{x:A} (f x = x)$ is an h-proposition, and equivalent to ${\|A\|}$.
=--
+-- {: .proof}
###### Proof
Suppose $H: \prod_{(x,y:A)} (f x = f y)$, and let $(a,p),(b,q):Fix(f)$; we want to show $(a,p)=(b,q)$.  Let $r:a=b$ be the concatenated path
$$ a \xrightarrow{p^{-1}} f a \xrightarrow{H_{a,a}^{-1}} f a \xrightarrow{H_{a,b}} f b \xrightarrow{q} b. $$
It will suffice to show that $p \bullet r = ap_f(r) \bullet q$, where $ap_f$ denotes the action of $f$ on paths.  However, the dependent action of $H$ on paths implies that $H_{x,y} \bullet ap_f(s) = H_{x,y'}$ for any $x:A$ and any $s:y=y'$, and in particular $ap_f(r) = H_{a,a}^{-1} \bullet H_{a,b}$.  From this $p \bullet r = ap_f(r) \bullet q$ is immediate.  Thus, $Fix(f)$ is an h-proposition.

Now we have a map $g:A\to Fix(f)$ defined by $g(x) \coloneqq (f x, H_{f x,x})$, so by the universal property of ${\|A\|}$, we have ${\|A\|} \to Fix(f)$.  On the other hand, we have the first projection $pr_1:Fix(f) \to A$, and hence $Fix(f) \to {\|A\|}$.  Thus, these two h-propositions are equal.
=--

+-- {: .un_theorem}
###### Theorem
A type $A$ has [[split support]] if and only if it admits a steady endomap $f:A\to A$.
=--
+-- {: .proof}
###### Proof
Given ${\|A\|} \to A$, the composite $A\to {\|A\|} \to \A$ is steady.  Conversely, if $f$ is steady, $Fix(f) = {\|A\|}$ by the lemma, so $pr_1:Fix(f) \to A$ splits the support of $A$.
=--

Note that $pr_1 \circ g = f$, so that if we start with a steady endomap of $A$, deduce a splitting of the support of $A$, and then reconstruct a steady endomap, we obtain the same map.  However, the proof of steadiness is generally different from the one we began with, so this "logical equivalence" is not an equivalence of types.

+-- {: .un_cor}
###### Corollary
A type $A$ is an [[h-set]] if and only if every identity type $x=_A y$ admits a steady endomap.
=--
+-- {: .proof}
###### Proof
We know that $A$ is an h-set just when all $x=_A y$ have split support.
=--


## References

* [[Nicolai Kraus]] and [[Martin Escardo]] and [[Thierry Coquand]] and [[Thorsten Altenkirch]], "Generalizations of Hedberg's theorem", M. Hasegawa (Ed.): TLCA 2013, LNCS 7941, pp. 173-188. Springer, Heidelberg 2013. [PDF](http://www.cs.bham.ac.uk/~mhe/papers/hedberg.pdf).  In this paper, steady functions are called "constant".
 {#KECA}


[[!redirects steady function]]
[[!redirects steady functions]]
