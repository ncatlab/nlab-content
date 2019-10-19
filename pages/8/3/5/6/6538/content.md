__Quantum group Fourier transform__ refers to several variants of Fourier transforms attached to Hopf algebras or their analytic versions. 

The usual Fourier transform is between functions on locally compact abelian group $G$ and functions on its [[Pontrjagin dual]] locally compact abelian group $\hat{G}$ (the group of continuous characters on $G$ with the topology of uniform convergence on compact sets), cf. wikipedia, [Pontrjagin duality](http://en.wikipedia.org/wiki/Pontryagin_duality). 

In noncommutative case, the role of Pontrjagin duality is played by a version of [[Tannaka-Krein theorem|Tannaka-Krein duality]]. 

To avoid analytic details for starters, and still to introduce elements of the general story, one can look at the case when $G$ is finite. Then, over a field $k$, the group Hopf algebra $k \hat{G}$ is isomorphic with the [[dual Hopf algebra]] $(k G)^*$ of the group Hopf algebra $k G$ which is itself isomorphic as a Hopf algebra to the function algebra $k(G)$. The composition is giving the Fourier transform $k \hat{G}\cong k(G)$, which is a linear map from the convolution algebra of $G$ to the function algebra on $G$. In such a situation one has a discrete version of Haar measure. Define 

$$
\mathcal{F}(h)(u) := \sum_{\chi\in \hat{G}} h (\chi)\chi(u)
$$
$$
\mathcal{F}^{-1}(\phi)(\chi) := \frac{1}{|G|}\sum_{u\in G}\chi(u^{-1})\phi(u)
$$
$$
\Lambda = \sum_{u\in G} u \in k G
$$
$$
\Lambda^* = \sum_{\chi} \chi
$$

where one assumes that $|G|$ is invertible in $k$. It holds that

$\chi \Lambda^* = \epsilon(\chi)\Lambda^*$ for all $\chi\in k \hat{G}$ and $\Lambda \phi = \Lambda \epsilon(\phi)$ for all $\phi\in k G$. In other words, $\Lambda$ is a right integral _in_ $k G$ and $\Lambda^*$ is a left integral in $(k G)^*$. 

One can write 

$$
\mathcal{F}(h) = \Lambda_{(1)}\langle h, \Lambda_{(2)}\rangle, 
$$
for $h\in k \hat{G} = (k G)^*$ (notice the usage of left [[coregular action]]) and

$$
\mathcal{F}^{-1}(\phi) = \frac{\Lambda^*_{(1)}\langle \Lambda^*_{(2)},S \phi\rangle}{\langle \Lambda^*, \Lambda \rangle}
$$

for $\phi\in k G$ and where $S: k G\to (k G)^{op,cop}$ is the antipode.
These formulas make sense for more general [[dual bialgebra|Hopf algebras in duality]] provided there are appropriate analogues of $\Lambda$ and $\Lambda^*$ and $\langle \Lambda^*, \Lambda\rangle$ is invertible in $k$. That generalization is called the __quantum group Fourier transform__. 


They can also be related to the [[fundamental operator]] in Hopf algebra $H$, see under [[multiplicative unitary]].

### Literature

* V. Lyubashenko, _Modular transformations and tensor categories_, J. Pure Appl. Algebra __98__ (1995) 279–327 <a href="https://doi.org/10.1016/0022-4049(94)00045-K">doi</a>

> For an abelian tensor category we investigate a Hopf algebra F in it, the “algebra of
functions” or “automorphisms of the identity functor”. We show the existence of the object of integrals for any Hopf algebra in a rigid abelian category. If some assumptions of finiteness and non-degeneracy are satisfied, the Hopf algebra F has an integral and there are morphisms $S, T : F \to F$, called modular transformations. They yield a representation of a modular group. The properties of $S$ are similar to those of the Fourier transform.

* V. Lyubashenko, S. Majid, _Fourier transform identities in quantum mechanics and the quantum line_, Phys. Lett. B284 (1992) 66-70 <a href="https://doi.org/10.1016/0370-2693(92)91926-Z">doi</a>; _Braided groups and quantum Fourier transform_, J. Algebra 166 506-28 [doi](https://doi.org/10.1006/jabr.1994.1165)
* T H Koornwinder, B J Schroers, J K Slingerland, F A Bais, _Fourier transform and the Verlinde formula for the quantum double of a finite group_,  J. Phys. A32: 48 [doi](https://doi.org/10.1088/0305-4470/32/48/313) 
* [[Shahn Majid]], _Foundations of quantum group theory_, 1995, 2nd. ed 2000
* M. Enock, J. M. Schwartz, _Kac algebras and duality of locally compact groups_,  Springer-Verlag, 1992, , x+257 pp. [gBooks](http://books.google.com/books/about/Kac_algebras_and_duality_of_locally_comp.html?id=U6e6aD1gj3oC), [MR94e:46001](http://www.ams.org/mathscinet-getitem?mr=1215933)
* Massoud Amini, _Tannaka&#8211;Krein duality for compact groupoids I, Representation theory_, Advances in Mathematics __214__, n. 1, 2007, 78-91 [doi](http://dx.doi.org/10.1016/j.aim.2006.09.015) 
* Laurent Freidel, [[nlab:Shahn Majid]], _Noncommutative harmonic analysis, sampling theory and the Duflo map in $2+1$ quantum gravity_, Classical Quantum Gravity __25__ (2008), no. 4, 045006 [MR2009f:83058](http://www.ams.org/mathscinet-getitem?mr=2388191), [doi](http://dx.doi.org/10.1088/0264-9381/25/4/045006)
* [[zoranskoda:ncFourier]]
