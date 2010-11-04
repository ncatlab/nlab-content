<div class="rightHandSide toc">
[[!include differential graded objects - contents]]
</div>


##Some  relationships between  differential graded algebras and differential graded Lie algebras (DGLA)





##Idea

Here we will look at the relationships between the two topics in the title! We will explore some of the functors linking the two categories.

##The functors $C^*$ and $L_*$.

####Cochain functors $C^* : DGLA\to CDGA$

Let $(V,\partial)$ be a differential graded vector space.  We let

$$C^r(V) = \bigoplus_{p+q=r}C^{p,q} (V),$$


where $C^{p,q} (V) \subset Hom^{p+q}(\otimes^p sV, k)$ is the subspace of (graded) _symmetric_ functions:

$$f(su_1,\ldots,su_p) = \varepsilon(\sigma)f(su_{\sigma(1)},\ldots,su_{\sigma(p))}),$$

for each permutation $\sigma$, having $\varepsilon(\sigma)$ as its Koszul sign.

The product of $f\in C^{p,q}$ and $g\in C^{r,s}$ is 

$$(f\wedge g)(su_1, \ldots,su_{p+r}) = \sum_{\sigma}\varepsilon(\sigma)f(su_{\sigma(1)},\ldots, su_{\sigma(p)})g(su_{\sigma(p+1)},\ldots,su_{\sigma(p+r)}),$$

where the sum is over all $(p,r)$-[[shuffles]], $\sigma$ and $\varepsilon(\sigma)$ is the Koszul sign of :

$$(f,g,su_1,\ldots, su_{p+r})\to (f,su_{\sigma(1)},\ldots, su_{\sigma(p)},g,su_{\sigma(p+1)},\ldots,su_{\sigma(p+r)}).$$

With this product, $C(V)$ is a commutative graded algebra.

Now let $(L,\partial)$ be a [[differential graded Lie algebra]]. There are two derivations with square zero, which anti-commute defined by

$$\array{
(d_1f)(su_1,\ldots,su_n) &=&(-1)^{|f|}\sum_{i=1}^p(-1)^{|su_1|+ \ldots + |su_{i-1}|}f(su_1,\ldots,s\partial u_i,\ldots,su_p) \\
(d_2f)(su_1,\ldots,su_n)&=&(-1)^{|f|}\sum_{i\lt j}\varepsilon_{ij}(-1)^{|su_i|}f(s[u_i,u_j],su_1,\ldots, s\hat{u_i}, \ldots,s\hat{u_j},\ldots,su_p),}$$

where $\varepsilon_{ij}$ is the Koszul sign of 
	
$$(su_1, \ldots, su_p)\to (su_i,su_j,su_1,\ldots, s\hat{u_i}, \ldots,s\hat{u_j},\ldots,su_p),$$ 

where ''$s\hat{u_i}$'' indicates that the element $su_i$ has been omitted.  Putting $d = d_1 + d_2$, we have a commutative dga, $C^*(L,\partial)$, $d_1$ and $d_2$ being called, respectively, the linear and quadratic part of $d$.


When $L$ has finite type, this algebra can be identified with $\bigwedge s\# L$.  Before making this precise, we will develop the extension of duality to the tensor algebra.

Let $\# V$ be the dual of a gvs $V$ of finite type, the elements of the tensor algebra $T(\#V)$ can be interpreted as multilinear functions on $V$ 

$$\langle x_1\otimes \ldots x_p,y_1,\ldots , y_p\rangle  = \varepsilon \prod_{i=1}^{p}\langle x_i,y_i\rangle ,$$

where $\varepsilon$ is the Koszul sign of 
 
$$(x_1,\ldots,x_p,y_1,\ldots,y_p)\to (x_1,y_1,\ldots, ,x_p,y_p).$$

The free commutative graded algebra $\bigwedge\# V$ then can be identified as the algebra $C^*(V)$ defined above, via the canonical injection $\chi : \bigwedge \# V\to T(\# V)$.


## The cochains of a dgla, $(L,\partial)$, of finite type.

Applying the preceding conventions, we get



$$\array{C^*(L,\partial) &=& (\bigwedge s^{-1}\#L, d = d_1+d_2);\\
\langle d_1s^{-1}z;sx\rangle  &=& - \langle z;\partial x\rangle ;\\
\langle d_2s^{-1}z;sx_1,sx_2\rangle &=& (-1)^{|x_1|}\langle z;[x_1,x_2]\rangle }$$
for  $ z\in \#L, x_i\in L, x\in L.$



## Remark

The differential $d$ is a sum of a linear differential $d_1$ and a quadratic differential, $d_2$.  By a word length argument, $d^2 = 0$ is equivalent to 

$\left\{\array{
(a) & d_1^2 = 0\\
(b) & d_1d_2 + d_2d_1 = 0\\
(c) & d_2^2 = 0
}\right.$

If one lifts the definitions of $d_1$ and $d_2$ back to the Lie algebra $(L,\partial)$, one has 

(a) is equivalent to $\partial^2 = 0$;

(b) is equivalent to '$\partial$ is a Lie algebra derivation';

(c) is equivalent to 'the bracket satisfies the Jacobi identity'.



Conversely if $(\bigwedge V,d_1 + d_2)$ is a cdga, free on $V$ as a cga, we can define a dgla structure on $s^{-1}\#V$ using the above formulae.

## Definition

$CDGA_{fg}$ will denote the subcategory of $CDGA$ with


* as objects the cdgas $(\bigwedge V, d)$ of finite type, which are free as cgas on a gvs of generators $V = \sum_{k\geq 1}V^k$ with differential given by a linear part and a quadratic part;

* as arrows, the cdga morphisms that send generators to generators.


The preceding remark translates as

+-- {: .num_prop}
######Proposition
$C^*$ is an isomorphism between $CDGA_{fg}$ and the full subcategory of $DGLA$ formed by Lie algebras of finite type.
=--


Let $\overline{C}$ be the inverse functor.



Let $(\bigwedge V, d)$ and $(\bigwedge V^\prime, d^\prime)$ be two cdgas of finite type, which are free as cgas.  Denote by $d_1$, the linear part of $d$, the differential $\overline{d}$ induced by $d$ on $H(\bigwedge V, d_1) = \bigwedge H(V,d_1)$, has zero linear part.  Its quadratic part $\overline{d_2}$ is thus a differential.  It determines, via $\overline{C}$, a gla structure on $s^{-1}\#H(V,d_1)$

If $(\bigwedge V, d) = C^*(L,\partial)$, we can easily check that the identification of $s^{-1}\#H(V,d_1)$ with $H(L,\partial)$ is a Lie algebra isomorphism.

In particular, if $d$ is decomposable, $(d(V)\subseteq \bigwedge^{\geq 2}V)$, then $s^{-1}\#V$ has a Lie algebra structure defined by $\overline{C}(\bigwedge V,d_2)$.  Applying our earlier description of this, we have that the bracket on $s^{-1}\#V$ is characterised by

$$\langle v;s[s^{-1}x_1,s^{-1}x_2]\rangle  = (-1)^{|x_2|+1}\langle d_2v;x_1,x_2\rangle ,v \in V, x_i\in \#V.$$


Now let $\Phi : (\bigwedge V, d) \to (\bigwedge V^\prime, d^\prime)$ be a morphism of cdgas, then 

$$s^{-1}\#H(Q(\Phi)): s^{-1}\#H(\bigwedge V^\prime, d^\prime_1) \to  s^{-1}\#H(\bigwedge V, d_1)$$ 

is a Lie algebra morphism.

## The functor $L_*$

Let $(A,d)$ be a connected cdga of finite type.  Recall that $\mathbb{L}(s^{-1}\# A) \subset T(s^{-1}\#A) $ denotes the free Lie algebra on $s^{-1}\#A$ and note that $T^p(s^{-1}\#A)  = \#T^p(sA)$.  The linear and quadratic derivations $\partial_1$ and $\partial_2$ respectively are determined on $\mathbb{L}(s^{-1}\#A) $ by 

$\array{
\langle sa;\partial_1s^{-1}b\rangle  &=& -\langle da;b\rangle ,\\
\langle sa_1.sa_2;\partial_2s^{-1}b\rangle & =& (-1)^{|a_1|}\langle a_1.a_2;b\rangle ; \quad a\in A, a_i\in A,b\in \#A.}$

The three conditions

(a) $d^2 = 0$, 

(b) $d$ is an algebra derivative, 

(c) $A$ is associative,

are equivalent, respectively, to

(a) $\partial_1^2 = 0$,

(b) $\partial_1\partial_2 + \partial_2\partial_1 = 0$, 

(c) $\partial_2^2 = 0$.



## Definition

$L_* $ is the functor with domain the full subcategory $f-CDGA_0$ of $CDGA$ formed by the connected cdgas of finite type and with codomain $DGLA$.  It is defined by $L_*(A,d) = (\mathbb{L}(s^{-1}\#A,\partial = \partial_1 + \partial_2$).

Note: $L_* = P\circ \# \circ B$. [$B$ , the bar construction, $\#$ duality, and $P$, primitives.]


## Definition
 

Let $DGLA_{fq}$ be the subcategory of $DGLA$ having as objects the dglas $(\mathbb{L}(V),\partial)$, which, as graded Lie algebras, are free on a vector space of generators $V$ of finite type, having a differential that is the sum of a linear and a quadratic part, and for arrows the dgla morphisms that send generators to generators.  

The above remarks show

+-- {: .num_prop}
######Proposition
$L_*$ is an isomorphism between $DGLA_{fq}$ and $f-CDGA$_0$.
=--


+-- {: .query}

 [[Urs Schreiber|Urs]]: eventually it would be nice if we could put these very detailed discussions in context with existing entries such as [[L-infinity-algebra]] and [[NQ-supermanifold]] which do mention closely related things. Or, in as far as these existing entries are to be regarded as not so good in the light of the present discussiion, we should point out what's amiss and eventually improve things.

[[Tim Porter|Tim]]: I agree, but before that I am hoping that others will help me to sort out the relationships here and with those other areas as I am no expert in this.
=--


We denote by $\overline{L}$, the inverse functor.

Let $(L(W), \partial)$ be a dgla, that is, as a gla, free on a finite type vector space $W$.  Denote by $\partial_1$, the linear part of $\partial$, and $\overline{\partial}_2$, the quadratic part of the differential induced by $\partial$ on $\mathbb{L}(H(W,\partial_1))$.  The space $k \oplus s^{-1}\#H(W,\partial_1)$ has then a commutative graded algebra structure induced via $\overline{L}$.  If $(\mathbb{L}(W),\partial) = L_*(A,d)$, the identification of $k \oplus s^{-1}\#H(W,\partial_1)$  with $H(A,\partial)$ is an algebra isomorphism.

In particular, if $\partial$ is decomposable, $(\partial(W) \subset \mathbb{L}^{\geq 2}(W)$), then $k \oplus s^{-1}\#W$ has a graded commutative algebra  structure defined by $\overline{L}(\mathbb{L}(W),\partial_2)$.  Applying earlier results, the multiplication on $s^{-1}\#W$ is characterised by 

$\langle s(s^{-1}x_1.s^{-1}x_2;w\rangle  = (-1)^{|x_2| + 1}\langle x_1,x_2;\partial_2 w\rangle ; \quad w\in W,x_i \in\#W.$




[[!redirects differential graded algebras and differential graded Lie alg]]
