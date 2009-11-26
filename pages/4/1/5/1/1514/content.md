#Contents#
* automatic table of contents goes here
{:toc}

#Path integral in quantum mechanics#

A simple form of the path integral is realized in [[quantum mechanics]], where it was originally dreamed up by [[Richard Feynman]] and then made precise using the [[Feynman-Kac formula]].

The [[Schrodinger equation|Schrödinger equation]] says that the rate at which the phase of an energy eigenvector rotates is proportional to its energy:
\[ i \hbar \frac{d}{dt} \psi = H \psi. \]
Therefore, the probability that the system evolves to the final state $\psi_F$ after evolving for time $t$ from the initial state $\psi_I$ is
\[ \langle \psi_F|e^{-iHt}|\psi_I\rangle.\]
Chop this up into time steps $\Delta t = t/N$ and use the fact that 
\[\int_{-\infty}^{\infty}|q\rangle\langle q| = 1\]
to get
\[ \langle \psi_F| e^{-iH\Delta t} \left(\int_{-\infty}^{\infty} |q_{N-1} \rangle \langle q_{N-1}| dq_{N-1}\right) e^{-iH\Delta t} \left(\int_{-\infty}^{\infty} |q_{N-2} \rangle \langle q_{N-2}| dq_{N-2}\right) e^{-iH\Delta t} \cdots e^{-iH\Delta t} \left(\int_{-\infty}^{\infty} |q_1 \rangle \langle q_1| dq_1\right) e^{-iH\Delta t} |\psi_I\rangle \]
\[ = \int_{q_1} \cdots \int_{q_{N-2}} \int_{q_{N-1}} \langle \psi_F| e^{-iH\Delta t} |q_{N-1} \rangle \langle q_{N-1}| e^{-iH\Delta t} |q_{N-2} \rangle \langle q_{N-2}|  e^{-iH\Delta t} \cdots e^{-iH\Delta t} |q_1 \rangle \langle q_1| e^{-iH\Delta t} |\psi_I\rangle dq_{N-1} dq_{N-2} \cdots dq_1 \]
Assume we have the free Hamiltonian $H=p^2/2m.$  Looking at an individual term $\langle q_{n+1}| e^{-iH\Delta t} |q_{n} \rangle,$ we can insert a factor of 1 and solve to get
\[ \array{\langle q_{n+1}| e^{-iH\Delta t} \left(\int_{-\infty}^{\infty} \frac{dp}{2\pi}|p\rangle \langle p|\right)|q_{n} \rangle &=& \int_{-\infty}^{\infty} \frac{dp}{2\pi} e^{-ip^2\Delta t/2m} \langle q_{n+1}|p\rangle \langle p|q_{n} \rangle \\ &=& \int_{-\infty}^{\infty} \frac{dp}{2\pi} e^{-ip^2\Delta t/2m} e^{ip(q_{n+1}-q_n)} \\ &=& \left(\frac{-i 2\pi m}{\Delta t}\right)^{\frac{1}{2}} e^{i \Delta t (m/2)[(q_{n+1}-q_n)/\Delta t]^2}.} \]
Defining
\[\int Dq = \lim_{N \to \infty} \left(\frac{-i 2\pi m}{\Delta t}\right)^{\frac{N}{2}} \prod_{n=0}^{N-1} \int dq_n,\]
and letting $\Delta t \to 0, N \to \infty,$ we get
\[ \langle \psi_F|e^{-iHt}|\psi_I\rangle = \int Dq e^{i \int_0^t dt \frac{1}{2}m \dot{q}^2}. \]

For arbitrary Hamiltonians $H = \frac{p^2}{2m} + V(x),$ we get
\[ \array{\langle \psi_F|e^{-iHt}|\psi_I\rangle &=& \int Dq e^{i \int_0^t dt \frac{1}{2}m \dot{q}^2 - V(x)} \\ &=& \int Dq e^{i\int_0^t\mathcal{L}(\dot{q},q) dt} \\ &=& \int Dq e^{iS(q)}, } \]
where $S(q)$ is the [[action]] functional.

+--{.query}
Is there an easy way to see how the Hamiltonian transforms into the Lagrangian in the exponent?
=--

## References ##

For simple systems like particles propagating on a [[Riemannian manifold]] and charged under a [[gauge field]] given by a [[connection on a bundle]] the path integral can be made pretty much rigorous

* [[Christian Baer]], [[Frank Pfaeffle]], _Path integrals on manifolds by finite dimensional approximation_ ([arXiv](http://arxiv.org/abs/math/0703272))

+--{.query}
Zoran: usually the QUADRATIC Hamiltonians are the ones for which the integral is well understood in several approaches; and of course many cases corresponding to the exactly solvable models. 
=--


#The path integral in the bigger picture#

Ours is the age whose central fundamental theoretical physics question is: 

>_What is [[quantum field theory]]_? 

A closely related question is:

> _What is the path integral_ ? 

After its conception by Feynman in the middle of the 20th century It was notably Edward Witten's achievement in the late 20th century to make clear the vast potential for fundamental physics and pure math underlying the concept of the quantum field theoretic path integral.

And yet, among all the aspects of QFT, the notion of the path integral is the one that has resisted attempts at formalization the most.

While [[FQFT|functorial quantum field theory]] is the formalization of the properties that the _locality_ and the _sewing law_ of the path integral is demanded to have -- whatever the path integral is, it is a process that in the end yields a [[functor]] on a [[(infinity,n)-category of cobordisms]] -- by itself, this sheds no light on what that procedure called "path integration" or "path integral quantization" is.

The single major insight into the right [[higher category theory|higher categorical]] formalization of the path integral is probably the idea indicated in

* Dan Freed

  * _Quantum groups from path integrals_ ([arXiv](http://xxx.lanl.gov/abs/q-alg/9501025))

  * _Higher algebraic structures and quantization_ ([arXiv](http://arxiv.org/abs/hep-th/9212115))

which says that

* it is wrong to think of the _action functional_ that the path integral integrates over as just a _function_: it is a higher categorical object;

* accordingly, the path integral is not something that just controls the numbers or linear maps assigned by a $d$-dimensional [[quantum field theory]] in dimension $d$: also the assignment to higher codimensions is to be regarded as part of the path integral;

  * notably: the fact that quantum mechanics assigns a (Hilbert) space of sections of a vector bundle to codimension 1 is to be regarded as due to a _summing operation_ in the sense of the path integral, too: the space of sections of a vector bundle is the continuum equivalent of the direct sum of its fibers


More recently, one sees attempts to formalize this observation of Freed's, notably in the context of the [[cobordism hypothesis]]:

* [[geometric infinity-function theory]] is used to compute at least something like a path integral in codimension 1 and 2 in the context of [[sigma-model]] QFT;

* something not unsimilar is [[schreiber:Nonabelian cocycles and their sigma model QFTs|here]], the underlying idea of which for a toy example is spelled out at

  *[[exercise in groupoidification - the path integral]];

* and something similar or is indicated in section 3 and section 6 of

  * Freed, Hopkins, Lurie, Teleman, _Topological QFT from Compact Lie Groups_ ([arXiv](http://arxiv.org/abs/0905.0731))

based on material (on categories of "families") in _[[On the Classification of Topological Field Theories]]_ . 


