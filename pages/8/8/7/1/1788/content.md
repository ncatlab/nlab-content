
+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

***


$\mathbf{H}$ an [[(∞,1)-topos|∞-topos]] 

$$
  \mathbf{H} \simeq Sh_\infty(C)
$$

[[(∞,1)-category of (∞,1)-sheaves]]/[[∞-stacks]]

write $Type \in \mathbf{H}$ for the internal [[universe]] of small objects, the [[object classifier]]: defined as the representing object
for the core of the small [[codomain fibration]]:

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

an equivalent notion for this is 

$$
  x : X \vdash E(x) : Type
$$

Notation:

| [[(∞,1)-topos theory|∞-topos theory]] | [[homotopy type theory]] |
|--|--|
| $X \stackrel{\vdash E}{\to} Type$  |  $x : X \vdash E(x) : Type$ |


$$
  Gpr(\mathbf{H}) \simeq $\mathbf{H}^{*/}_{\geq 1}$
$$

**Definition: $GrpType : Type$

$$
  GrpdType =  \sum_{A : Type} isConnected(X) \times isInhabited(X)
$$

For instance for $\vdash \Sigma : Type$

$$
  \mathbf{B}\mathbf{Aut}(\Sigma) = Image(* \stackrel{\Sigma}{\to} Type)
$$

$$
  \mathbf{Act}_{\mathbf{H}}(G) = \mathbf{H}_{/\mathbf{B}G}
$$

$$
  * : \mathbf{B}G \vdash V : Type
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
  * : \mathbf{B} U(1) \vdash (X, \mathbf{c}_1) : Type
$$

circle bundle

then 

$$
  \vdash \prod_{* : \mathbf{B} U(1)} (X, \mathbf{c}_1) \to \mathbb{C} : Type
$$

is space of smooth sections of the associated complex line bundle

Example

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
