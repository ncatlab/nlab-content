#Contents#
* automatic table of contents goes here
{:toc}


#Idea and definition#

Classically, a **Schur functor** is a specific sort of [[functor]] 

$$F: FinVect_{\mathbb{C}} \to FinVect_{\mathbb{C}}$$ 

on the category of finite-dimensional complex [[vector space|vector spaces]].  Namely, it is a functor of this sort that is algebraic on homsets: the homsets are vector spaces, and we demand that for any pair of objects $V, W \in FinVect_{\mathbb{C}}$ the functor

$$ F: hom(V,W) \to hom(F V , F W) $$

is a polynomial function from the vector space 
$hom(V,W)$ to the vector space $hom(F V , F W)$

In more modern treatments, a Schur functor is a functor defined (in a [[polymorphism|polymorphic]] way) on [[module|modules]] over more general [[commutative ring]] $R$ (possibly with some conditions on $R$), so that "Schur functor" really connotes a family of functors 

$$F_R: Mod_R \to Mod_R$$ 

It turns out that much of the theory of Schur functors can be generalized even further, beyond module categories.  In this article, Todd Trimble and John Baez plan to explore the scope of such generality and --- we hope --- write a paper about what we find.

# Examples #

The first thing that should be understood from the beginning is that a general Schur functor $F$ is _nonlinear_: the action on [[hom-set]]s 

$$hom(V, W) \to hom(F(V), F(W))$$ 

is not assumed to respect linear structure. In fact, linear Schur functors are rather uninteresting: because every finite-dimensional space is a finite [[biproduct]] of the $1$-dimensional space $\mathbb{C}$, and because [[linear functor]]s preserve finite biproducts, it turns out that every linear Schur functor $F$ is [[representable functor|representable]] as $hom(X, -)$ where $X = F(\mathbb{C})$. The category of linear Schur functors is equivalent to $Vect_{fd}$. 

Rather more representative examples of Schur functors include: 

* For each $k \geq 0$, the $k^{th}$ [[tensor power]] $V \mapsto V^{\otimes k}$ is a Schur functor. 

* For each $k \geq 0$, the $k^{th}$ [[symmetric power]] $V \mapsto Sym^k(V)$ is a Schur functor. 

* For each $k \geq 0$, the $k^{th}$ [[alternating power]] $V \mapsto Alt^k(V)$ is a Schur functor. 

Even though Schur functors do not respect linear structure, the category $Schur$ of Schur functors is nevertheless a [[linear category]], so we can talk about [[irreducible object]]s, decompositions into [[direct sum|direct sums]], and so on. It turns out that every Schur functor $F$ can be expressed as a direct sum of irreducible $Schur$-objects $S_\lambda$ indexed by [[Young diagram]]s $\lambda$, and these $S_\lambda$ are usually what people think of when they say "Schur functors". 

+--{.query} 
[[Todd Trimble]]: I took this statement about decompositions from the blog discussion, but what's the precise statement? I have a hard time believing that it's a finite decomposition in general. I'm hoping the situation is analogous to analytic functors in the case of species, but I'm not at all sure what the precise statement should be. 

Even if it is something analogous to analytic functors, I am reminded that analytic functors on $Set$ aren't just any old functors; they are characterized by certain properties such as weak preservation of pullbacks. Is there something similar that needs to be said for the very general sense of 'Schur functor' given above?

[[John Baez]]: I think we don't need anything more than what we're assuming above.  But let's prove that. 

[[Todd Trimble]]: Scratch the query as stated above then: I see you've edited in an algebraicity hypothesis. We share a hope that the sophisticated machinery of strong natural transformations and modifications will automatically enforce such a thing. That would be nice. 

=--

# Schur functors associated with Young diagrams #

Functors such as the $k^{th}$ alternating power, $k^{th}$ symmetric power, etc. make sense in much wider contexts than just $Vect_{\mathbb{C}}$. Indeed, let $C$ be any [[symmetric monoidal category|symmetric monoidal]] [[abelian category]] whose hom-objects are $\mathbb{Q}$-vector spaces. 

+--{.query}
[[Todd Trimble]]: 
I wimped out and chose rational vector spaces as the base of enrichment. For one thing, the blog commentary seems to suggest that there are delicate issues in nonzero characteristic. Even in cases where there is no integer torsion, it seems to me that integer divisibility makes certain things come out a lot more cleanly, and (if I am not mistaken) means that certain finite cocompleteness conditions can be relaxed in favor of Cauchy completeness (in the enriched category sense of Lawvere). More on this later. 

[[John Baez]]: You're right that there are special tricky endofunctors 
$$ F: FinVect_{k} \to FinVect_{k} $$
that can be defined only when $k$ has characteristic $p$.
So, using categories enriched over $Vect_k$ with $k$ having characteristic zero is probably a wise idea, at least for starters.  But I'm really hoping that we can drop that in the more sophisticated approach where we work with all symmetric monoidal abelian categories simultaneously and demand pseudonaturality.  I'm hoping this will 'wash out' the tricky functors that only work in characteristic $p$, leaving us with just the Schur functors we know and love.  

[[Todd Trimble]]: Could be! 

=-- 

Recall that the [[group algebra]] $\mathbb{Q}[S_n]$ decomposes as a direct sum of matrix algebras 

$$\bigoplus_{\lambda} hom(V_\lambda, V_\lambda)$$ 

where $\lambda$ is indexed over Young diagrams and $V_\lambda$ is the corresponding irreducible representation, or, just at the level of $S_n$-representations, 

$$\bigoplus_{\lambda'} V_{\lambda'}$$ 

where this time $\lambda'$ ranges over $n$-box [[Young tableaux]], and $V_\lambda'$ represents the irreducible subrepresentation attached to $\lambda$.  

This group algebra lives as a [[monoid]] in the symmetric monoidal category of finite-dimensional rational spaces $FinVect_{\mathbb{Q}}$. If $Sk$ is the skeleton of $Vect_{fd}$ consisting of the finite coproducts $\mathbb{Q}^n$, then there is an evident linear functor 

$$Sk \to C: \mathbb{Q}^n \mapsto I^n$$ 

where $I^n$ is the $n$-fold coproduct of the monoidal unit $I$ of $C$. By left Kan extension along the inclusion $Sk \hookrightarrow Vect_{fd}$, we therefore obtain a canonical [[change of base]] functor 

$$i: FinVect_{\mathbb{Q}} \to C$$ 

which is in fact [[symmetric monoidal functor|symmetric monoidal]]. This means the change of base maps the group algebra $\mathbb{Q}[S_n]$ to a monoid in $C$, again denoted $\mathbb{Q}[S_n]$ by abuse of notation, and it maps each of the irreducible representations $V_\lambda$ to a corresponding module over the monoid $\mathbb{Q}[S_n]$ in $C$, which we again denote by $V_\lambda$. 

If $X$ is an object of $C$, the symmetric group $S_n$ has a
representation on $X^{\otimes n}$.  It thus has a representation 

$$V_\lambda \otimes X^{\otimes n}$$ 

and we define $S_\lambda(X)$ to be the object of $S_n$-coinvariants of $V_{\lambda} \otimes X^{\otimes n}$:

$$S_\lambda(X) = V_{\lambda} \otimes X^{\otimes n} / S_n$$

This construction of $S_\lambda(X)$ defines the **Schur functor** $S_\lambda$ on $C$. 

+--{.query} 
With the possible exception of the left Kan extension alluded to above, all these constructions may be carried out if we weaken the abelian assumption on $C$ to mere Cauchy completeness (relative to enrichment in rational vector spaces), which more concretely means that $C$ admits finite coproducts and splittings of idempotent projections. This observation was made by Noah Snyder on the blog.

(Jamie: Doesn't Cauchy completeness for abelian categories in fact correspond to _biproducts_ and split idempotents?)

Todd: Coproducts _are_ biproducts in the $Ab$-enriched case! That is, I was assuming as given that $C$ was enriched in something like $Ab$ or $Vect$. 

It would actually feel more natural to me to speak of the object of coinvariants rather than the object of invariants, but in the present context it should come to the same thing as either is the splitting of the idempotent operator $\frac1{n!}\sum g$. That is to say: there is a natural splitting of the idempotent natural transformation 
$$e_X = \frac1{n!} \sum_{g \in S_n} g: V_\lambda \otimes X^{\otimes n} \to V_\lambda \otimes X^{\otimes n}$$ 
which can be viewed either as invariants (equalizer of $e$ and the identity) or coinvariants (coequalizer of $e$ and the identity). 

[[John Baez]]: we need to use coinvariants when we get to  the more sophisticated approach where our constructions are supposed to preserved by <i>right exact</i> functors.  Also, coinvariants work even in characteristic $p$, while invariants involve dividing by $n!$.  So, coinvariants rule, and I've switched to working with them above.  Also, following Jamie Vicary's correction, I've switched to using Young tableaux instead of Young diagrams: for each Young diagram there are many isomorphic Schur functors, one for each Young tableau of that shape. 

[[Todd Trimble]]: That's fine to switch to coinvariants; I completely agree that's the correct conceptual way to go in general. As far as Young diagrams vs. Young tableaux, point taken, but see also my response to Jamie (which I've incorporated above). 

Of course, I've already noted that "right exact" could be overkill in certain contexts. When the object of coinvariants arises by splitting an idempotent (as in the case of enrichment over rational vector spaces), we don't need full right exactness to preserve the construction, although we might want to retain additivity: preservation of direct sums. I hope we can be a bit flexible about hypotheses until we're further along in this.

[[Rod McGuire]] Isn't a switch from Young diagrams to Young tableaux essentially the same as changing from groups to groupoids?  

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

* The exactness condition might mean (on the strong end of the spectrum) being abelian, or (on the weak end) being Cauchy complete in the enriched sense, i.e., additive and closed under splitting of idempotents, or (somewhere in the middle) being finitely cocomplete, i.e., additive and admitting coequalizers. 

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
