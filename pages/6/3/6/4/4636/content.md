
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

There is a general abstract [[adjunction]] $(\mathcal{O} \dashv Spec)$ between [[presheaves]] and [[copresheaves]] over a [[category]].

This is sometimes known as _Isbell [[duality]]_ .
 .

## Definition

Let $\mathcal{V}$ be a good enriching category (a [[cosmos]], i.e. a [[complete category|complete]] and [[cocomplete category|cocomplete]] [[closed monoidal category|closed]] [[symmetric monoidal category]]).

Let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]].

Write $[\mathcal{C}^{op}, \mathcal{V}]$ and $[\mathcal{C}, \mathcal{V}]$ for the [[enriched functor categories]].

+-- {: .un_prop}
###### Proposition

There is an $V$-[[adjunction]]

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

+-- {: .proof}
###### Proof

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
