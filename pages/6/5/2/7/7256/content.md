
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Introduction 

In this article, we collect some results about representable functors $C(c, -) \colon C \to V$ (where $V$ is some base of hom-enrichment) that preserve coproducts. 

When $C$ is an [[extensive category]] regarded as enriched in $Set$, we call $c$ a _[[connected object]]_, and this terminology matches well one's intuition about connectedness from familiar cases such as $C = Top$, or $C$ the category of graphs, etc. Some basic results with proofs may be found at [[connected object]], including 

* A connected colimit (i.e., a colimit over a [[connected category|connected diagram]] of) connected objects is connected. 

* If $X$ is connected and $X \to Y$ is epic, then $Y$ is connected. 

For non-extensive categories (e.g., categories of modules), the relation to "connectedness" tends to be less intuitive[^fine].  Nevertheless, the concept of (arbitrary) coproduct-preserving representable remains important, and it is useful to collect some basic information.

## Absoluteness

In an [[Ab-enriched category]], *finite* coproducts are [[absolute colimits]], hence are preserved by *every* representable.  Thus, the interest is in representables which preserve infinite coproducts as well (which is what most of this page is about).

At the other extreme from extensive categories, in a [[SupLat]]-enriched category (such as [[SupLat]] or [[Rel]]) *arbitrary* coproducts are absolute, and hence preserved by every representable.

## Module categories 

Let $\mathbf{Mod}_R$ denote the category of right modules over a ring $R$, and suppose an object $M$ induces a coproduct-preserving hom-functor $\mathbf{Mod}_R(M, -) \colon \mathbf{Mod}_R \to \mathbf{Ab}$. Various names for such $M$ appear in the literature, "compact" and "dually slender" among them. In any event, a [question arose on MathOverflow](http://mathoverflow.net/questions/59282/sums-compact-objects-f-g-objects-in-categories-of-modules) as to whether or to what extent this condition coincides with the condition of being finitely generated, for various rings $R$. 

The information provided below was mostly culled from the answers given to that question, especially those by [Pierre-Yves Gaillard](#Gaillard) and [Fernando Muro](#Muro). Here and there some minor details and background information have been filled in, and some key results have been slightly rearranged. 

### Positive results 

We begin with some easy preliminary remarks. Given a family of objects $\{B_i\}_{i \in I}$ in an $\mathbf{Ab}$-enriched category $C$ and a functor $F \colon C \to \mathbf{Ab}$, there is a canonical arrow 

$$\oplus_i F(B_i) \to F(\oplus_i B_i)$$ 

and if this arrow is an isomorphism for every family $B_i$, we say $F$ preserves coproducts. Turning to the case of representable functors on modules, let 

$$p_j \colon \oplus_i B_i \to B_j$$ 

be the obvious projection ($p_j \circ i_j = 1_{B_j}$, else $p_j \circ i_k = 0$), and given $f \colon M \to \oplus_i B_i$, put 

$$f_j \coloneqq p_j \circ f.$$ 

Then $\mathbf{Mod}_R(M, -)$ preserves the particular coproduct $\oplus_i B_i$ if for each $f \colon M \to \oplus_i B_i$, we have $f_j = 0$ for all but finitely many $j$. 

Clearly $\mathbf{Mod}_R(R, -)$ preserves coproducts, and if $F$, $G$ are coproduct-preserving functors $\mathbf{Mod}_R \to \mathbf{Ab}$, then so is $F \oplus G$. It follows that 

* $\mathbf{Mod}_R(R^n, -)$ preserves coproducts. 

+-- {: .num_prop}
###### Proposition 
If $\mathbf{Mod}_R(M, -)$ preserves coproducts and $q \colon M \to N$ is epic, then $\mathbf{Mod}_R(N, -)$ preserves coproducts. 
=-- 

+-- {: .proof} 
###### Proof 
Given $f \colon N \to \oplus_i B_i$, we have $p_j \circ f \circ q = 0$ for all but finitely many $j$, whence $f_j = p_j \circ f = 0$ for all but finitely many $j$ since $q$ is epic. 
=--

Combining the two preceding observations, we infer that 

* $\mathbf{Mod}_R(M, -)$ preserves coproducts if $M$ is finitely generated. 

Here is a sharper description of coproduct-preserving representables, based on subobject lattices. 

+-- {: .num_theorem #prop1}
###### Theorem 
$\mathbf{Mod}_R(M, -)$ preserves coproducts if and only if the union of every countable chain of proper submodules of $M$ is a proper submodule.  
=-- 

+-- {: .proof} 
###### Proof 
(As adapted from [Gaillard's answer](#Gaillard).) Let $M_0\subset M_1\subset\cdots$ be a chain of proper submodules of $M$ whose union is $M$, and put $Q_n = M/M_n$. Since for each $m \in M$ we have $q_n(m) = 0$ for all but finitely many $n$, the map 

$$q = \langle q_n \rangle \colon M \to \prod_n Q_n,$$ 

corresponding to the tuple of quotient maps $q_n \colon M \to Q_n$, factors through the inclusion $\oplus_n Q_n \hookrightarrow \prod_n Q_n$. However, since each $q_n$ is nonzero, $q$ does not belong to the subgroup 

$$\oplus_n \mathbf{Mod}_R(M, Q_n) \hookrightarrow \prod_n \mathbf{Mod}_R(M, Q_n) \cong \mathbf{Mod}_R(M, \prod_n Q_n)$$ 

and thus the canonical map $\oplus_n \mathbf{Mod}_R(M, Q_n) \to \mathbf{Mod}_R(M, \oplus_n Q_n)$ is not an isomorphism. 

In the other direction, if $\mathbf{Mod}_R(M, -)$ does not preserve coproducts, then we can find some map 

$$f \colon M \to \oplus_{i\in I} B_i$$ 

not belonging to the subgroup $\oplus_{i \in I} \mathbf{Mod}_R(M, B_i) \hookrightarrow \mathbf{Mod}_R(M, \oplus_{i \in I} B_i)$. This means that infinitely many components $f_i \colon M \to B_i$ are nonzero. Choose a countable subset $N \subset I$ such that $f_n \colon M \to B_n$ is nonzero for every $n \in N$, and put 

$$M_n \coloneqq \bigcap_{k \geq n} \ker(f_k).$$
 
Each $M_n$ is a proper submodule of $M$, and the $M_n$ form a nondecreasing chain, but the union of the $M_n$ is $M$ (because for each $m \in M$, only finitely many $f_n(m)$ can be nonzero). 
=-- 

+-- {: .num_theorem #theorem2}
###### Theorem 
Let $R$ be a Noetherian ring, and suppose $M \to N$ is a monomorphism of $R$-modules. Then if $\mathbf{Mod}_R(N, -)$ is coproduct-preserving, so is $\mathbf{Mod}_R(M, -)$. 
=-- 

+-- {: .proof}
###### Proof 
(As adapted from [Muro's answer](#Muro).) Consider a family $B_i$ of modules, and a map $f \colon M \to \oplus_i B_i$. Since there are [enough injectives](http://ncatlab.org/nlab/show/injective+object#AbHasEnoughInjectives), there exists an embedding $i_j \colon B_j \to E_j$ in an injective module, for each $j$. 
Next, as explained [here](http://ncatlab.org/nlab/show/injective+object#DirectSumInjectives), the Noetherian assumption allows us to infer that $\oplus_i E_i$ is injective. Thus, there exists $g$ such that the diagram 

$$\array{
M & \to & N \\
 ^\mathllap{f} \downarrow & & \downarrow^\mathrlap{g} \\
\oplus_j B_j & \underset{\oplus_j i_j}{\to} & \oplus_j E_j
}$$ 

commutes. Because $\mathbf{Mod}_R(N, -)$ preserves coproducts, we have $g_j = 0$ for all but finitely many $j$. Since the diagram 

$$\array{
M & \to & N \\
 ^\mathllap{f_j} \downarrow & & \downarrow^\mathrlap{g_j} \\
B_j & \underset{i_j}{\to} & E_j
}$$

commutes and $i_j$ is injective, we see $f_j = 0$ for all but finitely many $j$, whence $\mathbf{Mod}_R(M, -)$ preserves coproducts. 
=-- 

+-- {: .num_corollary} 
###### Corollary 
Let $R$ be Noetherian. If $\mathbf{Mod}_R(M, -)$ preserves coproducts, then $M$ is finitely generated. 
=-- 

+-- {: .proof}
###### Proof 
(Combining [Gaillard's](#Gaillard) and [Muro's](#Muro) answers.) We prove the contrapositive. Suppose $M$ is not finitely generated. Then we can find a strictly increasing sequence of submodules of $M$: 

$$M_1 \hookrightarrow M_2 \hookrightarrow \ldots \hookrightarrow M.$$ 

Let $M'$ be the union of the $M_i$. By [Theorem 1](#prop1), the representable $\mathbf{Mod}_R(M', -)$ does not preserve coproducts. By [Theorem 2](#theorem2), we infer that $\mathbf{Mod}_R(M, -)$ does not preserve coproducts. 
=-- 

* **Remark:** A ring for which finitely generated modules coincide with modules $M$ such that $\mathbf{Mod}_R(M, -)$ is coproduct-preserving is called **steady**. Thus, Noetherian rings are steady. Cf. [Martin Brandenburg's answer](#Brandenburg). 

### Negative results 

Next, we construct an example of a ring $R$ and an $R$-module $M$ such that $\mathbf{Mod}_R(M, -)$ preserves coproducts but $M$ is not finitely generated. 

+-- {: .num_lemma #lem} 
###### Lemma 
A module $M$ is finitely generated if and only if the union of a totally ordered family of proper submodules of $M$ is a proper submodule. 
=-- 

+-- {: .proof}
###### Proof 
The following proof is a practically verbatim transcription from [Gaillard's answer](#Gaillard), modulo some notational changes. Assume that $M$ is not finitely generated. Let $P$ be the set of those submodules $N$ of $M$ such that $M/N$ is not finitely generated, ordered by inclusion. Clearly the poset $P$ is nonempty and has no maximal element. By (the contrapositive of) Zorn's Lemma, there is a nonempty totally ordered subset $T \hookrightarrow P$ which has no upper bound. Letting $U$ be the union of the submodules occurring in $T$, we see that $M/U$ is finitely generated. There is thus a finitely generated submodule $F$ of $M$ which generates $M$ modulo $U$. Then the collection 

$$\{N+F: N \in T\}$$ 

is a totally ordered set of proper submodules whose union is $M$.
=-- 

Thus, our task is to construct a ring $R$ and an $R$-module $M$ such that every _countable_ chain of proper submodules of $M$ is bounded above by a proper submodule of $M$ (cf. Theorem \ref{theorem2}), but admitting an uncountable chain of proper submodules whose union is $M$ (so that $M$ is not finitely generated, by the preceding lemma \ref{lem}). The solution as presented below is essentially from the answers of [Gaillard](#Gaillard) and [Brandenburg](#Brandenburg), with a few extra glosses. 

The task is more or less straightforward if we just remember that [[valuation ring|valuation rings]] can model arbitrarily complicated [rates of growth](http://ncatlab.org/nlab/show/valuation+ring#example_rates_of_growth_10), i.e., in the present case, we just want to build a valuation field with uncountable supply of rates of growth (or of degrees of infinite/infinitesimal elements). Thus, consider for example the free abelian group generated by the first uncountable ordinal, and make this a totally ordered group $G$ by imposing the lexicographic order. This is the value group of a valuation field $K$ whose elements are [[Hahn series]], formally described as functions 

$$f \colon G \to \mathbb{R}$$ 

whose support is well-ordered when considered as a subset of the opposite order $G^{op}$. (More suggestively, we think of $f$ as a formal series 

$$\sum_{g \in G} a_g x^g$$ 

where $a_g = f(g)$ and $x$ is an indeterminate viewed as a generic infinite element, with obvious rules for adding and multiplying. The well-ordering condition is used to ensure that the rules for addition and multiplication are well-founded, and the value $v(f)$ of such a series is the least $g \in G^{op}$ lying in the support of $f$. That is to say, the greatest $g \in G$ that indexes a non-zero coefficient $a_g$.) 

Now let $R$ be the valuation ring consisting of _bounded_ elements of $K$, i.e., those $f \colon G \to \mathbb{R}$ in $K$ where $f(g) = 0$ whenever $g$ is greater than the identity element of $G$. Then $K$ is the field of fractions of $R$, and we may regard $K$ as an $R$-module. 

For each $t \in \omega_1$, let $R_t$ be the $R$-submodule of $K$ consisting of all those $f \colon G \to \mathbb{R}$ in $K$ such that $v(f) \leq t$. These $R_t$ are "principal fractional ideals", and they form a system of proper submodules which is cofinal in the lattice of $R$-submodules of $K$, ordered by inclusion. 

By cofinality, any _countable_ chain of submodules of $K$ is bounded above by some $R_t$, so that $\mathbf{Mod}_R(K, -)$ preserves coproducts. However, the union of all the $R_t$ is $K$, so that $K$ is not finitely generated. 

## References 

* Sasha (mathoverflow.net/users/2095), "Sums-compact" objects = f.g. objects in categories of modules?, Question 59282 (version: 2011-11-19)
([link](http://mathoverflow.net/questions/59282/sums-compact-objects-f-g-objects-in-categories-of-modules))
{#Sasha} 

* Fernando Muro (mathoverflow.net/users/12166), "Sums-compact" objects = f.g. objects in categories of modules?, Answer 59320 (version: 2011-03-23) ([link](http://mathoverflow.net/questions/59282/sums-compact-objects-f-g-objects-in-categories-of-modules/59320#59320))
{#Muro}

* Pierre-Yves Gaillard (mathoverflow.net/users/461), "Sums-compact" objects = f.g. objects in categories of modules?, Answer 81333 (version: 2011-11-29) ([link](http://mathoverflow.net/questions/59282/sums-compact-objects-f-g-objects-in-categories-of-modules/81333#81333))
{#Gaillard} 

* Martin Brandenburg (mathoverflow.net/users/2841), "Sums-compact" objects = f.g. objects in categories of modules?, Answer 81623 (version: 2011-11-22) ([link](http://mathoverflow.net/questions/59282/sums-compact-objects-f-g-objects-in-categories-of-modules/81623#81623))
{#Brandenburg}

## Footnote 

[^fine]: The divide between extensive categories and categories of modules is somewhat analogous to the divide between the classical particles and quantum particles. In the classical picture, if an elementary particle (which we can think of as "connected") is in a state described by a union $U + V$, then it is either in state $U$ or in state $V$. Whereas in the quantum picture, one has to consider superpositions $U \oplus V$ of states $U$, $V$, and the usual sort of classical logic of disjunctions breaks down. Notice that classical logic (meaning here, non-quantum logic) is largely derived from our experience with extensive categories such as toposes. 
