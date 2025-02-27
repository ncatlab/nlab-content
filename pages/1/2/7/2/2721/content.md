
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}


## Idea


For every [[Lie algebra]] or [[∞-Lie algebra]] or [[∞-Lie algebroid]] $\mathfrak{a}$ there is its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{a})$ and its [[Weil algebra]] $W(\mathfrak{a})$ and a canonical [[dg-algebra]] morphism

$$
  CE(\mathfrak{a}) \leftarrow W(\mathfrak{a})
  \,.
$$ 

Recall that a [[∞-Lie algebra cohomology|cocycle]] on $\mathfrak{a}$ is a closed element in $CE(\mathfrak{a})$. An invariant polynomial is a closed elements in $W(\mathfrak{a})$ that sits in the shifted copy $\wedge^\bullet (\mathfrak{a}^*[1])$.

This means that for $X \in \mathfrak{a}$, for $\iota_X : W(\mathfrak{a}) \to W(\mathfrak{a})$ the contraction derivation and $ad_X := [d_W, \iota_X]$ the corresponding [[Lie derivative]], we have in particular that an invariant polynomial $\langle -\rangle \in W(\mathfrak{a})$ is invariant in the sense that 

$$
  ad_X \langle -\rangle = 0
  \,.
$$

For $\mathfrak{a} = \mathfrak{g}$ an ordinary [[Lie algebra]], an invariant polynomial on $\mathfrak{g}$ is precisely a symmetric multilinear map on $\mathfrak{g}$ which is $ad$-invariant in the ordinary sense.


## Definition

+-- {: .num_defn}
###### Definition

For $\mathfrak{a}$ an [[∞-Lie algebroid]] (of finite type, i.e. degreewise of finite rank) with [[Chevalley-Eilenberg algebra]] 

$$
  CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{a}^*, d_{CE(\mathfrak{a}}))
$$ 

and [[Weil algebra]] 

$$
  W(\mathfrak{a}) = (\wedge^\bullet (\mathfrak{a}^* \oplus \mathfrak{a}^*[1]), d_{W(\mathfrak{a})})
$$

an **invariant polynomial** on $\mathfrak{a}$ is an elements $\langle - \rangle \in W(\mathfrak{a})$ with the property that

* $\langle - \rangle$ is a wedge product of generators in the shifted copy of 
  $\mathfrak{a}^*$ $W(\mathfrak{a})$, i.e.

  $$
    \langle - \rangle \in \wedge^\bullet \mathfrak{a}^*[1]
  $$

  or equivalently: for all $x \in \mathfrak{a}$ and $\iota_X : W(\mathfrak{a}) \to W(\mathfrak{a})$ the contraction [[derivation]], we have

  $$
    \iota_x \langle -\rangle = 0
    \,;
  $$

* it is closed in $W(\mathfrak{a})$ in that $d_{W(\mathfrak{a})} \langle - \rangle = 0$

   or more generally its differential is again in the shifted copy.

=--


+-- {: .num_remark}
###### Remark


This implies that for 

$$
  ad_x := [d_{W(\mathfrak{a})}, \iota_X]
$$

the [[Lie derivative]] in $W(\mathfrak{a})$ along $x \in \mathfrak{a}$, which encodes the coadjoint action of $\mathfrak{a}$ on $W(\mathfrak{a})$, we have

$$
  ad_x \langle - \rangle = 0
$$

for all $x$. But the condition for an invariant polynomial is stronger than these ad-invariances. For instance there are  [[∞-Lie algebra cohomology|∞-Lie algebra cocycles]] $\mu \in CE(\mathfrak{g})$ which when regarded as elements in $W(\mathfrak{g})$ are ad-invariant. But being entirely in the un-shifted copy, $\mu \in \wedge^\bullet \mathfrak{g}^*$, these are not invariant polynomials.

=--

+-- {: .num_defn #DecomposableInvPolynomial}
###### Definition 

We say an invariant polynomial is _decomposable_ if it is the wedge product in $W(\mathfrak{g})$ of two invariant polynomials of non-vanishing degree. 

=--

+-- {: .num_defn #HorizontalEquivalence}
###### Definition 

Two invariant polynomials $P_1, P_2 \in W(\mathfrak{g})$ are _horizontally equivalent_ if there is $\omega \in ker(W(\mathfrak{g}) \to CE(\mathfrak{g}))$ such that

$$
  P_1 = P_2 + d_W \omega
  \,.
$$

=--

+-- {: .num_prop #DecomposablePolysAreHorizontallyTrivial}
###### Proposition

Every decomposable invariant polynomial, def. \ref{DecomposableInvPolynomial}, is horizontally equivalent to 0.

=--

+-- {: .proof}
###### Proof

Let $P = P_1 \wedge P_2$ be a wedge product of two indecomposable polynomials. Then there exists a [[Chern-Simons element]] $cs_1 \in W(\mathfrak{g})$ such that $d_W cs_1 = P_1$. By the assumption that $P_2$ is in non-vanishing degree and hence in $ker(W(\mathfrak{g}) \to CE(\mathfrak{g}))$ it follows that 

1. also $cs_1 \wedge P_2$ is in $ker(W(\mathfrak{g}) \to CE(\mathfrak{g}))$ 

1. $d_W (cs_1 \wedge P_2) = P_1 \wedge P_2$ .

Therefore $cs_1 \wedge P_1$ exhibits a horizontal equivalence $P_1 \wedge P_2 \sim 0$.

=--


+-- {: .num_prop #ClassesOfInvPolysFormGradedVectorSpace}
###### Observation

Horizontal equivalence classes of invariant polynomials on $\mathfrak{g}$ form a [[graded vector space]] $inv(\mathfrak{g})_V$. There is a morphism of graded vector spaces

$$
  inv(\mathfrak{g})_V \hookrightarrow W(\mathfrak{g})
$$

unique up to horizontal equivalence, that sends each horizontal equivalence class to a representative.

=--

+-- {: .num_remark}
###### Remark

By prop. \ref{DecomposablePolysAreHorizontallyTrivial} it follows that 
$inv(\mathfrak{g})_V$ contains only indecomposable invariant polynomials.

=--


+-- {: .num_defn}
###### Definition

We write $inv(\mathfrak{g})$ for the [[dg-algebra]] whose underlying [[graded algebra]] is the [[free construction|free]] graded algebra on the [[graded vector space]] $inv(\mathfrak{g})_V$, and whose [[differential]] is trivial.

Since invariant polynomials are closed, the inclusion of graded vector spaces from observation \ref{ClassesOfInvPolysFormGradedVectorSpace} induces an inclusion ([[monomorphism]]) of dg-algebras

$$
  inv(g) \hookrightarrow W(g)
  \,.
$$


=--



## Examples

### On Lie algebras {#OnLieAlgebras}


+-- {: .num_lemma}
###### Observation

For $\mathfrak{g}$ a [[Lie algebra]], this definition of invariant polynomials is equivalent to more traditional ones.

=--

+-- {: .proof}
###### Proof

To see this explicitly, let $\{t^a\}$ be a basis of $\mathfrak{g}^*$ and $\{r^a\}$ the corresponding basis of $\mathfrak{g}^*[1]$. Write $\{C^a{}_{b c}\}$ for the structure constants of the Lie bracket in this basis. 

Then for $P = P_{(a_1 , \cdots , a_k)} r^{a_1} \wedge \cdots \wedge r^{a_k} \in \wedge^{r} \mathfrak{g}^*[1]$ an element in the shifted generators, the condition that it is $d_{W(\mathfrak{g})}$-closed is equivalent to

$$
  C^{b}_{c (a_1} P_{b, \cdots, a_k)} t^c \wedge r^{a_1} \wedge \cdots \wedge r^{a_k}
  \,,
$$

where the parentheses around indices denotes symmetrization, as usual, so that this is equivalent to

$$
  \sum_{i} C^{b}_{c (a_i} P_{a_1 \cdots a_{i-1} b a_{i+1} \cdots, a_k)}
  = 0
$$ 


for all choice of indices. This is the component-version of the familiar invariance statement 

$$
  \sum_i P(t_1, \cdots, t_{i-1}, [t_c, t_i], t_{i+1}, \cdots , t_k)
  = 0
$$

for all $t_\bullet \in  \mathfrak{g}$.


=--


### On semisimple Lie algebras 
 {#SemisimpLie}

See [[Killing form]], [[string Lie 2-algebra]].



### On tangent Lie algebroids

For $X$ a [[smooth manifold]], and invariant polynomial on the [[tangent Lie algebroid]] $\mathfrak{a} = T X$ is precisely a closed [[differential form]] on $X$.

### On the string Lie 2-algebra
 {#OnStringLie2Algebra}

For $\mathfrak{g}$ a [[semisimple Lie algebra]] let 
$\mu_3 := \langle -,[-,-]\rangle$ be the canonical [[Lie algebra cocycle]] in degree 3, which is the one in [[transgression]] with the [[Killing form]] invariant polynomial $\langle -,-\rangle$.

Write $\mathfrak{g}_{\mu_3}$ for the corresponding [[string Lie 2-algebra]]. We have that the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g}_{\mu_3})$ is given by

$$
  d_{CE} t^a = - \frac{1}{2}C^a{}_{b c} t^b \wedge t^c
$$

$$
  d_{CE} b = \mu_3
$$

and the [[Weil algebra]] $W(\mathfrak{g}_{\mu_3})$ is given by

$$
  d_W t^a = - \frac{1}{2}C^a{}_{b c} t^b \wedge t^c + r^a
$$

$$
  d_W b = \mu_3 - h
$$

$$
  d_W r^a = - C^a_{b c} t^b \wedge r^c
$$

$$
  d_W h = d_W \mu_3 = \sigma \mu_3
  \,,
$$

where $\sigma$ acts by degree shift isomorphism on unshifted generators.

It follows at once that every invariant polynomial 

$$
  P = P_{a_1, \cdots, a_n} r^{a_1} \wedge \cdots \wedge r^{a_n}
$$ 

on the Lie algebra $\mathfrak{g}$ canonically identifies also with an invariant polynomial of the string Lie 2-algebra. But the differnce is that the [[Killing form]] $\langle -,- \rangle := P_{a b} r^a \wedge r^b$ is non-trivial as a polynomial on $\mathfrak{g}$, but as a polynomial on $\mathfrak{g}_{\mu_3}$ becomes 
horizontally equivalent ,def. \ref{HorizontalEquivalence}), to the trivial invariant polynomial.

+-- {: .num_prop}
###### Proposition

On the [[string Lie 2-algebra]] $\mathfrak{g}_{\mu_3}$ the [[Killing form]] $\langle -,-\rangle$ is horizontally equivalent to 0.

=--

+-- {: .proof}
###### Proof

Let $cs_3 \in W(\mathfrak{g})$ be any [[Chern-Simons element]] for $\langle -,- \rangle$, hence an element such that 

1. $cs_3|_{CE(\mathfrak{g})} = \mu_3$;

1. $d_W cs_3 = \langle -,- \rangle$.

Then notice that by the above we have in $W(\mathfrak{g}_{\mu_3})$ that the differential of the new generator $h$ is equal to that of $\mu_3$:

$$
  d_W h = d_W \mu_3
  \,.
$$

We on $\mathfrak{g}_{\mu_4}$ we can replace $\mu_3$ by $h$ and still get a  [[Chern-Simons element]] for the Killing form:

$$
  \tilde cs_3 := cs_3 - \mu_3 + h
  \,.
$$

$$
  d_W \tilde cs_3 = \langle -,- \rangle
  \,.
$$

But while $\mu_3$ is not in $ker(W(\mathfrak{g}_{\mu_3}) \to CE(\mathfrak{g}_{\mu_3}))$, the element $h$ is, by definition. Therefore $\tilde cs_3$ is in that kernel, and hence exhibits a horizontal equivalence between $\langle -,- \rangle$ and $0$.

=--

This is a special case of the more general statement below, about [invariant polynomials on shifted central extensions](OnShiftedCentralExtenstions).

For illustration purposes it is useful to consider the following variant of this example:

+-- {: .num_defn}
###### Definition

Write

$$
 (b \mathbb{R} \to \mathfrak{string}) \in L_\infty Alg
$$

for the [[L-∞ algebra]] defined by the fact that its [[Chevalley-Eilenberg algebra]] is given by

$$
  d_{CE} t^a = - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
$$

$$
  d_{CE} b = \mu_3 - c
$$

$$
  d_{CE} c = 0
  \,,
$$

where $\{t^a\}$ is a dual basis in degree 1 for some [[semisimple Lie algebra]] $\mathfrak{g}$ as above, $b$ and $c$ are generators in degree 2 and 3, respectively, and $\mu_3 \propto \langle -,[-,-]\rangle$ is the canonical [[Lie algebra cohomology|Lie algebra cocycle]] in degree 3, as above.

=--

It is easily seen that

+-- {: .num_prop}
###### Observation

The canonical morphism

$$
  \mathfrak{g} \to (b \mathbb{R} \to \mathfrak{string})
$$

given dually by sending 

$$
  t^a \mapsto t^a\,,\,\,\, b \mapsto 0\,,\, \,\, c \mapsto \mu_3
$$

is a weak equivalence.

=--

So the Lie 3-algebra $(b \mathbb{R} \to \mathfrak{string})$ is a kind of [[resolution]] of the ordinary Lie algebra $\mathfrak{g}$. It is for instance of use in the presentation of twisted [[differential string structure]]s, where the shifted piece $b \mathbb{R}$ in $(b \mathbb{R} \to \mathfrak{string})$ picks up the failure of $\mathfrak{so}$-valued [[connection on an ∞-bundle|connections]] to lift to $\mathfrak{string}$-[[connection on a 2-bundle|2-connections]].

The proof of the following proposition may be instructive for seeing how the definition of horizontal equivalence of invariant polynomials takes care of having the invariant polynomials of $(b\mathbb{R} \to \mathfrak{string})$ agree with those of $\mathfrak{g}$.

+-- {: .num_prop}
###### Observation

There is an [[isomorphism]]

$$
  inv(\mathfrak{g}) \simeq inv(b \mathbb{R} \to \mathfrak{string})
  \,.
$$

=--

+-- {: .proof}
###### Proof

Notice that the [[Weil algebra]] of $(b\mathbb{R} \to \mathfrak{string})$ is given by

$$
  d_W t^a = - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c + r^a
$$

$$
  d_W b = \mu_3 - c - h
$$

$$
  d_W c = g
$$

for new generators $\{r^a\}$ in degree 2, $h$ in degree 3 and $g$ in degree 4, coming with their [[Bianchi identities]]

$$
  d_W r^a = - C^a{}_{b c}t^b \wedge r^c
$$

$$
  d_W h = d_W \mu_3 - g
$$

$$
  d_W g = 0
$$

For the following computations let $\{k_{a b}\}$ be the structure constants of the [[Killing form]], so that

$$
  \langle -,- \rangle = k_{a b} r^a \wedge r^b
$$

and assume that $\mu_3$ is normalized such that 

$$
  \mu_3 = k_{a a'}C^{a'}_{b c} t^a \wedge t^b \wedge t^c
$$

(if another normalization is chosen, then the corresponding factor will float around the following formulas without changing anything of the end result).

Now the indecomposable invariant polynomials are those of $\mathfrak{g}$ and one additional one: $g$. This means that before deviding out horizontal equivalence on generators, the invariant polynomials of $(b \mathbb{R} \to \mathfrak{string})$ are not equal to those of $\mathfrak{g}$, due to the superfluous generator $g$.

But we do have the horizontal equivalence relation

$$
  \langle -,-\rangle = g + d_W (cs - \mu_3 + h)
 \,,
$$

where $cs$ is any [[Chern-Simons element]] for $\langle - , \rangle$, for instance

$$
  cs 
   = 
   \frac{1}{6} k_{a a'}C^{a'}_{b c} t^a \wedge t^b \wedge t^c 
   + 
   k_{a b} t^a r^b
  \,,
$$

Notice that the homotopy $cs - \mu_3 + h$ here is indeed in $ker(W(\mathfrak{g}) \to CE(\mathfrak{g}))$: the component of $cs$ not in that kernel is precisely $\mu$. The above formula subtracts this offending summand and replaces it with the new generator $h$, which by definition _is_ in the kernel and whose image under $d_W$ is the image of $\mu$ under $d_W$, plus the superfluous new generator of invariant polynomials.

Therefore in horizontal equivalence classes of invariant polynomials on $(b \mathbb{R} \to \mathfrak{string})$ the superfluous $g$ is identified with the Killing form $\langle-,- \rangle$, and hence the claim follows.


=--

### On symplectic Lie $n$-algebroids

A [[symplectic Lie n-algebroid]] is an [[L-infinity algebroid]] that carries a binary and non-degeneraty invariant polynomial of grade $n$. This is a generalization of the notion of [[symplectic form]] to which it reduces for $n = 0$.

## Properties
 {#Properties}

### As differential forms on the moduli stack of connections
 {#AsFormsOnBGconn}

The invariant polynomials of a Lie algebra $\mathfrak{g}$, thought of as equipped with trivial differential, are the de Rham complex of differential forms on the universal moduli stack $\mathbf{B}G_{conn}$ of $G$-[[principal connections]] [Freed-Hopkins 13](#FreedHopkins13).

$$
  \mathrm{inv}(\mathfrak{g})\simeq \Omega^\bullet(\mathbf{B}G_{conn})
  \,.
$$

For more on this see also at _[Weil algebra -- Characterization in the smooth infinity-topos](Weil+algebra#CharacterizationInSmoothTopos)_.

### On reductive Lie algebras 
 {#OnReductiveLieAlg}

+-- {: .num_prop}
###### Proposition

Let $\mathfrak{g}$ be a [[reductive Lie algebra]]. Then the subalgebra of invariant polynomials in the [[Weil algebra]] is the [[free construction|free graded algebra]] on the [[graded vector space]] of indecomposable invariant polynomials.

This graded vector space has a vector space [[isomorphism]] of degree -1 to the graded vector space of odd generators of the [[Lie algebra cohomology]] $H^\bullet(\mathfrak{g}) = H^\bullet(CE(\mathfrak{g}))$. 

=--

This appears for instance as ([GHV, vol III, page 242, theorem I](#GHV)).



## Role in $\infty$-Chern-Weil theory

In ($\infty$-)[[Chern-Weil theory]] the crucial role played by the invariant polynomials is their relation to [[∞-Lie algebra cocycle]]s. One may understand invariant invariant polynomials as extending under [[Lie integration]] $\infty$-Lie algebra cocycles from [[cohomology]] to [[differential cohomology]].


### Transgression cocycles and Chern-Simons elements {#TransgressionCocycles}


+-- {: .un_defn}
###### Definition
**(Chern-Simons elements and transgression cocycles)**

Let $\mathfrak{a} = \mathfrak{g}$ be an [[∞-Lie algebra]]. Since the [[cochain cohomology]] of the [[Weil algebra]] $W(\mathfrak{g})$ is trivial, for every invariant polynomial $\langle -\rangle \in W(\mathfrak{g})$ there is necessarily an element $cs \in W(\mathfrak{g})$ with

$$
  d_{W(\mathfrak{g})} cs = \langle -\rangle
  \,.
$$

This we call a [[Chern-Simons element]] for $\langle -\rangle$.

This element $cs$ will in general not sit entirely in the shifted copy. Its restriction

$$
  \mu := cs|_{\wedge^\bullet \mathfrak{g}^*} \in CE(\mathfrak{g})
$$

is a [[∞-Lie algebra cohomology|∞-Lie algebra cocycle]]. We say this is _in transgression_ with $\langle -\rangle$.

In total this construction yields a commuting diagram

$$
  \array{
     CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^{n-1}\mathbb{R})
     &&& cocycle
     \\
     \uparrow && \uparrow
     \\
     W(\mathfrak{g}) &\stackrel{(cs,\langle -\rangle)}{\leftarrow}&
     W(b^{n-1} \mathbb{R})
     &&&
     Chern-Simons-element
     \\
     \uparrow && \uparrow
     \\
     inv(\mathfrak{g}) &\stackrel{\langle -\rangle}{\leftarrow}&
     CE(b^n \mathbb{R})
     &&&
     invariant\; polynomial
  }
  \,,
$$

where $b^{n-1}\mathbb{R}$ denotes the [[∞-Lie algebra]] whose CE-algebra has a single generator in degree $n$ and vanishing differential, and where $CE(b^n \mathbb{R}) = inv(b^{n-1}\mathbb{R})$ is the algebra of invariant polynomials of $b^{n-1} \mathbb{R}$.

=--

+-- {: .un_prop}
###### Proposition

The element $\mu \in CE(\mathfrak{g})$ associated to an invariant polynomial $\langle -\rangle$ by the above procedure is indeed a cocycle, and its cohomology class is independent of the choice of the element $cs$ involved.

=--

+-- {: .proof}
###### Proof

The procedure that assigns $\mu$ to $\langle- \rangle$ is illustarted by the following diagram

$$
  \array{
    0 && \langle-\rangle &\leftarrow & \langle-\rangle
    \\
    \;\;\uparrow^{\mathrlap{d_{CE(\mathfrak{g})}}}
    &&
    \;\;\uparrow^{\mathrlap{d_{W(\mathfrak{g})}}}
    \\
    \mu &\leftarrow& cs
    \\
    \\
    \\
    \\
    CE(\mathfrak{a})
    &\leftarrow&
    W(\mathfrak{a})
    &\leftarrow&
    inv(\mathfrak{a})    
  }
$$

From the fact that all morphisms involved respect the differential and from the fact that the image of $\langle-\rangle$ in $CE(\mathfrak{g})$ vanishes it follows that 

* the element $\mu$ satisfies $d_{CE(\mathfrak{a})} \mu = 0$, hence that it is an [[∞-Lie algebra cohomology|∞-Lie algebra cocycle]];

* any two different choices of $cs$ lead to cocylces $\mu$ that are cohomologous.

=--


This construction exhibits effectively the preimage of the [[connecting homomorphism]] in the [[cochain cohomology]] sequence induced by $W(\mathfrak{g}) \to CE(\mathfrak{g})$:

The [[dg-algebra]] of invariant polynomials is a sub-dg-algebra of the kernel of the morphism $i^* : W(\mathfrak{a}) \to CE(\mathfrak{a})$ from the [[Weil algebra]] to the [[Chevalley-Eilenberg algebra]] of $\mathfrak{a}$

$$
  inv(\mathfrak{a}) \subset CE(\Sigma \mathfrak{a}) = ker(W(\mathfrak{a}) \to CE(\mathfrak{a}))
  \,.
$$

From the short [[nLab:exact sequence]]

$$
  CE(\Sigma \mathfrak{a}) \to W(\mathfrak{a}) \to 
  CE(\mathfrak{a})
$$

we obtain the long exact sequence in [[chain homology and cohomology|cohomology]]

$$
  \cdots 
  \to 
  H^{n+1}(CE(\mathfrak{a}))
  \stackrel{\delta}{\to} H^{n+2}(CE(\Sigma \mathfrak{a}))
  \to \cdots 
  \,.
$$

We say that $\mu \in CE(\mathfrak{a})$ is in transgression with $\omega \in inv(\mathfrak{a}) \subset CE(\Sigma \mathfrak{a})$ if their classes map to each other under the [[connecting homomorphism]] $\delta$:

$$
  \delta : [\mu] \mapsto [\omega]
  \,.
$$


**Example.** In the case where $\mathfrak{g}$ is an ordinary semisimple [[Lie algebra]], this reduces to the ordinary study of ordinary Chern-Simons 3-forms associated with $\mathfrak{g}$-valued 1-forms. This is described in the section [On semisimple Lie algebras](#SemisimpLie).

### Chern-Simons and curvature characteristic forms

For $\mathfrak{g}$ a [[∞-Lie algebra|Lie n-alghebra]], let $\mathbf{B}G := \mathbf{cosk}_{n+1} \exp(\mathfrak{g})$ be the [[∞-Lie group]] obtained by [[Lie integration]] from it.

For $X$ a [[paracompact space|paracompact]] [[smooth manifold]] with [[good open cover]] $\{U_i \to X\}$ whose [[Cech nerve]] we write $C(U)$, a [[cocycle]] for a $G$-[[principal ∞-bundle]] on $X$ is cocycle with coefficients in the simplicial sheaf

$$
  \mathbf{B}G = 
  \mathbf{cosk}_{n+1}((U,[k]) \mapsto \{ 
     \Omega^\bullet_{vert}(U \times \Delta^k)
     \leftarrow
     CE(\mathfrak{g})
  \})
  \,.
$$


We say an $\infty$-connection on this is an extension to a cocycle with coefficients in the simplicial sheaf

$$
  \mathbf{B}G_{diff} = 
  \mathbf{cosk}_{n+1}((U,[k]) \mapsto \left\{ 
    \array{
       \Omega^\bullet_{vert}(U \times \Delta^k)
       &\leftarrow&
       CE(\mathfrak{g})
       &&& underlying \; cocycle
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet(U\times \Delta^k)
       &\stackrel{}{\leftarrow}&
       W(\mathfrak{g})
       &&&
       connection
     }
  \right\}
  \,.
$$

The diagrams on the left encode those $\mathfrak{g}$-valued forms on $U \times \Delta^k$ whose [[curvature]] vanishes on $\Delta^k$. One can show that one can always find a _genuine_ $\infty$-connection: one for which the curvatures have no leg along $\Delta^k$, in that they land in $\Omega^\bullet(U) \otimes C^\infty(\Delta^k)$. For those the above diagram extends to

$$
  \array{
     \Omega^\bullet(U \times \Delta^k)_{vert}
     &\leftarrow&
     CE(\mathfrak{g})
     &&& underlying \; cocycle
     \\
     \uparrow && \uparrow
     \\
     \Omega^\bullet(U\times \Delta^k)
     &\stackrel{}{\leftarrow}&
     W(\mathfrak{g})
     &&&
     connection
     \\
     \uparrow && \uparrow
     \\
     \Omega^\bullet(U)
     &\leftarrow&
     inv(\mathfrak{g})
     &&&
     curvature
   }
  \,.
$$ 

This defines the [[simplicial presheaf]] that classifies [[connections on ∞-bundles]].

By [[pasting]]-postcomposition with the above diagrams for an invariant polynomial we obtain connections with values in $b^n \mathbb{R}$

$$
  \array{
     \Omega^\bullet_{vert}(U \times \Delta^k)
     &\leftarrow&
     CE(\mathfrak{g})
     &\stackrel{\mu}{\leftarrow}&
     CE(b^{n-1}\mathbb{R})
     &&& underlying \; cocycle
     \\
     \uparrow && \uparrow && \uparrow
     \\
     \Omega^\bullet(U\times \Delta^k)
     &\stackrel{}{\leftarrow}&
     W(\mathfrak{g})
     &\stackrel{(cs,\langle- \rangle)}{\leftarrow}&
     W(b^{n-1}\mathbb{R})
     &&&
     Chern-Simons forms
     \\
     \uparrow && \uparrow && \uparrow
     \\
     \Omega^\bullet(U)
     &\leftarrow&
     inv(\mathfrak{g})
     &\stackrel{\langle -\rangle}{\leftarrow}&
     CE(b^n \mathbb{R})
     &&&
     curvature\;characteristic\;form
   }
  \,,
$$ 

where in the bottom row we have the [[curvature characteristic forms]] $\langle F_\nabla\rangle$ coresponding to the connection, and in the middle the corresponding [[Chern-Simons forms]].

More details for the moment at [[∞-Chern-Weil theory introduction]].




## Related concepts

* [[∞-Lie algebra cocycle]]

* [[Chern-Simons element]]

* **invariant polynomial**, [[invariant theory]]

## References

The idea of invariant polynomials as a $G$-invariant subalgebra in the [[Weil algebra]], and their use in what is now called [[Chern-Weil theory]], originates with 


* [[André Weil]], _Géométrie différentielle des espaces fibres_, unpublished, item [1949e] in: _André Weil Oeuvres Scientifiques / Collected Papers_, vol. 1 (1926-1951), 422-436, Springer 2009 ([ISBN:978-3-662-45256-1](https://www.springer.com/gp/book/9783662452561))

* [[Henri Cartan]], _Cohomologie réelle d'un espace fibré principal différentiable. I : notions d'algèbre différentielle, algèbre de Weil d'un groupe de Lie _, Séminaire Henri Cartan, Volume 2  (1949-1950), Talk no. 19, May 1950  ([numdam:SHC_1949-1950__2__A18_0](http://www.numdam.org/item/?id=SHC_1949-1950__2__A18_0))

  \linebreak

  [[Henri Cartan]], _Notions d'algèbre différentielle; applications aux groupes de Lie et aux variétés o&ugrave; opère un groupe de Lie_, in: Centre Belge de Recherches Mathématiques, _Colloque de Topologie (Espaces Fibrés) Tenu &agrave; Bruxelles du 5 au 8 juin 1950_, Georges Thon 1951 ([GoogleBooks](https://books.google.de/books/about/Colloque_de_topologie_espaces_fibres.html?id=sagqHQAACAAJ&redir_esc=y))

  \linebreak

  (These two articles have the same content, with the same section outline, but not the same wording. The first one is a tad more detailed.)

* {#Chern50} [[Shiing-shen Chern]], _Differential geometry of fiber bundles_, in: Proceedings of the International Congress of Mathematicians, Cambridge, Mass., (August-September 1950), vol. 2, pages 397-411,  Amer. Math. Soc., Providence, R. I. (1952) ([[Chern-DifferentialGeometryOfFiberBundles.pdf:file]], [full proceedings vol 2 pdf](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1950.2/ICM1950.2.ocr.pdf))

* {#KobayashiNomizu63} [[Shoshichi Kobayashi]], [[Katsumi Nomizu]], Section XII.2 in: _Foundations of Differential Geometry, Volume 1_, Wiley 1963 ([web](https://www.zuj.edu.jo/download/foundations-of-differential-geometry-vol-1-kobayashi-nomizu-pdf/), [ISBN:9780471157335](https://www.wiley.com/en-us/Foundations+of+Differential+Geometry%2C+Volume+1-p-9780471157335), [Wikipedia](https://en.wikipedia.org/wiki/Foundations_of_Differential_Geometry))


Invariant polynomials for Lie algebras of [[simple Lie groups]] are disussed in

* [[José de Azcárraga]],  A. J. Macfarlane, A. J. Mountain, J. C. Perez Bueno, _Invariant tensors for simple groups_, Nucl. Phys. B510 (1998) 657-687 ([arXiv:physics/9706006](http://arxiv.org/abs/physics/9706006))

A standard textbook account of the traditional theory is in volume III of 

* {#GHV} [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)
 

The notion of invariant polynomials of $L_\infty$-algebras has been introduced in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_\infty$-connections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+a+cohesive+topos+--+references#SSSI">web</a>).

Discussion via [[differential cohomology]] of the [[moduli stack]] $\mathbf{B}G_{conn}$:

* {#FreedHopkins13} [[Daniel Freed]], [[Michael Hopkins]]: _*Chern-Weil forms and abstract homotopy theory*, Bull. Amer. Math. Soc. **50** (2013) 431-468 &lbrack;[arXiv:1301.5959](http://arxiv.org/abs/1301.5959), [doi:S0273-0979-2013-01415-0](https://www.ams.org/journals/bull/2013-50-03/S0273-0979-2013-01415-0)&rbrack;
  > (via [[de Rham cohomology]])

* [[Daniel Grady]]: *On the differential K-theory of moduli stacks* &lbrack;[arXiv:2501.03108](https://arxiv.org/abs/2501.03108)&rbrack;
  > (via [[ordinary differential cohomology]] and [[differential K-theory]])

An account in the more general context of Lie theory in [[cohesive (infinity,1)-toposes]] is in section 3.3.11 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ .


[[!redirects algebra of invariant polynomials]]
[[!redirects dg-algebra of invariant polynomials]]

[[!redirects invariant polynomials]]