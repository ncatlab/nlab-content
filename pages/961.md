
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Congruences
* table of contents
{: toc}

## Definitions

+-- {: .num_defn #Definition}
###### Definition

In a [[finitely complete category]] $C$, a **congruence** on an object $X$ is an [[internalization|internal]] [[equivalence relation]] on $X$.

This means that it consists of a [[subobject]] of the product $R\stackrel{(p_1,p_2)}\hookrightarrow X \times X$ equipped with the following [[morphisms]]: 

* internal [[reflexive relation|reflexivity]]: $r \colon X \to R$ which is a [[section]] both of $p_1$ and of $p_2$, i.e., $p_1 r = p_2 r = 1_X$;

* internal [[symmetric relation|symmetry]]: $s \colon R \to R$ which interchanges $p_1$ and $p_2$, i.e., $p_1\circ s = p_2$ and $p_2\circ s = p_1$;

* internal [[transitive relation|transitivity]]: $t: R \times_X R \to R$ which factors the left/right projection map $R \times_X R \to X \times X$ through $R$, i.e., the following diagram commutes
  $$\array{
    && R \\  
    & {}^{\mathllap{t}}\nearrow & \downarrow \\
    R \times_X R & \stackrel{(p_1 q_1,p_2 q_2)}\rightarrow & X \times X
  }
  $$
where $q_1$ and $q_2$ are the projections defined by the [[pullback | pullback diagram]]
  $$\array{
    R \times_X R & \stackrel{q_2}\rightarrow & R
    \\
    \downarrow^{\mathrlap{q_1}} && \downarrow^{\mathrlap{p_1}}
    \\
    R & \stackrel{p_2}\rightarrow & X
  }
  $$
=--

+-- {: .num_remark}
###### Remark

Since $i$ is a [[monomorphism]], the maps $r$, $s$, and $t$ are necessarily unique if they exist.

=--

+-- {: .num_remark}
###### Remark

Equivalently, a congruence on $X$ is an [[internal category]] with $X$ the object of [[objects]], such that the (source,target)-map is a [[monomorphism]] and such that if there is a morphism $x_1 \to x_2$ then there is also a morphism $x_2 \to x_1$ (internally).

=--

+-- {: .num_remark}
###### Remark

We can equivalently define a congruence $R$ as (a representing object of) a representable sub-presheaf of $\hom(-, X \times X)$ so that for each object $Y$, the composite of $R(Y) \hookrightarrow \hom(Y, X \times X) \cong \hom(Y, X) \times \hom(Y, X)$ exhibits $R(Y)$ as an equivalence relation on the set $\hom(Y, X)$. The upshot of this definition is that it makes sense even when $C$ is not finitely complete.

=--

+-- {: .num_defn #EffectiveCongruence}
###### Definition

A congruence which is the kernel pair of some morphism (example \ref{KernelPairIsCongruence}) is called **effective**.  

=--

+-- {: .num_defn #QuotientObject}
###### Definition

The [[coequalizer]] of a congruence is called a **[[quotient object]]**.  

The quotient of an effective congruence is called an **effective quotient**.  

=--

+-- {: .num_defn}
###### Definition

A [[regular category]] is called an [[exact category]] if every congruence is effective.

=--



## Properties

+-- {: .num_prop}
###### Proposition

An effective congruence, def. \ref{EffectiveCongruence}, is always the [[kernel pair]] of its quotient, def. \ref{QuotientObject}, if that quotient exists.

=--


## Examples

+-- {: .num_example #KernelPairIsCongruence}
###### Example

Every [[kernel pair]] is a congruence.

=--


+-- {: .num_example}
###### Example

An [[equivalence relation]] is precisely a congruence in [[Set]].

=--

+-- {: .num_example}
###### Example

The eponymous example is congruence modulo $n$ (for a fixed [[natural number]] $n$), which can be considered a congruence on $\mathbb{N}$ in the category of [[rigs]], or on $\mathbb{Z}$ in the category of [[rings]].

=--

+-- {: .num_example}
###### Example

A [[quotient group]] by a  [[normal subgroup]] $K \hookrightarrow G$ is the quotient of the congruence $R = \{(x,y) : xy^{-1} \in K \}$.

Alternatively, a [[quotient group]] by a  [[normal subgroup]] $K \hookrightarrow G$ is the quotient of the congruence 
 $G \times K \stackrel{(p_1,p_2)}{\hookrightarrow} G \times G$, where $p_1$ is projection on the first factor and $p_2$ is multiplication in $G$ (these are source and target maps in the [[action groupoid]] $G \sslash K$).

A special case of this is that of a _[[quotient module]]_.

=--


## Related pages

* The notions of [[regular category]] and [[exact category]] can naturally be formulated in terms of congruences.  A "higher arity" version, corresponding to [[coherent categories]] and [[pretoposes]] is discussed at [[familial regularity and exactness]].

* A [[Mal'cev category]] is a [[finitely complete category]] in which every internal relation satisfying reflexivity is thereby actually a congruence.

* [[higher category theory|Higher-categorical]] generalizations are that of a [[2-congruence]] and of a [[groupoid object in an (∞,1)-category]]. See also [[(n,r)-congruence]].


[[!redirects congruence]]
[[!redirects congruences]]
[[!redirects congruence relation]]
[[!redirects congruence relations]]
[[!redirects internal equivalence relation]]
[[!redirects internal equivalence relations]]
[[!redirects internal congruence]]
[[!redirects internal congruences]]