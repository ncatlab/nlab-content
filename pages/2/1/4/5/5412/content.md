
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $\mathcal{T}$ a [[topos]] and $X \in \mathcal{T}$ any [[object]] the [[over category]] $\mathcal{T}/X$ is itself a topos: the [[little topos]] incarnation of $X$.

## Properties

### Etale geometric morphism

+-- {: .un_prop}
###### Proposition

For $\mathcal{T}$ a [[Grothendieck topos]] and $X \in \mathcal{T}$ any object, the canonical projection functor $X_! : \mathcal{T}/X \to X$ is part of an [[essential geometric morphism]]

$$
  (X_! \dashv X^* \dashv X_*)
  : 
  \mathcal{T}/X \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
  \mathcal{T}
  \,.
$$

=--

+-- {: .proof}
###### Proof

One see that the functor $X^*$ is given by taking the [[product]] with $X$:

$$
  X^* : K \mapsto (p_2 : K \times X \to X)
  \,,
$$

since [[commuting diagram]]s

$$
  \array{
    A &&\to&& K \times X
    \\
    & \searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
$$

are evidently uniquely specified by their components $A \to K$.

Moreover, since in the Grothendieck topos $\mathcal{T}$ we have [[universal colimits]], it follows that $(-) \times X$ preserves all [[colimit]]s. Therefore by the [[adjoint functor theorem]] a further [[right adjoint]] $X_*$ exists. 

=--


+-- {: .un_defn}
###### Definition

A [[geometric morphism]] $\mathcal{E} \to \mathcal{T}$ equivalent to one of the form $(X_! \dashv X^* \dashv X_*)$ is called an
**[[etale geometric morphism]]** .

=-- 


### Presheaf over-topos

We discuss special properties of over-[[presheaf toposes]].

Let $C$ be a [[small category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. 

Write

* $PSh(C/c) = [(C/c)^{op}, Set]$ for the [[category of presheaves]] on $C/c$ 

* and write $PSh(C)/Y(y)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(c)$ is the [[Yoneda embedding]]. 

+-- {: .un_prop}
###### Proposition

There is an [[equivalence of categories]]

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



## Related concepts

* **over-topos**

* [[over-(∞,1)-topos]]

[[!redirects over topos]]
[[!redirects over toposes]]
[[!redirects over-toposes]]