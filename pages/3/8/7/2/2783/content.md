* toc
{: toc}

# Idea

The forgetful 2-functors 

* from [[regular categories]] to [[lex categories]],
* from [[exact categories]] to [[lex categories]], and
* from [[exact categories]] to [[regular categories]]

have left adjoints, and in fact are [[monadic adjunction|(2-)monadic]].  Their left adjoints are called (free) regular or exact completions.

In the third case the monad is [[idempotent monad|idempotent]], so the left adjoint can properly be called a [[completion]], while in the first two cases, the monad is only [[lax-idempotent monad|lax-idempotent]], so the left adjoint should technically be called a [[free completion]].  However, the phrases *regular completion* and *exact completion* are also commonly used for the first two cases.  To disambiguate the second and third cases the phrases *ex/lex completion* and *ex/reg completion* are also used, and so by analogy the first case is called *reg/lex completion*.

In fact, the reg/lex and ex/lex completion can be applied to a category that merely has [[weak finite limits]], although in this case the sense in which the construction is "free" is more complicated.


# Constructions

## The ex/lex completion

There are several constructions of the ex/lex completion.  Perhaps the quickest one to state (Hu-Tholen 1996) is that if $C$ is [[small category|small]], then $C_{ex/lex}$ is the full subcategory of its [[presheaf category]] $Set^{C^{op}}$ spanned by those presheaves $F$ such that

* $F$ admits a [[regular epimorphism]] $y(X)\twoheadrightarrow F$ from a [[representable presheaf]], 
* with the additional property that if $K\rightrightarrows y(X)$ is the [[kernel pair]] of $y(X)\twoheadrightarrow F$, then $K$ also admits a regular epi $y(Z)\to K$ from a representable presheaf.

A more explicit construction is as follows.  Let us think, informally, of the objects of $C$ as [[presets]] and the morphisms of $C$ as "proofs".  An object of $C_{ex} = C_{ex/lex}$ will then be a "set" or [[setoid]] constructed from $C$.  Precisely, we take the objects of $C_{ex}$ to be the **pseudo-equivalence relations** in $C$: a pseudo-equivalence relation consists of:

* an object $X\in C$ and
* a parallel pair $s,t\colon R\rightrightarrows X$, such that
* there exists an arrow $i\colon X\to R$ with $s i = t i = 1_X$,
* there exists an arrow $v\colon R\to R$ with $s v = t$ and $t v = s$, and
* there exists an arrow $c\colon R\times_X R \to R$ with $s c = s \pi_1$ and $t c = t \pi_2$.  (If $C$ has merely weak finite limits, we assert this for some, and hence every, weak pullback $R\times^w_X R$.)

If $(s,t)\colon R\to X\times X$ is a [[monomorphism]], then these conditions make it precisely a [[congruence]] or internal [[equivalence relation]] in $C$.  In general, we can think of the fiber of $R$ over $(x_1,x_2)$ as giving a collection of "reasons" or "proofs" that $x_1 \mathrel{R} x_2$.  Then $i$ supplies a uniform proof that $x \mathrel{R} x$ for every $x$, while $v$ supplies a uniform proof that $x \mathrel{R} y$ implies $y \mathrel{R} x$, and $c$ supplies a uniform proof thath $x \mathrel{R} y$ and $y \mathrel{R} z$ imply $x \mathrel{R} z$.

If $R\rightrightarrows X$ and $S\rightrightarrows Y$ are two pseudo-equivalence relations, a morphism between them in $C_{ex}$ is defined to be a morphism $f\colon X\to Y$ in $C$, such that there exists a morphism $f_1\colon R\to S$ with $s f_1 = f s$ and $t f_1 = f t$.  That is, $f_1$ supplies a uniform proof that if $x \mathrel{R} y$ then $f(x) \mathrel{S} f(y)$.  Moreover, we declare two such morphisms $f,g\colon X\to Y$ to be *equal* if there exists a morphism $h\colon X\to S$ such that $s h = f$ and $t h = g$ (that is, a uniform proof that $f(x) \mathrel{S} g(x)$).  Because $S\rightrightarrows Y$ is a pseudo-equivalence relation, this defines an actual equivalence relation on the morphisms $f\colon X\to Y$, which is compatible with composition; thus we have a well-defined category $C_{ex}$.

We have a [[full and faithful functor]] $C\to C_{ex}$ sending an object $X$ to the pseudo-equivalence relation $X\rightrightarrows X$.  One can then verify directly that $C_{ex}$ is exact, that this embedding preserves finite limits, and that it is universal with respect to lex functors from $C$ into exact categories.

There are also other constructions.  Of course, the ex/lex completion can also be obtained by composing (any construction of) the reg/lex completion with (any construction of) the ex/reg completion.


## The reg/lex completion

The reg/lex completion $C_{reg}= C_{reg/lex}$ is perhaps most succinctly described as the subcategory of $C_{ex}$ consisting of those objects which admit monomorphisms into objects of $C$.  (If $C$ only has weak finite products, we have instead to consider the objects admitting a jointly-monic finite family of morphism into objects of $C$.)  That is, instead of adding *all* quotients of pseudo-equivalence relations in $C$, we only add those quotients which are necessary in order to be able to construct [[images]] of morphisms in $C$.  For many construction of $C_{ex}$, this idea can then be made more explicit and sometimes simplified.

For instance, if we regard $C_{ex}$ as a full subcategory of $Set^{C^{op}}$ as above, then we can likewise regard $C_{reg}$ as the full subcategory of $Set^{C^{op}}$ determined by those presheaves $F$ such that

* $F$ admits a regular epimorphism $y(X) \twoheadrightarrow F$ from a representable presheaf, and
* $F$ admits a monomorphism $F\rightarrowtail y(Z)$ into a representable presheaf (or a jointly-monic finite family of such, if $C$ is only weakly lex).

If we construct $C_{ex}$ using pseudo-equivalence relations, as above, then we can characterize the pseudo-equivalence relations which we need to form $C_{reg}$ as precisely the (weak) [[kernel pairs]] of morphisms of $C$ (or finite families of such).  Therefore, we obtain an equivalent definition of $C_{reg}$ as follows.  Its objects are morphisms of $C$ (regarded as stand-ins for their formally added images, or for their weak kernel pairs).  A morphism from $p\colon X\to Y$ to $q\colon Z\to W$ should be a morphism $f\colon X\to Z$ for which there exists an $f_1$ relating the weak kernel of $p$ to the weak kernel of $q$, modulo an equivalence relation generated by maps from $X$ to the weak kernel of $q$.  But by definition of kernel pairs, two morphisms will be identified under this latter equivalence relation if and only if they have the same composite with $q$, so it makes sense to define the morphisms of $C_{reg}$ from $p\colon X\to Y$ to $q\colon Z\to W$ to be certain morphisms $\overline{f}\colon X\to W$ which factor through $q$ (non-uniquely).  We still have to impose the condition that $f$ should preserve the kernel pairs, but in terms of $\overline{f}$ this is simply the statement that $\overline{f} r = \overline{f} s$, where 
$(r,s)$ is the (weak) kernel pair of $p$.  This is the definition of $C_{reg}$ given in the [[Elephant]].  (If $C$ has merely weak finite limits, instead of single morphisms as the objects of $C_{reg}$ we must consider finite families of such.)

We can then verify that $C_{reg}$ is regular, that we have a full and faithful functor $C\to C_{reg}$, which preserves finite limits, and is universal among lex functors from $C$ to regular categories.

Again, there are also other constructions.


## The ex/reg completion

If $C$ is regular, a quick definition of $C_{ex/reg}$ is as the full subcategory of the category $Sh(C)$ of [[sheaves]] for the [[regular coverage]] on $C$ spanned by those sheaves which are quotients of [[congruences]] in $C$.  (Lack 1999)

A more explicit description can be obtained by first passing from $C$ to its [[allegory]] of internal relations, then [[split idempotent|splitting]] the idempotents which are equivalence relations in $C$, and finally reconstructing a regular category from the resulting allegory.  Yet more explicitly, this means that the objects of $C$ are congruences in $C$, and the morphisms are relations which are [[entire relation|entire]] and [[functional relation|functional]] relative to the given congruences.

Another way of phrasing this is that $C_{ex/reg}$ is the category of internal [[0-categories]] in $C$ and [[anafunctors]] between them.


# Properties of completions

(to be written...)


# Preservation of additional structure

(to be written...)


# Examples

(to be written...)


# References

* Carboni and Celia Magno, "The free exact category on a left exact one", J. Austral. Math. Soc. (Ser. A), 1982.

* Hu and Tholen, "A note on free regular and exact completions and their infinitary generalizations", [TAC](http://www.tac.mta.ca/tac/volumes/1996/n10/2-10abs.html) 1996.

* Carboni and Vitale, "Regular and exact completions", JPAA 1998.

* Stephen Lack, "A note on the exact completion of a regular
 category, and its infinitary generalizations" [TAC](http://www.tac.mta.ca/tac/volumes/1999/n3/5-03abs.html) 1999.

* The [[Elephant]], Sections A1.3 and A3.


[[!redirects regular or exact completion]]
[[!redirects regular and exact completion]]
[[!redirects exact completion]]
[[!redirects ex/lex completion]]
[[!redirects ex/reg completion]]
[[!redirects reg/lex completion]]
[[!redirects regular or exact completions]]
[[!redirects regular and exact completions]]
[[!redirects exact completions]]
[[!redirects ex/lex completions]]
[[!redirects ex/reg completions]]
[[!redirects reg/lex completions]]
