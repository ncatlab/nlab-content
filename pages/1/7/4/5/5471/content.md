
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

For $\mathcal{G}$ a [[geometry (for structured (∞,1)-toposes)]] a $\mathcal{G}$-[[structured (∞,1)-topos]] $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is _locally representable_ if it is locally equivalent to $Spec U$ for $U \in Pro(\mathcal{G})$ (the [[pro-objects in an (∞,1)-category]]), or $U \in \mathcal{G}$ itself if it is _locally finite presented_ .

This generalizes

* the notion of [[smooth manifold]] from [[differential geometry]];

* the notion of [[scheme]] from [[algebraic geometry]].

* etc.

## Definition

Let $\mathcal{G}$ be a [[geometry (for structured (∞,1)-toposes)]]. Write $\mathcal{G}_0$ for the underlying
discrete geometry. The identity functor

$$
  p : \mathcal{G}_0 \to \mathcal{G}
$$

is then a morphism of geometries.

Recall the notation $LTop(\mathcal{G})$ for the [[(∞,1)-category]] of $\mathcal{G}$-[[structured (∞,1)-topos]]es and [[geometric morphism]]s between them.

### Affine $\mathcal{G}$-schemes 

+-- {: .num_theorem}
###### Theorem ( [[Structured Spaces|StSp]] 2.1.1 )

There is a pair of [[adjoint (∞,1)-functor]]s

$$
  p^* : LTop(\mathcal{G}) \stackrel{\leftarrow}{\to}
  LTop(\mathcal{G}_0)
  : 
  \mathbf{Spec}_{\mathcal{G}_0}^{\mathcal{G}}
$$

with $\mathbf{Spec}_{\mathcal{G}_0}^{\mathcal{G}}$
 left adjoint to the canonical functor $p^*$ given by precomposition with $p$.

=--

+-- {: .num_remark}
###### Remark ( [[Structured Spaces|StSp]] p. 38 )

There is a canonical morphism

$$
  can :
  Pro(\mathcal{G})^{op}
  \to
  LTop(\mathcal{G}_0)
$$

=--


+-- {: .num_defn}
###### Definition ( affine $\mathcal{G}$-scheme, [[Structured Spaces|StSp]] 2.3.9)

Write $\mathbf{Spec}^{\mathcal{G}}$ for the [[(∞,1)-functor]]

$$
  \mathbf{Spec}^{\mathcal{G}} :
  Pro(\mathcal{G})^{op}
  \stackrel{can}{\to}
  LTop(\mathcal{G}_0)
  \stackrel{
    \mathbf{Spec}_{\mathcal{G}_0}^{\mathcal{G}}
  }{\to}
  LTop(\mathcal{G})
  \,.
$$

A $\mathcal{G}$-[[structured (∞,1)-topos]] in the image of this functor is an **affine $\mathcal{G}$-scheme**.

=--

### $\mathcal{G}$-Schemes 

+-- {: .num_defn}
###### Definition (geometric scheme, [[Structured Spaces|StSp]] 2.3.9)

Let $\mathcal{G}$ be a [[geometry (for structured (∞,1)-toposes)]].

A $\mathcal{G}$-[[structured (∞,1)-topos]] $(\mathcal{X},\mathcal{O}_{\mathcal{X}})$ is a **$\mathcal{G}$-scheme** if 

* there exists a collection $\{U_i \in \mathcal{X}\}$ 

such that

* the $\{U_i\}$ cover $\mathcal{X}$ in that the canonical morphism $\coprod_i U_i \to {*}$ (with ${*}$ the [[terminal object]] of $\mathcal{X}$) is an [[effective epimorphism]];

* for every $U_i$ there exists an equivalence

  $$
   (\mathcal{X}/{U_i}, \mathcal{O}_{\mathcal{X}}|_{U_i})
   \simeq \mathbf{Spec}^{\mathcal{G}} A_i
  $$

  of structured $(\infty,1)$-toposes for some $A_i \in Pro(\mathcal{G})$ (in the [[(∞,1)-category]] of [[pro-object]]s of $\mathcal{G}$).

=--

+-- {: .num_defn}
###### Definition (pregeometric scheme, [[Structured Spaces|StSp]], 3.4.6)


For $\mathcal{T}$ a pregeometry, a $\mathcal{T}$-[[structured (infinity,1)-topos]]
$(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is a **$\mathcal{T}$-scheme** if 
it is a $\mathcal{G}$-scheme for [[generalized the|the]] geometric envelope
$\mathcal{G}$ of $\mathcal{T}$.

This means that
for $f : \mathcal{T} \to \mathcal{G}$ [[generalized the|the]]  geometric envelope and
for $\mathcal{O}'_{\mathcal{X}}$
[[generalized the|the]] $\mathcal{G}$-structure on $\mathcal{X}$ such that
$\mathcal{O}_{\mathcal{X}} \simeq \mathcal{O}'_{\mathcal{X}} \circ f$, we have
that $(\mathcal{X}, \mathcal{O}'_{\mathcal{X}})$ is a $\mathcal{G}$-scheme.

=--


### Smooth $\mathcal{G}$-schemes 

Let $\Tau$ be a [[pregeometry (for structured (∞,1)-toposes)]] and let $\Tau \hookrightarrow \mathcal{G}$ be an inclusion into an enveloping [[geometry (for structured (∞,1)-toposes)]].

We think of the objects of $\Tau$ as the _smooth_ test spaces -- for instance the [[cartesian product]]s of some affine line $R$ with itsef -- and of the objects of $\mathcal{G}$ as affine test spaces that may have singular points where they are not smooth.

The idea is that a _smooth_ $\mathcal{G}$-scheme is a $\mathcal{G}$-structured space that is locally not only equivalent to objects in $\mathcal{G}$, but even to the very nice -- "smooth" -- objects in $\mathcal{Tau}$.

+-- {: .num_defn}
###### Definition ( smooth $\mathcal{G}$-scheme, [[Structured Spaces|StSp]] 3.5.6)

With an envelope $\Tau \hookrightarrow \mathcal{G}$ fixed, a $\mathcal{G}$-scheme is called **smooth** if there the affine schemes $\mathbf{Spec}^{\mathcal{G}} A_i$ appearing in its definition may be chosen with $A_i$ in the image of the includion $\tau \hookrightarrow \mathcal{G}$.

=--



### Examples

#### Ordinary schemes 

See the discussion at [[derived scheme]] for how ordinary [[scheme]]s are special cases of [[generalized scheme]]s.

#### Ordinary Deligne-Mumford stacks 

See the discussion at [[derived Deligne-Mumford stack]] for how ordinary [[Deligne-Mumford stack]]s are special cases of [[derived Deligne-Mumford stack]]s.

#### Derived schemes

+-- {: .num_defn}
###### Definition (derived scheme, [[Structured Spaces]], 4.2.8)

Let $k$ be a commutative ring. Recall the pregoemtry $\mathcal{T}_{Zar}(k)$.

A **[[derived scheme]]** over $k$ is a $\mathcal{T}_{Zar}(k)$-scheme.

=--

#### Derived smooth manifolds 

* [[derived smooth manifold]].


#### Derived Deligne-Mumford stacks

+-- {: .num_defn}
###### Definition (derived Deligne-Mumford stack, [[Structured Spaces]], 4.3.19)


Let $k$ be a commutative ring. Recall the pregeometry $\mathcal{T}_{et}(k)$

A **[[derived Deligne-Mumford stack]]** over $k$ is a $\mathcal{T}_{et}(k)$-scheme.


=--

#### Derived schemes with $E_\infty$-ring valued structure sheaves 

The above [[derived scheme]]s have structure sheaves with values in [[simplicial object|simplicial]] commutative rings. There is also a notion of derived scheme whose structure sheaf takes values in [[E-infinity ring]]s. The theory of these is to be described in full detail in 

* [[Jacob Lurie]], _[[Spectral Schemes]]_ .

An indication of some details is in 

* [[Paul Goerss]], _[[Topological Algebraic Geometry - A Workshop]]_

See at _[[E-∞ scheme]]_ and _[[E-∞ geometry]]_.



## Related concepts

* [[geometry (for structured (∞,1)-toposes)]]

* [[structured (∞,1)-topos]]

* **locally representable structured (∞,1)-topos**

## References 

Generalized schemes are definition 2.3.9 of

* [[Jacob Lurie]], _[[Structured Spaces|Derived Algebraic Geometry V - Structured Spaces]]_

The definition of affine $\mathcal{G}$-schemes (absolute spectra) is in section 2.2.

[[!redirects locally representable structured (∞,1)-topos]]

[[!redirects locally representable structured (∞,1)-toposes]]
[[!redirects locally representable structured (infinity,1)-toposes]]

