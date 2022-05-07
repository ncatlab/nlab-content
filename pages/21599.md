
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[smooth manifold]] $X$, by a _tangential structure_ one typically understands (e.g. [GMWT 09, Sec. 5](GMWT09)) a [[lift]] of the [[classifying map]] $X \overset{\vdash}{\longrightarrow} B GL(n)$ of its [[tangent bundle]]  through any prescribed [[map]] $B \overset{f}{\longrightarrow} B GL(n)$ into the [[classifying space]] of the [[general linear group]], up to [[homotopy]]:

$$
  \array{
    && B
    \\
    &  
    {}^{ 
      \mathllap{
        {tangential} \atop {structure} 
      }
    }\nearrow
    & \big\downarrow^{ f }
    \\
    X 
      &\underset{
        \vdash T X
      }{\longrightarrow}&
    B GL(n)
  }
$$

Since this is all considered (only) for [[homotopy types]] of topological spaces (e.g. via the [[classical model structure on topological spaces]]) and there is a [[weak homotopy equivalence]] $B GL(n) \simeq  B O(n)$ to the [[classifying space]] of the [[orthogonal group]] (the latter being the [[maximal compact subgroup]] of $GL(n)$), authors typically consider the equivalent diagram over $B O(n)$.

Beware that the same kind of lift but understood in [[differentiable stack|differentiable]] [[classifying stacks]] instead of just [[classifying spaces]] is a _[[G-structure]]_ as commonly understood bow (for $A = \mathbf{B}G$ is the classifying stack/[[delooping]] of a [[Lie group]] $G$). 



## Details


### In terms of $(B,f)$-structures 
 {#InTermsOfBfStructures}

+-- {: .num_defn #BfStructure}
###### Definition

A **$(B,f)$-structure** is 

1. for each $n\in \mathbb{N}$ a [[pointed topological space|pointed]] [[CW-complex]] $B_n \in Top_{CW}^{\ast/}$

1. equipped with a pointed [[Serre fibration]] 

   $$
     \array{
       B_n
       \\
       \downarrow^{\mathrlap{f_n}}
       \\
       B O(n)
     }
   $$

   to the [[classifying space]] $B O(n)$ ([def.](classifying+space#EOn));

1. for all $n_1 \leq n_2$ a pointed continuous function

   $\iota_{n_1, n_2} \;\colon\; B_{n_1} \longrightarrow B_{n_2}$

   which is the identity for $n_1 = n_2$;

such that for all $n_1 \leq n_2 \in \mathbb{N}$ these [[commuting square|squares commute]]

$$
  \array{
    B_{n_1} &\overset{\iota_{n_1,n_2}}{\longrightarrow}& B_{n_2}
    \\
    {}^{\mathllap{f_{n_1}}}\downarrow && \downarrow^{\mathrlap{f_{n_2}}}
    \\
    B O(n_1) &\longrightarrow& B O(n_2)
  }
  \,,
$$

where the bottom map is the canonical one ([def.](classifying+space#InclusionOfBOnIntoBOnPlusOne)).

The $(B,f)$-structure is **multiplicative** if it is moreover equipped with a system of maps $\mu_{n_1,n_2} \colon B_{n_1}\times B_{n_2} \to B_{n_1 + n_2}$ which cover the canonical multiplication maps ([def.](classifying+space#WhitneySumMapOnClassifyingSpaces))

$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{\mu_{n_1, n_2}}{\longrightarrow}&
    B_{n_1 + n_2}
    \\
    {}^{\mathllap{f_{n_1} \times f_{n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{f_{n_1 + n_2}}}
    \\
    B O(n_1) \times B O(n_2)
     &\longrightarrow&
    B O(n_1 + n_2)
  }
$$
 
and which satisfy the evident [[associativity]] and [[unitality]], for $B_0 = \ast$ the unit, and, finally, which commute with the maps $\iota$ in that all $n_1,n_2, n_3 \in \mathbb{N}$ these squares commute:


$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{id \times \iota_{n_2,n_2+n_3}}{\longrightarrow}&
    B_{n_1} \times B_{n_2 + n_3}
    \\
    {}^{\mathllap{\mu_{n_1, n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{n_1,n_2 + n_3}}}
    \\
    B_{n_1 + n_2}
      &\underset{\iota_{n_1+n_2, n_1 + n_2 + n_3}}{\longrightarrow}&
    B_{n_1 + n_2 + n_3}
  }
$$

and

$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{\iota_{n_1,n_1+n_3} \times id}{\longrightarrow}&
    B_{n_1+n_3} \times B_{n_2 }
    \\
    {}^{\mathllap{\mu_{n_1, n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{n_1 + n_3 , n_2}}}
    \\
    B_{n_1 + n_2}
      &\underset{\iota_{n_1+n_2, n_1 + n_2 + n_3}}{\longrightarrow}&
    B_{n_1 + n_2 + n_3}
  }
  \,.
$$


Similarly, an **$S^2$-$(B,f)$-structure** is a compatible system

$$
  f_{2n} \colon B_{2n} \longrightarrow B O(2n)
$$

indexed only on the even natural numbers.

Generally, an **$S^k$-$(B,f)$-structure** for $k \in \mathbb{N}$, $k \geq 1$ is a compatible system

$$
  f_{k n} \colon B_{ k n} \longrightarrow B O(k n)
$$

for all $n \in \mathbb{N}$, hence for all $k n \in k \mathbb{N}$.

=--

([Lashof 63](#Lashof63), [Stong 68, beginning of chapter II](#Stong68), [Kochman 96, section 1.4](#Kochman96))

See also at _[[B-bordism]]_.


+-- {: .num_example #ExamplesOfBfStructures}
###### Example

Examples of $(B,f)$-structures (def. \ref{BfStructure}) include the following:

1. $B_n = B O(n)$ and $f_n = id$ is **orthogonal structure** (or "no structure");

1. $B_n = E O(n)$ and $f_n$ the [[universal principal bundle]]-projection is **[[framing]]-structure**;

1. $B_n = B SO(n) = E O(n)/SO(n)$ the classifying space of the [[special orthogonal group]] and $f_n$ the canonical projection is **[[orientation]] structure**;

1. $B_n = B Spin(n) = E O(n)/Spin(n)$ the classifying space of the [[spin group]] and $f_n$ the canonical projection is **[[spin structure]]**.

Examples of $S^2$-$(B,f)$-structures include

1. $B_{2n} = B U(n) = E O(2n)/U(n)$ the classifying space of the [[unitary group]], and $f_{2n}$ the canonical projection is **[[almost complex structure]]**.

=--


+-- {: .num_defn }
###### Definition

Given a [[smooth manifold]] $X$ of [[dimension]] $n$, and given a $(B,f)$-structure as in def. \ref{BfStructure}, then a **$(B,f)$-structure on the manifold** is an [[equivalence class]] of the following structure:

1. an [[embedding]] $i_X \; \colon \; X \hookrightarrow \mathbb{R}^k$ for some $k \in \mathbb{N}$;

1. a [[homotopy class]] of a  [[lift]] $\hat g$ of the classifying map $g$ of the [[tangent bundle]] 

   $$
     \array{
       && B_{n}
       \\
       &{}^{\mathllap{\hat g}}\nearrow& \downarrow^{\mathrlap{f_n}}
       \\
       X &\overset{g}{\longrightarrow}& B O(n)
     }
     \,.
   $$

The equivalence relation on such structures is to be that generated by the relation $((i_{X})_1, \hat g_1) \sim ((i_{X})_,\hat g_2)$ if 

1. $k_2 \geq k_1$

1. the second inclusion factors through the first as 

   $$
     (i_X)_2 
       \;\colon\; 
     X 
       \overset{(i_X)_1}{\hookrightarrow}
     \mathbb{R}^{k_1} 
       \hookrightarrow
     \mathbb{R}^{k_2}
   $$

1. the lift of the classifying map factors accordingly (as homotopy classes)

   $$
     \hat g_2
       \;\colon\;
     X 
       \overset{\hat g_1}{\longrightarrow}
     B_{n}
       \longrightarrow
     B_{n}
     \,.
   $$

=--

## Examples

The tangential structures corresponding to lifts through the [Whitehead tower of the orthogonal group](Whitehead+tower#OfTheOrthogonalGroup)


* [[orientation]]

* [[spin structure]]

* [[string structure]]

* [[fivebrane structure]]

* ...

* [[framing]]


## References


The concept of tangential structure originates with [[cobordism theory]], originally under the name _$(B,f)$-structures_:
 
* {#Lashof63} [[Richard Lashof]], _Poincar&#233; duality and cobordism_, Trans. AMS 109 (1963), 257-277 ([doi:10.1090/S0002-9947-1963-0156357-4](https://doi.org/10.1090/S0002-9947-1963-0156357-4))

* {#Stong68} [[Robert Stong]], beginning of chapter II of: _Notes on Cobordism theory_, 1968,

  reprinted as: Princeton Legacy Library, Princeton University Press 2016 ([ISBN:9780691649016](http://press.princeton.edu/titles/6465.html), [toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf))

* {#Kochman96} [[Stanley Kochman]], section 1.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

The terminology "tangential structure" became popular around

* {#GMWT09} [[Søren Galatius]], [[Ib Madsen]], [[Ulrike Tillmann]],[[Michael Weiss]], Section 5 of: _The homotopy type of the cobordism category_, Acta Math. 202 (2009), no. 2, 195--239 ([arXiv:math/0605249](http://arxiv.org/abs/math/0605249))

[[!redirects tangential structures]]

[[!redirects (B,f)-structure]]
[[!redirects (B,f)-structures]]




