
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}
 
## Idea

Hochschild (co)homology is a homological construction which makes sense for any [[associative algebra]], or more generally any [[dg-algebra]] or [[ring spectrum]].  It has multiple interpretations in [[higher category theory]].  Presently, everything below pertains to Hochschild homology of *commutative* algebras; an exposition of the noncommutative case remains to be written.

Thus, for $A$ a commutative [[∞-algebra]], its _Hochschild homology complex_ is its [[(∞,1)-colimit|(∞,1)-tensoring]] $S^1 \cdot A$ with the [[∞-groupoid]] incarnation of the circle. More generally, for $S$ any $\infty$-groupoid/simplicial set, $S \cdot A$ is the corresponding _higher order Hochschild homology_ of $A$.

In the presence of [[function algebras on ∞-stacks]] it may happen that $A = \mathcal{O}(X)$ is the algebra of functions on some [[∞-stack]] $X$ and that $\mathcal{O}(-)$ sends [[powering]]s of  $X$ to tensorings of $\mathcal{O}(X)$. In that case it follows that the Hochschild homology complex of $\mathcal{O}(X)$ is the function complex $\mathcal{O}(\mathcal{L}(X))$ on the [[derived loop space]] $\mathcal{L}X$ of $X$.


### The Hochschild complex {#TraditionalIdeas}
 
Originally the notion of Hochschild homology was introduced as the 
[[chain homology]] of a certain [[chain complex]] associated to any [[bimodule]] $N$ over some [[algebra]] $A$: its [[bar complex]], written 
 
$$
  C_\bullet(A,N) := N \otimes_{A \otimes A^{op}} \mathrm{B}_\bullet A
  \,,
$$
  
where $N$ and $A$ are regarded as $A \otimes A^{op}$-bimodules in the obvious way.

Then it was understood that this complex is the result of tensoring the $A$-bimodules $N$ with $A$ over $A \otimes A^{op}$ but using the [[derived functor]] of the [[tensor product]] functor --  the [[Tor functor]] -- in the ambient [[model structure on chain complexes]]:
 
$$
   C_\bullet(A,N) = N \otimes^D_{A\otimes A^{op}} A = Tor^\bullet_{A\otimes A^{op}}(N,A)
   \,.
$$  
 
Then still a little later, it was understood that this is just the ordinary tensor product in the [[symmetric monoidal (∞,1)-category]] of [[chain complex]]es. If this
is understood, we can just write again simply 
$$
  C_\bullet(A,N) := N \otimes_{A \otimes A^{op}} A
  \,.
$$

This, generally, is the definition of the Hochschild homology object of any bimodule over a [[monoid in a monoidal (∞,1)-category|monoid]] in a symmetric monoidal $(\infty,1)$-category (symmetry is needed to make sense of $A^{op}$).  Dually, the Hochschild *cohomology* object is 

$$ C^\bullet(A,N) := Hom_{A\otimes A^{op}}(A,N).$$

Of special interest is the case where $N = A$. In this case the Hochschild cohomology object is also called the ("$(\infty,1)$-" or "derived-")**center** of $A$:
  
$$
  Z(A) := Hom_{A\otimes A^{op}}(A,A).
$$
 
Dually, the Hochschild homology object when $N=A$ is called the [[universal trace]] or *shadow*.  In this case, if $A = \mathcal{O}(X)$ can be identified with an $\infty$-algebra of functions on an object $X$, which is therefore commutative so that $A^{op}= A$, and if taking functions commutes with $(\infty,1)$-pullbacks, then 

$$
  Z(\mathcal{O}(X)) \simeq \mathcal{O}(X \times_{X \times X} X)
  \simeq
  \mathcal{O}(\mathcal{L}X)
$$

is the $\infty$-algebra of functions on the [[free loop space object]] of $X$.
 

### Properties

By the [Hochschild-Kostant-Rosenberg theorem](#HochschildKostantRosenberg) and its generalizations, the Hochschild homology $HH_\bullet(\mathcal{O}(X),\mathcal{O}(X))$ of an ordinary algebra tends to behave like the algebra of [[Kähler differentials]] of $\mathcal{O}(X)$. More generally, this computes the [[cotangent complex]] of the $\infty$-algebra $\mathcal{O}(X)$. The [[cup product]] gives the wedge product of forms and the $S^1$-action the de Rham differential. 

Dually this means that in [[derived geometry]] the free loop space object $\mathcal{L} X$ consists of [[infinitesimal object|infinitesimal]] loops in $X$ (in ordinary geometry it would be equal to $Spec A$, consisting only of constant loops).

Analogously, Hochschild _cohomology_ $HH^\bullet(\mathcal{O}(X), \mathcal{O}(X))$ of  $\mathcal{O}(X)$ computes the [[multivector field]]s on $X$. There are pairing operations on HH homology and cohomology that make them support a general differential calculus on $X$, which makes sense even if $\mathcal{O}(X)$ is a noncommutative algebra.



## Definition {#Details}


We start with the general-abstract definition of Hochschild homology and then look at special and more traditional cases.

### General abstract {#GeneralAbstractDefinition}

We look at the very general abstract definition of Hochschild (co)homology and some important subcases.

#### Hochschild homology

We discuss Hochschild homology of commutative algebras for the case that these are related to function algebras on derived loop spaces.

+-- {: .num_defn #DefByTensoring}
###### Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]] that admits [[function algebras on ∞-stacks]] (see there for details)

$$
  Alg^{op} \stackrel{\overset{\mathcal{O}}{\longleftarrow}}{\underset{}{\longrightarrow}}
  \mathbf{H}
  \,.
$$

In particular the [[(∞,1)-category]] of [[∞-algebra]]s $Alg^{op}$ is [[(∞,1)-colimit|(∞,1)-tensored]] over [[∞Grpd]]. Then for $A \in Alg$ and $K \in \infty Grpd$ we say that

$$
  K \cdot A \in Alg
$$

is the _Hochschild homology complex_ of $A$ over $K$.

We say  a full [[sub-(∞,1)-category]] of $\mathbf{H}$ consists of **$\mathcal{O}$-perfect objects** if on these $\mathcal{O}$ commutes with [[(∞,1)-limit]]s.

Then for $X$ an $\mathcal{O}$-perfect object we have 

$$
  K \cdot \mathcal{O}(X)
   \simeq
  \mathcal{O}(X^{K}) 
  \,.
$$

=--

For $K = S^1$ the [[circle]], this is _ordinary_ Hochschild homology, while for general $K$ it is called _higher order Hochschild homology_ .




+-- {: .num_example}
###### Example

For $\mathcal{O}$ the functor that forms [[symmetric monoidal (∞,1)-category|symmetric monoidal (∞,1)-categories]] of [[quasicoherent sheaf|quasicoherent ∞-stacks of modules]] over [[∞-stack]]s over an [[(∞,1)-site]] of [[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]] for the ordinary theory of commutative $k$-algebras this has setup been considered in detail in ([Ben-ZviFrancisNadler](#Ben-ZviFrancisNadler)).

=--

The following definition formalizes large classes of $\mathcal{O}$-perfect objects given by [[representable functor|representables]].

+-- {: .num_defn}
###### Definition

Let $T$ be an [[(∞,1)-algebraic theory]] and $T Alg_\infty$ its [[(∞,1)-category]] of $\infty$-algebras. Let $C$ with $T \hookrightarrow C \hookrightarrow T Alg_\infty^{op}$ be a [[small (∞,1)-category|small]] full [[sub-(∞,1)-category]] of $T Alg_\infty^{op}$ which is closed under [[(∞,1)-limit]]s in $T Alg$ and equipped with the structure of a [[subcanonical coverage|subcanonical]] [[(∞,1)-site]]. 

Take $\mathbf{H} := Sh(C)$ the [[(∞,1)-category of (∞,1)-sheaves]] on $C$. This is an [[(∞,1)-topos]] for [[derived geometry]] modeled on $T Alg_\infty$.  Write $C \hookrightarrow \mathbf{H}$ for the [[(∞,1)-Yoneda embedding]].

For $X \in C\stackrel{}{\hookrightarrow} \mathbf{H} $ write $\mathcal{O}(X)$ for the same object regarded as an object of $T Alg_\infty$.

=--

+-- {: .num_defn}
###### Proposition/Definition 

In the context of the above definition we have 

$$
  \mathcal{O} (\mathcal{L}X) \simeq S^1 \cdot \mathcal{O}(X) \in T Alg_\infty
  \,,
$$

where on the right we have the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring">(∞,1)-tensoring</a> of $T Alg_\infty$ over $\infty Grpd$, which is the [[(∞,1)-colimit]] over the [[diagram]] $S^1$ of the [[(∞,1)-functor]] constant on $\mathcal{O}(X)$

$$
  S^1 \cdot \mathcal{O}(X) \simeq {\lim_{\to}}_{S^1} \mathcal{O}(X)
  \,.
$$

This object we call the **Hochschild homology complex** of $\mathcal{O}X$.

Generally for higher order Hochschild homology we have

$$
  \mathcal{O}(X^K) \simeq K \cdot \mathcal{O}(X) 
   \simeq
   {\lim_{\to}}_{K} \mathcal{O}(X)
   \in T Alg_\infty
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because the [[(∞,1)-Yoneda embedding]] preserves [[(∞,1)-limits]] the limit $X^K$ may be computed in $C$. By assumption $C$ is closed under limits in $T Alg_\infty^{op}$. The limit $X^K$ in $T Alg^{op}$ is the colimit $K \cdot \mathcal{O}(X)$ in the [[opposite (∞,1)-category]] of $\infty$-algebras.

=--

This definition of general higher order Hochschild homology by $(\infty,1)$-copowering is 

* explicit in [To&#235;nVezzosi](#ToenVezzosi), for ordinary Hochschild homology, hence $K = S^1$,

* almost explicit in ([GinotTradlerZeinalian](#GinotTradlerZeinalian)), for higher order Hochschild homology for [[dg-algebra]]s. Details on that are below in the section [Higher order Hochschild homology modeled on cdg-algebras](#OvercdgAlgs)

* explicit in [Ben-Zvi/Francis/Nadler, corollary 4.12](#Ben-ZviFrancisNadler) for HH with values in [[quasicoherent sheaf|quasicoherent ∞-stacks]] and over perfect $\infty$-stacks (see there for details).

#### Topological chiral homology {#TopologicalChiralHomology}

Notice that the tensoring that gives the Hochschild homology is given by the $\infty$-colimit over the constant functor

$$
  K \cdot A \simeq {\lim_\to}_K A
  \,.
$$

This generalizes to $\infty$-colimits of functors constant on an algebra, but over a genuine [[(∞,1)-category]] diagram.

Specifically let $X$ be framed $n$-manifold, $A$ an [[little k-cubes operad|En-algebra]] and $D_X$ the [[(∞,1)-category]] whose objects are framed embeddings of disjoint unions of open discs into $X$ and morphisms are inclusions of these. Let $F_A$ be the functor that assigns $A^{k}$ to an object corresponding to $k$ discs in $X$, and iterated products/units to morphisms 

Then the [[(∞,1)-colimit]]

$$
  {\lim_\to}_{D_X} F_A
$$

is called the [[topological chiral homology]] of $X$.

For $A$ an ordinary associatve algebra, hence in particular an $E_1$-algebra, and $X$ the circle, this reproduces the ordinary Hochschild homology of $A$ (see below).

For more details see ([GinotTradlerZeinalian](#GinotTradlerZeinalian)).

### Specific concrete

We unwind the above general abstract definition in special classes of examples and find more explicit and more traditional definitions of Hochschild homology.

#### Pirashvili's higher order Hochschild homology {#PirashviliHigherOrder}

We demonstrate how the above $(\infty,1)$-category theoretic definition of higher order Hochschild homology reproduces the simplicial definition by ([Pirashvili](#Pirashvili)).

+-- {: .num_prop}
###### Proposition

Let $T$ be a [[Lawvere theory]] regarded as a 0-[[truncated]] [[(∞,1)-algebraic theory]]. 

Consider a [[model structure on simplicial T-algebras]]/on [[homotopy T-algebras]] [[presentable (∞,1)-category|presenting]] $T Alg_\infty$ such that 

1. it is a [[simplicial model category]];

1. [[tensoring]] with simplicial sets preserves weak equivalences and hence cofibrant replacement.

Then for $\mathcal{O}(X) \in T Alg \hookrightarrow T Alg_\infty$ and $K \in \infty Grpd$ the higher order Hochschild homology complex $K \cdot \mathcal{O}(X)$  is presented by the ordinary [[tensoring]] $K \cdot \mathcal{O}(X)$ in the model category, for $K$ any [[simplicial set]] incarnation of the $\infty$-groupoid.

=--

+-- {: .proof}
###### Proof

The $(\infty,1)$-tensoring in an $(\infty,1)$-category [[presentable (∞,1)-category|presented]] by a [[simplicial model category]] is modeled by the ordinary [[tensoring]] of the latter on a cofibrant [[resolution]] of the given object. This is discussed in the section <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#ModelsForTensoring">∞-tensoring -- models</a>.

=--

+-- {: .num_remark}
###### Remark

We can always use the [[model structure on homotopy T-algebras]] to satisfy the assumption of the above proposition. That is a [[simplicial model category]] for every $T$ and every ordinary algebra is cofibrant in this structure. 

Notice that in this model category even if $\mathcal{O}(X)$ is fibrant (which it is if $\mathcal{O}X$ is an ordinary algebra), then $K \cdot \mathcal{O}(X)$ is in general far from being fibant. Computing the [[simplicial homotopy group]]s of $K \cdot \mathcal{O}(X)$ and hence the Hochschild homology involves passing to a fibrant reolsution of $K \cdot \mathcal{O}(X)$ first, that will make it a [[homotopy T-algebra]].

On the other hand, if we find a simplicial [[model structure on simplicial T-algebras]] (which are degreewise genuine $T$-algebras) then the coproducts involved degreewise in forming $K \cdot \mathcal{O}(X)$ will be [[tensor products of algebras]], and hence in particular themselves again algebras. For such a model the tensoring $K \cdot \mathcal{O}(X)$ yields explicitly (under the [[Dold-Kan correspondence]]). 

This is the case for the tensoring of [[dg-algebra]]s over simplicial sets and leads to [[Teimuraz Pirashvili]]'s formulation of higher order Hochschild homology for ordinary algebras ([Pirashvili](#Pirashvili)). 

This we describe below 

* for ordinary Hochschild homology in [Examples -- Simplicial algebra on the circle](#TensoringWithSimplicialCircleAlgebra);

* for higher order Hochschild homology of dg-algebras in [Higher order Hochschild homology modeled on cdg-algebras](#OvercdgAlgs).

=--


## Examples

We first give a detailed discussion of the standard Hochschild complex of a commutative algebra, but  from the general abstract $(\infty,1)$-category theoretic point of view. 

Then we look in detail at higher order Hochschild homology in the $(\infty,1)$-topos over an [[(∞,1)-site]] of formal duals of [[dg-algebra]]s. In this context the classical [theorem by Jones](#JonesTheorem) on Hochschild homology and loop space cohomology is a natural consequence of the general machinery.

### Gradings and conventions {#GradingsAndConventions}

In [[derived geometry]] two categorical gradings interact: a [[cohesive (∞,1)-topos|cohesive]] $\infty$-groupoid $X$ has a space of [[k-morphism]]s $X_k$ for all non-negative $k$, and each such has itself a _[[simplicial T-algebra]]_ of functions with a component in each non-positive degree. But the directions of the face maps are opposite. We recall the grading situation from [[function algebras on ∞-stacks]].

Functions on a bare $\infty$-groupoid $K$, modeled as a [[simplicial set]], form a [[cosimplicial algebra]] $\mathcal{O}(K)$, which under the [[monoidal Dold-Kan correspondence]] identifies with a cochain [[dg-algebra]] (meaning: with positively graded differential) in non-negative degree

$$
  \left(
    \array{
        \vdots
       \\
       \downarrow \downarrow \downarrow \downarrow      
        \\
        K_2
       \\
       \downarrow^{\partial_0} \downarrow^{\partial_1} \downarrow^{\partial_2}
       \\
       K_1
       \\
       \downarrow^{\partial_0} \downarrow^{\partial_1}
       \\
       K_0
     }
  \right)
   \;\;\;\;\;
   \stackrel{\mathcal{O}}{\mapsto}
   \;\;\;\;\;
  \left(
  \array{
    \vdots
    \\
    \uparrow \uparrow \uparrow \uparrow   
    \\
    \mathcal{O}(K_2)
    \\
    \uparrow^{\partial_0^*} \uparrow^{\partial_1^*} \uparrow^{\partial_2^*}
    \\
    \mathcal{O}(K_1)
    \\
    \uparrow^{\partial_0^*} \uparrow^{\partial_1^*}
    \\
    \mathcal{O}(K_0)
  }
  \right)
   \;\;\;\;\;
  \stackrel{\sim}{\leftrightarrow}
   \;\;\;\;\;
  \left(
    \array{
     \cdots
     \\
     \uparrow^{\mathrlap{\sum_i (-1)^i \partial_i^*}}
     \\
     A_2
     \\
     \uparrow^{\mathrlap{\sum_i (-1)^i \partial_i^*}}
     \\
     A_1
     \\
     \uparrow^{\mathrlap{\sum_i (-1)^i \partial_i^*}}
     \\
     A_0
     \\
     \uparrow
     \\
     0
     \\
     \uparrow
     \\
     0
     \\
     \uparrow
     \\
     \vdots
   }
  \right)
  \,.
$$

On the other hand, a representable $X$ has itself a _[[simplicial T-algebra]]_ of functions, which under the monoidal Dold-Kan correspondence also identifies with a cochain dg-algebra, but then necessarily in non-positive degree to match with the above convention. So we write

$$
  \mathcal{O}(X)
   \;\;\;\;\;
  =
   \;\;\;\;\;
  \left(
   \array{
     \mathcal{O}(X)_0
     \\
     \uparrow \uparrow
     \\
     \mathcal{O}(X)_{-1}
     \\
     \uparrow \uparrow \uparrow
     \\
     \mathcal{O}(X)_{-2}
     \\
     \uparrow \uparrow \uparrow \uparrow
     \\
     \vdots
   }
  \right)
   \;\;\;\;\;
  \stackrel{\sim}{\leftrightarrow}
   \;\;\;\;\;
  \left(
    \array{
        \vdots
        \\
        \uparrow
        \\
        0
        \\
        \uparrow
        \\
        0
        \\
        \uparrow
        \\
       \mathcal{O}(X)_0
       \\
       \uparrow
       \\
       \mathcal{O}(X)_{-1}
       \\
       \uparrow
       \\
       \mathcal{O}(X)_{-2}
       \\
       \uparrow
       \\
       \vdots
    }
  \right)
  \,.
$$

Taking this together, for $X_\bullet$ a general [[∞-stack]], its function algebra is generally an _unbounded_ cochain dg-algebra with mixed contributions as above, the simplicial degrees contributing in the positive direction, and the homological resolution degrees in the negative direction:

$$
  \mathcal{O}(X_\bullet)
   \;\;\;\;\;
   =
   \;\;\;\;\;
  \left(
     \array{
        \vdots
        \\
        \uparrow
        \\
        \bigoplus_{k-p = q} \mathcal{O}(X_k)_{-p}
        \\
        \uparrow
        \\
        \vdots
        \\
        \uparrow^d
        \\
        \mathcal{O}(X_1)_0 \oplus \mathcal{O}(X_2)_{-1} \oplus 
          \mathcal{O}(X_3)_{-2} \oplus \cdots
        \\
        \uparrow^{d}
        \\
        \mathcal{O}(X_0)_0 \oplus \mathcal{O}(X_1)_{-1} \oplus 
          \mathcal{O}(X_2)_{-2} \oplus \cdots
        \\
        \uparrow^{d}
        \\
        \mathcal{O}(X_0)_{-1} \oplus \mathcal{O}(X_1)_{-2} \oplus 
          \mathcal{O}(X_2)_{-3}\oplus \cdots       
        \\
        \uparrow^{d}
        \\
        \vdots
     }
  \right)
  \,.
$$ 

### The Hochschild chain complex of an associative algebra {#HochschildChainComplex}

We consider in detail the classical case of Hochschild (co)homology of an [[associative algebra]] approaching it from the general abstract perspective on Hochschild homology. 

This section focuses on exposition. The formal context in which the constructions considered here follow from first principles is discussed below in [Higher order Hochschild homology modeled on cdg-algebras](#OvercdgAlgs)

#### The simplicial circle {#SimplicialCircleAlgebra}

We shall use two different equivalent models of the circle in $\infty Grpd$ in terms of models in $sSet$:

1. the simplicial set $\Delta[1]/\partial \Delta[1]$

   This is not fibrant (not a [[Kan complex]]). On the contrary, this is
   the smallest simplicial model available for the circle, with the least 
   number of horn fillers.

   In low degrees it looks as follows

   $$
     \array{
       \vdots && \vdots
       \\
       (\Delta[1]/\partial\Delta[1])_3
        & = &
       (* * * *) \coprod (* \to * * *) \coprod (* * \to * *) \coprod (* * * \to * ) 
       &
       \\
       \\
       (\Delta[1]/\partial\Delta[1])_2 
         & = & (* * *) \coprod (*\to* *) \coprod (* * \to *)
       \\
       \\
       (\Delta[1]/\partial\Delta[1])_1 & = & (* *) \coprod  (* \to *)
       \\
       \\
       (\Delta[1]/\partial\Delta[1])_0 & = &  (*) 
     }
     \,.
   $$

   Here for instance the expression $(* * \to * )$ denotes the morphism of simplicial sets $\Delta[2] \to \Delta[1]/\partial \Delta[1]$ that sends the first edge (the 2-face) of the 2-simplex to the unique degenerate 1-cell and the second edge (the 0-face) to the unique non-degenerate 1-cell of $\Delta[1]/ \partial \Delta[1]$.

1. the [[nerve]] of the [[delooping]] [[groupoid]] $\mathbf{B}\mathbb{Z}$ of the additive group of [[integer]]s.

   This model is fibrant (is a [[Kan complex]]) and makes manifest the group structure on $S^1$, which is the [[strict 2-group]] structure on $\mathbf{B}\mathbb{Z}$ or equivalently the structure of a [[simplicial group]] on its [[nerve]].

   $$
      \mathbf{B}\mathbb{Z} \times \mathbf{B}\mathbb{Z} \to 
        \mathbf{B}\mathbb{Z}
   $$

   $$
      ((* \stackrel{k}{\to} * ), (* \stackrel{l}{\to} * ))
      \mapsto
      (* \stackrel{k+l}{\to} * )
      \,.
   $$


#### Tensoring with the simplicial circle
{#TensoringWithSimplicialCircleAlgebra}

Let $A \in CAlg_k$ be a commutative [[associative algebra]] over a commutative [[ring]] $k$.

Above in the section on [Higher order Hochschild homology](#PirashviliHigherOrder) we had discussed how the Hochschild homology of $A$ is given by the [[simplicial algebra]] $(\Delta[1]/\partial \Delta[1]) \cdot A \in CAlg_k^{\Delta^{op}}$ that is the [[tensoring]] of $A$ regarded as a constant simplicial algebra with the [[simplicial set]] $\Delta[1]/\partial \Delta[1]$ (the 1-[[simplex]] with its two 0-cells identified).

We describe now in detail what this simplicial circle algebra looks like. The proof that this construction is indeed homotopy-good is given below in [As functions on the derived loop space](#FuncsOnDerivedLoopSpace)



When forming the [[copower]]ing of $A$ with the simplicial circle $S^1$, we get the same structure as displayed above, but with one copy of $A$ for each item in parenthesis. 

To be very explicit, we recall and demonstrate the following elementary fact.

+-- {: .num_prop}
###### Proposition

In $CAlg_k$ the [[coproduct]] is given by the [[tensor product]] over $k$:

$$
  \left(
  \array{
    A 
      &\stackrel{i_A}{\to}& 
    A \coprod B 
      &\stackrel{i_B}{\leftarrow}& 
    B
   }
  \right)
  \simeq
  \left(
    \array{
      A 
        &\stackrel{Id_A \otimes_k e_B}{\to}& 
      A \otimes_k B 
        & \stackrel{e_A \otimes Id_B}{\leftarrow}&
      B
   }
  \right)
$$

=--

+-- {: .proof}
###### Proof

We check the [[universal property]] of the coproduct: for $C \in CAlg_k$ and $f,g : A,B \to C$ two morphisms, we need to show that there is a unique morphism $(f,g) : A \otimes_k B \to C$  such that the diagram

$$
  \array{
    A 
     &\stackrel{Id_A \otimes e_B}{\to}&
    A \otimes_k B
     &\stackrel{e_A \otimes Id_B}{\leftarrow}&
    B
    \\
    & {}_{\mathllap{f}}\searrow & \downarrow^{\mathrlap{(f,g)}} & \swarrow_{\mathrlap{g}} 
    \\
    && C
  }
$$

commutes.
For the left triangle to commute we need that $(f,g)$ sends elements of the form $(a,e_B)$ to $f(a)$. For the right triangle to commute we need that $(f,g)$ sends elements of the form $(e_A, b)$ to $g(b)$. Since every element of $A \otimes_k B$ is a product of two elements of this form

$$
  (a,b) = (a,e_B) \cdot (e_A, b)
$$

this already uniquely determines $(f,g)$ to be given on elements by the map

$$
  (a,b) \mapsto f(a) \cdot g(b)
  \,.
$$

That this is indeed an $k$-algebra homomorphism follows from the fact that $f$ and $g$ are

=--

Notice that for all this it is crucial that we are working with commutative algebras.

+-- {: .num_cor}
###### Corollary

We have that the tensoring of $A$ with the map of sets from two points to the single point

$$
  (* \coprod * \to *) \cdot A
  \simeq
  (
    A \otimes_k A
     \stackrel{\mu}{\to}
    A
  )
$$

is the product morphism on $A$. And that the tensoring with the map from the empty set to the point 

$$
  (\emptyset \to *)\cdot A
  \simeq
  (k \stackrel{e_A}{\to} A)
$$

is the unit morphism on $A$. Generally, for $f : S \to T$ any map of sets we have that the tensoring

$$
  (S \stackrel{f}{\to} T) \cdot A
  =
  A^{\otimes_k |S|}
  \to
  A^{\otimes_k |T|}
$$

is the morphism between [[tensor power]]s of $A$ of the cardinalities of $S$ and $T$, respectively, whose component over a copy of $A$ on the right corresponding to $t \in T$ is the iterated product $A^{\otimes_k |f^{-1}\{t\}|} \to A$ on as many tensor powers of $A$ as there are elements in the preimage of $t$ under $f$.

=--


We see that in low degree the simplicial algebra $(\Delta[1]/\partial \Delta[1]) \cdot A$ has the components 

$$
  \array{
    \vdots && \vdots
    \\
    ((\Delta[1]/\partial\Delta[1]) \cdot A)_3
     & = &
    A \otimes A \otimes A \otimes A
    &
    \\
    \\
    ((\Delta[1]/\partial\Delta[1]) \cdot A)_2 
      & = & A \otimes A \otimes A
    \\
    \\
    ((\Delta[1]/\partial\Delta[1]) \cdot A)_1 & = & A \otimes A
    \\
    \\
    ((\Delta[1]/\partial\Delta[1]) \cdot A)_0 & = &  A 
  }
  \,.
$$

The two face maps from degree 1 to degree 0 both come from mapping two points to a single point, so they are both the product on $A$.

$$
  A \otimes_k A \stackrel{\overset{\mu}{\longrightarrow}}{\underset{\mu}{\longrightarrow}} A
  \,.
$$

The three face maps from degree 3 to degree 2 are more interesting. We have

$$
  \partial^2_0
  \;\;\;
  :
  \;\;\;
  \array{
    (* * *)   &\mapsto & (* *)
    \\
    \coprod  & \nearrow &\coprod&  
    \\
    (* \to * *) & & (* \to *)
    \\
    \coprod &\nearrow&& 
    \\
    (* * \to *)
  }
$$

and

$$
  \partial^2_1
  \;\;\;
  :
  \;\;\;
  \array{
    (* * *)   &\mapsto & (* *)
    \\
    \coprod  &  &\coprod&  
    \\
    (* \to * *) & \mapsto & (* \to *)
    \\
    \coprod &\nearrow&& 
    \\
    (* * \to *)
  }
$$

and

$$
  \partial^2_2
  \;\;\;
  :
  \;\;\;
  \array{
    (* * \to *)   &\mapsto & (* *)
    \\
    \coprod  & \nearrow &\coprod&  
    \\
    (* * *) &  & (* \to *)
    \\
    \coprod &\nearrow&& 
    \\
    (* \to * *)
  }
  \,.
$$

Notice that for the last one we had to cyclically permute the source in order to display the maps in this planar fashion.

So therefore we get the tensorings

$$
  (\partial^2_0) \cdot A =
  (
   A \otimes_k A \otimes_k A
     \stackrel{\mu \otimes_k Id}{\to}
   A
  )
$$

and

$$
  (\partial^2_1) \cdot A =
  (
   A \otimes_k A \otimes_k A
     \stackrel{Id \otimes_k \mu}{\to}
   A
  )
$$

and

$$
  (\partial^2_2) \cdot A =
  (
   A \otimes_k A \otimes_k A
     \stackrel{\mu \otimes_k Id \circ \sigma_{2,3,1}}{\to}
   A
  )
  \,.
$$


In summary we have so far 

$$
  (\Delta[1]/\partial \Delta[1])\cdot A =
  \left(
     \cdots 
    A\otimes_k A \otimes_k A
      \stackrel{\overset{\mu \otimes_k Id \sigma_{2,3,1}}{\to}}{\stackrel{\overset{Id \otimes_k \mu}{\longrightarrow}}{\underset{\mu \otimes_k Id}{\longrightarrow}}} A \otimes_k A
    \stackrel{\overset{\mu}{\longrightarrow}}{\underset{\mu}{\longrightarrow}}A 
  \right)
  \,.
$$


The [[Moore complex]] of this simplicial algebra is the traditional **Hochschild chain complex** of $A$

$$
  C_\bullet(A,A) = C_\bullet((\Delta[1]/\partial \Delta[1]) \cdot A)
  \,.
$$

This we describe in more detail in the section [Explicit description of the Hochschild complex](#ExplicitHochschildChains).


Generally, for $K$ any simplicial set, $K \cdot A$ is the simplicial algebra whose Moore complex is the complex that ([Pirashvili](#Pirashvili)) uses to define higher order Hochschild homology.



#### Identification with K&#228;hler differential forms {#IdWithK&#228;hlerForOrdAlgebra}

We spell out in detail how in degree 0 and 1 the [[homology]] of the Hochschild complex of $A$ is that of its [[Kähler differential form]]s. Under mild conditions on $A$ this is also true in higher degrees, which is the statement of the [Hochschild-Kostant-Rosenberg theorem](#HochschildKostantRosenberg).


+-- {: .num_prop #Kaehler1Forms}
###### Proposition

The [[homology]] of the Hochschild complex $S^1 \cdot A$ in degree 1 is the  [[Kähler differential form]]s of $A$

$$
  HH_1(A,A) = H_\bullet(S^1\cdot A) \simeq \Omega^1_K(A/k)
  \,.
$$

The [[isomorphism]] is induced by the identifications

$$
  \array{
    \vdots
    \\
     (f \in A_{(* * * )}, g \in A_{(*\to * *)}, h \in A_{(* * \to *)} 
     & \mapsto & \frac{1}{2} f \wedge d g \wedge d h
    \\
    (f \in A_{(* *)}, g \in A_{* \to *}) &\mapsto& f \wedge d g
    \\
    (f \in A_{(*)}) & \mapsto & f 
  }
  \,,
$$

where on the left we display elements of $A^{\otimes_k}$ under the [above](#TensoringWithSimplicialCircleAlgebra) identification of these tensor powers in $S^1 \cdot A$.

=--

+-- {: .proof}
###### Proof

By the above discussion, the [[Moore complex]]-differential acts on  $(f,g,h) \in A \otimes_k A \otimes_k A$ by

$$
  \begin{aligned}
    \partial (f,g,h)
    &=
    (f g, h) - (f, g h) + (h f, g)
    \\
    &
    \sim
    f g \wedge d h -  f \wedge d (g h) + f h \wedge d g
  \end{aligned}
  \,.
$$  

The last term on the right is precisely the term by which one has to quotient out the module of formal expressions $f \wedge d g$ to get the module of [[Kähler differential]]s: setting it to 0 is the [[derivation]] property of $d$

$$
  (\partial (f,g,h) = 0)
  \Leftrightarrow
  f \wedge ( d(g h) = h \wedge d g + g \wedge d h )
  \,.
$$

Therefore we have manifestly

$$
  \Omega^1_K(A) \simeq C_1(A,A)/im(\partial)
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

We may also compute the $\partial$-homology on the [[normalized chain complex]], which is in degree 1 the quotient of $A \otimes_k A$ by the image of the degeneracy map $\sigma : A \to A \otimes_k A$, which is

$$
  \left(
    \array{
      (*) &\to& (* *)
      \\
      \coprod && \coprod
      \\
      \emptyset &\to& (* \to *)
    }
  \right)
  \cdot 
  A  
$$

and thus maps

$$
  f \mapsto f \wedge d 1
  \,.
$$

So passage to the normalized chains imposes the condition

$$
  d 1 = 0
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Under the identification of $HH_\bullet(A,A) = H_\bullet(S^1 \cdot A)$ with K&#228;hler differential forms, the [[cup product]] on homology identifies with the [[exterior algebra|wedge product]] of differential 0- and 1-forms.

=--

+-- {: .proof}
###### Proof

Under the [[monoidal Dold-Kan correspondence]] the product on the [[Moore complex]] $N_\bullet(S^1 \cdot A)$ is given by the [[Eilenberg-Zilber map]] $\nabla$

$$
  N_\bullet(S^1 \cdot A) \otimes_k
  N_\bullet(S^1 \cdots)
  \stackrel{\nabla}{\to}
  N_\bullet((S^1 \cdot A) \otimes (S^1 \cdot A))
  \stackrel{N_\bullet(\cdot)}{\to}
  N_\bullet(S^1 \cdot A)
  \,,
$$

where for $\omega \in (S^1\cdot A)_p $ and $\lambda \in (S^1 \cdot A)_q$ we have

$$
  \nabla : \omega \otimes \lambda \mapsto 
  \sum_{(\mu,\nu)\in Shuff(p,q)} sign(\mu,\nu) s_\nu(\omega) \otimes s_\mu(\lambda)
  \,.
$$

For instance for $\omega = f \wedge d g \in (S^1 \cdot A )_0$  we have

$$
  s_1 (f \wedge d g) = f \wedge d g \wedge d 1
$$

and

$$
  s_2(h \wedge d q) = (h \wedge d 1 \wedge d q)
$$

and the tensor product (in $(S^1 \cdot A)_2$!) is componentwise

$$
  s_1(f \wedge d g) \otimes s_2(h \wedge d q) = (f \otimes h) \wedge 
   d(g \otimes 1) \wedge d(1 \otimes q) 
  \,.
$$

Therefore

$$
  \nabla(\omega, \lambda) = f h \wedge d q \wedge d q
  \,.
$$ 

=--


#### The simplicial circle action {#SimplicialCircleActionForOrdAlgebra}

We describe the canonical [[action]] of the [[automorphism 2-group]] of the circle $S^1$ on $S^1 \cdot A$ and how its degree-1 part induces under the [above](#IdWithK&#228;hlerForOrdAlgebra) identification $H_\bullet(S^1 \cdot A) \simeq \Omega^\bullet_K(A)$ the action of the de Rham differential.

+-- {: .num_prop}
###### Proposition


The [[automorphism 2-group]] of the categorical circle is

$$
  Aut_{\infty Grpd}(\mathbf{B}\mathbb{Z}, \mathbf{B}\mathbb{Z})
  \simeq
  \coprod_{\{+1,-1\}} \mathbf{B}\mathbb{Z}
  \,.
$$

=--

+-- {: .proof}
###### Proof

We may compute the automorphism 2-group in the full [[sub-(∞,1)-category]] [[Grpd]] $\subset$ [[∞Grpd]], whose morphisms are [[functor]]s and 2-morphisms are [[natural isomorphism]]s (see the statement about [[homotopy n-type|homotopy 1-types]] at [[homotopy hypothesis]] for details). A functor between [[delooping]] [[groupoid]]s $\mathbf{B}G \to \mathbf{B}H$ is precisely a [[group]] [[homomorphism]] $G \to H$. The additive group endomorphisms of $\mathbb{Z}$ are precisely given by multiplication with elements in $\mathbb{Z}$, the two automorphisms in there are $\pm 1$.

The natural transformations between such functors are 

$$
  \left(
    \array{
      & \nearrow \searrow^{\mathrlap{\pm 1}}
      \\
      \mathbf{B}\mathbb{Z}
      & \Downarrow^{r}&
      \mathbf{B}\mathbb{Z}
      \\
      & \searrow \nearrow_{\mathrlap{\pm 1}}
    }
  \right)
  \;\;
    :
  \;\;
  \left(
  \array{
    *
    \\
    \downarrow^{\mathrlap{1}}
    \\
    *    
  }
  \right)
  \;\;
   \mapsto
  \;\;
  \left(
  \array{
     * &\stackrel{r}{\to}& *
     \\
     {}^{\mathllap{\pm 1}}\downarrow && \downarrow^{\mathrlap{\pm 1}}
     \\
     * &\stackrel{r}{\to}& *
  }
  \right)
  \,.
$$

=--

Now consider the [[right homotopy]] that exhibits the morphism 1 in $Aut(\mathbf{B}\mathbb{Z})_{Id}$.

$$
  \array{  
    && \mathbf{B}\mathbb{Z}
    \\
    &{}^{\mathllap{Id}}\nearrow & \uparrow
    \\
    \mathbf{B}\mathbb{Z} &\stackrel{\eta}{\to}& \mathbf{B}\mathbb{Z}^{I} 
    \\
    &  {}_{\mathllap{Id}}\searrow
    \\
    && \mathbf{B}\mathbb{Z}
  }
  \,.
$$

This sends 

$$
  \eta : * \mapsto (* \stackrel{1}{\to} * )
  \,.
$$

This means that under [[copowering]] this on $A$

$$
  (\mathbf{B}\mathbb{Z} \to \mathbf{B}\mathbb{Z}^I)\cdot A
$$

we get in degree 0 the morphism

$$
  A_{*} \stackrel{Id}{\to} A_{* \to *} \hookrightarrow \bigotimes_r A_{* \stackrel{r}{\to} *}
  \,.
$$

Under the above identification of the homology of $\mathbf{B}\mathbb{Z} \cdot A$ with K&#228;hler forms, this is on elements the map

$$
  f \mapsto d f
  \,.
$$



+-- {: .num_remark}
###### Remark
**(automorphisms of the odd line)**

This means that under the identification of $(\mathbf{B}\mathbb{Z}) \cdot k \simeq C^\infty(k^{0|1})$ with functions on the [[odd line]],in degree 0 this corresponds to the even vector field $\theta \partial/\partial \theta$ on the odd line, and in degree 1 to the odd vector field $\partial/\partial\that$.

(...)

=--


#### Traditional description of the Hochschild complex {#ExplicitHochschildChains}

We spell out explicitly the Hochschild chain complex for an 
[[associative algebra]] (over some ring $k$) with coefficients in a [[bimodule]].


+-- {: .num_defn #PlainBarComplex}
###### Definition

The [[bar complex]] of $A$ is the [[connective chain complex|connective]] [[chain complex]]

$$
  \mathrm{B}_\bullet A :=
  (
    \cdots \to A^{\otimes_k n}
    \stackrel{\partial}{\to}
    A^{\otimes_k n-1}
    \to \cdots
    \to A \otimes_k A \otimes_k A 
    \stackrel{\partial}{\to}
    A \otimes_k A
  )
$$

which in degree $n$ has the $(n+1)$ [[tensor power]] of $A$ with itself, and whose [[differential]] is given by 

$$
  \partial(a_0, a_1, \cdots a_n)
  :=
  (a_0 a_1, a_2, \cdots, a_n)
  - 
  (a_0, a_1 a_2 , a_3, \cdots, a_n)
  + 
  \cdots
  - (-1)^n (a_0, a_1, \cdots, a_{n-1} a_n)
  \,,
$$ 

regarded as a chain complex in $A$-[[bimodule]]s for the evident bimodule structure in each degree.

=--

+-- {: .num_defn}
###### Definition

Let $N$ be an $A$-[[bimodule]]. The **Hochschild chain complex** $C_\bullet(A,N)$ of $A$ with coefficients in $N$ is the chain complex obtained by taking in the [bar complex](#PlainBarComplex) degreewise the [[tensor product]] of $A$-bimodules with $N$:

$$
  C_\bullet(A,N) := N_{A \otimes A^{op}}\mathrm{B}_\bullet A
  \,.
$$

The **Hochschild homology** of $A$ with coefficients in $N$ is the [[homology]] of the Hochschild chain complex, written

$$
  HH_n(A,N) := H_n( C_\bullet(A,N))
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

At the level of the underlying $k$-[[module]]s we have natural isomorphisms

$$
  N_{A \otimes_k A^{op}} A^{\otimes_k (n+2)}
  \simeq
  N \otimes_k \otimes A^{\otimes_k n}
$$

given on elements by sending

$$
  (\nu, (a_0, a_1, \cdots, a_n, a_{n+1}))
  \sim
  (a_{n+1} \nu a_{0}, (1, a_1, \cdots, a_n, 1))
  \mapsto
  (a_0 \nu a_{n+1}, a_1, \cdots, a_n)
  \,.
$$

The action of the differential in $C_\bullet(A,N)$ on elements of the latter form is then

$$
  \partial(\nu, a_1, \cdots, a_n)
  =
  (\nu a_1, a_2, \cdots, a_n)
  -
  (\nu, a_1 a_2, a_3, \cdots)
  + 
  \cdots
  +  
  (-1)^n
  (\nu , a_1, \cdots, a_{n-1} a_n)
  - (-1)^{n}
  (a_n \nu, a_1, a_2, \cdots, a_{n-1})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

In words this means that the Hochschild complex is obtained froms the bar complex by "gluing the two ends of a sequence of elements of $A$ to a circle by a bimodule".

The fact that the circle appears here has in fact a deep significance: the Hochschild chain complex may be understood in [[higher geometry]] as encoding functions on a [[free loop space object]] of whatever $A$ behaves like being functions on.

=--





#### As function algebra on the derived loop space {#FuncsOnDerivedLoopSpace}

We give a formal derivation of the Hochschild complex of an ordinary commutative associative algebra $\mathcal{O}(X)$ as the function algebra on the [[derived loop space]] object $\mathcal{L}X$ in the context of [[derived geometry]].

So let now $T$ be the [[Lawvere theory]] of ordiary commutative [[associative algebra]]s over a [[field]] $k$, regard as a 0-[[truncated]] [[(∞,1)-algebraic theory]]. 

+-- {: .num_defn}
###### Proposition

The [[(∞,1)-category]] $CAlg(k)_\infty$ of [[algebras over a Lawvere theory|∞-algebras]] over $T$ is [[presentable (∞,1)-category|presented]] by the [[model structure on simplicial T-algebras|model structure on simplicial commutative k-algebras]] $(CAlg_k^{\Delta^{op}})_{proj}$.

This is [[Quillen equivalence|Quillen equivalent]] to the standard [[model structure on dg-algebras|model structure on connected dg-chain algebras]].

$$
  (CAlg_k^{\Delta^{op}})_{proj}
  \simeq
  dgAlg_k^+
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

The first statement is discussed at [[(∞,1)-algebraic theory]] and [[homotopy T-algebra]]. The second statement is discussed at [[monoidal Dold-Kan correspondence]].

=--

Let 

$$
  T \subset C \subset  T Alg_\infty^{op}
$$

be a [[subcanonical coverage|subcanonical]] [[(∞,1)-site]] that is a full 
[[sub-(∞,1)-category]] of formal duals of $\infty$-$T$-algebras, closed under [[(∞,1)-limit]]s in $T Alg_\infty^{op}$. 

Let 

$$
  \mathbf{H} \coloneqq Sh_{(\infty,1)}(C)
$$ 

be the [[(∞,1)-sheaf (∞,1)-topos]] over $C$. 

Following the notation at [[Isbell duality]] and [[function algebras on ∞-stacks]] we write $\mathcal{O}(X) \in T Alg_\infty$ for an object that under the [[(∞,1)-Yoneda embedding]] $C \hookrightarrow T Alg_\infty^{op} \to \mathbf{H}$ maps to an object called $X$ in $\mathbf{H}$.

+-- {: .num_defn}
###### Definition

For $\mathcal{O}(X) \in T Alg \hookrightarrow T Alg_\infty$ an ordinary $T$-algebra, we say that the [[free loop space object]] 

$$
  \mathcal{L}X \coloneq [S^1,X]
$$ 

of $X$ formed in $\mathbf{H}$ is the **[[derived loop space]]** of $X$.

=--

+-- {: .num_remark}
###### Remark

The term _derived_ is just to emphasize that we do not form the [[free loop space object]] in an [[(∞,1)-topos]] of $(\infty,1)$-sheaves over a 1-[[site]] inside the 1-category $Alg_k^{op}$. These "underived" (not embedded into [[(∞,1)-category theory]]) free loop space objects would just be equivalent to $X$. The [[derived loop space]] instead has rich interesting structure.

But if the ambient context of [[higher geometry]] over the genuine [[(∞,1)-site]] of formal duals to $\infty$-algebras is clear, we can just speak of _free loop space objects_ . They are canonically given.

=--

+-- {: .num_prop #LimitInAlg}
###### Proposition 

We have that $\mathcal{O}(\mathcal{L}X)$ is given by the [[(∞,1)-pushout]] in $CAlg_\infty$ 

$$
  \mathcal{O}\mathcal{L}X \simeq \mathcal{O}(X) \coprod_{\mathcal{O}(X)\otimes \mathcal{O}(X) } \mathcal{O}(X)
$$

hence by the universal [[cocone]]

$$
  \array{
    \mathcal{O}\mathcal{L}X &\leftarrow&
    \mathcal{O}(X)
    \\
    \uparrow && \uparrow
    \\
    \mathcal{O}(X) &\leftarrow& \mathcal{O}(X) \otimes \mathcal{O}(X)
  }
$$

=--

+-- {: .proof}
###### Proof

Since [[∞-stackification]] $L : PSh_{(\infty,1)}(C) \to \mathbf{H}$ is a [[left exact (∞,1)-functor]] and hence preserves finite [[(∞,1)-limit]]s, we have that the defining pullback for $\mathcal{L}X$ may be computed in the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$. Since the [[(∞,1)-Yoneda embedding]] preserves all [[(∞,1)-limit]]s this in turn may be computed in the [[(∞,1)-site]] $C$, hence by assumption in $T Alg_\infty$. The relevant $(\infty,1)$-pullback there is the claimed $(\infty,1)$-pushout in the [[opposite (∞,1)-category]] $T Alg_\infty$. 

=--

+-- {: .num_prop}
###### Proposition

The $\infty$-algebra $\mathcal{O} \mathcal{L}X$ of functions on the derived loop space of $X$ is when modeled by a simplicial algebra in $CAlg_k^{\Delta^{op}}$ under the [[monoidal Dold-Kan correspondence]] equivalent to the Hochschild chain complex of $\mathcal{O}X$ with coefficients in itself:

$$
  \mathcal{O} \mathcal{L}X \simeq C_\bullet(\mathcal{O}(X), \mathcal{O}(X))
  \,.
$$

=--

+-- {: .proof}
###### Proof

First observe that the [[coproduct]] in $CAlg_k$ is the 
[[tensor product of commutative algebras]]  over $k$

$$
  A \coprod B = A \otimes_k B
  \,.
$$

By the discussion at [[homotopy T-algebra]] we may model $T Alg_\infty$ by the _injective_ [[model structure on simplicial presheaves]] on $T^{op}$, [[Bousfield localization of model categories|left Bousfield localized]] at the morphisms $T[k] \otimes T[l] \to T[k+l]$. This localized model structure we write $[T, sSet]_{inj,prod}$.

By the [above proposition](#LimitInAlg) we have that $\mathcal{O}\mathcal{L}X$ is given by the [[homotopy pushout]] in $[T, sSet]_{inj,prod}$ of 

$$
  \mathcal{O}X \leftarrow \mathcal{O}(X)\otimes_k \mathcal{O}(X) \to \mathcal{O}(X)
  \,,
$$

where both morphism are simple the product on $\mathcal{O}(X) \in CAlg_k$. By general properties of [[homotopy pushout]]s and the injective [[model structure on simplicial presheaves]] we have that this homotopy pushout is computed by an ordinary pushout once we pass to a weakly equivalent diagram in which one of the two morphism is a cofibration of simplicial algebras.

$$
  \array{
  \mathcal{O}X 
   &\leftarrow& 
    \mathcal{O}(X)\otimes_k \mathcal{O}(X) &\hookrightarrow& \mathrm{B} \mathcal{O}(X)
  \\
  \downarrow^{\mathrlap{=}} && \downarrow^{\mathrlap{=}} && 
   \downarrow^{\mathrlap{\simeq}}
   \\
  \mathcal{O}X &\leftarrow& 
    \mathcal{O}(X)\otimes_k \mathcal{O}(X) &\to& \mathcal{O}(X)
  }
  \,.
$$

It is sufficient to find a [[resolution]] $\mathrm{B} \mathcal{O}(X)$ in the global model structure $[T, sSet]_{inj}$ because left Bousfield localization strictly increases the class of weak equivalences, so that every gloabl weak equivalence is also a local weak equivalence.

Since we are in the _injective_ model structure this just means that this morphism $\mathcal{O}(X) \otimes_k \mathcal{O}(X) \to \mathrm{B} \mathcal{O}X$ needs to be over each $x^n$  in $T$ a [[monomorphism]] of simplicial sets. 
If we find $\mathrm{B} \mathcal{O}X$ also as a strictly product-preserving functor (notice that the general functor in our model category need not even preserve products weakly, it will do so after fibrant replacement) then it being monomorphism over $x^1$ implies that it is monic over every $x^n$.

There is a standard resolution of the kind we need called the [[bar complex]], see for intance ([Ginzburg, page 16](#Ginzburg)) for an explicit description.
This is usually discussed as a [[chain complex]] in the category of $\mathcal{O}(X)$-[[module]]s. But in fact after applying the [[Dold-Kan correspondence]] to regard it as a simplicial module it is naturally even a [[simplicial object]] in $CAlg_k$:
 
$$
  \mathrm{B} \mathcal{O}(X) 
   :=
  \left(
     \cdots 
    \mathcal{O}(X) \otimes_k \mathcal{O}(X) \otimes_k
     \mathcal{O}(X) \otimes_k \mathcal{O}(X)
     \stackrel{\overset{\mu \otimes Id \otimes Id}{\longrightarrow}}{\stackrel{\overset{Id \otimes \mu Id}{\longrightarrow}}{\underset{Id \otimes Id \otimes \mu}{\longrightarrow}}}
    \mathcal{O}(X) \otimes_k \mathcal{O}(X) \otimes_k
     \mathcal{O}(X) 
     \stackrel{\overset{\mu \otimes Id}{\longrightarrow}}{\underset{Id \otimes \mu}{\longrightarrow}} 
     \mathcal{O}(X) \otimes_k \mathcal{O}(X)
  \right)
  \in 
  CAlg_k^{\Delta^{op}}
  \,,
$$

with the evident face and degeneracy maps given by binary product operation in the algebra and insertion of units. 

Take the morphism $\mathcal{O}(X) \otimes \mathcal{O}(X) \to \mathrm{B} \mathcal{O}(X)$ degreewise to be the inclusion of $\mathcal{O}(X) \otimes \mathcal{O}(X)$ as the two outer direct summands

$$
  \mathcal{O}(X)
  \otimes_k 
  \mathcal{O}(X)
  \stackrel{Id \otimes e \otimes e \otimes \cdots \otimes e \otimes Id}{\longrightarrow}
  \mathcal{O}(X) \otimes_k \mathcal{O}(X) \otimes_k \cdots 
  \otimes_k \mathcal{O}(X)
  \,,
$$

where $e : k \to \mathcal{O}(X)$ is the monoid unit.

This is clearly degreewise a [[monomorphism]], hence is a monomorphism. Under the [[Moore complex]] functor $N : Ab^{\Delta^{op}} \to Ch_\bullet^+$ it maps to the standard bar complex resolution as found in the traditional literature (as reviewed for instance in [Ginzburg](#Ginzburg)). This morphism of chain complexes is an [[isomorphism]] in [[homology]]. Since under the [[Dold-Kan correspondence]] [[simplicial homotopy group]]s are identified with [[homology]] groups, we find that indeed $\mu : \mathrm{B}\mathcal{O}(X) \to \mathcal{O}(X)$ is a weak equivalence in $[T,sSet]_{inj}$ and hence in $[T, sSet]_{inj,prod}$.

We may now compute the pushout in $[T, sSet]$ and this will compute the desired homotopy pushout. Notice that this pushout indeed takes place just in simplicial copresheaves, not in product-preserving copresheaves! 

But this ordinary pushout it manifestly the claimed one.

=--


+-- {: .num_remark}
###### Remark

This derivation

* crucially uses the assumption that $A$ is a commutative algebra;

* curiously does _not_ make use of any specific property of the set of morphisms $\{T[k] \coprod T[l] \to T[k+l] \}$ at which we are considering the left Bousfield localization. The entire construction proceeds entirely at the underlying simplicial sets of our simplicial algebras. In fact, the resulting homotopy pushout $\mathcal{O}(X) \coprod_{\mathcal{O}(X) \otimes \mathcal{O}(X)} \mathrm{B}\mathcal{O}(X)$ is a simplicial copresheaf on $T$ that no longer preserves any products: there is no manifest algebra structure.

  But also, this object is far from being fibant in the localized model structure $[T, sSet]_{proj,prod}$. The Bousfield localization, hence the information about the set of maps at which we are localizing, hence the algebra structure, kicks in only once we pass now to the fibrant [[resolution]] of our pushout. That **fibrant replacement equips the Hochschild chain complex with the structure of an $\infty$-algebra.**

=--


### Higher order Hochschild homology modeled on cdg-algebras {#OvercdgAlgs}

We discuss details of Hochschild homology in the context of [[dg-geometry]]:  the [[(∞,1)-topos]] over an [[(∞,1)-site]] of formal duals of commutative [[dg-algebra]]s over a field, [[presentable (∞,1)-category|presented]] by the [[model structure on dg-algebras]].


Fix a [[field]] $k$ of [[characteristic]] 0. We consider now the context of [[dg-geometry]] with its [[function algebras on ∞-stacks]] taking values in unbounded dg-algebras, exhibited by the [[adjoint (∞,1)-functors]]

$$
  (\mathcal{O} \dashv Spec) : 
   (cdgAlg_k^{op})^\circ
   \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\longrightarrow}}
   \mathbf{H} := Sh_\infty((cdgAlg_k^-)^{op})
   \,.
$$

For the discussion of Hochschild homology in this $\mathbf{H}$, the main fact about the [[model structure on dg-algebras]] that we need is this:

+-- {: .num_prop #PoweringAndCopoweringIndgContext}
###### Proposition

In the [[model structure on dg-algebras|projective model structure on unbounded commutative dg-algebras]] over $k$ we have that

1. the [[derived functor|derived]] [[copower]]ing of $cdgAlg_k$ over [[sSet]] is presented by the ordinary powering of $cdgAlg_k$ over $sSet$;

1. the [[derived functor|derived]] [[power]]ing of $cdgAlg_k$ over degreewise finite simplicial sets is presented by forming polynomial [[differential forms on simplices]], $S \mapsto \Omega^\bullet_{poly}(S)$.

=--

This is discussed in detail at [[model structure on dg-algebras]] in the sections <a href="http://nlab.mathforge.org/nlab/show/model+structure+on+dg-algebras#DerivedCopowering">Derived copowering</a> and <a href="http://nlab.mathforge.org/nlab/show/model+structure+on+dg-algebras#DerivedPowering">Derived powering</a>.

#### Higher order Hochschild complexes

By the [above fact](#PoweringAndCopoweringIndgContext)
[Pirashvili's copowering definition](#PirashviliHigherOrder) of higher order Hochschild homology holds true in dg-geometry. For $X$ a [[manifold]] regarded as a [[topological space]] and then as a [[constant ∞-stack]] in $\mathbf{H}$ we have for any $A \in cdgAlg_k$

$$
  \mathcal{O}[X, Spec A]
  \simeq
  X \cdot A
$$

in $cdgAlg_k$.


#### Jones' theorem 
 {#JonesTheorem}

[[Jones' theorem]] asserts that the Hochschild homology of the [[dgc-algebra]] of [[differential forms]] on a [[smooth manifold]] computes the [[ordinary cohomology]] of the corresponding [[free loop space]]. We discuss now how this result follows using derived loop spaces of [[constant ∞-stacks]]

See also at _[[Sullivan model for free loop spaces]]_ the section on _[Relation to Hochschild homology](Sullivan+model+of+free+loop+space#RelationToHochschildHomology)_.

+-- {: .num_prop}
###### Fact

For $X$ a [[smooth manifold]], $\Omega^\bullet(X)$ its [[de Rham dg-algebra]] and $\mathcal{L} X$ its [[free loop space]], we have

$$
  H^\bullet(\mathcal{L} X, \mathbb{R}) 
    \simeq 
  HH_\bullet(\Omega^\bullet(X), \Omega^\bullet(X))
  \,.
$$

=--

We sketch the proof in terms of the above derived loop space technology.

+-- {: .proof}
###### Proof 

Set $k = \mathbb{R}$. Write $LConst X \in \mathbf{H}$ for the [[constant ∞-stack]] on the [[homotopy type]] of $X$, regarded as a [[topological space]] $\simeq$ [[∞Grpd]]. Then

$$
  \mathcal{O} LConst X \simeq C^\bullet(X,k) \simeq \Omega^\bullet(X)
   \in
  dgcAlg_{\mathbb{R}}
$$

is (...) the $k$-valued [[singular cohomology|singular cochain]] complex of $X$, which by the [[de Rham theorem]] is equivalent to the [[de Rham dg-algebra]].

Since $LConst$ is a [[left exact (∞,1)-functor]] it commutes with forming [[free loop space objects]] and therefore

$$
  \mathcal{L} LConst X \simeq LConst (\mathcal{L} X)
  \,.
$$

Since $LConst X$ is $\mathcal{O}$-perfect (...) we have by the above copowering-description of the Hochschild complexes that the cohomology of the loop space of $X$

$$
  \mathcal{O} ((LConst X)^{S^1}) \simeq C^\bullet(\mathcal{L} X, k)
$$

is given by the Hochschild complex of the dg-algebra $\Omega^\bullet(X)$

$$
  \mathcal{O} ((LConst X)^{S^1}) \simeq S^1 \cdot \Omega^\bullet(X)
  \,.
$$

=--


#### The circle and the odd line {#CircleAndOddLine}

Consider as before the categorical [[circle]] $S^1$ as the corresponding [[constant ∞-stack]] in $\mathbf{H}$. We describe the function $\infty$-algebra on $S^1$. Below this will serve to explain the nature of the canonical circle action on the Hochschild complex of a cdg-algebra.

+-- {: .num_prop}
###### Proposition

We have an equivalence

$$
  \mathcal{O}(S^1) \simeq (k \oplus k[-1])
  \,,
$$

where on the right we have the [[ring of dual numbers]] over $k$, regarded as a [[dg-algebra]] with the odd generator in degree 1 and trivial differential.

=--

+-- {: .proof}
###### Proof

Every [[∞-groupoid]] is the [[(∞,1)-colimit]] over itself (as described there) of the [[(∞,1)-functor]] constant on the point. This [[(∞,1)-colimit]] is preserved by the left [[adjoint (∞,1)-functor]] $LConst : \infty Grpd \to \mathbf{H}$, so that we have

$$
  S^1 \simeq {\lim_{\to}}_{S^1} *
$$

in $\mathcal{H}$. The [[(∞,1)-functor]] $\mathcal{O}$ is also left adjoint, so that 

$$
  \mathcal{O}(S^1) \simeq {\lim_{\leftarrow}}_{S^1} \mathcal{O}(*)
$$

in $cdgAlg_k^\circ$.  Since the point is representable, we have by the definition of $\mathcal{O}$ as the left $(\infty,1)$-[[Kan extension]] of the inclusion $(cdgAlg_k^-)^{op} \hookrightarrow (cdgAlg_k)^{op}$ that this is

$$
  \cdots \simeq {\lim_{\leftarrow}}_{S^1} k
  \,.
$$

This is the formula for the $(\infty,1)$-power of the cdg-algebra $k$ by by $\infty$-groupoid $S^1$. By the [above fact](#PoweringAndCopoweringIndgContext), using that the circle is a finite $(\infty,1)$-groupoid, this is given by the cdg-algebra of polynomial [[differential forms on simplices]] of $S^1$

$$
  \cdots \simeq \Omega^\bullet_{poly}(S^1)
  \,.
$$

By a central theorem of [[rational homotopy theory]] (recalled at [[differential forms on simplices]]) this is equivalent to the [[singular cohomology|singular cochains]] on the circle

$$
  \cdots \simeq C^\bullet(S^1, k)
  \,.
$$

But $S^1 \simeq \mathcal{B}\mathbb{Z}$ is a [[classifying space]] of a Lie algebra, so that this is a [[formal dg-algebra]], equivalent to its [[cochain cohomology]]. Over the field $k$ of characteristic 0 this is 

$$
  H^n(S^1, k) = 
  \left\{
     \array{
        k & for\; n = 0
        \\
        k & for \; n = 1
        \\
        0 & otherwise
     }
  \right.
  \,.
$$ 

Therefore

$$
  \cdots \simeq k \oplus k[-1]
   \,.
$$

=--

+-- {: .num_remark}
###### Remark

This means that $Spec \mathcal{O}(S^1)$ is no longer the circle itself, but the [[odd line]], regarded with its canonical $\mathbb{Z}$-grading.

This point is amplified in ([Ben-ZivNadler](#Ben-ZviNadler)).

=--


#### The cotangent complex as functions on the derived loop space


+-- {: .num_cor}
###### Corollary

We have that 

$$
  [S^1, Spec A] : U \mapsto cdgAlg_k(A, \mathcal{O}(U) \oplus \mathcal{O}(U)[-1])
  \,.
$$

=--

+-- {: .proof}
###### Proof

$$
  \begin{aligned}
    [S^1, Spec A](U) & \simeq \mathbf{H}(S^1 \times U , Spec A)
    \\
    & \simeq cdgAlg_k(A, \mathcal{O}(S^1 \times U))
    \\
    & \simeq cdgAlg_k(A, \mathcal{O}(U) \oplus \mathcal{O}(U)[-1])
  \end{aligned}
  \,.
$$

=--

(...)

## Properties


### Algebra structure on $(HH^\bullet(A,A), HH_\bullet(A,A))$ {#AlgebraStrucOnHochschild}

There is rich algebraic structure on Hochschild homology and cohomology itself, and on the pairing of the to. We describe various aspects of this.

#### Differential calculus {#DifferentialCalculus}


It turns out that

* Hochschild homology of $\mathcal{O}(X)$ encodes [[Kähler differential form]]s on $X$;

* Hochschild cohomology of $\mathcal{O}(X)$ encodes [[multivector field]]s on $X$;

* there are  natural pairings between $HH_\bullet(\mathcal{O}(X), \mathcal{O}(X))$ and $HH^\bullet(\mathcal{O}(X), \mathcal{O}(X))$ that mimic the structure of the natural pairings between vector fields and differential forms on [[smooth manifold]].

See ([Tamarkin-Tsygan](#TamarkinTsygan)) and see at _[[Kontsevich formality]]_ for more. This equivalence enters the construction of [[formal deformation quantization]] of [[Poisson manifolds]].


One way to understand or interpret this conceptually is to regard the [[derived loop space]] object of a 0-[[truncated]] object $X$ to consist of [[infinitesimal object|infinitesimal]] loops in $X$.

##### Hochschild-Kostant-Rosenberg theorem {#HochschildKostantRosenberg} 

The **[[Hochschild-Kostant-Rosenberg theorem]]** states that under suitable conditions, the Hochschild homology of an algebra (with coefficients in itself) computes the wedge powers of its [[Kähler differential]]s.

Let $A$ be an [[associative algebra]] over $k$. Recall the natural [identification](#Kaehler1Forms)

$$
  HH_1(A,A) \simeq \Omega^1(A)
$$

of the first Hochschild homology of $A$ with coefficients in itself and degree-1 [[Kähler differential form]]s of $A$.



Write $\Omega^0(R/k) := R \simeq HH_0(R,R)$.

For $n \geq 2$ Write $\Omega^n(R/k) = \wedge^n_R \Omega(R/k)$ for the $n$-fold [[exterior algebra|wedge product]] of $\Omega(R/k)$ with itself: the degree $n$-K&#228;hler-differentials.

+-- {: .num_theorem }
###### Theorem

The isomorphism $\Omega^1(R/k) \simeq H_1(R,R)$ extends to a graded ring morphism

$$
  \psi : \Omega^\bullet(R/k) \to H_\bullet(R,R)
  \,.
$$

=--

If the $k$-algebra $R$ is sufficiently well-behaved, then this morphism is an [[isomorphism]] that identifies the Hochschild homology of $R$ in degree $n$ with $\Omega^n(R/k)$ for all $n$:

+-- {: .num_theorem }
###### Theorem
**(Hochschild-Kostant-Rosenberg theorem)**


If $k$ is a [[field]] and $R$ a commutative $k$-[[algebra]] which is 

* essentially of finite type 

* smooth over $k$

then there is an [[isomorphism]] of graded $R$-algebras

$$
  \psi : \Omega^\bullet(R/k) \stackrel{\simeq}{\to}
  HH_\bullet(R,R)
  \,.
$$

Moreover, dually, there is an isomorphism of Hochschild cohomology with wedge products of derivations:

$$
  \wedge^\bullet_R Der(R,R) \simeq HH^\bullet(R,R)
$$

=--

This is reviewed for instance as ([Weibel, theorem 9.4.7](#Weibel)) or as ([Ginzburg, theorem 9.1.3](#Ginzburg)).


#### $E_n$-algebra structure: Deligne-Kontsevich conjecture/theorem {#EnAlgebraStructure}

The next statement is known as the [[Deligne conjecture]].


+-- {: .num_prop #DeligneConjectureViaDerivedMappingSpaces}
###### Proposition

The [higher order Hochschild homology](PirashviliHigherOrder) $\mathcal{O} (X^{S^d})$ of an object $X$ with respect to the $d$-[[sphere]] $S^d$ and with coefficients in a [[integral transforms on sheaves|geometric function object]] is naturally an [[Ek-Algebras|E(d+1)-algebra)]]: an [[algebra over an operad]] over the [[little k-cubes operad]] for $k = d+1$ .

For let $\Sigma^{d+1} = D^{d+1}\setminus \coprod_r D^{d+1}$ be the $(d+1)$-[[ball]] with $r$ small $d+1$-balls taken out. We have a [[cospan]] of boundary inclusions

$$
  \array{
     && \Sigma^{d+1}
     \\
     & \nearrow && \nwarrow
     \\
     \coprod_r S^d  &&&& S^d
  }
$$

in [[∞Grpd]] and under $LConst : \infty Grpd \to \mathbf{H}$ then also in our [[(∞,1)-topos]].

Applying the <a href="http://ncatlab.org/nlab/show/(infinity,1)-topos#ClosedMonoidalStructure">(∞,1)-topos internal hom</a> $[-,X]$ or equivalent the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring">(∞,1)-powering</a> $X^{(-)}$ into a given object $X \in \mathbf{H}$ to this [[cospan]] produces the [[span]]

$$
  \array{
     && X^{\Sigma^{d+1}}
     \\
     & {}^{\mathllap{i_r}}\swarrow && \searrow^{\mathrlap{o}}
     \\
     \prod_r X^{S^d} &&&& X^{S^d}
  }
$$ 

in $\mathbf{H}$. Then the [[integral transforms on sheaves]] 

$$
  o_1 i_r^* : \prod_r \mathbf{H}/X^{S^d} \to \mathbf{H}/X^{d}
$$

induced by these spans constitute the $E_n$-action on the function objects on $X^{S^d}$.

=--

This was observed in ([Ben-ZviFrancisNadler, corollary 6.8](#Ben-ZviFrancisNadler)).

For $d = 1$, under the identification of the [[HKR theorem]] above (when it applies),  the Gerstenhaber bracket is identified with the [[Schouten bracket]] ([Tsyagin, theorem 2.2.2](https://arxiv.org/abs/math/9904132v1))


+-- {: .num_remark }
###### Remark
**(Deligne conjecture)**

Some historical comments on the [[Deligne conjecture]].
 
Historically it was first found that there is the structure of a [[Gerstenhaber algebra]] on $HH^\bullet(A,A)$.  By ([Cohen](#Cohen)) it was known that Gerstenhaber algebras arise as the [[homology]] of [[E2-algebra]]s in [[chain complex]]s. In a letter in 1993 Deligne wondered whether the Gerstenhaber structure on the Hochschild cohomology $HH^\bullet(A,A)$ lifts to an [[E2-algebra]]-structure on the cochain complex $C^\bullet(A,A)$.

In [GerstenhaberVoronov (1994)](#GerstenhaberVoronov) a resolution of the Gerstenhaber algebra structure was given, but the relationship to $E_2$-algebras remained unclear.

In ([Tamarkin (1998)](#Tamarkin)) a genuine resolution in the [[model structure on operads]] of the Gerstenhaber operad was given and shown to act via the Gerstenhaber-Voronov construction on $C^\bullet(A,A)$. This proved Deligne's conjecture.

Various authors later further refined this result. A summary of this history can be found in ([Hess](#Hess)).

In [Hu-Kriz-Voronov (2003)](#HuKrizVoronov) it was further shown that for $A$ an [[En-algebra]], $C^\bullet(A,A)$ is an $E_{n+1}$-algebra.

Notice that the identification of Hochschild (co)homology as coming from higher order free loop spaces makes all this structure manifest.

=--





#### $HH$ of constant $\infty$-stacks: String topology BV-algebra {#StringTopology}

Let $T$ be the [[algebraic theory]] of ordinary [[associative algebra]]s over a [[field]] $k$, regarded as an [[(∞,1)-algebraic theory]] and let $\mathbf{H}$ be the [[(∞,1)-topos]] of $(\infty,1)$-sheaves over a small site in $T Alg_\infty^{op}$.

Under the [[inverse image]] of the [[global section]] [[(∞,1)-geometric morphism]] and the [[homotopy hypothesis]]-equivalence

$$
  \mathbf{H} \stackrel{\overset{LConst}{\longleftarrow}}{\underset{\Gamma}{\longrightarrow}}
  \infty Grpd
  \stackrel{\overset{\Pi}{\longleftarrow}}{\underset{|-|}{\longrightarrow}}
  Top
$$

we may regard every [[topological space]] $X$ as a [[constant ∞-stack]] $LConst X$, an object in $\mathbf{H}$.


+-- {: .num_prop }
###### Proposition

The function algebra on $LConst X$ is the cosimplicial algebra of singular cochains on $X$. Under the [[monoidal Dold-Kan correspondence]] it identifies with the cochain [[dg-algebra]] $C^\bullet(X)$ that computes the [[singular cohomology]] of $X$.

=--

This has maybe been first made explicit by [[Bertrand Toën]]. Details are at [[function algebras on ∞-stacks]].


+-- {: .num_prop }
###### Corollary

The Hochschild homology of $C^\bullet(X)$ is the [[singular cohomology]] of the [[free loop space]] $L X$.

=--

+-- {: .proof}
###### Proof

Apply the [central identification](#GeneralAbstractDefinition) $\mathcal{O} \mathcal{L}(LConst X)  \simeq S^1 \cdot \mathcal{O}(LConst X)$. Then observe that the [[free loop space object]] $\mathcal{L} LConst X$  of the constant $\infty$-stack is the constant $\infty$-stack on the ordinary [[free loop space]], because $LConst$ is a [[left exact (∞,1)-functor]] and because $\mathcal{L}X \simeq L X$ in [[Top]]. Then use by the above remark that $\mathcal{O} LConst L X$ is singular cochains on $L X$. 

=--

This result, which follows directly from the general abstract desciption of Hichschild homology is known as **Jones' theorem**. We now review the results in the literature on this point.

Let $X$ be a [[compact manifold]] [[oriented]] [[smooth manifold]] of [[dimension]] $d$. Write $C^\bullet(X)$ for the [[dg-algebra]] of cochains for [[singular cohomology]] of $X$. Write $L X$ for the topological [[free loop space]] of $X$ and $H_\bullet(L X)$ for its [[singular homology]].


+-- {: .num_theorem }
###### Theorem

There is a linear isomorphism of degree $d$

$$
  \mathbb{D}
  :
  HH^{-p-q}(C^\bullet(X), C^\bullet(X)^{\vee})
    \simeq
  HH^{-p}(C^\bullet(X), C^\bullet(X))
  \,.
$$

=--

This is due to ([FelixThomasVigue-Poirrier, section 7](#FelixThomasVigue-Poirrier))).

+-- {: .num_theorem }
###### Theorem
**(Jones' theorem)**

There is an [[isomorphism]]

$$
  J 
  : 
  H_{p+q}(L X) 
    \stackrel{\simeq}{\to}  
  HH^{-p-d}(C^\bullet(X), C^\bullet(X)^{\vee})
$$

such that the canonical [[string topology]] [[BV-operator]] $\Delta$ of the [[BV-algebra]] $H_{\bullet + d}(L X)$ and the [[Connes coboundary]] $B^\vee$ on $HH^{\bullet-d}(C^\bullet(X), C^\bullet(X)^{\vee})$ satisfy

$$
  J \circ \Delta = B^{\vee} \circ J
  \,.
$$

=--

This is due to ([Jones](#Jones)).


+-- {: .num_theorem }
###### Theorem

The [[Connes coboundary]] defines via the isomorphism $\mathbb{D}$ from above the structure of a [[BV-algebra]] on $HH^\bullet(C^\bullet(X), C^\bullet(X))$.


=--

This is ([Menichi, theorem 3](#Menichi)).


### Relation to cyclic (co)homology

There is an <a href="http://ncatlab.org/nlab/show/free+loop+space+object#CircleAction">intrinsic circle action</a> on Hochschild (co)chains. Passing to the cyclically invariant (co)chains yields [[cyclic (co)homology]].


### Further

#### Hochschild cohomology and extensions {#Extensions}

+-- {: .num_defn }
###### Definition

An [[exact sequence]] $0 \to N \to E \to R$ of $k$-modules where
$E \to R$ is a surjective morphism of $k$-algebras is
called a **$k$-split** extension or a **Hochschild extension** of $R$ by $E$ if the sequence is a [[split sequence]] as a sequence of $k$-[[module]]s.

Two extensions are _equivalent_ if there is an isomorphism or $k$-algebra $E \stackrel{\simeq}{\to} E'$ that makes

$$
  \array{
    N &\to& E &\to& R
    \\
    \downarrow^{\mathrlap{=}} && \downarrow && \downarrow^{\mathrlap{=}}
    \\
    N &\to& E' &\to& R
  }
$$

commute.

=--


+-- {: .num_remark }
###### Remark

Due to the $k$-splitness assumption there is an isomorphism of $k$-modules $E \simeq R \oplus N$ and this is equipped with a $k$-algebra structure such that the product on the $R$ [[direct sum]]mand is that of $R$. From this we find that the product on $E$ is of the form

$$
  (r_1, n_1) \cdot (r_2, n_2) =
  (r_1 r_2 , r_1 n_2 + n_1 r_2 + f(r_1, r_2))
  \,,
$$

where $f : R \otimes_k R \to N$ is some $k$-linear map. Since the product on $E$ is (by definition) associative, it follows that for $f$ that this satisfies for all $r_0, r_1, r_2 \in R$ the _cocycle equation_

$$
  r_0 f(r_1, r_2) - f(r_0 r_1, r_2) + f(r_0 , r_1 r_2) - f(r_0, r_1) r_2 = 0
$$

as an equation in $N$. This says that $f$ must be a Hochschild cocycle

$$
  f \in HH^2(R,N)
  \,.
$$ 

=--


Conversely, every such cocycle yields a $k$-split extension of $R$ by $N$ this way:



+-- {: .num_theorem }
###### Theorem

For $R$ a $k$-algebra and $N$ an $R$-[[bimodule]], equivalence
classes of Hochschild extensions of $R$ by $N$ are in bijection with
degree 2 Hochschild cohomology $HH^2(R,N)$.

=--

See for instance [[An Introduction to Homological Algebra|Weibel, theorem 9.3.1]].


#### Hochschild cohomology and deformations {#Deformations}

As a special case of the above statement about extensions of $R$, we obtain a statement about _deformation_ of $R$.

A standard problem is to deform a $k$-algebra $R$ by introducing a new "parameter" $t$ that squares to 0 -- $t \cdot t = 0$ and a new product

$$
  r_1 \cdot_t r_2 = r_1 r_2 + t f(r_1, r_2)  
  \,.
$$

From the above we see that this is the same as finding an $k$-split extension of $R$ by itself. So in particular such extensions are given by Hochschild cocycles $f \in HH^2(R,R)$.

See for instance [Ginzburg, section 7](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf) and for more see [[deformation quantization]].




## Related entries

* [[Sullivan model of free loop space]]

* [[cyclic homology]], [[dihedral homology]]

* [[topological Hochschild homology]]
 
## References
 
Hochschild cohomology of ordinary algebras was introduced in

* [[Gerhard Hochschild]], _On the cohomology groups of an associative algebra_, The Annals of Mathematics, 2nd ser., __46__ 1 (1945) 58-6 &lbrack;[jstor:1969145](http://www.jstor.org/stable/1969145)&rbrack;

Early further discussion:

* [[Michael Barr]], *Cohomology of commutative algebra I*, Ph.D. Thesis, University of Pennsylvania (1962), Retyped with a few corections and notes (2003) &lbrack;[pdf](https://www.math.mcgill.ca/barr/papers/thes.pdf), [[Barr-CohomologyThesis.pdf:file]]&rbrack;

and in relation to [[monadic cohomology]]:

* [[Michael Barr]], *Harrison homology, Hochschild homology and triples* J. Algebra **8** 3 (1968) 314–323 &lbrack;<a hrf="https://doi.org/10.1016/0021-8693(68)90062-8">doi:10.1016/0021-8693(68)90062-8</a>, [pdf](https://www.math.mcgill.ca/barr/papers/harr-hoch.pdf), [[Barr-HarrHochAndTriples.pdf:file]]&rbrack;


Textbook discussions:

* {#Weibel} [[Charles Weibel]], chapter 9 of: _[[An Introduction to Homological Algebra]]_
 
* {#Ginzburg} [[Victor Ginzburg]], chapter 4 of: _Lectures on noncommutative geometry_ &lbrack;[arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603)&rbrack;


The definition of the higher order Hochschild complex as (implicitly) the tensoring of an algebra with a simplicial set:

* {#Pirashvili} [[Teimuraz Pirashvili]], _Hodge decomposition for higher order Hochschild homology_ Annales Scientifiques de l'&#201;cole Normale Sup&#233;rieure Volume 33, Issue 2, March 2000, Pages 151-179 ([ps](http://www.mathematik.uni-bielefeld.de/sfb343/preprints/pr98058.ps.gz))


A survey of traditional higher order Hochschild (co)homology and further developments and results are described in

* [[Grégory Ginot]], _Higher order Hochschild cohomology_ 
  ([pdf](http://www.institut.math.jussieu.fr/~ginot/papers/Higher-Order-Hochschild-Long.pdf))

A considerably refined discussion of this which almost makes the construction of Hochschild complexes as an $(\infty,1)$-copowering operation manifest is in

* [[Grégory Ginot]], Thomas Tradler, [[Mahmoud Zeinalian]], _Derived higher Hochschild homology, topological chiral homology and factorization algebras_, [arxiv/1011.6483](http://arxiv.org/abs/1011.6483)
{#GinotTradlerZeinalian}
* Nathalie Wahl, Craig Westerland, _Hochschild homology of structured algebras_, [arxiv/1110.0651](http://arxiv.org/abs/1110.0651)


The full $(\infty,1)$-categorical picture of Hochschild homology as the cohomology of [[derived stack|derived]] [[free loop space object]]s is due to

* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], 
  _[[geometric infinity-function theory|Integral transforms and Drinfeld centers in derived algebraic geometry]]_ ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))
{#Ben-ZviFrancisNadler}

based on

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Langlands Parameters_ ([arXiv:0706.0322](http://arxiv.org/abs/0706.0322)) .

Specifically the dicussion of differential forms via such an $\infty$-category theoretic perspective of the HKR-theorem is discussed in 

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))
{#Ben-ZviNadler}

* [[Bertrand Toën]] [[Gabriele Vezzosi]], _$S^1$-Equivariant simplicial algebras and de Rham theory_ ([arXiv:0904.3256](http://arxiv.org/abs/0904.3256))

 
General homotopy-theoretic setups and results for contexts in which this makes sense are discussed in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _HAG II, geometric stacks and applicatons_ ([arXiv:math/0404373v4](http://arxiv4.library.cornell.edu/abs/math/0404373v4))
{#ToenVezzosiStacks}

Jones's theorem is due to

* J. D. S. Jones, _Cyclic homology and equivariant homology_ , Invent. Math. 87
(1987), no. 2, 403-423.
{#Jones}

The BV-algebra structure on Hochschild cohomology of singular cochain algebras is discussed in

* Y. F&eacute;lix, J.-C. Thomas, M. Vigu&eacute;-Poirrier, _The Hochschild cohomology of a closed manifold_ Publ. Math. IH&Eacute;S Sci. (2004) no 99, 235-252
{#FelixThomasVigue-Poirrier}

* [[Luc Menichi]], _Batalin-Vilkovisky algebra structures on Hochschild cohomology_ ([pdf](http://math.univ-angers.fr/perso/lmenichi/BV_Hochschild.pdf))

The abstract differential caclulus on $(HH^\bullet(A,A), HH_\bullet(A,A))$ is discussed for instance in

* [[Dmitry Tamarkin]], [[Boris Tsygan]], _Cyclic Formality and Index Theorems_ ,  Letters in Mathematical Physics
Volume 56, Number 2, 85-97 ([journal](http://www.springerlink.com/content/u33hv13g0669h414/))
{#TamarkinTsygan}

A review of Deligne's conjecture and its solutions is in

* [[Kathryn Hess]], _Deligne's Hochschild cohomology conjecture_ ([pdf](http://sma.epfl.ch/~hessbell/Pub_DeligneColloq.pdf))
{#Hess}

More developments are in 

* [[Grégory Ginot]], Thomas Tradler, [[Mahmoud Zeinalian]], _Higher Hochschild cohomology, Brane topology and centralizers of $E_n$-algebra maps_, ([arXiv:1205.7056](http://arxiv.org/abs/1205.7056))
* Nathalie Wahl, _Universal operations in 
Hochschild homology_, [arxiv/1212.6498](http://arxiv.org/abs/1212.6498)

Relation to [[factorization homology]] is discussed in 

* Geoffroy Horel, _Factorization homology and calculus &#224; la Kontsevich Soibelman_ ([arXiv:1307.0322](http://arxiv.org/abs/1307.0322))

For more references on the relation to _[[topological chiral homology]]_ see there.

Interesting wishlists for treatments of Hochschild cohomology are in [this](http://mathoverflow.net/questions/28472/book-on-hochschild-cohomology) MO discussion.



[[!redirects Hochschild homology]]

[[!redirects Hochschild complex]]
[[!redirects Hochschild cochain complex]]
[[!redirects Hochschild complexes]]
[[!redirects Hochschild cochain complexes]]


[[!redirects hochschild homology]]
[[!redirects hochschild cohomology]]
[[!redirects hochschild complex]]

[[!redirects Connes coboundary operator]]
[[!redirects Connes coboundary operators]]
[[!redirects Connes coboundary]]
[[!redirects Connes coboundaries]]

