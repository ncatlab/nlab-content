[[!redirects smooth topoi]]
[[!redirects smooth toposes]]

<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>

#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

A __smooth topos__ or __smooth [[lined topos]]__ is 
the kind of [[topos]] studied in [[synthetic differential geometry]], a [[category]] of [[generalized smooth spaces]] for which a notion of [[infinitesimal space]] exists.

It is defined to be a [[category]] of objects that behave like [[spaces]], one of which --- the _line_ object $R$ --- is equipped with the structure of a commutative [[algebra]], such that for [[infinitesimal object]]s $S \subset R^n$ all morphisms $S \to R$ are _linear_  --- i.e. such that the [[Kock-Lawvere axiom]] holds.

# Definition #

There is a standard definition  and various straightforward variations.

## standard defnition ##


+-- {: .un_defn }
###### Definition

For $(\mathcal{T},R)$ a [[lined topos]] there is the obvious notion of $R$-algebra objects $A$
in $T$.  

For $A$ and $B$ any two $R$-algebra objects, there is the [[subobject]] $R Alg_T(A,B) \subset B^A$ of morphisms $A \to B$ that are algebra homomorphisms.

Write

$$
  Spec(A) := R Alg_{\mathcal{T}}(A,R) 
$$

for the algebra spectrum of $A$ in $\mathcal{T}$.

An **$R$-[[infinitesimal object|Weil algebra]]** $W$ is an $R$-algebra of the form $W = R \oplus J$, 
where $J$ is an $R$-finite-dimensional nilpotent ideal.

=--


+-- {: .un_defn }
###### Definition
**(smooth topos)**

A [[lined topos]] $(\mathcal{T},R)$ is a **smooth topos** if 

* the algebra spectra $Spec(W)$ of all [[infinitesimal object|Weil algebras]] $W$
  in $\mathcal{T}$  are [[infinitesimal object]]s in that
  the functor $(-)^{Spec W} : \mathcal{T} \to \maathcal{T}$ has a [[right adjoint]] (the "[[amazing right adjoint]]");

* it satisfies the [[Kock-Lawvere axiom]] in that for all $R$-Weil algebra objects $W$ the canonical morphism

  $$
    W \to R^{Spec(W)}
  $$

  is an [[isomorphism]] in $\mathcal{T}$.

=--




# Examples #

## well-adapted models ##

A smooth topos $(\mathcal{T},R)$ is called a **well adapated model** if there is a [[full and faithful functor]] 

$$ 
  Diff \hookrightarrow \mathcal{T}
$$

from the [[category]] [[Diff]] of smooth [[manifold]]s into it, that takes the real line $\mathbb{R}$ to the [[lined topos|line object]] $R$.

In these _well adapted models_ ordinary [[differential geometry]] is therefore faithfully embedded. 

For a list of examples of well adopted models see

* [[Models for Smooth Infinitesimal Analysis]].

Notice that by far not all models are of this form, as the following examples show. On the contrary, the axioms of [[synthetic differential geometry]] may be regarded as providing a unified framework in particular for [[differential geometry]] of [[manifold]]s and [[algebraic geometry]] of [[algebraic space]]s, [[scheme]]s and other objects.

## models for supergeometry ##

It is straightforward to slightly enhance the axioms of smooth toposes such as to incorporate the step from [[differential geometry]] to [[supergeometry]], one just requires that algebra structure on the [[lined topos|line object]] $R$ is further refined to thatr of a [[superalgebra]]. The result is called a [[super smooth topos]]. See there for a list of models of these.

## models for algebraic geometry ##

A simple model of a [[smooth topos]] that may be regarded as a context inside which much of [[algebraic geometry]] takes place is the following:

Let $k$ be a [[field]] and let $ (k-Alg^{finp})^{op}$ be the [[opposite category]] of the [[category]] of finitely presented $k$-[[algebra]]s. Then the [[presheaf]] category $\mathcal{T} = PSh((k-Alg^{finp})^{op})$ equipped with the [[lined topos|line object]] $R = k[T]$ (the algebra of polynomials over $k$ in one variable $T$) 

$$
  (
    \mathcal{T} = PSh((k-Alg^{finp})^{op}), 
    R = k[T]
  )
$$

is a smooth topos. This is described in section 9.3 of

* [[Anders Kock]], _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

Notice that despite the name of that book, this model is _not_ a well adapted model in that ordinary smooth [[manifold]]s do not embed full and faithfully into this topos. 

Instead, interpreting the internal notion of manifold described in that book -- called _formal manifolds_ in the model $\mathcal{T} = PSh((k-Alg^{finp})^{op})$ produces something like [[formal scheme]]s over $k$. 

Indeed, much of [[algebraic geometry]] over $k$ may be thought of as being concerned with this model for a smooth topos. A main difference is that in [[algebraic geometry]] attention is usually focused on particularly well behaved objects inside $\mathcal{T} = PSh((k-Alg^{finp})^{op})$: those that satisfy a [[sheaf]] condition with respect to a [[Grothendieck topology]] on $(k-Alg^{finp})^{op}$ and among those moreover those that are _locally isomorphic_ to a [[representable functor|representable]]: these are the [[scheme]]s or [[algebraic space]]s over $k$.

Probably the [[category of sheaves]] [[localization]] of $PSh((k-Alg^{finp})^{op})$ with respect to one of the standard topologies (Zariski or etale) is still a [[smooth topos]], so that this conmdition can be enforced by passing to a more restrictive model.

But since [[scheme]]s alone will never form a [[topos]], and smooth topos axiomatization of [[algebraic geometry]] will always contain more general -- also more "pathological" -- objects than [[scheme]]s. It's an example of an old dictum by [[Grothendieck]] that it is useful to have a nicely behaved category that contains pathological objects than a badly-bahved category of only nice objects: the [[topos]]-[[category theory|general nonsense]] allows useful general constructions in $\mathcal{T}$ which may in each individual case be checked for whether they land in the sub-category of [[schemes]] or [[algebraic space]]s or not.

A similar comment of course applies to the "well-adapted models" mentioned above: into these ordinary [[manifold]]s only embed, they contain "smooth space"s much more general than manifolds (such as [[diffeological space]]s) but also possibly "pathological" ones, from some perspective or other.

See also

* [[synthetic differential geometry applied to algebraic geometry]].

## warning on preservation of (co)limits ##

Most of the examples above provided [[topos]]es into which a [[category]] $NiceSpaces$ of nicely behaved [[space]]s, such as [[manifold]]s or [[scheme]]s embeds [[full and faithful functor|full and faithfully]].

$$
  NiceSpaces \hookrightarrow \mathcal{T}
  \,.
$$

But the inclusion functor will in general not preserve all [[limit]]s and [[colimit]]s that exist in $NiceSpaces$.

For instance for the well-adopted models the full and faithful inclusion of [[Diff]] typically respects only [[pullback]]s of [[manifold]]s along [[transversal map]]. This is because this is the case for the inclusion $Diff \hookrightarrow \mathbb{L}$ of [[Diff]] into the category of [[smooth locus|smooth loci]] and the [[Grothendieck topology]] for these models is typically [[subcanonical coverage|subcanonical]]. See the discussion at [[smooth locus]] for more on this.

This means that universal constructions in a smooth topos may yield different results than in a smaller category of more nicely behaved spaces. However, it is noteworthy that in the above example of manifolds, one may argue that the ordinary [[pullback]] of manifolds along non-[[transversal map]]s is the _wrong_ pullback in any case: it doesn't behave well with the [[cohomology]] of manifolds. One motivation for derived geometry, in the case of manifolds specifically the motivation for considering [[derived smooth manifold]]s, is to pass from objects in a [[topos]] instead more generally to objects in an [[(∞,1)-topos]] of [[derived stack|stack]] [[∞-stack]]s.

+--{.query}
Zoran: In derived geometry we want to go to derived infinity-stacks, not just infinity stacks. The embedding into infinity stacks is commuting with pullbacks, but not the one into derived infinity stacks. At least in algebraic world, and if I understand what Spivak has for spectra it is the same story.
=--