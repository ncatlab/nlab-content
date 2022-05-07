
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

For $C$ a [[monoidal category]], the **category of [[monoid in a monoidal category|monoids]]** $Mon(C)$  in $C$ is the [[category]] whose

* [[objects]] are [[monoid in a monoidal category|monoids]] in $C$;

* [[morphism]]s are morphisms in $C$ of the underlying objects that respect the monoid structure.

Similarly for the **category of [[commutative monoid in a symmetric monoidal category|commutative monoids]]** $CMon(C)$, if $C$ is symmetric monoidal.

=--


+-- {: .num_remark}
###### Remark

If [[Assoc]] denotes the [[associative operad]] in $C$, then $Mon(C) = Alg_C Assoc$ is the category of [[algebras over an operad]] for $Assoc$.

=--

+-- {: .num_remark}
###### Remark

Every category of monoids comes with a [[forgetful functor]] $U \colon Mon(C) \to C$ which is [[faithful functor|faithful]] and [[conservative 
functor|conservative]].  In many cases it is [[monadic functor|monadic]].

=--

## Properties

The properties of the [[category]] of monoids $Mon (C)$, especially with respect to [[colimit]]s, are markedly different according to whether or not the [[tensor product]] of $C$ preserves colimits in each variable.  (This is automatically the case if $C$ is [[closed monoidal category|closed]].)

Most "algebraic" situations have this property, but others do not.  For instance, the category of [[monads]] on a fixed category $A$ is $Mon (C)$, where $C= [A,A]$ is the category of [[endofunctors]] of $A$ with composition as its monoidal structure.  This monoidal product preserves colimits in one variable (since colimits in $[A,A]$ are computed pointwise), but not in the other (since most endofunctors do not preserve colimits).  So far, the material on this page focuses on the case where $\otimes$ does preserve colimits in both variables, although some of the references at the end discuss the more general case.


### Local presentability

+-- {: .num_theorem}
###### Theorem

Let $C$ be a [[closed monoidal category|closed]] [[symmetric monoidal category]] with countable [[coproducts]] which is [[locally presentable category|locally presentable]].

Then

1. $U : Mon(C) \to C$ is a finitary [[monadic functor]].

1. If $C$ is a $\lambda$-[[locally presentable category]] then so is $Mon(C)$.

=--

This appears in ([Porst, page 7](#Porst)).


### Free and relative free monoids {#FreeMonoids}

+-- {: .num_prop}
###### Proposition

Let $C$ be a [[monoidal category]] with countable [[coproduct]]s that are preserved by the [[tensor product]]. Then the forgetful functor $U_C$ has a [[left adjoint]] $F_C : C \to Mon(C)$. On an object $X \in C$ the underlying object of $F_C X$ is

$$
  U_C F_C X 
  = 
  \coprod_{n \in \mathbb{N}} X^{\otimes n}
  = 
  I_C \coprod X \coprod (X \otimes X) \coprod \cdots
$$

in $C$, with the monoidal structure given by tensor product/juxtaposition.


=--


+-- {: .proof}
###### Proof 

A morphism $f : F_C X \to A$ in $Mon(C)$ with components $f_k : X^{\otimes k} \to U_C A$ is entirely fixed by its component $\tilde f = f_1 : X \to U_C A$ on $X$, because by the homomorphism property and the special free nature of the product in $F_C X$

$$
  \array{
    X^{\otimes k} \otimes X^{\otimes (n-k)} &\stackrel{f_k \otimes f_{n-k}}{\to}&
    A \otimes A
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\mu_A}}
    \\
    X^{\otimes n} &\stackrel{f_{n}}{\to}& A
  }
$$

it follows that 

$$
  f_n :
  X^{\otimes n} \stackrel{f_1^{\otimes n}}{\to} A^{\otimes n} \stackrel{\mu_A}{\to} A
  \,.
$$

Conversely, every choice for $f_1$ extends to a morphism $f$ in $Mon(C)$ this way.

=--


+-- {: .num_example}
###### Examples

Free algebras of the form $F(A)$ are called **[[tensor algebra]]**s, at least for $C = $ [[Vect]] and similar.

The elements of the free algebra $F(A)$ are somtimes called [[lists]], at least for $C = $ [[Set]] and similar.
=--

### Pushouts

We discuss forming [[pushouts]] in a category of monoids. The case

* [For commutative monoids](#PushoutOfCommutativeMonoids)

has a simple description. The case

* [For non-commutative monoids](#PushoutOfNoncommutativeMonoids)

is more involved.


#### Of commutative monoids
 {#PushoutOfCommutativeMonoids}


+-- {: .num_prop #PushoutsInCMonGivenByTensorProduct}
###### Proposition

Suppose that $\mathcal{C}$ is 

* a [[symmetric monoidal category]];

* with [[reflexive coequalizers]]

* that are preserved by the [[tensor product]] functors $A \otimes (-) \colon \mathcal{C} \to \mathcal{C}$ for all objects $A$ in $\mathcal{C}$.

Then for $f \colon A \to B$ and $g \colon A \to C$ two morphisms in the category $CMon(\mathcal{C})$ of _[[commutative monoid in a symmetric monoidal category|commutative monoids]]_ in $\mathcal{C}$, the underlying object in $\mathcal{C}$ of the [[pushout]] in $CMon(\mathcal{C})$ coincides with that of the pushout in the category $A$[[Mod]] of $A$-[[modules]]

$$
  U(B \coprod_A C) \simeq  B \otimes_A C 
  \,.
$$

Here $B$ and $C$ are regarded as equipped with the canonical $A$-module structure induced by the morphisms $f$ and $g$, respectively.

=--

This appears for instance as ([Johnstone, page 478, cor. 1.1.9](#Johnstone)).



#### Of noncommutative monoids
 {#PushoutOfNoncommutativeMonoids}

+-- {: .num_prop #PushOutOfMonoidsAlongFreeMorphisms}
###### Proposition

If $C$ is [[cocomplete category|cocomplete]] and its tensor product preserves colimits on both sides, then the category $Mon(C)$ of monoids has all [[pushout]]s 

$$
  \array{
    F(K) &\stackrel{F(f)}{\to}& F(L)
    \\
    {}^{\mathllap{p}}\downarrow && \downarrow
    \\
    X &\to& P
  }
$$

along morphisms $F(f) : F(K) \to F(L)$, for $f : K \to L$ a morphism in $C$ and $F : C \to Mon(C)$ the free monoid functor from above.

Moreover, these pushouts in $Mon(C)$ are computed in $C$ as the [[colimit]] over a sequence

$$
  P \simeq \lim_{\to}( X := P_0 \to P_1 \to P_2 \to \cdots )
$$

of objects $(P_n)_{n \in \mathbb{N}}$, which are each given by pushouts in $C$ inductively as follows. 

Assume $P_{n-1}$ has been defined. Write $Sub(\mathbf{n})$ for the [[poset]] of [[subset]]s of the $n$-element set $\mathbf{n}$ (this is the poset of paths along the edges of an $n$-dimensional cube). Define a [[diagram]]

$$
  K : Sub \mathbf{n} \to C
$$

by setting on subsets $S \subset \mathbf{n}$

$$
  K_S := X \otimes V_1 \otimes X \otimes V_2 \otimes  \cdots \otimes V_n \otimes X
$$

where

$$
  V_i := \left\{
     \array{
        K & if \, i \notin S
        \\
        L & if \, i \in S
     }
  \right.
$$

and by assigning to a morphism $S_1 \subset S_2$ the morphism which is the [[tensor product]] of identities on $X$, identities on $L$ and the given morphism $f : K \to L$.

Write $K^-$ for the same diagram minus the terminal object $S = \mathbf{n}$. 

Now take $P_n$ to be the [[pushout]]

$$
  \array{
    \lim_{\to} K^- &\to& K \mathbf{n}
    \\
    \downarrow && \downarrow
    \\
    P_{n-1} &\to& P_n
  }
  \,,
$$

where the top morphism is the canonical one induced by the commutativity of the diagram $K$, and where the left morphism is defined in terms of components $K^-(S)$ of the colimit for $S \subset \mathbf{n}$ a proper subset by the tensor product morphisms of the form 

$$
  (\cdots X \otimes K \otimes \cdots \otimes L \otimes \cdots)
  \stackrel{\cdots \otimes \mu_X \circ (Id \otimes p) \otimes \cdots \otimes Id_L \otimes \cdots}{\to}  
  (X \otimes L)^{|S|} \otimes X
  \to P_{|S|} \to P_{n-1}
  \,.
$$

This gives the underlying object of the monoid $P$. Take the monoid structure on it as follows. The unit of $P$ is the composite

$$
 e_P : I_C \stackrel{e_X}{\to} X \to P
$$

with the unit of $X$. The product we take to be the image in the colimit of compatible morphisms $P_k \otimes P_k \to P_{k + l}$ defined by induction on $lk + l$ as follows. we observe that we have a pushout diagram

$$
  \array{
     Q_k \otimes (X \otimes L)^{\otimes l}
    \coprod_{Q_k \otimes Q_l}
    (X \otimes L)^{\otimes l} \otimes X \otimes Q_l
    &\to&
    (X \otimes L)^{\otimes k} \otimes X \otimes (X \otimes L)^{\otimes l} \otimes X
    \\
    \downarrow && \downarrow
    \\
    P_{k-1} \otimes P_l \coprod_{P_{k-1} \otimes P_{l-1}}
    P_k \otimes P_{l-1}
    &\to&
    P_k \otimes P_l
  }
  \,,
$$

where $Q_n := (\lim_{\to} K)_n$ is the colimit as in the above at stage $n$.

There is a morphism from the bottom left object to $P_{k+l}$ given by the induction assumption. Moreover we have a morphism from the top right object to $P_{k+1}$ obtained by first multiplying the two adjacent factors of $X$ and then applying the morphism $(X \otimes L)^{\otimes k+l} \otimes X \to P_{k+l}$.
These are compatible and hence give the desired morphism $P_k \otimes P_k \to P_{k+l}$.


=--

This construction is spelled out for instance in the proof of [SchwedeShipley, lemma 6.2](#SchwedeShipley)

+-- {: .proof}
###### Proof 

First we need to discuss that this definition is actually consistent, in that the morphism $\lim_\to K^- \to P_{n-1}$ is well defined and the monoid structure on $P$ is well defined.

(...)

That $X \to P$ is a morphism of monoids follows then essentially by the definition of the monoid structure on $P$.

Finally we need to check the universal property of the cocone $P$ obtained this way:

(...)


=--

### Filtered colimits
 {#FilteredColimits}

+-- {: .num_prop }
###### Proposition

For $C$ a [[closed monoidal category|closed]] [[symmetric monoidal category]] the [[forgetful functor]]

$$
  U : CMon(C) \to C
$$

from commutative monoids to $C$ [[creates colimits|creates]] [[filtered colimit]]s.

=--

This appears for instance as ([Johnstone, C1.1 lemma 1.1.8](#Johnstone)).


### Structure induced from monoidal functors

If $F : C\to D$ is a [[lax monoidal functor]], then it induces canonically a functor between categories of monoids

$$
  Mon(F) : Mon(C) \to Mon(D)
  \,.
$$

This is one good way to remember the difference between *lax* and *colax* monoidal functors.


### Model structure

If $C$ is a [[monoidal model category]], then $Mon(C)$ may inherit itself the structure of a [[model category]]. See [[model structure on monoids in a monoidal model category]].

### Enrichment over $CMon$

Some categories are _implicitly_ [[enriched category|enriched]] over commutative monoids, in particular [[semiadditive categories]]. Also [[Ab]]-[[enriched categories]] (and hence in particular [[abelian categories]]) of course have an underlying $CMon$-enrichment.

## Related categories

* [[Grp]], [[Ab]]

* [[Ring]], [[CRing]]

* [[Rng]]

## References

A general discussion of categories of monoids in [[symmetric monoidal categories]] is in

* {#Porst} [[Hans Porst]], _On Categories of Monoids, Comonoids and bimonoids_ ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.144.4291&rep=rep1&type=pdf))


Free monoid constructions are discussed in 

* [[Eduardo Dubuc]], _Free monoids_ Algebra J. 29, 208&#8211;228 (1974)

* [[Max Kelly]], _A unified treatment of transfinite constructions for free algebras, free monoids,colimits, associated sheaves, and so on_ Bull. Austral. Math. Soc. 22(1), 1&#8211;83 (1980)

* [[Stephen Lack]], _Note on the construction of free monoids_ Appl Categor Struct (2010) 18:17&#8211;29 

The detailed discussion of pushouts along free monoid morphisms is in the proof of lemma 6.2 of

* [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 
{#SchwedeShipley}

Some remarks on commutative monoids are in section C1.1 of

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]]_


Discussion of the [[closed monoidal category]] structure on a category of algebras of a [[commutative algebraic theory]] is in

* [[Peter Freyd]], _Algebra valued functors in general and tensor products in particular_, Colloq. Math. 14 (1966), 89-106.

[[!redirects categories of monoids]]

[[!redirects category of commutative monoids]]

[[!redirects Mon]]
[[!redirects AbMon]]
[[!redirects CMon]]

category: category