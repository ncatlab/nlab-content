#Contents#
* automatic table of contents goes here
{:toc}


## Idea and definition ##

Classically, a **Schur functor** is a specific sort of [[functor]] 

$$F: FinVect_{\mathbb{C}} \to FinVect_{\mathbb{C}}$$ 

on the category of finite-dimensional complex [[vector space|vector spaces]].  Namely, it is a functor where $F(V)$ is obtained by taking a [[tensor power]] of $V$, say $V^{\otimes n}$, and then picking out the subspace that transforms according to a particular [[irreducible representation]] of the [[symmetric group]] $S_n$, which acts on $V^{\otimes n}$ by permuting the tensor factors.  

The irreducible representations of $S_n$ correspond to $n$-box [[Young diagram|Young diagrams]], so a Schur functor of this sort is named by a Young diagram. This is the beginning of a long and fascinating story connecting Schur functors with other objects that are named by Young diagrams: for example, elementary [[symmetric function|symmetric functions]] and [[cohomology]] classes on BGL, the classifying space for [[vector bundles]].  

More generally, any finite direct sum of the Schur functors described above may be called a Schur functor.  This gives a category of Schur functors and natural transformations between them.  Since the coproduct of all the symmetric groups $S_n$ is equivalent to the groupoid of finite sets and bijections, say $\mathbb{P}$, it is not surprising that this category of Schur functors is equivalent to the functor category

$$  [\mathbb{P}, FinVect_{\mathbb{C}}] \, , $$

This category could be called the 'category of finite-dimensional complex representations of the groupoid of finite sets', or the 'category of finite-dimensional linear [[species]]'.  

The category of representations of any groupoid has many nice features: for example, it is a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]], meaning roughly that it has a well-behaved tensor product, direct sums, kernels, and cokernels.   So, the category of Schur functors

$$  [\mathbb{P}, FinVect_{\mathbb{C}}] \, , $$

is of this sort.  But, it is also [[semisimple abelian category|semisimple]]: indeed, every Schur functor is a finite direct sum of 'irreducible' Schur functors, which correspond to Young diagrams.

The category of representations of a groupoid has even more nice features when the groupoid itself has a [[monoidal category|monoidal structure]]: then the representation category acquires a monoidal structure thanks to [[Day convolution]].  The groupoid $\mathbb{P}$ has, in fact, _two_ important monoidal structures, coming from the product and disjoint union of finite sets --- and since product distributes over disjoint union, $\mathbb{P}$ is a [[rig category]].  This is all reflected in the category of Schur functors.

On top of all this, it turns out that the composite of Schur functors is again a Schur functor.  In the classical literature this is called [[plethysm]].  This gives the category

$$  [\mathbb{P}, FinVect_{\mathbb{C}}] \, , $$

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

To understand them more generally, let $C$ be any [[symmetric monoidal category|symmetric monoidal]] [[Cauchy complete category|Cauchy complete]] [[category]] enriched over $Vect_k$, where $k$ is any field of characteristic zero.   (In the present context, Cauchy completeness means that $C$ has [[biproducts]], also known as [[direct sums]], and also that [[idempotent|idempotents]] [[splitting|split]].)

Recall that the [[group algebra]] $k[S_n]$ decomposes as a direct sum of matrix algebras 

$$\bigoplus_{\lambda} hom(V_\lambda, V_\lambda)$$ 

where $\lambda$ ranges over isomorphism classes of irreducible representations of $S_n$, $V_\lambda$ is any representation chosen from its isomorphism class, and the $\hom$ here is the hom of underlying vector spaces. In more concrete terms, these representations $V_\lambda$ are labelled by $n$-box [[Young diagram|Young diagrams]].   At the level of $S_n$-representations, we have

$$k[S_n] \cong \bigoplus_{\nu} V_{\nu}$$ 

where this time $\nu$ ranges over $n$-box [[Young tableau]]x, and $V_\nu$ represents the irreducible subrepresentation of $k[S_n]$ attached to $\nu$.  

This group algebra lives as a [[monoid]] in the symmetric monoidal category $FinVect_k$. We would also like to interpret it as living in $C$, by "change of base" from $FinVect_k$ to $C$. 

### Change of base ###

To achieve this change of base, let $Mat$ be the $k$-linear category whose objects are integers $m \geq 0$ and whose morphisms $m \to n$ are $m \times n$ matrices with entries in $k$. Because $C$ is Cauchy complete and in particular has finite biproducts (direct sums), there is an evident linear functor 

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

(In the case where $C$ has arbitrary coproducts, one can think of $i: FinVect_k \to C$ as a piece of the functor $Vect_k \to C$ which is left adjoint to the lax monoidal functor $\hom(I, -): C \to Vect_k$. There is some general categorical lore that such left adjoints in the 2-category of (symmetric) monoidal categories and lax symmetric monoidal functors are automatically strong monoidal, and this is a case in point.) 

The symmetric monoidal functor $i$ therefore maps the group algebra $k[S_n]$, as a [[monoid]] in the monoidal category $FinVect_k$, to a monoid in $C$, which we again call $k[S_n]$ by abuse of notation.  It also maps each of the Young tableau representations $V_\nu$, as a module over $k[S_n]$ in $FinVect_k$, to a corresponding module over the monoid $k[S_n]$ in $C$, which we again denote by $V_\nu$. 

### Modules over a bimonoid ###

Next we exploit the fact that, just like any [[group algebra]], $k[S_n]$ is a cocommutative [[bialgebra]] --- or in fancier language, a cocommutative [[bimonoid]] in the symmetric monoidal category $FinVect_k$.  Since $i : FinVect_k \to C$ is a symmetric monoidal functor, this means that $i$ carries $k[S_n]$ to a cocommutative bimonoid in $C$.  As noted above, we call bimonoid by the same name, $k[S_n]$.

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

This operator makes sense since $k$ has characteristic zero (we can divide by $n!$), and crucially, this operator is _idempotent_ (because $e = \sigma e$ for all $\sigma \in S_n$). Because we assume idempotents split in $C$, we have a (split) coequalizer 

$$V_\nu \otimes X^{\otimes n} \stackrel{\overset{e}{\to}}{\underset{1}{\to}} V_\nu \otimes X^{\otimes n} \to V_\nu \otimes_{S_n} X^{\otimes n}$$

This coequalizer is indeed the object of $S_n$-coinvariants of $V_\nu \otimes X^{\otimes n}$, i.e., the joint coequalizer of the diagram consisting of all arrows

$$V_\nu \otimes X^{\otimes n} \stackrel{\sigma \cdot-}{\to} V_\nu \otimes X^{\otimes n}$$

ranging over $\sigma \in S_n$ (it is the joint coequalizer because $e = \sigma e$ for all $\sigma$). 

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

### Schur functors are "natural" ### 

Suppose now that we have a symmetric monoidal linear functor $G: C \to D$. We can think of $G$ as a "change of base category", and Schur functors are "natural" with respect to change of base. 

That is to say: if $G$ is a symmetric monoidal $k$-linear functor $C \to D$, then by definition $G$ preserves tensor products (at least up to coherent natural isomorphism), and $G$ will automatically preserve both direct sums (by linearity) as well as splittings of idempotents (as all functors do). Therefore, for a Schur functor $S_\lambda(X) = V_\lambda \otimes_{S_n} X^{\otimes n}$, we have natural isomorphisms 

$$\array{
S_{\lambda, D} (G X) = V_{\lambda, D} \otimes_{S_n} (G X)^{\otimes n} & \cong & V_{\lambda, D} \otimes_{S_n} G(X^{\otimes n}) \\
 & \cong & G(V_{\lambda, C}) \otimes_{S_n} G(X^{\otimes n}) \\
 & \cong & G(V_{\lambda, C} \otimes_{S_n} X^{\otimes n})
}$$ 

where the first isomorphism uses the symmetric monoidal structure of $G$; the second uses the fact that $V_{\lambda, D} \cong G(V_{\lambda, C})$ because there is, up to isomorphism, only one symmetric monoidal linear functor $FinVect_k \to D$; the third uses the symmetric monoidal structure again and preservation of idempotent splittings. 

The same principle holds if $R$ is any representation, obtained as a direct sum of irreducible representations $V_\lambda$ (precisely because $G$ preserves direct sums). In summary, Schur functors $S_R$ transfer "naturally" across change of base functors $G: C \to D$. 

## Conceptual description of Schur functors ##

As we have seen, Schur functors $S_R$ are definable under fairly mild hypotheses: for fields $k$ of characteristic zero, they can be defined on any symmetric monoidal $k$-linear category $C$ satisfying the very mild cocompleteness condition of Cauchy completeness. So, for such $C$ we can define a Schur functor 

$$S_R: C \to C$$ 

and moreover, if $G: C \to D$ is a symmetric monoidal $k$-linear functor, the Schur functors on $C$ and $D$ are "naturally" compatible, in the sense that the diagram 

$$\array{
C & \stackrel{S_{R, C}}{\to} & C \\
G \downarrow & & \downarrow G \\
D & \underset{S_{R, D}}{\to} & D
}$$ 

commutes up to a canonical isomorphism $\phi_G: S_{R, D} \circ G \cong G \circ S_{R, C}$, and moreover these $\phi_G$ fit together sensibly with respect to composites of symmetric monoidal linear functors. 

In this highly abstract framework, it may be wondered what is the essential role played by the representations $R$ of the symmetric group. The natural isomorphisms $\phi_G$ which relate the Schur functors across change of base $G: C \to D$ make for a pleasant observation, but surely this is merely general nonsense of the larger story of Schur functors, which are after all deeply studied and incredibly rich classical constructions? 

Let us put the question another way. So, the Schur functors $S_R$ have a uniform (or "polymorphic") definition across all symmetric monoidal linear (Cauchy complete) categories $C$, one which is natural with respect to symmetric monoidal change of base functors $G: C \to D$. [Or again, not quite natural in a strict sense (of strict commutativity where $G S_{R, C} = S_{R, D} G$), but "_pseudonatural_" in the sense of commuting up to isomorphism $\phi_G$, with the $\phi_G$ fitting together compatibly with respect to composition of $G$'s.] Now pseudonaturality is a very general phenomenon in 2-category theory, and the question is: among all such pseudonatural transformations, what makes the Schur functors special? What extra properties pick out exactly the Schur functors from this class? 

The perhaps surprising answer is: no extra properties! That is, the Schur functors are uniquely characterized as uniformly defined functors that are (pseudo)natural with change of base! 

Let us now make this precise. Schur functors $S$ are defined on certain symmetric monoidal linear categories but respect neither the symmetric monoidal structure nor the linear structure. So, we have to forget some of the structure of the objects on which Schur functors are defined. Let 

$$U: SymMonLinCauch \to Cat$$ 

be the evident forgetful 2-functor, from the 2-category of symmetric monoidal $k$-linearly Cauchy complete categories (and symmetric monoidal linear functors, etc.) to the 2-category of categories, functors, and natural transformations. 

If $U, V: S \stackrel{\to}{\to} C$ are two 2-functors between 2-categories, we have a general notion of pseudonatural transformation: 

+-- {: .un_def} 
######Definition 
A **pseudonatural transformation** $\phi: U \to V$ is a rule that assigns to each 0-cell $s$ of $S$ a 1-cell $\phi(s): U(s) \to V(s)$ of $C$, and to each 1-cell $f: s \to t$ a 2-cell $\phi(f)$:  
$$\array{
U(s) & \stackrel{\phi(s)}{\to} & V(s) \\
U(f) \downarrow & \phi(f) \swArrow & \downarrow V(f) \\
U(t) & \underset{\phi(t)}{\to} & V(t)
}$$ 
such that the following pasting diagram equalities hold (to be filled in). 
=-- 

In 2-category theory, the correct notion of morphism between pseudonatural transformations is that of _modification_. 

+-- {: .un_def} 
######Definition 
With notation as above, let $\phi, \psi: U \to V$ be two pseudonatural transformations. A **modification** $x: \phi \to \psi$ is a rule which associates to each 0-cell $s$ of $S$ a 2-cell $x(s): \phi(s) \to \psi(t)$ of $C$, such that the following compatibility condition holds (to be filled in). 
=-- 

We now propose our conceptual definition of Schur functor. 

+-- {: .un_def} 
######Definition 
A **Schur functor** is a pseudonatural transformation $U \to U$, where 
$$U: SymMonLinCauch \to Cat$$ 
is the forgetful 2-functor. A **morphism** of Schur functors is a modification between such pseudonatural transformations. 
=-- 

What this proposed definition makes immediately clear is that _Schur functors are closed under composition_. This provides a satisfying conceptual explanation of _plethysm_, as we will explore in the next two sections. 

## Representability ##

Again, let $SymMonLinCauch_k$ is the 2-category of small symmetric monoidal _Cauchy-complete_ $k$-linear categories over a field $k$ of characteristic zero, with morphisms symmetric monoidal $k$-linear functors and 2-morphisms the symmetric monoidal $k$-linear transformations. 

+-- {: .un_thm}
######Theorem 
The underlying functor 
$$U: SymMonLinCauch_k \to Cat$$ 
is representable, in fact is represented by the Cauchy completion of the $k$-linearization of the groupoid of finite permutations $\mathbb{P}$. (If $k \mathbb{P}$ denotes the $k$-linearization, then $\widebar{k \mathbb{P}}$ denotes its Cauchy completion.) 
=-- 

+-- {: .proof} 
######Proof (Sketch)
It is well-known that $\mathbb{P}$ is the representing object for the underlying 2-functor 

$$U_0: SymMonCat \to Cat$$

Let $SymMonLin$ denote the 2-category of symmetric monoidal $k$-linear (but not necessarily linearly Cauchy complete) categories, and let $Lin$ denote the 2-category of small $k$-linear categories. Let $k(-): Cat \to Lin$ denote $k$-linearization, given by change of hom-base 

$$k \cdot - : Set \to Vect_k$$ 

applied to a small $Set$-enriched category $(C_0, hom: C_0 \times C_0 \to Set)$ to yield a $k$-linear category $(C_0, C_0 \times C_0 \to Vect_k)$. $k(-): Cat \to Lin$ is left 2-adjoint to the underlying 2-functor $u: Lin \to Cat$, and the 2-adjunction $k(-) \dashv u$ has a lifts to the level of symmetric monoidal structure, where we obtain a 2-adjunction 

$$(k(-): SymMonCat \to SymMonLin) \dashv (U_1: SymMonLin \to SymMonCat)$$ 

Finally, let $LinCauch$ denote the 2-category of $k$-linearly Cauchy-complete categories. The linear Cauchy completion gives a 2-reflector $\widebar{(-)}: Lin \to LinCat$ which is left 2-adjoint to the 2-embedding $i: LinCauch \to Lin$, and again the 2-adjunction $\widebar{(-)} \dashv i$ lifts to the level of symmetric monoidal structure to give a 2-adjunction 

$$(\widebar{(-)}: SymMonLin \to SymMonLinCauch) \dashv (U_2: SymMonLinCauch \to SymMonLin)$$ 

Putting this all together, the underlying functor $U: SymMonLinCauch \to Cat$ is the evident composite 

$$SymMonLinCauch \stackrel{U_2}{\to} SymMonLin \stackrel{U_1}{\to} SymMonCat \stackrel{U_0}{\to} Cat$$ 

and therefore we have pseudonatural equivalences 

$$\array{
SymMonLinCauch(\widebar{k(\mathbb{P})}, -) & \cong & SymMonLin(k(\mathbb{P}), U_2 -) \\
 & \cong & SymMonCat(\mathbb{P}, U_1 U_2 -) \\
 & \cong & U_0 U_1 U_2 \\
 & \cong & U
}$$ 

so that $\widebar{k \mathbb{P}}$ is the representing object. 
=--

### Structure of the representing object

Let us now calculate $\widebar{k \mathbb{P}}$. It is the linear category of all $k$-linear functors 

$$k\mathbb{P}^{op} \to Vect_k$$  

which as modules are left adjoint to modules 

$$k\mathbb{P} \to Vect_k .$$ 

But since $k\mathbb{P}$ is the coproduct of the one-object $k$-linear categories $k S_n$, this comes down to a sequence of right modules 

$$(k S_n)^{op} \to Vect_k$$ 

which are left adjoint to modules $k S_n \to Vect_k$. As is well known, these adjoint modules are the finitely generated projective right modules over $S_n$. 

Hence an object of the Cauchy completion $\widebar{k \mathbb{P}}$ is given by a sequence of finitely generated projective $S_n$-modules, one for each $n$. 

Now in characteristic zero, Maschke's theorem (all short exact sequences of $S_n$-modules split) implies that all finitely generated $S_n$-modules are projective. Thus, finitely generated projective $S_n$-modules boil down to finite-dimensional representations of $S_n$. 

Therefore an object of the Cauchy completion is a sequence of finite-dimensional $S_n$-modules, in other words a functor $\mathbb{P}^{op} \to Vect_k$ with values in spaces of finite dimension. In summary, then, we have the following result. 

+-- {: .un_thm} 
######Theorem 
The representing object $\widebar{k \mathbb{P}}$ is equivalent to the symmetric monoidal category of functors $\mathbb{P}^{op} \to FinVect_k$. 
=-- 

The linear symmetric monoidal structure is inherited from the monoidal structure of $\mathbb{P}$. Explicitly, the monoidal structure on $\mathbb{P}$ is given by group homomorphisms 

$$S_m \times S_n \to S_{m+n}$$ 

To be continued.    

## Composition of Schur functors ##

There's a Schur functor from a symmetric monoidal category to itself for every $\mathbb{Z}[S_n]$ module $M$, given by 
$$S_M(X)=X^{\otimes n}\otimes_{\Z[S_n]}M.$$

The composition of these functors corresponds to a strange monoidal structure on $\oplus_n\mathbb{Z}[S_n]$-mod, given by plethysm:
$$M\boxtimes N=\mathrm{Ind}_{S_n\wr S_m}^{S_{mn}} M\wr N.$$

The Schur functors described above are those corresponding to irreducible modules over $\mathbb{Q}$. 

_Todd_: To be related to composition of analytic functors a la Joyal species... We also have material on plethysm, Tall-Wraith monoid, etc. to be linked to. 