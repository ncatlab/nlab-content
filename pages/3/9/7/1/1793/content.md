
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

Via these model structures, all of the standard techniques in [[homological algebra]], such as injective and projective resolutions, are special cases of constructions in [[homotopy theory]], such as cofibrant and fibrant [[resolution]]s.

The existence of these model structures depends subtly on whether the chain complexes in question are bounded or not. 

### In non-negative degree

Chain complexes in non-negative degree in an [[abelian category]] $A$ are special in that they may be identified via the [[Dold?Kan correspondence]] as [[simplicial object]]s in $A$.

$$
  Ch_+(A) \simeq A^{\Delta^{op}}
  \,.
$$

At least if $A$ is the category of [[abelian groups]], so that $A^{\Delta^{op}}$ is the category of abelian [[simplicial group]]s it inherits naturally a model category structure from the [[model structure on simplicial sets]], which [[presentable (∞,1)-category|presents]] the [[(∞,1)-category]] of [[∞-groupoid]]s.

The model structure on chain complexes transports this presentation  of the special $\infty$-groupoids given by abelian simplicial groups along the Dold-Kan correspondence to chain complexes.

Analogous statements apply to the category of unbounded chain complexes and the canonical [[stable (infinity,1)-category]] [[Spec]] of [[spectrum|spectra]]. 

### For unbounded chain complexes

See the [references](#References) by Spaltenstein and Hinich below.

## Definitions 

(...)

### Model structures on cochain complexes in non-negative degree {#CochainNonNeg}

Let $C$ be an [[abelian category]]. 

Recall that by the dual [[Dold-Kan correspondence]] the category $C^\Delta$ of [[cosimplicial object]]s in $C$ is equivalent to the catagory $Ch^\bullet_+(C)$ of [[cochain complex]]es in non-negative degree. This means that we can transfer results discussed at [[model structure on cosimplicial objects]] to cochain complexes (see [Bousfield2003, section 4.4](http://arxiv.org/PS_cache/math/pdf/0312/0312531v1.pdf) for more).

#### General results

Let $G \in Obj(C)$ be a [[class]] of objects, such that $C$ has enough $G$-[[injective object]]s. 

Then there is a model category structure $Ch^\bullet_+(C)_G$ whose

* weak equivalences are maps $f : X \to Y$ such that for each $A \in G$ the induced map $C(Y,A) \to C(X,A)$ is a [[quasi-isomorphism]] of chain complexes of abelian groups;

* $f$ is a cofibration if it is $G$-monic in positive degree;

* $f$ is a fibration if it is degreewise a [[split epimorphism]] with $G$-injective kernel.
 
If for example we take $G$ to be the class of all objects of $C$, then this induces a model structure $Ch^\bullet_+(C)_{tot}$ whose

* weak equivalences are cochain [[homotopy equivalence]]s;

* fibrations are morphisms that are degreewise [[split epimorphism]]s;

* cofibration are morphisms that are in positive degree [[split monomorphism]]s.

As an example of that, if $C = $ [[Vect]] is a category of [[vector space]]s over some field, we have that every epi/mono splits and that every [[quasi-isomorphism]] is a homotopy equivalence. 

This is the model structure which induces the [[transferred model structure|transferred]] [[model structure on dg-algebra]]s over a field. 

#### The projective model structure {#CochainNonNegProj}


+-- {: .un_theorem}
###### Theorem

The category $Ch^\bullet_+(Ab)$ of non-negatively graded cochain complexes of [[abelian group]]s becomes a model category with

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

We record a detailed proof of the model structure on $Ch^\bullet_+(Ab)$ with fibrations the degreewise surjections, following the appendix of ([Stel](#Stel)).

+-- {: .un_def}
###### Definition

As usual, for $n \in \mathbb{N}$ write $\mathbb{Z}[n]$ for the complex concentrated on the additive group of [[integer]]s in degree $n$, and for $n \geq 1$  write $\mathbb{Z}[n-1,n]$ for the cochain complex $(0 \to \cdots 0 \to \mathbb{Z} \stackrel{Id}{\to} \mathbb{Z} \to 0 \cdots)$ with the two copies of $\mathbb{Z}$ in degree $n-1$ and $n$.

For $n = 0$ let $\mathbb{Z}[-1,0] = 0$, for convenience.

=--





+-- {: .un_lemma}
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

+-- {: .un_lemma}
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


+-- {: .un_lemma}
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

+-- {: .un_lemma}
###### Lemma
{#ProjStrucFactAxiomI}

Every morphism $f : A \to B$ can be factored as 
a morphism with left leifting property against all
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

+-- {: .un_lemma}
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

+-- {: .un_lemma}
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
    \hat B \stackrel{p}{\to}
  }
$$

makes manifest that this exhibts $f$ as a retract of $j$
and as such inherits its left lefting properties.

=--

This series of lemmas establishes the claimed model structure
on $Ch^\bullet_+(Ab)$.

### Model structure on unbounded chain complexes {#OnUnbounded}

#### General results

Let $\mathcal{A}$ be an [[abelian category]] with all [[limit]]s and 
[[colimit]]s.

Write $Ch(\mathcal{A})$ for [[category of chain complexes|category of unbounded chain complexes]] in $\mathcal{A}$. 

Following [Christensen-Hovey](#ChristensenHovey) there is a family of model category structures on $Ch(\mathcal{A})$, all refining the [[category with weak equivalences]] given by [[quasi-isomorphism]]s, but where the fibrations are degreewise surjections in a generalized sense, a sense that is parameterized by a choice of _projective class_ . 

{#ProjectiveClass}

+-- {: .un_defn}
###### Definition

A **projective class** on $\mathcal{A}$ is a collection $\mathcal{P} \subset ob \mathcal{A}$ of [[object]]s and a collection $\mathcal{E} \subset mor \mathcal{A}$ of [[morphism]]s, such that

* $\mathcal{E}$ is precisely the collection of $\mathcal{P}$-epic maps;

* $\mathcal{P}$ is precisely the collection of all objects $P$ such that each map in $\mathcal{E}$ is $P$-epic.

=--

{#TrivialProjectiveClass}

+-- {: .un_example}
###### Example

Taking $\mathcal{P} := ob \mathcal{A}$ to be the class of _all_ objects yields a projective class -- called the *trivial projective class** . The corresponding morphisms are the class $\mathcal{E}$ of all [[split epimorphism]]s in $\mathcal{A}$.

=--

{#PullbackProjectiveClass}

+-- {: .un_example}
###### Example

Let $R$ be a [[ring]] and $\mathcal{A} = $ $R$-[[Mod]] be the category of $R$-[[module]]s. Choosing $\mathcal{P}$ to be the class of all summands of [[direct sums]] of [[finitely presented]] modules yields a projective class.

=--

+-- {: .un_example}
###### Example

Given a pair of [[adjoint functor]]s 

$$
  (F \dahsv U) : \mathcal{A} \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} \mathcal{B}
$$ 

between [[abelian categories]] and given $(\mathcal{P}, \mathcal{E})$ a projective class in $\mathcal{B}$ then its **pullback projective class** $(U * \mathcal{P}, U^* \mathcal{E})$ along $U$ on $\mathcal{A}$ is defined by

* $U^* \mathcal{P} := \{retracts\;of\; F P | P \in \mathcal{P}\}$

 
=--

+-- {: .un_theorem}
###### Definition/Theorem

Given a projective class $\mathcal{P}$ in $\mathcal{A}$, call a morphism $f \in Ch(\mathcal{A)$ 

* a fibration if $\mathcal{A}(P,f)$ is a surjection in [[Ab]] for all $P \in \mathcal{P}$;

* a weak equivalence if it is a [[quasi-isomorphism]]. 

Then this constitutes a [[model category]] structure precisely if cofibrant [[resolution]]s exist, which is the case in particular if

1. $\mathcal{P}$ is the [pullback projective class](#PullbackProjectiveClass) of a [trivial projective class](#TrivialProjectiveClass) along a functor $U$ that preserves countable [[direct sum]]s;

1. blah-blah


When the structure exists, it is a [[proper model category]].


=--

This is theorem 2.2 in [Christensen-Hovey](#ChristensenHovey).

#### Examples 

Let $R$ be an associative ring and $\mathcal{A} = R$[[Mod]].

* The **categorical projective class** on $\mathcal{A}$ is the [projective class](#ProjectiveClass) with $\mathcal{P}$ the class of [[sirect sum]]mands of free modules. The $\mathcal{P}$-model structure on $Ch(\mathcal{A})$ has as fibrations the degreewise surjections.

* The **pure projective class** on $\mathcal{A}$ has as $\mathcal{P}$ summands of sums of finitely presented modules. Fibrations in the corresponding model structure are the maps that are degreewise those epimorphisms that appear in $\mathcal{P}$-exact sequences.

## History and references {#References}

Of course the description of model categories of chain complexes as ([[presentable (infinity,1)-category|presentations]] of) special cases of (stable) $(\infty,1)$-categories is exactly opposite to the historical development of these ideas. 

While the homotopical treatment of weak equivalences of chain complexes ([[quasi-isomorphism]]s) in [[homological algebra]] is at the beginning of all studies of higher categories and a "folk theorem" ever since

* [[Andre Joyal]], Letter to Alexander Grothendieck. April 11, 1984

it seems that the injective model structure on chain complexes has been made fully explicit in print only in proposition 3.13 of

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math/0102087), [pdf](http://arxiv.org/PS_cache/math/pdf/0102/0102087v1.pdf))

(at least according to the remark below that).

The projective model structure is discussed after that in 

* [[Mark Hovey]], _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. 353, 6 ([pdf](http://www.mathaware.org/tran/2001-353-06/S0002-9947-01-02721-0/S0002-9947-01-02721-0.pdf))

An explicit proof of the model structure on cochain complexes of abelian group with fibrations the degreewise surjections is recorded in the appendix of

* [[nLab:Herman Stel]], _[[schreiber:master thesis Stel|∞-Stacks and their Function Algebras -- with Applications to ∞-Lie Theory]]_ (2010)
{#Stel}

### For unbounded chain complexes

Work specifically on model structures on unbounded complexes includes the following.

Spaltenstein wrote a famous paper 

* N. Spaltenstein, _Resoutions of unbounded complexes_, Compositio Mathematica, 65 no. 2 (1988), p. 121-154 ([numdam](http://www.numdam.org/item?id=CM_1988__65_2_121_0))

on how to do homological algebra with unbounded complexes (in both sides) where he introduced notions like K-projective and K-injective complexes. Later, 

* V. Hinich, _Homological algebra of homotopy algebras_, Comm. Algebra, vol. 25 (1997), no. 10, 3291-3323
([pdf at author's page](http://math.haifa.ac.il/hinich/WEB/mypapers/haha.pdf)) 

shown that there is a model category structure on the category of unbounded chain complexes, reproduced Spaltenstein's results from that perspective and extended them widely. 

The article variant model structures on chain complexes are discussed in

* [[Dan Christensen]], [[Mark Hovey]], _Quillen model structures for relative homological algebra_ ([pdf](http://jdc.math.uwo.ca/papers/relative.pdf))
{#ChristensenHovey}

discusses model structures on unbounded chain complexes with generalized notions of epimorphisms induced from "projectve classes".


See also 

* [[Dan Christensen]], _Derived categories and projective classes_ , (2005) ([hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Christensen/derived))




[[!redirects model structures on chain complexes]]

[[!redirects model structure on cochain complexes]]
[[!redirects model structures on cochain complexes]]
