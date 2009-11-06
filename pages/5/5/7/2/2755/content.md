
#Contents#
* automatic table of contents goes here
{:toc}


#Idea#

One imagines that from a [[quantum field theory]] one can derive a [[classical field theory]] of which the original quantum field theory may be regarded as a [[quantization]].  Whereas quantization may be haphazard, since quantum physics seems to be a more fundamental description of reality that need not be derivable from anything classical, we expect taking the classical limit to be more systematic, since the appearance of a classical world in some regimes should be explicable by fundamental quantum theories.  However, it may not be as systematic as some people would like, as in this [blog discussion](http://golem.ph.utexas.edu/category/2009/10/this_weeks_finds_in_mathematic_43.html#c028689).

What precisely this means and to which degree precisely it makes sense depends on which precise formulation of these concepts one considers. For instance when regarding [[deformation quantization]] as definition the quantum theory then taking the classical limit is an obvious straightforward operation. But in more complete contexts, such as when the [[quantum field theory]] is realized as an [[FQFT]] or [[AQFT]], the passage to the classical limit may be subtle or not make sense at all.

Most prescriptions for taking classical limits are formulated in algebraic settings. To fit for instance a 1-dimensional [[FQFT]] into the discussion one is likely to find in the literature, one will have to encode it equivalently in its [[spectral triple]] (as described there) and then proceed with that.


#Relations to coherent states#

One method for producing [[classical mechanics]] from a quantum theory is by looking at [[coherent state]]s of the quantum theory. The standard (Glauber) coherent states 
have a localized probability distribution in classical [[phase space]] whose center follows the classical equations of motion when the Hamiltonian is quadratic in positions and momenta. 

(For nonquadratic Hamiltonians, this only holds approximately over short times. For example, 
for the 2-body problem with a $1/r^2$ interaction, 
Glauber coherent states are not preserved by the dynamics.
In this particular case, there are, however, alternative SO(2,4)-based coherent states that are preserved by the dynamics, smeared over Kepler-like orbits. The reason is that the Kepler 2-body problem - and its quantum version, the hydrogen atom - are superintegrable systems with the large dynamical symmetry group SO(2,4).)

In general, roughly, coherent states form a nice orbit of unit vectors of a Hilbert space $H$ under a dynamical symmetry group $G$ with a triangular decomposition, such that the linear combinations of coherent states are dense in $H$, and the inner product $\phi^*\psi$ of coherent states $\phi$ and $\psi$ can be calculated explicitly in terms of the highest weight representation theory of $G$. The diagonal of the $N$-th tensor power of $H$ has coherent states $\psi_N$ (labelled by the same classical phase space as the original coherent states, and corresponding to the $N$-fold highest weight) with inner product 

$$
\phi_N^* \psi_N = (\phi^* \psi)^N
$$

and for $N\to \infty$, one gets a good classical limit.
For the Heisenberg group, $\phi^*\psi$ is a $1/\hbar$-th power, 
and the $N$-th power corresponds to replacing $\hbar$ by $\hbar/N$. Thus one gets the standard classical limit.


#References#

Basic literature on relations between [[coherent state]]s and the classical limit, based on irreducible unitary representations of Lie groups includes the book

* A. M. Perelomov, 
Generalized Coherent States and Their Applications, 
Springer Verlag, Berlin, 1986.

and the paper

* L. Yaffe, _Large $N$ limits as classical mechanics_, 
Rev. Mod. Phys. 54, 407--435 (1982)

Both references assume that the Lie group is finite-dimensional and semisimple. This excludes the Heisenberg group, in terms of which the standard (Glauber) coherent states are usually defined. However, the Heisenberg group has a triangular decomposition, and this suffices to apply
Perelomov's theory in spirit. 

The online book

* [[Arnold Neumaier]], [[Dennis Westra]], _Classical and Quantum Mechanics via Lie algebras_ ([arXiv](http://lanl.arxiv.org/abs/0810.1019))

contains a general discussion of the relations between classical mechanics and quantum mechanics, and discusses
in Chapter 16 the concept of a triangular decomposition of Lie algebras and a summary of the associated representation theory (though in its present version not the general relation to coherent states).

For other relevant approaches to a rigorous classical limit, see the online sources

* &lt;http://www.projecteuclid.org/Dienst/Repository/1.0/Disseminate/euclid.cmp/1103859040/body/pdf>

* &lt;http://www.univie.ac.at/nuhag-php/bibtex/open_files/si80_SIMON!!!.pdf>

* &lt;http://arxiv.org/abs/quant-ph/9504016>

* &lt;http://arxiv.org/pdf/math-ph/9807027>


