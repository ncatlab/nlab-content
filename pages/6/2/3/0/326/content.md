
<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Defintion

For $C$ a [[locally small category]], its **hom-functor** is the [[functor]]

$$ 
  hom : C^{op} \times C \to Set
$$

from the [[product category]] of the category $C$ with its [[opposite category]] to the category [[Set]] of [[set]]s, which sends

* an [[object]] $(c, c') \in C^{op} \times C$, i.e. a pair of objects in $C$, to the [[hom-set]] $Hom_C(c,c')$ in $C$, the set of [[morphism]]s $q : c \to c'$ in $C$;

* a morphism $(c,c') \stackrel{}{\to} (d,d')$, i.e. a pair of morphisms


  $$
    \array{
      c & c'
      \\
      \uparrow^{\mathrlap{f}} & \downarrow^{\mathrlap{g}}
      \\
      d & d'
    }
  $$

  in $C$ to the [[function]] $Hom_C(c,c') \to Hom_C(d,d')$ that sends 

  $$
    (q : c \stackrel{}{\to} c')
    \;\;\;
    \mapsto
    \;\;\,
    \left(
    g \circ q \circ f \; : \;
    \array{
       c &\stackrel{q}{\to}& c'
       \\
       \uparrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}}
       \\
       d && d'
    }
    \right)
    \,.
  $$

More generally, for $V$ a [[closed monoidal category|closed]] [[symmetric monoidal category]] and $C$ a $V$-[[enriched category]], its hom-functor is the functor

$$
  C(-,-) : C^{op} \times C \to V
$$

that sends objects $c,c' \in C$ to the [[hom-object]] $C(c,c') \in V$.

Some categories $C$ are equipped with an operation that behaves like a hom-functor, but takes values in $C$ itself

$$
  [-,-] : C^{op} \times C \to C
  \,.
$$

Such an operation is called an [[internal hom]] functor, and categories carrying this are called [[closed categories]].

## Properties

### Representable functors

For any object $c \in C$ one obtains a hom-functor

$$
  hom(c,-) : C \to Set
$$

and a hom-functor

$$
  hom(-,c) : C^{op} \to Set
$$

by fixing one of the arguments of $hom : C^{op} \times C \to Set$ to be $c$. Formally this is

$$
  hom(c,-) : C \stackrel{\simeq}{\to} * \times C  \stackrel{(c,Id)}{\to} C^{op} \times C \stackrel{hom(-,-)}{\to} Set
$$

and

$$
  hom(-,c) : C \stackrel{\simeq}{\to} C^{op} \times *  \stackrel{(Id,c)}{\to} C^{op} \times C \stackrel{hom(-,-)}{\to} Set
  \,.
$$

Functors of the form $C^{op} \to Set$ are called [[presheaves]] on $C$, and functors equivalent to $hom(-,c)$ are called [[representable functor]]s or **representable presheaves** on $C$.

Functors of the form $C \to Set$ are called [[copresheaves]] on $C$, and functors equivalent to $hom(c,-)$ are called co[[representable functor]]s or **representable copresheaves** on $C$.


### Preservation of limits

The hom-functor preserves all [[limit]]s in both arguments separately. This means:

* for fixed object $c \in C$ the functor $hom(c,-) : C \to C$ sends limit [[diagram]]s in $C$ to limit diagrams in $C$;

* for fixed object $c' \in C$ the functor $hom(-,c') : C^{op} \to C$ sends limit diagrams in $C^{op}$ -- which are [[colimit]] [[diagram]]s in $C$! -- to limit diagrams in $C$. 

For instance for 

$$
  \array{
     y \times_x z &\to& y
     \\
     \downarrow && \downarrow
     \\
     z &\to& x
  }
$$

a [[pullback]] [[diagram]] in $C$ and for $c \in C$ any object, the induced diagram

$$
  \array{
     Hom_C(c,y) \times_{Hom_C(c,x)} Hom_C(c,z)\simeq & Hom_C(c,y \times_x z)  &\to& Hom_C(c,y)
     \\
     & \downarrow && \downarrow
     \\
     & Hom_C(c,z) &\to& Hom_C(c,x)
  }
$$

in [[Set]] is again a pullback diagram. A moment of reflection shows that this statement is _equivalent_ to the very definition of limit.


## Examples

...

[[!redirects hom-functors]]

[[!redirects hom functor]]
[[!redirects hom functors]]
