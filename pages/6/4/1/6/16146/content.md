
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In a [[monoidal category]], there is a notion of [[modules]] over [[monoid objects]] which generalizes the classical notion of [[modules]] over [[rings]].
This is a special case of [[module over a monad]] where the monad is taken to be $A \otimes -$, with $A$ some [[monoid object]].

## Definition

Let $(\mathcal{V}, \otimes, I)$ be a [[monoidal category]] and $A$ a [[monoid object]] in $\mathcal{V}$, hence an object $A \in \mathcal{V}$ equipped with a multiplication morphism

$$
  \cdot : A \otimes A \to A
$$ 

and a unit element

$$
  e : I \to A
$$

satisfying the [[associativity law]] and the [[unit law]].

+-- {: .num_defn #ModuleInMonoidalCategory}
###### Definition

A (left) **module** over $A$ in $(\mathcal{V}, \otimes, I)$ is

* an [[object]] $N \in \mathcal{V}$ 

* equipped with a morphism

  $$
    \lambda : A \otimes N \to N
  $$

  in $\mathcal{V}$

such that this satisfies the axioms of an [[action]], in that the following are [[commuting diagrams]] in $\mathcal{V}$:

$$
  \array{
     A \otimes A \otimes N &\stackrel{id_A \otimes \lambda}{\to}& A \otimes N
     \\
     \downarrow^{\mathrlap{\cdot \otimes id_n}} && \downarrow^{\mathrlap{\lambda}}
     \\
     A \otimes N &\stackrel{\lambda}{\to}& N
  }
$$

and

$$
  \array{   
     I \otimes N &&\stackrel{e \otimes id_N}{\to}&& A \otimes N
     \\
     & \searrow && \swarrow_{\mathrlap{\lambda}}
     \\
     && N
  }
  \,.
$$

=--

## Examples

### Modules over monoids in abelian groups

Recall that a [[ring]], in the classical sense, is a [[monoid object]] in the category [[Ab]] of [[abelian groups]] with [[monoidal structure]] given by the [[tensor product of abelian groups]] $\otimes$. Accordingly a _module over $R$_ is a module in $(Ab,\otimes)$ according to def. \ref{ModuleInMonoidalCategory}.

We unwind what this means in terms of [[abelian groups]] 
regarded as [[sets]] with extra [[structure]]:

+-- {: .num_defn #ModuleOverARing}
###### Definition

A **module** $N$ over a ring $R$ is

1. an [[object]] $N \in $ [[Ab]], hence an [[abelian group]];

1. equipped with a [[morphism]]

   $$
     \alpha : R \otimes N \to N
   $$ 

   in [[Ab]]; hence a [[function]] of the underlying [[sets]] that sends elements

   $$
     (r,n) \mapsto  r n  \coloneqq \alpha(r,n)
   $$

   and which is a [[bilinear function]] in that it satisfies

   $$
    (r, n_1 + n_2) \mapsto r n_1 + r n_2
   $$

   and

   $$
    (r_1 + r_2, n) \mapsto r_1 n + r_2 n
   $$

   for all $r, r_1, r_2 \in R$ and $n,n_1, n_2 \in N$;

1. such that the [[diagram]]

   $$
     \array{
        R \otimes R \otimes N 
        &\stackrel{\cdot_R \otimes Id_N}{\to}& R \otimes N
        \\
        {}^{\mathllap{Id_R \otimes \alpha}}\downarrow 
        && 
        \downarrow^{\mathrlap{\alpha}}
        \\
        R \otimes N &\to& N 
     }
   $$

   [[commuting diagram|commutes]] in [[Ab]],  which means that for all elements as before we have

   $$
     (r_1 \cdot r_2) n = r_1 (r_2 n)
      \,.
   $$

1. such that the diagram

   $$
     \array{
        1 \otimes N &&\stackrel{1 \otimes id_N}{\to}&& R \otimes N
        \\
        & \searrow && \swarrow_{\mathrlap{\alpha}}
        \\
        && N
     }
   $$
     
   commutes, which means that on elements as above 

   $$
     1 \cdot n = n
     \,.
   $$

=--


+-- {: .num_remark }
###### Remark


The category of all modules over all commutative rings is [[Mod]]. It is a [[bifibration]]

$$
  Mod \to CRing
$$

over [[CRing]].

This fibration may be characterized intrinsically, which gives
yet another way of defining $R$-modules. This we turn to 
[below](#ModulesOverARingInTermsOfStabilizedSlices).

=--

### $G$-sets
 {#GSets}

Simpler than the traditionally default notion of a module in 
$(Ab,\otimes)$, as [above](#Rings) is that of a module in 
[[Set]], equipped with its [[cartesian monoidal category|cartesian monoidal structure]].
(These days one may want to think of this as a notion of modules 
over [[F1]].)

A [[monoid object]] in $(Set,\times)$ is just a [[monoid]], for 
instance a [[discrete group]] $G$. A $G$-module in $(Set,\times)$
is simpy an _[[action]]_, say a [[group action]].

+-- {: .num_defn #ActionOfDiscreteGroupOnSet}
###### Definition

For $S \in $ [[Set]] and $G$ a [[discrete group]], a **$G$-[[action]]** of $G$ on $S$ is a [[function]]

$$
  \lambda \colon G \times S \to S
$$ 

such that

1. the neutral element acts trivially

   $$
     \array{
        * \times S &&\stackrel{\simeq}{\to}&& S
        \\  
        & {}_{(e,id_S)}\searrow && \nearrow_{\mathrlap{\lambda}}
        \\
        && G \times S
     }
   $$

1. the action property holds: for all $g_1, g_2 \in G$ and $s \in S$ we have $\lambda(g_1,\lambda(g_2, s)) = \lambda(g_1 \cdot g_2, s)$.

=--

### Abelian groups with $G$-action as modules over the group ring
 {#AbelianGroupsWithGAction}

If a [[discrete group]] acts, as in def. \ref{ActionOfDiscreteGroupOnSet},
on the set underlying an [[abelian group]] and acts by [[linear maps]] (abelian group [[homomorphisms]]), then this action is equivalently a module over the [[group ring]]  $\mathbb{Z}[G]$ as in def. \ref{ModuleOverARing}.

+-- {: .num_defn }
###### Definition

For $G$ a [[discrete group]], write $\mathbb{Z}[G] \in $ [[Ring]] for the [[ring]] 

1. whose underlying [[abelian group]] is the [[free abelian group]] on the set underlying $G$;

1. whose multiplication is given on [[basis]] elements by the group operation in $G$. 

=--

+-- {: .num_remark }
###### Remark

For $G$ a [[finite group]] an element $r$r of $\mathbb{Z}[G]$ is for the form

$$
  r = \sum_{g \in G} r_g g
$$

with $r_g \in \mathbb{Z}$. Addition is given by addition of the [[coefficients]] $r_g$ and multiplication is given by the formula

$$
  \begin{aligned}
    r \cdot \tilde r 
    & = 
    \sum_{g \in G} \sum_{\tilde g \in G} (r_g \tilde r_{\tilde g}) g \cdot \tilde g
    \\
    & = 
    \sum_{q \in G}
    \left(
      \sum_{g \tilde g = q} r_g \tilde r_{\tilde g}
    \right)
    q
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

For $A \in $ [[Ab]] an [[abelian group]] with underlying set $U(A)$, $G$-[[actions]] $\lambda \colon G \times U(A) \to U(A)$ such that for each element $g \in G$ the function $\lambda(g,-) \colon U(A) \to U(A)$ is an abelian group homomorphism are equivalently $\mathbb{Z}[G]$-[[module]] structures on $A$.

=--

+-- {: .proof}
###### Proof

Since the underlying abelian group of $\mathbb{Z}[G]$ is a [[free abelian group|free]] by definition, a [[bilinear map]] $\mathbb{Z}[G] \times A \to A$ is equivalently for each [[basis]] element $g \in G$ a [[linear map]] $A \to A$. Similarly the module property is determined on basis elements, where it reduces manifestly to the action property of $G$ on $U(A)$.

=--

+-- {: .num_remark }
###### Remark

This reformulation of linear $G$-[[actions]] in terms of [[modules]] allows to treat $G$-actions in terms of [[homological algebra]]. See at _[Ext -- Relation to group cohomology](Ext#RelationToGroupCohomology)_.

=--

### more examples

* In a [[symmetric monoidal category|symmetric monoidal]] [[category of chain complexes]] equipped with the [[tensor product of chain complexes]], then a [[monoid]] is a [[dg-algebra]], and a module is a _[[dg-module]]_. See there for more.

## References

The basic properties of categories of modules over [[monoid objects]] in [[symmetric monoidal categories]] are spelled out in sections 1.2 and 1.3 of

* Florian Marty, _Des Ouverts Zariski et des Morphismes Lisses en G&#233;om&#233;trie Relative_, Ph.D. Thesis, 2009, [web](http://thesesups.ups-tlse.fr/540/)

A summary is in section 4.1 of

* [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_, [arXiv:1410.1716](http://arxiv.org/abs/1410.1716).

See also [MO/180673](http://mathoverflow.net/questions/180673/category-of-modules-over-commutative-monoid-in-symmetric-monoidal-category), and the references at [[modules over a monad]].

For the classical case of the [[symmetric monoidal category]] [[Ab]], a standard textbook is

* F.W. Anderson, K.R. Fuller, _Rings and Categories of Modules_, Graduate Texts in Mathematics, Vol. 13, Springer-Verlag, New York, (1992).

[[!redirects modules over a monoid]]
[[!redirects modules over monoids]]
[[!redirects modules over a monoid]]