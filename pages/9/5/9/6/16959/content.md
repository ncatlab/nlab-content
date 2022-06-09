
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--
 
#Contents#
* table of contents
{:toc}
 
## Idea
 
The join $X \star Y$ of topological spaces $X$ and $Y$ consists of $X$, $Y$, and [[convex set|convex combinations]] of a point of $X$ and a point of $Y$ (with some suitable topology).
 
## Definition
 
+-- {: .num_defn #PushoutJoin}
###### Definition
 
Write $I \coloneqq [0,1]$ for the unit [[interval]], regarded as a [[topological space]].
 
For $X,Y $ two [[topological spaces]], the [[join]] $X \star Y$ is the [[colimit]] in [[Top]] of the [[diagram]]
 
$$
  \array{
   & & X \times Y & & & & X \times Y & & 
   \\
   & \mathllap{\pi_1} \swarrow & & \searrow \mathrlap{i_0} & & \mathllap{i_1} \swarrow & & \searrow \mathrlap{\pi_2} & 
   \\ 
   X & & & & X \times I \times Y & & & & Y
}
$$ 
 
where $i_0$ is the inclusion $(x, y) \mapsto (x, 0, y)$, and $i_1$ is the inclusion $(x, y) \mapsto (x, 1, y)$. 
 
=--
 
(This in turn, by the discussion at _[[mapping cone]]_, is a model for the [[homotopy type]] of the [[homotopy pushout]] of the two projections $X \leftarrow X \times Y \to Y$.)
 
Intuitively, $X \star Y$ is the union of all line segments connecting $X$ to $Y$ when these are placed in general position in an ambient [[Euclidean space]]. 
 
The join is [[monoidal category|associative]]; intuitively, a join of three spaces $X, Y, Z$ is the union of 2-[[simplices]] whose vertices lie in $X, Y, Z$ respectively when these are placed in general position. Thus the join endows $Top$ with a [[monoidal category]] structure whose unit is the empty space. 
 
## Milnor’s join construction
 
There is another topology on the join of spaces, due to [[John Milnor|Milnor]], which appears in his [[Milnor construction|construction of universal bundles]]. ([Milnor 1956, section 2](#Milnor1956))
 
+-- {: .num_defn #MilnorJoin }
###### Definition
 
Milnor’s join $X \overline{\star} Y$ has the same underlying set as $X \star Y$ and the coarsest topology which makes $t \colon X \overline{\star} Y \to [0,1]$ (given on $X \times I \times Y$ by $(x,t,y)\mapsto t$, constantly $0$ on $X$, and constantly $1$ on $Y$) and the projections $\pi_1 \colon t^{-1}([0,1)) \to X$ and $\pi_2 \colon t^{-1}((0,1]) \to Y$ continuous.
 
If $p\colon X \to S$ and $p\colon Y \to S$ are spaces over $S$, then their _fibrewise join_ or _Whitney sum_ $X \overline{\star}_S Y$ is the space $\{ x \in X \overline{\star} Y : t(x) \in (0,1) \implies p(\pi_1(x))=q(\pi_2(y)) \}$.
 
=--
 
The inclusions $X \hookrightarrow X \overline{\star} Y$ and $Y \hookrightarrow X \overline{\star} Y$ are [[Hurewicz cofibration|closed Hurewicz cofibrations]]: the open set $t^{-1}[[0,1)]$ deforms onto $X$ and $t^{-1}[(0,1]]$ deforms onto $Y$.
 
\begin{proposition} The identity map $X \star Y \to X \overline{\star} Y$ is a homotopy equivalence. If $X$ and $Y$ are compact, then it is a homeomorphism.
\end{proposition}
(See [Fritsch–Golasiński 2004, section 1](#FG2004))
 
\begin{proposition}\label{FibrewiseJoinOfFibrationsIsFibration}
If $p \colon X \to S$ and $q \colon Y \to S$ are [[Hurewicz fibration|Hurewicz fibrations]], then so is $X \overline{\star}_S Y \to S$
\end{proposition}
(See [Hall 1965](#Hall1965), [Lemmens 1970, theorem I](#Lemmens1970))
 
## Examples 
 
+-- {: .num_example } 
###### Example 
 
The join of any topological space $X$ with the [[point]] is the [[cone]] on $X$:
 
$$
  X \star 1 =  C X
  \,.
$$
 
=--
 
 
+-- {: .num_example #JoinWith0Sphere} 
###### Example 
 
The join of any topological space $X$ with the [[0-sphere]] $S^0$
is the [[suspension|(unreduced) suspension]] of $X$:
 
$$
  X \star S^0 \cong S X
  \,.
$$
 
=--
 
+-- {: .num_example } 
###### Example 
 
The join of [[n-spheres]] with each other is
 
$$ 
  S^m \star S^n \cong S^{m+n+1}
$$
 
=--
 
+-- {: .num_example} 
###### Example 
For $X = S^1, Y = S^1$, we may consider $X$ to consist of [[quaternions]] $a + b i$ and $Y$ to consist of quaternions $c j + d k$ such that $a^2 + b^2 = 1 = c^2 + d^2$. Then $X$ and $Y$ are in general position in $\mathbb{H} \cong \mathbb{R}^4$ with respect to each other, and the quotient map 
 
$$X \times I \times Y \to S^3$$ 
 
$$\,$$
 
$$(a + b i, t, c + d i) \mapsto t^{1/2}(a + b i) + (1 - t)^{1/2}(c + d i)$$ 
 
is an explicit realization of the [[unit sphere]] $S^3$ as $X \star Y$. 
=-- 
 
+-- {: .num_example} 
###### Example 
For a topological group $G$, the [[Milnor construction]] of the total space $E G$ of the [[classifying space|classifying bundle]] is an iterated join, i.e., the colimit of a diagram of inclusions 
 
$$G \to G \overline{\star} G \to G \overline{\star} G \overline{\star} G \to \ldots$$ 
 
where the identity element of $G$ is used to embed each $G^{\bar \star n}$ into its successor $G^{\bar \star (n+1)}$. The idea is that passing to higher joins kills off more and more lower-dimensional [[homotopy groups]], until one reaches the colimit which is then weakly contractible. 
 
The same idea applies to a general space $X$; an $H$-space structure and higher homotopy associativities (collectively embodied in a structure of algebra over the [[associahedron|Stasheff operad]]) may be used to build a classifying bundle in iterative fashion, with the [[Hopf construction]] giving the first stage of the iteration. 
=-- 
 
+-- {: .num_example} 
###### Example 
If $p \colon X \to Y$ is a fibration, then $p$ factors as a [[Hurewicz cofibration]] $X \hookrightarrow X \overline{\star}_Y Y$ followed by an [[acyclic fibration|acyclic]] [[Hurewicz fibration]] $X \overline{\star}_Y Y \to Y$ by proposition \ref{FibrewiseJoinOfFibrationsIsFibration}: the embedding $Y \hookrightarrow X \overline{\star}_Y Y$ and retraction $X \overline{\star}_Y Y \to Y$ exhibit $Y$ as a strong deformation retract of $X \overline{\star}_Y Y$.
 
(This fact is used in Strøm’s construction of his [[Strøm model structure|model structure on topological spaces]].)
 
=-- 
 
## Related concepts
 
* [[suspension]]
 
* [[Hopf construction]]

* [[join type]]
 
* [[join of simplicial sets]], 
 
* [[join of categories]], [[join of quasi-categories]]
 
## References

* {#Hall1965} I.M. Hall, _The generalized Whitney sum_, The Quarterly Journal of Mathematics 16(4): 360–384, December 1965. [10.1093/qmath/16.4.360](https://doi.org/10.1093/qmath/16.4.360)

* {#Lemmens1970} P.W.H. Lemmens, _A note on the join of fibrations_, Indagationes Mathematicae 73: 53–56 (1970) [doi:10.1016/S1385-7258(70)80008-7](https://doi.org/10.1016/S1385-7258%2870%2980008-7)
 
* {#Milnor1956} [[John Milnor]], _Construction of Universal Bundles_, _II_, Ann. of Math. __63__:3 (1956) 430-436, [doi:10.2307/1970012](https://doi.org/10.2307/1970012)
 
Discussion of relation to homotopy limits etc.
 
* Jean-Paul Doeraene, _Homotopy pull backs, homotopy push outs and joins_,     Bull. Belg. Math. Soc. Simon Stevin,    Volume 5, Number 1 (1998), 15-37. [pdf on Project Euclid](https://projecteuclid.org/euclid.bbms/1103408963)
 
Comparison with other forms of join:
 
* {#FG2004}  [[Rudolf Fritsch]] and [[Marek Golasiński]], _Topological, simplicial and categorical joins_, Archiv der Mathematik 82(5):468-480, January 2004. 
 
Discussion in [[homotopy type theory]] (applied to [[n-image]] factorization) is in 
 
* {#Rijke17} [[Egbert Rijke]], _The join construction_ ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))
 
 
[[!redirects joins of topological spaces]]

