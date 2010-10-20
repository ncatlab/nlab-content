
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[quantum mechanics]], the _Kochen-Specker theorem_ -- developed in 1967 by [[Simon Kochen]] and [[Ernst Specker]] -- is a no-go theorem that places limits on the types of [[hidden variable theories]] that may be used to explain the apparent randomness of quantum mechanics in a causal way.  It roughly asserts that it is impossible to assign values to all physical quantities while simultaneously preserving the functional relations between them.  It is a complement to [[Bell's theorem]], developed by [[John Bell]] in 1964, and is related to [[Gleason's theorem]], developed in 1957 by [[Andrew Gleason]] (who incidentally is the person who communicated the original Kochen-Specker paper to the _Journal of Mathematics and Mechanics_ ).  [[Christopher Isham]] has recently shown that the Kochen-Specker theorem is equivalent to the statement that the spectral [[presheaf]] has no global elements.

## Kochen-Specker theorem

+-- {: .un_defn}
###### Definition

Let $B(\mathcal{H})$ be the algebra of [[bounded operator]]s on some [[Hilbert space]] $\mathcal{H}$. (In physics $\mathcal{H}$ is the space of states of a [[quantum mechanics|quantum mechanical]] system, and the elements $\hat A \in B(\mathcal{H})$ represent quantum observables.) 

A **valuation** on $B(\mathcal{H})$ is a [[function]] 

$$
  \lambda : B(\mathcal{H}) \to \mathbb{R}
$$ 

to the [[real number]]s, satisfying two conditions:


1. _value rule_ -- the value $\lambda(\hat{A})$ belongs to the spectrum of $\hat{A}$;

2. _functional composition principle_ (FUNC) -- for any pair of self-adjoint operators $\hat{A}$, $\hat{B}$ such that $\hat{B}=h(\hat{A})$ for some real-valued function $h$ we have $\lambda(\hat{B})=h(\lambda(\hat{A}))$.

=--


Note that is $\hat{A}_{1}$ and $\hat{A}_{2}$ commute, it follows from the spectral theorem that there exists an operator $\hat{C}$ and functions $h_{1}$ and $h_{2}$ such that $\hat{A}_{1}=h_{1}(\hat{C})$ and $\hat{A}_{2}=h_{2}(\hat{C})$.  It follows from FUNC that

$$
  \lambda(\hat{A}_{1} + \hat{A}_{2}) = \lambda(\hat{A}_{1}) + \lambda(\hat{A}_{2})
$$

and

$$
  \lambda(\hat{A}_{1}\hat{A}_{2})=\lambda(\hat{A}_{1})\lambda(\hat{A}_{2}).
$$

Now we have:

+-- {: .un_theorem}
###### Theorem 
**(Kochen-Specker)**

No valuations on $B(\mathcal{H})$ exist if dim($\mathcal{H}$)>2.

=--

### Consequences

If a valuation _did_ exist and was restricted to a commutative sub-algebra of operators, it would be an element of the [[spectrum]] of the algebra.  Since such elements _do_ exist, valuations must exist on any commutative sub-algebra of operators but not on the _non_-commutative algebra, $\mathcal{B}(\mathcal{H})$, of all bounded operators.  Isham calls these valuations _local_.

## Sheaf-theoretic interpretation

[[Chris Isham]] and [[Jeremy Butterfield]] gave a [[topos theory|topos theoretic]] reformulation of the Kochen-Specker theorem as follows.

+-- {: .un_defn}
###### Definition
**(category of contexts)**

Let $\mathcal{V}(\mathcal{H})$ be the [[category]] (a [[poset]]) whose

* [[object]]s are _commutative_ [[von Neumann algebra|von Neumann subalgebras]] $V \subset B(\mathcal{H})$;

* [[morphism]]s $V_1 \to V_2$ are inclusions $V_1 \subset V_2$.

=--

Isham calls this the **category of contexts** of $B(\mathcal{H})$.
Each commutative algebra is viewed as a context within which to view a quantum system in an essentially classical way in the sense that the physical quantities in any such algebra can be given consistent values (as they can in a classical context).

+-- {: .un_defn}
###### Definition
**(spectral presheaf)**

Let $\Sigma : \mathcal{V}(\mathcal{B})^{op} \to Set$ be the [[presheaf]] on the category of context such that

* to $V \subset B(\mathcal{H})$ it assigned the set underlying the 
  spectrum of $V$: the set of multiplicative linear [[functional]]s 
  $\kappa : V \to \mathbb{R}$;

* to an inclusion $i : V_1 \hookrightarrow V_2$ it assigns the corresponding 
  function $i^* : \Sigma(V_2) \to \Sigma(V_1)$ that sends a functional
  $V_2 \stackrel{\kappa}{\to} \mathbb{R}$ to its restriction
  $V_1 \hookrightarrow V_2 \stackrel{\kappa}{\to} \mathbb{R}$.


=--


Recall that the [[terminal object]], $* = 1_{Set^{\mathcal{V}(\mathcal{H})^{op}}}$ in the [[category of presheaves]] on $\mathcal{V}(\mathcal{H})$ is the [[presheaf]] that assigns the singleton set $*$ (the [[terminal object]] in [[Set]]) to each commutative algebra.  

A [[global element]] of the spectral presheaf $\Sigma$ is a morphism $e : * \to \Sigma$ in the presheaf topos. Being a [[natural transformation]] of functors, such a global element $\lambda : 1_{Set^{\mathcal{V}(\mathcal{H})^{op}}} \to \underline{\Sigma}$ of the spectral presheaf, $\underline{\Sigma}$ would associate an element of the spectrum of an algebra $V$ to that algebra such that all local valuations are global, i.e. for $V \subseteq W$ valuations on $V$ are local valuations on $W$ but global on $V$.  

Because notice that a multiplicative linear functional $\kappa : V \to\mathbb{R}$ ssatisfies the axioms of a valuation when restricted to the self-adjoint elements of $V$.

By the Kochen-Specker theorem these cannot exist, hence a global element of $\Sigma$ cannot exist.

+-- {: .un_lemma}
###### Observation
(Hamilton, Isham, Butterfield)

The Kochen-Specker theorem is equivalent to the statement that in the presheaf [[topos]] $[\mathcal{V}(\mathcal{H})^{op}, Set]$ the spectral presheaf $\Sigma$ has no [[global element]]s.

=--




## Contextuality

## References

The original article is

* [[Simon Kochen]] and [[Ernst Specker]], _The problem of hidden variables in quantum mechanics_ , Journal of Mathematics and Mechanics, [pdf](http://www.iumj.indiana.edu/IUMJ/dfulltext.php?year=1968&volume=17&artid=17004).

The sheaf-theoretic interpretation of the theorem was proposed in

* [[Chris Isham]], [[Jeremy Butterfield]], _A topos perspective on the Kochen-Specker theorem: I. Quantum States as Generalized Valuations_ ([arXiv:quant-ph/9803055](http://arxiv.org/abs/quant-ph/9803055))

The formulation in terms of presheaves on the category of commutative sub-algebra of $B(\mathcal{H})$ was proposed in 

* J. Hamilton, [[Chris Isham]], [[Jeremy Butterfield]], _A Topos Perspective on the Kochen-Specker Theorem: III. Von Neumann Algebras as the Base Category_ ([arXiv:quant-ph/9911020](http://arxiv.org/abs/quant-ph/9911020))


The original paper outlining [[Bell's theorem]] is

* J. S. Bell, _On the Einstein Podolsky Rosen Paradox_ , Physics, [pdf](http://www.drchinese.com/David/Bell_Compact.pdf).

The original paper outlining [[Gleason's theorem]] is

* A.M. Gleason, _Measures on the closed subspaces of a Hilbert space_ , Journal of Mathematics and Mechanics, [pdf](http://www.iumj.indiana.edu/IUMJ/FULLTEXT/1957/6/56050).



## Discussion