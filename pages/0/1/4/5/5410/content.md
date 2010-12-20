
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Two-sided fibrations

* table of contents
{:toc}

## Idea

Just as a [[Grothendieck fibration]] $E\to B$ is an alternate way to encode a [[pseudofunctor]] $B^{op}\to $ [[Cat]], a *two-sided fibration* $A \leftarrow E \to B$ is a way to encode a pseudofunctor $A\times B^{op}\to Cat$.

## Definition


+-- {: .un_defn}
###### Definition

A **two-sided discrete fibration** is a [[span]] $q \colon E \to A$, $p \colon E \to B$ of [[categories]] and [[functors]] such that 
1. each $b \to p e$ in $B$ has a unique lift in $E$ that has codomain $e$ and is in the fiber over $q e$
1. each $q e \to a$ in $A$ has a unique lift in $E$ that has domain $e$ and is in the fiber over $p e$
1. for each $f\colon e \to e'$ in $E$, the codomain of the lift of $q f$ equals the domain of the lift of $p f$ and their composite is $f$.

Write 

$$
  DFib(A,B) \subset Span(A,B)
$$ 

for the full [[subcategory]] on the category of  [[span]]s on the 2-sided discrete fibrations.

=--



+-- {: .un_defn}
###### Definition


A **two-sided fibration** is a span $q \colon E \to A$, $p \colon E \to B$ such that
1. each $b \to p e$ in $B$ has a [[cartesian morphism|cartesian]] lift in $E$ with codomain $e$ and lying in the fiber over the identity at $q e$
1. each $q e \to a$ in $A$ has an opcartesian lift in $E$ with domain $e$ and lying in the fiber over the identity at $p e$
1. for each $f \colon e \to e'$ in $E$ the canonical arrow between the codomain of any opcartesian lift of $q f$ as in (2) and the domain of the cartesian lift of $p f$ as in (1) is an [[isomorphism]].

=--

## Properties

+-- {: .un_def}
###### Definition

Given a profunctor $F : B^{op} \times A \to Set$,
its [[collage]] is the category $K_F$ over the [[interval category]] 

$$
  p : K_F \to \Delta[1]
$$ 

With $p^{-1}(0) = B$, $p^{-1}(1) = A$, $K_F(b,a) = F(b,a)$ 
and $K_F(a,b) = \emptyset$ for all $b \in B$, $a \in A$, where 

* the composite of $b \stackrel{e}{\to} a$ with $a \stackrel{f}{\to} a'$ is given by $F(b,f)(e)$;

* the composite of $b \stackrel{g}{\to} b'$ with $b' \stackrel{e'}{\to} a'$ is given by $F(g, a')(e')$.


=--


+-- {: .un_prop #EquivDFibWithProf}
###### Proposition

There is an [[equivalence of categories]]

$$
  [B^{op} \times A, Set]
    \stackrel{\simeq}{\to}
  DFib(A,B) 
$$

$$
  F \mapsto E_F
  \,,
$$

[[pseudo-natural transformation|pseudo-natural]] in $A, B \in Cat$, between [[profunctor]]s in [[Set]] and discrete fibrations from $A$ to $B$, where $E_F$ is the category whose

* objects are [[section]]s $\sigma : \Delta[1] \to K_F$ of the [[collage]]
  $p : K_F \to \Delta[1]$

* morphisms are [[natural transformation]]s between such sections;

* the two projections $A \leftarrow E_F \to B$ are the two functors induced
  by restriction along $\{0\} \to \Delta[1] \leftarrow \{1\}$.

=--


+-- {: .proof}
###### Proof

First we write out $E_F$ in detail. In the following $b, b', \cdots \in B$
and $a,a', \dots \in A$.

The objects of $E_F$ are morphisms

$$
  \array{
    b 
    \\
    {}^{\mathllap{e}}\downarrow
    \\
    a
  }
$$

in $K_F$, hence triples $(b \in B, a \in A, e \in F(b,a))$.

Morphisms are [[commuting diagram]]s

$$
  \array{
    b &\stackrel{g}{\to}& b'
    \\
    {}^{\mathllap{e}}\downarrow && \downarrow^{\mathrlap{e'}}
    \\
    a &\stackrel{f}{\to}& a'
  }
$$

in $K_F$. We may identify these with pairs $((b \stackrel{g}{\to}b') \in B,(a \stackrel{f}{\to} a') \in A)$ such that 

$$
  F(g,a')(e') = F(b,f)(e)
  \,.
$$ 

We check that this construction yields a two-sided fibration. The three conditions are

1. For
  
   $$
     \array{
        b 
        \\
        {}^{\mathllap{e}}\downarrow
        \\
        a
     }
   $$

   an object of $E_F$ and $a \stackrel{f}{\to} a'$ a morphism in $A$,
   we have that

   $$
     \array{
        b &\stackrel{Id}{\to}& b
        \\
        {}^{\mathllap{e}}\downarrow 
        & & 
        \downarrow^{\mathrlap{f e}}
        \\
        a &\underset{f}{\to}& a'
     }
   $$

   is the unique lift to a morphism in $E$ that maps to $Id_b$.

1. Analogously, for
  
   $$
     \array{
        b' 
        \\
        {}^{\mathllap{e'}}\downarrow
        \\
        a'
     }
   $$

   an object of $E_F$ and $b \stackrel{g}{\to} b'$ a morphism in $B$,
   we have that

   $$
     \array{
        b &\stackrel{g}{\to}& b'
        \\
        {}^{\mathllap{e' g}}\downarrow 
        & & 
        \downarrow^{\mathrlap{e'}}
        \\
        a' &\underset{id}{\to}& a'
     }
   $$

   is the unique lift to a morphism in $E$ that maps to $Id_{a'}$.

1. For 
   
   $$
     \array{
        b &\stackrel{g}{\to}& b'
        \\
        {}^{\mathllap{e}}\downarrow && 
        \downarrow^{\mathrlap{e'}}
        \\
        a &\underset{f}{\to}& a'
     }
   $$

   an arbitrary morphism in $E_F$, these two unique lifts of its $A$- and its
   $B$-projection, respectively, are

   $$
     \array{
        b &\stackrel{Id}{\to}& b
        \\
        {}^{\mathllap{e}}\downarrow 
        & & 
        \downarrow^{\mathrlap{f e}}
        \\
        a &\underset{f}{\to}& a'
     }
   $$

   and

   $$
     \array{
        b &\stackrel{g}{\to}& b'
        \\
        {}^{\mathllap{e' g}}\downarrow & & 
        \downarrow^{\mathrlap{e'}}
        \\
        a' &\underset{Id}{\to}& a'
     }
     \,.
   $$

   The codomain and domain do match, since $f e = e' g$   by the 
   existence of the original morphism, and their composite is the original 
   morphism

   $$
     \array{
        b &\stackrel{Id}{\to}& b &\stackrel{g}{\to}& b
        \\
        {}^{\mathllap{e}}\downarrow 
        & & 
        {}^{\mathllap{f e}}\downarrow^{\mathrlap{e' g}}
         &&
         \downarrow^{\mathrlap{e'}}
        \\
        a &\underset{f}{\to}& a' &\stackrel{Id}{\to}& a'
     }    
     \,.
   $$

To see that this construction indeed yields an equivalence of categories, define a functor $(A\leftarrow E \to B) \mapsto (F_E : B^{op} \times A \to Set)$ by setting

* $F_E(b,a) := E_{b,a}$;

* for a morphism $b \stackrel{g}{\to} b'$ let $F_E(g,a') : F_E(b',a') \to F_E(b,a')$ be the function that sends $b' \stackrel{e'}{\to} a'$ to the domain of the unique lift of $b \stackrel{g}{\to} b'$ with this codomain and mapping to $Id_{a'}$;

* for a morphism $a \stackrel{f}{\to} a'$ let $F_E(b,f) : F_E(b,a) \to F_E(b,a')$ be the function that sends $b \stackrel{e}{\to} a$ to the codomain of the unique lift of $a \stackrel{f}{\to} a'$ with this domain and mapping to $Id_{b}$;.

One checks that this yields an equivalence of categories. 

=--

+-- {: .un_lemma}
###### Observation

The category $E_F$ is equivalently characterizd as being the [[comma category]] of the diagram $B \to K_F \leftarrow A$.

=--


## Related concepts

* [[Grothendieck fibration]], **two-sided fibration**,

* [[Cartesian fibration]]

## References

The notion is originally discussed in

* [[Ross Street]], Ross Street. Fibrations and Yoneda's lemma in a 2-category. In Category Seminar (Proc. Sem., Sydney, 1972/1973), pages 104  133. Lecture Notes in Math., Vol. 420. Springer, Berlin, 1974.

* [[Ross Street]], _Fibrations in bicategories_ Cahiers Topologie G&#233;om. Diff&#233;rentielle,
21(2):111{160, 1980. (Corrections in 28(1):53{56, 1987)

A useful review is in

* [[Emily Riehl]], _Two-sided discrete fibrations in 2-categories and bicategories_ 2010 ([pdf](http://math.uchicago.edu/~eriehl/fibrations.pdf))
{#Riehl}

[[!redirects two-sided fibrations]]
[[!redirects two-sided discrete fibration]]
[[!redirects two-sided discrete fibrations]]


[[!redirects 2-sided fibration]]
[[!redirects 2-sided fibrations]]
[[!redirects 2-sided discrete fibration]]
[[!redirects 2-sided discrete fibrations]]
