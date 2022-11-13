
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _power object_ generalizes the notion of [[power set]] from the [[category]] [[Set]] to an arbitrary category with [[finite limit]]s.

## Definition

Let $C$ be a [[category]] with [[finitely complete category|finite limits]]. A **power object** of an object $c \in C$ is 

* an [[object]] $\Omega^c$ 

* a [[monomorphism]] $\in_c \hookrightarrow c \times \Omega^c$

such that

* for every other object $d$ and every [[monomorphism]] $r \hookrightarrow c \times d$ there is a unique morphism
$\chi_r : d \to \Omega^c$ such that $r$ is the [[pullback]]

$$
  \array{
    r &\to& \in_c
    \\
    \downarrow && \downarrow
    \\
    c \times d
    &\stackrel{Id_c \times \chi_r}{\to}&
    c \times \Omega^c
  }
$$

If $C$ may lack some finite limits, then we may weaken that condition as follows:

*  If $C$ has all [[pullbacks]] (but may lack products), then equip each of $\in_c$ and $r$ with a jointly monic pair of morphisms, one to $c$ and one to $\Omega^c$ or $d$, in place of the single monomorphism to the product of these targets; $r$ must then be the joint pullback

   $$ \array {
   & c          & \leftarrow    & r & \rightarrow & d &  \\
   Id_c & \downarrow & & \downarrow & & \downarrow & \chi_r \\
   & c          & \leftarrow      & \in_c      & \rightarrow       & \Omega^c & \\
   } $$

*  If $C$ may lack some pullbacks, then we simply require that the pullback that $r$ is to equal must exist.  But arguably we should require, if $\Omega^c$ is to be a power object, that this pullback exists for any given map $\chi: d \to \Omega^c$.

## Examples

* If $1$ is a [[terminal object]], then $\Omega^1$ is precisely a [[subobject classifier]].

* A power object in [[Set]] is precisely a [[power set]].

* A category with finite [[limits]] and power objects for all objects is precisely a [[topos]]. The power object $P A $ of any object $A$ in the topos is the [[exponential object]] $P A = \Omega^A$ into the [[subobject classifier]]. 

* See [[Trimble on ETCS I]] for the axiom of power sets in the elementary theory of the category of sets.

[[!redirects power objects]]