
> This page is about object classifier objects in [[(∞,1)-toposes]]. For the unrelated notion of the [[classifying topos]] of the [[theory of objects]] see at _[[classifying topos for the theory of objects]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A crucial ingredient in a [[topos]] is a [[subobject classifier]]. From the point of view of [[homotopy theory]], that this has to do with [[subobjects]] turns out to be a coincidence of low dimensions: subobjects are [[(-1)-truncated]] morphisms. 

As discussed also at [[stuff, structure, property]], the classifying objects in [[higher topos theory]] classify more general morphisms.

When one passes all the way to [[∞-toposes]], there should be objects that classify _all_ morphisms, subject to some bound on size. This is made precise in the context of [[(∞,1)-topos theory]].

One way to characterize an [[(∞,1)-topos]] is as 

* a [[presentable (∞,1)-category]]

* with [[universal colimits]]

* such that for all sufficiently large [[regular cardinal]]s $\kappa$ there is a **classifying object** for the class of all $\kappa$-compact morphisms in $X$.

This statement is originally due to [[Charles Rezk]]. It is reproduced as ([[Higher Topos Theory|Lurie HTT, theorem 6.1.6.8]]).


In terms of [[homotopy type theory]] these object classifiers are _[[types of types]]_. See there for more details and see at _[[relation between category theory and type theory]]_.

+-- {: .num_remark #ReflectonOnCharacterizationByObjectClassifier}
###### Remark

An [[object classifier]] is a (small) _self-reflection_ of the $(\infty, 1)$-topos inside itself ([[type of types]], internal [[universe]]). It possesses an [[category object in an (infinity,1)-category|internal (∞,1)-topos ]] structure. See also ([[Science of Logic#WesenAlsReflexionInIhmSelbst|WdL, book 2, section 1]]).

=--

## Definition
 {#Definition}


Let $\mathcal{C}$ be a [[(∞,1)-category]], and let $S$ be a class of [[1-morphisms]] of $\mathcal{C}$ which is stable under [[(∞,1)-pullback]]. Then an **$S$-classifier** is a [[terminal object in an (∞,1)-category|terminal object]] in the sub-[[arrow category|category of arrows]] $\mathcal{C}^{\Delta^1}$ of $S$ whose morphisms are [[(∞,1)-pullback]] squares in $\mathcal{C}$.

Explicitly, an $S$-classifier consists of 

* a morphism $\widehat {S Type} \longrightarrow S Type$ in $S$ 

* such that for each $X \stackrel{p}{\to} B$ in $S$, there exists an essentially unique [[(∞,1)-pullback]] square of the form

  $$
    \array{
       X &\longrightarrow& \widehat {S Type}
       \\
       \downarrow^{\mathrlap{p}} && \downarrow
       \\
       B &\stackrel{'X'}{\longrightarrow}& S Type
    }
    \,.
  $$

  in $\mathcal{C}$

Here $'X'$ may be called the _name_, or the _[[classifying morphism]]_, or the _[[modulating morphism]]_ or the _internal reflection_ of $X$ over $B$, 

For example,

* When $S$ is the class of **all monomorphisms** in $C$, an $S$-classifier is called a **subobject classifier**. For instance, every topos has a subobject classifier.

* When $S$ is the class of **all faithful morphisms** in $C$, an $S$-classifier is called a **discrete object classifier**. For instance, every (2,1)-topos has a discrete object classifier.

* When $S$ is the class of **all morphisms** in $C$, an $S$-classifier is called an **object classifier**. However, due to size issues, interesting categories tend not to have such objects, which is one reason to be interested in the next example:

* When $S$ is the class of **all relatively $\kappa$-compact morphisms** (for some regular cardinal $\kappa$--see below for the definition), an $S$-classifier is called a **$\kappa$-compact-object classifier**.

**Note on terminology:** In all cases, the "things" classified by an "(adjectives) object classifier" are _arrows_ -- this is no different from the most famous case of _[[subobject classifiers]]_, which classify _monos_. For each object $X$, a _subobject classifier_ classifies the _subobjects of $X$_. For each object $X$, an _object classifier_ classifies the _objects over $X$_.

So with that $\kappa$ fixed, we may write

$$
  \array{
    \widehat Type
    \\
    \downarrow
    \\
    Type
  }
$$

for such a "universal bundle of $\kappa$-small objects". Intuitively this is easy to describe: a point in $Type$ corresponds to a $\kappa$-small object, hence is the "name" $'X'$ or "code for" a $\kappa$-small object, and the [[fiber]] in $\widehat Type$ over that point is the very object $X$ itself. 

If one gives the projection of the universal object bundle $\widehat Type \to Type$ a name, such as $El$, and writes $El^{-1}(-)$ for its preimages then $X \simeq El^{-1}('X')$. This is, with the ${(-)}^{-1}$-suppressed, the notation used at _[Type universes a la Tarski](type+of+types#TarskiStyle)_.

## Details

### n-truncated object classifier

+-- {: .num_defn}
###### Definition

Let $C$ be an [[(∞,1)-category]] and $S \in C_1$ a class of [[morphisms]] that is stable under [[(∞,1)-pullback]] in $C$.

Let $Cod_C$ be the [[codomain fibration]] of $X$, i.e. the [[(∞,1)-category of (∞,1)-functors]]

$$
  Cod_C := Func(\Delta[1], C)
$$

equipped with the [[Cartesian fibration]] $Cod_C \to C$ induced from the endpoint inclusion $\Delta[0] \to \Delta[1]$.

Write

* $Cod_C^S$ for the full [[sub-(∞,1)-category]] of $Cod_C$ on the object in $S$;

* $Cod_C^{(S)}$ the non-full subcategory whose objects are the elements of $S$, and whose morphisms are squares that are pullback diagrams.

Then evaluation at $\Delta[0] \to \Delta[1]$ yields

* a [[Cartesian fibration]] $Cod_C^S \to C$;

* a [[right fibration]] $Cod_C^{(S)} \to C$.

We say a morphism $f :x \to y$ in $C$ _classifies_ $S$ -- or simply that $y$ classifies $S$ -- if it is the [[terminal object]] in $Cod_C^{(S)}$.

=--

This is [[Higher Topos Theory|HTT, notation 6.1.3.4]] and [[Higher Topos Theory|HTT, def. 6.1.6.1 ]].

#### Subobject classifier {#DetailsSubObjClassf}

+-- {: .num_defn}
###### Definition

A **subobject classifier** for $C$ is an object that classifies the class $S$ of [[monomorphism in an (∞,1)-category|monomorphisms]]/[[(-1)-truncated]] morphisms in $C$.

=--

This is ([[Higher Topos Theory|HTT, def. 6.1.6.1 ]]).


+-- {: .num_example}
###### Example

The $(\infty,1)$-category [[∞Grpd]] has a a subobject classifier: the [[0-groupoid]]/[[set]] $\{\emptyset,*\}$ with two elements (the two [[(-1)-truncated]] $\infty$-groupoids).

=--

+-- {: .num_prop}
###### Proposition

Every [[(∞,1)-topos]] has a [[subobject classifier]].

=--



This appears as ([[Higher Topos Theory|HTT, prop. 6.1.6.3]]) and the remark below that.

#### Discrete object classifier 

+-- {: .num_defn}
###### Definition

A **discrete object classifier** for $C$ is an object that classifies the class $S$ of [[faithful morphism in an (∞,1)-category|faithful morphism]]/[[(0)-truncated]] morphisms in $C$.

=--

+-- {: .num_example}
###### Example

The $(\infty,1)$-category [[∞Grpd]] has a a discrete object classifier: the [[1-groupoid]]/[[groupoid]] [[Set]] whose elements are sets ([[0-truncated]] $\infty$-groupoids).

=--

+-- {: .num_prop}
###### Proposition

Every [[(∞,1)-topos]] has a [[discrete object classifier]].

=--

### Object classifier {#DetailsObjClassf}


**Remark/Warning.** The point of having [[subobjects]] and hence [[monomorphisms]] classified by an object in an ordinary [[topos]] may be thought of as being solely due to the fact that in a 1-[[topos]], any object necessarily classifies a _[[poset]]_ i.e. a [[(0,1)-category]] of morphisms, and the point of subobjects/monomorphisms of a given object is that they do not have [[automorphisms]].

In an $(\infty,1)$-topos we thus expect an object that classifies _all_ morphisms, in that the assignment

$$
  c \mapsto Core(C_{/c})
$$

of an object $c\in C$ to the [[core]] of its [[over quasi-category|over (∞,1)-category]] yields a [[(∞,1)-functor]] $C^{op} \to \infty Grpd$ that is [[representable functor|representable]].

Indeed, this is _essentially_ the case -- up to size issues, that the following definitions take care of.

+-- {: .num_defn #RelativelyKappaCompact}
###### Definition

For $\kappa$ some [[cardinal]], say a morphism $f : x \to y$ in $C$ is **[[relatively k-compact morphism in an (infinity,1)-category|relatively k-compact]]** if for all [[(∞,1)-pullbacks]] along $h : y' \to y$ to $\kappa$-[[compact object in an (∞,1)-category|compact object]]s, $y'$, the pulled back object $h^* x'$ is itself a $\kappa$-compact object.

=--


+-- {: .num_theorem}
###### Theorem

A [[presentable (∞,1)-category]] $C$  is an [[(∞,1)-topos]] precisely if

1. it has [[universal colimits]];

1. for sufficiently large regular [[cardinal]]s $\kappa$, $C$ has a classifying object for relatively $\kappa$-compact morphisms.

=--


This is due to [[Charles Rezk]]. The statement appears as [[Higher Topos Theory|HTT, theorem 6.1.6.8]].

The proof essentially consists of showing that by the [[adjoint functor theorem]], the existence of object classifiers is equivalent to [[continuous functor|continuity]] of the [[core]] [[self-indexing]] $C^{op} \to \infty Gpd$ defined by $x\mapsto Core(C/x)$.  In the presence of universal colimits, this latter condition is equivalent to all colimits being [[van Kampen colimits]], which in turn yields the connection to the Giraud-type exactness properties.



## Examples

### Object classifier in $\infty Grpd$
  {#ObjectClassifierInInfinityGroupoid}

We discuss that the $\kappa$-small object classifier in the $(\infty,1)$-topos
[[∞Grpd]] of [[∞-groupoids]] is itself the [[core]] of the [[(∞,1)-category]] $\infty Grpd_\kappa$ of $\kappa$-small $\infty$-groupoids. Observing that the connected components of this are the [[delooping]] $B Aut(F)$ of the [[automorphism ∞-group]] of a given [[homotopy type]] $[F]$, and using that [[∞Grpd]] is [[presentable (∞,1)-category|presented]] by [[Top]] $\simeq$ [[sSet]] (see also at _[[homotopy hypothesis]]_) this recovers classical theorems about the classification of [[fibrations]] in simplicial sets/topological spaces by a [[universal Kan fibration]], as listed in the [References](http://ncatlab.org/nlab/show/associated+infinity-bundle#References) at _[[associated ∞-bundle]]_.

+-- {: .num_prop }
###### Proposition

The $\kappa$-compact object classifier in [[∞Grpd]]
is 

$$
  Type_\kappa := Core(\infty Grpd_\kappa)
  \,,
$$ 

the [[core]] of the [[full sub-(∞,1)-category]] of [[∞Grpd]] on the $\kappa$-[[small ∞-groupoids]].

The corresponding [[universal bundle]] is presented by the map of [[simplicial sets]]

$$
   \widehat Type_\kappa \to Type_\kappa
$$

which is the [[pullback]] of simplicial sets

$$
  \array{
    \widehat Type_\kappa &\to& Z_{\infty Grpd}
    \\
    \downarrow && \downarrow
    \\  
    Type_\kappa &\to& \infty Grpd 
  }
$$

of the [[universal right fibration]] along the defining inclusion of (the [[Kan complex]] presenting) $Type_\kappa$.

=--

+-- {: .num_lemma #RelativelyCompactInInfinityGroupods}
###### Lemma

In [[∞Grpd]] the relatively $\kappa$-compact morphisms, $X \to Y$, def. \ref{RelativelyKappaCompact}, are precisely those all whose [[homotopy fibers]]

$$
  X_{y} := X \times_{Y} \{y\}
$$ 

over all [[objects]] $y \in Y$ are $\kappa$-[[small infinity-groupoids]].

=--

+-- {: .proof}
###### Proof

We may write $Y$ as an [[(∞,1)-colimit]] over itself (see there)

$$
  Y \simeq {\lim_{\to}}_{y \in Y} \{y\} 
$$

and then use the fact that [[∞Grpd]] -- being an [[(∞,1)-topos]] -- has 
[[universal colimits]], to obtain the [[(∞,1)-pullback]] diagram

$$
  \array{
    {\lim_{\to}}_{y \in Y} X_y 
      &\stackrel{\simeq}{\to}
     & X
    \\
    \downarrow && \downarrow
    \\
    {\lim_{\to}}_{y \in Y} \{y\}
    &\stackrel{\simeq}{\to}&
    Y
  }
$$

exhibiting $X$ as an $(\infty,1)$-colimit of $\kappa$-small objects
over $Y$. By stability of $\kappa$-compact objects under
$\kappa$-small colimits (see [here](http://ncatlab.org/nlab/show/compact+object+in+an+%28infinity%2C1%29-category#StabilityUnderColimits))
it follows that $X$ is $\kappa$-compact if $Y$ is. 

=--

+-- {: .proof}
###### Proof of the proposition

Since [[right fibrations]] are stable under pullback (see [here](http://ncatlab.org/nlab/show/right%2Fleft+Kan+fibration#PreservationByPullback)), this is still a right fibration. Since, up to equivalence, every morphism into a [[Kan complex]] is a 
right fibration (see [here](http://ncatlab.org/nlab/show/right%2Fleft+Kan+fibration#OverKanComplex)), and since every
morphism out of a Kan complex into $\infty Grpd_\kappa$ factors
through the core $Type_\kappa$ it follows that
$Type_\kappa$ classifies all morphisms $X \to Y$ in [[∞Grpd]] whose [[homotopy fibers]] 

$$
  X_y \simeq X \times_Y \{y\}
$$ 

are $\kappa$-[[compact object in an (∞,1)-category|compact]].

The claim then follows with lemma \ref{RelativelyCompactInInfinityGroupods}.

=--

### Object classifier in presheaf $(\infty,1)$-toposes

Let $C$ be an [[(∞,1)-category]] and $\mathbf{H} = PSh_{\infty}(C)$ the [[(∞,1)-category of (∞,1)-presheaves]] over $C$.



By the [[(∞,1)-Yoneda lemma]], 
the $\kappa$-compact object classifier here should be
the presheaf which assigns to $U \in C$ the 
$\infty$-groupoid of relatively $\kappa$-compact
morphisms $X \to U$ in $PSh_\infty(C)$.

## Related concepts

* [[univalent foundations for mathematics]]

* [[type of propositions]], [[subobject classifier]], [[partial map classifier]]

* [[type of sets]], [[category of sets]], [[discrete object classifier]]

* [[type of types]], [[univalence]]

* [[classifying morphism]]

* [[Awodey's conjecture]]

## References



* [[Jacob Lurie]],  section 6.1.6 of _[[Higher Topos Theory]]_ 



[[!redirects object classifier]]
[[!redirects object classifiers]]
[[!redirects (sub)object classifier in an (∞,1)-topos]]
[[!redirects (sub)object classifiers in an (∞,1)-topos]]
[[!redirects (sub)object classifier in an (infinity,1)-topos]]
[[!redirects (sub)object classifiers in an (infinity,1)-topos]]
[[!redirects object classifier in an (∞,1)-topos]]
[[!redirects object classifiers in an (∞,1)-topos]]
[[!redirects object classifier in an (infinity,1)-topos]]
[[!redirects object classifiers in an (infinity,1)-topos]]
[[!redirects (sub)object classifier in an (∞,1)-category]]
[[!redirects (sub)object classifiers in an (∞,1)-category]]
[[!redirects (sub)object classifier in an (infinity,1)-category]]
[[!redirects (sub)object classifiers in an (infinity,1)-category]]
[[!redirects object classifier in an (∞,1)-category]]
[[!redirects object classifiers in an (∞,1)-category]]
[[!redirects object classifier in an (infinity,1)-category]]
[[!redirects object classifiers in an (infinity,1)-category]]