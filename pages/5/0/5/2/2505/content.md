
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--







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

Next:

* [[A Survey of Elliptic Cohomology - equivariant cohomology]]



>the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention, meaning: **somebody should go through this and polish**


***

#Contents#

* toc
{:toc}


#elliptic curves#

**Definition** An [[elliptic curve]] over $\mathbb{C}$ is equivalently

* a [[Riemann surface]] $X$ of [[genus]] 1 with a fixed point $P \in X$

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

# topological invariants of the moduli stack # 

Since the upper half plane is contractible, the homotopy type of $\mathfrak{h}//\mathbb{Z}_2$ are the same as that of $* // \mathbb{Z}_2$ and similarly for the (group)cohomology

$$
  H^\bullet(\mathcal{M}_{1,1}, \mathbb{Z})
  = H\bullet(SL_2(\mathbb{Z}), \mathbb{Z})
$$


and similalry for homology.

In particular

$$
  H_1(\mathcal{M}_{1,1}, \mathbb{Z})
  \simeq
  SL_2(\mathbb{Z})^{ab} \simeq \mathbb{Z}/12\mathbb{Z}
$$

for all $m \in \mathbb{N}$ then

$$
  1 \to SL_2(\mathbb{Z})[m]
  \to 
  SL_2(\mathbb{Z})
  \to 
  SL_2(\mathbb{Z}/m \mathbb{Z})
  \to 
  1
$$

so that

$$
   H^1(\mathcal{M}_{1,1}, \mathbb{Z})
  =
  0
$$

**fact** the group $SL_2(\mathbb{Z})[m]$ is free for $m \gt 2$.

so far all $\mathbb{Q}$-representations $V$ we have

$$
  H^k(SL_2(\mathbb{Z}), V)
  \simeq
  H^l(SL_2(\mathbb{Z}), V)^{SL_2(\mathbb{Z}/m\mathbb{Z})}
$$

due to the freeness we have also that

$$
  H^k(SL_2(\mathbb{Z}), V) = 0
$$

for $k \geq 2$

and hence

$$
  H^2(SL_2(\mathbb{Z}), \mathbb{Z})
$$

is [[torsion]]

$$
  \cdots \simeq
  Hom(H_1(SL_2(\mathbb{Z}), \mathbb{Z}), \mathbb{Q}/\mathbb{Z})
  \simeq
  \mathbb{Z}/12 \mathbb{Z}
  \,.
$$

**proposition** 

as [[orbifold]]s, we have an isomorphism

$$
  \mathcal{M}_{1,1} \simeq
  X//(S_3 \times C_2)
$$

where

$$
  X :=
\mathbb{P}^1 - \{0,1, \infty\}
$$

and $S_3$ acts on that by permuting $0,1, \infty$. (Think of $\mathbb{P}^1$ as the [[Riemann sphere]]: there is a unique holomorphic automorphism of that permuting these three points in a given fashion.) While $C_2$ acts trivially.

*proof** 

$$
  \array{
   1 \to SL_2(\mathbb{Z})[2]
   &\to& 
   SL_2(\mathbb{Z})
   &\to& 
   S_3 \simeq SL_2(\mathbb{Z}/2\mathbb{Z})
   &\to& 
   1
   \\
   &&& {}_{\phi}\searrow& \downarrow
   \\
  &&&& PSL_2(\mathbb{Z})
  }
$$

now $PSL_2(\mathbb{Z})[2]$ is known to be torsion free. It acts in a standard way on the [[upper half plane]] $\mathfrak{h}$.

A little discussion shows that

$$
  \mathfrak{h}/PSL_2(\mathb{Z})[2]
  \simeq
  X
$$

this implies that

$$
  PSL_2(\mathbb{Z})[2]
  \simeq
  F_2
$$

the [[free group]] on two generators. 

Then the second but last map

$$
  1 \to C_2 \to SL_2(\mathbb{Z})[2]
  \to 
  F_2
  \to 1
$$

has a [[section]], from which we get that 

$$
  SL_2(\mathbb{Z})[2]
  \simeq
  F_2 \times C_2
$$


and so

$$
  X//(C_2 \times S_3)
  \simeq
  (X//C_2) // S_3
  \simeq
  ((\mathfrak{h}// SPL_2(\mathbb{Z})[2])//C_2)//S_3
  \simeq
  ((\mathfrak{h}//PSL_2(\mathbb{Z}[2]))//S_3)
  \simeq
  \mathfrak{h}/ SL_2(\mathbb{Z})
$$

which is the **end of the proof**.

**corollary** The [[Euler characteristic]] of the [[moduli stack]] of [[elliptic curve]]s is

$$
  \chi(\mathcal{M}_{1,1}) = \frac{-1}{12}
  \,.
$$

now consider the line bundle

$$
  \array{
    \mathbb{C} \times \mathfrak{h}
    \\
    \downarrow
    \\
     \mathfrak{h}//SL_2(\mathbb{Z}) 
  }
$$

with action on the total space for $k \in\mathbb{Z}$

$$
  \left(
    \array{
      a & b \\ c & d
    }
  \right)
  :
  (z, \tau)
  \mapsto
  (c \tau + d)^k z, \frac{a \tau + b}{c \tau + d}
$$

call this [[line bundle]] on the [[moduli stack]] $\mathcal{L}_k \to \mathcal{M}_{1,1}$. We will see that all line bundles are isomorphic to one of these.

**remark**

$$
  f : \mathfrak{h} \to \mathcal{C}
$$

is a [[section]] of $\mathcal{L}_k$ iff

$$
  f\left(
    \frac{a \tau + b}{c \tau + d}
  \right)
  =
  (c \tau + d)^k f(\tau)
$$

hence precisely if it defines a [[modular function]] of weight $k$! This gives a geometric interpretation of modular functions.

$$
  \array{
    \mathbb{C} \times \mathfrak{h}
    \\
    \downarrow
     \\
     \mathfrak{h}
  }
$$

and define an action of $G := SL_2(\mathbb{Z}) \letimes \mathbb{Z}^2$

where $\mathbb{Z}^2$ acts on $SL_2(\mathbb{Z})$ by

$$
  \left(
    \array{
       a & b \\ c & d
    }
  \right)
   : (m , n)
   \mapsto 
   a m + b m, c m + d n
$$

and on $\mathbb{C} \times \mathfrak{h}$ by

$$
  (m, n) : (z,\tau) \mapsto (z + m \tau + n, \tau)
$$

the resulting bundle 

$$
  \array{
    \mathbb{C} \times \mathfrak{h}//G
    \\
    \downarrow
     \\
     \mathcal{M}_{1,1}
  }
$$


we call

$$
  \mathcal{E} \to \mathcal{M}_{1,1}
$$

**theorem** for any [[complex manifold]] $T$ there is a bijection between families of elliptic curves over $T$ and [[orbifold]] maps $T \to \mathcal{M}_{1,1}$ classify them.

Suppose we have an "isotrivial family" (meaning all fibers are isomorphic elliptic curves, i.e. a fiber bundle of elliptic curves)

$$
  \array{
    
    \\
    \downarrow
    \\
    T &\stackrel{\phi}{\to}& \mathcal{M}_{1,1}
  }
$$

recall that the group that defines $T$ as an [[orbifold]] is the first [[homotopy group]] $\pi_1(T)$.

The only condition that we get from the definition of orbifold maps is that

$$
  \phi : \pi_1(T) \to SL_2(\mathbb{Z})
$$

factors through the [[stabilizer group]] $\simeq Aut(E_p)$ of our base point $p \in \mathcal{M}_{1,1}$ 



# compactified moduli stack #

one can see that over _compact_ $T$ with $\mathcal{M}_{1,1}$ we cannot have nontrivial famlies _without_ singular fibers.

To get around that we want a **compactification** $\bar \mathcal{M}_{1,1}$ of the [[moduli stack]].

also fur purposes of intersection theory, we need to further compactify.


recall the  description of $\mathcal{M}_{1,1}$ as a weak quotient of $\mathbb{P}^1$.  Then consider:

**definition** 

Let

$$
  \bar \mathcal{M}_{1,1} := \mathbb{P}^1//(C_2 \times S_3)
$$

otice that this is now an [[orbifold]] which is no longer _basic_ by the above definition. In fact, we can cover it by charts of basic orbifolds as follows: consider


$$
  \array{
    && \mathfrak{h}//(C_2 \times \mathbb{Z})
    \\
    &  \swarrow && \searrow
    \\
    \mathfrak{h}//SL_2(\mathbb{Z})
    &&&&
    \mathbb{D}//C_2
  }
$$

>with the arrows being maps of orbifolds whose precise details I haven't typed.

then let $\mathbb{D}^*$ be the punctured disk and realize the diagram

$$
  \array{
    && \mathbb{D}^*//C_2
    \\
    &  \swarrow && \searrow
    \\
    \mathcal{M}_{1,1}
    &&&&
    \mathbb{D}//C_2
  }
$$

where the right morphism is just the inclusion

now we build a chart of $\bar \mathcal{M}_{1,1}$ consisting of the two patches $\mathcal{M}_{1,1}$ and $\mathbb{D}/C_2/$

from this we get the alternative

**definition** 

$$
  \bar \mathcal{M}_{1,1}
  :=
  \mathcal{M}_{1,1} \coprod_{\mathbb{D}^*//C_2}
  \mathbb{D}//C_2
$$


the [[colimit]] on the right manifestly glues in the "point at infinity" that is not hit by the map $\mathbb{D}^*//C_2 \to \mathcal{M}_{1,1}$.

# Gromov-Witten invariants  #

**definition** A **stable curve** (over $\mathcal{C}$) of genus $g$ with $n$ marked points is a proper, connected curve with $n$ smooth marked points such that all singularities are nodes and such that the the [[automorphism]] group (of autos respecting the smooth marked points) is finite,

$$
  |Aut(C)| \lt + \infty
$$

and such that the [[arithmetic genus]] is $g$.

Now $\bat \mathcal{M}_{g,n}$ is the [[fine moduli space]] for smooth curves of genus $g$.


There is a [[line bundle]]

$$
  \mathcal{T}_i^* \to \bar \mathcal{M}_{g,n}
$$

built fiberwise from the cotangent spaces of the elliptic curves. 

one of them is obtained from one of the $n$ sections $s_i$ of the universal family $\mathcal{F} \to \bar \mathcal{M}_{g,n}$. The fiber over a point is the cotangent space of the elliptic curve over that point at this section.


Write for the first [[Chern class]] 

$$
  c_1(\mathcal{T}_i^*) = \Psi_i
$$

$$
  k_1, \cdots, k_n
  \in \mathbb{Z}_{\geq 0}
$$

such that 

$$
  \sum_{i = 1}^n k_i = 3 g - 3 + n
$$

then we get numbers called the [[Gromov-Witten invariants]] ("of the point")

$$
  \langle 
    \tau_{k_1}, \cdots, \tau_{k_n}
  \rangle_g
   :=
  \int_{\bar \mathcal{M}_{1,1}}
  \prod_{i = 1}^n
   \Psi_i^{k_i} 
$$

## example: $\langle \tau_1\rangle_1$ ##

Let $x, y$ by affine coordinates on $\mathbb{P}^2$

Let $f(x,y)$ and $g(x,y)$ be two generic cubics, in particular there are nine joint zeros

$$
 |\langle (x,y)| f(x,y) = g(x,y) = 0\rangle| = 0
$$

called $p_1, \cdots, p_9$.

define then

$$
  F := 
  \left\lbrace
    (x,y,t)
    \in \mathbb{P}^2 \times \mathbb{P}^1
    :
    f(x,y) - t g(x,y) = 0
  \right\rbrace
$$

and consider

$$
  \array{
    F
    \\
    \downarrow^{pr_2}
    \\
    \mathbb{P}^1
    &\stackrel{\phi}{\to}&
    \bar \mathcal{M}_{1,1}
    \\
    &\searrow & \downarrow^{q}
    \\
    && \bar M_{1,1}
  }
$$

That map $q$ has degree $\frac{1}{2}$ (!) since $\mathbb{P}^1 \to \bar \mathcal{M}_{1,1}$ has degree 12

we also find that the diaginal map $\mathbb{P}^1 \to \bar M_{1,1}$ has degree 12. It follows that $\phi$ has degree 24:

$$
  deg(\phi) = 24
  \,.
$$

Now let $\mathcal{T}_i^* \to \bar \mathcal{M}_{g,n}$ be one of these line bundles. Consider the [[pullback]] $\phi^*(\mathcal{T}_1)$

then by some argument not reproduced here we find

$$
  \int_{\mathbb{P}^1} c_1(\phi^*(\mathcal{T}_1)^*)
  \,.
$$

Then since the order of $\phi$ is 24 we find that the first [[Gromov-Witten invariant]] is

$$
  \langle
    \tau_1
  \rangle_1
  =
  \frac{1}{24}
  \,.
$$

#extending structures to the compactified moduli space#

recall that the [[moduli stack]] of [[elliptic curve]] is, as a global [[orbifold]]

$$
  \mathcal{M}_{1,1} := \mathfrak{h}//SL_2(\mathbb{Z})
$$

and also

$$
  \cdots \simeq (\mathbb{P}^1 - \{0,1,\infty\})//(C_2 \times S_3)
$$

and there is a [[line bundle]] on this given by

$$
  \mathcal{L}_k :=
  (\mathbb{C} \times \mathfrak{h})//SL_2(\mathbb{Z})
$$

where the action is given by

$$
  \left(
    \array{
       a& b \\ c & d      
    }
  \right)
  : (z, \tau)
   \mapsto
   (c\tau + d)^{k} z, \frac{a \tau + b}{c \tau + d}
$$


since $SL_2(\mathbb{Z})^{ab} = \mathbb{Z}/12\mathbb{Z}$
one finds the [[Picard group]]

$$
  Pic \mathcal{M}_{1,1} \simeq \mathbb{Z}/12\mathbb{Z}
$$

meromorphic (holomorphic) sections $f$ of $\mathcal{L}_k$ are [[modular function]]s of weight $k$, i.e. $f : \mathfrak{h} \to \mathbb{C}$ such that

$$
  \forall \gamma = (\frac{a b}{c d}) \in SL_2(\mathbb{Z})
  : 
  f(\gamma \tau) = (c \tau + d)^k f(\tau)
$$

the **universal elliptic curve** over $\mathcal{M}_{1,1}$ is

$$
  \mathcal{E} := (\mathbb{C} \times \mathfrak{h})//(SL_2(\mathbb{Z}) \ltimes \mathbb{Z}^2)
$$

Then we ended last time with describing the compactified moduli space 

$$
  \bar \mathcal{M}_{1,1} := \mathbb{P}^1//(C_2 \times S_3)
$$

## extending the line bundles ##

**proposition** $\mathbb{L}_k$ has a universal extension $\bar \mathcal{L}_k$ to $\bar \mathcal{M}_{1,1}$

**proof** 

take

$$
  (\mathbb{C} \times \mathbb{D}//C_2) \to (\mathbb{D}//C_2)
$$

where $C_2$ acts by 

$$
  \pm 1 \;\; (z,\tau) \mapsto (\pm^k z , \tau)
$$

note that since $\left(\array{1 & n \\ 0 1}\right) \in S_2(\mathbb{Z})$ for all $n \in \mathbb{Z}$ ay [[modular function]] $f : \mathfrak{h} \to \mathbb{C}$

$$
  f(\tau)
  =
  \sum{-\infty}^\infty
  a_n q^ n
$$

where $q := e^{2 \pi i \tau}$

is called a holomorphic **[[modular form]]** of weight $k$ if $f : \mathfrak{h} \to \mathbb{C}$ is holomorphic and $a_n = 0$ for all $n \lt 0$

**remark** modular forms of weight $k$ are in bijection with sections of the line bundle $\bar \mathcal{L}_k$.

**example** for any [[lattice]] $\Lambda$ in $\mathbb{C}$ and for any $k \gt 2$ we have

$$
  S_k(\Lambda) := \Sum_{0 \neq \lambda \in \Lambda}
    \frac{1}{\lambda^k}
$$

obviously for all $u \in \mathbb{C}^*$ $S_k(u \Lambda) = u^{-k} S_k(\Lambda)$

and for all $\tau \in \mathfrak{h}$ with $C_k(\tau) := S_k(\Lambda_\tau)$ it follows that $G_k : \mathfrak{h} \to \mathbb{C}$ is holomorphic

since $\Lambda_{\gamma \tau} = (c \tau + d)^{-1} \Lambda_\tau$ it follows that $G_k$ is a modular function of weight $k$

**fact** $G_{2k} = 2 \zeta(2 k) &#252; 2 \frac{(2 \pi i)^{2k}}{(2k-1)!} \sum_{n=1}^\infty b_{2k-1}(n)q^n$

with $b_k(n) := \sum_{d|n} d^k$ and where $\zeta$ is the [[zeta-function]]

it follows that

$G_{2k}$ is a modular form of weight $2k$ (which is not a cusp form).

an important cusp form is

setting $g_2 = 60 G_4$ and $g_3 = 140 G_6$

the [[modular form]]

$$
  \Delta := g_2(\tau)^3 - 27 g_3(\tau)^2
$$

is a cusp form of weight 12. $\Delta$ does not have any 0 in $\mathfrak{h}$ and it has a simple zero at $q = 0$.

we have an isomorphism

$$
  \bar \mathcal{L}_{12}
  \simeq
  \mathcal{O}_{\bar \mathcal{M}_{1,1}(\infty)}
$$

where on the right is the sheaf with at most a pole at $\infty$. This isomorphism going from right to left is induced by multiplication with $\Delta$. 

we have an exact sequence

$$
  0 \to \mathbb{Z} \to Pic(\bar \mathcal{M}_{1,1})
  \to \mathbb{Z}/12\mathbb{Z} \to 0
$$

where the first nontrivial map sends 1 to $\bar \mathcal{L}_{12}$ and the second one $\bar \mathcal{L}_1$ to the generator.

set for all $k$

$$
  M_k := \{modular forms of weight k\}
$$

$$
  M_k^\circ := \{cusp forms of weight k\}
$$

**proposition** $M_\bullet$ is an even graded algebra freely generated by $G_4$ and $G_6$ and the ideal $M_\bullet^\circ$ is generated by $\Delta$.

the dimensions are

$$
  dim M_{2k}  =
  \left\{
     floor k/6 & for k = 1 mod 6
     \\
     1+ floor k/6 & otherwise
  \right.
$$

> ???????

## extending the universal family of elliptic curves  ##

Recall the three definition of [[elliptic curve]]s from above.

Now a fourth definition:

**definition** an elliptic curve is a smooth curve of degree 3 in $\mathbb{C}\mathbb{P}^2$ together with a point in it.

* that this equation implies the first one above follows from the genus formula, which says that a degree $n$ curve as in the definition has genus $g = \frac{(n-1)(n-2)}{2}$

* that the first def implies this one 