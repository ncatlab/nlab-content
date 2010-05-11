
<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
***
[[!include compact object - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

An _infinitesimal quantity_ is supposed to be a quantity that is infinitely small in size, yet not necessarily perfectly small (zero).  An _infinitesimal space_ is supposed to be a space whose extension is infinitely small, yet not necessarily perfectly small (pointline). 

Infinitesimal objects have been conceived and used in one way or other for a long time, notably in [[algebraic geometry]], where [[Grothendieck]] emphasized the now familiar role of [[duality|formal dual]]s ([[affine scheme]]s) of commutative rings $R$ with nilpotent ideals $J\subset R$ as _infintitesimal thickenings_ of the formal dual of the quotient ring $R/J$.

### Formalization in synthetic differential geometry 

A proposal for formalizing the [[category theory|abstract nonsense]] behind the notion of the _infinitesimal_ such that these algebraic constructions become _models_ for more general axioms was given by [[William Lawvere]] in his 1967 lecture (see the references below).

Lawvere observed that a simple yet powerful characterization of the notion of _infinitesimal space_ $D$ is that $D$ is an [[object]] in a [[topos]] $\mathcal{T}$ of [[space]]s such that the [[inner hom]] [[functor]] $(-)^D : \mathcal{T} \to \mathcal{T}$ has a [[right adjoint]].

If the [[topos]] in question furthermore is equipped with a [[lined topos|line object]] $R$ that plays the role of the _real line_ $\mathbb{R}$ then a sensible notion of _infinitesimal quantities_ in $R$ is obtained when all [[morphism]]s $D \to R$ from infinitesimal spaces $D$ are necessarily _linear_ maps. This is now known as the [[Kock-Lawvere axiom]] on [[lined topos]]es $(\mathcal{T}, R)$. When it is satisfies $(\mathcal{T}R)$ is called a [[smooth topos]]. The study of these is known as [[synthetic differential geometry]].

The notion of infinitesimal object and infinitesimal space then makes sense in any [[smooth topos]], and may be reasoned about generally for all smooth toposes. In any concrete [[Models for Smooth Infinitesimal Analysis|model]] for the axioms there will accordingly be concrete realizations of these infinitesimal objects.

### Realizations in algebraic geometry 

Notably, for instance the [[Grothendieck topos]] of [[presheaf|presheaves]] on the [[opposite category]] $k CAlg^{op}$ of that of commutative $k$-[[algebra]]s (over some [[field]] $k$) is a simple realization of a [[smooth topos]] (see for instance [Kock-SGM, section 93](http://home.imf.au.dk/kock/SGM-final.pdf)). This topos and its variants and in particular their [[category of sheaves|sheaf]]-[[localization]]s provide the context in which [[algebraic geometry]] takes place.

Therefore the notion of infinitesimals in [[algebraic geometry]] may be understood as being models of the general notion of infinitesimals in [[synthetic differential geometry]] in context such as $\mathcal{T} = Sh(k CAlg^{op})$ or similar.

The vast majority of existing work on infinitesimals and infinitesimal neighbourhoods comes from [[algebraic geometry]]. It is the foundation of Grothendieck's approach to [[regular differential operators]], to costratifications, [[crystalline cohomology]] and [[Grothendieck connection|de Rham descent]]. 

Similar infinitesimal thickenings also appear in the [[noncommutative geometry]] of Kapranov, and in the language of [[abelian category|abelian categories]] of [[quasicoherent sheaf|quasicoherent sheaves]] in the work of Lunts and Rosenberg on regular [[differential operator]]s in the content of [[noncommutative geometry]], which strongly takes into account [[tensor product]]s.

### Comparison to infinitesimals in nonstandard analysis 

Another notion of infinitesimals has been has arisen in the context of [[nonstandard analysis]]. The infinitesimal quantities considered there differ from the general ones in [[synthetic differential geometry]] in that they are all _invertible_ (their inverses being "infinitely large").   Nevertheless, one can construct models of [[synthetic differential geometry]] which, in addition to nilpotent infinitesimals, contain invertible infinitesimals; see for instance [[Models for Smooth Infinitesimal Analysis|MSIA, chapters VI and VII]].  Such invertible infinitesimals can be applied in some of the same ways as the infinitesimals of nonstandard analysis.

However, as pointed out in MSIA (intro. to Chapter VII), "there are some obvious differences."  The primary tool used in nonstandard analysis is a completely general [[transfer principle]], saying that any statement in the ordinary world is also true in the nonstandard world.  In particular, this implies that the infinitesimal and infinitely large quantities in nonstandard analysis obey all the same rules of arithmetic and analysis as do the standard ones.  By contrast, a limited sort of transfer principle relating a pair of specific models for SDG is proven in MSIA, but it applies only to statements of a certain logical form.  Moreover, the arithmetic of invertible infinitesimals in SDG has some unfamiliar aspects: for instance, mathematical induction is only valid for statements of a certain logical form, and the axiom of finite choice fails.

The construction of models for nonstandard analysis does, however, have a topos-theoretic description, using [[filterpower]]s.


## Definition 

### Atomic object 

+-- {: .un_defn}
###### Definition (Lawvere)

In a [[cartesian closed category]] $C$ an [[object]] $D$ is called **infinitesimal** **atomic** if the [[hom-functor]]
$(-)^D : C \to C$ for maps out of $D$ (i.e. the functor of 
[[exponential object|exponentiation]] by $D$) is a [[left adjoint]], i.e.
if it has a [[right adjoint]].
=--

In particular, since every [[left adjoint]] functor preserves colimits,
such an object is in particular a [[tiny object]] and in particular a [[compact object]].


+-- {: .un_remark}
###### Remark 
**(intuitive interpretation)**

Here is how to think of what this definition means intuitively. For that, notice how maps out of an ordinary space fail to preserve [[colimit]]s:

for definiteness, consider the case of a [[cover]] of a [[space]] $X$ by spaces $\{U_i \to X\}_i$ so that $X$ is the [[coequalizer]]

$$
  (\coprod_{i,j} U_i \times_X U_j)
  \stackrel{\to}{\to}
  (\coprod_i U_i)
  \to X
$$

as discussed in detail at [[sieve]] and [[sheaf]]. This says effectively that every point of $X$ is element of at least one of the covering spaces $U_i$ and that one obtains $X$ by identifying the points in the covering spaces that correspond to the same one in $X$.

Now let $\Sigma$ be any other space. We may assume here that the [[internal hom]] $[\Sigma,-] : T \to T$ at least preserves [[coproduct]]s, so that applying this functor to the above diagram yields

$$
  (\coprod_{i,j} [\Sigma,U_i \times_X U_j])
  \stackrel{\to}{\to}
  (\coprod_i [\Sigma,U_i])
  \to [\Sigma,X]
  \,.
$$

Now notice how this will in general fail to still be a [[coequalizer]]: if it were, for one the morphism $  (\coprod_i [\Sigma,U_i])
  \to [\Sigma,X]$ would have to be an [[epimorphism]]. But this can't be in general, because it would mean that every map $\Sigma \to X$ factors through one of the covering spaces. The problem here is that in general the image of $\Sigma \to X$ may be _larger_ than any of the $U_i$.

This is maybe most familiar in the context of [[loop space]]s (for $\Sigma$ the circle): the loop space of a cover of $X$ is not in general a cover of the loop space.

But suppose that $\Sigma$ were infinitesimal. One thning that should mean is that there is no other space that is "effectively smaller" in some useful sense. For $\Sigma$ infinitesimal, we do expect that every map $\Sigma \to X$ can always be factored through at least one of the $U_i$: because $\Sigma$ is so small, the image of a map out of it can never be too large.

So only if $\Sigma$ qualifies as having infinitesimal extension can the functor $[\Sigma,-]$ be expected to preserve colimits.

=--


### Formal infinitesimal space 

+-- {: .un_def}
###### Definition **(formal infinitesimal space)**

An object $\Delta$ in a [[smooth topos]] $(\mathcal{T}, R)$
is called a **formally infinitesimal object** if it is the
algebra-spectrum of (what in the [[synthetic differential geometry|sdg]]-literature is usually called) a _Weil-$R$-algebra_ in $\mathcal{T}$

$$
  \Delta \simeq Spec_R(W)
  \,.
$$

=--


Here

* $W = R \oplus J$ is an [[internalization|internal]] $R$-algebra object in $\mathcal{T}$ with $J$ an $R$-finite dimensional nilpotent ideal
  
* $Spec_R(W) := R Alg_{\mathcal{T}}(W,R) \subset R^W$ is the [[subobject]] of the [[internal hom]] of morphisms that respect the $R$-algebra structure on $W$ and $R$.


All the spaces that are described as collection of degree $n$ infinitesimal neighbours are of this form. Infinitesimal spaces not of this form are germ-spaces (see the examples below). These violate the finite-dimensionality assumption on $J$.



## Examples 


### Infinitesimal intervals 

There are several different objects that one may think 
of as an infinitesimal interval. 

The smallest of them is often denoted $D$ and sometimes called the **disembodied tangent vector** or the *walking tangent vector** . 

This is described in more detail at

* [[infinitesimal interval object]].

It is such that a morphism $D \to X$ into a [[manifold]] $X$ is the same as
a choice of point $x \in X$ and of a [[tangent vector]] 
$v \in T_x X$. Equivalently, it is such that restricting a smooth function $f : \mathbb{R} \to \mathbb{R}$ along the inclusion  $D \hookrightarrow \mathbb{R}$ produces the first-order [[jet]] defined
by $f$ at the point $0 \hookrightarrow D \to \mathbb{R}$.

Accordingly, for each $k \in \mathbb{N}$ 
there is a "slightly bigger" infinitesimal interval often denoted $D_k$, which is such that restricting a smooth function $f : \mathbb{R} \to \mathbb{R}$
along $D_k \to \mathbb{R}$ produces the order-$k$ jet represented by this 
function at the given point. 

Still infinitesimal but bigger than all these is the object 
$\Lambda_0 := \cap_{0 \in U \subset \mathbb{R}} U$ of intersections of all neighbourhods of the origin of $\mathbb{R}$. This is such that the restriction of
a map $f : \mathbb{R} \to \mathbb{R}$ along $\Lambda_0 \hookrightarrow \mathbb{R}$
produces the [[germ]] of $f$ at $0$. 


### The standard infinitesimal interval 

#### Models

The classical example of a realization of an infinitesimal object is in terms of what is (traditionally but undescriptively) called the _ring of [[dual number]]s_. For that we place ourselves in some context in which [[space]]s are characterized [[duality|dually]]
in terms of the [[space and quantity|quantities]] on them, i.e. in terms of their would-be function algebras. 

For some real number $t \in \mathbb{R}$, 
functions on the closed [[interval]] $[-t,t] \subset \mathbb{R}$  of length $2 t$ may be thought of 
as represented by functions on the whole real line $\mathbb{R}$, where two representatives represent the same function on the interval if they differ
by a function that vanishes on the interval.

Precisely: 

+-- {: .un_lemma}
###### Lemma

The ([[generalized smooth algebra|generalized smooth]]) algebra of smooth 
functions $C^\infty([-t,t])$ on $[-t,t]$ is isomorphic to the quotient of the
algebra of smooth functions $C^\infty(\mathbb{R})$ on all of $\mathbb{R}$ by the
functions that vanish on $[-t,t]$

$$
  C^\infty([-t,t]) \simeq C^\infty(\mathbb{R})/\{f \in C^\infty(\mathbb{R})| \forall x \in [-t,t]: f(x) = 0\}
    \,.
$$
=--

+-- {: .proof}
###### Proof

This is a corollary of the smooth version of the [[Tietze extension theorem]], 
which says that for $U \subset \mathbb{R}^n$ a closed subset, every smooth
function on $U$ extends to a smooth function on all of $\mathbb{R}^n$.

See page 20 of [[Models for Smooth Infinitesimal Analysis|MSIA]].
=--


As we think of the length of the interval shrinking to an infinitesimal  value, the notion of derivative of functions is such that we want to say
that the statement "a function vanishes on the infinitesimal interval" is equivalent to "a function vanishes at the origin and its first derivative there vanishes,  too". This in turn is usually equivalent (in a smooth context) to "a function is a square of a function that vanishes at the origin".


Accordingly, in a context where one considers [[polynomial]] functions over the [[ground field]]
$k$, the infinitesimal
interval is given by the [[space]] -- usually called $D$ --
that is [[duality|dual]] to the [[ring]]
$k[\epsilon] := k[Z]/Z^2$ which is the quotient of the polynomial ring in 
one variable $Z$ modulo the polynomial $Z^2$. This is often called the 
**ring of dual numbers** (where the term 'dual' historically refers to its being $2$-dimensional). In terms of generators and relations this is the ring
generated by a single element $\epsilon$ subject to the relation that $\epsilon^2 = 0$.

Similarly, in the smooth context of, for instance, Moerdijk--Reyes
_[[Models for Smooth Infinitesimal Analysis]]_, $D$ is the [[space]] [[duality|dual]]
to the [[generalized smooth algebra]] $C^\infty(\mathbb{R})/J^2$ obtained as the
smooth functions on the real line modulo squares of functions that vanish at the origin.

+-- {: .un_defn}
###### Definition (the $1$-dimensional infinitesimal space)

In the context of [[generalized smooth algebra]], the $1$-dimensional infinitesimal
space is the space $D$ whose function algebra is the quotient 

$$
  C^\infty(D) := C^\infty(\mathbb{R})/\{x^2\}
$$

of all functions on the real line, modulo those that are a product with the function $x \mapsto x^2$.
=--

This does reproduce the above ring of dual numbers due to the [[Hadamard lemma]], which says that for $g \in C^\infty(\mathbb{R})$ a smooth function, there exists
a smooth function $h \in C^\infty(\mathbb{R})$ such that for all $x \in \mathbb{R}$
we have $g(x) = g(0) + x g'(x) + x^2 h(x)$. So modulo $x^2$, every smooth function is in fact
a polynomial function. 

+--{.query}
Zoran:  reason, if my memory is right, Leites in his around 1976 survey of supermanifolds proveds and puts important role of Hadamard's lemma in supercontext, but I do not recall details, maybe somebody shoudl check.
=--

See pages 19&20 of _[[Models for Smooth Infinitesimal Analysis|MSIA]]_.

In this dual generators-and-relations description, the infinitesimal interval is very familiar in many mathematically less sophisticated contexts. It prevails for instance
in the basic physics textbook treatment since [[Isaac Newton]] up to this day. [[Sophus Lie]] is famously
quoted as having said that he found many of his famous insights by such 
"synthetic reasoning" and only a lack of proper formalization prevented him
from writing them up in this way instead of in the more wide-spread way of 
differential calculus.


#### Axiomatics

More generally, one may abstract the above properties of concrete realizations
of the infinitesimal interval such as to get such a notion in an arbitrary suitable
context. A suitable context for [[synthetic differential geometry]] is any
[[topos]] $C$ equipped with an [[internalization|internal]] [[commutative ring]] $R$. 

Using the [[topos]]-[[internal logic]] we may speak of both $R$ and $D$ as 
if they were [[set]]s, where "element" means [[generalized element]]. This 
way we have:

+-- {: .un_defn}
###### Definition (infinitesimal interval object)

Let $(\mathcal{T}, R)$ be a [[smooth topos]]. Then the **[[infinitesimal interval object]]**
$D$ is the [[subobject]] of $R$ of all those elements whose square is 0.

$$
  D = \{x \in R | x^2 = 0\}
$$
=--

It may be helpful to recall that in terms of [[limit]]s this notation means that
$D$ is the [[equalizer]] of 

$$
  R \stackrel{(-)^2}{\to} R
$$

and

$$
  R \stackrel{}{\to} 0 \stackrel{}{\to} R
  \,.
$$

For with $x : U \to D$ any morphism embodying a generalized element
$x \in D$, the universal property of the [[limit]] identifies this
uniquely with a morphism $U \to R$, hence with a generalized element 
of $R$, such that $U \to R \stackrel{(-)^2}{\to} R$ is the $0$ element 
of $R$ with domain of definition $U$ : $\cdots = U \to 0 \to R$.


### The cartesian product of infinitesimal intervals 

This works analogously to how the $k$-[[cube]] is the $k$-fold [[cartesian product]]
$D^k$ of the [[unit interval]] $[-1,1]$ with itself.

+-- {: .un_defn}
###### Definition

The infinitesimal $k$-cube $D^k$ is the $k$-fold cartesian product of the
infinitesimal interval $D$ with itself.

This means that in terms of generalized elements we have

$$
  D^k = \{(x_1, \cdots, x_n) \in R^n | \forall j,k  : \;x_j \cdot x_k = 0 \}
$$
=--


### The $k$-dimensional infinitesimal interval

+-- {: .un_defn}
###### Definition

For $n\in \mathbb{N}$ the $k$-dimensional infinitesimal interval is

$$
  D(n) := \{ (x_1,\cdots, c_k) \in R^k | \forall j,k : x_j \cdot x_k = 0 \}
$$
=--

+-- {: .un_remark}
###### Remark

Since in particular $x_j^2 = 0$ for all elements of the 
infinitesimal $n$-disk, we have an inclusion

$$
  D(n) \subset D^n
$$

which is proper if $n \gt 1$. For $n = 1$ we have $D(1) = D$.

While $D(n)$ is closed under multiplication by elements of $R$, it is
not in general closed under addition of its elements. For instance for
$d_1,d_2 \in D(1) = D$ we have that $d_1 + d_2$ (the operation being in $R$)
is still in $D$ precisely if $(d_1,d_2)$ is in $D(2)$.
=--


### The infinitesimal neighbourhood 

For $x \in X$ a point in a manifold, the infinitesimal [[neighbourhood]] $U_p$ is the intersection of all open neighbourhoods of $x$. This is such that the restriction of a function $f : X \to \mathbb{R}$ along the inclusion $U_p \to X$ is precisely the [[germ]] of the function $f$.

All of the infinitesimal spaces above are contained in the corresponding infinitesimal neighbourhood. So this is the "largest" of the infinitesimal spaces discussed here.


### Spaces of infinitesimal $k$-simplices

An **infinitesimal $k$-[[simplex]]** in $R^n$ based at the origin is a collection $(\vec x_i \in R^n)_{i = 1}^k$ of points in $R^n$, such that each is an infinitesimal neighbour of the origin

$$
  \forall i : \;\; \vec x_i \sim 0
$$ 

and each are infinitesimal neighbours of each other

$$
  \forall i,j: \;\; (\vec x_i - \vec x_j) \sim 0
  \,.
$$

Following section 1.2 of

* [[Anders Kock]],  _Synthetic differential geometry of manifold_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

we write $\tilde D(k,n)$ for the space of all infinitesimal $k$-simplices in $R^n$. More precisely, this is defined as the formal dual of the algebra $C^\infty(\tilde D(k,n))$ defined as follows.

+-- {: .un_def}
###### Definition

The algebra $C^\infty(\tilde D(k,n))$ is the 
commutative $\mathbb{R}$-algebra generated from $k \times n$ generators $(x_i^j)_{1 \leq i \leq n, 1 \leq j \leq n}$ subject to the relations

$$
  \forall i, j,j' : \;\; x_i^{j} x_i^{j'} = 0
$$

and

$$
  \forall i,i',j,j'   : \;\;\; (x_i^j - x_{i'}^j) (x_i^{j'} - x_{i'}^{j'}) = 0
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

By multiplying out the latter set of relations and using the former, these relations are seen to be equivalent to the set of relations

\[
  \forall i,i',j,j' : \;\;\;
  x_i^j x_{i'}^{j'} + x_{i'}^j x_{i}^{j'} = 0
  \,.
\]

Notice that this implies also that

$$
  \forall i,i', j: \;\;\;  x_i^{j} x_{i'}^j = 0
  \,.
$$

=--

A general element $f$ of this algebra we think of as a function on a certain infinitesimal neightbourhood of the origin of $R^{k \cdot n}$, interpreted as the space of infinitesimal $k$-simplices in $R^n$ based at 0.

Since $C^\infty(\tilde D(k,n))$ is a Weil algebra in the sense of synethtic differential geometry, its structure as an $\mathbb{R}$-algebra extends uniquely to the structure of a [[smooth algebra]] and we may think of $\tilde D(k,n)$ as an infinitesimal [[smooth locus]].

+-- {: .un_example}
###### Example

For $n = 2$ and $k = 2$ we have that $C^\infty(\tilde D(2,2))$ consists of elements of the form

$$
  \begin{aligned}
    a \cdot x_1 + b \cdot x_2 + (v \cdot x_1) (w \cdot x_2) 
    &= 
    a_1 x_1^1 + a_2 x_1^2 + b_1 x_2^1 + b_2 x_1^2
    \\
    & (v_1 w_2 - v_2 w_1) \frac{1}{2}(x_1^1 x_2^2 - x_1^2 x_2^1)
  \end{aligned}
$$

for $(a, b, v, w \in (\mathbb{R}^n)^*)_{1 \leq i \leq n}$ a collection of ordinary covectors and with "$\cdot$" denoting the evident contraction, and where in the last step we used the above relations.

It is noteworthy here that the coefficient of the term which is linear in each of the $x_i$ is the wedge product of two covectors: we may naturally identify the subalgebra of $C^\infty(\tilde D(2,2))$ on those elements that vanish if either $x_1$ or $x_2$ are set to 0 as space $\wedge^2 T_0^* \mathbb{R}^2$ of 2-forms at the origin of $\mathbb{R}^2$. 

Of course for this identification to be more than a meaningless coincidence we need that this is the beginning of a pattern that holds more generally. But this is indeed the case.

=--

Let $\Xi$ be the set of _square_ submatrices of the $k \times n$-matrix $(x_i^j)$. For \xi \in \Xi$ a submatrix, we write $det(\xi)$ for the corresponding [[determinant]], computes as a product in $C^\infty(\tilde D(k,n))$.


+-- {: .un_prop}
###### Proposition


The elements $f \in C^\infty(\tilde D(k,n))$ are precisely of the form

$$
  f = \sum_{\xi \in \Xi} det(\xi) f_\xi
$$

for _unique_ $\{f_\xi \in \mathbb{R} | \xi \in \Xi\}$.

=--

+-- {: .un_prop}
###### Proposition

This is a direct extension of the argument in the above example: a general product of $r$ generators in $C^\infty(\tilde D(k,n))$ is

$$
  x_{i_1}^{j_1} x_{i_2}^{j_2} \cdots x_{i_r}^{j_r}
  \,.
$$

By the relations in $C^\infty(\tilde D(k,n))$, for any permutation $\sigma$ of $r$ elements, this is equal to

$$
  \cdots = sgn(\sigma) x_{i_1}^{j_{\sigma}} x_{i_2}^{\sigma(j_{\sigma(2)})} \cdots x_{i_r}^{j_{\sigma(r)}}
  \,,
$$

where $sgn(\sigma) \in \{+1, -1\} \subset \mathbb{R}$ is the [[signature]] of the permutation. It follows that each such element may be written as

$$
  \cdots = \frack{1}{r!} det(x_{i_{\bullet}}^{j_{\bullet}})
$$

for $(x_{i_\bullet}^{j_\bullet}) \in \Xi$ the corresponding submatrix of $(x_i^j)$.

=--

+-- {: .un_remark}
###### Remark

In section 1.3 of

* [[Anders Kock]],  _Synthetic differential geometry of manifold_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

effectively this proposition appears as the "[[Kock-Lawvere axiom]] scheme for $\tilde D(k,n)$" when $\tilde D(k,n)$ is regarded as an object of a suitable [[smooth topos]]. It is useful to record this simple but very crucial observation of Anders Kock here in the category $Alg_{\mathbb{R}}^{op}$ or in the category $C^\infty Alg^{op}$ of [[smooth loci]], as we do here, where it is just a simple observation. The point of the Kock-Lawvere axiom scheme is effectively to ensure that the properties of $C^\infty(\tilde D(k,n)) \in C^\infty Alg^{op}$ are preserved under [[Yoneda embedding]] into a corresponding [[sheaf topos]]. But it has been observed that it serves to clarify what is going on in parts of Ander Kock's book by separating the combinatorial and algebraic arguments from their internalization into suitable [[smooth topos]]es.

=--

Let $C^\infty(\tilde D(k,n))_{top}$ be the sub-[[vector space]] of the underlying vector space of $C^\infty(\tilde D(k,n))$ on those elements that vanish if the collection of generators $x_i = (x_i^1 , x_i^2, \cdots, x_i^n)$ is set to 0, for all $i$. This are those elements that are linear combinations of the form $\sum_{\xi_{top} \in Xi_{top}} det(\xi_{top}) f_{\xi_{top}}$, for $\xi_{top}$ ranging over the $k \times k$-submatrices of $(x_i^j)$.


+-- {: .un_corollary}
###### Corollary


The map 

$$
  \wedge^k (\mathbb{R}^n)^* \to C^\infty(\tilde D(k,n))_{top}
$$

given by

$$
  \omega^1 \wedge \omega^2 \wedge
  \cdots \wedge \omega^k
  \mapsto
  (\omega^1 \cdot x_1) (\omega^2 \cdot x_2) \cdots
  (\omega^k \cdot x_k)
$$

is well defined and constitutes an [[isomorphism]] of vector spaces.

=--

So inside the space of functions on infinitesimal simplices, we find the differential forms. The next crucial observation now is that there is a _natural reason_ to restrict to $C^\infty(\tilde D(k,n)) \subset C^\infty(\tilde D(k,n))$.

...


## References

Infinitesimal spaces and their properties were familiar in all
those areas where spaces are characterized by the algebras of functions on them.

It was in a seminal lecture 

* [[William Lawvere]], _Categorical Dynamics_ lectures at the University of Chicago (1967) 

reproduced in  

* [[Anders Kock]], _Topos theoretic methods in Geometry_, Aarhus Universitet (1979)

that the proposal was made
to axiomatize the properties of infinitesimal objects by making use
of the fact that they are supposed to be objects of a 
[[cartesian closed category]].

It was from this insight that [[synthetic differential geometry]] was
eventually developed. 

* Lawvere, _Outline of synthetic differential geometry_,
([web](http://www.acsu.buffalo.edu/~wlawvere/downloadlist.html))

This is a classical case of [[general abstract nonsense]] used to
understand a subtle situation.

A summary and discussion of the axiomatically defined standard infinitesimal 
objects $D$, $D_k$, $D_k(n)$ is in section 1.2 of

* Anders Kock, _Synthetic Geometry of Manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

### Atomic spaces 

Details on the right adjoint to the exponentiation functor $(-)^X$ for
$X$ an infinitesimal object are in appendix 4 of 

* Moerdijk, Reyes, _[[Models for Smooth Infinitesimal Analysis]]_


### Formally infinitesimal spaces 

For formal infinitesimal objects and Weil algebras see 

section I.16 of 

* [[Anders Kock]], _Synthetic differential geometry_ ([pdf]())

and chapter I, section 4 and chapter II, theorem 1.13 and onwards in

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal  Analysis]]


## Discussion

+-- {: .query}
Do all of the following really involve infinitesimal *objects*?  Or should we move the others to [[infinitesimal quantity]] to clarify that this page is about objects of categories as defined below?  ---Toby

[[Urs Schreiber]]: good point. I think Lawvere's definition is, as stated, to be thought of as defining _infinitesimal space_s, yes. For infinitesimal quantities it will likely have to be dualized (in the hopefully obvious way). 

So maybe we should rename the entry here into _infinitesimal space_ and, yes, create another entry on infinitesimal quantities. Yes, I think that's a good idea. I have to run now, but I can implement it later.

_Toby_:  I could do it too, although I\'d like to see what Zoran thinks.

_Zoran_: I don't really feel/know what is the most sensitive here. Surely our understanding is developing and we will see more in future (you see yet another thing are the sheaves supported on infinitesimal neighborhoods as well as the duality between infinitesimals and (regular) differential operators in algebraic setting, the duality whose analogue I do not understand in the smooth context (cf. Maszczyk 0611806). 
=--



[[!redirects infinitesimal objects]]
[[!redirects infinitesimal quantity]]
[[!redirects infinitesimal quantities]]
[[!redirects infinitesimal space]]
[[!redirects infinitesimal spaces]]
