
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### General

In full generality, we have the following definition of _gerbe_ .

+-- {: .num_defn #GeneralDef}
###### Definition

Given an [[(∞,1)-topos]] $\mathcal{X}$, a **gerbe** in $\mathcal{X}$ is an [[object]] $\mathcal{G} \in \mathcal{X}$ that is

1. [[1-truncated]]

1. [[1-connective]] (= [[connected]]).

=--


The first condition says that a gerbe is an object in the [[(2,1)-topos]] $\tau_{\leq 1 } \mathcal{X} \hookrightarrow \mathcal{X}$ inside $\mathcal{X}$. This means that for $C$ any [[(∞,1)-site]] of definition for $\mathcal{X}$, a gerbe is a [[(2,1)-sheaf]] on $C$, $\mathcal{G} \in Sh_{(2,1)}(C)$: a [[stack]] on $C$.

The second condition says that  a gerbe is a stack that _locally_ looks like the [[delooping]] of a [[sheaf]] of [[group]]s. More precisely, it says that 

* the morphism $\mathcal{G} \to *$ to the [[terminal object in an (∞,1)-category|terminal object]] of $\mathcal{X}$ is an [[effective epimorphism in an (∞,1)-category|effective epimorphism)]];

* the 0th [[categorical homotopy groups in an (∞,1)-topos|categorical homotopy]] group $\pi_0 \mathcal{G}$ is isomorphic to the terminal object $*$ as objects in the [[sheaf topos]] $\tau_{\leq 0} \mathcal{X} = Sh_{(1,1)}(C)$. Here $\pi_0 \mathcal{G}$ is the [[sheafification]] of the presheaf of connected components of the groupoids that $\mathcal{G} : C^{op} \to Grpd \hookrightarrow \infty Grpd$ assigns to each object in the site.

Traditionally this is phrased before sheafification as saying that a gerbe is a stack that is _locally_  non-empty and _locally_ connected . This is the traditional definition, due to [Giraud](#Giraud).

Also traditionally gerbes are considered in the [[little topos|little (2,1)-toposes]] $\tau_{\leq 1} \mathcal{X}$ of a [[topological manifold]] or [[smooth manifold]] $X$ or a [[topological stack]] or [[differentiable stack]] $X$. One then speaks of a _gerbe over $X$_ .

More precisely, we may associate to any $X \in C :=$ [[Top]] or $X \in C :=$ [[Diff]] the corresponding [[big site]] $C/X$ and form the [[(2,1)-topos]] $\tau_{leq} \mathcal{X} := Sh_{(2,1)}(C/X)$. In terms of this a gerbe is given by a collection of groupoids assigned to patches of $X$, satisfying certain conditions.

Equivalent to this is the [[over-(∞,1)-topos|over-(2,1)-topos]] $\tau_{\leq 1} \mathcal{H}/j(X)$, where $\tau_{\leq 1}\mathcal{H} := Sh_{(2,1)}(C)$ is the [[big topos|big]] [[(2,1)-topos]] over $C$ (and $j$ denotes its [[(∞,1)-Yoneda embedding|(2,1)-Yoneda embedding]]).

Since this $\mathcal{H}$ is a [[cohesive (∞,1)-topos]] we may think of its objects a general [[topological ∞-groupoid|continuous ∞-groupoid]]s or [[∞-Lie groupoid|smooth ∞-groupoid]]s. In large parts of the literature coming after [Giraud](#Giraud) gerbes, or related structures equivalent to them, are described this way in terms of [[topological groupoid]]s and [[Lie groupoid]]s. This perspective is associated with the notion of a _[[bundle gerbe]]_ .


### $G$-Gerbes

We discuss gerbes that have a "strucure group" $G$ akin to a [[principal bundle]]. Indeed, while not the same concept, these _$G$-gerbes_ are [[equivalence in an (∞,1)-category|equivalent]] to $AUT(G)$-[[principal 2-bundle]]s, for $AUT(G)$ the [[automorphism 2-group]] of $G$.


+-- {: .num_remark #RelationToEMObjects}
###### Remark


The definition \ref{GeneralDef} of _gerbe_ is almost verbatim that of _[[Eilenberg-MacLane object]]_ in degree 1. The only difference is that the latter is required to have not only the homotopy sheaf $\pi_0 = *$, but even have a "global section" in the form of a morphism $* \to P$.

First consider this locally. A gerbe (as any [[1-connected]] object) necessarily has _local_ sections:

for 

$$
  (x^* \dashv x_*) :  \infty Grpd
   \stackrel{\overset{x^*}{\leftarrow}}{\underset{x_*}{\to}}
  \mathcal{X}
$$

any [[point of a topos|topos point]], the [[stalk]] functor $x^*$, being an [[inverse image]] is [[left exact functor|left exact]] and hence preserves [[categorical homotopy groups in an (∞,1)-topos|homotopy sheaves]] and [[terminal object]]s. It follows that the 0th homotopy sheaf is trivial

$$
  \pi_1 x^* P \simeq x^* \pi_1(P) \simeq x^* * \simeq *
$$

as are all the degree-$p$ homotopy sheaves for $p \gt 1$. Therefore $x^* P$ is a [[groupoid]] with a single object: the [[delooping]] groupoid of a [[group]] $G_x$:

$$
  x^* P \simeq B G_x
  \,.
$$

More generally, by the discussion at [[looping and delooping]] we have in an [[equivalence of (∞,1)-categories]]

$$
  (\Omega \dashv \mathbf{B})
  :
  \infty Gpr(\mathcal{X})
   \stackrel{\overset{\Omega}{\leftarrow}}{\underset{\mathbf{B}}{\to}}
  \mathcal{X}_{pt, \geq 1}
$$

between the [[∞-group]] objects in the ambient [[(∞,1)-topos]] $\mathcal{X}$ and the [[pointed object|pointed]] [[connected]] objects.

It follows that for a gerbe $P$ that admits a global section $* \to P$ the above relation holds not only [[stalk]]-wise, but globally: it is the [[delooping]] of its own first [[categorical homotopy groups in an (∞,1)-topos|sheaf of homotopy groups]]

$$
  P \simeq \mathbf{B} \pi_1(P)
  \,.
$$

=--

The following definition characterizes gerbes that are _locally_ of the form of remark \ref{RelationToEMObjects}.

+-- {: .num_defn #GGerbe}
###### Definition

Let $G \in Grp(\mathcal{X})$ be a group object. A gerbe $P \in \mathcal{X}$ is a **$G$-gerbe** if there exists an [[effective epimorphism]] $U \to *$ and an [[equivalence in an (∞,1)-category|equivalence]]

$$
  P|_U \simeq \mathbf{B}(G|_U)
  \,,
$$ 


where $P|_U := P \times U$ and $G|_U := G \times U$.

=--

+-- {: .num_remark }
###### Remark

In a typical application one considers gerbes over some [[topological space]] $X$. In that case 

* $\mathcal{X} = Sh_{(\infty,1)}(Op(X))$ is the [[(∞,1)-category of (∞,1)-sheaves]] on the [[category of open subsets]] of $X$;

* the [[terminal object]] of $\mathcal{X}$ _is_ the space $X$, regarded as an object in its own $(\infty,1)$-topos, hence we can write $X := * \in \mathcal{X}$;

* a [[group object]] $G \in \mathcal{X}$ is [[sheaf]] of [[group]]s on $X$;

* an [[effective epimorphism]] $U \to *$, hence $U \to *$ is obtained from any [[open cover]] $\{U_i \to X\}$ by setting $U := \coprod_i U_i$; 

* with such a choice of effective epimorphism, $G|_U = \coprod_i G|_{U_i}$ is simply the restriction of the sheaf of groups $G$ to each [[open subset]] that is a member of the cover;

* $\mathbf{B}G_{U} \in \mathcal{X}/U$ is the [[stack]] of $G_{U}$-[[principal bundle]]s on $U$. 

=--

## Properties

### Equivalence of $G$-gerbes to $AUT(G)$-2-bundles

Let $\mathcal{X}$ be any ambient [[(∞,1)-topos]].

Let $G \in Grp(\mathcal{X}) \subset \infty Grpd(\mathcal{X})$ be a [[group object]] (a [[0-truncated]] [[∞-group]]).

Write

$$
  G Gerbe \subset \mathcal{X}
$$

for the [[core]] of the full [[sub-(∞,1)-category]] on $G$-gerbes in $\mathcal{X}$.

Write 

$$
  AUT(G) := 
  Aut_{\mathcal{X}_{*}}(\mathbf{B}G) 
  \in 
  2 Grp(\mathcal{X}) \subset \infty Grp(\mathcal{X})
$$

for the [[2-group]] object called the [[automorphism 2-group]] of $G$.

+-- {: .num_prop #ClassificationOfGGerbes}
###### Proposition

$G$-gerbes in $\mathcal{X}$ are classified by first $AUT(G)$-[[nonabelian cohomology]]

$$
  \pi_0 G Gerbe \simeq \pi_0 \mathcal{X}(*, \mathbf{B} AUT(G))
   =:
   H_{\mathcal{X}}^1(X,AUT(G))
  \,.
$$

=--

In the general perspective of [[(∞,1)-topos theory]] this appears as  ([JardineLuo, theorem 23](#JardineLuo)). 


+-- {: .num_cor}
###### Corollary

Since [[nonabelian cohomology]] with coefficients in $AUT(G)$ also classified $AUT(G)$-[[principal 2-bundles]] it follows that also

$$
  \pi_0 G Gerbe \simeq AUT(G) 2Bund(*)
  \,.
$$

Notice that under this equivalence a $G$-gerbe is not identified with the total space object of the corresponding $AUT(G)$-[[principal 2-bundle]]. The latter differs by an $Aut(H)$-factor. Where a $G$-gerbe is locally equivalent to 

$$
  \mathbf{B}(G|_U)
  = 
  G|_U \stackrel{\to}{\to} *|_U
$$

an $AUT(G)$-principal 2-bundle is locally equivalent to

$$
  AUT(G|_U)
  = 
  Aut(G|_U) \times G
   \stackrel{\overset{Ad(p_2) \cdot p_1}{\to}}{\underset{p_1}{\to}}
  Aut(G|_U) 
  \,.
$$

Instead, under the above equivalence a gerbe is identified with the [[associated ∞-bundle]] with fibers $\mathbf{B}G$ 
that is associated via the canonical [[action]] of $AUT(G) = Aut(\mathbf{B}G)$ on $\mathbf{B}G$.

=--


### Banded gerbes

For $G \in Grp(\mathcal{G})$, the [[automorphism 2-group]] $AUT(G)$ has a canonical morphism to its [[0-truncated|0-truncation]], the ordinary [[outer automorphism]] group object of $G$:

$$
   \to AUT(G) \to \pi_0(Aut(G)) =:  Out(G)
  \,.
$$

Therefore every $AUT(G)$-[[cocycle]] has an underlying $Out(G)$-cocycle (an $Out(G)$-[[principal bundle]]):

$$
  \mathcal{X}(* , \mathbf{B}AUT(G)) 
   \to 
  \mathcal{X}(* , \mathbf{B}Out(G))   
  \,.
$$

By prop. \ref{ClassificationOfGGerbes} this an assignment of $Out(G)$-cohomology classes to $G$-gerbes:

$$
  Band : \pi_0 ( G Gerbe ) \to H_{\mathcal{X}}^1(X,Out(G))
  \,.
$$

For $P \in G Gerbe$ one says that $Band(P)$ is its **band**. 

Sometimes in applications one considers not just the restriction from all gerbes to $G$-gerbes for some $G$, but further to $K$-banded $G$-gerbes for some $K \in H_{\mathcal{X}}^1(X,Out(G))$.

The [[groupoid]] $G Gerbe_K(X)$ of $K$-banded gerbes is the $K$-[[twisted cohomology|twisted]] $\mathbf{B}^2 Z(G)$-cohomology of $X$ (where $Z(G)$ is the [[center]] of $G$): it is the [[homotopy pullback]]

$$
  \array{
    G Gerbe_K(X) &\to& {*}
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{K}}
    \\ 
    \mathcal{X}(X,\mathbf{B}AUT(G))
    &\to&
    \mathcal{X}(X, \mathbf{B}Out(G))
  }
 \,.
$$

## Sub-entries

More details on gerbes is at the following sub-entries:

* [[gerbe (as a stack)]]

* [[gerbe (in nonabelian cohomology)]]

* [[gerbe (in differential geometry)]]

* [[bundle gerbe]]

* [[gerbe (general idea)]]

## Examples

* [[determinantal gerbe]]

## Related concepts

* [[principal bundle]] / [[torsor]] / [[associated bundle]]

* [[principal 2-bundle]] / **gerbe** / [[bundle gerbe]]

* [[principal 3-bundle]] / [[2-gerbe]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]]  / [[∞-gerbe]]


## References

The definition of _gerbe_ goes back to (see also [[nonabelian cohomology]])

* [[J. Giraud]], _Cohomologie non ab&#233;lienne_ , Springer  (1971)

Introductions include

* [[Lawrence Breen]], _Notes on 1- and 2-gerbes_ in [[John Baez]], [[Peter May]] (eds.) _[[Towards Higher Categories]]_ ([arXiv:math/0611317](http://arxiv.org/abs/math/0611317)).
  {#Breen}

* [[Ieke Moerdijk]], _Introduction to the language of stacks and gerbes_ ([arXiv:math/0212266](http://arxiv.org/abs/math/0212266))

* [[Lawrence Breen]], _Notes on 1- and 2-gerbes_ in [[John Baez]], [[Peter May]] (eds.) _[[Towards Higher Categories]]_ ([arXiv:math/0611317](http://arxiv.org/abs/math/0611317)).
  {#Breen}

A discussion from the point of view of [[(∞,1)-topos theory]] is in 

* [[Rick Jardine]], Z. Luo, _Higher order principal bundles_ , K-theory (2004) ([web](http://www.math.uiuc.edu/K-theory/0681/))
 {#JardineLuo}

The definition for $n$-gerbes as $n$-truncated and $n$-connected objects (see [[∞-gerbe]]) is in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects gerbes]]
[[!redirects gerb]]
