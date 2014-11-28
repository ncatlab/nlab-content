
# Contents
* automatic table of contents goes here
{: toc}

## Definitions 

+-- {: .num_defn} 
###### Definition 
Let $\mathcal{C}$ and $\mathcal{D}$ be [[categories]] with [[pullbacks]]. A [[functor]] $T: \mathcal{C} \to \mathcal{D}$ is _taut_ if $T$ preserves [[inverse images]], i.e., [[pullbacks]] of the form 

$$\array{
P & \to & B \\
\downarrow & & \downarrow \\
A & \underset{i}{\to} & C
}$$ 

where $i$ is [[monomorphism|monic]]. (This implies in particular that $T$ preserves monos.) 
=-- 

+-- {: .num_defn} 
###### Definition 
Let $\mathcal{D}$ be a category with pullbacks, and let $\eta: S \to T$ be a [[natural transformation]] between functors $S, T: \mathcal{C} \to \mathcal{D}$. Then $\eta$ is _taut_ if the naturality square 

$$\array{
S A & \stackrel{\eta A}{\to} & T A \\
\mathllap{S i} \downarrow & & \downarrow \mathrlap{T i} \\ 
T A & \underset{\eta B}{\to} & T B
}$$ 

is a pullback for every monomorphism $i$ in $\mathcal{C}$. 
=-- 

A [[monad]] $(T, m, u)$ on a category with pullbacks is _taut_ if $T$ is a taut functor and $m, u$ are taut transformations. 


## Examples 

A number of examples of taut functors can be deduced by applying the following observation. 

+-- {: .num_prop} 
###### Proposition 
Let $T: \mathcal{C} \to \mathcal{D}$ be a functor that preserves weak pullbacks, and assume epis in $D$ are [[regular epimorphism|regular]]. Then $T$ is taut. 
=-- 

+-- {: .proof} 
###### Proof 
In the first place, $T$ preserves monos. For $i: A \to B$ is monic if and only if 

$$\array{
A & \stackrel{1_A}{\to} & A \\
\mathllap{1_A} \downarrow & & \downarrow \mathrlap{i} \\
A & \underset{i}{\to} & B
}$$ 

is a pullback. By hypothesis, the canonical map $\phi: T(A) \to T(A) \times_{T(B)} T(A)$ is (regular) epic, but it is also monic because its composition with either projection $T(A) \times_{T(B)} T(A) \to T(A)$ is the identity. Therefore $\phi$ is an isomorphism, i.e., applying $T$ to the displayed pullback is a pullback, and this forces $T(i)$ to be monic. 

Now if 

$$\array{
P & \stackrel{j}{\to} & B \\
\mathllap{q} \downarrow & & \downarrow \mathrlap{p} \\
A & \underset{i}{\to} & C
}$$ 

is a pullback with $i$ monic, we have that $j$ and therefore $T(j)$ is monic. 
The canonical map $\phi: T(P) \to T(A) \times_{T(C)} T(B)$ is (regular) epic, but also monic, since the mono $T(j)$ factors through it. Thus $\phi$ is an isomorphism, which completes the proof. 
=-- 

A similar proof shows that weakly cartesian natural transformations are also taut. 

As a result of this proposition, 

* Any [[cartesian functor]] is (trivially) taut. 

* The [[ultrafilter|ultrafilter endofunctor]] on $Set$ is taut. (See [here](/nlab/show/relational+beta-module#functor) for a proof that the ultrafilter functor preserves weak pullbacks.) In fact, the ultrafilter monad is taut. 

* Similarly, the [[filter|filter monad]] on $Set$ is taut. 

* The covariant power set monad, whose algebras are [[sup-lattices]], is taut. 

* An [analytic endofunctor](/nlab/show/operad#analytic) induced by a [[species]] is taut. Furthermore, a morphism of species induces a weakly cartesian transformation between the corresponding analytic functors, thus _a fortiori_ a taut transformation. In particular, an analytic monad is taut. 

As an exception, we have 

* The double (contravariant) power set functor $P \circ P^{op}: Set \to Set$ is not taut. 

## Applications 

* Paul Taylor has made tautness of $T$ a central assumption in his account of induction via [[well-founded coalgebras]] over $T$. See chapter VI of his [book](#Taylor). 

* Tautness assumptions play a role in viewing relational $T$-algebras and related structures as generalized multicategories in the sense of [Cruttwell-Shulman](#CS). In the prototypical case of [[relational beta-modules]], there is a [[virtual double category]] of relations. A taut monad $T$ on $Set$ (such as the ultrafilter monad) induces a monad $\bar{T}$ on this virtual double category (that is, a monad in an appropriate 2-category of virtual double categories). From there, one can define a horizontal Kleisli construction which is another virtual double category $HKl(Rel, \bar{T})$, and a $\bar{T}$-multicategory in $Rel$ is by definition a monoid in $HKl(Rel, \bar{T})$. In the special case $T = \beta$, the ultrafilter monad, this concept recapitulates Barr's notion of relational $\beta$-module as synonym of "[[topological space]]". This can be generalized further by working with a virtual double category of "$V$-matrices" where $V$ is a completely distributive quantale ($Rel$ being the case $V = \mathbf{2}$). Again with $T$ a taut monad, one can define a virtual double category $HKl(V\text{-}Mat, \bar{T})$ and then define generalized multicategories as before. (These were studied in a series of articles by [Clementino, Hofmann, Tholen](#CHT2), [Seal](#Seal) and others under the name "$(T, V)$-algebras".) 

## References 

* [[Paul Taylor]], *Practical Foundations of Mathematics*, Cambridge University Press (1999). 
{#Taylor} 

* [[Geoff Cruttwell]] and [[Michael Shulman]], _A unified framework for generalized multicategories_, [arxiv/0907.2460](http://arxiv.org/abs/0907.2460)
{#CS} 

* Maria Manuel Clementino, Dirk Hofmann, and Walter Tholen, _One Setting for All: Metric, Topology, Uniformity, Approach Structure._ ([pdf](http://www.math.yorku.ca/~tholen/ProMat_V_.pdf)) 
{#CHT2} 

* Gavin J. Seal, _Canonical and op-canonical lax algebras_, Theory and 
Applications of Categories, 14 (2005), 221&#8211;243. ([web](http://www.tac.mta.ca/tac/volumes/14/10/14-10abs.html)) 
{#Seal}


[[!redirects taut functors]]
[[!redirects taut monad]]
[[!redirects taut monads]]

