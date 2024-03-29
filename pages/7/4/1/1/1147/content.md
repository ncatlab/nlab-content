
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

This entry is about special properties of [[functor]]s on [[comma category|comma categories]]. See also [[category of presheaves]].


# Contents
* automatic table of contents goes here
{: toc}

## Presheaves on over-categories and over-categories of presheaves

Let $C$ be a [[category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. Write
$PSh(C/c) = [(C/c)^{op}, Set]$ for the category of [[presheaf|presheaves]] on $C/c$ and write
$PSh(C)/Y(c)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(C)$ is the [[Yoneda embedding]]. 

+-- {: .un_prop}
###### Proposition

There is an [[equivalence]] of categories

$$
  e : PSh(C/c) \stackrel{\simeq}{\to} PSh(C)/Y(c)
  \,.
$$

=--


+-- {: .proof}
###### Proof

The functor $e$ takes $F \in PSh(C/c)$ to the presheaf
$F' : d \mapsto \sqcup_{f \in C(d,c)} F(f)$ which is equipped with the natural transformation $\eta : F' \to Y(c)$ with component map 

$$
  \eta_d : \sqcup_{f \in C(d,c)} F(f) \to C(d,c)
  : ((f \in C(d,c), \theta \in F(f)) \mapsto f
  \,.
$$

A weak inverse of $e$ is given by the functor 
$$
  \bar e : PSh(C)/Y(c) \to PSh(C/c)
$$
which sends $\eta : F' \to Y(c)$ to $F \in PSh(C/c)$ given by
$$
  F : (f : d \to c) \mapsto F'(d)|_c
  \,,
$$
where $F'(d)|_c$ is the [[pullback]]
$$
  \array{
     F'(d)|_c &\to& F'(d)
     \\
     \downarrow && \downarrow^{\eta_d}
     \\
     pt &\stackrel{f}{\to}& C(d,c)
  }
  \,.
$$ 

=--

+-- {: .un_lemma}
###### Example


Suppose the presheaf $F \in PSh(C/c)$ does not actually depend on the morphsims to $c$, i.e. suppose that it factors through the forgetful functor from the [[over category]] to $C$:
$$
  F : (C/c)^{op} \to C^{op} \to Set
  \,.
$$

Then
$
  F'(d) = \sqcup_{f \in C(d,c)} F(f)
  = \sqcup_{f \in C(d,c)} F(d)
  \simeq
  C(d,c) \times F(d) 
$
and hence $F ' = Y(c) \times F$ with respect to the [[closed monoidal structure on presheaves]].

=--

See [[over-topos]] for more.


## Over-categories of presheaf categories and presheaves on categories of elements

Generalizing the above,

+-- {: .un_prop}
###### Proposition

For every $P \colon \mathbf{Set}^D$, there is an [[equivalence]] of categories

$$
  \varphi : \mathbf{Set}^{el(P)} \stackrel{\simeq}{\to} \mathbf{Set}^D / P
  \,.
$$

where $el(P) = \ast / P$ is the [[category of elements]] of $P$.
=--

+-- {: .proof}
###### Proof

The construction is completely analogous to the above; Given $F \colon \mathbf{Set}^{el(P)}$, $\varphi(F)$ is defined pointwise as a coproduct:
$$
  \varphi(F)(c) = \coprod_{(x,Pc)} F(x,Pc)
$$
where $(x,Pc) = (\ast \stackrel{x}{\to} Pc)$ is an object of $el(P)$. The action on morphisms is defined analogously. This comes equipped with a natural transformation $\alpha \colon \varphi(F) \to P$, with component
$$
  \array{
    \alpha_c \colon \varphi(F)(c) \to Pc          \\
    \alpha_c(F(x,Pc)) = x \in Pc                  \\
  }
$$
Given an object $(Q \stackrel{\alpha}{\to} P)$ of $\mathbf{Set}^D / P$ the action of a weak inverse $\bar \varphi$ can be specified as $ \bar{\varphi}(\alpha)(x,Pc) = \alpha_c^{-1}(x)$, that is, the wedge of the pullback:
$$ 
  \array{
     \bar{\varphi}(\alpha)(x,Pc) &\to& Qc
     \\
     \downarrow && \downarrow^{\alpha_c}
     \\
     pt &\stackrel{x}{\to}& Pc
  }
  \,.
$$
The action of $\bar{\varphi}(\alpha)$ on arrows of $el(P)$, functoriality, etc is derived from its definition as a pullback and the def of morphisms in $el(P)$. 

=--


### Relationship with the over-categories statement

Putting $D = C^{op}, P = Y(c)$ in the above yields:
$$
  \mathbf{Set}^{el(Y(c))} \simeq \mathbf{Set}^D / Y(c)
$$
Now it is easy to see that $el(Y(c)) \simeq (C / c)^{op}$; we get then:
$$
  \mathbf{Set}^{(C / c)^{op}} \simeq \mathbf{Set}^{C^{op}} / Y(c)
$$


## In higher category theory

For the analogous result in the context of [[(∞,1)-category]] theory see
<a href="http://ncatlab.org/nlab/show/(infinity%2C1)-category+of+(infinity%2C1)-presheaves#WithOvercategories">(∞,1)-Category of (∞,1)-presheaves -- Interaction with overcategories</a>


## Related concepts

* [[comma category]]

* [[presheaf]]
