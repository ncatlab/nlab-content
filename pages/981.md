# The cycle category
* table of contents
{: toc}


## Idea

[[Alain Connes]]\'s __cycle category__ $\Lambda$ (sometimes denoted $\mathcal{C}$), often called his __cyclic category__ or __category of cycles__, is a useful source for [[presheaves]] analogous to the [[simplex category]] $\Delta$.


## Definition 

Multiple descriptions of the cycle category $\Lambda$ are possible, but a convenient starting point is to consider first a category $L$ whose morphisms are natural numbers $n \geq 0$, and where the hom-set $L(m, n)$ consists of increasing functions $f: \mathbb{Z} \to \mathbb{Z}$ satisfying the "spiraling property", that $f(i + m + 1) = f(i) + n + 1$, with composition given by functional composition. Then, define $\Lambda$ to be a quotient category of $L$ having the same objects, with $\Lambda(m, n) = L(m, n)/\sim$ where $\sim$ is the equivalence relation for which $f \sim g$ means $f - g$ is a constant multiple of $n+1$. Let $q: L \to \Lambda$ be the quotient. 

+-- {: .num_remark #simplex} 
###### Remark 
Notice that $f \in L(m, n)$ is completely determined by the values $f(0), \ldots, f(m)$. There is a faithful embedding $i: \Delta \to L$ which on objects is the identity, where $f \in L(m, n)$ belongs to the image of $i$ iff $0 \leq f(0)$ and $f(m) \leq n$. The composite 

$$\Delta \stackrel{i}{\hookrightarrow} L \stackrel{q}{\to} \Lambda$$ 

is again faithful, so that the simplex category sits inside $\Lambda$. 
=-- 

+-- {: .num_remark} 
###### Remark 
Of course the successor function $\tau: \mathbb{Z} \to \mathbb{Z}$ gives a function $\tau_n \in L(n, n)$ defined by $\tau_n(i) = i+1$, which in turn induces a function $q(\tau) \in \Lambda(n, n)$ such that $q(\tau)^{n+1} = 1_n$. In this way, we have inclusions $\mathbb{Z}/(n+1) \hookrightarrow \Lambda(n, n)$ of cyclic groups inside $\Lambda$. 
=-- 

## Structure of the cycle category 

To analyze the structure of $\Lambda$ further, we make a series of easy observations. 

+-- {: .num_prop} 
###### Proposition 
Every morphism $f$ of $L$, regarded as a functor $\mathbb{Z} \to \mathbb{Z}$, has a left adjoint $f^\ast: \mathbb{Z} \to \mathbb{Z}$ that is also a morphism of $L$. Similarly, every morphism $f$ of $L$ has a right adjoint $f_\ast$ belonging to $L$. 
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
 & iff & j \leq f(f^\ast(j))+m+1-m-1) \\
 & iff & j \leq f(f^\ast(j)) \\ 
 & iff & f^\ast(j) \leq f^\ast(j).
}$$

Also, since $(\mathbb{Z}, \leq)$ as a category is self-dual, every morphism $f$ of $L$ dually has a right adjoint that is a morphism of $L$. 
=-- 

+-- {: .num_cor} 
###### Corollary 
$L$ is a self-dual category. 
=-- 

+-- {: .proof} 
###### Proof 
The duality functor $L^{op} \to L$ is the identity on objects and takes $f: m \to n$ to $f^\ast: n \to m$. It is contravariant since the left adjoint of a composite $f g$ is $g^\ast f^\ast = (f g)^\ast$. It is an equivalence because its inverse is the right-adjoint mapping, $f \mapsto f_\ast$. 
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
The cyclic group $\mathbb{Z}/(m+1)$ acts on $\Delta^{op}(m, n)$ via the following formula for $f \in L(m, n), f(0) = 0$: 

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

$$k \cdot f = (k \cdot f^\ast)_\ast = [(\tau^{-f^\ast(k)} \circ f^\ast \circ \tau^k]_\ast = (\tau^k)_\ast \circ f^\ast_ast \circ (\tau^{-f^\ast(k)})_\ast = \tau^{-k} \circ f \circ \tau^{f^\ast(k)}$$ 

and this conjugation preserves the action axioms. 
=-- 


Denote the generator of $\Aut_\Lambda([n])$ by $\tau_n$; then of course $\tau_n^{n+1} = \mathrm{id}_{[n]}$. This enables more standard, and equivalent, presentation of $\Lambda$ by [[presentation of a category by generators and relations|generators and relations]]. In addition to the cosimplicial identities between the coboundaries $\delta_i$ and codegeneracies $\sigma_j$ and $\tau^{n+1}_n = \mathrm{id}$ there are following identities:
$$\array{
\tau_n\delta_i = \delta_{i-1}\tau_{n-1},\,\, 1\leq i \leq n\\
\tau_n\delta_0 = \delta_n\\
\tau_n\sigma_i = \sigma_{i-1}\tau_{n-1},\,\, 1\leq i \leq n\\
\tau_m\sigma_0 = \sigma_n\tau_{n+1}^2
}$$

__[[cyclic object|Cyclic objects]]__ in a category $C$ are the contravariant functors $\Lambda^{\mathrm{op}}\to C$, [[cocyclic object]]s are the covariant functors $\Lambda\to C$.  Note that $\Lambda$ itself is, via its inclusion into $Cat$, an example of a cocyclic object in $Cat$.  (Thus, the common term "the cyclic category" to refer to $\Lambda$ is misleading, just like using "the [[simplicial category]]" to refer to the [[simplex category]] $\Delta$.)

If $A$ is an [[abelian category]] then the category of $A$-presheaves on $\Lambda$ is usually called (Connes\'s) category of __cyclic modules__ in $A$.


## Properties

### General

+-- {: .un_theorem}
###### Theorem

1. $\Aut_\Lambda([n]) = \mathbf{Z}/(n+1)\mathbf{Z}$

2. $\Lambda([n],[m]) = \Delta([n],[m])\times \mathbf{Z}/(n+1)\mathbf{Z}$ (as a set)

3. Any morphism $f$ in $\Lambda([n],[m])$ can be uniquely written as a composition $f = \phi\circ g$ where $\phi\in\Delta([n],[m])$ and $g\in\Aut_\Lambda([n])$.
=--

The generalizations of this theorem are the starting point of the theory of [[skew-simplicial set]]s of Krasausukas or equivalently crossed simplicial groups of Loday and Fiedorowicz.

The cyclic category is a [[generalized Reedy category]], as explained [here](http://arxiv.org/abs/0809.3341).

### Generalized Reedy model structure

The cycle category is a [[generalized Reedy category]]. Hence "cyclic spaces" carry a [[generalized Reedy model structure]].

## References

Blog [discussion](http://golem.ph.utexas.edu/category/2007/06/the_curious_incident_of_the_do.html) 

Literature:

* [[J.-L. Loday]], _Cyclic homology_, Grundleheren Math.Wiss. 301, Springer 2nd ed.

* [[V. Drinfeld]], _On the notion of geometric realization_, [arXiv:math.CT/0304064](http://front.math.ucdavis.edu/0304.5064)

* [[Alain Connes]], _Noncommutative geometry_, Academic Press 1994
(also at <http://www.alainconnes.org>)

* R. Krasauskas, _Skew-simplicial groups_, (Russian)  Litovsk. Mat. Sb.  __27__ (1987),  no. 1, 89--99, [MR88m:18022](http://www.ams.org/mathscinet-getitem?mr=88m:18022) (English transl. [[krasauskas.pdf:file]])

* W. G. Dwyer, D. M. Kan, 
_Normalizing the cyclic modules of Connes_,
Comment. Math. Helv. 60 (1985), no. 4, 582--600. 

* W. G. Dwyer, M. J. Hopkins, D. M. Kan, 
_The homotopy theory of cyclic sets_,
Trans. Amer. Math. Soc. 291 (1985), no. 1, 281--289. 

* Z. Fiedorowicz, Jean-Louis Loday, _Crossed simplicial groups and their associated homology_,  Trans. Amer. Math. Soc. __326__ (1991),  no. 1, 57--87, [MR91j:18018](http://www.ams.org/mathscinet-getitem?mr=91j:18018), [doi](http://dx.doi.org/10.2307/2001855)


## Discussion

This discussion is about getting the definition right.

+--{: .query}
[[Mike Shulman|Mike]]: Sorry, I don't think I believe this either.  The category freely generated by any of the above graphs (for $n\gt 0$) has infinitely many morphisms between any pair of objects, and therefore (since it is free) infinitely many endomorphisms.  But aren't the hom-sets of $\Lambda$ supposed to be finite? 

[[Zoran Škoda]] Hom sets of $\Lambda$-yes, but we are now trying to find the concrete realization of objects of $\Lambda$: there are many realizations some involving some sort of categories with infinitely many morphisms. Each $C_n$ in presentation above have infinitely many morphisms in $\mathrm{Cat}$, but only finitely many in $\Lambda$ as I just corrected (thanks for being alert and convince me to think three times!). The infinities in models for $\Lambda$ have to do with a 'reason' why for example finite group model has $SL(2,Z)$ symmetry -- as it is natural to be explained in terms of second iteration of inertia orbifold, which is closely related to cyclic cohomology. But it is confusing because the t-operators are finite...Drinfeld <a href="http://front.math.ucdavis.edu/0304.5064">talks</a> about $Z_+$ categories when talking about $\Lambda$, maybe I confused something, I'll think about it, in that setup there are infinitely many morphisms for what he calls $[n]_{cyc}$ but maybe it is not the same what I intended to do.

[[Mike Shulman|Mike]]: What does it mean for a functor to be "of degree 1?"  I assume that your parenthetical is meant to explain this, but to me it is not obvious.

[[Zoran Skoda]]: By degree I mean the degree of a map in the sense of homotopy theory -- the class of circle to circle map, either at the level of nerves or looking at the subset of circle. 

[[Mike Shulman|Mike]]: It's not immediately obvious to me that the nerve of your category $[n]_\Lambda$ is homotopically a sphere or something else for which the notion of 'degree' makes sense.  What does "looking at the subset of circle" mean?  I would prefer if we give a more explicit combinatorial description of $\Lambda$ as its definition, although we could also include this version later on the page.

[[Zoran Skoda]]: As I wrote above, $k\mapsto k/(n+1)\,\mathrm{mod}\,\mathbf{Z}$, is THE formula for embedding $[n]_{\Lambda}$ into the circle.  On the other hand, the nerve the free category on the graph $0\to 1\to ..\to n\to 0$ is homotopically the circle, isn't it? I think the definition is cleaner than the explanation below via generators and relations.

[[Mike Shulman|Mike]]: What about "$\Lambda$ is the category of finite nonempty [[cyclic order|cyclically ordered]] sets?"  I think that gets across the intended intuition better than either, and is cleaner than either modulo a definition of "cyclic order."

[[Zoran Skoda]]: very good!

[[Mike Shulman|Mike]]: I think I understand what you are getting at with your definition now, although I still don't think it's quite right yet.  I agree that the nerve of $[n]_\Lambda$ is homotopically a circle---except when $n=0$.  And I think that exception means that not all the functors you want have degree 1---those that factor through $[0]_\Lambda$ have degree 0.  It seems like those might be the only functors with degree 0, though so maybe it would suffice to consider all functors with degree 0 or 1.

[[Mike Shulman]]: Apparently I'm wrong: the $0$-cycle is still supposed to be a "loop" of some sort.  So maybe your definition is right as long as the category $[0]_\Lambda$ is defined as freely generated by an endomorphism $0\to 0$.

This page should probably be rewritten with an "Idea" section at the beginning and then descriptions of the many different ways to define it formally.
=--


This discussion is about the name of the category.

+--{.query}
We might also call it the [[cycle category]] in analogy with [[simplex category]], [[cube category]], and [[globe category]] that we\'ve already got here.  If that\'s a good system.  ---Toby

[[Mike Shulman|Mike]]: I like that system.

[[Zoran Škoda]] I personally prefer category of cycles, even sometimes category of simplices, category of (hyper)cubes as I hear from geometers.  Partly because when you translate to other languages, bahuvrihi style (which is anyway an abbreviation of the other form) is not preferred
(unlike in German where it is even written as one word, and in English in which it is one word but is written as two), or sometimes impossible, hence one needs to convert the modifier back into an adjective when translating, what one does not need with saxon genitive. But I am ambivalent to that issue in other cases, but cycle category sounds too similar to cyclic category (for simplicial there is no problem as it sounds very different from simplex)...

[[Mike Shulman|Mike]]: Of course, also "category of simplices" has a different meaning: one talks about "the category of simplices _of_ a simplicial set" to mean the comma category of $\Delta$ over it.  The simplex category is then the category of simplices of the terminal simplicial set.

Regarding translation, I would be inclined to just regard that as something that happens in translation.  Since English uses [noun adjuncts](http://en.wikipedia.org/wiki/Noun_adjunct) frequently, it must be commonplace for translators to replace them with the preferred forms in other languages.  There are lots of other cases in translation where you can't just replace word-for-word; doesn't translation really consist instead of writing new sentences in the target language with the same meaning as those in the source language?

[[Zoran Skoda]]: Look, one can translate a phrase, but not just a stack of nouns. Stack of nouns either stays stack of nouns (what is very awkward nowdays, with young people using lots of stacks of nouns literally from English semi-translated to languages which do not do massive bahuvrihi compounds) or need to be expanded/described. But how to expand cycle category then to category of cycles. Hence I have no problem to translate cycle category to Croatian, but then it will coincide in Croatian with category of cycles. Or I can make unnatural compounds with hyphen ciklus-kategorija, what sounds like water-fruit for juicy fruit or for fruit with juice. What do you, mathematics-man think of this word-compound tongue-thing ? And beware that the cost (unusualness) in many languages of such compounds is orders of magnitude more unusual than in English. Or give me another descriptive expansion (if category of cycles already used/not accepted!).

By the way, I hear around certain students of Kan talking "the category of simplices" for $\Delta$. I see no problem with the fact that there are more general "categories of simplices" in specialistic usage (non-specialists use them very little and specialists will anyway say simplices where...$\Delta$ is used by everybody, not only homotopy theorists or simplicial experts, the latter comma category is a rather specialists' thing).

[[Mike Shulman|Mike]]: You appear to be trying to ridicule me for exactly I was saying one _shouldn't_ do.  Of course, when you translate "cycle category" to Croatian it will come out the same as "category of cycles."  When written in language X, mathematics should be written in language X, not simply obtained from language Y by replacing things word-for-word; this is just as true when X=English and Y=Croatian as when X=Croatian and Y=English.  In particular, a noun together with some noun adjuncts _is_ a phrase in English, not just a "stack of nouns," and should be translated to result in a grammatical phrase in whatever other language one is translating to.  Don't blame me because _some_ people translate things from English incorrectly.

I don't have a problem with people saying "category of simplices" for $\Delta$, but I prefer to say "simplex category" myself as it is slightly more precise.

[[Mike Shulman|Mike]]: You do, however, have a good point that when writing in English we should not try to distinguish in _meaning_ between "cycle category" and "category of cycles," since when translating into many other languages they will become the same.  I would still prefer that we name the page "cycle category" here on the nLab, since it accords better with our existing terminology for similar categories, but I think you should feel free to use "category of cycles."
=--

[[!redirects cyclic category]]
[[!redirects Connes' cyclic category]]
[[!redirects category of cycles]]

category: category