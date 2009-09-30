<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include higher category theory - contents]]


***

[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]


</div>



+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

and

* [[Gromov-Witten invariants]]

see there for background and context.

This entry contains a basic introduction to [[elliptic curve]]s and their [[moduli space]]s.


=--

Previous:

* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]


>the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention, meaning: **somebody should go through this and polish**


***

#Contents#

* toc
{:toc}


#elliptic curves#

**Definition** An [[elliptic curve]] over $\mathbb{C}$ is equivalently

* a [[Riemann surface]] $X$ of [[genus]] 1 with fixed point $P \in X$

* a quotient $\mathbb{C}/\Lambda$ where $\Lambda$ is a [[lattice]] in $\mathbb{C}$;

* a compact complex [[Lie group]] of dimension 1.

* a [[smooth scheme|smooth]] [[algebraic curve]] of degree 3 in $\mathcal{P}$.

**Remark**  The third definition is the one that is easiest to generalize. For our simple purposes, though, the second one will be the most convenient.

From the second definition it follows that to study the [[moduli space]] of [[elliptic curve]]s it suffices to study the [[moduli space]] of [[lattice]]s in $\mathbb{C}$.

**Definition** A **[[framed elliptic curve]]** is an [[elliptic curve]] $(X,P)$ (in the sense of the first definition above) together with an ordered basis $(a,b)$ of $H_1(X, \mathbb{Z})$ with $(a \cdot b) = 1 $

A **framed lattice** in $\mathbb{C}$ is a lattice $\Lambda$ together with an ordered basis $(\lambda_1, \lambda_2)$ of $\Lambda$ such that $Im(\lambda_2/\lambda_1) \gt 0$.

(So turning $\lambda_1$ to $\lambda_2$ in the plane means going counterclockwise).

#moduli spaces of elliptic curves#

this implies that

the [[upper half plane]] $\mathfrak{h}$ is in bijection with framed lattices in $\mathbb{C}$ which in turn is in bijection with [[isomorphism]] classes of framed elliptic curves over $\mathbb{C}$

$$
  \mathfrak{h}
  \simeq
  \{framed lattices in \mathbb{C}\}
  \simeq
  \{framed elliptic curves over \mathbb{C}\}/_\sim
$$

and we have

$$
  \{elliptic curves over \mathbb{C}\}_\sim
  \simeq
  \mathfrak{h}/{SL_2(\mathbb{Z})}
$$

where $SL_2(\mathbb{Z}) = \left\{ \left(\array{a & b \\ c & d }\right)| a d - c d = 1\right\}$ acts  by

$$
  \tau \mapsto \frac{a \tau + b}{c \tau + d}
$$

**Claim** the quotient $\mathfrak{h}/_{SL_2(\mathbb{Z})}$ is [[biholomorphic map|biholomorphic]] to the disk and has a unique structure of a [[Riemann surface]] which makes the quotient map
$\mathfrak{h} \to \mathfrak{h}/SL_2(\mathbb{Z})$ a [[holomorphic map]]

>**warning** possibly something wrong here, audience doesn't believe the bit about the disk

**definition** write $M_{1,1} := \mathfrak{h}/SL_2(\mathbb{Z})$

**definition** a **homolorphic family of [[elliptic curve]]s** over a [[complex manifold]] $T$ is 

* a holomorphic map $\pi : X \to T$ 

* together with a [[section]] $s : T \to X$ of $\pi$ such that for any $t \in T$ the pair $(X_t, s(t))$ is an [[elliptic curve]] (using the first definition above).

For every family 

$$
  \array{
    X \\ \downarrow^\pi \\ T 
  }
$$

we would like to have $F \to M_{1,1}$
$$
  \array{
    X \simeq \phi^* F &\to& F
    \\
    \downarrow & & \downarrow
    \\
    T &\to& M_{1,1}
  }
$$

where

$$
  \phi:   t \mapsto [X_t, s(t)]
$$

such that

* $\phi : T \to M_{1,1}$ is a [[holomorphic map]]

* every [[holomorphic map]] $T \to M_{1,1}$ corresponds to a family over $t$;

* there is a universal family over $M_{1,1}$

This is _impossible_ . One can construct explicit counterexamples. These counterexamples involved [[elliptic curve]]s with nontrivial [[automorphism]]s. 

For instance

$$
  \{
    (x,y,z) \in \mathbb{P}^2 \times X : 
    y^2 = x(x-1)(x-\lambda)
  \}
  \to
  X := \mathbb{P}^1 - \{0,1,\infty\}
$$


> but see the discussion at [[moduli space]] for a discussion of the statement "it's te automorphisms that prevent the [[moduli space]] from existing"


consider

$$
  \mathbb{Z}^2 \hookrightarrow \mathbb{C} \times \mathfrak{h}
$$

given by

$$
  (m,n) : 
  (z,\tau)
  \mapsto
  (z + m \tau + n, \tau)
$$

Then consider the family

$$
  \array{
     E := \mathbb{C}/_{\mathbb{Z}^2} \times \mathfrak{h}
    \\ \downarrow \\ \mathfrak{h}
  }
$$

is a family of [[elliptic curve]]s over $\mathfrak{h}$

and $E_\tau = \mathbb{C}/{\Lambda_\tau}$ with

$$
  \Lambda_{\tau} := \mathbb{Z}\cdot 1 \oplus \mathbb{Z}\cdot \tau
$$

is a family of framed elliptic curves.

**fact** the space $\mathfrak{h}$ with the family $E \to \mathfrak{h}$ is a [[fine moduli space]] for [[framed elliptic curve]]s.

Consider any map $\phi : T \to \mathfrak{h}$

with pullback of the universal family

$$
  \array{
     X \stackrel{?}{\to} \phi^* E &\to & E
    \\
    \downarrow && \downarrow
    \\
    T &\stackrel{\phi}{\to}&
    \mathfrak{h} 
  }
$$

**claim** for every point $t \in T$ there is an open neighbourhood $t_0 \in U \hookrightarrow T$ such that one can choose [[differential form|1-forms]] $\omega_t$ on $X_\tau$ which vary holomorphically with respect to $t$.

Notice that _locally_ every family of elliptic curves is framed (since we can locally extend a choice of basis for $H_1$).  So 

$$
  \array{
    && \mathfrak{h}
    \\
    && \downarrow^{SL_2(\mathbb{Z})}
    \\
    M_{1,1} &\stackrel{Id}{\to}&
    M_{1,1}
  }
$$

at $i$ and $\rho = e^{2\pi i/6}$ , $C = \{\pm I\}$

isn't locally liftable at $i$ and $\rho$ so it is not a univresal family of unframed curves.

#orbifolds#

**definition** A **basic pointed orbifold** (basic meaning global) is a triple $X//\Gamma := (X,\Gamma,\rho)$, where 

* $X$ is a [[connected space|connected]] and [[simply connected space|simply connected]] [[topological space]] (or in other variants a [[complex manifold]] or whatever is under consideration)

* $\Gamma$ is a discrete [[group]]

* $\rho : \Gamma \to Aut(X)$ is a group homomorphism

(here "pointed" because we specified the action $\rho$ instead of its iso-class under the following morphisms)

A morphism from  $(X,\gamma, \rho)$ to $(X', \Gamma', \rho')$ is a pair

$$
  (f,\phi)
$$

where

* $f : X \to X'$ is a continuous map

* $\phi : \Gamma \to \Gamma'$ is a group homomorphism

such that for all $\gamma \in \Gamma$

$$
  \array{
    X &\stackrel{f}{\to}& X'
    \\
    \downarrow^{\gamma} && \downarrow^{\phi(\gamma)}
    \\
    X &\stackrel{f}{\to}& X'
  }
$$

This really leads an enlargement of the plain category of spaces:

**remark** We have a faithful embedding of spaxces into orbifolds defined this way: for any connected semi-locally simply connected space $X$ with [[universal cover]] $\tilde X$
we have

$$
  X \mapsto \tilde X //\pi_1(X)
$$

> **warning** notice all the simply-connectedness assumoptions above for making sense of this

**remark** let $X$ be a [[nice topological space]]. Let $G = \pi_1(X)$ be its first [[homotopy group]] and let a discrete group $\Gamma$ action on $X$.

then define

$$
  \tilde \Gamma :=
  \left\{
    (\gamma,g)
    \in
    \Gamma \times Aut(\tilde X)
    |
    \array{
       \tilde X &\stackrel{g}{\to}& \tilde X
       \\
       \downarrow^p && \downarrow^p
       \\
       X &\stackrel{\gamma}{\to}& X
    }
  \right\}
$$

then we have an exact sequence

$$
  1 \to G \to \tilde \Gamma \to \Gamma \to 1
$$

where $G \to \tilde \Gamma$ is given by $(g \mapsto (1,g))$ and $\tilde \Gamma \to \Gamma$ by $(\gamma,g) \mapsto \gamma$.

**definition** 

For an [[orbifold]] $(X,\Gamma,\rho)$ write $I \times (X,\Gamma,\rho) := (I \times X, \Gamma, \rho)$.

Then a **homotopy** from $(f,\phi)$ to $(f',\phi') : (X,\Gamma, \rho) \to (X',\Gamma', \rho')$

is a map

$$
  (F,\Psi) : I \times (X, \Gamma, \rho) \to (X', \Gamma', \rho')
$$

such that 

* $\Psi = \phi = \phi'$

* $f(-) = F(0,-)$, $f'(-) = F(1,-)$

now write

$$
  S^1 := (\mathbb{R}, \mathbb{Z})
$$

(the circle regarded as a global orbifold)

**definition**

The first [[homotopy group]] for our definition of orbifold is:

$$
  \pi_1(X//\gamma) 
  \simeq
  \{
    homotopy classes of maps S^1 \to X//\Gamma
  \}
$$

**exercise** show that this is $\cdots \simeq \Gamma$

>(recall again the simply-connectness assumoption!!)

*definition** A morphism

$$
  (f,\phi) : (X,\Gamma) \to (X',\Gamma')
$$

is a [[weak homotopy equivalence]] if $\phi$ is an ismorphism and $H_\bullet(f) : H_\bullet(X) \to X_\bullet(X')$. 

**note** Let $E \Gamma$ be a contractible space on which $\Gamma$ acts properly, dic. and free, then 

$$
  (E \Gamma \times X, \Gamma)
  \stackrel{(f,\phi)}{\to}
  (X,\Gamma)
$$

with $\phi = Id_\Gamma$ and $f$ the projection is a [[weak homotopy equivalence]].

**definition** a [[local system]] $V$ on $(X,\Gamma)$ with fiber $V$ a group homomorphism $\Gamma \to Aut(V)$ with

**definition**

Introduce the following notation for [[homotopy group]]s, [[homology]] and [[integral cohomology]] of our [[orbifold]]s with coefficients in a local system:

* $\pi_n(X//\Gamma)$ := \pi_n(X)$ for $n \geq 2$

* $H_\bullet(X//\Gamma, V) := H_\bullet(E \Gamma \times_\Gama X, V)$  

* $H^\bullet(X//\Gamma, V) := H^\bullet(E \Gamma \times_\Gama X, V)$

**example** ${*}//\Gamma$ has a [[weak homotopy equivalence]] to the [[classifying space]] $\mathcal{B}\Gamma$

it follows that for local system $V$ we have

$$
  H^\bullet({*}//\Gamma, V) = H^\bullet_{gp}(\Gamma,V)
$$

where on the right we have [[group cohomology]]

***

We have all kinds of constructions on orbifolds by saying they are structures on $X$ with suitable extension of the action of $\Gamma$ to them

A **[[vector bundle]] on an orbifold** $V \to X//\Gamma$ is a vector bundle $V \to X$ with isomorphism action by $\Gamma$ specified, covering that on $X$.

for instance the [[tangent bundle]] of $X //\Gamma$ is given by $(T X)//\Gamma \to X//\Gamma $ in the obvious way.

**definition** say that $\Gamma$ acts virtually freely if $\exists$ a finite index subgroup $\Gamma'$ of $\Gamma$ which acts freely on $X$.

**note** $SL_2(\mathbb{Z})$ acts virtually freely on $\mathfrak{h}$

$$
  SL_2(\mathbb{Z})[m]
  \to
  SL_2(\mathbb{Z})
  \to SL_2(\mathbb{Z}/ m \mathbb{Z})
$$

Let $\Gamma' \lt \Gamma$ be a finite index subgroup which acts freely on $X$.

set

$$
  X' := X// \Gamma'; 
$$

the map

$$
  X/\Gamma' \to X//\Gamma
$$

**must be viewed as an unramified covering of degree $[\Gamma:\Gamma']$.**

> supposedly important statement

**definition**

the [[Euler characteristic]] of a global orbifold is

$$
  \chi(X//\Gamma) :=
  \frac{1}{[\Gamma: \Gamma']} \chi(X/\Gamma')
$$

> compare [[groupoid cardinality]]


#moduli stack/orbifold of elliptic curves#

**definition** 

Define now the global orbifold

$$
  \mathcal{M}_{1,1} := \mathfrak{h}//SL_2(\mathbb{Z})
$$

**proposition**

$$
  H_1(\mathcal{M}_{1,1}, \mathbb{Z})
  = \mathbb{Z}/12\mathbb{Z}
$$

$$
  H^1(\mathcal{M}_{1,1}, \mathbb{Z}) = 0
$$

$$
  H^2(\mathcal{M}_{1,1}, \mathbb{Z})
  = \mathbb{Z}/12 \mathbb{Z}
$$

$$
  H_\bullet(\mathcal{M}_{1,1}, \mathbb{Q})
  \simeq
  H_\bullet(M_{1,1}, \mathbb{Q})
$$

and similarly for [[integral cohomology]]

$$
  \chi(\mathcal{M}_{1,1}) = -\frac{1}{12}
$$

$$
  Pic(\mathcal{M}_{1,1}) \simeq \mathbb{Z}/12\mathbb{Z}
$$

> so... to be continued