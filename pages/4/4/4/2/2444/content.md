

#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

There are two different things that one might mean by a "complex supermanifold", and the term is in fact used for two different notions in the literature:

1. In the first sense, a complex supermanifold is a [[supermanifold]] that is related to complex [[vector bundle]]s as ordinary supermanifolds are related to real [[vector bundle]]s.
 

1. In the second sense, a complex supermanifold is a super(complex manifold), a super-version of [[complex manifold]].

# complex {super manifold} #


>**raw material** will be polished

**example**

Lez $E \to X$ be a complex [[vector bundle]] of rank $\delta$

This gives rise to the [[complex supermanifold]] $\Pi E$

A **complex supermanifold** is a [[ringed space]] $X = (|X|, O_X)$ such that

* the [[structure sheaf]] $O_X$ a [[sheaf]] of commutative complex [[super algebra]]s

*  locally $O_X$ is [[isomorphism|isomorphic]] to $
  C^\infty(\mathbb{R}^d) \otimes_{\mathbb{C}} \wedge^\bullet \mathbb{C}^\delta
$


**Remark** $C^\infty(X) := O_X(X)$ does not in general have a $\mathbb{C}$-antilinear involution  $\bar{-} : C^\infty(X) \to C^\infty(X)$ but there does exist a canonical complex conjugation on the quotient $C^\infty(X)$ by the ideal of nilpotent sections, which is $C^\infty(X_{red}; \mathbb{C})$.

So on a complex supermanifold we have complex conjugation only on the reduced manifold.

Write [[cSDiff]] for the [[category]] of complex supermanifolds

as for ordinary [[supermanifold]]s we want to have the statement

$$
  cSDiff(X,Y) \simeq
  ComplexSuperAlg(C^\infty(Y), C^\infty(X))
$$

but this requires saying precisely what we mean by an algebra homomorphism of the algebras of global sections $C^\infty(X)$ of a [[complex supermanifold]]. 

So define this to be a morphism that so we require that

$$
  \phi : C^\infty(Y) \to C^\infty(X)
$$

such that $\phi_{red}(\bar f_{red}) = \bar{\phi_{red}(f_{red})}$

now we define the complex supermanifold $\mathbb{R}_{cs}^{d|\delta}$ by setting for $S$ an arbitrary complex supermanifold we 

$$
  \mathbb{R}_{cs}^{d|\delta}(S)
  =
   cSDiff(S, \mathbb{R}_{cs}^{d|\delta})
  :=
  \{
    (x_1, \cdots, x_d, \theta_1, \cdots, \theta_{\delta})|
    x_i \in C^\infty(S)^{ev} , 
    \theta_j \in C^\infty(S)^{odd};
    with x_i real in that \bar (x_i)_{red} = (x_i)_{red};
  \}
$$


**example** 

for

$$
  \mathbb{R}^{2|1}(S)
  =
  \{
    (x,y,\theta) |
    x,y \in C^\infty(S)^{ev}, 
    \theta \in C^\infty(S)^{odd}; x,y real
  \}
$$

we shall write

$$
  \simeq \{
     (z,\bar z, \theta)
     | z, \bar z \in C^\infty(S)^{ev}
  \}
$$

**Remark** For $X$ a complex supermanifold $X_{red}$ is **not** a [[complex manifold]] but just a [[manifold]] regarded as a [[ringed space]] with [[structure sheaf]] taken to be the sheaf of $\mathbb{C}$-valued smooth functions on the ordinary real manifold.

So the notion of complex here is such that it generalizes the relation

$$
  \Pi : \{real vector bundles\} \to Supermanifolds
$$

to 

$$
  \Pi : \{complex vector bundles\} \to cSupermanifold
$$


Notice that in parts of the literature the term "complex supermanifold" is used differently, as a super-generalization of [[complex manifold]]. The terminology is a mess -- but its not our fault!





#super {complex manifold}#


...