
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
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

For $T$ any abelian [[Lawvere theory]], here we discuss -- in a variation of the theme of [[Isbell conjugation]], in generalization of ([To&#235;n](#Toen)) and following ([Stel](#Stel)) --  a [[simplicial Quillen adjunction]] between model category structures on cosimplicial $T$-algebras and on simplicial presheaves over duals of $T$-algebras. We find mild general conditions under which this descends to the local model structure that models $\infty$-stacks over duals of $T$-algebras. In these cases the left adjoint of the Quillen adjunction is given by sending $\infty$-stacks to their cosimplicial $T$-algebras of functions with values in the canonical $T$-[[line object]], and the adjunction models small objects relative to a choice of a small full subcategory $T\subset C \subset T Alg^{op}$  of the localization 

$$
  \mathbf{L} \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow} \mathbf{H} = Sh_{(\infty,1)}(C )
$$

of the $(\infty,1)$-topos of $(\infty,1)$-sheaves over duals of $T$-algebras at those morphisms that induce isomorphisms in cohomology with coefficients the canonical $T$-[[line object]]. 

For the special case where $T$ is the theory of ordinary commutative algebras this reproduces the situation of ([To&#235;n](#Toen)) and many statements are straightforward generalizations from that situation. For the case that $T$ is the theory of _[[smooth algebra]]s_ ($C^\infty$-rings) we obtain a refinement of this to the context of synthetic differential geometry. In these cases, in as far as objects in $\mathbf{H}$ may be understood as [[∞-Lie groupoid]]s, the objects in $\mathbf{L}$ may be understood as [[∞-Lie algebroid]]s. 

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

The free $T$-algebra $F_T(1)$ on a single generator may be thought of as the $T$-algebra of functions on the  **$T$-line**. For instance

* for $T = k$ we have that $F_T(1) = k[X]$ is the free $k$-algebra on a single generator $X$;

* for $T = CartSp$ we have that $F_T(1) = C^\infty(\mathbb{R})$.

We say more on the canonical $T$-[[line object]] below in [The Line object](#Line)

#### Model structure on cosimplicial $T$-algebras {#ModelTAlg}

+-- {: .un_theorem}
###### Theorem
{#ModelTransferToTAlg}

There is a [[cofibrantly generated model category|cofibrantly generated]] [[model structure on cosimplicial abelian groups]] $Ab^\Delta_{proj}$ whose weak equivalences are the morphisms that induce [[quasi-isomorphism]] under passage to [[Dold-Kan correspondence|normalized cochain complexes]] and fibrations are the degreewise surjections.  

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

The proof of the existence of the [[model structure on cochain complexes]] in non-negative degree -- $Ch^\bullet_+(Ab)$ -- whose fibrations are the _degreewise surjections_ (and weak equivalences the usual [[quasi-isomorphism]])s is spelled out <a href="http://ncatlab.org/nlab/show/model+structure+on+chain+complexes#CochainNonNegProj">here</a>.

By the dual [[Dold-Kan correspondence]] $Ab^\Delta \simeq Ch^\bullet_+(Ab)$ this induces the [[model structure on cosimplicial abelian groups]] whose fibrations are the degreewise surjections (using that the [[Moore complex|normalized cochain complex functor]] sends surjections to surjections).

That with the standard structure of an [[sSet]]-[[enriched category]] on $Ab^\Delta$ this constitutes a [[simplicial model category]]-structure is proven <a href="http://ncatlab.org/nlab/show/model+structure+on+cosimplicial+abelian+groups#SimplicialEnrichmentOfProjective">here</a>.

Now we use the basic fact of [[Lawvere theories]] that any morphism $f : T_1 \to T_2$ of such induces a pair of [[adjoint functor]]s

$$
  (f_* \dashv f^*) : T_2 Alg \stackrel{\overset{f_*}{\leftarrow}}{\underset{f^*}{\to}}
  T_1 Alg
$$

between their categories of algebras: the <a href="http://ncatlab.org/nlab/show/Lawvere%20theory#AdjCatAlgs">adjunction of relatively free algebras</a>.

Since by assumption that our $T$ is an abelian Lawvere theory we are given a morphism $ab : Ab \to T$ from the theory of [[abelian group]]s, this means that we have an [[adjunction]] 

$$
  (ab_* \dashv ab^*) : T Alg \stackrel{\overset{ab_*}{\leftarrow}}{\underset{ab^*}{\to}}
  Ab
$$

and hence also an adjunction

$$
  (ab_*^\Delta \dashv (ab^*)^\Delta) : T Alg^\Delta \stackrel{\overset{}{\leftarrow}}{\underset{}{\to}}
  Ab^\Delta
  \,.
$$

We need to check that the [[right adjoint]] $(ab^*)^\Delta$ induces the [[transferred model structure]] on $T Alg^\Delta$ from the above model structure $Ab^\Delta_{proj}$. 

By the facts recalled at [[transferred model structure]], we need to check that $T Alg^\Delta_{proj}$ 

* has a fibrant replacement functor;

* has functorial [[path space object]]s for fibrant objects;

and for the simplicial enrichment that

* $(ab^*)^\Delta$ preserves the [[power]]ing.

The first condition is trivial, since all objects are fibrant. The last condition is evidently satisfied, since 

$$
  U_T(A^S)_n = U_T(\prod_{S_n} A_n) = \prod_{S_n} U_T(A_n) = ((U_T(A))^S)_n
  \,.
$$

Using this, we claim that we can take the path space object functor to be given by [[power]]ing with the simplicial [[interval]]

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
  T \subset C \hookrightarrow T Alg^{op}
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



#### The line object {#Line}

The adjunction that we shall be concerned with is essentially [[Isbell conjugation]]. We recall some basics of <a href="http://ncatlab.org/nlab/show/Isbell+conjugation#FunctionAlgebrasOnPresheaves">Function T-algebras on presheaves</a>.

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

Let $S \subset mor [C^{op}, sSet]$ be a class of [[split hypercover]]s. 

+-- {: .un_def}
###### Definition

Write $[C^{op}, sSet]_{proj,loc}$ for the 
[[left Bousfield localization]] $[C^{op}, sSet]_{proj}$ at this class.

=--

By general results on left Bousfield localization, this exists always for $S$ a [[small set]], notably for $f$ the set of [[Cech nerve]] projections $C(U) \to X$ for [[cover]]s $\{U_i \to X\}$ of the [[Grothendieck topology]] on $C$. By general results on the [[local model structure on simplicial presheaves]], the localization also exists for $S$ the class of all (split) hypercovers. 


### The Yoneda-Quillen-adjunction {#YonedaQuillenAdjunction}

We relate now the [model structure on cosimplicial T-algebras](#ModelTAlg) with the [model structure on simplicial presheaves](#ModelPresheaves) over $C \subset T Alg^{op}$ using the [function algebra functor](#Line) $\mathcal{O}$ and the [prolonged Yoneda embedding](#ProlongedYoneda) $j$.

+-- {: .un_theorem}
###### Theorem

The functors $j$ and $\mathcal{O}$ constitute a [[simplicial Quillen adjunction]] 

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
  T Alg^\Delta (A(-), [C^{op}, sSet](X, j(F_T(-))))
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

where the crucial step is the isomorphism $B(-) \simeq T Alg(F_T(-), B)$ for the line object discussed [above](#Line). This computation is just simplicial-degreewise the adjunction discussed at <a href="http://ncatlab.org/nlab/show/Isbell%20duality#FunctionAlgebrasOnPresheaves">Isbell duality -- Function T-algebras on presheaves</a>.

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

Let $J$ be a [[subcanonical coverage]] on $C \subset (TAlg^\Delta)^{op}$, $X \in Ob(C)$ and $f : Y \to j(X)$ a [[split hypercover]] with respect to $J$.

Then for $i \neq  1$ we have that $f$ induces an isomorphism in $R$-cohomology in degree $i$: $H^i(\mathcal{O}(f)) : H^i(\mathcal{O}(X)) \stackrel{\simeq}{\to} H^i(\mathcal{O}(Y))$ .

=--


+-- {: .proof}
###### Proof

Regard $f$ as a [[simplicial object]] in the [[overcategory]]

$$
  Sh(C)/X \simeq Sh(C/X)
  \,.
$$

Write 

$$
  \bar f \in Ab(Sh(C)/X)^{\Delta^{op}}
$$ 

for the degreewise free abelian group object of that, a simplicial object in the category of abelian group objects in the sheaf topos over $C$. The [[chain homology]] of the corresponding normalized chain complex vanishes in positive degree (as discussed <a href="http://ncatlab.org/nlab/show/hypercover#HypercoverHomology">here</a>):

$$
  H_{n \geq 1}(\bar f) = 0
  \,.
$$


Let now by the [[Freyd-Mitchell embedding theorem]]

$$
  i : Ab(Sh(C/Y)) \hookrightarrow R Mod
$$

be a [[full and faithful functor]] from the [[abelian category]] of abelian group object into the category of $R$-[[module]] over some ring $R$. 

Write $K \in R Mod$ for the canonical $T$-[line object](#Line) regarded first as the abelian group object $U_T(-) \times X \in Ab(Sh(C/X))$ and then injected with $i$ into $R Mod$.


Using this, the cochain cohomology $H^i(\mathcal{O}(Y_\bullet))$ that we are after is equivalently the cohomology of

$$
  \begin{aligned}
    \mathcal{O}(Y)
    & \simeq Sh(C)^\Delta(Y_\bullet, U_T(-))
    \\
    & \simeq Sh(C)/X(f_\bullet , U_T(-) \times X)
    \\
    & \simeq Ab(Sh(C)/X)( \bar f_\bullet, U_T(-)\times X)
    \\
    & \simeq R Mod( i(\bar f_\bullet), i(U_T(-) \times X) )
    \\
    & \simeq R Mod( i(\bar f_\bullet), K )
  \end{aligned}
  \,.
$$

To compute this, we use the [[universal coefficient theorem]], which says that we have an [[exact sequence]]

$$
  0 \to Ext^1(H_{n-1}(i(\bar f_\bullet), K))
  \to H^n(R Mod(i(\bar f_\bullet), K))
  \to Ab(H_n(i(\bar f_\bullet)), C)
  \to 0
  \,.
$$

By the above fact that the homology $H_n(i(\bar f))$ vanishes in positive degree, this gives finally that 

$$
  H^n(\mathcal{O}(Y))
$$

vanishes in degree $n \geq 2$. That it also vanishes in degree 0 is seen to be equivalent to the sheaf condition on $X$, which is true by the assumption that we are working with a [[subcanonical coverage]].

=--



+-- {: .un_theorem}
###### Theorem
**(passage to local model structure)**
{#PassageToLocalTheorem}

If for all split (hyper-)covers $f \in S$ we have that $H^1(\mathcal{O}(f))$ is an isomorphisms then $(\mathcal{O} \dashv j)$ is a [[simplicial Quillen adjunction]] to the [[local model structure on simplicial presheaves]].

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

The following proposition asserts that the Quillen adjunction that we have established is very special, in that it is the model-category theoretic analog of a [[reflective subcategory]]. Below in the section [Localization of the (∞,1)-topos at R-cohomology](#Intrinsic) we see that this indeed presents such a reflective inclusion in [[(∞,1)-category theory]].

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



##  Localization of the $(\infty,1)$-topos at $R$-cohomology {#Intrinsic}

In this section we discuss that in terms of the [[(∞,1)-category theory]] 
that is [[presentable (∞,1)-category|presented]] by the model category theoretic structures [above](#Models), these serve to establish the following intrinsic statement.

+-- {: .un_theorem}
###### Theorem

The Quillen adjunction $(\mathcal{O} \dashv j)$ is a [[nLab:presentable (∞,1)-category|presentation]] models $C$-small objects (...) the inthe [[reflective sub-(∞,1)-category]]

$$
  \mathbf{L}_C \stackrel{\stackrel{\mathcal{O}}{\leftarrow}}{\hookrightarrow}
  \mathbf{H}:=
  Sh_{(\infty,1)}(C)
$$

of the [[nLab:(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(C)$, where $\mathbb{L}_C$ is  the [[nLab:localization of an (∞,1)-category|localization]] at those morphisms that induce isomorphisms in intrinsic $R$-[[cohomology]], for $R$ the [canonical T-line object](#Line).

=--

We obtain a proof of this after the following discussions.

### $R$-Cohomology

Since $T$ is assumed to be an abelian Lawvere theory, the [T-line object](#Line) $R \in [C^{op}, sSet]$ canonically has the structure of an abelian [[group object]] in $[C^{op}, sSet]$. As such it presents a 0-[[truncated]] [[∞-group]] in the $Sh_{(\infty,1)}(C)$, and so we may consider its [[Eilenberg-MacLane object]]s $\mathbf{B}^n R$ for $n \in \mathbb{N}$.


The following proposition provides a model for these Eilenberg-MacLane objects.

Write $\Xi : Ch^\bullet_+ \to Ab^\Delta$ for the dual [[Dold-Kan correspondence]] map. Notice that the free $\mathcal{Ab}$-algebra is $F_{Ab}(*) = \mathbb{Z}$, the free abelian group on a single generator, the [[integer]]. Write $F_{Ab}(*)[n] = \mathbb{Z}[n]$ for the [[cochain complex]] concentrated in degree $n$ on $F_{Ab}(*)$. For $ab_* : Ab \to T Alg$ the left adjoint to the underlying abelian group functor $ab^* : T Alg \to Ab$ we have then thagt $ab_* \Xi (F_{Ab}(*)[n])$ is the cosimplicial $T$-algebra which in degree $k$ is a product of copies of the free $T$-algebra corresponding to the product of copies $\mathbb{Z}$ in $\Xi \mathbb{Z}[n]$.

+-- {: .un_prop}
###### Proposition

For $n \in \mathbb{N}$ the object $\mathbf{B}^n R \in Sh_{(\infty,1)}(C)$ is presented in $[C^{op}, sSet]_{proj,loc}$ by

$$
  \mathbf{B}^n R_{chn} := j(ab_* \Xi(F_{Ab}(*)[n])
  \,.
$$

=--

Every [[(∞,1)-topos]] such as $\mathbf{H} = Sh_{(\infty,1)}(C)$ comes with its [[cohomology|intrinsic notion of abelian cohomology]]: for $X \in \mathbf{H}$ any object and for $A \in \mathbf{H}$ a [[∞-group]] object with arbitrary [[delooping]]s $\mathbf{B}^n A$, the $n$th cohomology group of $X$ with coefficients in $A$ is

$$
  H^n(X,A) := \pi_0 \mathbf{H}(X,\mathbf{B}^n A)
  \,.
$$

In terms of the [[model category]] presentation by $[C^{op}, sSet]_{proj,loc}$ and writing $X \in [C^{op}, sSet]$ for a representative of $X \in \mathbf{H}$ this is the [[hom-set]] in the [[homotopy category]]

$$
  \cdots \simeq Ho_{[C^{op}, sSet]_{proj,loc}}(X, \mathbf{B}^n A_{chn})
  \,.
$$

+-- {: .un_prop}
###### Proposition
{#RCohomologyByO}

For $X \in [C^{op}, sSet]$ representing an object $X \in \mathbf{H}$, the intrinsic $R$-cohomology of $X$ coincides with the [[cochain cohomology]] of its cosimplicial function algebra $\mathbb{L}\mathcal{O}(X) \in T Alg^\Delta$:

$$
  H^n(X,R) \simeq H^n( \mathbb{L} \mathcal{O}(X))
  \,.
$$

=--

+-- {: .proof}
###### Proof

Notice that $ab_* \Xi(\mathbb{Z}[n])$, being the image of a cofibrant object in $Ab^\Delta$, is cofibrant in $T Alg^\Delta_{proj}$, hence fibrant in 
$(T Alg^\Delta_{proj})^{op}$. 

Using this, we comute as follows

$$
  \begin{aligned}
    H(X,\mathbf{B}^n R)
    & =
    Ho_{[C^{op}, sSet]_{proj}}(X, j(ab_* \Xi(\mathbb{Z}[n]))
    \\
    & \simeq
    Ho_{(T Alg^\Delta_{proj})^{op}}(\mathbb{L}\mathcal{O}(X), 
     ab_* \Xi(\mathbb{Z}[n])
    \\
    & \simeq
    Ho_{(T Alg^\Delta_{proj})}( 
        ab_* \Xi(\mathbb{Z}[n]),
       \mathbb{L}\mathcal{O}(X)
    )
    \\
    & \simeq 
    Ho_{(Ab^\Delta_{proj})}( 
        \Xi(\mathbb{Z}[n]),
       ab^* \mathbb{L}\mathcal{O}(X)
    )
    \\
    & \simeq 
    Ho_{Ch^\bullet}( 
        \mathbb{Z}[n],
       N^\bullet ab^* \mathbb{L}\mathcal{O}(X)
    )
    \\
    & \simeq
    H^n(\mathbb{L}\mathcal{O}(X))
  \end{aligned}
$$

=--

This is essentially the argument of ([To&#235;n, corollary 2.2.6](#Toen)).


### $R$-Local objects

+-- {: .un_def}
###### Definition

We say a morphism $f : X \to Y$ in $[C^{op}, sSet]$ is an **$R$-equivalence** if it induces isomorphisms in $R$-cohomology. 

$$
  H^i(f,R) : H^i(Y,R) \stackrel{\simeq}{\to} H^i(X,R)
  \,.
$$

By the [above proposition](#RCohomologyByO) this is equivalent to 
saying that the [[derived functor]] $\mathbb{L}\mathcal{O}$ takes
$f$ to a weak equivalence.

We say an object $K \in [C^{op}, sSet]_{proj,loc}$ is an **$R$-[[local object]]** if for all $R$-equivalences $f$ we have that

$$
  \mathbf{H}(f,K) : \mathbf{H}(Y,K) \to \mathbf{H}(X,K)
$$

is an equivalence, equivalently if the [[derived hom-space]]
functor produces a weak equivalence
$\mathbb{R}Hom_{[C^{op}, sSet]_{proj,loc}}(f,K)$ 
(of [[Kan complex]]es).

=--


+-- {: .un_prop}
###### Proposition

The $R$-local objects of $[C^{op}, sSet]_{proj,loc}$ that are equivalent to those in the image of $C^{\Delta^{op}} \hookrightarrow [C^{op}, sSet]$ span precisely the homotopy-essential image of the restriction of $\mathbb{R}j$ to $C^{\Delta^{op}}$

$$
  C^{\Delta^{op}} \hookrightarrow (T Alg^{\Delta})^{op}
  \stackrel{\mathbb{R}j}{\to}
  [C^{op}, sSet]_{proj,cov}
  \,.
$$

=--

+-- {: .proof}
###### Proof


We may explicitly see this by observing that the proof of 
([To&#235;n, theorem 2.2.9](#Toen)) goes through verbatim: it only uses the general properties of the $(\mathcal{O} \dashv j)$-adjunction that we have established above, as well as the fact that $T Alg^{\Delta}_{proj}$ is a 
[[cofibrantly generated model category]] for $T$ the theory of ordinary
commutative algebras. But by our [result on the model structure on TAlg](#ModelTransferToTAlg) we have that for general $T$ this is the [[transferred model structure]] of the [[model structure on cosimplicial abelian groups]], which is cofibrantly generated. Hence by the general properties of transferred model structures, also $T Alg^\Delta_{proj}$ is.

But more abstractly, we can also simply use the general theory of [[reflective sub-(∞,1)-categories]] and their characterization as the reflective [[localization of an (∞,1)-category]] at a set of weak equivalences: from the above we know that on the full sub-$(\infty,1)$-category of $((T Alg^\Delta_{proj})^{op})^\circ$ on the objects in $C^{\Delta^{op}} \hookrightarrow (T Alg^\Delta)^{op}$ is a reflective sub-$(\infty,1)$-category 

$$
  \mathbf{L} \stackrel{\overset{\mathbb{L} \mathcal{O}}{\hookrightarrow}}{\underset{\mathbb{R} i}{\to}}
  \mathbf{H} := Sh_{(\infty,1)}(C)
$$ 

and that the left adjoint to the embedding inverts precisely the $R$-equivalences. Hence $\mathbf{L}$ is the full sub-$(\infty,1)$-category of $\mathbf{H}$ on $R$-local objects.

=--


## In derived geometry {#DerivedGeometry}

We now discuss funciton algebras on $\infty$-stacks more generally in the context of [[derived geometry]], meaning that we we pass in the above from sites inside the opposite of a 1-category of $T$-algebras to an [[(∞,1)-site]] inside the opposite of an [[(∞,1)-category]] of [[∞-algebras over an (∞,1)-algebraic theory]].


### Over ordinary associative algebras

Let $k$ be a [[field]] of characteristic $0$.

+-- {: .un_def}
###### Definition

Write $(cdgAlg_k^{op})^\circ$ for the [[(∞,1)-category]] that is 
[[presentable (∞,1)-category|presented]] by the [[model structure on dg-algebras|model structure on unbounded commutative cochain dg-algebras]] over $k$.

Write 

$$
  i : (cdgAlg_k^{op})^\circ_- \subset (cdgAlg_k^{op})^\circ
$$

for the full [[sub-(∞,1)-category]] on cochain dg-algebras concentrated in non-positive degree.

=--

Let $C \subset (cdgAlg_k^{op})^\circ_-$ be a [[small (∞,1)-category|small]] full sub-$(\infty,1)$-category equipped with the structure of a [[subcanonical coverage|subcanonical]] [[(∞,1)-site]].

Set

$$
  \mathbf{H} := Sh_{(\infty,1)}(C)
  \,.
$$

+-- {: .un_def}
###### Definition

Write 

$$
  \mathcal{O} : \mathbf{H} \to ((cdgAlg_k^{op})^\circ
$$

for the $(\infty,1)$-[[Yoneda extension]] of the inclusion $C \hookrightarrow ((cdgAlg_k^{op})^\circ_, \hookrightarrow ((cdgAlg_k^{op})^\circ$.

=--

+-- {: .un_remark}
###### Remark

By the [[(∞,1)-co-Yoneda lemma]] we may express any $X \in Sh_{(\infty,1)}(C)$ by an [[(∞,1)-colimit]] over representables

$$
  X \simeq {\lim_\to}_i U_i \;\; \in Sh(C)
  \,.
$$

The functor $\mathcal{O}$ simply evaluates this colimit in $((cdgAlg_k^{op})^\circ$, which is the [[(∞,1)-limit]] in the [[opposite (∞,1)-category]]

$$
  \mathcal{O}X \simeq {\lim_\leftarrow}_i \mathcal{O}(U_i) \;\; \in (cdgAlg_k)^\circ
  \,,
$$

where we write $\mathcal{O}(U_i)$ simply for the object $U_i$ regarded in the opposite category.

=--


+-- {: .un_lemma}
###### Observation

By construction $\mathcal{O}$ is a colimit-preserving $(\infty,1)$-functor between [[locally presentable (∞,1)-categories]]. Accordingly, by the [[adjoint (∞,1)-functor theorem]] is has a [[right adjoint|right]] [[adjoint (∞,1)-functor]].

$$
  j : ((cdgAlg_k^{op})^\circ \to Sh_{(\infty,1)}(C)
  \,.
$$

This is given by 

$$
  Spec(A) : U \mapsto ((cdgAlg_k^{op})^\circ(U,A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows by the general yoga of [[Kan extension]]s. Explcitly, we check the hom-equivalence

$$
  \begin{aligned}
    Sh_C(X, Spec A) & \simeq \mathbf{H}({\lim_{\to}}_i U_i, Spec A)
    \\
    & \simeq {\lim_\leftarrow}_i \mathbf{H}(U_i, Spec A)
    \\
    & \simeq 
    {\lim_\leftarrow}_i C(U_i, A) 
    \\
     & \simeq 
    {\lim_\leftarrow}_i (cdgAlg_k)^\circ(A, \mathcal{O}(U_i))
    \\
    & \simeq 
    (cdgAlg_k)^\circ(A, {\lim_\to}_i  \mathcal{O}(U_i))
    \\
    & \simeq 
    (cdgAlg_k^{op})^\circ({\lim_\to}_i  \mathcal{O}(U_i), A)
  \end{aligned}
  \,.
$$

=--

This is considered in ([Ben-Zvi/Nadler, prop. 3.1](#BenZviNadler)).

+-- {: .un_lemma}
###### Observation

The above [Yoneda-Quillen adjunction](#YonedaQuillenAdjunction) for $T$ the theory of commutative $k$-algebras is compatible with this in that it also does  model the $(\infty,1)$-Yoneda extension of the inclusion

$$
  T Alg_k^{op} \hookrightarrow (T Alg_k^{\Delta})^{op}
$$

=--

+-- {: .proof}
###### Proof

By the general discussion of cofibrant replacement in the projective [[model structure on simplicial presheaves]] we have that every $X \in [C^{op}, sSet]_{proj,loc}$ has a cofibrant resolution of the form $\int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot \coprod_{i_n} U_{i_n}$, where the integrand the integrand we have the [[fat simplex]] tensored degreewise with a coproduct of representables such that the degenerate cells split off as direct summands (a [[split hypercover]]). This makes $[n] \mapsto \coprod_{i_n} U_{i_n}$ [[Reedy model structure|Reedy cofibrant]] an therefore the whole coend is a model for its [[homotopy colimit]].

Since both the simplex as well as the [[fat simplex]] $\mathbf{\Delta}$ are Reedy cofibrant cosimplicial simplicial sets, this is moreover equivalent to $\int^{[k]} \mathbf{\Delta}[k] \cdot \coprod_{i_n} U_{i_n}$ and this is still cofibrant. Now the left Quillen functor $\mathcal{O}$ takes this to $\int^{[k]} \mathbf{\Delta}[k] \cdot \coprod_{i_n} \mathcal{O}(U_{i_n})$. Since every object in $(T Alg^{\Delta})^{op}$ is cofibrant, this coend is still a homotopy colimit.

This shows that the [[derived functor]] of the left Quillen functor $\mathcal{O}$ sends the decomposition of any $\infty$-stack as the $(\infty,1)$-colimit over representable to the $(\infty,1)$-colimit of the images of these representables.

=--


## Examples and applications {#Examples}


+-- {: .un_prop}
###### Proposition (Examples)

The conditons of the above theorem are satisfied for instance for

* $T$ the theory of ordinary commutative algebras over a field $k$ and $J$ the [[fpqc topology]].

  In this case the adjunction is that considered in ([To&#235;n](#Toen)).

* $T$ the theory of [[nLab:smooth algebra]]s and $C \hookrightarrow T Alg^{op}$ the [[site]] of the [[Cahiers topos]]. This is what we discuss in more detail below.

=--

### Rational homotopy theory

$T$ the Lawvere theory of $\mathbb{Q}$-algebras. Then $(\mathcal{O} \dashv j)$ reproduces the setup discussed at [[rational homotopy theory in an (∞,1)-topos]].

### $\infty$-Lie theory in the $\infty$-Cahiers topos

In this section we study the general theory for the case that

* $T := $ [[CartSp]] is the ([[syntactic category]] of the) Lawvere theory of [[smooth algebra]]s.

Write $Smooth Alg := T Alg$ for the category of smooth algebras. Sheaf toposes on sub-sites $C \subset Smooth Alg^{op}$ are well known to provide [[smooth topos]]es that are [[Models for Smooth Infinitesimal Analysis|well adapted models]] for [[synthetic differential geometry]].

We consider here the choice

* $C \subset Smooth Alg^{op}$ is the [[site]] for the [[Cahiers topos]].

+-- {: .un_defn}
###### Definition

The [[Cahiers topos]] is the [[sheaf topos]] $Sh(ThCartSp)$ on the [[site]] [[ThCartSp]] $\subset CartSp Alg^{op}$ with [[coverage]] given by the families $\{U_i \times S \stackrel{(p,Id)}{\to} X \times S\}$, where $U \in $ [[CartSp]], $S$ is an [[infinitesimal space]] (the dual of a Weil algebra) and where $\{U_i \to X\}$ is a [[good open cover]] in [[CartSp]]. 

The **$(\infty,1)$-Cahiers-topos** is the [[(∞,1)-category of (∞,1)-sheaves]] on [[ThCartSp]] with respect to the good open cover coverage.

=--

+-- {: .un_remark}
###### Remark

The good open cover [[coverage]] generates the [[Grothendieck topology]] of all [[open cover]]s on [[CartSp]].  Therefore the sheaf toposes on $ThCartSp$ with covering families coming from all open covers of Cartesian spaces is equivalent to the sheaf topos on $ThCartSp$ with only good open covering.

By the discussioin at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#LocalizationAtCoverage">Cech localization of simplicial presheaves at a coverage</a>, the analogous statement holds true for the [[(∞,1)-topos]]es over these sites. 

Therefore we may model $Sh_{(\infty,1)}(ThCartSp_{good-open})$ by the [[left Bousfield localization]] of $[ThCartSp^{op}, sSet]_{proj}$ at the [[Cech nerve]]s of all good open cover. Notice that the construction of [[good open cover]]s (see there) on [[paracompact space]]s (such as [[Cartesian space]]s) by geodescally convex regions shows that we may always find a good open cover all whose finite non-empty intersections are [[diffeomorphism|diffeomorphic]] to an open ball, hence to a Cartesian space. We shall adopt for the present purposes therefore that a cover $\{U_i \to X\}$ is _good_ if all finite intersections are isomorphic to Cartesian spaces. 

The point is that with this definition, the [[Cech nerve]] $C(U) \in [ThCartSp^{op}, sSet]_{proj}$ is cofibrant, by the <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects">characterization of cofibrant objects</a> in the projective model structure. 

As a consequence of this, we have the following useful technical result.

=--


+-- {: .un_lemma}
###### Definition/Observation

Write $[ThCartSp^{op}, sSet]_{proj,cov}$ for the [[left Bousfield localization]] of the global projective model structure $[ThCartSp^{op}]_{proj}$ at the [[Cech nerve]]s $C(U) \to X\times S$ of [[good open cover]]s $\{U_i \times S \to X \times S\}$ in [[ThCartSp]].

We have that 

* this presents the $(\infty,1)$-Cahiers topos $Sh_{(\infty,1)}(ThCartSp) \simeq ([ThCartSp^{op}, sSet]_{proj,cov})$;

* the fibrant objects of $[ThCartSp^{op}, sSet]_{proj,cov}$ are precisely those fibrant objects  $A \in [ThCartSp^{op}, sSet]_{proj}$ such that for all goop open covers $\{ U_i \times S \to X \times S\}$ with Cech nerve $p_U : C(U) \to X \times S$ we have that 

  $$
    [ThCartSp^{op}, sSet]( p_U , A )
  $$

  is a weak equivalence (of [[Kan complex]]es).

=--

+-- {: .un_lemma}
###### Lemma

The Cech nerves projeections $p_U : C(U) \to X \times S$ induce isomorphisms on the cohomology of their cosimplicial function algebras: $H^p(\mathcal{O}(p_U))$ is an isomorphism, for all $p \in \mathbb{N}$.

=--

+-- {: .proof}
###### Proof

This is a standard fact about [[Cech cohomology]]. An explicit way to see it is to choose a smooth [[partition of unity]] subordinate to the cover. See <a href="http://ncatlab.org/nlab/show/partition+of+unity#CechCoboundaries">Coboundaries for Cech cocycles</a>.

=--

This means that the assumptions of the [Theorem on passage to the local model structure](#PassageToLocalTheorem) are satisfied.

+-- {: .un_corollary}
###### Corollary

We have a [[simplicial Quillen adjunction]]

$$
  (Smooth Alg^\Delta_{proj})^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{j}{\to}}
  [ThCartSp^{op}, sSet]_{proj,cov}
  \,.
$$

=--

#### $\infty$-Lie algebroids

+-- {: .un_def}
###### Definition

The objects of the $(\infty,1)$-Cahiers topos we call **synthetic differential** [[∞-Lie groupoid]]s.

The objects of the reflective sub-$(\infty,1)$-category of $R$-local objects in the $(\infty,1)$-Cahiers topos 

$$
  \mathbf{L} \stackrel{\leftarrow}{\hookrightarrow}
  \mathbf{H} = Sh_{(\infty,1)}(ThCartSp)
$$

we call **[[∞-Lie algebroid]]**s. 

A [[connected]] $\infty$-Lie algebroid we call an **[[∞-Lie algebra]]**.



=--


(...)

Passing along the embedding $\mathbf{L} \hookrightarrow \mathbf{H}$ we may compute [[∞-Lie algebra cohomology]] in $\mathbf{H}$.

(...)



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

Or the **path $\infty$-Lie algebroid** .

(...)

#### The tangent category of smooth algebras

(...)

The [[tangent category]] of the category of [[smooth algebra]]s is the category of modules over $C^\infty$-rings. 

**Proposition** This abstract definition of module over $C^\infty$-rings reproduces the definition given by Kock.

The tangent category of the category of _simplicial_ $C^\infty$-rings is ...

This serves the purpose of presenting the $\infty$-stack of $\infty$-vector bundles on $T Alg^{op}$.

(...)






## Appendix

### Enrichment of categories of simplicial objects {#Enrichment}

We make use of the canonical structure of an [[sSet]]-[[enriched category]] on any [[category of cosimplicial objects]] in a category with all limits and colimits (see there).

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

We use the [[model category]] structure on $Ab^\Delta$ whose fibratin are the degreewise surjections, and whose weak equivalences are the usual [[quasi-isomorphism]]s under the dual [[Dold-Kan correspondence]] $Ab^\Delta \simeq Ch^\bullet_+(Ab)$.

The model structure is described in detail at <a href="http://ncatlab.org/nlab/show/model+structure+on+chain+complexes#CochainNonNegProj">model structure on chain complexes - the projective structure</a>.

The structure of a [[simplicial model category]] is described in detail at [[model structure on cosimplicial abelian groups]].

## Further questions

+-- {: .query}

[[Urs Schreiber]]: want to work out the following:

if $Sh_{(\infty,1)}(C)$ is a [[locally contractible (∞,1)-topos]] we have the [[schreiber:path ∞-groupoid]] functor $\Pi$

$$
  \Pi : Sh_{(\infty,1)}(C) \to \infty Grpd \simeq Top
$$

which forms geometric realization of simplicial spaces. In irs kernel (preimage of contractible spaces) sit objects such as $\mathbf{B}^n R$ that have nontrivial homotopy groups in $Sh_{(\infty,1)}(C)$ but which nevertheless become contractibe in $\infty Grpd$ under $\Pi$.

We can think of this kernel of $\Pi$ hence as being smooth objects that have "no topology". These should at least include the $\infty$-Lie algebroids. So it ought to be true that the inclusion

$$
  ((T Alg^{\Delta})^{op})^\circ \hookrightarrow Sh_{(\infty,1)}(C)
$$

lands in the kernel of $\Pi$. Now, by statement discussed at [[∞-Lie groupoid]], $\Pi$ does not in general preserve [[(∞,1)-limit]]s, but it does preserve [[homotopy fiber]]s. So every object that is successively built form extensions classified by maps $A \to \mathbf{B}^n R$ will be sent by $\Pi$ to a contractible space.

But at least if $T$ is the theory of ordinary $k$-algebras, it is true that the objects in the image of the inclusion are of this form, since in terms of the [[derived functor]] of the inclusion 1-functor those are duals of [[Sullivan algebra]]s. 



=--

## References

The Quillen adjunction over abelian $T$-algebras that we consider generalizes that discussed in 

* [[nLab:Bertrand Toën]], _Champs affine_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))
{#Toen}

over ordinary commutative $k$-algebras. See also [[rational homotopy theory in an (infinity,1)-topos]].

The generalization to arbitrary abelian $T$-algebras and the application to synthetic differential geometry is the content of 

* [[Herman Stel]], _$\infty$-Stacks and their function algebras -- with applications to $\infty$-Lie theory_ , master thesis (2010) ([[schreiber:master thesis Stel|web]])
{#Stel}

on which this entry here is based.

The considerations in 

* [[David Spivak]], _Derived smooth manifolds_  Duke Math. J. Volume 153, Number 1 (2010), 55-128. ([pdf](http://www.uoregon.edu/~dspivak/derived-smooth-manifolds.pdf))
{#Spivak}

on [[derived smooth manifold]]s may be considered as complementary to the approach taken here: there simplicial $C^\infty$-rings are considered, instead of cosimplicial ones. A fully comprehensive treatment of _derived synthetic differential geometry_ would consider the combination of both aspects: simplicial presheaves on duals of simplicial $C^\infty$-rings with a functor $\mathcal{O}$ taking them to cosimplicial-simplicial $C^\infty$-rings. 

For ordinary commutative algebras the generalizaton of Toen's setup to geometry over duals of simplicial algebras is used for instance in

* [[David Ben-Zvi]], [[David Nadler]], _Loop spaces and connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))
{#BenZviNadler}


[[!redirects function algebras on ∞-stacks]]

[[!redirects rational homotopy theory in an (∞,1)-topos]]
[[!redirects rational homotopy theory in an (infinity,1)-topos]]