
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An **$n$-truncated [[∞-groupoid]]** is an [[n-groupoid]].

An **$n$-truncated [[topological space]]** is a [[homotopy n-type]]: all [[homotopy group]]s above degree $n$ are trivial.

An **$n$-truncated object** in a general [[(∞,1)-category]] is an object such that all hom-$\infty$-groupoids into it are $n$-truncated.

If an object in an [[(∞,1)-topos]]_ is $k$-truncated for any (possibly large) $k$, then it is $n$-truncated precisely if all its [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] above degree $n$ are trivial. 

The complementary notion of $n$-truncated object  is that of an [[n-connected object of an (∞,1)-category]].

## Definition

### In terms of truncations

+-- {: .un_defn}
###### Definition
**($n$-truncated $\infty$-groupoid)**

An [[∞-groupoid]] $A \in \infty Grpd$ is **$n$-truncated** for $n \in \mathbb{N}$ if it is an [[n-groupoid]]:

Precisely: in the model of [[∞-groupoid]]s given by [[Kan complex]]es $A$ is **$n$-truncated** if the [[simplicial homotopy group]]s $\pi_k(A,x)$ are trivial for all $x$ and all $k \gt n$.

=--

It makes sense for the following to adopt the convention that $A$ is called 

* _$(-1)$-truncated_ if it is empty or contractible -- this is a [[(-1)-groupoid]].

* $(-2)$-truncated if it is non-empty and contractible -- this is a [[(-2)-groupoid]].

(following [[Higher Topos Theory|HTT, p. 6]]).

To generalize this, let now $C$ be an arbitrary [[(∞,1)-category]]. For $X,A$ objects in $C$ write $C(X,A) \in $ [[? Grpd]] for the [[(∞,1)-categorical hom-space]] (if $C$ is given as a [[simplicially enriched category]] then this is just the [[SSet]]-[[hom-object]] which is guaranteed to be a [[Kan complex]]).

Using this, it shall be useful to slightly reformulate the above as follows:

+-- {: .un_lemma}
###### Observation

An [[∞-groupoid]] $A$ is $n$-truncated precisely for all other [[∞-groupoid]]s $X$ the hom-$\infty$-groupoid $\infty Grpd(X,A)$ is $n$-truncated.

=--

In categorical terms this just says that [[(n,k)-transformation|(∞,k)-transformation]] between $X$ and $A$ whose components a [[k-morphism]]s in $A$ cannot be nontrivial for $k \gt n$ if there are no nontrivial [[k-morphism]]s with $k \gt n$ in $A$.

Using this fact we can transport the notion of $n$-truncation to any [[(∞,1)-category]] by testing it on hom-[[∞-groupoid]]s:

+-- {: .un_defn}
###### Definition
**($n$-truncated object in an $(\infty,1)$-category)**

An object $A \in C$ of an [[(∞,1)-category]] $C$ is **$n$-truncated**, for $n \in \mathbb{N}$, if for all $X \in C$ the hom-[[∞-groupoid]] $C(X,A)$ is $n$-truncated.

=--

This is [[Higher Topos Theory|HTT, def. 5.5.6.1]].


Some terminology:

* A 0-truncated object is also called **discrete** . Notice that this is _categorically discrete_ as in [[discrete category]], not discrete in the sense of [[topological space]]s. An object in an [[(∞,1)-topos]] is discrete in this sense if, regarded as an [[∞-groupoid]] with extra structure it has only trivial morphisms.

* By the above convention on (-2)-truncated $\infty$-groupoid, it is the [[terminal object]]s of $C$ that are (-2)-truncated.


+-- {: .un_defn}
###### Definition
**($n$-truncated morphism in an $(\infty,1)$-category)**

A morphism $f : X \to Y$ of [[∞-groupoid]]s is $n$-truncated if all of its [[nLab:homotopy fiber]]s are.

A morphism $f : X \to Y$ in an [[(∞,1)-category]] $C$ is $n$-truncated if for all $W \in C$ the postcomposition morphism

$$
  C(W,f) : C(W,X) \to C(W,Y)
$$

is $n$-truncated in [[∞Grpd]].

=--

By the [characterization of homotopy fiber of functor categories](http://ncatlab.org/nlab/show/fiber+sequence#OfFuncCats)
this is equivalent to saying that $F$ is $k$-truncated when regarded as an
object of the [[over quasi-category|over (∞,1)-category]] $C_{/Y}$.

### In terms of categorical homotopy groups 

At least if the ambient [[(∞,1)-category]] is even an [[∞-stack]] [[(∞,1)-topos]] there is an alternative, more intrinsic, characterization of $n$-truncation in terms of [[categorical homotopy groups in an (∞,1)-topos]]:

+-- {: .un_prop}
###### Proposition

Suppose that an object $X$ in an [[∞-stack]] [[(∞,1)-topos]] is $k$-truncated for _some_ $k \in \mathbb{N}$ (possibly very large).

Then for any $n \in \mathbb{N}$ this $X$ is $n$-truncated precisely if all the [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] above degree $n$ are trivial.

=--

+-- {: .proof}
###### Proof


This is [[Higher Topos Theory|HTT, prop 6.5.1.7]].

=--

+-- {: .un_remark}
###### Remark

Notice that this expected statement does require the assumption that $X$ is $k$-truncated for some $k$. Without any _a priori_ truncation assumption on $X$, there is no comparable statement about the relaton to categorical homotopy groups. See [[Higher Topos Theory|HTT, remark 6.5.1.8]].

=--


## Properties

### Recursive definition {#RecursiveDefinition}

+-- {: .un_prop}
###### Proposition

In an $(\infty,1)$-category $C$ with finite limits, a morphism
$f : X \to Y$ is $k$-truncated (for $k \geq -1$) precisely if the
diagonal morphism $X \to X \times_Y X$ is $(k-1)$-truncated.

=--

This is [[Higher Topos Theory|HTT, lemma 5.5.6.15]].

+-- {: .proof}
###### Proof

By definition $f$ is $k$-truncated if for each object 
$d \in C$ we have that $C(d,f)$ is $k$-truncated in 
[[∞Grpd]]. Since the [[hom-functor]]s $C(d,-)$ preserve
finite [[limit in a quasi-category|limits]], wee have 
in particular that $X \to X \times_Y X$ in $C$ 
is $k$-truncated 
if $C(d,X) \to C(d,X) \times_{C(d,Y)} C(d,X)$ is
$k$-truncated for all $d$ in [[∞Grpd]]. Therefore it is 
sufficient to prove the statement for
morphisms in $C =$ [[∞Grpd]].

So let now $f : X \to Y$ be a morphism of [[∞-groupoid]]s. 
We may find a fibration $\bar \phi : \bar X \to \bar Y$ 
between [[Kan complex]]es  in [[sSet]] that models $f : X \to Y$
in the standard [[model structure on simplicial sets]], and by the
standard rules for [[homotopy pullback]]s it follows that the object
$X \times_Y X$ in $\infty$-Grpd is then modeled by the ordinary 
[[pullback]] $\bar X \times_{\bar Y} \bar X$ in [[sSet]]. And the
homotopy fibers of $f$ over $y \in Y$ are then given by the ordinary fibers 
$\bar X_y$ of $\bar f$ in $sSet$.

This way the statement is reduced to the following fact: a [[Kan complex]]
$\bar X_y$ is $k$-truncated precisely if the [[homotopy fiber]]s of
$\bar X_y \to \bar X_y \times \bar X_y$ are $(k-1)$-truncated.

We write now $X$ for $\bar X_y$, for simplicity. To see the last statement, 
let $(a,b) : * \to X \times X$ and compute the [[homotopy pullback]]

$$
  \array{
     Q &\to& *
     \\
     \downarrow && \downarrow^{\mathrlap{(a,b)}}
     \\
     X &\to& X \times X
  }
$$

as usual by replacing the right vertical morphism by the fibration
$(X \times X)^I \times_{X \times X} (a,b) \to X \times X$
and then forming the ordinary pullback. This shows that 
$Q$ is equivalent to the space of paths $P_{a,b}X$ in $X$ from $a$ to $b$.
(Use that gluing of [[path space object]]s at endpoints of 
paths produces a new
path space, see for instance section 4 of [[BrownAHT]]).

If $X$ is [[connected]], then choosing any path $a \to b$ 
gives an isomorphism from the the homotopy groups of $P_{a,b} X$
to those of the [[loop space]] $\Omega_a X$. These latter are indeed those
of $X$, shifted down in degree by one (as described for instance at
[[fiber sequence]]).

If $X$ is not connected, we can easily reduce to the case that it is.

=--



### General

+-- {: .un_prop}
###### Proposition

For $C$ an $(\infty,1)$-category and $k \geq -2$, the full [[sub-(∞,1)-category]] $\tau_{\leq k} C$ is stable under all [[limit in a quasi-category|limits]] in $C$.

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.6.5]].



## Truncation 

### Definition

Under mild conditions there is for each $n$ a universal way to send an arbitrary object $A$ to its $n$-truncation $\tau_{\leq n} A$. This is a general version of [[decategorification]] where [[k-morphism|n-morphism]]s are identified if they are connected by an invertible $(n+1)$-morphism.

For $C$ an [[(∞,1)-category]] and $n \geq -2$ in $\mathbb{Z}$ write $\tau_{\leq n} C $ for the [[full subcategory]] of $C$ on its $n$-truncated objects. 

So for instance for $C = $ [[∞Grpd]] we have $\tau_{\leq n} \infty Grpd = n Grpd$.


+-- {: .un_prop}
###### Proposition

If $C$ is an [[(∞,1)-category]] that is [[presentable (∞,1)-category|presentable]] then the canonical inclusion [[(∞,1)-functor]]

$$
  \tau_{\leq n} C \hookrightarrow C
$$

has an [[accessible (infinity,1)-functor|accessible]] [[left adjoint]]

$$
  \tau_{\leq n} : C \to C_{\leq n}
  \,.
$$

=--

This is [[Higher Topos Theory|HTT 5.5.6.18]].


Indeed, as the notation suggests, $C_{\leq n}$ is the [[essential image]] of $C$ under $\tau_{\leq n}$. The image  $\tau_{\leq n} A$ of an object $A$ under this operation is the **$n$-truncation** of $A$.

So $n$-truncated objects form a [[reflective sub-(∞,1)-category]] 

$$
  \tau_{\leq n} C
  \stackrel{\overset{\tau_{\leq n}}{\leftarrow}}{\hookrightarrow}
  C
  \,.
$$

### Properties {#Properties}

#### General {#GeneralPropsTruncation}


+-- {: .un_cor}
###### Observation/Corollary

A left [[exact functor]] 
$F : C \to D$
between $(\infty,1)$-categories with finite limits sends
$k$-truncated objects/morphisms to $k$-truncated objects/morphisms.

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.6.1.6]].


+-- {: .proof}
###### Proof

Follows from the above recursive characterization of 
$k$-truncated morphisms by the $(k-1)$-truncation of their
diagonal, which is preserved by the finite limit preserving $F$.

=--


+-- {: .un_prop}
###### Proposition

A presentable $(\infty,1)$-functor $F : C \to D$  between
[[locally presentable (∞,1)-categories]] $C$ and $D$ commutes with 
truncation:

$$
  F \circ \tau^C_{\leq k} \simeq \tau^D_{\leq k} \circ F
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.6.28]].

+-- {: .proof}
###### Proof

By the above lemma, $F$ restricts to a functor on the truncations. So we need to show that the diagram

$$
  \array{
    C &\stackrel{F}{\to}& D
    \\
    {}^{\mathllap{\tau_{\leq k}}}\downarrow 
    & (?) & 
    \downarrow^{\mathrlap{\tau_{\leq k}}}
    \\
    \tau_{\leq k } C &\stackrel{F}{\to}&
    \tau_{\leq k} D
  }
$$

in [[(∞,1)Cat]] can be filled by a 2-cell. To see this, notice that the
[[adjoint (∞,1)-functor]] of both composite morphisms exists 
(because that of $F$ exists by the [[adjoint (∞,1)-functor theorem]]
and bcause adjoints of composites are composites of adjoints)
and since the bottom morphism is just the restriction of the top morphism
and the right adjoints of the vertical morphisms are full inclusions
this adjoint diagram 

$$
  \array{
    C &\stackrel{G}{\leftarrow}& D
    \\
    \uparrow 
    & & 
    \uparrow
    \\
    \tau_{\leq k } C &\stackrel{G}{\leftarrow}&
    \tau_{\leq k} D
  }
  \,.
$$

evidently commutes, since it just expresses this restriction.

=--


+-- {: .un_prop}
###### Proposition

If $C$ is an [[(∞,1)-topos]], then truncation $\tau_{\leq n} : C \to C$ preserves finite [[limit in a quasi-category|products]].

=--

This appears as [[Higher Topos Theory|HTT, lemma 6.5.1.2]].

+-- {: .proof}
###### Proof

First notice that the statement is true for $C = $ [[∞Grpd]]. For instance we can use the example [In ∞Grpd and Top](#InInfGrpd), model [[∞-groupoid]]s by [[Kan complex]]es and notice that then $\tau_{\leq n}$ is given by the truncation functor $tr_{n+1} : sSet \to [\Delta^{op}_{\leq n+1}, sSet]$. This is also a [[right adjoint]] and as such preserves in particular product in $sSet$, which are $(\infty,1)$-products in $\infty Grpd$.

From that we deduce that the statement is true for  $C$ any [[(∞,1)-category of (∞,1)-presheaves]] $C = PSh_{(\infty,1)}(K) = Func_{(\infty,1)}(K^{op}, \infty Grpd)$ because all relevant operations there are objectwise those in $\infty Grpd$.

So far this shows even that on presheaf $(\infty,1)$-toposes all products (not necessarily finite) are preserved by truncation.

A general [[(∞,1)-topos]] $C$ is (by definition) a left exact [[reflective sub-(∞,1)-category]] of a presheaf $(\infty,1)$-topos, 

$$
  C \stackrel{\overset{L}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  PSh_{(\infty,1)}(K)
  \,.
$$ 

Let $\prod_{j} i(X_j)$ be the product of the objects in question
taken in $PSh(K)$. By the above there we have an equivalence

$$
  \tau_{\leq k} \prod_j i(X_j)
  \stackrel{\simeq}{\to}
  \prod_j \tau_{\leq} i(X_j)
  \,.
$$

Now applying $L$ to this equivalence and using now that $L$ preserves the
_finite_ product, this gives an equivalence

$$
  L \tau_{\leq k} \prod_j i(X_j)
  \stackrel{\simeq}{\to}
  L \prod_j \tau_{\leq} i(X_j)
  \simeq
  \prod_j L \tau_{\leq} i(X_j)
$$

in $C$. The claim follows now with the above result that $L \circ \tau_{\leq n} \simeq \tau_{\leq n} \circ L$.

=--




#### Postnikov tower

By the fact that the truncation functor $\tau_{\leq n}$ is a [[left adjoint]] one obtains canonical morphisms

$$
  \tau_{\leq n}A  \to A
$$

as the [[adjunct]] of the [[identity]] on $A$, and then by iteration also canonical morphisms

$$
  \tau_{\leq (n+1)} A \to \tau_{\leq n} A
  \,.
$$

For any $A \in C$ the sequence

$$
  \cdots
   \to \tau_{\leq 2}A \to \tau_{\leq 1} A \to \tau_{\leq 0} A
$$

is the [[Postnikov tower in an (∞,1)-category]] of $A$. See there for more details.



### Relation to homotopy groups {#RelationToHomotopyGroups}

In an $(\infty,1)$-topos $C$ there is a notion of categorical [[homotopy groups in an (∞,1)-topos]]. For the $(\infty,1)$-topos [[∞Grpd]] given by the model of [[Kan complex]]es this coincides with the notion of [[simplicial homotopy groups]]:

+-- {: .un_lemma}
###### Observation

An object $A$ in the [[(∞,1)-topos]] [[∞Grpd]] is $n$-truncated precisely if its [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] $\pi_k(A)$ vanish for all $k \gt n$.

=--

This simple relation between $n$-truncation and categorical homotopy groups is almost, but not exactly true in an arbitrary [[(∞,1)-topos]].

+-- {: .un_prop}
###### Proposition

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and $X \in \mathbf{H}$ an $n$-truncated object.

Then

1. for $k \gt n$ we have for the [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] $\pi_k(A) = *$;

1. if (for $n \geq 0$) $\pi_n(A) = *$, then $X$ is in fact $(n-1)$-truncated. 

=--

This implies 

+-- {: .un_corollary}
###### Corollary

If $X \in \mathbf{H}$ is truncated at all (for any value), then it is $n$-truncated precisely if all categorical homotopy groups vanish $\pi_k(A) = *$ for $k \gt n$.

=--

**Notice.** If $A$ on the other hand is not truncated at all, then all its homotopy groups may be trivial and $A$ may still not be equivalent to the [[terminal object]]. This means that [[Whitehead's theorem]] may fail in a general [[(∞,1)-topos]] for untruncated objects. It holds, however, in [[hypercomplete (∞,1)-topos]]es.


## Examples

### Truncated morphisms

A morphism $f : X \to 0$ is 

* (-2)-truncated precisely if it is an 
  [[equivalence in a quasi-category|equivalence]];

* (-1)-truncated precisely if it is a 
  [[monomorphism in an (infinity,1)-category|monomorphism]].

### In $\infty Grpd$ and in $Top$ {#InInfGrpd}

An object in [[∞Grpd]] is $n$-truncated precisely if it is an [[n-groupoid]]. To some extent this is so by definition. Equivalently, an object in [[Top]] is $n$-truncated if it is (in the equivalence class of) a [[homotopy n-type]].

So we have for $n \in \mathbb{N}$ a [[reflective sub-(∞,1)-category]]

$$
  n Grpd \stackrel{\overset{\tau_{\leq n}}{\leftarrow}}{\hookrightarrow}
  \infty Grpd
  \,.
$$



+-- {: .un_lemma}
###### Observation

If we model the [[(∞,1)-category]] [[∞Grpd]] as the [[Kan complex]]-[[enriched category]]/fibrant [[simplicial category]] $KanCplx \subset $ [[sSet]] of [[Kan complex]]es, then the truncation adjunction

$$
  (\tau_{\leq n } \dashv i)
  :
  n Grpd \stackrel{\overset{\tau_{\leq n}}{\leftarrow}}{\hookrightarrow}
  \infty Grpd
  \,.
$$

is modeled by the [[simplicial skeleton|simplicial coskeleton]] [[sSet]]-enriched adjunction

$$
  (tr_{n+1} \dashv cosk_{n+1})
  :
  KanCplx_{n+1} \stackrel{\overset{tr_{n+1}}{\leftarrow}}{\underset{cosk_{n+1}}{\to}}
  KanCplx
  \,,
$$

where $KanCplx_{n+1}$ is the subcategory of $[\Delta^{op}_{\leq n+1}, Set]$ on those truncated simplicial sets that are truncations of Kan complexes, regarded as a Kan-complex-enriched category by the embedding via $cosk_{n+1}$.

=--

+-- {: .proof}
###### Proof


Notice that every [[Kan complex]] $X$ which is $n$-truncated is homotopy equivalent to one in the image of $cosk_{n+1}$, namely to $cosk_{n+1} tr_{n+1} X$, because by one of the [properties](http://ncatlab.org/nlab/show/simplicial+skeleton#Truncation) of $cosk_{n+1}$ we have that the unit 

$$
  X \to cosk_{n+1} tr_{n+1} X
$$

induces isomorphisms on homotopy groups $\pi_k$ for $k \leq n$.  

This shows that $KanCplx_{n+1}$ is indeed a full [[sub-(∞,1)-category]] of $KanCplx$ on $n$-truncated objects  

Moreover, by the fact discussed at <a href="http://ncatlab.org/nlab/show/adjoint+(infinity%2C1)-functor#SimplicialAndDerived">Simplicial and derived adjunctions</a> at [[adjoint (∞,1)-functor]] we have that the [[sSet]]-enriched adjunction $(tr_{n+1} \dashv cosk_{n+1})$ on $KanCplx$ indeed presents a pair of [[adjoint (∞,1)-functor]]s on [[∞Grpd]]. So $tr_{n+1} : KanCplx \to KanCplx$ indeed presents the [[left adjoint]] $\tau_{\leq} : \infty Grpd \to n Grpd$ to the inclusion $n Grpd \hookrightarrow \infty Grpd$.

=--



## References

The discussion of truncated objects in an $(\infty,1)$-category is in section 5.5.6 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The discussion of categorical [[homotopy groups in an (∞,1)-topos]] is in section 6.5.1.

A classical article that amplifies the expression of Postnikov towers in terms of [[coskeleton]]s is

* [[William Dwyer]], [[Dan Kan]], _An obstruction theory for diagrams of simplicial sets_ ([pdf](http://www.nd.edu/~wgd/Dvi/ObstructionTheoryForDiagrams.pdf))


[[!redirects truncated]]

[[!redirects n-truncated object of an (∞,1)-topos]]
[[!redirects n-truncated object in an (∞,1)-category]]
[[!redirects n-truncated object in an (∞,1)-topos]]
[[!redirects n-truncated object in an (infinity,1)-topos]]
[[!redirects n-truncated object of an (infinity,1)-topos]]

[[!redirects n-truncated object of an (∞,1)-category]]
[[!redirects n-truncated object in an (∞,1)-category]]
[[!redirects n-truncated object in an (infinity,1)-topos]]

[[!redirects truncated object of an (∞,1)-topos]]
[[!redirects truncated object in an (∞,1)-category]]
[[!redirects truncated object in an (∞,1)-topos]]
[[!redirects truncated object in an (infinity,1)-topos]]
[[!redirects truncated object of an (infinity,1)-topos]]

[[!redirects truncated object of an (∞,1)-category]]
[[!redirects truncated object in an (∞,1)-category]]
[[!redirects truncated object in an (infinity,1)-topos]]

[[!redirects n-truncated object of an (infinity,1)-topos]]


[[!redirects truncation]]
[[!redirects truncations]]