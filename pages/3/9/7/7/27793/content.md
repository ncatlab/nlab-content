
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition 

A *band* is a [[semigroup]] in which every element is [[idempotent]]. 

## Order structures on bands 

There are two distinct order structures on bands, referred to in the literature by the "natural poset" structure and the "natural preorder" structure. 

The natural preorder structure is defined by declaring $x \preceq y$ iff $x = x y x$. This is indeed a preorder by the following result. 

\begin{theorem} 
The relation $\preceq$ is reflexive and transitive. 
\end{theorem}

\begin{proof} 
(This proof appears in a relevant MathStackExchange [discussion](https://math.stackexchange.com/a/5074668/43208).) Reflexivity is obvious from $x = x x = x x x$. Transitivity follows from the following argument: let $A$ denote an instance of associativity and $I$ an instance of idempotency. From $x y x = x$ (condition 1) and $y z y = y$ (condition 2), we have 

$$x =_1 x y x =_2 x y z y x =_I x y(z y x)(z y x) =_A x(y z y)x z y x =_2 x y x z y x =_1 x z y x\qquad(P).$$

Then 
$$x z x =_P x z(x z y x) =_A (x z)(x z)y x =_I x z y x =_P x$$

which completes the proof. 
\end{proof} 

As is the case with any preorder structure, there is an associated equivalence relation $\sim$, where $x \sim y$ iff the two conditions $x \preceq y$ and $y \preceq x$ hold. 

\begin{proposition} 
Every $\sim$-equivalence class is a [[rectangular band]]. 
\end{proposition} 

\begin{proof} 
Let $[x]$ denote the equivalence class of $x$. If $y, z \in [x]$, then $x y x = x$, and also $y z y = y$ (since $y \sim z$), so by equation $P$ above, $x z y x = x$. By the same token, since $x, y, z$ are all equivalent, we can equally well say $z y x z = z$, whence $(z y)x(z y) = z y$. From these two conclusions, it follows that $z y$ is also in $[x]$, so that each equivalence class $[x]$ is closed under multiplication, and therefore is a band. 

The rectangularity condition is immediate by definition: for any $\sim$-equivalent elements $x, y$, we have $x = x y x$. 
\end{proof} 

## Examples of bands 

* A [[semilattice]] (in this article, we mean semilattices without identity) is the same thing as a [[commutative]] band. 

* An [[idempotent monoid]] is a [[unital magma|unital]] [[band]]. 

* A [[rectangular band]] is a band (see there). 

* A [[skew lattice]] $(L, \wedge, \vee)$ is a band, using either $\wedge$ or $\vee$ as the semigroup operation. 

* A [[Boolean ring]] is a [[ring]] whose multiplication operation is a band. 

* Similarly, a [[multiplicatively idempotent semiring]] is a [[semiring]] whose multiplication operation is a band. 

* An [[additively idempotent semiring|idempotent semiring]] is a [[semiring]] whose addition operation is a band. 

To be added: varieties of bands, and particularly of regular bands. 

* A *split band* is defined in definition 1.1 of [McAlister & Blyth 1978](#MB78). 

## Relation to semilattices 

The category of semilattices is a full subcategory of the category of bands; by general categorical considerations, the full inclusion has a left adjoint, called the [[reflector]] from bands to semilattices. 

The following result, due to Clifford and Preston, is fundamental. 

\begin{theorem} 
Given a band $B$, the equivalence relation induced from the natural preorder, where $x \sim y$ iff $(x \preceq y) \wedge (y \preceq x)$, is a band [[congruence]]. The quotient $B/\sim$ is a semilattice, and $B \to B/\sim$ is universal among all maps from $B$ to semilattices, thus defining the reflector $B \mapsto B/\sim$ from bands to semilattices. 
\end{theorem} 

## Properties of bands 

By a theorem of [McLean](#McLean54), finitely generated bands are finite; see [Howie 76, Section IV.4](#Howie76).

### Relation to rectangular bands

* Every [[rectangular band]] is a [[band]] since the defining identity implies $ x y z = x z$ for all $x,y,z$ whence by taking $y=z=x$ one gets $x x x = x x$ and from the defining identity $x x x=x$ hence $x x = x$. In order to get the first equation expand $x y z$ by substituting $ x z x$ for $x$: $x y z = (x z x) y z = x (z (xy) z) = x z \; .$

* Every [[band]] $S$ has a decomposition as a [[disjoint union]] $\coprod_{x\in L} R_x$ where $L$ is a semilattice, each $R_x$ is a [[subobject|sub]]-semigroup that is a rectangular band, and $R_x R_y \subseteq R_{x y}$ for every $x$ and $y$. This is a bit weaker than saying we have a [[functor]] from the [[poset]] $L$ to the [[category]] of rectangular bands, because we lack connecting morphisms $R_x \to R_y$.

### Regular bands

A band $S$ satisfying the [[graphic category| graphic identity]] $x y x = x y$ for all $x$ and $y$ is said to be _left-regular_. Left-regular bands can arise from hyperplane arrangements and there has been work studying [[random walk|random walks]] on these hyperplane arrangements by analysing the semigroup algebras of the associated bands: see [Brown 00](#Brown00) and [Margolis-Saliola-Steinberg 15](#MargolisSaliolaSteinberg15). Left-regular band monoids are also called _graphic monoids_ which are examples of 1-object [[graphic category|graphic categories]].

### Skeletons and split bands

For the definition of a skeleton of a band, see definition 1.2 of [McAlister & Blyth 1978](#MB78) for the time being...

But according to lemma 1.3 of [McAlister & Blyth 1978](#MB78), a band is split [[if and only if]] it has a skeleton. 

## Related concepts

* [[semigroup]]

* [[semilattice]]

* [[idempotent monoid]]

* [[Boolean ring]]

## References

* {#McLean54} David McLean, _Idempotent Semigroups_, The American Mathematical Monthly, Vol. 61, No. 2 (February 1954), pp. 110-113. 

* {#Howie76} J. Howie, _An introduction to semigroup theory_, Academic Press 1976.

* {#Brown00} K. S. Brown, _Semigroups, Semirings, and Markov Chains_, J. Theor. Prob. **13** no.3 (2000) pp.871-938. ([arXiv:math/0006145](https://arxiv.org/abs/math/0006145))

* {#MargolisSaliolaSteinberg15}  Stuart Margolis, Franco Saliola, [[Benjamin Steinberg]], _Cell complexes, poset topology and the representation theory of algebras arising in algebraic combinatorics and discrete geometry_ ([arXiv:1508.05446](https://arxiv.org/abs/1508.05446))

Split bands and the skeleton of a band are defined in:

* {#MB78} [[Donald McAlister]], [[Tom Blyth]], *Split orthodox semigroups*, Journal of Algebra, Volume 51, Issue 2, April 1978, Pages 491-525, &lbrack;<a href="https://doi.org/10.1016/0021-8693(78)90118-7">doi:10.1016/0021-8693(78)90118-7</a>]&rbrack;

* {#HCG22} Kaiqing Huang, Yizhi Chen, Aiping Gan, *Structure of split additively orthodox semirings*, AIMS Mathematics, 2022, 7(6): 11345-11361. &lbrack;[doi: 10.3934/math.2022633](https://doi.org/10.3934/math.2022633), [pdf](https://www.aimspress.com/aimspress-data/math/2022/6/PDF/math-07-06-633.pdf)&rbrack;

See also

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Band_(algebra)">Band (algebra)</a>*

[[!redirects band]]
[[!redirects bands]]

[[!redirects idempotent semigroup]]
[[!redirects idempotent semigroups]]

[[!redirects split band]]
[[!redirects split bands]]

[[!redirects skeleton of a band]]
[[!redirects skeleta of a band]]
