
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _structured $(\infty,1)$-topos_ is a generalization of the notion of a [[locally ringed space]] and locally [[ringed topos]] generalized to [[(∞,1)-topos]]es. This is a way to formalize [[higher geometry]]/[[derived geometry]]-structure on [[little topos|little]] [[(∞,1)-topos]]s.

So a structured $(\infty,1)$-topos is an [[(∞,1)-topos]] $\mathcal{X}$ equipped with an [[(∞,1)-sheaf|(∞,1)-]][[structure sheaf]] $\mathcal{O}$ that we think of as the collection of _functions_ on $\mathcal{X}$ that preserve extra geometric structure -- for instance [[topology|continuous structure]] or [[smooth structure]].

Being an $\infty$-function $\infty$-algebra, $\mathcal{O}(\mathcal{U})$ is an algebra over an [[(∞,1)-algebraic theory]] $\mathcal{G}$, called the (pre)[[geometry (for structured (∞,1)-toposes)]], since this encodes the nature of the extra geometric structure on $\mathcal{X}$.

Formally therefore a geometric structure $(\infty,1)$-sheaf of $\mathcal{X}$ is a product/limit-preserving [[(∞,1)-functor]]

$$
  \mathcal{O} : \mathcal{G} \to \mathcal{X}
  \,.
$$

Here we think of $\mathcal{X} = Sh_{(\infty,1)}(C)$ as being the [[(∞,1)-sheaf (∞,1)-topos]] on some [[(∞,1)-site]] $C$ and for any $V \in \mathcal{G}$ we think of

$$
  \mathcal{O}_V \in Sh_{(\infty,1)}(C)
$$

as being the [[(∞,1)-sheaf]] of structure-preserving functions on $C$ with values in $V$.


## Definition

Let $S$ be a [[geometry (for structured (∞,1)-toposes)|geometry]] and let $Sh(S)$ be the [[(∞,1)-topos]] of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]] on $S$. 

Notice that if $S = Op(X)$ is the nerve of the [[category of open subsets]] of some [[topological space]] $X$, then $Sh(X) \coloneqq Sh(S)$ is the [[(∞,1)-category of (∞,1)-sheaves]] on $X$, as in the above motivating introduction. 

We want to define a _structure sheaf_ on $S$ (for instance on $Op(X)$) of quantities modeled on some $(\infty,1)$-category $V$ to be an [[(∞,1)-functor]]

$$
  O_X : V \to Sh(S)
$$

to be thought of as the assignment to each _value space_ $v \in V$ of an $(\infty,1)$-sheaf  of $v$-valued functions on $S$ (on $X$ if $S = Op(X)$).

But since we are taking care of the sheaf condition on $S$, we also want to allow a similar kind of co-sheaf condition on $V$. In order to do so, $V$ is taken to be equipped with extra structure encoding covers in $V$, and $O_X$ is then required to respect this structure suitably.


### Geometries and admissibility structure

+-- {: .num_defn}
###### Definition 

An **admissiblility structure** on an $(\infty,1)$-category $V$ is 

* a choice of [[sub-quasi-category|sub (∞,1)-category]] $V^{ad} \hookrightarrow V$, whose morphisms are to be called the **admissible morphisms**, such that

  * for every admissible morphism $U \to X$ and any morphism $X' \to X$ there is a diagram

    $$  
      \array{
        U' &\to& U
        \\
        \downarrow && \downarrow
        \\
        X' &\to& X 
      }
    $$

    with $U' \to X'$ admissible;

  * for every diagram of the form 

    $$
      \array{
          && Y
          \\
          & \nearrow && \searrow
         \\
         X &&\to&& Z
      }
    $$

    with $X \to Z$ and $Y \to Z$ admissible, also $X \to Y$ is admissible.

* a [[Grothendieck topology]] on $V$ which has the property that it is generated from a [[coverage]] consisting of admissible morphisms.

=--


This is [[Structured Spaces|StrSh, def 1.2.1]] in view of remark 1.2.4 below that.



+-- {: .num_defn}
###### Definition ([StrSh, def 1.2.5](http://arxiv.org/abs/0905.0459))

An $(\infty,1)$-category $V$ equipped with an admissiblility structure is a **geometry** if it is essentially small, admits finite limits and is [[idempotent complete (infinity,1)-category|idempotent complete]].
=--

The admissible morphisms in an admissibility structure are roughly to be thought of as those morphisms that behave as _open immersions_ ,


### Structure sheaves: local $\infty$-algebras


+-- {: .num_defn}
###### Definition ([StrSh, def 1.2.8](http://arxiv.org/abs/0905.0459))
**(structure sheaf)**

Let $\mathcal{G}$ be a geometry and $\mathcal{X}$ an $(\infty,1)$-topos
An [[(∞,1)-functor]]

$$
  O_{\mathcal{X}} : \mathcal{G} \to \mathcal{X}
$$

is a $\mathcal{G}$-**structure** on $\mathcal{X}$ or 
$\mathcal{G}$-**[[structure sheaf]]** on $\mathcal{X}$ if 

* it is a left [[exact (∞,1)-functor]];

* it respects gluing in $\mathcal{G}$ in that 
  for $\{U_i \to V\}_i$ 
  a covering [[sieve]] consisting of admissible morphism, 
  the induced morphism

  $$
    \coprod_i O_X(U_i) \to O_X(V)
  $$

  is an [[effective epimorphism]] in $\mathcal{X}$.

=--

Write $Str_{\mathcal{G}}(\mathcal{X}) \subset Func(\mathcal{G},\mathcal{X})$ for the full subcategory of such morphisms of the [[(∞,1)-category of (∞,1)-functors]].

+-- {: .num_remark}
###### Remark

Without the condition on preservations of covers, the above defined the [[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]] over the [[essentially algebraic (∞,1)-theory]] $\mathcal{G}$. The preservation of covers encodes the **local** $\mathcal{G}$-algebras. 

Therefore we shall equivalently write

$$
  \mathcal{G}Alg_{loc}(\mathcal{X}) \simeq Str_{\mathcal{G}}(\mathcal{X})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

$\mathcal{G}Alg_{loc}(\mathcal{X})$ is the $(\infty,1)$-category of algebras over an $(\infty,1)$-[[geometric theory]]. 

=--

This is discussed [below](#InTermsOfClassifying).


### As algebras over geometric $(\infty,1)$-theories
{#InTermsOfClassifying}

By the [[(∞,1)-Yoneda lemma]], a 
cover-preserving functor $\mathcal{O} : \mathcal{G} \to \mathcal{X}$
[[Yoneda extension|Yoneda extends]] equivalently to a [[(∞,1)-colimit]]-preserving [[(∞,1)-functor]]

$$
  \mathcal{O} : Sh_{(\infty,1)}(\mathcal{G}) \to \mathcal{X}
  \,.
$$

By the [[adjoint (∞,1)-functor theorem]] this has a [[right adjoint|right]] [[adjoint (∞,1)-functor]] and if 
$\mathcal{O}$ preserves 
finite [[(∞,1)-limits]] then so does its extension. Therefore local $\mathcal{G}$-[[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]] in $\mathcal{X}$ are equivalent to [[(∞,1)-geometric morphism]]s

$$
  \mathcal{X} \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\to}
  Sh_{(\infty,1)}(\mathcal{G})
  \,.
$$

This means that structure sheaves 
$\mathcal{O} : \mathcal{G} \to \mathcal{X}$ are equivalently encoded
in [[geometric morphism]]s to the [[(∞,1)-category of (∞,1)-sheaves]] on the geometry.

Formally we have:

+-- {: .num_prop}
###### Proposition

For $\mathcal{G}$ a geometry, precomposition of the [[inverse image]] functor with the [[(∞,1)-Yoneda embedding]] $y : \mathcal{G} \to Sh_{(\infty,1)}(\mathcal{G})$ induces an [[equivalence of (∞,1)-categories]]

$$
  Topos(\mathcal{X}, Sh_{(\infty,1)}(\mathcal{G}))
  \stackrel{\simeq}{\to}
  \mathcal{G}Alg_{loc}(\mathcal{X})
$$

between the  [[(∞,1)-category of (∞,1)-functors|(∞,1)-category of (∞,1)-geometric morphisms]] from $\mathcal{X}$ to $Sh_{(\infty,1)}(\mathcal{G})$ and the $(\infty,1)$-category of local $\mathcal{G}$-[[∞-algebra over an (∞,1)-algebraic theory|∞-algebra]]s in $\mathcal{X}$.

=--

This is ([StrSp, prop 1.42](#Lurie)).

+-- {: .proof}
###### Proof

This follows from the general fact, discussed in the section <a href="http://nlab.mathforge.org/nlab/show/Yoneda+lemma+for+(infinity%2C1)-categories#LocalYonedaEmbedding">Local yoneda embedding</a> at [[(∞,1)-Yoneda lemma]] that the essential image of the $(\infty,1)$-functor

$$
  Topos(\mathcal{X}, Sh_{(\infty,1)}(\mathcal{G}))
  \stackrel{L}{\to}
  Topos(\mathcal{X}, PSh_{(\infty,1)}(\mathcal{G}))
  \stackrel{y}{\to}
  Func(\mathcal{G}, \mathcal{X})
$$

is spanned by the left exact and cover preserving functors. 


=--

+-- {: .num_remark}
###### Remark

We may think of this as saying that $Sh_{(\infty,1)}(\mathcal{G})$ is the $(\infty,1)$-[[classifying topos]] for the $(\infty,1)$-[[geometric theory]] of **local [[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]]** over the [[essentially algebraic (∞,1)-theory]] $\mathcal{G}$.

=--




### Local morphisms between structure sheaves {#LocalMorphisms}

+-- {: .num_remark}
###### Remark

The $(\infty,1)$-category $Str_{\mathcal{G}}(\mathcal{X})$
of $\mathcal{G}$-structure sheaves on an $(\infty,1)$-topos $\mathcal{X}$ 
does _not_ depend on the admissibility structure of $\mathcal{G}$, but only on the [[Grothendieck topology]] induced by it. 

=--

(See [[Structured Spaces|StrSp, remark below prop. 1.4.2]]).

The admissibility structure does serve to allow the following definition of _local_ morphisms of structure sheaves.

#### In terms of admissibility structures

+-- {: .num_defn}
###### Definition 
**(local morphism of structure sheaves)**

A [[natural transformation]] $\eta : \mathcal{O} \to \mathcal{O}' : \mathcal{G} \to \mathcal{X}$ of structure sheaves is **local** if for every admissible morphism $U \to X$ in $\mathcal{G}$ the naturality diagram

$$
  \array{
    \mathcal{O}(U) &\stackrel{\eta(U)}{\to}& \mathcal{O}'(U)
    \\
    \downarrow && \downarrow
    \\
    \mathcal{O}(X) &\stackrel{\eta(X)}{\to}& \mathcal{O}'(X)
  }
$$

is a [[limit in a quasi-category|pullback square]] in $\mathcal{X}$.

Write

$$
  Str^{loc}_{\mathcal{G}}(\mathcal{X}) \subset Str_{\mathcal{G}}(\mathcal{X})
$$

for the [[sub-quasi-category|sub-(∞,1)-category]] of $\mathcal{G}$-structures on $\mathcal{X}$ spanned by local transformations between them.

=--


#### In terms of classifying $(\infty,1)$-toposes
 {#InTermsOfClassifyingToposes}

Alternatively, the local transformations can be characterized as follows


it turns out the local transformations are the right half of a [[factorization system]] on $Str_{\mathcal{G}}(\mathcal{X})$, and that this factorization system depends functorially on $\mathcal{X}$, in that for every geometric morphism $\mathcal{X} \to \mathcal{Y}$ the induced $Str_{\mathcal{G}}(\mathcal{X}) \to Str_{\mathcal{G}}(\mathcal{Y})$ respects these factorization  systems. (theorem 1.3.1)

This one can turn around, to characterize local transformations (and hence admissibility structures on $\mathcal{G}$) in terms of functorial factorization systems on classifying $(\infty,1)$-toposes (def. 1.4.3):

For $\mathcal{K}$ an $(\infty,1)$-topos, declare that a _geometric structure_ on $\mathcal{K}$ is a choice of factorization systems on $Topos_{geom}(\mathcal{X}, \mathcal{K})^{op}$ that is functorial in $\mathcal{X}$ . Given such we have another way of saying "local transformation": this is the non-full subcategory $Str^{loc}_{\mathcal{K}}(\mathcal{X})$ of $Topos_{geom}(\mathcal{X}, \mathcal{K})^{op}$ on all objects and on the right part of the factorization system.

And this is indeed the same kind of datum as an admissibility structure on a geometry (example 1.4.4): in the case that $\mathcal{K} = Sh(\mathcal{G})$ is the classifying topos for the geometry $\mathcal{G}$, the defining equivalence $Topos_{geom}(\mathcal{X}, Sh(\mathcal{G}))^{op} \stackrel{\simeq}{\to} Str_{\mathcal{G}}(\mathcal{X})$ identifies the two sub-categories of local transformations, $Str^{loc}_{\mathcal{G}}(\mathcal{X})$ and $Str^{loc}_{Sh(\mathcal{G})}(\mathcal{X})$.




### The $(\infty,1)$-category of structured $(\infty,1)$-toposes {#CatOfStructuredToposes}

Let $(\infty,1)Toposes \subset $ [[(∞,1)Cat]]  be the [[sub-quasi-category|sub (∞,1)-category]] of [[(∞,1)-topos]]es: objects are [[(∞,1)-topos]]es, morphisms are [[geometric morphism]]s.

Write $LTop \coloneqq (\infty,1)Toposes^{op}$.

+-- {: .num_defn}
###### Definition 
**($(\infty,1)$-category of $\mathcal{G}$-structured $(\infty,1)$-toposes)**

For $\mathcal{G}$ a geometry, the $(\infty,1)$-category of
$\mathcal{G}$-structured $(\infty,1)$-toposes 

$$
  LTop(\mathcal{G})
$$

is defined as follows.

It is the [[sub-quasi-category|sub (∞,1)-category]] 

$$
  LTop(\mathcal{G})
  \subset
  Func(\mathcal{G}, E LTop) \times_{Func(\mathcal{G}, LTop)} LTop
  \,,
$$

where $E LTop \to LTop$ is the [[coCartesian fibration]] associated by the [[(∞,1)-Grothendieck construction]] to the inclusion functor $LTop \hookrightarrow (\infty,1)Cat$, spanned by the following objects and morphisms:

* objects are $\mathcal{G}$-structures $\mathcal{O} : \mathcal{G} \to \mathcal{X}$ on some $(\infty,1)$-topos $\mathcal{X}$:

  an object in 
  $Func(\mathcal{G}, E LTop) \times_{Func(\mathcal{G}, LTop)} LTop$ is an object $\mathcal{X} \on LTop$ together with a functor $\mathcal{G} \to E LTop|_{\mathcal{X}}$ into the fiber of $E Top$ over that object; but that fiber is $\mathcal{X}$ itself, so an object in the fiber product is a functor $\mathcal{G} \to \mathcal{X}$ and this is in $LTop(\mathcal{G})$ if it is a $\mathcal{G}$-structure on $\mathcal{X}$;

* morphisms $\alpha : \mathcal{O} \to \mathcal{O}'$ 
  are _local_ morphisms of $\mathcal{G}$-structures: 

  for $f^* : \mathcal{X} \to \mathcal{Y}$ the image of $\alpha$ in $LTop$,
  $\alpha$ is in $LTop(\mathcal{G})$ precisely if for every admissible morphism $U \to X$ in $\mathcal{G}$ the square

  $$
    \array{
     f^* \mathcal{O}(U) &\to& f^*\mathcal{O}(X)
     \\
     \downarrow^{} && \downarrow^{}
     \\
     \mathcal{O}'(U) &\to& \mathcal{O}'(X)
    }
  $$

  is a pullback square in $\mathcal{Y}$.

=--

This is [[Structured Spaces|StrSp, def 1.4.8]]


### The spectrum construction

For $f : \mathcal{G} \to \mathcal{G}'$ a morphism of geometries, let

$$
  \mathcal{O}_{\mathcal{G}}^{\mathcal{G}'}
  : 
  Topos(\mathcal{G}') \to Topos(\mathcal{G})
$$

be the induced functor on categories of structured toposes.

+-- {: .num_theorem}
###### Theorem

This functor is a left [[adjoint (∞,1)-functor]]

$$
  (
    \mathcal{O}_{\mathcal{G}}^{\mathcal{G}'}
      \dashv
    Spec_{\mathcal{G}^{\mathcal{G}'}})
  )
  : 
  Topos(\mathcal{G})
  \stackrel{\overset{\mathcal{O}_{\mathcal{G}}^{\mathcal{G}'}
}{\leftarrow}}{\underset{Spec_{\mathcal{G}}^{\mathcal{G}'}
}{\to}}
  Topos(\mathcal{G}')
  \,.
$$

=--

This is ([Lurie, theorem 2.1.1](#Lurie)).

+-- {: .num_defn}
###### Definition

For $\mathcal{G}$ a geometry, let $\mathcal{G}_0$ be the corresponding discrete geometry. We have a canonical morphism $\mathcal{G}_0 \to \mathcal{G}$.

Write

$$
  Spec^{\mathcal{G}} 
    : 
  Pro(\mathcal{G})
   \to 
  Topos(\mathcal{G}_0)
   \stackrel{Spec_{\mathcal{G}_0}^{\math}}{\to}
  Topos(\mathcal{G})
$$

for the composite.

=--

+-- {: .num_theorem}
###### Theorem

This fits into an adjunction

$$
  (\mathcal{O} \dashv Spec) : 
  Pro \mathcal{G} \stackrel{\overset{}{\leftarrow}}{\underset{}{\to}}
  Top(\mathcal{G})
  \,.
$$

=--

This is ([Lurie, theorem xyz](#Lurie)).

## Examples

### Classes of examples

#### Canonical structure sheaves on objects in the big topos {#CanonicalStructureSheafOnObjectsInBigTopos}

For $\mathcal{G}$ a [[geometry (for structured (infinity,1)-toposes)|geometry]] let

$$
  \mathbf{H} \coloneqq Sh_\infty(\mathcal{G})
$$

be the [[(∞,1)-category of (∞,1)-sheaves]] on $\mathcal{G}$. This is the [[big topos]] of [[higher geometry]] modeled on $\mathcal{G}$. By the [above discussion](#InTermsOfClassifying) it is also the classifying topos of $\mathcal{G}$-[[structure sheaves]] on toposes:

a $\mathcal{G}$-valued structure sheaf $\mathcal{O}_{\mathcal{X}} : \mathcal{G} \to \mathcal{X}$ on an [[(∞,1)-topos]] $\mathcal{X}$ is equivalently an [[(∞,1)-geometric morphism]]

$$
  (p^* \dashv p_*) 
   :  
  \mathcal{X} \stackrel{\leftarrow}{\to} \mathbf{H}
  \stackrel{j}{\leftarrow}
  \mathcal{G}
$$

in that $\mathcal{O}_{\mathcal{X}} = p^* j$, where $j$ is the [[(∞,1)-Yoneda embedding]].

Notice that for every object $X \in \mathcal{H}$ its [[little topos]]-incarnation is the [[over-(∞,1)-topos]] $\mathbf{H}/X$. This canonically sits over $\mathbf{H}$ by its [[etale geometric morphism]]

$$
  \mathcal{X} \coloneqq \mathbf{H}/X
  \stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}
  \mathbf{H}
  \,.
$$

So we have

+-- {: .num_lemma}
###### Observation

The [[little topos]] $\mathcal{X} \coloneqq \mathbf{H}/X$ of every object $X$ in the big topos $\mathbf{H}$ over $\mathcal{G}$ is canonically equipped with a $\mathcal{G}$-structure sheaf

$$
  \mathcal{O}_X : \mathcal{G} \stackrel{j}{\to} \mathbf{H}
  \stackrel{X^*}{\to}
  \mathbf{H}/X
  \,.
$$

=--

We want to show that for $V \in \mathcal{G}$ the [[(∞,1)-sheaf]] $\mathcal{O}_X(V)$ may indeed be thought of as the "sheaf of $V$-valued functions on $X$".

Notice that for any $V \in \mathbf{H}$ we have that $X^*(F) = (p_2 : V \times X \to X)$.

Now assume first that $X$ is itself representable. Then by the discussion at [[over-(∞,1)-topos]] we have that $\mathbf{H}/X$ is a lucalization of $PSh_\infty(\mathcal{G})/X \simeq PSh_\infty(\mathcal{G}/X)$, where $\mathcal{G}/X$ is the [[big site]] of $X$. Under this equivalence (more details on this at [[over-topos]]) we have that $(V \times X \to X)$ identifies with the presheaf given by

$$
  (U \to X) \mapsto \mathcal{G}(U,V)
  \,.
$$

This is the "sheaf of $V$-valued functions on $X$".

(...)


### Specific examples

#### Structure sheaves of continuous functions {#StrSheafOfcontFuncts}

  Consider $X$ an ordinary [[topological space]] and
   $Sh(X)$ the ordinary [[category of sheaves]] on its 
   [[category of open subsets]]. Let $\mathcal{G} = Top$
   be some [[small category|small]] version of [[Top]]
   with its usual [[Grothendieck topology]] with 
   admissible [[covering]]
   families being [[open cover]]s. Consider the functor

   $$
     O_X : Top \to Sh(X)
   $$

   that sends a topological space $V$ to the sheaf of 
   [[continuous function]]s with values in $V$:

   $$
     O_X(V) : U \mapsto C(U,V) = Hom_{Top}(U,V)
     \,.
   $$

   By general properties of the [[hom-functor]], this respects [[limit]]s. 
   The gluing condition says that
   for $V_1, V_2 \subset V$ an open cover of $V$ by two patches, 
   the morphism of sheaves

   $$
     O_X(V_1) \coprod O_X(V_2) \to O_X(V)
   $$

   is an [[epimorphism]] of sheaves. This means that 
   for each point $x \in X$ the map of [[stalk]]s

   $$
     O_X(V_1)_x \coprod O_X(V_2)_x \to O_X(V)_x
   $$
   
   is an epimorphism of sets. But this just says that given
   any function $f : U_x \to V$ on a neighbourhood $U_x$ of $x$, 
   there is a smaller neighbourhood $W_x \subset U_x$ such that 
   the restriction $f|_{W_x}$ factors either through $V_1$ or
   through $V_2$. This is clearly the case by the fact that $V_1,V_2$
   form an open cover. (A neighbourhood  of $f(x) \in V$ exists which
   is contained in $V_1$ or in $V_2$, so take its preimage under
   $f$ as $U_x$).


#### Locally ringed spaces

[StrSh, remark 2.5.11](http://arxiv.org/PS_cache/arxiv/pdf/0905/0905.0459v1.pdf#page=71) 

   Let $X$ be a topological space as before, but consider now the
   geometry $\mathcal{G} = CRing^{op}$ to be the opposite category of
   commutative [[ring]]s, where a covering family of 
   $Spec R \in CRing^{op}$ is a family of maps of the form
   $R \to R[\frac{1}{r_i}]$ with $\{r_i \in R\}_i$ generating the unit
   ideal in $R$. So we think of $Spec R[\frac{1}{r_i}]$ as 
   an the open subset of $Spec R$ on wich the function $r_i$
   does not vanish, and a covering family we think of as an open 
   cover by such open subsets, in direct analogy to the above example.
 
   Now given a sheaf of rings 

   $$
     \bar O_X \in Sh(X,CRing)
   $$

   on $X$ (making $X$ a [[ringed space]]), which we 
   may regard as the functor

   $$
     O_X : CRing^{op} \to Sh(X)
   $$

   that it [[representable functor|represents]]

   $$
     O_X(Spec R) : U \mapsto  
                   Hom_{CRing^{op}}(\bar O_X(U), Spec R)
                           = Hom_{CRing}(R, \bar O_X(U))
   $$

   we check what 
   conditions this has to satisfy to qualify as a 
   structure sheaf in the above sense.

   The condition that

   $$
     \coprod_i O_X(Spec R[\frac{1}{r_i}])
     \to Spec R
   $$

   is an epimorphism of sheaves again means that it is [[stalk]]wise
   an epimorphism of sets. Now, a ring homomorphism 
   $R[\frac{1}{r_i}] \to \bar O_X(U)$ is given by
   a ring homomorphism $f : R \to O_X(U)$ such that $f(r_i)$ is
   invertible in $O_X(U)$. (We think of this as the pullback of
   functions on $Spec R$ to functions on $U$ by a map $U \to Spec R$
   that lands only in the open subset where the functoin $r_i$ is 
   non-vanishing).

   So the condition that the above is an epimorphism on small enough
   $U$ says that for every ring homomorphism $\phi : R \to \bar O_X(U)$
   the value of $\phi$ on at least one of the $r_i$ is invertible 
   element in $O_X(U)$. 

   Thinking of this dually this is just the same kind of statement as
   in the first example, really. But now we can say this more 
   algebraically: 

   by assumption there is a linear combination of the $r_i$ to the
   identity in $R$

   $$
     1 = \sum_i \alpha_i r_i
   $$

   in $R$ (the partition of unity of functions on $Spec R$) 
   and hence $\sum_i \alpha_i \phi(r_1) = 1$ in $(O_X)_x$
   That for this invertible finite sum at least one of the
   summands is invertible is the condition that $(O_X)_x$ is
   a _local ring_ .

   So a [[ringed space]] has a structure sheaf in the above sense
   if it is a [[locally ringed space]].
   
   





#### Ordinary ringed spaces

It may be worthwhile to retell the motivating example in the "Idea" introduction above for the maybe more familiar case of ordinary (1-categorical) structure sheaves with values in (unital) rings.

An ordinary [[topological space]] $X$ with its [[category of open subsets]] $Op(X)$ is a [[ringed space]] or $Op(X)$ is a [[ringed site]] if it is equipped with a [[sheaf]] $O_X : Op(X)^{op} \to Rings$ with values in the category of [[rings]]. For $U \subset X$ one thinks of $O_X(U)$ as the ring of allowed functions on $U$.

If for the moment we ignore the technicality that $O_X$ is supposed to be a [[sheaf]] and just regard it as a [[presheaf]], and if we furthermore invoke the idea of [[space and quantity]] and think of a ring $R$ as a generalized quantity in form of a copresheaf, canonically the [[representable functor|co-representable]] co-presheaf

$$
  R : (Ring^fin)^{op} \to \Set
$$

on finitely generated rings, which sends

$$
 R : R' \mapsto Hom(R,R')
$$

then we find that $O_X$ is in fact a presheaf on $Op(X)$ with values in a co-presheaf on $(Ring^{fin})^{op}$

$$
  O_X : Op(X)^{op} \to [(Ring^{fin})^{op}, Set]
$$

or equivalently a generalized quantity on $(Ring^{fin})^{op}$ with values in presheaves on $X$:

$$
  O_X : (Ring^{fin})^{op} \to [Op(X)^{op}, Set]
  \,.
$$

Since rings can be identified with left-exact functors $(Ring^{fin})^{op}\to Set$, we don't need to impose any admissibility structure in order to recover the notion of a sheaf of rings, since left-exactness is part of the definition of a "structure sheaf."  We do, however, need an admissibility structure if we want to recover the notion of a sheaf of *local* rings, as in the previous example above.

#### Derived ringed spaces

Now formulate the previous example according to the above definition:

Let $CRing^{fin}$ be the category of finitely generated commutative rings There is a standard admissibility structure on $(CRing^{fin})^{op}$ that makes it a _geometry_ in the above sense.

Then for $X$ a topological space an $(\infty,1)$-functor $(CRing^{fin})^{op} \to Sh(S)$ to $(infty,1)$-sheaves on $X$  is a sheaf of local commutative rings on $X$. ([StrSh, example 1.2.13](http://arxiv.org/abs/0905.0459))

To generalize this to **derived structure sheaves** we replace the category of rings here with the $(\infty,1)$-category of simplicial rings.

**Definition**  ([StrSh def 4.1.1](http://arxiv.org/abs/0905.0459))

The $(\infty,1)$-category of **simplicial commutative rings** over an ordinary commutative ring $k$ is

$$
  SCR_k \coloneqq PSh_\Sigma(FreeAlg_k)
$$

the $(\infty,1)$-category of [[(∞,1)-presheaves]] on commutative $k$-algebras of the form $k[x_1, \cdots, x_n]$.

Then...


#### Derived smooth manifolds 

([StrSh, example 4.5.2](http://arxiv.org/abs/0905.0459))

Every ordinary [[smooth manifold]] $X$ becomes canonically a generalized space with structure sheaf as follows:

Let $V \coloneqq Diff$ be some version of the category of smooth manifolds. This becomes a _pregeometry_ in the above sense by taking admissible morphisms to be inclusions of open submanifolds.

Then for $Sh(X) \coloneqq Sh(Op(X))$ the $(\infty,1)$-topos of $(\infty,1)$-sheaves on $X$, the obvious $(\infty,1)$-functor

$$
  O_X : V \to Sh(X)
$$

which for every co-test manifold $v$ is the sheaf

$$
  O_X(v) : (U \subset X) \mapsto Hom_{Diff}(U,v)
$$

is a $Diff$-structure sheaf. Notice that this is precisely nothing but the structure sheaf of smooth functions from the introduction above. 

The point is that there are other, more fancy structure sheaves

$$
  O_X : V \to Sh(X)
$$

possible. They describe **[[derived smooth manifolds]]** as described in [DerSmooth](http://math.berkeley.edu/~dspivak/thesis2.pdf).

## Properties

### Limits and colimits
  {#LimitsAndColimits}


Let $\mathcal{G}$ be a [[geometry for structured (infinity,1)-toposes]]. Write $F : (\infty,1)Topos(\mathcal{G}) \to $ [[(∞,1)Topos]] for the [[forgetful functor|forgetful]] [[(∞,1)-functor]] from $\mathcal{G}$-structured $(\infty,1)$-toposes to their underlying $(\infty,1)$-topos.


+-- {: .prop_prop}
###### Proposition

The $(\infty,1)$-category $(\infty,1)Topos(\mathcal{G})$ has all [[filtered (∞,1)-category|cofiltered]] [[(∞,1)-limit]]s and the forgetful functor 
$F : (\infty,1)Topos(\mathcal{G}) \to (\infty,1)Topos$ preserves these.


=--

This appears as ([Lurie, corl 1.5.4](#Lurie)).


### Embedding into the ambient big $(\infty,1)$-topos
 {#EmbeddingIntoTheAmbientBigTopos}


+-- {: .num_defn}
###### Definition

For $\mathcal{G}$ a [[geometry (for structured (∞,1)-toposes)]] write 

$$
  \hat \mathcal{G} \coloneqq Pro(\mathcal{G})
$$

for its [[(∞,1)-category]] of [[ind-object in an (∞,1)-category|pro-objects]].

Write $\widehat{\infty Grpd}$ for the very large [[(∞,1)-category]] of large [[∞-groupoid]]s and

$$
  \hat Sh(\hat \mathcal{G}, \widehat{\infty Grpd})
$$

for the [[very large (∞,1)-sheaf (∞,1)-topos]].

=--

+-- {: .num_prop}
###### Proposition

The canonical inclusion

$$
  Scheme(\mathcal{G}) \to 
  \hat PSh(\hat \mathcal{G}, \widehat{\infty Grpd})
$$

of [[locally representable structured (∞,1)-topos]]es by 

$$
  (X, \mathcal{O}_X) \mapsto Hom(Spec(-), (X, \mathcal{O}_X))
$$

is a [[full and faithful (∞,1)-functor]].

=--

This is ([Lurie, theorem, 2.4.1](#Lurie)).


## Related concepts

* [[ringed space]], [[locally ringed space]]

* [[ringed site]], [[locally ringed site]]

* [[ringed topos]], [[locally ringed topos]]

* [[locally algebra-ed topos]]

* **locally algebra-ed (∞,1)-topos**

* [[geometry (for structured (∞,1)-toposes)]],  **structured $(\infty,1)$-topos** , [[locally representable structured (∞,1)-topos]]

Analogous structures in the axiomatic context of [[differential cohesion]] are discussed in _[differential cohesion --  Structure sheaves](cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#StructureSheaves)_.


## References

The notion of structured $(\infty,1)$-toposes was introduced in

* [[Jacob Lurie]], _[[Structured Spaces]]_ 
{#Lurie}

Analogous precursor discussion in 1-category theory, hence for [[ringed toposes]] is in 

* [[Monique Hakim]], _Topos annel&#233;s et sch&#233;mas relatifs_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 64, Springer, Berlin, New York (1972). 

The special case of "smoothly structured spaces" ([[derived smooth manifolds]]) is  discussed in 

* [[David Spivak]], _Derived smooth manifolds_ PhD thesis ([pdf](http://www.uoregon.edu/~dspivak/files/thesis1.pdf))



[[!redirects structured (∞,1)-topos]]

[[!redirects structured (∞,1)-toposes]]
[[!redirects structured (∞,1)-topoi]]
[[!redirects structured (infinity,1)-toposes]]
[[!redirects structured (infinity,1)-topoi]]


[[!redirects structured generalized spaces]]
[[!redirects structured generalized space]]
[[!redirects ringed (∞,1)-topos]]
[[!redirects ringed generalized spaces]]
[[!redirects ringed generalized space]]

[[!redirects locally algebra-ed (∞,1)-topos]]
[[!redirects locally algebra-ed (infinity,1)-topos]]
[[!redirects locally algebra-ed (∞,1)-toposes]]
[[!redirects locally algebra-ed (infinity,1)-toposes]]