
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[sheaf]] $F$ of [[set]]s on (the [[category of open subsets]] of) a [[topological space]] $X$ is __flabby__ (flasque) if for any open subset $U\subset X$, the restriction morphism $F(X)\to F(U)$ is [[surjection|onto]]. Equivalently, for any open $U\subset V\subset X$ the restriction $F(V)\to F(U)$ is surjective. In mathematical literature in English, the original French word __flasque__ is still often used instead of flabby here. 

The concept generalizes in a straightforward manner to flabby sheaves on [[locale]]s.


## Properties

* Flabbiness is a local property: if $F|_U$ is flabby for every sufficiently small open subset, then $F$ is flabby.
* Given a continuous map $f:X\to Y$ and a flabby sheaf $F$ on $X$, the [[direct image]] sheaf $f_* F : V\mapsto F(f^{-1}V)$ is also flabby.
* Any [[exact sequence]] of sheaves of [[abelian groups]] $0\to F_1\to F_2\to F_3\to 0$ in which $F_1$ is flabby, is also an exact sequence in the category of presheaves (the exactness for stalks implies exactness for groups of sections over any fixed open set). As a corollary, if $F_1$ and $F_2$ are flabby, then $F_3$ is flabby; and if $F_1$ and $F_3$ are flabby, so is $F_2$.


## Examples

An archetypal example is the sheaf of all set-theoretic (not necessarily continuous) [[sections]] of a [[bundle]] $E\to X$; regarding that every sheaf over a topological space is the sheaf of sections of an [[etale space]], every sheaf can be embedded into a flabby sheaf $C^0(X,F)$ defined by

$$
U \mapsto \prod_{x\in U} F_x
$$

where $F_x$ denotes the [[stalk]] of $F$ at point $x$. This construction assumes that all stalks $F_x$ are inhabited, and also that the law of excluded middle is available. In the absence of either, the refined construction

$$
U \mapsto \prod_{x\in U} P_{\leq 1}(F_x)
$$

works, where $P_{\leq 1}(F_x)$ is the set of [[subsingleton]]s of $F_x$.


## Characterization using the internal language

+-- {: .num_prop}
###### Proposition

Let $F$ be a sheaf on a topological space (or [[locale]]) $X$. Then the following statements are equivalent.

1. $F$ is flabby.
2. For any open subset $U \subseteq X$ and any section $s \in F(U)$ there is an open covering $X = \bigcup_i V_i$ such that, for each $i$, there is an extension of $s$ to $U \cup V_i$ (that is, a section $s' \in F(U \cup V_i)$ such that $s'|_U = s$).
 (If $X$ is a space instead of a locale, this can be equivalently formulated as follows: For any open subset $U \subseteq X$, any section $s \in F(U)$, and any point $x \in X$, there is an open neighbourhood $V$ of $x$ and an extension of $s$ to $U \cup V$ (that is, a section $s' \in F(U \cup V)$ such that $s'|_U = s$).)

3. From the point of view of the [[internal language]] of the [[topos]] of sheaves over $X$, for any [[subsingleton]] $K \subseteq F$ there exists an element $s : F$ such that $s \in K$ if $K$ is [[inhabited]]. More precisely,
$$ Sh(X) \models
  \forall K \subseteq F.
  (\forall s,s':K. s = s') \Rightarrow \exists s:F.
  (K \text{ is inhabited} \Rightarrow s \in K). $$
4. The canonical map $F \to \mathcal{P}_{\leq 1}(F), s \mapsto \{s\}$ is [[final functor|final]] from the internal point of view, that is
$$ Sh(X) \models
  \forall K : \mathcal{P}_{\leq 1}(F).
  \exists s : F.
  K \subseteq \{s\}. $$
Here $\mathcal{P}_{\leq 1}(F)$ is the object of subsingletons of $F$.

=--

+-- {: .proof}
###### Proof

The implication "1 $\Rightarrow$ 2" is trivial. The converse direction uses a typical argument with [[Zorn's lemma]], considering a maximal extension.
The equivalence "$2 \Leftrightarrow 3$" is routine, using the [[Kripke-Joyal semantics]] to interpret the internal statement. We omit details for the time being.
Condition 4 is a straightforward reformulation of condition 3.

=--

For a more detailed discussion, see [Blechschmidt](#Blechschmidt18).

+-- {: .num_remark}
###### Remark

Condition 2 of the proposition is, unlike the standard definition of flabbiness given at the top of the article, manifestly local. Also the equivalence with condition 3 and condition 4 is [[intuitionistic logic|constructively valid]]. Therefore one could consider to adopt condition 2 as the definition of flabbiness.

=--

+-- {: .num_remark}
###### Remark

The object $\mathcal{P}_{\leq 1}(F)$ of subsingletons of $F$ can be interpreted as the object of [[partial map classifier|"partially-defined elements"]] of $F$. The sheaf $F$ is flabby if and only if any such partially-defined element can be refined to an honest element of $F$.

=--

## Related concepts

* [[sheaf]]

* [[abelian sheaf cohomology]]

  * [[soft sheaf]]

  * [[fine sheaf]]

  * **flabby sheaf**

## References

Flabby sheaves were probably first studied in [[Tohoku]], where flabby [[resolution]]s were also considered. A classical reference is 

* {#Godement58} [[Roger Godement]] _Topologie Algébrique et Théorie des Faisceaux_. Actualités Sci. Ind. No. 1252. Publ. Math. Univ. Strasbourg. No. 13 Hermann, Paris 1958.

See also

* [[Günter Tamme]], section I 3.5 of _[[Introduction to Étale Cohomology]]_
* [wikipedia](https://en.wikipedia.org/wiki/Injective_sheaf#Flasque_or_flabby_sheaves)
* [EOM](https://www.encyclopediaofmath.org/index.php/Flabby_sheaf)

Work relating flabby sheaves to the internal logic of a topos include:

* [[Anders Kock]], _Algebras for the Partial Map Classifier Monad_, in Category Theory. Proceedings of the International Conference held in Como, Italy, July 22–28, 1990, [pdf](http://home.math.au.dk/kock/jonna5.pdf)

* {#Blechschmidt18} [[Ingo Blechschmidt]], *Flabby and injective objects in toposes*, [arXiv:1810.12708](https://arxiv.org/abs/1810.12708)

* {#Escardo19} [[Martin Escardo]], *Injectives types in univalent mathematics*, [arxiv:1903.01211](https://arxiv.org/abs/1903.01211)

category: sheaf theory


[[!redirects flasque sheaf]]
[[!redirects flabby sheaves]]
[[!redirects flasque sheaves]]
