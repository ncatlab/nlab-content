
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A __pseudonatural transformation__ is a [[lax natural transformation]] whose $2$-cell components are all [[equivalence|invertible]].  

## Definition

+-- {: .num_defn} 
######Definition 

Given two [[2-functors]] $U, V: S \stackrel{\to}{\to} C$ between [[2-categories]], a **pseudonatural transformation** $\phi: U \to V$ is a rule that assigns to each [[object]] $s$ of $S$ a [[morphism]] $\phi(s): U(s) \to V(s)$ of $C$, and to each [[morphism]] $f: r \to s$ of $S$ an [[equivalence|invertible]] [[2-morphism]] $\phi(f)$ of $C$:  

$$
\array{
U(r) & \stackrel{U(f)}{\to} & U(s) \\
\phi(r) \downarrow & \phi(f) \swArrow & \downarrow \phi(s) \\
V(r) & \underset{V(f)}{\to} & V(s)
}
$$ 

such that the following [[coherence law]]s are satisfied in  $C$ (throughout we leave the [[associator]]s and [[unitor]]s in $C$ implicit):

1. respect for composition: for all composable morphisms $r \stackrel{f}{\to} s \stackrel{g}{\to} t$ in $S$ we have an equality

   $$
   \array{
      && U(s)
      \\
      & {}^{\mathllap{U(f)}}\nearrow &\downarrow^{\phi(s)}& \searrow^{\mathrlap{U(g)}}
      \\
     U(r) &\swArrow_{\phi(f)}&V(s) &\swArrow_{\phi(g)}& U(t)
     \\
     {}^{\mathllap{\phi(r)}}\downarrow &{}^{V(f)}\nearrow& 
      \Downarrow^{V(f,g)}
     &\searrow^{V(g)}& \downarrow^{\mathrlap{\phi(t)}} 
     \\
     V(r) &&\underset{V( g\circ f)}{\to}&& V(s)
   }
    \;\;\;
    =
    \;\;\;
   \array{
     && U(s)
     \\
     & {}^{\mathllap{U(f)}}\nearrow &\Downarrow^{U(f,g)}& \searrow^{\mathrlap{U(g)}}
     \\
     U(r) &&\stackrel{U(g \circ f)}{\to}&& U(t)
     \\
     {}^{\mathllap{\phi(r)}}\downarrow && 
       \swArrow_{\phi(g \circ f )}
     && \downarrow^{\mathrlap{\phi(t)}}
     \\
     V(r) &&\underset{V(g \circ f)}{\to}&& V(t)
   }
     \,,
   $$

   of [[pasting]] [[2-morphisms]] as indicated, where $U(f,g)$ and $V(f,g)$ denote the compositors of the [[2-functor]]s $U$ and $V$,

1. respect for units, (...)

1. naturality

   for every [[2-morphism]] 

   $$
     \array{
        && \stackrel{f}{\to}
        \\
        & \nearrow && \searrow
        \\
        r &&\Downarrow^{F}&& s
        \\
        & \searrow && \nearrow
        \\
        && \underset{g}{\to}
     }
   $$

   in $S$ an equality

   $$
     \array{
        && \stackrel{U(f)}{\to}
        \\
        & \nearrow &\Downarrow^{U(F)}& \searrow
        \\
        U(r) &&\stackrel{U(g)}{\to}&& U(s)
        \\
        {}^{\mathllap{\phi(r)}}\downarrow &&\swArrow_{\phi(g)}&& \downarrow^{\mathrlap{\phi(s)}}
        \\
        V(r) &&\underset{V(g)}{\to}&& V(s)
     }
     \;\;\;
       =
     \;\;\;
     \array{
       U(r) &&\stackrel{U(f)}{\to}&& U(s)
       \\
       {}^{\mathllap{\phi(r)}}\downarrow &&\swArrow_{\phi(f)}&& \downarrow^{\mathrlap{\phi(s)}}
       \\
       V(r) &&\stackrel{V(f)}{\to}&& V(s)
       \\
       & \searrow &\Downarrow^{V(F)}& \nearrow
       \\
       && \underset{V(g)}{\to}
     }
   $$

   in $C$.

=-- 

A pseudonatural transformation is called a **pseudonatural equivalence** if each component $\phi(s)$ is an [[equivalence]] in the 2-category $C$.  This is equivalent to $\phi$ itself being an equivalence in the 2-category $[S,C]$ of 2-functors, pseudonatural transformations, and [[modifications]].

## Related concepts

* [[homotopy]]

* [[transfor]]

  * [[natural transformation]]

    * [[dinatural transformation]], [[extranatural transformation]]

  * **pseudonatural transformation**

  * [[lax natural transformation]]

## References for the globular approach

[[Camell Kachour]]*: Kamel Kachour, D&#233;finition alg&#233;brique des cellules non-strictes, Cahiers de Topologie et de G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;gorique (2008), volume 1, pages 1&#8211;68.

[[Camell Kachour]]*: Steps toward the Weak &#969;-category of the Weak &#969;-categories in the globular setting, Published in : Categories and General Algebraic Structures with Applications (2015).

[[!redirects pseudonatural transformation]]
[[!redirects pseudonatural transformations]]
[[!redirects pseudo-natural transformation]]
[[!redirects pseudo-natural transformations]]
[[!redirects pseudo natural transformation]]
[[!redirects pseudo natural transformations]]
[[!redirects pseudonatural equivalence]]
[[!redirects pseudonatural equivalences]]
[[!redirects pseudo-natural equivalence]]
[[!redirects pseudo-natural equivalences]]
[[!redirects pseudo natural equivalence]]
[[!redirects pseudo natural equivalences]]