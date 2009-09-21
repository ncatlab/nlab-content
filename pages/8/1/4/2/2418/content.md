+-- {: .standout}

This is a sub-entry of [[geometric models for elliptic cohomology]] and [[A Survey of Elliptic Cohomology]] 

See there for background and context.

=--


> **raw material**: this are notes taken more or less verbatim in a seminar -- needs polishing


Previous:

* [[Axiomatic field theories and their motivation from topology]].

* [[(1,1)-dimensional Euclidean field theories and K-theory]]


recall the big diagram from the end of the [[(1,1)-dimensional Euclidean field theories and K-theory|previous entry]].

The **goal** now is to replace everywhere [[topological K-theory]] by [[tmf]].


previously we had assumed that $X$ has [[string structure]]. Now we assume [[String structure]].

So we are looking for a diagram of the form


$$
  \array{
    1
    && 
    (2|1)EFT^0(X)/\sim
    && \stackrel{\simeq conjectural}{\leftarrow}&&
    tmf^0(X)
    && \ni 1
    \\
    \downarrow && \downarrow^{quantization}
    &&&&
    \downarrow^{\int_X}
    &&
    \downarrow
    \\
    \sigma_{(2|1)(X)}&& (2|1)EFT^{-n}(X)/\sim
    &&\stackrel{\simeq conjectural }{\leftarrow}&&
    tmf^{-n}(pt)
    &&
    \\
    &\searrow & \searrow &&& \swarrow& \swarrow
    \\
    &&&& mf^{-n}
    \\
    &&&&
    index^{S^1}(D_{L X})
    = W(X)
  }
$$

the vertical maps here are due to various theorems by various people -- except for the "physical quantization" on the left, that is ued in physics but hasn't been formalized

the **horizontal maps are the conjecure we are after** in the Stolz-Teichner program: The top horizontal map will involve making the notion of $(2|1)$EFT _local_ by refining it to an _extended_ [[FQFT]]s. This will not be considered here.


we will explain the following items

* the [[ring]] $mf^\bullet$ of [[integral modular form]]s

  $$
    mf^\bullet \simeq \mathbb{Z}[c_4, c_6, \Delta, \Delta^{-1}]/(c_4^{3}- c_6^{2} - 1728 \Delta)
  $$

  one calls $w = -\frac{n}{2}$ the _weight_ . We have degree of $\Delta$ is $deg(\Delta) = -24$, hence $w(\Delta) = 12$.

* $W(X)$ is the [[Witten genus]]

  $$
    W(X) = \sum_{k \in \mathbb{Z}} a_k \cdot q^k
    \,,
    a_k \in \mathbb{Z}
  $$

  where $a_k = index(D_X \otimes E_k)$ where $E_k$ is some explicit vector bundle over $X$.

## modular forms ##

**definition** An **(integral) [[modular form]]** of weight $w$ is a [[holomorphic function]] on the [[upper half plane]]

$$
  f : (\mathbb{R}^2)_+ \hookrightarrow \mathbb{C}
$$

(complex numbers with strictly positive imaginary part) 

such that

1. if $A = \left( \array{a & b \\ c& d}\right) \in SL_2(\mathbb{Z})$ acting by $A : \tau \mapsto = \frac{a \tau + b }{c \tau + d}$ we have
 
   $$
     f(A(\tau)) = (c \tau + d)^w f(\tau)
   $$

   **note** take $A = \left( \array{1 & 1 \\ 0& 1}\right)$ then we get that $f(\tau + 1) = f(\tau)$

1. $f$ has at worst a pole at $\{0\}$ (for _weak_ modular forms this condition is relaxed)

   it follows that $f = f(q)$ with $q = e^{2 \pi i \tau}$ is a meromorphic funtion on the open disk.


1. **integrality** $\tilde f(q) = \sum_{k = -N}^\infty a_k \cdot q^k$ then $a_k \in \mathbb{Z}$

by this definition, modular forms are not relly functions on the upper half plane, but function on a [[moduli space]] of [[torus|tori]]. See the following definition:

if the weight vanishes, we say that modular form is a **[[modular function]]** .

**definition (2|1)-dim [[partition function]]** 

Let $E$ be an EFT

$$
  (2|1)EFT^0 \stackrel{S}{\to}
  2 EFT \ne E
$$

$$
  E \mapsto E_{red}
$$

then the [[partition function]] is the map $Z_E : \mathbb{C} \to \mathbb{R}$

$$
  Z_E : \tau \mapsto E_{red}(T_\tau)
$$

where

$$
  T_\tau := \mathbb{C}/{\mathbb{Z} \times \mathbb{Z} \cdot \tau}
$$

is thee standard torus of modulus $\tau$. 

then the central **theorem** that we are after here is

**therorem (Stolz-Teichner)** (after a suggestion by [[Edward Witten]])

There is a precise definition of $(2|1)$-EFTs $E$ such that the [[partition function]] $Z_E$ is an integral [[modular function]]

(so this is really four theorems: the function is holomorphic, integral, etc.)

moreover, every [[integral modular function]] arises in this way.