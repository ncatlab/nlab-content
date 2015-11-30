## Definition

An **inverse semigroup** is a [[semigroup]] $S$ (a set with an associative binary operation) such that for every element $s\in S$, there exists a *unique* "inverse" $s^*\in S$ such that $s s^* s = s$ and $s^* s s^* = s^*$. It is evident from this that $s^{\ast\ast} = s$. 

## Examples

Needless to say, a [[group]] is an inverse semigroup. More to the point however: 

* The fundamental example is the following: for any set $X$, let $I(X)$ be the set of all partial [[bijections]] on $X$, i.e. bijections between subsets of $X$.  The composite of partial bijections is their composite as [[relations]] (or as [[partial functions]]).

This inverse semigroup plays a role in the theory similar to that of [[permutation]] groups in the theory of [[groups]].  It is also paradigmatic of the general philosophy that

> Groups describe global symmetries, while inverse semigroups describe local symmetries.

Other examples include:

* If $X$ is a topological space, let $\Gamma(X)\subseteq I(X)$ consist of the homeomorphisms between open subsets of $X$.  Then $\Gamma(X)$ is a [[pseudogroup of transformations]] on $X$ (a general pseudogroup of transformations is a sub-inverse-semigroup of $\Gamma(X)$). 

* If $L$ is a [[meet-semilattice]], then $L$ is an inverse semigroup under the meet operation. 

## Properties

+-- {: .query}
Lots to say here: the meet-[[semilattice]] of [[idempotents]], the connection with [[ordered groupoid]]s, various representation theorems.
=--

+-- {: .num_prop #triv} 
###### Proposition 
For any $x$ in an inverse semigroup, $x x^\ast$ and $x^\ast x$ are idempotent. If $e$ is idempotent, then $e^\ast = e$. 
=-- 

The proof is trivial. 

+-- {: .num_lemma #comm} 
###### Lemma 
In an inverse semigroup, the product of any two idempotents $e, f$ is idempotent, and any two idempotents commute. 
=-- 

+-- {: .proof} 
###### Proof 
One easily checks that $(e f)^\ast = f(e f)^\ast e$, and that $f(e f)^\ast e$ is an idempotent. So $(e f)^\ast$ is idempotent; as a result, $(e f)^\ast = e f$. Thus $e f$ and similarly $f e$ are idempotent. We then have 

$$e f (f e) e f = e f^2 e^2 f = e f e f = e f, \qquad f e (e f) f e = f e^2 f^2 e = f e f e = f e$$ 

since $e, f, e f, f e$ are all idempotent, and so $f e = (e f)^\ast = e f$, completing the proof. 
=-- 

Thus the idempotents in an inverse semigroup form a subsemigroup which is commutative and idempotent. Such a structure is the same as a meet-semilattice except for the fact that there might not have an empty meet or top element; that is, we define an order $\leq$ on idempotents by $e \leq f$ if and only if $e = e f$, whence multiplication of idempotents becomes the binary meet. 



+-- {: .num_lemma #invol} 
###### Lemma 
For any two elements $x, y$ in an inverse semigroup, $(x y)^\ast = y^\ast x^\ast$. 
=-- 

+-- {: .proof} 
###### Proof 
Since the idempotents $x^\ast x, y y^\ast$ commute, we have 

$$x y (y^\ast x^\ast) x y = x (y y^\ast)(x^\ast x) y = x x^\ast x y y^\ast y = x y$$ 

and similarly $y^\ast x^\ast (x y)y^\ast x^\ast = y^\ast y y^\ast x^\ast x x^\ast = y^\ast x^\ast$, which is all we need. 
=-- 

+-- {: .num_prop #ord} 
###### Proposition 
For elements $x, y$ in an inverse semigroup, the following are equivalent: 

1. There exists an idempotent $e$ such that $x = e y$, 
1. $x = x x^\ast y$, 
1. There exists an idempotent $f$ such that $x = y f$, 
1. $x = y x^\ast x$. 
=-- 

+-- {: .proof} 
###### Proof 
We show $3. \Rightarrow 2.$; a similar proof shows $1. \Rightarrow 4.$ Clearly then we have $3. \Rightarrow 2. \Rightarrow 1. \Rightarrow 4. \Rightarrow 3.$ 

Given an idempotent $f$ such that $x = y f$, we have 

$$\array{
x & = & y f & \\
 & = & y y^\ast y f & \\ 
 & = & y f y^\ast y & since \; idempotents \; commute \\
 & = & y f f y^\ast y & \\ 
 & = & y f f^\ast y^\ast y & \text{Proposition 1} \\ 
 & = & y f (y f)^\ast y & \text{Lemma 2} \\ 
 & = & x x^\ast y & 
}$$ 

which gives $3. \Rightarrow 2.$ 
=-- 

A [[partial order]] $\leq$ is defined on an inverse semigroup by saying $x \leq y$ if any of the four conditions of Proposition \ref{ord} is satisfied. When restricted to idempotents, this order coincides with the meet-semilattice order. 

+-- {: .num_prop} 
###### Proposition 
If $a \leq b$ and $x \leq y$ in an inverse semigroup, then $a x \leq b y$ and $x^\ast \leq y^\ast$. 
=-- 

+-- {: .proof} 
###### Proof 
We observe from Proposition \ref{ord} that for any elements $c, x$ we have $c x^\ast x = x x^\ast c$. From the hypotheses $a = a a^\ast b$ and $x = y x^\ast x$ we have $a x = a a^\ast b y x^\ast x = (x x^\ast) a a^\ast b y$ by our observation. But $e = (x x^\ast)(a a^\ast)$ is idempotent by Lemma \ref{comm}. This gives $a x \leq b y$. If $x = e y$ for an idempotent $e$, then $x^\ast = (e y)^\ast = y^\ast e^\ast = y^\ast e$; this gives $x^\ast \leq y^\ast$, 
=-- 



##Links

* [[homotopy theory of inverse semigroups]]

* [[cohomology of inverse semi-groups]]

## References

* [[Mark V. Lawson]], tutorial lectures on semigroups in Ottawa, notes available [here](http://www.ma.hw.ac.uk/~markl/ottawa.html).
*  [[Mark V. Lawson]], _Constructing ordered groupoids_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 46 no. 2 (2005), p. 123--138, [URL stable](http://www.numdam.org/item?id=CTGDC_2005__46_2_123_0)
* [[Mark V. Lawson]], Inverse semigroups: the theory of partial symmetries, World Scientific, 1998.
* [[Mark V. Lawson]], G. Kurdyavtseva, _The classifying space of an inverse semigroup_,  Period. Math. Hungar., to appear, [as preprint: ArXiv 1210.4421](http://arxiv.org/pdf/1210.4421.pdf)
* Alan L. T. Paterson, _Groupoids, inverse semigroups, and their operator algebras_, Progress in Mathematics __170__, Birkh&#228;user 1999, [MR 1724106](http://www.ams.org/mathscinet-getitem?mr=1724106)
* Alcides Buss, Ruy Exel, [[Ralf Meyer]], _Inverse semigroup actions as groupoid actions_, Semigroup Forum __85__ (2012), 227--243, [arxiv/1104.0811](http://arxiv.org/abs/1104.0811)
* Ruy Exel, _Inverse semigroups and combinatorial $C^\ast$-algebras_, Bull. Braz. Math. Soc. (N.S.) 39 (2008), no. 2, 191&#8211;313, [doi](http://dx.doi.org/10.1007/s00574-008-0080-7) MR 2419901
* Alcides Buss, Ruy Exel, _Fell bundles over inverse semigroups and twisted &#233;tale groupoids_, J. Oper. Theory __67__, No. 1, 153-205 (2012) [MR2821242](http://www.ams.org/mathscinet-getitem?mr=2821242) [Zbl 1249.46053](http://zbmath.org/?q=an:1249.46053) [arxiv/0903.3388](http://arxiv.org/abs/0903.3388)[journal](http://www.mathjournals.org/jot/2012-067-001/0000-000-000-000.html); _Twisted actions and regular Fell bundles over inverse semigroups_, [arxiv/1003.0613](http://arxiv.org/abs/1003.0613)
* [[Pedro Resende]], _Lectures on &#233;tale groupoids, inverse semigroups and quantales_, Lecture Notes for the GAMAP IP Meeting, Antwerp, 4-18 Sep 2006, 115 pp. [pdf](http://www.math.ist.utl.pt/%7Epmr/poci55958/gncg51gamap-version2.pdf); _&#201;tale groupoids and their quantales_, Adv. Math. 208 (2007) 147-209; also published electronically: [doi](http://dx.doi.org/10.1016/j.aim.2006.02.004) [math/0412478](http://arxiv.org/abs/math/0412478); _A note on infinitely distributive inverse semigroups_, Semigroup Forum 73 (2006) 156-158; [doi](http://dx.doi.org/10.1007/s00233-005-0547-4) [math/0506454](http://arxiv.org/abs/math.RA/0506454)
* [[B. Steinberg]], _Strong Morita equivalence of inverse semigroups_, Houston J. Math. 37 (2011) 895-927
[[!redirects inverse semigroups]]