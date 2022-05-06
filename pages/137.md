+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[category theory]] concept of _epimorphism_ is a generalization or strengthening of the concept of _[[surjective functions]]_ between [[sets]] (example \ref{EpimorphismsOfSets} below).

The [[formal duality|formally dual concept]] is that of _[[monomorphism]]_, similarly related to the concept of [[injective function]].

Common jargon includes "is a mono" or "is monic" for "is a monomorphism", and "is an epi" or "is epic" for "is an epimorphism", and "is an iso" for "is an isomorphism".


## Definition

A [[morphism]]  $f \colon X \to Y$ in some [[category]] is called an _epimorphism_ (sometimes abbrieviated to _epi_, or described as being _epic_), if for every other [[object]] $Z$ and every [[pair of parallel morphisms]] $g_1,g_2 \colon Y \to Z$ then 

$$
  \left(
    g_1\circ f
    \,=\,
    g_2 \circ f
  \right)
  \;\Rightarrow\;
  \left(
    g_1 = g_2
  \right)
  \,.
$$

Stated more abstractly, this says that $f$ is an epimorphism precisely if for every object $Z$ the [[hom-functor]] $Hom(-,Z)$ sends it to an [[injective function]] 

$$
  Hom(Y,Z) 
   \stackrel{f^*}{\hookrightarrow} 
  Hom(X,Z)
$$

between [[hom-sets]]. Since injective functions are the [[monomorphisms]] in [[Set]] (example \ref{EpimorphismsOfSets} below) this means that $f$ is an epimorphism precisely if $Hom(f,Z)$ is a monomorphism for all $Z$.

Finally, this means that $f$ is an epimorphism in a [[category]] $\mathcal{C}$ precisely if it is a [[monomorphism]] in the [[opposite category]] $\mathcal{C}^{op}$.

## Examples

+-- {: .num_example #EpimorphismsOfSets}
###### Example
**(epimorphisms of sets)**

The epimorphisms in the category [[Set]] of [[sets]] are precisely the [[surjective functions]]. 

=--

Thus the concept of epimorphism may be thought of as a category-theoretic generalization of the concept of surjection.  

But beware that in categories of sets with [[extra structure]], epimorphisms need not be surjective (in contrast to [[monomorphisms]], which are usually [[injective]]).  

+-- {: .num_example #EpimorphismsOfRings}
###### Example
**(epimorphisms of rings)**

In the categories [[Ring]] or [[CRing]] of ([[commutative ring|commutative]]) [[rings]] and [[ring homomorphisms]] between them, then every surjective ring homomorphisms is an epimorphism, but not every epimorphism is surjective. 

A counterexample is the defining inclusion $\mathbb{Z} \hookrightarrow \mathbb{Q}$ of the ring of [[integers]] into the ring of [[rational numbers]]. This is an injective epimorphism of rings.

For more see for instance at [[Stacks Project]], _[10.106 Epimorphisms of rings](http://stacks.math.columbia.edu/tag/04VM)_.

=--

Often, though, the surjections correspond to a stronger notion of epimorphism.

+-- {: .num_example}
###### Example

Every [[isomorphism]] is both an epimorphism and a [[monomorphism]].

=--

But beware that the converse fails:

+-- {: .num_example}
###### Example

A morphism that is both an epimorphism and a [[monomorphism]] need not be an [[isomorphism]].

For instance in the categories [[Ring]] or [[CRing]] as in example \ref{EpimorphismsOfRings}, then the defining inclusion $\mathbb{Z} \hookrightarrow \mathbb{Q}$ of the ring of [[integers]] into that of [[rational numbers]] is both a monomorphism and an epimorphism, but clearly not an isomorphism.

=--


## Properties

+-- {: .num_prop}
###### Proposition

The following are equivalent:

* $f : x \to y$ is an epimorphism in $C$;

* $f$ is a [[monomorphism]] in the [[opposite category]] $C^{op}$;

* postcomposition with $f$ is a monomorphism in [[Set]]: that is, for all $c \in C$, $f \circ - : Hom(c,x) \to Hom(c,y)$ is an [[injection]];

* the [[commuting diagram]] 
  $$
    \array{
      x &\stackrel{f}{\to}& y
      \\
      {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Id}}
     \\
     y &\underset{Id}{\to}& y
    }
  $$

  is a [[pushout]] diagram.

=--

+-- {: .num_prop}
###### Proposition

If $f \colon x \to y$ and $g \colon y \to z$ are epimorphisms, so is their composite $g f$.  If $g f$ is an epimorphism, so is $g$.

=--


+-- {: .num_prop}
###### Proposition

Every [[coequalizer]] $x \to y$

$$
  z \stackrel{\to}{\to} x \to y
$$

is an epimorphism.

=--

The converse of the above proposition fails, and an epimorphism is called a [[regular epimorphism]] if it is the coequalizer of some pair of morphisms.


+-- {: .num_prop}
###### Proposition

Epimorphisms are preserved by [[pushout]]: if $f : x \to y$ is an epimorphism and

$$
  \array{
    x &\to& a
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{g}
    \\
    y &\to& b
  }
$$

is a [[pushout]] diagram, then also $g$ is an epimorphism.

=--

+-- {: .proof}
###### Proof

Let $h_1,h_2 : b \to c$ be two morphisms such that $\stackrel{g}{\to} \stackrel{h_1}{\to} = \stackrel{g}{\to} \stackrel{h_2}{\to} $. Then by the commutativity of the diagram also $x \to y \to b \stackrel{h_1}{\to} c$ equals $x \to y \to b \stackrel{h_2}{\to} c$. Since $x \to y$ is assumed to be epi, it follows that $y \to b \stackrel{h_1}{\to} c$ equals $y \to b \stackrel{h_2}{\to} c$. But this means that $h_1$ and $h_2$ define the same [[cocone]]. By the universality of the pushout $b$ there is a unique map of cocones from $b$ to $c$. Hence $h_1$ must equal $h_2$. Therefore $g$ is epi. 

=---

+-- {: .num_prop}
###### Proposition

Epimorphisms are preserved by any [[left adjoint]] [[functor]], or more generally any functor that preserves [[pushouts]]: if $F : C \to D$ is a [[functor]] that preserves pushouts and $f \in Mor(C)$ an epimorphism then $F(f) \in Mor(D)$ is an epimorphism.

=--

+-- {: .proof}
###### Proof

If $F : C \to D$ is a left adjoint we can argue this way: by the [[adjunction]] [[natural isomorphism]] we have for all $d \in Obj(D)$

$$
  Hom_D(L(f),d) \simeq Hom_C(f,R(d))
  \,.
$$

The right hand is a monomorphism by assumption, hence so is the left hand, hence $L(f)$ is epi.

More generally, if $F$ preserves pushouts we can use the fact that $f$ is epic iff

$$
    \array{
      x &\stackrel{f}{\to}& y
      \\
      {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Id}}
     \\
     y &\underset{Id}{\to}& y
    }
  $$

is a [[pushout]] diagram.

=--

+-- {: .num_prop #EpimorphismsAreReflectedByFaithfulFunctors}
###### Proposition

Epimorphisms are [[reflected limit|reflected]] by [[faithful functors]].

=--

+-- {: .proof}
###### Proof

Let $F \colon \mathcal{C}\longrightarrow \mathcal{D}$ be a [[faithful functor]]. Consider $f \colon x \longrightarrow y$ a [[morphism]] in $\mathcal{C}$ such that $F(f) \colon F(x)\longrightarrow F(y)$ is an epimorphism in $\mathcal{D}$. We need to show that then $f$ itself is an epimorphism.

So consider morphisms $g,h \colon y \longrightarrow z$ such that $g \circ f = h \circ f$. We need to show that this implies that already $g = h$ (injectivity of $Hom(f,z)$). But functoriality implies that $F(g)\circ F(f) = F(h) \circ F(f)$, and since $F(f)$ is epic this implies that $F(g) = F(h)$. Now the statement follows with the assumption that $F$ is faithful, hence [[injection|injective]] on morphisms.

=--

Epimorphisms get along with colimits in a number of ways, some of which we have seen above.   Here is another:

+-- {: .num_prop}
###### Proposition

Any morphism from an initial object is an epimorphism.  The coproduct of epimorphisms is an epimorphism.
=--

+-- {: .proof}
###### Proof

For the first suppose $0 \in C$ is initial and $f : x \to 0$.  Given morphisms $g,h: 0 \to y$ with $g \circ f = h \circ f$ we have $g = h$ simply because $0$ is initial.  

For the second suppose $f_1 : x_1 \to y_1$ and $f_2 : x_2 \to y_2$ are epimorphisms; we wish to show that $f_1 + f_2 : x_1+x_2 \to y_1 + y_2$ is an epimorphism.   Suppose we have morphisms $g, h: y_1+y_2 \to z$ with $g \circ (f_1+f_2) = h \circ (f_1 + f_2)$.   Then $g \circ i_1 \circ f_1 = h \circ i_1 \circ f_1$ where $i_1 : x_1 \to x_1 + x_2$ is the canonical map into the coproduct.  Since $f_1$ is epic we conclude $g \circ i_1 = h \circ i_1$.  Similarly we have $g \circ i_2 = h \circ i_2$.  If follows that $g = h$.  
=--

Epimorphisms do not get along quite as well with limits.  For example, the unique morphism to the terminal object is not always an epimorphism (though this is true in $Set$), and the projections from a product onto its factors, e.g. $p_1 : x_1 \times x_2 \to x_1$, are not always epimorphisms (even in $Set$: take $x_2$ to be empty).


## Variations {#Variations}

There are a sequence of variations on the concept of epimorphism, which conveniently arrange themselves in a [[total order]].  In order from strongest to weakest, we have:

* [[split epimorphism]] = morphism having a [[section]]
* [[effective descent morphism]]
* [[descent morphism]] = [[pullback-stability|stable]] [[regular epimorphism]]
* [[effective epimorphism]] = [[coequalizer]] of its [[kernel pair]]
* [[regular epimorphism]] = [[coequalizer]] of some [[parallel pair]] of morphisms
* [[strict epimorphism]] = joint coequalizer of all pairs which it coequalizes
* [[strong epimorphism]] = an epimorphism [[orthogonality|right orthogonal]] to [[monomorphisms]]
* [[extremal epimorphism]] = an epimorphism not factoring through any nontrivial monomorphism.
* epimorphism.

In [[Set|the category of sets]], every epimorphism is effective descent (and even split if you believe the [[axiom of choice]]).  Thus, it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.  The following discussion may be helpful in this regard.

First we note:

* Descent and effective descent morphisms are only defined in a category with [[pullbacks]].  The other notions can be defined in any category, although of course for an effective epimorphism one must in general assert the existence of the kernel pair.

Moreover, if the category has finite [[limits]], then the picture becomes much simpler:

* If a strict epimorphism has a kernel pair, then it is effective and hence also regular.  Thus, in a category with pullbacks, effective = regular = strict.  Probably for this reason, there is substantial variation among authors in their use of these words; some use "effective epi" or "regular epi" to mean what we have called a "strict epi".

* Likewise, in a category with pullbacks, every extremal epimorphism is strong, since monomorphisms are always pullback-stable.

* Moreover, in a category with [[equalizers]], strong and extremal epimorphisms do not need to explicitly be asserted to be epic; that follows from the other condition in their definition.

Also worth noting are:

* In a [[regular category]], every extremal epimorphism is a descent morphism (i.e. a pullback-stable regular epimorphism).  Thus in this case there remain only four types of epimorphism: split, effective descent, regular, and plain.

* In an [[exact category]], or a category that has pullback-stable [[reflexive coequalizers]] (which implies that it is regular), any regular epimorphism is effective descent.  Thus in this case we have only three types: split, regular, and plain.

* In a [[pretopos]] (hence also in a [[topos]]), every epimorphism is regular, leaving only two types: split and plain.  The collapsing of these two types into one is called the [[axiom of choice]] for that category.

Thus, in general, the two serious distinctions come

* Between split epimorphisms and regular ones: in very few categories are all regular epimorphisms split.  Splitting of even regular epimorphisms is a form of the axiom of choice, which may be valid in [[Set]] (if you believe it) but very often fails [[internalization|internally]].

* Between extremal epimorphisms and "plain" epimorphisms: in many categories, the plain epimorphisms are oddly behaved, but the extremal ones are what we would expect.  For instance, the inclusion $\mathbb{Z}\hookrightarrow\mathbb{Q}$ is an epimorphism of [[ring]]s, but the extremal epimorphisms of rings are just the surjective ring homomorphisms.  More generally, in all [[algebraic category|algebraic categories]] (categories of algebra for a [[Lawvere theory]]), which are regular, the regular epimorphisms are the morphisms whose underlying function is surjective.

Moreover, even in non-regular categories, there seems to be a strong tendency for strong/extremal epimorphisms to coincide with regular/strict ones.  For example, this is the case in [[Top]], where both are the class of quotient maps.  (The plain epimorphisms are the surjective continuous functions.)

However, the distinction is real.  For instance, in the category generated by the following graph:
$$
\array{ &&&& C\\
  &&& ^f\nearrow\\
  A& \underoverset{h}{k}{\rightrightarrows} & B \\
  &&& _g\searrow\\
  &&&& D}
$$
subject to the equations $f h = f k$ and $g h = g k$, both $f$ and $g$ are strong, but not strict, epimorphisms.

## Related concepts

* [[monomorphism]]

* [[image]], [[coimage]]

* [[n-epimorphism]]

[[!redirects epimorphisms]]
[[!redirects epic]]
[[!redirects epics]]
[[!redirects epi]]
[[!redirects epis]]
[[!redirects Epimorphism]]
[[!redirects Epimorphisms]]
[[!redirects Epic]]
[[!redirects Epics]]
[[!redirects Epi]]
[[!redirects Epis]]
