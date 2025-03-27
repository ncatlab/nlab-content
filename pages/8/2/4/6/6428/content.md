
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
* table of contents
{:toc}

## Idea

For $Conf$ a [[configuration space]] and

$$
  S : Conf \to \mathbb{R}
$$

an [[action functional]] that is invariant under a [[group]] $G$ of symmetries [[action|acting]] on $Conf$, in that

$$
  \forall g \in G, \phi \in Conf : \,\,\, S(g(\phi)) = S(\phi)
$$


a solution $\phi_0$ to the [[Euler-Lagrange equations]] of motion is said to exhibit **spontaneously broken symmetry** if it is not a fixed-point of that group [[action]]: if there is $g \in G$ such that $g(\phi_0) \neq \phi_0$.

The "breaking" refers to the fact that the group no longer acts. It is called "spontaneous" because one imagines that by a physical process the theory "finds" one of its solutions. This comes from the class of examples where a statistical system is first considered at high temperature and then cooled down. At some point it will "spontaneously" freeze in one allowed configuration. A standard example is a [[ferromagnet]]: at high temperature its [[magnetization]] vanishes, while at very low temperature it spontaneously finds a direction of magnetization, thus "breaking" rotational symmetry.

One calls the subgroup $G_{\phi_0} \subset G$ that fixes the given configuration $\phi_0$ the _unbroken symmetry group_ .

In the context of the [[quantum field theory]] arising by [[quantization]] of this action functional one considers the given classical solution $\phi_0$ as a background about which to consider [[perturbation theory|perturbations]] of the remaining [[effective quantum field theory]]. 

The fields in this effective QFT are then small excitations $\delta \phi$ around the given $\phi_0$. Since the original symmetry group still acts on the full fields $\phi_0 + \delta \phi$, the remaining symmetry group of the effective field theory is $G_{\phi_0}$, whose elements $g$ send

$$
  g : (\phi_0 + \delta \phi) \mapsto g(\phi_0) + g(\delta \phi)
  = \phi_0 + g \delta \phi
 \,.
$$

Since in the effective theory around $\phi_0$ the [[vacuum]] state where all the $\delta \phi$ have no excitations (or rather: are in their ground state) corresponds to $\phi_0$ itself one says in this context that _a quantum theory exhibits spontaneouly broken symmetry if its vacuum state is not invariant under the pertinent symmetries_ .

## Formalization in cohesive homotopy-type theory
 {#FormalizaitonInCohesion}

We indicate the formalization of the concept in the axiomatics of [[cohesion]].

Let $\mathbb{G}$ be a cohesive [[abelian infinity-group]] (for instance $\mathbb{G}$ the [[circle group]] $U(1)$ in [[smooth infinity-groupoid|smooth cohesion]]).

Then a [[prequantum line bundle]] on a [[phase space]] $P$ is given by a [[modulating morphism]]

$$
  P \longrightarrow \mathbf{B}\mathbb{G}_{conn}
$$

to the [[moduli stack]] $\mathbf{B}\mathbb{G}_{conn}$ of $\mathbb{G}$-[[principal connections]].

A symmetry of the theory means that there is a cohesive [[infinity-group]] $G$ [[infinity-action|infinity-acting]] on $P$ such that the prequantum bundle descends to the [[homotopy quotient]]

$$
  \array{
     P  &\longrightarrow& \mathbf{B}\mathbb{G}_{conn}
     \\
     \downarrow & \nearrow
     \\
     P/G
   }
$$

Now given an [[infinity-action]] of $\mathbb{G}$ on some $V$ (take $\mathbb{G} = U(1)$ and $V = \mathbb{C}$ for traditional quantum mechanics) then a [[quantum state]] (a [[wavefunction]]) is a [[section]] of the [[associated infinity-bundle]], hence a diagram of the form

$$
   \array{
         P &\stackrel{\Psi}{\longrightarrow}& V/\mathbb{G}
         \\
         \downarrow &\swArrow_{\simeq}& \downarrow
         \\
         \mathbf{B}\mathbb{G}_{conn}
         &\longrightarrow&
         \mathbf{B}\mathbb{G}
    }
$$

So this is something defined on phase space $P$. If that also descends to the [[homotopy quotient]] $P/G$ (this is hard to draw here, but should be clear) then that makes the wavefunction also $G$-equivariant. If not, then the wavefunction $\Psi$ "breaks" the $G$-symmetry.

Now if on top of this we have that the given $\Psi$ is a "ground state", then if it does not descend to the homotopy quotient we say "the $G$-symmetry is spontaneously broken".

To axiomatize what "ground state" means: introduce another $\mathbb{R}$-action on $P$ which is a [[Hamiltonian action]], i.e. with respect to which the prequantum bundle is required to be equivariant. Then ask $\Psi$ to  (be [[polarization|polarized]] and) be a minimal eigenstate of the respective Hamiltonian. That makes it a "ground state".

For more on the general translation between traditional [[geometric quantization]] and [[cohesion|cohesive]] homotopy theory see at _[[schreiber:Higher geometric prequantum theory]]_.

## Examples

### Scalars in mexican hat potential

A standard example which is both very simple but at the same time of central importance in one of the main applications in the [[standard model of particle physics]] -- the [[electroweak symmetry breaking]] via the [[Higgs mechanism]] -- is this:

Let $Conf = C^\infty(X = [0,1]^d, \mathbb{R}^N)$ be the configuration space of $N$ real scalar fields and take the action functional to be

$$
  S : \phi \mapsto \int_X \left( -\frac{1}{2}\vert \nabla \phi \vert^2
  -
  \frac{h}{2} \vert\phi\vert^2 - \frac{g}{4} \vert\phi\vert^4
  \right) d\mu_X
$$

for some $h, g \in \mathbb{R}$. This is manifestly invariant under the canonical action of the [[orthogonal group]] $G = O(N)$ on $Conf$.

This action functional has a class of critical points given by constant maps $\phi : X \to \mathbb{R}^n : \phi(x) = \Phi$. These extremize the [[action functional]] precisely if the $\Phi$ extremize the potential energy

$$
  \frac{h}{2} \vert\phi\vert^2 + \frac{g}{4} \vert\phi\vert^4
  \,.
$$

If both $g$ and $h$ are positive, then there is only one such critical point, given by $\Phi = 0$.  Therefore in this case the unique constant solution does _not_ break the symmetry, in that $g( \Phi = 0) = (\Phi = 0)$ for all $g \in O(N)$.

However, if $h$ is negative and $g$ positive, then the solutions are all those $\Phi$ with

$$
  \vert \Phi \vert^2 = - \frac{h}{g} \gt 0
  \,.
$$

The set of all these is closed under the action of $G = O(N)$ -- this group takes one of these solutions into another -- but none of these solutions is _fixed_ by this action.

One says in this case that any such solution $\phi : x \mapsto \Phi$ is a solution that _spontaneously breaks the symmetry_ of the theory.


### In gravity

The theory of [[gravity]] on a given [[topological manifold]] $X$ has as 
[[configuration space|configurations]] [[pseudo-Riemannian metric]]s on $X$ and its [[action functional]] -- the [[Einstein-Hilbert action]] or one of its variants -- is invariant under the [[action]] of the [[diffeomorphism]] group on $X$.

The corresponding [[Euler-Lagrange equation]]s are _[[Einstein's equations]]_. A given solution $(X,g)$ _breaks_ the symmetry given by a [[diffeomorphism]] $f : X \to X$ unless $f$ is an [[isometry]]. This means that the unbroken symmetries connected to the identity correspond precisely to the [[Killing vector field]]s on $(X,g)$.

#### Kaluza-Klein reductions

Spontaneous symmetry breaking in [[gravity]] plays a central role for instance in the context of the [[Kaluza-Klein mechanism]]. For instance for $dim X = 5$ the [[effective field theory]] of gravity around a solution of the form $(X = X_4 \times S^1, g_4 \otimes g_1)$ is 4-dimensional gravity coupled to [[electromagnetism]] (and a [[dilaton]] field): the components of the field of gravity along the circle transmute into the electromagnetic field. The ansatz _breaks_ all the symmetries that would mix the remaining 4-dimensional gravitational excitations with these new electromagnetic excitations.

This is discussed in a bit of detail for instance in 
([Strominger, lecture 1](#Strominger)).

#### Super Kaluza-Klein reductions

The above discussion has a direct analog in theories of higher 
[[supergravity]]. By the same logic, one finds that the 
[[effective quantum field theory]] around classical solutions that are
[[Kaluza-Klein mechanism|Kaluza-Klein reductions]] of the form 
$(X^4 \times Y^d, (g_4 \otimes g_d))$ exhibits as global symmetries all
those [[diffeomorphism]]s that are not _spontaneously broken_ by this solution.

In this case, though, there are also [[supersymmetry]] analogs of the plain diffeomorphism action. Such a local supersymmetry remains unbroken in the given solution if it comes from a [[Killing spinor field]].

Therefore KK-reductions to 4-dimensional [[Minkowski space]] in supergravity that admit precisely four Killing spinors of the form $(\psi_4 = const \otimes \psi_d = covariantly const)$ give rise to [[effective field theories]] with exactly one remaining global [[supersymmetry]]. See also at _[[supersymmetry breaking]]_.

For more see [[supersymmetry and Calabi-Yau manifolds]].

This is discussed in a bit of detail for instance in 
([Strominger, lecture 2](#Strominger)).

#### Scherk-Schwarz mechanism

Specifically, the _[[Scherk-Schwarz mechanism]]_ ([Scherk-Schwarz 79](#ScherkSchwarz79)) is the [[spontaneously broken symmetry|spontaneous]] [[supersymmetry breaking]] by [[KK-compactification]] on a [[circle]] whose [[spin structure]] imposes anti-periodic [[boundary conditions]] for [[fermion fields]].



## Related concepts

* [[gauge group]]

  * [[global gauge group]], [[local gauge group]]

* [[Goldstone boson]]

* [[QFT with defects|topological defects]] in the [[vacuum]]

  * [[domain wall]], [[cosmic string]], [[monopole]]

* [[enhanced gauge symmetry]]

## References

In 

* [[Steven Weinberg]], _The quantum theory of fields_

sponaneously broken [[global gauge group]] symmetry is discussed in vol I, section 19, and spontaneously broken [[local gauge group]] symmetry in vol I, section 21.4.

Survey:

* Jose Bernabeu, _Symmetries and their breaking in the fundamental laws of physics_ ([arXiv:2006.13996](https://arxiv.org/abs/2006.13996))

* [[Tomáš Brauner]]: *Effective Field Theory for Spontaneously Broken Symmetry*, Lecture Notes in Physics **1023**, Springer (2024) &lbrack;[arXiv:2404.14518](https://arxiv.org/abs/2404.14518), [doi:10.1007/978-3-031-48378-3](https://doi.org/10.1007/978-3-031-48378-3)&rbrack;
  > (perspective of [[effective field theory]])





Textbook discussion of broken symmetry in [[gravity]] and [[supergravity]] in the context of the [[Kaluza-Klein mechanism]] is in

* {#Strominger} [[Andrew Strominger]] (notes by [[John Morgan]]), _Kaluza-Klein compactifications, Supersymmetry and Calabi-Yau spaces_ , volume II, starting on page 1091 in: _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))
 

Discussion of spontaneous [[supersymmetry breaking]] is in 

* Yael Shadmi, _Supersymmetry breaking_ ([arXiv:hep-th/0601076](http://arxiv.org/abs/hep-th/0601076)) 

* [[Joseph Polchinski]], volume II, appendix B of _[[String theory]]_

The article

* [[Klaas Landsman]], Robin Reuvers, _A Flea on Schr&#246;dinger's Cat_,  Found. Phys. 43, 373-407 (2013) ([arXiv:1210.2353](http://arxiv.org/abs/1210.2353), [pdf](http://www.math.ru.nl/~landsman/Catresubmission.pdf))

points out that for symmetric systems with a symmetric ground state, already a tiny perturbation mixing the ground state with the first excited stated causes spontaneous symmetry breaking in the suitable limit, and suggests that this already resolves the [[measurement problem]] in [[quantum mechanics]].




[[!redirects spontaneously broken symmetries]]

[[!redirects spontaneous symmetry breaking]]


[[!redirects broken symmetry]]
[[!redirects broken symmetries]]

[[!redirects symmetry breaking]]