 +-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Model structures on chain complexes are [[model category]] structures on [[categories of chain complexes]] whose weak equivalences are [[quasi-isomorphisms]].  (There is  also a [[Hurewicz model structure on chain complexes]] whose weak equivalences are [[chain homotopy equivalences]].)


Via these model structures, all of the standard techniques in [[homological algebra]], such as [[injective resolutions]] and [[projective resolutions]], are special cases of constructions in [[homotopy theory]], such as [[cofibrant resolutions]] and [[fibrant resolutions]].

The existence of these model structures depends subtly on whether the chain complexes in question are bounded or not.

### In non-negative degree


[[chain complex|Chain complexes]] in non-negative degree in an [[abelian category]] $A$ are special in that they may be identified via the [[Dold-Kan correspondence]] as [[simplicial object]]s in $A$.

$$
  Ch_{\bullet \geq 0}(A) \simeq A^{\Delta^{op}}
  \,.
$$

Similarly, [[cochain complex|cochain complexes]] are identified with [[cosimplicial object]]s

$$
  Ch^{\bullet \geq 0}(A) \simeq A^{\Delta}
  \,.
$$

At least if $A$ is the category of [[abelian groups]], so that $A^{\Delta^{op}}$ is the category of abelian [[simplicial group]]s it inherits naturally a model category structure from the [[model structure on simplicial sets]], which [[presentable (∞,1)-category|presents]] the [[(∞,1)-category]] of [[∞-groupoid]]s.

The model structure on chain complexes transports this presentation  of the special $\infty$-groupoids given by abelian simplicial groups along the Dold-Kan correspondence to chain complexes.

Analogous statements apply to the category of unbounded chain complexes and the canonical [[stable (infinity,1)-category]] [[Spec]] of [[spectrum|spectra]].

This we discuss below in

* _[In non-negative degree](#CochainNonNeg)_

### For unbounded chain complexes

Model structures on unbounded (co)chain complexes can be understood as
presentations of [[spectrum objects]] in model structures of bounded (co)chain complexes.

See

* _[For unbounded chain complexes](#ForUnboundedChainComplexes)_


## Definitions

### In non-negative degree
 {#CochainNonNeg}

Let $C$ be an [[abelian category]].

Recall that by the dual [[Dold-Kan correspondence]] the category $C^\Delta$ of [[cosimplicial object]]s in $C$ is equivalent to the category $Ch^\bullet_+(C)$ of [[cochain complexes]] in non-negative degree. This means that we can transfer results discussed at [[model structure on cosimplicial objects]] to cochain complexes (see [Bousfield2003, section 4.4](http://arxiv.org/PS_cache/math/pdf/0312/0312531v1.pdf) for more).

#### The standard (Quillen) model structures
  {#StandardQuillenOnBounded}

Let $R$ be a [[ring]] and write $ \mathcal{A} \coloneqq R$[[Mod]] for its [[category]] of [[modules]].

We discuss the

* [Projective structure on chain complexes](#ProjectiveStructureOnChainComplexes)

* [Injective structure on cochain complexes](#InjectiveStructureOnCochainComplexes)

##### Projective structure on chain complexes
 {#ProjectiveStructureOnChainComplexes}

+-- {: .num_theorem #ProjectiveModelStructure}
###### Theorem

There is a [[model category]] structure on the [[category of chain complexes]]
$Ch_{\bullet \geq 0 }(\mathcal{A})$ (in non-negative degree) whose

* weak equivalences are [[quasi-isomorphisms]];

* fibrations are the morphisms that are [[epimorphisms]] in $R$[[Mod]] in each _[[positive number|positive]]_ degree;

* cofibrations are degreewise [[monomorphisms]] with degreewise [[projective object|projective]] [[cokernel]];

called the **projective model structure**.

=--

The projective model structure on $Ch_{\bullet \geq 0}$ is originally due to
([Quillen 67, II.4, pages II.4.11, II.4.12](#Quillen67)).
See also ([Goerss-Schemmerhorn 06, Theorem 1.5](#GoerssSchemmerhorn06), [Dungan 10, 2.4.2, proof in section 2.5](#Dungan10)).


##### Injective structure on cochain complexes
 {#InjectiveStructureOnCochainComplexes}

Dually

+-- {: .num_theorem #InjectiveModelStructure}
###### Theorem

There is a [[model category]] structure on non-negatively graded [[cochain complexes]]  $Ch^{\bullet \geq 0 }(\mathcal{A})$ whose

* weak equivalences are [[quasi-isomorphisms]];

* cofibrations are the morphisms that are [[monomorphisms]] in $R Mod$ in each _[[positive number|positive]]_ degree;

* fibrations are degreewise [[epimorphisms]] with [[injective object|injective]] [[kernel]],

called the **injective model structure**.

=--

([Dungan 10, Theorem 2.4.5](#Dungan10))


+-- {: .num_remark }
###### Remark

This means that a chain complex $C_\bullet \in Ch_{\bullet}(\mathcal{A})$ is a [[cofibrant object]] in the projective model structure, theorem \ref{ProjectiveModelStructure}, precisely if it consists of [[projective modules]]. Accordingly, a [[cofibrant resolution]] in the projective model structure is precisely what in [[homological algebra]] is called a _[[projective resolution]]_. Dually for [[fibrant resolutions]] in the injective model structure, theorem \ref{InjectiveModelStructure}, and [[injective resolutions]] in homological algebra.

This way the traditional definition of [[derived functor in homological algebra]] relates to the general construction of [[derived functors]] in [[model category]] theory. See there for more details. Similar comments apply to the various other model structures below.


=--



#### Resolution model structures
  {#GeneralResults}

There are _resolution model structures_ on cosimplicial objects in a model category, due to ([DwyerKanStover](#DwyerKanStover)), reviewed in ([Bousfield](#Bousfield))



+-- {: .num_defn}
###### Definition

(...)

=--

+-- {: .num_theorem}
###### Theorem

Let $A$ be an [[abelian category]] and let $\mathcal{G} \in Obj(A)$ be a [[class]] of objects, such that $A$ has enough $\mathcal{G}$-[[injective object]]s.

Then there is a model category structure on non-negatively graded cochain complexes $Ch^{\bullet \geq 0}(A)_{\mathcal{G}}$ whose

* weak equivalences are maps $f : X \to Y$ such that for each $K \in A$ the induced map $A(Y,K) \to A(X,K)$ is a [[quasi-isomorphism]] of chain complexes of abelian groups;

* $f$ is a cofibration if it is $\mathcal{G}$-monic in positive degree;

* $f$ is a fibration if it is degreewise a [[split epimorphism]] with degreewise $\mathcal{G}$-injective kernel.

=--

See [Bousfield2003, section 4.4](http://arxiv.org/PS_cache/math/pdf/0312/0312531v1.pdf).

If $A$ has enough [[injective object]]s and $\mathcal{G}$ is the class of all of them, this reproduces the
[standard Quillen model structure](#StandardQuillenOnBounded) discussed above:

+-- {: .num_cor}
###### Corollary

Let $A$ be an [[abelian category]] with enough [[injective object]]s. Then there is a model category structure on non-negatively graded cochain complexes $Ch^{\geq 0}(A)$ whose

* weak equivalences are the [[quasi-isomorphism]]s;

* fibrations are the morphisms that are [[epimorphism]]s with injective [[kernel]] in each degree;

* cofibrations are the morphisms which are [[monomorphism]]s in $A$ in each _positive_ degree.

=--

If we take $\mathcal{G}$ to be the class of all objects of $A$ this gives the following structure.

+-- {: .num_cor}
###### Corollary

There is a model structure on $Ch^{\bullet\geq 0}(A)_{tot}$ whose

* weak equivalences are cochain [[homotopy equivalence]]s;

* fibrations are the morphisms that are degreewise [[split epimorphism]]s and whose [[kernel]]s are [[injective object]]s;

* cofibration are the morphisms that are in positive degree [[monomorphism]]s.

=--

+-- {: .num_example}
###### Example

If $C = $ [[Vect]] is a category of [[vector space]]s over some [[field]], we have that every epi/mono splits and that every [[quasi-isomorphism]] is a homotopy equivalence.  Moreover, in this case every chain complex is quasi-isomorphic to its [[homology]] (regarded as a chain complex with zero differentials).

This is the model structure which induces the [[transferred model structure|transferred]] [[model structure on dg-algebras]] over a [[field]] that is used in [[rational homotopy theory]].

=--

#### Projective model structure on connective cochain complexes 
  {#CochainNonNegProj}

We discuss a model structure on connective cochain complexes of abelian groups in which the fibrations are the degreewise epis. This follows an analogous proof in ([Jardine 97](model+structure+on+dg-algebras#Jardine97)).


+-- {: .num_theorem #ProjectiveModelStructureOnConnectiveCochainComplexes}
###### Theorem
**(projective model structure on connective cochain complexs )**

The category $Ch^{\bullet \geq 0}(Ab)$ of non-negatively graded cochain complexes of [[abelian groups]] becomes a [[model category]] with

* fibrations the degreewise surjections;

* weak equivalences the [[quasi-isomorphism]]s.

Moreover this is a [[simplicial model category]]-structure
with respect to the canonical structure of an [[sSet]]-[[enriched category]]
induced from the dual [[Dold-Kan correspondence|Dold-Kan equivalence]]
$Ch^\bullet_+(Ab) \simeq Ab^\Delta$ by the fact that $Ab^\Delta$  is a [[category of cosimplicial objects]] (see there) in a category with all limits and colimits.

=--

The first part of this theorem is claimed, without proof, in [Castiglioni-Cortinas 03, Def. 4.7](#CastiglioniCortinas03).

+-- {: .proof}
###### Proof

We spell out a proof of the model structure below in a sequence of
lemmas. The proof that this is a simplicial model category is
at [[model structure on cosimplicial abelian groups]].

=--

We record a detailed proof of the model structure on $Ch^{\bullet \geq 0}(Ab)$ with fibrations the degreewise surjections, following the appendix of ([Stel 10](#Stel)).


As usual, for $n \in \mathbb{N}$ write $\mathbb{Z}[n]$ for the complex concentrated on the additive group of [[integer]]s in degree $n$, and for $n \geq 1$  write $\mathbb{Z}[n-1,n]$ for the cochain complex $(0 \to \cdots 0 \to \mathbb{Z} \stackrel{Id}{\to} \mathbb{Z} \to 0 \cdots)$ with the two copies of $\mathbb{Z}$ in degree $n-1$ and $n$.


For $n = 0$ let $\mathbb{Z}[-1,0] = 0$, for convenience.







+-- {: .num_lemma #ProjStructGenCofibs}
###### Lemma


For all $n \in \mathbb{N}$ the canonical maps $0 \to \mathbb{Z}[n]$ and $\mathbb{Z}[n] \to \mathbb{Z}[n-1,n]$ are cofibrations, in that they  have the [[left lifting property]] against acyclic fibrations.

=--

+-- {: .proof}
###### Proof


Let $p : A \stackrel{\simeq}{\to} B$ be degreewise surjective and an isomorphism on cohomology.

First consider $\mathbb{Z}[0]\to \mathbb{Z}[-1,0] = 0$. We need to construct lifts

$$
  \array{
     \mathbb{Z}[0] &\stackrel{f}{\to}& A
     \\
     \downarrow &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{p}
     \\
     0 &\stackrel{}{\to}& B
  }
  \,.
$$

Since $p(f_0(1)) = 0$ we have by using that $p$ is a quasi-iso that $f_0(1) = 0 \; mod\; im d_A$. But in degree 0 this means that $f_0(1) = 0$. And so the unique possible lift in the above diagram does exist.


Consider now $\mathbb{Z}[n] \to \mathbb{Z}[n-1,n]$ for $n \geq 1$. We need to construct a lift in all diagrams of the form

$$
  \array{
     \mathbb{Z}[n] &\stackrel{f}{\to}& A
     \\
     \downarrow &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{p}
     \\
     \mathbb{Z}[n-1,n] &\stackrel{g}{\to}& B
  }
  \,.
$$

Such a lift is equivalently an element $\sigma \in A_{n-1}$ such that

* $d_A \sigma = f_n(1)$

* $p_{n-1}(\sigma) = g_{n-1}(1)$.

Since $p$ is a quasi-isomorphism, and since it takes the closed element $f_n(1) \in A_n$ to the exact element $p_n(f_n(1)) = d_B g_{n-1}(1)$ it follows that $f_n(1)$ itself must be exact in that there is $z \in A_{n-1}$ with $d_A z = f_n(1)$. Pick such.

So then $d_B ( p(z) - g_{n-1}(1) ) = 0$ and again using that $p$ is a quasi-isomorphism this means that there must be a closed $a \in A_{n-1}$ such that $p(a) = p(z)- g_{n-1}(1) + d_B b$ for some $b \in B_{n-2}$. Choose such $a$ and $b$.

Since $p$ is degreewise onto, there is $a'$ with $p(a') = b$. Choosing this the above becomes $p(a) = p(z) - g_{n-1}(1) + p(d_A a')$.

Set then

$$
  \sigma := z - a + d_A a'
  \,.
$$

It follows with the above that this satisfies the two conditions on $\sigma$:

$$
  \begin{aligned}
     d_A \sigma &= d_A z - d_A a + d_A d_A a'
     \\
     & =
     d_A z
     \\
      & = f_n(1)
  \end{aligned}
$$

$$
  \begin{aligned}
     p( \sigma ) &=  p(z) - p(a) + p(d_A a')
     \\
     & = g_{(n-1)}(1)
  \end{aligned}
  \,.
$$

Finally consider $0 \to \mathbb{Z}[n]$ for all $n$. We need to produce lifts in

$$
  \array{
     0 &\stackrel{}{\to}& A
     \\
     \downarrow &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{p}
     \\
     \mathbb{Z}[n] &\stackrel{g}{\to}& B
  }
  \,.
$$

Such a lift is a choice of element $\sigma \in A_n$ such that

* $d_A \sigma = 0$;

* $p(\sigma) = g_n(1)$;

Since $g_n(1)$ is closed and $p$ a surjective quasi-isomorphism, we may find a closed $a \in A_n$ and an $a' \in A_{n-1}$ such that
$p (a) = g_{n}(1) + d_B(p(a'))$. Set then

$$
  \sigma := a - d_A a'
  \,.
$$

=--

+-- {: .num_lemma}
###### Lemma

For all $n \in \mathbb{N}$, the morphism $0 \to \mathbb{Z}[n-1,n]$
are acyclic cofibrations, in that they have the [[left lifting property]] again all degreewise surjections.

=--

+-- {: .proof}
###### Proof

For $n = 0$ this is trivial. For $n \geq 1$ a diagram

$$
  \array{
    0 &\to& A
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    \mathbb{Z}[n-1,n] &\stackrel{g}{\to}& B
  }
$$

is equivalently just any element $g_{n-1}(1) \in B$ and
a lift $\sigma$ accordingly just any element $\sigma \in A$
with $p(\sigma) = g_{n-1}(1)$. Such exists because $p$ is degreewise
surjctive by assumption.

=--


+-- {: .num_lemma #ProjStructCharAcyclicFibrations}
###### Lemma


A morphism $f : A \to B$ is an acyclic fibration precisely if it has
the [[right lifting property]] against $0 \to \mathbb{Z}[n]$ and
$\mathbb{Z}[n] \to \mathbb{Z}[n-1,n]$ for all $n$.

=--

+-- {: .proof}
###### Proof


By the above lemmas, it remains to show only one direction:
if $f$ has the RLP, then it is an acyclic fibration.

So assume $f$ has the RLP. Then from the existence of the lifts

$$
  \array{
     0 &\to& A
     \\
     \downarrow && \downarrow
     \\
     \mathbb{Z}[n] &\stackrel{g}{\to}& B
  }
$$

one deduces that $f$ is degreewise surjective on closed elements.
In particular this means it is surjective in cohomology.

With that, it follows from the existence of all the lifts

$$
  \array{
     \mathbb{Z}[n] &\stackrel{f}{\to}& A
     \\
     \downarrow &{}^{\mathllap{\sigma}}\nearrow& \downarrow
     \\
     \mathbb{Z}[n-1,n] &\stackrel{g}{\to}& B
  }
$$

for $f$ a lift of the closed element $g_n(1)$ that $f$ is
degreewise surjective on all elements.

Moreover, these lifts say that if $f_n(1)$ is any closed element such that
under $p$ it becomes exact ($d_B g_{n-1}(1) = p(f_n(1))$), then it
must already be exact itself ($d_A \sigma_{n-1}(1) = f_n(1)$). Hence
$f$ is also injective on cohomology and hence by the above is
an isomorphism on cohomology.

=--

+-- {: .num_lemma #ProjStrucFactAxiomI}
###### Lemma


Every morphism $f : A \to B$ can be factored as
a morphism with left lifting property against all
fibrations followed by a fibration.

=--

+-- {: .proof}
###### Proof

Apply the [[small object argument]]-reasoning to the
maps in $ J = \{0 \to \mathbb{Z}[n-1,n]\}$.

Since for $n \in \mathbb{N}$ a morphism $\mathbb{Z}[n,n+1]\to B$
corresponds to an element $b \in B_n$. From the commuting
diagram

$$
  \array{
    0 &\to& A
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    \coprod_{{n \in \mathbb{n}} \atop {b \in B_n}}
    \mathbb{Z}[n,n+1] &\stackrel{}{\to}&
    B
  }
$$

one obtains a factorization through its [[pushout]]

$$
  \array{
     && A
     \\
       &{}^{\mathllap{j}}\swarrow& \downarrow
     \\
     A \coprod \coprod_{{n \in \mathbb{n}} \atop {b \in B_n}}
     \mathbb{Z}[n,n+1]
     && \downarrow^{\mathrlap{f}}
     \\
     &\searrow_{p}& \downarrow
     \\
     && B
  }
  \,.
$$

Since $j$ is the pushout of an acyclic cofibration, it is
itself an acyclic cofibration. Moreover, since the cohomology
of $\coprod_{{n \in \mathbb{n}} \atop {b \in B_n}} \mathbb{Z}[n,n+1]$
clearly vanishes, it is a quasi-isomorphism.

The map $p$ is manifestly degreewise
onto and hence a fibration.

=--

+-- {: .num_lemma}
###### Lemma

Every morphism $f : A \to B$ may be factored as a
cofibration followed by an acyclic fibration.

=--

+-- {: .proof}
###### Proof

By a  [lemma above](#ProjStructCharAcyclicFibrations) acyclic fibrations
are precisely the maps with the right lifting property against
morphisms in $I = \{0 \to \mathbb{Z}[n], \mathbb{Z}[n]\to \mathbb{Z}[n-1,n]\}$, which by the [first lemma above](#ProjStructGenCofibs)
are cofibrations.

The claim then follows again from the [[small object argument]]
apllied to $I$.

=--

+-- {: .num_lemma}
###### Lemma

A morphism $f : A \to B$ that is both a cofibration
(:= LLP against acyclic fibrations ) and a weak equivalence
has the left lifting property against all fibrations.

=--

+-- {: .proof}
###### Proof

By a standard argument, this follows from the
factorization lemma proven [above](#ProjStrucFactAxiomI),
which says that we may find a factorization

$$
  \array{
    A &\stackrel{j}{\to}& \hat B
    \\
    & {}_{\mathllap{f}}\searrow & \downarrow^{\mathrlap{p}}
    \\
    && B
  }
$$

with $j$ having LLP against all fibrations and being
a weak equivalence, and $p$ a fibration. Since $f$ is
assumed to be a weak equivalence, it follows that
$p$ is an acyclic fibration. By definition of cofibrations
as $LLP(Fib \cap W)$ this implies that we have the lift in

$$
  \array{
    A &\stackrel{j}{\to}& \hat B
    \\
    {}^{\mathllap{f}}\downarrow
    &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    B &\stackrel{Id}{\to}& B
  }
  \,.
$$

Equivalently redrawing this as

$$
  \array{
    A &\stackrel{Id}{\to}& A &\stackrel{Id}{\to}& A
    \\
    {}^{\mathllap{f}}\downarrow && {}^{\mathllap{p}}
    \downarrow && {}^{\mathllap{i}}\downarrow
    \\
    B &\stackrel{\sigma}{\to}&
    \hat B
    & \stackrel{p}{\to} &
    B
  }
$$

makes manifest that this exhibts $f$ as a retract of $j$
and as such inherits its left lefting properties.

=--

This series of lemmas establishes the claimed model structure
on $Ch^\bullet_+(Ab)$.


### In unbounded degree
  {#OnUnbounded}

There are several approaches to defining model structures on the [[category of unbounded chain complexes]] $Ch(\mathcal{A})$ -


#### Standard projective model structure on unbounded chain complexes
 {#ProjectiveModelStructureOnUnboundedChainComplexes}

+-- {: .num_prop #ProjModelStructureOnUnbounded}
###### Proposition

For $k$ a [[commutative ring]] the [[category of unbounded chain complexes]] of $k$-[[modules]] $Ch_\bullet(k Mod)$ carries the structure of a

* [[proper model category|proper]]

* [[cofibrantly generated model category|cofibrantly generated]]

[[model category]] with

* weak equivalences the [[quasi-isomorphisms]]

* fibrations the (degreewise) [[epimorphisms]].

The cofibrations are all in particular degreewise split injections, but not every degreewise split injection is a cofibration.

=--

See ([Hovey-Palmieri-Strickland 97, remark after theorem 9.3.1](#HoveyPalmieriStrickland97), [Schwede-Shipley 98, p. 7](#SchwedeShipley98)).

+-- {: .num_prop }
###### Proposition

The [[category of simplicial objects]] $(Ch_\bullet(k Mod))^{\Delta^{op}}$ in the [[category of unbounded chain complexes]]
carries the structure of a [[simplicial model category]] whose

* weak equivalences are the maps that are [[quasi-isomorphisms]] under the [[total chain complex]] functor.

=--

This is ([Rezk-Schwede-Shipley 01, cor 4.6](#RezkSchwedeShipley01)), using the methods discussed at _[simplicial model category -- Simplicial Quillen equivalent models](simplicial+model+category#SimpEquivMods)_.

Below this model structure is recovered as one example of the [Christensen-Hovey projective class construction](#InUnboundedDegreeGeneralResults), as example \ref{CategoricalProjectiveClasses}.


#### Christensen-Hovey model structures using projective classes
 {#InUnboundedDegreeGeneralResults}

Let $\mathcal{A}$ be an [[abelian category]] with all [[limit]]s and
[[colimit]]s.

[Christensen-Hovey](#ChristensenHovey) construct a family of model category structures on $Ch(\mathcal{A})$ parameterized by a choice of _projective class_ .
The cofibrations, fibrations and weak equivalences all depend on the projective class.

+-- {: .num_defn #ProjectiveClass}
###### Definition

A **projective class** on $\mathcal{A}$ is a collection $\mathcal{P} \subset ob \mathcal{A}$ of [[object]]s and a collection $\mathcal{E} \subset mor \mathcal{A}$ of [[morphism]]s, such that

* $\mathcal{E}$ is precisely the collection of $\mathcal{P}$-epic maps;

* $\mathcal{P}$ is precisely the collection of all objects $P$ such that each map in $\mathcal{E}$ is $P$-epic;

* for each object $X$ in $\mathcal{A}$, there is a morphism $P \to X$ in
  $\mathcal{E}$ with $P$ in $\mathcal{P}$.

=--


+-- {: .num_example #TrivialProjectiveClass}
###### Example

Taking $\mathcal{P} := ob \mathcal{A}$ to be the class of _all_ objects yields a projective class -- called the _trivial projective class_ . The corresponding morphisms are the class $\mathcal{E}$ of all [[split epimorphism]]s in $\mathcal{A}$.

=--


+-- {: .num_example #PullbackProjectiveClass}
###### Example

Let $R$ be a [[ring]] and $\mathcal{A} = $ $R$-[[Mod]] be the category of $R$-[[module]]s. Choosing $\mathcal{P}$ to be the class of all summands of [[direct sums]] of [[finitely presented]] modules yields a projective class.

=--

+-- {: .num_example}
###### Example

Given a pair of [[adjoint functors]]

$$
  (F \dashv U) : \mathcal{A} \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} \mathcal{B}
$$

between [[abelian categories]] and given $(\mathcal{P}, \mathcal{E})$ a projective class in $\mathcal{B}$ then its **pullback projective class** $(U * \mathcal{P}, U^* \mathcal{E})$ along $U$ on $\mathcal{A}$ is defined by

* $U^* \mathcal{P} := \{retracts\;of\; F P | P \in \mathcal{P}\}$


=--

+-- {: .num_theorem #ModelStructureOnUnboundedFromProjectiveClass}
###### Definition/Theorem

Given a projective class $\mathcal{P}$ in $\mathcal{A}$ (def. \ref{ProjectiveClass}), call a morphism $f \in Ch(\mathcal{A})$

* a fibration if $\mathcal{A}(P,f)$ is a surjection in [[Ab]] for all $P \in \mathcal{P}$;

* a weak equivalence if $\mathcal{A}(P,f)$ is a [[quasi-isomorphism]] in $Ch(Ab)$
  for all $P \in \mathcal{P}$.

Then this constitutes a [[model category]] structure precisely if cofibrant [[resolution]]s exist, which is the case in particular if

1. $\mathcal{P}$ is the pullback projective class (def. \ref{PullbackProjectiveClass}) of a trivial projective class (def. \ref{TrivialProjectiveClass}) along a functor $U$ that preserves countable [[direct sum]]s;

1. [^fine]

[^fine]:Some one finish this part.

When the structure exists, it is a [[proper model category]].


=--

This is theorem 2.2 in [Christensen-Hovey](#ChristensenHovey).

We shall write $Ch(\mathcal{A})_{\mathcal{P}}$ for this model category structure.

#### Examples
 {#ExamplesOfStructuresOnUnboundedComplexes}

We list some examples for the model structures on chain complexes in unbounded degree discussed [above](#InUnboundedDegreeGeneralResults).

Let $R$ be an associative ring and $\mathcal{A} = R$[[Mod]].

* [Categorical projective class structure](#CategoricalProjectiveClass)

* [Pure projective class structure](#PureProjectiveClass)


##### Categorical projective class structure
 {#CategoricalProjectiveClass}

+-- {: .num_example #CategoricalProjectiveClasses}
###### Example

The **categorical projective class** on $\mathcal{A}$ is the projective class (def. \ref{ProjectiveClass}) with $\mathcal{P}$ the class of [[direct sum]]mands of free modules. The $\mathcal{P}$-model structure on $Ch(\mathcal{A})$ has

* as fibrations the degreewise surjections.

So this reproduces the standard projective model structure from prop. \ref{ProjModelStructureOnUnbounded}.

=--

##### Pure projective class structure
 {#PureProjectiveClass}

+-- {: .num_example }
###### Example


The **pure projective class** on $\mathcal{A}$ has as $\mathcal{P}$ summands of sums of finitely presented modules. Fibrations in the corresponding model structure are the maps that are degreewise those epimorphisms that appear in $\mathcal{P}$-exact sequences.

=--

#### Gillespie's approach using cotorsion pairs

[Hovey](#HoveyOverview) has shown that, roughly speaking, [[model structures]] on [[abelian categories]] correspond to cotorsion pairs.  See [[abelian model structure]].

[Gillespie](#HoveyOverview) shows that if $\mathcal{A}$ is a [[Grothendieck abelian category]], then a [[cotorsion pair]] induces an [[abelian model structure]] on the category of (unbounded) complexes $Ch(\mathcal{A})$, where the [[weak equivalences]] are [[quasi-isomorphisms]].

+-- {: .num_theorem}
###### Theorem
Let $\mathcal{A}$ be a [[Grothendieck abelian category]].  Suppose $(\mathcal{D}, \mathcal{E})$ is a hereditary [[cotorsion pair]] that is cogenerated by a set, such that $\mathcal{D}$ is a [[Kaplansky class]] on $\mathcal{A}$ and $\mathcal{A}$ has enough $\mathcal{D}$-objects.

Then there is an [[abelian model structure]] on the category of complexes $Ch(\mathcal{A})$ such that the trivial objects are the acyclic complexes.
=--

Gillespie uses this result to get a **[[monoidal model category|monoidal]]** [[model structure]] on $Ch(Qcoh(X))$, the category of complexes of [[quasi-coherent sheaves]] on a [[quasi-compact scheme|quasi-compact]] [[separated scheme|separated]] [[scheme]] $X$.  This gives a better understanding of the [[derived category of quasi-coherent sheaves]] $D(Qcoh(X))$, and in particular gives immediately the [[derived functor]] $\cdot \otimes^{\mathbf{L}} \cdot$ (which is usually a problem due to sheaves not having enough projectives).

#### Cisinski-Deglise approach using descent structures

A third approach is due to [Cisinski-Deglise](#CisinskiDeglise).

Let $\mathcal{A}$ be a [[Grothendieck abelian category]].  We will define a notion of **descent structures** on $\mathcal{A}$.

+-- {: .num_defn}
###### Definition
For each object $E$ of $\mathcal{A}$ and integer $n \in \mathbf{Z}$, we define the complexes $S^n E$ and $D^n E$ as follows: let $(S^n E)^n = E$ in degree $n$ and 0 elsewhere; and let $(D^n E)^n = (D^n E)^{n+1} = E$ and 0 elsewhere.  There are canonical morphisms $S^{n+1} E \hookrightarrow D^n E$.
=--

+-- {: .num_defn}
###### Definition
Let $\mathcal{G}$ be an essentially small set of objects of $\mathcal{A}$.  A morphism in $Ch(\mathcal{A})$ is called a **$\mathcal{G}$-cofibration** if it is contained in the smallest class of morphisms in $Ch(\mathcal{A})$ that is closed under [[pushouts]], [[transfinite compositions]] and [[retracts]], generated by the inclusions $S^{n+1} E \to D^n E$, for any integer $n$ and any $E \in \mathcal{G}$.  A complex $C$ in $Ch(\mathcal{A})$ is called **$\mathcal{G}$-cofibrant** if the morphism $0 \to C$ is a $\mathcal{G}$-cofibration.
=--

+-- {: .num_defn}
###### Definition
A [[chain complex]] $C$ in $Ch(\mathcal{A})$ is called **$\mathcal{G}$-local** if for all $E \in \mathcal{G}$ and $n \in \mathbf{Z}$, the canonical morphism
$$ Hom_{\mathbf{K}(\mathcal{A})}(E[n], C) \to Hom_{\mathbf{D}(\mathcal{A})}(E[n], C) $$
is an isomorphism.  Here $\mathbf{K}(\mathcal{A})$ and $\mathbf{D}(\mathcal{A})$ denote the [[homotopy category of complexes]] and the [[derived category]] of $\mathcal{A}$, respectively.
=--

+-- {: .num_defn}
###### Definition
Let $\mathcal{H}$ be a small family of complexes in $Ch(\mathcal{A})$.  An complex $C$ in $Ch(\mathcal{A})$ is called **$\mathcal{H}$-flasque** if for all $n \in \mathbf{Z}$ and $H \in \mathcal{H}$,
$$ Hom_{\mathbf{K}(\mathcal{A})}(H, C[n]) = 0. $$
=--

Finally we define:

+-- {: .num_defn}
###### Definition
A **descent structure** on $\mathcal{A}$ is a pair $(\mathcal{G},\mathcal{H})$, where $\mathcal{G}$ is an essentially small set of generators of $\mathcal{A}$, and $\mathcal{H}$ is an essentially small set of $\mathcal{G}$-cofibrant acyclic complexes such that any $\mathcal{H}$-flasque complex is $\mathcal{G}$-local.
=--

Now one defines a [[model structure]] associated to any such descent structure.

+-- {: .num_theorem}
###### Theorem
Let $(\mathcal{G},\mathcal{H})$ be a descent structure on the [[Grothendieck abelian category]] $\mathcal{A}$.  There is a [[proper model category|proper]] [[cellular model category|cellular]] [[model structure]] on the category $Ch(\mathcal{A})$, where the [[weak equivalences]] are [[quasi-isomorphisms]] of [[complexes]], and [[cofibrations]] are $\mathcal{G}$-cofibrations.

Also, a complex $C$ in $Ch(\mathcal{A})$ is [[fibrant]] if and only if it is $\mathcal{H}$-flasque or equivalently $\mathcal{G}$-local.
=--

We call this the **$\mathcal{G}$-model structure** on $Ch(\mathcal{A})$.  As in Gillespie's approach we can sometimes get a [[monoidal model structure]].  We refer to [Cisinski-Deglise](#CisinskiDeglise) for the notion of a **weakly flat** descent structure.

+-- {: .num_theorem}
###### Theorem
Suppose $(\mathcal{G}, \mathcal{H})$ is a _weakly flat_ descent structure on $\mathcal{A}$.  Then the $\mathcal{G}$-model structure is further [[monoidal model category|monoidal]].
=--

## Properties

### Left/right exact functors and Quillen adjunctions {#ExactFuncsAndQuillenFuncs}

Let $\mathcal{A}$ and $\mathcal{B}$ be [[abelian categories]]. Let the [[categories of chain complexes]] $Ch_\bullet^+(\mathcal{A})$ and $Ch_\bullet^+(\mathcal{B})$ be equipped with the model structure described [above](#GeneralResults) where fibrations are the degreewise [[split monomorphism]]s with [[injective object|injective]] [[kernel]]s.

+-- {: .num_prop}
###### Proposition

If

$$
  (L \dashv R) : \mathcal{A} \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} \mathcal{B}
$$

is a pair of [[adjoint functor]]s where $L$ preserves [[monomorphism]]s, then

$$
  (Ch_\bullet^+(L)
    \dashv
   Ch_\bullet(R) : Ch_\bullet^+(\mathcal{A})
   \stackrel{\overset{Ch_\bullet^+(L)}{\leftarrow}}{\underset{Ch_\bullet(R)}{\to}}
   Ch_\bullet^+(\mathcal{B})
$$

is a [[Quillen adjunction]].

=--


+-- {: .proof}
###### Proof

Every functor preserves split epimorphism. Being a [[right adjoint]] in particular $R$ is a [[left exact functor]] and hence preserves kernels. Using the characterization of [[injective object]]s as those $I$ for which $Hom(-,I)$ sends monomorphisms to epimorphisms, we have that $R$ preserves injectives because $L$ preserves monomorphisms, by the adjunction isomorphism.

Hence $L$ preserves all cofibrations and $R$ all fibrations.

=--

### Cofibrant generation

+-- {: .num_prop}
###### Proposition

The injective model structure on $Ch^{\geq 0}(R Mod)$ (from theorem \ref{InjectiveModelStructure}) is a [[cofibrantly generated model category]].

=--

This appears for instance as [Hovey, theorem 2.3.13](#Hovey), where it is stated for unbounded (in both directions) chain complexes.

For results on model structures on chain complexes that are provably not cofibrantly generated see section 5.4 of [Christensen, Hovey](#ChristensenHovey).



### Inclusion into simplicial objects

Let $\mathcal{A} = $ [[Ab]] be the category of [[abelian group]]s. The [[Dold-Kan correspondence]] provides a [[Quillen equivalence]]

$$
  (N \dashv \Gamma) : Ch_\bullet^+ \stackrel{\overset{N}{\leftarrow}}{\underset{\Gamma}{\to}}
  sAb
$$

between the projective model structure on connective chain complexes and the [[model structure on simplicial T-algebras|model structure on simplicial abelian groups]]. This in turns sits as a [[transferred model structure]] along the [[forgetful functor]] over the [[model structure on simplicial sets]]

$$
  (F \dashv U) : sAb \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  sSet
  \,.
$$

The combined Quillen adjunction

$$
  (N F  \dashv U \Gamma) : Ch_\bullet \stackrel{\leftarrow}{\to} sSet
$$

prolongs to a Quillen adjunction on the projective [[model structure on simplicial presheaves]] on any [[site]] $C$ , which we denote by the same symbols

$$
  (N F  \dashv U \Gamma) : [C,Ch_\bullet]_{proj} \stackrel{\leftarrow}{\to} [C, sSet]_{proj}
  \,.
$$

With due care this descends to the [[local model structure on simplicial presheaves]] which [[presentable (infinity,1)-category|presents]] the [[(∞,1)-sheaf (∞,1)-topos]] on $C$. Then the above Quillen adjunction serves to embed [[abelian sheaf cohomology]] on $C$ into the larger context of [[nonabelian cohomology]] on $C$. See [[cohomology]] for more on this.

### Cofibrations

We discuss cofibrations in the [model structures on unbounded complexes](#OnUnbounded).

Let $\mathcal{P}$ be a given projective class on an abelian category $\mathcal{A}$, def. \ref{ProjectiveClass} and write $Ch(\mathcal{A})_{\mathcal{P}}$ for the corresponding model structure on unbounded chain complexes, theorem \ref{ModelStructureOnUnboundedFromProjectiveClass}.


+-- {: .num_prop}
###### Proposition

An object $C \in Ch(\mathcal{A})_{\mathcal{P}}$ is cofibrant precisely if

1. in each degree $n \in \mathbb{Z}$ the object $C_n$ is relatively projective in $\mathcal{A}$;

1. every morphism from $C$ into a weakly  contractible complex in $Ch(\mathcal{A})_{\mathcal{P}}$ is [[chain homotopy|chain homotopic]] to the [[zero morphism]].

=--

This appears as ([ChristensenHovey, lemma 2.4](#ChristensenHovey)).

+-- {: .num_prop}
###### Proposition

A morphism $f : A \to B$ in $Ch(\mathcal{A})_{\mathcal{P}}$ is a cofibration precisely if it is degreewise

1. a [[split monomorphism]];

1. with cofibrant [[cokernel]].

=--

This appears as ([ChristensenHovey, prop. 2.5](#ChristensenHovey)).

### Relation to module spectra

For $R$ any ring, there is the [[Eilenberg-MacLane spectrum]] $H R$. This is an [[algebra spectrum]], hence there is a notion of $H R$-[[module spectra]]. These are [[Quillen equivalence|Quillen equivalent]] to chain complexes of $R$-modules. See [[module spectrum]] for details.




## Related concepts

* [[model structure on equivariant chain complexes]]

* [[model structure on chain complexes of super vector spaces]]

* [[model structure on dg-modules]]

* [[model structure on dg-algebras]]

* [[stable model category]]

* [[(∞,1)-category of chain complexes]]


## References
 {#References}

### For bounded chain complexes

The projective model structure on connective chain complexes (Theorem \ref{ProjectiveModelStructure}) is due to 

* {#Quillen67} [[Daniel Quillen]], Section II.4 item 5 in: _[[Homotopical Algebra]]_, Lecture Notes in Mathematics 43, Springer 1967([doi:10.1007/BFb0097438](https://doi.org/10.1007/BFb0097438))

see also

* {#GoerssSchemmerhorn06} [[Paul Goerss]], [[Kirsten Schemmerhorn]], Theorem 1.5 in: _Model categories and simplicial methods_, Notes from lectures given at the University of Chicago, August 2004, in: _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007([arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537), [doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))

The projective model structure on connective *co*chain complexes (Theorem \ref{ProjectiveModelStructureOnConnectiveCochainComplexes}) is claimed, without proof, in:

* {#Hess06} [[Kathryn Hess]], p. 6 of _Rational homotopy theory: a brief introduction_, contribution to _[Summer School on Interactions between Homotopy Theory and Algebra](https://jdc.math.uwo.ca/summerschool/)_, University of Chicago, July 26-August 6, 2004, Chicago ([arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626)), chapter in Luchezar Lavramov, [[Dan Christensen]], [[William Dwyer]], [[Michael Mandell]], [[Brooke Shipley]] (eds.), _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007 ([doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))

* {#CastiglioniCortinas03} J. L. Castiglioni, G. Corti&#241;as, Def. 4.7 of: _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_, J. Pure Appl. Algebra  191  (2004),  no. 1-2, 119--142, ([arXiv:math.KT/0306289](http://arxiv.org/abs/math/0306289), [doi:10.1016/j.jpaa.2003.11.009](https://doi.org/10.1016/j.jpaa.2003.11.009))




Of course the description of model categories of chain complexes as ([[presentable (infinity,1)-category|presentations]] of) special cases of (stable) $(\infty,1)$-categories is exactly opposite to the historical development of these ideas.

While the homotopical treatment of weak equivalences of chain complexes ([[quasi-isomorphism]]s) in [[homological algebra]] is at the beginning of all studies of higher categories and a "folk theorem" ever since

* [[Andre Joyal]], Letter to Alexander Grothendieck. April 11, 1984

it seems that the injective model structure on chain complexes has been made fully explicit in print only in proposition 3.13 of

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math/0102087), [pdf](http://arxiv.org/PS_cache/math/pdf/0102/0102087v1.pdf))

(at least according to the remark below that).

The projective model structure is discussed after that in

* [[Mark Hovey]], _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. 353, 6 ([pdf](http://www.mathaware.org/tran/2001-353-06/S0002-9947-01-02721-0/S0002-9947-01-02721-0.pdf))

An explicit proof of the injective model structure with monos in positive degree is spelled out in

* {#Dungan10} [[Gregory Dungan]], _Review of model categories_, 2010 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.696.123&rep=rep1&type=pdf), [[DunganModelCategories.pdf:file]])

An explicit proof of the model structure on cochain complexes of abelian group with fibrations the degreewise surjections is recorded in the appendix of

* [[Herman Stel]], _[[schreiber:master thesis Stel|∞-Stacks and their Function Algebras -- with Applications to ∞-Lie Theory]]_ (2010)
{#Stel}

The resolution model structures on cofibrant objects go back to

* [[William Dwyer]], [[Dan Kan]], C. Stover, _An $E_2$ model category structure for pointed simplicial spaces_, J. Pure and Applied Algebra 90 (1993) 137&#8211;152
{#DwyerKanStover}

and are reviewed in

* A. Bousfield, _Cosimplicial resolutions and homotopy spectral sequences in model categories_ Geometry and Topology, volume 7 (2003)
{#Bousfield}




### For unbounded chain complexes
  {#ForUnboundedChainComplexes}

Work specifically on model structures on unbounded complexes includes the following.

Spaltenstein wrote a famous paper

* N. Spaltenstein, _Resolutions of unbounded complexes_, Compositio Mathematica, 65 no. 2 (1988), p. 121-154 ([numdam](http://www.numdam.org/item?id=CM_1988__65_2_121_0))

on how to do homological algebra with unbounded complexes (in both sides) where he introduced notions like K-projective and K-injective complexes. Later,

* [[Vladimir Hinich]], _Homological algebra of homotopy algebras_, Comm. Algebra, vol. 25 (1997), no. 10, 3291-3323
([pdf at author's page](http://math.haifa.ac.il/hinich/WEB/mypapers/haha.pdf))

shows that there is a model category structure on the category of unbounded chain complexes, reproduces Spaltenstein's results from that perspective and extends them.

The model structure on unbounded chain complexs with fibrations the degreewise surjections is noted in the remark after theorem 9.3.1 in

* [[Mark Hovey]], J. Palmieri, [[Neil Strickland]], _Axiomatic stable homotopy theory_, Mem. Amer. Math. Soc. 128 (1997), no. 610.
 {#HoveyPalmieriStrickland97}

and noticed as cofibrantly generated model structure on p. 7 of

* [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ ([arXiv:math/9801082](http://arxiv.org/abs/math/9801082))
 {#SchwedeShipley98}

A textbook account is around Theorem 2.3.11 of:

* {#Hovey} [[Mark Hovey]], _Model Categories_, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover), [ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s))

That the corresponding [[category of simplicial objects]] in unbounded chain complexes is thus a [[Quillen equivalence|Quillen equivalent]] [[simplicial model category]] is cor. 4.6 in

* [[Charles Rezk]], [[Stefan Schwede]], [[Brooke Shipley]], _Simplicial structures on model categories and functors_, American Journal of Mathematics, Vol. 123, No. 3 (Jun., 2001), pp. 551-575  ([arXiv:0101162](http://arxiv.org/abs/math/0101162), [jstor](http://www.jstor.org/stable/pdfplus/25099071.pdf))
 {#RezkSchwedeShipley01}


The article

* [[Dan Christensen]], [[Mark Hovey]], _Quillen model structures for relative homological algebra_ ([pdf](http://jdc.math.uwo.ca/papers/relative.pdf))
{#ChristensenHovey}

discusses model structures on unbounded chain complexes with generalized notions of epimorphisms induced from "projective classes".

See also

* [[Dan Christensen]], _Derived categories and projective classes_ , (2005) ([hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Christensen/derived))

Another approach is due to [[James Gillespie]], using [[cotorsion pairs]].  An overview of this work is in

* [[Mark Hovey]], _Cotorsion pairs and model categories_, 2006 ([pdf](http://homepages.math.uic.edu/~bshipley/hovey.pdf))
{#HoveyOverview}

Some generalizations and simplifications of the original approach are discussed in

* [[James Gillespie]], _Kaplansky classes and derived categories_, 2007, [pdf](http://phobos.ramapo.edu/~jgillesp/updated%20qcsheaf.pdf)
{#Gillespie}

Finally a third approach to the unbounded case is discussed in

* [[Denis-Charles Cisinski]], F. D&#233;glise, _Local and stable homologial algebra in Grothendieck abelian categories_, Homology, Homotopy and Applications, vol. 11 (1) (2009)  ([url](http://www.intlpress.com/HHA/v11/n1/a11/))
{#CisinskiDeglise}

A discussion of the homotopy theory of [[presheaves]] of unbounded chain complex is in

* [[Rick Jardine]], _Presheaves of chain complexes_ ([ps](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.57.6884&rep=rep1&type=ps))

A model structure on noncommutative [[dg-algebra]]s whose proof strategy is useful also for cochain complexes is in

* [[Rick Jardine]], _[[JardineModelDG.pdf:file]]_ , Cyclic Cohomology and Noncommutative Geometry, Fields Institute Communications, Vol. 17, AMS (1997), 55-58.


[[!redirects model structures on chain complexes]]

[[!redirects model structure on cochain complexes]]
[[!redirects model structures on cochain complexes]]


[[!redirects model structure on unbounded chain complexes]]
[[!redirects model structures on unbounded chain complexes]]

[[!redirects projective model structure on chain complexes]]
[[!redirects injective model structure on chain complexes]] 

[[!redirects injective model structure on connective cochain complexes]]
