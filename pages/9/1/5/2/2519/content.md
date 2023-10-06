
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

A __smooth topos__ or __smooth [[lined topos]]__ is 
the kind of [[topos]] studied in [[synthetic differential geometry]], a [[category]] of [[generalized smooth spaces]] for which a notion of [[infinitesimal space]] exists.

It is defined to be a [[category]] of objects that behave like [[spaces]], one of which --- the _line_ object $R$ --- is equipped with the structure of a commutative [[algebra]], such that for [[infinitesimal object | infinitesimal objects]] $S \subset R^n$ all morphisms $S \to R$ are _linear_  --- i.e. such that the [[Kock-Lawvere axiom]] holds.

# Definition #

There is a standard definition and various straightforward variations.

## Standard definition ##

For $(\mathcal{T},R)$ a [[lined topos]] there is the notion of an $R$-algebra object in $\mathcal{T}$. For $A$ and $B$ any two $R$-algebra objects, let $R Alg_\mathcal{T}(A,B)$ denote the [[subobject]] of $B^A$ consisting of morphisms $A \to B$ which are algebra homomorphisms. Let $Spec(A)$ denote the algebra spectrum $R Alg_\mathcal{T}(A,R)$ of $A$ in $\mathcal{T}$.

+-- {: .num_defn }
###### Definition
An **$R$-[[infinitesimal object|Weil algebra]]** $W$ is an $R$-algebra of the form $W = R \oplus J$, 
where $J$ is an $R$-finite-dimensional nilpotent ideal.

=--


+-- {: .num_defn }
###### Definition
A [[lined topos]] $(\mathcal{T},R)$ is a **smooth topos** if, for each $R$-[[infinitesimal object|Weil algebras]] $W$, the functor $(-)^{Spec W} : \mathcal{T} \to \mathcal{T}$ has a [[right adjoint]] and the canonical morphism

  $$
    W \to R^{Spec(W)}
  $$

  is an [[isomorphism]] in $\mathcal{T}$. 
=--

That is to say, each $R$-Weil algebra in a lined topos is [[infinitesimal object|infinitesimal]] and satisfies the [[Kock-Lawvere axiom]]. The right adjoint of $(-)^{Spec W}$ is known as the "[[amazing right adjoint]]". 

# Examples #

## Well-adapted models ##

A smooth topos $(\mathcal{T},R)$ is called a **well adapted model** if there is a [[full and faithful functor]] 

$$ 
  Diff \hookrightarrow \mathcal{T}
$$

from the [[category]] [[Diff]] of [[smooth manifold | smooth manifolds]] into it, that takes the real line $\mathbb{R}$ to the [[lined topos|line object]] $R$.

In these _well adapted models_ ordinary [[differential geometry]] is therefore faithfully embedded. 

For a list of examples of well adapted models see

* [[Models for Smooth Infinitesimal Analysis]].

Notice that by far not all models are of this form, as the following examples show. On the contrary, the axioms of [[synthetic differential geometry]] may be regarded as providing a unified framework in particular for [[differential geometry]] of [[manifold | manifolds]] and [[algebraic geometry]] of [[algebraic space | algebraic spaces]], [[scheme | schemes]] and other objects.

## Models for supergeometry ##

It is straightforward to slightly enhance the axioms of smooth toposes such as to incorporate the step from [[differential geometry]] to [[supergeometry]], one just requires that algebra structure on the [[lined topos|line object]] $R$ is further refined to that of a [[superalgebra]]. The result is called a [[super smooth topos]]. See there for a list of models of these.

## Models for algebraic geometry ##

A simple model of a [[smooth topos]] that may be regarded as a context inside which much of [[algebraic geometry]] takes place is the following:

Let $k$ be a [[field]] and let $ (k-Alg^{finp})^{op}$ be the [[opposite category]] of the [[category]] of finitely presented $k$-[[algebra | algebras]]. Then the [[presheaf]] category $\mathcal{T} = PSh((k-Alg^{finp})^{op})$ equipped with the [[lined topos|line object]] $R = k[T]$ (the algebra of polynomials over $k$ in one variable $T$) 

$$
  (
    \mathcal{T} = PSh((k-Alg^{finp})^{op}), 
    R = k[T]
  )
$$

is a smooth topos. This is described in section 9.3 of

* [[Anders Kock]], _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

Notice that despite the name of that book, this model is _not_ a well adapted model in that ordinary [[smooth manifold | smooth manifolds]] do not embed full and faithfully into this topos. 

Instead, interpreting the internal notion of manifold described in that book -- called _formal manifolds_ in the model $\mathcal{T} = PSh((k-Alg^{finp})^{op})$ produces something like [[formal scheme | formal schemes]] over $k$. 

Indeed, much of [[algebraic geometry]] over $k$ may be thought of as being concerned with this model for a smooth topos. A main difference is that in [[algebraic geometry]] attention is usually focused on particularly well behaved objects inside $\mathcal{T} = PSh((k-Alg^{finp})^{op})$: those that satisfy a [[sheaf]] condition with respect to a [[Grothendieck topology]] on $(k-Alg^{finp})^{op}$ and among those moreover those that are _locally isomorphic_ to a [[representable functor|representable]]: these are the [[scheme | schemes]] or [[algebraic space | algebraic spaces]] over $k$.

Probably the [[category of sheaves]] [[localization]] of $PSh((k-Alg^{finp})^{op})$ with respect to one of the standard topologies (Zariski or etale) is still a [[smooth topos]], so that this condition can be enforced by passing to a more restrictive model.

But since [[scheme | schemes]] alone will never form a [[topos]], and smooth topos axiomatization of [[algebraic geometry]] will always contain more general -- also more "pathological" -- objects than [[scheme | schemes]]. It's an example of an old dictum by [[Grothendieck]] that it is more useful to have a nicely behaved category that contains pathological objects than a badly-behaved category of only nice objects: the [[topos]]-[[category theory|general nonsense]] allows useful general constructions in $\mathcal{T}$ which may in each individual case be checked for whether they land in the sub-category of [[schemes]] or [[algebraic space | algebraic spaces]] or not.

A similar comment of course applies to the "well-adapted models" mentioned above: into these ordinary [[manifold | manifolds]] only embed, they contain "smooth space"s much more general than manifolds (such as [[diffeological space | diffeological spaces]]) but also possibly "pathological" ones, from some perspective or other.

See also

* [[synthetic differential geometry applied to algebraic geometry]].

## Warning on preservation of (co)limits ##

Most of the examples above provided [[topos | toposes]] into which a [[category]] $NiceSpaces$ of nicely behaved [[space | spaces]], such as [[manifold | manifolds]] or [[scheme | schemes]] embeds [[full and faithful functor|full and faithfully]].

$$
  NiceSpaces \hookrightarrow \mathcal{T}
  \,.
$$

But the inclusion functor will in general not preserve all [[limit | limits]] and [[colimit | colimits]] that exist in $NiceSpaces$.

For instance for the well-adopted models the full and faithful inclusion of [[Diff]] typically respects only [[pullback | pullbacks]] of [[manifold | manifolds]] along [[transversal map]]. This is because this is the case for the inclusion $Diff \hookrightarrow \mathbb{L}$ of [[Diff]] into the category of [[smooth locus|smooth loci]] and the [[Grothendieck topology]] for these models is typically [[subcanonical coverage|subcanonical]]. See the discussion at [[smooth locus]] for more on this.

This means that universal constructions in a smooth topos may yield different results than in a smaller category of more nicely behaved spaces. However, it is noteworthy that in the above example of manifolds, one may argue that the ordinary [[pullback]] of manifolds along non-[[transversal map | transversal maps]] is the _wrong_ pullback in any case: it doesn't behave well with the [[cohomology]] of manifolds. One motivation for derived geometry, in the case of manifolds specifically the motivation for considering [[derived smooth manifold | derived smooth manifolds]], is to pass from objects in a [[topos]] instead more generally to objects in an [[(∞,1)-topos]] of [[derived stack|stack]] [[∞-stack | ∞-stacks]].

[[!redirects smooth topoi]]
[[!redirects smooth toposes]]
