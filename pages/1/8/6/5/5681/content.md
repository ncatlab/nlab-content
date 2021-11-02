

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

Let $C$ be an [[(∞,1)-category]] and $f : A \to B$ and $g : X \to Y$ two [[morphism]]s in $C$. Write $C_{A\sslash Y}$ for the [[over-(∞,1)-category|under-over-(∞,1)-category]].

We say that $f$ is **left orthogonal** to $g$ and that $g$ is **right orthogonal** to $f$ and write

$$
  f \perp g
$$

if for every [[commuting diagram]]

$$
  \array{
    A &\to& X
    \\
    {}^{\mathllap{f}}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{g}}
    \\
    B &\to& Y
  }
$$

in $C$ we have that $C_{A\sslash Y}(B,X) \simeq *$ is [[contractible]].

=--

Note that the notation $C_{A\sslash Y}(B,X)$ subtly includes the given commuting diagram, since $C_{A\sslash Y}$ is only defined relative to a particular given morphism $A\to Y$.  Here we take that to be the common composite of the given commuting square, with $B$ and $X$ regarded as objects of $C_{A\sslash Y}$ via the resulting commuting triangles.


+-- {: .num_defn}
###### Definition

Let $C$ be an [[(∞,1)-category]]. An **orthogonal factorization system** on $C$ is a pair $(S_L, S_R)$ of [[class]]es of [[morphism]]s in $C$ that satisfy the following axioms.

1. Both classes are stable under [[retract]]s.

1. Every morphism in $S_L$ is left orthogonal to every morphism in $S_R$;

1. For every morphism $h : X \to Z$ in $C$ there exists a commuting triangle

   $$
     \array{
        && Y
        \\
        & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{g}}
        \\
       X &&\stackrel{h}{\to}&& Z
     }
   $$

   with $f \in S_L$ and $g \in S_R$.

=--

## Properties

### Closure properties
 {#ClosureProperties}

\begin{proposition}
\label{RightClassStableUnderLimitsInArrowCategory}
For $(L,R)$ a factorization system in an [[(∞,1)-category]] $\mathcal{C}$, the [[full sub-(∞,1)-category]] of the [[arrow category]] $Func(\Delta^1, \mathcal{C})$ on the morphisms in $R$ is closed under [[(∞,1)-limits]] of shapes that exist in $\mathcal{C}$. [[formal duality|Dually]], the full subcategory on $L$ is closed under [[(∞,1)-colimits]] that exist in $\mathcal{C}$.
\end{proposition}
([Lurie 2009, prop. 5.2.8.6 (7), (8)](#Lurie))

In fact:
\begin{proposition}
\label{RightClassReflectiveInArrowCategory}
The [[full sub-(infinity,1)-category|full sub-$\infty$-category]] of the [[arrow category]] on the right class is a [[reflective sub-(infinity,1)-category|reflective sub-$\infty$-category]]
$$
  \big(\mathcal{C}^{\Delta[1]}\big)_R
  \underoverset
    {\underset{}{\hookrightarrow}}
    {\overset{}{\longleftarrow}}
    {\;\; \bot \;\;}
  \mathcal{C}^{\Delta[1]}
$$

Moreover, the [[unit of an adjunction|adjunction units]] 
$\eta_f \colon f \to \bar f$ are of the form

$$
  \array{
     X &\stackrel{\in L}{\longrightarrow}& \bar X
     \\
     {}^{\mathllap{f}}
     \big\downarrow 
     && 
     \big\downarrow{}^{\mathrlap{\bar f \in R} }
     \\
     Y &\stackrel{\simeq}{\longrightarrow}& \bar Y
  }
  \,.
$$
(In words: the reflection into $\big(\mathcal{C}^{\Delta[1]}\big)_R$ is given by the factorization in $(L,R)$.)
\end{proposition}
([Lurie 2009, Lemma 5.2.8.19](#Lurie))




## Examples

* In an [[(∞,1)-topos]] the classe of [[n-connected]] and that of [[n-truncated]] morphisms form an orthogonal factorization system, for all $(-2) \leq n \leq \infty $. 

  See [[(n-connected, n-truncated) factorization system]].


## Related concepts

* [[factorization system]]

  * [[weak factorization system]]

  * [[orthogonal factorization system]]

* [[factorization system in a 2-category]]

* [[factorization system in an (∞,1)-category]]

  * **orthogonal factorization system in an (∞,1)-category**

  * [[orthogonal factorization system in a derivator]].

  * [[homotopy factorization system in a model category]]

## References

Section 5.2.8 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

Formalization in [[homotopy type theory]] is discussed in 

* [[Egbert Rijke]], _Orthogonal factorization in HoTT_, talk at IAS, January 24, 2013 ([video](http://video.ias.edu/1213/univalent/0124-EgbertRijke))

[[!redirects orthogonal factorization system in an (∞,1)-category]]

[[!redirects factorization system in an (∞,1)-category]]
[[!redirects factorization system in an (infinity,1)-category]]

[[!redirects factorization system in an infinity1-category]]
[[!redirects orthogonal factorization system in an infinity1-category]]
