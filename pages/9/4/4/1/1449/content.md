

#Definition#

Let $C$ be a [[category]] with [[pullback]]s. A **power object** of an object $c \in C$ is 

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

#Examples#

* A category with finite [[limit]]s and power objects for all objects is a [[topos]].

* See [[Trimble on ETCS I]] for the **Axiom of power sets** in the elementary theory of the category of sets.