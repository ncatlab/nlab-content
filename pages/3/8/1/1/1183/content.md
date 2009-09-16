<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


#Idea#

A _$\sigma$-model_ is a [[quantum field theory]]  which is induced from a _target space_ that carries some geometric structure, usually that of an [[schreiber:Differential Nonabelian Cohomology|n-bundle with connection]] representing a gauge background field.

The _fields_ of a $\sigma$-model on parameter space $\Sigma$ are maps from $\Sigma$ to target space $X$.

One way to make this precise for _topological_ $\sigma$-models is to say that target space $X$, or possibly the gauge bundle $P \to X$ over it, [[representable functor|represents]] an functor that sends [[cobordism]] [[cospan]]s to [[span]]s which in turn are taken to act by pull-push on the quantum states, which are objects in [[geometric infinity-function theory]] living over the mapping spaces $[\Sigma, P]$.

## Physical interpretation ##

$\sigma$-model quantum field theories on parameter spaces $\Sigma$ of top dimension $n+1$ are to be thought of as encoding the quantum mechanics of the propagation of an $n$-dimensional particle, called an _$n$-brane_, in target space $X$, subject to the forces imposed on it by the backgreound field, under which it is said to be charged.


These cases describe non-topological quantum field theories. Here the formalization of the notion of $\sigma$-model is not entirely complete. Yet 

#Examples#

## Non-topological $\sigma$-models ##

* The canonical textbook example of a quantum mechanical system is of this form for $n=1$: A line [[vector bundle|bundle]] with [[connection on a bundle|connection]] $E \to X$ on a [[Riemannian manifold]] $X$ induces the 1-dimensional [[quantum field theory]] which is the quantum mechanics of a point particle which propagates on $X$, subject to the forces of gravitation (given by the metric on $X$) and [[electromagnetism]] (given by the line bundle with connection). The Hamilton operator encoding this quantum dynamics in this case is the Laplace-operator of $T X$ twisted by the line bundle $E$.

* Generalizing in the above example the line bundle $E$ by an abelian [[bundle gerbe]] with a connection yields a background for a 2-dimensional $\sigma$-model which mayb be thought of as describing the propgation of a [[string theory|string]].  The best-studied version of this is the case where $X = G$ is a [[Lie group]], in which case this $\sigma$-model is known as the _Wess--Zumino--Witten model_.



## Topological $\sigma$-models ##

* [[Dijkgraaf-Witten theory]] is the (2+1)-dimensioanl $\sigma$-model induced from an abelian 2-gerbe on $\mathbf{B} G$, for $G$ a finite group.

* [[Chern-Simons theory]] is supposed to be analogously the $\sigma$-model induced from an abelian 2-gerbe with connection on $\mathbf{B}G$, but now for $G$ a Lie group.

* Rozansky--Witten theory is essentially the $\sigma$-model for $X$ a smooth projective variety.




# References #

First indications on how to formalize $\sigma$-models in a [[higher category theory|higher categorical]] context were given in

* Dan Freed, _Higher algebraic structures and quantization_ ([arXiv](http://arxiv.org/abs/hep-th/9212115))

A more complete formalization along the lines of the above operation was indicated in

* Marco Grandis, [[Cospans in Algebraic Topology]]

and

* David Ben-Zvi, John Francis, David Nadler, _Integral transforms and Drinfeld centers in derived geometry_ ([arXiv](http://arxiv.org/abs/0805.0157)) .

More discussion of the latter is at [[geometric infinity-function theory]].

[[!redirects sigma-models]]
[[!redirects sigma model]]
[[!redirects ∞-model]]
[[!redirects ∞-models]]