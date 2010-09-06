
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _Lie algebra_ is the [[infinitesimal object|infinitesimal]] approximation to a [[Lie group]]. 

## Definition

### Ordinary definition

A _Lie algebra_ is a [[vector space]] $\mathfrak{g}$ equuipped with a bilinear skew-symmetric map $[-,-]  _\mathfrak{g} \vee \mathfrak{g} \to \mathfrak{g}$ which satisfies the [[Jacobi identity]]:

$$
  \forall x,y,z \in \mathfrak{g} : [x,[y,z]] + [z,[x,y]] + [y,[z,x]] = 0
  \,.
$$

A [[homomorphism]] of Lie algebras is a linear map $\phi : \mathfrak{g} \to \mathfrak{h}$ such that for all $x,y \in \mathfrak{g}$ we have

$$
  \phi([x,y]_{\mathfrak{g}}) = [\phi(x),\phi(y)]_{\mathfrak{h}}
  \,.
$$

This defines the [[category]] [[LieAlg]] of Lie algebras.

### In a general linear category

The notion of _Lie algebra_ may be formulated [[internalization|internal to]] any [[linear category]]. This general definition subsumes as special case generalizations such as [[super Lie algebra]]s. 

Given a [[commutative unital ring]] $k$, and a (strict for simplicity) [[symmetric monoidal category|symmetric monoidal]] $k$-[[linear category]] $(C,\otimes,1)$ with the symmetry $\tau$, a **Lie algebra** in $(C,\otimes,1,\tau)$ is an object $L$ in $C$ together with a morphism $[,]: A\otimes A\to A$ such that the [[Jacobi identity]] 

$$[,[,]]+[,[,]]\circ(id_L\otimes\tau_{L,L})\circ(\tau\otimes id_L)+[,[,]]\circ (\tau_{L,L}\otimes id_L)\circ (id_L\otimes\tau_{L,L}) = 0$$ 

and antisymmetry 

$$[,]+[,]\otimes\tau_{L,L} = 0$$

hold. If $k$ is the ring $\mathbb{Z}$ of [[integer]]s, then we say (internal) __Lie ring__, and if $k$ is a [[field]] and $C=Vec$ then we say a __Lie $k$-algebra__. Other interesting cases are super-Lie algebras, which are the Lie algebras in the symmetric monoidal category $\mathbb{Z}_2-Vec$ of [[supervector space]]s and the Lie algebras in the [[Loday-Pirashvili tensor category]] of linear maps. 

Alternatively, Lie algebras are the algebras over certain quadratic [[operad]], called the [[Lie operad]], which is the [[Koszul dual]] of the [[commutative algebra]] operad.  

## Cohomology

See [[Lie algebra cohomology]].

## Lie integration

See

* [[Lie integration]];

* [[Lie theory]].

## Special properties

* [[abelian Lie algebra]]

* [[simple Lie algebra]]

* [[semisimple Lie algebra]]

## Higher Lie algebras

The notion of  _Lie algebra_ is a special case that of [[∞-Lie algebra]] and more generally that of [[∞-Lie algebroid]]. See there for more details.



[[!redirects Lie algebras]]