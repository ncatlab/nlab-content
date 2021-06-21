

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

One of the basic facts of [[category theory]] is that the [[hom-functor]] on a [[category]] $\mathcal{C}$ [[preserved limit|preserve]] [[limits]] in both [[variables]] (remembering that a limit in the first variable, due to contravariance, is actually a [[colimit]] in $\mathcal{C}$).

## Statement

### Ordinary hom-functor

+-- {: .num_prop #HomFunctorPreservesLimits}
###### Proposition
**([[hom-functor]] [[preserved limit|preserves]] [[limits]])**

Let $\mathcal{C}$ be a [[category]] and write

$$

  Hom_{\mathcal{C}}
   \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
   \longrightarrow
  Set
$$

for its [[hom-functor]]. This [[preserved limit|preserves]] [[limits]] in both its arguments (recalling that a limit in the [[opposite category]] $\mathcal{C}^{op}$ is a [[colimit]] in $\mathcal{C}$).

More in detail, let $X_\bullet \colon \mathcal{I} \longrightarrow \mathcal{C}$ be a [[diagram]]. Then:

1. If the [[limit]] $\underset{\longleftarrow}{\lim}_i X_i$ exists in $\mathcal{C}$ then for all $Y \in \mathcal{C}$ there is a [[natural isomorphism]]

   $$
     Hom_{\mathcal{C}}\left(Y, \underset{\longleftarrow}{\lim}_i X_i \right)
     \simeq
     \underset{\longleftarrow}{\lim}_i \left( Hom_{\mathcal{C}}\left( Y, X_i \right) \right)
      \,,
   $$

   where on the right we have the limit over the diagram of [[hom-sets]] given by 
   
   $$
     Hom_{\mathcal{C}}(Y,-) \circ X \;\colon\; \mathcal{I} \overset{X}{\longrightarrow} \mathcal{C} \overset{Hom_{\mathcal{C}}(Y,-)  }{\longrightarrow} Set\,.
   $$

1. If the [[colimit]] $\underset{\longrightarrow}{\lim}_i X_i$ exists in $\mathcal{C}$ then for all $Y \in \mathcal{C}$ there is a [[natural isomorphism]]

   $$
     Hom_{\mathcal{C}}\left(\underset{\longrightarrow}{\lim}_i X_i ,Y\right)
     \simeq
     \underset{\longleftarrow}{\lim}_i \left( Hom_{\mathcal{C}}\left( X_i , Y\right) \right)
      \,,
   $$

   where on the right we have the limit over the diagram of [[hom-sets]] given by 
   
   $$
     Hom_{\mathcal{C}}(-,Y) \circ X \;\colon\; \mathcal{I}^{op} \overset{X}{\longrightarrow} \mathcal{C}^{op} \overset{Hom_{\mathcal{C}}(-,Y)  }{\longrightarrow} Set\,.
   $$

=--

+-- {: .proof}
###### Proof

We give the proof of the first statement. The proof of the second statement is [[formal dual|formally dual]].

First observe that, by the very definition of [[limit|limiting]] [[cones]], maps out of some $Y$ into them are in natural bijection
with the set $Cones\left(Y, X_\bullet \right)$ of cones over the diagram $X_\bullet$ with tip $Y$:

$$
  Hom\left(
    Y,
    \underset{\longleftarrow}{\lim}_{i} X_i
  \right)
    \;\simeq\;
  Cones\left(
    Y, X_\bullet
  \right)
  \,.
$$

Hence it remains to show that there is also a natural bijection like so:

$$
  Cones\left(
    Y,
    X_\bullet
  \right)
    \;\simeq\;
  \underset{\longleftarrow}{\lim}_{i} \left( Hom(Y,X_i) \right)
  \,.
$$

Now, again by the very definition of limiting cones, a single element in the limit on the right is equivalently a cone of the form

$$
  \left\{
  \array{
    && \ast
    \\
    & {}^{\mathllap{const_{p_i}}}\swarrow && \searrow^{\mathrlap{const_{p_j}}}
    \\
    Hom(Y,X_i)
     && \underset{X_\alpha \circ (-)}{\longrightarrow} &&
    Hom(Y,X_j)
  }
  \right\}_{i, j \in Obj(\mathcal{I}), \alpha \in Hom_{\mathcal{I}}(i,j) }
  \,.
$$

This is equivalently for each object $i \in \mathcal{I}$ a choice of morphism $p_i \colon Y \to X_i$ , such that  for each pair of objects $i,j \in \mathcal{I}$
and each $\alpha \in Hom_{\mathcal{I}}(i,j)$ we have $X_\alpha \circ p_i = p_j$. And indeed, this is precisely the characterization of an element in the
set $  Cones\left( Y, X_{\bullet} \right)$.

=--

### Internal hom-functor


+-- {: .num_prop #InternalHomPreservesLimits}
###### Proposition
**(internal hom-functor preserves limits)**

Let $\mathcal{C}$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with [[internal hom]]-[[bifunctor]] $[-,-]$. Then this bifunctor preserves [[limits]] in the second variable, and sends colimits in the first variable to limits:

$$
  [X, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} Y(j)]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [X, Y(j)]
$$

and

$$
  [\underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j),X]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j),X]  
$$


=--


+-- {: .proof}
###### Proof

For $X \in \mathcal{C}$ any object, $[X,-]$ is a [[right adjoint]] by definition, and hence preserves limits by _[[adjoints preserve (co-)limits]]_.

For the other case, let $Y \;\colon\; \mathcal{L} \to \mathcal{C}$ be a [[diagram]] in $\mathcal{C}$, and let $C \in \mathcal{C}$ be any object. Then there are isomorphisms

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(C, [ \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X ] )
    & \simeq
    Hom_{\mathcal{C}}( C \otimes \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X )
    \\
    & \simeq
    Hom_{\mathcal{C}}( \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} (C \otimes Y(j)), X )   
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( (C \otimes Y(j)), X )    
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( C, [Y(j), X] )    
    \\
    & \simeq
    Hom_{\mathcal{C}}( C, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] )    
  \end{aligned}
$$

which are [[natural isomorphism|natural]] in $C \in \mathcal{C}$, where we used that the ordinary [[hom-functor]] respects (co)limits as shown (see at _[[hom-functor preserves limits]]_), and that the [[left adjoint]] $C \otimes (-)$ preserves colimits (see at _[[adjoints preserve (co-)limits]]_).

Hence by the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]], there is an isomorphism

$$
  \left[ \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X \right]  
  \overset{\simeq}{\longrightarrow}
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] 
  \,.
$$


=--




## Related statements

* [[limits preserve limits]]

* [[adjoints preserve (co-)limits]]

* [[limits commute with limits]]

* [[limits of presheaves are computed objectwise]]

[[!redirects hom-functors preserve limits]]


[[!redirects internal hom-functor preserves limits]]


