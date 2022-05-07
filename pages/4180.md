> This entry is about semigroups with a unary operator $i$ such that $s \cdot i(s) \cdot s = s$ and $i(s) \cdot s \cdot i(s) = i(s)$. For the semigroup with a two-sided inverse, see [[invertible semigroup]]

# Contents # 
* table of contents 
{:toc} 

## Definition

An **inverse semigroup** is a [[semigroup]] $S$ (a set with an associative binary operation) such that for every element $s\in S$, there exists a *unique* "inverse" $s^*\in S$ such that $s s^* s = s$ and $s^* s s^* = s^*$. It is evident from this that $s^{\ast\ast} = s$. 

## Examples

Needless to say, a [[group]] is an inverse semigroup. More to the point however: 

* The fundamental example is the following: for any set $X$, let $I(X)$ be the set of all partial [[bijections]] on $X$, i.e. bijections between subsets of $X$.  The composite of partial bijections is their composite as [[relations]] (or as [[partial functions]]).  In fact, any inverse semigroup is isomorphic to a sub-inverse-semigroup of $I(X)$ by the "Cayley's theorem" for inverse semigroups (see below).

This inverse semigroup plays a role in the theory similar to that of [[permutation]] groups in the theory of [[groups]].  It is also paradigmatic of the general philosophy that

> Groups describe global symmetries, while inverse semigroups describe local symmetries.

Other examples include:

* If $X$ is a topological space, let $\Gamma(X)\subseteq I(X)$ consist of the homeomorphisms between open subsets of $X$.  Then $\Gamma(X)$ is a [[pseudogroup of transformations]] on $X$ (a general pseudogroup of transformations is a sub-inverse-semigroup of $\Gamma(X)$). 

* If $L$ is a [[meet-semilattice]], then $L$ is an inverse semigroup under the meet operation. 

## Properties

+-- {: .query}
Lots to say here: the meet-[[semilattice]] of [[idempotents]], the connection with [[ordered groupoid]]s, various representation theorems.
=--

### Idempotents form a subsemigroup 

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
One easily checks that $(e f)^\ast = f(e f)^\ast e$, and that $f(e f)^\ast e$ is an idempotent. So $(e f)^\ast$ is idempotent; as a result, $(e f)^\ast = e f$. Thus $e f$ and similarly $f e$ are idempotent. Next we have 

$$e f (f e) e f = e f^2 e^2 f = e f e f = e f, \qquad f e (e f) f e = f e^2 f^2 e = f e f e = f e$$ 

since $e, f, e f, f e$ are all idempotent, and so $f e = (e f)^\ast = e f$, which completes the proof. 
=-- 

Thus the idempotents in an inverse semigroup form a subsemigroup which is commutative and idempotent. Such a structure is the same as a meet-semilattice except for the fact that there might not have an empty meet or top element; that is, we define an order $\leq$ on idempotents by $e \leq f$ if and only if $e = e f$, whence multiplication of idempotents becomes the binary meet. 

### $\ast$ is an anti-involution 

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

### Order structure 

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

A [[preorder]] $\leq$ is defined on an inverse semigroup by saying $x \leq y$ if any of the four conditions of Proposition \ref{ord} is satisfied; transitivity follows by equivalence to 1. and closure of idempotents under multiplication. When restricted to idempotents, this preorder coincides with the meet-semilattice order. 

+-- {: .num_prop #order} 
###### Proposition 
If $a \leq b$ and $x \leq y$ in an inverse semigroup, then $a x \leq b y$ and $x^\ast \leq y^\ast$. 
=-- 

+-- {: .proof} 
###### Proof 
Writing $a = e b$ for some idempotent $e$, we have $a x = e (b x)$ and so $a x \leq b x$. Similarly $b x \leq b y$, so $a x \leq b y$ by transitivity. 
This gives $a x \leq b y$. If $x = e y$ for an idempotent $e$, then $x^\ast = (e y)^\ast = y^\ast e^\ast$; this gives $x^\ast \leq y^\ast$, 
=-- 

+-- {: .num_cor} 
###### Corollary 
The preorder $\leq$ on an inverse semigroup is a [[partial order]], i.e., if $x \leq y$ and $y \leq x$, then $x = y$. 
=-- 

+-- {: .proof} 
###### Proof 
From $x \leq y$ we derive $x^\ast \leq y^\ast$ and $x x^\ast \leq y y^\ast$, and similarly from $y \leq x$ we derive $y y^\ast \leq x x^\ast$. Thus $x x^\ast = y y^\ast$ since the preorder on idempotents is a meet-semilattice, which is a partial order. Then from $x \leq y$ we derive $x = x x^\ast y = y y^\ast y = y$. 
=-- 

Thus an inverse semigroup is naturally regarded as an internal semigroup in the category of posets (equivalently, a finite-product preserving functor from the [[Lawvere theory]] of semigroups to [[Pos]]). 

### Connection with ordered groupoids 

In this section, an *ordered groupoid* means an [[internal category|internal]] [[groupoid]] in the [[finitely complete category]] of posets [[Pos]]. For any finitely complete category $C$, we observe that the forgetful functor $Gpd(C) \to SemiCat(C)$, taking an internal groupoid in $C$ to the underlying [[semicategory]] (remembering only composition of morphisms, forgetting presence of inverses and identity morphisms), has a right adjoint which takes a semicategory to the [[core]] groupoid of the category of idempotents attached to a semicategory (see [here](/nlab/show/semicategory#idempotents) for details). (This observation is formulated in [[internal logic|finite limit logic]], and thus by a Yoneda lemma argument, its validity reduces to that of the observation in the special case $C = Set$.) 

In particular, this construction may be applied to an inverse semigroup seen as a semigroup in $Pos$: 

+-- {: .num_defn} 
###### Definition 
The groupoid $Ind(S)$ attached to an inverse semigroup $S$ is the core of the category of idempotents $Idem(S)$ of $S$, which as a semigroup in $Pos$ is viewed as a one-object semicategory $B S$ in $Pos$. 
=-- 

In more detail: an arrow $e \to e'$ in $Idem(S)$ is a triple $(e, x, e')$ of elements in $S$, where $e, e'$ are idempotent elements and $x$ is an element such that $x e = x = e' x$. Such an arrow is invertible precisely when $e = x^\ast x$ and $e' = x x^\ast$, with inverse $x^\ast$. Thus the core consists of such arrows $x: x^\ast x \to x x^\ast$. 

A key example to keep in mind is the inverse semigroup of partial bijections $\phi$ on a set, where the arrows of the corresponding groupoid are actual invertible maps $\dom(\phi) \to range(\phi)$ between subsets. In general, the object part of the associated groupoid is not just a poset, but a poset with binary meets. 

The reason for the notation $Ind(S)$ is that this ordered groupoid is a so-called *inductive groupoid*, defined as follows: 

+-- {: .num_defn} 
###### Definition 
An **inductive groupoid** is an internal groupoid $G$ in $Pos$ with the following additional properties: 

* The object part $G_0$ admits binary meets; 

* Given $x: e \to f$ in $G_1$ and $e' \leq e$ in $G_0$, there exists a unique $x': e' \to f$ in $G_1$ with $x' \leq x$, called the *restriction* $[x|_\ast e']$. 

* Given $x: e \to f$ in $G_1$ and $f \geq f'$ in $G_0$, there exists a unique $x': e \to f'$ in $G_1$ with $x \geq x'$, called the *corestriction* $[f' _\ast| x]$. 
=-- 

In fact conditions 2. and 3. in this definition are equivalent. A *morphism* of inductive groupoids $G \to G'$ is an internal functor from $G$ to $G'$ in $Pos$. 

For $G$ an inductive groupoid, a tensor product $\otimes: G_1 \times G_1 \to G_1$ may be defined by the rule 

$$x \otimes y = [x|_\ast dom(x) \wedge cod(y)] \cdot [dom(x) \wedge cod(y) _\ast|y]$$ 

where $\cdot$ indicates composition in $G$. It may be shown that $(G_1, \otimes)$ is an inverse semigroup $Inv(G)$, and the two notions are equivalent: 

+-- {: .num_theorem} 
###### Theorem 
**(Ehresmann-Schein-Nampooripad)** 
There are canonical isomorphisms $S \to Inv(Ind(S))$ and $G \to Ind(Inv(G))$, providing an equivalent of categories $InvSemiGrp \simeq IndGpd$. 
=-- 

### Warning on the definition 

With only a subtle change in definition, the result is that one gets only groups: 

+-- {: .num_prop} 
###### Proposition 
Let $S$ be an [[inhabited set|inhabited]] semigroup with the property that for every $a \in S$ there exists a unique $x \in S$ such that $a x a = a$. Then $S$ is a group. 
=-- 

+-- {: .proof} 
###### Proof 
Since $S$ is inhabited, say by an element $b$, it has an idempotent $e$, for example $b b^\ast$. We will show that $x e = x$ for any $x$; by a similar argument $e x = x$, so that any idempotent $e$ is an identity (*the* identity $1$), whence the idempotents $a a^\ast$ and $a^\ast a$ equal $1$ for any $a$ and $S$ is a group. 

If $a y a = a$ for unique $y$, then from $(a y a) y a = a y a = a$ it follows $y a y = y$ and hence $S$ is an inverse semigroup. The same observation means it is enough to show $(x e) x^\ast (x e) = x e$, since then also $x^\ast (x e) x^\ast = x^\ast$, which by uniqueness implies $x e = x$. 

The above results on inverse semigroups apply and we derive 

$$\array{
x e x^\ast x e & = & x e e x^\ast x e & \\ 
 & = & x e e^\ast x^\ast x e & Proposition \; 1 \\ 
 & = & x e (x e)^\ast x e & Lemma 2 \\ 
 & = & x e
}$$ 

as was to be shown. 
=-- 

### "Cayley's Theorem" for inverse semigroups

+-- {: .num_theorem}
###### Theorem 

Every inverse semigroup $S$ can be realized as a semigroup of partial bijections on a set.
=-- 

+-- {: .proof}
###### Proof
First use the conventional Cayley's theorem to embed $S$ in $\text{End}(S)$ through the map sending $s\in S$ to the map $x\mapsto sx$.  We can now consider $S$ a subset of $\text{End}(S)$.

For each map $s\in S$, $s^\ast s s^\ast=s^\ast$, so $s|_{s^\ast(S)}:s^\ast(S)\rightarrow s(S)$ has left inverse $s^\ast|_{s(S)}:s(S)\rightarrow s^\ast(S)$.  Similarly, as $s s^\ast s=s$, this map is a right inverse, so $s|_{s^\ast(S)}$ is a bijection.

Consider the map $S\rightarrow I(S)$ defined by $s\mapsto (s|_{s^\ast(S)}: s^\ast(S)\rightarrow s(S))$.  We now check that this map is a homomorphism.  For $s,t\in S$, we want to compose the partial bijections $s|_{s^\ast(S)}$ and $t|_{t^\ast(S)}$.  To do this, we first compute the overlap between the codomain of the former and the domain of the latter, which is $s(S)\cap t^\ast (S)$.  The domain of $t|_{t^\ast(S)}\circ s|_{s^\ast(S)}$ is then $s^\ast (s(S)\cap t^\ast (S))=s^\ast t^\ast(S)=(ts)^\ast (S)$ as required.  Finally, we check injectivity.  If $s,t\in S$ and $s_{s^\ast(S)}=t_{t^\ast(S)}$, then $s^\ast(S)=t^\ast(S)$ so $ss^\ast=ts^\ast$.  But then $s^\ast s s^\ast = s^\ast t s^\ast$, so $s=t$.
=-- 

##Links

* [[homotopy theory of inverse semigroups]]

* [[cohomology of inverse semi-groups]]

## Related concepts

* [[associative quasigroup]] (semigroups with division instead of inverses)

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

* Darien DeWolf and Dorette Pronk, _The Ehresmann-Schein-Nampooripad Theorem for Inverse Categories_, [arXiv](https://arxiv.org/abs/1507.08615). 



[[!redirects inverse semigroups]]