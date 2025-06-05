

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

****

#### Products
 {#Products}

\begin{proposition}\label{ProductOfGrothendieckToposes}
The [[Cartesian product]] of [[presheaf toposes]] $PSh(C_i)$ in $Topos$ is the presheaf topos on the [[product category]] of their sites:
$$
  PSh(C_1)
  \times_{Topos}
  PSh(C_2)
  \;\simeq\;
  PSh(C_1 \times_{Cat} C_2 )
  \,.
$$
More generally, for $J_i$ a [[Grothendieck topology]] on $C_i$, the product in $Topos$ of the sheaf topos is the sheaf topos over the product site $(C_1 \times C_2, J_1 \times J_2)$, where $J_1 \times J_2$ is the Grothendieck topology on the [[product category]] generated from products of [[covering sieves]] from $J_1$ and $J_2$:
$$
  Sh(C_1, J_1)
  \times_{Topos}
  PSh(C_2, J_2)
  \;\simeq\;
  PSh(C_1 \times C_2,\,  J_1 \times J_2 )
  \,.
$$
\end{proposition}

(cf. [Pitts 1985, proof of Thm. 2.3](#Pitts85), [Valero 2018 p 98-99](#Valero18))


\linebreak

## History

More recently, the S-matrix perspective becomes fashionable also in [[Yang-Mills theory]], with people noticing that [[super Yang-Mills theory]] and [[Tr(ϕ³)]] enjoy good structures in its scattering amplitudes which are essentially invisible in the vast summation of [[Feynman diagrams]] that extract the S-matrix from the [[action functional]]. Instead there are entirely different mathematical structures that encode at least some sub-class of scattering amplitudes (see at _[[amplituhedron]]_ and _[[associahedron]]_). This has lead to increasingly close ties between the S-matrix program and the mathematical fields of [[geometry]] and [[combinatorics]], allowing for the development of various other structures in [[quantum field theory]] that encode, for instance, the [[Wheeler superspace|Wheeler]]-[[wavefunction]] of the [[observable universe|universe]] (see at _[[cosmohedron]]_) and the [[ultraviolet divergence|UV]]/[[infrared divergence|IR]] [[divergent series|divergence]] of [[Feynman integrals]] (see at _[[Feynman polytope]]_). 

****


[[KummerSurfaceProjections.png:file]]
