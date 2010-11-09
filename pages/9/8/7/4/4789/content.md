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

A _Chern-Simons element_ in an [[∞-Lie algebroid]] is an element of the [[Weil algebra]] that interpolates between an [[∞-Lie algebroid cocycle]] and an [[invariant polynomial]].

It is an algebraic model for a universal [[circle n-bundle with connection]] on the [[Lie integration]] $\exp(\mathfrak{a}) \in $ [[?LieGrpd]] of $\mathfrak{a}$.

The pullback of this connection $cs$ along an $\exp(\mathfrak{a})$-[[connection on an ∞-bundle]] $(A,B,C, \cdots)$ is the corresponding [[Chern-Simons form]] $CS(A,B,C,...)$. This is part of the [[∞-Chern-Weil homomorphism]]. The integrals of these Chern-Simons forms yield [[action functional]]s over spaces of connections which generalize those of standard [[Chern-Simons theory]]. Many [[sigma-model]]s of [[quantum field theory]] arise this way.

## Definition


+-- {: .un_def}
###### Definition

For $\mathfrak{g}$ an [[∞-Lie algebra]] or more generally [[∞-Lie algebroid]], $\mu \in CE(\mathfrak{g})$ a [[∞-Lie algebra cocycle]] (a closed element of the [[Chevalley-Eilenberg algebra]]) and $\langle - \rangle \in W(\mathfrak{g})$ an [[invariant polynomial]] (a closed element in the shifted generators of the[[Weil algebra]] ), a **Chern-Simons element** exhibiting the _transgression_ between the two is an element

$$
  cs \in W(\mathfrak{g})
$$

such that

1. we have $d_{W(\mathfrak{g})} cs = \langle -\rangle$

1. and $cs|_{CE(\mathfrak{g})} = \mu$

where the restriction is along the canonical morphism $W(\mathfrak{g}) \to CE(\mathfrak{g})$.

=--

We may equivalently express these two conditions as asserting the existence of a [[commuting diagram]] in [[dgAlg]] of the form

\[
  \array{
    CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^{n-1} \mathbb{R})
    &&&
    cocycle
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{g}) &\stackrel{cs}{\leftarrow}& W(b^{n-1} \mathbb{R})
    &&&
    Chern-Simons\;element
    \\
    \uparrow && \uparrow
    \\
    inv(\mathfrak{g}) &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(b^{n-1} \mathbb{R})
    &&&
    invariant polynomial
  }
  \,.
  \label{TheDiagram}
\]


+-- {: .un_def}
###### Definition

If we think of 

* $W(\mathfrak{g})$ as differential forms on the total space of the universal $G$-bundles;

* $CE(\mathfrak{g})$ as differential forms on the fiber

* $inv(\mathfrak{g})$ as differential forms on the base space

then the abov expresses the classical notion of transgression of forms from the fiber to the base of a fibe bundle (for instance [Borel, section 9](#Borel)).

=--

## Chern-Simons forms


As the term _Chern-Simons element_ indicates, when composed with [[∞-Lie algebra valued forms]] one obtain [[Chern-Simons forms]]:

As discussed at [[∞-Chern-Weil theory]] (see [[∞-Chern-Weil theory introduction]] for an introduction), a [[connection on an ∞-bundle]] with values in an $\infty$-Lie algebroid $\mathfrak{g}$, together with its [[gauge transformation]]s, is locally -- on a patch $U \in $ [[CartSp]] -- given by a [[truncated|truncation]] of the [[∞-groupoid]] whose [[k-morphism]]s are [[commuting diagram]]s in [[dgAlg]] of the form


\[
  \array{
    \Omega^\bullet(U \times \Delta^k)_{vert}
    &\stackrel{A_{vert}}{\leftarrow}&
    CE(\mathfrak{g})
    &&& transition\;function
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U \times \Delta^k)
    &\stackrel{A}{\leftarrow}&
    W(\mathfrak{g})
    &&&
    connection
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)
    &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(\mathfrak{g})
    &&&
    curvature\;characteristic\;form
  }
  \label{ConnectionDiagram}
  \,.
\]

Given such a connection with values in $\mathfrak{g}$, and given a refinement of an [[∞-Lie algebroid cocycle]] $\mu : \mathfrak{g} \to b^{n-1}\mathbb{R}$ as above, by forming the [[pasting]] composite diagrams \eqref{ConnectionDiagram} and \eqref{TheDiagram}, we obtain the corresponding local data for a $b^{n-1}\mathbb{R}$-valued connection:


\[
  \array{
    \Omega^\bullet(U \times \Delta^k)_{vert}
    &\stackrel{A_{vert}}{\leftarrow}&
    CE(\mathfrak{g})
    &\stackrel{\mu}{\leftarrow}&
    CE(b^{n-1}\mathbb{R})
    &&& characteristic\;class
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U \times \Delta^k)
    &\stackrel{A}{\leftarrow}&
    W(\mathfrak{g})
    &\stackrel{cs}{\leftarrow}&
    W(b^{n-1}\mathbb{R})
    &&&
    Chern-Simons\;form
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)
    &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(\mathfrak{g})
    &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(b^{n-1}\mathbb{R})
    &&&
    curvature\;characteristic\;form
  }
  \label{ChernWeilDiagram}
  \,.
\]

This is the local data of a [[circle n-bundle with connection]]. The connection form itself, appearing in the middle horizontal row

$$
  \Omega^\bullet(U) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{cs}{\leftarrow}
  W(b^{n-1}\mathbb{R})
  :
  CS(A)
$$

is the [[Chern-Simons form]] of the $\mathfrak{g}$-connection evaluated in the given Chern-Simons element. Its [[curvature]] is the [[curvature characteristic form]] $\langle F_A \rangle$ appearing in the bottom line of the diagram, which is obtained by evaluating the $\mathfrak{g}$-valued [[curvature]] in the given [[invariant polynomial]]. The top row, obtained by evaluating the [[∞-Lie algebroid cocycle]] on the transition functions yields -- after truncation followed by a quotient, see <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">integration of ∞-Lie algebra cocycles</a> -- the [[characteristic class]] that classifies the circle $n$-bundle.

The operation in the bottom row here is at the heart of the [[∞-Chern-Weil homomorphism]]. The joint operation on all rows refines this to [[secondary characteristic classes]]. 

For instance for $\mathfrak{g}$ a [[semisimple Lie algebra]] and $\mu$ the ordinary cocycle in [[Lie algebra cohomology]] in degree 3 or seven, this sends $G$-[[principal bundle]]s with [[connection on a bundle]] to the corresponding [[Chern-Simons circle 3-bundle]] and [[Chern-Simons circle 7-bundle with connection]], respectively.

This is part of the general [[∞-Chern-Weil homomorphism]].

We will see below in diagram \eqref{PhysicsDiagram} yet one incarnation of the transgression diagram, identifying it for the case that $\mathfrak{g}$ is a symplectic $\infty$-Lie algebroid with the triple $\mu =$[[Hamiltonian]], $cs = $[[Lagrangian]], $\langle - \rangle =$ [[symplectic structure]].

## Chern-Simons action functionals

Every Chern-Simons element $cs \in W(\mathfrak{a})$ of degree $d$ on an [[∞-Lie algebroid]] $\mathfrak{a}$ induces an [[action functional]] on the space of [[∞-Lie algebroid valued forms]] on $\mathfrak{a}$ over a $d$-[[dimensional]] [[smooth manifold]] $\Sigma$ 

$$
  S_{cs} : \Omega(\Sigma, \mathfrak{a}) \to \mathbb{R}
$$

given by

$$
  (A,B,C, \cdots) \mapsto \int_\Sigma CS(A,B,C, \cdots)
  \,.
$$

This generalizes the action functional of ordinary [[Chern-Simons theory]] to general Chern-Simons elements. In the [examples](#Examples) below is a list of various [[quantum field theories]] that arise as generalized Chern-Simons theories this way.

For more details see [[schreiber:infinity-Chern-Simons theory]].

## Examples {#Examples}

### On semisimple Lie algebra-- Standard Chern-Simons action functional {#StandardCS}

Let $\mathfrak{g}$ be a [[semisimple Lie algebra]]. For the following computations, choose a [[basis]] $\{t^a\}$ of $\mathfrak{g}^*$ and let $\{r^a\}$ denotes the corresponding degree-shifted basis of $\mathfrak{g}^*[1]$. 

Notice that in terms of this the differential of the CE-algebra is

$$
  d_{CE(\mathfrak{g})} : t^a \mapsto -\frac{1}{2}C^a{}_{b c}t^b \wedge t^c
$$

and that of the Weil algebra

$$
  d_{W(\mathfrak{g})} : t^a \mapsto -\frac{1}{2}C^a{}_{b c}t^b \wedge t^c
  + r^a
$$

and

$$
  d_{W(\mathfrak{g})} : r^a \mapsto  -C^a{}_{b c} t^b \wedge r^c
  \,.
$$

Let $P_{a b} r^a \wedge r^b \in W(\mathfrak{g})$ be the [[Killing form]] invariant polynomial. This being invariant

$$
  d_{W(\mathfrak{g})} P_{a b} r^a \wedge r^b 
  =
  2 P_{a b} C^{a}{}_{d e} t^d \wedge r^e \wedge r^b = 0
$$

is equivalent to the fact that the coefficients

$$
  C_{a b c} := P_{a a'}C^{a'}{}_{b c}
$$

are skew-symmetric in $a$ and $b$, and therefore skew in all three indices.


+-- {: .un_prop}
###### Proposition

A Chern-Simons element for the [[Killing form]] invariant polynomial $ \langle -, - \rangle = P(-,-)$ is

$$
  \begin{aligned}
    cs &=
    P_{a b} t^a \wedge (d_{W(\mathfrak{g})} t^b) 
    + 
    \frac{1}{3} P_{a a'}C^{a'}{}_{b c} t^a \wedge t^b \wedge t^c 
    \\
    & =
    P_{a b} t^a \wedge r^b
    -
    \frac{1}{6} 
    P_{a a'}C^{a'}{}_{b c} t^a \wedge t^b \wedge t^c 
  \end{aligned}
  \,.
$$

In particular the Killing form $\langle -,-\rangle$ is in transgression with the degree 3-cocycle

$$
  \mu = -\frac{1}{6}\langle -,[-,-]\rangle
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

We compute 

$$
  \begin{aligned}
    d_{W(\mathfrak{g})}
    \left(
       P_{a b} t^a \wedge r^b
       +
       \frac{1}{2}P_{a a'}C^{a'}{}_{b c} t^a \wedge t^b \wedge t^c        
    \right)
    & = 
      P_{a b} r^a \wedge r^b
      \\
      & -\frac{1}{2} P_{a b} C^a{}_{d e} t^d \wedge t^e \wedge r^b
      \\
      & + P_{a b} C^b{}_{d e} t^a \wedge t^d \wedge r^e
      \\
      & - \frac{3}{6} 
       P_{a a'}C^{a'}{}_{b c} t^a \wedge t^b \wedge r^c        
      \\
      & =
      P_{a b} r^a \wedge r^b
      \\
      & + \frac{1}{2}C_{a b c} t^a \wedge t^b \wedge r^c
      \\
      & - \frac{1}{2} 
       C_{a b c} t^a \wedge t^b \wedge r^c        
      \\
      & = P_{a b } r^a \wedge r^b
  \end{aligned}
  \,.
$$

=--


Under a [[Lie algebra-valued form]]

$$
  \Omega^\bullet(X) \stackrel{}{\leftarrow} W(\mathfrak{g}) : A
$$

this Chern-Simons element is sent to

$$
  cs(A) = P_{a b} A^a \wedge d A^b + \frac{1}{3} C_{a b c} A^a \wedge A^b \wedge A^c
  \,.
$$

If $\mathfrak{g}$ is a [[matrix Lie algebra]] then the Killing form is the [[trace]] and this is equivalently

$$
  cs(A) = tr(A \wedge d A) + \frac{2}{3} tr(A \wedge A \wedge A)
  \,.
$$

This is a familiar form of the standard [[Chern-Simons form]] in degree 3.

For $\Sigma$ a 3-[[dimensional]] [[smooth manifold]] the corresponding [[action functional]] $S_{CS} : \Omega^1(\Sigma, \mathfrak{g}) \to \mathbb{R}$

$$
  S_{CS} : A \mapsto \int_\Sigma cs(A)
$$

is the standard action functional of [[Chern-Simons theory]].

### Higher CS-forms on semisimple Lie algebras

For $\mu \in CE(\mathfrak{g})$ any higher order cocycle, $CS_\mu(A)$ is the corresponding higher order Chern-Simons form.

#### Action functional for Chern-Simons (super-)gravity

Higher Chern-Simons elements on the [[Poincare Lie algebra]] $\mathfrak{g} = \mathfrak{iso}(d,1)$ or the [[super Poincare Lie algebra]] $\mathfrak{g} = \mathfrak{siso}(d,1)$ yield [[action functional]]s for [[gravity]] and [[supergravity]].

(...)

See ([Zanelli](#Zanelli)).

#### Fractional secondary Pontryagin classes

For instance for $\mu_7$ the 7-cocycle on a [[semisimple Lie algebra]], $CS_{\mu_7}(A)$ is the corresponding Chern-Simons 7-form, corresponding to the second [[Pontryagin class]].

Notice that this we may also think of as a 7-cocycle on the corresponding [[string Lie 2-algebra]]. As such it is the one that classifies the extension to the [[fivebrane Lie 6-algebra]]. The corresponding Chern-Simons 7-form appears as the local conneciton data in the [[Chern-Simons circle 7-bundle with connection]] that obstructions the lift from a [[differential string structure]] to a differential [[fivebrane structure]].


### On strict Lie 2-algebras -- BF-theory action functional {#BF}

+-- {: .un_prop}
###### Proposition

Let $\mathfrak{g} = (\mathfrak{g}_2 \stackrel{\partial}{\to} \mathfrak{g})_1$ be a [[strict Lie 2-algebra]].

Then

* every [[invariant polynomial]] $\langle -\rangle_{\mathfrak{g}_1} \in inv(\mathfrak{g}_1)$ on $\mathfrak{g}_1$ is a Chern-Simons element on $\mathfrak{g}$, restricting to the trivial [[∞-Lie algebra cocycle]];

* for $\mathfrak{g}_1$ a [[semisimple Lie algebra]] and 
  $\langle - \rangle_{\mathfrak{g}_1}$ the [[Killing form]], the corresponding Chern-Simons action functional on [[∞-Lie algebra valued forms]]

  $$
    \Omega^\bullet(X) \stackrel{(A,B)}{\leftarrow}
    W(\mathfrak{g}_2 \to \mathfrak{g}_1)
    \stackrel{(\langle - \rangle_{\mathfrak{g}_1}, d_W \langle - \rangle_{\mathfrak{g}_1} )}{\leftarrow}
    W(b^{n-1} \mathbb{R})
  $$

is the sum of the [[action functional]]s of [[topological Yang-Mills theory]] with [[BF-theory]] with [[cosmological constant]] (in the sense of [[gravity as a BF-theory]]):

$$
  CS_{\langle-\rangle_{\mathfrak{g}_1}}(A,B) 
  = 
  \langle F_A \wedge F_A\rangle_{\mathfrak{g}_1}
  - 
  2\langle F_A \wedge \partial B\rangle_{\mathfrak{g}_1}
  +
  2\langle \partial B \wedge \partial B\rangle_{\mathfrak{g}_1}   
  \,,
$$

where $F_A$ is the ordinary [[curvature]] 2-form of $A$.

=--

This is from ([SSSI](#SSSI-BFtheory)).

+-- {: .proof}
###### Proof

For $\{t_a\}$ a [[basis]] of $\mathfrak{g}_1$ and $\{b_i\}$ a basis of $\mathfrak{g}_2$ we have

$$
  d_{W(\mathfrak{g})} : \sigma t^a \mapsto 
  d_{W(\mathfrak{g}_1)}
  + 
  \partial^a{}_i \sigma b^i
  \,.
$$

Therefore with $\langle -\rangle_{\mathfrak{g}_1} = P_{a_1 \cdots a_n} \sigma r^{a_1} \wedge \cdots \sigma t^{a_n}$ we have

$$
  d_{W(\mathfrak{g})} \langle - \rangle_{\mathfrak{g}_1}
  = 
  n P_{a_1 \cdots a_n}\partial^{a_1}{}_i  \sigma b^{i} \wedge \cdots \sigma t^{a_n}
  \,.
$$

The right hand is a polynomial in the shifted generators of $W(\mathfrak{g})$, and hence an [[invariant polynomial]] on $\mathfrak{g}$. Therefore $\langle - \rangle_{\mathfrak{g}_1}$ is a Chern-Simons element for it. 

Now for $(A,B)$ an [[∞-Lie algebra-valued form]], we have that the 2-form curvature is

$$
  F_{(A,B)}^1 = F_A - \partial B
  \,.
$$

Therefore

$$
  \begin{aligned}
    CS_{\langle -\rangle_{\mathfrak{g}_1}}(A,B)
    & = \langle F_{(A,B)}^1\rangle_{\mathfrak{g}_1}
    \\
    & = 
    \langle F_A \wedge F_A\rangle_{\mathfrak{g}_1}
    - 
    2\langle F_A \wedge \partial B\rangle_{\mathfrak{g}_1}
    +
    2\langle \partial B \wedge \partial B\rangle_{\mathfrak{g}_1}   
  \end{aligned}
  \,.
$$


=--



### On symplectic $\infty$-Lie algebroids -- The AKSZ Lagrangian {#Symplectic}


A [[schreiber:symplectic ∞-Lie algebroid]] / [[n-symplectic manifold]] $(\mathfrak{a}, \omega)$ is a [[∞-Lie algebroid|Lie n-algebroid]] $\mathfrak{a}$ equipped with a binary non-degenerate [[invariant polynomial]] $\omega \in W(\mathfrak{a})$ of degree $n+2$.

The corresponding Chern-Simons elements of $\omega$ are the integrands for the [[action functional]]s of various [[TQFT]] [[sigma-model]]s.

With $\{-,-\} : CE(\mathfrak{a}) \otimes CE(\mathfrak{a}) \to CE(\mathfrak{a})$ the graded [[Poisson bracket]] induced by $\omega$ we have (see [Roytenberg](#Roytenberg)) that there exists a [[∞-Lie algebra cocycle]]  $\mu \in CE(\mathfrak{a})$ such that

$$
  d_{CE(\mathfrak{a})} = \{\mu, -\}
  \,.
$$

So in particular $\mu$ being a cocycle means that 

$$
  d_{CE(\mathfrak{a})} \mu = \{\mu, \mu\} = 0
  \,.
$$

+-- {: .un_prop}
###### Proposition

The cocycle $\mu$ is in transgression with the invariant polynomial $\frac{1}{2}\omega$ via the Chern-Simons element 

$$
  \begin{aligned}
    cs &= \frac{1}{2 (n+2)}\iota_{\epsilon} \omega - \mu
  \end{aligned}
  \,,
$$

where $\epsilon$ is the Euler vector field ([Roytenberg](#Roytenberg)).

=--

Here $\mathbf{d}$ is the shift derivation in the [[Weil algebra]], in that $d_{W(\mathfrak{a})} = d_{CE(\mathfrak{a})} + \mathbf{d}$.

+-- {: .proof}
###### Proof

To safe typing signs, we write as if all functions were even graded. By standard reasoning the computation holds true then also for arbitrary grading.
 
Observe that 

1. on unshifted generators we have

   $$
     (\mathbf{d}x^b) \omega_{a b} \{x^a  , -\} = \mathbf{d}
   $$


1. we have graded commutators 

   * $[\mathbf{d}, \iota_v] = N$ (the degree operator) 

   and 

   * $[d_{CE(\mathfrak{a})}, \iota_v] = -N d_{CE(\mathfrak{a})}\mathbf{d}^{-1}$.

   (as one checks on generators).

Therefore 

$$
  \begin{aligned}
    d_{W(\mathfrak{a})} \frac{1}{2(n+2)}\iota_{v} \omega
    &= 
    [d_{W(\mathfrak{a})}, \iota_{v}] \frac{1}{2(n+2)}\omega
    \\
    & =
    (Id - d_{CE(\mathfrak{a})} \mathbf{d}^{-1} ) \frac{1}{2}\omega
    \\
    & =
    \frac{1}{2}\omega - \omega_{a b} \{\mu, x^a\} \mathbf{d}x^b
    \\
    &= \frac{1}{2} \omega + \mathbf{d}\mu
  \end{aligned}
  \,,
$$

where in the first line we used that by definition of [[invariant polynomial]] $d_{W(\mathfrak{a})} \omega = 0$. Similarly, using that by definition $d_{CE(\mathfrak{a})} \mu = 0$ we have 

$$
  d_{W(\mathfrak{a})} \mu = \mathbf{d}\mu
  \,.
$$

So in total we have

$$
  d_{W(\mathfrak{a})} (\frac{1}{2(n+2)} \iota_\epsilon \omega - \mu)
  =
  \frac{1}{2}\omega
  \,.
$$

=--

+-- {: .remark}
###### Remark

In local coordinates where $\omega = \omega_{a b} \mathbf{d}x^a \wedge \mathbf{d}x^b$ we have 

$$
  cs = \frac{1}{2} \omega_{a b} x^a \wedge \mathbf{d}x^b + \mu
  \,.
$$

The Chern-Simons action functional corresponding to this Chern-Simons element
on $\mathfrak{a}$ is that considered in [[AKSZ theory]]. 

Below we spell out some low-dimensional cases explicitly.

=--

#### Higher phase space ---Hamiltonian and Lagrangian mechanics


The symplectic Lie $n$-algebroid $(\mathfrak{P}, \omega)$ may be thought of as an [[n-symplectic manifold]] that models the [[phase space]] of a physical system. 

This means for $(\mathfrak{g},\langle-\rangle) = (\mathfrak{P}, \omega)$ a symplectic Lie $n$-algebroid, the general diagram \eqref{TheDiagram} exhibiting the transgression between cocycles and invariant polynomials via Chern-Simons elements may be labeled in terms of [[Hamiltonian mechanics]], [[Lagrangian mechanics]] and [[symplectic geometry]] as follows

\[
  \array{
    CE(\mathfrak{P})
    &\stackrel{H}{\leftarrow}&
    CE(b^{n}\mathbb{R})
    &&& Hamiltonian
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{P})
    &\stackrel{L}{\leftarrow}&
    W(b^n \mathbb{R})
    &&&
    Lagrangian
    \\
    \uparrow && \uparrow
    \\
    inv(\mathfrak{P})
    &\stackrel{\omega}{\leftarrow}&
    inv(b^n \mathbb{R})
    &&&
    symplectic\;structure
  }
  \label{PhysicsDiagram}
\]


=--


See [[Hamiltonian]], [[Lagrangian]], [[symplectic structure]].

#### On a symplectic manifold -- The topological particle

For $X$ a [[smooth manifold]] we may regard its cotangent bundle
$\mathfrak{a} = T^* X$ as a Lie 0-algebroid and the canonical 2-form 
$\omega \in W(\mathfrak{a}) = \Omega^\bullet(X)$ as a binary invariant 
polynomial in degree 2.

The Chern-Simons element is the canonical 1-form $\alpha$ which in local coordinates is $\alpha = p_i d q^i$.

The corresponding action functional on the line 

$$
  \int_{\mathbb{R}} \gamma^* (p_i\, d q^i)
$$

is the familiar term for the action functional of the particle (missing the kinetic term, which makes it "topological").

#### On a Poisson Lie algebroid -- The Poisson $\sigma$-model

+-- {: .un_prop}
###### Proposition

Let $\mathfrak{a} = \mathfrak{P}(X,\pi)$ by a [[Poisson Lie algebroid]]. This comes with the canonical [[invariant polynomial]] $\omega = \mathbf{d} \partial_i \wedge \mathbf{d} x^i$.

The correspinding [[∞-Lie algebroid cocycle]] is 

$$
  \mu_{\omega} = \pi
$$

and a Chern-Simons element for this is

$$
  cs_\omega = \pi^{i j} \partial_i  \wedge \partial_j 
  + \partial_i \wedge \mathbf{d}x^i
  \,.
$$

For $Sigma$ a 2-[[dimensional]] [[smooth manifold]] the corresponding [[action functional]] on [[∞-Lie algebroid-valued forms]] $S : \Omega^\bullet(X, \mathfrak{P}(X,\pi)) \to \mathbb{R}$ is the actional functional of the [[Poisson sigma-model]]

$$
  S : (X, \eta) \mapsto \int_\Sigma (\eta \wedge d X + \pi(\eta \wedge \eta)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We compute in a local coordinte patch:

$$
  \begin{aligned}
    d_{W(\mathfrak{P}(X,\pi))} (\pi^{i j} \partial_i \wedge \partial_j
   + \partial_i \wedge \mathbf{d} x^i)
    = &
   \mathbf{d}x^k (\partial_k \pi^{i j}) \partial_i \wedge \partial_j
   \\
   & + 2 \pi^{i j} (\mathbf{d}\partial_i) \wedge \partial_j
   \\
   & - (\partial_i \pi^{j k}) \partial_j \wedge \partial_k \wedge 
       \mathbf{d}x^i
   \\
   & +
   (\mathbf{d}\partial_i)\wedge (\mathbf{d} x^i)
   \\
   & + (-)(-) 2\pi^{i j} \partial_i \wedge \mathbf{d}\partial_j
   \\
   = & 
   (\mathbf{d}\partial_i)\wedge (\mathbf{d} x^i)
  \end{aligned}
  \,.
$$

=--

### On higher extensions of the super Poincare Lie algebra -- supergravity

See [[D'Auria-Fre formulation of supergravity]] for the moment.


## Related concepts

* [[∞-Lie algebroid cocycle]]

* **Chern-Simons element**

* [[invariant polynomial]]


## References

A classical references on transgression of forms from the fiber to the base of a [[fiber bundle]] is section 9 of.

* [[Armand Borel]], _Topology of Lie groups and characteristic classes_  Bull. Amer. Math. Soc. Volume 61, Number 5 (1955), 397-432. ([EUCLID](http://projecteuclid.org/euclid.bams/1183520007))
{#Borel}

The general definition of Chern-Simons element on $\infty$-Lie algebras and $\infty$-Lie algebroids is <a href="http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3480v2.pdf#page=21">definition 21</a> in

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_\infty$-connections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)
{#SSSI}


The examples of the [[BF-theory]] invariant polynomials and Chern-Simons elements are in <a href="http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3480v2.pdf#page=43">prop. 18</a> and <a href="http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3480v2.pdf#page=51">def. 26</a> and the BF-action functional itself is extracted below <a href="http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3480v2.pdf#page=56">proposition 28</a>.
{#SSSI-BFtheory}

Further discussion is in 

* [[Chris Rogers]] [[Urs Schreiber]], _$\infty$-Chern-Simons action functionals_


A survey of higher Chern-Simons elements and their action functionals as applied to [[gravity]] and [[supergravity]] is in

* Jorge Zanelli, _Lecture notes on Chern-Simons (super-)gravities_ [arXiv:0502193](http://arxiv.org/abs/hep-th/0502193)
{#Zanelli}

For the discussion of symplectic $n$-Lie algebroids above see [[n-symplectic manifold]] and

* [[Dmitry Roytenberg]], _On the structure of graded symplectic supermanifolds and Courant algebroids_ ([arXiv:math/0203110](http://arxiv.org/abs/math/0203110))
{#Roytenberg}



[[!redirects Chern-Simons elements]]

[[!redirects generalized Chern-Simons theory]]
[[!redirects generalized Chern-Simons theories]]
[[!redirects ∞-Chern-Simons theory]]