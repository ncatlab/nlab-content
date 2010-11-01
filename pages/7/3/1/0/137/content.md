#Contents#
* automatic table of contents goes here
{:toc}

## Definition

An **epimorphism** in a [[category]] $C$ is a [[morphism]] 
$f : X \to Y$ 
such that every contravariant [[hom-functor]] $Hom(-,Z)$ sends it to an [[injection]]
$$
  \forall Z \in C : \;
  Hom(Y,Z) \stackrel{f^*}{\hookrightarrow} 
  Hom(X,Z)
  \,.
$$

In more elementary terms, $f: X \to Y$ is an epimorphism if, given any $g, h: Y \to Z$, such that the composites $\stackrel{f}{\to} \stackrel{g}{\to} = \stackrel{f}{\to} \stackrel{h}{\to}$ are equal, then already $g = h$:
$$
\left(\array{
  &              & Y \\
  & \nearrow_{f} &   & \searrow^{g} \\
X &              &   &              & Z \\
  & \searrow^{f} &   & \nearrow_{h} \\
  &              & Y \\
} 
\right)
\quad\quad \Rightarrow \quad\quad 
\left(\array{
X & \rightarrow^{f} & Y & \rightrightarrows^g_h & Z \\
}\right)$$

## Examples

The epimorphisms in [[Set]] are the [[surjection|surjective]] functions; thus epimorphisms can be thought of as a categorical notion of surjection.  However, this is frequently not quite right: in categories of sets with [[stuff, structure, property|extra structure]], epimorphisms need not be surjective (unlike the case for [[monomorphism]]s, which are usually injective).  Often, though, the surjections correspond to a stronger notion of epimorphism.

## Properties

+-- {: .un_prop}
###### Proposition

The following are equivalent

* $f : x \to y$ is an epimorphism in $C$;

* $f$ is a [[monomorphism]] in the [[opposite category]] $C^{op}$;

* for all $d$, $Hom(f,d)$ is a [[monomorphism]] in [[Set]] -- an [[injection]];

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

+-- {: .un_prop}
###### Proposition

Every [[coequalizer]]

$$
  z \stackrel{\to}{\to} x \to y
$$

is an epimorphism.

=--


+-- {: .un_prop}
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

+-- {: .un_prop}
###### Proposition

Epimorphisms are preserved by [[left adjoint]] [[functor]]s:

if $F : C \to D$ is a [[functor]] which is [[left adjoint]] then for $f \in Mor(C)$ an epimorphism also $F(f) \in Mod(D)$ is an epimorphism

=--

+-- {: .proof}
###### Proof

One argument is this:

By the [[adjunction]] [[natural isomorphism]] we have for all $d \in Obj(D)$

$$
  Hom_D(L(f),d) \simeq Hom_C(f,R(d))
  \,.
$$

The right hand is a monomorphism by assumption, hence so is the left hand, hence $L(f)$ is epi.

Another argument is this: use that by the above $f$ is epi precisely if

$$
  \array{
    & \stackrel{f}{\to} &
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Id}}
    \\
    & \underset{Id}{\to} & 
  }
$$

is a [[pushout]] diagram and observe that left adjoint functors preserve pushouts (and of course [[identity|identities]]).

=--

## Variations 

There are a sequence of variations on the concept of epimorphism, from strongest to weakest:


[[split epimorphism]] $\Rightarrow$
[[regular epimorphism]] $\Rightarrow$ 
[[strict epimorphism]]$\Rightarrow$
[[strong epimorphism]]$\Rightarrow$ 
[[extremal epimorphism]]$\Rightarrow$
epimorphism.

In [[Set|the category of sets]], every epimorphism is regular (and even split if you believe the [[axiom of choice]]), so it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.

In general, the two serious distinctions come

* Between split epimorphisms and regular ones: in very few categories are all regular epimorphisms split.  Splitting of even regular epimorphisms is a form of the axiom of choice, which may be valid  in [[Set]] (if you believe it) but very often fails [[internalization|internally]].

* Between extremal epimorphisms and "plain" epimorphisms: in many categories, the plain epimorphisms are oddly behaved, but the extremal ones are what we would expect.  For instance, the inclusion $\mathbb{Z}\hookrightarrow\mathbb{Q}$ is an epimorphism of [[ring]]s, but the extremal epimorphisms of rings are just the surjective ring homomorphisms.

The remaining distinctions frequently collapse.  For instance:

* In a category with [[pullback]]s, any strict epimorphism is regular, and any extremal epimorphism is strong.

* In a [[regular category]], every extremal epimorphism is regular, so the sequence reduces to three: split, regular = strict = strong = extremal, plain.  In [[algebraic category|algebraic categories]] (categories of algebra for a [[Lawvere theory]]), which are regular, the regular/strict/strong/extremal epimorphisms are the morphisms whose underlying function is surjective.

* In a [[pretopos]] (hence also in a [[topos]]), every epimorphism is regular, so the only distinction remaining is split versus non-split.

Moreover, even in non-regular categories, there seems to be a strong tendency for strong/extremal epimorphisms to coincide with regular/strict ones.  For example, this is the case in [[Top]].  However, the distinction is real; for instance, in the category generated by the following graph:
$$
\array{ &&&& C\\
  &&& ^f\nearrow\\
  A& \underoverset{h}{k}{\rightrightarrows} & B \\
  &&& _g\searrow\\
  &&&& D}
$$
subject to the equations $f h = f k$ and $g h = g k$, both $f$ and $g$ are strong, but not strict, epimorphisms.


[[!redirects epimorphisms]]
[[!redirects epic]]
[[!redirects epics]]
