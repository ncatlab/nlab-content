
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

Model structures on chain complexes are [[model category]] structures on [[categories of chain complexes]] whose weak equivalences are [[quasi-isomorphism]]s. 


Via these model structures, all of the standard techniques in [[homological algebra]], such as [[injective resolutions]] and [[projective resolutions]], are special cases of constructions in [[homotopy theory]], such as [[cofibrant resolutions]] and [[fibrant resolutions]]. 

The existence of these model structures depends subtly on whether the chain complexes in question are bounded or not. 

### In non-negative degree

[[chain complex|Chain complexes]] in non-negative degree in an [[abelian category]] $A$ are special in that they may be identified via the [[Dold?Kan correspondence]] as [[simplicial object]]s in $A$.

$$
  Ch_{\bullet \geq 0}(A) \simeq A^{\Delta^{op}}
  \,.
$$

Similarly, [[cochain complex]]s are identified with [[cosimplicial object]]s

$$
  Ch^{\bullet \geq 0}(A) \simeq A^{\Delta}
  \,.
$$

At least if $A$ is the category of [[abelian groups]], so that $A^{\Delta^{op}}$ is the category of abelian [[simplicial group]]s it inherits naturally a model category structure from the [[model structure on simplicial sets]], which [[presentable (∞,1)-category|presents]] the [[(∞,1)-category]] of [[∞-groupoid]]s.

The model structure on chain complexes transports this presentation  of the special $\infty$-groupoids given by abelian simplicial groups along the Dold-Kan correspondence to chain complexes.

Analogous statements apply to the category of unbounded chain complexes and the canonical [[stable (infinity,1)-category]] [[Spec]] of [[spectrum|spectra]]. 

### For unbounded chain complexes

Model structures on unbounded (co)chain complexes can be understood as
presentations of [[spectrum object]]s in model structures of bounded (co)chain complexes.


## Definitions 



### In non-negative degree 
 {#CochainNonNeg}

Let $C$ be an [[abelian category]]. 

Recall that by the dual [[Dold-Kan correspondence]] the category $C^\Delta$ of [[cosimplicial object]]s in $C$ is equivalent to the catagory $Ch^\bullet_+(C)$ of [[cochain complexes]] in non-negative degree. This means that we can transfer results discussed at [[model structure on cosimplicial objects]] to cochain complexes (see [Bousfield2003, section 4.4](http://arxiv.org/PS_cache/math/pdf/0312/0312531v1.pdf) for more).

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

* fibrations are the morphisms that are [[epimorphisms]] in $R$[[Mod]] in each _positive_ degree;

* cofibrations are degreewise [[monomorphisms]] with degreewise [[projective object|projective]] [[cokernel]];

called the **projective model structure**.

=--

##### Injective structure on cochain complexes
 {#InjectiveStructureOnCochainComplexes}

Dually

+-- {: .num_theorem #InjectiveModelStructure}
###### Theorem

There is a [[model category]] structure on non-negatively graded [[cochain complex]]es 
$Ch^{\bullet \geq 0 }(A)$ whose

* weak equivalences are [[quasi-isomorphism]]s;

* cofibrations are the morphisms that are [[monomorphism]]s in $R Mod$ in each _positive_ degree;

* fibrations are degreewise [[epimorphism]]s with [[injective object|injective]] [[kernel]],

called the **injective model structure**.

=--

This model structure on $Ch^{\bullet \geq 0}$ is originally due to 
([Quillen II, section 4](#Quillen)).
An account is given for instance in ([Dungan, 2.4.2, proof in section 2.5](#Dungan)).

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

* $f$ is a fibration if it is degreewise a [[split epimorphism]] with $\mathcal{G}$-injective kernel.
 
=--

See [Bousfield2003, section 4.4](http://arxiv.org/PS_cache/math/pdf/0312/0312531v1.pdf).

If $A$ has enough [[injective object]]s and $\mathcal{G}$ is the clss of all of them, this reproduces the 
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

If $C = $ [[Vect]] is a category of [[vector space]]s over some field, we have that every epi/mono splits and that every [[quasi-isomorphism]] is a homotopy equivalence.  Moreover, in this case every chain complex is quasi-isomorphic to its [[homology]] (regarded as a chain complex with zero differentials).

This is the model structure which induces the [[transferred model structure|transferred]] [[model structure on dg-algebra]]s over a field. 

=--

#### With fibrations being surjections in all degrees
  {#CochainNonNegProj}

We discuss a model structure on cochain complexes of abelian groups
in which the fibrations are the degreewise epis. This
follows an analogous proof in ([Jardine](#Jardine))

+-- {: .num_theorem}
###### Theorem

The category $Ch^{\bullet \geq 0}(Ab)$ of non-negatively graded cochain complexes of [[abelian group]]s becomes a model category with

* fibrations the degreewise surjections;

* weak equivalences the [[quasi-isomorphism]]s.


This is a [[simplicial model category]]-structure
with respect to the canonical structure of an [[sSet]]-[[enriched category]]
induced from the dual [[Dold-Kan correspondence|Dold-Kan equivalence]]
$Ch^\bullet_+(Ab) \simeq Ab^\Delta$ by the fact that $Ab^\Delta$  is a [[category of cosimplicial objects]] (see there) in a category with all limits and colimits.

=--


+-- {: .proof}
###### Proof

We spell out a proof of the model structure below in a sequence of 
lemmas. The proof that this is a simplicial model category is
at [[model structure on cosimplicial abelian groups]].

=--

We record a detailed proof of the model structure on $Ch^{\bullet \geq 0}(Ab)$ with fibrations the degreewise surjections, following the appendix of ([Stel](#Stel)).


As usual, for $n \in \mathbb{N}$ write $\mathbb{Z}[n]$ for the complex concentrated on the additive group of [[integer]]s in degree $n$, and for $n \geq 1$  write $\mathbb{Z}[n-1,n]$ for the cochain complex $(0 \to \cdots 0 \to \mathbb{Z} \stackrel{Id}{\to} \mathbb{Z} \to 0 \cdots)$ with the two copies of $\mathbb{Z}$ in degree $n-1$ and $n$.

For $n = 0$ let $\mathbb{Z}[-1,0] = 0$, for convenience.

=--





+-- {: .num_lemma}
###### Lemma
{#ProjStructGenCofibs}

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


+-- {: .num_lemma}
###### Lemma
{#ProjStructCharAcyclicFibrations}

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

+-- {: .num_lemma}
###### Lemma
{#ProjStrucFactAxiomI}

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

#### General results
 {#InUnboundedDegreeGeneralResults}

Let $\mathcal{A}$ be an [[abelian category]] with all [[limit]]s and 
[[colimit]]s.

Write $Ch(\mathcal{A})$ for [[category of chain complexes|category of unbounded chain complexes]] in $\mathcal{A}$. 

Following [Christensen-Hovey](#ChristensenHovey) there is a family of model category structures on $Ch(\mathcal{A})$ parameterized by a choice of _projective class_ . 
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

Given a pair of [[adjoint functor]]s 

$$
  (F \dashv U) : \mathcal{A} \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} \mathcal{B}
$$ 

between [[abelian categories]] and given $(\mathcal{P}, \mathcal{E})$ a projective class in $\mathcal{B}$ then its **pullback projective class** $(U * \mathcal{P}, U^* \mathcal{E})$ along $U$ on $\mathcal{A}$ is defined by

* $U^* \mathcal{P} := \{retracts\;of\; F P | P \in \mathcal{P}\}$

 
=--

+-- {: .num_theorem #ModelStructureOnUnboundedFromProjectiveClass}
###### Definition/Theorem

Given a [projective class](#ProjectiveClass) $\mathcal{P}$ in $\mathcal{A}$, call a morphism $f \in Ch(\mathcal{A})$ 

* a fibration if $\mathcal{A}(P,f)$ is a surjection in [[Ab]] for all $P \in \mathcal{P}$;

* a weak equivalence if $\mathcal{A}(P,f)$ is a [[quasi-isomorphism]] in $Ch(Ab)$
  for all $P \in \mathcal{P}$. 

Then this constitutes a [[model category]] structure precisely if cofibrant [[resolution]]s exist, which is the case in particular if

1. $\mathcal{P}$ is the [pullback projective class](#PullbackProjectiveClass) of a [trivial projective class](#TrivialProjectiveClass) along a functor $U$ that preserves countable [[direct sum]]s;

1. blah-blah


When the structure exists, it is a [[proper model category]].


=--

This is theorem 2.2 in [Christensen-Hovey](#ChristensenHovey).

We shall write $Ch(\mathcal{A})_{\mathcal{P}}$ for this model category structure.



#### Examples 
 {#ExamplesOfStructuresOnUnboundedComplexes}

We list some example for the model structure on chain complexes is unbounded degree discussed [above](#InUnboundedDegreeGeneralResults).

Let $R$ be an associative ring and $\mathcal{A} = R$[[Mod]].

* [Categorical projective class structure](#CategoricalProjectiveClass)

* [Pure projective class structure](#CategoricalProjectiveClass)

##### Categorical projective class structure
 {#CategoricalProjectiveClass}

The **categorical projective class** on $\mathcal{A}$ is the [projective class](#ProjectiveClass) with $\mathcal{P}$ the class of [[direct sum]]mands of free modules. The $\mathcal{P}$-model structure on $Ch(\mathcal{A})$ has 

* as fibrations the degreewise surjections.

##### Pure projective class structure
 {#CategoricalProjectiveClass}

The **pure projective class** on $\mathcal{A}$ has as $\mathcal{P}$ summands of sums of finitely presented modules. Fibrations in the corresponding model structure are the maps that are degreewise those epimorphisms that appear in $\mathcal{P}$-exact sequences.

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

The [injective model structure](#InjectiveModelStructure) on $Ch_{\geq 0}(R Mod)$ is a [[cofibrantly generated model category]].

=--

This appears for instance as [Hovey, theorem 2.3.13](#Hovey).

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

## Examples

### On dg-modules

* [[model structure on dg-modules]].


## Related concepts

* [[stable model category]]

* [[(∞,1)-category of chain complexes]]


## References 
 {#References}

### For bounded chain complexes

An original source for the standard model structure on $Ch^{\bullet \geq 0}(A)$ with $A$ having enough injectives is

* [[Dan Quillen]], _Homotopical Algebra_ , Lecture Notes in Mathematics, vol. 43, Springer-Verlag, 1967
{#Quillen}


Of course the description of model categories of chain complexes as ([[presentable (infinity,1)-category|presentations]] of) special cases of (stable) $(\infty,1)$-categories is exactly opposite to the historical development of these ideas. 

While the homotopical treatment of weak equivalences of chain complexes ([[quasi-isomorphism]]s) in [[homological algebra]] is at the beginning of all studies of higher categories and a "folk theorem" ever since

* [[Andre Joyal]], Letter to Alexander Grothendieck. April 11, 1984

it seems that the injective model structure on chain complexes has been made fully explicit in print only in proposition 3.13 of

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math/0102087), [pdf](http://arxiv.org/PS_cache/math/pdf/0102/0102087v1.pdf))

(at least according to the remark below that).

The projective model structure is discussed after that in 

* [[Mark Hovey]], _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. 353, 6 ([pdf](http://www.mathaware.org/tran/2001-353-06/S0002-9947-01-02721-0/S0002-9947-01-02721-0.pdf))

An explicit proof of the injective model structure with monos in positive degree is spelled out in 

* Gregory Dungan, _Model categories_ ([pdf](http://www.math.fsu.edu/~gdungan/MC10.04.07.pdf))
{#Dungan}

An explicit proof of the model structure on cochain complexes of abelian group with fibrations the degreewise surjections is recorded in the appendix of

* [[Herman Stel]], _[[schreiber:master thesis Stel|∞-Stacks and their Function Algebras -- with Applications to ∞-Lie Theory]]_ (2010)
{#Stel}

The resolution model structures on cofibrant objects go back to

* [[William Dwyer]], [[Dan Kan]], C. Stover, _An $E_2$ model category structure for pointed simplicial spaces_, J. Pure and Applied Algebra 90 (1993) 137&#8211;152
{#DwyerKanStover}

and are reviewed in

* A. Bousfield, _Cosimplicial resolutions and homotopy spectral sequences in model categories_ Geometry and Topology, volume 7 (2003)
{#Bousfield}

Discussion of model category structures on chain complexes in [[Grothendieck abelian categories]] is in

* [[Denis-Charles Cisinski]], F. D&#233;glise, _Local and stable homologial algebra in Grothendieck abelian categories_, Homology, Homotopy and Applications, vol. 11 (1) (2009)  ([pdf](http://www.intlpress.com/HHA/v11/n1/a11/v11n1a11.pdf))


A general textbook account is in chapter 2 of

* [[Mark Hovey]], _Model categories_ 
  {#Hovey}


### For unbounded chain complexes

Work specifically on model structures on unbounded complexes includes the following.

Spaltenstein wrote a famous paper 

* N. Spaltenstein, _Resoutions of unbounded complexes_, Compositio Mathematica, 65 no. 2 (1988), p. 121-154 ([numdam](http://www.numdam.org/item?id=CM_1988__65_2_121_0))

on how to do homological algebra with unbounded complexes (in both sides) where he introduced notions like K-projective and K-injective complexes. Later, 

* [[Vladimir Hinich]], _Homological algebra of homotopy algebras_, Comm. Algebra, vol. 25 (1997), no. 10, 3291-3323
([pdf at author's page](http://math.haifa.ac.il/hinich/WEB/mypapers/haha.pdf)) 

shown that there is a model category structure on the category of unbounded chain complexes, reproduced Spaltenstein's results from that perspective and extended them widely. 

The article 

* [[Dan Christensen]], [[Mark Hovey]], _Quillen model structures for relative homological algebra_ ([pdf](http://jdc.math.uwo.ca/papers/relative.pdf))
{#ChristensenHovey}

discusses model structures on unbounded chain complexes with generalized notions of epimorphisms induced from "projective classes".

See also 

* [[Dan Christensen]], _Derived categories and projective classes_ , (2005) ([hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Christensen/derived))

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

