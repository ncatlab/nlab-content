
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Abstract

For $T$ any abelian [[Lawvere theory]], we establish a [[simplicial Quillen adjunction]] between model category structures on cosimplicial $T$-algebras and on simplicial presheaves over duals of $T$-algebras. We find mild general conditions under which this descends to the local model structure that models $\infty$-stacks over duals of $T$-algebras. In these cases the Quillen adjunction models the localization 

$$
  \mathbf{L} \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow} \mathbf{H} = Sh_{(\infty,1)}(C \subset T Alg^{op})
$$

of the $(\infty,1)$-topos of $(\infty,1)$-sheaves over duals of $T$-algebras at those morphisms that induce isomorphisms in cohomology with coefficients the canonical $T$-line object. In as far as objects of $\mathbf{H}$ have the interpretation of [[∞-Lie groupoid]]s the objects of $\mathbf{L}$ have the interpretatin of [[∞-Lie algebroid]]s.

For the special case where $T$ is the theory of ordinary commutative algebras this reproduces the situation of ([To&#235;n](#Toen)) and many statements are straightforward generalizations from that situation. For the case that $T$ is the theory of _[[smooth algebra]]s_ ($C^\infty$-rings) we obtain a refinement of this to the context of synthetic differential geometry. 

As an application, we show how Anders Kock's simplicial model for synthetic combinatorial differential forms finds a natural interpretation as the differentiable $\infty$-stack of infinitesimal paths of a manifold. This construction is an $\infty$-categorical and synthetic differential resolution of the _de Rham space_ functor introduced by Grothendieck for the cohomological description of flat connections. We observe that also the construction of the $\infty$-stack of modules lifts to the synthetic differential setup and thus obtain a notion of synthetic $\infty$-vector bundles with flat connection.


## Models for $\infty$-stacks and their function algebras {#Models}


### Cosimplicial $T$-algebras

A good general notion of function algebras on generalized [[space]]s are $T$-algebras, for $T$ a [[Lawvere theory]]. A good general notion of function algebras on [[internal ∞-groupoid]]s in such spaces are [[cosimplicial object|cosimplicial]] $T$-algebras.

We recall some basics and then discuss a [[model category]] structure on cosimplicial $T$-algebras for the cases that $T$ contains the theory of [[abelian group]]s.

#### $T$-Algebras {#TAlgebras}

A [[Lawvere theory]] may be thought of as a generalization of the theory of ordinary [[associative algebra]]s. 

A Lawvere theory is encoded in its [[syntactic category]] $T$, which by definition is a category with finite [[product]]s such that every object (isomorphic to) an integer multiple $x^k$ of a fixed object $x \in T$. We are to think of the [[hom-set]] $T(k,1)$ as the set of $k$-ary operations of the algebras defined by the theory. A **$T$-algebra** is accordingly a product-preserving functor $A : T \to Set$. Its image $U_T(A) := A(1) \in Set$ is the underlying set, and its value $A(f) : U_T(A)^k \to U_T(A)$ on an element $f \in T(k,1)$ is the $k$-ary operation $f$ as implemented by $A$.

The category of $T$-algebras is the [[full subcategory]] $T Alg \subset [T, Set]$ of the [[category of presheaves]] on $T^{op}$ on these product-preserving functors.

**Examples**. 

* The category $T = \mathcal{Ab}$ of free finitely generated abelian groups is the syntactic category of the Lawvere theory whose algebras are abelian groups.

* For $k$ a field, the category $T = k$ of free finitely generated $k$-algebras is the Lawvere theory whose algebras are $k$-[[associative algebra]]s;

* The category $T = $ [[CartSp]] is the syntactic category whose algebras are [[smooth algebra]]s.

A morphism of Lawvere theories $T_1 \to T_2$ is again a product-preserving functor.

+-- {: .un_defn}
###### Definition

An **abelian Lawvere theory** $T$ is a morphism of Lawvere theories $ab_T : \mathcal{Ab} \to T$.

=--

For $T$ abelian, $T$-algebras have an underlying [[abelian group]], given by the functor

$$
  ab_T^* : T Alg \to Ab
  \,.
$$

This functor is a [[right adjoint]].

For example associative algebras and smooth algebras are algebras over an abelian Lawvere theory, and their underlying abelian groups are the evident ones.

Similarly, the forgetful functor $U_T : T Alg \to Set$ has a [[left adjoint]], the free $T$-algebra functor $F_T : Set \to T Alg$. By the [[Yoneda lemma]] this sends the $n$-element set $(n)$ to $F_T(n) : k \mapsto T(n,k)$.

More generally, for any $A \in T Alg$ the copresheaf

$$
  T Alg(F_T(-), A) : T \to Set
$$

is isomorphic to $A$.

The free $T$-algebra $F_T(1)$ on a single generator may be thoigh of as the $T$-algebra of functions on the  **$T$-line**. For instance

* for $T = k$ we have that $F_T(1) = k[X]$ is the free $k$-algebra on a single generator $X$;

* for $T = CartSp$ we have that $F_T(1) = C^\infty(\mathbb{R})$.

We say more on the canonical $T$-line object below in [The Line object](#Line)

#### Model structure on cosimplicial $T$-algebras {#ModelTAlg}

+-- {: .un_theorem}
###### Theorem

There is a [[cofibrantly generated model category|cofibrantly generated]] [[model structure on cosimplicial abelian groups]] $Ab^\Delta_{proj}$ whose weak equivalences are the morphism that induce [[quasi-isomorphism]] under passage to [[Dold-Kan correspondence|normalized cochain complexes]] and fibrations are the degreewise surjections.  

With respect to the [canonical sSet-enrichment](#Enrichment) of the [[category of cosimplicial objects]] $Ab^{\Delta}$, this
is a [[simplicial model category]].

For $ab_T : \mathcal{Ab} \to T$ any abelian Lawvere theory, the [[adjunction]]

$$
  ((ab_*)^\Delta \dashv (ab^*)^\Delta ) 
   : T Alg^{\Delta} \stackrel{\overset{ab_*}{\leftarrow}}{\underset{ab^*}{\to}} Ab^\Delta
$$

induces a [[transferred model structure]] $T Alg^{\Delta}_{proj}$ on the category of cosimplicial $T$-algebras, whose weak equivalences and fibrations are those morphisms that under $(ab^*)^\Delta$ become weak equivalences and fibrations, respectively, in $Ab^\Delta_{proj}$.

This, too, is a [[simplicial model category]] with respect to its [standard sSet-enrichment](#Enrichment).

=--

+-- {: .proof}
###### Proof

The simplicial enrichment of $Ab^\Delta_{proj}$ is discussed at [[model structure on cosimplicial abelian groups]]. We here give the proof of the transferred simplicial model structure on $T Alg^\Delta_{proj}$.

By the facts recalled at [[transferred model structure]], we need to check that $T Alg^\Delta_{proj}$ 

* has a fibrant replacement functor;

* has functorial [[path space object]]s for fibrant objects

and for the simplicial enrichment that

* $(ab^*)^\Delta$ preserves the [[power]]ing.

The first condition is trivial, since all objects are fibrant. The last condition is evidently satisfied, since 

$$
  U(A^S)_n = U(\prod_{S_n} A_n) = \prod_{S_n} U(A_n) = ((U(A))^S)_n
  \,.
$$

Using this, we claim that we can take the path space object functor to be given by [[power]]ing with the simplicial interval

$$ 
 (-)^I : A \mapsto A^{\Delta[1]}
 \,.
$$

This is because $\Delta[0] \coprod \Delta[0] \hookrightarrow \Delta[1] \to \Delta[0]$ factors the co-diagonal in $sSet_{Quillen}$ by a cofibration followed by a weak equivalence between cofibrant objects. Accordingly the induced

$$
  A \to A^I \to A \times A 
$$

factors the digonal, and the morphism on the left is a weak equivalence, since it is the image under the left Quillen functor $A^{(-)}$ of a weak equivalence between cofibrant objects (and by the [[factorization lemma]] such weak equivalences are preserved by left Quillen functors).

=--



### Simplicial presheaves on duals of $T$-algebras

A good notion of a generalized [[space]] modeled on objects in a category $C$ is a [[nLab:sheaf]] on $C$. A good notion of an [[nLab:∞-groupoid]] in such generalized spaces is an [[nLab:(∞,1)-sheaf]] on $C$. Such objects are modeled by the [[nLab:model structure on simplicial presheaves]] on $C$.

We are interested here in that case that 

$$
  C \hookrightarrow T Alg^{op}
$$ 

is a [[small category|small]] [[full subcategory]] of the [[nLab:opposite category]] of $T$-algebras, for $T$ an abelian Lawvere theory. In the remainder of this section we assume such a choice to be fixed. Below in the section on [Examples and applications](#Examples) we discuss concrete choices of interest.

Notice that such a choice induces also a full subcategory of (co)simplicial objects

$$
  C^{\Delta^{op}} \hookrightarrow (T Alg^\Delta)^{op}
  \,.
$$


#### The prolonged Yoneda embedding {#ProlongedYoneda}

Write

$$
  j : T Alg^{op} \to [C^{op}, Set]
$$

for the ordinary [[nLab:Yoneda embedding]] and

$$
  j : (T Alg^\Delta)^{op} \to [C^{op}, sSet]
$$

for its degreewise simplicial prolongation 

$$
  j(A) : (B \in T Alg)  \mapsto ([n] \mapsto T Alg(A_n, B))
  \,.
$$


+-- {: .un_lemma}
###### Lemma
{#simplicialYoneda}

For $B \in T Alg$ and $(T Alg^\Delta)_s$ denoting the [simplicially enriched](#Enrichment) category of $T$-algebras, we have a natural identification

$$
  j(A) \simeq (T Alg^\Delta)^{op}_s(-, A) 
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using [[nLab:end]]/[[nLab:coend]]-calculus for handling the [canonical enrichment](#Enrichment) of $T Alg^\Delta$, we have
for $B \in T Alg^{op} \hookrightarrow (T Alg \Delta)^{op}$
and $A \in (T Alg^\Delta)^{op}$ [[nLab:natural transformation|natural]] isomorphisms

$$
\begin{aligned}
  (T Alg^\Delta)^{op}_s(B, A)_n
  & :=
  (T Alg^\Delta)^{op}(B \cdot \Delta^n, A)
  \\
  & \simeq \int_{k \in \Delta} T Alg(A_k, \prod_{\Delta(k,n)} B)
  \\
  & \simeq \int_{k \in \Delta} T Alg(\Delta(k,n)\cdot A_k, B)
  \\
  & \simeq T Alg( \int^{k \in \Delta} \Delta(k,n) \cdot A_k, B)
  \\
  & \simeq T Alg(A_n , B)
  \,,
\end{aligned}
$$

where in the last step we used the [[nLab:Yoneda lemma]] in its
coend-form (the [[nLab:co-Yoneda lemma]]).

=--



#### The line object


Recall from [above](#TAlgebras) that we write $F_T(*)$ for the free $T$-algebra on a single generator. 

+-- {: .un_def}
###### Definition

We call $R := j(F_T(*))$ the **line object** in $[C^{op}, sSet]$. 

=--

+-- {: .un_lemma}
###### Observation

As a presheaf, the line object $R$ sends a $T$-algebra $B \in T Alg$ to its underlying set $U_T(B)$

$$
  R : B \mapsto T Alg(F_T(*), B) \simeq Set(*, U_T(B)) \simeq U_T(B)
  \,.
$$

=--

This characterization may look simpler, but does not capture the important fact that homming into $R$ produces _$T$-algebras of functions_ . This is what the following definition deals with.


+-- {: .un_def}
###### Definition
**($T$-algebras of functions)**

For $X \in [C^{op}, sSet]$, the [[nLab:cosimplicial set]] 

$$
  U_T(\mathcal{O}(X)) := [C^{op},sSet](X_\bullet, R) \in Set
$$

we call the cosimplicial set of $R$-valued _functions_ on $X$. This is naturally the cosimplical set underlying the cosimplicial $T$-algebra

$$
  \mathcal{O}(X) : (k \in T) \mapsto [C^{op},sSet](X_\bullet, j(F_T(k)))
  \,.
$$

We call $\mathcal{O}(X) \in T Alg^{op}$ the **$T$-algebra of functions** on $X$. This extends to a functor

$$
  \mathcal{O} : [C^{op}, sSet] \to (T Alg^{\Delta})^{op}
  \,.
$$
 
=--

In the next section we see that $(\mathcal{O} \dashv j)$ forms a [[simplicial Quillen adjunction]].



#### Model structure on simplicial presheaves {#ModelPresheaves}

Write $[C^{op}, sSet]_{proj}$ for the global projective [[model structure on simplicial presheaves]] over $C$. With the simplicial enrichment $[C^{op}, sSet]_s$ this is naturally a [[simplicial model category]].

Let $S \subset mor [C^{op}, sSet]$ be a class of [[hypercover]]s. 

+-- {: .un_def}
###### Definition

Write $[C^{op}, sSet]_{proj,loc}$ for the 
[[left Bousfield localization]] $[C^{op}, sSet]_{proj}$ at this class.

=--

By general results on Bousfield localization, this exists always for $S$ a [[small set]], notably for $f$ the set of [[Cech nerve]] projections $C(U) \to X$ for [[cover]]s $\{U_i \to X\}$ of the [[Grothendieck topology]] on $C$. By general results on the [[local model structure on simplicial presheaves]], the localization also exists for $S$ the class of all hypercovers. 

(...)

### The Yoneda-Quillen-adjunction

We relate now the [model structure on cosimplicial T-algebras](#ModelTAlg) with the [model structure on simplicial presheaves](#ModelPresheaves) over $C \subset T Alg^{op}$ using the [function algebra functor](#Line) $\mathcal{O}$ and the [prolonged Yoneda embedding](#ProlongedYoneda) $j$.

+-- {: .un_theorem}
###### Theorem

The functors $j$ and $\mathcal{O}$ constitute an [[simplicial Quillen adjunction]] 

$$
  (\mathcal{O} \dashv j) : 
  (TAlg^\Delta_{proj})^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{j}{\hookrightarrow}}
  [C^{op}, sSet]_{proj}
  \,.
$$


=--

+-- {: .proof}
###### Proof

We first establish the [[nLab:adjunction]] itself: using [[nLab:end]]-calculus for expressing [[nLab:hom-set]]s in [[nLab:functor category|functor categories]] we have for $X \in [C^{op}, sSet]$ and $A \in T Alg^\Delta$ [[nLab:natural transformation|natural]] isomorphisms

$$
\begin{aligned}
  (T Alg^\Delta)^{op}(\mathcal{O}(X), A)
  & :=
  (T Alg^\Delta)^{op}(A(-), [C^{op}, sSet](X, j(F_T(-))))
  \\
  & \simeq
  \int_{k \in T} \int_{[n] \in \Delta}
  Set(A_n(k), [C^{op}, Set](X_n, j( F_T(k)) ))
  \\
  & \simeq
  \int_{k \in T} \int_{[n] \in \Delta} \int_{B \in C}
  Set(A_n(k), Set(X_n(B), T Alg(F_T(k), B)))
  \\
  & \simeq
  \int_{k \in T} \int_{[n] \in \Delta} \int_{B \in C}
  Set(A_n(k), Set(X_n(B), B(k)))
  \\
  & \simeq
  \int_{k \in T} \int_{[n] \in \Delta} Set(X_n(B), \int_{k \in T}
   Set(A_n(k), B(k))
  )
  \\
  & \simeq
  \int_{k \in T} \int_{[n] \in \Delta} Set(X_n(B), T Alg(A_n, B))
  \\
  & \simeq
  [C^{op}, sSet](X, j(A))
  \,.
\end{aligned}
 \,,
$$

where the crucial step is the isomorphism $B(-) \simeq T Alg(F_T(-), B)$ for the line object discussed [above](#Line). 

That this lifts to an $sSet$-enriched adjunction follows with the [prolonged Yoneda lemma](#ProlongedYoneda) $j(A) \simeq (T Alg^\Delta)^{op}_s(-,A)$ and the $sSet$-[[nLab:tensoring]] and [[nLab:cotensoring]] of $[C^{op}, sSet]_s$ and $(T Alg^\Delta)^{op}_s$:

$$
  \begin{aligned}
    (T Alg^\Delta)^{op}_s(\mathcal{O}(X), A)_n
    &
    := 
    (T Alg^\Delta)^{op}(\mathcal{O}(X), A^{\Delta^n})
    \\
    & \simeq
    [C^{op}, sSet](X, j(A^{\Delta_n}))
    \\
    & \simeq   [C^{op}, sSet](X, (T Alg^\Delta)^{op}_s(-,A^{\Delta^n}))
    \\
    & \simeq   \int_{B \in C} sSet(X(B), (T Alg^\Delta)^{op}_s(B,A^{\Delta^n})))
    \\
    & \simeq   \int_{B \in C} sSet(X(B), (T Alg^\Delta)^{op}_s(B \cdot \Delta^n,A)))
    \\
    & \simeq   \int_{B \in C} sSet(X(B)\times \Delta^n , (T Alg^\Delta)^{op}_s(B,A)))
   \\
    & \simeq
    [C^{op}, sSet](X \cdot \Delta^n, j(A))
    \\
    & =: [C^{op}, sSet]_n(X, j(A))_n
    \,.
  \end{aligned}
$$

By the pushout-product axiom satisfied by the $sSet$-[[nLab:enriched model category]] $(T Alg^\Delta)_s$ and using that in $(T Alg^\Delta_{proj})^{op}$ every object $B$ is cofibrant, we have that for $f : A_1 \to A_2$ a fibration (acyclic fibration) in $(T Alg^\Delta_{proj})^{op}$ and for $B \in C \subset T Alg^{op}$ any object, the morphism $j(A_1 \to A_2)(B) = (T Alg^{\Delta})^{op}_s(B,f)$ is a fibration (acyclic fibration) in $sSet$. Therefore $j(f)$ is a fibration (acyclic fibration) in $[C^{op}, sSet]_{proj}$.

This establishes that $j$ is a right Quillen functor and completes the proof.

=--


The following theorems say that the obstructions to making this Quillen adjunction descent to [[nLab:local model structures on simplicial presheaves]] are mild.

+-- {: .un_prop}
###### Proposition

Let $J$ be a [[subcanonical coverage]] on $C \subset (TAlg^\Delta)^{op}$, $X \in Ob(C)$ and $f : Y \to j(X)$ a [[hypercover]] with respect to $J$.

Then for $i \gt 1$ we have that $f$ induces an isomorphism in $R$-cohomology in degree $i$: $H^i(\mathcal{O}(f))$ is an [[nLab:isomorphism]].

=--


+-- {: .proof}
###### Proof

(...)

=--



+-- {: .un_theorem}
###### Theorem

If for all (hyper-)covers $f \in S$ we have that $H^0(\mathcal{O}(f))$ and  $H^1(\mathcal{O}(f))$ are isomorphisms then $(\mathcal{O} \dashv j)$ is a [[simplicial Quillen adjunction]] to the [[local model structure on simplicial presheaves]].

$$
  (\mathcal{O} \dashv j) : 
  (TAlg^\Delta_{proj})^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{j}{\hookrightarrow}}
  [C^{op}, sSet]_{proj, loc}
  \,.
$$


=--


+-- {: .proof}
###### Proof

By the previous proposition we have that under the given assumptions every (hyper-)cover $f : Y\to X $ in $[C^{op}, sSet]$ is taken by $\mathcal{O}$ to a weak equivalence.

Using this we can follow the remainder of the argument of [To&#235;n, prop. 2.2.2](#Toen):

Since the [[model structure on simplicial presheaves]] is a [[left proper model category]] and since [[left Bousfield localization]] preserves left properness, we have that $[C^{op}, sSet]_{proj,loc}$ is [[proper model category|left proper]]. Since moreover left Bousfield localization does not change the class of cofibrations, we know that $\mathcal{O}$ still preserves cofibrations.

Then by the <a href="http://ncatlab.org/nlab/show/simplicial+Quillen+adjunction#Recognition">recognition theorem for simplicial Quillen adjunction</a> it is sufficient to check that $j$ sends fibrant objects $A \in (T Alg^\Delta_{proj})^{op}$ to [[local object]]s with respect to the morphisms $f$.

Since by definition of hypercovers, their domain and codomain is cofibrant (codomain because it is a representable, domain by assumption that it is a degreewise coproduct of representables with disjoint degeneracies, see the discussion of cofibrancy in the projective structure at [[model structure on simplicial presheaves]]), this means that it is sufficient to check that for all $f$ and fibrant $c$ we have that $[C^{op}, sSet]_s(f, j(c))$ is a weak equivalence. But by the adjunction $(\mathcal{O} \dashv j)$ this is isomorphically $(T Alg^\Delta)^{op}(\mathcal{O}(f), c)$. 

Now by the above propositions and assumptions, we have that $\mathcal{O}(f)$ is a weak equivalence. Since all objects in $(T Alg^\Delta_{proj})^{op}$ are cofibrant, it is a weak equivalence between cofibrant objects.  With the [[factorization lemma]] it follows that in an [[enriched model category]] the enriched hom of a weak equivalence into a fibrant object is a weak equivalence.

=--


+-- {: .un_theorem}
###### Proposition

When restricted along $C^{\Delta^{op}} \subset (T Alg^\Delta)^{op}$ the functor $j$ is _homotopy full and faithful_ in that for all $A \in C^{\Delta^{op}}$ we have that the canonical morphism

$$
  A \to \mathbb{L}\mathcal{O} \; \mathbb{R}j \; A
$$

into the image of the [[derived functor]]s of $j$ and $\mathcal{O}$ is an [[isomorphism]] in the [[homotopy category]] $Ho(T Alg^\Delta_{proj})$.

=--

+-- {: .proof}
###### Proof

With the above results, this follows verbatim as the proof of the analogous  ([To&#235;n, corollary 2.2.3](#Toen)).

=--

##  Localization of the $(\infty,1)$-topos at $R$-cohomology


In this section we discuss that in terms of the [[(∞,1)-category theory]] 
that is [[presentable (∞,1)-category|presented]] by the model category theoretic structures [above](#Models), these serve to establish the following intrinsic statement.

+-- {: .un_theorem}
###### Theorem

The Quillen adjunction $(\mathcal{O} \dashv j)$ is a [[nLab:presentable (∞,1)-category|presentation]] of the [[reflective sub-(∞,1)-category]]

$$
  \mathbf{L}(C) \stackrel{\stackrel{\mathcal{O}}{\leftarrow}}{\hookrightarrow}
  Sh_{(\infty,1)}(C)
$$

of the [[nLab:(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(C)$ which is the [[nLab:localization of an (∞,1)-category|localization]] at those morphisms that induce isomorphisms in $R$-cohomology, for $R$ the [canonical T-line object](#Line).

Here $\mathbf{L}(C)$ is the full [[sub-(∞,1)-category]] of $((T Alg^\Delta_{proj})^{op})^\circ$ on those objects in the homotopy-essential image of the inclusion $C^{\Delta^{op}} \to (T Alg^\Delta)^{op}$.

=--


### $R$-Cohomology

Since the $T$-line $R \in [C^{op}, sSet]$ canonically has the structure of an [[abelian group]] in $[C^{op}, sSet]$. As such it presents a 0-[[truncated]] [[∞-group]] in $Sh_{(\infty,1)}(C)$, and so we may consider its [[Eilenberg-MacLane object]]s $\matbf{B}^n R$ for $n \in \mathbb{N}$.


Write $\Xi : Ch^\bullet_+ \to Ab^\Delta$ for the dual [[Dold-Kan correspondence]] map. Notice that $F_{Ab}(*) = \mathbb{Z}$, the free abelian group on a single generator. Write $F_{Ab}(*)[n]$ for the [[cochain complex]] concentrated in degree $n$ on $F_{Ab}(*)$. For $ab_* : Ab \to T Alg$ the left adjoint to the underlying abelian group functor $ab^* : T Alg \to Ab$ we have then thagt $ab_* \Xi (F_{Ab}(*)[n])$ is the cosimplicial $T$-algebra which in degree $k$ is a product of copies of the free $T$-algebra corresponding to the product of copies $\mathbb{Z}$ in $\Xi \mathbb{Z}[n]$.


We claim that 
$$
  \mathbf{B}A \simeq j(ab_* \Xi(F_{Ab}(*)[n])
$$

**Proposition**

For $X \in [C^{op}, sSet]$, the [[cohomology|intrinsic cohomology]] $H(X, \mathbf{B}^n R)$ with coefficients in $R$ is the [[cochain cohomology]] $H^n(\mathbb{L}\mathcal{O}(X))$ of the cochain complex  of its cosimplicial function algebra.

Proof.

Notice that $ab_* \Xi(F_{Ab}(*)[n]$ is fibrant in $(T Alg^\Delta_{proj})^{op}$. Then


$$
  \begin{aligned}
    H(X,\mathbf{B}^n R)
    & =
    Ho_{[C^{op}, sSet]_{proj}}(X, j(ab_* \Xi(F_{Ab}(*)[n]))
    \\
    & \simeq
    Ho_{(T Alg^\Delta_{proj})^{op}}(\mathbb{L}\mathcal{O}(X), 
     ab_* \Xi(F_{Ab}(*)[n])
    \\
    & \simeq
    Ho_{(T Alg^\Delta_{proj})}( 
        ab_* \Xi(F_{Ab}(*)[n]),
       \mathbb{L}\mathcal{O}(X)
    )
    \\
    & \simeq 
    Ho_{(T Alg^\Delta_{proj})}( 
        \Xi(F_{Ab}(*)[n]),
       ab^* \mathbb{L}\mathcal{O}(X)
    )
    \\
    & \simeq 
    Ho_{Ch^\bullet}( 
        F_{Ab}(*)[n],
       N^\bullet ab^* \mathbb{L}\mathcal{O}(X)
    )
    \\
    & =
    Ho_{Ch^\bullet}( 
        \mathbb{Z}[n],
       N^\bullet ab^* \mathbb{L}\mathcal{O}(X)
    )
    \\
    & \simeq
    H^n(\mathbb{L}\mathcal{O}(X))
  \end{aligned}
$$

(...)

### $R$-Local objects

(...)


## Examples and applications {#Examples}


+-- {: .un_prop}
###### Proposition (Examples)

The conditons of the above theorem are satisfied for instance for

* $T$ the theory of ordinary commutative algebras over a field $k$ and $J$ the xyz-topology.

  In this case the adjunction is that considered in ([To&#235;n](#Toen)).

* $T$ the theory of [[nLab:smooth algebra]]s and $C \hookrightarrow T Alg^{op}$ the [[site]] of the [[Cahiers topos]]. This is what we discuss in more detail below.

=--

### Rational homotopy theory

$T$ the Lawvere theory of $\mathbb{Q}$-algebras. Then $(\mathcal{O} \dashv j)$ reproduces the setup discussed at [[rational homotopy theory in an (∞,1)-topos]].

### $\infty$-Lie theory

$T = $ [[CartSp]] the ([[syntactic category]] of the) Lawvere theory of [[smooth algebra]]s. A [[Fermat theory]]. $C \subset CartSp Alg$ the [[site]] for the [[Cahiers topos]].

#### The infinitesimal path $\infty$-groupoid of a manifold

(...)



For $U \in CartSp$ let

$$
   U^{\Delta^\bullet_{inf}} \in C^{\Delta^{op}}
$$

be the simplicial object of <a href="http://ncatlab.org/nlab/show/infinitesimal%20object#SpacOfInfSimpl">infinitesimal simplices</a> in $U$.

**Definition**

We call

$$
  \mathbf{\Pi}_{inf}(U)
  :=
  \mathbb{R}j\; (U^{\Delta^\bullet_{inf}})
  \in 
  [C^{op}, sSet]
$$

the infinitesimal path $\infty$-Lie groupoid of $U$.

(...)

#### The tangent category of smooth algebras

(...)

The [[tangent category]] of the category of [[smooth algebra]]s is the category of modules over $C^\infty$-rings. 

**Proposition** This abstract definition of module over $C^\infty$-rings reproduces the definition given by Kock.

The tangent category of the category of _simplicial_ $C^\infty$-rings is ...

This serves the purpose of presenting the $\infty$-stack of $\infty$-vector bundles on $T Alg^{op}$.

(...)


### $\infty$-Lie algebra cohomology

(...)

Passing along the embedding $\mathbf{L} \hookrightarrow \mathbf{H}$ we may compute [[∞-Lie algebra cohomology]] in $\mathbf{H}$.

(...)

## Function algebra on derived $\infty$-stacks

In a higher categorical context, it is unnatural to constrain the site $T Alg^{op}$ to be a 1-category, as so far we do above. A complete $(\infty,1)$-category theoretic setup would replace the [[algebraic theory]] $T$ with an [[(∞,1)-algebraic theory]], let $T Alg_{(\infty,1)}$ be its [[(∞,1)-category]] of algebras and equip $C \subset T Alg_{(\infty,1)}$ with the structure of an [[(∞,1)-site]].

In an intermedite step, if $T$ remains an ordinary algebraic theory, but is regarded as an $(\infty,1)$-algebraic theory, its $(\infty,1)$-algebras $A \in T Alg_{(\infty,1)}$ are typically modeled by _simplicial_ $T$-algebras . In that case the above setup produces an adjunction between simplicial presheaves on duals of simplicial algebras, and cosimplicial simplicial algebras.

For $T$ the theory of ordinary commutative algebras, this yields a derived extension of Toen's setup that has been considered in ([BenZvi-Nadler2010](#BenZviNadler)). For $T$ the theory of smooth algebras, simplicial $T$-algebras are the objects studied in ([Spivak](#Spivak)) as models for [[derived smooth manifold]]s.




## Appendix

### Enrichment of categories of simplicial objects {#Enrichment}

We recall some basic facts on [[sSet]]-[[enriched category|enriched]] [[categories of simplicial objects]].

+-- {: .un_defn}
###### Definition

Let $D$ be a [[nLab:category]] with all [[nLab:limit]]s and [[nLab:colimit]]s. This implies that it is [[nLab:copower|tensored]] over [[nLab:Set]]

$$
  \cdot : D \times Set \to D
  \,.
$$

This induces a functor

$$
  \cdot^{\Delta^{op}} : D^{\Delta^{op}} \times sSet \to D^{\Delta^{op}}
$$

which we shall also write just "$\cdot$".

For $X,Y \in D^{\Delta^{op}}$ write

$$
  D^{\Delta^{op}}(X,Y) := Hom_{D^{\Delta^{op}}}(X \cdot \Delta[\bullet], Y)
  \in sSet
$$

and for $X,Y,Z \in D^{\Delta^{op}}$ let

$$
  D^{\Delta^{op}}(X,Y)
    \times  
  D^{\Delta^{op}}(Y,Z)
  \to 
  D^{\Delta^{op}}(X,Z)
$$

be given in degree $n$ by

$$
  (X \cdot \Delta[n] \to Y, Y \cdot \Delta[n] \to Z)
  \mapsto
  ( X \cdot \Delta[n] \to X \cdot \Delta[n]\times \Delta[n] \to Y \cdot \Delta[n]  \to Z)
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

With the above definitions $D^{\Delta^{op}}$ becomes an [[nLab:sSet]]-[[nLab:enriched category]] which is both [[nLab:copower|tensored]] as well as [[nLab:power|cotensored]] over $sSet$.

=--

+-- {: .un_def}
###### Definition

We regard $D^{\Delta}$ as an $sSet$-enriched category by 

$$
  D^{\Delta} \simeq ({D^{op}}^{\Delta^{op}})^{op}
  \,.
$$

=--


+-- {: .un_example}
###### Example

For $X \in [C^{op}, sSet]$ and $S \in sSet$ we have that the tensoring is given by

$$
  X \cdots S : (U \in C) \mapsto X(U) \times S 
  \,.
$$

=--

+-- {: .un_example}
###### Example

For $A \in (T Alg^{\Delta})^{op}$ and $S \in sSet $ we have that the tensoring is given by

$$
  (A \cdot S)_n
  =
  \prod_{S_s} A \in T Alg
  \,,
$$

with the [[nLab:product]] taken in $T Alg$.

=--



### Model structure on cosimplicial abelian groups

(...)

See [[nLab:model structure on cosimplicial abelian groups]].

(...)

## References

The Quillen adjunction over abelian $T$-algebras that we consider generalizes that discussed in 

* [[nLab:Bertrand Toën]], _Champs affine_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))
{#Toen}

over ordinary commutative $k$-algebras. See also [[rational homotopy theory in an (infinity,1)-topos]].

The generalization to arbitrary abelian $T$-algebras and the application to synthetic differential geometry is the content of 

* [[Herman Stel]], _Function algebras on $\infty$-stacks -- Synthetic differental $\infty$-groupoids_ , master thesis (2010) ([[schreiber:master thesis Stel|web]])

on which this entry here is based.

The considerations in 

* [[David Spivak]], _Derived smooth manifolds_  Duke Math. J. Volume 153, Number 1 (2010), 55-128. ([pdf](http://www.uoregon.edu/~dspivak/derived-smooth-manifolds.pdf))
{#Spivak}

on [[derived smooth manifold]]s may be considered as complementary to the approach taken here: there simplicial $C^\infty$-rings are considered, instead of cosimplicial ones. A fully comprehensive treatment of _derived synthetic differential geometry_ would consider the combination of both aspects: simplicial presheaves on duals of simplicial $C^\infty$-rings with a functor $\mathcal{O}$ taking them to cosimplicial-simplicial $C^\infty$-rings. 

For ordinary commutative algebras the generalizaton of Toen's setup to geometry over duals of simplicial algebras is used for instance in

* [[David Ben-Zvi]], [[David Nadler]], _Loop spaces and connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))
{#BenZviNadler}

[[!redirects function algebras on ∞-stacks]]