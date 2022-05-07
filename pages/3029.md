
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _group extension_ of a [[group]] $G$ by a group $A$ is third group $\hat G$ that sits in a [[short exact sequence]], that can usefully be thought of as a [[fiber sequence]], $A \to \hat G \to G$.


## Definition
 {#Definition}

+-- {: .num_defn #GroupExtension}
###### Definition

Two consecutive [[homomorphisms]] of  [[groups]]

\[\label{shortExtension} 
  A
  \overset{i}\hookrightarrow \hat G\overset{p}\to G
\]

are a **[[short exact sequence]]** if 

1. $i$ is [[monomorphism]], 

1. $p$ an [[epimorphism]] 

1. the [[image]] of $i$ is all of the [[kernel]] of $p$: $ker(p)\simeq im(i)$. 

We say that such a short exact sequence exhibits $\hat G$ as an **extension** of $G$ by $A$.

If $A \hookrightarrow \hat G$ factors through the [[center]] of $\hat G$ we say that this is a **[[central extension]]**.

=--

+-- {: .num_remark }
###### Remark

Sometimes in the literature one sees $\hat G$ called an extension "of $A$ by $G$". This is however in conflict with terms such as _[[central extension]]_, _[[extension of principal bundles]]_, etc, where the extension is always regarded _of the base, by the [[fiber]]_.  (On the other hand, our terminology conflicts with the usual meaning of "extension" in algebra.  For example, in Galois theory if $k$ is a field, then an extension of $k$ contains $k$ as a subfield.)

=--

Under the [[looping and delooping]]-equivalence, this is equivalently reformulated as follows. For $G \in$ [[Grp]] a [[group]], write $\mathbf{B}G \in $ [[Grpd]] for its [[delooping]] groupoid.

+-- {: .num_defn }
###### Definition

A sequence $A \to \hat G \to G$ is a [[short exact sequence]] of groups precisely if the [[delooping]]

$$
  \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G
$$ 

is a [[fiber sequence]] in the [[(2,1)-category]] [[Grpd]].

=--

This says that group extensions are special cases of the general notion discussed at _[[∞-group extension]]_. See there for more details.

+-- {: .num_defn #MorphismOfGroupExtensions}
###### Definition

A [[homomorphism]] of extensions $f : \hat G_1 \to \hat G_2$
of a given $G$ by a given $A$ is a [[group homomorphism]] of this form which fits into a [[commuting diagram]]

$$
  \array{
     && \hat G_1
    \\
    & \nearrow && \searrow
    \\
    A &&\downarrow^{\mathrlap{f}}&& G
    \\
    & \searrow && \nearrow
    \\
    && \hat G_2
  }
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

A morphism of extensions as in def. \ref{MorphismOfGroupExtensions} is necessarily an [[isomorphism]].

\[
  \label{equivExt}
  \array{
     1\to &A&\stackrel{i}\to &\hat G_1&\stackrel{p}\to &G&\to 1
     \\
    &\downarrow\mathrlap{=}&&\downarrow\mathrlap\epsilon&&\downarrow\mathrlap=&
    \\
    1\to &A&\stackrel{i'}\to &\hat G_2&\stackrel{p'}\to& G&\to 1
  }
  \,.
\]


=--

+-- {: .proof}
###### Proof

By the [[short five lemma]].

=--



## Properties

We discuss properties of group extensions in stages, 

* [General properties](#PropertiesGeneral)

* [Central group extensions](#PropertiesCentralGroupExtensions)

* [Abelian group extensions](#PropertiesAbelianGroupExtensions)

* [Schreier theory for nonabelian extensions](#SchreierTheory)


### General 
 {#PropertiesGeneral}


#### Fibers of extensions are normal subgroups

+-- {: .num_prop }
###### Proposition

For $A \hookrightarrow \hat G \to G$ a group extension, the inclusion $A \hookrightarrow \hat G$ is a [[normal subgroup]] inclusion.

=--

+-- {: .proof}
###### Proof

We need to check that for all $a \in A \hookrightarrow G$ and $g \in G$ the result of the [[adjoint action]] $g a g^{-1}$ formed in $\hat G$ is again in $A \stackrel{i}{\hookrightarrow} \hat G$. 

Since $p : \hat G \to G$ is a group homomorphism we have that 

$$
  \begin{aligned}
    p(g a g^{-1}) & = p(q) p(a) p(g^{-1})
    \\
    & = p(g) p(a) p(g)^{-1}
    \\
    & = p(g) p(g)^{-1}
    \\
    & = 1
  \end{aligned}
$$

and hence $g a g^{-1}$ is in the [[kernel]] of $p$. By the defining exactness property therefore it is in the [[image]] of $i$. 

=--



#### Extensions as torsors / principal bundles
  {#Torsors}

+-- {: .num_prop}
###### Proposition

For $A \stackrel{i}{\to} \hat G \stackrel{p}{\to} G$ a group extension, we have that $p : \hat G \to G$ is an $A$-[[torsor]] over $G$ where  the [[action]] of $A$ on $\hat G$ is defined by

$$  
  \rho : A \times \hat G \stackrel{(i,Id)}{\to} \hat G \times_G \hat G \stackrel{\cdot}{\to} \hat G
  \,.
$$


=--

+-- {: .proof}
###### Proof

That $\rho$ is indeed an action _over_ $B$ in that

$$
  \array{  
     A \times \hat G &&\stackrel{\rho}{\to}&& \hat G
     \\
     & {}_{\mathllap{ p \circ p_2}}\searrow && \swarrow_{\mathrlap{p}}
     \\
     &&  G 
  }
$$

follows from the fact that $p$ is a group homomorphism and that $A$ is in its [[kernel]].

That $A$ is actually _equal_ to the kernel gives the principality condition

$$
  (\rho, p_2) : A\times \hat G \stackrel{\simeq}{\to} \hat G \times_G \hat G
  \,.
$$

=--

For $A$ an [[abelian group]] we may understand the $A$-torsor/$A$-[[principal bundle]] $\hat G$ as the [[delooping]] of the $\mathbf{B}A$-[[principal 2-bundle]] $\mathbf{B} \hat G \to \mathbf{BG}$ that is classified by (is the [[homotopy fiber]] of) the 2-[[cocycle]] in [[group cohomology]]  $c : \mathbf{B}G \to \mathbf{B}^2 A$ that classifies the extension.

All this is then summarized by the statement that

$$
  A \to \hat G \to G \to \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G \stackrel{c}{\to}
  \mathbf{B}^2 A
$$

is a [[fiber sequence]] in [[∞Grpd]] (or in [[?LieGrpd]] if we have [[Lie group]] extensions, etc).

Here we may think of $\mathbf{B}\hat G$ as being the $\mathbf{B}A$-[[principal 2-bundle]] over $\mathbf{B}G$ classified by $c$. See the examples discussed at [[bundle gerbe]].


#### Split extensions and semidirect product groups
 {#SplitExtensionsAndSemidirectProductGroups}


+-- {: .num_defn #SplitExtension}
###### Definition

A group extension $A \to \hat G \stackrel{p}{\to} G$ is called **split** if there is a [[section]] [[homomorphism]] $\sigma \colon G \to \hat G$, hence a group homomorphism such that $p \circ \sigma = id_G$.

=--

+-- {: .num_remark}
###### Remark

It is important here that $\sigma$ is itself required to be a group homomorphism, not just a [[function]] on the underlying sets. The latter always exists as soon as the [[axiom of choice]] holds, since $p$ is an [[epimorphism]] by definition.

=--

+-- {: .num_prop #SplitExtensionsAreSemidirectProducts}
###### Proposition

Split extensions $\hat G$ of $G$ by $A$, def. \ref{SplitExtension}, are equivalently [[semidirect product groups]] 

$$
  A \hookrightarrow \hat G \simeq A \rtimes_\rho G \to G
$$

for some [[action]] $\rho \colon G \times A  \to A$ of $G$ on $A$. 

=--

This means that the underlying set is $U(A \rtimes_\rho G) = U(A) \times U(G)$ and the group operation in $A \rtimes_\rho G$ is 

$$
  (a_1, g_1) \cdot (a_2, g_2)
  = 
  (a_1 \cdot \rho(g_1)(a_2) , g_1 \cdot g_2)
  \,.
$$

The inclusion of $A$ is by

$$
  a \mapsto (a,e)
$$

and the projection to $G$ is by

$$
  (a,g) \mapsto g
  \,.
$$


+-- {: .proof}
###### Proof

Given a split extension $A \stackrel{i}{\to} \hat G \stackrel{p}{\to} G$ with splitting $\sigma \colon G \to \hat G$, define an [[action]] of $G$ on $A$ by the restriction of the [[adjoint action]] $\rho_{ad}$ of $\hat G$ on itself to $A$:

$$
  \rho 
    \colon 
  A \times G 
   \stackrel{(i,\sigma)}{\to}
 \hat G \times \hat G
   \stackrel{\rho_{ad}}{\to}
 \hat G
$$

$$
  (a,g) \mapsto \sigma(g)^{-1} \cdot a \cdot \sigma(g)
  \,.
$$

Then (...)

=--

+-- {: .num_prop}
###### Proposition

A split extension $A \to \hat G \to G$ is a [[central extension]] precisely if the [[action]] $\rho$ induced from it as in prop. \ref{SplitExtensionsAreSemidirectProducts} is trivial.

=--

+-- {: .proof}
###### Proof

For it to be a central extension the inclusion $A \to A \rtimes_\rho G$ has to land in the [[center]] of $A \rtimes_\rho G$, hence all elements $a \in A$ have to commute as elements $(a,e) \in A \rtimes_\rho G$ with all elements of $A \rtimes_\rho G$. But consider elements of the form $(e,g) \in A \rtimes_\rho G$ for all $g \in G$. Then

$$
  (a,e) \cdot (e,g) = (a, g)
$$

but

$$
  (e,g) \cdot (a,e) = (\rho(g)(a), g)
  \,.
$$

For these to be equal for all $a \in A$, $\rho(g)$ has to be the identity. Since this is to be true for all $g \in G$, the action has to be trivial. 

=--

+-- {: .num_prop}
###### Remark

This means in particular that split central extensions are product groups $A \to G$. If all groups involved are [[abelian groups]], then these are equivalently the [[direct sums]] $A \oplus G$ of abelian groups. In this way the notion of split group extension reduces to that of [[split short exact sequences]] of abelian groups.

=--

+-- {: .num_prop}
###### Remark

If we have a split extension the different  splittings are given by [[derivation on a group|derivation]]s, but with possibly non-abelian values. In fact if we have $s: G\to A\rtimes G$ is a section then $s(g) = (a(g),g)$, and the multiplication in $A\rtimes G$ implies that $a: G\to A$ is a derivation. These are considered as the (possibly non-abelian) 1-cocycles of $G$ with (twisted) coefficients in $A$, as considered in, for instance, Serre's notes on [[Galois cohomology]].

=--
### Central group extensions
 {#PropertiesCentralGroupExtensions}

We discuss properties of _central_ group extensions, those where $A \hookrightarrow \hat G$ factors through the [[center]] of $\hat G$. This is a special case of the general discussion below in _[Nonabelian group extensions (Schreier theory)](#SchreierTheory)_ but is considerably less complex to write out in components.

We first discuss the

* [Classification by group cohomology](#CentralExtensionClassificationByGroupCohomology)

of central extensions in components, and then show in 

* [Formulation in homotopy theory](#FormulationInHomotopyTheory)

how this follows from a more systematic abstract theory.

#### Classification by group cohomology
 {#CentralExtensionClassificationByGroupCohomology}

We discuss the classification of _central_ extensions by [[group cohomology]]. This is a special case of the more general (and more complicated) discussion below in _[Nonabelian group extensions (Schreier theory)](#SchreierTheory)_.

For $G$ a [[group]] and $A$ an [[abelian group]], write 

$$
  H^2_{grp}(G,A) \;\; \in Ab
$$ 

for the degree-2 [[group cohomology]] of $G$ with [[coefficients]] in $A$, and write 

$$
  Ext(G,A) \;\;\in Ab
$$

for the group of central extensions of $G$ by $A$.


+-- {: .num_theorem }
###### Theorem

There is a [[natural equivalence]]

$$
  Ext(G,A) \simeq H^2_{Grp}(G,A)
  \,.
$$


=--

We prove this below as prop. \ref{ExtractionAndReconstructionConsituteEquivalence}. Here we first introduce stepwise the ingredients that go into the proof.

+-- {: .num_defn #CentralExtensionAssociatedTo2Cocycle}
###### Definition
**(central extension associated to group 2-cocycle)**

For $[c] \in H^2_{Grp}(G,A)$ a [[group cohomology]] class represented by a [[cocycle]] $c \colon G \times G \to A$, define a group 

$$
  G \times_c A \in Grp
$$

as follows. The underlying set is the [[cartesian product]] $U(G) \times U(A)$ of the underlying sets of $G$ and $A$. The group operation on this is given by

$$
  (g_1, a_1) \cdot (g_2, a_2)
  \coloneqq
  (g_1 \cdot g_2 ,\; a_1 + a_2 + c(g_1, g_2))
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

This defines indeed a group: the [[cocycle]] condition on $c$ gives precisely the  [[associativity]] of the product on $G \times_c A$.
Moreover, the construction extends to a [[homomorphism]] of groups

$$
  Rec : H^2_{Grp}(G,A) \to Ext(G,A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Forming the product of three elements of $G \times_c A$ bracketed to the left is, according to def. \ref{CentralExtensionAssociatedTo2Cocycle},

$$
  \left(
    \left(g_1, a_1\right) \cdot \left(g_2, a_2\right)
  \right)
  \cdot
  \left(
    g_3, a_3
  \right)
 = 
  \left( 
    g_1 g_2 g_3 \;,\; a_1 + a_2 + a_3 
    + 
    c(g_1, g_2) +  c\left(  g_1 g_2, g_3 \right) 
  \right)
  \,.
$$

Bracketing the same three elements to the right yields

$$
  \left(g_1, a_1\right) 
   \cdot 
  \left(
     \left(g_2, a_2\right)
     \cdot
   \left(
    g_3, a_3
  \right)
 \right)
 = 
  \left( 
    g_1 g_2 g_3 \;,\; a_1 + a_2 + a_3 
    + 
    c(g_2, g_3) +  c\left(  g_1 , g_2 g_3 \right) 
  \right)
  \,.
$$

The difference between the two expressions is read off to be precisely

$$
  (1, (d c) (g_1, g_2, g_3))
 \,,
$$

where $d c$ denotes the group cohomology differential of $c$. Hence this vanishes precisely if $c$ is a group 2-cocycle, hence we have an associative product.

To see that it has inverses, notice that for all $(g,a)$ we have

$$
  (g,a)
  \cdot
  (g^{-1}, - a - c(g,g^{-1}))
  = 
  (e, a - a - c(g,g^{-1})+ c(g,g^{-1}) )
$$

and hence inverses are given by $(g,a)^{-1} = (g^{-1}, -a - c(g,g^{-1}))$. Hence $G \times_c A$ is indeed a group. 

By the discussion at [group cohomology  -- degree-2](group+cohomology#Degree2) we may assume without restriction that $c$ is a normalized cocycle, hence that $c(e,-) = c(-,e) = 0$. Using this we find that the inclusion 

$$
  i \colon A \to G \times_c A
$$

given by $a \mapsto (e,a)$ is a group homomorphism. Moreover, the projection on the underlying sets evidently yields a group homomorphism $p \colon G \times_c A \to G$ given by $(g,a) \mapsto g$. The kernel of this is $A$, and hence 

$$
  A \stackrel{i}{\hookrightarrow} G \times_c A \stackrel{p}{\to} G
$$

is indeed a group extension. It is a [[central extension]] again using the assumption that $c$ is normalized $c(g,e) = c(e,g) = 0$:

$$
  (g,a) \cdot (e,\tilde a) = (g, a + \tilde a + 0) = (e,\tilde a) \cdot (g,a)
  \,.
$$

Finally to see that the construction is independent of the choice of coycle $c$ representing $[c]$, let $\tilde c$ be another representative which differs by a [[coboundary]] $h \colon G \to A$ with

$$
  \tilde c (g_1,g_2) \coloneqq c(g_1,g_2) - h(g_1) - h(g_2) + h(g_1 g_2)
  \,.
$$

We claim that then we have a homomorphism of central extensions (hence an isomorphism) of the form

$$  
  \array{
     A &\to& G \times_c A &\to& G
     \\
     \downarrow^{\mathrlap{id}} 
      && 
     \downarrow^{\mathrlap{(id_G, p_2 -h \circ p_1)}} && \downarrow^{\mathrlap{=}}
     \\
     A &\to& G \times_{\tilde c} A &\to& G
  }
  \,.
$$

To see this we check for all elements that

$$
  \begin{aligned}
   (g_1, a_1 - h(g_1)) \cdot (g_2, a_2 - h(g_2))
   & = 
   (g_1 g_2, a_1 + a_2 - h(g_1) - h(g_2) + c(g_1, g_2))
   \\
   & = 
  (g_1 g_2, a_1 + a_2 + \tilde c(g_1, g_2) - h(g_1 g_2) )
  \end{aligned}
  \,.
$$

Hence the construction of $G \times_c A$ indeed defines a function $H^2_{Grp}(G,A) \to CentrExt(G,A)$. 

=--

Assume the [[axiom of choice]] in the ambient [[foundations]].

+-- {: .num_defn #2CocycleExtractedFromCentralExtension}
###### Definition
**(2-cocycle extracted from central extension)**

Given a central extension $A \to \hat G \to G$ define a group 2-cocycle $c : G \times G \to A$ as follows.

Choose a [[section]] $\sigma : U(G) \to U(\hat G)$ of the underlying [[sets]] (which exists by the [[axiom of choice]] and the fact that $p : \hat G \to G$ is by definition an [[epimorphism]]). Then define $c$ by

$$
  c
  \colon
  (g_1, g_2) 
    \mapsto
  -\sigma(g_1)^{-1} \sigma(g_2)^{-1} \sigma(g_1 g_2)
  \in A
  \,,
$$

where on the right we are using that by the section-property of $\sigma$ and the group homomorphism property of $p$

$$
  p(\sigma(g_1)^{-1} \sigma(g_2)^{-1} \sigma(g_1 g_2)) = 1
$$

and hence by the exactness of the extension the argument is in $A \hookrightarrow \hat G$.

=--

Below in remark \ref{RelationBetweenComponentCocycleExtractionAndHomotopyTheory} is a discussion of how this construction arises from a more systematic discussion in [[homotopy theory]].

+-- {: .num_prop}
###### Proposition

The construction of prop. \ref{2CocycleExtractedFromCentralExtension} indeed yields a 2-cocycle in [[group cohomology]]. It extends to a morphism

$$
  Extr \colon Ext(G,A) \to H^2_{Grp}(G,A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The cocycle condition to be checked is that 

$$
  c(g_1, g_2) - c(g_0 g_1, g_2) + c(g_0, g_1 g_2) - c(g_0, g_1)
  = 
  1
$$

for all $g_0, g_1, g_2 \in G$. Writing this out with def. \ref{2CocycleExtractedFromCentralExtension} yields

$$
  \sigma(g_1)^{-1} \sigma(g_2)^{-1} \sigma(g_1 g_2)
  \left(\sigma(g_0 g_1)^{-1} \sigma(g_2)^{-1} \sigma(g_0 g_1 g_2)\right)^{-1}
  \sigma(g_0)^{-1} \sigma(g_1 g_2)^{-1} \sigma(g_0 g_1 g_2)
  \left( \sigma(g_0)^{-1} \sigma(g_1)^{-1} \sigma(g_0 g_1)  \right)^{-1}
  \,.
$$

Here it is sufficient to observe that for every term also the inverse term appears.

To see that this is a well-defined map to $H^2_{grp}(G,A)$ we need to check that for $\tilde \sigma : G \to \hat G$ a different choice of section, the corresponding cocycles differ by a group coboundary $\tilde c - c = d h$. Clearly this is obtained by setting

$$
  h \colon g \mapsto \tilde \sigma(g)\sigma(g)^{-1}
  \,,
$$

where we use that the right hand side is in $A \hookrightarrow \hat G$ since because both $\sigma$ and $\tilde \sigma$ are sections of $p$, the image of the right hand under $p$ is the neutral element in $G$.

=--

+-- {: .num_prop #ExtractionAndReconstructionConsituteEquivalence}
###### Proposition

The two morphisms of  def. \ref{CentralExtensionAssociatedTo2Cocycle} and
def. \ref{2CocycleExtractedFromCentralExtension} exhibit the [[equivalence]]

$$
  H^2_{Grp}(G,A) \stackrel{\underoverset{\simeq}{Extr}{\leftarrow}}{\underset{Rec}{\to}} CentrExt(G,A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let $[c] \in H^2_{Grp}(G,A)$. Then by construction of $\hat G \coloneqq G \times_c A$ there is a canonical section of the underlying function of sets $U(G \times_c A) \to U(G)$ given by $(id_{U(G)}, 0) U(G) \to U(G) \times U(A)$. The cocycle induced by this section sends

$$
  \begin{aligned}
    (g_1, g_2) & \mapsto (g_1, 0) (g_2, 0) (g_1 g_2, 0)^{-1}
    \\
    & = 
    (g_1, 0) (g_1, 0) ((g_1 g_2)^{-1}, - c(g_1 g_2, (g_1 g_2)^{-1}) )
    \\
    & =  (g_1 g_2, c(g_1, g_2) ) ((g_1 g_2)^{-1}, - c(g_1 g_2, (g_1 g_2)^{-1}) )
    \\
    & = (e, c(g_1, g_2) - c(g_1 g_2, (g_1 g_2)^{-1}) + c(g_1 g_2, (g_1 g_2)^{-1}))
   \\
   & = (e, c(g_1, g_2))
  \end{aligned}
  \,,
$$

which is $c(g_1, g_2) \in A \hookrightarrow G \times_c A$, and hence this recovers the 2-cocycle that we started with.

This shows that $Extr \circ Rec = id$ and in particular that $Rec$ is a [[surjection]]. It is readily seen that the [[kernel]] of $Rec$ is trivial, and so it is an equivalence.


=--

#### Formulation in homotopy theory
 {#FormulationInHomotopyTheory}

We discuss the classification of central group extensions by degree-2 [[group cohomology]] in the more abstract context of [[homotopy theory]] (via the translation discussed at _[[looping and delooping]]_), complementing the [above](CentralExtensionClassificationByGroupCohomology
) component-wise discussion. 


Let 

$$
  A \hookrightarrow \hat G \to G
$$ 

be a central group extension, def. \ref{GroupExtension}, hence with $A$ an [[abelian group]] included in the [[center]] of $G$. Then $A$ is in particular a [[normal subgroup]] and hence the homorphism

$$
  (A \to \hat G) 
$$ 

may be regarded as a [[crossed module]] of groups. This is equivalently a [[strict 2-group]] structure on the [[groupoid]] whose objects are $\hat G$ and whose morphisms are labeled in $A$

$$
  (A \to \hat G) = 
  \{ 
     g \stackrel{a}{\to} a \cdot g
  \}
  \,.
$$



+-- {: .num_defn }
###### Definition

Write

$$
  \mathbf{B}(A \to \hat G) \in Grpd
$$

for the [[delooping]] of this [[2-group]] to a one-object [[2-groupoid]].

The [[∞-nerve]] (or [[Duskin nerve]]) $N \mathbf{B}(A \to \hat G) \in $ [[sSet]] of this is a (3-[[coskeleton|coskeletal]]) [[Kan complex]] that realizes this as a [[truncated object of an (infinity,1)-category|2-truncated]]  [[∞-groupoid]]. 

$$
  \mathbf{B}(A \to \hat G) \in \infty Grpd
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The obvious strict [[2-functor]]

$$
  \mathbf{B}(A \to \hat G) \stackrel{\simeq}{\to} \mathbf{B}H
$$

is an [[weak homotopy equivalence|equivalence]] of 2-groupoids. 

=--

+-- {: .proof}
###### Proof

One way to see this is to notice that this is a [[k-surjective functor]] for all $k \in \{0,1,2,3\}$, hence a weak equivalence in the [[folk model structure]] on $\omega$-groupoids. Equivalently, under the [[nerve]] the morphism of [[simplicial sets]]

$$
  N\mathbf{B}(A \to \hat G) \to N \mathbf{B}H
$$

is an acyclic [[Kan fibration]], hence a [[weak equivalence]] in the standard [[model structure on simplicial sets]].

=--

+-- {: .num_prop }
###### Proposition

The extension $A \to \hat G \to G$ sits in a long [[homotopy fiber sequence]] in the [[(∞,1)-category]] [[∞Grpd]] of the form

$$
  A \to \hat G \to G \to \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^2 A
$$

which in [[Kan complexes]]/[[simplicial sets]] is [[presentable (infinity,1)-category|presented]] by  the [[zigzag]] of  [[n-functors]] between [[strict ∞-groupoid]] (sequence of [[2-anafunctors]]) of the form
 
$$
  \array{
     && && && && && \mathbf{B}(A \to \hat G) &\to & \mathbf{B}(A \to 1) = \mathbf{B}^2 A
     \\
     && && && && && {}^{\mathrlap{\simeq}}\downarrow
     \\
     &&  && (A \to \hat G) &\to& \mathbf{B}A &\to& \mathbf{B}\hat G &\to&  \mathbf{B}G
     \\
     && && \downarrow^{\mathrlap{\simeq}}
     \\
     A &\to& \hat G &\to& G
  }
  \,.
$$

In particular, the induced [[connecting homomorphism]]

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^2 A
$$

is the [[group cohomology]] [[cocycle]] that classifies the delooped extension as a $\mathbf{B}A$-[[principal 2-bundle]].

=--

+-- {: .proof}
###### Proof

One sees directly that the morphisms $\mathbf{B}\hat G \to \mathbf{B}G$ and  $\mathbf{B}(A \to \hat G ) \to \mathbf{B}^2 A $ as well as their loopings $\hat G \to G$ and  $(A \to \hat G) \to G$ are [[Kan fibrations]]. By the discussion at [[homotopy pullback]] this means that the set-theoretic [[fibers]] of these morphisms are models for their [[homotopy fibers]]. But the ordinary [[kernel]] of $\mathbf{B}(A \to \hat G) \to \mathbf{B}(A \to 1) = \mathbf{B}^2 A$ is manifestly $\mathbf{B} \hat G$, and so on.

=--

+-- {: .num_remark #RelationBetweenComponentCocycleExtractionAndHomotopyTheory}
###### Remark

The construction in def. \ref{2CocycleExtractedFromCentralExtension}

$$
  Rec : CentrExt(G,A) \to H^2_{Grp}(G,A)
$$

is precisely the result of moving set-theoretically through the [[zigzag]]

$$
  \array{
    \mathbf{B}(A \to \hat G) &\to& \mathbf{B}(A \to 1) = \mathbf{B}^2 A
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}G
  }
$$

from the bottom left to the top right, 
and that this is well-defined on [[cohomology]] comes down to the statement that the vertical morphism is a [[weak homotopy equivalence]].

This is a nonabelian analog of the discussion at _[[mapping cone]]_ in the section _[Homology exact sequences and fiber sequences](mapping%20cone#HomologyExactSequencesAndFiberSequences)_.

=--

### Abelian group extensions
 {#PropertiesAbelianGroupExtensions}

+-- {: .num_remark}
###### Remark

For $A, G \in $ [[Ab]] $\hookrightarrow$ [[Grp]] even a [[central extension]] $\hat G$ of $G$ by $A$ is not necessarily itself an abelian group. 

=--

But by prop. \ref{ExtractionAndReconstructionConsituteEquivalence} above it is so if the group 2-cocycle that classifies the extension is symmetric:

+-- {: .num_defn}
###### Definition

A 2-cocycle $c \colon G \times G \to A$ in [[group cohomology]] is **symmetric** if

$$
  \forall_{g_1, g_2 \in G} c(g_1, g_2) = c(g_2, g_1)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

A group 2-cocycle cohomologous to a symmetric group 2-cocycle is itself symmetric. Hence we may speak of symmetric group cohomology classes in degree 2.

=--


+-- {: .num_defn}
###### Definition

Write 

$$
  H^2_{Grp}(G,A)_{sym} \hookrightarrow H^2_{Grp}(G,A)
$$

for the set (group) of classes of symmetric group 2-cocycles on $G$ with coefficients in $A$. 

=--


+-- {: .num_defn}
###### Definition

For $G,A \in Ab \hookrightarrow Grp$, write
$Ext(G,A)$
for the subset of equivalence class of abelian group extensions of $G$ by $A$.

=--

The theory of _abelian group extensions_ in [[Ab]] is naturally and classically treated with tools of [[homological algebra]], such as the theory of [[Ext]]-functors.

For the moment see at _[[projective resolution]]_ the section 

* _[Projective resolutions adapted to group cocycles](projective+resolution#ProjectiveResolutionsForGroupCocycles)_

and

* _[Derived Hom-functor / Ext-functor](projective+resolution#DerivedHomFunctor)_ .

### Nonabelian group extensions (Schreier theory)
 {#SchreierTheory}

We discuss the classification theory for the general case of nonabelian
group extensions, first in the form of 

* _[Traditional Schreier theory](SchreierTheoryTraditional)_

and then more abstractly in the language of [[homotopy theory]] in

* _[Homotopy theory perspective on Schreier theory](#SchreierTheorynPOV)_


#### Traditional description
 {#SchreierTheoryTraditional}

[[Otto Schreier]] (1926) and [[Samuel Eilenberg|Eilenberg]]-[[Saunders MacLane|Mac Lane]] (late 1940-s) developed a theory of classification of nonabelian extensions of abstract groups leading to the low dimensional [[nonabelian group cohomology]]. This is sometimes called **Schreier's theory** of nonabelian group extensions.

The traditional Schreier-Mac Lane way to obtain nonabelian group 2-cocycle
from a group extension as above starts with choosing a set-theoretic section of $p:G\to B$. 

**Note.** The exposition which follows in this long "traditional" section of this entry is mainly from personal notes of Zoran &#352;koda from 1997. 

Each element $g$ of $G$ defines an inner automorphism $\phi(g)$ of $K$
by $\phi(g)(k) = gkg^{-1}$. 
The restriction $\phi|_K$ takes
(by definition) values in the subgroup $Int(K)$ of inner automorphisms
of $K$. In fact $\phi:G\to Inn(G)\subset Aut(K)$ is a homomorphism of groups.

If $g_1$ and $g_2$ are in the same left coset, that is $g_1K = g_2K$,
then there is $k \in K$, $g_1 = g_2k$, so that $\forall k' \in K$ we have
$\phi(g_1k') = \phi(g_2kk') = \phi(g_2)\phi(kk')$ and therefore
$\phi(g_1K) \subset \phi(g_2)Int(K)$. Thus we obtain a well-defined map
$\phi_* : G/K \rightarrow Aut(K)/Int(K)$.
Choose a set-theoretic section of the projection $p : G \rightarrow B$
and let
\[\psi \stackrel{def}{=} \phi \circ \sigma: B \rightarrow Aut(K).\]
**Warning.** Unlike $\phi$, the map $\psi$ is *not* a homomorphism of groups. 

We attempt to reconstruct $G$ from
the knowledge of $\psi$ and $K$.
As a set, $G$ can be naturally identified with $B \times K$.
Indeed, write each element $g \in G$ as
$\sigma(b)k, b \in B, k \in K$ by setting
$b = p(g), k = \sigma(p(g))^{-1}g$. 
Elements $b \in B$ and $k \in K$ in that decomposition are unique,
and we get a bijection
\begin{equation}
B\times K\ni (b,k)\mapsto\sigma(b)k \in G,
\end{equation}
whose inverse is the map $g \mapsto (p(g), \sigma(p(g))^{-1}g)$.
By means of that bijection, $B \times K$ inherits the group structure
from $G$. Let us figure out the multiplication rule on $B \times K.$
If $\sigma(b_1)k_1 = g_1$, and $\sigma(b_2)k_2 = g_2$, then,
\begin{equation}
g_1g_2 = \sigma(b_1)k_1\sigma(b_2)k_2 =
\sigma(b_1)\sigma(b_2)\sigma(b_2)^{-1}k_1\sigma(b_2)k_2.
\end{equation}
 Now $p(\sigma(b_1)\sigma(b_2)) = p(b_1b_2)$ so
$$\chi(b_1,b_2) \stackrel{def}{=}
 \sigma(b_1b_2)^{-1}\sigma(b_1)\sigma(b_2) \in K.
$$
This formula clearly
defines a function $\chi : B \times B \rightarrow K$. In this notation, 
$$\array{
g_1g_2 & = & \sigma(b_1b_2)\chi(b_1,b_2)\phi(\sigma(b_2)^{-1})(k_1)k_2 \\
       & = & \sigma(b_1b_2)\chi(b_1,b_2)[\psi(b_2)^{-1}(k_1)] k_2.
}$$
and using bijection of $G$ with $B\times K$ this can be expressed in terms of elements in $B\times K$ so that
\begin{equation}\label{mrule}
(b_1,k_1)(b_2,k_2) = (b_1b_2,\chi(b_1,b_2)[\psi(b_2)^{-1}(k_1)] k_2).
\end{equation}

According to this formula, *all the information about the multiplication is encoded in functions $\chi : B \times B \rightarrow Aut(K)$
and $\psi : B \rightarrow Aut(K)$, and we may forget about $\sigma$* at this point. However, _not every pair $(\chi,\psi)$ will
give some multiplication rule on $B \times K$_.
Let $a,b,c \in B$,
and $e = e_K$ be the unity element in $K$.
Then
$$
[(a,e)(b,e)](c,e) = (a b, \chi(a,b))(c,e) =
 (a b c, \chi(a b,c) \psi(c)^{-1}(\chi(a,b))).
$$
From the other side, this has to be the same, by associativity, to
$$
(a,e)[(b,e)(c,e)] = (a,e)(bc,\chi(b,c)) = (a b c,\chi(a,b c)\chi(b,c))
$$
where we took into account that expressions like $[\psi^{-1}(b)(e)] = e$,
because $\psi(b)$ is an *automorphism* for each $b \in B$.

 Comparing the expressions above we obtain
\[\label{psi1}
 \chi(a b,c)\psi(c)^{-1}(\chi(a,b)) = \chi(a,b c)\chi(b,c),
    for all a,b,c \in B.
\]

If the pair $(\chi,\psi)$ is constructed as above, then

$$\array{
\psi(a)\psi(b)k & = & \phi(\sigma(a))\phi(\sigma(b))k \\
        & = & \sigma(a)\sigma(b)k\sigma(b)^{-1}\sigma(a)^{-1} \\
        & = & \sigma(a b)\chi(a,b)k\chi(a,b)^{-1}\sigma(a b)^{-1} \\
        & = & \psi(a b) Ad_K(\chi(a,b)) k,
}$$

where $Ad_K$ is the canonical map $K \rightarrow Int(K)$, $k\mapsto k(-)k^{-1}$.

Thus we obtain the relation
\[\label{psi2}
\psi(a)\psi(b) = \psi(a b) Ad_K(\chi(a,b))
\]

+-- {: .num_defn}
###### Definition
Let $B$ and $K$ be two groups.
Let $\chi: B \times B \rightarrow K$
and $\psi : B \rightarrow Aut(K)$ satisfy \eqref{psi1}
and \eqref{psi2}. Then we call that the family
$\{\chi(b_1,b_2)| b_1,b_2 \in B\}$
is a factor system (This term is due Schreier(1924))
or a **nonabelian group 2-cocycle with automorphisms**, and
the family $\{\psi(b) | b \in B \}$ -- a system of automorphisms
=--

A 2-cocycle $\chi$ is **counital** if $\chi(b,e) = \chi(e,b) = e$, for all $b \in B$.

If $K$ is commutative, then $\psi$ is always a homomorphism (cf. (eq:psi2)). Then $K$ is a right $B$-module through $\psi(-)^{-1}$. That justifies the sometimes used term "(right) cocycle $B$-module" for $(K,\psi,\chi)$. If $\psi$ is trivial ($\psi(b) = Id_K, \forall b \in B$)
then the cocycle condition (eq:psi1) becomes
\begin{equation}
\chi(a b,c)\chi(a,b) = \chi(a,b c)\chi(b,c). 
\end{equation}

+-- {: .num_theorem}
###### Theorem
If formulas (eq:psi1) and (eq:psi2)
are both satisfied, then the formula (eq:mrule)
for multiplication of pairs defines a group multiplication on $B \times K$. That set, together
with multiplication (eq:mrule) is called the
**cocycle cross product** of $B$ and $K$ with cocycle $\chi$ and
action $\psi$. If the cocycle is trivial i.e. $\chi(\cdot,\cdot) = e_K$,
we call it the **(external) semidirect product**.
=--

+-- {: .proof}
###### Proof

We have checked above the [[associativity]] for pairs of the form $(a,e)$ etc. This was useful to find the cocycle condition correctly. Now the general associativity should be a similar calculation with general elements. Using (eq:psi1) and (eq:psi2) it can be done.

$$\array{
\psi(a)\psi(e)k & =& \psi(a)Ad_K(\chi(a,e))k \\
& = &\psi(a)\chi(a,e)k\chi(a,e)^{-1}
}$$
where we used \eqref{psi2}.

Thus $Ad_K(\chi(a,e)) = \psi(e)$ and therefore it does not
depend on $a$.

Then use (eq:psi1) with $b = c = e$ to get
$\psi(e)^{-1}(\chi(a,e)) = \chi(e,e), \forall a \in B$.

Thus $\chi(a,e)^{-1}(\chi(a,e))\chi(a,e) = \chi(e,e)$,
that is $\chi(a,e)$ does not depend on $a$.

Now we claim that the *unit* element is given by $(e, \chi(e,e)^{-1})$.
To verify that it is also a right unit we compute

$$\array{
(a,b)(e,\chi(e,e)^{-1}) & = & (a, \chi(a,e) \psi(e)^{-1}(b)\chi(e,e)^{-1}) \\
& = & (a, \chi(a,e)\chi(e,e)^{-1}b\chi(e,e)\chi(e,e)^{-1})
}$$

what is equal to $(a,b)$ by just proved statement that
$\chi(a,e)$ does not depend on $a$.

Now use (eq:psi1) with $a = b = e$ to get

\[\label{psiac}
\psi(c)^{-1}(\chi(e,e)) = \chi(e,c), \forall c \in B.
\]

Thus we can verify that $(e, \chi(e,e)^{-1})$ is a left unit too
by a calculation as follows. Namely

$$(e,\chi(e,e)^{-1})(a,b)= (a,\chi(e,a)\psi(a)^{-1}(\chi(e,e)^{-1})b)$$

by the definition of the product. Then by (eq:psiac), this equals to

$$(a,\psi(a)^{-1}(\chi(e,e))\psi(a)^{-1}(\chi(e,e)^{-1})b)$$

and, because $\psi(a)^{-1}$ is an antiautomorphism, this is finally
equal to $(a,b)$.

Now check that each element $(a,b)$ can be
factorized as $(a,e)(e,\chi(e,e)^{-1}b)$.
In order to show that $(a,b)$ has
an inverse it is then enough to
show that both $(a,e)$ and
$(e,\chi(e,e)^{-1}b)$ have inverses.

Claim: the inverse of $(a,e)$ is 

$$(a^{-1},\chi(a,a)^{-1}\chi(e,e)^{-1}).$$ 

To this aim, we calculate

$$(a,e)(a^{-1},\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}) = (e,\chi(a,a^{-1})\psi(a^{-1})^{-1}(e)\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}) =(e,\chi(e,e^{-1}),$$ 

because $\psi(a)^{-1}(e) = e$. Furthermore, 

$$(a,e)(a^{-1},\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}) = (e,\chi(a,a^{-1})\psi(a^{-1})^{-1}(e)\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}) = (e,\chi(e,e^{-1}),$$ 

because $\psi(a)^{-1}(e) = e$. Next, 

$$(a^{-1},\chi(a,a^{-1})^{-1}\chi(e,e)^{-1})(a,e) =
(e,\chi(a^{-1},a)\psi(a)^{-1}(\chi(a,a^{-1}) \chi(e,e)^{-1}))$$ 

what equals $(e,\chi(e,e)^{-1})$.

Indeed, (eq:psi1) with $a = a, b = a^{-1}, c = a$
reads $\chi(e,a) \psi(a)^{-1}(\chi(a, a^{-1}))$ $=\chi(a,e)\chi(a^{-1},a)$.

Then apply (eq:psiac) and take inverse of both sides
to obtain

$$\psi(a)^{-1}(\chi(a,a^{-1})^{-1}\chi(e,e)^{-1}))
= \chi(a^{-1},a)^{-1}\chi(a,e)^{-1}.$$ 

Then recall that $\chi(a,e)$ does not depend on $a$ and multiply by  $\chi(a^{-1},a)$ from the left.

Claim: the inverse of $(e,\chi(e,e)^{-1}k)$
is $(e,\chi(e,e)k^{-1})$.
Here the verification is symmetric ($k$ vs. $k^{-1}$) for the left and for the right inverse and immediate.
=--

Given groups $K$ and $B$ and any maps $\chi$ and $\psi$ satisfying (eq:psi1) and (eq:psi2), needed to define a cocycle cross product $B\times_\chi K$ of $K$ and $B$, one defines the map $i : K \rightarrow B \times_\chi K$ by $k \mapsto (e,\chi(e,e)^{-1}k)$.
Then $i$ is a monomorphism of groups, $i(K)$ is
a normal subroup of the cocycle cross product of $B$ and $K$,
and there is a canonical isomorphism $B \cong G/K$.
We define the set-theoretic maps $\sigma',\chi'$ and $\psi'$
as follows. $\sigma' : B \rightarrow B \times K$
is defined by $\sigma'(b) = (b, e)$ , for all $b \in B$.
Then $\chi' : B \times B \to i(K)$ is defined by
$\chi'(b_1,b_2) = \sigma'(b_1b_2)^{-1}\sigma'(b_1)\sigma'(b_2)$
and $\psi' : B \to Aut(i(K))$ is defined
    by $\psi'(b)i(k) = \sigma'(b)i(k)\sigma'(b)^{-1}$.
Using the natural identifications $i : K \cong i(K)$,
and $i_{Aut} : Aut(i(K)) \cong Aut(K)$, we have $\psi' = i_{Aut}\circ \psi$ and $\chi' = i \circ \chi$. Now

$$\array{
\chi'=i\circ\chi 
&\Leftrightarrow&(b_1,e)(b_2,e)(e,\chi(e,e)^{-1}k)
=(b_1 b_2,e)(e,\chi(e,e)^{-1}\chi(b_1,b_2)k)\\
&\Leftrightarrow& (b_1b_2,\chi(b_1,b_2))(e,\chi(e,e)^{-1}k) = (b_1 b_2,\chi(b_1 b_2,e)\chi(e,e)^{-1}\chi(b_1,b_2)k)\\
&\Leftrightarrow&
\chi(b_1 b_2,e)\psi(e)^{-1}(\chi(b_1,b_2))\chi(e,e)^{-1}k = \chi(b_1 b_2,e)\chi(e,e)^{-1}\chi(b_1,b_2)k
}$$

for all $b_1,b_2 \in B$ for all $k \in K$ in all these lines.
The last line is true by (eq:psi1).

Similarly, $\psi' = i_{Aut} \circ \psi$ iff $(b,e)(e,\chi(e,e)^{-1}k) = (e,\chi(e,e)^{-1}\psi(b)k)(b,e)$ for all $b$ and $k$. 

Here the LHS computes as $(b,k)$ using $\chi(b,e) = \chi(e,e)$, and the RHS is 

$$(e,\psi(b)k)(b,e) = (b, \chi(e,b)\psi(b)^{-1}(\chi(e,e)^{-1}\psi(b)(k)))
= (b, k)$$

by (eq:psiac).


+-- {: .num_prop }
###### Proposition

The following are equivalent

* (i) extension \eqref{shortExtension} is split

* (ii) for extension \eqref{shortExtension}
there is a subgroup $B_1 \subset G$ such that
$B_1 \cap i(K) = 1$ and $B_1i(K) = G$
($G$ is an internal semidirect product of $K$ and $B_1$).

* (iii) extension \eqref{shortExtension} is
isomorphic to an external semidirect product
of $K$ and $B$. 

=--

+-- {: .proof}
###### Proof

(i) $\Rightarrow$ (ii) If the extension is split then
there is a *homomorphism* $\sigma : B \rightarrow G$
such that $p \circ \sigma = id_B$. Let $B_1 = \sigma(B)$.
By exactness of \eqref{shortExtension}), all
elements in $i(K)$ map $p$ sends to 1, and by
 $p \circ \sigma = id_B$ map $p|_{B_1}$ is injection,
therefore the only element in $i(K)$
which belongs to $B_1$ is 1.

$B_1i(K) = G$ is also obvious: e.g. for given $g \in G,$
$p(g) = p\sigma p(g)$, so that $p((\sigma p (g))^{-1}g) = 1$
what means $(\sigma p (g))^{-1}g \in {Ker}(p)$ so that
$g = (\sigma p (g))i(k)$ for some $k \in K$ by exactness.


(ii) $\Rightarrow$ (iii) Our previous elaborate discussion of
cocycle cross products makes it obvious:
choosing a section $\sigma$ which is a homomorphism
gives $\chi(a,b) = 1$, and we can construct
equivalent external semidirect product
as a cocycle cross product with trivial $\chi$.

(iii) $\Rightarrow$ (i) Equivalence of extensions preserves the
property of the corresponding short exact sequence to be split.
Every external semidirect product is as a set $K\times B$
and the product is given by formula \eqref{mrule} without a cocycle.
The map $\sigma : B \rightarrow G$,
$B \ni b \mapsto (1_K,b) \in K \times B$, splits the sequence.

=--

+-- {: .num_defn }
###### Definition

An extension \eqref{shortExtension} is Abelian
iff $K$ is Abelian. An Abelian extension \eqref{shortExtension}
is central iff it is isomorphic to a cocycle cross product
extension with all the automorphisms $\psi(b), b \in B$ trivial.
We say that the extension \eqref{shortExtension}
is Abelian iff $G$ is Abelian.

=--

Remarks. (i) Note that \eqref{psi2} implies that $\psi$
is a homomorphism if $K$ in the case of Abelian extensions (for
any choice of set-theoretic section $\sigma$.

(ii) If $G$ is Abelian then \eqref{shortExtension} is central,
but not every central extension is corresponding to an Abelian $G$.
Abelian extensions in terms of the above definition trivially
(strictly!) include both central extensions and extensions with $G$
central.
By abuse of language one sometimes says for $G$
to be an extension of $K$ what leads to strange expression that not every
Abelian extension (as extension -- in terms of the definition above) is Abelian (as a group).



#### Comparing different extensions;  2-coboundaries {#2Coboundaries}

Let us now investigate when two extensions
$G_1$ and $G_2$ of $B$ by $K$,
given by $\psi,\chi$ and $\psi',\chi'$ respectively, are equivalent, cf. diagram \eqref{equivExt}.

We know that $\epsilon|_K : i(k) \stackrel{\epsilon}\mapsto i'(k)$, for all $k \in K$.
The formula for $i$ in \luse{crossform} says that whenever we represent
an extension as a cocycle extension we have $i(k) = (e,\chi(e,e)^{-1}k).$
Thus $\epsilon(e,\chi(e,e)^{-1}k) = (e,\chi'(e,e)^{-1}k)$, for all $k \in K.$ Also recall (or recalculate) that every element $(a,k)$ in $G$ can be
factorized as $(a,e)(e,\chi(e,e)^{-1}k)$.
By the definition $\epsilon$ is a homomorphism of groups,
so $\epsilon(a,k) = \epsilon(a,e)\epsilon(e,\chi(e,e)^{-1}k)$.
Also the cosets are preserved, so $\epsilon(a,e) = (a,\lambda(a))$
where $\lambda : B \rightarrow K$ is some set-theoretic map.
Thus

$$\array{
\epsilon(a,k) & = & (a,\lambda(a))(e,\chi'(e,e)^{-1}k) \\
    & = & (a, \chi'(a,e)\psi'(e)^{-1}(\lambda(a))\chi'(e,e)^{-1}k) \\
    & = & (a, \lambda(a)k).
}$$

Now multiply more general elements in $G$:

$$
\array{
\epsilon((b_1,k_1)(b_2,k_2)) = (b_1,\lambda(b_1)k_1)(b_2,\lambda(b_2)k_2) \\
= (b_1b_2,\chi'(b_1,b_2)\psi'(b_2)^{-1}(\lambda(b_1)k_1)\lambda(b_2)k_2)
}$$

what should be the same as

\[
\epsilon((b_1b_2,\chi(b_1,b_2)\psi(b_2)^{-1}(k_1)k_2))
 = (b_1b_2,\lambda(b_1b_2)\chi(b_1b_2)\psi(b_2)^{-1}(k_1)k_2)
\]

In a special case, when $k_1 = e_K$ we have therefore

\begin{equation}
\chi(b_1,b_2) = \lambda(b_1b_2)^{-1}\chi'(b_1,b_2)
\psi'(b_2)^{-1}(\lambda(b_1))\lambda(b_2) \label{equiv1}
\end{equation}

In order to obtain a relation between $\psi'(b)(k)$
and $\psi(b)(k)$ note that
\[
\epsilon ((e,\chi(e,e)^{-1}k)(b,e)) = (e, \chi'(e,e)^{-1}k)(b,\lambda(b)).
\]
That is equivalent to any in the following chain of formulas:
$$\array{
\epsilon (b,\chi(e,b)\psi(b)^{-1}(\chi(e,e)^{-1}k)) &=&
    (b, \psi'(b)^{-1}(\chi'(e,e)^{-1}k)\lambda(b)) \\
\Leftrightarrow \lambda(b)\chi(e,b)\psi(b)^{-1}(\chi(e,e)^{-1}k))
&=& \chi'(e,b)\psi'(b)^{-1}(\chi'(e,e)^{-1}k)\lambda(b) 
}$$

Then by \eqref{psiac}, it follows that 
$$\array{
     \lambda(b)\chi(e,b)\chi(e,b)^{-1}\psi(b)^{-1}(k)
&=& \chi'(e,b)\chi'(e,b)^{-1}\psi'(b)^{-1}(k)\lambda(b)   \\
\Leftrightarrow \lambda(b)\psi(b)^{-1}(k))
&=& (\psi'(b)^{-1}(k))\lambda(b) \\
\Leftrightarrow (Ad_K(\lambda(b)) \circ\psi(b)^{-1})(k)
&=& \psi'(b)^{-1}(k)
}$$

Now invert the maps in $Aut(K)$ to obtain

\[
\psi'(b) = \psi(b)Ad_K(\lambda(b)^{-1}) \label{equiv2}
\]

Thus we obtain


+-- {: .num_theorem }
###### Theorem

Two extensions of a group $B$ by group $K$ with
corresponding systems $(\psi,\chi)$ and $(\psi',\chi')$ are
equivalent iff there is a [[homomorphism]]
$\lambda: B \rightarrow K$ such that
the relations \eqref{equiv1}
and \eqref{equiv2} are valid.

=--

+-- {: .proof}
###### Proof

If function $\lambda$ takes values in the center of $B$
then \eqref{equiv2} implies that $\psi' = \psi : B \rightarrow Aut(K)$
and conversely.

If instead of functions $\psi$ and $\psi'$ we consider the
respective maps into the group of external automorphisms
(cosets of automorphisms with respect
to the group of internal homomorphisms)
$[\psi], [\psi']:~B \rightarrow Aut(K)/Int(K)$,
then the equivalent extensions define the same maps.
By \eqref{psi2} these maps are actually homomorphisms (unlike e.g.$\psi$).
For a given $\psi$ if there is $\chi$ so that $(\psi,\chi)$ does define
an extension of $B$ by $K$ we say that
the extension is *associated* to (the homomorphism) $[\psi]$.
That does not mean that any given homomorphism
in $hom_{Group}(B,Aut(K)/Int(K))$
is associated to any extension, nor it means that if
a homomorphism is associated to some extension,
that every its representative in $hom_{Set}(B,Aut(K))$
is a part of a pair $(\psi,\chi)$ defining an extension.
To see that situation in more detail we start with a *given*
automorphism, which we call $\theta$ ,
and *choose* an element $\psi(a)\in\theta(a)$, the representative
of a coset in $Aut(K)/Int(K)$;
that choice should be specified for all $a \in B$.
Note that for any $\rho \in Aut(K), a \in K$ we have, by direct inspection,
$\rho Ad_K(a)\rho^{-1} = Ad_K(\rho(a))$. Thus there is a well-defined function

$$  Ad_K \circ h : B \times B \rightarrow Int(K), \,\,\,
(Ad_K\circ h)(a,b) := \psi(a b)^{-1}\psi(a)\psi(b)$$

- indeed 

\[\psi(a)Ad_K(r_1)\psi(b)Ad_K(r_2) = \psi(a)\psi(b)Ad_K(\psi(b)^{-1}(r_1)r_2)\] 

so choosing $\psi(a b) \in [\psi(a b)]$ is the same as choosing it in $[\psi(a)][\psi(b)]$ and guarantees that $\psi(a b)^{-1}\psi(a)\psi(b)$ is in $Int(K)$. Let us choose some $h$ so that $Ad_K \circ h$ is interpretable as a genuine composition.

$$\array{
(\psi(a)\psi(b))\psi(c) & = & \psi(a b)Ad_K(h(a,b))\psi(c) \\
    & = & \psi(a b)\psi(c)\psi(c)^{-1}Ad_K(h(a,b))\psi(c) \\
    & = & \psi(a b c)Ad_K(h(a b,c))Ad_K(\psi(c)^{-1}h(a,b)) \\
    & = & \psi(a b c)Ad_K(h(a b,c)\psi(c)^{-1}h(a,b))
}$$

what is by associativity the same as

$$\array{
\psi(a)(\psi(b)\psi(c)) & = & \psi(a)\psi(b c)Ad_K(h(b,c)) \\
    & = & \psi(a b c)Ad_K(h(a,b c))Ad_K(h(b,c)) \\
    & = & \psi(a b c)Ad_K(h(a,b c)h(b,c)).
}$$

Thus $Ad_K(h(a b,c)\psi(c)^{-1}h(a,b)) = Ad_K(h(a,b c)h(b,c)).$
Two elements of $K$ generate the same automorphism iff they
differ by a central element. Thus

\begin{equation} \label{2semicoc}
h(a b,c)\psi(c)^{-1}h(a,b) = h(a,b c)h(b,c)z(a,b,c)
\end{equation}

for a unique central element $z(a,b,c) \in Z(K).$
 The correspondence $z : (a,b,c) \mapsto z(a,b,c)$ maps
$B \times B \times B$ into $Z(K)$.

=--

+-- {: .num_prop }
###### Proposition

$z$ is an (Abelian) 3-cocycle with values
 in $_/Z(K)_{\psi^{-1}}$
($Z(K)$ understood as trivial-$\psi^{-1}$ $B$-bimodule):

\begin{equation}
z(b,c,d)z(a,b c,d)\psi(d)^{-1}z(a,b,c) = z(a,b,c d)z(a b,c,d)
\label{3coc}
\end{equation}

=--

+-- {: .proof}
###### Proof

To see this we calcuate
$$\array{
h(a b c,d)[\psi(d)^{-1}h(a b,c)\psi(c)^{-1}h(a,b)]
& = h(a b c,d)[\psi(d)^{-1}h(a,b c)h(b,c)z(a,b,c)] \\
& = h(a,b c d)h(b c,d)z(a,b c,d)[\psi(d)^{-1}h(b,c)z(a,b,c)] \\
& = h(a,b c d)h(b,c d)h(c,d)z(b,c,d)z(a,b c,d)\psi(d)^{-1}z(a,b,c)
}$$
Compare
$$\array{
h(a b c,d)[\psi(d)^{-1}h(a b,c)\psi(c)^{-1}h(a,b)]
& = h(a b c,d)[\psi(d)^{-1}h(a,b c)]\psi(d)^{-1}\psi(c)^{-1}h(a,b) \\
& = h(a b c,d)[\psi(d)^{-1}h(a b,c)]h(c,d)^{-1}[\psi(c d)^{-1}h(a,b)]h(c,d) \\
& = h(a b c,d)h(a b,c d)z(a b,c,d)[\psi(c d)^{-1}h(a,b)]h(c,d) \\
& = h(a,b c d)h(b,c d)h(c,d)z(a,b,c d)z(a b,c,d)
}$$

=--

+-- {: .num_prop }
###### Proposition

(i) If we choose a different $h$
such that 

$$Ad_K(h(a,b)) = \psi(a b)^{-1}\psi(a)\psi(b),$$

then $z$ will change only up to a 3-coboundary $d f,$
i.e. there is a function $f : B \times B \rightarrow Z(K)$,
such that $z' = (d f)z$ where

\[ (d f)(a,b,c) = f^{-1}(b,c)f^{-1}(a,b c)f(a b,c)\psi(c)^{-1}f(a,b),\,\,\,\,\,
for all a,b,c \in B.\]

(ii) Conversely, if $z$ is
a 3-cocycle obtained from $\psi$ as above and $d f$ is a 3-coboundary,
then there is a $h'$ determining
the same inner automoprhism of $K$
such that the corresponding 3-cocycle $z'$ is equal to $(df)z$.

(iii) Let $\psi, \psi' : B \rightarrow Aut(K)$ be
two set-theoretic sections so that $[\psi] = [\psi'] = \theta : B
\rightarrow Aut(K)/Int(K)$, then (for arbitrary choice of
$h$, $h'$) the cocycles $z$ and $z'$
obtained as above differ only up to a 3-coboundary. $\|$

=--

+-- {: .proof}
###### Proof

(i) Choose two different $h',h: B \times B \rightarrow K$
such that $Ad_K(h') = Ad_K(h)$. Then $h'(a,b) = h(a,b)f(a,b)$ where
$f : B \times B \rightarrow Z(K)$ is some function with values
in center of $K$.  A direct comparison of \eqref{2semicoc} written for
$h,z$ and $h',z'$ respectively proves the assertion.

(ii) Trivial: Any $f : B \times B \rightarrow Z(K)$
such that $h' = hf$ will not change the inner automorphism.
Thus any central 3-coboundary  $df$ can be obtained by
changing a choice of $h$.

(iii) $[\psi'] = [\psi]$ implies that exists $k : B \rightarrow K,
\psi'(a) = \psi(a)Ad_K(k(a)).$ Then

$$\array{
\psi'(a b)Ad_K(h'(a,b)) & = & \psi'(a)\psi'(b) = \psi(a)Ad_K(k(a))\psi(b)Ad_K(k(b))\\
& = & \psi(a)\psi(b)Ad_K([\psi(b)^{-1}k(a)]k(b)) \\
& = & \psi(a b)Ad_K(h(a,b)[\psi(b)^{-1}k(a)]k(b)) \\
& = & \psi'(a b)Ad_K(k(a b)^{-1}h(a,b)[\psi(b)^{-1}k(a)]k(b)).
}$$

Thus $ h'(a,b) = k(a b)^{-1}h(a,b)[\psi(b)^{-1}k(a)]k(b),$
for appropriate choice of $h'$ - what can change $z'$ up to coboundary -
using the freedom from (i). If we want formula involving $\psi'$
instead than we use $\psi'(a) = \psi(a)Ad_K(k(a))$ to obtain
$k(a b)h'(a,b) = h(a,b)k(b)[\psi'(b)^{-1}k(a)]$.
Using that and previous identities,

$$\array{
k(a b c)h'(a b,c)\psi'(c)^{-1}h'(a,b) 
&=& h(a b,c)k(c)[\psi'(c)^{-1}k(a b)]\psi'(c)^{-1}h'(a,b) \\
&=& h(a b,c)k(c)\psi'(c)^{-1}k(a b)h'(a,b) \\
&=& h(a b,c)k(c)\psi'(c)^{-1}h(a,b)k(b)[\psi'(b)^{-1}k(a)] \\
&=& h(a b,c)[\psi(c)^{-1}h(a,b)]k(c)\psi'(c)^{-1}k(b)[\psi'(b)^{-1}k(a)] \\
&=& h(a,b c)h(b,c)z(a,b,c)k(c)
    [\psi'(c)^{-1}k(b)][\psi'(c)^{-1}\psi'(b)^{-1}k(a)] \\
&=& h(a,b c)h(b,c)k(c)[\psi'(c)^{-1}k(b)]
    [\psi'(c)^{-1}\psi'(b)^{-1}k(a)]z(a,b,c) \\
&=& h(a,b c)k(b c)h'(b,c)[\psi'(c)^{-1}\psi'(b)^{-1}k(a)]z(a,b,c) \\
&=& h(a,b c)k(b c)h'(b,c)h'(b,c)^{-1}[\psi'(b c)^{-1}k(a)]h'(b,c)z(a,b,c)\\
&=& h(a,b c)k(b c)[\psi'(b c)^{-1}k(a)]h'(b,c)z(a,b,c)\\
&=& k(a b c)h'(a,b c)h'(b,c)z(a,b,c) 
}$$

for all $a,b,c \in B$. Thus $h'(a b,c)\psi'(c)^{-1}h'(a,b) = h'(a,b c)h'(b,c)z(a,b,c)$ i.e.
our choice of $h'$ insured no change in $z$. Of course that means
that in arbitrary choice of $h'$
we do not miss more than a coboundary by (i).

=--

+-- {: .num_cor }
###### Corollary

A given homomorphism
$\theta : B \times B \rightarrow Aut(K)/Int(K)$
is associated to some extension of $B$ by $K$ iff $z$ is
a 3-coboundary. 

=--


+-- {: .proof}
###### Proof

Indeed, if $\theta$ is associated to an extension,
then we know that there is an isomorphism of the extension with
a cross product given by some cocycle $\chi$ and
some automorphism $\psi$ such that $[\psi] = \theta$. But using
the identification, $\chi = h$ for that particular choice
of $\psi$, so that $z = 1$. By the proposition, every
other $z$ obtained from $\theta$ is in the same cohomology class,
thus every such $z$ is a coboundary. Conversely, if $z$ is
a coboundary, then by the proposition, we can change it to $z = 1$,
and then we have all the conditions for a cross product
extension satisfied.

=--

#### Formulation in homotopy theory 
 {#SchreierTheorynPOV}

One may regard the above from the [[nPOV]] as a special case of the way cocycles in the general notion of [[cohomology]] classify their [[homotopy fibers]]. More on this is at

* [[group cohomology]]

* [[nonabelian group cohomology]].

## Examples

By the above classification theorems, all the examples at _[[group cohomology]]_ equivalently induce examples for group extensions. And indeed by definition every [[short exact sequence]] defines an extension.

But examples of fundamental importance include for instance

* the [[real numbers]] as an extension of the [[circle group]]

  $$
    \mathbb{Z} \to \mathbb{R} \to U(1)
    \,.
  $$

* the [[spin group]] as an extension of the [[special orthogonal group]]

  $$  
    \mathbb{Z}_2 \to Spin \to SO
  $$

* etc.


* [[universal central extension]]

## Related concepts

* [[group cohomology]]

  * [[Galois cohomology]]

  * [[nonabelian group cohomology]], [[groupoid cohomology]]

* **group extension**, [[∞-group extension]]

   [[Ext-group]], [[central extension]], [[maximal central extension]]

  * [[Baer sum]]

  * [[solvable group]], [[nilpotent group]]

  * [[ring extension]]

* [[Lie group cohomology]] 

  * [[∞-Lie groupoid cohomology]]

* [[central extension of groupoids]]

* [[Lie algebra extension]]

* [[central charge]]



## References

### General


* [[Samuel Eilenberg]], [[Saunders MacLane]], Cohomology theory in abstract groups. II. Group extensions with a non-Abelian kernel.  Ann. of Math. (2)  48,  (1947). 326--341 [jstor](http://www.jstor.org/pss/1969174)

* [[Saunders MacLane]], Cohomology theory in abstract groups. III. Operator 
homomorphisms of kernels.  Ann. of Math. (2)  50,  (1949). 736--761. 

* [[Lawrence Breen]], Th&#233;orie de Schreier sup&#233;rieure, Ann. Sci. &#201;cole Norm. Sup. (4) 25 (1992), no. 5, 465--514 [numdam](http://www.numdam.org/item?id=ASENS_1992_4_25_5_465_0). 


Textbooks include

* A. G. Kurosh, Theory of groups 

* [[Kenneth Brown]], _Cohomology of groups_, Graduate Texts in Mathematics, __87__, Springer-Verlag, New York-Berlin, 1982. 


Lecture notes and similar include

* [[Brian Conrad]], _Group cohomology and group extensions_ ([pdf](http://math.stanford.edu/~conrad/249BPage/handouts/gpext.pdf))

* [[Terry Tao]], _Some notes on group extensions_ ([blog](http://terrytao.wordpress.com/2010/01/23/some-notes-on-group-extensions/))

* [[Patrick Morandi]], _Group extensions and $H^3$_ ([pdf](http://sierra.nmsu.edu/morandi/notes/GroupExtensions.pdf))

  _Nobabelian cohomology_ ([pdf](http://sierra.nmsu.edu/morandi/notes/nonabeliancohomology.pdf))

* Raphael Ho, _Classifications of group extensions and $H^2$_ ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Ho.pdf))

See also:

* [[R. Brown]], [[T. Porter]], _On the Schreier theory of non-abelian extensions: generalisations and computations_, Proc. Roy. Irish Acad. Sect. A, 96 (1996), 213 &#8211; 227.

* [[Manuel Bullejos]], [[Antonio M. Cegarra]],  A 3-dimensional non-abelian cohomology of groups with applications to homotopy classification of continuous maps Canad. J. Math., vol. 43, (2), 1991, 1-32.

* [[Antonio M. Cegarra]], [[Antonio R. Garzón]], A long exact sequence in non-abelian cohomology, Proc. Int. Conf. Como 1990., Lec. Notes in Math. 1488, Springer 1991.

A theory for central 2-group extensions is here:

* [[Antonio R. Garzón]] and E.M. Vitale, On the second cohomology categorical group and a Hochschild-Serre 2-exact sequence, Theory and Applications of Categories, Vol. 30 (2015), 933-984.  ([pdf](http://www.tac.mta.ca/tac/volumes/30/27/30-27.pdf))


See also references to Dedecker listed [[zoranskoda:Paul Dedecker|here]]. 

### Applications

A bit of discussion of some occurences of central extensions of groups in [[physics]] is in 

* G. Tuynman and W. Wiegerinck, _Central extensions of physics_ ([pdf](http://math.univ-lille1.fr/~gmt/PaperFolder/CentralExtensions.pdf))

(In fact there are many more than mentioned in that introduction.)

Extensions of [[supergroups]] are discussed in 

* {#Drupieski14} [[Christopher Drupieski]], _Strict polynomial superfunctors and universal extension classes for algebraic supergroups_ ([arXiv:1408.5764](http://arxiv.org/abs/1408.5764))


[[!redirects Schreier's theory]]
[[!redirects Schreier theory]]

[[!redirects extension of groups]]
[[!redirects extensions of groups]]

[[!redirects central extension of groups]]
[[!redirects central extensions of groups]]

[[!redirects group extension]]
[[!redirects group extensions]]

[[!redirects abelian group extension]]
[[!redirects abelian group extensions]]
