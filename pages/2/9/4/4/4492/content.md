

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _Bianchi identity_ is a [[differential equation]] satisfied by [[curvature]] data. 

It can be thought of as generalizing the equation $d (d A) = 0$ for a real-valued [[differential form|1-form]] $A$ to higher degree and nonabelian forms. 

Generally it applies to [[schreiber:∞-Lie algebroid valued differential forms]].

## Definition

### For 2-form curvatures

Let $U$ be a [[smooth manifold]]. 

For $A \in \Omega^1(U)$ a differential 1-form, its [[curvature]] 2-form is the de Rham differential $F_a = d A$. The Bianchi identity in this case is the equation

$$
  d F = 0
  \,.
$$
 
More generally, for $\mathfrak{g}$ an arbitrary [[Lie algebra]] and $A \in \Omega^1(U,\mathfrak{g})$ a [[Lie-algebra valued 1-form]], its [[curvature]] is the 2-form $F_A = d A + [A \wedge A]$. The Bianchi identity in this case is the equation

$$
  d F_A + [A\wedge F_A] = 0
$$

satisfied by these curvature 2-forms. 

### Reformulation in terms of Weil algebras

We may reformulate the above identities as follows.

For $\mathfrak{g}$ a [[Lie algebra]] we have naturally associated two [[dg-algebra]]s: the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ and the [[Weil algebra]] $W(\mathfrak{g})$.

The dg-algebra morphisms 

$$
  \Omega^\bullet(U) \leftaarrow W(\mathfrak{g}) : (A,F_A)
$$

are precisely in bijection with [[Lie-algebra valued 1-form]]s as follows: the [[Weil algebra]] is of the form

$$
  W(\mathfrak{g}) = \wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1]), d_{W(\mathfrak{g})}  
$$

with one copy of $\mathfrak{g}^*$ in degree 1, the other in degree 2. By the [[free construction|free]] nature of the Weil algebra, dg-algebra morphisms $\Omega^\bullet(U) \leftarrow W(\mathfrak{g})$ are in bijection to their underlying morphisms of vector spaces of generators

$$
  \Omega^1(U) \leftarrow \mathfrak{g}^* : A
  \,.
$$

This identifies the 1-form $A \in \Omega^1(U,\mathfrak{g})$. This extends uniquely to a morphism of dg-algebras and thereby fixes the image of the shifted generators

$$
  \Omega^2(U) \leftarrow \mathfrak{g}^*[1] : F_A
  \,.
$$

The _Bianchi identity_ is precisely the statement that these linear maps, extended to morphisms of graded algebra, are compatible with the differentials and hence do constitute [[dg-algebra]] morphisms.

Concretely, if $\{t^a\}$ is a dual basis for $\mathfrak{g}^*$ and $\{r^a\}$ the corresponding dual basis for $\mathfrak{g}^*[1]$ and $\{C^a{}_{b c}\}$ the structure constants of the Lie bracket $[-,-]$ on $\mathfrak{g}$, then the differential $d_{W(\mathfrak{g})}$ on the Weil algebra is defined on generators by

$$
  d_{W(\mathfrak{g})} t^a = - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c + r^a
$$
 

and

$$
  d_{W(\mathfrak{g})} r^a = C^a{}_{b c} t^b \wedge r^c
  \,.
$$

The image of $t^a$ under $\Omega^\bullet(U) \leftarrow W(\mathfrak{g}) : (A,F_A)$ is the component $A^a$. The image of $r^a$ is therefore, by respect for the differential on $t^a$

$$
  r^a \mapsto (F_A)^a := d A^a + \frac{1}{2}C^a{}_{b c} A^b \wedge A^c
  \,.
$$

Respect for the differential on $r^a$ then implies

$$
  d (F_A)^a + C^a{}_{b c} A^a \wedge (F_A)^c = 0
  \,. 
$$

This is the Bianchi identity.

### For curvature of $\infty$-Lie algebra valued forms.

Let now $\mathfrak{g}$ be an arbitrary [[L-∞-algebra]] and $W(\mathfrak{g})$ is [[Weil algebra]]. Then a collection of $\mathfrak{g}$-valued differential forms is a [[dg-algebra]] morphism

$$
  \Omega^\bullet(U) \leftarrow W(\mathfrak{g})   
  ,.
$$

As before, this is fixed by its value on the unshifted generators of $W(\mathfrak{g})$, and this defines the $\mathfrak{g}$-valued connection forms. The image of the shifted generators are the corresponding [[curvature]] forms. The respect for the differential in $W(\mathfrak{g})$ of these is their Bianchi identity.

For the moment see: [[schreiber:curvature of ∞-Lie algebroid valued differential forms]].