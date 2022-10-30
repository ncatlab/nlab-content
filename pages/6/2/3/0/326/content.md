
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $C$ a [[locally small category]], its **hom-functor** is the [[functor]]

$$ 
  hom : C^{op} \times C \to Set
$$

from the [[product category]] of the category $C$ with its [[opposite category]] to the category [[Set]] of [[sets]], which sends

* an [[object]] $(c, c') \in C^{op} \times C$, i.e. a pair of objects in $C$, to the [[hom-set]] $Hom_C(c,c')$ in Set, the set of [[morphisms]] $q : c \to c'$ in $C$;

* a morphism $(c,c') \stackrel{}{\to} (d,d')$, i.e. a pair of morphisms


  $$
    \array{
      c & c'
      \\
      \downarrow^{\mathrlap{f^{op}}} & \downarrow^{\mathrlap{g}}
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

+-- {: .query} 
Note: when the symbol $\circ$ is used, it denotes traditional right-to-left order of composition. For those who prefer the left-to-right order, the symbol $;$ may be used in place of $\circ$. Further discussion of this should go to the nForum page [here](https://nforum.ncatlab.org/discussion/7239/realigned-arrows-for-clarification-and-fixed-composition-order/). 
=-- 

More generally, for $V$ a [[closed monoidal category|closed]] [[symmetric monoidal category]] and $C$ a $V$-[[enriched category]], its _[[enriched hom-functor]]_ is the [[enriched functor]]

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

### In homotopy type theory

Note: the [[HoTT book]] calls a [[category]] a "precategory" and a [[univalent category]] a "category", but here we shall refer to the standard terminology of "category" and "univalent category" respectively. 

For any [[category]] $A$, we have a hom-functor
$$hom_A : A^{op} \times A \to \mathit{Set}$$
It takes a pair $(a,b):(A^{op})_0 \times A_0 \equiv A_0\times A_0$ to the set $hom_A(a,b)$. For a morphism $(f,f') : hom_{A^{op} \times A}((a,b),(a',b'))$, by definition we have $f:hom_A(a',a)$ and $f': hom_A(b,b')$, so we can define

$$(hom_A)_{(a,b),(a',b')}(f,f') \equiv (g\mapsto f' g f) : hom_A(a,b) \to hom_A(a',b')$$

## Properties

### Representable functors

Given a hom-functor $hom:C^{op}\times C\to Set$, for any object $c \in C$ one obtains a functor

$$
  h^c: C \to Set
$$

given by $h^c\coloneqq hom(c,-)$ and a functor

$$
  h_c : C^{op} \to Set
$$

given by $h_c\coloneqq hom(-,c)$, i.e. by fixing one of the arguments of $hom: C^{op} \times C \to Set$ to be $c$. 

Formally this is

$$
  hom(c,-) : C \stackrel{\simeq}{\to} * \times C  \stackrel{(c,Id)}{\to} C^{op} \times C \stackrel{hom(-,-)}{\to} Set
$$

and

$$
  hom(-,c) : C \stackrel{\simeq}{\to} C^{op} \times *  \stackrel{(Id,c)}{\to} C^{op} \times C \stackrel{hom(-,-)}{\to} Set
  \,.
$$

Functors of the form $C^{op} \to Set$ are called [[presheaves]] on $C$, and functors [[natural isomorphism|naturally isomorphic]] to $hom(-,c)$ are called [[representable functors]] or **representable presheaves** on $C$.

Functors of the form $C \to Set$ are called [[copresheaves]] on $C$, and functors naturally isomorphic to $hom(c,-)$ are called co[[representable functors]] or **representable copresheaves** on $C$.


### Preservation of limits

The [[hom-functor preserves limits]] in both arguments separately. This means:

* for fixed object $c \in C$ the functor $hom(c,-) : C \to Set$ sends limit [[diagrams]] in $C$ to limit diagrams in $Set$;

* for fixed object $c' \in C$ the functor $hom(-,c') : C^{op} \to Set$ sends limit diagrams in $C^{op}$ -- which are [[colimit]] [[diagrams]] in $C$! -- to limit diagrams in $Set$. 

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

### Relation to profunctors

The hom-functor $hom : C^{op}\times C\to Set$ is also the identity [[profunctor]] $1_C: C &#8696; C$.

One way to see this is to notice that its [[adjunct]] 

$$
  C \to [C^{op}, Set]
$$

under the [[internal hom]] [[adjunction]] in the 1-category [[Cat]] is the functor

$$
  C \stackrel{id}{\to} C \stackrel{j}{\to} [C^{op}, Set]
  \,,
$$

where $j$ is the [[Yoneda embedding]]. Profunctors $\mathbf{F} : C^{op} \times C \to Set$ whose hom-adjunct is of the form $C \stackrel{F}{\to} C \stackrel{j}{\to} [C^{op}, Set]$ for $F$ an ordinary functor are those in the inclusion of these ordinary functors into profunctors. So the hom-functor is the image of the identity functor under this inclusion.


## Examples

...


## Related concepts

* [[hom-set]], [[hom-object]]

* [[hom-functor]]

* [[enriched hom-functor]], [[internal hom-functor]]

* [[derived hom-functor]]


[[!include homotopy-homology-cohomology]]


* [[internal hom]], [[enriched hom]], [[derived hom space]], [[Ext]]



[[!redirects hom-functors]]

[[!redirects hom functor]]
[[!redirects hom functors]]

[[!redirects hom]]
[[!redirects Hom]]
