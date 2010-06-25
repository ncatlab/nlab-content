#Contents#
* automatic table of contents goes here
{:toc}


#Idea and definition#

Classically, a **Schur functor** is a specific sort of [[functor]] 

$$F: FinVect_{\mathbb{C}} \to FinVect_{\mathbb{C}}$$ 

on the category of finite-dimensional complex [[vector space|vector spaces]].  Namely, it is a functor of this sort that is algebraic on homsets: the homsets are vector spaces, and we demand that for any pair of objects $V, W \in FinVect_{\mathbb{C}}$ the functor

$$ F: hom(V,W) \to hom(F(V) , F(W)) $$

is a polynomial function from the vector space 
$hom(V,W)$ to the vector space $hom(F(V), F(W))$

In more modern treatments, a Schur functor is a functor defined (in a [[polymorphism|polymorphic]] way) on [[module|modules]] over more general [[commutative ring]] $R$ (possibly with some conditions on $R$), so that "Schur functor" really connotes a family of functors 

$$F_R: Mod_R \to Mod_R$$ 

It turns out that much of the theory of Schur functors can be generalized even further, beyond module categories.  In this article, Todd Trimble and John Baez plan to explore the scope of such generality and --- we hope --- write a paper about what we find.

# Examples #

The first thing that should be understood from the beginning is that a general Schur functor $F$ is _nonlinear_: the action on [[hom-set|hom-sets]] 

$$hom(V, W) \to hom(F(V), F(W))$$ 

is not assumed to respect the linear structure. In fact, linear Schur functors are rather uninteresting: because every finite-dimensional space is a finite [[direct sum]] of copies of the $1$-dimensional space $\mathbb{C}$, and because [[linear functor|linear functors]] preserve finite direct sums (that is, [[biproduct|biproducts]], it turns out that every linear Schur functor $F$ is [[representable functor|representable]] as $hom(X, -)$ where $X = F(\mathbb{C})$.  So, the category of linear Schur functors is equivalent to $FinVect_{\mathbb{C}}$. 

More representative examples of Schur functors include: 

* For each $k \geq 0$, the $k^{th}$ [[tensor power]] $V \mapsto V^{\otimes k}$ is a Schur functor. 

* For each $k \geq 0$, the $k^{th}$ [[symmetric power]] $V \mapsto S^k(V)$ is a Schur functor. 

* For each $k \geq 0$, the $k^{th}$ [[alternating power]] $V \mapsto \Lambda^k(V)$ is a Schur functor. 

Even though Schur functors do not respect linear structure, the category $Schur$ of Schur functors is nevertheless a [[linear category]], so we can talk about [[irreducible object|irreducible objects]], decompositions into [[direct sum|direct sums]], and so on. It turns out that every Schur functor $F$ can be expressed as a direct sum of irreducible $Schur$-objects $S_\lambda$ indexed by [[Young diagram]]s $\lambda$, and these $S_\lambda$ are usually what people think of when they say "Schur functors". 

+--{.query} 

We need to lead up to a proof that the above conceptual definition of Schur functor is actually _correct_, i.e., that it matches the usual definition given below. 

=--
# Schur functors associated with Young diagrams #

Functors such as the $k^{th}$ alternating power, $k^{th}$ symmetric power, etc. make sense in much wider contexts than just $FinVect_{\mathbb{C}}$.   They also make sense on categories of group representations, chain complexes, group representations, coherent sheaves of vector spaces, and so on.  

To understand them more generally, let $C$ be any [[symmetric monoidal category|symmetric monoidal]] [[Cauchy complete]] category enriched over $FinVect_k$, where $k$ is any field of characteristic zero.   (In the present context, Cauchy completeness means that $C$ has [[biproducts]], also known as [[direct sums]], and also that [[idempotent|idempotents]] [[splitting|split]].)

Recall that the [[group algebra]] $k[S_n]$ decomposes as a direct sum of matrix algebras 

$$\bigoplus_{\lambda} hom(V_\lambda, V_\lambda)$$ 

where $\lambda$ ranges over isomorphism classes of irreducible representations of $S_n$, and $V_\lambda$ is any representation chosen from its isomorphism class. In more concrete terms, these representations $V_\lambda$ are labelled by $n$-box [[Young diagram|Young diagrams]].   At the level of $S_n$-representations, we have

$$k[S_n] \cong \bigoplus_{\nu} V_{\nu}$$ 

where this time $\nu$ ranges over $n$-box [[Young tableau]]x, and $V_\nu$ represents the irreducible subrepresentation of $k[S_n]$ attached to $\nu$.  

This group algebra lives as a [[monoid]] in the symmetric monoidal category $FinVect_k$. We would like it to also live in $C$.  

To achieve, this let $Sk$ be the [[skeleton]] of $FinVect_k$ consisting of the vector spaces $k^n$ and all linear maps between these.   There is an evident linear functor

$$ Sk \to C $$

sending $k^n$ to $I^n$, where $I$ is the tensor unit in $C$.  Since $Sk$ is equivalent as a linear category to $Vect_k$, we therefore obtain a linear functor 

$$i: FinVect_k \to C$$ 

which is in fact [[symmetric monoidal functor|symmetric monoidal]].  

+--{.query} 

Is $i$ the unique symmetric monoidal linear functor from $FinVect_k$ to $C$, up to symmetric monoidal natural transformation?

=--

This functor $i$ therefore maps the group algebra $k[S_n]$ to a monoid in $C$, which we again call $k[S_n]$ by abuse of notation.  It also maps each of the irreducible representations $V_\lambda$ to a corresponding module over the monoid $k[S_n]$ in $C$, which we again denote by $V_\lambda$. 

If $X$ is an object of $C$, the symmetric group $S_n$ has a representation on $X^{\otimes n}$.  It thus has a representation 

$$V_\nu \otimes X^{\otimes n}$$ 

and we define $S_\nu(X)$ to be the object of $S_n$-coinvariants of $V_{\nu} \otimes X^{\otimes n}$, by which we mean:

$$S_\nu(X) = V_{\nu} \otimes X^{\otimes n} / S_n$$

We can construct this by splitting idempotents: namely, $V_{\nu}$ is the cokernel of an idempotent in $k[S_n]$, so $S_\nu(X)$ may be defined as the cokernel of the corresponding idempotent in $k[S_n] \otimes X^{\otimes n}$.

This construction of $S_\nu(X)$ defines the **Schur functor** $S_\nu$ on $C$.   

As we have constructed them, there is one such functor for each Young tableau.  However, different Young tableaux with the same underlying Young diagram give isomorphic representations of $S_n$ and thus naturally isomorphic Schur functors.  So, it is more typical to say there is one Schur functor $S_\lambda$ for each Young diagram $\lambda$.

More generally we can define a Schur functor 

$$    S_R : C \to C $$

for any finite-dimensional representation $R$ of $S_n$, as follows.  We can write $R$ as a finite direct sum of irreducible representations:

$$  R = \bigoplus_i V_{\lambda_i}  $$

and then define, for any object $x \in C$, 

$$  S_R(x) = \bigoplus_i S_{\lambda_i}(x) \, .$$

Using Schur's lemma, one can check that this construction extends uniquely to a functor (?).

=-- 

# Schur functors as actions of the plethystic monoidal category

There's a Schur functor from a symmetric monoidal category to itself for every $\mathbb{Z}[S_n]$ module $M$, given by 
$$S_M(X)=X^{\otimes n}\otimes_{\Z[S_n]}M.$$

The composition of these functors corresponds to a strange monoidal structure on $\oplus_n\mathbb{Z}[S_n]$-mod, given by plethysm:
$$M\boxtimes N=\mathrm{Ind}_{S_n\wr S_m}^{S_{mn}} M\wr N.$$

The Schur functors described above are those corresponding to irreducible modules over $\mathbb{Q}$. 

_Todd_: To be related to composition of analytic functors a la Joyal species... We also have material on plethysm, Tall-Wraith monoid, etc. to be linked to. 

# (Tentative) High-level description of Schur functors #

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

## Discussion for module categories 

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
