
#Contents#
* table of contents
{:toc}

## Statement

The Cantor-Schroeder-Bernstein theorem says that the order relation on [[cardinalities]] of [[set]]s is antisymmetric. In other words, define an order on sets by $X \leq Y$ if there exists a [[monomorphism]] $f: X \to Y$. Then, if both $X \leq Y$ and $Y \leq X$, there exists an [[isomorphism]] of sets $X \cong Y$. 

## Proof 

We prove that the Cantor-Schroeder-Bernstein theorem holds in a [[Boolean topos]]. The theorem is not however intuitionistically valid, in that it fails in some [[topos]]es, such as the topos $Set^{\bullet \to \bullet}$. 

Throughout we use ordinary set-theoretic reasoning which can be translated into the formal theory of toposes. (This can be formalized via the Mitchell-Benabou language, for instance.) 

+-- {: .un_lem}
###### Lemma (Knaster-Tarski fixed-point theorem) 
Let $f: P X \to P X$ be an order-preserving map. Then there exists $S$ in $P X$ for which $f(S) = S$. 
=-- 

+-- {: .proof}
###### Proof 
Let $S$ be the (internal) intersection of $U = \{T \in PX: f(T) \leq T\}$. 
Since $S \leq T$ for every $T$ in $U$, we have $f(S) \leq f(T) \leq T$ for every $T$ in $U$. Thus $f(S) \leq S$ by definition of $S$. Applying $f$ again, we get $f f(S) \leq f(S)$. Hence $f(S)$ belongs to $U$. But then $S \leq f(S)$ by definition of $S$.
=--

**Remark:** This proof _is_ intuitionistically valid. It can be seen as a special case of a result of Lambek on the initial [[algebra of an endofunctor]]. 

+-- {: .proof}
######Proof of Cantor-Schroeder-Bernstein
Suppose given two monos $f: X \to Y$, $g: Y \to X$. Let $\exists_f: P X \to P Y$ denote existential quantification along $f$, and let $\neg_X: P X \to P X$ denote negation. Then the composite 

$$\neg_X \exists_g \neg_Y \exists_f: P X \to P X$$ 

is order-preserving, and so has a fixed point $S$ by the lemma. Now define 
$h: X \to Y$ by the rule 

$$h(x) 
\array{
= & f(x) & if x \in S \\
= & g^{-1}(x) & if x \notin S
}$$ 

(the multi-line definition is where we use the Boolean condition). The second line makes sense because $\neg S$ is in the image of $g$. The inverse of $h$ is 

$$j(y) 
\array{
= & f^{-1}(x) & if y \in \exists_f(S) \\
= & g(y) & if y \notin \exists_f(S)
}$$

That $j$ is inverse to h uses the fact that $\neg S = \exists_g \neg \exists_f(S)$. The rest is obvious. 
=--

This is substantially the proof given in Johnstone's [[Elephant]], D4.1.11. The Boolean condition is not strictly speaking necessary, i.e., the [[principle of excluded middle]] does not logically follow from the Cantor-Schroeder-Bernstein statement since, for example, the latter holds vacuously (every mono is an iso) in the non-Boolean topos 

$$FinSet^C$$ 

where $C$ is a finite category. But it is certainly the most natural supposition to make. 

## In other categories

The CSB property holds in many other categories of interest, for example vector spaces and algebraically closed fields. The question of when the CSB property holds was partially addressed in this [MO post](http://mathoverflow.net/questions/1058/when-does-cantor-bernstein-hold), where model-theoretic criteria come into play, sometimes under strengthenings of the notion of monomorphism (e.g., [[elementary embedding]], [[split monomorphism]]). 

More examples and discussion can be found at this Secret Blogging Seminar [post](http://sbseminar.wordpress.com/2007/10/30/theme-and-variations-schroeder-bernstein/). 
