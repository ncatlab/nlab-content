
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

Recall that a functor $E \to B$ is called a [[fibration]] if its [[fibres]] $E_b$ vary [[pseudofunctor|functorially]] in $b$; taking _fibre_ to mean _strict fibre_ results in the notion of [[Grothendieck fibration]], while taking it to mean [[essential fibre]] gives the notion of [[Street fibration]].

Similarly, a *two-sided fibration* $A \leftarrow E \to B$ is a pair of functors whose fibres $E(a,b)$ vary functorially in both $a$ and $b$.

## Definition

Let $K$ be a [[bicategory]] with finite [[2-limits]], and recall that [[fibration in a 2-category|fibrations]] in $K$ may be defined in any of several ways; most importantly, cloven fibrations $E \to B$ in $K$ are the (pseudo)algebras for a (pseudo) 2-monad $L$ on $K/B$.  For a morphism $p \colon E \to A$ in $K$, $L p$ is given by composing the [[span]] $A \overset{p}{\leftarrow} E \to 1$ with the canonical span $\Phi A = A \overset{dom}{\leftarrow} A^{\mathbf{2}} \overset{cod}{\to} A$, so that $L p \colon E/p \to A$ is the canonical projection.  More generally, the same construction gives a monad $L$ on $Span K(B,A)$ whose algebras we call **left fibrations**.  In [[Cat]], a span $C \overset{p}{\leftarrow} H \overset{q}{\to} D$ is a left fibration if $p$ is a cloven fibration whose chosen cartesian lifts are $q$-vertical.

Dually, there is a 2-monad $R$ on each $Span K(B,A)$ whose algebras
are called **right fibrations**, the special case of $Span Cat(D,1)$ yielding cloven opfibrations.

There is then a composite 2-monad $M$ that takes a span $E$ from $B$ to $A$ to $M E = \Phi A \circ E \circ \Phi B$, and $M$-algebras are called **two-sided fibrations**.

+-- {: .un_prop}
###### Proposition

A two-sided Street fibration from $B$ to $A$ in $Cat$ is given by a span $p \colon E \to A$, $q \colon E \to B$ such that

1. each $a \to p x$ in $A$ has a [[cartesian morphism|cartesian]] lift in $E$ with codomain $x$ whose image under $q$ is invertible (that is, $E$ is a left fibration)

1. each $q x \to b$ in $B$ has an opcartesian lift in $E$ with domain $x$ whose image under $p$ is invertible ($E$ is a right fibration)

1. for each $f \colon e \to e'$ in $E$ the canonical arrow between the codomain of any opcartesian lift of $q f$ as in (2) and the domain of the cartesian lift of $p f$ as in (1) is an [[isomorphism]].
=--

+-- {: .proof}
###### Proof
**Warning**: incomplete, possibly wrong

By the usual theory of [[distributive laws]], an $M$-algebra $m \colon M E \to E$ gives rise to $L$- and $R$-algebras $m \cdot (\Phi A \circ \eta^R_E)$ and $m \cdot (\eta^L_E \circ \Phi B)$, and conversely an $L$-algebra $\ell$ and an $R$-algebra $r$ underlie an $M$-algebra if and only if there is an isomorphism $r \cdot (\ell \circ \Phi B) \cong \ell \cdot (\Phi A \circ r)$ that makes $r$ a morphism of $L$-algebras.

Now given $\ell$ and $r$, because $L$ is [[colax-idempotent]], there is a unique two-cell $\bar r \colon r \cdot (\ell \circ \Phi B) \Rightarrow \ell \cdot (\Phi A \circ r)$ that makes $r$ a colax morphism of $L$-algebras.  So we want to show that given an $L$-algebra and an $R$-algebra in $Cat$, this two-cell is invertible if and only if condition (3) above holds.

The two-cell in question is given here by $\ell \cdot (\Phi A \circ r) \cdot (\epsilon \circ \Phi B)$, where $\epsilon$ is the counit of the adjunction $\eta^L_E \dashv \ell$.

... to be continued ...

=--


# Two-sided discrete fibrations

## Definition

A two-sided fibration $A \leftarrow E \to B$ in $K$ is **discrete** if it is [[discrete object|discrete]] as an object of $K/A \times B$.

For Grothendieck fibrations in [[Cat]], this means the following.

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

Note that profunctors can also be characterized by their collages, these being the two-sided [[codiscrete cofibrations]]; and the collage corresponding to a two-sided fibration is its [[cocomma object]].


## Related concepts

* [[Grothendieck fibration]], [[Street fibration]], [[discrete fibration]], **two-sided fibration**,

* [[Cartesian fibration]]

## References

The notion is originally discussed in

* [[Ross Street]]. _Fibrations and Yoneda's lemma in a 2-category_. In Category Seminar (Proc. Sem., Sydney, 1972/1973), pages 104  133. Lecture Notes in Math., Vol. 420. Springer, Berlin, 1974.

* [[Ross Street]], _Fibrations in bicategories_. Cahiers Topologie G&#233;om. Diff&#233;rentielle,
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
