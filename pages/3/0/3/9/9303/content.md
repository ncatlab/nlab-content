
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Given a [[stack]] $\mathcal{S}$ over a [[site]] $\mathcal{C}$. One often wants to rigidify (kill off a flat subgroup of the [[inertia orbifold|inertia]]) in order to realize the stack as a [[gerbe]] over an [[algebraic space]].

Alternative idea: 

Given a [[moduli stack]] classifying some kind of structure, one sometimes wants to "remove the automorphisms" inside it such as to be left with just a [[moduli space]]. This is sometimes called "rigidification". The archetypical example is the passage from the the groupoid of [[line bundles]] over a space to its [[decategorification]] given by the (set underlying the) [[Picard group]]. Doing this over all spaces means passing from the stack of line bundles to the _[[Picard scheme]]_. The general process of "rigidification" is supposed to be a mechanism that generalizes this process ([ACV, 5.1.1](#ACV)).

## Definition
 {#Definition}

We first give the simple general definition of rigidification

* [General definition](#GeneralDefinition)

Then we discuss specifically the case for [[algebraic stacks]] where one may add a bunch of technical assumptions

* [Definition for algebraic stacks](#DefinitionForAlgebraicStacks)

### General
 {#GeneralDefinition}

For $\mathbf{H}$ an [[(∞,1)-topos]] and $X \in \mathbf{H}$ any [[object]], write $\mathbf{Aut}(X) \in Grp(\mathbf{H})$ for its internal [[automorphism ∞-group]]. Consider a [[braided ∞-group]] $H \in BrGrp(\mathbf{H})$ and an [[∞-group]] [[homomorphism]]

$$
  \iota
  \;\colon\;
  \mathbf{B}H \to \mathbf{Aut}(X)
$$

of [[∞-groups]]. 
This defines an [[∞-action]] of $\mathbf{B}H$ on $X$, hence a [[fiber sequence]] in $\mathbf{H}$ of the form

$$
  \array{
    X &\to& X//\mathbf{B}H
    \\
    && \downarrow
    \\
    && \mathbf{B}^2 H
  }
  \;\;\;\;
  inside
  \;\;\;\;
  \array{
    X &\to& X//\mathbf{Aut}(X)
    \\
    && \downarrow
    \\
    && \mathbf{B} \mathbf{Aut}(X)
  } 
  \,.
$$

+-- {: .num_defn}
###### Definition

The [[∞-quotient]] $X//\mathbf{B}H$ is what is sometimes called the "rigidification" of $X$, especially if $H$ is maximal such that there is a homomorphism $\mathbf{B}H \to \mathbf{Aut}(X)$.

=--




### For algebraic stacks
 {#DefinitionForAlgebraicStacks}

Let $X$ be a [[scheme]]. Let $\mathcal{S}\to X$ be an [[algebraic stack]] fibered in groupoids over $X$. Let $H$ be a finitely presented, [[separated morphism|separated]], [[group scheme]] over $X$ such that for each $\xi\in\mathcal{S}(T)$ there is an embedding $H(T)\to Aut_T(\xi)$ compatible with pullback.

It follows that $H$ must be [[abelian group|abelian]] (because $H(T)$ lies in the center of $Aut_T(\xi)$). The condition on $H$ is trivially satisfied whenever $\mathcal{S}$ is banded by $H$.

Define the $H$-rigidification of $\mathcal{S}$ to be $\mathcal{S}^H$. ([ACV, def. 5.1.4](#ACV)).

Theorem ([A-C-V, theorem 5.1.5](#ACV)): The space $\mathcal{S}^H$ exists such that there is a [[formally smooth morphism|smooth]] surjective finitely presented morphism of stacks $\mathcal{S}\to \mathcal{S}^H$ satisfying the following:

1. For any $\xi\in \mathcal{S}(T)$ with image $\eta\in \mathcal{S}^H(T)$, we have $H(T)$ lies in the kernel of $Aut_T(\xi)\to Aut_T(\eta)$.
2. The map $\mathcal{S}\to \mathcal{S}^H$ is universal with respect to stack morphisms satisfying (1).
3. If $T$ is the spectrum of an algebraically closed field, then $Aut_T(\eta)=Aut_T(\xi)/H(T)$.
4. A moduli space for $\mathcal{S}$ is also a moduli space for $\mathcal{S}^H$.

and if $\mathcal{S}$ is a [[Deligne-Mumford stack]], then $\mathcal{S}^H$ is also a Deligne-Mumford stack and $\mathcal{S}\to \mathcal{S}^H$ is [[formally etale morphism|etale]].



## Examples
 {#Examples}

We discuss some examples. First, to get rid of all distraction introduced by the dependence on objects of a [[site]] of definition, we consider the special case where the underlying site is the point, hence where stacks are just plain [[groupoids]] -- _geometrically [[discrete groupoids]]_ for emphasis. 

* [For a geometrically discrete groupoid](#ForAGeometricallyDiscreteGroupoid)

Then we discuss aspects of regidification for [[algebraic stacks]]

* [For an algebraic stack](#ForAnAlgebraicStack).

### For a geometrically discrete groupoid
 {#ForAGeometricallyDiscreteGroupoid}

If $\mathbf{H} = $ [[∞Grpd]] and $X \in \infty Grpd$ is a [[1-truncated]] object, hence just a [[groupoid]], then $\mathbf{Aut}(X)$ is its [[automorphism 2-group]]. Its [[objects]] are naturally identified with those [[functors]] $\alpha \colon X \to X$ that are [[equivalence of groupoids|equivalences]], and its [[morphisms]] with the [[natural isomorphisms]] $g \colon \alpha \to \beta$ between these. In particular if $\alpha = \beta = id$ is the identity automorphism, then such a $g$ is a [[function]] which to each [[object]] $\xi \in X$ assigns an [[automorphism]] $g_\xi \colon \xi \to \xi$ in $X$ such that for each [[morphism]] $\phi \colon \xi \to \eta$ in $X$ the naturality square

$$
  \array{
    \xi &\stackrel{\phi}{\to}& \eta
    \\
    \downarrow^{\mathrlap{g_\xi}} && \downarrow^{\mathrlap{g_\eta}}
    \\
    \xi &\stackrel{\phi}{\to}& \eta
  }
  \,.
$$

[[commuting diagram|commutes]].

Now for $H$ an [[abelian group]] there is the [[delooping]] [[groupoid]] $\mathbf{B}H$ which has a single object and $H$ as the group of morphisms from that object to itself. Both $\mathbf{Aut}(X)$ and $\mathbf{B}H$ are [[2-groups]] in this case. A homomorphism of 2-groups

$$
  \iota 
   \;\colon\;
  \mathbf{B}H
  \to 
  \mathbf{Aut}(X)
$$

has to send the essentially unique point of $\mathbf{B}H$ to the [[identity]] [[functor]] $id_X$ and is hence
equivalently a [[function]] that sends each element $g \in G$ to a [[natural isomorphism]] $g \colon id_X \to id_X$, hence a function $g_{(-)}$ that sends each object $\xi \in X$ to a morphism $g_\xi \colon \xi \to \xi$ in $X$, such that the above diagram commutes. Moreover, this being a [[2-group]] [[homomorphism]] means that for $g_1, g_2 \in H$ two elements, they are sent to the composite $(g_2)_\xi\circ (g_1)_\xi$ in $X$.

In other words, we have a [[functor]]

$$
  \rho \colon X \times \mathbf{B}H \to X
  \,,
$$

which takes a pair of objects $(\xi,\ast)$ to $\xi$, takes a pair of morphisms of the form $(id_\xi, \ast \stackrel{g}{\to} \ast)$ to $(\xi \stackrel{g_\xi}{\to} \xi)$ and takes a pair of morphisms of the form $(\xi \stackrel{\phi}{\to} \eta, id_\ast)$ to $(\xi \stackrel{\phi}{\to} \eta)$; and which satisfies the action property, 

$$
  \array{
      X \times \mathbf{B}H \times \mathbf{B}H
      &\stackrel{\rho \times id_{\mathbf{B}H}}{\to}&
      X \times \mathbf{B}H
      \\
      {}^{\mathllap{id_X \times \cdot_{\mathbf{B}H}}}\downarrow &\swArrow& \downarrow^{\rho}
      \\
      X \times \mathbf{B}G &\stackrel{\rho}{\to}& X
  }
  \,.
$$

In fact, with the groupoids explicitly presented the way we have discussed them, the [[natural transformation]] filling this [[diagram]] is the [[identity]] and hence we have exhibited the [[∞-action]] of the [[2-group]] $\mathbf{B}H$ on the groupoid $X$ by an ordinary [[action]]. More precisely, under passing to [[nerves]] of [[groupoids]] we have exhibited it as the [[action]] of a [[simplicial group]] on a [[Kan complex]], which is just a [[simplicial object|simplicial diagram]] of ordinary actions of ordinary groups on plain sets. Since these are [[simplicial skeleton|2-coskeletal]] simplicial sets (being the nerves of just 1-groupoids), it is sufficient to consider them just in degrees 0,1,2. So then we have the following simplicial diagram of ordinary groups acting on ordinary sets

$$
  \left(
    \array{
      X_1 \times_{X_0} X_1
      \\
      \downarrow \downarrow \downarrow
      \\
      X_1
      \\
      \downarrow \downarrow 

      \\
      X_0
    }
  \right)
  \times
  \left(
    \array{
      H \times H
      \\
      \downarrow \downarrow \downarrow
      \\
      H
      \\
      \downarrow \downarrow 
      \\
      \ast
    }
  \right)
  \to
  \left(
    \array{
      X_1 \times_{X_0} X_1
      \\
      \downarrow \downarrow \downarrow
      \\
      X_1
      \\
      \downarrow \downarrow 

      \\
      X_0
    }
  \right)
  \,.
$$

In degree 0 this is the identity map $(\xi,\ast) \mapsto \xi$, in degree 1 it is (with the symbols as above) the map $(\phi,g) \mapsto g_\eta \circ \phi = \phi \circ g_\xi$ and so on.

Finally, the [[∞-quotient]] $X//\mathbf{B}H$ of an [[∞-action]] of an [[∞-group]] presented as an ordinary action of a [[simplicial group]] on a [[Kan complex]] this way is presented by the [[Borel construction]], namely the ordinary [[quotient]] of [[simplicial sets]]

$$
  X \times_{\mathbf{B}H} \mathbf{E}\mathbf{B}H
  \coloneqq
  (X \times \mathbf{E}\mathbf{B}H)/\mathbf{B}H
$$

(where now all symbols stand for the corresponding simplicial sets as described above). Here 

$$
  \mathbf{E} \mathbf{B}H
  \coloneqq
  (\mathbf{B}H)^{\Delta^1} \times_{\mathbf{B}G} *
$$

is a model for the total space of the [[universal principal infinity-bundle|universal principal 2-bundle]] over $\mathbf{B}H$.

So the [[Kan complex]] $X \times_{\mathbf{B}H} \mathbf{E}\mathbf{B}H$ presents the "rigidification" of $X$ with respect to the chosen $\iota \colon \mathbf{B}H \to \mathbf{Aut}(X)$.



### For an algebraic stack
 {#ForAnAlgebraicStack}

The standard example is the $\mathbb{G}_m$-rigidification of the [[Picard scheme|Picard stack]]. Suppose $X/k$ is an irreducible [[variety]] over a [[field]]. One can say that the failure of the Picard stack, $\mathcal{Pic}_X$ to be representable comes from the fact that objects in fiber categories have automorphisms by the multiplicative group, so we would like to kill this group.

As pointed out in _[[Picard scheme]]_, the relative Picard scheme is the [[sheafification]] of $\mathcal{Pic}_X$ and [[representable]]. Moreover $\mathcal{Pic}_X\to Pic_X$ is a $\mathbb{G}_m$-gerbe, so $\mathbb{G}_m$ satisfies the conditions to rigidify. 

By the [[universal property]], the rigidification is exactly $Pic_X$, so in this case we see that the sheafification and the rigidification by the inertia are the same.


## References

* [[Dan Abramovich]], Alessio Corti, and [[Angelo Vistoli]], _Twisted Bundles and Admissible Covers_ ([arXiv:0106211](http://arxiv.org/abs/math/0106211))
 {#ACV}

* Matthieu Romagny, _Group Actions on Stacks and Applications_, Michigan Math. J. Volume 53, Issue 1 (2005), 209-236 ([Project Euclid](http://projecteuclid.org/euclid.mmj/1114021093)).

category: algebraic geometry
[[!redirects rigidification]]