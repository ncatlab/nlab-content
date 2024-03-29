
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _chain map_ is a [[homomorphism]] of [[chain complexes]]. 
Chain complexes with chain maps between them form the [[category of chain complexes]].

## Definition

Let $V_\bullet, W_\bullet \in Ch_\bullet(\mathcal{A})$ be two  [[chain complexes]] in some ambient [[additive category]] $\mathcal{A}$ (often assumed to be an [[abelian category]]). 


+-- {: .num_defn}
###### Definition

A **chain map** $f : V_\bullet \to W_\bullet$ is a collection of [[morphism]] $\{f_n : V_n \to W_n\}_{n \in \mathbb{Z}}$ in $\mathcal{A}$ such that all the [[diagrams]]

$$
  \array{
    V_{n+1} &\stackrel{d^V_n}{\to}& V_n
    \\
    \downarrow^{\mathrlap{f_{n+1}}} 
    &&
    \downarrow^{\mathrlap{f_{n}}} 
    \\
    W_{n+1} &\stackrel{d^W_n}{\to} & W_n
  }
$$ 

[[commuting diagram|commute]], hence such that all the [[equations]]

$$
  f_n \circ d^V_n = d^W_{n} \circ f_{n+1}
$$

hold.

=--

+-- {: .num_remark}
###### Remark

A chain map $f$ induces for each $n \in \mathbb{Z}$ a morphism $H_n(f)$ on [[homology groups]], see prop. \ref{OnHomology} below. If these are all [[isomorphisms]], then $f$ is called a _[[quasi-isomorphism]]_.

=--

## Properties

### On homology
 {#OnHomology}

+-- {: .num_prop #OnHomology}
###### Proposition

For $f : C_\bullet \to D_\bullet$ a chain map, it respects [[boundaries]] and [[cycles]], so that for all $n \in \mathbb{Z}$ it restricts to a morphism

$$
  B_n(f) : B_n(C_\bullet) \to B_n(D_\bullet)
$$

and

$$
  Z_n(f) : Z_n(C_\bullet) \to Z_n(D_\bullet)
  \,.
$$

In particular it also respects [[chain homology]]

$$
  H_n(f) : H_n(C_\bullet) \to H_n(D_\bullet)
  \,.
$$

=--

+-- {: .num_cor}
###### Corollary

Conversely this means that taking [[chain homology]] is a [[functor]]

$$
  H_n(-) : Ch_\bullet(\mathcal{A}) \to \mathcal{A}
$$

from the [[category of chain complexes]] in $\mathcal{A}$ to $\mathcal{A}$ itself.

=--

In fact this is a universal [[delta-functor]].

## Related concepts

* [[category of chain complexes]]

  * [[chain complex]]

  * **chain map**, [[quasi-isomorphism]]

  * [[chain homotopy]], [[null homotopy]]

## References

A basic discussion is for instance in section 1.1 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_.

A more comprehensive discussion is in section 11 of 

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_,


[[!redirects chain maps]]

[[!redirects cochain map]]
[[!redirects cochain maps]]
