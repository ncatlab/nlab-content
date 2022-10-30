
<div class="rightHandSide toc">
[[!include enriched category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In a [[closed monoidal category]] $C$ the [[tensor product]] $a \otimes b$ and [[internal hom]] $[b,c]$ are related by the defining [[natural isomorphism]]

$$
  C(a \otimes b, c) \simeq C(a, [b,c])
  \,.
$$

The notion of **copowering** generalizes this to the situation where a category $C$ does not act on itself by tensors, but where another category $V$ acts on $C$.

The dual notion is that of [[power]]ing.

## Definition 

Let $V$ be a [[closed monoidal category|closed]] [[symmetric monoidal category]].  In a $V$-[[enriched category]] $C$, the **copower** of an object $x\in C$ by an object $k\in V$ is an object $k\odot x \in C$ with a [[natural isomorphism]]

$$
  C(k\odot x, y) \cong V(k, C(x,y))
$$

where $C(-,-)$ is the $V$-valued [[hom-functor]] of $C$ and $V(-,-)$ is the [[internal hom]] of $V$.

## Terminology

Copowers are frequently called _tensors_ and a $V$-category having all copowers is called _tensored_, while the word "copower" is reserved for the case $V=Set$.  However, there seems to be no good reason for making this distinction.  Moreover, the word "tensor" is fairly overused, and unfortunate since a tensor (= a copower) is a colimit, while a cotensor (= [[power]]) is a limit.


## Properties

* In the $V$-category $V$, the copower is just the [[tensor product]] of $V$.

* Copowers are a special sort of [[weighted limit|weighted colimit]].  Conversely, all weighted colimits can be constructed from copowers together with [[conical colimit]]s.  The dual  limit notion of a copower is a [[power]].


## Examples

* Every [[locally small category]] $C$ with all [[coproduct]]s is canonically copowered over [[Set]]: the copowering functor

  $$
    \otimes : Set \times C \to C
  $$

  sends $(S,b)$ to $|S|$-many copies of $b \in C$:

  $$
    S \otimes b := \coprod_{s \in S} b
    \,.
  $$

  The defining natural isomorphism in this situation is then just the fact that the [[hom functor]] sends colimits in its first argument to limits:

  $$
    C(\coprod_{s \in S} b , c)
    \simeq
    \prod_{s \in S} C(b,c)
    \simeq
    Set(S, C(b,c))
    \,.
  $$



## In higher category theory

The notion of copowering has evident analogs in [[higher category theory]].

For the notion of copowering in [[(∞,1)-category theory]] see the section <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring">Tensoring</a> at [[limit in a quasi-category]].