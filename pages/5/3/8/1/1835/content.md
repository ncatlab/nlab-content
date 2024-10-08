#Contents#
* table of contents
{: toc}

## Idea

A _scheme_ is a [[space]] that _locally_ looks like a particularly simple [[ringed space]]: an [[affine scheme]].
This can be formalised either within the category of [[locally ringed spaces]] or within the category of presheaves of sets on the category of affine schemes $Aff$.

The notion of scheme originated in [[algebraic geometry]] where it is, since [[Grothendieck]]'s revolution of that subject, a central notion. 

However, the idea that

+-- {: .standout}

A scheme is a ringed space that is locally isomorphic to an affine space.

=--

is much more general and need not be restricted to the locality in Zariski topology and to a notion of affine spaces that are [[duality|formal duals]] of rings. If one takes another subcanonical Grothendieck topology $\tau$ on $Aff$ then one talks about __$\tau$-locally affine spaces__. More generally one can take another "category of local models" $Loc$ replacing $Aff$ and suitable topology and consider sheaves on it, as locally affine space in this generalized sense. The category $Loc$ can sometimes be represented by ringed spaces of special type and the gluing can be sometimes made in a genuine (classical, not Grothendieck) topology, within the category of ringed spaces. 

For instance a smooth [[manifold]] is a ringed space locally isomorphic to a "smooth affine space" $\mathbb{R}^n$, with its standard smooth structure.

The standard concept of scheme in [[algebraic geometry]] is therefore usefully understood as a special case of [[generalized scheme]]s that naturally appear for instance also in [[differential geometry]], in [[synthetic differential geometry]] and many other topics.


## Definition 

Throughout this article, "ring" will mean "commutative ring with unit". 

### As locally ringed spaces ##

A __scheme__ is a [[locally ringed space]] $(X, \mathcal{O}_X)$ such that, for every point $x$ of $X$, there is an open subset $U$ of $X$ with $x \in U$ such that the locally ringed space $(U, \mathcal{O}_{X} | U)$ is isomorphic to an [[affine scheme]], that is to say, a commutative [[prime spectrum|ring spectrum]] $Spec A = (|Spec A|, \mathcal{O}_{Spec A})$. 

Here $\mathcal{O}_{X} | U$ denotes the restriction of $\mathcal{O}_{X}$ to $U$, that is to say, the sheaf $i^{*}(\mathcal{O}_{X})$, where $i: U \hookrightarrow X$ is the inclusion map, and $i^{*}$ is the corresponding [[inverse image]] functor from the category of sheaves on $X$ to the category of sheaves on $U$.

A [[morphism of schemes]] $f : (X,\mathcal{O}_X) \to (Y,\mathcal{O}_Y)$ is a morphism of the underlying [[locally ringed space]]s. This means it is a morphism of [[ringed space|ringed spaces]] such that for each point $x \in X$ the induced map of [[local ring]]s
$$
  (\mathcal{O}_Y)_{f(x)} \to  (\mathcal{O}_X)_x
$$
is _local_ (in that it carries the maximal ideal to the maximal ideal). See [[functor of points]].


### As sheaves on $CRing^{op}$

+-- {: .num_defn}
###### Definition
(k-ring, k-functor,affine k-scheme)

For a ring $k$ the _category of $k$-rings_, denoted by $M_k,$ is defined to be the category of commutative associative $k$-algebras with unit. This is equivalently the [[under category]] $k\downarrow CRing$ of pairs $(R,f:k\to R)$ where $R$ is a commutative ring and $f$ is a ring homomorphism.

The _category of $k$-functors_, denoted by $co Psh (M_k)$, is defined to be the category of covariant functors $M_k\to Set$.

The forgetful functor $O_k:R\mapsto R$ sending a $k$-ring to its underlying set is called the _affine line_.

For the full and faithful contravariant functor
$$Sp_k:\begin{cases}
M_k&\to& co Psh(M_k)
\\
A&\mapsto& M_k(A,-)
\end{cases}$$
$Sp_k A$ (and every isomorphic functor) is called an _affine $k$-scheme_. $Sp_k$ restricts to an equivalence between the categories of $k$-rings and the category $Aff Sch_k$ of affine $k$-schemes. We think of this category as of $M_k^{op}$. The functor $Sp_k$ commutes with limits and scalar extension (see below). Consequently $Aff Sch_k$ is closed under limits and base change.

Note that the affine line $O_k$ defined above is naturally isomorphic to $M_k(k[t],-)$, and so $O_k$ is an affine $k$-scheme.

A _function on a_ $k$-functor $X$ is defined to be an object $f\in O(X):=co Psh (M_k)(X,O_k)$. $O(X)$ is a $k$-ring, naturally in $X$, by componentwise addition and multiplication.

=--

+-- {: .num_remark}
###### Remark
The category of $k$-functors has limits.

The terminal object is $e:R\mapsto\{\varnothing\}$. Products and pullbacks are computed component-wise.
=--

+-- {: .num_remark}
###### Remark
For $\phi:k\to k'$ the ''base change'' functor $(-)\otimes_k k':co Psh(M_k)\to co Psh(M_{k'})$ induced by $(-)\circ \phi:M_k\to M_{k'}$ given by postcompositions with $\phi$ is called _scalar extension_. 
=--

Now we come to the definition of not necessarily affine k-schemes

For a $k$-functor $X\in coPsh(M_k)$ and $E\subseteq O(X)$ a set of functions on $X$, we define
$$V(E)(R):=\{x\in X(R) |\forall f\in E, f(x)=0\}$$
and
$$D(E)(R):=\{x\in X(R)|f\in E, \;\text{ the } \; f(x) \; \text{ generate the unit ideal of } \; R\}$$

For a transformation $u:Y\to X$ of $k$-functors and $Z\subseteq X$ a subfunctor we define
$$u^{-1}(Z)(R):=\{y\in Y(R)|u(y)\in Z(R)\}$$

A subfunctor $Y\subseteq X$ is called _open subfunctor_ resp. _closed subfunctor_ if for every transformation $u:T\to X$ we have $u^{-1}(Y)$ is of the form $V(E)$ resp. $D(E)$.

+-- {: .num_defn #DefAsSheaves}
###### Definition

A $k$-functor $X$ is called a $k$_-scheme_ if the following two conditions hold:

1. ($X$ is a sheaf for the [[Zariski site|Zariski Grothendieck topology]] on $M_k^{op}$) For all $k$-rings and all families $(f_i)_i$ such that $R=\sum_i R f_i$ we have: if for all $x_i\in R[f_i^{-1}]$ such that the images of $x_i$ and $x_j$ coincide in $X(R[f_i^{-1} f_j^{-1}])$ there is a unique $x\in X(R)$ mapping to the $x_i$.

1. ($X$ has a cover of Zariski open immersions of affine $k$-schemes) The exists a small family $(U_i)_i$ of open affine subfunctors of $X$ such that for all fields $K\in M_k$ we have that $X(K)=\bigcup_i U_i(K)$.

=--

+-- {: .num_remark}
###### Remark
The category of $k$-schemes is closed under finite limits, forming open- and closed subfunctors, and scalar extension. As a subcategory of the category of Zariski sheaves, it is also closed under taking small coproducts. 

=--

### Translation between the two approaches

The [[fundamental theorem on morphisms of schemes]]  asserts that there is a [[fully faithful functor]] from the category $Sch$ of schemes to $Psh(Aff) \equiv Psh(CRing^{op}) $,  the category of [[presheaf|presheaves]] on the category of affine schemes, or equivalently on the opposite of the category of commutative rings,
given by
$$(X,\mathcal{O}_X)\mapsto Sch((|Spec (-)|,\mathcal{O}_{Spec(-)}),(X,\mathcal{O}_X))$$

This identifies schemes with those presheaves on [[CRing]]${}^{op}$ that

1. are [[sheaf|sheaves]] with respect to the Zariski [[Grothendieck topology]] on $CRing^{op}$;
2. have a [[cover]] by Zariski-open immersions of [[affine scheme]]s in the category of presheaves over $Aff$.

The standard reference for the functor-of-points approach to schemes is [Demazure-Gabriel](#DG). 

+-- {: .num_remark} 
###### Remark 
Different authors take different approaches to the underlying set-theoretic issues. The astute reader will have noticed that we consider the category of _all_ functors $CRing \to Set$ -- which is not a locally small category. Nor is the category of sheaves on the site $CRing^{op}$ with its Zariski topology actually a Grothendieck topos. With due regard to such set-theoretic issues, this approach seems to be conceptually the simplest. Or, one could keep one's options open: for some suitable small category of rings left to one's discretion, for example the category of [[finitely presented object|finitely presented]] rings, one can consider schemes locally modelled on that category. 

Demazure-Gabriel steer a middle course involving [[universes]]: assuming two universes $U$ and $V$ with $\mathbb{N} \in U \in V$, one has a category of "small rings" (belonging to $U$) and a category of sets (belonging to $V$) and one considers functors $M \to Set$ from small rings (called "models") to (not necessarily small) sets. They remark that the device of using universes is really just a convenience that could mostly be dispensed with: one could work within the standard Bernays-G&#246;del framework by assuming that the models are inclusive enough to hold various standard commutative algebra constructions (e.g., quotients, localizations, completions) while still remaining a small category. However, since they wish to avail themselves of direct limits in the category of models, they choose to work with universes instead. 
=-- 

## Properties

* [[schemes are sober]]

The category of schemes admits [[small coproducts]].

It does not admit [[coequalizers]]:
<https://mathoverflow.net/questions/9961/colimits-of-schemes/23966#23966>

The category of schemes admits [[finite limits]].

It does not admit [[infinite products]]:
<https://mathoverflow.net/questions/9134/arbitrary-products-of-schemes-dont-exist-do-they/65534#65534>

(...)

## Generalizations

In [[algebraic geometry]] this is a basic object of study, since the revolution of [[Grothendieck]]. There are generalizations like [[relative schemes]] (which are just objects in a [[slice category]] $Sch/S$), relative [[noncommutative scheme]]s in [[noncommutative algebraic geometry]] introduced by A. Rosenberg in terms of categories and covers defined using pairs of [[adjoint functors]], the generalized schemes of [[Nikolai Durov]], the [[algebraic stack]]s of [[Deligne-Mumford stack|Deligne-Mumford]] and Artin, the dg-schemes of Kapranov, the [[derived scheme]]s of [[Jacob Lurie]], the higher [[algebraic stack]]s of [[Bertrand Toen|Toën]]--Vezzosi, almost schemes (Ofer Gabber and Lorenzo Ramero), formal schemes (Cartier--Grothendieck), [[locally affine spaces]] in the fpqc, fppf or &#233;tale topology (Grothendieck), [[algebraic spaces]], etc. See also [[generalized scheme]], [[simplicial scheme]], [[super-scheme]], [[semiring scheme]].

### Underlying topological space vs. underlying locale 

[[Jacob Lurie]] argues that underlying locale point of view is better than underlying topological space point of view, see [[schemes as locally affine structured (∞,1)-toposes]].

## References

Terminology: [[EGA]] says prescheme, for what we call scheme, and says scheme for what we call [[separated scheme]].

Generalizations: [[simplicial scheme]], [[super-scheme]], [[semiring scheme]], [[noncommutative scheme]], [[derived scheme]]

Other related entries include 

* [[morphism of schemes]]
* [[Serre's theorem on Proj]], [[Serre's theorem on quasicoherent sheaves on affine schemes]]
* [[locally ringed space]]

### Standard monographs

* Robin Hartshorne, _Algebraic geometry_, Springer

* Qing Liu, _Algebraic geometry and arithmetic curves_, 592 pp. Oxford Univ. Press 2002 

* D. Eisenbud, J. Harris, _The geometry of schemes_, Springer Grad. Texts in Math.

* [[David Mumford]], _Red book of varieties and schemes_

* Amnon Neeman, _Algebraic and analytic geometry_, London Math. Soc. Lec. Note Series __345__ 

* William Fulton, _Intersection theory_, Springer 1984

* Ulrich G&#246;rtz, Torsten Wedhorn, _Algebraic geometry I. Schemes with examples and exercises_, Advanced Lectures in Mathematics. Vieweg + Teubner, Wiesbaden, 2010. viii+615 pp. [Springerlink book](http://www.springerlink.com/content/kt5u74/#section=748613&page=1)

* [[Michel Demazure]], [[Pierre Gabriel]], _Groupes algebriques_, tome 1 (later volumes never appeared), Mason and Cie, Paris 1970 (functor of points approach, mainly) 
{#DG}

* Michel Demazure, lectures on p-divisible groups [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

* [[EGA]], [[FGA explained]]

### Other references

* Ravi Vakil's Berkeley [course notes](http://math.stanford.edu/~vakil/0708-216)
* [[Paul Goerss]], [[Topological Algebraic Geometry - A Workshop]]  -- at the beginning one finds a quick introduction in the light of its higher categorical generalizations 

* Wikipedia: [scheme (mathematics)](http://en.wikipedia.org/wiki/Scheme_%28mathematics%29). 

MathOverflow: [arbitrary-products-of-schemes-dont-exist](http://mathoverflow.net/questions/9134/arbitrary-products-of-schemes-dont-exist-do-they), [model-of-a-scheme-regular-over-the-generic-point](http://mathoverflow.net/questions/32196/model-of-a-scheme-regular-over-the-generic-point), [categorical-construction-of-the-category-of-schemes](http://mathoverflow.net/questions/26506/categorical-construction-of-the-category-of-schemes), [when-is-an-algebraic-space-a-scheme](http://mathoverflow.net/questions/4573/when-is-an-algebraic-space-a-scheme), [is-an-algebraic-space-group-always-a-scheme](http://mathoverflow.net/questions/8918/is-an-algebraic-space-group-always-a-scheme), [connections-between-various-generalized-algebraic-geometries-toen-vaquie-durov](http://mathoverflow.net/questions/89475/connections-between-various-generalized-algebraic-geometries-toen-vaquie-durov)

category: algebraic geometry
[[!redirects schemes]]
[[!redirects algebraic scheme]]
[[!redirects algebraic schemes]]