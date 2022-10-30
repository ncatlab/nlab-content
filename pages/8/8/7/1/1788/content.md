
+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

***


#Contents#
* table of contents
{:toc}


### Homotopy type theory


Consider $\mathbf{H}$ an [[(∞,1)-topos|∞-topos]], 
that is and [[(∞,1)-category of (∞,1)-sheaves]]/[[∞-stacks]]

$$
  \mathbf{H} \simeq Sh_\infty(C)
$$

For instance $C = $ [[CartSp]]$_{synth}$ then $\mathbf{H} = $ [[SynthDiff∞Grpd]]. 

Write $Type \in \mathbf{H}$ for the internal [[universe]] of small objects, the [[object classifier]]

+-- {: .num_defn }
###### Definition

$Type$ is the [[representable functor|representing object]]
for the [[core]] of the [[small object|small]] [[codomain fibration]].

=--

The corresponding equivalence

$$
  name
  :
  Core(\mathbf{H}_{/X})^{small} \stackrel{\simeq}{\to} \mathbf{H}(X,Type)
$$

sends an $X$-family of objects to its "name":


$(E \to X) \in \mathbf{H}_{/X}$ maps to 

$$
  X \stackrel{\vdash E}{\to} Type
$$

defined by [[(∞,1)-pullback|∞-pullback]]

$$
  \array{
     E &\to& \widehat{Type}
     \\
     \downarrow && \downarrow
     \\
     X &\underset{\vdash E}{\to}& Type
  }
$$



$$
  x : X \vdash E(x) : Type
$$

**morphisms to sequents.**


| $\,$ | [[types]] | [[terms]] |
|--|--|--|
| [[(∞,1)-topos theory|∞-topos theory]] | $\;\;\;\;X \stackrel{\vdash \;\;\;\;E}{\to} \;\;\Type$ | $\;\;\;\;X \stackrel{\vdash \;\;\;t}{\to} {}_X \;\;E$ |
|[[homotopy type theory]] | $x : X \vdash E(x) : Type$ | $x : X \vdash t(x) : E(x) $ |

### The Theorem

Let 

$$
  \nabla : \mathbf{B}\mathbb{G}_{conn}
  \vdash
  X(\nabla) : Type
$$

be a [[circle n-bundle with connection]], here to be thought of 
as a _[[prequantum n-bundle]]_.

Then 

$$
  \nabla : \mathbf{B}^n \mathb{G}_{conn}
  \vdash
  X(\nabla) \stackrel{\simeq}{\to} X(\nabla)
  : Type
$$

is the cohesive [[quantomorphism n-group]].



### Groups

$$
  Gpr(\mathbf{H}) \simeq $\mathbf{H}^{*/}_{\geq 1}$
$$

$$
  \mathbf{B}\mathbf{Aut}(\Sigma)
   \coloneqq 
   \;
  \vdash image(\vdash \Sigma) : Type
$$

$$
  \mathbf{Act}_{\mathbf{H}}(G) = \mathbf{H}_{/\mathbf{B}G}
$$

$$
  * : \mathbf{B}G \vdash V : Type
$$



the canonical action of $\mathbf{Aut}(\Sigma)$ is

$$
  \Sigma : \mathbf{B}\mathbf{Aut}(\Sigma)
  \vdash 
  \Sigma : Type
$$

which interprets to

$$
  \array{
    \Sigma &\to& \Sigma\sslash \mathbf{Aut}(\Sigma) &\to& \widehat{Type}
    \\
    && \downarrow && \downarrow
    \\
    && \mathbf{B}\mathbf{Aut}(\Sigma) &\hookrightarrow& Type
  }
$$


for $(X \stackrel{f}{\to} Y) \in \mathbf{H}^{\Delta^1}$

[[dependent sum]] $\dashv$ [[base change]] $\dashv$ [[dependent product]]

$$
  (\sum_f \dashv f^* \dashv \prod_f)
   :
  \mathbf{H}_{/X}
    \stackrel{\overset{\sum_f}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{\prod_f}{\to}}}
  \mathbf{H}_{/Y}
$$



Invariants =  $\vdash \prod_{* : \mathbf{B}G} V : Type$


[[locally cartesian closed (∞,1)-category]]

[[internal hom]] in $\mathbf{H}_{/\Gamma}$ is, by definition, again in the slice

$(E \stackrel{e}{\to} X)$, $(F \stackrel{f}{\to} X)$

$$
  \array{
    [e,f] &\to& \widehat{Type}
    \\
    \downarrow && \downarrow
    \\
    \Gamma &\underset{\vdash E(x) \to F(x)}{\to}& Type
  }
$$

$$
  x : \Gamma \vdash E(x) \to F(x) : Type
$$

**Example**

An [[atlas]] is

$$
  x : X \vdash U(x) : Type
$$

such that

$$ 
  \vdash isAtlas : \prod_{x : X} isInhabited(U(x)) 
$$

**Example**

Space of _bisections_ of a Lie groupoid $X$ with objects $U$

$$
  \vdash \prod_{x : X} U(x) \stackrel{\simeq}{\to} U(x) : Type
$$

**Example**

Conjugation action on $[V_1,V_2]$ is

$$
  * : \mathbf{B}G \vdash V_1 \to V_2 : Type
$$

Example: $\mathbf{H} = $ [[Smooth∞Grpd]] $= Sh_\infty(SmthMfd=)$

$\mathbf{orth} : \mathbf{B} O(n) \to \mathbf{B} GL(n)$

$\Sigma : Type$ a smooth manifold

$$
  * : \mathbf{B} GL(n) \vdash T \Sigma\to \mathbf{orth}
$$

is moduli stack of vielbein fields on $\Sigma$ = Riemannian metric on $\Sigma$.

$$
  * : \mathbf{B} GL(n), \Sigma : \mathbf{B}\mathbf{Aut}(\sigma)
  \vdash
  T \Sigma \to \mathbf{orth}
$$

is generally covariant moduli of vielbein fields, hence 
Lie integrated BRST complex of general relativity: $\pi_1$
is integrated diffeomorphisms ghosts

Example

$$
  * : \mathbf{B} U(1) \vdash \mathbb{C} : Type
$$

defining representation

for

$$
  \mathbf{c}_1 : \mathbf{B} U(1) \vdash X(\mathbf{c}_1) : Type
$$

circle bundle

then 

$$
  \vdash \prod_{\mathbf{c}_1 : \mathbf{B} U(1)} X(\mathbf{c}_1) \to \mathbb{C} : Type
$$

is space of smooth sections of the associated complex line bundle

**Example**

$$
  * : \mathbf{B}^2 U(1) \vdash \mathbf{B}U(n) : Type
$$

is canonical action of $\mathbf{B}U(1)$, then for

$$
  * : \mathbf{B}^2 U(1) \vdash (X, \mathbf{DD}_1) : Type
$$

a B-field instanton configuration with [[Dixmier-Douady class]] $\mathb{DD}_1$ on $X$, then

$$
  \vdash \prod_{* : \mathbf{B}^2 U(1)} (X,\mathbf{DD}) \to \mathbf{B}U(n)  : Type
$$

is moduli stack of $\mathbf{DD}$-twisted $U(n)$-[[twisted bundles]]


cohesion in $\mathbf{H}$:

$$
  X : Type \vdash \sharp X : Type
$$

$$
  X : Type : ResolveCohesion : X \to \sharp X 
$$

$$
  X : Type : \Pi X : Type
$$

$$
  X : Type : IncludeConstantPaths : X \to \Pi X
$$

(...)


prequantum $n$-bundle

$$
  \nabla : \mathbf{B}^n \mathbb{G}_{conn}
  \vdash
  X(\nabla) : Type
$$

quantomorphism $n$-group

$$
  \mathbf{QuantMorph}_{X(\nabla)}
  \coloneqq
  \;\;\;
  \vdash 
  \prod_{\nabla : \mathbf{B}^n \mathbb{G}_n}
  X(\nabla) 
     \stackrel{\simeq}{\to}
  X(\nabla)
  : Type
$$

Lie differentiation

$$
  i_{inf} :  FormalPoints \hoookrightarrow CartSp_{synth}
$$

$$
  i_{inf}^* 
  :
  Sh_{\infty}(CartSp_{synth})^{*}_{\geq 1}
  Sh_\infty(FormalPoints)^{*}_{\geq 1}
  \simeq
  L_\infty
$$


***


category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects ??? ????]]
[[!redirects Featured math : Quora]]
