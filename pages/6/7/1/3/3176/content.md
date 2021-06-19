
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _logical morphism_ or _logical functor_ is a [[homomorphism]] between [[elementary topos]]es that preserves the structure of a topos as a context for [[logic]]: a functor which preserves all the elementary topos structure, including in particular [[power objects]], but not necessarily any infinitary structure (such as present additionally in a [[sheaf topos]]).  

If instead a topos is regarded as a context for [[geometry]] or specifically [[geometric logic]], then the notion of [[homomorphism]] preserving this is that of a  _[[geometric morphism]]_. 

## Definition

Since all the elementary topos structure follows from having [[finite limits]] and [[power objects]], it suffices to define a logical functor to preserve these, up to [[isomorphism]].  It then follows that it is also a [[locally cartesian closed functor]], a [[Heyting functor]], etc.

+-- {: .num_defn}
###### Definition

Let $\mathcal{E}$ be an [[elementary topos]]. Write $\Omega \in \mathcal{E}$ for the [[subobject classifier]]. For each [[object]] $A \in \mathcal{E}$ write

$$
  P A \coloneqq \Omega^A
$$

for the [[exponential object]]. Write

$$
  \in_A \hookrightarrow P A \times A
$$

for the [[subobject]] classified by the [[evaluation map]] $ev : P A \times A \to \Omega$. 

=--

This exhibits $P A$ as a [[power object]] for $A$. 

+-- {: .num_defn}
###### Definition

A [[functor]] $F : \mathcal{E} \to \mathcal{F}$ between [[elementary toposes]] is called a **logical morphism** if 

1. $F$ preserves finite [[limits]];

1. for every object $A \in \mathcal{E}$ 

   * the canonical morphism

     $$
       \phi_A : F(P A) \to P (F A)
     $$

     is an [[isomorphism]]; this is the [[name of the relation]]

     $$
       F(\in_A) \hookrightarrow F(P A \times A) \simeq F(P A) \times F A
     $$

     (using that [[cartesian functor]]s preserve both [[product]]s as well as [[monomorphism]])

   * equivalently: $F(P A)$ equipped with the [[relation]] $F(\in_A)$ is a [[power object]] for $F(A)$ in $\mathcal{F}$.

=--

The notion of logical functors between [[topos]]es is in contrast to [[geometric morphism]]s between toposes: the former preserve the structure of an [[elementary topos]], the latter those of a [[sheaf topos]].

But both can be combined:

+-- {: .num_defn #AtomicGeometricMorphism}
###### Definition

A [[geometric morphism]] whose [[inverse image]] is a logical functor 
is called an [[atomic geometric morphism]]. 

=--

+-- {: .num_remark}
###### Remark

The other case, that the [[direct image]] of a geometric morphism is a logical functor is not of interest. See cor. \ref{LogicalMorphismsAsDirectImages} below.

=--


## Properties

### General

+-- {: .num_prop #LeftRightAdjoint}
###### Proposition

A logical functor has a [[left adjoint]] precisely if it has a [[right adjoint]].

=--

This appears as ([Johnstone, cor. A2.2.10](#Johnstone)).

+-- {: .proof}
###### Proof

For $F : \mathcal{E} \to \mathcal{F}$ a logical functor, we have by definition a [[diagram]]

$$
  \array{
     \mathcal{E}^{op} &\stackrel{F^{op}}{\to}& \mathcal{F}^{op}
     \\
     {}^{\mathllap{P}}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{P}}
     \\
     \mathcal{E} &\stackrel{F}{\to}& \mathcal{F}
  }
$$

in [[Cat]]. This satisfies the assumptions of the [[adjoint lifting theorem]] and hence $F$ has a right adjoint precisely if $F^{op}$ does. But a right adjoint of $F^{op}$ is a left adjoint of $F$, and vice versa.

=--

+-- {: .num_prop #PresMono}
###### Proposition
If a logical functor $F : \mathcal{E} \to \mathcal{F}$ has a left adjoint $L$, then $L$ preserves [[monomorphisms]], and indeed induces a bijection between subobjects of $A\in \mathcal{F}$ and subobjects of $L A\in \mathcal{E}$.
=--
+-- {: .proof}
###### Proof
Since $F(\Omega_{\mathcal{E}}) = \Omega_{\mathcal{F}}$, we have a bijection
$$ Sub_{\mathcal{F}}(A) \cong \mathcal{F}(A,\Omega_{\mathcal{F}}) \cong \mathcal{E}(L A,\Omega_{\mathcal{E}}) \cong Sub_{\mathcal{E}}(L A).$$
It remains to check that this bijection is implemented by the action of $L$, which can be done with [[partial map classifiers]]; see ([Johnstone, Lemma A2.4.8](#Johnstone)).
=--

+-- {: .num_prop #CharPullback}
###### Proposition
For a logical functor $F : \mathcal{E} \to \mathcal{F}$ having a left adjoint $L$, the following are equivalent:

1. The induced functor $L':\mathcal{F} \to \mathcal{E}/L 1$ is an [[equivalence of categories]], i.e. the adjunction $L\dashv F$ can be identified with the pullback adjunction $\mathcal{E}/B \rightleftarrows \mathcal{E}$ for some $B$ (namely $L1$).
1. $L$ is [[conservative functor|conservative]].
1. $L$ is [[faithful functor|faithful]].
1. $L$ preserves [[equalizers]].
1. $L$ preserves [[pullbacks]].
=--
This appears as ([Johnstone, Prop. A2.3.8](#Johnstone)).
+-- {: .proof}
###### Proof
The left adjoint of pullback has all the other properties.  Any pullback-preserving functor preserves equalizers.  An equalizer-preserving functor is faithful as soon as it reflects invertibility of monomorphisms, which follows from Proposition \ref{PresMono} above.  A faithful functor reflects monos and epis, hence is conservative once its domain is [[balanced category|balanced]].  

Finally, if $L$ is conservative then so is $L'$, and its right adjoint $F'$ (given by $F$ followed by pullback along $\eta : 1 \to F L 1$) is also logical, hence cartesian closed.  Thus, $L'\dashv F'$ is a [[Hopf adjunction]] for the cartesian monoidal structures, and $L'$ preserves the terminal object.  Now the counit of $L'\dashv F'$ can be factored as
$$ L' F' A \cong L'(1\times F' A) \xrightarrow{\cong} L' 1 \times A \cong 1\times A\cong A $$
so it is an isomorphism.  By the triangle identity, $L'(\eta)$ is an isomorphism, but $L'$ is conservative, hence the unit $\eta$ is also an isomorphism, and $L'\dashv F'$ is an equivalence.
=--

This appears as ([Johnstone, cor. A2.2.10](#Johnstone)).

+-- {: .num_cor #LogicalMorphismsRightAdjointToCartesianFunctors}
###### Corollary
If a logical functor is [[right adjoint]] to a [[left exact functor]], then it is an [[equivalence of categories]].
=--

This appears as ([Johnstone, scholium 2.3.9](#Johnstone)).



### Preserved structures

In particular, a logical functor preserves the truth of all sentences in the [[internal logic]].  If it is moreover [[conservative functor|conservative]], then it also *reflects* the truth of such sentences.  For example, the [[transfer principle]] of [[nonstandard analysis]] can be stated as the fact that a certain functor is logical and conservative.

### Relation to geometric morphisms

The difference between geometric and logical functors between toposes is, in a certain sense, a [[categorification]] of the difference between a [[homomorphism]] of [[frames]] and a homomorphism of [[Heyting algebras]].  When the latter are [[complete lattice|complete]], these are the same objects with the same [[isomorphisms]] but different morphisms.  

However, while frame homomorphisms naturally categorified by geometric functors, a more precise categorification of Heyting algebra homomorphisms would be [[Heyting functors]], which preserve the internal first-order logic, but not the higher-order logic as logical functors do.

+-- {: .num_prop #LogicalMorphismsAsDirectImages}
###### Proposition

A logical functor is the [[direct image]] of a [[geometric morphism]] precisely if it is an [[equivalence of categories|equivalence]].

=--

+-- {: .proof}
###### Proof

Since by definition the direct image of a geometric morphism has a [[left adjoint]] that preserves [[finite limits]].

=--

But logical inverse images are of interest. Recall from def. \ref{AtomicGeometricMorphism} above that a [[geometric morphism]] with logical inverse image is called an [[atomic geometric morphism]].

+-- {: .num_cor}
###### Corollary

Every [[atomic geometric morphism]] is an [[essential geometric morphism]].

=--

+-- {: .proof}
###### Proof

By prop. \ref{LeftRightAdjoint}.

=--

The following is the main source of examples of atomic geometric morphisms.

+-- {: .num_prop}
###### Proposition

The [[inverse image]] of any [[base change geometric morphism]], hence in particular of any [[etale geometric morphism]], is a [[logical morphism]].

=--

+-- {: .proof}
###### Proof

The inverse image is given by [[pullback]] along the given morphism.

=--

+-- {: .num_prop}
###### Remark

When considering the [[internal logic]] of a given [[topos]] $\mathcal{E}$ relations, [[predicate]]s/[[proposition]]s about [[variable]]s of [[type]] $A \in ob \mathcal{E}$ are [[subobject]]s of $A$. Application of function symbols to such expressions corresponds to pullback along the morphism representing the function symbol. The above says that this is, indeed, a _logical operation_.

=--

## Examples


* The inclusion [[FinSet]] $\hookrightarrow$ [[Set]] is logical.

* More generally, for any [[small category]] $C$ the inclusion

  $$
    [C^{op}, FinSet] \hookrightarrow [C^{op}, Set]
  $$

  into the [[presheaf topos]] is logical.

* For $G$ a [[group]] and $\mathbf{B}G$ its [[delooping]] [[groupoid]], the [[forgetful functor]]

  $$
    [\mathbf{B}G, Set] \to Set
  $$

  from [[permutation representation]]s to [[Set]] is logical.

## References

Section A2.1 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

Section IV.2, page 170 of


* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 {#MacLaneMoerdijk}

[[!redirects logical functor]]
[[!redirects logical functors]]
[[!redirects logical morphism]]
[[!redirects logical morphisms]]
