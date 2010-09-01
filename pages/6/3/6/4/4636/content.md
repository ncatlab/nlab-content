
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

There is a general abstract [[adjunction]] $(\mathcal{O} \dashv Spec)$ between [[presheaves]] and [[copresheaves]] over a [[category]].

This is sometimes known as _Isbell conjugation_ .

## Definition

Let $\mathcal{V}$ be a good enriching category (a [[cosmos]], i.e. a [[complete category|complete]] and [[cocomplete category|cocomplete]] [[closed monoidal category|closed]] [[symmetric monoidal category]]).

Let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]].

Write $[\mathcal{C}^{op}, \mathcal{V}]$ and $[\mathcal{C}, \mathcal{V}]$ for the [[enriched functor categories]].

+-- {: .un_prop}
###### Proposition

There is a $V$-[[adjunction]]

$$
  (\mathcal{O} \dashv Spec)
  :
  [C, \mathcal{V}]^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  [C^{op}, \mathcal{V}]
$$

where 

$$
  \mathcal{O}(X) : c \mapsto [C^{op}, \mathcal{V}](X, \mathcal{V}(-,c))
  \,,
$$

and

$$
  Spec(A) : c \mapsto [C, \mathcal{V}]^{op}(\mathcal{V}(c,-),A)
  \,.
$$

=--

The proof is mostly a tautology after the notation is unwinded. The mechanism of the proof may still be of interest and be relevant for generalizations and for less tautological variations of the setup. We therefore spell out several proofs.

+-- {: .proof}
###### Proof A

Use the [[end]]-expression for the [[hom-object]]s of the [[enriched functor categories]] to compute

$$
  \begin{aligned}
     [C,\mathcal{V}]^{op}(\mathcal{O}(X), A)
     & :=
     \int_{c \in C} \mathcal{V}(A(c), \mathcal{O}(X)(c))
     \\
     & := 
     \int_{c \in C} \mathcal{V}(A(c), [C^{op}, \mathcal{V}](X, \mathcal{V}(-,c)))
     \\
     & :=
     \int_{c \in C} \int_{d \in C} \mathcal{V}(A(c), \mathcal{V}(X(d), \mathcal{V}(d,c)))
     \\
     & \simeq 
     \int_{d \in C} \int_{c \in C} \mathcal{V}(X(d), \mathcal{V}(A(c), \mathcal{V}(d,c)))
    \\
     & =:
     \int_{d \in C}  \mathcal{V}(X(d), [C,\mathcal{V}]^{op}(\mathcal{V}(d,-),A))
    \\
     & =:
     \int_{d \in C}  \mathcal{V}(X(d), Spec(A)(d))
    \\
     & =:
     [C^{op}, \mathcal{V}](X, Spec(A))
  \end{aligned}
  \,.
$$

=--

Notice that apart from writing out or hiding the ends, the only step that is not a definition is precisely the middle one, where we used that $\mathcal{V}$ is a [[symmetric monoidal category|symmetric]] [[closed monoidal category]].

The following proof does not use ends and needs instead slightly more preparation, but has then the advantage that its structue goes through also in great generality in [[higher category theory]].
{#ProofB}

+-- {: .proof}
###### Proof B

Notice that 

**Lemma 1:** $Spec(\mathcal{V}(c,-)) \simeq \mathcal{V}(-,c)$

because we have a natural isomorphism

$$
  \begin{aligned}
    Spec(\mathcal{V}(c,-))(d) 
    & :=
    [C,\mathcal{V}](\mathcal{V}(c,-), \mathcal{V}(d,-))
    \\
    & \simeq
    \mathcal{V}(d,c)
  \end{aligned}
$$ 

by the [[Yoneda lemma]].

From this we get

**Lemma 2:** $[C^{op}, \mathcal{V}](Spec \mathcal{V}(c,-), Spec A) \simeq 
    [C,\mathcal{V}](A, \mathcal{V}(c,-))$

by the sequence of natural isomorphisms

$$
  \begin{aligned}
     [C^{op}, \mathcal{V}](Spec \mathcal{V}(c,-), Spec A)
     & \simeq
     [C^{op}, \mathcal{V}](\mathcal{V}(-,c), Spec A)
     \\
     & \simeq (Spec A)(c)
     \\
     & := [C, \mathcal{V}](A, \mathcal{V}(c,-))
  \end{aligned}
  \,,
$$

where the first is Lemma 1 and the second the [[Yoneda lemma]].

Since (by what is sometimes called the [[co-Yoneda lemma]]) every object $X \in [C^{op}, \mathcal{V}]$ may be written as a [[colimit]]

$$
  X \simeq {\lim_\to}_i \mathcal{V}(-,c_i) 
$$

over [[representable functor|representables]] $\mathcal{V}(-,c_i)$ we have

$$
  X \simeq {\lim_\to}_i Spec(\mathcal{V}(c_i,-))
  \,.
$$

In terms of the same diagram of representables it then follows that

**Lemma 3:** 

$$
  \mathcal{O}(X) \simeq {\lim_{\leftarrow}}_i \mathcal{V}(c_i,-)
$$

because using the above colimit representation and the Yoneda lemma we have natural isomorphisms

$$
  \begin{aligned}
     \mathcal{O}(X)(d) 
     &=
     [C^{op}, \mathcal{V}](X, \mathcal{V}(-,c))
     \\
     & \simeq
     [C^{op}, \mathcal{V}]({\lim_\to}_i \mathcal{V}(-,c_i), \mathcal{V}(-,c))
     \\
     & \simeq
     {\lim_\leftarrow}_i [C^{op}, \mathcal{V}](\mathcal{V}(-,c_i), \mathcal{V}(-,c))
     \\
     & \simeq 
     {\lim_\leftarrow}_i \mathcal{V}(c_i,c)
  \end{aligned}
  \,.
$$


Using all this we can finally obtain the adjunction in 
question by the following sequence of natural isomorphisms

$$
  \begin{aligned}
     [C,\mathcal{V}]^{op}(\mathcal{O}(X), A)
     & 
     \simeq
     [C,\mathcal{V}](A, {\lim_\leftarrow}_i \mathcal{V}(c_i,-), )
     \\
     & \simeq 
     {\lim_{\leftarrow}}_i [C, \mathcal{V}](A, \mathcal{V}(c_i,-))
     \\
     & \simeq 
     {\lim_{\leftarrow}}_i [C^{op}, \mathcal{V}](Spec \mathcal{V}(c_i,-), Spec A)
     \\
     & \simeq
     [C^{op}, \mathcal{V}]({\lim_{\to}}_i  Spec \mathcal{V}(c_i,-), Spec A)
     \\
     & \simeq
     [C^{op}, \mathcal{V}](X, Spec A)     
  \end{aligned}
  \,.
$$

=--

The pattern of this proof has the advantage that it goes through in great generality also on [[higher category theory]] without reference to a higher notion of enriched category theory.

## Properties

### Respect for limits

Choose any [[class]] $L$ of [[limit]]s in $C$ and write $[C,\mathcal{V}]_\times \subset [C,\mathcal{V}]$ for the [[full subcategory]] on those functors that preserve these limits. 

+-- {: .un_prop}
###### Proposition

The $(\mathcal{O} \dashv Spec)$-adjunction does descend to this inclusion, in that we have an adjunction

$$
  (\mathcal{O} \dashv Spec)
  :
  [C, \mathcal{V}]_{\times}^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  [C^{op}, \mathcal{V}]
$$

=--

+-- {: .proof}
###### Proof

Because the [[hom-functor]]s preserves all [[limit]]s:

$$
  \begin{aligned}
    \mathcal{O}(X)({\lim_{\leftarrow}}_j c_j)
    & := [C^{op}, \mathcal{V}](X,\mathcal{V}(-,{\lim_{\leftarrow}}_j c_j))
    \\
    & \simeq [C^{op}, \mathcal{V}](X,{\lim_{\leftarrow}}_j  \mathcal{V}(-,c_j))
    \\
    & \simeq {\lim_{\leftarrow}}_j  [C^{op}, \mathcal{V}](X,\mathcal{V}(-,c_j))
    \\
    & =: {\lim_{\leftarrow}}_j \mathcal{O}(X)(c_j)
  \end{aligned}
  \,.
$$ 

=--

### Isbell envelope

See [[Isbell envelope]].

## Examples

### Function $T$-Algebras on presheaves {#FunctionAlgebrasOnPresheaves}

Let $\mathcal{V}$ be any [[cartesian closed category]]. 

Let $C := T$ be the [[syntactic category]] of a $\mathcal{V}$-enriched [[Lawvere theory]], that is a $\mathcal{V}$-category with finite [[product]]s such that all objects are generated under products from a single object $1$.

Then write $T Alg := [C,\mathcal{V}]_\times$ for category of product-preserving functors: the category of $T$-algebras. This comes with the canonical forgetful functor

$$
  U_T : T Alg \to \mathcal{V} :   A \mapsto A(1)
$$

Write 

$$
  F_T : T^{op} \hookrightarrow T Alg
$$ 

for the [[Yoneda embedding]]. 

+-- {: .un_def}
###### Definition

Call 

$$
  \mathbb{A}_T := Spec(F_T(1))  \in [C^{op}, \mathcal{V}]
$$

the **$T$-line object**.

=--

+-- {: .un_lemma}
###### Observation

For all $X \in [C^{op}, \mathcal{V}]$ we have

$$
  \mathcal{O}(X) \simeq
  [C^{op}, \mathcal{V}](X, Spec(F_T(-)))
  \,.
$$

In particular 

$$
  U_T(\mathcal{O}(X)) \simeq [C^{op}, \mathcal{V}](X,\mathbb{A}_T)
  \,.
$$

=--


+-- {: .proof}
###### Proof

We have isomorphisms natural in $k \in T$

$$
\begin{aligned}
  [C^{op}, \mathcal{V}](X, Spec(F_T(k)))
  & \simeq
  T Alg(F_T(k), \mathcal{O}(X))
  \\
  & \simeq
  \mathcal{O}(X)(k)
\end{aligned}
$$

by the above adjunction and then by the [[Yoneda lemma]].

=-- 


All this generalizes to the following case:

instead of setting $C := T$ let more generally

$$
  T \subset C \subset T Alg^{op}
$$

be a [[small category|small]] [[full subcategory]] of $T$-algebras, containing all the free $T$-algebras.

Then the original construction of $\mathcal{O} \dashv Spec$ no longer makes sense, but that in terms of the line object still does

+-- {: .un_prop}
###### Proposition

Set

$$
 Spec A : B \mapsto T Alg(A,B)
$$

and

$$
  \mathcal{O}(X) : k \mapsto 
  [C^{op}, \mathcal{V}](X, Spec(F_T(k)))
  \,.
$$

Then we still have an adjunction

$$
  (\mathcal{O} \dashv Spec)
  :
  T Alg^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  [C^{op}, \mathcal{V}]
  \,.
$$


=--


+-- {: .proof}
###### Proof


$$
  \begin{aligned}
    T Alg^{op}(\mathcal{O}(X), A)
    & :=
    \int_{k \in T} \mathcal{V}( A(k), \mathcal{O}(X)(k) )
    \\
    & := 
    \int_{k \in T} \mathcal{V}( A(k), [C^{op}, \mathcal{V}](X, Spec(F_T(k))) )
    \\
    & := \int_{k \in T} \int_{B \in C}
    \mathcal{V}(A(k), \mathcal{V}(X(B), T Alg(F_T(k), B) ))
    \\
    & \simeq \int_{k \in T} \int_{B \in C}
    \mathcal{V}(A(k), \mathcal{V}(X(B), B(k) ))
    \\
    & \simeq \int_{k \in T} \int_{B \in C}
    \mathcal{V}(X(B), \mathcal{V}(A(k), B(k) ))
    \\
    & =: \int_{B \in C} \mathcal{V}(X(B), T Alg(A,B))
    \\
    & =:
    \int_{B \in C} \mathcal{V}(X(B), Spec(A)(B))
    \\
    & =:
    [C^{op}, Set](X,Spec(A))
  \end{aligned}
  \,.
$$

The first step that is not a definition is the [[Yoneda lemma]]. The step after that is the symmetric-closed-monoidal structure of $\mathcal{V}$.

=--

### Function $k$-algebras on derived $\infty$-stacks {#FuncCompDerStacks}

The structure of our [Proof B](#ProofB) above goes through in higher category theory. 

Formulated in terms of [[derived stack]]s over the [[(∞,1)-category]] of [[dg-algebra]]s, this is essentially the argument appearing on [page 23](http://arxiv.org/PS_cache/arxiv/pdf/1002/1002.3636v1.pdf#page=23) of ([Ben-ZviNadler](#Ben-ZviNadler)).

### Function $T$-algebras on $\infty$-stacks

for the moment see [[function algebras on ∞-stacks]]

## References

Isbell conjugation is reviewed on [page 17](#http://www.tac.mta.ca/tac/reprints/articles/8/tr8.pdf#page=17) of 

* [[Bill Lawvere]], _Taking categories seriously_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/8/tr8.pdf))

Isbell conjugacy for [[(∞,1)-presheaves]] over the [[(∞,1)-category]] of duals of [[dg-algebra]]s is discussed around page 32 of

* [[David Ben-Zvi]], [[David Nadler]], _Loop spaces and connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))
{#Ben-ZviNadler}


[[!redirects Isbell duality]]
