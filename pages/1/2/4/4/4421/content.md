
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

A _Chern-Simons form_ $CS(A)$ is a [[differential form]] naturally associated to a differential form $A \in \Omega^1(P,\mathfrak{g})$ with values in a [[Lie algebra]] $\mathfrak{g}$: it is the form trivializing (locally) a [[curvature characteristic form]] $\langle F_A \wedge \cdots \wedge F_A \rangle$ of $A$, for $\langle \cdots \rangle$ an [[invariant polynomial]]: 

$$
  d_{dR} CS(A) = \langle F_A \wedge \cdots \wedge F_A \rangle
  \,,
$$

where $F_A \in \Omega^2(X,\mathfrak{g})$ is the [[curvature]] 2-form of $A$.

Therefore it is often also called a [[secondary characteristic form]].

More generally, for $A,A' \in \Omega^1(P, \mathfrak{g})$ two $\mathfrak{g}$-valued 1-forms and for $\hat A \in \Omega^1(P \times [0,1],\mathfrak{g})$ a "path of connections", the Chern-Simons form relative to $A$ and $A'$ is a form that trivializes the _difference_ between the two curvature characteristic forms

$$
  d_{dR}CS(A,A') = \langle (F_A)^k \rangle - \langle (F_{A'})^k \rangle
  \,.
$$

Chern-Simons forms are of interest notably when the differential forms $A,A'$ are (local representatives of) [[connection on a bundle|connections]] on a $G$-[[principal bundle]] $P \to X$, for instance if $A \in \Omega^1(P,\mathfrak{g})$ is an [[Ehresmann connection]] 1-form.

Often the term _Chern-Simons form_ is taken to refer to the case where $\mathfrak{g}$ is a [[semisimple Lie algebra]] with binary [[invariant polynomial]] $\langle -, -\rangle$ (e.g. the [[Killing form]]) in which case $CS(A)$ is the 3-form

$$
  \langle A \wedge d_{dR} A\rangle
  + 
  c
  \langle
    A \wedge [A \wedge A]
  \rangle
  \,.
$$

 Even more specifically, often the term is understood to refer to the case where $\mathfrak{g} \subset \mathfrak{gl}(n)$ is a [[matrix Lie algebra]], for instance $\mathfrak{o}(n)$ (for the [[orthogonal group]]) or notably $\mathfrak{u}(n)$ (for the [[unitary group]]). In that case the invariant polynomials may be taken to be given by matrix [[trace]]s: $\langle \cdots \rangle = tr(\cdots )$.

## Details {#Details}


It is sufficient to discuss properties of Chern-Simons forms for $\mathfrak{g}$-valued 1-forms. The corresponding statements for connections on a $G$-bundle follow straightforwardly.


### Paths of connections {#PathsOfConnections}

Let $U$ be a [[smooth manifold]]. 

+-- {: .un_prop}
###### Definition

A **smooth path** of $\mathfrak{g}$-valued 1-forms on $U$ is a smooth 1-form $\hat A \in \Omega^1(U\times [0,1],\mathfrak{g})$ 

Call this path **pure shift** if $\iota_{\partial_t} \hat A = 0$, where $t : U \times [0,1] \to [0,1] \hookrightarrow \mathbb{R}$ is the canonical coordinate along the interval. 

We say this path goes from $A_0 := \psi_0^* \hat A$ to $A_1 := \psi_1^* \hat A$, where

$$
  \psi_t :  U \simeq U \times * \stackrel{Id \times t}{\to} U \times [0,1]
$$

picks the copy of $U$ at parameter $t$.

=--

So a smooth path is a smooth 1-form on the cylinder $U \times [0,1]$ and it is _pure shift_ if it has no "leg" along the $[0,1]$-direction. We will see that $\iota_{\partial_t} \hat A$ is infinitesimal gauge transformation, while $\partial_t \hat A$ is infinitesimal shift of the connection.


+-- {: .un_def}
###### Definition/Observation

Let $P$ be an [[invariant polynomial]] on $\mathfrak{g}$ of arity $n$.

Consider the [[fiber integration]]

$$
  CS_P(A_0,A_1) :=
  \int_{[0,1]} P(F_{\hat A} \wedge \cdots \wedge F_{\hat A})
  \,.
$$

This defines a $(2n-1)$-form $CS_P(A_0,A_1) \in \Omega^{2n-1}(U)$.

We have that the exterior differential of this form is the difference of the [[curvature characteristic form]]s of $A_0$ and $A_1$:

$$
  d_{dR} CS_P(A_0,A_1)
  =
  P(F_{A_1} \wedge \cdots \wedge F_{A_1})
  -
  P(F_{A_0} \wedge \cdots \wedge F_{A_0})
$$


=--

+-- {: .proof}
###### Proof

Write the fiber integration more explicitly as a [[Riemann integral]]

$$
  CS_P(A_0,A_1) =
  \int_{[0,1]} 
    \psi_t^* \iota_{\partial_t} P(F_{\hat A} \wedge \cdots \wedge F_{\hat A})
    d t
  \,.
$$


Then use that $d_{dR}$ is linear and commutes with pullback, use [[Cartan's magic formula]] $d_{dR} \circ \iota_{\partial_t} + \iota_{\partial} \circ d_{dR} = \mathcal{L}_{\partial_t}$ in view of the fact that $P(F_{\hat A} \wedge \cdots \wedge F_{\hat A})$ is a [[closed form]] and then finally apply the [[Stokes theorem]]:

$$
  \begin{aligned}
    d_{dR} \int_0^1 \psi^*_t  \iota_{\partial_t} 
    P(F_{\hat A} \wedge \cdots \wedge F_{\hat A}) d t
   & =
    \int_0^1 d_{dR}  \psi^*_t  \iota_{\partial_t} 
     P(F_{\hat A} \wedge \cdots \wedge F_{\hat A}) d t
    \\
   & =
    \int_0^1 \psi^*_t  d_{dR}   \iota_{\partial_t} 
      P(F_{\hat A} \wedge \cdots \wedge F_{\hat A}) d t
    \\
   & =
    \int_0^1 \psi^*_t  \frac{d}{d t} 
      P(F_{\hat A} \wedge \cdots \wedge F_{\hat A}) d t
    \\
   & =
    \int_0^1 \left(\frac{d}{d t} 
      P(F_{\hat A} \wedge \cdots \wedge F_{\hat A})\right)(t) d t
    \\
   & =
   \psi^*_1 P(F_{\hat A} \wedge \cdots \wedge F_{\hat A})
   -
   \psi^*_0 P(F_{\hat A} \wedge \cdots \wedge F_{\hat A})   
   \\
    &=
   P(F_{A_1} \wedge \cdots \wedge F_{A_1})
   -
   P(F_{A_0} \wedge \cdots \wedge F_{A_0})       
  \end{aligned}
  \,.
$$

=--


### Explicit formulas

Above we saw that a general expression for the Chern-Simons $CS_P(A_0,A_1)$ obtained from a path of connections $\hat A$ between $A_0$ and $A_1$ is

$$
  CS_P(A_0, A_1) = \int_{[0,1]} P(F_{\hat A} \wedge \cdots \wedge F_{\hat A})
  \,.
$$

We now unwind this to get explicit formulas for the Chern-Simons form in terms of wedge products of connection forms and their curvatures.

For  $\hat A$ a pure shift path, $\hat A : t \mapsto A_t$
notice that the [[curvature]] 2-form of $\hat A$ is 

$$
  F_{\hat A}(t) = F_{A_t} + (\partial_t A_t) \wedge d t
  \,.
$$

Inserting this into the above expression yields

$$
  CS_P(A_0,A_1)
  =
  \int_0^1 P(\partial_t A \wedge F_{A_t} \wedge \cdots \wedge F_{A_t})
  \,.
$$

Notably if $A_0 = 0$ and $\hat A$ is the _constant_ path $\hat A : t \mapsto t A$ to $A_1  := A$ such that

$$
  \begin{aligned}
    F_{\hat A} 
    &= t d_{dR} A + t^2 [A \wedge A]
    \\
    &=  
    t F_A + (t^2 - t) [A \wedge A]
  \end{aligned}
$$


this yields

$$
  CS_P(A)
  :=
  \int_0^1 P(A \wedge (t F_{A} + (t^2 - t) [A \wedge A])) 
    \wedge \cdots (t F_{A} + (t^2 - t) [A \wedge A])))
  \,.
$$

This is just an integral over a polynomial in $t$ with constant coefficients in forms. Peforming the integral yields a bunch of coefficients $c_i$ and with these the Chern-Simons form achieves the form

$$
  CS(A)
  = 
  c_1 \langle A \wedge F_A \wedge \cdots \wedge F_A \rangle
  + 
  c_2 \langle A \wedge [A \wedge A] \wedge F_A \wedge \cdots F_A \rangle
  +
  \cdots
  \,.
$$ 

Particularly for $n = 2$ and using the definition of the 
[[curvature]] 2-form $F_A = d_{dR} A + [A \wdge A]$ we get 

$$
  CS(A)
  =
  \langle A \wedge d A\rangle
  + 
  c \langle A \wedge [A \wedge A]\rangle
  \,.
$$


### Gauged paths of connections

Above we defined $CS(A_0,A_1)$ for every path of connections form $A_0$ to $A_1$ which is _pure shift_ . This is a possibly convenient but unnecessary restriction:

Notice that a general (gauged) path is a general 1-form $\hat A \in \Omega^1(U \times [0,1], \mathfrak{g})$ which we can decompose in the form

$$
  \hat A : t \mapsto  A_t + \lambda d t 
  \,,
$$

where $\lambda$ is a $\mathfrak{g}$-valued function. The [[parallel transport]] of $\lambda d t$ along $[0,1]$ defines an element in $G$ and shift $(\partial_t A)_t$ of the connection along $[0,1]$ is now relative to the gauge transformation on $A$ induced by this function: the curvature 2-form now is

$$
  F_{\hat A}
  : t \mapsto
  F_{A_t}
  + 
  ((\partial_t A)_t + d_U \lambda(t) + [\lambda,A]) \wedge d t
$$

+-- {: .un_prop}
###### Proposition

The Chern-Simons form $\int_{[0,1]} P(F_{\hat A} \wedge \cdots \wedge F_{\hat A})$ defined with respect to any gauged lift of a pure shift path of connections differs from that of the pure shift path by an exact term.

=--



## In $\infty$-Chern-Weil theory {#InInfCSTheory}

We discuss now a more encompassing perspective on Chern-Simons forms the way it occurs in [[∞-Chern-Weil theory]].

### Prerequisites {#PrerequisitesHigher}

We need to collect a few notions described elsewhere, on which the following discussion is based.

For $\mathfrak{g}$ a [[Lie algebra]] or more generally an [[∞-Lie algebra]]  we have the following [[dg-algebra]]s naturally associated with it:

* the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$;

* the [[Weil algebra]] $W(\mathfrak{g})$;

* the algebra of [[invariant polynomial]]s $inv(\mathfrak{g})$.

Given $n \in \mathbb{N}$, the [[Lie integration]] of $\mathfrak{g}$ to degree $n$ is the [[∞-Lie groupoid]] which is the $n$-[[truncation]] of the [[simplicial presheaf]]

$$
  \exp(\mathfrak{g}) :  U,[n] \mapsto 
   dgAlg(
     CE(\mathfrak{g}),
     C^\infty(U)\otimes \Omega^\bullet(\Delta^n)
        )
  \,,
$$

where here and in the following $\Omega^\bullet(\Delta^n)$ denotes the [[de Rham complex]] dg-algebra of those smooth [[differential form]]s $\omega$ on the standard smooth $n$-simplex that have _sitting instants_ in that for each $k \in \mathbb{N}$ every $k$-face of $\Delta^n$ has an open neighbourhood such that restricted to that neighbourhood $\omega$ is constant in the direction perpendicular to the face.

This is a one-object [[∞-Lie groupoid]] which we may write

$$
  \mathbf{B}G = \mathbf{cosk}_{n+1} \exp(\mathfrak{g})
  \,,
$$

thus defining the [[∞-Lie group]] $G$ that integrates $\mathfrak{g}$ in degree $n$.

At [[∞-Chern-Weil theory]] is explained that a [[resolution]] of $\mathbf{B}G$ that serves to compute [[curvature characteristic form]]s in that it encodes [[pseudo-connection]]s on $G$-[[principal ∞-bundle]]s is given by the simplicial presheaf

$$
  \mathbf{B}G_{diff}
  :=
  \mathbf{cosk}_{n+1}
  \left(
  U,[n]
  \mapsto
  \left\{
    \array{
      C^\infty(U) \otimes \Omega^\bullet(\Delta^n)
      &\leftarrow&
      CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
      &\leftarrow&
      W(\mathfrak{g})
    }
  \right\}
  \right)
  \,,
$$

where the vertical morphisms are the canonical ones.

Much of the subtlety of the full theory of connections of $\infty$-bundles comes from the finite [[coskeleton]]-truncation here. For the following discussion of Chern-Simons forms it is helpful to first ignore this issue by taking $n = \infty$, hence ignoring the truncation for the moment. This is sufficient for understand everything about Chern-Simons forms locally. 

A [[cocycle]] in [[∞-Lie algebra cohomology]] in degree $k$ is a morphism

$$
  CE(\mathfrak{g}) \leftarrow CE(b^{k-1} \mathbb{R}) : \mu
  \,.
$$

Simply by composition (since we ignore the truncation for the moment), this integrates to a cocycle of the corresponding $\infty$-Lie groupoids

$$
  \exp(\mu) : \exp(\mathfrak{g}) \to \exp(b^{k-1}\mathbb{R})
  \,,
$$


At [[∞-Chern-Weil theory]] it is discussed how the proper lift of this through the extension $\mathbf{B}G_{diff}$ that computes the [[schreiber:differential cohomology in an (∞,1)-topos|abstractly defined]] curvature characteristic classes is given by finding the [[invariant polynomial]] $\langle -,-\rangle \in W(\mathfrak{g})$ that is in transgression with $\mu$ in that we have a commuting diagram

$$
  \array{
     CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^{k-1}\mathbb{R})
     \\
     \uparrow && \uparrow
     \\
     W(\mathfrak{g}) &\stackrel{(cs, \langle-,-\rangle))}{\leftarrow}&
     W(b^{k-1}\mathbb{R})
     \\
     \uparrow && \uparrow
     \\
     inv(\mathfrak{g}) &\stackrel{\langle -,-\rangle}{\leftarrow}& 
     CE(b^k \mathbb{R})
  }
$$

with a choice of interpolating Chern-Simons element $cs \in W(\mathfrak{g})$,
which induces by precomposition with its upper part the morphism

$$
  \exp((cs,\langle-,-\rangle)) : 
   \mathbf{B}G_{diff} \to \exp(b^{k-1}\mathbb{R})_{diff}
  \,.
$$

By further projection to its lower part we get furthermore a morphism

$$
   \exp(b^{k-1}\mathbb{R})_{diff}
   \to 
   \mathbf{\flat}_{dR}\mathbf{B}^k \mathbb{R}_{simp}
   :=
   (U,[n] \mapsto
   \{ \Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^n)
    \leftarrow
     W(b^k \mathbb{R})
    \})
  \,.
$$


Finally -- and this is crucial now for obtaining the incarnation of Chern-Simons forms at integrals of curvature forms as in the above discussion -- at [[∞-Lie groupoid]] in the section <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#DeRhamOfSimplicialManifold">on simplicial differential forms</a> (see also [[circle n-bundles with connection]] the section <a href="http://ncatlab.org/nlab/show/circle+n-bundle+with+connection#U1FromLieIntegration">Models from ∞-Lie integration</a>) it is discussed that the operation
that takes the $n$-cells on the right and integrates the corresponding forms
over the $n$-simplex yields an equivalence

$$
  \int_{\Delta^\bullet} : 
   (U,[n] \mapsto
   \{ \Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^n)
    \leftarrow
     W(b^k \mathbb{R})
    \})
    \;\;\;\;\to \;\;\;\;
    \Xi(  \stackrel{d_{dR}}{\to}\Omega^{k-1}(-)\stackrel{d_{dR}}{\to}\Omega^k_{closed}(-))  
$$

to the image of the $\mathbb{R}$-[[Deligne complex]] of sheaves 
under the [[Dold-Kan correspondence]].


### Higher order Chern-Simons form {#HigherOrderChernSimonsForms}

With all of the above in hand, we can make now the following observations:

For $X$ a smooth manifold and $\mathfrak{g}$ an [[∞-Lie algebra]]
with coefficient for pseudo-connections being $\mathbf{B}G_{diff}$ as above, a morphism

$$
  A : X \to \mathbf{B}G_{diff}
$$

of simplicial presheaves (no resolution on the left, since we are concentrating on globally defined forms for the present purpose) is effectively a $\mathfrak{g}$-values differential form on $X$

For $\mu$ a cocycle on $\mathfrak{g}$ and $\langle -,-\rangle$ a corresponding invariant polynomial the composite

$$
  X \to \mathbf{B}G_{diff} \to \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}
$$

discussed above produces the corresponding [[curvature characteristic form]].

A [[homotopy]] 

$$
  (\nabla \to \nabla') : X \cdot \Delta[1] \to \mathbf{B}G_{diff}
$$

is a smooth path in the space of $\mathfrak{g}$-valued forms on $X$. Under the [[adjunction]]

$$
  [X \cdot \Delta[1], \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}]
  \simeq
  [X, \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}^{\Delta[1]}]
$$

this corresponds to a $(k-1)$-form on $X$ this is the Chern-Simons form

$$
  CS(\nabla \to \nabla') : X \to \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}^{\Delta[1]}
  \,.
$$

The higher homotopies are higher order Chern-Simons forms.


The following proposition says this in a more precise way for ordinary Chern-Simons forms.

#### Ordinary Chern-Simons forms revisited {#OrdinaryCSRevisited}

We now show how the [traditional definition](#PathsOfConnections) of Chern-Simons forms is reproduced by the [general abstract](#HigherOrderChernSimonsForms) mechanism.

+-- {: .un_prop}
###### Proposition
**(ordinary Chern-Simons form)**

Let $\mathfrak{g}$ be a [[Lie algebra]], and $\langle -,-\rangle \in W(\mathfrak{g})$ an  [[invariant polynomial]]. 

Then morphisms (of simplicial presheaves)

$$
  A : X \to \mathbf{B}G_{diff}
$$

are in canonical bijection with [[Lie-algebra valued 1-forms]] $A \in \Omega^1(X,\mathfrak{g})$. Morphisms

$$
  X \to \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}
$$

are in canonical bijection with closed $k$-forms on $X$ and composition with the morphism 

$$
  \mathbf{B}G_{diff} \to \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}
$$

discussed [above](#PrerequisitesHigher) and under this canonical identification the composite

$$
  \langle F_A \rangle : X \stackrel{A}{\to}
   \mathbf{B}G_{diff} \stackrel{}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}
$$

is the corresponding [[curvature characteristic form]].

Homotopies

$$
  (A_1 \stackrel{\gamma}{\to} A_2)  : X\times \Delta[1] \to \mathbf{B}G_{diff}
$$

are in canonical bijection with smooth paths in the space of $\mathfrak{g}$-valued 1-forms on $X$ and under composition with $\mathbf{B}G_{diff} \to \mathbf{\flat}_{dR}\mathbf{B}^k \mathbb{R}$ these identify with the corresponding Chern-Simons form

$$
  \langle F_A\rangle
  \stackrel{CS(A \stackrel{\gamma}{\to} A')}{\to}
  \langle F_{A'}\rangle
  : 
  X \to (\mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn})^{\Delta[1]}
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is a straightforward unwinding of the definitions. We spell it out in the following in order to highlight the way the mechanism works.

By the [[Yoneda lemma]] and the definition of $\mathbf{B}G_{diff}$, a morphism $X \to \mathbf{B}G_{diff}$ is equivalently a diagram

$$
  \array{
    C^\infty(X) \otimes \Omega^\bullet(\Delta^0) &\leftarrow& CE(\mathfrak{g})
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(X) \otimes \Omega^\bullet(\Delta^0)
    &\stackrel{(A,F_A)}{\leftarrow}&
    W(\mathfrak{g})
  }
  \,.
$$

Since $CE(\mathfrak{g})$ is trivial in degree 0 and since $C^\infty(X)\otimess \Omega^\bullet(\Delta^0)$ is trivial above degree 0, the top morphism is necessarily 0 and the commutativity of the diagram is an empty condition.

The bottom morphism on the other hand enccodes precisely a $\mathfrak{g}$-valued form, as discussed in some detail at [[Weil algebra]].

Composition with the morphism $\mathbf{B}G_{diff} \to \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}$ is composition of the bottom morphism of the above digram with $W(\mathfrak{g}) \leftarrow CE(b^{k-1}\mathbb{R}) : \langle - \rangle$ followed by [[fiber integration]] of the resulting $k$-form

$$
  \Omega^\bullet(X)\otimes \Omega^\bullet(\Delta^0)
  \stackrel{(A,F_A)}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{\langle - \rangle}{\leftarrow}
  CE(b^{k-1}\mathbb{R})
  : 
  \langle F_A \rangle
$$

over the point. This fiber integration is of course trivial, so that we find that indeed $X \stackrel{(A,F_A)}{\to} \mathbf{B}G_{diff} \stackrel{\langlw - \rangle}{\to} \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}_{chn}$ is the [[curvature characteristic form]] defined on $\langle -\rangle$ on $A$.

Next, a homotopy $(A \stackrel{\gamma}{\to} A') : X \cdot \Delta[1] \to \mathbf{B}G_{diff}$ is (again by the [[Yoneda lemma]]) a diagram

$$
  \array{
    C^\infty(X) \otimes \Omega^\bullet(\Delta^1) 
    &\stackrel{\lambda}{\leftarrow}& CE(\mathfrak{g})
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(X) \otimes \Omega^\bullet(\Delta^0)
    &\stackrel{(A,F_A) \stackrel{\gamma}{\to} (A',F_{A'})}{\leftarrow}&
    W(\mathfrak{g})
  }
  \,.
$$

The top morphism defines an $X$-parameterized family of $\mathfrak{g}$-valued 1-form on the interval $[0,1]$, which is canonically identified with a smooth function $g : X \times [0,1] \to G$ into the simply connected [[Lie group]] [[Lie integration|integrating]]] $\mathfrak{g}$ based at the identity, $g(x,0) = e$, by the formula

$$
  \lambda = g^* \theta
$$

where $\theta \in \Omega^1(G, \mathfrak{g})$ is the [[Maurer-Cartan form]] on $G$,

or conversely by [[parallel transport]]

$$
  f(x,s) = P \exp(\int_{[0,s]} \lambda(x,s) d s)
$$

We may think of this as a smooth _path of gauge transformations_ . 

The bottom morphism encodes a $\mathfrak{g}$-valued form

$$
  \hat A + \lambda \in \Omega^1(X \times [0,1] , \mathfrak{g})
$$

with $\hat A \in \Omega^1(X,\mathfrak{g}) \otimes C^\infty([0,1])$ and $\lambda$ as before, such that $\hat A(s = 0) = A$ and $\hat A(s = 1) = A'$.

This is a _smooth path in the space of 1-forms_ . In the case that $\lambda = 0$ this is a _pure shift path_ in the [terminology above](#PathsOfConnections). we look at this case in the following, for ease of notation.

Under composition with $W(\mathfrak{g}) \leftarrow CE(b^{k-1}\mathbb{R}) : \langle -\rangle$ this becomes a $k$-form

$$
  \langle F_{\hat A } \rangle \in \Omega^{k}(X)\otimes C^\infty(\Delta^1)\oplus \Omega^{k-1}(X)\otimes \Omega^1(\Delta^1)
  \,.
$$

The [[fiber integration]] of this over $\Delta^1$ is manifestly the same operation as that in the definition of the Chern-Simons form [above](#PathsOfConnections).

=--




## As secondary characteristic forms

If a [[curvature characteristic form]] _vanishes_ (for instance if the [[connection on a bundle|connection]] is flat or the degree of the curvature characteristic form is simply greater than the dimension of $X$) the corresponding Chern-Simons form is a [[closed form]]. So in this case the [[de Rham cohomology]] class of the curvature characteristic form becomes trivial, but the Chern-Simons form provides another de Rham class. This is therefore called a **[[secondary characteristic class]]**.



### Chern-Simons theory

In particular on a 3-dimensional [[smooth manifold]] $X$ necessarily the Chern-Simons 3-form is closed. The [[functional]]

$$
  (A \in \Omega^1(X,\mathfrak{g}))
  \mapsto
  \int_X CS(A)
$$

is the [[action functional]] of the [[quantum field theory]] called [[Chern-Simons theory]].

More generally, for $X$ a $(2n-1)$-dimensional [[smooth manifold]] and $\langle -,\cdots, -\rangle$ an invariant polynomial of arity $n$, the analous formula defines the [[action functional]] of  $(2n+1)$-dimensional Chern-Simons theory.


## In terms of $\infty$-Lie algebroids

As discussed at [[invariant polynomial]], Chern-Simons elements int the [[Weil algebra]] $W(\mathfrak{g})$ of a [[Lie algebra]] $\mathfrak{g}$ induce the transgression between invariant polynomials and cocycles in [[Lie algebra cohomology]].

For 

$$
  \array{
    T_{vert} P &\stackrel{A_{vert}}{\to}& \mathfrak{g}
    \\
    \downarrow && \downarrow
    \\
    T P &\stackrel{(A,F_A)}{\to}& inn(\mathfrak{g})
    \\
    \downarrow && \downarrow
    \\
    T X &\stackrel{(P_i(F_A))}{\to}& \prod_i b^{n_i} \mathfrak{u}(1)
  }
$$

the data of an [[Ehresmann connection]] on a $G$-[[principal bundle]] expressed as a diagram of [[∞-Lie algebroid]]s with the [[curvature characteristic form]]s on the bottom, a choice of transgression element $cs_P$ for an [[invariant polynomial]] $P$ in transgression with a Lie algebra cocycle $\mu$ induces a diagram

$$
  \array{
    \mathfrak{g} &\stackrel{\mu}{\to}& b^n \mathfrak{u}(1)
    \\
    \downarrow && \downarrow
    \\
    inn(\mathfrak{g}) &\stackrel{(cs_P,P)}{\to}& e b^{n} \mathfrak{u}(1)
    \\
    \downarrow && \downarrow
    \\
    \prod_i b^{n_i}\mathfrak{u}(1) &\stackrel{p_i}{\to}& b^{n+1} \mathfrak{u}(1)
  }
  \,.
$$

The [[pasting]] of this to the above [[Ehresmann connection]] expresses in the middle horizontal morphism the Chern-Simons form $cs_P(A)$ and its [[curvature characteristic form]] $P(F_A)$

$$
  \array{
    T_{vert} P &\stackrel{A_{vert}}{\to}& \mathfrak{g} &\stackrel{\mu}{\to}& 
    b^n \mathfrak{u}(1)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    T P &\stackrel{A}{\to}& inn(\mathfrak{g})
    &\stackrel{(cs_P,P)}{\to}&
    e b^n \mathfrak{u}(1)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    T X &\stackrel{(P_i)}{\to}& \prod_i b^{n_i} \mathfrak{u}(1)
    &\stackrel{p_i}{\to}&
    b^{n+1} \mathfrak{u}(1)
  }
  \,.
$$



## References

The article introducing  the concept is 

* [[Shiing-Shen Chern]], [[James Simons]], _Characteristic forms and geometric invariants_  The Annals of Mathematics, Second Series, Vol. 99, No. 1 (Jan., 1974), pp. 48-69  ([jstor](http://www.jstor.org/pss/1971013)) ([pdf](http://www.dpmms.cam.ac.uk/~hk244/chern-simons.cp.pdf))

As it says in the introduction of this article, it was motivated by an attempt to find a combinatorial formula for the [[Pontrjagin class]] of a [[Riemannian manifold]] (i.e. that associated to the [[orthogonal group|O(n)]]-[[principal bundle]] to which the [[tangent bundle]] is associated) and the Chern-Simons form appeared as a boundary term that obstructed to original attempt to derive the Pontrrjagin class by integrating curvature classes simplex-by-simplex. But 
A combinatorial formula of the kind these authors were looking for was however (nevertheless) given later in

* [[Jean-Luc Brylinski]], [[Dennis McLaughlin]] _&#268;ech cocycles for characteristic classes_ , Comm. Math. Phys.  178  (1996) (<a href="http://www.springerlink.com/content/762g1m76jp6425x5/">pdf</a>)

The statements about "pure shift" paths are reviewed on the first few pages of

* [[James Simons]], [[Dennis Sullivan]], _Structured vector bundles define differential K-theory_ ([arXiv](http://arxiv.org/abs/0810.4935?context=math.DG))

which discusses the relevance of Chern-Simons forms in [[differential K-theory]].

The [[L-∞-algebra]]-formulation is discussed in [SSS08](http://arxiv.org/abs/0801.3480).

An abstract algebraic model of the algebra of Chern's characteristic classes and Chern-Simons secondary characteristic classes and of the gauge group action on this algebra (which also enables some noncommutative generalizations) is pioneered in 2 articles

* Israel M. Gelfand, Mikhail M. Smirnov, _The algebra of Chern-Simons classes, the Poisson bracket on it, and the action of the gauge group_,  Lie theory and geometry, 261--288, Progr. Math. __123__, Birkh&#228;user 1994; _Chern-Simons classes and cocycles on the Lie algebra of the gauge group_, The Gelfand Mathematical Seminars, 1993--1995,  101--122, Birkh&#228;user 1996.

[[!redirects Chern-Simons forms]]