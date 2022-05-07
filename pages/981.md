[[!redirects cycle category]]


# The cyclic category
* table of contents
{: toc}


## Idea

[[Alain Connes]]\'s __cyclic category__ $\Lambda$ (sometimes denoted $\mathcal{C}$) is a [[small category]] whose [[presheaves]] -- called _[[cyclic sets]]_ or more generally _[[cyclic objects]]_  -- are somewhere intermediate between [[simplicial sets]] and [[symmetric sets]]. It strictly contains the [[simplex category]], and has [[cyclic groups]] for [[automorphism groups]]. Among its virtues, it is a self-dual category. 

The cycle category is used for the description of the cyclic structure on [[Hochschild homology]]/[[Hochschild cohomology]] and accordingly for the description of [[cyclic homology]]/[[cyclic cohomology]].


## Definitions 

Multiple descriptions of the cyclic category $\Lambda$ are possible, but a convenient starting point is to consider first a category $L$ whose [[objects]] are [[natural numbers]] $n \geq 0$, and where the [[hom-set]] $L(m, n)$ consists of increasing functions $f: \mathbb{Z} \to \mathbb{Z}$ satisfying the "spiraling property", that $f(i + m + 1) = f(i) + n + 1$, with [[composition]] given by ordinary function composition. The category $L$ is ([[equivalence of categories|equivalent]] to) the category $\Lambda_\infty$ called the [[paracyclic category]] by [Nikolaus and Scholze](#NS).

Then, define $\Lambda$ to be a quotient category of $L$ having the same objects, with $\Lambda(m, n) = L(m, n)/\sim$ where $\sim$ is the equivalence relation for which $f \sim g$ means $f - g$ is a constant multiple of $n+1$. Let $q: L \to \Lambda$ be the quotient. 

+-- {: .num_remark #simplex} 
###### Remark 
Notice that $f \in L(m, n)$ is completely determined by the values $f(0), \ldots, f(m)$. There is a [[faithful functor|faithful]] [[subcategory|embedding]] $i \colon \Delta \to L$ which on objects is the identity, where $f \in L(m, n)$ belongs to the image of $i$ iff $0 \leq f(0)$ and $f(m) \leq n$. The composite 

$$\Delta \stackrel{i}{\hookrightarrow} L \stackrel{q}{\to} \Lambda$$ 

is again [[faithful functor|faithful]], so that the [[simplex category]] sits inside $\Lambda$. 
=-- 

+-- {: .num_remark} 
###### Remark 
Of course the [[successor]] function $\tau \colon \mathbb{Z} \to \mathbb{Z}$ gives a function $\tau_n \in L(n, n)$ defined by $\tau_n(i) = i+1$, which in turn induces a function $q(\tau) \in \Lambda(n, n)$ such that $q(\tau)^{n+1} = 1_n$. In this way, we have inclusions $\mathbb{Z}/(n+1) \hookrightarrow \Lambda(n, n)$ of [[cyclic groups]] inside $\Lambda$. 
=-- 

__[[cyclic object|Cyclic objects]]__ in a category $C$ are the [[contravariant functors]] $\Lambda^{\mathrm{op}}\to C$, [[cocyclic objects]] are the [[covariant functors]] $\Lambda\to C$.  Note that $\Lambda$ itself is, via its inclusion into $Cat$, an example of a [[cocyclic object]] in $Cat$.  (Thus, the common term "the cyclic category" to refer to $\Lambda$ is misleading, just like using "the [[simplicial category]]" to refer to the [[simplex category]] $\Delta$.)

If $A$ is an [[abelian category]] then the category of $A$-presheaves on $\Lambda$ is usually called (Connes\'s) category of __cyclic modules__ in $A$.


## Structure of the cyclic category {#structure}

To analyze the structure of $\Lambda$ further, we make a series of easy observations. These are largely based on [Elmendorf 93](#Elm). 

+-- {: .num_prop} 
###### Proposition 
Every [[morphism]] $f$ of $L$, regarded as a functor $\mathbb{Z} \to \mathbb{Z}$, has a [[left adjoint]] $f^\ast: \mathbb{Z} \to \mathbb{Z}$ that is also a morphism of $L$. Similarly, every morphism $f$ of $L$ has a [[right adjoint]] $f_\ast$ belonging to $L$. 
=-- 

+-- {: .proof} 
###### Proof 
By the spiraling property of $f$, for any $j \in \mathbb{Z}$ the comma category $(j \downarrow f)$ as a subset of $\mathbb{Z}$ has a lower bound in $\mathbb{Z}$ and hence is well-ordered. It is also nonempty, and we define $f^\ast(j)$ to be the least element of $(j \downarrow f)$. In other words $f^\ast(j)$ is the least $i$ such that $j \leq f(i)$. It is easy to check that $f^\ast$ obeys the spiraling property $f^\ast(j+n+1) = f^\ast(j)+m+1$, since 

$$\array{
f^\ast(j+n+1) \leq f^\ast(j)+m+1 & iff & j+n+1 \leq f(f^\ast(j)+m+1) \\ 
 & iff & j+n+1 \leq f(f^\ast(j))+n+1 \\ 
 & iff & j \leq f(f^\ast(j)) \\ 
 & iff & f^\ast(j) \leq f^\ast(j)
}$$ 

and 

$$\array{
f^\ast(j)+m+1 \leq f^\ast(j+n+1) & iff & f^\ast(j) \leq f^\ast(j+n+1)-m-1 \\ 
 & iff & j \leq f(f^\ast(j+n+1)-m-1) \\ 
 & iff & j \leq f(f^\ast(j+n+1))-n-1 \\
 & iff & j + n + 1\leq f(f^\ast(j) + n + 1) \\ 
 & iff & f^\ast(j+n+1) \leq f^\ast(j+n+1).
}$$

Also, since $(\mathbb{Z}, \leq)$ as a category is self-dual, every morphism $f$ of $L$ dually has a right adjoint that is a morphism of $L$. 
=-- 

+-- {: .num_cor} 
###### Corollary 
$L$ is a self-dual category. 
=-- 

+-- {: .proof} 
###### Proof 
The [[opposite category|duality]] functor $L^{op} \to L$ is the identity on objects and takes $f: m \to n$ to $f^\ast: n \to m$. It is contravariant since the left adjoint of a composite $f g$ is $g^\ast f^\ast = (f g)^\ast$. It is an equivalence because its inverse is the right-adjoint mapping, $f \mapsto f_\ast$. 
=-- 

+-- {: .num_prop} 
###### Proposition  
$\Lambda$ is a self-dual category. 
=-- 

+-- {: .proof} 
###### Proof 
If $f \sim g$ in $L(m, n)$, then $f = \tau^{k (n+1)} \circ g$ for some $k \in \mathbb{Z}$. Observe that $\tau^\ast = \tau^{-1}$, so $f^\ast = g^\ast \circ \tau^{-k(n+1)} = \tau^{-k(m+1)} \circ g^\ast$ where the last equation holds because $g^\ast: n \to m$ is spiraling. This shows $f^\ast \sim g^\ast$, i.e., the self-duality of $L$ descends to $\Lambda$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
For a morphism $f \in L(m, n)$, we have $f^\ast(0) \leq 0$ iff $0 \leq f(0)$, and $0 \leq f^\ast(0)$ iff $f(m) \leq f(n)$. Hence $f^\ast(0) = 0$ iff ($0 \leq f(0)$ and $f(m) \leq n$). 
=-- 

+-- {: .proof} 
###### Proof  
The first assertion is immediate from the adjunction $f^\ast \dashv f$. The second follows from the deduction 

$$\array{
0 \leq f^\ast(0) & iff & -1 \lt f^\ast(0) \\ 
 & iff & \neg (f^\ast(0) \leq -1) \\ 
 & iff & \neg (0 \leq f(-1)) \\ 
 & iff & f(-1) \lt 0 \\ 
 & iff & f(m) \lt n+1 \\ 
 & iff & f(m) \leq n
}$$ 

where the step to the penultimate line used the spiraling property. 
=-- 

The previous proposition, in conjunction with the self-duality of $L$ and Remark \ref{simplex}, shows that $\Delta^{op}$ faithfully maps to $L$ by $\Delta^{op}(m, n) \cong \{f \in L(m, n): f(0) = 0\}$. Passing to the quotient $q: L \to \Lambda$, this description also realizes $\Delta^{op}$ as sitting inside $\Lambda$, and the next result is immediate. 

+-- {: .num_prop #unique1} 
###### Proposition 
Every morphism $f: m \to n$ in $\Lambda$ may be uniquely decomposed as $f = \tau_n^{f(0)} g$ where $g$ belongs to $\Delta^{op}(m, n) \subset L(m, n)$, and the exponent $f(0)$ is considered modulo $n+1$. 
=-- 

+-- {: .num_prop #action} 
###### Proposition 
The [[cyclic group]] $\mathbb{Z}/(m+1)$ [[group action|acts]] on $\Delta^{op}(m, n)$ via the following formula for $f \in L(m, n), f(0) = 0$: 

$$k \cdot f = \tau^{-f(k)} \circ f \circ \tau^k$$ 

or in other words, via $(k \cdot f)(i) \coloneqq f(k+i) - f(k)$. 
=-- 

+-- {: .proof} 
###### Proof 
Clearly $k \cdot f \in \{g \in L(m, n): g(0) = 0\}$. We calculate 

$$\array{
j \cdot (k \cdot f) & = & \tau^{-(k \cdot f)(j)} \circ (k \cdot f) \circ \tau^j \\ 
 & = & \tau^{-(f(j+k) - f(k))} \circ \tau^{-f(k)} \circ f \circ \tau^k \circ \tau^j \\ 
 & = & \tau^{-f(j+k)} \circ f \circ \tau^{j+k} \\ 
 & = & (j + k) \cdot f.
}$$

Moreover, $((m+1)\cdot f)(i) = f(i+m+1)-f(0+m+1) = f(i)+n+1 - (f(0)+n+1) = f(i) - f(0) = f(i)$, so that the $\mathbb{Z}$-action $(k, f) \mapsto k \cdot f$ factors through a $\mathbb{Z}/(m+1)$-action. 
=--  

+-- {: .num_prop} 
###### Proposition 
Every morphism $f: m \to n$ in $\Lambda$ may be uniquely decomposed as $f = h \tau_m^{-k}$ where $h$ belongs to $\Delta$ and $k$ is unique modulo $m+1$. The cyclic group $\mathbb{Z}/(n+1)$ acts on $\Delta(m, n) \cong \{f \in L(m, n): 0 \f(0)\; and\; f(m) \leq n$ by the formula $k \cdot f = \tau^{-k} \circ f \circ \tau^{f^\ast(k)}$. 
=-- 

+-- {: .proof} 
###### Proof 
This follows from previous propositions by dualizing. For $f \in L(m, n)$ we write $f^\ast: n \to m$ uniquely in the form $\tau_m^k g$ with $g \in \Delta^{op}(n, m)$, by Proposition \ref{unique1}. Taking right adjoints, $f = g_\ast \tau_m^{-k}$ where $g_\ast \in \Delta(m, n)$. We define the action on $\Delta(m, n)$ by conjugating the action on $\Delta^{op}(n, m)$ provided by Proposition \ref{action}, i.e., for $f \in \Delta(m, n)$ we define 

$$k \cdot f = (k \cdot f^\ast)_\ast = [\tau^{-f^\ast(k)} \circ f^\ast \circ \tau^k]_\ast = (\tau^k)_\ast \circ f^\ast_\ast \circ (\tau^{-f^\ast(k)})_\ast = \tau^{-k} \circ f \circ \tau^{f^\ast(k)}$$ 

and this conjugation preserves the action axioms. 
=-- 


Denoting the generator $q(\tau_n)$ of $\Aut_\Lambda([n])$ also by $\tau_n$, we saw $\tau_n^{n+1} = \mathrm{id}_{[n]}$. One may read off from the development above a (perhaps more standard, and equivalent) presentation of $\Lambda$ by [[presentation of a category by generators and relations|generators and relations]]. In addition to the cosimplicial identities between the coboundaries $\delta_i$ and codegeneracies $\sigma_j$ and $\tau^{n+1}_n = \mathrm{id}$ there are the following identities:
$$\array{
\tau_n\delta_i = \delta_{i-1}\tau_{n-1},\,\, 1\leq i \leq n\\
\tau_n\delta_0 = \delta_n\\
\tau_n\sigma_i = \sigma_{i-1}\tau_{n-1},\,\, 1\leq i \leq n\\
\tau_m\sigma_0 = \sigma_n\tau_{n+1}^2
}$$



## Properties

### General

We reiterate the development in the [section on structure](#structure) in summary form: 

+-- {: .num_theorem}
###### Theorem

1. $\Aut_\Lambda([n]) = \mathbf{Z}/(n+1)\mathbf{Z}$

2. $\Lambda([n],[m]) = \Delta([n],[m])\times \mathbf{Z}/(n+1)\mathbf{Z}$ (as a set)

3. Any morphism $f$ in $\Lambda([n],[m])$ can be uniquely written as a composition $f = \phi\circ g$ where $\phi\in\Delta([n],[m])$ and $g\in\Aut_\Lambda([n])$.
=--

The generalizations of this theorem are the starting point of the theory of [[skew-simplicial set]]s of Krasausukas or equivalently crossed simplicial groups of Loday and Fiedorowicz.

The cyclic category is a [[generalized Reedy category]], as explained [here](http://arxiv.org/abs/0809.3341).

### Generalized Reedy model structure

The cycle category is a [[generalized Reedy category]]. Hence "cyclic spaces" carry a [[generalized Reedy model structure]].

## Related concepts

* [[cyclic object]]

* [[cyclic set]], [[cyclic space]],

* [[cyclotomic space]], [[cyclotomic spectrum]]

* [[cyclic homology]]


## References

* [[Jean-Louis Loday]], *The Cyclic Category, Tor and Ext Interpretation* ([doi:10.1007/978-3-662-21739-9_6](https://doi.org/10.1007/978-3-662-21739-9_6))

  Chapter 6 in: *Cyclic Homology*, Grundlehren **301**, Springer 1992 ([doi:10.1007/978-3-662-21739-9](https://link.springer.com/book/10.1007/978-3-662-21739-9))


* [[V. Drinfeld]], _On the notion of geometric realization_, [arXiv:math.CT/0304064](http://front.math.ucdavis.edu/0304.5064)

* [[Alain Connes]], _Noncommutative geometry_, Academic Press 1994
(also at <http://www.alainconnes.org>)

* R. Krasauskas, _Skew-simplicial groups_, (Russian)  Litovsk. Mat. Sb.  __27__ (1987),  no. 1, 89--99, [MR88m:18022](http://www.ams.org/mathscinet-getitem?mr=88m:18022) (English transl. [[krasauskas.pdf:file]])

* [[William Dwyer]], [[Daniel Kan]], 
_Normalizing the cyclic modules of Connes_,
Comment. Math. Helv. 60 (1985), no. 4, 582--600. 

* [[William Dwyer]], [[Mike Hopkins]], [[Daniel Kan]],  _The homotopy theory of cyclic sets_,
Trans. Amer. Math. Soc. 291 (1985), no. 1, 281--289. 

* Z. Fiedorowicz, [[Jean-Louis Loday]], _Crossed simplicial groups and their associated homology_,  Trans. Amer. Math. Soc. __326__ (1991),  no. 1, 57--87, [MR91j:18018](http://www.ams.org/mathscinet-getitem?mr=91j:18018), [doi](http://dx.doi.org/10.2307/2001855) 

* {#Elm} [[Anthony Elmendorf]], *A simple formula for cyclic duality*, Proc. Amer. Math. Soc. Volume 118, Number 3 (July 1993), 709-711. ([pdf](http://www.ams.org/journals/proc/1993-118-03/S0002-9939-1993-1143017-0/S0002-9939-1993-1143017-0.pdf))

* {#NS} [[Thomas Nikolaus]], [[Peter Scholze]], *On topological cyclic homology* ([arxiv:1707.01799](https://arxiv.org/abs/1707.01799))

See also 

* Wikipedia, _[Cyclic category](https://en.wikipedia.org/wiki/Cyclic_category)_

* Blog [discussion](http://golem.ph.utexas.edu/category/2007/06/the_curious_incident_of_the_do.html) 


[[!redirects cyclic category]]
[[!redirects Connes' cyclic category]]
[[!redirects category of cycles]]

category: category