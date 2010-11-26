
# Contents
* automatic table of contents goes here
{:toc}

## Statement

The _Cantor--Schroeder--Bernstein_ theorem says that the usual [[order relation]] on [[cardinalities]] of [[set]]s is [[antisymmetric relation|antisymmetric]]. In other words, define an order on sets by $X \leq Y$ if there exists a [[monomorphism]] $f\colon X \to Y$. Then, if both $X \leq Y$ and $Y \leq X$, there exists an [[isomorphism]] of sets $X \cong Y$.

The result is really only interesting in the absence of the [[axiom of choice]] ($AC$).  With $AC$, it is a trivial corollary of the [[well-ordering theorem]].  However, the theorem actually requires only [[excluded middle]], although it does not hold in [[constructive mathematics]].


## Proof 

We prove that the Cantor--Schroeder--Bernstein theorem holds in a [[Boolean topos]]. The theorem is not however [[intuitionistic logic|intuitionistically]] valid, in that it fails in some [[topos]]es, such as the topos $Set^{\bullet \to \bullet}$ (the [[arrow category]] of $Set$).

Throughout we use ordinary [[set theory|set-theoretic]] reasoning which can be translated into the formal theory of toposes. (This can be formalized via the [[Mitchell–Benabou language]], for instance.) 

+-- {: .un_lem}
###### Lemma (Knaster--Tarski fixed-point theorem) 
Let $f\colon P X \to P X$ be an order-preserving map. Then there exists $S$ in $P X$ for which $f(S) = S$. 
=-- 

+-- {: .proof}
###### Proof 
Let $S$ be the (internal) [[intersection]] of $U = \{T \in P X : f(T) \leq T\}$. Since $S \leq T$ for every $T$ in $U$, we have $f(S) \leq f(T) \leq T$ for every $T$ in $U$. Hence $f(S) \leq S$ by definition of $S$. Applying $f$ again, we get $f f(S) \leq f(S)$. Hence $f(S)$ belongs to $U$. But then $S \leq f(S)$ by definition of $S$.
=--

+-- {: .un_remark}
###### Remark

The preceding proof is valid in _any_ topos (and so holds for $Set$ even intuitionistically). It can be seen as a special case of a result of Lambek on the [[initial algebra|initial]] [[algebra of an endofunctor]]. 
=--

+-- {: .proof}
###### Proof of Cantor--Schroeder--Bernstein

Suppose given two monos $f\colon X \to Y$, $g\colon Y \to X$. Let $\exists_f\colon P X \to P Y$ denote [[existential quantification]] along $f$, and let $\neg_X\colon P X \to P X$ denote [[negation]]. Then the composite 

$$\neg_X \exists_g \neg_Y \exists_f\colon P X \to P X$$ 

is order-preserving, and so has a fixed point $S$ by the lemma. Now define 
$h\colon X \to Y$ by the rule 

$$\array{
h(x) & = & f(x) & if x \in S \\
h(x) & = & g^{-1}(x) & if x \notin S
}$$ 

(the multi-line definition is where we use the Boolean condition). The second line makes sense because $\neg S$ is in the image of $g$. The inverse of $h$ is 

$$\array{
j(y) & = & f^{-1}(y) & if y \in \exists_f(S) \\
j(y) & = & g(y) & if y \notin \exists_f(S)
}$$

That $j$ is inverse to h uses the fact that $\neg S = \exists_g \neg \exists_f(S)$. The rest is obvious. 
=--

This classic proof is substantially the proof given in Johnstone's [[Elephant]], D4.1.11. The Boolean condition is not strictly speaking necessary, i.e., the [[principle of excluded middle]] ($EM$) does not logically follow from the Cantor--Schroeder--Bernstein statement since, for example, the latter holds vacuously (every mono is an iso) in the non-Boolean topos 

$$FinSet^C$$ 

where $C$ is any nontrivial [[finite category]]. But $EM$ is certainly the most natural supposition to make.


## In other categories

The CSB property holds in many other [[categories]] of interest, for example [[vector space]]s and [[algebraically closed field]]s. The question of when the CSB property holds was partially addressed in this [MO post](http://mathoverflow.net/questions/1058/when-does-cantor-bernstein-hold), where model-theoretic criteria come into play, sometimes under strengthenings of the notion of monomorphism (e.g., [[elementary embedding]], [[split monomorphism]]).

In [[Top]], for example, we have [[embeddings]] $\mathbb{R} \cong (0,1) \to [0,1] \to \mathbb{R}$, yet $[0,1] \ncong \mathbb{R}$.  This counterexample also shows that the CSB theorem fails in Brouwer\'s [[intuitionstic mathematics]] even for $Set$ (since every function between those sets must be continuous by Brouwer\'s continuity principle).

More examples and discussion can be found at this Secret Blogging Seminar [post](http://sbseminar.wordpress.com/2007/10/30/theme-and-variations-schroeder-bernstein/). 

In a [celebrated work](#Gowers), [[Timothy Gowers]] gave a negative solution in the case of [[Banach space]]s.


## Name

The CSB theorem was first stated by [[Georg Cantor]], but his proof relied on the [[well-ordering theorem]].  The modern (choice-free) theorem was proved (independently) by [[Felix Bernstein]] and [[Ernst Schröder]].  It has been variously named after two or three of these in almost every possible combination, although Cantor (when mentioned at all) seems always to be mentioned first.


## References 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]: A Topos Theory Conpendium_, Vol. I, Clarendon Press, Oxford (2002)

* [[Timothy Gowers]], _A Solution to the Schroeder-Bernstein Problem for Banach Spaces_, Bulletin of the London Mathematical Society, Volume 28, Issue 3 (1996), 297-304 [(abstract)](http://blms.oxfordjournals.org/content/28/3/297.abstract)
{#Gowers}


[[!redirects Cantor-Schroeder-Bernstein theorem]]
[[!redirects Cantor–Schroeder–Bernstein theorem]]
[[!redirects Cantor--Schroeder--Bernstein theorem]]
