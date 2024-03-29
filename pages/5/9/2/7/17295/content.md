
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Injective and projective morphisms are [[morphisms]] in a [[category]] satisfying some [[lifting property]]. Often they appear jointly to form [[weak factorization systems]].

## Definition

### Injective and projective

Given a [[category]] $\mathcal{C}$ and a [[class]] $J \subset Mor(\mathcal{C})$ of its [[morphisms]], then any morphism $f \in Mor(\mathcal{C})$ is called

* a **$J$-injective morphism** if it has the [[right lifting property]] against elements in $J$;

* a **$J$-projective morphism** if it has the [[left lifting property]] against elements in $J$.

If $\mathcal{C}$ has a [[terminal object]] $\ast$, then an object $X$ for which $X \stackrel{\exists!}{\to} \ast$ is a $J$-injective morphism is called a $J$-[[injective object]].

If $\mathcal{C}$ has an [[initial object]] $\emptyset$, then an object $X$ for which $\emptyset \stackrel{\exists!}{\to} X$ is a $J$-projective morphism is called a $J$-[[projective object]].

### Fibration and cofibration

Frequently one furthermore says:

* a **$J$-[[cofibration]]** is a morphism that has the [[left lifting property]] against all $J$-injective morphisms;

* a **$J$-[[fibration]]** is a morphism that has the [[right lifting property]] against all $J$-projective morphisms.

## Properties

### Closure properties
 {#ClosureProperties}

+-- {: .num_prop #ClosurePropertiesOfInjectiveAndProjectiveMorphisms}
###### Proposition

Let $\mathcal{C}$ be a [[category]] and let $K\subset Mor(\mathcal{C})$ be a [[class]] of [[morphisms]]. Write $K Proj$ and $K Inj$, respectively, for the sub-classes of $K$-[[projective morphisms]] and of $K$-[[injective morphisms]] (the "[[Quillen negation]]" of $K$). Then:

1. Both classes contain the class of [[isomorphism]] of $\mathcal{C}$.

1. Both classes are closed under [[composition]] in $\mathcal{C}$.

   $K Proj$ is also closed under [[transfinite composition]].

1. Both classes are closed under forming [[retracts]] in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$.

1. $K Proj$ is closed under forming [[pushouts]] of morphisms in $\mathcal{C}$ ("[[cobase change]]").

   $K Inj$ is closed under forming [[pullback]] of morphisms in $\mathcal{C}$ ("[[base change]]").

1. $K Proj$ is closed under forming [[coproducts]] in $\mathcal{C}^{\Delta[1]}$.

   $K Inj$ is closed under forming [[products]] in $\mathcal{C}^{\Delta[1]}$.

=--

+-- {: .proof}
###### Proof

We go through each item in turn.

**containing isomorphisms**

Given a [[commuting square]]

$$
  \array{
    A &\overset{f}{\rightarrow}& X
    \\
    {}_{\mathllap{\in Iso}}^{\mathllap{i}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    B &\underset{g}{\longrightarrow}& Y
  }
$$

with the left morphism an isomorphism, the a [[lift]] is given by using the [[inverse]] of this isomorphism ${}^{{f \circ i^{-1}}}\nearrow$. Hence in particular there is a lift when $p \in K$ and so $i \in K Proj$. The other case is [[formal dual|formally dual]].

**closure under composition**

Given a [[commuting square]] of the form

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
$$

consider its [[pasting]] decomposition as

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow 
    &\searrow& \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
  \,.
$$

Now the bottom commuting square has a lift, by assumption. This yields another [[pasting]] decomposition

$$
  \array{
    A &\longrightarrow& X
    \\
    {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow 
    && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in K Inj}}
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in K Inj}}
    \\
    B &\longrightarrow& Y
  }
$$

and now the top commuting square has a lift by assumption. This is now equivalently a lift in the total diagram, showing that $p_1\circ p_1$ has the right lifting property against $K$ and is hence in $K Inj$. The case of composing two morphisms in $K Proj$  is [[formal dual|formally dual]]. From this the closure of $K Proj$ under [[transfinite composition]] follows since the latter is given by [[colimits]] of sequential composition and successive lifts against the underlying sequence as above constitutes a [[cocone]], whence the extension of the lift to the colimit follows by its [[universal property]].

**closure under retracts**

Let $j$ be the [[retract]] of an $i \in K Proj$, i.e. let there be a [[commuting diagram]] of the form.

$$
  \array{
    id_A \colon & A &\longrightarrow& C &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{i}}_{\mathrlap{\in K Proj}} && \downarrow^{\mathrlap{j}}
    \\
    id_B \colon & B &\longrightarrow& D &\longrightarrow& B
  }
  \,.
$$

Then for 

$$
  \array{
     A &\longrightarrow& X
     \\
     {}^{\mathllap{j}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
     \\
     B &\longrightarrow& Y
  }
$$

a [[commuting square]], it is equivalent to its [[pasting]] composite with that retract diagram 

$$
  \array{
    A &\longrightarrow& C &\longrightarrow& A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{i}}_{\mathrlap{\in K Proj}} && \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B &\longrightarrow& D &\longrightarrow& B &\longrightarrow & Y
  }
  \,.
$$

Now the pasting composite of the two squares on the right has a lift, by assumption,

$$
  \array{
    A &\longrightarrow& C &\longrightarrow& A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{j}} 
      && 
    \downarrow^{\mathrlap{i}}_{\mathrlap{\in K Proj}} 
      && 
    \nearrow 
      && 
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B &\longrightarrow& D &\longrightarrow& B &\longrightarrow & Y
  }
  \,.
$$

By composition, this is also a lift in the total outer rectangle, hence in the original square. Hence $j$ has the left lifting property against all $p \in K$ and hence is in $K Proj$. The other case is [[formal duality|formally dual]].



**closure under pushout and pullback**

Let $p \in K Inj$ and and let 

$$
  \array{
    Z \times_f X &\longrightarrow& X
    \\
    {}^{\mathllap{{f^* p}}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Z &\stackrel{f}{\longrightarrow} & Y 
  }
$$

be a [[pullback]] diagram in $\mathcal{C}$. We need to show that $f^* p$ has the [[right lifting property]] with respect to all $i \in K$. So let

$$
  \array{
     A &\longrightarrow& Z \times_f X
     \\
     {}^{\mathllap{i}}_{\mathllap{\in K}}\downarrow && \downarrow^{\mathrlap{\mathrlap{f^* p}}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z
  }
$$

be a [[commuting square]]. We need to construct a diagonal lift of that square. To that end, first consider the [[pasting]] composite with the pullback square from above to obtain the commuting diagram

$$
  \array{
     A &\longrightarrow& Z \times_f X &\longrightarrow& X
     \\
     {}^{\mathllap{i}}\downarrow && \downarrow^{\mathrlap{f^* p}} 
     && \downarrow^{\mathrlap{p}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

By the right lifting property of $p$, there is a diagonal lift of the total outer diagram

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{i}} &{}^{\hat {(f g)}}\nearrow&  \downarrow^{\mathrlap{p}}
    \\
    B &\stackrel{f g}{\longrightarrow}& Y
  }
  \,.
$$

By the [[universal property]] of the [[pullback]] this gives rise to the lift $\hat g$ in

$$
  \array{
     && Z \times_f X &\longrightarrow& X
     \\
     &{}^{\hat g} \nearrow& \downarrow^{\mathrlap{f^* p}} 
     && \downarrow^{\mathrlap{p}}
     \\
     B &\stackrel{g}{\longrightarrow}& Z &\stackrel{f}{\longrightarrow}& Y
  }
  \,.
$$

In order for $\hat g$ to qualify as the intended lift of the total diagram, it remains to show that 

$$
  \array{
     A &\longrightarrow& Z \times_f X
     \\
     \downarrow^{\mathrlap{i}} & {}^{\hat g}\nearrow
     \\
     B
  }
$$

commutes. To do so we notice that we obtain two [[cones]] with tip $A$:

* one is given by the morphisms 
  1. $A \to Z \times_f X \to X$
  2. $A \stackrel{i}{\to} B \stackrel{g}{\to} Z$

  with universal morphism into the pullback being

  * $A \to Z \times_f X$

* the other by
  1. $A \stackrel{i}{\to} B \stackrel{\hat g}{\to} Z \times_f X \to X$
  2. $A \stackrel{i}{\to} B \stackrel{g}{\to} Z$.
  
  with universal morphism into the pullback being
  
  * $A \stackrel{i}{\to} B \stackrel{\hat g}{\to} Z \times_f X$.

The commutativity of the diagrams that we have established so far shows that the first and second morphisms here equal each other, respectively. By the fact that the universal morphism into a pullback diagram is _unique_ this implies the required identity of morphisms.

The other case is [[formal dual|formally dual]].

**closure under (co-)products**

Let $\{(A_s \overset{i_s}{\to} B_s) \in K Proj\}_{s \in S}$ be a set of elements of $K Proj$. Since [[colimits]] in the [[presheaf category]] $\mathcal{C}^{\Delta[1]}$ are computed componentwise, their [[coproduct]] in this [[arrow category]] is the universal morphism out of the coproduct of objects $\underset{s \in S}{\coprod} A_s$ induced via its [[universal property]] by the set of morphisms $i_s$:

$$
  \underset{s \in S}{\sqcup} A_s
  \overset{(i_s)_{s\in S}}{\longrightarrow}
  \underset{s \in S}{\sqcup} B_s  
  \,.
$$

Now let 

$$
  \array{
    \underset{s \in S}{\sqcup} A_s &\longrightarrow& X
    \\
    {}^{\mathllap{(i_s)_{s\in S}}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    \underset{s \in S}{\sqcup} B_s
    &\longrightarrow&
    Y
  }
$$

be a [[commuting square]]. This is in particular a [[cocone]] under the [[coproduct]] of objects, hence by the [[universal property]] of the coproduct, this is equivalent to a set of commuting diagrams

$$
  \left\{
  \;\;\;\;\;\;\;\;\;
  \array{
    A_s &\longrightarrow& X
    \\
    {}^{\mathllap{i_s}}_{\mathllap{\in K Proj}}\downarrow 
      && 
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B_s
    &\longrightarrow&
    Y
  }
  \;\;\;\;
  \right\}_{s\in S}
  \,.
$$

By assumption, each of these has a lift $\ell_s$. The collection of these lifts

$$
  \left\{
  \;\;\;\;\;\;\;\;\;
  \array{
    A_s &\longrightarrow& X
    \\
    {}^{\mathllap{i_s}}_{\mathllap{\in Proj}}\downarrow 
      &{}^{\ell_s}\nearrow& \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    B_s
    &\longrightarrow&
    Y
  }
  \;\;\;\;
  \right\}_{s\in S}
$$

is now itself a compatible [[cocone]], and so once more by the [[universal property]] of the coproduct, this is equivalent to a lift $(\ell_s)_{s\in S}$ in the original square

$$
  \array{
    \underset{s \in S}{\sqcup} A_s &\longrightarrow& X
    \\
    {}^{\mathllap{(i_s)_{s\in S}}}\downarrow 
     &{}^{(\ell_s)_{s\in S}}\nearrow& 
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in K}}
    \\
    \underset{s \in S}{\sqcup} B_s
    &\longrightarrow&
    Y
  }
  \,.
$$

This shows that the coproduct of the $i_s$ has the left lifting property against all $f\in K$ and is hence in $K Proj$. The other case is [[formal dual|formally dual]].



=--


## Related concepts

* the [[small object argument]] is about factoring morphisms into $J$-cofibrations followed by $J$-injective morphisms.

[[!redirects injective or projective morphisms]]

[[!redirects injective morphism]]
[[!redirects injective morphisms]]

[[!redirects projective morphism]]
[[!redirects projective morphisms]]

[[!redirects injective and projective morphisms]]
[[!redirects projective and injective morphisms]]
