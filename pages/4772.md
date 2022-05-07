
> This entry is about _conjugation_ in the sense of adjoint actions, as in forming [[conjugacy classes]]. For conjugation in the sense of [[anti-involutions]] on [[star algebras]] see at _[[complex conjugation]]_.

***



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _adjoint action_ is an [[action]] by _conjugation_ .

## Definition

### Of a group on itself

The _adjoint action_ of a [[group]] $G$ on itself is the [[action]] $Ad : G \times G \to G$ given by

$$
  Ad : (g,h) \mapsto g^{-1} \cdot h \cdot g
  \,.
$$

### Of a Lie group on its Lie algebra

The adjoint action $ad : G \times \mathfrak{g} \to \mathfrak{g}$ of a [[Lie group]] $G$ on its [[Lie algebra]] $\mathfrak{g}$ is for each $g \in G$ the [[derivative]] $d Ad(g) : T_e G \to T_e G$ of this action in the second argument at the neutral element of $G$

$$
  ad : (g,x) \mapsto Ad(g)_*(x)
  \,.
$$

This is often written as $ad(g)(x) = g^{-1} x g$ even though for a general Lie group the expression on the right is not the product of three factors in any way.  But for a [[matrix Lie group]] $G$ it is: in this case both $g$ as well as $x$ are canonically identified with [[matrices]] and the expression on the right is the product of these matrices.

Since this is a linear action, it is called the _[[adjoint representation]]_ of a Lie group. The [[associated bundles]] with respect to this representation are called [[adjoint bundles]].

### Of a Lie algebra on itself

Differentiating the above example also in the second argument, yields the adjoint action of a Lie algebra on itself

$$
  ad : \mathfrak{g} \times \mathfrak{g} \to \mathfrak{g}
$$

which is simply the Lie bracket

$$
  ad_x : y \mapsto [x,y]
  \,.
$$


### Of a Hopf algebra on itself

Let $k$ be a commutative unital ring and $H = (H,m,\eta,\Delta,\epsilon, S)$ be a [[Hopf algebra|Hopf]] $k$-algebra with multiplication $m$, unit map $\eta$, comultiplication $\Delta$, counit $\epsilon$ and the antipode map $S: H\to H^{op}$. We can use [[Sweedler notation]] $\Delta(h) = \sum h_{(1)}\otimes_k h_{(2)}$. The adjoint action of $H$ on $H$ is given by

$$
h\triangleright g = \sum h_{(1)} g S(h_{(2)})
$$

and it makes $H$ not only an $H$-module, but in fact a monoid in the monoidal category of $H$-modules (usually called $H$-[[module algebra]]). 

## Related concepts

* [[coadjoint action]]

* [[adjoint representation]], [[adjoint bundle]]

* [[conjugation action]]

* [[conjugacy class]]

* [[twisted ad-equivariant K-theory]]


## References

* Sigurdur Helgason, _Differential geometry, Lie groups, and symmetric spaces_ 

* [[Eckhard Meinrenken]], _Clifford algebras and Lie theory_, Springer

* [[eom]]: [adjoint representation of a Lie group](http://www.encyclopediaofmath.org/index.php/Adjoint_representation_of_a_Lie_group), [adjoint group](http://www.encyclopediaofmath.org/index.php/Adjoint_group)

[[!redirects adjoint actions]]

[[!redirects conjugation]]
[[!redirects conjugations]]
