
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
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

A _weak factorization system_ on a [[category]] is a [[pair]] $(\mathcal{L},\mathcal{R})$ of [[classes]] of [[morphisms]] ("[[projective morphisms]]" and "[[injective morphisms]]") such that 1) every morphism of the category factors as the composite of one in $\mathcal{L}$ followed by one in $\mathcal{R}$, and 2) $\mathcal{L}$ and $\mathcal{R}$ are closed under having the [[lifting property]] against each other.

If the liftings here are unique, then one speaks of an _orthogonal factorization system_. A classical example of an orthogonal factorization system is the [[(epi,mono)-factorization system]] on the category [[Set]] or in fact on any [[topos]].

Non-orthogonal weak factorization systems are the key ingredient in [[model categories]], which by definition carry a weak factorization system called ($\mathcal{L} = $ [[cofibrations]],$\mathcal{R} = $ [[acyclic fibrations]]) and another one called ($\mathcal{L} =$ [[acyclic cofibrations]], $\mathcal{R} =$ [[fibrations]]). Indeed most examples of non-orthogonal weak factorization systems arise in the context of model category theory.  A key tool for constructing these, or verifying their existence, is the _[[small object argument]]_.

There are other [[properties]] which one may find or impose on a weak factorization system, for instance [[functorial factorization]]. There is also [[extra structure]] which one may find or impose, such as for [[algebraic weak factorization systems]]. For more variants see at _[[factorization system]]_.

## Definition

### Weak factorization systems

+-- {: .num_defn #WeakFactorizationSystem}
###### Definition

A **weak factorization system** (WFS) on a [[category]] $\mathcal{C}$ is a [[pair]] $(\mathcal{L},\mathcal{R})$ of [[classes]] of [[morphisms]] of $\mathcal{C}$ such that

1. Every [[morphism]] $f \colon X\to Y$ of $\mathcal{C}$ may be factored as the [[composition]] of a morphism in $\mathcal{L}$ followed by one in $\mathcal{R}$

   $$
     f\;\colon\;  X \overset{\in \mathcal{L}}{\longrightarrow} Z \overset{\in \mathcal{R}}{\longrightarrow} Y
     \,.
   $$

1. The classes are closed under having the [[lifting property]] against each other:

   1. $\mathcal{L}$ is precisely the class of morphisms having the [[left lifting property]] against every morphism in $\mathcal{R}$;

   1. $\mathcal{R}$ is precisely the class of morphisms having the [[right lifting property]] against every morphism in $\mathcal{L}$.

=--

+-- {: .num_defn #FunctorialFactorization}
###### Definition

For $\mathcal{C}$ a [[category]], a **[[functorial factorization]]** of the morphisms in $\mathcal{C}$ is a [[functor]]

$$
  fact \;\colon\; \mathcal{C}^{\Delta[1]} \longrightarrow \mathcal{C}^{\Delta[2]}
$$

which is a [[section]] of the [[composition]] functor $d_1 \;\colon \;\mathcal{C}^{\Delta[2]}\to \mathcal{C}^{\Delta[1]}$.

=--

+-- {: .num_remark}
###### Remark

In def. \ref{FunctorialFactorization} we are using the following notation, see at _[[simplex category]]_ and at _[[nerve of a category]]_:

Write $\Delta[1] = \{0 \to 1\}$ and $\Delta[2] = \{0 \to 1 \to 2\}$ for the [[ordinal numbers]], regarded as [[posets]] and hence as [[categories]]. The [[arrow category]] $Arr(\mathcal{C})$ is equivalently the [[functor category]] $\mathcal{C}^{\Delta[1]} \coloneqq Funct(\Delta[1], \mathcal{C})$, while $\mathcal{C}^{\Delta[2]}\coloneqq Funct(\Delta[2], \mathcal{C})$ has as objects pairs of composable morphisms in $\mathcal{C}$. There are three injective functors $\delta_i \colon [1] \rightarrow [2]$, where $\delta_i$ omits the index $i$ in its image.
By precomposition, this induces [[functors]] $d_i  \colon \mathcal{C}^{\Delta[2]} \longrightarrow \mathcal{C}^{\Delta[1]}$. Here

* $d_1$ sends a pair of composable morphisms to their [[composition]];

* $d_2$ sends a pair of composable morphisms to the first morphism;

* $d_0$ sends a pair of composable morphisms to the second morphism.

=--

+-- {: .num_defn #FunctorialWeakFactorizationSystem}
###### Definition

A weak factorization system, def. \ref{WeakFactorizationSystem}, is called a **functorial weak factorization system** if the factorization of morphisms may be chosen to be a [[functorial factorization]] $fact$, def. \ref{FunctorialFactorization}, i.e. such that $d_2 \circ fact$ lands in $\mathcal{L}$ and $d_0\circ fact$ in $\mathcal{R}$.

=--

+-- {: .num_remark}
###### Remark

Not all weak factorization systems are functorial, although most (including those produced by the [[small object argument]], with due care) are. But all [[orthogonal factorization systems]], def. \ref{OrthogonalFactorizationSystem}, automatically are functorial.  An example of a weak factorization that is not functorial can be found in [Isaksen 2001](https://arxiv.org/abs/math/0106152).

=--




### Orthogonal factorization systems

+-- {: .num_defn #OrthogonalFactorizationSystem}
###### Definition

An **[[orthogonal factorization system]]** (OFS) is a weak factorization system $(\mathcal{L},\mathcal{R})$, def. \ref{WeakFactorizationSystem} such that the lifts of elements in $\mathcal{L}$ against elements in $\mathcal{R}$ are _unique_.

=--

+-- {: .num_remark }
###### Remark

While every OFS (def. \ref{OrthogonalFactorizationSystem}) is a WFS (def. \ref{WeakFactorizationSystem}), the primary examples of each are different:

A "basic example" of an OFS is [[(epi,mono)-factorization]] in [[Set]] (meaning $L$ is the collection of [[epimorphisms]] and $R$ that of [[monomorphisms]]), while a "basic example" of a WFS is (mono, epi) in $Set$.
The superficial similarity of these two examples masks the fact that they generalize in very different ways.

The OFS (epi, mono) generalizes to any [[topos]] or [[pretopos]], and in fact to any [[regular category]] if we replace "epi" with [[regular epimorphism|regular epi]].  Likewise it generalizes to any [[quasitopos]] if we instead replace "mono" with [[regular monomorphism|regular mono]].

On the other hand, saying that (mono,epi) is a WFS in [[Set]] is equivalent to the [[axiom of choice]].  A less loaded statement is that $(L,R)$ is a WFS, where $L$ is the class of inclusions $A\hookrightarrow A\sqcup B$ into a binary [[coproduct]] and $R$ is the class of [[split epimorphism|split epis]].  In this form the statement generalizes to any [[extensive category]]; see also [[weak factorization system on Set]].

=--

### Algebraic weak factorization systems

An [[algebraic weak factorization system]] enhances the *properties* of lifting and factorization to algebraic [[stuff, structure, property|structure]].

### Accessible weak factorization systems

An [[accessible weak factorization system]] is a wfs on a [[locally presentable category]] whose factorization is given by an [[accessible functor]].


## Properties

### Closure properties
 {#ClosureProperties}

+-- {: .num_prop #ClosuredPropertiesOfWeakFactorizationSystem}
###### Proposition

Let $(\mathcal{L},\mathcal{R})$ be a weak factorization system, def. \ref{WeakFactorizationSystem} on some [[category]] $\mathcal{C}$. Then

1. Both classes contain the class of [[isomorphism]] of $\mathcal{C}$.

1. Both classes are closed under [[composition]] in $\mathcal{C}$.

   $\mathcal{L}$ is also closed under [[transfinite composition]].

1. Both classes are closed under forming [[retracts]] in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$ (see remark \ref{RetractsOfMorphisms}).

1. $\mathcal{L}$ is closed under forming [[pushouts]] of morphisms in $\mathcal{C}$ ("[[cobase change]]").

   $\mathcal{R}$ is closed under forming [[pullback]] of morphisms in $\mathcal{C}$ ("[[base change]]").

1. $\mathcal{L}$ is closed under forming [[coproducts]] in $\mathcal{C}^{\Delta[1]}$.

   $\mathcal{R}$ is closed under forming [[products]] in $\mathcal{C}^{\Delta[1]}$.

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

with the left morphism an isomorphism, then a [[lift]] is given by using the [[inverse]] of this isomorphism ${}^{{f \circ i^{-1}}}\nearrow$. Hence in particular there is a lift when $p \in \mathcal{R}$ and so $i \in \mathcal{L}$. The other case is [[formal dual|formally dual]].

**closure under composition**

Given a [[commuting square]] of the form

$$
  \array{
    A &\longrightarrow& X
    \\
    \downarrow && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in \mathcal{R}}}
    \\
    {}^{\mathllap{i}}_{\mathllap{\in \mathcal{L}}}\downarrow && \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in \mathcal{R}}}
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
    &\searrow& \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in \mathcal{R}}}
    \\
    {}^{\mathllap{i}}_{\mathllap{\in \mathcal{L}}}\downarrow && \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in \mathcal{R}}}
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
    {}^{\mathllap{i}}_{\mathllap{\in \mathcal{L}}}\downarrow
    && \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in \mathcal{R}}}
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{p_2}}_{\mathrlap{\in \mathcal{R}}}
    \\
    B &\longrightarrow& Y
  }
$$

and now the top commuting square has a lift by assumption. This is now equivalently a lift in the total diagram, showing that $p_1\circ p_1$ has the right lifting property against $\mathcal{L}$ and is hence in $\mathcal{R}$. The case of composing two morphisms in $\mathcal{L}$  is [[formal dual|formally dual]]. From this the closure of $\mathcal{L}$ under [[transfinite composition]] follows since the latter is given by [[colimits]] of sequential composition and successive lifts against the underlying sequence as above constitutes a [[cocone]], whence the extension of the lift to the colimit follows by its [[universal property]].

**closure under retracts**

Let $j$ be the [[retract]] of an $i \in \mathcal{L}$, i.e. let there be a [[commuting diagram]] of the form.

$$
  \array{
    id_A \colon & A &\longrightarrow& C &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{i}}_{\mathrlap{\in \mathcal{L}}} && \downarrow^{\mathrlap{j}}
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
     {}^{\mathllap{j}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in \mathcal{R}}}
     \\
     B &\longrightarrow& Y
  }
$$

a [[commuting square]], it is equivalent to its [[pasting]] composite with that retract diagram

$$
  \array{
    A &\longrightarrow& C &\longrightarrow& A &\longrightarrow& X
    \\
    \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{i}}_{\mathrlap{\in \mathcal{L}}} && \downarrow^{\mathrlap{j}} && \downarrow^{\mathrlap{f}}_{\mathrlap{\in \mathcal{R}}}
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
    \downarrow^{\mathrlap{i}}_{\mathrlap{\in \mathcal{L}}}
      &&
    \nearrow
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in \mathcal{R}}}
    \\
    B &\longrightarrow& D &\longrightarrow& B &\longrightarrow & Y
  }
  \,.
$$

By composition, this is also a lift in the total outer rectangle, hence in the original square. Hence $j$ has the left lifting property against all $p \in \mathcal{R}$ and hence is in $\mathcal{L}$. The other case is [[formal duality|formally dual]].



**closure under pushout and pullback**

Let $p \in \mathcal{R}$ and and let

$$
  \array{
    Z \times_f X &\longrightarrow& X
    \\
    {}^{\mathllap{{f^* p}}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Z &\stackrel{f}{\longrightarrow} & Y
  }
$$

be a [[pullback]] diagram in $\mathcal{C}$. We need to show that $f^* p$ has the [[right lifting property]] with respect to all $i \in \mathcal{L}$. So let

$$
  \array{
     A &\longrightarrow& Z \times_f X
     \\
     {}^{\mathllap{i}}_{\mathllap{\in \mathcal{L}}}\downarrow && \downarrow^{\mathrlap{\mathrlap{f^* p}}}
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

Let $\{(A_s \overset{i_s}{\to} B_s) \in \mathcal{L}\}_{s \in S}$ be a set of elements of $\mathcal{L}$. Since [[colimits]] in the [[presheaf category]] $\mathcal{C}^{\Delta[1]}$ are computed componentwise, their [[coproduct]] in this [[arrow category]] is the universal morphism out of the coproduct of objects $\underset{s \in S}{\coprod} A_s$ induced via its [[universal property]] by the set of morphisms $i_s$:

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
    {}^{\mathllap{(i_s)_{s\in S}}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in \mathcal{R}}}
    \\
    \underset{s \in S}{\sqcup} B_s
    &\longrightarrow&
    Y
  }
$$

be a [[commuting square]]. This is in particular a [[cocone]] under the [[coproduct]] of objects, hence by the [[universal property]] of the coproduct, this is equivalent to a set of commuting diagrams

$$
  \left\{
  \;\;\;\;
  \array{
    A_s &\longrightarrow& X
    \\
    {}^{\mathllap{i_s}}_{\mathllap{\in \mathcal{L}}}\downarrow
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in \mathcal{R}}}
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
  \;\;\;\;
  \array{
    A_s &\longrightarrow& X
    \\
    {}^{\mathllap{i_s}}_{\mathllap{\in \mathcal{L}}}\downarrow
      &{}^{\ell_s}\nearrow& \downarrow^{\mathrlap{f}}_{\mathrlap{\in \mathcal{R}}}
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
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in \mathcal{R}}}
    \\
    \underset{s \in S}{\sqcup} B_s
    &\longrightarrow&
    Y
  }
  \,.
$$

This shows that the coproduct of the $i_s$ has the left lifting property against all $f\in \mathcal{R}$ and is hence in $\mathcal{L}$. The other case is [[formal dual|formally dual]].



=--


+-- {: .num_remark}
###### Remark

Beware, in the situation of prop. \ref{ClosuredPropertiesOfWeakFactorizationSystem},
that $\mathcal{L}$ is not in general closed under all [[colimits]] in $\mathcal{C}^{\Delta[1]}$, and similarly $\mathcal{R}$ is not in general closed under all [[limits]] in $\mathcal{C}^{\Delta[1]}$. Also $\mathcal{L}$ is not in general closed under forming [[coequalizers]] in $\mathcal{C}$, and $\mathcal{R}$ is not in general closed under forming [[equalizers]] in $\mathcal{C}$. However, if $(\mathcal{L},\mathcal{R})$ is an [[orthogonal factorization system]], def. \ref{OrthogonalFactorizationSystem}, then $\mathcal{L}$ is closed under all colimits and $\mathcal{R}$ is closed under all limits.

=--

+-- {: .num_remark #RetractsOfMorphisms}
###### Remark

Here by a _retract_ of a [[morphism]] $X \stackrel{f}{\longrightarrow} Y$ in some [[category]] $\mathcal{C}$ is meant a [[retract]] of $f$ as an object in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$, hence a morphism $A \stackrel{g}{\longrightarrow} B$ such that in $\mathcal{C}^{\Delta[1]}$ there is a factorization of the identity on $g$ through $f$

$$
  id_g \;\colon\;
  g \longrightarrow f \longrightarrow g
  \,.
$$

This means equivalently that in $\mathcal{C}$ there is a [[commuting diagram]] of the form

$$
  \array{
    id_A \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}}
    \\
    id_B \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
  \,.
$$

=--

### Retract argument

+-- {: .num_lemma #RetractArgument}
###### Lemma
**([[retract argument]])**

Consider a [[composition|composite]] [[morphism]]

$$
  f \;\colon\; X\stackrel{i}{\longrightarrow} A \stackrel{p}{\longrightarrow} Y
  \,.
$$

Then:

1. If $f$ has the [[left lifting property]] against $p$, then $f$ is a [[retract]] of $i$.

1. If $f$ has the [[right lifting property]] against $i$, then $f$ is a [[retract]] of $p$.

=--

+-- {: .proof}
###### Proof

We discuss the first statement, the second is [[formal duality|formally dual]].

Write the factorization of $f$ as a [[commuting square]] of the form

$$
  \array{
    X &\stackrel{i}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Y &= & Y
  }
  \,.
$$

By the assumed [[lifting property]] of $f$ against $p$ there exists a diagonal filler $g$ making a [[commuting diagram]] of the form

$$
  \array{
    X &\stackrel{i}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow &{}^{\mathllap{g}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    Y &= & Y
  }
  \,.
$$

By rearranging this diagram a little, it is equivalent to

$$
  \array{
    & X &=& X
    \\
    & {}^{\mathllap{f}}\downarrow
     &&
    {}^{\mathllap{i}}\downarrow
    \\
    id_Y \colon & Y &\underset{g}{\longrightarrow}& A &\underset{p}{\longrightarrow}&
    Y
  }
  \,.
$$

Completing this to the right, this yields a diagram exhibiting the required retract according to remark \ref{RetractsOfMorphisms}:

$$
  \array{
    id_X \colon & X &=& X &=& X
    \\
    & {}^{\mathllap{f}}\downarrow
     &&
    {}^{\mathllap{i}}\downarrow
     &&
     {}^{\mathllap{f}}\downarrow
    \\
    id_Y \colon & Y &\underset{g}{\longrightarrow}& A &\underset{p}{\longrightarrow}&
    Y
  }
  \,.
$$


=--



## Examples

* [[model category|Model categories]] provide many examples of weak factorization systems.  In fact, most applications of WFS involve model categories or model-categorical ideas.

* The existence of certain [[weak factorization system on Set|WFS on Set]] is related to the [[axiom of choice]].


* See the [[joyalscatlab:Weak factorisation systems|Catlab]] for more examples.




## Related concepts

* [[retract argument]]

* [[injective and projective morphisms]]

* [[algebraic weak factorization system]]

[[!include algebraic model structures - table]]


## References

* [[joyalscatlab:HomePage|Joyal's CatLab]], _[[joyalscatlab:Weak factorisation systems]]_

* {#Hirschorn} Philip S. Hirschhorn, _Model Categories and Their Localizations_ ([AMS](http://www.ams.org/bookstore?fn=20&arg1=whatsnew&item=SURV-99), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

* Jiri Rosicky, Walter Tholen , *Factorization, Fibration and Torsion*, [arxiv](https://arxiv.org/abs/0801.0063) (2007)

Introductory texts:

* [[Introduction to Homotopy Theory]]

* {#Riehl2008} [[Emily Riehl]], [_Factorization Systems_](https://math.jhu.edu/~eriehl/factorization.pdf), 2008

* [[Emily Riehl]], Chapter 11 in: *[[Categorical Homotopy Theory]]*, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457), [pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf)&rbrack;

The following dissertation section is entirely written after learning of [Riehl (2008)](#Riehl2008) above, but has complementary examples and may dive deeper into some proofs:

* {#Nuyts2020} [[Andreas Nuyts]], _Contributions to Multimode and Presheaf Type Theory, section 2.4: Factorization Systems_, [PhD thesis](https://lirias.kuleuven.be/retrieve/581985), KU Leuven, Belgium, 2020


[[!redirects weak factorization systems]]

