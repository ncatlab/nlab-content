<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>


+-- {: .standout}

This is a sub-entry of [[geometric models for elliptic cohomology]] and [[A Survey of Elliptic Cohomology]] 

See there for background and context.

This entry here is about the definition of $(2|1)$-dimensional [[super-cobordism]] categories and $(2|1)$-dimensional [[FQFT]]s given by functors on these.

=--

Let [[SDiff]] be the [[category]] of [[supermanifold]]s.

We will define a [[stack]]/[[fibered category]] on $SDiff$ called $E Bord_{2|1}$ whose morphisms are smooth families of (2|1)-dimensional [[super-cobordism]]s, and a [[stack]]/[[fibered category]] $sTV^{fam}$ of topological super vector bundles.

So recall

* [[supergeometry - contents|supergeometry]].

**question**: What is the right notion of Riemannian or Euclidean structure on [[super-cobordism]]s?

**strategy**: From the [[path integral]] perspective we need some structure on $\Sigma$ such that the "space" of maps $Maps(\Sigma,X)$ naturally carries some measure that allows to perform a [[path integral]].

This perspective suggests certain genralizations of the notion of [[Riemannian manifold]] to [[supermanifold]]s which may be a little different than what one might have thought of naively.

We want to define [[Euclidean supermanifold]]s as a genralization of [[Riemannian manifold]] with _flat_ Riemannian metric.

notice that there is a canonical bijection between

* flat [[Riemannian metric]]s on a $d$-dimensional [[manifold]] $X$

* a maximal [[atlas]] on $X$ consisting of charts such that all transition functions belong the the **Euclidean group** or **Galileo group** 

  $$
    Eucl(\mathbb{R}^d)
    :=
    \mathbb{R}^d \rtimes O(\mathbb{R}^d)
  $$

  (rigid translations and rotations)

In analogy to that we define:

Similarly a **Euclidean structure** on a $(d|\delta)$-dimensional [[supermanifold]] is defined using the Euclidean [[super Lie group]] given by the [[semidirect product]]

$$
  Eucl(\mathbb{R}^{d|\delta})
  :=
  \mathbb{R}^{d|\delta}
  \rtimes
  Spin(\mathbb{R}^d)
$$

where the [[Spin]] group acts on the translations in $\mathbb{R}^{d|\delta}$ in a way to be specified.


first recall the notion of

* [[complex supermanifold]]

**goal** replace $(\mathbb{R}^d, Eucl(\mathbb{R}^d))$ by
$(X,G)$ where $X$ is a suitable [[supermanifold]]
and $G$ a suitable [[super Lie group]].

**Definition** A $(X,G)$-structure on a $(d|\delta)$-dimensional [[supermanifold]] $Y$ consists of

* a maximal [[atlas]] consisting of charts

  $$
    Y \sup_{opn} U_i
    \stackrel{\phi_i}{\to_\simeq}
    V_i \subset_{open} X
  $$

  (where on the left $Y_\red\superset_{open} (U_i)_{red}$) with O_Y|_{(U_i)_{red} = O_{U_i}}

* such that the transition function 

  $$
    X \sup \phi_i(U_i \cap U_j) 
    \stackrel{\phi_j \circ \phi_i^{-1}}{\to}
    \phi_j(U_i \cap U_j)
    \subset X
  $$

  is a restriction of a map

  $$
    X \simeq
    X \times pt
    \stackrel{id \times g}{\to}
    X \times G
    \stackrel{action}{\to}
    X
  $$

**definition** A family of $(X,G)$-(complex-, super-)manifolds is a map

$$
  \array{
    Y \\ \downrrow^p \\ S
  }
$$

together with a maximal atlas of charts

$$
  \array{
     Y \sup_{open} U_i &&\stackrel{\phi_i}{\to_\simeq}&&
      V_i \subset_{open} S \times X
     \\
     & \searrow && \swarrow
     \\
     && S
  }
$$

such that the transition maps

$$
  \array{  
     S \times X \superset \phi_i(U_i \times U_j)
     &&\to&&
     \phi_j(U_i \cap U_j)
     \subset S \times X
     \\
     & \searrow && \swarrow
     \\
     && S
  }
$$

is the restriction of a map of the following form 

for some

$$
  S\times X \stackrel{Id \times g \times id}{\to}
  S \times G \times X
  \stackrel{Id \times action}{\to}
$$

for some

$$
  S \stackrel{g}{\to} G
$$

**example** a family $Y \to S$ of $(mathbb{R}^d, Eucl(\mathbb{R}^d))$-manifolds, for $S$ an ordinary [[manifold]] is a submersion with flat Riemannian metric on the fibers.

**goal** define the [[super Euclidean group]] the data needed to defne that 

1. $V$ a $d$-dimensional inner product space

1. a [[spinor representation]] $\Delta^*$ of $Spin(V)$

1. a $Spin(V)$-equivariant map

   $$
      \Gamma : \Delta^* \otimes_{\mathbb{C}}
       \Delta^* \to V \otimes_{\mathbb{R}} \mathbb{C}
   $$

recall some basics of [[Clifford algebra]] $Cl(V)$ for a real [[inner product space]] $V$ of dimension $d$

$$
  \array{
     Spin(V) &\subset& Cl(V)^{ev}
     \\
     \downarrow^{double cover}
     \\
     SO(V)
  }
$$

where the [[Clifford algebra]] is

$$
  Cl(V) := T(V) / (v \cdot v + |v|^2 \cdots Id)
$$

where $T(V)$ is the [[tensor algebra]]

$$
  T(V) = \mathbb{R} \oplus V \oplus (V \otimes V)
     \oplus (V \otimes V \otimes V) \oplus \cdots
$$

so $dim(Cl(V)) = 2^d$

it is naturally a [[super algebra]]

$$
  Cl(V) = Cl(V)^{ev} \oplus Cl(V)^{odd}
$$

the [[Spin group]] is the intersection of the [[Pin group]]

the [[Pin group]] $Pin(V) \subset Cl(V)^\timews$ is the group generated by the elements in the [[group of units]] in $Cl(V)$ that have unit norm, $|v| = 1$

and thenn the Spin group is

$$
  \array{
    Spin(V) := & Pin(V) \cap Cl(V)^{ev} &\to&
      Pin(V)
    \\
    \downarrow^{double cov.} && \downarrow^{double cov.}
    \\
    SO(V) &\hookrightarrow& O(V)
  }
$$ 

**examples**

$$
  \array{
    d & Cl(V)^{ev} & Spin(V)
    \\
    \\
    0 & \mathbb{R} & \{\pm 1\}
    \\
    1 & \mathbb{R} & \{\pm 1\}
    \\
    2 & \{a \cdot 1 + b e_1 e_2\}
        \simeq \mathbb{C}
     & S^1 = U(1)
   }
$$

where $\{e_1, e_2\}$ is the canonical basis of $\mathbb{R}^2 \simeq V$

Construction of $Eucl(\mathbb{R}^{d|\delta})$ for 

* $d = dim_{\mathbb{R}} V$

**remark** $\delta$ is a multiple of $2^{[\frac{d-1}{2}]}$

set

$$
  X = \Pi
  \left(
    \array{ V \times \Delta^* \\ \downarrow \\ V}
  \right)
  = 
  V \times \Pi \Delta^*
$$

is a [[complex supermanifold]] of dimension $(d|\delta)$

$$
  C^\infty(V \times \Pi \Delta^*)
  =
  C^\infty(V) \otimes 
  \wedge^\bullet \Delta
  = 
  C^\infty(V, \wedge^\bullet(\Delta))
$$

for $\delta = 1$ this is

$$
  \cdots = C^\infty(C, \wedge^\bullet \Delta)^{ev}
    \oplus
   C^\infty(C, \wedge^\bullet \Delta)^{odd}
$$

$$
  \cdots \simeq
    C^\infty(V) \oplus C^\infty(V, \wedge^\bullet \Delta)
$$

where the last factor is $\simeq C^\infty(V; \Delta) \simeq C^\infty(V, S^+)$ where $S^+$ is the [[spinor bundle]]

now define the multiplication 

$$
  (V \times \Pi \Delta^*)
  \times
  (V \times \Pi \Delta^*)
  \stackrel{\mu}{\to}
  (V \times \Pi \Delta^*)  
$$

by sayin what it does on sets of probes by $S$

$$
  (V \times \Pi \Delta^*)(S)
  \times
  (V \times \Pi \Delta^*)(S)
  \stackrel{\mu(S)}{\to}
  (V \times \Pi \Delta^*)(S)
$$

here on the left we have the sets of sections

$$
  C^\infty(S)^{ev} \otimes V
  \times
  C^\infty(S)^{ev} \otimes \Delta^*
$$

so we can map these as

$$
  ((v_1, \theta_1),
   (v_2, \theta_2)
  )
  \mapsto
  (v_1 + v_2 + \Gamma(\theta_1 \otimes \theta_2), 
   \theta_1 + \theta_2)
$$

