
#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

Twisted K-theory is a [[twisted cohomology]] version of [[K-theory]], where the twist is given by a cocycle in degree 3 [[Eilenberg-MacLane spectrum|ordinary cohomology]].

## Definition ##

Let $Vectr$ be the stack of [[vectorial bundle]]s. (If we just take [[vector bundle]]s we get a notion of twisted K-theory that only allows twists that are finite order elements in their [[cohomology group]]).

There is a canonical morphism

$$
  \rho : \mathbf{B} U(1) \to Vect \hookrightarrow Vectr
$$

coming from the standard [[representation]] of the [[group]] $U(1)$.

Let $\mathbf{B}_{\otimes} Vectr$ be the [[delooping]] of $Vectr$ with respect to the [[tensor product]] [[monoidal category|monoidal structure]] (not the additive structure).

Then we have a [[fibration sequence]]

$$
  Vectr \to {*} \to \mathbf{B}_\otimes Vectr
$$

of [[(infinity,1)-category|(infinity,1)-categories]] (instead of [[infinity-groupoid]]s).

The entire morphism above deloops

$$
  \mathbf{B}\rho : \mathbf{B}^2 U(1) \to \mathbf{B}_\otimes Vect \hookrightarrow \mathbf{B}_{\otimes} Vectr
$$

being the standard representation of the [[2-group]] $\mathbf{B}U(1)$.

From the general nonsense of [[twisted cohomology]] this induces canonically now for every $\mathbf{B}^2 U(1)$-[[cohomology|cocycle]] $c$ (for instance given by a [[bundle gerbe]]) a notion of $c$-twisted $Vectr$-cohomology:

$$
 \array{
   \mathbf{H}^c(X, Vectr)
   &\to&
   {*}
   \\
   \downarrow
   &&
   \downarrow^{\mathbf{B}\rho \circ c}
   \\
   {*} &\to& \mathbf{H}(X,\mathbf{B}_\otimes Vectr)
 }
  \,.
$$

After unwrapping what this means, the result of

* Kiyonori Gomi, _Twisted K-theory and finite-dimensional approximation_ ([arXiv](http://arxiv.org/abs/0803.2327))

shows that [[concordance]] classes in $\mathbf{H}^c(X,Vectr)$ yield twisted K-theory.

+-- {: .standout}

This entry contains research ideas. 

=--

## References ##

The basic idea underlying this description of twisted bundles as homotopies from the gerbe to the trivial gerbe but inside a category of "2-vector bundles" was (apparently first?) presented around secton 3.2 of

* Urs Schreiber, _Sections of 2-vector bundles_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/atd.pdf))

A more refined description  of this is in section 4.4.3 _Twisted vector bundles_ of

* U. Schreiber, [[Konrad Waldorf]], _Connections on non-abelian Gerbes and their Holonomy_ ([arXiv](http://arxiv.org/abs/0808.1923))

The above formulation of the relevant homotopies evolved from the joint work mentioned at [[twisted cohomology]] and in particular from interaction with [[Thomas Nikolaus]].