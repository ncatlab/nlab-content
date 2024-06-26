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
* table of contents
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

* [[weak equivalences]] are the [[quasi-isomorphisms]];

* [[fibrations]] are the morphisms that are [[underlying]] [[epimorphisms]] in $R$[[Mod]] in each _[[positive number|positive]]_ degree;

* [[cofibrations]] are degreewise [[monomorphisms]] with degreewise [[projective object|projective]] [[cokernel]];

called the **projective model structure**.

=--

The projective model structure on $Ch_{\bullet \geq 0}$ is originally due to
([Quillen 67, II.4, pages II.4.11, II.4.12](#Quillen67)).
See also ([Goerss-Schemmerhorn 06, Theorem 1.5](#GoerssSchemmerhorn06), [Dungan 10, 2.4.2, proof in section 2.5](#Dungan10)).


\begin{prop}\label{ProjectiveModelStructureOnConnectiveChainComplexesIsProper}
  The projective model structure on connective chain complexes is a [[proper model category]].
\end{prop}
(e.g. [Jardine 03, Prop. 1.5](#Jardine03))

\begin{proposition}
\label{ProjectiveModelStructureOnConnectiveChainComplexesIsMonoidal}
{#MonoidalModelStructureOnConnectiveChainComplexes} With respect to the [[tensor product of chain complexes]] this is a [[monoidal model category]].
\end{proposition}
(e.g. [Jardine 03, Prop. 1.5](#Jardine03),  [Schwede & Shipley 2003, p. 312 (26 of 48)](#SchwedeShipley03)). 



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

If $C = $ [[Vect]] is a category of [[vector spaces]] over some [[field]], we have that every epi/mono splits and that every [[quasi-isomorphism]] is a homotopy equivalence.  Moreover, in this case every chain complex is quasi-isomorphic to its [[homology]] (regarded as a chain complex with zero differentials).

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

For all $n \in \mathbb{N}$, the morphism $0 \to \mathbb{Z}[n-1,n]$ are acyclic cofibrations, in that they have the [[left lifting property]] again all degreewise surjections.

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

\begin{proposition}
\label{StandardModelStructureOnUnboundedComplexes}
For $R$ a [[commutative ring]] the [[category of unbounded chain complexes]] $Ch_\bullet(R Mod)$ of $R$-[[modules]]  admits the [[structure]] of a

* [[proper model category|proper]]

* [[cofibrantly generated model category|cofibrantly generated]] 

  {#GeneratingCofibrationsOfUnboundedProjectiveStructure} with generating (acyclic) cofibrations being, for $n \in \mathbb{Z}$:

\begin{tikzcd}[sep=10pt]
      S^{n-1}
      \ar[d, "{ i_n }"]
      \ar[r, phantom, ":\equiv"]
      &
      \big[\;
      \cdots
      \ar[r]
      &
      0 
      \ar[r]
      \ar[d]
      &
      0
      \ar[r]
      \ar[d]
      &
      0
      \ar[r]
      \ar[d]
      &
      R
      \ar[r]
      \ar[d, "{\mathrm{id}}"]
      &
      0
      \ar[r]
      \ar[d]
      &
      \cdots
      \;\big]
      \\
      D^n
      \ar[r, phantom, ":\equiv"]
      &
      \big[\;
      \cdots
      \ar[r]
      &
      0 
      \ar[r]
      &
      0
      \ar[r]
      &
      \underset{
        \mathclap{
          \raisebox{-3pt}{
            \scalebox{.7}{
              $\mathrm{deg} = n$
            }
          }
        }
      }{
      R
      }
      \ar[r, "{ \mathrm{id} }"]
      &
      R
      \ar[r]
      &
      0
      \ar[r]
      &
      \cdots
      \;\big]
\end{tikzcd}

\begin{tikzcd}[sep=10pt]
      0
      \ar[d, "{ j_n }"]
      \ar[r, phantom, ":\equiv"]
      &
      \big[\;
      \cdots
      \ar[r]
      &
      0 
      \ar[r]
      \ar[d]
      &
      0
      \ar[r]
      \ar[d]
      &
      0
      \ar[r]
      \ar[d]
      &
      0
      \ar[r]
      \ar[d]
      &
      0
      \ar[r]
      \ar[d]
      &
      \cdots
      \;\big]
      \\
      D^n
      \ar[r, phantom, ":\equiv"]
      &
      \big[\;
      \cdots
      \ar[r]
      &
      0 
      \ar[r]
      &
      0
      \ar[r]
      &
      \underset{
        \mathclap{
          \raisebox{-3pt}{
            \scalebox{.7}{
              $\mathrm{deg} = n$
            }
          }
        }
      }{
      R
      }
      \ar[r, "{\mathrm{id}}"]
      &
      R
      \ar[r]
      &
      0
      \ar[r]
      &
      \cdots
      \;\big]
\end{tikzcd}


* [[combinatorial model category|combinatorial]]

[[model category]] with

* [[weak equivalences]] the [[quasi-isomorphisms]]

* [[fibrations]] the (degreewise) [[epimorphisms]].

* [[cofibrations]] the degreewise [[split monomorphism|split injections]] with cofibrant [[cokernel]].

\end{proposition}
(For partial characterization of the [[cofibrant objects]] see further [below](#BoundedBelowComplexesOfProjectivesAreProjectivelyCofibrant).)
\begin{proof}
Properness and cofibrant generation are discussed in [Hovey, Palmieri & Strickland (1997), remark after theorem 9.3.1](#HoveyPalmieriStrickland97) and [Schwede & Shipley (1998), p. 7](#SchwedeShipley98), see also [Fauk (2006), Thm. 3.2](#Fausk06). The characterization of the cofibrations is in [Hovey (1999), Lem. 2.3.6](#Hovey99) and that of the generating cofibrations are made explicit in [Hovey (1999), Def. 2.3.3](#Hovey99). Cf. also [Muro & Roitzheim (2019), pp. 3](#MuroRoitzheim19).

{#LocalPresentability} It remains to see that the [[underlying]] [[category of chain complexes]] is [[locally presentable category|locally presentable]], so that the model structure is [[combinatorial model category|combinatorial]]. (This minor but important point must be clear to the above authors, but seems not to be made explicit in any of the references.) This follows because:

1. $R$[[Mod]] is a [[Grothendieck abelian category]] (by [this example](Grothendieck+category#CateoriesOfModules));

1. when $\mathcal{A}$ is a Grothendieck abelian category then so is $Ch_\bullet(\mathcal{A})$ (by [this example](Grothendieck+category#ChainComplexesInGrothAbCat));

1. all Grothendick abelian categories are locally presentable (by [this example](locally+presentable+category#GrothAbCatsAreLocPresntbl)).

\end{proof}

\begin{remark}\label{NotAllUnboundedComplexesAreProjectivelyCofibrant}
  It is clear that every chain complex in the model structure of Prop. \ref{StandardModelStructureOnUnboundedComplexes} is [[fibrant object|fibrant]]. However, over general rings (not though over [[fields]], see Prop. \ref{UnboundedChainComplexOfVectorSpacesProjectivelyCofibrant} below) *not* every chain complex is [[cofibrant object|cofibrant]], not even those consisting of [[projective modules]] --
a [[counterexample]] is given in [Hovey (1999), Rem. 2.3.7](#Hovey99):

For $\mathbb{K}$ any [[field]], let $R \coloneqq \mathbb{K} \oplus \mathbb{K} \cdot x$ be its [[ring of dual numbers]], i.e. with $x^2 = 0$. 

Denote its [[augmented algebra|augmentation]] by

$$
  \array{
    \mathllap{
    \epsilon
    \;\colon\;
    }
    \mathbb{K} \oplus \mathbb{K} \cdot x
    &\longrightarrow&
    \mathbb{K}
    \\
    a + b x &\mapsto& a
  }
$$

Via this [[ring homomorphism]] we regard $\mathbb{K}$ as an $R$-[[module]].

Now in the category $Ch_\bullet(R Mod)$, consider the following unbounded chain complex:

$$
  \mathcal{A}
  \;\coloneqq\;
  \left(
  \cdots
  \to 
  \mathbb{K} \oplus \mathbb{K}x
  \xrightarrow{
    \;\;
    \cdot x
    \;\;
  }
  \mathbb{K} \oplus \mathbb{K}x
  \xrightarrow{
    \;\;
    \cdot x
    \;\;
  }
  \mathbb{K} \oplus \mathbb{K}x
  \to 
  \cdots
  \right)
  \,.
$$
Since its [[chain homology]] clearly vanishes in every degree, the morphism it receives out of the [[zero object]] is a [[quasi-isomorphism]] and hence a [[weak equivalence]]
$$
  0 \underset{\in \mathrm{W}}{\longrightarrow} \mathcal{A}
$$
and hence would be an [[acyclic cofibration]] if $\mathcal{A}$ were cofibrant.

But consider then the following [[lifting problem]] with this morphism

$$
  \array{
    &\longrightarrow&
    \big(
      \cdots \to 0 \to 0 \to R \to 0 \to 0 \to \cdots
    \big)
    \\
    \Bigg\downarrow
    &&
    \Bigg\downarrow
    {}^{
      \epsilon
    }
    \\
    \mathcal{A}
    &
    \overset{
      \;\;
      \epsilon
      \;\;\;
    }{
      \longrightarrow
    }
    &
    \big(
      \cdots \to 0 \to 0 \to \mathbb{K} \to 0 \to 0 \to \cdots
    \big)
    \mathrlap{\,,.}
  }
$$

Since the morphism on the right is clearly degreewise surjective and hence a [[fibration]] in the model structure, cofibrancy of $\mathcal{A}$ would imply that a [[lift]] in this diagram exists. But to be even a lift of the [[underlying]] [[graded modules]] this lift would have to be the [[identity morphism]] on $R$ in degree 0, in order to make (in degree 0), this [[diagram]] of $R$-[[modules]] [[commuting diagram|commute]]:

$$
  \array{
    && R
    \\
    & \mathllap{^{id}}\nearrow 
    & \downarrow \mathrlap{^\epsilon}
    \\
    R &\underset{\epsilon}{\longrightarrow}& \mathbb{K}
  }
$$

But that underlying lift fails to be a [[chain map]] in degrees (-1,0), where the following [[diagram]] does *not* [[commuting diagram|commute]]

$$
  \array{
    0 
    &\longrightarrow&
    \mathbb{K} \oplus \mathbb{K}x     
    \\
    \mathllap{^{id}}
    \Big\uparrow
    &\color{red}\times&
    \Big\uparrow
    \mathrlap{^{id}}
    \\
    \mathbb{K} \oplus \mathbb{K}x 
    &\underset{\cdot x}{\longrightarrow}&      
    \mathbb{K} \oplus \mathbb{K}x 
    \mathrlap{\,.}
  }
$$

It follows that the lift does not exist, hence that we have found an object $\mathcal{A}$ in the model structure from Prop. \ref{StandardModelStructureOnUnboundedComplexes} which is not cofibrant.
\end{remark}

On the other hand:

\begin{proposition}\label{BoundedBelowComplexesOfProjectivesAreProjectivelyCofibrant}
**([[bounded-below chain complexes]] of [[projective modules]] are projectively [[cofibrant object|cofibrant]])**
\linebreak
  Every [[bounded-below chain complex]] of [[projective modules]] is [[cofibrant object|cofibrant]] in the model structure of Prop. \ref{StandardModelStructureOnUnboundedComplexes}.
\end{proposition}
([Hovey (1999), Lem. 2.3.6](#Hovey99))

This implies:

\begin{proposition}
\label{UnboundedChainComplexOfVectorSpacesProjectivelyCofibrant}
  For $k$ a [[field]]:

1. every [[object]] in the projective model structure $Ch_\bullet(k Mod)$ (Prop. \ref{StandardModelStructureOnUnboundedComplexes}) is [[cofibrant objects|cofibrant]].

1. the [[cofibrations]] are exactly the [[monomorphisms]].

\end{proposition}
\begin{proof}
 By the assumption that $k$ is a field, every $k$-module (i.e. every $k$-[[vector space]]) is [[projective module|projective]] ([this Prop.](projective+module#ModuleOverAFieldIsProjective)). Therefore Prop. \ref{BoundedBelowComplexesOfProjectivesAreProjectivelyCofibrant} says, in this situation, that every [[bounded-below chain complex]] is cofibrant
Moreover, since every injection of vector spaces splits ([here](Vect#ShortExactSequencesSplit)) the characterization of cofibrations in Prop. \ref{StandardModelStructureOnUnboundedComplexes} says that every [[injection]] into a [[bounded-below chain complex]] of vector spaces is a cofibration (since its [[cokernel]] is clearly itself bounded-below and hence cofibrant by the previous statement) . 

Now every chain complex $V_\bullet$ is the [[colimit]] of its stages of lower [[connective covers]]:

$$
  cn_0 V_\bullet
  \hookrightarrow
  cn_{-1} V_\bullet
  \hookrightarrow
  cn_{-2} V_\bullet
  \hookrightarrow
  \cdots
  \,.
$$
By the previous paragraph, $cn_0 V_\bullet$ is cofibrant and each morphism in this [[cotower]] is a cofibration. Therefore $cn_0 V_\bullet \hookrightarrow V_\bullet$ is a [[transfinite composition]] of cofibrations, hence a cofibration, and therefore $V_\bullet$ is cofibrant.  

This proves the first statement. From this the second follows by the characterization of the cofibrations in Prop. \ref{StandardModelStructureOnUnboundedComplexes} and using again that all injections here are split.
\end{proof}
(Alternatively one may argue via the generating cofibration, cf. [MO:a/2457259](https://math.stackexchange.com/a/2457259/58526).)


\begin{proposition}
\label{MonoidalProjectiveModelStructureOnUnboundedChainComplexes}
The [[tensor product of chain complexes]] makes the projective model structure on unbounded chain complexes $Ch_\bullet(R Mod)$ (Prop. \ref{StandardModelStructureOnUnboundedComplexes}) a [[monoidal model category]].
\end{proposition}
For the special case that all [[submodules]] of [[free modules]] are again free (such as over $R = \mathbb{Z}$ the [[integers]], by [this Prop.](free+abelian+group#SubgroupsOfFreeAbelianGroupsAreFree), or for $R = k$ a [[field]] by [this Prop](free+module#EveryModuleOverAFieldIsFree), and in general for $R$ a [[principal ideal domain]], by [this Prop.](free+module#submod)) a short proof is given in [Strickland (2020), Prop. 25](#Strickland20). The general statement is also a special case of [Hovey (2001), Cor. 3.7](#Hovey01) [Fausk (2006), Thm. 6.1](#Fausk06) (who state an even more general result about *[[sheaves]]* of chain complexes).

\begin{proposition}
\label{LocalizedReedyModelStructureOnSimplicialUnboundedChainComplexes}
The  [[category of simplicial objects]] $sCh(R Mod)_\bullet$ in the projective model structure on unbounded chain complexes (from Prop. \ref{BoundedBelowComplexesOfProjectivesAreProjectivelyCofibrant}) carries the structure of a [[combinatorial model category|combinatorial]] [[simplicial model category]] (obtained as a [[Bousfield localization of model categories|left Bousfield localization]] of the [[Reedy model structure]]), whose weak equivalences are the maps that are [[quasi-isomorphisms]] under the [[total chain complex]] functor, and such that the [[underlying]] [[model category]] is [[Quillen equivalence|Quillen equivalent]] via :
\[
  \label{QuillenEquivalenceBetweenProjectiveUnboundedChainAndSimpEnhancement}
  const 
    \,\colon\,
  Ch_\bullet(R Mod) 
  \rightleftarrows
  sCh_\bullet(R Mod)
   \,\colon\,
  ev_0
  \,.
\]
\end{proposition}
\begin{proof}
The existence as a simplicial model category and Quillen equivalence of the underlying categories is due to [Rezk, Schwede & Shipley (2001), cor. 4.6](#RezkSchwedeShipley01), using methods like those discussed at *[simplicial model category -- Simplicial Quillen equivalent models](simplicial+model+category#SimpEquivMods)*.

Moreover, general facts imply that 

1. a Reedy model structure with coefficients in a combinatorial model category is itself combinatorial (see [here](Reedy+model+structure#CombinatorialStructure))

1. the [[left Bousfield localization]] of a combinatorial model category is itself combinatorial (see [here](Bousfield+localization+of+model+categories#Existence)).

\end{proof}

Below, this model structure is recovered as example \ref{CategoricalProjectiveClasses} of the [Christensen-Hovey projective class construction](#InUnboundedDegreeGeneralResults).


\begin{proposition}
\label{OverGroundFieldAllObjectsInSimplicialStructureOnUnboundedComplexesAreCofibrant}
 Over a [[field]] $k$, every object in the model structure on $sCh_\bullet(k Mod)$ (from Prop. \ref{LocalizedReedyModelStructureOnSimplicialUnboundedChainComplexes}) is cofibrant.
\end{proposition}
\begin{proof}
Since [[Bousfield localization of model categories|left Bousfield localization]] does not change the class of cofibrations, we need to show that every object $V_\bullet^\bullet \in sCh_\bullet(k Mod)$ is [Reedy cofibrant](Reedy+model+structure#ReedyModelStructure),
hence (cf. [this Remark](Reedy+model+structure#ReedyCofibrantObjects)) that the comparison morphisms from the [[latching objects]] $L_r V^r_\bullet \to V^r_\bullet$ are monomorphisms for all $r \in \mathbb{R}$.
But since $Ch_\bullet(k Mod)$ is an [[abelian category]] (cf. [here](category+of+chain+complexes#AbelianCategoryStructure)), [this Prop.](Reedy+model+structure#LatchingInAbelianCategoryIsDegeneracySubobject) at *[[Reedy model structure]]* says that these are [[monomorphisms]] and hence the claim follows by Prop. \ref{UnboundedChainComplexOfVectorSpacesProjectivelyCofibrant}.
\end{proof}

\begin{proposition}
\label{MonoidalSimplicialEnhancementOfUnboundedChainModelStructure}
  At least over a [[field]] $k$,
  the local model structure on $sCh_\bullet(k)$ from Prop. \ref{LocalizedReedyModelStructureOnSimplicialUnboundedChainComplexes} becomes a [[monoidal model category]] via the $\Delta$-object-wise [[tensor product of chain complexes]], and the [[Quillen equivalence]] (eq:QuillenEquivalenceBetweenProjectiveUnboundedChainAndSimpEnhancement) is a compatibly [[monoidal Quillen adjunction]] with respect to the corresponding monoidal model structure on $Ch_\bullet(k)$ from Prop. \ref{MonoidalProjectiveModelStructureOnUnboundedChainComplexes}, Prop. \ref{MonoidalProjectiveModelStructureOnUnboundedChainComplexes}.
\end{proposition}
This ought to be compatible with the simplicial structure such as to give a [[simplicial monoidal model category]].
\begin{proof}
  First, the plain [[Reedy model structure]] in $sCh_\bullet(k)$ becomes a [[monoidal model category]] under the objectwise [[tensor product of chain complexes]], by [Barwick (2010), Thm. 3.51](monoidal+model+category#Barwick10) (beware that the notation "$\mathbf{M}(A)$" there does refer to the Reedy model structure on *presheaves*, $Func(A^{op}, \mathbf{M})$ (cf. p. 265), which means that the condition that $A^{\leftarrow}$ consists of epimorphisms *is* satisfied for our case where, under this notational convention, $A = \Delta$).



{#SimplicialMonoidalModelStructure} Next, to see that this monoidal model structure passes to the [[Bousfield localization of model categories|left Bousfield localization]] of $sCh_\bullet(k)$ at the realization equivalences:

Observing that every object in $sCh(k)$ is a simplicial homotopy colimit of simplicially constant objects (by an argument as in [this Prop.](homotopy+limit#SimplicialSetIsHomotopyColimitOverItself)) and recalling that the local objects in $sCh(k)$ are the homotopically constant simplicial objects, it is sufficient to check --- by [Barwick (2010), Prop. 4.47](Bousfield+localization+of+model+categories#Barwick10) --- that for $V \,\in\, Ch(k)$ and $\mathscr{W} \,\in\, sCh(k)$ homotopically constant, also their [[internal hom]] $[const(V),\,\mathscr{W}] \,\in\, sCh(k)$ is homotopically constant. 

Now, on general grounds, the internal hom in $sCh(k)$ is given by an [[end]] over the internal hom in $Ch(k)$ (to be denoted by the same angular bracket notation), as follows:
$$
  [\mathscr{V},\,\mathscr{W}]
  \;\colon\;
  [s]
  \;\mapsto\;
  \int_{[s'] \in \Delta}
  \big[ 
    (\Delta[s] \cdot \mathscr{V})_{s'}
    ,\,
    \mathscr{W}_{s'}
  \big]
  \,,
$$
where $(-)\cdot(-)$ denotes the canonical [[tensoring]] of $sCh(k)$ over [[sSet]].

So in the case at hand, where $\mathscr{V} \,=\, const(V)$, we find this to be:
$$
  \begin{array}{l}
    [const(V),\, \mathscr{W}] 
    \,\colon\, 
    [s] \;\mapsto\; 
    \\
    \int_{s'}
    \big[
      \Delta(s',s) 
      \cdot V
      ,\,
      \mathscr{W}_{s'}
    \big]
    \\
    \;\simeq\;
    \Big[
      V
      ,\,
    \int_{s'}
      (\mathscr{W}_{s'})^{\Delta(s',s)}
    \Big]
    \\
    \;\simeq\;   
    \Big[
      V
      ,\,
      \mathscr{W}_s
    \Big]
    \,,
  \end{array}
$$
where we passed from [[tensoring]] $S\cdot (-)$ to its [[right adjoint]] [[powering]] $(-)^S$, used that an [internal hom preserves limits](hom-functor+preserves+limits#InternalHomFunctor) and then the [[enriched Yoneda lemma]] in its [[end]]-form (discussed at *[[co-Yoneda lemma]]*).

But since the objects $V,\,\mathscr{W}_{k'} \,\in\,Ch(k)$ are cofibrant and fibrant (as all objects of $Ch(k)$, by the above discussion), the functor $[V,-] \,\colon\, Ch(k) \to Ch(k) $ is a [[right Quillen functor]] and as such preserves weak equivalences between the fibrant objects $\mathscr{W}_{\bullet}$ (by [Ken Brown's lemma](Introduction+to+Homotopy}Theory#KenBrownLemma)). This means that if the simplicial chain complex $\mathscr{W}_\bullet$ is homotopically constant then so is the simplicial chain complex $ [const(V),\mathscr{W}] \,\colon\, [s] \,\mapsto\, [V,\, \mathscr{W}_s]$, which was to be shown.

It remains to observe that the Quillen equivalence to $Ch_\bullet(k)$ is a [[monoidal Quillen adjunction]], but this is immediate since $const$ is by aconstruction a [[strong monoidal functor]] and the [[tensor unit]] is [[cofibrant object|cofibrant]] (as all objects). 
\end{proof}


\linebreak

#### Standard injective model structure on unbounded chain complexes
 {#InjectiveModelStructureOnUnboundedChainComplexes}

\begin{proposition}
\label{StandardInjectiveModelStructureOnUnboundedComplexes}
For $R$ a [[commutative ring]] the [[category of unbounded chain complexes]] $Ch_\bullet(R Mod)$ of $R$-[[modules]]  carries the structure of a

* [[cofibrantly generated model category|cofibrantly generated]] 

* [[combinatorial model category|combinatorial]]

[[model category]] with

* [[weak equivalences]] the [[quasi-isomorphisms]]

* [[cofibrations]] the (degreewise) [[injections]].

\end{proposition}
This is [Hovey (1999), Thm. 2.3.13](#Hovey99).


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

1. $\mathcal{P}$ is the pullback projective class (def. \ref{PullbackProjectiveClass}) of a trivial projective class (def. \ref{TrivialProjectiveClass}) along a functor $U$ that preserves countable [[direct sums]];

1. (...)

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

> Beware that this entry has evolved in a way that deserves re-organization now: What follows are mainly properties of or arguments for the model structures on not-unbounded chain complexes.

### Properness
 {#Properness}

Model categories of chain complexes tend to be [[proper model categories]].

\begin{prop}\label{PushoutAlongDegreewiseInjectionsPreservesQuasiIosmorphism}
**([[pushout]] along degreewise [[injections]] presrves [[quasi-isomorphism]])** \linebreak
  Let 
  $$
   \array{
    A &\overset{\; i \;}{\longrightarrow}& B
    \\
    {}^{\mathllap{f}}
    \big\downarrow
    &{}^{{}_{(po)}}&
    \big\downarrow {}^{\mathrlap{g}}
    \\
    C &\underset{\; j \;}{\longrightarrow}& D
   }
  $$
  be a [[pushout]] [[commuting diagram|square]] of [[chain maps]] between (unbounded) [[chain complexes]], such that 

* $i$ is a degreewise [[injection]];

* $f$ is a [[quasi-isomorphism]].

Then also $g$ is a [[quasi-isomorphism]].

[[formal duality|Dually]], the [[pullback]] of a quasi-isomorphism along a degreewise [[surjection]] is again a quasi-isomorphism.
\end{prop}
(e.g. [Strickland 2020, Prop. 24](#Strickland20))
\begin{proof}
  The [[pushout]] of chain complexes is degreewise a pushout in the underlying [[abelian category]].
  Since pushout in abelian categories preserves monomorphisms ([this Prop.](abelian+category#PullbackPreservesEpimorphisms)) it follows that also $j_n$ is a monomorphism. Finally, the [[pasting law]] implies that the induced morphism of [[cokernels]] of $i$ and $j$ is an [[isomorphism]]. In summary, this means that we have a [[commuting diagram]] of chain complexes as follows:
  $$
   \array{
    A
    &\overset{\;\;\; i \;\;\;}{\hookrightarrow}& 
    B 
    &\longrightarrow&
    cok(i)
    \\
    {}^{\mathllap{f}}
    \big\downarrow
    &{}^{{}_{(po)}}&
    \big\downarrow {}^{\mathrlap{g}}
    &&
    \big\downarrow {}^{\mathrlap{\simeq}}
    \\
    C
    &\underset{\;\;\; j \;\;\;}{\hookrightarrow}& 
    D
    &\longrightarrow&
    cok(j)
    \,.
   }
  $$

This implies a morphism of the corresponding [[long exact sequences in chain homology]] of the form:

$$
  \array{
    \cdots
    &\to&
    H_{n+1}
    \big(
      cok(i)
    \big)
    &
    \xrightarrow{\; \delta \;}
    &
    H_n(A)
    &
    \xrightarrow{\; i_\ast\;}
    &
    H_n(B)
    &
    \xrightarrow{\;\;\;}
    &
    H_n\big(cok(i)\big)
    &
    \xrightarrow{\;\delta\;}
    &
    H_{n-1}(A)
    &
    \to
    &
    \cdots  
    \\
    &&
    {}^{\mathllap{}}
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{f_\ast}}
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{g_\ast}}
    \big\downarrow
    &&
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{f_\ast}}
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    \\
    \cdots
    &\to&
    H_{n+1}
    \big(
      cok(j)
    \big)
    &
    \xrightarrow{\; \delta \;}
    &
    H_n(C)
    &
    \xrightarrow{\; j_\ast\;}
    &
    H_n(D)
    &
    \xrightarrow{\;\;\;}
    &
    H_n\big(cok(j)\big)
    &
    \xrightarrow{\;\delta\;}
    &
    H_{n-1}(C)
    &
    \to
    &
    \cdots  
  }
$$
From this the [[five lemma]] implies that $g_\ast$ is an isomorphism on [[chain homology]], hence that $g$ is a quasi-isomorphism.
\end{proof}


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

see also:

* {#DwyerSpalinski95} [[William Dwyer]], [[Jan Spalinski]], Section 7 of: *[[Homotopy theories and model categories]]* ([[DwyerSpalinski_HomotopyTheories.pdf:file]]) 

  in: [[Ioan Mackenzie James|I. M. James]], *[[Handbook of Algebraic Topology]]*, North Holland 1995 ([ISBN:9780080532981](https://www.elsevier.com/books/handbook-of-algebraic-topology/james/978-0-444-81779-2), [doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))


* {#GoerssSchemmerhorn06} [[Paul Goerss]], [[Kirsten Schemmerhorn]], Theorem 1.5 in: _Model categories and simplicial methods_, Notes from lectures given at the University of Chicago, August 2004, in: _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007([arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537), [doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))

The projective model structure on connective *co*chain complexes (Theorem \ref{ProjectiveModelStructureOnConnectiveCochainComplexes}) is claimed, without proof, in:

* {#Hess06} [[Kathryn Hess]], p. 6 of _Rational homotopy theory: a brief introduction_, contribution to _[Summer School on Interactions between Homotopy Theory and Algebra](https://jdc.math.uwo.ca/summerschool/)_, University of Chicago, July 26-August 6, 2004, Chicago ([arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626)), chapter in Luchezar Lavramov, [[Dan Christensen]], [[William Dwyer]], [[Michael Mandell]], [[Brooke Shipley]] (eds.), _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007 ([doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))

* {#CastiglioniCortinas03} J. L. Castiglioni, G. Corti&#241;as, Def. 4.7 of: _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_, J. Pure Appl. Algebra  191  (2004),  no. 1-2, 119--142, ([arXiv:math.KT/0306289](http://arxiv.org/abs/math/0306289), [doi:10.1016/j.jpaa.2003.11.009](https://doi.org/10.1016/j.jpaa.2003.11.009))




Of course the description of model categories of chain complexes as ([[presentable (infinity,1)-category|presentations]] of) special cases of (stable) $(\infty,1)$-categories is exactly opposite to the historical development of these ideas.

While the homotopical treatment of weak equivalences of chain complexes ([[quasi-isomorphism]]s) in [[homological algebra]] is at the beginning of all studies of higher categories and a "folk theorem" ever since

* [[Andre Joyal]], Letter to Alexander Grothendieck. April 11, 1984

it seems that the injective model structure on chain complexes has been made fully explicit in print only in proposition 3.13 (according to remark 3.14 there) of

* [[Tibor Beke]] *Sheafifiable homotopy model categories*,  Math. Proc. Cambridge Philos. Soc. __129__ 3 (2000) 447-475 &lbrack;[arXiv:math/0102087](http://arxiv.org/abs/math/0102087), [doi:10.1017/S0305004100004722](https://doi.org/10.1017/S0305004100004722)&rbrack; 

The projective model structure is discussed after that (and shown to be a [[monoidal model category]]) in:

* {#Hovey99KTh} [[Mark Hovey]], *Model category structures on chain complexes of sheaves* (1999) &lbrack;[K-theory:0366](https://faculty.math.illinois.edu/K-theory/0366), [pdf](https://faculty.math.illinois.edu/K-theory/0366/sheaves.pdf), [[Hovey-SheavesOfChainComplexesPreprint.pdf:file]]&rbrack;

* {#Hovey01} [[Mark Hovey]], _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. **353** 6 (2001) &lbrack;[ams:S0002-9947-01-02721-0](https://www.ams.org/journals/tran/2001-353-06/S0002-9947-01-02721-0), [jstor:221954](https://www.jstor.org/stable/221954)&rbrack;  

An explicit proof of the injective model structure with monos in positive degree is spelled out in

* {#Dungan10} [[Gregory Dungan]], _Review of model categories_, 2010 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.696.123&rep=rep1&type=pdf), [[DunganModelCategories.pdf:file]])

An explicit proof of the model structure on cochain complexes of abelian groups with fibrations the degreewise surjections is recorded in the appendix of

* [[Herman Stel]], _[[schreiber:master thesis Stel|∞-Stacks and their Function Algebras -- with Applications to ∞-Lie Theory]]_ (2010)
{#Stel}

The resolution model structures on cofibrant objects go back to

* [[William Dwyer]], [[Dan Kan]], C. Stover, _An $E_2$ model category structure for pointed simplicial spaces_, J. Pure and Applied Algebra 90 (1993) 137&#8211;152
{#DwyerKanStover}

and are reviewed in

* {#Bousfield} [[Aldridge Bousfield]], _Cosimplicial resolutions and homotopy spectral sequences in model categories_ Geometry and Topology, volume 7 (2003)





### For unbounded chain complexes
  {#ForUnboundedChainComplexes}

Influential precusor discussion of homotopy theory of unbounded chain complexes (introducing notions like K-projective and K-injective complexes):

* [[Nicolas Spaltenstein]], *Resolutions of unbounded complexes*, Compositio Mathematica **65** 2 (1988) 121-154 &lbrack;[numdam:CM_1988__65_2_121_0](http://www.numdam.org/item?id=CM_1988__65_2_121_0), [eudml:89885](https://eudml.org/doc/89885)&rbrack;

The observation that from this one obtains a model category structure on unbounded chain complexes is due to:

* {#Hinich97} [[Vladimir Hinich]],  *Homological algebra of homotopy algebras*, Communications in Algebra **25** 10   (1997) 3291-3323 &lbrack;[arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), [doi:10.1080/00927879708826055](https://doi.org/10.1080/00927879708826055), Erratum: [arXiv:math/0309453](http://arxiv.org/abs/math/0309453)&rbrack;

and maybe independently due to:

* {#HoveyPalmieriStrickland97} [[Mark Hovey]], [[John Palmieri]], [[Neil Strickland]],  after theorem 9.3.1 in: *Axiomatic stable homotopy theory*, Memoirs Amer. Math. Soc. **610** (1997) &lbrack;[ISBN:978-1-4704-0195-5](https://bookstore.ams.org/memo-128-610), [pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/axiomatic.pdf)&rbrack;

(where the relevant insights are credited to [Weibel (1994)](https://ncatlab.org/nlab/show/homological+algebra#Weibel94))

and shown to be [[cofibrantly generated model category|cofibrantly generated]] in:

* {#SchwedeShipley98} [[Stefan Schwede]], [[Brooke Shipley]], p. 7 of: *Algebras and modules in monoidal model categories*, Proc. London Math. Soc. **80** 2  (2000)  491-511  &lbrack;[arXiv:math/9801082](https://arxiv.org/abs/math/9801082), [doi:10.1112/S002461150001220X](https://doi.org/10.1112/S002461150001220X)&rbrack;

* {#Hovey99} [[Mark Hovey]], Thm 2.3.1 in: *[[Model Categories]]*, Mathematical Surveys and Monographs, **63** AMS (1999) &lbrack;[ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover)&rbrack;

and shown to be ([[cofibrantly generated model category|cofibrantly generated]] and in addition) [[proper model category|proper]] and [[monoidal model category|monoidal]] in:

* {#Strickland20} [[Neil Strickland]], *The model structure for chain complexes* &lbrack;[arXiv:2001.08955](https://arxiv.org/abs/2001.08955)&rbrack;


In the context of the [[Dold-Kan correspondence]] with the [[model structure on simplicial abelian groups]]:

* {#SchwedeShipley03} [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_, Algebr. Geom. Topol. **3** (2003) 287-334 &lbrack;[arXiv:math.AT/0209342](http://arxiv.org/abs/math.AT/0209342), [euclid:euclid.agt/1513882376](https://projecteuclid.org/euclid.agt/1513882376)&rbrack;


That the corresponding [[category of simplicial objects]] in unbounded chain complexes is thus a [[Quillen equivalence|Quillen equivalent]] [[simplicial model category]] is 

* {#RezkSchwedeShipley01} [[Charles Rezk]], [[Stefan Schwede]], [[Brooke Shipley]], Cor. 4.6 in: *Simplicial structures on model categories and functors*, American Journal of Mathematics **123** 3 (2001) 551-575  &lbrack;[arXiv:0101162](http://arxiv.org/abs/math/0101162), [jstor:25099071](https://www.jstor.org/stable/25099071)&rbrack;

Generalization to [[presheaves]] of chain complexes:

* {#Fausk06} [[Halvard Fausk]], *T-model structures on chain complexes of presheaves* &lbrack;[arXiv:math/0612414](https://arxiv.org/abs/math/0612414)&rbrack;

The article

* {#ChristensenHovey} [[Dan Christensen]], [[Mark Hovey]], _Quillen model structures for relative homological algebra_, Math. Proc. Cambridge Philos. Soc. **133** 2 (2002) 261-293 &lbrack;[arXiv:math/0011216](https://arxiv.org/abs/math/0011216), [doi:10.1017/S0305004102006126](https://doi.org/10.1017/S0305004102006126)&rbrack;

discusses model structures on unbounded chain complexes with generalized notions of epimorphisms induced from "projective classes". See also:

* [[Dan Christensen]], _Derived categories and projective classes_ , (2005) ([hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Christensen/derived))

Another approach is due to James Gillespie, using [[cotorsion pairs]].  An overview of this work is in

* {#HoveyOverview} [[Mark Hovey]], _Cotorsion pairs and model categories_, 2006 ([pdf](http://homepages.math.uic.edu/~bshipley/hovey.pdf))


Some generalizations and simplifications of the original approach are discussed in

* {#Gillespie} James Gillespie, _Kaplansky classes and derived categories_, 2007, [pdf](http://phobos.ramapo.edu/~jgillesp/updated%20qcsheaf.pdf)

Generalization to [[bicomplexes]]:

* {#MuroRoitzheim19} [[Fernando Muro]], [[Constanze Roitzheim]], *Homotopy Theory of Bicomplexes*, Journal of Pure and Applied Algebra **223** 5 (2019) 1913-1939 &lbrack;[arXiv:1802.07610](https://arxiv.org/abs/1802.07610), [doi:10.1016/j.jpaa.2018.08.007](https://doi.org/10.1016/j.jpaa.2018.08.007)&rbrack;



Finally a third approach to the unbounded case is discussed (in a context of [[mixed motives]]) in:

* [[Denis-Charles Cisinski]], [[Frédéric Déglise]], *Local and stable homological algebra in Grothendieck abelian categories*, Homology, Homotopy and Applications **11** 1 (2009) 219–260 &lbrack;[arXiv:0712.3296](http://arxiv.org/abs/0712.3296), [hha:1251832567](https://projecteuclid.org/journals/homology-homotopy-and-applications/volume-11/issue-1/Local-and-stable-homological-algebra-in-Grothendieck-abelian-categories/hha/1251832567.full)&rbrack;

* {#CisinskiDeglise09} [[Denis-Charles Cisinski]], [[Frédéric Déglise]], *Triangulated categories of mixed motives*, Springer Monographs in Mathematics, Springer (2019) &lbrack;[arXiv:0912.2110](http://arxiv.org/abs/0912.2110), [doi:10.1007/978-3-030-33242-6](https://doi.org/10.1007/978-3-030-33242-6)&rbrack;



A discussion of the homotopy theory of [[presheaves]] of unbounded chain complex is in

* {#Jardine03} [[J. F. Jardine]], _Presheaves of chain complexes_, K-theory 30.4 (2003): 365-420 ([pdf](https://pdfs.semanticscholar.org/360c/fd4eb76da956e0c8dd897377f6d6f342e44e.pdf), [[JardinePresheavesOfChainComplexes.pdf:file]])

A model structure on noncommutative [[dg-algebra]]s whose proof strategy is useful also for cochain complexes is in

* [[J. F. Jardine]], _[[JardineModelDG.pdf:file]]_, Cyclic Cohomology and Noncommutative Geometry, Fields Institute Communications **17**, AMS (1997) 55-58.


[[!redirects model structures on chain complexes]]

[[!redirects model structure on cochain complexes]]
[[!redirects model structures on cochain complexes]]

[[!redirects model structure on connective chain complexes]]
[[!redirects model structures on connective chain complexes]]


[[!redirects model structure on unbounded chain complexes]]
[[!redirects model structures on unbounded chain complexes]]

[[!redirects projective model structure on chain complexes]]
[[!redirects projective model structures on chain complexes]]

[[!redirects injective model structure on chain complexes]] 
[[!redirects injective model structures on chain complexes]] 

[[!redirects injective model structure on connective cochain complexes]]

[[!redirects projective model structure on unbounded chain complexes]]
[[!redirects projective model structures on unbounded chain complexes]]

[[!redirects injective model structure on unbounded chain complexes]]
[[!redirects injective model structures on unbounded chain complexes]]

[[!redirects model category of chain complexes]]
[[!redirects model categories of chain complexes]]

