+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

* **coimage**

* [[image]]

***

# Coimages
* table of contents
{: toc}

## Idea

The _coimage_ of a morphism is the notion [[duality|dual]] to its [[image]]. 

Under certain conditions coimages coincide with images and even if not, often the _coimage_ is what one wants to think of as the image. You cannot have an image or coimage without the other. For more of the general theory see [[image]].



## Definition

The **coimage** of a [[morphism]] $f : c \to d$ in a [[category]] $C$ is the [[image]] of the corresponding morphism in the [[opposite category]] $C^{op}$.


### In terms of colimits

If $C$ has finite [[limit]]s and [[colimit]]s, then the coimage of a morphism $f : c \to d$ is the [[coequalizer]] of its [[kernel pair]]:

$$
  coim f \simeq colim ( c \times_d c \stackrel{\to}{\to} c)
  \,,
$$

This is isomorphic to the [[pushout]] $c \sqcup_{c\times_d c} c$

$$
  coim f \simeq c \sqcup_{c\times_d c} c
  \,.
$$

So in

$$
  \array{
    c \times_d c &&\to&& c
    \\
     &&& \swarrow
    \\
    \downarrow^f && coim f && \downarrow^f
    \\
    & \nearrow && \searrow
    \\
    C && \stackrel{f}{\to} && d
  }
$$

the outer square is a [[pullback]] square while the inner is a [[pushout]].

Notice that being a coequalizer, the morphism

$$
  c \to coim f
$$

is an [[epimorphism]] and in fact a [[regular epimorphism]].


### In an $(\infty,1)$-category  {#InInfCat}

In an [[(∞,1)-category]] $C$ with [[(∞,1)-limit]]s and -colimits, the colimit-definition of coimages generalizes as follows:

for $f : c \to d$ a morphism in $C$, let

$$
  C(f) = 
  \left(
    \cdots \stackrel{\to}{\stackrel{\to}{\to}} c \times_d c \stackrel{\to}{\to} c
  \right)
$$

be the [[Cech nerve]] of $f$. This is the [[groupoid object in an (∞,1)-category]] that resolves the [[kernel pair]] [[equivalence relation]]: where $c \times_d \stackrel{\to}{\to} c$ is the relation that makes two [[generalized element]]s of $c$ _equal_ if their image in $d$ is equal,  the full Cech nerve is the internal [[∞-groupoid]] where there is just an equivalence between such two elements.

The Cech nerve is a [[simplicial object|simplicial]] [[diagram]]

$$
  C(f) : \Delta^{op} \to C
$$

The **coimage** of $f$ is the [[(∞,1)-colimit]] over this diagram

$$
  coim(f) := \lim_\leftarrow
    \left(
    \cdots \stackrel{\to}{\stackrel{\to}{\to}} c \times_d c \stackrel{\to}{\to} c
  \right)
$$

## Properties

* Morphisms for which image and coimage coincide (in a certain sense) are [[strict morphism]]s.



## Examples

### For $(\infty,1)$-coimages

Let $G$ be a [[group]]. In the [[(∞,1)-category]] $C =$ [[∞-Grpd]] we have $G$ as a 0-[[truncated]] [[∞-group]] object as well as its [[delooping]] $\mathbf{B}G$, which is the one-object [[groupoid]] with $G$ as its morphisms.

Then: the coimage of the point inclusion $f : * \to \mathbf{B}G$ is $\mathbf{B}G$ itself.

Because the homotopy-[[Cech nerve]] of the point inclusion is the usual simplicial incarnation of $G$

$$
  C(f) = \left(
    \cdots G \times G \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} *
  \right)
$$

now regarded as a simplicial object in [[∞Grpd]]. Its homotopy colimit is again $\mathbf{B}G$. This follows for instance abstractly from the fact that [[∞Grpd]] is an [[(∞,1)-topos]] and therefore satisfies [[Giraud's axioms]], which say that every [[groupoid object in an (∞,1)-category]] is _effective_ in an [[(∞,1)-topos]]. 


[[!redirects coimage]]
[[!redirects coimages]]
