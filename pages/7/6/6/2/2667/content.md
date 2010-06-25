#Contents#
* automatic table of contents goes here
{:toc}


## Idea and definition ##

Classically, a **Schur functor** is a specific sort of [[functor]] 

$$F: FinVect_{\mathbb{C}} \to FinVect_{\mathbb{C}}$$ 

on the category of finite-dimensional complex [[vector space|vector spaces]].  Namely, it is a functor where $F(V)$ is obtained by taking a [[tensor power]] of $V$, say $V^{\otimes n}$, and then picking out the subspace that transforms according to a particular [[irreducible representation]] of the [[symmetric group]] $S_n$, which acts on $V^{\otimes n}$ by permuting the tensor factors.  

The irreducible representations of $S_n$ correspond to $n$-box [[Young diagram|Young diagrams]], so a Schur functor of this sort is named by a Young diagram. This is the beginning of a long and fascinating story connecting Schur functors with other objects that are named by Young diagrams: for example, elementary [[symmetric function|symmetric functions]] and [[cohomology]] classes on BGL, the classifying space for [[vector bundles]].  

More generally, any finite direct sum of the Schur functors described above may be called a Schur functor.  This gives a category of Schur functors and natural transformations between them.  Since the coproduct of all the symmetric groups $S_n$ is equivalent to the groupoid of finite sets and bijections, say $FinSet^\times$, it is not surprising that this category of Schur functors is equivalent to the functor category

$$  [FinSet^\times, FinVect_{\mathbb{C}}] \, , $$

This category could be called the 'category of finite-dimensional complex representations of the groupoid of finite sets', or the 'category of finite-dimensional linear [[species]]'.  

The category of representations of any groupoid has many nice features: for example, it is a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]], meaning roughly that it has a well-behaved tensor product, direct sums, kernels, and cokernels.   So, the category of Schur functors

$$  [FinSet^\times, FinVect_{\mathbb{C}}] \, , $$

is of this sort.  But, it is also [[semisimple abelian category|semisimple]]: indeed, every Schur functor is a finite direct sum of 'irreducible' Schur functors, which correspond to Young diagrams.

The category of representations of a groupoid has even more nice features when the groupoid itself has a [[monoidal category|monoidal structure]]: then the representation category acquires a monoidal structure thanks to [[Day convolution]].  The groupoid $FinSet^\times$ has, in fact, _two_ important monoidal structures, coming from the product and disjoint union of finite sets --- and since product distributes over disjoint union, $FinSet^\times$ is a [[rig category]].  This is all reflected in the category of Schur functors.

On top of all this, it turns out that the composite of Schur functors is again a Schur functor.  In the classical literature this is called [[plethysm]].  This gives the category

$$  [FinSet^\times, FinVect_{\mathbb{C}}] \, , $$

yet another, perhaps unexpected monoidal structure.

In more modern treatments, a Schur functor is a functor defined on [[module|modules]] over more general [[commutative ring]] $R$ (possibly with some conditions on $R$), so that "Schur functor" really connotes a family of functors 

$$F_R: Mod_R \to Mod_R  \, .$$ 

And indeed, much of the theory of Schur functors can be generalized even further, to categories of [[group representations]], [[vector bundles]], [[coherent sheaves]] and the like.  In this article, Todd Trimble and John Baez plan to explore the scope of such generality and --- we hope --- write a paper about what we find.

## Examples ##

The first thing that should be understood from the beginning is that a general Schur functor $F$ is _nonlinear_: the action on [[hom-set|hom-sets]] 

$$hom(V, W) \to hom(F(V), F(W))$$ 

is not assumed to respect the linear structure. In fact, linear Schur functors are rather uninteresting: because every finite-dimensional space is a finite [[direct sum]] of copies of the $1$-dimensional space $\mathbb{C}$, and because [[linear functor|linear functors]] preserve finite direct sums (that is, [[biproduct|biproducts]], it turns out that every linear Schur functor $F$ is [[representable functor|representable]] as $hom(X, -)$ where $X = F(\mathbb{C})$.  So, the category of linear Schur functors is equivalent to $FinVect_{\mathbb{C}}$. 

More representative examples of Schur functors include: 

* For each $k \geq 0$, the $k^{th}$ [[tensor power]] $V \mapsto V^{\otimes k}$ is a Schur functor. 

* For each $k \geq 0$, the $k^{th}$ [[symmetric algebra|symmetric power]] $V \mapsto S^k(V)$ is a Schur functor. 

* For each $k \geq 0$, the $k^{th}$ [[exterior algebra|alternating power]] $V \mapsto \Lambda^k(V)$ is a Schur functor. 

Even though Schur functors do not respect the linear structure on homsets, the category $Schur$ of Schur functors is nevertheless a [[linear category]], so we can talk about [[irreducible object|irreducible objects]], decompositions into [[direct sum|direct sums]], and so on. It turns out that every Schur functor $F$ can be expressed as a direct sum of irreducible $Schur$-objects $S_\lambda$ indexed by [[Young diagram]]s $\lambda$, and these $S_\lambda$ are usually what people think of when they say "Schur functors". 

## Schur functors associated with Young diagrams ##

Functors such as the $k^{th}$ alternating power, $k^{th}$ symmetric power, etc. make sense in much wider contexts than just $FinVect_{\mathbb{C}}$.   They also make sense on categories of group representations, chain complexes, group representations, coherent sheaves of vector spaces, and so on.  

To understand them more generally, let $C$ be any [[symmetric monoidal category|symmetric monoidal]] [[Cauchy complete category|Cauchy complete]] [[category]] enriched over $FinVect_k$, where $k$ is any field of characteristic zero.   (In the present context, Cauchy completeness means that $C$ has [[biproducts]], also known as [[direct sums]], and also that [[idempotent|idempotents]] [[splitting|split]].)

Recall that the [[group algebra]] $k[S_n]$ decomposes as a direct sum of matrix algebras 

$$\bigoplus_{\lambda} hom(V_\lambda, V_\lambda)$$ 

where $\lambda$ ranges over isomorphism classes of irreducible representations of $S_n$, $V_\lambda$ is any representation chosen from its isomorphism class, and the $\hom$ here is the hom of underlying vector spaces. In more concrete terms, these representations $V_\lambda$ are labelled by $n$-box [[Young diagram|Young diagrams]].   At the level of $S_n$-representations, we have

$$k[S_n] \cong \bigoplus_{\nu} V_{\nu}$$ 

where this time $\nu$ ranges over $n$-box [[Young tableau]]x, and $V_\nu$ represents the irreducible subrepresentation of $k[S_n]$ attached to $\nu$.  

This group algebra lives as a [[monoid]] in the symmetric monoidal category $FinVect_k$. We would also like to interpret it as living in $C$, by "change of base" from $FinVect_k$ to $C$. 

### Change of base ###

To achieve this change of base, let $Mat$ be the $k$-linear category whose objects are integers $m \geq 0$ and whose morphisms $m \to n$ are $m \times n$ matrices with entries in $k$. There is an evident linear functor 

$$Mat \to C$$ 

which takes $m$ to $I^m$, the direct sum of $m$ copies of the tensor unit $I$. It is the unique linear functor taking $1$ to $I$, up to unique linear isomorphism. In the case $C = FinVect_k$, the linear functor 

$$Mat \to FinVect_k,$$ 

taking $1$ to $k$, is a linear equivalence (exhibiting $Mat$ as a [[skeleton]] of $C$). Thus we could equally well say that there is a linear functor 

$$i: FinVect_k \to C$$ 

which, up to unique linear isomorphism, is the unique linear functor taking $k$ to $I$. Notice that a [[symmetric monoidal functor]] of this form must take the tensor unit $k$ to $I$ (up to coherent isomorphism, as always), and in fact $i$ is symmetric monoidal, because there is a canonical isomorphism

$$I^m \otimes I^n \cong I^{m n},$$ 

using the fact that $\otimes$ preserves direct sums in each argument, and the fact that there is a canonical isomorphism $I \otimes I \cong I$. 

In summary, we have the following proposition. 

+-- {: .un_prop}
######Proposition 
There is exactly one symmetric monoidal linear functor 
$i: FinVect_k \to C$, up to symmetric monoidal linear isomorphism. 
=--

(As a matter of fact, $i: FinVect_k \to C$ can also be described as the left adjoint to the lax monoidal functor $\hom(I, -): C \to FinVect_k$, and it is well known that such left adjoints carry strong monoidal structure.) 

This symmetric monoidal functor $i$ therefore maps the group algebra $k[S_n]$, as a [[monoid]] in the monoidal category $FinVect_k$, to a monoid in $C$, which we again call $k[S_n]$ by abuse of notation.  It also maps each of the Young tableau representations $V_\nu$, as a module over $k[S_n]$ in $FinVect_k$, to a corresponding module over the monoid $k[S_n]$ in $C$, which we again denote by $V_\nu$. 

### Modules over a bimonoid ###

Next we exploit the fact that, just like any [[group algebra]], $k[S_n]$ is a cocommutative [[bialgebra]] --- or in fancier language, a cocommutative [[bimonoid]] in the symmetric monoidal category $FinVect_k$.  Since $i : FinVect_k \to C$ is a symmetric monoidal category, this means that $i$ carries $k[S_n]$ to a commutative bimonoid in $C$.  As noted above, we call bimonoid by the same name, $k[S_n]$.

The category of modules over a cocommutative bimonoid is a symmetric monoidal category. More explicitly, in the case of the bimonoid $k[S_n]$ in $C$ with comultiplication 

$$\delta: k[S_n] \to k[S_n] \otimes k[S_n],$$

the tensor product $V \otimes W$ of two $k[S_n]$-modules in $C$ carries a module structure where the action is defined by 

$$k[S_n] \otimes V \otimes W \stackrel{\delta \otimes 1_{V \otimes W}}{\to} k[S_n] \otimes k[S_n] \otimes V \otimes W \stackrel{1 \otimes \sigma \otimes 1}{\to} k[S_n] \otimes V \otimes k[S_n] \otimes W \stackrel{\alpha_V \otimes \alpha_W}{\to} V \otimes W$$ 

where $\sigma$ is a symmetry isomorphism and $\alpha_V$, $\alpha_W$ are the actions on $V$ and $W$. 

### Definition of Schur functors on $C$ ###

Now we consider a particular case of tensor product representations. If $X$ is an object of $C$, the symmetric group $S_n$ has a representation on $X^{\otimes n}$. (Indeed, for each $\sigma \in S_n$, there is a corresponding symmetry isomorphism $X^{\otimes n} \to X^{\otimes n}$. From this one may construct an action 

$$k[S_n] \otimes X^{\otimes n} \cong \bigoplus_{\sigma \in S_n} I \otimes X^{\otimes n} \to X^{\otimes n}$$ 

which is the required representation.) So, if $V_\nu$ is a Young tableau representation of $k[S_n]$ in $C$, we obtain a tensor product representation 

$$V_\nu \otimes X^{\otimes n}$$ 

of $k[S_n]$ in $C$. 

Consider next the **averaging operator** $e = \frac1{n!} \sum_{\sigma \in S_n} \sigma$: 

$$e: V_\nu \otimes X^{\otimes n} \to V_\nu \otimes X^{\otimes n}$$ 

This operator makes sense since $k$ has characteristic zero, and crucially, this operator is _idempotent_ (because $e = \sigma e$ for all $\sigma \in S_n$). Because we assume idempotents split in $C$, we have a (split) coequalizer 

$$V_\nu \otimes X^{\otimes n} \stackrel{\overset{e}{\to}}{\underset{1}{\to}} V_\nu \otimes X^{\otimes n} \to V_\nu \otimes_{S_n} X^{\otimes n}$$

We may now define the Schur functor $S_\nu$ on $C$ attached to a Young tableau $\nu$. 

+-- {: .un_def}
######Definition 
The **Schur functor** $S_\nu: C \to C$ is defined as follows. Given an object $X$ of $C$, $S_\nu(X)$ is the object of $S_n$-coinvariants $V_{\nu} \otimes_{S_n} X^{\otimes n}$. Given a morphism $f: X \to Y$ in $C$, $S_\nu(f)$ is the unique map $S_\nu(X) \to S_\nu(Y)$ such that 
$$\array{
V_\nu \otimes X^{\otimes n} & \to & S_\nu(X) \\
1 \otimes f^{\otimes n} \downarrow \; \; & & \downarrow S_\nu(f) \\
V_\nu \otimes Y^{\otimes n} & \to & S_\nu(Y)
}$$ 
commutes, where the horizontal arrows are the coequalizer maps. 
=--

As we have constructed them, there is one such functor for each Young tableau.  However, different Young tableaux with the same underlying Young diagram give isomorphic representations of $S_n$ and thus naturally isomorphic Schur functors.  So, it is more typical to say there is one Schur functor $S_\lambda$ for each Young diagram $\lambda$.

More generally we can define a **Schur functor**

$$  S_R : C \to C  $$

for any finite-dimensional representation $R$ of $S_n$, as follows.  We can write $R$ as a finite direct sum of irreducible representations:

$$  R = \bigoplus_i V_{\lambda_i}  $$

and then define 

$$  S_R(-) = \bigoplus_i S_{\lambda_i}(-) \, .$$ 

## Schur functors as actions of the plethystic monoidal category ##

There's a Schur functor from a symmetric monoidal category to itself for every $\mathbb{Z}[S_n]$ module $M$, given by 
$$S_M(X)=X^{\otimes n}\otimes_{\Z[S_n]}M.$$

The composition of these functors corresponds to a strange monoidal structure on $\oplus_n\mathbb{Z}[S_n]$-mod, given by plethysm:
$$M\boxtimes N=\mathrm{Ind}_{S_n\wr S_m}^{S_{mn}} M\wr N.$$

The Schur functors described above are those corresponding to irreducible modules over $\mathbb{Q}$. 

_Todd_: To be related to composition of analytic functors a la Joyal species... We also have material on plethysm, Tall-Wraith monoid, etc. to be linked to. 

## (Tentative) High-level description of Schur functors ##

As we have just seen, Schur functors such as the $S_\lambda$ makes sense in pretty wide contexts, and the formula for the $S_\lambda$ is in some sense "polymorphic". The question arises as to the right way to give sense to such [[polymorphism]], or in other words the compatibility between these Schur functors across the various structured categories where they are defined. Here is a very general expression of that compatibility proposed by [[John Baez]]. 

The general idea is that Schur functors such as the $S_\lambda$ defined above on individual categories commute with suitable change-of-base functors between these categories. This commutation expresses a kind of naturality, for which we would like a clean and high-level description. 

The above discussion shows that Schur functors $S_\lambda$ "live on" (are definable in terms of structure in) symmetric monoidal linear categories satisfying some (possibly mild) exactness or cocompleteness condition. 

* "Linear" might mean here either enriched in $Ab$ (abelian groups) or enriched in $Vect$ (vector spaces over $\mathbb{Q}$) -- there are various possibilities. 

* The exactness condition might mean (on the strong end of the spectrum) being abelian, or (on the weak end) being Cauchy complete in the enriched sense, i.e., additive and closed under splitting of idempotents, or (somewhere in the middle) being finitely cocomplete, i.e., additive and admitting coequalizers. We require that the tensor product of the symmetric monoidal structure preserve, in each of its separate arguments, any colimits assumed to exist. 

Since the discussion is for now tentative, we'll hedge our bets and go with the vague term "linear" and tacitly understand there's also some exactness condition which will go unmentioned. 

"Change of base" will mean a functor between symmetric monoidal linear categories preserving relevant structure: a symmetric monoidal linear functor which preserves some class of finite colimits, say either all finite colimits (right exactness) or just the absolute colimits (finite coproducts and split coequalizers: any linear functor preserves those). Again, in the tentative discussion we'll leave the exactness condition tacit but unmentioned, and just say "symmetric monoidal linear functor" to cover the type of change-of-base functor we're after. 

Hence we have some 2-category $SymMonLin$ whose objects are "symmetric monoidal linear categories", whose 1-morphisms are "symmetric monoidal linear functors", and whose 2-morphisms are symmetric monoidal linear transformations. 

Now Schur functors, while they are _defined_ in terms of such structure, are not assumed to _respect_ any of this structure except of course for the bare category structure, so they live as 1-morphisms in the 2-category $Cat$. However, they should be _polymorphically defined_: defined for every object $C$ of $SymMonLin$ and invariant with respect to change of base. The right way to say it is that there is a forgetful 2-functor 

$$U: SymMonLin \to Cat$$ 

and to propose the polymorphic definition: a **Schur functor** is a strong (i.e., pseudo) natural transformation from $U$ to itself. That is, a Schur functor is a family of functors 

$$S_C: U(C) \to U(C)$$ 

which commute with symmetric monoidal linear functors $f: C \to D$ up to (coherent) natural isomorphisms $S_f$:  

$$\array{
U(C) & \overset{S_C}{\to} & U(C) \\
U(f) \downarrow & S_f \swArrow & \downarrow U(f) \\
U(D) & \underset{S_D}{\to} & U(D)
}$$ 

(Coherent in the standard sense implied by strong naturality.) Following usual procedure in 2-category theory, a **morphism** between Schur functors is a modification $\phi: S \to T$ between such strong natural transformations. 

## Discussion for module categories ##

The weakest or baseline assumption is that objects of $SymMonLin$ are symmetric monoidal additive categories in which idempotents split. In the case of modules over a commutative ring $A$, this means that minimally we have to include finitely generated projective $A$-modules. This plays a role analogous to finite-dimensional vector spaces over a field, and in fact let's emphasize the analogy by letting $Vect_A$ denote the category of finitely generated projectives over $A$. 

Here are some very easy but possibly suggestive observations: 

* A 1-object symmetric monoidal $Ab$-category is precisely a commutative ring $A$. 

* The Cauchy completion of $A$ is the symmetric monoidal $Ab$-category $Vect_A$. 

* A symmetric monoidal $Ab$-functor between commutative rings is precisely a ring homomorphism $\phi: A \to B$. 

* A symmetric monoidal $Ab$-functor $Vect_A \to Vect_B$ is monoidally isomorphic to one of the form 
$$B \otimes_A -: Vect_A \to Vect_B$$ 
for some unique $A$-algebra structure (ring homomorphism) $f: A \to B$. 

Thus, if $S$ is a (polymorphic) Schur functor, the pseudonaturality forces the presence of strength isomorphisms 

$$B \otimes_A S(M) \cong S(B \otimes_A M)$$ 

for any $A$-algebra $f: A \to B$ and for any $M$ in $Vect_A$ (and in fact for any $A$-module $M$ whatsoever). 

_To be continued..._
